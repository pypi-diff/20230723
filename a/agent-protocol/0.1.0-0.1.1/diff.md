# Comparing `tmp/agent_protocol-0.1.0.tar.gz` & `tmp/agent_protocol-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "agent_protocol-0.1.0.tar", max compression
+gzip compressed data, was "agent_protocol-0.1.1.tar", max compression
```

## Comparing `agent_protocol-0.1.0.tar` & `agent_protocol-0.1.1.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0     2078 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/README.md
--rw-r--r--   0        0        0       76 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/agent_protocol/__init__.py
--rw-r--r--   0        0        0     4074 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/agent_protocol/agent.py
--rw-r--r--   0        0        0      202 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/agent_protocol/dependencies.py
--rw-r--r--   0        0        0     1683 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/agent_protocol/models.py
--rw-r--r--   0        0        0      329 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/agent_protocol/server.py
--rw-r--r--   0        0        0      723 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     2914 1970-01-01 00:00:00.000000 agent_protocol-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0     2078 2023-07-23 11:51:55.219507 agent_protocol-0.1.1/README.md
+-rw-r--r--   0        0        0       76 2023-07-23 11:51:55.219507 agent_protocol-0.1.1/agent_protocol/__init__.py
+-rw-r--r--   0        0        0     4008 2023-07-23 11:51:55.219507 agent_protocol-0.1.1/agent_protocol/agent.py
+-rw-r--r--   0        0        0      202 2023-07-23 11:51:55.219507 agent_protocol-0.1.1/agent_protocol/dependencies.py
+-rw-r--r--   0        0        0     1683 2023-07-23 11:51:55.219507 agent_protocol-0.1.1/agent_protocol/models.py
+-rw-r--r--   0        0        0      329 2023-07-23 11:51:55.219507 agent_protocol-0.1.1/agent_protocol/server.py
+-rw-r--r--   0        0        0      692 2023-07-23 11:51:55.223507 agent_protocol-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0     2908 1970-01-01 00:00:00.000000 agent_protocol-0.1.1/PKG-INFO
```

### Comparing `agent_protocol-0.1.0/README.md` & `agent_protocol-0.1.1/README.md`

 * *Files identical despite different names*

### Comparing `agent_protocol-0.1.0/agent_protocol/agent.py` & `agent_protocol-0.1.1/agent_protocol/agent.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,15 +1,14 @@
-import trio
+import asyncio
+
 import uuid
 
-from hypercorn.trio import serve
+from hypercorn.asyncio import serve
 from hypercorn.config import Config
 from typing import Awaitable, Callable, List, Optional, Tuple, Any
-from .dependencies import *
-from .models import Step, Task, TaskRequestBody
 
 
 from .server import app
 from .models import (
     Task,
     TaskRequestBody,
     Step,
@@ -152,8 +151,8 @@
 
         return Agent
 
     @staticmethod
     def start(port: int = 8000):
         config = Config()
         config.bind = [f"localhost:{port}"]  # As an example configuration setting
-        trio.run(serve, app, config)
+        asyncio.run(serve(app, config))
```

### Comparing `agent_protocol-0.1.0/agent_protocol/models.py` & `agent_protocol-0.1.1/agent_protocol/models.py`

 * *Files identical despite different names*

### Comparing `agent_protocol-0.1.0/PKG-INFO` & `agent_protocol-0.1.1/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 Metadata-Version: 2.1
 Name: agent-protocol
-Version: 0.1.0
+Version: 0.1.1
 Summary: API for interacting with Agent
 Home-page: https://e2b.dev/
 License: MIT
 Author: e2b
 Author-email: hello@e2b.dev
 Requires-Python: >=3.7,<4.0.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: fastapi (>=0.100.0,<0.101.0)
-Requires-Dist: hypercorn[trio] (>=0.14.4,<0.15.0)
+Requires-Dist: hypercorn (>=0.14.4,<0.15.0)
 Project-URL: Bug Tracker, https://github.com/e2b/sdk/issues
 Project-URL: Repository, https://github.com/e2b-dev/sdk/tree/main/agent/python/
 Description-Content-Type: text/markdown
 
 # Agent Communication Protocol - Python SDK
 
 This SDK implements the Agent Communication Protocol in Python and allows you to easily wrap your agent in a webserver compatible with the protocol - you only need to define an agent task handler.
```

