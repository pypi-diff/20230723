# Comparing `tmp/aio-request-0.1.9a3.tar.gz` & `tmp/aio-request-0.1.9a4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "aio-request-0.1.9a3.tar", last modified: Mon Jun 28 12:00:08 2021, max compression
+gzip compressed data, was "aio-request-0.1.9a4.tar", last modified: Tue Jul 13 13:02:09 2021, max compression
```

## Comparing `aio-request-0.1.9a3.tar` & `aio-request-0.1.9a4.tar`

### file list

```diff
@@ -1,31 +1,32 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-28 12:00:08.393817 aio-request-0.1.9a3/
--rw-r--r--   0 runner    (1001) docker     (121)     1068 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)     3817 2021-06-28 12:00:08.393817 aio-request-0.1.9a3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     2720 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-28 12:00:08.393817 aio-request-0.1.9a3/aio_request/
--rw-r--r--   0 runner    (1001) docker     (121)     2734 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)    11917 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/aiohttp.py
--rw-r--r--   0 runner    (1001) docker     (121)     5973 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/base.py
--rw-r--r--   0 runner    (1001) docker     (121)     5354 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/client.py
--rw-r--r--   0 runner    (1001) docker     (121)     1278 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/context.py
--rw-r--r--   0 runner    (1001) docker     (121)     1131 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/deadline.py
--rw-r--r--   0 runner    (1001) docker     (121)      597 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/delays_provider.py
--rw-r--r--   0 runner    (1001) docker     (121)      662 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/metrics.py
--rw-r--r--   0 runner    (1001) docker     (121)     3288 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/opentelemetry.py
--rw-r--r--   0 runner    (1001) docker     (121)     5066 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/pipeline.py
--rw-r--r--   0 runner    (1001) docker     (121)      428 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/priority.py
--rw-r--r--   0 runner    (1001) docker     (121)     1559 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/prometheus.py
--rw-r--r--   0 runner    (1001) docker     (121)     4324 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/request.py
--rw-r--r--   0 runner    (1001) docker     (121)     8972 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/request_strategy.py
--rw-r--r--   0 runner    (1001) docker     (121)      842 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/response_classifier.py
--rw-r--r--   0 runner    (1001) docker     (121)     1865 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/tracing.py
--rw-r--r--   0 runner    (1001) docker     (121)      253 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/transport.py
--rw-r--r--   0 runner    (1001) docker     (121)     1987 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/aio_request/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-06-28 12:00:08.393817 aio-request-0.1.9a3/aio_request.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     3817 2021-06-28 12:00:08.000000 aio-request-0.1.9a3/aio_request.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      698 2021-06-28 12:00:08.000000 aio-request-0.1.9a3/aio_request.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2021-06-28 12:00:08.000000 aio-request-0.1.9a3/aio_request.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       35 2021-06-28 12:00:08.000000 aio-request-0.1.9a3/aio_request.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       12 2021-06-28 12:00:08.000000 aio-request-0.1.9a3/aio_request.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2021-06-28 12:00:08.393817 aio-request-0.1.9a3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1237 2021-06-28 11:59:58.000000 aio-request-0.1.9a3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-07-13 13:02:09.157032 aio-request-0.1.9a4/
+-rw-r--r--   0 runner    (1001) docker     (121)     1068 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (121)     3817 2021-07-13 13:02:09.157032 aio-request-0.1.9a4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     2720 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/README.md
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-07-13 13:02:09.157032 aio-request-0.1.9a4/aio_request/
+-rw-r--r--   0 runner    (1001) docker     (121)     2772 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)    11917 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/aiohttp.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5973 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/base.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3331 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/client.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1278 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/context.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1131 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/deadline.py
+-rw-r--r--   0 runner    (1001) docker     (121)      597 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/delays_provider.py
+-rw-r--r--   0 runner    (1001) docker     (121)      662 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/metrics.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3288 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/opentelemetry.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5600 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/pipeline.py
+-rw-r--r--   0 runner    (1001) docker     (121)      428 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/priority.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1559 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/prometheus.py
+-rw-r--r--   0 runner    (1001) docker     (121)     4324 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/request.py
+-rw-r--r--   0 runner    (1001) docker     (121)     8972 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/request_strategy.py
+-rw-r--r--   0 runner    (1001) docker     (121)      842 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/response_classifier.py
+-rw-r--r--   0 runner    (1001) docker     (121)     3585 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/setup.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1865 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/tracing.py
+-rw-r--r--   0 runner    (1001) docker     (121)      253 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/transport.py
+-rw-r--r--   0 runner    (1001) docker     (121)     1987 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/aio_request/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2021-07-13 13:02:09.157032 aio-request-0.1.9a4/aio_request.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)     3817 2021-07-13 13:02:08.000000 aio-request-0.1.9a4/aio_request.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)      721 2021-07-13 13:02:08.000000 aio-request-0.1.9a4/aio_request.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2021-07-13 13:02:08.000000 aio-request-0.1.9a4/aio_request.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       35 2021-07-13 13:02:08.000000 aio-request-0.1.9a4/aio_request.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       12 2021-07-13 13:02:08.000000 aio-request-0.1.9a4/aio_request.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       38 2021-07-13 13:02:09.161032 aio-request-0.1.9a4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)     1237 2021-07-13 13:02:01.000000 aio-request-0.1.9a4/setup.py
```

### Comparing `aio-request-0.1.9a3/LICENSE` & `aio-request-0.1.9a4/LICENSE`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/PKG-INFO` & `aio-request-0.1.9a4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aio-request
-Version: 0.1.9a3
+Version: 0.1.9a4
 Summary: Various strategies for sending requests
 Home-page: UNKNOWN
 Author: Yury Pliner
 Author-email: yury.pliner@gmail.com
 License: MIT
 Description: # aio-request
```

### Comparing `aio-request-0.1.9a3/README.md` & `aio-request-0.1.9a4/README.md`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/__init__.py` & `aio-request-0.1.9a4/aio_request/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 # flake8: noqa
 import collections
 import re
 import sys
 
 from .base import ClosableResponse, EmptyResponse, Header, Method, Request, Response
-from .client import Client, setup
+from .client import Client, DefaultClient
 from .context import get_context, set_context
 from .deadline import Deadline
 from .delays_provider import constant_delays, linear_delays
 from .metrics import NOOP_METRICS_PROVIDER, MetricsProvider, NoopMetricsProvider
 from .pipeline import (
     LowTimeoutRequestModule,
     MetricsModule,
-    RequestHandler,
+    NextModuleFunc,
     RequestModule,
-    RequestSendingModule,
     TracingModule,
+    TransportModule,
     build_pipeline,
 )
 from .priority import Priority
 from .request import delete, get, post, post_json, put, put_json
 from .request_strategy import (
     MethodBasedStrategy,
     ParallelRequestStrategy,
@@ -31,14 +31,15 @@
     SingleAttemptRequestStrategy,
     parallel_strategy,
     retry_until_deadline_expired,
     sequential_strategy,
     single_attempt_strategy,
 )
 from .response_classifier import DefaultResponseClassifier, ResponseClassifier, ResponseVerdict
+from .setup import setup, setup_v2
 from .tracing import NOOP_TRACER, NoopSpan, NoopTracer, Span, Tracer
 from .transport import Transport
 
 try:
     import aiohttp
 
     from .aiohttp import AioHttpDnsResolver, AioHttpTransport, aiohttp_middleware_factory, aiohttp_timeout
@@ -57,15 +58,15 @@
     import opentelemetry.semconv
     import opentelemetry.trace
 
     from .opentelemetry import OpenTelemetryTracer
 except ImportError:
     pass
 
-__version__ = "0.1.9a3"
+__version__ = "0.1.9a4"
 
 version = f"{__version__}, Python {sys.version}"
 
 VersionInfo = collections.namedtuple("VersionInfo", "major minor micro release_level serial")
 
 
 def _parse_version(v: str) -> VersionInfo:
```

### Comparing `aio-request-0.1.9a3/aio_request/aiohttp.py` & `aio-request-0.1.9a4/aio_request/aiohttp.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/base.py` & `aio-request-0.1.9a4/aio_request/base.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/client.py` & `aio-request-0.1.9a4/aio_request/pipeline.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,149 +1,181 @@
-import contextlib
-from typing import AsyncIterator, Callable, Optional, Union
+import abc
+import asyncio
+import time
+from typing import Awaitable, Callable, List, Optional
 
 import yarl
 
-from .base import ClosableResponse, Method, Request, Response
-from .context import get_context
+from .base import ClosableResponse, EmptyResponse, Header, Request
 from .deadline import Deadline
-from .delays_provider import linear_delays
-from .metrics import NOOP_METRICS_PROVIDER, MetricsProvider
-from .pipeline import LowTimeoutRequestModule, MetricsModule, RequestSendingModule, TracingModule, build_pipeline
+from .metrics import MetricsProvider
 from .priority import Priority
-from .request_strategy import (
-    MethodBasedStrategy,
-    RequestStrategy,
-    ResponseWithVerdict,
-    sequential_strategy,
-    single_attempt_strategy,
-)
-from .response_classifier import DefaultResponseClassifier, ResponseClassifier
-from .tracing import NOOP_TRACER, Tracer
+from .tracing import SpanKind, Tracer
 from .transport import Transport
 
+NextModuleFunc = Callable[[yarl.URL, Request, Deadline, Priority], Awaitable[ClosableResponse]]
 
-class Client:
-    __slots__ = (
-        "_endpoint",
-        "_transport",
-        "_response_classifier",
-        "_request_strategy",
-        "_priority",
-        "_timeout",
-        "_request_enricher",
-        "_pipeline",
-    )
 
-    def __init__(
+class RequestModule(abc.ABC):
+    __slots__ = ()
+
+    @abc.abstractmethod
+    async def execute(
         self,
+        next: NextModuleFunc,
         *,
         endpoint: yarl.URL,
-        transport: Transport,
-        response_classifier: ResponseClassifier,
-        request_strategy: RequestStrategy,
-        timeout: float,
+        request: Request,
+        deadline: Deadline,
+        priority: Priority,
+    ) -> ClosableResponse:
+        ...
+
+
+class LowTimeoutRequestModule(RequestModule):
+    __slots__ = ("_low_timeout_threshold",)
+
+    def __init__(self, low_timeout_threshold: float):
+        self._low_timeout_threshold = low_timeout_threshold
+
+    async def execute(
+        self,
+        next: NextModuleFunc,
+        *,
+        endpoint: yarl.URL,
+        request: Request,
+        deadline: Deadline,
         priority: Priority,
+    ) -> ClosableResponse:
+        if deadline.expired or deadline.timeout < self._low_timeout_threshold:
+            return EmptyResponse(status=408)
+
+        return await next(endpoint, request, deadline, priority)
+
+
+class TransportModule(RequestModule):
+    __slots__ = ("_transport", "_emit_system_headers", "_request_enricher")
+
+    def __init__(
+        self,
+        transport: Transport,
+        *,
         emit_system_headers: bool,
-        low_timeout_threshold: float,
-        request_enricher: Optional[Callable[[Request], Request]],
-        metrics_provider: MetricsProvider = NOOP_METRICS_PROVIDER,
-        tracer: Tracer = NOOP_TRACER,
+        request_enricher: Optional[Callable[[Request, bool], Awaitable[Request]]],
     ):
-        self._endpoint = endpoint
         self._transport = transport
-        self._response_classifier = response_classifier
-        self._request_strategy = request_strategy
-        self._priority = priority
-        self._timeout = timeout
+        self._emit_system_headers = emit_system_headers
         self._request_enricher = request_enricher
-        self._pipeline = build_pipeline(
-            [
-                TracingModule(tracer=tracer),
-                MetricsModule(metrics_provider=metrics_provider),
-                LowTimeoutRequestModule(low_timeout_threshold=low_timeout_threshold),
-                RequestSendingModule(transport, emit_system_headers=emit_system_headers),
-            ]
-        )
 
-    @contextlib.asynccontextmanager
-    async def request(
+    async def execute(
         self,
-        request: Request,
+        _: NextModuleFunc,
         *,
-        deadline: Optional[Deadline] = None,
-        priority: Optional[Priority] = None,
-        strategy: Optional[RequestStrategy] = None,
-    ) -> AsyncIterator[Response]:
-        if self._request_enricher is not None:
-            request = self._request_enricher(request)
-        context = get_context()
-        response_ctx = (strategy or self._request_strategy).request(
-            self._send_request,
-            self._endpoint,
-            request,
-            deadline or context.deadline or Deadline.from_timeout(self._timeout),
-            self.normalize_priority(priority or self._priority, context.priority),
+        endpoint: yarl.URL,
+        request: Request,
+        deadline: Deadline,
+        priority: Priority,
+    ) -> ClosableResponse:
+        if self._emit_system_headers:
+            request = request.update_headers(
+                {
+                    Header.X_REQUEST_DEADLINE_AT: str(deadline),  # for backward compatibility
+                    Header.X_REQUEST_PRIORITY: str(priority),
+                    Header.X_REQUEST_TIMEOUT: str(deadline.timeout),
+                }
+            )
+
+        request = (
+            await self._request_enricher(request, self._emit_system_headers)
+            if self._request_enricher is not None
+            else request
         )
-        async with response_ctx as response:
-            yield response.response
 
-    @staticmethod
-    def normalize_priority(priority: Priority, context_priority: Optional[Priority]) -> Priority:
-        if context_priority is None:
-            return priority
-
-        if priority == Priority.LOW and context_priority == Priority.HIGH:
-            return Priority.NORMAL
-
-        if priority == Priority.HIGH and context_priority == Priority.LOW:
-            return Priority.NORMAL
-
-        return priority
-
-    async def _send_request(
-        self, endpoint: yarl.URL, request: Request, deadline: Deadline, priority: Priority
-    ) -> ResponseWithVerdict[ClosableResponse]:
-        response = await self._pipeline(endpoint, request, deadline, priority)
-        return ResponseWithVerdict(response, self._response_classifier.classify(response))
-
-
-def setup(
-    *,
-    transport: Transport,
-    endpoint: Union[str, yarl.URL],
-    safe_method_strategy: RequestStrategy = sequential_strategy(attempts_count=3, delays_provider=linear_delays()),
-    unsafe_method_strategy: RequestStrategy = single_attempt_strategy(),
-    response_classifier: Optional[ResponseClassifier] = None,
-    timeout: float = 20.0,
-    priority: Priority = Priority.NORMAL,
-    low_timeout_threshold: float = 0.005,
-    emit_system_headers: bool = True,
-    request_enricher: Optional[Callable[[Request], Request]] = None,
-    metrics_provider: MetricsProvider = NOOP_METRICS_PROVIDER,
-    tracer: Tracer = NOOP_TRACER,
-) -> Client:
-    request_strategy = MethodBasedStrategy(
-        {
-            Method.GET: safe_method_strategy,
-            Method.POST: unsafe_method_strategy,
-            Method.PUT: unsafe_method_strategy,
-            Method.DELETE: unsafe_method_strategy,
+        return await self._transport.send(endpoint, request, deadline.timeout)
+
+
+class MetricsModule(RequestModule):
+    __slots__ = ("_metrics_provider",)
+
+    def __init__(self, metrics_provider: MetricsProvider):
+        self._metrics_provider = metrics_provider
+
+    async def execute(
+        self,
+        next: NextModuleFunc,
+        *,
+        endpoint: yarl.URL,
+        request: Request,
+        deadline: Deadline,
+        priority: Priority,
+    ) -> ClosableResponse:
+        started_at = time.perf_counter()
+        try:
+            response = await next(endpoint, request, deadline, priority)
+            self._capture_metrics(endpoint, request, response.status, started_at)
+            return response
+        except asyncio.CancelledError:
+            self._capture_metrics(endpoint, request, 499, started_at)
+            raise
+
+    def _capture_metrics(self, endpoint: yarl.URL, request: Request, status: int, started_at: float) -> None:
+        tags = {
+            "request_endpoint": endpoint.human_repr(),
+            "request_method": request.method,
+            "request_path": request.url.path,
+            "response_status": str(status),
         }
-    )
-    return Client(
-        endpoint=yarl.URL(endpoint) if isinstance(endpoint, str) else endpoint,
-        transport=transport,
-        response_classifier=response_classifier or DefaultResponseClassifier(),
-        request_strategy=request_strategy,
-        timeout=timeout,
-        priority=priority,
-        request_enricher=request_enricher,
-        low_timeout_threshold=low_timeout_threshold,
-        emit_system_headers=emit_system_headers,
-        metrics_provider=(
-            # try to acquire metrics_provider from transport
-            getattr(transport, "_metrics_provider", None)
-            or metrics_provider
-        ),
-        tracer=tracer,
-    )
+        elapsed = max(0.0, time.perf_counter() - started_at)
+        self._metrics_provider.increment_counter("aio_request_status", tags)
+        self._metrics_provider.observe_value("aio_request_latency", tags, elapsed)
+
+
+class TracingModule(RequestModule):
+    __slots__ = ("_tracer", "_emit_system_headers")
+
+    def __init__(self, tracer: Tracer, *, emit_system_headers: bool):
+        self._tracer = tracer
+        self._emit_system_headers = emit_system_headers
+
+    async def execute(
+        self,
+        next: NextModuleFunc,
+        *,
+        endpoint: yarl.URL,
+        request: Request,
+        deadline: Deadline,
+        priority: Priority,
+    ) -> ClosableResponse:
+        span_name = str(request.url)
+        with self._tracer.start_span(span_name, SpanKind.CLIENT) as span:
+            span.set_request_method(request.method)
+            span.set_request_endpoint(endpoint)
+            span.set_request_path(request.url)
+
+            response = await next(
+                endpoint,
+                (request.update_headers(self._tracer.get_context_headers()) if self._emit_system_headers else request),
+                deadline,
+                priority,
+            )
+
+            span.set_response_status(response.status)
+
+            return response
+
+
+def build_pipeline(modules: List[RequestModule]) -> NextModuleFunc:
+    async def _unsupported(
+        _: yarl.URL,
+        __: Request,
+        ___: Deadline,
+        ____: Priority,
+    ) -> ClosableResponse:
+        raise NotImplementedError()
+
+    def _execute_module(m: RequestModule, n: NextModuleFunc) -> NextModuleFunc:
+        return lambda e, r, d, p: m.execute(n, endpoint=e, request=r, deadline=d, priority=p)
+
+    pipeline: NextModuleFunc = _unsupported
+    for module in reversed(modules):
+        pipeline = _execute_module(module, pipeline)
+    return pipeline
```

### Comparing `aio-request-0.1.9a3/aio_request/context.py` & `aio-request-0.1.9a4/aio_request/context.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/deadline.py` & `aio-request-0.1.9a4/aio_request/deadline.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/delays_provider.py` & `aio-request-0.1.9a4/aio_request/delays_provider.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/metrics.py` & `aio-request-0.1.9a4/aio_request/metrics.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/opentelemetry.py` & `aio-request-0.1.9a4/aio_request/opentelemetry.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/prometheus.py` & `aio-request-0.1.9a4/aio_request/prometheus.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/request.py` & `aio-request-0.1.9a4/aio_request/request.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/request_strategy.py` & `aio-request-0.1.9a4/aio_request/request_strategy.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/response_classifier.py` & `aio-request-0.1.9a4/aio_request/response_classifier.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/tracing.py` & `aio-request-0.1.9a4/aio_request/tracing.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request/utils.py` & `aio-request-0.1.9a4/aio_request/utils.py`

 * *Files identical despite different names*

### Comparing `aio-request-0.1.9a3/aio_request.egg-info/PKG-INFO` & `aio-request-0.1.9a4/aio_request.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aio-request
-Version: 0.1.9a3
+Version: 0.1.9a4
 Summary: Various strategies for sending requests
 Home-page: UNKNOWN
 Author: Yury Pliner
 Author-email: yury.pliner@gmail.com
 License: MIT
 Description: # aio-request
```

### Comparing `aio-request-0.1.9a3/aio_request.egg-info/SOURCES.txt` & `aio-request-0.1.9a4/aio_request.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -13,14 +13,15 @@
 ./aio_request/opentelemetry.py
 ./aio_request/pipeline.py
 ./aio_request/priority.py
 ./aio_request/prometheus.py
 ./aio_request/request.py
 ./aio_request/request_strategy.py
 ./aio_request/response_classifier.py
+./aio_request/setup.py
 ./aio_request/tracing.py
 ./aio_request/transport.py
 ./aio_request/utils.py
 aio_request.egg-info/PKG-INFO
 aio_request.egg-info/SOURCES.txt
 aio_request.egg-info/dependency_links.txt
 aio_request.egg-info/requires.txt
```

### Comparing `aio-request-0.1.9a3/setup.py` & `aio-request-0.1.9a4/setup.py`

 * *Files identical despite different names*

