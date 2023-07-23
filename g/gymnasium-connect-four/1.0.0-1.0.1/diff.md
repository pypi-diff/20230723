# Comparing `tmp/gymnasium_connect_four-1.0.0.tar.gz` & `tmp/gymnasium_connect_four-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gymnasium_connect_four-1.0.0.tar", last modified: Sun Jul 23 17:33:52 2023, max compression
+gzip compressed data, was "gymnasium_connect_four-1.0.1.tar", last modified: Sun Jul 23 17:51:00 2023, max compression
```

## Comparing `gymnasium_connect_four-1.0.0.tar` & `gymnasium_connect_four-1.0.1.tar`

### file list

```diff
@@ -1,31 +1,31 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 17:33:52.691677 gymnasium_connect_four-1.0.0/
--rw-rw-rw-   0        0        0     1091 2023-07-23 15:11:33.000000 gymnasium_connect_four-1.0.0/LICENSE
--rw-rw-rw-   0        0        0      251 2023-07-23 17:33:52.691677 gymnasium_connect_four-1.0.0/PKG-INFO
--rw-rw-rw-   0        0        0     2706 2023-07-23 17:31:23.000000 gymnasium_connect_four-1.0.0/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 17:33:52.671686 gymnasium_connect_four-1.0.0/connect_four_gymnasium/
--rw-rw-rw-   0        0        0     8933 2023-07-23 15:24:04.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/ConnectFourEnv.py
--rw-rw-rw-   0        0        0       42 2023-07-23 15:35:19.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 17:33:52.682685 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/
--rw-rw-rw-   0        0        0     4199 2023-07-23 16:48:20.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/AdultPlayer.py
--rw-rw-rw-   0        0        0     3643 2023-07-23 16:48:25.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/AdultSmarterPlayer.py
--rw-rw-rw-   0        0        0      295 2023-07-23 16:46:25.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/BabyPlayer.py
--rw-rw-rw-   0        0        0     1489 2023-07-23 16:46:28.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/ChildPlayer.py
--rw-rw-rw-   0        0        0     1896 2023-07-23 16:48:02.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/ChildSmarterPlayer.py
--rw-rw-rw-   0        0        0      602 2023-07-23 16:51:40.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/ConsolePlayer.py
--rw-rw-rw-   0        0        0     4068 2023-07-23 17:21:33.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/MinMaxPlayer.py
--rw-rw-rw-   0        0        0      482 2023-07-23 16:51:55.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/ModelPlayer.py
--rw-rw-rw-   0        0        0      393 2023-07-23 15:52:13.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/Player.py
--rw-rw-rw-   0        0        0     2559 2023-07-23 16:48:37.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/TeenagerPlayer.py
--rw-rw-rw-   0        0        0     3949 2023-07-23 16:49:03.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/TeenagerSmarterPlayer.py
--rw-rw-rw-   0        0        0      442 2023-07-23 17:21:40.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 17:33:52.684685 gymnasium_connect_four-1.0.0/connect_four_gymnasium/tools/
--rw-rw-rw-   0        0        0     3380 2023-07-23 17:21:26.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/tools/EloLeaderboard.py
--rw-rw-rw-   0        0        0       42 2023-07-23 16:29:17.000000 gymnasium_connect_four-1.0.0/connect_four_gymnasium/tools/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 17:33:52.689692 gymnasium_connect_four-1.0.0/gymnasium_connect_four.egg-info/
--rw-rw-rw-   0        0        0      251 2023-07-23 17:33:52.000000 gymnasium_connect_four-1.0.0/gymnasium_connect_four.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      992 2023-07-23 17:33:52.000000 gymnasium_connect_four-1.0.0/gymnasium_connect_four.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 17:33:52.000000 gymnasium_connect_four-1.0.0/gymnasium_connect_four.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       32 2023-07-23 17:33:52.000000 gymnasium_connect_four-1.0.0/gymnasium_connect_four.egg-info/requires.txt
--rw-rw-rw-   0        0        0       23 2023-07-23 17:33:52.000000 gymnasium_connect_four-1.0.0/gymnasium_connect_four.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 17:33:52.691677 gymnasium_connect_four-1.0.0/setup.cfg
--rw-rw-rw-   0        0        0      517 2023-07-23 17:28:26.000000 gymnasium_connect_four-1.0.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:51:00.363174 gymnasium_connect_four-1.0.1/
+-rw-rw-rw-   0        0        0     1091 2023-07-23 15:11:33.000000 gymnasium_connect_four-1.0.1/LICENSE
+-rw-rw-rw-   0        0        0      251 2023-07-23 17:51:00.362173 gymnasium_connect_four-1.0.1/PKG-INFO
+-rw-rw-rw-   0        0        0     3334 2023-07-23 17:37:53.000000 gymnasium_connect_four-1.0.1/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 17:51:00.342173 gymnasium_connect_four-1.0.1/connect_four_gymnasium/
+-rw-rw-rw-   0        0        0     8971 2023-07-23 17:49:53.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/ConnectFourEnv.py
+-rw-rw-rw-   0        0        0       42 2023-07-23 15:35:19.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:51:00.354173 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/
+-rw-rw-rw-   0        0        0     4199 2023-07-23 16:48:20.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/AdultPlayer.py
+-rw-rw-rw-   0        0        0     3643 2023-07-23 16:48:25.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/AdultSmarterPlayer.py
+-rw-rw-rw-   0        0        0      295 2023-07-23 16:46:25.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/BabyPlayer.py
+-rw-rw-rw-   0        0        0     1489 2023-07-23 16:46:28.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ChildPlayer.py
+-rw-rw-rw-   0        0        0     1896 2023-07-23 16:48:02.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ChildSmarterPlayer.py
+-rw-rw-rw-   0        0        0      602 2023-07-23 16:51:40.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ConsolePlayer.py
+-rw-rw-rw-   0        0        0     4068 2023-07-23 17:21:33.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/MinMaxPlayer.py
+-rw-rw-rw-   0        0        0      482 2023-07-23 16:51:55.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ModelPlayer.py
+-rw-rw-rw-   0        0        0      393 2023-07-23 15:52:13.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/Player.py
+-rw-rw-rw-   0        0        0     2559 2023-07-23 16:48:37.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/TeenagerPlayer.py
+-rw-rw-rw-   0        0        0     3949 2023-07-23 16:49:03.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/TeenagerSmarterPlayer.py
+-rw-rw-rw-   0        0        0      442 2023-07-23 17:21:40.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:51:00.356172 gymnasium_connect_four-1.0.1/connect_four_gymnasium/tools/
+-rw-rw-rw-   0        0        0     3380 2023-07-23 17:21:26.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/tools/EloLeaderboard.py
+-rw-rw-rw-   0        0        0       42 2023-07-23 16:29:17.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/tools/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:51:00.361172 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/
+-rw-rw-rw-   0        0        0      251 2023-07-23 17:51:00.000000 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      992 2023-07-23 17:51:00.000000 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 17:51:00.000000 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       32 2023-07-23 17:51:00.000000 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       23 2023-07-23 17:51:00.000000 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 17:51:00.363174 gymnasium_connect_four-1.0.1/setup.cfg
+-rw-rw-rw-   0        0        0      517 2023-07-23 17:50:55.000000 gymnasium_connect_four-1.0.1/setup.py
```

### Comparing `gymnasium_connect_four-1.0.0/LICENSE` & `gymnasium_connect_four-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.0/README.md` & `gymnasium_connect_four-1.0.1/README.md`

 * *Files 20% similar despite different names*

```diff
@@ -45,14 +45,29 @@
 5.  TeenagerPlayer:        1644
 6.  MinimaxPlayer depth 2: 1596
 7.  ChildSmarterPlayer:    1548
 8.  ChildPlayer:           1223
 9.  MinimaxPlayer depth 1: 1174
 10. BabyPlayer:             985
 ```
+
+## Testing
+
+We believe in the importance of testing. That's why we have included a suite of tests in the `test` directory. To run the tests, simply use the command `pytest`.
+
+## Contribute & Support
+
+We warmly welcome contributions from the community. If you have an idea for an improvement or found a bug, don't hesitate to open an issue or submit a pull request. Your input is greatly appreciated, and our project is made better by your participation!
+
+If you find this repository useful, please give it a star!
+
+## License
+
+This project is licensed under the MIT License. See the `LICENSE` file for details.
+
 Todo 
 - readme
 - test
 - pip
 - exemple
 - exemple with jupiter
 - bot readme
```

### Comparing `gymnasium_connect_four-1.0.0/connect_four_gymnasium/ConnectFourEnv.py` & `gymnasium_connect_four-1.0.1/connect_four_gymnasium/ConnectFourEnv.py`

 * *Files 0% similar despite different names*

```diff
@@ -172,14 +172,16 @@
         padding_center = 6
         circle_radius = 32
         text_players_size = 90
 
         windows_width = (padding * 2) + (circle_radius * 2 * self.COLUMNS_COUNT) + padding_center * (self.COLUMNS_COUNT - 1)
         end_height_board = (padding * 2) + (circle_radius * 2 * self.ROWS_COUNT) + padding_center * (self.ROWS_COUNT - 1)
         windows_height = end_height_board + text_players_size
+        
+        pygame.font.init()
         # if render GUI, we want to limit the frame rate to X FPS for better visualization
         if self.render_mode == "human":
             self.wait_for_render()
 
         if self.window is None and self.render_mode == "human":
             pygame.init()
             pygame.display.init()
```

### Comparing `gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/AdultPlayer.py` & `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/AdultPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/AdultSmarterPlayer.py` & `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/AdultSmarterPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/ChildPlayer.py` & `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ChildPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/ChildSmarterPlayer.py` & `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ChildSmarterPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/ConsolePlayer.py` & `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ConsolePlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/MinMaxPlayer.py` & `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/MinMaxPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/TeenagerPlayer.py` & `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/TeenagerPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.0/connect_four_gymnasium/players/TeenagerSmarterPlayer.py` & `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/TeenagerSmarterPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.0/connect_four_gymnasium/tools/EloLeaderboard.py` & `gymnasium_connect_four-1.0.1/connect_four_gymnasium/tools/EloLeaderboard.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.0/gymnasium_connect_four.egg-info/SOURCES.txt` & `gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.0/setup.py` & `gymnasium_connect_four-1.0.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from setuptools import setup, find_packages
 
 
 setup(
     name='gymnasium_connect_four',
-    version='1.0.0',
+    version='1.0.1',
     description='A connect 4 (connect four) environment for OpenAI Gym and Gymnasium',
     author='Lucas Bertola',
     url='https://github.com/lucasBertola/Connect-4-env',  
     # author_email='your.email@example.com',
     packages=find_packages(),
     install_requires=[
         'pygame==2.1.3',
```

