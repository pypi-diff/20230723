# Comparing `tmp/kuki-0.9.4.tar.gz` & `tmp/kuki-0.9.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "kuki-0.9.4.tar", last modified: Sat Jul 22 11:33:48 2023, max compression
+gzip compressed data, was "kuki-0.9.5.tar", last modified: Sun Jul 23 14:42:25 2023, max compression
```

## Comparing `kuki-0.9.4.tar` & `kuki-0.9.5.tar`

### file list

```diff
@@ -1,37 +1,37 @@
-drwxr-xr-x   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-22 11:33:48.663136 kuki-0.9.4/
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)    11357 2023-05-07 13:15:07.000000 kuki-0.9.4/LICENSE
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)    12044 2023-07-22 11:33:48.664136 kuki-0.9.4/PKG-INFO
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)      459 2023-07-20 14:47:33.000000 kuki-0.9.4/README.md
-drwxr-xr-x   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-22 11:33:48.661136 kuki-0.9.4/kuki/
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        0 2023-05-07 13:14:38.000000 kuki-0.9.4/kuki/__init__.py
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1176 2023-05-20 06:39:32.000000 kuki-0.9.4/kuki/config_util.py
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1579 2023-07-19 15:39:03.000000 kuki-0.9.4/kuki/kest.py
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1994 2023-07-19 16:18:20.000000 kuki-0.9.4/kuki/ktrl.py
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     4652 2023-07-22 06:51:24.000000 kuki-0.9.4/kuki/ktrl_util.py
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     4577 2023-07-22 07:28:15.000000 kuki-0.9.4/kuki/kuki.py
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     4031 2023-07-22 05:33:03.000000 kuki-0.9.4/kuki/package_util.py
-drwxr-xr-x   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-22 11:33:48.663136 kuki-0.9.4/kuki/q/
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-03 12:47:22.000000 kuki-0.9.4/kuki/q/__init__.py
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     4535 2023-07-03 16:51:49.000000 kuki-0.9.4/kuki/q/cli.q
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     7819 2023-07-15 09:03:13.000000 kuki-0.9.4/kuki/q/kest.q
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)      219 2023-07-19 16:35:57.000000 kuki-0.9.4/kuki/q/ktrl.q
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1898 2023-07-21 09:56:43.000000 kuki-0.9.4/kuki/q/kuki.q
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     2187 2023-07-20 15:49:50.000000 kuki-0.9.4/kuki/q/log.q
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1435 2023-07-15 14:20:22.000000 kuki-0.9.4/kuki/q/path.q
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)    18538 2023-07-22 11:32:34.000000 kuki-0.9.4/kuki/registry_util.py
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     3704 2023-07-19 16:32:47.000000 kuki-0.9.4/kuki/util.py
-drwxr-xr-x   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-22 11:33:48.662136 kuki-0.9.4/kuki.egg-info/
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)    12044 2023-07-22 11:33:48.000000 kuki-0.9.4/kuki.egg-info/PKG-INFO
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)      554 2023-07-22 11:33:48.000000 kuki-0.9.4/kuki.egg-info/SOURCES.txt
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        1 2023-07-22 11:33:48.000000 kuki-0.9.4/kuki.egg-info/dependency_links.txt
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)       84 2023-07-22 11:33:48.000000 kuki-0.9.4/kuki.egg-info/entry_points.txt
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        1 2023-07-22 11:33:48.000000 kuki-0.9.4/kuki.egg-info/not-zip-safe
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)       17 2023-07-22 11:33:48.000000 kuki-0.9.4/kuki.egg-info/requires.txt
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)       10 2023-07-22 11:33:48.000000 kuki-0.9.4/kuki.egg-info/top_level.txt
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)      470 2023-07-22 11:33:48.664136 kuki-0.9.4/setup.cfg
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)      315 2023-07-03 15:40:17.000000 kuki-0.9.4/setup.py
-drwxr-xr-x   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-22 11:33:48.663136 kuki-0.9.4/test/
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        0 2023-05-07 13:15:07.000000 kuki-0.9.4/test/__init__.py
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        0 2023-05-07 13:15:07.000000 kuki-0.9.4/test/conftest.py
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1423 2023-07-19 15:39:03.000000 kuki-0.9.4/test/test_kest.py
--rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)    15810 2023-07-21 15:26:05.000000 kuki-0.9.4/test/test_kuki.py
+drwxr-xr-x   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-23 14:42:25.191703 kuki-0.9.5/
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)    11357 2023-05-07 13:15:07.000000 kuki-0.9.5/LICENSE
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)    12044 2023-07-23 14:42:25.191703 kuki-0.9.5/PKG-INFO
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)      459 2023-07-20 14:47:33.000000 kuki-0.9.5/README.md
+drwxr-xr-x   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-23 14:42:25.188703 kuki-0.9.5/kuki/
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        0 2023-05-07 13:14:38.000000 kuki-0.9.5/kuki/__init__.py
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1176 2023-05-20 06:39:32.000000 kuki-0.9.5/kuki/config_util.py
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1375 2023-07-23 05:45:31.000000 kuki-0.9.5/kuki/kest.py
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1994 2023-07-19 16:18:20.000000 kuki-0.9.5/kuki/ktrl.py
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     4652 2023-07-22 06:51:24.000000 kuki-0.9.5/kuki/ktrl_util.py
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     4577 2023-07-22 07:28:15.000000 kuki-0.9.5/kuki/kuki.py
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     4031 2023-07-22 05:33:03.000000 kuki-0.9.5/kuki/package_util.py
+drwxr-xr-x   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-23 14:42:25.190703 kuki-0.9.5/kuki/q/
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-03 12:47:22.000000 kuki-0.9.5/kuki/q/__init__.py
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     4535 2023-07-03 16:51:49.000000 kuki-0.9.5/kuki/q/cli.q
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     7819 2023-07-15 09:03:13.000000 kuki-0.9.5/kuki/q/kest.q
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)      219 2023-07-19 16:35:57.000000 kuki-0.9.5/kuki/q/ktrl.q
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1913 2023-07-22 16:08:18.000000 kuki-0.9.5/kuki/q/kuki.q
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     2187 2023-07-20 15:49:50.000000 kuki-0.9.5/kuki/q/log.q
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1435 2023-07-15 14:20:22.000000 kuki-0.9.5/kuki/q/path.q
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)    18538 2023-07-22 11:32:34.000000 kuki-0.9.5/kuki/registry_util.py
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     3704 2023-07-19 16:32:47.000000 kuki-0.9.5/kuki/util.py
+drwxr-xr-x   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-23 14:42:25.189703 kuki-0.9.5/kuki.egg-info/
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)    12044 2023-07-23 14:42:25.000000 kuki-0.9.5/kuki.egg-info/PKG-INFO
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)      554 2023-07-23 14:42:25.000000 kuki-0.9.5/kuki.egg-info/SOURCES.txt
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        1 2023-07-23 14:42:25.000000 kuki-0.9.5/kuki.egg-info/dependency_links.txt
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)       84 2023-07-23 14:42:25.000000 kuki-0.9.5/kuki.egg-info/entry_points.txt
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        1 2023-07-23 14:42:25.000000 kuki-0.9.5/kuki.egg-info/not-zip-safe
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)       15 2023-07-23 14:42:25.000000 kuki-0.9.5/kuki.egg-info/requires.txt
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)       10 2023-07-23 14:42:25.000000 kuki-0.9.5/kuki.egg-info/top_level.txt
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)      468 2023-07-23 14:42:25.191703 kuki-0.9.5/setup.cfg
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)      315 2023-07-03 15:40:17.000000 kuki-0.9.5/setup.py
+drwxr-xr-x   0 jshinonome  (1000) jshinonome  (1000)        0 2023-07-23 14:42:25.191703 kuki-0.9.5/test/
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        0 2023-05-07 13:15:07.000000 kuki-0.9.5/test/__init__.py
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)        0 2023-05-07 13:15:07.000000 kuki-0.9.5/test/conftest.py
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)     1423 2023-07-19 15:39:03.000000 kuki-0.9.5/test/test_kest.py
+-rw-r--r--   0 jshinonome  (1000) jshinonome  (1000)    15810 2023-07-21 15:26:05.000000 kuki-0.9.5/test/test_kuki.py
```

### Comparing `kuki-0.9.4/LICENSE` & `kuki-0.9.5/LICENSE`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/PKG-INFO` & `kuki-0.9.5/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: kuki
-Version: 0.9.4
+Version: 0.9.5
 Summary: K Ultimate pacKage Installer
 Author: Jo Shinonome
 License: Apache-2.0
 Keywords: q,k
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

### Comparing `kuki-0.9.4/kuki/config_util.py` & `kuki-0.9.5/kuki/config_util.py`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/kuki/kest.py` & `kuki-0.9.5/kuki/kest.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,32 +1,26 @@
 import json
 import logging
 import subprocess
 import sys
 from pathlib import Path
 
-from .util import PROCESS_DEFAULT, PROFILE_DEFAULT, generate_cmd, generate_process_options
+from .util import PROFILE_DEFAULT, generate_cmd, generate_process_options
 
 FORMAT = "%(asctime)s %(levelname)s: %(message)s"
 DATE_FORMAT = "%Y-%m-%d %H:%M:%S"
 
 logging.basicConfig(level=logging.INFO, format=FORMAT, datefmt=DATE_FORMAT)
 
 logger = logging.getLogger()
 
 kest_path = Path("kest.json")
 
-kest_process_default = PROCESS_DEFAULT.copy()
-
-kest_process_default.pop("blocked")
-kest_process_default.pop("replicate")
-kest_process_default.pop("disable_system_cmd")
-
 KEST_DEFAULT = {
-    "process": kest_process_default,
+    "process": {},
     "profile": PROFILE_DEFAULT,
 }
 
 
 def kest(args):
     # use kest.json if available
     if "-init" in args:
```

### Comparing `kuki-0.9.4/kuki/ktrl.py` & `kuki-0.9.5/kuki/ktrl.py`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/kuki/ktrl_util.py` & `kuki-0.9.5/kuki/ktrl_util.py`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/kuki/kuki.py` & `kuki-0.9.5/kuki/kuki.py`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/kuki/package_util.py` & `kuki-0.9.5/kuki/package_util.py`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/kuki/q/cli.q` & `kuki-0.9.5/kuki/q/cli.q`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/kuki/q/kest.q` & `kuki-0.9.5/kuki/q/kest.q`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/kuki/q/kuki.q` & `kuki-0.9.5/kuki/q/kuki.q`

 * *Files 2% similar despite different names*

```diff
@@ -48,15 +48,15 @@
 // local import - import {"./[folder/]/module"}
 // module doesn't include .q
 import:{[moduleFunc]
   if[100h<>type moduleFunc;'"requires format {\"module\"} for import"];
   module: moduleFunc[];
   path: first -3#value moduleFunc;
   path: 1_string first ` vs hsym `$path;
-  $[module like "./*"; .kuki.importLocal[path;module];.kuki.importGlobal[module]]
+  $[any module like/: ("./*";"../*"); .kuki.importLocal[path;module];.kuki.importGlobal[module]]
  };
 
 import {"./log"};
 import {"./cli"};
 import {"./path"};
 
 import {"./",first .Q.opt[.z.x][`kScriptType]};
```

### Comparing `kuki-0.9.4/kuki/q/log.q` & `kuki-0.9.5/kuki/q/log.q`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/kuki/q/path.q` & `kuki-0.9.5/kuki/q/path.q`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/kuki/registry_util.py` & `kuki-0.9.5/kuki/registry_util.py`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/kuki/util.py` & `kuki-0.9.5/kuki/util.py`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/kuki.egg-info/PKG-INFO` & `kuki-0.9.5/kuki.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: kuki
-Version: 0.9.4
+Version: 0.9.5
 Summary: K Ultimate pacKage Installer
 Author: Jo Shinonome
 License: Apache-2.0
 Keywords: q,k
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

### Comparing `kuki-0.9.4/kuki.egg-info/SOURCES.txt` & `kuki-0.9.5/kuki.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/test/test_kest.py` & `kuki-0.9.5/test/test_kest.py`

 * *Files identical despite different names*

### Comparing `kuki-0.9.4/test/test_kuki.py` & `kuki-0.9.5/test/test_kuki.py`

 * *Files identical despite different names*

