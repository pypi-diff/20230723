# Comparing `tmp/pybsky-0.0.1.tar.gz` & `tmp/pybsky-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pybsky-0.0.1.tar", last modified: Sun Jul 23 19:33:45 2023, max compression
+gzip compressed data, was "pybsky-0.0.2.tar", last modified: Sun Jul 23 19:40:03 2023, max compression
```

## Comparing `pybsky-0.0.1.tar` & `pybsky-0.0.2.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 19:33:45.459002 pybsky-0.0.1/
--rw-rw-rw-   0        0        0     1100 2023-07-23 19:26:05.000000 pybsky-0.0.1/LICENSE
--rw-rw-rw-   0        0        0     1177 2023-07-23 19:33:45.459002 pybsky-0.0.1/PKG-INFO
--rw-rw-rw-   0        0        0      554 2023-07-18 19:21:41.000000 pybsky-0.0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 19:33:45.435950 pybsky-0.0.1/pybsky/
--rw-rw-rw-   0        0        0       68 2023-07-23 18:34:27.000000 pybsky-0.0.1/pybsky/__init__.py
--rw-rw-rw-   0        0        0     1021 2023-07-23 18:18:34.000000 pybsky-0.0.1/pybsky/client.py
-drwxrwxrwx   0        0        0        0 2023-07-23 19:33:45.452950 pybsky-0.0.1/pybsky/core/
--rw-rw-rw-   0        0        0      122 2023-07-23 18:34:23.000000 pybsky-0.0.1/pybsky/core/__init__.py
--rw-rw-rw-   0        0        0      115 2023-07-21 12:03:54.000000 pybsky-0.0.1/pybsky/core/configs.py
--rw-rw-rw-   0        0        0      266 2023-07-21 11:59:59.000000 pybsky-0.0.1/pybsky/core/exceptions.py
--rw-rw-rw-   0        0        0        0 2023-07-18 19:13:17.000000 pybsky-0.0.1/pybsky/core/log.py
--rw-rw-rw-   0        0        0     5947 2023-07-23 18:36:54.000000 pybsky-0.0.1/pybsky/core/user_agents.py
--rw-rw-rw-   0        0        0     1038 2023-07-23 18:38:10.000000 pybsky-0.0.1/pybsky/core/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 19:33:45.456950 pybsky-0.0.1/pybsky/mixins/
--rw-rw-rw-   0        0        0       60 2023-07-23 18:34:35.000000 pybsky-0.0.1/pybsky/mixins/__init__.py
--rw-rw-rw-   0        0        0        0 2023-07-18 19:51:23.000000 pybsky-0.0.1/pybsky/mixins/base.py
--rw-rw-rw-   0        0        0      878 2023-07-23 18:18:45.000000 pybsky-0.0.1/pybsky/mixins/feed.py
--rw-rw-rw-   0        0        0     1399 2023-07-23 18:18:50.000000 pybsky-0.0.1/pybsky/mixins/login.py
-drwxrwxrwx   0        0        0        0 2023-07-23 19:33:45.447951 pybsky-0.0.1/pybsky.egg-info/
--rw-rw-rw-   0        0        0     1177 2023-07-23 19:33:45.000000 pybsky-0.0.1/pybsky.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      430 2023-07-23 19:33:45.000000 pybsky-0.0.1/pybsky.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 19:33:45.000000 pybsky-0.0.1/pybsky.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        7 2023-07-23 19:33:45.000000 pybsky-0.0.1/pybsky.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     1031 2023-07-23 19:33:30.000000 pybsky-0.0.1/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 19:33:45.459002 pybsky-0.0.1/setup.cfg
--rw-rw-rw-   0        0        0      991 2023-07-23 19:20:21.000000 pybsky-0.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:40:03.421621 pybsky-0.0.2/
+-rw-rw-rw-   0        0        0     1100 2023-07-23 19:26:05.000000 pybsky-0.0.2/LICENSE
+-rw-rw-rw-   0        0        0     1183 2023-07-23 19:40:03.420621 pybsky-0.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0      560 2023-07-23 19:38:22.000000 pybsky-0.0.2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 19:40:03.399622 pybsky-0.0.2/pybsky/
+-rw-rw-rw-   0        0        0       68 2023-07-23 18:34:27.000000 pybsky-0.0.2/pybsky/__init__.py
+-rw-rw-rw-   0        0        0     1021 2023-07-23 18:18:34.000000 pybsky-0.0.2/pybsky/client.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:40:03.416622 pybsky-0.0.2/pybsky/core/
+-rw-rw-rw-   0        0        0      122 2023-07-23 18:34:23.000000 pybsky-0.0.2/pybsky/core/__init__.py
+-rw-rw-rw-   0        0        0      115 2023-07-21 12:03:54.000000 pybsky-0.0.2/pybsky/core/configs.py
+-rw-rw-rw-   0        0        0      266 2023-07-21 11:59:59.000000 pybsky-0.0.2/pybsky/core/exceptions.py
+-rw-rw-rw-   0        0        0        0 2023-07-18 19:13:17.000000 pybsky-0.0.2/pybsky/core/log.py
+-rw-rw-rw-   0        0        0     5947 2023-07-23 18:36:54.000000 pybsky-0.0.2/pybsky/core/user_agents.py
+-rw-rw-rw-   0        0        0     1038 2023-07-23 18:38:10.000000 pybsky-0.0.2/pybsky/core/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:40:03.419622 pybsky-0.0.2/pybsky/mixins/
+-rw-rw-rw-   0        0        0       60 2023-07-23 18:34:35.000000 pybsky-0.0.2/pybsky/mixins/__init__.py
+-rw-rw-rw-   0        0        0        0 2023-07-18 19:51:23.000000 pybsky-0.0.2/pybsky/mixins/base.py
+-rw-rw-rw-   0        0        0      878 2023-07-23 18:18:45.000000 pybsky-0.0.2/pybsky/mixins/feed.py
+-rw-rw-rw-   0        0        0     1399 2023-07-23 18:18:50.000000 pybsky-0.0.2/pybsky/mixins/login.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:40:03.411622 pybsky-0.0.2/pybsky.egg-info/
+-rw-rw-rw-   0        0        0     1183 2023-07-23 19:40:03.000000 pybsky-0.0.2/pybsky.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      430 2023-07-23 19:40:03.000000 pybsky-0.0.2/pybsky.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 19:40:03.000000 pybsky-0.0.2/pybsky.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        7 2023-07-23 19:40:03.000000 pybsky-0.0.2/pybsky.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     1031 2023-07-23 19:39:45.000000 pybsky-0.0.2/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 19:40:03.421621 pybsky-0.0.2/setup.cfg
+-rw-rw-rw-   0        0        0      991 2023-07-23 19:20:21.000000 pybsky-0.0.2/setup.py
```

### Comparing `pybsky-0.0.1/LICENSE` & `pybsky-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `pybsky-0.0.1/PKG-INFO` & `pybsky-0.0.2/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pybsky
-Version: 0.0.1
+Version: 0.0.2
 Summary: Python Client for bsky social media
 Author: softrebel, ovan
 Author-email: Mohammadreza softrebel <sh.mohammad66@yahoo.com>, Mahdi Ovan <mahdi.ovan@yahoo.com>
 Project-URL: Homepage, https://github.com/softrebel/pybsky
 Project-URL: Bug Tracker, https://github.com/softrebel/pybsky/issues
 Keywords: python,pybsky,bsky
 Classifier: Programming Language :: Python :: 3
@@ -13,18 +13,19 @@
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Pybsky
 
 <div align='center'>
-    <img src=assets/cover.png height="150" width="500" alt="pybsky-logo" >
+    <img src="./assets/cover.png" height="150" width="500" alt="pybsky-logo" >
 
 </div>
 
+
 ## TODO List:
 
 - [x] Create Client
 - [x] Add Login logic
 - [ ] Get Profile logic
 - [ ] Get Follwer/Following logic
 - [ ] Follow/Unfollow
```

### Comparing `pybsky-0.0.1/README.md` & `pybsky-0.0.2/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 # Pybsky
 
 <div align='center'>
-    <img src=assets/cover.png height="150" width="500" alt="pybsky-logo" >
+    <img src="./assets/cover.png" height="150" width="500" alt="pybsky-logo" >
 
 </div>
 
+
 ## TODO List:
 
 - [x] Create Client
 - [x] Add Login logic
 - [ ] Get Profile logic
 - [ ] Get Follwer/Following logic
 - [ ] Follow/Unfollow
```

### Comparing `pybsky-0.0.1/pybsky/client.py` & `pybsky-0.0.2/pybsky/client.py`

 * *Files identical despite different names*

### Comparing `pybsky-0.0.1/pybsky/core/user_agents.py` & `pybsky-0.0.2/pybsky/core/user_agents.py`

 * *Files identical despite different names*

### Comparing `pybsky-0.0.1/pybsky/core/utils.py` & `pybsky-0.0.2/pybsky/core/utils.py`

 * *Files identical despite different names*

### Comparing `pybsky-0.0.1/pybsky/mixins/feed.py` & `pybsky-0.0.2/pybsky/mixins/feed.py`

 * *Files identical despite different names*

### Comparing `pybsky-0.0.1/pybsky/mixins/login.py` & `pybsky-0.0.2/pybsky/mixins/login.py`

 * *Files identical despite different names*

### Comparing `pybsky-0.0.1/pybsky.egg-info/PKG-INFO` & `pybsky-0.0.2/pybsky.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pybsky
-Version: 0.0.1
+Version: 0.0.2
 Summary: Python Client for bsky social media
 Author: softrebel, ovan
 Author-email: Mohammadreza softrebel <sh.mohammad66@yahoo.com>, Mahdi Ovan <mahdi.ovan@yahoo.com>
 Project-URL: Homepage, https://github.com/softrebel/pybsky
 Project-URL: Bug Tracker, https://github.com/softrebel/pybsky/issues
 Keywords: python,pybsky,bsky
 Classifier: Programming Language :: Python :: 3
@@ -13,18 +13,19 @@
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Pybsky
 
 <div align='center'>
-    <img src=assets/cover.png height="150" width="500" alt="pybsky-logo" >
+    <img src="./assets/cover.png" height="150" width="500" alt="pybsky-logo" >
 
 </div>
 
+
 ## TODO List:
 
 - [x] Create Client
 - [x] Add Login logic
 - [ ] Get Profile logic
 - [ ] Get Follwer/Following logic
 - [ ] Follow/Unfollow
```

### Comparing `pybsky-0.0.1/pyproject.toml` & `pybsky-0.0.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "pybsky"
-version = "0.0.1"
+version = "0.0.2"
 authors = [
   { name="Mohammadreza softrebel", email="sh.mohammad66@yahoo.com" },
     { name="Mahdi Ovan", email="mahdi.ovan@yahoo.com" },
 ]
 description ='Python Client for bsky social media'
 readme = "README.md"
 requires-python = ">=3.10"
```

### Comparing `pybsky-0.0.1/setup.py` & `pybsky-0.0.2/setup.py`

 * *Files identical despite different names*

