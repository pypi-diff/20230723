# Comparing `tmp/fusion-engine-0.2.4.tar.gz` & `tmp/fusion-engine-0.2.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fusion-engine-0.2.4.tar", last modified: Thu Jul 20 12:22:11 2023, max compression
+gzip compressed data, was "fusion-engine-0.2.5.tar", last modified: Sun Jul 23 14:45:21 2023, max compression
```

## Comparing `fusion-engine-0.2.4.tar` & `fusion-engine-0.2.5.tar`

### file list

```diff
@@ -1,37 +1,37 @@
-drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-20 12:22:11.505118 fusion-engine-0.2.4/
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     1071 2023-07-02 09:01:28.000000 fusion-engine-0.2.4/LICENCE.md
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     5099 2023-07-20 12:22:11.503915 fusion-engine-0.2.4/PKG-INFO
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     3856 2023-07-20 10:41:07.000000 fusion-engine-0.2.4/README.md
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     1647 2023-07-20 12:21:59.000000 fusion-engine-0.2.4/pyproject.toml
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)       24 2023-07-07 14:54:41.000000 fusion-engine-0.2.4/requirements.txt
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)       38 2023-07-20 12:22:11.505366 fusion-engine-0.2.4/setup.cfg
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     1018 2023-07-12 18:18:50.000000 fusion-engine-0.2.4/setup.py
-drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-20 12:22:11.465794 fusion-engine-0.2.4/src/
-drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-20 12:22:11.474852 fusion-engine-0.2.4/src/fusion_engine.egg-info/
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     5099 2023-07-20 12:22:11.000000 fusion-engine-0.2.4/src/fusion_engine.egg-info/PKG-INFO
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      881 2023-07-20 12:22:11.000000 fusion-engine-0.2.4/src/fusion_engine.egg-info/SOURCES.txt
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)        1 2023-07-20 12:22:11.000000 fusion-engine-0.2.4/src/fusion_engine.egg-info/dependency_links.txt
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)       25 2023-07-20 12:22:11.000000 fusion-engine-0.2.4/src/fusion_engine.egg-info/requires.txt
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)       13 2023-07-20 12:22:11.000000 fusion-engine-0.2.4/src/fusion_engine.egg-info/top_level.txt
-drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-20 12:22:11.475921 fusion-engine-0.2.4/src/fusionengine/
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      894 2023-07-20 12:21:48.000000 fusion-engine-0.2.4/src/fusionengine/__init__.py
-drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-20 12:22:11.477067 fusion-engine-0.2.4/src/fusionengine/debugfiles/
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)    64239 2023-07-07 11:13:39.000000 fusion-engine-0.2.4/src/fusionengine/debugfiles/fe.png
-drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-20 12:22:11.501858 fusion-engine-0.2.4/src/fusionengine/files/
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     3439 2023-07-10 21:29:12.000000 fusion-engine-0.2.4/src/fusionengine/files/body.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     1372 2023-07-14 21:16:17.000000 fusion-engine-0.2.4/src/fusionengine/files/color.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      382 2023-07-04 15:09:45.000000 fusion-engine-0.2.4/src/fusionengine/files/data.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      105 2023-07-20 10:28:33.000000 fusion-engine-0.2.4/src/fusionengine/files/debug.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     2409 2023-07-09 21:02:50.000000 fusion-engine-0.2.4/src/fusionengine/files/draw.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      232 2023-07-16 22:38:57.000000 fusion-engine-0.2.4/src/fusionengine/files/enums.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)    10707 2023-07-09 21:03:18.000000 fusion-engine-0.2.4/src/fusionengine/files/event.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)       91 2023-07-02 09:01:28.000000 fusion-engine-0.2.4/src/fusionengine/files/exceptions.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      113 2023-07-16 22:46:12.000000 fusion-engine-0.2.4/src/fusionengine/files/fonts.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      904 2023-07-09 20:56:06.000000 fusion-engine-0.2.4/src/fusionengine/files/image.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      557 2023-07-20 10:26:42.000000 fusion-engine-0.2.4/src/fusionengine/files/imports.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)        0 2023-06-11 19:02:09.000000 fusion-engine-0.2.4/src/fusionengine/files/physics.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      537 2023-07-09 21:03:30.000000 fusion-engine-0.2.4/src/fusionengine/files/shape.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     5566 2023-07-02 09:01:28.000000 fusion-engine-0.2.4/src/fusionengine/files/storage.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      792 2023-07-09 21:03:41.000000 fusion-engine-0.2.4/src/fusionengine/files/systems.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     3234 2023-07-19 08:46:10.000000 fusion-engine-0.2.4/src/fusionengine/files/ui.py
--rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     1867 2023-07-14 21:27:23.000000 fusion-engine-0.2.4/src/fusionengine/files/window.py
+drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-23 14:45:21.225293 fusion-engine-0.2.5/
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     1071 2023-07-02 09:01:28.000000 fusion-engine-0.2.5/LICENCE.md
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     5200 2023-07-23 14:45:21.224599 fusion-engine-0.2.5/PKG-INFO
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     3957 2023-07-22 09:11:24.000000 fusion-engine-0.2.5/README.md
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     1647 2023-07-22 09:10:37.000000 fusion-engine-0.2.5/pyproject.toml
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)       24 2023-07-07 14:54:41.000000 fusion-engine-0.2.5/requirements.txt
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)       38 2023-07-23 14:45:21.225485 fusion-engine-0.2.5/setup.cfg
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     1020 2023-07-23 14:45:14.000000 fusion-engine-0.2.5/setup.py
+drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-23 14:45:21.194755 fusion-engine-0.2.5/src/
+drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-23 14:45:21.205520 fusion-engine-0.2.5/src/fusion_engine.egg-info/
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     5200 2023-07-23 14:45:20.000000 fusion-engine-0.2.5/src/fusion_engine.egg-info/PKG-INFO
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      881 2023-07-23 14:45:20.000000 fusion-engine-0.2.5/src/fusion_engine.egg-info/SOURCES.txt
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)        1 2023-07-23 14:45:20.000000 fusion-engine-0.2.5/src/fusion_engine.egg-info/dependency_links.txt
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)       25 2023-07-23 14:45:20.000000 fusion-engine-0.2.5/src/fusion_engine.egg-info/requires.txt
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)       13 2023-07-23 14:45:20.000000 fusion-engine-0.2.5/src/fusion_engine.egg-info/top_level.txt
+drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-23 14:45:21.206636 fusion-engine-0.2.5/src/fusionengine/
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      854 2023-07-23 14:45:10.000000 fusion-engine-0.2.5/src/fusionengine/__init__.py
+drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-23 14:45:21.207589 fusion-engine-0.2.5/src/fusionengine/debugfiles/
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)    64239 2023-07-07 11:13:39.000000 fusion-engine-0.2.5/src/fusionengine/debugfiles/fe.png
+drwxr-xr-x   0 dmarhitych-pro   (501) staff       (20)        0 2023-07-23 14:45:21.223393 fusion-engine-0.2.5/src/fusionengine/files/
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     3384 2023-07-22 19:36:51.000000 fusion-engine-0.2.5/src/fusionengine/files/body.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     1372 2023-07-14 21:16:17.000000 fusion-engine-0.2.5/src/fusionengine/files/color.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      382 2023-07-04 15:09:45.000000 fusion-engine-0.2.5/src/fusionengine/files/data.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      105 2023-07-20 10:28:33.000000 fusion-engine-0.2.5/src/fusionengine/files/debug.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     2510 2023-07-21 11:57:23.000000 fusion-engine-0.2.5/src/fusionengine/files/draw.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      232 2023-07-16 22:38:57.000000 fusion-engine-0.2.5/src/fusionengine/files/enums.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)    10707 2023-07-09 21:03:18.000000 fusion-engine-0.2.5/src/fusionengine/files/event.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)       91 2023-07-02 09:01:28.000000 fusion-engine-0.2.5/src/fusionengine/files/exceptions.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      113 2023-07-16 22:46:12.000000 fusion-engine-0.2.5/src/fusionengine/files/fonts.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      905 2023-07-23 14:27:15.000000 fusion-engine-0.2.5/src/fusionengine/files/image.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      557 2023-07-20 10:26:42.000000 fusion-engine-0.2.5/src/fusionengine/files/imports.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)        0 2023-06-11 19:02:09.000000 fusion-engine-0.2.5/src/fusionengine/files/physics.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      537 2023-07-09 21:03:30.000000 fusion-engine-0.2.5/src/fusionengine/files/shape.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     5566 2023-07-02 09:01:28.000000 fusion-engine-0.2.5/src/fusionengine/files/storage.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)      792 2023-07-09 21:03:41.000000 fusion-engine-0.2.5/src/fusionengine/files/systems.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     3678 2023-07-22 19:42:38.000000 fusion-engine-0.2.5/src/fusionengine/files/ui.py
+-rw-r--r--   0 dmarhitych-pro   (501) staff       (20)     2050 2023-07-23 14:41:55.000000 fusion-engine-0.2.5/src/fusionengine/files/window.py
```

### Comparing `fusion-engine-0.2.4/LICENCE.md` & `fusion-engine-0.2.5/LICENCE.md`

 * *Files identical despite different names*

### Comparing `fusion-engine-0.2.4/PKG-INFO` & `fusion-engine-0.2.5/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fusion-engine
-Version: 0.2.4
+Version: 0.2.5
 Summary: This a fully custom engine based on Python and PySDL2, it's written in pure Python!
 Author-email: Dimkauzh <uzhdimka@gmail.com>
 License: LICENSE.md
 Keywords: game,python,gamedev,game-engine,sdl2,game-development,pure-python,sdl2-mixer,sdl2-ttf,sdl2-image,python-game,pysdl2,sdl2-library,python-game-library,python-game-engine,python-games
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
@@ -37,15 +37,15 @@
 
 We have our own website with our docs on it. Things like information could be a little outdated, but the docs are hosted there. [See here](https://dimkauzh.github.io/fusion-engine/)
 
 ### 💻 Development
 
 Keep in mind that this project is in work, so if you want to see code,
 then it is in dev branch but there is no 'full version' of this project!
-We working hard to make first alpha version of it!
+We're working hard to make first alpha version of it!
 
 ## 💾 Installation
 
 To install our package, run this:
 
 ```bash
   pip install fusion-engine
@@ -78,14 +78,15 @@
 
 ## 📃 Documentation
 
 See at [The wiki of the project](https://dimkauzh.github.io/fusion-engine/wiki/wiki.html) (Still in work!)
 
 ## 📯 Coming features
 
+### 🛠️ Features we are working on
 We are working hard to implement very basic and complex stuff so our engine becomes more rigid. These features are worked on or will be worked on:
 
 - [x] Engine
   - [x] Create window
   - [x] Draw shapes
   - [x] Draw images
   - [x] Input
@@ -108,38 +109,39 @@
     - [ ] File support
     - [ ] And more...
 - [ ] CLI
   - [ ] Create CLI to build your game
   - [ ] Creates a full project
   - [ ] Will create a full project dir
 
-### Features that maybe will be implemented
+### 🔩 Features that maybe will be implemented
 
 - [ ] UI (Using own GUI library)
   - [ ] Menu
   - [ ] Create project
   - [ ] Editor
   - [ ] Code editor build in
   - [ ] Run game
 
-- If you have more ideas, please tell us them in our [discord group](https://discord.gg/Smg3CK4ZMc)!
+💡 - If you have more ideas, please tell us them in our [discord group](https://discord.gg/Smg3CK4ZMc) or create an issue!
 
 ## 🗄️ About
 
+### ⚙️ Engine
 Fusion Engine is currently (6/14/2023) build with Python and some Python libraries:
 
 - PySDL2 is used for rendering and windowing
 - PySDL2-DLL is used by PySDL2 for SDL2 binaries
-- PyMunk is used for fysics simulation
-- TKinter for UI
+- PyMunk is used for physics simulation
+- Custom build in UI for UI
 - Setuptools for PyPi package
 - Json for storing data
 
 This project began May 1, 2023. The original project began in C, but it's entirely rewritten in Python for it's big userbase and ease of use (productivity). This is actually also my EuroPython 2023 project.
 
 ### 🇺🇦 Ukraine
 We as fusion team support Ukraine and we hope it will win. Fusion engine is dedicated to Ukraine fighting the Russian invasion.
 🇺🇦 Please support Ukraine! 🇺🇦
 
 ## 🚀 About Me
 
-A 13 year old game developer with much passion about game development. So I made this project to grow my programming skills and just make a tool that I can use for myself or a tool for other people to help them develop games.
+A 13-year-old game developer with much passion about game development. So I made this project to grow my programming skills and just make a tool that I can use for myself or a tool for other people to help them develop games.
```

### Comparing `fusion-engine-0.2.4/README.md` & `fusion-engine-0.2.5/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 
 We have our own website with our docs on it. Things like information could be a little outdated, but the docs are hosted there. [See here](https://dimkauzh.github.io/fusion-engine/)
 
 ### 💻 Development
 
 Keep in mind that this project is in work, so if you want to see code,
 then it is in dev branch but there is no 'full version' of this project!
-We working hard to make first alpha version of it!
+We're working hard to make first alpha version of it!
 
 ## 💾 Installation
 
 To install our package, run this:
 
 ```bash
   pip install fusion-engine
@@ -51,14 +51,15 @@
 
 ## 📃 Documentation
 
 See at [The wiki of the project](https://dimkauzh.github.io/fusion-engine/wiki/wiki.html) (Still in work!)
 
 ## 📯 Coming features
 
+### 🛠️ Features we are working on
 We are working hard to implement very basic and complex stuff so our engine becomes more rigid. These features are worked on or will be worked on:
 
 - [x] Engine
   - [x] Create window
   - [x] Draw shapes
   - [x] Draw images
   - [x] Input
@@ -81,38 +82,39 @@
     - [ ] File support
     - [ ] And more...
 - [ ] CLI
   - [ ] Create CLI to build your game
   - [ ] Creates a full project
   - [ ] Will create a full project dir
 
-### Features that maybe will be implemented
+### 🔩 Features that maybe will be implemented
 
 - [ ] UI (Using own GUI library)
   - [ ] Menu
   - [ ] Create project
   - [ ] Editor
   - [ ] Code editor build in
   - [ ] Run game
 
-- If you have more ideas, please tell us them in our [discord group](https://discord.gg/Smg3CK4ZMc)!
+💡 - If you have more ideas, please tell us them in our [discord group](https://discord.gg/Smg3CK4ZMc) or create an issue!
 
 ## 🗄️ About
 
+### ⚙️ Engine
 Fusion Engine is currently (6/14/2023) build with Python and some Python libraries:
 
 - PySDL2 is used for rendering and windowing
 - PySDL2-DLL is used by PySDL2 for SDL2 binaries
-- PyMunk is used for fysics simulation
-- TKinter for UI
+- PyMunk is used for physics simulation
+- Custom build in UI for UI
 - Setuptools for PyPi package
 - Json for storing data
 
 This project began May 1, 2023. The original project began in C, but it's entirely rewritten in Python for it's big userbase and ease of use (productivity). This is actually also my EuroPython 2023 project.
 
 ### 🇺🇦 Ukraine
 We as fusion team support Ukraine and we hope it will win. Fusion engine is dedicated to Ukraine fighting the Russian invasion.
 🇺🇦 Please support Ukraine! 🇺🇦
 
 ## 🚀 About Me
 
-A 13 year old game developer with much passion about game development. So I made this project to grow my programming skills and just make a tool that I can use for myself or a tool for other people to help them develop games.
+A 13-year-old game developer with much passion about game development. So I made this project to grow my programming skills and just make a tool that I can use for myself or a tool for other people to help them develop games.
```

### Comparing `fusion-engine-0.2.4/pyproject.toml` & `fusion-engine-0.2.5/pyproject.toml`

 * *Files identical despite different names*

### Comparing `fusion-engine-0.2.4/setup.py` & `fusion-engine-0.2.5/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -30,8 +30,10 @@
             for path in glob.glob(dir):
                 print("removing", path)
                 removed_dirs += 1
             if os.path.exists(dir):
                 shutil.rmtree(dir)
         print(f"removed {removed_files} files and {removed_dirs} directories")
 
+
+
 setup(cmdclass={"clean": clean})
```

### Comparing `fusion-engine-0.2.4/src/fusion_engine.egg-info/PKG-INFO` & `fusion-engine-0.2.5/src/fusion_engine.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fusion-engine
-Version: 0.2.4
+Version: 0.2.5
 Summary: This a fully custom engine based on Python and PySDL2, it's written in pure Python!
 Author-email: Dimkauzh <uzhdimka@gmail.com>
 License: LICENSE.md
 Keywords: game,python,gamedev,game-engine,sdl2,game-development,pure-python,sdl2-mixer,sdl2-ttf,sdl2-image,python-game,pysdl2,sdl2-library,python-game-library,python-game-engine,python-games
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
@@ -37,15 +37,15 @@
 
 We have our own website with our docs on it. Things like information could be a little outdated, but the docs are hosted there. [See here](https://dimkauzh.github.io/fusion-engine/)
 
 ### 💻 Development
 
 Keep in mind that this project is in work, so if you want to see code,
 then it is in dev branch but there is no 'full version' of this project!
-We working hard to make first alpha version of it!
+We're working hard to make first alpha version of it!
 
 ## 💾 Installation
 
 To install our package, run this:
 
 ```bash
   pip install fusion-engine
@@ -78,14 +78,15 @@
 
 ## 📃 Documentation
 
 See at [The wiki of the project](https://dimkauzh.github.io/fusion-engine/wiki/wiki.html) (Still in work!)
 
 ## 📯 Coming features
 
+### 🛠️ Features we are working on
 We are working hard to implement very basic and complex stuff so our engine becomes more rigid. These features are worked on or will be worked on:
 
 - [x] Engine
   - [x] Create window
   - [x] Draw shapes
   - [x] Draw images
   - [x] Input
@@ -108,38 +109,39 @@
     - [ ] File support
     - [ ] And more...
 - [ ] CLI
   - [ ] Create CLI to build your game
   - [ ] Creates a full project
   - [ ] Will create a full project dir
 
-### Features that maybe will be implemented
+### 🔩 Features that maybe will be implemented
 
 - [ ] UI (Using own GUI library)
   - [ ] Menu
   - [ ] Create project
   - [ ] Editor
   - [ ] Code editor build in
   - [ ] Run game
 
-- If you have more ideas, please tell us them in our [discord group](https://discord.gg/Smg3CK4ZMc)!
+💡 - If you have more ideas, please tell us them in our [discord group](https://discord.gg/Smg3CK4ZMc) or create an issue!
 
 ## 🗄️ About
 
+### ⚙️ Engine
 Fusion Engine is currently (6/14/2023) build with Python and some Python libraries:
 
 - PySDL2 is used for rendering and windowing
 - PySDL2-DLL is used by PySDL2 for SDL2 binaries
-- PyMunk is used for fysics simulation
-- TKinter for UI
+- PyMunk is used for physics simulation
+- Custom build in UI for UI
 - Setuptools for PyPi package
 - Json for storing data
 
 This project began May 1, 2023. The original project began in C, but it's entirely rewritten in Python for it's big userbase and ease of use (productivity). This is actually also my EuroPython 2023 project.
 
 ### 🇺🇦 Ukraine
 We as fusion team support Ukraine and we hope it will win. Fusion engine is dedicated to Ukraine fighting the Russian invasion.
 🇺🇦 Please support Ukraine! 🇺🇦
 
 ## 🚀 About Me
 
-A 13 year old game developer with much passion about game development. So I made this project to grow my programming skills and just make a tool that I can use for myself or a tool for other people to help them develop games.
+A 13-year-old game developer with much passion about game development. So I made this project to grow my programming skills and just make a tool that I can use for myself or a tool for other people to help them develop games.
```

### Comparing `fusion-engine-0.2.4/src/fusion_engine.egg-info/SOURCES.txt` & `fusion-engine-0.2.5/src/fusion_engine.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `fusion-engine-0.2.4/src/fusionengine/__init__.py` & `fusion-engine-0.2.5/src/fusionengine/__init__.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,13 +1,11 @@
 __author__ = "Dimkauzh"
-__version__ = "0.2.4"
+__version__ = "0.2.5"
 
-import fusionengine.files.data as data
 import fusionengine.files.systems as sysconfig
-
 from fusionengine.files.imports import *
 
 class Main:
     def __init__(self):
         sdl2.SDL_Init(sdl2.SDL_INIT_VIDEO)
         self.window = window.Window()
         self.color = color.Colors()
```

### Comparing `fusion-engine-0.2.4/src/fusionengine/debugfiles/fe.png` & `fusion-engine-0.2.5/src/fusionengine/debugfiles/fe.png`

 * *Files identical despite different names*

### Comparing `fusion-engine-0.2.4/src/fusionengine/files/body.py` & `fusion-engine-0.2.5/src/fusionengine/files/body.py`

 * *Files 5% similar despite different names*

```diff
@@ -42,24 +42,22 @@
         if bodytype == BodyType.RIGID_BODY:
             self.body = _RigidBody(self.window,
                                    self.x,
                                    self.y,
                                    self.width,
                                    self.height
                                    )
-            self._addspace.append(self.body.body)
         else:
             self.body = _StaticBody(self.window,
                                     self.x,
                                     self.y,
                                     self.width,
                                     self.height
                                     )
-            self._addspace.append(self.body.body)
-
+        self._addspace.append(self.body.body)
         self._set_body_data(self.x, self.y, self.width, self.height, self.body.space)
         self.box = pymunk.Poly.create_box(self.body.body)
         self._addspace.append(self.box)
 
         self._addspaces()
 
     def image(self, window: window._CustomRenderer, image_path: str, x: int, y: int, width: int, height: int) -> None:
```

### Comparing `fusion-engine-0.2.4/src/fusionengine/files/color.py` & `fusion-engine-0.2.5/src/fusionengine/files/color.py`

 * *Files identical despite different names*

### Comparing `fusion-engine-0.2.4/src/fusionengine/files/draw.py` & `fusion-engine-0.2.5/src/fusionengine/files/draw.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,57 +1,58 @@
 import fusionengine.files.systems as sysconfig
 import fusionengine.files.window as window
 
 from fusionengine.files.imports import *
 import fusionengine.files.shape as shape
 
+
 class Draw:
     def __init__(self) -> None:
         self.rendereroptions = sysconfig.RendererOptions()
 
     def draw_line(self, window: window._CustomRenderer, x1: int, y1: int, x2: int, y2: int, color: tuple) -> None:
         sdl2.SDL_SetRenderDrawColor(window.renderer,
-                               color[0],
-                               color[1],
-                               color[2],
-                               color[3]
-                               )
+                                    color[0],
+                                    color[1],
+                                    color[2],
+                                    color[3]
+                                    )
 
         sdl2.SDL_RenderDrawLine(window.renderer, x1, y1, x2, y2)
 
     def draw_line_rect(self, window: window._CustomRenderer, x: int, y: int, width: int, height: int, color: tuple) -> None:
         rdr = window.renderer
         self.draw_line(rdr, x, y, x + width, y, color)
         self.draw_line(rdr, x, y + height, x + width, y + height, color)
         self.draw_line(rdr, x, y, x, y + height, color)
         self.draw_line(rdr, x + width, y, x + width, y + height, color)
 
     def draw_rect(self, window: window._CustomRenderer, x: int, y: int, width: int, height: int, color: tuple) -> None:
         sdl2.SDL_SetRenderDrawColor(window.renderer,
-                               color[0],
-                               color[1],
-                               color[2],
-                               color[3]
-                               )
+                                    color[0],
+                                    color[1],
+                                    color[2],
+                                    color[3]
+                                    )
 
         rect = sdl2.SDL_Rect(x, y, width, height)
         sdl2.SDL_RenderFillRect(window.renderer, rect)
 
     def draw_own_rect(self, window: window._CustomRenderer, rect: shape._CustomShape) -> None:
         sdl2.SDL_SetRenderDrawColor(window.renderer,
-                               rect.color[0],
-                               rect.color[1],
-                               rect.color[2],
-                               rect.color[3]
-                               )
+                                    rect.color[0],
+                                    rect.color[1],
+                                    rect.color[2],
+                                    rect.color[3]
+                                    )
 
         sdl2.SDL_RenderFillRect(window.renderer, rect.rect)
 
     def set_background_color(self, window: window._CustomRenderer, color: tuple) -> None:
         sdl2.SDL_SetRenderDrawColor(window.renderer,
-                               color[0],
-                               color[1],
-                               color[2],
-                               color[3]
-                               )
+                                    color[0],
+                                    color[1],
+                                    color[2],
+                                    color[3]
+                                    )
 
         sdl2.SDL_RenderClear(window.renderer)
```

### Comparing `fusion-engine-0.2.4/src/fusionengine/files/event.py` & `fusion-engine-0.2.5/src/fusionengine/files/event.py`

 * *Files identical despite different names*

### Comparing `fusion-engine-0.2.4/src/fusionengine/files/image.py` & `fusion-engine-0.2.5/src/fusionengine/files/image.py`

 * *Files 10% similar despite different names*

```diff
@@ -13,9 +13,9 @@
     def open_image(self, window: window._CustomRenderer, image, x: int, y: int, width: int, height: int) -> _CustomImage:
         image = sdl2.ext.load_image(image)
         texture = sdl2.SDL_CreateTextureFromSurface(window.renderer, image)
         rect = sdl2.SDL_Rect(x, y, width, height)
         return _CustomImage(window, texture, rect)
 
     def draw_image(self, image: _CustomImage) -> None:
-        sdl2.SDL_RenderClear(image.renderer)
+        #sdl2.SDL_RenderClear(image.renderer)
         sdl2.SDL_RenderCopy(image.renderer, image.texture, None, image.rect)
```

### Comparing `fusion-engine-0.2.4/src/fusionengine/files/imports.py` & `fusion-engine-0.2.5/src/fusionengine/files/imports.py`

 * *Files identical despite different names*

### Comparing `fusion-engine-0.2.4/src/fusionengine/files/shape.py` & `fusion-engine-0.2.5/src/fusionengine/files/shape.py`

 * *Files identical despite different names*

### Comparing `fusion-engine-0.2.4/src/fusionengine/files/storage.py` & `fusion-engine-0.2.5/src/fusionengine/files/storage.py`

 * *Files identical despite different names*

### Comparing `fusion-engine-0.2.4/src/fusionengine/files/systems.py` & `fusion-engine-0.2.5/src/fusionengine/files/systems.py`

 * *Files identical despite different names*

### Comparing `fusion-engine-0.2.4/src/fusionengine/files/ui.py` & `fusion-engine-0.2.5/src/fusionengine/files/ui.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,27 +1,29 @@
 from fusionengine.files.imports import *
 import fusionengine.files.draw as draw
+import fusionengine.files.window as windowfe
+
 
 class CustomButton:
-    def __init__(self, window, text, x, y, width, height, font_path, font_size_input, centre, color_input):
-        self.window = window
-        self.text = text
-        self.x = x
-        self.y = y
+    def __init__(self, window: window._CustomRenderer, text: str, x: int, y: int, width: int, height: int, font_path: str, font_sharp: int, centre: int, color_input: tuple) -> None:
+        self.window: windowfe._CustomRenderer = window
+        self.text: str = text
+        self.x: int = x
+        self.y: int = y
         self.width = width
         self.height = height
         self.font_path = font_path
-        self.font_size_input = font_size_input
+        self.font_size_input = font_sharp
         self.color = (color_input[0], color_input[1], color_input[2], color_input[3])
         self.is_pressed = False
-    
-        if font_size_input == "default":
+
+        if self.font_size_input == "default":
             font_size = 1000
         else:
-            font_size = font_size_input
+            font_size = font_sharp
 
         draw.Draw().draw_rect(window, x, y, width, height, self.color)
 
         sdl2.sdlttf.TTF_Init()
         self.font = sdl2.sdlttf.TTF_OpenFont(font_path.encode("utf-8"), font_size)
 
         text_surface = sdl2.sdlttf.TTF_RenderText_Solid(self.font, text.encode(), sdl2.SDL_Color(0, 0, 0))
@@ -29,58 +31,62 @@
         text_rect = sdl2.SDL_Rect(x + centre, y + centre, width - centre * 2, height - centre * 2)
         sdl2.SDL_RenderCopy(self.window.renderer, self.texture, None, text_rect)
 
         sdl2.sdlttf.TTF_CloseFont(self.font)
         sdl2.SDL_FreeSurface(text_surface)
         sdl2.sdlttf.TTF_Quit()
 
-    def _handle_event(self):
+    def _handle_event(self) -> bool:
         event = self.window.event
         _pressed = False
         if event.type == sdl2.SDL_MOUSEBUTTONDOWN:
             mouse_x, mouse_y = event.button.x, event.button.y
             if self.x <= mouse_x <= self.x + self.width and self.y <= mouse_y <= self.y + self.height:
                 _pressed = True
         elif event.type == sdl2.SDL_MOUSEBUTTONUP:
             _pressed = False
 
         return _pressed
 
-    def is_button_pressed(self):
+    def is_button_pressed(self) -> bool:
         return self._handle_event()
-    
-    def set_color(self, color):
+
+    def set_color(self, color: tuple) -> None:
         self.color = color
 
-    def button_pressed(self, func):
+    def button_pressed(self, func: callable) -> None:
         if self.is_button_pressed() and callable(func):
             func()
 
+
 class Button:
-    def __init__(self):
+    def __init__(self) -> None: 
         pass
 
-    def new_button(self, window, text, x, y, width, height, font_path, font_size, centre, color):
-        return CustomButton(window, text, x, y, width, height, font_path, font_size, centre, color)
+    def new_button(self, window: window._CustomRenderer, text: str, x: int, y: int, width: int, height: int, font_path: str, font_sharp: int, centre: int, color: tuple) -> CustomButton:
+        return CustomButton(window, text, x, y, width, height, font_path, font_sharp, centre, color)
+
 
 class Text:
-    def __init__(self):
+    def __init__(self) -> None:
         pass
 
-    def print_text(self, window, text, x, y, width, height, font_path, font_sharp, color):
+    def print_text(self, window: window._CustomRenderer, text: str, x: int, y: int, width: int, height: int, font_path: str, font_sharp: int, color: tuple) -> None:
         sdl2.sdlttf.TTF_Init()
         self.font = sdl2.sdlttf.TTF_OpenFont(font_path.encode("utf-8"), font_sharp)
         sdl2.SDL_SetRenderDrawColor(window.renderer, color[0], color[1], color[2], color[3])
 
-        text_surface = sdl2.sdlttf.TTF_RenderText_Solid(self.font, text.encode(), sdl2.SDL_Color(color[0], color[1], color[2], color[3]))
+        text_surface = sdl2.sdlttf.TTF_RenderText_Solid(self.font, text.encode(),
+                                                        sdl2.SDL_Color(color[0], color[1], color[2], color[3]))
         self.texture = sdl2.SDL_CreateTextureFromSurface(window.renderer, text_surface)
         text_rect = sdl2.SDL_Rect(x, y, width, height)
         sdl2.SDL_RenderCopy(window.renderer, self.texture, None, text_rect)
 
         sdl2.sdlttf.TTF_CloseFont(self.font)
         sdl2.SDL_FreeSurface(text_surface)
         sdl2.sdlttf.TTF_Quit()
 
+
 class UI:
-    def __init__(self):
+    def __init__(self) -> None:
         self.button = Button()
         self.text = Text()
```

### Comparing `fusion-engine-0.2.4/src/fusionengine/files/window.py` & `fusion-engine-0.2.5/src/fusionengine/files/window.py`

 * *Files 16% similar despite different names*

```diff
@@ -22,28 +22,36 @@
                                        sdl2.SDL_WINDOWPOS_CENTERED,
                                        width,
                                        height,
                                        sdl2.SDL_WINDOW_SHOWN
                                        )
         self._running = True
         self.window = _CustomRenderer(self.window_window)
+
         return self.window
 
     def loop(self, your_loop):
-        while self.running(self.window):
+        while self._running:
+            self._refresh(self.window)
             your_loop()
 
     def running(self, window:_CustomRenderer) -> bool:
         self._refresh(window)
         return self._running
 
     def _refresh(self, window: _CustomRenderer) -> None:
+        self.window = window
+
         sdl2.SDL_UpdateWindowSurface(window.window)
         sdl2.SDL_RenderPresent(window.renderer)
 
+        sdl2.SDL_SetRenderDrawColor(self.window.renderer, 0, 0, 0, 255)
+        sdl2.SDL_RenderClear(self.window.renderer)
+
+
         self._LAST = self._NOW
         self._NOW = sdl2.SDL_GetPerformanceCounter()
 
         self.DELTATIME = (self._NOW - self._LAST)*1000 / sdl2.SDL_GetPerformanceFrequency()
 
         if sdl2.SDL_PollEvent(window.event) != 0 and window.event.type == sdl2.SDL_QUIT:
             self._running = False
```

