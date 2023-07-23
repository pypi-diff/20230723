# Comparing `tmp/agenta-0.1.8.tar.gz` & `tmp/agenta-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "agenta-0.1.8.tar", max compression
+gzip compressed data, was "agenta-0.1.9.tar", max compression
```

## Comparing `agenta-0.1.8.tar` & `agenta-0.1.9.tar`

### file list

```diff
@@ -1,30 +1,30 @@
--rw-r--r--   0        0        0      187 2023-05-31 15:39:19.179107 agenta-0.1.8/README.md
--rw-r--r--   0        0        0      167 2023-06-15 11:20:19.125778 agenta-0.1.8/agenta/__init__.py
--rw-r--r--   0        0        0     2378 2023-06-05 14:29:35.924380 agenta-0.1.8/agenta/cli/helper.py
--rw-r--r--   0        0        0     2108 2023-06-05 14:29:35.924670 agenta-0.1.8/agenta/cli/main.py
--rw-r--r--   0        0        0     9048 2023-06-14 16:46:45.333385 agenta-0.1.8/agenta/cli/variant_commands.py
--rw-r--r--   0        0        0      131 2023-05-15 11:40:40.483678 agenta-0.1.8/agenta/client/Readme.md
--rw-r--r--   0        0        0        0 2023-05-15 11:36:10.263480 agenta-0.1.8/agenta/client/__init__.py
--rw-r--r--   0        0        0      325 2023-05-26 07:42:52.867662 agenta-0.1.8/agenta/client/api_models.py
--rw-r--r--   0        0        0     4355 2023-06-05 14:29:35.925335 agenta-0.1.8/agenta/client/client.py
--rw-r--r--   0        0        0      641 2023-06-14 09:00:50.278508 agenta-0.1.8/agenta/config.py
--rw-r--r--   0        0        0      131 2023-06-14 09:00:50.278836 agenta-0.1.8/agenta/config.toml
--rw-r--r--   0        0        0     3556 2023-06-13 16:45:28.867392 agenta-0.1.8/agenta/docker/backup.py
--rw-r--r--   0        0        0      416 2023-06-14 16:37:25.543970 agenta-0.1.8/agenta/docker/docker-assets/Dockerfile.template
--rw-r--r--   0        0        0      102 2023-05-11 15:47:22.031685 agenta-0.1.8/agenta/docker/docker-assets/README.md
--rwxr-xr-x   0        0        0       43 2023-06-07 09:27:57.848261 agenta-0.1.8/agenta/docker/docker-assets/entrypoint.sh
--rw-r--r--   0        0        0      325 2023-06-14 16:38:07.035581 agenta-0.1.8/agenta/docker/docker-assets/main.py
--rw-r--r--   0        0        0     2905 2023-06-15 11:41:57.531394 agenta-0.1.8/agenta/docker/docker_utils.py
--rw-r--r--   0        0        0      241 2023-06-15 11:10:04.129954 agenta-0.1.8/agenta/sdk/__init__.py
--rw-r--r--   0        0        0     6531 2023-06-15 11:10:04.140988 agenta-0.1.8/agenta/sdk/agenta.py
--rw-r--r--   0        0        0      864 2023-06-15 11:10:04.152507 agenta-0.1.8/agenta/sdk/context.py
--rw-r--r--   0        0        0       87 2023-06-15 11:10:04.169035 agenta-0.1.8/agenta/sdk/init.py
--rw-r--r--   0        0        0      202 2023-06-15 11:40:20.994457 agenta-0.1.8/agenta/sdk/router.py
--rw-r--r--   0        0        0      760 2023-06-15 11:41:35.771121 agenta-0.1.8/agenta/sdk/types.py
--rw-r--r--   0        0        0       43 2023-06-07 08:37:18.934913 agenta-0.1.8/agenta/templates/simple_prompt/.env.example
--rw-r--r--   0        0        0      482 2023-05-31 17:12:43.842983 agenta-0.1.8/agenta/templates/simple_prompt/README.md
--rw-r--r--   0        0        0      660 2023-05-31 17:02:48.853909 agenta-0.1.8/agenta/templates/simple_prompt/app.py
--rw-r--r--   0        0        0       31 2023-05-10 09:29:53.673600 agenta-0.1.8/agenta/templates/simple_prompt/requirements.txt
--rw-r--r--   0        0        0       60 2023-05-15 11:25:55.227110 agenta-0.1.8/agenta/templates/simple_prompt/template.toml
--rw-r--r--   0        0        0      598 2023-06-15 11:44:11.433222 agenta-0.1.8/pyproject.toml
--rw-r--r--   0        0        0      975 1970-01-01 00:00:00.000000 agenta-0.1.8/PKG-INFO
+-rw-r--r--   0        0        0      187 2023-05-31 15:39:19.179107 agenta-0.1.9/README.md
+-rw-r--r--   0        0        0      167 2023-06-15 12:39:19.152533 agenta-0.1.9/agenta/__init__.py
+-rw-r--r--   0        0        0     2378 2023-06-05 14:29:35.924380 agenta-0.1.9/agenta/cli/helper.py
+-rw-r--r--   0        0        0     2108 2023-06-05 14:29:35.924670 agenta-0.1.9/agenta/cli/main.py
+-rw-r--r--   0        0        0     9216 2023-06-15 14:52:51.004447 agenta-0.1.9/agenta/cli/variant_commands.py
+-rw-r--r--   0        0        0      131 2023-05-15 11:40:40.483678 agenta-0.1.9/agenta/client/Readme.md
+-rw-r--r--   0        0        0        0 2023-05-15 11:36:10.263480 agenta-0.1.9/agenta/client/__init__.py
+-rw-r--r--   0        0        0      325 2023-05-26 07:42:52.867662 agenta-0.1.9/agenta/client/api_models.py
+-rw-r--r--   0        0        0     4599 2023-06-15 15:00:16.398983 agenta-0.1.9/agenta/client/client.py
+-rw-r--r--   0        0        0      641 2023-06-14 09:00:50.278508 agenta-0.1.9/agenta/config.py
+-rw-r--r--   0        0        0      131 2023-06-14 09:00:50.278836 agenta-0.1.9/agenta/config.toml
+-rw-r--r--   0        0        0     3556 2023-06-13 16:45:28.867392 agenta-0.1.9/agenta/docker/backup.py
+-rw-r--r--   0        0        0      416 2023-06-15 12:39:19.153091 agenta-0.1.9/agenta/docker/docker-assets/Dockerfile.template
+-rw-r--r--   0        0        0      102 2023-05-11 15:47:22.031685 agenta-0.1.9/agenta/docker/docker-assets/README.md
+-rwxr-xr-x   0        0        0       43 2023-06-07 09:27:57.848261 agenta-0.1.9/agenta/docker/docker-assets/entrypoint.sh
+-rw-r--r--   0        0        0      325 2023-06-15 12:39:19.153350 agenta-0.1.9/agenta/docker/docker-assets/main.py
+-rw-r--r--   0        0        0     3751 2023-06-15 14:41:52.728896 agenta-0.1.9/agenta/docker/docker_utils.py
+-rw-r--r--   0        0        0      241 2023-06-15 12:39:19.153906 agenta-0.1.9/agenta/sdk/__init__.py
+-rw-r--r--   0        0        0     6531 2023-06-15 12:39:19.154239 agenta-0.1.9/agenta/sdk/agenta.py
+-rw-r--r--   0        0        0      864 2023-06-15 12:39:19.154407 agenta-0.1.9/agenta/sdk/context.py
+-rw-r--r--   0        0        0       87 2023-06-15 12:39:19.154606 agenta-0.1.9/agenta/sdk/init.py
+-rw-r--r--   0        0        0      202 2023-06-15 12:39:19.154801 agenta-0.1.9/agenta/sdk/router.py
+-rw-r--r--   0        0        0      760 2023-06-15 12:39:19.154984 agenta-0.1.9/agenta/sdk/types.py
+-rw-r--r--   0        0        0       43 2023-06-07 08:37:18.934913 agenta-0.1.9/agenta/templates/simple_prompt/.env.example
+-rw-r--r--   0        0        0      482 2023-05-31 17:12:43.842983 agenta-0.1.9/agenta/templates/simple_prompt/README.md
+-rw-r--r--   0        0        0      660 2023-05-31 17:02:48.853909 agenta-0.1.9/agenta/templates/simple_prompt/app.py
+-rw-r--r--   0        0        0       31 2023-05-10 09:29:53.673600 agenta-0.1.9/agenta/templates/simple_prompt/requirements.txt
+-rw-r--r--   0        0        0       60 2023-05-15 11:25:55.227110 agenta-0.1.9/agenta/templates/simple_prompt/template.toml
+-rw-r--r--   0        0        0      598 2023-06-15 15:04:04.596750 agenta-0.1.9/pyproject.toml
+-rw-r--r--   0        0        0      975 1970-01-01 00:00:00.000000 agenta-0.1.9/PKG-INFO
```

### Comparing `agenta-0.1.8/agenta/cli/helper.py` & `agenta-0.1.9/agenta/cli/helper.py`

 * *Files identical despite different names*

### Comparing `agenta-0.1.8/agenta/cli/main.py` & `agenta-0.1.9/agenta/cli/main.py`

 * *Files identical despite different names*

### Comparing `agenta-0.1.8/agenta/cli/variant_commands.py` & `agenta-0.1.9/agenta/cli/variant_commands.py`

 * *Files 2% similar despite different names*

```diff
@@ -3,16 +3,16 @@
 from typing import List
 
 import click
 import questionary
 import toml
 from agenta.cli import helper
 from agenta.client import client
-from agenta.client.api_models import AppVariant
-from agenta.docker.docker_utils import build_and_upload_docker_image
+from agenta.client.api_models import AppVariant, Image
+from agenta.docker.docker_utils import build_and_upload_docker_image, build_tar_docker_container
 from docker.models.images import Image as DockerImage
 
 
 @click.group()
 def variant():
     """Commands for variants"""
     pass
@@ -56,24 +56,26 @@
         if not overwrite:
             click.echo("Operation cancelled.")
             sys.exit(0)
 
     if not overwrite:
         config['variants'].append(variant_name)
     try:
-        docker_image: DockerImage = build_and_upload_docker_image(
-            folder=app_path, app_name=app_name, variant_name=variant_name)
+        tar_path = build_tar_docker_container(folder=app_path)
+        image: Image = client.send_docker_tar(app_name, variant_name, tar_path)
+        # docker_image: DockerImage = build_and_upload_docker_image(
+        #     folder=app_path, app_name=app_name, variant_name=variant_name)
     except Exception as ex:
         click.echo(click.style(f"Error while building image: {ex}", fg='red'))
         return None
     try:
         if overwrite:
-            client.update_variant_image(app_name, variant_name, docker_image)
+            client.update_variant_image(app_name, variant_name, image)
         else:
-            client.add_variant_to_server(app_name, variant_name, docker_image)
+            client.add_variant_to_server(app_name, variant_name, image)
     except Exception as ex:
         if overwrite:
             click.echo(click.style(f"Error while updating variant: {ex}", fg='red'))
         else:
             click.echo(click.style(f"Error while adding variant: {ex}", fg='red'))
         return None
     if overwrite:
```

### Comparing `agenta-0.1.8/agenta/client/client.py` & `agenta-0.1.9/agenta/client/client.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,32 +1,31 @@
 import os
+from pathlib import Path
 from typing import List
 
+import agenta.config
 import requests
 from agenta.client.api_models import AppVariant, Image
 from docker.models.images import Image as DockerImage
-import agenta.config
 
 BACKEND_URL = os.environ["BACKEND_ENDPOINT"]
 
 
 class APIRequestError(Exception):
     """Exception to be raised when an API request fails."""
 
 
-def add_variant_to_server(app_name: str, variant_name: str, docker_image: DockerImage):
+def add_variant_to_server(app_name: str, variant_name: str, image: Image):
     """Adds a variant to the server.
 
     Arguments:
         app_name -- Name of the app
         variant_name -- Name of the variant
         image_name -- Name of the image
     """
-    image: Image = Image(docker_id=docker_image.id,
-                         tags=f"{docker_image.tags[0]}")
     app_variant: AppVariant = AppVariant(
         app_name=app_name, variant_name=variant_name)
     response = requests.post(f"{BACKEND_URL}/app_variant/add/from_image/",
                              json={"app_variant": app_variant.dict(), "image": image.dict()}, timeout=600)
     if response.status_code != 200:
         error_message = response.text
         raise APIRequestError(
@@ -87,25 +86,38 @@
     # Check for successful request
     if response.status_code != 200:
         error_message = response.text
         raise APIRequestError(
             f"Request to remove_variant endpoint failed with status code {response.status_code} and error message: {error_message}")
 
 
-def update_variant_image(app_name: str, variant_name: str, docker_image: DockerImage):
+def update_variant_image(app_name: str, variant_name: str, image: Image):
     """Adds a variant to the server.
 
     Arguments:
         app_name -- Name of the app
         variant_name -- Name of the variant
         image_name -- Name of the image
     """
-    image: Image = Image(docker_id=docker_image.id,
-                         tags=f"{docker_image.tags[0]}")
     app_variant: AppVariant = AppVariant(
         app_name=app_name, variant_name=variant_name)
     response = requests.put(f"{BACKEND_URL}/app_variant/update_variant_image/",
                             json={"app_variant": app_variant.dict(), "image": image.dict()}, timeout=600)
     if response.status_code != 200:
         error_message = response.text
         raise APIRequestError(
             f"Request to update app_variant failed with status code {response.status_code} and error message: {error_message}.")
+
+
+def send_docker_tar(app_name: str, variant_name: str, tar_path: Path) -> Image:
+    with tar_path.open('rb') as tar_file:
+        response = requests.post(
+            f"{BACKEND_URL}/containers/build_image/?app_name={app_name}&variant_name={variant_name}",
+            files={
+                'tar_file': tar_file,
+            },
+            timeout=1200
+        )
+
+    response.raise_for_status()
+    image = Image.parse_obj(response.json())
+    return image
```

### Comparing `agenta-0.1.8/agenta/config.py` & `agenta-0.1.9/agenta/config.py`

 * *Files identical despite different names*

### Comparing `agenta-0.1.8/agenta/docker/backup.py` & `agenta-0.1.9/agenta/docker/backup.py`

 * *Files identical despite different names*

### Comparing `agenta-0.1.8/agenta/docker/docker_utils.py` & `agenta-0.1.9/agenta/docker/docker_utils.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 import logging
 import os
 import shutil
 from pathlib import Path
 from tempfile import TemporaryDirectory
 
 import docker
+import tarfile
 from agenta.config import settings
 from docker.models.images import Image
 
 logger = logging.getLogger(__name__)
 logger.setLevel(logging.DEBUG)
 
 
@@ -22,29 +23,55 @@
     dockerfile_template = Path(__file__).parent / \
         "docker-assets" / "Dockerfile.template"
     dockerfile_path = out_folder / "Dockerfile"
     shutil.copy(dockerfile_template, dockerfile_path)
     return dockerfile_path
 
 
+def build_tar_docker_container(folder: Path) -> Path:
+    """Builds the tar file container the files needed for the docker container
+
+    Arguments:
+        folder -- the path containing the code for the app
+
+    Returns:
+        the path to the created tar file
+    """
+
+    dockerfile_path = create_dockerfile(folder)
+    shutil.copytree(Path(__file__).parent.parent / "sdk", folder / "agenta", dirs_exist_ok=True)
+    shutil.copy(Path(__file__).parent /
+                "docker-assets" / "main.py", folder)
+    shutil.copy(Path(__file__).parent /
+                "docker-assets" / "entrypoint.sh", folder)
+    # tar the directory
+
+    tarfile_path = folder/"docker.tar.gz"
+    with tarfile.open(tarfile_path, "w:gz") as tar:
+        tar.add(folder, arcname=folder.name)
+    # dockerfile_path.unlink()
+    return tarfile_path
+
+
 def build_and_upload_docker_image(folder: Path, variant_name: str, app_name: str) -> Image:
-    """Builds an image from the folder and returns the path
+    """
+    DEPRECATED
+    Builds an image from the folder and returns the path
 
     Arguments:
         folder -- The folder containg the app code
 
     Returns:
         The image object
     TODO: Check that the variant name does not exist
     TODO: Deal with different app names (probably we need to look then at multiple tags)
     TODO: Error handling
     """
     # Initialize Docker client
     client = docker.from_env()
-    print(folder)
 
     with TemporaryDirectory() as temp_dir:
         # Create a Dockerfile for the app
         # TODO: Later do this in the temp dir
         dockerfile_path = create_dockerfile(folder)
         shutil.copytree(Path(__file__).parent.parent / "sdk", folder / "agenta",)
         shutil.copy(Path(__file__).parent /
@@ -60,15 +87,14 @@
         tag = f"{registry}/{app_name.lower()}_{variant_name.lower()}:latest"
         print("Building Docker image...")
         try:
             image, build_log = client.images.build(
                 path=temp_dir,
                 tag=tag,
                 buildargs={"ROOT_PATH": f"/{app_name}/{variant_name}"},
-
                 rm=True  # Remove intermediate containers after a successful build
             )
 
         except docker.errors.BuildError as ex:
             logger.error("Error building Docker image:\n")
             # Print the build log
             for line in ex.build_log:
```

### Comparing `agenta-0.1.8/agenta/sdk/agenta.py` & `agenta-0.1.9/agenta/sdk/agenta.py`

 * *Files identical despite different names*

### Comparing `agenta-0.1.8/agenta/sdk/context.py` & `agenta-0.1.9/agenta/sdk/context.py`

 * *Files identical despite different names*

### Comparing `agenta-0.1.8/agenta/sdk/types.py` & `agenta-0.1.9/agenta/sdk/types.py`

 * *Files identical despite different names*

### Comparing `agenta-0.1.8/agenta/templates/simple_prompt/app.py` & `agenta-0.1.9/agenta/templates/simple_prompt/app.py`

 * *Files identical despite different names*

### Comparing `agenta-0.1.8/pyproject.toml` & `agenta-0.1.9/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "agenta"
-version = "0.1.8"
+version = "0.1.9"
 description = "Code for the SDK and CLI for the Agenta Lab platform"
 authors = ["Mahmoud Mabrouk <mahmoudmabrouk.mail@gmail.com>"]
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.9"
 docker = "^6.1.1"
```

### Comparing `agenta-0.1.8/PKG-INFO` & `agenta-0.1.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: agenta
-Version: 0.1.8
+Version: 0.1.9
 Summary: Code for the SDK and CLI for the Agenta Lab platform
 Author: Mahmoud Mabrouk
 Author-email: mahmoudmabrouk.mail@gmail.com
 Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

