# Comparing `tmp/docker_harbormaster-0.3.0.tar.gz` & `tmp/docker_harbormaster-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "docker_harbormaster-0.3.0.tar", max compression
+gzip compressed data, was "docker_harbormaster-0.3.1.tar", max compression
```

## Comparing `docker_harbormaster-0.3.0.tar` & `docker_harbormaster-0.3.1.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0    34463 2023-03-01 21:51:16.285730 docker_harbormaster-0.3.0/LICENSE
--rw-r--r--   0        0        0    16724 2023-03-01 21:51:37.715400 docker_harbormaster-0.3.0/README.md
--rw-r--r--   0        0        0        0 2023-03-01 21:51:16.285730 docker_harbormaster-0.3.0/docker_harbormaster/__init__.py
--rwxr-xr-x   0        0        0    27109 2023-03-01 21:51:16.285730 docker_harbormaster-0.3.0/docker_harbormaster/cli.py
--rwxr-xr-x   0        0        0        0 2023-03-01 21:51:16.285730 docker_harbormaster-0.3.0/docker_harbormaster/conftest.py
--rw-r--r--   0        0        0     2777 2023-03-01 21:51:16.285730 docker_harbormaster-0.3.0/docker_harbormaster/utils.py
--rw-r--r--   0        0        0      843 2023-03-01 21:51:16.286729 docker_harbormaster-0.3.0/pyproject.toml
--rw-r--r--   0        0        0    17676 1970-01-01 00:00:00.000000 docker_harbormaster-0.3.0/PKG-INFO
+-rw-r--r--   0        0        0    34463 2023-07-22 23:52:55.987168 docker_harbormaster-0.3.1/LICENSE
+-rw-r--r--   0        0        0    20206 2023-07-22 23:53:03.523187 docker_harbormaster-0.3.1/README.md
+-rw-r--r--   0        0        0        0 2023-07-22 23:52:55.987168 docker_harbormaster-0.3.1/docker_harbormaster/__init__.py
+-rwxr-xr-x   0        0        0    28360 2023-07-22 23:52:55.987168 docker_harbormaster-0.3.1/docker_harbormaster/cli.py
+-rwxr-xr-x   0        0        0        0 2023-07-22 23:52:55.987168 docker_harbormaster-0.3.1/docker_harbormaster/conftest.py
+-rw-r--r--   0        0        0     2777 2023-07-22 23:52:55.987168 docker_harbormaster-0.3.1/docker_harbormaster/utils.py
+-rw-r--r--   0        0        0      815 2023-07-22 23:52:55.991168 docker_harbormaster-0.3.1/pyproject.toml
+-rw-r--r--   0        0        0    21117 1970-01-01 00:00:00.000000 docker_harbormaster-0.3.1/PKG-INFO
```

### Comparing `docker_harbormaster-0.3.0/LICENSE` & `docker_harbormaster-0.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `docker_harbormaster-0.3.0/docker_harbormaster/cli.py` & `docker_harbormaster-0.3.1/docker_harbormaster/cli.py`

 * *Files 10% similar despite different names*

```diff
@@ -129,15 +129,15 @@
     return output
 
 
 def _kill_orphan_containers(repo_id: str):
     """
     Kill all Docker containers for an app.
 
-    Instead of issuing a `docker-compose down`, this method looks for all
+    Instead of issuing a `docker compose down`, this method looks for all
     running containers that start with "{repo_id}_" (that's why it accepts
     a string instead of an App instance).
 
     That's because the configuration file might be missing, and we might
     not know what the compose file's name is.
     """
     stdout = _run_command_full(
@@ -200,14 +200,32 @@
 def _run_command(
     command: List[Union[Path, str]], chdir: Path, environment: Dict[str, str] = None
 ) -> int:
     """Run a command and return its exit code."""
     return _run_command_full(command, chdir, environment=environment)[0]
 
 
+def _postproc_command_assuming_exitcode0(status, stdout, errmsg: str) -> int:
+    """run_command postprocess to throw an exception of 'errmsg' and 'outout' if status != 0"""
+    if status != 0:
+        raise Exception(f"{errmsg}:\n{stdout.decode()}")
+
+    return status
+
+
+def _run_command_assuming_exitcode_0(
+    command: List[Union[Path, str]],
+    chdir: Path,
+    errmsg: str,
+    environment: Dict[str, str] = None,
+) -> int:
+    status, stdout = _run_command_full(command, chdir, environment=environment)
+    return _postproc_command_assuming_exitcode0(status, stdout, errmsg)
+
+
 class App:
     def __init__(
         self,
         id: str,
         configuration: Dict[str, Any],
         paths: AppPaths,
         cache=Dict[str, str],
@@ -252,40 +270,70 @@
         self.replacements.update(
             {
                 key: str(value)
                 for key, value in configuration.get("replacements", {}).items()
             }
         )
 
+        self.configuration_hash = hashlib.sha1(
+            yaml.dump(configuration).encode("utf-8")
+        ).hexdigest()
+
     def check_parameter_changes(self) -> bool:
         """
         Check if the environment/replacements have changed since the last run.
 
         We do this by hashing the environment/replacements dictionaries and comparing
         those hashes to the hashes in the cache file. If anything goes wrong, we do the
         safe thing and return `True`.
 
         We also update `self.cache` with the new values, for later writing.
         """
         env_hash = _hash_dict(self.environment)
         replacements_hash = _hash_dict(self.replacements)
+        configuration_hash = self.configuration_hash
 
         old_env_hash = self.cache.get("environment_hash", "")
         old_replacements_hash = self.cache.get("replacements_hash", "")
+        old_configuration_hash = self.cache.get("configuration_hash", "")
 
         debug(f"Old env hash: {old_env_hash}\nNew env hash: {env_hash}")
         debug(
             f"Old replacements hash: {old_replacements_hash}"
             f"\nNew replacements hash: {replacements_hash}"
         )
+        debug(
+            f"Old config hash: {old_configuration_hash}\nNew config hash: {configuration_hash}"
+        )
 
         self.cache["environment_hash"] = env_hash
         self.cache["replacements_hash"] = replacements_hash
+        self.cache["configuration_hash"] = configuration_hash
+
+        return (
+            env_hash != old_env_hash
+            or replacements_hash != old_replacements_hash
+            or configuration_hash != old_configuration_hash
+        )
 
-        return env_hash != old_env_hash or replacements_hash != old_replacements_hash
+    def ev_run_command_full(
+        self,
+        command: List[Union[str, Path]],
+        chdir: Path,
+        print_output: bool = False,
+    ) -> Tuple[int, bytes]:
+        return _run_command_full(
+            command, chdir, environment=self.environment, print_output=print_output
+        )
+
+    def ev_run_command_assuming_exitcode_0(
+        self, command: List[Union[Path, str]], chdir: Path, errmsg: str
+    ) -> int:
+        status, stdout = self.ev_run_command_full(command, chdir)
+        return _postproc_command_assuming_exitcode0(status, stdout, errmsg)
 
     @property
     def compose_config_command(self) -> List[str]:
         """
         Return a tuple with the command for the filenames of all the Compose files.
 
         The Compose command line accepts any number of YAML config files,
@@ -352,18 +400,19 @@
                 self.paths.repo_dir,
             )
             == 0
         )
 
     def is_running(self) -> bool:
         """Check if the app is running."""
-        stdout = _run_command_full(
+        stdout = self.ev_run_command_full(
             [
                 "/usr/bin/env",
-                "docker-compose",
+                "docker",
+                "compose",
                 *self.compose_config_command,
                 "ps",
                 "--services",
                 "--filter",
                 "status=running",
             ],
             self.paths.repo_dir,
@@ -374,95 +423,84 @@
         else:
             debug(f"{self.id} is NOT running.")
         # If `docker ps` returned nothing, nothing is running.
         return bool(stdout)
 
     def start(self, detach=True):
         """Start the Docker containers for this app."""
-        status, stdout = _run_command_full(
+        status = self.ev_run_command_assuming_exitcode_0(
             [
                 "/usr/bin/env",
-                "docker-compose",
+                "docker",
+                "compose",
                 *self.compose_config_command,
                 "pull",
             ],
             self.paths.repo_dir,
-            environment=self.environment,
+            "Could not pull the Docker image",
         )
 
-        if status != 0:
-            raise Exception(
-                f"Could not pull the docker-compose image:\n{stdout.decode()}"
-            )
-
         command = [
             "/usr/bin/env",
-            "docker-compose",
+            "docker",
+            "compose",
             *self.compose_config_command,
             "up",
             "--remove-orphans",
             "--build",
         ]
         if detach:
             command.append("--detach")
 
-        status, stdout = _run_command_full(
+        status, stdout = self.ev_run_command_full(
             command,
             self.paths.repo_dir,
-            environment=self.environment,
             print_output=not detach,
         )
-
-        if status != 0:
-            raise Exception(
-                f"Could not start the docker-compose container:\n{stdout.decode()}"
-            )
+        _postproc_command_assuming_exitcode0(
+            status, stdout, "Could not start the Docker container"
+        )
 
     def stop(self):
         if not self.is_running():
             # `docker ps` returned nothing, ie nothing is running.
             return
 
-        if (
-            _run_command(
-                [
-                    "/usr/bin/env",
-                    "docker-compose",
-                    *self.compose_config_command,
-                    "down",
-                    "--remove-orphans",
-                ],
-                self.paths.repo_dir,
-            )
-            != 0
-        ):
-            raise Exception("Could not stop the docker-compose container.")
+        self.ev_run_command_assuming_exitcode_0(
+            [
+                "/usr/bin/env",
+                "docker",
+                "compose",
+                *self.compose_config_command,
+                "down",
+                "--remove-orphans",
+            ],
+            self.paths.repo_dir,
+            "Could not stop the Docker container.",
+        )
 
     def clone(self) -> bool:
         """
         Clone a repository.
 
         Returns whether an update was done.
         """
-        if (
-            _run_command(
-                [
-                    "/usr/bin/env",
-                    "git",
-                    "clone",
-                    "-b",
-                    self.branch,
-                    self.url,
-                    self.paths.repo_dir,
-                ],
-                self.paths.workdir,
-            )
-            != 0
-        ):
-            raise Exception("Could not clone repository.")
+        _run_command_assuming_exitcode_0(
+            [
+                "/usr/bin/env",
+                "git",
+                "clone",
+                "-b",
+                self.branch,
+                self.url,
+                self.paths.repo_dir,
+            ],
+            self.paths.workdir,
+            "Could not clone repository.",
+        )
 
         return True
 
     def pull(self) -> bool:
         """
         Pull a repository.
 
@@ -500,40 +538,31 @@
         Pull the upstream changes, making sure they're applied locally.
 
         This method will do whatever is necessary to make sure that the upstream changes
         are applied locally. Basically, the idea is that, at the end of this method, the
         local repository looks exactly like the remote and branch that was specified, no
         matter what.
         """
-        if (
-            _run_command(
-                ["/usr/bin/env", "git", "remote", "set-url", "origin", self.url],
-                self.paths.repo_dir,
-            )
-            != 0
-        ):
-            raise Exception("Could not set origin.")
+        _run_command_assuming_exitcode_0(
+            ["/usr/bin/env", "git", "remote", "set-url", "origin", self.url],
+            self.paths.repo_dir,
+            "Could not set origin.",
+        )
 
-        if (
-            _run_command(
-                ["/usr/bin/env", "git", "fetch", "--force", "origin", self.branch],
-                self.paths.repo_dir,
-            )
-            != 0
-        ):
-            raise Exception("Could not fetch from origin.")
+        _run_command_assuming_exitcode_0(
+            ["/usr/bin/env", "git", "fetch", "--force", "origin", self.branch],
+            self.paths.repo_dir,
+            "Could not fetch from origin.",
+        )
 
-        if (
-            _run_command(
-                ["/usr/bin/env", "git", "reset", "--hard", f"origin/{self.branch}"],
-                self.paths.repo_dir,
-            )
-            != 0
-        ):
-            raise Exception("Could not reset local repository to the origin.")
+        _run_command_assuming_exitcode_0(
+            ["/usr/bin/env", "git", "reset", "--hard", f"origin/{self.branch}"],
+            self.paths.repo_dir,
+            "Could not reset local repository to the origin.",
+        )
 
     def clone_or_pull(self) -> bool:
         """Pull a repository, or clone it if it hasn't been initialized yet."""
         for _ in range(MAX_GIT_NETWORK_ATTEMPTS):
             try:
                 if self.is_repo():
                     click.echo(f"Pulling {self.url} to {self.paths.repo_dir}...")
@@ -669,14 +698,15 @@
         path = paths.caches_dir / stale_caches
         click.echo(f"The cache for {stale_caches} is stale, deleting {path}...")
         shutil.rmtree(path)
 
 
 @click.group(cls=HelpColorsGroup, help_headers_color="blue", help_options_color="green")
 @click.option("--debug", is_flag=True, help="Print debug information.")
+@click.version_option()
 def cli(debug: bool):
     global DEBUG
     DEBUG = debug
 
 
 @cli.command()
 @click.option(
@@ -708,15 +738,14 @@
 )
 @click.option(
     "-f",
     "--force-restart",
     is_flag=True,
     help="Restart all apps even if their repositories have not changed.",
 )
-@click.version_option()
 def run(config: Path, working_dir: Path, force_restart: bool):
     workdir = working_dir
     paths = Paths.for_workdir(workdir, config_dir=config.absolute().parent)
     paths.create_directories()
 
     configuration = Configuration.from_yaml(config, paths)
     if not configuration.apps:
```

### Comparing `docker_harbormaster-0.3.0/docker_harbormaster/utils.py` & `docker_harbormaster-0.3.1/docker_harbormaster/utils.py`

 * *Files identical despite different names*

### Comparing `docker_harbormaster-0.3.0/pyproject.toml` & `docker_harbormaster-0.3.1/pyproject.toml`

 * *Files 22% similar despite different names*

```diff
@@ -1,25 +1,24 @@
 [tool.poetry]
 name = "docker-harbormaster"
-version = "0.3.0"
+version = "0.3.1"
 description = "A supervisor for docker-compose apps."
 authors = ["Stavros Korokithakis <hi@stavros.io>"]
 repository = "https://gitlab.com/stavros/harbormaster"
 homepage = "https://gitlab.com/stavros/harbormaster"
 license = "AGPL-3.0-or-later"
 readme = "README.md"
 
 [tool.poetry.scripts]
 harbormaster = "docker_harbormaster.cli:cli"
 
 [tool.poetry.dependencies]
 python = ">=3.7,<4"
-PyYAML = ">=5.4.1"
+PyYAML = ">=6.0.0"
 click = ">=8.1.3"
-docker-compose = ">=1.29.1"
 attrs = ">=21.2.0"
 click-help-colors = ">=0.9.1"
 
 [tool.poetry.dev-dependencies]
 pytest = ">=5.2"
 gitchangelog = {url = "https://github.com/sarnold/gitchangelog/releases/download/3.1.1/gitchangelog-3.1.1-py3-none-any.whl"}
 GitPython = ">=3.1.18"
```

### Comparing `docker_harbormaster-0.3.0/PKG-INFO` & `docker_harbormaster-0.3.1/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,28 +1,27 @@
 Metadata-Version: 2.1
 Name: docker-harbormaster
-Version: 0.3.0
+Version: 0.3.1
 Summary: A supervisor for docker-compose apps.
 Home-page: https://gitlab.com/stavros/harbormaster
 License: AGPL-3.0-or-later
 Author: Stavros Korokithakis
 Author-email: hi@stavros.io
 Requires-Python: >=3.7,<4
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3 or later (AGPLv3+)
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Requires-Dist: PyYAML (>=5.4.1)
+Requires-Dist: PyYAML (>=6.0.0)
 Requires-Dist: attrs (>=21.2.0)
 Requires-Dist: click (>=8.1.3)
 Requires-Dist: click-help-colors (>=0.9.1)
-Requires-Dist: docker-compose (>=1.29.1)
 Project-URL: Repository, https://gitlab.com/stavros/harbormaster
 Description-Content-Type: text/markdown
 
 Harbormaster
 ============
 
 [![PyPI](https://img.shields.io/pypi/v/docker_harbormaster)](https://pypi.org/project/docker-harbormaster/)
@@ -481,14 +480,29 @@
     url: https://gitlab.com/stavros/harbormaster.git
     compose_config: apps/octoprint/docker-compose.harbormaster.yml
 ```
 
 # Changelog
 
 
+## v0.3.1 (2023-07-22)
+
+### Features
+
+* Add git-crypt to the Docker image. [Stavros Korokithakis]
+
+### Fixes
+
+* Change Compose filename. [Stavros Korokithakis]
+
+* Don't restart apps when their configuration hasn't been updated. [葛上昌司]
+
+* Move the --version command to the right place. [Stavros Korokithakis]
+
+
 ## v0.3.0 (2023-03-01)
 
 ### Features
 
 * Add docker image with webhook support. [Jonas Seydel]
 
 ### Fixes
@@ -519,13 +533,191 @@
 
 ## v0.1.20 (2021-11-14)
 
 ### Features
 
 * Restart an app if its environment vars change. [Stavros Korokithakis]
 
+* Add image pruning config option. [Stavros Korokithakis]
+
+* Allow Docker-supported installations. [Stavros Korokithakis]
+
 ### Fixes
 
 * Fix wrong volume path when Harbormaster is deployed inside Docker. [Stavros Korokithakis]
 
 
+## v0.1.19 (2021-10-09)
+
+### Features
+
+* Add YAML environment files. [Stavros Korokithakis]
+
+* Add n8n app. [Stavros Korokithakis]
+
+* Add default values to templates. [Stavros Korokithakis]
+
+* Add Octoprint app config. [Stavros Korokithakis]
+
+* Add executable building. [Stavros Korokithakis]
+
+### Fixes
+
+* Don't try to stop an app if its repo dir doesn't exist. [Stavros Korokithakis]
+
+* Fix changelog display. [Stavros Korokithakis]
+
+
+## v0.1.18 (2021-09-19)
+
+### Features
+
+* Add ztncui app. [Stavros Korokithakis]
+
+### Fixes
+
+* Don't pull disabled apps, no good can come of it. [Stavros Korokithakis]
+
+
+## v0.1.17 (2021-09-13)
+
+### Fixes
+
+* Streamline repository updates and improve change detection (fixes #3) [Stavros Korokithakis]
+
+* Do not pull disabled apps. [Stavros Korokithakis]
+
+* Fail gracefully if no configuration is specified. [Stavros Korokithakis]
+
+
+## v0.1.16 (2021-08-12)
+
+### Fixes
+
+* Fix Compose variables not getting rendered in some cases. [Stavros Korokithakis]
+
+
+## v0.1.15 (2021-06-21)
+
+### Features
+
+* Change `compose_filename` to `compose_config` [Stavros Korokithakis]
+
+* Retry git operations on failure. [Ali Piccioni]
+
+* Add bundled apps. [Stavros Korokithakis]
+
+
+## v0.1.14 (2021-05-19)
+
+### Fixes
+
+* Exit with a 1 if any of the apps failed to deploy. [Stavros Korokithakis]
+
+
+## v0.1.13 (2021-05-18)
+
+### Fixes
+
+* Pull images before starting app. [Stavros Korokithakis]
+
+
+## v0.1.12 (2021-05-18)
+
+### Features
+
+* Add the HM_REPO_DIR variable. [Stavros Korokithakis]
+
+### Fixes
+
+* Improve starting/stopping of apps. [Stavros Korokithakis]
+
+
+## v0.1.10 (2021-05-13)
+
+### Features
+
+* Show better error messages. [Stavros Korokithakis]
+
+### Fixes
+
+* Fix erroneous overwriting of replacements. [Stavros Korokithakis]
+
+* Fix error when environment variables are not strings. [Stavros Korokithakis]
+
+* Build containers when starting. [Stavros Korokithakis]
+
+
+## v0.1.9 (2021-05-12)
+
+### Features
+
+* Allow retrieving replacements and env vars from files. [Stavros Korokithakis]
+
+
+## v0.1.8 (2021-05-10)
+
+### Fixes
+
+* Stop containers properly. [Stavros Korokithakis]
+
+
+## v0.1.7 (2021-05-10)
+
+### Features
+
+* Add "enabled" flag. [Stavros Korokithakis]
+
+
+## v0.1.6 (2021-05-10)
+
+### Fixes
+
+* Gracefully stop containers most of the time. [Stavros Korokithakis]
+
+* Reset repository more forcefully when pulling. [Stavros Korokithakis]
+
+* Rename the default config file. [Stavros Korokithakis]
+
+
+## v0.1.5 (2021-05-10)
+
+### Features
+
+* Add replacements feature. [Stavros Korokithakis]
+
+
+## v0.1.4 (2021-05-09)
+
+### Features
+
+* Add environment variables to the config. [Stavros Korokithakis]
+
+
+## v0.1.3 (2021-05-06)
+
+### Features
+
+* Add the "branch" and "compose_filename" config keys. [Stavros Korokithakis]
+
+
+## v0.1.2 (2021-04-26)
+
+### Fixes
+
+* Support Python 3.6 and up. [Stavros Korokithakis]
+
+
+## v0.1.1 (2021-04-25)
+
+### Features
+
+* Add version command-line option. [Stavros Korokithakis]
+
+* Add directories. [Stavros Korokithakis]
+
+### Fixes
+
+* Fetch before trying to check for changes. [Stavros Korokithakis]
+
+
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

