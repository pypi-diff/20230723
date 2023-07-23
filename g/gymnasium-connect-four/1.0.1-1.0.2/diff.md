# Comparing `tmp/gymnasium_connect_four-1.0.1.tar.gz` & `tmp/gymnasium_connect_four-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gymnasium_connect_four-1.0.1.tar", last modified: Sun Jul 23 17:51:00 2023, max compression
+gzip compressed data, was "gymnasium_connect_four-1.0.2.tar", last modified: Sun Jul 23 18:00:41 2023, max compression
```

## Comparing `gymnasium_connect_four-1.0.1.tar` & `gymnasium_connect_four-1.0.2.tar`

### file list

```diff
@@ -1,31 +1,31 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 17:51:00.363174 gymnasium_connect_four-1.0.1/
--rw-rw-rw-   0        0        0     1091 2023-07-23 15:11:33.000000 gymnasium_connect_four-1.0.1/LICENSE
--rw-rw-rw-   0        0        0      251 2023-07-23 17:51:00.362173 gymnasium_connect_four-1.0.1/PKG-INFO
--rw-rw-rw-   0        0        0     3334 2023-07-23 17:37:53.000000 gymnasium_connect_four-1.0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 17:51:00.342173 gymnasium_connect_four-1.0.1/connect_four_gymnasium/
--rw-rw-rw-   0        0        0     8971 2023-07-23 17:49:53.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/ConnectFourEnv.py
--rw-rw-rw-   0        0        0       42 2023-07-23 15:35:19.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 17:51:00.354173 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/
--rw-rw-rw-   0        0        0     4199 2023-07-23 16:48:20.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/AdultPlayer.py
--rw-rw-rw-   0        0        0     3643 2023-07-23 16:48:25.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/AdultSmarterPlayer.py
--rw-rw-rw-   0        0        0      295 2023-07-23 16:46:25.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/BabyPlayer.py
--rw-rw-rw-   0        0        0     1489 2023-07-23 16:46:28.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ChildPlayer.py
--rw-rw-rw-   0        0        0     1896 2023-07-23 16:48:02.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ChildSmarterPlayer.py
--rw-rw-rw-   0        0        0      602 2023-07-23 16:51:40.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ConsolePlayer.py
--rw-rw-rw-   0        0        0     4068 2023-07-23 17:21:33.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/MinMaxPlayer.py
--rw-rw-rw-   0        0        0      482 2023-07-23 16:51:55.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ModelPlayer.py
--rw-rw-rw-   0        0        0      393 2023-07-23 15:52:13.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/Player.py
--rw-rw-rw-   0        0        0     2559 2023-07-23 16:48:37.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/TeenagerPlayer.py
--rw-rw-rw-   0        0        0     3949 2023-07-23 16:49:03.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/TeenagerSmarterPlayer.py
--rw-rw-rw-   0        0        0      442 2023-07-23 17:21:40.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 17:51:00.356172 gymnasium_connect_four-1.0.1/connect_four_gymnasium/tools/
--rw-rw-rw-   0        0        0     3380 2023-07-23 17:21:26.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/tools/EloLeaderboard.py
--rw-rw-rw-   0        0        0       42 2023-07-23 16:29:17.000000 gymnasium_connect_four-1.0.1/connect_four_gymnasium/tools/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 17:51:00.361172 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/
--rw-rw-rw-   0        0        0      251 2023-07-23 17:51:00.000000 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      992 2023-07-23 17:51:00.000000 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 17:51:00.000000 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       32 2023-07-23 17:51:00.000000 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/requires.txt
--rw-rw-rw-   0        0        0       23 2023-07-23 17:51:00.000000 gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 17:51:00.363174 gymnasium_connect_four-1.0.1/setup.cfg
--rw-rw-rw-   0        0        0      517 2023-07-23 17:50:55.000000 gymnasium_connect_four-1.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:00:41.304881 gymnasium_connect_four-1.0.2/
+-rw-rw-rw-   0        0        0     1091 2023-07-23 15:11:33.000000 gymnasium_connect_four-1.0.2/LICENSE
+-rw-rw-rw-   0        0        0      251 2023-07-23 18:00:41.303879 gymnasium_connect_four-1.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0     3334 2023-07-23 17:37:53.000000 gymnasium_connect_four-1.0.2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 18:00:41.282882 gymnasium_connect_four-1.0.2/connect_four_gymnasium/
+-rw-rw-rw-   0        0        0     9016 2023-07-23 18:00:27.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/ConnectFourEnv.py
+-rw-rw-rw-   0        0        0       42 2023-07-23 15:35:19.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:00:41.293880 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/
+-rw-rw-rw-   0        0        0     4199 2023-07-23 16:48:20.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/AdultPlayer.py
+-rw-rw-rw-   0        0        0     3643 2023-07-23 16:48:25.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/AdultSmarterPlayer.py
+-rw-rw-rw-   0        0        0      295 2023-07-23 16:46:25.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/BabyPlayer.py
+-rw-rw-rw-   0        0        0     1489 2023-07-23 16:46:28.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/ChildPlayer.py
+-rw-rw-rw-   0        0        0     1896 2023-07-23 16:48:02.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/ChildSmarterPlayer.py
+-rw-rw-rw-   0        0        0      602 2023-07-23 16:51:40.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/ConsolePlayer.py
+-rw-rw-rw-   0        0        0     4068 2023-07-23 17:21:33.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/MinMaxPlayer.py
+-rw-rw-rw-   0        0        0      482 2023-07-23 16:51:55.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/ModelPlayer.py
+-rw-rw-rw-   0        0        0      393 2023-07-23 15:52:13.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/Player.py
+-rw-rw-rw-   0        0        0     2559 2023-07-23 16:48:37.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/TeenagerPlayer.py
+-rw-rw-rw-   0        0        0     3949 2023-07-23 16:49:03.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/TeenagerSmarterPlayer.py
+-rw-rw-rw-   0        0        0      442 2023-07-23 17:21:40.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:00:41.296882 gymnasium_connect_four-1.0.2/connect_four_gymnasium/tools/
+-rw-rw-rw-   0        0        0     3380 2023-07-23 17:21:26.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/tools/EloLeaderboard.py
+-rw-rw-rw-   0        0        0       42 2023-07-23 16:29:17.000000 gymnasium_connect_four-1.0.2/connect_four_gymnasium/tools/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:00:41.302879 gymnasium_connect_four-1.0.2/gymnasium_connect_four.egg-info/
+-rw-rw-rw-   0        0        0      251 2023-07-23 18:00:41.000000 gymnasium_connect_four-1.0.2/gymnasium_connect_four.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      992 2023-07-23 18:00:41.000000 gymnasium_connect_four-1.0.2/gymnasium_connect_four.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 18:00:41.000000 gymnasium_connect_four-1.0.2/gymnasium_connect_four.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       32 2023-07-23 18:00:41.000000 gymnasium_connect_four-1.0.2/gymnasium_connect_four.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       23 2023-07-23 18:00:41.000000 gymnasium_connect_four-1.0.2/gymnasium_connect_four.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 18:00:41.304881 gymnasium_connect_four-1.0.2/setup.cfg
+-rw-rw-rw-   0        0        0      517 2023-07-23 18:00:32.000000 gymnasium_connect_four-1.0.2/setup.py
```

### Comparing `gymnasium_connect_four-1.0.1/LICENSE` & `gymnasium_connect_four-1.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/README.md` & `gymnasium_connect_four-1.0.2/README.md`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/connect_four_gymnasium/ConnectFourEnv.py` & `gymnasium_connect_four-1.0.2/connect_four_gymnasium/ConnectFourEnv.py`

 * *Files 2% similar despite different names*

```diff
@@ -225,13 +225,13 @@
         canvas.blit(text, (80, text_position_y_second_player))
 
         if self.render_mode == "human":
             self.window.blit(canvas, canvas.get_rect())
             pygame.event.pump()
             pygame.display.update()
         else:
-            return np.transpose
+            return np.transpose(pygame.surfarray.array3d(canvas), (1, 0, 2))
         
         def close(self):
             if self.window is not None:
                 pygame.display.quit()
                 pygame.quit()
```

### Comparing `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/AdultPlayer.py` & `gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/AdultPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/AdultSmarterPlayer.py` & `gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/AdultSmarterPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ChildPlayer.py` & `gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/ChildPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ChildSmarterPlayer.py` & `gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/ChildSmarterPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/ConsolePlayer.py` & `gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/ConsolePlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/MinMaxPlayer.py` & `gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/MinMaxPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/TeenagerPlayer.py` & `gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/TeenagerPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/connect_four_gymnasium/players/TeenagerSmarterPlayer.py` & `gymnasium_connect_four-1.0.2/connect_four_gymnasium/players/TeenagerSmarterPlayer.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/connect_four_gymnasium/tools/EloLeaderboard.py` & `gymnasium_connect_four-1.0.2/connect_four_gymnasium/tools/EloLeaderboard.py`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/gymnasium_connect_four.egg-info/SOURCES.txt` & `gymnasium_connect_four-1.0.2/gymnasium_connect_four.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `gymnasium_connect_four-1.0.1/setup.py` & `gymnasium_connect_four-1.0.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from setuptools import setup, find_packages
 
 
 setup(
     name='gymnasium_connect_four',
-    version='1.0.1',
+    version='1.0.2',
     description='A connect 4 (connect four) environment for OpenAI Gym and Gymnasium',
     author='Lucas Bertola',
     url='https://github.com/lucasBertola/Connect-4-env',  
     # author_email='your.email@example.com',
     packages=find_packages(),
     install_requires=[
         'pygame==2.1.3',
```

