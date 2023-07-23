# Comparing `tmp/pyroostermoney-0.2.3.tar.gz` & `tmp/pyroostermoney-0.2.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyroostermoney-0.2.3.tar", last modified: Sat Jul 22 13:03:52 2023, max compression
+gzip compressed data, was "pyroostermoney-0.2.4.tar", last modified: Sun Jul 23 10:01:18 2023, max compression
```

## Comparing `pyroostermoney-0.2.3.tar` & `pyroostermoney-0.2.4.tar`

### file list

```diff
@@ -1,34 +1,36 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 13:03:52.368996 pyroostermoney-0.2.3/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 13:03:52.364996 pyroostermoney-0.2.3/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 13:03:52.368996 pyroostermoney-0.2.3/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)      683 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/.github/workflows/build.yml
--rw-r--r--   0 runner    (1001) docker     (123)      486 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/.github/workflows/publish.yml
--rw-r--r--   0 runner    (1001) docker     (123)      325 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/.github/workflows/release.yml
--rw-r--r--   0 runner    (1001) docker     (123)     3138 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1065 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      593 2023-07-22 13:03:52.368996 pyroostermoney-0.2.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      136 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyproject.toml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 13:03:52.368996 pyroostermoney-0.2.3/pyroostermoney/
--rw-r--r--   0 runner    (1001) docker     (123)      194 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10059 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 13:03:52.368996 pyroostermoney-0.2.3/pyroostermoney/child/
--rw-r--r--   0 runner    (1001) docker     (123)    10239 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/child/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2591 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/child/card.py
--rw-r--r--   0 runner    (1001) docker     (123)     4528 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/child/jobs.py
--rw-r--r--   0 runner    (1001) docker     (123)     2995 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/child/money_pot.py
--rw-r--r--   0 runner    (1001) docker     (123)     1596 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/child/standing_order.py
--rw-r--r--   0 runner    (1001) docker     (123)     2478 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/child/transaction.py
--rw-r--r--   0 runner    (1001) docker     (123)     3307 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/const.py
--rw-r--r--   0 runner    (1001) docker     (123)     2103 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/events.py
--rw-r--r--   0 runner    (1001) docker     (123)      610 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     4650 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/family_account.py
--rw-r--r--   0 runner    (1001) docker     (123)     5006 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/pyroostermoney/roostermoney.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 13:03:52.368996 pyroostermoney-0.2.3/pyroostermoney.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      593 2023-07-22 13:03:52.000000 pyroostermoney-0.2.3/pyroostermoney.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      737 2023-07-22 13:03:52.000000 pyroostermoney-0.2.3/pyroostermoney.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 13:03:52.000000 pyroostermoney-0.2.3/pyroostermoney.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-22 13:03:52.000000 pyroostermoney-0.2.3/pyroostermoney.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-22 13:03:52.000000 pyroostermoney-0.2.3/pyroostermoney.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      225 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      487 2023-07-22 13:03:52.368996 pyroostermoney-0.2.3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      353 2023-07-22 13:03:39.000000 pyroostermoney-0.2.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:01:18.516096 pyroostermoney-0.2.4/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:01:18.512096 pyroostermoney-0.2.4/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:01:18.516096 pyroostermoney-0.2.4/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)      683 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/.github/workflows/build.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      486 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/.github/workflows/publish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      325 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/.github/workflows/release.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     3138 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1065 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      593 2023-07-23 10:01:18.516096 pyroostermoney-0.2.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3073 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)      136 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyproject.toml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:01:18.516096 pyroostermoney-0.2.4/pyroostermoney/
+-rw-r--r--   0 runner    (1001) docker     (123)      194 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8799 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:01:18.516096 pyroostermoney-0.2.4/pyroostermoney/child/
+-rw-r--r--   0 runner    (1001) docker     (123)    10239 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/child/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2591 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/child/card.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5328 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/child/jobs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2995 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/child/money_pot.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1596 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/child/standing_order.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2478 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/child/transaction.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4251 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/const.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2103 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/events.py
+-rw-r--r--   0 runner    (1001) docker     (123)      610 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4650 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/family_account.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3054 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/master_jobs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4795 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/pyroostermoney/roostermoney.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:01:18.516096 pyroostermoney-0.2.4/pyroostermoney.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      593 2023-07-23 10:01:18.000000 pyroostermoney-0.2.4/pyroostermoney.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      774 2023-07-23 10:01:18.000000 pyroostermoney-0.2.4/pyroostermoney.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 10:01:18.000000 pyroostermoney-0.2.4/pyroostermoney.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-23 10:01:18.000000 pyroostermoney-0.2.4/pyroostermoney.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-23 10:01:18.000000 pyroostermoney-0.2.4/pyroostermoney.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      225 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      487 2023-07-23 10:01:18.516096 pyroostermoney-0.2.4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      353 2023-07-23 10:01:07.000000 pyroostermoney-0.2.4/setup.py
```

### Comparing `pyroostermoney-0.2.3/.github/workflows/build.yml` & `pyroostermoney-0.2.4/.github/workflows/build.yml`

 * *Files identical despite different names*

### Comparing `pyroostermoney-0.2.3/.gitignore` & `pyroostermoney-0.2.4/.gitignore`

 * *Files identical despite different names*

### Comparing `pyroostermoney-0.2.3/LICENSE` & `pyroostermoney-0.2.4/LICENSE`

 * *Files identical despite different names*

### Comparing `pyroostermoney-0.2.3/PKG-INFO` & `pyroostermoney-0.2.4/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyroostermoney
-Version: 0.2.3
+Version: 0.2.4
 Summary: A RoosterMoney integration for Python.
 Home-page: https://github.com/pantherale0/pyroostermoney
 Author: pantherale0
 Author-email: support@system32.uk
 License: MIT
 Project-URL: Bug Tracker, https://github.com/pantherale0/pyroostermoney/issues
 Project-URL: Changelog, https://github.com/pantherale0/pyroostermoney/releases
```

### Comparing `pyroostermoney-0.2.3/pyroostermoney/api.py` & `pyroostermoney-0.2.4/pyroostermoney/api.py`

 * *Files 23% similar despite different names*

```diff
@@ -12,67 +12,14 @@
 
 from .const import HEADERS, BASE_URL, LOGIN_BODY, URLS, OAUTH_TOKEN_URL
 from .exceptions import InvalidAuthError, NotLoggedIn, AuthenticationExpired
 from .events import Events
 
 _LOGGER = logging.getLogger(__name__)
 
-async def _fetch_request(url, headers=None):
-    if headers is None:
-        headers=HEADERS
-    async with aiohttp.ClientSession() as session:
-        async with session.get(f"{BASE_URL}/{url}", headers=headers) as response:
-            data = await response.json()
-            return {
-                "status": response.status,
-                "response": data
-            }
-
-async def _post_request(url, body: dict, auth=None, headers=None):
-    if headers is None:
-        headers=HEADERS
-    async with aiohttp.ClientSession() as session:
-        async with session.post(f"{BASE_URL}/{url}",
-                                json=body,
-                                headers=headers,
-                                auth=auth) as response:
-            data = await response.json()
-            return {
-                "status": response.status,
-                "response": data
-            }
-
-async def _put_request(url, body: dict, auth=None, headers=None):
-    if headers is None:
-        headers=HEADERS
-    async with aiohttp.ClientSession() as session:
-        async with session.put(f"{BASE_URL}/{url}",
-                                json=body,
-                                headers=headers,
-                                auth=auth) as response:
-            data = await response.json()
-            return {
-                "status": response.status,
-                "response": data
-            }
-
-async def _delete_request(url, body: dict, auth=None, headers=None):
-    if headers is None:
-        headers=HEADERS
-    async with aiohttp.ClientSession() as session:
-        async with session.delete(f"{BASE_URL}/{url}",
-                                json=body,
-                                headers=headers,
-                                auth=auth) as response:
-            data = await response.json()
-            return {
-                "status": response.status,
-                "response": data
-            }
-
 class RoosterSession:
     """The main Rooster Session."""
 
     def __init__(self,
                  username: str,
                  password: str,
                  update_interval: int=30,
@@ -83,22 +30,56 @@
         self._headers = HEADERS
         self._logged_in = False
         self._logging_in = asyncio.Lock()
         self.events = Events()
         self.update_interval = update_interval
         self.use_updater = use_updater
 
+    async def _send_request(self,
+                      url,
+                      body: dict = None,
+                      auth=None,
+                      method="GET"):
+        """Handles sending HTTP requests"""
+        async with aiohttp.ClientSession() as session:
+            async with session.request(method=method,
+                                       url=f"{BASE_URL}/{url}",
+                                       json=body,
+                                       auth=auth,
+                                       headers=self._headers) as response:
+                output = {
+                    "status": response.status,
+                    "response": {}
+                }
+                if response.status == 401:
+                    raise PermissionError("Unauthorized session")
+                if response.status == 403:
+                    raise PermissionError("Access denied.")
+                if response.status == 204:
+                    return output
+                if response.status >= 200 and response.status < 204:
+                    output["response"] = await response.json()
+                    return output
+                return output
+
     def _parse_login(self, login_response, token):
         """Parses a login response"""
         if "tokens" in login_response:
             login_response=login_response.get("tokens")
+        if "error" in login_response:
+            error = login_response.get("error")
+            raise ConnectionError(error)
+        token_type = login_response.get("token_type")
+        access_token = login_response.get("access_token")
+
+        self._headers["Authorization"] = f"{token_type} {access_token}"
         return {
-                "access_token": login_response.get("access_token"),
+                "access_token": access_token,
                 "refresh_token": login_response.get("refresh_token"),
-                "token_type": login_response.get("token_type"),
+                "token_type": token_type,
                 "expiry_time": datetime.now() + timedelta(0,
                                                           login_response.get("expires_in")),
                 "security_code": token
             }
 
     async def async_login(self):
         """Logs into RoosterMoney and starts a new active session."""
@@ -120,120 +101,101 @@
             auth = aiohttp.BasicAuth(self._username, self._password)
 
             if "Authorization" in self._headers:
                 self._headers.pop("Authorization")
 
             login_response = await self.request_handler(url=URLS.get("login"),
                                                                 body=req_body,
-                                                                auth=auth,
-                                                                headers=self._headers)
+                                                                auth=auth)
 
             if login_response["status"] == 401:
                 raise InvalidAuthError(self._username, login_response["status"])
 
             login_response = login_response["response"]
             token = base64.b64encode(str(self._password[::-1]).encode('utf-8')).decode('utf-8')
 
             self._session = self._parse_login(login_response, token)
 
-            token_type = login_response["tokens"]["token_type"]
-            access_token = login_response["tokens"]["access_token"]
-
-            self._headers["Authorization"] = f"{token_type} {access_token}"
-
             self._logged_in = True
 
         return True
 
     async def refresh_token(self):
         """Refresh the current access token when the session expires."""
         async with aiohttp.ClientSession() as session:
             form = aiohttp.FormData()
             form.add_field("audience", "rooster-app")
             form.add_field("grant_type", "refresh_token")
             form.add_field("client_id", "rooster-app")
             form.add_field("refresh_token", self._session.get("refresh_token"))
-            async with session.post(OAUTH_TOKEN_URL, data=form) as request:
-                data = await request.json()
-                self._session = self._parse_login(data, self._session.get("security_code"))
+            try:
+                async with session.post(OAUTH_TOKEN_URL, data=form) as request:
+                    data = await request.json()
+                    self._session = self._parse_login(data, self._session.get("security_code"))
+            except ConnectionError:
+                await self.async_login()
 
     async def _internal_request_handler(self,
                                         url,
                                         body=None,
-                                        headers=None,
                                         auth=None,
                                         method="GET",
                                         login_request=False,
                                         add_security_token=False):
         """Handles all incoming requests to make sure that the session is active."""
 
         if self._session is None and self._logged_in:
             raise RuntimeError("Invalid state. Missing session data yet currently logged in?")
         if self._session is None and self._logged_in is False and auth is not None:
             _LOGGER.info("Not logged in, trying now.")
-            if headers is None:
-                headers = self._headers
-            return await _post_request(url, body, auth, headers)
+            return await self._send_request(url, body, auth, "POST")
         if self._session is None and self._logged_in is False and auth is None:
             raise NotLoggedIn()
         if self._session is not None and self._logged_in is False:
             raise RuntimeError("Invalid state. Session data available yet not logged in?")
         if self._session["expiry_time"] < datetime.now() and login_request:
             _LOGGER.debug("Login request.")
-            return await _post_request(url, body, auth, headers)
+            return await self._send_request(url, body, auth, "POST")
 
         # Check if auth has expired
         # pylint: disable=no-else-raise
         # pylint: disable=no-else-return
         if self._session["expiry_time"] < datetime.now():
             raise AuthenticationExpired()
 
-        if headers is None:
-            headers = self._headers
-
         if add_security_token:
-            headers["securitytoken"] = self._session["security_code"]
+            self._headers["securitytoken"] = self._session["security_code"]
+        elif "securitytoken" in self._headers:
+            self._headers.pop("securitytoken")
 
-        if method == "GET":
-            return await _fetch_request(url, headers=headers)
-        if method == "POST":
-            return await _post_request(url, body=body, headers=headers)
-        if method == "PUT":
-            return await _put_request(url, body=body, headers=headers)
-        if method == "DELETE":
-            return await _delete_request(url, body=body, headers=headers)
-        else:
-            raise ValueError("Invalid type argument.")
+        return await self._send_request(url=url, body=body, auth=auth, method=method.upper())
 
     async def request_handler(self,
                                         url,
                                         body=None,
-                                        headers=None,
                                         auth=None,
                                         method="GET",
                                         login_request=False,
                                         add_security_token=False):
         """Public calls for the private _internal_request_handler."""
         _LOGGER.debug("Sending %s HTTP request to %s", method, url)
         try:
             return await self._internal_request_handler(
                 url=url,
                 body=body,
-                headers=headers,
                 auth=auth,
                 method=method,
                 login_request=login_request,
                 add_security_token=add_security_token
             )
         except AuthenticationExpired:
             await self.refresh_token()
             return await self._internal_request_handler(
                 url=url,
                 body=body,
-                headers=headers,
                 auth=auth,
                 method=method,
                 login_request=login_request
             )
         except NotLoggedIn as exc:
             raise NotLoggedIn() from exc
         except aiohttp.ClientOSError as exc:
```

### Comparing `pyroostermoney-0.2.3/pyroostermoney/child/__init__.py` & `pyroostermoney-0.2.4/pyroostermoney/child/__init__.py`

 * *Files identical despite different names*

### Comparing `pyroostermoney-0.2.3/pyroostermoney/child/card.py` & `pyroostermoney-0.2.4/pyroostermoney/child/card.py`

 * *Files identical despite different names*

### Comparing `pyroostermoney-0.2.3/pyroostermoney/child/jobs.py` & `pyroostermoney-0.2.4/pyroostermoney/child/jobs.py`

 * *Files 16% similar despite different names*

```diff
@@ -4,25 +4,36 @@
 # pylint: disable=too-many-arguments
 from datetime import datetime
 from enum import Enum
 
 from pyroostermoney.api import RoosterSession
 from pyroostermoney.const import CURRENCY, URLS
 
+class JobScheduleTypes(Enum):
+    """Job schedule types."""
+    REPEATING = 2
+    ANYTIME = 1
+    UNKNOWN = -1
+
+class JobTime(Enum):
+    """Job times."""
+    MORNING = 12
+    AFTERNOON = 17
+    ANYTIME = 23
+
 class JobState(Enum):
     """Job states."""
-    POOL = 0
+    NO_PREVIOUS_STATE = 0
     TODO = 1
-    SKIPPED = 2
-    PAUSED = 3
-    OVERDUE = 4
-    NO_PREVIOUS_STATE = 5
+    AWAITING_APPROVAL = 2
+    APPROVED = 3
+    PAUSED = 4
+    OVERDUE = 5
     NOT_DONE = 6
-    AWAITING_APPROVAL = 7
-    APPROVED = 8
+    SKIPPED = 7
 
     def __str__(self) -> str:
         return str(self.name)
 
 class JobActions(Enum):
     """All supported job actions."""
     APPROVE = 8
@@ -47,14 +58,15 @@
                  reopened,
                  reward_amount,
                  scheduled_job_id,
                  state,
                  time_of_day,
                  title,
                  job_type,
+                 schedule_type,
                  session,
                  user_id_list: list | None=None):
         self.allowance_period_id: int = allowance_period_id
         self.currency: str = currency
         self.description: str = description
         self.due_any_day: bool = due_any_day
         self.due_date: datetime = due_date
@@ -63,24 +75,34 @@
         self.image_url: str = image_url
         self.locked: bool = locked
         self.master_job_id: int = master_job_id
         self.reopened: bool = reopened
         self.reward_amount: float = reward_amount
         self.scheduled_job_id: int = scheduled_job_id
         self.state: JobState = state
-        self.time_of_day: int = time_of_day
+        self.time_of_day: JobTime = JobTime(time_of_day)
+        self.schedule_type: JobScheduleTypes = (
+            JobScheduleTypes(schedule_type) if schedule_type is not None
+            else JobScheduleTypes.UNKNOWN)
         self.title: str = title
         self.type: int = job_type
         self._session: RoosterSession = session
         if user_id_list is not None:
             self.user_id_list = user_id_list
 
     @staticmethod
     def from_dict(obj: dict, session) -> 'Job':
         """Converts to a job from a dict."""
+        if "scheduleInfo" in obj:
+            # Move nested scheduleInfo into main
+            for info in obj.get("scheduleInfo").keys():
+                if info == "type":
+                    info = "scheduleType"
+                obj[info] = obj.get("scheduleInfo").get(info)
+            obj["scheduleInfo"] = None
         if "dueDate" in obj:
             _due_date = datetime.strptime(obj.get("dueDate"), "%Y-%m-%d")
         else:
             _due_date = None
         return Job(
             allowance_period_id=int(obj.get("allowancePeriodId", -1)),
             currency=str(obj.get("currency", CURRENCY)),
@@ -96,15 +118,16 @@
             reward_amount=float(obj.get("rewardAmount", 0)),
             scheduled_job_id=int(obj.get("scheduledJobId", 0)),
             state=JobState(obj.get("state", 0)),
             time_of_day=int(obj.get("timeOfDay", 0)),
             title=str(obj.get("title", "")),
             job_type=int(obj.get("type", 0)),
             session=session,
-            user_id_list=obj.get("childUserIds", None)
+            user_id_list=obj.get("childUserIds", None),
+            schedule_type=obj.get("scheduleType")
         )
 
     @staticmethod
     def convert_response(raw_response: dict, session: RoosterSession) -> list['Job']:
         """Converts a raw response."""
         if "response" in raw_response:
             raw_response=raw_response["response"]
@@ -124,9 +147,10 @@
         await self._session.request_handler(
             url=URLS.get("scheduled_job_action").format(
                 schedule_id=self.scheduled_job_id,
                 action=str(action)
             ),
             body={
                 "message": message
-            }
+            },
+            method="POST"
         )
```

### Comparing `pyroostermoney-0.2.3/pyroostermoney/child/money_pot.py` & `pyroostermoney-0.2.4/pyroostermoney/child/money_pot.py`

 * *Files identical despite different names*

### Comparing `pyroostermoney-0.2.3/pyroostermoney/child/standing_order.py` & `pyroostermoney-0.2.4/pyroostermoney/child/standing_order.py`

 * *Files identical despite different names*

### Comparing `pyroostermoney-0.2.3/pyroostermoney/child/transaction.py` & `pyroostermoney-0.2.4/pyroostermoney/child/transaction.py`

 * *Files identical despite different names*

### Comparing `pyroostermoney-0.2.3/pyroostermoney/const.py` & `pyroostermoney-0.2.4/pyroostermoney/const.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,21 +1,22 @@
 # pylint: disable=line-too-long
 """Static Rooster Money variables"""
 
-VERSION="0.2.3"
+VERSION="0.2.4"
 BASE_URL="https://api.rooster.money"
 OAUTH_TOKEN_URL="https://auth.rooster.money/oidc/token"
 LANGUAGE="en-GB"
 COUNTRY="gb"
 CURRENCY="GBP"
 TIMEZONE_ID=60
 TIMEZONE="GMT+01:00"
 DEFAULT_PRECISION=2
 DEFAULT_BANK_NAME="Rooster Money"
 DEFAULT_BANK_TYPE="Business"
+DEFAULT_JOB_IMAGE_URL="https://images.roostermoney.com/static/default_job_icon.png"
 MOBILE_APP_VERSION="10.3.1"
 
 SAVINGS_POT_ID="SAVE_POT"
 SPEND_POT_ID="SPEND_POT"
 GIVE_POT_ID="GIVE_POT"
 GOAL_POT_ID="GOAL_POT"
 
@@ -42,15 +43,16 @@
     "boost_pot": "api/v1/families/{family_id}/children/{user_id}/pots/{pot_id}/boost",
     "scheduled_job_action": "/api/parent/scheduled-jobs/{schedule_id}/{action}"
 }
 
 HEADERS = {
     "content-type": "application/json",
     "accept": "application/json",
-    "user-agent": f"Mozilla/5.0 Rooster Money {MOBILE_APP_VERSION}"
+    "user-agent": f"Mozilla/5.0 Rooster Money {MOBILE_APP_VERSION}",
+    "version": MOBILE_APP_VERSION
 }
 
 LOGIN_BODY={
     "countryOfResidence": COUNTRY,
     "cultureCode": LANGUAGE,
     "currency": CURRENCY,
     "dismissibleAlertSections": [],
@@ -96,7 +98,34 @@
         "precision": DEFAULT_PRECISION
     },
     "metaData": {
         "flowSource": "spend pot"
     },
     "reason": ""
 }
+
+CREATE_MASTER_JOB_BODY = {
+            "childUserIds": [],
+            "masterJob": {
+                "createdByGuardianId": 1,
+                "currency": CURRENCY,
+                "description": "",
+                "familyId":1,
+                "imageUrl": "",
+                "rewardAmount": 0.0,
+                "scheduleInfo": {
+                    "afterLastDone": False,
+                    "dueAnyDay": False,
+                    "repeatEvery": 1,
+                    "startingDate": {
+                        "day": "",
+                        "month": "",
+                        "year": ""
+                    },
+                    "timeOfDay": 23,
+                    "type": 1
+                },
+                "scheduleType": 1,
+                "title": "",
+                "type": 0
+            }
+        }
```

### Comparing `pyroostermoney-0.2.3/pyroostermoney/events.py` & `pyroostermoney-0.2.4/pyroostermoney/events.py`

 * *Files identical despite different names*

### Comparing `pyroostermoney-0.2.3/pyroostermoney/exceptions.py` & `pyroostermoney-0.2.4/pyroostermoney/exceptions.py`

 * *Files identical despite different names*

### Comparing `pyroostermoney-0.2.3/pyroostermoney/family_account.py` & `pyroostermoney-0.2.4/pyroostermoney/family_account.py`

 * *Files identical despite different names*

### Comparing `pyroostermoney-0.2.3/pyroostermoney/roostermoney.py` & `pyroostermoney-0.2.4/pyroostermoney/roostermoney.py`

 * *Files 14% similar despite different names*

```diff
@@ -7,14 +7,15 @@
 from datetime import datetime, timedelta
 
 from .const import URLS
 from .child import ChildAccount, Job
 from .family_account import FamilyAccount
 from .api import RoosterSession
 from .events import EventSource, EventType
+from .master_jobs import MasterJobs
 
 _LOGGER = logging.getLogger(__name__)
 
 class RoosterMoney(RoosterSession):
     """The RoosterMoney module."""
 
     def __init__(self,
@@ -28,14 +29,15 @@
             password=password,
             use_updater=use_updater,
             update_interval=update_interval
         )
         self.account_info = None
         self.children: list[ChildAccount] = []
         self.master_job_list: list[Job] = []
+        self.master_jobs: MasterJobs = None
         self._discovered_children: list = []
         self.family_account: FamilyAccount = None
         self._update_lock = asyncio.Lock()
         self._updater = None
         self._remove_card_information = remove_card_information
         self._init = True
 
@@ -43,14 +45,15 @@
         if self.use_updater:
             self._updater.cancel()
             self._updater = None
 
     async def async_login(self):
         await super().async_login()
         await self.get_family_account()
+        self.master_jobs = MasterJobs(self)
         await self.update()
         if self.use_updater:
             _LOGGER.debug("Using auto updater for RoosterMoney")
             self._updater = asyncio.create_task(self._update_scheduler())
         self._init = False
 
     async def _update_scheduler(self):
@@ -64,15 +67,16 @@
     async def update(self):
         """Perform an update of all root types"""
         if self._update_lock.locked():
             return True
 
         async with self._update_lock:
             await self.get_children()
-            await self.get_master_job_list()
+            await self.master_jobs.update()
+            self.master_job_list = self.master_jobs.jobs
             for child in self.children:
                 await child.update()
             await self.family_account.update()
 
     async def get_children(self) -> list[ChildAccount]:
         """Returns a list of available children."""
         account_info = await self.get_account_info()
@@ -107,24 +111,14 @@
         self.account_info = self.account_info["response"]
         return self.account_info
 
     def get_child_account(self, user_id) -> ChildAccount:
         """Fetches and returns a given child account details."""
         return [x for x in self.children if x.user_id == user_id][0]
 
-    async def get_master_job_list(self) -> list[Job]:
-        """Gets master job list (/parent/master-jobs)"""
-        response = await self.request_handler(
-            url=URLS.get("get_master_job_list")
-        )
-        jobs = Job.convert_response(response.get("response"), self)
-        for job in jobs:
-            self.master_job_list.append(job)
-        return self.master_job_list
-
     async def get_family_account(self) -> FamilyAccount:
         """Gets family account details (/parent/family/account)"""
         response = await self.request_handler(
             url=URLS.get("get_family_account")
         )
         account = await self.get_account_info()
         self.family_account =  FamilyAccount(response["response"], account, self)
```

### Comparing `pyroostermoney-0.2.3/pyroostermoney.egg-info/PKG-INFO` & `pyroostermoney-0.2.4/pyroostermoney.egg-info/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyroostermoney
-Version: 0.2.3
+Version: 0.2.4
 Summary: A RoosterMoney integration for Python.
 Home-page: https://github.com/pantherale0/pyroostermoney
 Author: pantherale0
 Author-email: support@system32.uk
 License: MIT
 Project-URL: Bug Tracker, https://github.com/pantherale0/pyroostermoney/issues
 Project-URL: Changelog, https://github.com/pantherale0/pyroostermoney/releases
```

### Comparing `pyroostermoney-0.2.3/pyroostermoney.egg-info/SOURCES.txt` & `pyroostermoney-0.2.4/pyroostermoney.egg-info/SOURCES.txt`

 * *Files 18% similar despite different names*

```diff
@@ -1,22 +1,24 @@
 .gitignore
 LICENSE
+cli.py
 pyproject.toml
 requirements.txt
 setup.cfg
 setup.py
 .github/workflows/build.yml
 .github/workflows/publish.yml
 .github/workflows/release.yml
 pyroostermoney/__init__.py
 pyroostermoney/api.py
 pyroostermoney/const.py
 pyroostermoney/events.py
 pyroostermoney/exceptions.py
 pyroostermoney/family_account.py
+pyroostermoney/master_jobs.py
 pyroostermoney/roostermoney.py
 pyroostermoney.egg-info/PKG-INFO
 pyroostermoney.egg-info/SOURCES.txt
 pyroostermoney.egg-info/dependency_links.txt
 pyroostermoney.egg-info/requires.txt
 pyroostermoney.egg-info/top_level.txt
 pyroostermoney/child/__init__.py
```

