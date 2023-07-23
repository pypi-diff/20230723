# Comparing `tmp/nonebot_plugin_starrail_calendar-1.0.4.tar.gz` & `tmp/nonebot_plugin_starrail_calendar-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_starrail_calendar-1.0.4.tar", max compression
+gzip compressed data, was "nonebot_plugin_starrail_calendar-1.0.5.tar", max compression
```

## Comparing `nonebot_plugin_starrail_calendar-1.0.4.tar` & `nonebot_plugin_starrail_calendar-1.0.5.tar`

### file list

```diff
@@ -1,18 +1,14 @@
--rw-r--r--   0        0        0    35823 2022-05-26 22:27:12.688017 nonebot_plugin_starrail_calendar-1.0.4/LICENSE
--rw-r--r--   0        0        0       50 2023-05-09 12:28:29.877145 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/.idea/.gitignore
--rw-r--r--   0        0        0      273 2023-05-09 12:28:29.715697 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/.idea/misc.xml
--rw-r--r--   0        0        0      323 2023-05-09 12:28:29.696706 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/.idea/modules.xml
--rw-r--r--   0        0        0      344 2023-05-09 12:28:29.684758 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/.idea/nonebot_plugin_starrail_calendar.iml
--rw-r--r--   0        0        0      188 2023-05-09 12:28:29.729563 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/.idea/vcs.xml
--rw-r--r--   0        0        0     5550 2023-05-09 12:33:57.768042 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/__init__.py
--rw-r--r--   0        0        0     2387 2022-10-25 13:40:10.642123 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/browser.py
--rw-r--r--   0        0        0     4739 2023-05-02 02:09:58.604479 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/data_source.py
--rw-r--r--   0        0        0     1901 2023-05-02 03:04:38.808483 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/draw_calendar.py
--rw-r--r--   0        0        0     2371 2023-05-01 13:36:07.373205 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/calendar.html
--rw-r--r--   0        0        0     6882 2022-06-26 03:57:47.000000 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/index.css
--rw-r--r--   0        0        0   315626 2022-06-26 03:57:47.000000 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/iview.css
--rw-r--r--   0        0        0     6346 2022-06-26 03:57:47.000000 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/normalize.css
--rw-r--r--   0        0        0     2255 2023-04-29 01:27:19.441019 nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/utils.py
--rw-r--r--   0        0        0      546 2023-05-13 06:56:42.245245 nonebot_plugin_starrail_calendar-1.0.4/pyproject.toml
--rw-r--r--   0        0        0      596 2023-05-09 12:37:06.326249 nonebot_plugin_starrail_calendar-1.0.4/README.md
--rw-r--r--   0        0        0     1090 1970-01-01 00:00:00.000000 nonebot_plugin_starrail_calendar-1.0.4/PKG-INFO
+-rw-r--r--   0        0        0    35823 2022-05-26 22:27:12.688017 nonebot_plugin_starrail_calendar-1.0.5/LICENSE
+-rw-r--r--   0        0        0     5601 2023-07-23 04:22:45.835743 nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/__init__.py
+-rw-r--r--   0        0        0     2387 2022-10-25 13:40:10.642123 nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/browser.py
+-rw-r--r--   0        0        0      253 2023-05-14 14:40:54.472627 nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/config.py
+-rw-r--r--   0        0        0     4786 2023-07-23 04:20:12.757136 nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/data_source.py
+-rw-r--r--   0        0        0     1901 2023-05-02 03:04:38.808483 nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/draw_calendar.py
+-rw-r--r--   0        0        0     2371 2023-05-01 13:36:07.373205 nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/template/calendar.html
+-rw-r--r--   0        0        0     6882 2022-06-26 03:57:47.000000 nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/template/index.css
+-rw-r--r--   0        0        0   315626 2022-06-26 03:57:47.000000 nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/template/iview.css
+-rw-r--r--   0        0        0     6346 2022-06-26 03:57:47.000000 nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/template/normalize.css
+-rw-r--r--   0        0        0     2255 2023-04-29 01:27:19.441019 nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/utils.py
+-rw-r--r--   0        0        0      547 2023-07-23 04:26:48.376437 nonebot_plugin_starrail_calendar-1.0.5/pyproject.toml
+-rw-r--r--   0        0        0      596 2023-05-09 12:37:06.326249 nonebot_plugin_starrail_calendar-1.0.5/README.md
+-rw-r--r--   0        0        0     1091 1970-01-01 00:00:00.000000 nonebot_plugin_starrail_calendar-1.0.5/PKG-INFO
```

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/LICENSE` & `nonebot_plugin_starrail_calendar-1.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/__init__.py` & `nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,137 +1,134 @@
 import logging
 import nonebot
-import re
 
 from apscheduler.schedulers.asyncio import AsyncIOScheduler
 from nonebot import get_bot, on_command
 from nonebot.adapters.onebot.v11 import GroupMessageEvent, MessageEvent, Message, MessageSegment, ActionFailed
 from nonebot.params import CommandArg
 from nonebot.plugin import PluginMetadata
+from .config import *
 
 from .utils import *
 from .draw_calendar import *
 
 __plugin_meta__ = PluginMetadata(
     name="星穹铁道活动日历",
     description="查看《崩坏：星穹铁道》活动",
     usage="<星穹/星琼>日历",
     extra={
         'author':   'TonyKun',
-        'version':  '1.0',
+        'version':  '1.1',
         'priority': 24,
     }
 )
 
 driver = nonebot.get_driver()
 scheduler = AsyncIOScheduler()
-calendar = on_command('星穹日历', aliases={"星穹日历", '星琼日历'}, priority=24, block=True)
+calendar = on_command('星穹日历', aliases={"星穹日历", '星琼日历', '星铁日历', '崩铁日历'}, priority=24, block=True)
 
 
 @driver.on_startup
 async def _():
     scheduler.start()
     for group_id, group_data in load_data('data.json').items():
         scheduler.add_job(
             func=send_calendar,
             trigger='cron',
             hour=group_data['hour'],
             minute=group_data['minute'],
-            id="star_rali_calendar_" + group_id,
+            id="starrali_calendar_" + group_id,
             args=(group_id, group_data),
             misfire_grace_time=10
         )
 
 
 async def send_calendar(group_id, group_data):
-    im = await generate_day_schedule('cn')
-    if 'cardimage' not in group_data or not group_data['cardimage']:
-        msg = MessageSegment.image(im)
-
-    await get_bot().send_group_msg(group_id=int(group_id), message=msg)
+    im = await generate_day_schedule('cn', viewport={"width": config.width, "height": config.height})
+    await get_bot().send_group_msg(group_id=int(group_id), message=MessageSegment.image(im))
 
 
 def update_group_schedule(group_id, group_data):
     group_id = str(group_id)
     if group_id not in group_data:
         return
 
     scheduler.add_job(
         func=send_calendar,
         trigger='cron',
         args=(group_id, group_data),
-        id=f'star_rali_calendar_{group_id}',
+        id=f'starrali_calendar_{group_id}',
         replace_existing=True,
         hour=group_data[group_id]['hour'],
         minute=group_data[group_id]['minute'],
         misfire_grace_time=10
     )
 
 
 @calendar.handle()
 async def _(event: Union[GroupMessageEvent, MessageEvent], msg: Message = CommandArg()):
+    import re
     if event.message_type == 'private':
         await calendar.finish('仅支持群聊模式下使用本指令')
 
     group_id = str(event.group_id)
     group_data = load_data('data.json')
     server = 'cn'
     fun = msg.extract_plain_text().strip()
     action = re.search(r'(?P<action>on|off|time|status|cardimage)', fun)
     if not fun:
-        im = await generate_day_schedule(server, viewport={"width": 600, "height": 10})
+        im = await generate_day_schedule(server, viewport={"width": config.width, "height": config.height})
 
         try:
-            await calendar.finish(f'[CQ:cardimage,file={im}]')
+            await calendar.finish(MessageSegment.image(im))
         except ActionFailed as e:
             logging.error(e)
 
     elif action:
 
         # 添加定时推送任务
         if action.group('action') == 'on':
             group_data[group_id] = {
                 'server_list': [
                     str(server)
                 ],
                 'hour': 8,
                 'minute': 0,
-                'cardimage': False
             }
             if event.message_type == 'guild':
                 await calendar.finish("暂不支持频道内推送~")
 
-            if scheduler.get_job('star_rali_calendar_' + group_id):
-                scheduler.remove_job("star_rali_calendar_" + group_id)
+            if scheduler.get_job('starrali_calendar_' + group_id):
+                scheduler.remove_job("starrali_calendar_" + group_id)
             save_data(group_data, 'data.json')
 
             scheduler.add_job(
                 func=send_calendar,
                 trigger='cron',
                 hour=8,
                 minute=0,
-                id="star_rali_calendar_" + group_id,
+                id="starrali_calendar_" + group_id,
                 args=(group_id, group_data[group_id]),
                 misfire_grace_time=10
             )
 
             await calendar.finish('星穹日历推送已开启', at_sender=True)
 
         # 关闭推送功能
         elif action.group('action') == 'off':
             del group_data[group_id]
-            if scheduler.get_job("star_rali_calendar_" + group_id):
-                scheduler.remove_job("star_rali_calendar_" + group_id)
+            if scheduler.get_job("starrali_calendar_" + group_id):
+                scheduler.remove_job("starrali_calendar_" + group_id)
             save_data(group_data, 'data.json')
             await calendar.finish('星穹日历推送已关闭', at_sender=True)
 
         # 设置推送时间
         elif action.group('action') == 'time':
             match = str(msg).split(" ")
-            time = re.search(r'(\d{1,2}):(\d{2})', match[1])
+            time = re.search(r'(\d{1,2}):(\d{2})', match[1]) or re.search(r'(\d{1,2})：(\d{2})', match[1])
 
             if time:
                 if not time or len(time.groups()) < 2:
                     await calendar.finish("请指定推送时间", at_sender=True)
                 else:
                     group_data[group_id]['hour'] = int(time.group(1))
                     group_data[group_id]['minute'] = int(time.group(2))
```

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/browser.py` & `nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/browser.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/data_source.py` & `nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/data_source.py`

 * *Files 2% similar despite different names*

```diff
@@ -19,15 +19,18 @@
     'cn': asyncio.Lock(),
 }
 
 ignored_key_words = [
     '有奖问卷',
     '公平运营',
     '防沉迷',
-    '游戏优化'
+    '游戏优化',
+    '保密测试',
+    '社群',
+    '社媒聚合页'
 ]
 
 ignored_ann_ids = [
     '194',
     '185'
 ]
 
@@ -103,15 +106,15 @@
 
             event = {
                 'title': data['title'],
                 'banner': data['banner'],
                 'color': '#2196f3'
             }
 
-            if '活动跃迁开启' in data['title']:
+            if '概率UP' in data['title']:
                 event['color'] = '#73BF00'
                 event['banner'] = data['banner']
 
             if '无名勋礼' in data['title']:
                 event['color'] = '#F00078'
                 event['banner'] = data['banner']
```

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/draw_calendar.py` & `nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/draw_calendar.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/calendar.html` & `nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/template/calendar.html`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/index.css` & `nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/template/index.css`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/iview.css` & `nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/template/iview.css`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/template/normalize.css` & `nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/template/normalize.css`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/nonebot_plugin_starrail_calendar/utils.py` & `nonebot_plugin_starrail_calendar-1.0.5/nonebot_plugin_starrail_calendar/utils.py`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/pyproject.toml` & `nonebot_plugin_starrail_calendar-1.0.5/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 [tool.poetry]
 name = "nonebot-plugin-starrail-calendar"
-version = "1.0.4"
+version = "1.0.5"
 description = "查看《崩坏：星穹铁道》官方活动"
 authors = ["nicklly <1134741727@qq.com>"]
 readme = "README.md"
 packages = [{include = "nonebot_plugin_starrail_calendar"}]
 
 [tool.poetry.dependencies]
-python = "3.10.9"
+python = "3.10.11"
 nonebot2 = "2.0.0rc4"
 nonebot-adapter-onebot = "2.2.2"
 playwright = "1.32.1"
 httpx = "0.23.3"
 apscheduler = "3.10.1"
 jinja2 = "3.1.2"
```

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/README.md` & `nonebot_plugin_starrail_calendar-1.0.5/README.md`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_starrail_calendar-1.0.4/PKG-INFO` & `nonebot_plugin_starrail_calendar-1.0.5/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-starrail-calendar
-Version: 1.0.4
+Version: 1.0.5
 Summary: 查看《崩坏：星穹铁道》官方活动
 Author: nicklly
 Author-email: 1134741727@qq.com
-Requires-Python: ==3.10.9
+Requires-Python: ==3.10.11
 Classifier: Programming Language :: Python :: 3
 Requires-Dist: apscheduler (==3.10.1)
 Requires-Dist: httpx (==0.23.3)
 Requires-Dist: jinja2 (==3.1.2)
 Requires-Dist: nonebot-adapter-onebot (==2.2.2)
 Requires-Dist: nonebot2 (==2.0.0rc4)
 Requires-Dist: playwright (==1.32.1)
```

