# Comparing `tmp/MyBaleCloud-2.0.1.tar.gz` & `tmp/MyBaleCloud-2.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MyBaleCloud-2.0.1.tar", last modified: Sun Jul 23 19:42:18 2023, max compression
+gzip compressed data, was "MyBaleCloud-2.0.2.tar", last modified: Sun Jul 23 19:59:23 2023, max compression
```

## Comparing `MyBaleCloud-2.0.1.tar` & `MyBaleCloud-2.0.2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 19:42:18.082589 MyBaleCloud-2.0.1/
--rw-rw-rw-   0        0        0     1081 2023-07-23 12:21:12.000000 MyBaleCloud-2.0.1/LICENSE.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 19:42:18.065935 MyBaleCloud-2.0.1/MyBaleCloud/
--rw-rw-rw-   0        0        0     9838 2023-07-23 12:59:53.000000 MyBaleCloud-2.0.1/MyBaleCloud/balecloud.py
-drwxrwxrwx   0        0        0        0 2023-07-23 19:42:18.079574 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/
--rw-rw-rw-   0        0        0      755 2023-07-23 19:42:17.000000 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      239 2023-07-23 19:42:17.000000 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 19:42:17.000000 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-07-23 19:42:17.000000 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/requires.txt
--rw-rw-rw-   0        0        0       12 2023-07-23 19:42:17.000000 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      755 2023-07-23 19:42:18.084579 MyBaleCloud-2.0.1/PKG-INFO
--rw-rw-rw-   0        0        0      140 2023-07-23 12:21:47.000000 MyBaleCloud-2.0.1/README.md
--rw-rw-rw-   0        0        0       86 2023-07-23 19:42:18.089232 MyBaleCloud-2.0.1/setup.cfg
--rw-rw-rw-   0        0        0     1653 2023-07-23 19:42:09.000000 MyBaleCloud-2.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:59:23.342290 MyBaleCloud-2.0.2/
+-rw-rw-rw-   0        0        0     1081 2023-07-23 12:21:12.000000 MyBaleCloud-2.0.2/LICENSE.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 19:59:23.321289 MyBaleCloud-2.0.2/MyBaleCloud/
+-rw-rw-rw-   0        0        0     9750 2023-07-23 19:58:27.000000 MyBaleCloud-2.0.2/MyBaleCloud/balecloud.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:59:23.336352 MyBaleCloud-2.0.2/MyBaleCloud.egg-info/
+-rw-rw-rw-   0        0        0      755 2023-07-23 19:59:23.000000 MyBaleCloud-2.0.2/MyBaleCloud.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      239 2023-07-23 19:59:23.000000 MyBaleCloud-2.0.2/MyBaleCloud.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 19:59:23.000000 MyBaleCloud-2.0.2/MyBaleCloud.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 19:59:23.000000 MyBaleCloud-2.0.2/MyBaleCloud.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       12 2023-07-23 19:59:23.000000 MyBaleCloud-2.0.2/MyBaleCloud.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      755 2023-07-23 19:59:23.343293 MyBaleCloud-2.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0      140 2023-07-23 12:21:47.000000 MyBaleCloud-2.0.2/README.md
+-rw-rw-rw-   0        0        0       86 2023-07-23 19:59:23.346294 MyBaleCloud-2.0.2/setup.cfg
+-rw-rw-rw-   0        0        0     1653 2023-07-23 19:59:11.000000 MyBaleCloud-2.0.2/setup.py
```

### Comparing `MyBaleCloud-2.0.1/LICENSE.txt` & `MyBaleCloud-2.0.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `MyBaleCloud-2.0.1/MyBaleCloud/balecloud.py` & `MyBaleCloud-2.0.2/MyBaleCloud/balecloud.py`

 * *Files 1% similar despite different names*

```diff
@@ -226,20 +226,17 @@
                 try:
                     return requests.get(f'https://tapi.bale.ai/bot{self.token}/getChatMember?chat_id={str(chatID)}&user_id={str(userID)}').json()
                     break
                 except:continue
                 
                 
     def getLastUpdates(self, offset : int = 0, limit : int = 0):
-         
-        while 1:
-            try:
-                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/getUpdates', data={
-                    'offset' : int(offset),
-                    'limit' : int(limit)
-                },
-                headers=headers)
-                return (req.json())['result'][-1]
-                break
-            except:continue
+        try:
+            req = requests.post(f'https://tapi.bale.ai/bot{self.token}/getUpdates', data={
+                'offset' : int(offset),
+                'limit' : int(limit)
+            },
+            headers=headers)
+            return (req.json())['result'][-1]
+        except:pass
```

### Comparing `MyBaleCloud-2.0.1/MyBaleCloud.egg-info/PKG-INFO` & `MyBaleCloud-2.0.2/MyBaleCloud.egg-info/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MyBaleCloud
-Version: 2.0.1
+Version: 2.0.2
 Summary: a library for bale bot messenger
 Home-page: https://github.com/HostBlack1Let/MyBale
 Download-URL: https://github.com/user/reponame/archive/v_01.tar.gz
 Author: Host1let
 Author-email: hslhostlet@gmail.com
 License: MIT
 Keywords: SOME,MEANINGFULL,KEYWORDS
```

### Comparing `MyBaleCloud-2.0.1/PKG-INFO` & `MyBaleCloud-2.0.2/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MyBaleCloud
-Version: 2.0.1
+Version: 2.0.2
 Summary: a library for bale bot messenger
 Home-page: https://github.com/HostBlack1Let/MyBale
 Download-URL: https://github.com/user/reponame/archive/v_01.tar.gz
 Author: Host1let
 Author-email: hslhostlet@gmail.com
 License: MIT
 Keywords: SOME,MEANINGFULL,KEYWORDS
```

### Comparing `MyBaleCloud-2.0.1/setup.py` & `MyBaleCloud-2.0.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from distutils.core import setup
 setup(
   name = 'MyBaleCloud',         # How you named your package folder (MyLib)
   packages = ['MyBaleCloud'],   # Chose the same as "name"
-  version = '2.0.1',      # Start with a small number and increase it with every change you make
+  version = '2.0.2',      # Start with a small number and increase it with every change you make
   license='MIT',        # Chose a license from here: https://help.github.com/articles/licensing-a-repository
   description = 'a library for bale bot messenger',   # Give a short description about your library
   author = 'Host1let',                   # Type in your name
   author_email = 'hslhostlet@gmail.com',      # Type in your E-Mail
   url = 'https://github.com/HostBlack1Let/MyBale',   # Provide either the link to your github or to your website
   download_url = 'https://github.com/user/reponame/archive/v_01.tar.gz',    # I explain this later on
   keywords = ['SOME', 'MEANINGFULL', 'KEYWORDS'],   # Keywords that define your package best
```

