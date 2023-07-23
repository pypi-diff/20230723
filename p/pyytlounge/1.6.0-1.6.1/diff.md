# Comparing `tmp/pyytlounge-1.6.0.tar.gz` & `tmp/pyytlounge-1.6.1.tar.gz`

## Comparing `pyytlounge-1.6.0.tar` & `pyytlounge-1.6.1.tar`

### file list

```diff
@@ -1,19 +1,19 @@
--rw-r--r--   0        0        0      453 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/CHANGELOG.md
--rw-r--r--   0        0        0     1432 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/test.py
--rw-r--r--   0        0        0       71 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/variables_example.py
--rw-r--r--   0        0        0     1109 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/.github/workflows/python-publish.yml
--rw-r--r--   0        0        0      997 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/.github/workflows/test.yml
--rw-r--r--   0        0        0      495 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/.vscode/launch.json
--rw-r--r--   0        0        0       74 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/src/pyytlounge/__init__.py
--rw-r--r--   0        0        0       48 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/src/pyytlounge/api.py
--rwxr-xr-x   0        0        0     1040 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/src/pyytlounge/manual_pairing.py
--rw-r--r--   0        0        0    18847 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/src/pyytlounge/wrapper.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/tests/__init__.py
--rw-r--r--   0        0        0      219 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/tests/conftest.py
--rw-r--r--   0        0        0     4102 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/tests/devices.py
--rw-r--r--   0        0        0      446 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/tests/test_process_event.py
--rw-r--r--   0        0        0       48 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/.gitignore
--rw-r--r--   0        0        0    35148 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/LICENSE
--rw-r--r--   0        0        0      447 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/README.md
--rw-r--r--   0        0        0      671 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/pyproject.toml
--rw-r--r--   0        0        0     1082 2020-02-02 00:00:00.000000 pyytlounge-1.6.0/PKG-INFO
+-rw-r--r--   0        0        0      730 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/CHANGELOG.md
+-rw-r--r--   0        0        0     1432 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/test.py
+-rw-r--r--   0        0        0       71 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/variables_example.py
+-rw-r--r--   0        0        0     1109 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/.github/workflows/python-publish.yml
+-rw-r--r--   0        0        0      997 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/.github/workflows/test.yml
+-rw-r--r--   0        0        0      495 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/.vscode/launch.json
+-rw-r--r--   0        0        0       74 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/src/pyytlounge/__init__.py
+-rw-r--r--   0        0        0       48 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/src/pyytlounge/api.py
+-rwxr-xr-x   0        0        0     1040 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/src/pyytlounge/manual_pairing.py
+-rw-r--r--   0        0        0    19795 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/src/pyytlounge/wrapper.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/tests/__init__.py
+-rw-r--r--   0        0        0      219 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/tests/conftest.py
+-rw-r--r--   0        0        0     4102 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/tests/devices.py
+-rw-r--r--   0        0        0      446 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/tests/test_process_event.py
+-rw-r--r--   0        0        0       48 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/.gitignore
+-rw-r--r--   0        0        0    35148 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/LICENSE
+-rw-r--r--   0        0        0      447 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/README.md
+-rw-r--r--   0        0        0      671 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/pyproject.toml
+-rw-r--r--   0        0        0     1082 2020-02-02 00:00:00.000000 pyytlounge-1.6.1/PKG-INFO
```

### Comparing `pyytlounge-1.6.0/test.py` & `pyytlounge-1.6.1/test.py`

 * *Files identical despite different names*

### Comparing `pyytlounge-1.6.0/.github/workflows/python-publish.yml` & `pyytlounge-1.6.1/.github/workflows/python-publish.yml`

 * *Files identical despite different names*

### Comparing `pyytlounge-1.6.0/.github/workflows/test.yml` & `pyytlounge-1.6.1/.github/workflows/test.yml`

 * *Files identical despite different names*

### Comparing `pyytlounge-1.6.0/src/pyytlounge/manual_pairing.py` & `pyytlounge-1.6.1/src/pyytlounge/manual_pairing.py`

 * *Files identical despite different names*

### Comparing `pyytlounge-1.6.0/src/pyytlounge/wrapper.py` & `pyytlounge-1.6.1/src/pyytlounge/wrapper.py`

 * *Files 4% similar despite different names*

```diff
@@ -147,14 +147,32 @@
 
 
 def get_thumbnail_url(video_id: str, thumbnail_idx=0) -> str:
     """Returns thumbnail for given video. Use thumbnail idx to get different thumbnails."""
     return f"https://img.youtube.com/vi/{video_id}/{thumbnail_idx}.jpg"
 
 
+class NotConnectedException(Exception):
+    """This exception indicates an operation that failed due to an incorrect state.
+    The operation requires that there is an active connection to the API.
+    Use the connected() and connect() functions on YtLoungeApi."""
+
+
+class NotPairedException(Exception):
+    """This exception indicates an operation that failed due to an incorrect state.
+    The operation requires that the API has been paired with a screen.
+    Use the paired() and pair() functions on YtLoungeApi."""
+
+
+class NotLinkedException(Exception):
+    """This exception indicates an operation that failed due to an incorrect state.
+    The operation requires that the API has been linked with a screen.
+    Use the linked(), pair() and refresh_auth() functions on YtLoungeApi."""
+
+
 class YtLoungeApi:
     """Wrapper class for YouTube Lounge API"""
 
     def __init__(self, device_name: str, logger: logging.Logger = None):
         self.device_name = device_name
         self.auth = AuthState()
         self._sid = None
@@ -187,23 +205,23 @@
                  last_event_id = {self._last_event_id}\n\
                  "
 
     @property
     def screen_name(self) -> str:
         """Returns screen name as returned by YouTube"""
         if not self.linked():
-            raise Exception("Not linked")
+            raise NotLinkedException("Not linked")
 
         return self._screen_name
 
     @property
     def screen_device_name(self) -> str:
         """Returns device name built from device info returned by YouTube"""
         if not self.connected():
-            raise Exception("Not connected")
+            raise NotConnectedException("Not connected")
         brand = self._device_info["brand"]
         model = self._device_info["model"]
         return f"{brand} {model}"
 
     async def pair(self, pairing_code) -> bool:
         """Pair with a device using a manual input pairing code"""
 
@@ -221,15 +239,15 @@
                 except Exception as ex:
                     self._logger.exception(ex)
                     return False
 
     async def refresh_auth(self) -> bool:
         """Refresh lounge token using stored refresh token."""
         if not self.paired():
-            raise Exception("Must be paired")
+            raise NotPairedException("Must be paired")
 
         async with aiohttp.ClientSession() as session:
             refresh_url = f"{api_base}/pairing/get_lounge_token_batch"
             refresh_data = {"screen_ids": self.auth.screen_id}
             async with session.post(url=refresh_url, data=refresh_data) as resp:
                 try:
                     screens = await resp.json()
@@ -323,15 +341,15 @@
                     yield events
 
     async def is_available(self) -> bool:
         """Asks YouTube API if the screen is available.
         Must be linked prior to this."""
 
         if not self.linked():
-            raise Exception("Not connected")
+            raise NotConnectedException("Not connected")
 
         body = {"lounge_token": self.auth.lounge_id_token}
 
         url = f"{api_base}/pairing/get_screen_availability"
 
         async with aiohttp.ClientSession() as session:
             result = await session.post(url=url, data=body)
@@ -347,15 +365,15 @@
         if not self.state.videoId:
             return None
         return get_thumbnail_url(self.state.videoId, thumbnail_idx)
 
     async def connect(self) -> bool:
         """Attempt to connect using the previously set tokens"""
         if not self.linked():
-            raise Exception("Not linked")
+            raise NotLinkedException("Not linked")
 
         connect_body = {
             "app": "web",
             "mdx-version": "3",
             "name": self.device_name,
             "id": self.auth.screen_id,
             "device": "REMOTE_CONTROL",
@@ -385,30 +403,30 @@
                         return False
                     lines = text.splitlines()
                     async for events in self._parse_event_chunks(desync(lines)):
                         self._process_events(events)
                     self._command_offset = 1
                     return self.connected()
                 except Exception as ex:
-                    self._logger.exception(ex)
+                    self._logger.exception(ex, resp.status, resp.reason)
                     return False
 
     def _handle_session_result(self, status_code: int, reason: str) -> bool:
         if status_code == 400 and "Unknown SID" in reason:
             self._connection_lost()
             return False
         if status_code == 410 and "Gone" in reason:
             self._connection_lost()
             return False
         return True
 
     async def subscribe(self, callback: Callable[[PlaybackState], Any]) -> None:
         """Start listening for events"""
         if not self.connected():
-            raise Exception("Not connected")
+            raise NotConnectedException("Not connected")
 
         params = {
             "device": "REMOTE_CONTROL",
             "name": self.device_name,
             "app": "youtube-desktop",
             "loungeIdToken": self.auth.lounge_id_token,
             "VER": "8",
@@ -418,17 +436,17 @@
             "CI": "0",
             "AID": self._last_event_id,
             "gsessionid": self._gsession,
             "TYPE": "xmlhttp",
         }
         url = f"{api_base}/bc/bind"
         self._logger.info("Subscribing to lounge id %s", self.auth.lounge_id_token)
-        try:
-            async with aiohttp.ClientSession(timeout=ClientTimeout()) as session:
-                async with session.get(url=url, params=params) as resp:
+        async with aiohttp.ClientSession(timeout=ClientTimeout()) as session:
+            async with session.get(url=url, params=params) as resp:
+                try:
                     if not self._handle_session_result(resp.status, resp.reason):
                         return
 
                     async for events in self._parse_event_chunks(
                         iter_response_lines(resp.content)
                     ):
                         pre_state_update = self.state_update
@@ -437,21 +455,21 @@
                             await callback(self.state)
                         if not self.connected():
                             break
                     self._logger.info(
                         "Subscribe completed, status %i %s", resp.status, resp.reason
                     )
 
-        except Exception as ex:
-            self._logger.exception(ex)
+                except Exception as ex:
+                    self._logger.exception(ex, resp.status, resp.reason)
 
     async def disconnect(self) -> bool:
         """Disconnect from the current session"""
         if not self.connected():
-            raise Exception("Not connected")
+            raise NotConnectedException("Not connected")
 
         command_body = {
             "ui": "",
             "TYPE": "terminate",
             "clientDisconnectReason": "MDX_SESSION_DISCONNECT_REASON_DISCONNECTED_BY_USER",
         }
         params = {
@@ -479,15 +497,15 @@
                     return True
                 except Exception as ex:
                     self._logger.exception(ex)
                     return False
 
     async def _command(self, command: str, command_parameters: dict = None) -> bool:
         if not self.connected():
-            raise Exception("Not connected")
+            raise NotConnectedException("Not connected")
 
         command_body = {"count": 1, "ofs": self._command_offset, "req0__sc": command}
         if command_parameters:
             for cmd_param in command_parameters:
                 value = command_parameters[cmd_param]
                 command_body[f"req0_{cmd_param}"] = value
```

### Comparing `pyytlounge-1.6.0/tests/devices.py` & `pyytlounge-1.6.1/tests/devices.py`

 * *Files identical despite different names*

### Comparing `pyytlounge-1.6.0/LICENSE` & `pyytlounge-1.6.1/LICENSE`

 * *Files identical despite different names*

### Comparing `pyytlounge-1.6.0/pyproject.toml` & `pyytlounge-1.6.1/pyproject.toml`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "pyytlounge"
-version = "1.6.0"
+version = "1.6.1"
 authors = [
   { name="Fabio", email="example@example.com" },
 ]
 description = "YouTube Lounge API wrapper"
 readme = "README.md"
 requires-python = ">=3.8"
 classifiers = [
```

### Comparing `pyytlounge-1.6.0/PKG-INFO` & `pyytlounge-1.6.1/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyytlounge
-Version: 1.6.0
+Version: 1.6.1
 Summary: YouTube Lounge API wrapper
 Project-URL: Homepage, https://github.com/FabioGNR/pyytlounge
 Project-URL: Bug Tracker, https://github.com/FabioGNR/pyytlounge/issues
 Author-email: Fabio <example@example.com>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

