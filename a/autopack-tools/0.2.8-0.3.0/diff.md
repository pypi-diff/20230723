# Comparing `tmp/autopack_tools-0.2.8.tar.gz` & `tmp/autopack_tools-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "autopack_tools-0.2.8.tar", max compression
+gzip compressed data, was "autopack_tools-0.3.0.tar", max compression
```

## Comparing `autopack_tools-0.2.8.tar` & `autopack_tools-0.3.0.tar`

### file list

```diff
@@ -1,17 +1,19 @@
--rw-r--r--   0        0        0     1069 2023-06-25 23:21:07.938011 autopack_tools-0.2.8/LICENSE
--rw-r--r--   0        0        0     2862 2023-07-02 21:31:24.435654 autopack_tools-0.2.8/README.md
--rw-r--r--   0        0        0        6 2023-06-25 23:21:01.956323 autopack_tools-0.2.8/autopack/VERSION
--rw-r--r--   0        0        0        0 2023-06-30 20:06:04.842978 autopack_tools-0.2.8/autopack/__init__.py
--rw-r--r--   0        0        0      134 2023-06-25 23:21:01.956609 autopack_tools-0.2.8/autopack/__main__.py
--rw-r--r--   0        0        0     2870 2023-07-04 00:01:05.734894 autopack_tools-0.2.8/autopack/api.py
--rw-r--r--   0        0        0     1116 2023-07-03 23:59:48.436637 autopack_tools-0.2.8/autopack/cli.py
--rw-r--r--   0        0        0      317 2023-06-29 18:48:28.424876 autopack_tools-0.2.8/autopack/errors.py
--rw-r--r--   0        0        0     2698 2023-07-03 23:58:29.022022 autopack_tools-0.2.8/autopack/get_pack.py
--rw-r--r--   0        0        0     3804 2023-07-12 23:56:33.101607 autopack_tools-0.2.8/autopack/installation.py
--rw-r--r--   0        0        0     2976 2023-07-10 03:48:17.484061 autopack_tools-0.2.8/autopack/pack.py
--rw-r--r--   0        0        0      676 2023-07-04 00:56:08.699966 autopack_tools-0.2.8/autopack/pack_response.py
--rw-r--r--   0        0        0      455 2023-06-29 21:34:17.271996 autopack_tools-0.2.8/autopack/search.py
--rw-r--r--   0        0        0     2625 2023-07-12 23:24:57.527362 autopack_tools-0.2.8/autopack/selection.py
--rw-r--r--   0        0        0     3874 2023-07-12 23:56:37.571529 autopack_tools-0.2.8/autopack/utils.py
--rw-r--r--   0        0        0     1005 2023-07-12 23:57:13.494760 autopack_tools-0.2.8/pyproject.toml
--rw-r--r--   0        0        0     3657 1970-01-01 00:00:00.000000 autopack_tools-0.2.8/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-06-25 23:21:07.938011 autopack_tools-0.3.0/LICENSE
+-rw-r--r--   0        0        0     2862 2023-07-02 21:31:24.435654 autopack_tools-0.3.0/README.md
+-rw-r--r--   0        0        0        6 2023-06-25 23:21:01.956323 autopack_tools-0.3.0/autopack/VERSION
+-rw-r--r--   0        0        0       51 2023-07-22 21:10:26.696185 autopack_tools-0.3.0/autopack/__init__.py
+-rw-r--r--   0        0        0      134 2023-06-25 23:21:01.956609 autopack_tools-0.3.0/autopack/__main__.py
+-rw-r--r--   0        0        0     2996 2023-07-23 04:25:50.740940 autopack_tools-0.3.0/autopack/api.py
+-rw-r--r--   0        0        0     1091 2023-07-22 21:45:58.090041 autopack_tools-0.3.0/autopack/cli.py
+-rw-r--r--   0        0        0      317 2023-07-22 20:36:24.222128 autopack_tools-0.3.0/autopack/errors.py
+-rw-r--r--   0        0        0     2568 2023-07-23 01:25:16.569309 autopack_tools-0.3.0/autopack/get_pack.py
+-rw-r--r--   0        0        0     3935 2023-07-23 04:34:40.466812 autopack_tools-0.3.0/autopack/installation.py
+-rw-r--r--   0        0        0     5017 2023-07-23 05:42:45.831435 autopack_tools-0.3.0/autopack/pack.py
+-rw-r--r--   0        0        0      252 2023-07-22 21:40:46.525129 autopack_tools-0.3.0/autopack/pack_response.py
+-rw-r--r--   0        0        0      393 2023-07-22 23:02:14.133585 autopack_tools-0.3.0/autopack/pack_search_response.py
+-rw-r--r--   0        0        0     2217 2023-07-22 21:58:39.610211 autopack_tools-0.3.0/autopack/prompts.py
+-rw-r--r--   0        0        0      394 2023-07-22 23:03:16.870292 autopack_tools-0.3.0/autopack/search.py
+-rw-r--r--   0        0        0     2955 2023-07-23 02:03:04.865063 autopack_tools-0.3.0/autopack/selection.py
+-rw-r--r--   0        0        0     7904 2023-07-23 05:25:55.315020 autopack_tools-0.3.0/autopack/utils.py
+-rw-r--r--   0        0        0     1061 2023-07-23 02:46:27.020017 autopack_tools-0.3.0/pyproject.toml
+-rw-r--r--   0        0        0     3709 1970-01-01 00:00:00.000000 autopack_tools-0.3.0/PKG-INFO
```

### Comparing `autopack_tools-0.2.8/LICENSE` & `autopack_tools-0.3.0/LICENSE`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.2.8/README.md` & `autopack_tools-0.3.0/README.md`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.2.8/autopack/api.py` & `autopack_tools-0.3.0/autopack/api.py`

 * *Files 26% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 from urllib.parse import urljoin
 
 import requests
 from marshmallow import ValidationError
 
 from autopack.errors import AutoPackFetchError
 from autopack.pack_response import PackResponse
+from autopack.pack_search_response import PackSearchResponse
 from autopack.utils import find_or_create_autopack_dir
 
 API_URL = os.environ.get("AUTOPACK_API_URL", "https://autopack.ai/")
 
 
 def get_pack_details(pack_id: str, remote=False) -> PackResponse:
     if remote:
@@ -22,31 +23,25 @@
 
 def get_pack_details_locally(pack_id: str) -> PackResponse:
     metadata_dir = find_or_create_autopack_dir()
 
     metadata_file = os.path.join(metadata_dir, "pack_metadata.json")
 
     if not os.path.exists(metadata_file):
-        raise AutoPackFetchError(
-            f"Metadata file does not exist, please install or re-install {pack_id}."
-        )
+        raise AutoPackFetchError(f"Metadata file does not exist, please install or re-install {pack_id}.")
 
     with open(metadata_file, "r") as f:
         try:
             metadata = json.load(f)
         except JSONDecodeError as e:
-            raise AutoPackFetchError(
-                f"Could  can't fetch locally. Please install or re-install {pack_id}. {e}"
-            )
+            raise AutoPackFetchError(f"Could  can't fetch locally. Please install or re-install {pack_id}. {e}")
 
     pack_metadata = metadata.get(pack_id)
     if not pack_metadata:
-        raise AutoPackFetchError(
-            f"Could  can't find pack locally. Please install {pack_id}"
-        )
+        raise AutoPackFetchError(f"Could  can't find pack locally. Please install {pack_id}")
 
     return PackResponse(**pack_metadata)
 
 
 def get_pack_details_remotely(pack_id: str) -> PackResponse:
     endpoint = "/api/details"
 
@@ -54,36 +49,38 @@
     params = {"id": pack_id}
 
     response = requests.get(url, params=params)
     if response.status_code == 200:
         data = response.json()
 
         try:
-            return PackResponse(**data)
+            return PackResponse(
+                package_path=data.get("package_path"), class_name=data.get("class_name"), repo_url=data.get("repo_url")
+            )
         except (ValidationError, TypeError) as e:
             message = f"Pack fetch received invalid data: {e}"
             raise AutoPackFetchError(message)
 
     elif response.status_code <= 500:
         raise AutoPackFetchError(f"Error: {response.status_code}")
     else:
         raise AutoPackFetchError(f"Error: {response.status_code}")
 
 
-def pack_search(query: str) -> list[PackResponse]:
+def pack_search(query: str) -> list[PackSearchResponse]:
     endpoint = "/api/search"
     url = urljoin(API_URL, endpoint)
     params = {"query": query}
 
     response = requests.get(url, params=params)
     if response.status_code == 200:
         data = response.json()
 
         try:
-            return [PackResponse(**datum) for datum in data["packs"]]
+            return [PackSearchResponse(**datum) for datum in data["packs"]]
         except (ValidationError, TypeError) as e:
             message = f"Pack fetch received invalid data: {e}"
             print(message)
             raise AutoPackFetchError(message)
 
     elif response.status_code <= 500:
         print(f"Error: {response.status_code}")
```

### Comparing `autopack_tools-0.2.8/autopack/cli.py` & `autopack_tools-0.3.0/autopack/cli.py`

 * *Files 10% similar despite different names*

```diff
@@ -5,17 +5,15 @@
 
 
 def parse_args():
     parser = argparse.ArgumentParser(description="AutoPack CLI tool")
 
     subparsers = parser.add_subparsers(dest="command")
     install_parser = subparsers.add_parser("install", help="Install a pack")
-    install_parser.add_argument(
-        "pack", help="ID (author/repo/pack_name) of the pack to install"
-    )
+    install_parser.add_argument("pack", help="ID of the pack to install")
 
     search_parser = subparsers.add_parser("search", help="Search for packs")
     search_parser.add_argument("query", help="The search query")
 
     parser.add_argument(
         "-f",
         "--force",
@@ -26,15 +24,15 @@
     return parser.parse_args()
 
 
 def main():
     args = parse_args()
 
     if args.command == "install":
-        result = install_pack(args.pack, args.force)
+        result = install_pack(args.pack, args.force, quiet=False)
         if result:
             print("Installation completed")
         else:
             print("Installation failed")
 
     if args.command == "search":
         print_search(args.query)
```

### Comparing `autopack_tools-0.2.8/autopack/get_pack.py` & `autopack_tools-0.3.0/autopack/get_pack.py`

 * *Files 14% similar despite different names*

```diff
@@ -2,62 +2,63 @@
 
 from autopack.api import get_pack_details
 from autopack.errors import AutoPackError, AutoPackNotFoundError
 from autopack.pack import Pack
 from autopack.utils import fetch_pack_object, load_metadata_file
 
 
-def try_get_pack(pack_id: str, quiet=False, remote=False) -> Union[Pack, None]:
+def try_get_pack(pack_id: str, remote=False) -> Union[type[Pack], None]:
     """
-    Get a pack based on its ID, in `author/repo_name/pack_name` format. Same as `get_pack` but does not raise an
-    Exception. If there is a problem finding or loading a pack it will return None.
+    Get a pack based on its ID. Same as `get_pack` but does not raise an Exception. If there is a problem finding or
+    loading a pack it will return None.
 
     Args:
         pack_id (str): The ID of the pack to fetch.
         quiet (bool, Optional): If True, won't print any output
         remote (bool, Optional): If True, will make network requests to fetch pack metadata
 
     Returns:
         Pack or None: The fetched pack, None if the pack could not be loaded
     """
 
     try:
-        return get_pack(pack_id, quiet=quiet, remote=remote)
+        return get_pack(pack_id, remote=remote)
     except AutoPackError:
         return None
 
 
-def get_all_installed_packs(quiet=False):
+def get_all_installed_packs():
+    """Returns all of the"""
     metadata = load_metadata_file()
     pack_ids = list(metadata.keys())
-    return try_get_packs(pack_ids, quiet=quiet, remote=False)
+    return try_get_packs(pack_ids, remote=False)
 
 
-def try_get_packs(pack_ids: list[str], quiet=False, remote=False) -> list[Pack]:
+def try_get_packs(pack_ids: list[str], remote=False) -> list[type[Pack]]:
     """
-    Get a list of packs based on their IDs, in `author/repo_name/pack_name` format.
+    Get a list of packs based on their IDs
 
     Args:
         pack_ids (list[str]): The IDs of the packs to fetch.
         quiet (bool, Optional): If True, won't print any output
         remote (bool, Optional): If True, will make network requests to fetch pack metadata
 
     Returns:
         list[Pack]: The successfully fetched packs
     """
     packs = []
     for pack_id in pack_ids:
-        pack = try_get_pack(pack_id, quiet, remote)
+        pack = try_get_pack(pack_id, remote)
         if pack:
             packs.append(pack)
 
     return packs
 
 
-def get_pack(pack_id: str, quiet=False, remote=False) -> Pack:
+def get_pack(pack_id: str, remote=False) -> type[Pack]:
     """
     Get a pack based on its ID, in `author/repo_name/pack_name` format.
 
     Args:
         pack_id (str): The ID of the pack to fetch.
         quiet (bool, Optional): If True, won't print any output
         remote (bool, Optional): If True, will make network requests to fetch pack metadata
@@ -72,8 +73,8 @@
         AutoPackLoadError: If the pack was found but there was an error importing or finding the pack class.
     """
     pack_data = get_pack_details(pack_id, remote=remote)
 
     if not pack_data:
         raise AutoPackNotFoundError()
 
-    return fetch_pack_object(pack_data, quiet=quiet)
+    return fetch_pack_object(pack_data)
```

### Comparing `autopack_tools-0.2.8/pyproject.toml` & `autopack_tools-0.3.0/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "autopack-tools"
-version = "0.2.8"
+version = "0.3.0"
 repository = "https://github.com/AutoPackAI/autopack"
 homepage = "https://autopack.ai"
 description = "Package Manager for AI Agent tools"
 authors = ["Erik Peterson <e@eriklp.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{ include = "autopack" }]
@@ -15,28 +15,30 @@
 [tool.poetry.dependencies]
 python = ">=3.8.1,<4.0"
 requests = "^2.31.0"
 dataclasses-json = "^0.5.8"
 urllib3 = "^1.26.16"
 gitpython = "^3.1.31"
 langchain = ">=0.0.215"
+types-requests = "^2.31.0.2"
 
 [tool.poetry.group.dev.dependencies]
 black = "^23.3.0"
 flake8 = "^6.0.0"
 mypy = "^1.4.0"
 isort = "^5.12.0"
 pytest = "^7.3.2"
 pytest-mock = "^3.11.1"
 types-requests = "^2.31.0.1"
 psycopg2 = "^2.9.6"
 autoflake = "^2.2.0"
 types-psycopg2 = "^2.9.21.10"
 pipreqs = "^0.4.13"
 gitpython = "^3.1.31"
+pytest-asyncio = "^0.21.1"
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.ruff]
 line-length = 120
```

### Comparing `autopack_tools-0.2.8/PKG-INFO` & `autopack_tools-0.3.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: autopack-tools
-Version: 0.2.8
+Version: 0.3.0
 Summary: Package Manager for AI Agent tools
 Home-page: https://autopack.ai
 License: MIT
 Author: Erik Peterson
 Author-email: e@eriklp.com
 Requires-Python: >=3.8.1,<4.0
 Classifier: License :: OSI Approved :: MIT License
@@ -12,14 +12,15 @@
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: dataclasses-json (>=0.5.8,<0.6.0)
 Requires-Dist: gitpython (>=3.1.31,<4.0.0)
 Requires-Dist: langchain (>=0.0.215)
 Requires-Dist: requests (>=2.31.0,<3.0.0)
+Requires-Dist: types-requests (>=2.31.0.2,<3.0.0.0)
 Requires-Dist: urllib3 (>=1.26.16,<2.0.0)
 Project-URL: Repository, https://github.com/AutoPackAI/autopack
 Description-Content-Type: text/markdown
 
 # AutoPack
 
 AutoPack is a Python library and CLI designed to interact with the [AutoPack repository](https://autopack.ai), a
```

