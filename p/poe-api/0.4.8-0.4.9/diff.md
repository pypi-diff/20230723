# Comparing `tmp/poe_api-0.4.8-py3-none-any.whl.zip` & `tmp/poe_api-0.4.9-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 41548 bytes, number of entries: 42
--rw-r--r--  2.0 unx    23325 b- defN 23-Jul-04 01:53 poe.py
+Zip file size: 41727 bytes, number of entries: 42
+-rw-r--r--  2.0 unx    23935 b- defN 23-Jul-08 14:53 poe.py
 -rw-r--r--  2.0 unx     1093 b- defN 23-May-27 23:16 poe_graphql/AddHumanMessageMutation.graphql
 -rw-r--r--  2.0 unx      504 b- defN 23-Jun-04 03:20 poe_graphql/AddMessageBreakMutation.graphql
 -rw-r--r--  2.0 unx      180 b- defN 23-May-27 23:16 poe_graphql/AutoSubscriptionMutation.graphql
 -rw-r--r--  2.0 unx       97 b- defN 23-May-27 23:16 poe_graphql/BioFragment.graphql
 -rw-r--r--  2.0 unx       73 b- defN 23-May-27 23:16 poe_graphql/ChatAddedSubscription.graphql
 -rw-r--r--  2.0 unx      100 b- defN 23-May-27 23:16 poe_graphql/ChatFragment.graphql
 -rw-r--r--  2.0 unx    11486 b- defN 23-Jun-04 03:16 poe_graphql/ChatListPaginationQuery.graphql
@@ -32,13 +32,13 @@
 -rw-r--r--  2.0 unx      147 b- defN 23-May-27 23:16 poe_graphql/SummarizeQuotePostQuery.graphql
 -rw-r--r--  2.0 unx      180 b- defN 23-May-27 23:16 poe_graphql/SummarizeSharePostQuery.graphql
 -rw-r--r--  2.0 unx      368 b- defN 23-May-27 23:16 poe_graphql/UserSnippetFragment.graphql
 -rw-r--r--  2.0 unx      400 b- defN 23-May-27 23:16 poe_graphql/ViewerInfoQuery.graphql
 -rw-r--r--  2.0 unx     1038 b- defN 23-May-27 23:16 poe_graphql/ViewerStateFragment.graphql
 -rw-r--r--  2.0 unx      657 b- defN 23-May-27 23:16 poe_graphql/ViewerStateUpdatedSubscription.graphql
 -rw-r--r--  2.0 unx        0 b- defN 23-May-27 23:16 poe_graphql/__init__.py
--rw-r--r--  2.0 unx    35149 b- defN 23-Jul-04 01:56 poe_api-0.4.8.dist-info/LICENSE
--rw-r--r--  2.0 unx    18289 b- defN 23-Jul-04 01:56 poe_api-0.4.8.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-04 01:56 poe_api-0.4.8.dist-info/WHEEL
--rw-r--r--  2.0 unx       16 b- defN 23-Jul-04 01:56 poe_api-0.4.8.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx     3969 b- defN 23-Jul-04 01:56 poe_api-0.4.8.dist-info/RECORD
-42 files, 107118 bytes uncompressed, 35006 bytes compressed:  67.3%
+-rw-r--r--  2.0 unx    35149 b- defN 23-Jul-08 14:56 poe_api-0.4.9.dist-info/LICENSE
+-rw-r--r--  2.0 unx    18418 b- defN 23-Jul-08 14:56 poe_api-0.4.9.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-08 14:56 poe_api-0.4.9.dist-info/WHEEL
+-rw-r--r--  2.0 unx       16 b- defN 23-Jul-08 14:56 poe_api-0.4.9.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx     3969 b- defN 23-Jul-08 14:56 poe_api-0.4.9.dist-info/RECORD
+42 files, 107857 bytes uncompressed, 35185 bytes compressed:  67.4%
```

## zipnote {}

```diff
@@ -105,23 +105,23 @@
 
 Filename: poe_graphql/ViewerStateUpdatedSubscription.graphql
 Comment: 
 
 Filename: poe_graphql/__init__.py
 Comment: 
 
-Filename: poe_api-0.4.8.dist-info/LICENSE
+Filename: poe_api-0.4.9.dist-info/LICENSE
 Comment: 
 
-Filename: poe_api-0.4.8.dist-info/METADATA
+Filename: poe_api-0.4.9.dist-info/METADATA
 Comment: 
 
-Filename: poe_api-0.4.8.dist-info/WHEEL
+Filename: poe_api-0.4.9.dist-info/WHEEL
 Comment: 
 
-Filename: poe_api-0.4.8.dist-info/top_level.txt
+Filename: poe_api-0.4.9.dist-info/top_level.txt
 Comment: 
 
-Filename: poe_api-0.4.8.dist-info/RECORD
+Filename: poe_api-0.4.9.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## poe.py

```diff
@@ -57,15 +57,14 @@
         "value": random.randint(100, 125),
         "category": "time",
         "path": "/[handle]",
         "extra_data": {},
       },
     })
 
-  print(payload)
   return payload
 
 
 def request_with_retries(method, *args, **kwargs):
   attempts = kwargs.get("attempts") or 10
   url = args[0]
   for i in range(attempts):
@@ -133,14 +132,15 @@
     self.token = token
     self.device_id = device_id
     self.proxy = proxy
     self.client_identifier = client_identifier
 
     self.active_messages = {}
     self.message_queues = {}
+    self.suggestion_callbacks = {}
 
     self.headers = {**headers, **{
       "Referrer": "https://poe.com/",
       "Origin": "https://poe.com",
       "Host": "poe.com",
       "Sec-Fetch-Dest": "empty",
       "Sec-Fetch-Mode": "cors",
@@ -470,14 +470,20 @@
 
       for message_str in data["messages"]:
         message_data = json.loads(message_str)
         if message_data["message_type"] != "subscriptionUpdate":
           continue
         message = message_data["payload"]["data"]["messageAdded"]
 
+        #handle suggested replies
+        if "suggestedReplies" in message and type(message["suggestedReplies"]) == list and len(message["suggestedReplies"]) > 0:
+          self.suggestion_callbacks[message["messageId"]](message["suggestedReplies"][-1])
+          if len(message["suggestedReplies"]) >= 3:
+            del self.suggestion_callbacks[message["messageId"]]
+
         copied_dict = self.active_messages.copy()
         for key, value in copied_dict.items():
           #add the message to the appropriate queue
           if value == message["messageId"] and key in self.message_queues:
             self.message_queues[key].put(message)
             return
 
@@ -488,15 +494,15 @@
             return
 
     except Exception:
       logger.error(traceback.format_exc())
       self.disconnect_ws()
       self.connect_ws()
 
-  def send_message(self, chatbot, message, with_chat_break=False, timeout=20, async_recv=True):
+  def send_message(self, chatbot, message, with_chat_break=False, timeout=20, async_recv=True, suggest_callback=None):
     # if there is another active message, wait until it has finished sending
     timer = 0
     while None in self.active_messages.values():
       time.sleep(0.01)
       timer += 0.01
       if timer > timeout:
         raise RuntimeError("Timed out waiting for other messages to send.")
@@ -526,15 +532,15 @@
 
     if not message_data["data"]["messageEdgeCreate"]["message"]:
       raise RuntimeError(f"Daily limit reached for {chatbot}.")
     try:
       human_message = message_data["data"]["messageEdgeCreate"]["message"]
       human_message_id = human_message["node"]["messageId"]
     except TypeError:
-      raise RuntimeError(f"An unknown error occured. Raw response data: {message_data}")
+      raise RuntimeError(f"An unknown error occurred. Raw response data: {message_data}")
 
     # indicate that the current message is waiting for a response
     self.active_messages[human_message_id] = None
     self.message_queues[human_message_id] = queue.Queue()
 
     last_text = ""
     message_id = None
@@ -554,14 +560,18 @@
           continue
 
       #update info about response
       message["text_new"] = message["text"][len(last_text):]
       last_text = message["text"]
       message_id = message["messageId"]
 
+      # set a suggestion callback on response
+      if callable(suggest_callback) and not message_id in self.suggestion_callbacks:
+        self.suggestion_callbacks[message_id] = suggest_callback
+
       yield message
     
     def recv_post_thread():
       bot_message_id = self.active_messages[human_message_id]
 
       # wait 2 seconds after sending the request
       time.sleep(2.5)
```

## Comparing `poe_api-0.4.8.dist-info/LICENSE` & `poe_api-0.4.9.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `poe_api-0.4.8.dist-info/METADATA` & `poe_api-0.4.9.dist-info/METADATA`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: poe-api
-Version: 0.4.8
+Version: 0.4.9
 Summary: A reverse engineered API wrapper for Quora's Poe
 Home-page: https://github.com/ading2210/poe-api
 Author: ading2210
 License: GPLv3
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License (GPL)
 Classifier: Operating System :: OS Independent
@@ -211,14 +211,15 @@
 #### Sending Messages:
 You can use the `client.send_message` function to send a message to a chatbot, which accepts the following arguments:
  - `chatbot` - The codename of the chatbot. (example: `capybara`)
  - `message` - The message to send to the chatbot.
  - `with_chat_break = False` - Whether the conversation context should be cleared.
  - `timeout = 20` - The max number of seconds in between received chunks until a `RuntimeError` is raised. 
  - `async_recv = True` - Whether or not to make the `receive_POST` request async. If this is disabled, then there will be an extra wait of about 3 seconds after the message is complete.
+ - `suggest_callback = None` - Callback for suggested replies. See `examples/send_message.py` for an example on how to use this.
 
 The function is a generator which returns the most recent version of the generated message whenever it is updated.
 
 Streamed Example:
 ```python
 message = "Summarize the GNU GPL v3"
 for chunk in client.send_message("capybara", message):
```

## Comparing `poe_api-0.4.8.dist-info/RECORD` & `poe_api-0.4.9.dist-info/RECORD`

 * *Files 4% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-poe.py,sha256=Y4xlNcn44VGnV-KUcW2ObsNKeADiQHlKnaC1A79wkcM,23325
+poe.py,sha256=WAduAPTpJAisLWtsnmm3VssnnA_JscLg0xucxxa_PkM,23935
 poe_graphql/AddHumanMessageMutation.graphql,sha256=Va4SoysKE2qPlJfbwoKp6mNv0vs5hnVR20g8hPvAxdY,1093
 poe_graphql/AddMessageBreakMutation.graphql,sha256=lFDgYYX0ZTHso-ZQwm-oUk-HaSTRqOmj-zIjBQRL2sM,504
 poe_graphql/AutoSubscriptionMutation.graphql,sha256=3i8EnqwUrjOcJ2Hxly-lKhwPBJdbpO99POiM_K6jVD4,180
 poe_graphql/BioFragment.graphql,sha256=3ZdXaPtuHK38bG10WFH6bvpebcyrTLu5fs-ddtfLjf0,97
 poe_graphql/ChatAddedSubscription.graphql,sha256=NFLZJAwi0V2WQea1oelyRUrtNrwOE58NOeX8ChzVE10,73
 poe_graphql/ChatFragment.graphql,sha256=NFVSvT3NdYlEquue3yTHPu9ezCIgx6k1OXJZo2ytIzU,100
 poe_graphql/ChatListPaginationQuery.graphql,sha256=WameJV_yyS6Ey_VKn7okXAzR45AE9wOB2U6QlRgp-M4,11486
@@ -31,12 +31,12 @@
 poe_graphql/SummarizeQuotePostQuery.graphql,sha256=V4PQ1XkEDCsVR3z7h4SLsonZsWG7RptFd6JPwlGwOvE,147
 poe_graphql/SummarizeSharePostQuery.graphql,sha256=iCN8oiUUp2jfsiBxmsTA7k3_60E0MNwA5gnNrhnYpJc,180
 poe_graphql/UserSnippetFragment.graphql,sha256=Eg8rK7XM6-HqVJkpEBY0bJaYqF-FdDdWdg-Jj3VTnF0,368
 poe_graphql/ViewerInfoQuery.graphql,sha256=Xtn-VGGiknKgrW81s7YfIJwhmilobrSqiCObpoJdYfw,400
 poe_graphql/ViewerStateFragment.graphql,sha256=aicUJncsRpPBh_L2xqDv0aHcUIPIsDrDFPfDs3jcFoU,1038
 poe_graphql/ViewerStateUpdatedSubscription.graphql,sha256=1dPs0WuOLl4ybZXm4bUF60eVc94O10EkKOtqnQYODic,657
 poe_graphql/__init__.py,sha256=47DEQpj8HBSa-_TImW-5JCeuQeRkm5NMpJWZG3hSuFU,0
-poe_api-0.4.8.dist-info/LICENSE,sha256=OXLcl0T2SZ8Pmy2_dmlvKuetivmyPd5m1q-Gyd-zaYY,35149
-poe_api-0.4.8.dist-info/METADATA,sha256=x5_lbFBGm0vCqayizVEO7CuZA7ahxi18bah_2jCZlPc,18289
-poe_api-0.4.8.dist-info/WHEEL,sha256=g4nMs7d-Xl9-xC9XovUrsDHGXt-FT0E17Yqo92DEfvY,92
-poe_api-0.4.8.dist-info/top_level.txt,sha256=7Sk_jA5I5n3fNZ1671pcBau4TWZLe6UXCEnCD5NhGGI,16
-poe_api-0.4.8.dist-info/RECORD,,
+poe_api-0.4.9.dist-info/LICENSE,sha256=OXLcl0T2SZ8Pmy2_dmlvKuetivmyPd5m1q-Gyd-zaYY,35149
+poe_api-0.4.9.dist-info/METADATA,sha256=Vwt7D5RLuPcXoGI9BmyEO_L1BvKET83c7H4CmbbPp58,18418
+poe_api-0.4.9.dist-info/WHEEL,sha256=g4nMs7d-Xl9-xC9XovUrsDHGXt-FT0E17Yqo92DEfvY,92
+poe_api-0.4.9.dist-info/top_level.txt,sha256=7Sk_jA5I5n3fNZ1671pcBau4TWZLe6UXCEnCD5NhGGI,16
+poe_api-0.4.9.dist-info/RECORD,,
```

