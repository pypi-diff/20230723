# Comparing `tmp/pueda-0.1.5.tar.gz` & `tmp/pueda-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pueda-0.1.5.tar", last modified: Wed Jun 14 20:15:21 2023, max compression
+gzip compressed data, was "pueda-0.1.6.tar", last modified: Sun Jul 23 15:36:31 2023, max compression
```

## Comparing `pueda-0.1.5.tar` & `pueda-0.1.6.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-06-14 20:15:21.824193 pueda-0.1.5/
--rwxrwxrwx   0 marco     (1000) marco     (1000)    11357 2022-12-10 01:01:26.000000 pueda-0.1.5/LICENSE
--rwxrwxrwx   0 marco     (1000) marco     (1000)     2267 2023-06-14 20:15:21.824432 pueda-0.1.5/PKG-INFO
--rwxrwxrwx   0 marco     (1000) marco     (1000)     1923 2023-02-27 23:28:27.000000 pueda-0.1.5/README.md
-drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-06-14 20:15:21.759828 pueda-0.1.5/data/
-drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-06-14 20:15:21.761004 pueda-0.1.5/data/icarus/
-drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-06-14 20:15:21.771894 pueda-0.1.5/data/icarus/inc/
--rwxrwxrwx   0 marco     (1000) marco     (1000)       88 2023-02-26 23:04:23.000000 pueda-0.1.5/data/icarus/inc/dump.vh
-drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-06-14 20:15:21.774094 pueda-0.1.5/data/icarus/src/
--rwxrwxrwx   0 marco     (1000) marco     (1000)      296 2023-02-26 23:04:23.000000 pueda-0.1.5/data/icarus/src/dump.v
--rwxrwxrwx   0 marco     (1000) marco     (1000)      103 2023-06-14 20:15:21.825369 pueda-0.1.5/setup.cfg
--rwxrwxrwx   0 marco     (1000) marco     (1000)      963 2023-06-14 20:12:57.000000 pueda-0.1.5/setup.py
-drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-06-14 20:15:21.762571 pueda-0.1.5/src/
-drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-06-14 20:15:21.812516 pueda-0.1.5/src/pueda/
--rwxrwxrwx   0 marco     (1000) marco     (1000)      150 2023-03-15 01:01:16.000000 pueda-0.1.5/src/pueda/__init__.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)     3092 2023-03-15 01:37:00.000000 pueda-0.1.5/src/pueda/common.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)     7433 2023-03-26 15:13:03.000000 pueda-0.1.5/src/pueda/edalize.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)      866 2023-02-27 22:13:51.000000 pueda-0.1.5/src/pueda/gtkw.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)     2924 2023-03-15 02:15:01.000000 pueda-0.1.5/src/pueda/icarus.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)     4934 2023-03-15 01:37:22.000000 pueda-0.1.5/src/pueda/myhdl.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)     1795 2023-06-14 20:12:34.000000 pueda-0.1.5/src/pueda/pyverilator.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)     1688 2023-03-15 01:49:00.000000 pueda-0.1.5/src/pueda/vcd.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)      325 2023-01-22 17:37:49.000000 pueda-0.1.5/src/pueda/veriloggen.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)     1376 2023-02-28 20:52:57.000000 pueda-0.1.5/src/pueda/yosys.py
-drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-06-14 20:15:21.819027 pueda-0.1.5/src/pueda.egg-info/
--rwxrwxrwx   0 marco     (1000) marco     (1000)     2267 2023-06-14 20:15:21.000000 pueda-0.1.5/src/pueda.egg-info/PKG-INFO
--rwxrwxrwx   0 marco     (1000) marco     (1000)      558 2023-06-14 20:15:21.000000 pueda-0.1.5/src/pueda.egg-info/SOURCES.txt
--rwxrwxrwx   0 marco     (1000) marco     (1000)        1 2023-06-14 20:15:21.000000 pueda-0.1.5/src/pueda.egg-info/dependency_links.txt
--rwxrwxrwx   0 marco     (1000) marco     (1000)       69 2023-06-14 20:15:21.000000 pueda-0.1.5/src/pueda.egg-info/requires.txt
--rwxrwxrwx   0 marco     (1000) marco     (1000)        6 2023-06-14 20:15:21.000000 pueda-0.1.5/src/pueda.egg-info/top_level.txt
-drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-06-14 20:15:21.823204 pueda-0.1.5/test/
--rwxrwxrwx   0 marco     (1000) marco     (1000)     1384 2023-06-14 20:13:34.000000 pueda-0.1.5/test/test.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)     1162 2023-02-27 20:41:20.000000 pueda-0.1.5/test/test_myhdl_counter.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)      463 2023-02-27 20:41:20.000000 pueda-0.1.5/test/test_verilated_dpi_counter.py
--rwxrwxrwx   0 marco     (1000) marco     (1000)      454 2023-02-27 20:41:20.000000 pueda-0.1.5/test/test_verilator_counter.py
+drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-07-23 15:36:31.860701 pueda-0.1.6/
+-rwxrwxrwx   0 marco     (1000) marco     (1000)    11357 2022-12-10 01:01:26.000000 pueda-0.1.6/LICENSE
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     2267 2023-07-23 15:36:31.861025 pueda-0.1.6/PKG-INFO
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     1923 2023-02-27 23:28:27.000000 pueda-0.1.6/README.md
+drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-07-23 15:36:31.804370 pueda-0.1.6/data/
+drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-07-23 15:36:31.806531 pueda-0.1.6/data/icarus/
+drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-07-23 15:36:31.816916 pueda-0.1.6/data/icarus/inc/
+-rwxrwxrwx   0 marco     (1000) marco     (1000)       88 2023-02-26 23:04:23.000000 pueda-0.1.6/data/icarus/inc/dump.vh
+drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-07-23 15:36:31.818115 pueda-0.1.6/data/icarus/src/
+-rwxrwxrwx   0 marco     (1000) marco     (1000)      296 2023-02-26 23:04:23.000000 pueda-0.1.6/data/icarus/src/dump.v
+-rwxrwxrwx   0 marco     (1000) marco     (1000)      103 2023-07-23 15:36:31.862339 pueda-0.1.6/setup.cfg
+-rwxrwxrwx   0 marco     (1000) marco     (1000)      963 2023-07-23 15:33:11.000000 pueda-0.1.6/setup.py
+drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-07-23 15:36:31.807834 pueda-0.1.6/src/
+drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-07-23 15:36:31.836585 pueda-0.1.6/src/pueda/
+-rwxrwxrwx   0 marco     (1000) marco     (1000)      150 2023-03-15 01:01:16.000000 pueda-0.1.6/src/pueda/__init__.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     3092 2023-03-15 01:37:00.000000 pueda-0.1.6/src/pueda/common.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     7433 2023-03-26 15:13:03.000000 pueda-0.1.6/src/pueda/edalize.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)      866 2023-02-27 22:13:51.000000 pueda-0.1.6/src/pueda/gtkw.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     2924 2023-03-15 02:15:01.000000 pueda-0.1.6/src/pueda/icarus.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     4934 2023-03-15 01:37:22.000000 pueda-0.1.6/src/pueda/myhdl.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     2159 2023-07-23 15:32:32.000000 pueda-0.1.6/src/pueda/pyverilator.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     1688 2023-03-15 01:49:00.000000 pueda-0.1.6/src/pueda/vcd.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)      325 2023-01-22 17:37:49.000000 pueda-0.1.6/src/pueda/veriloggen.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     1376 2023-02-28 20:52:57.000000 pueda-0.1.6/src/pueda/yosys.py
+drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-07-23 15:36:31.850012 pueda-0.1.6/src/pueda.egg-info/
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     2267 2023-07-23 15:36:31.000000 pueda-0.1.6/src/pueda.egg-info/PKG-INFO
+-rwxrwxrwx   0 marco     (1000) marco     (1000)      558 2023-07-23 15:36:31.000000 pueda-0.1.6/src/pueda.egg-info/SOURCES.txt
+-rwxrwxrwx   0 marco     (1000) marco     (1000)        1 2023-07-23 15:36:31.000000 pueda-0.1.6/src/pueda.egg-info/dependency_links.txt
+-rwxrwxrwx   0 marco     (1000) marco     (1000)       69 2023-07-23 15:36:31.000000 pueda-0.1.6/src/pueda.egg-info/requires.txt
+-rwxrwxrwx   0 marco     (1000) marco     (1000)        6 2023-07-23 15:36:31.000000 pueda-0.1.6/src/pueda.egg-info/top_level.txt
+drwxrwxrwx   0 marco     (1000) marco     (1000)        0 2023-07-23 15:36:31.859371 pueda-0.1.6/test/
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     1384 2023-06-14 20:13:34.000000 pueda-0.1.6/test/test.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)     1162 2023-02-27 20:41:20.000000 pueda-0.1.6/test/test_myhdl_counter.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)      463 2023-02-27 20:41:20.000000 pueda-0.1.6/test/test_verilated_dpi_counter.py
+-rwxrwxrwx   0 marco     (1000) marco     (1000)      454 2023-02-27 20:41:20.000000 pueda-0.1.6/test/test_verilator_counter.py
```

### Comparing `pueda-0.1.5/LICENSE` & `pueda-0.1.6/LICENSE`

 * *Files identical despite different names*

### Comparing `pueda-0.1.5/PKG-INFO` & `pueda-0.1.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pueda
-Version: 0.1.5
+Version: 0.1.6
 Summary: Collection of python for micro-Electronic Design Automation
 Home-page: https://github.com/bat52/pueda
 Author: Marco Merlin
 Author-email: marcomerli@gmail.com
 License: Apache 2.0
 Keywords: python EDA CAD
 Platform: UNKNOWN
```

### Comparing `pueda-0.1.5/README.md` & `pueda-0.1.6/README.md`

 * *Files identical despite different names*

### Comparing `pueda-0.1.5/setup.py` & `pueda-0.1.6/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     for d, folders, files in os.walk(datadir)]
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setup(
     name='pueda',
-    version='0.1.5',
+    version='0.1.6',
     license='Apache 2.0',
     author="Marco Merlin",
     author_email='marcomerli@gmail.com',
     packages=find_packages('src'),
     package_dir={'': 'src'},
     description="Collection of python for micro-Electronic Design Automation",
     long_description=long_description,
```

### Comparing `pueda-0.1.5/src/pueda/common.py` & `pueda-0.1.6/src/pueda/common.py`

 * *Files identical despite different names*

### Comparing `pueda-0.1.5/src/pueda/edalize.py` & `pueda-0.1.6/src/pueda/edalize.py`

 * *Files identical despite different names*

### Comparing `pueda-0.1.5/src/pueda/gtkw.py` & `pueda-0.1.6/src/pueda/gtkw.py`

 * *Files identical despite different names*

### Comparing `pueda-0.1.5/src/pueda/icarus.py` & `pueda-0.1.6/src/pueda/icarus.py`

 * *Files identical despite different names*

### Comparing `pueda-0.1.5/src/pueda/myhdl.py` & `pueda-0.1.6/src/pueda/myhdl.py`

 * *Files identical despite different names*

### Comparing `pueda-0.1.5/src/pueda/vcd.py` & `pueda-0.1.6/src/pueda/vcd.py`

 * *Files identical despite different names*

### Comparing `pueda-0.1.5/src/pueda/yosys.py` & `pueda-0.1.6/src/pueda/yosys.py`

 * *Files identical despite different names*

### Comparing `pueda-0.1.5/src/pueda.egg-info/PKG-INFO` & `pueda-0.1.6/src/pueda.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pueda
-Version: 0.1.5
+Version: 0.1.6
 Summary: Collection of python for micro-Electronic Design Automation
 Home-page: https://github.com/bat52/pueda
 Author: Marco Merlin
 Author-email: marcomerli@gmail.com
 License: Apache 2.0
 Keywords: python EDA CAD
 Platform: UNKNOWN
```

### Comparing `pueda-0.1.5/src/pueda.egg-info/SOURCES.txt` & `pueda-0.1.6/src/pueda.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pueda-0.1.5/test/test.py` & `pueda-0.1.6/test/test.py`

 * *Files identical despite different names*

### Comparing `pueda-0.1.5/test/test_myhdl_counter.py` & `pueda-0.1.6/test/test_myhdl_counter.py`

 * *Files identical despite different names*

