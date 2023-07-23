# Comparing `tmp/selenium_driverless-1.0.3.tar.gz` & `tmp/selenium_driverless-1.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "selenium_driverless-1.0.3.tar", last modified: Sat Jul 22 12:43:58 2023, max compression
+gzip compressed data, was "selenium_driverless-1.0.4.tar", last modified: Sun Jul 23 12:37:54 2023, max compression
```

## Comparing `selenium_driverless-1.0.3.tar` & `selenium_driverless-1.0.4.tar`

### file list

```diff
@@ -1,34 +1,31 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 12:43:58.807123 selenium_driverless-1.0.3/
--rw-rw-rw-   0        0        0      688 2023-07-21 13:27:27.000000 selenium_driverless-1.0.3/LICENSE.md
--rw-rw-rw-   0        0        0       89 2023-01-11 09:10:16.000000 selenium_driverless-1.0.3/MANIFEST.in
--rw-rw-rw-   0        0        0     3397 2023-07-22 12:43:58.807123 selenium_driverless-1.0.3/PKG-INFO
--rw-rw-rw-   0        0        0     2081 2023-07-22 12:43:35.000000 selenium_driverless-1.0.3/README.md
--rw-rw-rw-   0        0        0      567 2023-07-21 21:05:54.000000 selenium_driverless-1.0.3/build_upload.md
--rw-rw-rw-   0        0        0      101 2022-11-24 08:05:09.000000 selenium_driverless-1.0.3/pyproject.toml
--rw-rw-rw-   0        0        0      133 2023-07-22 12:43:58.809134 selenium_driverless-1.0.3/setup.cfg
--rw-rw-rw-   0        0        0     1936 2023-07-21 20:56:42.000000 selenium_driverless-1.0.3/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-22 12:43:58.770367 selenium_driverless-1.0.3/src/
-drwxrwxrwx   0        0        0        0 2023-07-22 12:43:58.781846 selenium_driverless-1.0.3/src/selenium_driverless/
--rw-rw-rw-   0        0        0       23 2023-07-22 12:43:53.000000 selenium_driverless-1.0.3/src/selenium_driverless/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-22 12:43:58.795019 selenium_driverless-1.0.3/src/selenium_driverless/async_/
--rw-rw-rw-   0        0        0        0 2023-07-21 21:02:35.000000 selenium_driverless-1.0.3/src/selenium_driverless/async_/__init__.py
--rw-rw-rw-   0        0        0     2720 2023-07-21 20:13:40.000000 selenium_driverless-1.0.3/src/selenium_driverless/async_/mobile.py
--rw-rw-rw-   0        0        0    46666 2023-07-22 12:42:32.000000 selenium_driverless-1.0.3/src/selenium_driverless/async_/webdriver.py
-drwxrwxrwx   0        0        0        0 2023-07-22 12:43:58.796018 selenium_driverless-1.0.3/src/selenium_driverless/files/
--rw-rw-rw-   0        0        0        0 2023-07-21 16:36:38.000000 selenium_driverless-1.0.3/src/selenium_driverless/files/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-22 12:43:58.800117 selenium_driverless-1.0.3/src/selenium_driverless/scripts/
--rw-rw-rw-   0        0        0        0 2022-11-29 13:10:11.000000 selenium_driverless-1.0.3/src/selenium_driverless/scripts/__init__.py
--rw-rw-rw-   0        0        0     1400 2023-01-11 12:23:14.000000 selenium_driverless-1.0.3/src/selenium_driverless/scripts/multi_thread.py
--rw-rw-rw-   0        0        0    15809 2023-07-21 20:46:21.000000 selenium_driverless-1.0.3/src/selenium_driverless/scripts/options.py
-drwxrwxrwx   0        0        0        0 2023-07-22 12:43:58.803141 selenium_driverless-1.0.3/src/selenium_driverless/utils/
--rw-rw-rw-   0        0        0        0 2023-07-21 21:02:48.000000 selenium_driverless-1.0.3/src/selenium_driverless/utils/__init__.py
--rw-rw-rw-   0        0        0     3569 2023-07-21 19:38:37.000000 selenium_driverless-1.0.3/src/selenium_driverless/utils/utils.py
--rw-rw-rw-   0        0        0      386 2023-07-22 12:09:37.000000 selenium_driverless-1.0.3/src/selenium_driverless/webdriver.py
-drwxrwxrwx   0        0        0        0 2023-07-22 12:43:58.787952 selenium_driverless-1.0.3/src/selenium_driverless.egg-info/
--rw-rw-rw-   0        0        0     3397 2023-07-22 12:43:58.000000 selenium_driverless-1.0.3/src/selenium_driverless.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      800 2023-07-22 12:43:58.000000 selenium_driverless-1.0.3/src/selenium_driverless.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 12:43:58.000000 selenium_driverless-1.0.3/src/selenium_driverless.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      132 2023-07-22 12:43:58.000000 selenium_driverless-1.0.3/src/selenium_driverless.egg-info/requires.txt
--rw-rw-rw-   0        0        0       20 2023-07-22 12:43:58.000000 selenium_driverless-1.0.3/src/selenium_driverless.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-07-22 12:43:58.805118 selenium_driverless-1.0.3/tests/
--rw-rw-rw-   0        0        0     3238 2023-01-12 15:12:48.000000 selenium_driverless-1.0.3/tests/test_driverless.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:37:54.568357 selenium_driverless-1.0.4/
+-rw-rw-rw-   0        0        0      688 2023-07-21 13:27:27.000000 selenium_driverless-1.0.4/LICENSE.md
+-rw-rw-rw-   0        0        0       89 2023-01-11 09:10:16.000000 selenium_driverless-1.0.4/MANIFEST.in
+-rw-rw-rw-   0        0        0     3250 2023-07-23 12:37:54.568357 selenium_driverless-1.0.4/PKG-INFO
+-rw-rw-rw-   0        0        0     1934 2023-07-23 12:37:21.000000 selenium_driverless-1.0.4/README.md
+-rw-rw-rw-   0        0        0      567 2023-07-21 21:05:54.000000 selenium_driverless-1.0.4/build_upload.md
+-rw-rw-rw-   0        0        0      101 2022-11-24 08:05:09.000000 selenium_driverless-1.0.4/pyproject.toml
+-rw-rw-rw-   0        0        0      133 2023-07-23 12:37:54.569358 selenium_driverless-1.0.4/setup.cfg
+-rw-rw-rw-   0        0        0     1936 2023-07-21 20:56:42.000000 selenium_driverless-1.0.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:37:54.543040 selenium_driverless-1.0.4/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 12:37:54.553122 selenium_driverless-1.0.4/src/selenium_driverless/
+-rw-rw-rw-   0        0        0       23 2023-07-23 12:37:43.000000 selenium_driverless-1.0.4/src/selenium_driverless/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:37:54.560357 selenium_driverless-1.0.4/src/selenium_driverless/files/
+-rw-rw-rw-   0        0        0        0 2023-07-21 16:36:38.000000 selenium_driverless-1.0.4/src/selenium_driverless/files/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:37:54.564357 selenium_driverless-1.0.4/src/selenium_driverless/scripts/
+-rw-rw-rw-   0        0        0        0 2022-11-29 13:10:11.000000 selenium_driverless-1.0.4/src/selenium_driverless/scripts/__init__.py
+-rw-rw-rw-   0        0        0     2720 2023-07-21 20:13:40.000000 selenium_driverless-1.0.4/src/selenium_driverless/scripts/mobile.py
+-rw-rw-rw-   0        0        0     1400 2023-01-11 12:23:14.000000 selenium_driverless-1.0.4/src/selenium_driverless/scripts/multi_thread.py
+-rw-rw-rw-   0        0        0    16797 2023-07-23 12:34:39.000000 selenium_driverless-1.0.4/src/selenium_driverless/scripts/options.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:37:54.565358 selenium_driverless-1.0.4/src/selenium_driverless/utils/
+-rw-rw-rw-   0        0        0        0 2023-07-21 21:02:48.000000 selenium_driverless-1.0.4/src/selenium_driverless/utils/__init__.py
+-rw-rw-rw-   0        0        0     3625 2023-07-22 16:31:37.000000 selenium_driverless-1.0.4/src/selenium_driverless/utils/utils.py
+-rw-rw-rw-   0        0        0    47194 2023-07-23 12:36:44.000000 selenium_driverless-1.0.4/src/selenium_driverless/webdriver.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:37:54.559358 selenium_driverless-1.0.4/src/selenium_driverless.egg-info/
+-rw-rw-rw-   0        0        0     3250 2023-07-23 12:37:54.000000 selenium_driverless-1.0.4/src/selenium_driverless.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      714 2023-07-23 12:37:54.000000 selenium_driverless-1.0.4/src/selenium_driverless.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 12:37:54.000000 selenium_driverless-1.0.4/src/selenium_driverless.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      132 2023-07-23 12:37:54.000000 selenium_driverless-1.0.4/src/selenium_driverless.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       20 2023-07-23 12:37:54.000000 selenium_driverless-1.0.4/src/selenium_driverless.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 12:37:54.567358 selenium_driverless-1.0.4/tests/
+-rw-rw-rw-   0        0        0     3238 2023-01-12 15:12:48.000000 selenium_driverless-1.0.4/tests/test_driverless.py
```

### Comparing `selenium_driverless-1.0.3/LICENSE.md` & `selenium_driverless-1.0.4/LICENSE.md`

 * *Files identical despite different names*

### Comparing `selenium_driverless-1.0.3/PKG-INFO` & `selenium_driverless-1.0.4/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: selenium_driverless
-Version: 1.0.3
+Version: 1.0.4
 Summary: Undetected selenium without chromedriver usage
 Home-page: https://github.com/kaliiiiiiiiii/Selenium-Driverless
 Author: Aurin Aegerter
 Author-email: aurinliun@gmx.ch
 Project-URL: Documentation, https://github.com/kaliiiiiiiiii/Selenium-Driverless
 Project-URL: Bug Reports, https://github.com/kaliiiiiiiiii/Selenium-Driverless/issues
 Project-URL: Source Code, https://github.com/kaliiiiiiiiii/Selenium-Driverless
@@ -48,40 +48,35 @@
 * ```pip install selenium-driverless```
 
 
 ### Usage
 
 #### example script
 ```python
-import asyncio
+from selenium_driverless import webdriver
 
-
-async def main():
-    from selenium_driverless.async_.webdriver import ChromeDriver
-    from selenium_driverless.scripts.options import Options
-    options = Options()
-    async with ChromeDriver(options=options) as driver:
-        await driver.get('http://nowsecure.nl#relax')
-        await asyncio.sleep(4)
-        title = await driver.title
-        url = await driver.current_url
-        source = await driver.page_source
-        print(title)
-
-
-asyncio.run(main())
+options = webdriver.Options()
+with webdriver.Chrome(options=options) as driver:
+    driver.get('http://nowsecure.nl#relax')
+    driver.implicitly_wait(3)
+    
+    title = driver.title
+    url = driver.current_url
+    source = driver.page_source
+    print(title)
 ```
 
 ## Help
 
 Please feel free to open an issue or fork!
 
 ## Todo
 
-
+- implementations
+  - [ ] find element
 
 ## Deprecated
 
 ## Authors
 
 [Aurin Aegerter](mailto:aurinliun@gmx.ch)
```

### Comparing `selenium_driverless-1.0.3/build_upload.md` & `selenium_driverless-1.0.4/build_upload.md`

 * *Files identical despite different names*

### Comparing `selenium_driverless-1.0.3/setup.py` & `selenium_driverless-1.0.4/setup.py`

 * *Files identical despite different names*

### Comparing `selenium_driverless-1.0.3/src/selenium_driverless/async_/mobile.py` & `selenium_driverless-1.0.4/src/selenium_driverless/scripts/mobile.py`

 * *Files identical despite different names*

### Comparing `selenium_driverless-1.0.3/src/selenium_driverless/async_/webdriver.py` & `selenium_driverless-1.0.4/src/selenium_driverless/webdriver.py`

 * *Files 11% similar despite different names*

```diff
@@ -18,65 +18,61 @@
 # modified by kaliiiiiiiiii | Aurin Aegerter
 
 """The WebDriver implementation."""
 import asyncio
 import contextlib
 import copy
 import os.path
-import pkgutil
 import subprocess
-import types
 import typing
 import warnings
 from abc import ABCMeta
 from base64 import b64decode
 from base64 import urlsafe_b64encode
 from contextlib import asynccontextmanager
 from importlib import import_module
 from typing import Dict
 from typing import List
 from typing import Optional
 from typing import Union
 
+import pycdp.cdp.target
 from selenium.common.exceptions import InvalidArgumentException
 from selenium.common.exceptions import JavascriptException
 from selenium.common.exceptions import NoSuchCookieException
 from selenium.common.exceptions import NoSuchElementException
 from selenium.common.exceptions import WebDriverException
 from selenium.webdriver.common.by import By
 from selenium.webdriver.common.html5.application_cache import ApplicationCache
+
 from selenium_driverless.scripts.options import Options as BaseOptions
 from selenium.webdriver.common.print_page_options import PrintOptions
 from selenium.webdriver.common.timeouts import Timeouts
 from selenium.webdriver.common.virtual_authenticator import Credential
 from selenium.webdriver.common.virtual_authenticator import VirtualAuthenticatorOptions
 from selenium.webdriver.common.virtual_authenticator import (
     required_virtual_authenticator,
 )
 from selenium.webdriver.remote.bidi_connection import BidiConnection
 from selenium.webdriver.remote.command import Command
 from selenium.webdriver.remote.errorhandler import ErrorHandler
 from selenium.webdriver.remote.file_detector import FileDetector
 from selenium.webdriver.remote.file_detector import LocalFileDetector
-from selenium_driverless.async_.mobile import Mobile
+from selenium_driverless.scripts.mobile import Mobile
 from selenium.webdriver.remote.script_key import ScriptKey
 from selenium.webdriver.remote.shadowroot import ShadowRoot
 from selenium.webdriver.remote.switch_to import SwitchTo
 from selenium.webdriver.remote.webelement import WebElement
 from selenium.webdriver.support.relative_locator import RelativeBy
 from selenium.webdriver.common.desired_capabilities import DesiredCapabilities
 from selenium_driverless.scripts.options import Options
 
-cdp = None
-
 
 def import_cdp():
-    global cdp
-    if not cdp:
-        cdp = import_module("selenium.webdriver.common.bidi.cdp")
+    return import_module("selenium.webdriver.common.bidi.cdp")
 
 
 def _create_caps(caps):
     """Makes a W3C alwaysMatch capabilities object.
 
     Filters out capability names that are not in the W3C spec. Spec-compliant
     drivers will reject requests containing unknown capability names.
@@ -132,39 +128,37 @@
     """Abstract Base Class for all Webdriver subtypes.
 
     ABC's allow custom implementations of Webdriver to be registered so
     that isinstance type checks will succeed.
     """
 
 
-class ChromeDriver(BaseWebDriver):
+class Chrome(BaseWebDriver):
     """Allows you to drive the browser without chromedriver."""
 
     _web_element_cls = WebElement
     _shadowroot_cls = ShadowRoot
 
     def __init__(
             self,
-            options: Options = None
+            options: Options = None,
+            loop: asyncio.AbstractEventLoop = None
     ) -> None:
         """Creates a new instance of the chrome driver. Starts the service and
         then creates new instance of chrome driver.
 
         :Args:
          - options - this takes an instance of ChromeOptions
         """
+        self._conn = None
         self.session = None
-        self.conn = None
         self.browser_pid = None
-        async_used = None
-        try:
-            self._loop = asyncio.get_running_loop()
-            async_used = True
-        except RuntimeError:
-            self._loop = asyncio.get_event_loop()
+        if not loop:
+            loop = asyncio.get_event_loop()
+        self._loop = loop
 
         try:
             options = options or Options()
             self._options = options
 
             browser_name = DesiredCapabilities.CHROME["browserName"],
             vendor_prefix = "goog"
@@ -180,37 +174,29 @@
             self.pinned_scripts = {}
             self.error_handler = ErrorHandler()
             self._switch_to = SwitchTo(self)
             self._mobile = Mobile(self)
             self.file_detector = LocalFileDetector()
             self._authenticator_id = None
             self.start_client()
-            if not async_used:
-                self._loop.run_until_complete(self.start_session(self._capabilities))
+            self.start_session(self._capabilities)
 
         except Exception:
-            if not async_used:
-                self._loop.run_until_complete(self.quit())
+            self.quit()
             raise
         self._is_remote = False
 
     def __repr__(self):
         return f'<{type(self).__module__}.{type(self).__name__} (session="{self.target_id}")>'
 
     def __enter__(self):
         return self
 
-    async def __aexit__(self, exc_type, exc_val, exc_tb):
-        await self.quit()
-
-    def __await__(self):
-        return self.start_session().__await__()
-
-    async def __aenter__(self):
-        return await self.start_session()
+    def __exit__(self, exc_type, exc_val, exc_tb):
+        self.quit()
 
     @property
     def mobile(self) -> Mobile:
         return self._mobile
 
     @property
     def name(self) -> str:
@@ -236,15 +222,15 @@
         """Called after executing a quit command.
 
         This method may be overridden to define custom shutdown
         behavior.
         """
         pass
 
-    async def start_session(self, capabilities: dict or None = None) -> None:
+    def start_session(self, capabilities: dict or None = None):
         """Creates a new session with the desired capabilities.
 
         :Args:
          - capabilities - a capabilities dict to start the session with.
         """
         if not capabilities:
             capabilities = self._capabilities
@@ -263,26 +249,25 @@
             stderr=subprocess.PIPE,
             close_fds=IS_POSIX,
         )
 
         if self._options.debugger_address.split(":")[1] == "0":
             path = self._options.user_data_dir + "/DevToolsActivePort"
             while not os.path.isfile(path):
-                await asyncio.sleep(0.1)
+                self.implicitly_wait(0.1)
             self._options.debugger_address = "localhost:" + read(path, sel_root=False).split("\n")[0]
-        self.conn = await connect_cdp(f'http://{self._options.debugger_address}')
+        self._conn = self._loop.run_until_complete(connect_cdp(f'http://{self._options.debugger_address}'))
         self.browser_pid = browser.pid
-        targets = await self.conn.execute(cdp.target.get_targets())
+        targets = self._loop.run_until_complete(self._conn.execute(cdp.target.get_targets()))
         for target in targets:
             if target.type_ == "page":
                 self.target_id = target.target_id
                 break
-        self.session = await self.conn.connect_session(self.target_id)
+        self.session = self._loop.run_until_complete(self._conn.connect_session(self.target_id))
         self.caps = capabilities
-        return self
 
     def _wrap_value(self, value):
         if isinstance(value, dict):
             converted = {}
             for key, val in value.items():
                 converted[key] = self._wrap_value(val)
             return converted
@@ -307,49 +292,45 @@
             for key, val in value.items():
                 value[key] = self._unwrap_value(val)
             return value
         if isinstance(value, list):
             return list(self._unwrap_value(item) for item in value)
         return value
 
-    async def execute(self, driver_command: str, params: dict = None) -> dict:
-        """Sends a command to be executed by a command.CommandExecutor.
-
-        :Args:
-         - driver_command: The name of the command to execute as a string.
-         - params: A dictionary of named parameters to send with the command.
-
-        :Returns:
-          The command's JSON response loaded into a dictionary object.
+    def execute(self, driver_command: str = None, params: dict = None, cmd=None):
         """
-        if driver_command == "executeCdpCommand":
-            value = await self.execute_cdp_cmd(params["script"], params["params"])
-            return {"success": 0, "value": value, "sessionId": self.target_id}
-        else:
+        executes on current pycdp.cdp cmd on current session
+        driver_command and params aren't used
+        """
+        if driver_command or params:
             raise NotImplementedError("chrome not started with chromedriver")
+        return self._loop.run_until_complete(self.session.execute(cmd=cmd))
 
-    async def get(self, url: str) -> None:
-        from pycdp import cdp
+    def get(self, url: str) -> None:
         """Loads a web page in the current browser session."""
-        await self.session.execute(cdp.page.enable())
-        with self.session.safe_wait_for(cdp.page.DomContentEventFired) as navigation:
-            await self.session.execute(cdp.page.navigate(url))
-            await navigation
+        from pycdp import cdp
+        self.execute(cmd=cdp.page.enable())
+
+        async def get(_url: str):
+            with self.session.safe_wait_for(cdp.page.DomContentEventFired) as navigation:
+                await self.session.execute(cmd=cdp.page.navigate(_url))
+                await navigation
+
+        self._loop.run_until_complete(get(url))
 
     @property
-    async def title(self) -> str:
+    def title(self) -> str:
         """Returns the title of the current page.
 
         :Usage:
             ::
 
                 title = driver.title
         """
-        target = await self.current_target
-        return target.title
+        return self.current_target.title
 
     def pin_script(self, script: str, script_key=None) -> ScriptKey:
         """Store common javascript scripts to be executed later by a unique
         hashable ID."""
         script_key_instance = ScriptKey(script_key)
         self.pinned_scripts[script_key_instance.id] = script
         return script_key_instance
@@ -360,15 +341,15 @@
             self.pinned_scripts.pop(script_key.id)
         except KeyError:
             raise KeyError(f"No script with key: {script_key} existed in {self.pinned_scripts}") from None
 
     def get_pinned_scripts(self) -> List[str]:
         return list(self.pinned_scripts)
 
-    async def execute_script(self, script, *args):
+    def execute_script(self, script, *args):
         """Synchronously Executes JavaScript in the current window/frame.
 
         :Args:
          - script: The JavaScript to execute.
          - \\*args: Any applicable arguments for your JavaScript.
 
         :Usage:
@@ -383,17 +364,17 @@
                 script = self.pinned_scripts[script.id]
             except KeyError:
                 raise JavascriptException("Pinned script could not be found")
 
         script = f"(function(...arguments){{{script}}})(...{json.dumps(args)})"
 
         script = cdp.runtime.evaluate(expression=script, include_command_line_api=True,
-                                      user_gesture=True, await_promise=True,
-                                      allow_unsafe_eval_blocked_by_csp=True)
-        result = await self.session.execute(script)
+                                      user_gesture=True, await_promise=False,
+                                      allow_unsafe_eval_blocked_by_csp=True, return_by_value=True)
+        result = self.execute(cmd=script)
         if result[1]:
             class JSEvalException(result[1], Exception):
                 pass
 
             raise JSEvalException(result[1].description)
         return result[0].value
 
@@ -407,170 +388,179 @@
         :Usage:
             ::
 
                 script = "var callback = arguments[arguments.length - 1]; " \\
                          "window.setTimeout(function(){ callback('timeout') }, 3000);"
                 driver.execute_async_script(script)
         """
-        converted_args = list(args)
-        command = Command.W3C_EXECUTE_SCRIPT_ASYNC
-
-        return self.execute(command, {"script": script, "args": converted_args})["value"]
+        from pycdp import cdp
+        import json
+        script = """
+        (function(...arguments){
+            const promise = new Promise((resolve, reject) => {
+                arguments.push(resolve)
+            });""" + script + "return promise})(..." + json.dumps(args) + ")"
+        script = cdp.runtime.evaluate(expression=script, include_command_line_api=True,
+                                      user_gesture=True, await_promise=True,
+                                      allow_unsafe_eval_blocked_by_csp=True)
+        result = self.execute(cmd=script)
+        if result[1]:
+            raise Exception(result[1].description)
+        return result[0].value
 
     @property
-    async def current_url(self) -> str:
+    def current_url(self) -> str:
         """Gets the URL of the current page.
 
         :Usage:
             ::
 
                 driver.current_url
         """
-        target = await self.current_target
-        return target.url
+        return self.current_target.url
 
     @property
-    async def page_source(self) -> str:
+    def page_source(self) -> str:
         """Gets the source of the current page.
 
         :Usage:
             ::
 
                 driver.page_source
         """
-        return await self.execute_script("return document.documentElement.outerHTML")
+        return self.execute_script("return document.documentElement.outerHTML")
 
-    async def close(self) -> None:
+    def close(self) -> None:
         """Closes the current window.
 
         :Usage:
             ::
 
                 driver.close()
         """
         from pycdp import cdp
-        await self.session.execute(cdp.page.close())
+        self.execute(cmd=cdp.page.close())
 
-    async def quit(self) -> None:
+    def quit(self) -> None:
         """Quits the driver and closes every associated window.
 
         :Usage:
             ::
 
                 driver.quit()
         """
         import os
         import shutil
         # noinspection PyBroadException
         try:
             try:
-                await self.close()
+                self.close()
 
                 # wait for process to be killed
                 while True:
                     try:
                         os.kill(self.browser_pid, 15)
                     except OSError:
                         break
-                    await asyncio.sleep(0.1)
+                    self.implicitly_wait(0.1)
 
                 shutil.rmtree(self._options.user_data_dir, ignore_errors=True)
             finally:
                 self.stop_client()
         except Exception as e:
             # We don't care about the message because something probably has gone wrong
             pass
         finally:
             pass  # self.service.stop()
 
     @property
-    async def targets(self):
+    def targets(self):
         from pycdp import cdp
-        return await self.conn.execute(cdp.target.get_targets())
+        return self.execute(cmd=cdp.target.get_targets())
 
     @property
-    async def current_target(self):
-        for target in await self.targets:
-            if target.attached:
-                return target
+    def current_target(self):
+        from pycdp import cdp
+        return self.execute(cmd=cdp.target.get_target_info(self.current_window_handle))
 
     @property
-    async def current_window_handle(self) -> str:
+    def current_window_handle(self) -> pycdp.cdp.target.TargetID:
         """Returns the handle of the current window.
 
         :Usage:
             ::
 
                 driver.current_window_handle
         """
-        target = await self.current_target
-        return target.target_id
+        # noinspection PyProtectedMember
+        return self.session._target_id
 
     @property
-    async def current_window_id(self):
+    def current_window_id(self):
         from pycdp import cdp
-        target = await self.current_target
-        target_id = target.target_id
+        target_id = self.current_window_handle
         script = cdp.browser.get_window_for_target(target_id)
-        result = await self.conn.execute(script)
+        result = self.execute(cmd=script)
         return result[0]
 
     @property
-    async def window_handles(self) -> List[str]:
+    def window_handles(self) -> List[str]:
         """Returns the handles of all windows within the current session.
 
         :Usage:
             ::
 
                 driver.window_handles
         """
+        warnings.warn("window_handles aren't ordered by tab position")
         tabs = []
-        for target in await self.targets:
+        for target in self.targets:
             if target.type_ == "page":
                 tabs.append(target.target_id)
         return tabs
 
-    async def set_window_state(self, state):
+    def set_window_state(self, state):
         states = ["normal", "minimized", "maximized", "fullscreen"]
         if state not in states:
             raise ValueError(f"expected one of {states}, but got: {state}")
-        window_id = await self.current_window_id
+        window_id = self.current_window_id
         bounds = {"windowState": state}
-        await self.execute_cdp_cmd("Browser.setWindowBounds", {"bounds": bounds, "windowId": window_id})
+        self.execute_cdp_cmd("Browser.setWindowBounds", {"bounds": bounds, "windowId": window_id})
 
-    async def normalize_window(self):
-        await self.set_window_state("normal")
+    def normalize_window(self):
+        self.set_window_state("normal")
 
-    async def maximize_window(self) -> None:
+    def maximize_window(self) -> None:
         """Maximizes the current window that webdriver is using."""
-        await self.normalize_window()
-        await self.set_window_state("maximized")
+        self.normalize_window()
+        self.set_window_state("maximized")
 
-    async def fullscreen_window(self) -> None:
+    def fullscreen_window(self) -> None:
         """Invokes the window manager-specific 'full screen' operation."""
-        await self.normalize_window()
-        await self.set_window_state("fullscreen")
+        self.normalize_window()
+        self.set_window_state("fullscreen")
 
-    async def minimize_window(self) -> None:
-        await self.normalize_window()
+    def minimize_window(self) -> None:
+        self.normalize_window()
         """Invokes the window manager-specific 'minimize' operation."""
-        await self.set_window_state("maximized")
+        self.set_window_state("maximized")
 
-    async def print_page(self, print_options: Optional[PrintOptions] = None) -> str:
+    def print_page(self, print_options: Optional[PrintOptions] = None) -> str:
         """Takes PDF of the current page.
 
         The driver makes a best effort to return a PDF based on the
         provided parameters.
         """
         from pycdp import cdp
         options = {}
         if print_options:
             options = print_options.to_dict()
             raise NotImplementedError()
-        page = await self.session.execute(cdp.page.print_to_pdf())
+
+        page = self.execute(cmd=cdp.page.print_to_pdf())
         return page[0]
 
     @property
     def switch_to(self) -> SwitchTo:
         """
         :Returns:
             - SwitchTo: an object containing all options to switch focus into
@@ -583,15 +573,23 @@
                 driver.switch_to.default_content()
                 driver.switch_to.frame('frame_name')
                 driver.switch_to.frame(1)
                 driver.switch_to.frame(driver.find_elements(By.TAG_NAME, "iframe")[0])
                 driver.switch_to.parent_frame()
                 driver.switch_to.window('main')
         """
-        return self._switch_to
+        raise NotImplementedError("You might use driver.switch_to_target(driver.targets[0].target_id.) instead")
+        # return self._switch_to
+
+    def switch_to_target(self, target_id):
+        from pycdp import cdp
+        self.session.close()
+        self.session = self._loop.run_until_complete(self._conn.connect_session(target_id))
+        self.execute(cmd=cdp.target.activate_target(self.current_window_handle))
+        return self.session
 
     # Navigation
     def back(self) -> None:
         """Goes one step backward in the browser history.
 
         :Usage:
             ::
@@ -615,15 +613,15 @@
 
         :Usage:
             ::
 
                 driver.refresh()
         """
         from pycdp import cdp
-        await  self.session.execute(cdp.page.reload())
+        self.execute(cmd=cdp.page.reload())
 
     # Options
     def get_cookies(self) -> List[dict]:
         """Returns a set of dictionaries, corresponding to cookies visible in
         the current session.
 
         :Usage:
@@ -698,15 +696,15 @@
          - time_to_wait: Amount of time to wait (in seconds)
 
         :Usage:
             ::
 
                 driver.implicitly_wait(30)
         """
-        self.execute(Command.SET_TIMEOUTS, {"implicit": int(float(time_to_wait) * 1000)})
+        self._loop.run_until_complete(asyncio.sleep(time_to_wait))
 
     def set_script_timeout(self, time_to_wait: float) -> None:
         """Set the amount of time that the script should wait during an
         execute_async_script call before throwing an error.
 
         :Args:
          - time_to_wait: The amount of time to wait (in seconds)
@@ -761,26 +759,27 @@
                     ::
                         my_timeouts = Timeouts()
                         my_timeouts.implicit_wait = 10
                         driver.timeouts = my_timeouts
                 """
         _ = self.execute(Command.SET_TIMEOUTS, timeouts._to_json())["value"]
 
-    async def find_element(self, by=By.ID, value: Optional[str] = None) -> WebElement:
+    def find_element(self, by=By.ID, value: Optional[str] = None) -> WebElement:
         """Find an element given a By strategy and locator.
 
         :Usage:
             ::
 
                 element = driver.find_element(By.ID, 'foo')
 
         :rtype: WebElement
         """
+        # by = RelativeBy({by: value})
         if isinstance(by, RelativeBy):
-            elements = await self.find_elements(by=by, value=value)
+            elements = self.find_elements(by=by, value=value)
             if not elements:
                 raise NoSuchElementException(f"Cannot locate relative element with: {by.root}")
             return elements[0]
 
         if by == By.ID:
             by = By.CSS_SELECTOR
             value = f'[id="{value}"]'
@@ -789,29 +788,31 @@
             value = f".{value}"
         elif by == By.NAME:
             by = By.CSS_SELECTOR
             value = f'[name="{value}"]'
 
         return self.execute(Command.FIND_ELEMENT, {"using": by, "value": value})["value"]
 
-    async def find_elements(self, by=By.ID, value: Optional[str] = None) -> List[WebElement]:
+    def find_elements(self, by=By.ID, value: Optional[str] = None) -> List[WebElement]:
         """Find elements given a By strategy and locator.
 
         :Usage:
             ::
 
                 elements = driver.find_elements(By.CLASS_NAME, 'foo')
 
         :rtype: list of WebElement
         """
+        from selenium_driverless.utils.utils import sel_path, read
+        by = RelativeBy({by: value})
         if isinstance(by, RelativeBy):
             _pkg = ".".join(__name__.split(".")[:-1])
-            raw_function = pkgutil.get_data(_pkg, "findElements.js").decode("utf8")
+            raw_function = read(sel_path() + "webdriver/remote/findElements.js", sel_root=False)
             find_element_js = f"/* findElements */return ({raw_function}).apply(null, arguments);"
-            return await self.execute_script(find_element_js, by.to_dict())
+            return self.execute_script(find_element_js, by.to_dict())
 
         if by == By.ID:
             by = By.CSS_SELECTOR
             value = f'[id="{value}"]'
         elif by == By.CLASS_NAME:
             by = By.CSS_SELECTOR
             value = f".{value}"
@@ -844,153 +845,153 @@
                         driver.get_screenshot_as_file('/Screenshots/foo.png')
                 """
         if not str(filename).lower().endswith(".png"):
             warnings.warn(
                 "name used for saved screenshot does not match file " "type. It should end with a `.png` extension",
                 UserWarning,
             )
-        png = await self.get_screenshot_as_png()
+        png = self.get_screenshot_as_png()
         try:
             with open(filename, "wb") as f:
                 f.write(png)
         except OSError:
             return False
         finally:
             del png
         return True
 
-    async def save_screenshot(self, filename) -> bool:
+    def save_screenshot(self, filename) -> bool:
         # noinspection GrazieInspection
         """Saves a screenshot of the current window to a PNG image file.
                 Returns False if there is any IOError, else returns True. Use full
                 paths in your filename.
 
                 :Args:
                  - filename: The full path you wish to save your screenshot to. This
                    should end with a `.png` extension.
 
                 :Usage:
                     ::
 
                         driver.save_screenshot('/Screenshots/foo.png')
                 """
-        return await self.get_screenshot_as_file(filename)
+        return self.get_screenshot_as_file(filename)
 
-    async def get_screenshot_as_png(self) -> bytes:
+    def get_screenshot_as_png(self) -> bytes:
         """Gets the screenshot of the current window as a binary data.
 
         :Usage:
             ::
 
                 driver.get_screenshot_as_png()
         """
-        base_64 = await self.get_screenshot_as_base64()
+        base_64 = self.get_screenshot_as_base64()
         return b64decode(base_64.encode("ascii"))
 
-    async def get_screenshot_as_base64(self) -> str:
+    def get_screenshot_as_base64(self) -> str:
         """Gets the screenshot of the current window as a base64 encoded string
         which is useful in embedded images in HTML.
 
         :Usage:
             ::
 
                 driver.get_screenshot_as_base64()
         """
         from pycdp import cdp
-        return await self.session.execute(cdp.page.capture_screenshot(format_="png"))
+        return self.execute(cmd=cdp.page.capture_screenshot(format_="png"))
 
     # noinspection PyPep8Naming
-    async def set_window_size(self, width, height, windowHandle: str = "current") -> None:
+    def set_window_size(self, width, height, windowHandle: str = "current") -> None:
         """Sets the width and height of the current window. (window.resizeTo)
 
         :Args:
          - width: the width in pixels to set the window to
          - height: the height in pixels to set the window to
 
         :Usage:
             ::
 
                 driver.set_window_size(800,600)
         """
         if windowHandle != "current":
             warnings.warn("Only 'current' window is supported for W3C compatible browsers.")
-        await self.set_window_rect(width=int(width), height=int(height))
+        self.set_window_rect(width=int(width), height=int(height))
 
     # noinspection PyPep8Naming
-    async def get_window_size(self, windowHandle: str = "current") -> dict:
+    def get_window_size(self, windowHandle: str = "current") -> dict:
         """Gets the width and height of the current window.
 
         :Usage:
             ::
 
                 driver.get_window_size()
         """
 
         if windowHandle != "current":
             warnings.warn("Only 'current' window is supported for W3C compatible browsers.")
-        size = await self.get_window_rect()
+        size = self.get_window_rect()
 
         if size.get("value", None):
             size = size["value"]
 
         return {k: size[k] for k in ("width", "height")}
 
     # noinspection PyPep8Naming
-    async def set_window_position(self, x, y, windowHandle: str = "current") -> dict:
+    def set_window_position(self, x, y, windowHandle: str = "current") -> dict:
         """Sets the x,y position of the current window. (window.moveTo)
 
         :Args:
          - x: the x-coordinate in pixels to set the window position
          - y: the y-coordinate in pixels to set the window position
 
         :Usage:
             ::
 
                 driver.set_window_position(0,0)
         """
         if windowHandle != "current":
             warnings.warn("Only 'current' window is supported for W3C compatible browsers.")
-        return await self.set_window_rect(x=int(x), y=int(y))
+        return self.set_window_rect(x=int(x), y=int(y))
 
     # noinspection PyPep8Naming
-    async def get_window_position(self, windowHandle="current") -> dict:
+    def get_window_position(self, windowHandle="current") -> dict:
         """Gets the x,y position of the current window.
 
         :Usage:
             ::
 
                 driver.get_window_position()
         """
 
         if windowHandle != "current":
             warnings.warn("Only 'current' window is supported for W3C compatible browsers.")
-        position = await self.get_window_rect()
+        position = self.get_window_rect()
 
         return {k: position[k] for k in ("x", "y")}
 
-    async def get_window_rect(self) -> dict:
+    def get_window_rect(self) -> dict:
         """Gets the x, y coordinates of the window as well as height and width
         of the current window.
 
         :Usage:
             ::
 
                 driver.get_window_rect()
         """
         from pycdp import cdp
-        script = cdp.browser.get_window_bounds(await self.current_window_id)
-        bounds = await self.conn.execute(script)
+        script = cdp.browser.get_window_bounds(self.current_window_id)
+        bounds = self.execute(cmd=script)
         json = bounds.to_json()
         json["x"] = json["left"]
         del json["left"]
         json["y"] = json["top"]
         del json["top"]
         return json
 
-    async def set_window_rect(self, x=None, y=None, width=None, height=None) -> dict:
+    def set_window_rect(self, x=None, y=None, width=None, height=None) -> dict:
         """Sets the x, y coordinates of the window as well as height and width
         of the current window. This method is only supported for W3C compatible
         browsers; other browsers should use `set_window_position` and
         `set_window_size`.
 
         :Usage:
             ::
@@ -1004,16 +1005,16 @@
         if (x is None and y is None) and (not height and not width):
             raise InvalidArgumentException("x and y or height and width need values")
 
         json = {"left": x, "top": y, "width": width, 'height': height}
         bounds = cdp.browser.Bounds()
         bounds = bounds.from_json(json=json)
 
-        script = cdp.browser.set_window_bounds(await self.current_window_id, bounds)
-        await self.conn.execute(script)
+        script = cdp.browser.set_window_bounds(self.current_window_id, bounds)
+        self.execute(cmd=script)
         json["x"] = json["left"]
         del json["left"]
         json["y"] = json["top"]
         del json["top"]
 
         return json
 
@@ -1100,16 +1101,15 @@
                 driver.get_log('client')
                 driver.get_log('server')
         """
         return self.execute(Command.GET_LOG, {"type": log_type})["value"]
 
     @asynccontextmanager
     async def bidi_connection(self):
-        global cdp
-        import_cdp()
+        cdp = import_cdp()
         if self.caps.get("se:cdp"):
             ws_url = self.caps.get("se:cdp")
             version = self.caps.get("se:cdpVersion").split(".")[0]
         else:
             version, ws_url = self._get_cdp_details()
 
         if not ws_url:
@@ -1228,35 +1228,43 @@
                     offline=False,
                     latency=5,  # additional latency (ms)
                     download_throughput=500 * 1024,  # maximal throughput
                     upload_throughput=500 * 1024)  # maximal throughput
 
             Note: 'throughput' can be used to set both (for download and upload).
         """
-        self.execute("setNetworkConditions", {"network_conditions": network_conditions})
+        from pycdp import cdp
+        self.execute(cmd=cdp.network.emulate_network_conditions(**network_conditions))
 
     def delete_network_conditions(self) -> None:
         """Resets Chromium network emulation settings."""
         self.execute("deleteNetworkConditions")
 
-    def set_permissions(self, name: str, value: str) -> None:
+    def set_permissions(self, name: str, value: str, origin: str = None) -> None:
         """Sets Applicable Permission.
 
         :Args:
          - name: The item to set the permission on.
          - value: The value to set on the item
 
         :Usage:
             ::
 
                 driver.set_permissions('clipboard-read', 'denied')
         """
-        self.execute("setPermissions", {"descriptor": {"name": name}, "state": value})
+        settings = ["granted", "denied", "prompt"]
+        if value not in settings:
+            raise ValueError(f"value needs to be within {settings}, but got {value}")
+        args = {"permission": {"name": name}, "setting": value}
+        if origin:
+            args["origin"] = origin
+        from pycdp import cdp
+        self.execute_cdp_cmd("Browser.setPermission", args)
 
-    async def execute_cdp_cmd(self, cmd: str, cmd_args: dict or None = None):
+    def execute_cdp_cmd(self, cmd: str, cmd_args: dict or None = None):
         """Execute Chrome Devtools Protocol command and get returned result The
         command and command args should follow chrome devtools protocol
         domains/commands, refer to link
         https://chromedevtools.github.io/devtools-protocol/
 
         :Args:
          - cmd: A str, command name
@@ -1269,26 +1277,27 @@
             A dict, empty dict {} if there is no result to return.
             For example to getResponseBody:
             {'base64Encoded': False, 'body': 'response body string'}
         """
         if not cmd_args:
             cmd_args = {}
 
-        def execute_cdp_cmd(cmd_dict):
-            json = yield cmd_dict
+        def execute_cdp_cmd(_cmd_dict):
+            json = yield _cmd_dict
             return json
 
         cmd_dict = dict(method=cmd, params=cmd_args)
         request = execute_cdp_cmd(cmd_dict)
-        return await self.session.execute(request)
+        return self.execute(cmd=request)
 
     def get_sinks(self) -> list:
         """
         :Returns: A list of sinks available for Cast.
         """
+        self.execute_cdp_cmd("Cast.enable")
         return self.execute("getSinks")["value"]
 
     def get_issue_message(self):
         """
         :Returns: An error message when there is any issue in a Cast session.
         """
         return self.execute("getIssueMessage")["value"]
@@ -1296,32 +1305,32 @@
     def set_sink_to_use(self, sink_name: str) -> dict:
         """Sets a specific sink, using its name, as a Cast session receiver
         target.
 
         :Args:
          - sink_name: Name of the sink to use as the target.
         """
-        return self.execute("setSinkToUse", {"sinkName": sink_name})
+        return self.execute_cdp_cmd("Cast.setSinkToUse", {"sinkName": sink_name})
 
     def start_desktop_mirroring(self, sink_name: str) -> dict:
         """Starts a desktop mirroring session on a specific receiver target.
 
         :Args:
          - sink_name: Name of the sink to use as the target.
         """
-        return self.execute("startDesktopMirroring", {"sinkName": sink_name})
+        return self.execute_cdp_cmd("Cast.startDesktopMirrorin", {"sinkName": sink_name})
 
     def start_tab_mirroring(self, sink_name: str) -> dict:
         """Starts a tab mirroring session on a specific receiver target.
 
         :Args:
          - sink_name: Name of the sink to use as the target.
         """
-        return self.execute("startTabMirroring", {"sinkName": sink_name})
+        return self.execute_cdp_cmd("Cast.startTabMirroring", {"sinkName": sink_name})
 
     def stop_casting(self, sink_name: str) -> dict:
         """Stops the existing Cast session on a specific receiver target.
 
         :Args:
          - sink_name: Name of the sink to stop the Cast session.
         """
-        return self.execute("stopCasting", {"sinkName": sink_name})
+        return self.execute_cdp_cmd("Cast.stopCasting", {"sinkName": sink_name})
```

### Comparing `selenium_driverless-1.0.3/src/selenium_driverless/scripts/multi_thread.py` & `selenium_driverless-1.0.4/src/selenium_driverless/scripts/multi_thread.py`

 * *Files identical despite different names*

### Comparing `selenium_driverless-1.0.3/src/selenium_driverless/scripts/options.py` & `selenium_driverless-1.0.4/src/selenium_driverless/scripts/options.py`

 * *Files 18% similar despite different names*

```diff
@@ -24,25 +24,26 @@
 from typing import Union, Optional, List, BinaryIO
 
 from selenium.common.exceptions import InvalidArgumentException
 from selenium.webdriver.common.desired_capabilities import DesiredCapabilities
 from selenium.webdriver.common.proxy import Proxy
 
 
+# noinspection PyUnreachableCode
 class Options(metaclass=ABCMeta):
     KEY = "goog:chromeOptions"
 
     def __init__(self) -> None:
         from selenium_driverless.utils.utils import find_chrome_executable, sel_driverless_path, random_port
         import uuid
         super().__init__()
 
         self._caps = self.default_capabilities
         self._proxy = None
-        self.set_capability("pageLoadStrategy", "normal")
+        # self.set_capability("pageLoadStrategy", "normal")
         self.mobile_options = None
 
         self._binary_location = find_chrome_executable()
         self._extension_files = []
         self._extensions = []
         self._experimental_options = {}
         self._debugger_address = None
@@ -55,104 +56,115 @@
 
     @property
     def capabilities(self):
         return self._caps
 
     def set_capability(self, name, value) -> None:
         """Sets a capability."""
+        raise NotImplementedError()
         self._caps[name] = value
 
     @property
     def browser_version(self) -> str:
         """
         :returns: the version of the browser if set, otherwise None.
         """
+        raise NotImplementedError()
         return self._caps.get("browserVersion")
 
     @browser_version.setter
     def browser_version(self, version: str) -> None:
         """Requires the major version of the browser to match provided value:
         https://w3c.github.io/webdriver/#dfn-browser-version.
 
         :param version: The required version of the browser
         """
+        raise NotImplementedError()
         self.set_capability("browserVersion", version)
 
     @property
     def platform_name(self) -> str:
         """
         :returns: The name of the platform
         """
+        raise NotImplementedError()
         return self._caps["platformName"]
 
     @platform_name.setter
     def platform_name(self, platform: str) -> None:
         """Requires the platform to match the provided value:
         https://w3c.github.io/webdriver/#dfn-platform-name.
 
         :param platform: the required name of the platform
         """
+        raise NotImplementedError()
         self.set_capability("platformName", platform)
 
     @property
     def page_load_strategy(self) -> str:
         """
         :returns: page load strategy if set, the default is "normal"
         """
+        raise NotImplementedError()
         return self._caps["pageLoadStrategy"]
 
     @page_load_strategy.setter
     def page_load_strategy(self, strategy: str) -> None:
         """Determines the point at which a navigation command is returned:
         https://w3c.github.io/webdriver/#dfn-table-of-page-load-strategies.
 
         :param strategy: the strategy corresponding to a document readiness state
         """
+        raise NotImplementedError()
         if strategy in ["normal", "eager", "none"]:
             self.set_capability("pageLoadStrategy", strategy)
         else:
             raise ValueError("Strategy can only be one of the following: normal, eager, none")
 
     @property
     def unhandled_prompt_behavior(self) -> str:
         """
         :returns: unhandled prompt behavior if set, the default is "dismiss and notify"
         """
+        raise NotImplementedError()
         return self._caps["unhandledPromptBehavior"]
 
     @unhandled_prompt_behavior.setter
     def unhandled_prompt_behavior(self, behavior: str) -> None:
         """How the driver should respond when an alert is present and the
         command sent is not handling the alert:
         https://w3c.github.io/webdriver/#dfn-table-of-page-load-strategies.
 
         :param behavior: behavior to use when an alert is encountered
         """
+        raise NotImplementedError()
         if behavior in ["dismiss", "accept", "dismiss and notify", "accept and notify", "ignore"]:
             self.set_capability("unhandledPromptBehavior", behavior)
         else:
             raise ValueError(
                 "Behavior can only be one of the following: dismiss, accept, dismiss and notify, "
                 "accept and notify, ignore"
             )
 
     @property
     def timeouts(self) -> dict:
         """
         :returns: Values for implicit timeout, pageLoad timeout and script timeout if set (in milliseconds)
         """
+        raise NotImplementedError()
         return self._caps["timeouts"]
 
     @timeouts.setter
     def timeouts(self, timeouts: dict) -> None:
         """How long the driver should wait for actions to complete before
         returning an error https://w3c.github.io/webdriver/#timeouts.
 
         :param timeouts: values in milliseconds for implicit wait, page load and script timeout
         """
+        raise NotImplementedError()
         if all(x in ("implicit", "pageLoad", "script") for x in timeouts.keys()):
             self.set_capability("timeouts", timeouts)
         else:
             raise ValueError("Timeout keys can only be one of the following: implicit, pageLoad, script")
 
     def enable_mobile(
             self,
@@ -161,81 +173,90 @@
             device_serial: Optional[str] = None,
     ) -> None:
         """Enables mobile browser use for browsers that support it.
 
         :Args:
             android_activity: The name of the android package to start
         """
+        raise NotImplementedError()
         if not android_package:
             raise AttributeError("android_package must be passed in")
         self.mobile_options = {"androidPackage": android_package}
         if android_activity:
             self.mobile_options["androidActivity"] = android_activity
         if device_serial:
             self.mobile_options["androidDeviceSerial"] = device_serial
 
     @property
     def accept_insecure_certs(self) -> bool:
         """
         :returns: whether the session accepts insecure certificates
         """
+        raise NotImplementedError()
         return self._caps.get("acceptInsecureCerts", False)
 
     @accept_insecure_certs.setter
     def accept_insecure_certs(self, value: bool) -> None:
         """Whether untrusted and self-signed TLS certificates are implicitly
         trusted: https://w3c.github.io/webdriver/#dfn-insecure-tls-
         certificates.
 
         :param value: whether to accept insecure certificates
         """
+        raise NotImplementedError()
         self._caps["acceptInsecureCerts"] = value
 
     @property
     def strict_file_interactability(self) -> bool:
         """
         :returns: whether session is strict about file interactability
         """
+        raise NotImplementedError()
         return self._caps.get("strictFileInteractability", False)
 
     @strict_file_interactability.setter
     def strict_file_interactability(self, value: bool) -> None:
         """Whether interactability checks will be applied to file type input
         elements. The default is false.
 
         :param value: whether file interactability is strict
         """
+        raise NotImplementedError()
         self._caps["strictFileInteractability"] = value
 
     @property
     def set_window_rect(self) -> bool:
         """
         :returns: whether the remote end supports setting window size and position
         """
+        raise NotImplementedError()
         return self._caps.get("setWindowRect", False)
 
     @set_window_rect.setter
     def set_window_rect(self, value: bool) -> None:
         """Whether the remote end supports all of the resizing and positioning
         commands. The default is false. https://w3c.github.io/webdriver/#dfn-
         strict-file-interactability.
 
         :param value: whether remote end must support setting window resizing and repositioning
         """
+        raise NotImplementedError()
         self._caps["setWindowRect"] = value
 
     @property
     def proxy(self) -> Proxy:
         """
         :Returns: Proxy if set, otherwise None.
         """
+        raise NotImplementedError()
         return self._proxy
 
     @proxy.setter
     def proxy(self, value: Proxy) -> None:
+        raise NotImplementedError()
         if not isinstance(value, Proxy):
             raise InvalidArgumentException("Only Proxy objects can be passed in.")
         self._proxy = value
         self._caps["proxy"] = value.to_capabilities()
 
     #
     # Options(BaseOptions) from here on
@@ -267,14 +288,15 @@
             self._arguments.append(argument)
         else:
             raise ValueError("argument can not be null")
 
     def ignore_local_proxy_environment_variables(self) -> None:
         """By calling this you will ignore HTTP_PROXY and HTTPS_PROXY from
         being picked up and used."""
+        raise NotImplementedError()
         self._ignore_local_proxy = True
 
     #
     #   ChromiumOptions(ArgOptions) form here on
     #
 
     @property
@@ -300,26 +322,27 @@
         """
         return self._debugger_address
 
     @debugger_address.setter
     def debugger_address(self, value: str) -> None:
         """
         Allows you to set the address of the remote devtools instance
-        that the ChromeDriver instance will try to connect to during an
+        that the Chrome instance will try to connect to during an
         active wait.
         :Args:
          - value: address of remote devtools instance if any (hostname[:port])
         """
         self._debugger_address = value
 
     @property
     def extensions(self) -> List[str]:
         """
         :Returns: A list of encoded extensions that will be loaded
         """
+        raise NotImplementedError()
 
         def _decode(file_data: BinaryIO) -> str:
             # Should not use base64.encodestring() which inserts newlines every
             # 76 characters (per RFC 1521).  Chromedriver has to remove those
             # unnecessary newlines before decoding, causing performance hit.
             return base64.b64encode(file_data.read()).decode("utf-8")
 
@@ -328,54 +351,58 @@
             with open(extension, "rb") as f:
                 encoded_extensions.append(_decode(f))
 
         return encoded_extensions + self._extensions
 
     def add_extension(self, extension: str) -> None:
         """Adds the path to the extension to a list that will be used to
-        extract it to the ChromeDriver.
+        extract it to the Chrome.
 
         :Args:
          - extension: path to the \\*.crx file
         """
+        raise NotImplementedError()
         if extension:
             extension_to_add = os.path.abspath(os.path.expanduser(extension))
             if os.path.exists(extension_to_add):
                 self._extension_files.append(extension_to_add)
             else:
                 raise OSError("Path to the extension doesn't exist")
         else:
             raise ValueError("argument can not be null")
 
     def add_encoded_extension(self, extension: str) -> None:
         """Adds Base64 encoded string with extension data to a list that will
-        be used to extract it to the ChromeDriver.
+        be used to extract it to the Chrome.
 
         :Args:
          - extension: Base64 encoded string with extension data
         """
+        raise NotImplementedError()
         if extension:
             self._extensions.append(extension)
         else:
             raise ValueError("argument can not be null")
 
     @property
     def experimental_options(self) -> dict:
         """
         :Returns: A dictionary of experimental options for chromium
         """
+        raise NotImplementedError()
         return self._experimental_options
 
     def add_experimental_option(self, name: str, value: Union[str, int, dict, List[str]]) -> None:
         """Adds an experimental option which is passed to chromium.
 
         :Args:
           name: The experimental option name.
           value: The option value.
         """
+        raise NotImplementedError()
         self._experimental_options[name] = value
 
     @property
     def headless(self) -> bool:
         """
         :Returns: True if the headless argument is set, else False
         """
@@ -409,18 +436,18 @@
 
     def to_capabilities(self) -> dict:
         """
         Creates a capabilities with all the options that have been set
         :Returns: A dictionary with everything
         """
         caps = self._caps
-        chrome_options = self.experimental_options.copy()
+        chrome_options = {}  # self.experimental_options.copy()
         if self.mobile_options:
             chrome_options.update(self.mobile_options)
-        chrome_options["extensions"] = self.extensions
+        # chrome_options["extensions"] = self.extensions
         if self.binary_location:
             chrome_options["binary"] = self.binary_location
         chrome_options["args"] = self._arguments
         if self.debugger_address:
             chrome_options["debuggerAddress"] = self.debugger_address
 
         caps[self.KEY] = chrome_options
```

### Comparing `selenium_driverless-1.0.3/src/selenium_driverless/utils/utils.py` & `selenium_driverless-1.0.4/src/selenium_driverless/utils/utils.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # from https://github.com/ultrafunkamsterdam/undetected-chromedriver/blob/1c704a71cf4f29181a59ecf19ddff32f1b4fbfc0/undetected_chromedriver/__init__.py#L844
 # edited by kaliiiiiiiiii | Aurin Aegerter
 
 import sys
-from dataclasses import dataclass
 import typing
 import json
 import os
+import selenium
 
 import selenium_driverless
 import socket
 from contextlib import closing
 
 IS_POSIX = sys.platform.startswith(("darwin", "cygwin", "linux", "linux2"))
 T_JSON_DICT = typing.Dict[str, typing.Any]
@@ -60,14 +60,18 @@
             return os.path.normpath(candidate)
 
 
 def sel_driverless_path():
     return os.path.dirname(selenium_driverless.__file__) + "/"
 
 
+def sel_path():
+    return os.path.dirname(selenium.__file__) + "/"
+
+
 def read(filename: str, encoding: str = "utf-8", sel_root: bool = True):
     if sel_root:
         path = sel_driverless_path() + filename
     else:
         path = filename
     with open(path, encoding=encoding) as f:
         return f.read()
```

### Comparing `selenium_driverless-1.0.3/src/selenium_driverless.egg-info/PKG-INFO` & `selenium_driverless-1.0.4/src/selenium_driverless.egg-info/PKG-INFO`

 * *Files 24% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: selenium-driverless
-Version: 1.0.3
+Version: 1.0.4
 Summary: Undetected selenium without chromedriver usage
 Home-page: https://github.com/kaliiiiiiiiii/Selenium-Driverless
 Author: Aurin Aegerter
 Author-email: aurinliun@gmx.ch
 Project-URL: Documentation, https://github.com/kaliiiiiiiiii/Selenium-Driverless
 Project-URL: Bug Reports, https://github.com/kaliiiiiiiiii/Selenium-Driverless/issues
 Project-URL: Source Code, https://github.com/kaliiiiiiiiii/Selenium-Driverless
@@ -48,40 +48,35 @@
 * ```pip install selenium-driverless```
 
 
 ### Usage
 
 #### example script
 ```python
-import asyncio
+from selenium_driverless import webdriver
 
-
-async def main():
-    from selenium_driverless.async_.webdriver import ChromeDriver
-    from selenium_driverless.scripts.options import Options
-    options = Options()
-    async with ChromeDriver(options=options) as driver:
-        await driver.get('http://nowsecure.nl#relax')
-        await asyncio.sleep(4)
-        title = await driver.title
-        url = await driver.current_url
-        source = await driver.page_source
-        print(title)
-
-
-asyncio.run(main())
+options = webdriver.Options()
+with webdriver.Chrome(options=options) as driver:
+    driver.get('http://nowsecure.nl#relax')
+    driver.implicitly_wait(3)
+    
+    title = driver.title
+    url = driver.current_url
+    source = driver.page_source
+    print(title)
 ```
 
 ## Help
 
 Please feel free to open an issue or fork!
 
 ## Todo
 
-
+- implementations
+  - [ ] find element
 
 ## Deprecated
 
 ## Authors
 
 [Aurin Aegerter](mailto:aurinliun@gmx.ch)
```

### Comparing `selenium_driverless-1.0.3/src/selenium_driverless.egg-info/SOURCES.txt` & `selenium_driverless-1.0.4/src/selenium_driverless.egg-info/SOURCES.txt`

 * *Files 22% similar despite different names*

```diff
@@ -8,17 +8,15 @@
 src/selenium_driverless/__init__.py
 src/selenium_driverless/webdriver.py
 src/selenium_driverless.egg-info/PKG-INFO
 src/selenium_driverless.egg-info/SOURCES.txt
 src/selenium_driverless.egg-info/dependency_links.txt
 src/selenium_driverless.egg-info/requires.txt
 src/selenium_driverless.egg-info/top_level.txt
-src/selenium_driverless/async_/__init__.py
-src/selenium_driverless/async_/mobile.py
-src/selenium_driverless/async_/webdriver.py
 src/selenium_driverless/files/__init__.py
 src/selenium_driverless/scripts/__init__.py
+src/selenium_driverless/scripts/mobile.py
 src/selenium_driverless/scripts/multi_thread.py
 src/selenium_driverless/scripts/options.py
 src/selenium_driverless/utils/__init__.py
 src/selenium_driverless/utils/utils.py
 tests/test_driverless.py
```

### Comparing `selenium_driverless-1.0.3/tests/test_driverless.py` & `selenium_driverless-1.0.4/tests/test_driverless.py`

 * *Files identical despite different names*

