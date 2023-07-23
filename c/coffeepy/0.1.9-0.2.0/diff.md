# Comparing `tmp/coffeepy-0.1.9.tar.gz` & `tmp/coffeepy-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "coffeepy-0.1.9.tar", last modified: Sun Jul 23 13:05:43 2023, max compression
+gzip compressed data, was "coffeepy-0.2.0.tar", last modified: Sun Jul 23 14:14:27 2023, max compression
```

## Comparing `coffeepy-0.1.9.tar` & `coffeepy-0.2.0.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:05:43.621141 coffeepy-0.1.9/
--rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-07-23 13:05:32.000000 coffeepy-0.1.9/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     3697 2023-07-23 13:05:43.621141 coffeepy-0.1.9/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-07-23 13:05:32.000000 coffeepy-0.1.9/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     1049 2023-07-23 13:05:32.000000 coffeepy-0.1.9/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 13:05:43.621141 coffeepy-0.1.9/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:05:43.617141 coffeepy-0.1.9/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:05:43.617141 coffeepy-0.1.9/src/coffeepy/
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 13:05:32.000000 coffeepy-0.1.9/src/coffeepy/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5767 2023-07-23 13:05:32.000000 coffeepy-0.1.9/src/coffeepy/coffeepy.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:05:43.621141 coffeepy-0.1.9/src/coffeepy.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3697 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      323 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 13:05:43.000000 coffeepy-0.1.9/src/coffeepy.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:05:43.621141 coffeepy-0.1.9/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     6333 2023-07-23 13:05:32.000000 coffeepy-0.1.9/tests/test_coffeepy.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:14:27.867357 coffeepy-0.2.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-07-23 14:14:16.000000 coffeepy-0.2.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2450 2023-07-23 14:14:27.867357 coffeepy-0.2.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-07-23 14:14:16.000000 coffeepy-0.2.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1041 2023-07-23 14:14:16.000000 coffeepy-0.2.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 14:14:27.867357 coffeepy-0.2.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:14:27.867357 coffeepy-0.2.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:14:27.867357 coffeepy-0.2.0/src/coffeepy/
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 14:14:16.000000 coffeepy-0.2.0/src/coffeepy/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6111 2023-07-23 14:14:16.000000 coffeepy-0.2.0/src/coffeepy/coffeepy.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:14:27.867357 coffeepy-0.2.0/src/coffeepy.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2450 2023-07-23 14:14:27.000000 coffeepy-0.2.0/src/coffeepy.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      323 2023-07-23 14:14:27.000000 coffeepy-0.2.0/src/coffeepy.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 14:14:27.000000 coffeepy-0.2.0/src/coffeepy.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-23 14:14:27.000000 coffeepy-0.2.0/src/coffeepy.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       36 2023-07-23 14:14:27.000000 coffeepy-0.2.0/src/coffeepy.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 14:14:27.000000 coffeepy-0.2.0/src/coffeepy.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:14:27.867357 coffeepy-0.2.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     4170 2023-07-23 14:14:16.000000 coffeepy-0.2.0/tests/test_coffeepy.py
```

### Comparing `coffeepy-0.1.9/LICENSE` & `coffeepy-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `coffeepy-0.1.9/README.md` & `coffeepy-0.2.0/README.md`

 * *Files identical despite different names*

### Comparing `coffeepy-0.1.9/pyproject.toml` & `coffeepy-0.2.0/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,37 +1,36 @@
 
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "coffeepy"
-version = "0.1.9"
+version = "0.2.0"
 authors = [
   { name="kuvaus", email="coffeepy@kuvaus.org" },
 ]
 dependencies = [
-    "jeepney"
+    "jeepney;sys_platform=='linux'"
 ]
 description = "Coffeepy prevents the system from sleeping"
 readme = "README.md"
-license = { file = "LICENSE"}
 requires-python = ">=3.7"
 classifiers = [
     "Operating System :: MacOS",
     "Operating System :: Microsoft :: Windows",
     "Operating System :: POSIX :: Linux",
+    "Operating System :: OS Independent",
     "Programming Language :: Python :: 3",
     "Programming Language :: Python :: 3.7",
     "Programming Language :: Python :: 3.8",
     "Programming Language :: Python :: 3.9",
     "Programming Language :: Python :: 3.10",
     "Programming Language :: Python :: 3.11",
     "License :: OSI Approved :: MIT License",
-    "Operating System :: OS Independent",
 ]
 
 [project.scripts]
 coffeepy = "coffeepy.coffeepy:run"
 
 [project.urls]
 "Homepage" = "https://github.com/kuvaus/coffeepy"
```

### Comparing `coffeepy-0.1.9/src/coffeepy/coffeepy.py` & `coffeepy-0.2.0/src/coffeepy/coffeepy.py`

 * *Files 4% similar despite different names*

```diff
@@ -4,17 +4,18 @@
 import ctypes
 import sys
 import subprocess
 import time
 import argparse
 import os
 import warnings
-import jeepney
-from jeepney.io.blocking import open_dbus_connection
 
+if 'linux' in sys.platform:
+    import jeepney
+    from jeepney.io.blocking import open_dbus_connection
 
 animation = [
     "  ☕️   ",
     " ☁️☕️   ",
     "  ☕️   ",
     "  ☕️☁️  ",
     " ☁️☕️   ",
@@ -55,51 +56,53 @@
 # On Windows check if we use Windows Terminal
 def check_windows_terminal():
     if ('win32' in sys.platform) and (os.environ.get("WT_SESSION") is not None):
         return True
     else:
         return False
 
-# On Linux use jeepney
+# On Linux use DBUS
 def get_connection():
     try:
         connection = open_dbus_connection(bus="SESSION")
     except Exception as e:
         print("Could not set DBUS SESSION")
         connection = None
     return connection
 
-proxy = jeepney.DBusAddress('/org/freedesktop/ScreenSaver', bus_name='org.freedesktop.ScreenSaver', interface='org.freedesktop.ScreenSaver')
-
 def set_dbus_awake(connection):
+    proxy = jeepney.DBusAddress('/org/freedesktop/ScreenSaver', bus_name='org.freedesktop.ScreenSaver', interface='org.freedesktop.ScreenSaver')
     msg = jeepney.new_method_call(proxy, "Inhibit", "ss", ("coffeepy", "wakelock active"))
     reply = connection.send_and_get_reply(msg)
     cookie = reply.body[0]
     return cookie
 
 def unset_dbus_awake(connection, cookie):
     if cookie is None:
         return
     else:
+        proxy = jeepney.DBusAddress('/org/freedesktop/ScreenSaver', bus_name='org.freedesktop.ScreenSaver', interface='org.freedesktop.ScreenSaver')
         msg = jeepney.new_method_call(proxy, "UnInhibit", "u", (cookie,))
         connection.send_and_get_reply(msg)
 
+# On Linux use systemd if DBUS fails
 def set_systemd_mask():
     print("Trying with systemd (this will need sudo permissions)")
     result = subprocess.run(["systemctl", "mask", "sleep.target", "suspend.target", "hibernate.target", "hybrid-sleep.target"])
     if result.returncode != 0:
         print("Systemd failed.")
         sys.exit(0)
         
 def unset_systemd_mask():
     result = subprocess.run(["systemctl", "unmask", "sleep.target", "suspend.target", "hibernate.target", "hybrid-sleep.target"])
     if result.returncode != 0:
         print("Systemd failed.")
         sys.exit(0)
-        
+
+# Parse CLI arguments
 def parse_args(args=None):
 
     coffee_emoji = "☕️"
     if 'win32' in sys.platform and not check_windows_terminal():
         coffee_emoji = ""
 
     description = 'Coffeepy (v'+get_version('coffeepy')+') '+coffee_emoji+""" prevents the system from sleeping.
@@ -125,14 +128,15 @@
         
     if args.time == 0:
         duration = float('inf')  # Set duration to infinity
     else:
         duration = args.time * 60  # Convert minutes to seconds
 
     proc = None
+    connection = None
 
     if 'darwin' in sys.platform:
         print('Running \'coffeepy\' on MacOS to prevent the system from sleeping')
         proc = subprocess.Popen(['caffeinate', '-dims'])
 
     elif 'linux' in sys.platform:
         print('Running \'coffeepy\' on Linux to prevent the system from sleeping')
@@ -141,14 +145,15 @@
         else:
             # Check for DBUS
             connection = get_connection()
             if connection is not None:
             # Keep system awake using DBUS
                 cookie = set_dbus_awake(connection)
             else:
+            # Keep system awake using systemd
                 print("You need to install either \'dbus\' or \'caffeinate\' package for this program to run")
                 set_systemd_mask()
 
 
     elif 'win32' in sys.platform:
         print('Running \'coffeepy\' on Windows to prevent the system from sleeping')
         ctypes.windll.kernel32.SetThreadExecutionState(0x80000002)
@@ -173,14 +178,15 @@
         if proc:
             proc.terminate()
         if 'linux' in sys.platform and not check_caffeinate():
             if connection is not None:
                 # Reset DBUS connection
                 unset_dbus_awake(connection, cookie)
             else:
+                # Reset systemd changes
                 unset_systemd_mask()
         if 'win32' in sys.platform:
             ctypes.windll.kernel32.SetThreadExecutionState(0x80000000)
 
 
 if __name__ == "__main__":
     run()
```

