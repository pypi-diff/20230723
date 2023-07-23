# Comparing `tmp/vagd-0.4.7.tar.gz` & `tmp/vagd-0.4.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "vagd-0.4.7.tar", last modified: Sun Jul 23 18:26:16 2023, max compression
+gzip compressed data, was "vagd-0.4.8.tar", last modified: Sun Jul 23 18:54:33 2023, max compression
```

## Comparing `vagd-0.4.7.tar` & `vagd-0.4.8.tar`

### file list

```diff
@@ -1,41 +1,41 @@
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.364571 vagd-0.4.7/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)    35149 2023-03-05 14:43:59.000000 vagd-0.4.7/LICENSE
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4389 2023-07-23 18:26:16.364571 vagd-0.4.7/PKG-INFO
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     3805 2023-06-17 16:19:04.000000 vagd-0.4.7/README.md
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      900 2023-07-23 18:22:49.000000 vagd-0.4.7/pyproject.toml
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)       38 2023-07-23 18:26:16.364571 vagd-0.4.7/setup.cfg
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.357904 vagd-0.4.7/src/
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.361237 vagd-0.4.7/src/vagd/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)       53 2023-03-20 14:52:11.000000 vagd-0.4.7/src/vagd/__init__.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      224 2023-07-23 17:47:27.000000 vagd-0.4.7/src/vagd/__main__.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      939 2023-06-17 11:38:21.000000 vagd-0.4.7/src/vagd/box.py
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.364571 vagd-0.4.7/src/vagd/gdb/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)    20349 2023-03-04 14:19:11.000000 vagd-0.4.7/src/vagd/gdb/__init__.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4178 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/events.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      983 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/printing.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)       47 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/prompt.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      865 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/types.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      135 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/unwinder.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      844 2023-03-04 12:55:58.000000 vagd-0.4.7/src/vagd/gdb/xmethod.pyi
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)       44 2023-03-14 14:03:57.000000 vagd-0.4.7/src/vagd/gdb.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1195 2023-04-08 07:51:28.000000 vagd-0.4.7/src/vagd/helper.py
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.364571 vagd-0.4.7/src/vagd/res/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)    12925 2023-07-23 18:20:22.000000 vagd-0.4.7/src/vagd/res/seccomp.json
--rwxr-xr-x   0 gfelber   (1000) gfelber   (1000)     1371 2023-07-23 17:55:01.000000 vagd-0.4.7/src/vagd/res/template.txt
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1307 2023-07-15 07:29:51.000000 vagd-0.4.7/src/vagd/templates.py
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.364571 vagd-0.4.7/src/vagd/virts/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      132 2023-03-20 14:52:11.000000 vagd-0.4.7/src/vagd/virts/__init__.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     6028 2023-07-23 18:17:58.000000 vagd-0.4.7/src/vagd/virts/dogd.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)    10666 2023-06-17 15:51:31.000000 vagd-0.4.7/src/vagd/virts/pwngd.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)    10849 2023-06-17 15:49:55.000000 vagd-0.4.7/src/vagd/virts/qegd.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1345 2023-03-20 14:52:11.000000 vagd-0.4.7/src/vagd/virts/shgd.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     3592 2023-03-20 14:52:11.000000 vagd-0.4.7/src/vagd/virts/vagd.py
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      843 2023-03-14 14:21:12.000000 vagd-0.4.7/src/vagd/wrapper.py
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.361237 vagd-0.4.7/src/vagd.egg-info/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4389 2023-07-23 18:26:16.000000 vagd-0.4.7/src/vagd.egg-info/PKG-INFO
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)      708 2023-07-23 18:26:16.000000 vagd-0.4.7/src/vagd.egg-info/SOURCES.txt
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)        1 2023-07-23 18:26:16.000000 vagd-0.4.7/src/vagd.egg-info/dependency_links.txt
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)       31 2023-07-23 18:26:16.000000 vagd-0.4.7/src/vagd.egg-info/requires.txt
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)        5 2023-07-23 18:26:16.000000 vagd-0.4.7/src/vagd.egg-info/top_level.txt
-drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:26:16.364571 vagd-0.4.7/test/
--rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1207 2023-07-23 17:36:24.000000 vagd-0.4.7/test/test.py
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:54:33.536836 vagd-0.4.8/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)    35149 2023-03-05 14:43:59.000000 vagd-0.4.8/LICENSE
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4362 2023-07-23 18:54:33.536836 vagd-0.4.8/PKG-INFO
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     3805 2023-06-17 16:19:04.000000 vagd-0.4.8/README.md
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      871 2023-07-23 18:54:15.000000 vagd-0.4.8/pyproject.toml
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)       38 2023-07-23 18:54:33.536836 vagd-0.4.8/setup.cfg
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:54:33.530169 vagd-0.4.8/src/
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:54:33.533502 vagd-0.4.8/src/vagd/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)       53 2023-03-20 14:52:11.000000 vagd-0.4.8/src/vagd/__init__.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      224 2023-07-23 17:47:27.000000 vagd-0.4.8/src/vagd/__main__.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      939 2023-06-17 11:38:21.000000 vagd-0.4.8/src/vagd/box.py
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:54:33.536836 vagd-0.4.8/src/vagd/gdb/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)    20349 2023-03-04 14:19:11.000000 vagd-0.4.8/src/vagd/gdb/__init__.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4178 2023-03-04 12:55:58.000000 vagd-0.4.8/src/vagd/gdb/events.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      983 2023-03-04 12:55:58.000000 vagd-0.4.8/src/vagd/gdb/printing.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)       47 2023-03-04 12:55:58.000000 vagd-0.4.8/src/vagd/gdb/prompt.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      865 2023-03-04 12:55:58.000000 vagd-0.4.8/src/vagd/gdb/types.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      135 2023-03-04 12:55:58.000000 vagd-0.4.8/src/vagd/gdb/unwinder.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      844 2023-03-04 12:55:58.000000 vagd-0.4.8/src/vagd/gdb/xmethod.pyi
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)       44 2023-03-14 14:03:57.000000 vagd-0.4.8/src/vagd/gdb.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1195 2023-04-08 07:51:28.000000 vagd-0.4.8/src/vagd/helper.py
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:54:33.536836 vagd-0.4.8/src/vagd/res/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)    12925 2023-07-23 18:20:22.000000 vagd-0.4.8/src/vagd/res/seccomp.json
+-rwxr-xr-x   0 gfelber   (1000) gfelber   (1000)     1371 2023-07-23 17:55:01.000000 vagd-0.4.8/src/vagd/res/template.txt
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1307 2023-07-15 07:29:51.000000 vagd-0.4.8/src/vagd/templates.py
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:54:33.536836 vagd-0.4.8/src/vagd/virts/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      132 2023-03-20 14:52:11.000000 vagd-0.4.8/src/vagd/virts/__init__.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     6028 2023-07-23 18:17:58.000000 vagd-0.4.8/src/vagd/virts/dogd.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)    10666 2023-06-17 15:51:31.000000 vagd-0.4.8/src/vagd/virts/pwngd.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)    10849 2023-06-17 15:49:55.000000 vagd-0.4.8/src/vagd/virts/qegd.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1345 2023-03-20 14:52:11.000000 vagd-0.4.8/src/vagd/virts/shgd.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     3592 2023-03-20 14:52:11.000000 vagd-0.4.8/src/vagd/virts/vagd.py
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      843 2023-03-14 14:21:12.000000 vagd-0.4.8/src/vagd/wrapper.py
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:54:33.536836 vagd-0.4.8/src/vagd.egg-info/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     4362 2023-07-23 18:54:33.000000 vagd-0.4.8/src/vagd.egg-info/PKG-INFO
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)      708 2023-07-23 18:54:33.000000 vagd-0.4.8/src/vagd.egg-info/SOURCES.txt
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)        1 2023-07-23 18:54:33.000000 vagd-0.4.8/src/vagd.egg-info/dependency_links.txt
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)       31 2023-07-23 18:54:33.000000 vagd-0.4.8/src/vagd.egg-info/requires.txt
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)        5 2023-07-23 18:54:33.000000 vagd-0.4.8/src/vagd.egg-info/top_level.txt
+drwxr-xr-x   0 gfelber   (1000) gfelber   (1000)        0 2023-07-23 18:54:33.536836 vagd-0.4.8/test/
+-rw-r--r--   0 gfelber   (1000) gfelber   (1000)     1207 2023-07-23 17:36:24.000000 vagd-0.4.8/test/test.py
```

### Comparing `vagd-0.4.7/LICENSE` & `vagd-0.4.8/LICENSE`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/PKG-INFO` & `vagd-0.4.8/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 Metadata-Version: 2.1
 Name: vagd
-Version: 0.4.7
+Version: 0.4.8
 Summary: VirtuAlization GDb integrations in pwntools
-Author-email: 0x6fe1be2 <author@example.com>
+Author: 0x6fe1be2
 Project-URL: Homepage, https://github.com/gfelber/vagd
 Project-URL: Documentation, https://gfelber.github.io/vagd/
 Project-URL: Bug Tracker, https://github.com/gfelber/vagd/issues
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: POSIX :: Linux
 Requires-Python: >=3.7
```

### Comparing `vagd-0.4.7/README.md` & `vagd-0.4.8/README.md`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/pyproject.toml` & `vagd-0.4.8/pyproject.toml`

 * *Files 7% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 [project]
 name = "vagd"
-version = "0.4.7"
+version = "0.4.8"
 authors = [
-  { name="0x6fe1be2", email="author@example.com" },
+  { name="0x6fe1be2"},
 ]
 description = "VirtuAlization GDb integrations in pwntools"
 readme = "README.md"
 requires-python = ">=3.7"
 dependencies = ['pwntools', 'python-vagrant', 'docker']
 classifiers = [
     "License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
```

### Comparing `vagd-0.4.7/src/vagd/box.py` & `vagd-0.4.8/src/vagd/box.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/gdb/__init__.pyi` & `vagd-0.4.8/src/vagd/gdb/__init__.pyi`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/gdb/events.pyi` & `vagd-0.4.8/src/vagd/gdb/events.pyi`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/gdb/printing.pyi` & `vagd-0.4.8/src/vagd/gdb/printing.pyi`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/gdb/types.pyi` & `vagd-0.4.8/src/vagd/gdb/types.pyi`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/gdb/xmethod.pyi` & `vagd-0.4.8/src/vagd/gdb/xmethod.pyi`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/helper.py` & `vagd-0.4.8/src/vagd/helper.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/res/seccomp.json` & `vagd-0.4.8/src/vagd/res/seccomp.json`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/res/template.txt` & `vagd-0.4.8/src/vagd/res/template.txt`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/templates.py` & `vagd-0.4.8/src/vagd/templates.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/virts/dogd.py` & `vagd-0.4.8/src/vagd/virts/dogd.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/virts/pwngd.py` & `vagd-0.4.8/src/vagd/virts/pwngd.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/virts/qegd.py` & `vagd-0.4.8/src/vagd/virts/qegd.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/virts/shgd.py` & `vagd-0.4.8/src/vagd/virts/shgd.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/virts/vagd.py` & `vagd-0.4.8/src/vagd/virts/vagd.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd/wrapper.py` & `vagd-0.4.8/src/vagd/wrapper.py`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/src/vagd.egg-info/PKG-INFO` & `vagd-0.4.8/src/vagd.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 Metadata-Version: 2.1
 Name: vagd
-Version: 0.4.7
+Version: 0.4.8
 Summary: VirtuAlization GDb integrations in pwntools
-Author-email: 0x6fe1be2 <author@example.com>
+Author: 0x6fe1be2
 Project-URL: Homepage, https://github.com/gfelber/vagd
 Project-URL: Documentation, https://gfelber.github.io/vagd/
 Project-URL: Bug Tracker, https://github.com/gfelber/vagd/issues
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: POSIX :: Linux
 Requires-Python: >=3.7
```

### Comparing `vagd-0.4.7/src/vagd.egg-info/SOURCES.txt` & `vagd-0.4.8/src/vagd.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `vagd-0.4.7/test/test.py` & `vagd-0.4.8/test/test.py`

 * *Files identical despite different names*

