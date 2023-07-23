# Comparing `tmp/ns_asphalt9-0.1.5.tar.gz` & `tmp/ns_asphalt9-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ns_asphalt9-0.1.5.tar", last modified: Fri Jul 14 17:51:28 2023, max compression
+gzip compressed data, was "ns_asphalt9-0.1.6.tar", last modified: Sun Jul 23 12:45:28 2023, max compression
```

## Comparing `ns_asphalt9-0.1.5.tar` & `ns_asphalt9-0.1.6.tar`

### file list

```diff
@@ -1,51 +1,50 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-14 17:51:28.660193 ns_asphalt9-0.1.5/
--rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      180 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     2020 2023-07-14 17:51:28.660193 ns_asphalt9-0.1.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1041 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-14 17:51:28.656193 ns_asphalt9-0.1.5/ns_asphalt9/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-14 17:51:28.660193 ns_asphalt9-0.1.5/ns_asphalt9/core/
--rw-r--r--   0 runner    (1001) docker     (123)       28 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-14 17:51:28.660193 ns_asphalt9-0.1.5/ns_asphalt9/core/actions/
--rw-r--r--   0 runner    (1001) docker     (123)      359 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/actions/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      589 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/actions/common.py
--rw-r--r--   0 runner    (1001) docker     (123)     4652 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/actions/enter_page.py
--rw-r--r--   0 runner    (1001) docker     (123)     4043 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/actions/process_race.py
--rw-r--r--   0 runner    (1001) docker     (123)     4339 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/actions/select_car.py
--rw-r--r--   0 runner    (1001) docker     (123)      706 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     2828 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/consts.py
--rw-r--r--   0 runner    (1001) docker     (123)     2146 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/controller.py
--rw-r--r--   0 runner    (1001) docker     (123)      671 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/globals.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-14 17:51:28.660193 ns_asphalt9-0.1.5/ns_asphalt9/core/gui/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/gui/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    23659 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/gui/app.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-14 17:51:28.660193 ns_asphalt9-0.1.5/ns_asphalt9/core/gui/images/
--rw-r--r--   0 runner    (1001) docker     (123)     3097 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/gui/images/help.png
--rw-r--r--   0 runner    (1001) docker     (123)     2900 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/gui/images/home.png
--rw-r--r--   0 runner    (1001) docker     (123)   202347 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/gui/images/logo.png
--rw-r--r--   0 runner    (1001) docker     (123)     3159 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/gui/images/settings.png
--rw-r--r--   0 runner    (1001) docker     (123)     1518 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/ocr.py
--rw-r--r--   0 runner    (1001) docker     (123)     1843 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/page_factory.py
--rw-r--r--   0 runner    (1001) docker     (123)    13412 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/pages.py
--rw-r--r--   0 runner    (1001) docker     (123)      265 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/screenshot.py
--rw-r--r--   0 runner    (1001) docker     (123)     2686 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/tasks.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-14 17:51:28.660193 ns_asphalt9-0.1.5/ns_asphalt9/core/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1016 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/utils/decorator.py
--rw-r--r--   0 runner    (1001) docker     (123)      459 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/utils/fetch_cars.py
--rw-r--r--   0 runner    (1001) docker     (123)     1360 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/utils/fetch_tracks.py
--rw-r--r--   0 runner    (1001) docker     (123)     1993 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/utils/log.py
--rw-r--r--   0 runner    (1001) docker     (123)      862 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/core/utils/timer.py
--rw-r--r--   0 runner    (1001) docker     (123)     5400 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/ns_asphalt9/main.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-14 17:51:28.656193 ns_asphalt9-0.1.5/ns_asphalt9.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2020 2023-07-14 17:51:28.000000 ns_asphalt9-0.1.5/ns_asphalt9.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1226 2023-07-14 17:51:28.000000 ns_asphalt9-0.1.5/ns_asphalt9.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-14 17:51:28.000000 ns_asphalt9-0.1.5/ns_asphalt9.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       54 2023-07-14 17:51:28.000000 ns_asphalt9-0.1.5/ns_asphalt9.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-14 17:51:28.000000 ns_asphalt9-0.1.5/ns_asphalt9.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      107 2023-07-14 17:51:28.000000 ns_asphalt9-0.1.5/ns_asphalt9.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-07-14 17:51:28.000000 ns_asphalt9-0.1.5/ns_asphalt9.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1299 2023-07-14 17:51:28.660193 ns_asphalt9-0.1.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      387 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-14 17:51:28.660193 ns_asphalt9-0.1.5/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     1204 2023-07-14 17:51:18.000000 ns_asphalt9-0.1.5/tests/test_ocr.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:45:28.817182 ns_asphalt9-0.1.6/
+-rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      180 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     2020 2023-07-23 12:45:28.817182 ns_asphalt9-0.1.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1041 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:45:28.813182 ns_asphalt9-0.1.6/ns_asphalt9/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:45:28.817182 ns_asphalt9-0.1.6/ns_asphalt9/core/
+-rw-r--r--   0 runner    (1001) docker     (123)       28 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:45:28.817182 ns_asphalt9-0.1.6/ns_asphalt9/core/actions/
+-rw-r--r--   0 runner    (1001) docker     (123)      425 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/actions/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1005 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/actions/common.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4650 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/actions/enter_page.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1160 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/actions/process_race.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4268 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/actions/select_car.py
+-rw-r--r--   0 runner    (1001) docker     (123)      706 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2895 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/consts.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2146 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/controller.py
+-rw-r--r--   0 runner    (1001) docker     (123)      831 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/globals.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:45:28.817182 ns_asphalt9-0.1.6/ns_asphalt9/core/gui/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/gui/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23659 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/gui/app.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:45:28.817182 ns_asphalt9-0.1.6/ns_asphalt9/core/gui/images/
+-rw-r--r--   0 runner    (1001) docker     (123)     3097 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/gui/images/help.png
+-rw-r--r--   0 runner    (1001) docker     (123)     2900 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/gui/images/home.png
+-rw-r--r--   0 runner    (1001) docker     (123)   202347 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/gui/images/logo.png
+-rw-r--r--   0 runner    (1001) docker     (123)     3159 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/gui/images/settings.png
+-rw-r--r--   0 runner    (1001) docker     (123)     3752 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/ocr.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1843 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/page_factory.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13896 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/pages.py
+-rw-r--r--   0 runner    (1001) docker     (123)      265 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/screenshot.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2779 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/tasks.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:45:28.817182 ns_asphalt9-0.1.6/ns_asphalt9/core/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1016 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/utils/decorator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1993 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/utils/log.py
+-rw-r--r--   0 runner    (1001) docker     (123)      862 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/utils/timer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29936 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/core/utils/track_data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5420 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/ns_asphalt9/main.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:45:28.813182 ns_asphalt9-0.1.6/ns_asphalt9.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2020 2023-07-23 12:45:28.000000 ns_asphalt9-0.1.6/ns_asphalt9.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1189 2023-07-23 12:45:28.000000 ns_asphalt9-0.1.6/ns_asphalt9.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 12:45:28.000000 ns_asphalt9-0.1.6/ns_asphalt9.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       54 2023-07-23 12:45:28.000000 ns_asphalt9-0.1.6/ns_asphalt9.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 12:45:28.000000 ns_asphalt9-0.1.6/ns_asphalt9.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      107 2023-07-23 12:45:28.000000 ns_asphalt9-0.1.6/ns_asphalt9.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-07-23 12:45:28.000000 ns_asphalt9-0.1.6/ns_asphalt9.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1299 2023-07-23 12:45:28.817182 ns_asphalt9-0.1.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      387 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:45:28.817182 ns_asphalt9-0.1.6/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      642 2023-07-23 12:45:15.000000 ns_asphalt9-0.1.6/tests/test_pages.py
```

### Comparing `ns_asphalt9-0.1.5/LICENSE` & `ns_asphalt9-0.1.6/LICENSE`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/PKG-INFO` & `ns_asphalt9-0.1.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ns_asphalt9
-Version: 0.1.5
+Version: 0.1.6
 Summary: Asphalt 9 daily task handling tool based on NXBT and V4L2.
 Home-page: https://pypi.python.org/pypi/ns_asphalt9
 Author: codehai
 Author-email: wmpksb@gmail.com
 License: GNU General Public License v3 (GPLv3)
 Project-URL: Code, https://github.com/codehai/ns_asphalt9
 Project-URL: Issue tracker, https://github.com/codehai/ns_asphalt9/issues
```

### Comparing `ns_asphalt9-0.1.5/README.md` & `ns_asphalt9-0.1.6/README.md`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/actions/common.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/actions/common.py`

 * *Files 27% similar despite different names*

```diff
@@ -6,14 +6,29 @@
 def connect_controller():
     """连接手柄"""
     pro.press_buttons([Buttons.L, Buttons.R], down=1)
     time.sleep(1)
     pro.press_buttons([Buttons.A], down=0.5)
 
 
+def restart():
+    """重启游戏"""
+    # 回到主页
+    pro.press_button(Buttons.HOME, 3)
+    # 切到第二个游戏
+    pro.press_button(Buttons.DPAD_RIGHT, 1)
+    # 按一下确认打开，再按一下确认关闭
+    pro.press_group([Buttons.A] * 2, 1)
+    pro.press_button(Buttons.B, 1)
+    # 回到A9
+    pro.press_button(Buttons.DPAD_LEFT, 1)
+    # 进入游戏
+    pro.press_group([Buttons.A] * 2, 2)
+
+
 def demoted():
     """降级"""
     globals.DIVISION = ""
     pro.press_button(Buttons.B, 3)
 
 
 def set_eng():
```

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/actions/enter_page.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/actions/enter_page.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import time
 
 from .. import consts, globals, tasks
 from ..controller import Buttons, pro
-from ..ocr import ocr_screen
+from ..ocr import OCR
 from ..utils.decorator import retry
 from ..utils.log import logger
 
 
 def enter_game():
     """进入游戏"""
     buttons = [
@@ -56,15 +56,15 @@
     pro.press_group([Buttons.ZL] * 4, 0.5)
     if mode == consts.mp2_zh:
         pro.press_group([Buttons.DPAD_DOWN], 0.5)
     if mode == consts.mp3_zh:
         pro.press_group([Buttons.DPAD_DOWN] * 2, 0.5)
     time.sleep(2)
     pro.press_group([Buttons.A], 2)
-    page = ocr_screen()
+    page = OCR.get_page()
     if in_series(page, mode):
         pass
     else:
         raise Exception(f"Failed to access {mode}, current page = {page.name}")
 
 
 def _enter_carhunt(page=None, mode=0):
@@ -85,22 +85,22 @@
     if page and page.name == page_name:
         return
     reset_to_career()
     pro.press_group([Buttons.ZL] * 5, 0.5)
     pro.press_group([Buttons.A], 2)
     pro.press_group([Buttons.ZR] * globals.CONFIG[config_key]["寻车位置"], 0.5)
     time.sleep(1)
-    page = ocr_screen()
+    page = OCR.get_page()
     if page.has_text(page_feature):
         pro.press_a()
     else:
         pro.press_group([Buttons.ZL] * 12, 0)
         for i in range(20):
             pro.press_group([Buttons.ZR], 0.5)
-            page = ocr_screen()
+            page = OCR.get_page()
             if page.has_text(page_feature):
                 globals.CONFIG[config_key]["寻车位置"] = i + 1
                 pro.press_a()
                 break
         else:
             raise Exception(f"Failed to access carhunt, current page = {page.name}")
 
@@ -122,22 +122,22 @@
     """领卡"""
     reset_to_career()
     pro.press_group([Buttons.DPAD_DOWN] * 3, 0.2)
     pro.press_group([Buttons.DPAD_LEFT] * 8, 0.2)
     pro.press_group([Buttons.A], 0.5)
     pro.press_group([Buttons.DPAD_UP], 0.5)
     pro.press_group([Buttons.A] * 2, 5)
-    page = ocr_screen()
+    page = OCR.get_page()
     if page.has_text("CLASSIC PACK.*POSSIBLE CONTENT"):
         pro.press_group([Buttons.A] * 3, 3)
         pro.press_group([Buttons.B], 0.5)
         tasks.TaskManager.set_done()
     else:
         raise Exception(f"Failed to access carhunt, current page = {page.name}")
-    
+
 
 @retry(max_attempts=3)
 def prix_pack():
     """大奖赛领卡"""
     reset_to_career()
     pro.press_group([Buttons.DPAD_DOWN] * 3, 0.2)
     pro.press_group([Buttons.DPAD_LEFT] * 6, 0.2)
@@ -145,17 +145,16 @@
     pro.press_group([Buttons.DPAD_UP] * 8, 0.2)
     if not globals.CONFIG["大奖赛"]["位置"]:
         logger.info("Please set grand prix position!")
         return
     pro.press_group([Buttons.DPAD_DOWN] * globals.CONFIG["大奖赛"]["位置"], 0.5)
     for _ in range(2):
         pro.press_group([Buttons.A], 5)
-        page = ocr_screen()
+        page = OCR.get_page()
         if page.name == consts.grand_prix:
             pro.press_group([Buttons.DPAD_LEFT] * 4, 0.2)
             pro.press_group([Buttons.DPAD_RIGHT], 0.2)
             pro.press_group([Buttons.A] * 3, 3)
             tasks.TaskManager.set_done()
             break
     else:
         raise Exception(f"Failed to access carhunt, current page = {page.name}")
-
```

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/actions/select_car.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/actions/select_car.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import time
 
 from .. import consts, globals, tasks
 from ..actions import process_race
 from ..controller import Buttons, pro
-from ..ocr import ocr_screen
+from ..ocr import OCR
 from ..utils.log import logger
 from ..tasks import TaskManager
 
 
 def world_series_reset():
     division = globals.DIVISION
     if not division:
@@ -48,17 +48,19 @@
 def world_series_positions():
     division = globals.DIVISION
     if not division:
         division = "青铜"
     config = globals.CONFIG["多人一"][division]
     return config["车库位置"]
 
+
 def mp3_position():
     return globals.CONFIG["多人三"]["车库位置"]
 
+
 def other_series_position():
     return globals.CONFIG["多人二"]["车库位置"]
 
 
 def carhunt_position():
     return globals.CONFIG["寻车"]["车库位置"]
 
@@ -76,70 +78,63 @@
         elif globals.CONFIG["模式"] == consts.mp2_zh:
             return other_series_position(), other_series_reset, consts.mp2_zh
         else:
             return world_series_positions(), world_series_reset, consts.mp1_zh
     elif mode == consts.car_hunt_zh:
         return carhunt_position(), carhunt_reset, mode
     elif mode == consts.legendary_hunt_zh:
-        return legendary_hunt_position(), carhunt_reset, mode        
+        return legendary_hunt_position(), carhunt_reset, mode
     else:
         return default_positions(), default_reset, mode
 
 
+def move_to_position(positions, reset, mode):
+    if globals.SELECT_COUNT[mode] >= len(positions):
+        globals.SELECT_COUNT[mode] = 0
+    if positions:
+        reset()
+        position = positions[globals.SELECT_COUNT[mode]]
+        logger.info(
+            f"Start try position = {position}, count = {globals.SELECT_COUNT[mode]}"
+        )
+        for i in range(position["row"] - 1):
+            pro.press_button(Buttons.DPAD_DOWN, 0)
+
+        for i in range(position["col"] - 1):
+            pro.press_button(Buttons.DPAD_RIGHT, 0)
+
+    time.sleep(2)
+
+
 def select_car():
     # 选车
     logger.info("Start select car.")
     while globals.G_RUN.is_set():
         positions, reset, mode = get_race_config()
-        reset()
-        if globals.SELECT_COUNT[mode] >= len(positions):
-            globals.SELECT_COUNT[mode] = 0
-        if positions:
-            position = positions[globals.SELECT_COUNT[mode]]
-            logger.info(f"Start try position = {position}, count = {globals.SELECT_COUNT[mode]}")
-            for i in range(position["row"] - 1):
-                pro.press_button(Buttons.DPAD_DOWN, 0)
-
-            for i in range(position["col"] - 1):
-                pro.press_button(Buttons.DPAD_RIGHT, 0)
-
-        time.sleep(2)
-
+        move_to_position(positions, reset, mode)
+        # 进入车辆详情页
         pro.press_group([Buttons.A], 2)
-
-        page = ocr_screen()
-
+        page = OCR.get_page()
         # 如果没有进到车辆详情页面, router到默认任务
         if page.name != consts.car_info:
             TaskManager.task_enter(globals.CONFIG["模式"], page)
             return
-
-        pro.press_group([Buttons.A], 2)
-
-        page = ocr_screen()
-
-        if page.name in [
-            consts.loading_race,
-            consts.searching,
-            consts.racing,
-            consts.loading_carhunt,
-        ]:
-            break
-        elif page.name == consts.tickets:
-            pro.press_button(Buttons.DPAD_DOWN, 2)
-            pro.press_a(2)
-            pro.press_b(2)
-            pro.press_a(2)
-        else:
-            if page.name == consts.car_info and page.has_text(
+        # 如果车辆详情页有段位信息，说明车库段位与实际段位不匹配
+        if  page.has_text(
                 "BRONZE|SILVER|GOLD|PLATINUM"
             ):
-                globals.DIVISION = ""
-            for i in range(2):
-                pro.press_b()
-                page = ocr_screen()
-                if page.name == consts.select_car:
-                    break
+            globals.DIVISION = ""
+        # 判断是否有play按钮
+        if not OCR.has_play(mode):
+            pro.press_b()
             globals.SELECT_COUNT[mode] += 1
             continue
+        # 判断寻车是否有票
+        if mode in [consts.car_hunt_zh, consts.legendary_hunt_zh] and OCR.get_ticket() == 0:
+            pro.press_a(2)
+            pro.press_button(Buttons.DPAD_DOWN, 2)
+            pro.press_a(2)
+            pro.press_b(2)
+        pro.press_a(2)
+        break
     process_race()
     tasks.TaskManager.set_done()
```

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/cache.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/cache.py`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/consts.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/consts.py`

 * *Files 3% similar despite different names*

```diff
@@ -75,14 +75,18 @@
 no_opponents = "no_opponents"
 # 生涯
 career = "career"
 # 大奖赛
 grand_prix = "grand_prix"
 # 通行证页
 legend_pass = "legend_pass"
+# 无多人
+no_mp = "no_mp"
+# error code
+error_code = "error_code"
 
 
 # 键盘与手柄映射
 KEY_MAPPING = {
     "6": "MINUS",
     "7": "PLUS",
     "[": "CAPTURE",
```

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/controller.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/controller.py`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/globals.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/globals.py`

 * *Files 22% similar despite different names*

```diff
@@ -35,12 +35,21 @@
 
 # 选车次数
 SELECT_COUNT = {
     consts.mp1_zh: 0,
     consts.mp2_zh: 0,
     consts.mp3_zh: 0,
     consts.car_hunt_zh: 0,
-    consts.legendary_hunt_zh: 0
+    consts.legendary_hunt_zh: 0,
+}
+
+# 比赛次数
+RACE_COUNT = {
+    consts.mp1_zh: 0,
+    consts.mp2_zh: 0,
+    consts.mp3_zh: 0,
+    consts.car_hunt_zh: 0,
+    consts.legendary_hunt_zh: 0,
 }
 
 # 比赛中
 RACING = 0
```

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/gui/app.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/gui/app.py`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/gui/images/help.png` & `ns_asphalt9-0.1.6/ns_asphalt9/core/gui/images/help.png`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/gui/images/home.png` & `ns_asphalt9-0.1.6/ns_asphalt9/core/gui/images/home.png`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/gui/images/logo.png` & `ns_asphalt9-0.1.6/ns_asphalt9/core/gui/images/logo.png`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/gui/images/settings.png` & `ns_asphalt9-0.1.6/ns_asphalt9/core/gui/images/settings.png`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/page_factory.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/page_factory.py`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/pages.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/pages.py`

 * *Files 2% similar despite different names*

```diff
@@ -35,15 +35,16 @@
             consts.world_series,
             consts.searching,
             consts.loading_race,
         ]:
             self.division = consts.divisions_zh.get(divisions[0], "")
 
         modes = re.findall(
-            "LEGENDARY HUNT|CAR HUNT|WORLD SERIES|LIMITED SERIES|TRIAL SERIES", self.text
+            "LEGENDARY HUNT|CAR HUNT|WORLD SERIES|LIMITED SERIES|TRIAL SERIES",
+            self.text,
         )
         if modes and self.name not in [consts.multi_player]:
             self.mode = consts.modes_zh.get(modes[0], "")
             if self.mode == consts.car_hunt_zh:
                 hunt_cars = re.findall("APEX AP-0", self.text)
                 if hunt_cars:
                     self.hunt_car = hunt_cars[0]
@@ -336,14 +337,25 @@
     feature = "NO CONNECTION"
     part_match = False
     action = staticmethod(pro.press_button)
     args = (Buttons.B,)
 
 
 @cache_decorator("page")
+class ErrorCdoe(Page):
+    """Error Code: 2124-8028"""
+
+    name = consts.error_code
+    feature = "Error Code"
+    part_match = False
+    action = staticmethod(pro.press_button)
+    args = (Buttons.A,)
+
+
+@cache_decorator("page")
 class ClubReward(Page):
     """俱乐部奖励"""
 
     name = consts.club_reward
     feature = "YOUR CLUB ACHIEVED"
     part_match = False
 
@@ -581,7 +593,18 @@
         match_count = len(re.findall(cls.feature, text))
         if match_count:
             if "ENDS IN" in text:
                 match_count = 0
             else:
                 match_count = 10
         return match_count
+
+
+@cache_decorator("page")
+class NoMP(Page):
+    """无多人任务(大概率是网络问题)"""
+
+    name = consts.no_mp
+    feature = "NEW MULTIPLAYER SERIES.*COMING SOON"
+    part_match = False
+
+    action = staticmethod(actions.restart)
```

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/tasks.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/tasks.py`

 * *Files 8% similar despite different names*

```diff
@@ -29,28 +29,33 @@
         timer = threading.Timer(
             duration * 60, cls.task_producer, (task, duration), {"skiped": skiped}
         )
         timer.start()
         return timer
 
     @classmethod
+    def destroy(cls):
+        for t in cls.timers:
+            t.cancel()
+
+    @classmethod
     def task_dispatch(cls, page) -> None:
         if "任务" not in globals.CONFIG:
             return False
 
         if page.name not in [
             consts.world_series,
             consts.limited_series,
             consts.trial_series,
             consts.carhunt,
             consts.card_pack,
             consts.legend_pass,
             consts.legendary_hunt,
             consts.daily_events,
-            consts.multi_player
+            consts.multi_player,
         ]:
             return False
 
         if globals.task_queue.empty():
             if cls.status == consts.TaskStatus.done:
                 cls.task_enter(globals.CONFIG["模式"], page=page)
                 cls.status = consts.TaskStatus.default
```

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/utils/decorator.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/utils/decorator.py`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/utils/log.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/utils/log.py`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/core/utils/timer.py` & `ns_asphalt9-0.1.6/ns_asphalt9/core/utils/timer.py`

 * *Files identical despite different names*

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9/main.py` & `ns_asphalt9-0.1.6/ns_asphalt9/main.py`

 * *Files 5% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 import traceback
 import types
 
 from .core import consts
 from .core import globals as G
 from .core.controller import Buttons, pro
 from .core.gui.app import App
-from .core.ocr import ocr_screen
+from .core.ocr import OCR
 from .core.pages import Page
 from .core.screenshot import screenshot
 from .core.tasks import TaskManager
 from .core.utils.log import logger
 
 
 def process_screen(page: Page):
@@ -43,29 +43,30 @@
 
 
 def event_loop():
     TaskManager.task_init()
 
     while G.G_RACE_RUN_EVENT.is_set() and G.G_RUN.is_set():
         try:
-            page = ocr_screen()
+            page = OCR.get_page()
             if page.division:
                 G.DIVISION = page.division
             if page.mode:
                 G.MODE = page.mode
             dispatched = TaskManager.task_dispatch(page)
             if not dispatched:
                 process_screen(page)
             time.sleep(3)
         except Exception as err:
             # filename = capture()
             logger.error(
                 f"Caught exception, err = {err}, traceback = {traceback.format_exc()}"
             )
 
+    TaskManager.destroy()
     G.G_RACE_QUIT_EVENT.set()
 
 
 def command_input(queue):
     while G.G_RUN.is_set():
         command = queue.get()
 
@@ -163,15 +164,14 @@
     G.G_RUN.clear()
     logger.info(f"G_RUN state {G.G_RUN.is_set()}")
     G.output_queue.put("Quit App.")
     app.destroy()
 
 
 def init_config():
-
     parser = argparse.ArgumentParser(description="NS Asphalt9 Tool.")
     parser.add_argument("-c", "--config", type=str, default="settings", help="自定义配置文件")
     args = parser.parse_args()
     return args.config
 
 
 def main():
```

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9.egg-info/PKG-INFO` & `ns_asphalt9-0.1.6/ns_asphalt9.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ns-asphalt9
-Version: 0.1.5
+Version: 0.1.6
 Summary: Asphalt 9 daily task handling tool based on NXBT and V4L2.
 Home-page: https://pypi.python.org/pypi/ns_asphalt9
 Author: codehai
 Author-email: wmpksb@gmail.com
 License: GNU General Public License v3 (GPLv3)
 Project-URL: Code, https://github.com/codehai/ns_asphalt9
 Project-URL: Issue tracker, https://github.com/codehai/ns_asphalt9/issues
```

### Comparing `ns_asphalt9-0.1.5/ns_asphalt9.egg-info/SOURCES.txt` & `ns_asphalt9-0.1.6/ns_asphalt9.egg-info/SOURCES.txt`

 * *Files 6% similar despite different names*

```diff
@@ -30,12 +30,11 @@
 ns_asphalt9/core/gui/app.py
 ns_asphalt9/core/gui/images/help.png
 ns_asphalt9/core/gui/images/home.png
 ns_asphalt9/core/gui/images/logo.png
 ns_asphalt9/core/gui/images/settings.png
 ns_asphalt9/core/utils/__init__.py
 ns_asphalt9/core/utils/decorator.py
-ns_asphalt9/core/utils/fetch_cars.py
-ns_asphalt9/core/utils/fetch_tracks.py
 ns_asphalt9/core/utils/log.py
 ns_asphalt9/core/utils/timer.py
-tests/test_ocr.py
+ns_asphalt9/core/utils/track_data.py
+tests/test_pages.py
```

### Comparing `ns_asphalt9-0.1.5/setup.cfg` & `ns_asphalt9-0.1.6/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = nxbt
-version = 0.1.5
+version = 0.1.6
 author = codehai
 author-email = wmpksb@gmail.com
 project_urls = 
 	Code = https://github.com/codehai/ns_asphalt9
 	Issue tracker = https://github.com/codehai/ns_asphalt9/issues
 license = GNU General Public License v3 (GPLv3)
 license-file = LICENSE
```

