# Comparing `tmp/netlify-python-0.1.1.tar.gz` & `tmp/netlify-python-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "netlify-python-0.1.1.tar", last modified: Mon Nov 14 15:50:03 2022, max compression
+gzip compressed data, was "netlify-python-0.2.0.tar", last modified: Sat Jul 22 23:10:48 2023, max compression
```

## Comparing `netlify-python-0.1.1.tar` & `netlify-python-0.2.0.tar`

### file list

```diff
@@ -1,26 +1,27 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-14 15:50:03.774840 netlify-python-0.1.1/
--rw-r--r--   0 runner    (1001) docker     (121)     1063 2022-11-14 15:49:36.000000 netlify-python-0.1.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)     3278 2022-11-14 15:50:03.774840 netlify-python-0.1.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     2613 2022-11-14 15:49:36.000000 netlify-python-0.1.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-14 15:50:03.770841 netlify-python-0.1.1/netlify/
--rw-r--r--   0 runner    (1001) docker     (121)       92 2022-11-14 15:49:36.000000 netlify-python-0.1.1/netlify/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)       83 2022-11-14 15:49:36.000000 netlify-python-0.1.1/netlify/__main__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-14 15:50:03.770841 netlify-python-0.1.1/netlify/auth/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-11-14 15:49:36.000000 netlify-python-0.1.1/netlify/auth/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      391 2022-11-14 15:49:36.000000 netlify-python-0.1.1/netlify/auth/bearer.py
--rw-r--r--   0 runner    (1001) docker     (121)     5030 2022-11-14 15:49:36.000000 netlify-python-0.1.1/netlify/client.py
--rw-r--r--   0 runner    (1001) docker     (121)      114 2022-11-14 15:49:36.000000 netlify-python-0.1.1/netlify/enums.py
--rw-r--r--   0 runner    (1001) docker     (121)      638 2022-11-14 15:49:36.000000 netlify-python-0.1.1/netlify/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-11-14 15:49:36.000000 netlify-python-0.1.1/netlify/py.typed
--rw-r--r--   0 runner    (1001) docker     (121)     3417 2022-11-14 15:49:36.000000 netlify-python-0.1.1/netlify/schemas.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-14 15:50:03.770841 netlify-python-0.1.1/netlify/util/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-11-14 15:49:36.000000 netlify-python-0.1.1/netlify/util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     5754 2022-11-14 15:49:36.000000 netlify-python-0.1.1/netlify/util/extended_dataclass.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-11-14 15:50:03.770841 netlify-python-0.1.1/netlify_python.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     3278 2022-11-14 15:50:03.000000 netlify-python-0.1.1/netlify_python.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      462 2022-11-14 15:50:03.000000 netlify-python-0.1.1/netlify_python.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-11-14 15:50:03.000000 netlify-python-0.1.1/netlify_python.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)      206 2022-11-14 15:50:03.000000 netlify-python-0.1.1/netlify_python.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)        8 2022-11-14 15:50:03.000000 netlify-python-0.1.1/netlify_python.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)     1678 2022-11-14 15:49:36.000000 netlify-python-0.1.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-11-14 15:50:03.774840 netlify-python-0.1.1/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:10:48.032120 netlify-python-0.2.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-07-22 23:10:16.000000 netlify-python-0.2.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3331 2023-07-22 23:10:48.032120 netlify-python-0.2.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2666 2023-07-22 23:10:16.000000 netlify-python-0.2.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:10:48.028120 netlify-python-0.2.0/netlify/
+-rw-r--r--   0 runner    (1001) docker     (123)       92 2023-07-22 23:10:16.000000 netlify-python-0.2.0/netlify/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       83 2023-07-22 23:10:16.000000 netlify-python-0.2.0/netlify/__main__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:10:48.032120 netlify-python-0.2.0/netlify/auth/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 23:10:16.000000 netlify-python-0.2.0/netlify/auth/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      400 2023-07-22 23:10:16.000000 netlify-python-0.2.0/netlify/auth/bearer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3828 2023-07-22 23:10:16.000000 netlify-python-0.2.0/netlify/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-07-22 23:10:16.000000 netlify-python-0.2.0/netlify/enums.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1005 2023-07-22 23:10:16.000000 netlify-python-0.2.0/netlify/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 23:10:16.000000 netlify-python-0.2.0/netlify/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)     3954 2023-07-22 23:10:16.000000 netlify-python-0.2.0/netlify/schemas.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3455 2023-07-22 23:10:16.000000 netlify-python-0.2.0/netlify/transport.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:10:48.032120 netlify-python-0.2.0/netlify_python.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3331 2023-07-22 23:10:48.000000 netlify-python-0.2.0/netlify_python.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      468 2023-07-22 23:10:48.000000 netlify-python-0.2.0/netlify_python.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 23:10:48.000000 netlify-python-0.2.0/netlify_python.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      239 2023-07-22 23:10:48.000000 netlify-python-0.2.0/netlify_python.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-22 23:10:48.000000 netlify-python-0.2.0/netlify_python.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     2085 2023-07-22 23:10:16.000000 netlify-python-0.2.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 23:10:48.032120 netlify-python-0.2.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:10:48.032120 netlify-python-0.2.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     5806 2023-07-22 23:10:16.000000 netlify-python-0.2.0/tests/test_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2755 2023-07-22 23:10:16.000000 netlify-python-0.2.0/tests/test_transport.py
```

### Comparing `netlify-python-0.1.1/LICENSE` & `netlify-python-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `netlify-python-0.1.1/PKG-INFO` & `netlify-python-0.2.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: netlify-python
-Version: 0.1.1
+Version: 0.2.0
 Summary: Bare-bones python library for the official Netlify API
 Author-email: Chris Brousseau <cbrews@users.noreply.github.com>
 License: MIT
 Keywords: http,netlify,client-library
 Classifier: Development Status :: 1 - Planning
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Libraries
@@ -91,14 +91,19 @@
 Everything here out should be in the venv.
 
 Install your dependencies:
 ```bash
 $ pip install .[dev]
 ```
 
+Setup pre-commits:
+```bash
+$ pre-commit install
+```
+
 You should be good to go now.
 
 ### Building the package
 Get your build dependencies in place:
 
 ```bash
 $ pip install .[build]
```

### Comparing `netlify-python-0.1.1/README.md` & `netlify-python-0.2.0/README.md`

 * *Files 7% similar despite different names*

```diff
@@ -72,14 +72,19 @@
 Everything here out should be in the venv.
 
 Install your dependencies:
 ```bash
 $ pip install .[dev]
 ```
 
+Setup pre-commits:
+```bash
+$ pre-commit install
+```
+
 You should be good to go now.
 
 ### Building the package
 Get your build dependencies in place:
 
 ```bash
 $ pip install .[build]
```

### Comparing `netlify-python-0.1.1/netlify/exceptions.py` & `netlify-python-0.2.0/netlify/exceptions.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,27 +1,39 @@
-from dataclasses import dataclass
+from typing import Any
 
-from netlify.util.extended_dataclass import ExtendedDataclass as EDC
+from pydantic import BaseModel
 
 
-@dataclass
-class NetlifyError(EDC):
-    code: int
-    message: str
+class NetlifyErrorSchema(BaseModel):
+    code: int | None = None
+    message: str | None = None
+    errors: dict[str, Any] | None = None
 
 
-class NetlifyException(Exception):
+class NetlifyError(Exception):
     method: str
     path: str
-    code: int
-    message: str
+    code: int | None
+    message: str | None
+    errors: dict[str, Any] | None
 
-    def __init__(self, method: str, path: str, error: NetlifyError):
+    def __init__(self, method: str, path: str, error: NetlifyErrorSchema):
         self.method = method
         self.path = path
         self.code = error.code
         self.message = error.message
+        self.errors = error.errors
 
         super().__init__(
             f"Netlify request to {self.method} {self.path} did not succeed. "
-            f"code: {self.code}, message: '{self.message}'"
+            f"code: {self.code}"
+            if self.code is not None
+            else "" f"message: {self.message}"
+            if self.message is not None
+            else "" f"errors: {self.errors}"
+            if self.errors is not None
+            else ""
         )
+
+
+# Backwards compatibility
+NetlifyException = NetlifyError
```

### Comparing `netlify-python-0.1.1/netlify_python.egg-info/PKG-INFO` & `netlify-python-0.2.0/netlify_python.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: netlify-python
-Version: 0.1.1
+Version: 0.2.0
 Summary: Bare-bones python library for the official Netlify API
 Author-email: Chris Brousseau <cbrews@users.noreply.github.com>
 License: MIT
 Keywords: http,netlify,client-library
 Classifier: Development Status :: 1 - Planning
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Libraries
@@ -91,14 +91,19 @@
 Everything here out should be in the venv.
 
 Install your dependencies:
 ```bash
 $ pip install .[dev]
 ```
 
+Setup pre-commits:
+```bash
+$ pre-commit install
+```
+
 You should be good to go now.
 
 ### Building the package
 Get your build dependencies in place:
 
 ```bash
 $ pip install .[build]
```

### Comparing `netlify-python-0.1.1/pyproject.toml` & `netlify-python-0.2.0/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -7,14 +7,15 @@
 readme = "README.md"
 license = { text = "MIT" }
 requires-python = ">=3.10"
 dynamic = ["version"]
 dependencies = [
   "httpx>=0.23.0",
   "python-dateutil>=2.8.2",
+  "pydantic>1",
 ]
 classifiers = [
   "Development Status :: 1 - Planning",
   "Intended Audience :: Developers",
   "Topic :: Software Development :: Libraries",
   "Programming Language :: Python :: 3.10",
   "Programming Language :: Python :: 3.11",
@@ -24,22 +25,23 @@
   "http", 
   "netlify", 
   "client-library",
 ]
 
 [project.optional-dependencies]
 dev = [
-  "black==22.10.0",
-  "mypy==0.990",
-  "pylint==2.15.5",
-  "isort==5.10.1",
-  "pytest==7.2.0",
-  "types-python-dateutil==2.8.19.3",
-  "pytest-cov==4.0.0",
-  "pytest-httpx==0.21.2",
+  "black==23.7.0",
+  "mypy==1.4.1",
+  "ruff==0.0.277",
+  "pytest==7.4.0",
+  "types-python-dateutil==2.8.19.14",
+  "pytest-cov==4.1.0",
+  "pytest-httpx==0.22.0",
+  "pre-commit==3.3.3",
+  "pytest-mock==3.0.0",
 ]
 build = [
   "build",
   "twine",
 ]
 
 [build-system]
@@ -53,14 +55,15 @@
 
 [tool.isort]
 profile = "black"
 
 [tool.mypy]
 python_version = "3.10"
 
+explicit_package_bases = true
 warn_unused_configs = true
 warn_redundant_casts = true
 
 strict_optional = true
 check_untyped_defs = true
 disallow_untyped_defs = true
 
@@ -80,8 +83,25 @@
   "pragma: no cover",
   "raise NotImplementedError",
   "def __repr__",
   "raise AssertionError",
   "if 0:",
   "if __name__ == .__main__.:",
   "@(abc.)?abstractmethod",
+]
+
+[tool.ruff]
+line-length = 88
+select = [
+  "E",   # pycodestyle errors
+  "W",   # pycodestyle warnings
+  "F",   # pyflakes
+  "Q",   # pyflakes quotes
+  "B",   # bugbear
+  "UP",  # pyupgrade
+  "N",   # PEP-8 naming
+  "I",   # isort
+  "PLC", # pylint conventions
+  "PLE", # pylint conventions
+  "PLW", # pylint conventions
+  "RUF",  
 ]
```

