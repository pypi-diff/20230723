# Comparing `tmp/zomboid_rcon-1.0.0.tar.gz` & `tmp/zomboid_rcon-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zomboid_rcon-1.0.0.tar", last modified: Sun Jul 23 20:19:14 2023, max compression
+gzip compressed data, was "zomboid_rcon-1.0.2.tar", last modified: Sun Jul 23 20:50:04 2023, max compression
```

## Comparing `zomboid_rcon-1.0.0.tar` & `zomboid_rcon-1.0.2.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/
--rw-r--r--   0 runner    (1001) docker     (123)    35129 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    46395 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5032 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     1053 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/zomboid_rcon/
--rw-r--r--   0 runner    (1001) docker     (123)      268 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/zomboid_rcon/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/zomboid_rcon/source/
--rw-r--r--   0 runner    (1001) docker     (123)     3135 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/zomboid_rcon/source/CommandResult.py
--rw-r--r--   0 runner    (1001) docker     (123)     2760 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/zomboid_rcon/source/RconClient.py
--rw-r--r--   0 runner    (1001) docker     (123)      265 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/zomboid_rcon/source/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9087 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/zomboid_rcon/zomboid_rcon.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    46395 2023-07-23 20:19:14.000000 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      368 2023-07-23 20:19:14.000000 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 20:19:14.000000 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       44 2023-07-23 20:19:14.000000 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-23 20:19:14.000000 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:50:04.516208 zomboid_rcon-1.0.2/
+-rw-r--r--   0 runner    (1001) docker     (123)    35129 2023-07-23 20:49:51.000000 zomboid_rcon-1.0.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    46568 2023-07-23 20:50:04.516208 zomboid_rcon-1.0.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5192 2023-07-23 20:49:51.000000 zomboid_rcon-1.0.2/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-07-23 20:49:51.000000 zomboid_rcon-1.0.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 20:50:04.516208 zomboid_rcon-1.0.2/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:50:04.512208 zomboid_rcon-1.0.2/zomboid_rcon/
+-rw-r--r--   0 runner    (1001) docker     (123)      268 2023-07-23 20:49:51.000000 zomboid_rcon-1.0.2/zomboid_rcon/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:50:04.516208 zomboid_rcon-1.0.2/zomboid_rcon/source/
+-rw-r--r--   0 runner    (1001) docker     (123)     3135 2023-07-23 20:49:51.000000 zomboid_rcon-1.0.2/zomboid_rcon/source/CommandResult.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2760 2023-07-23 20:49:51.000000 zomboid_rcon-1.0.2/zomboid_rcon/source/RconClient.py
+-rw-r--r--   0 runner    (1001) docker     (123)      265 2023-07-23 20:49:51.000000 zomboid_rcon-1.0.2/zomboid_rcon/source/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9365 2023-07-23 20:49:51.000000 zomboid_rcon-1.0.2/zomboid_rcon/zomboid_rcon.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:50:04.516208 zomboid_rcon-1.0.2/zomboid_rcon.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    46568 2023-07-23 20:50:04.000000 zomboid_rcon-1.0.2/zomboid_rcon.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      368 2023-07-23 20:50:04.000000 zomboid_rcon-1.0.2/zomboid_rcon.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 20:50:04.000000 zomboid_rcon-1.0.2/zomboid_rcon.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       44 2023-07-23 20:50:04.000000 zomboid_rcon-1.0.2/zomboid_rcon.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-23 20:50:04.000000 zomboid_rcon-1.0.2/zomboid_rcon.egg-info/top_level.txt
```

### Comparing `zomboid_rcon-1.0.0/LICENSE` & `zomboid_rcon-1.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `zomboid_rcon-1.0.0/PKG-INFO` & `zomboid_rcon-1.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zomboid_rcon
-Version: 1.0.0
+Version: 1.0.2
 Summary: Python class for interacting with Project Zomboid servers using RCON 
 Author-email: Jack Whitworth <jack@jackwhitworth.com>
 License: GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -676,47 +676,47 @@
         may consider it more useful to permit linking proprietary applications with
         the library.  If this is what you want to do, use the GNU Lesser General
         Public License instead of this License.  But first, please read
         <https://www.gnu.org/licenses/why-not-lgpl.html>.
         
 Project-URL: Homepage, https://github.com/JMWhitworth/zomboid_rcon
 Keywords: project-zomboid,rcon,project-zomboid-rcon
-Classifier: Development Status :: 4 - Beta
+Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Build Tools
 Classifier: License :: OSI Approved :: GNU General Public License (GPL)
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE
 
 # Zomboid-rcon: Python RCON for Project Zomboid Servers
  
-### Version: 1.0.0
+### Version: 1.0.2
 
 Zomboid-rcon enables you to easily communicate with your Project Zomboid servers via RCON. With zomboid-rcon, you can send commands to your server, manage players, and more, all from within your Python script.
 
+- [Homepage](https://jackwhitworth.com/posts/zomboid-rcon/)
+- [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
+- [Pypi Package](https://pypi.org/project/zomboid-rcon/)
+
 <br><br>
 
 # Installation
 
 To get started, simply install zomboid-rcon using pip:
 
 ```bash
 pip install zomboid-rcon
 ```
 
-- [Homepage](https://jackwhitworth.com/posts/zomboid-rcon/)
-- [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
-- [Pypi Package](https://pypi.org/project/zomboid-rcon/)
-
 <br><br>
 
 # Usage
 
 Using zomboid-rcon is easy. Here's a basic example:
 
 ```python
@@ -761,14 +761,15 @@
 - `godmode("user")` : Makes a player invincible.
 - `gunshot()` : Makes a gunshot noise near the player.
 - `help()` : Brings up the help menu. (Lists native RCON commands. For all zomboid_rcon commands, refer to this list)
 - `invisible("user")` : Makes a player invisible to zombies.
 - `noclip("user")` : Allows a player to pass through solid objects.
 - `quit()` : Saves and quits the server.
 - `releasesafehouse()` : Releases a safehouse you own.
+- `reloadlua("filename")` : Reload a lua script on the server.
 - `reloadoptions()` : Reloads server options.
 - `replay("user", [-record | -play | -stop], "filename")` : Records and plays a replay for a moving player.
 - `save()` : Saves the current world.
 - `sendpulse()` : Toggles sending server performance info to the client.
 - `showoptions()` : Shows a list of current server options and values.
 - `startrain()` : Starts rain on the server.
 - `stoprain()` : Stops rain on the server.
@@ -781,14 +782,15 @@
 - `adduser("user", "pwd")` : Adds a new user to the whitelist.
 - `addusertowhitelist("user")` : Adds a single user connected with a password to the whitelist.
 - `removeuserfromwhitelist("user")` : Removes a single user connected with a password to the whitelist.
 - `banid("SteamID")` : Bans a Steam ID.
 - `unbanid("SteamID")` : Unbans a Steam ID.
 - `banuser("user")` : Bans a user.
 - `unbanuser("user")` : Unbans a user.
+- `checkModsNeedUpdate()` : Indicates whether a mod has been updated. Writes answer to log file.
 - `grantadmin("user")` : Gives admin rights to a user.
 - `removeadmin("user")` : Removes admin rights to a user.
 - `kickuser("user")` : Kicks a user from the server.
 - `players()` : Lists all connected players.
 - `servermsg("message")` : Broadcast a message to all players. (Spaces are replaced with underscores for compatibility)
 - `setaccesslevel("user", [admin | moderator | overseer | gm | observer])` : Set the access/permission level of a player.
 - `voiceban("user", [-true | -false])` : Ban a user from using the voice feature.
```

### Comparing `zomboid_rcon-1.0.0/README.md` & `zomboid_rcon-1.0.2/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -1,27 +1,27 @@
 # Zomboid-rcon: Python RCON for Project Zomboid Servers
  
-### Version: 1.0.0
+### Version: 1.0.2
 
 Zomboid-rcon enables you to easily communicate with your Project Zomboid servers via RCON. With zomboid-rcon, you can send commands to your server, manage players, and more, all from within your Python script.
 
+- [Homepage](https://jackwhitworth.com/posts/zomboid-rcon/)
+- [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
+- [Pypi Package](https://pypi.org/project/zomboid-rcon/)
+
 <br><br>
 
 # Installation
 
 To get started, simply install zomboid-rcon using pip:
 
 ```bash
 pip install zomboid-rcon
 ```
 
-- [Homepage](https://jackwhitworth.com/posts/zomboid-rcon/)
-- [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
-- [Pypi Package](https://pypi.org/project/zomboid-rcon/)
-
 <br><br>
 
 # Usage
 
 Using zomboid-rcon is easy. Here's a basic example:
 
 ```python
@@ -66,14 +66,15 @@
 - `godmode("user")` : Makes a player invincible.
 - `gunshot()` : Makes a gunshot noise near the player.
 - `help()` : Brings up the help menu. (Lists native RCON commands. For all zomboid_rcon commands, refer to this list)
 - `invisible("user")` : Makes a player invisible to zombies.
 - `noclip("user")` : Allows a player to pass through solid objects.
 - `quit()` : Saves and quits the server.
 - `releasesafehouse()` : Releases a safehouse you own.
+- `reloadlua("filename")` : Reload a lua script on the server.
 - `reloadoptions()` : Reloads server options.
 - `replay("user", [-record | -play | -stop], "filename")` : Records and plays a replay for a moving player.
 - `save()` : Saves the current world.
 - `sendpulse()` : Toggles sending server performance info to the client.
 - `showoptions()` : Shows a list of current server options and values.
 - `startrain()` : Starts rain on the server.
 - `stoprain()` : Stops rain on the server.
@@ -86,14 +87,15 @@
 - `adduser("user", "pwd")` : Adds a new user to the whitelist.
 - `addusertowhitelist("user")` : Adds a single user connected with a password to the whitelist.
 - `removeuserfromwhitelist("user")` : Removes a single user connected with a password to the whitelist.
 - `banid("SteamID")` : Bans a Steam ID.
 - `unbanid("SteamID")` : Unbans a Steam ID.
 - `banuser("user")` : Bans a user.
 - `unbanuser("user")` : Unbans a user.
+- `checkModsNeedUpdate()` : Indicates whether a mod has been updated. Writes answer to log file.
 - `grantadmin("user")` : Gives admin rights to a user.
 - `removeadmin("user")` : Removes admin rights to a user.
 - `kickuser("user")` : Kicks a user from the server.
 - `players()` : Lists all connected players.
 - `servermsg("message")` : Broadcast a message to all players. (Spaces are replaced with underscores for compatibility)
 - `setaccesslevel("user", [admin | moderator | overseer | gm | observer])` : Set the access/permission level of a player.
 - `voiceban("user", [-true | -false])` : Ban a user from using the voice feature.
```

### Comparing `zomboid_rcon-1.0.0/pyproject.toml` & `zomboid_rcon-1.0.2/pyproject.toml`

 * *Files 19% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "zomboid_rcon"
-version = "1.0.0"
+version = "1.0.2"
 description = "Python class for interacting with Project Zomboid servers using RCON "
 readme = "README.md"
 license = { file = "LICENSE" }
 authors = [{ name = "Jack Whitworth", email = "jack@jackwhitworth.com" }]
 classifiers = [
-    'Development Status :: 4 - Beta',
+    'Development Status :: 5 - Production/Stable',
     'Intended Audience :: Developers',
     'Topic :: Software Development :: Build Tools',
     'License :: OSI Approved :: GNU General Public License (GPL)',
     'Programming Language :: Python :: 3.8',
     'Programming Language :: Python :: 3.9',
     'Programming Language :: Python :: 3.10',
     'Programming Language :: Python :: 3.11',
```

### Comparing `zomboid_rcon-1.0.0/zomboid_rcon/source/CommandResult.py` & `zomboid_rcon-1.0.2/zomboid_rcon/source/CommandResult.py`

 * *Files identical despite different names*

### Comparing `zomboid_rcon-1.0.0/zomboid_rcon/source/RconClient.py` & `zomboid_rcon-1.0.2/zomboid_rcon/source/RconClient.py`

 * *Files identical despite different names*

### Comparing `zomboid_rcon-1.0.0/zomboid_rcon/zomboid_rcon.py` & `zomboid_rcon-1.0.2/zomboid_rcon/zomboid_rcon.py`

 * *Files 6% similar despite different names*

```diff
@@ -3,19 +3,14 @@
     :copyright: (c) 2023 by JW: https://jackwhitworth.com
     :license: GPL-3.0, see LICENSE for more details.
 """
 
 
 from .source import CommandResult, RconClient
 
-"""
-Credit to Shockbyte for the following resource:
-https://shockbyte.com/billing/knowledgebase/479/All-Console-Commands-for-Your-Project-Zomboid-Server.html
-"""
-
 
 class ZomboidRCON(RconClient):
     """
     Used to interact with Zomboid servers via RCON
     """
     def __init__(self,
             ip:str='localhost',
@@ -149,14 +144,22 @@
         """
         Releases a safehouse you own.
         /releasesafehouse
         """
         return self.command("releasesafehouse")
 
 
+    def reloadlua(self, filename:str) -> CommandResult:
+        """
+        Reload a lua script on the server.
+        /reloadlua "filename"
+        """
+        return self.command("reloadlua", filename)
+
+
     def reloadoptions(self) -> CommandResult:
         """
         Reloads server options.
         /reloadoptions
         """
         return self.command("reloadoptions")
 
@@ -291,14 +294,22 @@
         """
         Unbans a user.
         /unban "user"
         """
         return self.command("unbanuser", user)
 
 
+    def checkModsNeedUpdate(self) -> CommandResult:
+        """
+        Indicates whether a mod has been updated. Writes answer to log file.
+        /checkModsNeedUpdate
+        """
+        return self.command("checkModsNeedUpdate")
+
+
     def grantadmin(self, user:str) -> CommandResult:
         """
         Gives admin rights to a user.
         /grantadmin "user"
         """
         return self.command("grantadmin", user)
```

### Comparing `zomboid_rcon-1.0.0/zomboid_rcon.egg-info/PKG-INFO` & `zomboid_rcon-1.0.2/zomboid_rcon.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zomboid-rcon
-Version: 1.0.0
+Version: 1.0.2
 Summary: Python class for interacting with Project Zomboid servers using RCON 
 Author-email: Jack Whitworth <jack@jackwhitworth.com>
 License: GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -676,47 +676,47 @@
         may consider it more useful to permit linking proprietary applications with
         the library.  If this is what you want to do, use the GNU Lesser General
         Public License instead of this License.  But first, please read
         <https://www.gnu.org/licenses/why-not-lgpl.html>.
         
 Project-URL: Homepage, https://github.com/JMWhitworth/zomboid_rcon
 Keywords: project-zomboid,rcon,project-zomboid-rcon
-Classifier: Development Status :: 4 - Beta
+Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Build Tools
 Classifier: License :: OSI Approved :: GNU General Public License (GPL)
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE
 
 # Zomboid-rcon: Python RCON for Project Zomboid Servers
  
-### Version: 1.0.0
+### Version: 1.0.2
 
 Zomboid-rcon enables you to easily communicate with your Project Zomboid servers via RCON. With zomboid-rcon, you can send commands to your server, manage players, and more, all from within your Python script.
 
+- [Homepage](https://jackwhitworth.com/posts/zomboid-rcon/)
+- [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
+- [Pypi Package](https://pypi.org/project/zomboid-rcon/)
+
 <br><br>
 
 # Installation
 
 To get started, simply install zomboid-rcon using pip:
 
 ```bash
 pip install zomboid-rcon
 ```
 
-- [Homepage](https://jackwhitworth.com/posts/zomboid-rcon/)
-- [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
-- [Pypi Package](https://pypi.org/project/zomboid-rcon/)
-
 <br><br>
 
 # Usage
 
 Using zomboid-rcon is easy. Here's a basic example:
 
 ```python
@@ -761,14 +761,15 @@
 - `godmode("user")` : Makes a player invincible.
 - `gunshot()` : Makes a gunshot noise near the player.
 - `help()` : Brings up the help menu. (Lists native RCON commands. For all zomboid_rcon commands, refer to this list)
 - `invisible("user")` : Makes a player invisible to zombies.
 - `noclip("user")` : Allows a player to pass through solid objects.
 - `quit()` : Saves and quits the server.
 - `releasesafehouse()` : Releases a safehouse you own.
+- `reloadlua("filename")` : Reload a lua script on the server.
 - `reloadoptions()` : Reloads server options.
 - `replay("user", [-record | -play | -stop], "filename")` : Records and plays a replay for a moving player.
 - `save()` : Saves the current world.
 - `sendpulse()` : Toggles sending server performance info to the client.
 - `showoptions()` : Shows a list of current server options and values.
 - `startrain()` : Starts rain on the server.
 - `stoprain()` : Stops rain on the server.
@@ -781,14 +782,15 @@
 - `adduser("user", "pwd")` : Adds a new user to the whitelist.
 - `addusertowhitelist("user")` : Adds a single user connected with a password to the whitelist.
 - `removeuserfromwhitelist("user")` : Removes a single user connected with a password to the whitelist.
 - `banid("SteamID")` : Bans a Steam ID.
 - `unbanid("SteamID")` : Unbans a Steam ID.
 - `banuser("user")` : Bans a user.
 - `unbanuser("user")` : Unbans a user.
+- `checkModsNeedUpdate()` : Indicates whether a mod has been updated. Writes answer to log file.
 - `grantadmin("user")` : Gives admin rights to a user.
 - `removeadmin("user")` : Removes admin rights to a user.
 - `kickuser("user")` : Kicks a user from the server.
 - `players()` : Lists all connected players.
 - `servermsg("message")` : Broadcast a message to all players. (Spaces are replaced with underscores for compatibility)
 - `setaccesslevel("user", [admin | moderator | overseer | gm | observer])` : Set the access/permission level of a player.
 - `voiceban("user", [-true | -false])` : Ban a user from using the voice feature.
```

