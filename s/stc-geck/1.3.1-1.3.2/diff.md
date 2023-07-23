# Comparing `tmp/stc-geck-1.3.1.tar.gz` & `tmp/stc-geck-1.3.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "stc-geck-1.3.1.tar", last modified: Thu Jul  6 11:01:58 2023, max compression
+gzip compressed data, was "stc-geck-1.3.2.tar", last modified: Sun Jul 23 16:40:12 2023, max compression
```

## Comparing `stc-geck-1.3.1.tar` & `stc-geck-1.3.2.tar`

### file list

```diff
@@ -1,19 +1,20 @@
-drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-06 11:01:58.393175 stc-geck-1.3.1/
--rw-r--r--   0 pasha      (501) staff       (20)       24 2022-12-01 11:19:40.000000 stc-geck-1.3.1/MANIFEST.in
--rw-r--r--   0 pasha      (501) staff       (20)      743 2023-07-06 11:01:58.392811 stc-geck-1.3.1/PKG-INFO
--rw-r--r--   0 pasha      (501) staff       (20)      398 2023-07-03 19:45:17.000000 stc-geck-1.3.1/README.md
--rw-r--r--   0 pasha      (501) staff       (20)      600 2023-07-06 11:01:49.000000 stc-geck-1.3.1/pyproject.toml
--rw-r--r--   0 pasha      (501) staff       (20)       96 2023-07-05 16:20:57.000000 stc-geck-1.3.1/requirements.txt
--rw-r--r--   0 pasha      (501) staff       (20)       38 2023-07-06 11:01:58.393284 stc-geck-1.3.1/setup.cfg
-drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-06 11:01:58.389440 stc-geck-1.3.1/stc_geck/
--rw-r--r--   0 pasha      (501) staff       (20)      924 2023-07-06 11:01:38.000000 stc-geck-1.3.1/stc_geck/advices.py
--rw-r--r--   0 pasha      (501) staff       (20)     6136 2023-07-05 16:12:35.000000 stc-geck-1.3.1/stc_geck/cli.py
--rw-r--r--   0 pasha      (501) staff       (20)     5950 2023-07-05 19:36:58.000000 stc-geck-1.3.1/stc_geck/client.py
--rw-r--r--   0 pasha      (501) staff       (20)     1640 2023-07-05 19:36:42.000000 stc-geck-1.3.1/stc_geck/utils.py
-drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-06 11:01:58.392040 stc-geck-1.3.1/stc_geck.egg-info/
--rw-r--r--   0 pasha      (501) staff       (20)      743 2023-07-06 11:01:58.000000 stc-geck-1.3.1/stc_geck.egg-info/PKG-INFO
--rw-r--r--   0 pasha      (501) staff       (20)      320 2023-07-06 11:01:58.000000 stc-geck-1.3.1/stc_geck.egg-info/SOURCES.txt
--rw-r--r--   0 pasha      (501) staff       (20)        1 2023-07-06 11:01:58.000000 stc-geck-1.3.1/stc_geck.egg-info/dependency_links.txt
--rw-r--r--   0 pasha      (501) staff       (20)       43 2023-07-06 11:01:58.000000 stc-geck-1.3.1/stc_geck.egg-info/entry_points.txt
--rw-r--r--   0 pasha      (501) staff       (20)       97 2023-07-06 11:01:58.000000 stc-geck-1.3.1/stc_geck.egg-info/requires.txt
--rw-r--r--   0 pasha      (501) staff       (20)        9 2023-07-06 11:01:58.000000 stc-geck-1.3.1/stc_geck.egg-info/top_level.txt
+drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 16:40:12.474511 stc-geck-1.3.2/
+-rw-r--r--   0 pasha      (501) staff       (20)       24 2022-12-01 11:19:40.000000 stc-geck-1.3.2/MANIFEST.in
+-rw-r--r--   0 pasha      (501) staff       (20)     1033 2023-07-23 16:40:12.473872 stc-geck-1.3.2/PKG-INFO
+-rw-r--r--   0 pasha      (501) staff       (20)      688 2023-07-22 19:34:42.000000 stc-geck-1.3.2/README.md
+-rw-r--r--   0 pasha      (501) staff       (20)      600 2023-07-22 19:20:49.000000 stc-geck-1.3.2/pyproject.toml
+-rw-r--r--   0 pasha      (501) staff       (20)      161 2023-07-20 13:58:38.000000 stc-geck-1.3.2/requirements.txt
+-rw-r--r--   0 pasha      (501) staff       (20)       38 2023-07-23 16:40:12.474828 stc-geck-1.3.2/setup.cfg
+drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 16:40:12.467378 stc-geck-1.3.2/stc_geck/
+-rw-r--r--   0 pasha      (501) staff       (20)        0 2023-07-19 19:56:31.000000 stc-geck-1.3.2/stc_geck/__init__.py
+-rw-r--r--   0 pasha      (501) staff       (20)      923 2023-07-06 11:45:56.000000 stc-geck-1.3.2/stc_geck/advices.py
+-rw-r--r--   0 pasha      (501) staff       (20)     7344 2023-07-22 18:20:45.000000 stc-geck-1.3.2/stc_geck/cli.py
+-rw-r--r--   0 pasha      (501) staff       (20)     7229 2023-07-22 08:15:51.000000 stc-geck-1.3.2/stc_geck/client.py
+-rw-r--r--   0 pasha      (501) staff       (20)     1877 2023-07-22 08:16:03.000000 stc-geck-1.3.2/stc_geck/utils.py
+drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 16:40:12.472698 stc-geck-1.3.2/stc_geck.egg-info/
+-rw-r--r--   0 pasha      (501) staff       (20)     1033 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/PKG-INFO
+-rw-r--r--   0 pasha      (501) staff       (20)      341 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/SOURCES.txt
+-rw-r--r--   0 pasha      (501) staff       (20)        1 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/dependency_links.txt
+-rw-r--r--   0 pasha      (501) staff       (20)       43 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/entry_points.txt
+-rw-r--r--   0 pasha      (501) staff       (20)      162 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/requires.txt
+-rw-r--r--   0 pasha      (501) staff       (20)        9 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/top_level.txt
```

### Comparing `stc-geck-1.3.1/PKG-INFO` & `stc-geck-1.3.2/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,29 +1,39 @@
 Metadata-Version: 2.1
 Name: stc-geck
-Version: 1.3.1
+Version: 1.3.2
 Summary: GECK (Garden Of Eden Creation Kit) is a toolkit for setting up and maintaning STC
 Author: Interdimensional Walker
 Project-URL: Homepage, https://github.com/nexus-stc/stc
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 
 # GECK (Garden of Eden Creation Kit)
 
+GECK is a Python library and Bash tool for interacting with STC programmatically.
+It allows to startup embedded Summa instance, do search queries and iterate over database.
+
 ## Install
 
 ```bash
 pip install stc-geck
 ```
 
-## Usage
+## Examples
+
+### CLI
 
 ```bash
 # Iterate over all stored documents
-geck --ipfs-http-endpoint 127.0.0.1:8080 - documents
+geck --ipfs-http-base-url 127.0.0.1:8080 - documents
 
 # Do a match search by field
-geck --ipfs-http-endpoint 127.0.0.1:8080 - search doi:10.3384/ecp1392a41
+geck --ipfs-http-base-url 127.0.0.1:8080 - search doi:10.3384/ecp1392a41
+
 # Do a match search by word
-geck --ipfs-http-endpoint 127.0.0.1:8080 - search hemoglobin --limit 10
+geck --ipfs-http-base-url 127.0.0.1:8080 - search hemoglobin --limit 10
 ```
+
+### Python
+
+Examples for Python can be found in [examples directory](/geck/examples/search-stc.ipynb)
```

### Comparing `stc-geck-1.3.1/pyproject.toml` & `stc-geck-1.3.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools<65.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "stc-geck"
-version = "1.3.1"
+version = "1.3.2"
 authors = [{ name = "Interdimensional Walker" }]
 description = "GECK (Garden Of Eden Creation Kit) is a toolkit for setting up and maintaning STC"
 readme = "README.md"
 requires-python = ">=3.8"
 classifiers = [
     "Programming Language :: Python :: 3.8",
 ]
```

### Comparing `stc-geck-1.3.1/stc_geck/advices.py` & `stc-geck-1.3.2/stc_geck/advices.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,9 @@
 from aiosumma import SummaClient
 
-
 PR_TEMPORAL_RANKING_FORMULA = "original_score * custom_score * fastsigm(abs(now - issued_at) / (86400 * 3) + 5, -1) * 1.96 * " \
                               "fastsigm(iqpr(quantized_page_rank), 0.15)"
 
 
 async def get_documents_on_topic(summa_client: SummaClient, topic: str, documents: int = 20):
     return await summa_client.search_documents([{
         "index_alias": "nexus_science",
```

### Comparing `stc-geck-1.3.1/stc_geck/cli.py` & `stc-geck-1.3.2/stc_geck/cli.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,18 +1,20 @@
 #!/usr/bin/env python3
+import asyncio
 import json
 import logging
 import os.path
 import sys
+from typing import Optional
 
 import fire
+import humanfriendly
+from client import StcGeck
 from termcolor import colored
 
-from .client import StcGeck
-
 
 class ItemNotFound(Exception):
     def __init__(self, query):
         self.query = query
 
     def __str__(self):
         return f'ItemNotFound(query="{self.query}")'
@@ -26,53 +28,30 @@
         return f'CidNotFound(query="{self.query}")'
 
 
 class StcGeckCli:
     def __init__(
         self,
         ipfs_http_base_url: str,
+        ipfs_api_base_url: str,
         ipfs_data_directory: str,
         index_name: str,
         grpc_api_endpoint: str,
-        embed: bool,
         timeout: int,
     ):
         self.geck = StcGeck(
             ipfs_http_base_url=ipfs_http_base_url,
+            ipfs_api_base_url=ipfs_api_base_url,
             ipfs_data_directory=ipfs_data_directory,
             index_names=(index_name,),
             grpc_api_endpoint=grpc_api_endpoint,
-            embed=embed,
+            timeout=timeout,
         )
+        self.grpc_api_endpoint = grpc_api_endpoint
         self.index_name = index_name
-        self.timeout = timeout
-
-    async def search(self, query: str, limit: int = 1):
-        """
-        Searches in STC using default Summa match queries.
-        Examples: `doi:10.1234/abc, isbns:9781234567890, "fetal hemoglobin"`
-
-        :param query: query in Summa match format
-        :param limit: how many results to return, higher values incurs LARGE performance penalty.
-
-        :return: metadata records
-        """
-        print(f"{colored('INFO', 'green')}: Setting up indices: {self.index_name}...")
-        async with self.geck as geck:
-            print(f"{colored('INFO', 'green')}: Searching {query}...")
-            response = await geck.get_summa_client().search([{
-                "index_alias": self.index_name,
-                "query": {
-                    "match": {"value": query}
-                },
-                "collectors": [{"top_docs": {"limit": limit}}],
-                "is_fieldnorms_scoring_enabled": False,
-            }])
-            documents = list(map(lambda x: json.loads(x.document), response.collector_outputs[0].documents.scored_documents))
-            return documents
 
     async def documents(self):
         """
         Stream all STC documents.
 
         :return: metadata records
         """
@@ -99,25 +78,74 @@
             if 'cid' in results[0]:
                 print(f"{colored('INFO', 'green')}: Receiving file {query}...")
                 if (real_extension := results[0].get('extension', 'pdf')) != output_path_ext:
                     print(
                         f"{colored('WARN', 'yellow')}: Receiving file extension `{real_extension}` "
                         f"is not matching with your output path extension `{output_path_ext}`. Changed to correct one.")
                     output_path_ext = real_extension
-                data = await self.geck.download(results[0]["cid"], self.timeout)
+                data = await self.geck.download(results[0]["cid"])
                 final_file_name = output_path + '.' + output_path_ext
                 with open(final_file_name, 'wb') as f:
                     f.write(data)
                     f.close()
                     print(f"{colored('INFO', 'green')}: File {final_file_name} is written")
             else:
                 print(f"{colored('ERROR', 'red')}: Not found CID for {query}", file=sys.stderr)
         else:
             print(f"{colored('ERROR', 'red')}: Not found {query}", file=sys.stderr)
 
+    async def random_cids(self, n: Optional[int] = None, space: Optional[str] = None):
+        """
+        Return random CIDs for pinning from the STC Hub API.
+
+        :param n: number of items to pin
+        :param space: approximate disk space you would like to allocate for pinning
+        """
+        if not n and not space:
+            raise ValueError("`n` or `space_bytes` should be set")
+        if space:
+            # 3.61MB is the average size of the item
+            n = int(humanfriendly.parse_size(space) / (3.61 * 1024 * 1024))
+        async with self.geck as geck:
+            return await geck.random_cids(n=n)
+
+    async def search(self, query: str, limit: int = 1):
+        """
+        Searches in STC using default Summa match queries.
+        Examples: `doi:10.1234/abc, isbns:9781234567890, "fetal hemoglobin"`
+
+        :param query: query in Summa match format
+        :param limit: how many results to return, higher values incurs LARGE performance penalty.
+
+        :return: metadata records
+        """
+        print(f"{colored('INFO', 'green')}: Setting up indices: {self.index_name}...")
+        async with self.geck as geck:
+            print(f"{colored('INFO', 'green')}: Searching {query}...")
+            response = await geck.get_summa_client().search([{
+                "index_alias": self.index_name,
+                "query": {
+                    "match": {"value": query}
+                },
+                "collectors": [{"top_docs": {"limit": limit}}],
+                "is_fieldnorms_scoring_enabled": False,
+            }])
+            documents = list(map(lambda x: json.loads(x.document), response.collector_outputs[0].documents.scored_documents))
+            return documents
+
+    async def serve(self):
+        """
+        Start serving Summa
+        """
+        print(f"{colored('INFO', 'green')}: Setting up indices: {self.index_name}...")
+        async with self.geck:
+            print(f"{colored('INFO', 'green')}: Serving on {self.grpc_api_endpoint}")
+            while True:
+                await asyncio.sleep(5)
+
     async def create_ipfs_directory(
         self,
         output_car: str,
         query: str = None,
         limit: int = 100,
         name_template: str = '{id}.{extension}',
     ):
@@ -129,45 +157,46 @@
         print(f"{colored('INFO', 'green')}: Setting up indices: {self.index_name}...")
         async with self.geck as geck:
             return await geck.create_ipfs_directory(self.index_name, output_car, query, limit, name_template)
 
 
 async def stc_geck_cli(
     ipfs_http_base_url: str = 'http://127.0.0.1:8080',
+    ipfs_api_base_url: str = 'http://127.0.0.1:5001',
     ipfs_data_directory: str = '/ipns/standard-template-construct.org/data/',
     index_name: str = 'nexus_science',
     grpc_api_endpoint: str = '127.0.0.1:10082',
-    embed: bool = True,
-    timeout: int = 600,
+    timeout: int = 120,
     debug: bool = False,
 ):
     """
     :param ipfs_http_base_url: IPFS HTTP API Endpoint
     :param ipfs_data_directory: path to the directory with index
     :param index_name: `nexus_free` (non-classified content) or `nexus_science` (similar to Crossref)
     :param grpc_api_endpoint: port used for Summa
-    :param embed: setup embedded Summa server
     :param timeout: timeout for requests to IPFS
     :param debug: add debugging output
     :return:
     """
     logging.basicConfig(stream=sys.stdout, level=logging.INFO if debug else logging.ERROR)
     stc_geck_client = StcGeckCli(
         ipfs_http_base_url=ipfs_http_base_url,
+        ipfs_api_base_url=ipfs_api_base_url,
         ipfs_data_directory=ipfs_data_directory,
         index_name=index_name,
         grpc_api_endpoint=grpc_api_endpoint,
-        embed=embed,
         timeout=timeout,
     )
     return {
-        'search': stc_geck_client.search,
+        'create-ipfs-directory': stc_geck_client.create_ipfs_directory,
         'download': stc_geck_client.download,
         'documents': stc_geck_client.documents,
-        'create-ipfs-directory': stc_geck_client.create_ipfs_directory,
+        'random-cids': stc_geck_client.random_cids,
+        'search': stc_geck_client.search,
+        'serve': stc_geck_client.serve,
     }
 
 
 def main():
     fire.Fire(stc_geck_cli, name='geck')
```

### Comparing `stc-geck-1.3.1/stc_geck/client.py` & `stc-geck-1.3.2/stc_geck/client.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,20 +1,22 @@
+import json
 import logging
 import re
 import tempfile
 from typing import Tuple
 from urllib.parse import urlparse
 
 import aiohttp
 import orjson
 import summa_embed
 from aiokit import AioThing
 from aiosumma import SummaClient
-
-from .utils import create_car
+from izihawa_ipfs_api import IpfsApiClient, IpfsHttpClient
+from izihawa_utils.random import reservoir_sampling_async
+from utils import create_car, is_endpoint_listening
 
 
 def get_config():
     return {
         'debug': True,
         'api': {
             'http_endpoint': None,
@@ -28,75 +30,95 @@
             'doc_store_cache_num_blocks': 256,
             'indices': {},
             'writer_heap_size_bytes': 1073741824,
         }
     }
 
 
-def canonoize_base_url(endpoint):
-    endpoint = endpoint.rstrip('/')
-    if not endpoint.startswith('http'):
-        endpoint = 'http://' + endpoint
-    return endpoint
+def canonoize_base_url(base_url):
+    base_url = base_url.rstrip('/')
+    if not base_url.startswith('http'):
+        base_url = 'http://' + base_url
+    return base_url
 
 
 async def query_wrapper(response):
     for scored_document in response.collector_outputs[0].documents.scored_documents:
         yield orjson.loads(scored_document.document)
 
 
 async def load_document(documents):
     async for document in documents:
         document = orjson.loads(document)
         if 'cid' in document:
             yield document
 
 
+async def trace_iteration(iter, every_n, **kwargs):
+    i = 1
+    async for el in iter:
+        if i % every_n == 0:
+            logging.getLogger('statbox').info({
+                'c': i,
+                **kwargs
+            })
+        i += 1
+        yield el
+
+
 async def detect_host_header(url):
     async with aiohttp.ClientSession() as session:
         async with session.get(url, allow_redirects=False) as resp:
             if 300 <= resp.status < 400:
                 redirection_url = resp.headers['Location']
                 if 'localhost' in redirection_url:
                     parsed_url = urlparse(redirection_url)
                     return re.search(r'(.*)\.localhost.*', parsed_url.netloc).group(0)
 
 
 class StcGeck(AioThing):
     def __init__(
         self,
-        ipfs_http_base_url: str = 'http://localhost:8080',
+        ipfs_http_base_url: str = 'http://127.0.0.1:8080',
+        ipfs_api_base_url: str = 'http://127.0.0.1:5001',
         ipfs_data_directory: str = '/ipns/standard-template-construct.org/data',
         index_names: Tuple[str, ...] = ('nexus_science',),
         grpc_api_endpoint: str = '127.0.0.1:10082',
-        embed: bool = True,
+        timeout: int = 120,
     ):
         super().__init__()
         self.ipfs_http_base_url = canonoize_base_url(ipfs_http_base_url)
+        self.ipfs_http_client = IpfsHttpClient(self.ipfs_http_base_url, timeout=timeout)
+        self.starts.append(self.ipfs_http_client)
+        self.ipfs_api_client = IpfsApiClient(canonoize_base_url(ipfs_api_base_url), timeout=timeout)
+        self.starts.append(self.ipfs_api_client)
         self.ipfs_data_directory = '/' + ipfs_data_directory.strip('/') + '/'
         self.index_names = index_names
         self.grpc_api_endpoint = grpc_api_endpoint
-        self.embed = embed
+        self.is_embed = False
         self.summa_embed_server = None
         self.summa_client = SummaClient(
             endpoint=self.grpc_api_endpoint,
             max_message_length=2 * 1024 * 1024 * 1024 - 1,
         )
         self.temp_dir = None
 
     async def start(self):
         self.temp_dir = tempfile.TemporaryDirectory()
-        if self.embed:
+        if not is_endpoint_listening(self.grpc_api_endpoint):
+            logging.getLogger('info').info({'action': 'launching_embedded'})
+            self.is_embed = True
+
             server_config = get_config()
             server_config['api']['grpc_endpoint'] = self.grpc_api_endpoint
             server_config['data_path'] = self.temp_dir.name
             server_config['log_path'] = self.temp_dir.name
             for index_name in self.index_names:
                 query_parser_config = {
-                    'default_fields': ['abstract', 'title']
+                    'default_fields': ['abstract', 'content', 'title']
                 }
                 full_path = self.ipfs_http_base_url + self.ipfs_data_directory + index_name + '/'
                 headers_template = {'range': 'bytes={start}-{end}'}
                 remote_index_config = {'remote': {
                     'method': 'GET',
                     'url_template': f'{full_path}{{file_name}}',
                     'headers_template': headers_template,
@@ -119,32 +141,47 @@
             await self.summa_embed_server.stop()
             self.summa_embed_server = None
         self.temp_dir.cleanup()
 
     def get_summa_client(self):
         return self.summa_client
 
-    async def download(self, cid: str, timeout: int = 120):
-        async with aiohttp.ClientSession(timeout=aiohttp.ClientTimeout(total=timeout)) as session:
-            async with session.get(f'{self.ipfs_http_base_url}/ipfs/{cid}') as resp:
-                return await resp.read()
+    async def download(self, cid: str):
+        return await self.ipfs_http_client.get_item(cid)
+
+    async def random_cids(self, n: int = 1000):
+        items = await reservoir_sampling_async(
+            async_iterator=trace_iteration(
+                self.ipfs_api_client.ls_stream(
+                    '/ipns/hub.standard-template-construct.org',
+                    size=False,
+                    resolve_type=False,
+                ),
+                10000,
+                action='trace_listing_items',
+            ),
+            n=n
+        )
+        cids = []
+        for item in items:
+            item = json.loads(item)
+            link = item['Objects'][0]['Links'][0]
+            cids.append(link['Hash'])
+        return cids
 
     async def create_ipfs_directory(
         self,
         index_name: str,
         output_car: str,
         query: str = None,
         limit: int = 100,
         name_template: str = '{id}.{extension}',
     ):
-        if query and self.embed:
+        if query and self.is_embed:
             logging.getLogger('warning').warning('Too high limit for embedded Summa')
-        '''
-        All following conditions are introduced to mitigate performance issues.
-        '''
         if query:
             return await create_car(
                 output_car,
                 query_wrapper(await self.summa_client.search([{
                     'index_alias': index_name,
                     'collectors': [{'top_docs': {'limit': limit, 'scorer': {'order_by': 'issued_at'}}}],
                     'query': {'boolean': {'subqueries': [
```

### Comparing `stc-geck-1.3.1/stc_geck.egg-info/PKG-INFO` & `stc-geck-1.3.2/stc_geck.egg-info/PKG-INFO`

 * *Files 21% similar despite different names*

```diff
@@ -1,29 +1,39 @@
 Metadata-Version: 2.1
 Name: stc-geck
-Version: 1.3.1
+Version: 1.3.2
 Summary: GECK (Garden Of Eden Creation Kit) is a toolkit for setting up and maintaning STC
 Author: Interdimensional Walker
 Project-URL: Homepage, https://github.com/nexus-stc/stc
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 
 # GECK (Garden of Eden Creation Kit)
 
+GECK is a Python library and Bash tool for interacting with STC programmatically.
+It allows to startup embedded Summa instance, do search queries and iterate over database.
+
 ## Install
 
 ```bash
 pip install stc-geck
 ```
 
-## Usage
+## Examples
+
+### CLI
 
 ```bash
 # Iterate over all stored documents
-geck --ipfs-http-endpoint 127.0.0.1:8080 - documents
+geck --ipfs-http-base-url 127.0.0.1:8080 - documents
 
 # Do a match search by field
-geck --ipfs-http-endpoint 127.0.0.1:8080 - search doi:10.3384/ecp1392a41
+geck --ipfs-http-base-url 127.0.0.1:8080 - search doi:10.3384/ecp1392a41
+
 # Do a match search by word
-geck --ipfs-http-endpoint 127.0.0.1:8080 - search hemoglobin --limit 10
+geck --ipfs-http-base-url 127.0.0.1:8080 - search hemoglobin --limit 10
 ```
+
+### Python
+
+Examples for Python can be found in [examples directory](/geck/examples/search-stc.ipynb)
```

