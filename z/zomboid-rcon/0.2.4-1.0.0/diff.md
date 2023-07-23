# Comparing `tmp/zomboid_rcon-0.2.4.tar.gz` & `tmp/zomboid_rcon-1.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zomboid_rcon-0.2.4.tar", last modified: Sun Jul 23 15:42:29 2023, max compression
+gzip compressed data, was "zomboid_rcon-1.0.0.tar", last modified: Sun Jul 23 20:19:14 2023, max compression
```

## Comparing `zomboid_rcon-0.2.4.tar` & `zomboid_rcon-1.0.0.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/
--rw-r--r--   0 runner    (1001) docker     (123)    35129 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    44108 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2745 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     1053 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/zomboid_rcon/
--rw-r--r--   0 runner    (1001) docker     (123)      268 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/zomboid_rcon/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/zomboid_rcon/source/
--rw-r--r--   0 runner    (1001) docker     (123)     3066 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/zomboid_rcon/source/CommandResult.py
--rw-r--r--   0 runner    (1001) docker     (123)     2695 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/zomboid_rcon/source/RconClient.py
--rw-r--r--   0 runner    (1001) docker     (123)      265 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/zomboid_rcon/source/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1277 2023-07-23 15:42:14.000000 zomboid_rcon-0.2.4/zomboid_rcon/zomboid_rcon.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:42:29.380878 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    44108 2023-07-23 15:42:29.000000 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      368 2023-07-23 15:42:29.000000 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 15:42:29.000000 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       44 2023-07-23 15:42:29.000000 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-23 15:42:29.000000 zomboid_rcon-0.2.4/zomboid_rcon.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/
+-rw-r--r--   0 runner    (1001) docker     (123)    35129 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    46395 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5032 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1053 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/zomboid_rcon/
+-rw-r--r--   0 runner    (1001) docker     (123)      268 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/zomboid_rcon/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/zomboid_rcon/source/
+-rw-r--r--   0 runner    (1001) docker     (123)     3135 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/zomboid_rcon/source/CommandResult.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2760 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/zomboid_rcon/source/RconClient.py
+-rw-r--r--   0 runner    (1001) docker     (123)      265 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/zomboid_rcon/source/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9087 2023-07-23 20:18:56.000000 zomboid_rcon-1.0.0/zomboid_rcon/zomboid_rcon.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 20:19:14.225799 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    46395 2023-07-23 20:19:14.000000 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      368 2023-07-23 20:19:14.000000 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 20:19:14.000000 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       44 2023-07-23 20:19:14.000000 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-23 20:19:14.000000 zomboid_rcon-1.0.0/zomboid_rcon.egg-info/top_level.txt
```

### Comparing `zomboid_rcon-0.2.4/LICENSE` & `zomboid_rcon-1.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `zomboid_rcon-0.2.4/PKG-INFO` & `zomboid_rcon-1.0.0/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zomboid_rcon
-Version: 0.2.4
+Version: 1.0.0
 Summary: Python class for interacting with Project Zomboid servers using RCON 
 Author-email: Jack Whitworth <jack@jackwhitworth.com>
 License: GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -691,91 +691,137 @@
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE
 
 # Zomboid-rcon: Python RCON for Project Zomboid Servers
  
+### Version: 1.0.0
+
 Zomboid-rcon enables you to easily communicate with your Project Zomboid servers via RCON. With zomboid-rcon, you can send commands to your server, manage players, and more, all from within your Python script.
 
-<br>
+<br><br>
 
 # Installation
 
 To get started, simply install zomboid-rcon using pip:
 
-``` pip install zomboid-rcon ```
+```bash
+pip install zomboid-rcon
+```
 
-[Pypi Package](https://pypi.org/project/zomboid-rcon/) / [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
+- [Homepage](https://jackwhitworth.com/posts/zomboid-rcon/)
+- [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
+- [Pypi Package](https://pypi.org/project/zomboid-rcon/)
 
-<br>
+<br><br>
 
 # Usage
 
 Using zomboid-rcon is easy. Here's a basic example:
 
 ```python
 from zomboid_rcon import ZomboidRCON
 
 if __name__ == "__main__":
-    pz = ZomboidRCON(ip='localhost', port=27015, password='myPassword')
+    pz = ZomboidRCON(ip='localhost', port=12345, password='myPassword')
     command = pz.serverMsg("You dead yet?")
     print(command.response)
-    print(command.successful)
 ```
 
 This example connects to a server running on your local machine and sends the message "You dead yet?".
 
 Zomboid-rcon provides several built-in methods for common server management tasks, such as getting a list of connected players:
 
 ```python
 from zomboid_rcon import ZomboidRCON
 
 if __name__ == "__main__":
-    pz = ZomboidRCON(ip='localhost', password='myPassword')
-    
+    pz = ZomboidRCON(ip='localhost', port=12345, password='myPassword')
     print(pz.players().response)
 ```
 
 This example prints a list of all players currently connected to the server.
 
-<br>
+<br><br>
 
 # Available Commands
 
-Zomboid-rcon provides several built-in methods for common server management tasks:
+Zomboid-rcon provides built-in methods for the available RCON commands within Project Zomboid.
+
+### General Commands
 
-- ```serverMsg("Your message")``` : Global server messages
-- ```players()``` : List all players online
-- ```save()``` : Save the game in it's current state
-- ```quit()``` : Save & shut down the game server
-- ```showoptions()``` : Get game server settings
-- ```help()``` : Get all command options: Note that only the listed commands have pre-build methods. For any not listed here please use the 'command' method in the following example.
+- `additem("user", "item")` : Items can be found on the PZ wiki: https://pzwiki.net/wiki/Items
+- `addvehicle("user")` : Spawns a vehicle.
+- `addxp("user", "perk", xp)` : Gives XP to a player.
+- `alarm()` : Sounds a building alarm at the admin's position. Must be in a room.
+- `changeoption("option", "newOption")` : Changes a server option.
+- `chopper()` : Places a helicopter event on a random player.
+- `changepwd("pwd", "newPwd")` : Changes your password.
+- `createhorde("number")` : Spawns a horde near a player.
+- `godmode("user")` : Makes a player invincible.
+- `gunshot()` : Makes a gunshot noise near the player.
+- `help()` : Brings up the help menu. (Lists native RCON commands. For all zomboid_rcon commands, refer to this list)
+- `invisible("user")` : Makes a player invisible to zombies.
+- `noclip("user")` : Allows a player to pass through solid objects.
+- `quit()` : Saves and quits the server.
+- `releasesafehouse()` : Releases a safehouse you own.
+- `reloadoptions()` : Reloads server options.
+- `replay("user", [-record | -play | -stop], "filename")` : Records and plays a replay for a moving player.
+- `save()` : Saves the current world.
+- `sendpulse()` : Toggles sending server performance info to the client.
+- `showoptions()` : Shows a list of current server options and values.
+- `startrain()` : Starts rain on the server.
+- `stoprain()` : Stops rain on the server.
+- `teleport("user", "toUser")` : Teleports to a player.
+- `teleportto(x, y, z)` : Teleports to certain coordinates.
+
+### Moderation Commands
+
+- `addalltowhitelist()` : Adds all current users connected with a password to the whitelist.
+- `adduser("user", "pwd")` : Adds a new user to the whitelist.
+- `addusertowhitelist("user")` : Adds a single user connected with a password to the whitelist.
+- `removeuserfromwhitelist("user")` : Removes a single user connected with a password to the whitelist.
+- `banid("SteamID")` : Bans a Steam ID.
+- `unbanid("SteamID")` : Unbans a Steam ID.
+- `banuser("user")` : Bans a user.
+- `unbanuser("user")` : Unbans a user.
+- `grantadmin("user")` : Gives admin rights to a user.
+- `removeadmin("user")` : Removes admin rights to a user.
+- `kickuser("user")` : Kicks a user from the server.
+- `players()` : Lists all connected players.
+- `servermsg("message")` : Broadcast a message to all players. (Spaces are replaced with underscores for compatibility)
+- `setaccesslevel("user", [admin | moderator | overseer | gm | observer])` : Set the access/permission level of a player.
+- `voiceban("user", [-true | -false])` : Ban a user from using the voice feature.
 
 <br>
 
+### Command not listed?
+
 You can execute any custom command using the command method:
 ```python
-from zomboid_rcon import ZomboidRCON
-
-if __name__ == "__main__":
-    pz = ZomboidRCON(ip='localhost', password='myPassword')
-    print(pz.command("command", "arg1", "arg2").response)
+pz.command("command", "arg1", "arg2", "etc")
 ```
 
-<br>
+<br><br>
+
+# Demonstration
+
+![Zomboid RCON demonstration GIF](https://jackwhitworth.com/wp-content/uploads/2023/07/zomboid_rcon_demo.gif)
+
+<br><br>
 
 # Known Issues
 
 Please note that zomboid-rcon uses the [timeout_decorator](https://pypi.org/project/timeout-decorator/) package, which is currently only compatible with Unix/Linux systems. As a result, **timeouts may cause errors on Windows machines**. We are actively working on finding an alternative solution for Windows users.
 
-<br>
+<br><br>
 
 # Contributing
 
 We welcome contributions from anyone! If you would like to contribute to the project, please open an issue or submit a pull request on [Github](https://github.com/JMWhitworth/zomboid_rcon).
 
-<br>
+<br><br>
 
 # License
 
 Zomboid-rcon is licensed under the GPL-3.0 license.
```

### Comparing `zomboid_rcon-0.2.4/pyproject.toml` & `zomboid_rcon-1.0.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "zomboid_rcon"
-version = "0.2.4"
+version = "1.0.0"
 description = "Python class for interacting with Project Zomboid servers using RCON "
 readme = "README.md"
 license = { file = "LICENSE" }
 authors = [{ name = "Jack Whitworth", email = "jack@jackwhitworth.com" }]
 classifiers = [
     'Development Status :: 4 - Beta',
     'Intended Audience :: Developers',
```

### Comparing `zomboid_rcon-0.2.4/zomboid_rcon/source/CommandResult.py` & `zomboid_rcon-1.0.0/zomboid_rcon/source/CommandResult.py`

 * *Files 4% similar despite different names*

```diff
@@ -2,16 +2,19 @@
 Zomboid RCON: https://github.com/JMWhitworth/zomboid_rcon
     :copyright: (c) 2023 by JW: https://jackwhitworth.com
     :license: GPL-3.0, see LICENSE for more details.
 """
 
 
 class CommandResult:
-    """ A class representing the result of executing a command. """
+    """
+    A class representing the result of executing a command.
+    """
     
+
     def __init__(self,
             command:str,
             response:str,
             successful:bool=False,
             failureMessage:str="Command was unsuccessful"
         ):
         """        
@@ -22,73 +25,87 @@
             failureMessage (str, optional): The message to display if the command was unsuccessful. Defaults to "Command was unsuccessful".
         """
         self.command = command
         self.response = response
         self.successful = successful
         self.failureMessage = failureMessage
     
+
     @property
     def command(self) -> str:
-        """ Returns command used """
+        """
+        Returns command used
+        """
         return self._command
     
+
     @command.setter
     def command(self, command:str) -> None:
         """
         Validates input as string
         Returns true if set successfully
         """
         if isinstance(command, str):
             self._command = command.strip()
         else:
             raise ValueError("Command used must be a string")
     
+
     @property
     def failureMessage(self) -> str:
-        """ Returns failure message if command unsuccessful """
+        """
+        Returns failure message if command unsuccessful
+        """
         return self._failureMessage
     
+
     @failureMessage.setter
     def failureMessage(self, failureMessage:str) -> None:
         """
         Validates input as string
         Returns true if set successfully
         """
         if isinstance(failureMessage, str):
             self._failureMessage = failureMessage.strip()
         else:
             raise ValueError("Failure message used must be a string")
     
+
     @property
     def response(self) -> str:
         """
         Returns the command's response.
         If command failed, returns failure message.
         """
         if self.successful:
             return self._response
         
         return self.failureMessage
     
+
     @response.setter
     def response(self, newResponse:str) -> None:
         """
         Validates input as string
         Returns true if set successfully
         """
         if isinstance(newResponse, str):
             self._response = newResponse.strip()
         else:
             raise ValueError("Command response must be a string")
     
+
     @property
     def successful(self) -> bool:
-        """ Returns if command was successful """
+        """
+        Returns if command was successful
+        """
         return self._successful
     
+    
     @successful.setter
     def successful(self, successStatus:bool) -> None:
         """
         Validates input as boolean
         Returns true if set successfully
         """
         if isinstance(successStatus, bool):
```

### Comparing `zomboid_rcon-0.2.4/zomboid_rcon/source/RconClient.py` & `zomboid_rcon-1.0.0/zomboid_rcon/source/RconClient.py`

 * *Files 6% similar despite different names*

```diff
@@ -7,15 +7,18 @@
 
 from rcon.source        import Client
 from timeout_decorator  import timeout, TimeoutError
 
 from .CommandResult     import CommandResult
 
 class RconClient:
-    """ Parent class for handling RCON core functionality """
+    """
+    Parent class for handling RCON core functionality
+    """
+    
     
     def __init__(self,
             ip:str,
             port:int,
             password:str,
             retries:int=5,
             logging:bool=False
@@ -30,18 +33,22 @@
         """
         self._ip = ip
         self._port = port
         self._password = password
         self._retries = retries
         self.logging = logging
     
+
     def createClient(self) -> Client:
-        """ Returns an rcon.source.Client object for requests """
+        """
+        Returns an rcon.source.Client object for requests
+        """
         return Client(self._ip, self._port, passwd=self._password)
     
+
     def command(self, command:str, *args) -> CommandResult:
         """
         Attempts to execute a given command.
         Upon TimeoutError it will retry according to self._retries
         """
         tries = 0
         while tries < self._retries:
@@ -58,24 +65,30 @@
                 tries += 1
         return CommandResult(
             command = command,
             successful = False,
             response = f"Session timed out (after {self._retries} attempt(s))"
             )
     
+
     @timeout(10)
     def _command(self, command:str, *args) -> str:
-        """ Private method to handle timeouts """
+        """
+        Private method to handle timeouts
+        """
         try:
             with self.createClient() as client:
                 return client.run(command, *args)
         except ConnectionRefusedError:
             return "Connection refused"
     
+
     def getInfo(self) -> dict:
-        """ Returns dict of current object's information """
+        """
+        Returns dict of current object's information
+        """
         return {
             "ip": self._ip,
             "port": self._port,
             "password": self._password,
             "retries": self._retries
         }
```

### Comparing `zomboid_rcon-0.2.4/zomboid_rcon.egg-info/PKG-INFO` & `zomboid_rcon-1.0.0/zomboid_rcon.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zomboid-rcon
-Version: 0.2.4
+Version: 1.0.0
 Summary: Python class for interacting with Project Zomboid servers using RCON 
 Author-email: Jack Whitworth <jack@jackwhitworth.com>
 License: GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <https://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -691,91 +691,137 @@
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE
 
 # Zomboid-rcon: Python RCON for Project Zomboid Servers
  
+### Version: 1.0.0
+
 Zomboid-rcon enables you to easily communicate with your Project Zomboid servers via RCON. With zomboid-rcon, you can send commands to your server, manage players, and more, all from within your Python script.
 
-<br>
+<br><br>
 
 # Installation
 
 To get started, simply install zomboid-rcon using pip:
 
-``` pip install zomboid-rcon ```
+```bash
+pip install zomboid-rcon
+```
 
-[Pypi Package](https://pypi.org/project/zomboid-rcon/) / [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
+- [Homepage](https://jackwhitworth.com/posts/zomboid-rcon/)
+- [GitHub Repo](https://github.com/jmwhitworth/zomboid_rcon)
+- [Pypi Package](https://pypi.org/project/zomboid-rcon/)
 
-<br>
+<br><br>
 
 # Usage
 
 Using zomboid-rcon is easy. Here's a basic example:
 
 ```python
 from zomboid_rcon import ZomboidRCON
 
 if __name__ == "__main__":
-    pz = ZomboidRCON(ip='localhost', port=27015, password='myPassword')
+    pz = ZomboidRCON(ip='localhost', port=12345, password='myPassword')
     command = pz.serverMsg("You dead yet?")
     print(command.response)
-    print(command.successful)
 ```
 
 This example connects to a server running on your local machine and sends the message "You dead yet?".
 
 Zomboid-rcon provides several built-in methods for common server management tasks, such as getting a list of connected players:
 
 ```python
 from zomboid_rcon import ZomboidRCON
 
 if __name__ == "__main__":
-    pz = ZomboidRCON(ip='localhost', password='myPassword')
-    
+    pz = ZomboidRCON(ip='localhost', port=12345, password='myPassword')
     print(pz.players().response)
 ```
 
 This example prints a list of all players currently connected to the server.
 
-<br>
+<br><br>
 
 # Available Commands
 
-Zomboid-rcon provides several built-in methods for common server management tasks:
+Zomboid-rcon provides built-in methods for the available RCON commands within Project Zomboid.
+
+### General Commands
 
-- ```serverMsg("Your message")``` : Global server messages
-- ```players()``` : List all players online
-- ```save()``` : Save the game in it's current state
-- ```quit()``` : Save & shut down the game server
-- ```showoptions()``` : Get game server settings
-- ```help()``` : Get all command options: Note that only the listed commands have pre-build methods. For any not listed here please use the 'command' method in the following example.
+- `additem("user", "item")` : Items can be found on the PZ wiki: https://pzwiki.net/wiki/Items
+- `addvehicle("user")` : Spawns a vehicle.
+- `addxp("user", "perk", xp)` : Gives XP to a player.
+- `alarm()` : Sounds a building alarm at the admin's position. Must be in a room.
+- `changeoption("option", "newOption")` : Changes a server option.
+- `chopper()` : Places a helicopter event on a random player.
+- `changepwd("pwd", "newPwd")` : Changes your password.
+- `createhorde("number")` : Spawns a horde near a player.
+- `godmode("user")` : Makes a player invincible.
+- `gunshot()` : Makes a gunshot noise near the player.
+- `help()` : Brings up the help menu. (Lists native RCON commands. For all zomboid_rcon commands, refer to this list)
+- `invisible("user")` : Makes a player invisible to zombies.
+- `noclip("user")` : Allows a player to pass through solid objects.
+- `quit()` : Saves and quits the server.
+- `releasesafehouse()` : Releases a safehouse you own.
+- `reloadoptions()` : Reloads server options.
+- `replay("user", [-record | -play | -stop], "filename")` : Records and plays a replay for a moving player.
+- `save()` : Saves the current world.
+- `sendpulse()` : Toggles sending server performance info to the client.
+- `showoptions()` : Shows a list of current server options and values.
+- `startrain()` : Starts rain on the server.
+- `stoprain()` : Stops rain on the server.
+- `teleport("user", "toUser")` : Teleports to a player.
+- `teleportto(x, y, z)` : Teleports to certain coordinates.
+
+### Moderation Commands
+
+- `addalltowhitelist()` : Adds all current users connected with a password to the whitelist.
+- `adduser("user", "pwd")` : Adds a new user to the whitelist.
+- `addusertowhitelist("user")` : Adds a single user connected with a password to the whitelist.
+- `removeuserfromwhitelist("user")` : Removes a single user connected with a password to the whitelist.
+- `banid("SteamID")` : Bans a Steam ID.
+- `unbanid("SteamID")` : Unbans a Steam ID.
+- `banuser("user")` : Bans a user.
+- `unbanuser("user")` : Unbans a user.
+- `grantadmin("user")` : Gives admin rights to a user.
+- `removeadmin("user")` : Removes admin rights to a user.
+- `kickuser("user")` : Kicks a user from the server.
+- `players()` : Lists all connected players.
+- `servermsg("message")` : Broadcast a message to all players. (Spaces are replaced with underscores for compatibility)
+- `setaccesslevel("user", [admin | moderator | overseer | gm | observer])` : Set the access/permission level of a player.
+- `voiceban("user", [-true | -false])` : Ban a user from using the voice feature.
 
 <br>
 
+### Command not listed?
+
 You can execute any custom command using the command method:
 ```python
-from zomboid_rcon import ZomboidRCON
-
-if __name__ == "__main__":
-    pz = ZomboidRCON(ip='localhost', password='myPassword')
-    print(pz.command("command", "arg1", "arg2").response)
+pz.command("command", "arg1", "arg2", "etc")
 ```
 
-<br>
+<br><br>
+
+# Demonstration
+
+![Zomboid RCON demonstration GIF](https://jackwhitworth.com/wp-content/uploads/2023/07/zomboid_rcon_demo.gif)
+
+<br><br>
 
 # Known Issues
 
 Please note that zomboid-rcon uses the [timeout_decorator](https://pypi.org/project/timeout-decorator/) package, which is currently only compatible with Unix/Linux systems. As a result, **timeouts may cause errors on Windows machines**. We are actively working on finding an alternative solution for Windows users.
 
-<br>
+<br><br>
 
 # Contributing
 
 We welcome contributions from anyone! If you would like to contribute to the project, please open an issue or submit a pull request on [Github](https://github.com/JMWhitworth/zomboid_rcon).
 
-<br>
+<br><br>
 
 # License
 
 Zomboid-rcon is licensed under the GPL-3.0 license.
```

