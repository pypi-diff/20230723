# Comparing `tmp/hdmf_zarr-0.2.0.tar.gz` & `tmp/hdmf_zarr-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hdmf_zarr-0.2.0.tar", last modified: Fri Jan  6 16:40:55 2023, max compression
+gzip compressed data, was "hdmf_zarr-0.3.0.tar", last modified: Sun Jul 23 16:51:47 2023, max compression
```

## Comparing `hdmf_zarr-0.2.0.tar` & `hdmf_zarr-0.3.0.tar`

### file list

```diff
@@ -1,36 +1,44 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 16:40:55.565154 hdmf_zarr-0.2.0/
--rw-r--r--   0 runner    (1001) docker     (123)     2412 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)      186 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     4369 2023-01-06 16:40:55.565154 hdmf_zarr-0.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3296 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/README.rst
--rw-r--r--   0 runner    (1001) docker     (123)      287 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      321 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/requirements-dev.txt
--rw-r--r--   0 runner    (1001) docker     (123)      207 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/requirements-doc.txt
--rw-r--r--   0 runner    (1001) docker     (123)      140 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      518 2023-01-06 16:40:55.569154 hdmf_zarr-0.2.0/setup.cfg
--rwxr-xr-x   0 runner    (1001) docker     (123)     2117 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 16:40:55.549154 hdmf_zarr-0.2.0/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 16:40:55.569154 hdmf_zarr-0.2.0/src/hdmf_zarr/
--rw-r--r--   0 runner    (1001) docker     (123)      898 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/src/hdmf_zarr/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2045 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/src/hdmf_zarr/_due.py
--rw-r--r--   0 runner    (1001) docker     (123)      497 2023-01-06 16:40:55.569154 hdmf_zarr-0.2.0/src/hdmf_zarr/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)    54552 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/src/hdmf_zarr/backend.py
--rw-r--r--   0 runner    (1001) docker     (123)     3975 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/src/hdmf_zarr/nwb.py
--rw-r--r--   0 runner    (1001) docker     (123)     9738 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/src/hdmf_zarr/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 16:40:55.565154 hdmf_zarr-0.2.0/src/hdmf_zarr.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4369 2023-01-06 16:40:55.000000 hdmf_zarr-0.2.0/src/hdmf_zarr.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      638 2023-01-06 16:40:55.000000 hdmf_zarr-0.2.0/src/hdmf_zarr.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-01-06 16:40:55.000000 hdmf_zarr-0.2.0/src/hdmf_zarr.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-01-06 16:39:58.000000 hdmf_zarr-0.2.0/src/hdmf_zarr.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      111 2023-01-06 16:40:55.000000 hdmf_zarr-0.2.0/src/hdmf_zarr.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-01-06 16:40:55.000000 hdmf_zarr-0.2.0/src/hdmf_zarr.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5613 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/test.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 16:40:55.565154 hdmf_zarr-0.2.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-01-06 16:40:55.565154 hdmf_zarr-0.2.0/tests/unit/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/tests/unit/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    20820 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/tests/unit/test_io_convert.py
--rw-r--r--   0 runner    (1001) docker     (123)    70010 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/tests/unit/test_io_zarr.py
--rw-r--r--   0 runner    (1001) docker     (123)    21436 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/tests/unit/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     4617 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/tox.ini
--rw-r--r--   0 runner    (1001) docker     (123)    71305 2023-01-06 16:39:35.000000 hdmf_zarr-0.2.0/versioneer.py
+drwxr-xr-x   0 mavaylon   (501) staff       (20)        0 2023-07-23 16:51:47.739394 hdmf_zarr-0.3.0/
+-rw-r--r--   0 mavaylon   (501) staff       (20)     2412 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/LICENSE.txt
+-rw-r--r--   0 mavaylon   (501) staff       (20)      186 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/MANIFEST.in
+-rw-r--r--   0 mavaylon   (501) staff       (20)     4421 2023-07-23 16:51:47.739556 hdmf_zarr-0.3.0/PKG-INFO
+-rw-r--r--   0 mavaylon   (501) staff       (20)     3297 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/README.rst
+-rw-r--r--   0 mavaylon   (501) staff       (20)      287 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/pyproject.toml
+-rw-r--r--   0 mavaylon   (501) staff       (20)      305 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/requirements-dev.txt
+-rw-r--r--   0 mavaylon   (501) staff       (20)      207 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/requirements-doc.txt
+-rw-r--r--   0 mavaylon   (501) staff       (20)      156 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/requirements.txt
+-rw-r--r--   0 mavaylon   (501) staff       (20)      518 2023-07-23 16:51:47.740332 hdmf_zarr-0.3.0/setup.cfg
+-rwxr-xr-x   0 mavaylon   (501) staff       (20)     2181 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/setup.py
+drwxr-xr-x   0 mavaylon   (501) staff       (20)        0 2023-07-23 16:51:47.709381 hdmf_zarr-0.3.0/src/
+drwxr-xr-x   0 mavaylon   (501) staff       (20)        0 2023-07-23 16:51:47.740760 hdmf_zarr-0.3.0/src/hdmf_zarr/
+-rw-r--r--   0 mavaylon   (501) staff       (20)      898 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/src/hdmf_zarr/__init__.py
+-rw-r--r--   0 mavaylon   (501) staff       (20)     2045 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/src/hdmf_zarr/_due.py
+-rw-r--r--   0 mavaylon   (501) staff       (20)      497 2023-07-23 16:51:47.740865 hdmf_zarr-0.3.0/src/hdmf_zarr/_version.py
+-rw-r--r--   0 mavaylon   (501) staff       (20)    55949 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/src/hdmf_zarr/backend.py
+-rw-r--r--   0 mavaylon   (501) staff       (20)     3440 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/src/hdmf_zarr/nwb.py
+-rw-r--r--   0 mavaylon   (501) staff       (20)     9738 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/src/hdmf_zarr/utils.py
+drwxr-xr-x   0 mavaylon   (501) staff       (20)        0 2023-07-23 16:51:47.727020 hdmf_zarr-0.3.0/src/hdmf_zarr.egg-info/
+-rw-r--r--   0 mavaylon   (501) staff       (20)     4421 2023-07-23 16:51:47.000000 hdmf_zarr-0.3.0/src/hdmf_zarr.egg-info/PKG-INFO
+-rw-r--r--   0 mavaylon   (501) staff       (20)      980 2023-07-23 16:51:47.000000 hdmf_zarr-0.3.0/src/hdmf_zarr.egg-info/SOURCES.txt
+-rw-r--r--   0 mavaylon   (501) staff       (20)        1 2023-07-23 16:51:47.000000 hdmf_zarr-0.3.0/src/hdmf_zarr.egg-info/dependency_links.txt
+-rw-r--r--   0 mavaylon   (501) staff       (20)        1 2023-07-21 22:19:39.000000 hdmf_zarr-0.3.0/src/hdmf_zarr.egg-info/not-zip-safe
+-rw-r--r--   0 mavaylon   (501) staff       (20)      111 2023-07-23 16:51:47.000000 hdmf_zarr-0.3.0/src/hdmf_zarr.egg-info/requires.txt
+-rw-r--r--   0 mavaylon   (501) staff       (20)       10 2023-07-23 16:51:47.000000 hdmf_zarr-0.3.0/src/hdmf_zarr.egg-info/top_level.txt
+drwxr-xr-x   0 mavaylon   (501) staff       (20)        0 2023-07-23 16:51:47.727433 hdmf_zarr-0.3.0/tests/
+-rw-r--r--   0 mavaylon   (501) staff       (20)        0 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/tests/__init__.py
+drwxr-xr-x   0 mavaylon   (501) staff       (20)        0 2023-07-23 16:51:47.728016 hdmf_zarr-0.3.0/tests/__pycache__/
+-rw-r--r--   0 mavaylon   (501) staff       (20)      157 2023-07-22 00:39:45.000000 hdmf_zarr-0.3.0/tests/__pycache__/__init__.cpython-39.pyc
+drwxr-xr-x   0 mavaylon   (501) staff       (20)        0 2023-07-23 16:51:47.732357 hdmf_zarr-0.3.0/tests/unit/
+-rw-r--r--   0 mavaylon   (501) staff       (20)        0 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/tests/unit/__init__.py
+drwxr-xr-x   0 mavaylon   (501) staff       (20)        0 2023-07-23 16:51:47.737896 hdmf_zarr-0.3.0/tests/unit/__pycache__/
+-rw-r--r--   0 mavaylon   (501) staff       (20)      162 2023-07-22 00:39:45.000000 hdmf_zarr-0.3.0/tests/unit/__pycache__/__init__.cpython-39.pyc
+-rw-r--r--   0 mavaylon   (501) staff       (20)    50961 2023-07-22 00:40:15.000000 hdmf_zarr-0.3.0/tests/unit/__pycache__/base_tests_zarrio.cpython-39.pyc
+-rw-r--r--   0 mavaylon   (501) staff       (20)    17814 2023-07-22 00:39:45.000000 hdmf_zarr-0.3.0/tests/unit/__pycache__/test_io_convert.cpython-39-pytest-7.1.2.pyc
+-rw-r--r--   0 mavaylon   (501) staff       (20)     6444 2023-07-22 00:40:15.000000 hdmf_zarr-0.3.0/tests/unit/__pycache__/test_zarrio.cpython-39-pytest-7.1.2.pyc
+-rw-r--r--   0 mavaylon   (501) staff       (20)    20248 2023-07-22 00:40:15.000000 hdmf_zarr-0.3.0/tests/unit/__pycache__/utils.cpython-39.pyc
+-rw-r--r--   0 mavaylon   (501) staff       (20)    75762 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/tests/unit/base_tests_zarrio.py
+-rw-r--r--   0 mavaylon   (501) staff       (20)    29053 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/tests/unit/test_io_convert.py
+-rw-r--r--   0 mavaylon   (501) staff       (20)     4529 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/tests/unit/test_zarrio.py
+-rw-r--r--   0 mavaylon   (501) staff       (20)    21436 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/tests/unit/utils.py
+-rw-r--r--   0 mavaylon   (501) staff       (20)     4922 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/tox.ini
+-rw-r--r--   0 mavaylon   (501) staff       (20)    71305 2023-07-21 22:18:19.000000 hdmf_zarr-0.3.0/versioneer.py
```

### Comparing `hdmf_zarr-0.2.0/LICENSE.txt` & `hdmf_zarr-0.3.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `hdmf_zarr-0.2.0/PKG-INFO` & `hdmf_zarr-0.3.0/src/hdmf_zarr.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,42 +1,43 @@
 Metadata-Version: 2.1
-Name: hdmf_zarr
-Version: 0.2.0
+Name: hdmf-zarr
+Version: 0.3.0
 Summary: A package defining a Zarr I/O backend for HDMF
 Home-page: https://github.com/hdmf-dev/hdmf-zarr
 Author: Oliver Ruebel
 Author-email: oruebel@lbl.gov
 License: BSD
 Keywords: python Zarr cross-platform open-data data-format open-source open-science reproducible-research
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: MacOS
 Classifier: Operating System :: Unix
 Classifier: Topic :: Scientific/Engineering :: Medical Science Apps.
 Requires-Python: >=3.7
 Description-Content-Type: text/x-rst; charset=UTF-8
 License-File: LICENSE.txt
 
 .. image:: docs/source/figures/logo_hdmf_zarr.png
      :width: 400
-     
+
 hdmf-zarr
 =========
 
 The ``hdmf-zarr`` library implements a Zarr backend for HDMF as well as convenience classes for integration of Zarr with PyNWB to support writing of NWB files to Zarr.
 
-The Zarr backend is currently experimental and may still change. See the `overiew page <https://hdmf-zarr.readthedocs.io/en/latest/overview.html>`_ for an overview of the available features and known limitations of hdmf-zarr. 
+**Status:** The Zarr backend is **under development** and may still change. See the `overiew page <https://hdmf-zarr.readthedocs.io/en/latest/overview.html>`_ for an overview of the available features and known limitations of hdmf-zarr.
 
 
 Latest Release
 --------------
 
 .. image:: https://readthedocs.org/projects/hdmf-zarr/badge/?version=latest
      :target: https://hdmf-zarr.readthedocs.io/en/latest/?badge=latest
@@ -58,15 +59,15 @@
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/run_all_tests.yml
 
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/Check%20Sphinx%20external%20links/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/check_external_links.yml
 
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/Deploy%20release/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/deploy_release.yml
-    
+
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/black/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/black.yml
 
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/Run%20style%20check/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/run_flake8.yml
```

### Comparing `hdmf_zarr-0.2.0/README.rst` & `hdmf_zarr-0.3.0/README.rst`

 * *Files 9% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 .. image:: docs/source/figures/logo_hdmf_zarr.png
      :width: 400
-     
+
 hdmf-zarr
 =========
 
 The ``hdmf-zarr`` library implements a Zarr backend for HDMF as well as convenience classes for integration of Zarr with PyNWB to support writing of NWB files to Zarr.
 
-The Zarr backend is currently experimental and may still change. See the `overiew page <https://hdmf-zarr.readthedocs.io/en/latest/overview.html>`_ for an overview of the available features and known limitations of hdmf-zarr. 
+**Status:** The Zarr backend is **under development** and may still change. See the `overiew page <https://hdmf-zarr.readthedocs.io/en/latest/overview.html>`_ for an overview of the available features and known limitations of hdmf-zarr.
 
 
 Latest Release
 --------------
 
 .. image:: https://readthedocs.org/projects/hdmf-zarr/badge/?version=latest
      :target: https://hdmf-zarr.readthedocs.io/en/latest/?badge=latest
@@ -32,15 +32,15 @@
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/run_all_tests.yml
 
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/Check%20Sphinx%20external%20links/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/check_external_links.yml
 
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/Deploy%20release/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/deploy_release.yml
-    
+
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/black/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/black.yml
 
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/Run%20style%20check/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/run_flake8.yml
```

### Comparing `hdmf_zarr-0.2.0/setup.cfg` & `hdmf_zarr-0.3.0/setup.cfg`

 * *Files identical despite different names*

### Comparing `hdmf_zarr-0.2.0/setup.py` & `hdmf_zarr-0.3.0/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -13,20 +13,20 @@
     readme = fp.read()
 
 pkgs = find_packages('src', exclude=['data'])
 print('found these packages:', pkgs)
 
 
 reqs = [
-    'hdmf>=3.4.0',
+    'hdmf==3.5.4',  # temporary
     'zarr>=2.11.0',
+    'numpy>=1.22, <1.24; python_version>"3.7"',
     'numcodecs>=0.9.1',
-    'pynwb>=2.0.0',
+    'pynwb>=2.3.2',
     'setuptools',
-    'numpy>=1.22, <1.24; python_version>"3.7"'
 ]
 
 print(reqs)
 
 setup_args = {
     'name': 'hdmf_zarr',
     'version': versioneer.get_version(),
@@ -45,14 +45,15 @@
     'python_requires': '>=3.7',
     'classifiers': [
         "Programming Language :: Python",
         "Programming Language :: Python :: 3.7",
         "Programming Language :: Python :: 3.8",
         "Programming Language :: Python :: 3.9",
         "Programming Language :: Python :: 3.10",
+        "Programming Language :: Python :: 3.11",
         "License :: OSI Approved :: BSD License",
         "Development Status :: 5 - Production/Stable",
         "Intended Audience :: Developers",
         "Intended Audience :: Science/Research",
         "Operating System :: Microsoft :: Windows",
         "Operating System :: MacOS",
         "Operating System :: Unix",
```

### Comparing `hdmf_zarr-0.2.0/src/hdmf_zarr/__init__.py` & `hdmf_zarr-0.3.0/src/hdmf_zarr/__init__.py`

 * *Files identical despite different names*

### Comparing `hdmf_zarr-0.2.0/src/hdmf_zarr/_due.py` & `hdmf_zarr-0.3.0/src/hdmf_zarr/_due.py`

 * *Files identical despite different names*

### Comparing `hdmf_zarr-0.2.0/src/hdmf_zarr/backend.py` & `hdmf_zarr-0.3.0/src/hdmf_zarr/backend.py`

 * *Files 2% similar despite different names*

```diff
@@ -8,14 +8,17 @@
 import tempfile
 import logging
 
 # Zarr imports
 import zarr
 from zarr.hierarchy import Group
 from zarr.core import Array
+from zarr.storage import (DirectoryStore,
+                          TempStore,
+                          NestedDirectoryStore)
 import numcodecs
 
 # HDMF-ZARR imports
 from .utils import (ZarrDataIO,
                     ZarrReference,
                     ZarrSpecWriter,
                     ZarrSpecReader,
@@ -44,20 +47,49 @@
                        DtypeSpec,
                        NamespaceCatalog)
 from hdmf.query import HDMFDataset
 from hdmf.container import Container
 
 # Module variables
 ROOT_NAME = 'root'
+"""
+Name of the root builder for read/write
+"""
+
 SPEC_LOC_ATTR = '.specloc'
+"""
+Reserved attribute storing the path to the Group where the schema for the file are cached
+"""
+
+DEFAULT_SPEC_LOC_DIR = 'specifications'
+"""
+Default name of the group where specifications should be cached
+"""
+
+SUPPORTED_ZARR_STORES = (DirectoryStore,
+                         TempStore,
+                         NestedDirectoryStore)
+"""
+Tuple listing all Zarr storage backends supported by ZarrIO
+"""
 
 
 class ZarrIO(HDMFIO):
 
-    @docval({'name': 'path', 'type': str, 'doc': 'the path to the Zarr file'},
+    @staticmethod
+    def can_read(path):
+        try:
+            zarr.open(path, mode="r")
+            return True
+        except Exception:
+            return False
+
+    @docval({'name': 'path',
+             'type': (str, *SUPPORTED_ZARR_STORES),
+             'doc': 'the path to the Zarr file or a supported Zarr store'},
             {'name': 'manager', 'type': BuildManager, 'doc': 'the BuildManager to use for I/O', 'default': None},
             {'name': 'mode', 'type': str,
              'doc': 'the mode to open the Zarr file with, one of ("w", "r", "r+", "a", "w-")'},
             {'name': 'synchronizer', 'type': (zarr.ProcessSynchronizer, zarr.ThreadSynchronizer, bool),
              'doc': 'Zarr synchronizer to use for parallel I/O. If set to True a ProcessSynchronizer is used.',
              'default': None},
             {'name': 'object_codec_class', 'type': None,
@@ -82,54 +114,65 @@
         self.__path = path
         self.__file = None
         self.__built = dict()
         self._written_builders = WriteStatusTracker()  # track which builders were written (or read) by this IO object
         self.__dci_queue = ZarrIODataChunkIteratorQueue()  # a queue of DataChunkIterators that need to be exhausted
         # Codec class to be used. Alternates, e.g., =numcodecs.JSON
         self.__codec_cls = numcodecs.pickles.Pickle if object_codec_class is None else object_codec_class
-        super().__init__(manager, source=path)
-        warn_msg = ("The ZarrIO backend is experimental. It is under active development. "
-                    "The ZarrIO backend may change any time and backward compatibility is not guaranteed.")
-        warnings.warn(warn_msg)
+        source_path = self.__path
+        if isinstance(self.__path, SUPPORTED_ZARR_STORES):
+            source_path = self.__path.path
+        super().__init__(manager, source=source_path)
+
+    @property
+    def file(self):
+        """
+        The Zarr zarr.hierarchy.Group (or zarr.core.Array) opened by the backend.
+        May be None in case open has not been called yet, e.g., if no data has been
+        read or written yet via this instance.
+        """
+        return self.__file
 
     @property
     def path(self):
         """The path to the Zarr file as set by the use"""
         return self.__path
 
     @property
     def abspath(self):
         """The absolute path to the Zarr file"""
-        return os.path.abspath(self.path)
+        return os.path.abspath(self.source)
 
     @property
     def synchronizer(self):
         return self.__synchronizer
 
     @property
     def object_codec_class(self):
         return self.__codec_cls
 
     def open(self):
         """Open the Zarr file"""
         if self.__file is None:
-            self.__file = zarr.open(store=self.__path,
+            self.__file = zarr.open(store=self.path,
                                     mode=self.__mode,
                                     synchronizer=self.__synchronizer)
 
     def close(self):
         """Close the Zarr file"""
         self.__file = None
         return
 
     @classmethod
     @docval({'name': 'namespace_catalog',
              'type': (NamespaceCatalog, TypeMap),
              'doc': 'the NamespaceCatalog or TypeMap to load namespaces into'},
-            {'name': 'path', 'type': str, 'doc': 'the path to the Zarr file'},
+            {'name': 'path',
+             'type': (str, *SUPPORTED_ZARR_STORES),
+             'doc': 'the path to the Zarr file or a supported Zarr store'},
             {'name': 'namespaces', 'type': list, 'doc': 'the namespaces to load', 'default': None})
     def load_namespaces(cls, namespace_catalog, path, namespaces=None):
         '''
         Load cached namespaces from a file.
         '''
         f = zarr.open(path, 'r')
         if SPEC_LOC_ATTR not in f.attrs:
@@ -164,15 +207,15 @@
     def __cache_spec(self):
         """Interanl function used to cache the spec in the current file"""
         ref = self.__file.attrs.get(SPEC_LOC_ATTR)
         spec_group = None
         if ref is not None:
             spec_group = self.__file[ref]
         else:
-            path = 'specifications'  # do something to figure out where the specifications should go
+            path = DEFAULT_SPEC_LOC_DIR  # do something to figure out where the specifications should go
             spec_group = self.__file.require_group(path)
             self.__file.attrs[SPEC_LOC_ATTR] = path
         ns_catalog = self.manager.namespace_catalog
         for ns_name in ns_catalog.namespaces:
             ns_builder = NamespaceToBuilderHelper.convert_namespace(ns_catalog, ns_name)
             namespace = ns_catalog.get_namespace(ns_name)
             if namespace.version is None:
@@ -218,32 +261,33 @@
         :type check_on_disk: bool
         :return: True if the builder is found in self._written_builders using the builder ID, False otherwise. If
                  check_on_disk is enabled then the function cals get_builder_exists_on_disk in addtion to verify
                  that the builder has indeed been written to disk.
         """
         written = self._written_builders.get_written(builder)
         if written and check_on_disk:
-            written = written and self.get_builder_exists_on_disk(builder=builder, filepath=self.__path)
+            written = written and self.get_builder_exists_on_disk(builder=builder)
         return written
 
-    @docval({'name': 'builder', 'type': Builder, 'doc': 'The builder of interest'},
-            {'name': 'filepath', 'type': str,
-             'doc': 'The path to the Zarr file or None for this file', 'default': None})
+    @docval({'name': 'builder', 'type': Builder, 'doc': 'The builder of interest'})
     def get_builder_exists_on_disk(self, **kwargs):
-        """Convenience function to check whether a given builder exists on disk"""
-        builder_path = self.get_builder_disk_path(**kwargs)
+        """
+        Convenience function to check whether a given builder exists on disk in this Zarr file.
+        """
+        builder = getargs('builder', kwargs)
+        builder_path = self.get_builder_disk_path(builder=builder, filepath=None)
         exists_on_disk = os.path.exists(builder_path)
         return exists_on_disk
 
     @docval({'name': 'builder', 'type': Builder, 'doc': 'The builder of interest'},
             {'name': 'filepath', 'type': str,
              'doc': 'The path to the Zarr file or None for this file', 'default': None})
     def get_builder_disk_path(self, **kwargs):
         builder, filepath = getargs('builder', 'filepath', kwargs)
-        basepath = filepath if filepath is not None else self.__path
+        basepath = filepath if filepath is not None else self.source
         builder_path = os.path.join(basepath, self.__get_path(builder).lstrip("/"))
         return builder_path
 
     @docval({'name': 'builder', 'type': GroupBuilder, 'doc': 'the GroupBuilder object representing the NWBFile'},
             {'name': 'link_data', 'type': bool,
              'doc': 'If not specified otherwise link (True) or copy (False) Zarr Datasets', 'default': True},
             {'name': 'exhaust_dci', 'type': bool,
@@ -457,27 +501,43 @@
     def __resolve_ref(self, zarr_ref):
         """
         Get the full path to the object linked to by the zarr reference
 
         The function only constructs the links to the targe object, but it does not check if the object exists
 
         :param zarr_ref: Dict with `source` and `path` keys or a `ZarrRefernce` object
-        :return: Full path to the linked object
+        :return: 1) name of the target object
+                 2) the target zarr object within the target file
         """
         # Extract the path as defined in the zarr_ref object
         if zarr_ref.get('source', None) is None:
-            ref_path = str(zarr_ref['path'])
-        elif zarr_ref.get('path', None) is None:
-            ref_path = str(zarr_ref['source'])
+            source_file = str(zarr_ref['path'])
+        else:
+            source_file = str(zarr_ref['source'])
+        # Resolve the path relative to the current file
+        source_file = os.path.abspath(os.path.join(self.source, source_file))
+        object_path = zarr_ref.get('path', None)
+        # full_path = None
+        # if os.path.isdir(source_file):
+        #    if object_path is not None:
+        #        full_path = os.path.join(source_file, object_path.lstrip('/'))
+        #    else:
+        #        full_path = source_file
+        if object_path:
+            target_name = os.path.basename(object_path)
         else:
-            ref_path = os.path.join(zarr_ref['source'], zarr_ref['path'].lstrip("/"))
-        # Make the path relative to the current file
-        ref_path = os.path.abspath(os.path.join(self.path, ref_path))
+            target_name = ROOT_NAME
+        target_zarr_obj = zarr.open(source_file, mode='r')
+        if object_path is not None:
+            try:
+                target_zarr_obj = target_zarr_obj[object_path]
+            except Exception:
+                raise ValueError("Found bad link to object %s in file %s" % (object_path, source_file))
         # Return the create path
-        return ref_path
+        return target_name, target_zarr_obj
 
     def __get_ref(self, ref_object):
         """
         Create a ZarrReference object that points to the given container
 
         :param ref_object: the object to be referenced
         :type ref_object: Builder, Container, ReferenceBuilder
@@ -501,15 +561,15 @@
         # if isinstance(ref_object, RegionBuilder):
         #    region = ref_object.region
 
         # by checking os.isdir makes sure we have a valid link path to a dir for Zarr. For conversion
         # between backends a user should always use export which takes care of creating a clean set of builders.
         source = (builder.source
                   if (builder.source is not None and os.path.isdir(builder.source))
-                  else self.__path)
+                  else self.source)
         # Make the source relative to the current file
         source = os.path.relpath(os.path.abspath(source), start=self.abspath)
         # Return the ZarrReference object
         return ZarrReference(source, path)
 
     def __add_link__(self, parent, target_source, target_path, link_name):
         """
@@ -614,14 +674,15 @@
             else:
                 io_settings['dtype'] = data.dtype
             if isinstance(io_settings['dtype'], str):
                 # map to real dtype if we were given a string
                 io_settings['dtype'] = cls.__dtypes.get(io_settings['dtype'])
         try:
             dset = parent.create_dataset(name, **io_settings)
+            dset.attrs['zarr_dtype'] = np.dtype(io_settings['dtype']).str
         except Exception as exc:
             raise Exception("Could not create dataset %s in %s" % (name, parent.name)) from exc
         return dset
 
     @docval({'name': 'parent', 'type': Group, 'doc': 'the parent Zarr object'},  # noqa: C901
             {'name': 'builder', 'type': DatasetBuilder, 'doc': 'the DatasetBuilder to write'},
             {'name': 'link_data', 'type': bool,
@@ -994,15 +1055,15 @@
             return ret
 
         if name is None:
             name = str(os.path.basename(zarr_obj.name))
 
         # Create the GroupBuilder
         attributes = self.__read_attrs(zarr_obj)
-        ret = GroupBuilder(name=name, source=self.__path, attributes=attributes)
+        ret = GroupBuilder(name=name, source=self.source, attributes=attributes)
         ret.location = self.get_zarr_parent_path(zarr_obj)
 
         # read sub groups
         for sub_name, sub_group in zarr_obj.groups():
             sub_builder = self.__read_group(sub_group, sub_name)
             ret.set_group(sub_builder)
 
@@ -1027,43 +1088,45 @@
         :type parent: GroupBuilder
         """
         # read links
         if 'zarr_link' in zarr_obj.attrs:
             links = zarr_obj.attrs['zarr_link']
             for link in links:
                 link_name = link['name']
-                l_path = self.__resolve_ref(link)
-                if not os.path.exists(l_path):
-                    raise ValueError("Found bad link %s in %s in file %s to %s" %
-                                     (link_name, self.__get_path(parent), self.__path, l_path))
-                target_name = str(os.path.basename(l_path))
-                target_zarr_obj = zarr.open(l_path, mode='r')
+                target_name, target_zarr_obj = self.__resolve_ref(link)
                 # NOTE: __read_group and __read_dataset return the cached builders if the target has already been built
                 if isinstance(target_zarr_obj, Group):
                     builder = self.__read_group(target_zarr_obj, target_name)
                 else:
                     builder = self.__read_dataset(target_zarr_obj, target_name)
-                link_builder = LinkBuilder(builder=builder, name=link_name, source=self.__path)
+                link_builder = LinkBuilder(builder=builder, name=link_name, source=self.source)
                 link_builder.location = os.path.join(parent.location, parent.name)
                 self._written_builders.set_written(link_builder)  # record that the builder has been written
                 parent.set_link(link_builder)
 
     def __read_dataset(self, zarr_obj, name):
         ret = self.__get_built(zarr_obj)
         if ret is not None:
             return ret
 
-        if 'zarr_dtype' not in zarr_obj.attrs:
+        if 'zarr_dtype' in zarr_obj.attrs:
+            zarr_dtype = zarr_obj.attrs['zarr_dtype']
+        elif hasattr(zarr_obj, 'dtype'):   # Fallback for invalid files that are mssing zarr_type
+            zarr_dtype = zarr_obj.dtype
+            warnings.warn(
+                "Inferred dtype from zarr type. Dataset missing zarr_dtype: " + str(name) + "   " + str(zarr_obj)
+            )
+        else:
             raise ValueError("Dataset missing zarr_dtype: " + str(name) + "   " + str(zarr_obj))
 
         kwargs = {"attributes": self.__read_attrs(zarr_obj),
-                  "dtype": zarr_obj.attrs['zarr_dtype'],
+                  "dtype": zarr_dtype,
                   "maxshape": zarr_obj.shape,
                   "chunks": not (zarr_obj.shape == zarr_obj.chunks),
-                  "source": self.__path}
+                  "source": self.source}
         dtype = kwargs['dtype']
 
         # By default, use the zarr.core.Array as data for lazy data load
         data = zarr_obj
 
         # Read scalar dataset
         if dtype == 'scalar':
@@ -1132,21 +1195,15 @@
             elif reg_refs:
                 reg_pos.append(list(c))
 
         for p in obj_pos:
             o = data
             for i in p:
                 o = o[i]
-            path = self.__resolve_ref(o)
-            if not os.path.exists(path):
-                raise ValueError("Found bad link in dataset to %s" % (path))
-
-            target_name = os.path.basename(path)
-            target_zarr_obj = zarr.open(path, mode='r')
-
+            target_name, target_zarr_obj = self.__resolve_ref(o)
             o = data
             for i in range(0, len(p)-1):
                 o = data[p[i]]
             if isinstance(target_zarr_obj, zarr.hierarchy.Group):
                 o[p[-1]] = self.__read_group(target_zarr_obj, target_name)
             else:
                 o[p[-1]] = self.__read_dataset(target_zarr_obj, target_name)
@@ -1155,20 +1212,15 @@
         ret = dict()
         for k in zarr_obj.attrs.keys():
             if k not in self.__reserve_attribute:
                 v = zarr_obj.attrs[k]
                 if isinstance(v, dict) and 'zarr_dtype' in v:
                     # TODO Is this the correct way to resolve references?
                     if v['zarr_dtype'] == 'object':
-                        path = self.__resolve_ref(v['value'])
-                        if not os.path.exists(path):
-                            raise ValueError("Found bad link in attribute to %s" % (path))
-
-                        target_name = str(os.path.basename(path))
-                        target_zarr_obj = zarr.open(str(path), mode='r')
+                        target_name, target_zarr_obj = self.__resolve_ref(v['value'])
                         if isinstance(target_zarr_obj, zarr.hierarchy.Group):
                             ret[k] = self.__read_group(target_zarr_obj, target_name)
                         else:
                             ret[k] = self.__read_dataset(target_zarr_obj, target_name)
                     # TODO Need to implement region references for attributes
                     elif v['zarr_dtype'] == 'region':
                         raise NotImplementedError("Read of region references from attributes not implemented in ZarrIO")
```

### Comparing `hdmf_zarr-0.2.0/src/hdmf_zarr/nwb.py` & `hdmf_zarr-0.3.0/src/hdmf_zarr/nwb.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,42 +1,34 @@
 """Module with Zarr backend for NWB for integration with PyNWB"""
 from warnings import warn
 from .backend import ZarrIO
-import zarr
 
 from hdmf.utils import (docval,
-                        popargs)
+                        popargs,
+                        get_docval)
 from hdmf.backends.io import HDMFIO
 from hdmf.build import (BuildManager,
                         TypeMap)
 try:
     from pynwb import get_manager, get_type_map
 
     class NWBZarrIO(ZarrIO):
         """
         IO backend for PyNWB for writing NWB files
 
-        This class is similar to the NWBHDF5IO class in PyNWB. The main purpose of this class
+        This class is similar to the :py:class:`~pynwb.NWBHDF5IO` class in PyNWB. The main purpose of this class
         is to perform default setup for BuildManager, loading or namespaces etc., in the context
         of the NWB format.
         """
-
-        @docval({'name': 'path', 'type': str, 'doc': 'the path to the Zarr file'},
-                {'name': 'mode', 'type': str,
-                 'doc': 'the mode to open the Zarr file with, one of ("w", "r", "r+", "a", "w-")'},
+        @docval(*get_docval(ZarrIO.__init__),
                 {'name': 'load_namespaces', 'type': bool,
                  'doc': 'whether or not to load cached namespaces from given path - not applicable in write mode',
                  'default': False},
-                {'name': 'manager', 'type': BuildManager, 'doc': 'the BuildManager to use for I/O',
-                 'default': None},
                 {'name': 'extensions', 'type': (str, TypeMap, list),
                  'doc': 'a path to a namespace, a TypeMap, or a list consisting paths  to namespaces and TypeMaps',
-                 'default': None},
-                {'name': 'synchronizer', 'type': (zarr.ProcessSynchronizer, zarr.ThreadSynchronizer, bool),
-                 'doc': 'Zarr synchronizer to use for parallel I/O. If set to True a ProcessSynchronizer is used.',
                  'default': None})
         def __init__(self, **kwargs):
             path, mode, manager, extensions, load_namespaces, synchronizer = \
                 popargs('path', 'mode', 'manager', 'extensions',
                         'load_namespaces', 'synchronizer', kwargs)
             if load_namespaces:
                 if manager is not None:
```

### Comparing `hdmf_zarr-0.2.0/src/hdmf_zarr/utils.py` & `hdmf_zarr-0.3.0/src/hdmf_zarr/utils.py`

 * *Files identical despite different names*

### Comparing `hdmf_zarr-0.2.0/src/hdmf_zarr.egg-info/PKG-INFO` & `hdmf_zarr-0.3.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,42 +1,43 @@
 Metadata-Version: 2.1
-Name: hdmf-zarr
-Version: 0.2.0
+Name: hdmf_zarr
+Version: 0.3.0
 Summary: A package defining a Zarr I/O backend for HDMF
 Home-page: https://github.com/hdmf-dev/hdmf-zarr
 Author: Oliver Ruebel
 Author-email: oruebel@lbl.gov
 License: BSD
 Keywords: python Zarr cross-platform open-data data-format open-source open-science reproducible-research
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: MacOS
 Classifier: Operating System :: Unix
 Classifier: Topic :: Scientific/Engineering :: Medical Science Apps.
 Requires-Python: >=3.7
 Description-Content-Type: text/x-rst; charset=UTF-8
 License-File: LICENSE.txt
 
 .. image:: docs/source/figures/logo_hdmf_zarr.png
      :width: 400
-     
+
 hdmf-zarr
 =========
 
 The ``hdmf-zarr`` library implements a Zarr backend for HDMF as well as convenience classes for integration of Zarr with PyNWB to support writing of NWB files to Zarr.
 
-The Zarr backend is currently experimental and may still change. See the `overiew page <https://hdmf-zarr.readthedocs.io/en/latest/overview.html>`_ for an overview of the available features and known limitations of hdmf-zarr. 
+**Status:** The Zarr backend is **under development** and may still change. See the `overiew page <https://hdmf-zarr.readthedocs.io/en/latest/overview.html>`_ for an overview of the available features and known limitations of hdmf-zarr.
 
 
 Latest Release
 --------------
 
 .. image:: https://readthedocs.org/projects/hdmf-zarr/badge/?version=latest
      :target: https://hdmf-zarr.readthedocs.io/en/latest/?badge=latest
@@ -58,15 +59,15 @@
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/run_all_tests.yml
 
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/Check%20Sphinx%20external%20links/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/check_external_links.yml
 
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/Deploy%20release/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/deploy_release.yml
-    
+
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/black/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/black.yml
 
 .. image:: https://github.com/hdmf-dev/hdmf-zarr/workflows/Run%20style%20check/badge.svg
     :target: https://github.com/hdmf-dev/hdmf-zarr/actions/workflows/run_flake8.yml
```

### Comparing `hdmf_zarr-0.2.0/tests/unit/test_io_convert.py` & `hdmf_zarr-0.3.0/tests/unit/test_io_convert.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,24 +1,40 @@
 """
 Module for testing conversion of data between different I/O backends
 To reduce the amount of code needed, the tests use a series of mixin classes to
 construct a test case:
-- MixinTestCaseConvert is the base mixin class for conversion tests and
-  requires that the setUpContainer and roundtripExportContainer functions
+
+- ``MixinTestCaseConvert`` is the base mixin class for conversion tests and
+  requires that the ``setUpContainer`` and ``roundtripExportContainer`` functions
   are defined. The setUpContainer defines the container (and hence the problem case)
-  to be written to file. And the rountripExportContainer defined the process
+  to be written to file. And the roundtripExportContainer defined the process
   for writing, exporting, and then reading the container again.
-- TestXYZContainerMixin classes define the setUpContainer function
-- TestX1toX2Mixin defines the rountripExportContainer process
-- TestCase is the base test class for HDMF
+- ``TestXYZContainerMixin`` classes define the ``setUpContainer`` function
+- ``TestX1toX2Mixin`` defines the ``roundtripExportContainer`` process
+- ``TestCase`` is the base test class for HDMF
+
 A test case is then constructed by defining a class that inherits from the
-corresponding (usually 4) base classes, a mixin that define setUpContainer,
-a mixin that define roundtripExportContainer, MixinTestCaseConvert, and TestCase.
+corresponding (usually 4) base classes:
+
+1. a mixin that define ``setUpContainer``,
+2. a mixin that define ``roundtripExportContainer``,
+3. ``MixinTestCaseConvert``, and
+4. TestCase.
+
 I.e., even though a particular test class may look empty, it is the combination
-of the mixin classes that creates the particular test problem.
+of the mixin classes that creates the particular test problem. Many of the Mixin
+classes also define additional class variables to allow child classes to further
+customize the behavior of the mixin.
+
+.. note::
+
+    The mixin classes should not be instantiated or class variables be modified
+    directly as the individual mixin classes only define partial behavior and
+    modifying the behavior in the mixin will affect all downstream tests.
+    Mixin classes should always be used through inheritance.
 """
 import os
 import shutil
 import numpy as np
 from abc import ABCMeta, abstractmethod
 
 from hdmf_zarr.backend import (ZarrIO,
@@ -30,145 +46,260 @@
 from hdmf.common import DynamicTable
 from hdmf.common import CSRMatrix
 from tests.unit.utils import (Foo,
                               FooBucket,
                               FooFile,
                               get_foo_buildmanager)
 
+from zarr.storage import (DirectoryStore,
+                          TempStore,
+                          NestedDirectoryStore)
+
 
 class MixinTestCaseConvert(metaclass=ABCMeta):
     """
     Mixin class used to define the basic structure for a conversion test.
+
+    To implement a test case using this mixin we need to implement the abstract methods
+    ``setUpContainer`` and ``roundtripExportContainer``. The behavior of the mixin can
+    then be further customized via the class variables: IGNORE_NAME, IGNORE_HDMF_ATTRS,
+    IGNORE_STRING_TO_BYTE, WRITE_PATHS, EXPORT_PATHS.
+
     """
     IGNORE_NAME = False
+    """
+    Bool parameter passed to assertContainerEqual (False)
+    """
+
     IGNORE_HDMF_ATTRS = False
+    """
+    Bool parameter passed to assertContainerEqual (False)
+    """
+
     IGNORE_STRING_TO_BYTE = False
+    """
+    Bool parameter passed to assertContainerEqual (False)
+    """
+
+    WRITE_PATHS = [None, ]
+    """
+    List of paths to which to write files to as part of ``test_export_roundtrip``,
+    which passes the values to ``roundtripContainer``. The specific definition
+    of the individual paths depends on the backend used for writing in ``roundtripContainer``.
+    E.g., if :py:class:`~hdmf.backends.h5tools.HDF5IO` is used then the paths must be strings,
+    and when :py:class:`~hdmf_zarr.backend.ZarrIO` is used then paths may be strings or
+    supported ``zarr.storage`` backend objects, e.g., a ``zarr.storage.DirectoryStore``.
+    A value of None as part of list means to use the default filename for write.
+    (Default=[None, ])
+    """
+
+    EXPORT_PATHS = [None, ]
+    """
+    List of paths to which to export files to as part of ``test_export_roundtrip``,
+    which passes the values to ``roundtripContainer``. The specific definition
+    of the individual paths depends on the backend used for writing in ``roundtripContainer``.
+    E.g., if :py:class:`~hdmf.backends.h5tools.HDF5IO` is used then the paths must be strings,
+    and when :py:class:`~hdmf_zarr.backend.ZarrIO` is used then paths may be strings or
+    supported ``zarr.storage`` backend objects, e.g., a ``zarr.storage.DirectoryStore``.
+    A value of None as part of list means to use the default filename for export.
+    (Default=[None, ])
+    """
 
     def get_manager(self):
         raise NotImplementedError('Cannot run test unless get_manger  is implemented')
 
     def setUp(self):
         self.__manager = self.get_manager()
-        self.container = self.setUpContainer()
-        self.container_type = self.container.__class__.__name__
-        self.filename = 'test_%s.hdmf' % self.container_type
-        self.export_filename = 'test_export_%s.hdmf' % self.container_type
-        self.filenames = [self.filename, self.export_filename]
+        self.filenames = []
         self.ios = []
 
     def tearDown(self):
+        self.close_files_and_ios()
+
+    def close_files_and_ios(self):
         for io in self.ios:
             if io is not None:
                 io.close()
         for fn in self.filenames:
             if fn is not None and os.path.exists(fn):
                 if os.path.isdir(fn):
                     shutil.rmtree(fn)
                 else:
                     os.remove(fn)
+        self.filenames = []
+        self.ios = []
 
     @abstractmethod
     def setUpContainer(self):
         """Return the Container to read/write."""
         raise NotImplementedError('Cannot run test unless setUpContainer is implemented')
 
     @abstractmethod
-    def roundtripExportContainer(self):
+    def roundtripExportContainer(self, container, write_path, export_path):
         """
-        1. Write the container to self.filename
-        2. Export the file from 1 to self.export_filename using a new backend
-        3. Read the exported container from disk
-        4. Return the container read in 4 so that it can be compared with the original
-        Any HDMFIO backends that should remain open should be added to the self.io list
-        so that they can be closed on tearDown.
+        1. Write the container to write_path
+        2. Export the file from write_path to export_path using a new backend
+        3. Read the exported container export_path from disk
+        4. Return the container read in 3 so that it can be compared with the original
+        Any HDMFIO backends that should remain open MUST be added to the self.io list
+        so that they can be closed by close_files_and_ios (e.g., on tearDown),
         """
         raise NotImplementedError('Cannot run test unless roundtripExportContainer  is implemented')
 
     def test_export_roundtrip(self):
-        """Test that rountripping the container works"""
-        exported_container = self.roundtripExportContainer()
-        self.assertIsNotNone(str(self.container))  # added as a test to make sure printing works
-        self.assertIsNotNone(str(exported_container))
-        # make sure we get a completely new object
-        self.assertNotEqual(id(self.container), id(exported_container))
-        # the name of the root container of a file is always 'root' (see h5tools.py ROOT_NAME)
-        # thus, ignore the name of the container when comparing original container vs read container
-        self.assertContainerEqual(self.container, exported_container,
-                                  ignore_name=self.IGNORE_NAME,
-                                  ignore_hdmf_attrs=self.IGNORE_HDMF_ATTRS,
-                                  ignore_string_to_byte=self.IGNORE_STRING_TO_BYTE)
-        # TODO May need to add further asserts here
-
-
-############################################
-# HDMF Common test harness
-###########################################
+        """Test that roundtripping the container works"""
+        # determine and save the write and export paths
+        for write_path in self.WRITE_PATHS:
+            for export_path in self.EXPORT_PATHS:
+                container = self.setUpContainer()
+                container_type = container.__class__.__name__
+                if write_path is None:
+                    write_path = 'test_%s.hdmf' % container_type
+                if export_path is None:
+                    export_path = 'test_export_%s.hdmf' % container_type
+                self.filenames.append(write_path if isinstance(write_path, str) else write_path.path)
+                self.filenames.append(export_path if isinstance(export_path, str) else export_path.path)
+                # roundtrip the container
+                exported_container = self.roundtripExportContainer(
+                    container=container,
+                    write_path=write_path,
+                    export_path=export_path)
+                # assert that the roundtrip worked correctly
+                message = "Using: write_path=%s, export_path=%s" % (str(write_path), str(export_path))
+                self.assertIsNotNone(str(container), message)  # added as a test to make sure printing works
+                self.assertIsNotNone(str(exported_container), message)
+                # make sure we get a completely new object
+                self.assertNotEqual(id(container), id(exported_container), message)
+                # the name of the root container of a file is always 'root' (see h5tools.py ROOT_NAME)
+                # thus, ignore the name of the container when comparing original container vs read container
+                self.assertContainerEqual(container,
+                                          exported_container,
+                                          ignore_name=self.IGNORE_NAME,
+                                          ignore_hdmf_attrs=self.IGNORE_HDMF_ATTRS,
+                                          ignore_string_to_byte=self.IGNORE_STRING_TO_BYTE,
+                                          message=message)
+                self.close_files_and_ios()
+                # TODO: May need to add further asserts here
+
+
+##########################################################
+# Mixins for tesing export between different backend IO
+#########################################################
 class MixinTestHDF5ToZarr():
     """
     Mixin class used in conjunction with MixinTestCaseConvert to create conversion tests from HDF5 to Zarr.
     This class only defines the roundtripExportContainer and get_manager functions for the test.
     The setUpContainer function required for the test needs to be defined separately
     (e.g., by another mixin or the test class itself).
     """
+    WRITE_PATHS = [None, ]
+    EXPORT_PATHS = [None,
+                    DirectoryStore('test_export_DirectoryStore.zarr'),
+                    TempStore(),
+                    NestedDirectoryStore('test_export_NestedDirectoryStore.zarr')]
+
     def get_manager(self):
         return get_hdmfcommon_manager()
 
-    def roundtripExportContainer(self):
-        with HDF5IO(self.filename, manager=self.get_manager(), mode='w') as write_io:
-            write_io.write(self.container, cache_spec=True)
+    def roundtripExportContainer(self, container, write_path, export_path):
+        with HDF5IO(write_path, manager=self.get_manager(), mode='w') as write_io:
+            write_io.write(container, cache_spec=True)
 
-        with HDF5IO(self.filename, manager=self.get_manager(), mode='r') as read_io:
-            with ZarrIO(self.export_filename, mode='w') as export_io:
+        with HDF5IO(write_path, manager=self.get_manager(), mode='r') as read_io:
+            with ZarrIO(export_path, mode='w') as export_io:
                 export_io.export(src_io=read_io, write_args={'link_data': False})
 
-        read_io = ZarrIO(self.export_filename, manager=self.get_manager(), mode='r')
+        read_io = ZarrIO(export_path, manager=self.get_manager(), mode='r')
         self.ios.append(read_io)
         exportContainer = read_io.read()
         return exportContainer
 
 
 class MixinTestZarrToHDF5():
     """
     Mixin class used in conjunction with MixinTestCaseConvert to create conversion tests from Zarr to HDF5.
     This class only defines the roundtripExportContainer and get_manager functions for the test.
     The setUpContainer function required for the test needs to be defined separately
     (e.g., by another mixin or the test class itself)
     """
+    WRITE_PATHS = [None,
+                   DirectoryStore('test_export_DirectoryStore.zarr'),
+                   TempStore(),
+                   NestedDirectoryStore('test_export_NestedDirectoryStore.zarr')]
+    EXPORT_PATHS = [None, ]
+
     def get_manager(self):
         return get_hdmfcommon_manager()
 
-    def roundtripExportContainer(self):
-        with ZarrIO(self.filename, manager=self.get_manager(), mode='w') as write_io:
-            write_io.write(self.container, cache_spec=True)
+    def roundtripExportContainer(self, container,  write_path, export_path):
+        with ZarrIO(write_path, manager=self.get_manager(), mode='w') as write_io:
+            write_io.write(container, cache_spec=True)
 
-        with ZarrIO(self.filename, manager=self.get_manager(), mode='r') as read_io:
-            with HDF5IO(self.export_filename, mode='w') as export_io:
+        with ZarrIO(write_path, manager=self.get_manager(), mode='r') as read_io:
+            with HDF5IO(export_path,  mode='w') as export_io:
                 export_io.export(src_io=read_io, write_args={'link_data': False})
 
-        read_io = HDF5IO(self.export_filename, manager=self.get_manager(), mode='r')
+        read_io = HDF5IO(export_path, manager=self.get_manager(), mode='r')
         self.ios.append(read_io)
         exportContainer = read_io.read()
         return exportContainer
 
 
+class MixinTestZarrToZarr():
+    """
+    Mixin class used in conjunction with MixinTestCaseConvert to create conversion tests from Zarr to Zarr.
+    This class only defines the roundtripExportContainer and get_manager functions for the test.
+    The setUpContainer function required for the test needs to be defined separately
+    (e.g., by another mixin or the test class itself)
+    """
+    WRITE_PATHS = [None,
+                   DirectoryStore('test_export_DirectoryStore_Source.zarr'),
+                   TempStore(dir=os.path.dirname(__file__)),  # set dir to avoid switching drives on Windows
+                   NestedDirectoryStore('test_export_NestedDirectoryStore_Source.zarr')]
+    EXPORT_PATHS = [None,
+                    DirectoryStore('test_export_DirectoryStore_Export.zarr'),
+                    TempStore(dir=os.path.dirname(__file__)),   # set dir to avoid switching drives on Windows
+                    NestedDirectoryStore('test_export_NestedDirectoryStore_Export.zarr')]
+
+    def get_manager(self):
+        return get_hdmfcommon_manager()
+
+    def roundtripExportContainer(self, container,  write_path, export_path):
+        with ZarrIO(write_path, manager=self.get_manager(), mode='w') as write_io:
+            write_io.write(container, cache_spec=True)
+
+        with ZarrIO(write_path, manager=self.get_manager(), mode='r') as read_io:
+            with ZarrIO(export_path,  mode='w') as export_io:
+                export_io.export(src_io=read_io, write_args={'link_data': False})
+
+        read_io = ZarrIO(export_path, manager=self.get_manager(), mode='r')
+        self.ios.append(read_io)
+        exportContainer = read_io.read()
+        return exportContainer
+
+
+############################################
+# HDMF Common test container mixins
+###########################################
 class MixinTestDynamicTableContainer():
     """
     Mixin class used in conjunction with MixinTestCaseConvert to create conversion tests that
     test export of DynamicTable container classes. This class only defines the setUpContainer function for the test.
     The roundtripExportContainer function required for the test needs to be defined separately
     (e.g., by another mixin or the test class itself)
-    This mixin adds the class variable, TABLE_TYPE  which is an int to select between different
+    This mixin adds the class variable, ``TABLE_TYPE``  which is an int to select between different
     container types for testing:
-    TABLE_TYPE=0 : Table of int, float, bool, Enum
-    TABLE_TYPE=1 : Table of int, float, str, bool, Enum
+
+    * ``TABLE_TYPE=0`` : Table of int, float, bool, Enum
+    * ``TABLE_TYPE=1`` : Table of int, float, str, bool, Enum
     """
     TABLE_TYPE = 0
 
     def setUpContainer(self):
-        # TODO: The tables are names "root" because otherwise the Zarr backend does not determine the path correctly
+        # TODO: The tables are named "root" because otherwise the Zarr backend does not determine the path correctly
         if self.TABLE_TYPE == 0:
             table = DynamicTable(name=ROOT_NAME,
                                  description='an example table')
             table.add_column('foo', 'an int column')
             table.add_column('bar', 'a float column')
             table.add_column('qux', 'a boolean column')
             table.add_column('quux', 'a enum column', enum=True, index=False)
@@ -207,47 +338,35 @@
                          indptr=indptr,
                          shape=(3, 3))
 
 
 #########################################
 # HDMF Foo test container test harness
 #########################################
-class MixinTestZarrToHDF5Foo(MixinTestZarrToHDF5):
-    """
-    Convert mixin for Zarr to HDF5 but using the BuildManager for the Foo test containers
-    """
-    def get_manager(self):
-        return get_foo_buildmanager()
-
-
-class MixinTestHDF5ToZarrFoo(MixinTestHDF5ToZarr):
-    """
-    Convert mixin for HDF5 to Zarr but using the BuildManager for the Foo test containers
-    """
-    def get_manager(self):
-        return get_foo_buildmanager()
-
-
 class MixinTestFoo():
     """
     Mixin class used in conjunction with MixinTestCaseConvert to create conversion tests that
     test export of a variety of Foo container classes. This class only defines the setUpContainer
-    function for the test. The roundtripExportContainer and get_manager function required for
+    and get_manager functions. The roundtripExportContainer function required for
     the test needs to be defined separately, e.g., by another mixin for Foo test cases, e.g.,
-    MixinTestZarrToHDF5Foo or MixinTestHDF5ToZarrFoo.
+    MixinTestZarrToHDF5,  MixinTestHDF5ToZarr, or MixinTestZarrToZarr
     This mixin adds the class variable, FOO_TYPE  which is an int to select between different
     container types for testing:
-    FOO_TYPE=0 : File with two Foo buckets storing integer datasets
-    FOO_TYPE=1 : File with one Foo buckets storing integer dataset and a SoftLink to it
+
+    * ``FOO_TYPE=0`` : File with two Foo buckets storing integer datasets
+    * ``FOO_TYPE=1`` : File with one Foo buckets storing integer dataset and a SoftLink to it
     """
     FOO_TYPE = 0
     FOO_TYPES = {'int_data': 0,
                  'link_data': 1,
                  'str_data': 2}
 
+    def get_manager(self):
+        return get_foo_buildmanager()
+
     def setUpContainer(self):
         if self.FOO_TYPE == 0:
             foo1 = Foo('foo1', [0, 1, 2, 3, 4], "I am foo1", 17, 3.14)
             foo2 = Foo('foo2', [5, 6, 7, 8, 9], "I am foo2", 34, 6.28)
             foobucket = FooBucket('bucket1', [foo1, foo2])
             foofile = FooFile(buckets=[foobucket])
             return foofile
@@ -272,14 +391,17 @@
     See MixinTestDynamicTableContainer.setUpContainer for the container spec.
     """
     IGNORE_NAME = True
     IGNORE_HDMF_ATTRS = True
     IGNORE_STRING_TO_BYTE = False
     TABLE_TYPE = 0
 
+    def test_simple(self, write_path=None, export_path=None):
+        print(write_path, export_path)
+
 
 class TestZarrToHDF5DynamicTableC0(MixinTestDynamicTableContainer,
                                    MixinTestZarrToHDF5,
                                    MixinTestCaseConvert,
                                    TestCase):
     """
     Test the conversion of DynamicTable containers from Zarr to HDF5.
@@ -287,14 +409,28 @@
     """
     IGNORE_NAME = True
     IGNORE_HDMF_ATTRS = True
     IGNORE_STRING_TO_BYTE = False
     TABLE_TYPE = 0
 
 
+class TestZarrToZarrDynamicTableC0(MixinTestDynamicTableContainer,
+                                   MixinTestZarrToZarr,
+                                   MixinTestCaseConvert,
+                                   TestCase):
+    """
+    Test the conversion of DynamicTable containers from Zarr to HDF5.
+    See MixinTestDynamicTableContainer.setUpContainer for the container spec.
+    """
+    IGNORE_NAME = True
+    IGNORE_HDMF_ATTRS = True
+    IGNORE_STRING_TO_BYTE = False
+    TABLE_TYPE = 0
+
+
 class TestHDF5ToZarrDynamicTableC1(MixinTestDynamicTableContainer,
                                    MixinTestHDF5ToZarr,
                                    MixinTestCaseConvert,
                                    TestCase):
     """
     Test the conversion of DynamicTable containers from HDF5 to Zarr.
     See MixinTestDynamicTableContainer.setUpContainer for the container spec.
@@ -315,14 +451,28 @@
     """
     IGNORE_NAME = True
     IGNORE_HDMF_ATTRS = True
     IGNORE_STRING_TO_BYTE = True   # Need to ignore conversion of strings to bytes
     TABLE_TYPE = 1
 
 
+class TestZarrToZarrDynamicTableC1(MixinTestDynamicTableContainer,
+                                   MixinTestZarrToZarr,
+                                   MixinTestCaseConvert,
+                                   TestCase):
+    """
+    Test the conversion of DynamicTable containers from Zarr to HDF5.
+    See MixinTestDynamicTableContainer.setUpContainer for the container spec.
+    """
+    IGNORE_NAME = True
+    IGNORE_HDMF_ATTRS = True
+    IGNORE_STRING_TO_BYTE = True   # Need to ignore conversion of strings to bytes
+    TABLE_TYPE = 1
+
+
 class TestHDF5ToZarrCSRMatrix(MixinTestCSRMatrix,
                               MixinTestHDF5ToZarr,
                               MixinTestCaseConvert,
                               TestCase):
     """
     Test the conversion of CSRMatrix containers from HDF5 to Zarr.
     """
@@ -339,58 +489,98 @@
     Test the conversion of CSRMatrix containers from Zarr to HDF5.
     """
     IGNORE_NAME = True
     IGNORE_HDMF_ATTRS = True
     IGNORE_STRING_TO_BYTE = False
 
 
+class TestZarrToZarrCSRMatrix(MixinTestCSRMatrix,
+                              MixinTestZarrToZarr,
+                              MixinTestCaseConvert,
+                              TestCase):
+    """
+    Test the conversion of CSRMatrix containers from Zarr to HDF5.
+    """
+    IGNORE_NAME = True
+    IGNORE_HDMF_ATTRS = True
+    IGNORE_STRING_TO_BYTE = False
+
+
 class TestZarrToHDF5FooCase1(MixinTestFoo,
-                             MixinTestZarrToHDF5Foo,
+                             MixinTestZarrToHDF5,
+                             MixinTestCaseConvert,
+                             TestCase):
+    """
+    Test the conversion of a simple Foo container with two buckets of datasets from Zarr to HDF5
+    See MixinTestFoo.setUpContainer for the container spec used.
+    """
+    IGNORE_NAME = True
+    IGNORE_HDMF_ATTRS = True
+    IGNORE_STRING_TO_BYTE = True
+    FOO_TYPE = MixinTestFoo.FOO_TYPES['int_data']
+
+
+class TestZarrToZarrFooCase1(MixinTestFoo,
+                             MixinTestZarrToZarr,
                              MixinTestCaseConvert,
                              TestCase):
     """
     Test the conversion of a simple Foo container with two buckets of datasets from Zarr to HDF5
     See MixinTestFoo.setUpContainer for the container spec used.
     """
     IGNORE_NAME = True
     IGNORE_HDMF_ATTRS = True
     IGNORE_STRING_TO_BYTE = True
     FOO_TYPE = MixinTestFoo.FOO_TYPES['int_data']
 
 
 class TestHDF5toZarrFooCase1(MixinTestFoo,
-                             MixinTestHDF5ToZarrFoo,
+                             MixinTestHDF5ToZarr,
                              MixinTestCaseConvert,
                              TestCase):
     """
     Test the conversion of a simple Foo container with two buckets of datasets from Zarr to HDF5
     See MixinTestFoo.setUpContainer for the container spec used.
     """
     IGNORE_NAME = True
     IGNORE_HDMF_ATTRS = True
     IGNORE_STRING_TO_BYTE = True
     FOO_TYPE = MixinTestFoo.FOO_TYPES['int_data']
 
 
 class TestZarrToHDF5FooCase2(MixinTestFoo,
-                             MixinTestZarrToHDF5Foo,
+                             MixinTestZarrToHDF5,
+                             MixinTestCaseConvert,
+                             TestCase):
+    """
+    Test the conversion of a simple Foo container with two buckets of datasets from Zarr to HDF5
+    See MixinTestFoo.setUpContainer for the container spec used.
+    """
+    IGNORE_NAME = True
+    IGNORE_HDMF_ATTRS = True
+    IGNORE_STRING_TO_BYTE = True
+    FOO_TYPE = MixinTestFoo.FOO_TYPES['link_data']
+
+
+class TestZarrToZarrFooCase2(MixinTestFoo,
+                             MixinTestZarrToZarr,
                              MixinTestCaseConvert,
                              TestCase):
     """
     Test the conversion of a simple Foo container with two buckets of datasets from Zarr to HDF5
     See MixinTestFoo.setUpContainer for the container spec used.
     """
     IGNORE_NAME = True
     IGNORE_HDMF_ATTRS = True
     IGNORE_STRING_TO_BYTE = True
     FOO_TYPE = MixinTestFoo.FOO_TYPES['link_data']
 
 
 class TestHDF5toZarrFooCase2(MixinTestFoo,
-                             MixinTestHDF5ToZarrFoo,
+                             MixinTestHDF5ToZarr,
                              MixinTestCaseConvert,
                              TestCase):
     """
     Test the conversion of a simple Foo container with two buckets of datasets from Zarr to HDF5
     See MixinTestFoo.setUpContainer for the container spec used.
     """
     IGNORE_NAME = True
```

### Comparing `hdmf_zarr-0.2.0/tests/unit/test_io_zarr.py` & `hdmf_zarr-0.3.0/tests/unit/base_tests_zarrio.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,12 +1,17 @@
-"""Test module to validate the ZarrIO is working"""
+"""
+Module defining the base unit test cases for ZarrIO.
+
+The actual tests are then instantiated with various different backends in the
+test_zarrio.py module."""
 import unittest
 import os
 import numpy as np
 import shutil
+import warnings
 
 # Try to import Zarr and disable tests if Zarr is not available
 import zarr
 from hdmf_zarr.backend import ZarrIO
 from hdmf_zarr.utils import ZarrDataIO
 
 # Try to import numcodecs and disable compression tests if it is not available
@@ -30,74 +35,123 @@
 from tests.unit.utils import (Foo,
                               FooBucket,
                               FooFile,
                               get_foo_buildmanager,
                               CacheSpecTestHelper,
                               get_temp_filepath)
 
+from abc import ABCMeta, abstractmethod
+
 
-def total_directory_size(source):
-    """Helper function used to compute the size of a directory"""
+def total_size(source):
+    """Helper function used to compute the size of a directory or file"""
     dsize = os.path.getsize(source)
-    for item in os.listdir(source):
-        itempath = os.path.join(source, item)
-        if os.path.isfile(itempath):
-            dsize += os.path.getsize(itempath)
-        elif os.path.isdir(itempath):
-            dsize += total_directory_size(itempath)
+    if os.path.isdir(source):
+        for item in os.listdir(source):
+            itempath = os.path.join(source, item)
+            if os.path.isfile(itempath):
+                dsize += os.path.getsize(itempath)
+            elif os.path.isdir(itempath):
+                dsize += total_size(itempath)
     return dsize
 
 
-class TestZarrWriter(TestCase):
-    """Test writing of builder with Zarr"""
+class BaseZarrWriterTestCase(TestCase, metaclass=ABCMeta):
+    """
+    Base class for unit tests for ZarrIO with support to configure the data store used.
+
+    Child classes must implement the ``setUp`` function of the test and define the following
+    main instance variables to define the data store to use for the tests defined here:
+
+    :ivar store: The Zarr data store(s) to use.
+    :type store: Same as the `path`` parameter of :py:class:`~hdmf_zarr.backend.ZarrIO.__init__ `
+    :ivar store_path: The path(s) to the Zarr file defined by the store
+    """
+
+    @abstractmethod
     def setUp(self):
-        self.manager = get_foo_buildmanager()
-        self.path = "test_io.zarr"
+        raise NotImplementedError
 
     def tearDown(self):
-        if os.path.exists(self.path):
-            shutil.rmtree(self.path)
+        """
+        Remove all files and folders defined by self.store_path
+        """
+        paths = self.store_path if isinstance(self.store_path, list) else [self.store_path, ]
+        for path in paths:
+            if os.path.exists(path):
+                if os.path.isdir(path):
+                    shutil.rmtree(path)
+                elif os.path.isfile(path):
+                    os.remove(path)
+                else:
+                    warnings.warn("Could not remove: %s" % path)
+
+
+class BaseTestZarrWriter(BaseZarrWriterTestCase):
+    """
+    Test writing of builder with ZarrIO
+
+    The following main instance variables need to be set by child classes to
+    customize the data store to use for the tests defined here:
+
+    :ivar store: The Zarr data store to use.
+    :type store: Same as the `path`` parameter of :py:class:`~hdmf_zarr.backend.ZarrIO.__init__ `
+    :ivar store_path: The path(s) to the Zarr file defined by the store
+
+    The builder data for the tests is defined by:
+
+    :ivar manager: The build manager to use for writing the builders
+
+    and the functions ``createGroupBuilder``, ``createReferenceBuilder`` and
+    ``createReferenceCompoundBuilder``. Customizing the builder data is in
+    principle possible in child classes but has not been tested.
+    """
+
+    def setUp(self):
+        self.manager = get_foo_buildmanager()
+        self.store = "test_io.zarr"
+        self.store_path = self.store
 
     def createGroupBuilder(self):
         self.foo_builder = GroupBuilder('foo1',
                                         attributes={'data_type': 'Foo',
                                                     'namespace': 'test_core',
                                                     'attr1': 17.5},
                                         datasets={'my_data': self.__dataset_builder})
         # self.foo = Foo('foo1', self.__dataset_builder.data, attr1="bar", attr2=17, attr3=3.14)
         # self.manager.prebuilt(self.foo, self.foo_builder)
         self.builder = GroupBuilder(
             'root',
-            source=self.path,
+            source=self.store_path,
             groups={'test_bucket':
                     GroupBuilder('test_bucket',
                                  groups={'foo_holder':
                                          GroupBuilder('foo_holder',
                                                       groups={'foo1': self.foo_builder})})},
             attributes={'data_type': 'FooFile'})
 
-    def getReferenceBuilder(self):
+    def createReferenceBuilder(self):
         data_1 = np.arange(100, 200, 10).reshape(2, 5)
         data_2 = np.arange(0, 200, 10).reshape(4, 5)
         dataset_1 = DatasetBuilder('dataset_1', data_1)
         dataset_2 = DatasetBuilder('dataset_2', data_2)
 
         ref_dataset_1 = ReferenceBuilder(dataset_1)
         ref_dataset_2 = ReferenceBuilder(dataset_2)
         ref_data = [ref_dataset_1, ref_dataset_2]
         dataset_ref = DatasetBuilder('ref_dataset', ref_data, dtype='object')
 
         builder = GroupBuilder('root',
-                               source=self.path,
+                               source=self.store_path,
                                datasets={'dataset_1': dataset_1,
                                          'dataset_2': dataset_2,
                                          'ref_dataset': dataset_ref})
         return builder
 
-    def getReferenceCompoundBuilder(self):
+    def createReferenceCompoundBuilder(self):
         data_1 = np.arange(100, 200, 10).reshape(2, 5)
         data_2 = np.arange(0, 200, 10).reshape(4, 5)
         dataset_1 = DatasetBuilder('dataset_1', data_1)
         dataset_2 = DatasetBuilder('dataset_2', data_2)
 
         ref_dataset_1 = ReferenceBuilder(dataset_1)
         ref_dataset_2 = ReferenceBuilder(dataset_2)
@@ -106,59 +160,63 @@
             (2, 'dataset_2', ref_dataset_2)
         ]
         ref_data_type = [{'name': 'id', 'dtype': 'int'},
                          {'name': 'name', 'dtype': str},
                          {'name': 'reference', 'dtype': 'object'}]
         dataset_ref = DatasetBuilder('ref_dataset', ref_data, dtype=ref_data_type)
         builder = GroupBuilder('root',
-                               source=self.path,
+                               source=self.store_path,
                                datasets={'dataset_1': dataset_1,
                                          'dataset_2': dataset_2,
                                          'ref_dataset': dataset_ref})
         return builder
 
+    def test_cannot_read(self):
+        assert not ZarrIO.can_read("incorrect_path")
+
     def read_test_dataset(self):
-        reader = ZarrIO(self.path, manager=self.manager, mode='r')
+        reader = ZarrIO(self.store, manager=self.manager, mode='r')
         self.root = reader.read_builder()
         dataset = self.root['test_bucket/foo_holder/foo1/my_data']
         return dataset
 
     def read(self):
-        reader = ZarrIO(self.path, manager=self.manager, mode='r')
+        reader = ZarrIO(self.store, manager=self.manager, mode='r')
         self.root = reader.read_builder()
 
     def test_cache_spec(self):
 
-        self.io = ZarrIO(self.path, manager=self.manager, mode='w')
+        tempIO = ZarrIO(self.store, manager=self.manager, mode='w')
 
         # Setup all the data we need
         foo1 = Foo('foo1', [0, 1, 2, 3, 4], "I am foo1", 17, 3.14)
         foo2 = Foo('foo2', [5, 6, 7, 8, 9], "I am foo2", 34, 6.28)
         foobucket = FooBucket('test_bucket', [foo1, foo2])
         foofile = FooFile(buckets=[foobucket])
 
         # Write the first file
-        self.io.write(foofile, cache_spec=True)
-        self.io.close()
+        tempIO.write(foofile, cache_spec=True)
+        tempIO.close()
 
         # Load the spec and assert that it is valid
         ns_catalog = NamespaceCatalog()
-        ZarrIO.load_namespaces(ns_catalog, self.path)
+        ZarrIO.load_namespaces(ns_catalog, self.store)
         self.assertEqual(ns_catalog.namespaces, ('test_core',))
-        source_types = CacheSpecTestHelper.get_types(self.io.manager.namespace_catalog)
+        source_types = CacheSpecTestHelper.get_types(self.manager.namespace_catalog)
         read_types = CacheSpecTestHelper.get_types(ns_catalog)
         self.assertSetEqual(source_types, read_types)
 
     def test_write_int(self, test_data=None):
         data = np.arange(100, 200, 10).reshape(2, 5) if test_data is None else test_data
         self.__dataset_builder = DatasetBuilder('my_data', data, attributes={'attr2': 17})
         self.createGroupBuilder()
-        writer = ZarrIO(self.path, manager=self.manager, mode='a')
+        writer = ZarrIO(self.store, manager=self.manager, mode='a')
         writer.write_builder(self.builder)
         writer.close()
+        assert ZarrIO.can_read(self.store)
 
     def test_write_compound(self, test_data=None):
         """
         :param test_data: Optional list of the form [(1, 'STR1'), (2, 'STR2')], i.e., a list of tuples where
                           each tuple consists of an int and a string
         :return:
         """
@@ -166,77 +224,79 @@
                 (2, 'Bob'),
                 (3, 'Mike'),
                 (4, 'Jenny')] if test_data is None else test_data
         data_type = [{'name': 'id', 'dtype': 'int'},
                      {'name': 'name', 'dtype': str}]
         self.__dataset_builder = DatasetBuilder('my_data', data, dtype=data_type)
         self.createGroupBuilder()
-        writer = ZarrIO(self.path, manager=self.manager, mode='a')
+        writer = ZarrIO(self.store, manager=self.manager, mode='a')
         writer.write_builder(self.builder)
         writer.close()
 
     def test_write_chunk(self, test_data=None):
         data = np.arange(100, 200, 10).reshape(2, 5) if test_data is None else test_data
         data_io = ZarrDataIO(data=data, chunks=(1, 5), fillvalue=-1)
         self.__dataset_builder = DatasetBuilder('my_data', data_io, attributes={'attr2': 17})
         self.createGroupBuilder()
-        writer = ZarrIO(self.path, manager=self.manager, mode='a')
+        writer = ZarrIO(self.store, manager=self.manager, mode='a')
         writer.write_builder(self.builder)
         writer.close()
 
     def test_write_strings(self, test_data=None):
         data = [['a', 'aa', 'aaa', 'aaaa', 'aaaaa'],
                 ['b', 'bb', 'bbb', 'bbbb', 'bbbbb']] if test_data is None else test_data
         self.__dataset_builder = DatasetBuilder('my_data', data, attributes={'attr2': 17})
         self.createGroupBuilder()
-        writer = ZarrIO(self.path, manager=self.manager, mode='a')
+        writer = ZarrIO(self.store, manager=self.manager, mode='a')
         writer.write_builder(self.builder)
         writer.close()
 
     def test_write_links(self, test_data=None):
         data = np.arange(100, 200, 10).reshape(2, 5) if test_data is None else test_data
         self.__dataset_builder = DatasetBuilder('my_data', data, attributes={'attr2': 17})
         self.createGroupBuilder()
         link_parent = self.builder['test_bucket']
         link_parent.set_link(LinkBuilder(self.foo_builder, 'my_link'))
         link_parent.set_link(LinkBuilder(self.__dataset_builder, 'my_dataset'))
-        writer = ZarrIO(self.path, manager=self.manager, mode='a')
+        writer = ZarrIO(self.store, manager=self.manager, mode='a')
         writer.write_builder(self.builder)
         writer.close()
 
     def test_write_link_array(self):
         data = np.arange(100, 200, 10).reshape(2, 5)
         self.__dataset_builder = DatasetBuilder('my_data', data, attributes={'attr2': 17})
         self.createGroupBuilder()
-        writer = ZarrIO(self.path, manager=self.manager, mode='a')
+        writer = ZarrIO(self.store, manager=self.manager, mode='a')
         writer.write_builder(self.builder)
-        zarr_array = zarr.open(self.path+"/test_bucket/foo_holder/foo1/my_data", mode='r')
+        zarr_file = zarr.open(self.store, mode='r')
+        zarr_array = zarr_file["/test_bucket/foo_holder/foo1/my_data"]
         link_io = ZarrDataIO(data=zarr_array, link_data=True)
         link_dataset = DatasetBuilder('dataset_link', link_io)
         self.builder['test_bucket'].set_dataset(link_dataset)
         writer.write_builder(self.builder)
         writer.close()
 
-        reader = ZarrIO(self.path, manager=self.manager, mode='r')
+        reader = ZarrIO(self.store, manager=self.manager, mode='r')
         self.root = reader.read_builder()
         read_link = self.root['test_bucket/dataset_link']
         read_link_data = read_link['builder']['data'][:]
         self.assertTrue(np.all(data == read_link_data))
+        reader.close()
 
     def test_write_reference(self):
-        builder = self.getReferenceBuilder()
-        writer = ZarrIO(self.path,
+        builder = self.createReferenceBuilder()
+        writer = ZarrIO(self.store,
                         manager=self.manager,
                         mode='a')
         writer.write_builder(builder)
         writer.close()
 
     def test_write_reference_compound(self):
-        builder = self.getReferenceCompoundBuilder()
-        writer = ZarrIO(self.path, manager=self.manager, mode='a')
+        builder = self.createReferenceCompoundBuilder()
+        writer = ZarrIO(self.store, manager=self.manager, mode='a')
         writer.write_builder(builder)
         writer.close()
 
     def test_read_int(self):
         test_data = np.arange(100, 200, 10).reshape(5, 2)
         self.test_write_int(test_data=test_data)
         dataset = self.read_test_dataset()['data'][:]
@@ -277,34 +337,34 @@
         data = np.arange(100, 200, 10).reshape(2, 5)
         self.__dataset_builder = DatasetBuilder('my_data', data, attributes={'attr2': 17})
         self.createGroupBuilder()
         link_parent_1 = self.builder['test_bucket']
         link_parent_2 = self.builder['test_bucket/foo_holder']
         link_parent_1.set_link(LinkBuilder(self.__dataset_builder, 'my_dataset_1'))
         link_parent_2.set_link(LinkBuilder(self.__dataset_builder, 'my_dataset_2'))
-        writer = ZarrIO(self.path, manager=self.manager, mode='a')
+        writer = ZarrIO(self.store, manager=self.manager, mode='a')
         writer.write_builder(self.builder)
         writer.close()
         self.read()
         self.assertTrue(self.root['test_bucket'].links['my_dataset_1'].builder ==
                         self.root['test_bucket/foo_holder'].links['my_dataset_2'].builder)
 
     def test_read_reference(self):
         self.test_write_reference()
         self.read()
-        builder = self.getReferenceBuilder()['ref_dataset']
+        builder = self.createReferenceBuilder()['ref_dataset']
         read_builder = self.root['ref_dataset']
         # Load the linked arrays and confirm we get the same data as we had in the original builder
         for i, v in enumerate(read_builder['data']):
             self.assertTrue(np.all(builder['data'][i]['builder']['data'] == v['data'][:]))
 
     def test_read_reference_compound(self):
         self.test_write_reference_compound()
         self.read()
-        builder = self.getReferenceCompoundBuilder()['ref_dataset']
+        builder = self.createReferenceCompoundBuilder()['ref_dataset']
         read_builder = self.root['ref_dataset']
         # Load the elements of each entry in the compound dataset and compar the index, string, and referenced array
         for i, v in enumerate(read_builder['data']):
             self.assertEqual(v[0], builder['data'][i][0])  # Compare index value from compound tuple
             self.assertEqual(v[1], builder['data'][i][1])  # Compare string value from compound tuple
             self.assertTrue(np.all(v[2]['data'][:] == builder['data'][i][2]['builder']['data'][:]))  # Compare ref array
         # print(read_builder)
@@ -324,55 +384,56 @@
             (4, 'dataset_4', ReferenceBuilder(dataset_2))
         ]
         ref_data_type = [{'name': 'id', 'dtype': 'int'},
                          {'name': 'name', 'dtype': str},
                          {'name': 'reference', 'dtype': 'object'}]
         dataset_ref = DatasetBuilder('ref_dataset', ref_data, dtype=ref_data_type)
         builder = GroupBuilder('root',
-                               source=self.path,
+                               source=self.store_path,
                                datasets={'dataset_1': dataset_1,
                                          'dataset_2': dataset_2,
                                          'ref_dataset': dataset_ref})
-        writer = ZarrIO(self.path, manager=self.manager, mode='a')
+        writer = ZarrIO(self.store, manager=self.manager, mode='a')
         writer.write_builder(builder)
         writer.close()
 
         self.read()
         self.assertFalse(self.root["ref_dataset"].data[0][2] == self.root['ref_dataset'].data[1][2])
         self.assertTrue(self.root["ref_dataset"].data[0][2] == self.root['ref_dataset'].data[2][2])
 
 
-class TestZarrWriteUnit(TestCase):
+class BaseTestZarrWriteUnit(BaseZarrWriterTestCase):
     """
     Unit test for individual write functions
     """
-    def setUp(self):
-        self.path = "test_io.zarr"
-        self.io = ZarrIO(self.path, mode='w')
-        self.f = self.io._ZarrIO__file
 
-    def tearDown(self):
-        if os.path.exists(self.path):
-            shutil.rmtree(self.path)
+    def setUp(self):
+        self.store = "test_io.zarr"
+        self.store_path = self.store
 
     #############################################
     #  ZarrDataIO general
     #############################################
     def test_set_object_codec(self):
         # Test that the default codec is the Pickle store
-        self.assertEqual(self.io.object_codec_class.__qualname__, 'Pickle')
-        temp_io = ZarrIO(self.path, mode='w', object_codec_class=JSON)
-        self.assertEqual(temp_io.object_codec_class.__qualname__, 'JSON')
+        tempIO = ZarrIO(self.store, mode='w')
+        self.assertEqual(tempIO.object_codec_class.__qualname__, 'Pickle')
+        del tempIO  # also calls tempIO.close()
+        tempIO = ZarrIO(self.store, mode='w', object_codec_class=JSON)
+        self.assertEqual(tempIO.object_codec_class.__qualname__, 'JSON')
+        tempIO.close()
 
     def test_synchronizer_constructor_arg_bool(self):
         """Test that setting the synchronizer argument to True/False works in ZarrIO"""
-        self.assertIsNone(self.io.synchronizer)
-        self.io.close()
-        self.io = ZarrIO(self.path, mode='w', synchronizer=True)
-        self.assertTrue(isinstance(self.io.synchronizer, zarr.ProcessSynchronizer))
+        tempIO = ZarrIO(self.store, mode='w', synchronizer=False)
+        self.assertIsNone(tempIO.synchronizer)
+        del tempIO  # also calls tempIO.close()
+        tempIO = ZarrIO(self.store, mode='w', synchronizer=True)
+        self.assertTrue(isinstance(tempIO.synchronizer, zarr.ProcessSynchronizer))
+        tempIO.close()
 
     def test_zarrdataio_enable_default_compressor(self):
         """Default compression simply means not specifying any compressor and using Zarr defaults"""
         dataio = ZarrDataIO(np.arange(30).reshape(5, 2, 3), compressor=True)
         self.assertEqual(len(dataio.io_settings), 0)
 
     def test_zarrdataio_disable_compressor(self):
@@ -399,55 +460,67 @@
         data = ZarrDataIO(test_speed)
         with self.assertRaises(NotImplementedError):
             np.isfinite(data)  # Force call of H5DataIO.__array__
 
     def test_get_builder_exists_on_disk(self):
         """Test that get_builder_exists_on_disk finds the existing builder"""
         dset_builder = DatasetBuilder('test_dataset', 10, attributes={})
-        self.assertFalse(self.io.get_builder_exists_on_disk(dset_builder))  # Make sure False is returned before write
-        self.io.write_dataset(self.f, dset_builder)
-        self.assertTrue(self.io.get_builder_exists_on_disk(dset_builder))   # Make sure True is returned after write
+        tempIO = ZarrIO(self.store, mode='w')
+        self.assertFalse(tempIO.get_builder_exists_on_disk(builder=dset_builder))  # Make sure is False is before write
+        tempIO .write_dataset(tempIO.file, dset_builder)
+        self.assertTrue(tempIO.get_builder_exists_on_disk(builder=dset_builder))   # Make sure is True after write
+        tempIO.close()
 
     def test_get_written(self):
         """Test that get_builder_exists_on_disk finds the existing builder"""
+        tempIO = ZarrIO(self.store, mode='w')
         dset_builder = DatasetBuilder('test_dataset', 10, attributes={})
-        self.assertFalse(self.io.get_written(dset_builder))  # Make sure False is returned before write
-        self.io.write_dataset(self.f, dset_builder)
-        self.assertTrue(self.io.get_written(dset_builder))   # Make sure True is returned after write
-        self.assertTrue(self.io.get_written(dset_builder, check_on_disk=True))   # Make sure its also on disk
-        # Now delete it from disk and check again
-        shutil.rmtree(self.io.get_builder_disk_path(dset_builder))
-        self.assertTrue(self.io.get_written(dset_builder))   # The written flag should still be true
-        self.assertFalse(self.io.get_written(dset_builder, check_on_disk=True))   # But with check on disk should fail
+        self.assertFalse(tempIO.get_written(dset_builder))  # Make sure False is returned before write
+        tempIO.write_dataset(tempIO.file, dset_builder)
+        self.assertTrue(tempIO.get_written(dset_builder))   # Make sure True is returned after write
+        self.assertTrue(tempIO.get_written(dset_builder, check_on_disk=True))   # Make sure its also on disk
+        # Now delete it from disk and check again.
+        builder_path = tempIO.get_builder_disk_path(dset_builder)
+        if os.path.isdir(builder_path):  # Skip this check for file-based stores were we can easily delete objects
+            shutil.rmtree(builder_path)
+            # The written flag should still be true
+            self.assertTrue(tempIO.get_written(dset_builder))
+            # But with check on disk should fail
+            self.assertFalse(tempIO.get_written(dset_builder, check_on_disk=True))
+        tempIO.close()
 
     ##########################################
     #  write_attributes
     ##########################################
     def __write_attribute_test_helper(self, name, value, assert_value=True):
         """
         Helper function to write a single attribute and check its value for correctness
+
         :param name: Name of the attribute
         :param value: Value of the attribute
         :param assert_value: Boolean indicating whether we should check correctness of the returned value
         :returns: the value read from disk so we can do our own tests if needed
         """
         # write the attribute
-        testgroup = self.io._ZarrIO__file  # For testing we just use our file and create some attributes
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        testgroup = tempIO.file  # For testing we just use our file and create some attributes
         attr = {name: value}
-        self.io.write_attributes(testgroup, attr)
+        tempIO.write_attributes(testgroup, attr)
         # read the attribute
         read_val = testgroup.attrs[name]
         # assert that the read value matches the expected value
         if assert_value:
             if isinstance(value, (list, tuple, set)):
                 self.assertTupleEqual(read_val, tuple(value))
             elif isinstance(value, np.ndarray):
                 self.assertListEqual(list(read_val), value.tolist())
             else:
                 self.assertEqual(testgroup.attrs[name], value)
+        tempIO.close()
         return read_val
 
     def test_write_attributes_write_scalar_int(self):
         self.__write_attribute_test_helper('intattr', np.int32(5))
         self.__write_attribute_test_helper('intattr', 10)
 
     def test_write_attributes_write_scalar_float(self):
@@ -498,588 +571,663 @@
 
     def test_write_attributes_write_3Darray_of_floats(self):
         self.__write_attribute_test_helper('attr', np.arange(18).astype('float').reshape((2, 3, 3)) + 0.1)
 
     def test_write_attributes_write_reference_to_datasetbuilder(self):
         data_1 = np.arange(100, 200, 10).reshape(2, 5)
         dataset_1 = DatasetBuilder('dataset_1', data_1)
-        testgroup = self.io._ZarrIO__file  # For testing we just use our file and create some attributes
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
         attr = {'attr1': dataset_1}
-        self.io.write_attributes(testgroup, attr)
+        tempIO.write_attributes(obj=tempIO.file, attributes=attr)
         expected_value = {'attr1': {'zarr_dtype': 'object', 'value': {'source': ".", 'path': '/dataset_1'}}}
-        self.assertDictEqual(testgroup.attrs.asdict(), expected_value)
+        self.assertDictEqual(tempIO.file.attrs.asdict(), expected_value)
+        tempIO.close()
 
     def test_write_attributes_write_reference_to_referencebuilder(self):
         data_1 = np.arange(100, 200, 10).reshape(2, 5)
         dataset_1 = DatasetBuilder('dataset_1', data_1)
         ref1 = ReferenceBuilder(dataset_1)
-        testgroup = self.io._ZarrIO__file  # For testing we just use our file and create some attributes
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
         attr = {'attr1': ref1}
-        self.io.write_attributes(testgroup, attr)
+        tempIO.write_attributes(obj=tempIO.file, attributes=attr)
         expected_value = {'attr1': {'zarr_dtype': 'object', 'value': {'source': ".", 'path': '/dataset_1'}}}
-        self.assertDictEqual(testgroup.attrs.asdict(), expected_value)
+        self.assertDictEqual(tempIO.file.attrs.asdict(), expected_value)
+        tempIO.close()
 
     ##########################################
     #  write_dataset tests: scalars
     ##########################################
     def test_write_dataset_scalar(self):
         a = 10
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', a, attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', a, attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertTupleEqual(dset.shape, (1,))
         self.assertEqual(dset[()], a)
+        tempIO.close()
 
     def test_write_dataset_string(self):
         a = 'test string'
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', a, attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', a, attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertTupleEqual(dset.shape, (1,))
         self.assertEqual(dset[()], a)
+        tempIO.close()
 
     ##########################################
     #  write_dataset tests: lists
     ##########################################
     def test_write_dataset_list(self):
         a = np.arange(30).reshape(5, 2, 3)
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', a.tolist(), attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', a.tolist(), attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertTrue(np.all(dset[:] == a))
+        tempIO.close()
 
     def test_write_dataset_list_chunked(self):
         a = ZarrDataIO(np.arange(30).reshape(5, 2, 3),
                        chunks=(1, 1, 3))
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', a, attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', a, attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertTrue(np.all(dset[:] == a.data))
         self.assertEqual(dset.chunks, (1, 1, 3))
+        tempIO.close()
 
     def test_write_dataset_list_fillvalue(self):
         a = ZarrDataIO(np.arange(20).reshape(5, 4), fillvalue=-1)
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', a, attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', a, attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertTrue(np.all(dset[:] == a.data))
         self.assertEqual(dset.fill_value, -1)
+        tempIO.close()
 
     @unittest.skipIf(DISABLE_ZARR_COMPRESSION_TESTS, 'Skip test due to numcodec compressor not available')
     def test_write_dataset_list_compress(self):
         compressor = Blosc(cname='zstd', clevel=3, shuffle=Blosc.BITSHUFFLE)
         a = ZarrDataIO(np.arange(30).reshape(5, 2, 3),
                        compressor=compressor)
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', a, attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', a, attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertTrue(np.all(dset[:] == a.data))
         self.assertTrue(dset.compressor == compressor)
+        tempIO.close()
 
     @unittest.skipIf(DISABLE_ZARR_COMPRESSION_TESTS, 'Skip test due to numcodec compressor not available')
     def test_write_dataset_list_compress_and_filter(self):
         compressor = Blosc(cname='zstd', clevel=3, shuffle=Blosc.BITSHUFFLE)
         filters = [Delta(dtype='i4')]
         a = ZarrDataIO(np.arange(30, dtype='i4').reshape(5, 2, 3),
                        compressor=compressor,
                        filters=filters)
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', a, attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', a, attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertTrue(np.all(dset[:] == a.data))
         self.assertTrue(dset.compressor == compressor)
         self.assertListEqual(dset.filters, filters)
+        tempIO.close()
 
     ##########################################
     #  write_dataset tests: Iterable
     ##########################################
     def test_write_dataset_iterable(self):
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', range(10), attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', range(10), attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertListEqual(dset[:].tolist(), list(range(10)))
+        tempIO.close()
 
     ##############################################
     #  write_dataset tests: compound data tables
     #############################################
     def test_write_structured_array_table(self):
         cmpd_dt = np.dtype([('a', np.int32), ('b', np.float64)])
         data = np.zeros(10, dtype=cmpd_dt)
         data['a'][1] = 101
         data['b'][1] = 0.1
         dt = [{'name': 'a', 'dtype': 'int32', 'doc': 'a column'},
               {'name': 'b', 'dtype': 'float64', 'doc': 'b column'}]
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', data, attributes={}, dtype=dt))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', data, attributes={}, dtype=dt))
+        dset = tempIO.file['test_dataset']
         self.assertEqual(dset['a'].tolist(), data['a'].tolist())
         self.assertEqual(dset['b'].tolist(), data['b'].tolist())
+        tempIO.close()
 
     def test_write_nested_structured_array_table(self):
         b_cmpd_dt = np.dtype([('c', np.int32), ('d', np.float64)])
         cmpd_dt = np.dtype([('a', np.int32), ('b', b_cmpd_dt)])
         data = np.zeros(10, dtype=cmpd_dt)
         data['a'][1] = 101
         data['b']['c'] = 202
         data['b']['d'] = 10.1
         b_dt = [{'name': 'c', 'dtype': 'int32', 'doc': 'c column'},
                 {'name': 'd', 'dtype': 'float64', 'doc': 'd column'}]
         dt = [{'name': 'a', 'dtype': 'int32', 'doc': 'a column'},
               {'name': 'b', 'dtype': b_dt, 'doc': 'b column'}]
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', data, attributes={}, dtype=dt))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', data, attributes={}, dtype=dt))
+        dset = tempIO.file['test_dataset']
         # Test that all elements match. dset return np.void types so we just compare strings for simplicity
         for i in range(10):
             self.assertEqual(str(dset[i]), str(data[i]))
+        tempIO.close()
 
     #############################################
     #  write_dataset tests: data chunk iterator
     #############################################
     def test_write_dataset_iterable_multidimensional_array(self):
         a = np.arange(30).reshape(5, 2, 3)
         aiter = iter(a)
         daiter = DataChunkIterator.from_iterable(aiter, buffer_size=2)
-        self.io.write_dataset(parent=self.f,
-                              builder=DatasetBuilder('test_dataset', daiter, attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(parent=tempIO.file,
+                             builder=DatasetBuilder('test_dataset', daiter, attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertListEqual(dset[:].tolist(), a.tolist())
+        tempIO.close()
 
     def test_write_dataset_iterable_multidimensional_array_compression(self):
         a = np.arange(30).reshape(5, 2, 3)
         aiter = iter(a)
         daiter = DataChunkIterator.from_iterable(aiter, buffer_size=2)
         compressor = Blosc(cname='zstd', clevel=3, shuffle=Blosc.BITSHUFFLE)
         wrapped_daiter = ZarrDataIO(data=daiter,
                                     compressor=compressor)
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', wrapped_daiter, attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', wrapped_daiter, attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertEqual(dset.shape, a.shape)
         self.assertListEqual(dset[:].tolist(), a.tolist())
         self.assertTrue(dset.compressor == compressor)
+        tempIO.close()
 
     def test_write_dataset_data_chunk_iterator(self):
         dci = DataChunkIterator(data=np.arange(10), buffer_size=2)
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', dci, attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', dci, attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertListEqual(dset[:].tolist(), list(range(10)))
+        tempIO.close()
 
     def test_write_dataset_data_chunk_iterator_with_compression(self):
         dci = DataChunkIterator(data=np.arange(10), buffer_size=2)
         compressor = Blosc(cname='zstd', clevel=3, shuffle=Blosc.BITSHUFFLE)
         wrapped_dci = ZarrDataIO(data=dci,
                                  compressor=compressor,
                                  chunks=(2,))
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', wrapped_dci, attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', wrapped_dci, attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertListEqual(dset[:].tolist(), list(range(10)))
         self.assertTrue(dset.compressor == compressor)
         self.assertEqual(dset.chunks, (2,))
+        tempIO.close()
 
     def test_pass_through_of_recommended_chunks(self):
 
         class DC(DataChunkIterator):
             def recommended_chunk_shape(self):
                 return (5, 1, 1)
         dci = DC(data=np.arange(30).reshape(5, 2, 3))
         compressor = Blosc(cname='zstd', clevel=3, shuffle=Blosc.BITSHUFFLE)
         wrapped_dci = ZarrDataIO(data=dci,
                                  compressor=compressor)
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', wrapped_dci, attributes={}))
-        dset = self.f['test_dataset']
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', wrapped_dci, attributes={}))
+        dset = tempIO.file['test_dataset']
         self.assertEqual(dset.chunks, (5, 1, 1))
         self.assertTrue(dset.compressor == compressor)
+        tempIO.close()
 
     #############################################
     #  Copy/Link h5py.Dataset object
     #############################################
     def test_link_zarr_dataset_input(self):
         dset = DatasetBuilder('test_dataset', np.arange(10), attributes={})
-        self.io.write_dataset(self.f, builder=dset)
-        softlink = DatasetBuilder('test_softlink', self.f['test_dataset'], attributes={})
-        self.io.write_dataset(self.f, builder=softlink)
-        tempf = zarr.open(store=self.path, mode='r')
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, builder=dset)
+        softlink = DatasetBuilder('test_softlink', tempIO.file['test_dataset'], attributes={})
+        tempIO.write_dataset(tempIO.file, builder=softlink)
+        tempf = zarr.open(store=self.store, mode='r')
         expected_link = {'name': 'test_softlink',
                          'path': '/test_dataset',
-                         'source': os.path.abspath(self.path)}
+                         'source': os.path.abspath(self.store_path)}
         self.assertEqual(len(tempf.attrs['zarr_link']), 1)
         self.assertDictEqual(tempf.attrs['zarr_link'][0], expected_link)
+        tempIO.close()
 
     def test_copy_zarr_dataset_input(self):
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', np.arange(10), attributes={}))
-        self.io.write_dataset(self.f,
-                              DatasetBuilder('test_copy', self.f['test_dataset'], attributes={}),
-                              link_data=False)
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', np.arange(10), attributes={}))
+        tempIO.write_dataset(tempIO.file,
+                             DatasetBuilder('test_copy', tempIO.file['test_dataset'], attributes={}),
+                             link_data=False)
         # NOTE: In HDF5 this would be a HardLink. Since Zarr does not support links, this will be a copy instead.
-        self.assertListEqual(self.f['test_dataset'][:].tolist(),
-                             self.f['test_copy'][:].tolist())
+        self.assertListEqual(tempIO.file['test_dataset'][:].tolist(),
+                             tempIO.file['test_copy'][:].tolist())
+        tempIO.close()
 
     def test_link_dataset_zarrdataio_input(self):
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', np.arange(10), attributes={}))
-        self.io.write_dataset(self.f, DatasetBuilder('test_softlink',
-                                                     ZarrDataIO(data=self.f['test_dataset'],
-                                                                link_data=True),
-                                                     attributes={}))
-        tempf = zarr.open(store=self.path, mode='r')
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', np.arange(10), attributes={}))
+        tempIO.write_dataset(tempIO.file,
+                             DatasetBuilder(
+                                 'test_softlink',
+                                 ZarrDataIO(data=tempIO.file['test_dataset'], link_data=True),
+                                 attributes={})
+                             )
+        tempf = zarr.open(self.store, mode='r')
         expected_link = {'name': 'test_softlink',
                          'path': '/test_dataset',
-                         'source': os.path.abspath(self.path)}
+                         'source': os.path.abspath(self.store_path)}
         self.assertEqual(len(tempf.attrs['zarr_link']), 1)
         self.assertDictEqual(tempf.attrs['zarr_link'][0], expected_link)
+        tempIO.close()
 
     def test_copy_dataset_zarrdataio_input(self):
-        self.io.write_dataset(self.f, DatasetBuilder('test_dataset', np.arange(10), attributes={}))
-        self.io.write_dataset(self.f,
-                              DatasetBuilder('test_copy',
-                                             ZarrDataIO(data=self.f['test_dataset'],
-                                                        link_data=False),  # Force dataset copy
-                                             attributes={}),
-                              link_data=True)  # Make sure the default behavior is set to link the data
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        tempIO.write_dataset(tempIO.file, DatasetBuilder('test_dataset', np.arange(10), attributes={}))
+        tempIO.write_dataset(tempIO.file,
+                             DatasetBuilder('test_copy',
+                                            ZarrDataIO(data=tempIO.file['test_dataset'],
+                                                       link_data=False),  # Force dataset copy
+                                            attributes={}),
+                             link_data=True)  # Make sure the default behavior is set to link the data
         # NOTE: In HDF5 this would be a HardLink. Since Zarr does not support links, this will be a copy instead.
-        self.assertListEqual(self.f['test_dataset'][:].tolist(),
-                             self.f['test_copy'][:].tolist())
+        self.assertListEqual(tempIO.file['test_dataset'][:].tolist(),
+                             tempIO.file['test_copy'][:].tolist())
+        tempIO.close()
 
     def test_list_fill_empty(self):
-        dset = self.io.__list_fill__(self.f, 'empty_dataset', [], options={'dtype': int, 'io_settings': {}})
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
+        dset = tempIO.__list_fill__(tempIO.file, 'empty_dataset', [], options={'dtype': int, 'io_settings': {}})
         self.assertTupleEqual(dset.shape, (0,))
+        tempIO.close()
 
     def test_list_fill_empty_no_dtype(self):
+        tempIO = ZarrIO(self.store, mode='w')
+        tempIO.open()
         with self.assertRaisesRegex(Exception, r"cannot add empty_dataset to / - could not determine type"):
-            self.io.__list_fill__(self.f, 'empty_dataset', [])
+            tempIO.__list_fill__(tempIO.file, 'empty_dataset', [])
+        tempIO.close()
 
 
-class TestExportZarrToZarr(TestCase):
-    """Test exporting Zarr to Zarr."""
+class BaseTestExportZarrToZarr(BaseZarrWriterTestCase):
+    """
+    Test exporting Zarr to Zarr.
+
+    In contrast to the normal BaseZarrWriterTestCase, here the store and store_path
+    variable require to be a list of length 4.
+
+    :ivar store: List of 4  Zarr data stores to use.
+    :type store: List of 4 store values. Stores are the same as the `path``
+                  parameter of :py:class:`~hdmf_zarr.backend.ZarrIO.__init__ `
+    :ivar store_path: The paths to the Zarr file defined by the stores
+    """
 
     def setUp(self):
-        self.paths = [
+        self.store = [
             get_temp_filepath(),
             get_temp_filepath(),
             get_temp_filepath(),
             get_temp_filepath()
         ]
-
-    def tearDown(self):
-        for p in self.paths:
-            if os.path.exists(p):
-                shutil.rmtree(p)
+        self.store_path = self.store
 
     def test_basic(self):
         """Test that exporting a written container works between Zarr and Zarr."""
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+            with ZarrIO(self.store[1], mode='w') as export_io:
                 export_io.export(src_io=read_io)
 
-        self.assertTrue(os.path.exists(self.paths[1]))
-        self.assertEqual(foofile.container_source, self.paths[0])
+        self.assertTrue(os.path.exists(self.store_path[1]))
+        self.assertEqual(foofile.container_source, self.store_path[0])
 
-        with ZarrIO(self.paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store[1], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile = read_io.read()
-            self.assertEqual(read_foofile.container_source, self.paths[1])
+            self.assertEqual(read_foofile.container_source, self.store_path[1])
             self.assertContainerEqual(foofile, read_foofile, ignore_hdmf_attrs=True)
 
     def test_basic_container(self):
         """Test that exporting a written container, passing in the container arg, works."""
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile = read_io.read()
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+            with ZarrIO(self.store[1], mode='w') as export_io:
                 export_io.export(src_io=read_io, container=read_foofile)
 
-        self.assertTrue(os.path.exists(self.paths[1]))
-        self.assertEqual(foofile.container_source, self.paths[0])
+        self.assertTrue(os.path.exists(self.store_path[1]))
+        self.assertEqual(foofile.container_source, self.store_path[0])
 
-        with ZarrIO(self.paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store[1], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile = read_io.read()
-            self.assertEqual(read_foofile.container_source, self.paths[1])
+            self.assertEqual(read_foofile.container_source, self.store_path[1])
             self.assertContainerEqual(foofile, read_foofile, ignore_hdmf_attrs=True)
 
     def test_container_part(self):
         """Test that exporting a part of a written container raises an error."""
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile = read_io.read()
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+            with ZarrIO(self.store[1], mode='w') as export_io:
                 msg = ("The provided container must be the root of the hierarchy of the source used to read the "
                        "container.")
                 with self.assertRaisesWith(ValueError, msg):
                     export_io.export(src_io=read_io, container=read_foofile.buckets['bucket1'])
 
     def test_container_unknown(self):
         """Test that exporting a container that did not come from the src_io object raises an error."""
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+            with ZarrIO(self.store[1], mode='w') as export_io:
                 dummy_file = FooFile(buckets=[])
                 msg = "The provided container must have been read by the provided src_io."
                 with self.assertRaisesWith(ValueError, msg):
                     export_io.export(src_io=read_io, container=dummy_file)
 
     def test_cache_spec_disabled(self):
         """Test that exporting with cache_spec disabled works."""
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile, cache_spec=False)
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile = read_io.read()
 
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+            with ZarrIO(self.store[1], mode='w') as export_io:
                 export_io.export(
                     src_io=read_io,
                     container=read_foofile,
                     cache_spec=False)
-        self.assertFalse(os.path.exists(os.path.join(self.paths[1], 'specifications')))
+        self.assertFalse(os.path.exists(os.path.join(self.store_path[1], 'specifications')))
 
     def test_cache_spec_enabled(self):
         """Test that exporting with cache_spec works."""
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile = read_io.read()
 
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+            with ZarrIO(self.store[1], mode='w') as export_io:
                 export_io.export(
                     src_io=read_io,
                     container=read_foofile,
                     cache_spec=True)
-        self.assertTrue(os.path.exists(os.path.join(self.paths[1], 'specifications')))
+
+        with zarr.open(self.store[1], mode='r') as zarr_io:
+            self.assertTrue('specifications' in zarr_io.keys())
 
     def test_soft_link_group(self):
         """
         Test that exporting a written file with soft linked groups keeps links within the file." ,i.e, we have
         a group that links to a group in the same file and the new file after export should then have a link to the
         same group but in the new file """
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket], foo_link=foo1)
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+            with ZarrIO(self.store[1], mode='w') as export_io:
                 export_io.export(src_io=read_io, write_args=dict(link_data=False))
-        with ZarrIO(self.paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store[1], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile2 = read_io.read()
             # make sure the linked group is within the same file
-            self.assertEqual(read_foofile2.foo_link.container_source, self.paths[1])
-            zarr_linkspec1 = zarr.open(self.paths[0])['links'].attrs.asdict()['zarr_link'][0]
-            zarr_linkspec2 = zarr.open(self.paths[1])['links'].attrs.asdict()['zarr_link'][0]
+            self.assertEqual(read_foofile2.foo_link.container_source, self.store_path[1])
+            zarr_linkspec1 = zarr.open(self.store_path[0])['links'].attrs.asdict()['zarr_link'][0]
+            zarr_linkspec2 = zarr.open(self.store_path[1])['links'].attrs.asdict()['zarr_link'][0]
             self.assertEqual(zarr_linkspec1.pop('source'), ".")
             self.assertEqual(zarr_linkspec2.pop('source'), ".")
             self.assertDictEqual(zarr_linkspec1, zarr_linkspec2)
 
     def test_soft_link_dataset(self):
         """Test that exporting a written file with soft linked datasets keeps links within the file."""
         """Link to a dataset in the same file should have a link to the same new dataset in the new file """
         pass  # TODO this test currently fails. It does not create a SoftLink in the original file.
         """
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket], foofile_data=foo1.my_data)
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile, link_data=True)
         print ("WRITE DONE")
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+            with ZarrIO(self.store_paths[1], mode='w') as export_io:
                 export_io.export(src_io=read_io, write_args=dict(link_data=False))
-        print(zarr.open(self.paths[0]).tree())
-        print(zarr.open(self.paths[1]).tree())
-        with ZarrIO(self.paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
+        print(zarr.open(self.store_paths[0]).tree())
+        print(zarr.open(self.store_paths[1]).tree())
+        with ZarrIO(self.store_paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile2 = read_io.read()
             # make sure the linked dataset is within the same file
-            print(open(self.paths[1]+"/buckets/bucket1/foo_holder/foo1/.zattrs", 'r').read())
-            self.assertEqual(read_foofile2.foofile_data.path, self.paths[1])
+            print(open(self.source_paths[1]+"/buckets/bucket1/foo_holder/foo1/.zattrs", 'r').read())
+            self.assertEqual(read_foofile2.foofile_data.path, self.source_paths[1])
         """
 
     def test_external_link_group(self):
         """Test that exporting a written file with external linked groups maintains the links."""
         """External links remain"""
         pass  # TODO this test currently fails. The external link is changed to point to File 2 instead of File 1
         """
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
         # Create File 1 with the full data
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as read_io:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='w') as read_io:
             read_io.write(foofile)
         # Create file 2 with an external link to File 1
         manager = get_foo_buildmanager()
-        with ZarrIO(self.paths[0], manager=manager, mode='r') as read_io:
+        with ZarrIO(self.store_paths[0], manager=manager, mode='r') as read_io:
             read_foofile = read_io.read()
             # make external link to existing group
             foofile2 = FooFile(foo_link=read_foofile.buckets['bucket1'].foos['foo1'])
             print("-------------------Write File 2----------------------------")
-            with ZarrIO(self.paths[1], manager=manager, mode='w') as write_io:
+            with ZarrIO(self.store_paths[1], manager=manager, mode='w') as write_io:
                 write_io.write(foofile2)
-            self.assertDictEqual(zarr.open(self.paths[1])['links'].attrs.asdict(),
+            self.assertDictEqual(zarr.open(self.store_paths[1])['links'].attrs.asdict(),
                                  {'zarr_link': [{'name': 'foo_link',
                                                  'path': '/buckets/bucket1/foo_holder/foo1',
-                                                 'source': self.paths[0]}]})
+                                                 'source': self.source_paths[0]}]})
         # Export File 2 to a new File 3 and make sure the external link from File 2 is being preserved
-        with ZarrIO(self.paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
-             with ZarrIO(self.paths[2], mode='w') as export_io:
+        with ZarrIO(self.store_paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
+             with ZarrIO(self.store_paths[2], mode='w') as export_io:
                 print("-------------------Write File 3----------------------------")
                 export_io.export(src_io=read_io)
         #print()
-        print(zarr.open(self.paths[1])['links'].attrs.asdict())
-        print(zarr.open(self.paths[2])['links'].attrs.asdict())
-        with ZarrIO(self.paths[2], manager=get_foo_buildmanager(), mode='r') as read_io:
+        print(zarr.open(self.store_paths[1])['links'].attrs.asdict())
+        print(zarr.open(self.store_paths[2])['links'].attrs.asdict())
+        with ZarrIO(self.store_paths[2], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile2 = read_io.read()
             # make sure the linked group is read from the first file
-            self.assertEqual(read_foofile2.foo_link.container_source, self.paths[0])
+            self.assertEqual(read_foofile2.foo_link.container_source, self.source_paths[0])
         """
 
     def test_external_link_dataset(self):
         """Test that exporting a written file with external linked datasets maintains the links."""
         pass  # TODO this test currently fails
         """
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket], foofile_data=[1, 2, 3])
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
         manager = get_foo_buildmanager()
-        with ZarrIO(self.paths[0], manager=manager, mode='r') as read_io:
+        with ZarrIO(self.store_paths[0], manager=manager, mode='r') as read_io:
             read_foofile = read_io.read()
             # make external link to existing dataset
             foofile2 = FooFile(foofile_data=read_foofile.foofile_data)
-            with ZarrIO(self.paths[1], manager=manager, mode='w') as write_io:
+            with ZarrIO(self.store_paths[1], manager=manager, mode='w') as write_io:
                 write_io.write(foofile2)
-        with ZarrIO(self.paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
-            self.ios.append(read_io)  # track IO objects for tearDown
-            with ZarrIO(self.paths[2], mode='w') as export_io:
+        with ZarrIO(self.store_paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
+            with ZarrIO(self.store_paths[2], mode='w') as export_io:
                 export_io.export(src_io=read_io)
-        with ZarrIO(self.paths[2], manager=get_foo_buildmanager(), mode='r') as read_io:
-            self.ios.append(read_io)  # track IO objects for tearDown
+        with ZarrIO(self.store_paths[2], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile2 = read_io.read()
             # make sure the linked dataset is read from the first file
-            self.assertEqual(read_foofile2.foofile_data.file.filename, self.paths[0])
+            self.assertEqual(read_foofile2.foofile_data.file.filename, self.source_paths[0])
         """
 
     def test_external_link_link(self):
         """Test that exporting a written file with external links to external links maintains the links."""
         pass  # TODO this test currently fails
         """
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
         manager = get_foo_buildmanager()
-        with ZarrIO(self.paths[0], manager=manager, mode='r') as read_io:
+        with ZarrIO(self.store_paths[0], manager=manager, mode='r') as read_io:
             read_foofile = read_io.read()
             # make external link to existing group
             foofile2 = FooFile(foo_link=read_foofile.buckets['bucket1'].foos['foo1'])
-            with ZarrIO(self.paths[1], manager=manager, mode='w') as write_io:
+            with ZarrIO(self.store_paths[1], manager=manager, mode='w') as write_io:
                 write_io.write(foofile2)
         manager = get_foo_buildmanager()
-        with ZarrIO(self.paths[1], manager=manager, mode='r') as read_io:
+        with ZarrIO(self.store_paths[1], manager=manager, mode='r') as read_io:
             read_foofile2 = read_io.read()
             # make external link to external link
             foofile3 = FooFile(foo_link=read_foofile2.foo_link)
-            with ZarrIO(self.paths[2], manager=manager, mode='w') as write_io:
+            with ZarrIO(self.store_paths[2], manager=manager, mode='w') as write_io:
                 write_io.write(foofile3)
-        with ZarrIO(self.paths[2], manager=get_foo_buildmanager(), mode='r') as read_io:
-            with ZarrIO(self.paths[3], mode='w') as export_io:
+        with ZarrIO(self.store_paths[2], manager=get_foo_buildmanager(), mode='r') as read_io:
+            with ZarrIO(self.store_paths[3], mode='w') as export_io:
                 export_io.export(src_io=read_io)
-        with ZarrIO(self.paths[3], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store_paths[3], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile3 = read_io.read()
             # make sure the linked group is read from the first file
-            self.assertEqual(read_foofile3.foo_link.container_source, self.paths[0])
+            self.assertEqual(read_foofile3.foo_link.container_source, self.source_paths[0])
         """
 
     def test_attr_reference(self):
         """Test that exporting a written file with attribute references maintains the references."""
         """Attribute with object reference needs to point to the new object in the new file"""
         pass  # TODO this test currently fails because the paths in the attribute still points to the first file
         """
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket], foo_ref_attr=foo1)
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as read_io:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='w') as read_io:
             read_io.write(foofile)
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+            with ZarrIO(self.store_paths[1], mode='w') as export_io:
                 export_io.export(src_io=read_io,  write_args=dict(link_data=False))
-        #with ZarrIO(self.paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
+        #with ZarrIO(self.store_paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
         #    read_foofile2 = read_io.read()
             #self.assertTupleEqual(ZarrIO.get_zarr_paths(read_foofile2.foo_ref_attr.my_data),
-            #                     (self.paths[1], '/buckets/bucket1/foo_holder/foo1/my_data'))
+            #                     (self.source_paths[1], '/buckets/bucket1/foo_holder/foo1/my_data'))
             # make sure the attribute reference resolves to the container within the same file
             #self.assertIs(read_foofile2.foo_ref_attr, read_foofile2.buckets['bucket1'].foos['foo1'])
-        expected_ref = {'value': {'path': '/buckets/bucket1/foo_holder/foo1', 'source': self.paths[1]},
+        expected_ref = {'value': {'path': '/buckets/bucket1/foo_holder/foo1', 'source': self.source_paths[1]},
                         'zarr_dtype': 'object'}
-        real_ref = zarr.open(self.paths[1]).attrs['foo_ref_attr']
+        real_ref = zarr.open(self.store_paths[1]).attrs['foo_ref_attr']
         self.assertDictEqual(real_ref, expected_ref)
         """
 
     def test_pop_data(self):
         """Test that exporting a written container after removing an element from it works."""
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile = read_io.read()
             read_foofile.remove_bucket('bucket1')  # remove child group
 
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+            with ZarrIO(self.store[1], mode='w') as export_io:
                 export_io.export(src_io=read_io, container=read_foofile)
 
-        with ZarrIO(self.paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store[1], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile2 = read_io.read()
 
             # make sure the read foofile has no buckets
             self.assertDictEqual(read_foofile2.buckets, {})
 
         # check that file size of file 2 is smaller
-        dirsize1 = total_directory_size(self.paths[0])
-        dirsize2 = total_directory_size(self.paths[1])
+        dirsize1 = total_size(self.store_path[0])
+        dirsize2 = total_size(self.store_path[1])
         self.assertTrue(dirsize1 > dirsize2)
 
     def test_pop_linked_group(self):
         """Test that exporting a written container after removing a linked element from it works."""
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket], foo_link=foo1)
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile = read_io.read()
             read_foofile.buckets['bucket1'].remove_foo('foo1')  # remove child group
 
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+            with ZarrIO(self.store[1], mode='w') as export_io:
                 msg = ("links (links): Linked Foo 'foo1' has no parent. Remove the link or ensure the linked "
                        "container is added properly.")
                 with self.assertRaisesWith(OrphanContainerBuildError, msg):
                     export_io.export(src_io=read_io, container=read_foofile)
 
     def test_append_data(self):
         """Test that exporting a written container after adding groups, links, and references to it works."""
@@ -1087,154 +1235,153 @@
         #       created here and currently fails. I.e,. it fails in list_fill but instead we should actually
         #       create an external link instead
         pass
         """
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile = read_io.read()
             # create a foo with link to existing dataset my_data, add the foo to new foobucket
             # this should make a soft link within the exported file
             # TODO Assigning my_data is the problem. Which in turn causes the export to fail because the Zarr
             # DataType is not being understood. This is where the External link should be cerated instead?
             foo2 = Foo('foo2', read_foofile.buckets['bucket1'].foos['foo1'].my_data, "I am foo2", 17, 3.14)
             foobucket2 = FooBucket('bucket2', [foo2])
             read_foofile.add_bucket(foobucket2)
             # also add link from foofile to new foo2 container
             read_foofile.foo_link = foo2
             # also add link from foofile to new foo2.my_data dataset which is a link to foo1.my_data dataset
             read_foofile.foofile_data = foo2.my_data
             # also add reference from foofile to new foo2
             read_foofile.foo_ref_attr = foo2
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+            with ZarrIO(self.store_paths[1], mode='w') as export_io:
                 export_io.export(src_io=read_io, container=read_foofile)
-        with ZarrIO(self.paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
+        with ZarrIO(self.store_paths[1], manager=get_foo_buildmanager(), mode='r') as read_io:
             read_foofile2 = read_io.read()
             # test new soft link to dataset in file
             self.assertIs(read_foofile2.buckets['bucket1'].foos['foo1'].my_data,
                           read_foofile2.buckets['bucket2'].foos['foo2'].my_data)
             # test new soft link to group in file
             self.assertIs(read_foofile2.foo_link, read_foofile2.buckets['bucket2'].foos['foo2'])
             # test new soft link to new soft link to dataset in file
             self.assertIs(read_foofile2.buckets['bucket1'].foos['foo1'].my_data, read_foofile2.foofile_data)
             # test new attribute reference to new group in file
             self.assertIs(read_foofile2.foo_ref_attr, read_foofile2.buckets['bucket2'].foos['foo2'])
-        #with File(self.paths[1], 'r') as f:
-        #    self.assertEqual(f['foofile_data'].file.filename, self.paths[1])
+        #with File(self.store_paths[1], 'r') as f:
+        #    self.assertEqual(f['foofile_data'].file.filename, self.store_paths[1])
         #    self.assertIsInstance(f.attrs['foo_ref_attr'], h5py.Reference)
         """
 
     def test_append_external_link_data(self):
         """Test that exporting a written container after adding a link with link_data=True creates external links."""
         pass  # TODO: This test currently fails
         """
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
         foofile2 = FooFile(buckets=[])
-        with ZarrIO(self.paths[1], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store_paths[1], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile2)
         manager = get_foo_buildmanager()
-        with ZarrIO(self.paths[0], manager=manager, mode='r') as read_io1:
+        with ZarrIO(self.store_paths[0], manager=manager, mode='r') as read_io1:
             read_foofile1 = read_io1.read()
-            with ZarrIO(self.paths[1], manager=manager, mode='r') as read_io2:
+            with ZarrIO(self.store_paths[1], manager=manager, mode='r') as read_io2:
                 read_foofile2 = read_io2.read()
                 # create a foo with link to existing dataset my_data (not in same file), add the foo to new foobucket
                 # this should make an external link within the exported file
                 foo2 = Foo('foo2', read_foofile1.buckets['bucket1'].foos['foo1'].my_data, "I am foo2", 17, 3.14)
                 foobucket2 = FooBucket('bucket2', [foo2])
                 read_foofile2.add_bucket(foobucket2)
                 # also add link from foofile to new foo2.my_data dataset which is a link to foo1.my_data dataset
                 # this should make an external link within the exported file
                 read_foofile2.foofile_data = foo2.my_data
-                with ZarrIO(self.paths[2], mode='w') as export_io:
+                with ZarrIO(self.store_paths[2], mode='w') as export_io:
                     export_io.export(src_io=read_io2, container=read_foofile2)
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io1:
-            self.ios.append(read_io1)  # track IO objects for tearDown
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='r') as read_io1:
             read_foofile3 = read_io1.read()
-            with ZarrIO(self.paths[2], manager=get_foo_buildmanager(), mode='r') as read_io2:
+            with ZarrIO(self.store_paths[2], manager=get_foo_buildmanager(), mode='r') as read_io2:
                 read_foofile4 = read_io2.read()
                 self.assertEqual(read_foofile4.buckets['bucket2'].foos['foo2'].my_data,
                                  read_foofile3.buckets['bucket1'].foos['foo1'].my_data)
                 self.assertEqual(read_foofile4.foofile_data, read_foofile3.buckets['bucket1'].foos['foo1'].my_data)
-        #with File(self.paths[2], 'r') as f:
-        #    self.assertEqual(f['buckets/bucket2/foo_holder/foo2/my_data'].file.filename, self.paths[0])
-        #    self.assertEqual(f['foofile_data'].file.filename, self.paths[0])
+        #with File(self.source_paths[2], 'r') as f:
+        #    self.assertEqual(f['buckets/bucket2/foo_holder/foo2/my_data'].file.filename, self.source_paths[0])
+        #    self.assertEqual(f['foofile_data'].file.filename, self.souce_paths[0])
         #    self.assertIsInstance(f.get('buckets/bucket2/foo_holder/foo2/my_data', getlink=True),
         #                          h5py.ExternalLink)
         #    self.assertIsInstance(f.get('foofile_data', getlink=True), h5py.ExternalLink)
         """
 
     def test_append_external_link_copy_data(self):
         """Test that exporting a written container after adding a link with link_data=False copies the data."""
         pass  # TODO: This test currently fails
         """
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
         foofile2 = FooFile(buckets=[])
-        with ZarrIO(self.paths[1], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store_paths[1], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile2)
         manager = get_foo_buildmanager()
-        with ZarrIO(self.paths[0], manager=manager, mode='r') as read_io1:
+        with ZarrIO(self.store_paths[0], manager=manager, mode='r') as read_io1:
             read_foofile1 = read_io1.read()
-            with ZarrIO(self.paths[1], manager=manager, mode='r') as read_io2:
+            with ZarrIO(self.store_paths[1], manager=manager, mode='r') as read_io2:
                 read_foofile2 = read_io2.read()
                 # create a foo with link to existing dataset my_data (not in same file), add the foo to new foobucket
                 # this would normally make an external link but because link_data=False, data will be copied
                 foo2 = Foo('foo2', read_foofile1.buckets['bucket1'].foos['foo1'].my_data, "I am foo2", 17, 3.14)
                 foobucket2 = FooBucket('bucket2', [foo2])
                 read_foofile2.add_bucket(foobucket2)
                 # also add link from foofile to new foo2.my_data dataset which is a link to foo1.my_data dataset
                 # this would normally make an external link but because link_data=False, data will be copied
                 read_foofile2.foofile_data = foo2.my_data
-                with ZarrIO(self.paths[2], mode='w') as export_io:
+                with ZarrIO(self.store_paths[2], mode='w') as export_io:
                     export_io.export(src_io=read_io2, container=read_foofile2, write_args={'link_data': False})
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='r') as read_io1:
+        with ZarrIO(self.store_paths[0], manager=get_foo_buildmanager(), mode='r') as read_io1:
             read_foofile3 = read_io1.read()
-            with ZarrIO(self.paths[2], manager=get_foo_buildmanager(), mode='r') as read_io2:
+            with ZarrIO(self.store_paths[2], manager=get_foo_buildmanager(), mode='r') as read_io2:
                 read_foofile4 = read_io2.read()
                 # check that file can be read
                 self.assertNotEqual(read_foofile4.buckets['bucket2'].foos['foo2'].my_data,
                                     read_foofile3.buckets['bucket1'].foos['foo1'].my_data)
                 self.assertNotEqual(read_foofile4.foofile_data, read_foofile3.buckets['bucket1'].foos['foo1'].my_data)
                 self.assertNotEqual(read_foofile4.foofile_data, read_foofile4.buckets['bucket2'].foos['foo2'].my_data)
-        # with File(self.paths[2], 'r') as f:
-        #    self.assertEqual(f['buckets/bucket2/foo_holder/foo2/my_data'].file.filename, self.paths[2])
-        #    self.assertEqual(f['foofile_data'].file.filename, self.paths[2])
+        # with File(self.source_paths[2], 'r') as f:
+        #    self.assertEqual(f['buckets/bucket2/foo_holder/foo2/my_data'].file.filename, self.source_paths[2])
+        #    self.assertEqual(f['foofile_data'].file.filename, self.source_paths[2])
         """
 
     def test_export_dset_refs(self):
         """Test that exporting a written container with a dataset of references works."""
         pass  # TODO: This test currently fails
         """
         bazs = []
         num_bazs = 10
         for i in range(num_bazs):
             bazs.append(Baz(name='baz%d' % i))
         baz_data = BazData(name='baz_data1', data=bazs)
         bucket = BazBucket(name='bucket1', bazs=bazs.copy(), baz_data=baz_data)
-        with ZarrIO(self.paths[0], manager=_get_baz_manager(), mode='w') as write_io:
+        with ZarrIO(self.store_paths[0], manager=_get_baz_manager(), mode='w') as write_io:
             write_io.write(bucket)
-        with ZarrIO(self.paths[0], manager=_get_baz_manager(), mode='r') as read_io:
+        with ZarrIO(self.store_paths[0], manager=_get_baz_manager(), mode='r') as read_io:
             read_bucket1 = read_io.read()
             # NOTE: reference IDs might be the same between two identical files
             # adding a Baz with a smaller name should change the reference IDs on export
             new_baz = Baz(name='baz000')
             read_bucket1.add_baz(new_baz)
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+            with ZarrIO(self.store_paths[1], mode='w') as export_io:
                 export_io.export(src_io=read_io, container=read_bucket1)
-        with ZarrIO(self.paths[1], manager=_get_baz_manager(), mode='r') as read_io:
+        with ZarrIO(self.store_paths[1], manager=_get_baz_manager(), mode='r') as read_io:
             read_bucket2 = read_io.read()
             # remove and check the appended child, then compare the read container with the original
             read_new_baz = read_bucket2.remove_baz('baz000')
             self.assertContainerEqual(new_baz, read_new_baz, ignore_hdmf_attrs=True)
             self.assertContainerEqual(bucket, read_bucket2, ignore_name=True, ignore_hdmf_attrs=True)
             for i in range(num_bazs):
                 baz_name = 'baz%d' % i
@@ -1250,25 +1397,25 @@
         num_bazs = 10
         for i in range(num_bazs):
             b = Baz(name='baz%d' % i)
             bazs.append(b)
             baz_pairs.append((i, b))
         baz_cpd_data = BazCpdData(name='baz_cpd_data1', data=baz_pairs)
         bucket = BazBucket(name='bucket1', bazs=bazs.copy(), baz_cpd_data=baz_cpd_data)
-        with ZarrIO(self.paths[0], manager=_get_baz_manager(), mode='w') as write_io:
+        with ZarrIO(self.store_paths[0], manager=_get_baz_manager(), mode='w') as write_io:
             write_io.write(bucket)
-        with ZarrIO(self.paths[0], manager=_get_baz_manager(), mode='r') as read_io:
+        with ZarrIO(self.store_paths[0], manager=_get_baz_manager(), mode='r') as read_io:
             read_bucket1 = read_io.read()
             # NOTE: reference IDs might be the same between two identical files
             # adding a Baz with a smaller name should change the reference IDs on export
             new_baz = Baz(name='baz000')
             read_bucket1.add_baz(new_baz)
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+            with ZarrIO(self.store_paths[1], mode='w') as export_io:
                 export_io.export(src_io=read_io, container=read_bucket1)
-        with ZarrIO(self.paths[1], manager=_get_baz_manager(), mode='r') as read_io:
+        with ZarrIO(self.store_paths[1], manager=_get_baz_manager(), mode='r') as read_io:
             read_bucket2 = read_io.read()
             # remove and check the appended child, then compare the read container with the original
             read_new_baz = read_bucket2.remove_baz(new_baz.name)
             self.assertContainerEqual(new_baz, read_new_baz, ignore_hdmf_attrs=True)
             self.assertContainerEqual(bucket, read_bucket2, ignore_name=True, ignore_hdmf_attrs=True)
             for i in range(num_bazs):
                 baz_name = 'baz%d' % i
@@ -1278,76 +1425,84 @@
 
     def test_non_manager_container(self):
         """Test that exporting with a src_io without a manager raises an error."""
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
 
         class OtherIO(HDMFIO):
 
+            @staticmethod
+            def can_read(path):
+                pass
+
             def read_builder(self):
                 pass
 
             def write_builder(self, **kwargs):
                 pass
 
             def open(self):
                 pass
 
             def close(self):
                 pass
 
         with OtherIO() as read_io:
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+            with ZarrIO(self.store[1], mode='w') as export_io:
                 msg = 'When a container is provided, src_io must have a non-None manager (BuildManager) property.'
                 with self.assertRaisesWith(ValueError, msg):
                     export_io.export(src_io=read_io, container=foofile, write_args={'link_data': False})
 
     def test_non_Zarr_src_link_data_true(self):
         """Test that exporting with a src_io without a manager raises an error."""
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
 
         class OtherIO(HDMFIO):
 
             def __init__(self, manager):
                 super().__init__(manager=manager)
 
+            @staticmethod
+            def can_read(path):
+                pass
+
             def read_builder(self):
                 pass
 
             def write_builder(self, **kwargs):
                 pass
 
             def open(self):
                 pass
 
             def close(self):
                 pass
 
         with OtherIO(manager=get_foo_buildmanager()) as read_io:
-            with ZarrIO(self.paths[1], mode='w') as export_io:
+            with ZarrIO(self.store[1], mode='w') as export_io:
                 msg = "Cannot export from non-Zarr backend OtherIO to Zarr with write argument link_data=True."
                 with self.assertRaisesWith(UnsupportedOperation, msg):
                     export_io.export(src_io=read_io, container=foofile)
 
     def test_wrong_mode(self):
         """Test that exporting with a src_io without a manager raises an error."""
         foo1 = Foo('foo1', [1, 2, 3, 4, 5], "I am foo1", 17, 3.14)
         foobucket = FooBucket('bucket1', [foo1])
         foofile = FooFile(buckets=[foobucket])
 
-        with ZarrIO(self.paths[0], manager=get_foo_buildmanager(), mode='w') as write_io:
+        with ZarrIO(self.store[0], manager=get_foo_buildmanager(), mode='w') as write_io:
             write_io.write(foofile)
 
-        with ZarrIO(self.paths[0], mode='r') as read_io:
-            with ZarrIO(self.paths[1], mode='a') as export_io:
-                msg = "Cannot export to file %s in mode 'a'. Please use mode 'w'." % self.paths[1]
+        with ZarrIO(self.store[0], mode='r') as read_io:
+            with ZarrIO(self.store[1], mode='a') as export_io:
+                msg = "Cannot export to file %s in mode 'a'. Please use mode 'w'." % self.store_path[1]
                 with self.assertRaisesWith(UnsupportedOperation, msg):
                     export_io.export(src_io=read_io)
```

### Comparing `hdmf_zarr-0.2.0/tests/unit/utils.py` & `hdmf_zarr-0.3.0/tests/unit/utils.py`

 * *Files identical despite different names*

### Comparing `hdmf_zarr-0.2.0/versioneer.py` & `hdmf_zarr-0.3.0/versioneer.py`

 * *Files identical despite different names*

