# Comparing `tmp/AutoQPF-0.1.3.tar.gz` & `tmp/AutoQPF-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "AutoQPF-0.1.3.tar", last modified: Sun Jul 23 02:29:10 2023, max compression
+gzip compressed data, was "AutoQPF-0.1.4.tar", last modified: Sun Jul 23 04:43:10 2023, max compression
```

## Comparing `AutoQPF-0.1.3.tar` & `AutoQPF-0.1.4.tar`

### file list

```diff
@@ -1,16 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 02:29:10.716466 AutoQPF-0.1.3/
-drwxrwxrwx   0        0        0        0 2023-07-23 02:29:10.711464 AutoQPF-0.1.3/AutoQPF.egg-info/
--rw-rw-rw-   0        0        0     2289 2023-07-23 02:29:10.000000 AutoQPF-0.1.3/AutoQPF.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      244 2023-07-23 02:29:10.000000 AutoQPF-0.1.3/AutoQPF.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 02:29:10.000000 AutoQPF-0.1.3/AutoQPF.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       12 2023-07-23 02:29:10.000000 AutoQPF-0.1.3/AutoQPF.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-07-23 02:29:10.000000 AutoQPF-0.1.3/AutoQPF.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     1091 2023-07-22 05:44:21.000000 AutoQPF-0.1.3/LICENSE
--rw-rw-rw-   0        0        0     2289 2023-07-23 02:29:10.714466 AutoQPF-0.1.3/PKG-INFO
--rw-rw-rw-   0        0        0     1617 2023-07-22 21:26:58.000000 AutoQPF-0.1.3/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 02:29:10.714466 AutoQPF-0.1.3/auto_qpf/
--rw-rw-rw-   0        0        0      259 2023-07-23 02:27:06.000000 AutoQPF-0.1.3/auto_qpf/__init__.py
--rw-rw-rw-   0        0        0     6125 2023-07-22 21:27:05.000000 AutoQPF-0.1.3/auto_qpf/qpf.py
--rw-rw-rw-   0        0        0      257 2023-07-22 04:57:33.000000 AutoQPF-0.1.3/auto_qpf/qpf_exceptions.py
--rw-rw-rw-   0        0        0       42 2023-07-23 02:29:10.716466 AutoQPF-0.1.3/setup.cfg
--rw-rw-rw-   0        0        0      963 2023-07-23 02:23:21.000000 AutoQPF-0.1.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:43:10.051165 AutoQPF-0.1.4/
+drwxrwxrwx   0        0        0        0 2023-07-23 04:43:10.047156 AutoQPF-0.1.4/AutoQPF.egg-info/
+-rw-rw-rw-   0        0        0     2289 2023-07-23 04:43:09.000000 AutoQPF-0.1.4/AutoQPF.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      266 2023-07-23 04:43:09.000000 AutoQPF-0.1.4/AutoQPF.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 04:43:09.000000 AutoQPF-0.1.4/AutoQPF.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       12 2023-07-23 04:43:09.000000 AutoQPF-0.1.4/AutoQPF.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 04:43:09.000000 AutoQPF-0.1.4/AutoQPF.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     1091 2023-07-22 05:44:21.000000 AutoQPF-0.1.4/LICENSE
+-rw-rw-rw-   0        0        0     2289 2023-07-23 04:43:10.051165 AutoQPF-0.1.4/PKG-INFO
+-rw-rw-rw-   0        0        0     1617 2023-07-22 21:26:58.000000 AutoQPF-0.1.4/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 04:43:10.050162 AutoQPF-0.1.4/auto_qpf/
+-rw-rw-rw-   0        0        0      259 2023-07-23 02:27:06.000000 AutoQPF-0.1.4/auto_qpf/__init__.py
+-rw-rw-rw-   0        0        0      561 2023-07-23 04:41:05.000000 AutoQPF-0.1.4/auto_qpf/long_path.py
+-rw-rw-rw-   0        0        0     6572 2023-07-23 04:42:31.000000 AutoQPF-0.1.4/auto_qpf/qpf.py
+-rw-rw-rw-   0        0        0      257 2023-07-22 04:57:33.000000 AutoQPF-0.1.4/auto_qpf/qpf_exceptions.py
+-rw-rw-rw-   0        0        0       42 2023-07-23 04:43:10.051165 AutoQPF-0.1.4/setup.cfg
+-rw-rw-rw-   0        0        0      963 2023-07-23 04:42:43.000000 AutoQPF-0.1.4/setup.py
```

### Comparing `AutoQPF-0.1.3/AutoQPF.egg-info/PKG-INFO` & `AutoQPF-0.1.4/AutoQPF.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AutoQPF
-Version: 0.1.3
+Version: 0.1.4
 Summary: Generates QPF frame time codes to be used with x264/x265
 Home-page: https://github.com/jlw4049/AutoQPF
 Author: Jessie Wilson
 Author-email: jessielw4049@gmail.com
 License: MIT
 Keywords: AutoQPF
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `AutoQPF-0.1.3/LICENSE` & `AutoQPF-0.1.4/LICENSE`

 * *Files identical despite different names*

### Comparing `AutoQPF-0.1.3/PKG-INFO` & `AutoQPF-0.1.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AutoQPF
-Version: 0.1.3
+Version: 0.1.4
 Summary: Generates QPF frame time codes to be used with x264/x265
 Home-page: https://github.com/jlw4049/AutoQPF
 Author: Jessie Wilson
 Author-email: jessielw4049@gmail.com
 License: MIT
 Keywords: AutoQPF
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `AutoQPF-0.1.3/README.md` & `AutoQPF-0.1.4/README.md`

 * *Files identical despite different names*

### Comparing `AutoQPF-0.1.3/auto_qpf/qpf.py` & `AutoQPF-0.1.4/auto_qpf/qpf.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,11 +1,13 @@
 from pathlib import Path
 from pymediainfo import MediaInfo
 from typing import Union
+import platform
 
+from auto_qpf.long_path import check_for_long_path
 from auto_qpf.qpf_exceptions import (
     ImproperChapterError,
     NoChapterDataError,
     ChapterIndexError,
 )
 
 
@@ -31,14 +33,22 @@
             file_output (Union[Path, str], optional): File output. Defaults to None (will auto create name).
             write_to_disk (bool, optional): If this is set, writes to disk, if not it'll return an object with the qpf.
             fps (Union[int, float], optional): Source FPS. Defaults to 23.976. If auto_detect_fps is true and
             input is a not a .txt file, this will be over-ridden automatically.
             auto_detect_fps (bool, optional): Auto detects non text based sources if a video track is present.
             Defaults to True.
         """
+        # check if we're on a windows platform, if so check for long path support
+        if platform.system() == "Windows":
+            long_path = check_for_long_path()
+            if not long_path:
+                print(
+                    "WARNING: Long path is not enabled for this OS. This can cause issues for paths greater > 260 characters."
+                )
+
         # convert file_input to Path object
         file_input = Path(file_input)
 
         # auto generate file output if none was provided
         if not file_output:
             file_output = self._auto_output(file_input)
```

### Comparing `AutoQPF-0.1.3/setup.py` & `AutoQPF-0.1.4/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 ]
 
 with open(os.path.join(os.path.dirname(__file__), "README.md")) as fd:
     ext_long_desc = fd.read()
 
 setup(
     name="AutoQPF",
-    version="0.1.3",
+    version="0.1.4",
     description="Generates QPF frame time codes to be used with x264/x265",
     long_description=ext_long_desc,
     long_description_content_type="text/markdown",
     url="https://github.com/jlw4049/AutoQPF",
     author="Jessie Wilson",
     author_email="jessielw4049@gmail.com",
     license="MIT",
```

