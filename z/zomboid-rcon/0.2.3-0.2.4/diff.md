# Comparing `tmp/zomboid_rcon-0.2.3.tar.gz` & `tmp/zomboid_rcon-0.2.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zomboid_rcon-0.2.3.tar", last modified: Thu Mar 30 09:29:56 2023, max compression
+gzip compressed data, was "zomboid_rcon-0.2.4.tar", last modified: Sun Jul 23 15:42:29 2023, max compression
```

## Comparing `zomboid_rcon-0.2.3.tar` & `zomboid_rcon-0.2.4.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxrwxr-x   0 jackwhitworth  (1000) jackwhitworth  (1000)        0 2023-03-30 09:29:56.245180 zomboid_rcon-0.2.3/
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)    35129 2023-03-30 09:01:17.000000 zomboid_rcon-0.2.3/LICENSE
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)    44033 2023-03-30 09:29:56.245180 zomboid_rcon-0.2.3/PKG-INFO
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)     2670 2023-03-30 09:27:40.000000 zomboid_rcon-0.2.3/README.md
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)     1053 2023-03-30 09:28:59.000000 zomboid_rcon-0.2.3/pyproject.toml
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)       38 2023-03-30 09:29:56.245180 zomboid_rcon-0.2.3/setup.cfg
-drwxrwxr-x   0 jackwhitworth  (1000) jackwhitworth  (1000)        0 2023-03-30 09:29:56.241180 zomboid_rcon-0.2.3/zomboid_rcon/
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)      268 2023-03-30 09:29:30.000000 zomboid_rcon-0.2.3/zomboid_rcon/__init__.py
-drwxrwxr-x   0 jackwhitworth  (1000) jackwhitworth  (1000)        0 2023-03-30 09:29:56.245180 zomboid_rcon-0.2.3/zomboid_rcon/source/
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)     3066 2023-03-30 09:29:30.000000 zomboid_rcon-0.2.3/zomboid_rcon/source/CommandResult.py
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)     2694 2023-03-30 09:29:30.000000 zomboid_rcon-0.2.3/zomboid_rcon/source/RconClient.py
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)      265 2023-03-30 09:29:30.000000 zomboid_rcon-0.2.3/zomboid_rcon/source/__init__.py
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)     1277 2023-03-30 09:29:30.000000 zomboid_rcon-0.2.3/zomboid_rcon/zomboid_rcon.py
-drwxrwxr-x   0 jackwhitworth  (1000) jackwhitworth  (1000)        0 2023-03-30 09:29:56.241180 zomboid_rcon-0.2.3/zomboid_rcon.egg-info/
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)    44033 2023-03-30 09:29:56.000000 zomboid_rcon-0.2.3/zomboid_rcon.egg-info/PKG-INFO
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)      368 2023-03-30 09:29:56.000000 zomboid_rcon-0.2.3/zomboid_rcon.egg-info/SOURCES.txt
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)        1 2023-03-30 09:29:56.000000 zomboid_rcon-0.2.3/zomboid_rcon.egg-info/dependency_links.txt
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)       44 2023-03-30 09:29:56.000000 zomboid_rcon-0.2.3/zomboid_rcon.egg-info/requires.txt
--rw-rw-r--   0 jackwhitworth  (1000) jackwhitworth  (1000)       13 2023-03-30 09:29:56.000000 zomboid_rcon-0.2.3/zomboid_rcon.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/
+-rw-r--r--   0 runner    (1001) docker     (123)    35129 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    44108 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2745 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1053 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/zomboid_rcon/
+-rw-r--r--   0 runner    (1001) docker     (123)      268 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/zomboid_rcon/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/zomboid_rcon/source/
+-rw-r--r--   0 runner    (1001) docker     (123)     3066 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/zomboid_rcon/source/CommandResult.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2695 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/zomboid_rcon/source/RconClient.py
+-rw-r--r--   0 runner    (1001) docker     (123)      265 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/zomboid_rcon/source/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1277 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/zomboid_rcon/zomboid_rcon.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    44108 2023-07-23 15:42:29.000000 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      368 2023-07-23 15:42:29.000000 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 15:42:29.000000 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       44 2023-07-23 15:42:29.000000 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-23 15:42:29.000000 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/top_level.txt
```

### Comparing `zomboid_rcon-0.2.3/LICENSE` & `zomboid_rcon-0.2.4/LICENSE`

 * *Files identical despite different names*

### Comparing `zomboid_rcon-0.2.3/PKG-INFO` & `zomboid_rcon-0.2.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zomboid_rcon
-Version: 0.2.3
+Version: 0.2.4
 Summary: Python class for interacting with Project Zomboid servers using RCON 
 Author-email: Jack Whitworth <jack@jackwhitworth.com>
 License: GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -701,30 +701,30 @@
 
 # Installation
 
 To get started, simply install zomboid-rcon using pip:
 
 ``` pip install zomboid-rcon ```
 
-[Pypi Package.](https://pypi.org/project/zomboid-rcon/)
+[Pypi Package](https://pypi.org/project/zomboid-rcon/) / [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
 
 <br>
 
 # Usage
 
 Using zomboid-rcon is easy. Here's a basic example:
 
 ```python
 from zomboid_rcon import ZomboidRCON
 
 if __name__ == "__main__":
-    pz = ZomboidRCON(ip='localhost', password='myPassword')
+    pz = ZomboidRCON(ip='localhost', port=27015, password='myPassword')
     command = pz.serverMsg("You dead yet?")
     print(command.response)
-    print(command.success)
+    print(command.successful)
 ```
 
 This example connects to a server running on your local machine and sends the message "You dead yet?".
 
 Zomboid-rcon provides several built-in methods for common server management tasks, such as getting a list of connected players:
 
 ```python
```

### Comparing `zomboid_rcon-0.2.3/README.md` & `zomboid_rcon-0.2.4/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -6,30 +6,30 @@
 
 # Installation
 
 To get started, simply install zomboid-rcon using pip:
 
 ``` pip install zomboid-rcon ```
 
-[Pypi Package.](https://pypi.org/project/zomboid-rcon/)
+[Pypi Package](https://pypi.org/project/zomboid-rcon/) / [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
 
 <br>
 
 # Usage
 
 Using zomboid-rcon is easy. Here's a basic example:
 
 ```python
 from zomboid_rcon import ZomboidRCON
 
 if __name__ == "__main__":
-    pz = ZomboidRCON(ip='localhost', password='myPassword')
+    pz = ZomboidRCON(ip='localhost', port=27015, password='myPassword')
     command = pz.serverMsg("You dead yet?")
     print(command.response)
-    print(command.success)
+    print(command.successful)
 ```
 
 This example connects to a server running on your local machine and sends the message "You dead yet?".
 
 Zomboid-rcon provides several built-in methods for common server management tasks, such as getting a list of connected players:
 
 ```python
```

### Comparing `zomboid_rcon-0.2.3/pyproject.toml` & `zomboid_rcon-0.2.4/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "zomboid_rcon"
-version = "0.2.3"
+version = "0.2.4"
 description = "Python class for interacting with Project Zomboid servers using RCON "
 readme = "README.md"
 license = { file = "LICENSE" }
 authors = [{ name = "Jack Whitworth", email = "jack@jackwhitworth.com" }]
 classifiers = [
     'Development Status :: 4 - Beta',
     'Intended Audience :: Developers',
```

### Comparing `zomboid_rcon-0.2.3/zomboid_rcon/source/CommandResult.py` & `zomboid_rcon-0.2.4/zomboid_rcon/source/CommandResult.py`

 * *Files identical despite different names*

### Comparing `zomboid_rcon-0.2.3/zomboid_rcon/source/RconClient.py` & `zomboid_rcon-0.2.4/zomboid_rcon/source/RconClient.py`

 * *Files 1% similar despite different names*

```diff
@@ -58,15 +58,15 @@
                 tries += 1
         return CommandResult(
             command = command,
             successful = False,
             response = f"Session timed out (after {self._retries} attempt(s))"
             )
     
-    @timeout(5)
+    @timeout(10)
     def _command(self, command:str, *args) -> str:
         """ Private method to handle timeouts """
         try:
             with self.createClient() as client:
                 return client.run(command, *args)
         except ConnectionRefusedError:
             return "Connection refused"
```

### Comparing `zomboid_rcon-0.2.3/zomboid_rcon/zomboid_rcon.py` & `zomboid_rcon-0.2.4/zomboid_rcon/zomboid_rcon.py`

 * *Files identical despite different names*

### Comparing `zomboid_rcon-0.2.3/zomboid_rcon.egg-info/PKG-INFO` & `zomboid_rcon-0.2.4/zomboid_rcon.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zomboid-rcon
-Version: 0.2.3
+Version: 0.2.4
 Summary: Python class for interacting with Project Zomboid servers using RCON 
 Author-email: Jack Whitworth <jack@jackwhitworth.com>
 License: GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -701,30 +701,30 @@
 
 # Installation
 
 To get started, simply install zomboid-rcon using pip:
 
 ``` pip install zomboid-rcon ```
 
-[Pypi Package.](https://pypi.org/project/zomboid-rcon/)
+[Pypi Package](https://pypi.org/project/zomboid-rcon/) / [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
 
 <br>
 
 # Usage
 
 Using zomboid-rcon is easy. Here's a basic example:
 
 ```python
 from zomboid_rcon import ZomboidRCON
 
 if __name__ == "__main__":
-    pz = ZomboidRCON(ip='localhost', password='myPassword')
+    pz = ZomboidRCON(ip='localhost', port=27015, password='myPassword')
     command = pz.serverMsg("You dead yet?")
     print(command.response)
-    print(command.success)
+    print(command.successful)
 ```
 
 This example connects to a server running on your local machine and sends the message "You dead yet?".
 
 Zomboid-rcon provides several built-in methods for common server management tasks, such as getting a list of connected players:
 
 ```python
```

