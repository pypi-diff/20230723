# Comparing `tmp/nmfu-0.5.1.tar.gz` & `tmp/nmfu-0.5.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nmfu-0.5.1.tar", last modified: Mon Apr  3 03:28:30 2023, max compression
+gzip compressed data, was "nmfu-0.5.2.tar", last modified: Sun Jul 23 05:20:36 2023, max compression
```

## Comparing `nmfu-0.5.1.tar` & `nmfu-0.5.2.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0     1001     1001        0 2023-04-03 03:28:30.490012 nmfu-0.5.1/
--rw-rw-r--   0     1001     1001    35150 2023-04-03 03:28:20.000000 nmfu-0.5.1/LICENSE
--rw-r--r--   0     1001     1001     3209 2023-04-03 03:28:30.490012 nmfu-0.5.1/PKG-INFO
--rw-rw-r--   0     1001     1001     1884 2023-04-03 03:28:20.000000 nmfu-0.5.1/README.md
-drwxr-xr-x   0     1001     1001        0 2023-04-03 03:28:30.490012 nmfu-0.5.1/nmfu.egg-info/
--rw-r--r--   0     1001     1001     3209 2023-04-03 03:28:30.000000 nmfu-0.5.1/nmfu.egg-info/PKG-INFO
--rw-r--r--   0     1001     1001      219 2023-04-03 03:28:30.000000 nmfu-0.5.1/nmfu.egg-info/SOURCES.txt
--rw-r--r--   0     1001     1001        1 2023-04-03 03:28:30.000000 nmfu-0.5.1/nmfu.egg-info/dependency_links.txt
--rw-r--r--   0     1001     1001       36 2023-04-03 03:28:30.000000 nmfu-0.5.1/nmfu.egg-info/entry_points.txt
--rw-r--r--   0     1001     1001       86 2023-04-03 03:28:30.000000 nmfu-0.5.1/nmfu.egg-info/requires.txt
--rw-r--r--   0     1001     1001        5 2023-04-03 03:28:30.000000 nmfu-0.5.1/nmfu.egg-info/top_level.txt
--rw-rw-r--   0     1001     1001   266828 2023-04-03 03:28:20.000000 nmfu-0.5.1/nmfu.py
--rw-rw-r--   0     1001     1001      100 2023-04-03 03:28:20.000000 nmfu-0.5.1/pyproject.toml
--rw-r--r--   0     1001     1001       41 2023-04-03 03:28:30.490012 nmfu-0.5.1/setup.cfg
--rw-rw-r--   0     1001     1001     1857 2023-04-03 03:28:20.000000 nmfu-0.5.1/setup.py
+drwxr-xr-x   0     1001     1001        0 2023-07-23 05:20:36.737058 nmfu-0.5.2/
+-rw-rw-r--   0     1001     1001    35150 2023-07-23 05:20:27.000000 nmfu-0.5.2/LICENSE
+-rw-r--r--   0     1001     1001     3209 2023-07-23 05:20:36.737058 nmfu-0.5.2/PKG-INFO
+-rw-rw-r--   0     1001     1001     1884 2023-07-23 05:20:27.000000 nmfu-0.5.2/README.md
+drwxr-xr-x   0     1001     1001        0 2023-07-23 05:20:36.737058 nmfu-0.5.2/nmfu.egg-info/
+-rw-r--r--   0     1001     1001     3209 2023-07-23 05:20:36.000000 nmfu-0.5.2/nmfu.egg-info/PKG-INFO
+-rw-r--r--   0     1001     1001      219 2023-07-23 05:20:36.000000 nmfu-0.5.2/nmfu.egg-info/SOURCES.txt
+-rw-r--r--   0     1001     1001        1 2023-07-23 05:20:36.000000 nmfu-0.5.2/nmfu.egg-info/dependency_links.txt
+-rw-r--r--   0     1001     1001       36 2023-07-23 05:20:36.000000 nmfu-0.5.2/nmfu.egg-info/entry_points.txt
+-rw-r--r--   0     1001     1001       86 2023-07-23 05:20:36.000000 nmfu-0.5.2/nmfu.egg-info/requires.txt
+-rw-r--r--   0     1001     1001        5 2023-07-23 05:20:36.000000 nmfu-0.5.2/nmfu.egg-info/top_level.txt
+-rw-rw-r--   0     1001     1001   266721 2023-07-23 05:20:27.000000 nmfu-0.5.2/nmfu.py
+-rw-rw-r--   0     1001     1001      100 2023-07-23 05:20:27.000000 nmfu-0.5.2/pyproject.toml
+-rw-r--r--   0     1001     1001       41 2023-07-23 05:20:36.737058 nmfu-0.5.2/setup.cfg
+-rw-rw-r--   0     1001     1001     1857 2023-07-23 05:20:27.000000 nmfu-0.5.2/setup.py
```

### Comparing `nmfu-0.5.1/LICENSE` & `nmfu-0.5.2/LICENSE`

 * *Files identical despite different names*

### Comparing `nmfu-0.5.1/PKG-INFO` & `nmfu-0.5.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nmfu
-Version: 0.5.1
+Version: 0.5.2
 Summary: A parser generator that turns procedural programs into C state machines
 Home-page: https://github.com/mincrmatt12/nmfu
 Author: Matthew Mirvish
 Author-email: matthew@mm12.xyz
 License: GPLv3
 Project-URL: Bug Tracker, https://github.com/mincrmatt12/nmfu/issues
 Project-URL: Source Code, https://github.com/mincrmatt12/nmfu
```

### Comparing `nmfu-0.5.1/README.md` & `nmfu-0.5.2/README.md`

 * *Files identical despite different names*

### Comparing `nmfu-0.5.1/nmfu.egg-info/PKG-INFO` & `nmfu-0.5.2/nmfu.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nmfu
-Version: 0.5.1
+Version: 0.5.2
 Summary: A parser generator that turns procedural programs into C state machines
 Home-page: https://github.com/mincrmatt12/nmfu
 Author: Matthew Mirvish
 Author-email: matthew@mm12.xyz
 License: GPLv3
 Project-URL: Bug Tracker, https://github.com/mincrmatt12/nmfu/issues
 Project-URL: Source Code, https://github.com/mincrmatt12/nmfu
```

### Comparing `nmfu-0.5.1/nmfu.py` & `nmfu-0.5.2/nmfu.py`

 * *Files 0% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 
 This program is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
 GNU General Public License for more details.
 """
 
-__version__ = "0.5.1"
+__version__ = "0.5.2"
 
 import abc
 import enum
 import string
 import itertools
 import queue
 import io
@@ -837,22 +837,18 @@
         if isinstance(chained_dfa.starting_state, DFProxyState):
             # Add an extra state that will represent the condition point properly (see docs for equivalent_on_values)
             valid, to_else = chained_dfa.starting_state.equivalent_on_values()
             if valid and to_else:
                 fake_start = DFState()
                 chained_dfa.add(fake_start)
 
-                # Tie them separately; note this will cause things to go wrong in certain cases
-                # with conditionals; but we generally don't deal with those
-                if valid:
-                    fake_start[valid] = chained_dfa.starting_state
-                    fake_start[valid].fallthrough(True)
-                if to_else:
-                    fake_start[to_else] = chained_dfa.starting_state
-                    fake_start[to_else].fallthrough(True).handles_else()
+                fake_start[valid] = chained_dfa.starting_state
+                fake_start[valid].fallthrough(True)
+                fake_start[to_else] = chained_dfa.starting_state
+                fake_start[to_else].fallthrough(True).handles_else()
                 chained_dfa.starting_state = fake_start
 
         # Check for ambiguity: if any transitions added to a sub_state try to redirect a valid character a different valid
         # state, there is ambiguity. In other words, we only want to add transitions that would previously lead to the error state.
 
         chained_transitions = [x for x in chained_dfa.starting_state.transitions if DFTransition.Else in x.on_values]
         chained_transitions.extend(x for x in chained_dfa.starting_state.transitions if DFTransition.Else not in x.on_values)
@@ -4255,14 +4251,15 @@
                     "macro_int_expr_arg": MacroArgumentKind.INTEXPR,
                     "macro_hook_arg": MacroArgumentKind.HOOK,
                     "macro_breaktgt_arg": MacroArgumentKind.LOOP,
                 }[i.data]
             if name in defined:
                 raise DuplicateDefinitionError("macro argument", i, name)
             parsed_args.append(MacroArgument(name, kind))
+            defined.add(name)
         return parsed_args
 
     def _convert_char_const(self, char_const: str):
         if len(char_const) == 3:
             return char_const[1]
         else:
             return {
@@ -5365,31 +5362,34 @@
         result = ""
         if type(value) is str:
             bytes_value = value.encode('utf-8')
         else:
             bytes_value = value
         for i in bytes_value:
             if chr(i) in ["\\", '"']:
-                result += "\\" + i
+                result += "\\" + chr(i)
             elif not (32 <= i < 127):
                 result += "\\x{:02x}".format(i)
             else:
                 result += chr(i)
         return result
 
-    def _generate_set_string(self, value: Union[str], into: OutputStorage):
+    def _generate_set_string(self, value: Union[bytes, str], into: OutputStorage):
         """
         Generate code that sets value into into
 
         : strncpy(state->c.into, "value", into.str_size)
 
         Must ensure value is short enough first.
         """
 
-        escaped_length = len(value.encode('utf-8'))
+        if isinstance(value, str):
+            escaped_length = len(value.encode('utf-8'))
+        else:
+            escaped_length = len(value)
 
         return f"memcpy(state->c.{into.name}, \"{self._escape_string(value)}\", {escaped_length if not into.str_null else escaped_length+1});"
 
     def _generate_action_implementation(self, action: Action, is_start: bool = False, is_end: bool = False, transition=None):
         result = Outputter()
         ctx = IntegerExprUseContext.ASSIGN_ON_MATCH
         if is_start:
```

### Comparing `nmfu-0.5.1/setup.py` & `nmfu-0.5.2/setup.py`

 * *Files identical despite different names*

