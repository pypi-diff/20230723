# Comparing `tmp/hydra-callbacks-0.2.0.tar.gz` & `tmp/hydra-callbacks-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hydra-callbacks-0.2.0.tar", last modified: Thu Apr  6 11:22:50 2023, max compression
+gzip compressed data, was "hydra-callbacks-0.3.0.tar", last modified: Sun Jul 23 12:49:06 2023, max compression
```

## Comparing `hydra-callbacks-0.2.0.tar` & `hydra-callbacks-0.3.0.tar`

### file list

```diff
@@ -1,39 +1,39 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 11:22:50.670799 hydra-callbacks-0.2.0/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 11:22:50.666799 hydra-callbacks-0.2.0/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 11:22:50.666799 hydra-callbacks-0.2.0/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     3130 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/.github/workflows/master-cd.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1221 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/.github/workflows/tags-release.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1270 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/.github/workflows/test-ci.yml
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1077 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     3203 2023-04-06 11:22:50.670799 hydra-callbacks-0.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2336 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     2833 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-06 11:22:50.670799 hydra-callbacks-0.2.0/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 11:22:50.666799 hydra-callbacks-0.2.0/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 11:22:50.666799 hydra-callbacks-0.2.0/src/hydra_callbacks/
--rw-r--r--   0 runner    (1001) docker     (123)      871 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/src/hydra_callbacks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      160 2023-04-06 11:22:50.000000 hydra-callbacks-0.2.0/src/hydra_callbacks/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)     9206 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/src/hydra_callbacks/callbacks.py
--rw-r--r--   0 runner    (1001) docker     (123)     1921 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/src/hydra_callbacks/logger.py
--rw-r--r--   0 runner    (1001) docker     (123)     4715 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/src/hydra_callbacks/monitor.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 11:22:50.670799 hydra-callbacks-0.2.0/src/hydra_callbacks.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3203 2023-04-06 11:22:50.000000 hydra-callbacks-0.2.0/src/hydra_callbacks.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      873 2023-04-06 11:22:50.000000 hydra-callbacks-0.2.0/src/hydra_callbacks.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-06 11:22:50.000000 hydra-callbacks-0.2.0/src/hydra_callbacks.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      117 2023-04-06 11:22:50.000000 hydra-callbacks-0.2.0/src/hydra_callbacks.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-04-06 11:22:50.000000 hydra-callbacks-0.2.0/src/hydra_callbacks.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 11:22:50.670799 hydra-callbacks-0.2.0/tests/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-06 11:22:50.670799 hydra-callbacks-0.2.0/tests/test_app/
--rw-r--r--   0 runner    (1001) docker     (123)       97 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_app/config.yaml
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_app/dummy.txt
--rw-r--r--   0 runner    (1001) docker     (123)      295 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_app/dummy_app.py
--rw-r--r--   0 runner    (1001) docker     (123)      581 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_app/gather_app.py
--rw-r--r--   0 runner    (1001) docker     (123)      134 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_app/gather_app_conf.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      103 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_app/git_callback.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      164 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_app/latest_callback.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      514 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_app/perf_app.py
--rw-r--r--   0 runner    (1001) docker     (123)      147 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_app/ressource_monitor.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      119 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_app/runtime_perf.yaml
--rw-r--r--   0 runner    (1001) docker     (123)    11621 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_callbacks.py
--rw-r--r--   0 runner    (1001) docker     (123)      617 2023-04-06 11:21:46.000000 hydra-callbacks-0.2.0/tests/test_perflogger.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:49:06.777284 hydra-callbacks-0.3.0/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:49:06.773284 hydra-callbacks-0.3.0/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:49:06.773284 hydra-callbacks-0.3.0/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     3130 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/.github/workflows/master-cd.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1221 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/.github/workflows/tags-release.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1270 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/.github/workflows/test-ci.yml
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1077 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3945 2023-07-23 12:49:06.777284 hydra-callbacks-0.3.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3078 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     2833 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 12:49:06.777284 hydra-callbacks-0.3.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:49:06.773284 hydra-callbacks-0.3.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:49:06.777284 hydra-callbacks-0.3.0/src/hydra_callbacks/
+-rw-r--r--   0 runner    (1001) docker     (123)      869 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/src/hydra_callbacks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-07-23 12:49:06.000000 hydra-callbacks-0.3.0/src/hydra_callbacks/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10437 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/src/hydra_callbacks/callbacks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1921 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/src/hydra_callbacks/logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4714 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/src/hydra_callbacks/monitor.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:49:06.777284 hydra-callbacks-0.3.0/src/hydra_callbacks.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3945 2023-07-23 12:49:06.000000 hydra-callbacks-0.3.0/src/hydra_callbacks.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      872 2023-07-23 12:49:06.000000 hydra-callbacks-0.3.0/src/hydra_callbacks.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 12:49:06.000000 hydra-callbacks-0.3.0/src/hydra_callbacks.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      117 2023-07-23 12:49:06.000000 hydra-callbacks-0.3.0/src/hydra_callbacks.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-07-23 12:49:06.000000 hydra-callbacks-0.3.0/src/hydra_callbacks.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:49:06.777284 hydra-callbacks-0.3.0/tests/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:49:06.777284 hydra-callbacks-0.3.0/tests/test_app/
+-rw-r--r--   0 runner    (1001) docker     (123)       97 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_app/config.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_app/dummy.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      295 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_app/dummy_app.py
+-rw-r--r--   0 runner    (1001) docker     (123)      581 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_app/gather_app.py
+-rw-r--r--   0 runner    (1001) docker     (123)      134 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_app/gather_app_conf.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      103 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_app/git_callback.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      164 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_app/latest_callback.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      514 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_app/perf_app.py
+-rw-r--r--   0 runner    (1001) docker     (123)      145 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_app/resource_monitor.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      119 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_app/runtime_perf.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)    11727 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_callbacks.py
+-rw-r--r--   0 runner    (1001) docker     (123)      617 2023-07-23 12:48:06.000000 hydra-callbacks-0.3.0/tests/test_perflogger.py
```

### Comparing `hydra-callbacks-0.2.0/.github/workflows/master-cd.yml` & `hydra-callbacks-0.3.0/.github/workflows/master-cd.yml`

 * *Files identical despite different names*

### Comparing `hydra-callbacks-0.2.0/.github/workflows/tags-release.yml` & `hydra-callbacks-0.3.0/.github/workflows/tags-release.yml`

 * *Files identical despite different names*

### Comparing `hydra-callbacks-0.2.0/.github/workflows/test-ci.yml` & `hydra-callbacks-0.3.0/.github/workflows/test-ci.yml`

 * *Files identical despite different names*

### Comparing `hydra-callbacks-0.2.0/LICENSE` & `hydra-callbacks-0.3.0/LICENSE`

 * *Files identical despite different names*

### Comparing `hydra-callbacks-0.2.0/PKG-INFO` & `hydra-callbacks-0.3.0/PKG-INFO`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hydra-callbacks
-Version: 0.2.0
+Version: 0.3.0
 Summary: A collection of usefull hydra callbacks for hydra configuration
 Author-email: Pierre-Antoine Comby <pierre-antoine.comby@cea.fr>
 Project-URL: Homepage, https://github.com/paquiteau/hydra-callbacks
 Project-URL: Bug Reports, https://github.com/paquiteau/hydra-callbacks/issues
 Project-URL: Sources, https://github.com/paquiteau/hydra-callbacks
 Keywords: hydra,configuration,callback
 Classifier: Development Status :: 3 - Alpha
@@ -23,15 +23,15 @@
 
 
 [![style](https://img.shields.io/badge/style-black-black)](https://github.com/psf/black)
 [![framework](https://img.shields.io/badge/framework-hydra-blue)](https://hydra.cc)
 [![codecov](https://codecov.io/gh/paquiteau/hydra-callbacks/branch/master/graph/badge.svg?token=NEV7SY24YB)](https://codecov.io/gh/paquiteau/hydra-callbacks)
 [![CD](https://github.com/paquiteau/hydra-callbacks/actions/workflows/master-cd.yml/badge.svg)](https://github.com/paquiteau/hydra-callbacks/actions/workflows/master-cd.yml)
 [![CI](https://github.com/paquiteau/hydra-callbacks/actions/workflows/test-ci.yml/badge.svg)](https://github.com/paquiteau/hydra-callbacks/actions/workflows/test-ci.yml)
-[![Release](https://github.com/paquiteau/hydra-callbacks/releases/latest)](https://img.shields.io/github/v/release/paquiteau/hydra-callbacks)
+[![Release](https://img.shields.io/github/v/release/paquiteau/hydra-callbacks)](https://github.com/paquiteau/hydra-callbacks/releases/latest)
 
 A collection of usefulls callbacks for the [https://hydra.cc/](hydra) configuration framework.
 
 
 ## Installation 
 ``` shell 
 pip install hydra-callbacks
@@ -40,36 +40,56 @@
 Development version 
 ``` shell
 pip install git+https://github.com/paquiteau/hydra-callbacks
 ```
 
 ## Usage 
 
-In your hydra root config file add the following: 
+In your hydra root config file add the following, or analoguous:
 
 ``` yaml
-hydra: 
-  # ... 
-  callbacks: 
-    git_info:
-      _target_: hydra_callbacks.GitInfo 
+hydra:
+  callbacks:
+    git_infos:
+      _target_: hydra_callbacks.GitInfo
       clean: true
-    latest_link:
+    latest_run:
       _target_: hydra_callbacks.LatestRunLink
+    resource_monitor:
+      _target_: hydra_callbacks.ResourceMonitor
+      sample_interval: 0.5
+    runtime_perf:
+      _target_: hydra_callbacks.RuntimePerformance      
 ```
 
+This will enrich your script output with: 
+
+```console
+paquiteau@laptop$ python my_app.py
+[hydra] Git sha: 844b9ca1a74d8307ef5331351897cebb18f71b88, dirty: False
+
+## All your app log and outputs ##
+
+[hydra][INFO] - Total runtime: 0.51 seconds
+[hydra][INFO] - Writing monitoring data to [...]/outputs/2023-04-06/16-02-46/resource_monitoring.csv
+[hydra][INFO] - Latest run is at: [...]/outputs/latest
+```
+
+
+Detailled configuration for each callback is available in the `tests/test_app/` folder.
 
 ## Available Callbacks 
 
-| Name               | Action                                     |
-|:-------------------|:-------------------------------------------|
-| GitInfo            | Check status of Repository                 |
-| LatestRunLink      | Get a link to the latest run               |
-| MultiRunGatherer   | Gather results json file in a single table |
-| RuntimePerformance | Get Execution time for each run            |
+| Name               | Action                                             |
+|:-------------------|:---------------------------------------------------|
+| GitInfo            | Check status of Repository                         |
+| LatestRunLink      | Get a link to the latest run                       |
+| MultiRunGatherer   | Gather results json file in a single table         |
+| RuntimePerformance | Get Execution time for each run                    |
+| ResourceMonitor    | Monitor resources of running jobs (CPU and Memory) |
 
 And more to come ! 
 
 ## Also Available 
   
   - `PerfLogger` : A simple to use performance logger
   
@@ -90,9 +110,8 @@
 ```
 
 ## You too, have cool Callbacks, or idea for one ? 
 
 Open a PR or an issue !
 
 ### Possible Ideas
-- [In progress] A Ressource Monitoring Callback 
 - A callback that summarize log from multiple runs
```

### Comparing `hydra-callbacks-0.2.0/README.md` & `hydra-callbacks-0.3.0/README.md`

 * *Files 27% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 
 [![style](https://img.shields.io/badge/style-black-black)](https://github.com/psf/black)
 [![framework](https://img.shields.io/badge/framework-hydra-blue)](https://hydra.cc)
 [![codecov](https://codecov.io/gh/paquiteau/hydra-callbacks/branch/master/graph/badge.svg?token=NEV7SY24YB)](https://codecov.io/gh/paquiteau/hydra-callbacks)
 [![CD](https://github.com/paquiteau/hydra-callbacks/actions/workflows/master-cd.yml/badge.svg)](https://github.com/paquiteau/hydra-callbacks/actions/workflows/master-cd.yml)
 [![CI](https://github.com/paquiteau/hydra-callbacks/actions/workflows/test-ci.yml/badge.svg)](https://github.com/paquiteau/hydra-callbacks/actions/workflows/test-ci.yml)
-[![Release](https://github.com/paquiteau/hydra-callbacks/releases/latest)](https://img.shields.io/github/v/release/paquiteau/hydra-callbacks)
+[![Release](https://img.shields.io/github/v/release/paquiteau/hydra-callbacks)](https://github.com/paquiteau/hydra-callbacks/releases/latest)
 
 A collection of usefulls callbacks for the [https://hydra.cc/](hydra) configuration framework.
 
 
 ## Installation 
 ``` shell 
 pip install hydra-callbacks
@@ -19,36 +19,56 @@
 Development version 
 ``` shell
 pip install git+https://github.com/paquiteau/hydra-callbacks
 ```
 
 ## Usage 
 
-In your hydra root config file add the following: 
+In your hydra root config file add the following, or analoguous:
 
 ``` yaml
-hydra: 
-  # ... 
-  callbacks: 
-    git_info:
-      _target_: hydra_callbacks.GitInfo 
+hydra:
+  callbacks:
+    git_infos:
+      _target_: hydra_callbacks.GitInfo
       clean: true
-    latest_link:
+    latest_run:
       _target_: hydra_callbacks.LatestRunLink
+    resource_monitor:
+      _target_: hydra_callbacks.ResourceMonitor
+      sample_interval: 0.5
+    runtime_perf:
+      _target_: hydra_callbacks.RuntimePerformance      
 ```
 
+This will enrich your script output with: 
+
+```console
+paquiteau@laptop$ python my_app.py
+[hydra] Git sha: 844b9ca1a74d8307ef5331351897cebb18f71b88, dirty: False
+
+## All your app log and outputs ##
+
+[hydra][INFO] - Total runtime: 0.51 seconds
+[hydra][INFO] - Writing monitoring data to [...]/outputs/2023-04-06/16-02-46/resource_monitoring.csv
+[hydra][INFO] - Latest run is at: [...]/outputs/latest
+```
+
+
+Detailled configuration for each callback is available in the `tests/test_app/` folder.
 
 ## Available Callbacks 
 
-| Name               | Action                                     |
-|:-------------------|:-------------------------------------------|
-| GitInfo            | Check status of Repository                 |
-| LatestRunLink      | Get a link to the latest run               |
-| MultiRunGatherer   | Gather results json file in a single table |
-| RuntimePerformance | Get Execution time for each run            |
+| Name               | Action                                             |
+|:-------------------|:---------------------------------------------------|
+| GitInfo            | Check status of Repository                         |
+| LatestRunLink      | Get a link to the latest run                       |
+| MultiRunGatherer   | Gather results json file in a single table         |
+| RuntimePerformance | Get Execution time for each run                    |
+| ResourceMonitor    | Monitor resources of running jobs (CPU and Memory) |
 
 And more to come ! 
 
 ## Also Available 
   
   - `PerfLogger` : A simple to use performance logger
   
@@ -69,9 +89,8 @@
 ```
 
 ## You too, have cool Callbacks, or idea for one ? 
 
 Open a PR or an issue !
 
 ### Possible Ideas
-- [In progress] A Ressource Monitoring Callback 
 - A callback that summarize log from multiple runs
```

### Comparing `hydra-callbacks-0.2.0/pyproject.toml` & `hydra-callbacks-0.3.0/pyproject.toml`

 * *Files identical despite different names*

### Comparing `hydra-callbacks-0.2.0/src/hydra_callbacks/__init__.py` & `hydra-callbacks-0.3.0/src/hydra_callbacks/__init__.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 """A collection of Hydra callbacks for logging and performance analysis."""
 from .callbacks import (
     AnyRunCallback,
     GitInfo,
     LatestRunLink,
     MultiRunGatherer,
-    RessourceMonitor,
+    ResourceMonitor,
     RuntimePerformance,
 )
 from .logger import PerfLogger
 
 __all__ = [
     "AnyRunCallback",
     "RuntimePerformance",
     "GitInfo",
     "MultiRunGatherer",
-    "RessourceMonitor",
+    "ResourceMonitor",
     "LatestRunLink",
     "PerfLogger",
 ]
 
 
 try:
     # -- Distribution mode --
```

### Comparing `hydra-callbacks-0.2.0/src/hydra_callbacks/callbacks.py` & `hydra-callbacks-0.3.0/src/hydra_callbacks/callbacks.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,47 +1,67 @@
 """Callback mechanism for hydra  jobs."""
+from __future__ import annotations
+from typing import Callable
 import errno
 import glob
 import json
 import logging
 import os
+from pathlib import Path
 import time
 
 import pandas as pd
 from hydra.core.hydra_config import HydraConfig
 from hydra.core.utils import JobReturn
 from hydra.experimental.callback import Callback
 from hydra.types import TaskFunction
 from hydra.utils import to_absolute_path
 from omegaconf import DictConfig, open_dict
 
 from .monitor import ResourceMonitorService
 
+callback_logger = logging.getLogger("hydra.callbacks")
+
 
 class AnyRunCallback(Callback):
     """Abstract Callback that execute on any run."""
 
+    def __init__(self, enabled: bool = True):
+        callback_logger.debug("Init %s", self.__class__.__name__)
+
+        self.enabled = enabled
+        if not self.enabled:
+            # don't do anything if not enabled
+            self.on_job_start = lambda *args, **kwargs: None
+            self.on_job_end = lambda *args, **kwargs: None
+            self._on_anyrun_start = lambda *args, **kwargs: None
+            self._on_anyrun_end = lambda *args, **kwargs: None
+
     def on_run_start(self, config: DictConfig, **kwargs: None) -> None:
         """Execute before a single run."""
+        callback_logger.debug("run start callback %s", self.__class__.__name__)
         self._on_anyrun_start(config, **kwargs)
 
     def on_multirun_start(self, config: DictConfig, **kwargs: None) -> None:
         """Execute before a multi run."""
+        callback_logger.debug("(multi)run start callback %s", self.__class__.__name__)
         self._on_anyrun_start(config, **kwargs)
 
     def _on_anyrun_start(self, config: DictConfig, **kwargs: None) -> None:
         """Execute before any run."""
         pass
 
     def on_run_end(self, config: DictConfig, **kwargs: None) -> None:
         """Execute before a single run."""
+        callback_logger.debug("run end callback %s", self.__class__.__name__)
         self._on_anyrun_end(config, **kwargs)
 
     def on_multirun_end(self, config: DictConfig, **kwargs: None) -> None:
         """Execute before a multi run."""
+        callback_logger.debug("(multi)run end callback %s", self.__class__.__name__)
         self._on_anyrun_end(config, **kwargs)
 
     def _on_anyrun_end(self, config: DictConfig, **kwargs: None) -> None:
         """Execute before any run."""
         pass
 
 
@@ -51,56 +71,52 @@
     Parameters
     ----------
     enabled : bool
         if True, will log the total runtime.
     """
 
     def __init__(self, enabled: bool = True):
-        self.enabled = enabled
-        if not self.enabled:
-            self._on_anyrun_start = lambda *args, **kwargs: None
-            self._on_anyrun_end = lambda *args, **kwargs: None
+        super().__init__(enabled)
 
     def _on_anyrun_start(self, config: DictConfig, **kwargs: None) -> None:
         """Execute before any run."""
         self.start_time = time.perf_counter()
 
     def _on_anyrun_end(self, config: DictConfig, **kwargs: None) -> None:
         """Execute after any run."""
         end_time = time.perf_counter()
         duration = end_time - self.start_time
-        logging.getLogger("hydra").info(f"Total runtime: {duration:.2f} seconds")
+        callback_logger.info(f"Total runtime: {duration:.2f} seconds")
 
 
 class GitInfo(AnyRunCallback):
     """
     Callback that check git infos and log them.
 
     Parameters
     ----------
     clean
         if True, will fail if the repo is not clean
     """
 
     def __init__(self, clean: bool = False):
+        super().__init__()
         self.clean = clean
 
     def _on_anyrun_start(self, config: DictConfig, **kwargs: None) -> None:
         """Execute before any run."""
         import git
 
-        log = logging.getLogger("hydra")
-
         repo = git.Repo(search_parent_directories=True)
         sha = repo.head.object.hexsha
         is_dirty = repo.is_dirty()
-        log.warning(f"Git sha: {sha}, dirty: {is_dirty}")
+        callback_logger.warning(f"Git sha: {sha}, dirty: {is_dirty}")
 
         if is_dirty and self.clean:
-            log.error("Repo is dirty, aborting")  # pragma: no cover
+            callback_logger.error("Repo is dirty, aborting")  # pragma: no cover
             # sys.exit(1) raises an error, that is catched by hydra.
             # os._exit exits directly by stopping the process.
             os._exit(1)  # pragma: no cover
 
         # Add git info to config
         with open_dict(config):  # disable hydra's config protection
             config.git = {"sha": sha, "is_dirty": is_dirty}
@@ -109,36 +125,50 @@
 class MultiRunGatherer(Callback):
     """Define a callback to gather job results from json files after a multirun.
 
     Parameters
     ----------
     result_file: str
         name of the file to gathers from all the jobs.
+    aggregator: Callable
+        function to aggregate the results. This function should take a list of
+        filepath as input and process them. By default this assume that each
+        result file is a json file, and will load them as a list of dict, and
+        save them as a csv file.
     """
 
-    def __init__(self, result_file: str = "results.json"):
+    def __init__(self, result_file: str = "results.json", aggregator: Callable = None):
+        callback_logger.debug("Init %s", self.__class__.__name__)
         self.result_file = result_file
 
+        self.aggregator = aggregator or self._default_aggregator
+
     def on_multirun_end(self, config: DictConfig, **kwargs: None) -> None:
         """Run after all job have ended.
 
         Will write a DataFrame from all the results. at the run location.
         """
         save_dir = config.hydra.sweep.dir
         os.chdir(save_dir)
+        self.aggregator(glob.glob(f"*/{self.result_file}"))
+
+    def _default_aggregator(self, files: list[os.PathLike]) -> os.PathLike:
+        """Aggregat the results as a dataframe and save it as csv."""
         results = []
-        for filename in glob.glob(f"*/{self.result_file}"):
+        for filename in files:
             with open(filename) as f:
                 loaded = json.load(f)
                 if isinstance(loaded, list):
                     results.extend(loaded)
                 else:
                     results.append(loaded)
         df = pd.DataFrame(results)
         df.to_csv("agg_results.csv")
+        callback_logger.info(f"Gathered results in {Path.cwd() / 'agg_results.csv'}")
+        return Path.cwd() / "agg_results.csv"
 
 
 class LatestRunLink(Callback):
     """Callback that create a symlink to the latest run in the base output dir.
 
     Parameters
     ----------
@@ -147,14 +177,15 @@
     multirun_base_dir: str
         name of the basedir for multirun
     """
 
     def __init__(
         self, run_base_dir: str = "outputs", multirun_base_dir: str = "multirun"
     ):
+        callback_logger.debug("Init %s", self.__class__.__name__)
         self.run_base_dir = to_absolute_path(run_base_dir)
         self.multirun_base_dir = to_absolute_path(multirun_base_dir)
 
     def on_run_end(self, config: DictConfig, **kwargs: None) -> None:
         """Execute after a single run."""
         self._on_anyrun_end(config.hydra.run.dir, self.run_base_dir)
 
@@ -164,29 +195,29 @@
 
     def _on_anyrun_end(self, run_dir: str, base_dir: str) -> None:
         latest_dir_path = os.path.join(base_dir, "latest")
         self._force_symlink(
             to_absolute_path(run_dir),
             to_absolute_path(latest_dir_path),
         )
-        logging.getLogger("hydra").info(f"Latest run is at: {latest_dir_path}")
+        callback_logger.info(f"Latest run is at: {latest_dir_path}")
 
     def _force_symlink(self, src: str, dest: str) -> None:
         """Create a symlink from src to test, overwriting dest if necessary."""
         try:
             os.symlink(src, dest)
         except OSError as e:
             if e.errno == errno.EEXIST:
                 os.remove(dest)
                 os.symlink(src, dest)
             else:
                 raise e  # pragma: no cover
 
 
-class RessourceMonitor(AnyRunCallback):
+class ResourceMonitor(AnyRunCallback):
     """Callback that samples the cpu and memory usage during job execution.
 
     The collected  data (cpu percent, memory usage) is written to a csv file.
 
     TODO: Add GPU support.
 
     Parameters
@@ -201,22 +232,15 @@
 
     def __init__(
         self,
         enabled: bool = True,
         sample_interval: float = 1,
         monitoring_file: str = "resource_monitoring.csv",
     ):
-        self.enabled = enabled
-        if not self.enabled:
-            # don't do anything if not enabled
-            self.on_job_start = lambda *args, **kwargs: None
-            self.on_job_end = lambda *args, **kwargs: None
-            self._on_anyrun_start = lambda *args, **kwargs: None
-            self._on_anyrun_end = lambda *args, **kwargs: None
-            return
+        super().__init__(enabled)
 
         self.sample_interval = sample_interval
         self.monitoring_file = monitoring_file
 
     def on_run_start(self, config: DictConfig, **kwargs: None) -> None:
         """Execute after a single run."""
         self._on_anyrun_start(config.hydra.run.dir)
@@ -230,17 +254,15 @@
         self.monitoring_file = os.path.join(
             to_absolute_path(run_dir), self.monitoring_file
         )
         self._monitor = {}
 
     def _on_anyrun_end(self, config: DictConfig, **kwargs: None) -> None:
         """Run on any run end."""
-        logging.getLogger("hydra").info(
-            f"Writing monitoring data to {self.monitoring_file}"
-        )
+        callback_logger.info(f"Writing monitoring data to {self.monitoring_file}")
 
     def on_job_start(
         self, config: DictConfig, *, task_function: TaskFunction, **kwargs: None
     ) -> None:
         """Execute before a single job."""
         job_full_id = self._get_job_info()
         self._monitor[job_full_id] = ResourceMonitorService(
```

### Comparing `hydra-callbacks-0.2.0/src/hydra_callbacks/logger.py` & `hydra-callbacks-0.3.0/src/hydra_callbacks/logger.py`

 * *Files identical despite different names*

### Comparing `hydra-callbacks-0.2.0/src/hydra_callbacks/monitor.py` & `hydra-callbacks-0.3.0/src/hydra_callbacks/monitor.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-"""Ressource Monitor Utilities."""
+"""Resource Monitor Utilities."""
 import multiprocessing
 import os
 import time
 from typing import Callable
 
 import numpy as np
 import psutil
```

### Comparing `hydra-callbacks-0.2.0/src/hydra_callbacks.egg-info/PKG-INFO` & `hydra-callbacks-0.3.0/src/hydra_callbacks.egg-info/PKG-INFO`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hydra-callbacks
-Version: 0.2.0
+Version: 0.3.0
 Summary: A collection of usefull hydra callbacks for hydra configuration
 Author-email: Pierre-Antoine Comby <pierre-antoine.comby@cea.fr>
 Project-URL: Homepage, https://github.com/paquiteau/hydra-callbacks
 Project-URL: Bug Reports, https://github.com/paquiteau/hydra-callbacks/issues
 Project-URL: Sources, https://github.com/paquiteau/hydra-callbacks
 Keywords: hydra,configuration,callback
 Classifier: Development Status :: 3 - Alpha
@@ -23,15 +23,15 @@
 
 
 [![style](https://img.shields.io/badge/style-black-black)](https://github.com/psf/black)
 [![framework](https://img.shields.io/badge/framework-hydra-blue)](https://hydra.cc)
 [![codecov](https://codecov.io/gh/paquiteau/hydra-callbacks/branch/master/graph/badge.svg?token=NEV7SY24YB)](https://codecov.io/gh/paquiteau/hydra-callbacks)
 [![CD](https://github.com/paquiteau/hydra-callbacks/actions/workflows/master-cd.yml/badge.svg)](https://github.com/paquiteau/hydra-callbacks/actions/workflows/master-cd.yml)
 [![CI](https://github.com/paquiteau/hydra-callbacks/actions/workflows/test-ci.yml/badge.svg)](https://github.com/paquiteau/hydra-callbacks/actions/workflows/test-ci.yml)
-[![Release](https://github.com/paquiteau/hydra-callbacks/releases/latest)](https://img.shields.io/github/v/release/paquiteau/hydra-callbacks)
+[![Release](https://img.shields.io/github/v/release/paquiteau/hydra-callbacks)](https://github.com/paquiteau/hydra-callbacks/releases/latest)
 
 A collection of usefulls callbacks for the [https://hydra.cc/](hydra) configuration framework.
 
 
 ## Installation 
 ``` shell 
 pip install hydra-callbacks
@@ -40,36 +40,56 @@
 Development version 
 ``` shell
 pip install git+https://github.com/paquiteau/hydra-callbacks
 ```
 
 ## Usage 
 
-In your hydra root config file add the following: 
+In your hydra root config file add the following, or analoguous:
 
 ``` yaml
-hydra: 
-  # ... 
-  callbacks: 
-    git_info:
-      _target_: hydra_callbacks.GitInfo 
+hydra:
+  callbacks:
+    git_infos:
+      _target_: hydra_callbacks.GitInfo
       clean: true
-    latest_link:
+    latest_run:
       _target_: hydra_callbacks.LatestRunLink
+    resource_monitor:
+      _target_: hydra_callbacks.ResourceMonitor
+      sample_interval: 0.5
+    runtime_perf:
+      _target_: hydra_callbacks.RuntimePerformance      
 ```
 
+This will enrich your script output with: 
+
+```console
+paquiteau@laptop$ python my_app.py
+[hydra] Git sha: 844b9ca1a74d8307ef5331351897cebb18f71b88, dirty: False
+
+## All your app log and outputs ##
+
+[hydra][INFO] - Total runtime: 0.51 seconds
+[hydra][INFO] - Writing monitoring data to [...]/outputs/2023-04-06/16-02-46/resource_monitoring.csv
+[hydra][INFO] - Latest run is at: [...]/outputs/latest
+```
+
+
+Detailled configuration for each callback is available in the `tests/test_app/` folder.
 
 ## Available Callbacks 
 
-| Name               | Action                                     |
-|:-------------------|:-------------------------------------------|
-| GitInfo            | Check status of Repository                 |
-| LatestRunLink      | Get a link to the latest run               |
-| MultiRunGatherer   | Gather results json file in a single table |
-| RuntimePerformance | Get Execution time for each run            |
+| Name               | Action                                             |
+|:-------------------|:---------------------------------------------------|
+| GitInfo            | Check status of Repository                         |
+| LatestRunLink      | Get a link to the latest run                       |
+| MultiRunGatherer   | Gather results json file in a single table         |
+| RuntimePerformance | Get Execution time for each run                    |
+| ResourceMonitor    | Monitor resources of running jobs (CPU and Memory) |
 
 And more to come ! 
 
 ## Also Available 
   
   - `PerfLogger` : A simple to use performance logger
   
@@ -90,9 +110,8 @@
 ```
 
 ## You too, have cool Callbacks, or idea for one ? 
 
 Open a PR or an issue !
 
 ### Possible Ideas
-- [In progress] A Ressource Monitoring Callback 
 - A callback that summarize log from multiple runs
```

### Comparing `hydra-callbacks-0.2.0/src/hydra_callbacks.egg-info/SOURCES.txt` & `hydra-callbacks-0.3.0/src/hydra_callbacks.egg-info/SOURCES.txt`

 * *Files 0% similar despite different names*

```diff
@@ -21,9 +21,9 @@
 tests/test_app/dummy.txt
 tests/test_app/dummy_app.py
 tests/test_app/gather_app.py
 tests/test_app/gather_app_conf.yaml
 tests/test_app/git_callback.yaml
 tests/test_app/latest_callback.yaml
 tests/test_app/perf_app.py
-tests/test_app/ressource_monitor.yaml
+tests/test_app/resource_monitor.yaml
 tests/test_app/runtime_perf.yaml
```

### Comparing `hydra-callbacks-0.2.0/tests/test_app/gather_app.py` & `hydra-callbacks-0.3.0/tests/test_app/gather_app.py`

 * *Files identical despite different names*

### Comparing `hydra-callbacks-0.2.0/tests/test_app/perf_app.py` & `hydra-callbacks-0.3.0/tests/test_app/perf_app.py`

 * *Files identical despite different names*

### Comparing `hydra-callbacks-0.2.0/tests/test_callbacks.py` & `hydra-callbacks-0.3.0/tests/test_callbacks.py`

 * *Files 5% similar despite different names*

```diff
@@ -233,28 +233,32 @@
         "hydra.job_logging.formatters.simple.format='[JOB] %(message)s'",
     ]
     result, _err = run_python_script(cmd)
     assert _err == ""
     assert_regex_match(
         result,
         dedent(
-            """
+            """\
             [HYDRA] Launching 3 jobs locally
             [HYDRA] 	#0 : +a=1
             [JOB] foo: bar
             a: 1
 
             [HYDRA] 	#1 : +a=2
             [JOB] foo: bar
             a: 2
 
             [HYDRA] 	#2 : +a=3
             [JOB] foo: bar
             a: 3
-            """
+
+            [HYDRA] Gathered results in {tmpdir}/agg_results.csv
+            """.format(
+                tmpdir=tmpdir
+            )
         ),
     )
     with open(tmpdir / "agg_results.csv") as f:
         assert len(f.readlines()) == 4
 
 
 def test_dirty_git_repo_error(tmpdir: Path) -> None:
@@ -292,20 +296,20 @@
                 sha=sha,
             )
         ),
     )
 
 
 @pytest.mark.parametrize("multirun", [True, False])
-def test_ressource_monitor(tmpdir: Path, multirun) -> None:
+def test_resource_monitor(tmpdir: Path, multirun) -> None:
     """Test for resource monitor callback."""
 
     cmd = [
         "tests/test_app/dummy_app.py",
-        "--config-name=ressource_monitor.yaml",
+        "--config-name=resource_monitor.yaml",
         "hydra.sweep.dir=" + str(tmpdir),
         "hydra.run.dir=" + str(tmpdir),
         "hydra.job.chdir=True",
         "hydra.hydra_logging.formatters.simple.format='[HYDRA] %(message)s'",
         "hydra.job_logging.formatters.simple.format='[JOB] %(message)s'",
     ]
     if multirun:
@@ -322,57 +326,55 @@
         """.format(
                 tmpdir=tmpdir, logger="HYDRA" if multirun else "JOB"
             )
         ),
     )
 
 
-def test_ressource_monitor_disabled(tmpdir):
-
+def test_resource_monitor_disabled(tmpdir):
     cmd = [
         "tests/test_app/dummy_app.py",
-        "--config-name=ressource_monitor.yaml",
-        "hydra.callbacks.ressource_monitor.enabled=False",
+        "--config-name=resource_monitor.yaml",
+        "hydra.callbacks.resource_monitor.enabled=False",
         "hydra.sweep.dir=" + str(tmpdir),
         "hydra.run.dir=" + str(tmpdir),
         "hydra.job.chdir=True",
         "hydra.hydra_logging.formatters.simple.format='[HYDRA] %(message)s'",
         "hydra.job_logging.formatters.simple.format='[JOB] %(message)s'",
     ]
 
     result, _err = run_python_script(cmd)
 
     assert_regex_match(result, "[JOB] foo: bar")
 
 
-def test_ressource_monitor_raises(tmpdir):
-
+def test_resource_monitor_raises(tmpdir):
     cmd = [
         "tests/test_app/dummy_app.py",
-        "--config-name=ressource_monitor.yaml",
-        "hydra.callbacks.ressource_monitor.sample_interval=0.1",
+        "--config-name=resource_monitor.yaml",
+        "hydra.callbacks.resource_monitor.sample_interval=0.1",
         "hydra.sweep.dir=" + str(tmpdir),
         "hydra.run.dir=" + str(tmpdir),
         "hydra.job.chdir=True",
         "hydra.hydra_logging.formatters.simple.format='[HYDRA] %(message)s'",
         "hydra.job_logging.formatters.simple.format='[JOB] %(message)s'",
     ]
 
     result, _err = run_python_script(cmd, raise_exception=False)
 
     assert "RuntimeError: Sampling interval (0.10s) cannot be lower than 0.2s" in _err
 
 
-def test_ressource_monitor_results(tmpdir: Path) -> None:
+def test_resource_monitor_results(tmpdir: Path) -> None:
     """Test for resource monitor callback."""
     sampling_time = 0.3  # seconds
     cmd = [
         "tests/test_app/perf_app.py",
-        "--config-name=ressource_monitor.yaml",
-        "hydra.callbacks.ressource_monitor.sample_interval=" + str(sampling_time),
+        "--config-name=resource_monitor.yaml",
+        "hydra.callbacks.resource_monitor.sample_interval=" + str(sampling_time),
         "hydra.sweep.dir=" + str(tmpdir),
         "hydra.run.dir=" + str(tmpdir),
         "hydra.job.chdir=True",
         "hydra.hydra_logging.formatters.simple.format='[HYDRA] %(message)s'",
         "hydra.job_logging.formatters.simple.format='[JOB] %(message)s'",
     ]
```

### Comparing `hydra-callbacks-0.2.0/tests/test_perflogger.py` & `hydra-callbacks-0.3.0/tests/test_perflogger.py`

 * *Files identical despite different names*

