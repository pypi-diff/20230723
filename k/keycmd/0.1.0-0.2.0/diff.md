# Comparing `tmp/keycmd-0.1.0.tar.gz` & `tmp/keycmd-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "keycmd-0.1.0.tar", max compression
+gzip compressed data, was "keycmd-0.2.0.tar", max compression
```

## Comparing `keycmd-0.1.0.tar` & `keycmd-0.2.0.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0       23 2023-07-20 08:44:53.986331 keycmd-0.1.0/keycmd/__init__.py
--rw-r--r--   0        0        0     1222 2023-07-20 09:01:16.664444 keycmd-0.1.0/keycmd/__main__.py
--rw-r--r--   0        0        0     1992 2023-07-20 09:01:16.677975 keycmd-0.1.0/keycmd/conf.py
--rw-r--r--   0        0        0      803 2023-07-20 10:49:42.404715 keycmd-0.1.0/keycmd/creds.py
--rw-r--r--   0        0        0      339 2023-07-20 08:56:56.572873 keycmd-0.1.0/keycmd/logs.py
--rw-r--r--   0        0        0     1486 2023-07-20 09:01:16.677975 keycmd-0.1.0/keycmd/shell.py
--rw-r--r--   0        0        0     1083 2023-07-20 08:11:40.321032 keycmd-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     5773 2023-07-20 10:51:55.623017 keycmd-0.1.0/README.md
--rw-r--r--   0        0        0     6369 1970-01-01 00:00:00.000000 keycmd-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0     6268 2023-07-23 06:47:53.768874 keycmd-0.2.0/README.md
+-rw-r--r--   0        0        0       22 2023-07-23 06:47:53.768874 keycmd-0.2.0/keycmd/__init__.py
+-rw-r--r--   0        0        0     1166 2023-07-23 06:47:53.768874 keycmd-0.2.0/keycmd/__main__.py
+-rw-r--r--   0        0        0     1973 2023-07-23 06:47:53.768874 keycmd-0.2.0/keycmd/conf.py
+-rw-r--r--   0        0        0      776 2023-07-23 06:47:53.768874 keycmd-0.2.0/keycmd/creds.py
+-rw-r--r--   0        0        0      312 2023-07-23 06:47:53.768874 keycmd-0.2.0/keycmd/logs.py
+-rw-r--r--   0        0        0     1438 2023-07-23 06:47:53.768874 keycmd-0.2.0/keycmd/shell.py
+-rw-r--r--   0        0        0     1055 2023-07-23 06:47:53.768874 keycmd-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0     6864 1970-01-01 00:00:00.000000 keycmd-0.2.0/PKG-INFO
```

### Comparing `keycmd-0.1.0/keycmd/__main__.py` & `keycmd-0.2.0/keycmd/__main__.py`

 * *Ordering differences only*

 * *Files 20% similar despite different names*

```diff
@@ -1,56 +1,56 @@
-import argparse
-
-import tomli
-
-from . import __version__
-from .conf import load_conf
-from .creds import get_env
-from .logs import error, log, set_verbose
-from .shell import run_cmd, run_shell
-
-
-cli = argparse.ArgumentParser(
-    prog="keycmd",
-)
-cli.add_argument(
-    "-v",
-    "--verbose",
-    action="store_true",
-    default=False,
-    help="enable verbose output, useful for configuration debugging",
-)
-cli.add_argument(
-    "--version", action="store_true", default=False, help="print version info"
-)
-cli.add_argument(
-    "--shell",
-    action="store_true",
-    default=False,
-    help="spawn a subshell instead of running a command",
-)
-cli.add_argument("command", nargs="*", help="command to run")
-
-
-def main():
-    """CLI entrypoint"""
-    args = cli.parse_args()
-
-    if args.verbose:
-        set_verbose()
-
-    if args.version:
-        log(f"v{__version__}")
-        return
-
-    try:
-        conf = load_conf()
-    except tomli.TOMLDecodeError as err:
-        error(err)
-    env = get_env(conf)
-
-    if args.shell:
-        run_shell(env=env)
-    elif args.command:
-        run_cmd(args.command, env=env)
-    else:
-        error("missing command argument")
+import argparse
+
+import tomli
+
+from . import __version__
+from .conf import load_conf
+from .creds import get_env
+from .logs import error, log, set_verbose
+from .shell import run_cmd, run_shell
+
+
+cli = argparse.ArgumentParser(
+    prog="keycmd",
+)
+cli.add_argument(
+    "-v",
+    "--verbose",
+    action="store_true",
+    default=False,
+    help="enable verbose output, useful for configuration debugging",
+)
+cli.add_argument(
+    "--version", action="store_true", default=False, help="print version info"
+)
+cli.add_argument(
+    "--shell",
+    action="store_true",
+    default=False,
+    help="spawn a subshell instead of running a command",
+)
+cli.add_argument("command", nargs="*", help="command to run")
+
+
+def main():
+    """CLI entrypoint"""
+    args = cli.parse_args()
+
+    if args.verbose:
+        set_verbose()
+
+    if args.version:
+        log(f"v{__version__}")
+        return
+
+    try:
+        conf = load_conf()
+    except tomli.TOMLDecodeError as err:
+        error(err)
+    env = get_env(conf)
+
+    if args.shell:
+        run_shell(env=env)
+    elif args.command:
+        run_cmd(args.command, env=env)
+    else:
+        error("missing command argument")
```

### Comparing `keycmd-0.1.0/keycmd/conf.py` & `keycmd-0.2.0/keycmd/conf.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,77 +1,82 @@
-from pathlib import Path
-from pprint import pformat
-
-import tomli
-
-from .logs import vlog
-
-
-def load_toml(path):
-    """Load a toml file"""
-    with path.open("rb") as fh:
-        try:
-            return tomli.load(fh)
-        except tomli.TOMLDecodeError as err:
-            raise tomli.TOMLDecodeError(f"invalid TOML in {path}:\n{err}")
-
-
-def load_pyproj(path):
-    """Load [tool.keycmd] from a pyproject.toml file"""
-    data = load_toml(path)
-    return data.get("tool", {}).get("keycmd", {})
-
-
-def defaults():
-    """Generate the default config"""
-    return {}
-
-
-def merge_conf(a, b):
-    """
-    Merges two deep dictionary structures.
-    All other datatypes are simply overwritten
-    """
-    a = a.copy()
-    for key, value in b.items():
-        if isinstance(value, dict):
-            old_value = a.setdefault(key, {})
-            a[key] = merge_conf(old_value, value)
-        else:
-            a[key] = value
-    return a
-
-
-def load_conf():
-    """
-    Load merged configuration from the following files:
-    - defaults()
-    - ~/.keycmd
-    - ./.keycmd
-    - first pyproject.toml found while walking file system up from .
-    """
-    conf = defaults()
-    cwd = Path.cwd()
-
-    # fixed conf locations, in order
-    for path in [Path.home(), cwd]:
-        fpath = path / ".keycmd"
-        if fpath.is_file():
-            vlog(f"loading config file {fpath}")
-            conf = merge_conf(conf, load_toml(fpath))
-
-    # dynamic conf locations, walk up from current directory
-    cur = cwd
-    while cur != cur.anchor:
-        pyproj = cur / "pyproject.toml"
-        if pyproj.is_file():
-            vlog(f"loading config file {pyproj}")
-            conf = merge_conf(conf, load_pyproj(pyproj))
-            break
-        # stop at the boundary of git repositories
-        if (cur / ".git").is_dir():
-            break
-        cur = cur.parent
-
-    vlog(f"merged config:\n{pformat(conf)}")
-
-    return conf
+from pathlib import Path
+from pprint import pformat
+
+import tomli
+
+from .logs import vlog
+
+
+def load_toml(path):
+    """Load a toml file"""
+    with path.open("rb") as fh:
+        try:
+            return tomli.load(fh)
+        except tomli.TOMLDecodeError as err:
+            raise tomli.TOMLDecodeError(f"invalid TOML in {path}:\n{err}")
+
+
+def load_pyproj(path):
+    """Load [tool.keycmd] from a pyproject.toml file"""
+    data = load_toml(path)
+    return data.get("tool", {}).get("keycmd", {})
+
+
+def defaults():
+    """Generate the default config"""
+    return {}
+
+
+def merge_conf(a, b):
+    """
+    Merges two deep dictionary structures.
+    All other datatypes are simply overwritten
+    """
+    a = a.copy()
+    for key, value in b.items():
+        if isinstance(value, dict):
+            old_value = a.setdefault(key, {})
+            a[key] = merge_conf(old_value, value)
+        else:
+            a[key] = value
+    return a
+
+
+def load_conf():
+    """
+    Load merged configuration from the following files:
+    - defaults()
+    - ~/.keycmd
+    - first pyproject.toml found while walking file system up from .
+    - ./.keycmd
+    """
+    conf = defaults()
+    cwd = Path.cwd()
+
+    # ~/.keycmd
+    fpath = Path.home() / ".keycmd"
+    if fpath.is_file():
+        vlog(f"loading config file {fpath}")
+        conf = merge_conf(conf, load_toml(fpath))
+
+    # pyproject.toml
+    cur = cwd
+    while cur != cur.anchor:
+        pyproj = cur / "pyproject.toml"
+        if pyproj.is_file():
+            vlog(f"loading config file {pyproj}")
+            conf = merge_conf(conf, load_pyproj(pyproj))
+            break
+        # stop at the boundary of git repositories
+        if (cur / ".git").is_dir():
+            break
+        cur = cur.parent
+
+    # ./.keycmd
+    fpath = cwd / ".keycmd"
+    if fpath.is_file():
+        vlog(f"loading config file {fpath}")
+        conf = merge_conf(conf, load_toml(fpath))
+
+    vlog(f"merged config:\n{pformat(conf)}")
+
+    return conf
```

### Comparing `keycmd-0.1.0/keycmd/creds.py` & `keycmd-0.2.0/keycmd/creds.py`

 * *Ordering differences only*

 * *Files 22% similar despite different names*

```diff
@@ -1,27 +1,27 @@
-import base64
-from os import environ
-
-import keyring
-
-from .logs import vlog
-
-
-def b64(value):
-    """Convert a string to its base64 representation"""
-    return base64.b64encode(value.encode("utf-8")).decode("utf-8")
-
-
-def get_env(conf):
-    """Load credentials from the OS keyring according to user configuration"""
-    env = environ.copy()
-    for key, src in conf["keys"].items():
-        password = keyring.get_password(src["credential"], src["username"])
-        if src.get("b64"):
-            password = b64(password)
-        env[key] = password
-        vlog(
-            f"exposing credential {src['credential']}"
-            f" belonging to user {src['username']}"
-            f" as environment variable {key} (b64: {src.get('b64', False)})"
-        )
-    return env
+import base64
+from os import environ
+
+import keyring
+
+from .logs import vlog
+
+
+def b64(value):
+    """Convert a string to its base64 representation"""
+    return base64.b64encode(value.encode("utf-8")).decode("utf-8")
+
+
+def get_env(conf):
+    """Load credentials from the OS keyring according to user configuration"""
+    env = environ.copy()
+    for key, src in conf["keys"].items():
+        password = keyring.get_password(src["credential"], src["username"])
+        if src.get("b64"):
+            password = b64(password)
+        env[key] = password
+        vlog(
+            f"exposing credential {src['credential']}"
+            f" belonging to user {src['username']}"
+            f" as environment variable {key} (b64: {src.get('b64', False)})"
+        )
+    return env
```

### Comparing `keycmd-0.1.0/keycmd/shell.py` & `keycmd-0.2.0/keycmd/shell.py`

 * *Ordering differences only*

 * *Files 11% similar despite different names*

```diff
@@ -1,48 +1,48 @@
-import os
-from pathlib import Path
-from pprint import pformat
-from subprocess import run
-from sys import exit
-
-from shellingham import detect_shell, ShellDetectionFailure
-
-from .logs import vlog, vwarn
-
-
-def get_shell():
-    """Use shellingham to detect the shell that invoked
-    this Python process"""
-    try:
-        shell_name, shell_path = detect_shell(os.getpid())
-    except ShellDetectionFailure:
-        vwarn("failed to detect parent process shell, falling back to system default")
-        if os.name == "posix":
-            shell_path = os.environ["SHELL"]
-        elif os.name == "nt":
-            shell_path = os.environ["COMSPEC"]
-        else:
-            raise NotImplementedError(f"os {os.name} support not available")
-        shell_name = Path(shell_path).name.lower()
-    vlog(f"detected shell: {shell_path}")
-    return shell_name, shell_path
-
-
-def run_shell(env=None):
-    """Open an interactive shell for the user to interact
-    with."""
-    _, shell_path = get_shell()
-    vlog("spawning subshell")
-    p = run(shell_path, shell=False, env=env)
-    exit(p.returncode)
-
-
-def run_cmd(cmd, env=None):
-    """Run a one-off command in a shell."""
-    shell_name, shell_path = get_shell()
-    opt = "-c"
-    if shell_name == "cmd":
-        opt = "/C"
-    full_command = [shell_path, opt, *cmd]
-    vlog(f"running command: {pformat(full_command)}")
-    p = run(full_command, shell=False, env=env)
-    exit(p.returncode)
+import os
+from pathlib import Path
+from pprint import pformat
+from subprocess import run
+from sys import exit
+
+from shellingham import detect_shell, ShellDetectionFailure
+
+from .logs import vlog, vwarn
+
+
+def get_shell():
+    """Use shellingham to detect the shell that invoked
+    this Python process"""
+    try:
+        shell_name, shell_path = detect_shell(os.getpid())
+    except ShellDetectionFailure:
+        vwarn("failed to detect parent process shell, falling back to system default")
+        if os.name == "posix":
+            shell_path = os.environ["SHELL"]
+        elif os.name == "nt":
+            shell_path = os.environ["COMSPEC"]
+        else:
+            raise NotImplementedError(f"os {os.name} support not available")
+        shell_name = Path(shell_path).name.lower()
+    vlog(f"detected shell: {shell_path}")
+    return shell_name, shell_path
+
+
+def run_shell(env=None):
+    """Open an interactive shell for the user to interact
+    with."""
+    _, shell_path = get_shell()
+    vlog("spawning subshell")
+    p = run(shell_path, shell=False, env=env)
+    exit(p.returncode)
+
+
+def run_cmd(cmd, env=None):
+    """Run a one-off command in a shell."""
+    shell_name, shell_path = get_shell()
+    opt = "-c"
+    if shell_name == "cmd":
+        opt = "/C"
+    full_command = [shell_path, opt, *cmd]
+    vlog(f"running command: {pformat(full_command)}")
+    p = run(full_command, shell=False, env=env)
+    exit(p.returncode)
```

### Comparing `keycmd-0.1.0/pyproject.toml` & `keycmd-0.2.0/pyproject.toml`

 * *Files 23% similar despite different names*

```diff
@@ -1,45 +1,46 @@
-[tool.poetry]
-name = "keycmd"
-version = "0.1.0"
-description = ""
-authors = ["Korijn van Golen <korijn.vangolen@zimmerbiomet.com>"]
-license = "MIT"
-readme = "README.md"
-
-[tool.poetry.dependencies]
-python = "^3.9"
-keyring = "~24.2.0"
-tomli = "^2.0.1"
-shellingham = "^1.5.0.post1"
-
-[tool.poetry.scripts]
-keycmd = 'keycmd.__main__:main'
-
-[tool.poetry.group.dev.dependencies]
-ruff = "^0.0.278"
-black = "^23.7.0"
-
-[build-system]
-requires = ["poetry-core"]
-build-backend = "poetry.core.masonry.api"
-
-[tool.ruff]
-select = [
-	"E",  # pycodestyle
-	"F",  # pyflakes
-	"I",  # isort
-	"N",  # pep8-naming
-	"ARG",  # flake8-unused-arguments
-	"T10",  # flake8-debugger
-	"RUF",  # Ruff-specific rules
-]
-
-[tool.ruff.isort]
-force-sort-within-sections = true
-order-by-type = false
-lines-after-imports = 2
-
-# example config for development and testing
-[tool.keycmd.keys]
-ARTIFACTS_TOKEN = { credential = "azure@poetry-repository-main", username = "azure" }
-ARTIFACTS_TOKEN_B64 = { credential = "azure@poetry-repository-main", username = "azure", b64 = true }
+[tool.poetry]
+name = "keycmd"
+version = "0.2.0"
+description = ""
+authors = ["Korijn van Golen <korijn.vangolen@zimmerbiomet.com>"]
+license = "MIT"
+readme = "README.md"
+
+[tool.poetry.dependencies]
+python = "^3.9"
+keyring = "~24.2.0"
+tomli = "^2.0.1"
+shellingham = "^1.5.0.post1"
+
+[tool.poetry.scripts]
+keycmd = 'keycmd.__main__:main'
+
+[tool.poetry.group.dev.dependencies]
+ruff = "^0.0.278"
+black = "^23.7.0"
+twine = "^4.0.2"
+
+[build-system]
+requires = ["poetry-core"]
+build-backend = "poetry.core.masonry.api"
+
+[tool.ruff]
+select = [
+	"E",  # pycodestyle
+	"F",  # pyflakes
+	"I",  # isort
+	"N",  # pep8-naming
+	"ARG",  # flake8-unused-arguments
+	"T10",  # flake8-debugger
+	"RUF",  # Ruff-specific rules
+]
+
+[tool.ruff.isort]
+force-sort-within-sections = true
+order-by-type = false
+lines-after-imports = 2
+
+# example config for development and testing
+[tool.keycmd.keys]
+ARTIFACTS_TOKEN = { credential = "azure@poetry-repository-main", username = "azure" }
+ARTIFACTS_TOKEN_B64 = { credential = "azure@poetry-repository-main", username = "azure", b64 = true }
```

### Comparing `keycmd-0.1.0/README.md` & `keycmd-0.2.0/README.md`

 * *Files 11% similar despite different names*

```diff
@@ -1,14 +1,18 @@
 # keycmd
 
+[![CI](https://github.com/clinicalgraphics/keycmd/actions/workflows/ci.yml/badge.svg)](https://github.com/clinicalgraphics/keycmd/actions/workflows/ci.yml)
+[![PyPI version ](https://badge.fury.io/py/keycmd.svg)
+](https://badge.fury.io/py/keycmd)
+
 The main functionality of `keycmd` is to load secrets from your OS keyring and expose them as environment variables for the duration of a single shell command or alternatively for the lifetime of a subshell.
 
 This enables you to store sensitive data such as authentication tokens and passwords in your OS keyring, so you no longer need to rely on insecure practises such as `.env` files, or pasting secrets into your terminal. 😱
 
-The most common use case is to load credentials for package managers such as pip, npm when using private package indexes, such as Azure Artifact Feeds. Another common use case is docker build secrets.
+The most common use case is to load credentials for package managers such as pip and npm when using private package indexes, such as Azure Artifact Feeds. Another common use case is docker build secrets.
 
 ## Usage
 
 Install `keycmd` from pypi using `pip install keycmd`, or whatever alternative python package manager you prefer.
 
 The CLI has the following options:
 
@@ -32,55 +36,55 @@
 * `keycmd --shell`
 
 The first is the most preferred method, since your secrets will only be exposed as environment variables during a one-off command. The latter is less preferable, but can be convenient if you are debugging some process that depends on the credentials you are exposing.
 
 ## Configuration
 
 > **Note**
-> if you are having trouble configuring keycmd, refer to the section [debugging configuration](#debugging-configuration).
+> if you are having trouble configuring keycmd, refer to section [debugging configuration](#debugging-configuration).
 
 ### Locations
 
 Configuration can be stored in three places (where `~` is the user home folder and `.` is the current working directory when calling `keycmd`):
 
 - `~/.keycmd`
-- `./.keycmd`
 - first `pyproject.toml` found while walking file system up from `.`
+- `./.keycmd`
 
-Configuration is merged where more local configuration values have precendence.
+Configuration files are loaded and merged in the listed order.
 
 ### Options
 
 The options are a nested dictionary, defined as follows:
 
 * `keys`: dict
   * `{key_name}`: dict
     * `credential`: str
     * `username`: str
     * `b64`: bool, optional
 
 You can define as many keys as you like. For each key, you are required to define:
 
-* the `key_name`, which is the name of the environment variable under which the credential will be exposed.
+* the `key_name`, which is the name of the environment variable under which the credential will be exposed
 * the `credential`, which is the name of the credential in your OS keyring
 * the `username`, which is the name of the user owning the credential in the OS keyring
 
 Optionally, you can also set `b64` to `true` to apply base64 encoding to the credential.
 
 ## Example configuration for Poetry, npm and docker-compose
 
-In this example, I've stored the following configuration in `~/.keyring`:
+In this example, I've stored the following configuration in `~/.keycmd`:
 
 ```toml
 [keys]
 ARTIFACTS_TOKEN = { credential = "korijn@poetry-repository-main", username = "korijn" }
 ARTIFACTS_TOKEN_B64 = { credential = "korijn@poetry-repository-main", username = "korijn", b64 = true }
 ```
 
-This configuration piggybacks off of the credentials created in the OS keyring by [Poetry](https://python-poetry.org/) when [configuring credentials](https://python-poetry.org/docs/repositories/#configuring-credentials) for a private repository. In this case, we expose the same credential is exposed twice:
+This configuration piggybacks off of the credentials created in the OS keyring by [Poetry](https://python-poetry.org/) when [configuring credentials](https://python-poetry.org/docs/repositories/#configuring-credentials) for a private repository. In this case, the same credential is exposed twice:
 
 * As the environment variable `ARTIFACTS_TOKEN`
 * Again but with base64 encoding applied as the environment variable `ARTIFACTS_TOKEN_B64`
 
 For my npm project, I have a [`.npmrc` file](https://docs.npmjs.com/cli/v7/configuring-npm/npmrc) with the following contents:
 
 ```
@@ -90,42 +94,45 @@
 //pkgs.dev.azure.com/my_organization/_packaging/main/npm/registry/:_password=${ARTIFACTS_TOKEN_B64}
 //pkgs.dev.azure.com/my_organization/_packaging/main/npm/registry/:email=email
 //pkgs.dev.azure.com/my_organization/_packaging/main/npm/:username=dev
 //pkgs.dev.azure.com/my_organization/_packaging/main/npm/:_password=${ARTIFACTS_TOKEN_B64}
 //pkgs.dev.azure.com/my_organization/_packaging/main/npm/:email=email
 ```
 
-Now, I can set up my `node_modules` just by calling `keycmd npm install`.
+Now, I can set up my `node_modules` just by calling `keycmd npm install`! 🚀
+
+> **Note**
+> npm will complain if you make any calls such as `npm run [...]` without the environment variable set. 🙄 You can set them to the empty string to make npm shut up. I use `export ARTIFACTS_TOKEN_B64=` (or `setx ARTIFACTS_TOKEN_B64=` on Windows).
 
 Additionally, I also have a docker-compose file in this project which is configured as follows:
 
 ```yml
 secrets:
   token:
     environment: ARTIFACTS_TOKEN
   token_b64:
     environment: ARTIFACTS_TOKEN_B64
 ```
 
-When I call `keycmd docker compose build` these two variables are exposed by keycmd and subsequently they are available as [docker compose build secrets](https://docs.docker.com/compose/use-secrets/).
+When I call `keycmd docker compose build` these two variables are exposed by keycmd and subsequently they are available as [docker compose build secrets](https://docs.docker.com/compose/use-secrets/). 👌
 
 ## Debugging configuration
 
 If you're not getting the results you expected, use the `-v` flag
 to debug your configuration.
 
 ```
 ❯ poetry run keycmd -v echo %ARTIFACTS_TOKEN_B64%
 keycmd: loading config file C:\Users\kvang\.keycmd
 keycmd: loading config file C:\Users\kvang\dev\keycmd\pyproject.toml
 keycmd: merged config:
-{'keys': {'ARTIFACTS_TOKEN': {'credential': 'azure@poetry-repository-main',
-                              'username': 'azure'},
+{'keys': {'ARTIFACTS_TOKEN': {'credential': 'korijn@poetry-repository-main',
+                              'username': 'korijn'},
           'ARTIFACTS_TOKEN_B64': {'b64': True,
-                                  'credential': 'azure@poetry-repository-main',
-                                  'username': 'azure'}}}
-keycmd: exposing credential azure@poetry-repository-main belonging to user azure as environment variable ARTIFACTS_TOKEN (b64: False)
-keycmd: exposing credential azure@poetry-repository-main belonging to user azure as environment variable ARTIFACTS_TOKEN_B64 (b64: True)
+                                  'credential': 'korijn@poetry-repository-main',
+                                  'username': 'korijn'}}}
+keycmd: exposing credential korijn@poetry-repository-main belonging to user korijn as environment variable ARTIFACTS_TOKEN (b64: False)
+keycmd: exposing credential korijn@poetry-repository-main belonging to user korijn as environment variable ARTIFACTS_TOKEN_B64 (b64: True)
 keycmd: detected shell: C:\Windows\System32\cmd.exe
 keycmd: running command: ['C:\\Windows\\System32\\cmd.exe', '/C', 'echo', '%ARTIFACTS_TOKEN_B64%']
 aSdtIG5vdCB0aGF0IHN0dXBpZCA6KQ==
 ```
```

### Comparing `keycmd-0.1.0/PKG-INFO` & `keycmd-0.2.0/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: keycmd
-Version: 0.1.0
+Version: 0.2.0
 Summary: 
 License: MIT
 Author: Korijn van Golen
 Author-email: korijn.vangolen@zimmerbiomet.com
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -14,19 +14,23 @@
 Requires-Dist: keyring (>=24.2.0,<24.3.0)
 Requires-Dist: shellingham (>=1.5.0.post1,<2.0.0)
 Requires-Dist: tomli (>=2.0.1,<3.0.0)
 Description-Content-Type: text/markdown
 
 # keycmd
 
+[![CI](https://github.com/clinicalgraphics/keycmd/actions/workflows/ci.yml/badge.svg)](https://github.com/clinicalgraphics/keycmd/actions/workflows/ci.yml)
+[![PyPI version ](https://badge.fury.io/py/keycmd.svg)
+](https://badge.fury.io/py/keycmd)
+
 The main functionality of `keycmd` is to load secrets from your OS keyring and expose them as environment variables for the duration of a single shell command or alternatively for the lifetime of a subshell.
 
 This enables you to store sensitive data such as authentication tokens and passwords in your OS keyring, so you no longer need to rely on insecure practises such as `.env` files, or pasting secrets into your terminal. 😱
 
-The most common use case is to load credentials for package managers such as pip, npm when using private package indexes, such as Azure Artifact Feeds. Another common use case is docker build secrets.
+The most common use case is to load credentials for package managers such as pip and npm when using private package indexes, such as Azure Artifact Feeds. Another common use case is docker build secrets.
 
 ## Usage
 
 Install `keycmd` from pypi using `pip install keycmd`, or whatever alternative python package manager you prefer.
 
 The CLI has the following options:
 
@@ -50,55 +54,55 @@
 * `keycmd --shell`
 
 The first is the most preferred method, since your secrets will only be exposed as environment variables during a one-off command. The latter is less preferable, but can be convenient if you are debugging some process that depends on the credentials you are exposing.
 
 ## Configuration
 
 > **Note**
-> if you are having trouble configuring keycmd, refer to the section [debugging configuration](#debugging-configuration).
+> if you are having trouble configuring keycmd, refer to section [debugging configuration](#debugging-configuration).
 
 ### Locations
 
 Configuration can be stored in three places (where `~` is the user home folder and `.` is the current working directory when calling `keycmd`):
 
 - `~/.keycmd`
-- `./.keycmd`
 - first `pyproject.toml` found while walking file system up from `.`
+- `./.keycmd`
 
-Configuration is merged where more local configuration values have precendence.
+Configuration files are loaded and merged in the listed order.
 
 ### Options
 
 The options are a nested dictionary, defined as follows:
 
 * `keys`: dict
   * `{key_name}`: dict
     * `credential`: str
     * `username`: str
     * `b64`: bool, optional
 
 You can define as many keys as you like. For each key, you are required to define:
 
-* the `key_name`, which is the name of the environment variable under which the credential will be exposed.
+* the `key_name`, which is the name of the environment variable under which the credential will be exposed
 * the `credential`, which is the name of the credential in your OS keyring
 * the `username`, which is the name of the user owning the credential in the OS keyring
 
 Optionally, you can also set `b64` to `true` to apply base64 encoding to the credential.
 
 ## Example configuration for Poetry, npm and docker-compose
 
-In this example, I've stored the following configuration in `~/.keyring`:
+In this example, I've stored the following configuration in `~/.keycmd`:
 
 ```toml
 [keys]
 ARTIFACTS_TOKEN = { credential = "korijn@poetry-repository-main", username = "korijn" }
 ARTIFACTS_TOKEN_B64 = { credential = "korijn@poetry-repository-main", username = "korijn", b64 = true }
 ```
 
-This configuration piggybacks off of the credentials created in the OS keyring by [Poetry](https://python-poetry.org/) when [configuring credentials](https://python-poetry.org/docs/repositories/#configuring-credentials) for a private repository. In this case, we expose the same credential is exposed twice:
+This configuration piggybacks off of the credentials created in the OS keyring by [Poetry](https://python-poetry.org/) when [configuring credentials](https://python-poetry.org/docs/repositories/#configuring-credentials) for a private repository. In this case, the same credential is exposed twice:
 
 * As the environment variable `ARTIFACTS_TOKEN`
 * Again but with base64 encoding applied as the environment variable `ARTIFACTS_TOKEN_B64`
 
 For my npm project, I have a [`.npmrc` file](https://docs.npmjs.com/cli/v7/configuring-npm/npmrc) with the following contents:
 
 ```
@@ -108,43 +112,46 @@
 //pkgs.dev.azure.com/my_organization/_packaging/main/npm/registry/:_password=${ARTIFACTS_TOKEN_B64}
 //pkgs.dev.azure.com/my_organization/_packaging/main/npm/registry/:email=email
 //pkgs.dev.azure.com/my_organization/_packaging/main/npm/:username=dev
 //pkgs.dev.azure.com/my_organization/_packaging/main/npm/:_password=${ARTIFACTS_TOKEN_B64}
 //pkgs.dev.azure.com/my_organization/_packaging/main/npm/:email=email
 ```
 
-Now, I can set up my `node_modules` just by calling `keycmd npm install`.
+Now, I can set up my `node_modules` just by calling `keycmd npm install`! 🚀
+
+> **Note**
+> npm will complain if you make any calls such as `npm run [...]` without the environment variable set. 🙄 You can set them to the empty string to make npm shut up. I use `export ARTIFACTS_TOKEN_B64=` (or `setx ARTIFACTS_TOKEN_B64=` on Windows).
 
 Additionally, I also have a docker-compose file in this project which is configured as follows:
 
 ```yml
 secrets:
   token:
     environment: ARTIFACTS_TOKEN
   token_b64:
     environment: ARTIFACTS_TOKEN_B64
 ```
 
-When I call `keycmd docker compose build` these two variables are exposed by keycmd and subsequently they are available as [docker compose build secrets](https://docs.docker.com/compose/use-secrets/).
+When I call `keycmd docker compose build` these two variables are exposed by keycmd and subsequently they are available as [docker compose build secrets](https://docs.docker.com/compose/use-secrets/). 👌
 
 ## Debugging configuration
 
 If you're not getting the results you expected, use the `-v` flag
 to debug your configuration.
 
 ```
 ❯ poetry run keycmd -v echo %ARTIFACTS_TOKEN_B64%
 keycmd: loading config file C:\Users\kvang\.keycmd
 keycmd: loading config file C:\Users\kvang\dev\keycmd\pyproject.toml
 keycmd: merged config:
-{'keys': {'ARTIFACTS_TOKEN': {'credential': 'azure@poetry-repository-main',
-                              'username': 'azure'},
+{'keys': {'ARTIFACTS_TOKEN': {'credential': 'korijn@poetry-repository-main',
+                              'username': 'korijn'},
           'ARTIFACTS_TOKEN_B64': {'b64': True,
-                                  'credential': 'azure@poetry-repository-main',
-                                  'username': 'azure'}}}
-keycmd: exposing credential azure@poetry-repository-main belonging to user azure as environment variable ARTIFACTS_TOKEN (b64: False)
-keycmd: exposing credential azure@poetry-repository-main belonging to user azure as environment variable ARTIFACTS_TOKEN_B64 (b64: True)
+                                  'credential': 'korijn@poetry-repository-main',
+                                  'username': 'korijn'}}}
+keycmd: exposing credential korijn@poetry-repository-main belonging to user korijn as environment variable ARTIFACTS_TOKEN (b64: False)
+keycmd: exposing credential korijn@poetry-repository-main belonging to user korijn as environment variable ARTIFACTS_TOKEN_B64 (b64: True)
 keycmd: detected shell: C:\Windows\System32\cmd.exe
 keycmd: running command: ['C:\\Windows\\System32\\cmd.exe', '/C', 'echo', '%ARTIFACTS_TOKEN_B64%']
 aSdtIG5vdCB0aGF0IHN0dXBpZCA6KQ==
 ```
```

