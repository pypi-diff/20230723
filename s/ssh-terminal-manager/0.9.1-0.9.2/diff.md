# Comparing `tmp/ssh_terminal_manager-0.9.1.tar.gz` & `tmp/ssh_terminal_manager-0.9.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ssh_terminal_manager-0.9.1.tar", last modified: Sun Jul 23 03:25:28 2023, max compression
+gzip compressed data, was "ssh_terminal_manager-0.9.2.tar", last modified: Sun Jul 23 08:09:34 2023, max compression
```

## Comparing `ssh_terminal_manager-0.9.1.tar` & `ssh_terminal_manager-0.9.2.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 03:25:28.583340 ssh_terminal_manager-0.9.1/
--rw-rw-r--   0 adrian    (1000) adrian    (1000)     1063 2023-07-11 04:42:39.000000 ssh_terminal_manager-0.9.1/LICENSE
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      864 2023-07-23 03:25:28.579340 ssh_terminal_manager-0.9.1/PKG-INFO
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      223 2023-07-11 04:42:39.000000 ssh_terminal_manager-0.9.1/README.md
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      874 2023-07-23 03:22:55.000000 ssh_terminal_manager-0.9.1/pyproject.toml
--rw-rw-r--   0 adrian    (1000) adrian    (1000)       38 2023-07-23 03:25:28.583340 ssh_terminal_manager-0.9.1/setup.cfg
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 03:25:28.575340 ssh_terminal_manager-0.9.1/src/
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 03:25:28.579340 ssh_terminal_manager-0.9.1/src/ssh_terminal_manager/
--rw-r--r--   0 adrian    (1000) adrian    (1000)     8859 2023-07-22 10:32:33.000000 ssh_terminal_manager-0.9.1/src/ssh_terminal_manager/__init__.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)      393 2023-07-22 10:32:33.000000 ssh_terminal_manager-0.9.1/src/ssh_terminal_manager/errors.py
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 03:25:28.579340 ssh_terminal_manager-0.9.1/src/ssh_terminal_manager.egg-info/
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      864 2023-07-23 03:25:28.000000 ssh_terminal_manager-0.9.1/src/ssh_terminal_manager.egg-info/PKG-INFO
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      343 2023-07-23 03:25:28.000000 ssh_terminal_manager-0.9.1/src/ssh_terminal_manager.egg-info/SOURCES.txt
--rw-rw-r--   0 adrian    (1000) adrian    (1000)        1 2023-07-23 03:25:28.000000 ssh_terminal_manager-0.9.1/src/ssh_terminal_manager.egg-info/dependency_links.txt
--rw-rw-r--   0 adrian    (1000) adrian    (1000)       70 2023-07-23 03:25:28.000000 ssh_terminal_manager-0.9.1/src/ssh_terminal_manager.egg-info/requires.txt
--rw-rw-r--   0 adrian    (1000) adrian    (1000)       21 2023-07-23 03:25:28.000000 ssh_terminal_manager-0.9.1/src/ssh_terminal_manager.egg-info/top_level.txt
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 08:09:34.449744 ssh_terminal_manager-0.9.2/
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)     1063 2023-07-11 04:42:39.000000 ssh_terminal_manager-0.9.2/LICENSE
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      864 2023-07-23 08:09:34.449744 ssh_terminal_manager-0.9.2/PKG-INFO
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      223 2023-07-11 04:42:39.000000 ssh_terminal_manager-0.9.2/README.md
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      874 2023-07-23 08:09:05.000000 ssh_terminal_manager-0.9.2/pyproject.toml
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)       38 2023-07-23 08:09:34.449744 ssh_terminal_manager-0.9.2/setup.cfg
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 08:09:34.445745 ssh_terminal_manager-0.9.2/src/
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 08:09:34.445745 ssh_terminal_manager-0.9.2/src/ssh_terminal_manager/
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     8859 2023-07-23 04:56:11.000000 ssh_terminal_manager-0.9.2/src/ssh_terminal_manager/__init__.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)      393 2023-07-23 04:56:11.000000 ssh_terminal_manager-0.9.2/src/ssh_terminal_manager/errors.py
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 08:09:34.449744 ssh_terminal_manager-0.9.2/src/ssh_terminal_manager.egg-info/
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      864 2023-07-23 08:09:34.000000 ssh_terminal_manager-0.9.2/src/ssh_terminal_manager.egg-info/PKG-INFO
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      343 2023-07-23 08:09:34.000000 ssh_terminal_manager-0.9.2/src/ssh_terminal_manager.egg-info/SOURCES.txt
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)        1 2023-07-23 08:09:34.000000 ssh_terminal_manager-0.9.2/src/ssh_terminal_manager.egg-info/dependency_links.txt
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)       70 2023-07-23 08:09:34.000000 ssh_terminal_manager-0.9.2/src/ssh_terminal_manager.egg-info/requires.txt
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)       21 2023-07-23 08:09:34.000000 ssh_terminal_manager-0.9.2/src/ssh_terminal_manager.egg-info/top_level.txt
```

### Comparing `ssh_terminal_manager-0.9.1/LICENSE` & `ssh_terminal_manager-0.9.2/LICENSE`

 * *Files identical despite different names*

### Comparing `ssh_terminal_manager-0.9.1/PKG-INFO` & `ssh_terminal_manager-0.9.2/src/ssh_terminal_manager.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: ssh_terminal_manager
-Version: 0.9.1
+Name: ssh-terminal-manager
+Version: 0.9.2
 Summary: Use terminal commands to control and monitor remote devices
 Author-email: zhbjsh <zhbjsh@outlook.com>
 Project-URL: Homepage, https://github.com/zhbjsh/ssh-terminal-manager
 Project-URL: Bug Tracker, https://github.com/zhbjsh/ssh-terminal-manager/issues
 Keywords: ssh,terminal,console,shell,bash,cmd,power shell,commands,command line
 Classifier: Programming Language :: Python :: 3.10
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `ssh_terminal_manager-0.9.1/pyproject.toml` & `ssh_terminal_manager-0.9.2/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "ssh_terminal_manager"
-version = "0.9.1"
+version = "0.9.2"
 authors = [
   { name="zhbjsh", email="zhbjsh@outlook.com" },
 ]
 description = "Use terminal commands to control and monitor remote devices"
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers = [
@@ -26,14 +26,14 @@
   "power shell",
   "commands",
   "command line"
 ]
 dependencies = [
   "icmplib >= 3.0",
   "paramiko >= 3.2.0",
-  "terminal-manager >= 0.9.1",
+  "terminal-manager >= 0.9.2",
   "wakeonlan >= 3.0.0"
 ]
 
 [project.urls]
 "Homepage" = "https://github.com/zhbjsh/ssh-terminal-manager"
 "Bug Tracker" = "https://github.com/zhbjsh/ssh-terminal-manager/issues"
```

### Comparing `ssh_terminal_manager-0.9.1/src/ssh_terminal_manager/__init__.py` & `ssh_terminal_manager-0.9.2/src/ssh_terminal_manager/__init__.py`

 * *Files identical despite different names*

### Comparing `ssh_terminal_manager-0.9.1/src/ssh_terminal_manager.egg-info/PKG-INFO` & `ssh_terminal_manager-0.9.2/PKG-INFO`

 * *Files 27% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: ssh-terminal-manager
-Version: 0.9.1
+Name: ssh_terminal_manager
+Version: 0.9.2
 Summary: Use terminal commands to control and monitor remote devices
 Author-email: zhbjsh <zhbjsh@outlook.com>
 Project-URL: Homepage, https://github.com/zhbjsh/ssh-terminal-manager
 Project-URL: Bug Tracker, https://github.com/zhbjsh/ssh-terminal-manager/issues
 Keywords: ssh,terminal,console,shell,bash,cmd,power shell,commands,command line
 Classifier: Programming Language :: Python :: 3.10
 Classifier: License :: OSI Approved :: MIT License
```

