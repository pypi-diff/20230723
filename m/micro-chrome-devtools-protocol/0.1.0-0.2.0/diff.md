# Comparing `tmp/micro-chrome-devtools-protocol-0.1.0.tar.gz` & `tmp/micro-chrome-devtools-protocol-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "micro-chrome-devtools-protocol-0.1.0.tar", last modified: Sat Jul 22 18:22:30 2023, max compression
+gzip compressed data, was "micro-chrome-devtools-protocol-0.2.0.tar", last modified: Sun Jul 23 18:47:56 2023, max compression
```

## Comparing `micro-chrome-devtools-protocol-0.1.0.tar` & `micro-chrome-devtools-protocol-0.2.0.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxr-x   0 aib       (1000) aib       (1000)        0 2023-07-22 18:22:30.868863 micro-chrome-devtools-protocol-0.1.0/
--rw-rw-r--   0 aib       (1000) aib       (1000)     1074 2023-07-22 18:06:46.000000 micro-chrome-devtools-protocol-0.1.0/LICENSE
--rw-rw-r--   0 aib       (1000) aib       (1000)     1031 2023-07-22 18:22:30.868863 micro-chrome-devtools-protocol-0.1.0/PKG-INFO
--rw-rw-r--   0 aib       (1000) aib       (1000)      297 2023-07-22 18:18:13.000000 micro-chrome-devtools-protocol-0.1.0/README.md
-drwxrwxr-x   0 aib       (1000) aib       (1000)        0 2023-07-22 18:22:30.868863 micro-chrome-devtools-protocol-0.1.0/micro_chrome_devtools_protocol.egg-info/
--rw-rw-r--   0 aib       (1000) aib       (1000)     1031 2023-07-22 18:22:30.000000 micro-chrome-devtools-protocol-0.1.0/micro_chrome_devtools_protocol.egg-info/PKG-INFO
--rw-rw-r--   0 aib       (1000) aib       (1000)      315 2023-07-22 18:22:30.000000 micro-chrome-devtools-protocol-0.1.0/micro_chrome_devtools_protocol.egg-info/SOURCES.txt
--rw-rw-r--   0 aib       (1000) aib       (1000)        1 2023-07-22 18:22:30.000000 micro-chrome-devtools-protocol-0.1.0/micro_chrome_devtools_protocol.egg-info/dependency_links.txt
--rw-rw-r--   0 aib       (1000) aib       (1000)        5 2023-07-22 18:22:30.000000 micro-chrome-devtools-protocol-0.1.0/micro_chrome_devtools_protocol.egg-info/top_level.txt
--rw-rw-r--   0 aib       (1000) aib       (1000)        0 2023-07-22 18:06:33.000000 micro-chrome-devtools-protocol-0.1.0/pyproject.toml
--rw-rw-r--   0 aib       (1000) aib       (1000)      788 2023-07-22 18:22:30.868863 micro-chrome-devtools-protocol-0.1.0/setup.cfg
-drwxrwxr-x   0 aib       (1000) aib       (1000)        0 2023-07-22 18:22:30.868863 micro-chrome-devtools-protocol-0.1.0/ucdp/
--rw-rw-r--   0 aib       (1000) aib       (1000)       62 2023-07-22 18:16:19.000000 micro-chrome-devtools-protocol-0.1.0/ucdp/__init__.py
--rw-rw-r--   0 aib       (1000) aib       (1000)      234 2023-07-22 17:53:51.000000 micro-chrome-devtools-protocol-0.1.0/ucdp/data.py
--rw-rw-r--   0 aib       (1000) aib       (1000)       98 2023-07-22 17:53:51.000000 micro-chrome-devtools-protocol-0.1.0/ucdp/event.py
--rw-rw-r--   0 aib       (1000) aib       (1000)     2988 2023-07-22 17:53:51.000000 micro-chrome-devtools-protocol-0.1.0/ucdp/ucdp.py
+drwxrwxr-x   0 aib       (1000) aib       (1000)        0 2023-07-23 18:47:56.979317 micro-chrome-devtools-protocol-0.2.0/
+-rw-rw-r--   0 aib       (1000) aib       (1000)     1074 2023-07-22 18:06:46.000000 micro-chrome-devtools-protocol-0.2.0/LICENSE
+-rw-rw-r--   0 aib       (1000) aib       (1000)     1050 2023-07-23 18:47:56.979317 micro-chrome-devtools-protocol-0.2.0/PKG-INFO
+-rw-rw-r--   0 aib       (1000) aib       (1000)      297 2023-07-22 18:18:13.000000 micro-chrome-devtools-protocol-0.2.0/README.md
+drwxrwxr-x   0 aib       (1000) aib       (1000)        0 2023-07-23 18:47:56.979317 micro-chrome-devtools-protocol-0.2.0/micro_chrome_devtools_protocol.egg-info/
+-rw-rw-r--   0 aib       (1000) aib       (1000)     1050 2023-07-23 18:47:56.000000 micro-chrome-devtools-protocol-0.2.0/micro_chrome_devtools_protocol.egg-info/PKG-INFO
+-rw-rw-r--   0 aib       (1000) aib       (1000)      315 2023-07-23 18:47:56.000000 micro-chrome-devtools-protocol-0.2.0/micro_chrome_devtools_protocol.egg-info/SOURCES.txt
+-rw-rw-r--   0 aib       (1000) aib       (1000)        1 2023-07-23 18:47:56.000000 micro-chrome-devtools-protocol-0.2.0/micro_chrome_devtools_protocol.egg-info/dependency_links.txt
+-rw-rw-r--   0 aib       (1000) aib       (1000)        5 2023-07-23 18:47:56.000000 micro-chrome-devtools-protocol-0.2.0/micro_chrome_devtools_protocol.egg-info/top_level.txt
+-rw-rw-r--   0 aib       (1000) aib       (1000)        0 2023-07-22 18:06:33.000000 micro-chrome-devtools-protocol-0.2.0/pyproject.toml
+-rw-rw-r--   0 aib       (1000) aib       (1000)      807 2023-07-23 18:47:56.979317 micro-chrome-devtools-protocol-0.2.0/setup.cfg
+drwxrwxr-x   0 aib       (1000) aib       (1000)        0 2023-07-23 18:47:56.979317 micro-chrome-devtools-protocol-0.2.0/ucdp/
+-rw-rw-r--   0 aib       (1000) aib       (1000)       62 2023-07-23 18:41:46.000000 micro-chrome-devtools-protocol-0.2.0/ucdp/__init__.py
+-rw-rw-r--   0 aib       (1000) aib       (1000)      234 2023-07-22 17:53:51.000000 micro-chrome-devtools-protocol-0.2.0/ucdp/data.py
+-rw-rw-r--   0 aib       (1000) aib       (1000)       98 2023-07-22 17:53:51.000000 micro-chrome-devtools-protocol-0.2.0/ucdp/event.py
+-rw-rw-r--   0 aib       (1000) aib       (1000)     3668 2023-07-23 18:21:41.000000 micro-chrome-devtools-protocol-0.2.0/ucdp/ucdp.py
```

### Comparing `micro-chrome-devtools-protocol-0.1.0/LICENSE` & `micro-chrome-devtools-protocol-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `micro-chrome-devtools-protocol-0.1.0/PKG-INFO` & `micro-chrome-devtools-protocol-0.2.0/PKG-INFO`

 * *Files 26% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: micro-chrome-devtools-protocol
-Version: 0.1.0
+Version: 0.2.0
 Summary: A lightweight library for speaking the Chrome DevTools Protocol in order to debug JavaScript
 Home-page: https://github.com/aib/ucdp
-Author: aib
+Author: Orhan "aib" Kavrakoglu
 Author-email: aibok42@gmail.com
 License: MIT
 Keywords: chrome,chromium,devtools,protocol,node,nodejs,electron,debugging,debugger
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Debuggers
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: JavaScript
```

### Comparing `micro-chrome-devtools-protocol-0.1.0/micro_chrome_devtools_protocol.egg-info/PKG-INFO` & `micro-chrome-devtools-protocol-0.2.0/micro_chrome_devtools_protocol.egg-info/PKG-INFO`

 * *Files 26% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 Metadata-Version: 2.1
 Name: micro-chrome-devtools-protocol
-Version: 0.1.0
+Version: 0.2.0
 Summary: A lightweight library for speaking the Chrome DevTools Protocol in order to debug JavaScript
 Home-page: https://github.com/aib/ucdp
-Author: aib
+Author: Orhan "aib" Kavrakoglu
 Author-email: aibok42@gmail.com
 License: MIT
 Keywords: chrome,chromium,devtools,protocol,node,nodejs,electron,debugging,debugger
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Software Development :: Debuggers
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: JavaScript
```

### Comparing `micro-chrome-devtools-protocol-0.1.0/setup.cfg` & `micro-chrome-devtools-protocol-0.2.0/setup.cfg`

 * *Files 10% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 [metadata]
 name = micro-chrome-devtools-protocol
 version = attr: ucdp.__version__
 url = https://github.com/aib/ucdp
-author = aib
+author = Orhan "aib" Kavrakoglu
 author_email = aibok42@gmail.com
 classifiers = 
 	Intended Audience :: Developers
 	Topic :: Software Development :: Debuggers
 	Programming Language :: Python :: 3
 	Programming Language :: JavaScript
 	License :: OSI Approved :: MIT License
```

### Comparing `micro-chrome-devtools-protocol-0.1.0/ucdp/ucdp.py` & `micro-chrome-devtools-protocol-0.2.0/ucdp/ucdp.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,102 +1,126 @@
 import collections
 import json
 import logging
 import queue
+import threading
 
 from .data import UcdpData
 from .event import UcdpEvent
 
 from typing import Callable, Iterable
 EventCallback = Callable[[UcdpEvent], None]
 
 class NoSenderSetException(Exception):
 	def __init__(self):
 		super().__init__("No sender set, use set_sender")
 
 class Ucdp:
-	def __init__(self):
-		self.logger = logging.getLogger('Ucdp')
-		self.method_logger = logging.getLogger('Ucdp.method')
-		self.event_logger = logging.getLogger('Ucdp.event')
-		self.sender = None
+	LOGGER_NAME = 'Ucdp'
+	METHOD_LOGGER_NAME = 'Ucdp.method'
+	EVENT_LOGGER_NAME = 'Ucdp.event'
+
+	def __init__(self, use_event_thread=True):
+		self.use_event_thread = use_event_thread
+
 		self.data = UcdpData()
-		self.event_subscribers = collections.defaultdict(list)
-		self.all_events_subscribers = []
-		self.pending_results = {}
-		self.next_msg_id = 1
+
+		self._logger = logging.getLogger(self.LOGGER_NAME)
+		self._method_logger = logging.getLogger(self.METHOD_LOGGER_NAME)
+		self._event_logger = logging.getLogger(self.EVENT_LOGGER_NAME)
+
+		self._sender = None
+		self._all_events_subscribers = []
+		self._event_subscribers = collections.defaultdict(list)
+		self._pending_results = {}
+		self._next_msg_id = 1
+
+		if self.use_event_thread:
+			self._event_queue = queue.SimpleQueue()
+			threading.Thread(name='Ucdp::_event_handler_caller', target=self._event_handler_caller, daemon=True).start()
 
 	def set_sender(self, sender: Callable[[str], None]):
-		self.sender = sender
+		self._sender = sender
 
 	def process_message(self, message: str):
 		msg = json.loads(message)
 		if 'method' in msg:
 			event = UcdpEvent(name=msg['method'], params=msg['params'])
 			self._process_event(event)
 		elif 'result' in msg:
 			self._process_result(msg['id'], msg['result'])
 		else:
-			self.logger.warning("Unknown message format, ignoring: %s", msg)
+			self._logger.warning("Unknown message format, ignoring: %s", msg)
 
 	def subscribe_events_decorator(self, events: None | str | Iterable[str] = None) -> Callable[[EventCallback], EventCallback]:
 		def wrapper(f):
 			self.subscribe_events(f, events)
 			return f
 		return wrapper
 
 	def subscribe_events(self, cb: EventCallback, events: None | str | Iterable[str] = None):
 		if events is None:
-			self.all_events_subscribers.append(cb)
+			self._all_events_subscribers.append(cb)
 		elif isinstance(events, str):
-			self.event_subscribers[events].append(cb)
+			self._event_subscribers[events].append(cb)
 		elif hasattr(events, '__iter__'):
 			for event in events:
-				self.event_subscribers[event].append(cb)
+				self._event_subscribers[event].append(cb)
 		else:
-			self.event_subscribers[events].append(cb)
+			self._event_subscribers[events].append(cb)
+
+	def call_nowait(self, method: str, **params):
+		msg = self._get_msg(method, params)
+		self._send_msg(msg)
 
 	def call(self, method: str, **params):
 		msg = self._get_msg(method, params)
 		q = queue.SimpleQueue()
-		self.pending_results[msg['id']] = q
+		self._pending_results[msg['id']] = q
 		self._send_msg(msg)
 		result = q.get()
-		del self.pending_results[msg['id']]
+		del self._pending_results[msg['id']]
 		return result
 
 	def _get_msg(self, method: str, params: dict):
 		msg = {
-			'id': self.next_msg_id,
+			'id': self._next_msg_id,
 			'method': method,
 			'params': params,
 		}
-		self.next_msg_id += 1
+		self._next_msg_id += 1
 		return msg
 
 	def _send_msg(self, msg: dict):
-		if self.sender is None:
+		if self._sender is None:
 			raise NoSenderSetException()
 
-		self.method_logger.debug("<- Method %s: %s %s", msg['id'], msg['method'], msg['params'])
-		self.sender(json.dumps(msg))
+		self._method_logger.debug("<- Method %s: %s %s", msg['id'], msg['method'], msg['params'])
+		self._sender(json.dumps(msg))
 
 	def _process_result(self, result_id: int, result: dict):
-		self.method_logger.debug("-> Result %s: %s", result_id, result)
+		self._method_logger.debug("-> Result %s: %s", result_id, result)
 
-		pending = self.pending_results.get(result_id, None)
+		pending = self._pending_results.get(result_id, None)
 		if pending is None:
-			self.logger.warning("Received result %s with no waiters: %s", result_id, result)
+			self._logger.warning("Received result %s with no waiters: %s", result_id, result)
 		else:
 			pending.put(result)
 
 	def _process_event(self, event: UcdpEvent):
-		self.event_logger.debug("-> Event %s: %s", event.name, event.params)
+		self._event_logger.debug("-> Event %s: %s", event.name, event.params)
 		self.data._process_event(event)
-		self._emit_event(event)
+		if self.use_event_thread:
+			self._event_queue.put(event)
+		else:
+			self._emit_event(event)
+
+	def _event_handler_caller(self):
+		while True:
+			self._emit_event(self._event_queue.get())
 
-	def _emit_event(self, event: UcdpEvent):
-		for sub in self.all_events_subscribers:
+	def _emit_event(self, event):
+		for sub in self._all_events_subscribers:
 			sub(event)
 
-		for sub in self.event_subscribers.get(event.name, []):
+		for sub in self._event_subscribers.get(event.name, []):
 			sub(event)
```

