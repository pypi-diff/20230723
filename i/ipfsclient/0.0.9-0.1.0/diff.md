# Comparing `tmp/ipfsclient-0.0.9.tar.gz` & `tmp/ipfsclient-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ipfsclient-0.0.9.tar", last modified: Sat Jul  8 01:39:10 2023, max compression
+gzip compressed data, was "ipfsclient-0.1.0.tar", last modified: Sun Jul 23 19:32:27 2023, max compression
```

## Comparing `ipfsclient-0.0.9.tar` & `ipfsclient-0.1.0.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 nate       (501) staff       (20)        0 2023-07-08 01:39:10.306853 ipfsclient-0.0.9/
--rw-r--r--   0 nate       (501) staff       (20)     1211 2023-04-18 22:36:57.000000 ipfsclient-0.0.9/LICENSE
--rw-r--r--   0 nate       (501) staff       (20)     2467 2023-07-08 01:39:10.306747 ipfsclient-0.0.9/PKG-INFO
--rw-r--r--   0 nate       (501) staff       (20)     2004 2023-04-18 22:38:30.000000 ipfsclient-0.0.9/README.md
-drwxr-xr-x   0 nate       (501) staff       (20)        0 2023-07-08 01:39:10.305904 ipfsclient-0.0.9/ipfsclient/
--rw-r--r--   0 nate       (501) staff       (20)       58 2023-07-08 01:29:11.000000 ipfsclient-0.0.9/ipfsclient/__init__.py
--rw-r--r--   0 nate       (501) staff       (20)    11412 2023-07-08 01:30:52.000000 ipfsclient-0.0.9/ipfsclient/ipfs.py
-drwxr-xr-x   0 nate       (501) staff       (20)        0 2023-07-08 01:39:10.306587 ipfsclient-0.0.9/ipfsclient.egg-info/
--rw-r--r--   0 nate       (501) staff       (20)     2467 2023-07-08 01:39:10.000000 ipfsclient-0.0.9/ipfsclient.egg-info/PKG-INFO
--rw-r--r--   0 nate       (501) staff       (20)      204 2023-07-08 01:39:10.000000 ipfsclient-0.0.9/ipfsclient.egg-info/SOURCES.txt
--rw-r--r--   0 nate       (501) staff       (20)        1 2023-07-08 01:39:10.000000 ipfsclient-0.0.9/ipfsclient.egg-info/dependency_links.txt
--rw-r--r--   0 nate       (501) staff       (20)       11 2023-07-08 01:39:10.000000 ipfsclient-0.0.9/ipfsclient.egg-info/top_level.txt
--rw-r--r--   0 nate       (501) staff       (20)       38 2023-07-08 01:39:10.306883 ipfsclient-0.0.9/setup.cfg
--rw-r--r--   0 nate       (501) staff       (20)      955 2023-07-08 01:27:01.000000 ipfsclient-0.0.9/setup.py
+drwxr-xr-x   0 nate       (501) staff       (20)        0 2023-07-23 19:32:27.235452 ipfsclient-0.1.0/
+-rw-r--r--   0 nate       (501) staff       (20)     1211 2023-04-18 22:36:57.000000 ipfsclient-0.1.0/LICENSE
+-rw-r--r--   0 nate       (501) staff       (20)     2467 2023-07-23 19:32:27.235341 ipfsclient-0.1.0/PKG-INFO
+-rw-r--r--   0 nate       (501) staff       (20)     2004 2023-04-18 22:38:30.000000 ipfsclient-0.1.0/README.md
+drwxr-xr-x   0 nate       (501) staff       (20)        0 2023-07-23 19:32:27.234476 ipfsclient-0.1.0/ipfsclient/
+-rw-r--r--   0 nate       (501) staff       (20)       58 2023-07-23 19:31:59.000000 ipfsclient-0.1.0/ipfsclient/__init__.py
+-rw-r--r--   0 nate       (501) staff       (20)    11522 2023-07-23 19:31:27.000000 ipfsclient-0.1.0/ipfsclient/ipfs.py
+drwxr-xr-x   0 nate       (501) staff       (20)        0 2023-07-23 19:32:27.235172 ipfsclient-0.1.0/ipfsclient.egg-info/
+-rw-r--r--   0 nate       (501) staff       (20)     2467 2023-07-23 19:32:27.000000 ipfsclient-0.1.0/ipfsclient.egg-info/PKG-INFO
+-rw-r--r--   0 nate       (501) staff       (20)      204 2023-07-23 19:32:27.000000 ipfsclient-0.1.0/ipfsclient.egg-info/SOURCES.txt
+-rw-r--r--   0 nate       (501) staff       (20)        1 2023-07-23 19:32:27.000000 ipfsclient-0.1.0/ipfsclient.egg-info/dependency_links.txt
+-rw-r--r--   0 nate       (501) staff       (20)       11 2023-07-23 19:32:27.000000 ipfsclient-0.1.0/ipfsclient.egg-info/top_level.txt
+-rw-r--r--   0 nate       (501) staff       (20)       38 2023-07-23 19:32:27.235482 ipfsclient-0.1.0/setup.cfg
+-rw-r--r--   0 nate       (501) staff       (20)      955 2023-07-08 01:27:01.000000 ipfsclient-0.1.0/setup.py
```

### Comparing `ipfsclient-0.0.9/LICENSE` & `ipfsclient-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `ipfsclient-0.0.9/PKG-INFO` & `ipfsclient-0.1.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ipfsclient
-Version: 0.0.9
+Version: 0.1.0
 Summary: IPFS RPC Client
 Home-page: https://github.com/nanoswap/ipfsclient
 Author: Nathaniel Schultz
 Author-email: nate@nanoswap.finance
 Project-URL: Bug Tracker, https://github.com/nanoswap/ipfsclient/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: The Unlicense (Unlicense)
```

### Comparing `ipfsclient-0.0.9/README.md` & `ipfsclient-0.1.0/README.md`

 * *Files identical despite different names*

### Comparing `ipfsclient-0.0.9/ipfsclient/ipfs.py` & `ipfsclient-0.1.0/ipfsclient/ipfs.py`

 * *Files 2% similar despite different names*

```diff
@@ -239,41 +239,45 @@
             #     files={
             #         'file': example.SerializeToString()
             #     }
             # )
         except requests.exceptions.HTTPError as e:
             raise RuntimeError(e.response._content.decode()) from e
 
-    def add(self: Self, filename: str, data: bytes) -> None:
+    def add(self: Self, filename: str, data: bytes) -> str:
         """Create a new file in ipfs.
 
         This does not work for updating existing files.
 
         Args:
             filename (str): The filename for the uploaded data
             data (bytes): The data that will be written to the new file
+
+        Returns:
+            str: CID of the added file
         """
         # Split the filename into its directory and basename components
         parts = os.path.split(filename)
 
         # If the directory part is not empty, create it recursively
         if parts[0]:
             self.mkdir(parts[0])
 
         try:
-            self._make_request(
+            response = self._make_request(
                 endpoint="add",
                 params={
                     "to-files": f"{IPFS_HOME}/{filename}",
                     "raw-leaves": True
                 },
                 files={
                     'file': data
                 }
             )
+            return response.json()["Hash"]
         except Exception as e:
             LOG.exception(e)
             if e.response:
                 raise RuntimeError(
                     e.response._content.decode()
                 ) from e
             else:
```

### Comparing `ipfsclient-0.0.9/ipfsclient.egg-info/PKG-INFO` & `ipfsclient-0.1.0/ipfsclient.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ipfsclient
-Version: 0.0.9
+Version: 0.1.0
 Summary: IPFS RPC Client
 Home-page: https://github.com/nanoswap/ipfsclient
 Author: Nathaniel Schultz
 Author-email: nate@nanoswap.finance
 Project-URL: Bug Tracker, https://github.com/nanoswap/ipfsclient/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: The Unlicense (Unlicense)
```

### Comparing `ipfsclient-0.0.9/setup.py` & `ipfsclient-0.1.0/setup.py`

 * *Files identical despite different names*

