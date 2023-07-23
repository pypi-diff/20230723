# Comparing `tmp/nonebot_plugin_eventmonitor-0.1.7.tar.gz` & `tmp/nonebot_plugin_eventmonitor-0.1.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_eventmonitor-0.1.7.tar", last modified: Fri Jul 21 15:08:47 2023, max compression
+gzip compressed data, was "nonebot_plugin_eventmonitor-0.1.8.tar", last modified: Sun Jul 23 13:48:22 2023, max compression
```

## Comparing `nonebot_plugin_eventmonitor-0.1.7.tar` & `nonebot_plugin_eventmonitor-0.1.8.tar`

### file list

```diff
@@ -1,18 +1,19 @@
-drwxrwxrwx   0        0        0        0 2023-07-21 15:08:47.975588 nonebot_plugin_eventmonitor-0.1.7/
--rw-rw-rw-   0        0        0    35149 2023-01-29 04:13:58.000000 nonebot_plugin_eventmonitor-0.1.7/LICENSE
--rw-rw-rw-   0        0        0     1478 2023-07-21 15:08:47.975588 nonebot_plugin_eventmonitor-0.1.7/PKG-INFO
--rw-rw-rw-   0        0        0      847 2023-07-21 15:01:10.000000 nonebot_plugin_eventmonitor-0.1.7/README.md
-drwxrwxrwx   0        0        0        0 2023-07-21 15:08:47.944874 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor/
--rw-rw-rw-   0        0        0     7158 2023-07-21 15:03:44.000000 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor/__init__.py
--rw-rw-rw-   0        0        0     1878 2023-07-21 09:06:43.000000 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor/admin.py
--rw-rw-rw-   0        0        0     1088 2023-07-21 09:06:47.000000 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor/honour.py
--rw-rw-rw-   0        0        0     2018 2023-07-21 14:45:01.000000 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor/stamp.py
--rw-rw-rw-   0        0        0     4903 2023-07-21 14:52:24.000000 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-21 15:08:47.974591 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor.egg-info/
--rw-rw-rw-   0        0        0     1478 2023-07-21 15:08:47.000000 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      469 2023-07-21 15:08:47.000000 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-21 15:08:47.000000 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       59 2023-07-21 15:08:47.000000 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor.egg-info/requires.txt
--rw-rw-rw-   0        0        0       28 2023-07-21 15:08:47.000000 nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-21 15:08:47.976587 nonebot_plugin_eventmonitor-0.1.7/setup.cfg
--rw-rw-rw-   0        0        0      993 2023-07-21 15:07:31.000000 nonebot_plugin_eventmonitor-0.1.7/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:48:22.364841 nonebot_plugin_eventmonitor-0.1.8/
+-rw-rw-rw-   0        0        0    35149 2023-01-29 04:13:58.000000 nonebot_plugin_eventmonitor-0.1.8/LICENSE
+-rw-rw-rw-   0        0        0     1601 2023-07-23 13:48:22.364841 nonebot_plugin_eventmonitor-0.1.8/PKG-INFO
+-rw-rw-rw-   0        0        0      970 2023-07-23 13:29:15.000000 nonebot_plugin_eventmonitor-0.1.8/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 13:48:22.351223 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/
+-rw-rw-rw-   0        0        0      734 2023-07-23 13:05:32.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/__init__.py
+-rw-rw-rw-   0        0        0     2823 2023-07-23 12:12:06.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/admin.py
+-rw-rw-rw-   0        0        0     7871 2023-07-23 12:32:13.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/handle.py
+-rw-rw-rw-   0        0        0     1621 2023-07-23 12:08:52.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/honour.py
+-rw-rw-rw-   0        0        0     2166 2023-07-23 12:34:54.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/stamp.py
+-rw-rw-rw-   0        0        0     7116 2023-07-23 13:05:35.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:48:22.364841 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/
+-rw-rw-rw-   0        0        0     1601 2023-07-23 13:48:22.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      507 2023-07-23 13:48:22.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 13:48:22.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       59 2023-07-23 13:48:22.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       28 2023-07-23 13:48:22.000000 nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 13:48:22.364841 nonebot_plugin_eventmonitor-0.1.8/setup.cfg
+-rw-rw-rw-   0        0        0      993 2023-07-23 13:06:41.000000 nonebot_plugin_eventmonitor-0.1.8/setup.py
```

### Comparing `nonebot_plugin_eventmonitor-0.1.7/LICENSE` & `nonebot_plugin_eventmonitor-0.1.8/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_eventmonitor-0.1.7/PKG-INFO` & `nonebot_plugin_eventmonitor-0.1.8/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,26 +1,29 @@
 Metadata-Version: 2.1
 Name: nonebot_plugin_eventmonitor
-Version: 0.1.7
+Version: 0.1.8
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
 
-- v0.1.7
+- v0.1.8
 
+  - 修复群文件不能检测(少写一个字母qwq)
+  - 增加功能开关指令：event状态/event配置 
+- v0.1.7
   - 新增所有功能开关[#issue5](https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues/9
   - 增加权限控制
   - 修复潜在的bug
 - v0.1.6
   - 修复bug
 - v0.1.5
   - 优化配置文件 [#issue4](https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues/6
```

### Comparing `nonebot_plugin_eventmonitor-0.1.7/README.md` & `nonebot_plugin_eventmonitor-0.1.8/README.md`

 * *Files 23% similar despite different names*

```diff
@@ -1,12 +1,15 @@
 <details>
     <summary><h2>更新日志</h2></summary>
 
-- v0.1.7
+- v0.1.8
 
+  - 修复群文件不能检测(少写一个字母qwq)
+  - 增加功能开关指令：event状态/event配置 
+- v0.1.7
   - 新增所有功能开关[#issue5](https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues/9
   - 增加权限控制
   - 修复潜在的bug
 - v0.1.6
   - 修复bug
 - v0.1.5
   - 优化配置文件 [#issue4](https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues/6
```

### Comparing `nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor/admin.py` & `nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/admin.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,44 +1,63 @@
 from datetime import datetime
 from .utils import superusers
 
 
 async def admin_changer(sub_type, user_id, bot_qq) : 
     admin_msg = ""
-
+    
+    # 根据管理员变动类型选择不同的消息
     if sub_type == "set":
+        # 如果用户ID等于机器人的QQ号，返回特定消息
         admin_msg = (
             "我也是管理啦，你们要小心喵~"
             if user_id == bot_qq
-            else f"🚔 管理员变动\n恭喜[CQ:at,qq={user_id}]喜提本群管理喵~"
+            else f"🚔 管理员变动\n恭喜@{user_id}喜提本群管理喵~"
         )
     elif sub_type == "unset":
+        # 如果用户ID等于机器人的QQ号，返回特定消息
         admin_msg = (
             "呜呜，别下咱管理呀QwQ，喵呜~"
             if user_id == bot_qq
-            else f"🚔 管理员变动\n[CQ:at,qq={user_id}]痛失本群管理喵~"
+            else f"🚔 管理员变动\n@{user_id}痛失本群管理喵~"
         )
+        
     return admin_msg
 
+
 async def del_user_bye(add_time, user_id):
     global del_user_msg
     del_time = datetime.fromtimestamp(add_time)
+    
+    # 检查用户ID是否在超级用户列表superusers中
     if user_id in superusers:
+        # 如果是超级用户，生成特定的离开消息
         del_user_msg = f"⌈{del_time}⌋\n@{user_id}恭送主人离开喵~"
         print(superusers)
     else:
-        del_user_msg = f"✈️ 成员变动⌈{del_time}⌋\nQQ号为：{user_id}的小可爱退群喵~" \
+        # 如果不是超级用户，生成通用的离开消息，包含用户的QQ号和头像图片
+        del_user_msg = f"✈️ 成员变动 ✈️ \n时间: ⌈{del_time}⌋\nQQ号为：{user_id}的小可爱退群喵~" \
                        f"[CQ:image,file=https://q4.qlogo.cn/headimg_dl?dst_uin={user_id}&spec=640]"
+                       
         return del_user_msg
 
+
 async def add_user_wecome(add_time, user_id, bot_qq):
-    global groups_all, add_user_msg
-    add_time = datetime.fromtimestamp(add_time)
+    global groups_all, add_user_msg   
+    # 将时间戳转换为datetime类型的时间add_time
+    add_time = datetime.fromtimestamp(add_time) 
+    # 判断用户ID是否等于机器人的QQ号
     if user_id == bot_qq:
+        # 如果是机器人自己加入群组，生成特定的欢迎消息
         add_user_msg = f"本喵被邀进入贵群喵~\n" \
                        f"火速上个管理喵~"
+    # 判断用户ID是否在超级用户列表superusers中
     elif user_id in superusers:
-        add_user_msg = f"✨ 成员变动 ✨\n@{user_id}[CQ:at,qq={user_id}]欢迎主人进群喵~[CQ:face,id=175]"
+        # 如果是超级用户加入群组，生成特定的欢迎消息，包含用户ID和CQ表情
+        add_user_msg = f"✨ 成员变动 ✨\n@{user_id}欢迎主人进群喵~[CQ:face,id=175]"
     else:
-        add_user_msg = f"✨ 成员变动 ✨\n欢迎[CQ:at,qq={user_id}]的加入喵~\n加入时间：⌈{add_time}⌋，请在群内积极发言喵~" \
+        # 如果是普通用户加入群组，生成通用的欢迎消息，包含用户ID、加入时间和用户头像图片的链接
+        add_user_msg = f"✨ 成员变动 ✨\n欢迎@{user_id}的加入喵~\n加入时间：⌈{add_time}⌋，请在群内积极发言喵~" \
                        f"[CQ:image,file=https://q4.qlogo.cn/headimg_dl?dst_uin={user_id}&spec=640]"
+    
     return add_user_msg
+
```

### Comparing `nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor/stamp.py` & `nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor/stamp.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,16 +1,18 @@
 import random
 from .utils import nickname
 
     
 async def chuo_send_msg():
-    rand_num = random.randint(0, len(chuo_msg) - 1)
+    # 使用 random.randint() 生成一个随机整数，作为选择消息的索引
+    rand_num = random.randint(0, len(chuo_msg) - 1)  
+    # 返回位于随机索引处的消息
     return chuo_msg[rand_num]
 
-
+#戳一戳文案
 chuo_msg = [
     f"别戳了，{nickname}怕疼QwQ",
     f"呜呜，再戳{nickname}脸都要肿了",
     f"戳坏了{nickname}，你赔得起吗？",
     f"再戳{nickname}，我要叫我主人了",
     f"别老戳{nickname}了，您歇会吧~",
     f"再戳{nickname}，咬你了嗷~",
```

### Comparing `nonebot_plugin_eventmonitor-0.1.7/nonebot_plugin_eventmonitor.egg-info/PKG-INFO` & `nonebot_plugin_eventmonitor-0.1.8/nonebot_plugin_eventmonitor.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,26 +1,29 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-eventmonitor
-Version: 0.1.7
+Version: 0.1.8
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
 
-- v0.1.7
+- v0.1.8
 
+  - 修复群文件不能检测(少写一个字母qwq)
+  - 增加功能开关指令：event状态/event配置 
+- v0.1.7
   - 新增所有功能开关[#issue5](https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues/9
   - 增加权限控制
   - 修复潜在的bug
 - v0.1.6
   - 修复bug
 - v0.1.5
   - 优化配置文件 [#issue4](https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues/6
```

### Comparing `nonebot_plugin_eventmonitor-0.1.7/setup.py` & `nonebot_plugin_eventmonitor-0.1.8/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools 
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="nonebot_plugin_eventmonitor",
-    version="0.1.7",
+    version="0.1.8",
     author="schwarzwald",
     description="监控群事件的插件，支持戳一戳，成员变动，群荣誉，运气王变化等提示",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/Reversedeer/nonebot_plugin_eventmonitor",
     project_urls={
         "Bug Tracker": "https://github.com/Reversedeer/nonebot_plugin_eventmonitor/issues",
```

