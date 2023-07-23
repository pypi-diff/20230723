# Comparing `tmp/my_ui_booking.com-0.1.tar.gz` & `tmp/my_ui_booking.com-0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "my_ui_booking.com-0.1.tar", last modified: Sun Jul 23 11:54:14 2023, max compression
+gzip compressed data, was "my_ui_booking.com-0.2.tar", last modified: Sun Jul 23 14:17:29 2023, max compression
```

## Comparing `my_ui_booking.com-0.1.tar` & `my_ui_booking.com-0.2.tar`

### file list

```diff
@@ -1,9 +1,9 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 11:54:14.242502 my_ui_booking.com-0.1/
--rw-rw-rw-   0        0        0      121 2023-07-23 11:54:14.242502 my_ui_booking.com-0.1/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-07-23 11:54:14.241500 my_ui_booking.com-0.1/my_ui_booking.com.egg-info/
--rw-rw-rw-   0        0        0      121 2023-07-23 11:54:14.000000 my_ui_booking.com-0.1/my_ui_booking.com.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      172 2023-07-23 11:54:14.000000 my_ui_booking.com-0.1/my_ui_booking.com.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 11:54:14.000000 my_ui_booking.com-0.1/my_ui_booking.com.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 11:54:14.000000 my_ui_booking.com-0.1/my_ui_booking.com.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 11:54:14.243938 my_ui_booking.com-0.1/setup.cfg
--rw-rw-rw-   0        0        0      166 2023-07-23 11:53:55.000000 my_ui_booking.com-0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 14:17:29.147819 my_ui_booking.com-0.2/
+-rw-rw-rw-   0        0        0      121 2023-07-23 14:17:29.146544 my_ui_booking.com-0.2/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-07-23 14:17:29.144547 my_ui_booking.com-0.2/my_ui_booking.com.egg-info/
+-rw-rw-rw-   0        0        0      121 2023-07-23 14:17:29.000000 my_ui_booking.com-0.2/my_ui_booking.com.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      172 2023-07-23 14:17:29.000000 my_ui_booking.com-0.2/my_ui_booking.com.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 14:17:29.000000 my_ui_booking.com-0.2/my_ui_booking.com.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 14:17:29.000000 my_ui_booking.com-0.2/my_ui_booking.com.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 14:17:29.147819 my_ui_booking.com-0.2/setup.cfg
+-rw-rw-rw-   0        0        0      166 2023-07-23 14:17:12.000000 my_ui_booking.com-0.2/setup.py
```

