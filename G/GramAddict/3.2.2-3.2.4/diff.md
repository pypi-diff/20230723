# Comparing `tmp/gramaddict-3.2.2.tar.gz` & `tmp/GramAddict-3.2.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gramaddict-3.2.2.tar", last modified: Thu Apr 28 08:26:39 2022, max compression
+gzip compressed data, was "GramAddict-3.2.4.tar", last modified: Fri Mar 31 15:05:33 2023, max compression
```

## Comparing `gramaddict-3.2.2.tar` & `GramAddict-3.2.4.tar`

### file list

```diff
@@ -1,55 +1,68 @@
-drwxrwxrwx   0        0        0        0 2022-04-28 08:26:39.124951 gramaddict-3.2.2/
-drwxrwxrwx   0        0        0        0 2022-04-28 08:26:38.960659 gramaddict-3.2.2/GramAddict/
--rw-rw-rw-   0        0        0       97 2021-10-24 18:47:51.000000 gramaddict-3.2.2/GramAddict/__init__.py
--rw-rw-rw-   0        0        0     4568 2022-04-28 08:25:07.000000 gramaddict-3.2.2/GramAddict/__main__.py
-drwxrwxrwx   0        0        0        0 2022-04-28 08:26:39.040932 gramaddict-3.2.2/GramAddict/core/
--rw-rw-rw-   0        0        0        0 2021-10-24 18:47:51.000000 gramaddict-3.2.2/GramAddict/core/__init__.py
--rw-rw-rw-   0        0        0    16294 2022-03-23 18:19:12.000000 gramaddict-3.2.2/GramAddict/core/bot_flow.py
--rw-rw-rw-   0        0        0     8508 2022-03-02 19:12:11.000000 gramaddict-3.2.2/GramAddict/core/config.py
--rw-rw-rw-   0        0        0     4989 2022-03-17 10:00:06.000000 gramaddict-3.2.2/GramAddict/core/decorators.py
--rw-rw-rw-   0        0        0    27605 2022-04-28 08:17:35.000000 gramaddict-3.2.2/GramAddict/core/device_facade.py
--rw-rw-rw-   0        0        0    10261 2021-10-24 18:47:51.000000 gramaddict-3.2.2/GramAddict/core/download_from_github.py
--rw-rw-rw-   0        0        0    32226 2022-04-28 08:25:07.000000 gramaddict-3.2.2/GramAddict/core/filter.py
--rw-rw-rw-   0        0        0    34151 2022-03-17 18:30:12.000000 gramaddict-3.2.2/GramAddict/core/handle_sources.py
--rw-rw-rw-   0        0        0    39031 2022-03-25 18:49:35.000000 gramaddict-3.2.2/GramAddict/core/interaction.py
--rw-rw-rw-   0        0        0     4721 2022-03-09 12:00:11.000000 gramaddict-3.2.2/GramAddict/core/log.py
--rw-rw-rw-   0        0        0     5278 2022-03-17 10:03:19.000000 gramaddict-3.2.2/GramAddict/core/navigation.py
--rw-rw-rw-   0        0        0     1679 2021-10-24 18:47:51.000000 gramaddict-3.2.2/GramAddict/core/persistent_list.py
--rw-rw-rw-   0        0        0     1476 2022-03-14 08:50:57.000000 gramaddict-3.2.2/GramAddict/core/plugin_loader.py
--rw-rw-rw-   0        0        0     8327 2021-11-09 18:26:39.000000 gramaddict-3.2.2/GramAddict/core/report.py
--rw-rw-rw-   0        0        0    13643 2022-03-17 11:04:08.000000 gramaddict-3.2.2/GramAddict/core/resources.py
--rw-rw-rw-   0        0        0     2299 2021-05-04 13:37:32.000000 gramaddict-3.2.2/GramAddict/core/scroll_end_detector.py
--rw-rw-rw-   0        0        0    12779 2022-02-06 10:50:10.000000 gramaddict-3.2.2/GramAddict/core/session_state.py
--rw-rw-rw-   0        0        0     9274 2022-04-28 08:25:07.000000 gramaddict-3.2.2/GramAddict/core/storage.py
--rw-rw-rw-   0        0        0    27226 2022-04-28 08:25:07.000000 gramaddict-3.2.2/GramAddict/core/utils.py
--rw-rw-rw-   0        0        0    81690 2022-03-22 20:57:12.000000 gramaddict-3.2.2/GramAddict/core/views.py
-drwxrwxrwx   0        0        0        0 2022-04-28 08:26:39.097944 gramaddict-3.2.2/GramAddict/plugins/
--rw-rw-rw-   0        0        0        0 2021-10-24 18:47:51.000000 gramaddict-3.2.2/GramAddict/plugins/__init__.py
--rw-rw-rw-   0        0        0    23735 2022-03-25 18:47:17.000000 gramaddict-3.2.2/GramAddict/plugins/action_unfollow_followers.py
--rw-rw-rw-   0        0        0      838 2022-03-09 22:57:16.000000 gramaddict-3.2.2/GramAddict/plugins/cloned_app.py
--rw-rw-rw-   0        0        0    15871 2022-03-17 10:03:31.000000 gramaddict-3.2.2/GramAddict/plugins/core_arguments.py
--rw-rw-rw-   0        0        0     1685 2022-03-14 08:22:49.000000 gramaddict-3.2.2/GramAddict/plugins/data_analytics.py
--rw-rw-rw-   0        0        0     8632 2022-02-03 15:46:32.000000 gramaddict-3.2.2/GramAddict/plugins/interact_blogger.py
--rw-rw-rw-   0        0        0     6768 2022-02-03 15:46:32.000000 gramaddict-3.2.2/GramAddict/plugins/interact_blogger_followers.py
--rw-rw-rw-   0        0        0     6143 2022-02-03 15:46:32.000000 gramaddict-3.2.2/GramAddict/plugins/interact_blogger_post_likers.py
--rw-rw-rw-   0        0        0     4495 2022-01-31 18:58:24.000000 gramaddict-3.2.2/GramAddict/plugins/interact_feed.py
--rw-rw-rw-   0        0        0     6671 2022-01-31 18:58:24.000000 gramaddict-3.2.2/GramAddict/plugins/interact_hashtag_likers.py
--rw-rw-rw-   0        0        0     6238 2022-01-31 18:58:24.000000 gramaddict-3.2.2/GramAddict/plugins/interact_hashtag_posts.py
--rw-rw-rw-   0        0        0     6407 2022-01-31 18:58:24.000000 gramaddict-3.2.2/GramAddict/plugins/interact_place_likers.py
--rw-rw-rw-   0        0        0     5950 2022-01-31 18:58:24.000000 gramaddict-3.2.2/GramAddict/plugins/interact_place_posts.py
--rw-rw-rw-   0        0        0     5757 2022-03-17 18:30:34.000000 gramaddict-3.2.2/GramAddict/plugins/like_from_urls.py
--rw-rw-rw-   0        0        0     4693 2022-03-23 09:49:19.000000 gramaddict-3.2.2/GramAddict/plugins/remove_followers.py
--rw-rw-rw-   0        0        0     9838 2022-03-14 08:25:10.000000 gramaddict-3.2.2/GramAddict/plugins/telegram.py
--rw-rw-rw-   0        0        0       23 2022-04-28 08:24:28.000000 gramaddict-3.2.2/GramAddict/version.py
--rw-rw-rw-   0        0        0     1176 2021-05-04 13:37:32.000000 gramaddict-3.2.2/LICENSE
--rw-rw-rw-   0        0        0    18224 2022-04-28 08:26:39.121950 gramaddict-3.2.2/PKG-INFO
--rw-rw-rw-   0        0        0    17390 2022-03-14 08:22:49.000000 gramaddict-3.2.2/README.md
-drwxrwxrwx   0        0        0        0 2022-04-28 08:26:39.118950 gramaddict-3.2.2/gramaddict.egg-info/
--rw-rw-rw-   0        0        0    18224 2022-04-28 08:26:38.000000 gramaddict-3.2.2/gramaddict.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1547 2022-04-28 08:26:38.000000 gramaddict-3.2.2/gramaddict.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-04-28 08:26:38.000000 gramaddict-3.2.2/gramaddict.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       57 2022-04-28 08:26:38.000000 gramaddict-3.2.2/gramaddict.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      219 2022-04-28 08:26:38.000000 gramaddict-3.2.2/gramaddict.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2022-04-28 08:26:38.000000 gramaddict-3.2.2/gramaddict.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2022-04-28 08:26:39.124951 gramaddict-3.2.2/setup.cfg
--rw-rw-rw-   0        0        0     1566 2022-03-14 09:23:44.000000 gramaddict-3.2.2/setup.py
+-rw-r--r--   0        0        0      932 2021-10-24 18:47:51.335476 GramAddict-3.2.4/.github/ISSUE_TEMPLATE/bug_report.md
+-rw-r--r--   0        0        0      261 2021-05-04 13:37:31.942538 GramAddict-3.2.4/.github/ISSUE_TEMPLATE/feature_request.md
+-rw-r--r--   0        0        0     1396 2021-05-04 13:37:31.943504 GramAddict-3.2.4/.github/PULL_REQUEST_TEMPLATE.md
+-rw-r--r--   0        0        0     1087 2023-03-31 10:37:06.276749 GramAddict-3.2.4/.github/workflows/code-checker.yml
+-rw-r--r--   0        0        0     2417 2021-11-08 10:09:45.577515 GramAddict-3.2.4/.github/workflows/codeql-analysis.yml
+-rw-r--r--   0        0        0      226 2022-07-04 16:03:49.371025 GramAddict-3.2.4/.gitignore
+-rw-r--r--   0        0        0    15007 2023-03-31 08:26:38.871891 GramAddict-3.2.4/CHANGELOG.md
+-rw-r--r--   0        0        0     3369 2021-05-06 22:39:30.226271 GramAddict-3.2.4/CODE_OF_CONDUCT.md
+-rw-r--r--   0        0        0    14716 2022-03-14 08:22:49.622426 GramAddict-3.2.4/CONTRIBUTING.md
+-rw-r--r--   0        0        0      474 2021-06-24 07:58:48.344937 GramAddict-3.2.4/DEPLOYMENT.MD
+-rw-r--r--   0        0        0      131 2021-10-24 18:47:51.338481 GramAddict-3.2.4/FUNDING.yml
+-rw-r--r--   0        0        0      220 2023-03-31 10:37:57.780914 GramAddict-3.2.4/GramAddict/__init__.py
+-rw-r--r--   0        0        0     5035 2023-03-31 10:38:00.827614 GramAddict-3.2.4/GramAddict/__main__.py
+-rw-r--r--   0        0        0        0 2023-03-31 09:31:32.145486 GramAddict-3.2.4/GramAddict/core/__init__.py
+-rw-r--r--   0        0        0    16308 2023-03-31 10:38:00.867129 GramAddict-3.2.4/GramAddict/core/bot_flow.py
+-rw-r--r--   0        0        0     8508 2023-03-31 08:26:38.874887 GramAddict-3.2.4/GramAddict/core/config.py
+-rw-r--r--   0        0        0     4989 2023-03-31 08:26:38.876408 GramAddict-3.2.4/GramAddict/core/decorators.py
+-rw-r--r--   0        0        0    27907 2023-03-31 08:26:38.878389 GramAddict-3.2.4/GramAddict/core/device_facade.py
+-rw-r--r--   0        0        0    10261 2021-10-24 18:47:51.345812 GramAddict-3.2.4/GramAddict/core/download_from_github.py
+-rw-r--r--   0        0        0    32222 2023-03-31 08:26:38.879885 GramAddict-3.2.4/GramAddict/core/filter.py
+-rw-r--r--   0        0        0    34149 2023-03-31 08:51:17.563696 GramAddict-3.2.4/GramAddict/core/handle_sources.py
+-rw-r--r--   0        0        0    39031 2023-03-31 08:26:38.883388 GramAddict-3.2.4/GramAddict/core/interaction.py
+-rw-r--r--   0        0        0     4721 2022-03-09 12:00:11.136459 GramAddict-3.2.4/GramAddict/core/log.py
+-rw-r--r--   0        0        0     5278 2023-03-31 08:26:38.884893 GramAddict-3.2.4/GramAddict/core/navigation.py
+-rw-r--r--   0        0        0     1679 2021-10-24 18:47:51.351817 GramAddict-3.2.4/GramAddict/core/persistent_list.py
+-rw-r--r--   0        0        0     1474 2023-03-31 08:51:17.219619 GramAddict-3.2.4/GramAddict/core/plugin_loader.py
+-rw-r--r--   0        0        0     8327 2022-06-13 17:55:01.565606 GramAddict-3.2.4/GramAddict/core/report.py
+-rw-r--r--   0        0        0    13643 2023-03-31 08:26:38.887895 GramAddict-3.2.4/GramAddict/core/resources.py
+-rw-r--r--   0        0        0     2299 2023-03-31 08:26:38.889393 GramAddict-3.2.4/GramAddict/core/scroll_end_detector.py
+-rw-r--r--   0        0        0    12779 2022-07-04 16:03:49.382028 GramAddict-3.2.4/GramAddict/core/session_state.py
+-rw-r--r--   0        0        0     9328 2023-03-31 08:26:38.890894 GramAddict-3.2.4/GramAddict/core/storage.py
+-rw-r--r--   0        0        0    26580 2023-03-31 10:38:00.889629 GramAddict-3.2.4/GramAddict/core/utils.py
+-rw-r--r--   0        0        0    82166 2023-03-31 08:51:18.686596 GramAddict-3.2.4/GramAddict/core/views.py
+-rw-r--r--   0        0        0        0 2021-10-24 18:47:51.358823 GramAddict-3.2.4/GramAddict/plugins/__init__.py
+-rw-r--r--   0        0        0    23733 2023-03-31 08:51:17.978814 GramAddict-3.2.4/GramAddict/plugins/action_unfollow_followers.py
+-rw-r--r--   0        0        0      838 2023-03-31 08:26:38.897393 GramAddict-3.2.4/GramAddict/plugins/cloned_app.py
+-rw-r--r--   0        0        0    15871 2023-03-31 08:26:38.898396 GramAddict-3.2.4/GramAddict/plugins/core_arguments.py
+-rw-r--r--   0        0        0     1685 2023-03-31 08:26:38.899901 GramAddict-3.2.4/GramAddict/plugins/data_analytics.py
+-rw-r--r--   0        0        0     8628 2023-03-31 08:51:17.675236 GramAddict-3.2.4/GramAddict/plugins/interact_blogger.py
+-rw-r--r--   0        0        0     6768 2023-03-31 08:26:38.902908 GramAddict-3.2.4/GramAddict/plugins/interact_blogger_followers.py
+-rw-r--r--   0        0        0     6143 2023-03-31 08:26:38.904410 GramAddict-3.2.4/GramAddict/plugins/interact_blogger_post_likers.py
+-rw-r--r--   0        0        0     4493 2023-03-31 08:51:17.848276 GramAddict-3.2.4/GramAddict/plugins/interact_feed.py
+-rw-r--r--   0        0        0     6671 2023-03-31 08:26:38.906409 GramAddict-3.2.4/GramAddict/plugins/interact_hashtag_likers.py
+-rw-r--r--   0        0        0     6238 2023-03-31 08:26:38.907909 GramAddict-3.2.4/GramAddict/plugins/interact_hashtag_posts.py
+-rw-r--r--   0        0        0     6407 2023-03-31 08:26:38.908909 GramAddict-3.2.4/GramAddict/plugins/interact_place_likers.py
+-rw-r--r--   0        0        0     5950 2023-03-31 08:26:38.909911 GramAddict-3.2.4/GramAddict/plugins/interact_place_posts.py
+-rw-r--r--   0        0        0     5757 2023-03-31 08:26:38.911410 GramAddict-3.2.4/GramAddict/plugins/like_from_urls.py
+-rw-r--r--   0        0        0     1763 2022-01-31 18:58:24.984231 GramAddict-3.2.4/GramAddict/plugins/plugin.example
+-rw-r--r--   0        0        0     4693 2023-03-31 08:26:38.912908 GramAddict-3.2.4/GramAddict/plugins/remove_followers.py
+-rw-r--r--   0        0        0     9838 2023-03-31 08:26:38.913911 GramAddict-3.2.4/GramAddict/plugins/telegram.py
+-rw-r--r--   0        0        0     1176 2021-05-04 13:37:32.038234 GramAddict-3.2.4/LICENSE
+-rw-r--r--   0        0        0    18349 2023-03-31 08:26:38.916908 GramAddict-3.2.4/README.md
+-rw-r--r--   0        0        0       20 2022-07-04 16:03:49.395031 GramAddict-3.2.4/config-examples/blacklist.txt
+-rw-r--r--   0        0        0      238 2022-07-04 16:03:49.395031 GramAddict-3.2.4/config-examples/comments_list.txt
+-rw-r--r--   0        0        0     4691 2023-03-31 08:26:38.918914 GramAddict-3.2.4/config-examples/config.yml
+-rw-r--r--   0        0        0     1835 2022-07-04 16:03:49.398031 GramAddict-3.2.4/config-examples/filters.yml
+-rw-r--r--   0        0        0       60 2022-07-04 16:03:49.398031 GramAddict-3.2.4/config-examples/pm_list.txt
+-rw-r--r--   0        0        0      366 2022-07-04 16:03:49.399032 GramAddict-3.2.4/config-examples/telegram.yml
+-rw-r--r--   0        0        0       20 2022-07-04 16:03:49.400032 GramAddict-3.2.4/config-examples/whitelist.txt
+-rw-r--r--   0        0        0     1140 2023-03-31 11:25:11.827023 GramAddict-3.2.4/pyproject.toml
+-rw-r--r--   0        0        0      196 2023-03-31 10:38:18.258180 GramAddict-3.2.4/requirements.txt
+-rw-r--r--   0        0        0  3860582 2021-05-04 13:37:32.077298 GramAddict-3.2.4/res/demo.gif
+-rw-r--r--   0        0        0    15262 2021-05-04 13:37:32.079252 GramAddict-3.2.4/res/discord.png
+-rw-r--r--   0        0        0   365778 2022-01-31 18:58:25.006703 GramAddict-3.2.4/res/logo.png
+-rw-r--r--   0        0        0    57713 2021-10-24 18:47:51.377840 GramAddict-3.2.4/res/telegram-reports.png
+-rw-r--r--   0        0        0     2933 2021-06-24 07:58:48.362941 GramAddict-3.2.4/res/telegram.png
+-rw-r--r--   0        0        0       39 2021-06-23 18:00:06.888488 GramAddict-3.2.4/run.py
+-rw-r--r--   0        0        0    19339 1970-01-01 00:00:00.000000 GramAddict-3.2.4/PKG-INFO
```

### Comparing `gramaddict-3.2.2/GramAddict/__main__.py` & `GramAddict-3.2.4/GramAddict/__main__.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import argparse
 from os import getcwd, path
 
+from GramAddict import __version__
 from GramAddict.core.bot_flow import start_bot
 from GramAddict.core.download_from_github import download_from_github
-from GramAddict.version import __version__
 
 
 def cmd_init(args):
     if args.account_name is not None:
         print(f"Script launched in {getcwd()}, files will be available there.")
         for username in args.account_name:
             if not path.exists("./run.py"):
@@ -43,18 +43,21 @@
 def cmd_dump(args):
     import os
     import shutil
     import time
 
     import uiautomator2 as u2
     from colorama import Fore, Style
-    
-    if "--no-kill" not in args:
+
+    if not args.no_kill:
         os.popen("adb shell pkill atx-agent").close()
-    d = u2.connect()
+    try:
+        d = u2.connect(args.device)
+    except RuntimeError as err:
+        raise SystemExit(err)
 
     def dump_hierarchy(device, path):
         xml_dump = device.dump_hierarchy()
         with open(path, "w", encoding="utf-8") as outfile:
             outfile.write(xml_dump)
 
     def make_archive(name):
@@ -96,14 +99,27 @@
             dict(args=["--config"], nargs="?", help="provide the config.yml path"),
         ],
     ),
     dict(
         action=cmd_dump,
         command="dump",
         help="dump current screen",
+        flags=[
+            dict(
+                args=["--device"],
+                nargs=None,
+                default=None,
+                help="provide the device name if more then one connected",
+            ),
+            dict(
+                args=["--no-kill"],
+                action="store_true",
+                help="don't kill the uia2 demon",
+            ),
+        ],
     ),
 ]
 
 
 def main() -> None:
     parser = argparse.ArgumentParser(
         prog="GramAddict",
```

### Comparing `gramaddict-3.2.2/GramAddict/core/bot_flow.py` & `GramAddict-3.2.4/GramAddict/core/bot_flow.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 import logging
 import random
 from datetime import datetime, timedelta
 from time import sleep
 
 from colorama import Fore, Style
 
+from GramAddict import __tested_ig_version__
 from GramAddict.core.config import Config
 from GramAddict.core.device_facade import create_device, get_device_info
 from GramAddict.core.filter import Filter
 from GramAddict.core.filter import load_config as load_filter
 from GramAddict.core.interaction import load_config as load_interaction
 from GramAddict.core.log import (
     configure_logger,
@@ -45,16 +46,14 @@
     show_ending_conditions,
     stop_bot,
     wait_for_next_session,
 )
 from GramAddict.core.views import AccountView, ProfileView, TabBarView, UniversalActions
 from GramAddict.core.views import load_config as load_views
 
-TESTED_IG_VERSION = "226.1.0.16.117"
-
 
 def start_bot(**kwargs):
     # Logging initialization
     logger = logging.getLogger(__name__)
 
     # Pre-Load Config
     configs = Config(first_run=True, **kwargs)
@@ -146,18 +145,18 @@
 
         logger.info("Device screen ON and unlocked.")
         if open_instagram(device):
             try:
                 running_ig_version = get_instagram_version()
                 logger.info(f"Instagram version: {running_ig_version}")
                 if tuple(running_ig_version.split(".")) > tuple(
-                    TESTED_IG_VERSION.split(".")
+                    __tested_ig_version__.split(".")
                 ):
                     logger.info(
-                        f"You have a newer version of IG then the one tested! (Tested version: {TESTED_IG_VERSION}). That shouldn't be a problem.",
+                        f"You have a newer version of IG then the one tested! (Tested version: {__tested_ig_version__}). That shouldn't be a problem.",
                         extra={"color": f"{Style.BRIGHT}"},
                     )
             except Exception as e:
                 logger.error(f"Error retrieving the IG version. Exception: {e}")
 
             UniversalActions.close_keyboard(device)
         else:
```

### Comparing `gramaddict-3.2.2/GramAddict/core/config.py` & `GramAddict-3.2.4/GramAddict/core/config.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/core/decorators.py` & `GramAddict-3.2.4/GramAddict/core/decorators.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/core/device_facade.py` & `GramAddict-3.2.4/GramAddict/core/device_facade.py`

 * *Files 1% similar despite different names*

```diff
@@ -123,18 +123,18 @@
             view = self.deviceV2(**kwargs)
             if index is not None and view.count > 1:
                 view = self.deviceV2(**kwargs)[index]
         except uiautomator2.JSONRPCError as e:
             raise DeviceFacade.JsonRpcError(e)
         return DeviceFacade.View(view=view, device=self.deviceV2)
 
-    def back(self):
+    def back(self, modulable: bool = True):
         logger.debug("Press back button.")
         self.deviceV2.press("back")
-        random_sleep()
+        random_sleep(modulable=modulable)
 
     def start_screenrecord(self, output="debug_0000.mp4", fps=20):
         import imageio
 
         def _run_MOD(self):
             from collections import deque
 
@@ -628,14 +628,21 @@
 
         def get_property(self, prop: str):
             try:
                 return self.viewV2.info[prop]
             except uiautomator2.JSONRPCError as e:
                 raise DeviceFacade.JsonRpcError(e)
 
+        def is_scrollable(self):
+            try:
+                if self.viewV2.exists():
+                    return self.viewV2.info["scrollable"]
+            except uiautomator2.JSONRPCError as e:
+                raise DeviceFacade.JsonRpcError(e)
+
         @staticmethod
         def get_ui_timeout(ui_timeout: Timeout) -> int:
             ui_timeout = Timeout.ZERO if ui_timeout is None else ui_timeout
             if ui_timeout == Timeout.ZERO:
                 ui_timeout = 0
             elif ui_timeout == Timeout.TINY:
                 ui_timeout = 1
```

### Comparing `gramaddict-3.2.2/GramAddict/core/download_from_github.py` & `GramAddict-3.2.4/GramAddict/core/download_from_github.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/core/filter.py` & `GramAddict-3.2.4/GramAddict/core/filter.py`

 * *Files 0% similar despite different names*

```diff
@@ -192,16 +192,16 @@
                     )
                     return False
         else:
             logger.debug("filters.yml not loaded!")
             return True
 
     def return_check_profile(self, username, profile_data, skip_reason=None) -> bool:
-        # if self.storage is not None:
-        #     self.storage.add_filter_user(username, profile_data, skip_reason)
+        if self.storage is not None:
+            self.storage.add_filter_user(username, profile_data, skip_reason)
 
         return skip_reason is not None
 
     def check_profile(self, device, username):
         """
         This method assumes being on someone's profile already.
         """
```

### Comparing `gramaddict-3.2.2/GramAddict/core/handle_sources.py` & `GramAddict-3.2.4/GramAddict/core/handle_sources.py`

 * *Files 0% similar despite different names*

```diff
@@ -720,15 +720,14 @@
         screen_skipped_followers_count = 0
         scroll_end_detector.notify_new_page()
         user_list = device.find(
             resourceIdMatches=self.ResourceID.USER_LIST_CONTAINER,
         )
         row_height, n_users = inspect_current_view(user_list)
         try:
-
             for item in user_list:
                 cur_row_height = item.get_height()
                 if cur_row_height < row_height:
                     continue
                 user_info_view = item.child(index=1)
                 user_name_view = user_info_view.child(index=0).child()
                 if not user_name_view.exists():
```

### Comparing `gramaddict-3.2.2/GramAddict/core/interaction.py` & `GramAddict-3.2.4/GramAddict/core/interaction.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/core/log.py` & `GramAddict-3.2.4/GramAddict/core/log.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/core/navigation.py` & `GramAddict-3.2.4/GramAddict/core/navigation.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/core/persistent_list.py` & `GramAddict-3.2.4/GramAddict/core/persistent_list.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/core/plugin_loader.py` & `GramAddict-3.2.4/GramAddict/core/plugin_loader.py`

 * *Files 2% similar despite different names*

```diff
@@ -35,12 +35,12 @@
 
         for _, pluginname, ispkg in pkgutil.iter_modules(
             imported_package.__path__, f"{imported_package.__name__}."
         ):
             if not ispkg:
                 plugin_module = __import__(pluginname, fromlist=["plugins"])
                 clsmembers = inspect.getmembers(plugin_module, inspect.isclass)
-                for (_, c) in clsmembers:
+                for _, c in clsmembers:
                     if issubclass(c, Plugin) & (c is not Plugin):
                         if self.output:
                             logger.info(f"  - {c.__name__}: {c.__doc__}")
                         self.plugins.append(c())
```

### Comparing `gramaddict-3.2.2/GramAddict/core/report.py` & `GramAddict-3.2.4/GramAddict/core/report.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/core/resources.py` & `GramAddict-3.2.4/GramAddict/core/resources.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/core/scroll_end_detector.py` & `GramAddict-3.2.4/GramAddict/core/scroll_end_detector.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/core/session_state.py` & `GramAddict-3.2.4/GramAddict/core/session_state.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/core/storage.py` & `GramAddict-3.2.4/GramAddict/core/storage.py`

 * *Files 2% similar despite different names*

```diff
@@ -128,16 +128,19 @@
         if user is None:
             return FollowingStatus.NOT_IN_LIST
         else:
             return FollowingStatus[user[USER_FOLLOWING_STATUS].upper()]
 
     def add_filter_user(self, username, profile_data, skip_reason=None):
         user = profile_data.__dict__
-        user["follow_button_text"] = None if profile_data.is_restricted else profile_data.follow_button_text.name
-
+        user["follow_button_text"] = (
+            profile_data.follow_button_text.name
+            if not profile_data.is_restricted
+            else None
+        )
         user["skip_reason"] = None if skip_reason is None else skip_reason.name
         self.history_filter_users[username] = user
         if self.history_filter_users_path is not None:
             with atomic_write(
                 self.history_filter_users_path, overwrite=True, encoding="utf-8"
             ) as outfile:
                 json.dump(self.history_filter_users, outfile, indent=4, sort_keys=False)
```

### Comparing `gramaddict-3.2.2/GramAddict/core/utils.py` & `GramAddict-3.2.4/GramAddict/core/utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,25 +14,25 @@
 from random import randint, shuffle, uniform
 from subprocess import PIPE
 from time import sleep
 from typing import Optional, Tuple, Union
 from urllib.parse import urlparse
 
 import emoji
+import requests
 import urllib3
 from colorama import Fore, Style
-from requests import get
+from packaging.version import parse as parse_version
 
-from GramAddict import __file__
+from GramAddict import __file__, __version__
 from GramAddict.core.config import Config
 from GramAddict.core.log import get_log_file_config
 from GramAddict.core.report import print_full_report
 from GramAddict.core.resources import ResourceID as resources
 from GramAddict.core.storage import ACCOUNTS
-from GramAddict.version import __version__
 
 http = urllib3.PoolManager()
 logger = logging.getLogger(__name__)
 
 
 def load_config(config: Config):
     global app_id
@@ -42,62 +42,44 @@
     app_id = config.args.app_id
     args = config.args
     configs = config
     ResourceID = resources(app_id)
 
 
 def update_available():
-    urllib3.disable_warnings()
-    if "b" not in __version__:
-        version_request = "https://raw.githubusercontent.com/GramAddict/bot/master/GramAddict/version.py"
-    else:
-        version_request = "https://raw.githubusercontent.com/GramAddict/bot/develop/GramAddict/version.py"
-    try:
-        r = get(version_request, verify=True)
-        online_version_raw = r.text.split('"')[1]
+    response = requests.get("https://pypi.python.org/pypi/gramaddict/json")
+    if response.ok:
+        latest_version = response.json()["info"]["version"]
 
-    except Exception as e:
-        logger.error(
-            f"There was an error retrieving the latest version of GramAddict: {e}"
-        )
-        return False, False
-    if "b" not in __version__:
-        local_version = __version__.split(".")
-        online_version = online_version_raw.split(".")
+        current_version = parse_version(__version__)
+        latest_version = parse_version(latest_version)
+
+        return current_version < latest_version, latest_version
     else:
-        local_version = __version__.split(".")[:-1] + __version__.split(".")[-1].split(
-            "b"
-        )
-        online_version = online_version_raw.split(".")[:-1] + online_version_raw.split(
-            "."
-        )[-1].split("b")
-    for n in range(len(online_version)):
-        if int(online_version[n]) > int(local_version[n]):
-            return True, online_version_raw
-        if int(online_version[n]) == int(local_version[n]):
-            continue
-        break
-    return False, online_version_raw
+        return False, None
 
 
 def check_if_updated(crash=False):
     if not crash:
         logger.info("Checking for updates...")
-    new_update, version = update_available()
+    new_update, latest_version = update_available()
     if new_update:
         logger.warning("NEW VERSION FOUND!")
         logger.warning(
-            f"Version {version} has been released! Please update so that you can get all the latest features and bugfixes. Changelog here -> https://github.com/GramAddict/bot/blob/master/CHANGELOG.md"
+            f"Version {latest_version} has been released! Please update so that you can get all the latest features and bugfixes. Changelog here -> https://github.com/GramAddict/bot/blob/master/CHANGELOG.md"
         )
         logger.warning("HOW TO UPDATE:")
         logger.warning("If you installed with pip: pip3 install GramAddict -U")
         logger.warning("If you installed with git: git pull")
         sleep(5)
+    elif latest_version is None:
+        logger.error("Unable to get latest version from pypi!")
     elif not crash:
         logger.info("Bot is updated.", extra={"color": f"{Style.BRIGHT}"})
+
     if not crash:
         logger.info(
             f"GramAddict v.{__version__}",
             extra={"color": f"{Style.BRIGHT}{Fore.MAGENTA}"},
         )
 
 
@@ -223,24 +205,29 @@
     """
     cmd: str = f"adb{'' if configs.device_id is None else ' -s ' + configs.device_id} shell settings put global heads_up_notifications_enabled {0 if not enabled else 1}"
     return subprocess.run(cmd, stdout=PIPE, stderr=PIPE, shell=True, encoding="utf8")
 
 
 def check_screen_timeout():
     MIN_TIMEOUT = 5 * 6_000
-    cmd: str = f"adb{'' if configs.device_id is None else ' -s ' + configs.device_id} shell settings get system screen_off_timeout"
+    cmd: str = f"adb{'' if configs.device_id is None else f' -s {configs.device_id}'} shell settings get system screen_off_timeout"
     resp = subprocess.run(cmd, stdout=PIPE, stderr=PIPE, shell=True, encoding="utf8")
-    if int(resp.stdout.lstrip()) < MIN_TIMEOUT:
-        logger.info(
-            f"Setting timeout of the screen to {MIN_TIMEOUT/6_000:.0f} minutes."
-        )
-        cmd: str = f"adb{'' if configs.device_id is None else ' -s ' + configs.device_id} shell settings put system screen_off_timeout {MIN_TIMEOUT}"
-        subprocess.run(cmd, stdout=PIPE, stderr=PIPE, shell=True, encoding="utf8")
-    else:
-        logger.info("Screen timeout is fine!")
+    try:
+        if int(resp.stdout.lstrip()) < MIN_TIMEOUT:
+            logger.info(
+                f"Setting timeout of the screen to {MIN_TIMEOUT/6_000:.0f} minutes."
+            )
+            cmd: str = f"adb{'' if configs.device_id is None else f' -s {configs.device_id}'} shell settings put system screen_off_timeout {MIN_TIMEOUT}"
+
+            subprocess.run(cmd, stdout=PIPE, stderr=PIPE, shell=True, encoding="utf8")
+        else:
+            logger.info("Screen timeout is fine!")
+    except ValueError:
+        logger.info("Unable to get screen timeout!")
+        logger.debug(resp.stdout)
 
 
 def open_instagram(device):
     nl = "\n"
     FastInputIME = "com.github.uiautomator/.FastInputIME"
     logger.info("Open Instagram app.")
 
@@ -560,42 +547,40 @@
     )
     return False
 
 
 def get_value(
     count: str,
     name: Optional[str],
-    default: Union[int, float] = 0,
+    default: Optional[Union[int, float]] = 0,
     its_time: bool = False,
 ) -> Optional[Union[int, float]]:
     def print_error() -> None:
         logger.error(
             f'Using default value instead of "{count}", because it must be '
             "either a number (e.g. 2) or a range (e.g. 2-4)."
         )
 
     if count is None:
         return None
-    parts = count.split("-")
     try:
-        if len(parts) == 1:
-            if "." in count:
-                value = float(count)
-            else:
-                value = int(count)
-        elif len(parts) == 2:
+        if "." in count:
+            value = float(count)
+        else:
+            value = int(count)
+    except ValueError:
+        parts = count.split("-")
+        if len(parts) == 2:
             if not its_time:
                 value = randint(int(parts[0]), int(parts[1]))
             else:
                 value = round(uniform(int(parts[0]), int(parts[1])), 2)
         else:
-            raise ValueError
-    except ValueError:
-        value = default
-        print_error()
+            value = default
+            print_error()
     if name is not None:
         logger.info(name.format(value), extra={"color": Style.BRIGHT})
     return value
 
 
 def validate_url(x) -> bool:
     try:
```

### Comparing `gramaddict-3.2.2/GramAddict/core/views.py` & `GramAddict-3.2.4/GramAddict/core/views.py`

 * *Files 2% similar despite different names*

```diff
@@ -1054,30 +1054,42 @@
                 logger.info(
                     f"You are already logged as {username}!",
                     extra={"color": f"{Style.BRIGHT}{Fore.BLUE}"},
                 )
                 return True
             logger.debug(f"You're logged as {current_profile_name.strip()}")
             action_bar.click()
-            found_obj = self.device.find(
-                resourceId=ResourceID.ROW_USER_TEXTVIEW,
-                textMatches=case_insensitive_re(username),
-            )
-            if found_obj.exists(Timeout.SHORT):
-                logger.info(
-                    f"Switching to {username}...",
-                    extra={"color": f"{Style.BRIGHT}{Fore.BLUE}"},
-                )
-                found_obj.click()
-                random_sleep()
-                action_bar = ProfileView._getActionBarTitleBtn(self)
+            if self._find_username(username):
                 if action_bar is not None:
                     current_profile_name = action_bar.get_text()
                     if current_profile_name.strip().upper() == username.upper():
                         return True
+                else:
+                    logger.error(
+                        "Cannot find action bar (where you select your account)!"
+                    )
+        return False
+
+    def _find_username(self, username, has_scrolled=False):
+        list_view = self.device.find(resourceId=ResourceID.LIST)
+        username_obj = self.device.find(
+            resourceId=ResourceID.ROW_USER_TEXTVIEW,
+            textMatches=case_insensitive_re(username),
+        )
+        if username_obj.exists(Timeout.SHORT):
+            logger.info(
+                f"Switching to {username}...",
+                extra={"color": f"{Style.BRIGHT}{Fore.BLUE}"},
+            )
+            username_obj.click()
+            return True
+        elif list_view.is_scrollable() and not has_scrolled:
+            logger.debug("User list is scrollable.")
+            list_view.scroll(Direction.DOWN)
+            self._find_username(username, has_scrolled=True)
         return False
 
     def refresh_account(self):
         textview = self.device.find(
             resourceIdMatches=ResourceID.ROW_PROFILE_HEADER_TEXTVIEW_POST_CONTAINER
         )
         universal_actions = UniversalActions(self.device)
@@ -1660,15 +1672,14 @@
                     if n == 3 or not last_lin_layout.child(index=n).exists():
                         if n == 3:
                             return last_index, 0
                         else:
                             return last_index - 1, n
 
     def getProfileInfo(self):
-
         username = self.getUsername()
         posts = self.getPostsCount()
         followers = self.getFollowersCount()
         following = self.getFollowingCount()
 
         return username, posts, followers, following
```

### Comparing `gramaddict-3.2.2/GramAddict/plugins/action_unfollow_followers.py` & `GramAddict-3.2.4/GramAddict/plugins/action_unfollow_followers.py`

 * *Files 0% similar despite different names*

```diff
@@ -206,15 +206,14 @@
         )
 
     def on_unfollow(self):
         self.state.unfollowed_count += 1
         self.session_state.totalUnfollowed += 1
 
     def sort_followings_by_date(self, device, newest_to_oldest=False) -> bool:
-
         sort_button = device.find(
             resourceId=self.ResourceID.SORTING_ENTRY_ROW_OPTION,
         )
         if not sort_button.exists(Timeout.MEDIUM):
             logger.error(
                 "Cannot find button to sort followings. Continue without sorting."
             )
```

### Comparing `gramaddict-3.2.2/GramAddict/plugins/cloned_app.py` & `GramAddict-3.2.4/GramAddict/plugins/cloned_app.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/plugins/core_arguments.py` & `GramAddict-3.2.4/GramAddict/plugins/core_arguments.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/plugins/data_analytics.py` & `GramAddict-3.2.4/GramAddict/plugins/data_analytics.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/plugins/interact_blogger.py` & `GramAddict-3.2.4/GramAddict/plugins/interact_blogger.py`

 * *Files 0% similar despite different names*

```diff
@@ -161,15 +161,14 @@
         on_interaction,
         stories_percentage,
         likes_percentage,
         follow_percentage,
         comment_percentage,
         pm_percentage,
     ):
-
         interaction = partial(
             interact_with_user,
             my_username=self.session_state.my_username,
             likes_count=self.args.likes_count,
             likes_percentage=likes_percentage,
             stories_percentage=stories_percentage,
             follow_percentage=follow_percentage,
@@ -216,15 +215,14 @@
         on_interaction,
         stories_percentage,
         likes_percentage,
         follow_percentage,
         comment_percentage,
         pm_percentage,
     ):
-
         interaction = partial(
             interact_with_user,
             my_username=self.session_state.my_username,
             likes_count=self.args.likes_count,
             likes_percentage=likes_percentage,
             stories_percentage=stories_percentage,
             follow_percentage=follow_percentage,
```

### Comparing `gramaddict-3.2.2/GramAddict/plugins/interact_blogger_followers.py` & `GramAddict-3.2.4/GramAddict/plugins/interact_blogger_followers.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/plugins/interact_blogger_post_likers.py` & `GramAddict-3.2.4/GramAddict/plugins/interact_blogger_post_likers.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/plugins/interact_feed.py` & `GramAddict-3.2.4/GramAddict/plugins/interact_feed.py`

 * *Files 0% similar despite different names*

```diff
@@ -111,15 +111,14 @@
         stories_percentage,
         likes_percentage,
         follow_percentage,
         comment_percentage,
         pm_percentage,
         interact_percentage,
     ):
-
         interaction = partial(
             interact_with_user,
             my_username=self.session_state.my_username,
             likes_count=self.args.likes_count,
             likes_percentage=likes_percentage,
             stories_percentage=stories_percentage,
             follow_percentage=follow_percentage,
```

### Comparing `gramaddict-3.2.2/GramAddict/plugins/interact_hashtag_likers.py` & `GramAddict-3.2.4/GramAddict/plugins/interact_hashtag_likers.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/plugins/interact_hashtag_posts.py` & `GramAddict-3.2.4/GramAddict/plugins/interact_hashtag_posts.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/plugins/interact_place_likers.py` & `GramAddict-3.2.4/GramAddict/plugins/interact_place_likers.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/plugins/interact_place_posts.py` & `GramAddict-3.2.4/GramAddict/plugins/interact_place_posts.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/plugins/like_from_urls.py` & `GramAddict-3.2.4/GramAddict/plugins/like_from_urls.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/plugins/remove_followers.py` & `GramAddict-3.2.4/GramAddict/plugins/remove_followers.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/GramAddict/plugins/telegram.py` & `GramAddict-3.2.4/GramAddict/plugins/telegram.py`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/LICENSE` & `GramAddict-3.2.4/LICENSE`

 * *Files identical despite different names*

### Comparing `gramaddict-3.2.2/PKG-INFO` & `GramAddict-3.2.4/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -1,27 +1,7 @@
-Metadata-Version: 2.1
-Name: gramaddict
-Version: 3.2.2
-Summary: Completely free and open source human-like Instagram bot. Powered by UIAutomator2 and compatible with basically any android device that can run instagram - real or emulated.
-Home-page: https://github.com/GramAddict/bot/
-Author: GramAddict Team
-Author-email: maintainers@gramaddict.org
-License: UNKNOWN
-Platform: UNKNOWN
-Classifier: Programming Language :: Python :: 3.6
-Classifier: Programming Language :: Python :: 3.7
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Operating System :: OS Independent
-Requires-Python: >=3.6
-Description-Content-Type: text/markdown
-Provides-Extra: telegram-reports
-Provides-Extra: analytics
-License-File: LICENSE
-
 <p align="center">
   <img src="https://github.com/GramAddict/bot/raw/master/res/logo.png">
   <br />
   <h1 align="center">GramAddict</h1>
   <br />
   <p align="center">Looking for Instagram automation? I'm proud to present you a <b>100% free and open source Instagram bot</b>. This bot will allow you to grow your following and engagement by liking, following, commenting and sending PM automatically with your Android phone/tablet/emulator. <b>No root required.</b> <p>
   <p align="center">
@@ -47,15 +27,15 @@
 	    <img src="https://img.shields.io/github/last-commit/GramAddict/bot/master?style=flat">
     </a>
     <a href="https://pypi.org/project/gramaddict/">
       <img src="https://img.shields.io/pypi/dm/gramaddict">
     </a>
     <a href="https://github.com/GramAddict/bot#backers">
 	    <img src="https://img.shields.io/opencollective/backers/gramaddict?style=flat">
-    </a>  
+    </a>
     <a href="https://discord.gg/NK8PNEFGFF">
 	    <img src="https://img.shields.io/discord/771481743471017994?style=flat">
     </a>
   </p>
 </p>
 
 <br />
@@ -76,39 +56,39 @@
     <img src="https://img.shields.io/discord/771481743471017994?style=flat">
   </a>
 
 ## I saw there are a lot of similar projects on GitHub, why should I choose this one?
 You're right, there are plenty of other bot solutions. Most of them use API requests. However, you will get your account banned if you use API (1-30 days)!
 There's also a very similar project to this one, yet it's not free and the dev doesn't care about the community much. They removed few lines from the core and ask you for a subscription plan in order to use those features. Furthermore, you don't even know what's the real code during execution - it's encrypted. And if they are stealing something else? Who knows? I don't.
 This bot is __free to use__ and __open source__, you won't get charged for few extra lines, __EVER__.
-I'm focused on the community and not on finding ways how to get money out of this project. __I really care about the community__ and every dev should too. ðŸ¤—
+I'm focused on the community and not on finding ways how to get money out of this project. __I really care about the community__ and every dev should too. 🤗
 
 ## So this bot does not use API?
 __No__ this bot is working through __adb__ and is powered by __uiautomator2__ which is a testing wrapper for Android devices. In fact, your device (or an emulator) is used for doing the botting sh*it. That's very secure compared to other botting systems around there. I also made it look as much human as possible. You can think about the bot as a __stupid__ friend using your phone and doing things for you. The example bottom is quite old but will show you what we are talking about.
 <p align="center">
   <img src="https://github.com/GramAddict/bot/raw/master/res/demo.gif">
 </p>
 
 ## Urra! I'll never get banned anymore with this bot!
-No no no, wait! ðŸ¤¦
+No no no, wait! 🤦
 You have to configure the bot for doing things as a human would do. Do you really spend all the day scrolling on Instagram? If yes contact a medic :P
-You don't have to do so many actions or Instagram will block you. That appends even if you do that by your hands.. Have you ever added a lot of people in a row and got blocked for that action? Or spamming people with a link in PM? 
+You don't have to do so many actions or Instagram will block you. That appends even if you do that by your hands.. Have you ever added a lot of people in a row and got blocked for that action? Or spamming people with a link in PM?
 __DON'T F*CKING DO THAT__
 
 __Be gently and anonymous and nobody will notice that you're botting, trust me__.
 
 ## Do I need a computer for running the bot?
 Yes, but you can also run it [directly on your phone](https://docs.gramaddict.org/#/termux)!!
 
-In any case, you can decide to use a physical device or an emulator (if you're under Windows I suggest you use [Memu](https://www.memuplay.com/)).
+In any case, you can decide to use a physical device or an emulator. If you're under Windows I suggest you use [Memu](https://www.memuplay.com/), under Mac OS we found out that [Android studio](https://developer.android.com/studio) works well (Installable with [homebrew](https://formulae.brew.sh/cask/android-studio)).
 For hosting the bot you can use:
 - your computer (with Windows, macOS, or Linux)
 - a Raspberry (which is a cheap little pc Linux based)
 
-## Cool! What can I do with this bot? 
+## Cool! What can I do with this bot?
 There are lots of __cool features__ you can use __for free__!
 - Works without rooting
 - Works with both emulators and physical devices
 - Can be used stand-alone (without the use of a computer)
 - Includes realistic random human-like delays and actions
 - Can watch stories while interacting
 - Comment post with emojis and [spintax logic](https://github.com/GramAddict/docs/blob/main/configuration.md#spintax-support)
@@ -154,15 +134,15 @@
 [Follow this guide to accomplish that](https://docs.gramaddict.org/#/configuration?id=telegram-reports).
 
 <img src="https://github.com/GramAddict/bot/raw/master/res/telegram-reports.png" width="200">
 
 > In this case trends are negative because I use this account only for tuning this bot, and it's private...
 > I didn't accept anyone lately so the trends are meh :P
 
-Cool, isn't it? ðŸ’¦
+Cool, isn't it? 💦
 # Quick start
 Now that you're there you still don't know how to install that whole thing.
 I'll try to help you accomplish that with a short tutorial. The full is available [here](https://docs.gramaddict.org/#/quickstart).
 
 ## What do you need:
 - a computer (with Windows, macOS or Linux)
 - Python installed on your machine (with pip)
@@ -186,34 +166,34 @@
 Is good practice creating virtual environments when you install a new package. That will save you from a lot of problems!
 
 #### Create a virtual environment
 We create a virtual environment called `.venv` and activate it:
 
 - create a directory where you will create the new environment
 - write in console: `python3 -m venv .venv`
-  > We use `venv` instead of `virtualenv` because `venv` is shipped directly with python3 and you don't have to install anything ðŸ¤ª
+  > We use `venv` instead of `virtualenv` because `venv` is shipped directly with python3 and you don't have to install anything 🤪
 - activate the .venv:
     - `source .venv/bin/activate` on Linux/macOS
     - `.venv\Scripts\activate.bat` on Windows cmd
     - `.venv\Scripts\activate.ps1` on Windows PowerShell
       > If you activate the venv correctly, you will see a little (.venv) on the left side of the command line!
 #### With pip (I suggest you this way):
 
 - install the package: `pip3 install GramAddict`
 - check if it's installed: `gramaddict --version`
-- if everything is fine you will get the GramAddict version installed ðŸ¥³
+- if everything is fine you will get the GramAddict version installed 🥳
 
 #### With git:
 > __Warning:__ console commands like `gramaddict init`, `gramaddict dump` and `gramaddict run` won't work if you installed the bot with git.
 - clone the project: `git clone https://github.com/GramAddict/bot.git gramaddict`
 - enter the gramaddict folder: `cd gramaddict`
 - install the requirements: `pip3 install -r requirements.txt`
 
 ### Step 3: Install adb:
-Adb stands for [Android Debug Bridge](https://developer.android.com/studio/command-line/adb). It's needed for making this bot working properly. I think this one is the hardest part to accomplish but don't give up! You can do it, with my help. ðŸ’ª
+Adb stands for [Android Debug Bridge](https://developer.android.com/studio/command-line/adb). It's needed for making this bot working properly. I think this one is the hardest part to accomplish but don't give up! You can do it, with my help. 💪
 1. download [this package](https://developer.android.com/studio/releases/platform-tools) and unzip it somewhere and remind the path
    > __Warning:__ place that where you're sure you won't ever delete it, otherwise the bot won't work anymore!
 2. add platform-tools path to the PATH environment variable
    - if you're on __Linux/macOS__ that's pretty easy:
       - open ~/.bash_profile with any text editor you like
       - add the following line with the full path to the platform-tools directory: export PATH=~/Library/Android/sdk/platform-tools/:$PATH. This path may be different depending on the way you installed platform-tools
       - save file and restart Terminal
@@ -227,27 +207,45 @@
       - press all the Ok and restart Command Prompt
 3. check that everything is fine
    - write `adb version`, you should get something like that:
       > C:\Users\dedil>adb version
       > Android Debug Bridge version 1.0.41
       > Version 30.0.5-6877874
 
-### Step 4: Start the bot:
-This bot works only if your Instagram is in [English](https://help.instagram.com/111923612310997).
+### Step 4: Set up the device:
+
+**Physical device**
+
 1. First thing you have to do is to [enable developer options and USB debugging](https://developer.android.com/studio/debug/dev-options#enable).
 2. connect your phone to your computer with a USB cable
 3. device will ask you to allow connection. Press "Connect"
-4. type `adb devices` in terminal
+
+**Emulator for Mac OS**
+
+1. Install the [Homebrew](https://brew.sh)
+2. Install the [Cask](https://cask.readthedocs.io/en/latest/index.html) by running `brew install cask`
+3. Add the Cask application folder to your `$PATH`, e.g. `echo 'export PATH="$HOME/.cask/bin:$PATH"' >> ~/.bash_profile` and open a new terminal or reload with `source ~/.bash_profile`
+4. Install the [Android Studio](https://formulae.brew.sh/cask/android-studio)
+5. Run the Android Studio and click on 'More Actions -> Virtual Device Manager', then select the device and image, I found out that Pixel 2 API 28 combo works well.
+6. Run the virtual device and install the Instagram app on it, don't forget to log in.
+
+**Verify the device with adb**
+
+Type `adb devices` in terminal
    - a list of devices attached should be displayed, if not you did something wrong
       > List of devices attached
       > A0B1CD2345678901    device
 
    - this is your device ID, you have to use it only if you have more than one device connected at the same time
-5. initialize uiautomator2: `uiautomator2 init`
-6. initialize GramAddict: `gramaddict init your_ig_account_name_here`
+
+### Step 5: Start the bot:
+
+This bot works only if your Instagram is in [English](https://help.instagram.com/111923612310997).
+1. initialize uiautomator2: `uiautomator2 init`
+2. initialize GramAddict: `gramaddict init your_ig_account_name_here`
     > __Warning:__ works only if you installed the bot with pip, if you used git you have to create account folder and youraccountname folder manually.
     - that script will crate all the files you need for configure and start this bot
     - you will find them inside the folder `accounts/youraccountname/`
       ```sh
         gramaddict/
           run.py
           accounts/
@@ -256,42 +254,42 @@
               telegram.yml
               filters.yml
               whitelist.txt
               blacklist.txt
               comments_list.txt
               pm_list.txt
       ```
-7. now that you have all the requirements you have to configure the whole thing by [following this guide](https://docs.gramaddict.org/#/configuration)
-8. now you're done, and you can finally start the bot: `python3 run.py --config accounts/yourusername/config.yml` or `gramaddict run --config accounts/yourusername/config.yml`
+3. now that you have all the requirements you have to configure the whole thing by [following this guide](https://docs.gramaddict.org/#/configuration)
+4. now you're done, and you can finally start the bot: `python3 run.py --config accounts/yourusername/config.yml` or `gramaddict run --config accounts/yourusername/config.yml`
 
 Failed? [Check this out!](https://docs.gramaddict.org/#/quickstart?id=troubleshooting)
 
 # Bot crashes, what should I do?
-The script isn't perfect and may fail sometimes. If this is the case you can open a ticket on our [discord channel](https://discord.gg/NK8PNEFGFF). In that way you won't share with anyone your Instagram account name ðŸ˜ˆ. We'll be very happy to help you!
+The script isn't perfect and may fail sometimes. If this is the case you can open a ticket on our [discord channel](https://discord.gg/NK8PNEFGFF). In that way you won't share with anyone your Instagram account name 😈. We'll be very happy to help you!
 
 # WOW! You dedicated so much time to this project! Why you did that for free??
 Well, we used to be in three a long time ago but suddenly my two friends left. This has been an opportunity for me to improve my skills in Python and that's why I didn't leave the project and keep maintaining it.
 But of course donations are very welcome, so if you think I did a great job you can buy me a beer :)
 
 
 <a  href="https://www.buymeacoffee.com/mastrolube"  target="_blank"><img  src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png"  hspace="10" alt="Buy Me A Coffee"  style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;"  ></a>
 
 # Can I do something to make this project grown?
-On GitHub there is a `star system` which indicates how good a project is. If you like this project it will be amazing if you can press the little star at the top! â­
+On GitHub there is a `star system` which indicates how good a project is. If you like this project it will be amazing if you can press the little star at the top! ⭐
 # Contributors
 
 This project exists thanks to all of our Contributors [[Contribute](https://docs.gramaddict.org/#/contributing)].
 
 <a href="https://github.com/gramaddict/bot/graphs/contributors"><img src="https://opencollective.com/gramaddict/contributors.svg?width=890&button=false" /></a>
 
 <br />
 
 # Backers
 
-Thank you to everyone that supports us financially! ðŸ™ [[Become a backer](https://opencollective.com/gramaddict#backer)]
+Thank you to everyone that supports us financially! 🙏 [[Become a backer](https://opencollective.com/gramaddict#backer)]
 
 <a href="https://opencollective.com/gramaddict#backers" target="_blank"><img src="https://opencollective.com/gramaddict/backers.svg?width=890"></a>
 <br />
 
 # Talk botty with us
 
 <p>
@@ -299,9 +297,7 @@
     <img hspace="3" alt="Join us on Discord" src="https://github.com/GramAddict/bot/raw/master/res/discord.png" height=84/>
   </a>
 </p>
 
 ---
 
 > **Disclaimer**<a name="disclaimer" />: This project comes with no guarantee or warranty. You are responsible for whatever happens from using this project. It is possible to get soft or hard banned by using this project if you are not careful.
-
-
```

#### html2text {}

```diff
@@ -1,18 +1,7 @@
-Metadata-Version: 2.1 Name: gramaddict Version: 3.2.2 Summary: Completely free
-and open source human-like Instagram bot. Powered by UIAutomator2 and
-compatible with basically any android device that can run instagram - real or
-emulated. Home-page: https://github.com/GramAddict/bot/ Author: GramAddict Team
-Author-email: maintainers@gramaddict.org License: UNKNOWN Platform: UNKNOWN
-Classifier: Programming Language :: Python :: 3.6 Classifier: Programming
-Language :: Python :: 3.7 Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9 Classifier: Operating System
-:: OS Independent Requires-Python: >=3.6 Description-Content-Type: text/
-markdown Provides-Extra: telegram-reports Provides-Extra: analytics License-
-File: LICENSE
          [https://github.com/GramAddict/bot/raw/master/res/logo.png]
                            ****** GramAddict ******
 
 Looking for Instagram automation? I'm proud to present you a 100% free and open
    source Instagram bot. This bot will allow you to grow your following and
  engagement by liking, following, commenting and sending PM automatically with
              your Android phone/tablet/emulator. No root required.
@@ -49,72 +38,75 @@
 also a very similar project to this one, yet it's not free and the dev doesn't
 care about the community much. They removed few lines from the core and ask you
 for a subscription plan in order to use those features. Furthermore, you don't
 even know what's the real code during execution - it's encrypted. And if they
 are stealing something else? Who knows? I don't. This bot is __free to use__
 and __open source__, you won't get charged for few extra lines, __EVER__. I'm
 focused on the community and not on finding ways how to get money out of this
-project. __I really care about the community__ and every dev should too.
-Ã°Å¸Â¤â ## So this bot does not use API? __No__ this bot is working through
-__adb__ and is powered by __uiautomator2__ which is a testing wrapper for
-Android devices. In fact, your device (or an emulator) is used for doing the
-botting sh*it. That's very secure compared to other botting systems around
-there. I also made it look as much human as possible. You can think about the
-bot as a __stupid__ friend using your phone and doing things for you. The
-example bottom is quite old but will show you what we are talking about.
+project. __I really care about the community__ and every dev should too. ð¤
+## So this bot does not use API? __No__ this bot is working through __adb__ and
+is powered by __uiautomator2__ which is a testing wrapper for Android devices.
+In fact, your device (or an emulator) is used for doing the botting sh*it.
+That's very secure compared to other botting systems around there. I also made
+it look as much human as possible. You can think about the bot as a __stupid__
+friend using your phone and doing things for you. The example bottom is quite
+old but will show you what we are talking about.
           [https://github.com/GramAddict/bot/raw/master/res/demo.gif]
-## Urra! I'll never get banned anymore with this bot! No no no, wait! Ã°Å¸Â¤Â¦
-You have to configure the bot for doing things as a human would do. Do you
-really spend all the day scrolling on Instagram? If yes contact a medic :P You
-don't have to do so many actions or Instagram will block you. That appends even
-if you do that by your hands.. Have you ever added a lot of people in a row and
+## Urra! I'll never get banned anymore with this bot! No no no, wait! ð¤¦ You
+have to configure the bot for doing things as a human would do. Do you really
+spend all the day scrolling on Instagram? If yes contact a medic :P You don't
+have to do so many actions or Instagram will block you. That appends even if
+you do that by your hands.. Have you ever added a lot of people in a row and
 got blocked for that action? Or spamming people with a link in PM? __DON'T
 F*CKING DO THAT__ __Be gently and anonymous and nobody will notice that you're
 botting, trust me__. ## Do I need a computer for running the bot? Yes, but you
 can also run it [directly on your phone](https://docs.gramaddict.org/#/
-termux)!! In any case, you can decide to use a physical device or an emulator
-(if you're under Windows I suggest you use [Memu](https://www.memuplay.com/)).
-For hosting the bot you can use: - your computer (with Windows, macOS, or
-Linux) - a Raspberry (which is a cheap little pc Linux based) ## Cool! What can
-I do with this bot? There are lots of __cool features__ you can use __for
-free__! - Works without rooting - Works with both emulators and physical
-devices - Can be used stand-alone (without the use of a computer) - Includes
-realistic random human-like delays and actions - Can watch stories while
-interacting - Comment post with emojis and [spintax logic](https://github.com/
-GramAddict/docs/blob/main/configuration.md#spintax-support) - Send PM - Type
-like a human (letter by letter by faking using suggestions. For example, you
-won't type `H - e - l - l - o` letter by letter but something like `H - He -
-Hello`) - Browse carousels and watch their contents - Watch videos for a
-specific amount of time - Scheduler - Getting tasty telegram reports - Supports
-multiple actions in one session - Lots of customizable limits to keep your
-account safe from soft bans - Available interactions - interact with a user's
-followers or following - interact with a top or recent hashtag's post likers -
-interact with a top or recent hashtag post - interact with a top or recent
-place's post likers - interact with a top or recent place post - interact with
-user's post likers - interact with a single blogger - interact with your feed -
-interact with users from a list (*.txt) - interact with posts from links inside
-a list (*.txt) - unfollow any followers - unfollow any followers, followed by
-bot - unfollow any followers, followed by bot, who don't follow you back -
-unfollow from a list (*.txt) - scrape mode for collecting usernames instead of
-interacting with them (you will find more information about that in the doc) -
-Lots of available filters to customize who you interact with - you can
-blacklist people to avoid interacting with them - you can whitelist people to
-not remove them when you unfollow people - biography main characters and
-language - profile name main characters - private / public / business / non
-business account - number of posts / followers / following ... and more!
+termux)!! In any case, you can decide to use a physical device or an emulator.
+If you're under Windows I suggest you use [Memu](https://www.memuplay.com/),
+under Mac OS we found out that [Android studio](https://developer.android.com/
+studio) works well (Installable with [homebrew](https://formulae.brew.sh/cask/
+android-studio)). For hosting the bot you can use: - your computer (with
+Windows, macOS, or Linux) - a Raspberry (which is a cheap little pc Linux
+based) ## Cool! What can I do with this bot? There are lots of __cool
+features__ you can use __for free__! - Works without rooting - Works with both
+emulators and physical devices - Can be used stand-alone (without the use of a
+computer) - Includes realistic random human-like delays and actions - Can watch
+stories while interacting - Comment post with emojis and [spintax logic](https:
+//github.com/GramAddict/docs/blob/main/configuration.md#spintax-support) - Send
+PM - Type like a human (letter by letter by faking using suggestions. For
+example, you won't type `H - e - l - l - o` letter by letter but something like
+`H - He - Hello`) - Browse carousels and watch their contents - Watch videos
+for a specific amount of time - Scheduler - Getting tasty telegram reports -
+Supports multiple actions in one session - Lots of customizable limits to keep
+your account safe from soft bans - Available interactions - interact with a
+user's followers or following - interact with a top or recent hashtag's post
+likers - interact with a top or recent hashtag post - interact with a top or
+recent place's post likers - interact with a top or recent place post -
+interact with user's post likers - interact with a single blogger - interact
+with your feed - interact with users from a list (*.txt) - interact with posts
+from links inside a list (*.txt) - unfollow any followers - unfollow any
+followers, followed by bot - unfollow any followers, followed by bot, who don't
+follow you back - unfollow from a list (*.txt) - scrape mode for collecting
+usernames instead of interacting with them (you will find more information
+about that in the doc) - Lots of available filters to customize who you
+interact with - you can blacklist people to avoid interacting with them - you
+can whitelist people to not remove them when you unfollow people - biography
+main characters and language - profile name main characters - private / public
+/ business / non business account - number of posts / followers / following ...
+and more!
 Full documentation available on [docs.gramaddict.org](https://
 docs.gramaddict.org) ## Telegram reports? What's that? You can get __reports__
 through telegram from your bot activities! [Follow this guide to accomplish
 that](https://docs.gramaddict.org/#/configuration?id=telegram-reports). [https:
 //github.com/GramAddict/bot/raw/master/res/telegram-reports.png] > In this case
 trends are negative because I use this account only for tuning this bot, and
 it's private... > I didn't accept anyone lately so the trends are meh :P Cool,
-isn't it? Ã°Å¸âÂ¦ # Quick start Now that you're there you still don't know
-how to install that whole thing. I'll try to help you accomplish that with a
-short tutorial. The full is available [here](https://docs.gramaddict.org/#/
+isn't it? ð¦ # Quick start Now that you're there you still don't know how to
+install that whole thing. I'll try to help you accomplish that with a short
+tutorial. The full is available [here](https://docs.gramaddict.org/#/
 quickstart). ## What do you need: - a computer (with Windows, macOS or Linux) -
 Python installed on your machine (with pip) - Adb tools - a physical device or
 an emulator (with Android 4.4+) ### Step 1: Install Python (>=3.6): >Python
 3.10 is currently not supported! If you're on Linux or macOS you should have
 Python and Git installed, just check that your Python version is >= 3.6. On
 Windows you have to [install it](https://www.python.org/downloads/release/
 python-397/) for sure. Failed? [Detailed tutorial here](https://
@@ -129,29 +121,29 @@
 Install GramAddict: You can install GramAddict in two ways: with __pip__ or
 with __git__. Is good practice creating virtual environments when you install a
 new package. That will save you from a lot of problems! #### Create a virtual
 environment We create a virtual environment called `.venv` and activate it: -
 create a directory where you will create the new environment - write in
 console: `python3 -m venv .venv` > We use `venv` instead of `virtualenv`
 because `venv` is shipped directly with python3 and you don't have to install
-anything Ã°Å¸Â¤Âª - activate the .venv: - `source .venv/bin/activate` on Linux/
+anything ð¤ª - activate the .venv: - `source .venv/bin/activate` on Linux/
 macOS - `.venv\Scripts\activate.bat` on Windows cmd -
 `.venv\Scripts\activate.ps1` on Windows PowerShell > If you activate the venv
 correctly, you will see a little (.venv) on the left side of the command line!
 #### With pip (I suggest you this way): - install the package: `pip3 install
 GramAddict` - check if it's installed: `gramaddict --version` - if everything
-is fine you will get the GramAddict version installed Ã°Å¸Â¥Â³ #### With git: >
+is fine you will get the GramAddict version installed ð¥³ #### With git: >
 __Warning:__ console commands like `gramaddict init`, `gramaddict dump` and
 `gramaddict run` won't work if you installed the bot with git. - clone the
 project: `git clone https://github.com/GramAddict/bot.git gramaddict` - enter
 the gramaddict folder: `cd gramaddict` - install the requirements: `pip3
 install -r requirements.txt` ### Step 3: Install adb: Adb stands for [Android
 Debug Bridge](https://developer.android.com/studio/command-line/adb). It's
 needed for making this bot working properly. I think this one is the hardest
-part to accomplish but don't give up! You can do it, with my help. Ã°Å¸âÂª 1.
+part to accomplish but don't give up! You can do it, with my help. ðª 1.
 download [this package](https://developer.android.com/studio/releases/platform-
 tools) and unzip it somewhere and remind the path > __Warning:__ place that
 where you're sure you won't ever delete it, otherwise the bot won't work
 anymore! 2. add platform-tools path to the PATH environment variable - if
 you're on __Linux/macOS__ that's pretty easy: - open ~/.bash_profile with any
 text editor you like - add the following line with the full path to the
 platform-tools directory: export PATH=~/Library/Android/sdk/platform-tools/:
@@ -161,53 +153,62 @@
 click "My Computer" on left side - in the pop-up menu, click `Properties` - in
 the `System Properties` window, click the `Advanced` tab, and then click
 `Environment Variables` - in the `System Variables` window, highlight `Path`,
 and click `Edit` - in the `Edit System Variables` window, press on `New` -
 enter the full path for the folder platform-tools you unzipped before - press
 all the Ok and restart Command Prompt 3. check that everything is fine - write
 `adb version`, you should get something like that: > C:\Users\dedil>adb version
-> Android Debug Bridge version 1.0.41 > Version 30.0.5-6877874 ### Step 4:
-Start the bot: This bot works only if your Instagram is in [English](https://
-help.instagram.com/111923612310997). 1. First thing you have to do is to
-[enable developer options and USB debugging](https://developer.android.com/
-studio/debug/dev-options#enable). 2. connect your phone to your computer with a
-USB cable 3. device will ask you to allow connection. Press "Connect" 4. type
-`adb devices` in terminal - a list of devices attached should be displayed, if
-not you did something wrong > List of devices attached > A0B1CD2345678901
-device - this is your device ID, you have to use it only if you have more than
-one device connected at the same time 5. initialize uiautomator2: `uiautomator2
-init` 6. initialize GramAddict: `gramaddict init your_ig_account_name_here` >
+> Android Debug Bridge version 1.0.41 > Version 30.0.5-6877874 ### Step 4: Set
+up the device: **Physical device** 1. First thing you have to do is to [enable
+developer options and USB debugging](https://developer.android.com/studio/
+debug/dev-options#enable). 2. connect your phone to your computer with a USB
+cable 3. device will ask you to allow connection. Press "Connect" **Emulator
+for Mac OS** 1. Install the [Homebrew](https://brew.sh) 2. Install the [Cask]
+(https://cask.readthedocs.io/en/latest/index.html) by running `brew install
+cask` 3. Add the Cask application folder to your `$PATH`, e.g. `echo 'export
+PATH="$HOME/.cask/bin:$PATH"' >> ~/.bash_profile` and open a new terminal or
+reload with `source ~/.bash_profile` 4. Install the [Android Studio](https://
+formulae.brew.sh/cask/android-studio) 5. Run the Android Studio and click on
+'More Actions -> Virtual Device Manager', then select the device and image, I
+found out that Pixel 2 API 28 combo works well. 6. Run the virtual device and
+install the Instagram app on it, don't forget to log in. **Verify the device
+with adb** Type `adb devices` in terminal - a list of devices attached should
+be displayed, if not you did something wrong > List of devices attached >
+A0B1CD2345678901 device - this is your device ID, you have to use it only if
+you have more than one device connected at the same time ### Step 5: Start the
+bot: This bot works only if your Instagram is in [English](https://
+help.instagram.com/111923612310997). 1. initialize uiautomator2: `uiautomator2
+init` 2. initialize GramAddict: `gramaddict init your_ig_account_name_here` >
 __Warning:__ works only if you installed the bot with pip, if you used git you
 have to create account folder and youraccountname folder manually. - that
 script will crate all the files you need for configure and start this bot - you
 will find them inside the folder `accounts/youraccountname/` ```sh gramaddict/
 run.py accounts/ youraccountname/ config.yml telegram.yml filters.yml
-whitelist.txt blacklist.txt comments_list.txt pm_list.txt ``` 7. now that you
+whitelist.txt blacklist.txt comments_list.txt pm_list.txt ``` 3. now that you
 have all the requirements you have to configure the whole thing by [following
-this guide](https://docs.gramaddict.org/#/configuration) 8. now you're done,
+this guide](https://docs.gramaddict.org/#/configuration) 4. now you're done,
 and you can finally start the bot: `python3 run.py --config accounts/
 yourusername/config.yml` or `gramaddict run --config accounts/yourusername/
 config.yml` Failed? [Check this out!](https://docs.gramaddict.org/#/
 quickstart?id=troubleshooting) # Bot crashes, what should I do? The script
 isn't perfect and may fail sometimes. If this is the case you can open a ticket
 on our [discord channel](https://discord.gg/NK8PNEFGFF). In that way you won't
-share with anyone your Instagram account name Ã°Å¸ËË. We'll be very happy to
-help you! # WOW! You dedicated so much time to this project! Why you did that
-for free?? Well, we used to be in three a long time ago but suddenly my two
-friends left. This has been an opportunity for me to improve my skills in
-Python and that's why I didn't leave the project and keep maintaining it. But
-of course donations are very welcome, so if you think I did a great job you can
-buy me a beer :) [Buy_Me_A_Coffee] # Can I do something to make this project
-grown? On GitHub there is a `star system` which indicates how good a project
-is. If you like this project it will be amazing if you can press the little
-star at the top! Ã¢Â­ # Contributors This project exists thanks to all of our
-Contributors [[Contribute](https://docs.gramaddict.org/#/contributing)].
-[https://opencollective.com/gramaddict/contributors.svg?width=890&button=false]
-
-# Backers Thank you to everyone that supports us financially! Ã°Å¸â¢ [[Become
-a backer](https://opencollective.com/gramaddict#backer)] [https://
+share with anyone your Instagram account name ð. We'll be very happy to help
+you! # WOW! You dedicated so much time to this project! Why you did that for
+free?? Well, we used to be in three a long time ago but suddenly my two friends
+left. This has been an opportunity for me to improve my skills in Python and
+that's why I didn't leave the project and keep maintaining it. But of course
+donations are very welcome, so if you think I did a great job you can buy me a
+beer :) [Buy_Me_A_Coffee] # Can I do something to make this project grown? On
+GitHub there is a `star system` which indicates how good a project is. If you
+like this project it will be amazing if you can press the little star at the
+top! â­ # Contributors This project exists thanks to all of our Contributors [
+[Contribute](https://docs.gramaddict.org/#/contributing)]. [https://
+opencollective.com/gramaddict/contributors.svg?width=890&button=false]
+# Backers Thank you to everyone that supports us financially! ð [[Become a
+backer](https://opencollective.com/gramaddict#backer)] [https://
 opencollective.com/gramaddict/backers.svg?width=890]
 # Talk botty with us
 [Join_us_on_Discord]
 --- > **Disclaimer**: This project comes with no guarantee or warranty. You are
 responsible for whatever happens from using this project. It is possible to get
 soft or hard banned by using this project if you are not careful.
```

### Comparing `gramaddict-3.2.2/README.md` & `GramAddict-3.2.4/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,285 +1,339 @@
-<p align="center">
-  <img src="https://github.com/GramAddict/bot/raw/master/res/logo.png">
-  <br />
-  <h1 align="center">GramAddict</h1>
-  <br />
-  <p align="center">Looking for Instagram automation? I'm proud to present you a <b>100% free and open source Instagram bot</b>. This bot will allow you to grow your following and engagement by liking, following, commenting and sending PM automatically with your Android phone/tablet/emulator. <b>No root required.</b> <p>
-  <p align="center">
-    <a href="https://github.com/gramaddict/bot/blob/master/LICENSE">
-      <img src="https://img.shields.io/github/license/gramaddict/bot?style=flat" />
-    </a>
-    <a href="https://www.python.org/">
-      <img src="https://img.shields.io/badge/built%20with-Python3-red.svg?style=flat" />
-    </a>
-    <a href="https://github.com/GramAddict/bot/pulls">
-      <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat" />
-    </a>
-    <a href="https://github.com/GramAddict/bot/issues">
-    	<img src="https://img.shields.io/github/issues/gramaddict/bot?style=flat" />
-    </a>
-    <a href="https://github.com/GramAddict/bot/pulls">
-      <img src="https://img.shields.io/github/issues-pr/gramaddict/bot?style=flat" />
-    </a>
-    <a href="https://github.com/GramAddict/bot/stargazers">
-	    <img src="https://img.shields.io/github/stars/gramaddict/bot?style=flat">
-    </a>
-    <a href="https://img.shields.io/github/last-commit/gramaddict/bot/master?style=flat">
-	    <img src="https://img.shields.io/github/last-commit/GramAddict/bot/master?style=flat">
-    </a>
-    <a href="https://pypi.org/project/gramaddict/">
-      <img src="https://img.shields.io/pypi/dm/gramaddict">
-    </a>
-    <a href="https://github.com/GramAddict/bot#backers">
-	    <img src="https://img.shields.io/opencollective/backers/gramaddict?style=flat">
-    </a>  
-    <a href="https://discord.gg/NK8PNEFGFF">
-	    <img src="https://img.shields.io/discord/771481743471017994?style=flat">
-    </a>
-  </p>
-</p>
-
-<br />
-
-# Why should I automate my Instagram account?
-It's very hard nowadays to grow an account. Have you ever been on the explore page? IG will show your post only to close accounts & accounts you interact most with, you will never be on the explore page. Nobody will see your beautiful photos, your hilarious memes, or whatever you are posting. But now you can do something about that! With GramAddict you can __get noticed easily__, and if you really deserve it, your account will __grow super fast__!
-
-## So, do I need to publish good content to grow?
-Of course you have to! This bot will mainly help you to get the __visibility you deserve__ and which is Instagram not giving you.
-
-## Ok but I don't know how to start this journey...
-Don't worry about that now, it's not that hard to start botting with GramAddict! I tried to make it as noob-friendly as possible. In any case, if you follow the docs with all the steps provided, you will make it! You are also invited to join our community and ask for any help!
-
-## There is a community around this project?
-Yes! We are on __discord__ and we count a lot of __active users__ you can ask us whatever you want!
-
-  <a href="https://discord.gg/NK8PNEFGFF">
-    <img src="https://img.shields.io/discord/771481743471017994?style=flat">
-  </a>
-
-## I saw there are a lot of similar projects on GitHub, why should I choose this one?
-You're right, there are plenty of other bot solutions. Most of them use API requests. However, you will get your account banned if you use API (1-30 days)!
-There's also a very similar project to this one, yet it's not free and the dev doesn't care about the community much. They removed few lines from the core and ask you for a subscription plan in order to use those features. Furthermore, you don't even know what's the real code during execution - it's encrypted. And if they are stealing something else? Who knows? I don't.
-This bot is __free to use__ and __open source__, you won't get charged for few extra lines, __EVER__.
-I'm focused on the community and not on finding ways how to get money out of this project. __I really care about the community__ and every dev should too. 🤗
-
-## So this bot does not use API?
-__No__ this bot is working through __adb__ and is powered by __uiautomator2__ which is a testing wrapper for Android devices. In fact, your device (or an emulator) is used for doing the botting sh*it. That's very secure compared to other botting systems around there. I also made it look as much human as possible. You can think about the bot as a __stupid__ friend using your phone and doing things for you. The example bottom is quite old but will show you what we are talking about.
-<p align="center">
-  <img src="https://github.com/GramAddict/bot/raw/master/res/demo.gif">
-</p>
-
-## Urra! I'll never get banned anymore with this bot!
-No no no, wait! 🤦
-You have to configure the bot for doing things as a human would do. Do you really spend all the day scrolling on Instagram? If yes contact a medic :P
-You don't have to do so many actions or Instagram will block you. That appends even if you do that by your hands.. Have you ever added a lot of people in a row and got blocked for that action? Or spamming people with a link in PM? 
-__DON'T F*CKING DO THAT__
-
-__Be gently and anonymous and nobody will notice that you're botting, trust me__.
-
-## Do I need a computer for running the bot?
-Yes, but you can also run it [directly on your phone](https://docs.gramaddict.org/#/termux)!!
-
-In any case, you can decide to use a physical device or an emulator (if you're under Windows I suggest you use [Memu](https://www.memuplay.com/)).
-For hosting the bot you can use:
-- your computer (with Windows, macOS, or Linux)
-- a Raspberry (which is a cheap little pc Linux based)
-
-## Cool! What can I do with this bot? 
-There are lots of __cool features__ you can use __for free__!
-- Works without rooting
-- Works with both emulators and physical devices
-- Can be used stand-alone (without the use of a computer)
-- Includes realistic random human-like delays and actions
-- Can watch stories while interacting
-- Comment post with emojis and [spintax logic](https://github.com/GramAddict/docs/blob/main/configuration.md#spintax-support)
-- Send PM
-- Type like a human (letter by letter by faking using suggestions. For example, you won't type `H - e - l - l - o` letter by letter but something like `H - He - Hello`)
-- Browse carousels and watch their contents
-- Watch videos for a specific amount of time
-- Scheduler
-- Getting tasty telegram reports
-- Supports multiple actions in one session
-- Lots of customizable limits to keep your account safe from soft bans
-- Available interactions
-    - interact with a user's followers or following
-    - interact with a top or recent hashtag's post likers
-    - interact with a top or recent hashtag post
-    - interact with a top or recent place's post likers
-    - interact with a top or recent place post
-    - interact with user's post likers
-    - interact with a single blogger
-    - interact with your feed
-    - interact with users from a list (*.txt)
-    - interact with posts from links inside a list (*.txt)
-    - unfollow any followers
-    - unfollow any followers, followed by bot
-    - unfollow any followers, followed by bot, who don't follow you back
-    - unfollow from a list (*.txt)
-    - scrape mode for collecting usernames instead of interacting with them (you will find more information about that in the doc)
-
-- Lots of available filters to customize who you interact with
-    - you can blacklist people to avoid interacting with them
-    - you can whitelist people to not remove them when you unfollow people
-    - biography main characters and language
-    - profile name main characters
-    - private / public / business / non business account
-    - number of posts / followers / following
-    ... and more!
-<br />
-
-Full documentation available on [docs.gramaddict.org](https://docs.gramaddict.org)
-
-## Telegram reports? What's that?
-You can get __reports__ through telegram from your bot activities!
-[Follow this guide to accomplish that](https://docs.gramaddict.org/#/configuration?id=telegram-reports).
-
-<img src="https://github.com/GramAddict/bot/raw/master/res/telegram-reports.png" width="200">
-
-> In this case trends are negative because I use this account only for tuning this bot, and it's private...
-> I didn't accept anyone lately so the trends are meh :P
-
-Cool, isn't it? 💦
-# Quick start
-Now that you're there you still don't know how to install that whole thing.
-I'll try to help you accomplish that with a short tutorial. The full is available [here](https://docs.gramaddict.org/#/quickstart).
-
-## What do you need:
-- a computer (with Windows, macOS or Linux)
-- Python installed on your machine (with pip)
-- Adb tools
-- a physical device or an emulator (with Android 4.4+)
-### Step 1: Install Python (>=3.6):
->Python 3.10 is currently not supported!
-
-If you're on Linux or macOS you should have Python and Git installed, just check that your Python version is >= 3.6.
-
-On Windows you have to [install it](https://www.python.org/downloads/release/python-397/) for sure.
-
-Failed? [Detailed tutorial here](https://docs.gramaddict.org/#/quickstart?id=step-1-install-python-if-not-installed).
->A little reminder: we refer to python with __python3__. You may also have python2 installed if you're on Linux for example. If you're on Windows you can use __python__ instead of python3.
->Check which python alias you have to use by typing `python -V` or `python3 -V` or `py -V` and use the right one for the rest of the tutorial.
-
->Check that pip3 is installed by typing `pip3 -V`
->If that returns an error you have to install it! How? [Google is your best friend!](https://www.google.com/search?q=how+to+install+pip) :P
-### Step 2: Install GramAddict:
-You can install GramAddict in two ways: with __pip__ or with __git__.
-Is good practice creating virtual environments when you install a new package. That will save you from a lot of problems!
-
-#### Create a virtual environment
-We create a virtual environment called `.venv` and activate it:
-
-- create a directory where you will create the new environment
-- write in console: `python3 -m venv .venv`
-  > We use `venv` instead of `virtualenv` because `venv` is shipped directly with python3 and you don't have to install anything 🤪
-- activate the .venv:
-    - `source .venv/bin/activate` on Linux/macOS
-    - `.venv\Scripts\activate.bat` on Windows cmd
-    - `.venv\Scripts\activate.ps1` on Windows PowerShell
-      > If you activate the venv correctly, you will see a little (.venv) on the left side of the command line!
-#### With pip (I suggest you this way):
-
-- install the package: `pip3 install GramAddict`
-- check if it's installed: `gramaddict --version`
-- if everything is fine you will get the GramAddict version installed 🥳
-
-#### With git:
-> __Warning:__ console commands like `gramaddict init`, `gramaddict dump` and `gramaddict run` won't work if you installed the bot with git.
-- clone the project: `git clone https://github.com/GramAddict/bot.git gramaddict`
-- enter the gramaddict folder: `cd gramaddict`
-- install the requirements: `pip3 install -r requirements.txt`
-
-### Step 3: Install adb:
-Adb stands for [Android Debug Bridge](https://developer.android.com/studio/command-line/adb). It's needed for making this bot working properly. I think this one is the hardest part to accomplish but don't give up! You can do it, with my help. 💪
-1. download [this package](https://developer.android.com/studio/releases/platform-tools) and unzip it somewhere and remind the path
-   > __Warning:__ place that where you're sure you won't ever delete it, otherwise the bot won't work anymore!
-2. add platform-tools path to the PATH environment variable
-   - if you're on __Linux/macOS__ that's pretty easy:
-      - open ~/.bash_profile with any text editor you like
-      - add the following line with the full path to the platform-tools directory: export PATH=~/Library/Android/sdk/platform-tools/:$PATH. This path may be different depending on the way you installed platform-tools
-      - save file and restart Terminal
-   - on __Windows__ there are more steps to accomplish that:
-      - open Windows Explorer (you can press WINKEY+E) and right-click "My Computer" on left side
-      - in the pop-up menu, click `Properties`
-      - in the `System Properties` window, click the `Advanced` tab, and then click `Environment Variables`
-      - in the `System Variables` window, highlight `Path`, and click `Edit`
-      - in the `Edit System Variables` window, press on `New`
-      - enter the full path for the folder platform-tools you unzipped before
-      - press all the Ok and restart Command Prompt
-3. check that everything is fine
-   - write `adb version`, you should get something like that:
-      > C:\Users\dedil>adb version
-      > Android Debug Bridge version 1.0.41
-      > Version 30.0.5-6877874
-
-### Step 4: Start the bot:
-This bot works only if your Instagram is in [English](https://help.instagram.com/111923612310997).
-1. First thing you have to do is to [enable developer options and USB debugging](https://developer.android.com/studio/debug/dev-options#enable).
-2. connect your phone to your computer with a USB cable
-3. device will ask you to allow connection. Press "Connect"
-4. type `adb devices` in terminal
-   - a list of devices attached should be displayed, if not you did something wrong
-      > List of devices attached
-      > A0B1CD2345678901    device
-
-   - this is your device ID, you have to use it only if you have more than one device connected at the same time
-5. initialize uiautomator2: `uiautomator2 init`
-6. initialize GramAddict: `gramaddict init your_ig_account_name_here`
-    > __Warning:__ works only if you installed the bot with pip, if you used git you have to create account folder and youraccountname folder manually.
-    - that script will crate all the files you need for configure and start this bot
-    - you will find them inside the folder `accounts/youraccountname/`
-      ```sh
-        gramaddict/
-          run.py
-          accounts/
-            youraccountname/
-              config.yml
-              telegram.yml
-              filters.yml
-              whitelist.txt
-              blacklist.txt
-              comments_list.txt
-              pm_list.txt
-      ```
-7. now that you have all the requirements you have to configure the whole thing by [following this guide](https://docs.gramaddict.org/#/configuration)
-8. now you're done, and you can finally start the bot: `python3 run.py --config accounts/yourusername/config.yml` or `gramaddict run --config accounts/yourusername/config.yml`
-
-Failed? [Check this out!](https://docs.gramaddict.org/#/quickstart?id=troubleshooting)
-
-# Bot crashes, what should I do?
-The script isn't perfect and may fail sometimes. If this is the case you can open a ticket on our [discord channel](https://discord.gg/NK8PNEFGFF). In that way you won't share with anyone your Instagram account name 😈. We'll be very happy to help you!
-
-# WOW! You dedicated so much time to this project! Why you did that for free??
-Well, we used to be in three a long time ago but suddenly my two friends left. This has been an opportunity for me to improve my skills in Python and that's why I didn't leave the project and keep maintaining it.
-But of course donations are very welcome, so if you think I did a great job you can buy me a beer :)
-
-
-<a  href="https://www.buymeacoffee.com/mastrolube"  target="_blank"><img  src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png"  hspace="10" alt="Buy Me A Coffee"  style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;"  ></a>
-
-# Can I do something to make this project grown?
-On GitHub there is a `star system` which indicates how good a project is. If you like this project it will be amazing if you can press the little star at the top! ⭐
-# Contributors
-
-This project exists thanks to all of our Contributors [[Contribute](https://docs.gramaddict.org/#/contributing)].
-
-<a href="https://github.com/gramaddict/bot/graphs/contributors"><img src="https://opencollective.com/gramaddict/contributors.svg?width=890&button=false" /></a>
-
-<br />
-
-# Backers
-
-Thank you to everyone that supports us financially! 🙏 [[Become a backer](https://opencollective.com/gramaddict#backer)]
-
-<a href="https://opencollective.com/gramaddict#backers" target="_blank"><img src="https://opencollective.com/gramaddict/backers.svg?width=890"></a>
-<br />
-
-# Talk botty with us
-
-<p>
-  <a href="https://discord.gg/NK8PNEFGFF">
-    <img hspace="3" alt="Join us on Discord" src="https://github.com/GramAddict/bot/raw/master/res/discord.png" height=84/>
-  </a>
-</p>
-
----
-
-> **Disclaimer**<a name="disclaimer" />: This project comes with no guarantee or warranty. You are responsible for whatever happens from using this project. It is possible to get soft or hard banned by using this project if you are not careful.
+Metadata-Version: 2.1
+Name: GramAddict
+Version: 3.2.4
+Summary: Human-like Instagram bot powered by UIAutomator2
+Author-email: GramAddict Team <maintainers@gramaddict.org>
+Requires-Python: >=3.6
+Description-Content-Type: text/markdown
+Classifier: License :: Free for non-commercial use
+Classifier: Operating System :: OS Independent
+Classifier: Programming Language :: Python :: 3
+Requires-Dist: colorama==0.4.4
+Requires-Dist: ConfigArgParse==1.5.3
+Requires-Dist: PyYAML==6.0
+Requires-Dist: uiautomator2==2.16.14
+Requires-Dist: urllib3==1.26.7
+Requires-Dist: emoji==1.6.1
+Requires-Dist: langdetect==1.0.9
+Requires-Dist: atomicwrites==1.4.0
+Requires-Dist: spintax==1.0.4
+Requires-Dist: requests~=2.28.2
+Requires-Dist: packaging~=20.9
+Requires-Dist: matplotlib==3.4.2 ; extra == "analytics"
+Requires-Dist: flit ; extra == "dev"
+Requires-Dist: pre-commit ; extra == "dev"
+Requires-Dist: black ; extra == "dev"
+Requires-Dist: flake8 ; extra == "dev"
+Requires-Dist: isort ; extra == "dev"
+Requires-Dist: pandas==1.2.4 ; extra == "telegram-reports"
+Requires-Dist: pytest-cov ; extra == "telegram-reports"
+Project-URL: Documentation, https://docs.gramaddict.org/#/
+Project-URL: Source, https://github.com/GramAddict/bot
+Provides-Extra: analytics
+Provides-Extra: dev
+Provides-Extra: telegram-reports
+
+<p align="center">
+  <img src="https://github.com/GramAddict/bot/raw/master/res/logo.png">
+  <br />
+  <h1 align="center">GramAddict</h1>
+  <br />
+  <p align="center">Looking for Instagram automation? I'm proud to present you a <b>100% free and open source Instagram bot</b>. This bot will allow you to grow your following and engagement by liking, following, commenting and sending PM automatically with your Android phone/tablet/emulator. <b>No root required.</b> <p>
+  <p align="center">
+    <a href="https://github.com/gramaddict/bot/blob/master/LICENSE">
+      <img src="https://img.shields.io/github/license/gramaddict/bot?style=flat" />
+    </a>
+    <a href="https://www.python.org/">
+      <img src="https://img.shields.io/badge/built%20with-Python3-red.svg?style=flat" />
+    </a>
+    <a href="https://github.com/GramAddict/bot/pulls">
+      <img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat" />
+    </a>
+    <a href="https://github.com/GramAddict/bot/issues">
+    	<img src="https://img.shields.io/github/issues/gramaddict/bot?style=flat" />
+    </a>
+    <a href="https://github.com/GramAddict/bot/pulls">
+      <img src="https://img.shields.io/github/issues-pr/gramaddict/bot?style=flat" />
+    </a>
+    <a href="https://github.com/GramAddict/bot/stargazers">
+	    <img src="https://img.shields.io/github/stars/gramaddict/bot?style=flat">
+    </a>
+    <a href="https://img.shields.io/github/last-commit/gramaddict/bot/master?style=flat">
+	    <img src="https://img.shields.io/github/last-commit/GramAddict/bot/master?style=flat">
+    </a>
+    <a href="https://pypi.org/project/gramaddict/">
+      <img src="https://img.shields.io/pypi/dm/gramaddict">
+    </a>
+    <a href="https://github.com/GramAddict/bot#backers">
+	    <img src="https://img.shields.io/opencollective/backers/gramaddict?style=flat">
+    </a>
+    <a href="https://discord.gg/NK8PNEFGFF">
+	    <img src="https://img.shields.io/discord/771481743471017994?style=flat">
+    </a>
+  </p>
+</p>
+
+<br />
+
+# Why should I automate my Instagram account?
+It's very hard nowadays to grow an account. Have you ever been on the explore page? IG will show your post only to close accounts & accounts you interact most with, you will never be on the explore page. Nobody will see your beautiful photos, your hilarious memes, or whatever you are posting. But now you can do something about that! With GramAddict you can __get noticed easily__, and if you really deserve it, your account will __grow super fast__!
+
+## So, do I need to publish good content to grow?
+Of course you have to! This bot will mainly help you to get the __visibility you deserve__ and which is Instagram not giving you.
+
+## Ok but I don't know how to start this journey...
+Don't worry about that now, it's not that hard to start botting with GramAddict! I tried to make it as noob-friendly as possible. In any case, if you follow the docs with all the steps provided, you will make it! You are also invited to join our community and ask for any help!
+
+## There is a community around this project?
+Yes! We are on __discord__ and we count a lot of __active users__ you can ask us whatever you want!
+
+  <a href="https://discord.gg/NK8PNEFGFF">
+    <img src="https://img.shields.io/discord/771481743471017994?style=flat">
+  </a>
+
+## I saw there are a lot of similar projects on GitHub, why should I choose this one?
+You're right, there are plenty of other bot solutions. Most of them use API requests. However, you will get your account banned if you use API (1-30 days)!
+There's also a very similar project to this one, yet it's not free and the dev doesn't care about the community much. They removed few lines from the core and ask you for a subscription plan in order to use those features. Furthermore, you don't even know what's the real code during execution - it's encrypted. And if they are stealing something else? Who knows? I don't.
+This bot is __free to use__ and __open source__, you won't get charged for few extra lines, __EVER__.
+I'm focused on the community and not on finding ways how to get money out of this project. __I really care about the community__ and every dev should too. 🤗
+
+## So this bot does not use API?
+__No__ this bot is working through __adb__ and is powered by __uiautomator2__ which is a testing wrapper for Android devices. In fact, your device (or an emulator) is used for doing the botting sh*it. That's very secure compared to other botting systems around there. I also made it look as much human as possible. You can think about the bot as a __stupid__ friend using your phone and doing things for you. The example bottom is quite old but will show you what we are talking about.
+<p align="center">
+  <img src="https://github.com/GramAddict/bot/raw/master/res/demo.gif">
+</p>
+
+## Urra! I'll never get banned anymore with this bot!
+No no no, wait! 🤦
+You have to configure the bot for doing things as a human would do. Do you really spend all the day scrolling on Instagram? If yes contact a medic :P
+You don't have to do so many actions or Instagram will block you. That appends even if you do that by your hands.. Have you ever added a lot of people in a row and got blocked for that action? Or spamming people with a link in PM?
+__DON'T F*CKING DO THAT__
+
+__Be gently and anonymous and nobody will notice that you're botting, trust me__.
+
+## Do I need a computer for running the bot?
+Yes, but you can also run it [directly on your phone](https://docs.gramaddict.org/#/termux)!!
+
+In any case, you can decide to use a physical device or an emulator. If you're under Windows I suggest you use [Memu](https://www.memuplay.com/), under Mac OS we found out that [Android studio](https://developer.android.com/studio) works well (Installable with [homebrew](https://formulae.brew.sh/cask/android-studio)).
+For hosting the bot you can use:
+- your computer (with Windows, macOS, or Linux)
+- a Raspberry (which is a cheap little pc Linux based)
+
+## Cool! What can I do with this bot?
+There are lots of __cool features__ you can use __for free__!
+- Works without rooting
+- Works with both emulators and physical devices
+- Can be used stand-alone (without the use of a computer)
+- Includes realistic random human-like delays and actions
+- Can watch stories while interacting
+- Comment post with emojis and [spintax logic](https://github.com/GramAddict/docs/blob/main/configuration.md#spintax-support)
+- Send PM
+- Type like a human (letter by letter by faking using suggestions. For example, you won't type `H - e - l - l - o` letter by letter but something like `H - He - Hello`)
+- Browse carousels and watch their contents
+- Watch videos for a specific amount of time
+- Scheduler
+- Getting tasty telegram reports
+- Supports multiple actions in one session
+- Lots of customizable limits to keep your account safe from soft bans
+- Available interactions
+    - interact with a user's followers or following
+    - interact with a top or recent hashtag's post likers
+    - interact with a top or recent hashtag post
+    - interact with a top or recent place's post likers
+    - interact with a top or recent place post
+    - interact with user's post likers
+    - interact with a single blogger
+    - interact with your feed
+    - interact with users from a list (*.txt)
+    - interact with posts from links inside a list (*.txt)
+    - unfollow any followers
+    - unfollow any followers, followed by bot
+    - unfollow any followers, followed by bot, who don't follow you back
+    - unfollow from a list (*.txt)
+    - scrape mode for collecting usernames instead of interacting with them (you will find more information about that in the doc)
+
+- Lots of available filters to customize who you interact with
+    - you can blacklist people to avoid interacting with them
+    - you can whitelist people to not remove them when you unfollow people
+    - biography main characters and language
+    - profile name main characters
+    - private / public / business / non business account
+    - number of posts / followers / following
+    ... and more!
+<br />
+
+Full documentation available on [docs.gramaddict.org](https://docs.gramaddict.org)
+
+## Telegram reports? What's that?
+You can get __reports__ through telegram from your bot activities!
+[Follow this guide to accomplish that](https://docs.gramaddict.org/#/configuration?id=telegram-reports).
+
+<img src="https://github.com/GramAddict/bot/raw/master/res/telegram-reports.png" width="200">
+
+> In this case trends are negative because I use this account only for tuning this bot, and it's private...
+> I didn't accept anyone lately so the trends are meh :P
+
+Cool, isn't it? 💦
+# Quick start
+Now that you're there you still don't know how to install that whole thing.
+I'll try to help you accomplish that with a short tutorial. The full is available [here](https://docs.gramaddict.org/#/quickstart).
+
+## What do you need:
+- a computer (with Windows, macOS or Linux)
+- Python installed on your machine (with pip)
+- Adb tools
+- a physical device or an emulator (with Android 4.4+)
+### Step 1: Install Python (>=3.6):
+>Python 3.10 is currently not supported!
+
+If you're on Linux or macOS you should have Python and Git installed, just check that your Python version is >= 3.6.
+
+On Windows you have to [install it](https://www.python.org/downloads/release/python-397/) for sure.
+
+Failed? [Detailed tutorial here](https://docs.gramaddict.org/#/quickstart?id=step-1-install-python-if-not-installed).
+>A little reminder: we refer to python with __python3__. You may also have python2 installed if you're on Linux for example. If you're on Windows you can use __python__ instead of python3.
+>Check which python alias you have to use by typing `python -V` or `python3 -V` or `py -V` and use the right one for the rest of the tutorial.
+
+>Check that pip3 is installed by typing `pip3 -V`
+>If that returns an error you have to install it! How? [Google is your best friend!](https://www.google.com/search?q=how+to+install+pip) :P
+### Step 2: Install GramAddict:
+You can install GramAddict in two ways: with __pip__ or with __git__.
+Is good practice creating virtual environments when you install a new package. That will save you from a lot of problems!
+
+#### Create a virtual environment
+We create a virtual environment called `.venv` and activate it:
+
+- create a directory where you will create the new environment
+- write in console: `python3 -m venv .venv`
+  > We use `venv` instead of `virtualenv` because `venv` is shipped directly with python3 and you don't have to install anything 🤪
+- activate the .venv:
+    - `source .venv/bin/activate` on Linux/macOS
+    - `.venv\Scripts\activate.bat` on Windows cmd
+    - `.venv\Scripts\activate.ps1` on Windows PowerShell
+      > If you activate the venv correctly, you will see a little (.venv) on the left side of the command line!
+#### With pip (I suggest you this way):
+
+- install the package: `pip3 install GramAddict`
+- check if it's installed: `gramaddict --version`
+- if everything is fine you will get the GramAddict version installed 🥳
+
+#### With git:
+> __Warning:__ console commands like `gramaddict init`, `gramaddict dump` and `gramaddict run` won't work if you installed the bot with git.
+- clone the project: `git clone https://github.com/GramAddict/bot.git gramaddict`
+- enter the gramaddict folder: `cd gramaddict`
+- install the requirements: `pip3 install -r requirements.txt`
+
+### Step 3: Install adb:
+Adb stands for [Android Debug Bridge](https://developer.android.com/studio/command-line/adb). It's needed for making this bot working properly. I think this one is the hardest part to accomplish but don't give up! You can do it, with my help. 💪
+1. download [this package](https://developer.android.com/studio/releases/platform-tools) and unzip it somewhere and remind the path
+   > __Warning:__ place that where you're sure you won't ever delete it, otherwise the bot won't work anymore!
+2. add platform-tools path to the PATH environment variable
+   - if you're on __Linux/macOS__ that's pretty easy:
+      - open ~/.bash_profile with any text editor you like
+      - add the following line with the full path to the platform-tools directory: export PATH=~/Library/Android/sdk/platform-tools/:$PATH. This path may be different depending on the way you installed platform-tools
+      - save file and restart Terminal
+   - on __Windows__ there are more steps to accomplish that:
+      - open Windows Explorer (you can press WINKEY+E) and right-click "My Computer" on left side
+      - in the pop-up menu, click `Properties`
+      - in the `System Properties` window, click the `Advanced` tab, and then click `Environment Variables`
+      - in the `System Variables` window, highlight `Path`, and click `Edit`
+      - in the `Edit System Variables` window, press on `New`
+      - enter the full path for the folder platform-tools you unzipped before
+      - press all the Ok and restart Command Prompt
+3. check that everything is fine
+   - write `adb version`, you should get something like that:
+      > C:\Users\dedil>adb version
+      > Android Debug Bridge version 1.0.41
+      > Version 30.0.5-6877874
+
+### Step 4: Set up the device:
+
+**Physical device**
+
+1. First thing you have to do is to [enable developer options and USB debugging](https://developer.android.com/studio/debug/dev-options#enable).
+2. connect your phone to your computer with a USB cable
+3. device will ask you to allow connection. Press "Connect"
+
+**Emulator for Mac OS**
+
+1. Install the [Homebrew](https://brew.sh)
+2. Install the [Cask](https://cask.readthedocs.io/en/latest/index.html) by running `brew install cask`
+3. Add the Cask application folder to your `$PATH`, e.g. `echo 'export PATH="$HOME/.cask/bin:$PATH"' >> ~/.bash_profile` and open a new terminal or reload with `source ~/.bash_profile`
+4. Install the [Android Studio](https://formulae.brew.sh/cask/android-studio)
+5. Run the Android Studio and click on 'More Actions -> Virtual Device Manager', then select the device and image, I found out that Pixel 2 API 28 combo works well.
+6. Run the virtual device and install the Instagram app on it, don't forget to log in.
+
+**Verify the device with adb**
+
+Type `adb devices` in terminal
+   - a list of devices attached should be displayed, if not you did something wrong
+      > List of devices attached
+      > A0B1CD2345678901    device
+
+   - this is your device ID, you have to use it only if you have more than one device connected at the same time
+
+### Step 5: Start the bot:
+
+This bot works only if your Instagram is in [English](https://help.instagram.com/111923612310997).
+1. initialize uiautomator2: `uiautomator2 init`
+2. initialize GramAddict: `gramaddict init your_ig_account_name_here`
+    > __Warning:__ works only if you installed the bot with pip, if you used git you have to create account folder and youraccountname folder manually.
+    - that script will crate all the files you need for configure and start this bot
+    - you will find them inside the folder `accounts/youraccountname/`
+      ```sh
+        gramaddict/
+          run.py
+          accounts/
+            youraccountname/
+              config.yml
+              telegram.yml
+              filters.yml
+              whitelist.txt
+              blacklist.txt
+              comments_list.txt
+              pm_list.txt
+      ```
+3. now that you have all the requirements you have to configure the whole thing by [following this guide](https://docs.gramaddict.org/#/configuration)
+4. now you're done, and you can finally start the bot: `python3 run.py --config accounts/yourusername/config.yml` or `gramaddict run --config accounts/yourusername/config.yml`
+
+Failed? [Check this out!](https://docs.gramaddict.org/#/quickstart?id=troubleshooting)
+
+# Bot crashes, what should I do?
+The script isn't perfect and may fail sometimes. If this is the case you can open a ticket on our [discord channel](https://discord.gg/NK8PNEFGFF). In that way you won't share with anyone your Instagram account name 😈. We'll be very happy to help you!
+
+# WOW! You dedicated so much time to this project! Why you did that for free??
+Well, we used to be in three a long time ago but suddenly my two friends left. This has been an opportunity for me to improve my skills in Python and that's why I didn't leave the project and keep maintaining it.
+But of course donations are very welcome, so if you think I did a great job you can buy me a beer :)
+
+
+<a  href="https://www.buymeacoffee.com/mastrolube"  target="_blank"><img  src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png"  hspace="10" alt="Buy Me A Coffee"  style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;"  ></a>
+
+# Can I do something to make this project grown?
+On GitHub there is a `star system` which indicates how good a project is. If you like this project it will be amazing if you can press the little star at the top! ⭐
+# Contributors
+
+This project exists thanks to all of our Contributors [[Contribute](https://docs.gramaddict.org/#/contributing)].
+
+<a href="https://github.com/gramaddict/bot/graphs/contributors"><img src="https://opencollective.com/gramaddict/contributors.svg?width=890&button=false" /></a>
+
+<br />
+
+# Backers
+
+Thank you to everyone that supports us financially! 🙏 [[Become a backer](https://opencollective.com/gramaddict#backer)]
+
+<a href="https://opencollective.com/gramaddict#backers" target="_blank"><img src="https://opencollective.com/gramaddict/backers.svg?width=890"></a>
+<br />
+
+# Talk botty with us
+
+<p>
+  <a href="https://discord.gg/NK8PNEFGFF">
+    <img hspace="3" alt="Join us on Discord" src="https://github.com/GramAddict/bot/raw/master/res/discord.png" height=84/>
+  </a>
+</p>
+
+---
+
+> **Disclaimer**<a name="disclaimer" />: This project comes with no guarantee or warranty. You are responsible for whatever happens from using this project. It is possible to get soft or hard banned by using this project if you are not careful.
+
```

#### html2text {}

```diff
@@ -1,7 +1,24 @@
+Metadata-Version: 2.1 Name: GramAddict Version: 3.2.4 Summary: Human-like
+Instagram bot powered by UIAutomator2 Author-email: GramAddict Team
+gramaddict.org> Requires-Python: >=3.6 Description-Content-Type: text/markdown
+Classifier: License :: Free for non-commercial use Classifier: Operating System
+:: OS Independent Classifier: Programming Language :: Python :: 3 Requires-
+Dist: colorama==0.4.4 Requires-Dist: ConfigArgParse==1.5.3 Requires-Dist:
+PyYAML==6.0 Requires-Dist: uiautomator2==2.16.14 Requires-Dist: urllib3==1.26.7
+Requires-Dist: emoji==1.6.1 Requires-Dist: langdetect==1.0.9 Requires-Dist:
+atomicwrites==1.4.0 Requires-Dist: spintax==1.0.4 Requires-Dist:
+requests~=2.28.2 Requires-Dist: packaging~=20.9 Requires-Dist:
+matplotlib==3.4.2 ; extra == "analytics" Requires-Dist: flit ; extra == "dev"
+Requires-Dist: pre-commit ; extra == "dev" Requires-Dist: black ; extra ==
+"dev" Requires-Dist: flake8 ; extra == "dev" Requires-Dist: isort ; extra ==
+"dev" Requires-Dist: pandas==1.2.4 ; extra == "telegram-reports" Requires-Dist:
+pytest-cov ; extra == "telegram-reports" Project-URL: Documentation, https://
+docs.gramaddict.org/#/ Project-URL: Source, https://github.com/GramAddict/bot
+Provides-Extra: analytics Provides-Extra: dev Provides-Extra: telegram-reports
          [https://github.com/GramAddict/bot/raw/master/res/logo.png]
                            ****** GramAddict ******
 
 Looking for Instagram automation? I'm proud to present you a 100% free and open
    source Instagram bot. This bot will allow you to grow your following and
  engagement by liking, following, commenting and sending PM automatically with
              your Android phone/tablet/emulator. No root required.
@@ -56,44 +73,47 @@
 spend all the day scrolling on Instagram? If yes contact a medic :P You don't
 have to do so many actions or Instagram will block you. That appends even if
 you do that by your hands.. Have you ever added a lot of people in a row and
 got blocked for that action? Or spamming people with a link in PM? __DON'T
 F*CKING DO THAT__ __Be gently and anonymous and nobody will notice that you're
 botting, trust me__. ## Do I need a computer for running the bot? Yes, but you
 can also run it [directly on your phone](https://docs.gramaddict.org/#/
-termux)!! In any case, you can decide to use a physical device or an emulator
-(if you're under Windows I suggest you use [Memu](https://www.memuplay.com/)).
-For hosting the bot you can use: - your computer (with Windows, macOS, or
-Linux) - a Raspberry (which is a cheap little pc Linux based) ## Cool! What can
-I do with this bot? There are lots of __cool features__ you can use __for
-free__! - Works without rooting - Works with both emulators and physical
-devices - Can be used stand-alone (without the use of a computer) - Includes
-realistic random human-like delays and actions - Can watch stories while
-interacting - Comment post with emojis and [spintax logic](https://github.com/
-GramAddict/docs/blob/main/configuration.md#spintax-support) - Send PM - Type
-like a human (letter by letter by faking using suggestions. For example, you
-won't type `H - e - l - l - o` letter by letter but something like `H - He -
-Hello`) - Browse carousels and watch their contents - Watch videos for a
-specific amount of time - Scheduler - Getting tasty telegram reports - Supports
-multiple actions in one session - Lots of customizable limits to keep your
-account safe from soft bans - Available interactions - interact with a user's
-followers or following - interact with a top or recent hashtag's post likers -
-interact with a top or recent hashtag post - interact with a top or recent
-place's post likers - interact with a top or recent place post - interact with
-user's post likers - interact with a single blogger - interact with your feed -
-interact with users from a list (*.txt) - interact with posts from links inside
-a list (*.txt) - unfollow any followers - unfollow any followers, followed by
-bot - unfollow any followers, followed by bot, who don't follow you back -
-unfollow from a list (*.txt) - scrape mode for collecting usernames instead of
-interacting with them (you will find more information about that in the doc) -
-Lots of available filters to customize who you interact with - you can
-blacklist people to avoid interacting with them - you can whitelist people to
-not remove them when you unfollow people - biography main characters and
-language - profile name main characters - private / public / business / non
-business account - number of posts / followers / following ... and more!
+termux)!! In any case, you can decide to use a physical device or an emulator.
+If you're under Windows I suggest you use [Memu](https://www.memuplay.com/),
+under Mac OS we found out that [Android studio](https://developer.android.com/
+studio) works well (Installable with [homebrew](https://formulae.brew.sh/cask/
+android-studio)). For hosting the bot you can use: - your computer (with
+Windows, macOS, or Linux) - a Raspberry (which is a cheap little pc Linux
+based) ## Cool! What can I do with this bot? There are lots of __cool
+features__ you can use __for free__! - Works without rooting - Works with both
+emulators and physical devices - Can be used stand-alone (without the use of a
+computer) - Includes realistic random human-like delays and actions - Can watch
+stories while interacting - Comment post with emojis and [spintax logic](https:
+//github.com/GramAddict/docs/blob/main/configuration.md#spintax-support) - Send
+PM - Type like a human (letter by letter by faking using suggestions. For
+example, you won't type `H - e - l - l - o` letter by letter but something like
+`H - He - Hello`) - Browse carousels and watch their contents - Watch videos
+for a specific amount of time - Scheduler - Getting tasty telegram reports -
+Supports multiple actions in one session - Lots of customizable limits to keep
+your account safe from soft bans - Available interactions - interact with a
+user's followers or following - interact with a top or recent hashtag's post
+likers - interact with a top or recent hashtag post - interact with a top or
+recent place's post likers - interact with a top or recent place post -
+interact with user's post likers - interact with a single blogger - interact
+with your feed - interact with users from a list (*.txt) - interact with posts
+from links inside a list (*.txt) - unfollow any followers - unfollow any
+followers, followed by bot - unfollow any followers, followed by bot, who don't
+follow you back - unfollow from a list (*.txt) - scrape mode for collecting
+usernames instead of interacting with them (you will find more information
+about that in the doc) - Lots of available filters to customize who you
+interact with - you can blacklist people to avoid interacting with them - you
+can whitelist people to not remove them when you unfollow people - biography
+main characters and language - profile name main characters - private / public
+/ business / non business account - number of posts / followers / following ...
+and more!
 Full documentation available on [docs.gramaddict.org](https://
 docs.gramaddict.org) ## Telegram reports? What's that? You can get __reports__
 through telegram from your bot activities! [Follow this guide to accomplish
 that](https://docs.gramaddict.org/#/configuration?id=telegram-reports). [https:
 //github.com/GramAddict/bot/raw/master/res/telegram-reports.png] > In this case
 trends are negative because I use this account only for tuning this bot, and
 it's private... > I didn't accept anyone lately so the trends are meh :P Cool,
@@ -150,33 +170,43 @@
 click "My Computer" on left side - in the pop-up menu, click `Properties` - in
 the `System Properties` window, click the `Advanced` tab, and then click
 `Environment Variables` - in the `System Variables` window, highlight `Path`,
 and click `Edit` - in the `Edit System Variables` window, press on `New` -
 enter the full path for the folder platform-tools you unzipped before - press
 all the Ok and restart Command Prompt 3. check that everything is fine - write
 `adb version`, you should get something like that: > C:\Users\dedil>adb version
-> Android Debug Bridge version 1.0.41 > Version 30.0.5-6877874 ### Step 4:
-Start the bot: This bot works only if your Instagram is in [English](https://
-help.instagram.com/111923612310997). 1. First thing you have to do is to
-[enable developer options and USB debugging](https://developer.android.com/
-studio/debug/dev-options#enable). 2. connect your phone to your computer with a
-USB cable 3. device will ask you to allow connection. Press "Connect" 4. type
-`adb devices` in terminal - a list of devices attached should be displayed, if
-not you did something wrong > List of devices attached > A0B1CD2345678901
-device - this is your device ID, you have to use it only if you have more than
-one device connected at the same time 5. initialize uiautomator2: `uiautomator2
-init` 6. initialize GramAddict: `gramaddict init your_ig_account_name_here` >
+> Android Debug Bridge version 1.0.41 > Version 30.0.5-6877874 ### Step 4: Set
+up the device: **Physical device** 1. First thing you have to do is to [enable
+developer options and USB debugging](https://developer.android.com/studio/
+debug/dev-options#enable). 2. connect your phone to your computer with a USB
+cable 3. device will ask you to allow connection. Press "Connect" **Emulator
+for Mac OS** 1. Install the [Homebrew](https://brew.sh) 2. Install the [Cask]
+(https://cask.readthedocs.io/en/latest/index.html) by running `brew install
+cask` 3. Add the Cask application folder to your `$PATH`, e.g. `echo 'export
+PATH="$HOME/.cask/bin:$PATH"' >> ~/.bash_profile` and open a new terminal or
+reload with `source ~/.bash_profile` 4. Install the [Android Studio](https://
+formulae.brew.sh/cask/android-studio) 5. Run the Android Studio and click on
+'More Actions -> Virtual Device Manager', then select the device and image, I
+found out that Pixel 2 API 28 combo works well. 6. Run the virtual device and
+install the Instagram app on it, don't forget to log in. **Verify the device
+with adb** Type `adb devices` in terminal - a list of devices attached should
+be displayed, if not you did something wrong > List of devices attached >
+A0B1CD2345678901 device - this is your device ID, you have to use it only if
+you have more than one device connected at the same time ### Step 5: Start the
+bot: This bot works only if your Instagram is in [English](https://
+help.instagram.com/111923612310997). 1. initialize uiautomator2: `uiautomator2
+init` 2. initialize GramAddict: `gramaddict init your_ig_account_name_here` >
 __Warning:__ works only if you installed the bot with pip, if you used git you
 have to create account folder and youraccountname folder manually. - that
 script will crate all the files you need for configure and start this bot - you
 will find them inside the folder `accounts/youraccountname/` ```sh gramaddict/
 run.py accounts/ youraccountname/ config.yml telegram.yml filters.yml
-whitelist.txt blacklist.txt comments_list.txt pm_list.txt ``` 7. now that you
+whitelist.txt blacklist.txt comments_list.txt pm_list.txt ``` 3. now that you
 have all the requirements you have to configure the whole thing by [following
-this guide](https://docs.gramaddict.org/#/configuration) 8. now you're done,
+this guide](https://docs.gramaddict.org/#/configuration) 4. now you're done,
 and you can finally start the bot: `python3 run.py --config accounts/
 yourusername/config.yml` or `gramaddict run --config accounts/yourusername/
 config.yml` Failed? [Check this out!](https://docs.gramaddict.org/#/
 quickstart?id=troubleshooting) # Bot crashes, what should I do? The script
 isn't perfect and may fail sometimes. If this is the case you can open a ticket
 on our [discord channel](https://discord.gg/NK8PNEFGFF). In that way you won't
 share with anyone your Instagram account name ð. We'll be very happy to help
```

