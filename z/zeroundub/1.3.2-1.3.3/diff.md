# Comparing `tmp/zeroundub-1.3.2.tar.gz` & `tmp/zeroundub-1.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zeroundub-1.3.2.tar", last modified: Sun Jun 11 09:58:30 2023, max compression
+gzip compressed data, was "zeroundub-1.3.3.tar", last modified: Sun Jul 23 13:52:35 2023, max compression
```

## Comparing `zeroundub-1.3.2.tar` & `zeroundub-1.3.3.tar`

### file list

```diff
@@ -1,60 +1,60 @@
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.667069 zeroundub-1.3.2/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     1064 2022-03-30 16:46:10.000000 zeroundub-1.3.2/LICENSE
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)    13305 2023-06-11 09:58:30.663069 zeroundub-1.3.2/PKG-INFO
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)    12844 2023-06-02 14:44:51.000000 zeroundub-1.3.2/README.md
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)      963 2023-06-11 09:58:11.000000 zeroundub-1.3.2/pyproject.toml
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)       56 2023-06-10 13:07:08.000000 zeroundub-1.3.2/requirements.txt
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)       38 2023-06-11 09:58:30.667069 zeroundub-1.3.2/setup.cfg
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)       91 2023-03-04 13:55:34.000000 zeroundub-1.3.2/setup.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)        0 2022-03-30 16:19:57.000000 zeroundub-1.3.2/zeroundub/__init__.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/cli/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)        0 2022-03-30 08:12:21.000000 zeroundub-1.3.2/zeroundub/cli/__init__.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/cli/cmdline/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)        0 2022-03-30 16:31:10.000000 zeroundub-1.3.2/zeroundub/cli/cmdline/__init__.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     6712 2023-06-11 09:37:32.000000 zeroundub-1.3.2/zeroundub/cli/cmdline/undub.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)      624 2023-03-04 14:04:37.000000 zeroundub-1.3.2/zeroundub/cli/error.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     1460 2023-06-02 14:24:48.000000 zeroundub-1.3.2/zeroundub/cli/progress.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)      592 2023-03-04 14:04:37.000000 zeroundub-1.3.2/zeroundub/cli/utils.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/gui/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)        0 2022-11-28 21:00:19.000000 zeroundub-1.3.2/zeroundub/gui/__init__.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)    27628 2023-06-11 09:51:43.000000 zeroundub-1.3.2/zeroundub/gui/tkgui.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/utils/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)        0 2022-03-30 09:04:44.000000 zeroundub-1.3.2/zeroundub/utils/__init__.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     1817 2023-03-04 15:57:05.000000 zeroundub-1.3.2/zeroundub/utils/file.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/wagrenier/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)        0 2022-03-30 09:08:55.000000 zeroundub-1.3.2/zeroundub/wagrenier/__init__.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     6210 2023-03-04 16:18:26.000000 zeroundub-1.3.2/zeroundub/wagrenier/pssmux.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/zero/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)        0 2022-03-30 09:07:28.000000 zeroundub-1.3.2/zeroundub/zero/__init__.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     1526 2023-03-04 15:47:42.000000 zeroundub-1.3.2/zeroundub/zero/dvd.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/zero/iso/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)      114 2023-03-04 14:04:37.000000 zeroundub-1.3.2/zeroundub/zero/iso/__init__.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)    35480 2023-06-02 14:25:46.000000 zeroundub-1.3.2/zeroundub/zero/iso/repack.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     3317 2023-06-02 12:29:56.000000 zeroundub-1.3.2/zeroundub/zero/pk2.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/zero/reader/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)        0 2022-03-30 13:21:51.000000 zeroundub-1.3.2/zeroundub/zero/reader/__init__.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/zero/reader/adapter/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)       70 2022-03-30 13:29:33.000000 zeroundub-1.3.2/zeroundub/zero/reader/adapter/__init__.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     1109 2023-03-04 16:13:12.000000 zeroundub-1.3.2/zeroundub/zero/reader/adapter/abstract.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     1311 2023-03-04 16:25:19.000000 zeroundub-1.3.2/zeroundub/zero/reader/adapter/filesystem.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     1186 2023-03-04 16:25:39.000000 zeroundub-1.3.2/zeroundub/zero/reader/adapter/iso.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)      192 2022-03-30 13:28:56.000000 zeroundub-1.3.2/zeroundub/zero/reader/entry.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     5835 2023-03-04 16:25:51.000000 zeroundub-1.3.2/zeroundub/zero/reader/pjzreader.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/zero/text/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)        0 2022-03-26 15:11:49.000000 zeroundub-1.3.2/zeroundub/zero/text/__init__.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)    12200 2023-03-04 16:24:20.000000 zeroundub-1.3.2/zeroundub/zero/text/parser.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub/zero/text/tables/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)      106 2022-03-30 16:25:21.000000 zeroundub-1.3.2/zeroundub/zero/text/tables/__init__.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     1519 2023-03-04 15:30:27.000000 zeroundub-1.3.2/zeroundub/zero/text/tables/european.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     3581 2023-03-04 15:28:37.000000 zeroundub-1.3.2/zeroundub/zero/text/tables/japanese.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)    23415 2023-03-04 15:32:21.000000 zeroundub-1.3.2/zeroundub/zero/text/tables/subtitles.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)      300 2023-03-04 14:04:37.000000 zeroundub-1.3.2/zeroundub/zero/text/tables/utils.py
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)    10210 2023-06-10 13:06:18.000000 zeroundub-1.3.2/zeroundub/zero/tim2.py
-drwxrwxr-x   0 baecchi   (5002) baecchi   (5002)        0 2023-06-11 09:58:30.663069 zeroundub-1.3.2/zeroundub.egg-info/
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)    13305 2023-06-11 09:58:30.000000 zeroundub-1.3.2/zeroundub.egg-info/PKG-INFO
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)     1280 2023-06-11 09:58:30.000000 zeroundub-1.3.2/zeroundub.egg-info/SOURCES.txt
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)        1 2023-06-11 09:58:30.000000 zeroundub-1.3.2/zeroundub.egg-info/dependency_links.txt
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)      104 2023-06-11 09:58:30.000000 zeroundub-1.3.2/zeroundub.egg-info/entry_points.txt
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)       57 2023-06-11 09:58:30.000000 zeroundub-1.3.2/zeroundub.egg-info/requires.txt
--rw-rw-r--   0 baecchi   (5002) baecchi   (5002)       10 2023-06-11 09:58:30.000000 zeroundub-1.3.2/zeroundub.egg-info/top_level.txt
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.198761 zeroundub-1.3.3/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     1064 2022-03-30 16:46:10.000000 zeroundub-1.3.3/LICENSE
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)    13395 2023-07-23 13:52:35.198761 zeroundub-1.3.3/PKG-INFO
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)    12934 2023-07-23 13:40:14.000000 zeroundub-1.3.3/README.md
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)      963 2023-07-23 13:37:23.000000 zeroundub-1.3.3/pyproject.toml
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)       56 2023-07-23 13:31:59.000000 zeroundub-1.3.3/requirements.txt
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)       38 2023-07-23 13:52:35.198761 zeroundub-1.3.3/setup.cfg
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)       91 2023-03-04 13:55:34.000000 zeroundub-1.3.3/setup.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.194761 zeroundub-1.3.3/zeroundub/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)        0 2022-03-30 16:19:57.000000 zeroundub-1.3.3/zeroundub/__init__.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.194761 zeroundub-1.3.3/zeroundub/cli/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)        0 2022-03-30 08:12:21.000000 zeroundub-1.3.3/zeroundub/cli/__init__.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.194761 zeroundub-1.3.3/zeroundub/cli/cmdline/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)        0 2022-03-30 16:31:10.000000 zeroundub-1.3.3/zeroundub/cli/cmdline/__init__.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     6712 2023-06-11 09:37:32.000000 zeroundub-1.3.3/zeroundub/cli/cmdline/undub.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)      624 2023-03-04 14:04:37.000000 zeroundub-1.3.3/zeroundub/cli/error.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     1460 2023-06-02 14:24:48.000000 zeroundub-1.3.3/zeroundub/cli/progress.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)      592 2023-03-04 14:04:37.000000 zeroundub-1.3.3/zeroundub/cli/utils.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.194761 zeroundub-1.3.3/zeroundub/gui/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)        0 2022-11-28 21:00:19.000000 zeroundub-1.3.3/zeroundub/gui/__init__.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)    27648 2023-07-23 13:34:11.000000 zeroundub-1.3.3/zeroundub/gui/tkgui.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.194761 zeroundub-1.3.3/zeroundub/utils/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)        0 2022-03-30 09:04:44.000000 zeroundub-1.3.3/zeroundub/utils/__init__.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     1817 2023-03-04 15:57:05.000000 zeroundub-1.3.3/zeroundub/utils/file.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.194761 zeroundub-1.3.3/zeroundub/wagrenier/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)        0 2022-03-30 09:08:55.000000 zeroundub-1.3.3/zeroundub/wagrenier/__init__.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     6210 2023-03-04 16:18:26.000000 zeroundub-1.3.3/zeroundub/wagrenier/pssmux.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.198761 zeroundub-1.3.3/zeroundub/zero/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)        0 2022-03-30 09:07:28.000000 zeroundub-1.3.3/zeroundub/zero/__init__.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     1526 2023-03-04 15:47:42.000000 zeroundub-1.3.3/zeroundub/zero/dvd.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.198761 zeroundub-1.3.3/zeroundub/zero/iso/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)      114 2023-03-04 14:04:37.000000 zeroundub-1.3.3/zeroundub/zero/iso/__init__.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)    35480 2023-06-02 14:25:46.000000 zeroundub-1.3.3/zeroundub/zero/iso/repack.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     3317 2023-06-02 12:29:56.000000 zeroundub-1.3.3/zeroundub/zero/pk2.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.198761 zeroundub-1.3.3/zeroundub/zero/reader/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)        0 2022-03-30 13:21:51.000000 zeroundub-1.3.3/zeroundub/zero/reader/__init__.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.198761 zeroundub-1.3.3/zeroundub/zero/reader/adapter/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)       70 2022-03-30 13:29:33.000000 zeroundub-1.3.3/zeroundub/zero/reader/adapter/__init__.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     1109 2023-03-04 16:13:12.000000 zeroundub-1.3.3/zeroundub/zero/reader/adapter/abstract.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     1311 2023-03-04 16:25:19.000000 zeroundub-1.3.3/zeroundub/zero/reader/adapter/filesystem.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     1186 2023-03-04 16:25:39.000000 zeroundub-1.3.3/zeroundub/zero/reader/adapter/iso.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)      192 2022-03-30 13:28:56.000000 zeroundub-1.3.3/zeroundub/zero/reader/entry.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     5835 2023-03-04 16:25:51.000000 zeroundub-1.3.3/zeroundub/zero/reader/pjzreader.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.198761 zeroundub-1.3.3/zeroundub/zero/text/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)        0 2022-03-26 15:11:49.000000 zeroundub-1.3.3/zeroundub/zero/text/__init__.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)    12200 2023-03-04 16:24:20.000000 zeroundub-1.3.3/zeroundub/zero/text/parser.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.198761 zeroundub-1.3.3/zeroundub/zero/text/tables/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)      106 2022-03-30 16:25:21.000000 zeroundub-1.3.3/zeroundub/zero/text/tables/__init__.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     1519 2023-03-04 15:30:27.000000 zeroundub-1.3.3/zeroundub/zero/text/tables/european.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     3581 2023-03-04 15:28:37.000000 zeroundub-1.3.3/zeroundub/zero/text/tables/japanese.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)    24058 2023-07-23 13:42:54.000000 zeroundub-1.3.3/zeroundub/zero/text/tables/subtitles.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)      300 2023-03-04 14:04:37.000000 zeroundub-1.3.3/zeroundub/zero/text/tables/utils.py
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)    10210 2023-06-10 13:06:18.000000 zeroundub-1.3.3/zeroundub/zero/tim2.py
+drwxrwxr-x   0 baecchi   (1000) baecchi   (1000)        0 2023-07-23 13:52:35.194761 zeroundub-1.3.3/zeroundub.egg-info/
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)    13395 2023-07-23 13:52:35.000000 zeroundub-1.3.3/zeroundub.egg-info/PKG-INFO
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)     1280 2023-07-23 13:52:35.000000 zeroundub-1.3.3/zeroundub.egg-info/SOURCES.txt
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)        1 2023-07-23 13:52:35.000000 zeroundub-1.3.3/zeroundub.egg-info/dependency_links.txt
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)      104 2023-07-23 13:52:35.000000 zeroundub-1.3.3/zeroundub.egg-info/entry_points.txt
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)       57 2023-07-23 13:52:35.000000 zeroundub-1.3.3/zeroundub.egg-info/requires.txt
+-rw-rw-r--   0 baecchi   (1000) baecchi   (1000)       10 2023-07-23 13:52:35.000000 zeroundub-1.3.3/zeroundub.egg-info/top_level.txt
```

### Comparing `zeroundub-1.3.2/LICENSE` & `zeroundub-1.3.3/LICENSE`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/PKG-INFO` & `zeroundub-1.3.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zeroundub
-Version: 1.3.2
+Version: 1.3.3
 Summary: Undub project for Tecmo's Project Zero - the EU version (the first one) for the PS2
 Author: karas84
 Project-URL: Homepage, https://github.com/karas84/ProjectZeroUndub
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
@@ -218,11 +218,12 @@
 - [wagrenier](https://github.com/wagrenier) again, for his help with replacing all game models with the Japanese ones
 - [pgert](https://forums.pcsx2.net/Thread-PCSX2-Widescreen-Game-Patches?pid=240786#pid240786)
   and the whole [PCSX2 community](https://forums.pcsx2.net/) for the great patches that can
   be injected into the game
 - [pelvicthrustman](https://www.psx-place.com/threads/ps2-patch-engine-by-pelvicthrustman.19167/)
   and [Snaggly](https://github.com/Snaggly) for their tools to inject patches into the ELF
 - [weirdbeardgame](https://github.com/weirdbeardgame/), for the Kirie camera bug fix
+- [FlamePurge](https://www.romhacking.net/community/1523/) for proofreading the subtitles
 - All the guys out there on so many forums I've lost track of, that released bits of
   information about many game file formats
 - Finally, to 2010 me, who painstakingly spent weeks building his own undub, reversed-engineered
   the game data and transcribed all FMVs and cutscenes
```

### Comparing `zeroundub-1.3.2/README.md` & `zeroundub-1.3.3/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -205,11 +205,12 @@
 - [wagrenier](https://github.com/wagrenier) again, for his help with replacing all game models with the Japanese ones
 - [pgert](https://forums.pcsx2.net/Thread-PCSX2-Widescreen-Game-Patches?pid=240786#pid240786)
   and the whole [PCSX2 community](https://forums.pcsx2.net/) for the great patches that can
   be injected into the game
 - [pelvicthrustman](https://www.psx-place.com/threads/ps2-patch-engine-by-pelvicthrustman.19167/)
   and [Snaggly](https://github.com/Snaggly) for their tools to inject patches into the ELF
 - [weirdbeardgame](https://github.com/weirdbeardgame/), for the Kirie camera bug fix
+- [FlamePurge](https://www.romhacking.net/community/1523/) for proofreading the subtitles
 - All the guys out there on so many forums I've lost track of, that released bits of
   information about many game file formats
 - Finally, to 2010 me, who painstakingly spent weeks building his own undub, reversed-engineered
   the game data and transcribed all FMVs and cutscenes
```

### Comparing `zeroundub-1.3.2/pyproject.toml` & `zeroundub-1.3.3/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 [build-system]
 requires = ["setuptools>=61.2", "wheel", "build>=0.8.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 description = "Undub project for Tecmo's Project Zero - the EU version (the first one) for the PS2"
 name = "zeroundub"
-version = "1.3.2"
+version = "1.3.3"
 authors = [{ name = "karas84" }]
 classifiers = [
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
     "Operating System :: OS Independent",
 ]
 requires-python = ">=3.7"
```

### Comparing `zeroundub-1.3.2/zeroundub/cli/cmdline/undub.py` & `zeroundub-1.3.3/zeroundub/cli/cmdline/undub.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/cli/error.py` & `zeroundub-1.3.3/zeroundub/cli/error.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/cli/progress.py` & `zeroundub-1.3.3/zeroundub/cli/progress.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/cli/utils.py` & `zeroundub-1.3.3/zeroundub/cli/utils.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/gui/tkgui.py` & `zeroundub-1.3.3/zeroundub/gui/tkgui.py`

 * *Files 1% similar despite different names*

```diff
@@ -585,26 +585,26 @@
         if eu_iso_path:
             self.eu_iso_path = eu_iso_path
             self.button_iso_jp.state(["!disabled"])
 
     def select_jp_iso(self):
         jp_iso_path = fd.askopenfilename(
             title="Select Japanese ISO",
-            initialdir=os.path.expanduser("~"),
+            initialdir=os.path.dirname(self.eu_iso_path),
             filetypes=self.filetypes,
         )
 
         if jp_iso_path:
             self.jp_iso_path = jp_iso_path
             self.button_iso_undub.state(["!disabled"])
 
     def select_undub_iso(self):
         undub_iso_path = fd.asksaveasfilename(
             title="Choose Output Undub ISO",
-            initialdir=os.path.expanduser("~"),
+            initialdir=os.path.dirname(self.eu_iso_path),
             filetypes=self.filetypes,
         )
 
         if undub_iso_path:
             if os.path.splitext(undub_iso_path.lower())[1] != ".iso":
                 undub_iso_path += ".iso"
             self.undub_iso_path = undub_iso_path
```

### Comparing `zeroundub-1.3.2/zeroundub/utils/file.py` & `zeroundub-1.3.3/zeroundub/utils/file.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/wagrenier/pssmux.py` & `zeroundub-1.3.3/zeroundub/wagrenier/pssmux.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/zero/dvd.py` & `zeroundub-1.3.3/zeroundub/zero/dvd.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/zero/iso/repack.py` & `zeroundub-1.3.3/zeroundub/zero/iso/repack.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/zero/pk2.py` & `zeroundub-1.3.3/zeroundub/zero/pk2.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/zero/reader/adapter/abstract.py` & `zeroundub-1.3.3/zeroundub/zero/reader/adapter/abstract.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/zero/reader/adapter/filesystem.py` & `zeroundub-1.3.3/zeroundub/zero/reader/adapter/filesystem.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/zero/reader/adapter/iso.py` & `zeroundub-1.3.3/zeroundub/zero/reader/adapter/iso.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/zero/reader/pjzreader.py` & `zeroundub-1.3.3/zeroundub/zero/reader/pjzreader.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/zero/text/parser.py` & `zeroundub-1.3.3/zeroundub/zero/text/parser.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/zero/text/tables/european.py` & `zeroundub-1.3.3/zeroundub/zero/text/tables/european.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/zero/text/tables/japanese.py` & `zeroundub-1.3.3/zeroundub/zero/text/tables/japanese.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub/zero/text/tables/subtitles.py` & `zeroundub-1.3.3/zeroundub/zero/text/tables/subtitles.py`

 * *Files 9% similar despite different names*

```diff
@@ -2,290 +2,290 @@
 import os
 import hashlib
 
 from typing import BinaryIO
 
 
 subtitles_en_encoded = {
-    0: "9c2c60c274d05a2d6bea5b5017",
+    0: "9c0c40e254d05a0d4bca7b7037",
     1: "6e56c3e4f9f869edc4cabfd14ec522c20a9640b4bcb5d4aabd456fcf5168673564a73a78300573ae1a69fc0021a41d655c3f",
     2: "63251060755875725472f41c2114ed683ee972efe1756eea7360ff6412ff6dd2b06250ff2630b172c2fe2f",
     3: "34de2115c366b3c873c2e66988df2f209e",
     4: "6981967697a521eeb62105ab64319d21728465846aba6f802f",
-    5: "7c677d75d37129773566a66cdb6f8d23246aec24b424516af269840f42763f689273902657684866f46898731a7c1061db28bf618e614a672127",
-    6: "ce6fc86c99295f7f152af965b5626779036f336ef427",
-    7: "8b6e387b067f8161912c71633b74786b754f7640660d",
-    8: "7e740d53734f550a4a6c3d57404d8b58740a524d475b474d710e0807",
-    9: "6455b6988d635d4140690e544f5b0958e1da8c71436d4f773b43790d6c5f724974484f0d",
-    10: "5568715e4c49de7e7a417e4140464b0e1541064f4841f9795a094b42504649768d5e",
-    11: "7a424a09413b4548403f71500947e4958b614f5d2459436c0a557a6f660949464d4b7d684c4d055747d2",
-    12: "435a5342566ff39b8d71463f5b7772407a276d556c497a54494b7673780d464ede4b3b4870434806",
-    13: "794a7a730641483f5af978463f5e43095d4d9f52034d7a0a7c435a09413b444c4f7b16464705c29b94754f76427a3c5f3f5a77556d497a4445566b6e33",
-    14: "6409469b466f0a6a4246495e5a303100",
-    15: "4e76774c12fe69095e448d06444a76447c0c4848523b51684d4a070830",
-    16: "3e29484943e29f9276476d0c2d17013b1c1e2310",
-    17: "72424a6c3d7146549b48744574020706246b6b075509645eb8297a47424848449043045631",
-    18: "4f42426b3d6848533b655b003f48484244fb93916c0401002471700a4b7a3d7b4044084a417279094140514dd0",
-    19: "6a5a4b5607",
-    20: "56e2dd8c34407a4971031f3b5a427e4d550a5076737c4c006311467e5f8a09404b436d44064f5b43fbda926d027d5f7258734f7b04",
-    21: "6168513f764a0a4a4c4f510d47034b708a48095377445722724c440c72483f6f433d5640405d3f5dfa9b9c710c",
-    22: "560c797e406b0d7e433f5873495f44773331035a4f477e5e774590442259436c3e4f7a5d7345f8992c444c0545435140310435",
-    23: "614f4f556269083533",
-    24: "6851094c6d735d4140e4da8875513f447a514835040d",
-    25: "48757e5d0043680a6b44975c086e734d4d4731300112",
-    26: "6646445d0d",
-    27: "5a764a026c73417e5b4d7a0cfc8f8c67311e3113",
-    28: "52065d4c71797a5f09494c3b5d7a0b77403f45419044264846575d48474c78074b495e4c02b822",
-    29: "07070b645204563f9d45774800070e",
-    30: "4c40485a3f7d095e57f799943a0c31",
-    31: "68767f0c6c5e724b5e4b7673780d41415a6b4f710c8a4622435b3f435e465b407be42b",
-    32: "686a405209454c4d460576900a6f444b095073436b7106",
-    33: "7e467e68095e44e5da8b3956774d6b24",
-    34: "647a4831",
-    35: "664f4f6f3d7248070e04",
-    36: "48427059924d0867026b40474c0f493ee67c4d6b5c19",
-    37: "605d02550351779f5e3b5c4b5b5374423f5708435b6c68095a44e1d4d13a",
-    38: "7677493f51426b546c00",
-    39: "67427968665c01",
-    40: "7d7a436b02d035",
-    41: "66425f503f724bb7",
-    42: "5d4f4d48444c43430d0b31",
-    43: "b5445b4e7a070631",
-    44: "654945423f41414e000d063b564a404013fe93923a0c31",
-    45: "78325748774409467671095e4d485c11",
-    46: "75778712",
-    47: "6768035875725e3fe2654c0d66464c570252436953705fc1",
-    48: "6b6f176c3c756a5b5a094d0859464bf59fdf664c0f475a0c3106",
-    49: "6017734a03404fe0483e66745b02984d4c423f4e510743414a4831b8d4",
-    50: "be34467a4170750d",
-    51: "5e0d7155680c7f43474c713c",
-    52: "4e584043950b3b6c76424d08464b720c",
-    53: "6e70494bb675507046484d070bd0",
-    54: "724b403f58745c4b16",
-    55: "6e740d",
-    56: "4b76495d0e72755b5b4ae4db",
-    57: "b860564c0f416a3b4a7e524308",
-    58: "673f404940463e6b912d69455c564ef94e40095a777923614cfb8f8d7b02794d72724066006808404c4d507a58225b476b587a443e9c4d7c50586849000d33",
-    59: "72774450084f4f77714a4b714f09437e6f42094ce5da8b674d24424f50005a4d3f55447e107b42415b06310d",
-    60: "79739b0a4273697e5b0768084e416b3c5d4605414d119c4f4e72434a0369747252b69e906652070106",
-    61: "537445311f03",
-    62: "50494e0b",
-    63: "7d4b511e297f45426a3f964f526f4d474b7b23",
-    64: "704840b8d4d1",
-    65: "5c4d680c7c745973493f4477456806484620",
-    66: "50704016",
-    67: "77964b6f0d6c0c5d404f5620",
-    68: "6c55094a517be5270008",
-    69: "645005488743500b3135",
-    70: "7d4b7e693f5e4168085d467e6816",
-    71: "6051b189df7a450f4a6c694b011d01",
-    72: "c2590f5a0e52424e524a5502",
-    73: "7277f3de69744f5d1346e5b6f0674750654951095e434c41e24278d00c31",
-    74: "656b0a5a077e5f4d6b447ae4da8f7d477c493f4c4b3b6a4b7e0c5e585e51415c3e",
-    75: "63405a974c07",
-    76: "575e3c593f48425a460d30310e6b6b0d5f3f5d4113784840fdd4d127",
-    77: "7e474b5d473f5a4b7069705a0e351f",
-    78: "7d4f7e51ac5f9b3e46634d5057445e13544b433fe59b926c204e5d2d6f484a1340e5485b0943704e08535c4f480831b8",
-    79: "ad9771507a0c6b7349660d6b51744975065d4a6b75155941498d0a784b72495b4911",
-    80: "6f7e4f53676b31030b",
-    81: "db9b997c595c0e",
-    82: "6c71750f5d066771563b5e564a47494c768d7909444012",
-    83: "6670514eb6929a7b4f010000",
-    84: "6976584a7a3c",
-    85: "4b414968085e47673f",
-    86: "747e0c5d9b464c07474f034e6ae48886270e07",
-    87: "7f447b7a59463133310950774d48557b3e4e7a4756de4a5c0e516b715c351f31",
-    88: "7f5d4f5e0272780c",
-    89: "484541b69b8d710266436a1c",
-    90: "643b4c4648395e03687c715d005e740a7b459b07",
+    5: "7c677d75d37129773566a66cdb6f8d23246aec24b424516af269840f42763f689273902657684866f46898731a7c106ddb6de97e947b4c663c7aa1",
+    6: "48da7d8e7b10651278b467ae7e6a6e512b3e62f56fcf",
+    7: "637d2c106dd22c85753e623961212d72437245735a03",
+    8: "4842076f4e4f5903766e3f6149935f69453f6148465d4b704e08",
+    9: "64500cf4889078414c573b59425d08405faf899a75507c443f744a3f5e705d7a43754304",
+    10: "696a736c484000aa4b704b7245474d02287e0040484443e37f09474a5b434f4c6c8a",
+    11: "4b75480e48007649470e7265094b57f98e976c5825594f513f5c466d643f404e4c4c4c6b794d09514c04",
+    12: "9a4e404153567af7889a70026844767749155f7a437a4d6945424a717a3f4c094291457004",
+    13: "484446460e4a7a3d5246417b0efb71026b5b475d094d9b06444a6b0a7a0c424c417f2246403f48484244fb939171056c0c6873496d487e5270596f5506",
+    14: "6a3f7b7a415d008b447e4b6c55",
+    15: "4f4146463e774b02687d5a12f163404742de4042573f4b6c4d5707",
+    16: "0011637a5c474c4b7c7b513b1e07badace2d1a29",
+    17: "78774a5e3b43486f4344454c743331072ab75e3c593f615b060e767e4b47444042f32e5d08",
+    18: "7d414459de5142563f56580d3f497e42417641474b3132072376f9da976c0a4b474a027c454e7a3d774c524d07",
+    19: "6376775c08",
+    20: "6c570f8d07514546483fe28d9034557a4974500d6844497843066329737c6c5d00427e4b6d48de4f5a414f3f4d5f094b5ef98e97715031",
+    21: "6f68583b426c0a4f78436b3e4e0a48465d400d524b446bf4414c433f4846086a46005877446c3b5c71434b4c00",
+    22: "560df09f9360027e5f3f6f447058785831023555454e7a6977444747206c4b6c0c9d4244424b71790c76543f44f38c6907",
+    23: "64444b535a50310435",
+    24: "61570942697352737857085e4f6c3c414c57f3d4",
+    25: "a87c436b0c76500d6f424a6c3d6f4541497e15",
+    26: "5749925f063031",
+    27: "6847463f6d40404b4c464803746a5d5631320224",
+    28: "7d036843f89e9a613f59790c6c430d4f733d79444744207a446658734571440896455e4c06",
+    29: "675d075d027c484f4802",
+    30: "7e44f7780948055a54464674d0",
+    31: "6e72480e5a4f764d5d4676724e094df78a8f714c3f5870114166117d5c455777786d12",
+    32: "6355596f0a7345954c08474c3f55444c0f5876f9604d31",
+    33: "644e485d055142563f8a427a5811",
+    34: "61456202",
+    35: "577b44590e727908",
+    36: "7a4df98f937002560c6b7a477a117e0e5a4b70697012",
+    37: "60540d680a6b449f5d085e476d5243470f613efc61516b1355485e0b",
+    38: "724b403f8c456b495d07",
+    39: "6d7a4a6a675d08",
+    40: "797e755d08",
+    41: "6df3968f344f7a0d",
+    42: "5251033b657e454b4e76737a08",
+    43: "6b4369437a02d035",
+    44: "7a425f4c3f7747fb2700085d4c4941064b4c72d00307",
+    45: "737a45443f5945440e6841495711",
+    46: "7440620c010213",
+    47: "7ae5da8b7c4b6c0c6b4b483b604642663c6440575b475c1d",
+    48: "568a0a5d3b49596e6f0d7eb67d40484d4c0041443f436f0f",
+    49: "560a924e3b5d7e777a3f51415c0c4e4c4a42b69786295a4e47400c",
+    50: "5e084d5572494d0c",
+    51: "6fab437b683b4a479347470f",
+    52: "4e5641445801036076f89edf7c4b720d",
+    53: "537443740d7e4270597542040d31",
+    54: "4977480952915a7e15",
+    55: "514308",
+    56: "7c46436b0d4f765452f96603",
+    57: "585a504c094c8a0641447c413a",
+    58: "650e4a4176493f6a47095c7a6f4c4857f592df7d484c256077765d6d5e084f4f724a4454046d3f8d6878524a4725f9445c5c4f733c4b4c46f78f8c710c3102",
+    59: "6b73456c0779445a474a4b714b08444f6c463b416dde5c7754277049570369493f594b4d0d4771705c0c",
+    60: "4b404c0e7e705d4857b189df68475a095e46004c47154349735971490e5d4076500d7f91455131",
+    61: "5070440e3506",
+    62: "6441723d",
+    63: "7e415c1c224c964b523b454f536d797544f2c5",
+    64: "a66845070106",
+    65: "56745f3f5242684a470a5e4b4152034a481c",
+    66: "53709311",
+    67: "7577495d096c3c5d4144e2c5",
+    68: "b26d027a557a680d",
+    69: "52543f5566496807",
+    70: "7d4b7e693f5a4853de5e734b6b13",
+    71: "605c09513f5243094b496cfd270008",
+    72: "605d025ede6b42436a625f02",
+    73: "4b757a094474475b0e766f094f4cf89b9365530f417d7e4e465d48a5",
+    74: "645c0e5d3f424648474846543fe6976878450f5c49b6e2fe6b097c60575a46431d",
+    75: "6246f9457adf",
+    76: "6b6b0b6c0d4d466d5a033f656bb189df674d3f487e51463a",
+    77: "4a4b7e5f56115c4b415a705b0706d0",
+    78: "7d4e7b533c587a0c46504c406a7357026b42493f5d4f5e792353e5da8b614f0f4140476c0a6e70703f5d4f745a07",
+    79: "707e5aee0d8a7646620c474243425d00544f6bfef08b61435c0e6e7a4d4a414eb4",
+    80: "60494f5b665606091d",
+    81: "6d42406aef8fde",
+    82: "504d710b6b3b5570583f427a4f7441444a65783f404c1f",
+    83: "ba456c443f444c5a4b0c310719",
+    84: "50713e0d6eff88966c01",
+    85: "7d47416d3b5f485f3f",
+    86: "49463b42564c4c0e5670de745c5b575403",
+    87: "4f4a45f7899a280a7f424b436c4f03727c744c00725c09556a71533a",
+    88: "7f479153084a5601",
+    89: "744e70b69b8d6c0050405d21",
+    90: "520a477073385d006c4947523e6a4c3b485a9b0d",
     91: "",
-    92: "610e557e706b0d51f9da8c6c4f0f46474f3f47474b3f5c43514b0e6b41715635330c",
-    93: "7052718e02",
-    94: "664812",
-    95: "6d42406aef8fd13a0c3e",
-    96: "61326e44705f0d3133",
-    97: "484c0e04350a68455d4f0e4392464d5a5d034a44095c4c49465c48495b06",
-    98: "675d075d026b967806457c56e2da8f7d477c493f4c4b3b5c41433e734a695e5c5109",
-    99: "6042786a875b033f734b4d42420c4a41744c707b5f6810",
-    100: "5b43f8dd8b3444705e78546f0d62475c543e7b5d446607",
-    101: "64533f9a565c5403776c0e56703b4d794a579c8e9760590f49786f7a2d4c4474567e4a35a503",
-    102: "527a7a5847085d46768d034f464745035270b6979a270e07",
-    103: "5b407b3b6c466858135e4a0357416a084b5d8c6f5b3b4d734d3b43504b446c7a0f",
-    104: "736a6b085a41466b09477c91695d095c42e3d4d127",
-    105: "630f437e5058036cff426e036f4456036b465f414e4f6befd6f5665c064c455648064a513f594b73403fe34c6b6e46750c5299484140070407",
-    106: "64414c385d0669716d5f5cb69b9d665b52094440012c5a4a6a0e4f6a5f6b034a743f",
-    107: "6e7a4a46875604004f46454b094f4003",
-    108: "527742530a",
-    109: "dfda9261516b0c6c574c62060708",
-    110: "4976426f0c52e7540c5a415b3f5b9f5a41734524",
-    111: "653d5d734f4d4305dc11417e423f4647738e2841434123",
-    112: "6e45475c000f54706b0e4e733ff98f8b295d465a464d6a6609477a3d",
-    113: "6f45485d313e02",
-    114: "7777480efc45915d49035a4a45440d6841555a4503517ee5f098614b7b4571440d764f0f3f543f4a4f5f774e3f444c498c244a7a530c5a4c5a7bf76447484e070b03",
-    115: "7540577a7a93434d783d7946523b404c426f32",
-    116: "685a05e2929a3470705c7a037e735a40487b3c64484c474d4e00095b469b23574f513f494b5a5c76724a48036f49075a4a4972b68e977102784d6b4603",
-    117: "424d5d066d744c09444f5b4f0c5e49408a4c440e5670014e7e3a68445a41086b59460e4d40473f8d494c0f4d7068457f33",
-    118: "5de38edf674a7a0c7c4c58774c47016a3c414853460842435d4002f4484e4a02684c5d094a7a4e474f0f53705a40b69b8f75506b267d5a0d6f40465d7a095c594d3f47494c43417099420f",
-    119: "594a724f413d574c5b5b455e4c440347f8da8b979a4d4ee161ef60f479d223",
-    120: "b9ac2c732e8248803b859c2e3a3951d690f9290f947f55052c6efbe59aac3a19193332027852ec91e8570b1d1547363dee9e92362ec02ed17c606e5d7a056ae57b816e4e300471c464ab7416650831fe708374137d107ad660973241660175c061df3340677667e371917c60716c",
-    121: "5b1662f3737d733d36e370e16285733f5a157bc0748a3b345177493fe25e114c457453520a57703d795c4c4c7246730c964c5a0e466a55454c5c087fe5035a4e4c0977425646054c738c4171540d50474a4e4f4d06",
-    122: "69f388df7f465c493b43565d5c0943ea979e7d4c3f447af94837274c7e4356434d783d6b4149593b4d7e589b095b4b4373444809404e789c6a465b054c4a4f057a6f9b427145475008",
-    123: "5f4473114c77434046330831",
-    124: "d3949b654f5c5d0e527e41711f0335",
-    125: "6d5d037149714408464000504e7ab6938c34446d497aab427d0d577a4f48040d31",
-    126: "5c6c094c45754d3f4d8d095b46473f485f0941476ab6654b405d094d425646497a688d06311f",
-    127: "643d514a59420d060fb68e9034407a0c7d5a0d7348553b554f4e4631",
-    128: "3331076d45486831",
-    129: "b34b7d5f665908",
-    130: "64414d7400",
-    131: "78414a416cb6674d6a406cab4c8c480946735d0c44414a4646034cf79994035e400e594a7a5b433e6a417856077d4d424c46401d0e0d",
-    132: "6b76fd8fd13a0c",
-    133: "560c714c5a3b5a4c477275534c055e485503543f894b68207d5e465d494a6b01444c5d4d30b827",
-    134: "6fe549de780c5447427308424b7e476b583d5d734f500841f3898b6044560e41443f7140474030",
-    135: "524476590f",
-    136: "484b494f450266917d0d09010c4f4f69074650565151535b494d4131",
-    137: "d38c9a7b005a46467d7e3c5d41445d004d47670003543f8d5e745a6f4947225d477a4547560954744047425eb68e97685e0f415a4a7a5a3f4148745c42461742704d0f531353464331",
-    138: "db9b99615b6a0d3fdf454c474c3f494d4c4c4f4c5b5d03",
-    139: "5b914e015d094af97b49435d095c425351057b6e685008",
-    140: "6887077f6b6b500040553e584c3d744f7e5a1558fe938c34457e587a034e7742547e4208040d",
-    141: "53787e5f45de5e73436c0c44495a473f69433f5d463331b8",
-    142: "7d4647035a408d7d3d744e0c667468024b5be4e4efda9e7a463f496c404c6b4d08",
-    143: "646b593d5b41475209494c4d6a8a3c62436a0f0207",
-    144: "660873e3898b29535d40583e6f427e0c6d475f7d42455c570629706f3f9b45534f3b436b0c5e41424e3f45436f5645f82c484e444490080d0b",
-    145: "5b74460e523e5f70435f620c4f4172536bb6979a382866436a0340585a533f494d02",
-    146: "654057595a5b023f4b46459b0e4d710b",
-    147: "57457047000c31",
-    148: "56477b77503b5e416e425c3f9f437e0d5040770a4d70774d4fb6989e7749155870035a734d5b433e68414c5c3b4c4b4e70907b35330b",
-    149: "62495c4b7a300235",
-    150: "427749b68d9e67027e4068425468085a526c694e4e495842440e48705ade4f417b4735",
-    151: "64785b3b554c5d4909455b516b0d507a4b419741086a77495a7a370e494b476f46424f9c8e976c0a484f5a473f5b4c4f73794d094a7d4e3e4e70430d9f77400e4669436d4d41534a0e",
-    152: "704e7ab6929e70026b433f504c785f4e7d4f454f037a6b7a5b598a42724478020706",
-    153: "7a4a7a6e473f5e41e3655d0644485c0d8c4350513f72463f41487c4546060a415d55b6929a7b005a405d72275e4e7345067f40684c66680c6e5798784c6f010931",
-    154: "4e415f7e514c5a0f000c3f50474d3ef38c9a7b0e0701",
-    155: "6d684b503f534048464309584b4c5aab494d660d687e0c6e56916e59784b076c4d4b444d4f2757767640456c0d6f487ee2da90604a7a5e3f5348745845433e784647025d085d477ad0",
-    156: "7343595d49fb6b4bf90d1756770c0917121c1d1c",
-    157: "77454bab409f426c4470750c6a436d09734050774d5c48b68e9034407a266c7e497108705f0d6f444b0370476f01035b4203697ade484b71494542663c4148419c8e90294b5c450e56776d034b404f484c68074b4944de5e4303794440ef0d4e6f06",
-    158: "7b73435a08535c4c47066ae5da8b7c436b0c574a406e5a462c734c735f4049483b464f463f9c4b4c44094543526b54247d4c5e3d684869f3889e78027b497c42497e5b0948715a33",
-    159: "784143065a4943473f9175435d3b5bfe95df634d73483f5b513f564b49544f094a5c24687fe6de4f4e6c433ffc4c69724c4d055b513b40426b3f53420e4a91717a06414d534b05245577494a4e0551485f035c5bff8e9a2944405c4b7140417a525d4f4b4107",
-    160: "7f465d5aee404e7a5f3f2258750ede2c18271b17",
-    161: "565c0e5e464d40467a3f4a43717a7e6e4c5d6c0ee295df7e4b43450e5677524653424e09584b4824e6428b426b4c76750c7c563e4774484f6b040e5e4c0850560047437cff9e9a70026b433ff85d7e464d2c6a45780c474f414b5c00444c5a4bde484e4a027c42405d4171524c0840526d0859f9764206",
-    162: "c209884b02414d4040026f46437458494a3f5f7a6a7a5248403fe4959079513f4d7351487a4c500814787340404d43035c96450c4c505a4c52474d6d010e5d407a3c4642577e544e465d2277e5da8c604b73403f4a433b595c4f6a483d4b464942035b96415c4c06",
-    163: "6f094c47566b4d493b557e5f42404d6d116a0e5696415778495d0f683f6d416c177eb68d977d567a0c6c4b4c7f475e5f3e4b744b5c54430f47783f4dde594d725047237771086b407806414c434068f783df674f4e5c0e567777094f7167504d4d4b7a3e",
-    164: "650473410ee0489b410c575c424b4a0d4c4e074055404e3fe593987c566c497a4a437c5e174d474206535d4c4e765a4e3e8a73494a0945e50d433b447fe29f8d34437c4f7056436f06",
-    165: "7a436e5978414b43543b16195c49d20e132f1a2916",
-    166: "717a0879725b7d496948e49f9baa7647437a0c4a4b6c605a5c4b454d7c2c6c5b915970553f74400349019e7cf367fe33724a3b4e5feb8ae5f2f301",
-    167: "6b716a409edd60fe71f96303447aaa89e8e5a04547424973626d415cfedd8c1e41774573475f7e460506734873584049484d7b12474009b5414876005a0c40406f494011",
-    168: "4f74433f5efe958b7b02765f3ffa58445d423f414e4708404046115d4e465e560d8d494e403f7044795f09564a7a5e4046460e567e4735",
-    169: "6f483f5c9649097e4a5ff8f3e4da9099246c7f7d05685d773077fbbd36362f97019b21d1dd793d2b18cc8bac230a907c10473a28afecf5f5180d1b3d71003d2ae116dfe519581450103c31f95fdf940576c075a435",
-    170: "af7e713c43753e7b146e8675ae3c517239730c78c83da175646d62690e67907fd17a2877246d477ae77a833f704f274b5b41ed00b046335226444d52854cb74a7a4c5d02084df347fa51614f5a4d0703cc40bd566645494d074ab8",
-    171: "77a254774044473e57a11498518d0919145a1c8a10",
-    172: "4242114b0248d842bc0774442a08ed5ed55acc5c7f4c6e441947bf4068445748d65eda5d5b0bf55fd547670c2943ec40b54203596d4b1d43fc0d8242734763",
-    173: "791d47c84bfb5a685a5b0f0847b25b28440859db10a0517b42025ed7119e420a5a2c55ed1ebf7bd55f12501141c552625a7f43fc14b65b8b5857120d50ea539d405a525e5ea45bd9543d171558cf19e374624d575caa50a6188459535c4d58e84ba758904009564f5c5f05",
-    174: "645f0a490e584a5f5e1a425b4b535d5d14495a57534e5f53565d195b58554e4e361850554c5f1f482f4a2449601663492d54265f664d221a3c5526516a49245729303d52214e20497c1a285f214e3648305b2c14",
-    175: "055f274e3d573b5f281a6a082852711a6e03650a50",
-    176: "73415c0d4f0d5e447176434635",
-    177: "64766806487a7a6a5b3d6c4d5f13495d525a0273974c7e12574f4a2d4741423c76423b524e4c1172715547589b474c035b4a427346f19aa2",
-    178: "44405a05734b4f463f7c474c0e7341434a5a11f8e8889aac7f4c5f40694b4a0c",
-    179: "563d4a4940385c0e4a4c5de6e88c9aac7b4148513c5d0e4a7e6d594d4076464909",
-    180: "7a58e1ee9fdf63473f417a570d5941466b0e454a5a4d370e6e14567a155df3f3f8da926840f20d5a526cf472484b29584b50414a676e35",
-    181: "69414203524e9b0f4a774c5de289df7d4c3f5877ee0d4048496c474d4d2249465f42027e4e42095a4fe49f9e79027e583f4e480c",
-    182: "60077b414c045c016f4f40464a0e56779b543a77420e7a5a7a6c3b454c6a0d70493b4558e2da9072026b4476500d767d4741404f4e02",
-    183: "6f0747474e0b5d084b884b4c3f774246523f4042593b4f43737c2756b6999e670e4e4645410d494d056b740872480c5a474840545902",
-    184: "6749ef8968480508573841034c687a56465d48066b4847500e567e5c7aa1",
-    185: "b399344769496d035e74714c5d4745004f4f545b4d706c0c5c70115a4a975d0e3f414f4d7f5a54bada8b714e730c72460d5a41466b244a425b01454353584646447f0e8a48134d7a3e",
-    186: "7de293936d0b3f5703754c587a114a5a056806435d5256034c0e4d5e56f793270033",
-    187: "484357594b4f7d485b0f17a48e9738022e1925b91d",
-    188: "64094c714155035c494451035b5c5a467a6c0c9d5c4365673f4f50e2f08b7c476d4938f80d5e464a7a5a4a4a46460d4a465a56254a7b6c454c7a680e578d0e4b713e6b75405f3b43425e6c464346b8",
-    189: "b3d862473f5f7aee433b416b114150554345460e036f53095f9f5d287e3d5570404f470077423b503f5b45ff8e9a3449764170e54203",
-    190: "7a48724b564b414f7c0e47513f787e7b4c9040544b4e660d4a7e5650f394967a453f447af94835",
-    191: "6448504309574503534948464254777199425b3f7c5148467a40f39edf674d72496be344757b16",
-    192: "7d5b005046544f48585d026845015f4c0cf49f9a670e4a5c5b4049064b406d7e086b5e0c4d4f4316",
-    193: "695303554ff3de7d594c087171490343425b6f76484e085545475ade435a6f4d5a5a476d13",
-    194: "ce9693344d790c6be3425e4c077a4f504f41445d087a7a4d5c77681128b54148760c067d4641464502027e414e0c4c4e3fe2fef397c0",
-    195: "554f3f653fff457e3c47575154005749074d414b1d",
-    196: "4b4949097d476ef3daac7b5b4e714b026e49484748423f724f6b684f4f042b4f513f524c4d460e91460c4049075f45417e434608",
-    197: "614e5646b69b8d6c6f333b434b445303064c404d086b424c064d4841743024608a3b4e500c5f4845ea06544d7a4e03494f4102f060584f09454c69480d7d489b4324417a5a4a7a4e05116b4448b6998a66517a0c76f80d787344424545544608",
-    198: "7546584b5a0a48529b0e407a4a4b714849f89ddf6746077e5e52464953034242154d5f3f6d464c5c4e0803680543de515d404c76707c0c4ae38edf7b443f5876e64835",
-    199: "48415709464f51444e7f4a4b4c3f8c44576b7e4553244d790a6f454468017ee49f9e3a0c31",
-    200: "656b034142464c6c0e4e4a434403655c0c3f4a7a4744fbfff89fdf63436c267b4c44434e076d4b5146495340400e4b71594d3b6a415493070e00",
-    201: "6b3f6a4d71494b5b00774a3b59765f0df1889061523f456c295e59404b730e4a465a4402310e",
-    202: "6f3f7e4f535c548c434701430e4840716c5806313524754756773e6b454ce5da9c684d4c5d49303509",
-    203: "4b764a6e034b7e704c5a4f3b4b496c0c8a734209584e59476d235a4d3f495557745543035a774e43f189df7d494c24404d6d4f7e403c7e5f423f7d4273045c3fe59f9a3a",
-    204: "6b3f5e7a4e48404b426d0e564b4d0140464d4b7b44425d0f4e6cf9fb9c8d977a4a4f3f67024f4d405143497b0049793d47570f5206534e554b8c115a41027c7d595a5b5b420947464d6c565a08",
-    205: "3f",
-    206: "71478e4b513e0074465949e5dbdf5245507e575129454e51480c6d4f567a6e0f",
-    207: "6e5a0f067740494f9349424c09000c3f4943725f4633310d0824757754694306f7889a345b70593f414259410778414c4617",
-    208: "754b4d5f46396c0e517070435d457640f1da976c5c4307070b",
-    209: "794e42513f594d724d71a503030973774f56035f4e934246274a703f4f02747741745f700c40530e4170704b714a00b8d4",
-    210: "a87c476d493fe34c5b4c076b46475a08464c46481c",
-    211: "567059027c7d4712dfda9d614c46740e564b4d2b40585e6c4506707b0e57404406514e524bc1",
-    212: "6b4d415330310002574843580b3106",
-    213: "744b493f78496b783fc5928d7d4c7a0c524244494c4931000c297c494802405d41504d030d30",
-    214: "4c964b02766f0c6f5c463f40f7898b346f7e457bee43353207386249524a43093231",
-    215: "67117b764c9009563f467a48523b5c710e417070473f454be49fd1346f662676e55e6f7547515d530057494b550272493f9041563f76490d",
-    216: "7c764a5b017a7a540b1f3527c292966702684d660d0303",
-    217: "624e6d47470d060f",
-    218: "794d4e4756070600",
-    219: "600a4a419009563f7b4b71490e5d487b0c7054660203b8f0a87c476d493f4a5e0d405320",
-    220: "7a4a425c0144415f4f3e765d026b6e505b904e085a4d3f5e43662c53f9979a604a7642780d030309747043475740484345034147295f915c5677030c35",
-    221: "5540434045000c310a684f547249b8d4d1",
-    222: "5950310c4b42464c444e714b0c0d06017a49584c0a4445d0000c",
-    223: "563c687254feda9660056c0c7ee7413b7d09565b45414e080907",
-    224: "6b41444f09469740463f717a3a",
-    225: "73fe938c34557e55310d03",
-    226: "64094f7e5847035c4e0d454c08514c5141474e09549647513f78707455b8d4d11e7677493fe644696e4640094d55505207794b0e56777a6c4431d007",
-    227: "6d47497069490f0059f98fd866473f58704c0d68414d54061d04",
-    228: "6e7676705d4f020733",
-    229: "759248510e5576684e09447ba00300",
-    230: "4f4b416c3e5747500702b8f0ab7c4b6c0c68ea54353207",
-    231: "7b0948415543075d470e457688440c5d47416db697966650705e15ff420d5d4f7e5d06734671300d33",
-    232: "6c403303714c463031d00f024842553f4a47573c505de3da9775547a266b4c0d59484c7a0e5b4c5d5303475a4d3e7347447a21",
-    233: "657d1170429686345b70593f4b4c4947006b0e444c5d4f49285740525d089d4f4f7a5f4331080eb6a39e6c0e0701",
-    234: "6b7143560a7def232800574907fb6c000c0d",
-    235: "7c4d9b296f74584a0d7e4f5a5051000c0913497342155f6fe49b9166464a717a3f5b495a577e6407081d",
-    236: "5d4f494d5a49d00d060d706a705e02727902070b",
-    237: "534d693b4a7a0c74e2630c07d011654a523ee6553f70456b264144095b494b5db6fbf7e189967b4c313335",
-    238: "6e3f447a6a7a016f470e5d444a4511594a430cd009137946463d764f585b5e6d02b8b89cae97720272417b58405c000c31",
-    239: "744b553f46426c693f6f5b4d45774f026c589f5a577a074a5f020702167e553b5c464c3f744b477559410c7c49557ad0080d",
-    240: "624d43f3b6f093916d00727a070d670b5f4d014f4f464203594e7252434756155f913d45484d4f0f0e020954410273484d4b020702",
-    241: "df29407e697bde5a460f4a76554b0e5d457a3b4b47506d4e69246bf8da8b664845294f7a5e31",
-    242: "564f4d415670040d313d5758e588863a0c31",
-    243: "7b77465f7e0a4776793f44590e467e7d4e4e4768510c4b4602d00117",
-    244: "4a77490e60737a4c4741404e01564f6cfdda967a0eff454b287445500f5841025e4b7a3d7bf9917d063109",
-    245: "7d447a0a61737471f17246790e6f7e5448020207",
-    246: "784b448d3d454644423f476cb6e2f7939160477b0c714c5a350635",
-    247: "787646470e6f427a094b4f4e7e5c76525fb699906c4d680314544c0e7a587a1142424e3b78434e7b07",
-    248: "4c793f4be38d78095a404c4a034c6b034fec4c4b752c42eb49426d7bb6938b33513f58704c0d77496f4a300d0724535f6d5b51000c31df",
-    249: "65470c544d71590e724d5f7c754831b8d4df494d3b4d7b4448403b5e703b4e5b50487a6c067e6a7a54efde794bf95e49753c76483f76e361155e767c44690c",
-    250: "dc2efaf3daac7c5076427a03607a417f4a700f094b73153f6b4d520c464642502a8e5b506f715a4306ff89df75473b4b7746070035",
-    251: "6176434a4b0c02313e7273793f75e28c6840ec414f757b1574766aff7373033135",
-    252: "787547ae32e3e28f9e7802774d6c034b4c404b7a4a03296155085b3e7e40443f7458478c000c31",
-    253: "7d465c3e5d59f3da8d7d566a7a433e414c497244311f0d24405c4b71560242427090413b577654447a310903",
-    254: "65406e764c0b351db6ad976d027b457b0354425c077d4b414c45442743575c524a409b4a026b4f065d4145e5b6e1958d7846202646e4583c4a4f0e41487365035d5c464f4654d00831",
-    255: "6b475141480d3031b659414d690dcd63e4782f2b48792e7d25fe917022434d7f107d6b5d0847563f716e6e51b6989a34517a4d73464903",
-    256: "7d4f7a0e704c58445e03037c5b4c5a4b094b5b45f4434d6d7b0f5f41fe785a107143683f",
-    257: "573f4e44f8dd8b294740407f3c6b734a0e484556080f072c49774d507e0345590341e2c1",
-    258: "5a7352683f425c543b5464560c576df244fb49286f41115a466217",
-    259: "aa4b4d5c473f4b5e460d5b47e6f3b6e29b8d7f513f43710340542345704a5b0d060f0c5555556b3d424a434406684e4847d00d06",
-    260: "67566d6b0e4d714c0c4574557a060035066c565a5c07744340b697907b45236d5d7a7f447e3e516f496a5246000c48424708594b7b3fb6414e662361416955705a0e6c4f4a4f094a4235030b",
-    261: "df294c5c5d8a0e4a6a5e6d670c3506146e04410c4b49f193916f44404e086b5e035d4a725b39584153781141425c485b0f0706",
-    262: "b54a5c747e09310e0c7b485e4731350207644de249454702310c",
-    263: "52623ef29b8a6e46524c5b0b030303744b433b5b4f5a0e4d71455115794c4856417099096c4b4f70707d484b1f0d00",
-    264: "6b5a026841680742065e745f6b4c45f3da8b63034976584715434c095a41fc5d02724d7150447472080131",
-    265: "aa454b096a7372404d4340453f7c7e554db6978a72590e4b4d15424c43476c454b5e7e0848713d567345683d437e428d7474421e3130",
-    266: "74404b5b460eff670272553f547e594a7759466c15b34b70426f4519",
-    267: "7b49f3da9c7c4b73486d464303070915794a465a4403404c557b3f5a4a7a0e4a4297467f5e4b4700494d714424",
-    268: "61673f4c476e4f466b495ab8d4d1217e464c086850500e4d754157266b444066744c7c0c5f78437042aa7c7c021e31",
-    269: "5757084d484d09e234407a02311e3f6442680d407f71de43114e7a47435d40b69f87644d6c493f5042404c5377474c4422554e42513f7f424b5a46388a034d5b46703f4b5a766d5d08080311",
-    270: "52086df39fd12700066009564843034c6b350300",
+    92: "610e557e70583b45700c5a454b0277744f3f4240f3da927b507a0c6b4a407e09",
+    93: "7a52715a0d3133",
+    94: "51460e04350b",
+    95: "524d985c515b0c31303e",
+    96: "604cfd8fd12704",
+    97: "784b000c315f404273114d4f594f665b3c517e3d564c417b8a4b4d5512",
+    98: "6957016cb68e977102734d6c570d6b43467c783f46460a6f427a0c7c4a5c50914302",
+    99: "6e4f455d585c09037a4b494e47094f41464440476c8d3c",
+    100: "62467302e2da997b5078496b0354745d5b067a6b576202",
+    101: "7e5a0849566a66de47513f534c0c474c495d246f40776d0c7f5e705eb699937b517a4831",
+    102: "7d7e4c6d4d095276765b1078475d4f3f8a4c08404630",
+    103: "4b46473f69436f5b07f99cdf70455a0e716e6d7f56087a4b7f0e7ef84e7f6f7e0f",
+    104: "605d5d0e6896425c0752424c536bb683907c1f",
+    105: "600f456b686a0368585c410c57464b3f6b42449f704b6f5531237454034d496f7a0e586b3f5f44454b3f41476e8e794709444af7939127",
+    106: "6e40402c570c5470f95f67037a4e5c565c075e450d2c46f98fdf645b555d09424207",
+    107: "6e44795b5b6a003fe842767b03744212",
+    108: "b340435b05",
+    109: "63094d5b516b09556a7f6603",
+    110: "72fe9b8b294f544c095c425303567e574b714b20",
+    111: "6a0d6f764a754713b7034b414209404b45500e4a7a6c07",
+    112: "6b4ffd8fd3345b70593f44423b475c523e694a6f445ce0450c4e4b00",
+    113: "5241955606330c",
+    114: "6f4478096c4e4c4440b5454b72493f654b6d976d0951527e294b5940484643783e434c303fdfda9c665f434a0e4a7a735b207776500c504b6d754d4e764349a503d0",
+    115: "624f514b424548434408415c52034e7afa8ad1",
+    116: "55513f5877460d4945537a3d4c415243754f3f6148419a4b4c33015f414a2269f77a0e424c5a51444846413f6f910a507a7c730954734d09497e684c07",
+    117: "7cf38edf674a7a0c7e4f5e74085e4770684c4d055747004e4c2259975d480e5677480e46467a3c5c44463b4a485f4a4c30",
+    118: "d48f8b345177493f40426e444d483968094144554d004e465c46d2234140463f564d68107d4847474f3f454c5c4c0e436f9f535d2543663e5473726cf3da8b634d3f4a7a464172464e5532",
+    119: "6b4140464b0852495a5d428a4c440e4b710d5a414d3f6448444e4a765c57b8",
+    120: "b29a66026c5c7651446f085e4f6c095c41577c49494d0f4a67de454b4b02564d4574464c042448444d005046f3da9d9a9c0c60e52def2dfe7fce6c85bc2c367d86499326d1cb38353e14c6f5f825479c7a1e027521fbe59afe0458062f3701312aad9eff570b1d15473c39e9d1",
+    121: "b13c798168c06b602f4669577bad6ac9425b7c1a73cf3cee6374744778e01b89735c671032c77dc474477f017ac97fd37b44667670fe60d871723523667361bb702f443766e936927e9f7f7172545ac87e8b727a0c",
+    122: "57496dab5e74584b3b4b5359573f6f7a444143750a77498c4c0424497a445c40414f3ee2614755094e44594303567a7a924d7b11427b40294c45510840fa96df695d4c577547575706",
+    123: "685de3da9e784d714931a503",
+    124: "5e434377435559036f7c76470e",
+    125: "6b680a7343904e084f513f52444c0f416db66a5b4c400d4945056f7a975e33",
+    126: "4d40094a714678114c680c5d4b780676e5da91665e0f424b446b08775e5d7e404b506e0a",
+    127: "56035f4e40480d0831e295df76473f4e66ab457e5f07684f424f0d",
+    128: "3133316449416e04",
+    129: "524d985c515b0c310f",
+    130: "604640433f",
+    131: "c2614b4f5b095642534f563f7a8c4d3f504171064445434d4f01f49b9c7f286b433f54457e5f423b524e4f5a3f7f7a454f424433",
+    132: "5297416e043102",
+    133: "6008404d68015e4c4e4477ec7102684466ab64de5a485415535e4c5b4440550346f3889a25",
+    134: "4b414a0e6b3f5e4f7272097c4c447a585a035c4f5a5303427ae58e967a5b3f4379034072464c08",
+    135: "5375425c0b070e",
+    136: "784b7c71950a62456a020706484d6d01495f4a5a67e26147e54ad0",
+    137: "745a465c0e6c414d4b78026f447c5d3b42425109b6b3df7a5e405e5e477b165a4c4077714a3d584b754d4f520e56779f7c03485b444c523b574649434f4d2d574f4d016bb6899a6c0e",
+    138: "644e4e6b62690809714141474d3e4b4c727b904f68593e",
+    139: "684c4609563f4a46434e456809504a58e4da9b7c5e5600",
+    140: "635b3f4c6a45543b455d0369493f484d42432a574e76e5da9875567a0c7ce7425e4c4331000c",
+    141: "6f4d405f4d0e56779753064e4858f3295a4909444003080d",
+    142: "51777e3c5b4c568a0774783f504f5c067659516f660a7a447b0cf3899c75527a0d",
+    143: "5d56593b5a4f7a52064b4170686b0959915f350431",
+    144: "6503455b516b3d5f6b5f533d6bfe6c0e6142444493606962042670693d474f5df3b6ff8edf634b73403f4b4c6b584c483e4c7a4d404808",
+    145: "6d4740056bde6b745e6d580c484d476be2da926c0e2376476b3b476e5f5a0654730e",
+    146: "6149485f5a6a313f9d464d4f3b45710d",
+    147: "654741493e",
+    148: "794a7a4f52b67f465c495ede4751403f7a4445067947765f4a3b4e4f40762c6bf9da887c476d493f57454850077d4b4e4c46461f",
+    149: "674a5c477a060706",
+    150: "ad46473f5d7a593f4d42557e7b5c3e6d566958497c42467199117d42430c77434c7a30",
+    151: "6b4de4da8c7b57730c72565e6f085b43737d4047056f464b507ad23c70784059494045156a447e11784de29fdf67477e407a470d744e4f0678735b09445d40034b5a7a5a904a5c640c",
+    152: "48447809734747085146085d437c5f4b794f439b0f4d687a5e516b73474c490c",
+    153: "4b47495bf3da8c665f435d0e4f7e51095c7a6f5d094c75086e4d7e5248d23b4e5b573d4e7a5108545c554f2c68ff96933443735b7e5a5e3b5e527d4043580d",
+    154: "59726d4c569b583b4b7148094d58476d330c31",
+    155: "6858f37b0e5540474648de524b446b3b4c7e48013d51460a59574751e69f9b29534c4a41704a2353774048795f3f59777a583d4d8a764c6f0f577a475e417e074d474f09563f424c4c30",
+    156: "c59f8f7d45444d4d6c0e1b6b480506101c1d1c037d63",
+    157: "df45493f407e755f744d903e5e7c5c0771475945465a48036a700e407a2768457af8da907a026b447a03407a5805066d73095e40094e474c7e924c5f09414df2035ae40d4f5174005d4e40064543404c42f80d9643680d6b740c7b4b704d3d465331",
+    158: "7c4648efda8b7b4e7b0c6a680c6b407e450d534543566f49156042465e4a7171de46437b084b4b7a72094c48e68e86034c405c0e517a7e46554e4009447e444242568d0a424c6803",
+    159: "7ae348076849427e064c46424000544e70b68e9078463f596c035a734d5b433e4469265e47553b4f425170de59485847454a026a5e0e754c583d6f423ff59592710277496d4601115f414f7d453d5b485506585d47567ade7f4f5d7843f8999a655676427800",
+    160: "717a5157494b484c5108176b76b9de17182b1c3fdb60",
+    161: "5268095a404b4f7e4a0d7b7e494a4b5b91696c065d4701594842493f5441544a534e44035946f3f0926655475b497740027e5409484c4141580f0d5de40d5b7a0d7b7e4f74469b7a096940076c584b434722594b7b3f404b78756f3c4b4d6d4bb69b916d0a4c414056764e5c4305495c5e035a41f946d0",
+    162: "65385b7a3b4e78477009694755705d4945035b424545514773b688907b4f6c0c7ee75f7e494d5f30274842454f4d460854444c084b865d455c4b705f02095c7742094141537a5a47f9762341f80e8d5a4b4f4405474c3b5f4472594b02784370783f53414d6ff3d4",
+    163: "be344e76586b4f483b4d48547244785e05066f035c964f594e405a09690e517e5a24480868744658463b554f484b4769efda997d456a5e7a03427d0848066942704d472c4f4d088a484909404f454c59436601427e516d0d5a414d3f544d5a509f40417a0f",
+    164: "60084d733e4b7e786fb68e8d7541740c70450d685d4a4e3e5e744b41524f414f6d154d904a026f444b45776c403f5c7543440d46423ff7da93685e4a5c0e437c71465f71670c",
+    165: "7f46586b7541417a5f0eba1d8a5900031f1312131d03696a",
+    166: "6445034276e5999062476d497b035e7440780c4d4f55575d5c40764741148e734353465fab444c3b493ef5929a67563f4379034969495e436c5e33",
+    167: "6f46534a7f075d40448d4b027d453b524e7a087b7444754a705fff898bad76224d774542466d71410e44494d6f4f735d9b493f4f713d654c4248da67b67ae567785f24",
+    168: "7e45efddf0e8ef5b473e765fda8c61ff60ef264c4a7baa9ceee48a504041556c2d6c4742efda947d466c0c6f4f4c624147413e597c4b07",
+    169: "6f48086b5a4b0e4a915c4c7a550943480f6f44560e6b74496b41baf08b7c476d493fe25e0d4807794f4b4d5c01474f7a49430946430d9f2c5a4a6a754a3d4b40544a3b4e4708400e5577496f43067441934347720b",
+    170: "65f3e4b69c9691637d65384c6b15682b719fbd3b377d86499b21d1cb3822667bc391e86a0f946955022c2bfcad93e31813553b22473d3ead4997e9500b7f1d063f31e35ddf8c0376ca3bb8728b7e6d68057d337f046fc768b4734f33",
+    171: "03780869c970b7787f3e732f1b76b63e87243929614f2a",
+    172: "48fb3f9c70734b2d445b41f24cf94f65443c011e49ea01bb407d51534d150e9440af5628545a030057c44fb203764b48480c4ab150e7426a4b4d05104aeb4c87",
+    173: "728d4c55434a52c9537007454f0c539353b04e66082b49ec5bd94782087e5a6e410d4ea9050d637a4783499f584a4aef459c5c6e0c3d43ec40b50b52486d4b1b58f649e94570436d4c0c0eca41ac00106c515a104bf3476d100851de55ed5179430e50dd48d75d4f542d0d",
+    174: "c0579241d25057561a13c252725d3153b947ae599b405b5c1552ea54905a41427414a0598b5364451447dd44cb1b2d4b5256e95de34f891851560252a44aad5491335952454e44490c4348495a5f5d5e51431f",
+    175: "69574a475f59585048160b054e50161903000a0b1a7d77",
+    176: "741a58554a54241a0a5528536d",
+    177: "722d49655e235b3352684d28496a503e49381a2153255f6f4e385f5b553c5f73533a1a2152331a3a552d542d5b33547b4c3556315b395f71",
+    178: "7209494152075b071a05547d094372417d68065b7a697b136e7e5a4941464c0f",
+    179: "67027c9f493c4603454a4b414a51793f5b7347520e423f7641595c9f404b4d4a02",
+    180: "7d7649f59aac7b4c09487e5a0e56777c5d0849765a42040978a8fb9ff5ff694c4705764f405b3f6e5d5a4f714f4b085f58fce49591ff22",
+    181: "6845493b5a46473f7a41475d6b5b0e414711fbe59fdf7943715f764c432741486842024246453b5d4441457e720ef7e2b6979a27",
+    182: "67ab49464839e13c5b46604049035c4d6c643c44410e4650438c25417a570efb9fdf7b576b0c70ed0d59414e6c0e4f4246524047400c",
+    183: "56004246470be2da9a6247710c744d425a094f7059024f474f7c2d6008424f4c3f9642717f0e41710c6b711144503e5e7c42725e54b8",
+    184: "bb916d557e553303643c71095e4c41564a4840035c48455a085a9f5e4731",
+    185: "554a0940694d5f0e684c417874437ab696967a5a43475a055949295177725b33115c4543475a450c035242fa92295c4c0869774d572a657a530f5b4e566f4540464a026b433fe29fd1",
+    186: "56576b0c6c57447770071c0769004b49574a08776b0b5b3f715b518a0e433f55514d7f441f",
+    187: "c59f8f6047724e7a510d1c1b537702021012131d027365",
+    188: "6a084a754189074748766c0ee5958a6f436c3e406f4252661d034c576f2c5d404450460a5d095f5cfb9b7d4674754107454b507a274b4a55ff9e9a67026a5f3fe2430d5d4f765d024e494f5e4b4c461d",
+    189: "660f687a0c8d4b47713e765905fb838c714e79023fc2590d5e466c2443035f4e40434d085a41087f3f5b40766f4b0295474f70707033",
+    190: "7a43764b575876414b08ff89df7047794571e2597e446611444856564c4e494d4107414d8c4b0c",
+    191: "577c547a0d594c006b42705f705b44f89d936d027e5b7ee048434c433f5d4d4e4d557347404520",
+    192: "53693d559b5b484f526c0d557a0156f3da9d7147710c73fe5f7e48094e435b45005749074741481c",
+    193: "576cde5d4a7a3d5241483f41f89fdf77436a5f76e54a3b68415b5a00444a55465a5c4b5020",
+    194: "614a450943f0da8b6141554c09404c544f4c7a69087b544d5d4e55162a6b4c4c4ebade5d5e44477b330c424c4f0e7379065d40444011",
+    195: "6893077a3c58414b027149f78edf604d3f4876ee12",
+    196: "7941423f7c4d534d017c406c76424d3f564f4b9a4b4c3f724f5d5c4d452a4f513f594d40470870f0b6ff94df7847784971ef033532",
+    197: "6b5d5d480042544a5a040e4e7a465f050f4970f2da8b7b4c07714b4148062b6a590c7653066c7c4747085646477106424d4e0e98495a4c074f5256433b4f47434d2b4f4fe4919a65303f6f474b03435a545e4b09416c0a4a494e5d4e7a6a4b07",
+    198: "ac7457465f0c485eeb06414078494d464a4345b67d410a485d5d7a4c5f3f42902743553b5849705e461f3f650afbda8d614c714571ec0d74695d12464600574f4a4c06",
+    199: "7a414f0946915c407649467a4800e4938b66484b6c244d4508554b445f3f41547a7c000d06",
+    200: "4852034d4d41955008424b747b3b6157b8daab75497e4176e5483b6b484123444f4a48403b5c4b517a9f5f40763f404e5a4d3f5e73484035",
+    201: "683fe1959170476d0c76450d4540543f49504c5d5103415d286c6a724049b6fef3889a2b",
+    202: "6b3f4f7e5359585b427b0e43034f494c5b5a0c3103286c775d59de5d4847513f7e4372485c480e",
+    203: "4a4472423f4f4cfb9f8d7502774d6c0359454c076f4155465a2b58700043676d41504d018a4e4a4f455d0f5c767a26467069434342027a677a0d46f794d87d005a4a4d30",
+    204: "52076d7b4e784e4a7a6f095c467e0341714f977f42475c0148507044245577454e4f3b6f064f4b7e5543f39edf664709475a513f5771456d6e432d6f71547851086bf9da9c75526b596d460d4a41486c5a510d",
+    205: "08",
+    206: "7346584b513e017e465f4d6db7b6d7968872505415434d514d0151425c7a5307",
+    207: "526f00037c404d424c4b409b240f0e767071464b110807237746476d4709476d4608964f547a005f465c0cf79693334e48714b1d02",
+    208: "7c49465f493853066c7243465c494f4d4602469b524908",
+    209: "7346436b3d5b705d42733e037c46436b116c494bf794f57d4c3f4d3f4844404649700951034b4e4e4143443f",
+    210: "4846476d7806414c694bb68e976c57064e464b4819",
+    211: "6b4a680e417e423fc20d4f5b427e4502574044f4405d5f507b3f41443f6a447e116d43594511",
+    212: "6a7a7152310300b6b29a7852310231",
+    213: "df45480975705e47037b49514143463e524f4b7b79471cb8d4f54741423f4d57515b440d0302",
+    214: "4c48433f745d035c4943034d435d8a03654c4a7a7a400c310325634c6d41450d0231",
+    215: "63067f747bf8dd8b34557e426b03594209447043470340445f470d087e5a22444d6d6b9740416b6f0c6f5b4f7b0cfb9fdf7a4d6b0c6be403",
+    216: "4f7440410957415a072d487747423f6849870f",
+    217: "6976437243083506",
+    218: "4a414f70780c3103",
+    219: "67b6999e7a056b0c79e2437f3c5d5a4c004b465f091f0c157b779b5c473f6b5503416a1c",
+    220: "7c496c6f0d42586941b6938c34566d55764d4a275d483f5d435a0852424f465c5b40464907207a4f934b5677744c7803000749735c74436b4d43e2d4",
+    221: "b47d507649310d030d624e6d47470d060f",
+    222: "6e5a03034a7e454372754757d007065d4369480272430eb8d4",
+    223: "b63455765f7703594540543f5947514d014c02475a564245d0000c",
+    224: "5c424f7e3e595d48590e55765e4b064b7e0d",
+    225: "c292966702684d6602",
+    226: "6f485048714a025740485a084a46455b0cf45a4a7a3c527255e4958d344f6a5f6bab4f7e3c5d5a4c52450d0809",
+    227: "644145465e460cde574d6a3b6d7e07e2959034517343680d0303",
+    228: "644e7441564c060f03",
+    229: "724f494a095f475d42094d9b0f",
+    230: "7677756c3b50f783de1e7677456cab5a7a6508",
+    231: "7b0948415543076f410e4576697b016b9640530e6f766f544c522ae295df604a7e583f4e4c7503",
+    232: "6d4b041373427a333107010c7e755cde4d414a0266735309417ff848246f4c086b7f4b43095043e388df7b55710c73e24b7e23",
+    233: "6054094f4e4f5f0750475b02779f45420e5b0878f98f9170286b447eff0d4e484a7a5b473207467f4633",
+    234: "60477246084f427d74de5a4d3f4749310000",
+    235: "67744c12c4958f71025e406b425f0307093f7a4a462272575a4c4d7973474c783e7e72456a4d96d13a0c",
+    236: "4f407a425e480709315d564c580140470d",
+    237: "64565d08934b027058563e066cf38edf644509405d6a245c4c3ffa282a53034b46f87a474d4d09",
+    238: "7c917c3d734959483f574111574b4e4b1375724a3e0c4ffe9fdf4c43516d726d082a7a4a7a28644f417f4c5e0d",
+    239: "7d449b03444c506a3f6c577b784448056c5c7c6f527a0c72e4390c07f4505d0f5276ee104c7759715841024e4e554700b8b8",
+    240: "d5e0979a344476737f0772493a3c56066d4d0e4b4443471146424756974954275d4c3d7749444e1f3102b6e5f9da93784c78062704",
+    241: "660e464369450344700a44766b7a0d5a41443f634b6d5e915c286b4803584448583c72407506",
+    242: "634074485741350300446e5a5366d0080d",
+    243: "764a4be4f3b69e966d00726606494f594e40554858034b4c11",
+    244: "7b73430a6b5d76429a7447400365405347094e5d026b4f4626474c55b67d473f6b769b0e4d40426d0d",
+    245: "7a464c0d5d774f4046764f7c0e52f6899420071f",
+    246: "5d4a7e106c7a455447447649463f746c0de39b967a567a483f4d426c0b",
+    247: "74777871095446473f4b484a52604a5855094f91424d6d3326594738614703494245017f4b7ef2d4",
+    248: "a86c0ee6585d563f534c4e400e4b5e037e7a7eff90054a7a41465e7a0a4a6b3a6cb56f47710e4e7e53460d266159515f873c",
+    249: "61420a517a406bb6fff8899e7a473e0c57460d794d7c4e70035d4111476a5b4c4b503f54694354efda8f645a6840700340403b427642295d4b7c745201",
+    250: "4d496b793f75fe8c65474c0560474a417a4d02ab484a240668eb5d0d7070fa83f564576d5c7050483b41680f6a4c094a724f31",
+    251: "62415c4b7ad20d564446084c595c7a4d4b717243789ca896755d7a433f",
+    252: "77414b3b587645564f4e0c777f553b7a7e4ffa9b6d008164523c6f3f477372aa7d69486d350233",
+    253: "6eeb35aae2929a345076586a42413b4a7e48774d07245958764d4f004d4547404e00b54750767b07",
+    254: "6d4fe4939a2f06350f494b500e7f437b115a41570c7d7b4574717a2cf78a7d4fe845437f3c6b493f6ae27b6c0d68745e7146b16180cf958a334e730c704d415409546a4844465a00",
+    255: "64416c76490631355e4d915c0278585144300978e2dd8c34567074257c424d023b486a450347560e4f6a4256034c7ade557e7d73434931",
+    256: "4b4f480e7b736f4c563a13c2929a66473f4d6d46274046557a0e504c58445e024d474408",
+    257: "61de4d43710752094f45f8f2b68e977102744966a5274c4e465c4b06766f03475d1f",
+    258: "7e4b478a067e524b035142563e6be470474c7c27fe65b66760723e",
+    259: "59616b77efde7e5a440c695f6f7b09454f50746f3b724bb697861e407048660d030343526c5a024f414a480268475940060007",
+    260: "605c538a0e4d717b0f4041fc78071e310c556b6d6b0d4af89fdf644e5b4b115e6a7f4b4642005c52405d537b33084375470c5e4b4db6b662774a16524a5c43745f2b54454f73ab4ff0000c35",
+    261: "67114452685cde4b5d5c50660b266a0a4408f4f3f1e694917d4c780c6b4c0d5e41486824504c58440c724154746e00",
+    262: "6841534f460f0c00de71475d463031006f7e40484d75093106",
+    263: "63620642425c4f4f6f4857b8d4d12973414a08697a5f3f714c775114574f4d554042440869467370900e767e4e020635",
+    264: "6e6b08597a55064209454e685944fd6c015d41de424b694915774c3b5c764e500c414842e593906f030007",
+    265: "7c7754036c4e7442574340443d7c4d50450345545a5cde414b17684872455b41425c473f7242075d44e25e00444d7151767470b8",
+    266: "ad976c5c430940560d405a0747476e4b465d4b5033236576624f5d4017",
+    267: "4a964c084d4a76724d5b495f0d000c247577456942034e526b493f5946f3da9c644a497b5c47710a4546404caa",
+    268: "635b3f487e564a7368435d31d0030e7a407a3b5948590e4d715d662c56fa9b86684349096c7a5c4c40024f4c49023506",
+    269: "686b3d417a423c690e7d49df3d5343473f7d42460e48294df779476d4d3f55675c426c48036d7093476f457244412555fe9b8b344670496c4d0a590942694b4c034d594a5b591c3f",
+    270: "560e517a4b0704d0633b5f4b4c004756310f35",
 }
 
 
 ig_msg_e_digest = "540a862fc08283823b61d8f56a39d08636348e0c273c5b4c99ddd6a25e343c91"
-subtitles_en_digest = "be54c6abc7dbecba20f344219a6b22a8e23bdb0877dee35a1721d530d86dfd44"
+subtitles_en_digest = "ea45d6e4fb195f521a215e3fac27609b9f2b6abc84590ce0c6a10b07d9d4aa6d"
 
 
 def xor(first, second):
     return bytes(x ^ y for x, y in zip(first, second))
 
 
 def decode_english_subtitles(ig_msg_e: BinaryIO):
@@ -315,7 +315,35 @@
 
     decoded_sub_digest = sha256_hash.hexdigest()
 
     if decoded_sub_digest != subtitles_en_digest:
         raise RuntimeError("subtitle digest mismatch")
 
     return decoded_subs
+
+
+def encode_english_subtitles(ig_msg_e: BinaryIO, subs_e: dict[int, str]):
+    pos = ig_msg_e.tell()
+    ig_msg_e.seek(0, os.SEEK_SET)
+    ig_msg_e_bin = ig_msg_e.read()
+    ig_msg_e.seek(pos, os.SEEK_SET)
+
+    computed_ig_msg_e_digest = hashlib.sha256(ig_msg_e_bin).hexdigest()
+    if computed_ig_msg_e_digest != ig_msg_e_digest:
+        raise RuntimeError("IG_MSG_E.OBJ digest mismatch")
+
+    sub_size = sum(len(sub) for sub in subs_e.values())
+    xor_base = ig_msg_e_bin.replace(b"\x00", b"")[:sub_size]
+
+    position = 0
+    sha256_hash = hashlib.sha256()
+    encoded_sub_e: dict[int, str] = {}
+    for num, sub in subs_e.items():
+        sub_bytes = sub.encode("utf-8")
+        enc = xor(xor_base[position:], sub_bytes)
+        position += len(sub)
+        sha256_hash.update(sub_bytes)
+        encoded_sub_e[num] = enc.hex()
+
+    decoded_sub_digest = sha256_hash.hexdigest()
+
+    return encoded_sub_e, decoded_sub_digest
```

### Comparing `zeroundub-1.3.2/zeroundub/zero/tim2.py` & `zeroundub-1.3.3/zeroundub/zero/tim2.py`

 * *Files identical despite different names*

### Comparing `zeroundub-1.3.2/zeroundub.egg-info/PKG-INFO` & `zeroundub-1.3.3/zeroundub.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zeroundub
-Version: 1.3.2
+Version: 1.3.3
 Summary: Undub project for Tecmo's Project Zero - the EU version (the first one) for the PS2
 Author: karas84
 Project-URL: Homepage, https://github.com/karas84/ProjectZeroUndub
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7
@@ -218,11 +218,12 @@
 - [wagrenier](https://github.com/wagrenier) again, for his help with replacing all game models with the Japanese ones
 - [pgert](https://forums.pcsx2.net/Thread-PCSX2-Widescreen-Game-Patches?pid=240786#pid240786)
   and the whole [PCSX2 community](https://forums.pcsx2.net/) for the great patches that can
   be injected into the game
 - [pelvicthrustman](https://www.psx-place.com/threads/ps2-patch-engine-by-pelvicthrustman.19167/)
   and [Snaggly](https://github.com/Snaggly) for their tools to inject patches into the ELF
 - [weirdbeardgame](https://github.com/weirdbeardgame/), for the Kirie camera bug fix
+- [FlamePurge](https://www.romhacking.net/community/1523/) for proofreading the subtitles
 - All the guys out there on so many forums I've lost track of, that released bits of
   information about many game file formats
 - Finally, to 2010 me, who painstakingly spent weeks building his own undub, reversed-engineered
   the game data and transcribed all FMVs and cutscenes
```

### Comparing `zeroundub-1.3.2/zeroundub.egg-info/SOURCES.txt` & `zeroundub-1.3.3/zeroundub.egg-info/SOURCES.txt`

 * *Files identical despite different names*

