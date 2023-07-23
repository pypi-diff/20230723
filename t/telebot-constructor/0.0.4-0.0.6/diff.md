# Comparing `tmp/telebot_constructor-0.0.4.tar.gz` & `tmp/telebot_constructor-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "telebot_constructor-0.0.4.tar", max compression
+gzip compressed data, was "telebot_constructor-0.0.6.tar", max compression
```

## Comparing `telebot_constructor-0.0.4.tar` & `telebot_constructor-0.0.6.tar`

### file list

```diff
@@ -1,9 +1,14 @@
--rw-r--r--   0        0        0      836 2023-07-21 13:34:06.132139 telebot_constructor-0.0.4/README.md
--rw-r--r--   0        0        0     1330 2023-07-21 13:34:31.331984 telebot_constructor-0.0.4/pyproject.toml
--rw-r--r--   0        0        0        0 2023-07-21 13:34:06.136139 telebot_constructor-0.0.4/telebot_constructor/__init__.py
--rw-r--r--   0        0        0    11842 2023-07-21 13:34:06.136139 telebot_constructor-0.0.4/telebot_constructor/app.py
--rw-r--r--   0        0        0       94 2023-07-21 13:34:06.136139 telebot_constructor-0.0.4/telebot_constructor/bot_config.py
--rw-r--r--   0        0        0      643 2023-07-21 13:34:06.136139 telebot_constructor-0.0.4/telebot_constructor/construct.py
--rw-r--r--   0        0        0     2718 2023-07-21 13:34:06.136139 telebot_constructor-0.0.4/telebot_constructor/runners.py
--rw-r--r--   0        0        0     3226 2023-07-21 13:34:29.859992 telebot_constructor-0.0.4/telebot_constructor/static/index.html
--rw-r--r--   0        0        0     1477 1970-01-01 00:00:00.000000 telebot_constructor-0.0.4/PKG-INFO
+-rw-r--r--   0        0        0      932 2023-07-23 08:40:20.750195 telebot_constructor-0.0.6/README.md
+-rw-r--r--   0        0        0     1330 2023-07-23 08:40:38.634629 telebot_constructor-0.0.6/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-07-23 08:40:20.754195 telebot_constructor-0.0.6/telebot_constructor/__init__.py
+-rw-r--r--   0        0        0    12799 2023-07-23 08:40:20.754195 telebot_constructor-0.0.6/telebot_constructor/app.py
+-rw-r--r--   0        0        0     4882 2023-07-23 08:40:20.754195 telebot_constructor-0.0.6/telebot_constructor/auth.py
+-rw-r--r--   0        0        0       94 2023-07-23 08:40:20.754195 telebot_constructor-0.0.6/telebot_constructor/bot_config.py
+-rw-r--r--   0        0        0      785 2023-07-23 08:40:20.754195 telebot_constructor-0.0.6/telebot_constructor/construct.py
+-rw-r--r--   0        0        0       64 2023-07-23 08:40:20.754195 telebot_constructor-0.0.6/telebot_constructor/debug.py
+-rw-r--r--   0        0        0        0 2023-07-23 08:40:20.754195 telebot_constructor-0.0.6/telebot_constructor/py.typed
+-rw-r--r--   0        0        0     2718 2023-07-23 08:40:20.754195 telebot_constructor-0.0.6/telebot_constructor/runners.py
+-rw-r--r--   0        0        0     1553 2023-07-23 08:40:37.586604 telebot_constructor-0.0.6/telebot_constructor/static/group_chat_auth_login.html
+-rw-r--r--   0        0        0     3469 2023-07-23 08:40:37.586604 telebot_constructor-0.0.6/telebot_constructor/static/index.html
+-rw-r--r--   0        0        0      360 2023-07-23 08:40:20.754195 telebot_constructor-0.0.6/telebot_constructor/static.py
+-rw-r--r--   0        0        0     1573 1970-01-01 00:00:00.000000 telebot_constructor-0.0.6/PKG-INFO
```

### Comparing `telebot_constructor-0.0.4/README.md` & `telebot_constructor-0.0.6/README.md`

 * *Files 9% similar despite different names*

```diff
@@ -17,7 +17,15 @@
      ```bash
      poetry self add poetry-dynamic-versioning-plugin
      ```
    - To create virtualenv inside the project’s root directory, use command
      ```bash
      poetry config virtualenvs.in-project false --local
      ```
+
+
+### Running in debug mode
+
+```sh
+export TELEBOT_CONSTRUCTOR_DEBUG=1
+python run_polling.py
+```
```

### Comparing `telebot_constructor-0.0.4/pyproject.toml` & `telebot_constructor-0.0.6/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "telebot-constructor"
-version = "0.0.4"
+version = "0.0.6"
 description = "No-code Telegram bot constructor"
 authors = ["Igor Vaiman <gosha.vaiman@gmail.com>"]
 license = "GPL-3"
 readme = "README.md"
 packages = [{include = "telebot_constructor"}]
 include = ["telebot_constructor/static/*"]
```

### Comparing `telebot_constructor-0.0.4/telebot_constructor/app.py` & `telebot_constructor-0.0.6/telebot_constructor/app.py`

 * *Files 19% similar despite different names*

```diff
@@ -9,29 +9,37 @@
 import telebot.api
 from aiohttp import web
 from aiohttp_swagger import setup_swagger  # type: ignore
 from telebot.webhook import WebhookApp
 from telebot_components.redis_utils.interface import RedisInterface
 from telebot_components.stores.generic import KeyDictStore, KeySetStore
 
+from telebot_constructor.auth import Auth
 from telebot_constructor.bot_config import BotConfig
 from telebot_constructor.construct import construct_bot
 from telebot_constructor.runners import (
     ConstructedBotRunner,
     PollingConstructedBotRunner,
     WebhookAppConstructedBotRunner,
 )
+from telebot_constructor.static import static_file_content
 
 logger = logging.getLogger(__name__)
 
 
 class TelebotConstructorApp:
     STORE_PREFIX = "telebot-constructor"
+    URL_PREFIX = "/constructor"
+
+    def __init__(self, redis: RedisInterface, auth: Auth, static_files_dir_override: Optional[Path] = None) -> None:
+        self.auth = auth
+        self.static_files_dir = static_files_dir_override or Path(__file__).parent / "static"
+        self._runner: Optional[ConstructedBotRunner] = None
+        logger.info(f"Will serve static frontend files from {self.static_files_dir.absolute()}")
 
-    def __init__(self, redis: RedisInterface, static_files_dir_override: Optional[Path] = None) -> None:
         # user id -> {bot name -> config}
         self.bot_config_store = KeyDictStore[BotConfig](
             name="bot-configs",
             prefix=self.STORE_PREFIX,
             redis=redis,
             expiration_time=None,
             dumper=BotConfig.model_dump_json,
@@ -39,26 +47,26 @@
         )
         self.running_bots_store = KeySetStore[str](
             name="bot-running",
             prefix=self.STORE_PREFIX,
             redis=redis,
             expiration_time=None,
         )
-        self.static_files_dir = static_files_dir_override or Path(__file__).parent / "static"
-        self._runner: Optional[ConstructedBotRunner] = None
-        logger.info(f"Will serve static frontend files from {self.static_files_dir.absolute()}")
 
     @property
     def runner(self) -> ConstructedBotRunner:
         if self._runner is None:
             raise RuntimeError("Constructed bot runner was not initialized properly")
         return self._runner
 
     async def authenticate(self, request: web.Request) -> str:
-        return "admin"  # TODO: username lookup based on access token / other auth method
+        username = await self.auth.authenticate_request(request)
+        if username is None:
+            raise web.HTTPUnauthorized(reason="Authentication required")
+        return username
 
     VALID_BOT_NAME_RE = re.compile(r"^[0-9a-zA-Z\-_]{5,16}$")
 
     def parse_bot_name(self, request: web.Request) -> str:
         name = request.match_info.get("bot_name")
         if name is None:
             raise web.HTTPNotFound()
@@ -68,28 +76,34 @@
 
     async def load_bot_config(self, username: str, bot_name: str) -> BotConfig:
         config = await self.bot_config_store.get_subkey(username, bot_name)
         if config is None:
             raise web.HTTPNotFound(reason=f"No config found for bot name {bot_name!r}")
         return config
 
-    def setup_roots(self, app: web.Application) -> None:
+    async def setup_routes(self, app: web.Application) -> None:
         routes = web.RouteTableDef()
 
         ##################################################################################
         # static file routes
 
-        @routes.get("/constructor")
+        @routes.get(self.URL_PREFIX)
         async def index(request: web.Request) -> web.Response:
-            return web.Response(body=(self.static_files_dir / "index.html").read_bytes(), content_type="text/html")
+            username = await self.auth.authenticate_request(request)
+            if username is None:
+                return await self.auth.unauthenticated_client_response(request, static_files_dir=self.static_files_dir)
+            return web.Response(
+                body=static_file_content(self.static_files_dir / "index.html"),
+                content_type="text/html",
+            )
 
         ##################################################################################
         # bot configs CRUD
 
-        @routes.post("/constructor/config/{bot_name}")
+        @routes.post(self.URL_PREFIX + "/config/{bot_name}")
         async def upsert_new_bot_config(request: web.Request) -> web.Response:
             """
             ---
             description: Create or update bot configuration
             produces:
             - application/json
             responses:
@@ -111,15 +125,15 @@
                 raise web.HTTPBadRequest(reason=str(e))
             await self.bot_config_store.set_subkey(username, bot_name, bot_config)
             if existing_bot_config is None:
                 return web.json_response(text=bot_config.model_dump_json(), status=201)
             else:
                 return web.json_response(text=existing_bot_config.model_dump_json())
 
-        @routes.get("/constructor/config/{bot_name}")
+        @routes.get(self.URL_PREFIX + "/config/{bot_name}")
         async def get_bot_config(request: web.Request) -> web.Response:
             """
             ---
             description: Get config for bot with a given name
             produces:
             - application/json
             responses:
@@ -129,15 +143,15 @@
                     description: No config found
             """
             username = await self.authenticate(request)
             bot_name = self.parse_bot_name(request)
             config = await self.load_bot_config(username, bot_name)
             return web.json_response(text=config.model_dump_json())
 
-        @routes.delete("/constructor/config/{bot_name}")
+        @routes.delete(self.URL_PREFIX + "/config/{bot_name}")
         async def remove_bot_config(request: web.Request) -> web.Response:
             """
             ---
             description: Delete bot config; if the bot was running, it is stopped
             produces:
             - application/json
             responses:
@@ -148,15 +162,15 @@
             bot_name = self.parse_bot_name(request)
             config = await self.load_bot_config(username, bot_name)
             await self.runner.stop(username, bot_name)
             await self.running_bots_store.remove(username, bot_name)
             await self.bot_config_store.remove_subkey(username, bot_name)
             return web.json_response(text=config.model_dump_json())
 
-        @routes.get("/constructor/config")
+        @routes.get(self.URL_PREFIX + "/config")
         async def list_bot_configs(request: web.Request) -> web.Response:
             """
             ---
             description: List all bot configs
             produces:
             - application/json
             responses:
@@ -168,15 +182,15 @@
             return web.json_response(
                 data={name: config.model_dump(mode="json") for name, config in bot_configs.items()}
             )
 
         ##################################################################################
         # bot lifecycle control: start, stop, list running
 
-        @routes.post("/constructor/start/{bot_name}")
+        @routes.post(self.URL_PREFIX + "/start/{bot_name}")
         async def start_bot(request: web.Request) -> web.Response:
             """
             ---
             description: Start bot
             produces:
             - text/plain
             responses:
@@ -184,22 +198,25 @@
                     description: Bot started
                 "200":
                     description: Bot is already running
             """
             username = await self.authenticate(request)
             bot_name = self.parse_bot_name(request)
             bot_config = await self.load_bot_config(username, bot_name)
-            bot_runner = await construct_bot(username, bot_name, bot_config)
+            try:
+                bot_runner = await construct_bot(username, bot_name, bot_config)
+            except Exception as e:
+                raise web.HTTPBadRequest(reason=str(e))
             if await self.runner.start(username=username, bot_name=bot_name, bot_runner=bot_runner):
                 await self.running_bots_store.add(username, bot_name)
                 return web.Response(text="Bot started", status=201)
             else:
                 return web.Response(text="Bot is already running")
 
-        @routes.post("/constructor/stop/{bot_name}")
+        @routes.post(self.URL_PREFIX + "/stop/{bot_name}")
         async def stop_bot(request: web.Request) -> web.Response:
             """
             ---
             description: Stop bot
             produces:
             - text/plain
             responses:
@@ -212,15 +229,15 @@
             bot_name = self.parse_bot_name(request)
             if await self.runner.stop(username=username, bot_name=bot_name):
                 await self.running_bots_store.remove(username, bot_name)
                 return web.Response(text="Bot stopped")
             else:
                 return web.Response(text="Bot was not running")
 
-        @routes.get("/constructor/running")
+        @routes.get(self.URL_PREFIX + "/running")
         async def list_running_bots(request: web.Request) -> web.Response:
             """
             ---
             description: List running bots
             produces:
             - application/json
             responses:
@@ -228,41 +245,45 @@
                     description: List of running bots' names
             """
             username = await self.authenticate(request)
             running_bots = await self.running_bots_store.all(username)
             return web.json_response(data=sorted(running_bots))
 
         app.add_routes(routes)
-        setup_swagger(app=app)
+        setup_swagger(app=app, swagger_url=f"{self.URL_PREFIX}/swagger")
+        await self.auth.setup_routes(app)
 
     async def _ensure_running_bots(self) -> None:
         """Ensure that all bots stored as running are indeed running; used mainly on startup"""
         usernames = await self.running_bots_store.list_keys()
         logger.info("Found %s usernames with bot running flags", len(usernames))
         for username in usernames:
             running_bots = await self.running_bots_store.all(username)
             logger.info("Username %s has %s running bots: %s", usernames, len(running_bots), running_bots)
             for bot_name in running_bots:
                 bot_config = await self.bot_config_store.get_subkey(username, bot_name)
                 if bot_config is None:
                     logger.error(f"Bot {bot_name!r} is in running bots store, but has no config")
                     await self.running_bots_store.remove(username, bot_name)
                     continue
-                bot_runner = await construct_bot(username=username, bot_name=bot_name, bot_config=bot_config)
-                await self.runner.start(username=username, bot_name=bot_name, bot_runner=bot_runner)
+                try:
+                    bot_runner = await construct_bot(username=username, bot_name=bot_name, bot_config=bot_config)
+                    await self.runner.start(username=username, bot_name=bot_name, bot_runner=bot_runner)
+                except Exception:
+                    logger.exception(f"Error creating bot {bot_name} ({username = })")
 
     # public methods to run constructor in different scenarios
 
     async def run_polling(self, port: int) -> None:
         """For standalone run"""
         logger.info("Running telebot constructor w/ polling")
         self._runner = PollingConstructedBotRunner()
         await self._ensure_running_bots()
         aiohttp_app = web.Application()
-        self.setup_roots(aiohttp_app)
+        await self.setup_routes(aiohttp_app)
         aiohttp_runner = web.AppRunner(aiohttp_app)
         await aiohttp_runner.setup()
         site = web.TCPSite(aiohttp_runner, "0.0.0.0", port)
         logger.info(f"Running server on {site.name}")
         try:
             await site.start()
             while True:
@@ -273,8 +294,8 @@
             await telebot.api.session_manager.close_session()
             logger.debug("Cleanup completed")
             await aiohttp_runner.cleanup()
 
     async def setup_on_webhook_app(self, webhook_app: WebhookApp) -> None:
         self._runner = WebhookAppConstructedBotRunner(webhook_app)
         await self._ensure_running_bots()
-        self.setup_roots(webhook_app.aiohttp_app)
+        await self.setup_routes(webhook_app.aiohttp_app)
```

### Comparing `telebot_constructor-0.0.4/telebot_constructor/construct.py` & `telebot_constructor-0.0.6/telebot_constructor/construct.py`

 * *Files 15% similar despite different names*

```diff
@@ -9,8 +9,13 @@
     """Main heavy lifting function responsible for creating bot with all the necessary handlers / components / etc"""
     bot = AsyncTeleBot(token=bot_config.token)
 
     @bot.message_handler(commands=["start"])
     async def dummy_start_handler(message: tg.Message) -> None:
         await bot.reply_to(message, "hello world")
 
+    try:
+        await bot.get_me()
+    except Exception:
+        raise ValueError("Failed to getMe the bot, the token is probably invalid")
+
     return BotRunner(bot_prefix=f"{username}-{bot_name}", bot=bot)
```

### Comparing `telebot_constructor-0.0.4/telebot_constructor/runners.py` & `telebot_constructor-0.0.6/telebot_constructor/runners.py`

 * *Files identical despite different names*

### Comparing `telebot_constructor-0.0.4/telebot_constructor/static/index.html` & `telebot_constructor-0.0.6/telebot_constructor/static/index.html`

 * *Files 7% similar despite different names*

```diff
@@ -3,16 +3,17 @@
 
 <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>Telebot constructor</title>
 </head>
 
-<body onload="reloadConfigs()">
-    <h1>Telebot constructor v0.0.1</h1>
+<body onload="reloadConfigs()"
+    style="font-family: 'Courier New', Courier, monospace; width: min(95vw, 800px); margin: 0 auto;">
+    <h1>Telebot constructor</h1>
     <div>
         <h3>Add bot</h3>
         <form>
             <label for="bot_name">Name</label><br>
             <input type="text" id="bot_name" name="bot_name"><br>
             <label for="bot_token">Token</label><br>
             <input type="text" id="bot_token" name="bot_token"><br>
@@ -64,26 +65,30 @@
     async function removeBotConfig(name) {
         const resp = await fetch(`/constructor/config/${name}`, { method: "DELETE" });
         const statusEl = document.getElementById(`${name}-status`);
         await reloadConfigs();
     }
 
     async function createNewConfig() {
-        const name = document.getElementById("bot_name").value;
-        const token = document.getElementById("bot_token").value;
+        const nameEl = document.getElementById("bot_name");
+        const tokenEl = document.getElementById("bot_token");
+        const name = nameEl.value;
+        const token = tokenEl.value;
         if (name.length === 0 || token.length === 0) {
-            console.log("form not complete");
+            console.log("form not completed");
             return;
         }
         const payload = JSON.stringify({ token });
         console.log(payload);
-        const resp = await fetch(`/constructor/config/${name}`, { method: "POST", body: payload });
+        const resp = await fetch(`/constructor/config/${encodeURIComponent(name)}`, { method: "POST", body: payload });
         console.log(resp);
         if (resp.ok) {
+            nameEl.value = "";
+            tokenEl.value = "";
             await reloadConfigs();
         } else {
-            document.getElementById("newBotConfigStatus").innerHTML = await resp.text()
+            document.getElementById("newBotConfigStatus").innerHTML = await resp.text();
         }
     }
 </script>
 
 </html>
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
 
-****** Telebot constructor v0.0.1 ******
+****** Telebot constructor ******
 **** Add bot ****
 Name
 [bot_name            ]
 Token
 [bot_token           ]
 New bot
```

### Comparing `telebot_constructor-0.0.4/PKG-INFO` & `telebot_constructor-0.0.6/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: telebot-constructor
-Version: 0.0.4
+Version: 0.0.6
 Summary: No-code Telegram bot constructor
 License: GPL-3
 Author: Igor Vaiman
 Author-email: gosha.vaiman@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: Other/Proprietary License
 Classifier: Programming Language :: Python :: 3
@@ -36,7 +36,15 @@
      poetry self add poetry-dynamic-versioning-plugin
      ```
    - To create virtualenv inside the project’s root directory, use command
      ```bash
      poetry config virtualenvs.in-project false --local
      ```
 
+
+### Running in debug mode
+
+```sh
+export TELEBOT_CONSTRUCTOR_DEBUG=1
+python run_polling.py
+```
+
```

