# Comparing `tmp/glotter2-0.7.1.tar.gz` & `tmp/glotter2-0.7.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "glotter2-0.7.1.tar", max compression
+gzip compressed data, was "glotter2-0.7.2.tar", max compression
```

## Comparing `glotter2-0.7.1.tar` & `glotter2-0.7.2.tar`

### file list

```diff
@@ -1,22 +1,22 @@
--rw-r--r--   0        0        0     1105 2023-02-25 14:19:23.663270 glotter2-0.7.1/LICENSE.txt
--rw-r--r--   0        0        0     3096 2023-06-10 21:58:05.055966 glotter2-0.7.1/README.md
--rw-r--r--   0        0        0      191 2023-04-01 17:41:06.994287 glotter2-0.7.1/glotter/__init__.py
--rw-r--r--   0        0        0     4258 2023-06-10 17:29:20.213170 glotter2-0.7.1/glotter/__main__.py
--rw-r--r--   0        0        0    12978 2023-03-28 18:23:01.742869 glotter2-0.7.1/glotter/auto_gen_test.py
--rw-r--r--   0        0        0     2334 2023-06-10 21:13:27.448366 glotter2-0.7.1/glotter/batch.py
--rw-r--r--   0        0        0     4297 2023-06-10 00:48:10.057388 glotter2-0.7.1/glotter/containerfactory.py
--rw-r--r--   0        0        0      680 2023-02-26 16:00:40.206266 glotter2-0.7.1/glotter/decorators.py
--rw-r--r--   0        0        0     1340 2023-06-10 19:43:20.404026 glotter2-0.7.1/glotter/download.py
--rw-r--r--   0        0        0     4753 2023-03-18 14:28:46.995459 glotter2-0.7.1/glotter/project.py
--rw-r--r--   0        0        0     3087 2023-02-26 19:19:43.729458 glotter2-0.7.1/glotter/report.py
--rw-r--r--   0        0        0      762 2023-06-08 23:13:27.025405 glotter2-0.7.1/glotter/run.py
--rw-r--r--   0        0        0     7758 2023-03-18 19:56:57.285778 glotter2-0.7.1/glotter/settings.py
--rw-r--r--   0        0        0      327 2023-03-14 17:43:43.187564 glotter2-0.7.1/glotter/singleton.py
--rw-r--r--   0        0        0     6648 2023-06-10 00:21:29.981543 glotter2-0.7.1/glotter/source.py
--rw-r--r--   0        0        0     1933 2023-03-17 22:36:01.438407 glotter2-0.7.1/glotter/test.py
--rw-r--r--   0        0        0     5027 2023-04-01 18:00:31.534775 glotter2-0.7.1/glotter/test_doc_generator.py
--rw-r--r--   0        0        0     2195 2023-06-08 23:02:04.303251 glotter2-0.7.1/glotter/test_generator.py
--rw-r--r--   0        0        0     5490 2023-02-25 19:40:59.629278 glotter2-0.7.1/glotter/testinfo.py
--rw-r--r--   0        0        0      853 2023-03-17 22:34:49.362111 glotter2-0.7.1/glotter/utils.py
--rw-r--r--   0        0        0     1595 2023-06-10 21:58:16.714262 glotter2-0.7.1/pyproject.toml
--rw-r--r--   0        0        0     4344 1970-01-01 00:00:00.000000 glotter2-0.7.1/PKG-INFO
+-rw-r--r--   0        0        0     1105 2023-02-25 14:19:23.663270 glotter2-0.7.2/LICENSE.txt
+-rw-r--r--   0        0        0     3175 2023-07-23 14:36:48.084097 glotter2-0.7.2/README.md
+-rw-r--r--   0        0        0      191 2023-04-01 17:41:06.994287 glotter2-0.7.2/glotter/__init__.py
+-rw-r--r--   0        0        0     4258 2023-06-10 17:29:20.213170 glotter2-0.7.2/glotter/__main__.py
+-rw-r--r--   0        0        0    12978 2023-03-28 18:23:01.742869 glotter2-0.7.2/glotter/auto_gen_test.py
+-rw-r--r--   0        0        0     2334 2023-06-10 21:13:27.448366 glotter2-0.7.2/glotter/batch.py
+-rw-r--r--   0        0        0     4340 2023-07-23 14:38:28.096405 glotter2-0.7.2/glotter/containerfactory.py
+-rw-r--r--   0        0        0      680 2023-02-26 16:00:40.206266 glotter2-0.7.2/glotter/decorators.py
+-rw-r--r--   0        0        0     1340 2023-06-10 19:43:20.404026 glotter2-0.7.2/glotter/download.py
+-rw-r--r--   0        0        0     4753 2023-03-18 14:28:46.995459 glotter2-0.7.2/glotter/project.py
+-rw-r--r--   0        0        0     3087 2023-02-26 19:19:43.729458 glotter2-0.7.2/glotter/report.py
+-rw-r--r--   0        0        0      762 2023-06-08 23:13:27.025405 glotter2-0.7.2/glotter/run.py
+-rw-r--r--   0        0        0     7758 2023-03-18 19:56:57.285778 glotter2-0.7.2/glotter/settings.py
+-rw-r--r--   0        0        0      327 2023-03-14 17:43:43.187564 glotter2-0.7.2/glotter/singleton.py
+-rw-r--r--   0        0        0     6648 2023-06-10 00:21:29.981543 glotter2-0.7.2/glotter/source.py
+-rw-r--r--   0        0        0     1933 2023-03-17 22:36:01.438407 glotter2-0.7.2/glotter/test.py
+-rw-r--r--   0        0        0     5027 2023-04-01 18:00:31.534775 glotter2-0.7.2/glotter/test_doc_generator.py
+-rw-r--r--   0        0        0     2195 2023-06-08 23:02:04.303251 glotter2-0.7.2/glotter/test_generator.py
+-rw-r--r--   0        0        0     5490 2023-02-25 19:40:59.629278 glotter2-0.7.2/glotter/testinfo.py
+-rw-r--r--   0        0        0      853 2023-03-17 22:34:49.362111 glotter2-0.7.2/glotter/utils.py
+-rw-r--r--   0        0        0     1595 2023-07-23 14:40:21.876895 glotter2-0.7.2/pyproject.toml
+-rw-r--r--   0        0        0     4423 1970-01-01 00:00:00.000000 glotter2-0.7.2/PKG-INFO
```

### Comparing `glotter2-0.7.1/LICENSE.txt` & `glotter2-0.7.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/README.md` & `glotter2-0.7.2/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -21,14 +21,16 @@
 
 If you'd like to contribute to Glotter2, read our [contributing guidelines](./CONTRIBUTING.md).
 
 ## Changelog
 
 ### Glotter2 releases
 
+* 0.7.2:
+  * Make sure temporary directory used for docker is world accessible
 * 0.7.1:
   * Remove work-in-progress from changelog
 * 0.7.0:
   * Add `try/finally` to auto-generated project fixture to make sure docker
     container is cleaned up
   * Add `try/finally` to `run` command to make sure docker container is
     cleaned up
```

### Comparing `glotter2-0.7.1/glotter/__main__.py` & `glotter2-0.7.2/glotter/__main__.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/auto_gen_test.py` & `glotter2-0.7.2/glotter/auto_gen_test.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/batch.py` & `glotter2-0.7.2/glotter/batch.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/containerfactory.py` & `glotter2-0.7.2/glotter/containerfactory.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,7 +1,8 @@
+import os
 import shutil
 import tempfile
 from datetime import datetime, timedelta
 from uuid import uuid4 as uuid
 
 import docker
 
@@ -27,14 +28,15 @@
 
         :param source: the source to use inside the container
         :return: a running container specific to the source
         """
         key = source.full_path
 
         tmp_dir = tempfile.mkdtemp()
+        os.chmod(tmp_dir, 0o777)
         shutil.copy(source.full_path, tmp_dir)
         self._volume_dis[key] = tmp_dir
 
         image = self.get_image(source.test_info.container_info)
         volume_info = {tmp_dir: {"bind": "/src", "mode": "rw"}}
         if key not in self._containers:
             self._containers[key] = self._client.containers.run(
```

### Comparing `glotter2-0.7.1/glotter/decorators.py` & `glotter2-0.7.2/glotter/decorators.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/download.py` & `glotter2-0.7.2/glotter/download.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/project.py` & `glotter2-0.7.2/glotter/project.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/report.py` & `glotter2-0.7.2/glotter/report.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/run.py` & `glotter2-0.7.2/glotter/run.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/settings.py` & `glotter2-0.7.2/glotter/settings.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/source.py` & `glotter2-0.7.2/glotter/source.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/test.py` & `glotter2-0.7.2/glotter/test.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/test_doc_generator.py` & `glotter2-0.7.2/glotter/test_doc_generator.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/test_generator.py` & `glotter2-0.7.2/glotter/test_generator.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/testinfo.py` & `glotter2-0.7.2/glotter/testinfo.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/glotter/utils.py` & `glotter2-0.7.2/glotter/utils.py`

 * *Files identical despite different names*

### Comparing `glotter2-0.7.1/pyproject.toml` & `glotter2-0.7.2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [tool.poetry]
 name = "glotter2"
 packages = [{include="glotter"}]
-version = "0.7.1"
+version = "0.7.2"
 description = "An execution library for scripts written in any language. This is a fork of https://github.com/auroq/glotter"
 authors = ["auroq", "rzuckerm"]
 readme = "README.md"
 license = "LICENSE.txt"
 homepage = "https://github.com/rzuckerm/glotter2"
 documentation = "https://rzuckerm.github.io/glotter2"
 classifiers = [
```

### Comparing `glotter2-0.7.1/PKG-INFO` & `glotter2-0.7.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: glotter2
-Version: 0.7.1
+Version: 0.7.2
 Summary: An execution library for scripts written in any language. This is a fork of https://github.com/auroq/glotter
 Home-page: https://github.com/rzuckerm/glotter2
 License: LICENSE.txt
 Author: auroq
 Requires-Python: >=3.8,<4.0
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
@@ -50,14 +50,16 @@
 
 If you'd like to contribute to Glotter2, read our [contributing guidelines](./CONTRIBUTING.md).
 
 ## Changelog
 
 ### Glotter2 releases
 
+* 0.7.2:
+  * Make sure temporary directory used for docker is world accessible
 * 0.7.1:
   * Remove work-in-progress from changelog
 * 0.7.0:
   * Add `try/finally` to auto-generated project fixture to make sure docker
     container is cleaned up
   * Add `try/finally` to `run` command to make sure docker container is
     cleaned up
```

