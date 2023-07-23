# Comparing `tmp/docker_harbormaster-0.3.1.tar.gz` & `tmp/docker_harbormaster-0.3.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "docker_harbormaster-0.3.1.tar", max compression
+gzip compressed data, was "docker_harbormaster-0.3.2.tar", max compression
```

## Comparing `docker_harbormaster-0.3.1.tar` & `docker_harbormaster-0.3.2.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0    34463 2023-07-22 23:52:55.987168 docker_harbormaster-0.3.1/LICENSE
--rw-r--r--   0        0        0    20206 2023-07-22 23:53:03.523187 docker_harbormaster-0.3.1/README.md
--rw-r--r--   0        0        0        0 2023-07-22 23:52:55.987168 docker_harbormaster-0.3.1/docker_harbormaster/__init__.py
--rwxr-xr-x   0        0        0    28360 2023-07-22 23:52:55.987168 docker_harbormaster-0.3.1/docker_harbormaster/cli.py
--rwxr-xr-x   0        0        0        0 2023-07-22 23:52:55.987168 docker_harbormaster-0.3.1/docker_harbormaster/conftest.py
--rw-r--r--   0        0        0     2777 2023-07-22 23:52:55.987168 docker_harbormaster-0.3.1/docker_harbormaster/utils.py
--rw-r--r--   0        0        0      815 2023-07-22 23:52:55.991168 docker_harbormaster-0.3.1/pyproject.toml
--rw-r--r--   0        0        0    21117 1970-01-01 00:00:00.000000 docker_harbormaster-0.3.1/PKG-INFO
+-rw-r--r--   0        0        0    34463 2023-07-23 20:50:33.755018 docker_harbormaster-0.3.2/LICENSE
+-rw-r--r--   0        0        0    17897 2023-07-23 20:50:49.822507 docker_harbormaster-0.3.2/README.md
+-rw-r--r--   0        0        0        0 2023-07-23 20:50:33.777018 docker_harbormaster-0.3.2/docker_harbormaster/__init__.py
+-rwxr-xr-x   0        0        0    28575 2023-07-23 20:50:33.756852 docker_harbormaster-0.3.2/docker_harbormaster/cli.py
+-rwxr-xr-x   0        0        0        0 2023-07-23 20:50:33.777018 docker_harbormaster-0.3.2/docker_harbormaster/conftest.py
+-rw-r--r--   0        0        0     2777 2023-07-23 20:50:33.756852 docker_harbormaster-0.3.2/docker_harbormaster/utils.py
+-rw-r--r--   0        0        0      815 2023-07-23 20:50:33.757768 docker_harbormaster-0.3.2/pyproject.toml
+-rw-r--r--   0        0        0    18808 1970-01-01 00:00:00.000000 docker_harbormaster-0.3.2/PKG-INFO
```

### Comparing `docker_harbormaster-0.3.1/LICENSE` & `docker_harbormaster-0.3.2/LICENSE`

 * *Files identical despite different names*

### Comparing `docker_harbormaster-0.3.1/README.md` & `docker_harbormaster-0.3.2/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,7 +1,30 @@
+Metadata-Version: 2.1
+Name: docker-harbormaster
+Version: 0.3.2
+Summary: A supervisor for docker-compose apps.
+Home-page: https://gitlab.com/stavros/harbormaster
+License: AGPL-3.0-or-later
+Author: Stavros Korokithakis
+Author-email: hi@stavros.io
+Requires-Python: >=3.7,<4
+Classifier: License :: OSI Approved :: GNU Affero General Public License v3 or later (AGPLv3+)
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Requires-Dist: PyYAML (>=6.0.0)
+Requires-Dist: attrs (>=21.2.0)
+Requires-Dist: click (>=8.1.3)
+Requires-Dist: click-help-colors (>=0.9.1)
+Project-URL: Repository, https://gitlab.com/stavros/harbormaster
+Description-Content-Type: text/markdown
+
 Harbormaster
 ============
 
 [![PyPI](https://img.shields.io/pypi/v/docker_harbormaster)](https://pypi.org/project/docker-harbormaster/)
 
 Harbormaster is a small utility that lets you easily deploy multiple
 Docker-Compose applications on a single host.
@@ -31,14 +54,41 @@
 repositories in its configuration, and restarts the Compose services if they have
 changed. That's it!
 
 It also cleanly stores data for all apps in a single `data/` directory, so you always
 have one directory that holds all the state, which you can easily back up and restore.
 
 
+## How it works
+
+Let's say you have the application you want to run, in a git repository, with
+a `docker-compose.yml` file in the same repo.
+
+Ideally, you'd want a flow that would fetch new commits in that repo, and restart the
+Docker container if there were any changes.
+
+That's all Harbormaster does. Simply tell it where your application lives, in the form
+of a `harbormaster.yml` file:
+
+```yaml
+apps:
+  myapp:
+    url: https://github.com/someuser/somerepo.git
+```
+
+Then run `harbormaster -c harbormaster.yml`, and Harbormaster will clone the repo you
+specified in the config, and run `docker compose up` on it.
+
+It does some other nice things, like give you separate directories for the repos and
+their data, so you can easily make backups of your apps, and that's about it!
+
+If you run Harbormaster again, it will check that repo for changes, and if it finds any,
+it will pull them, stop the container, and start it again with the new changes.
+
+
 ## Installation
 
 You can run Harbormaster directly from Docker, without installing anything. Skip down to
 the [Docker installation](#docker-installation) section.
 
 Installing Harbormaster is simple. You can use `pipx` (recommended):
 
@@ -91,23 +141,14 @@
 
 Alternatively you can use `stavros/harbormaster:webhook` which ships with
 [webhook](https://github.com/adnanh/webhook) to trigger updates. The image comes with
 an example configuration but you should mount a custom one to `/hooks.json` with proper
 [rules](https://github.com/adnanh/webhook/blob/master/docs/Hook-Rules.md) for verifying
 the source.
 
-## High-level architecture overview
-
-At its core, Harbormaster works very simply: It takes a YAML file containing a list of
-repositories, pulls/clones them as necessary, messes with their `docker-compose.yml`
-files in the way you specify, and tells Compose to start, stop, or restart them, as
-needed.
-
-That's all it does.
-
 
 ## Usage
 
 Harbormaster uses a single YAML configuration file that's basically a list of
 repositories containing `docker-compose.yml` files/apps to deploy:
 
 ```yaml
@@ -457,14 +498,27 @@
     url: https://gitlab.com/stavros/harbormaster.git
     compose_config: apps/octoprint/docker-compose.harbormaster.yml
 ```
 
 # Changelog
 
 
+## v0.3.2 (2023-07-23)
+
+### Fixes
+
+* Fix tests. [Stavros Korokithakis]
+
+* Fix the Harbormaster Docker container. [Stavros Korokithakis]
+
+* Fix issue with the Harbormaster Docker image not being able to find the data dir. [Stavros Korokithakis]
+
+* Add docker-cli-compose to the Dockerfile. [Stavros Korokithakis]
+
+
 ## v0.3.1 (2023-07-22)
 
 ### Features
 
 * Add git-crypt to the Docker image. [Stavros Korokithakis]
 
 ### Fixes
@@ -506,194 +560,13 @@
 * Remove the need for passing the data path to the HM container. [Stavros Korokithakis]
 
 * Forward environment variables from the host to the Dockerized HM instance. [Stavros Korokithakis]
 
 
 ## v0.1.20 (2021-11-14)
 
-### Features
-
-* Restart an app if its environment vars change. [Stavros Korokithakis]
-
-* Add image pruning config option. [Stavros Korokithakis]
-
-* Allow Docker-supported installations. [Stavros Korokithakis]
-
 ### Fixes
 
 * Fix wrong volume path when Harbormaster is deployed inside Docker. [Stavros Korokithakis]
 
 
-## v0.1.19 (2021-10-09)
-
-### Features
-
-* Add YAML environment files. [Stavros Korokithakis]
-
-* Add n8n app. [Stavros Korokithakis]
-
-* Add default values to templates. [Stavros Korokithakis]
-
-* Add Octoprint app config. [Stavros Korokithakis]
-
-* Add executable building. [Stavros Korokithakis]
-
-### Fixes
-
-* Don't try to stop an app if its repo dir doesn't exist. [Stavros Korokithakis]
-
-* Fix changelog display. [Stavros Korokithakis]
-
-
-## v0.1.18 (2021-09-19)
-
-### Features
-
-* Add ztncui app. [Stavros Korokithakis]
-
-### Fixes
-
-* Don't pull disabled apps, no good can come of it. [Stavros Korokithakis]
-
-
-## v0.1.17 (2021-09-13)
-
-### Fixes
-
-* Streamline repository updates and improve change detection (fixes #3) [Stavros Korokithakis]
-
-* Do not pull disabled apps. [Stavros Korokithakis]
-
-* Fail gracefully if no configuration is specified. [Stavros Korokithakis]
-
-
-## v0.1.16 (2021-08-12)
-
-### Fixes
-
-* Fix Compose variables not getting rendered in some cases. [Stavros Korokithakis]
-
-
-## v0.1.15 (2021-06-21)
-
-### Features
-
-* Change `compose_filename` to `compose_config` [Stavros Korokithakis]
-
-* Retry git operations on failure. [Ali Piccioni]
-
-* Add bundled apps. [Stavros Korokithakis]
-
-
-## v0.1.14 (2021-05-19)
-
-### Fixes
-
-* Exit with a 1 if any of the apps failed to deploy. [Stavros Korokithakis]
-
-
-## v0.1.13 (2021-05-18)
-
-### Fixes
-
-* Pull images before starting app. [Stavros Korokithakis]
-
-
-## v0.1.12 (2021-05-18)
-
-### Features
-
-* Add the HM_REPO_DIR variable. [Stavros Korokithakis]
-
-### Fixes
-
-* Improve starting/stopping of apps. [Stavros Korokithakis]
-
-
-## v0.1.10 (2021-05-13)
-
-### Features
-
-* Show better error messages. [Stavros Korokithakis]
-
-### Fixes
-
-* Fix erroneous overwriting of replacements. [Stavros Korokithakis]
-
-* Fix error when environment variables are not strings. [Stavros Korokithakis]
-
-* Build containers when starting. [Stavros Korokithakis]
-
-
-## v0.1.9 (2021-05-12)
-
-### Features
-
-* Allow retrieving replacements and env vars from files. [Stavros Korokithakis]
-
-
-## v0.1.8 (2021-05-10)
-
-### Fixes
-
-* Stop containers properly. [Stavros Korokithakis]
-
-
-## v0.1.7 (2021-05-10)
-
-### Features
-
-* Add "enabled" flag. [Stavros Korokithakis]
-
-
-## v0.1.6 (2021-05-10)
-
-### Fixes
-
-* Gracefully stop containers most of the time. [Stavros Korokithakis]
-
-* Reset repository more forcefully when pulling. [Stavros Korokithakis]
-
-* Rename the default config file. [Stavros Korokithakis]
-
-
-## v0.1.5 (2021-05-10)
-
-### Features
-
-* Add replacements feature. [Stavros Korokithakis]
-
-
-## v0.1.4 (2021-05-09)
-
-### Features
-
-* Add environment variables to the config. [Stavros Korokithakis]
-
-
-## v0.1.3 (2021-05-06)
-
-### Features
-
-* Add the "branch" and "compose_filename" config keys. [Stavros Korokithakis]
-
-
-## v0.1.2 (2021-04-26)
-
-### Fixes
-
-* Support Python 3.6 and up. [Stavros Korokithakis]
-
-
-## v0.1.1 (2021-04-25)
-
-### Features
-
-* Add version command-line option. [Stavros Korokithakis]
-
-* Add directories. [Stavros Korokithakis]
-
-### Fixes
-
-* Fetch before trying to check for changes. [Stavros Korokithakis]
-
```

### Comparing `docker_harbormaster-0.3.1/docker_harbormaster/cli.py` & `docker_harbormaster-0.3.2/docker_harbormaster/cli.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 #!/usr/bin/env python3
 import ast
 import hashlib
 import json
 import os
 import re
+import shlex
 import shutil
 import signal
 import subprocess
 import sys
 import tempfile
 import time
 from pathlib import Path
@@ -21,15 +22,14 @@
 
 import attr
 import click
 import yaml
 from click_help_colors import HelpColorsGroup
 
 from .utils import AppPaths
-from .utils import DATA_DIR_NAME
 from .utils import options_to_dict
 from .utils import Paths
 
 
 DEBUG: bool = False
 
 MAX_GIT_NETWORK_ATTEMPTS = 3
@@ -170,17 +170,39 @@
     # Include the environment in our command.
     env = os.environ.copy()
     if environment:
         env.update(environment)
 
     wd = os.getcwd()
     os.chdir(chdir)
-    debug("Command: " + " ".join([str(x) for x in command]))
+    # We concatenate the command here instead of just passing it to Popen, because the
+    # Harbormaster container (the way to deploy HM) uses a symlink inside with the same
+    # name as the host directory (to make the paths inside the container match up with
+    # the host).
+    #
+    # We do this because otherwise relative volume paths (e.g. `.:/code`) don't work,
+    # as it tries to map the current directory inside the container (e.g. `/main`) to
+    # the outside, where it has a different path (e.g. `/home/foo/hm`), so we create
+    # a symlink called `/home/foo/hm` inside the container, with `/main` as a target.
+    #
+    # In order for Compose to see the current directory as the symlink (ie
+    # `/home/foo/hm`), instead of the absolute path (ie `/main`), we need to use a shell
+    # and cd to the symlink before running Compose.
+    #
+    # I haven't found another way to do this, but if you do, feel free to change it.
+    concatenated_command = f"cd {shlex.quote(str(chdir))}; " + " ".join(
+        [shlex.quote(str(c)) for c in command]
+    )
+    debug(f"Command: {concatenated_command}")
     process = subprocess.Popen(
-        command, stdout=subprocess.PIPE, stderr=subprocess.STDOUT, env=env, shell=False
+        concatenated_command,
+        stdout=subprocess.PIPE,
+        stderr=subprocess.STDOUT,
+        env=env,
+        shell=True,
     )
 
     stdout_list: List[bytes] = []
     if process.stdout:
         try:
             for line in process.stdout:
                 stdout_list.append(line)
@@ -354,35 +376,20 @@
 
     def _render_config_vars(self):
         """
         Render Harbormaster variables in the Compose file.
 
         This replaces variables like {{ HM_DATA_DIR }} with their value counterparts.
         """
-        # There's a particularity in how the Docker deployment of Harbormaster (ie
-        # running Harbormaster itself in a container) works: Harbormaster inside the
-        # container tries to tell Compose to mount the apps' volumes in its working
-        # directory, but Compose mounts them on the *host* instead. This is because
-        # Compose doesn't know that the caller is in a container, it just sees someone
-        # ask it to mount the `data` volume into `/main/data/someapp`.
-        # We work around that with a hack here by looking for an environment variable
-        # with the path to mount on the host.
-        data_env_var = os.environ.get("HARBORMASTER_HOST_DATA")
-        data_dir = (
-            (Path(data_env_var) / DATA_DIR_NAME / self.id)
-            if data_env_var
-            else self.paths.data_dir
-        )
-
         for cfn in self.compose_config:
             with (self.paths.repo_dir / cfn).open("r+") as cfile:
                 contents = cfile.read()
 
                 replacements = {
-                    "DATA_DIR": str(data_dir),
+                    "DATA_DIR": str(self.paths.data_dir),
                     "CACHE_DIR": str(self.paths.cache_dir),
                     "REPO_DIR": str(self.paths.repo_dir),
                 }
                 replacements.update(self.replacements)
                 contents = _render_template(contents, replacements)
 
                 cfile.truncate(0)
@@ -727,15 +734,14 @@
     "--working-dir",
     default=".",
     type=click.Path(
         exists=True,
         file_okay=False,
         readable=True,
         writable=True,
-        resolve_path=True,
         path_type=Path,
     ),
     help="The root directory to work in.",
 )
 @click.option(
     "-f",
     "--force-restart",
```

### Comparing `docker_harbormaster-0.3.1/docker_harbormaster/utils.py` & `docker_harbormaster-0.3.2/docker_harbormaster/utils.py`

 * *Files identical despite different names*

### Comparing `docker_harbormaster-0.3.1/pyproject.toml` & `docker_harbormaster-0.3.2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "docker-harbormaster"
-version = "0.3.1"
+version = "0.3.2"
 description = "A supervisor for docker-compose apps."
 authors = ["Stavros Korokithakis <hi@stavros.io>"]
 repository = "https://gitlab.com/stavros/harbormaster"
 homepage = "https://gitlab.com/stavros/harbormaster"
 license = "AGPL-3.0-or-later"
 readme = "README.md"
```

