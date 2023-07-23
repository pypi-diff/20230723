# Comparing `tmp/async_poe_client-0.1.1.tar.gz` & `tmp/async_poe_client-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "async_poe_client-0.1.1.tar", max compression
+gzip compressed data, was "async_poe_client-0.1.2.tar", max compression
```

## Comparing `async_poe_client-0.1.1.tar` & `async_poe_client-0.1.2.tar`

### file list

```diff
@@ -1,44 +1,44 @@
--rw-r--r--   0        0        0       32 2023-07-22 14:46:24.800780 async_poe_client-0.1.1/async_poe_client/__init__.py
--rw-r--r--   0        0        0    46899 2023-07-23 04:18:17.047991 async_poe_client-0.1.1/async_poe_client/client.py
--rw-r--r--   0        0        0     1145 2023-07-19 06:18:30.461961 async_poe_client-0.1.1/async_poe_client/poe_graphql/AddHumanMessageMutation.graphql
--rw-r--r--   0        0        0      536 2023-07-19 06:18:30.461961 async_poe_client-0.1.1/async_poe_client/poe_graphql/AddMessageBreakMutation.graphql
--rw-r--r--   0        0        0      187 2023-07-19 06:18:30.461961 async_poe_client-0.1.1/async_poe_client/poe_graphql/AutoSubscriptionMutation.graphql
--rw-r--r--   0        0        0      701 2023-07-22 07:43:55.501987 async_poe_client-0.1.1/async_poe_client/poe_graphql/availableBotsListModalPaginationQuery.graphql
--rw-r--r--   0        0        0      105 2023-07-19 06:18:30.461961 async_poe_client-0.1.1/async_poe_client/poe_graphql/BioFragment.graphql
--rw-r--r--   0        0        0      169 2023-07-22 05:55:18.261809 async_poe_client-0.1.1/async_poe_client/poe_graphql/BotDeletionButton_poeBotDelete_Mutation.graphql
--rw-r--r--   0        0        0       78 2023-07-19 06:18:30.462960 async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatAddedSubscription.graphql
--rw-r--r--   0        0        0      106 2023-07-19 06:18:30.462960 async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatFragment.graphql
--rw-r--r--   0        0        0    12084 2023-07-19 06:18:30.462960 async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatListPaginationQuery.graphql
--rw-r--r--   0        0        0      712 2023-07-19 06:18:30.462960 async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatPaginationQuery.graphql
--rw-r--r--   0        0        0      162 2023-07-19 06:18:30.462960 async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatViewQuery.graphql
--rw-r--r--   0        0        0      167 2023-07-19 06:18:30.463987 async_poe_client-0.1.1/async_poe_client/poe_graphql/DeleteHumanMessagesMutation.graphql
--rw-r--r--   0        0        0      129 2023-07-19 06:18:30.463987 async_poe_client-0.1.1/async_poe_client/poe_graphql/DeleteMessageMutation.graphql
--rw-r--r--   0        0        0      154 2023-07-19 06:18:30.463987 async_poe_client-0.1.1/async_poe_client/poe_graphql/DeleteUserMessagesMutation.graphql
--rw-r--r--   0        0        0     1148 2023-07-19 06:18:30.463987 async_poe_client-0.1.1/async_poe_client/poe_graphql/ExploreBotsListPaginationQuery.graphql
--rw-r--r--   0        0        0      111 2023-07-19 06:18:30.463987 async_poe_client-0.1.1/async_poe_client/poe_graphql/HandleFragment.graphql
--rw-r--r--   0        0        0      319 2023-07-19 06:18:30.464960 async_poe_client-0.1.1/async_poe_client/poe_graphql/LoginWithVerificationCodeMutation.graphql
--rw-r--r--   0        0        0     1985 2023-07-19 06:18:30.464960 async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageAddedSubscription.graphql
--rw-r--r--   0        0        0      141 2023-07-19 06:18:30.464960 async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageDeletedSubscription.graphql
--rw-r--r--   0        0        0      207 2023-07-19 06:18:30.464960 async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageFragment.graphql
--rw-r--r--   0        0        0      152 2023-07-19 06:18:30.464960 async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageRemoveVoteMutation.graphql
--rw-r--r--   0        0        0      223 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageSetVoteMutation.graphql
--rw-r--r--   0        0        0     1832 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/PoeBotCreateMutation.graphql
--rw-r--r--   0        0        0      968 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/PoeBotEditMutation.graphql
--rw-r--r--   0        0        0      963 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SendMessageMutation.graphql
--rw-r--r--   0        0        0      275 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SendVerificationCodeForLoginMutation.graphql
--rw-r--r--   0        0        0      222 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/ShareMessagesMutation.graphql
--rw-r--r--   0        0        0      321 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SignupWithVerificationCodeMutation.graphql
--rw-r--r--   0        0        0      166 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/StaleChatUpdateMutation.graphql
--rw-r--r--   0        0        0      170 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SubscriptionsMutation.graphql
--rw-r--r--   0        0        0       98 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SummarizePlainPostQuery.graphql
--rw-r--r--   0        0        0      150 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SummarizeQuotePostQuery.graphql
--rw-r--r--   0        0        0      183 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SummarizeSharePostQuery.graphql
--rw-r--r--   0        0        0      382 2023-07-19 06:18:30.467959 async_poe_client-0.1.1/async_poe_client/poe_graphql/UserSnippetFragment.graphql
--rw-r--r--   0        0        0      421 2023-07-19 06:18:30.467959 async_poe_client-0.1.1/async_poe_client/poe_graphql/ViewerInfoQuery.graphql
--rw-r--r--   0        0        0     1068 2023-07-19 06:18:30.467959 async_poe_client-0.1.1/async_poe_client/poe_graphql/ViewerStateFragment.graphql
--rw-r--r--   0        0        0      700 2023-07-19 06:18:30.467959 async_poe_client-0.1.1/async_poe_client/poe_graphql/ViewerStateUpdatedSubscription.graphql
--rw-r--r--   0        0        0       50 2023-07-22 08:59:35.588026 async_poe_client-0.1.1/async_poe_client/requirements.txt
--rw-r--r--   0        0        0     1648 2023-07-22 06:27:05.417257 async_poe_client-0.1.1/async_poe_client/util.py
--rw-r--r--   0        0        0      442 2023-07-23 04:33:18.578622 async_poe_client-0.1.1/pyproject.toml
--rw-r--r--   0        0        0    15226 2023-07-23 03:53:43.488554 async_poe_client-0.1.1/README.md
--rw-r--r--   0        0        0    15491 1970-01-01 00:00:00.000000 async_poe_client-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0       32 2023-07-22 14:46:24.800780 async_poe_client-0.1.2/async_poe_client/__init__.py
+-rw-r--r--   0        0        0    48013 2023-07-23 07:04:39.334949 async_poe_client-0.1.2/async_poe_client/client.py
+-rw-r--r--   0        0        0     1145 2023-07-19 06:18:30.461961 async_poe_client-0.1.2/async_poe_client/poe_graphql/AddHumanMessageMutation.graphql
+-rw-r--r--   0        0        0      536 2023-07-19 06:18:30.461961 async_poe_client-0.1.2/async_poe_client/poe_graphql/AddMessageBreakMutation.graphql
+-rw-r--r--   0        0        0      187 2023-07-19 06:18:30.461961 async_poe_client-0.1.2/async_poe_client/poe_graphql/AutoSubscriptionMutation.graphql
+-rw-r--r--   0        0        0      701 2023-07-22 07:43:55.501987 async_poe_client-0.1.2/async_poe_client/poe_graphql/availableBotsListModalPaginationQuery.graphql
+-rw-r--r--   0        0        0      105 2023-07-19 06:18:30.461961 async_poe_client-0.1.2/async_poe_client/poe_graphql/BioFragment.graphql
+-rw-r--r--   0        0        0      169 2023-07-22 05:55:18.261809 async_poe_client-0.1.2/async_poe_client/poe_graphql/BotDeletionButton_poeBotDelete_Mutation.graphql
+-rw-r--r--   0        0        0       78 2023-07-19 06:18:30.462960 async_poe_client-0.1.2/async_poe_client/poe_graphql/ChatAddedSubscription.graphql
+-rw-r--r--   0        0        0      106 2023-07-19 06:18:30.462960 async_poe_client-0.1.2/async_poe_client/poe_graphql/ChatFragment.graphql
+-rw-r--r--   0        0        0    12084 2023-07-19 06:18:30.462960 async_poe_client-0.1.2/async_poe_client/poe_graphql/ChatListPaginationQuery.graphql
+-rw-r--r--   0        0        0      712 2023-07-19 06:18:30.462960 async_poe_client-0.1.2/async_poe_client/poe_graphql/ChatPaginationQuery.graphql
+-rw-r--r--   0        0        0      162 2023-07-19 06:18:30.462960 async_poe_client-0.1.2/async_poe_client/poe_graphql/ChatViewQuery.graphql
+-rw-r--r--   0        0        0      167 2023-07-19 06:18:30.463987 async_poe_client-0.1.2/async_poe_client/poe_graphql/DeleteHumanMessagesMutation.graphql
+-rw-r--r--   0        0        0      129 2023-07-19 06:18:30.463987 async_poe_client-0.1.2/async_poe_client/poe_graphql/DeleteMessageMutation.graphql
+-rw-r--r--   0        0        0      154 2023-07-19 06:18:30.463987 async_poe_client-0.1.2/async_poe_client/poe_graphql/DeleteUserMessagesMutation.graphql
+-rw-r--r--   0        0        0     1148 2023-07-19 06:18:30.463987 async_poe_client-0.1.2/async_poe_client/poe_graphql/ExploreBotsListPaginationQuery.graphql
+-rw-r--r--   0        0        0      111 2023-07-19 06:18:30.463987 async_poe_client-0.1.2/async_poe_client/poe_graphql/HandleFragment.graphql
+-rw-r--r--   0        0        0      319 2023-07-19 06:18:30.464960 async_poe_client-0.1.2/async_poe_client/poe_graphql/LoginWithVerificationCodeMutation.graphql
+-rw-r--r--   0        0        0     1985 2023-07-19 06:18:30.464960 async_poe_client-0.1.2/async_poe_client/poe_graphql/MessageAddedSubscription.graphql
+-rw-r--r--   0        0        0      141 2023-07-19 06:18:30.464960 async_poe_client-0.1.2/async_poe_client/poe_graphql/MessageDeletedSubscription.graphql
+-rw-r--r--   0        0        0      207 2023-07-19 06:18:30.464960 async_poe_client-0.1.2/async_poe_client/poe_graphql/MessageFragment.graphql
+-rw-r--r--   0        0        0      152 2023-07-19 06:18:30.464960 async_poe_client-0.1.2/async_poe_client/poe_graphql/MessageRemoveVoteMutation.graphql
+-rw-r--r--   0        0        0      223 2023-07-19 06:18:30.465959 async_poe_client-0.1.2/async_poe_client/poe_graphql/MessageSetVoteMutation.graphql
+-rw-r--r--   0        0        0     1832 2023-07-19 06:18:30.465959 async_poe_client-0.1.2/async_poe_client/poe_graphql/PoeBotCreateMutation.graphql
+-rw-r--r--   0        0        0      968 2023-07-19 06:18:30.465959 async_poe_client-0.1.2/async_poe_client/poe_graphql/PoeBotEditMutation.graphql
+-rw-r--r--   0        0        0      963 2023-07-19 06:18:30.465959 async_poe_client-0.1.2/async_poe_client/poe_graphql/SendMessageMutation.graphql
+-rw-r--r--   0        0        0      275 2023-07-19 06:18:30.465959 async_poe_client-0.1.2/async_poe_client/poe_graphql/SendVerificationCodeForLoginMutation.graphql
+-rw-r--r--   0        0        0      222 2023-07-19 06:18:30.465959 async_poe_client-0.1.2/async_poe_client/poe_graphql/ShareMessagesMutation.graphql
+-rw-r--r--   0        0        0      321 2023-07-19 06:18:30.466959 async_poe_client-0.1.2/async_poe_client/poe_graphql/SignupWithVerificationCodeMutation.graphql
+-rw-r--r--   0        0        0      166 2023-07-19 06:18:30.466959 async_poe_client-0.1.2/async_poe_client/poe_graphql/StaleChatUpdateMutation.graphql
+-rw-r--r--   0        0        0      170 2023-07-19 06:18:30.466959 async_poe_client-0.1.2/async_poe_client/poe_graphql/SubscriptionsMutation.graphql
+-rw-r--r--   0        0        0       98 2023-07-19 06:18:30.466959 async_poe_client-0.1.2/async_poe_client/poe_graphql/SummarizePlainPostQuery.graphql
+-rw-r--r--   0        0        0      150 2023-07-19 06:18:30.466959 async_poe_client-0.1.2/async_poe_client/poe_graphql/SummarizeQuotePostQuery.graphql
+-rw-r--r--   0        0        0      183 2023-07-19 06:18:30.466959 async_poe_client-0.1.2/async_poe_client/poe_graphql/SummarizeSharePostQuery.graphql
+-rw-r--r--   0        0        0      382 2023-07-19 06:18:30.467959 async_poe_client-0.1.2/async_poe_client/poe_graphql/UserSnippetFragment.graphql
+-rw-r--r--   0        0        0      421 2023-07-19 06:18:30.467959 async_poe_client-0.1.2/async_poe_client/poe_graphql/ViewerInfoQuery.graphql
+-rw-r--r--   0        0        0     1068 2023-07-19 06:18:30.467959 async_poe_client-0.1.2/async_poe_client/poe_graphql/ViewerStateFragment.graphql
+-rw-r--r--   0        0        0      700 2023-07-19 06:18:30.467959 async_poe_client-0.1.2/async_poe_client/poe_graphql/ViewerStateUpdatedSubscription.graphql
+-rw-r--r--   0        0        0       53 2023-07-23 07:11:13.271223 async_poe_client-0.1.2/async_poe_client/requirements.txt
+-rw-r--r--   0        0        0     1648 2023-07-22 06:27:05.417257 async_poe_client-0.1.2/async_poe_client/util.py
+-rw-r--r--   0        0        0      445 2023-07-23 07:11:27.600128 async_poe_client-0.1.2/pyproject.toml
+-rw-r--r--   0        0        0    16694 2023-07-23 05:29:25.780280 async_poe_client-0.1.2/README.md
+-rw-r--r--   0        0        0    16948 1970-01-01 00:00:00.000000 async_poe_client-0.1.2/PKG-INFO
```

### Comparing `async_poe_client-0.1.1/async_poe_client/client.py` & `async_poe_client-0.1.2/async_poe_client/client.py`

 * *Files 2% similar despite different names*

```diff
@@ -3,83 +3,93 @@
 import json
 import random
 import re
 import time
 import uuid
 from typing import List, Union, AsyncGenerator, Optional, Any
 
-import httpx
-import websockets
+import aiohttp
+from aiohttp_socks import ProxyConnector
 from loguru import logger
-from websockets.client import connect
 
 from .util import (
     HOME_URL,
     GQL_URL,
     GQL_RECV_URL,
     SETTING_URL,
     CONST_NAMESPACE,
     generate_data,
     QUERIES,
     generate_nonce,
 )
 
 
 class Poe_Client:
-    def __init__(self, p_b: str):
+    def __init__(self, p_b: str, proxy: str = ""):
         self.bots: dict = {}
         self.bot_list_url: str = ""
-        self.client = httpx.AsyncClient()
         self.formkey: str = ""
         self.home_bot_list: List[str] = []
         self.next_data: dict = {}
         self.p_b: str = p_b
         self.sdid: str = ""
         self.subscription: dict = {}
         self.tchannel_data: dict = {}
         self.user_id: str = ""
         self.viewer: dict = {}
         self.ws_domain = f"tch{random.randint(1, int(1e6))}"[:8]
-        self.client.headers = {
-            'Accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7',
+        self.proxy = proxy
+        self.headers = {
+            'Accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9',
             'Accept-Encoding': 'gzip, deflate, br',
             'Accept-Language': 'zh-CN,zh;q=0.9,en;q=0.8,en-GB;q=0.7,en-US;q=0.6',
             'Cache-Control': 'max-age=0',
             "Cookie": f"p-b={self.p_b}; SL_G_WPT_TO=zh-CN; SL_GWPT_Show_Hide_tmp=1; SL_wptGlobTipTmp=1;",
-            'Sec-Ch-Ua': '"Microsoft Edge";v="117", "Not;A=Brand";v="8", "Chromium";v="117"',
+            'Sec-Ch-Ua': '"Microsoft Edge";v="117", "Not;A Brand";v="8", "Chromium";v="117"',
             'Sec-Ch-Ua-Mobile': '?0',
             'Sec-Ch-Ua-Platform': '"Windows"',
             'Sec-Fetch-Dest': 'document',
             'Sec-Fetch-Mode': 'navigate',
             'Sec-Fetch-Site': 'same-origin',
             'Sec-Fetch-User': '?1',
             'Upgrade-Insecure-Requests': '1',
             'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36 Edg/117.0.0.0',
         }
 
-        self.client.cookies = {"p-b": f"{self.p_b}"}
+    @property
+    def session_args(self):
+        args = {
+            'headers': self.headers,
+            'cookies': {"p-b": self.p_b},
+        }
+        if self.proxy:
+            connector = ProxyConnector.from_url(self.proxy)
+            args['connector'] = connector
+        return args
 
     async def get_basedata(self) -> None:
         """
         This function fetches the basic data from the HOME_URL and sets various attributes of the object.
 
         Raises:
             Raises an Exception if it fails to get the base data.
             Raises a ValueError if it fails to extract 'next_data', 'viewer', 'user_id', or 'formkey' from the response.
         """
         try:
-            response = await self.client.get(HOME_URL)
+            async with aiohttp.ClientSession(**self.session_args) as client:
+                response = await client.get(HOME_URL)
+                text = await response.text()
         except Exception as e:
             raise Exception("Failed to get basedata from home.") from e
         try:
             """get next_data"""
             json_regex = (
                 r'<script id="__NEXT_DATA__" type="application\/json">(.+?)</script>'
             )
-            json_text = re.search(json_regex, response.text).group(1)
+            json_text = re.search(json_regex, text).group(1)
             self.next_data = json.loads(json_text)
         except Exception as e:
             raise ValueError("Failed to extract 'next_data' from the response.") from e
 
         """extract data from next_data"""
         try:
             self.bot_list_url = (
@@ -97,42 +107,44 @@
                 "Failed to extract 'viewer' or 'user_id' from 'next_data'."
             ) from e
 
         """extract formkey from response html"""
         # by @aditiaryan and @ading2210
         try:
             script_regex = r"<script>var.*?;</script>"
-            script_text = re.findall(script_regex, response.text)[0]
+            script_text = re.findall(script_regex, text)[0]
             key_regex = r'var [a-zA-Z]+="(.*?)",[a-zA-Z]=Array'
             key = re.search(key_regex, script_text).group(1)
             cipher_regex = r".\[(\d+)\]=.\[(\d+)\]"
             cipher_pairs = re.findall(cipher_regex, script_text)
             formkey_list = [""] * len(cipher_pairs)
             for pair in cipher_pairs:
                 formkey_index, key_index = map(int, pair)
                 formkey_list[formkey_index] = key[key_index]
             self.formkey = "".join(formkey_list)[:-1]
-            self.client.headers.update({"poe-formkey": self.formkey})
+            self.headers["poe-formkey"] = self.formkey
         except AttributeError as e:
             raise ValueError(
                 "Failed to extract 'formkey' from the response text."
             ) from e
 
     async def get_channel_data(self) -> None:
         """
         This function fetches the channel data from the SETTING_URL and sets the 'tchanneldata' attribute of the object.
 
         Raises:
             Raises a ValueError if it fails to extract the channel data from the response.
         """
         try:
-            response = await self.client.get(SETTING_URL)
-            json_data = response.json()
-            self.tchannel_data = json_data["tchannelData"]
-            self.client.headers.update({"Poe-Tchannel": self.tchannel_data["channel"]})
+            async with aiohttp.ClientSession(**self.session_args) as client:
+                response = await client.get(SETTING_URL)
+                data = await response.text()
+                json_data = json.loads(data)
+                self.tchannel_data = json_data["tchannelData"]
+                self.headers["Poe-Tchannel"] = self.tchannel_data["channel"]
         except Exception as e:
             raise ValueError("Failed to extract tchannel from response.") from e
 
     def get_websocket_url(self, channel=None) -> str:
         """
         This function generates and returns the WebSocket URL.
 
@@ -184,17 +196,20 @@
         url = (
             f'https://poe.com/_next/data/{self.next_data["buildId"]}/{url_botname}.json'
         )
         retry = 3
         error = Exception("Unknown error")
         while retry > 0:
             try:
-                response = await self.client.get(url, timeout=3)
-                chat_data = response.json()["pageProps"]["data"]["chatOfBotHandle"]
-                return chat_data
+                async with aiohttp.ClientSession(**self.session_args) as client:
+                    response = await client.get(url, timeout=3)
+                    data = await response.text()  # noqa: E501
+                    json_data = json.loads(data)
+                    chat_data = json_data["pageProps"]["data"]["chatOfBotHandle"]
+                    return chat_data
             except Exception as e:
                 error = e
                 retry -= 1
         raise ValueError(f"Failed to get bot chat_data from {url}") from error
 
     async def get_bot_info(self, url_botname: str) -> dict:
         """
@@ -207,17 +222,19 @@
             Returns a dictionary containing the bot's information.
 
         Raises:
             Raises a ValueError exception if it fails to get the bot's info.
         """
         url = f'https://poe.com/_next/data/{self.next_data["buildId"]}/edit_bot.json?bot={url_botname}'
         try:
-            response = await self.client.get(url, timeout=3)
-            bot_info = response.json()
-            return bot_info["pageProps"]
+            async with aiohttp.ClientSession(**self.session_args) as client:
+                response = await client.get(url, timeout=3)
+                data = await response.text()
+                bot_info = json.loads(data)
+                return bot_info["pageProps"]
         except Exception as e:
             raise ValueError(f"Failed to get bot info from {url}. Make sure the bot is not deleted") from e
 
     async def save_botdata(self, url_botname: str) -> None:
         """
         This function saves the bot's chat data for later use.
 
@@ -265,36 +282,38 @@
         Raises:
             Raises an Exception if the query fails after 5 retries.
         """
 
         data = generate_data(query_name, variables)
         base_string = data + self.formkey + "Jb1hi3fg1MxZpzYfy"
         query_headers = {
-            **self.client.headers,
+            **self.headers,
             "content-type": "application/json",
             "poe-tag-id": hashlib.md5(base_string.encode()).hexdigest(),
         }
         retry = 5
         detail_error = Exception("unknown error")
         while retry:
             try:
-                if query_name == "recv":
-                    await self.client.post(
-                        GQL_RECV_URL, headers=query_headers, data=data
-                    )
-                    return None
-                else:
-                    response = await self.client.post(
-                        GQL_URL, data=data, headers=query_headers
-                    )
-                json_data = response.json()
-                if "success" in json_data.keys() and not json_data["success"]:
-                    detail_error = Exception(json_data["message"])
-                    raise detail_error
-                return json_data
+                async with aiohttp.ClientSession(**self.session_args) as client:
+                    if query_name == "recv":
+                        await client.post(
+                            GQL_RECV_URL, headers=query_headers, data=data
+                        )
+                        return None
+                    else:
+                        response = await client.post(
+                            GQL_URL, data=data, headers=query_headers
+                        )
+                    data = await response.text()
+                    json_data = json.loads(data)
+                    if "success" in json_data.keys() and not json_data["success"]:
+                        detail_error = Exception(json_data["message"])
+                        raise detail_error
+                    return json_data
             except Exception as e:
                 detail_error = e
                 logger.error(
                     f"Failed to sending query:{query_name},error:{detail_error}. (retry: {retry}/5)"
                 )
                 retry -= 1
         raise Exception(
@@ -756,73 +775,65 @@
             Exception: If there is a failure in receiving messages from the bot through websockets.
 
         Note:
             This function opens a websocket connection to the bot, sends the question, and then listens for responses. It should be used within an 'async for' loop.
 
         """
         ua = 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36 Edg/117.0.0.0'
-        async with connect(
-                self.get_websocket_url(),
-                user_agent_header=ua,
-                close_timeout=0,
-                ping_timeout=3,
-                open_timeout=3,
-                timeout=3
-        ) as ws:  # noqa: E501
-            human_message_id = await self.send_message(
-                url_botname, question, with_chat_break
-            )
-            last_text = ""
-            message = None
-            yield_header = False
-            suggestion_list = []
-            while True:
-                try:
-                    raw_data = await ws.recv()
-                    message = json.loads(json.loads(raw_data)["messages"][-1])[
-                        "payload"
-                    ]["data"]["messageAdded"]
-                    if message["messageId"] > human_message_id:
-                        plain_text = message["text"][len(last_text):]
-                        last_text = message["text"]
-                        if (
-                                self.bots[url_botname]["defaultBotObject"][
-                                    "hasSuggestedReplies"
-                                ]
-                                and suggest_able
-                        ):
-                            suggestion_num = len(message["suggestedReplies"])
-                            if 0 < suggestion_num < 3:
-                                if not yield_header:
-                                    yield_header = True
-                                    yield "\n\nSuggested Reply:"
-                                suggestion_list.append(message['suggestedReplies'][-1])
-                                yield f"\n{str(suggestion_num)}:{message['suggestedReplies'][-1]}"
-                            elif suggestion_num >= 3:
-                                suggestion_list.append(message['suggestedReplies'][-1])
-                                self.bots[url_botname]["Suggestion"] = suggestion_list
-                                yield f"\n{str(suggestion_num)}:{message['suggestedReplies'][-1]}"
-                                break
-                            else:
-                                yield plain_text
-                        else:
-                            if message["state"] == "complete":
-                                yield plain_text
-                                break
+        async with aiohttp.ClientSession(headers={'User-Agent': ua}) as session:
+            async with session.ws_connect(self.get_websocket_url(), timeout=3, proxy=self.proxy) as ws:
+                human_message_id = await self.send_message(
+                    url_botname, question, with_chat_break
+                )
+                last_text = ""
+                message = None
+                yield_header = False
+                suggestion_list = []
+                while True:
+                    try:
+                        raw_data = await ws.receive_json()
+                        message = json.loads(raw_data["messages"][-1])["payload"]["data"]["messageAdded"]  # noqa: E501
+                        if message["messageId"] > human_message_id:
+                            plain_text = message["text"][len(last_text):]
+                            last_text = message["text"]
+                            if (
+                                    self.bots[url_botname]["defaultBotObject"][
+                                        "hasSuggestedReplies"
+                                    ]
+                                    and suggest_able
+                            ):
+                                suggestion_num = len(message["suggestedReplies"])
+                                if 0 < suggestion_num < 3:
+                                    if not yield_header:
+                                        yield_header = True
+                                        yield "\n\nSuggested Reply:"
+                                    suggestion_list.append(message['suggestedReplies'][-1])
+                                    yield f"\n{str(suggestion_num)}:{message['suggestedReplies'][-1]}"
+                                elif suggestion_num >= 3:
+                                    suggestion_list.append(message['suggestedReplies'][-1])
+                                    self.bots[url_botname]["Suggestion"] = suggestion_list
+                                    yield f"\n{str(suggestion_num)}:{message['suggestedReplies'][-1]}"
+                                    break
+                                else:
+                                    yield plain_text
                             else:
-                                yield plain_text
-                except websockets.ConnectionClosed:
-                    break
-                except Exception as e:
-                    raise Exception(
-                        f"Failed to get message from {url_botname} through websockets:{str(e)}"
-                    ) from e
-            await self.send_recv(
-                url_botname, last_text, message["messageId"], human_message_id
-            )
+                                if message["state"] == "complete":
+                                    yield plain_text
+                                    break
+                                else:
+                                    yield plain_text
+                    except asyncio.exceptions.TimeoutError as e:
+                        raise Exception(f"Failed to get message from {url_botname} through websocket:{str(e)}") from e
+                    except Exception as e:
+                        raise Exception(
+                            f"Failed to get message from {url_botname} through websocket:{str(e)}"
+                        ) from e
+                await self.send_recv(
+                    url_botname, last_text, message["messageId"], human_message_id
+                )
 
     async def send_chat_break(self, url_botname: str) -> None:
         """
         Asynchronously sends a chat break to a specified bot, effectively clearing the bot's conversation memory.
 
         Parameters:
             url_botname (str): The unique identifier of the bot to which the chat break is to be sent.
```

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/AddHumanMessageMutation.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/AddHumanMessageMutation.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/AddMessageBreakMutation.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/AddMessageBreakMutation.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/availableBotsListModalPaginationQuery.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/availableBotsListModalPaginationQuery.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatListPaginationQuery.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/ChatListPaginationQuery.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatPaginationQuery.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/ChatPaginationQuery.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/ExploreBotsListPaginationQuery.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/ExploreBotsListPaginationQuery.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageAddedSubscription.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/MessageAddedSubscription.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/PoeBotCreateMutation.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/PoeBotCreateMutation.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/PoeBotEditMutation.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/PoeBotEditMutation.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/SendMessageMutation.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/SendMessageMutation.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/ViewerStateFragment.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/ViewerStateFragment.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/poe_graphql/ViewerStateUpdatedSubscription.graphql` & `async_poe_client-0.1.2/async_poe_client/poe_graphql/ViewerStateUpdatedSubscription.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.1/async_poe_client/util.py` & `async_poe_client-0.1.2/async_poe_client/util.py`

 * *Files identical despite different names*

