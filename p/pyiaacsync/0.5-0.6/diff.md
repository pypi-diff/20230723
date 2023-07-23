# Comparing `tmp/pyiaacsync-0.5.tar.gz` & `tmp/pyiaacsync-0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/pyiaacsync-0.5.tar", last modified: Thu Apr 27 00:30:14 2023, max compression
+gzip compressed data, was "dist/pyiaacsync-0.6.tar", last modified: Sun Jul 23 03:50:58 2023, max compression
```

## Comparing `pyiaacsync-0.5.tar` & `pyiaacsync-0.6.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 manasbellani   (501) wheel        (0)        0 2023-04-27 00:30:14.000000 pyiaacsync-0.5/
--rw-r--r--   0 manasbellani   (501) wheel        (0)     5688 2023-04-27 00:30:14.000000 pyiaacsync-0.5/PKG-INFO
--rw-r--r--   0 manasbellani   (501) wheel        (0)     4585 2023-04-26 04:33:24.000000 pyiaacsync-0.5/README.md
-drwxr-xr-x   0 manasbellani   (501) wheel        (0)        0 2023-04-27 00:30:14.000000 pyiaacsync-0.5/pyiaacsync/
--rw-r--r--   0 manasbellani   (501) wheel        (0)        0 2023-03-17 07:03:20.000000 pyiaacsync-0.5/pyiaacsync/__init__.py
--rw-r--r--   0 manasbellani   (501) wheel        (0)    13875 2023-04-27 00:29:31.000000 pyiaacsync-0.5/pyiaacsync/pyiaacsync.py
-drwxr-xr-x   0 manasbellani   (501) wheel        (0)        0 2023-04-27 00:30:14.000000 pyiaacsync-0.5/pyiaacsync.egg-info/
--rw-r--r--   0 manasbellani   (501) wheel        (0)     5688 2023-04-27 00:30:14.000000 pyiaacsync-0.5/pyiaacsync.egg-info/PKG-INFO
--rw-r--r--   0 manasbellani   (501) wheel        (0)      235 2023-04-27 00:30:14.000000 pyiaacsync-0.5/pyiaacsync.egg-info/SOURCES.txt
--rw-r--r--   0 manasbellani   (501) wheel        (0)        1 2023-04-27 00:30:14.000000 pyiaacsync-0.5/pyiaacsync.egg-info/dependency_links.txt
--rw-r--r--   0 manasbellani   (501) wheel        (0)        7 2023-04-27 00:30:14.000000 pyiaacsync-0.5/pyiaacsync.egg-info/requires.txt
--rw-r--r--   0 manasbellani   (501) wheel        (0)       11 2023-04-27 00:30:14.000000 pyiaacsync-0.5/pyiaacsync.egg-info/top_level.txt
--rw-r--r--   0 manasbellani   (501) wheel        (0)       38 2023-04-27 00:30:14.000000 pyiaacsync-0.5/setup.cfg
--rw-r--r--   0 manasbellani   (501) wheel        (0)      864 2023-04-26 04:34:15.000000 pyiaacsync-0.5/setup.py
+drwxr-xr-x   0 manasbellani   (501) wheel        (0)        0 2023-07-23 03:50:58.000000 pyiaacsync-0.6/
+-rw-r--r--   0 manasbellani   (501) wheel        (0)     5886 2023-07-23 03:50:58.000000 pyiaacsync-0.6/PKG-INFO
+-rw-r--r--   0 manasbellani   (501) wheel        (0)     4775 2023-07-23 03:46:36.000000 pyiaacsync-0.6/README.md
+drwxr-xr-x   0 manasbellani   (501) wheel        (0)        0 2023-07-23 03:50:58.000000 pyiaacsync-0.6/pyiaacsync/
+-rw-r--r--   0 manasbellani   (501) wheel        (0)        0 2023-03-17 07:03:20.000000 pyiaacsync-0.6/pyiaacsync/__init__.py
+-rw-r--r--   0 manasbellani   (501) wheel        (0)    15268 2023-07-23 02:41:02.000000 pyiaacsync-0.6/pyiaacsync/pyiaacsync.py
+drwxr-xr-x   0 manasbellani   (501) wheel        (0)        0 2023-07-23 03:50:58.000000 pyiaacsync-0.6/pyiaacsync.egg-info/
+-rw-r--r--   0 manasbellani   (501) wheel        (0)     5886 2023-07-23 03:50:58.000000 pyiaacsync-0.6/pyiaacsync.egg-info/PKG-INFO
+-rw-r--r--   0 manasbellani   (501) wheel        (0)      235 2023-07-23 03:50:58.000000 pyiaacsync-0.6/pyiaacsync.egg-info/SOURCES.txt
+-rw-r--r--   0 manasbellani   (501) wheel        (0)        1 2023-07-23 03:50:58.000000 pyiaacsync-0.6/pyiaacsync.egg-info/dependency_links.txt
+-rw-r--r--   0 manasbellani   (501) wheel        (0)        7 2023-07-23 03:50:58.000000 pyiaacsync-0.6/pyiaacsync.egg-info/requires.txt
+-rw-r--r--   0 manasbellani   (501) wheel        (0)       11 2023-07-23 03:50:58.000000 pyiaacsync-0.6/pyiaacsync.egg-info/top_level.txt
+-rw-r--r--   0 manasbellani   (501) wheel        (0)       38 2023-07-23 03:50:58.000000 pyiaacsync-0.6/setup.cfg
+-rw-r--r--   0 manasbellani   (501) wheel        (0)      864 2023-07-23 03:41:33.000000 pyiaacsync-0.6/setup.py
```

### Comparing `pyiaacsync-0.5/PKG-INFO` & `pyiaacsync-0.6/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyiaacsync
-Version: 0.5
+Version: 0.6
 Summary: Deploy infrastructure as code via polling
 Home-page: https://github.com/manasmbellani/pyiaacsync
 License: UNKNOWN
 Description: # PyIAACSync
         
         ## Introduction
         infrastructure-as-code tools such as Terraform and Palumi are gaining popularity and increasingly becoming neceessary to support the principles of Site Reliability Engineering (SRE). 
@@ -17,18 +17,19 @@
         PyIAACSync provides a framework which allows software engineering teams getting into infrastructure-as-code to easily create and sync assets which they have defined in YAML spec files, in a polled manner (non-event driven). The infrastructue components can be `anything` (AWS asset, GCP asset, any SIEM detection rule) that can be:
             a. described in YAML files, and 
             b. can be read, created or deleted via API calls
         
         Software engineers need to create the following to leverage `pyiaacsync`:
         1. A folder (`iaac_sync_folder`) that contains the specs/configs for the infrastructure to create
         2. A simple asset python file that contains a class describing the asset with the following `static` functions:
-           - validate: to validate whether the spec/config that has been supplied in the 
-           - create: to create the asset via the supplied spec/config
-           - delete: to delete that has been supplied via the spec/config
-           - check: to check whether the asset that has been deployed matches the spec/config aka `integrity check`. If not, the asset will be re-created
+           - `validate`: to validate whether the spec/config that has been supplied in the 
+           - `create`: to create the asset via the supplied spec/config
+           - `delete`: to delete that has been supplied via the spec/config
+           - `check`: to check whether the asset that has been deployed matches the spec/config aka `integrity check`. If not, the asset will be re-created
+           - `update` (Optional): to be called to update an existing asset, eg when the configuration gets changed. If not defined for the assets , then the `delete` / `create` gets called.
         
         Please see `Usage` section that describes the example in more detail
         
         ## Install
         
         ### via PyPI
```

### Comparing `pyiaacsync-0.5/README.md` & `pyiaacsync-0.6/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -11,18 +11,19 @@
 PyIAACSync provides a framework which allows software engineering teams getting into infrastructure-as-code to easily create and sync assets which they have defined in YAML spec files, in a polled manner (non-event driven). The infrastructue components can be `anything` (AWS asset, GCP asset, any SIEM detection rule) that can be:
     a. described in YAML files, and 
     b. can be read, created or deleted via API calls
 
 Software engineers need to create the following to leverage `pyiaacsync`:
 1. A folder (`iaac_sync_folder`) that contains the specs/configs for the infrastructure to create
 2. A simple asset python file that contains a class describing the asset with the following `static` functions:
-   - validate: to validate whether the spec/config that has been supplied in the 
-   - create: to create the asset via the supplied spec/config
-   - delete: to delete that has been supplied via the spec/config
-   - check: to check whether the asset that has been deployed matches the spec/config aka `integrity check`. If not, the asset will be re-created
+   - `validate`: to validate whether the spec/config that has been supplied in the 
+   - `create`: to create the asset via the supplied spec/config
+   - `delete`: to delete that has been supplied via the spec/config
+   - `check`: to check whether the asset that has been deployed matches the spec/config aka `integrity check`. If not, the asset will be re-created
+   - `update` (Optional): to be called to update an existing asset, eg when the configuration gets changed. If not defined for the assets , then the `delete` / `create` gets called.
 
 Please see `Usage` section that describes the example in more detail
 
 ## Install
 
 ### via PyPI
```

### Comparing `pyiaacsync-0.5/pyiaacsync/pyiaacsync.py` & `pyiaacsync-0.6/pyiaacsync/pyiaacsync.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,14 +11,19 @@
     pass
 
 class AssetNotDeletedException(Exception):
     """Exception generated when an asset is not deleted
     """
     pass
 
+class AssetNotUpdatedException(Exception):
+    """Exception generated when an asset is not updated
+    """
+    pass
+
 class FileNotFoundException(Exception):
     """Exception generated when a file has not been found
     """
     pass
 
 class FileAlreadyExists(Exception):
     """Exception generated when a file already exists
@@ -221,33 +226,48 @@
                                         is_asset_in_sync = self.asset.check(asset_id, config, **args)
 
                                     # If the spec file has changed OR is brand new, then re-create the asset (delete, then create)
                                     if (not state_hash) or (state_hash != config_hash) or not is_asset_in_sync:
 
                                         # Recreate the asset by first attempting to delete it
                                         if asset_id:
-                                            if self.asset.delete(asset_id, **args):
-                                                if config_path in self.state:
-                                                    # Update the state file that asset has been deleted
-                                                    del self.state[config_path]
-                                            else:
-                                                raise AssetNotDeletedException(f"Asset with config in file {config_path} could not be deleted")
-                                            
-                                        # Try to create the asset again now
-                                        asset_id = self.asset.create(config, **args)
-                                        if asset_id:
-                                            if config_path not in self.state:
-                                                self.state[config_path] = {}
-                                            # Update the state file with the hash and the new asset ID created
-                                            self.state[config_path]['hash'] = config_hash
-                                            self.state[config_path]['asset_id'] = asset_id
 
+                                            # Check if there is an update function in the asset, if yes, then call it
+                                            if hasattr(self.asset, 'update') and callable(self.asset.update):
+                                                if self.asset.update(asset_id, config, **args):
+                                                    # Call the update function, and ensure that the same asset ID is returned
+                                                    # if asset ID not returned then there was an error
+                                                    self.state[config_path]['hash'] = config_hash
+                                                    self.state[config_path]['asset_id'] = asset_id
+                                                else:
+                                                    raise AssetNotUpdatedException(f"Asset with config in file {config_path} could not be updated")
+
+                                            else:
+                                                if self.asset.delete(asset_id, **args):
+                                                    # Asset ID deleted
+                                                    asset_id = ''
+                                                    if config_path in self.state:
+                                                        # Update the state file that asset has been deleted
+                                                        del self.state[config_path]
+                                                else:
+                                                    raise AssetNotDeletedException(f"Asset with config in file {config_path} could not be deleted")
+                                        
+                                        # Try to create the asset again now, if it is deleted
                                         if not asset_id:
-                                            raise AssetNotCreatedException(f"Asset with config in file {config_path} could not be created")
-            
+                                            asset_id = self.asset.create(config, **args)
+                                            if asset_id:
+                                                if config_path not in self.state:
+                                                    self.state[config_path] = {}
+                                                # Update the state file with the hash and the new asset ID created
+                                                self.state[config_path]['hash'] = config_hash
+                                                self.state[config_path]['asset_id'] = asset_id
+
+                                            if not asset_id:
+                                                raise AssetNotCreatedException(f"Asset with config in file {config_path} could not be created")
+                
                 # Delete any assets which are not in the config spec (git)
                 if self.state:
 
                     # Read all the config spec keys and loop through them
                     state_config_paths = list(self.state.keys())
                     for config_path in state_config_paths:
```

### Comparing `pyiaacsync-0.5/pyiaacsync.egg-info/PKG-INFO` & `pyiaacsync-0.6/pyiaacsync.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyiaacsync
-Version: 0.5
+Version: 0.6
 Summary: Deploy infrastructure as code via polling
 Home-page: https://github.com/manasmbellani/pyiaacsync
 License: UNKNOWN
 Description: # PyIAACSync
         
         ## Introduction
         infrastructure-as-code tools such as Terraform and Palumi are gaining popularity and increasingly becoming neceessary to support the principles of Site Reliability Engineering (SRE). 
@@ -17,18 +17,19 @@
         PyIAACSync provides a framework which allows software engineering teams getting into infrastructure-as-code to easily create and sync assets which they have defined in YAML spec files, in a polled manner (non-event driven). The infrastructue components can be `anything` (AWS asset, GCP asset, any SIEM detection rule) that can be:
             a. described in YAML files, and 
             b. can be read, created or deleted via API calls
         
         Software engineers need to create the following to leverage `pyiaacsync`:
         1. A folder (`iaac_sync_folder`) that contains the specs/configs for the infrastructure to create
         2. A simple asset python file that contains a class describing the asset with the following `static` functions:
-           - validate: to validate whether the spec/config that has been supplied in the 
-           - create: to create the asset via the supplied spec/config
-           - delete: to delete that has been supplied via the spec/config
-           - check: to check whether the asset that has been deployed matches the spec/config aka `integrity check`. If not, the asset will be re-created
+           - `validate`: to validate whether the spec/config that has been supplied in the 
+           - `create`: to create the asset via the supplied spec/config
+           - `delete`: to delete that has been supplied via the spec/config
+           - `check`: to check whether the asset that has been deployed matches the spec/config aka `integrity check`. If not, the asset will be re-created
+           - `update` (Optional): to be called to update an existing asset, eg when the configuration gets changed. If not defined for the assets , then the `delete` / `create` gets called.
         
         Please see `Usage` section that describes the example in more detail
         
         ## Install
         
         ### via PyPI
```

### Comparing `pyiaacsync-0.5/setup.py` & `pyiaacsync-0.6/setup.py`

 * *Files 17% similar despite different names*

```diff
@@ -16,15 +16,15 @@
 
 # Read the description from the markdown file
 with open('README.md', 'r') as f:
     description = f.read()
 
 setup(
     name="pyiaacsync",
-    version="0.5",
+    version="0.6",
     packages=find_packages(),
     install_requires=requirements,
     description=project_description,
     long_description=description,
     long_description_content_type="text/markdown",
     url=get_git_remote_url()
 )
```

