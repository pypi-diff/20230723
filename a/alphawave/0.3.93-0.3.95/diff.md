# Comparing `tmp/alphawave-0.3.93.tar.gz` & `tmp/alphawave-0.3.95.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "alphawave-0.3.93.tar", last modified: Thu Jul 20 19:06:00 2023, max compression
+gzip compressed data, was "alphawave-0.3.95.tar", last modified: Sun Jul 23 18:04:41 2023, max compression
```

## Comparing `alphawave-0.3.93.tar` & `alphawave-0.3.95.tar`

### file list

```diff
@@ -1,63 +1,72 @@
-drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-20 19:06:00.686530 alphawave-0.3.93/
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1070 2023-06-05 21:12:30.000000 alphawave-0.3.93/LICENSE
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     9439 2023-07-20 19:06:00.686530 alphawave-0.3.93/PKG-INFO
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     8859 2023-06-18 19:15:49.000000 alphawave-0.3.93/README.md
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1022 2023-07-20 19:05:50.000000 alphawave-0.3.93/pyproject.toml
--rw-rw-r--   0 bruce     (1000) bruce     (1000)       38 2023-07-20 19:06:00.686530 alphawave-0.3.93/setup.cfg
-drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-20 19:06:00.678530 alphawave-0.3.93/src/
-drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-20 19:06:00.682530 alphawave-0.3.93/src/alphawave/
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     9961 2023-07-18 17:07:38.000000 alphawave-0.3.93/src/alphawave/AlphaWave.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1370 2023-06-10 00:08:35.000000 alphawave-0.3.93/src/alphawave/Colorize.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)      740 2023-06-18 18:50:38.000000 alphawave-0.3.93/src/alphawave/DefaultResponseValidator.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     8173 2023-07-09 19:31:41.000000 alphawave-0.3.93/src/alphawave/JSONResponseValidator.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1173 2023-06-19 22:47:36.000000 alphawave-0.3.93/src/alphawave/MemoryFork.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     7164 2023-07-11 18:23:11.000000 alphawave-0.3.93/src/alphawave/OSClient.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     5926 2023-07-11 18:29:03.000000 alphawave-0.3.93/src/alphawave/OpenAIClient.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     4120 2023-07-16 20:12:02.000000 alphawave-0.3.93/src/alphawave/PythonResponseValidator.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1365 2023-07-10 16:02:12.000000 alphawave-0.3.93/src/alphawave/RepairTestClient.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     3008 2023-06-15 23:14:04.000000 alphawave-0.3.93/src/alphawave/Response.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     6969 2023-07-18 17:07:21.000000 alphawave-0.3.93/src/alphawave/TOMLResponseValidator.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)      800 2023-06-15 04:12:01.000000 alphawave-0.3.93/src/alphawave/TestClient.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1515 2023-06-15 04:12:10.000000 alphawave-0.3.93/src/alphawave/TestClientTest.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)        0 2023-06-06 23:52:12.000000 alphawave-0.3.93/src/alphawave/__init__.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1377 2023-07-11 21:25:58.000000 alphawave-0.3.93/src/alphawave/alphawaveTypes.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     4163 2023-06-04 18:16:08.000000 alphawave-0.3.93/src/alphawave/internalTypes.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)      782 2023-06-07 21:02:29.000000 alphawave-0.3.93/src/alphawave/jsonParser.py
-drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-20 19:06:00.682530 alphawave-0.3.93/src/alphawave.egg-info/
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     9439 2023-07-20 19:06:00.000000 alphawave-0.3.93/src/alphawave.egg-info/PKG-INFO
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1818 2023-07-20 19:06:00.000000 alphawave-0.3.93/src/alphawave.egg-info/SOURCES.txt
--rw-rw-r--   0 bruce     (1000) bruce     (1000)        1 2023-07-20 19:06:00.000000 alphawave-0.3.93/src/alphawave.egg-info/dependency_links.txt
--rw-rw-r--   0 bruce     (1000) bruce     (1000)      199 2023-07-20 19:06:00.000000 alphawave-0.3.93/src/alphawave.egg-info/requires.txt
--rw-rw-r--   0 bruce     (1000) bruce     (1000)       44 2023-07-20 19:06:00.000000 alphawave-0.3.93/src/alphawave.egg-info/top_level.txt
-drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-20 19:06:00.682530 alphawave-0.3.93/src/alphawave_agents/
--rw-rw-r--   0 bruce     (1000) bruce     (1000)    17679 2023-07-12 20:04:10.000000 alphawave-0.3.93/src/alphawave_agents/Agent.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1715 2023-07-11 02:39:22.000000 alphawave-0.3.93/src/alphawave_agents/AgentCommandSection.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     7018 2023-07-16 16:56:57.000000 alphawave-0.3.93/src/alphawave_agents/AgentCommandValidator.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1428 2023-07-12 19:12:18.000000 alphawave-0.3.93/src/alphawave_agents/AskCommand.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1871 2023-06-07 03:14:30.000000 alphawave-0.3.93/src/alphawave_agents/CompleteTaskCommand.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1336 2023-06-06 16:52:41.000000 alphawave-0.3.93/src/alphawave_agents/ConfirmAnswerCommand.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1423 2023-07-12 19:12:30.000000 alphawave-0.3.93/src/alphawave_agents/FinalAnswerCommand.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1518 2023-07-12 19:12:07.000000 alphawave-0.3.93/src/alphawave_agents/MathCommand.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     3249 2023-07-12 00:55:02.000000 alphawave-0.3.93/src/alphawave_agents/PromptCommand.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     7938 2023-07-12 19:12:49.000000 alphawave-0.3.93/src/alphawave_agents/SchemaBasedCommand.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     2452 2023-06-09 18:41:37.000000 alphawave-0.3.93/src/alphawave_agents/SentimentAnalysis.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     2149 2023-06-06 16:59:49.000000 alphawave-0.3.93/src/alphawave_agents/SetPropertyCommand.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)        0 2023-06-06 23:52:38.000000 alphawave-0.3.93/src/alphawave_agents/__init__.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1859 2023-07-06 03:51:05.000000 alphawave-0.3.93/src/alphawave_agents/agentTypes.py
-drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-20 19:06:00.682530 alphawave-0.3.93/src/alphawave_pyexts/
--rw-rw-r--   0 bruce     (1000) bruce     (1000)    11096 2023-06-24 23:27:36.000000 alphawave-0.3.93/src/alphawave_pyexts/FsInference.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     6409 2023-07-19 16:46:22.000000 alphawave-0.3.93/src/alphawave_pyexts/LLMClient.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     2858 2023-07-12 19:14:52.000000 alphawave-0.3.93/src/alphawave_pyexts/SearchCommand.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)    11610 2023-06-22 19:47:31.000000 alphawave-0.3.93/src/alphawave_pyexts/chat.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     2607 2023-06-24 00:18:59.000000 alphawave-0.3.93/src/alphawave_pyexts/configuration_RW.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)    25504 2023-07-20 19:04:26.000000 alphawave-0.3.93/src/alphawave_pyexts/conversation.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     1154 2023-06-24 03:11:55.000000 alphawave-0.3.93/src/alphawave_pyexts/handler.py
-drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-20 19:06:00.686530 alphawave-0.3.93/src/alphawave_pyexts/llmsearch/
--rw-rw-r--   0 bruce     (1000) bruce     (1000)    13645 2023-07-11 19:55:51.000000 alphawave-0.3.93/src/alphawave_pyexts/llmsearch/google_search_concurrent.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)      972 2023-07-12 19:15:47.000000 alphawave-0.3.93/src/alphawave_pyexts/llmsearch/search_service.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)    47520 2023-06-24 00:15:02.000000 alphawave-0.3.93/src/alphawave_pyexts/modelling_RW.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)    12724 2023-07-02 15:55:18.000000 alphawave-0.3.93/src/alphawave_pyexts/serverUtils.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)     8718 2023-07-18 17:08:04.000000 alphawave-0.3.93/src/alphawave_pyexts/utilityV2.py
-drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-20 19:06:00.686530 alphawave-0.3.93/tests/
--rw-rw-r--   0 bruce     (1000) bruce     (1000)    14779 2023-06-07 17:09:31.000000 alphawave-0.3.93/tests/testOSClient.py
--rw-rw-r--   0 bruce     (1000) bruce     (1000)    14639 2023-06-18 18:49:14.000000 alphawave-0.3.93/tests/testOpenAiClient.py
+drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-23 18:04:41.053033 alphawave-0.3.95/
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1070 2023-06-05 21:12:30.000000 alphawave-0.3.95/LICENSE
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     9439 2023-07-23 18:04:41.053033 alphawave-0.3.95/PKG-INFO
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     8859 2023-06-18 19:15:49.000000 alphawave-0.3.95/README.md
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1022 2023-07-23 18:04:31.000000 alphawave-0.3.95/pyproject.toml
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)       38 2023-07-23 18:04:41.053033 alphawave-0.3.95/setup.cfg
+drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-23 18:04:41.045033 alphawave-0.3.95/src/
+drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-23 18:04:41.049033 alphawave-0.3.95/src/alphawave/
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     9620 2023-07-23 02:34:43.000000 alphawave-0.3.95/src/alphawave/AlphaWave.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1370 2023-06-10 00:08:35.000000 alphawave-0.3.95/src/alphawave/Colorize.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)      740 2023-06-18 18:50:38.000000 alphawave-0.3.95/src/alphawave/DefaultResponseValidator.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     8205 2023-07-21 01:41:52.000000 alphawave-0.3.95/src/alphawave/JSONResponseValidator.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1173 2023-06-19 22:47:36.000000 alphawave-0.3.95/src/alphawave/MemoryFork.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     6803 2023-07-23 02:16:38.000000 alphawave-0.3.95/src/alphawave/OSClient.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     5920 2023-07-23 02:28:01.000000 alphawave-0.3.95/src/alphawave/OpenAIClient.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     4120 2023-07-16 20:12:02.000000 alphawave-0.3.95/src/alphawave/PythonResponseValidator.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1365 2023-07-10 16:02:12.000000 alphawave-0.3.95/src/alphawave/RepairTestClient.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     3008 2023-06-15 23:14:04.000000 alphawave-0.3.95/src/alphawave/Response.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     6969 2023-07-18 17:07:21.000000 alphawave-0.3.95/src/alphawave/TOMLResponseValidator.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)      800 2023-06-15 04:12:01.000000 alphawave-0.3.95/src/alphawave/TestClient.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1515 2023-06-15 04:12:10.000000 alphawave-0.3.95/src/alphawave/TestClientTest.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)        0 2023-06-06 23:52:12.000000 alphawave-0.3.95/src/alphawave/__init__.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1377 2023-07-11 21:25:58.000000 alphawave-0.3.95/src/alphawave/alphawaveTypes.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     4163 2023-06-04 18:16:08.000000 alphawave-0.3.95/src/alphawave/internalTypes.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)      782 2023-06-07 21:02:29.000000 alphawave-0.3.95/src/alphawave/jsonParser.py
+drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-23 18:04:41.049033 alphawave-0.3.95/src/alphawave.egg-info/
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     9439 2023-07-23 18:04:41.000000 alphawave-0.3.95/src/alphawave.egg-info/PKG-INFO
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     2134 2023-07-23 18:04:41.000000 alphawave-0.3.95/src/alphawave.egg-info/SOURCES.txt
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)        1 2023-07-23 18:04:41.000000 alphawave-0.3.95/src/alphawave.egg-info/dependency_links.txt
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)      199 2023-07-23 18:04:41.000000 alphawave-0.3.95/src/alphawave.egg-info/requires.txt
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)       44 2023-07-23 18:04:41.000000 alphawave-0.3.95/src/alphawave.egg-info/top_level.txt
+drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-23 18:04:41.049033 alphawave-0.3.95/src/alphawave_agents/
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)    17577 2023-07-23 03:33:26.000000 alphawave-0.3.95/src/alphawave_agents/Agent.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1715 2023-07-11 02:39:22.000000 alphawave-0.3.95/src/alphawave_agents/AgentCommandSection.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     7197 2023-07-21 01:51:42.000000 alphawave-0.3.95/src/alphawave_agents/AgentCommandValidator.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1422 2023-07-23 03:31:47.000000 alphawave-0.3.95/src/alphawave_agents/AskCommand.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1871 2023-06-07 03:14:30.000000 alphawave-0.3.95/src/alphawave_agents/CompleteTaskCommand.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1336 2023-06-06 16:52:41.000000 alphawave-0.3.95/src/alphawave_agents/ConfirmAnswerCommand.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1417 2023-07-23 03:32:25.000000 alphawave-0.3.95/src/alphawave_agents/FinalAnswerCommand.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1512 2023-07-23 03:32:00.000000 alphawave-0.3.95/src/alphawave_agents/MathCommand.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     3249 2023-07-12 00:55:02.000000 alphawave-0.3.95/src/alphawave_agents/PromptCommand.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     7932 2023-07-23 03:32:46.000000 alphawave-0.3.95/src/alphawave_agents/SchemaBasedCommand.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     2452 2023-06-09 18:41:37.000000 alphawave-0.3.95/src/alphawave_agents/SentimentAnalysis.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     2149 2023-06-06 16:59:49.000000 alphawave-0.3.95/src/alphawave_agents/SetPropertyCommand.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)        0 2023-06-06 23:52:38.000000 alphawave-0.3.95/src/alphawave_agents/__init__.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1859 2023-07-06 03:51:05.000000 alphawave-0.3.95/src/alphawave_agents/agentTypes.py
+drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-23 18:04:41.053033 alphawave-0.3.95/src/alphawave_pyexts/
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)    11096 2023-06-24 23:27:36.000000 alphawave-0.3.95/src/alphawave_pyexts/FsInference.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     6403 2023-07-23 02:20:11.000000 alphawave-0.3.95/src/alphawave_pyexts/LLMClient.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     2897 2023-07-23 03:22:29.000000 alphawave-0.3.95/src/alphawave_pyexts/SearchCommand.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)    10249 2023-07-20 20:27:59.000000 alphawave-0.3.95/src/alphawave_pyexts/agentChat.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)    10823 2023-07-20 20:44:34.000000 alphawave-0.3.95/src/alphawave_pyexts/chat.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1154 2023-07-20 20:28:15.000000 alphawave-0.3.95/src/alphawave_pyexts/chatglm2.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     2607 2023-06-24 00:18:59.000000 alphawave-0.3.95/src/alphawave_pyexts/configuration_RW.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)    26042 2023-07-23 16:05:09.000000 alphawave-0.3.95/src/alphawave_pyexts/conversation.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)      742 2023-07-20 20:28:29.000000 alphawave-0.3.95/src/alphawave_pyexts/falcon7.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1154 2023-06-24 03:11:55.000000 alphawave-0.3.95/src/alphawave_pyexts/handler.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1094 2023-07-20 20:29:07.000000 alphawave-0.3.95/src/alphawave_pyexts/llama-2-13b-chat.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1387 2023-07-20 20:29:07.000000 alphawave-0.3.95/src/alphawave_pyexts/llama-2-70b-chat.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)      894 2023-07-20 20:29:07.000000 alphawave-0.3.95/src/alphawave_pyexts/llama-2-70b.py
+drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-23 18:04:41.053033 alphawave-0.3.95/src/alphawave_pyexts/llmsearch/
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)    13634 2023-07-23 02:23:28.000000 alphawave-0.3.95/src/alphawave_pyexts/llmsearch/google_search_concurrent.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)      941 2023-07-23 02:25:16.000000 alphawave-0.3.95/src/alphawave_pyexts/llmsearch/search_service.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)    47520 2023-06-24 00:15:02.000000 alphawave-0.3.95/src/alphawave_pyexts/modelling_RW.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)    12724 2023-07-02 15:55:18.000000 alphawave-0.3.95/src/alphawave_pyexts/serverUtils.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     8664 2023-07-23 02:19:51.000000 alphawave-0.3.95/src/alphawave_pyexts/utilityV2.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)      831 2023-07-20 20:29:42.000000 alphawave-0.3.95/src/alphawave_pyexts/vicuna13.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)      813 2023-07-20 20:29:35.000000 alphawave-0.3.95/src/alphawave_pyexts/vicuna7.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)     1121 2023-07-20 20:29:58.000000 alphawave-0.3.95/src/alphawave_pyexts/wvicuna30.py
+drwxrwxr-x   0 bruce     (1000) bruce     (1000)        0 2023-07-23 18:04:41.053033 alphawave-0.3.95/tests/
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)    14779 2023-06-07 17:09:31.000000 alphawave-0.3.95/tests/testOSClient.py
+-rw-rw-r--   0 bruce     (1000) bruce     (1000)    14639 2023-06-18 18:49:14.000000 alphawave-0.3.95/tests/testOpenAiClient.py
```

### Comparing `alphawave-0.3.93/LICENSE` & `alphawave-0.3.95/LICENSE`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/PKG-INFO` & `alphawave-0.3.95/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: alphawave
-Version: 0.3.93
+Version: 0.3.95
 Summary: AlphaWave-py - Functions for smaller Large Language Models (sLLMs)
 Author-email: Steven Ickman <author@example.com>, Bruce DAmbrosio <bruce.dambrosio@gmail.com>
 Project-URL: Homepage, https://tuuyi.io/alphawave
 Project-URL: Bug Tracker, https://github.com/Stevenic/alphawave-py/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `alphawave-0.3.93/README.md` & `alphawave-0.3.95/README.md`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/pyproject.toml` & `alphawave-0.3.95/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "alphawave"
-version = "0.3.93"
+version = "0.3.95"
 authors = [
   { name="Steven Ickman", email="author@example.com" },
   { name="Bruce DAmbrosio", email="bruce.dambrosio@gmail.com" },
 ]
 
 description = "AlphaWave-py - Functions for smaller Large Language Models (sLLMs)"
```

### Comparing `alphawave-0.3.93/src/alphawave/AlphaWave.py` & `alphawave-0.3.95/src/alphawave/AlphaWave.py`

 * *Files 4% similar despite different names*

```diff
@@ -59,43 +59,38 @@
 class AlphaWave(AsyncIOEventEmitter):
     def __init__(self, **kwargs):
         super().__init__()
         self.options = AlphaWaveOptions()
         update_dataclass(self.options, **kwargs)
         #display_dataclass(self.options)
         
-    async def completePrompt(self, input=None):
+    def completePrompt(self, input=None):
         client, prompt, prompt_options, memory, functions, history_variable, input_variable, max_history_messages, max_repair_attempts, tokenizer, validator, logRepairs = get_values(self.options, ('client', 'prompt', 'prompt_options', 'memory', 'functions', 'history_variable', 'input_variable', 'max_history_messages', 'max_repair_attempts', 'tokenizer', 'validator', 'logRepairs'))
 
         if self.options.input_variable:
             if input:
                 memory.set(input_variable, input)
             else:
                 input = memory.get(input_variable) if memory.has(input_variable) else ''
         elif not input:
             input = ''
 
         try:
             self.emit('beforePrompt', memory, functions, tokenizer, prompt, prompt_options)
-            response = await client.completePrompt(memory, functions, tokenizer, prompt, prompt_options)
+            response = client.completePrompt(memory, functions, tokenizer, prompt, prompt_options)
             self.emit('afterPrompt', memory, functions, tokenizer, prompt, prompt_options, response)
             if response['status'] != 'success':
                 return response
 
             if not isinstance(response['message'], dict):
                 response['message'] = {'role': 'assistant', 'content': response['message'] or ''}
 
             self.emit('beforeValidation', memory, functions, tokenizer, response, max_repair_attempts)
-            #print(f'***** Alphawave pre validation')
             validation = validator.validate_response(memory, functions, tokenizer, response, max_repair_attempts)
-            #print(f'***** Alphawave post validation {validation}')
             self.emit('afterValidation', memory, functions, tokenizer, response, max_repair_attempts, validation)
-            #if 'coroutine' in str(type(validation)).lower():
-            #    validation = await validation
-            #print(f'***** Alphawave validation response \n{validation}')
             if validation['valid']:
                 if 'value' in validation:
                     response['message']['content'] = validation['value']
         
                 #print(f'***** Alphawave adding input to history \n{history_variable}')
                 self.addInputToHistory(memory, history_variable, input)
                 self.addResponseToHistory(memory, history_variable, response['message'])
@@ -109,15 +104,15 @@
             #self.addInputToHistory(fork, history_variable, input)
             #self.addResponseToHistory(fork, history_variable, response['message'])
 
             if self.options.logRepairs:
                 print(Colorize.output(response['message']['content']))
 
             self.emit('beforeRepair', fork, functions, tokenizer, response, max_repair_attempts, validation)
-            repair = await self.repairResponse(fork, functions, tokenizer, response, validation, max_repair_attempts)
+            repair = self.repairResponse(fork, functions, tokenizer, response, validation, max_repair_attempts)
             #if 'coroutine' in str(type(repair)).lower():
             #    repair = await repair
             self.emit('afterRepair', fork, functions, tokenizer, response, max_repair_attempts, validation)
 
             if self.options.logRepairs:
                 if repair['status'] == 'success':
                     self.emit('repairSuccess', fork, functions, tokenizer, response, max_repair_attempts, validation)
@@ -152,15 +147,15 @@
                 history.append(message)
             else:
                 history[-1]['content']=message
             if len(history) > self.options.max_history_messages:
                 history = history[int(self.options.max_history_messages/2):]
             memory.set(variable, history)
 
-    async def repairResponse(self, fork, functions, tokenizer, response, validation, remaining_attempts):
+    def repairResponse(self, fork, functions, tokenizer, response, validation, remaining_attempts):
         client, prompt, prompt_options, memory, history_variable, validator, log_repairs = get_values(self.options, ('client', 'prompt', 'prompt_options', 'memory',  'history_variable', 'validator', 'log_repairs'))
 
         # Are we out of attemp ts?
         feedback = validation.get('feedback', 'The response was invalid. Try another strategy.')
         #print(f'remaining_repair {remaining_attempts}')    
         if remaining_attempts <= 0:
             return {
@@ -180,15 +175,15 @@
         ])
 
         # Log the repair
         if self.options.logRepairs:
             print(Colorize.value('feedback', feedback))
 
         # Ask client to complete prompt
-        repair_response = await client.completePrompt(fork, functions, tokenizer, repair_prompt, prompt_options)
+        repair_response = client.completePrompt(fork, functions, tokenizer, repair_prompt, prompt_options)
         if repair_response['status'] != 'success':
             return repair_response
 
         # Ensure response is a message
         if not isinstance(repair_response['message'], dict):
             repair_response['message'] = { 'role': 'assistant', 'content': repair_response.get('message', '') }
 
@@ -201,10 +196,10 @@
             if 'value' in validation:
                 repair_response['message']['content'] = validation['value']
 
             return repair_response
 
         # Try next attempt
         remaining_attempts -= 1
-        return await self.repairResponse(fork, functions, tokenizer, repair_response, validation, remaining_attempts)
+        return self.repairResponse(fork, functions, tokenizer, repair_response, validation, remaining_attempts)
```

### Comparing `alphawave-0.3.93/src/alphawave/Colorize.py` & `alphawave-0.3.95/src/alphawave/Colorize.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave/DefaultResponseValidator.py` & `alphawave-0.3.95/src/alphawave/DefaultResponseValidator.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave/JSONResponseValidator.py` & `alphawave-0.3.95/src/alphawave/JSONResponseValidator.py`

 * *Files 1% similar despite different names*

```diff
@@ -51,14 +51,15 @@
         if not (s.startswith('{') and s.endswith('}')):
             s = '{' + s + '}'
         s = re.sub(r"'([^\"']+)':", r'"\1":', s) # keys as doublequote
         s = s.replace('\\*', '*')
         s = s.replace('\\+', '+')
         s = s.replace('\\-', '-')
         s = s.replace('\\/', '/')
+        s = s.replace('\n', '')
         try:
             s = json.loads(s)
             #print(f'***** JSONReponseValidator parse_dict json.loads success')
             return s
         except json.JSONDecodeError as e:
            pass
```

### Comparing `alphawave-0.3.93/src/alphawave/MemoryFork.py` & `alphawave-0.3.95/src/alphawave/MemoryFork.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave/OSClient.py` & `alphawave-0.3.95/src/alphawave/OSClient.py`

 * *Files 12% similar despite different names*

```diff
@@ -64,15 +64,15 @@
         if self.options.endpoint:
             self.options.endpoint = self.options.endpoint.strip()
             if self.options.endpoint.endswith('/'):
                 self.options.endpoint = self.options.endpoint[:-1]
 
         self._session = requests.Session()
 
-    async def completePrompt(self, memory: PromptMemory, functions: PromptFunctions, tokenizer: Tokenizer, prompt: PromptSection, options: PromptCompletionOptions) -> PromptResponse:
+    def completePrompt(self, memory: PromptMemory, functions: PromptFunctions, tokenizer: Tokenizer, prompt: PromptSection, options: PromptCompletionOptions) -> PromptResponse:
         if isinstance(options, dict):
             argoptions = options
             options = PromptCompletionOptions(completion_type = argoptions['completion_type'],
                                               model = argoptions['model'],
                                               max_input_tokens = argoptions['max_input_tokens'],
                                               temperature = argoptions['temperature'],
                                               top_p = argoptions['top_p'],
@@ -94,16 +94,18 @@
             print(Colorize.title('CHAT PROMPT:'))
             for msg in result.output:
                 if not isinstance(msg, dict):
                     print(Colorize.output(msg))
                     msg = msg.__dict__
                 print(Colorize.output(json.dumps(msg, indent=2)), end='')
             print()
+
         request = self.copyOptionsToRequest(CreateChatCompletionRequest(model = options.model, messages =  result.output), options, ['max_tokens', 'temperature', 'top_p', 'n', 'stream', 'logprobs', 'echo', 'stop', 'presence_penalty', 'frequency_penalty', 'best_of', 'logit_bias', 'user'])
-        response = await self.createChatCompletion(request)
+
+        response = self.createChatCompletion(request)
         if self.options.logRequests:
             print(Colorize.title('CHAT RESPONSE:'))
             print(Colorize.value('status', response.status))
             print(Colorize.value('duration', time.time() - startTime, 'ms'))
             print(Colorize.output(response.message))
         
         if response.status == 'success':
@@ -119,30 +121,23 @@
 
     def copyOptionsToRequest(self, target: Dict[str, Any], src: Any, fields: list) -> Dict[str, Any]:
         for field in fields:
             if hasattr(src, field) and getattr(src, field) is not None:
                 setattr(target,field, getattr(src,field))
         return target
 
-    async def createCompletion(self, request: CreateCompletionRequest) -> requests.Response:
-        url = f"{self.options.endpoint or self.DefaultEndpoint}/v1/completions"
-        return await self.post(url, request)
-
-    async def createChatCompletion(self, request: CreateChatCompletionRequest) -> requests.Response:
+    def createChatCompletion(self, request: CreateChatCompletionRequest) -> requests.Response:
         url = f"{self.options.endpoint or self.DefaultEndpoint}/v1/chat/completions"
-        return await self.post(url, request)
-
-    async def post(self, url: str, request: object) -> requests.Response:
         requestHeaders = {
             'Content-Type': 'application/json',
             'User-Agent': self.UserAgent
         }
         result = ''
         try:
-            result = await ut.ask_LLM(request.model,
+            result = ut.ask_LLM(request.model,
                                 request.messages,
                                 request.max_tokens,
                                 request.temperature,
                                 request.top_p,
                                 self.options.endpoint,
                                 self.options.port
                                 )
```

### Comparing `alphawave-0.3.93/src/alphawave/OpenAIClient.py` & `alphawave-0.3.95/src/alphawave/OpenAIClient.py`

 * *Files 0% similar despite different names*

```diff
@@ -37,15 +37,15 @@
         self.options.update(kwargs)
         if not self.options['apiKey']:
             print("Client created without an 'apiKey'.")
             raise ValueError
 
         self._session = requests.Session()
 
-    async def completePrompt(self, memory: PromptMemory, functions: PromptFunctions, tokenizer: Tokenizer, prompt: PromptSection, options: PromptCompletionOptions) -> PromptResponse:
+    def completePrompt(self, memory: PromptMemory, functions: PromptFunctions, tokenizer: Tokenizer, prompt: PromptSection, options: PromptCompletionOptions) -> PromptResponse:
         startTime = time.time()
         max_input_tokens = 1024
 
         #
         ### form prompt messages
         #
         if isinstance(options, dict):
```

### Comparing `alphawave-0.3.93/src/alphawave/PythonResponseValidator.py` & `alphawave-0.3.95/src/alphawave/PythonResponseValidator.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave/RepairTestClient.py` & `alphawave-0.3.95/src/alphawave/RepairTestClient.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave/Response.py` & `alphawave-0.3.95/src/alphawave/Response.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave/TOMLResponseValidator.py` & `alphawave-0.3.95/src/alphawave/TOMLResponseValidator.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave/TestClient.py` & `alphawave-0.3.95/src/alphawave/TestClient.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave/TestClientTest.py` & `alphawave-0.3.95/src/alphawave/TestClientTest.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave/alphawaveTypes.py` & `alphawave-0.3.95/src/alphawave/alphawaveTypes.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave/internalTypes.py` & `alphawave-0.3.95/src/alphawave/internalTypes.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave/jsonParser.py` & `alphawave-0.3.95/src/alphawave/jsonParser.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave.egg-info/PKG-INFO` & `alphawave-0.3.95/src/alphawave.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: alphawave
-Version: 0.3.93
+Version: 0.3.95
 Summary: AlphaWave-py - Functions for smaller Large Language Models (sLLMs)
 Author-email: Steven Ickman <author@example.com>, Bruce DAmbrosio <bruce.dambrosio@gmail.com>
 Project-URL: Homepage, https://tuuyi.io/alphawave
 Project-URL: Bug Tracker, https://github.com/Stevenic/alphawave-py/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `alphawave-0.3.93/src/alphawave.egg-info/SOURCES.txt` & `alphawave-0.3.95/src/alphawave.egg-info/SOURCES.txt`

 * *Files 8% similar despite different names*

```diff
@@ -36,18 +36,27 @@
 src/alphawave_agents/SentimentAnalysis.py
 src/alphawave_agents/SetPropertyCommand.py
 src/alphawave_agents/__init__.py
 src/alphawave_agents/agentTypes.py
 src/alphawave_pyexts/FsInference.py
 src/alphawave_pyexts/LLMClient.py
 src/alphawave_pyexts/SearchCommand.py
+src/alphawave_pyexts/agentChat.py
 src/alphawave_pyexts/chat.py
+src/alphawave_pyexts/chatglm2.py
 src/alphawave_pyexts/configuration_RW.py
 src/alphawave_pyexts/conversation.py
+src/alphawave_pyexts/falcon7.py
 src/alphawave_pyexts/handler.py
+src/alphawave_pyexts/llama-2-13b-chat.py
+src/alphawave_pyexts/llama-2-70b-chat.py
+src/alphawave_pyexts/llama-2-70b.py
 src/alphawave_pyexts/modelling_RW.py
 src/alphawave_pyexts/serverUtils.py
 src/alphawave_pyexts/utilityV2.py
+src/alphawave_pyexts/vicuna13.py
+src/alphawave_pyexts/vicuna7.py
+src/alphawave_pyexts/wvicuna30.py
 src/alphawave_pyexts/llmsearch/google_search_concurrent.py
 src/alphawave_pyexts/llmsearch/search_service.py
 tests/testOSClient.py
 tests/testOpenAiClient.py
```

### Comparing `alphawave-0.3.93/src/alphawave_agents/Agent.py` & `alphawave-0.3.95/src/alphawave_agents/Agent.py`

 * *Files 2% similar despite different names*

```diff
@@ -92,38 +92,32 @@
 def update_dataclass(instance, source):
     for key, value in source.items():
         if key in instance and value is not None:
             instance[key] =  value
 
 ##
 PromptInstructionSectionJSON = TemplateSection(\
-"""
-Reason step-by-step about the user task.
-If the task can be completed from known fact, reasoning, or has been completed earlier, respond immediately. 
-Otherwise, develop a concise plan for completing the task. Base your plan on known fact, reasoning, prior results, and the available commands.
-2. Select the first step of that plan as the next command to perform. 
-3. Respond with:
-  - your reasoning 
-  - the JSONformat shown above for that next command, instantiating actual inputs where indicated
+"""You are a helpful, friendly, obedient AI.
+If a question or task can be answer from known fact or reasoning respond and STOP. 
+Otherwise, select a command to perform, and respond using the command format provided.
+You should choose to respond directly. Remember, though, you are more than just an AI, since you have commands available.
 """, 'system')
+
 PromptOneShotJSON = [
     UserMessage("What is 35 * 64?"),
     AssistantMessage("""I will use the math command.
 {"command": "math", "inputs":{"code":"35*64"}}""")]
 
 
 PromptInstructionSectionTOML = TemplateSection(\
-"""
-Reason step-by-step about the user task:
-1. Develop a concise plan for finding an answer and showing it to the user. Base your plan on known fact, reasoning, and the available commands.
-2. Select the first step of that plan as the next command to perform. 
-3. Respond with:
-  - your reasoning 
-  - the JSONformat shown above for that next command, substituting your inputs where indicated
-""", 'system')
+"""You are a helpful AI.
+If a question or task can be completed from known fact, reasoning, or has been completed, respond immediately. 
+Otherwise, develop a concise plan for completing the task. Base your plan on known fact, reasoning, prior results, and the available commands.
+Select the first step of that plan as the next command to perform, and respond with the command format provided to invoke the command.
+""",'system')
 
 PromptOneShotTOML = [
     UserMessage("What is 35 * 64?"),
     AssistantMessage("""I will use the math command.
 [RESPONSE]
 command = "math"
 inputs.code = "35*64"
@@ -207,15 +201,15 @@
 
     def getCommand(self, title: str):
         return self._commands.get(title)
 
     def hasCommand(self, title: str):
         return title in self._commands
 
-    async def completeTask(self, input: Optional[str] = None, agentId: Optional[str] = None, executeInitialThought: bool = False):
+    def completeTask(self, input: Optional[str] = None, agentId: Optional[str] = None, executeInitialThought: bool = False):
       try:
         # Initialize the input to the next step
         stepInput = input if input is not None else self.memory.get(self.options['input_variable'])
         if self.top_level_task is None:
             self.top_level_task = stepInput
 
         # Dispatch to child agent if needed
@@ -225,15 +219,15 @@
         while step < self.options['max_steps']:
             # Wait for step delay to prevent gpt overrun
             if step > 0 and self._options['step_delay'] > 0:
                 sys.stdout.flush()
                 time.sleep(self._options['step_delay']/100) # assumes step delay is in seconds
             # Execute next step
             #print(f'***** Agent completeTask calling execute_next_step {stepInput}')
-            result, ran_command = await self.execute_next_step(stepInput, agentId)
+            result, ran_command = self.execute_next_step(stepInput, agentId)
             #print(f'***** Agent completeTask return from execute_next_step {ran_command}, {result}')
             if ran_command:
                 # check for command in response from command
                 # Create command validator
                 #validator = AgentCommandValidator(self._commands, self._options['client'], self._options['prompt_options'].model,
                 #                                  self._options['syntax'], memory=self.memory, history_variable=history_variable)
                 # just a stub, need to finish if good idea
@@ -264,45 +258,49 @@
         key = f"{self.options['agent_variable']}-{agentId}" if agentId else self.options['agent_variable']
         self.memory.set(key, state)
 
     def get_agent_history_variable(self, agentId: Optional[str] = None):
         return f"{self._options['history_variable']}-{agentId}" if agentId else self._options['history_variable']
 
 
-    async def execute_next_step(self, input: Optional[str] = None, agent_id: Optional[str] = None, execute_initial_thought: bool = False):
+    def execute_next_step(self, input: Optional[str] = None, agent_id: Optional[str] = None, execute_initial_thought: bool = False):
         try:
             #print(f'***** Agent execute_next_step input {input}')
             state = self.get_agent_state(agent_id)
             # Create agents prompt section
+            agent_prompt = []
             if isinstance(self._options['prompt'], list):
                 agent_prompt = TemplateSection('\n'.join(self._options['prompt']), 'system')
+                sections = [agent_prompt]
             elif isinstance(self._options['prompt'], dict):
                 agent_prompt = self._options['prompt']
-            else:
+                sections = [agent_prompt]
+            elif isinstance(self._options['prompt'], str):
                 agent_prompt = TemplateSection(self._options['prompt'], 'system')
+                sections = [agent_prompt]
             
+                
             # Ensure the context variable is set
             if 'context' in state:
                 self.memory.set(self.options['context_variable'], state['context'])
 
             # Create prompt
             history_variable = self.get_agent_history_variable(agent_id)
             try:
-                sections = [agent_prompt]
                 sections.append(AgentCommandSection(self._commands, one_shot=True, syntax=self._options['syntax']))
                 
                 if self._options['syntax'] == 'JSON':
                     pis = PromptInstructionSectionJSON
                     pos = PromptOneShotJSON
                 else:
                     pis = PromptInstructionSectionTOML
                     pos = PromptOneShotTOML
                     
                 sections.append(pis)
-                sections.extend(pos)
+                #sections.extend(pos)
                 prompt = Prompt([
                     GroupSection(sections, 'system'),
                     ConversationHistory(history_variable, 1.0, True)
                 ])
                 if input:
                     #print(f'***** Agent append Text Section {input}')
                     prompt.sections.append(TextSection(input, 'user', -1, True, '\n', 'user'))
@@ -345,15 +343,15 @@
                     logRepairs = self._options['logRepairs'],
                     validator = validator
                 )
 
                 # Complete the prompt
                 max_attempts = 2 if self._options['retry_invalid_responses'] else 1
                 for attempt in range(max_attempts):
-                    response = await wave.completePrompt()
+                    response = wave.completePrompt()
                     
                     if response['status'] != 'invalid_response':
                         break
 
                 # Ensure response succeeded
                 # Note at this point AgentCommandValidator has approved response
                 if response['status'] != 'success':
@@ -372,15 +370,15 @@
                 #print(f'***** Agent execute_next_step returning no next command')
                 return thought, False  # False means don't keep going, no command to run
             self._events.emit('newThought', thought)
             #print(f'***** Agent execute_next_step calling execute_command state {state}, thought {thought}')
 
             command_name = thought['command']
             command_input = str(thought['inputs'] or '')
-            result = await self.execute_command(state, thought)
+            result = self.execute_command(state, thought)
             #print(f'command_result \n{result}\n')
             # Check for task result and error
             task_response = result if isinstance(result, dict) and result.get('type') == 'TaskResponse' else None
             if task_response:
                 if task_response['status'] in ['error', 'invalid_response', 'rate_limited', 'too_many_steps', 'too_long']:
                     #print(f'***** Agent execute_next_step fail {task_response}')
                     return task_response, False
@@ -403,20 +401,18 @@
             traceback.print_exc()
             return {
                 'type': "TaskResponse",
                 'status': "error",
                 'message': str(err)
             }, False
 
-    async def execute_command(self, state: AgentState, thought: AgentThought):
+    def execute_command(self, state: AgentState, thought: AgentThought):
         # a command to execute
         command_name = thought['command']
         command = self._commands.get(command_name, None) or {}
         input = thought['inputs'] or {}
         # Execute command and return result
         #print(f'***** Agent execute_command  {command_name}, {input}')
-        response = await command.execute(input, self.memory, self.functions, self.tokenizer)
-        if 'coroutine' in str(type(response)).lower():
-            return await response
+        response = command.execute(input, self.memory, self.functions, self.tokenizer)
         #print(f'***** Agent execute_command {command_name}\n{response}\n')
         return response
```

### Comparing `alphawave-0.3.93/src/alphawave_agents/AgentCommandSection.py` & `alphawave-0.3.95/src/alphawave_agents/AgentCommandSection.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_agents/AgentCommandValidator.py` & `alphawave-0.3.95/src/alphawave_agents/AgentCommandValidator.py`

 * *Files 8% similar despite different names*

```diff
@@ -38,43 +38,45 @@
 
         self._commands = commands
 
     def validate_response(self, memory, functions, tokenizer, response, remaining_attempts) -> Union[AgentThought, None]:
         try:
           #print(f"***** AgentCommandValidator validate syntax: \n{self._syntax}\nresponse\n{response}")
           message = response['message']
-          raw_text = message if isinstance(message, str) else message.get('content', '')
+          raw_text = message if isinstance(message, str) else message.get('content', '').replace('\n','')
           if (self._syntax == 'JSON' and '{"command":' not in raw_text) or (self._syntax == 'TOML' and 'response' not in raw_text.lower()):
               # means no form found, assume llm doesn't need to use a command
+              #print(f"***** AgentCommandValidator no command found")
               return {
                   'type': 'Validation',
                   'valid': True,
                   'value': raw_text,
                   'feedback': 'no command'
               }
           
           # Validate that the response contains a thought
           validation_result = self._input_validator.validate_response(memory, functions, tokenizer, response, remaining_attempts)
           if not validation_result['valid']:
-            return validation_result
+              #print(f'*****AgentCommandValidator validate failed {validation_result}')
+              return validation_result
 
           # Validate that the command exists
           thought = validation_result['value']
           #print(f'*****AgentCommandValidator post validate thought  \n{thought}\n')
           if not('command' in thought) or not('inputs' in thought):
-              print(f"***** AgentCommandValidator command or inputs not found")
+              #print(f"***** AgentCommandValidator command or inputs not found")
               return {
                   'type': 'Validation',
                   'valid': False,
                   'feedback': f'command not found or invalid, or inputs missing. The commands you have are {list(self._commands.keys())}'
               }
 
           command_name = thought['command']
           if command_name not in self._commands:
-              print(f"***** AgentCommandValidator no such command {command_name}")
+              #print(f"***** AgentCommandValidator no such command {command_name}")
               return {
                   'type': 'Validation',
                   'valid': False,
                   'feedback': f'The command {command_name} does not exist. The only commands you have are {list(self._commands.keys())}'
               }
           
           # Validate that the command input is valid
```

### Comparing `alphawave-0.3.93/src/alphawave_agents/AskCommand.py` & `alphawave-0.3.95/src/alphawave_agents/AskCommand.py`

 * *Files 3% similar despite different names*

```diff
@@ -35,9 +35,9 @@
         self.question = question
 
 class AskCommand(SchemaBasedCommand):
     def __init__(self, title: Optional[str] = '', description: Optional[str] = ''):
         global schema
         super().__init__(schema, title, description)
 
-    async def execute(self, input: AskCommandInput, memory: PromptMemory, functions: PromptFunctions, tokenizer: Tokenizer) -> TaskResponse:
+    def execute(self, input: AskCommandInput, memory: PromptMemory, functions: PromptFunctions, tokenizer: Tokenizer) -> TaskResponse:
         return asdict(TaskResponse(status="input_needed",message=input['question']))
```

### Comparing `alphawave-0.3.93/src/alphawave_agents/CompleteTaskCommand.py` & `alphawave-0.3.95/src/alphawave_agents/CompleteTaskCommand.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_agents/ConfirmAnswerCommand.py` & `alphawave-0.3.95/src/alphawave_agents/ConfirmAnswerCommand.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_agents/FinalAnswerCommand.py` & `alphawave-0.3.95/src/alphawave_agents/FinalAnswerCommand.py`

 * *Files 7% similar despite different names*

```diff
@@ -25,11 +25,11 @@
 class FinalAnswerCommandInput:
     answer:str
 
 class FinalAnswerCommand(SchemaBasedCommand):
     def __init__(self, title: Optional[str] = None, description: Optional[str] = None):
         super().__init__(CommandSchema(), title, description)
 
-    async def execute(self, input: FinalAnswerCommandInput, memory: PromptMemory, functions: PromptFunctions, tokenizer: Tokenizer) -> TaskResponse:
+    def execute(self, input: FinalAnswerCommandInput, memory: PromptMemory, functions: PromptFunctions, tokenizer: Tokenizer) -> TaskResponse:
         print(f'\nAnswer: \n{input}\n')
         return_msg = {"type": "TaskResponse", "status": "input_needed", "message": input['answer'] }
         return return_msg
```

### Comparing `alphawave-0.3.93/src/alphawave_agents/MathCommand.py` & `alphawave-0.3.95/src/alphawave_agents/MathCommand.py`

 * *Files 1% similar despite different names*

```diff
@@ -33,15 +33,15 @@
 )
 
 class MathCommand(SchemaBasedCommand):
 
     def __init__(self, title = None, description = None):
         super().__init__(schema, title, description)
 
-    async def execute(self, input: MathCommandInput, memory: Any, functions: Any, tokenizer: Any) -> Any:
+    def execute(self, input: MathCommandInput, memory: Any, functions: Any, tokenizer: Any) -> Any:
         try:
             exp = input['code']
             exp = exp.replace('\\*', '*')
             exp = exp.replace('\\+', '+')
             exp = exp.replace('\\-', '-')
             exp = exp.replace('\\/', '/')
             return eval(exp)
```

### Comparing `alphawave-0.3.93/src/alphawave_agents/PromptCommand.py` & `alphawave-0.3.95/src/alphawave_agents/PromptCommand.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_agents/SchemaBasedCommand.py` & `alphawave-0.3.95/src/alphawave_agents/SchemaBasedCommand.py`

 * *Files 0% similar despite different names*

```diff
@@ -47,15 +47,15 @@
     def schema(self) -> CommandSchema:
         return self._schema
 
     @property
     def title(self) -> str:
         return self._title or self._schema['title']
 
-    async def execute(self, inputs: Dict[str, Any], memory: 'PromptMemory', functions: 'PromptFunctions', tokenizer: 'Tokenizer') -> Any:
+    def execute(self, inputs: Dict[str, Any], memory: 'PromptMemory', functions: 'PromptFunctions', tokenizer: 'Tokenizer') -> Any:
         raise NotImplementedError
 
     def validate(self, inputs: Dict[str, Any], memory: 'PromptMemory', functions: 'PromptFunctions', tokenizer: 'Tokenizer', syntax: str ='JSON') -> 'Validation':
         #print(f'***** SchemaBasedCommand validate inputs {inputs}\nschema\n{self._schema}')
         if self._schema is None:
             return {
                 'type': 'Validation',
```

### Comparing `alphawave-0.3.93/src/alphawave_agents/SentimentAnalysis.py` & `alphawave-0.3.95/src/alphawave_agents/SentimentAnalysis.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_agents/SetPropertyCommand.py` & `alphawave-0.3.95/src/alphawave_agents/SetPropertyCommand.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_agents/agentTypes.py` & `alphawave-0.3.95/src/alphawave_agents/agentTypes.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/FsInference.py` & `alphawave-0.3.95/src/alphawave_pyexts/FsInference.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/LLMClient.py` & `alphawave-0.3.95/src/alphawave_pyexts/LLMClient.py`

 * *Files 0% similar despite different names*

```diff
@@ -17,15 +17,15 @@
 host='192.168.1.195'
 port = 5004
 
 
 def get_available_models():
     return list(cv.conv_templates.keys())
 
-async def run_query(model, messages, max_tokens, temp, top_p, host = host, port = port, tkroot = None, tkdisplay=None, format=True): 
+def run_query(model, messages, max_tokens, temp, top_p, host = host, port = port, tkroot = None, tkdisplay=None, format=True): 
     global USER_PREFIX, ASSISTANT_PREFIX, SYSTEM_PREFIX
 
     conv=cv.get_conv_template(model)
     user_prompt = conv.roles[0]
     asst_prompt = conv.roles[1]
     system_prompt = conv.roles[1]
```

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/SearchCommand.py` & `alphawave-0.3.95/src/alphawave_pyexts/SearchCommand.py`

 * *Files 3% similar despite different names*

```diff
@@ -41,20 +41,21 @@
         super().__init__(search_schema, title, description)
         self.client = client
         self.model = model
         self.return_urls = return_urls
         self.max_chars = max_chars
         self.logResponse = logResponse
         
-    async def execute(self, input: input, memory: Any, functions: Any, tokenizer: Any) -> Any:
+    def execute(self, input: input, memory: Any, functions: Any, tokenizer: Any) -> Any:
         try:
+            print(f' starting web search {input}')
             if type(input) == dict and 'query' in input:
                 query = input['query']
                 memory = VolatileMemory()  # don't let anything bleed back to surrounding task
-                response = await search_service.run_chat(self.client, query, self.model, memory, functions, tokenizer, self.max_chars)
+                response = search_service.run_chat(self.client, query, self.model, memory, functions, tokenizer, self.max_chars)
                 sc_text = ''
                 sc_urls = []
                 if type(response) is list:
                     for item in response:
                         if type(item) == dict and 'url' in item:
                             sc_urls.append('\n'+item['url'])
                         if type(item) == dict and 'text' in item:
```

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/chat.py` & `alphawave-0.3.95/src/alphawave_pyexts/chat.py`

 * *Files 10% similar despite different names*

```diff
@@ -22,41 +22,32 @@
 ASSISTANT_PREFIX = 'Assistant'
 STOP_1 = '</s>'
 STOP_2 = USER_PREFIX
 FORMAT=True
 
 prompt_text = 'You are helpful, creative, clever, and very friendly. '
 PROMPT = Prompt([
-    UserMessage(prompt_text),
+    SystemMessage(prompt_text),
     ConversationHistory('history', .5),
     UserMessage('{{$input}}')
 ])
 
+#print(f' models: {llm.get_available_models()}')
 parser = argparse.ArgumentParser()
-parser.add_argument('model', type=str, default='wizardLM', choices=['wizardLM', 'zero_shot', 'vicuna_v1.1', 'dolly', 'oasst_pythoa', 'stablelm', 'baize', 'rwkv', 'openbuddy', 'phoenix', 'claude', 'mpt', 'bard', 'billa', 'h2ogpt', 'snoozy', 'manticore', 'falcon_instruct', 'falcon_instruct2', 'falcon_instruct3', 'gpt_35', 'gpt_4'],help='select prompting based on modelto load')
-parser.add_argument('--user', type=str, default='', help='user prefix, overrides model template')
-parser.add_argument('--asst', type=str, default='', help='assistant prefix, overrides model template')
-parser.add_argument('--stop1', type=str, default='',help='stop string')
-parser.add_argument('--stop2', type=str, default='', help='alternative stop string')
-args = parser.parse_args()
-if args.user:
-    USER_PREFIX = args.user
-    STOP_2 = args.user
-if args.asst:
-    ASSISTANT_PREFIX = args.asst
-if args.stop1:
-    STOP_1 = args.stop1
-if args.stop2:
-    STOP_2 = args.stop2
-if args.model:
-    model = args.model
-else:
-    model = 'wizardLM'
-
+#parser.add_argument('model', type=str, default='wizardLM', choices=['guanaco', 'wizardLM', 'zero_shot', 'vicuna_v1.1', 'dolly', 'oasst_pythia', 'stablelm', 'baize', 'rwkv', 'openbuddy', 'phoenix', 'claude', 'mpt', 'bard', 'billa', 'h2ogpt', 'snoozy', 'manticore', 'falcon_instruct', 'gpt_35', 'gpt_4'],help='select prompting based on modelto load')
 
+model = ''
+modelin = input('model name? ').strip()
+if modelin is not None and len(modelin)>1:
+    model = modelin.strip()
+    models = llm.get_available_models()
+    while model not in models:
+        print(models)
+        modelin = input('model name? ').strip()
+        model=modelin
 
 def show_prompt():
     pass
 
 def set_model():
     pass
 
@@ -78,47 +69,51 @@
     except Exception as e:
         print ("parse failed", e)
 
 PREV_LEN = 0
 def submit():
     global PREV_LEN
     input_text = input_area.get("1.0", tk.END)
-    if len(input_text) > PREV_LEN:
-        new_text = input_text[PREV_LEN:]
+    if FORMAT and len(input_text) > PREV_LEN:
+        new_text = input_text[PREV_LEN:].strip()
+    else:
+        new_text = input_text.strip()
     input_area.insert(tk.END, '\n')
     response = run_query(new_text)
-    PREV_LEN=len(input_text)
+    input_area.insert(tk.END, '\n')
+    PREV_LEN=len(input_area.get("1.0", tk.END))-1
+    return(input, response)
 
 def setFormat():
     global FORMAT
     if FORMAT:
         format_button.config(text='RAW')
         FORMAT=False
     else:
         format_button.config(text='FORMAT')
         FORMAT=True
 
 
 def setPrompt():
     global PROMPT
     input_text = input_area.get("1.0", tk.END)
+    input_text = input_text.strip()
     if input_text.startswith("NoPrompt"):
         input_text = ''
     if input_text.startswith("Helpfull"):
-        input_text = 'Response as a helpful, friendly, information assistant. Say "I don\'t know" if you have no information"'
+        input_text = 'Respond as a helpful, friendly, information assistant. Say "I don\'t know" if you have no information"'
     if input_text.startswith("Bhagaven"):
         input_text = 'Respond as a compassionate, empathetic, self-realized follower of Ramana Maharshi'
     if input_text.startswith("ACT"):
         input_text = 'Respond as a compassionate, empathetic, counselor familiar with Acceptance Commitment Theray'
     if input_text.startswith("Flirt"):
-        input_text = 'Respond as a friendly,\ chatty, flirty young woman named Samantha. You are 21 years old.'
+        input_text = 'Respond as a friendly, chatty, flirty young woman named Samantha.'
     if input_text.startswith("Agent"):
         input_text =\
-            """
-Define steps as:
+            """Define steps as:
 orient: identify the task
 thought: think step by step about the task. Identify ambiguities or logical consequences in the problem statement that impact your response to the task.
 action: act to further progress on the task. Your available acts are:
 i. answer: if the answer is available, respond with answer then respond STOP
 ii. logic: use known fact or logical reasoning based on known fact to expand on thought, then respond with reasoning.
 iii. ask: ask user a question to clarify the task. Display: question, Display: STOP
 iv. search: use the llmsearch plugin to search the web for question based on thought
@@ -144,16 +139,16 @@
     global memory, PREV_POS
     PREV_POS="1.0"
     input_area.delete("1.0", tk.END)
     memory.set('history', [])
 
 root = tk.Tk()
 
-root.title(args.model)
-root.geometry("1260x1024")
+root.title(model)
+root.geometry("1440x1260")
 #root.config(cursor="watch")
 root.rowconfigure(0, weight=1)
 root.columnconfigure(0, weight=1)
 
 textFrame = tk.Frame(root, bg="#010101")
 controlFrame = tk.Frame(root, bg="#101010")#, width=2)
 textFrame.grid(row=0, column=0, sticky="nsew")
@@ -178,26 +173,25 @@
 # Set the font of the dropdown list
 style.configure("TCombobox", selectbackground='gray', fieldbackground='black', background='light gray')
 style.map('TCombobox', fieldbackground=[('readonly','grey')])
 style.configure("TCombobox", font=('Arial', 12))  # sets the font in the entry part
 style.configure("TCombobox.Listbox", font=('Arial', 12), background='grey')  # sets the font in the dropdown list part
 
 
-
-input_area = tk.Text(textFrame, height=80,bg='black', fg='white', font=("Arial", 11))
+input_area = tk.Text(textFrame, height=80,bg='#101820', fg='AntiqueWhite1', font=("Bitstream Charter", 11), wrap=tk.WORD)
 input_area.grid(row=0, column=0, sticky='nsew')
 input_area.pack(expand=True)
 submit_button = tk.Button(controlFrame,  text="Submit", command=submit, font=("Arial", 12), bg='grey')
 submit_button.pack(side='top', fill='x')
 
 clear_button = tk.Button(controlFrame,  text="Clear", command=clear, font=("Arial",12), bg='grey')
 clear_button.pack(side='top', fill='x')
 
 temperature = tk.StringVar()
-temperature.set('.7')
+temperature.set('.1')
 temperature.trace("w", on_value_change)
 temp_label = ttk.Label(controlFrame, text="Temperature", style='TLabel')
 temp_label.pack(side='top', fill='x')
 temp_button = ttk.Combobox(controlFrame, textvariable=temperature, values = [.01,.1,.2,.4,.5,.7,.9,1.0], style='TCombobox')
 temp_button.pack(side='top', fill='x')
 
 top_p = tk.StringVar()
@@ -227,82 +221,59 @@
 root.columnconfigure(0, weight=1)
 
 functions = FunctionRegistry()
 tokenizer = GPT3Tokenizer()
 memory = VolatileMemory({'input':'', 'history':[]})
 max_tokens = 2000
 # Render the prompt for a Text Completion call
-async def render_text_completion():
-    print(f"\n***** chat memory pre render \n{memory.get('history')}\n")
-    as_text = await PROMPT.renderAsText(memory, functions, tokenizer, max_tokens)
-    print(as_text)
+def render_text_completion():
+    #print(f"\n***** chat memory pre render \n{memory.get('history')}\n")
+    as_text = PROMPT.renderAsText(memory, functions, tokenizer, max_tokens)
+    #print(as_text)
     text = ''
     if not as_text.tooLong:
         text = as_text.output
     return text
 
 # Render the prompt for a Text Completion call
-async def render_messages_completion():
-    print(f"\n***** chat memory pre render input: \n{memory.get('input')}")
-    print(f"***** chat memory pre render \n{memory.get('history')}\n")
-    as_msgs = await PROMPT.renderAsMessages(memory, functions, tokenizer, max_tokens)
+def render_messages_completion():
+    #print(f"\n***** chat memory pre render input: \n{memory.get('input')}")
+    #print(f"***** chat memory pre render \n{memory.get('history')}\n")
+    as_msgs = PROMPT.renderAsMessages(memory, functions, tokenizer, max_tokens)
     msgs = []
     if not as_msgs.tooLong:
         msgs = as_msgs.output
     return msgs
 
 
 host = '127.0.0.1'
 port = 5004
 
 def run_query(query):
     global model, temperature, top_p, max_tkns, memory
     try:
         memory.set('input', query)
         if FORMAT:
-            msgs = asyncio.run(render_messages_completion())
-            for msg in msgs:
-                print(str(msg))
-            response = ut.ask_LLM(model, msgs, int(max_tkns.get()), float(temperature.get()), float(top_p.get()), host, port, root, input_area)
+            msgs = render_messages_completion()
+            #for msg in msgs:
+            #    print(str(msg))
+            response = asyncio.run(ut.ask_LLM(model, msgs, int(max_tkns.get()), float(temperature.get()), float(top_p.get()), host, port, root, input_area))
             #print(response)
             history = memory.get('history')
-            history.append({'role':llm.USER_PREFIX, 'content': query})
-            history.append({'role': llm.ASSISTANT_PREFIX, 'content': response})
+            #print(f'***** chat post query user {llm.USER_PREFIX}, {llm.ASSISTANT_PREFIX}')
+            #query = query.replace(llm.ASSISTANT_PREFIX+':', '')
+            #query = query.replace(llm.ASSISTANT_PREFIX, '')
+            #print(f'***** chat post query query {query}')
+            history.append({'role':llm.USER_PREFIX, 'content': query.strip()})
+            response = response.replace(llm.ASSISTANT_PREFIX+':', '')
+            response = response.replace(llm.ASSISTANT_PREFIX, '')
+            #print(f'response asst_prefix {llm.ASSISTANT_PREFIX}, response post-removal{response}')
+            #print(f'***** chat post query response {response}')
+            history.append({'role': llm.ASSISTANT_PREFIX, 'content': response.strip()})
             memory.set('history', history)
         else:
             # just send the raw input text to server
-            llm.run_query(model, query, int(max_tkns.get()), float(temperature.get()), float(top_p.get()), host, port, root, input_area, format=False)
+            asyncio.run(llm.run_query(model, query, int(max_tkns.get()), float(temperature.get()), float(top_p.get()), host, port, root, input_area, format=False))
     except Exception:
         traceback.print_exc()
         
-if args.user is not None:
-    USER_PREFIX = args.user
-    STOP_2=args.user
-if args.asst is not None:
-    ASSISTANT_PREFIX = args.asst
-if args.stop1 is not None:
-    STOP_1 = args.stop1
-if args.stop2 is not None:
-    STOP_2 = args.stop2
-if args.model is not None:
-    model = args.model
-else:
-    model = 'wizardLM-30B'
-
-
-
-
 root.mainloop()
-
-"""
-Find an arithmetic expression over the integers 2, 3, and 6 that evaluates to 12. You must use each integer exactly once. Use the following approach. Create a trial expression. Evaluate the results. If it is false, build hypothesis for generating a better expression, then generate a new trial expression and evaluate again. Do this until the correct result is found. If the result is 12 then the process is over.
-"""
-
-"""
-Human: you are an instruction-following AI. Follow these instructions: Find an arithmetic expression over the integers 2, 3, and 6 that evaluates to 12. You must use each integer exactly once. Use the following approach.
-Loop:
-  Generate a trial expression using previously generated hypotheses, if any
-  Evaluate the trial expression. 
-  Test if the evaluation equals 12?
-  If not, build a hypothesis to obtain higher success rate in expression generation.
-Untill Test is True.
-"""
```

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/configuration_RW.py` & `alphawave-0.3.95/src/alphawave_pyexts/configuration_RW.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/conversation.py` & `alphawave-0.3.95/src/alphawave_pyexts/conversation.py`

 * *Files 1% similar despite different names*

```diff
@@ -506,14 +506,40 @@
         messages=(),
         offset=0,
         sep_style=SeparatorStyle.NO_COLON_SINGLE,
         sep=None,
     )
 )
 
+# ChatGPT default template
+register_conv_template(
+    Conversation(
+        name="gpt-3.5-turbo-16k",
+        system="",
+        roles=("user", "assistant"),
+        messages=(),
+        offset=0,
+        sep_style=SeparatorStyle.NO_COLON_SINGLE,
+        sep=None,
+    )
+)
+
+# ChatGPT default template
+register_conv_template(
+    Conversation(
+        name="gpt-4",
+        system="",
+        roles=("user", "assistant"),
+        messages=(),
+        offset=0,
+        sep_style=SeparatorStyle.NO_COLON_SINGLE,
+        sep=None,
+    )
+)
+
 # Llama-2 default template
 register_conv_template(
     Conversation(
         name="llama-2",
         system="",
         roles=("user", "assistant", "system"),
         messages=(),
```

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/handler.py` & `alphawave-0.3.95/src/alphawave_pyexts/handler.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/llmsearch/google_search_concurrent.py` & `alphawave-0.3.95/src/alphawave_pyexts/llmsearch/google_search_concurrent.py`

 * *Files 1% similar despite different names*

```diff
@@ -187,15 +187,15 @@
         urls.append(url)
     return urls
 
 def log_url_process(site, reason, raw_text, extract_text, gpt_text):
     return
 
 
-async def llm_tldr (text, query, client, model, memory, functions, tokenizer, max_chars):
+def llm_tldr (text, query, client, model, memory, functions, tokenizer, max_chars):
     text = text[:max_chars] # make sure we don't run over token limit
     prompt = Prompt([UserMessage('Analyze the following Text to identify if there is any content relevant to the query {{$query}}, Respond using this JSON template:\n\n{"relevant": "Yes" if there is any text found in the input that is relevant to the query, "No" otherwise>, "tldr": "<relevant content found in Text, rewritten coherence>"}\n\nText:\n{{$input}}\n. ')])
     response_text=''
     completion = None
     schema = {
         "schema_type":"object",
         "title":"tldr",
@@ -213,15 +213,15 @@
         "required":["relevant", "tldr"],
         "returns":"extract"
     }
     
     options = PromptCompletionOptions(completion_type='chat', model=model)
     # don't clutter primary memory with tldr stuff
     fork = MemoryFork(memory)
-    response = await ut.run_wave(client, {'input':text, 'query':query}, prompt, options, fork, functions, tokenizer, validator=JSONResponseValidator(schema))
+    response = ut.run_wave(client, {'input':text, 'query':query}, prompt, options, fork, functions, tokenizer, validator=JSONResponseValidator(schema))
     #print(f'\n***** google llm_tldr processing \n{response}')
     if type(response) == dict and 'status' in response and response['status'] == 'success'and 'message' in response:
         message = response['message']
         if type(message) != dict:
             try:
                 message = json.loads(message)
             except Exception as e:
@@ -271,15 +271,15 @@
         if len(candidate) > 4 and candidate[0].isdigit():
             candidate = candidate[1:].lstrip('. ')
             if len(candidate) > 4 and candidate[0].isdigit(): # strip second digit if more than 10 items
                 candidate = candidate[1:].lstrip('. ')
             items += candidate+' '
     return items
 
-async def search_google(original_query, search_level, query_phrase, keywords, client, model, memory, functions, tokenizer, max_chars):
+def search_google(original_query, search_level, query_phrase, keywords, client, model, memory, functions, tokenizer, max_chars):
   start_time = time.time()
   all_urls=[]; urls_used=[]; urls_tried=[]
   index = 0; tried_index = 0
   full_text=''
   keyword_weights = {}
   for keyword in keywords:
       zipf = wf.zipf_frequency(keyword, 'en')
@@ -315,12 +315,12 @@
         if url in gpt_phrase_urls:
             gpt_phrase_urls.remove(url)
 
     # interleave both lists now that duplicates are removed
     urls = [val for tup in zip_longest(orig_phrase_urls, gpt_phrase_urls) for val in tup if val is not None]
     all_urls = copy.deepcopy(urls)
     full_text = \
-        await process_urls(extract_query, keywords, keyword_weights, all_urls, search_level, client, model, memory, functions, tokenizer, max_chars)
+        asyncio.run(process_urls(extract_query, keywords, keyword_weights, all_urls, search_level, client, model, memory, functions, tokenizer, max_chars))
   except:
       traceback.print_exc()
   return  full_text
```

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/llmsearch/search_service.py` & `alphawave-0.3.95/src/alphawave_pyexts/llmsearch/search_service.py`

 * *Files 5% similar despite different names*

```diff
@@ -7,26 +7,26 @@
 from alphawave.MemoryFork import MemoryFork
 import alphawave_pyexts.llmsearch.google_search_concurrent as gs
 import alphawave_pyexts.utilityV2 as ut
 import asyncio
 history = {}
 
 
-async def run_chat(client, query_string, model,  memory, functions, tokenizer, max_chars=1500, search_level=gs.QUICK_SEARCH):
+def run_chat(client, query_string, model,  memory, functions, tokenizer, max_chars=1500, search_level=gs.QUICK_SEARCH):
   #tracemalloc.start()
   response_text = ''
   storeInteraction = True
   try:
     #
     fork = MemoryFork(memory)
-    query_phrase, keywords = await ut.get_search_phrase_and_keywords(client, query_string, model, fork, functions, tokenizer)
+    query_phrase, keywords = ut.get_search_phrase_and_keywords(client, query_string, model, fork, functions, tokenizer)
 
     google_text=\
-      await gs.search_google(query_string, gs.QUICK_SEARCH, query_phrase, keywords, client, model, fork, functions, tokenizer, max_chars)
+      gs.search_google(query_string, gs.QUICK_SEARCH, query_phrase, keywords, client, model, fork, functions, tokenizer, max_chars)
     return google_text
   except:
     traceback.print_exc()
   return ''
 
 if __name__ == '__main__' :
   while True:
-    asyncio.run(run_chat(input('Yes?')))
+    run_chat(input('Yes?'))
```

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/modelling_RW.py` & `alphawave-0.3.95/src/alphawave_pyexts/modelling_RW.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/serverUtils.py` & `alphawave-0.3.95/src/alphawave_pyexts/serverUtils.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/src/alphawave_pyexts/utilityV2.py` & `alphawave-0.3.95/src/alphawave_pyexts/utilityV2.py`

 * *Files 2% similar despite different names*

```diff
@@ -37,26 +37,26 @@
 from alphawave.MemoryFork import MemoryFork
 
 openai.api_key = os.getenv("OPENAI_API_KEY")
 google_key = os.getenv("GOOGLE_KEY")
 google_cx = os.getenv("GOOGLE_CX")
 GOOGLE = 'google'
 
-async def ask_LLM(model, gpt_message, max_tokens=100, temp=0.7, top_p=1.0, host = None, port = None, tkroot = None, tkdisplay=None):
+def ask_LLM(model, gpt_message, max_tokens=100, temp=0.7, top_p=1.0, host = None, port = None, tkroot = None, tkdisplay=None):
     completion = None
     response = ''
     #print(f'***** utility ask_LLL temperature {temp}')
     try:
       if not model.lower().startswith('gpt'):
-        completion = await llm.run_query(model, gpt_message, max_tokens, temp, top_p, host, port, tkroot, tkdisplay )
+        completion = llm.run_query(model, gpt_message, max_tokens, temp, top_p, host, port, tkroot, tkdisplay )
         if completion is not None:
           response = completion
 
       else:
-        stream= await openai.ChatCompletion.create(
+        stream= openai.ChatCompletion.create(
             model=model, messages=gpt_message, max_tokens=max_tokens, temperature=temp, top_p=1, stop='STOP', stream=True)
         response = ''
         if stream is None:
           return response
         for chunk in stream:
           item = chunk['choices'][0]['delta']
           if 'content' in item.keys():
@@ -96,15 +96,15 @@
 def part_of_keyword(word, keywords):
     for keyword in keywords:
         if word in keyword:
             return True
     return False
 
 
-async def run_wave (client, input, prompt, prompt_options, memory, functions, tokenizer, max_repair_attempts=1, logRepairs=False, validator=DefaultResponseValidator()):
+def run_wave (client, input, prompt, prompt_options, memory, functions, tokenizer, max_repair_attempts=1, logRepairs=False, validator=DefaultResponseValidator()):
     # Create a wave for the prompt
     fork = MemoryFork(memory)
     for key, value in input.items():
       fork.set(key, value)
 
     wave = AlphaWave(client=client,
                      prompt=prompt,
@@ -112,24 +112,24 @@
                      memory=fork,
                      functions=functions,
                      max_repair_attempts = max_repair_attempts,
                      tokenizer=tokenizer,
                      validator = validator,
                      logRepairs = logRepairs)
 
-    response = await wave.completePrompt()
+    response = wave.completePrompt()
     # Ensure response succeeded
     return {
       'type': "TaskResponse",
       'status': response['status'],
       'message': response['message']
     }
       
 
-async def get_search_phrase_and_keywords(client, query_string, model, memory, functions, tokenizer):
+def get_search_phrase_and_keywords(client, query_string, model, memory, functions, tokenizer):
 
     prompt = Prompt([UserMessage('Text:\n\n{{$input}}\n\n. Analyze the above Text. Respond using this JSON template:\n\n{"Phrase": <rewrite of Text as an effective google search phrase>, "Keywords": [keywords in Text],"NamedEntities": [NamedEntities in text]}')])
     response_text=''
     completion = None
     schema = {
       'schema_type':'object',
       'title':'rephrase',
@@ -151,15 +151,15 @@
       'required':['Phrase', 'Keywords', 'NamedEntities'],
       'returns':"query answer"
     }
 
     phrase = ''; keywords = []
     try:
         options = PromptCompletionOptions(completion_type='chat', model=model)
-        response = await run_wave(client, {'input':query_string}, prompt, options, memory, functions, tokenizer, validator=JSONResponseValidator(schema))
+        response = run_wave(client, {'input':query_string}, prompt, options, memory, functions, tokenizer, validator=JSONResponseValidator(schema))
         
         #print(response)
         if type(response) == dict and 'status' in response and response['status'] == 'success':
             content = response['message']['content']
             if type(content) == dict:
                 if 'Phrase' in content:
                     phrase = content['Phrase']
@@ -167,15 +167,15 @@
                     keywords = content['Keywords']
                 return phrase, keywords
     except Exception as e:
         traceback.print_exc()
     return phrase, keywords
 
 
-async def get_toml_search_phrase_and_keywords(client, query_string, model, memory, functions, tokenizer):
+def get_toml_search_phrase_and_keywords(client, query_string, model, memory, functions, tokenizer):
 
     prompt = Prompt([UserMessage(
 """Your task is to generate Keywords and a concise Phrase on the topic of the following Text.
 Respond ONLY with Phrase and Keywords. Use this TOML schema for your response:
 [RESPONSE]
 Phrase="<concise topic phrase>"
 Keywords="<keywords>"
@@ -200,15 +200,15 @@
         }
     }
 
     phrase = ''; keywords = []
     try:
         memory.set('input', query_string)
         options = PromptCompletionOptions(completion_type='chat', model=model)
-        response = await run_wave(client, {"input":query_string}, prompt, options, memory, functions, tokenizer,
+        response = run_wave(client, {"input":query_string}, prompt, options, memory, functions, tokenizer,
                                   max_repair_attempts=2, validator=TOMLResponseValidator(schema))
         
         #print(response)
         if type(response) == dict and 'status' in response and response['status'] == 'success':
             content = response['message']['content']
             if type(content) == dict:
                 if 'Phrase' in content:
```

### Comparing `alphawave-0.3.93/tests/testOSClient.py` & `alphawave-0.3.95/tests/testOSClient.py`

 * *Files identical despite different names*

### Comparing `alphawave-0.3.93/tests/testOpenAiClient.py` & `alphawave-0.3.95/tests/testOpenAiClient.py`

 * *Files identical despite different names*

