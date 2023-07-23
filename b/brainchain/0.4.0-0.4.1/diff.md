# Comparing `tmp/brainchain-0.4.0.tar.gz` & `tmp/brainchain-0.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "brainchain-0.4.0.tar", max compression
+gzip compressed data, was "brainchain-0.4.1.tar", max compression
```

## Comparing `brainchain-0.4.0.tar` & `brainchain-0.4.1.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1732 2023-06-20 22:57:22.671703 brainchain-0.4.0/brainchain/README.md
--rw-r--r--   0        0        0      167 2023-07-06 20:56:21.342669 brainchain-0.4.0/brainchain/__init__.py
--rw-r--r--   0        0        0    11495 2023-07-21 21:52:52.254607 brainchain-0.4.0/brainchain/brainchain.py
--rw-r--r--   0        0        0     5579 2023-06-20 22:25:05.537647 brainchain-0.4.0/brainchain/carnivore.py
--rw-r--r--   0        0        0     2243 2023-07-06 00:06:03.958510 brainchain-0.4.0/brainchain/coredata.py
--rw-r--r--   0        0        0      665 2023-07-20 04:24:18.860063 brainchain-0.4.0/brainchain/factcheck.py
--rw-r--r--   0        0        0    15070 2023-07-05 18:42:36.359889 brainchain-0.4.0/brainchain/requirements.txt
--rw-r--r--   0        0        0     6333 2023-07-06 18:26:20.604519 brainchain-0.4.0/brainchain/sales_intel.py
--rw-r--r--   0        0        0      581 2023-07-21 21:53:09.537786 brainchain-0.4.0/pyproject.toml
--rw-r--r--   0        0        0      612 1970-01-01 00:00:00.000000 brainchain-0.4.0/PKG-INFO
+-rw-r--r--   0        0        0     1732 2023-06-20 22:57:22.671703 brainchain-0.4.1/brainchain/README.md
+-rw-r--r--   0        0        0      167 2023-07-06 20:56:21.342669 brainchain-0.4.1/brainchain/__init__.py
+-rw-r--r--   0        0        0    11485 2023-07-23 13:18:19.901321 brainchain-0.4.1/brainchain/brainchain.py
+-rw-r--r--   0        0        0     5579 2023-06-20 22:25:05.537647 brainchain-0.4.1/brainchain/carnivore.py
+-rw-r--r--   0        0        0     2243 2023-07-06 00:06:03.958510 brainchain-0.4.1/brainchain/coredata.py
+-rw-r--r--   0        0        0      665 2023-07-20 04:24:18.860063 brainchain-0.4.1/brainchain/factcheck.py
+-rw-r--r--   0        0        0    15070 2023-07-05 18:42:36.359889 brainchain-0.4.1/brainchain/requirements.txt
+-rw-r--r--   0        0        0     6333 2023-07-06 18:26:20.604519 brainchain-0.4.1/brainchain/sales_intel.py
+-rw-r--r--   0        0        0      581 2023-07-23 13:18:23.876547 brainchain-0.4.1/pyproject.toml
+-rw-r--r--   0        0        0      612 1970-01-01 00:00:00.000000 brainchain-0.4.1/PKG-INFO
```

### Comparing `brainchain-0.4.0/brainchain/README.md` & `brainchain-0.4.1/brainchain/README.md`

 * *Files identical despite different names*

### Comparing `brainchain-0.4.0/brainchain/brainchain.py` & `brainchain-0.4.1/brainchain/brainchain.py`

 * *Files 1% similar despite different names*

```diff
@@ -201,15 +201,15 @@
             payload["document_text"] = text_first_page
 
         headers = {"Authorization": f"Bearer {self.api_key}"}
         response = requests.post(endpoint, headers=headers, json=payload)
         content = response.content.decode('utf-8')
         return json.loads(content)
 
-    def summon(self, prompt, agent_type="CCR", model="gpt-4-0613", max_tokens=2048, temperature=0.18, top_p=0.15, top_k=0.0, presence_penalty=1.0, frequency_penalty=1.0, chat_history: list = []):
+    def summon(self, prompt, agent_type="OAMF", model="gpt-4-0613", max_tokens=2048, temperature=0, top_p=0, top_k=0.0, presence_penalty=0.0, frequency_penalty=0.0, chat_history: list = []):
         endpoint = self.services["agent-service"]["agent"]
         headers = {"Authorization": f"Bearer {self.api_key}"}
         params = {
             "prompt": prompt,
             "env": self.env,
             "agent_type": agent_type,
             "model": model,
@@ -224,15 +224,15 @@
         response = requests.post(endpoint, headers=headers, json=params)
 
         if response.status_code == 200:
             return response.json()
         else:
             response.raise_for_status()
 
-    async def asummon(self, prompt, agent_type="CCR", model="gpt-4-0613", max_tokens=2048, temperature=0.18, top_p=0.15, top_k=0.0, presence_penalty=1.0, frequency_penalty=1.0, chat_history: list = []):
+    async def asummon(self, prompt, agent_type="OAMF", model="gpt-4-0613", max_tokens=2048, temperature=0, top_p=0, top_k=0.0, presence_penalty=0.0, frequency_penalty=0.0, chat_history: list = []):
         endpoint = self.services["agent-service"]["agent"]
         headers = {"Authorization": f"Bearer {self.api_key}"}
         params = {
             "prompt": prompt,
             "env": self.env,
             "agent_type": agent_type,
             "model": model,
```

### Comparing `brainchain-0.4.0/brainchain/carnivore.py` & `brainchain-0.4.1/brainchain/carnivore.py`

 * *Files identical despite different names*

### Comparing `brainchain-0.4.0/brainchain/coredata.py` & `brainchain-0.4.1/brainchain/coredata.py`

 * *Files identical despite different names*

### Comparing `brainchain-0.4.0/brainchain/factcheck.py` & `brainchain-0.4.1/brainchain/factcheck.py`

 * *Files identical despite different names*

### Comparing `brainchain-0.4.0/brainchain/requirements.txt` & `brainchain-0.4.1/brainchain/requirements.txt`

 * *Files identical despite different names*

### Comparing `brainchain-0.4.0/brainchain/sales_intel.py` & `brainchain-0.4.1/brainchain/sales_intel.py`

 * *Files identical despite different names*

### Comparing `brainchain-0.4.0/pyproject.toml` & `brainchain-0.4.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "brainchain"
-version = "0.4.0"
+version = "0.4.1"
 description = "Brainchain API client"
 authors = ["Arthur M. Collé <arthur@brainchain.ai>", "Audrey Lorberfeld <alorberfeld@brainchain.ai>"]
 
 [tool.poetry.dependencies]
 python = ">=3.8,<4.0"
 requests = "2.31.0"
 promptlayer = "0.1.92"
```

### Comparing `brainchain-0.4.0/PKG-INFO` & `brainchain-0.4.1/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: brainchain
-Version: 0.4.0
+Version: 0.4.1
 Summary: Brainchain API client
 Author: Arthur M. Collé
 Author-email: arthur@brainchain.ai
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
```

