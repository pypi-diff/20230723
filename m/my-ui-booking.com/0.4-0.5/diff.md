# Comparing `tmp/my_ui_booking.com-0.4.tar.gz` & `tmp/my_ui_booking.com-0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "my_ui_booking.com-0.4.tar", last modified: Sun Jul 23 14:23:42 2023, max compression
+gzip compressed data, was "my_ui_booking.com-0.5.tar", last modified: Sun Jul 23 14:25:04 2023, max compression
```

## Comparing `my_ui_booking.com-0.4.tar` & `my_ui_booking.com-0.5.tar`

### file list

```diff
@@ -1,9 +1,13 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 14:23:42.878201 my_ui_booking.com-0.4/
--rw-rw-rw-   0        0        0      118 2023-07-23 14:23:42.878201 my_ui_booking.com-0.4/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-07-23 14:23:42.876067 my_ui_booking.com-0.4/my_ui_booking.com.egg-info/
--rw-rw-rw-   0        0        0      118 2023-07-23 14:23:42.000000 my_ui_booking.com-0.4/my_ui_booking.com.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      172 2023-07-23 14:23:42.000000 my_ui_booking.com-0.4/my_ui_booking.com.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 14:23:42.000000 my_ui_booking.com-0.4/my_ui_booking.com.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 14:23:42.000000 my_ui_booking.com-0.4/my_ui_booking.com.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 14:23:42.879347 my_ui_booking.com-0.4/setup.cfg
--rw-rw-rw-   0        0        0      163 2023-07-23 14:23:33.000000 my_ui_booking.com-0.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 14:25:04.686828 my_ui_booking.com-0.5/
+-rw-rw-rw-   0        0        0      118 2023-07-23 14:25:04.685831 my_ui_booking.com-0.5/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-07-23 14:25:04.650991 my_ui_booking.com-0.5/my_ui_booking/
+-rw-rw-rw-   0        0        0        0 2023-07-23 01:47:12.000000 my_ui_booking.com-0.5/my_ui_booking/__init__.py
+-rw-rw-rw-   0        0        0      564 2023-07-23 07:31:35.000000 my_ui_booking.com-0.5/my_ui_booking/booking.py
+-rw-rw-rw-   0        0        0       38 2023-07-23 07:13:57.000000 my_ui_booking.com-0.5/my_ui_booking/constants.py
+drwxrwxrwx   0        0        0        0 2023-07-23 14:25:04.684829 my_ui_booking.com-0.5/my_ui_booking.com.egg-info/
+-rw-rw-rw-   0        0        0      118 2023-07-23 14:25:04.000000 my_ui_booking.com-0.5/my_ui_booking.com.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      250 2023-07-23 14:25:04.000000 my_ui_booking.com-0.5/my_ui_booking.com.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 14:25:04.000000 my_ui_booking.com-0.5/my_ui_booking.com.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       14 2023-07-23 14:25:04.000000 my_ui_booking.com-0.5/my_ui_booking.com.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 14:25:04.686828 my_ui_booking.com-0.5/setup.cfg
+-rw-rw-rw-   0        0        0      163 2023-07-23 14:24:59.000000 my_ui_booking.com-0.5/setup.py
```

