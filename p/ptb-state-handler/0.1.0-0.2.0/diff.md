# Comparing `tmp/ptb-state-handler-0.1.0.tar.gz` & `tmp/ptb_state_handler-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ptb-state-handler-0.1.0.tar", last modified: Sun Oct 18 18:56:20 2020, max compression
+gzip compressed data, was "ptb_state_handler-0.2.0.tar", max compression
```

## Comparing `ptb-state-handler-0.1.0.tar` & `ptb_state_handler-0.2.0.tar`

### file list

```diff
@@ -1,7 +1,6 @@
--rw-r--r--   0        0        0    11357 2020-10-18 18:56:08.095366 ptb-state-handler-0.1.0/LICENSE
--rw-r--r--   0        0        0      498 2020-10-18 18:56:08.095366 ptb-state-handler-0.1.0/pyproject.toml
--rw-r--r--   0        0        0      102 2020-10-18 18:56:08.095366 ptb-state-handler-0.1.0/state_handler/__init__.py
--rw-r--r--   0        0        0      859 2020-10-18 18:56:08.095366 ptb-state-handler-0.1.0/state_handler/state.py
--rw-r--r--   0        0        0     3449 2020-10-18 18:56:08.095366 ptb-state-handler-0.1.0/state_handler/state_handler.py
--rw-r--r--   0        0        0      680 2020-10-18 18:56:20.748451 ptb-state-handler-0.1.0/setup.py
--rw-r--r--   0        0        0      620 2020-10-18 18:56:20.748668 ptb-state-handler-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0    11357 2023-07-23 07:51:50.333359 ptb_state_handler-0.2.0/LICENSE
+-rw-r--r--   0        0        0      497 2023-07-23 07:51:50.333359 ptb_state_handler-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0      102 2023-07-23 07:51:50.333359 ptb_state_handler-0.2.0/state_handler/__init__.py
+-rw-r--r--   0        0        0      899 2023-07-23 07:51:50.333359 ptb_state_handler-0.2.0/state_handler/state.py
+-rw-r--r--   0        0        0     3529 2023-07-23 07:51:50.333359 ptb_state_handler-0.2.0/state_handler/state_handler.py
+-rw-r--r--   0        0        0      626 1970-01-01 00:00:00.000000 ptb_state_handler-0.2.0/PKG-INFO
```

### Comparing `ptb-state-handler-0.1.0/LICENSE` & `ptb_state_handler-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `ptb-state-handler-0.1.0/state_handler/state.py` & `ptb_state_handler-0.2.0/state_handler/state.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,27 +1,27 @@
 from typing import TYPE_CHECKING, Callable, List
 
 from telegram import Update
 
 if TYPE_CHECKING:
-    from telegram.ext import CallbackContext, Dispatcher, Handler
+    from telegram.ext import CallbackContext, Application, BaseHandler
 
 
 class State:
-    def __init__(self, name: str, on_activate: Callable, handlers: List['Handler']):
+    def __init__(self, name: str, on_activate: Callable, handlers: List['BaseHandler']):
         self.name = name
         self.on_activate: Callable = on_activate
-        self.handlers: List['Handler'] = handlers
+        self.handlers: List['BaseHandler'] = handlers
 
-    def activate(self, update: 'Update', context: 'CallbackContext'):
-        return self.on_activate(update, context)
+    async def activate(self, update: 'Update', context: 'CallbackContext'):
+        return await self.on_activate(update, context)
 
-    def handle(
+    async def handle(
         self,
         update: 'Update',
-        dispatcher: 'Dispatcher',
+        application: 'Application',
         context: 'CallbackContext' = None,
     ):
         for handler in self.handlers:
             check_result = handler.check_update(update)
             if check_result:
-                return handler.handle_update(update, dispatcher, check_result, context)
+                return await handler.handle_update(update, application, check_result, context)
```

### Comparing `ptb-state-handler-0.1.0/state_handler/state_handler.py` & `ptb_state_handler-0.2.0/state_handler/state_handler.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 from collections import defaultdict
 from typing import TYPE_CHECKING, Any, Dict, List, Optional
 
 from telegram import Chat
-from telegram.ext import CallbackContext, Dispatcher, Handler
+from telegram.ext import CallbackContext, Application, BaseHandler, ConversationHandler
 
 from .state import State
 
 if TYPE_CHECKING:
     from telegram import Update
 
 
-class StateHandler(Handler):
+class StateHandler(BaseHandler):
     BACK = '_back'
 
     def __init__(
-        self, entry_point: Handler, states: List[State], allow_reentry: bool = True
+        self, entry_point: BaseHandler, states: List[State], allow_reentry: bool = True
     ):
         super().__init__(...)
         self.entry_point = entry_point
         self.states = self._states_to_mapping(states)
         self.users_states = defaultdict(list)
         self.allow_reentry = allow_reentry
 
@@ -43,63 +43,63 @@
 
         if not user_state or (self.allow_reentry and entry_check_result):
             return entry_check_result
 
         else:
             return True
 
-    def handle_update(
+    async def handle_update(
         self,
         update: 'Update',
-        dispatcher: 'Dispatcher',
+        application: 'Application',
         check_result: Any,
         context: Optional['CallbackContext'] = None,
     ):
         user_id, user_state = self._get_current_user_state(update)
 
         reentry = self.allow_reentry and self.entry_point.check_update(update)
 
         if reentry or not user_state:
-            new_state_key = self.entry_point.handle_update(
-                update, dispatcher, check_result, context
+            new_state_key = await self.entry_point.handle_update(
+                update, application, check_result, context
             )
             self.__clear_user_states(user_id)
 
         else:
-            new_state_key = user_state.handle(update, dispatcher, context)
+            new_state_key = await user_state.handle(update, application, context)
 
         if new_state_key:
-            self.activate_state(user_id, new_state_key, update, context)
+            await self.activate_state(user_id, new_state_key, update, context)
 
     def _get_current_user_state(self, update: 'Update'):
         user = update.effective_user
         user_states = self.__get_user_states(user.id)
 
         if user_states:
             user_state_key = user_states[-1]
             user_state = self.states.get(user_state_key, None)
 
             return user.id, user_state
 
         return user.id, None
 
-    def activate_state(
+    async def activate_state(
         self, user_id: int, state_key: str, update: 'Update', context: 'CallbackContext'
     ):
         if state_key == self.BACK:
             self.__pop_user_state(user_id)
             state_key = self.__pop_user_state(user_id)
 
         state = self.states.get(state_key, None)
 
         if state:
-            result_state_key = state.activate(update, context)
+            result_state_key = await state.activate(update, context)
 
             if result_state_key:
-                self.activate_state(user_id, result_state_key, update, context)
+                await self.activate_state(user_id, result_state_key, update, context)
 
             else:
                 self.__set_user_state(user_id, state_key)
 
     def __set_user_state(self, user_id: int, state: str):
         self.users_states[user_id].append(state)
```

### Comparing `ptb-state-handler-0.1.0/PKG-INFO` & `ptb_state_handler-0.2.0/PKG-INFO`

 * *Files 19% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: ptb-state-handler
-Version: 0.1.0
+Version: 0.2.0
 Summary: State handler for python-telegram-bot library
 License: Apache-2.0
 Author: Vlad Pastushenko
 Author-email: iam@vladpi.me
-Requires-Python: >=3.6,<4.0
+Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.6
-Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
-Requires-Dist: python-dotenv (>=0.14.0,<0.15.0)
-Requires-Dist: python-telegram-bot (>=12.0)
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Requires-Dist: python-dotenv (>=1.0.0,<2.0.0)
+Requires-Dist: python-telegram-bot (>=20.0,<21.0)
```

