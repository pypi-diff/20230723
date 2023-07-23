# Comparing `tmp/fruitcraft-0.0.3.tar.gz` & `tmp/fruitcraft-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fruitcraft-0.0.3.tar", max compression
+gzip compressed data, was "fruitcraft-0.0.4.tar", max compression
```

## Comparing `fruitcraft-0.0.3.tar` & `fruitcraft-0.0.4.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     1068 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/LICENSE
--rw-r--r--   0        0        0      128 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/README.md
--rw-r--r--   0        0        0       99 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/fruitcraft/__init__.py
--rw-r--r--   0        0        0    13181 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/fruitcraft/client.py
--rw-r--r--   0        0        0    22685 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/fruitcraft/f_types/__init__.py
--rw-r--r--   0        0        0      727 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/fruitcraft/f_types/errors.py
--rw-r--r--   0        0        0     3985 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/fruitcraft/f_types/utils.py
--rw-r--r--   0        0        0      809 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/pyproject.toml
--rw-r--r--   0        0        0     1026 1970-01-01 00:00:00.000000 fruitcraft-0.0.3/PKG-INFO
+-rw-r--r--   0        0        0     1068 2023-07-22 22:57:17.607171 fruitcraft-0.0.4/LICENSE
+-rw-r--r--   0        0        0      128 2023-07-22 22:57:17.607171 fruitcraft-0.0.4/README.md
+-rw-r--r--   0        0        0       99 2023-07-22 22:57:17.607171 fruitcraft-0.0.4/fruitcraft/__init__.py
+-rw-r--r--   0        0        0    13246 2023-07-22 22:57:17.607171 fruitcraft-0.0.4/fruitcraft/client.py
+-rw-r--r--   0        0        0    22775 2023-07-22 22:57:17.607171 fruitcraft-0.0.4/fruitcraft/f_types/__init__.py
+-rw-r--r--   0        0        0      727 2023-07-22 22:57:17.607171 fruitcraft-0.0.4/fruitcraft/f_types/errors.py
+-rw-r--r--   0        0        0     3985 2023-07-22 22:57:17.607171 fruitcraft-0.0.4/fruitcraft/f_types/utils.py
+-rw-r--r--   0        0        0      809 2023-07-22 22:57:17.607171 fruitcraft-0.0.4/pyproject.toml
+-rw-r--r--   0        0        0     1026 1970-01-01 00:00:00.000000 fruitcraft-0.0.4/PKG-INFO
```

### Comparing `fruitcraft-0.0.3/LICENSE` & `fruitcraft-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `fruitcraft-0.0.3/fruitcraft/client.py` & `fruitcraft-0.0.4/fruitcraft/client.py`

 * *Files 2% similar despite different names*

```diff
@@ -164,14 +164,16 @@
             self.mut.release()
             raise e
     
     async def __do_quest_with_options(self, opt: QuestRequest) -> QuestResponse:
         if self.last_q_value:
             opt.check = hash_q_string(self.last_q_value)
         
+        opt._cards_selection
+        
         api_response: APIResponse = await self.send_and_parse("battle/quest", opt, QuestResponse)
         if isinstance(api_response.data, QuestResponse):
             if api_response.data.q:
                 self.last_q_value = str(api_response.data.q)
             
             return api_response.data
     
@@ -189,38 +191,39 @@
         return CardsSelection(
             cards=cards,
             hero_id=hero_id,
         )
     
     
     def get_level1_card(self) -> CardsSelection:
-        final_cards: AttackCardInfo = None
+        final_card: AttackCardInfo = None
         final_since: int = 0
         
         for current in self.last_loaded_player.cards:
             if current.power > 40:
                 continue
             
             my_since = time.time() - current.internal_last_time_used
             if my_since < 16:
                 continue
             
-            if not final_cards:
-                final_cards = current
+            if not final_card:
+                final_card = current
                 continue
             
             if my_since > final_since:
-                final_cards = current
+                final_card = current
                 final_since = my_since
         
-        if not final_cards:
+        if not final_card:
             return None
         
+        final_card.set_as_used()
         return CardsSelection(
-            cards=[final_cards.id],
+            cards=[final_card.id],
             no_heal=True,
         )
         
     
     def get_weakest_card(self) -> CardsSelection:
         if not self.last_loaded_player:
             raise Exception("No player loaded")
```

### Comparing `fruitcraft-0.0.3/fruitcraft/f_types/__init__.py` & `fruitcraft-0.0.4/fruitcraft/f_types/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 from pydantic import BaseModel
 from .utils import xor_encrypt
 from typing import (
     Any, List, Dict, Optional
 )
+import time
 
 class IntArray(str):
     pass
 
 LeagueWinnerRanges = Dict[str, int]
 
 class LoadRequestDefaults:
@@ -76,14 +77,16 @@
     id: Optional[int] = 0
     last_used_at: Optional[int] = 0
     power: Optional[int] = 0
     base_card_id: Optional[int] = 0
     player_id: Optional[int] = 0
     internal_last_time_used: Optional[int] = 0
 
+    def set_as_used(self):
+        self.internal_last_time_used = time.time()
 
 
 class QuestResponse(DScaffold):
     code: Optional[int] = 0
     arguments: Optional[List[Any]] = []
     outcome: Optional[bool] = False
     boss_mode: Optional[bool] = False
```

### Comparing `fruitcraft-0.0.3/fruitcraft/f_types/errors.py` & `fruitcraft-0.0.4/fruitcraft/f_types/errors.py`

 * *Files identical despite different names*

### Comparing `fruitcraft-0.0.3/fruitcraft/f_types/utils.py` & `fruitcraft-0.0.4/fruitcraft/f_types/utils.py`

 * *Files identical despite different names*

### Comparing `fruitcraft-0.0.3/pyproject.toml` & `fruitcraft-0.0.4/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "fruitcraft"
-version = "0.0.3"
+version = "0.0.4"
 description = "Full Python Wrapper for fruitcraft game API. By Mr.AW ."
 authors = ["Mr. AW <mrawfruitly@gmail.com>"]
 packages = [
     { include = "fruitcraft" }
 ]
 classifiers = [
     "Programming Language :: Python :: 3",
```

### Comparing `fruitcraft-0.0.3/PKG-INFO` & `fruitcraft-0.0.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fruitcraft
-Version: 0.0.3
+Version: 0.0.4
 Summary: Full Python Wrapper for fruitcraft game API. By Mr.AW .
 Home-page: https://github.com/MrAwFruitly/FruitcraftClient-py
 Keywords: fruit,fruitcraft,fruit-craft,game-library
 Author: Mr. AW
 Author-email: mrawfruitly@gmail.com
 Requires-Python: >=3.7,<4.0
 Classifier: License :: OSI Approved :: MIT License
```

