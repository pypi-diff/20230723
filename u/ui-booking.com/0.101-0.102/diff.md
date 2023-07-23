# Comparing `tmp/ui_booking.com-0.101.tar.gz` & `tmp/ui_booking.com-0.102.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ui_booking.com-0.101.tar", last modified: Sun Jul 23 11:41:37 2023, max compression
+gzip compressed data, was "ui_booking.com-0.102.tar", last modified: Sun Jul 23 11:45:02 2023, max compression
```

## Comparing `ui_booking.com-0.101.tar` & `ui_booking.com-0.102.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 11:41:37.955436 ui_booking.com-0.101/
--rw-rw-rw-   0        0        0      120 2023-07-23 11:41:37.955436 ui_booking.com-0.101/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-07-23 11:41:37.950452 ui_booking.com-0.101/activities/
--rw-rw-rw-   0        0        0        0 2023-07-23 01:47:12.000000 ui_booking.com-0.101/activities/__init__.py
--rw-rw-rw-   0        0        0      564 2023-07-23 07:31:35.000000 ui_booking.com-0.101/activities/booking.py
--rw-rw-rw-   0        0        0       38 2023-07-23 07:13:57.000000 ui_booking.com-0.101/activities/constants.py
--rw-rw-rw-   0        0        0       42 2023-07-23 11:41:37.956432 ui_booking.com-0.101/setup.cfg
--rw-rw-rw-   0        0        0      165 2023-07-23 11:41:32.000000 ui_booking.com-0.101/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 11:41:37.954439 ui_booking.com-0.101/ui_booking.com.egg-info/
--rw-rw-rw-   0        0        0      120 2023-07-23 11:41:37.000000 ui_booking.com-0.101/ui_booking.com.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      229 2023-07-23 11:41:37.000000 ui_booking.com-0.101/ui_booking.com.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 11:41:37.000000 ui_booking.com-0.101/ui_booking.com.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       11 2023-07-23 11:41:37.000000 ui_booking.com-0.101/ui_booking.com.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 11:45:02.672975 ui_booking.com-0.102/
+-rw-rw-rw-   0        0        0      120 2023-07-23 11:45:02.672975 ui_booking.com-0.102/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-07-23 11:45:02.669320 ui_booking.com-0.102/activities/
+-rw-rw-rw-   0        0        0        0 2023-07-23 01:47:12.000000 ui_booking.com-0.102/activities/__init__.py
+-rw-rw-rw-   0        0        0      564 2023-07-23 07:31:35.000000 ui_booking.com-0.102/activities/booking.py
+-rw-rw-rw-   0        0        0       38 2023-07-23 07:13:57.000000 ui_booking.com-0.102/activities/constants.py
+-rw-rw-rw-   0        0        0       42 2023-07-23 11:45:02.672975 ui_booking.com-0.102/setup.cfg
+-rw-rw-rw-   0        0        0      165 2023-07-23 11:44:46.000000 ui_booking.com-0.102/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:45:02.671719 ui_booking.com-0.102/ui_booking.com.egg-info/
+-rw-rw-rw-   0        0        0      120 2023-07-23 11:45:02.000000 ui_booking.com-0.102/ui_booking.com.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      229 2023-07-23 11:45:02.000000 ui_booking.com-0.102/ui_booking.com.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 11:45:02.000000 ui_booking.com-0.102/ui_booking.com.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 11:45:02.000000 ui_booking.com-0.102/ui_booking.com.egg-info/top_level.txt
```

### Comparing `ui_booking.com-0.101/activities/booking.py` & `ui_booking.com-0.102/activities/booking.py`

 * *Files identical despite different names*

