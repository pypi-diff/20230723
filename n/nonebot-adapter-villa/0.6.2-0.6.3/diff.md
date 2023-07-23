# Comparing `tmp/nonebot_adapter_villa-0.6.2.tar.gz` & `tmp/nonebot_adapter_villa-0.6.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_adapter_villa-0.6.2.tar", max compression
+gzip compressed data, was "nonebot_adapter_villa-0.6.3.tar", max compression
```

## Comparing `nonebot_adapter_villa-0.6.2.tar` & `nonebot_adapter_villa-0.6.3.tar`

### file list

```diff
@@ -1,19 +1,19 @@
--rw-r--r--   0        0        0     1062 2023-07-21 07:37:21.910586 nonebot_adapter_villa-0.6.2/LICENSE
--rw-r--r--   0        0        0     7323 2023-07-21 07:37:21.910586 nonebot_adapter_villa-0.6.2/README.md
--rw-r--r--   0        0        0      228 2023-07-21 07:37:21.910586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/__init__.py
--rw-r--r--   0        0        0    12154 2023-07-21 07:37:21.910586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/adapter.py
--rw-r--r--   0        0        0      114 2023-07-21 07:37:21.910586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/api/__init__.py
--rw-r--r--   0        0        0       25 2023-07-21 07:37:21.910586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/api/client.py
--rw-r--r--   0        0        0     3293 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/api/client.pyi
--rw-r--r--   0        0        0    13152 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/api/handle.py
--rw-r--r--   0        0        0     9534 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/api/models.py
--rw-r--r--   0        0        0     1734 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/api/request.py
--rw-r--r--   0        0        0    14467 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/bot.py
--rw-r--r--   0        0        0     1190 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/config.py
--rw-r--r--   0        0        0    12798 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/event.py
--rw-r--r--   0        0        0     2717 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/exception.py
--rw-r--r--   0        0        0     9952 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/message.py
--rw-r--r--   0        0        0     1449 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/permission.py
--rw-r--r--   0        0        0       76 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/utils.py
--rw-r--r--   0        0        0     2125 2023-07-21 07:37:21.914586 nonebot_adapter_villa-0.6.2/pyproject.toml
--rw-r--r--   0        0        0     8249 1970-01-01 00:00:00.000000 nonebot_adapter_villa-0.6.2/PKG-INFO
+-rw-r--r--   0        0        0     1062 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/LICENSE
+-rw-r--r--   0        0        0     7323 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/README.md
+-rw-r--r--   0        0        0      228 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/__init__.py
+-rw-r--r--   0        0        0    12302 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/adapter.py
+-rw-r--r--   0        0        0      114 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/api/__init__.py
+-rw-r--r--   0        0        0       25 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/api/client.py
+-rw-r--r--   0        0        0     3293 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/api/client.pyi
+-rw-r--r--   0        0        0    13152 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/api/handle.py
+-rw-r--r--   0        0        0     9534 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/api/models.py
+-rw-r--r--   0        0        0     1734 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/api/request.py
+-rw-r--r--   0        0        0    14504 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/bot.py
+-rw-r--r--   0        0        0     1190 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/config.py
+-rw-r--r--   0        0        0    12798 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/event.py
+-rw-r--r--   0        0        0     2717 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/exception.py
+-rw-r--r--   0        0        0     9952 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/message.py
+-rw-r--r--   0        0        0     1449 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/permission.py
+-rw-r--r--   0        0        0       76 2023-07-23 07:05:16.999946 nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/utils.py
+-rw-r--r--   0        0        0     2125 2023-07-23 07:05:17.003946 nonebot_adapter_villa-0.6.3/pyproject.toml
+-rw-r--r--   0        0        0     8249 1970-01-01 00:00:00.000000 nonebot_adapter_villa-0.6.3/PKG-INFO
```

### Comparing `nonebot_adapter_villa-0.6.2/LICENSE` & `nonebot_adapter_villa-0.6.3/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_adapter_villa-0.6.2/README.md` & `nonebot_adapter_villa-0.6.3/README.md`

 * *Files identical despite different names*

### Comparing `nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/adapter.py` & `nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/adapter.py`

 * *Files 1% similar despite different names*

```diff
@@ -55,15 +55,15 @@
         self.driver.on_startup(self._forward_http)
         self.driver.on_startup(self._start_forward)
         self.driver.on_shutdown(self._stop_forward)
 
     async def _forward_http(self):
         for bot_info in self.villa_config.villa_bots:
             if bot_info.callback_url:
-                bot = Bot(self, bot_info)
+                bot = Bot(self, bot_info.bot_id, bot_info)
                 self.bot_connect(bot)
                 log("INFO", f"<y>Bot {bot.self_id} connected</y>")
                 http_setup = HTTPServerSetup(
                     URL(bot_info.callback_url),
                     "POST",
                     f"大别野 {bot_info.bot_id} HTTP",
                     self._handle_http,
@@ -86,14 +86,15 @@
                                     if bot.bot_id == bot_id
                                 ),
                                 None,
                             )
                         ) is not None:
                             bot = Bot(
                                 self,
+                                bot_info.bot_id,
                                 bot_info,
                             )
                             self.bot_connect(bot)
                             log("INFO", f"<y>Bot {bot.self_id} connected</y>")
                         else:
                             log(
                                 "WARNING",
@@ -133,15 +134,15 @@
                 )
             return Response(415, content="Invalid Request Body")
         return Response(415, content="Invalid Request Body")
 
     async def _start_forward(self) -> None:
         for bot_info in self.villa_config.villa_bots:
             if bot_info.ws_url:
-                bot = Bot(self, bot_info)
+                bot = Bot(self, bot_info.bot_id, bot_info)
                 self.bot_connect(bot)
                 log("INFO", f"<y>Bot {bot.self_id} connected</y>")
                 self.tasks.append(
                     asyncio.create_task(
                         self._forward_ws(URL(bot_info.ws_url), bot_info.ws_secret),
                     ),
                 )
@@ -179,14 +180,15 @@
                                                     if bot.bot_id == bot_id
                                                 ),
                                                 None,
                                             )
                                         ) is not None:
                                             bot = Bot(
                                                 self,
+                                                bot_info.bot_id,
                                                 bot_info,
                                             )
                                             self.bot_connect(bot)
                                             log(
                                                 "INFO",
                                                 f"<y>Bot {bot.self_id} connected</y>",
                                             )
```

### Comparing `nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/api/client.pyi` & `nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/api/client.pyi`

 * *Files identical despite different names*

### Comparing `nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/api/handle.py` & `nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/api/handle.py`

 * *Files identical despite different names*

### Comparing `nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/api/models.py` & `nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/api/models.py`

 * *Files identical despite different names*

### Comparing `nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/api/request.py` & `nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/api/request.py`

 * *Files identical despite different names*

### Comparing `nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/bot.py` & `nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/bot.py`

 * *Files 2% similar despite different names*

```diff
@@ -112,17 +112,19 @@
     大别野协议 Bot 适配。
     """
 
     @override
     def __init__(
         self,
         adapter: "Adapter",
+        self_id: str,
         bot_info: BotInfo,
+        **kwargs: Any,
     ) -> None:
-        super().__init__(adapter, bot_info.bot_id)
+        super().__init__(adapter, self_id)
         self.adapter: Adapter = adapter
         self.bot_secret: str = bot_info.bot_secret
         self.bot_secret_encrypt = hmac.new(
             bot_info.pub_key.encode(),
             bot_info.bot_secret.encode(),
             hashlib.sha256,
         ).hexdigest()
```

### Comparing `nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/config.py` & `nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/config.py`

 * *Files identical despite different names*

### Comparing `nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/event.py` & `nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/event.py`

 * *Files identical despite different names*

### Comparing `nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/exception.py` & `nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/exception.py`

 * *Files identical despite different names*

### Comparing `nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/message.py` & `nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/message.py`

 * *Files identical despite different names*

### Comparing `nonebot_adapter_villa-0.6.2/nonebot/adapters/villa/permission.py` & `nonebot_adapter_villa-0.6.3/nonebot/adapters/villa/permission.py`

 * *Files identical despite different names*

### Comparing `nonebot_adapter_villa-0.6.2/pyproject.toml` & `nonebot_adapter_villa-0.6.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "nonebot-adapter-villa"
-version = "0.6.2"
+version = "0.6.3"
 description = "NoneBot2米游社大别野Bot适配器。MiHoYo Villa Bot adapter for nonebot2."
 authors = ["CMHopeSunshine <277073121@qq.com>"]
 license = "MIT"
 readme = "README.md"
 homepage = "https://github.com/CMHopeSunshine/nonebot-adapter-villa"
 repository = "https://github.com/CMHopeSunshine/nonebot-adapter-villa"
 documentation = "https://github.com/CMHopeSunshine/nonebot-adapter-villa"
```

### Comparing `nonebot_adapter_villa-0.6.2/PKG-INFO` & `nonebot_adapter_villa-0.6.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nonebot-adapter-villa
-Version: 0.6.2
+Version: 0.6.3
 Summary: NoneBot2米游社大别野Bot适配器。MiHoYo Villa Bot adapter for nonebot2.
 Home-page: https://github.com/CMHopeSunshine/nonebot-adapter-villa
 License: MIT
 Keywords: nonebot,mihoyo,bot
 Author: CMHopeSunshine
 Author-email: 277073121@qq.com
 Requires-Python: >=3.8,<4.0
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: nonebot-adapter-villa Version: 0.6.2 Summary:
+Metadata-Version: 2.1 Name: nonebot-adapter-villa Version: 0.6.3 Summary:
 NoneBot2ç±³æ¸¸ç¤¾å¤§å«éBotééå¨ãMiHoYo Villa Bot adapter for nonebot2.
 Home-page: https://github.com/CMHopeSunshine/nonebot-adapter-villa License: MIT
 Keywords: nonebot,mihoyo,bot Author: CMHopeSunshine Author-email:
 277073121@qq.com Requires-Python: >=3.8,<4.0 Classifier: License :: OSI
 Approved :: MIT License Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8 Classifier: Programming
 Language :: Python :: 3.9 Classifier: Programming Language :: Python :: 3.10
```

