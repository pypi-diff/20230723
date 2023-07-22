# Comparing `tmp/llmflows-0.0.7.tar.gz` & `tmp/llmflows-0.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "llmflows-0.0.7.tar", last modified: Sun Jul 16 16:29:28 2023, max compression
+gzip compressed data, was "llmflows-0.0.8.tar", last modified: Sat Jul 22 23:42:06 2023, max compression
```

## Comparing `llmflows-0.0.7.tar` & `llmflows-0.0.8.tar`

### file list

```diff
@@ -1,50 +1,50 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 16:29:28.838099 llmflows-0.0.7/
--rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-07-16 16:29:16.000000 llmflows-0.0.7/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     9412 2023-07-16 16:29:28.838099 llmflows-0.0.7/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8910 2023-07-16 16:29:16.000000 llmflows-0.0.7/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 16:29:28.834099 llmflows-0.0.7/llmflows/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 16:29:28.834099 llmflows-0.0.7/llmflows/callbacks/
--rw-r--r--   0 runner    (1001) docker     (123)      249 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/callbacks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1659 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/callbacks/async_base_callback.py
--rw-r--r--   0 runner    (1001) docker     (123)     2219 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/callbacks/async_functional_callback.py
--rw-r--r--   0 runner    (1001) docker     (123)     1625 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/callbacks/base_callback.py
--rw-r--r--   0 runner    (1001) docker     (123)     2014 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/callbacks/functional_callback.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 16:29:28.838099 llmflows-0.0.7/llmflows/flows/
--rw-r--r--   0 runner    (1001) docker     (123)      370 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3782 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/async_base_flow.py
--rw-r--r--   0 runner    (1001) docker     (123)     4998 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/async_base_flowstep.py
--rw-r--r--   0 runner    (1001) docker     (123)     3975 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/async_chat_flowstep.py
--rw-r--r--   0 runner    (1001) docker     (123)     2656 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/async_flow.py
--rw-r--r--   0 runner    (1001) docker     (123)     2178 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/async_flowstep.py
--rw-r--r--   0 runner    (1001) docker     (123)     4021 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/base_flow.py
--rw-r--r--   0 runner    (1001) docker     (123)     5504 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/base_flowstep.py
--rw-r--r--   0 runner    (1001) docker     (123)     3770 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/chat_flowstep.py
--rw-r--r--   0 runner    (1001) docker     (123)     2665 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/flow.py
--rw-r--r--   0 runner    (1001) docker     (123)     1951 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/flowstep.py
--rw-r--r--   0 runner    (1001) docker     (123)     2361 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/functional_flowstep.py
--rw-r--r--   0 runner    (1001) docker     (123)     3630 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/flows/vectorstore_flowstep.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 16:29:28.838099 llmflows-0.0.7/llmflows/llms/
--rw-r--r--   0 runner    (1001) docker     (123)      198 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/llms/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      718 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/llms/llm.py
--rw-r--r--   0 runner    (1001) docker     (123)     4263 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/llms/llm_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     6033 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/llms/message_history.py
--rw-r--r--   0 runner    (1001) docker     (123)     4078 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/llms/openai.py
--rw-r--r--   0 runner    (1001) docker     (123)     5066 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/llms/openai_chat.py
--rw-r--r--   0 runner    (1001) docker     (123)     3663 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/llms/openai_embeddings.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 16:29:28.838099 llmflows-0.0.7/llmflows/prompts/
--rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/prompts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1359 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/prompts/prompt_template.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 16:29:28.838099 llmflows-0.0.7/llmflows/vectorstores/
--rw-r--r--   0 runner    (1001) docker     (123)      108 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/vectorstores/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3229 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/vectorstores/pinecone.py
--rw-r--r--   0 runner    (1001) docker     (123)     2438 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/vectorstores/vector_doc.py
--rw-r--r--   0 runner    (1001) docker     (123)     1586 2023-07-16 16:29:16.000000 llmflows-0.0.7/llmflows/vectorstores/vector_store.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 16:29:28.834099 llmflows-0.0.7/llmflows.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     9412 2023-07-16 16:29:28.000000 llmflows-0.0.7/llmflows.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1231 2023-07-16 16:29:28.000000 llmflows-0.0.7/llmflows.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-16 16:29:28.000000 llmflows-0.0.7/llmflows.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       79 2023-07-16 16:29:28.000000 llmflows-0.0.7/llmflows.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-16 16:29:28.000000 llmflows-0.0.7/llmflows.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      705 2023-07-16 16:29:16.000000 llmflows-0.0.7/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-16 16:29:28.838099 llmflows-0.0.7/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:42:06.741030 llmflows-0.0.8/
+-rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-07-22 23:41:55.000000 llmflows-0.0.8/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    10082 2023-07-22 23:42:06.741030 llmflows-0.0.8/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9580 2023-07-22 23:41:55.000000 llmflows-0.0.8/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:42:06.733029 llmflows-0.0.8/llmflows/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:42:06.737029 llmflows-0.0.8/llmflows/callbacks/
+-rw-r--r--   0 runner    (1001) docker     (123)      249 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/callbacks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1659 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/callbacks/async_base_callback.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2219 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/callbacks/async_functional_callback.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1625 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/callbacks/base_callback.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2014 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/callbacks/functional_callback.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:42:06.737029 llmflows-0.0.8/llmflows/flows/
+-rw-r--r--   0 runner    (1001) docker     (123)      370 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3782 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/async_base_flow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4998 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/async_base_flowstep.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3975 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/async_chat_flowstep.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2656 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/async_flow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2178 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/async_flowstep.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3932 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/base_flow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5504 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/base_flowstep.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3770 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/chat_flowstep.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2665 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/flow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1951 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/flowstep.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2361 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/functional_flowstep.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3630 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/flows/vectorstore_flowstep.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:42:06.737029 llmflows-0.0.8/llmflows/llms/
+-rw-r--r--   0 runner    (1001) docker     (123)      198 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/llms/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      718 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/llms/llm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4263 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/llms/llm_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6033 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/llms/message_history.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4078 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/llms/openai.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5066 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/llms/openai_chat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3663 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/llms/openai_embeddings.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:42:06.737029 llmflows-0.0.8/llmflows/prompts/
+-rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/prompts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1359 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/prompts/prompt_template.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:42:06.737029 llmflows-0.0.8/llmflows/vectorstores/
+-rw-r--r--   0 runner    (1001) docker     (123)      108 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/vectorstores/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3229 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/vectorstores/pinecone.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2438 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/vectorstores/vector_doc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1586 2023-07-22 23:41:55.000000 llmflows-0.0.8/llmflows/vectorstores/vector_store.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:42:06.733029 llmflows-0.0.8/llmflows.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    10082 2023-07-22 23:42:06.000000 llmflows-0.0.8/llmflows.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1231 2023-07-22 23:42:06.000000 llmflows-0.0.8/llmflows.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 23:42:06.000000 llmflows-0.0.8/llmflows.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       79 2023-07-22 23:42:06.000000 llmflows-0.0.8/llmflows.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-22 23:42:06.000000 llmflows-0.0.8/llmflows.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      705 2023-07-22 23:41:55.000000 llmflows-0.0.8/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 23:42:06.741030 llmflows-0.0.8/setup.cfg
```

### Comparing `llmflows-0.0.7/LICENSE` & `llmflows-0.0.8/LICENSE`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/PKG-INFO` & `llmflows-0.0.8/README.md`

 * *Files 20% similar despite different names*

```diff
@@ -1,21 +1,7 @@
-Metadata-Version: 2.1
-Name: llmflows
-Version: 0.0.7
-Summary: LLMFlows - Simple, Explicit and Transparent LLM Apps
-Author: Stoyan Stoyanov
-Project-URL: Homepage, https://github.com/stoyan-stoyanov/llmflows
-Project-URL: github, https://github.com/stoyan-stoyanov/llmflows
-Classifier: Programming Language :: Python :: 3
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Operating System :: OS Independent
-Requires-Python: >=3.9
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
 # LLMFlows - Simple, Explicit, and Transparent LLM Apps
 
 <p align="center">
   <img style="width: 80%" src="docs/llmflows_last_logo.png" />
 </p>
 
 [![Twitter](https://img.shields.io/twitter/follow/LLMFlows?style=social)](https://twitter.com/LLMFlows)
@@ -27,140 +13,218 @@
 
 Documentation: [https://readthedocs.org](https://readthedocs.org/)<br/>
 PyPI: [https://pypi.org/project/llmflows](https://pypi.org/project/llmflows/)</br>
 Twitter: [https://twitter.com/LLMFlows](https://twitter.com/LLMFlows)<br/>
 Substack: [https://llmflows.substack.com](https://llmflows.substack.com/)<br/>
 
 ## About
-LLMFlows is a framework for building simple, explicit, and transparent LLM applications.
+LLMFlows is a framework for building simple, explicit, and transparent LLM(Large 
+Language Model) applications.
 
 ## Installation
 ```
 pip install llmflows
 ```
 
 ## Philosophy
 
 ### **Simple**
 Our goal is to build a simple, well-documented framework with minimal abstractions that 
 allow users to build flexible LLM-powered apps without compromising on capabilities.
 
 ### **Explicit**
 We want to create an explicit API enabling users to write clean and readable code while 
-easily creating complex flows of LLMs interacting with each other.
+easily creating complex flows of LLMs interacting with each other. LLMFlows' classes 
+give users full control and do not have any hidden prompts or LLM calls. 
 
 ### **Transparent**
 We aim to help users have full transparency on their LLM-powered apps by providing 
 traceable flows and complete information for each app component, making it easy to 
 monitor, maintain, and debug.
 
+## Getting Started
+### LLMs
+LLMs are one of the main abstractions in LLMFlows. LLM classes are wrappers around LLM 
+APIs such as OpenAI's APIs. They provide methods for configuring and calling these APIs, 
+retrying failed calls, and formatting the responses.
+
+```python
+from llmflows.llms import OpenAI
 
-## Usage
-You can quickly build a simple application with LLMFlows' `LLM` and `PrompTemplate` 
-classes:
+llm = OpenAI(api_key="<your-openai-api-key>")
+
+result, call_data, model_config = llm.generate(
+   prompt="Generate a cool title for an 80s rock song"
+)
+```
+
+
+### PromptTemplates
+The `PromptTemplate` class allows us to create strings with variables that we can fill 
+in dynamically later on. Once a prompt template object is created an actual prompt can 
+be generated by providing the required variables.
 
 ```python
+from llmflows.llms import OpenAI
+from llmflows.prompts import PromptTemplate
 
-from llmflows.llms.openai import OpenAI
-from llmflows.prompts.prompt_template import PromptTemplate
 
 prompt_template = PromptTemplate(
-   prompt="Generate a title for a 90s hip-hop song about {topic}."
+    prompt="Generate a title for a 90s hip-hop song about {topic}."
 )
 llm_prompt = prompt_template.get_prompt(topic="friendship")
 
-llm = OpenAI()
+print(llm_prompt)
+
+llm = OpenAI(api_key="<your-openai-api-key>")
 song_title = llm.generate(llm_prompt)
 
+print(song_title)
 ```
 
-You can also create a simple chat application with a few lines of code:
-```python
-from llmflows.llms import OpenAIChat
+### Chat LLMs
+Unlike regular LLMs that only require a prompt to generate text, chat LLMs require a 
+conversation history. The conversation history is represented 
+as a list of messages between a user and an assistant. This conversation history is 
+sent to the model, and a new message is generated based on it.
 
+LLMFlows provides a `MessageHistory` class to manage the required conversation history 
+for chat LLMs.
 
-llm = OpenAIChat(system_prompt="You are a useful assistant")
+You can build a simple chatbot by using the `OpenAIChat` and `MessageHistory` classes:
+
+```python
+from llmflows.llms import OpenAIChat, MessageHistory
+
+llm = OpenAIChat(api_key="<your-openai-api-key>")
+message_history = MessageHistory()
 
 while True:
     user_message = input("You:")
-    llm.add_message(user_message)
-    llm_response, call_data, model_config = llm.generate()
+    message_history.add_user_message(user_message)
+
+    llm_response, call_data, model_config = llm.generate(message_history)
+    message_history.add_ai_message(llm_response)
+
     print(f"LLM: {llm_response}")
 ```
 
-However, real-world applications are often more complex and have dependencies between 
-prompts and LLM calls. For example:
+### LLM Flows
+Often times, real-world applications can be more complex and can have dependencies 
+between prompts and LLM calls. For example:
 
 ![Complex flow](docs/complex_flow.png)
 
-You can build such flow using the `Flow` and `Flowstep` classes. LLMFlows will figure 
-out the dependencies and make sure each flowstep runs only when all its dependencies 
-are met:
+When you want to build apps with complex dependencies you can use the `Flow` and 
+`Flowstep` classes. LLMFlows will figure out the dependencies and make sure each 
+flowstep runs only when all its dependencies are met:
 
 ```python
 from llmflows.flows import Flow, FlowStep
 from llmflows.llms import OpenAI
 from llmflows.prompts import PromptTemplate
 
+openai_llm = OpenAI(api_key="<your-openai-api-key>")
+
 # Create prompt templates
 title_template = PromptTemplate("What is a good title of a movie about {topic}?")
 song_template = PromptTemplate(
     "What is a good song title of a soundtrack for a movie called {movie_title}?"
 )
 characters_template = PromptTemplate(
     "What are two main characters for a movie called {movie_title}?"
 )
 lyrics_template = PromptTemplate(
     "Write lyrics of a movie song called {song_title}. The main characters are "
     "{main_characters}"
 )
 
 # Create flowsteps
-flowstep1 = FlowStep(
+movie_title_flowstep = FlowStep(
+    name="Movie Title Flowstep",
+    llm=openai_llm,
+    prompt_template=title_template,
+    output_key="movie_title",
+)
+
+song_title_flowstep = FlowStep(
+    name="Song Title Flowstep",
+    llm=openai_llm,
+    prompt_template=song_template,
+    output_key="song_title",
+)
+
+characters_flowstep = FlowStep(
+    name="Characters Flowstep",
+    llm=openai_llm,
+    prompt_template=characters_template,
+    output_key="main_characters",
+)
+
+song_lyrics_flowstep = FlowStep(
+    name="Song Lyrics Flowstep",
+    llm=openai_llm,
+    prompt_template=lyrics_template,
+    output_key="song_lyrics",
+)
+
+# Connect flowsteps
+movie_title_flowstep.connect(song_title_flowstep, characters_flowstep, song_lyrics_flowstep)
+song_title_flowstep.connect(song_lyrics_flowstep)
+characters_flowstep.connect(song_lyrics_flowstep)
+
+# Create and run Flow
+soundtrack_flow = Flow(title_flowstep)
+results = soundtrack_flow.start(topic="friendship", verbose=True)
+```
+
+### Async Flows
+Sometimes multiple flow steps can run in parallel if all their dependencies are met. 
+For cases like this, LLMFlows provides async classes to improve the runtime of any 
+complex flow by running flow steps that already have all their required inputs in 
+parallel.
+
+```python
+
+...
+
+movie_title_flowstep = AsyncFlowStep(
     name="Flowstep 1",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=title_template,
     output_key="movie_title",
 )
 
-flowstep2 = FlowStep(
+song_title_flowstep = FlowStep(
     name="Flowstep 2",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=song_template,
     output_key="song_title",
 )
 
-flowstep3 = FlowStep(
+characters_flowstep = AsyncFlowStep(
     name="Flowstep 3",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=characters_template,
     output_key="main_characters",
 )
 
-flowstep4 = FlowStep(
+song_lyrics_flowstep = AsyncFlowStep(
     name="Flowstep 4",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=lyrics_template,
     output_key="song_lyrics",
 )
 
-# Connect flowsteps
-flowstep1.connect(flowstep2, flowstep3, flowstep4)
-flowstep2.connect(flowstep4)
-flowstep3.connect(flowstep4)
+...
 
-# Create and run Flow
-soundtrack_flow = Flow(flowstep1)
-results = soundtrack_flow.start(topic="friendship", verbose=True)
 ```
 
-In addition, LLMFlows provides async classes to improve the runtime of any complex flow 
-by running flow steps that already have all their required inputs in parallel.
-Check our documentation for more examples, such as creating question-answering apps and 
-web applications with Flask and FastAPI.
+Check our documentation for more examples, such as integrating vector databases, 
+creating question-answering apps and web applications with Flask and FastAPI.
 
 ## Features
 
 ### **LLMs**
 - Utilize LLMs such as OpenAI's ChatGPT to generate natural language text.
 - Configure LLM classes easily, choosing specific models, parameters, and settings.
 - Benefit from automatic retries when model calls fail, ensuring reliable LLM 
@@ -187,61 +251,29 @@
 - Leverage vector databases for seamless storage and querying of vectors, enabling straightforward integration with LLM-powered applications.
 
 ### **Callbacks**
 - Execute callback functions at different stages within flow steps, enabling enhanced customization, logging, tracing, or other specific integrations.
 - Utilize callbacks to comprehensively control and monitor LLM-powered apps, ensuring 
   clear visibility into the execution process.
 
-### **Complete Transparency**
-After executing a Flow you can answer questions such as:
+### **Explicit API and Full Transparency**
+With LLMFlows you have the full control to create explicit applications without any hidden prompts or predefined behaviors.
+
+In addition LLMFlows allows you to answer questions such as:
 
 - When was a particular flowstep run?
 - How much time did it take?
 - What were the input variables?
 - What was the prompt template?
 - What did the prompt look like?
 - What was the exact configuration of the model?
 - How many times did we retry the request?
 - What was the raw data the API returned?
 - How many tokens were used?
 - What was the final result?
 
-## FAQ
-
-### **How is this different than langchain?**
-Langchain is a great library, and LLMFlows has undoubtedly been inspired by it. 
-However, our philosophy is a bit different. Langchian has a "chain for everything" 
-philosophy and provides many classes with multiple LLM calls, logic, and built-in 
-default prompts. While this is great for beginners and default use cases, we feel this 
-can be overwhelming if users want to do anything "out of the ordinary." In contrast, 
-we are focusing on providing as few building blocks as possible and having an 
-easy-to-understand API while matching (and in some cases exceeding) the capabilities 
-of langchain.
-
-### **You only have OpenAI wrappers, but I want to use AcmeLLM.**
-We decided to release the library initially supporting only OpenAI LLMs, but we have a 
-roadmap and will slowly add new wrappers around the most popular models. If you are 
-willing to spend some time, we are looking for contributors and maintainers.
-
-### **You only support Pinecone. Do you have plans to extend the list?**
-Yes! Over time, we will also add Chroma, Weaviate, Redis, Elastic Search, and other 
-popular solutions. If you want to help us out, check out our contribution section.
-
-### **Why can't I find any info related to document loaders?**
-For the time being, we have decided not to implement document loaders for a few reasons:
-
-1. plenty of capable libraries like Llama-index and langchain have tons of loaders.
-2. We think mixing document loaders with LLM and prompt management libraries is awkward 
-3. since document loading usually happens in separate pipelines and is not part of the 
-4. LLM-powered app.
-5. Real-life documents are messy. In our experience, no matter how many loaders are out 
-6. there, they will never cover all the specific use cases.
-
-While we will not invest time into document loaders, we might change direction if we 
-get significant interest and contributors.
-
 ## License
 LLMFlows is covered by the MIT license. For more information, check `LICENCE.md`.
 
 ## Contributing
-Thank you for spending the time to read our README! If you like what you saw and are 
-considering contributing, please check `CONTRIBUTING.md`
+Thank you for spending time going over our README! If you find LLMFlows exciting and 
+you are considering contributing, please check [`CONTRIBUTING.md`](https://github.com/stoyan-stoyanov/llmflows/blob/main/CONTRIBUTING.md).
```

### Comparing `llmflows-0.0.7/README.md` & `llmflows-0.0.8/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,7 +1,21 @@
+Metadata-Version: 2.1
+Name: llmflows
+Version: 0.0.8
+Summary: LLMFlows - Simple, Explicit and Transparent LLM Apps
+Author: Stoyan Stoyanov
+Project-URL: Homepage, https://github.com/stoyan-stoyanov/llmflows
+Project-URL: github, https://github.com/stoyan-stoyanov/llmflows
+Classifier: Programming Language :: Python :: 3
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Operating System :: OS Independent
+Requires-Python: >=3.9
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
 # LLMFlows - Simple, Explicit, and Transparent LLM Apps
 
 <p align="center">
   <img style="width: 80%" src="docs/llmflows_last_logo.png" />
 </p>
 
 [![Twitter](https://img.shields.io/twitter/follow/LLMFlows?style=social)](https://twitter.com/LLMFlows)
@@ -13,140 +27,218 @@
 
 Documentation: [https://readthedocs.org](https://readthedocs.org/)<br/>
 PyPI: [https://pypi.org/project/llmflows](https://pypi.org/project/llmflows/)</br>
 Twitter: [https://twitter.com/LLMFlows](https://twitter.com/LLMFlows)<br/>
 Substack: [https://llmflows.substack.com](https://llmflows.substack.com/)<br/>
 
 ## About
-LLMFlows is a framework for building simple, explicit, and transparent LLM applications.
+LLMFlows is a framework for building simple, explicit, and transparent LLM(Large 
+Language Model) applications.
 
 ## Installation
 ```
 pip install llmflows
 ```
 
 ## Philosophy
 
 ### **Simple**
 Our goal is to build a simple, well-documented framework with minimal abstractions that 
 allow users to build flexible LLM-powered apps without compromising on capabilities.
 
 ### **Explicit**
 We want to create an explicit API enabling users to write clean and readable code while 
-easily creating complex flows of LLMs interacting with each other.
+easily creating complex flows of LLMs interacting with each other. LLMFlows' classes 
+give users full control and do not have any hidden prompts or LLM calls. 
 
 ### **Transparent**
 We aim to help users have full transparency on their LLM-powered apps by providing 
 traceable flows and complete information for each app component, making it easy to 
 monitor, maintain, and debug.
 
+## Getting Started
+### LLMs
+LLMs are one of the main abstractions in LLMFlows. LLM classes are wrappers around LLM 
+APIs such as OpenAI's APIs. They provide methods for configuring and calling these APIs, 
+retrying failed calls, and formatting the responses.
+
+```python
+from llmflows.llms import OpenAI
 
-## Usage
-You can quickly build a simple application with LLMFlows' `LLM` and `PrompTemplate` 
-classes:
+llm = OpenAI(api_key="<your-openai-api-key>")
+
+result, call_data, model_config = llm.generate(
+   prompt="Generate a cool title for an 80s rock song"
+)
+```
+
+
+### PromptTemplates
+The `PromptTemplate` class allows us to create strings with variables that we can fill 
+in dynamically later on. Once a prompt template object is created an actual prompt can 
+be generated by providing the required variables.
 
 ```python
+from llmflows.llms import OpenAI
+from llmflows.prompts import PromptTemplate
 
-from llmflows.llms.openai import OpenAI
-from llmflows.prompts.prompt_template import PromptTemplate
 
 prompt_template = PromptTemplate(
-   prompt="Generate a title for a 90s hip-hop song about {topic}."
+    prompt="Generate a title for a 90s hip-hop song about {topic}."
 )
 llm_prompt = prompt_template.get_prompt(topic="friendship")
 
-llm = OpenAI()
+print(llm_prompt)
+
+llm = OpenAI(api_key="<your-openai-api-key>")
 song_title = llm.generate(llm_prompt)
 
+print(song_title)
 ```
 
-You can also create a simple chat application with a few lines of code:
-```python
-from llmflows.llms import OpenAIChat
+### Chat LLMs
+Unlike regular LLMs that only require a prompt to generate text, chat LLMs require a 
+conversation history. The conversation history is represented 
+as a list of messages between a user and an assistant. This conversation history is 
+sent to the model, and a new message is generated based on it.
 
+LLMFlows provides a `MessageHistory` class to manage the required conversation history 
+for chat LLMs.
 
-llm = OpenAIChat(system_prompt="You are a useful assistant")
+You can build a simple chatbot by using the `OpenAIChat` and `MessageHistory` classes:
+
+```python
+from llmflows.llms import OpenAIChat, MessageHistory
+
+llm = OpenAIChat(api_key="<your-openai-api-key>")
+message_history = MessageHistory()
 
 while True:
     user_message = input("You:")
-    llm.add_message(user_message)
-    llm_response, call_data, model_config = llm.generate()
+    message_history.add_user_message(user_message)
+
+    llm_response, call_data, model_config = llm.generate(message_history)
+    message_history.add_ai_message(llm_response)
+
     print(f"LLM: {llm_response}")
 ```
 
-However, real-world applications are often more complex and have dependencies between 
-prompts and LLM calls. For example:
+### LLM Flows
+Often times, real-world applications can be more complex and can have dependencies 
+between prompts and LLM calls. For example:
 
 ![Complex flow](docs/complex_flow.png)
 
-You can build such flow using the `Flow` and `Flowstep` classes. LLMFlows will figure 
-out the dependencies and make sure each flowstep runs only when all its dependencies 
-are met:
+When you want to build apps with complex dependencies you can use the `Flow` and 
+`Flowstep` classes. LLMFlows will figure out the dependencies and make sure each 
+flowstep runs only when all its dependencies are met:
 
 ```python
 from llmflows.flows import Flow, FlowStep
 from llmflows.llms import OpenAI
 from llmflows.prompts import PromptTemplate
 
+openai_llm = OpenAI(api_key="<your-openai-api-key>")
+
 # Create prompt templates
 title_template = PromptTemplate("What is a good title of a movie about {topic}?")
 song_template = PromptTemplate(
     "What is a good song title of a soundtrack for a movie called {movie_title}?"
 )
 characters_template = PromptTemplate(
     "What are two main characters for a movie called {movie_title}?"
 )
 lyrics_template = PromptTemplate(
     "Write lyrics of a movie song called {song_title}. The main characters are "
     "{main_characters}"
 )
 
 # Create flowsteps
-flowstep1 = FlowStep(
+movie_title_flowstep = FlowStep(
+    name="Movie Title Flowstep",
+    llm=openai_llm,
+    prompt_template=title_template,
+    output_key="movie_title",
+)
+
+song_title_flowstep = FlowStep(
+    name="Song Title Flowstep",
+    llm=openai_llm,
+    prompt_template=song_template,
+    output_key="song_title",
+)
+
+characters_flowstep = FlowStep(
+    name="Characters Flowstep",
+    llm=openai_llm,
+    prompt_template=characters_template,
+    output_key="main_characters",
+)
+
+song_lyrics_flowstep = FlowStep(
+    name="Song Lyrics Flowstep",
+    llm=openai_llm,
+    prompt_template=lyrics_template,
+    output_key="song_lyrics",
+)
+
+# Connect flowsteps
+movie_title_flowstep.connect(song_title_flowstep, characters_flowstep, song_lyrics_flowstep)
+song_title_flowstep.connect(song_lyrics_flowstep)
+characters_flowstep.connect(song_lyrics_flowstep)
+
+# Create and run Flow
+soundtrack_flow = Flow(title_flowstep)
+results = soundtrack_flow.start(topic="friendship", verbose=True)
+```
+
+### Async Flows
+Sometimes multiple flow steps can run in parallel if all their dependencies are met. 
+For cases like this, LLMFlows provides async classes to improve the runtime of any 
+complex flow by running flow steps that already have all their required inputs in 
+parallel.
+
+```python
+
+...
+
+movie_title_flowstep = AsyncFlowStep(
     name="Flowstep 1",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=title_template,
     output_key="movie_title",
 )
 
-flowstep2 = FlowStep(
+song_title_flowstep = FlowStep(
     name="Flowstep 2",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=song_template,
     output_key="song_title",
 )
 
-flowstep3 = FlowStep(
+characters_flowstep = AsyncFlowStep(
     name="Flowstep 3",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=characters_template,
     output_key="main_characters",
 )
 
-flowstep4 = FlowStep(
+song_lyrics_flowstep = AsyncFlowStep(
     name="Flowstep 4",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=lyrics_template,
     output_key="song_lyrics",
 )
 
-# Connect flowsteps
-flowstep1.connect(flowstep2, flowstep3, flowstep4)
-flowstep2.connect(flowstep4)
-flowstep3.connect(flowstep4)
+...
 
-# Create and run Flow
-soundtrack_flow = Flow(flowstep1)
-results = soundtrack_flow.start(topic="friendship", verbose=True)
 ```
 
-In addition, LLMFlows provides async classes to improve the runtime of any complex flow 
-by running flow steps that already have all their required inputs in parallel.
-Check our documentation for more examples, such as creating question-answering apps and 
-web applications with Flask and FastAPI.
+Check our documentation for more examples, such as integrating vector databases, 
+creating question-answering apps and web applications with Flask and FastAPI.
 
 ## Features
 
 ### **LLMs**
 - Utilize LLMs such as OpenAI's ChatGPT to generate natural language text.
 - Configure LLM classes easily, choosing specific models, parameters, and settings.
 - Benefit from automatic retries when model calls fail, ensuring reliable LLM 
@@ -173,61 +265,29 @@
 - Leverage vector databases for seamless storage and querying of vectors, enabling straightforward integration with LLM-powered applications.
 
 ### **Callbacks**
 - Execute callback functions at different stages within flow steps, enabling enhanced customization, logging, tracing, or other specific integrations.
 - Utilize callbacks to comprehensively control and monitor LLM-powered apps, ensuring 
   clear visibility into the execution process.
 
-### **Complete Transparency**
-After executing a Flow you can answer questions such as:
+### **Explicit API and Full Transparency**
+With LLMFlows you have the full control to create explicit applications without any hidden prompts or predefined behaviors.
+
+In addition LLMFlows allows you to answer questions such as:
 
 - When was a particular flowstep run?
 - How much time did it take?
 - What were the input variables?
 - What was the prompt template?
 - What did the prompt look like?
 - What was the exact configuration of the model?
 - How many times did we retry the request?
 - What was the raw data the API returned?
 - How many tokens were used?
 - What was the final result?
 
-## FAQ
-
-### **How is this different than langchain?**
-Langchain is a great library, and LLMFlows has undoubtedly been inspired by it. 
-However, our philosophy is a bit different. Langchian has a "chain for everything" 
-philosophy and provides many classes with multiple LLM calls, logic, and built-in 
-default prompts. While this is great for beginners and default use cases, we feel this 
-can be overwhelming if users want to do anything "out of the ordinary." In contrast, 
-we are focusing on providing as few building blocks as possible and having an 
-easy-to-understand API while matching (and in some cases exceeding) the capabilities 
-of langchain.
-
-### **You only have OpenAI wrappers, but I want to use AcmeLLM.**
-We decided to release the library initially supporting only OpenAI LLMs, but we have a 
-roadmap and will slowly add new wrappers around the most popular models. If you are 
-willing to spend some time, we are looking for contributors and maintainers.
-
-### **You only support Pinecone. Do you have plans to extend the list?**
-Yes! Over time, we will also add Chroma, Weaviate, Redis, Elastic Search, and other 
-popular solutions. If you want to help us out, check out our contribution section.
-
-### **Why can't I find any info related to document loaders?**
-For the time being, we have decided not to implement document loaders for a few reasons:
-
-1. plenty of capable libraries like Llama-index and langchain have tons of loaders.
-2. We think mixing document loaders with LLM and prompt management libraries is awkward 
-3. since document loading usually happens in separate pipelines and is not part of the 
-4. LLM-powered app.
-5. Real-life documents are messy. In our experience, no matter how many loaders are out 
-6. there, they will never cover all the specific use cases.
-
-While we will not invest time into document loaders, we might change direction if we 
-get significant interest and contributors.
-
 ## License
 LLMFlows is covered by the MIT license. For more information, check `LICENCE.md`.
 
 ## Contributing
-Thank you for spending the time to read our README! If you like what you saw and are 
-considering contributing, please check `CONTRIBUTING.md`
+Thank you for spending time going over our README! If you find LLMFlows exciting and 
+you are considering contributing, please check [`CONTRIBUTING.md`](https://github.com/stoyan-stoyanov/llmflows/blob/main/CONTRIBUTING.md).
```

### Comparing `llmflows-0.0.7/llmflows/callbacks/async_base_callback.py` & `llmflows-0.0.8/llmflows/callbacks/async_base_callback.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/callbacks/async_functional_callback.py` & `llmflows-0.0.8/llmflows/callbacks/async_functional_callback.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/callbacks/base_callback.py` & `llmflows-0.0.8/llmflows/callbacks/base_callback.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/callbacks/functional_callback.py` & `llmflows-0.0.8/llmflows/callbacks/functional_callback.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/flows/async_base_flow.py` & `llmflows-0.0.8/llmflows/flows/async_base_flow.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/flows/async_base_flowstep.py` & `llmflows-0.0.8/llmflows/flows/async_base_flowstep.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/flows/async_chat_flowstep.py` & `llmflows-0.0.8/llmflows/flows/async_chat_flowstep.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/flows/async_flow.py` & `llmflows-0.0.8/llmflows/flows/async_flow.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/flows/async_flowstep.py` & `llmflows-0.0.8/llmflows/flows/async_flowstep.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/flows/base_flow.py` & `llmflows-0.0.8/llmflows/flows/base_flow.py`

 * *Files 1% similar despite different names*

```diff
@@ -103,16 +103,14 @@
         Args:
             user_inputs (dict): The set of input keys provided by the user.
 
         Raises:
             ValueError: If not all required input keys are covered.
         """
 
-        print(self.output_keys.union(user_inputs.keys()))
-        print(self.input_keys)
         if not self.input_keys.issubset(self.output_keys.union(user_inputs.keys())):
             missing_inputs = self.input_keys.difference(
                 self.output_keys.union(user_inputs.keys())
             )
             raise ValueError(f"Some flowsteps have missing inputs: {missing_inputs}")
 
     def start(self, **inputs):
```

### Comparing `llmflows-0.0.7/llmflows/flows/base_flowstep.py` & `llmflows-0.0.8/llmflows/flows/base_flowstep.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/flows/chat_flowstep.py` & `llmflows-0.0.8/llmflows/flows/chat_flowstep.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/flows/flow.py` & `llmflows-0.0.8/llmflows/flows/flow.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/flows/flowstep.py` & `llmflows-0.0.8/llmflows/flows/flowstep.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/flows/functional_flowstep.py` & `llmflows-0.0.8/llmflows/flows/functional_flowstep.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/flows/vectorstore_flowstep.py` & `llmflows-0.0.8/llmflows/flows/vectorstore_flowstep.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/llms/llm.py` & `llmflows-0.0.8/llmflows/llms/llm.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/llms/llm_utils.py` & `llmflows-0.0.8/llmflows/llms/llm_utils.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/llms/message_history.py` & `llmflows-0.0.8/llmflows/llms/message_history.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/llms/openai.py` & `llmflows-0.0.8/llmflows/llms/openai.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/llms/openai_chat.py` & `llmflows-0.0.8/llmflows/llms/openai_chat.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/llms/openai_embeddings.py` & `llmflows-0.0.8/llmflows/llms/openai_embeddings.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/prompts/prompt_template.py` & `llmflows-0.0.8/llmflows/prompts/prompt_template.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/vectorstores/pinecone.py` & `llmflows-0.0.8/llmflows/vectorstores/pinecone.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/vectorstores/vector_doc.py` & `llmflows-0.0.8/llmflows/vectorstores/vector_doc.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows/vectorstores/vector_store.py` & `llmflows-0.0.8/llmflows/vectorstores/vector_store.py`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/llmflows.egg-info/PKG-INFO` & `llmflows-0.0.8/llmflows.egg-info/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: llmflows
-Version: 0.0.7
+Version: 0.0.8
 Summary: LLMFlows - Simple, Explicit and Transparent LLM Apps
 Author: Stoyan Stoyanov
 Project-URL: Homepage, https://github.com/stoyan-stoyanov/llmflows
 Project-URL: github, https://github.com/stoyan-stoyanov/llmflows
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -27,140 +27,218 @@
 
 Documentation: [https://readthedocs.org](https://readthedocs.org/)<br/>
 PyPI: [https://pypi.org/project/llmflows](https://pypi.org/project/llmflows/)</br>
 Twitter: [https://twitter.com/LLMFlows](https://twitter.com/LLMFlows)<br/>
 Substack: [https://llmflows.substack.com](https://llmflows.substack.com/)<br/>
 
 ## About
-LLMFlows is a framework for building simple, explicit, and transparent LLM applications.
+LLMFlows is a framework for building simple, explicit, and transparent LLM(Large 
+Language Model) applications.
 
 ## Installation
 ```
 pip install llmflows
 ```
 
 ## Philosophy
 
 ### **Simple**
 Our goal is to build a simple, well-documented framework with minimal abstractions that 
 allow users to build flexible LLM-powered apps without compromising on capabilities.
 
 ### **Explicit**
 We want to create an explicit API enabling users to write clean and readable code while 
-easily creating complex flows of LLMs interacting with each other.
+easily creating complex flows of LLMs interacting with each other. LLMFlows' classes 
+give users full control and do not have any hidden prompts or LLM calls. 
 
 ### **Transparent**
 We aim to help users have full transparency on their LLM-powered apps by providing 
 traceable flows and complete information for each app component, making it easy to 
 monitor, maintain, and debug.
 
+## Getting Started
+### LLMs
+LLMs are one of the main abstractions in LLMFlows. LLM classes are wrappers around LLM 
+APIs such as OpenAI's APIs. They provide methods for configuring and calling these APIs, 
+retrying failed calls, and formatting the responses.
+
+```python
+from llmflows.llms import OpenAI
+
+llm = OpenAI(api_key="<your-openai-api-key>")
+
+result, call_data, model_config = llm.generate(
+   prompt="Generate a cool title for an 80s rock song"
+)
+```
 
-## Usage
-You can quickly build a simple application with LLMFlows' `LLM` and `PrompTemplate` 
-classes:
+
+### PromptTemplates
+The `PromptTemplate` class allows us to create strings with variables that we can fill 
+in dynamically later on. Once a prompt template object is created an actual prompt can 
+be generated by providing the required variables.
 
 ```python
+from llmflows.llms import OpenAI
+from llmflows.prompts import PromptTemplate
 
-from llmflows.llms.openai import OpenAI
-from llmflows.prompts.prompt_template import PromptTemplate
 
 prompt_template = PromptTemplate(
-   prompt="Generate a title for a 90s hip-hop song about {topic}."
+    prompt="Generate a title for a 90s hip-hop song about {topic}."
 )
 llm_prompt = prompt_template.get_prompt(topic="friendship")
 
-llm = OpenAI()
+print(llm_prompt)
+
+llm = OpenAI(api_key="<your-openai-api-key>")
 song_title = llm.generate(llm_prompt)
 
+print(song_title)
 ```
 
-You can also create a simple chat application with a few lines of code:
-```python
-from llmflows.llms import OpenAIChat
+### Chat LLMs
+Unlike regular LLMs that only require a prompt to generate text, chat LLMs require a 
+conversation history. The conversation history is represented 
+as a list of messages between a user and an assistant. This conversation history is 
+sent to the model, and a new message is generated based on it.
+
+LLMFlows provides a `MessageHistory` class to manage the required conversation history 
+for chat LLMs.
 
+You can build a simple chatbot by using the `OpenAIChat` and `MessageHistory` classes:
 
-llm = OpenAIChat(system_prompt="You are a useful assistant")
+```python
+from llmflows.llms import OpenAIChat, MessageHistory
+
+llm = OpenAIChat(api_key="<your-openai-api-key>")
+message_history = MessageHistory()
 
 while True:
     user_message = input("You:")
-    llm.add_message(user_message)
-    llm_response, call_data, model_config = llm.generate()
+    message_history.add_user_message(user_message)
+
+    llm_response, call_data, model_config = llm.generate(message_history)
+    message_history.add_ai_message(llm_response)
+
     print(f"LLM: {llm_response}")
 ```
 
-However, real-world applications are often more complex and have dependencies between 
-prompts and LLM calls. For example:
+### LLM Flows
+Often times, real-world applications can be more complex and can have dependencies 
+between prompts and LLM calls. For example:
 
 ![Complex flow](docs/complex_flow.png)
 
-You can build such flow using the `Flow` and `Flowstep` classes. LLMFlows will figure 
-out the dependencies and make sure each flowstep runs only when all its dependencies 
-are met:
+When you want to build apps with complex dependencies you can use the `Flow` and 
+`Flowstep` classes. LLMFlows will figure out the dependencies and make sure each 
+flowstep runs only when all its dependencies are met:
 
 ```python
 from llmflows.flows import Flow, FlowStep
 from llmflows.llms import OpenAI
 from llmflows.prompts import PromptTemplate
 
+openai_llm = OpenAI(api_key="<your-openai-api-key>")
+
 # Create prompt templates
 title_template = PromptTemplate("What is a good title of a movie about {topic}?")
 song_template = PromptTemplate(
     "What is a good song title of a soundtrack for a movie called {movie_title}?"
 )
 characters_template = PromptTemplate(
     "What are two main characters for a movie called {movie_title}?"
 )
 lyrics_template = PromptTemplate(
     "Write lyrics of a movie song called {song_title}. The main characters are "
     "{main_characters}"
 )
 
 # Create flowsteps
-flowstep1 = FlowStep(
+movie_title_flowstep = FlowStep(
+    name="Movie Title Flowstep",
+    llm=openai_llm,
+    prompt_template=title_template,
+    output_key="movie_title",
+)
+
+song_title_flowstep = FlowStep(
+    name="Song Title Flowstep",
+    llm=openai_llm,
+    prompt_template=song_template,
+    output_key="song_title",
+)
+
+characters_flowstep = FlowStep(
+    name="Characters Flowstep",
+    llm=openai_llm,
+    prompt_template=characters_template,
+    output_key="main_characters",
+)
+
+song_lyrics_flowstep = FlowStep(
+    name="Song Lyrics Flowstep",
+    llm=openai_llm,
+    prompt_template=lyrics_template,
+    output_key="song_lyrics",
+)
+
+# Connect flowsteps
+movie_title_flowstep.connect(song_title_flowstep, characters_flowstep, song_lyrics_flowstep)
+song_title_flowstep.connect(song_lyrics_flowstep)
+characters_flowstep.connect(song_lyrics_flowstep)
+
+# Create and run Flow
+soundtrack_flow = Flow(title_flowstep)
+results = soundtrack_flow.start(topic="friendship", verbose=True)
+```
+
+### Async Flows
+Sometimes multiple flow steps can run in parallel if all their dependencies are met. 
+For cases like this, LLMFlows provides async classes to improve the runtime of any 
+complex flow by running flow steps that already have all their required inputs in 
+parallel.
+
+```python
+
+...
+
+movie_title_flowstep = AsyncFlowStep(
     name="Flowstep 1",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=title_template,
     output_key="movie_title",
 )
 
-flowstep2 = FlowStep(
+song_title_flowstep = FlowStep(
     name="Flowstep 2",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=song_template,
     output_key="song_title",
 )
 
-flowstep3 = FlowStep(
+characters_flowstep = AsyncFlowStep(
     name="Flowstep 3",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=characters_template,
     output_key="main_characters",
 )
 
-flowstep4 = FlowStep(
+song_lyrics_flowstep = AsyncFlowStep(
     name="Flowstep 4",
-    llm=OpenAI(),
+    llm=openai_llm,
     prompt_template=lyrics_template,
     output_key="song_lyrics",
 )
 
-# Connect flowsteps
-flowstep1.connect(flowstep2, flowstep3, flowstep4)
-flowstep2.connect(flowstep4)
-flowstep3.connect(flowstep4)
+...
 
-# Create and run Flow
-soundtrack_flow = Flow(flowstep1)
-results = soundtrack_flow.start(topic="friendship", verbose=True)
 ```
 
-In addition, LLMFlows provides async classes to improve the runtime of any complex flow 
-by running flow steps that already have all their required inputs in parallel.
-Check our documentation for more examples, such as creating question-answering apps and 
-web applications with Flask and FastAPI.
+Check our documentation for more examples, such as integrating vector databases, 
+creating question-answering apps and web applications with Flask and FastAPI.
 
 ## Features
 
 ### **LLMs**
 - Utilize LLMs such as OpenAI's ChatGPT to generate natural language text.
 - Configure LLM classes easily, choosing specific models, parameters, and settings.
 - Benefit from automatic retries when model calls fail, ensuring reliable LLM 
@@ -187,61 +265,29 @@
 - Leverage vector databases for seamless storage and querying of vectors, enabling straightforward integration with LLM-powered applications.
 
 ### **Callbacks**
 - Execute callback functions at different stages within flow steps, enabling enhanced customization, logging, tracing, or other specific integrations.
 - Utilize callbacks to comprehensively control and monitor LLM-powered apps, ensuring 
   clear visibility into the execution process.
 
-### **Complete Transparency**
-After executing a Flow you can answer questions such as:
+### **Explicit API and Full Transparency**
+With LLMFlows you have the full control to create explicit applications without any hidden prompts or predefined behaviors.
+
+In addition LLMFlows allows you to answer questions such as:
 
 - When was a particular flowstep run?
 - How much time did it take?
 - What were the input variables?
 - What was the prompt template?
 - What did the prompt look like?
 - What was the exact configuration of the model?
 - How many times did we retry the request?
 - What was the raw data the API returned?
 - How many tokens were used?
 - What was the final result?
 
-## FAQ
-
-### **How is this different than langchain?**
-Langchain is a great library, and LLMFlows has undoubtedly been inspired by it. 
-However, our philosophy is a bit different. Langchian has a "chain for everything" 
-philosophy and provides many classes with multiple LLM calls, logic, and built-in 
-default prompts. While this is great for beginners and default use cases, we feel this 
-can be overwhelming if users want to do anything "out of the ordinary." In contrast, 
-we are focusing on providing as few building blocks as possible and having an 
-easy-to-understand API while matching (and in some cases exceeding) the capabilities 
-of langchain.
-
-### **You only have OpenAI wrappers, but I want to use AcmeLLM.**
-We decided to release the library initially supporting only OpenAI LLMs, but we have a 
-roadmap and will slowly add new wrappers around the most popular models. If you are 
-willing to spend some time, we are looking for contributors and maintainers.
-
-### **You only support Pinecone. Do you have plans to extend the list?**
-Yes! Over time, we will also add Chroma, Weaviate, Redis, Elastic Search, and other 
-popular solutions. If you want to help us out, check out our contribution section.
-
-### **Why can't I find any info related to document loaders?**
-For the time being, we have decided not to implement document loaders for a few reasons:
-
-1. plenty of capable libraries like Llama-index and langchain have tons of loaders.
-2. We think mixing document loaders with LLM and prompt management libraries is awkward 
-3. since document loading usually happens in separate pipelines and is not part of the 
-4. LLM-powered app.
-5. Real-life documents are messy. In our experience, no matter how many loaders are out 
-6. there, they will never cover all the specific use cases.
-
-While we will not invest time into document loaders, we might change direction if we 
-get significant interest and contributors.
-
 ## License
 LLMFlows is covered by the MIT license. For more information, check `LICENCE.md`.
 
 ## Contributing
-Thank you for spending the time to read our README! If you like what you saw and are 
-considering contributing, please check `CONTRIBUTING.md`
+Thank you for spending time going over our README! If you find LLMFlows exciting and 
+you are considering contributing, please check [`CONTRIBUTING.md`](https://github.com/stoyan-stoyanov/llmflows/blob/main/CONTRIBUTING.md).
```

### Comparing `llmflows-0.0.7/llmflows.egg-info/SOURCES.txt` & `llmflows-0.0.8/llmflows.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `llmflows-0.0.7/pyproject.toml` & `llmflows-0.0.8/pyproject.toml`

 * *Files 17% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "llmflows"
-version = "0.0.7"
+version = "0.0.8"
 authors = [
   { name="Stoyan Stoyanov"},
 ]
 description = "LLMFlows - Simple, Explicit and Transparent LLM Apps"
 readme = "README.md"
 requires-python = ">=3.9"
 classifiers = [
```

