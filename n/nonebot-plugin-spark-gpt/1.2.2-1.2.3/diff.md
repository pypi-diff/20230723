# Comparing `tmp/nonebot_plugin_spark_gpt-1.2.2.tar.gz` & `tmp/nonebot_plugin_spark_gpt-1.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_spark_gpt-1.2.2.tar", max compression
+gzip compressed data, was "nonebot_plugin_spark_gpt-1.2.3.tar", max compression
```

## Comparing `nonebot_plugin_spark_gpt-1.2.2.tar` & `nonebot_plugin_spark_gpt-1.2.3.tar`

### file list

```diff
@@ -1,121 +1,84 @@
--rw-r--r--   0        0        0      219 2023-07-11 09:53:31.539890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/__init__.py
--rw-r--r--   0        0        0    17261 2023-07-11 09:53:31.540890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/adapter.py
--rw-r--r--   0        0        0      138 2023-07-11 09:53:31.541890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/__init__.py
--rw-r--r--   0        0        0       27 2023-07-11 09:53:31.542890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/client.py
--rw-r--r--   0        0        0    51932 2023-07-11 09:53:31.542890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/client.pyi
--rw-r--r--   0        0        0    98693 2023-07-11 09:53:31.543890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/handle.py
--rw-r--r--   0        0        0   115238 2023-07-11 09:53:31.544890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/model.py
--rw-r--r--   0        0        0     1482 2023-07-11 09:53:31.544890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/request.py
--rw-r--r--   0        0        0    34839 2023-07-11 09:53:31.544890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/types.py
--rw-r--r--   0        0        0     2441 2023-07-11 09:53:31.545890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/utils.py
--rw-r--r--   0        0        0     7255 2023-07-11 09:53:31.545890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/bot.py
--rw-r--r--   0        0        0     2192 2023-07-11 09:53:31.546890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/config.py
--rw-r--r--   0        0        0    28334 2023-07-11 09:53:31.546890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/event.py
--rw-r--r--   0        0        0     2076 2023-07-11 09:53:31.546890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/exception.py
--rw-r--r--   0        0        0    13603 2023-07-11 09:53:31.547890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/message.py
--rw-r--r--   0        0        0     2874 2023-07-11 09:53:31.547890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/payload.py
--rw-r--r--   0        0        0     1946 2023-07-11 09:53:31.547890 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/typing.py
--rw-r--r--   0        0        0      626 2023-07-11 09:53:31.548892 nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/utils.py
--rw-r--r--   0        0        0      836 2023-07-18 04:47:31.258172 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/__init__.py
--rw-r--r--   0        0        0        0 2023-07-19 08:14:04.493611 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/__init__.py
--rw-r--r--   0        0        0     2791 2023-07-20 05:24:51.550258 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/bard.py
--rw-r--r--   0        0        0     9823 2023-07-20 05:24:51.554259 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/chatgpt_web.py
--rw-r--r--   0        0        0     9032 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/claude_ai.py
--rw-r--r--   0        0        0     4733 2023-07-20 03:24:26.105431 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/load_config.py
--rw-r--r--   0        0        0     6760 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/newbing.py
--rw-r--r--   0        0        0     8434 2023-07-19 09:50:18.910215 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/poe.py
--rw-r--r--   0        0        0     7619 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/slack_claude.py
--rw-r--r--   0        0        0     8129 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/spark_desk.py
--rw-r--r--   0        0        0     7435 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/sydneybing.py
--rw-r--r--   0        0        0     6802 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/tongyiqianwen.py
--rw-r--r--   0        0        0        0 2023-07-19 08:14:04.488610 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/__init__.py
--rw-r--r--   0        0        0    12575 2023-07-20 04:51:29.348311 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/Bard.py
--rw-r--r--   0        0        0        0 2023-07-19 08:51:03.240242 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/__init__.py
--rw-r--r--   0        0        0    17586 2023-07-19 08:50:59.147722 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/BingImageCreator.py
--rw-r--r--   0        0        0    11837 2023-07-19 08:51:01.064843 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/chathub.py
--rw-r--r--   0        0        0     2107 2023-07-19 08:51:04.982654 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/constants.py
--rw-r--r--   0        0        0     4582 2023-07-19 08:51:08.212221 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/conversation.py
--rw-r--r--   0        0        0     1312 2023-07-19 08:51:06.614074 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/conversation_style.py
--rw-r--r--   0        0        0     8088 2023-07-19 08:51:10.504420 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/EdgeGPT.py
--rw-r--r--   0        0        0    14626 2023-07-19 08:50:55.647270 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/EdgeUtils.py
--rw-r--r--   0        0        0       48 2023-07-19 08:50:53.449019 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/exceptions.py
--rw-r--r--   0        0        0      278 2023-07-19 08:50:48.240509 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/ImageGen.py
--rw-r--r--   0        0        0     2332 2023-07-19 08:50:51.738573 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/locale.py
--rw-r--r--   0        0        0     7757 2023-07-19 08:50:44.460438 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/main.py
--rw-r--r--   0        0        0     5948 2023-07-19 08:50:50.007184 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/request.py
--rw-r--r--   0        0        0      992 2023-07-19 08:51:13.314721 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/utilities.py
--rw-r--r--   0        0        0    25186 2023-07-19 14:24:28.880037 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe.py
--rw-r--r--   0        0        0        0 2023-07-19 06:18:30.467959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/__init__.py
--rw-r--r--   0        0        0     1145 2023-07-19 06:18:30.461961 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/AddHumanMessageMutation.graphql
--rw-r--r--   0        0        0      536 2023-07-19 06:18:30.461961 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/AddMessageBreakMutation.graphql
--rw-r--r--   0        0        0      187 2023-07-19 06:18:30.461961 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/AutoSubscriptionMutation.graphql
--rw-r--r--   0        0        0      105 2023-07-19 06:18:30.461961 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/BioFragment.graphql
--rw-r--r--   0        0        0       78 2023-07-19 06:18:30.462960 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/ChatAddedSubscription.graphql
--rw-r--r--   0        0        0      106 2023-07-19 06:18:30.462960 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/ChatFragment.graphql
--rw-r--r--   0        0        0    12084 2023-07-19 06:18:30.462960 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/ChatListPaginationQuery.graphql
--rw-r--r--   0        0        0      712 2023-07-19 06:18:30.462960 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/ChatPaginationQuery.graphql
--rw-r--r--   0        0        0      162 2023-07-19 06:18:30.462960 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/ChatViewQuery.graphql
--rw-r--r--   0        0        0      167 2023-07-19 06:18:30.463987 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/DeleteHumanMessagesMutation.graphql
--rw-r--r--   0        0        0      129 2023-07-19 06:18:30.463987 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/DeleteMessageMutation.graphql
--rw-r--r--   0        0        0      154 2023-07-19 06:18:30.463987 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/DeleteUserMessagesMutation.graphql
--rw-r--r--   0        0        0     1148 2023-07-19 06:18:30.463987 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/ExploreBotsListPaginationQuery.graphql
--rw-r--r--   0        0        0      111 2023-07-19 06:18:30.463987 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/HandleFragment.graphql
--rw-r--r--   0        0        0      319 2023-07-19 06:18:30.464960 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/LoginWithVerificationCodeMutation.graphql
--rw-r--r--   0        0        0     1985 2023-07-19 06:18:30.464960 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/MessageAddedSubscription.graphql
--rw-r--r--   0        0        0      141 2023-07-19 06:18:30.464960 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/MessageDeletedSubscription.graphql
--rw-r--r--   0        0        0      207 2023-07-19 06:18:30.464960 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/MessageFragment.graphql
--rw-r--r--   0        0        0      152 2023-07-19 06:18:30.464960 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/MessageRemoveVoteMutation.graphql
--rw-r--r--   0        0        0      223 2023-07-19 06:18:30.465959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/MessageSetVoteMutation.graphql
--rw-r--r--   0        0        0     1832 2023-07-19 06:18:30.465959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/PoeBotCreateMutation.graphql
--rw-r--r--   0        0        0      968 2023-07-19 06:18:30.465959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/PoeBotEditMutation.graphql
--rw-r--r--   0        0        0      963 2023-07-19 06:18:30.465959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/SendMessageMutation.graphql
--rw-r--r--   0        0        0      275 2023-07-19 06:18:30.465959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/SendVerificationCodeForLoginMutation.graphql
--rw-r--r--   0        0        0      222 2023-07-19 06:18:30.465959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/ShareMessagesMutation.graphql
--rw-r--r--   0        0        0      321 2023-07-19 06:18:30.466959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/SignupWithVerificationCodeMutation.graphql
--rw-r--r--   0        0        0      166 2023-07-19 06:18:30.466959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/StaleChatUpdateMutation.graphql
--rw-r--r--   0        0        0      170 2023-07-19 06:18:30.466959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/SubscriptionsMutation.graphql
--rw-r--r--   0        0        0       98 2023-07-19 06:18:30.466959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/SummarizePlainPostQuery.graphql
--rw-r--r--   0        0        0      150 2023-07-19 06:18:30.466959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/SummarizeQuotePostQuery.graphql
--rw-r--r--   0        0        0      183 2023-07-19 06:18:30.466959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/SummarizeSharePostQuery.graphql
--rw-r--r--   0        0        0      382 2023-07-19 06:18:30.467959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/UserSnippetFragment.graphql
--rw-r--r--   0        0        0      421 2023-07-19 06:18:30.467959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/ViewerInfoQuery.graphql
--rw-r--r--   0        0        0     1068 2023-07-19 06:18:30.467959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/ViewerStateFragment.graphql
--rw-r--r--   0        0        0      700 2023-07-19 06:18:30.467959 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/poe_graphql/ViewerStateUpdatedSubscription.graphql
--rw-r--r--   0        0        0       83 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/__init__.py
--rw-r--r--   0        0        0     1454 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/conversation_style.py
--rw-r--r--   0        0        0      127 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/main.py
--rw-r--r--   0        0        0     5878 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/SydneyGPT.py
--rw-r--r--   0        0        0      719 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/SydneyGPTUtils.py
--rw-r--r--   0        0        0        0 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/__init__.py
--rw-r--r--   0        0        0     5727 2023-07-20 05:13:18.977262 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/config.py
--rw-r--r--   0        0        0     1571 2023-07-20 03:24:26.109430 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/load_config.py
--rw-r--r--   0        0        0     4998 2023-07-19 08:26:34.686822 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/mytypes.py
--rw-r--r--   0        0        0     4583 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/prefix_data.py
--rw-r--r--   0        0        0    30736 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/prompt_data.py
--rw-r--r--   0        0        0     9955 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/user_data.py
--rw-r--r--   0        0        0    14902 2023-07-20 05:13:18.986267 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/app.py
--rw-r--r--   0        0        0      547 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/data/spark_gpt/common/config.json
--rw-r--r--   0        0        0        0 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/templates/__init__.py
--rw-r--r--   0        0        0     4730 2023-07-18 14:23:03.984592 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/templates/config.html
--rw-r--r--   0        0        0     2246 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/templates/index.html
--rw-r--r--   0        0        0    10215 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/templates/prefix.html
--rw-r--r--   0        0        0    10211 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/templates/prompt.html
--rw-r--r--   0        0        0       23 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/__init__.py
--rw-r--r--   0        0        0       51 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/nonebot/__init__.py
--rw-r--r--   0        0        0    17900 2023-07-20 03:23:26.900518 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/nonebot/bot_main.py
--rw-r--r--   0        0        0    26033 2023-07-18 04:44:52.814514 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/nonebot/config_main.py
--rw-r--r--   0        0        0     2275 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/nonebot/userlinks.py
--rw-r--r--   0        0        0    15735 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/nonebot/utils.py
--rw-r--r--   0        0        0     6523 2023-07-19 09:05:38.201293 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/temp_bots.py
--rw-r--r--   0        0        0     2092 2023-07-19 11:14:09.912607 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/render.py
--rw-r--r--   0        0        0  1458204 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/katex/katex.min.b64_fonts.css
--rw-r--r--   0        0        0   270288 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/katex/katex.min.js
--rw-r--r--   0        0        0     1290 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/katex/mathtex-script-type.min.js
--rw-r--r--   0        0        0    19652 2023-07-18 14:07:51.094876 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/markdown.css
--rw-r--r--   0        0        0     1259 2023-07-20 05:13:35.656800 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/markdown.html
--rw-r--r--   0        0        0     4963 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/pygments-default.css
--rw-r--r--   0        0        0      125 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/text.css
--rw-r--r--   0        0        0     1113 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/utils.py
--rw-r--r--   0        0        0     1007 2023-07-20 05:13:43.722190 nonebot_plugin_spark_gpt-1.2.2/pyproject.toml
--rw-r--r--   0        0        0     8478 2023-07-20 05:30:34.715963 nonebot_plugin_spark_gpt-1.2.2/README.md
--rw-r--r--   0        0        0     9689 1970-01-01 00:00:00.000000 nonebot_plugin_spark_gpt-1.2.2/PKG-INFO
+-rw-r--r--   0        0        0      219 2023-07-11 09:53:31.539890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/__init__.py
+-rw-r--r--   0        0        0    17261 2023-07-11 09:53:31.540890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/adapter.py
+-rw-r--r--   0        0        0      138 2023-07-11 09:53:31.541890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/__init__.py
+-rw-r--r--   0        0        0       27 2023-07-11 09:53:31.542890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/client.py
+-rw-r--r--   0        0        0    51932 2023-07-11 09:53:31.542890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/client.pyi
+-rw-r--r--   0        0        0    98693 2023-07-11 09:53:31.543890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/handle.py
+-rw-r--r--   0        0        0   115238 2023-07-11 09:53:31.544890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/model.py
+-rw-r--r--   0        0        0     1482 2023-07-11 09:53:31.544890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/request.py
+-rw-r--r--   0        0        0    34839 2023-07-11 09:53:31.544890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/types.py
+-rw-r--r--   0        0        0     2441 2023-07-11 09:53:31.545890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/utils.py
+-rw-r--r--   0        0        0     7255 2023-07-11 09:53:31.545890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/bot.py
+-rw-r--r--   0        0        0     2192 2023-07-11 09:53:31.546890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/config.py
+-rw-r--r--   0        0        0    28334 2023-07-11 09:53:31.546890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/event.py
+-rw-r--r--   0        0        0     2076 2023-07-11 09:53:31.546890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/exception.py
+-rw-r--r--   0        0        0    13603 2023-07-11 09:53:31.547890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/message.py
+-rw-r--r--   0        0        0     2874 2023-07-11 09:53:31.547890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/payload.py
+-rw-r--r--   0        0        0     1946 2023-07-11 09:53:31.547890 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/typing.py
+-rw-r--r--   0        0        0      626 2023-07-11 09:53:31.548892 nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/utils.py
+-rw-r--r--   0        0        0      836 2023-07-18 04:47:31.258172 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-19 08:14:04.493611 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/__init__.py
+-rw-r--r--   0        0        0     2791 2023-07-20 05:24:51.550258 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/bard.py
+-rw-r--r--   0        0        0     9823 2023-07-20 05:24:51.554259 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/chatgpt_web.py
+-rw-r--r--   0        0        0     9032 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/claude_ai.py
+-rw-r--r--   0        0        0     4733 2023-07-20 03:24:26.105431 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/load_config.py
+-rw-r--r--   0        0        0     6760 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/newbing.py
+-rw-r--r--   0        0        0     6166 2023-07-23 07:41:54.436040 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/poe.py
+-rw-r--r--   0        0        0     7619 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/slack_claude.py
+-rw-r--r--   0        0        0     8129 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/spark_desk.py
+-rw-r--r--   0        0        0     7435 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/sydneybing.py
+-rw-r--r--   0        0        0     6802 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/tongyiqianwen.py
+-rw-r--r--   0        0        0        0 2023-07-19 08:14:04.488610 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/__init__.py
+-rw-r--r--   0        0        0    12575 2023-07-20 04:51:29.348311 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/Bard.py
+-rw-r--r--   0        0        0        0 2023-07-19 08:51:03.240242 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/__init__.py
+-rw-r--r--   0        0        0    17586 2023-07-19 08:50:59.147722 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/BingImageCreator.py
+-rw-r--r--   0        0        0    11837 2023-07-19 08:51:01.064843 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/chathub.py
+-rw-r--r--   0        0        0     2107 2023-07-19 08:51:04.982654 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/constants.py
+-rw-r--r--   0        0        0     4582 2023-07-19 08:51:08.212221 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/conversation.py
+-rw-r--r--   0        0        0     1312 2023-07-19 08:51:06.614074 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/conversation_style.py
+-rw-r--r--   0        0        0     8088 2023-07-19 08:51:10.504420 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/EdgeGPT.py
+-rw-r--r--   0        0        0    14626 2023-07-19 08:50:55.647270 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/EdgeUtils.py
+-rw-r--r--   0        0        0       48 2023-07-19 08:50:53.449019 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/exceptions.py
+-rw-r--r--   0        0        0      278 2023-07-19 08:50:48.240509 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/ImageGen.py
+-rw-r--r--   0        0        0     2332 2023-07-19 08:50:51.738573 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/locale.py
+-rw-r--r--   0        0        0     7757 2023-07-19 08:50:44.460438 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/main.py
+-rw-r--r--   0        0        0     5948 2023-07-19 08:50:50.007184 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/request.py
+-rw-r--r--   0        0        0      992 2023-07-19 08:51:13.314721 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/utilities.py
+-rw-r--r--   0        0        0       83 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/__init__.py
+-rw-r--r--   0        0        0     1454 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/conversation_style.py
+-rw-r--r--   0        0        0      127 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/main.py
+-rw-r--r--   0        0        0     5878 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/SydneyGPT.py
+-rw-r--r--   0        0        0      719 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/SydneyGPTUtils.py
+-rw-r--r--   0        0        0        0 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/__init__.py
+-rw-r--r--   0        0        0     5727 2023-07-20 05:13:18.977262 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/config.py
+-rw-r--r--   0        0        0     1571 2023-07-20 03:24:26.109430 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/load_config.py
+-rw-r--r--   0        0        0     5024 2023-07-22 16:08:08.595543 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/mytypes.py
+-rw-r--r--   0        0        0     4583 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/prefix_data.py
+-rw-r--r--   0        0        0    30736 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/prompt_data.py
+-rw-r--r--   0        0        0     9955 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/user_data.py
+-rw-r--r--   0        0        0    14902 2023-07-20 05:13:18.986267 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/app.py
+-rw-r--r--   0        0        0      547 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/data/spark_gpt/common/config.json
+-rw-r--r--   0        0        0        0 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/templates/__init__.py
+-rw-r--r--   0        0        0     4730 2023-07-18 14:23:03.984592 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/templates/config.html
+-rw-r--r--   0        0        0     2246 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/templates/index.html
+-rw-r--r--   0        0        0    10215 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/templates/prefix.html
+-rw-r--r--   0        0        0    10211 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/templates/prompt.html
+-rw-r--r--   0        0        0       23 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/__init__.py
+-rw-r--r--   0        0        0       51 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/nonebot/__init__.py
+-rw-r--r--   0        0        0    17900 2023-07-20 03:23:26.900518 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/nonebot/bot_main.py
+-rw-r--r--   0        0        0    26033 2023-07-18 04:44:52.814514 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/nonebot/config_main.py
+-rw-r--r--   0        0        0     2275 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/nonebot/userlinks.py
+-rw-r--r--   0        0        0    15735 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/nonebot/utils.py
+-rw-r--r--   0        0        0     6523 2023-07-19 09:05:38.201293 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/temp_bots.py
+-rw-r--r--   0        0        0     2127 2023-07-23 16:05:13.197720 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/render.py
+-rw-r--r--   0        0        0  1458204 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/katex/katex.min.b64_fonts.css
+-rw-r--r--   0        0        0   270288 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/katex/katex.min.js
+-rw-r--r--   0        0        0     1290 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/katex/mathtex-script-type.min.js
+-rw-r--r--   0        0        0    19652 2023-07-18 14:07:51.094876 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/markdown.css
+-rw-r--r--   0        0        0     1259 2023-07-23 16:09:07.997172 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/markdown.html
+-rw-r--r--   0        0        0     4963 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/pygments-default.css
+-rw-r--r--   0        0        0      125 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/text.css
+-rw-r--r--   0        0        0     1113 1979-12-31 16:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/utils.py
+-rw-r--r--   0        0        0     1016 2023-07-23 16:13:42.982870 nonebot_plugin_spark_gpt-1.2.3/pyproject.toml
+-rw-r--r--   0        0        0     8478 2023-07-23 16:09:22.248830 nonebot_plugin_spark_gpt-1.2.3/README.md
+-rw-r--r--   0        0        0     9698 1970-01-01 00:00:00.000000 nonebot_plugin_spark_gpt-1.2.3/PKG-INFO
```

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/adapter.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/adapter.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/client.pyi` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/client.pyi`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/handle.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/handle.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/model.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/model.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/request.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/request.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/types.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/types.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/api/utils.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/api/utils.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/bot.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/bot.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/config.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/config.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/event.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/event.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/exception.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/exception.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/message.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/message.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/payload.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/payload.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/typing.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/typing.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot/adapters/discord/utils.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot/adapters/discord/utils.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/__init__.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/__init__.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/bard.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/bard.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/chatgpt_web.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/chatgpt_web.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/claude_ai.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/claude_ai.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/load_config.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/load_config.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/newbing.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/newbing.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/poe.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/slack_claude.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,231 +1,202 @@
 import asyncio
-import uuid
 
 from nonebot.log import logger
-from nonebot.utils import run_sync
+from slack_sdk.web.async_client import AsyncWebClient
 
-from .utils import poe
 from ..common.config import config
-from ..common.mytypes import CommonUserInfo, BotData, BotInfo
+from ..common.mytypes import BotData, BotInfo, CommonUserInfo
 from ..common.user_data import common_users
 
-COOKIE = ""
-PROXY = ""
+SLACK_USER_TOKEN = ""
+CHANNEL_ID = ""
+CLAUDE_ID = ""
+RECEIVE_INTERVAL = 2
 ABLE = True
-SUBSCRIBE_ABLE = True
-CLIENT = None
-WHITE_LIST = ""
+PRE_MSG = "<忽略'@Claude',删除'@Claude',不说没看到也不说看到>"
 
 
 def load_config():
-    global COOKIE, PROXY, ABLE, SUBSCRIBE_ABLE, WHITE_LIST
+    global SLACK_USER_TOKEN, CHANNEL_ID, CLAUDE_ID, ABLE
     ABLE = True
-    SUBSCRIBE_ABLE = True
     try:
-        PROXY = config.get_config(source="Poe配置", config_name="proxy")
-    except Exception as e:
-        logger.info(f"加载Poe配置时warn:{str(e)},如果你已经配置了分流或全局代理,请无视此warn")
-
-    try:
-        COOKIE = config.get_config(source="Poe配置", config_name="cookie")
+        SLACK_USER_TOKEN = config.get_config("Claude Slack配置", "slack_user_token")
     except Exception as e:
         ABLE = False
-        SUBSCRIBE_ABLE = False
-        logger.warning(f"加载Poe配置时warn:{str(e)},无法使用Poe")
-
+        logger.warning(f"加载Cluade Slack配置时warn:{str(e)},无法使用Cluade Slack")
     try:
-        subscrid = config.get_config(source="Poe配置", config_name="subscribed")
-        if subscrid != "True":
-            SUBSCRIBE_ABLE = False
-            logger.warning(f"加载Poe配置时info:poe设定为未订阅,无法使用poe的订阅功能")
+        CHANNEL_ID = config.get_config("Claude Slack配置", "channel_id")
     except Exception as e:
-        SUBSCRIBE_ABLE = False
-        logger.warning(f"加载Poe配置时info:poe设定为未订阅,无法使用poe的订阅功能")
+        ABLE = False
+        logger.warning(f"加载Cluade Slack配置时warn:{str(e)},无法使用Cluade Slack")
     try:
-        WHITE_LIST += config.get_config(source="Poe配置", config_name="whitelist")
+        CLAUDE_ID = config.get_config("Claude Slack配置", "claude_id")
     except Exception as e:
-        logger.warning(f"加载Poe配置时warn:{str(e)},订阅功能白名单用户无法正常获取")
+        ABLE = False
+        logger.warning(f"加载Cluade Slack配置时warn:{str(e)},无法使用Cluade Slack")
 
 
 load_config()
 
+CLIENT = AsyncWebClient(token=SLACK_USER_TOKEN)
+
 
-class Poe_Bot:
+class Slack_Claude_Bot:
     def __init__(
-            self, common_userinfo: CommonUserInfo, bot_info: BotInfo, bot_data: BotData,
+            self, common_userinfo: CommonUserInfo, bot_info: BotInfo, bot_data: BotData
     ):
         self.lock = asyncio.Lock()
         self.nickname = bot_info.nickname
-        self.common_userinfo = common_userinfo
-        self.botdata = bot_data
-        self.source = bot_data.source
 
-        if self.source == "poe claude":
-            self.base_model = "a2"
-        elif self.source == "poe chatgpt":
-            self.base_model = "chinchilla"
-        elif self.source == "poe chatgpt4":
-            if not SUBSCRIBE_ABLE:
-                raise Exception("Poe账户未订阅,无法使用订阅功能")
-            if self.common_userinfo.user_id not in WHITE_LIST:
-                raise Exception("你不在poe订阅功能白名单内,无法使用订阅功能")
-            self.base_model = "beaver"
-        else:
-            if not SUBSCRIBE_ABLE:
-                raise Exception("Poe账户未订阅,无法使用订阅功能")
-            if self.common_userinfo.user_id not in WHITE_LIST:
-                raise Exception("你不在poe订阅功能白名单内,无法使用订阅功能")
-            self.base_model = "a2_2"
-
-        if not COOKIE:
-            raise Exception("Poe的配置cookie没有填写,无法使用")
-
-    def __hash__(self) -> int:
-        return hash((self.common_userinfo.user_id, self.nickname))
-
-    async def ask(self, question: str):
-        if self.botdata.source == "poe chatgpt4" or self.botdata.source == "poe claude-2-100k":
-            if not SUBSCRIBE_ABLE:
-                raise Exception("Poe账户未订阅,无法使用订阅功能")
-            if not self.common_userinfo.user_id in WHITE_LIST:
-                raise Exception("你不在poe订阅功能白名单内,无法使用订阅功能")
-        if self.botdata.prefix:
-            question += self.botdata.prefix + "\n" + question
-        if not self.botdata.handle:
-            await self.refresh()
-        try:
-            answer = await self.chat(question)
+        self.botdata = bot_data
+        self.common_userinfo = common_userinfo
+        if not (SLACK_USER_TOKEN and CHANNEL_ID and CLAUDE_ID):
+            raise Exception(
+                "Claude Slack的配置项slack_user_token,CHANNEL_ID,claude_id没有填写全,无法使用"
+            )
 
-            return answer
-        except Exception as e:
-            raise e
+    def __hash__(self):
+        return hash((self.nickname, self.common_userinfo.user_id))
 
     async def refresh(self):
-        if self.botdata.source == "poe chatgpt4" or self.botdata.source == "poe claude-2-100k":
-            if not SUBSCRIBE_ABLE:
-                raise Exception("Poe账户未订阅,无法使用订阅功能")
-            if self.common_userinfo.user_id not in WHITE_LIST:
-                raise Exception("你不在poe订阅功能白名单内,无法使用订阅功能")
-        if not self.botdata.handle:
+        self.botdata.msg_ts = ""
+        self.botdata.thread_ts = ""
+
+        if self.botdata.prompt:
             try:
-                await self.new_bot()
-                await self.chat(self.botdata.prompt)
+                _ = await self.claude_chat(question=self.botdata.prompt)
+
+                return
             except Exception as e:
-                raise e
+                error = f"Claude Slack刷新预设时error:{str(e)}"
+                logger.error(error)
+                raise Exception(error)
         else:
+            common_users.save_userdata(self.common_userinfo)
+            return
+
+    async def ask(self, question: str):
+        if not self.botdata.thread_ts and self.botdata.prompt:
             try:
-                await self.chat_break()
-                await self.chat(self.botdata.prompt)
+                _ = await self.claude_chat(question=self.botdata.prompt)
             except Exception as e:
-                raise e
+                error = f"Claude Slack加载预设时error:{str(e)}"
+                logger.error(error)
+                raise Exception(error)
 
-        return
+        if self.botdata.prefix:
+            question = self.botdata.prefix + "\n" + question
+        try:
+            answer = await self.claude_chat(question=question)
 
-    @run_sync
-    def chat_break(self):
-        detail_error = "未知错误"
-        retry = 1
-        if not CLIENT:
-            try:
-                self.new_client()
-            except Exception as e:
-                raise e
-        while retry > 0:
-            error = "未知错误"
-            try:
-                CLIENT.send_chat_break(self.botdata.handle)
-                return
-            except Exception as e:
-                detail_error = str(e)
-                logger.error(f"Poe在清除会话记录时error:{detail_error}")
-                # # if retry % 1 == 0:
-                #     try:
-                #         self.new_client()
-                #     except Exception as e:
-                #         raise e
-                retry -= 1
-        error = f"Poe在清除会话记录时出错次数超过上限:{detail_error}"
-        raise Exception(error)
+            return answer
+        except Exception as e:
+            error = f"Claude Slack询问时error:{str(e)}"
+            logger.error(error)
+            raise Exception(error)
 
-    @run_sync
-    def chat(self, question: str):
-        if not CLIENT:
-            try:
-                self.new_client()
-            except Exception as e:
-                raise e
-        retry = 1
-        while retry > 0:
-            detail_error = "未知错误"
-            try:
-                for chunk in CLIENT.send_message(self.botdata.handle, question):
-                    pass
-                return chunk["text"]
-            except Exception as e:
-                detail_error = str(e)
-                logger.error(f"Poe在询问时error:{str(detail_error)}")
-                # if retry % 1 == 0:
-                #     try:
-                #         self.new_client()
-                #     except Exception as e:
-                #         raise e
-                retry -= 1
-        error = f"Poe在询问时错误次数超过上限:{detail_error}"
-        logger.error(error)
-        raise Exception(error)
-
-    @run_sync
-    def new_bot(self):
-        if not CLIENT:
-            try:
-                self.new_client()
-            except Exception as e:
-                raise e
-        generated_uuid = uuid.uuid4()
-        random_handle = generated_uuid.hex.replace("-", "")[0:15]
-        self.botdata.handle = random_handle
-        retry = 1
+    async def receive_message(self):
+        retry = 5
         detail_error = "未知错误"
         while retry > 0:
+            await asyncio.sleep(1)
             try:
-                CLIENT.create_bot(
-                    self.botdata.handle,
-                    "在吗",
-                    base_model=self.base_model,
+                # 使用Web客户端调用conversations.replies方法
+                result = await CLIENT.conversations_replies(
+                    ts=self.botdata.thread_ts,
+                    channel=CHANNEL_ID,
+                    oldest=self.botdata.msg_ts,
                 )
-                common_users.save_userdata(common_userinfo=self.common_userinfo)
-                return
+                result = result.data
+                if (
+                        not result
+                        or len(result["messages"]) < 1
+                        or result["messages"][-1]["user"] != CLAUDE_ID
+                        or (
+                        result["messages"][-1]["text"] == "_Typing…_"
+                        or (
+                                result["messages"][-1]["text"].startswith(
+                                    "\n&gt; _*Please note:*"
+                                )
+                                and result["messages"][-2]["text"] == "_Typing…_"
+                        )
+                )
+                ):
+                    await asyncio.sleep(2)
+                    raise Exception("slack的claude没有回复")
+                elif "error" in result.keys():
+                    raise Exception(result["error"])
+                elif result["ok"]:
+                    if result["messages"][-1]["text"].startswith(
+                            "\n&gt; _*Please note:*"
+                    ):
+                        return result["messages"][-2]["text"]
+                    else:
+                        return result["messages"][-1]["text"]
+                else:
+                    raise Exception("未知错误")
             except Exception as e:
                 detail_error = str(e)
-                logger.error(f"Poe在创建新的bot时报错:{detail_error}")
-                if retry == 1:
-                    try:
-                        self.new_client()
-                    except Exception as e:
-                        raise e
+                error = f"Claude Slack在获取消息到频道{CHANNEL_ID}时error: {e}"
+                logger.error(error)
                 retry -= 1
+        raise Exception(detail_error)
 
-        error = f"Poe在创建新的bot时报错次数超出上限:{detail_error}"
-        logger.error(error)
-        raise Exception(error)
-
-    def new_client(self):
-        global CLIENT
-        retry = 1
+    async def send_msg(self, msg: str):
+        result = await CLIENT.chat_postMessage(
+            channel=CHANNEL_ID,
+            text=f"<@{CLAUDE_ID}>{PRE_MSG}{msg}",
+            thread_ts=self.botdata.thread_ts,
+        )
+        if result["ok"]:
+            return result["ts"]
+        else:
+            result = result["ok"]
+            error = f"在发向claude的消息时error:{result}"
+            logger.error(error)
+            raise Exception(error)
+
+    async def get_msg(self, question: str):
+        response = "_Typing…_"
+        retry = 3
         detail_error = "未知错误"
-        while retry > 0:
-            try:
-                if PROXY:
-                    CLIENT = poe.Client(token=COOKIE, proxy=PROXY)
-                    return
-                else:
-                    CLIENT = poe.Client(token=COOKIE)
-                    return
-            except Exception as e:
-                detail_error = str(e)
-                retry -= 1
-                error = f"Poe在生成新的Client时报错:{detail_error}"
-                logger.error(error)
-        error = f"Poe在生成新的Client时报错次数超出上限:{detail_error}"
-        logger.error(error)
-        raise Exception(error)
+        while response.endswith("_Typing…_"):
+            while retry > 0:
+                try:
+                    response = await self.receive_message()
+                    if not response.endswith("_Typing…_"):
+                        break
+                except Exception as e:
+                    detail_error = str(e)
+                    if detail_error == "slack的claude没有回复":
+                        await self.send_msg(question)
+                    retry -= 1
+            if retry <= 0:
+                raise Exception(detail_error)
+        return response
+
+    async def claude_chat(self, question: str):
+        try:
+            # new_ts可以理解为新发送的消息的id,而self.botdata.thread_ts则是一个消息列的id
+            new_ts = await self.send_msg(question)
+            self.botdata.msg_ts = new_ts
+            if not self.botdata.thread_ts:
+                self.botdata.thread_ts = new_ts
+            common_users.save_userdata(common_userinfo=self.common_userinfo)
+        except Exception as e:
+            error = f"Claud Slack在发送消息时error:{str(e)}"
+            logger.error(error)
+            raise Exception(error)
+        try:
+            answer = await asyncio.wait_for(
+                self.get_msg(question),
+                timeout=120,
+            )
+            return answer
+        except asyncio.TimeoutError as e:
+            error = "Claude Slack在获取消息时超时"
+            logger.error(error)
+            raise Exception(error)
+        except Exception as e:
+            error = f"Claude Slack在获取消息时error{str(e)},如果多次无回复可以尝试刷新对话"
+            logger.error(error)
+            raise Exception(error)
```

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/spark_desk.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/spark_desk.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/sydneybing.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/sydneybing.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/tongyiqianwen.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/tongyiqianwen.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/Bard.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/Bard.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/BingImageCreator.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/BingImageCreator.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/chathub.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/chathub.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/constants.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/constants.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/conversation.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/conversation.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/conversation_style.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/conversation_style.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/EdgeGPT.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/EdgeGPT.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/EdgeUtils.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/EdgeUtils.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/locale.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/locale.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/main.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/main.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/request.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/request.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/utilities.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/EdgeGPT/utilities.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/conversation_style.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/conversation_style.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/SydneyGPT.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/SydneyGPT.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/SydneyGPTUtils.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/chatbot/utils/SydneyGPT/SydneyGPTUtils.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/config.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/config.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/load_config.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/load_config.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/mytypes.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/mytypes.py`

 * *Files 1% similar despite different names*

```diff
@@ -22,14 +22,15 @@
 
 
 class BotData(BaseModel):
     """Bot的数据类型"""
 
     """poe"""
     handle: Optional[str]
+    model: Optional[str]
     """chatgpt web"""
     conversation_id: Optional[str]
     parent_id: Optional[str]
     """通义千问"""
     sessionId: Optional[str]
     parentMsgId: Optional[str]
     userId: Optional[str]
```

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/prefix_data.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/prefix_data.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/prompt_data.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/prompt_data.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/user_data.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/user_data.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/app.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/app.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/data/spark_gpt/common/config.json` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/data/spark_gpt/common/config.json`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/templates/config.html` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/templates/config.html`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/templates/index.html` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/templates/index.html`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/templates/prefix.html` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/templates/prefix.html`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/common/web/templates/prompt.html` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/common/web/templates/prompt.html`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/nonebot/bot_main.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/nonebot/bot_main.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/nonebot/config_main.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/nonebot/config_main.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/nonebot/userlinks.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/nonebot/userlinks.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/nonebot/utils.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/nonebot/utils.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/platforms/temp_bots.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/platforms/temp_bots.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/render.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/render.py`

 * *Files 2% similar despite different names*

```diff
@@ -26,14 +26,15 @@
 
 
 async def read_tpl(path: str) -> str:
     return await read_file(f"{TEMPLATES_PATH}/{path}")
 
 
 async def md_to_pic(md: str, width: int = 600, font_path: str = Font_Path):
+    md = md.replace("\n", "  \n")
     if md.count("```") % 2 == 1:
         md += "  \n```"
     md = markdown.markdown(
         md,
         extensions=[
             "pymdownx.tasklist",
             "tables",
```

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/katex/katex.min.b64_fonts.css` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/katex/katex.min.b64_fonts.css`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/katex/katex.min.js` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/katex/katex.min.js`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/katex/mathtex-script-type.min.js` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/katex/mathtex-script-type.min.js`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/markdown.css` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/markdown.css`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/markdown.html` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/markdown.html`

 * *Files 0% similar despite different names*

```diff
@@ -31,15 +31,15 @@
                 font-family: "Custom Font";
                 padding: 8px !important;
             }
         }
 
         .markdown-body::after {
             font-family: "Custom Font";
-            content: "Spark GPT 1.2.2";
+            content: "Spark GPT 1.2.3";
             font-size: 10px !important;
             font-weight: bold;
             color: black;
         }
     </style>
 </head>
```

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/templates/pygments-default.css` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/templates/pygments-default.css`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/nonebot_plugin_spark_gpt/utils/utils.py` & `nonebot_plugin_spark_gpt-1.2.3/nonebot_plugin_spark_gpt/utils/utils.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_spark_gpt-1.2.2/pyproject.toml` & `nonebot_plugin_spark_gpt-1.2.3/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "nonebot_plugin_spark_gpt"
-version = "1.2.2"
+version = "1.2.3"
 description = "Spark-GPT,将多种来源的gpt接入qq,TG,Kook,Discord及更多平台,提供webui进行实时配置热更新,效率高超,使用便捷,管理完善,功能强大"
 authors = ["canxin121 <1969730106@qq.com>"]
 readme = "README.md"
 packages = [{ include = "nonebot_plugin_spark_gpt"},{ include = "nonebot"}]
 
 [tool.poetry.dependencies]
 nonebot-adapter-onebot = "^2.2.1"
@@ -15,15 +15,15 @@
 python = "^3.10"
 aiohttp = "^3.8.4"
 bidict = "^0.22.1"
 edgegpt = "0.12.1"
 Sydneygpt = "0.11.8"
 fastapi = "^0.100.0"
 httpx = "^0.24.1"
-poe-api = "^0.4.8"
+async-poe-client = "^0.1.4"
 pydantic = "^1.10.9"
 slack-sdk = "^3.21.3"
 uvicorn = "^0.22.0"
 python-multipart = "^0.0.6"
 charset_normalizer = "^3.1.0"
 googlebard = "^1.4.0"
```

### Comparing `nonebot_plugin_spark_gpt-1.2.2/README.md` & `nonebot_plugin_spark_gpt-1.2.3/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -17,15 +17,15 @@
     <img src="https://img.shields.io/badge/OneBot-v11-black?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABABAMAAABYR2ztAAAAIVBMVEUAAAAAAAADAwMHBwceHh4UFBQNDQ0ZGRkoKCgvLy8iIiLWSdWYAAAAAXRSTlMAQObYZgAAAQVJREFUSMftlM0RgjAQhV+0ATYK6i1Xb+iMd0qgBEqgBEuwBOxU2QDKsjvojQPvkJ/ZL5sXkgWrFirK4MibYUdE3OR2nEpuKz1/q8CdNxNQgthZCXYVLjyoDQftaKuniHHWRnPh2GCUetR2/9HsMAXyUT4/3UHwtQT2AggSCGKeSAsFnxBIOuAggdh3AKTL7pDuCyABcMb0aQP7aM4AnAbc/wHwA5D2wDHTTe56gIIOUA/4YYV2e1sg713PXdZJAuncdZMAGkAukU9OAn40O849+0ornPwT93rphWF0mgAbauUrEOthlX8Zu7P5A6kZyKCJy75hhw1Mgr9RAUvX7A3csGqZegEdniCx30c3agAAAABJRU5ErkJggg==" alt="onebot">
     <a href="https://github.com/canxin121/nonebot_poe_chat/releases/">
     <img src="https://img.shields.io/github/last-commit/canxin121/Spark-GPT" alt="github">
     </a>
 </p>
 <div align="left">
 
-## 最新版本号1.2.2
+## 最新版本号1.2.3
 # 详细教程-> [![残心文档库](source/doc.png)](https://canxin121.github.io/docs/docs/Spark_GPT.html)  
   
 ---
 # 介绍部分
 
 ## 功能特性
```

#### html2text {}

```diff
@@ -1,14 +1,14 @@
                 [https://socialify.git.ci/canxin121/Spark-GPT/
 image?font=Raleway&forks=1&issues=1&language=1&logo=https%3A%2F%2Fcanxin121.github.io%2Fdocs%2Flogo.png&name=1&owner=1&pattern=Charlie%20Brown&pulls=1&stargazers=1&theme=Auto]
                          ****** Spark-GPTä»åº ******
                                    Spark-GPT
                             [pypi] [python] [pypi]
                                [onebot]_[github]
-## ææ°çæ¬å·1.2.2 # è¯¦ç»æç¨-> [![æ®å¿ææ¡£åº](source/doc.png)]
+## ææ°çæ¬å·1.2.3 # è¯¦ç»æç¨-> [![æ®å¿ææ¡£åº](source/doc.png)]
 (https://canxin121.github.io/docs/docs/Spark_GPT.html) --- # ä»ç»é¨å ##
 åè½ç¹æ§ - æ±èä¼å¤æ¥æºçgpt(poe
 (chatgpt+claude),chatgptç½é¡µç,Newbing,Sdyney bing,slack claude,claude
 ai,è®¯é£æç«,éä¹åé®),æ¯æå¤å¹³å°(tg,kook( åå¼é»å¦),qq
 (gocq),discord)ä½¿ç¨ä¸ä¸åå¹³å°ç¨æ·æ°æ®ç»å®äºé -
 æ¯æäººæ ¼é¢è®¾ååç¼ç³»ç»,æ¯ææè½¬å¾æè½¬é¾æ¥,æ¯ææ¯ä¸ªç¨æ·åå»ºä¸åæ¥æºä¸åäººæ ¼çbot,åæ¶æ¯æå¬ç¨å±åçbot
 -
```

### Comparing `nonebot_plugin_spark_gpt-1.2.2/PKG-INFO` & `nonebot_plugin_spark_gpt-1.2.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,31 +1,31 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-spark-gpt
-Version: 1.2.2
+Version: 1.2.3
 Summary: Spark-GPT,将多种来源的gpt接入qq,TG,Kook,Discord及更多平台,提供webui进行实时配置热更新,效率高超,使用便捷,管理完善,功能强大
 Author: canxin121
 Author-email: 1969730106@qq.com
 Requires-Python: >=3.10,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: Sydneygpt (==0.11.8)
 Requires-Dist: aiohttp (>=3.8.4,<4.0.0)
+Requires-Dist: async-poe-client (>=0.1.4,<0.2.0)
 Requires-Dist: bidict (>=0.22.1,<0.23.0)
 Requires-Dist: charset_normalizer (>=3.1.0,<4.0.0)
 Requires-Dist: edgegpt (==0.12.1)
 Requires-Dist: fastapi (>=0.100.0,<0.101.0)
 Requires-Dist: googlebard (>=1.4.0,<2.0.0)
 Requires-Dist: httpx (>=0.24.1,<0.25.0)
 Requires-Dist: nonebot-adapter-kaiheila (>=0.2.7,<0.3.0)
 Requires-Dist: nonebot-adapter-onebot (>=2.2.1,<3.0.0)
 Requires-Dist: nonebot-adapter-telegram (>=0.1.0b6,<0.2.0)
 Requires-Dist: nonebot-plugin-htmlrender (>=0.2.1,<0.3.0)
 Requires-Dist: nonebot-plugin-templates (>=0.1.1,<0.2.0)
-Requires-Dist: poe-api (>=0.4.8,<0.5.0)
 Requires-Dist: pydantic (>=1.10.9,<2.0.0)
 Requires-Dist: python-multipart (>=0.0.6,<0.0.7)
 Requires-Dist: slack-sdk (>=3.21.3,<4.0.0)
 Requires-Dist: uvicorn (>=0.22.0,<0.23.0)
 Description-Content-Type: text/markdown
 
 <div align="center">
@@ -47,15 +47,15 @@
     <img src="https://img.shields.io/badge/OneBot-v11-black?style=social&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAEAAAABABAMAAABYR2ztAAAAIVBMVEUAAAAAAAADAwMHBwceHh4UFBQNDQ0ZGRkoKCgvLy8iIiLWSdWYAAAAAXRSTlMAQObYZgAAAQVJREFUSMftlM0RgjAQhV+0ATYK6i1Xb+iMd0qgBEqgBEuwBOxU2QDKsjvojQPvkJ/ZL5sXkgWrFirK4MibYUdE3OR2nEpuKz1/q8CdNxNQgthZCXYVLjyoDQftaKuniHHWRnPh2GCUetR2/9HsMAXyUT4/3UHwtQT2AggSCGKeSAsFnxBIOuAggdh3AKTL7pDuCyABcMb0aQP7aM4AnAbc/wHwA5D2wDHTTe56gIIOUA/4YYV2e1sg713PXdZJAuncdZMAGkAukU9OAn40O849+0ornPwT93rphWF0mgAbauUrEOthlX8Zu7P5A6kZyKCJy75hhw1Mgr9RAUvX7A3csGqZegEdniCx30c3agAAAABJRU5ErkJggg==" alt="onebot">
     <a href="https://github.com/canxin121/nonebot_poe_chat/releases/">
     <img src="https://img.shields.io/github/last-commit/canxin121/Spark-GPT" alt="github">
     </a>
 </p>
 <div align="left">
 
-## 最新版本号1.2.2
+## 最新版本号1.2.3
 # 详细教程-> [![残心文档库](source/doc.png)](https://canxin121.github.io/docs/docs/Spark_GPT.html)  
   
 ---
 # 介绍部分
 
 ## 功能特性
```

#### html2text {}

```diff
@@ -1,32 +1,32 @@
-Metadata-Version: 2.1 Name: nonebot-plugin-spark-gpt Version: 1.2.2 Summary:
+Metadata-Version: 2.1 Name: nonebot-plugin-spark-gpt Version: 1.2.3 Summary:
 Spark-
 GPT,å°å¤ç§æ¥æºçgptæ¥å¥qq,TG,Kook,Discordåæ´å¤å¹³å°,æä¾webuiè¿è¡å®æ¶éç½®ç­æ´æ°,æçé«è¶,ä½¿ç¨ä¾¿æ·,ç®¡çå®å,åè½å¼ºå¤§
 Author: canxin121 Author-email: 1969730106@qq.com Requires-Python: >=3.10,<4.0
 Classifier: Programming Language :: Python :: 3 Classifier: Programming
 Language :: Python :: 3.10 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: Sydneygpt (==0.11.8) Requires-Dist: aiohttp (>=3.8.4,<4.0.0)
-Requires-Dist: bidict (>=0.22.1,<0.23.0) Requires-Dist: charset_normalizer
-(>=3.1.0,<4.0.0) Requires-Dist: edgegpt (==0.12.1) Requires-Dist: fastapi
-(>=0.100.0,<0.101.0) Requires-Dist: googlebard (>=1.4.0,<2.0.0) Requires-Dist:
-httpx (>=0.24.1,<0.25.0) Requires-Dist: nonebot-adapter-kaiheila
-(>=0.2.7,<0.3.0) Requires-Dist: nonebot-adapter-onebot (>=2.2.1,<3.0.0)
-Requires-Dist: nonebot-adapter-telegram (>=0.1.0b6,<0.2.0) Requires-Dist:
-nonebot-plugin-htmlrender (>=0.2.1,<0.3.0) Requires-Dist: nonebot-plugin-
-templates (>=0.1.1,<0.2.0) Requires-Dist: poe-api (>=0.4.8,<0.5.0) Requires-
-Dist: pydantic (>=1.10.9,<2.0.0) Requires-Dist: python-multipart
-(>=0.0.6,<0.0.7) Requires-Dist: slack-sdk (>=3.21.3,<4.0.0) Requires-Dist:
-uvicorn (>=0.22.0,<0.23.0) Description-Content-Type: text/markdown
+Requires-Dist: async-poe-client (>=0.1.4,<0.2.0) Requires-Dist: bidict
+(>=0.22.1,<0.23.0) Requires-Dist: charset_normalizer (>=3.1.0,<4.0.0) Requires-
+Dist: edgegpt (==0.12.1) Requires-Dist: fastapi (>=0.100.0,<0.101.0) Requires-
+Dist: googlebard (>=1.4.0,<2.0.0) Requires-Dist: httpx (>=0.24.1,<0.25.0)
+Requires-Dist: nonebot-adapter-kaiheila (>=0.2.7,<0.3.0) Requires-Dist:
+nonebot-adapter-onebot (>=2.2.1,<3.0.0) Requires-Dist: nonebot-adapter-telegram
+(>=0.1.0b6,<0.2.0) Requires-Dist: nonebot-plugin-htmlrender (>=0.2.1,<0.3.0)
+Requires-Dist: nonebot-plugin-templates (>=0.1.1,<0.2.0) Requires-Dist:
+pydantic (>=1.10.9,<2.0.0) Requires-Dist: python-multipart (>=0.0.6,<0.0.7)
+Requires-Dist: slack-sdk (>=3.21.3,<4.0.0) Requires-Dist: uvicorn
+(>=0.22.0,<0.23.0) Description-Content-Type: text/markdown
                 [https://socialify.git.ci/canxin121/Spark-GPT/
 image?font=Raleway&forks=1&issues=1&language=1&logo=https%3A%2F%2Fcanxin121.github.io%2Fdocs%2Flogo.png&name=1&owner=1&pattern=Charlie%20Brown&pulls=1&stargazers=1&theme=Auto]
                          ****** Spark-GPTä»åº ******
                                    Spark-GPT
                             [pypi] [python] [pypi]
                                [onebot]_[github]
-## ææ°çæ¬å·1.2.2 # è¯¦ç»æç¨-> [![æ®å¿ææ¡£åº](source/doc.png)]
+## ææ°çæ¬å·1.2.3 # è¯¦ç»æç¨-> [![æ®å¿ææ¡£åº](source/doc.png)]
 (https://canxin121.github.io/docs/docs/Spark_GPT.html) --- # ä»ç»é¨å ##
 åè½ç¹æ§ - æ±èä¼å¤æ¥æºçgpt(poe
 (chatgpt+claude),chatgptç½é¡µç,Newbing,Sdyney bing,slack claude,claude
 ai,è®¯é£æç«,éä¹åé®),æ¯æå¤å¹³å°(tg,kook( åå¼é»å¦),qq
 (gocq),discord)ä½¿ç¨ä¸ä¸åå¹³å°ç¨æ·æ°æ®ç»å®äºé -
 æ¯æäººæ ¼é¢è®¾ååç¼ç³»ç»,æ¯ææè½¬å¾æè½¬é¾æ¥,æ¯ææ¯ä¸ªç¨æ·åå»ºä¸åæ¥æºä¸åäººæ ¼çbot,åæ¶æ¯æå¬ç¨å±åçbot
 -
```

