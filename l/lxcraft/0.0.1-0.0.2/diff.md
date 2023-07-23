# Comparing `tmp/lxcraft-0.0.1.tar.gz` & `tmp/lxcraft-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lxcraft-0.0.1.tar", last modified: Sat Jul 22 15:58:17 2023, max compression
+gzip compressed data, was "lxcraft-0.0.2.tar", last modified: Sun Jul 23 19:55:56 2023, max compression
```

## Comparing `lxcraft-0.0.1.tar` & `lxcraft-0.0.2.tar`

### file list

```diff
@@ -1,40 +1,62 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:58:17.234667 lxcraft-0.0.1/
--rw-r--r--   0 runner    (1001) docker     (123)      558 2023-07-22 15:58:09.000000 lxcraft-0.0.1/.cruft.json
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:58:17.230667 lxcraft-0.0.1/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:58:17.234667 lxcraft-0.0.1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      718 2023-07-22 15:58:09.000000 lxcraft-0.0.1/.github/workflows/multi-test.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      832 2023-07-22 15:58:09.000000 lxcraft-0.0.1/.github/workflows/release.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-07-22 15:58:09.000000 lxcraft-0.0.1/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1246 2023-07-22 15:58:09.000000 lxcraft-0.0.1/.pre-commit-config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-07-22 15:58:09.000000 lxcraft-0.0.1/.python-version
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:58:17.234667 lxcraft-0.0.1/.vscode/
--rw-r--r--   0 runner    (1001) docker     (123)      272 2023-07-22 15:58:09.000000 lxcraft-0.0.1/.vscode/launch.json
--rw-r--r--   0 runner    (1001) docker     (123)      421 2023-07-22 15:58:09.000000 lxcraft-0.0.1/.vscode/settings.json
--rw-r--r--   0 runner    (1001) docker     (123)     1056 2023-07-22 15:58:09.000000 lxcraft-0.0.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       25 2023-07-22 15:58:09.000000 lxcraft-0.0.1/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)      761 2023-07-22 15:58:17.234667 lxcraft-0.0.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      470 2023-07-22 15:58:09.000000 lxcraft-0.0.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:58:17.234667 lxcraft-0.0.1/lxcraft/
--rw-r--r--   0 runner    (1001) docker     (123)       43 2023-07-22 15:58:09.000000 lxcraft-0.0.1/lxcraft/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-22 15:58:09.000000 lxcraft-0.0.1/lxcraft/__main__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:58:17.234667 lxcraft-0.0.1/lxcraft/debian/
--rw-r--r--   0 runner    (1001) docker     (123)       60 2023-07-22 15:58:09.000000 lxcraft-0.0.1/lxcraft/debian/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1126 2023-07-22 15:58:09.000000 lxcraft-0.0.1/lxcraft/debian/package.py
--rw-r--r--   0 runner    (1001) docker     (123)      707 2023-07-22 15:58:09.000000 lxcraft-0.0.1/lxcraft/plan.py
--rw-r--r--   0 runner    (1001) docker     (123)      160 2023-07-22 15:58:17.000000 lxcraft-0.0.1/lxcraft/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:58:17.234667 lxcraft-0.0.1/lxcraft.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      761 2023-07-22 15:58:17.000000 lxcraft-0.0.1/lxcraft.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      631 2023-07-22 15:58:17.000000 lxcraft-0.0.1/lxcraft.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 15:58:17.000000 lxcraft-0.0.1/lxcraft.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       50 2023-07-22 15:58:17.000000 lxcraft-0.0.1/lxcraft.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-22 15:58:17.000000 lxcraft-0.0.1/lxcraft.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      186 2023-07-22 15:58:09.000000 lxcraft-0.0.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       54 2023-07-22 15:58:09.000000 lxcraft-0.0.1/requirements-dev.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 15:58:09.000000 lxcraft-0.0.1/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      423 2023-07-22 15:58:17.234667 lxcraft-0.0.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      714 2023-07-22 15:58:09.000000 lxcraft-0.0.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:58:17.234667 lxcraft-0.0.1/tests/
--rwxr-xr-x   0 runner    (1001) docker     (123)       36 2023-07-22 15:58:09.000000 lxcraft-0.0.1/tests/clean.sh
--rw-r--r--   0 runner    (1001) docker     (123)      596 2023-07-22 15:58:09.000000 lxcraft-0.0.1/tests/test_debian_package.py
--rw-r--r--   0 runner    (1001) docker     (123)       86 2023-07-22 15:58:09.000000 lxcraft-0.0.1/tests/test_version.py
--rw-r--r--   0 runner    (1001) docker     (123)      191 2023-07-22 15:58:09.000000 lxcraft-0.0.1/tox.ini
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.863034 lxcraft-0.0.2/
+-rw-r--r--   0 runner    (1001) docker     (123)      558 2023-07-23 19:55:47.000000 lxcraft-0.0.2/.cruft.json
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.855034 lxcraft-0.0.2/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.859034 lxcraft-0.0.2/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      404 2023-07-23 19:55:47.000000 lxcraft-0.0.2/.github/workflows/docker-test.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     1080 2023-07-23 19:55:47.000000 lxcraft-0.0.2/.github/workflows/release.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-07-23 19:55:47.000000 lxcraft-0.0.2/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1236 2023-07-23 19:55:47.000000 lxcraft-0.0.2/.pre-commit-config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-07-23 19:55:47.000000 lxcraft-0.0.2/.python-version
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.859034 lxcraft-0.0.2/.vscode/
+-rw-r--r--   0 runner    (1001) docker     (123)      272 2023-07-23 19:55:47.000000 lxcraft-0.0.2/.vscode/launch.json
+-rw-r--r--   0 runner    (1001) docker     (123)      399 2023-07-23 19:55:47.000000 lxcraft-0.0.2/.vscode/settings.json
+-rw-r--r--   0 runner    (1001) docker     (123)      206 2023-07-23 19:55:47.000000 lxcraft-0.0.2/CHANGELOG.md
+-rw-r--r--   0 runner    (1001) docker     (123)      195 2023-07-23 19:55:47.000000 lxcraft-0.0.2/Justfile
+-rw-r--r--   0 runner    (1001) docker     (123)     1056 2023-07-23 19:55:47.000000 lxcraft-0.0.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       25 2023-07-23 19:55:47.000000 lxcraft-0.0.2/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)      945 2023-07-23 19:55:56.863034 lxcraft-0.0.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      654 2023-07-23 19:55:47.000000 lxcraft-0.0.2/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.859034 lxcraft-0.0.2/develop/
+-rw-r--r--   0 runner    (1001) docker     (123)      250 2023-07-23 19:55:47.000000 lxcraft-0.0.2/develop/docker-bash
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-07-23 19:55:47.000000 lxcraft-0.0.2/develop/just-test.sh
+-rw-r--r--   0 runner    (1001) docker     (123)      559 2023-07-23 19:55:47.000000 lxcraft-0.0.2/develop/setup.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.859034 lxcraft-0.0.2/lxcraft/
+-rw-r--r--   0 runner    (1001) docker     (123)       74 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      313 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/base.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.863034 lxcraft-0.0.2/lxcraft/debian/
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/debian/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      896 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/debian/package.py
+-rw-r--r--   0 runner    (1001) docker     (123)      274 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/debian/service.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.863034 lxcraft-0.0.2/lxcraft/path/
+-rw-r--r--   0 runner    (1001) docker     (123)      110 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/path/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      334 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/path/directory.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2170 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/path/filecontent.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1278 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/plan.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.863034 lxcraft-0.0.2/lxcraft/python/
+-rw-r--r--   0 runner    (1001) docker     (123)       65 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/python/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      834 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/python/pip_packages.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1364 2023-07-23 19:55:47.000000 lxcraft-0.0.2/lxcraft/user.py
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-07-23 19:55:56.000000 lxcraft-0.0.2/lxcraft/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.859034 lxcraft-0.0.2/lxcraft.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      945 2023-07-23 19:55:56.000000 lxcraft-0.0.2/lxcraft.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1081 2023-07-23 19:55:56.000000 lxcraft-0.0.2/lxcraft.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:55:56.000000 lxcraft-0.0.2/lxcraft.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       50 2023-07-23 19:55:56.000000 lxcraft-0.0.2/lxcraft.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 19:55:56.000000 lxcraft-0.0.2/lxcraft.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      276 2023-07-23 19:55:47.000000 lxcraft-0.0.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       55 2023-07-23 19:55:47.000000 lxcraft-0.0.2/requirements-dev.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:55:47.000000 lxcraft-0.0.2/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      423 2023-07-23 19:55:56.863034 lxcraft-0.0.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      714 2023-07-23 19:55:47.000000 lxcraft-0.0.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.863034 lxcraft-0.0.2/tests/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:55:56.863034 lxcraft-0.0.2/tests/template/
+-rw-r--r--   0 runner    (1001) docker     (123)      108 2023-07-23 19:55:47.000000 lxcraft-0.0.2/tests/template/main.py
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-07-23 19:55:47.000000 lxcraft-0.0.2/tests/template/test.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      175 2023-07-23 19:55:47.000000 lxcraft-0.0.2/tests/template/wwwkindos.conf
+-rw-r--r--   0 runner    (1001) docker     (123)      320 2023-07-23 19:55:47.000000 lxcraft-0.0.2/tests/test_debian_package.py
+-rw-r--r--   0 runner    (1001) docker     (123)      310 2023-07-23 19:55:47.000000 lxcraft-0.0.2/tests/test_directory.py
+-rw-r--r--   0 runner    (1001) docker     (123)      843 2023-07-23 19:55:47.000000 lxcraft-0.0.2/tests/test_fastapi_uvicorn_gunicorn_supervisor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1077 2023-07-23 19:55:47.000000 lxcraft-0.0.2/tests/test_file_content.py
+-rw-r--r--   0 runner    (1001) docker     (123)      216 2023-07-23 19:55:47.000000 lxcraft-0.0.2/tests/test_user.py
+-rw-r--r--   0 runner    (1001) docker     (123)       86 2023-07-23 19:55:47.000000 lxcraft-0.0.2/tests/test_version.py
```

### Comparing `lxcraft-0.0.1/.cruft.json` & `lxcraft-0.0.2/.cruft.json`

 * *Files identical despite different names*

### Comparing `lxcraft-0.0.1/.github/workflows/release.yaml` & `lxcraft-0.0.2/.github/workflows/release.yaml`

 * *Files 15% similar despite different names*

```diff
@@ -24,7 +24,13 @@
 
       - name: Build a binary wheel and a source tarball
         run: python setup.py sdist bdist_wheel
 
       - name: Publish distribution 📦 to PyPI
         if: startsWith(github.ref, 'refs/tags')
         uses: pypa/gh-action-pypi-publish@release/v1
+
+      - name: Create the GH release
+        if: startsWith(github.ref, 'refs/tags/')  # Only create a release if the ref is a tag
+        uses: softprops/action-gh-release@v1
+        with:
+          body_path: ${{ github.workspace }}/CHANGELOG.md
```

### Comparing `lxcraft-0.0.1/.gitignore` & `lxcraft-0.0.2/.gitignore`

 * *Files identical despite different names*

### Comparing `lxcraft-0.0.1/.pre-commit-config.yaml` & `lxcraft-0.0.2/.pre-commit-config.yaml`

 * *Files 2% similar despite different names*

```diff
@@ -38,13 +38,13 @@
     # Ruff version.
     rev: 'v0.0.265'
     hooks:
     - id: ruff
 
 -   repo: local
     hooks:
-    -   id: run-pytest
-        name: Run tests using pytest
+    -   id: run-just
+        name: Run tests using just
         entry:
-            python -m pytest
+            just test
         language: system
-        pass_filenames: false
+        pass_filenames: false
```

### Comparing `lxcraft-0.0.1/LICENSE` & `lxcraft-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `lxcraft-0.0.1/PKG-INFO` & `lxcraft-0.0.2/PKG-INFO`

 * *Files 27% similar despite different names*

```diff
@@ -1,25 +1,35 @@
 Metadata-Version: 2.1
 Name: lxcraft
-Version: 0.0.1
+Version: 0.0.2
 Summary: Create the skeleton for a python package/project
 Home-page: https://github.com/joaompinto/lxcraft
 Author: João Pinto
 Author-email: lamego.pinto@gmail.com
 License: MIT
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Pythonic Configuration Manager for Linux Systems
 
 [![PyPi](https://img.shields.io/pypi/v/lxcraft.svg?style=flat-square)](https://pypi.python.org/pypi/lxcraft)
 [![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg?style=flat-square)](https://github.com/ambv/black)
 
 
+## How to use
 ```python
 from lxcraft import Plan
 from lxcraft.debian import APTPackages
 
 Plan("ensure nginx is installed", [
-    APTPackages(["nginx"], must_be_installed=True)
+    APTPackages(["nginx"])
 ]).run()
 ```
+
+## How to develop
+
+In order to develop you must use Linux or WSL with docker.
+
+```sh
+develop/docker-bash     # Enter the development docker instance
+just                    # Run the tests
+```
```

### Comparing `lxcraft-0.0.1/lxcraft/debian/package.py` & `lxcraft-0.0.2/lxcraft/debian/package.py`

 * *Files 10% similar despite different names*

```diff
@@ -5,33 +5,27 @@
 
 
 @dataclass
 class APTPackages:
     """List of packages that must be installed"""
 
     package_list: list[str]
-    must_be_installed: bool = True
 
-    def is_installed(selfl, package_name: str):
-        rc, _ = getstatusoutput(f"dpkg -s {package_name}")
-        return rc == 0
-
-    def get_action(self):
+    def get_actions(self):
         package_list = []
         for package in self.package_list:
             if self.is_installed(package):
-                if self.must_be_installed:
-                    continue
-            else:
-                if not self.must_be_installed:
-                    continue
+                continue
             package_list.append(package)
         if not package_list:
-            return None
-        action = "install" if self.must_be_installed else "remove"
-        return partial(package_action, action, " ".join(package_list))
+            return
+        return [partial(self.package_action, " ".join(package_list))]
 
+    def package_action(self, package_list: str):
+        rc = os.system(f"apt install -y {package_list}")
+        if rc != 0:
+            raise Exception(f"Command terminated with non zero exit code {rc}")
 
-def package_action(action: str, package_list: str):
-    rc = os.system(f"apt {action} -y {package_list}")
-    if rc != 0:
-        raise Exception(f"Command terminated with non zero exit code {rc}")
+    @staticmethod
+    def is_installed(package_name: str):
+        rc, _ = getstatusoutput(f"dpkg -s {package_name}")
+        return rc == 0
```

### Comparing `lxcraft-0.0.1/lxcraft.egg-info/PKG-INFO` & `lxcraft-0.0.2/lxcraft.egg-info/PKG-INFO`

 * *Files 27% similar despite different names*

```diff
@@ -1,25 +1,35 @@
 Metadata-Version: 2.1
 Name: lxcraft
-Version: 0.0.1
+Version: 0.0.2
 Summary: Create the skeleton for a python package/project
 Home-page: https://github.com/joaompinto/lxcraft
 Author: João Pinto
 Author-email: lamego.pinto@gmail.com
 License: MIT
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Pythonic Configuration Manager for Linux Systems
 
 [![PyPi](https://img.shields.io/pypi/v/lxcraft.svg?style=flat-square)](https://pypi.python.org/pypi/lxcraft)
 [![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg?style=flat-square)](https://github.com/ambv/black)
 
 
+## How to use
 ```python
 from lxcraft import Plan
 from lxcraft.debian import APTPackages
 
 Plan("ensure nginx is installed", [
-    APTPackages(["nginx"], must_be_installed=True)
+    APTPackages(["nginx"])
 ]).run()
 ```
+
+## How to develop
+
+In order to develop you must use Linux or WSL with docker.
+
+```sh
+develop/docker-bash     # Enter the development docker instance
+just                    # Run the tests
+```
```

### Comparing `lxcraft-0.0.1/setup.py` & `lxcraft-0.0.2/setup.py`

 * *Ordering differences only*

 * *Files 1% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 import io
 from pathlib import Path
+
 from setuptools import setup
 
 SCRIPT_DIR = Path(__file__).parent
 
 
 scm_version_options = {"write_to": "lxcraft/version.py"}
 
 
 def setup_package():
-
     # Get readme
     readme_path = Path(SCRIPT_DIR, "README.md")
     with io.open(readme_path, encoding="utf8") as f:
         readme = f.read()
 
     # Get requiremeents
     with io.open("requirements.txt", encoding="utf8") as f:
```

