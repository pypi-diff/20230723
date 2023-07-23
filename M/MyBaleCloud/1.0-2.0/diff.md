# Comparing `tmp/MyBaleCloud-1.0.tar.gz` & `tmp/MyBaleCloud-2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MyBaleCloud-1.0.tar", last modified: Sat Jul 22 22:18:45 2023, max compression
+gzip compressed data, was "MyBaleCloud-2.0.tar", last modified: Sat Jul 22 22:24:57 2023, max compression
```

## Comparing `MyBaleCloud-1.0.tar` & `MyBaleCloud-2.0.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 22:18:45.542732 MyBaleCloud-1.0/
--rw-rw----   0 root         (0) everybody  (9997)     1064 2023-07-22 21:00:19.000000 MyBaleCloud-1.0/LICENSE.txt
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 22:18:45.402732 MyBaleCloud-1.0/MyBaleCloud/
--rw-rw----   0 root         (0) everybody  (9997)     8896 2023-07-22 22:14:54.000000 MyBaleCloud-1.0/MyBaleCloud/balecloud.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 22:18:45.526732 MyBaleCloud-1.0/MyBaleCloud.egg-info/
--rw-rw----   0 root         (0) everybody  (9997)      734 2023-07-22 22:18:44.000000 MyBaleCloud-1.0/MyBaleCloud.egg-info/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)      239 2023-07-22 22:18:45.000000 MyBaleCloud-1.0/MyBaleCloud.egg-info/SOURCES.txt
--rw-rw----   0 root         (0) everybody  (9997)        1 2023-07-22 22:18:45.000000 MyBaleCloud-1.0/MyBaleCloud.egg-info/dependency_links.txt
--rw-rw----   0 root         (0) everybody  (9997)        9 2023-07-22 22:18:45.000000 MyBaleCloud-1.0/MyBaleCloud.egg-info/requires.txt
--rw-rw----   0 root         (0) everybody  (9997)       12 2023-07-22 22:18:45.000000 MyBaleCloud-1.0/MyBaleCloud.egg-info/top_level.txt
--rw-rw----   0 root         (0) everybody  (9997)      734 2023-07-22 22:18:45.546732 MyBaleCloud-1.0/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)       42 2023-07-22 21:02:47.000000 MyBaleCloud-1.0/README.md
--rw-rw----   0 root         (0) everybody  (9997)       79 2023-07-22 22:18:45.554732 MyBaleCloud-1.0/setup.cfg
--rw-rw----   0 root         (0) everybody  (9997)     1627 2023-07-22 22:18:35.000000 MyBaleCloud-1.0/setup.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 22:24:57.194732 MyBaleCloud-2.0/
+-rw-rw----   0 root         (0) everybody  (9997)     1064 2023-07-22 21:00:19.000000 MyBaleCloud-2.0/LICENSE.txt
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 22:24:56.970732 MyBaleCloud-2.0/MyBaleCloud/
+-rw-rw----   0 root         (0) everybody  (9997)     8776 2023-07-22 22:24:26.000000 MyBaleCloud-2.0/MyBaleCloud/balecloud.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 22:24:57.150732 MyBaleCloud-2.0/MyBaleCloud.egg-info/
+-rw-rw----   0 root         (0) everybody  (9997)      734 2023-07-22 22:24:56.000000 MyBaleCloud-2.0/MyBaleCloud.egg-info/PKG-INFO
+-rw-rw----   0 root         (0) everybody  (9997)      239 2023-07-22 22:24:56.000000 MyBaleCloud-2.0/MyBaleCloud.egg-info/SOURCES.txt
+-rw-rw----   0 root         (0) everybody  (9997)        1 2023-07-22 22:24:56.000000 MyBaleCloud-2.0/MyBaleCloud.egg-info/dependency_links.txt
+-rw-rw----   0 root         (0) everybody  (9997)        9 2023-07-22 22:24:56.000000 MyBaleCloud-2.0/MyBaleCloud.egg-info/requires.txt
+-rw-rw----   0 root         (0) everybody  (9997)       12 2023-07-22 22:24:56.000000 MyBaleCloud-2.0/MyBaleCloud.egg-info/top_level.txt
+-rw-rw----   0 root         (0) everybody  (9997)      734 2023-07-22 22:24:57.194732 MyBaleCloud-2.0/PKG-INFO
+-rw-rw----   0 root         (0) everybody  (9997)       42 2023-07-22 21:02:47.000000 MyBaleCloud-2.0/README.md
+-rw-rw----   0 root         (0) everybody  (9997)       79 2023-07-22 22:24:57.202732 MyBaleCloud-2.0/setup.cfg
+-rw-rw----   0 root         (0) everybody  (9997)     1627 2023-07-22 22:24:43.000000 MyBaleCloud-2.0/setup.py
```

### Comparing `MyBaleCloud-1.0/LICENSE.txt` & `MyBaleCloud-2.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `MyBaleCloud-1.0/MyBaleCloud/balecloud.py` & `MyBaleCloud-2.0/MyBaleCloud/balecloud.py`

 * *Files 14% similar despite different names*

```diff
@@ -12,26 +12,20 @@
         headers = {'Content-Type': 'Application/json', 'Accept': 'Application/json'}
 
     def sendMessage(self, message : str = None, chatID : str = None, messageID : str = None):
         if (message == None or chatID == None):
             raise ValueError('message or chatID argument cannot be empty')
         else:
             if messageID == None:
-                req = requests.post(f"https://tapi.bale.ai/bot{self.token}/sendMessage",data ={
-                "chat_id":chatID,
-                "text":message,
-                }, headers=headers)
+                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendMessage?chat_id={chatID}&text={message}', headers=headers)
                 
                 return req.json()
                 
             else:
-                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendMessage',data = {
-                "chat_id":chatID,
-                "text":message,
-                "reply_to_message_id":messageID},headers=headers)
+                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendMessage?chat_id={chatID}&text={message}&reply_to_message_id={messageID}',headers=headers)
     
                 return req.json()
     
     def editMessageText(self, newMessage : str = None, chatID : str = None, messageID : str = None, ):
         if (newMessage == None or chatID == None or messageID == None):
             raise ValueError('newMessage / chatID / messageID cannot be empty')
         else:
```

### Comparing `MyBaleCloud-1.0/MyBaleCloud.egg-info/PKG-INFO` & `MyBaleCloud-2.0/MyBaleCloud.egg-info/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MyBaleCloud
-Version: 1.0
+Version: 2.0
 Summary: a library for bale bot messenger
 Home-page: https://github.com/HostBlack1Let/MyBale
 Download-URL: https://github.com/user/reponame/archive/v_01.tar.gz
 Author: Host1let
 Author-email: hslhostlet@gmail.com
 License: MIT
 Keywords: SOME,MEANINGFULL,KEYWORDS
```

### Comparing `MyBaleCloud-1.0/PKG-INFO` & `MyBaleCloud-2.0/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MyBaleCloud
-Version: 1.0
+Version: 2.0
 Summary: a library for bale bot messenger
 Home-page: https://github.com/HostBlack1Let/MyBale
 Download-URL: https://github.com/user/reponame/archive/v_01.tar.gz
 Author: Host1let
 Author-email: hslhostlet@gmail.com
 License: MIT
 Keywords: SOME,MEANINGFULL,KEYWORDS
```

### Comparing `MyBaleCloud-1.0/setup.py` & `MyBaleCloud-2.0/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from distutils.core import setup
 setup(
   name = 'MyBaleCloud',         # How you named your package folder (MyLib)
   packages = ['MyBaleCloud'],   # Chose the same as "name"
-  version = '1.0',      # Start with a small number and increase it with every change you make
+  version = '2.0',      # Start with a small number and increase it with every change you make
   license='MIT',        # Chose a license from here: https://help.github.com/articles/licensing-a-repository
   description = 'a library for bale bot messenger',   # Give a short description about your library
   author = 'Host1let',                   # Type in your name
   author_email = 'hslhostlet@gmail.com',      # Type in your E-Mail
   url = 'https://github.com/HostBlack1Let/MyBale',   # Provide either the link to your github or to your website
   download_url = 'https://github.com/user/reponame/archive/v_01.tar.gz',    # I explain this later on
   keywords = ['SOME', 'MEANINGFULL', 'KEYWORDS'],   # Keywords that define your package best
```

