# Comparing `tmp/pyempaq-0.3.1.tar.gz` & `tmp/pyempaq-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyempaq-0.3.1.tar", last modified: Thu Apr 20 14:27:20 2023, max compression
+gzip compressed data, was "pyempaq-0.4.0.tar", last modified: Sun Jul 23 19:26:09 2023, max compression
```

## Comparing `pyempaq-0.3.1.tar` & `pyempaq-0.4.0.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxrwxr-x   0 facundo   (1000) facundo   (1000)        0 2023-04-20 14:27:20.355540 pyempaq-0.3.1/
--rw-rw-r--   0 facundo   (1000) facundo   (1000)    35149 2021-07-15 22:17:23.000000 pyempaq-0.3.1/LICENSE
--rw-rw-r--   0 facundo   (1000) facundo   (1000)       59 2021-09-26 15:51:02.000000 pyempaq-0.3.1/MANIFEST.in
--rw-rw-r--   0 facundo   (1000) facundo   (1000)    12899 2023-04-20 14:27:20.355540 pyempaq-0.3.1/PKG-INFO
--rw-rw-r--   0 facundo   (1000) facundo   (1000)    12207 2023-04-19 21:19:57.000000 pyempaq-0.3.1/README.md
-drwxrwxr-x   0 facundo   (1000) facundo   (1000)        0 2023-04-20 14:27:20.355540 pyempaq-0.3.1/pyempaq/
--rw-rw-r--   0 facundo   (1000) facundo   (1000)      267 2023-02-19 18:32:46.000000 pyempaq-0.3.1/pyempaq/__init__.py
--rw-rw-r--   0 facundo   (1000) facundo   (1000)      258 2021-07-17 21:32:58.000000 pyempaq-0.3.1/pyempaq/__main__.py
--rw-rw-r--   0 facundo   (1000) facundo   (1000)      488 2023-04-20 14:27:16.000000 pyempaq-0.3.1/pyempaq/_version.py
--rw-rw-r--   0 facundo   (1000) facundo   (1000)     1485 2022-06-19 15:17:40.000000 pyempaq-0.3.1/pyempaq/common.py
--rw-rw-r--   0 facundo   (1000) facundo   (1000)     6381 2023-04-17 17:23:34.000000 pyempaq-0.3.1/pyempaq/config_manager.py
--rw-rw-r--   0 facundo   (1000) facundo   (1000)     9755 2023-04-20 14:26:40.000000 pyempaq-0.3.1/pyempaq/main.py
--rw-rw-r--   0 facundo   (1000) facundo   (1000)     6600 2023-04-20 14:26:40.000000 pyempaq-0.3.1/pyempaq/unpacker.py
-drwxrwxr-x   0 facundo   (1000) facundo   (1000)        0 2023-04-20 14:27:20.355540 pyempaq-0.3.1/pyempaq.egg-info/
--rw-rw-r--   0 facundo   (1000) facundo   (1000)    12899 2023-04-20 14:27:20.000000 pyempaq-0.3.1/pyempaq.egg-info/PKG-INFO
--rw-rw-r--   0 facundo   (1000) facundo   (1000)      383 2023-04-20 14:27:20.000000 pyempaq-0.3.1/pyempaq.egg-info/SOURCES.txt
--rw-rw-r--   0 facundo   (1000) facundo   (1000)        1 2023-04-20 14:27:20.000000 pyempaq-0.3.1/pyempaq.egg-info/dependency_links.txt
--rw-rw-r--   0 facundo   (1000) facundo   (1000)       47 2023-04-20 14:27:20.000000 pyempaq-0.3.1/pyempaq.egg-info/entry_points.txt
--rw-rw-r--   0 facundo   (1000) facundo   (1000)       28 2023-04-20 14:27:20.000000 pyempaq-0.3.1/pyempaq.egg-info/requires.txt
--rw-rw-r--   0 facundo   (1000) facundo   (1000)        8 2023-04-20 14:27:20.000000 pyempaq-0.3.1/pyempaq.egg-info/top_level.txt
--rw-rw-r--   0 facundo   (1000) facundo   (1000)       28 2022-04-15 13:03:12.000000 pyempaq-0.3.1/requirements.txt
--rw-rw-r--   0 facundo   (1000) facundo   (1000)       38 2023-04-20 14:27:20.355540 pyempaq-0.3.1/setup.cfg
--rwxrwxr-x   0 facundo   (1000) facundo   (1000)     1776 2023-04-19 21:47:43.000000 pyempaq-0.3.1/setup.py
+drwxrwxr-x   0 facundo   (1000) facundo   (1000)        0 2023-07-23 19:26:09.252106 pyempaq-0.4.0/
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)    35149 2021-07-15 22:17:23.000000 pyempaq-0.4.0/LICENSE
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)       59 2021-09-26 15:51:02.000000 pyempaq-0.4.0/MANIFEST.in
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)    13582 2023-07-23 19:26:09.252106 pyempaq-0.4.0/PKG-INFO
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)    12890 2023-07-12 18:17:27.000000 pyempaq-0.4.0/README.md
+drwxrwxr-x   0 facundo   (1000) facundo   (1000)        0 2023-07-23 19:26:09.252106 pyempaq-0.4.0/pyempaq/
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)      267 2023-06-05 21:26:44.000000 pyempaq-0.4.0/pyempaq/__init__.py
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)      258 2021-07-17 21:32:58.000000 pyempaq-0.4.0/pyempaq/__main__.py
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)      488 2023-07-23 19:25:50.000000 pyempaq-0.4.0/pyempaq/_version.py
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)     1570 2023-07-08 01:49:55.000000 pyempaq-0.4.0/pyempaq/common.py
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)     6381 2023-07-06 21:13:56.000000 pyempaq-0.4.0/pyempaq/config_manager.py
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)    10423 2023-07-08 01:49:55.000000 pyempaq-0.4.0/pyempaq/main.py
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)    10057 2023-07-22 23:14:11.000000 pyempaq-0.4.0/pyempaq/unpacker.py
+drwxrwxr-x   0 facundo   (1000) facundo   (1000)        0 2023-07-23 19:26:09.252106 pyempaq-0.4.0/pyempaq.egg-info/
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)    13582 2023-07-23 19:26:09.000000 pyempaq-0.4.0/pyempaq.egg-info/PKG-INFO
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)      383 2023-07-23 19:26:09.000000 pyempaq-0.4.0/pyempaq.egg-info/SOURCES.txt
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)        1 2023-07-23 19:26:09.000000 pyempaq-0.4.0/pyempaq.egg-info/dependency_links.txt
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)       47 2023-07-23 19:26:09.000000 pyempaq-0.4.0/pyempaq.egg-info/entry_points.txt
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)       32 2023-07-23 19:26:09.000000 pyempaq-0.4.0/pyempaq.egg-info/requires.txt
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)        8 2023-07-23 19:26:09.000000 pyempaq-0.4.0/pyempaq.egg-info/top_level.txt
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)       32 2023-07-22 22:42:52.000000 pyempaq-0.4.0/requirements.txt
+-rw-rw-r--   0 facundo   (1000) facundo   (1000)       38 2023-07-23 19:26:09.252106 pyempaq-0.4.0/setup.cfg
+-rwxrwxr-x   0 facundo   (1000) facundo   (1000)     1776 2023-06-05 21:26:44.000000 pyempaq-0.4.0/setup.py
```

### Comparing `pyempaq-0.3.1/LICENSE` & `pyempaq-0.4.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pyempaq-0.3.1/PKG-INFO` & `pyempaq-0.4.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyempaq
-Version: 0.3.1
+Version: 0.4.0
 Summary: A Python packer to run anywhwere any project with any virtualenv dependencies.
 Home-page: https://github.com/facundobatista/pyempaq
 Author: Facundo Batista
 Author-email: facundo@taniquetil.com.ar
 License: GPL-v3
 Platform: UNKNOWN
 Classifier: Environment :: Console
@@ -84,22 +84,30 @@
 
 In the **execution phase** all that needs to be done by the final user is to run it using Python, which can be done from the command line (e.g. `python3 supergame.pyz`) or by doing double click from the file explorer in those systems that relate the `.pyz` extension to Python (e.g. Windows).
 
 In this execution phase, the *unpacker* script put by PyEmpaq inside the packed file will be run, running the following steps:
 
 - check if the needed setup exists from a previous run; if yes, it will just run the payload project with almost no extra work; otherwise...
 
-- create a directory in the user data dir, and expand the `.pyz` file there
+- create a directory in the user data dir (or the indicated one, see below), and expand the `.pyz` file there
 
 - create a virtualenv in that new directory, and install all the payload's project dependencies
 
 - run the payload's project inside that virtualenv
 
 The verification that the unpacker does to see if has a reusable setup from the past is based on the `.pyz` timestamp; if it changed (a new file was distributed), a new setup will be created and used.
 
+The environment variable `PYEMPAQ_UNPACK_BASE_PATH` can be used to specify in which base directory PyEmpaq will unpack the different projects. If indicated, the path must exist and be a directory.
+
+PyEmpaq transparently returns the payload's exit code except when it must exit before the execution of the payload. In that case, it uses special codes equal or above 64, meaning:
+
+- `64`: `unpack-restrictions` are not met on the final user's system.
+- `65`: the indicated `PYEMPAQ_UNPACK_BASE_PATH` does not exist
+- `66`: the indicated `PYEMPAQ_UNPACK_BASE_PATH` is not a directory
+
 
 ## Command line options
 
 There is one mandatory parameter:
 
 - `source`: it needs to point the configuration file or to the directory where the configuration will be located (it will be searched by its default name `pyempaq.yaml`).
 
@@ -112,15 +120,15 @@
 - `pyempaq ~/repo/proj/config.yaml`
 
 You can control verbosity by adding these command line parameters to control logging levels:
 
 - `-v, --verbose` - Show detailed information, typically of interest only when diagnosing problems.
 - `-q, --quiet` - Only events of WARNING level and above will be tracked.
 
-All that said, there is an special option `-V, --version` that if used will just print the version and exit.
+All that said, there is an special option `-V, --version` (new in v0.3) that if used will just print the version and exit.
 
 > **Note**
 > In the **execution phase**, if you have an environment variable `PYEMPAQ_DEBUG=1` it will show the Pyempaq log lines during the execution.
 
 
 ## The configuration file
 
@@ -136,27 +144,27 @@
 
     - `script` [†]: the filepath of the python script to run; when unpacking PyEmpaq will do `python3 SCRIPT`.
 
     - `module` [†]: the name of the module to invoke; when unpacking PyEmpaq will do `python3 -m MODULE`.
 
     - `entrypoint` [†]: freeform, as a list of strings; when unpacking PyEmpaq will only insert the proper python3 at the beginning: `python3 STR1 STR2 ...`.
 
-    - `default-args` [optional]: the default arguments to be passed to the script/module/entrypoint (if not overriden when the distributed `.pyz` is executed).
+    - `default-args` [optional]: the default arguments to be passed to the script/module/entrypoint (if not overridden when the distributed `.pyz` is executed).
 
 - `requirements` [optional]: a list of filepaths pointing to the requirement files with pip-installable dependencies.
 
 - `dependencies` [optional]: a list of strings to directly specify packages to be installed by `pip` without needing to have a requirement file.
 
-- `include` [optional]: a list of strings, each one specifying a pattern to decide what files and directories to include in the pack (see below); if not included it defaults to `["./**"]` which means all the files and directories in the project.
+- `include` [optional, new in v0.3]: a list of strings, each one specifying a pattern to decide what files and directories to include in the pack (see below); if not included it defaults to `["./**"]` which means all the files and directories in the project.
 
-- `exclude` [optional]: a list of strings, each one specifying a pattern to decide what files and directories to exclude from the pack (see below).
+- `exclude` [optional, new in v0.3]: a list of strings, each one specifying a pattern to decide what files and directories to exclude from the pack (see below).
 
-- `unpack-restrictions` [optional]: a section to specify different restrictions to be verified/enforced during unpack.
+- `unpack-restrictions` [optional, new in v0.3]: a section to specify different restrictions to be verified/enforced during unpack.
 
-    - `minimum-python-version` [optional]: a string specifying the minimum version possible to run correctly.
+    - `minimum-python-version` [optional, new in v0.3]: a string specifying the minimum version possible to run correctly.
 
 All specified filepaths must exist inside the project and must be relative (to the project's base directory), with the exception of `basedir` itself which can be absolute or relative (to the configuration file location).
 
 Both `include` and `exclude` options use pattern matching according to the rules used by the Unix shell, using `*`, `?`, and character ranges expressed with `[]`. Also `**` will match any files and zero or more directories. For more information or subtleties check the [`glob.glob`](https://docs.python.org/dev/library/glob.html#glob.glob) documentation.
 
 Note that the final user may ignore/bypass any unpack restrictions using the `PYEMPAQ_IGNORE_RESTRICTIONS` environment variable with a value of comma-separated names of which restrictions to ignore.
```

### Comparing `pyempaq-0.3.1/README.md` & `pyempaq-0.4.0/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -65,22 +65,30 @@
 
 In the **execution phase** all that needs to be done by the final user is to run it using Python, which can be done from the command line (e.g. `python3 supergame.pyz`) or by doing double click from the file explorer in those systems that relate the `.pyz` extension to Python (e.g. Windows).
 
 In this execution phase, the *unpacker* script put by PyEmpaq inside the packed file will be run, running the following steps:
 
 - check if the needed setup exists from a previous run; if yes, it will just run the payload project with almost no extra work; otherwise...
 
-- create a directory in the user data dir, and expand the `.pyz` file there
+- create a directory in the user data dir (or the indicated one, see below), and expand the `.pyz` file there
 
 - create a virtualenv in that new directory, and install all the payload's project dependencies
 
 - run the payload's project inside that virtualenv
 
 The verification that the unpacker does to see if has a reusable setup from the past is based on the `.pyz` timestamp; if it changed (a new file was distributed), a new setup will be created and used.
 
+The environment variable `PYEMPAQ_UNPACK_BASE_PATH` can be used to specify in which base directory PyEmpaq will unpack the different projects. If indicated, the path must exist and be a directory.
+
+PyEmpaq transparently returns the payload's exit code except when it must exit before the execution of the payload. In that case, it uses special codes equal or above 64, meaning:
+
+- `64`: `unpack-restrictions` are not met on the final user's system.
+- `65`: the indicated `PYEMPAQ_UNPACK_BASE_PATH` does not exist
+- `66`: the indicated `PYEMPAQ_UNPACK_BASE_PATH` is not a directory
+
 
 ## Command line options
 
 There is one mandatory parameter:
 
 - `source`: it needs to point the configuration file or to the directory where the configuration will be located (it will be searched by its default name `pyempaq.yaml`).
 
@@ -93,15 +101,15 @@
 - `pyempaq ~/repo/proj/config.yaml`
 
 You can control verbosity by adding these command line parameters to control logging levels:
 
 - `-v, --verbose` - Show detailed information, typically of interest only when diagnosing problems.
 - `-q, --quiet` - Only events of WARNING level and above will be tracked.
 
-All that said, there is an special option `-V, --version` that if used will just print the version and exit.
+All that said, there is an special option `-V, --version` (new in v0.3) that if used will just print the version and exit.
 
 > **Note**
 > In the **execution phase**, if you have an environment variable `PYEMPAQ_DEBUG=1` it will show the Pyempaq log lines during the execution.
 
 
 ## The configuration file
 
@@ -117,27 +125,27 @@
 
     - `script` [†]: the filepath of the python script to run; when unpacking PyEmpaq will do `python3 SCRIPT`.
 
     - `module` [†]: the name of the module to invoke; when unpacking PyEmpaq will do `python3 -m MODULE`.
 
     - `entrypoint` [†]: freeform, as a list of strings; when unpacking PyEmpaq will only insert the proper python3 at the beginning: `python3 STR1 STR2 ...`.
 
-    - `default-args` [optional]: the default arguments to be passed to the script/module/entrypoint (if not overriden when the distributed `.pyz` is executed).
+    - `default-args` [optional]: the default arguments to be passed to the script/module/entrypoint (if not overridden when the distributed `.pyz` is executed).
 
 - `requirements` [optional]: a list of filepaths pointing to the requirement files with pip-installable dependencies.
 
 - `dependencies` [optional]: a list of strings to directly specify packages to be installed by `pip` without needing to have a requirement file.
 
-- `include` [optional]: a list of strings, each one specifying a pattern to decide what files and directories to include in the pack (see below); if not included it defaults to `["./**"]` which means all the files and directories in the project.
+- `include` [optional, new in v0.3]: a list of strings, each one specifying a pattern to decide what files and directories to include in the pack (see below); if not included it defaults to `["./**"]` which means all the files and directories in the project.
 
-- `exclude` [optional]: a list of strings, each one specifying a pattern to decide what files and directories to exclude from the pack (see below).
+- `exclude` [optional, new in v0.3]: a list of strings, each one specifying a pattern to decide what files and directories to exclude from the pack (see below).
 
-- `unpack-restrictions` [optional]: a section to specify different restrictions to be verified/enforced during unpack.
+- `unpack-restrictions` [optional, new in v0.3]: a section to specify different restrictions to be verified/enforced during unpack.
 
-    - `minimum-python-version` [optional]: a string specifying the minimum version possible to run correctly.
+    - `minimum-python-version` [optional, new in v0.3]: a string specifying the minimum version possible to run correctly.
 
 All specified filepaths must exist inside the project and must be relative (to the project's base directory), with the exception of `basedir` itself which can be absolute or relative (to the configuration file location).
 
 Both `include` and `exclude` options use pattern matching according to the rules used by the Unix shell, using `*`, `?`, and character ranges expressed with `[]`. Also `**` will match any files and zero or more directories. For more information or subtleties check the [`glob.glob`](https://docs.python.org/dev/library/glob.html#glob.glob) documentation.
 
 Note that the final user may ignore/bypass any unpack restrictions using the `PYEMPAQ_IGNORE_RESTRICTIONS` environment variable with a value of comma-separated names of which restrictions to ignore.
```

### Comparing `pyempaq-0.3.1/pyempaq/common.py` & `pyempaq-0.4.0/pyempaq/common.py`

 * *Files 7% similar despite different names*

```diff
@@ -11,14 +11,18 @@
 logger = logging.getLogger('logger')
 
 
 class ExecutionError(Exception):
     """The subprocess didn't finish ok."""
 
 
+class PackError(Exception):
+    """An error occurred while packing the project."""
+
+
 def find_venv_bin(basedir, exec_base):
     """Heuristics to find the pip executable in different platforms."""
     bin_dir = basedir / "bin"
     if bin_dir.exists():
         # linux-like environment
         return bin_dir / exec_base
```

### Comparing `pyempaq-0.3.1/pyempaq/config_manager.py` & `pyempaq-0.4.0/pyempaq/config_manager.py`

 * *Files identical despite different names*

### Comparing `pyempaq-0.3.1/pyempaq/main.py` & `pyempaq-0.4.0/pyempaq/main.py`

 * *Files 6% similar despite different names*

```diff
@@ -17,28 +17,28 @@
 import venv
 import zipapp
 from collections import namedtuple
 from pathlib import Path
 from typing import List
 
 from pyempaq import __version__
-from pyempaq.common import find_venv_bin, logged_exec, ExecutionError
+from pyempaq.common import find_venv_bin, logged_exec, ExecutionError, PackError
 from pyempaq.config_manager import load_config, ConfigError, Config
 
 
 # setup logging
 logging.basicConfig(
     format='%(asctime)s.%(msecs)03d %(levelname)-5s %(message)s', datefmt='%H:%M:%S')
 logger = logging.getLogger(__name__)
 
 # collected arguments
 Args = namedtuple("Args", "project_name basedir entrypoint requirement_files")
 
 # dependencies needed for the unpacker to run ok
-UNPACKER_DEPS = ["appdirs", "packaging"]
+UNPACKER_DEPS = ["packaging", "platformdirs"]
 
 
 def get_pip():
     """Ensure an usable version of `pip`."""
     useful_pip = Path("pip3")
     # try to see if it's already installed
     try:
@@ -191,14 +191,26 @@
     tmpdir = Path(tempfile.mkdtemp())
     logger.debug("Working in temp dir %r", str(tmpdir))
 
     # copy all the project content inside "orig" in temp dir
     origdir = tmpdir / "orig"
     copy_project(config.basedir, origdir, config.include, config.exclude)
 
+    # ensure all requirements are included by users
+    missing_requirements = []
+    for path in config.requirements:
+        if not (origdir / path).exists():
+            missing_requirements.append(str(path))
+
+    if missing_requirements:
+        raise PackError(
+            f"The indicated requirements {missing_requirements} are not included "
+            "along the packed files; ensure to include them explicitly in the config."
+        )
+
     # copy the common module
     pyempaq_dir = tmpdir / "pyempaq"
     pyempaq_dir.mkdir()
     common_src = project_root / "common.py"
     common_final_src = tmpdir / "pyempaq" / "common.py"
     shutil.copy(common_src, common_final_src)
 
@@ -256,8 +268,16 @@
         logger.info("Parsing configuration in %r", str(args.source))
         config = load_config(args.source)
     except ConfigError as err:
         logger.error(err)
         for err in err.errors:
             logger.error(err)
         exit(1)
-    pack(config)
+
+    try:
+        pack(config)
+    except PackError as exc:
+        logger.error("Pack error: %s", exc)
+        exit(2)
+    except Exception as exc:
+        logger.error("Unknown internal error: %r", exc)
+        exit(3)
```

### Comparing `pyempaq-0.3.1/pyempaq.egg-info/PKG-INFO` & `pyempaq-0.4.0/pyempaq.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyempaq
-Version: 0.3.1
+Version: 0.4.0
 Summary: A Python packer to run anywhwere any project with any virtualenv dependencies.
 Home-page: https://github.com/facundobatista/pyempaq
 Author: Facundo Batista
 Author-email: facundo@taniquetil.com.ar
 License: GPL-v3
 Platform: UNKNOWN
 Classifier: Environment :: Console
@@ -84,22 +84,30 @@
 
 In the **execution phase** all that needs to be done by the final user is to run it using Python, which can be done from the command line (e.g. `python3 supergame.pyz`) or by doing double click from the file explorer in those systems that relate the `.pyz` extension to Python (e.g. Windows).
 
 In this execution phase, the *unpacker* script put by PyEmpaq inside the packed file will be run, running the following steps:
 
 - check if the needed setup exists from a previous run; if yes, it will just run the payload project with almost no extra work; otherwise...
 
-- create a directory in the user data dir, and expand the `.pyz` file there
+- create a directory in the user data dir (or the indicated one, see below), and expand the `.pyz` file there
 
 - create a virtualenv in that new directory, and install all the payload's project dependencies
 
 - run the payload's project inside that virtualenv
 
 The verification that the unpacker does to see if has a reusable setup from the past is based on the `.pyz` timestamp; if it changed (a new file was distributed), a new setup will be created and used.
 
+The environment variable `PYEMPAQ_UNPACK_BASE_PATH` can be used to specify in which base directory PyEmpaq will unpack the different projects. If indicated, the path must exist and be a directory.
+
+PyEmpaq transparently returns the payload's exit code except when it must exit before the execution of the payload. In that case, it uses special codes equal or above 64, meaning:
+
+- `64`: `unpack-restrictions` are not met on the final user's system.
+- `65`: the indicated `PYEMPAQ_UNPACK_BASE_PATH` does not exist
+- `66`: the indicated `PYEMPAQ_UNPACK_BASE_PATH` is not a directory
+
 
 ## Command line options
 
 There is one mandatory parameter:
 
 - `source`: it needs to point the configuration file or to the directory where the configuration will be located (it will be searched by its default name `pyempaq.yaml`).
 
@@ -112,15 +120,15 @@
 - `pyempaq ~/repo/proj/config.yaml`
 
 You can control verbosity by adding these command line parameters to control logging levels:
 
 - `-v, --verbose` - Show detailed information, typically of interest only when diagnosing problems.
 - `-q, --quiet` - Only events of WARNING level and above will be tracked.
 
-All that said, there is an special option `-V, --version` that if used will just print the version and exit.
+All that said, there is an special option `-V, --version` (new in v0.3) that if used will just print the version and exit.
 
 > **Note**
 > In the **execution phase**, if you have an environment variable `PYEMPAQ_DEBUG=1` it will show the Pyempaq log lines during the execution.
 
 
 ## The configuration file
 
@@ -136,27 +144,27 @@
 
     - `script` [†]: the filepath of the python script to run; when unpacking PyEmpaq will do `python3 SCRIPT`.
 
     - `module` [†]: the name of the module to invoke; when unpacking PyEmpaq will do `python3 -m MODULE`.
 
     - `entrypoint` [†]: freeform, as a list of strings; when unpacking PyEmpaq will only insert the proper python3 at the beginning: `python3 STR1 STR2 ...`.
 
-    - `default-args` [optional]: the default arguments to be passed to the script/module/entrypoint (if not overriden when the distributed `.pyz` is executed).
+    - `default-args` [optional]: the default arguments to be passed to the script/module/entrypoint (if not overridden when the distributed `.pyz` is executed).
 
 - `requirements` [optional]: a list of filepaths pointing to the requirement files with pip-installable dependencies.
 
 - `dependencies` [optional]: a list of strings to directly specify packages to be installed by `pip` without needing to have a requirement file.
 
-- `include` [optional]: a list of strings, each one specifying a pattern to decide what files and directories to include in the pack (see below); if not included it defaults to `["./**"]` which means all the files and directories in the project.
+- `include` [optional, new in v0.3]: a list of strings, each one specifying a pattern to decide what files and directories to include in the pack (see below); if not included it defaults to `["./**"]` which means all the files and directories in the project.
 
-- `exclude` [optional]: a list of strings, each one specifying a pattern to decide what files and directories to exclude from the pack (see below).
+- `exclude` [optional, new in v0.3]: a list of strings, each one specifying a pattern to decide what files and directories to exclude from the pack (see below).
 
-- `unpack-restrictions` [optional]: a section to specify different restrictions to be verified/enforced during unpack.
+- `unpack-restrictions` [optional, new in v0.3]: a section to specify different restrictions to be verified/enforced during unpack.
 
-    - `minimum-python-version` [optional]: a string specifying the minimum version possible to run correctly.
+    - `minimum-python-version` [optional, new in v0.3]: a string specifying the minimum version possible to run correctly.
 
 All specified filepaths must exist inside the project and must be relative (to the project's base directory), with the exception of `basedir` itself which can be absolute or relative (to the configuration file location).
 
 Both `include` and `exclude` options use pattern matching according to the rules used by the Unix shell, using `*`, `?`, and character ranges expressed with `[]`. Also `**` will match any files and zero or more directories. For more information or subtleties check the [`glob.glob`](https://docs.python.org/dev/library/glob.html#glob.glob) documentation.
 
 Note that the final user may ignore/bypass any unpack restrictions using the `PYEMPAQ_IGNORE_RESTRICTIONS` environment variable with a value of comma-separated names of which restrictions to ignore.
```

### Comparing `pyempaq-0.3.1/setup.py` & `pyempaq-0.4.0/setup.py`

 * *Files identical despite different names*

