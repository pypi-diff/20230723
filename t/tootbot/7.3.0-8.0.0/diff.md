# Comparing `tmp/tootbot-7.3.0.tar.gz` & `tmp/tootbot-8.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tootbot-7.3.0.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
+gzip compressed data, was "tootbot-8.0.0.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
```

## Comparing `tootbot-7.3.0.tar` & `tootbot-8.0.0.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0     4489 2023-07-13 06:21:13.997566 tootbot-7.3.0/README.rst
--rw-r--r--   0        0        0     3772 2023-07-13 06:21:14.001566 tootbot-7.3.0/pyproject.toml
--rw-r--r--   0        0        0      752 2023-07-13 06:21:14.001566 tootbot-7.3.0/src/tootbot/__init__.py
--rw-r--r--   0        0        0     7692 2023-07-13 06:21:14.001566 tootbot-7.3.0/src/tootbot/app.py
--rw-r--r--   0        0        0    32863 2023-07-13 06:21:14.001566 tootbot-7.3.0/src/tootbot/collect.py
--rw-r--r--   0        0        0    19177 2023-07-13 06:21:14.001566 tootbot-7.3.0/src/tootbot/control.py
--rw-r--r--   0        0        0     4877 2023-07-13 06:21:14.001566 tootbot-7.3.0/src/tootbot/create_config.py
--rw-r--r--   0        0        0     4603 2023-07-13 06:21:14.001566 tootbot-7.3.0/src/tootbot/debug.py
--rw-r--r--   0        0        0     2472 2023-07-13 06:21:14.001566 tootbot-7.3.0/src/tootbot/monitoring.py
--rw-r--r--   0        0        0    16491 2023-07-13 06:21:14.001566 tootbot-7.3.0/src/tootbot/publish.py
--rw-r--r--   0        0        0     6314 1970-01-01 00:00:00.000000 tootbot-7.3.0/PKG-INFO
+-rw-r--r--   0        0        0     4488 2023-07-23 09:31:42.136361 tootbot-8.0.0/README.rst
+-rw-r--r--   0        0        0     3817 2023-07-23 09:31:42.144362 tootbot-8.0.0/pyproject.toml
+-rw-r--r--   0        0        0      752 2023-07-23 09:31:42.144362 tootbot-8.0.0/src/tootbot/__init__.py
+-rw-r--r--   0        0        0     7954 2023-07-23 09:31:42.144362 tootbot-8.0.0/src/tootbot/app.py
+-rw-r--r--   0        0        0    34549 2023-07-23 09:31:42.144362 tootbot-8.0.0/src/tootbot/collect.py
+-rw-r--r--   0        0        0    19673 2023-07-23 09:31:42.144362 tootbot-8.0.0/src/tootbot/control.py
+-rw-r--r--   0        0        0     5434 2023-07-23 09:31:42.148362 tootbot-8.0.0/src/tootbot/create_config.py
+-rw-r--r--   0        0        0     4603 2023-07-23 09:31:42.148362 tootbot-8.0.0/src/tootbot/debug.py
+-rw-r--r--   0        0        0     2472 2023-07-23 09:31:42.148362 tootbot-8.0.0/src/tootbot/monitoring.py
+-rw-r--r--   0        0        0    16491 2023-07-23 09:31:42.148362 tootbot-8.0.0/src/tootbot/publish.py
+-rw-r--r--   0        0        0     6366 1970-01-01 00:00:00.000000 tootbot-8.0.0/PKG-INFO
```

### Comparing `tootbot-7.3.0/README.rst` & `tootbot-8.0.0/README.rst`

 * *Files 6% similar despite different names*

```diff
@@ -29,28 +29,28 @@
 
 **!!! Tootbot no longer supports posting to Twitter. !!!**
 
 If you need twitter functionality look into `reddit-twitter-bot`_ as a possible alternative.
 
 **!!! Tootbot no longer supports deleting old toots. !!!**
 
-If you'd like to delete older toots from your Mastodon account look into `MastodonAmnesia`_ as a tool that might
+If you'd like to delete older toots from your Mastodon account look into `Fedinesia`_ as a tool that might
 work for you.
 
 Disclaimer
 ----------
 
 The developers of Tootbot hold no liability for what you do with this script or what happens to you by using this
 script. Abusing this script *can* get you banned from Mastodon, so make sure to read up on proper usage of the API
 for each site.
 
 Setup and usage
 ---------------
 
-For instructions on setting up and using Tootbot, please visit `the wiki`_
+For instructions on setting up and using Tootbot, please look at `the documentation`_
 
 Supporting Tootbot
 ------------------
 
 There are a number of ways you can support Tootbot:
 
 - Create an issue with problems or ideas you have with/for Tootboot
@@ -70,18 +70,18 @@
 
 Tootbot is licences under the `GNU General Public License v3.0`_
 
 
 
 .. _Mastodon: https://joinmastodon.org/
 .. _reddit-twitter-bot: https://github.com/rhiever/reddit-twitter-bot
-.. _MastodonAmnesia: https://pypi.org/project/mastodonamnesia/
+.. _Fedinesia: https://pypi.org/project/fedinesia/
 .. _@babyelephantgifs: https://botsin.space/@babyelephantgifs
 .. _Healthchecks: https://healthchecks.io/
-.. _the wiki: https://codeberg.org/MarvinsMastodonTools/tootbot/wiki
+.. _the documentation: https://marvinsmastodontools.codeberg.page/tootbot/
 .. _buy me a coffee: https://www.buymeacoffee.com/marvin8
 .. _GNU General Public License v3.0: http://www.gnu.org/licenses/agpl-3.0.html
 .. _Changelog: https://codeberg.org/MarvinsMastodonTools/tootbot/src/branch/main/CHANGELOG.rst
 
 .. |GPL| image:: https://www.gnu.org/graphics/gplv3-with-text-136x68.png
     :alt: GPL3
     :target: https://codeberg.org/MarvinsMastodonTools/tootbot/src/branch/main/license.txt
```

### Comparing `tootbot-7.3.0/pyproject.toml` & `tootbot-8.0.0/pyproject.toml`

 * *Files 3% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["flit_core >=3.2,<4"]
 build-backend = "flit_core.buildapi"
 
 [project]
 name = "tootbot"
-description = "A Python bot that looks up posts from specified subreddits and automatically posts them on Mastodon"
+description = "A Python bot that looks up posts from specified subreddits and/or redditors and automatically posts them on Mastodon"
 readme = "README.rst"
 authors = [
   { name = "marvin8", email = "marvin8@tuta.io" },
 ]
 requires-python = ">=3.8"
 license = {text = "AGPL-3.0-or-later"}
 dynamic = ["version"]
@@ -26,41 +26,42 @@
     "python-magic>=0.4.27",
     "asyncpraw>=7.7.1",
     "outdated>=0.2.2",
     "tqdm>=4.65.0",
     "aiosqlite>=0.17.0",
     "yt-dlp>=2023.7.6",
     "minimal-activitypub>=0.5.5",
+    "aiohttp>=3.8.5",
 ]
 [project.optional-dependencies]
 doc = [
     "Sphinx>=6.2.1",
     "python-docs-theme>=2023.5",
     "sphinx-rtd-theme>=1.2.2",
 ]
 dev = [
     "pre-commit>=3.3.3",
     "black>=23.7.0",
     "mypy>=1.4.1",
     "safety>=2.3.4",
     "pip-audit>=2.6.0",
-    "types-aiofiles>=23.1.0.4",
+    "types-aiofiles>=23.1.0.5",
     "interrogate>=1.5.0",
-    "ruff>=0.0.278",
+    "ruff>=0.0.280",
     "flit>=3.9.0",
 ]
 
 [project.scripts]
 tootbot = "tootbot.app:start_main"
 tootbot_create_config = "tootbot.create_config:create"
 tootbot_debug_submission = "tootbot.debug:start_debug_single_submission"
 
 [project.urls]
 Changelog = "https://codeberg.org/MarvinsMastodonTools/tootbot/src/branch/main/CHANGELOG.rst"
-Wiki = "https://codeberg.org/MarvinsMastodonTools/tootbot/wiki"
+Documentation = "https://marvinsmastodontools.codeberg.page/tootbot/"
 "Bug Tracker" = "https://codeberg.org/MarvinsMastodonTools/tootbot/issues"
 homepage = "https://codeberg.org/MarvinsMastodonTools/tootbot"
 repository = "https://codeberg.org/MarvinsMastodonTools/tootbot"
 
 [tool.interrogate]
 ignore-init-method = true
 ignore-init-module = false
```

### Comparing `tootbot-7.3.0/src/tootbot/__init__.py` & `tootbot-8.0.0/src/tootbot/__init__.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 """Package 'tootbot' level definitions."""
 import sys
 from typing import Final
 
-__version__: Final[str] = "7.3.0"
+__version__: Final[str] = "8.0.0"
 __display_name__: Final[str] = "Tootbot"
 __package_name__: Final[str] = __display_name__.lower()
 
 # Package level Static Variables
 POST_RECORDER_SQLITE_DB: Final[str] = "history.db"
 POST_RECORDER_HISTORY_RETENTION_DAYS: Final[int] = 31
 USER_AGENT: Final[str] = __display_name__
```

### Comparing `tootbot-7.3.0/src/tootbot/app.py` & `tootbot-8.0.0/src/tootbot/app.py`

 * *Files 2% similar despite different names*

```diff
@@ -65,14 +65,21 @@
         debug_log=args.debug_log_file,
     )
 
     print(f"Welcome to {__display_name__} ({__version__})")
     logger.debug("Welcome to %s (%s)", __display_name__, VERSION_DEBUG)
     check_updates()
 
+    if len(config.redditors) == 0 and len(config.subreddits) == 0:
+        logger.error(
+            "Nothing to do! Please configure at least one subreddit or redditor to follow."
+        )
+        await config.bot.post_recorder.close_db()
+        sys.exit(1)
+
     try:
         secrets = await get_secrets(config_dir=config_dir)
     except ImgurClientError as imgur_error:
         logger.error("Error on creating ImgurClient: %s", imgur_error)
         logger.error(FATAL_TOOTBOT_ERROR)
         await config.bot.post_recorder.close_db()
         sys.exit(1)
```

### Comparing `tootbot-7.3.0/src/tootbot/collect.py` & `tootbot-8.0.0/src/tootbot/collect.py`

 * *Files 4% similar despite different names*

```diff
@@ -30,15 +30,15 @@
 from tqdm.asyncio import tqdm as aiotqdm
 
 from . import PROGRESS_BAR_FORMAT
 from . import USER_AGENT
 from . import __display_name__
 from .control import Configuration
 from .control import Secret
-from .control import SubredditConfig
+from .control import SourcesConfig
 
 logger = logging.getLogger(__display_name__)
 
 RH = TypeVar("RH", bound="RedditHelper")
 LMH = TypeVar("LMH", bound="LinkedMediaHelper")
 
 
@@ -187,45 +187,83 @@
 
         reddit_con = asyncpraw.Reddit(
             user_agent=USER_AGENT,
             client_id=self.api_secret.client_id,
             client_secret=self.api_secret.client_secret,
         )
 
+        for redditor in self.config.redditors:
+            tasks.append(self.get_redditor_posts(redditor, reddit_con))
+
         for subreddit in self.config.subreddits:
-            tasks.append(self.get_reddit_posts(subreddit, reddit_con))
-        progress_title = "Processing Subreddits"
+            tasks.append(self.get_subreddit_posts(subreddit, reddit_con))
+
+        progress_title = "Processing Redditors/Subreddits"
         task_results = await aiotqdm.gather(
             *tasks,
             desc=f"{progress_title:.<60}",
             ncols=120,
             bar_format=PROGRESS_BAR_FORMAT,
             total=len(tasks),
         )
 
         for result in task_results:
             self.posts.update(result)
 
         await reddit_con.close()
 
-    async def get_reddit_posts(
+    async def get_redditor_posts(
         self: RH,
-        subreddit: SubredditConfig,
+        redditor: SourcesConfig,
+        reddit_con: asyncpraw.Reddit,
+    ) -> Dict[str, Dict[str, asyncpraw.models.Submission]]:
+        """Collect posts considered hot from configured sub/multi-reddits.
+
+        :param redditor: redditors to check for posts to x-post
+        :param reddit_con: API reference
+
+        :returns:
+        Dictionary with str of tags to use and subreddit posts
+        """
+        posts = {}
+        logger.debug("Retrieving posts from redditor %s", redditor.name)
+        try:
+            redditor_info = await reddit_con.redditor(redditor.name)
+            redditor_posts: Dict[str, asyncpraw.models.Submission] = {}
+            async for submission in redditor_info.submissions.new(
+                limit=self.config.reddit.post_limit,
+            ):
+                redditor_posts[submission.id] = submission
+            posts[redditor.tags] = redditor_posts
+        except asyncprawcore.AsyncPrawcoreException as reddit_error:
+            logger.warning(
+                "Error when getting reddit posts from u/%s: %s",
+                redditor.name,
+                reddit_error,
+            )
+
+        logger.debug("Added %s posts", len(posts))
+
+        return posts
+
+    async def get_subreddit_posts(
+        self: RH,
+        subreddit: SourcesConfig,
         reddit_con: asyncpraw.Reddit,
     ) -> Dict[str, Dict[str, asyncpraw.models.Submission]]:
         """Collect posts considered hot from configured sub/multi-reddits.
 
         :param subreddit: subreddits to check for posts to x-post
         :param reddit_con: API reference
 
         :returns:
         Dictionary with str of tags to use and subreddit posts
         """
         posts = {}
-        logger.debug("Retrieving posts from %s", subreddit.name)
+        logger.debug("Retrieving posts from subreddit %s", subreddit.name)
         try:
             subreddit_info = await reddit_con.subreddit(subreddit.name)
             subreddit_posts: Dict[str, asyncpraw.models.Submission] = {}
             async for submission in subreddit_info.hot(
                 limit=self.config.reddit.post_limit
             ):
                 subreddit_posts[submission.id] = submission
@@ -261,14 +299,20 @@
             desc=f"{title:.<60}",
             total=len(self.posts),
             ncols=120,
             bar_format=PROGRESS_BAR_FORMAT,
         ):
             post_ids = list(posts.keys())
             for id in post_ids:
+                logger.debug("checking post: %s", posts[id])
+                if posts[id].author is None:
+                    del posts[id]
+                    logger.debug("Post removed as no user info available")
+                    continue
+
                 logger.debug(
                     "RedditHelper.remove_posts_by_ignored_users() - Checking post: %s from user: %s",
                     id,
                     posts[id].author.name,
                 )
                 if str(posts[id].author.name) in self.config.ignore_users_list:
                     del posts[id]
@@ -353,14 +397,17 @@
             "submission='%s', max_len=%s, add_hash_tags='%s', promo_message='%s')",
             submission.id,
             max_len,
             add_hash_tags,
             promo_message,
         )
 
+        # Build full permalink
+        permalink = "https://reddit.com" + submission.permalink
+
         author_tag = ""
         if self.config.mastodon_config.use_redditor_tag:
             redditor: Redditor = submission.author
             # "-" breaks hashtags on Mastodon, so replace any "-" with "_"
             reddit_user = redditor.name.replace("-", "_")
             author_tag = f"posted by #u{reddit_user} "
 
@@ -378,18 +425,15 @@
 
         promo_string = ""
         if promo_message:
             promo_string = f" \n \n{self.config.promo.message}"
 
         caption_max_length = max_len
         caption_max_length -= (
-            len(submission.shortlink)
-            + len(author_tag)
-            + len(hashtag_string)
-            + len(promo_string)
+            len(permalink) + len(author_tag) + len(hashtag_string) + len(promo_string)
         )
 
         caption: str = ""
         # Create contents of the Mastodon post
         if len(submission.title) < caption_max_length:
             temp_caption = submission.title + " "
         else:
@@ -401,15 +445,15 @@
         if self.config.mastodon_config.use_tags:
             caption += hashtag_string
 
         if self.config.mastodon_config.use_backlink:
             if self.config.mastodon_config.link_to_media:
                 caption += submission.url
             else:
-                caption += submission.shortlink
+                caption += permalink
         caption += promo_string
 
         return caption
 
 
 class LinkedMediaHelper:
     """Helper class providing methods to get media attachments."""
```

### Comparing `tootbot-7.3.0/src/tootbot/control.py` & `tootbot-8.0.0/src/tootbot/control.py`

 * *Files 2% similar despite different names*

```diff
@@ -8,14 +8,15 @@
 from logging import getLogger
 from logging.handlers import TimedRotatingFileHandler
 from sqlite3 import OperationalError
 from typing import Any
 from typing import Final
 from typing import List
 from typing import Optional
+from typing import Tuple
 from typing import Type
 from typing import TypeVar
 from typing import Union
 
 import aiosqlite
 import arrow
 from minimal_activitypub import __display_name__ as minimal_activitypub_logger
@@ -340,28 +341,29 @@
     use_tags: bool
     use_backlink: bool
     link_to_media: bool
     use_redditor_tag: bool
 
 
 @dataclass
-class SubredditConfig:
+class SourcesConfig:
     """Dataclass to hold configuration settings about the subreddits to be monitored."""
 
     name: str
     tags: str
 
 
 @dataclass
 class Configuration:
     """Dataclass to hold all settings for tootbot."""
 
     # pylint: disable-msg=too-many-locals
     bot: BotConfig
-    subreddits: List[SubredditConfig]
+    subreddits: List[SourcesConfig]
+    redditors: List[SourcesConfig]
     promo: PromoConfig
     health: HealthCheckConfig
     media: MediaConfig
     mastodon_config: MastodonConfig
     reddit: RedditReaderConfig
     ignore_users_list: List[str]
 
@@ -440,40 +442,51 @@
             use_tags=config["Mastodon"].getboolean("UseTags", fallback=True),
             use_backlink=config["Mastodon"].getboolean("UseBacklink", fallback=True),
             link_to_media=config["Mastodon"].getboolean("MediaLink", fallback=False),
             use_redditor_tag=config["Mastodon"].getboolean(
                 "UseRedditorTag", fallback=False
             ),
         )
-        subreddits = await Configuration._load_subreddits_settings(config)
+        subreddits, redditors = Configuration._load_sources_settings(config)
 
         ignore_users_list = Configuration._load_ignore_users_list(config)
 
         configuration = cls(
             bot=bot,
             subreddits=subreddits,
+            redditors=redditors,
             promo=promo,
             health=health,
             media=media,
             mastodon_config=mastodon_config,
             reddit=reddit,
             ignore_users_list=ignore_users_list,
         )
         logger.debug("After loading of config: %s", configuration)
         return configuration
 
     @staticmethod
-    async def _load_subreddits_settings(
+    def _load_sources_settings(
         config: configparser.ConfigParser,
-    ) -> List[SubredditConfig]:
-        """Load Subreddit configuration options."""
+    ) -> Tuple[List[SourcesConfig], List[SourcesConfig]]:
+        """Load Subreddit configuration options.
+
+        returns: tuple of two lists. First a list of Subreddits, and second a list of Redditors to follow
+        """
         subreddits = []
-        for subreddit, hashtags in config.items("Subreddits"):
-            subreddits.append(SubredditConfig(subreddit, hashtags.strip()))
-        return subreddits
+        if config.has_section("Subreddits"):
+            for subreddit, hashtags in config.items("Subreddits"):
+                subreddits.append(SourcesConfig(subreddit, hashtags.strip()))
+
+        redditors = []
+        if config.has_section("Redditors"):
+            for redditor, hashtags in config.items("Redditors"):
+                redditors.append(SourcesConfig(redditor, hashtags.strip()))
+
+        return subreddits, redditors
 
     @staticmethod
     def _load_ignore_users_list(
         config: configparser.ConfigParser,
     ) -> List[str]:
         """Load ignore_users_list."""
         ignore_users: List[str] = []
```

### Comparing `tootbot-7.3.0/src/tootbot/create_config.py` & `tootbot-8.0.0/src/tootbot/create_config.py`

 * *Files 5% similar despite different names*

```diff
@@ -46,14 +46,34 @@
 # (e.g. hashtag1, hashtag2)
 [Subreddits]
 cats: cats
 kittens+bodegacats: cats, kittens, bodegcats
 dogs: dogs
 puppies+goodboy: dogs, puppies, goodboy
 
+# Name of redditors (reddit users) to follow and take posts from
+# lines in the Redditors section are formatted as:
+# username: hashtags
+# hashtags can be one or multiple hashtags separated by commas without the "#" symbol
+# (e.g. hashtag1, hashtag2)
+[Redditors]
+Sunkisty: variety
+
+# Name of redditors (reddit users) to skip / ignore
+# lines in the IgnoreUsersList section are formatted as:
+# username:
+# the trailing colon (":") is important!
+[IgnoreUsersList]
+toughgetsgoing:
+Turbulent-Egg-9222:
+Time_Comfortable8644:
+YouHaveANiceName:
+Humble_Dumbbell:
+
+
 # Settings related to promotional messages
 [PromoSettings]
 # How often should the promotional message be added
 # Setting is for a promotional message to be added every x messages
 # I.e. 0 = no promotional messages added ever
 #      1 = promotional message added to every new post
 #      2 = promotional message added to every 2nd new post
```

### Comparing `tootbot-7.3.0/src/tootbot/debug.py` & `tootbot-8.0.0/src/tootbot/debug.py`

 * *Files identical despite different names*

### Comparing `tootbot-7.3.0/src/tootbot/monitoring.py` & `tootbot-8.0.0/src/tootbot/monitoring.py`

 * *Files identical despite different names*

### Comparing `tootbot-7.3.0/src/tootbot/publish.py` & `tootbot-8.0.0/src/tootbot/publish.py`

 * *Files identical despite different names*

### Comparing `tootbot-7.3.0/PKG-INFO` & `tootbot-8.0.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: tootbot
-Version: 7.3.0
-Summary: A Python bot that looks up posts from specified subreddits and automatically posts them on Mastodon
+Version: 8.0.0
+Summary: A Python bot that looks up posts from specified subreddits and/or redditors and automatically posts them on Mastodon
 Author-email: marvin8 <marvin8@tuta.io>
 Requires-Python: >=3.8
 Description-Content-Type: text/x-rst
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Classifier: Environment :: Console
 Classifier: Intended Audience :: Developers
@@ -15,29 +15,30 @@
 Requires-Dist: python-magic>=0.4.27
 Requires-Dist: asyncpraw>=7.7.1
 Requires-Dist: outdated>=0.2.2
 Requires-Dist: tqdm>=4.65.0
 Requires-Dist: aiosqlite>=0.17.0
 Requires-Dist: yt-dlp>=2023.7.6
 Requires-Dist: minimal-activitypub>=0.5.5
+Requires-Dist: aiohttp>=3.8.5
 Requires-Dist: pre-commit>=3.3.3 ; extra == "dev"
 Requires-Dist: black>=23.7.0 ; extra == "dev"
 Requires-Dist: mypy>=1.4.1 ; extra == "dev"
 Requires-Dist: safety>=2.3.4 ; extra == "dev"
 Requires-Dist: pip-audit>=2.6.0 ; extra == "dev"
-Requires-Dist: types-aiofiles>=23.1.0.4 ; extra == "dev"
+Requires-Dist: types-aiofiles>=23.1.0.5 ; extra == "dev"
 Requires-Dist: interrogate>=1.5.0 ; extra == "dev"
-Requires-Dist: ruff>=0.0.278 ; extra == "dev"
+Requires-Dist: ruff>=0.0.280 ; extra == "dev"
 Requires-Dist: flit>=3.9.0 ; extra == "dev"
 Requires-Dist: Sphinx>=6.2.1 ; extra == "doc"
 Requires-Dist: python-docs-theme>=2023.5 ; extra == "doc"
 Requires-Dist: sphinx-rtd-theme>=1.2.2 ; extra == "doc"
 Project-URL: Bug Tracker, https://codeberg.org/MarvinsMastodonTools/tootbot/issues
 Project-URL: Changelog, https://codeberg.org/MarvinsMastodonTools/tootbot/src/branch/main/CHANGELOG.rst
-Project-URL: Wiki, https://codeberg.org/MarvinsMastodonTools/tootbot/wiki
+Project-URL: Documentation, https://marvinsmastodontools.codeberg.page/tootbot/
 Project-URL: homepage, https://codeberg.org/MarvinsMastodonTools/tootbot
 Project-URL: repository, https://codeberg.org/MarvinsMastodonTools/tootbot
 Provides-Extra: dev
 Provides-Extra: doc
 
 Tootbot
 =======
@@ -70,28 +71,28 @@
 
 **!!! Tootbot no longer supports posting to Twitter. !!!**
 
 If you need twitter functionality look into `reddit-twitter-bot`_ as a possible alternative.
 
 **!!! Tootbot no longer supports deleting old toots. !!!**
 
-If you'd like to delete older toots from your Mastodon account look into `MastodonAmnesia`_ as a tool that might
+If you'd like to delete older toots from your Mastodon account look into `Fedinesia`_ as a tool that might
 work for you.
 
 Disclaimer
 ----------
 
 The developers of Tootbot hold no liability for what you do with this script or what happens to you by using this
 script. Abusing this script *can* get you banned from Mastodon, so make sure to read up on proper usage of the API
 for each site.
 
 Setup and usage
 ---------------
 
-For instructions on setting up and using Tootbot, please visit `the wiki`_
+For instructions on setting up and using Tootbot, please look at `the documentation`_
 
 Supporting Tootbot
 ------------------
 
 There are a number of ways you can support Tootbot:
 
 - Create an issue with problems or ideas you have with/for Tootboot
@@ -111,18 +112,18 @@
 
 Tootbot is licences under the `GNU General Public License v3.0`_
 
 
 
 .. _Mastodon: https://joinmastodon.org/
 .. _reddit-twitter-bot: https://github.com/rhiever/reddit-twitter-bot
-.. _MastodonAmnesia: https://pypi.org/project/mastodonamnesia/
+.. _Fedinesia: https://pypi.org/project/fedinesia/
 .. _@babyelephantgifs: https://botsin.space/@babyelephantgifs
 .. _Healthchecks: https://healthchecks.io/
-.. _the wiki: https://codeberg.org/MarvinsMastodonTools/tootbot/wiki
+.. _the documentation: https://marvinsmastodontools.codeberg.page/tootbot/
 .. _buy me a coffee: https://www.buymeacoffee.com/marvin8
 .. _GNU General Public License v3.0: http://www.gnu.org/licenses/agpl-3.0.html
 .. _Changelog: https://codeberg.org/MarvinsMastodonTools/tootbot/src/branch/main/CHANGELOG.rst
 
 .. |GPL| image:: https://www.gnu.org/graphics/gplv3-with-text-136x68.png
     :alt: GPL3
     :target: https://codeberg.org/MarvinsMastodonTools/tootbot/src/branch/main/license.txt
```

