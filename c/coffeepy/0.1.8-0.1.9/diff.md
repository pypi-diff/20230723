# Comparing `tmp/coffeepy-0.1.8.tar.gz` & `tmp/coffeepy-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "coffeepy-0.1.8.tar", last modified: Fri Jul 21 22:52:00 2023, max compression
+gzip compressed data, was "coffeepy-0.1.9.tar", last modified: Sun Jul 23 13:05:43 2023, max compression
```

## Comparing `coffeepy-0.1.8.tar` & `coffeepy-0.1.9.tar`

### file list

```diff
@@ -1,18 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 22:52:00.437009 coffeepy-0.1.8/
--rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-07-21 22:51:50.000000 coffeepy-0.1.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2312 2023-07-21 22:52:00.437009 coffeepy-0.1.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-07-21 22:51:50.000000 coffeepy-0.1.8/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      862 2023-07-21 22:51:50.000000 coffeepy-0.1.8/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-21 22:52:00.437009 coffeepy-0.1.8/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 22:52:00.433009 coffeepy-0.1.8/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 22:52:00.437009 coffeepy-0.1.8/src/coffeepy/
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-21 22:51:50.000000 coffeepy-0.1.8/src/coffeepy/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4267 2023-07-21 22:51:50.000000 coffeepy-0.1.8/src/coffeepy/coffeepy.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 22:52:00.437009 coffeepy-0.1.8/src/coffeepy.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2312 2023-07-21 22:52:00.000000 coffeepy-0.1.8/src/coffeepy.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      288 2023-07-21 22:52:00.000000 coffeepy-0.1.8/src/coffeepy.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-21 22:52:00.000000 coffeepy-0.1.8/src/coffeepy.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-21 22:52:00.000000 coffeepy-0.1.8/src/coffeepy.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-21 22:52:00.000000 coffeepy-0.1.8/src/coffeepy.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 22:52:00.437009 coffeepy-0.1.8/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     5557 2023-07-21 22:51:50.000000 coffeepy-0.1.8/tests/test_coffeepy.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:05:43.621141 coffeepy-0.1.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-07-23 13:05:32.000000 coffeepy-0.1.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3697 2023-07-23 13:05:43.621141 coffeepy-0.1.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-07-23 13:05:32.000000 coffeepy-0.1.9/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1049 2023-07-23 13:05:32.000000 coffeepy-0.1.9/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 13:05:43.621141 coffeepy-0.1.9/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:05:43.617141 coffeepy-0.1.9/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:05:43.617141 coffeepy-0.1.9/src/coffeepy/
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 13:05:32.000000 coffeepy-0.1.9/src/coffeepy/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5767 2023-07-23 13:05:32.000000 coffeepy-0.1.9/src/coffeepy/coffeepy.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:05:43.621141 coffeepy-0.1.9/src/coffeepy.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3697 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      323 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:05:43.621141 coffeepy-0.1.9/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     6333 2023-07-23 13:05:32.000000 coffeepy-0.1.9/tests/test_coffeepy.py
```

### Comparing `coffeepy-0.1.8/LICENSE` & `coffeepy-0.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `coffeepy-0.1.8/PKG-INFO` & `coffeepy-0.1.9/README.md`

 * *Files 16% similar despite different names*

```diff
@@ -1,26 +1,7 @@
-Metadata-Version: 2.1
-Name: coffeepy
-Version: 0.1.8
-Summary: Coffeepy prevents the system from sleeping
-Author-email: kuvaus <coffeepy@kuvaus.org>
-Project-URL: Homepage, https://github.com/kuvaus/coffeepy
-Project-URL: Bug Tracker, https://github.com/kuvaus/coffeepy/issues
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Operating System :: OS Independent
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
 [![Supported Python versions](https://img.shields.io/pypi/pyversions/coffeepy.svg?style=flat)](https://pypi.python.org/pypi/coffeepy/) [![PyPI Version](https://img.shields.io/pypi/v/coffeepy.svg)](https://pypi.python.org/pypi/coffeepy)
 # Coffeepy
 
 Coffeepy ☕️ is a small program that prevents the system from sleeping.
 Works on MacOS, Windows and Linux.
 
 <img alt="coffeepy" src="https://github-production-user-asset-6210df.s3.amazonaws.com/22169537/253075028-9eaccaca-a567-4bd8-86c1-63d4870664ad.gif" width="600" />
```

### Comparing `coffeepy-0.1.8/pyproject.toml` & `coffeepy-0.1.9/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,22 +1,29 @@
 
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "coffeepy"
-version = "0.1.8"
+version = "0.1.9"
 authors = [
   { name="kuvaus", email="coffeepy@kuvaus.org" },
 ]
+dependencies = [
+    "jeepney"
+]
 description = "Coffeepy prevents the system from sleeping"
 readme = "README.md"
+license = { file = "LICENSE"}
 requires-python = ">=3.7"
 classifiers = [
+    "Operating System :: MacOS",
+    "Operating System :: Microsoft :: Windows",
+    "Operating System :: POSIX :: Linux",
     "Programming Language :: Python :: 3",
     "Programming Language :: Python :: 3.7",
     "Programming Language :: Python :: 3.8",
     "Programming Language :: Python :: 3.9",
     "Programming Language :: Python :: 3.10",
     "Programming Language :: Python :: 3.11",
     "License :: OSI Approved :: MIT License",
@@ -26,7 +33,8 @@
 [project.scripts]
 coffeepy = "coffeepy.coffeepy:run"
 
 [project.urls]
 "Homepage" = "https://github.com/kuvaus/coffeepy"
 "Bug Tracker" = "https://github.com/kuvaus/coffeepy/issues"
 
+
```

### Comparing `coffeepy-0.1.8/src/coffeepy/coffeepy.py` & `coffeepy-0.1.9/src/coffeepy/coffeepy.py`

 * *Files 26% similar despite different names*

```diff
@@ -4,14 +4,17 @@
 import ctypes
 import sys
 import subprocess
 import time
 import argparse
 import os
 import warnings
+import jeepney
+from jeepney.io.blocking import open_dbus_connection
+
 
 animation = [
     "  ☕️   ",
     " ☁️☕️   ",
     "  ☕️   ",
     "  ☕️☁️  ",
     " ☁️☕️   ",
@@ -36,36 +39,67 @@
         return version(package)
     else:
         with warnings.catch_warnings():
             warnings.filterwarnings("ignore", category=DeprecationWarning)
             import pkg_resources
             return pkg_resources.get_distribution(package).version
 
+
+# On macOS check caffeinate
 def check_caffeinate():
     try:
         subprocess.check_output(['which', 'caffeinate'])
         return True
     except subprocess.CalledProcessError:
         return False
 
-def check_x11():
-    try:
-        subprocess.check_output(['which', 'xset'])
-        return True
-    except subprocess.CalledProcessError:
-        print("You need to install either \'caffeinate\' or \'x11-xserver-utils\' package for this program to run")
-        return False
-
-
+# On Windows check if we use Windows Terminal
 def check_windows_terminal():
     if ('win32' in sys.platform) and (os.environ.get("WT_SESSION") is not None):
         return True
     else:
         return False
 
+# On Linux use jeepney
+def get_connection():
+    try:
+        connection = open_dbus_connection(bus="SESSION")
+    except Exception as e:
+        print("Could not set DBUS SESSION")
+        connection = None
+    return connection
+
+proxy = jeepney.DBusAddress('/org/freedesktop/ScreenSaver', bus_name='org.freedesktop.ScreenSaver', interface='org.freedesktop.ScreenSaver')
+
+def set_dbus_awake(connection):
+    msg = jeepney.new_method_call(proxy, "Inhibit", "ss", ("coffeepy", "wakelock active"))
+    reply = connection.send_and_get_reply(msg)
+    cookie = reply.body[0]
+    return cookie
+
+def unset_dbus_awake(connection, cookie):
+    if cookie is None:
+        return
+    else:
+        msg = jeepney.new_method_call(proxy, "UnInhibit", "u", (cookie,))
+        connection.send_and_get_reply(msg)
+
+def set_systemd_mask():
+    print("Trying with systemd (this will need sudo permissions)")
+    result = subprocess.run(["systemctl", "mask", "sleep.target", "suspend.target", "hibernate.target", "hybrid-sleep.target"])
+    if result.returncode != 0:
+        print("Systemd failed.")
+        sys.exit(0)
+        
+def unset_systemd_mask():
+    result = subprocess.run(["systemctl", "unmask", "sleep.target", "suspend.target", "hibernate.target", "hybrid-sleep.target"])
+    if result.returncode != 0:
+        print("Systemd failed.")
+        sys.exit(0)
+        
 def parse_args(args=None):
 
     coffee_emoji = "☕️"
     if 'win32' in sys.platform and not check_windows_terminal():
         coffee_emoji = ""
 
     description = 'Coffeepy (v'+get_version('coffeepy')+') '+coffee_emoji+""" prevents the system from sleeping.
@@ -100,19 +134,24 @@
         print('Running \'coffeepy\' on MacOS to prevent the system from sleeping')
         proc = subprocess.Popen(['caffeinate', '-dims'])
 
     elif 'linux' in sys.platform:
         print('Running \'coffeepy\' on Linux to prevent the system from sleeping')
         if check_caffeinate():
             proc = subprocess.Popen(['caffeinate', '-dims'])
-        elif check_x11():
-            subprocess.Popen(['xset', 's', 'off'])
-            subprocess.Popen(['xset', '-dpms'])
         else:
-            sys.exit(0)
+            # Check for DBUS
+            connection = get_connection()
+            if connection is not None:
+            # Keep system awake using DBUS
+                cookie = set_dbus_awake(connection)
+            else:
+                print("You need to install either \'dbus\' or \'caffeinate\' package for this program to run")
+                set_systemd_mask()
+
 
     elif 'win32' in sys.platform:
         print('Running \'coffeepy\' on Windows to prevent the system from sleeping')
         ctypes.windll.kernel32.SetThreadExecutionState(0x80000002)
 
     print('Press Ctrl-C to quit')
     
@@ -130,16 +169,18 @@
     except KeyboardInterrupt:
         print('\nExiting')
 
     finally:
         if proc:
             proc.terminate()
         if 'linux' in sys.platform and not check_caffeinate():
-            # Reset xset settings
-            subprocess.Popen(['xset', 's', 'on'])
-            subprocess.Popen(['xset', '+dpms'])
+            if connection is not None:
+                # Reset DBUS connection
+                unset_dbus_awake(connection, cookie)
+            else:
+                unset_systemd_mask()
         if 'win32' in sys.platform:
             ctypes.windll.kernel32.SetThreadExecutionState(0x80000000)
 
 
 if __name__ == "__main__":
     run()
```

