# Comparing `tmp/yagrc-1.1.1.tar.gz` & `tmp/yagrc-1.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "yagrc-1.1.1.tar", last modified: Sun Nov  7 02:44:03 2021, max compression
+gzip compressed data, was "yagrc-1.1.2.tar", last modified: Sun Jul 23 00:58:35 2023, max compression
```

## Comparing `yagrc-1.1.1.tar` & `yagrc-1.1.2.tar`

### file list

```diff
@@ -1,49 +1,49 @@
-drwxrwxrwx   0        0        0        0 2021-11-07 02:44:03.947640 yagrc-1.1.1/
--rw-rw-rw-   0        0        0    11357 2021-02-11 00:14:48.000000 yagrc-1.1.1/LICENSE
--rw-rw-rw-   0        0        0     8585 2021-11-07 02:44:03.948617 yagrc-1.1.1/PKG-INFO
--rw-rw-rw-   0        0        0     7764 2021-02-14 22:44:31.000000 yagrc-1.1.1/README.md
-drwxrwxrwx   0        0        0        0 2021-11-07 02:44:03.861949 yagrc-1.1.1/examples/
--rw-rw-rw-   0        0        0      669 2021-02-14 21:59:29.000000 yagrc-1.1.1/examples/importer_client.py
--rw-rw-rw-   0        0        0      638 2021-02-14 22:00:31.000000 yagrc-1.1.1/examples/lazy_client.py
--rw-rw-rw-   0        0        0      705 2021-02-14 22:01:17.000000 yagrc-1.1.1/examples/reflector_client.py
-drwxrwxrwx   0        0        0        0 2021-11-07 02:44:03.866830 yagrc-1.1.1/examples/service/
-drwxrwxrwx   0        0        0        0 2021-11-07 02:44:03.873666 yagrc-1.1.1/examples/service/arithmetic/
--rw-rw-rw-   0        0        0      657 2021-02-11 19:08:48.000000 yagrc-1.1.1/examples/service/arithmetic/subtract.proto
--rw-rw-rw-   0        0        0     4008 2021-02-11 19:15:19.000000 yagrc-1.1.1/examples/service/arithmetic/subtract_pb2.py
--rw-rw-rw-   0        0        0     2484 2021-02-11 19:15:19.000000 yagrc-1.1.1/examples/service/arithmetic/subtract_pb2_grpc.py
--rw-rw-rw-   0        0        0      546 2021-02-11 19:46:09.000000 yagrc-1.1.1/examples/service/subtract_client.py
--rw-rw-rw-   0        0        0     1242 2021-02-11 19:51:06.000000 yagrc-1.1.1/examples/service/subtract_server.py
--rw-rw-rw-   0        0        0      345 2021-11-06 17:44:58.000000 yagrc-1.1.1/pyproject.toml
--rw-rw-rw-   0        0        0      847 2021-11-07 02:44:03.950569 yagrc-1.1.1/setup.cfg
--rw-rw-rw-   0        0        0       38 2021-02-07 23:16:13.000000 yagrc-1.1.1/setup.py
-drwxrwxrwx   0        0        0        0 2021-11-07 02:44:03.847304 yagrc-1.1.1/src/
-drwxrwxrwx   0        0        0        0 2021-11-07 02:44:03.877570 yagrc-1.1.1/src/yagrc/
--rw-rw-rw-   0        0        0      775 2021-02-11 23:38:35.000000 yagrc-1.1.1/src/yagrc/dump.py
--rw-rw-rw-   0        0        0    13076 2021-11-06 18:29:01.000000 yagrc-1.1.1/src/yagrc/importer.py
--rw-rw-rw-   0        0        0    10620 2021-11-06 19:28:31.000000 yagrc-1.1.1/src/yagrc/reflector.py
-drwxrwxrwx   0        0        0        0 2021-11-07 02:44:03.917375 yagrc-1.1.1/src/yagrc.egg-info/
--rw-rw-rw-   0        0        0     8585 2021-11-07 02:44:03.000000 yagrc-1.1.1/src/yagrc.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1174 2021-11-07 02:44:03.000000 yagrc-1.1.1/src/yagrc.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2021-11-07 02:44:03.000000 yagrc-1.1.1/src/yagrc.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       83 2021-11-07 02:44:03.000000 yagrc-1.1.1/src/yagrc.egg-info/requires.txt
--rw-rw-rw-   0        0        0        6 2021-11-07 02:44:03.000000 yagrc-1.1.1/src/yagrc.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2021-11-07 02:44:03.928113 yagrc-1.1.1/tests/
--rw-rw-rw-   0        0        0     4243 2021-11-06 19:26:38.000000 yagrc-1.1.1/tests/conftest.py
-drwxrwxrwx   0        0        0        0 2021-11-07 02:44:03.933973 yagrc-1.1.1/tests/service/
-drwxrwxrwx   0        0        0        0 2021-11-07 02:44:03.945687 yagrc-1.1.1/tests/service/Testing_protos/
--rw-rw-rw-   0        0        0      288 2021-02-09 00:05:47.000000 yagrc-1.1.1/tests/service/Testing_protos/AddAltTypes.proto
--rw-rw-rw-   0        0        0     3169 2021-02-08 23:36:32.000000 yagrc-1.1.1/tests/service/Testing_protos/AddAltTypes_pb2.py
--rw-rw-rw-   0        0        0      159 2021-02-08 23:36:32.000000 yagrc-1.1.1/tests/service/Testing_protos/AddAltTypes_pb2_grpc.py
--rw-rw-rw-   0        0        0      722 2021-02-09 00:05:32.000000 yagrc-1.1.1/tests/service/Testing_protos/AddTypes.proto
--rw-rw-rw-   0        0        0    15504 2021-02-08 23:36:34.000000 yagrc-1.1.1/tests/service/Testing_protos/AddTypes_pb2.py
--rw-rw-rw-   0        0        0      159 2021-02-08 23:36:34.000000 yagrc-1.1.1/tests/service/Testing_protos/AddTypes_pb2_grpc.py
--rw-rw-rw-   0        0        0     1129 2021-02-09 00:17:40.000000 yagrc-1.1.1/tests/service/Testing_protos/Add_One.proto
--rw-rw-rw-   0        0        0     3725 2021-02-08 23:52:28.000000 yagrc-1.1.1/tests/service/Testing_protos/Add_One_pb2.py
--rw-rw-rw-   0        0        0     8757 2021-02-08 23:52:28.000000 yagrc-1.1.1/tests/service/Testing_protos/Add_One_pb2_grpc.py
--rw-rw-rw-   0        0        0     1158 2021-02-11 00:32:09.000000 yagrc-1.1.1/tests/service/addone_client.py
--rw-rw-rw-   0        0        0     2575 2021-02-11 00:27:34.000000 yagrc-1.1.1/tests/service/addone_server.py
--rw-rw-rw-   0        0        0      184 2021-02-11 20:17:01.000000 yagrc-1.1.1/tests/test_dump.py
--rw-rw-rw-   0        0        0     4191 2021-02-14 22:27:49.000000 yagrc-1.1.1/tests/test_importer.py
--rw-rw-rw-   0        0        0     2961 2021-11-06 18:28:49.000000 yagrc-1.1.1/tests/test_lazy.py
--rw-rw-rw-   0        0        0     2885 2021-02-11 23:15:35.000000 yagrc-1.1.1/tests/test_null.py
--rw-rw-rw-   0        0        0     3822 2021-02-14 22:26:20.000000 yagrc-1.1.1/tests/test_reflector.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:58:35.519011 yagrc-1.1.2/
+-rw-rw-rw-   0        0        0    11357 2021-02-11 00:14:48.000000 yagrc-1.1.2/LICENSE
+-rw-rw-rw-   0        0        0     8562 2023-07-23 00:58:35.519011 yagrc-1.1.2/PKG-INFO
+-rw-rw-rw-   0        0        0     7764 2021-02-14 22:44:31.000000 yagrc-1.1.2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 00:58:35.487764 yagrc-1.1.2/examples/
+-rw-rw-rw-   0        0        0      669 2021-02-14 21:59:29.000000 yagrc-1.1.2/examples/importer_client.py
+-rw-rw-rw-   0        0        0      638 2021-02-14 22:00:31.000000 yagrc-1.1.2/examples/lazy_client.py
+-rw-rw-rw-   0        0        0      705 2021-02-14 22:01:17.000000 yagrc-1.1.2/examples/reflector_client.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:58:35.487764 yagrc-1.1.2/examples/service/
+drwxrwxrwx   0        0        0        0 2023-07-23 00:58:35.487764 yagrc-1.1.2/examples/service/arithmetic/
+-rw-rw-rw-   0        0        0      657 2021-02-11 19:08:48.000000 yagrc-1.1.2/examples/service/arithmetic/subtract.proto
+-rw-rw-rw-   0        0        0     1375 2023-07-08 21:53:58.000000 yagrc-1.1.2/examples/service/arithmetic/subtract_pb2.py
+-rw-rw-rw-   0        0        0     2484 2023-07-08 21:53:58.000000 yagrc-1.1.2/examples/service/arithmetic/subtract_pb2_grpc.py
+-rw-rw-rw-   0        0        0      546 2021-02-11 19:46:09.000000 yagrc-1.1.2/examples/service/subtract_client.py
+-rw-rw-rw-   0        0        0     1242 2021-02-11 19:51:06.000000 yagrc-1.1.2/examples/service/subtract_server.py
+-rw-rw-rw-   0        0        0      345 2021-11-06 17:44:58.000000 yagrc-1.1.2/pyproject.toml
+-rw-rw-rw-   0        0        0      848 2023-07-23 00:58:35.519011 yagrc-1.1.2/setup.cfg
+-rw-rw-rw-   0        0        0       38 2021-02-07 23:16:13.000000 yagrc-1.1.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:58:35.487764 yagrc-1.1.2/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 00:58:35.487764 yagrc-1.1.2/src/yagrc/
+-rw-rw-rw-   0        0        0      793 2021-12-07 16:43:11.000000 yagrc-1.1.2/src/yagrc/dump.py
+-rw-rw-rw-   0        0        0    13076 2021-11-06 18:29:01.000000 yagrc-1.1.2/src/yagrc/importer.py
+-rw-rw-rw-   0        0        0    10559 2023-07-23 00:34:01.000000 yagrc-1.1.2/src/yagrc/reflector.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:58:35.503385 yagrc-1.1.2/src/yagrc.egg-info/
+-rw-rw-rw-   0        0        0     8562 2023-07-23 00:58:35.000000 yagrc-1.1.2/src/yagrc.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1174 2023-07-23 00:58:35.000000 yagrc-1.1.2/src/yagrc.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 00:58:35.000000 yagrc-1.1.2/src/yagrc.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       84 2023-07-23 00:58:35.000000 yagrc-1.1.2/src/yagrc.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        6 2023-07-23 00:58:35.000000 yagrc-1.1.2/src/yagrc.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 00:58:35.519011 yagrc-1.1.2/tests/
+-rw-rw-rw-   0        0        0     4066 2023-07-13 20:48:46.000000 yagrc-1.1.2/tests/conftest.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:58:35.519011 yagrc-1.1.2/tests/service/
+drwxrwxrwx   0        0        0        0 2023-07-23 00:58:35.519011 yagrc-1.1.2/tests/service/Testing_protos/
+-rw-rw-rw-   0        0        0      288 2021-02-09 00:05:47.000000 yagrc-1.1.2/tests/service/Testing_protos/AddAltTypes.proto
+-rw-rw-rw-   0        0        0     1186 2023-07-08 21:51:26.000000 yagrc-1.1.2/tests/service/Testing_protos/AddAltTypes_pb2.py
+-rw-rw-rw-   0        0        0      159 2023-07-08 21:51:26.000000 yagrc-1.1.2/tests/service/Testing_protos/AddAltTypes_pb2_grpc.py
+-rw-rw-rw-   0        0        0      722 2022-10-08 21:16:55.000000 yagrc-1.1.2/tests/service/Testing_protos/AddTypes.proto
+-rw-rw-rw-   0        0        0     3158 2023-07-08 21:51:19.000000 yagrc-1.1.2/tests/service/Testing_protos/AddTypes_pb2.py
+-rw-rw-rw-   0        0        0      159 2023-07-08 21:51:19.000000 yagrc-1.1.2/tests/service/Testing_protos/AddTypes_pb2_grpc.py
+-rw-rw-rw-   0        0        0     1129 2021-02-09 00:17:40.000000 yagrc-1.1.2/tests/service/Testing_protos/Add_One.proto
+-rw-rw-rw-   0        0        0     1755 2023-07-08 21:50:07.000000 yagrc-1.1.2/tests/service/Testing_protos/Add_One_pb2.py
+-rw-rw-rw-   0        0        0     8757 2023-07-08 21:50:07.000000 yagrc-1.1.2/tests/service/Testing_protos/Add_One_pb2_grpc.py
+-rw-rw-rw-   0        0        0     1158 2021-02-11 00:32:09.000000 yagrc-1.1.2/tests/service/addone_client.py
+-rw-rw-rw-   0        0        0     2575 2021-02-11 00:27:34.000000 yagrc-1.1.2/tests/service/addone_server.py
+-rw-rw-rw-   0        0        0      184 2021-02-11 20:17:01.000000 yagrc-1.1.2/tests/test_dump.py
+-rw-rw-rw-   0        0        0     4191 2021-02-14 22:27:49.000000 yagrc-1.1.2/tests/test_importer.py
+-rw-rw-rw-   0        0        0     2961 2021-11-06 18:28:49.000000 yagrc-1.1.2/tests/test_lazy.py
+-rw-rw-rw-   0        0        0     2885 2021-02-11 23:15:35.000000 yagrc-1.1.2/tests/test_null.py
+-rw-rw-rw-   0        0        0     3853 2023-07-13 20:49:57.000000 yagrc-1.1.2/tests/test_reflector.py
```

### Comparing `yagrc-1.1.1/LICENSE` & `yagrc-1.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/PKG-INFO` & `yagrc-1.1.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,22 +1,21 @@
 Metadata-Version: 2.1
 Name: yagrc
-Version: 1.1.1
+Version: 1.1.2
 Summary: Yet another gRPC reflection client
 Home-page: https://github.com/sparky8512/yagrc
 Author-email: sparky8512-py@yahoo.com
 License: Apache License 2.0
-Platform: UNKNOWN
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Requires-Python: >=3.5
+Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 Provides-Extra: test
 License-File: LICENSE
 
 # Yet Another gRPC Reflection Client
 
 A minimalist [gRPC](https://grpc.io/) reflection client for Python. Reflected grpc type classes can be used either by getting them by the names defined in their proto files, or by importing the same modules you would when using protoc to [generate them](https://grpc.io/docs/languages/python/generated-code/).
@@ -161,9 +160,7 @@
 ## Similar projects
 
 [grpc requests](https://github.com/spaceone-dev/grpc_requests) is a Python grpc client that supports reflection, but it exposes a different type class interface than the protoc-generated ones (as far as I can tell...).
 
 [Eagr](https://github.com/kensho-technologies/eagr) includes a Python grpc reflection client interface, but it's a small part of a much larger project, most of which is unrelated to reflection.
 
 There's lots of reflection clients for other languages, too, and probably others for Python. [gRPCurl](https://github.com/fullstorydev/grpcurl), in particular, is useful if you want to examine reflected service protocols interactively.
-
-
```

### Comparing `yagrc-1.1.1/README.md` & `yagrc-1.1.2/README.md`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/examples/importer_client.py` & `yagrc-1.1.2/examples/importer_client.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/examples/lazy_client.py` & `yagrc-1.1.2/examples/lazy_client.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/examples/reflector_client.py` & `yagrc-1.1.2/examples/reflector_client.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/examples/service/arithmetic/subtract.proto` & `yagrc-1.1.2/examples/service/arithmetic/subtract.proto`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/examples/service/arithmetic/subtract_pb2_grpc.py` & `yagrc-1.1.2/examples/service/arithmetic/subtract_pb2_grpc.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/examples/service/subtract_client.py` & `yagrc-1.1.2/examples/service/subtract_client.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/examples/service/subtract_server.py` & `yagrc-1.1.2/examples/service/subtract_server.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/setup.cfg` & `yagrc-1.1.2/setup.cfg`

 * *Files 14% similar despite different names*

```diff
@@ -33,21 +33,21 @@
 00000200: 7469 6f6e 5f63 6f6e 7465 6e74 5f74 7970  tion_content_typ
 00000210: 6520 3d20 7465 7874 2f6d 6172 6b64 6f77  e = text/markdow
 00000220: 6e0d 0a0d 0a5b 6f70 7469 6f6e 735d 0d0a  n....[options]..
 00000230: 696e 7374 616c 6c5f 7265 7175 6972 6573  install_requires
 00000240: 203d 200d 0a09 6772 7063 696f 3e3d 312e   = ...grpcio>=1.
 00000250: 3132 2e30 0d0a 0967 7270 6369 6f5f 7265  12.0...grpcio_re
 00000260: 666c 6563 7469 6f6e 3e3d 312e 372e 330d  flection>=1.7.3.
-00000270: 0a09 7072 6f74 6f62 7566 3e3d 332e 342e  ..protobuf>=3.4.
-00000280: 300d 0a70 6163 6b61 6765 7320 3d20 0d0a  0..packages = ..
-00000290: 0979 6167 7263 0d0a 7061 636b 6167 655f  .yagrc..package_
-000002a0: 6469 7220 3d20 0d0a 093d 7372 630d 0a70  dir = ...=src..p
-000002b0: 7974 686f 6e5f 7265 7175 6972 6573 203d  ython_requires =
-000002c0: 203e 3d33 2e35 0d0a 0d0a 5b6f 7074 696f   >=3.5....[optio
-000002d0: 6e73 2e65 7874 7261 735f 7265 7175 6972  ns.extras_requir
-000002e0: 655d 0d0a 7465 7374 203d 2070 7974 6573  e]..test = pytes
-000002f0: 743b 2070 7974 6573 742d 6772 7063 0d0a  t; pytest-grpc..
-00000300: 0d0a 5b79 6170 665d 0d0a 6261 7365 645f  ..[yapf]..based_
-00000310: 6f6e 5f73 7479 6c65 203d 2067 6f6f 676c  on_style = googl
-00000320: 650d 0a0d 0a5b 6567 675f 696e 666f 5d0d  e....[egg_info].
-00000330: 0a74 6167 5f62 7569 6c64 203d 200d 0a74  .tag_build = ..t
-00000340: 6167 5f64 6174 6520 3d20 300d 0a0d 0a    ag_date = 0....
+00000270: 0a09 7072 6f74 6f62 7566 3e3d 342e 3232  ..protobuf>=4.22
+00000280: 2e30 0d0a 7061 636b 6167 6573 203d 200d  .0..packages = .
+00000290: 0a09 7961 6772 630d 0a70 6163 6b61 6765  ..yagrc..package
+000002a0: 5f64 6972 203d 200d 0a09 3d73 7263 0d0a  _dir = ...=src..
+000002b0: 7079 7468 6f6e 5f72 6571 7569 7265 7320  python_requires 
+000002c0: 3d20 3e3d 332e 370d 0a0d 0a5b 6f70 7469  = >=3.7....[opti
+000002d0: 6f6e 732e 6578 7472 6173 5f72 6571 7569  ons.extras_requi
+000002e0: 7265 5d0d 0a74 6573 7420 3d20 7079 7465  re]..test = pyte
+000002f0: 7374 3b20 7079 7465 7374 2d67 7270 630d  st; pytest-grpc.
+00000300: 0a0d 0a5b 7961 7066 5d0d 0a62 6173 6564  ...[yapf]..based
+00000310: 5f6f 6e5f 7374 796c 6520 3d20 676f 6f67  _on_style = goog
+00000320: 6c65 0d0a 0d0a 5b65 6767 5f69 6e66 6f5d  le....[egg_info]
+00000330: 0d0a 7461 675f 6275 696c 6420 3d20 0d0a  ..tag_build = ..
+00000340: 7461 675f 6461 7465 203d 2030 0d0a 0d0a  tag_date = 0....
```

### Comparing `yagrc-1.1.1/src/yagrc/dump.py` & `yagrc-1.1.2/src/yagrc/dump.py`

 * *Files 10% similar despite different names*

```diff
@@ -3,15 +3,16 @@
 
 from yagrc import reflector
 
 
 def dump_protocols(channel, filenames=None, symbols=None):
     """Get serialized FileDescriptorSet message via reflection.
 
-    See `yagrc.reflector.GrpcReflectionClient.load_protocols` for arg details.
+    See `yagrc.reflector.GrpcReflectionClient.load_protocols` for arg and
+    exception details.
     """
     fdset = descriptor_pb2.FileDescriptorSet()
     grpc_reflector = reflector.GrpcReflectionEngine()
     for filename in grpc_reflector.load_protocols(channel, filenames, symbols):
         proto = descriptor_pb2.FileDescriptorProto()
         descr = grpc_reflector.file_descriptor(filename)
         descr.CopyToProto(proto)
```

### Comparing `yagrc-1.1.1/src/yagrc/importer.py` & `yagrc-1.1.2/src/yagrc/importer.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/src/yagrc/reflector.py` & `yagrc-1.1.2/src/yagrc/reflector.py`

 * *Files 1% similar despite different names*

```diff
@@ -78,15 +78,14 @@
     This class is not meant to be used directly. Instead, use
     `GrpcReflectionClient` or `yagrc.importer.GrpcImporter`
     """
 
     def __init__(self):
         self.methods_by_file = {}
         self.pool = descriptor_pool.DescriptorPool()
-        self._factory = message_factory.MessageFactory(self.pool)
 
     def load_protocols(self, channel, filenames=None, symbols=None):
         """Implementation of `GrpcReflectionClient.load_protocols`"""
         stub = reflection_pb2_grpc.ServerReflectionStub(channel)
 
         requests = []
         if filenames:
@@ -165,15 +164,15 @@
 
     def message_from_descr(self, proto):
         """Get message class from message descriptor.
 
         Args:
             proto (google.protobuf.descriptor.Descriptor): Message descriptor.
         """
-        return self._factory.GetPrototype(proto)
+        return message_factory.GetMessageClass(proto)
 
     def gen_stub_class(self, service, method_protos):
         """Get service stub class from service descriptor.
 
         Args:
             service (google.protobuf.descriptor.ServiceDescriptor): Service
                 descriptor.
```

### Comparing `yagrc-1.1.1/src/yagrc.egg-info/PKG-INFO` & `yagrc-1.1.2/src/yagrc.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,22 +1,21 @@
 Metadata-Version: 2.1
 Name: yagrc
-Version: 1.1.1
+Version: 1.1.2
 Summary: Yet another gRPC reflection client
 Home-page: https://github.com/sparky8512/yagrc
 Author-email: sparky8512-py@yahoo.com
 License: Apache License 2.0
-Platform: UNKNOWN
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Requires-Python: >=3.5
+Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 Provides-Extra: test
 License-File: LICENSE
 
 # Yet Another gRPC Reflection Client
 
 A minimalist [gRPC](https://grpc.io/) reflection client for Python. Reflected grpc type classes can be used either by getting them by the names defined in their proto files, or by importing the same modules you would when using protoc to [generate them](https://grpc.io/docs/languages/python/generated-code/).
@@ -161,9 +160,7 @@
 ## Similar projects
 
 [grpc requests](https://github.com/spaceone-dev/grpc_requests) is a Python grpc client that supports reflection, but it exposes a different type class interface than the protoc-generated ones (as far as I can tell...).
 
 [Eagr](https://github.com/kensho-technologies/eagr) includes a Python grpc reflection client interface, but it's a small part of a much larger project, most of which is unrelated to reflection.
 
 There's lots of reflection clients for other languages, too, and probably others for Python. [gRPCurl](https://github.com/fullstorydev/grpcurl), in particular, is useful if you want to examine reflected service protocols interactively.
-
-
```

### Comparing `yagrc-1.1.1/src/yagrc.egg-info/SOURCES.txt` & `yagrc-1.1.2/src/yagrc.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/tests/conftest.py` & `yagrc-1.1.2/tests/conftest.py`

 * *Files 8% similar despite different names*

```diff
@@ -98,15 +98,13 @@
 
 # And another to simulate an unsatisfied dependency
 @pytest.fixture
 def force_unsatisfied_dep(monkeypatch):
     real_method = reflection.BaseReflectionServicer._file_by_filename
 
     def mock_file_by_filename(self, filename):
-        # it'd be awkward to just remove the response given how the service is
-        # written, so just return a duplicate copy of AddTypes.proto
-        if filename == "Testing_protos/AddAltTypes.proto":
-            return real_method(self, "Testing_protos/AddTypes.proto")
-        return real_method(self, filename)
+        response = real_method(self, filename)
+        del response.file_descriptor_response.file_descriptor_proto[-1]
+        return response
 
     monkeypatch.setattr(reflection.BaseReflectionServicer, "_file_by_filename",
                         mock_file_by_filename)
```

### Comparing `yagrc-1.1.1/tests/service/Testing_protos/AddTypes.proto` & `yagrc-1.1.2/tests/service/Testing_protos/AddTypes.proto`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/tests/service/Testing_protos/Add_One.proto` & `yagrc-1.1.2/tests/service/Testing_protos/Add_One.proto`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/tests/service/Testing_protos/Add_One_pb2_grpc.py` & `yagrc-1.1.2/tests/service/Testing_protos/Add_One_pb2_grpc.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/tests/service/addone_client.py` & `yagrc-1.1.2/tests/service/addone_client.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/tests/service/addone_server.py` & `yagrc-1.1.2/tests/service/addone_server.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/tests/test_importer.py` & `yagrc-1.1.2/tests/test_importer.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/tests/test_lazy.py` & `yagrc-1.1.2/tests/test_lazy.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/tests/test_null.py` & `yagrc-1.1.2/tests/test_null.py`

 * *Files identical despite different names*

### Comparing `yagrc-1.1.1/tests/test_reflector.py` & `yagrc-1.1.2/tests/test_reflector.py`

 * *Files 2% similar despite different names*

```diff
@@ -91,15 +91,16 @@
     reflector = yagrc_reflector.GrpcReflectionClient()
     reflector.load_protocols(grpc_channel)
 
 
 @pytest.mark.xfail(raises=KeyError, strict=True)
 def test_unsatisfied_dep(grpc_channel, force_unsatisfied_dep):
     reflector = yagrc_reflector.GrpcReflectionClient()
-    reflector.load_protocols(grpc_channel, symbols=["Testing.Addition"])
+    reflector.load_protocols(grpc_channel, filenames=["Testing_protos/Add_One.proto"])
+    assert False
 
 
 @pytest.mark.xfail(raises=yagrc_reflector.ServiceError, strict=True)
 def test_bad_proto(grpc_channel):
     reflector = yagrc_reflector.GrpcReflectionClient()
     reflector.load_protocols(grpc_channel, symbols=["Testing.Subtraction"])
     assert False
```

