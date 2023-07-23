# Comparing `tmp/apixdev-0.2.1.tar.gz` & `tmp/apixdev-0.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "apixdev-0.2.1.tar", last modified: Sun Jul 23 17:06:46 2023, max compression
+gzip compressed data, was "apixdev-0.2.2.tar", last modified: Sun Jul 23 19:07:20 2023, max compression
```

## Comparing `apixdev-0.2.1.tar` & `apixdev-0.2.2.tar`

### file list

```diff
@@ -1,36 +1,36 @@
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 17:06:46.437918 apixdev-0.2.1/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     1074 2023-07-23 16:27:29.000000 apixdev-0.2.1/LICENSE
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      662 2023-07-23 17:06:46.437918 apixdev-0.2.1/PKG-INFO
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      864 2023-07-23 16:50:50.000000 apixdev-0.2.1/README.md
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 17:06:46.433918 apixdev-0.2.1/apixdev/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)       71 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/__init__.py
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 17:06:46.433918 apixdev-0.2.1/apixdev/cli/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)        0 2022-08-11 15:34:34.000000 apixdev-0.2.1/apixdev/cli/__init__.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      630 2023-07-23 16:32:30.000000 apixdev-0.2.1/apixdev/cli/config.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      287 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/cli/images.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      569 2023-07-23 16:32:30.000000 apixdev-0.2.1/apixdev/cli/main.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     2716 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/cli/project.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      598 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/cli/projects.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      760 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/cli/tools.py
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 17:06:46.437918 apixdev-0.2.1/apixdev/core/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)        0 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/core/__init__.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      627 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/core/common.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     1478 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/core/compose.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     3351 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/core/docker.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      649 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/core/images.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     2170 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/core/odoo.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     3919 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/core/project.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      561 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/core/projects.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     1232 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/core/repository.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     5092 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/core/settings.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     2492 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/core/tools.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     2469 2023-07-23 16:27:29.000000 apixdev-0.2.1/apixdev/vars.py
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 17:06:46.433918 apixdev-0.2.1/apixdev.egg-info/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      662 2023-07-23 17:06:46.000000 apixdev-0.2.1/apixdev.egg-info/PKG-INFO
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      668 2023-07-23 17:06:46.000000 apixdev-0.2.1/apixdev.egg-info/SOURCES.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)        1 2023-07-23 17:06:46.000000 apixdev-0.2.1/apixdev.egg-info/dependency_links.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)       46 2023-07-23 17:06:46.000000 apixdev-0.2.1/apixdev.egg-info/entry_points.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      146 2023-07-23 17:06:46.000000 apixdev-0.2.1/apixdev.egg-info/requires.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)        8 2023-07-23 17:06:46.000000 apixdev-0.2.1/apixdev.egg-info/top_level.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)       38 2023-07-23 17:06:46.437918 apixdev-0.2.1/setup.cfg
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     1596 2023-07-23 17:06:30.000000 apixdev-0.2.1/setup.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:07:20.911989 apixdev-0.2.2/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1074 2023-07-23 16:27:29.000000 apixdev-0.2.2/LICENSE
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      662 2023-07-23 19:07:20.911989 apixdev-0.2.2/PKG-INFO
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      864 2023-07-23 16:50:50.000000 apixdev-0.2.2/README.md
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:07:20.907989 apixdev-0.2.2/apixdev/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)       71 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/__init__.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:07:20.907989 apixdev-0.2.2/apixdev/cli/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        0 2022-08-11 15:34:34.000000 apixdev-0.2.2/apixdev/cli/__init__.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      630 2023-07-23 16:32:30.000000 apixdev-0.2.2/apixdev/cli/config.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      287 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/cli/images.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      569 2023-07-23 16:32:30.000000 apixdev-0.2.2/apixdev/cli/main.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2984 2023-07-23 19:06:10.000000 apixdev-0.2.2/apixdev/cli/project.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      598 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/cli/projects.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      760 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/cli/tools.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:07:20.911989 apixdev-0.2.2/apixdev/core/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        0 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/__init__.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      627 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/common.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1478 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/compose.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     3351 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/docker.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      649 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/images.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2170 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/odoo.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     4399 2023-07-23 19:06:10.000000 apixdev-0.2.2/apixdev/core/project.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      561 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/projects.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1232 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/repository.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     5092 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/settings.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2492 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/tools.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2487 2023-07-23 18:37:37.000000 apixdev-0.2.2/apixdev/vars.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:07:20.907989 apixdev-0.2.2/apixdev.egg-info/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      662 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/PKG-INFO
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      668 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/SOURCES.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        1 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/dependency_links.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)       46 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/entry_points.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      146 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/requires.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        8 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/top_level.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)       38 2023-07-23 19:07:20.911989 apixdev-0.2.2/setup.cfg
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1596 2023-07-23 19:05:27.000000 apixdev-0.2.2/setup.py
```

### Comparing `apixdev-0.2.1/LICENSE` & `apixdev-0.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/PKG-INFO` & `apixdev-0.2.2/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: apixdev
-Version: 0.2.1
+Version: 0.2.2
 Summary: ApiX CLI
 Home-page: https://github.com/apikcloud/apix-cli
 Author: Aurelien ROY
 Author-email: roy.aurelien@gmail.com
 License: MIT
 Keywords: docker odoo development
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `apixdev-0.2.1/README.md` & `apixdev-0.2.2/README.md`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/cli/config.py` & `apixdev-0.2.2/apixdev/cli/config.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/cli/main.py` & `apixdev-0.2.2/apixdev/cli/main.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/cli/project.py` & `apixdev-0.2.2/apixdev/cli/project.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,7 +1,9 @@
+import sys
+
 import click
 
 from apixdev.cli.tools import abort_if_false, print_list
 from apixdev.core.odoo import Odoo
 from apixdev.core.project import Project
 
 
@@ -22,22 +24,31 @@
 
     project = Project(name)
 
     if not is_local:
         odoo = Odoo.new()
         database = odoo.get_databases(name, strict=True, limit=1)
 
+        if not database:
+            click.echo(f"No '{name}' database found.")
+            project.delete()
+            sys.exit(1)
+
         urls = [
             ("manifest.yaml", database.manifest_url),
             ("repositories.yaml", database.repositories_url),
             ("docker-compose.yaml", database.compose_url),
         ]
 
         for name, url in urls:
-            project.download(name, url)
+            try:
+                project.download(name, url)
+            except Exception as error:
+                click.echo(error)
+                sys.exit(1)
 
         project.pull_repositories()
         project.merge_requirements()
 
 
 @click.command()
 @click.option(
```

### Comparing `apixdev-0.2.1/apixdev/cli/projects.py` & `apixdev-0.2.2/apixdev/cli/projects.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/cli/tools.py` & `apixdev-0.2.2/apixdev/cli/tools.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/core/common.py` & `apixdev-0.2.2/apixdev/core/common.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/core/compose.py` & `apixdev-0.2.2/apixdev/core/compose.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/core/docker.py` & `apixdev-0.2.2/apixdev/core/docker.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/core/images.py` & `apixdev-0.2.2/apixdev/core/images.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/core/odoo.py` & `apixdev-0.2.2/apixdev/core/odoo.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/core/project.py` & `apixdev-0.2.2/apixdev/core/project.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 import os
 import subprocess
 from shutil import rmtree
 
 import requests
+from requests.exceptions import HTTPError
 
 from apixdev.core.compose import Compose
 from apixdev.core.settings import Settings
 from apixdev.core.tools import (
     filter_requirements,
     get_requirements_from_path,
     list_to_text,
@@ -64,22 +65,36 @@
             self.repositories_file,
             self.manifest_file,
         ]
         return bool(all(map(os.path.exists, files)))
 
     def download(self, filename, url, force=False):
         filepath = os.path.join(self.path, filename)
+        headers = {
+            "X-Api-Token": settings.get_var("apix.token"),
+        }
 
         if force and os.path.exists(filepath):
+            print("remove %s" % filepath)
             os.remove(filepath)
 
-        response = requests.get(url, allow_redirects=False)
+        try:
+            response = requests.get(url, headers=headers, allow_redirects=False)
+            response.raise_for_status()
+        except HTTPError as error:
+            code = error.response.status_code
+            raise Exception(
+                f"Error while trying to download {filename} from {url} (HTTP {code})."
+            )
+
         with open(filepath, "wb") as file:
             file.write(response.content)
 
+        return True
+
     def pull_repositories(self):
         if not self.repositories_file:
             return False
 
         env_file = self.env_file if os.path.exists(self.env_file) else settings.env_file
 
         # gitaggregate(f"-c {self.repositories_file}", _cwd=self.path)
```

### Comparing `apixdev-0.2.1/apixdev/core/projects.py` & `apixdev-0.2.2/apixdev/core/projects.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/core/repository.py` & `apixdev-0.2.2/apixdev/core/repository.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/core/settings.py` & `apixdev-0.2.2/apixdev/core/settings.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/core/tools.py` & `apixdev-0.2.2/apixdev/core/tools.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/apixdev/vars.py` & `apixdev-0.2.2/apixdev/vars.py`

 * *Files 2% similar despite different names*

```diff
@@ -30,14 +30,15 @@
 DEFAULT_PASSWORD = "admin"
 
 MANDATORY_VALUES = [
     "apix.database",
     "apix.url",
     "apix.user",
     "apix.password",
+    "apix.token",
     "local.workdir",
     "local.default_password",
     "git.remote_url",
     "git.remote_login",
     "git.remote_token",
     # "scaffold.odoo-template",
     # "scaffold.docker-template",
```

### Comparing `apixdev-0.2.1/apixdev.egg-info/PKG-INFO` & `apixdev-0.2.2/apixdev.egg-info/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: apixdev
-Version: 0.2.1
+Version: 0.2.2
 Summary: ApiX CLI
 Home-page: https://github.com/apikcloud/apix-cli
 Author: Aurelien ROY
 Author-email: roy.aurelien@gmail.com
 License: MIT
 Keywords: docker odoo development
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `apixdev-0.2.1/apixdev.egg-info/SOURCES.txt` & `apixdev-0.2.2/apixdev.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.1/setup.py` & `apixdev-0.2.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import find_packages, setup
 
 setup(
     name="apixdev",
-    version="0.2.1",
+    version="0.2.2",
     description="ApiX CLI",
     keywords="docker odoo development",
     url="https://github.com/apikcloud/apix-cli",
     author="Aurelien ROY",
     author_email="roy.aurelien@gmail.com",
     license="MIT",
     classifiers=[
```

