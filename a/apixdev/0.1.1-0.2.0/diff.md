# Comparing `tmp/apixdev-0.1.1.tar.gz` & `tmp/apixdev-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "apixdev-0.1.1.tar", last modified: Thu Aug 11 15:44:27 2022, max compression
+gzip compressed data, was "apixdev-0.2.0.tar", last modified: Sun Jul 23 16:51:45 2023, max compression
```

## Comparing `apixdev-0.1.1.tar` & `apixdev-0.2.0.tar`

### file list

```diff
@@ -1,30 +1,36 @@
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2022-08-11 15:44:27.910340 apixdev-0.1.1/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     1073 2022-08-10 07:51:57.000000 apixdev-0.1.1/LICENSE
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      236 2022-08-11 15:44:27.910340 apixdev-0.1.1/PKG-INFO
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      433 2022-08-11 15:41:10.000000 apixdev-0.1.1/README.md
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2022-08-11 15:44:27.910340 apixdev-0.1.1/apixdev/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)       71 2022-08-11 15:18:54.000000 apixdev-0.1.1/apixdev/__init__.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)    10357 2022-08-02 21:20:26.000000 apixdev-0.1.1/apixdev/__old.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)    10387 2022-08-09 22:23:13.000000 apixdev-0.1.1/apixdev/apix.py
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2022-08-11 15:44:27.910340 apixdev-0.1.1/apixdev/cli/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)        0 2022-08-11 15:34:34.000000 apixdev-0.1.1/apixdev/cli/__init__.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)       78 2022-08-03 21:04:48.000000 apixdev-0.1.1/apixdev/cli/common.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      633 2022-08-11 15:30:07.000000 apixdev-0.1.1/apixdev/cli/config.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      800 2022-08-11 15:19:55.000000 apixdev-0.1.1/apixdev/cli/main.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     3692 2022-08-11 15:20:06.000000 apixdev-0.1.1/apixdev/cli/project.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      653 2022-08-11 15:36:13.000000 apixdev-0.1.1/apixdev/cli/projects.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      493 2022-08-11 15:24:27.000000 apixdev-0.1.1/apixdev/cli/scaffold.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     1303 2022-08-04 10:33:47.000000 apixdev-0.1.1/apixdev/cli/tools.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     6461 2022-08-04 09:16:09.000000 apixdev-0.1.1/apixdev/common.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      940 2022-08-04 10:35:37.000000 apixdev-0.1.1/apixdev/compose.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     2534 2022-08-09 22:21:50.000000 apixdev-0.1.1/apixdev/config.py
--rw-rw-r--   0 aroy      (1000) aroy      (1000)     1270 2022-08-04 11:58:25.000000 apixdev-0.1.1/apixdev/repository.py
-drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2022-08-11 15:44:27.910340 apixdev-0.1.1/apixdev.egg-info/
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      236 2022-08-11 15:44:27.000000 apixdev-0.1.1/apixdev.egg-info/PKG-INFO
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      524 2022-08-11 15:44:27.000000 apixdev-0.1.1/apixdev.egg-info/SOURCES.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)        1 2022-08-11 15:44:27.000000 apixdev-0.1.1/apixdev.egg-info/dependency_links.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)       46 2022-08-11 15:44:27.000000 apixdev-0.1.1/apixdev.egg-info/entry_points.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)       73 2022-08-11 15:44:27.000000 apixdev-0.1.1/apixdev.egg-info/requires.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)        8 2022-08-11 15:44:27.000000 apixdev-0.1.1/apixdev.egg-info/top_level.txt
--rw-rw-r--   0 aroy      (1000) aroy      (1000)       38 2022-08-11 15:44:27.910340 apixdev-0.1.1/setup.cfg
--rw-rw-r--   0 aroy      (1000) aroy      (1000)      661 2022-08-11 15:44:01.000000 apixdev-0.1.1/setup.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 16:51:45.860455 apixdev-0.2.0/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1074 2023-07-23 16:27:29.000000 apixdev-0.2.0/LICENSE
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      669 2023-07-23 16:51:45.860455 apixdev-0.2.0/PKG-INFO
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      864 2023-07-23 16:50:50.000000 apixdev-0.2.0/README.md
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 16:51:45.860455 apixdev-0.2.0/apixdev/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)       71 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/__init__.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 16:51:45.860455 apixdev-0.2.0/apixdev/cli/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        0 2022-08-11 15:34:34.000000 apixdev-0.2.0/apixdev/cli/__init__.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      630 2023-07-23 16:32:30.000000 apixdev-0.2.0/apixdev/cli/config.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      287 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/cli/images.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      569 2023-07-23 16:32:30.000000 apixdev-0.2.0/apixdev/cli/main.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2716 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/cli/project.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      598 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/cli/projects.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      760 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/cli/tools.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 16:51:45.860455 apixdev-0.2.0/apixdev/core/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        0 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/core/__init__.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      627 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/core/common.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1478 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/core/compose.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     3351 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/core/docker.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      649 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/core/images.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2170 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/core/odoo.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     3919 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/core/project.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      561 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/core/projects.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1232 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/core/repository.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     5092 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/core/settings.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2492 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/core/tools.py
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     2469 2023-07-23 16:27:29.000000 apixdev-0.2.0/apixdev/vars.py
+drwxrwxr-x   0 aroy      (1000) aroy      (1000)        0 2023-07-23 16:51:45.860455 apixdev-0.2.0/apixdev.egg-info/
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      669 2023-07-23 16:51:45.000000 apixdev-0.2.0/apixdev.egg-info/PKG-INFO
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      668 2023-07-23 16:51:45.000000 apixdev-0.2.0/apixdev.egg-info/SOURCES.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        1 2023-07-23 16:51:45.000000 apixdev-0.2.0/apixdev.egg-info/dependency_links.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)       46 2023-07-23 16:51:45.000000 apixdev-0.2.0/apixdev.egg-info/entry_points.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)      146 2023-07-23 16:51:45.000000 apixdev-0.2.0/apixdev.egg-info/requires.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)        8 2023-07-23 16:51:45.000000 apixdev-0.2.0/apixdev.egg-info/top_level.txt
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)       38 2023-07-23 16:51:45.860455 apixdev-0.2.0/setup.cfg
+-rw-rw-r--   0 aroy      (1000) aroy      (1000)     1603 2023-07-23 16:27:29.000000 apixdev-0.2.0/setup.py
```

### Comparing `apixdev-0.1.1/LICENSE` & `apixdev-0.2.0/LICENSE`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -12,8 +12,8 @@
 
 THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
 IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
 FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
 AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
-SOFTWARE.
+SOFTWARE.
```

### Comparing `apixdev-0.1.1/apixdev/cli/config.py` & `apixdev-0.2.0/apixdev/cli/config.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,40 +1,38 @@
 import click
-import getpass
 
-from apixdev.apix import apix
-from apixdev.cli import tools
+from apixdev.cli.tools import print_dict
+from apixdev.core.settings import Settings
 
+settings = Settings()
 
 
 @click.group()
 def config():
     """View and edit configuration"""
-    pass
 
 
 @click.command()
 def view():
     """Resume configuration"""
-    
-    vals = apix.config.get_vars()
-    tools.print_dict(vals, False)
+
+    vals = settings.get_vars()
+    print_dict(vals, False)
 
 
 @click.command()
-@click.argument('key')
-@click.argument('value')
+@click.argument("key")
+@click.argument("value")
 def set(key, value):
     """Set a value"""
-    apix.config.set_vars({key: value})    
+    settings.set_vars({key: value})
 
 
 @click.command()
 def clear():
     """Clear all parameters"""
     raise NotImplementedError()
-    
 
 
 config.add_command(view)
 config.add_command(clear)
 config.add_command(set)
```

### Comparing `apixdev-0.1.1/apixdev/cli/projects.py` & `apixdev-0.2.0/apixdev/cli/projects.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,34 +1,34 @@
 import click
-import getpass
-
-from apixdev.apix import apix
-from apixdev.cli.common import abort_if_false
-import apixdev.cli.tools as tools
 
+from apixdev.cli.tools import abort_if_false, print_list
+from apixdev.core.projects import Projects
 
 
 @click.group()
 def projects():
     """Manage projects"""
-    pass
+
 
 @click.command()
-def ps():
+def ls():
     """List local projects"""
-    
-    projects = apix.get_local_projects()
-    tools.print_list(projects)
 
+    projects = Projects.from_path()
+    print_list(projects)
 
 
 @click.command()
-@click.option('--yes', is_flag=True, callback=abort_if_false,
-              expose_value=False,
-              prompt='Are you sure you want to stop all projects?')
+@click.option(
+    "--yes",
+    is_flag=True,
+    callback=abort_if_false,
+    expose_value=False,
+    prompt="Are you sure you want to stop all projects?",
+)
 def stop():
     """Stop all projects"""
     raise NotImplementedError()
 
 
-projects.add_command(ps)
+projects.add_command(ls)
 projects.add_command(stop)
```

### Comparing `apixdev-0.1.1/apixdev/repository.py` & `apixdev-0.2.0/apixdev/core/repository.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,51 +1,45 @@
 import logging
 import os
-from git import Repo, InvalidGitRepositoryError, GitCommandError
 
-_logger = logging.getLogger(__name__)
-
-REQUIRED_VALUES = ['url', 'branch', 'path']
+from git import GitCommandError, Repo
 
+_logger = logging.getLogger(__name__)
 
-class GitRepository():
+REQUIRED_VALUES = ["url", "branch", "path"]
 
 
+class GitRepository:
     def __init__(self, name, **kwargs):
         self.name = name
 
-        for k,v in kwargs.items():
+        for k, v in kwargs.items():
             self.__dict__[k] = v
 
-
     @property
     def _path(self):
         return os.path.join(self.path, self.name)
 
-
     def check(self):
         return all([self.__dict__.get(k, False) for k in REQUIRED_VALUES])
 
-
     def exists(self):
         return os.path.exists(self._path)
 
-
     def clone(self):
         # Repository doesn't exists locally, clone
         if not self.exists():
             if not self.check():
-                raise ValueError('Missing parameters.')
-            
-            self._repo = Repo.clone_from(self.url, self._path, branch=self.branch, progress=None, env=None)
+                raise ValueError("Missing parameters.")
+
+            self._repo = Repo.clone_from(
+                self.url, self._path, branch=self.branch, progress=None, env=None
+            )
         else:
             try:
                 _logger.info("Reset end pull repository")
                 self._repo = Repo(self._path)
-                self._repo.git.reset('--hard')
+                self._repo.git.reset("--hard")
                 self._repo.remotes.origin.pull()
             except GitCommandError as err:
                 _logger.error(err)
-                raise ValueError(err)            
-
-
-         
+                raise ValueError(err)
```

### Comparing `apixdev-0.1.1/apixdev.egg-info/SOURCES.txt` & `apixdev-0.2.0/apixdev.egg-info/SOURCES.txt`

 * *Files 11% similar despite different names*

```diff
@@ -1,24 +1,29 @@
 LICENSE
 README.md
 setup.py
 apixdev/__init__.py
-apixdev/__old.py
-apixdev/apix.py
-apixdev/common.py
-apixdev/compose.py
-apixdev/config.py
-apixdev/repository.py
+apixdev/vars.py
 apixdev.egg-info/PKG-INFO
 apixdev.egg-info/SOURCES.txt
 apixdev.egg-info/dependency_links.txt
 apixdev.egg-info/entry_points.txt
 apixdev.egg-info/requires.txt
 apixdev.egg-info/top_level.txt
 apixdev/cli/__init__.py
-apixdev/cli/common.py
 apixdev/cli/config.py
+apixdev/cli/images.py
 apixdev/cli/main.py
 apixdev/cli/project.py
 apixdev/cli/projects.py
-apixdev/cli/scaffold.py
-apixdev/cli/tools.py
+apixdev/cli/tools.py
+apixdev/core/__init__.py
+apixdev/core/common.py
+apixdev/core/compose.py
+apixdev/core/docker.py
+apixdev/core/images.py
+apixdev/core/odoo.py
+apixdev/core/project.py
+apixdev/core/projects.py
+apixdev/core/repository.py
+apixdev/core/settings.py
+apixdev/core/tools.py
```

