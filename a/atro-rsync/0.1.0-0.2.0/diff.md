# Comparing `tmp/atro_rsync-0.1.0.tar.gz` & `tmp/atro_rsync-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "atro_rsync-0.1.0.tar", max compression
+gzip compressed data, was "atro_rsync-0.2.0.tar", max compression
```

## Comparing `atro_rsync-0.1.0.tar` & `atro_rsync-0.2.0.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0        0 2023-06-17 12:33:58.233092 atro_rsync-0.1.0/README.md
--rw-r--r--   0        0        0     1426 2023-07-16 21:34:26.897673 atro_rsync-0.1.0/atro_rsync/__init__.py
--rw-r--r--   0        0        0       72 2023-06-24 20:11:31.873997 atro_rsync-0.1.0/atro_rsync/helpers.py
--rw-r--r--   0        0        0      328 2023-07-17 21:44:08.578070 atro_rsync-0.1.0/pyproject.toml
--rw-r--r--   0        0        0      332 1970-01-01 00:00:00.000000 atro_rsync-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-06-17 12:33:58.233092 atro_rsync-0.2.0/README.md
+-rw-r--r--   0        0        0     1387 2023-07-23 19:50:33.224264 atro_rsync-0.2.0/atro_rsync/__init__.py
+-rw-r--r--   0        0        0       72 2023-06-24 20:11:31.873997 atro_rsync-0.2.0/atro_rsync/helpers.py
+-rw-r--r--   0        0        0      307 2023-07-23 19:51:07.238294 atro_rsync-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0      289 1970-01-01 00:00:00.000000 atro_rsync-0.2.0/PKG-INFO
```

### Comparing `atro_rsync-0.1.0/atro_rsync/__init__.py` & `atro_rsync-0.2.0/atro_rsync/__init__.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,40 +1,37 @@
 import os
 import subprocess
 from pathlib import Path
-
-from atro_pylog import set_logger
-
 from atro_rsync.helpers import wrap_in_double_quotes
+import logging
 
-
-def rsync(source: Path, destination: Path, options: list[str] = [], exclusions: list[str] = [], cwd=os.getcwd(), logger=set_logger()):
+def rsync(source: Path, destination: Path, options: list[str] = [], exclusions: list[str] = [], cwd=os.getcwd()):
     log_msg = f"Running rsync from {source.as_posix()} to {destination.as_posix()}"
     if len(options) == 1:
         log_msg += f" with option {options[0]}"
     elif len(options) > 1:
         log_msg += f" with options {', '.join(options)}"
     exclusion_command = []
     if len(exclusions) > 0:
         if len(exclusions) == 1:
             log_msg += f" excluding {exclusions[0]}"
         else:
             log_msg += f" excluding {', '.join(exclusions)}"
 
         exclusion_command = [f'--exclude="{exclusion}"' for exclusion in exclusions]
 
-    logger.info(log_msg)
+    logging.info(log_msg)
     command_list = [
         "rsync",
         *options,
         wrap_in_double_quotes(str(source) + "/"),
         wrap_in_double_quotes(str(destination) + "/"),
         *exclusion_command,
     ]
     command = " ".join(command_list)
-    logger.info("Command ran: '" + command + "'")
+    logging.info("Command ran: '" + command + "'")
     output = subprocess.run(command, cwd=cwd, shell=True, capture_output=True)
-    logger.debug("Rsync output: " + output.stdout.decode())
+    logging.debug("Rsync output: " + output.stdout.decode())
     if output.stderr:
-        logger.error("Rsync error: " + output.stderr.decode())
+        logging.error("Rsync error: " + output.stderr.decode())
     if output.returncode != 0:
         raise Exception("Rsync failed")
```

