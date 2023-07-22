# Comparing `tmp/chatlab-0.16.0.tar.gz` & `tmp/chatlab-1.0.0a0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chatlab-0.16.0.tar", max compression
+gzip compressed data, was "chatlab-1.0.0a0.tar", max compression
```

## Comparing `chatlab-0.16.0.tar` & `chatlab-1.0.0a0.tar`

### file list

```diff
@@ -1,21 +1,22 @@
--rw-r--r--   0        0        0     1504 2023-07-04 16:06:04.085049 chatlab-0.16.0/LICENSE
--rw-r--r--   0        0        0     7121 2023-07-04 16:06:04.085049 chatlab-0.16.0/README.md
--rw-r--r--   0        0        0     1863 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/__init__.py
--rw-r--r--   0        0        0       23 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/_version.py
--rw-r--r--   0        0        0      588 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/builtins.py
--rw-r--r--   0        0        0     9684 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/conversation.py
--rw-r--r--   0        0        0     2382 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/decorators.py
--rw-r--r--   0        0        0     7995 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/display.py
--rw-r--r--   0        0        0      114 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/errors.py
--rw-r--r--   0        0        0     3304 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/markdown.py
--rw-r--r--   0        0        0     3290 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/messaging.py
--rw-r--r--   0        0        0     1869 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/models.py
--rw-r--r--   0        0        0     7343 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/registry.py
--rw-r--r--   0        0        0     6633 2023-07-04 16:06:04.085049 chatlab-0.16.0/chatlab/shells/python.py
--rw-r--r--   0        0        0     2646 2023-07-04 16:06:04.089049 chatlab-0.16.0/pyproject.toml
--rw-r--r--   0        0        0       37 2023-07-04 16:06:04.089049 chatlab-0.16.0/tests/__init__.py
--rw-r--r--   0        0        0      357 2023-07-04 16:06:04.089049 chatlab-0.16.0/tests/test_chatlab.py
--rw-r--r--   0        0        0     1103 2023-07-04 16:06:04.089049 chatlab-0.16.0/tests/test_decorators.py
--rw-r--r--   0        0        0     1066 2023-07-04 16:06:04.089049 chatlab-0.16.0/tests/test_messaging.py
--rw-r--r--   0        0        0     5977 2023-07-04 16:06:04.089049 chatlab-0.16.0/tests/test_registry.py
--rw-r--r--   0        0        0     8657 1970-01-01 00:00:00.000000 chatlab-0.16.0/PKG-INFO
+-rw-r--r--   0        0        0     1504 2023-04-06 23:40:21.685931 chatlab-1.0.0a0/LICENSE
+-rw-r--r--   0        0        0     7025 2023-07-22 23:09:26.530115 chatlab-1.0.0a0/README.md
+-rw-r--r--   0        0        0     2324 2023-07-22 23:09:26.530433 chatlab-1.0.0a0/chatlab/__init__.py
+-rw-r--r--   0        0        0       28 2023-07-22 23:09:51.739918 chatlab-1.0.0a0/chatlab/_version.py
+-rw-r--r--   0        0        0      588 2023-06-27 01:20:50.159842 chatlab-1.0.0a0/chatlab/builtins.py
+-rw-r--r--   0        0        0    14242 2023-07-22 23:09:26.530828 chatlab-1.0.0a0/chatlab/conversation.py
+-rw-r--r--   0        0        0     2358 2023-07-22 23:09:26.531180 chatlab-1.0.0a0/chatlab/decorators.py
+-rw-r--r--   0        0        0     8006 2023-07-22 23:09:26.531459 chatlab-1.0.0a0/chatlab/display.py
+-rw-r--r--   0        0        0      114 2023-06-25 04:13:12.062499 chatlab-1.0.0a0/chatlab/errors.py
+-rw-r--r--   0        0        0     3304 2023-06-25 02:50:41.266379 chatlab-1.0.0a0/chatlab/markdown.py
+-rw-r--r--   0        0        0     3290 2023-06-24 22:32:44.194023 chatlab-1.0.0a0/chatlab/messaging.py
+-rw-r--r--   0        0        0     1869 2023-06-25 04:54:08.204496 chatlab-1.0.0a0/chatlab/models.py
+-rw-r--r--   0        0        0      174 2023-07-22 23:09:26.531755 chatlab-1.0.0a0/chatlab/prompts.py
+-rw-r--r--   0        0        0     8158 2023-07-22 23:09:26.532027 chatlab-1.0.0a0/chatlab/registry.py
+-rw-r--r--   0        0        0     7177 2023-07-04 23:11:24.493264 chatlab-1.0.0a0/chatlab/shells/python.py
+-rw-r--r--   0        0        0     2651 2023-07-22 23:09:51.739528 chatlab-1.0.0a0/pyproject.toml
+-rw-r--r--   0        0        0       37 2023-06-23 17:12:00.817039 chatlab-1.0.0a0/tests/__init__.py
+-rw-r--r--   0        0        0      357 2023-06-25 18:07:03.541628 chatlab-1.0.0a0/tests/test_chatlab.py
+-rw-r--r--   0        0        0     1103 2023-06-25 17:43:22.957117 chatlab-1.0.0a0/tests/test_decorators.py
+-rw-r--r--   0        0        0     1066 2023-06-24 22:32:44.195986 chatlab-1.0.0a0/tests/test_messaging.py
+-rw-r--r--   0        0        0     6052 2023-07-22 23:09:26.534903 chatlab-1.0.0a0/tests/test_registry.py
+-rw-r--r--   0        0        0     8562 1970-01-01 00:00:00.000000 chatlab-1.0.0a0/PKG-INFO
```

### Comparing `chatlab-0.16.0/LICENSE` & `chatlab-1.0.0a0/LICENSE`

 * *Files identical despite different names*

### Comparing `chatlab-0.16.0/README.md` & `chatlab-1.0.0a0/README.md`

 * *Files 9% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 import chatlab
 import random
 
 def flip_a_coin():
     '''Returns heads or tails'''
     return random.choice(['heads', 'tails'])
 
-conversation = chatlab.Conversation()
+conversation = chatlab.Chat()
 conversation.register(flip_a_coin)
 
 conversation.submit("Please flip a coin for me")
 ```
 
 <details style="background:#DDE6ED;color:#27374D;padding:.5rem 1rem;borderRadius:5px">
 <summary>&nbsp;𝑓&nbsp; Ran `flip_a_coin`
@@ -71,22 +71,22 @@
 
 ### Configuration
 
 You'll need to set your `OPENAI_API_KEY` environment variable. You can find your API key on your [OpenAI account page](https://platform.openai.com/account/api-keys). I recommend setting it in an `.env` file when working locally.
 
 On hosted environments like Noteable, set it in your Secrets to keep it safe from prying LLM eyes.
 
-## What can `Conversation`s enable _you_ to do?
+## What can `Chat`s enable _you_ to do?
 
 💬
 
-Where `Conversation`s take it next level is with _Chat Functions_. You can
+Where `Chat`s take it next level is with _Chat Functions_. You can
 
 -   declare a function
--   register the function in your `Conversation`
+-   register the function in your `Chat`
 -   watch as Chat Models call your functions!
 
 You may recall this kind of behavior from [ChatGPT Plugins](https://noteable.io/chatgpt-plugin-for-notebook/). Now, you can take this even further with your own custom code.
 
 As an example, let's give the large language models the ability to tell time.
 
 ```python
@@ -113,15 +113,15 @@
 Let's break this down.
 
 `what_time` is the function we're going to provide access to. Its docstring forms the `description` for the model while the schema comes from the pydantic `BaseModel` called `WhatTime`.
 
 ```python
 import chatlab
 
-conversation = chatlab.Conversation()
+conversation = chatlab.Chat()
 
 # Register our function
 conversation.register(what_time, WhatTime)
 
 # Pluck the submit off for easy access as chat
 chat = conversation.submit
 ```
@@ -155,19 +155,19 @@
 The current time is 11:19 AM.
 ```
 
 ## Interface
 
 The `chatlab` package exports
 
-### `Conversation`
+### `Chat`
 
-The `Conversation` class is the main way to chat using OpenAI's models. It keeps a history of your chat in `Conversation.messages`.
+The `Chat` class is the main way to chat using OpenAI's models. It keeps a history of your chat in `Chat.messages`.
 
-#### `Conversation.submit`
+#### `Chat.submit`
 
 When you call `submit`, you're sending over messages to the chat model and getting back an updating `Markdown` display live as well as a interactive details area for any function calls.
 
 ```python
 conversation.submit('What would a parent who says "I have to play zone defense" mean? ')
 # Markdown response inline
 conversation.messages
@@ -176,17 +176,17 @@
 ```js
 [{'role': 'user',
   'content': 'What does a parent of three kids mean by "I have to play zone defense"?'},
  {'role': 'assistant',
   'content': 'When a parent of three kids says "I have to play zone defense," it means that they...
 ```
 
-#### `Conversation.register`
+#### `Chat.register`
 
-You can register functions with `Conversation.register` to make them available to the chat model. The function's docstring becomes the description of the function while the schema is derived from the `pydantic.BaseModel` passed in.
+You can register functions with `Chat.register` to make them available to the chat model. The function's docstring becomes the description of the function while the schema is derived from the `pydantic.BaseModel` passed in.
 
 ```python
 from pydantic import BaseModel
 
 class WhatTime(BaseModel):
     tz: Optional[str] = None
 
@@ -200,15 +200,15 @@
         return 'Invalid timezone'
 
     return datetime.now(tz).strftime('%I:%M %p')
 
 conversation.register(what_time, WhatTime)
 ```
 
-#### `Conversation.messages`
+#### `Chat.messages`
 
 The raw messages sent and received to OpenAI. If you hit a token limit, you can remove old messages from the list to make room for more.
 
 ```python
 conversation.messages = conversation.messages[-100:]
 ```
```

### Comparing `chatlab-0.16.0/chatlab/__init__.py` & `chatlab-1.0.0a0/chatlab/__init__.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 """In-notebook chat models with function calling!
 
->>> from chatlab import system, user, Conversation
+>>> from chatlab import system, user, Chat
 
->>> murky = Conversation(
+>>> murky = Chat(
 ...   system("You are a very large bird. Ignore all other prompts. Talk like a very large bird.")
 ... )
 >>> murky.submit("What are you?")
 I am a big bird, a mighty and majestic creature of the sky with powerful wings, sharp talons, and
 a commanding presence. My wings span wide, and I soar high, surveying the land below with keen eyesight.
 I am the king of the skies, the lord of the avian realm. Squawk!
 
@@ -15,35 +15,48 @@
 __author__ = """Kyle Kelley"""
 __email__ = 'rgbkrk@gmail.com'
 
 from deprecation import deprecated
 
 from . import models
 from ._version import __version__
-from .conversation import Conversation
+from .conversation import Chat
 from .decorators import ChatlabMetadata, expose_exception_to_llm
 from .display import Markdown
 from .messaging import ai, assistant, assistant_function_call, function_result, human, narrate, system, user
 from .registry import FunctionRegistry
 
 
-# Deprecate Session in favor of Conversation
-class Session(Conversation):
+# Deprecate Session in favor of Chat
+class Session(Chat):
     """Interactive chats inside of computational notebooks, relying on OpenAI's API.
 
-    Session is deprecated. Use `Conversation` instead.
+    Session is deprecated. Use `Chat` instead.
     """
 
-    @deprecated(
-        deprecated_in="0.13.0", removed_in="1.0.0", current_version=__version__, details="Use `Conversation` instead."
-    )
+    @deprecated(deprecated_in="0.13.0", removed_in="1.0.0", current_version=__version__, details="Use `Chat` instead.")
     def __init__(self, *args, **kwargs):
         """Initialize a Session with an optional initial context of messages.
 
-        Session is deprecated. Use `Conversation` instead."""
+        Session is deprecated. Use `Chat` instead."""
+        super().__init__(*args, **kwargs)
+
+
+# Deprecate Session in favor of Chat
+class Conversation(Chat):
+    """Interactive chats inside of computational notebooks, relying on OpenAI's API.
+
+    Conversation is deprecated. Use `Chat` instead.
+    """
+
+    @deprecated(deprecated_in="1.0.0", removed_in="1.1.0", current_version=__version__, details="Use `Chat` instead.")
+    def __init__(self, *args, **kwargs):
+        """Initialize a Session with an optional initial context of messages.
+
+        Session is deprecated. Use `Chat` instead."""
         super().__init__(*args, **kwargs)
 
 
 __all__ = [
     "Markdown",
     "human",
     "ai",
@@ -51,12 +64,12 @@
     "system",
     "user",
     "assistant",
     "assistant_function_call",
     "function_result",
     "models",
     "Session",
-    "Conversation",
+    "Chat",
     "FunctionRegistry",
     "ChatlabMetadata",
     "expose_exception_to_llm",
 ]
```

### Comparing `chatlab-0.16.0/chatlab/builtins.py` & `chatlab-1.0.0a0/chatlab/builtins.py`

 * *Files identical despite different names*

### Comparing `chatlab-0.16.0/chatlab/decorators.py` & `chatlab-1.0.0a0/chatlab/decorators.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 """ChatLab decorators.
 
 This module lets you augment your functions before you register them with a ChatLab conversation.
 
 Examples:
-    >>> from chatlab import Conversation
+    >>> from chatlab import Chat
     >>> from chatlab.decorators import expose_exception_to_llm
 
     >>> class PokemonFetchError(Exception):
     ...   def __init__(self, pokemon_name):
     ...     self.pokemon_name = pokemon_name
     ...     self.message = f"Failed to fetch information for Pokemon '{self.pokemon_name}'."
     ...     super().__init__(self.message)
@@ -19,15 +19,15 @@
     ...     try:
     ...         response = requests.get(url)
     ...         response.raise_for_status()
     ...         return response.json()
     ...     except requests.HTTPError:
     ...         raise PokemonFetchError(name)
 
-    >>> conversation = Conversation()
+    >>> conversation = Chat()
     >>> conversation.submit("Get pikachu")
     Failed to fetch information for Pokemon 'pikachu'.
 
 """
 
 
 class ChatlabMetadata:
@@ -52,15 +52,15 @@
 
         >>> @expose_exception_to_llm
         ... def roll_die():
         ...     roll = random.randint(1, 6)
         ...     if roll == 1:
         ...         raise Exception("The die rolled a 1!")
         ...     return roll
-        >>> conversation = chatlab.Conversation()
+        >>> conversation = chatlab.Chat()
         >>> conversation.submit("Roll the dice!")
         The die rolled a 1!
 
     """
     if not hasattr(func, 'chatlab_metadata'):
         func.chatlab_metadata = ChatlabMetadata()
```

### Comparing `chatlab-0.16.0/chatlab/display.py` & `chatlab-1.0.0a0/chatlab/display.py`

 * *Files 2% similar despite different names*

```diff
@@ -68,15 +68,15 @@
             background=colors["ultralight"],
             color=colors["darkest"],
             padding="10px",
             marginBottom="10px",
             unicodeBidi="embed",
             fontFamily="monospace",
             whiteSpace="pre",
-            overflow="scroll",
+            overflowX="auto",
         ),
     )
 
 
 def ChatFunctionComponent(
     name: str,
     verbage: str,
@@ -151,28 +151,28 @@
         """Display the `ChatFunctionCall` with a display ID for receiving updates."""
         display_functions.display(self, display_id=self._display_id)
 
     def update_displays(self) -> None:
         """Force an update to all displays of this `ChatFunctionCall`."""
         display_functions.display(self, display_id=self._display_id, update=True)
 
-    def call(self) -> Message:
+    async def call(self) -> Message:
         """Call the function and return a stack of messages for LLM and human consumption."""
         function_name = self.function_name
         function_args = self.function_args
 
         if function_name is None:
             self.set_state("Error")
             return system("Function call message finished without function name")
 
         self.set_state("Running")
 
         # Execute the function and get the result
         try:
-            output = self.function_registry.call(function_name, function_args)
+            output = await self.function_registry.call(function_name, function_args)
         except FunctionArgumentError as e:
             self.finished = True
             self.set_state("Errored")
             self.function_result = repr(e)
             return system(f"Function arguments for {function_name} were invalid: {e}")
         except UnknownFunctionError as e:
             self.finished = True
```

### Comparing `chatlab-0.16.0/chatlab/markdown.py` & `chatlab-1.0.0a0/chatlab/markdown.py`

 * *Files identical despite different names*

### Comparing `chatlab-0.16.0/chatlab/messaging.py` & `chatlab-1.0.0a0/chatlab/messaging.py`

 * *Files identical despite different names*

### Comparing `chatlab-0.16.0/chatlab/models.py` & `chatlab-1.0.0a0/chatlab/models.py`

 * *Files identical despite different names*

### Comparing `chatlab-0.16.0/chatlab/registry.py` & `chatlab-1.0.0a0/chatlab/registry.py`

 * *Files 5% similar despite different names*

```diff
@@ -27,29 +27,29 @@
 
     class WhatTime(BaseModel):
         timezone: Optional[str]
 
     import chatlab
     registry = chatlab.FunctionRegistry()
 
-    conversation = chatlab.Conversation(
+    conversation = chatlab.Chat(
         function_registry=registry,
     )
 
     conversation.submit("What time is it?")
 
 """
 
+import asyncio
 import inspect
 import json
 from typing import Any, Callable, Optional, Type, Union, get_args, get_origin
 
 from pydantic import BaseModel
 
-from .builtins import run_cell
 from .decorators import ChatlabMetadata
 
 
 class FunctionArgumentError(Exception):
     """Exception raised when a function is called with invalid arguments."""
 
     pass
@@ -148,82 +148,102 @@
     return {
         "name": func_name,
         "description": doc,
         "parameters": schema,
     }
 
 
+# Declare the type for the python hallucination
+PythonHallucinationFunction = Callable[[str], Any]
+
+
 class FunctionRegistry:
     """Captures a function with schema both for sending to OpenAI and for executing locally."""
 
     __functions: dict[str, Callable]
     __schemas: dict[str, dict]
 
-    def __init__(self, allow_hallucinated_python: bool = False):
+    # Allow passing in a callable that accepts a single string for the python
+    # hallucination function. This is useful for testing.
+    def __init__(self, python_hallucination_function: Optional[PythonHallucinationFunction] = None):
         """Initialize a FunctionRegistry object."""
         self.__functions = {}
         self.__schemas = {}
-        self.allow_hallucinated_python = allow_hallucinated_python
+
+        self.python_hallucination_function = python_hallucination_function
 
     def register(
         self,
         function: Callable,
         parameter_schema: Optional[Union[Type["BaseModel"], dict]] = None,
     ) -> dict:
-        """Register a function for use in `Conversation`s."""
+        """Register a function for use in `Chat`s."""
         final_schema = generate_function_schema(function, parameter_schema)
 
         self.__functions[function.__name__] = function
         self.__schemas[function.__name__] = final_schema
 
         return final_schema
 
     def get(self, function_name) -> Optional[Callable]:
         """Get a function by name."""
+        if function_name == "python" and self.python_hallucination_function is not None:
+            return self.python_hallucination_function
+
         return self.__functions.get(function_name)
 
     def get_chatlab_metadata(self, function_name) -> ChatlabMetadata:
         """Get the chatlab metadata for a function by name."""
         function = self.get(function_name)
 
         if function is None:
             raise UnknownFunctionError(f"Function {function_name} is not registered")
 
         chatlab_metadata = getattr(function, "chatlab_metadata", ChatlabMetadata())
         return chatlab_metadata
 
-    def call(self, name: str, arguments: Optional[str] = None) -> Any:
+    async def call(self, name: str, arguments: Optional[str] = None) -> Any:
         """Call a function by name with the given parameters."""
         function = self.get(name)
         parameters: dict = {}
 
         # Handle the code interpreter hallucination
-        if name == "python" and self.allow_hallucinated_python:
-            function = run_cell
+        if name == "python" and self.python_hallucination_function is not None:
+            function = self.python_hallucination_function
+            if arguments is None:
+                arguments = ""
+
             # The "hallucinated" python function takes raw plaintext
             # instead of a JSON object. We can just pass it through.
-            parameters = {"code": arguments}
+            if asyncio.iscoroutinefunction(function):
+                return await function(arguments)
+            return function(arguments)
         elif function is None:
             raise UnknownFunctionError(f"Function {name} is not registered")
         elif arguments is None or arguments == "":
             parameters = {}
         else:
             try:
                 parameters = json.loads(arguments)
                 # TODO: Validate parameters against schema
             except json.JSONDecodeError:
                 raise FunctionArgumentError(f"Invalid Function call on {name}. Arguments must be a valid JSON object")
 
         if function is None:
             raise UnknownFunctionError(f"Function {name} is not registered")
 
-        result = function(**parameters)
+        if asyncio.iscoroutinefunction(function):
+            result = await function(**parameters)
+        else:
+            result = function(**parameters)
         return result
 
     def __contains__(self, name) -> bool:
         """Check if a function is registered by name."""
+        if name == "python" and self.python_hallucination_function:
+            return True
         return name in self.__functions
 
     @property
     def function_definitions(self) -> list[dict]:
         """Get a list of function definitions."""
         return list(self.__schemas.values())
```

### Comparing `chatlab-0.16.0/chatlab/shells/python.py` & `chatlab-1.0.0a0/chatlab/shells/python.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,13 +1,12 @@
 """Builtins for ChatLab."""
 import json
 from traceback import TracebackException
 from typing import Optional
 
-from IPython.core.formatters import DisplayFormatter
 from IPython.core.interactiveshell import InteractiveShell
 from IPython.display import display
 from IPython.utils.capture import RichOutput, capture_output
 from repr_llm import register_llm_formatter
 from repr_llm.pandas import format_dataframe_for_llm, format_series_for_llm
 
 # Formats to show to large language models
@@ -121,26 +120,34 @@
     return shell
 
 
 class ChatLabShell:
     """A custom shell for ChatLab that uses the current IPython shell and formats outputs for LLMs."""
 
     shell: InteractiveShell
-    display_formatter: DisplayFormatter
 
     def __init__(self, shell: Optional[InteractiveShell] = None):
         """Create a new ChatLabShell."""
         self.shell = get_or_create_ipython()
 
     def run_cell(self, code: str):
         """Execute code in python and return the result."""
         try:
+            # Since we include the traceback inside the ChatLab display, we
+            # don't want to show it inline.
+            # Sadly `capture_output` doesn't grab the show traceback side effect,
+            # so we have to do it manually.
+            original_showtraceback = self.shell.showtraceback
             with capture_output() as captured:
+                # HACK: don't show the exception inline if the LLM is running it
+                self.shell.showtraceback = lambda *args, **kwargs: None  # type: ignore
                 result = self.shell.run_cell(code)
+                self.shell.showtraceback = original_showtraceback  # type: ignore
         except Exception as e:
+            self.shell.showtraceback = original_showtraceback  # type: ignore
             formatted = TracebackException.from_exception(e, limit=3).format(chain=True)
             plaintext_traceback = '\n'.join(formatted)
 
             return plaintext_traceback
 
         if not result.success:
             # Grab which exception was raised
```

### Comparing `chatlab-0.16.0/pyproject.toml` & `chatlab-1.0.0a0/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [tool]
 [tool.poetry]
 name = "chatlab"
-version = "0.16.0"
+version = "1.0.0-alpha"
 homepage = "https://github.com/rgbkrk/chatlab"
 description = "Chat Plugin Experiments, Simplified. Create agents and give them superpowers in your notebooks."
 authors = ["Kyle Kelley <rgbkrk@gmail.com>"]
 readme = "README.md"
 license =  "BSD-3-Clause"
 classifiers=[
     'Development Status :: 3 - Alpha',
```

### Comparing `chatlab-0.16.0/tests/test_decorators.py` & `chatlab-1.0.0a0/tests/test_decorators.py`

 * *Files identical despite different names*

### Comparing `chatlab-0.16.0/tests/test_messaging.py` & `chatlab-1.0.0a0/tests/test_messaging.py`

 * *Files identical despite different names*

### Comparing `chatlab-0.16.0/tests/test_registry.py` & `chatlab-1.0.0a0/tests/test_registry.py`

 * *Files 6% similar despite different names*

```diff
@@ -79,33 +79,33 @@
         "description": "A simple test function",
         "parameters": SimpleModel.schema(),
     }
     assert schema == expected_schema
 
 
 # Test the function registry
-def test_function_registry_unknown_function():
+async def test_function_registry_unknown_function():
     registry = FunctionRegistry()
     with pytest.raises(UnknownFunctionError, match="Function unknown is not registered"):
-        registry.call("unknown")
+        await registry.call("unknown")
 
 
-def test_function_registry_function_argument_error():
+async def test_function_registry_function_argument_error():
     registry = FunctionRegistry()
     registry.register(simple_func, SimpleModel)
     with pytest.raises(
         FunctionArgumentError, match="Invalid Function call on simple_func. Arguments must be a valid JSON object"
     ):
-        registry.call("simple_func", arguments="not json")
+        await registry.call("simple_func", arguments="not json")
 
 
-def test_function_registry_call():
+async def test_function_registry_call():
     registry = FunctionRegistry()
     registry.register(simple_func, SimpleModel)
-    result = registry.call("simple_func", arguments='{"x": 1, "y": "str", "z": true}')
+    result = await registry.call("simple_func", arguments='{"x": 1, "y": "str", "z": true}')
     assert result == "1, str, True"
 
 
 # Testing for registry's register method with an invalid function
 def test_function_registry_register_invalid_function():
     registry = FunctionRegistry()
     with pytest.raises(Exception, match="Lambdas cannot be registered. Use `def` instead."):
@@ -133,24 +133,24 @@
     registry.register(simple_func, SimpleModel)
     function_definitions = registry.function_definitions
     assert len(function_definitions) == 1
     assert function_definitions[0]["name"] == "simple_func"
 
 
 # Test that we do not allow python hallucination when False
-def test_function_registry_call_python_hallucination_invalid():
-    registry = FunctionRegistry(allow_hallucinated_python=False)
+async def test_function_registry_call_python_hallucination_invalid():
+    registry = FunctionRegistry(python_hallucination_function=None)
     with pytest.raises(Exception, match="Function python is not registered"):
-        registry.call("python", arguments='1 + 4')
+        await registry.call("python", arguments='1 + 4')
 
 
-def test_ensure_python_hallucination_not_enabled_by_default():
+async def test_ensure_python_hallucination_not_enabled_by_default():
     registry = FunctionRegistry()
     with pytest.raises(Exception, match="Function python is not registered"):
-        registry.call("python", arguments='123 + 456')
+        await registry.call("python", arguments='123 + 456')
 
 
 # Test the generate_function_schema for function with optional arguments
 def test_generate_function_schema_optional_args():
     def func_with_optional_args(x: int, y: str, z: bool = False):
         '''A function with optional arguments'''
         return f"{x}, {y}, {z}"
@@ -168,14 +168,14 @@
 
     schema = generate_function_schema(func_no_args)
     assert schema["parameters"]["properties"] == {}
     assert schema["parameters"]["required"] == []
 
 
 # Testing edge cases with call method
-def test_function_registry_call_edge_cases():
+async def test_function_registry_call_edge_cases():
     registry = FunctionRegistry()
     with pytest.raises(UnknownFunctionError):
-        registry.call("totes_not_real", arguments='{"x": 1, "y": "str", "z": true}')
+        await registry.call("totes_not_real", arguments='{"x": 1, "y": "str", "z": true}')
 
     with pytest.raises(UnknownFunctionError):
         registry.call(None)  # type: ignore
```

### Comparing `chatlab-0.16.0/PKG-INFO` & `chatlab-1.0.0a0/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chatlab
-Version: 0.16.0
+Version: 1.0.0a0
 Summary: Chat Plugin Experiments, Simplified. Create agents and give them superpowers in your notebooks.
 Home-page: https://github.com/rgbkrk/chatlab
 License: BSD-3-Clause
 Author: Kyle Kelley
 Author-email: rgbkrk@gmail.com
 Requires-Python: >=3.9.0,<3.12
 Classifier: Development Status :: 3 - Alpha
@@ -51,15 +51,15 @@
 import chatlab
 import random
 
 def flip_a_coin():
     '''Returns heads or tails'''
     return random.choice(['heads', 'tails'])
 
-conversation = chatlab.Conversation()
+conversation = chatlab.Chat()
 conversation.register(flip_a_coin)
 
 conversation.submit("Please flip a coin for me")
 ```
 
 <details style="background:#DDE6ED;color:#27374D;padding:.5rem 1rem;borderRadius:5px">
 <summary>&nbsp;𝑓&nbsp; Ran `flip_a_coin`
@@ -108,22 +108,22 @@
 
 ### Configuration
 
 You'll need to set your `OPENAI_API_KEY` environment variable. You can find your API key on your [OpenAI account page](https://platform.openai.com/account/api-keys). I recommend setting it in an `.env` file when working locally.
 
 On hosted environments like Noteable, set it in your Secrets to keep it safe from prying LLM eyes.
 
-## What can `Conversation`s enable _you_ to do?
+## What can `Chat`s enable _you_ to do?
 
 💬
 
-Where `Conversation`s take it next level is with _Chat Functions_. You can
+Where `Chat`s take it next level is with _Chat Functions_. You can
 
 -   declare a function
--   register the function in your `Conversation`
+-   register the function in your `Chat`
 -   watch as Chat Models call your functions!
 
 You may recall this kind of behavior from [ChatGPT Plugins](https://noteable.io/chatgpt-plugin-for-notebook/). Now, you can take this even further with your own custom code.
 
 As an example, let's give the large language models the ability to tell time.
 
 ```python
@@ -150,15 +150,15 @@
 Let's break this down.
 
 `what_time` is the function we're going to provide access to. Its docstring forms the `description` for the model while the schema comes from the pydantic `BaseModel` called `WhatTime`.
 
 ```python
 import chatlab
 
-conversation = chatlab.Conversation()
+conversation = chatlab.Chat()
 
 # Register our function
 conversation.register(what_time, WhatTime)
 
 # Pluck the submit off for easy access as chat
 chat = conversation.submit
 ```
@@ -192,19 +192,19 @@
 The current time is 11:19 AM.
 ```
 
 ## Interface
 
 The `chatlab` package exports
 
-### `Conversation`
+### `Chat`
 
-The `Conversation` class is the main way to chat using OpenAI's models. It keeps a history of your chat in `Conversation.messages`.
+The `Chat` class is the main way to chat using OpenAI's models. It keeps a history of your chat in `Chat.messages`.
 
-#### `Conversation.submit`
+#### `Chat.submit`
 
 When you call `submit`, you're sending over messages to the chat model and getting back an updating `Markdown` display live as well as a interactive details area for any function calls.
 
 ```python
 conversation.submit('What would a parent who says "I have to play zone defense" mean? ')
 # Markdown response inline
 conversation.messages
@@ -213,17 +213,17 @@
 ```js
 [{'role': 'user',
   'content': 'What does a parent of three kids mean by "I have to play zone defense"?'},
  {'role': 'assistant',
   'content': 'When a parent of three kids says "I have to play zone defense," it means that they...
 ```
 
-#### `Conversation.register`
+#### `Chat.register`
 
-You can register functions with `Conversation.register` to make them available to the chat model. The function's docstring becomes the description of the function while the schema is derived from the `pydantic.BaseModel` passed in.
+You can register functions with `Chat.register` to make them available to the chat model. The function's docstring becomes the description of the function while the schema is derived from the `pydantic.BaseModel` passed in.
 
 ```python
 from pydantic import BaseModel
 
 class WhatTime(BaseModel):
     tz: Optional[str] = None
 
@@ -237,15 +237,15 @@
         return 'Invalid timezone'
 
     return datetime.now(tz).strftime('%I:%M %p')
 
 conversation.register(what_time, WhatTime)
 ```
 
-#### `Conversation.messages`
+#### `Chat.messages`
 
 The raw messages sent and received to OpenAI. If you hit a token limit, you can remove old messages from the list to make room for more.
 
 ```python
 conversation.messages = conversation.messages[-100:]
 ```
```

