# Comparing `tmp/async_poe_client-0.1.0.tar.gz` & `tmp/async_poe_client-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "async_poe_client-0.1.0.tar", max compression
+gzip compressed data, was "async_poe_client-0.1.1.tar", max compression
```

## Comparing `async_poe_client-0.1.0.tar` & `async_poe_client-0.1.1.tar`

### file list

```diff
@@ -1,44 +1,44 @@
--rw-r--r--   0        0        0       32 2023-07-22 14:46:24.800780 async_poe_client-0.1.0/async_poe_client/__init__.py
--rw-r--r--   0        0        0    46122 2023-07-22 15:19:04.342451 async_poe_client-0.1.0/async_poe_client/client.py
--rw-r--r--   0        0        0     1145 2023-07-19 06:18:30.461961 async_poe_client-0.1.0/async_poe_client/poe_graphql/AddHumanMessageMutation.graphql
--rw-r--r--   0        0        0      536 2023-07-19 06:18:30.461961 async_poe_client-0.1.0/async_poe_client/poe_graphql/AddMessageBreakMutation.graphql
--rw-r--r--   0        0        0      187 2023-07-19 06:18:30.461961 async_poe_client-0.1.0/async_poe_client/poe_graphql/AutoSubscriptionMutation.graphql
--rw-r--r--   0        0        0      701 2023-07-22 07:43:55.501987 async_poe_client-0.1.0/async_poe_client/poe_graphql/availableBotsListModalPaginationQuery.graphql
--rw-r--r--   0        0        0      105 2023-07-19 06:18:30.461961 async_poe_client-0.1.0/async_poe_client/poe_graphql/BioFragment.graphql
--rw-r--r--   0        0        0      169 2023-07-22 05:55:18.261809 async_poe_client-0.1.0/async_poe_client/poe_graphql/BotDeletionButton_poeBotDelete_Mutation.graphql
--rw-r--r--   0        0        0       78 2023-07-19 06:18:30.462960 async_poe_client-0.1.0/async_poe_client/poe_graphql/ChatAddedSubscription.graphql
--rw-r--r--   0        0        0      106 2023-07-19 06:18:30.462960 async_poe_client-0.1.0/async_poe_client/poe_graphql/ChatFragment.graphql
--rw-r--r--   0        0        0    12084 2023-07-19 06:18:30.462960 async_poe_client-0.1.0/async_poe_client/poe_graphql/ChatListPaginationQuery.graphql
--rw-r--r--   0        0        0      712 2023-07-19 06:18:30.462960 async_poe_client-0.1.0/async_poe_client/poe_graphql/ChatPaginationQuery.graphql
--rw-r--r--   0        0        0      162 2023-07-19 06:18:30.462960 async_poe_client-0.1.0/async_poe_client/poe_graphql/ChatViewQuery.graphql
--rw-r--r--   0        0        0      167 2023-07-19 06:18:30.463987 async_poe_client-0.1.0/async_poe_client/poe_graphql/DeleteHumanMessagesMutation.graphql
--rw-r--r--   0        0        0      129 2023-07-19 06:18:30.463987 async_poe_client-0.1.0/async_poe_client/poe_graphql/DeleteMessageMutation.graphql
--rw-r--r--   0        0        0      154 2023-07-19 06:18:30.463987 async_poe_client-0.1.0/async_poe_client/poe_graphql/DeleteUserMessagesMutation.graphql
--rw-r--r--   0        0        0     1148 2023-07-19 06:18:30.463987 async_poe_client-0.1.0/async_poe_client/poe_graphql/ExploreBotsListPaginationQuery.graphql
--rw-r--r--   0        0        0      111 2023-07-19 06:18:30.463987 async_poe_client-0.1.0/async_poe_client/poe_graphql/HandleFragment.graphql
--rw-r--r--   0        0        0      319 2023-07-19 06:18:30.464960 async_poe_client-0.1.0/async_poe_client/poe_graphql/LoginWithVerificationCodeMutation.graphql
--rw-r--r--   0        0        0     1985 2023-07-19 06:18:30.464960 async_poe_client-0.1.0/async_poe_client/poe_graphql/MessageAddedSubscription.graphql
--rw-r--r--   0        0        0      141 2023-07-19 06:18:30.464960 async_poe_client-0.1.0/async_poe_client/poe_graphql/MessageDeletedSubscription.graphql
--rw-r--r--   0        0        0      207 2023-07-19 06:18:30.464960 async_poe_client-0.1.0/async_poe_client/poe_graphql/MessageFragment.graphql
--rw-r--r--   0        0        0      152 2023-07-19 06:18:30.464960 async_poe_client-0.1.0/async_poe_client/poe_graphql/MessageRemoveVoteMutation.graphql
--rw-r--r--   0        0        0      223 2023-07-19 06:18:30.465959 async_poe_client-0.1.0/async_poe_client/poe_graphql/MessageSetVoteMutation.graphql
--rw-r--r--   0        0        0     1832 2023-07-19 06:18:30.465959 async_poe_client-0.1.0/async_poe_client/poe_graphql/PoeBotCreateMutation.graphql
--rw-r--r--   0        0        0      968 2023-07-19 06:18:30.465959 async_poe_client-0.1.0/async_poe_client/poe_graphql/PoeBotEditMutation.graphql
--rw-r--r--   0        0        0      963 2023-07-19 06:18:30.465959 async_poe_client-0.1.0/async_poe_client/poe_graphql/SendMessageMutation.graphql
--rw-r--r--   0        0        0      275 2023-07-19 06:18:30.465959 async_poe_client-0.1.0/async_poe_client/poe_graphql/SendVerificationCodeForLoginMutation.graphql
--rw-r--r--   0        0        0      222 2023-07-19 06:18:30.465959 async_poe_client-0.1.0/async_poe_client/poe_graphql/ShareMessagesMutation.graphql
--rw-r--r--   0        0        0      321 2023-07-19 06:18:30.466959 async_poe_client-0.1.0/async_poe_client/poe_graphql/SignupWithVerificationCodeMutation.graphql
--rw-r--r--   0        0        0      166 2023-07-19 06:18:30.466959 async_poe_client-0.1.0/async_poe_client/poe_graphql/StaleChatUpdateMutation.graphql
--rw-r--r--   0        0        0      170 2023-07-19 06:18:30.466959 async_poe_client-0.1.0/async_poe_client/poe_graphql/SubscriptionsMutation.graphql
--rw-r--r--   0        0        0       98 2023-07-19 06:18:30.466959 async_poe_client-0.1.0/async_poe_client/poe_graphql/SummarizePlainPostQuery.graphql
--rw-r--r--   0        0        0      150 2023-07-19 06:18:30.466959 async_poe_client-0.1.0/async_poe_client/poe_graphql/SummarizeQuotePostQuery.graphql
--rw-r--r--   0        0        0      183 2023-07-19 06:18:30.466959 async_poe_client-0.1.0/async_poe_client/poe_graphql/SummarizeSharePostQuery.graphql
--rw-r--r--   0        0        0      382 2023-07-19 06:18:30.467959 async_poe_client-0.1.0/async_poe_client/poe_graphql/UserSnippetFragment.graphql
--rw-r--r--   0        0        0      421 2023-07-19 06:18:30.467959 async_poe_client-0.1.0/async_poe_client/poe_graphql/ViewerInfoQuery.graphql
--rw-r--r--   0        0        0     1068 2023-07-19 06:18:30.467959 async_poe_client-0.1.0/async_poe_client/poe_graphql/ViewerStateFragment.graphql
--rw-r--r--   0        0        0      700 2023-07-19 06:18:30.467959 async_poe_client-0.1.0/async_poe_client/poe_graphql/ViewerStateUpdatedSubscription.graphql
--rw-r--r--   0        0        0       50 2023-07-22 08:59:35.588026 async_poe_client-0.1.0/async_poe_client/requirements.txt
--rw-r--r--   0        0        0     1648 2023-07-22 06:27:05.417257 async_poe_client-0.1.0/async_poe_client/util.py
--rw-r--r--   0        0        0      442 2023-07-22 15:15:20.084220 async_poe_client-0.1.0/pyproject.toml
--rw-r--r--   0        0        0    14952 2023-07-22 14:33:51.305762 async_poe_client-0.1.0/README.md
--rw-r--r--   0        0        0    15221 1970-01-01 00:00:00.000000 async_poe_client-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0       32 2023-07-22 14:46:24.800780 async_poe_client-0.1.1/async_poe_client/__init__.py
+-rw-r--r--   0        0        0    46899 2023-07-23 04:18:17.047991 async_poe_client-0.1.1/async_poe_client/client.py
+-rw-r--r--   0        0        0     1145 2023-07-19 06:18:30.461961 async_poe_client-0.1.1/async_poe_client/poe_graphql/AddHumanMessageMutation.graphql
+-rw-r--r--   0        0        0      536 2023-07-19 06:18:30.461961 async_poe_client-0.1.1/async_poe_client/poe_graphql/AddMessageBreakMutation.graphql
+-rw-r--r--   0        0        0      187 2023-07-19 06:18:30.461961 async_poe_client-0.1.1/async_poe_client/poe_graphql/AutoSubscriptionMutation.graphql
+-rw-r--r--   0        0        0      701 2023-07-22 07:43:55.501987 async_poe_client-0.1.1/async_poe_client/poe_graphql/availableBotsListModalPaginationQuery.graphql
+-rw-r--r--   0        0        0      105 2023-07-19 06:18:30.461961 async_poe_client-0.1.1/async_poe_client/poe_graphql/BioFragment.graphql
+-rw-r--r--   0        0        0      169 2023-07-22 05:55:18.261809 async_poe_client-0.1.1/async_poe_client/poe_graphql/BotDeletionButton_poeBotDelete_Mutation.graphql
+-rw-r--r--   0        0        0       78 2023-07-19 06:18:30.462960 async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatAddedSubscription.graphql
+-rw-r--r--   0        0        0      106 2023-07-19 06:18:30.462960 async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatFragment.graphql
+-rw-r--r--   0        0        0    12084 2023-07-19 06:18:30.462960 async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatListPaginationQuery.graphql
+-rw-r--r--   0        0        0      712 2023-07-19 06:18:30.462960 async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatPaginationQuery.graphql
+-rw-r--r--   0        0        0      162 2023-07-19 06:18:30.462960 async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatViewQuery.graphql
+-rw-r--r--   0        0        0      167 2023-07-19 06:18:30.463987 async_poe_client-0.1.1/async_poe_client/poe_graphql/DeleteHumanMessagesMutation.graphql
+-rw-r--r--   0        0        0      129 2023-07-19 06:18:30.463987 async_poe_client-0.1.1/async_poe_client/poe_graphql/DeleteMessageMutation.graphql
+-rw-r--r--   0        0        0      154 2023-07-19 06:18:30.463987 async_poe_client-0.1.1/async_poe_client/poe_graphql/DeleteUserMessagesMutation.graphql
+-rw-r--r--   0        0        0     1148 2023-07-19 06:18:30.463987 async_poe_client-0.1.1/async_poe_client/poe_graphql/ExploreBotsListPaginationQuery.graphql
+-rw-r--r--   0        0        0      111 2023-07-19 06:18:30.463987 async_poe_client-0.1.1/async_poe_client/poe_graphql/HandleFragment.graphql
+-rw-r--r--   0        0        0      319 2023-07-19 06:18:30.464960 async_poe_client-0.1.1/async_poe_client/poe_graphql/LoginWithVerificationCodeMutation.graphql
+-rw-r--r--   0        0        0     1985 2023-07-19 06:18:30.464960 async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageAddedSubscription.graphql
+-rw-r--r--   0        0        0      141 2023-07-19 06:18:30.464960 async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageDeletedSubscription.graphql
+-rw-r--r--   0        0        0      207 2023-07-19 06:18:30.464960 async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageFragment.graphql
+-rw-r--r--   0        0        0      152 2023-07-19 06:18:30.464960 async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageRemoveVoteMutation.graphql
+-rw-r--r--   0        0        0      223 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageSetVoteMutation.graphql
+-rw-r--r--   0        0        0     1832 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/PoeBotCreateMutation.graphql
+-rw-r--r--   0        0        0      968 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/PoeBotEditMutation.graphql
+-rw-r--r--   0        0        0      963 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SendMessageMutation.graphql
+-rw-r--r--   0        0        0      275 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SendVerificationCodeForLoginMutation.graphql
+-rw-r--r--   0        0        0      222 2023-07-19 06:18:30.465959 async_poe_client-0.1.1/async_poe_client/poe_graphql/ShareMessagesMutation.graphql
+-rw-r--r--   0        0        0      321 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SignupWithVerificationCodeMutation.graphql
+-rw-r--r--   0        0        0      166 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/StaleChatUpdateMutation.graphql
+-rw-r--r--   0        0        0      170 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SubscriptionsMutation.graphql
+-rw-r--r--   0        0        0       98 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SummarizePlainPostQuery.graphql
+-rw-r--r--   0        0        0      150 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SummarizeQuotePostQuery.graphql
+-rw-r--r--   0        0        0      183 2023-07-19 06:18:30.466959 async_poe_client-0.1.1/async_poe_client/poe_graphql/SummarizeSharePostQuery.graphql
+-rw-r--r--   0        0        0      382 2023-07-19 06:18:30.467959 async_poe_client-0.1.1/async_poe_client/poe_graphql/UserSnippetFragment.graphql
+-rw-r--r--   0        0        0      421 2023-07-19 06:18:30.467959 async_poe_client-0.1.1/async_poe_client/poe_graphql/ViewerInfoQuery.graphql
+-rw-r--r--   0        0        0     1068 2023-07-19 06:18:30.467959 async_poe_client-0.1.1/async_poe_client/poe_graphql/ViewerStateFragment.graphql
+-rw-r--r--   0        0        0      700 2023-07-19 06:18:30.467959 async_poe_client-0.1.1/async_poe_client/poe_graphql/ViewerStateUpdatedSubscription.graphql
+-rw-r--r--   0        0        0       50 2023-07-22 08:59:35.588026 async_poe_client-0.1.1/async_poe_client/requirements.txt
+-rw-r--r--   0        0        0     1648 2023-07-22 06:27:05.417257 async_poe_client-0.1.1/async_poe_client/util.py
+-rw-r--r--   0        0        0      442 2023-07-23 04:33:18.578622 async_poe_client-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0    15226 2023-07-23 03:53:43.488554 async_poe_client-0.1.1/README.md
+-rw-r--r--   0        0        0    15491 1970-01-01 00:00:00.000000 async_poe_client-0.1.1/PKG-INFO
```

### Comparing `async_poe_client-0.1.0/async_poe_client/client.py` & `async_poe_client-0.1.1/async_poe_client/client.py`

 * *Files 2% similar despite different names*

```diff
@@ -34,31 +34,32 @@
         self.next_data: dict = {}
         self.p_b: str = p_b
         self.sdid: str = ""
         self.subscription: dict = {}
         self.tchannel_data: dict = {}
         self.user_id: str = ""
         self.viewer: dict = {}
-        self.ws_domain = f"tch{random.randint(1, int(1e6))}"
+        self.ws_domain = f"tch{random.randint(1, int(1e6))}"[:8]
         self.client.headers = {
-            "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7",
-            "Accept-Encoding": "gzip, deflate, br",
-            "Accept-Language": "zh-CN,zh;q=0.9,en;q=0.8,en-GB;q=0.7,en-US;q=0.6",
-            "Cache-Control": "max-age=0",
-            "p-b": f"{self.p_b}",
-            "Sec-Ch-Ua": '"Microsoft Edge";v="117", "Not;A=Brand";v="8", "Chromium";v="117"',
-            "Sec-Ch-Ua-Mobile": "?0",
-            "Sec-Ch-Ua-Platform": '"Windows"',
-            "Sec-Fetch-Dest": "document",
-            "Sec-Fetch-Mode": "navigate",
-            "Sec-Fetch-Site": "same-origin",
-            "Sec-Fetch-User": "?1",
-            "Upgrade-Insecure-Requests": "1",
-            "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36 Edg/117.0.0.0",
+            'Accept': 'text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7',
+            'Accept-Encoding': 'gzip, deflate, br',
+            'Accept-Language': 'zh-CN,zh;q=0.9,en;q=0.8,en-GB;q=0.7,en-US;q=0.6',
+            'Cache-Control': 'max-age=0',
+            "Cookie": f"p-b={self.p_b}; SL_G_WPT_TO=zh-CN; SL_GWPT_Show_Hide_tmp=1; SL_wptGlobTipTmp=1;",
+            'Sec-Ch-Ua': '"Microsoft Edge";v="117", "Not;A=Brand";v="8", "Chromium";v="117"',
+            'Sec-Ch-Ua-Mobile': '?0',
+            'Sec-Ch-Ua-Platform': '"Windows"',
+            'Sec-Fetch-Dest': 'document',
+            'Sec-Fetch-Mode': 'navigate',
+            'Sec-Fetch-Site': 'same-origin',
+            'Sec-Fetch-User': '?1',
+            'Upgrade-Insecure-Requests': '1',
+            'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36 Edg/117.0.0.0',
         }
+
         self.client.cookies = {"p-b": f"{self.p_b}"}
 
     async def get_basedata(self) -> None:
         """
         This function fetches the basic data from the HOME_URL and sets various attributes of the object.
 
         Raises:
@@ -95,16 +96,16 @@
             raise ValueError(
                 "Failed to extract 'viewer' or 'user_id' from 'next_data'."
             ) from e
 
         """extract formkey from response html"""
         # by @aditiaryan and @ading2210
         try:
-            script_regex = r"<script>if\(.+\)throw new Error;(.+)</script>"
-            script_text = re.search(script_regex, response.text).group(1)
+            script_regex = r"<script>var.*?;</script>"
+            script_text = re.findall(script_regex, response.text)[0]
             key_regex = r'var [a-zA-Z]+="(.*?)",[a-zA-Z]=Array'
             key = re.search(key_regex, script_text).group(1)
             cipher_regex = r".\[(\d+)\]=.\[(\d+)\]"
             cipher_pairs = re.findall(cipher_regex, script_text)
             formkey_list = [""] * len(cipher_pairs)
             for pair in cipher_pairs:
                 formkey_index, key_index = map(int, pair)
@@ -123,15 +124,15 @@
         Raises:
             Raises a ValueError if it fails to extract the channel data from the response.
         """
         try:
             response = await self.client.get(SETTING_URL)
             json_data = response.json()
             self.tchannel_data = json_data["tchannelData"]
-            self.client.headers.update({"poe-tchannel": self.tchannel_data["channel"]})
+            self.client.headers.update({"Poe-Tchannel": self.tchannel_data["channel"]})
         except Exception as e:
             raise ValueError("Failed to extract tchannel from response.") from e
 
     def get_websocket_url(self, channel=None) -> str:
         """
         This function generates and returns the WebSocket URL.
 
@@ -141,15 +142,15 @@
         Returns:
             Returns the WebSocket URL as a string.
         """
         if channel is None:
             channel = self.tchannel_data
         query = f'?min_seq={channel["minSeq"]}&channel={channel["channel"]}&hash={channel["channelHash"]}'
         return (
-                f'ws://{self.ws_domain}.tch.{channel["baseHost"]}/up/{channel["boxName"]}/updates'
+                f'wss://{self.ws_domain}.tch.{channel["baseHost"]}/up/{channel["boxName"]}/updates'
                 + query
         )
 
     async def create(self):
         """
         This function initializes the Async_Poe_Client instance by fetching the base data, channel data, and bot data,
         and then subscribing to the channel.
@@ -262,15 +263,15 @@
             Returns the JSON response data from the server if the query is successful. If the query_name is "recv", it doesn't return anything.
 
         Raises:
             Raises an Exception if the query fails after 5 retries.
         """
 
         data = generate_data(query_name, variables)
-        base_string = data + self.formkey + "WpuLMiXEKKE98j56k"
+        base_string = data + self.formkey + "Jb1hi3fg1MxZpzYfy"
         query_headers = {
             **self.client.headers,
             "content-type": "application/json",
             "poe-tag-id": hashlib.md5(base_string.encode()).hexdigest(),
         }
         retry = 5
         detail_error = Exception("unknown error")
@@ -282,16 +283,16 @@
                     )
                     return None
                 else:
                     response = await self.client.post(
                         GQL_URL, data=data, headers=query_headers
                     )
                 json_data = response.json()
-                if json_data["data"] is None:
-                    detail_error = Exception(json_data["errors"][0]["message"])
+                if "success" in json_data.keys() and not json_data["success"]:
+                    detail_error = Exception(json_data["message"])
                     raise detail_error
                 return json_data
             except Exception as e:
                 detail_error = e
                 logger.error(
                     f"Failed to sending query:{query_name},error:{detail_error}. (retry: {retry}/5)"
                 )
@@ -339,15 +340,15 @@
             api_key: Optional[str] = None,
             api_bot: Optional[bool] = False,
             api_url: Optional[str] = None,
             prompt_public: Optional[bool] = True,
             profile_picture_url: Optional[str] = None,
             linkification: Optional[bool] = False,
             markdown_rendering: Optional[bool] = True,
-            suggested_replies: Optional[bool] = False,
+            suggested_replies: Optional[bool] = True,
             private: Optional[bool] = False,
             temperature: Optional[int] = None,
     ) -> None:
         """
         This function is used to create a new bot with the specified configuration.
 
         Args:
@@ -517,17 +518,17 @@
             response = await self.send_query(
                 "BotDeletionButton_poeBotDelete_Mutation", {"botId": bot_id}
             )
         except Exception:
             raise ValueError(
                 f"Failed to delete bot {url_botname}. Make sure the bot exists!"
             )
-        if not response["data"]["poeBotDelete"]["status"] == "success":
+        if response["data"] is None and response["errors"]:
             raise ValueError(
-                f"Failed to delete bot {url_botname} :{response['data']['poeBotDelete']['status']}"  # noqa: E501
+                f"Failed to delete bot {url_botname} :{response['errors'][0]['message']}"  # noqa: E501
             )
         logger.info(f"Succeed to delete bot {url_botname}")
 
     async def explore_bots(
             self, count: int = 50, explore_all: bool = False
     ) -> List[dict]:
         """
@@ -754,26 +755,30 @@
         Raises:
             Exception: If there is a failure in receiving messages from the bot through websockets.
 
         Note:
             This function opens a websocket connection to the bot, sends the question, and then listens for responses. It should be used within an 'async for' loop.
 
         """
-        ua = "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36 Edg/117.0.0.0"
+        ua = 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/117.0.0.0 Safari/537.36 Edg/117.0.0.0'
         async with connect(
                 self.get_websocket_url(),
                 user_agent_header=ua,
                 close_timeout=0,
                 ping_timeout=3,
+                open_timeout=3,
+                timeout=3
         ) as ws:  # noqa: E501
             human_message_id = await self.send_message(
                 url_botname, question, with_chat_break
             )
             last_text = ""
             message = None
+            yield_header = False
+            suggestion_list = []
             while True:
                 try:
                     raw_data = await ws.recv()
                     message = json.loads(json.loads(raw_data)["messages"][-1])[
                         "payload"
                     ]["data"]["messageAdded"]
                     if message["messageId"] > human_message_id:
@@ -783,17 +788,23 @@
                                 self.bots[url_botname]["defaultBotObject"][
                                     "hasSuggestedReplies"
                                 ]
                                 and suggest_able
                         ):
                             suggestion_num = len(message["suggestedReplies"])
                             if 0 < suggestion_num < 3:
-                                yield f"\nsuggest repely{str(suggestion_num)}:{message['suggestedReplies'][-1]}"
-                            if suggestion_num >= 3:
-                                yield f"\nsuggest repely{str(suggestion_num)}:{message['suggestedReplies'][-1]}"
+                                if not yield_header:
+                                    yield_header = True
+                                    yield "\n\nSuggested Reply:"
+                                suggestion_list.append(message['suggestedReplies'][-1])
+                                yield f"\n{str(suggestion_num)}:{message['suggestedReplies'][-1]}"
+                            elif suggestion_num >= 3:
+                                suggestion_list.append(message['suggestedReplies'][-1])
+                                self.bots[url_botname]["Suggestion"] = suggestion_list
+                                yield f"\n{str(suggestion_num)}:{message['suggestedReplies'][-1]}"
                                 break
                             else:
                                 yield plain_text
                         else:
                             if message["state"] == "complete":
                                 yield plain_text
                                 break
@@ -1021,15 +1032,18 @@
         if not (del_all or count):
             raise TypeError(
                 "Please provide at least one of the following parameters: del_all=<bool>, count=<int>"
             )
         bots = await self.get_available_bots(count, del_all)
         for bot in bots:
             if not bot["isSystemBot"]:
-                await self.delete_bot(bot["handle"])
+                try:
+                    await self.delete_bot(bot["handle"])
+                except Exception as e:
+                    logger.error(f"Failed to delete {bot['handle']} : {str(e)}. Make sure the bot belong to you.")
             else:
                 logger.info("Can't delete SystemBot, skipped")
         logger.info("Succeed to delete bots")
 
     async def delete_all_conversations(self):
         """
         Asynchronously deletes all user messages in the conversations.
```

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/AddHumanMessageMutation.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/AddHumanMessageMutation.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/AddMessageBreakMutation.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/AddMessageBreakMutation.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/availableBotsListModalPaginationQuery.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/availableBotsListModalPaginationQuery.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/ChatListPaginationQuery.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatListPaginationQuery.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/ChatPaginationQuery.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/ChatPaginationQuery.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/ExploreBotsListPaginationQuery.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/ExploreBotsListPaginationQuery.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/MessageAddedSubscription.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/MessageAddedSubscription.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/PoeBotCreateMutation.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/PoeBotCreateMutation.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/PoeBotEditMutation.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/PoeBotEditMutation.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/SendMessageMutation.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/SendMessageMutation.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/ViewerStateFragment.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/ViewerStateFragment.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/poe_graphql/ViewerStateUpdatedSubscription.graphql` & `async_poe_client-0.1.1/async_poe_client/poe_graphql/ViewerStateUpdatedSubscription.graphql`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/async_poe_client/util.py` & `async_poe_client-0.1.1/async_poe_client/util.py`

 * *Files identical despite different names*

### Comparing `async_poe_client-0.1.0/README.md` & `async_poe_client-0.1.1/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -112,15 +112,15 @@
 - `description: str = ""` - 新 bot 的描述，可选字符串类型，默认为空字符串。
 - `intro_message: str = ""` - 新 bot 的介绍信息，可选字符串类型。如果这是一个空字符串，则 bot 将没有介绍信息。
 - `prompt_public: bool = True` - 预设人格是否应公开可见，可选布尔类型，默认为True。
 - `profile_picture_url: Optional[str] = `None`` - bot 的个人资料图片的 URL，可选字符串类型，默认为`None`
   。使用这个库实际上无法上传自定义图像。
 - `linkification: bool = False` - bot 是否应将响应中的某些文本转化为可点击的链接，可选布尔类型，默认为False。
 - `markdown_rendering: bool = True` - bot 的响应是否启用 markdown 渲染，可选布尔类型，默认为True。
-- `suggested_replies: bool = False` - bot 是否应在每次响应后建议可能的回复，可选布尔类型，默认为False。
+- `suggested_replies: bool = True` - bot 是否应在每次响应后建议可能的回复，可选布尔类型，默认为False。
 - `private: bool = False` - bot 是否应为私人的，可选布尔类型，默认为False。
 - `temperature: Optional[float] = `None`` - 新 bot 的温度，可选浮点数类型，默认为`None`。
 
 如果你希望新的 bot 使用你自己的 API（在[这里](https://github.com/poe-platform/api-bot-tutorial)可以获取poe官方的接入教程），请使用以下参数：
 
 - `api_bot = False` - bot 是否是 自己的API bot。
 - `api_key = `None`` - 新 bot 的 API 密钥。
@@ -200,17 +200,21 @@
 - `question:str` - 询问的内容
 - `suggest_able:Optional[bool]` - 是否显示建议回复(需要该bot支持建议回复才能一并输出出来)
 - `with_chatb_reak:Optional[bool]` - 是否在对话后清除bot的记忆(即保持单对话)
 
 返回值:str的AsyncGenerator
 
 ```python
+# 这里的get_available_bots()可以在第8条中看到使用说明
 bots = await poe_client.get_available_bots(count=2)
-async for message in poe_client.ask_stream(url_botname=bots[0]['handle'], question="introduce websockets"):
+async for message in poe_client.ask_stream(url_botname=bots[1]['handle'], question="introduce websockets"):
     print(message, end="")
+
+# 如果使用了建议回复,而且想要一个建议回复的列表,可以从bots属性中提取,它会记录某个bot的最后的建议回复
+print(poe_client.bots[bots[1]['handle']]['Suggestion'])
 ```
 
 #### (2).仅使用httpx的不支持建议回复和流式输出的函数
 
 函数:ask()
 
 参数:
```

### Comparing `async_poe_client-0.1.0/PKG-INFO` & `async_poe_client-0.1.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: async-poe-client
-Version: 0.1.0
+Version: 0.1.1
 Summary: A stable, fast and convenient async client for poe.com
 Author: canxin
 Author-email: 1969730106@qq.com
 Requires-Python: >=3.7,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
@@ -130,15 +130,15 @@
 - `description: str = ""` - 新 bot 的描述，可选字符串类型，默认为空字符串。
 - `intro_message: str = ""` - 新 bot 的介绍信息，可选字符串类型。如果这是一个空字符串，则 bot 将没有介绍信息。
 - `prompt_public: bool = True` - 预设人格是否应公开可见，可选布尔类型，默认为True。
 - `profile_picture_url: Optional[str] = `None`` - bot 的个人资料图片的 URL，可选字符串类型，默认为`None`
   。使用这个库实际上无法上传自定义图像。
 - `linkification: bool = False` - bot 是否应将响应中的某些文本转化为可点击的链接，可选布尔类型，默认为False。
 - `markdown_rendering: bool = True` - bot 的响应是否启用 markdown 渲染，可选布尔类型，默认为True。
-- `suggested_replies: bool = False` - bot 是否应在每次响应后建议可能的回复，可选布尔类型，默认为False。
+- `suggested_replies: bool = True` - bot 是否应在每次响应后建议可能的回复，可选布尔类型，默认为False。
 - `private: bool = False` - bot 是否应为私人的，可选布尔类型，默认为False。
 - `temperature: Optional[float] = `None`` - 新 bot 的温度，可选浮点数类型，默认为`None`。
 
 如果你希望新的 bot 使用你自己的 API（在[这里](https://github.com/poe-platform/api-bot-tutorial)可以获取poe官方的接入教程），请使用以下参数：
 
 - `api_bot = False` - bot 是否是 自己的API bot。
 - `api_key = `None`` - 新 bot 的 API 密钥。
@@ -218,17 +218,21 @@
 - `question:str` - 询问的内容
 - `suggest_able:Optional[bool]` - 是否显示建议回复(需要该bot支持建议回复才能一并输出出来)
 - `with_chatb_reak:Optional[bool]` - 是否在对话后清除bot的记忆(即保持单对话)
 
 返回值:str的AsyncGenerator
 
 ```python
+# 这里的get_available_bots()可以在第8条中看到使用说明
 bots = await poe_client.get_available_bots(count=2)
-async for message in poe_client.ask_stream(url_botname=bots[0]['handle'], question="introduce websockets"):
+async for message in poe_client.ask_stream(url_botname=bots[1]['handle'], question="introduce websockets"):
     print(message, end="")
+
+# 如果使用了建议回复,而且想要一个建议回复的列表,可以从bots属性中提取,它会记录某个bot的最后的建议回复
+print(poe_client.bots[bots[1]['handle']]['Suggestion'])
 ```
 
 #### (2).仅使用httpx的不支持建议回复和流式输出的函数
 
 函数:ask()
 
 参数:
```

