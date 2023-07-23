# Comparing `tmp/MyBaleCloud-2.0.tar.gz` & `tmp/MyBaleCloud-2.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MyBaleCloud-2.0.tar", last modified: Sat Jul 22 22:24:57 2023, max compression
+gzip compressed data, was "MyBaleCloud-2.0.1.tar", last modified: Sun Jul 23 19:42:18 2023, max compression
```

## Comparing `MyBaleCloud-2.0.tar` & `MyBaleCloud-2.0.1.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 22:24:57.194732 MyBaleCloud-2.0/
--rw-rw----   0 root         (0) everybody  (9997)     1064 2023-07-22 21:00:19.000000 MyBaleCloud-2.0/LICENSE.txt
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 22:24:56.970732 MyBaleCloud-2.0/MyBaleCloud/
--rw-rw----   0 root         (0) everybody  (9997)     8776 2023-07-22 22:24:26.000000 MyBaleCloud-2.0/MyBaleCloud/balecloud.py
-drwxrwx---   0 root         (0) everybody  (9997)        0 2023-07-22 22:24:57.150732 MyBaleCloud-2.0/MyBaleCloud.egg-info/
--rw-rw----   0 root         (0) everybody  (9997)      734 2023-07-22 22:24:56.000000 MyBaleCloud-2.0/MyBaleCloud.egg-info/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)      239 2023-07-22 22:24:56.000000 MyBaleCloud-2.0/MyBaleCloud.egg-info/SOURCES.txt
--rw-rw----   0 root         (0) everybody  (9997)        1 2023-07-22 22:24:56.000000 MyBaleCloud-2.0/MyBaleCloud.egg-info/dependency_links.txt
--rw-rw----   0 root         (0) everybody  (9997)        9 2023-07-22 22:24:56.000000 MyBaleCloud-2.0/MyBaleCloud.egg-info/requires.txt
--rw-rw----   0 root         (0) everybody  (9997)       12 2023-07-22 22:24:56.000000 MyBaleCloud-2.0/MyBaleCloud.egg-info/top_level.txt
--rw-rw----   0 root         (0) everybody  (9997)      734 2023-07-22 22:24:57.194732 MyBaleCloud-2.0/PKG-INFO
--rw-rw----   0 root         (0) everybody  (9997)       42 2023-07-22 21:02:47.000000 MyBaleCloud-2.0/README.md
--rw-rw----   0 root         (0) everybody  (9997)       79 2023-07-22 22:24:57.202732 MyBaleCloud-2.0/setup.cfg
--rw-rw----   0 root         (0) everybody  (9997)     1627 2023-07-22 22:24:43.000000 MyBaleCloud-2.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:42:18.082589 MyBaleCloud-2.0.1/
+-rw-rw-rw-   0        0        0     1081 2023-07-23 12:21:12.000000 MyBaleCloud-2.0.1/LICENSE.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 19:42:18.065935 MyBaleCloud-2.0.1/MyBaleCloud/
+-rw-rw-rw-   0        0        0     9838 2023-07-23 12:59:53.000000 MyBaleCloud-2.0.1/MyBaleCloud/balecloud.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:42:18.079574 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/
+-rw-rw-rw-   0        0        0      755 2023-07-23 19:42:17.000000 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      239 2023-07-23 19:42:17.000000 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 19:42:17.000000 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 19:42:17.000000 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       12 2023-07-23 19:42:17.000000 MyBaleCloud-2.0.1/MyBaleCloud.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      755 2023-07-23 19:42:18.084579 MyBaleCloud-2.0.1/PKG-INFO
+-rw-rw-rw-   0        0        0      140 2023-07-23 12:21:47.000000 MyBaleCloud-2.0.1/README.md
+-rw-rw-rw-   0        0        0       86 2023-07-23 19:42:18.089232 MyBaleCloud-2.0.1/setup.cfg
+-rw-rw-rw-   0        0        0     1653 2023-07-23 19:42:09.000000 MyBaleCloud-2.0.1/setup.py
```

### Comparing `MyBaleCloud-2.0/LICENSE.txt` & `MyBaleCloud-2.0.1/LICENSE.txt`

 * *Ordering differences only*

 * *Files 21% similar despite different names*

```diff
@@ -1,19 +1,19 @@
-Copyright (c) 2018 MyBaleCloud Host1let
-
-Permission is hereby granted, free of charge, to any person obtaining a copy
-of this software and associated documentation files (the "Software"), to deal
-in the Software without restriction, including without limitation the rights
-to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
-copies of the Software, and to permit persons to whom the Software is
-furnished to do so, subject to the following conditions:
-
-The above copyright notice and this permission notice shall be included in all
-copies or substantial portions of the Software.
-
-THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
-IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
-FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
-AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
-LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
-OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
-SOFTWARE.
+Copyright (c) 2018 MyBaleCloud Host1let
+
+Permission is hereby granted, free of charge, to any person obtaining a copy
+of this software and associated documentation files (the "Software"), to deal
+in the Software without restriction, including without limitation the rights
+to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
+copies of the Software, and to permit persons to whom the Software is
+furnished to do so, subject to the following conditions:
+
+The above copyright notice and this permission notice shall be included in all
+copies or substantial portions of the Software.
+
+THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
+IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
+FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
+AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
+LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
+OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
+SOFTWARE.
```

### Comparing `MyBaleCloud-2.0/MyBaleCloud/balecloud.py` & `MyBaleCloud-2.0.1/MyBaleCloud/balecloud.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,209 +1,245 @@
-# BackTrack
-# python3
-# HosT1LeT
-
-import requests
-
-
-class BaleCloud:
-    def __init__(self, botToken : str) -> None:
-        self.token = str(botToken)
-        global headers
-        headers = {'Content-Type': 'Application/json', 'Accept': 'Application/json'}
-
-    def sendMessage(self, message : str = None, chatID : str = None, messageID : str = None):
-        if (message == None or chatID == None):
-            raise ValueError('message or chatID argument cannot be empty')
-        else:
-            if messageID == None:
-                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendMessage?chat_id={chatID}&text={message}', headers=headers)
-                
-                return req.json()
-                
-            else:
-                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendMessage?chat_id={chatID}&text={message}&reply_to_message_id={messageID}',headers=headers)
-    
-                return req.json()
-    
-    def editMessageText(self, newMessage : str = None, chatID : str = None, messageID : str = None, ):
-        if (newMessage == None or chatID == None or messageID == None):
-            raise ValueError('newMessage / chatID / messageID cannot be empty')
-        else:
-            req = requests.get(f'https://tapi.bale.ai/bot{self.token}/editMessageText', data= {
-                'chat_id' : int(chatID),
-                'text' : str(newMessage),
-                'message_id' : object(messageID)
-            },
-            headers=headers)
-            return req.json()
-            
-    def delMessage(self, chatID : str = None, messageID : str = None):
-        if (chatID == None or messageID == None):
-            raise ValueError('chatID or messageID argument cannot be empty')
-        else:
-            req = requests.post(f'https://tapi.bale.ai/bot{self.token}/deleteMessage', data={
-                'chat_id' : str(chatID),
-                'message_id' : object(messageID)
-            },
-            headers=headers)
-            return req.json()
-        
-    def getUpdates(self, offset : int = 0, limit : int = 10):
-        while 1:
-            try:
-                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/getUpdates', data={
-                    'offset' : int(offset),
-                    'limit' : int(limit)
-                },
-                headers=headers)
-                return req.json()
-                break
-            except:continue
-    
-    def setWebhook(self, url : str = None):
-        if (url == None):
-            raise ValueError('url argument cannot be empty')
-        else:
-            req = requests.post(f'https://tapi.bale.ai/bot{self.token}/setWebhook', data={
-                'url' : url
-            },
-            headers=headers)
-    
-            return req
-        
-    def deleteWebhook(self):
-        while 1:
-            try:
-                req = requests.get(f'https://tapi.bale.ai/bot{self.token}/deleteWebhook', headers=headers)
-                return req.json()
-                break
-            except:continue
-
-        
-    def getMe(self):
-        while 1:
-            try:
-                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/getMe', headers=headers)
-                return req
-                break
-            except:continue
-            
-    def sendPhoto(self, photoPath : str = None, chatID : str = None, caption : str = '', messageID : str = None):
-        if (photoPath == None or chatID == None):
-            raise ValueError('photoPath or chatID argument cannot be empty')
-        else:
-            while 1:
-                try:
-                    req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendPhoto', data={
-                        'chat_id' : int(chatID),
-                        'photo' : str(photoPath),
-                        'caption' : str(caption) if caption != None else '',
-                        'reply_to_message_id' : object(messageID) if messageID != None else None or ''
-                        
-                    }, headers=headers)
-                    return req.json()
-                    break
-                except:continue
-            
-    def sendMp3(self, mp3filePath : str = None, chatID : str = None, caption : str = None, messageID : str = None):
-        if (mp3filePath == None or chatID == None):
-            raise ValueError('mp3filePath or chatID argument cannot be empty')
-        else:
-            while 1:
-                try:
-                    req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendAudio', data={
-                        'chat_id' : int(chatID),
-                        'audio' : str(mp3filePath),
-                        'caption' : str(caption) if caption != None else '',
-                        'reply_to_message_id' : object(messageID) if messageID != None else None or ''
-                    }, headers=headers)
-                    return req.json()
-                    break
-                except:continue
-                
-    def sendDocument(self, docPath : str = None, chatID : str = None, caption : str = None, messageID : str = None):
-        if (docPath == None or chatID == None):
-            raise ValueError('docPath or chatID argument cannot be empty')
-        else:
-            while 1:
-                try:
-                    req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendDocument', data={
-                        'chat_id' : int(chatID),
-                        'document' : str(docPath),
-                        'caption' : str(caption) if caption != None else '',
-                        'reply_to_message_id' : object(messageID) if messageID != None else '' or None
-                    }, headers=headers)
-                    return req.json()
-                    break
-                except:continue
-    
-    def sendVideo(self, videoPath : str = None, chatID : str = None, caption : str = None, messageID : str = None):
-        if (videoPath == None or chatID == None):
-            raise ValueError('videoPath or chatID argument cannot be empty')
-        else:
-            while 1:
-                try:
-                    req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendVideo', data= {
-                        'chat_id' : int(chatID),
-                        'video' : str(videoPath),
-                        'caption' : str(caption) if caption != None else '',
-                        'reply_to_message_id' : object(messageID) if messageID != None else '' or None
-                    }, headers=headers)
-                    return req.json()
-                    break
-                except:continue
-    
-    def getFile(self, fileID : str = None):
-        if (fileID == None):
-            raise ValueError('fileID argument cannot be empty')
-        else:
-            while 1:
-                try:
-                    return requests.get(f'https://tapi.bale.ai/bot{self.token}/getFile', data={
-                        'file_id' : str(fileID)
-                    }, headers=headers).json()
-                    break
-                except:continue
-                
-    def getChat(self, chatID : str = None):
-        if (chatID == None):
-            raise ValueError('chatID argument cannot be empty')
-        else:
-            while 1:
-                try:
-                    return requests.get(f'https://tapi.bale.ai/bot{self.token}/getChat?chat_id={str(chatID)}').json()
-                    break
-                except:continue
-                
-    def getChatAdministrators(self, chatID : str = None):
-        if (chatID == None):
-            raise ValueError('chatID argument cannot be empty')
-        else:
-            while 1:
-                try:
-                    return requests.get(f'https://tapi.bale.ai/bot{self.token}/getChatAdministrators?chat_id={str(chatID)}').json()
-                    break
-                except:continue
-                
-    def getChatMembersCount(self, chatID : str = None):
-        if (chatID == None):
-            raise ValueError('chatID argument cannot be empty')
-        else:
-            while 1:
-                try:
-                    return requests.get(f'https://tapi.bale.ai/bot{self.token}/getChatMembersCount?chat_id={str(chatID)}').json()
-                    break
-                except:continue
-                
-    def getChatMember(self, chatID : str = None, userID : str = None):
-        if (chatID == None or userID == None):
-            raise ValueError('chatID or userID argument cannot be empty')
-        else:
-            while 1:
-                try:
-                    return requests.get(f'https://tapi.bale.ai/bot{self.token}/getChatMember?chat_id={str(chatID)}&user_id={str(userID)}').json()
-                    break
-                except:continue
-                
-                
-    
+# BackTrack
+# python3
+# HosT1LeT
+
+import requests
+
+
+print("""
+\033[97mMyBaleCloud is \033[96mStarting\033[97m !
+
+\033[97mpreparing to \033[91msetup \033[97mlibrary
+
+""")
+
+
+class BaleCloud:
+    def __init__(self, botToken : str) -> None:
+        self.token = str(botToken)
+        global headers
+        headers = {'Content-Type': 'Application/json', 'Accept': 'Application/json'}
+
+    def sendMessage(self, message : str = None, chatID : str = None, messageID : str = None):
+         
+        if (message == None or chatID == None):
+            raise ValueError('message or chatID argument cannot be empty')
+        else:
+            if messageID == None:
+                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendMessage?chat_id={chatID}&text={message}', headers=headers)
+
+                return req.json()
+
+            else:
+                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendMessage?chat_id={chatID}&text={message}&reply_to_message_id={messageID}',headers=headers)
+
+                return req.json()
+
+    def editMessageText(self, newMessage : str = None, chatID : str = None, messageID : str = None, ):
+         
+        if (newMessage == None or chatID == None or messageID == None):
+            raise ValueError('newMessage / chatID / messageID cannot be empty')
+        else:
+            req = requests.get(f'https://tapi.bale.ai/bot{self.token}/editMessageText?chat_id={chatID}&text={newMessage}&message_id={messageID}',
+            headers=headers)
+            return req.json()
+
+    def delMessage(self, chatID : str = None, messageID : str = None):
+         
+        if (chatID == None or messageID == None):
+            raise ValueError('chatID or messageID argument cannot be empty')
+        else:
+            req = requests.post(f'https://tapi.bale.ai/bot{self.token}/deleteMessage', data={
+                'chat_id' : str(chatID),
+                'message_id' : object(messageID)
+            },
+            headers=headers)
+            return req.json()
+
+    def getUpdates(self, offset : int = 0, limit : int = 10):
+         
+        while 1:
+            try:
+                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/getUpdates', data={
+                    'offset' : int(offset),
+                    'limit' : int(limit)
+                },
+                headers=headers)
+                return req.json()
+                break
+            except:continue
+
+    def setWebhook(self, url : str = None):
+         
+        if (url == None):
+            raise ValueError('url argument cannot be empty')
+        else:
+            req = requests.post(f'https://tapi.bale.ai/bot{self.token}/setWebhook', data={
+                'url' : url
+            },
+            headers=headers)
+
+            return req
+
+    def deleteWebhook(self):
+         
+        while 1:
+            try:
+                req = requests.get(f'https://tapi.bale.ai/bot{self.token}/deleteWebhook', headers=headers)
+                return req.json()
+                break
+            except:continue
+
+
+    def getMe(self):
+         
+        while 1:
+            try:
+                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/getMe', headers=headers)
+                return req
+                break
+            except:continue
+
+    def sendPhoto(self, photoPathOrName : str = None, chatID : str = None, caption : str = '', messageID : str = None):
+         
+        if (photoPathOrName == None or chatID == None):
+            raise ValueError('photoPath or chatID argument cannot be empty')
+        else:
+            while 1:
+                try:
+                    with open(photoPathOrName, mode='rb') as MyPhoto:
+                        req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendPhoto', data={
+                            'chat_id' : int(chatID),
+                            'photo' : MyPhoto,
+                            'caption' : str(caption) if caption != None else '',
+                            'reply_to_message_id' : object(messageID) if messageID != None else None or ''
+
+                        }, headers=headers)
+                        return req.json()
+                        break
+                except:continue
+
+    def sendMp3(self, mp3filePathOrName : str = None, chatID : str = None, caption : str= None, messageID : str = None):
+         
+        if (mp3filePathOrName == None or chatID == None):
+            raise ValueError('mp3filePath or chatID argument cannot be empty')
+        else:
+            while 1:
+                try:
+                    with open(mp3filePathOrName, mode='rb') as MyMp3:
+                        req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendAudio', data={
+                            'chat_id' : int(chatID),
+                            'audio' : MyMp3,
+                            'caption' : str(caption) if caption != None else '',
+                            'reply_to_message_id' : object(messageID) if messageID != None else None or ''
+                        }, headers=headers)
+                        return req.json()
+                        break
+                except:continue
+
+    def sendDocument(self, docPathOrName : str = None, chatID : str = None, caption : str = None, messageID : str = None):
+         
+        if (docPathOrName == None or chatID == None):
+            raise ValueError('docPath or chatID argument cannot be empty')
+        else:
+            while 1:
+                try:
+                    with open(docPathOrName, mode='rb') as MyDoc:
+                        req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendDocument', data={
+                            'chat_id' : int(chatID),
+                            'document' : MyDoc,
+                            'caption' : str(caption) if caption != None else '',
+                            'reply_to_message_id' : object(messageID) if messageID != None else '' or None
+                        }, headers=headers)
+                        return req.json()
+                        break
+                except:continue
+
+    def sendVideo(self, videoPathOrName : str = None, chatID : str = None, caption : str = None, messageID : str = None):
+         
+        if (videoPathOrName == None or chatID == None):
+            raise ValueError('videoPath or chatID argument cannot be empty')
+        else:
+            while 1:
+                try:
+                    with open(videoPathOrName, mode='rb') as MyVid:
+                        req = requests.post(f'https://tapi.bale.ai/bot{self.token}/sendVideo', data= {
+                            'chat_id' : int(chatID),
+                            'video' : MyVid,
+                            'caption' : str(caption) if caption != None else '',
+                            'reply_to_message_id' : object(messageID) if messageID != None else '' or None
+                        }, headers=headers)
+                        return req.json()
+                        break
+                except:continue
+
+    def getFile(self, fileID : str = None):
+         
+        if (fileID == None):
+            raise ValueError('fileID argument cannot be empty')
+        else:
+            while 1:
+                try:
+                    return requests.get(f'https://tapi.bale.ai/bot{self.token}/getFile', data={
+                        'file_id' : str(fileID)
+                    }, headers=headers).json()
+                    break
+                except:continue
+
+    def getChat(self, chatID : str = None):
+         
+        if (chatID == None):
+            raise ValueError('chatID argument cannot be empty')
+        else:
+            while 1:
+                try:
+                    return requests.get(f'https://tapi.bale.ai/bot{self.token}/getChat?chat_id={str(chatID)}').json()
+                    break
+                except:continue
+
+    def getChatAdministrators(self, chatID : str = None):
+         
+        if (chatID == None):
+            raise ValueError('chatID argument cannot be empty')
+        else:
+            while 1:
+                try:
+                    return requests.get(f'https://tapi.bale.ai/bot{self.token}/getChatAdministrators?chat_id={str(chatID)}').json()
+                    break
+                except:continue
+
+    def getChatMembersCount(self, chatID : str = None):
+         
+        if (chatID == None):
+            raise ValueError('chatID argument cannot be empty')
+        else:
+            while 1:
+                try:
+                    return requests.get(f'https://tapi.bale.ai/bot{self.token}/getChatMembersCount?chat_id={str(chatID)}').json()
+                    break
+                except:continue
+
+    def getChatMember(self, chatID : str = None, userID : str = None):
+         
+        if (chatID == None or userID == None):raise ValueError('chatID or userID argument cannot be empty')
+        else:
+            while 1:
+                try:
+                    return requests.get(f'https://tapi.bale.ai/bot{self.token}/getChatMember?chat_id={str(chatID)}&user_id={str(userID)}').json()
+                    break
+                except:continue
+                
+                
+    def getLastUpdates(self, offset : int = 0, limit : int = 0):
+         
+        while 1:
+            try:
+                req = requests.post(f'https://tapi.bale.ai/bot{self.token}/getUpdates', data={
+                    'offset' : int(offset),
+                    'limit' : int(limit)
+                },
+                headers=headers)
+                return (req.json())['result'][-1]
+                break
+            except:continue
+            
+
```

### Comparing `MyBaleCloud-2.0/MyBaleCloud.egg-info/PKG-INFO` & `MyBaleCloud-2.0.1/MyBaleCloud.egg-info/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,19 +1,19 @@
-Metadata-Version: 2.1
-Name: MyBaleCloud
-Version: 2.0
-Summary: a library for bale bot messenger
-Home-page: https://github.com/HostBlack1Let/MyBale
-Download-URL: https://github.com/user/reponame/archive/v_01.tar.gz
-Author: Host1let
-Author-email: hslhostlet@gmail.com
-License: MIT
-Keywords: SOME,MEANINGFULL,KEYWORDS
-Classifier: Development Status :: 3 - Alpha
-Classifier: Intended Audience :: Developers
-Classifier: Topic :: Software Development :: Build Tools
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.4
-Classifier: Programming Language :: Python :: 3.5
-Classifier: Programming Language :: Python :: 3.6
-License-File: LICENSE.txt
+Metadata-Version: 2.1
+Name: MyBaleCloud
+Version: 2.0.1
+Summary: a library for bale bot messenger
+Home-page: https://github.com/HostBlack1Let/MyBale
+Download-URL: https://github.com/user/reponame/archive/v_01.tar.gz
+Author: Host1let
+Author-email: hslhostlet@gmail.com
+License: MIT
+Keywords: SOME,MEANINGFULL,KEYWORDS
+Classifier: Development Status :: 3 - Alpha
+Classifier: Intended Audience :: Developers
+Classifier: Topic :: Software Development :: Build Tools
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.4
+Classifier: Programming Language :: Python :: 3.5
+Classifier: Programming Language :: Python :: 3.6
+License-File: LICENSE.txt
```

### Comparing `MyBaleCloud-2.0/PKG-INFO` & `MyBaleCloud-2.0.1/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,19 +1,19 @@
-Metadata-Version: 2.1
-Name: MyBaleCloud
-Version: 2.0
-Summary: a library for bale bot messenger
-Home-page: https://github.com/HostBlack1Let/MyBale
-Download-URL: https://github.com/user/reponame/archive/v_01.tar.gz
-Author: Host1let
-Author-email: hslhostlet@gmail.com
-License: MIT
-Keywords: SOME,MEANINGFULL,KEYWORDS
-Classifier: Development Status :: 3 - Alpha
-Classifier: Intended Audience :: Developers
-Classifier: Topic :: Software Development :: Build Tools
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.4
-Classifier: Programming Language :: Python :: 3.5
-Classifier: Programming Language :: Python :: 3.6
-License-File: LICENSE.txt
+Metadata-Version: 2.1
+Name: MyBaleCloud
+Version: 2.0.1
+Summary: a library for bale bot messenger
+Home-page: https://github.com/HostBlack1Let/MyBale
+Download-URL: https://github.com/user/reponame/archive/v_01.tar.gz
+Author: Host1let
+Author-email: hslhostlet@gmail.com
+License: MIT
+Keywords: SOME,MEANINGFULL,KEYWORDS
+Classifier: Development Status :: 3 - Alpha
+Classifier: Intended Audience :: Developers
+Classifier: Topic :: Software Development :: Build Tools
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.4
+Classifier: Programming Language :: Python :: 3.5
+Classifier: Programming Language :: Python :: 3.6
+License-File: LICENSE.txt
```

### Comparing `MyBaleCloud-2.0/setup.py` & `MyBaleCloud-2.0.1/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,26 +1,26 @@
-from distutils.core import setup
-setup(
-  name = 'MyBaleCloud',         # How you named your package folder (MyLib)
-  packages = ['MyBaleCloud'],   # Chose the same as "name"
-  version = '2.0',      # Start with a small number and increase it with every change you make
-  license='MIT',        # Chose a license from here: https://help.github.com/articles/licensing-a-repository
-  description = 'a library for bale bot messenger',   # Give a short description about your library
-  author = 'Host1let',                   # Type in your name
-  author_email = 'hslhostlet@gmail.com',      # Type in your E-Mail
-  url = 'https://github.com/HostBlack1Let/MyBale',   # Provide either the link to your github or to your website
-  download_url = 'https://github.com/user/reponame/archive/v_01.tar.gz',    # I explain this later on
-  keywords = ['SOME', 'MEANINGFULL', 'KEYWORDS'],   # Keywords that define your package best
-  install_requires=[            # I get to this in a second
-          'requests',
-      ],
-  classifiers=[
-    'Development Status :: 3 - Alpha',      # Chose either "3 - Alpha", "4 - Beta" or "5 - Production/Stable" as the current state of your package
-    'Intended Audience :: Developers',      # Define that your audience are developers
-    'Topic :: Software Development :: Build Tools',
-    'License :: OSI Approved :: MIT License',   # Again, pick a license
-    'Programming Language :: Python :: 3',      #Specify which pyhton versions that you want to support
-    'Programming Language :: Python :: 3.4',
-    'Programming Language :: Python :: 3.5',
-    'Programming Language :: Python :: 3.6',
-  ],
-)
+from distutils.core import setup
+setup(
+  name = 'MyBaleCloud',         # How you named your package folder (MyLib)
+  packages = ['MyBaleCloud'],   # Chose the same as "name"
+  version = '2.0.1',      # Start with a small number and increase it with every change you make
+  license='MIT',        # Chose a license from here: https://help.github.com/articles/licensing-a-repository
+  description = 'a library for bale bot messenger',   # Give a short description about your library
+  author = 'Host1let',                   # Type in your name
+  author_email = 'hslhostlet@gmail.com',      # Type in your E-Mail
+  url = 'https://github.com/HostBlack1Let/MyBale',   # Provide either the link to your github or to your website
+  download_url = 'https://github.com/user/reponame/archive/v_01.tar.gz',    # I explain this later on
+  keywords = ['SOME', 'MEANINGFULL', 'KEYWORDS'],   # Keywords that define your package best
+  install_requires=[            # I get to this in a second
+          'requests',
+      ],
+  classifiers=[
+    'Development Status :: 3 - Alpha',      # Chose either "3 - Alpha", "4 - Beta" or "5 - Production/Stable" as the current state of your package
+    'Intended Audience :: Developers',      # Define that your audience are developers
+    'Topic :: Software Development :: Build Tools',
+    'License :: OSI Approved :: MIT License',   # Again, pick a license
+    'Programming Language :: Python :: 3',      #Specify which pyhton versions that you want to support
+    'Programming Language :: Python :: 3.4',
+    'Programming Language :: Python :: 3.5',
+    'Programming Language :: Python :: 3.6',
+  ],
+)
```

