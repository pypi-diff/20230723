# Comparing `tmp/rblx-open-cloud-1.3.1.tar.gz` & `tmp/rblx-open-cloud-1.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rblx-open-cloud-1.3.1.tar", last modified: Wed Jun  7 14:13:18 2023, max compression
+gzip compressed data, was "rblx-open-cloud-1.4.0.tar", last modified: Sun Jul 23 11:50:26 2023, max compression
```

## Comparing `rblx-open-cloud-1.3.1.tar` & `rblx-open-cloud-1.4.0.tar`

### file list

```diff
@@ -1,21 +1,22 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 14:13:18.474059 rblx-open-cloud-1.3.1/
--rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-06-07 14:13:02.000000 rblx-open-cloud-1.3.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     4019 2023-06-07 14:13:18.474059 rblx-open-cloud-1.3.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3668 2023-06-07 14:13:02.000000 rblx-open-cloud-1.3.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 14:13:18.470059 rblx-open-cloud-1.3.1/rblx_open_cloud.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4019 2023-06-07 14:13:18.000000 rblx-open-cloud-1.3.1/rblx_open_cloud.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      423 2023-06-07 14:13:18.000000 rblx-open-cloud-1.3.1/rblx_open_cloud.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-06-07 14:13:18.000000 rblx-open-cloud-1.3.1/rblx_open_cloud.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       26 2023-06-07 14:13:18.000000 rblx-open-cloud-1.3.1/rblx_open_cloud.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-06-07 14:13:18.000000 rblx-open-cloud-1.3.1/rblx_open_cloud.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-07 14:13:18.474059 rblx-open-cloud-1.3.1/rblxopencloud/
--rw-r--r--   0 runner    (1001) docker     (123)      286 2023-06-07 14:13:02.000000 rblx-open-cloud-1.3.1/rblxopencloud/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8153 2023-06-07 14:13:02.000000 rblx-open-cloud-1.3.1/rblxopencloud/creator.py
--rw-r--r--   0 runner    (1001) docker     (123)    29069 2023-06-07 14:13:02.000000 rblx-open-cloud-1.3.1/rblxopencloud/datastore.py
--rw-r--r--   0 runner    (1001) docker     (123)     1151 2023-06-07 14:13:02.000000 rblx-open-cloud-1.3.1/rblxopencloud/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     5409 2023-06-07 14:13:02.000000 rblx-open-cloud-1.3.1/rblxopencloud/experience.py
--rw-r--r--   0 runner    (1001) docker     (123)      329 2023-06-07 14:13:02.000000 rblx-open-cloud-1.3.1/rblxopencloud/group.py
--rw-r--r--   0 runner    (1001) docker     (123)    11769 2023-06-07 14:13:02.000000 rblx-open-cloud-1.3.1/rblxopencloud/oauth2.py
--rw-r--r--   0 runner    (1001) docker     (123)      598 2023-06-07 14:13:02.000000 rblx-open-cloud-1.3.1/rblxopencloud/user.py
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-06-07 14:13:18.474059 rblx-open-cloud-1.3.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      801 2023-06-07 14:13:02.000000 rblx-open-cloud-1.3.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:50:26.375072 rblx-open-cloud-1.4.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     4957 2023-07-23 11:50:26.371072 rblx-open-cloud-1.4.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4606 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:50:26.371072 rblx-open-cloud-1.4.0/rblx_open_cloud.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4957 2023-07-23 11:50:26.000000 rblx-open-cloud-1.4.0/rblx_open_cloud.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      448 2023-07-23 11:50:26.000000 rblx-open-cloud-1.4.0/rblx_open_cloud.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 11:50:26.000000 rblx-open-cloud-1.4.0/rblx_open_cloud.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       26 2023-07-23 11:50:26.000000 rblx-open-cloud-1.4.0/rblx_open_cloud.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-23 11:50:26.000000 rblx-open-cloud-1.4.0/rblx_open_cloud.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:50:26.371072 rblx-open-cloud-1.4.0/rblxopencloud/
+-rw-r--r--   0 runner    (1001) docker     (123)      404 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/rblxopencloud/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10465 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/rblxopencloud/creator.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33462 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/rblxopencloud/datastore.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1311 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/rblxopencloud/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8458 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/rblxopencloud/experience.py
+-rw-r--r--   0 runner    (1001) docker     (123)      675 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/rblxopencloud/group.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16489 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/rblxopencloud/oauth2.py
+-rw-r--r--   0 runner    (1001) docker     (123)      915 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/rblxopencloud/user.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6341 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/rblxopencloud/webhook.py
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 11:50:26.375072 rblx-open-cloud-1.4.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      801 2023-07-23 11:50:08.000000 rblx-open-cloud-1.4.0/setup.py
```

### Comparing `rblx-open-cloud-1.3.1/LICENSE` & `rblx-open-cloud-1.4.0/LICENSE`

 * *Files identical despite different names*

### Comparing `rblx-open-cloud-1.3.1/PKG-INFO` & `rblx-open-cloud-1.4.0/README.md`

 * *Files 10% similar despite different names*

```diff
@@ -1,21 +1,12 @@
-Metadata-Version: 2.1
-Name: rblx-open-cloud
-Version: 1.3.1
-Summary: API wrapper for Roblox Open Cloud
-Home-page: https://github.com/TreeBen77/rblx-open-cloud
-Author: TreeBen77
-License: MIT
-Keywords: roblox,open-cloud,data-store,place-publishing,mesageing-service
-Requires-Python: >=3.9.0
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
 # rblx-open-cloud
- 
+[![Discord Server](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdiscord.com%2Fapi%2Fv10%2Finvites%2F4CSc9E5uQy%3Fwith_counts%3Dtrue&query=%24.approximate_member_count&suffix=%20members&style=for-the-badge&logo=discord&logoColor=white&label=Discord%20Server&labelColor=%235865F2&color=%23353535)](https://discord.gg/4CSc9E5uQy)
+[![DevForum Post](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdevforum.roblox.com%2Ft%2Frblx-open-cloud-roblox-open-cloud-wrapper-for-python%2F1991959%2F1.json&query=%24.like_count&suffix=%20likes&style=for-the-badge&logo=robloxstudio&logoColor=white&label=DevForum%20Post&labelColor=%23009fff&color=%23353535&cacheSeconds=86400)](https://devforum.roblox.com/t/1991959)
+[![Downloads](https://img.shields.io/pypi/dm/rblx-open-cloud?style=for-the-badge&logo=pypi&logoColor=white&label=PyPi%20Downloads&labelColor=%23006dad&color=%23353535)](https://pypi.org/project/rblx-open-cloud)
+
 Python API wrapper for [Roblox Open Cloud](https://create.roblox.com/docs/open-cloud/index), it currently has 100% API coverage and I plan to add all new Open Cloud additions to the library.
 
 **Documentation: https://rblx-open-cloud.readthedocs.io**
 
 **Devforum Post: https://devforum.roblox.com/t/1991959**
 
 **Discord Server: https://discord.gg/gEBdHNAR46**
```

### Comparing `rblx-open-cloud-1.3.1/README.md` & `rblx-open-cloud-1.4.0/PKG-INFO`

 * *Files 27% similar despite different names*

```diff
@@ -1,9 +1,24 @@
+Metadata-Version: 2.1
+Name: rblx-open-cloud
+Version: 1.4.0
+Summary: API wrapper for Roblox Open Cloud
+Home-page: https://github.com/TreeBen77/rblx-open-cloud
+Author: TreeBen77
+License: MIT
+Keywords: roblox,open-cloud,data-store,place-publishing,mesageing-service
+Requires-Python: >=3.9.0
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
 # rblx-open-cloud
- 
+[![Discord Server](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdiscord.com%2Fapi%2Fv10%2Finvites%2F4CSc9E5uQy%3Fwith_counts%3Dtrue&query=%24.approximate_member_count&suffix=%20members&style=for-the-badge&logo=discord&logoColor=white&label=Discord%20Server&labelColor=%235865F2&color=%23353535)](https://discord.gg/4CSc9E5uQy)
+[![DevForum Post](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdevforum.roblox.com%2Ft%2Frblx-open-cloud-roblox-open-cloud-wrapper-for-python%2F1991959%2F1.json&query=%24.like_count&suffix=%20likes&style=for-the-badge&logo=robloxstudio&logoColor=white&label=DevForum%20Post&labelColor=%23009fff&color=%23353535&cacheSeconds=86400)](https://devforum.roblox.com/t/1991959)
+[![Downloads](https://img.shields.io/pypi/dm/rblx-open-cloud?style=for-the-badge&logo=pypi&logoColor=white&label=PyPi%20Downloads&labelColor=%23006dad&color=%23353535)](https://pypi.org/project/rblx-open-cloud)
+
 Python API wrapper for [Roblox Open Cloud](https://create.roblox.com/docs/open-cloud/index), it currently has 100% API coverage and I plan to add all new Open Cloud additions to the library.
 
 **Documentation: https://rblx-open-cloud.readthedocs.io**
 
 **Devforum Post: https://devforum.roblox.com/t/1991959**
 
 **Discord Server: https://discord.gg/gEBdHNAR46**
```

### Comparing `rblx-open-cloud-1.3.1/rblx_open_cloud.egg-info/PKG-INFO` & `rblx-open-cloud-1.4.0/rblx_open_cloud.egg-info/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,21 +1,24 @@
 Metadata-Version: 2.1
 Name: rblx-open-cloud
-Version: 1.3.1
+Version: 1.4.0
 Summary: API wrapper for Roblox Open Cloud
 Home-page: https://github.com/TreeBen77/rblx-open-cloud
 Author: TreeBen77
 License: MIT
 Keywords: roblox,open-cloud,data-store,place-publishing,mesageing-service
 Requires-Python: >=3.9.0
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # rblx-open-cloud
- 
+[![Discord Server](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdiscord.com%2Fapi%2Fv10%2Finvites%2F4CSc9E5uQy%3Fwith_counts%3Dtrue&query=%24.approximate_member_count&suffix=%20members&style=for-the-badge&logo=discord&logoColor=white&label=Discord%20Server&labelColor=%235865F2&color=%23353535)](https://discord.gg/4CSc9E5uQy)
+[![DevForum Post](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdevforum.roblox.com%2Ft%2Frblx-open-cloud-roblox-open-cloud-wrapper-for-python%2F1991959%2F1.json&query=%24.like_count&suffix=%20likes&style=for-the-badge&logo=robloxstudio&logoColor=white&label=DevForum%20Post&labelColor=%23009fff&color=%23353535&cacheSeconds=86400)](https://devforum.roblox.com/t/1991959)
+[![Downloads](https://img.shields.io/pypi/dm/rblx-open-cloud?style=for-the-badge&logo=pypi&logoColor=white&label=PyPi%20Downloads&labelColor=%23006dad&color=%23353535)](https://pypi.org/project/rblx-open-cloud)
+
 Python API wrapper for [Roblox Open Cloud](https://create.roblox.com/docs/open-cloud/index), it currently has 100% API coverage and I plan to add all new Open Cloud additions to the library.
 
 **Documentation: https://rblx-open-cloud.readthedocs.io**
 
 **Devforum Post: https://devforum.roblox.com/t/1991959**
 
 **Discord Server: https://discord.gg/gEBdHNAR46**
```

### Comparing `rblx-open-cloud-1.3.1/rblxopencloud/datastore.py` & `rblx-open-cloud-1.4.0/rblxopencloud/datastore.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from .exceptions import rblx_opencloudException, InvalidKey, NotFound, RateLimited, ServiceUnavailable, PreconditionFailed
 import requests, json, datetime
 import base64, hashlib, urllib.parse
 from typing import Union, Optional, Iterable, TYPE_CHECKING
+from . import user_agent
 
 if TYPE_CHECKING:
     from .experience import Experience
 
 if TYPE_CHECKING:
     from .experience import Experience
 
@@ -15,25 +16,31 @@
     "ListedEntry",
     "DataStore",
     "SortedEntry",
     "OrderedDataStore"
 )
 
 class EntryInfo():
+    """
+    Contains data about an entry such as version ID, timestamps, users and metadata.
+    """
     def __init__(self, version, created, updated, users, metadata) -> None:
         self.version: str = version
         self.created: datetime.date = datetime.datetime.fromisoformat((created.split("Z")[0]+"0"*6)[0:26])
         self.updated: datetime.date = datetime.datetime.fromisoformat((updated.split("Z")[0]+"0"*6)[0:26])
         self.users: list[int] = users
         self.metadata: dict = metadata
     
     def __repr__(self) -> str:
         return f"rblxopencloud.EntryInfo(\"{self.version}\", users={self.users}, metadata={self.metadata})"
 
 class EntryVersion():
+    """
+    Contains data about a version such as it's ID, timestamps, content length and wether this version is deleted.
+    """
     def __init__(self, version, deleted, content_length, created, key_created, datastore, key, scope) -> None:
         self.version: str = version
         self.deleted: bool = deleted
         self.content_length: int = content_length
         self.created: datetime.datetime = datetime.datetime.fromisoformat((created.split("Z")[0]+"0"*6)[0:26])
         self.key_created: datetime.datetime = datetime.datetime.fromisoformat((key_created.split("Z")[0]+"0"*6)[0:26])
         self.__datastore = datastore
@@ -52,27 +59,34 @@
         else:
             return self.__datastore.get_version(f"{self.__scope}/{self.__key}", self.version)
 
     def __repr__(self) -> str:
         return f"rblxopencloud.EntryVersion(\"{self.version}\", content_length={self.content_length})"
 
 class ListedEntry():
+    """
+    Object which contains an entry's key and scope.
+    """
     def __init__(self, key, scope) -> None:
         self.key: str = key
         self.scope: str = scope
     
     def __eq__(self, object) -> bool:
         if not isinstance(object, ListedEntry):
             return NotImplemented
         return self.key == object.key and self.scope == object.scope
     
     def __repr__(self) -> str:
         return f"rblxopencloud.ListedEntry(\"{self.key}\", scope=\"{self.scope}\")"
 
 class DataStore():
+    """
+    Represents a regular data store in an experience.
+    """
+
     def __init__(self, name, experience, api_key, created, scope):
         self.name: str = name
         self.__api_key: str = api_key
         self.scope: str = scope
         self.experience: Experience = experience
         if created: self.created = datetime.datetime.fromisoformat((created.split("Z")[0]+"0"*6)[0:26])
         else: self.created = None
@@ -80,31 +94,38 @@
     def __repr__(self) -> str:
         return f"rblxopencloud.DataStore(\"{self.name}\", scope=\"{self.scope}\", universe={repr(self.experience)})"
     
     def __str__(self) -> str:
         return self.name
 
     def list_keys(self, prefix: str="", limit: Optional[int]=None) -> Iterable[ListedEntry]:
-        """Returns an `Iterable` of keys in the database and scope, optionally matching a prefix. Will return keys from all scopes if `DataStore.scope` is `None`. The example below would list all versions, along with their value.
+        """
+        Returns an Iterable of keys in the database and scope, optionally matching a prefix. Will return keys from all scopes if :attr:`scope` is ``None``.
+
+        The example below would list all keys, along with their scope.
                 
         ```py
             for key in datastore.list_keys():
                 print(key.key, key.scope)
         ```
 
         You can simply convert it to a list by putting it in the list function:
 
         ```py
             list(datastore.list_versions())
-        ```"""
+        ### Parameters
+        prefix: str - Only return keys that start with this prefix.
+        limit: Optional[int] - Will not return more keys than this number. Set to `None` for no limit.
+        ```
+        """
         nextcursor = ""
         yields = 0
         while limit == None or yields < limit:
             response = requests.get(f"https://apis.roblox.com/datastores/v1/universes/{self.experience.id}/standard-datastores/datastore/entries",
-                headers={"x-api-key": self.__api_key}, params={
+                headers={"x-api-key": self.__api_key, "user-agent": user_agent}, params={
                 "datastoreName": self.name,
                 "scope": self.scope,
                 "AllScopes": not self.scope,
                 "prefix": prefix,
                 "cursor": nextcursor if nextcursor else None
             })
             if response.status_code == 400: raise rblx_opencloudException(response.json()["message"])
@@ -120,22 +141,26 @@
                 yields += 1
                 yield ListedEntry(key["key"], key["scope"])
                 if limit != None and yields >= limit: break
             nextcursor = data.get("nextPageCursor")
             if not nextcursor: break
     
     def get(self, key: str) -> tuple[Union[str, dict, list, int, float], EntryInfo]:
-        """Gets the value of a key. If `DataStore.scope` is `None` then `key` must be formatted like `scope/key`."""
+        """
+        Gets the value of a key.
+        ### Parameters
+        key: str - The key to find. When `DataStore.scope` is `None`, this must include the scope like this `scope/key`
+        """
         try:
             scope = self.scope
             if not scope: scope, key = key.split("/", maxsplit=1)
         except(ValueError):
             raise ValueError("a scope and key seperated by a forward slash is required for DataStore without a scope.")
         response = requests.get(f"https://apis.roblox.com/datastores/v1/universes/{self.experience.id}/standard-datastores/datastore/entries/entry",
-            headers={"x-api-key": self.__api_key}, params={
+            headers={"x-api-key": self.__api_key, "user-agent": user_agent}, params={
                 "datastoreName": self.name,
                 "scope": scope,
                 "entryKey": key
             })
 
         if response.status_code == 200:
             try: metadata = json.loads(response.headers["roblox-entry-attributes"])
@@ -150,26 +175,35 @@
         elif response.status_code == 403: raise InvalidKey(response.json()["message"])
         elif response.status_code == 404: raise NotFound(response.json()["message"])
         elif response.status_code == 429: raise RateLimited(response.json()["message"])
         elif response.status_code >= 500: raise ServiceUnavailable(f"Internal Server Error: '{response.text}'")
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}: '{response.text}'")
 
     def set(self, key: str, value: Union[str, dict, list, int, float], users:Optional[list[int]]=None, metadata:dict={}, exclusive_create:bool=False, previous_version:Optional[str]=None) -> EntryVersion:
-        """Sets the value of a key. If `DataStore.scope` is `None` then `key` must be formatted like `scope/key`."""
+        """
+        Sets the value of a key.
+        ### Parameters
+        key: str - The key to find. When `DataStore.scope` is `None`, this must include the scope like this `scope/key`
+        value: Union[str, dict, list, int, float] - The new value
+        users: list[int] - a list of Roblox user IDs to attach to the entry to assist with GDPR tracking/removal.
+        metadata: dict - a dictionary, just like the lua equivalent [DataStoreSetOptions:SetMetadata()](https://create.roblox.com/docs/reference/engine/classes/DataStoreSetOptions#SetMetadata)
+        exclusive_create: bool - whether to update the entry if it already has a value. Raises `rblx-open-cloud.PreconditionFailed` if it has a value.
+        previous_version: Optional[str] don't update if the current version is not this value. Raises `rblx-open-cloud.PreconditionFailed` if it has a value.
+        """
         if previous_version and exclusive_create: raise ValueError("previous_version and exclusive_create can not both be set")
         try:
             scope = self.scope
             if not scope: scope, key = key.split("/", maxsplit=1)
         except(ValueError):
             raise ValueError("a scope and key seperated by a forward slash is required for DataStore without a scope.")
         if users == None: users = []
         data = json.dumps(value)
 
         response = requests.post(f"https://apis.roblox.com/datastores/v1/universes/{self.experience.id}/standard-datastores/datastore/entries/entry",
-            headers={"x-api-key": self.__api_key, "roblox-entry-userids": json.dumps(users), "roblox-entry-attributes": json.dumps(metadata),
+            headers={"x-api-key": self.__api_key, "user-agent": user_agent, "roblox-entry-userids": json.dumps(users), "roblox-entry-attributes": json.dumps(metadata),
             "content-md5": base64.b64encode(hashlib.md5(data.encode()).digest())}, data=data, params={
                 "datastoreName": self.name,
                 "scope": scope,
                 "entryKey": key,
                 "exclusiveCreate": exclusive_create,
                 "matchVersion": previous_version
             })
@@ -197,24 +231,31 @@
                 error = "A Precondition Failed"
 
             raise PreconditionFailed(json.loads(response.text), EntryInfo(response.headers["roblox-entry-version"], response.headers["roblox-entry-created-time"],
     response.headers["roblox-entry-version-created-time"], userids, metadata), error)
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}: '{response.text}'")
 
     def increment(self, key: str, increment: Union[int, float], users:Optional[list[int]]=None, metadata:dict={}) -> tuple[Union[str, dict, list, int, float], EntryInfo]:
-        """Increments the value of a key. If `DataStore.scope` is `None` then `key` must be formatted like `scope/key`."""
+        """
+        Increments the value of a key.
+        # Parameters
+        key: The key to increment.
+        value: Union[int, float] - The number to increase the value by, use negative numbers to decrease it.
+        users: list[int] - a list of Roblox user IDs to attach to the entry to assist with GDPR tracking/removal.
+        metadata: dict - a dictionary of user-defind metadata, just like the lua equivalent [DataStoreSetOptions:SetMetadata()](https://create.roblox.com/docs/reference/engine/classes/DataStoreSetOptions#SetMetadata)
+        """
         try:
             scope = self.scope
             if not scope: scope, key = key.split("/", maxsplit=1)
         except(ValueError):
             raise ValueError("a scope and key seperated by a forward slash is required for DataStore without a scope.")
         if users == None: users = []
 
         response = requests.post(f"https://apis.roblox.com/datastores/v1/universes/{self.experience.id}/standard-datastores/datastore/entries/entry/increment",
-            headers={"x-api-key": self.__api_key, "roblox-entry-userids": json.dumps(users), "roblox-entry-attributes": json.dumps(metadata)}, params={
+            headers={"x-api-key": self.__api_key, "user-agent": user_agent, "roblox-entry-userids": json.dumps(users), "roblox-entry-attributes": json.dumps(metadata)}, params={
                 "datastoreName": self.name,
                 "scope": scope,
                 "entryKey": key,
                 "incrementBy": increment
             })
 
         if response.status_code == 200:
@@ -230,22 +271,26 @@
         elif response.status_code == 403: raise InvalidKey(response.json()["message"])
         elif response.status_code == 404: raise NotFound(response.json()["message"])
         elif response.status_code == 429: raise RateLimited(response.json()["message"])
         elif response.status_code >= 500: raise ServiceUnavailable(f"Internal Server Error: '{response.text}'")
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}: '{response.text}'")
     
     def remove(self, key: str) -> None:
-        """Removes a key. If `DataStore.scope` is `None` then `key` must be formatted like `scope/key`."""
+        """
+        Removes a key.
+        ### Parameters
+        key: str - The key to remove.
+        """
         try:
             scope = self.scope
             if not scope: scope, key = key.split("/", maxsplit=1)
         except(ValueError):
             raise ValueError("a scope and key seperated by a forward slash is required for DataStore without a scope.")
         response = requests.delete(f"https://apis.roblox.com/datastores/v1/universes/{self.experience.id}/standard-datastores/datastore/entries/entry",
-            headers={"x-api-key": self.__api_key}, params={
+            headers={"x-api-key": self.__api_key, "user-agent": user_agent}, params={
                 "datastoreName": self.name,
                 "scope": scope,
                 "entryKey": key
             })
 
         if response.status_code == 204: return None
         elif response.status_code == 400: raise rblx_opencloudException(response.json()["message"])
@@ -264,25 +309,32 @@
                 print(version, version.get_value())
         ```
 
         You can simply convert it to a list by putting it in the list function:
 
         ```py
             list(datastore.list_versions("key-name"))
-        ```"""
+        ```
+        ### Parameters
+        key: The key to find versions for.
+        after: datetime.datetime - Only find versions after this datetime
+        before: datetime.datetime - Only find versions before this datetime
+        limit: Optional[int] - Will not return more versions than this number. Set to `None` for no limit.
+        descending: bool - Wether the versions should be sorted by date ascending or descending.
+        """
         try:
             scope = self.scope
             if not scope: scope, key = key.split("/", maxsplit=1)
         except(ValueError):
             raise ValueError("a scope and key seperated by a forward slash is required for DataStore without a scope.")
         nextcursor = ""
         yields = 0
         while limit == None or yields < limit:
             response = requests.get(f"https://apis.roblox.com/datastores/v1/universes/{self.experience.id}/standard-datastores/datastore/entries/entry/versions",
-                headers={"x-api-key": self.__api_key}, params={
+                headers={"x-api-key": self.__api_key, "user-agent": user_agent}, params={
                     "datastoreName": self.name,
                     "scope": scope,
                     "entryKey": key,
                     "sortOrder": "Descending" if descending else "Ascending",
                     "cursor": nextcursor if nextcursor else None,
                     "startTime": after.isoformat() if after else None,
                     "endTime": before.isoformat() if before else None
@@ -301,22 +353,27 @@
                 yields += 1
                 yield EntryVersion(version["version"], version["deleted"], version["contentLength"], version["createdTime"], version["objectCreatedTime"], self, key, self.scope if self.scope else scope)
                 if limit == None or yields >= limit: break
             nextcursor = data.get("nextPageCursor")
             if not nextcursor: break
 
     def get_version(self, key: str, version: str) -> tuple[Union[str, dict, list, int, float], EntryInfo]:
-        """Gets the value of a key version. If `DataStore.scope` is `None` then `key` must be formatted like `scope/key`."""
+        """
+        Gets the value of a key version.
+        
+        key: str - The key to find.
+        version: str - The version ID to get.
+        """
         try:
             scope = self.scope
             if not scope: scope, key = key.split("/", maxsplit=1)
         except(ValueError):
             raise ValueError("a scope and key seperated by a forward slash is required for DataStore without a scope.") 
         response = requests.get(f"https://apis.roblox.com/datastores/v1/universes/{self.experience.id}/standard-datastores/datastore/entries/entry/versions/version",
-            headers={"x-api-key": self.__api_key}, params={
+            headers={"x-api-key": self.__api_key, "user-agent": user_agent}, params={
                 "datastoreName": self.name,
                 "scope": scope,
                 "entryKey": key,
                 "versionId": version
             })
 
         if response.status_code == 200:
@@ -336,56 +393,84 @@
         elif response.status_code == 403: raise InvalidKey(response.json()["message"])
         elif response.status_code == 404: raise NotFound(response.json()["message"])
         elif response.status_code == 429: raise RateLimited(response.json()["message"])
         elif response.status_code >= 500: raise ServiceUnavailable(f"Internal Server Error: '{response.text}'")
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}: '{response.text}'")
 
 class SortedEntry():
+    """
+    Object which contains a sorted entry's key, scope, and value.
+    """
     def __init__(self, key: str, value: int, scope: str="global") -> None:
         self.key: str = key
         self.scope: str = scope
         self.value: int = value
     
     def __eq__(self, object) -> bool:
         if not isinstance(object, SortedEntry):
             return NotImplemented
         return self.key == object.key and self.scope == object.scope and self.value == object.value
     
     def __repr__(self) -> str:
         return f"rblxopencloud.SortedEntry(\"{self.key}\", value={self.value})"
 
 class OrderedDataStore():
+    """
+    Class for interacting with the Ordered DataStore API for a specific Ordered DataStore.
+    """
+
     def __init__(self, name, experince, api_key, scope):
         self.name = name
         self.__api_key = api_key
         self.scope = scope
         self.experince = experince
     
     def __repr__(self) -> str:
         return f"rblxopencloud.OrderedDataStore(\"{self.name}\", scope=\"{self.scope}\", experince={repr(self.experince)})"
     
     def __str__(self) -> str:
         return self.name
     
     def sort_keys(self, descending: bool=True, limit: Union[None, int]=None, min=None, max=None) -> Iterable[SortedEntry]:
+        """
+        Returns a list of keys and their values.
+
+        The example below would list all keys, along with their value.
+                
+        ```py
+            for key in datastore.sort_keys():
+                print(key.name, key.value)
+        ```
+
+        You can simply convert it to a list by putting it in the list function:
+
+        ```py
+            list(datastore.sort_keys())
+        ```
+        ### Parameters
+        descending: bool - Wether the largest number should be first, or the smallest.
+        limit: int - Max number of entries to loop through.
+        min: int - Minimum entry value to retrieve
+        max: int - Maximum entry value to retrieve.
+        """
         if not self.scope: raise ValueError("A scope is required to list keys on OrderedDataStore.")
 
         filter = None
         if min and max:
             if min > max: raise ValueError("min must not be greater than max.")
             filter = f"entry >= {min} && entry <= {max}"
 
         if min: filter = f"entry >= {min}"
         if max: filter = f"entry <= {max}"
 
         nextcursor = ""
         yields = 0
         while limit == None or yields < limit:
             response = requests.get(f"https://apis.roblox.com/ordered-data-stores/v1/universes/{self.experince.id}/orderedDataStores/{urllib.parse.quote(self.name)}/scopes/{urllib.parse.quote(self.scope)}/entries",
-                headers={"x-api-key": self.__api_key}, params={
+                headers={"x-api-key": self.__api_key, "user-agent": user_agent}, params={
                 "max_page_size": limit if limit and limit < 100 else 100,
                 "order_by": "desc" if descending else None,
                 "page_token": nextcursor if nextcursor else None,
                 "filter": filter
             })
 
             if response.status_code == 400: raise rblx_opencloudException(response.json()["message"])
@@ -401,46 +486,59 @@
                 yields += 1
                 yield SortedEntry(key["id"], key["value"], self.scope)
                 if limit != None and yields >= limit: break
             nextcursor = data.get("nextPageToken")
             if not nextcursor: break
     
     def get(self, key: str) -> int:
+        """
+        Gets the value of a key.
+        ### Parameters
+        key: str - The key to find.
+        """
         try:
             if not self.scope: scope, key = key.split("/", maxsplit=1)
             else: scope = self.scope
         except(ValueError): raise ValueError("a scope and key seperated by a forward slash is required for OrderedDataStore without a scope.")
 
         response = requests.get(f"https://apis.roblox.com/ordered-data-stores/v1/universes/{self.experince.id}/orderedDataStores/{urllib.parse.quote(self.name)}/scopes/{urllib.parse.quote(scope)}/entries/{urllib.parse.quote(key)}",
-            headers={"x-api-key": self.__api_key})
+            headers={"x-api-key": self.__api_key, "user-agent": user_agent})
         
         if response.status_code == 200: return int(response.json()["value"])
         elif response.status_code == 400: raise rblx_opencloudException(response.json()["message"])
         elif response.status_code == 401: raise InvalidKey(response.text)
         elif response.status_code == 403: raise InvalidKey(response.json()["message"])
         elif response.status_code == 404: raise NotFound(response.json()["message"])
         elif response.status_code == 429: raise RateLimited(response.json()["message"])
         elif response.status_code >= 500: raise ServiceUnavailable(f"Internal Server Error: '{response.text}'")
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}: '{response.text}'")
         
     def set(self, key: str, value: int, exclusive_create: bool=False, exclusive_update: bool=False) -> int:
+        """
+        Sets the value of a key.
+        ### Parameters
+        key: str - The key to create/update.
+        value: int - The new integer value. Must be positive.
+        exclusive_create: - bool Wether to fail if the key already has a value.
+        exclusive_update: - bool Wether to fail if the key does not have a value.
+        """
         try:
             if not self.scope: scope, key = key.split("/", maxsplit=1)
             else: scope = self.scope
         except(ValueError): raise ValueError("a scope and key seperated by a forward slash is required for OrderedDataStore without a scope.")
         if exclusive_create and exclusive_update: raise ValueError("exclusive_create and exclusive_updated can not both be True")
 
         if not exclusive_create:
             response = requests.patch(f"https://apis.roblox.com/ordered-data-stores/v1/universes/{self.experince.id}/orderedDatastores/{urllib.parse.quote(self.name)}/scopes/{urllib.parse.quote(scope)}/entries/{urllib.parse.quote(key)}",
-                headers={"x-api-key": self.__api_key}, params={"allow_missing": not exclusive_update}, json={
+                headers={"x-api-key": self.__api_key, "user-agent": user_agent}, params={"allow_missing": not exclusive_update}, json={
                     "value": value
                 })
         else:
             response = requests.post(f"https://apis.roblox.com/ordered-data-stores/v1/universes/{self.experince.id}/orderedDatastores/{urllib.parse.quote(self.name)}/scopes/{urllib.parse.quote(scope)}/entries",
-                headers={"x-api-key": self.__api_key}, params={"id": key}, json={
+                headers={"x-api-key": self.__api_key, "user-agent": user_agent}, params={"id": key}, json={
                     "value": value
                 })
         
         if response.status_code == 200: return int(response.json()["value"])
         elif response.status_code == 400:
             if response.json()["message"] == "Entry already exists.":
                 raise PreconditionFailed(None, None, response.json()["message"])
@@ -450,40 +548,52 @@
         elif response.status_code == 403: raise InvalidKey(response.json()["message"])
         elif response.status_code == 404 and exclusive_update and response.json()["code"] == "NOT_FOUND": raise PreconditionFailed(response.json()["message"])
         elif response.status_code == 429: raise RateLimited(response.json()["message"])
         elif response.status_code >= 500: raise ServiceUnavailable(f"Internal Server Error: '{response.text}'")
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}: '{response.text}'")
 
     def increment(self, key: str, increment: int) -> None:
+        """
+        Increments the value of a key.
+        ### Parameters
+        key: str - The key to increment.
+        increment: int - The amount to increment the key by. You can use negative numbers to decrease the value.
+        """
         try:
             if not self.scope: scope, key = key.split("/", maxsplit=1)
             else: scope = self.scope
         except(ValueError): raise ValueError("a scope and key seperated by a forward slash is required for OrderedDataStore without a scope.")
 
         response = requests.post(f"https://apis.roblox.com/ordered-data-stores/v1/universes/{self.experince.id}/orderedDatastores/{urllib.parse.quote(self.name)}/scopes/{urllib.parse.quote(scope)}/entries/{urllib.parse.quote(key)}:increment",
-            headers={"x-api-key": self.__api_key}, json={
+            headers={"x-api-key": self.__api_key, "user-agent": user_agent}, json={
                 "amount": increment
             })
         
         if response.status_code == 200: return int(response.json()["value"])
         elif response.status_code == 401: raise InvalidKey("Your key may have expired, or may not have permission to access this resource.")
         elif response.status_code == 404: raise NotFound(f"The key {key} does not exist.")
         elif response.status_code == 409 and response.json()["message"] == "Entry value outside of bounds.": raise ValueError("New value can't be less than 0.")
         elif response.status_code == 429: raise RateLimited("You're being rate limited.")
         elif response.status_code >= 500: raise ServiceUnavailable("The service is unavailable or has encountered an error.")
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}")
 
     def remove(self, key: str) -> None:
+        """
+        Removes a key.
+        ### Parameters
+        key: str - The key to remove.
+        """
+
         try:
             if not self.scope: scope, key = key.split("/", maxsplit=1)
             else: scope = self.scope
         except(ValueError): raise ValueError("a scope and key seperated by a forward slash is required for OrderedDataStore without a scope.")
 
         response = requests.delete(f"https://apis.roblox.com/ordered-data-stores/v1/universes/{self.experince.id}/orderedDatastores/{urllib.parse.quote(self.name)}/scopes/{urllib.parse.quote(scope)}/entries/{urllib.parse.quote(key)}",
-            headers={"x-api-key": self.__api_key})
+            headers={"x-api-key": self.__api_key, "user-agent": user_agent})
         
         if response.status_code in [200, 204]: return None
         elif response.status_code == 400: raise rblx_opencloudException(response.json()["message"])
         elif response.status_code == 401: raise InvalidKey(response.text)
         elif response.status_code == 403: raise InvalidKey(response.json()["message"])
         elif response.status_code == 404: raise NotFound(response.json()["message"])
         elif response.status_code == 429: raise RateLimited(response.json()["message"])
```

### Comparing `rblx-open-cloud-1.3.1/rblxopencloud/exceptions.py` & `rblx-open-cloud-1.4.0/rblxopencloud/exceptions.py`

 * *Files 13% similar despite different names*

```diff
@@ -9,15 +9,17 @@
     "InvalidKey",
     "RateLimited",
     "ServiceUnavailable",
     "PreconditionFailed",
     "InsufficientScope",
     "InvalidAsset",
     "InvalidCode",
-    "ModeratedText"
+    "ModeratedText",
+    "UnknownEventType",
+    "UnhandledEventType"
 )
 
 class rblx_opencloudException(Exception): pass
 class NotFound(rblx_opencloudException): pass
 class InvalidKey(rblx_opencloudException): pass
 class RateLimited(rblx_opencloudException): pass
 class ServiceUnavailable(rblx_opencloudException): pass
@@ -29,7 +31,9 @@
 class InsufficientScope(InvalidKey):
     def __init__(self, scope, *args: object) -> None:
         self.required_scope: str = scope
         super().__init__(*args)
 class InvalidCode(InvalidKey): pass
 class InvalidAsset(rblx_opencloudException): pass
 class ModeratedText(rblx_opencloudException): pass
+class UnknownEventType(rblx_opencloudException): pass
+class UnhandledEventType(rblx_opencloudException): pass
```

### Comparing `rblx-open-cloud-1.3.1/rblxopencloud/oauth2.py` & `rblx-open-cloud-1.4.0/rblxopencloud/oauth2.py`

 * *Files 24% similar despite different names*

```diff
@@ -5,54 +5,72 @@
 from .user import User
 from .group import Group
 from .experience import Experience
 import requests, base64, jwt
 from cryptography.hazmat.primitives.asymmetric import ec
 from cryptography.hazmat.primitives.serialization import Encoding, PublicFormat, load_der_public_key
 from cryptography.hazmat.backends import default_backend
+import hashlib, string, secrets
+from . import user_agent
 
 __all__ = (
     "OAuth2App",
     "AccessToken",
     "PartialAccessToken",
     "AccessTokenInfo"
 )
 
 class AccessTokenInfo():
+    """
+    Object that contains information about a access token. 
+    """
+
     def __init__(self, data: dict):
         self.active: bool = data["active"]
         self.id: str = data["jti"]
         self.client_id: int = int(data["client_id"])
         self.user_id: int = data["sub"]
         self.scope: list[str] = data["scope"].split(" ")
         self.expires_at: datetime.datetime = datetime.datetime.fromtimestamp(data["exp"])
         self.issued_at: datetime.datetime = datetime.datetime.fromtimestamp(data["iat"])
     
     def __repr__(self) -> str:
-        return f"rblxopencloud.AccessTokenInfo(id={self.id}, user_id={self.user_id})"
+        return f"rblxopencloud.AccessTokenInfo(id=\"{self.id}\", user_id={self.user_id})"
 
 class Resources():
+    """
+    Object that contains all the authorized objects users, groups, and experiences.
+    """
+
     def __init__(self, experiences, accounts):
         self.experiences: list[Experience] = experiences
         self.accounts: list[Union[User, Group]] = accounts
     
     def __repr__(self) -> str:
         return f"rblxopencloud.Resources(experiences={self.experiences}, accounts={self.accounts})"
 
 class PartialAccessToken():
+    """
+    Represents a partial access via OAuth2 consent. It allows access to all resources authorized by the user, but not other information like the refresh token.
+    """
+
     def __init__(self, app, access_token) -> None:
         self.app: OAuth2App = app
         self.token: str = access_token
     
     def __repr__(self) -> str:
-        return f"rblxopencloud.PartialAccessToken(token={self.token[:15]}...)"
+        return f"rblxopencloud.PartialAccessToken(token=\"{self.token[:15]}...\")"
 
     def fetch_userinfo(self) -> User:
+        """
+        Returns a `rblx-open-cloud.User` object for this authorization. You can use this object to directly access user resources (like uploading files), if it was authorized.
+        """
+
         response = requests.get("https://apis.roblox.com/oauth/v1/userinfo", headers={
-            "authorization": f"Bearer {self.token}"
+            "authorization": f"Bearer {self.token}", "user-agent": user_agent
         })
         user = User(response.json().get("id") or response.json().get("sub"), f"Bearer {self.token}")
         user.username: str = response.json().get("preferred_username")
         user.display_name: str = response.json().get("nickname")
         user.created_at: datetime.datetime = datetime.datetime.fromtimestamp(response.json()["created_at"]) if response.json().get("created_at") else None
 
         if response.ok: return user
@@ -60,19 +78,23 @@
             if response.json()["error"] == "insufficient_scope":
                 raise InsufficientScope(response.json()["scope"], f"The access token does not have the required scope:'{response.json()['scope']}'")
             raise InvalidKey("The key has expired, been revoked or is invalid.")
         elif response.status_code >= 500: raise ServiceUnavailable("The service is unavailable or has encountered an error.")
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}")
     
     def fetch_resources(self) -> Resources:
+        """
+        Fetches the authorized accounts (users and groups), and experiences.
+        """
+
         response = requests.post("https://apis.roblox.com/oauth/v1/token/resources", data={
             "token": self.token,
             "client_id": self.app.id,
             "client_secret": self.app._OAuth2App__secret
-        })
+        }, headers={"user-agent": user_agent})
 
         if response.status_code == 401:
             if response.json()["error"] == "insufficient_scope":
                 raise InsufficientScope(response.json()["scope"], f"The access token does not have the required scope:'{response.json()['scope']}'")
             raise InvalidKey("The key has expired, been revoked or is invalid.")
         elif response.status_code >= 500: raise ServiceUnavailable("The service is unavailable or has encountered an error.")
         elif not response.ok: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}")
@@ -98,132 +120,195 @@
                         accounts.append(User(creator_id[1:], f"Bearer {self.token}"))
                     elif creator_id.startswith("G"):
                         accounts.append(Group(creator_id[1:], f"Bearer {self.token}"))
 
         return Resources(experiences=experiences, accounts=accounts)
 
     def fetch_token_info(self) -> AccessTokenInfo:
+        """
+        Fetches information the token such as the user's id, the authorized scope, and it's expiry time.
+        """
+
         response = requests.post("https://apis.roblox.com/oauth/v1/token/introspect", data={
             "token": self.token,
             "client_id": self.app.id,
             "client_secret": self.app._OAuth2App__secret
-        })
+        }, headers={"user-agent": user_agent})
         
         if response.ok: return AccessTokenInfo(response.json())
         elif response.status_code == 401:
             if response.json()["error"] == "insufficient_scope":
                 raise InsufficientScope(response.json()["scope"], f"The access token does not have the required scope:'{response.json()['scope']}'")
             raise InvalidKey("The key has expired, been revoked or is invalid.")
         elif response.status_code >= 500: raise ServiceUnavailable("The service is unavailable or has encountered an error.")
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}")
     
     def revoke(self):
         self.app.revoke_token(self.token)
 
 class AccessToken(PartialAccessToken):
+    """
+    Represents access via OAuth2 consent. It allows access to all resources authorized by the user.
+    """
     def __init__(self, app, payload, id_token) -> None:
         super().__init__(app, payload["access_token"])
         self.refresh_token: str = payload["refresh_token"]
         self.scope: list[str] = payload["scope"].split(" ")
         self.expires_at: datetime = datetime.datetime.now() + datetime.timedelta(payload["expires_in"])
         if id_token:
             self.user: Optional[User] = User(id_token.get("id") or id_token.get("sub"), f"Bearer {self.token}")
             self.user.username: str = id_token.get("preferred_username")
             self.user.display_name: str = id_token.get("nickname")
             self.user.created_at: datetime.datetime = datetime.datetime.fromtimestamp(id_token["created_at"]) if id_token.get("created_at") else None
         else: self.user: Optional[User] = None
 
     def __repr__(self) -> str:
-        return f"rblxopencloud.AccessToken(token={self.token[:15]}..., user={self.user})"
+        return f"rblxopencloud.AccessToken(token=\"{self.token[:15]}...\", user={self.user})"
     
     def revoke_refresh_token(self):
+        """
+        Shortcut to revoke the refresh token.
+        """
         self.app.revoke_token(self.refresh_token)
 
 class OAuth2App():
+    """
+    Represents an OAuth2 app. It is used to exchange codes, refresh tokens, and access the API for authenticated users.
+
+    id: int - The app's client ID.
+    secret: str - The app's client secret.
+    redirect_uri: str - The redirect URI that is being used for authorization. If you need to use multiple, you must make seperate :class:`rblx-open-cloud.OAuth2` objects.
+    openid_certs_cache_seconds: int - The number of seconds to cache the openid certs. You can ignore this if you don't know what it does.
+    """
+
     def __init__(self, id: int, secret: str, redirect_uri: str, openid_certs_cache_seconds: int = 3600):
         self.id: int = id
         self.redirect_uri: str = redirect_uri
         self.__secret: str = secret
 
         self.openid_certs_cache_seconds: int = openid_certs_cache_seconds
         self.__openid_certs_cache = None
         self.__openid_certs_cache_updated = None
     
     def __repr__(self) -> str:
-        return f"rblxopencloud.OAuth2App(id={self.id}, redirect_uri={self.redirect_uri})"
+        return f"rblxopencloud.OAuth2App(id={self.id}, redirect_uri=\"{self.redirect_uri}\")"
+
+    def generate_code_verifier(self, length: Optional[int]=128):
+        """
+        Generates a code verifier which can be provided `OAuth2App.generate_uri()` and :meth:`rblx-open-cloud.OAuth2App.exchange_code` to add extra security to the OAuth2 flow.
+
+        If a code verifier is used, it must be provided to both methods, and it should also be unique.
+        ### Parameters
+        length: Optional[int] - How long the code verifier should be.
+        """
+
+        return ''.join(secrets.choice(f"{string.ascii_letters}{string.digits}-._~") for _ in range(length))
+
+    def generate_uri(self, scope: Union[str, list[str]], state: Optional[str]=None, generate_code: Optional[bool]=True, code_verifier: Optional[str] = None) -> str:
+        """
+        Creates an authorization uri with the client information prefilled.
+        ### Parameters
+        scope: Union[str, list[str]] - A string, or list of strings specifying the scopes for authorization. For example `['openid', 'profile']`
+        state: str - A string that will be returned on the otherside of authorization. It isn't required, but is recommend for security.
+        generate_code: bool - Wether to generate a code on return. Defaults to `True`.
+        code_verifier: Optional[str] - The code verifier generated using OAuth2App.generate_code_verifier()`
+        """
 
-    def generate_uri(self, scope: Union[str, list[str]], state: Optional[str]=None, generate_code=True) -> str:
         params = {
             "client_id": self.id,
             "scope": " ".join(scope) if type(scope) == list else scope,
             "state": state,
             "redirect_uri": self.redirect_uri,
-            "response_type": "code" if generate_code else "none"
+            "response_type": "code" if generate_code else "none",
+            "code_challenge": base64.urlsafe_b64encode(hashlib.sha256(code_verifier.encode()).digest()).replace(b"=", b"").decode() if code_verifier else None,
+            "code_challenge_method": "S256" if code_verifier else None
         }
         return f"https://apis.roblox.com/oauth/v1/authorize?{parse.urlencode({key: value for key, value in params.items() if value is not None})}"
 
     def from_access_token_string(self, access_token: str) -> PartialAccessToken:
+        """
+        Creates an `rblx-open-cloud.PartialAccessToken` from an access token string, fairly useless due to these tokens expiring after 15 minutes.
+
+        It is also advised the refresh token instead of the access token, and refresh the token each time you need to access information instead of the access_token to improve security.
+        ### Parameters
+        access_token: str - The access token string.
+        """
+
         return PartialAccessToken(self, access_token)
 
-    def exchange_code(self, code: str) -> AccessToken:
+    def exchange_code(self, code: str, code_verifier: Optional[str]=None) -> AccessToken:
+        """
+        Creates an `rblx-open-cloud.AccessToken` from an authorization code returned from Roblox.
+        ### Parameters
+        code: str - The code from the authorization server.
+        code_verifier: Optional[str] - the string for this OAuth2 flow generated by `OAuth2App.generate_code_verifier()`.
+        """
         response = requests.post("https://apis.roblox.com/oauth/v1/token", data={
             "client_id": self.id,
             "client_secret": self.__secret,
             "redirect_uri": self.redirect_uri,
             "grant_type": "authorization_code",
+            "code_verifier": code_verifier,
             "code": code
-        })
+        }, headers={"user-agent": user_agent})
         id_token = None
         if response.json().get("id_token"):
             if not self.__openid_certs_cache or time.time() - self.__openid_certs_cache_updated > self.openid_certs_cache_seconds:
-                certs = requests.get("https://apis.roblox.com/oauth/v1/certs")
+                certs = requests.get("https://apis.roblox.com/oauth/v1/certs", headers={"user-agent": user_agent})
                 if not certs.ok: raise ServiceUnavailable("Failed to retrieve OpenID certs.")
-                self.__openid_certs_cache = convert_certs_to_keys(certs.json()["keys"])
+
+                self.__openid_certs_cache = []
+                for cert in certs.json()["keys"]:
+                    self.__openid_certs_cache.append(load_der_public_key(ec.EllipticCurvePublicNumbers(
+                        int.from_bytes(base64.urlsafe_b64decode(cert['x'] + '=='), 'big'),
+                        int.from_bytes(base64.urlsafe_b64decode(cert['y'] + '=='), 'big'),
+                        ec.SECP256R1()
+                    ).public_key(default_backend()).public_bytes(
+                        Encoding.DER,
+                        PublicFormat.SubjectPublicKeyInfo
+                    ), default_backend()))
                 self.__openid_certs_cache_updated = time.time()
 
             for cert in self.__openid_certs_cache:
                 try:
                     id_token = jwt.decode(response.json()["id_token"], cert,  algorithms=['ES256'], audience=str(self.id))
                     break
                 except(jwt.exceptions.PyJWTError): pass
 
         if response.ok: return AccessToken(self, response.json(), id_token)
-        elif response.status_code == 400: raise InvalidKey("The client id, client secret, or redirect uri is invalid.")
-        elif response.status_code == 401: raise InvalidCode("The code is invalid, or has been used.")
+        elif response.status_code == 400: raise InvalidKey(response.json().get("error_description", "The client id, client secret, or redirect uri is invalid."))
+        elif response.status_code == 401: raise InvalidCode(response.json().get("error_description", "The code is invalid, or has been used."))
         elif response.status_code >= 500: raise ServiceUnavailable("The service is unavailable or has encountered an error.")
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}")
 
     def refresh_token(self, refresh_token: str) -> AccessToken:
+        """
+        Creates an `rblx-open-cloud.AccessToken` from a refresh token. The new access token will have a different refresh token, and you must store the new refresh token.
+        ### Parameters
+        refresh_token: str - The refresh token to refresh.
+        """
         response = requests.post("https://apis.roblox.com/oauth/v1/token", data={
             "client_id": self.id,
             "client_secret": self.__secret,
             "grant_type": "refresh_token",
             "refresh_token": refresh_token
-        })
+        }, headers={"user-agent": user_agent})
         if response.ok: return AccessToken(self, response.json(), None)
-        elif response.status_code == 400: raise InvalidKey("The code, client id, client secret, or redirect uri is invalid.")
+        elif response.status_code == 400: raise InvalidKey(response.json().get("error_description", "The code, client id, client secret, or redirect uri is invalid."))
         elif response.status_code >= 500: raise ServiceUnavailable("The service is unavailable or has encountered an error.")
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}")
     
     def revoke_token(self, token: str):
+        """
+        Revokes the authorization for a given access token or refresh token string.
+
+        token: str - The refresh token to refresh.
+        """
         response = requests.post("https://apis.roblox.com/oauth/v1/token/revoke", data={
             "token": token,
             "client_id": self.id,
             "client_secret": self.__secret
-        })
+        }, headers={"user-agent": user_agent})
         if response.ok: return
         elif response.status_code == 400: raise InvalidKey("The code, client id, client secret, or redirect uri is invalid.")
         elif response.status_code >= 500: raise ServiceUnavailable("The service is unavailable or has encountered an error.")
         else: raise rblx_opencloudException(f"Unexpected HTTP {response.status_code}")
-
-def convert_certs_to_keys(certs):
-    keys = []
-    for cert in certs:
-        keys.append(load_der_public_key(ec.EllipticCurvePublicNumbers(
-            int.from_bytes(base64.urlsafe_b64decode(cert['x'] + '=='), 'big'),
-            int.from_bytes(base64.urlsafe_b64decode(cert['y'] + '=='), 'big'),
-            ec.SECP256R1()
-        ).public_key(default_backend()).public_bytes(
-            Encoding.DER,
-            PublicFormat.SubjectPublicKeyInfo
-        ), default_backend()))
-    return keys
```

### Comparing `rblx-open-cloud-1.3.1/setup.py` & `rblx-open-cloud-1.4.0/setup.py`

 * *Files identical despite different names*

