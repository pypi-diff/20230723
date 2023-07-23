# Comparing `tmp/httpx-file-0.0.1.dev0.tar.gz` & `tmp/httpx-file-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "httpx-file-0.0.1.dev0.tar", last modified: Wed Sep 29 17:01:10 2021, max compression
+gzip compressed data, was "httpx-file-0.2.0.tar", last modified: Sun Jul 23 17:14:37 2023, max compression
```

## Comparing `httpx-file-0.0.1.dev0.tar` & `httpx-file-0.2.0.tar`

### file list

```diff
@@ -1,12 +1,15 @@
-drwxrwxrwx   0        0        0        0 2021-09-29 17:01:10.043650 httpx-file-0.0.1.dev0/
--rw-rw-rw-   0        0        0     1474 2021-09-29 15:23:35.000000 httpx-file-0.0.1.dev0/LICENSE
--rw-rw-rw-   0        0        0     1951 2021-09-29 17:01:10.044636 httpx-file-0.0.1.dev0/PKG-INFO
-drwxrwxrwx   0        0        0        0 2021-09-29 17:01:10.040632 httpx-file-0.0.1.dev0/httpx_file.egg-info/
--rw-rw-rw-   0        0        0     1951 2021-09-29 17:01:09.000000 httpx-file-0.0.1.dev0/httpx_file.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      228 2021-09-29 17:01:09.000000 httpx-file-0.0.1.dev0/httpx_file.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2021-09-29 17:01:09.000000 httpx-file-0.0.1.dev0/httpx_file.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2021-09-29 03:30:12.000000 httpx-file-0.0.1.dev0/httpx_file.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       28 2021-09-29 17:01:09.000000 httpx-file-0.0.1.dev0/httpx_file.egg-info/requires.txt
--rw-rw-rw-   0        0        0        1 2021-09-29 17:01:09.000000 httpx-file-0.0.1.dev0/httpx_file.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     1267 2021-09-29 17:01:10.049632 httpx-file-0.0.1.dev0/setup.cfg
--rw-rw-rw-   0        0        0       37 2021-09-29 03:18:19.000000 httpx-file-0.0.1.dev0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:14:37.784633 httpx-file-0.2.0/
+-rw-rw-rw-   0        0        0     1497 2023-07-23 16:15:58.000000 httpx-file-0.2.0/LICENSE
+-rw-rw-rw-   0        0        0     2897 2023-07-23 17:14:37.785617 httpx-file-0.2.0/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-07-23 17:14:37.767557 httpx-file-0.2.0/httpx_file/
+-rw-rw-rw-   0        0        0     3956 2023-07-23 16:58:28.000000 httpx-file-0.2.0/httpx_file/__init__.py
+-rw-rw-rw-   0        0        0        0 2023-07-23 16:58:18.000000 httpx-file-0.2.0/httpx_file/py.typed
+drwxrwxrwx   0        0        0        0 2023-07-23 17:14:37.783616 httpx-file-0.2.0/httpx_file.egg-info/
+-rw-rw-rw-   0        0        0     2897 2023-07-23 17:14:37.000000 httpx-file-0.2.0/httpx_file.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      271 2023-07-23 17:14:37.000000 httpx-file-0.2.0/httpx_file.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 17:14:37.000000 httpx-file-0.2.0/httpx_file.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-07-23 16:24:14.000000 httpx-file-0.2.0/httpx_file.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       72 2023-07-23 17:14:37.000000 httpx-file-0.2.0/httpx_file.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 17:14:37.000000 httpx-file-0.2.0/httpx_file.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     1552 2023-07-23 17:14:37.786617 httpx-file-0.2.0/setup.cfg
+-rw-rw-rw-   0        0        0       39 2023-07-23 16:15:58.000000 httpx-file-0.2.0/setup.py
```

### Comparing `httpx-file-0.0.1.dev0/LICENSE` & `httpx-file-0.2.0/LICENSE`

 * *Ordering differences only*

 * *Files 10% similar despite different names*

```diff
@@ -1,24 +1,24 @@
-Copyright (c) 2021, Nuno André Novo
-All rights reserved.
-
-Redistribution and use in source and binary forms, with or without
-modification, are permitted provided that the following conditions are met:
-* Redistributions of source code must retain the above copyright notice, this
-  list of conditions and the following disclaimer.
-* Redistributions in binary form must reproduce the above copyright notice,
-  this list of conditions and the following disclaimer in the documentation
-  and/or other materials provided with the distribution.
-* Neither the name of the <copyright holder> nor the names of its contributors
-  may be used to endorse or promote products derived from this software without
-  specific prior written permission.
-
-THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
-ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
-WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
-DISCLAIMED. IN NO EVENT SHALL <COPYRIGHT HOLDER> BE LIABLE FOR ANY DIRECT,
-INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING,
-BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
-DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
-LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE
-OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
+Copyright (c) 2021, Nuno André Novo
+All rights reserved.
+
+Redistribution and use in source and binary forms, with or without
+modification, are permitted provided that the following conditions are met:
+* Redistributions of source code must retain the above copyright notice, this
+  list of conditions and the following disclaimer.
+* Redistributions in binary form must reproduce the above copyright notice,
+  this list of conditions and the following disclaimer in the documentation
+  and/or other materials provided with the distribution.
+* Neither the name of the <copyright holder> nor the names of its contributors
+  may be used to endorse or promote products derived from this software without
+  specific prior written permission.
+
+THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
+ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
+WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
+DISCLAIMED. IN NO EVENT SHALL <COPYRIGHT HOLDER> BE LIABLE FOR ANY DIRECT,
+INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING,
+BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
+DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
+LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE
+OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
 ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```

### Comparing `httpx-file-0.0.1.dev0/PKG-INFO` & `httpx-file-0.2.0/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,35 +1,38 @@
 Metadata-Version: 2.1
 Name: httpx-file
-Version: 0.0.1.dev0
+Version: 0.2.0
 Summary: File transport adapter for httpx.
-Home-page: https://github.com/nuno-andre/httpx-file
+Home-page: https://github.com/nuno-andre/httpx-file#readme
 Author: Nuno André
 Author-email: mail@nunoand.re
-License: MIT
+License: BSD-3-Clause
 Project-URL: Source, https://github.com/nuno-andre/httpx-file
 Project-URL: Bug Tracker, https://github.com/nuno-andre/httpx-file/issues
 Platform: any
-Classifier: Development Status :: 2 - Pre-Alpha
+Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Information Technology
 Classifier: Intended Audience :: System Administrators
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Classifier: Programming Language :: Python :: 3.12
 Classifier: Topic :: Software Development
 Classifier: Typing :: Typed
 Requires-Python: >=3.6.1
 Description-Content-Type: text/markdown
-Provides-Extra: tests
+Provides-Extra: dev
 License-File: LICENSE
 
 # httpx-file
 
 Transport adapter fort __[httpx](https://github.com/encode/httpx)__ to allow
 `file://` URI fetching in the local filesystem.
 
@@ -37,15 +40,17 @@
 ## Installation
 
 <a href="https://pypi.org/project/httpx-file/"><pre>
 pip install httpx-file
 </pre></a>
 
 
-## Usage
+## Usage 
+
+### Synchronous
 
 _httpx-file_ subclasses `httpx.Client`, so you can just replace `httpx.Client`
 with `httpx_file.Client` to get the same behavior with added `file://` protocol
 support.
 
 ```python
 from httpx_file import Client
@@ -60,8 +65,37 @@
 from httpx_file import FileTransport
 from httpx import Client
 
 client = Client(mounts={'file://': FileTransport()})
 client.get('file:///etc/fstab)
 ```
 
+### Asynchronous
+
+It is also possible to use _httpx-file_ possibilities asynchronous way. 
+To do this, you can just replace 'httpx.AsyncClient' with 'httpx_file.AsyncClient'.
+
+```python
+from httpx_file import AsyncClient
+
+# Taken from tests/test_transport.py
+
+from pathlib import Path
+
+THIS = Path(__file__)
+
+async def test_async_client():
+    async_client = AsyncClient()
+    async_response = await async_client.get(THIS.as_uri())
+
+    assert async_response.content == THIS.read_bytes()
+```
+
+Or you can also mount `FileTransport` in a `httpx.AsyncClient` instance.
+
+```python
+from httpx_file import FileTransport
+from httpx import AsyncClient
 
+client = AsyncClient(mounts={'file://': FileTransport()})
+client.get('file:///etc/fstab)
+```
```

#### html2text {}

```diff
@@ -1,25 +1,37 @@
-Metadata-Version: 2.1 Name: httpx-file Version: 0.0.1.dev0 Summary: File
-transport adapter for httpx. Home-page: https://github.com/nuno-andre/httpx-
-file Author: Nuno AndrÃ© Author-email: mail@nunoand.re License: MIT Project-
-URL: Source, https://github.com/nuno-andre/httpx-file Project-URL: Bug Tracker,
-https://github.com/nuno-andre/httpx-file/issues Platform: any Classifier:
-Development Status :: 2 - Pre-Alpha Classifier: Intended Audience :: Developers
-Classifier: Intended Audience :: Information Technology Classifier: Intended
-Audience :: System Administrators Classifier: License :: OSI Approved :: BSD
-License Classifier: Natural Language :: English Classifier: Operating System ::
-OS Independent Classifier: Programming Language :: Python Classifier:
+Metadata-Version: 2.1 Name: httpx-file Version: 0.2.0 Summary: File transport
+adapter for httpx. Home-page: https://github.com/nuno-andre/httpx-file#readme
+Author: Nuno AndrÃ© Author-email: mail@nunoand.re License: BSD-3-Clause
+Project-URL: Source, https://github.com/nuno-andre/httpx-file Project-URL: Bug
+Tracker, https://github.com/nuno-andre/httpx-file/issues Platform: any
+Classifier: Development Status :: 4 - Beta Classifier: Intended Audience ::
+Developers Classifier: Intended Audience :: Information Technology Classifier:
+Intended Audience :: System Administrators Classifier: License :: OSI Approved
+:: BSD License Classifier: Natural Language :: English Classifier: Operating
+System :: OS Independent Classifier: Programming Language :: Python Classifier:
 Programming Language :: Python :: 3.6 Classifier: Programming Language ::
 Python :: 3.7 Classifier: Programming Language :: Python :: 3.8 Classifier:
-Programming Language :: Python :: 3.9 Classifier: Topic :: Software Development
-Classifier: Typing :: Typed Requires-Python: >=3.6.1 Description-Content-Type:
-text/markdown Provides-Extra: tests License-File: LICENSE # httpx-file
-Transport adapter fort __[httpx](https://github.com/encode/httpx)__ to allow
-`file://` URI fetching in the local filesystem. ## Installation
+Programming Language :: Python :: 3.9 Classifier: Programming Language ::
+Python :: 3.10 Classifier: Programming Language :: Python :: 3.11 Classifier:
+Programming Language :: Python :: 3.12 Classifier: Topic :: Software
+Development Classifier: Typing :: Typed Requires-Python: >=3.6.1 Description-
+Content-Type: text/markdown Provides-Extra: dev License-File: LICENSE # httpx-
+file Transport adapter fort __[httpx](https://github.com/encode/httpx)__ to
+allow `file://` URI fetching in the local filesystem. ## Installation
 pip_install_httpx-file
- ## Usage _httpx-file_ subclasses `httpx.Client`, so you can just replace
-`httpx.Client` with `httpx_file.Client` to get the same behavior with added
-`file://` protocol support. ```python from httpx_file import Client client =
-Client() client.get('file:///etc/fstab) ``` Or you can also mount
+ ## Usage ### Synchronous _httpx-file_ subclasses `httpx.Client`, so you can
+just replace `httpx.Client` with `httpx_file.Client` to get the same behavior
+with added `file://` protocol support. ```python from httpx_file import Client
+client = Client() client.get('file:///etc/fstab) ``` Or you can also mount
 `FileTransport` in a `httpx.Client` instance. ```python from httpx_file import
 FileTransport from httpx import Client client = Client(mounts={'file://':
+FileTransport()}) client.get('file:///etc/fstab) ``` ### Asynchronous It is
+also possible to use _httpx-file_ possibilities asynchronous way. To do this,
+you can just replace 'httpx.AsyncClient' with 'httpx_file.AsyncClient'.
+```python from httpx_file import AsyncClient # Taken from tests/
+test_transport.py from pathlib import Path THIS = Path(__file__) async def
+test_async_client(): async_client = AsyncClient() async_response = await
+async_client.get(THIS.as_uri()) assert async_response.content ==
+THIS.read_bytes() ``` Or you can also mount `FileTransport` in a
+`httpx.AsyncClient` instance. ```python from httpx_file import FileTransport
+from httpx import AsyncClient client = AsyncClient(mounts={'file://':
 FileTransport()}) client.get('file:///etc/fstab) ```
```

### Comparing `httpx-file-0.0.1.dev0/httpx_file.egg-info/PKG-INFO` & `httpx-file-0.2.0/httpx_file.egg-info/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,35 +1,38 @@
 Metadata-Version: 2.1
 Name: httpx-file
-Version: 0.0.1.dev0
+Version: 0.2.0
 Summary: File transport adapter for httpx.
-Home-page: https://github.com/nuno-andre/httpx-file
+Home-page: https://github.com/nuno-andre/httpx-file#readme
 Author: Nuno André
 Author-email: mail@nunoand.re
-License: MIT
+License: BSD-3-Clause
 Project-URL: Source, https://github.com/nuno-andre/httpx-file
 Project-URL: Bug Tracker, https://github.com/nuno-andre/httpx-file/issues
 Platform: any
-Classifier: Development Status :: 2 - Pre-Alpha
+Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Information Technology
 Classifier: Intended Audience :: System Administrators
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Classifier: Programming Language :: Python :: 3.12
 Classifier: Topic :: Software Development
 Classifier: Typing :: Typed
 Requires-Python: >=3.6.1
 Description-Content-Type: text/markdown
-Provides-Extra: tests
+Provides-Extra: dev
 License-File: LICENSE
 
 # httpx-file
 
 Transport adapter fort __[httpx](https://github.com/encode/httpx)__ to allow
 `file://` URI fetching in the local filesystem.
 
@@ -37,15 +40,17 @@
 ## Installation
 
 <a href="https://pypi.org/project/httpx-file/"><pre>
 pip install httpx-file
 </pre></a>
 
 
-## Usage
+## Usage 
+
+### Synchronous
 
 _httpx-file_ subclasses `httpx.Client`, so you can just replace `httpx.Client`
 with `httpx_file.Client` to get the same behavior with added `file://` protocol
 support.
 
 ```python
 from httpx_file import Client
@@ -60,8 +65,37 @@
 from httpx_file import FileTransport
 from httpx import Client
 
 client = Client(mounts={'file://': FileTransport()})
 client.get('file:///etc/fstab)
 ```
 
+### Asynchronous
+
+It is also possible to use _httpx-file_ possibilities asynchronous way. 
+To do this, you can just replace 'httpx.AsyncClient' with 'httpx_file.AsyncClient'.
+
+```python
+from httpx_file import AsyncClient
+
+# Taken from tests/test_transport.py
+
+from pathlib import Path
+
+THIS = Path(__file__)
+
+async def test_async_client():
+    async_client = AsyncClient()
+    async_response = await async_client.get(THIS.as_uri())
+
+    assert async_response.content == THIS.read_bytes()
+```
+
+Or you can also mount `FileTransport` in a `httpx.AsyncClient` instance.
+
+```python
+from httpx_file import FileTransport
+from httpx import AsyncClient
 
+client = AsyncClient(mounts={'file://': FileTransport()})
+client.get('file:///etc/fstab)
+```
```

#### html2text {}

```diff
@@ -1,25 +1,37 @@
-Metadata-Version: 2.1 Name: httpx-file Version: 0.0.1.dev0 Summary: File
-transport adapter for httpx. Home-page: https://github.com/nuno-andre/httpx-
-file Author: Nuno AndrÃ© Author-email: mail@nunoand.re License: MIT Project-
-URL: Source, https://github.com/nuno-andre/httpx-file Project-URL: Bug Tracker,
-https://github.com/nuno-andre/httpx-file/issues Platform: any Classifier:
-Development Status :: 2 - Pre-Alpha Classifier: Intended Audience :: Developers
-Classifier: Intended Audience :: Information Technology Classifier: Intended
-Audience :: System Administrators Classifier: License :: OSI Approved :: BSD
-License Classifier: Natural Language :: English Classifier: Operating System ::
-OS Independent Classifier: Programming Language :: Python Classifier:
+Metadata-Version: 2.1 Name: httpx-file Version: 0.2.0 Summary: File transport
+adapter for httpx. Home-page: https://github.com/nuno-andre/httpx-file#readme
+Author: Nuno AndrÃ© Author-email: mail@nunoand.re License: BSD-3-Clause
+Project-URL: Source, https://github.com/nuno-andre/httpx-file Project-URL: Bug
+Tracker, https://github.com/nuno-andre/httpx-file/issues Platform: any
+Classifier: Development Status :: 4 - Beta Classifier: Intended Audience ::
+Developers Classifier: Intended Audience :: Information Technology Classifier:
+Intended Audience :: System Administrators Classifier: License :: OSI Approved
+:: BSD License Classifier: Natural Language :: English Classifier: Operating
+System :: OS Independent Classifier: Programming Language :: Python Classifier:
 Programming Language :: Python :: 3.6 Classifier: Programming Language ::
 Python :: 3.7 Classifier: Programming Language :: Python :: 3.8 Classifier:
-Programming Language :: Python :: 3.9 Classifier: Topic :: Software Development
-Classifier: Typing :: Typed Requires-Python: >=3.6.1 Description-Content-Type:
-text/markdown Provides-Extra: tests License-File: LICENSE # httpx-file
-Transport adapter fort __[httpx](https://github.com/encode/httpx)__ to allow
-`file://` URI fetching in the local filesystem. ## Installation
+Programming Language :: Python :: 3.9 Classifier: Programming Language ::
+Python :: 3.10 Classifier: Programming Language :: Python :: 3.11 Classifier:
+Programming Language :: Python :: 3.12 Classifier: Topic :: Software
+Development Classifier: Typing :: Typed Requires-Python: >=3.6.1 Description-
+Content-Type: text/markdown Provides-Extra: dev License-File: LICENSE # httpx-
+file Transport adapter fort __[httpx](https://github.com/encode/httpx)__ to
+allow `file://` URI fetching in the local filesystem. ## Installation
 pip_install_httpx-file
- ## Usage _httpx-file_ subclasses `httpx.Client`, so you can just replace
-`httpx.Client` with `httpx_file.Client` to get the same behavior with added
-`file://` protocol support. ```python from httpx_file import Client client =
-Client() client.get('file:///etc/fstab) ``` Or you can also mount
+ ## Usage ### Synchronous _httpx-file_ subclasses `httpx.Client`, so you can
+just replace `httpx.Client` with `httpx_file.Client` to get the same behavior
+with added `file://` protocol support. ```python from httpx_file import Client
+client = Client() client.get('file:///etc/fstab) ``` Or you can also mount
 `FileTransport` in a `httpx.Client` instance. ```python from httpx_file import
 FileTransport from httpx import Client client = Client(mounts={'file://':
+FileTransport()}) client.get('file:///etc/fstab) ``` ### Asynchronous It is
+also possible to use _httpx-file_ possibilities asynchronous way. To do this,
+you can just replace 'httpx.AsyncClient' with 'httpx_file.AsyncClient'.
+```python from httpx_file import AsyncClient # Taken from tests/
+test_transport.py from pathlib import Path THIS = Path(__file__) async def
+test_async_client(): async_client = AsyncClient() async_response = await
+async_client.get(THIS.as_uri()) assert async_response.content ==
+THIS.read_bytes() ``` Or you can also mount `FileTransport` in a
+`httpx.AsyncClient` instance. ```python from httpx_file import FileTransport
+from httpx import AsyncClient client = AsyncClient(mounts={'file://':
 FileTransport()}) client.get('file:///etc/fstab) ```
```

### Comparing `httpx-file-0.0.1.dev0/setup.cfg` & `httpx-file-0.2.0/setup.cfg`

 * *Files 14% similar despite different names*

```diff
@@ -10,71 +10,88 @@
 00000090: 7472 616e 7370 6f72 7420 6164 6170 7465  transport adapte
 000000a0: 7220 666f 7220 6874 7470 782e 0d0a 6c6f  r for httpx...lo
 000000b0: 6e67 5f64 6573 6372 6970 7469 6f6e 203d  ng_description =
 000000c0: 2066 696c 653a 2072 6561 646d 652e 6d64   file: readme.md
 000000d0: 0d0a 6c6f 6e67 5f64 6573 6372 6970 7469  ..long_descripti
 000000e0: 6f6e 5f63 6f6e 7465 6e74 5f74 7970 6520  on_content_type 
 000000f0: 3d20 7465 7874 2f6d 6172 6b64 6f77 6e0d  = text/markdown.
-00000100: 0a6c 6963 656e 7365 203d 204d 4954 0d0a  .license = MIT..
-00000110: 6c69 6365 6e73 655f 6669 6c65 7320 3d20  license_files = 
-00000120: 4c49 4345 4e53 450d 0a75 726c 203d 2068  LICENSE..url = h
-00000130: 7474 7073 3a2f 2f67 6974 6875 622e 636f  ttps://github.co
-00000140: 6d2f 6e75 6e6f 2d61 6e64 7265 2f68 7474  m/nuno-andre/htt
-00000150: 7078 2d66 696c 650d 0a70 726f 6a65 6374  px-file..project
-00000160: 5f75 726c 7320 3d20 0d0a 0953 6f75 7263  _urls = ...Sourc
-00000170: 6520 3d20 6874 7470 733a 2f2f 6769 7468  e = https://gith
-00000180: 7562 2e63 6f6d 2f6e 756e 6f2d 616e 6472  ub.com/nuno-andr
-00000190: 652f 6874 7470 782d 6669 6c65 0d0a 0942  e/httpx-file...B
-000001a0: 7567 2054 7261 636b 6572 203d 2068 7474  ug Tracker = htt
-000001b0: 7073 3a2f 2f67 6974 6875 622e 636f 6d2f  ps://github.com/
-000001c0: 6e75 6e6f 2d61 6e64 7265 2f68 7474 7078  nuno-andre/httpx
-000001d0: 2d66 696c 652f 6973 7375 6573 0d0a 636c  -file/issues..cl
-000001e0: 6173 7369 6669 6572 7320 3d20 0d0a 0944  assifiers = ...D
-000001f0: 6576 656c 6f70 6d65 6e74 2053 7461 7475  evelopment Statu
-00000200: 7320 3a3a 2032 202d 2050 7265 2d41 6c70  s :: 2 - Pre-Alp
-00000210: 6861 0d0a 0949 6e74 656e 6465 6420 4175  ha...Intended Au
-00000220: 6469 656e 6365 203a 3a20 4465 7665 6c6f  dience :: Develo
-00000230: 7065 7273 0d0a 0949 6e74 656e 6465 6420  pers...Intended 
-00000240: 4175 6469 656e 6365 203a 3a20 496e 666f  Audience :: Info
-00000250: 726d 6174 696f 6e20 5465 6368 6e6f 6c6f  rmation Technolo
-00000260: 6779 0d0a 0949 6e74 656e 6465 6420 4175  gy...Intended Au
-00000270: 6469 656e 6365 203a 3a20 5379 7374 656d  dience :: System
-00000280: 2041 646d 696e 6973 7472 6174 6f72 730d   Administrators.
-00000290: 0a09 4c69 6365 6e73 6520 3a3a 204f 5349  ..License :: OSI
-000002a0: 2041 7070 726f 7665 6420 3a3a 2042 5344   Approved :: BSD
-000002b0: 204c 6963 656e 7365 0d0a 094e 6174 7572   License...Natur
-000002c0: 616c 204c 616e 6775 6167 6520 3a3a 2045  al Language :: E
-000002d0: 6e67 6c69 7368 0d0a 094f 7065 7261 7469  nglish...Operati
-000002e0: 6e67 2053 7973 7465 6d20 3a3a 204f 5320  ng System :: OS 
-000002f0: 496e 6465 7065 6e64 656e 740d 0a09 5072  Independent...Pr
-00000300: 6f67 7261 6d6d 696e 6720 4c61 6e67 7561  ogramming Langua
-00000310: 6765 203a 3a20 5079 7468 6f6e 0d0a 0950  ge :: Python...P
-00000320: 726f 6772 616d 6d69 6e67 204c 616e 6775  rogramming Langu
-00000330: 6167 6520 3a3a 2050 7974 686f 6e20 3a3a  age :: Python ::
-00000340: 2033 2e36 0d0a 0950 726f 6772 616d 6d69   3.6...Programmi
-00000350: 6e67 204c 616e 6775 6167 6520 3a3a 2050  ng Language :: P
-00000360: 7974 686f 6e20 3a3a 2033 2e37 0d0a 0950  ython :: 3.7...P
-00000370: 726f 6772 616d 6d69 6e67 204c 616e 6775  rogramming Langu
-00000380: 6167 6520 3a3a 2050 7974 686f 6e20 3a3a  age :: Python ::
-00000390: 2033 2e38 0d0a 0950 726f 6772 616d 6d69   3.8...Programmi
-000003a0: 6e67 204c 616e 6775 6167 6520 3a3a 2050  ng Language :: P
-000003b0: 7974 686f 6e20 3a3a 2033 2e39 0d0a 0954  ython :: 3.9...T
-000003c0: 6f70 6963 203a 3a20 536f 6674 7761 7265  opic :: Software
-000003d0: 2044 6576 656c 6f70 6d65 6e74 0d0a 0954   Development...T
-000003e0: 7970 696e 6720 3a3a 2054 7970 6564 0d0a  yping :: Typed..
-000003f0: 706c 6174 666f 726d 7320 3d20 616e 790d  platforms = any.
-00000400: 0a0d 0a5b 6f70 7469 6f6e 735d 0d0a 7a69  ...[options]..zi
-00000410: 705f 7361 6665 203d 2066 616c 7365 0d0a  p_safe = false..
-00000420: 7079 7468 6f6e 5f72 6571 7569 7265 7320  python_requires 
-00000430: 3d20 3e3d 2033 2e36 2e31 0d0a 696e 7374  = >= 3.6.1..inst
-00000440: 616c 6c5f 7265 7175 6972 6573 203d 200d  all_requires = .
-00000450: 0a09 6874 7470 7820 3e3d 2030 2e31 380d  ..httpx >= 0.18.
-00000460: 0a0d 0a5b 6f70 7469 6f6e 732e 6578 7472  ...[options.extr
-00000470: 6173 5f72 6571 7569 7265 5d0d 0a74 6573  as_require]..tes
-00000480: 7473 203d 200d 0a09 7079 7465 7374 0d0a  ts = ...pytest..
-00000490: 0d0a 5b66 6c61 6b65 385d 0d0a 6d61 782d  ..[flake8]..max-
-000004a0: 6c69 6e65 2d6c 656e 6774 6820 3d20 3830  line-length = 80
-000004b0: 0d0a 6967 6e6f 7265 203d 2045 3234 312c  ..ignore = E241,
-000004c0: 2045 3430 320d 0a0d 0a5b 6567 675f 696e   E402....[egg_in
-000004d0: 666f 5d0d 0a74 6167 5f62 7569 6c64 203d  fo]..tag_build =
-000004e0: 200d 0a74 6167 5f64 6174 6520 3d20 300d   ..tag_date = 0.
-000004f0: 0a0d 0a                                  ...
+00000100: 0a6c 6963 656e 7365 203d 2042 5344 2d33  .license = BSD-3
+00000110: 2d43 6c61 7573 650d 0a6c 6963 656e 7365  -Clause..license
+00000120: 5f66 696c 6573 203d 204c 4943 454e 5345  _files = LICENSE
+00000130: 0d0a 7572 6c20 3d20 6874 7470 733a 2f2f  ..url = https://
+00000140: 6769 7468 7562 2e63 6f6d 2f6e 756e 6f2d  github.com/nuno-
+00000150: 616e 6472 652f 6874 7470 782d 6669 6c65  andre/httpx-file
+00000160: 2372 6561 646d 650d 0a70 726f 6a65 6374  #readme..project
+00000170: 5f75 726c 7320 3d20 0d0a 0953 6f75 7263  _urls = ...Sourc
+00000180: 6520 3d20 6874 7470 733a 2f2f 6769 7468  e = https://gith
+00000190: 7562 2e63 6f6d 2f6e 756e 6f2d 616e 6472  ub.com/nuno-andr
+000001a0: 652f 6874 7470 782d 6669 6c65 0d0a 0942  e/httpx-file...B
+000001b0: 7567 2054 7261 636b 6572 203d 2068 7474  ug Tracker = htt
+000001c0: 7073 3a2f 2f67 6974 6875 622e 636f 6d2f  ps://github.com/
+000001d0: 6e75 6e6f 2d61 6e64 7265 2f68 7474 7078  nuno-andre/httpx
+000001e0: 2d66 696c 652f 6973 7375 6573 0d0a 636c  -file/issues..cl
+000001f0: 6173 7369 6669 6572 7320 3d20 0d0a 0944  assifiers = ...D
+00000200: 6576 656c 6f70 6d65 6e74 2053 7461 7475  evelopment Statu
+00000210: 7320 3a3a 2034 202d 2042 6574 610d 0a09  s :: 4 - Beta...
+00000220: 496e 7465 6e64 6564 2041 7564 6965 6e63  Intended Audienc
+00000230: 6520 3a3a 2044 6576 656c 6f70 6572 730d  e :: Developers.
+00000240: 0a09 496e 7465 6e64 6564 2041 7564 6965  ..Intended Audie
+00000250: 6e63 6520 3a3a 2049 6e66 6f72 6d61 7469  nce :: Informati
+00000260: 6f6e 2054 6563 686e 6f6c 6f67 790d 0a09  on Technology...
+00000270: 496e 7465 6e64 6564 2041 7564 6965 6e63  Intended Audienc
+00000280: 6520 3a3a 2053 7973 7465 6d20 4164 6d69  e :: System Admi
+00000290: 6e69 7374 7261 746f 7273 0d0a 094c 6963  nistrators...Lic
+000002a0: 656e 7365 203a 3a20 4f53 4920 4170 7072  ense :: OSI Appr
+000002b0: 6f76 6564 203a 3a20 4253 4420 4c69 6365  oved :: BSD Lice
+000002c0: 6e73 650d 0a09 4e61 7475 7261 6c20 4c61  nse...Natural La
+000002d0: 6e67 7561 6765 203a 3a20 456e 676c 6973  nguage :: Englis
+000002e0: 680d 0a09 4f70 6572 6174 696e 6720 5379  h...Operating Sy
+000002f0: 7374 656d 203a 3a20 4f53 2049 6e64 6570  stem :: OS Indep
+00000300: 656e 6465 6e74 0d0a 0950 726f 6772 616d  endent...Program
+00000310: 6d69 6e67 204c 616e 6775 6167 6520 3a3a  ming Language ::
+00000320: 2050 7974 686f 6e0d 0a09 5072 6f67 7261   Python...Progra
+00000330: 6d6d 696e 6720 4c61 6e67 7561 6765 203a  mming Language :
+00000340: 3a20 5079 7468 6f6e 203a 3a20 332e 360d  : Python :: 3.6.
+00000350: 0a09 5072 6f67 7261 6d6d 696e 6720 4c61  ..Programming La
+00000360: 6e67 7561 6765 203a 3a20 5079 7468 6f6e  nguage :: Python
+00000370: 203a 3a20 332e 370d 0a09 5072 6f67 7261   :: 3.7...Progra
+00000380: 6d6d 696e 6720 4c61 6e67 7561 6765 203a  mming Language :
+00000390: 3a20 5079 7468 6f6e 203a 3a20 332e 380d  : Python :: 3.8.
+000003a0: 0a09 5072 6f67 7261 6d6d 696e 6720 4c61  ..Programming La
+000003b0: 6e67 7561 6765 203a 3a20 5079 7468 6f6e  nguage :: Python
+000003c0: 203a 3a20 332e 390d 0a09 5072 6f67 7261   :: 3.9...Progra
+000003d0: 6d6d 696e 6720 4c61 6e67 7561 6765 203a  mming Language :
+000003e0: 3a20 5079 7468 6f6e 203a 3a20 332e 3130  : Python :: 3.10
+000003f0: 0d0a 0950 726f 6772 616d 6d69 6e67 204c  ...Programming L
+00000400: 616e 6775 6167 6520 3a3a 2050 7974 686f  anguage :: Pytho
+00000410: 6e20 3a3a 2033 2e31 310d 0a09 5072 6f67  n :: 3.11...Prog
+00000420: 7261 6d6d 696e 6720 4c61 6e67 7561 6765  ramming Language
+00000430: 203a 3a20 5079 7468 6f6e 203a 3a20 332e   :: Python :: 3.
+00000440: 3132 0d0a 0954 6f70 6963 203a 3a20 536f  12...Topic :: So
+00000450: 6674 7761 7265 2044 6576 656c 6f70 6d65  ftware Developme
+00000460: 6e74 0d0a 0954 7970 696e 6720 3a3a 2054  nt...Typing :: T
+00000470: 7970 6564 0d0a 706c 6174 666f 726d 7320  yped..platforms 
+00000480: 3d20 616e 790d 0a0d 0a5b 6f70 7469 6f6e  = any....[option
+00000490: 735d 0d0a 7a69 705f 7361 6665 203d 2046  s]..zip_safe = F
+000004a0: 616c 7365 0d0a 7079 7468 6f6e 5f72 6571  alse..python_req
+000004b0: 7569 7265 7320 3d20 3e3d 2033 2e36 2e31  uires = >= 3.6.1
+000004c0: 0d0a 696e 7374 616c 6c5f 7265 7175 6972  ..install_requir
+000004d0: 6573 203d 200d 0a09 6874 7470 7820 3e3d  es = ...httpx >=
+000004e0: 2030 2e32 300d 0a09 6169 6f66 696c 6573   0.20...aiofiles
+000004f0: 0d0a 7061 636b 6167 6573 203d 2066 696e  ..packages = fin
+00000500: 643a 0d0a 696e 636c 7564 655f 7061 636b  d:..include_pack
+00000510: 6167 655f 6461 7461 203d 2054 7275 650d  age_data = True.
+00000520: 0a0d 0a5b 6f70 7469 6f6e 732e 7061 636b  ...[options.pack
+00000530: 6167 655f 6461 7461 5d0d 0a68 7474 7078  age_data]..httpx
+00000540: 5f66 696c 6520 3d20 0d0a 0970 792e 7479  _file = ...py.ty
+00000550: 7065 640d 0a0d 0a5b 6f70 7469 6f6e 732e  ped....[options.
+00000560: 6578 7472 6173 5f72 6571 7569 7265 5d0d  extras_require].
+00000570: 0a64 6576 203d 200d 0a09 666c 616b 6538  .dev = ...flake8
+00000580: 0d0a 0970 7974 6573 740d 0a09 7079 7465  ...pytest...pyte
+00000590: 7374 2d61 7379 6e63 696f 0d0a 0974 7970  st-asyncio...typ
+000005a0: 6573 2d61 696f 6669 6c65 730d 0a0d 0a5b  es-aiofiles....[
+000005b0: 666c 616b 6538 5d0d 0a6d 6178 2d6c 696e  flake8]..max-lin
+000005c0: 652d 6c65 6e67 7468 203d 2038 300d 0a69  e-length = 80..i
+000005d0: 676e 6f72 6520 3d20 4532 3431 2c20 4534  gnore = E241, E4
+000005e0: 3032 0d0a 0d0a 5b65 6767 5f69 6e66 6f5d  02....[egg_info]
+000005f0: 0d0a 7461 675f 6275 696c 6420 3d20 0d0a  ..tag_build = ..
+00000600: 7461 675f 6461 7465 203d 2030 0d0a 0d0a  tag_date = 0....
```

