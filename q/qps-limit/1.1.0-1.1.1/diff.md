# Comparing `tmp/qps_limit-1.1.0-py3-none-any.whl.zip` & `tmp/qps_limit-1.1.1-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,10 +1,10 @@
-Zip file size: 5613 bytes, number of entries: 8
--rw-rw-r--  2.0 unx      165 b- defN 23-Jul-07 09:35 qps_limit/__init__.py
--rw-rw-r--  2.0 unx     6926 b- defN 23-Jul-07 09:35 qps_limit/limiter.py
+Zip file size: 5719 bytes, number of entries: 8
+-rw-rw-r--  2.0 unx      165 b- defN 23-Jul-23 06:28 qps_limit/__init__.py
+-rw-rw-r--  2.0 unx     6926 b- defN 23-Jul-23 06:28 qps_limit/limiter.py
 -rw-rw-r--  2.0 unx     5474 b- defN 23-Jul-07 07:33 qps_limit/run.py
--rw-rw-r--  2.0 unx     2565 b- defN 23-Jul-07 09:35 qps_limit-1.1.0.dist-info/METADATA
--rw-rw-r--  2.0 unx       92 b- defN 23-Jul-07 09:35 qps_limit-1.1.0.dist-info/WHEEL
--rw-rw-r--  2.0 unx       10 b- defN 23-Jul-07 09:35 qps_limit-1.1.0.dist-info/top_level.txt
--rw-rw-r--  2.0 unx        1 b- defN 23-Jul-07 09:35 qps_limit-1.1.0.dist-info/zip-safe
-?rw-rw-r--  2.0 unx      621 b- defN 23-Jul-07 09:35 qps_limit-1.1.0.dist-info/RECORD
-8 files, 15854 bytes uncompressed, 4529 bytes compressed:  71.4%
+-rw-rw-r--  2.0 unx     2803 b- defN 23-Jul-23 06:29 qps_limit-1.1.1.dist-info/METADATA
+-rw-rw-r--  2.0 unx       92 b- defN 23-Jul-23 06:29 qps_limit-1.1.1.dist-info/WHEEL
+-rw-rw-r--  2.0 unx       10 b- defN 23-Jul-23 06:29 qps_limit-1.1.1.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx        1 b- defN 23-Jul-23 06:29 qps_limit-1.1.1.dist-info/zip-safe
+?rw-rw-r--  2.0 unx      621 b- defN 23-Jul-23 06:29 qps_limit-1.1.1.dist-info/RECORD
+8 files, 16092 bytes uncompressed, 4635 bytes compressed:  71.2%
```

## zipnote {}

```diff
@@ -3,23 +3,23 @@
 
 Filename: qps_limit/limiter.py
 Comment: 
 
 Filename: qps_limit/run.py
 Comment: 
 
-Filename: qps_limit-1.1.0.dist-info/METADATA
+Filename: qps_limit-1.1.1.dist-info/METADATA
 Comment: 
 
-Filename: qps_limit-1.1.0.dist-info/WHEEL
+Filename: qps_limit-1.1.1.dist-info/WHEEL
 Comment: 
 
-Filename: qps_limit-1.1.0.dist-info/top_level.txt
+Filename: qps_limit-1.1.1.dist-info/top_level.txt
 Comment: 
 
-Filename: qps_limit-1.1.0.dist-info/zip-safe
+Filename: qps_limit-1.1.1.dist-info/zip-safe
 Comment: 
 
-Filename: qps_limit-1.1.0.dist-info/RECORD
+Filename: qps_limit-1.1.1.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## qps_limit/__init__.py

```diff
@@ -1,8 +1,8 @@
-__version__ = '1.1.0'
+__version__ = '1.1.1'
 
 from .limiter import Limiter
 from .run import async_batch_run, batch_run
 
 __all__ = [
     'batch_run',
     'async_batch_run',
```

## qps_limit/limiter.py

 * *Ordering differences only*

```diff
@@ -22,14 +22,25 @@
         worker_max_qps: Optional[float] = None,
         streaming: bool = False,
         ordered: bool = True,
         verbose: bool = False,
         warmup_steps: int = 1,
         max_coroutines: int = 128
     ) -> Callable:
+        self.func = func
+        self.params = params
+        self.callback = callback
+        self.num_workers = num_workers
+        self.worker_max_qps = worker_max_qps
+        self.streaming = streaming
+        self.ordered = ordered
+        self.verbose = verbose
+        self.warmup_steps = warmup_steps
+        self.max_coroutines = max_coroutines
+
         self.logger = logging.getLogger(__name__)
         self.logger.setLevel(logging.INFO)
         handler = logging.StreamHandler()
         handler.setLevel(logging.INFO)
         formatter = logging.Formatter(
             fmt="%(asctime)s - %(levelname)s - %(message)s",
             datefmt="%m/%d/%Y %H:%M:%S"
@@ -39,25 +50,14 @@
 
         try:
             multiprocessing.set_start_method('fork')
         except RuntimeError:
             if self.verbose:
                 self.logger.error("multiprocessing set_start_method error")
 
-        self.func = func
-        self.params = params
-        self.callback = callback
-        self.num_workers = num_workers
-        self.worker_max_qps = worker_max_qps
-        self.streaming = streaming
-        self.ordered = ordered
-        self.verbose = verbose
-        self.warmup_steps = warmup_steps
-        self.max_coroutines = max_coroutines
-
         if self.verbose:
             self.logger.info("warmup worker nodes with {} data".format(self.warmup_steps))
         warmup_param_iterator = itertools.islice(self.params(), self.warmup_steps)
         warmup_start_time = time.time()
         batch_run(
             func=self.func,
             params=warmup_param_iterator,
```

## Comparing `qps_limit-1.1.0.dist-info/METADATA` & `qps_limit-1.1.1.dist-info/METADATA`

 * *Files 12% similar despite different names*

```diff
@@ -1,15 +1,16 @@
 Metadata-Version: 2.1
 Name: qps-limit
-Version: 1.1.0
+Version: 1.1.1
 Summary: Run functions under any limited rate
 Home-page: https://github.com/antct/qps-limit
 Author: tt
 Author-email: 527892245@qq.com
 License: GPLv2
+Platform: UNKNOWN
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: GNU General Public License v2 (GPLv2)
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
@@ -93,7 +94,20 @@
     streaming=False,
     ordered=True
 )
 
 for idx, r in f():
     print(idx, r)
 ```
+
+> The following code shows how to initialize resources that can not be `pickled` between processes
+
+```python
+resource = None
+
+async def func(n):
+    global resource
+    if resource is None:
+        resource = {}
+```
+
+
```

