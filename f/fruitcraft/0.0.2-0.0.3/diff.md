# Comparing `tmp/fruitcraft-0.0.2.tar.gz` & `tmp/fruitcraft-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fruitcraft-0.0.2.tar", max compression
+gzip compressed data, was "fruitcraft-0.0.3.tar", max compression
```

## Comparing `fruitcraft-0.0.2.tar` & `fruitcraft-0.0.3.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     1068 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/LICENSE
--rw-r--r--   0        0        0      128 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/README.md
--rw-r--r--   0        0        0       99 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/fruitcraft/__init__.py
--rw-r--r--   0        0        0    12326 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/fruitcraft/client.py
--rw-r--r--   0        0        0    21900 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/fruitcraft/f_types/__init__.py
--rw-r--r--   0        0        0      727 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/fruitcraft/f_types/errors.py
--rw-r--r--   0        0        0     3985 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/fruitcraft/f_types/utils.py
--rw-r--r--   0        0        0      809 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/pyproject.toml
--rw-r--r--   0        0        0     1026 1970-01-01 00:00:00.000000 fruitcraft-0.0.2/PKG-INFO
+-rw-r--r--   0        0        0     1068 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/LICENSE
+-rw-r--r--   0        0        0      128 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/README.md
+-rw-r--r--   0        0        0       99 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/fruitcraft/__init__.py
+-rw-r--r--   0        0        0    13181 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/fruitcraft/client.py
+-rw-r--r--   0        0        0    22685 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/fruitcraft/f_types/__init__.py
+-rw-r--r--   0        0        0      727 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/fruitcraft/f_types/errors.py
+-rw-r--r--   0        0        0     3985 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/fruitcraft/f_types/utils.py
+-rw-r--r--   0        0        0      809 2023-07-22 22:38:13.597217 fruitcraft-0.0.3/pyproject.toml
+-rw-r--r--   0        0        0     1026 1970-01-01 00:00:00.000000 fruitcraft-0.0.3/PKG-INFO
```

### Comparing `fruitcraft-0.0.2/LICENSE` & `fruitcraft-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `fruitcraft-0.0.2/fruitcraft/client.py` & `fruitcraft-0.0.3/fruitcraft/client.py`

 * *Files 4% similar despite different names*

```diff
@@ -120,14 +120,31 @@
         
         self.mut = asyncio.Lock()
         self.http_client = httpx.AsyncClient()
         self.passport = passport
         if not self.logger:
             self.logger = logging.getLogger(__name__)
     
+    async def get_error_messages(self) -> ErrorMessages:
+        return await self.get_device_constants_with_options(ErrorMessagesRequest())
+    
+    async def get_error_messages_with_options(self, opt: ErrorMessagesRequest) -> ErrorMessages:
+        opt.set_default_values()
+        
+        api_response: APIResponse = await self.send_and_parse("device/constants", opt, ErrorMessages)
+        return api_response.data
+    
+    async def get_device_constants(self) -> DeviceConstants:
+        return await self.get_device_constants_with_options(DeviceConstantsRequest())
+    
+    async def get_device_constants_with_options(self, opt: DeviceConstantsRequest) -> DeviceConstants:
+        opt.set_default_values()
+        api_response: APIResponse = await self.send_and_parse("device/constants", opt, DeviceConstants)
+        return api_response.data
+    
     async def do_quest(self, cards: CardsSelection) -> QuestResponse:
         return await self.do_quest_with_options(
             QuestRequest(
                 cards=new_int_array(cards.cards),
                 _cards_selection=cards,
                 hero_id=cards.hero_id,
             )
```

### Comparing `fruitcraft-0.0.2/fruitcraft/f_types/__init__.py` & `fruitcraft-0.0.3/fruitcraft/f_types/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,14 +5,27 @@
 )
 
 class IntArray(str):
     pass
 
 LeagueWinnerRanges = Dict[str, int]
 
+class LoadRequestDefaults:
+	DEFAULT_GAME_VERSION      = "1.9.10691"
+	DEFAULT_U_DID             = "a341224a6fa458c8"
+	DEFAULT_OS_TYPE           = 2
+	DEFAULT_OS_VERSION        = "7.1.2"
+	DEFAULT_PHONE_MODEL       = "google pixel 2"
+	DEFAULT_METRIX_UID        = "-"
+	DEFAULT_APPS_FLYER_UID     = "1686402669312-333768616178664406"
+	DEFAULT_DEVICE_NAME       = "unknown"
+	DEFAULT_CONSTANTS_VERSION = "142"
+	DEFAULT_STORE_TYPE        = "myket"
+	DEFAULT_CLIENT_VALUE      = "iOS"
+	DEFAULT_LANG_VALUE        = "fa-IR"
 
 def new_int_array(values: List[Any]) -> IntArray:
     output = "["
     for i, current in enumerate(values):
         output += str(current)
 
         if i != len(values)-1:
@@ -352,39 +365,43 @@
     latest_app_version_for_notice: Optional[str] = ""
     latest_constants_version: Optional[str] = ""
     modules_version: ModulesVersion = None
     emergency_message: Optional[str] = ""
     update_message: Optional[str] = ""
     
 
-PlayerMedals = Dict[str, int]
-ErrorMessages = Dict[str, str]
-DeviceConstants = Dict[str, Any]
-FruitExportContainer = Dict[str, FruitCardInfo]
+PlayerMedals: Dict[str, int] = dict
+ErrorMessages: Dict[str, str] = dict
+DeviceConstants: Dict[str, Any] = dict
+FruitExportContainer: Dict[str, FruitCardInfo] = dict
+
 
 
 class DeviceConstantsRequest(DScaffold):
     game_version: Optional[str] = ""
     os_version: Optional[str] = ""
-    phone_model: Optional[str] = ""
+    model: Optional[str] = ""
     constant_version: Optional[str] = ""
     store_type: Optional[str] = ""
-
-class LoadRequestDefaults:
-	DEFAULT_GAME_VERSION      = "1.9.10691"
-	DEFAULT_U_DID             = "a341224a6fa458c8"
-	DEFAULT_OS_TYPE           = 2
-	DEFAULT_OS_VERSION        = "7.1.2"
-	DEFAULT_PHONE_MODEL       = "google pixel 2"
-	DEFAULT_METRIX_UID        = "-"
-	DEFAULT_APPS_FLYER_UID     = "1686402669312-333768616178664406"
-	DEFAULT_DEVICE_NAME       = "unknown"
-	DEFAULT_CONSTANTS_VERSION = "142"
-	DEFAULT_STORE_TYPE        = "myket"
-	DEFAULT_CLIENT_VALUE      = "iOS"
+    
+    def set_default_values(self):
+        if not self.game_version:
+            self.game_version = LoadRequestDefaults.DEFAULT_GAME_VERSION
+        
+        if not self.os_version:
+            self.os_version = LoadRequestDefaults.DEFAULT_OS_VERSION
+        
+        if not self.model:
+            self.model = LoadRequestDefaults.DEFAULT_PHONE_MODEL
+        
+        if not self.constant_version:
+            self.constant_version = LoadRequestDefaults.DEFAULT_CONSTANTS_VERSION
+        
+        if not self.store_type:
+            self.store_type = LoadRequestDefaults.DEFAULT_STORE_TYPE
 
 
 class PlayerLoadRequest(DScaffold):
     game_version: Optional[str] = ""
     udid: Optional[str] = ""
     os_type: Optional[int] = 0
     restore_key: Optional[str] = ""
@@ -436,14 +453,18 @@
     client: Optional[str] = ""
 
 class LanguagePatchRequest(DScaffold):
     client: Optional[str] = ""
 
 class ErrorMessagesRequest(DScaffold):
     lang_id: Optional[str] = ""
+    
+    def set_default_values(self):
+        if not self.lang_id:
+            self.lang_id = LoadRequestDefaults.DEFAULT_LANG_VALUE
 
 class CardsSelection():
     cards: List[int] = None
     hero_id: int = 0
     
     # NoHeal indicates we shouldn't be trying to heal any of
     # the cards. This means we are 100% sure that they have already
```

### Comparing `fruitcraft-0.0.2/fruitcraft/f_types/errors.py` & `fruitcraft-0.0.3/fruitcraft/f_types/errors.py`

 * *Files identical despite different names*

### Comparing `fruitcraft-0.0.2/fruitcraft/f_types/utils.py` & `fruitcraft-0.0.3/fruitcraft/f_types/utils.py`

 * *Files identical despite different names*

### Comparing `fruitcraft-0.0.2/pyproject.toml` & `fruitcraft-0.0.3/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "fruitcraft"
-version = "0.0.2"
+version = "0.0.3"
 description = "Full Python Wrapper for fruitcraft game API. By Mr.AW ."
 authors = ["Mr. AW <mrawfruitly@gmail.com>"]
 packages = [
     { include = "fruitcraft" }
 ]
 classifiers = [
     "Programming Language :: Python :: 3",
```

### Comparing `fruitcraft-0.0.2/PKG-INFO` & `fruitcraft-0.0.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fruitcraft
-Version: 0.0.2
+Version: 0.0.3
 Summary: Full Python Wrapper for fruitcraft game API. By Mr.AW .
 Home-page: https://github.com/MrAwFruitly/FruitcraftClient-py
 Keywords: fruit,fruitcraft,fruit-craft,game-library
 Author: Mr. AW
 Author-email: mrawfruitly@gmail.com
 Requires-Python: >=3.7,<4.0
 Classifier: License :: OSI Approved :: MIT License
```

