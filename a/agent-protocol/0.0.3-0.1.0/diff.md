# Comparing `tmp/agent_protocol-0.0.3.tar.gz` & `tmp/agent_protocol-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "agent_protocol-0.0.3.tar", max compression
+gzip compressed data, was "agent_protocol-0.1.0.tar", max compression
```

## Comparing `agent_protocol-0.0.3.tar` & `agent_protocol-0.1.0.tar`

### file list

```diff
@@ -1,7 +1,8 @@
--rw-r--r--   0        0        0       76 2023-07-19 12:45:27.367291 agent_protocol-0.0.3/agent_protocol/__init__.py
--rw-r--r--   0        0        0     4040 2023-07-19 13:04:18.882968 agent_protocol-0.0.3/agent_protocol/agent.py
--rw-r--r--   0        0        0      202 2023-07-19 12:37:58.353578 agent_protocol-0.0.3/agent_protocol/dependencies.py
--rw-r--r--   0        0        0     1683 2023-07-19 12:59:33.427352 agent_protocol-0.0.3/agent_protocol/models.py
--rw-r--r--   0        0        0      329 2023-07-19 12:41:22.124876 agent_protocol-0.0.3/agent_protocol/server.py
--rw-r--r--   0        0        0      640 2023-07-19 13:04:49.229831 agent_protocol-0.0.3/pyproject.toml
--rw-r--r--   0        0        0      626 1970-01-01 00:00:00.000000 agent_protocol-0.0.3/PKG-INFO
+-rw-r--r--   0        0        0     2078 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/README.md
+-rw-r--r--   0        0        0       76 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/agent_protocol/__init__.py
+-rw-r--r--   0        0        0     4074 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/agent_protocol/agent.py
+-rw-r--r--   0        0        0      202 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/agent_protocol/dependencies.py
+-rw-r--r--   0        0        0     1683 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/agent_protocol/models.py
+-rw-r--r--   0        0        0      329 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/agent_protocol/server.py
+-rw-r--r--   0        0        0      723 2023-07-23 08:46:43.772148 agent_protocol-0.1.0/pyproject.toml
+-rw-r--r--   0        0        0     2914 1970-01-01 00:00:00.000000 agent_protocol-0.1.0/PKG-INFO
```

### Comparing `agent_protocol-0.0.3/agent_protocol/agent.py` & `agent_protocol-0.1.0/agent_protocol/agent.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,17 +3,14 @@
 
 from hypercorn.trio import serve
 from hypercorn.config import Config
 from typing import Awaitable, Callable, List, Optional, Tuple, Any
 from .dependencies import *
 from .models import Step, Task, TaskRequestBody
 
-config = Config()
-config.bind = ["localhost:8000"]  # As an example configuration setting
-
 
 from .server import app
 from .models import (
     Task,
     TaskRequestBody,
     Step,
     StepInput,
@@ -152,9 +149,11 @@
     def handle_task(handler: Callable[[TaskInput | None], Awaitable[StepHandler]]):
         global task_handler
         task_handler = handler
 
         return Agent
 
     @staticmethod
-    def start():
+    def start(port: int = 8000):
+        config = Config()
+        config.bind = [f"localhost:{port}"]  # As an example configuration setting
         trio.run(serve, app, config)
```

### Comparing `agent_protocol-0.0.3/agent_protocol/models.py` & `agent_protocol-0.1.0/agent_protocol/models.py`

 * *Files identical despite different names*

### Comparing `agent_protocol-0.0.3/pyproject.toml` & `agent_protocol-0.1.0/pyproject.toml`

 * *Files 24% similar despite different names*

```diff
@@ -1,13 +1,16 @@
 [tool.poetry]
 name = "agent-protocol"
-version = "0.0.3"
+version = "0.1.0"
 description = "API for interacting with Agent"
 authors = ["e2b <hello@e2b.dev>"]
 license = "MIT"
+readme = "README.md"
+homepage = "https://e2b.dev/"
+repository = "https://github.com/e2b-dev/sdk/tree/main/agent/python/"
 packages = [{ include = "agent_protocol" }]
 
 [tool.poetry.dependencies]
 python = ">=3.7, <4.0.0"
 fastapi = "^0.100.0"
 hypercorn = {extras = ["trio"], version = "^0.14.4"}
 
@@ -17,10 +20,9 @@
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry.scripts]
 src = "src.__main__:main"
 
-[project.urls]
-"Homepage" = "https://github.com/e2b/sdk"
+[tool.poetry.urls]
 "Bug Tracker" = "https://github.com/e2b/sdk/issues"
```

