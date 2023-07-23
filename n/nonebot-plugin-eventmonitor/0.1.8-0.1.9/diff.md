# Comparing `tmp/nonebot_plugin_eventmonitor-0.1.8.tar.gz` & `tmp/nonebot_plugin_eventmonitor-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_eventmonitor-0.1.8.tar", last modified: Sun Jul 23 13:48:22 2023, max compression
+gzip compressed data, was "nonebot_plugin_eventmonitor-0.1.9.tar", last modified: Sun Jul 23 15:01:13 2023, max compression
```

## Comparing `nonebot_plugin_eventmonitor-0.1.8.tar` & `nonebot_plugin_eventmonitor-0.1.9.tar`

### file list

```diff
@@ -1,19 +1,18 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 13:48:22.364841 nonebot_plugin_eventmonitor-0.1.8/
--rw-rw-rw-   0        0        0    35149 2023-01-29 04:13:58.000000 nonebot_plugin_eventmonitor-0.1.8/LICENSE
--rw-rw-rw-   0        0        0     1601 2023-07-23 13:48:22.364841 nonebot_plugin_eventmonitor-0.1.8/PKG-INFO
--rw-rw-rw-   0        0        0      970 2023-07-23 13:29:15.000000 nonebot_plugin_eventmonitor-0.1.8/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 13:48:22.351223 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/
--rw-rw-rw-   0        0        0      734 2023-07-23 13:05:32.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/__init__.py
--rw-rw-rw-   0        0        0     2823 2023-07-23 12:12:06.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/admin.py
--rw-rw-rw-   0        0        0     7871 2023-07-23 12:32:13.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/handle.py
--rw-rw-rw-   0        0        0     1621 2023-07-23 12:08:52.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/honour.py
--rw-rw-rw-   0        0        0     2166 2023-07-23 12:34:54.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/stamp.py
--rw-rw-rw-   0        0        0     7116 2023-07-23 13:05:35.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:48:22.364841 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/
--rw-rw-rw-   0        0        0     1601 2023-07-23 13:48:22.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      507 2023-07-23 13:48:22.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 13:48:22.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       59 2023-07-23 13:48:22.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/requires.txt
--rw-rw-rw-   0        0        0       28 2023-07-23 13:48:22.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 13:48:22.364841 nonebot_plugin_eventmonitor-0.1.8/setup.cfg
--rw-rw-rw-   0        0        0      993 2023-07-23 13:06:41.000000 nonebot_plugin_eventmonitor-0.1.8/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:01:13.150708 nonebot_plugin_eventmonitor-0.1.9/
+-rw-rw-rw-   0        0        0    35149 2023-01-29 04:13:58.000000 nonebot_plugin_eventmonitor-0.1.9/LICENSE
+-rw-rw-rw-   0        0        0     1601 2023-07-23 15:01:13.150708 nonebot_plugin_eventmonitor-0.1.9/PKG-INFO
+-rw-rw-rw-   0        0        0      970 2023-07-23 14:56:54.000000 nonebot_plugin_eventmonitor-0.1.9/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 15:01:13.119050 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor/
+-rw-rw-rw-   0        0        0     8271 2023-07-23 14:55:01.000000 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor/__init__.py
+-rw-rw-rw-   0        0        0     2823 2023-07-23 12:12:06.000000 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor/admin.py
+-rw-rw-rw-   0        0        0     1621 2023-07-23 14:34:04.000000 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor/honour.py
+-rw-rw-rw-   0        0        0     2166 2023-07-23 12:34:54.000000 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor/stamp.py
+-rw-rw-rw-   0        0        0     7116 2023-07-23 14:55:08.000000 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:01:13.150708 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor.egg-info/
+-rw-rw-rw-   0        0        0     1601 2023-07-23 15:01:12.000000 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      469 2023-07-23 15:01:13.000000 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:01:12.000000 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       59 2023-07-23 15:01:12.000000 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       28 2023-07-23 15:01:12.000000 nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 15:01:13.150708 nonebot_plugin_eventmonitor-0.1.9/setup.cfg
+-rw-rw-rw-   0        0        0      993 2023-07-23 14:57:06.000000 nonebot_plugin_eventmonitor-0.1.9/setup.py
```

### Comparing `nonebot_plugin_eventmonitor-0.1.8/LICENSE` & `nonebot_plugin_eventmonitor-0.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_eventmonitor-0.1.8/PKG-INFO` & `nonebot_plugin_eventmonitor-0.1.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 Metadata-Version: 2.1
 Name: nonebot_plugin_eventmonitor
-Version: 0.1.8
+Version: 0.1.9
 Summary: 监控群事件的插件，支持戳一戳，成员变动，群荣誉，运气王变化等提示
 Home-page: https://github.com/Reversedeer/nonebot_plugin_eventmonitor
 Author: schwarzwald
 Project-URL: Bug Tracker, https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 <details>
     <summary><h2>更新日志</h2></summary>
 
-- v0.1.8
+- v0.1.9
 
   - 修复群文件不能检测(少写一个字母qwq)
   - 增加功能开关指令：event状态/event配置 
 - v0.1.7
   - 新增所有功能开关[#issue5](https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues/9
   - 增加权限控制
   - 修复潜在的bug
```

### Comparing `nonebot_plugin_eventmonitor-0.1.8/README.md` & `nonebot_plugin_eventmonitor-0.1.9/README.md`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 <details>
     <summary><h2>更新日志</h2></summary>
 
-- v0.1.8
+- v0.1.9
 
   - 修复群文件不能检测(少写一个字母qwq)
   - 增加功能开关指令：event状态/event配置 
 - v0.1.7
   - 新增所有功能开关[#issue5](https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues/9
   - 增加权限控制
   - 修复潜在的bug
```

### Comparing `nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/admin.py` & `nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor/admin.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/honour.py` & `nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor/honour.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/stamp.py` & `nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor/stamp.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/utils.py` & `nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor/utils.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/PKG-INFO` & `nonebot_plugin_eventmonitor-0.1.9/nonebot_plugin_eventmonitor.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-eventmonitor
-Version: 0.1.8
+Version: 0.1.9
 Summary: 监控群事件的插件，支持戳一戳，成员变动，群荣誉，运气王变化等提示
 Home-page: https://github.com/Reversedeer/nonebot_plugin_eventmonitor
 Author: schwarzwald
 Project-URL: Bug Tracker, https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 <details>
     <summary><h2>更新日志</h2></summary>
 
-- v0.1.8
+- v0.1.9
 
   - 修复群文件不能检测(少写一个字母qwq)
   - 增加功能开关指令：event状态/event配置 
 - v0.1.7
   - 新增所有功能开关[#issue5](https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues/9
   - 增加权限控制
   - 修复潜在的bug
```

### Comparing `nonebot_plugin_eventmonitor-0.1.8/setup.py` & `nonebot_plugin_eventmonitor-0.1.9/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools 
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="nonebot_plugin_eventmonitor",
-    version="0.1.8",
+    version="0.1.9",
     author="schwarzwald",
     description="监控群事件的插件，支持戳一戳，成员变动，群荣誉，运气王变化等提示",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/Reversedeer/nonebot_plugin_eventmonitor",
     project_urls={
         "Bug Tracker": "https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues",
```

