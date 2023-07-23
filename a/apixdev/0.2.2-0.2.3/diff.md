# Comparing `tmp/apixdev-0.2.2.tar.gz` & `tmp/apixdev-0.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "apixdev-0.2.2.tar", last modified: Sun Jul 23 19:07:20 2023, max compression
+gzip compressed data, was "apixdev-0.2.3.tar", last modified: Sun Jul 23 19:29:17 2023, max compression
```

## Comparing `apixdev-0.2.2.tar` & `apixdev-0.2.3.tar`

### file list

```diff
@@ -1,36 +1,36 @@
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:07:20.911989 apixdev-0.2.2/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     1074 2023-07-23 16:27:29.000000 apixdev-0.2.2/LICENSE
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      662 2023-07-23 19:07:20.911989 apixdev-0.2.2/PKG-INFO
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      864 2023-07-23 16:50:50.000000 apixdev-0.2.2/README.md
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:07:20.907989 apixdev-0.2.2/apixdev/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)       71 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/__init__.py
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:07:20.907989 apixdev-0.2.2/apixdev/cli/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)        0 2022-08-11 15:34:34.000000 apixdev-0.2.2/apixdev/cli/__init__.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      630 2023-07-23 16:32:30.000000 apixdev-0.2.2/apixdev/cli/config.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      287 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/cli/images.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      569 2023-07-23 16:32:30.000000 apixdev-0.2.2/apixdev/cli/main.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     2984 2023-07-23 19:06:10.000000 apixdev-0.2.2/apixdev/cli/project.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      598 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/cli/projects.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      760 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/cli/tools.py
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:07:20.911989 apixdev-0.2.2/apixdev/core/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)        0 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/__init__.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      627 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/common.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     1478 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/compose.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     3351 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/docker.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      649 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/images.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     2170 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/odoo.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     4399 2023-07-23 19:06:10.000000 apixdev-0.2.2/apixdev/core/project.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      561 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/projects.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     1232 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/repository.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     5092 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/settings.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     2492 2023-07-23 16:27:29.000000 apixdev-0.2.2/apixdev/core/tools.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     2487 2023-07-23 18:37:37.000000 apixdev-0.2.2/apixdev/vars.py
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:07:20.907989 apixdev-0.2.2/apixdev.egg-info/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      662 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/PKG-INFO
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      668 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/SOURCES.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)        1 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/dependency_links.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)       46 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/entry_points.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      146 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/requires.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)        8 2023-07-23 19:07:20.000000 apixdev-0.2.2/apixdev.egg-info/top_level.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)       38 2023-07-23 19:07:20.911989 apixdev-0.2.2/setup.cfg
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     1596 2023-07-23 19:05:27.000000 apixdev-0.2.2/setup.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:29:17.061757 apixdev-0.2.3/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1074 2023-07-23 16:27:29.000000 apixdev-0.2.3/LICENSE
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      662 2023-07-23 19:29:17.061757 apixdev-0.2.3/PKG-INFO
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      864 2023-07-23 16:50:50.000000 apixdev-0.2.3/README.md
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:29:17.057757 apixdev-0.2.3/apixdev/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)       71 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/__init__.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:29:17.057757 apixdev-0.2.3/apixdev/cli/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        0 2022-08-11 15:34:34.000000 apixdev-0.2.3/apixdev/cli/__init__.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      630 2023-07-23 16:32:30.000000 apixdev-0.2.3/apixdev/cli/config.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      287 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/cli/images.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      569 2023-07-23 16:32:30.000000 apixdev-0.2.3/apixdev/cli/main.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2984 2023-07-23 19:06:10.000000 apixdev-0.2.3/apixdev/cli/project.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      598 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/cli/projects.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      760 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/cli/tools.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:29:17.061757 apixdev-0.2.3/apixdev/core/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        0 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/core/__init__.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      627 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/core/common.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1478 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/core/compose.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     3351 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/core/docker.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      649 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/core/images.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2170 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/core/odoo.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     4399 2023-07-23 19:06:10.000000 apixdev-0.2.3/apixdev/core/project.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      561 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/core/projects.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1232 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/core/repository.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     5092 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/core/settings.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2492 2023-07-23 16:27:29.000000 apixdev-0.2.3/apixdev/core/tools.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2206 2023-07-23 19:27:37.000000 apixdev-0.2.3/apixdev/vars.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 19:29:17.057757 apixdev-0.2.3/apixdev.egg-info/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      662 2023-07-23 19:29:17.000000 apixdev-0.2.3/apixdev.egg-info/PKG-INFO
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      668 2023-07-23 19:29:17.000000 apixdev-0.2.3/apixdev.egg-info/SOURCES.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        1 2023-07-23 19:29:17.000000 apixdev-0.2.3/apixdev.egg-info/dependency_links.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)       46 2023-07-23 19:29:17.000000 apixdev-0.2.3/apixdev.egg-info/entry_points.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      146 2023-07-23 19:29:17.000000 apixdev-0.2.3/apixdev.egg-info/requires.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        8 2023-07-23 19:29:17.000000 apixdev-0.2.3/apixdev.egg-info/top_level.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)       38 2023-07-23 19:29:17.061757 apixdev-0.2.3/setup.cfg
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1596 2023-07-23 19:28:47.000000 apixdev-0.2.3/setup.py
```

### Comparing `apixdev-0.2.2/LICENSE` & `apixdev-0.2.3/LICENSE`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/PKG-INFO` & `apixdev-0.2.3/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: apixdev
-Version: 0.2.2
+Version: 0.2.3
 Summary: ApiX CLI
 Home-page: https://github.com/apikcloud/apix-cli
 Author: Aurelien ROY
 Author-email: roy.aurelien@gmail.com
 License: MIT
 Keywords: docker odoo development
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `apixdev-0.2.2/README.md` & `apixdev-0.2.3/README.md`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/cli/config.py` & `apixdev-0.2.3/apixdev/cli/config.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/cli/main.py` & `apixdev-0.2.3/apixdev/cli/main.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/cli/project.py` & `apixdev-0.2.3/apixdev/cli/project.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/cli/projects.py` & `apixdev-0.2.3/apixdev/cli/projects.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/cli/tools.py` & `apixdev-0.2.3/apixdev/cli/tools.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/core/common.py` & `apixdev-0.2.3/apixdev/core/common.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/core/compose.py` & `apixdev-0.2.3/apixdev/core/compose.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/core/docker.py` & `apixdev-0.2.3/apixdev/core/docker.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/core/images.py` & `apixdev-0.2.3/apixdev/core/images.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/core/odoo.py` & `apixdev-0.2.3/apixdev/core/odoo.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/core/project.py` & `apixdev-0.2.3/apixdev/core/project.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/core/projects.py` & `apixdev-0.2.3/apixdev/core/projects.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/core/repository.py` & `apixdev-0.2.3/apixdev/core/repository.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/core/settings.py` & `apixdev-0.2.3/apixdev/core/settings.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/core/tools.py` & `apixdev-0.2.3/apixdev/core/tools.py`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/apixdev/vars.py` & `apixdev-0.2.3/apixdev/vars.py`

 * *Files 7% similar despite different names*

```diff
@@ -36,34 +36,25 @@
     "apix.password",
     "apix.token",
     "local.workdir",
     "local.default_password",
     "git.remote_url",
     "git.remote_login",
     "git.remote_token",
-    # "scaffold.odoo-template",
-    # "scaffold.docker-template",
     "docker.repository",
 ]
 IGNORED_VALUES = ["password"]
 BACKUP_URL = "{}/web/database/backup"
 RESTORE_URL = "{}/web/database/restore"
 LOCAL_URL = "http://localhost:8069"
-ODOORPC_OPTIONS = ["port"]
-
-COMPOSE_TEMPLATE_FILE = "docker-compose.yaml"
+ODOORPC_OPTIONS = [
+    "port",
+    "protocol",
+]
 
-COMPOSE_TEMPLATE_VALS = {
-    "services": {
-        "odoo": {
-            "image": "apik/odoo-saas:15.0-enterprise",
-            "environment": {"CUSTOM_REQUIREMENTS": []},
-        }
-    }
-}
 
 COMMANDS = {
     "start": {
         "args": ["up", "-d"],
         "cmd": docker_compose,
     },
     "stop": {
```

### Comparing `apixdev-0.2.2/apixdev.egg-info/PKG-INFO` & `apixdev-0.2.3/apixdev.egg-info/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: apixdev
-Version: 0.2.2
+Version: 0.2.3
 Summary: ApiX CLI
 Home-page: https://github.com/apikcloud/apix-cli
 Author: Aurelien ROY
 Author-email: roy.aurelien@gmail.com
 License: MIT
 Keywords: docker odoo development
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `apixdev-0.2.2/apixdev.egg-info/SOURCES.txt` & `apixdev-0.2.3/apixdev.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `apixdev-0.2.2/setup.py` & `apixdev-0.2.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import find_packages, setup
 
 setup(
     name="apixdev",
-    version="0.2.2",
+    version="0.2.3",
     description="ApiX CLI",
     keywords="docker odoo development",
     url="https://github.com/apikcloud/apix-cli",
     author="Aurelien ROY",
     author_email="roy.aurelien@gmail.com",
     license="MIT",
     classifiers=[
```

