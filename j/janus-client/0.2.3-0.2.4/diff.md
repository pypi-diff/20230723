# Comparing `tmp/janus-client-0.2.3.tar.gz` & `tmp/janus_client-0.2.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/home/joseph/janus_gst_client_py/dist/tmp720gtoci/janus-client-0.2.3.tar", last modified: Sun Mar 14 10:04:05 2021, max compression
+gzip compressed data, was "janus_client-0.2.4.tar", max compression
```

## Comparing `janus-client-0.2.3.tar` & `janus_client-0.2.4.tar`

### file list

```diff
@@ -1,16 +1,11 @@
-drwxr-xr-x   0 joseph    (1000) joseph    (1000)        0 2021-03-14 10:04:05.000000 janus-client-0.2.3/
--rw-r--r--   0 joseph    (1000) joseph    (1000)     6502 2021-03-14 10:04:05.000000 janus-client-0.2.3/PKG-INFO
--rw-r--r--   0 joseph    (1000) joseph    (1000)     4958 2021-03-14 09:59:36.000000 janus-client-0.2.3/README.md
-drwxr-xr-x   0 joseph    (1000) joseph    (1000)        0 2021-03-14 10:04:05.000000 janus-client-0.2.3/janus_client/
--rw-r--r--   0 joseph    (1000) joseph    (1000)      126 2021-03-14 09:58:22.000000 janus-client-0.2.3/janus_client/__init__.py
--rw-r--r--   0 joseph    (1000) joseph    (1000)    11381 2021-03-14 09:23:47.000000 janus-client-0.2.3/janus_client/core.py
--rw-r--r--   0 joseph    (1000) joseph    (1000)     2274 2021-03-14 09:18:33.000000 janus-client-0.2.3/janus_client/plugin_base.py
--rw-r--r--   0 joseph    (1000) joseph    (1000)    14218 2021-03-14 08:28:51.000000 janus-client-0.2.3/janus_client/plugin_video_room.py
--rw-r--r--   0 joseph    (1000) joseph    (1000)     2825 2021-03-14 09:18:42.000000 janus-client-0.2.3/janus_client/session.py
-drwxr-xr-x   0 joseph    (1000) joseph    (1000)        0 2021-03-14 10:04:05.000000 janus-client-0.2.3/janus_client.egg-info/
--rw-r--r--   0 joseph    (1000) joseph    (1000)     6502 2021-03-14 10:04:05.000000 janus-client-0.2.3/janus_client.egg-info/PKG-INFO
--rw-r--r--   0 joseph    (1000) joseph    (1000)      330 2021-03-14 10:04:05.000000 janus-client-0.2.3/janus_client.egg-info/SOURCES.txt
--rw-r--r--   0 joseph    (1000) joseph    (1000)        1 2021-03-14 10:04:05.000000 janus-client-0.2.3/janus_client.egg-info/dependency_links.txt
--rw-r--r--   0 joseph    (1000) joseph    (1000)       11 2021-03-14 10:04:05.000000 janus-client-0.2.3/janus_client.egg-info/requires.txt
--rw-r--r--   0 joseph    (1000) joseph    (1000)       13 2021-03-14 10:04:05.000000 janus-client-0.2.3/janus_client.egg-info/top_level.txt
--rw-r--r--   0 joseph    (1000) joseph    (1000)      684 2021-03-14 10:04:05.000000 janus-client-0.2.3/setup.cfg
+-rw-r--r--   0        0        0      211 2023-07-22 06:24:20.872509 janus_client-0.2.4/janus_client/__init__.py
+-rw-r--r--   0        0        0    11251 2023-07-22 07:10:09.526094 janus_client-0.2.4/janus_client/core.py
+-rw-r--r--   0        0        0     7186 2023-07-23 14:00:09.146471 janus_client-0.2.4/janus_client/media.py
+-rw-r--r--   0        0        0     2223 2023-07-22 07:07:52.191119 janus_client-0.2.4/janus_client/plugin_base.py
+-rw-r--r--   0        0        0    14360 2023-07-22 06:24:20.872509 janus_client-0.2.4/janus_client/plugin_video_room.py
+-rw-r--r--   0        0        0     9181 2023-07-23 13:49:35.776875 janus_client-0.2.4/janus_client/plugin_video_room_ffmpeg.py
+-rw-r--r--   0        0        0     3028 2023-07-22 07:08:40.841540 janus_client-0.2.4/janus_client/session.py
+-rw-r--r--   0        0        0     1069 2023-07-22 06:24:20.872509 janus_client-0.2.4/LICENSE
+-rw-r--r--   0        0        0      556 2023-07-23 14:58:25.212228 janus_client-0.2.4/pyproject.toml
+-rw-r--r--   0        0        0     6715 2023-07-23 14:33:40.913988 janus_client-0.2.4/README.md
+-rw-r--r--   0        0        0     7506 1970-01-01 00:00:00.000000 janus_client-0.2.4/PKG-INFO
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `janus-client-0.2.3/README.md` & `janus_client-0.2.4/README.md`

 * *Files 20% similar despite different names*

```diff
@@ -16,39 +16,63 @@
 
 ## Description
 
 The package is implementing a general purpose client that can communicate with a Janus server.
 
 Examples like VideoRoom plugin are also included in the package, but currently it depends on GStreamer for WebRTC and media streaming, and it will not be automatically installed. The reason for this is because it's not trivial to install/recompile it. Please refer to [Quirks section](#quirks).
 
+The VideoRoom plugin implemented in [plugin_video_room_ffmpeg.py](./janus_client/plugin_video_room_ffmpeg.py) uses FFmpeg instead. It depends on the ffmpeg-cli, but that is required to be installed separately.
+
+### FFmpeg Stream To WebRTC (**WARNING !!!**)
+
+This FFmpeg stream to WebRTC solution is a hacked solution. The fact is that FFmpeg doesn't support WebRTC and aiortc is implemented using PyAV. PyAV has much less features than a full fledged installed FFmpeg, so to support more features and keep things simple, I hacked about a solution without the use of WHIP server or UDP of RTMP.
+
+First the ffmpeg input part should be constructed by the user, before passing it to `janus_client.media.MediaPlayer`. When the media player needs to stream the video, the following happens:
+
+- a thread will be created
+- a ffmpeg process will be created. Output of ffmpeg is hardcode to be `rawvideo rgb24`
+- thread reads output of ffmpeg process
+- coverts the output data to numpy array
+- use PyAV to convert the numpy array to `av.VideoFrame` frame
+- hack the `pts` and `time_base` parameter of the frame. I don't know what it is and just found a value that works.
+- put the frame into video track queue as that is what is required by `aiortc.mediastreams.MediaStreamTrack`.
+
+Next the `MediaPlayer` is used as required by `aiortc`. An example of that can be found [here](https://github.com/aiortc/aiortc/tree/main/examples/janus).
+
+A fork of FFmpeg that supports WebRTC can be found [here](https://github.com/ossrs/ffmpeg-webrtc/pull/1).
+
 ### Features
 
 :heavy_check_mark: Connect to Janus server through websocket (using [websockets](https://github.com/aaugustin/websockets))  
 :heavy_check_mark: Handle transactions with Janus  
 :heavy_check_mark: Create/destroy sessions  
 :heavy_check_mark: Create/destroy plugins  
 :heavy_check_mark: Handle multiple sessions and or multiple plugins at the same time  
 :heavy_check_mark: Support authentication with shared static secret (API key) and/or stored token  
 :heavy_check_mark: Expose Admin/Monitor API client  
 
 ### In Progress
 
 :clock3: Emit events to respective session and plugin handlers  
-:clock3: Create plugin for videoroom plugin  
+:clock3: Create plugin for videoroom plugin using GStreamer  
 :clock3: Documentation  
 
 ### Dependencies
 
 - [websockets](https://github.com/aaugustin/websockets)
+- [aiortc](https://github.com/aiortc/aiortc)
+- [ffmpeg-python](https://github.com/kkroening/ffmpeg-python)
+- [numpy](https://numpy.org/)
+- [av](https://github.com/PyAV-Org/PyAV)
 
 ---
 
 ## Usage
 
-In [main.py](./main.py), you will see an example on how to use the client in general, such as connecting and creating sessions.  
+In [test_gst_videoroom.py](./test_gst_videoroom.py), you will see an example on how to use the client in general, such as connecting and creating sessions.  
 I use it to develop this package.
 
 For more details, please [Read The Docs](https://janus-client-in-python.readthedocs.io/en/latest/)
 
 Example:
 
 ```python
```

### Comparing `janus-client-0.2.3/janus_client/core.py` & `janus_client-0.2.4/janus_client/core.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,39 +1,42 @@
-
 import asyncio
 import websockets
 import json
 import uuid
 import traceback
 from .session import JanusSession
 from typing import Type, Dict, Any
 
-'''
+import logging
+
+logger = logging.getLogger(__name__)
+
+
+"""
 Architecture design to handle Janus transactions and events
 Assumption 1: All transaction ids are unique, and they will always get
     at least one reply when there are no network errors
 So to handle transactions, it will be tracked in JanusClient only.
 To handle events, it will be passed top down to all matching session id
     and plugin handle id.
 Each node down the tree with JanusClient as root, including JanusClient itself,
 shall have:
 1. handle_async_response method
 
 E.g.
 class JanusSession
     def handle_async_response(self, response):
         pass
-'''
+"""
 
 
 class JanusClient:
     """Janus client instance, connected through websocket"""
 
-    def __init__(self, uri: str, api_secret: str = None,
-                 token: str = None):
+    def __init__(self, uri: str, api_secret: str = None, token: str = None):
         """Initialize client instance
 
         :param uri: Janus server address
         :param api_secret: (optional) API key for shared static secret authentication
         :param token: (optional) Token for shared token based authentication
         """
 
@@ -46,53 +49,53 @@
 
     async def connect(self, **kwargs: Any) -> None:
         """Connect to server
 
         All extra keyword arguments will be passed to websockets.connect
         """
 
-        print("Connecting to: ", self.uri)
+        logger.info(f"Connecting to: {self.uri}")
         # self.ws = await websockets.connect(self.uri, ssl=ssl_context)
-        self.ws = await websockets.connect(self.uri,
-                                           subprotocols=[
-                                               websockets.Subprotocol("janus-protocol")],
-                                           **kwargs)
+        self.ws = await websockets.connect(
+            self.uri, subprotocols=[websockets.Subprotocol("janus-protocol")], **kwargs
+        )
         self.receive_message_task = asyncio.create_task(self.receive_message())
-        self.receive_message_task.add_done_callback(
-            self.receive_message_done_cb)
-        print("Connected")
+        self.receive_message_task.add_done_callback(self.receive_message_done_cb)
+        logger.info("Connected")
 
     async def disconnect(self) -> None:
         """Disconnect from server"""
 
-        print("Disconnecting")
+        logger.info("Disconnecting")
         self.receive_message_task.cancel()
         await self.ws.close()
 
     def is_async_response(self, response: dict):
         janus_type = response["janus"]
-        return ((janus_type == "event")
-                or (janus_type == "detached")
-                or (janus_type == "webrtcup")
-                or (janus_type == "media")
-                or (janus_type == "slowlink")
-                or (janus_type == "hangup"))
+        return (
+            (janus_type == "event")
+            or (janus_type == "detached")
+            or (janus_type == "webrtcup")
+            or (janus_type == "media")
+            or (janus_type == "slowlink")
+            or (janus_type == "hangup")
+        )
 
     def receive_message_done_cb(self, task, context=None):
         try:
             # Check if any exceptions are raised
             exception = task.exception()
             traceback.print_tb(exception.__traceback__)
-            print(f"{type(exception)} : {exception}")
-        except asyncio.CancelledError as e:
-            print("Receive message task ended")
-        except asyncio.InvalidStateError as e:
-            print("receive_message_done_cb called with invalid state")
+            logger.info(f"{type(exception)} : {exception}")
+        except asyncio.CancelledError:
+            logger.info("Receive message task ended")
+        except asyncio.InvalidStateError:
+            logger.info("receive_message_done_cb called with invalid state")
         except Exception as e:
-            traceback.print_tb(e.__traceback__)
+            traceback.logger.info_tb(e.__traceback__)
 
     async def receive_message(self):
         assert self.ws
         async for message_raw in self.ws:
             response = json.loads(message_raw)
             if self.is_async_response(response):
                 self.handle_async_response(response)
@@ -117,51 +120,55 @@
         # Authentication
         if self.api_secret is not None:
             message["apisecret"] = self.api_secret
         if self.token is not None:
             message["token"] = self.token
 
         # Send the message
-        print(json.dumps(message))
+        logger.info(json.dumps(message))
         await self.ws.send(json.dumps(message))
 
         # Wait for response
         # Assumption: there will be one and only one synchronous reply for a transaction.
         #   Other replies with the same transaction ID are asynchronous.
         response = await self.transactions[transaction_id].get()
-        print("Transaction reply: ", response)
+        logger.info(f"Transaction reply: {response}")
 
         # Transaction complete, delete it
         del self.transactions[transaction_id]
         return response
 
     def handle_async_response(self, response: dict):
         if "session_id" in response:
             # This is response for session or plugin handle
             if response["session_id"] in self.sessions:
-                self.sessions[response["session_id"]
-                              ].handle_async_response(response)
+                self.sessions[response["session_id"]].handle_async_response(response)
             else:
-                print("Got response for session but session not found. Session ID:",
-                      response["session_id"])
-                print("Unhandeled response:", response)
+                logger.info(
+                    f"Got response for session but session not found. Session ID: {response['session_id']}"
+                )
+                logger.info(f"Unhandeled response: {response}")
         else:
             # This is response for self
-            print("Async event for Janus client core:", response)
+            logger.info(f"Async event for Janus client core: {response}")
 
-    async def create_session(self, session_type: Type[JanusSession] = JanusSession) -> JanusSession:
+    async def create_session(
+        self, session_type: Type[JanusSession] = JanusSession
+    ) -> JanusSession:
         """Create Janus session instance
 
         :param session_type: Class type of session. Should be JanusSession,
             no other options yet.
         """
 
-        response = await self.send({
-            "janus": "create",
-        })
+        response = await self.send(
+            {
+                "janus": "create",
+            }
+        )
         session = session_type(client=self, session_id=response["data"]["id"])
         self.sessions[session.id] = session
         return session
 
     # Don't call this from client object, call destroy from session instead
     def destroy_session(self, session):
         del self.sessions[session.id]
@@ -187,37 +194,38 @@
     def __init__(self, uri: str, admin_secret: str):
         self.ws: websockets.WebSocketClientProtocol
         self.uri = uri
         self.admin_secret = admin_secret
         self.transactions: Dict[str, asyncio.Queue] = dict()
 
     async def connect(self, **kwargs: Any) -> None:
-        print("Connecting to: ", self.uri)
+        logger.info(f"Connecting to: {self.uri}")
         # self.ws = await websockets.connect(self.uri, ssl=ssl_context)
-        self.ws = await websockets.connect(self.uri,
-                                           subprotocols=[
-                                               websockets.Subprotocol("janus-admin-protocol")],
-                                           **kwargs)
+        self.ws = await websockets.connect(
+            self.uri,
+            subprotocols=[websockets.Subprotocol("janus-admin-protocol")],
+            **kwargs,
+        )
         self.receive_message_task = asyncio.create_task(self.receive_message())
-        print("Connected")
+        logger.info("Connected")
 
     async def disconnect(self):
-        print("Disconnecting")
+        logger.info("Disconnecting")
         self.receive_message_task.cancel()
         await self.ws.close()
 
     async def receive_message(self):
         assert self.ws
         async for message_raw in self.ws:
             response = json.loads(message_raw)
-            # WARNING: receive_message task will break with printing exception
+            # WARNING: receive_message task will break with logger.infoing exception
             #   when entering here without a transaction in response.
             #   It happens when the asynchronous event is not recognized in
             #   self.is_async_response()
-            # TODO: Find out how to print exceptions in created tasks
+            # TODO: Find out how to logger.info exceptions in created tasks
             if response["transaction"] in self.transactions:
                 await self.transactions[response["transaction"]].put(response)
 
     async def send(self, message: dict, authenticate: bool = True) -> dict:
         # Create transaction
         transaction_id = uuid.uuid4().hex
         message["transaction"] = transaction_id
@@ -225,46 +233,39 @@
         self.transactions[transaction_id] = asyncio.Queue()
 
         # Authentication
         if authenticate:
             message["admin_secret"] = self.admin_secret
 
         # Send the message
-        print(json.dumps(message))
+        logger.info(json.dumps(message))
         await self.ws.send(json.dumps(message))
 
         # Wait for response
         # Assumption: there will be one and only one synchronous reply for a transaction.
         #   Other replies with the same transaction ID are asynchronous.
         response = await self.transactions[transaction_id].get()
-        print("Transaction reply: ", response)
+        logger.info(f"Transaction reply: {response}")
 
         # Transaction complete, delete it
         del self.transactions[transaction_id]
         return response
 
     async def info(self):
         # Doesn't require admin secret
-        message = {
-            "janus": "info"
-        }
+        message = {"janus": "info"}
         return await self.send(message, authenticate=False)
 
     async def ping(self):
         # Doesn't require admin secret
-        message = {
-            "janus": "ping"
-        }
+        message = {"janus": "ping"}
         return await self.send(message, authenticate=False)
 
     async def add_token(self, token: str = uuid.uuid4().hex, plugins: list = []):
-        payload: dict = {
-            "janus": "add_token",
-            "token": token
-        }
+        payload: dict = {"janus": "add_token", "token": token}
         if plugins:
             payload["plugins"] = plugins
         return await self.send(payload)
 
     async def allow_token(self, token: str, plugins: list):
         # if not plugins:
         #     raise Exception("plugins should be non-empty array")
@@ -282,17 +283,15 @@
             "janus": "disallow_token",
             "token": token,
             "plugins": plugins,
         }
         return await self.send(payload)
 
     async def list_tokens(self):
-        payload = {
-            "janus": "list_tokens"
-        }
+        payload = {"janus": "list_tokens"}
         result = await self.send(payload)
         return result["data"]["tokens"]
 
     async def remove_token(self, token: str):
         payload = {
             "janus": "remove_token",
             "token": token,
```

### Comparing `janus-client-0.2.3/janus_client/plugin_base.py` & `janus_client-0.2.4/janus_client/plugin_base.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
-
 from __future__ import annotations
-import asyncio
 from typing import TYPE_CHECKING
+
 if TYPE_CHECKING:
     from .session import JanusSession
 
-class JanusPlugin():
+
+class JanusPlugin:
     """Base class to inherit when implementing a plugin"""
 
     name = "janus.plugin.base.dummy"
     """Plugin name
 
     Must override to match plugin name in Janus server.
     """
@@ -57,20 +57,17 @@
         :param sdpMLineIndex: (I don't know what is this)
         :param candidate: Candidate payload. (I got it from WebRTC instance callback)
         """
 
         candidate_payload = dict()
         if candidate:
             candidate_payload = {
-                "sdpMLineIndex" : sdpMLineIndex,
-                "candidate" : candidate,
+                "sdpMLineIndex": sdpMLineIndex,
+                "candidate": candidate,
             }
         else:
             # Reference: https://janus.conf.meetecho.com/docs/rest.html
             # - a null candidate or a completed JSON object to notify the end of the candidates.
             # TODO: test it
             candidate_payload = None
-        await self.send({
-            "janus": "trickle",
-            "candidate": candidate_payload
-        })
-        # TODO: Implement sending an array of candidates
+        await self.send({"janus": "trickle", "candidate": candidate_payload})
+        # TODO: Implement sending an array of candidates
```

### Comparing `janus-client-0.2.3/janus_client/plugin_video_room.py` & `janus_client-0.2.4/janus_client/plugin_video_room.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,12 @@
 
 from .plugin_base import JanusPlugin
 import asyncio
+import logging
+logger = logging.getLogger(__name__)
 
 import gi
 gi.require_version('GLib', '2.0')
 gi.require_version('GObject', '2.0')
 gi.require_version('Gst', '1.0')
 from gi.repository import Gst
 gi.require_version('GstWebRTC', '1.0')
@@ -49,25 +51,25 @@
         self.loop = asyncio.get_running_loop()
 
         # Create a new pipeline, elements will be added to this.
         self.pipeline = Gst.Pipeline.new()
 
     def handle_async_response(self, response: dict):
         if response["janus"] == "event":
-            print("Event response:", response)
+            logger.info(f"Event response: {response}")
             if "plugindata" in response:
                 if response["plugindata"]["data"]["videoroom"] == "attached":
                     # Subscriber attached
                     self.joined_event.set()
                 elif response["plugindata"]["data"]["videoroom"] == "joined":
                     # Participant joined (joined as publisher but may not publish)
                     self.joined_event.set()
         else:
-            print("Unimplemented response handle:", response["janus"])
-            print(response)
+            logger.info(f"Unimplemented response handle: {response['janus']}")
+            logger.info(response)
         # Handle JSEP. Could be answer or offer.
         if "jsep" in response:
             asyncio.create_task(self.handle_jsep(response["jsep"]))
 
     async def join(self, room_id: int, publisher_id: int, display_name: str) -> None:
         """Join a room
 
@@ -109,15 +111,15 @@
         offer = reply.get_value('offer')
         # Set local description
         promise = Gst.Promise.new()
         self.webrtcbin.emit('set-local-description', offer, promise)
         promise.interrupt()
 
         text = offer.sdp.as_text()
-        print('Sending offer and publishing:\n%s' % text)
+        logger.info('Sending offer and publishing:\n%s' % text)
         await self.send({
             "janus": "message",
             "body": {
                 "request": "publish",
                 "audio": True,
                 "video": True,
             },
@@ -128,17 +130,17 @@
             }
         })
         await self.joined_event.wait()
 
     async def unpublish(self) -> None:
         """Stop publishing"""
 
-        print("Set pipeline to null")
+        logger.info("Set pipeline to null")
         self.pipeline.set_state(Gst.State.NULL)
-        print("Set pipeline complete")
+        logger.info("Set pipeline complete")
         await self.send({
             "janus": "message",
             "body": {
                 "request": "unpublish",
             }
         })
         self.gst_webrtc_ready.clear()
@@ -236,30 +238,30 @@
                 "request": "listparticipants",
                 "room": room_id,
             }
         })
         return response["plugindata"]["data"]["participants"]
 
     def on_negotiation_needed(self, element):
-        print("on_negotiation_needed called")
+        logger.info("on_negotiation_needed called")
         self.gst_webrtc_ready.set()
         # promise = Gst.Promise.new_with_change_func(self.on_offer_created, element, None)
         # element.emit('create-offer', None, promise)
 
     def send_ice_candidate_message(self, _, sdpMLineIndex, candidate):
         icemsg = {'candidate': candidate, 'sdpMLineIndex': sdpMLineIndex}
-        print ("Sending ICE", icemsg)
+        logger.info (f"Sending ICE {icemsg}")
         # loop = asyncio.new_event_loop()
         future = asyncio.run_coroutine_threadsafe(
             self.trickle(sdpMLineIndex, candidate), self.loop)
         future.result()
 
     def on_incoming_decodebin_stream(self, _, pad):
         if not pad.has_current_caps():
-            print(pad, 'has no caps, ignoring')
+            logger.info(pad, 'has no caps, ignoring')
             return
 
         caps = pad.get_current_caps()
         name = caps.to_string()
         if name.startswith('video'):
             q = Gst.ElementFactory.make('queue')
             conv = Gst.ElementFactory.make('videoconvert')
@@ -312,43 +314,43 @@
 
     def extract_ice_from_sdp(self, sdp):
         mlineindex = -1
         for line in sdp.splitlines():
             if line.startswith("a=candidate"):
                 candidate = line[2:]
                 if mlineindex < 0:
-                    print("Received ice candidate in SDP before any m= line")
+                    logger.info("Received ice candidate in SDP before any m= line")
                     continue
-                print(
+                logger.info(
                     'Received remote ice-candidate mlineindex {}: {}'.format(mlineindex, candidate))
                 self.webrtcbin.emit('add-ice-candidate', mlineindex, candidate)
             elif line.startswith("m="):
                 mlineindex += 1
 
     async def handle_jsep(self, jsep):
-        print(jsep)
+        logger.info(jsep)
         if 'sdp' in jsep:
             sdp = jsep['sdp']
             if jsep['type'] == 'answer':
-                print('Received answer:\n%s' % sdp)
+                logger.info('Received answer:\n%s' % sdp)
                 _, sdpmsg = GstSdp.SDPMessage.new()
                 GstSdp.sdp_message_parse_buffer(bytes(sdp.encode()), sdpmsg)
 
                 answer = GstWebRTC.WebRTCSessionDescription.new(
                     GstWebRTC.WebRTCSDPType.ANSWER, sdpmsg)
                 promise = Gst.Promise.new()
                 self.webrtcbin.emit('set-remote-description', answer, promise)
                 promise.interrupt()
 
                 # Extract ICE candidates from the SDP to work around a GStreamer
                 # limitation in (at least) 1.16.2 and below
                 # This is tested to be not needed on 1.19.0.1
                 # self.extract_ice_from_sdp(sdp)
             elif jsep['type'] == 'offer':
-                print('Received offer:\n%s' % sdp)
+                logger.info('Received offer:\n%s' % sdp)
                 _, sdpmsg = GstSdp.SDPMessage.new()
                 GstSdp.sdp_message_parse_buffer(bytes(sdp.encode()), sdpmsg)
 
                 offer = GstWebRTC.WebRTCSessionDescription.new(
                     GstWebRTC.WebRTCSDPType.OFFER, sdpmsg)
                 promise = Gst.Promise.new()
                 self.webrtcbin.emit('set-remote-description', offer, promise)
```

### Comparing `janus-client-0.2.3/janus_client/session.py` & `janus_client-0.2.4/janus_client/session.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,16 +1,20 @@
-
 from __future__ import annotations
 import asyncio
 from typing import TYPE_CHECKING, Type, TypeVar, Dict
 from .plugin_base import JanusPlugin
+
 if TYPE_CHECKING:
     from .core import JanusClient
 
-PluginBaseType = TypeVar('PluginBaseType', bound=JanusPlugin)
+import logging
+
+logger = logging.getLogger(__name__)
+PluginBaseType = TypeVar("PluginBaseType", bound=JanusPlugin)
+
 
 class JanusSession:
     """Janus session instance, created by JanusClient"""
 
     def __init__(self, client: JanusClient, session_id: int):
         self.client = client
         self.id = session_id
@@ -38,41 +42,49 @@
         return await self.client.send(message)
 
     async def keepalive(self):
         # Reference: https://janus.conf.meetecho.com/docs/rest.html
         # A Janus session is kept alive as long as there's no inactivity for 60 seconds
         while True:
             await asyncio.sleep(30)
-            await self.send({
-                "janus": "keepalive",
-            })
+            await self.send(
+                {
+                    "janus": "keepalive",
+                }
+            )
 
     def handle_async_response(self, response: dict):
         if "sender" in response:
             # This is response for plugin handle
             if response["sender"] in self.plugin_handles:
                 self.plugin_handles[response["sender"]].handle_async_response(response)
             else:
-                print("Got response for plugin handle but handle not found. Handle ID:", response["sender"])
-                print("Unhandeled response:", response)
+                logger.info(
+                    f"Got response for plugin handle but handle not found. Handle ID: {response['sender']}"
+                )
+                logger.info(f"Unhandeled response: {response}")
         else:
             # This is response for self
-            print("Async event for session:", response)
+            logger.info(f"Async event for session: {response}")
 
-    async def create_plugin_handle(self, plugin_type: Type[PluginBaseType]) -> PluginBaseType:
+    async def create_plugin_handle(
+        self, plugin_type: Type[PluginBaseType]
+    ) -> PluginBaseType:
         """Create plugin handle for the given plugin type
 
         PluginBaseType = TypeVar('PluginBaseType', bound=JanusPlugin)
 
         :param plugin_type: Plugin type with janus_client.JanusPlugin as base class
         """
 
-        response = await self.send({
-            "janus": "attach",
-            "plugin": plugin_type.name,
-        })
+        response = await self.send(
+            {
+                "janus": "attach",
+                "plugin": plugin_type.name,
+            }
+        )
         plugin_handle = plugin_type(self, response["data"]["id"])
         self.plugin_handles[plugin_handle.id] = plugin_handle
         return plugin_handle
 
     def destroy_plugin_handle(self, plugin_handle):
-        del self.plugin_handles[plugin_handle.id]
+        del self.plugin_handles[plugin_handle.id]
```

