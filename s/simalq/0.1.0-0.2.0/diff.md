# Comparing `tmp/simalq-0.1.0.tar.gz` & `tmp/simalq-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "simalq-0.1.0.tar", last modified: Thu Jul 13 17:34:39 2023, max compression
+gzip compressed data, was "simalq-0.2.0.tar", last modified: Sun Jul 23 14:42:45 2023, max compression
```

## Comparing `simalq-0.1.0.tar` & `simalq-0.2.0.tar`

### file list

```diff
@@ -1,40 +1,40 @@
-drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-13 17:34:39.958485 simalq-0.1.0/
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     6676 2023-07-13 17:34:39.958485 simalq-0.1.0/PKG-INFO
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     6250 2023-07-13 17:31:08.000000 simalq-0.1.0/README.rst
--rw-rw-r--   0 hippo     (1000) hippo     (1000)       38 2023-07-13 17:34:39.958485 simalq-0.1.0/setup.cfg
--rw-rw-r--   0 hippo     (1000) hippo     (1000)      947 2023-07-13 17:33:39.000000 simalq-0.1.0/setup.py
-drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-13 17:34:39.958485 simalq-0.1.0/simalq/
--rw-rw-r--   0 hippo     (1000) hippo     (1000)       33 2023-07-13 17:33:55.000000 simalq-0.1.0/simalq/__init__.py
--rw-rw-r--   0 hippo     (1000) hippo     (1000)       76 2023-07-11 20:36:27.000000 simalq-0.1.0/simalq/__main__.py
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     2295 2023-07-12 20:19:26.000000 simalq-0.1.0/simalq/cmdline.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     1316 2023-06-01 20:01:39.000000 simalq-0.1.0/simalq/color.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)    11996 2023-07-11 18:54:38.000000 simalq-0.1.0/simalq/commands.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)    10081 2023-07-10 21:08:37.000000 simalq-0.1.0/simalq/display.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     6847 2023-07-03 21:27:25.000000 simalq-0.1.0/simalq/game_state.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     6062 2023-05-29 16:15:53.000000 simalq-0.1.0/simalq/geometry.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     1933 2023-04-19 21:08:28.000000 simalq-0.1.0/simalq/macros.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     8279 2023-07-12 20:19:26.000000 simalq-0.1.0/simalq/main.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     1811 2023-07-11 20:37:11.000000 simalq-0.1.0/simalq/quest.hy
-drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-13 17:34:39.958485 simalq-0.1.0/simalq/quest_definition/
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     4236 2023-07-12 18:59:44.000000 simalq-0.1.0/simalq/quest_definition/__init__.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)    19583 2023-07-12 18:59:44.000000 simalq-0.1.0/simalq/quest_definition/tutorial.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     3294 2023-07-11 21:34:31.000000 simalq-0.1.0/simalq/save_load.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     1970 2023-07-03 21:27:11.000000 simalq-0.1.0/simalq/strings.hy
-drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-13 17:34:39.958485 simalq-0.1.0/simalq/tile/
--rw-rw-r--   0 hippo     (1000) hippo     (1000)    10921 2023-07-09 16:18:07.000000 simalq-0.1.0/simalq/tile/__init__.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)    13654 2023-07-03 20:20:15.000000 simalq-0.1.0/simalq/tile/item.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)    24271 2023-07-09 16:18:09.000000 simalq-0.1.0/simalq/tile/monster.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     1832 2023-07-03 21:27:25.000000 simalq-0.1.0/simalq/tile/player.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)    17196 2023-07-09 16:18:09.000000 simalq-0.1.0/simalq/tile/scenery.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     2923 2023-07-09 16:18:07.000000 simalq-0.1.0/simalq/tile/tilepedia.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     3141 2023-06-23 16:13:46.000000 simalq-0.1.0/simalq/tile/unimplemented.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     7070 2023-07-11 20:37:11.000000 simalq-0.1.0/simalq/un_iq.hy
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     5688 2023-07-08 19:12:08.000000 simalq-0.1.0/simalq/util.hy
-drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-13 17:34:39.958485 simalq-0.1.0/simalq.egg-info/
--rw-rw-r--   0 hippo     (1000) hippo     (1000)     6676 2023-07-13 17:34:39.000000 simalq-0.1.0/simalq.egg-info/PKG-INFO
--rw-rw-r--   0 hippo     (1000) hippo     (1000)      690 2023-07-13 17:34:39.000000 simalq-0.1.0/simalq.egg-info/SOURCES.txt
--rw-rw-r--   0 hippo     (1000) hippo     (1000)        1 2023-07-13 17:34:39.000000 simalq-0.1.0/simalq.egg-info/dependency_links.txt
--rw-rw-r--   0 hippo     (1000) hippo     (1000)       74 2023-07-13 17:34:39.000000 simalq-0.1.0/simalq.egg-info/requires.txt
--rw-rw-r--   0 hippo     (1000) hippo     (1000)       13 2023-07-13 17:34:39.000000 simalq-0.1.0/simalq.egg-info/top_level.txt
-drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-13 17:34:39.958485 simalq-0.1.0/tests/
--rw-rw-r--   0 hippo     (1000) hippo     (1000)        0 2023-03-29 13:51:08.000000 simalq-0.1.0/tests/__init__.py
+drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-23 14:42:45.189661 simalq-0.2.0/
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     7495 2023-07-23 14:42:45.189661 simalq-0.2.0/PKG-INFO
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     7069 2023-07-23 14:41:19.000000 simalq-0.2.0/README.rst
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)       38 2023-07-23 14:42:45.189661 simalq-0.2.0/setup.cfg
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)      947 2023-07-23 14:41:41.000000 simalq-0.2.0/setup.py
+drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-23 14:42:45.189661 simalq-0.2.0/simalq/
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)       33 2023-07-23 14:41:41.000000 simalq-0.2.0/simalq/__init__.py
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)       76 2023-07-16 12:07:14.000000 simalq-0.2.0/simalq/__main__.py
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     2231 2023-07-23 13:24:54.000000 simalq-0.2.0/simalq/cmdline.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     1316 2023-06-01 20:01:39.000000 simalq-0.2.0/simalq/color.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)    11996 2023-07-11 18:54:38.000000 simalq-0.2.0/simalq/commands.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)    10081 2023-07-10 21:08:37.000000 simalq-0.2.0/simalq/display.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     6847 2023-07-03 21:27:25.000000 simalq-0.2.0/simalq/game_state.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     6062 2023-05-29 16:15:53.000000 simalq-0.2.0/simalq/geometry.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     1933 2023-04-19 21:08:28.000000 simalq-0.2.0/simalq/macros.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     8279 2023-07-12 20:19:26.000000 simalq-0.2.0/simalq/main.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     1811 2023-07-11 20:37:11.000000 simalq-0.2.0/simalq/quest.hy
+drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-23 14:42:45.189661 simalq-0.2.0/simalq/quest_definition/
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     4868 2023-07-23 12:14:20.000000 simalq-0.2.0/simalq/quest_definition/__init__.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)    19251 2023-07-22 17:33:35.000000 simalq-0.2.0/simalq/quest_definition/tutorial.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     3294 2023-07-11 21:34:31.000000 simalq-0.2.0/simalq/save_load.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     1970 2023-07-03 21:27:11.000000 simalq-0.2.0/simalq/strings.hy
+drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-23 14:42:45.189661 simalq-0.2.0/simalq/tile/
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)    11081 2023-07-23 14:01:15.000000 simalq-0.2.0/simalq/tile/__init__.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)    13654 2023-07-03 20:20:15.000000 simalq-0.2.0/simalq/tile/item.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)    24271 2023-07-09 16:18:09.000000 simalq-0.2.0/simalq/tile/monster.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     1832 2023-07-03 21:27:25.000000 simalq-0.2.0/simalq/tile/player.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)    18066 2023-07-23 13:59:34.000000 simalq-0.2.0/simalq/tile/scenery.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     2923 2023-07-09 16:18:07.000000 simalq-0.2.0/simalq/tile/tilepedia.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     3041 2023-07-23 13:48:29.000000 simalq-0.2.0/simalq/tile/unimplemented.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)    10358 2023-07-23 12:57:20.000000 simalq-0.2.0/simalq/un_iq.hy
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     5688 2023-07-08 19:12:08.000000 simalq-0.2.0/simalq/util.hy
+drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-23 14:42:45.189661 simalq-0.2.0/simalq.egg-info/
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)     7495 2023-07-23 14:42:45.000000 simalq-0.2.0/simalq.egg-info/PKG-INFO
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)      690 2023-07-23 14:42:45.000000 simalq-0.2.0/simalq.egg-info/SOURCES.txt
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)        1 2023-07-23 14:42:45.000000 simalq-0.2.0/simalq.egg-info/dependency_links.txt
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)       74 2023-07-23 14:42:45.000000 simalq-0.2.0/simalq.egg-info/requires.txt
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)       13 2023-07-23 14:42:45.000000 simalq-0.2.0/simalq.egg-info/top_level.txt
+drwxrwxr-x   0 hippo     (1000) hippo     (1000)        0 2023-07-23 14:42:45.189661 simalq-0.2.0/tests/
+-rw-rw-r--   0 hippo     (1000) hippo     (1000)        0 2023-03-29 13:51:08.000000 simalq-0.2.0/tests/__init__.py
```

### Comparing `simalq-0.1.0/PKG-INFO` & `simalq-0.2.0/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simalq
-Version: 0.1.0
+Version: 0.2.0
 Summary: Infinitesimal Quest 2 + ε: A turn-based puzzling dungeon crawler
 Author: Kodi B. Arfer
 Project-URL: Source Code, https://github.com/hylang/simalq
 Classifier: License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Description-Content-Type: text/x-rst
@@ -49,24 +49,27 @@
 "Aha!" cried the fell wizard Idok, deep in his underground laboratory, who had been spying on the princess through his mystical Macintosh LC so he could copy her homework answers. "Here is an opportunity to teach you, young princess, to be careful what you wish for." He typed a dread incantation in Hy, the long-dead language of squids born of snakes, and in a swarm of foul parentheses, Tris was carried off to a vast dungeon deep beneath the faraway elven land of Québec. The place looked familiar, and Tris realized that Idok had plagiarized pretty much the whole thing from the thesis of his doctoral advisor, the wicked sorcerer Karvarel. Her brother had braved these very dungeons years ago. She didn't have his memoirs handy, but she did know one really good magic spell, which allowed her to predict the future. Now, with this clairvoyance, her trusty sword and bow, and anything handy she happens to find lying around, Tris must escape the dungeon or die in the attempt. And if she can stuff her pockets with loot on the way, that would really help with her kingdom's latest financial crisis.
 
 Differences from IQ
 ============================================================
 
 Apart from cosmetic and other interface differences, the chief way SQ differs from IQ in its design is its commitment to determinism. SQ replaces IQ's random mechanics, such as monster pathfinding, with deterministic equivalents, sometimes making aspects of the game stateful that were previously stateless. SQ also deliberately omits interface hijinks like darkness and confusion. SQ adds flavor text for tiles, mid-game saving and loading, undo, visibility of the map outside the hero's shooting radius, fixes to bugs and weird behavior (e.g., winning with a "you have died" message if you win the game and die to poison on the same turn), removal of many engine limits (e.g., max and min level size), and the ability to adjust some core game rules (e.g., whether monsters can walk on items).
 
-While the author of IQ kindly provided me with its source code for reference, SQ is an original work that doesn't substantively copy IQ at the code level, and has many fine differences (deliberate, and probably also accidental) in behavior.
+The original IQ map layouts have a number of swastika-like designs. Yves Meynard, the author of IQ, explained to me in 2023 "I meant them to be a shorthand mark of evil. Looking back at IQ2, it's the one thing I wish I hadn't done, because there was a potential for misreading the symbol." I agree that without an explanatory context, like fighting Nazis, swastikas are uncomfortable to see in a video game. So, when SQ loads the original levels, it censors the swastikas by replacing them with new layouts I've made up for the corresponding level regions. I leave skull designs untouched, although the Totenkopf was also a Nazi symbol, because a generic skull shape is more universal and less Nazi-associated in contemporary times.
+
+While Yves kindly provided me with IQ's source code for reference, SQ is an original work that doesn't substantively copy IQ at the code level, and has many fine differences (deliberate, and probably also accidental) in behavior.
 
 Development status
 ============================================================
 
 SQ is reasonably polished and allows playing through several complete quests. The primary thing that's missing is the implementation of more tile types, to support more of IQ's original quests. I also plan to do some larger-scale code cleanup and document some of the interesting parts of the implementation, so that SQ better serves its purpose as an instructive example Hy program.
 
 Version history
 ============================================================
 
+- 0.2.0 (2023-07-23): The IQ quest New Nightmare has been denazified and added to ``--quests``.
 - 0.1.0 (2023-07-13): First playable release.
 
 License
 ============================================================
 
 This program is copyright 2023 Kodi B. Arfer.
```

### Comparing `simalq-0.1.0/README.rst` & `simalq-0.2.0/README.rst`

 * *Files 10% similar despite different names*

```diff
@@ -38,24 +38,27 @@
 "Aha!" cried the fell wizard Idok, deep in his underground laboratory, who had been spying on the princess through his mystical Macintosh LC so he could copy her homework answers. "Here is an opportunity to teach you, young princess, to be careful what you wish for." He typed a dread incantation in Hy, the long-dead language of squids born of snakes, and in a swarm of foul parentheses, Tris was carried off to a vast dungeon deep beneath the faraway elven land of Québec. The place looked familiar, and Tris realized that Idok had plagiarized pretty much the whole thing from the thesis of his doctoral advisor, the wicked sorcerer Karvarel. Her brother had braved these very dungeons years ago. She didn't have his memoirs handy, but she did know one really good magic spell, which allowed her to predict the future. Now, with this clairvoyance, her trusty sword and bow, and anything handy she happens to find lying around, Tris must escape the dungeon or die in the attempt. And if she can stuff her pockets with loot on the way, that would really help with her kingdom's latest financial crisis.
 
 Differences from IQ
 ============================================================
 
 Apart from cosmetic and other interface differences, the chief way SQ differs from IQ in its design is its commitment to determinism. SQ replaces IQ's random mechanics, such as monster pathfinding, with deterministic equivalents, sometimes making aspects of the game stateful that were previously stateless. SQ also deliberately omits interface hijinks like darkness and confusion. SQ adds flavor text for tiles, mid-game saving and loading, undo, visibility of the map outside the hero's shooting radius, fixes to bugs and weird behavior (e.g., winning with a "you have died" message if you win the game and die to poison on the same turn), removal of many engine limits (e.g., max and min level size), and the ability to adjust some core game rules (e.g., whether monsters can walk on items).
 
-While the author of IQ kindly provided me with its source code for reference, SQ is an original work that doesn't substantively copy IQ at the code level, and has many fine differences (deliberate, and probably also accidental) in behavior.
+The original IQ map layouts have a number of swastika-like designs. Yves Meynard, the author of IQ, explained to me in 2023 "I meant them to be a shorthand mark of evil. Looking back at IQ2, it's the one thing I wish I hadn't done, because there was a potential for misreading the symbol." I agree that without an explanatory context, like fighting Nazis, swastikas are uncomfortable to see in a video game. So, when SQ loads the original levels, it censors the swastikas by replacing them with new layouts I've made up for the corresponding level regions. I leave skull designs untouched, although the Totenkopf was also a Nazi symbol, because a generic skull shape is more universal and less Nazi-associated in contemporary times.
+
+While Yves kindly provided me with IQ's source code for reference, SQ is an original work that doesn't substantively copy IQ at the code level, and has many fine differences (deliberate, and probably also accidental) in behavior.
 
 Development status
 ============================================================
 
 SQ is reasonably polished and allows playing through several complete quests. The primary thing that's missing is the implementation of more tile types, to support more of IQ's original quests. I also plan to do some larger-scale code cleanup and document some of the interesting parts of the implementation, so that SQ better serves its purpose as an instructive example Hy program.
 
 Version history
 ============================================================
 
+- 0.2.0 (2023-07-23): The IQ quest New Nightmare has been denazified and added to ``--quests``.
 - 0.1.0 (2023-07-13): First playable release.
 
 License
 ============================================================
 
 This program is copyright 2023 Kodi B. Arfer.
```

### Comparing `simalq-0.1.0/setup.py` & `simalq-0.2.0/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     'blessed >= 1.20.0']
 
 import setuptools
 from pathlib import Path
 
 setuptools.setup(
     name = 'simalq',
-    version = '0.1.0',
+    version = '0.2.0',
     author = 'Kodi B. Arfer',
     description = 'Infinitesimal Quest 2 + ε: A turn-based puzzling dungeon crawler',
     long_description = Path('README.rst').read_text(),
     long_description_content_type = 'text/x-rst',
     project_urls = {
         'Source Code': 'https://github.com/hylang/simalq'},
     install_requires = dependencies,
```

### Comparing `simalq-0.1.0/simalq/cmdline.hy` & `simalq-0.2.0/simalq/cmdline.hy`

 * *Files 6% similar despite different names*

```diff
@@ -8,17 +8,16 @@
   simalq.quest-definition [builtin-quests])
 
 
 (setv url "http://hylang.org/simalq")
 
 (setv advertised-iq-quests #(
    "New First Quest"
-   "New DeathQuest"))
-  ; New Nightmare also works, but I want to denazify it before
-  ; advertising it.
+   "New DeathQuest"
+   "New Nightmare"))
   ; The other IQ quests have at least one unimplemented tile type.
 
 
 (defn handle-cmdline-args [args]
   (setv version-string f"Infinitesimal Quest 2 + ε version {__version__}")
   (setv p (parse-args :args args
     :prog "simalq"
```

### Comparing `simalq-0.1.0/simalq/color.hy` & `simalq-0.2.0/simalq/color.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/commands.hy` & `simalq-0.2.0/simalq/commands.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/display.hy` & `simalq-0.2.0/simalq/display.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/game_state.hy` & `simalq-0.2.0/simalq/game_state.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/geometry.hy` & `simalq-0.2.0/simalq/geometry.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/macros.hy` & `simalq-0.2.0/simalq/macros.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/main.hy` & `simalq-0.2.0/simalq/main.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/quest.hy` & `simalq-0.2.0/simalq/quest.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/quest_definition/__init__.hy` & `simalq-0.2.0/simalq/quest_definition/__init__.hy`

 * *Files 10% similar despite different names*

```diff
@@ -55,15 +55,15 @@
     :authors authors
     :starting-hp starting-hp
     :levels (tuple (gfor
       [i level-args] (enumerate levels)
       (mk-level :n (+ i 1) #** (kwdict level-args))))))
 
 (defn mk-level [
-    n
+    [n 1]
     [player-start #(0 0)]
     [width 16] [height 16] [wrap-x False] [wrap-y False]
     [tiles #()]
       ; The requested tiles are placed in a line east of the player
       ; start.
     [map None]
       ; Overrides `width`, `height`, `tiles`, and possibly
@@ -78,23 +78,24 @@
       (setv map (dedent
         (re.sub r"\A( *\n)*" "" (re.sub r"( *\n)*\Z" "" map))))
       (setv height (+ 1 (.count map "\n")))
       (setv width (ceil (/
         (try (.index map "\n") (except [ValueError] (len map)))
         2)))
       (setv m (Map.make :wrap-x wrap-x :wrap-y wrap-y :width width :height height))
-      (for [
-          [y row] (enumerate (reversed (.split map "\n")))
-          :do (when (% (len row) 2) (setv row (+ row " ")))
-          [x mapsym] (enumerate (partition 2 row))]
+      (setv mapsyms (dfor
+        [y row] (enumerate (reversed (.split map "\n")))
+        :do (when (% (len row) 2) (setv row (+ row " ")))
+        [x mapsym] (enumerate (partition 2 row))
+        #(x y) (.join "" mapsym)))
+      (for [[[x y] mapsym] (.items mapsyms)]
         (setv p (Pos m x y))
-        (setv mapsym (.join "" mapsym))
         (cond
           (in mapsym map-marks)
-            (mk-tile p (get map-marks mapsym))
+            (mk-tile p (get map-marks mapsym) m mapsyms)
           (= mapsym "@ ")
             (setv player-start #(x y))
           (= mapsym ". ")
             None
           (= mapsym "██")
             (mk-tile p "wall")
           True (do
@@ -120,20 +121,33 @@
     :map m
     :player-start (Pos m #* player-start)
     :poison-intensity poison-intensity
     :time-limit time-limit
     :exit-speed exit-speed
     :moving-exit-start moving-exit-start))
 
-(defn mk-tile [locator tile-spec]
+(defn mk-tile [locator tile-spec [map-object None] [mapsyms None]]
   (when (= tile-spec 'floor)
     (return))
   (if (isinstance tile-spec str)
     (setv  d {}  stem tile-spec)
     (setv  [stem #* d] tile-spec  d (kwdict d)))
+  (when (isinstance (.get d "target") str)
+    ; When it's a string, this attribute is treated specially: it
+    ; should come in as a mapsym, and we change it to the `Pos` for
+    ; that mapsym.
+    (setv matches (lfor
+      [xy mapsym] (.items mapsyms)
+      :if (= mapsym (get d "target"))
+      xy))
+    (unless matches
+      (raise (ValueError f"`target` not found: {mapsym}")))
+    (when (> (len matches) 1)
+      (raise (ValueError f"Ambiguous `target`: {mapsym}")))
+    (setv (get d "target") (Pos map-object #* (get matches 0))))
   (add-tile (locate locator) stem #** d))
 
 ;; --------------------------------------------------
 ;; * Load built-in quests
 ;; --------------------------------------------------
 
 (setv builtin-quests {})
```

### Comparing `simalq-0.1.0/simalq/quest_definition/tutorial.hy` & `simalq-0.2.0/simalq/quest_definition/tutorial.hy`

 * *Files 6% similar despite different names*

```diff
@@ -196,14 +196,15 @@
     ▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒> . . . . . . ██. . . . . . . . . ."
   :map-marks {
     "▒▒" "Void"
     "++" "door"
     "ld" "locked door"
     "<1" ["wallfall trap" :wallnum 1]
     "█1" ["trapped wall" :wallnum 1]
+    "{}" ["gate" :target "$ "]
     "w " ["wizard" :hp 3]
     "☉d" ["devil generator" :hp 3
       :summon-frequency (f/ 1 3)
       :summon-hp 1]
     "$ " "pile of gold"
     "k " "key"
     "! " "amulet of invulnerability"
@@ -333,19 +334,10 @@
         f"█{i}" ["trapped wall" :wallnum i]})
       k v)}]
 
 ;; * End matter
 
 })))
 
-; Set the gate target in a hacky way, since I haven't given `mk-quest`
-; a proper way to do it.
-(for [col (. quest levels [(- 7 1)] map data)  stack col  tile stack]
-  (when (= tile.stem "gate")
-    (object.__setattr__ tile "target" (next (gfor
-      col2 tile.pos.map.data  stack2 col2  tile2 stack2
-      :if (= tile2.stem "pile of gold")
-      tile2.pos)))))
-
 quest)
 
 (setv (get hy.M.simalq/quest-definition.builtin-quests name) quest-fn)
```

### Comparing `simalq-0.1.0/simalq/save_load.hy` & `simalq-0.2.0/simalq/save_load.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/strings.hy` & `simalq-0.2.0/simalq/strings.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/tile/__init__.hy` & `simalq-0.2.0/simalq/tile/__init__.hy`

 * *Files 2% similar despite different names*

```diff
@@ -96,15 +96,17 @@
     color-bg None
       ; Similar, for the background color. `None` means allowing
       ; other background-color effects, like the reality fringe, to
       ; determine it.
     flavor None
       ; Flavor text to show in a help screen.
     iq-ix None
-      ; The number that represents this tile in IQ.
+      ; The number that represents this tile in IQ. It can also be a
+      ; tuple, in which case all included numbers will be translated to
+      ; this tile.
     iq-ix-mapper None
       ; An alternative to `iq-ix` for many-to-one matchups from IQ to
       ; SQ tiles. It should be a list like
       ;   ["hp" {1 2  3 4  5 6}]
       ; where the first element is a slot name and the second is a
       ; dictionary mapping IQ values to values for the slot.
     points 0
@@ -215,16 +217,17 @@
   (setv (get Tile.types stem) cls)
 
   ; Also add the new class as a global variable of `simalq.tile` so
   ; `pickle` can find it.
   (setv (get (globals) stem) cls)
 
   (when (setx iq-ix (.get kwargs "iq_ix"))
-    (assert (not-in iq-ix Tile.types-by-iq-ix))
-    (setv (get Tile.types-by-iq-ix iq-ix) cls))
+    (for [i (if (isinstance iq-ix int) [iq-ix] iq-ix)]
+      (assert (not-in i Tile.types-by-iq-ix))
+      (setv (get Tile.types-by-iq-ix i) cls)))
   (when (in "iq_ix_mapper" kwargs)
     (setv [slot d] (get kwargs "iq_ix_mapper"))
     (assert (in slot (sfor  [_ s] (.all-slots cls)  s)))
     (for [[iq-ix slot-value] (.items d)]
       (assert (not-in iq-ix Tile.types-by-iq-ix))
       (setv (get Tile.types-by-iq-ix iq-ix)
         (dict :cls cls :slot slot :value slot-value))))
```

### Comparing `simalq-0.1.0/simalq/tile/item.hy` & `simalq-0.2.0/simalq/tile/item.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/tile/monster.hy` & `simalq-0.2.0/simalq/tile/monster.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/tile/player.hy` & `simalq-0.2.0/simalq/tile/player.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/tile/scenery.hy` & `simalq-0.2.0/simalq/tile/scenery.hy`

 * *Files 3% similar despite different names*

```diff
@@ -447,14 +447,35 @@
   :hook-player-walked-into (fn-dd [self]
     (doc f"Paralyzes you for {paralysis-duration} turns. While you're paralyzed, waiting is the only action you can take.")
     (+= (get G.player.status-effects StatusEffect.Para) paralysis-duration))
 
   :flavor "A magical field that causes you to vividly remember something embarrassing that you did as a teenager, forcing you to briefly freeze in horror. The problem with being royalty is that awkward adolescent moments all too easily become international incidents.")
 (setv paralysis-duration 3)
 
+(deftile Trap ", " "a broken trap"
+  :iq-ix #(
+    ; Removed trap-like tiles that stick around after stepping on them.
+     93   ; false exit
+    189)  ; confusion trap
+
+  :flavor "This once-vicious trap has decayed from neglect and is now pointlessly collecting dust. It was probably implemented in Flash or something.")
+
+(deftile Trap ", " "a pile of debris"
+  :color 'navy
+  :iq-ix #(
+    ; Removed trap-like tiles that are destroyed when you step on them.
+    122   ; dimness trap
+    148)  ; darkness trap
+
+  :hook-player-walked-into (fn [self]
+    "The tile is destroyed."
+    (destroy-tile self))
+
+  :flavor "Dungeon trash like sawdust, loose stones, pebbles, greasy chicken bones left over from goblin feasts, broken wands, and maybe a dead body, all bunched together into a small mound. Running through it will knock it over and get your boots really gross.")
+
 
 (deftile Scenery "()" "a magical energy shield"
   :color 'dark-orange
   :slot-defaults (dict
     :time-remaining 12)
   :mutable-slots #("time_remaining")
   :iq-ix None
```

### Comparing `simalq-0.1.0/simalq/tile/tilepedia.hy` & `simalq-0.2.0/simalq/tile/tilepedia.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq/tile/unimplemented.hy` & `simalq-0.2.0/simalq/tile/unimplemented.hy`

 * *Files 2% similar despite different names*

```diff
@@ -7,26 +7,24 @@
 (defclass UnimplementedTile [Tile]
   "An IQ tile type that we don't yet meaningfully implement or
   substitute, but we can put in `Tile.Tile.types-by-iq-ix` as a
   stub.")
 
 (for [[iq-ix stem] [
 
-    [93 "false_exit"]
     [94 "exit_to_level_"]
     [101 "fire_mage"]
     [102 "open_portcullis"]
     [103 "closed_portcullis"]
     [104 "wand_of_annihilation"]
     [105 "exit_making_wand"]
     [106 "wand_of_gating"]
     [108 "fountain"]
     [110 "candle"]
     [121 "poison_gas_bomb"]
-    [122 "dimness_trap"]
     [129 "archdevil"]
     [130 "exit_mobile"]
     [131 "invisible_wall"]
     [132 "golem"]
     [133 "controllable_teleporter"]
     [134 "siren"]
     [135 "spider"]
@@ -38,15 +36,14 @@
     [141 "phasing_wall_trap"]
     [142 "phasing_wall_trigger"]
     [143 "phase_wand"]
     [144 "unstable_moveable_wall_1"]
     [145 "unstable_moveable_wall_2"]
     [146 "fire_fountain"]
     [147 "wand_of_light"]
-    [148 "darkness_trap"]
     [149 "counterpoison_amulet"]
     [150 "poisonous_amulet"]
     [151 "passwall_amulet"]
     [152 "random_gate"]
     [153 "amulet_of_sight"]
     [154 "wand_of_flame"]
     [156 "wand_of_death"]
@@ -72,15 +69,14 @@
     [182 "gunk"]
     [183 "magical_key"]
     [184 "giant_ant"]
     [185 "dark_brain"]
     [186 "invisible_mage"]
     [187 "magical_mirror"]
     [188 "fading_wall"]
-    [189 "confusion_trap"]
     [190 "wall_generator_north"]
     [191 "wall_generator_south"]
     [192 "wall_generator_west"]
     [193 "wall_generator_east"]
     [194 "arrow_trap"]
     [195 "dragon_egg"]
     [196 "wyrm"]
```

### Comparing `simalq-0.1.0/simalq/un_iq.hy` & `simalq-0.2.0/simalq/un_iq.hy`

 * *Files 26% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 "Parse IQ quest files."
 
 ;; --------------------------------------------------------------
 ;; * Imports
 ;; --------------------------------------------------------------
 
 (require
-  hyrule [unless])
+  hyrule [unless case])
 (import
   types [FunctionType]
-  fractions [Fraction]
+  fractions [Fraction :as f/]
   zipfile [ZipFile]
   functools [cache]
   construct
   toolz [partition]
   simalq.util [cache-dir]
   simalq.geometry [Map Pos]
   simalq.quest [Quest Level]
@@ -211,19 +211,107 @@
             (callable (type result))
               ; A special case where a callback makes the tiles
               ; itself. It can return any number of them.
               (result p #* (get tile-extras p))
             T
               (raise (ValueError (+ "Bad `Tile.types-by-iq-ix` entry: " (repr result))))))))
 
-      (Level
+      (denazify name (+ i 1) (Level
         :n (+ i 1)
         :title l.title
         :player-start (mk-pos l.player-start)
         :next-level l.next-level
         :poison-intensity (if (= l.poison-interval 0)
-          (Fraction 0)
-          (Fraction 1 l.poison-interval))
+          (f/ 0)
+          (f/ 1 l.poison-interval))
         :time-limit l.time-limit
         :exit-speed l.exit-speed
         :moving-exit-start (mk-pos l.moving-exit-start)
-        :map m)))))
+        :map m))))))
+
+;; --------------------------------------------------------------
+;; * Denazification
+;; --------------------------------------------------------------
+
+(defn denazify [quest-name level-n level]
+  "Remove swastika-based designs in the given IQ level. The level is
+  modified in place and then returned."
+  (case [quest-name level-n]
+
+    ["New Nightmare" 1] (do
+      ; Replace the large central swastika.
+      (replace-map-rect level 10 10
+        :map "
+          . . . . . ██{}██. . . . .
+          . . . ██##██{}██##██. . .
+          . . ████d ██☉G██d ████. .
+          . ████d d ██. ██d d ████.
+          . ██% d d ██. ██d d % ██.
+          ████████████+↑████████████
+          {}{}☉G. . +←. +→. . ☉G{}{}
+          ████████████+↓████████████
+          . ██% d d ██. ██d d % ██.
+          . ████d d ██. ██d d ████.
+          . . ████d ██☉G██d ████. .
+          . . . ██##██{}██##██. . .
+          . . . . . ██{}██. . . . ."
+        :map-marks {
+          "% " "meal"
+          "d " ["devil" :hp 3]
+          "☉G" ["ghost generator"
+            :summon-frequency (f/ 2 3)
+            :summon-hp 2]})
+      ; Set targets for the gates.
+      (for [[x1 y1 x2 y2] (partition 4 [
+          16 11  3  3  11 16  3 29  16 21 29 29  21 16 29  3
+          16 10 16 16  10 16 16 16  16 22 16 16  22 16 16 16])]
+        (object.__setattr__ (get level.map.data x1 y1 0)
+          "target" (Pos level.map x2 y2))))
+
+    ["New Nightmare" 24] (do
+      ; Replace the 5-by-5 trap swastikas.
+      (for [[x y] [[12 29] [25 30] [25 18] [11 7] [26 6]]]
+        (replace-map-rect level x y
+          :map "
+            <>. . . <>
+            <>. . . <>
+            <><><><><>
+            <>. . . <>
+            <>. . . <>"
+          :map-marks {
+            "<>" "fixed damaging trap"}))
+      ; Reconfigure the room in the northwest corner.
+      (replace-map-rect level 2 32
+        :map "
+          <1█1█1K █1█1█1
+          <>█1█1G █1█1K
+          <>█1█1G █1█1G
+          ++G G k █1k G
+          <>█1█1█1█1G █1
+          <>█1█1█1█1G █1
+          <><><><><>dd<>"
+        :map-marks {
+          "++" "door"
+          "dd" "locked disappearing door"
+          "<1" ["wallfall trap" :wallnum 1]
+          "█1" ["trapped wall" :wallnum 1]
+          "<>" "fixed damaging trap"
+          "k " "key"
+          "G " ["ghost" :hp 3]
+          "K " ["Dark Knight" :hp 12]})))
+
+  level)
+
+(defn replace-map-rect [old x y #** mk-level-args]
+  "Replace a rectangular region of the level `old`. `x` and `y` are
+  the coordinates of where (0, 0) of the new level should be placed in
+  `old`."
+  (import
+    simalq.tile [mv-tile rm-tile]
+    simalq.quest-definition [mk-level])
+
+  (setv new (mk-level #** mk-level-args))
+  (for [xn (range new.map.width)  yn (range new.map.height)]
+    (for [tile (get old.map.data (+ xn x) (+ yn y))]
+      (rm-tile tile))
+    (for [tile (get new.map.data xn yn)]
+      (mv-tile tile (Pos old.map (+ xn x) (+ yn y))))))
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `simalq-0.1.0/simalq/util.hy` & `simalq-0.2.0/simalq/util.hy`

 * *Files identical despite different names*

### Comparing `simalq-0.1.0/simalq.egg-info/PKG-INFO` & `simalq-0.2.0/simalq.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: simalq
-Version: 0.1.0
+Version: 0.2.0
 Summary: Infinitesimal Quest 2 + ε: A turn-based puzzling dungeon crawler
 Author: Kodi B. Arfer
 Project-URL: Source Code, https://github.com/hylang/simalq
 Classifier: License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Description-Content-Type: text/x-rst
@@ -49,24 +49,27 @@
 "Aha!" cried the fell wizard Idok, deep in his underground laboratory, who had been spying on the princess through his mystical Macintosh LC so he could copy her homework answers. "Here is an opportunity to teach you, young princess, to be careful what you wish for." He typed a dread incantation in Hy, the long-dead language of squids born of snakes, and in a swarm of foul parentheses, Tris was carried off to a vast dungeon deep beneath the faraway elven land of Québec. The place looked familiar, and Tris realized that Idok had plagiarized pretty much the whole thing from the thesis of his doctoral advisor, the wicked sorcerer Karvarel. Her brother had braved these very dungeons years ago. She didn't have his memoirs handy, but she did know one really good magic spell, which allowed her to predict the future. Now, with this clairvoyance, her trusty sword and bow, and anything handy she happens to find lying around, Tris must escape the dungeon or die in the attempt. And if she can stuff her pockets with loot on the way, that would really help with her kingdom's latest financial crisis.
 
 Differences from IQ
 ============================================================
 
 Apart from cosmetic and other interface differences, the chief way SQ differs from IQ in its design is its commitment to determinism. SQ replaces IQ's random mechanics, such as monster pathfinding, with deterministic equivalents, sometimes making aspects of the game stateful that were previously stateless. SQ also deliberately omits interface hijinks like darkness and confusion. SQ adds flavor text for tiles, mid-game saving and loading, undo, visibility of the map outside the hero's shooting radius, fixes to bugs and weird behavior (e.g., winning with a "you have died" message if you win the game and die to poison on the same turn), removal of many engine limits (e.g., max and min level size), and the ability to adjust some core game rules (e.g., whether monsters can walk on items).
 
-While the author of IQ kindly provided me with its source code for reference, SQ is an original work that doesn't substantively copy IQ at the code level, and has many fine differences (deliberate, and probably also accidental) in behavior.
+The original IQ map layouts have a number of swastika-like designs. Yves Meynard, the author of IQ, explained to me in 2023 "I meant them to be a shorthand mark of evil. Looking back at IQ2, it's the one thing I wish I hadn't done, because there was a potential for misreading the symbol." I agree that without an explanatory context, like fighting Nazis, swastikas are uncomfortable to see in a video game. So, when SQ loads the original levels, it censors the swastikas by replacing them with new layouts I've made up for the corresponding level regions. I leave skull designs untouched, although the Totenkopf was also a Nazi symbol, because a generic skull shape is more universal and less Nazi-associated in contemporary times.
+
+While Yves kindly provided me with IQ's source code for reference, SQ is an original work that doesn't substantively copy IQ at the code level, and has many fine differences (deliberate, and probably also accidental) in behavior.
 
 Development status
 ============================================================
 
 SQ is reasonably polished and allows playing through several complete quests. The primary thing that's missing is the implementation of more tile types, to support more of IQ's original quests. I also plan to do some larger-scale code cleanup and document some of the interesting parts of the implementation, so that SQ better serves its purpose as an instructive example Hy program.
 
 Version history
 ============================================================
 
+- 0.2.0 (2023-07-23): The IQ quest New Nightmare has been denazified and added to ``--quests``.
 - 0.1.0 (2023-07-13): First playable release.
 
 License
 ============================================================
 
 This program is copyright 2023 Kodi B. Arfer.
```

### Comparing `simalq-0.1.0/simalq.egg-info/SOURCES.txt` & `simalq-0.2.0/simalq.egg-info/SOURCES.txt`

 * *Files identical despite different names*

