# Comparing `tmp/ex4nicegui-0.2.4.tar.gz` & `tmp/ex4nicegui-0.2.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ex4nicegui-0.2.4.tar", last modified: Fri Jul 21 14:32:53 2023, max compression
+gzip compressed data, was "ex4nicegui-0.2.5.tar", last modified: Sun Jul 23 07:22:38 2023, max compression
```

## Comparing `ex4nicegui-0.2.4.tar` & `ex4nicegui-0.2.5.tar`

### file list

```diff
@@ -1,70 +1,70 @@
-drwxrwxrwx   0        0        0        0 2023-07-21 14:32:53.595405 ex4nicegui-0.2.4/
--rw-rw-rw-   0        0        0     1094 2023-06-30 08:17:10.000000 ex4nicegui-0.2.4/LICENSE
--rw-rw-rw-   0        0        0      481 2023-07-21 14:32:53.592416 ex4nicegui-0.2.4/PKG-INFO
--rw-rw-rw-   0        0        0     2200 2023-07-10 15:25:21.000000 ex4nicegui-0.2.4/README.md
-drwxrwxrwx   0        0        0        0 2023-07-21 14:32:53.452379 ex4nicegui-0.2.4/ex4nicegui/
--rw-rw-rw-   0        0        0      337 2023-07-21 14:32:32.000000 ex4nicegui-0.2.4/ex4nicegui/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-21 14:32:53.470331 ex4nicegui-0.2.4/ex4nicegui/layout/
--rw-rw-rw-   0        0        0       31 2023-07-05 06:10:00.000000 ex4nicegui-0.2.4/ex4nicegui/layout/__init__.py
--rw-rw-rw-   0        0        0     2378 2023-07-05 06:10:00.000000 ex4nicegui-0.2.4/ex4nicegui/layout/gridbox.py
-drwxrwxrwx   0        0        0        0 2023-07-21 14:32:53.485291 ex4nicegui-0.2.4/ex4nicegui/reactive/
-drwxrwxrwx   0        0        0        0 2023-07-21 14:32:53.496261 ex4nicegui-0.2.4/ex4nicegui/reactive/ECharts/
--rw-rw-rw-   0        0        0  1581614 2023-07-17 15:29:41.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/ECharts/ECharts.js
--rw-rw-rw-   0        0        0     2550 2023-07-17 16:36:22.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/ECharts/ECharts.py
--rw-rw-rw-   0        0        0        0 2023-07-05 06:10:00.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/ECharts/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-21 14:32:53.502246 ex4nicegui-0.2.4/ex4nicegui/reactive/UseDraggable/
--rw-rw-rw-   0        0        0     4857 2023-07-17 16:36:22.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/UseDraggable/UseDraggable.js
--rw-rw-rw-   0        0        0     2888 2023-07-17 16:36:22.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/UseDraggable/UseDraggable.py
--rw-rw-rw-   0        0        0        0 2023-07-17 16:36:22.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/UseDraggable/__init__.py
--rw-rw-rw-   0        0        0      366 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/__index.py
--rw-rw-rw-   0        0        0       24 2023-07-05 06:10:00.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/__init__.py
--rw-rw-rw-   0        0        0     1356 2023-07-16 10:54:22.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/drawer.py
--rw-rw-rw-   0        0        0     6093 2023-07-16 10:54:22.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/local_file_picker.py
-drwxrwxrwx   0        0        0        0 2023-07-21 14:32:53.568478 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/
--rw-rw-rw-   0        0        0     1330 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/__init__.py
--rw-rw-rw-   0        0        0     2345 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/aggrid.py
--rw-rw-rw-   0        0        0     4292 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/base.py
--rw-rw-rw-   0        0        0     2250 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/button.py
--rw-rw-rw-   0        0        0     1275 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/card.py
--rw-rw-rw-   0        0        0     1769 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/checkbox.py
--rw-rw-rw-   0        0        0     2729 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/color_picker.py
--rw-rw-rw-   0        0        0     2700 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/date.py
--rw-rw-rw-   0        0        0     2443 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/drawer.py
--rw-rw-rw-   0        0        0     1783 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/echarts.py
--rw-rw-rw-   0        0        0     1687 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/html.py
--rw-rw-rw-   0        0        0     1600 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/icon.py
--rw-rw-rw-   0        0        0     1440 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/image.py
--rw-rw-rw-   0        0        0     3337 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/input.py
--rw-rw-rw-   0        0        0     1756 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/label.py
--rw-rw-rw-   0        0        0     2080 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/radio.py
--rw-rw-rw-   0        0        0      404 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/row.py
--rw-rw-rw-   0        0        0     2482 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/select.py
--rw-rw-rw-   0        0        0     2601 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/slider.py
--rw-rw-rw-   0        0        0     1979 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/switch.py
--rw-rw-rw-   0        0        0     3903 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/table.py
--rw-rw-rw-   0        0        0     2728 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/textarea.py
--rw-rw-rw-   0        0        0     2337 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/upload.py
--rw-rw-rw-   0        0        0      205 2023-07-21 14:29:40.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/officials/utils.py
--rw-rw-rw-   0        0        0     1217 2023-07-16 10:54:22.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/q_pagination.py
--rw-rw-rw-   0        0        0       24 2023-07-09 14:56:08.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/rxui.py
-drwxrwxrwx   0        0        0        0 2023-07-21 14:32:53.577457 ex4nicegui-0.2.4/ex4nicegui/reactive/useMouse/
--rw-rw-rw-   0        0        0     2722 2023-07-17 15:14:14.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/useMouse/UseMouse.js
--rw-rw-rw-   0        0        0     2580 2023-07-17 16:36:22.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/useMouse/UseMouse.py
--rw-rw-rw-   0        0        0        0 2023-07-08 17:55:18.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/useMouse/__init__.py
--rw-rw-rw-   0        0        0     2468 2023-07-19 08:10:43.000000 ex4nicegui-0.2.4/ex4nicegui/reactive/usePagination.py
-drwxrwxrwx   0        0        0        0 2023-07-21 14:32:53.582442 ex4nicegui-0.2.4/ex4nicegui/tools/
--rw-rw-rw-   0        0        0       40 2023-07-08 17:55:18.000000 ex4nicegui-0.2.4/ex4nicegui/tools/__init__.py
--rw-rw-rw-   0        0        0     4887 2023-07-10 13:40:51.000000 ex4nicegui-0.2.4/ex4nicegui/tools/debug.py
-drwxrwxrwx   0        0        0        0 2023-07-21 14:32:53.589421 ex4nicegui-0.2.4/ex4nicegui/utils/
--rw-rw-rw-   0        0        0        0 2023-07-05 06:10:00.000000 ex4nicegui-0.2.4/ex4nicegui/utils/__init__.py
--rw-rw-rw-   0        0        0      430 2023-07-08 17:55:18.000000 ex4nicegui-0.2.4/ex4nicegui/utils/common.py
--rw-rw-rw-   0        0        0     4807 2023-07-10 14:31:39.000000 ex4nicegui-0.2.4/ex4nicegui/utils/signals.py
-drwxrwxrwx   0        0        0        0 2023-07-21 14:32:53.466342 ex4nicegui-0.2.4/ex4nicegui.egg-info/
--rw-rw-rw-   0        0        0      481 2023-07-21 14:32:52.000000 ex4nicegui-0.2.4/ex4nicegui.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     2022 2023-07-21 14:32:53.000000 ex4nicegui-0.2.4/ex4nicegui.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-21 14:32:52.000000 ex4nicegui-0.2.4/ex4nicegui.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-07-21 14:32:52.000000 ex4nicegui-0.2.4/ex4nicegui.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       46 2023-07-21 14:32:52.000000 ex4nicegui-0.2.4/ex4nicegui.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-07-21 14:32:52.000000 ex4nicegui-0.2.4/ex4nicegui.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-21 14:32:53.595405 ex4nicegui-0.2.4/setup.cfg
--rw-rw-rw-   0        0        0     1501 2023-07-18 10:52:21.000000 ex4nicegui-0.2.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:22:38.136046 ex4nicegui-0.2.5/
+-rw-rw-rw-   0        0        0     1094 2023-06-30 08:17:10.000000 ex4nicegui-0.2.5/LICENSE
+-rw-rw-rw-   0        0        0      481 2023-07-23 07:22:38.135048 ex4nicegui-0.2.5/PKG-INFO
+-rw-rw-rw-   0        0        0     2200 2023-07-10 15:25:21.000000 ex4nicegui-0.2.5/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 07:22:38.027824 ex4nicegui-0.2.5/ex4nicegui/
+-rw-rw-rw-   0        0        0      337 2023-07-23 07:09:38.000000 ex4nicegui-0.2.5/ex4nicegui/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:22:38.042784 ex4nicegui-0.2.5/ex4nicegui/layout/
+-rw-rw-rw-   0        0        0       31 2023-07-05 06:10:00.000000 ex4nicegui-0.2.5/ex4nicegui/layout/__init__.py
+-rw-rw-rw-   0        0        0     2378 2023-07-05 06:10:00.000000 ex4nicegui-0.2.5/ex4nicegui/layout/gridbox.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:22:38.057744 ex4nicegui-0.2.5/ex4nicegui/reactive/
+drwxrwxrwx   0        0        0        0 2023-07-23 07:22:38.066721 ex4nicegui-0.2.5/ex4nicegui/reactive/ECharts/
+-rw-rw-rw-   0        0        0  1581614 2023-07-17 15:29:41.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/ECharts/ECharts.js
+-rw-rw-rw-   0        0        0     2550 2023-07-17 16:36:22.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/ECharts/ECharts.py
+-rw-rw-rw-   0        0        0        0 2023-07-05 06:10:00.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/ECharts/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:22:38.072705 ex4nicegui-0.2.5/ex4nicegui/reactive/UseDraggable/
+-rw-rw-rw-   0        0        0     4857 2023-07-23 07:06:08.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/UseDraggable/UseDraggable.js
+-rw-rw-rw-   0        0        0     2888 2023-07-23 06:34:34.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/UseDraggable/UseDraggable.py
+-rw-rw-rw-   0        0        0        0 2023-07-17 16:36:22.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/UseDraggable/__init__.py
+-rw-rw-rw-   0        0        0      366 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/__index.py
+-rw-rw-rw-   0        0        0       24 2023-07-05 06:10:00.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/__init__.py
+-rw-rw-rw-   0        0        0     1356 2023-07-16 10:54:22.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/drawer.py
+-rw-rw-rw-   0        0        0     6093 2023-07-16 10:54:22.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/local_file_picker.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:22:38.118094 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/
+-rw-rw-rw-   0        0        0     1330 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/__init__.py
+-rw-rw-rw-   0        0        0     2345 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/aggrid.py
+-rw-rw-rw-   0        0        0     4292 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/base.py
+-rw-rw-rw-   0        0        0     2250 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/button.py
+-rw-rw-rw-   0        0        0     1275 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/card.py
+-rw-rw-rw-   0        0        0     1769 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/checkbox.py
+-rw-rw-rw-   0        0        0     2744 2023-07-23 07:09:38.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/color_picker.py
+-rw-rw-rw-   0        0        0     2700 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/date.py
+-rw-rw-rw-   0        0        0     2443 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/drawer.py
+-rw-rw-rw-   0        0        0     1783 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/echarts.py
+-rw-rw-rw-   0        0        0     1687 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/html.py
+-rw-rw-rw-   0        0        0     1600 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/icon.py
+-rw-rw-rw-   0        0        0     1440 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/image.py
+-rw-rw-rw-   0        0        0     3337 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/input.py
+-rw-rw-rw-   0        0        0     1756 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/label.py
+-rw-rw-rw-   0        0        0     2080 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/radio.py
+-rw-rw-rw-   0        0        0      404 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/row.py
+-rw-rw-rw-   0        0        0     2482 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/select.py
+-rw-rw-rw-   0        0        0     2607 2023-07-23 07:09:38.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/slider.py
+-rw-rw-rw-   0        0        0     1979 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/switch.py
+-rw-rw-rw-   0        0        0     3903 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/table.py
+-rw-rw-rw-   0        0        0     2728 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/textarea.py
+-rw-rw-rw-   0        0        0     2337 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/upload.py
+-rw-rw-rw-   0        0        0      205 2023-07-21 14:29:40.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/officials/utils.py
+-rw-rw-rw-   0        0        0     1217 2023-07-16 10:54:22.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/q_pagination.py
+-rw-rw-rw-   0        0        0       24 2023-07-09 14:56:08.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/rxui.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:22:38.124076 ex4nicegui-0.2.5/ex4nicegui/reactive/useMouse/
+-rw-rw-rw-   0        0        0     2722 2023-07-17 15:14:14.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/useMouse/UseMouse.js
+-rw-rw-rw-   0        0        0     2580 2023-07-17 16:36:22.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/useMouse/UseMouse.py
+-rw-rw-rw-   0        0        0        0 2023-07-08 17:55:18.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/useMouse/__init__.py
+-rw-rw-rw-   0        0        0     2468 2023-07-19 08:10:43.000000 ex4nicegui-0.2.5/ex4nicegui/reactive/usePagination.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:22:38.127068 ex4nicegui-0.2.5/ex4nicegui/tools/
+-rw-rw-rw-   0        0        0       40 2023-07-08 17:55:18.000000 ex4nicegui-0.2.5/ex4nicegui/tools/__init__.py
+-rw-rw-rw-   0        0        0     4887 2023-07-10 13:40:51.000000 ex4nicegui-0.2.5/ex4nicegui/tools/debug.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:22:38.133052 ex4nicegui-0.2.5/ex4nicegui/utils/
+-rw-rw-rw-   0        0        0        0 2023-07-05 06:10:00.000000 ex4nicegui-0.2.5/ex4nicegui/utils/__init__.py
+-rw-rw-rw-   0        0        0      430 2023-07-08 17:55:18.000000 ex4nicegui-0.2.5/ex4nicegui/utils/common.py
+-rw-rw-rw-   0        0        0     4807 2023-07-10 14:31:39.000000 ex4nicegui-0.2.5/ex4nicegui/utils/signals.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:22:38.039794 ex4nicegui-0.2.5/ex4nicegui.egg-info/
+-rw-rw-rw-   0        0        0      481 2023-07-23 07:22:37.000000 ex4nicegui-0.2.5/ex4nicegui.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     2022 2023-07-23 07:22:37.000000 ex4nicegui-0.2.5/ex4nicegui.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 07:22:37.000000 ex4nicegui-0.2.5/ex4nicegui.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-07-23 07:22:37.000000 ex4nicegui-0.2.5/ex4nicegui.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       46 2023-07-23 07:22:37.000000 ex4nicegui-0.2.5/ex4nicegui.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 07:22:37.000000 ex4nicegui-0.2.5/ex4nicegui.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 07:22:38.137043 ex4nicegui-0.2.5/setup.cfg
+-rw-rw-rw-   0        0        0     1501 2023-07-18 10:52:21.000000 ex4nicegui-0.2.5/setup.py
```

### Comparing `ex4nicegui-0.2.4/LICENSE` & `ex4nicegui-0.2.5/LICENSE`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/README.md` & `ex4nicegui-0.2.5/README.md`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/layout/gridbox.py` & `ex4nicegui-0.2.5/ex4nicegui/layout/gridbox.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/ECharts/ECharts.js` & `ex4nicegui-0.2.5/ex4nicegui/reactive/ECharts/ECharts.js`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/ECharts/ECharts.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/ECharts/ECharts.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/UseDraggable/UseDraggable.js` & `ex4nicegui-0.2.5/ex4nicegui/reactive/UseDraggable/UseDraggable.js`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/UseDraggable/UseDraggable.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/UseDraggable/UseDraggable.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/drawer.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/drawer.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/local_file_picker.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/local_file_picker.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/__init__.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/__init__.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/aggrid.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/aggrid.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/base.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/base.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/button.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/button.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/card.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/card.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/checkbox.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/checkbox.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/color_picker.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/color_picker.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from typing import (
     Any,
     Callable,
     Optional,
+    Union,
 )
 from signe import effect
 from ex4nicegui.utils.signals import (
     ReadonlyRef,
     is_ref,
     _TMaybeRef as TMaybeRef,
 )
@@ -78,15 +79,15 @@
 
 
 class ColorPickerLazyBindableUi(ColorPickerBindableUi):
     def __init__(
         self,
         color: TMaybeRef[str] = "",
         *,
-        on_pick: Callable[..., Any] | None = None,
+        on_pick: Optional[Callable[..., Any]] = None,
         value: TMaybeRef[bool] = False,
     ) -> None:
         super().__init__(color, on_pick=on_pick, value=value)
 
     def _ex_setup(self):
         ele = self._element_picker
```

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/date.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/date.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/drawer.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/drawer.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/echarts.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/echarts.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/html.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/html.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/icon.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/icon.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/image.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/image.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/input.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/input.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/label.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/label.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/radio.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/radio.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/select.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/select.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/slider.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/slider.py`

 * *Files 5% similar despite different names*

```diff
@@ -75,16 +75,16 @@
 
 class LazySliderBindableUi(SliderBindableUi):
     def __init__(
         self,
         min: TMaybeRef[_TSliderValue],
         max: TMaybeRef[_TSliderValue],
         step: TMaybeRef[_TSliderValue] = 1,
-        value: TMaybeRef[_TSliderValue | None] = None,
-        on_change: Callable[..., Any] | None = None,
+        value: Optional[TMaybeRef[_TSliderValue]] = None,
+        on_change: Optional[Callable[..., Any]] = None,
     ) -> None:
         super().__init__(min, max, step, value, on_change)
 
     def _ex_setup(self):
         ele = self.element
 
         @effect
```

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/switch.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/switch.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/table.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/table.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/textarea.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/textarea.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/officials/upload.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/officials/upload.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/q_pagination.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/q_pagination.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/useMouse/UseMouse.js` & `ex4nicegui-0.2.5/ex4nicegui/reactive/useMouse/UseMouse.js`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/useMouse/UseMouse.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/useMouse/UseMouse.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/reactive/usePagination.py` & `ex4nicegui-0.2.5/ex4nicegui/reactive/usePagination.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/tools/debug.py` & `ex4nicegui-0.2.5/ex4nicegui/tools/debug.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui/utils/signals.py` & `ex4nicegui-0.2.5/ex4nicegui/utils/signals.py`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/ex4nicegui.egg-info/SOURCES.txt` & `ex4nicegui-0.2.5/ex4nicegui.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `ex4nicegui-0.2.4/setup.py` & `ex4nicegui-0.2.5/setup.py`

 * *Files identical despite different names*

