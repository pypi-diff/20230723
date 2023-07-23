# Comparing `tmp/devchat-0.1.9.tar.gz` & `tmp/devchat-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "devchat-0.1.9.tar", last modified: Sat May 27 15:17:23 2023, max compression
+gzip compressed data, was "devchat-0.2.0.tar", max compression
```

## Comparing `devchat-0.1.9.tar` & `devchat-0.2.0.tar`

### file list

```diff
@@ -1,35 +1,16 @@
-drwxr-xr-x   0 basicthinker   (501) staff       (20)        0 2023-05-27 15:17:23.126145 devchat-0.1.9/
--rw-r--r--   0 basicthinker   (501) staff       (20)    11357 2023-05-05 13:17:54.000000 devchat-0.1.9/LICENSE
--rw-r--r--   0 basicthinker   (501) staff       (20)     5663 2023-05-27 15:17:23.125984 devchat-0.1.9/PKG-INFO
--rw-r--r--   0 basicthinker   (501) staff       (20)     5207 2023-05-27 11:05:16.000000 devchat-0.1.9/README.md
-drwxr-xr-x   0 basicthinker   (501) staff       (20)        0 2023-05-27 15:17:23.122390 devchat-0.1.9/devchat/
--rw-r--r--   0 basicthinker   (501) staff       (20)        0 2023-05-05 13:17:54.000000 devchat-0.1.9/devchat/__init__.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     6242 2023-05-27 11:39:49.000000 devchat-0.1.9/devchat/_cli.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     4813 2023-05-27 12:10:59.000000 devchat-0.1.9/devchat/assistant.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     1682 2023-05-21 14:33:17.000000 devchat-0.1.9/devchat/chat.py
--rw-r--r--   0 basicthinker   (501) staff       (20)      566 2023-05-22 04:56:01.000000 devchat-0.1.9/devchat/message.py
-drwxr-xr-x   0 basicthinker   (501) staff       (20)        0 2023-05-27 15:17:23.124276 devchat-0.1.9/devchat/openai/
--rw-r--r--   0 basicthinker   (501) staff       (20)      248 2023-05-05 13:17:54.000000 devchat-0.1.9/devchat/openai/__init__.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     3083 2023-05-27 12:37:25.000000 devchat-0.1.9/devchat/openai/openai_chat.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     1561 2023-05-07 23:44:52.000000 devchat-0.1.9/devchat/openai/openai_message.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     6031 2023-05-22 11:27:42.000000 devchat-0.1.9/devchat/openai/openai_prompt.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     6767 2023-05-27 12:09:06.000000 devchat-0.1.9/devchat/prompt.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     4463 2023-05-27 12:07:58.000000 devchat-0.1.9/devchat/store.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     5076 2023-05-27 11:36:22.000000 devchat-0.1.9/devchat/utils.py
-drwxr-xr-x   0 basicthinker   (501) staff       (20)        0 2023-05-27 15:17:23.123509 devchat-0.1.9/devchat.egg-info/
--rw-r--r--   0 basicthinker   (501) staff       (20)     5663 2023-05-27 15:17:23.000000 devchat-0.1.9/devchat.egg-info/PKG-INFO
--rw-r--r--   0 basicthinker   (501) staff       (20)      628 2023-05-27 15:17:23.000000 devchat-0.1.9/devchat.egg-info/SOURCES.txt
--rw-r--r--   0 basicthinker   (501) staff       (20)        1 2023-05-27 15:17:23.000000 devchat-0.1.9/devchat.egg-info/dependency_links.txt
--rw-r--r--   0 basicthinker   (501) staff       (20)       46 2023-05-27 15:17:23.000000 devchat-0.1.9/devchat.egg-info/entry_points.txt
--rw-r--r--   0 basicthinker   (501) staff       (20)      130 2023-05-27 15:17:23.000000 devchat-0.1.9/devchat.egg-info/requires.txt
--rw-r--r--   0 basicthinker   (501) staff       (20)       14 2023-05-27 15:17:23.000000 devchat-0.1.9/devchat.egg-info/top_level.txt
--rw-r--r--   0 basicthinker   (501) staff       (20)      102 2023-05-05 13:17:54.000000 devchat-0.1.9/pyproject.toml
--rw-r--r--   0 basicthinker   (501) staff       (20)       38 2023-05-27 15:17:23.126185 devchat-0.1.9/setup.cfg
--rw-r--r--   0 basicthinker   (501) staff       (20)     1112 2023-05-27 15:15:31.000000 devchat-0.1.9/setup.py
-drwxr-xr-x   0 basicthinker   (501) staff       (20)        0 2023-05-27 15:17:23.125669 devchat-0.1.9/tests/
--rw-r--r--   0 basicthinker   (501) staff       (20)        0 2023-05-05 13:17:54.000000 devchat-0.1.9/tests/__init__.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     5996 2023-05-22 06:00:29.000000 devchat-0.1.9/tests/test_cli.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     1809 2023-05-07 23:44:52.000000 devchat-0.1.9/tests/test_openai_message.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     5887 2023-05-22 11:37:12.000000 devchat-0.1.9/tests/test_openai_prompt.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     2221 2023-05-21 23:12:05.000000 devchat-0.1.9/tests/test_store.py
--rw-r--r--   0 basicthinker   (501) staff       (20)     1225 2023-05-07 23:44:52.000000 devchat-0.1.9/tests/test_utils.py
+-rw-r--r--   0        0        0    11357 2023-07-05 11:57:19.300520 devchat-0.2.0/LICENSE
+-rw-r--r--   0        0        0     5267 2023-07-13 11:26:05.138364 devchat-0.2.0/README.md
+-rw-r--r--   0        0        0        0 2023-07-05 11:57:31.893875 devchat-0.2.0/devchat/__init__.py
+-rw-r--r--   0        0        0     9475 2023-07-22 04:20:24.586852 devchat-0.2.0/devchat/_cli.py
+-rw-r--r--   0        0        0     4503 2023-07-21 16:39:59.449026 devchat-0.2.0/devchat/assistant.py
+-rw-r--r--   0        0        0     1676 2023-07-21 16:39:59.449400 devchat-0.2.0/devchat/chat.py
+-rw-r--r--   0        0        0      758 2023-07-23 12:18:04.254562 devchat-0.2.0/devchat/message.py
+-rw-r--r--   0        0        0      248 2023-07-05 11:57:51.466105 devchat-0.2.0/devchat/openai/__init__.py
+-rw-r--r--   0        0        0     3558 2023-07-23 12:18:04.254963 devchat-0.2.0/devchat/openai/openai_chat.py
+-rw-r--r--   0        0        0     3293 2023-07-23 12:18:04.255359 devchat-0.2.0/devchat/openai/openai_message.py
+-rw-r--r--   0        0        0    10706 2023-07-23 12:18:04.255807 devchat-0.2.0/devchat/openai/openai_prompt.py
+-rw-r--r--   0        0        0     8874 2023-07-21 16:39:59.450857 devchat-0.2.0/devchat/prompt.py
+-rw-r--r--   0        0        0     9872 2023-07-23 12:18:04.256202 devchat-0.2.0/devchat/store.py
+-rw-r--r--   0        0        0     6778 2023-07-23 02:09:55.769806 devchat-0.2.0/devchat/utils.py
+-rw-r--r--   0        0        0     1154 2023-07-23 12:25:42.216663 devchat-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0     6557 1970-01-01 00:00:00.000000 devchat-0.2.0/PKG-INFO
```

### Comparing `devchat-0.1.9/LICENSE` & `devchat-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `devchat-0.1.9/PKG-INFO` & `devchat-0.2.0/README.md`

 * *Files 10% similar despite different names*

```diff
@@ -1,41 +1,29 @@
-Metadata-Version: 2.1
-Name: devchat
-Version: 0.1.9
-Summary: DevChat is an open-source tool that helps developers write prompts to generate code and documentation.
-Home-page: https://github.com/covespace/devchat
-License: Apache License 2.0
-Classifier: Development Status :: 4 - Beta
-Classifier: License :: OSI Approved :: Apache Software License
-Classifier: Programming Language :: Python :: 3
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
 <div align="center">
 
-![devchat](https://github.com/covespace/devchat/assets/592493/f39979fe-fe32-410b-bf9d-2118ac8ea3d5)
+![devchat](https://github.com/devchat-ai/devchat/assets/592493/f39979fe-fe32-410b-bf9d-2118ac8ea3d5)
 
 # DevChat
 
 <br>
 
 [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
-[![CircleCI](https://circleci.com/gh/covespace/devchat/tree/main.svg?style=shield)](https://circleci.com/gh/covespace/devchat/tree/main)
-[![GitHub license](https://img.shields.io/github/license/covespace/devchat.svg)](https://github.com/covespace/devchat/blob/main/LICENSE)
+[![CircleCI](https://circleci.com/gh/devchat-ai/devchat/tree/main.svg?style=shield)](https://circleci.com/gh/devchat-ai/devchat/tree/main)
+[![GitHub license](https://img.shields.io/github/license/devchat-ai/devchat.svg)](https://github.com/devchat-ai/devchat/blob/main/LICENSE)
 [![Downloads](https://pepy.tech/badge/devchat)](https://pepy.tech/project/devchat)
 [![PyPI version](https://badge.fury.io/py/devchat.svg)](https://badge.fury.io/py/devchat)
 [![Discord Chat](https://img.shields.io/discord/1106908489114206309?logo=discord)](https://discord.gg/9t3yrbBUXD)
 
 </div>
 <br>
 <div align="left">
 
 The DevChat core library and CLI.
 
-👉 For an enhanced experience and UI, we welcome you to install [Visual Studio Code extension](https://github.com/covespace/devchat-vscode) from [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=merico.devchat)! Enjoy DevChat! 👏
+👉 **For an enhanced experience and UI, we welcome you to install [Visual Studio Code extension](https://github.com/devchat-ai/devchat-vscode) from [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=merico.devchat)! Enjoy DevChat VSCode!** 👏
 
 ***
 
 ## What is DevChat?
 
 DevChat is the open-source solution to help you write prompts to generate code and documentation, going beyond simple code auto-completion.
 It isn't limited to performing predefined operations on short code snippets.
@@ -46,82 +34,80 @@
 
 ## Why DevChat?
 
 - Great output requires great input, to maximize the power of AI, DevChat assists you seamlessly to **provide the right context** to the AI.
     
   Chat history, code, files, directory trees, `git diff --cached`, or the output of any command.
   
-  ![20230523-220717-cut-merged-1684855581224](https://github.com/covespace/devchat-vscode/assets/592493/16bc09e4-4185-4bcb-8d5a-2173b0bfc3ed)
+  ![20230523-220717-cut-merged-1684855581224](https://github.com/devchat-ai/devchat-vscode/assets/592493/16bc09e4-4185-4bcb-8d5a-2173b0bfc3ed)
 
-  ![20230523-220717-00 00 28 206-00 00 44 950](https://github.com/covespace/devchat-vscode/assets/592493/d5556310-bc7f-4abb-86a3-8e76e4aa720e)  
+  ![20230523-220717-00 00 28 206-00 00 44 950](https://github.com/devchat-ai/devchat-vscode/assets/592493/d5556310-bc7f-4abb-86a3-8e76e4aa720e)  
 
 - Once you have generated code with AI, DevChat **streamlines the actions** to properly integrate and ship.
   
   View diffs, copy or insert, commit & sync, or export to documentation, wikis, and more.
   
-  ![20230523-220717-00 00 46 728-00 01 00 120](https://github.com/covespace/devchat-vscode/assets/592493/a2bab011-8e31-47a9-838f-36e43cd2e98c)
+  ![20230523-220717-00 00 46 728-00 01 00 120](https://github.com/devchat-ai/devchat-vscode/assets/592493/a2bab011-8e31-47a9-838f-36e43cd2e98c)
 
-  ![20230523-220717-00 01 00 120-00 01 14 452](https://github.com/covespace/devchat-vscode/assets/592493/31e90fd5-e797-4726-b5b2-5c4dce1c7551)
+  ![20230523-220717-00 01 00 120-00 01 14 452](https://github.com/devchat-ai/devchat-vscode/assets/592493/31e90fd5-e797-4726-b5b2-5c4dce1c7551)
 
 - To guide AI in your work, define **your own workflows** with DevChat.
   
-  ![20230523-220717-00 01 14 614-00 01 41 680](https://github.com/covespace/devchat-vscode/assets/592493/94502efd-781b-448d-b945-dffcc41d7af3)
+  ![20230523-220717-00 01 14 614-00 01 41 680](https://github.com/devchat-ai/devchat-vscode/assets/592493/94502efd-781b-448d-b945-dffcc41d7af3)
 
   Explore more prompt templates, iterative calls to AI, and program operations.
   
 - To ensure the experience fits your preferences, customize **your own experiences** with DevChat.
   
   Open-source, no waiting for opaque feature schedules. Access GPT-4 today and more models in the future.
   
 ## What is Prompt-Centric Software Development (PCSD)?
 
 - The traditional code-centric paradigm is evolving.
 
 - Write prompts to create code. Transform prompts into all the artifacts in software engineering.
 
-  <img width="600" alt="image" src="https://github.com/covespace/devchat/assets/592493/dd32e900-92fd-4fa4-8489-96ed17ab5e0e">
+  <img width="600" alt="image" src="https://github.com/devchat-ai/devchat/assets/592493/dd32e900-92fd-4fa4-8489-96ed17ab5e0e">
 
   <sub>(This image is licensed by devchat.ai under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.)</sub>
   
 - We like to call it DevPromptOps
   
-  <img width="500" alt="image" src="https://github.com/covespace/devchat/assets/592493/e8e1215b-53b0-4473-ab00-0665d33f204a">
+  <img width="500" alt="image" src="https://github.com/devchat-ai/devchat/assets/592493/e8e1215b-53b0-4473-ab00-0665d33f204a">
   
   <sub>(This image is licensed by devchat.ai under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.)</sub>
 
 ***
 
 ## Quick Start
 
-For UI, install the [Visual Studio Code extension](https://github.com/covespace/devchat-vscode) from [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=merico.devchat).
+**For UI, install our [Visual Studio Code extension](https://github.com/devchat-ai/devchat-vscode) from [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=merico.devchat).**
 
 For CLI:
 - Install DevChat by running: `pip install devchat`.
-- Make sure you are working in a Git repository, as DevChat only works within one.
-- Set your [OpenAI API Key](https://platform.openai.com/account/api-keys) by running `export OPENAI_API_KEY="[sk-...]"`.
+- Make sure you are working in a Git or SVN repository, as DevChat only works within one.
+- Set your [OpenAI API Key](https://platform.openai.com/account/api-keys) by running `export OPENAI_API_KEY="[sk-...]"` (or DevChat access key).
 - To access help, use the commands: `devchat --help` and `devchat prompt --help`.
 
 ## Community
 
 - Join our [Discord](https://discord.gg/9t3yrbBUXD)!
-
-- Participate in [discussions](https://github.com/covespace/devchat/discussions)!
+- Participate in [discussions](https://github.com/devchat-ai/devchat/discussions)!
 
 ## Contributing
 
-Issues and pull request are welcome: https://github.com/covespace/devchat/issues
+Issues and pull request are welcome: https://github.com/devchat-ai/devchat/issues
   
 ## Roadmap
 
 - [x] Implement code diff application.
 - [ ] Improve code diff application using code change instructions.
 - [ ] Develop a framework for defining workflows.
-- [ ] Implement topic management.
+- [x] Implement topic management.
 - [ ] Enable interaction with external development tools.
 - [ ] Introduce more selective workflows.
   
 ## Contact
   
 hello@merico.dev
 
 We are creators of [Apache DevLake](https://devlake.apache.org/).
-
```

### Comparing `devchat-0.1.9/devchat/_cli.py` & `devchat-0.2.0/devchat/_cli.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,62 +1,68 @@
 """
 This module contains the main function for the DevChat CLI.
 """
 from contextlib import contextmanager
 import json
-import logging
 import os
 import sys
 from typing import List, Optional, Tuple
+import importlib.metadata
 import rich_click as click
 from devchat.store import Store
 from devchat.openai import OpenAIChatConfig, OpenAIChat
 from devchat.assistant import Assistant
-from devchat.utils import find_git_root, git_ignore, parse_files, setup_logger
-
+from devchat.utils import find_root_dir, git_ignore, parse_files
+from devchat.utils import setup_logger, get_logger
 
+logger = get_logger(__name__)
 click.rich_click.USE_MARKDOWN = True
 
 
 @click.group()
+@click.version_option(importlib.metadata.version("devchat"), '--version',
+                      message='DevChat %(version)s')
 def main():
-    """DevChat CLI: A command-line interface for the DevChat chatbot."""
+    """DevChat CLI: A command-line interface for DevChat."""
 
 
 @contextmanager
 def handle_errors():
     """Handle errors in the CLI."""
     try:
         yield
     except Exception as error:
-        logger = logging.getLogger(__name__)
         logger.exception(error)
         click.echo(f"Error: {error}", err=True)
         sys.exit(os.EX_SOFTWARE)
 
 
 def init_dir() -> Tuple[dict, str]:
-    git_root = find_git_root()
-    chat_dir = os.path.join(git_root, ".chat")
+    root_dir = find_root_dir()
+    if not root_dir:
+        click.echo("Error: Failed to find home to store .chat", err=True)
+        sys.exit(os.EX_DATAERR)
+    chat_dir = os.path.join(root_dir, ".chat")
     if not os.path.exists(chat_dir):
         os.makedirs(chat_dir)
 
     default_config_data = {
-        'model': 'gpt-4',
-        'provider': 'OpenAI',
-        'OpenAI': {
-            'temperature': 0,
-            'stream': True
+        "model": "gpt-4",
+        "tokens-per-prompt": 6000,
+        "provider": "OpenAI",
+        "OpenAI": {
+            "temperature": 0,
+            "stream": True
         }
     }
 
     try:
         with open(os.path.join(chat_dir, 'config.json'), 'r', encoding='utf-8') as file:
             config_data = json.load(file)
-    except FileNotFoundError:
+    except Exception:
         config_data = default_config_data
 
     setup_logger(os.path.join(chat_dir, 'error.log'))
     git_ignore(chat_dir, '*')
     return config_data, chat_dir
 
 
@@ -67,16 +73,24 @@
               help='Input one or more specific previous prompts to include in the current prompt.')
 @click.option('-i', '--instruct', multiple=True,
               help='Add one or more files to the prompt as instructions.')
 @click.option('-c', '--context', multiple=True,
               help='Add one or more files to the prompt as a context.')
 @click.option('-m', '--model', help='Specify the model to temporarily use for the prompt '
               '(prefer to modify .chat/config.json).')
+@click.option('--config', 'config_str',
+              help='Specify a JSON string to overwrite the configuration for this prompt.')
+@click.option('-f', '--functions', type=click.Path(exists=True),
+              help='Path to a JSON file with functions for the prompt.')
+@click.option('-n', '--function-name',
+              help='Specify the function name when the content is the output of a function.')
 def prompt(content: Optional[str], parent: Optional[str], reference: Optional[List[str]],
-           instruct: Optional[List[str]], context: Optional[List[str]], model: Optional[str]):
+           instruct: Optional[List[str]], context: Optional[List[str]],
+           model: Optional[str], config_str: Optional[str] = None,
+           functions: Optional[str] = None, function_name: Optional[str] = None):
     """
     Main function to run the chat application.
 
     This function initializes the chat system based on the specified large language model (LLM),
     and performs interactions with the LLM by sending prompts and retrieving responses.
 
     Examples
@@ -98,41 +112,33 @@
     ```
 
     Note the quotes around EOF in the first line, to prevent the shell from expanding variables.
 
     Configuration
     -------------
 
-    DevChat CLI reads its configuration from `.chat/config.json` in your current Git root directory.
+    DevChat CLI reads its configuration from `.chat/config.json`
+    in your current Git or SVN root directory.
     If the file is not found, it uses the following default configuration:
     ```json
     {
-        "model": "gpt-3.5-turbo",
-        "tokens-per-prompt": 3000,
-        "provider": "OpenAI",
-        "OpenAI": {
-            "temperature": 0
-        }
-    }
-    ```
-
-    To customize the configuration, create `.chat/config.json` in your current Git root directory
-    and modify the settings as needed. We recoommend the following settings:
-    ```json
-    {
         "model": "gpt-4",
         "tokens-per-prompt": 6000,
         "provider": "OpenAI",
         "OpenAI": {
             "temperature": 0,
             "stream": true
         }
     }
     ```
 
+    To customize the configuration, create `.chat/config.json`
+    in your current Git or SVN root directory
+    and modify the settings as needed.
+
     Note: To use OpenAI's APIs, you must have an API key to run the CLI.
     Run the following command line with your API key:
 
     ```bash
     export OPENAI_API_KEY="sk-..."
     ```
 
@@ -149,52 +155,111 @@
         instruct_contents = parse_files(instruct)
         context_contents = parse_files(context)
 
         provider = config.get('provider')
         if provider == 'OpenAI':
             if model is None:
                 model = config['model']
-            openai_config = OpenAIChatConfig(model=model, **config['OpenAI'])
+
+            if config_str is not None:
+                config_json = json.loads(config_str)
+                config['OpenAI'].update(config_json)
+
+            openai_config = OpenAIChatConfig(model=model,
+                                             **config['OpenAI'])
 
             chat = OpenAIChat(openai_config)
             store = Store(chat_dir, chat)
 
             assistant = Assistant(chat, store)
             if 'tokens-per-prompt' in config:
                 assistant.token_limit = config['tokens-per-prompt']
 
+            functions_data = None
+            if functions is not None:
+                with open(functions, 'r', encoding="utf-8") as f_file:
+                    functions_data = json.load(f_file)
             assistant.make_prompt(content, instruct_contents, context_contents,
-                                  parent, reference)
+                                  functions_data, parent, reference,
+                                  function_name=function_name)
 
             for response in assistant.iterate_response():
                 click.echo(response, nl=False)
         else:
             click.echo(f"Error: Invalid LLM in configuration '{provider}'", err=True)
             sys.exit(os.EX_DATAERR)
 
 
 @main.command()
 @click.option('--skip', default=0, help='Skip number prompts before showing the prompt history.')
-@click.option('--max-count', default=100, help='Limit the number of commits to output.')
-def log(skip, max_count):
+@click.option('-n', '--max-count', default=1, help='Limit the number of commits to output.')
+@click.option('-t', '--topic', 'topic_root', default=None,
+              help='Hash of the root prompt of the topic to select prompts from.')
+@click.option('--delete', default=None, help='Delete a leaf prompt from the log.')
+def log(skip, max_count, topic_root, delete):
     """
-    Show the prompt history.
+    Manage the prompt history.
     """
+    if delete and (skip != 0 or max_count != 1 or topic_root is not None):
+        click.echo("Error: The --delete option cannot be used with other options.", err=True)
+        sys.exit(os.EX_USAGE)
+
     config, chat_dir = init_dir()
-    provider = config.get('provider')
-    recent_prompts = []
-    if provider == 'OpenAI':
-        openai_config = OpenAIChatConfig(model=config['model'], **config['OpenAI'])
-        chat = OpenAIChat(openai_config)
-        store = Store(chat_dir, chat)
-        recent_prompts = store.select_recent(skip, skip + max_count)
-    else:
-        click.echo(f"Error: Invalid LLM in configuration '{provider}'", err=True)
-        sys.exit(os.EX_DATAERR)
 
-    logs = []
-    for record in recent_prompts:
-        try:
-            logs.append(record.shortlog())
-        except Exception:
-            continue
-    click.echo(json.dumps(logs, indent=2))
+    with handle_errors():
+        provider = config.get('provider')
+        if provider == 'OpenAI':
+            openai_config = OpenAIChatConfig(model=config['model'], **config['OpenAI'])
+            chat = OpenAIChat(openai_config)
+            store = Store(chat_dir, chat)
+        else:
+            click.echo(f"Error: Invalid LLM in configuration '{provider}'", err=True)
+            sys.exit(os.EX_DATAERR)
+
+        if delete:
+            success = store.delete_prompt(delete)
+            if success:
+                click.echo(f"Prompt {delete} deleted successfully.")
+            else:
+                click.echo(f"Failed to delete prompt {delete}.")
+        else:
+            recent_prompts = store.select_prompts(skip, skip + max_count, topic_root)
+            logs = []
+            for record in recent_prompts:
+                try:
+                    logs.append(record.shortlog())
+                except Exception as exc:
+                    logger.exception(exc)
+                    continue
+            click.echo(json.dumps(logs, indent=2))
+
+
+@main.command()
+@click.option('--list', '-l', 'list_topics', is_flag=True,
+              help='List topics in reverse chronological order.')
+@click.option('--skip', default=0, help='Skip number of topics before showing the list.')
+@click.option('-n', '--max-count', default=100, help='Limit the number of topics to output.')
+def topic(list_topics: bool, skip: int, max_count: int):
+    """
+    Manage topics.
+    """
+    config, chat_dir = init_dir()
+
+    with handle_errors():
+        provider = config.get('provider')
+        if provider == 'OpenAI':
+            openai_config = OpenAIChatConfig(model=config['model'], **config['OpenAI'])
+            chat = OpenAIChat(openai_config)
+            store = Store(chat_dir, chat)
+        else:
+            click.echo(f"Error: Invalid LLM in configuration '{provider}'", err=True)
+            sys.exit(os.EX_DATAERR)
+
+        if list_topics:
+            topics = store.select_topics(skip, skip + max_count)
+            for topic_data in topics:
+                try:
+                    topic_data.update({'root_prompt': topic_data['root_prompt'].shortlog()})
+                except Exception as exc:
+                    logger.exception(exc)
+                    continue
+            click.echo(json.dumps(topics, indent=2))
```

### Comparing `devchat-0.1.9/devchat/assistant.py` & `devchat-0.2.0/devchat/assistant.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,16 +1,15 @@
-import logging
 from typing import Optional, List, Iterator
 from devchat.message import Message
 from devchat.chat import Chat
-from devchat.prompt import Prompt
 from devchat.store import Store
+from devchat.utils import get_logger
 
 
-logger = logging.getLogger(__name__)
+logger = get_logger(__name__)
 
 
 class Assistant:
     def __init__(self, chat: Chat, store: Store):
         """
         Initializes an Assistant object.
 
@@ -29,87 +28,81 @@
     def _check_limit(self):
         if self._prompt.request_tokens > self.token_limit:
             raise ValueError(f"Prompt tokens {self._prompt.request_tokens} "
                              f"beyond limit {self.token_limit}.")
 
     def make_prompt(self, request: str,
                     instruct_contents: Optional[List[str]], context_contents: Optional[List[str]],
-                    parent: Optional[str] = None, references: Optional[List[str]] = None):
+                    functions: Optional[List[dict]],
+                    parent: Optional[str] = None, references: Optional[List[str]] = None,
+                    function_name: Optional[str] = None):
         """
         Make a prompt for the chat API.
 
         Args:
             request (str): The user request.
             instruct_contents (Optional[List[str]]): A list of instructions to the prompt.
             context_contents (Optional[List[str]]): A list of context messages to the prompt.
             parent (Optional[str]): The parent prompt hash. None means a new topic.
             references (Optional[List[str]]): The reference prompt hashes.
         """
-        self._prompt = self._chat.init_prompt(request)
+        self._prompt = self._chat.init_prompt(request, function_name=function_name)
         self._check_limit()
         # Add instructions to the prompt
         if instruct_contents:
             combined_instruct = ''.join(instruct_contents)
             self._prompt.append_new(Message.INSTRUCT, combined_instruct)
             self._check_limit()
         # Add context to the prompt
         if context_contents:
             for context_content in context_contents:
                 self._prompt.append_new(Message.CONTEXT, context_content)
                 self._check_limit()
+        # Add functions to the prompt
+        if functions:
+            self._prompt.set_functions(functions)
+            self._check_limit()
 
         # Add history to the prompt
         for reference_hash in references:
             prompt = self._store.get_prompt(reference_hash)
             if not prompt:
                 logger.error("Reference %s not retrievable while making prompt.", reference_hash)
                 continue
             self._prompt.references.append(reference_hash)
-            self._append_prompt(prompt)
+            self._prompt.prepend_history(prompt, self.token_limit)
         if parent:
             self._prompt.parent = parent
             parent_hash = parent
             while parent_hash:
                 parent_prompt = self._store.get_prompt(parent_hash)
                 if not parent_prompt:
                     logger.error("Parent %s not retrievable while making prompt.", parent_hash)
                     break
-                if not self._append_prompt(parent_prompt):
+                if not self._prompt.prepend_history(parent_prompt, self.token_limit):
                     break
                 parent_hash = parent_prompt.parent
 
     def iterate_response(self) -> Iterator[str]:
         """Get an iterator of response strings from the chat API.
 
         Returns:
             Iterator[str]: An iterator over response strings from the chat API.
         """
         if self._chat.config.stream:
-            response_iterator = self._chat.stream_response(self._prompt)
-            for chunk in response_iterator:
-                yield self._prompt.append_response(str(chunk))
+            first_chunk = True
+            for chunk in self._chat.stream_response(self._prompt):
+                delta = self._prompt.append_response(str(chunk))
+                if first_chunk:
+                    first_chunk = False
+                    yield self._prompt.formatted_header()
+                yield delta
             self._store.store_prompt(self._prompt)
-            yield f'\n\nprompt {self._prompt.hash}\n'
-            for index in range(1, len(self._prompt.response)):
-                yield self._prompt.formatted_response(index) + '\n'
+            yield self._prompt.formatted_footer(0) + '\n'
+            for index in range(1, len(self._prompt.responses)):
+                yield self._prompt.formatted_full_response(index) + '\n'
         else:
-            response_str = str(self._chat.complete_response(self._prompt))
+            response_str = self._chat.complete_response(self._prompt)
             self._prompt.set_response(response_str)
             self._store.store_prompt(self._prompt)
-            for index in range(len(self._prompt.response)):
-                yield self._prompt.formatted_response(index) + '\n'
-
-    def _append_prompt(self, prompt: Prompt) -> bool:
-        # Append the first response and the request of the appended prompt
-        if not self._prompt.append_history(Message.CHAT, prompt.response[0],
-                                           self.available_tokens):
-            return False
-        if not self._prompt.append_history(Message.CHAT, prompt.request,
-                                           self.available_tokens):
-            return False
-
-        # Append the context messages of the appended prompt
-        for context_message in prompt.new_context:
-            if not self._prompt.append_history(Message.CONTEXT, context_message,
-                                               self.available_tokens):
-                return False
-        return True
+            for index in range(len(self._prompt.responses)):
+                yield self._prompt.formatted_full_response(index) + '\n'
```

### Comparing `devchat-0.1.9/devchat/chat.py` & `devchat-0.2.0/devchat/chat.py`

 * *Files 6% similar despite different names*

```diff
@@ -39,16 +39,16 @@
         Args:
             prompt (Prompt): A prompt of messages representing the conversation.
         Returns:
             str: A JSON string representing the complete response.
         """
 
     @abstractmethod
-    def stream_response(self, prompt: Prompt) -> Iterator[str]:
+    def stream_response(self, prompt: Prompt) -> Iterator:
         """
         Retrieve a streaming response as an iterator of JSON strings from the chat system.
 
         Args:
             prompt (Prompt): A prompt of messages representing the conversation.
         Returns:
-            Iterator[str]: An iterator over JSON strings representing the streaming response events.
+            Iterator: An iterator over JSON strings (to be converted to) representing the response.
         """
```

### Comparing `devchat-0.1.9/devchat/message.py` & `devchat-0.2.0/devchat/message.py`

 * *Files 7% similar despite different names*

```diff
@@ -7,20 +7,28 @@
     """
     The basic unit of information in a prompt.
     """
     content: str = ""
 
     INSTRUCT = "instruct"
     CONTEXT = "context"
+    FUNCTION = "function"
     CHAT = "chat"
 
     @abstractmethod
     def to_dict(self) -> dict:
         """
         Convert the message to a dictionary.
         """
 
+    @classmethod
+    @abstractmethod
+    def from_dict(cls, message_data: dict) -> 'Message':
+        """
+        Convert the message from a dictionary.
+        """
+
     @abstractmethod
     def stream_from_dict(self, message_data: dict) -> str:
         """
         Append to the message from a dictionary returned from a streaming chat API.
         """
```

### Comparing `devchat-0.1.9/devchat/openai/openai_chat.py` & `devchat-0.2.0/devchat/openai/openai_chat.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from typing import Optional, Union, List, Dict, Iterator
 from pydantic import BaseModel, Field, Extra
 import openai
 from devchat.chat import Chat
-from devchat.utils import get_git_user_info
+from devchat.utils import get_user_info, user_id
 from .openai_message import OpenAIMessage
 from .openai_prompt import OpenAIPrompt
 
 
 class OpenAIChatConfig(BaseModel):
     """
     Configuration object for the OpenAIChat class.
@@ -18,15 +18,15 @@
     stream: Optional[bool] = Field(None)
     stop: Optional[Union[str, List[str]]] = Field(None)
     max_tokens: Optional[int] = Field(None, ge=1)
     presence_penalty: Optional[float] = Field(None, ge=-2.0, le=2.0)
     frequency_penalty: Optional[float] = Field(None, ge=-2.0, le=2.0)
     logit_bias: Optional[Dict[int, float]] = Field(None)
     user: Optional[str] = Field(None)
-    request_timeout: Optional[int] = Field(12, ge=3)
+    request_timeout: Optional[int] = Field(32, ge=3)
 
     class Config:
         """
         Configuration class to forbid extra fields in the model.
         """
         extra = Extra.forbid
 
@@ -40,49 +40,57 @@
         Initialize the OpenAIChat class with a configuration object.
 
         Args:
             config (OpenAIChatConfig): Configuration object with parameters for the OpenAI Chat API.
         """
         self.config = config
 
-    def init_prompt(self, request: str) -> OpenAIPrompt:
-        user, email = get_git_user_info()
+    def init_prompt(self, request: str, function_name: Optional[str] = None) -> OpenAIPrompt:
+        user, email = get_user_info()
+        self.config.user = user_id(user, email)[1]
         prompt = OpenAIPrompt(self.config.model, user, email)
-        prompt.set_request(request)
+        prompt.set_request(request, function_name=function_name)
         return prompt
 
     def load_prompt(self, data: dict) -> OpenAIPrompt:
         data['_new_messages'] = {
-            k: [OpenAIMessage(**m) for m in v] if isinstance(v, list) else OpenAIMessage(**v)
-            for k, v in data['_new_messages'].items()
+            k: [OpenAIMessage.from_dict(m) for m in v]
+            if isinstance(v, list) else OpenAIMessage.from_dict(v)
+            for k, v in data['_new_messages'].items() if k != 'function'
         }
-        data['_history_messages'] = {k: [OpenAIMessage(**m) for m in v]
+        data['_history_messages'] = {k: [OpenAIMessage.from_dict(m) for m in v]
                                      for k, v in data['_history_messages'].items()}
         return OpenAIPrompt(**data)
 
     def complete_response(self, prompt: OpenAIPrompt) -> str:
         # Filter the config parameters with non-None values
         config_params = {
             key: value
             for key, value in self.config.dict().items() if value is not None
         }
+        if prompt.get_functions():
+            config_params['functions'] = prompt.get_functions()
+            config_params['function_call'] = 'auto'
         config_params['stream'] = False
 
         response = openai.ChatCompletion.create(
             messages=prompt.messages,
             **config_params
         )
-        return response
+        return str(response)
 
-    def stream_response(self, prompt: OpenAIPrompt) -> Iterator[str]:
+    def stream_response(self, prompt: OpenAIPrompt) -> Iterator:
         # Filter the config parameters with non-None values
         config_params = {
             key: value
             for key, value in self.config.dict().items() if value is not None
         }
+        if prompt.get_functions():
+            config_params['functions'] = prompt.get_functions()
+            config_params['function_call'] = 'auto'
         config_params['stream'] = True
 
         response = openai.ChatCompletion.create(
             messages=prompt.messages,
             **config_params
         )
         return response
```

### Comparing `devchat-0.1.9/devchat/openai/openai_prompt.py` & `devchat-0.2.0/devchat/openai/openai_prompt.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,16 +1,19 @@
 from dataclasses import dataclass
 import json
 import math
-from typing import List
+from typing import List, Optional
 from devchat.prompt import Prompt
 from devchat.message import Message
-from devchat.utils import update_dict, message_tokens
+from devchat.utils import update_dict, get_logger
+from devchat.utils import message_tokens, response_tokens
 from .openai_message import OpenAIMessage
 
+logger = get_logger(__name__)
+
 
 @dataclass
 class OpenAIPrompt(Prompt):
     """
     A class to represent a prompt and its corresponding responses from OpenAI APIs.
     """
 
@@ -26,56 +29,125 @@
         # Instruction
         if self._new_messages[Message.INSTRUCT]:
             combined += [msg.to_dict() for msg in self._new_messages[Message.INSTRUCT]]
         # History context
         if self._history_messages[Message.CONTEXT]:
             combined += [update_dict(msg.to_dict(), 'content',
                                      f"<context>\n{msg.content}\n</context>")
-                         for msg in self.new_context]
+                         for msg in self._history_messages[Message.CONTEXT]]
         # History chat
         if self._history_messages[Message.CHAT]:
-            combined += [msg.to_dict() for msg
-                         in reversed(self._history_messages[Message.CHAT])]
+            combined += [msg.to_dict() for msg in self._history_messages[Message.CHAT]]
         # Request
         if self.request:
             combined += [self.request.to_dict()]
         # New context
         if self.new_context:
             combined += [update_dict(msg.to_dict(), 'content',
                                      f"<context>\n{msg.content}\n</context>")
                          for msg in self.new_context]
         return combined
 
+    def input_messages(self, messages: List[dict]):
+        state = "new_instruct"
+        for message_data in messages:
+            message = OpenAIMessage.from_dict(message_data)
+
+            if state == "new_instruct":
+                if message.role == "system" and not message.content.startswith("<context>"):
+                    self._new_messages[Message.INSTRUCT].append(message)
+                else:
+                    state = "history_context"
+
+            if state == "history_context":
+                if message.role == "system" and message.content.startswith("<context>"):
+                    content = message.content.replace("<context>", "").replace("</context>", "")
+                    message.content = content.strip()
+                    self._history_messages[Message.CONTEXT].append(message)
+                else:
+                    state = "history_chat"
+
+            if state == "history_chat":
+                if message.role in ("user", "assistant"):
+                    self._history_messages[Message.CHAT].append(message)
+                else:
+                    state = "new_context"
+
+            if state == "new_context":
+                if message.role == "system" and message.content.startswith("<context>"):
+                    content = message.content.replace("<context>", "").replace("</context>", "")
+                    message.content = content.strip()
+                    self._new_messages[Message.CONTEXT].append(message)
+                else:
+                    logger.warning("Invalid new context message: %s", message)
+
+        if not self.request:
+            last_user_message = self._history_messages[Message.CHAT].pop()
+            if last_user_message.role == "user":
+                self._new_messages["request"] = last_user_message
+            else:
+                logger.warning("Invalid user request: %s", last_user_message)
+
     def append_new(self, message_type: str, content: str,
                    available_tokens: int = math.inf) -> bool:
         if message_type not in (Message.INSTRUCT, Message.CONTEXT):
             raise ValueError(f"Current messages cannot be of type {message_type}.")
-        message = OpenAIMessage(content, 'system')
+        # New instructions and context are of the system role
+        message = OpenAIMessage(content=content, role='system')
+
         num_tokens = message_tokens(message.to_dict(), self.model)
         if num_tokens > available_tokens:
             return False
+
         self._new_messages[message_type].append(message)
         self._request_tokens += num_tokens
         return True
 
-    def append_history(self, message_type: str, message: Message,
-                       available_tokens: int = math.inf) -> bool:
+    def set_functions(self, functions, available_tokens: int = math.inf):
+        num_tokens = message_tokens({"functions": json.dumps(functions)}, self.model)
+        if num_tokens > available_tokens:
+            return False
+
+        self._new_messages[Message.FUNCTION] = functions
+        self._request_tokens += num_tokens
+        return True
+
+    def get_functions(self):
+        return self._new_messages.get(Message.FUNCTION, None)
+
+    def _prepend_history(self, message_type: str, message: Message,
+                         token_limit: int = math.inf) -> bool:
         if message_type == Message.INSTRUCT:
             raise ValueError("History messages cannot be of type INSTRUCT.")
         num_tokens = message_tokens(message.to_dict(), self.model)
-        if num_tokens > available_tokens:
+        if num_tokens > token_limit - self._request_tokens:
             return False
-        self._history_messages[message_type].append(message)
+        self._history_messages[message_type].insert(0, message)
         self._request_tokens += num_tokens
         return True
 
-    def set_request(self, content: str) -> int:
+    def prepend_history(self, prompt: 'OpenAIPrompt', token_limit: int = math.inf) -> bool:
+        # Prepend the first response and the request of the prompt
+        if not self._prepend_history(Message.CHAT, prompt.responses[0], token_limit):
+            return False
+        if not self._prepend_history(Message.CHAT, prompt.request, token_limit):
+            return False
+
+        # Append the context messages of the appended prompt
+        for context_message in prompt.new_context:
+            if not self._prepend_history(Message.CONTEXT, context_message, token_limit):
+                return False
+        return True
+
+    def set_request(self, content: str, function_name: Optional[str] = None) -> int:
         if not content.strip():
             raise ValueError("The request cannot be empty.")
-        message = OpenAIMessage(content, 'user')
+        message = OpenAIMessage(content=content,
+                                role=('user' if not function_name else 'function'),
+                                name=function_name)
         self._new_messages['request'] = message
         self._request_tokens += message_tokens(message.to_dict(), self.model)
 
     def set_response(self, response_str: str):
         """
         Parse the API response string and set the Prompt object's attributes.
 
@@ -88,18 +160,20 @@
         self._id_from_dict(response_data)
 
         self._request_tokens = response_data['usage']['prompt_tokens']
         self._response_tokens = response_data['usage']['completion_tokens']
 
         for choice in response_data['choices']:
             index = choice['index']
-            if index >= len(self.response):
-                self.response.extend([None] * (index - len(self.response) + 1))
-            self.response[index] = OpenAIMessage(**choice['message'])
-        self.set_hash()
+            if index >= len(self.responses):
+                self.responses.extend([None] * (index - len(self.responses) + 1))
+                self._response_reasons.extend([None] * (index - len(self._response_reasons) + 1))
+            self.responses[index] = OpenAIMessage.from_dict(choice['message'])
+            if choice['finish_reason']:
+                self._response_reasons[index] = choice['finish_reason']
 
     def append_response(self, delta_str: str) -> str:
         """
         Append the content of a streaming response to the existing messages.
 
         Args:
             delta_str (str): The JSON-formatted delta string from the chat API.
@@ -112,31 +186,54 @@
         self._timestamp_from_dict(response_data)
         self._id_from_dict(response_data)
 
         delta_content = ''
         for choice in response_data['choices']:
             delta = choice['delta']
             index = choice['index']
+            finish_reason = choice['finish_reason']
 
-            if index >= len(self.response):
-                self.response.extend([None] * (index - len(self.response) + 1))
+            if index >= len(self.responses):
+                self.responses.extend([None] * (index - len(self.responses) + 1))
+                self._response_reasons.extend([None] * (index - len(self._response_reasons) + 1))
 
-            if not self.response[index]:
-                self.response[index] = OpenAIMessage(**delta)
+            if not self.responses[index]:
+                self.responses[index] = OpenAIMessage.from_dict(delta)
                 if index == 0:
-                    delta_content = self.formatted_header()
-                    delta_content += self.response[0].content
+                    delta_content = self.responses[0].content if self.responses[0].content else ''
             else:
                 if index == 0:
-                    delta_content = self.response[0].stream_from_dict(delta)
+                    delta_content = self.responses[0].stream_from_dict(delta)
                 else:
-                    self.response[index].stream_from_dict(delta)
+                    self.responses[index].stream_from_dict(delta)
+
+                if 'function_call' in delta:
+                    if 'name' in delta['function_call']:
+                        self.responses[index].function_call['name'] = \
+                            self.responses[index].function_call.get('name', '') + \
+                            delta['function_call']['name']
+                    if 'arguments' in delta['function_call']:
+                        self.responses[index].function_call['arguments'] = \
+                            self.responses[index].function_call.get('arguments', '') + \
+                            delta['function_call']['arguments']
 
+            if finish_reason:
+                self._response_reasons[index] = finish_reason
         return delta_content
 
+    def _count_response_tokens(self) -> int:
+        if self._response_tokens:
+            return self._response_tokens
+
+        total = 0
+        for response_message in self.responses:
+            total += response_tokens(response_message.to_dict(), self.model)
+        self._response_tokens = total
+        return total
+
     def _validate_model(self, response_data: dict):
         if not response_data['model'].startswith(self.model):
             raise ValueError(f"Model mismatch: expected '{self.model}', "
                              f"got '{response_data['model']}'")
 
     def _timestamp_from_dict(self, response_data: dict):
         if self._timestamp is None:
```

### Comparing `devchat-0.1.9/devchat/prompt.py` & `devchat-0.2.0/devchat/prompt.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,18 +1,17 @@
 from abc import ABC, abstractmethod
 from dataclasses import dataclass, field, asdict
 import hashlib
-import logging
 import math
 from typing import Dict, List
 from devchat.message import Message
-from devchat.utils import unix_to_local_datetime
+from devchat.utils import unix_to_local_datetime, get_logger, user_id
 
 
-logger = logging.getLogger(__name__)
+logger = get_logger(__name__)
 
 
 @dataclass
 class Prompt(ABC):
     """
     A class to represent a prompt and its corresponding responses from the chat API.
 
@@ -33,90 +32,122 @@
     model: str
     user_name: str
     user_email: str
     _new_messages: Dict = field(default_factory=lambda: {
         Message.INSTRUCT: [],
         'request': None,
         Message.CONTEXT: [],
-        'response': []
+        'responses': []
     })
     _history_messages: Dict[str, Message] = field(default_factory=lambda: {
         Message.CONTEXT: [],
         Message.CHAT: []
     })
     parent: str = None
     references: List[str] = field(default_factory=list)
     _timestamp: int = None
     _request_tokens: int = 0
     _response_tokens: int = 0
+    _response_reasons: List[str] = field(default_factory=list)
     _hash: str = None
 
+    def _check_complete(self) -> bool:
+        """
+        Check if the prompt is complete for hashing.
+
+        Returns:
+            bool: Whether the prompt is complete.
+        """
+        if not self.request or not self._request_tokens or not self.responses:
+            logger.warning("Incomplete prompt: request = %s (%d), response = %s",
+                           self.request, self._request_tokens, self.responses)
+            return False
+
+        if not self._response_tokens:
+            return False
+
+        return True
+
     @property
     def timestamp(self) -> int:
         return self._timestamp
 
     @property
-    @abstractmethod
-    def messages(self) -> List[dict]:
-        """
-        List of messages in the prompt to be sent to the chat API.
-        """
-
-    @property
     def new_context(self) -> List[Message]:
         return self._new_messages[Message.CONTEXT]
 
     @property
     def request(self) -> Message:
         return self._new_messages['request']
 
     @property
-    def response(self) -> List[Message]:
-        return self._new_messages['response']
+    def responses(self) -> List[Message]:
+        return self._new_messages['responses']
 
     @property
     def request_tokens(self) -> int:
         return self._request_tokens
 
     @property
     def response_tokens(self) -> int:
         return self._response_tokens
 
+    @abstractmethod
+    def _count_response_tokens(self) -> int:
+        """
+        Calculate the number of tokens used in the responses.
+        """
+
     @property
     def hash(self) -> str:
         return self._hash
 
+    @property
+    @abstractmethod
+    def messages(self) -> List[dict]:
+        """
+        List of messages in the prompt to be sent to the chat API.
+        """
+
+    @abstractmethod
+    def input_messages(self, messages: List[dict]):
+        """
+        Input the messages from the chat API to new and history messages.
+        The message list should be generated by the `messages` property.
+
+        Args:
+            messages (List[dict]): The messages from the chat API.
+        """
+
     @abstractmethod
     def append_new(self, message_type: str, content: str,
                    available_tokens: int = math.inf) -> bool:
         """
-        Append a new message provided by the user to the prompt.
+        Append a new message provided by the user to this prompt.
 
         Args:
             message_type (str): The type of the message.
             content (str): The content of the message.
             available_tokens (int): The number of tokens available for the message.
 
         Returns:
             bool: Whether the message is appended.
         """
 
     @abstractmethod
-    def append_history(self, message_type: str, message: Message,
-                       available_tokens: int = math.inf) -> bool:
+    def prepend_history(self, prompt: "Prompt", token_limit: int = math.inf) -> bool:
         """
-        Add to the history messages of the prompt.
+        Add the prompt to the beginning of the history messages.
 
         Args:
-            message_type (str): The type of the message.
-            message (Message): The message to add.
-            available_tokens (int): The number of tokens available for the message.
+            prompt(Prompt): The prompt to prepend.
+            token_limit (int): The max number of tokens for this prompt.
 
         Returns:
-            bool: Whether the message is appended.
+            bool: Whether the message is prepended.
         """
 
     @abstractmethod
     def set_request(self, content: str):
         """
         Set the request message for the prompt.
 
@@ -141,72 +172,104 @@
         Args:
             delta_str (str): The JSON-formatted delta string from the chat API.
 
         Returns:
             str: The delta content with index 0. None when the response is over.
         """
 
-    def set_hash(self) -> str:
+    def finalize_hash(self) -> str:
         """
         Calculate and set the hash of the prompt.
 
         Returns:
             str: The hash of the prompt. None if the prompt is incomplete.
         """
-        if not self.request or not self.response:
-            logger.error("Incomplete prompt for hashing: request = %s, response = %s",
-                         self.request, self.response)
-            return None
+        if not self._check_complete():
+            self._hash = None
+
+        if self._hash:
+            return self._hash
+
+        self._count_response_tokens()
+
         data = asdict(self)
-        assert data.pop('_hash') is None
+        data.pop('_hash')
         string = str(tuple(sorted(data.items())))
         self._hash = hashlib.sha256(string.encode('utf-8')).hexdigest()
         return self._hash
 
     def formatted_header(self) -> str:
         """Formatted string header of the prompt."""
-        formatted_str = f"User: {self.user_name} <{self.user_email}>\n"
+        formatted_str = f"User: {user_id(self.user_name, self.user_email)[0]}\n"
+
+        if not self._timestamp:
+            raise ValueError(f"Prompt lacks timestamp for formatting header: {self.request}")
 
         local_time = unix_to_local_datetime(self._timestamp)
         formatted_str += f"Date: {local_time.strftime('%a %b %d %H:%M:%S %Y %z')}\n\n"
 
         return formatted_str
 
-    def formatted_response(self, index: int) -> str:
+    def formatted_footer(self, index: int) -> str:
+        """Formatted string footer of the prompt."""
+        if not self.hash:
+            raise ValueError(f"Prompt lacks hash for formatting footer: {self.request}")
+
+        note = None
+        formatted_str = "\n\n"
+        reason = self._response_reasons[index]
+        if reason == 'length':
+            note = "Incomplete model output due to max_tokens parameter or token limit"
+        elif reason == 'function_call':
+            formatted_str += self.responses[index].function_call_to_json() + "\n\n"
+            note = "The model decided to call a function"
+        elif reason == 'content_filter':
+            note = "Omitted content due to a flag from our content filters"
+
+        if note:
+            formatted_str += f"Note: {note} (finish_reason: {reason})\n\n"
+
+        return formatted_str + f"prompt {self.hash}"
+
+    def formatted_full_response(self, index: int) -> str:
         """
-        Formatted response of the prompt.
+        Formatted full response of the prompt.
 
         Args:
             index (int): The index of the response to format.
 
         Returns:
-            str: The formatted response string. None if the response is incomplete.
+            str: The formatted response string. None if the response is invalid.
         """
-        formatted_str = self.formatted_header()
-
-        if index >= len(self.response) or not self.response[index]:
-            logger.error("Response index %d is incomplete to format: request = %s, response = %s",
-                         index, self.request, self.response)
+        if index >= len(self.responses) or not self.responses[index]:
+            logger.error("Response index %d is invalid to format: request = %s, response = %s",
+                         index, self.request, self.responses)
             return None
 
-        formatted_str += self.response[index].content.strip() + "\n\n"
-        formatted_str += f"prompt {self.hash}"
+        formatted_str = self.formatted_header()
+
+        if self.responses[index].content:
+            formatted_str += self.responses[index].content
 
-        return formatted_str
+        return formatted_str + self.formatted_footer(index)
 
     def shortlog(self) -> List[dict]:
         """Generate a shortlog of the prompt."""
-        if not self.request or not self.response:
+        if not self.request or not self.responses:
             raise ValueError("Prompt is incomplete for shortlog.")
-        logs = []
-        for message in self.response:
-            shortlog_data = {
-                "user": f"{self.user_name} <{self.user_email}>",
-                "date": self._timestamp,
-                "context": [msg.to_dict() for msg in self.new_context],
-                "request": self.request.content,
-                "response": message.content,
-                "hash": self.hash,
-                "parent": self.parent
-            }
-            logs.append(shortlog_data)
-        return logs
+
+        responses = []
+        for message in self.responses:
+            responses.append((message.content if message.content else "")
+                             + message.function_call_to_json())
+
+        return {
+            "user": user_id(self.user_name, self.user_email)[0],
+            "date": self._timestamp,
+            "context": [msg.to_dict() for msg in self.new_context],
+            "request": self.request.content,
+            "responses": responses,
+            "request_tokens": self._request_tokens,
+            "response_tokens": self._response_tokens,
+            "hash": self.hash,
+            "parent": self.parent
+        }
```

### Comparing `devchat-0.1.9/devchat/utils.py` & `devchat-0.2.0/devchat/utils.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,41 +1,66 @@
-"""
-utils.py - Utility functions for DevChat.
-"""
+import json
 import logging
 import os
 import re
 import getpass
 import socket
 import subprocess
-from typing import List, Tuple
+from typing import List, Tuple, Optional
 import datetime
-import pytz
-from dateutil import tz
+import hashlib
 import tiktoken
 
+log_formatter = logging.Formatter('%(asctime)s - %(name)s - %(levelname)s - %(message)s')
 
-def setup_logger(file_path, level=logging.WARNING):
-    """Utility function to set up a logger with the specified file path and level."""
-    formatter = logging.Formatter('%(asctime)s - %(name)s - %(levelname)s - %(message)s')
 
-    # Create a file handler for logging
-    file_handler = logging.FileHandler(file_path)
-    file_handler.setFormatter(formatter)
+def setup_logger(file_path: Optional[str] = None):
+    """Utility function to set up a global file log handler."""
+    if file_path is None:
+        handler = logging.StreamHandler()
+    else:
+        handler = logging.FileHandler(file_path)
+    handler.setFormatter(log_formatter)
+    logging.root.handlers = [handler]
+
+
+def get_logger(name: str = None, handler: logging.Handler = None) -> logging.Logger:
+    local_logger = logging.getLogger(name)
 
-    # Set up the global logger
-    logging.basicConfig(level=level, handlers=[file_handler])
+    # Default to 'INFO' if 'LOG_LEVEL' env is not set
+    log_level_str = os.getenv('LOG_LEVEL', 'INFO')
+    log_level = getattr(logging, log_level_str.upper(), logging.INFO)
+    local_logger.setLevel(log_level)
 
+    # If a handler is provided, configure and add it to the logger
+    if handler is not None:
+        handler.setLevel(log_level)
+        handler.setFormatter(log_formatter)
+        local_logger.addHandler(handler)
 
-def find_git_root():
+    local_logger.info("Get %s", str(local_logger))
+    return local_logger
+
+
+def find_root_dir() -> Optional[str]:
     try:
-        root = subprocess.check_output(["git", "rev-parse", "--show-toplevel"])
-        return root.decode("utf-8").strip()
-    except subprocess.CalledProcessError as error:
-        raise RuntimeError("Not inside a Git repository") from error
+        result = subprocess.run(["git", "rev-parse", "--show-toplevel"],
+                                capture_output=True, text=True, check=True, encoding='utf-8')
+        return result.stdout.strip()
+    except Exception:
+        try:
+            result = subprocess.run(["svn", "info"],
+                                    capture_output=True, text=True, check=True, encoding='utf-8')
+            if result.returncode == 0:
+                for line in result.stdout.splitlines():
+                    if line.startswith("Working Copy Root Path: "):
+                        return line.split("Working Copy Root Path: ", 1)[1].strip()
+        except Exception:
+            return os.path.expanduser("~")
+    return None
 
 
 def git_ignore(target_dir: str, *ignore_entries: str) -> None:
     gitignore_path = os.path.join(target_dir, '.gitignore')
 
     if os.path.exists(gitignore_path):
         with open(gitignore_path, 'r', encoding='utf-8') as gitignore_file:
@@ -55,40 +80,43 @@
         with open(gitignore_path, 'w', encoding='utf-8') as gitignore_file:
             gitignore_file.write('# devchat\n')
             for entry in ignore_entries:
                 gitignore_file.write(f'{entry}\n')
 
 
 def unix_to_local_datetime(unix_time) -> datetime.datetime:
-    # Get the local time zone
-    local_tz = tz.tzlocal()
-
-    # Convert the Unix time to a naive datetime object
-    naive_dt = datetime.datetime.utcfromtimestamp(unix_time)
+    # Convert the Unix time to a naive datetime object in UTC
+    naive_dt = datetime.datetime.utcfromtimestamp(unix_time).replace(tzinfo=datetime.timezone.utc)
 
-    # Localize the naive datetime object to the local time zone
-    local_dt = naive_dt.replace(tzinfo=pytz.utc).astimezone(local_tz)
+    # Convert the UTC datetime object to the local timezone
+    local_dt = naive_dt.astimezone()
 
     return local_dt
 
 
-def get_git_user_info() -> Tuple[str, str]:
+def get_user_info() -> Tuple[str, str]:
     try:
         cmd = ['git', 'config', 'user.name']
-        git_user_name = subprocess.check_output(cmd).decode('utf-8').strip()
-    except subprocess.CalledProcessError:
-        git_user_name = getpass.getuser()
+        user_name = subprocess.check_output(cmd, encoding='utf-8').strip()
+    except Exception:
+        user_name = getpass.getuser()
 
     try:
         cmd = ['git', 'config', 'user.email']
-        git_user_email = subprocess.check_output(cmd).decode('utf-8').strip()
-    except subprocess.CalledProcessError:
-        git_user_email = git_user_name + '@' + socket.gethostname()
+        user_email = subprocess.check_output(cmd, encoding='utf-8').strip()
+    except Exception:
+        user_email = user_name + '@' + socket.gethostname()
 
-    return git_user_name, git_user_email
+    return user_name, user_email
+
+
+def user_id(user_name, user_email) -> Tuple[str, str]:
+    user_str = f"{user_name} <{user_email}>"
+    user_hash = hashlib.sha1(user_str.encode('utf-8')).hexdigest()
+    return user_str, user_hash
 
 
 def parse_files(file_paths: List[str]) -> List[str]:
     if not file_paths:
         return []
 
     for file_path in file_paths:
@@ -104,20 +132,43 @@
                 raise ValueError(f"File {file_path} is empty.")
             contents.append(content)
     return contents
 
 
 def valid_hash(hash_str):
     """Check if a string is a valid hash value."""
-    # Hash values are usually alphanumeric with a fixed length
-    # depending on the algorithm used to generate them
-    pattern = re.compile(r'^[a-f0-9]{64}$')  # Example pattern for SHA-256 hash
+    pattern = re.compile(r'^[a-f0-9]{64}$')  # for SHA-256 hash
     return bool(pattern.match(hash_str))
 
 
+def check_format(formatted_response) -> bool:
+    pattern = r"(User: .+ <.+@.+>\nDate: .+\n\n(?:.*\n)*\n(?:prompt [a-f0-9]{64}\n\n?)+)"
+    return bool(re.fullmatch(pattern, formatted_response))
+
+
+def get_content(formatted_response) -> str:
+    header_pattern = r"User: .+ <.+@.+>\nDate: .+\n\n"
+    footer_pattern = r"\n(?:prompt [a-f0-9]{64}\n\n?)+"
+
+    content = re.sub(header_pattern, "", formatted_response)
+    content = re.sub(footer_pattern, "", content)
+
+    return content
+
+
+def get_prompt_hash(formatted_response) -> str:
+    if not check_format(formatted_response):
+        raise ValueError("Invalid formatted response.")
+    footer_pattern = r"\n(?:prompt [a-f0-9]{64}\n\n?)+"
+    # get the last prompt hash
+    prompt_hash = re.findall(footer_pattern, formatted_response)[-1].strip()
+    prompt_hash = prompt_hash.replace("prompt ", "")
+    return prompt_hash
+
+
 def update_dict(dict_to_update, key, value) -> dict:
     """
     Update a dictionary with a key-value pair and return the dictionary.
     """
     dict_to_update[key] = value
     return dict_to_update
 
@@ -126,29 +177,26 @@
     """Returns the number of tokens used by a message."""
     try:
         encoding = tiktoken.encoding_for_model(model)
     except KeyError as err:
         raise ValueError(f"Invalid model {model} for tiktoken.") from err
 
     num_tokens = 0
-    if model.startswith("gpt-3.5"):
+    if model == "gpt-3.5-turbo-0301":
         num_tokens += 4  # every message follows <|start|>{role/name}\n{content}<|end|>\n
         tokens_per_name = -1  # if there's a name, the role is omitted
-    elif model.startswith("gpt-4"):
+    else:
         num_tokens += 3
         tokens_per_name = 1
 
     for key, value in message.items():
+        if key == 'function_call':
+            value = json.dumps(value)
         num_tokens += len(encoding.encode(value))
         if key == "name":
             num_tokens += tokens_per_name
     return num_tokens
 
 
-def response_tokens(response: str, model: str) -> int:
+def response_tokens(message: dict, model: str) -> int:
     """Returns the number of tokens used by a response."""
-    try:
-        encoding = tiktoken.encoding_for_model(model)
-    except KeyError as err:
-        raise ValueError(f"Invalid model {model} for tiktoken.") from err
-
-    return len(encoding.encode(response)) + 3  # +3 for <|start|>assistant<|message|>
+    return message_tokens(message, model)
```

### Comparing `devchat-0.1.9/devchat.egg-info/PKG-INFO` & `devchat-0.2.0/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,41 +1,60 @@
 Metadata-Version: 2.1
 Name: devchat
-Version: 0.1.9
+Version: 0.2.0
 Summary: DevChat is an open-source tool that helps developers write prompts to generate code and documentation.
-Home-page: https://github.com/covespace/devchat
-License: Apache License 2.0
+Home-page: https://github.com/devchat-ai/devchat
+License: Apache-2.0
+Author: DevChat Team
+Author-email: hello@devchat.ai
+Requires-Python: >=3.8,<4.0
 Classifier: Development Status :: 4 - Beta
+Classifier: Intended Audience :: Developers
+Classifier: Intended Audience :: Education
+Classifier: Intended Audience :: Information Technology
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
+Classifier: Topic :: Software Development
+Requires-Dist: importlib-metadata (>=6.8.0,<7.0.0)
+Requires-Dist: networkx (>=3.1,<4.0)
+Requires-Dist: openai (>=0.27.8,<0.28.0)
+Requires-Dist: pydantic (>=1.10.7,<2.0.0)
+Requires-Dist: rich_click (>=1.6.1,<2.0.0)
+Requires-Dist: tiktoken (>=0.4.0,<0.5.0)
+Requires-Dist: tinydb (>=4.7.1,<5.0.0)
+Requires-Dist: urllib3 (<2.0)
 Description-Content-Type: text/markdown
-License-File: LICENSE
 
 <div align="center">
 
-![devchat](https://github.com/covespace/devchat/assets/592493/f39979fe-fe32-410b-bf9d-2118ac8ea3d5)
+![devchat](https://github.com/devchat-ai/devchat/assets/592493/f39979fe-fe32-410b-bf9d-2118ac8ea3d5)
 
 # DevChat
 
 <br>
 
 [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
-[![CircleCI](https://circleci.com/gh/covespace/devchat/tree/main.svg?style=shield)](https://circleci.com/gh/covespace/devchat/tree/main)
-[![GitHub license](https://img.shields.io/github/license/covespace/devchat.svg)](https://github.com/covespace/devchat/blob/main/LICENSE)
+[![CircleCI](https://circleci.com/gh/devchat-ai/devchat/tree/main.svg?style=shield)](https://circleci.com/gh/devchat-ai/devchat/tree/main)
+[![GitHub license](https://img.shields.io/github/license/devchat-ai/devchat.svg)](https://github.com/devchat-ai/devchat/blob/main/LICENSE)
 [![Downloads](https://pepy.tech/badge/devchat)](https://pepy.tech/project/devchat)
 [![PyPI version](https://badge.fury.io/py/devchat.svg)](https://badge.fury.io/py/devchat)
 [![Discord Chat](https://img.shields.io/discord/1106908489114206309?logo=discord)](https://discord.gg/9t3yrbBUXD)
 
 </div>
 <br>
 <div align="left">
 
 The DevChat core library and CLI.
 
-👉 For an enhanced experience and UI, we welcome you to install [Visual Studio Code extension](https://github.com/covespace/devchat-vscode) from [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=merico.devchat)! Enjoy DevChat! 👏
+👉 **For an enhanced experience and UI, we welcome you to install [Visual Studio Code extension](https://github.com/devchat-ai/devchat-vscode) from [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=merico.devchat)! Enjoy DevChat VSCode!** 👏
 
 ***
 
 ## What is DevChat?
 
 DevChat is the open-source solution to help you write prompts to generate code and documentation, going beyond simple code auto-completion.
 It isn't limited to performing predefined operations on short code snippets.
@@ -46,80 +65,79 @@
 
 ## Why DevChat?
 
 - Great output requires great input, to maximize the power of AI, DevChat assists you seamlessly to **provide the right context** to the AI.
     
   Chat history, code, files, directory trees, `git diff --cached`, or the output of any command.
   
-  ![20230523-220717-cut-merged-1684855581224](https://github.com/covespace/devchat-vscode/assets/592493/16bc09e4-4185-4bcb-8d5a-2173b0bfc3ed)
+  ![20230523-220717-cut-merged-1684855581224](https://github.com/devchat-ai/devchat-vscode/assets/592493/16bc09e4-4185-4bcb-8d5a-2173b0bfc3ed)
 
-  ![20230523-220717-00 00 28 206-00 00 44 950](https://github.com/covespace/devchat-vscode/assets/592493/d5556310-bc7f-4abb-86a3-8e76e4aa720e)  
+  ![20230523-220717-00 00 28 206-00 00 44 950](https://github.com/devchat-ai/devchat-vscode/assets/592493/d5556310-bc7f-4abb-86a3-8e76e4aa720e)  
 
 - Once you have generated code with AI, DevChat **streamlines the actions** to properly integrate and ship.
   
   View diffs, copy or insert, commit & sync, or export to documentation, wikis, and more.
   
-  ![20230523-220717-00 00 46 728-00 01 00 120](https://github.com/covespace/devchat-vscode/assets/592493/a2bab011-8e31-47a9-838f-36e43cd2e98c)
+  ![20230523-220717-00 00 46 728-00 01 00 120](https://github.com/devchat-ai/devchat-vscode/assets/592493/a2bab011-8e31-47a9-838f-36e43cd2e98c)
 
-  ![20230523-220717-00 01 00 120-00 01 14 452](https://github.com/covespace/devchat-vscode/assets/592493/31e90fd5-e797-4726-b5b2-5c4dce1c7551)
+  ![20230523-220717-00 01 00 120-00 01 14 452](https://github.com/devchat-ai/devchat-vscode/assets/592493/31e90fd5-e797-4726-b5b2-5c4dce1c7551)
 
 - To guide AI in your work, define **your own workflows** with DevChat.
   
-  ![20230523-220717-00 01 14 614-00 01 41 680](https://github.com/covespace/devchat-vscode/assets/592493/94502efd-781b-448d-b945-dffcc41d7af3)
+  ![20230523-220717-00 01 14 614-00 01 41 680](https://github.com/devchat-ai/devchat-vscode/assets/592493/94502efd-781b-448d-b945-dffcc41d7af3)
 
   Explore more prompt templates, iterative calls to AI, and program operations.
   
 - To ensure the experience fits your preferences, customize **your own experiences** with DevChat.
   
   Open-source, no waiting for opaque feature schedules. Access GPT-4 today and more models in the future.
   
 ## What is Prompt-Centric Software Development (PCSD)?
 
 - The traditional code-centric paradigm is evolving.
 
 - Write prompts to create code. Transform prompts into all the artifacts in software engineering.
 
-  <img width="600" alt="image" src="https://github.com/covespace/devchat/assets/592493/dd32e900-92fd-4fa4-8489-96ed17ab5e0e">
+  <img width="600" alt="image" src="https://github.com/devchat-ai/devchat/assets/592493/dd32e900-92fd-4fa4-8489-96ed17ab5e0e">
 
   <sub>(This image is licensed by devchat.ai under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.)</sub>
   
 - We like to call it DevPromptOps
   
-  <img width="500" alt="image" src="https://github.com/covespace/devchat/assets/592493/e8e1215b-53b0-4473-ab00-0665d33f204a">
+  <img width="500" alt="image" src="https://github.com/devchat-ai/devchat/assets/592493/e8e1215b-53b0-4473-ab00-0665d33f204a">
   
   <sub>(This image is licensed by devchat.ai under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.)</sub>
 
 ***
 
 ## Quick Start
 
-For UI, install the [Visual Studio Code extension](https://github.com/covespace/devchat-vscode) from [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=merico.devchat).
+**For UI, install our [Visual Studio Code extension](https://github.com/devchat-ai/devchat-vscode) from [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=merico.devchat).**
 
 For CLI:
 - Install DevChat by running: `pip install devchat`.
-- Make sure you are working in a Git repository, as DevChat only works within one.
-- Set your [OpenAI API Key](https://platform.openai.com/account/api-keys) by running `export OPENAI_API_KEY="[sk-...]"`.
+- Make sure you are working in a Git or SVN repository, as DevChat only works within one.
+- Set your [OpenAI API Key](https://platform.openai.com/account/api-keys) by running `export OPENAI_API_KEY="[sk-...]"` (or DevChat access key).
 - To access help, use the commands: `devchat --help` and `devchat prompt --help`.
 
 ## Community
 
 - Join our [Discord](https://discord.gg/9t3yrbBUXD)!
-
-- Participate in [discussions](https://github.com/covespace/devchat/discussions)!
+- Participate in [discussions](https://github.com/devchat-ai/devchat/discussions)!
 
 ## Contributing
 
-Issues and pull request are welcome: https://github.com/covespace/devchat/issues
+Issues and pull request are welcome: https://github.com/devchat-ai/devchat/issues
   
 ## Roadmap
 
 - [x] Implement code diff application.
 - [ ] Improve code diff application using code change instructions.
 - [ ] Develop a framework for defining workflows.
-- [ ] Implement topic management.
+- [x] Implement topic management.
 - [ ] Enable interaction with external development tools.
 - [ ] Introduce more selective workflows.
   
 ## Contact
   
 hello@merico.dev
```

