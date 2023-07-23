# Comparing `tmp/flux_led-1.0.0.tar.gz` & `tmp/flux_led-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "flux_led-1.0.0.tar", last modified: Wed Jul 19 01:41:34 2023, max compression
+gzip compressed data, was "flux_led-1.0.1.tar", last modified: Sun Jul 23 17:37:59 2023, max compression
```

## Comparing `flux_led-1.0.0.tar` & `flux_led-1.0.1.tar`

### file list

```diff
@@ -1,32 +1,32 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 01:41:34.564828 flux_led-1.0.0/
--rw-r--r--   0 runner    (1001) docker     (123)     7651 2023-07-19 01:41:24.000000 flux_led-1.0.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1100 2023-07-19 01:41:34.564828 flux_led-1.0.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    13313 2023-07-19 01:41:24.000000 flux_led-1.0.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 01:41:34.564828 flux_led-1.0.0/flux_led/
--rw-r--r--   0 runner    (1001) docker     (123)      401 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       68 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/aio.py
--rw-r--r--   0 runner    (1001) docker     (123)    35185 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/aiodevice.py
--rw-r--r--   0 runner    (1001) docker     (123)     1913 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/aioprotocol.py
--rw-r--r--   0 runner    (1001) docker     (123)     6805 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/aioscanner.py
--rw-r--r--   0 runner    (1001) docker     (123)      192 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/aioutils.py
--rw-r--r--   0 runner    (1001) docker     (123)    48613 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/base_device.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     3991 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/const.py
--rw-r--r--   0 runner    (1001) docker     (123)    13118 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/device.py
--rw-r--r--   0 runner    (1001) docker     (123)    27472 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/fluxled.py
--rwxr-xr-x   0 runner    (1001) docker     (123)    49122 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/models_db.py
--rw-r--r--   0 runner    (1001) docker     (123)    39399 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/pattern.py
--rwxr-xr-x   0 runner    (1001) docker     (123)    87787 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/protocol.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)    11637 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/scanner.py
--rw-r--r--   0 runner    (1001) docker     (123)     1607 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/sock.py
--rw-r--r--   0 runner    (1001) docker     (123)    11406 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/timer.py
--rw-r--r--   0 runner    (1001) docker     (123)    11241 2023-07-19 01:41:24.000000 flux_led-1.0.0/flux_led/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 01:41:34.564828 flux_led-1.0.0/flux_led.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1100 2023-07-19 01:41:34.000000 flux_led-1.0.0/flux_led.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      592 2023-07-19 01:41:34.000000 flux_led-1.0.0/flux_led.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-19 01:41:34.000000 flux_led-1.0.0/flux_led.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-19 01:41:34.000000 flux_led-1.0.0/flux_led.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      923 2023-07-19 01:41:34.000000 flux_led-1.0.0/flux_led.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-19 01:41:34.000000 flux_led-1.0.0/flux_led.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      370 2023-07-19 01:41:34.568828 flux_led-1.0.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2327 2023-07-19 01:41:24.000000 flux_led-1.0.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:37:59.790652 flux_led-1.0.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     7651 2023-07-23 17:37:49.000000 flux_led-1.0.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1100 2023-07-23 17:37:59.790652 flux_led-1.0.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    13313 2023-07-23 17:37:49.000000 flux_led-1.0.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:37:59.790652 flux_led-1.0.1/flux_led/
+-rw-r--r--   0 runner    (1001) docker     (123)      401 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       68 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/aio.py
+-rw-r--r--   0 runner    (1001) docker     (123)    35208 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/aiodevice.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2057 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/aioprotocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6805 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/aioscanner.py
+-rw-r--r--   0 runner    (1001) docker     (123)      192 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/aioutils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    48613 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/base_device.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     3991 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/const.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13118 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/device.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27472 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/fluxled.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)    49122 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/models_db.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39399 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/pattern.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)    87787 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/protocol.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)    11637 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/scanner.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1607 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/sock.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11406 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/timer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11241 2023-07-23 17:37:49.000000 flux_led-1.0.1/flux_led/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:37:59.790652 flux_led-1.0.1/flux_led.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1100 2023-07-23 17:37:59.000000 flux_led-1.0.1/flux_led.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      592 2023-07-23 17:37:59.000000 flux_led-1.0.1/flux_led.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 17:37:59.000000 flux_led-1.0.1/flux_led.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-23 17:37:59.000000 flux_led-1.0.1/flux_led.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      923 2023-07-23 17:37:59.000000 flux_led-1.0.1/flux_led.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 17:37:59.000000 flux_led-1.0.1/flux_led.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      370 2023-07-23 17:37:59.790652 flux_led-1.0.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2327 2023-07-23 17:37:49.000000 flux_led-1.0.1/setup.py
```

### Comparing `flux_led-1.0.0/LICENSE` & `flux_led-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/PKG-INFO` & `flux_led-1.0.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: flux_led
-Version: 1.0.0
+Version: 1.0.1
 Summary: A Python library to communicate with the flux_led smart bulbs
 Home-page: https://github.com/Danielhiversen/flux_led
 Author: Daniel Hjelseth Høyer
 Author-email: mail@dahoiv.net
 License: LGPLv3+
 Keywords: flux_led,smart bulbs,light
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `flux_led-1.0.0/README.md` & `flux_led-1.0.1/README.md`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/aiodevice.py` & `flux_led-1.0.1/flux_led/aiodevice.py`

 * *Files 1% similar despite different names*

```diff
@@ -194,18 +194,18 @@
     async def _async_send_state_query(self) -> None:
         assert self._protocol is not None
         await self._async_send_msg(self._protocol.construct_state_query())
 
     async def _async_wait_state_change(
         self, futures: List["asyncio.Future[Any]"], state: bool, timeout: float
     ) -> bool:
-        done, _ = await asyncio.wait(futures, timeout=timeout)
-        if done and self.is_on == state:
-            return True
-        return False
+        done, _ = await asyncio.wait(
+            futures, timeout=timeout, return_when=asyncio.FIRST_COMPLETED
+        )
+        return bool(done and self.is_on == state)
 
     async def _async_set_power_state(
         self, state: bool, accept_any_power_state_response: bool
     ) -> bool:
         assert self._protocol is not None
         power_state_future: "asyncio.Future[bool]" = asyncio.Future()
         state_future: "asyncio.Future[Union[LEDENETRawState, LEDENETOriginalRawState]]" = (
```

### Comparing `flux_led-1.0.0/flux_led/aioprotocol.py` & `flux_led-1.0.1/flux_led/aioprotocol.py`

 * *Files 4% similar despite different names*

```diff
@@ -28,30 +28,32 @@
         """Handle connection made."""
         self.transport = cast(WriteTransport, transport)
         self.peername = transport.get_extra_info("peername")
 
     def write(self, data: bytes) -> None:
         """Write data to the client."""
         assert self.transport is not None
-        _LOGGER.debug(
-            "%s => %s (%d)",
-            self.peername,
-            " ".join(f"0x{x:02X}" for x in data),
-            len(data),
-        )
+        if _LOGGER.isEnabledFor(logging.DEBUG):
+            _LOGGER.debug(
+                "%s => %s (%d)",
+                self.peername,
+                " ".join(f"0x{x:02X}" for x in data),
+                len(data),
+            )
         self.transport.write(data)
 
     def close(self) -> None:
         """Remove the connection and close the transport."""
         assert self.transport is not None
         self.transport.write_eof()
         self.transport.close()
 
     def data_received(self, data: bytes) -> None:
         """Process new data from the socket."""
-        _LOGGER.debug(
-            "%s <= %s (%d)",
-            self.peername,
-            " ".join(f"0x{x:02X}" for x in data),
-            len(data),
-        )
+        if _LOGGER.isEnabledFor(logging.DEBUG):
+            _LOGGER.debug(
+                "%s <= %s (%d)",
+                self.peername,
+                " ".join(f"0x{x:02X}" for x in data),
+                len(data),
+            )
         self._data_receive_callback(data)
```

### Comparing `flux_led-1.0.0/flux_led/aioscanner.py` & `flux_led-1.0.1/flux_led/aioscanner.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/base_device.py` & `flux_led-1.0.1/flux_led/base_device.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/const.py` & `flux_led-1.0.1/flux_led/const.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/device.py` & `flux_led-1.0.1/flux_led/device.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/fluxled.py` & `flux_led-1.0.1/flux_led/fluxled.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/models_db.py` & `flux_led-1.0.1/flux_led/models_db.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/pattern.py` & `flux_led-1.0.1/flux_led/pattern.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/protocol.py` & `flux_led-1.0.1/flux_led/protocol.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/scanner.py` & `flux_led-1.0.1/flux_led/scanner.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/sock.py` & `flux_led-1.0.1/flux_led/sock.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/timer.py` & `flux_led-1.0.1/flux_led/timer.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led/utils.py` & `flux_led-1.0.1/flux_led/utils.py`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led.egg-info/PKG-INFO` & `flux_led-1.0.1/flux_led.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: flux-led
-Version: 1.0.0
+Version: 1.0.1
 Summary: A Python library to communicate with the flux_led smart bulbs
 Home-page: https://github.com/Danielhiversen/flux_led
 Author: Daniel Hjelseth Høyer
 Author-email: mail@dahoiv.net
 License: LGPLv3+
 Keywords: flux_led,smart bulbs,light
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `flux_led-1.0.0/flux_led.egg-info/SOURCES.txt` & `flux_led-1.0.1/flux_led.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/flux_led.egg-info/requires.txt` & `flux_led-1.0.1/flux_led.egg-info/requires.txt`

 * *Files identical despite different names*

### Comparing `flux_led-1.0.0/setup.py` & `flux_led-1.0.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -44,15 +44,15 @@
     ],
 }
 
 
 setup(
     name="flux_led",
     packages=["flux_led"],
-    version="1.0.0",
+    version="1.0.1",
     description="A Python library to communicate with the flux_led smart bulbs",
     author="Daniel Hjelseth Høyer",
     author_email="mail@dahoiv.net",
     url="https://github.com/Danielhiversen/flux_led",
     license="LGPLv3+",
     include_package_data=True,
     package_data={"flux_led": ["py.typed"]},
```

