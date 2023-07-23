# Comparing `tmp/discoger-2.1.0.tar.gz` & `tmp/discoger-2.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "discoger-2.1.0.tar", last modified: Sun Jul  9 20:42:20 2023, max compression
+gzip compressed data, was "discoger-2.1.1.tar", last modified: Sun Jul 23 08:08:39 2023, max compression
```

## Comparing `discoger-2.1.0.tar` & `discoger-2.1.1.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-09 20:42:20.871458 discoger-2.1.0/
--rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-07-09 20:42:06.000000 discoger-2.1.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2845 2023-07-09 20:42:20.871458 discoger-2.1.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1495 2023-07-09 20:42:06.000000 discoger-2.1.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-09 20:42:20.871458 discoger-2.1.0/discoger/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-09 20:42:06.000000 discoger-2.1.0/discoger/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      339 2023-07-09 20:42:06.000000 discoger-2.1.0/discoger/_info.py
--rw-r--r--   0 runner    (1001) docker     (123)    10659 2023-07-09 20:42:06.000000 discoger-2.1.0/discoger/client.py
--rw-r--r--   0 runner    (1001) docker     (123)     2620 2023-07-09 20:42:06.000000 discoger-2.1.0/discoger/scrap.py
--rw-r--r--   0 runner    (1001) docker     (123)     4145 2023-07-09 20:42:06.000000 discoger-2.1.0/discoger/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-09 20:42:20.871458 discoger-2.1.0/discoger.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2845 2023-07-09 20:42:20.000000 discoger-2.1.0/discoger.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      293 2023-07-09 20:42:20.000000 discoger-2.1.0/discoger.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-09 20:42:20.000000 discoger-2.1.0/discoger.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-09 20:42:20.000000 discoger-2.1.0/discoger.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-09 20:42:20.000000 discoger-2.1.0/discoger.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       79 2023-07-09 20:42:20.871458 discoger-2.1.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1667 2023-07-09 20:42:06.000000 discoger-2.1.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:08:39.049098 discoger-2.1.1/
+-rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-07-23 08:08:19.000000 discoger-2.1.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2845 2023-07-23 08:08:39.049098 discoger-2.1.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1495 2023-07-23 08:08:19.000000 discoger-2.1.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:08:39.045098 discoger-2.1.1/discoger/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 08:08:19.000000 discoger-2.1.1/discoger/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      339 2023-07-23 08:08:19.000000 discoger-2.1.1/discoger/_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10885 2023-07-23 08:08:19.000000 discoger-2.1.1/discoger/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2903 2023-07-23 08:08:19.000000 discoger-2.1.1/discoger/scrap.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4145 2023-07-23 08:08:19.000000 discoger-2.1.1/discoger/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:08:39.049098 discoger-2.1.1/discoger.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2845 2023-07-23 08:08:38.000000 discoger-2.1.1/discoger.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      293 2023-07-23 08:08:39.000000 discoger-2.1.1/discoger.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 08:08:38.000000 discoger-2.1.1/discoger.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-23 08:08:38.000000 discoger-2.1.1/discoger.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 08:08:38.000000 discoger-2.1.1/discoger.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       79 2023-07-23 08:08:39.049098 discoger-2.1.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1667 2023-07-23 08:08:19.000000 discoger-2.1.1/setup.py
```

### Comparing `discoger-2.1.0/LICENSE` & `discoger-2.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `discoger-2.1.0/PKG-INFO` & `discoger-2.1.1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: discoger
-Version: 2.1.0
+Version: 2.1.1
 Summary: Get notification from Discogs
 Home-page: https://github.com/beudbeud/discoger
 Author: Beudbeud
 Author-email: beudbeud@gmail.com
 License: GNU General Public License v3 (GPLv3)
-Download-URL: https://github.com/beudbeud/discoger/archive/2.1.0.tar.gz
+Download-URL: https://github.com/beudbeud/discoger/archive/2.1.1.tar.gz
 Description: # Discoger
         
         Discoger Bot is a Telegram bot that allows you to be notified when a new sale for a vinyl in your Discogs wantlist is available.
         
         ## Usage
         
         1. Search for the Telegram bot "Discoger" or click [this link](https://t.me/Discogers_bot) to open a conversation with the bot.
```

### Comparing `discoger-2.1.0/README.md` & `discoger-2.1.1/README.md`

 * *Files identical despite different names*

### Comparing `discoger-2.1.0/discoger/client.py` & `discoger-2.1.1/discoger/client.py`

 * *Files 8% similar despite different names*

```diff
@@ -49,43 +49,48 @@
         logger.setLevel(self.log_level)
 
         self.commands = {  # command description used in the "help" command
             "/start": "Get used to the bot",
             "/help": "Gives you information about the available commands",
             "/list": "Show all items in your following list",
             "/delete": "Delete item from the following list",
+            "/wantlist": "Synchronize Discogs wantlist to following list",
             "https://www.discogs.com/release|master/.*": "Add release or master release in following list (ex: https://www.discogs.com/release/26741825)",
         }
+        self.options = {  # command description used in the "help" command
+            "/start": "Get used to the bot"
+        }
 
         try:
             self.d = discogs_client.Client("DiscogsAlert/0.1", user_token=self.secret)
             self.me = self.d.identity()
         except discogs_client.exceptions.HTTPError as e:
             logging.error("Error: Unable to authenticate.")
             raise SystemExit(e)
 
         @self.bot.message_handler(commands=["help", "start"])
         def send_welcome(message):
             chat_id = message.chat.id
             msg = "Hi there, I am Discoger bot"
-            db = YamlDB(filename="%s/%s.yaml" % (self.database_dir, self.home, chat_id))
+            db = YamlDB(filename="%s/%s.yaml" % (self.database_dir, chat_id))
             if not db.get("release_list"):
                 db["release_list"] = list()
                 db["chat_id"] = chat_id
                 db.save()
             self.bot.reply_to(message, msg)
             process_hi_step(chat_id)
 
         def process_hi_step(chat_id):
             markup = types.ReplyKeyboardMarkup()
             itembtna = types.KeyboardButton("/help")
             itembtnb = types.KeyboardButton("/check")
             itembtnc = types.KeyboardButton("/list")
             itembtnd = types.KeyboardButton("/delete")
-            markup.row(itembtna, itembtnb)
+            itembtne = types.KeyboardButton("/wantlist")
+            markup.row(itembtna, itembtnb, itembtne)
             markup.row(itembtnc, itembtnd)
             help_text = "What do you want?\n"
             for key in self.commands:
                 help_text += key + " "
                 help_text += self.commands[key] + "\n"
             self.bot.send_message(
                 chat_id, help_text, reply_markup=markup, disable_web_page_preview=True
@@ -123,15 +128,15 @@
                 self.bot.send_message(
                     chat_id, "%s is already in following list" % (release_id)
                 )
 
         @self.bot.message_handler(commands=["list"])
         def get_list(message):
             chat_id = message.chat.id
-            db = YamlDB(filename="%s/%s.yaml" % (self.database_dir, self.home, chat_id))
+            db = YamlDB(filename="%s/%s.yaml" % (self.database_dir, chat_id))
             if not db.get("release_list"):
                 self.bot.send_message(
                     chat_id,
                     "Your discoger following list is empty, send me a url first",
                 )
             else:
                 id_list = 0
@@ -188,30 +193,27 @@
             username = message.text
             db = YamlDB(filename="%s/%s.yaml" % (self.database_dir, chat_id))
             try:
                 user_info = self.d.user(username)
                 for i in user_info.wantlist:
                     release_info = self.d.release(i.id)
                     if not db.search("release_list[?release_id=='%s']" % (i.id)):
-                        release = scrap.DiscogerInfo(release_info.url, self.d, str(i.id))
+                        release = scrap.DiscogerInfo(
+                            release_info.url, self.d, str(i.id)
+                        )
                         db["release_list"].append(release.release_info)
                         db.save()
                         logging.info("Item %s added in following list" % (i.id))
                     else:
                         logging.info("Item %s already in your following list" % (i.id))
-                self.bot.send_message(
-                    chat_id, "Your wantlist is synchronized"
-                )
+                self.bot.send_message(chat_id, "Your wantlist is synchronized")
                 if not db.get("wantlist_user"):
                     db["wantlist_user"] = username
             except discogs_client.exceptions.DiscogsAPIError as e:
-                self.bot.send_message(
-                    chat_id, "Error, %s" % e
-                )
-
+                self.bot.send_message(chat_id, "Error, %s" % e)
 
         def check_discogs(chat_id=None):
             if chat_id:
                 logging.info("Check user list %s" % (chat_id))
                 db = YamlDB(filename="%s/%s.yaml" % (self.database_dir, chat_id))
                 utils.scrap_data(self, chat_id, db)
             else:
```

### Comparing `discoger-2.1.0/discoger/scrap.py` & `discoger-2.1.1/discoger/scrap.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from bs4 import BeautifulSoup
 import requests
 import re
+import logging
 
 
 class DiscogsScraper:
     def __init__(self, url, d):
         headers = {"User-Agent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_1)"}
         req = requests.get(url, headers=headers)
         soup = BeautifulSoup(req.text, "html.parser")
@@ -43,15 +44,15 @@
     @property
     def suggestion_price(self) -> str:
         _info = self.d.release(self.release_id)
         try:
             value = _info.price_suggestions.mint.value
             currency = _info.price_suggestions.mint.currency
             return "%s %s" % (round(value, 2), currency)
-        except:
+        except Exception:
             return "Unknow"
 
 
 class DiscogerInfo:
     def __init__(self, url, d, release_id):
         self.url = url
         self.discogs = d
@@ -63,18 +64,24 @@
 
         self.release_id = release_id
 
     @property
     def release_info(self) -> dict:
         release_info = dict()
         if self.media_type == "master":
-            master_release_info = self.discogs.master(self.release_id)
-            all_info = self.discogs.release(master_release_info.main_release.id)
+            try:
+                master_release_info = self.discogs.master(self.release_id)
+                all_info = self.discogs.release(master_release_info.main_release.id)
+            except self.d.exceptions.DiscogsAPIError as e:
+                logging.error("Error, %s" % e)
         else:
-            all_info = self.discogs.release(self.release_id)
+            try:
+                all_info = self.discogs.release(self.release_id)
+            except self.d.exceptions.DiscogsAPIError as e:
+                logging.error("Error, %s" % e)
         release_info["release_id"] = self.release_id
         release_info["artist"] = all_info.artists[0].name
         release_info["title"] = all_info.title
         release_info["url"] = self.url
         release_info["type"] = self.media_type
         release_info["image"] = all_info.images[0]["uri"]
         release_info["last_sell"] = dict()
```

### Comparing `discoger-2.1.0/discoger/utils.py` & `discoger-2.1.1/discoger/utils.py`

 * *Files identical despite different names*

### Comparing `discoger-2.1.0/discoger.egg-info/PKG-INFO` & `discoger-2.1.1/discoger.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: discoger
-Version: 2.1.0
+Version: 2.1.1
 Summary: Get notification from Discogs
 Home-page: https://github.com/beudbeud/discoger
 Author: Beudbeud
 Author-email: beudbeud@gmail.com
 License: GNU General Public License v3 (GPLv3)
-Download-URL: https://github.com/beudbeud/discoger/archive/2.1.0.tar.gz
+Download-URL: https://github.com/beudbeud/discoger/archive/2.1.1.tar.gz
 Description: # Discoger
         
         Discoger Bot is a Telegram bot that allows you to be notified when a new sale for a vinyl in your Discogs wantlist is available.
         
         ## Usage
         
         1. Search for the Telegram bot "Discoger" or click [this link](https://t.me/Discogers_bot) to open a conversation with the bot.
```

### Comparing `discoger-2.1.0/setup.py` & `discoger-2.1.1/setup.py`

 * *Files identical despite different names*

