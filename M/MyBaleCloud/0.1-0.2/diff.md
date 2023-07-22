# Comparing `tmp/MyBaleCloud-0.1.tar.gz` & `tmp/MyBaleCloud-0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MyBaleCloud-0.1.tar", last modified: Sat Jul 22 21:03:07 2023, max compression
+gzip compressed data, was "MyBaleCloud-0.2.tar", last modified: Sat Jul 22 21:30:30 2023, max compression
```

## Comparing `MyBaleCloud-0.1.tar` & `MyBaleCloud-0.2.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 21:03:06.992468 MyBaleCloud-0.1/
--rw-rw----   0 root         (0) everybody  (9997)     1064 2023-07-22 21:00:19.000000 MyBaleCloud-0.1/LICENSE.txt
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 21:03:06.724468 MyBaleCloud-0.1/MyBaleCloud/
--rw-rw----   0 root         (0) everybody  (9997)     8630 2023-07-22 20:41:39.000000 MyBaleCloud-0.1/MyBaleCloud/balecloud.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 21:03:06.968468 MyBaleCloud-0.1/MyBaleCloud.egg-info/
--rw-rw----   0 root         (0) everybody  (9997)      734 2023-07-22 21:03:06.000000 MyBaleCloud-0.1/MyBaleCloud.egg-info/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)      239 2023-07-22 21:03:06.000000 MyBaleCloud-0.1/MyBaleCloud.egg-info/SOURCES.txt
--rw-rw----   0 root         (0) everybody  (9997)        1 2023-07-22 21:03:06.000000 MyBaleCloud-0.1/MyBaleCloud.egg-info/dependency_links.txt
--rw-rw----   0 root         (0) everybody  (9997)        9 2023-07-22 21:03:06.000000 MyBaleCloud-0.1/MyBaleCloud.egg-info/requires.txt
--rw-rw----   0 root         (0) everybody  (9997)       12 2023-07-22 21:03:06.000000 MyBaleCloud-0.1/MyBaleCloud.egg-info/top_level.txt
--rw-rw----   0 root         (0) everybody  (9997)      734 2023-07-22 21:03:06.996468 MyBaleCloud-0.1/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)       42 2023-07-22 21:02:47.000000 MyBaleCloud-0.1/README.md
--rw-rw----   0 root         (0) everybody  (9997)       79 2023-07-22 21:03:07.004468 MyBaleCloud-0.1/setup.cfg
--rw-rw----   0 root         (0) everybody  (9997)     1627 2023-07-22 20:56:18.000000 MyBaleCloud-0.1/setup.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 21:30:30.896468 MyBaleCloud-0.2/
+-rw-rw----   0 root         (0) everybody  (9997)     1064 2023-07-22 21:00:19.000000 MyBaleCloud-0.2/LICENSE.txt
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 21:30:30.688468 MyBaleCloud-0.2/MyBaleCloud/
+-rw-rw----   0 root         (0) everybody  (9997)     8809 2023-07-22 21:29:52.000000 MyBaleCloud-0.2/MyBaleCloud/balecloud.py
+drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 21:30:30.852468 MyBaleCloud-0.2/MyBaleCloud.egg-info/
+-rw-rw----   0 root         (0) everybody  (9997)      734 2023-07-22 21:30:30.000000 MyBaleCloud-0.2/MyBaleCloud.egg-info/PKG-INFO
+-rw-rw----   0 root         (0) everybody  (9997)      239 2023-07-22 21:30:30.000000 MyBaleCloud-0.2/MyBaleCloud.egg-info/SOURCES.txt
+-rw-rw----   0 root         (0) everybody  (9997)        1 2023-07-22 21:30:30.000000 MyBaleCloud-0.2/MyBaleCloud.egg-info/dependency_links.txt
+-rw-rw----   0 root         (0) everybody  (9997)        9 2023-07-22 21:30:30.000000 MyBaleCloud-0.2/MyBaleCloud.egg-info/requires.txt
+-rw-rw----   0 root         (0) everybody  (9997)       12 2023-07-22 21:30:30.000000 MyBaleCloud-0.2/MyBaleCloud.egg-info/top_level.txt
+-rw-rw----   0 root         (0) everybody  (9997)      734 2023-07-22 21:30:30.896468 MyBaleCloud-0.2/PKG-INFO
+-rw-rw----   0 root         (0) everybody  (9997)       42 2023-07-22 21:02:47.000000 MyBaleCloud-0.2/README.md
+-rw-rw----   0 root         (0) everybody  (9997)       79 2023-07-22 21:30:30.904468 MyBaleCloud-0.2/setup.cfg
+-rw-rw----   0 root         (0) everybody  (9997)     1627 2023-07-22 21:29:00.000000 MyBaleCloud-0.2/setup.py
```

### Comparing `MyBaleCloud-0.1/LICENSE.txt` & `MyBaleCloud-0.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `MyBaleCloud-0.1/MyBaleCloud/balecloud.py` & `MyBaleCloud-0.2/MyBaleCloud/balecloud.py`

 * *Files 5% similar despite different names*

```diff
@@ -11,23 +11,27 @@
         global headers
         headers = {'Content-Type': 'Application/json', 'Accept': 'Application/json'}
 
     def sendMessage(self, message : str = None, chatID : str = None, messageID : str = None):
         if (message == None or chatID == None):
             raise ValueError('message or chatID argument cannot be empty')
         else:
-
-            req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendMessage',data= {
-            "chat_id" : int(chatID),
-            "message" : str(message),
-            "reply_to_message_id" : int(messageID) if messageID != None else '' or None
-},
-            headers=headers)
-
-            return req.json()
+            if messageID == None:
+                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendMessage?chat_id={chatID}&text={message}'
+    },
+                headers=headers)
+    
+                return req.json()
+                
+            else:
+                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendMessage?chat_id={chatID}&text={message}&reply_to_message_id={messageID}'
+    },
+                headers=headers)
+    
+                return req.json()
     
     def editMessageText(self, newMessage : str = None, chatID : str = None, messageID : str = None, ):
         if (newMessage == None or chatID == None or messageID == None):
             raise ValueError('newMessage / chatID / messageID cannot be empty')
         else:
             req = requests.get(f'https://tapi.bale.ai/bot{self.token}/editMessageText', data= {
                 'chat_id' : int(chatID),
@@ -203,8 +207,7 @@
                 try:
                     return requests.get(f'https://tapi.bale.ai/bot{self.token}/getChatMember?chat_id={str(chatID)}&user_id={str(userID)}').json()
                     break
                 except:continue
                 
                 
     
-
```

### Comparing `MyBaleCloud-0.1/MyBaleCloud.egg-info/PKG-INFO` & `MyBaleCloud-0.2/MyBaleCloud.egg-info/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MyBaleCloud
-Version: 0.1
+Version: 0.2
 Summary: a library for bale bot messenger
 Home-page: https://github.com/HostBlack1Let/MyBale
 Download-URL: https://github.com/user/reponame/archive/v_01.tar.gz
 Author: Host1let
 Author-email: hslhostlet@gmail.com
 License: MIT
 Keywords: SOME,MEANINGFULL,KEYWORDS
```

### Comparing `MyBaleCloud-0.1/PKG-INFO` & `MyBaleCloud-0.2/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MyBaleCloud
-Version: 0.1
+Version: 0.2
 Summary: a library for bale bot messenger
 Home-page: https://github.com/HostBlack1Let/MyBale
 Download-URL: https://github.com/user/reponame/archive/v_01.tar.gz
 Author: Host1let
 Author-email: hslhostlet@gmail.com
 License: MIT
 Keywords: SOME,MEANINGFULL,KEYWORDS
```

### Comparing `MyBaleCloud-0.1/setup.py` & `MyBaleCloud-0.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from distutils.core import setup
 setup(
   name = 'MyBaleCloud',         # How you named your package folder (MyLib)
   packages = ['MyBaleCloud'],   # Chose the same as "name"
-  version = '0.1',      # Start with a small number and increase it with every change you make
+  version = '0.2',      # Start with a small number and increase it with every change you make
   license='MIT',        # Chose a license from here: https://help.github.com/articles/licensing-a-repository
   description = 'a library for bale bot messenger',   # Give a short description about your library
   author = 'Host1let',                   # Type in your name
   author_email = 'hslhostlet@gmail.com',      # Type in your E-Mail
   url = 'https://github.com/HostBlack1Let/MyBale',   # Provide either the link to your github or to your website
   download_url = 'https://github.com/user/reponame/archive/v_01.tar.gz',    # I explain this later on
   keywords = ['SOME', 'MEANINGFULL', 'KEYWORDS'],   # Keywords that define your package best
```

