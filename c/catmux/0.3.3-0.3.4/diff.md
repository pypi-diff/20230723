# Comparing `tmp/catmux-0.3.3.tar.gz` & `tmp/catmux-0.3.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "catmux-0.3.3.tar", last modified: Fri Jul 21 15:25:21 2023, max compression
+gzip compressed data, was "catmux-0.3.4.tar", last modified: Sat Jul 22 23:01:28 2023, max compression
```

## Comparing `catmux-0.3.3.tar` & `catmux-0.3.4.tar`

### file list

```diff
@@ -1,29 +1,33 @@
-drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-21 15:25:21.172839 catmux-0.3.3/
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     1068 2023-04-04 19:35:47.000000 catmux-0.3.3/LICENSE
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     6391 2023-07-21 15:25:21.172839 catmux-0.3.3/PKG-INFO
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     5940 2023-07-21 15:13:50.000000 catmux-0.3.3/README.md
-drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-21 15:25:21.172839 catmux-0.3.3/catmux/
--rw-rw-r--   0 mauch     (1000) mauch     (1000)        0 2023-04-04 19:35:47.000000 catmux-0.3.3/catmux/__init__.py
--rw-rw-r--   0 mauch     (1000) mauch     (1000)      210 2023-07-21 15:13:50.000000 catmux-0.3.3/catmux/exceptions.py
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     1477 2023-04-04 19:35:47.000000 catmux-0.3.3/catmux/prefix.py
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     9333 2023-07-21 15:13:50.000000 catmux-0.3.3/catmux/session.py
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     2172 2023-04-04 19:35:47.000000 catmux-0.3.3/catmux/split.py
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     2426 2023-04-04 19:35:47.000000 catmux-0.3.3/catmux/tmux_wrapper.py
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     4066 2023-07-21 15:13:50.000000 catmux-0.3.3/catmux/window.py
-drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-21 15:25:21.172839 catmux-0.3.3/catmux.egg-info/
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     6391 2023-07-21 15:25:21.000000 catmux-0.3.3/catmux.egg-info/PKG-INFO
--rw-rw-r--   0 mauch     (1000) mauch     (1000)      444 2023-07-21 15:25:21.000000 catmux-0.3.3/catmux.egg-info/SOURCES.txt
--rw-rw-r--   0 mauch     (1000) mauch     (1000)        1 2023-07-21 15:25:21.000000 catmux-0.3.3/catmux.egg-info/dependency_links.txt
--rw-rw-r--   0 mauch     (1000) mauch     (1000)        7 2023-07-21 15:25:21.000000 catmux-0.3.3/catmux.egg-info/requires.txt
--rw-rw-r--   0 mauch     (1000) mauch     (1000)        7 2023-07-21 15:25:21.000000 catmux-0.3.3/catmux.egg-info/top_level.txt
-drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-21 15:25:21.172839 catmux-0.3.3/etc/
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     1984 2023-07-21 13:14:52.000000 catmux-0.3.3/etc/example_session.yaml
--rw-rw-r--   0 mauch     (1000) mauch     (1000)      810 2023-04-04 19:35:47.000000 catmux-0.3.3/etc/readme_tmux.txt
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     1593 2023-04-04 19:35:47.000000 catmux-0.3.3/etc/tmux_default.conf
-drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-21 15:25:21.172839 catmux-0.3.3/script/
--rwxrwxr-x   0 mauch     (1000) mauch     (1000)     4797 2023-07-21 15:13:50.000000 catmux-0.3.3/script/catmux_create_session
--rw-rw-r--   0 mauch     (1000) mauch     (1000)       38 2023-07-21 15:25:21.172839 catmux-0.3.3/setup.cfg
--rw-rw-r--   0 mauch     (1000) mauch     (1000)      964 2023-07-21 15:23:08.000000 catmux-0.3.3/setup.py
-drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-21 15:25:21.172839 catmux-0.3.3/test/
--rw-rw-r--   0 mauch     (1000) mauch     (1000)      873 2023-07-21 14:44:10.000000 catmux-0.3.3/test/test_helpers.py
--rw-rw-r--   0 mauch     (1000) mauch     (1000)     2159 2023-07-21 15:22:06.000000 catmux-0.3.3/test/test_parsing.py
+drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-22 23:01:28.309641 catmux-0.3.4/
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     1068 2023-04-04 19:35:47.000000 catmux-0.3.4/LICENSE
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     6358 2023-07-22 23:01:28.309641 catmux-0.3.4/PKG-INFO
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     5927 2023-07-22 21:14:37.000000 catmux-0.3.4/README.md
+drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-22 23:01:28.305641 catmux-0.3.4/catmux/
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)        0 2023-04-04 19:35:47.000000 catmux-0.3.4/catmux/__init__.py
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     1984 2023-07-22 20:22:49.000000 catmux-0.3.4/catmux/example_session.yaml
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)      210 2023-07-21 15:13:50.000000 catmux-0.3.4/catmux/exceptions.py
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     1758 2023-07-22 22:59:09.000000 catmux-0.3.4/catmux/prefix.py
+drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-22 23:01:28.309641 catmux-0.3.4/catmux/resources/
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)        0 2023-07-22 21:14:37.000000 catmux-0.3.4/catmux/resources/__init__.py
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     1984 2023-07-22 21:14:37.000000 catmux-0.3.4/catmux/resources/example_session.yaml
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)      810 2023-07-22 21:14:37.000000 catmux-0.3.4/catmux/resources/readme_tmux.txt
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     1593 2023-07-22 21:14:37.000000 catmux-0.3.4/catmux/resources/tmux_default.conf
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     8951 2023-07-22 22:59:09.000000 catmux-0.3.4/catmux/session.py
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     2172 2023-04-04 19:35:47.000000 catmux-0.3.4/catmux/split.py
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     2426 2023-07-22 22:53:23.000000 catmux-0.3.4/catmux/tmux_wrapper.py
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     4066 2023-07-21 15:13:50.000000 catmux-0.3.4/catmux/window.py
+drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-22 23:01:28.305641 catmux-0.3.4/catmux.egg-info/
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     6358 2023-07-22 23:01:28.000000 catmux-0.3.4/catmux.egg-info/PKG-INFO
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)      723 2023-07-22 23:01:28.000000 catmux-0.3.4/catmux.egg-info/SOURCES.txt
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)        1 2023-07-22 23:01:28.000000 catmux-0.3.4/catmux.egg-info/dependency_links.txt
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)        7 2023-07-22 23:01:28.000000 catmux-0.3.4/catmux.egg-info/requires.txt
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)        7 2023-07-22 23:01:28.000000 catmux-0.3.4/catmux.egg-info/top_level.txt
+drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-22 23:01:28.309641 catmux-0.3.4/script/
+-rwxrwxr-x   0 mauch     (1000) mauch     (1000)     4846 2023-07-22 21:14:37.000000 catmux-0.3.4/script/catmux_create_session
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)       38 2023-07-22 23:01:28.309641 catmux-0.3.4/setup.cfg
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)      825 2023-07-22 23:01:13.000000 catmux-0.3.4/setup.py
+drwxrwxr-x   0 mauch     (1000) mauch     (1000)        0 2023-07-22 23:01:28.309641 catmux-0.3.4/test/
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)      644 2023-07-22 21:03:52.000000 catmux-0.3.4/test/test_debug.py
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     1328 2023-07-22 22:59:09.000000 catmux-0.3.4/test/test_helpers.py
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     5112 2023-07-22 22:59:09.000000 catmux-0.3.4/test/test_parsing.py
+-rw-rw-r--   0 mauch     (1000) mauch     (1000)     2820 2023-07-22 22:59:09.000000 catmux-0.3.4/test/test_run.py
```

### Comparing `catmux-0.3.3/LICENSE` & `catmux-0.3.4/LICENSE`

 * *Files identical despite different names*

### Comparing `catmux-0.3.3/PKG-INFO` & `catmux-0.3.4/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,20 +1,19 @@
 Metadata-Version: 2.1
 Name: catmux
-Version: 0.3.3
+Version: 0.3.4
 Summary: A tmux orchestration package.
 Home-page: https://github.com/fmauch/catmux
 Author: Felix Exner
 Author-email: felix_mauch@web.de
 License: MIT
-Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
-Requires-Python: >=3.6
+Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Catmux
 [![codecov](https://codecov.io/gh/fmauch/catmux/branch/master/graph/badge.svg?token=bPcdYrOBRK)](https://codecov.io/gh/fmauch/catmux)
 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
 
@@ -50,20 +49,20 @@
 repository's root directory. If you use this option, please be aware that some examples behave
 differently if you have installed catmux this way and are calling it from the repository directory.
 Calling them from outside the directory (e.g. after leaving via `cd`) is fine and should result in
 the same behavior as with the recommended installation method.
 
 ## Usage
 Currently, there is no full-blown documentation, but the example config file in
-`etc/example_session.yaml` gives a detailed insight on possible commands.
+`catmux/resources/example_session.yaml` gives a detailed insight on possible commands.
 
 ### Running the example the most simple way
 After installation, you can run a simple example by calling the following command:
 ```
-catmux_create_session $(python3 -m catmux.prefix)/share/catmux/example_session.yaml
+catmux_create_session $(python3 -m catmux.prefix)/example_session.yaml
 ```
 
 To see further options, simply run it with argument `-h`:
 ```
 $ catmux_create_session -h
 usage: catmux_create_session [-h] [-n SESSION_NAME] [-t TMUX_CONFIG] [-d] [--overwrite OVERWRITE]
                              session_config
@@ -84,23 +83,23 @@
                         Overwrite a parameter from the session config. Parameters can be specified
                         using a comma-separated list such as '--overwrite param_a=1,param_b=2'.
 ```
 
 ### Full blown example
 To make use of all catmux features, run the following example command:
 ```
-catmux_create_session $(python3 -m catmux.prefix)/share/catmux/example_session.yaml \
-  --tmux_config $(python3 -m catmux.prefix)/share/catmux/tmux_default.conf \
+catmux_create_session $(python3 -m catmux.prefix)/example_session.yaml \
+  --tmux_config $(python3 -m catmux.prefix)/tmux_default.conf \
   --session_name example_session \
   --overwrite show_layouts=True,replacement_param="new catmux user"
 ```
 
 ### Killing a catmux session
 If you are not that familiar with tmux: To kill a session, simply type `tmux kill-session` in any
-terminal window. In the `etc/tmux_default.conf` there is a key-binding for that, see
+terminal window. In the `catmux/resources/tmux_default.conf` there is a key-binding for that, see
 `etc/readme_tmux.txt` for details.
 
 ### Tmux server to be used
 By default, catmux spawns its own tmux server called `catmux`. Therefore, a simple
 `tmux list-sessions` (or `tmux ls`) will not list the `catmux` session. To list the `catmux`
 session, use `tmux -L catmux list-sessions`. You can change the server's name by specifying the
 `-L <server_name>` parameter to `catmux_create_session`. That mechanism ensures that the environment
@@ -123,9 +122,7 @@
 For ROS2, the same is achievable with `ros2 pkg prefix` but the yaml has to be installed (similar
 to, for example, a launch file) and the installation path has to be specified:
 ```
 catmux_create_session $(ros2 pkg prefix <your_package_name>)/path/to/the/installed/<your_catmux_session_config.yaml>
 
 # for example: $ catmux_create_session $(ros2 pkg prefix catmux_test_pkg)/share/catmux_test_pkg/catmux_session.yaml
 ```
-
-
```

### Comparing `catmux-0.3.3/README.md` & `catmux-0.3.4/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -34,20 +34,20 @@
 repository's root directory. If you use this option, please be aware that some examples behave
 differently if you have installed catmux this way and are calling it from the repository directory.
 Calling them from outside the directory (e.g. after leaving via `cd`) is fine and should result in
 the same behavior as with the recommended installation method.
 
 ## Usage
 Currently, there is no full-blown documentation, but the example config file in
-`etc/example_session.yaml` gives a detailed insight on possible commands.
+`catmux/resources/example_session.yaml` gives a detailed insight on possible commands.
 
 ### Running the example the most simple way
 After installation, you can run a simple example by calling the following command:
 ```
-catmux_create_session $(python3 -m catmux.prefix)/share/catmux/example_session.yaml
+catmux_create_session $(python3 -m catmux.prefix)/example_session.yaml
 ```
 
 To see further options, simply run it with argument `-h`:
 ```
 $ catmux_create_session -h
 usage: catmux_create_session [-h] [-n SESSION_NAME] [-t TMUX_CONFIG] [-d] [--overwrite OVERWRITE]
                              session_config
@@ -68,23 +68,23 @@
                         Overwrite a parameter from the session config. Parameters can be specified
                         using a comma-separated list such as '--overwrite param_a=1,param_b=2'.
 ```
 
 ### Full blown example
 To make use of all catmux features, run the following example command:
 ```
-catmux_create_session $(python3 -m catmux.prefix)/share/catmux/example_session.yaml \
-  --tmux_config $(python3 -m catmux.prefix)/share/catmux/tmux_default.conf \
+catmux_create_session $(python3 -m catmux.prefix)/example_session.yaml \
+  --tmux_config $(python3 -m catmux.prefix)/tmux_default.conf \
   --session_name example_session \
   --overwrite show_layouts=True,replacement_param="new catmux user"
 ```
 
 ### Killing a catmux session
 If you are not that familiar with tmux: To kill a session, simply type `tmux kill-session` in any
-terminal window. In the `etc/tmux_default.conf` there is a key-binding for that, see
+terminal window. In the `catmux/resources/tmux_default.conf` there is a key-binding for that, see
 `etc/readme_tmux.txt` for details.
 
 ### Tmux server to be used
 By default, catmux spawns its own tmux server called `catmux`. Therefore, a simple
 `tmux list-sessions` (or `tmux ls`) will not list the `catmux` session. To list the `catmux`
 session, use `tmux -L catmux list-sessions`. You can change the server's name by specifying the
 `-L <server_name>` parameter to `catmux_create_session`. That mechanism ensures that the environment
```

### Comparing `catmux-0.3.3/catmux/prefix.py` & `catmux-0.3.4/catmux/prefix.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,12 +1,12 @@
-"""This module provides the installed prefix of the catmux module"""
+"""This module provides the installed prefix of the catmux resources"""
 # -- BEGIN LICENSE BLOCK ----------------------------------------------
 
 # catmux
-# Copyright (C) 2020  Felix Mauch
+# Copyright (C) 2023  Felix Exner
 # MIT License
 #
 # Permission is hereby granted, free of charge, to any person obtaining a copy
 # of this software and associated documentation files (the "Software"), to deal
 # in the Software without restriction, including without limitation the rights
 # to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 # copies of the Software, and to permit persons to whom the Software is
@@ -20,16 +20,25 @@
 # FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
 # AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 # LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 # OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 # SOFTWARE.
 # -- END LICENSE BLOCK ------------------------------------------------
 
+import os
+import sys
+from importlib import resources
+
 
 def get_prefix():
-    """Returns the installed prefix"""
+    """Returns the path of catmux's resource folder"""
+
+    if sys.version_info.major == 3 and sys.version_info.minor == 9:
+        with resources.files("catmux") as path:
+            return os.path.join(path, "resources")
 
-    return __file__.split("lib")[0]
+    with resources.path("catmux", "resources") as path:
+        return path
 
 
 if __name__ == "__main__":
     print(get_prefix())
```

### Comparing `catmux-0.3.3/catmux/session.py` & `catmux-0.3.4/catmux/session.py`

 * *Files 8% similar despite different names*

```diff
@@ -57,32 +57,31 @@
 
     def init_from_filepath(self, filepath):
         """Initializes the data from a file read from filepath."""
 
         try:
             self.__yaml_data = yaml.safe_load(open(filepath, "r"))
         except yaml.YAMLError as exc:
-            print("Error while loading config file: %s", exc)
-            print("Loaded file was: %s", filepath)
+            raise cme.InvalidConfig(
+                f"Config file {filepath} is not a valid yaml file:\n{exc}"
+            )
 
         self.init_from_yaml(self.__yaml_data)
 
     def init_from_yaml(self, yaml_data):
         """Initialize config directly by an already loaded yaml structure."""
 
         self.__yaml_data = yaml_data
         self._parse_common()
         self._parse_parameters()
         self._parse_windows()
 
     def run(self, debug=False):
         """Runs the loaded session"""
-        if len(self._windows) == 0:
-            print("No windows to run found")
-            return
+        assert len(self._windows) > 0
 
         first = True
         for window in self._windows:
             window.create(first)
             if debug:
                 window.debug()
             first = False
@@ -98,20 +97,20 @@
             )
 
     def _parse_common(self):
         if self.__yaml_data is None:
             print("parse_common was called without yaml data loaded.")
             raise RuntimeError
 
-        if "common" in self.__yaml_data:
+        if "common" in self.__yaml_data and self.__yaml_data["common"]:
             common = self.__yaml_data["common"]
-            if "before_commands" in common:
+            if "before_commands" in common and common["before_commands"]:
                 self._before_commands = common["before_commands"]
 
-            if "default_window" in common:
+            if "default_window" in common and common["default_window"]:
                 self._default_window = common["default_window"]
 
     def _parse_overwrites(self, data_string):
         """Separates a comma-separated list of foo=val1,bar=val2 into a dictionary."""
         if data_string is None:
             return None
 
@@ -169,77 +168,68 @@
 
     def _parse_windows(self):
         if self.__yaml_data is None:
             print("parse_windows was called without yaml data loaded.")
             raise RuntimeError
 
         if "windows" in self.__yaml_data:
+            if self.__yaml_data["windows"] is None:
+                raise cme.InvalidConfig("The 'windows' block must not be empty.")
             for window in self.__yaml_data["windows"]:
                 if "if" in window:
                     print("Detected if condition for window " + window["name"])
-                    try:
-                        if_param = self._parameters[window["if"]]
-                        if window["if"] not in self._parameters:
-                            print(
-                                "Skipping window "
-                                + window["name"]
-                                + " because parameter "
-                                + window["if"]
-                                + " was not found."
-                            )
-                            continue
-                        elif not check_boolean_field(if_param):
-                            print(
-                                "Skipping window "
-                                + window["name"]
-                                + " because parameter "
-                                + window["if"]
-                                + " is switched off globally"
-                            )
-                            continue
-                        else:
-                            print(
-                                "condition fulfilled: {} == {}".format(
-                                    window["if"], self._parameters[window["if"]]
-                                )
+                    if window["if"] not in self._parameters:
+                        print(
+                            "Skipping window "
+                            + window["name"]
+                            + " because parameter "
+                            + window["if"]
+                            + " was not found."
+                        )
+                        continue
+                    elif not check_boolean_field(self._parameters[window["if"]]):
+                        print(
+                            "Skipping window "
+                            + window["name"]
+                            + " because parameter "
+                            + window["if"]
+                            + " is switched off globally"
+                        )
+                        continue
+                    else:
+                        print(
+                            "condition fulfilled: {} == {}".format(
+                                window["if"], self._parameters[window["if"]]
                             )
-                    except KeyError:
-                        raise cme.InvalidConfig(
-                            f"Paramater '{window['if']}' not found in parameters."
                         )
                 if "unless" in window:
                     print("Detected unless condition for window " + window["name"])
-                    try:
-                        unless_param = self._parameters[window["unless"]]
 
-                        if check_boolean_field(unless_param):
+                    if window["unless"] in self._parameters:
+                        if check_boolean_field(self._parameters[window["unless"]]):
                             print(
                                 "Skipping window "
                                 + window["name"]
                                 + " because parameter "
                                 + window["unless"]
                                 + " is switched on globally"
                             )
                             continue
                         else:
                             print(
                                 "condition fulfilled: {} == {}".format(
                                     window["unless"], self._parameters[window["unless"]]
                                 )
                             )
-                    except KeyError:
-                        raise cme.InvalidConfig(
-                            f"Paramater '{window['unless']}' not found in parameters."
-                        )
 
                 kwargs = dict()
                 kwargs["before_commands"] = [cmd for cmd in self._before_commands]
 
                 kwargs.update(window)
 
                 print(kwargs)
 
                 self._windows.append(
                     Window(self._server_name, self._session_name, **kwargs)
                 )
         else:
-            print("No window section found in session config")
+            raise cme.InvalidConfig("No window section found in session config")
```

### Comparing `catmux-0.3.3/catmux/split.py` & `catmux-0.3.4/catmux/split.py`

 * *Files identical despite different names*

### Comparing `catmux-0.3.3/catmux/tmux_wrapper.py` & `catmux-0.3.4/catmux/tmux_wrapper.py`

 * *Files identical despite different names*

### Comparing `catmux-0.3.3/catmux/window.py` & `catmux-0.3.4/catmux/window.py`

 * *Files identical despite different names*

### Comparing `catmux-0.3.3/catmux.egg-info/PKG-INFO` & `catmux-0.3.4/catmux.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,20 +1,19 @@
 Metadata-Version: 2.1
 Name: catmux
-Version: 0.3.3
+Version: 0.3.4
 Summary: A tmux orchestration package.
 Home-page: https://github.com/fmauch/catmux
 Author: Felix Exner
 Author-email: felix_mauch@web.de
 License: MIT
-Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
-Requires-Python: >=3.6
+Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Catmux
 [![codecov](https://codecov.io/gh/fmauch/catmux/branch/master/graph/badge.svg?token=bPcdYrOBRK)](https://codecov.io/gh/fmauch/catmux)
 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
 
@@ -50,20 +49,20 @@
 repository's root directory. If you use this option, please be aware that some examples behave
 differently if you have installed catmux this way and are calling it from the repository directory.
 Calling them from outside the directory (e.g. after leaving via `cd`) is fine and should result in
 the same behavior as with the recommended installation method.
 
 ## Usage
 Currently, there is no full-blown documentation, but the example config file in
-`etc/example_session.yaml` gives a detailed insight on possible commands.
+`catmux/resources/example_session.yaml` gives a detailed insight on possible commands.
 
 ### Running the example the most simple way
 After installation, you can run a simple example by calling the following command:
 ```
-catmux_create_session $(python3 -m catmux.prefix)/share/catmux/example_session.yaml
+catmux_create_session $(python3 -m catmux.prefix)/example_session.yaml
 ```
 
 To see further options, simply run it with argument `-h`:
 ```
 $ catmux_create_session -h
 usage: catmux_create_session [-h] [-n SESSION_NAME] [-t TMUX_CONFIG] [-d] [--overwrite OVERWRITE]
                              session_config
@@ -84,23 +83,23 @@
                         Overwrite a parameter from the session config. Parameters can be specified
                         using a comma-separated list such as '--overwrite param_a=1,param_b=2'.
 ```
 
 ### Full blown example
 To make use of all catmux features, run the following example command:
 ```
-catmux_create_session $(python3 -m catmux.prefix)/share/catmux/example_session.yaml \
-  --tmux_config $(python3 -m catmux.prefix)/share/catmux/tmux_default.conf \
+catmux_create_session $(python3 -m catmux.prefix)/example_session.yaml \
+  --tmux_config $(python3 -m catmux.prefix)/tmux_default.conf \
   --session_name example_session \
   --overwrite show_layouts=True,replacement_param="new catmux user"
 ```
 
 ### Killing a catmux session
 If you are not that familiar with tmux: To kill a session, simply type `tmux kill-session` in any
-terminal window. In the `etc/tmux_default.conf` there is a key-binding for that, see
+terminal window. In the `catmux/resources/tmux_default.conf` there is a key-binding for that, see
 `etc/readme_tmux.txt` for details.
 
 ### Tmux server to be used
 By default, catmux spawns its own tmux server called `catmux`. Therefore, a simple
 `tmux list-sessions` (or `tmux ls`) will not list the `catmux` session. To list the `catmux`
 session, use `tmux -L catmux list-sessions`. You can change the server's name by specifying the
 `-L <server_name>` parameter to `catmux_create_session`. That mechanism ensures that the environment
@@ -123,9 +122,7 @@
 For ROS2, the same is achievable with `ros2 pkg prefix` but the yaml has to be installed (similar
 to, for example, a launch file) and the installation path has to be specified:
 ```
 catmux_create_session $(ros2 pkg prefix <your_package_name>)/path/to/the/installed/<your_catmux_session_config.yaml>
 
 # for example: $ catmux_create_session $(ros2 pkg prefix catmux_test_pkg)/share/catmux_test_pkg/catmux_session.yaml
 ```
-
-
```

### Comparing `catmux-0.3.3/etc/example_session.yaml` & `catmux-0.3.4/catmux/example_session.yaml`

 * *Files identical despite different names*

### Comparing `catmux-0.3.3/etc/readme_tmux.txt` & `catmux-0.3.4/catmux/resources/readme_tmux.txt`

 * *Files identical despite different names*

### Comparing `catmux-0.3.3/etc/tmux_default.conf` & `catmux-0.3.4/catmux/resources/tmux_default.conf`

 * *Files identical despite different names*

### Comparing `catmux-0.3.3/script/catmux_create_session` & `catmux-0.3.4/script/catmux_create_session`

 * *Files 18% similar despite different names*

```diff
@@ -28,16 +28,17 @@
 import os
 import logging
 import subprocess
 import sys
 
 import argparse
 
+from importlib import resources
+
 from catmux.session import Session as CatmuxSession
-from catmux.prefix import get_prefix
 import catmux.exceptions
 
 
 def safe_call(cmd_list):
     """Makes a subprocess check_call and outputs a clear error message on failure and then exits"""
     try:
         subprocess.check_output(cmd_list)
@@ -112,16 +113,18 @@
     if args.tmux_config:
         tmux_config = args.tmux_config
     elif os.path.exists(os.path.expanduser("~/.tmux.conf")):
         tmux_config = os.path.expanduser("~/.tmux.conf")
     elif os.path.exists("/etc/tmux.conf"):
         tmux_config = "/etc/tmux.conf"
     else:
-        prefix = get_prefix()
-        tmux_config = os.path.join(prefix, "share", "catmux", "tmux_default.conf")
+        with resources.path(
+            ".".join(["catmux", "resources"]), "tmux_default.conf"
+        ) as catmux_session:
+            tmux_config = catmux_session
 
     print("Using tmux config file: {}".format(tmux_config))
     command += ["-f", tmux_config]
 
     command += ["new-session", "-s", args.session_name]
     command.append("-d")
     print(" ".join(command))
```

