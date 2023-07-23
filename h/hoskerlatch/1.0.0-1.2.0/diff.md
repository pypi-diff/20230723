# Comparing `tmp/hoskerlatch-1.0.0.tar.gz` & `tmp/hoskerlatch-1.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hoskerlatch-1.0.0.tar", last modified: Tue Jun 27 20:41:20 2023, max compression
+gzip compressed data, was "hoskerlatch-1.2.0.tar", last modified: Sun Jul 23 21:27:17 2023, max compression
```

## Comparing `hoskerlatch-1.0.0.tar` & `hoskerlatch-1.2.0.tar`

### file list

```diff
@@ -1,19 +1,20 @@
-drwxrwxr-x   0 tom       (1000) tom       (1000)        0 2023-06-27 20:41:20.728657 hoskerlatch-1.0.0/
--rw-rw-r--   0 tom       (1000) tom       (1000)     1050 2022-11-13 15:45:04.000000 hoskerlatch-1.0.0/LICENSE
--rw-rw-r--   0 tom       (1000) tom       (1000)      296 2023-06-27 20:41:20.728657 hoskerlatch-1.0.0/PKG-INFO
--rw-rw-r--   0 tom       (1000) tom       (1000)      305 2023-06-27 20:38:45.000000 hoskerlatch-1.0.0/README.md
-drwxrwxr-x   0 tom       (1000) tom       (1000)        0 2023-06-27 20:41:20.728657 hoskerlatch-1.0.0/hoskerlatch.egg-info/
--rw-rw-r--   0 tom       (1000) tom       (1000)      296 2023-06-27 20:41:20.000000 hoskerlatch-1.0.0/hoskerlatch.egg-info/PKG-INFO
--rw-rw-r--   0 tom       (1000) tom       (1000)      299 2023-06-27 20:41:20.000000 hoskerlatch-1.0.0/hoskerlatch.egg-info/SOURCES.txt
--rw-rw-r--   0 tom       (1000) tom       (1000)        1 2023-06-27 20:41:20.000000 hoskerlatch-1.0.0/hoskerlatch.egg-info/dependency_links.txt
--rw-rw-r--   0 tom       (1000) tom       (1000)       26 2023-06-27 20:41:20.000000 hoskerlatch-1.0.0/hoskerlatch.egg-info/requires.txt
--rw-rw-r--   0 tom       (1000) tom       (1000)       12 2023-06-27 20:41:20.000000 hoskerlatch-1.0.0/hoskerlatch.egg-info/top_level.txt
-drwxrwxr-x   0 tom       (1000) tom       (1000)        0 2023-06-27 20:41:20.728657 hoskerlatch-1.0.0/scripts/
--rw-rw-r--   0 tom       (1000) tom       (1000)     1036 2023-06-27 20:33:28.000000 hoskerlatch-1.0.0/scripts/hoskerlatch
--rw-rw-r--   0 tom       (1000) tom       (1000)      899 2023-06-27 20:33:38.000000 hoskerlatch-1.0.0/scripts/hoskerunlatch
--rw-rw-r--   0 tom       (1000) tom       (1000)       38 2023-06-27 20:41:20.728657 hoskerlatch-1.0.0/setup.cfg
--rw-rw-r--   0 tom       (1000) tom       (1000)      995 2023-06-26 20:33:27.000000 hoskerlatch-1.0.0/setup.py
-drwxrwxr-x   0 tom       (1000) tom       (1000)        0 2023-06-27 20:41:20.728657 hoskerlatch-1.0.0/source/
--rw-rw-r--   0 tom       (1000) tom       (1000)      563 2023-06-26 18:34:26.000000 hoskerlatch-1.0.0/source/__init__.py
--rw-rw-r--   0 tom       (1000) tom       (1000)     5205 2023-06-26 20:32:47.000000 hoskerlatch-1.0.0/source/latcher.py
--rw-rw-r--   0 tom       (1000) tom       (1000)     2677 2023-06-26 19:07:37.000000 hoskerlatch-1.0.0/source/unlatcher.py
+drwxrwxr-x   0 tom       (1000) tom       (1000)        0 2023-07-23 21:27:17.548263 hoskerlatch-1.2.0/
+-rw-rw-r--   0 tom       (1000) tom       (1000)     1050 2022-11-13 15:45:04.000000 hoskerlatch-1.2.0/LICENSE
+-rw-rw-r--   0 tom       (1000) tom       (1000)      296 2023-07-23 21:27:17.548263 hoskerlatch-1.2.0/PKG-INFO
+-rw-rw-r--   0 tom       (1000) tom       (1000)      305 2023-06-27 20:38:45.000000 hoskerlatch-1.2.0/README.md
+drwxrwxr-x   0 tom       (1000) tom       (1000)        0 2023-07-23 21:27:17.548263 hoskerlatch-1.2.0/hoskerlatch.egg-info/
+-rw-rw-r--   0 tom       (1000) tom       (1000)      296 2023-07-23 21:27:17.000000 hoskerlatch-1.2.0/hoskerlatch.egg-info/PKG-INFO
+-rw-rw-r--   0 tom       (1000) tom       (1000)      336 2023-07-23 21:27:17.000000 hoskerlatch-1.2.0/hoskerlatch.egg-info/SOURCES.txt
+-rw-rw-r--   0 tom       (1000) tom       (1000)        1 2023-07-23 21:27:17.000000 hoskerlatch-1.2.0/hoskerlatch.egg-info/dependency_links.txt
+-rw-rw-r--   0 tom       (1000) tom       (1000)       26 2023-07-23 21:27:17.000000 hoskerlatch-1.2.0/hoskerlatch.egg-info/requires.txt
+-rw-rw-r--   0 tom       (1000) tom       (1000)       12 2023-07-23 21:27:17.000000 hoskerlatch-1.2.0/hoskerlatch.egg-info/top_level.txt
+drwxrwxr-x   0 tom       (1000) tom       (1000)        0 2023-07-23 21:27:17.548263 hoskerlatch-1.2.0/scripts/
+-rw-rw-r--   0 tom       (1000) tom       (1000)     1036 2023-06-27 20:33:28.000000 hoskerlatch-1.2.0/scripts/hoskerlatch
+-rw-rw-r--   0 tom       (1000) tom       (1000)      216 2023-07-23 21:25:39.000000 hoskerlatch-1.2.0/scripts/hoskerlatch-install-specials
+-rw-rw-r--   0 tom       (1000) tom       (1000)      899 2023-06-27 20:33:38.000000 hoskerlatch-1.2.0/scripts/hoskerunlatch
+-rw-rw-r--   0 tom       (1000) tom       (1000)       38 2023-07-23 21:27:17.548263 hoskerlatch-1.2.0/setup.cfg
+-rw-rw-r--   0 tom       (1000) tom       (1000)     1049 2023-07-23 21:14:29.000000 hoskerlatch-1.2.0/setup.py
+drwxrwxr-x   0 tom       (1000) tom       (1000)        0 2023-07-23 21:27:17.548263 hoskerlatch-1.2.0/source/
+-rw-rw-r--   0 tom       (1000) tom       (1000)      563 2023-06-26 18:34:26.000000 hoskerlatch-1.2.0/source/__init__.py
+-rw-rw-r--   0 tom       (1000) tom       (1000)     5691 2023-07-23 21:01:11.000000 hoskerlatch-1.2.0/source/latcher.py
+-rw-rw-r--   0 tom       (1000) tom       (1000)     2677 2023-07-23 19:24:56.000000 hoskerlatch-1.2.0/source/unlatcher.py
```

### Comparing `hoskerlatch-1.0.0/LICENSE` & `hoskerlatch-1.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `hoskerlatch-1.0.0/scripts/hoskerlatch` & `hoskerlatch-1.2.0/scripts/hoskerlatch`

 * *Files identical despite different names*

### Comparing `hoskerlatch-1.0.0/scripts/hoskerunlatch` & `hoskerlatch-1.2.0/scripts/hoskerunlatch`

 * *Files identical despite different names*

### Comparing `hoskerlatch-1.0.0/setup.py` & `hoskerlatch-1.2.0/setup.py`

 * *Files 20% similar despite different names*

```diff
@@ -3,20 +3,24 @@
 """
 
 # Non-standard imports.
 from setuptools import setup
 
 # Local constants.
 PACKAGE_NAME = "hoskerlatch"
-VERSION = "1.0.0"
+VERSION = "1.2.0"
 DESCRIPTION = "Encrypt and decrypt folders to a medium standard of security"
 GIT_URL_STEM = "https://github.com/tomhosker"
 AUTHOR = "Tom Hosker"
 AUTHOR_EMAIL = "tomdothosker@gmail.com"
-SCRIPT_PATHS = ("scripts/hoskerlatch", "scripts/hoskerunlatch")
+SCRIPT_PATHS = (
+    "scripts/hoskerlatch",
+    "scripts/hoskerunlatch",
+    "scripts/hoskerlatch-install-specials"
+)
 INSTALL_REQUIRES = ("cryptography", "hosker-utils")
 INCLUDE_PACKAGE_DATA = True
 
 ###################################
 # THIS IS WHERE THE MAGIC HAPPENS #
 ###################################
```

### Comparing `hoskerlatch-1.0.0/source/__init__.py` & `hoskerlatch-1.2.0/source/__init__.py`

 * *Files identical despite different names*

### Comparing `hoskerlatch-1.0.0/source/latcher.py` & `hoskerlatch-1.2.0/source/latcher.py`

 * *Files 10% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 
 # Standard imports.
 import base64
 import random
 import secrets
 import shutil
 import string
+import subprocess
 from pathlib import Path
 
 # Non-standard imports.
 from cryptography.fernet import Fernet
 from cryptography.hazmat.primitives.kdf.scrypt import Scrypt
 
 # Local constants.
@@ -118,17 +119,17 @@
             encrypted_file.write(encrypted_data)
 
     def clean(self):
         """ Remove any unencrypted data, as well as any generated files. """
         files_to_remove = (self.path_to_zip,)
         folders_to_remove = (self.path_to_target,)
         for file_path in files_to_remove:
-            Path(file_path).unlink()
+            secure_delete_file(file_path)
         for folder_path in folders_to_remove:
-            shutil.rmtree(folder_path)
+            secure_delete_folder(folder_path)
 
     def latch(self, password):
         """ (1) Zip. (2) Encrypt. (3) Clean. """
         self.zip_target()
         self.encrypt(password)
         self.clean()
 
@@ -145,20 +146,33 @@
         "".join(
             random.choice(string.ascii_lowercase+string.digits)
             for _ in range(FILENAME_LENGTH)
         )
     return result
 
 def make_key(salt, password):
-    """Derive the key from the password using the passed salt. """
+    """ Derive the key from the password using the passed salt. """
     parallelisation_parameter = 1
     key_derivation_function = \
         Scrypt(
             salt,
             KEY_LENGTH,
             MEMORY_COST,
             BLOCK_SIZE,
             parallelisation_parameter
         )
     derived_key = key_derivation_function.derive(password.encode())
     result = base64.urlsafe_b64encode(derived_key)
     return result
+
+def secure_delete_file(path_to_file):
+    """ Securely delete a given file. """
+    subprocess.run(["srm", path_to_file], check=True)
+
+def secure_delete_folder(path_to_folder):
+    """ Securely delete a given folder, recursively. """
+    for subpath in Path(path_to_folder).glob("*"):
+        if subpath.is_dir():
+            secure_delete_folder(str(subpath))
+        else:
+            secure_delete_file(str(subpath))
+    shutil.rmtree(path_to_folder)
```

### Comparing `hoskerlatch-1.0.0/source/unlatcher.py` & `hoskerlatch-1.2.0/source/unlatcher.py`

 * *Files identical despite different names*

