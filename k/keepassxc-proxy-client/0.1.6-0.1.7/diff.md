# Comparing `tmp/keepassxc-proxy-client-0.1.6.tar.gz` & `tmp/keepassxc-proxy-client-0.1.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "keepassxc-proxy-client-0.1.6.tar", last modified: Sat Jul 15 12:35:42 2023, max compression
+gzip compressed data, was "keepassxc-proxy-client-0.1.7.tar", last modified: Sun Jul 23 10:44:10 2023, max compression
```

## Comparing `keepassxc-proxy-client-0.1.6.tar` & `keepassxc-proxy-client-0.1.7.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 nix       (1000) nix       (1000)        0 2023-07-15 12:35:42.371925 keepassxc-proxy-client-0.1.6/
--rw-r--r--   0 nix       (1000) nix       (1000)       42 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.6/CHANGELOG.md
--rw-r--r--   0 nix       (1000) nix       (1000)      642 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.6/LICENSE
--rw-r--r--   0 nix       (1000) nix       (1000)      106 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.6/MANIFEST.in
--rw-r--r--   0 nix       (1000) nix       (1000)     3165 2023-07-15 12:35:42.371925 keepassxc-proxy-client-0.1.6/PKG-INFO
--rw-r--r--   0 nix       (1000) nix       (1000)     2015 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.6/README.md
-drwxr-xr-x   0 nix       (1000) nix       (1000)        0 2023-07-15 12:35:42.370925 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client/
--rw-r--r--   0 nix       (1000) nix       (1000)       22 2023-07-15 12:35:15.000000 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client/__init__.py
--rw-r--r--   0 nix       (1000) nix       (1000)     3229 2023-07-15 12:33:21.000000 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client/__main__.py
--rw-r--r--   0 nix       (1000) nix       (1000)     7716 2023-07-15 12:33:21.000000 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client/protocol.py
-drwxr-xr-x   0 nix       (1000) nix       (1000)        0 2023-07-15 12:35:42.370925 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client.egg-info/
--rw-r--r--   0 nix       (1000) nix       (1000)     3165 2023-07-15 12:35:42.000000 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client.egg-info/PKG-INFO
--rw-r--r--   0 nix       (1000) nix       (1000)      492 2023-07-15 12:35:42.000000 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client.egg-info/SOURCES.txt
--rw-r--r--   0 nix       (1000) nix       (1000)        1 2023-07-15 12:35:42.000000 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client.egg-info/dependency_links.txt
--rw-r--r--   0 nix       (1000) nix       (1000)       80 2023-07-15 12:35:42.000000 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client.egg-info/entry_points.txt
--rw-r--r--   0 nix       (1000) nix       (1000)       43 2023-07-15 12:35:42.000000 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client.egg-info/requires.txt
--rw-r--r--   0 nix       (1000) nix       (1000)       23 2023-07-15 12:35:42.000000 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client.egg-info/top_level.txt
--rw-r--r--   0 nix       (1000) nix       (1000)        1 2023-02-27 18:26:46.000000 keepassxc-proxy-client-0.1.6/keepassxc_proxy_client.egg-info/zip-safe
--rw-r--r--   0 nix       (1000) nix       (1000)       39 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.6/requirements.txt
--rw-r--r--   0 nix       (1000) nix       (1000)       38 2023-07-15 12:35:42.371925 keepassxc-proxy-client-0.1.6/setup.cfg
--rw-r--r--   0 nix       (1000) nix       (1000)     1860 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.6/setup.py
+drwxr-xr-x   0 nix       (1000) nix       (1000)        0 2023-07-23 10:44:10.240032 keepassxc-proxy-client-0.1.7/
+-rw-r--r--   0 nix       (1000) nix       (1000)       42 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.7/CHANGELOG.md
+-rw-r--r--   0 nix       (1000) nix       (1000)      642 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.7/LICENSE
+-rw-r--r--   0 nix       (1000) nix       (1000)      106 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.7/MANIFEST.in
+-rw-r--r--   0 nix       (1000) nix       (1000)     3165 2023-07-23 10:44:10.240032 keepassxc-proxy-client-0.1.7/PKG-INFO
+-rw-r--r--   0 nix       (1000) nix       (1000)     2015 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.7/README.md
+drwxr-xr-x   0 nix       (1000) nix       (1000)        0 2023-07-23 10:44:10.239032 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client/
+-rw-r--r--   0 nix       (1000) nix       (1000)       22 2023-07-23 10:42:22.000000 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client/__init__.py
+-rw-r--r--   0 nix       (1000) nix       (1000)     3230 2023-07-23 10:42:14.000000 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client/__main__.py
+-rw-r--r--   0 nix       (1000) nix       (1000)     7716 2023-07-15 12:33:21.000000 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client/protocol.py
+drwxr-xr-x   0 nix       (1000) nix       (1000)        0 2023-07-23 10:44:10.240032 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client.egg-info/
+-rw-r--r--   0 nix       (1000) nix       (1000)     3165 2023-07-23 10:44:10.000000 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client.egg-info/PKG-INFO
+-rw-r--r--   0 nix       (1000) nix       (1000)      492 2023-07-23 10:44:10.000000 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client.egg-info/SOURCES.txt
+-rw-r--r--   0 nix       (1000) nix       (1000)        1 2023-07-23 10:44:10.000000 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client.egg-info/dependency_links.txt
+-rw-r--r--   0 nix       (1000) nix       (1000)       80 2023-07-23 10:44:10.000000 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client.egg-info/entry_points.txt
+-rw-r--r--   0 nix       (1000) nix       (1000)       43 2023-07-23 10:44:10.000000 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client.egg-info/requires.txt
+-rw-r--r--   0 nix       (1000) nix       (1000)       23 2023-07-23 10:44:10.000000 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client.egg-info/top_level.txt
+-rw-r--r--   0 nix       (1000) nix       (1000)        1 2023-02-27 18:26:46.000000 keepassxc-proxy-client-0.1.7/keepassxc_proxy_client.egg-info/zip-safe
+-rw-r--r--   0 nix       (1000) nix       (1000)       39 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.7/requirements.txt
+-rw-r--r--   0 nix       (1000) nix       (1000)       38 2023-07-23 10:44:10.240032 keepassxc-proxy-client-0.1.7/setup.cfg
+-rw-r--r--   0 nix       (1000) nix       (1000)     1860 2023-02-27 18:25:33.000000 keepassxc-proxy-client-0.1.7/setup.py
```

### Comparing `keepassxc-proxy-client-0.1.6/LICENSE` & `keepassxc-proxy-client-0.1.7/LICENSE`

 * *Files identical despite different names*

### Comparing `keepassxc-proxy-client-0.1.6/PKG-INFO` & `keepassxc-proxy-client-0.1.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: keepassxc-proxy-client
-Version: 0.1.6
+Version: 0.1.7
 Summary: A CLI for keepassxc-proxy
 Home-page: https://github.com/hargoniX/keepassxc-proxy-client
 Author: Henrik Boeving
 Author-email: hargonix@gmail.com
 Project-URL: Issue tracker, https://github.com/hargoniX/keepassxc-proxy-client/issues
 Project-URL: Changelog, https://github.com/hargoniX/keepassxc-proxy-client/blob/master/CHANGELOG.md
 Classifier: Development Status :: 4 - Beta
```

### Comparing `keepassxc-proxy-client-0.1.6/README.md` & `keepassxc-proxy-client-0.1.7/README.md`

 * *Files identical despite different names*

### Comparing `keepassxc-proxy-client-0.1.6/keepassxc_proxy_client/__main__.py` & `keepassxc-proxy-client-0.1.7/keepassxc_proxy_client/__main__.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 creates a new association with it (this will prompt a dialogue from keepassxc)
 and prints it to stdout as JSON. Note that the public key that is printed is
 secret and can allow anyone with access to your local machine access to all
 passwords that are related to a URL, thus it should be stored safely.
 
 keepassxc_proxy_client get <file> <url>: Reads a keepassxc association from
 <file> and attempts to get the first password for <url>. Will exit with 1 if the
-assocation is not valid for the running keepassxc instance or the no logins are
+association is not valid for the running keepassxc instance or the no logins are
 found for the given URL.
 
 keepassxc_proxy_client unlock <file>: Causes a running KeepassXC instance
 to launch a dialogue window to allow the user to unlock a locked database.
 If the database is already unlocked it has no effect.
 """
```

### Comparing `keepassxc-proxy-client-0.1.6/keepassxc_proxy_client/protocol.py` & `keepassxc-proxy-client-0.1.7/keepassxc_proxy_client/protocol.py`

 * *Files identical despite different names*

### Comparing `keepassxc-proxy-client-0.1.6/keepassxc_proxy_client.egg-info/PKG-INFO` & `keepassxc-proxy-client-0.1.7/keepassxc_proxy_client.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: keepassxc-proxy-client
-Version: 0.1.6
+Version: 0.1.7
 Summary: A CLI for keepassxc-proxy
 Home-page: https://github.com/hargoniX/keepassxc-proxy-client
 Author: Henrik Boeving
 Author-email: hargonix@gmail.com
 Project-URL: Issue tracker, https://github.com/hargoniX/keepassxc-proxy-client/issues
 Project-URL: Changelog, https://github.com/hargoniX/keepassxc-proxy-client/blob/master/CHANGELOG.md
 Classifier: Development Status :: 4 - Beta
```

### Comparing `keepassxc-proxy-client-0.1.6/setup.py` & `keepassxc-proxy-client-0.1.7/setup.py`

 * *Files identical despite different names*

