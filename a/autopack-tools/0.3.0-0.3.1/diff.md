# Comparing `tmp/autopack_tools-0.3.0.tar.gz` & `tmp/autopack_tools-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "autopack_tools-0.3.0.tar", max compression
+gzip compressed data, was "autopack_tools-0.3.1.tar", max compression
```

## Comparing `autopack_tools-0.3.0.tar` & `autopack_tools-0.3.1.tar`

### file list

```diff
@@ -1,19 +1,19 @@
--rw-r--r--   0        0        0     1069 2023-06-25 23:21:07.938011 autopack_tools-0.3.0/LICENSE
--rw-r--r--   0        0        0     2862 2023-07-02 21:31:24.435654 autopack_tools-0.3.0/README.md
--rw-r--r--   0        0        0        6 2023-06-25 23:21:01.956323 autopack_tools-0.3.0/autopack/VERSION
--rw-r--r--   0        0        0       51 2023-07-22 21:10:26.696185 autopack_tools-0.3.0/autopack/__init__.py
--rw-r--r--   0        0        0      134 2023-06-25 23:21:01.956609 autopack_tools-0.3.0/autopack/__main__.py
--rw-r--r--   0        0        0     2996 2023-07-23 04:25:50.740940 autopack_tools-0.3.0/autopack/api.py
--rw-r--r--   0        0        0     1091 2023-07-22 21:45:58.090041 autopack_tools-0.3.0/autopack/cli.py
--rw-r--r--   0        0        0      317 2023-07-22 20:36:24.222128 autopack_tools-0.3.0/autopack/errors.py
--rw-r--r--   0        0        0     2568 2023-07-23 01:25:16.569309 autopack_tools-0.3.0/autopack/get_pack.py
--rw-r--r--   0        0        0     3935 2023-07-23 04:34:40.466812 autopack_tools-0.3.0/autopack/installation.py
--rw-r--r--   0        0        0     5017 2023-07-23 05:42:45.831435 autopack_tools-0.3.0/autopack/pack.py
--rw-r--r--   0        0        0      252 2023-07-22 21:40:46.525129 autopack_tools-0.3.0/autopack/pack_response.py
--rw-r--r--   0        0        0      393 2023-07-22 23:02:14.133585 autopack_tools-0.3.0/autopack/pack_search_response.py
--rw-r--r--   0        0        0     2217 2023-07-22 21:58:39.610211 autopack_tools-0.3.0/autopack/prompts.py
--rw-r--r--   0        0        0      394 2023-07-22 23:03:16.870292 autopack_tools-0.3.0/autopack/search.py
--rw-r--r--   0        0        0     2955 2023-07-23 02:03:04.865063 autopack_tools-0.3.0/autopack/selection.py
--rw-r--r--   0        0        0     7904 2023-07-23 05:25:55.315020 autopack_tools-0.3.0/autopack/utils.py
--rw-r--r--   0        0        0     1061 2023-07-23 02:46:27.020017 autopack_tools-0.3.0/pyproject.toml
--rw-r--r--   0        0        0     3709 1970-01-01 00:00:00.000000 autopack_tools-0.3.0/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-06-25 23:21:07.938011 autopack_tools-0.3.1/LICENSE
+-rw-r--r--   0        0        0     2862 2023-07-02 21:31:24.435654 autopack_tools-0.3.1/README.md
+-rw-r--r--   0        0        0        6 2023-06-25 23:21:01.956323 autopack_tools-0.3.1/autopack/VERSION
+-rw-r--r--   0        0        0       51 2023-07-22 21:10:26.696185 autopack_tools-0.3.1/autopack/__init__.py
+-rw-r--r--   0        0        0      134 2023-06-25 23:21:01.956609 autopack_tools-0.3.1/autopack/__main__.py
+-rw-r--r--   0        0        0     2869 2023-07-23 21:13:30.082198 autopack_tools-0.3.1/autopack/api.py
+-rw-r--r--   0        0        0     1091 2023-07-22 21:45:58.090041 autopack_tools-0.3.1/autopack/cli.py
+-rw-r--r--   0        0        0      317 2023-07-22 20:36:24.222128 autopack_tools-0.3.1/autopack/errors.py
+-rw-r--r--   0        0        0     2568 2023-07-23 01:25:16.569309 autopack_tools-0.3.1/autopack/get_pack.py
+-rw-r--r--   0        0        0     3935 2023-07-23 04:34:40.466812 autopack_tools-0.3.1/autopack/installation.py
+-rw-r--r--   0        0        0     5029 2023-07-23 20:21:14.829622 autopack_tools-0.3.1/autopack/pack.py
+-rw-r--r--   0        0        0      252 2023-07-22 21:40:46.525129 autopack_tools-0.3.1/autopack/pack_response.py
+-rw-r--r--   0        0        0      393 2023-07-22 23:02:14.133585 autopack_tools-0.3.1/autopack/pack_search_response.py
+-rw-r--r--   0        0        0     2217 2023-07-22 21:58:39.610211 autopack_tools-0.3.1/autopack/prompts.py
+-rw-r--r--   0        0        0      394 2023-07-22 23:03:16.870292 autopack_tools-0.3.1/autopack/search.py
+-rw-r--r--   0        0        0     3604 2023-07-23 21:07:17.383625 autopack_tools-0.3.1/autopack/selection.py
+-rw-r--r--   0        0        0     7904 2023-07-23 05:25:55.315020 autopack_tools-0.3.1/autopack/utils.py
+-rw-r--r--   0        0        0     1080 2023-07-23 21:13:44.586806 autopack_tools-0.3.1/pyproject.toml
+-rw-r--r--   0        0        0     3709 1970-01-01 00:00:00.000000 autopack_tools-0.3.1/PKG-INFO
```

### Comparing `autopack_tools-0.3.0/LICENSE` & `autopack_tools-0.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.0/README.md` & `autopack_tools-0.3.1/README.md`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.0/autopack/api.py` & `autopack_tools-0.3.1/autopack/api.py`

 * *Files 18% similar despite different names*

```diff
@@ -49,17 +49,15 @@
     params = {"id": pack_id}
 
     response = requests.get(url, params=params)
     if response.status_code == 200:
         data = response.json()
 
         try:
-            return PackResponse(
-                package_path=data.get("package_path"), class_name=data.get("class_name"), repo_url=data.get("repo_url")
-            )
+            return PackResponse(**data)
         except (ValidationError, TypeError) as e:
             message = f"Pack fetch received invalid data: {e}"
             raise AutoPackFetchError(message)
 
     elif response.status_code <= 500:
         raise AutoPackFetchError(f"Error: {response.status_code}")
     else:
```

### Comparing `autopack_tools-0.3.0/autopack/cli.py` & `autopack_tools-0.3.1/autopack/cli.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.0/autopack/get_pack.py` & `autopack_tools-0.3.1/autopack/get_pack.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.0/autopack/installation.py` & `autopack_tools-0.3.1/autopack/installation.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.0/autopack/pack.py` & `autopack_tools-0.3.1/autopack/pack.py`

 * *Files 1% similar despite different names*

```diff
@@ -72,15 +72,16 @@
 
         return self._run(*args, **kwargs)
 
     async def arun(self, *args, **kwargs):
         """Asynchronously execute the _arun function of the subclass, verifying the arguments. (Will eventually do
         callbacks or some such)
 
-        Args: **kwargs (dict): The arguments to pass to _arun. Each key should be the name of an argument,
+        Args:
+            **kwargs (dict): The arguments to pass to _arun. Each key should be the name of an argument,
         and the value should be the value of the argument.
 
         Returns:
             str: The response from the _arun function of the subclass
         """
         try:
             # Validate the arguments
```

### Comparing `autopack_tools-0.3.0/autopack/prompts.py` & `autopack_tools-0.3.1/autopack/prompts.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.0/autopack/selection.py` & `autopack_tools-0.3.1/autopack/selection.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,64 +1,76 @@
 import re
 from typing import Callable, Union, Optional
 
 from langchain.chat_models.base import BaseChatModel
 
 from autopack.api import pack_search
 from autopack.get_pack import try_get_pack
+from autopack.installation import install_pack
 from autopack.prompts import GET_MORE_TOOLS_TEMPLATE, TOOL_SELECTION_TEMPLATE
 from autopack.utils import functions_bulleted_list, call_llm
 
 
-def select_packs_prompt(task_description: str, function_request: Optional[str] = None) -> str:
+def select_packs_prompt(task_description: str, function_request: Optional[str] = None, installed_only=False) -> str:
     """
     Generate a prompt for the pack selection process based on the task description and an optional function request.
 
     Args:
         task_description (str): A description of the task to be used when selecting tools.
         function_request (Optional[str]): A specific type of function asked for (e.g. a `get_more_tools` function).
+        installed_only (Optional[bool]): If True will only use already-installed pack. If False will install the packs.
 
     Returns:
         str: A prompt that can be fed to the LLM for pack selection.
     """
 
     pack_ids = [pack.pack_id for pack in pack_search("")]
-    fetched_packs = [try_get_pack(pack_id) for pack_id in pack_ids]
-    installed_packs = [pack for pack in fetched_packs if pack is not None]
+    if installed_only:
+        fetched_packs = [try_get_pack(pack_id) for pack_id in pack_ids]
+        installed_packs = [pack for pack in fetched_packs if pack is not None]
+    else:
+        fetched_packs = [install_pack(pack_id, force_dependencies=True) for pack_id in pack_ids]
+        installed_packs = [pack for pack in fetched_packs if pack is not None]
 
     if function_request:
         return TOOL_SELECTION_TEMPLATE.format(task=task_description, functions=functions_bulleted_list(installed_packs))
 
     return GET_MORE_TOOLS_TEMPLATE.format(
         task=task_description,
         functions=functions_bulleted_list(installed_packs),
-        function_request=function_request,
+        functions_request=function_request,
     )
 
 
 def select_packs(
-    task_description: str, llm: Union[BaseChatModel, Callable], function_request: Optional[str] = None
+    task_description: str,
+    llm: Union[BaseChatModel, Callable],
+    function_request: Optional[str] = None,
+    installed_only=False,
 ) -> list[str]:
     """Given a user input describing the task they wish to accomplish, return a list of Pack IDs that the given LLM
     thinks will be suitable for this task.
 
     This is good for a "pre-processing" step after receiving the task but before trying to solve it. This allows you
     to benefit from the wide tool selection while keeping your token usage low.
 
     You can then further filter, install the packs if desired, and then fetch them using get_pack().
 
+    # TODO: Include user-provided packs into selection
+
     Args:
         task_description (str): A description of the task to be used when selecting tools
         llm (BaseChatModel): An LLM which will be used to evaluate the selection
         function_request (Optional[str]): A specific type of function asked for (e.g. a `get_more_tools` function)
+        installed_only (Optional[bool]): If True will only use already-installed pack. If False will install the packs.
 
     Returns:
         list[str]: A list of selected Pack IDs
     """
-    prompt = select_packs_prompt(task_description, function_request)
+    prompt = select_packs_prompt(task_description, function_request, installed_only=installed_only)
 
     response = call_llm(prompt, llm)
 
     return parse_selection_response(response)
 
 
 def parse_selection_response(response: str) -> list[str]:
```

### Comparing `autopack_tools-0.3.0/autopack/utils.py` & `autopack_tools-0.3.1/autopack/utils.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.0/pyproject.toml` & `autopack_tools-0.3.1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "autopack-tools"
-version = "0.3.0"
+version = "0.3.1"
 repository = "https://github.com/AutoPackAI/autopack"
 homepage = "https://autopack.ai"
 description = "Package Manager for AI Agent tools"
 authors = ["Erik Peterson <e@eriklp.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{ include = "autopack" }]
@@ -31,14 +31,15 @@
 types-requests = "^2.31.0.1"
 psycopg2 = "^2.9.6"
 autoflake = "^2.2.0"
 types-psycopg2 = "^2.9.21.10"
 pipreqs = "^0.4.13"
 gitpython = "^3.1.31"
 pytest-asyncio = "^0.21.1"
+openai = "^0.27.8"
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.ruff]
 line-length = 120
```

### Comparing `autopack_tools-0.3.0/PKG-INFO` & `autopack_tools-0.3.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: autopack-tools
-Version: 0.3.0
+Version: 0.3.1
 Summary: Package Manager for AI Agent tools
 Home-page: https://autopack.ai
 License: MIT
 Author: Erik Peterson
 Author-email: e@eriklp.com
 Requires-Python: >=3.8.1,<4.0
 Classifier: License :: OSI Approved :: MIT License
```

