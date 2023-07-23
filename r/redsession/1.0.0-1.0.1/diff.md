# Comparing `tmp/redsession-1.0.0.tar.gz` & `tmp/redsession-1.0.1.tar.gz`

## Comparing `redsession-1.0.0.tar` & `redsession-1.0.1.tar`

### file list

```diff
@@ -1,17 +1,17 @@
--rw-r--r--   0        0        0      545 2020-02-02 00:00:00.000000 redsession-1.0.0/.pre-commit-config.yaml
--rw-r--r--   0        0        0      604 2020-02-02 00:00:00.000000 redsession-1.0.0/.readthedocs.yaml
--rw-r--r--   0        0        0       55 2020-02-02 00:00:00.000000 redsession-1.0.0/requirements-docs.txt
--rw-r--r--   0        0        0      128 2020-02-02 00:00:00.000000 redsession-1.0.0/requirements-tests.txt
--rw-r--r--   0        0        0       93 2020-02-02 00:00:00.000000 redsession-1.0.0/requirements.txt
--rw-r--r--   0        0        0       98 2020-02-02 00:00:00.000000 redsession-1.0.0/redsession/__init__.py
--rw-r--r--   0        0        0     5964 2020-02-02 00:00:00.000000 redsession-1.0.0/redsession/middleware.py
--rw-r--r--   0        0        0      103 2020-02-02 00:00:00.000000 redsession-1.0.0/redsession/backend/__init__.py
--rw-r--r--   0        0        0     2080 2020-02-02 00:00:00.000000 redsession-1.0.0/redsession/backend/base.py
--rw-r--r--   0        0        0     1054 2020-02-02 00:00:00.000000 redsession-1.0.0/redsession/backend/redis.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 redsession-1.0.0/tests/__init__.py
--rw-r--r--   0        0        0     3309 2020-02-02 00:00:00.000000 redsession-1.0.0/tests/test_session.py
--rw-r--r--   0        0        0      102 2020-02-02 00:00:00.000000 redsession-1.0.0/.gitignore
--rw-r--r--   0        0        0     1068 2020-02-02 00:00:00.000000 redsession-1.0.0/LICENSE.md
--rw-r--r--   0        0        0     1075 2020-02-02 00:00:00.000000 redsession-1.0.0/README.rst
--rw-r--r--   0        0        0     1114 2020-02-02 00:00:00.000000 redsession-1.0.0/pyproject.toml
--rw-r--r--   0        0        0     2046 2020-02-02 00:00:00.000000 redsession-1.0.0/PKG-INFO
+-rw-r--r--   0        0        0      545 2020-02-02 00:00:00.000000 redsession-1.0.1/.pre-commit-config.yaml
+-rw-r--r--   0        0        0      641 2020-02-02 00:00:00.000000 redsession-1.0.1/.readthedocs.yaml
+-rw-r--r--   0        0        0       55 2020-02-02 00:00:00.000000 redsession-1.0.1/requirements-docs.txt
+-rw-r--r--   0        0        0      128 2020-02-02 00:00:00.000000 redsession-1.0.1/requirements-tests.txt
+-rw-r--r--   0        0        0       93 2020-02-02 00:00:00.000000 redsession-1.0.1/requirements.txt
+-rw-r--r--   0        0        0       98 2020-02-02 00:00:00.000000 redsession-1.0.1/redsession/__init__.py
+-rw-r--r--   0        0        0     5964 2020-02-02 00:00:00.000000 redsession-1.0.1/redsession/middleware.py
+-rw-r--r--   0        0        0      103 2020-02-02 00:00:00.000000 redsession-1.0.1/redsession/backend/__init__.py
+-rw-r--r--   0        0        0     2080 2020-02-02 00:00:00.000000 redsession-1.0.1/redsession/backend/base.py
+-rw-r--r--   0        0        0     1054 2020-02-02 00:00:00.000000 redsession-1.0.1/redsession/backend/redis.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 redsession-1.0.1/tests/__init__.py
+-rw-r--r--   0        0        0     3309 2020-02-02 00:00:00.000000 redsession-1.0.1/tests/test_session.py
+-rw-r--r--   0        0        0      102 2020-02-02 00:00:00.000000 redsession-1.0.1/.gitignore
+-rw-r--r--   0        0        0     1068 2020-02-02 00:00:00.000000 redsession-1.0.1/LICENSE.md
+-rw-r--r--   0        0        0     1320 2020-02-02 00:00:00.000000 redsession-1.0.1/README.rst
+-rw-r--r--   0        0        0     1169 2020-02-02 00:00:00.000000 redsession-1.0.1/pyproject.toml
+-rw-r--r--   0        0        0     2356 2020-02-02 00:00:00.000000 redsession-1.0.1/PKG-INFO
```

### Comparing `redsession-1.0.0/.pre-commit-config.yaml` & `redsession-1.0.1/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `redsession-1.0.0/.readthedocs.yaml` & `redsession-1.0.1/.readthedocs.yaml`

 * *Files 14% similar despite different names*

```diff
@@ -16,7 +16,8 @@
 
 # Optional but recommended, declare the Python requirements required
 # to build your documentation
 # See https://docs.readthedocs.io/en/stable/guides/reproducible-builds.html
 python:
   install:
     - requirements: requirements-docs.txt
+    - requirements: requirements.txt
```

### Comparing `redsession-1.0.0/redsession/middleware.py` & `redsession-1.0.1/redsession/middleware.py`

 * *Files identical despite different names*

### Comparing `redsession-1.0.0/redsession/backend/base.py` & `redsession-1.0.1/redsession/backend/base.py`

 * *Files identical despite different names*

### Comparing `redsession-1.0.0/redsession/backend/redis.py` & `redsession-1.0.1/redsession/backend/redis.py`

 * *Files identical despite different names*

### Comparing `redsession-1.0.0/tests/test_session.py` & `redsession-1.0.1/tests/test_session.py`

 * *Files identical despite different names*

### Comparing `redsession-1.0.0/LICENSE.md` & `redsession-1.0.1/LICENSE.md`

 * *Files identical despite different names*

### Comparing `redsession-1.0.0/README.rst` & `redsession-1.0.1/README.rst`

 * *Files 22% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-.. image:: https://github.com/TheJecksMan/red-session/blob/main/docs/_static/logo_lib.png
+.. image:: https://raw.githubusercontent.com/TheJecksMan/red-session/main/docs/_static/logo_lib.png
    :align: center
    :alt: red-session logo
    :width: 200
 
 .. image:: https://img.shields.io/pypi/pyversions/redsession
    :target: https://pypi.org/project/redsession/
    :alt: PyPI - Python Version
@@ -11,26 +11,30 @@
    :target: https://pypi.org/project/redsession/
    :alt: PyPI - License
 
 .. image:: https://img.shields.io/pypi/v/redsession
    :target: https://pypi.org/project/redsession/
    :alt: PyPI
 
+.. image:: https://readthedocs.org/projects/red-session/badge/?version=latest
+   :target: https://red-session.readthedocs.io/en/latest/?badge=latest
+   :alt: Documentation Status
+
 
 Introduction
 ============
 
 This async library provides the ability to quickly integrate server sessions into
 your application through the use of middleware. The library is compatible with python 3.8+.
 
 
 Note
 ----
 
-This library is designed for such frameworks as: FastAPI and Starlette.
+This library is designed for such frameworks as: **FastAPI and Starlette**.
 
 Dependencies used support redis version 5.0+
 
 Installation
 ============
 
 You can install or update starlette-middleware
@@ -39,8 +43,8 @@
 
     $ pip install redsession --upgrade
 
 
 Documentation
 =============
 
-You can find more information on usage here.
+You can find more information on usage `here <https://red-session.readthedocs.io/en/stable/>`_.
```

### Comparing `redsession-1.0.0/pyproject.toml` & `redsession-1.0.1/pyproject.toml`

 * *Files 9% similar despite different names*

```diff
@@ -30,14 +30,15 @@
     "itsdangerous>=2.1.2",
     "redis[hiredis]>=4.6.0",
     "orjson>=3.9.0",
 ]
 
 [project.urls]
 Repository = "https://github.com/TheJecksMan/red-session"
+Docs = "https://red-session.readthedocs.io/en/stable/"
 
 
 [tool.hatch.version]
 path = "redsession/__init__.py"
 
 [tool.hatch.build.targets.sdist]
 exclude = ["/.github", "/docs", "/examples"]
```

### Comparing `redsession-1.0.0/PKG-INFO` & `redsession-1.0.1/PKG-INFO`

 * *Files 19% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 Metadata-Version: 2.1
 Name: redsession
-Version: 1.0.0
+Version: 1.0.1
 Summary: Simple and fastest library for Redis server sessions
 Project-URL: Repository, https://github.com/TheJecksMan/red-session
+Project-URL: Docs, https://red-session.readthedocs.io/en/stable/
 Author: TheJecksMan
 License-Expression: MIT
 License-File: LICENSE.md
 Classifier: Development Status :: 4 - Beta
 Classifier: Framework :: FastAPI
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -20,15 +21,15 @@
 Requires-Python: >=3.8
 Requires-Dist: itsdangerous>=2.1.2
 Requires-Dist: orjson>=3.9.0
 Requires-Dist: redis[hiredis]>=4.6.0
 Requires-Dist: starlette>=0.27.0
 Description-Content-Type: text/x-rst
 
-.. image:: https://github.com/TheJecksMan/red-session/blob/main/docs/_static/logo_lib.png
+.. image:: https://raw.githubusercontent.com/TheJecksMan/red-session/main/docs/_static/logo_lib.png
    :align: center
    :alt: red-session logo
    :width: 200
 
 .. image:: https://img.shields.io/pypi/pyversions/redsession
    :target: https://pypi.org/project/redsession/
    :alt: PyPI - Python Version
@@ -37,26 +38,30 @@
    :target: https://pypi.org/project/redsession/
    :alt: PyPI - License
 
 .. image:: https://img.shields.io/pypi/v/redsession
    :target: https://pypi.org/project/redsession/
    :alt: PyPI
 
+.. image:: https://readthedocs.org/projects/red-session/badge/?version=latest
+   :target: https://red-session.readthedocs.io/en/latest/?badge=latest
+   :alt: Documentation Status
+
 
 Introduction
 ============
 
 This async library provides the ability to quickly integrate server sessions into
 your application through the use of middleware. The library is compatible with python 3.8+.
 
 
 Note
 ----
 
-This library is designed for such frameworks as: FastAPI and Starlette.
+This library is designed for such frameworks as: **FastAPI and Starlette**.
 
 Dependencies used support redis version 5.0+
 
 Installation
 ============
 
 You can install or update starlette-middleware
@@ -65,8 +70,8 @@
 
     $ pip install redsession --upgrade
 
 
 Documentation
 =============
 
-You can find more information on usage here.
+You can find more information on usage `here <https://red-session.readthedocs.io/en/stable/>`_.
```

