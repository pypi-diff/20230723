# Comparing `tmp/telnetlib3-2.0.3.tar.gz` & `tmp/telnetlib3-2.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "telnetlib3-2.0.3.tar", last modified: Sat Jul  8 15:08:13 2023, max compression
+gzip compressed data, was "telnetlib3-2.0.4.tar", last modified: Sun Jul 23 16:06:54 2023, max compression
```

## Comparing `telnetlib3-2.0.3.tar` & `telnetlib3-2.0.4.tar`

### file list

```diff
@@ -1,40 +1,40 @@
-drwxr-xr-x   0 jq         (501) staff       (20)        0 2023-07-08 15:08:13.956769 telnetlib3-2.0.3/
--rw-r--r--   0 jq         (501) staff       (20)      169 2020-07-03 00:14:03.000000 telnetlib3-2.0.3/.coveragerc
--rw-r--r--   0 jq         (501) staff       (20)     2343 2020-07-03 00:14:03.000000 telnetlib3-2.0.3/LICENSE.txt
--rw-r--r--   0 jq         (501) staff       (20)       38 2020-07-03 00:14:03.000000 telnetlib3-2.0.3/MANIFEST.in
--rw-r--r--   0 jq         (501) staff       (20)     7064 2023-07-08 15:08:13.956638 telnetlib3-2.0.3/PKG-INFO
--rw-r--r--   0 jq         (501) staff       (20)     6146 2023-03-28 16:48:37.000000 telnetlib3-2.0.3/README.rst
-drwxr-xr-x   0 jq         (501) staff       (20)        0 2023-07-08 15:08:13.952051 telnetlib3-2.0.3/docs/
--rw-r--r--   0 jq         (501) staff       (20)       58 2020-07-03 00:14:03.000000 telnetlib3-2.0.3/docs/api.rst
--rw-r--r--   0 jq         (501) staff       (20)     2058 2023-03-28 22:26:35.000000 telnetlib3-2.0.3/docs/contributing.rst
--rw-r--r--   0 jq         (501) staff       (20)     3711 2023-07-08 15:06:29.000000 telnetlib3-2.0.3/docs/history.rst
--rw-r--r--   0 jq         (501) staff       (20)      259 2020-07-03 00:14:03.000000 telnetlib3-2.0.3/docs/index.rst
--rw-r--r--   0 jq         (501) staff       (20)     6146 2023-03-28 16:48:37.000000 telnetlib3-2.0.3/docs/intro.rst
--rw-r--r--   0 jq         (501) staff       (20)     6729 2020-07-03 00:14:03.000000 telnetlib3-2.0.3/docs/rfcs.rst
--rw-r--r--   0 jq         (501) staff       (20)       49 2022-11-28 21:50:53.000000 telnetlib3-2.0.3/requirements-analysis.txt
--rw-r--r--   0 jq         (501) staff       (20)       86 2022-11-28 22:32:25.000000 telnetlib3-2.0.3/requirements-docs.txt
--rw-r--r--   0 jq         (501) staff       (20)       84 2023-03-28 22:26:35.000000 telnetlib3-2.0.3/requirements-tests.txt
--rw-r--r--   0 jq         (501) staff       (20)      179 2022-11-29 16:16:26.000000 telnetlib3-2.0.3/requirements.txt
--rw-r--r--   0 jq         (501) staff       (20)       38 2023-07-08 15:08:13.956805 telnetlib3-2.0.3/setup.cfg
--rw-r--r--   0 jq         (501) staff       (20)     1943 2023-07-08 15:06:42.000000 telnetlib3-2.0.3/setup.py
-drwxr-xr-x   0 jq         (501) staff       (20)        0 2023-07-08 15:08:13.955595 telnetlib3-2.0.3/telnetlib3/
--rw-r--r--   0 jq         (501) staff       (20)      990 2023-03-28 22:26:35.000000 telnetlib3-2.0.3/telnetlib3/__init__.py
--rw-r--r--   0 jq         (501) staff       (20)     2756 2023-03-28 22:26:35.000000 telnetlib3-2.0.3/telnetlib3/accessories.py
--rwxr-xr-x   0 jq         (501) staff       (20)    16453 2023-07-08 15:03:26.000000 telnetlib3-2.0.3/telnetlib3/client.py
--rw-r--r--   0 jq         (501) staff       (20)    12293 2023-03-20 18:26:59.000000 telnetlib3-2.0.3/telnetlib3/client_base.py
--rw-r--r--   0 jq         (501) staff       (20)     9360 2023-03-20 18:26:17.000000 telnetlib3-2.0.3/telnetlib3/client_shell.py
--rw-r--r--   0 jq         (501) staff       (20)     3091 2022-11-28 21:50:53.000000 telnetlib3-2.0.3/telnetlib3/relay_server.py
--rwxr-xr-x   0 jq         (501) staff       (20)    22716 2023-03-28 22:26:35.000000 telnetlib3-2.0.3/telnetlib3/server.py
--rw-r--r--   0 jq         (501) staff       (20)    11981 2023-03-28 22:26:35.000000 telnetlib3-2.0.3/telnetlib3/server_base.py
--rw-r--r--   0 jq         (501) staff       (20)     6625 2023-03-28 22:26:35.000000 telnetlib3-2.0.3/telnetlib3/server_shell.py
--rw-r--r--   0 jq         (501) staff       (20)    14974 2023-07-08 15:04:07.000000 telnetlib3-2.0.3/telnetlib3/slc.py
--rw-r--r--   0 jq         (501) staff       (20)    21202 2023-07-08 15:04:04.000000 telnetlib3-2.0.3/telnetlib3/stream_reader.py
--rw-r--r--   0 jq         (501) staff       (20)   103507 2023-03-31 17:48:21.000000 telnetlib3-2.0.3/telnetlib3/stream_writer.py
--rw-r--r--   0 jq         (501) staff       (20)     5348 2023-03-28 16:48:37.000000 telnetlib3-2.0.3/telnetlib3/telopt.py
-drwxr-xr-x   0 jq         (501) staff       (20)        0 2023-07-08 15:08:13.956373 telnetlib3-2.0.3/telnetlib3.egg-info/
--rw-r--r--   0 jq         (501) staff       (20)     7064 2023-07-08 15:08:13.000000 telnetlib3-2.0.3/telnetlib3.egg-info/PKG-INFO
--rw-r--r--   0 jq         (501) staff       (20)      760 2023-07-08 15:08:13.000000 telnetlib3-2.0.3/telnetlib3.egg-info/SOURCES.txt
--rw-r--r--   0 jq         (501) staff       (20)        1 2023-07-08 15:08:13.000000 telnetlib3-2.0.3/telnetlib3.egg-info/dependency_links.txt
--rw-r--r--   0 jq         (501) staff       (20)      104 2023-07-08 15:08:13.000000 telnetlib3-2.0.3/telnetlib3.egg-info/entry_points.txt
--rw-r--r--   0 jq         (501) staff       (20)       11 2023-07-08 15:08:13.000000 telnetlib3-2.0.3/telnetlib3.egg-info/top_level.txt
--rw-r--r--   0 jq         (501) staff       (20)        1 2020-07-03 00:14:32.000000 telnetlib3-2.0.3/telnetlib3.egg-info/zip-safe
+drwxr-xr-x   0 jq         (501) staff       (20)        0 2023-07-23 16:06:54.629361 telnetlib3-2.0.4/
+-rw-r--r--   0 jq         (501) staff       (20)      169 2020-07-03 00:14:03.000000 telnetlib3-2.0.4/.coveragerc
+-rw-r--r--   0 jq         (501) staff       (20)     2343 2020-07-03 00:14:03.000000 telnetlib3-2.0.4/LICENSE.txt
+-rw-r--r--   0 jq         (501) staff       (20)       38 2020-07-03 00:14:03.000000 telnetlib3-2.0.4/MANIFEST.in
+-rw-r--r--   0 jq         (501) staff       (20)     7064 2023-07-23 16:06:54.629202 telnetlib3-2.0.4/PKG-INFO
+-rw-r--r--   0 jq         (501) staff       (20)     6146 2023-03-28 16:48:37.000000 telnetlib3-2.0.4/README.rst
+drwxr-xr-x   0 jq         (501) staff       (20)        0 2023-07-23 16:06:54.610626 telnetlib3-2.0.4/docs/
+-rw-r--r--   0 jq         (501) staff       (20)       58 2020-07-03 00:14:03.000000 telnetlib3-2.0.4/docs/api.rst
+-rw-r--r--   0 jq         (501) staff       (20)     2058 2023-03-28 22:26:35.000000 telnetlib3-2.0.4/docs/contributing.rst
+-rw-r--r--   0 jq         (501) staff       (20)     3796 2023-07-23 16:02:36.000000 telnetlib3-2.0.4/docs/history.rst
+-rw-r--r--   0 jq         (501) staff       (20)      259 2020-07-03 00:14:03.000000 telnetlib3-2.0.4/docs/index.rst
+-rw-r--r--   0 jq         (501) staff       (20)     6146 2023-03-28 16:48:37.000000 telnetlib3-2.0.4/docs/intro.rst
+-rw-r--r--   0 jq         (501) staff       (20)     6729 2020-07-03 00:14:03.000000 telnetlib3-2.0.4/docs/rfcs.rst
+-rw-r--r--   0 jq         (501) staff       (20)       49 2022-11-28 21:50:53.000000 telnetlib3-2.0.4/requirements-analysis.txt
+-rw-r--r--   0 jq         (501) staff       (20)       86 2022-11-28 22:32:25.000000 telnetlib3-2.0.4/requirements-docs.txt
+-rw-r--r--   0 jq         (501) staff       (20)       84 2023-03-28 22:26:35.000000 telnetlib3-2.0.4/requirements-tests.txt
+-rw-r--r--   0 jq         (501) staff       (20)      179 2022-11-29 16:16:26.000000 telnetlib3-2.0.4/requirements.txt
+-rw-r--r--   0 jq         (501) staff       (20)       38 2023-07-23 16:06:54.629532 telnetlib3-2.0.4/setup.cfg
+-rw-r--r--   0 jq         (501) staff       (20)     1950 2023-07-23 16:03:52.000000 telnetlib3-2.0.4/setup.py
+drwxr-xr-x   0 jq         (501) staff       (20)        0 2023-07-23 16:06:54.625441 telnetlib3-2.0.4/telnetlib3/
+-rw-r--r--   0 jq         (501) staff       (20)      990 2023-03-28 22:26:35.000000 telnetlib3-2.0.4/telnetlib3/__init__.py
+-rw-r--r--   0 jq         (501) staff       (20)     2740 2023-07-23 16:03:47.000000 telnetlib3-2.0.4/telnetlib3/accessories.py
+-rwxr-xr-x   0 jq         (501) staff       (20)    16453 2023-07-08 15:03:26.000000 telnetlib3-2.0.4/telnetlib3/client.py
+-rw-r--r--   0 jq         (501) staff       (20)    12293 2023-03-20 18:26:59.000000 telnetlib3-2.0.4/telnetlib3/client_base.py
+-rw-r--r--   0 jq         (501) staff       (20)     9360 2023-03-20 18:26:17.000000 telnetlib3-2.0.4/telnetlib3/client_shell.py
+-rw-r--r--   0 jq         (501) staff       (20)     3091 2022-11-28 21:50:53.000000 telnetlib3-2.0.4/telnetlib3/relay_server.py
+-rwxr-xr-x   0 jq         (501) staff       (20)    22716 2023-03-28 22:26:35.000000 telnetlib3-2.0.4/telnetlib3/server.py
+-rw-r--r--   0 jq         (501) staff       (20)    11981 2023-03-28 22:26:35.000000 telnetlib3-2.0.4/telnetlib3/server_base.py
+-rw-r--r--   0 jq         (501) staff       (20)     6625 2023-03-28 22:26:35.000000 telnetlib3-2.0.4/telnetlib3/server_shell.py
+-rw-r--r--   0 jq         (501) staff       (20)    14974 2023-07-08 15:04:07.000000 telnetlib3-2.0.4/telnetlib3/slc.py
+-rw-r--r--   0 jq         (501) staff       (20)    21202 2023-07-08 15:04:04.000000 telnetlib3-2.0.4/telnetlib3/stream_reader.py
+-rw-r--r--   0 jq         (501) staff       (20)   103507 2023-03-31 17:48:21.000000 telnetlib3-2.0.4/telnetlib3/stream_writer.py
+-rw-r--r--   0 jq         (501) staff       (20)     5348 2023-03-28 16:48:37.000000 telnetlib3-2.0.4/telnetlib3/telopt.py
+drwxr-xr-x   0 jq         (501) staff       (20)        0 2023-07-23 16:06:54.628098 telnetlib3-2.0.4/telnetlib3.egg-info/
+-rw-r--r--   0 jq         (501) staff       (20)     7064 2023-07-23 16:06:54.000000 telnetlib3-2.0.4/telnetlib3.egg-info/PKG-INFO
+-rw-r--r--   0 jq         (501) staff       (20)      760 2023-07-23 16:06:54.000000 telnetlib3-2.0.4/telnetlib3.egg-info/SOURCES.txt
+-rw-r--r--   0 jq         (501) staff       (20)        1 2023-07-23 16:06:54.000000 telnetlib3-2.0.4/telnetlib3.egg-info/dependency_links.txt
+-rw-r--r--   0 jq         (501) staff       (20)      104 2023-07-23 16:06:54.000000 telnetlib3-2.0.4/telnetlib3.egg-info/entry_points.txt
+-rw-r--r--   0 jq         (501) staff       (20)       11 2023-07-23 16:06:54.000000 telnetlib3-2.0.4/telnetlib3.egg-info/top_level.txt
+-rw-r--r--   0 jq         (501) staff       (20)        1 2020-07-03 00:14:32.000000 telnetlib3-2.0.4/telnetlib3.egg-info/zip-safe
```

### Comparing `telnetlib3-2.0.3/LICENSE.txt` & `telnetlib3-2.0.4/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/PKG-INFO` & `telnetlib3-2.0.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: telnetlib3
-Version: 2.0.3
+Version: 2.0.4
 Summary: Python 3 asyncio Telnet server and client Protocol library
 Home-page: http://telnetlib3.rtfd.org/
 Author: Jeff Quast
 Author-email: contact@jeffquast.com
 License: ISC
 Keywords: telnet,server,client,bbs,mud,utf8,cp437,api,library,asyncio,talker
 Platform: any
```

### Comparing `telnetlib3-2.0.3/README.rst` & `telnetlib3-2.0.4/README.rst`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/docs/contributing.rst` & `telnetlib3-2.0.4/docs/contributing.rst`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/docs/history.rst` & `telnetlib3-2.0.4/docs/history.rst`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,14 @@
 History
 =======
+2.0.4
+ * change: stop using setuptools library to get current software version
+
 2.0.3
- * bugfix: NameError: when debug=True is with asyncio.run, :ghissue:`75`
+ * bugfix: NameError: when debug=True is used with asyncio.run, :ghissue:`75`
 
 2.0.2
  * bugfix: NameError: name 'sleep' is not defined in stream_writer.py
 
 2.0.1
  * bugfix: "write after close" is disregarded, caused many errors logged in socket.send()
  * bugfix: in accessories.repr_mapping() about using shlex.quote on non-str,
```

### Comparing `telnetlib3-2.0.3/docs/intro.rst` & `telnetlib3-2.0.4/docs/intro.rst`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/docs/rfcs.rst` & `telnetlib3-2.0.4/docs/rfcs.rst`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/setup.py` & `telnetlib3-2.0.4/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -10,16 +10,15 @@
 
 def _get_long_description(fname, encoding="utf8"):
     return open(fname, "r", encoding=encoding).read()
 
 
 setup(
     name="telnetlib3",
-    # keep in sync w/docs/conf.py manually for now, please!
-    version="2.0.3",
+    version="2.0.4",  # keep in sync with docs/conf.py and telnetlib3/accessories.py !!
     url="http://telnetlib3.rtfd.org/",
     license="ISC",
     author="Jeff Quast",
     description="Python 3 asyncio Telnet server and client Protocol library",
     long_description=_get_long_description(fname=_get_here("README.rst")),
     # requires python 3.7 and greater beginning with 2.0.0 release
     python_requires=">=3.7",
```

### Comparing `telnetlib3-2.0.3/telnetlib3/__init__.py` & `telnetlib3-2.0.4/telnetlib3/__init__.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3/accessories.py` & `telnetlib3-2.0.4/telnetlib3/accessories.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,9 @@
 """Accessory functions."""
 # std imports
-import pkg_resources
 import importlib
 import logging
 import asyncio
 import shlex
 
 __all__ = (
     "encoding_from_lang",
@@ -14,15 +13,15 @@
     "repr_mapping",
     "function_lookup",
     "make_reader_task",
 )
 
 
 def get_version():
-    return pkg_resources.get_distribution("telnetlib3").version
+    return "2.0.4"  # keep in sync with setup.py and docs/conf.py !!
 
 
 def encoding_from_lang(lang):
     """
     Parse encoding from LANG environment value.
 
     Example::
```

### Comparing `telnetlib3-2.0.3/telnetlib3/client.py` & `telnetlib3-2.0.4/telnetlib3/client.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3/client_base.py` & `telnetlib3-2.0.4/telnetlib3/client_base.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3/client_shell.py` & `telnetlib3-2.0.4/telnetlib3/client_shell.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3/relay_server.py` & `telnetlib3-2.0.4/telnetlib3/relay_server.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3/server.py` & `telnetlib3-2.0.4/telnetlib3/server.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3/server_base.py` & `telnetlib3-2.0.4/telnetlib3/server_base.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3/server_shell.py` & `telnetlib3-2.0.4/telnetlib3/server_shell.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3/slc.py` & `telnetlib3-2.0.4/telnetlib3/slc.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3/stream_reader.py` & `telnetlib3-2.0.4/telnetlib3/stream_reader.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3/stream_writer.py` & `telnetlib3-2.0.4/telnetlib3/stream_writer.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3/telopt.py` & `telnetlib3-2.0.4/telnetlib3/telopt.py`

 * *Files identical despite different names*

### Comparing `telnetlib3-2.0.3/telnetlib3.egg-info/PKG-INFO` & `telnetlib3-2.0.4/telnetlib3.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: telnetlib3
-Version: 2.0.3
+Version: 2.0.4
 Summary: Python 3 asyncio Telnet server and client Protocol library
 Home-page: http://telnetlib3.rtfd.org/
 Author: Jeff Quast
 Author-email: contact@jeffquast.com
 License: ISC
 Keywords: telnet,server,client,bbs,mud,utf8,cp437,api,library,asyncio,talker
 Platform: any
```

### Comparing `telnetlib3-2.0.3/telnetlib3.egg-info/SOURCES.txt` & `telnetlib3-2.0.4/telnetlib3.egg-info/SOURCES.txt`

 * *Files identical despite different names*

