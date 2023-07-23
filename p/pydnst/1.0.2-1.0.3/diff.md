# Comparing `tmp/pydnst-1.0.2.tar.gz` & `tmp/pydnst-1.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pydnst-1.0.2.tar", last modified: Sat Jul 22 12:44:38 2023, max compression
+gzip compressed data, was "pydnst-1.0.3.tar", last modified: Sat Jul 22 21:17:19 2023, max compression
```

## Comparing `pydnst-1.0.2.tar` & `pydnst-1.0.3.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-07-22 12:44:38.986441 pydnst-1.0.2/
--rw-r--r--   0 mm        (1000) mm        (1000)    11357 2020-06-11 21:16:01.000000 pydnst-1.0.2/LICENSE
--rw-rw-r--   0 mm        (1000) mm        (1000)     3319 2023-07-22 12:44:38.986441 pydnst-1.0.2/PKG-INFO
--rw-rw-r--   0 mm        (1000) mm        (1000)     2717 2023-07-22 12:42:38.000000 pydnst-1.0.2/README.md
-drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-07-22 12:44:38.986441 pydnst-1.0.2/pydnst/
--rw-rw-r--   0 mm        (1000) mm        (1000)      721 2023-07-22 10:08:44.000000 pydnst-1.0.2/pydnst/__init__.py
--rw-rw-r--   0 mm        (1000) mm        (1000)     3903 2023-07-22 11:17:11.000000 pydnst-1.0.2/pydnst/__main__.py
--rw-rw-rw-   0 mm        (1000) mm        (1000)    22237 2023-07-22 11:01:33.000000 pydnst-1.0.2/pydnst/client.py
--rw-rw-r--   0 mm        (1000) mm        (1000)     4604 2023-07-22 10:48:50.000000 pydnst-1.0.2/pydnst/commander.py
--rw-rw-r--   0 mm        (1000) mm        (1000)     2569 2022-11-10 10:54:29.000000 pydnst-1.0.2/pydnst/helpers.py
--rw-rw-r--   0 mm        (1000) mm        (1000)    12506 2023-07-22 09:55:25.000000 pydnst-1.0.2/pydnst/message.py
--rw-rw-r--   0 mm        (1000) mm        (1000)    27310 2023-07-22 10:48:27.000000 pydnst-1.0.2/pydnst/server.py
-drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-07-22 12:44:38.986441 pydnst-1.0.2/pydnst.egg-info/
--rw-rw-r--   0 mm        (1000) mm        (1000)     3319 2023-07-22 12:44:38.000000 pydnst-1.0.2/pydnst.egg-info/PKG-INFO
--rw-rw-r--   0 mm        (1000) mm        (1000)      303 2023-07-22 12:44:38.000000 pydnst-1.0.2/pydnst.egg-info/SOURCES.txt
--rw-rw-r--   0 mm        (1000) mm        (1000)        1 2023-07-22 12:44:38.000000 pydnst-1.0.2/pydnst.egg-info/dependency_links.txt
--rw-rw-r--   0 mm        (1000) mm        (1000)       36 2023-07-22 12:44:38.000000 pydnst-1.0.2/pydnst.egg-info/requires.txt
--rw-rw-r--   0 mm        (1000) mm        (1000)        7 2023-07-22 12:44:38.000000 pydnst-1.0.2/pydnst.egg-info/top_level.txt
--rw-rw-r--   0 mm        (1000) mm        (1000)       38 2023-07-22 12:44:38.986441 pydnst-1.0.2/setup.cfg
--rw-rw-r--   0 mm        (1000) mm        (1000)     6865 2023-07-22 12:42:51.000000 pydnst-1.0.2/setup.py
+drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-07-22 21:17:19.587303 pydnst-1.0.3/
+-rw-r--r--   0 mm        (1000) mm        (1000)    11357 2020-06-11 21:16:01.000000 pydnst-1.0.3/LICENSE
+-rw-rw-r--   0 mm        (1000) mm        (1000)     3419 2023-07-22 21:17:19.587303 pydnst-1.0.3/PKG-INFO
+-rw-rw-r--   0 mm        (1000) mm        (1000)     2817 2023-07-22 21:05:21.000000 pydnst-1.0.3/README.md
+drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-07-22 21:17:19.587303 pydnst-1.0.3/pydnst/
+-rw-rw-r--   0 mm        (1000) mm        (1000)      721 2023-07-22 10:08:44.000000 pydnst-1.0.3/pydnst/__init__.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)     3903 2023-07-22 11:17:11.000000 pydnst-1.0.3/pydnst/__main__.py
+-rw-rw-rw-   0 mm        (1000) mm        (1000)    22237 2023-07-22 11:01:33.000000 pydnst-1.0.3/pydnst/client.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)     4604 2023-07-22 10:48:50.000000 pydnst-1.0.3/pydnst/commander.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)     2569 2022-11-10 10:54:29.000000 pydnst-1.0.3/pydnst/helpers.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)    12506 2023-07-22 09:55:25.000000 pydnst-1.0.3/pydnst/message.py
+-rw-rw-r--   0 mm        (1000) mm        (1000)    27310 2023-07-22 10:48:27.000000 pydnst-1.0.3/pydnst/server.py
+drwxrwxr-x   0 mm        (1000) mm        (1000)        0 2023-07-22 21:17:19.587303 pydnst-1.0.3/pydnst.egg-info/
+-rw-rw-r--   0 mm        (1000) mm        (1000)     3419 2023-07-22 21:17:19.000000 pydnst-1.0.3/pydnst.egg-info/PKG-INFO
+-rw-rw-r--   0 mm        (1000) mm        (1000)      303 2023-07-22 21:17:19.000000 pydnst-1.0.3/pydnst.egg-info/SOURCES.txt
+-rw-rw-r--   0 mm        (1000) mm        (1000)        1 2023-07-22 21:17:19.000000 pydnst-1.0.3/pydnst.egg-info/dependency_links.txt
+-rw-rw-r--   0 mm        (1000) mm        (1000)       36 2023-07-22 21:17:19.000000 pydnst-1.0.3/pydnst.egg-info/requires.txt
+-rw-rw-r--   0 mm        (1000) mm        (1000)        7 2023-07-22 21:17:19.000000 pydnst-1.0.3/pydnst.egg-info/top_level.txt
+-rw-rw-r--   0 mm        (1000) mm        (1000)       38 2023-07-22 21:17:19.587303 pydnst-1.0.3/setup.cfg
+-rw-rw-r--   0 mm        (1000) mm        (1000)     6865 2023-07-22 21:17:14.000000 pydnst-1.0.3/setup.py
```

### Comparing `pydnst-1.0.2/LICENSE` & `pydnst-1.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `pydnst-1.0.2/PKG-INFO` & `pydnst-1.0.3/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pydnst
-Version: 1.0.2
+Version: 1.0.3
 Summary: DNS Tunneling client and server
 Home-page: https://github.com/mori-b/pydnst
 Author: Mori Benech
 Author-email: moribirom@gmail.com
 License: UNKNOWN
 Keywords: dns,tunneling,dns tunneling
 Platform: UNKNOWN
@@ -32,14 +32,16 @@
 
 pydnst is a DNS tunneling implementation in Python, supporting Linux only (the client might require a few paths tweaks to run on Windows).  
 The client sends keep-alive requests every 30 seconds. If the server has a command to send to a specific client, it sends it in a response to a keep-alive. Then the client sends another query containing the command response.  
 The server can manage up to 250 clients, communication is encrypted with a unique Fernet key per client, generated on the fly and shared using RSA encryption.  
 A simple rich interface on the server side enables to send commands to specific clients, and watch the responses in real-time.  
 The client being implemented in Python is not stealth.  
 
+![alt text](https://github.com/mori-b/pydnst/assets/22458480/fbd0e97c-2030-467b-94e0-b0943f1a9b1a)
+
 <a name="setup"></a>
 ## SET UP
 
 First acquire access to a machine with a public IP, this is where the pydnst server will run.  
 Then acquire a DNS name, as short as possible, and configure its nameservers with glue records pointing to your public IP.  
 You can then configure your pydnst.toml field DNST_SERVER_NAME, and run pydnst client on your victim machine.
```

### Comparing `pydnst-1.0.2/README.md` & `pydnst-1.0.3/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -13,14 +13,16 @@
 
 pydnst is a DNS tunneling implementation in Python, supporting Linux only (the client might require a few paths tweaks to run on Windows).  
 The client sends keep-alive requests every 30 seconds. If the server has a command to send to a specific client, it sends it in a response to a keep-alive. Then the client sends another query containing the command response.  
 The server can manage up to 250 clients, communication is encrypted with a unique Fernet key per client, generated on the fly and shared using RSA encryption.  
 A simple rich interface on the server side enables to send commands to specific clients, and watch the responses in real-time.  
 The client being implemented in Python is not stealth.  
 
+![alt text](https://github.com/mori-b/pydnst/assets/22458480/fbd0e97c-2030-467b-94e0-b0943f1a9b1a)
+
 <a name="setup"></a>
 ## SET UP
 
 First acquire access to a machine with a public IP, this is where the pydnst server will run.  
 Then acquire a DNS name, as short as possible, and configure its nameservers with glue records pointing to your public IP.  
 You can then configure your pydnst.toml field DNST_SERVER_NAME, and run pydnst client on your victim machine.
```

### Comparing `pydnst-1.0.2/pydnst/__init__.py` & `pydnst-1.0.3/pydnst/__init__.py`

 * *Files identical despite different names*

### Comparing `pydnst-1.0.2/pydnst/__main__.py` & `pydnst-1.0.3/pydnst/__main__.py`

 * *Files identical despite different names*

### Comparing `pydnst-1.0.2/pydnst/client.py` & `pydnst-1.0.3/pydnst/client.py`

 * *Files identical despite different names*

### Comparing `pydnst-1.0.2/pydnst/commander.py` & `pydnst-1.0.3/pydnst/commander.py`

 * *Files identical despite different names*

### Comparing `pydnst-1.0.2/pydnst/helpers.py` & `pydnst-1.0.3/pydnst/helpers.py`

 * *Files identical despite different names*

### Comparing `pydnst-1.0.2/pydnst/message.py` & `pydnst-1.0.3/pydnst/message.py`

 * *Files identical despite different names*

### Comparing `pydnst-1.0.2/pydnst/server.py` & `pydnst-1.0.3/pydnst/server.py`

 * *Files identical despite different names*

### Comparing `pydnst-1.0.2/pydnst.egg-info/PKG-INFO` & `pydnst-1.0.3/pydnst.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pydnst
-Version: 1.0.2
+Version: 1.0.3
 Summary: DNS Tunneling client and server
 Home-page: https://github.com/mori-b/pydnst
 Author: Mori Benech
 Author-email: moribirom@gmail.com
 License: UNKNOWN
 Keywords: dns,tunneling,dns tunneling
 Platform: UNKNOWN
@@ -32,14 +32,16 @@
 
 pydnst is a DNS tunneling implementation in Python, supporting Linux only (the client might require a few paths tweaks to run on Windows).  
 The client sends keep-alive requests every 30 seconds. If the server has a command to send to a specific client, it sends it in a response to a keep-alive. Then the client sends another query containing the command response.  
 The server can manage up to 250 clients, communication is encrypted with a unique Fernet key per client, generated on the fly and shared using RSA encryption.  
 A simple rich interface on the server side enables to send commands to specific clients, and watch the responses in real-time.  
 The client being implemented in Python is not stealth.  
 
+![alt text](https://github.com/mori-b/pydnst/assets/22458480/fbd0e97c-2030-467b-94e0-b0943f1a9b1a)
+
 <a name="setup"></a>
 ## SET UP
 
 First acquire access to a machine with a public IP, this is where the pydnst server will run.  
 Then acquire a DNS name, as short as possible, and configure its nameservers with glue records pointing to your public IP.  
 You can then configure your pydnst.toml field DNST_SERVER_NAME, and run pydnst client on your victim machine.
```

### Comparing `pydnst-1.0.2/setup.py` & `pydnst-1.0.3/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 
 # Always prefer setuptools over distutils
 from setuptools import setup, find_packages
 # To use a consistent encoding
 from codecs import open
 from os import path
 
-VERSION = '1.0.2'
+VERSION = '1.0.3'
 
 here = path.abspath(path.dirname(__file__))
 # Get the long description from the README file
 with open(path.join(here, 'README.md'), encoding='utf-8') as fd:
     long_description = fd.read()
 
 # Arguments marked as "Required" below must be included for upload to PyPI.
```

