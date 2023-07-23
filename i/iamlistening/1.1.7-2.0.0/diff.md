# Comparing `tmp/iamlistening-1.1.7.tar.gz` & `tmp/iamlistening-2.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "iamlistening-1.1.7.tar", max compression
+gzip compressed data, was "iamlistening-2.0.0.tar", max compression
```

## Comparing `iamlistening-1.1.7.tar` & `iamlistening-2.0.0.tar`

### file list

```diff
@@ -1,8 +1,13 @@
--rw-r--r--   0        0        0     1064 2023-07-20 14:53:29.280232 iamlistening-1.1.7/LICENSE
--rw-r--r--   0        0        0     2910 2023-07-20 14:53:29.280232 iamlistening-1.1.7/README.md
--rw-r--r--   0        0        0       99 2023-07-20 14:53:31.052356 iamlistening-1.1.7/iamlistening/__init__.py
--rw-r--r--   0        0        0      661 2023-07-20 14:53:29.280232 iamlistening-1.1.7/iamlistening/config.py
--rw-r--r--   0        0        0     2087 2023-07-20 14:53:29.280232 iamlistening-1.1.7/iamlistening/default_settings.toml
--rw-r--r--   0        0        0     4307 2023-07-20 14:53:29.280232 iamlistening-1.1.7/iamlistening/main.py
--rw-r--r--   0        0        0     3109 2023-07-20 14:53:31.040355 iamlistening-1.1.7/pyproject.toml
--rw-r--r--   0        0        0     3837 1970-01-01 00:00:00.000000 iamlistening-1.1.7/PKG-INFO
+-rw-r--r--   0        0        0     1064 2023-07-23 19:35:03.439154 iamlistening-2.0.0/LICENSE
+-rw-r--r--   0        0        0     2910 2023-07-23 19:35:03.439154 iamlistening-2.0.0/README.md
+-rw-r--r--   0        0        0      122 2023-07-23 19:35:07.095184 iamlistening-2.0.0/iamlistening/__init__.py
+-rw-r--r--   0        0        0      661 2023-07-23 19:35:03.439154 iamlistening-2.0.0/iamlistening/config.py
+-rw-r--r--   0        0        0     2669 2023-07-23 19:35:03.439154 iamlistening-2.0.0/iamlistening/default_settings.toml
+-rw-r--r--   0        0        0     4734 2023-07-23 19:35:03.439154 iamlistening-2.0.0/iamlistening/main.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:35:03.439154 iamlistening-2.0.0/iamlistening/platform/__init__.py
+-rw-r--r--   0        0        0      540 2023-07-23 19:35:03.439154 iamlistening-2.0.0/iamlistening/platform/discord.py
+-rw-r--r--   0        0        0     1239 2023-07-23 19:35:03.439154 iamlistening-2.0.0/iamlistening/platform/matrix.py
+-rw-r--r--   0        0        0      402 2023-07-23 19:35:03.439154 iamlistening-2.0.0/iamlistening/platform/rocket_chat.py
+-rw-r--r--   0        0        0      591 2023-07-23 19:35:03.439154 iamlistening-2.0.0/iamlistening/platform/telegram.py
+-rw-r--r--   0        0        0     3146 2023-07-23 19:35:07.087184 iamlistening-2.0.0/pyproject.toml
+-rw-r--r--   0        0        0     3897 1970-01-01 00:00:00.000000 iamlistening-2.0.0/PKG-INFO
```

### Comparing `iamlistening-1.1.7/LICENSE` & `iamlistening-2.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `iamlistening-1.1.7/README.md` & `iamlistening-2.0.0/README.md`

 * *Files identical despite different names*

### Comparing `iamlistening-1.1.7/iamlistening/config.py` & `iamlistening-2.0.0/iamlistening/config.py`

 * *Files identical despite different names*

### Comparing `iamlistening-1.1.7/iamlistening/default_settings.toml` & `iamlistening-2.0.0/iamlistening/default_settings.toml`

 * *Files 13% similar despite different names*

```diff
@@ -19,15 +19,18 @@
 bot_token = ""
 bot_channel_id = ""
 telethon_api_id = ""
 telethon_api_hash = ""
 matrix_hostname = ""
 matrix_user = ""
 matrix_pass = ""
-iamlistening_commands = "/help"
+rocket_chat_server = ""
+rocket_chat_user_id = ""
+rocket_chat_auth_token = ""
+
 
 
 
 
 
 
  
@@ -67,29 +70,52 @@
 bot_token = "1234556"
 bot_channel_id = "1234556"
 telethon_api_id = "1234556"
 telethon_api_hash = "1234556"
 matrix_hostname = ""
 matrix_user = ""
 matrix_pass = ""
+rocket_chat_server = ""
+rocket_chat_user_id = ""
+rocket_chat_auth_token = ""
 
 [testingdiscord]
 VALUE = "On Testing Discord"
 iamlistening_enabled = true
 bot_token = "1234556"
 bot_channel_id = "1234556"
 telethon_api_id = ""
 telethon_api_hash = ""
 matrix_hostname = ""
 matrix_user = ""
 matrix_pass = ""
+rocket_chat_server = ""
+rocket_chat_user_id = ""
+rocket_chat_auth_token = ""
 
 [testingmatrix]
 VALUE = "On Testing Matrix"
 iamlistening_enabled = true
 bot_token = "1234556"
 bot_channel_id = "1234556"
 telethon_api_id = ""
 telethon_api_hash = ""
 matrix_hostname = "123456789"
 matrix_user = "123456789"
 matrix_pass = "123456789"
+rocket_chat_server = ""
+rocket_chat_user_id = ""
+rocket_chat_auth_token = ""
+
+[testingrocketchat]
+VALUE = "On Testing RocketChat"
+iamlistening_enabled = true
+bot_token = "1234556"
+bot_channel_id = "1234556"
+telethon_api_id = ""
+telethon_api_hash = ""
+matrix_hostname = ""
+matrix_user = ""
+matrix_pass = ""
+rocket_chat_server = ""
+rocket_chat_user_id = ""
+rocket_chat_auth_token = ""
```

### Comparing `iamlistening-1.1.7/iamlistening/main.py` & `iamlistening-2.0.0/iamlistening/main.py`

 * *Files 9% similar despite different names*

```diff
@@ -10,97 +10,50 @@
 import simplematrixbotlib as botlib
 from telethon import TelegramClient, events
 
 from iamlistening import __version__
 
 from .config import settings
 
+# from .platform.discord import start_discord
+# from .platform import discord, matrix, rocket_chat, telegram
+
 
 class Listener:
     """ 👂 Listener class """
 
     def __init__(self):
         self.logger = logging.getLogger("Listener")
         self.latest_message = None
         self.loop = asyncio.get_event_loop()
         self.lock = threading.Lock()
         self.stopped = False
 
-    async def start(self):
-        """start"""
+    async def get_info_listener(self):
+        return (f"ℹ️ IAmListening v{__version__}\n")
 
+    async def start(self):
+        """Start the listener."""
         if settings.telethon_api_id:
-            # TELEGRAM
-            self.logger.debug("Telegram setup")
-            bot = await TelegramClient(
-                        None,
-                        settings.telethon_api_id,
-                        settings.telethon_api_hash
-                        ).start(bot_token=settings.bot_token)
-            await self.post_init()
+            await self.start_telegram()
 
-            @bot.on(events.NewMessage())
-            async def telethon(event):
-                await self.handle_message(event.message.message)
+        elif settings.matrix_hostname:
+            await self.start_matrix()
 
-            await bot.run_until_disconnected()
+        elif settings.rocket_chat_server:
+            await self.start_rocket_chat()
 
-        elif settings.matrix_hostname:
-            # MATRIX
-            self.logger.debug("Matrix setup")
-            config = botlib.Config()
-            config.emoji_verify = True
-            config.ignore_unverified_devices = True
-            config.store_path = './config/matrix/'
-            creds = botlib.Creds(
-                        settings.matrix_hostname,
-                        settings.matrix_user,
-                        settings.matrix_pass
-                        )
-            bot = botlib.Bot(creds, config)
-
-            @bot.listener.on_startup
-            async def room_joined(room):
-                await self.post_init()
-
-            @bot.listener.on_message_event
-            async def on_matrix_message(room, message):
-                await self.handle_message(message.body)
-            await bot.api.login()
-            bot.api.async_client.callbacks = botlib.Callbacks(
-                                                bot.api.async_client, bot
-                                                )
-            await bot.api.async_client.callbacks.setup_callbacks()
-            for action in bot.listener._startup_registry:
-                for room_id in bot.api.async_client.rooms:
-                    await action(room_id)
-            await bot.api.async_client.sync_forever(
-                                                    timeout=3000,
-                                                    full_state=True
-                                                )
         elif settings.bot_token:
-            # DISCORD
-            self.logger.debug("Discord setup")
-            intents = discord.Intents.default()
-            intents.message_content = True
-            bot = discord.Bot(intents=intents)
-
-            @bot.event
-            async def on_ready():
-                await self.post_init()
-
-            @bot.event
-            async def on_message(message: discord.Message):
-                await self.handle_message(message.content)
-            await bot.start(settings.bot_token)
+            await self.start_discord()
 
         else:
             self.logger.warning("Check settings")
             await asyncio.sleep(7200)
-
+    
+ 
     async def get_latest_message(self):
         """Return the latest message."""
         while True:
             with self.lock:
                 if self.latest_message is not None:
                     msg = self.latest_message
                     self.latest_message = None
@@ -110,24 +63,93 @@
 
     async def handle_message(self, message_content):
         """Handle a new message."""
         self.latest_message = message_content
 
 
     async def run_forever(self, max_iterations=None):
-        """Run the listener for a specified number of iterations or until stopped."""
+        """Run the listener for 
+        a specified number of iterations or until stopped."""
+
         iteration = 0
         while not self.stopped and (
             max_iterations is None or iteration < max_iterations):
             await self.start()
             iteration += 1
 
     async def post_init(self):
         return "bot is online"
 
     def stop(self):
         """Stop the listener."""
         self.stopped = True
 
-    async def get_info_listener(self):
-        return (f"ℹ️ {__class__.__name__} {__version__}\n")
+    async def start_discord(self):
+        """Start the Discord handler."""
+        self.logger.debug("Discord setup")
+        intents = discord.Intents.default()
+        intents.message_content = True
+        bot = discord.Bot(intents=intents)
+
+        @bot.event
+        async def on_ready():
+            await self.post_init()
+
+        @bot.event
+        async def on_message(message: discord.Message):
+            await self.handle_message(message.content)
+        await bot.start(settings.bot_token)
+
+    async def start_telegram(self):
+        """Start the Telegram handler."""
+        self.logger.debug("Telegram setup")
+        bot = await TelegramClient(
+                    None,
+                    settings.telethon_api_id,
+                    settings.telethon_api_hash
+                    ).start(bot_token=settings.bot_token)
+        await self.post_init()
+
+        @bot.on(events.NewMessage())
+        async def telethon(event):
+            await self.handle_message(event.message.message)
+
+        await bot.run_until_disconnected()
+
+
+    async def start_matrix(self):
+        """Start the Matrix handler."""
+        self.logger.debug("Matrix setup")
+        config = botlib.Config()
+        config.emoji_verify = True
+        config.ignore_unverified_devices = True
+        config.store_path = './config/matrix/'
+        creds = botlib.Creds(
+                    settings.matrix_hostname,
+                    settings.matrix_user,
+                    settings.matrix_pass
+                    )
+        bot = botlib.Bot(creds, config)
+
+        @bot.listener.on_startup
+        async def room_joined(room):
+            await self.post_init()
 
+        @bot.listener.on_message_event
+        async def on_matrix_message(room, message):
+            await self.handle_message(message.body)
+        await bot.api.login()
+        bot.api.async_client.callbacks = botlib.Callbacks(
+                                            bot.api.async_client, bot
+                                            )
+        await bot.api.async_client.callbacks.setup_callbacks()
+        for action in bot.listener._startup_registry:
+            for room_id in bot.api.async_client.rooms:
+                await action(room_id)
+        await bot.api.async_client.sync_forever(
+                                                timeout=3000,
+                                                full_state=True
+                                            )
+
+    async def start_rocket_chat(self):
+        """Start the RocketChat handler."""
+        self.logger.debug("RocketChat setup")
```

### Comparing `iamlistening-1.1.7/pyproject.toml` & `iamlistening-2.0.0/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 
 [tool.poetry]
 name = "iamlistening"
-version = "1.1.7"
+version = "2.0.0"
 description = "A python package to interact with messaging platform."
 authors = ["mraniki <8766259+mraniki@users.noreply.github.com>"]
 license = "MIT License"
 readme = "README.md"
 keywords = [
     "bot","messaging",
-    "discord", "telegram","matrix",
+    "discord", "telegram","matrix","rocket chat",
     ]
 packages = [
     {include = "iamlistening"}
 ]
 
 
 [tool.poetry.urls]
@@ -26,15 +26,16 @@
 
 [tool.poetry.dependencies]
 python = "^3.10"
 dynaconf = "^3.1.12"
 telethon= "^1.28.5"
 py-cord= "^2.4.1"
 simplematrixbotlib= "^2.9.0"
- 
+rocketchat-API= "^1.30.0"
+
 
 [tool.poetry.group.dev.dependencies]
 python-semantic-release = "^8.0.1"
 ruff = "^0.0.278"
 
 [tool.ruff]
 select = [
@@ -135,9 +136,9 @@
     "🥅",":goal_net:",
     "✅",":white_check_mark:",
     "🐳",":whale:",
     "🙈",":see_no_evil:",
     "⚗️",":alembic:",
     "🧐",":monocle_face:",
     "🔇",":mute:",
-    "🔊",":volume:",
+    "🔊",":loud:",
 ]
```

### Comparing `iamlistening-1.1.7/PKG-INFO` & `iamlistening-2.0.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,22 +1,23 @@
 Metadata-Version: 2.1
 Name: iamlistening
-Version: 1.1.7
+Version: 2.0.0
 Summary: A python package to interact with messaging platform.
 License: MIT
-Keywords: bot,messaging,discord,telegram,matrix
+Keywords: bot,messaging,discord,telegram,matrix,rocket chat
 Author: mraniki
 Author-email: 8766259+mraniki@users.noreply.github.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: dynaconf (>=3.1.12,<4.0.0)
 Requires-Dist: py-cord (>=2.4.1,<3.0.0)
+Requires-Dist: rocketchat-API (>=1.30.0,<2.0.0)
 Requires-Dist: simplematrixbotlib (>=2.9.0,<3.0.0)
 Requires-Dist: telethon (>=1.28.5,<2.0.0)
 Project-URL: Changelog, https://github.com/mraniki/iamlistening/blob/dev/CHANGELOG.rst
 Project-URL: Issues, https://github.com/mraniki/iamlistening/issues
 Project-URL: Support, https://github.com/mraniki/iamlistening/discussions
 Description-Content-Type: text/markdown
```

#### html2text {}

```diff
@@ -1,20 +1,21 @@
-Metadata-Version: 2.1 Name: iamlistening Version: 1.1.7 Summary: A python
+Metadata-Version: 2.1 Name: iamlistening Version: 2.0.0 Summary: A python
 package to interact with messaging platform. License: MIT Keywords:
-bot,messaging,discord,telegram,matrix Author: mraniki Author-email:
+bot,messaging,discord,telegram,matrix,rocket chat Author: mraniki Author-email:
 8766259+mraniki@users.noreply.github.com Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License Classifier: Programming
 Language :: Python :: 3 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11 Requires-Dist: dynaconf
 (>=3.1.12,<4.0.0) Requires-Dist: py-cord (>=2.4.1,<3.0.0) Requires-Dist:
-simplematrixbotlib (>=2.9.0,<3.0.0) Requires-Dist: telethon (>=1.28.5,<2.0.0)
-Project-URL: Changelog, https://github.com/mraniki/iamlistening/blob/dev/
-CHANGELOG.rst Project-URL: Issues, https://github.com/mraniki/iamlistening/
-issues Project-URL: Support, https://github.com/mraniki/iamlistening/
-discussions Description-Content-Type: text/markdown
+rocketchat-API (>=1.30.0,<2.0.0) Requires-Dist: simplematrixbotlib
+(>=2.9.0,<3.0.0) Requires-Dist: telethon (>=1.28.5,<2.0.0) Project-URL:
+Changelog, https://github.com/mraniki/iamlistening/blob/dev/CHANGELOG.rst
+Project-URL: Issues, https://github.com/mraniki/iamlistening/issues Project-
+URL: Support, https://github.com/mraniki/iamlistening/discussions Description-
+Content-Type: text/markdown
 [https://img.shields.io/badge/Wiki-%23000000.svg?style=for-
 the-badge&logo=wikipedia&logoColor=white]
 [https://img.shields.io/badge/github-
 %23000000.svg?style=for-the-
 badge&logo=github&logoColor=white] [Docker_Pulls]
 [https://img.shields.io/badge/tips-000000?style=for-the-             [Logo]
 badge&logo=buymeacoffee&logoColor=white] [https://
```

