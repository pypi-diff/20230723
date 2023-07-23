# Comparing `tmp/inspec-0.3.tar.gz` & `tmp/inspec-0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/inspec-0.3.tar", last modified: Sun Jan 10 07:58:16 2021, max compression
+gzip compressed data, was "inspec-0.5.tar", last modified: Sun Jul 23 19:21:37 2023, max compression
```

## Comparing `inspec-0.3.tar` & `inspec-0.5.tar`

### file list

```diff
@@ -1,33 +1,58 @@
-drwxrwxrwx   0 kevin     (1000) root         (0)        0 2021-01-10 07:58:16.702919 inspec-0.3/
--rwxrwxrwx   0 kevin     (1000) root         (0)     6269 2021-01-10 07:58:16.702619 inspec-0.3/PKG-INFO
--rwxrwxrwx   0 kevin     (1000) root         (0)     4574 2021-01-10 07:56:05.000000 inspec-0.3/README.md
-drwxrwxrwx   0 kevin     (1000) root         (0)        0 2021-01-10 07:58:16.692882 inspec-0.3/inspec/
--rwxrwxrwx   0 kevin     (1000) root         (0)      221 2021-01-10 07:41:36.000000 inspec-0.3/inspec/__init__.py
--rwxrwxrwx   0 kevin     (1000) root         (0)     8636 2021-01-10 07:47:59.000000 inspec-0.3/inspec/cli.py
--rwxrwxrwx   0 kevin     (1000) root         (0)     7750 2021-01-10 05:02:05.000000 inspec-0.3/inspec/colormap.py
--rwxrwxrwx   0 kevin     (1000) root         (0)      845 2021-01-08 05:30:04.000000 inspec-0.3/inspec/const.py
--rwxrwxrwx   0 kevin     (1000) root         (0)     7775 2021-01-10 07:41:36.000000 inspec-0.3/inspec/core.py
--rwxrwxrwx   0 kevin     (1000) root         (0)      818 2021-01-10 07:41:36.000000 inspec-0.3/inspec/defaults.py
-drwxrwxrwx   0 kevin     (1000) root         (0)        0 2021-01-10 07:58:16.701905 inspec-0.3/inspec/gui/
--rwxrwxrwx   0 kevin     (1000) root         (0)        0 2021-01-07 07:46:20.000000 inspec-0.3/inspec/gui/__init__.py
--rwxrwxrwx   0 kevin     (1000) root         (0)     7618 2021-01-10 07:41:36.000000 inspec-0.3/inspec/gui/audio_viewer.py
--rwxrwxrwx   0 kevin     (1000) root         (0)    23700 2021-01-10 07:41:36.000000 inspec-0.3/inspec/gui/base.py
--rwxrwxrwx   0 kevin     (1000) root         (0)     2143 2021-01-10 07:41:36.000000 inspec-0.3/inspec/gui/image_viewer.py
--rwxrwxrwx   0 kevin     (1000) root         (0)    10153 2021-01-10 03:00:28.000000 inspec-0.3/inspec/gui/live_audio_viewer.py
--rwxrwxrwx   0 kevin     (1000) root         (0)     2258 2021-01-09 00:10:09.000000 inspec-0.3/inspec/gui/utils.py
--rwxrwxrwx   0 kevin     (1000) root         (0)     2071 2021-01-10 07:48:55.000000 inspec-0.3/inspec/help.py
--rwxrwxrwx   0 kevin     (1000) root         (0)     3909 2021-01-10 07:41:36.000000 inspec-0.3/inspec/io.py
--rwxrwxrwx   0 kevin     (1000) root         (0)     6140 2021-01-10 07:30:22.000000 inspec-0.3/inspec/maps.py
--rwxrwxrwx   0 kevin     (1000) root         (0)      807 2021-01-07 21:20:53.000000 inspec-0.3/inspec/paginate.py
--rwxrwxrwx   0 kevin     (1000) root         (0)     3323 2021-01-10 05:02:05.000000 inspec-0.3/inspec/render.py
--rwxrwxrwx   0 kevin     (1000) root         (0)    13599 2021-01-10 07:41:36.000000 inspec-0.3/inspec/transform.py
--rwxrwxrwx   0 kevin     (1000) root         (0)      533 2021-01-10 07:41:36.000000 inspec-0.3/inspec/var.py
-drwxrwxrwx   0 kevin     (1000) root         (0)        0 2021-01-10 07:58:16.698216 inspec-0.3/inspec.egg-info/
--rwxrwxrwx   0 kevin     (1000) root         (0)     6269 2021-01-10 07:58:16.000000 inspec-0.3/inspec.egg-info/PKG-INFO
--rwxrwxrwx   0 kevin     (1000) root         (0)      563 2021-01-10 07:58:16.000000 inspec-0.3/inspec.egg-info/SOURCES.txt
--rwxrwxrwx   0 kevin     (1000) root         (0)        1 2021-01-10 07:58:16.000000 inspec-0.3/inspec.egg-info/dependency_links.txt
--rwxrwxrwx   0 kevin     (1000) root         (0)       61 2021-01-10 07:58:16.000000 inspec-0.3/inspec.egg-info/entry_points.txt
--rwxrwxrwx   0 kevin     (1000) root         (0)       95 2021-01-10 07:58:16.000000 inspec-0.3/inspec.egg-info/requires.txt
--rwxrwxrwx   0 kevin     (1000) root         (0)        7 2021-01-10 07:58:16.000000 inspec-0.3/inspec.egg-info/top_level.txt
--rwxrwxrwx   0 kevin     (1000) root         (0)       38 2021-01-10 07:58:16.703012 inspec-0.3/setup.cfg
--rwxrwxrwx   0 kevin     (1000) root         (0)     1169 2021-01-10 07:41:36.000000 inspec-0.3/setup.py
+drwxr-xr-x   0 kevin      (501) staff       (20)        0 2023-07-23 19:21:37.315434 inspec-0.5/
+-rw-r--r--   0 kevin      (501) staff       (20)     1064 2023-07-01 22:57:55.000000 inspec-0.5/LICENSE
+-rw-r--r--   0 kevin      (501) staff       (20)     2682 2023-07-23 19:21:37.315296 inspec-0.5/PKG-INFO
+-rw-r--r--   0 kevin      (501) staff       (20)      926 2023-07-22 21:54:12.000000 inspec-0.5/README.md
+-rw-r--r--   0 kevin      (501) staff       (20)     1465 2023-07-23 19:21:30.000000 inspec-0.5/pyproject.toml
+-rw-r--r--   0 kevin      (501) staff       (20)       38 2023-07-23 19:21:37.315473 inspec-0.5/setup.cfg
+drwxr-xr-x   0 kevin      (501) staff       (20)        0 2023-07-23 19:21:37.302441 inspec-0.5/src/
+drwxr-xr-x   0 kevin      (501) staff       (20)        0 2023-07-23 19:21:37.303151 inspec-0.5/src/inspec.egg-info/
+-rw-r--r--   0 kevin      (501) staff       (20)     2682 2023-07-23 19:21:37.000000 inspec-0.5/src/inspec.egg-info/PKG-INFO
+-rw-r--r--   0 kevin      (501) staff       (20)     1636 2023-07-23 19:21:37.000000 inspec-0.5/src/inspec.egg-info/SOURCES.txt
+-rw-r--r--   0 kevin      (501) staff       (20)        1 2023-07-23 19:21:37.000000 inspec-0.5/src/inspec.egg-info/dependency_links.txt
+-rw-r--r--   0 kevin      (501) staff       (20)       47 2023-07-23 19:21:37.000000 inspec-0.5/src/inspec.egg-info/entry_points.txt
+-rw-r--r--   0 kevin      (501) staff       (20)      205 2023-07-23 19:21:37.000000 inspec-0.5/src/inspec.egg-info/requires.txt
+-rw-r--r--   0 kevin      (501) staff       (20)       19 2023-07-23 19:21:37.000000 inspec-0.5/src/inspec.egg-info/top_level.txt
+-rw-r--r--   0 kevin      (501) staff       (20)     4613 2023-07-23 19:20:10.000000 inspec-0.5/src/inspec.py
+drwxr-xr-x   0 kevin      (501) staff       (20)        0 2023-07-23 19:21:37.307675 inspec-0.5/src/inspec_core/
+-rw-r--r--   0 kevin      (501) staff       (20)        0 2023-07-23 05:39:38.000000 inspec-0.5/src/inspec_core/__init__.py
+drwxr-xr-x   0 kevin      (501) staff       (20)        0 2023-07-23 19:21:37.310116 inspec-0.5/src/inspec_core/app/
+-rw-r--r--   0 kevin      (501) staff       (20)        0 2023-07-23 06:09:26.000000 inspec-0.5/src/inspec_core/app/__init__.py
+-rw-r--r--   0 kevin      (501) staff       (20)    19514 2023-07-23 06:28:43.000000 inspec-0.5/src/inspec_core/app/app.py
+-rw-r--r--   0 kevin      (501) staff       (20)     5765 2023-07-23 06:29:37.000000 inspec-0.5/src/inspec_core/app/draw.py
+-rw-r--r--   0 kevin      (501) staff       (20)     2398 2023-07-23 05:56:53.000000 inspec-0.5/src/inspec_core/app/events.py
+-rw-r--r--   0 kevin      (501) staff       (20)     4781 2023-07-23 06:12:33.000000 inspec-0.5/src/inspec_core/app/key_handlers.py
+-rw-r--r--   0 kevin      (501) staff       (20)     2127 2023-07-23 05:08:55.000000 inspec-0.5/src/inspec_core/app/paginate.py
+-rw-r--r--   0 kevin      (501) staff       (20)     1056 2023-07-23 06:12:42.000000 inspec-0.5/src/inspec_core/app/test_paginate.py
+-rw-r--r--   0 kevin      (501) staff       (20)     3991 2023-07-23 06:13:28.000000 inspec-0.5/src/inspec_core/app/video_example.py
+-rw-r--r--   0 kevin      (501) staff       (20)     8739 2023-07-23 06:04:43.000000 inspec-0.5/src/inspec_core/audio_utils.py
+-rw-r--r--   0 kevin      (501) staff       (20)     3511 2023-07-23 19:19:48.000000 inspec-0.5/src/inspec_core/cli.py
+-rw-r--r--   0 kevin      (501) staff       (20)     3567 2023-07-23 06:05:01.000000 inspec-0.5/src/inspec_core/colormaps.py
+drwxr-xr-x   0 kevin      (501) staff       (20)        0 2023-07-23 19:21:37.311951 inspec-0.5/src/inspec_core/components/
+-rw-r--r--   0 kevin      (501) staff       (20)        0 2023-07-23 06:09:17.000000 inspec-0.5/src/inspec_core/components/__init__.py
+-rw-r--r--   0 kevin      (501) staff       (20)     2833 2023-07-23 06:29:53.000000 inspec-0.5/src/inspec_core/components/audio_view.py
+-rw-r--r--   0 kevin      (501) staff       (20)      974 2023-07-23 06:16:38.000000 inspec-0.5/src/inspec_core/components/base_view.py
+-rw-r--r--   0 kevin      (501) staff       (20)     2230 2023-07-23 19:19:32.000000 inspec-0.5/src/inspec_core/components/image_view.py
+-rw-r--r--   0 kevin      (501) staff       (20)     3887 2023-07-23 06:30:07.000000 inspec-0.5/src/inspec_core/components/live_audio_view.py
+-rw-r--r--   0 kevin      (501) staff       (20)     2682 2023-07-23 06:16:38.000000 inspec-0.5/src/inspec_core/components/size.py
+-rw-r--r--   0 kevin      (501) staff       (20)     1287 2023-07-23 06:30:17.000000 inspec-0.5/src/inspec_core/components/test_preserve_aspect_ratio.py
+-rw-r--r--   0 kevin      (501) staff       (20)     2197 2023-07-23 06:30:24.000000 inspec-0.5/src/inspec_core/components/test_views.py
+-rw-r--r--   0 kevin      (501) staff       (20)     7662 2023-07-23 06:30:31.000000 inspec-0.5/src/inspec_core/components/video_view.py
+drwxr-xr-x   0 kevin      (501) staff       (20)        0 2023-07-23 19:21:37.313334 inspec-0.5/src/inspec_core/inspec_curses/
+-rw-r--r--   0 kevin      (501) staff       (20)       58 2023-07-23 06:11:04.000000 inspec-0.5/src/inspec_core/inspec_curses/__init__.py
+-rw-r--r--   0 kevin      (501) staff       (20)     3515 2023-07-23 06:01:39.000000 inspec-0.5/src/inspec_core/inspec_curses/color_pair.py
+-rw-r--r--   0 kevin      (501) staff       (20)     4088 2023-07-23 06:10:57.000000 inspec-0.5/src/inspec_core/inspec_curses/context.py
+-rw-r--r--   0 kevin      (501) staff       (20)      356 2023-07-23 06:16:38.000000 inspec-0.5/src/inspec_core/inspec_curses/debug.py
+-rw-r--r--   0 kevin      (501) staff       (20)     2431 2023-07-23 06:11:35.000000 inspec-0.5/src/inspec_core/inspec_curses/test_color_pair.py
+-rw-r--r--   0 kevin      (501) staff       (20)     1314 2023-07-23 06:30:43.000000 inspec-0.5/src/inspec_core/inspec_curses/test_context.py
+-rw-r--r--   0 kevin      (501) staff       (20)      135 2023-07-23 06:28:43.000000 inspec-0.5/src/inspec_core/inspec_curses/utils.py
+-rw-r--r--   0 kevin      (501) staff       (20)      172 2023-07-23 05:08:55.000000 inspec-0.5/src/inspec_core/options.py
+drwxr-xr-x   0 kevin      (501) staff       (20)        0 2023-07-23 19:21:37.314958 inspec-0.5/src/inspec_core/render/
+-rw-r--r--   0 kevin      (501) staff       (20)       93 2023-07-23 06:07:45.000000 inspec-0.5/src/inspec_core/render/__init__.py
+-rw-r--r--   0 kevin      (501) staff       (20)     1869 2023-07-23 06:08:07.000000 inspec-0.5/src/inspec_core/render/chars.py
+-rw-r--r--   0 kevin      (501) staff       (20)     4097 2023-07-23 06:08:17.000000 inspec-0.5/src/inspec_core/render/colors.py
+-rw-r--r--   0 kevin      (501) staff       (20)      714 2023-07-23 06:08:21.000000 inspec-0.5/src/inspec_core/render/display.py
+-rw-r--r--   0 kevin      (501) staff       (20)     9243 2023-07-23 06:16:38.000000 inspec-0.5/src/inspec_core/render/renderer.py
+-rw-r--r--   0 kevin      (501) staff       (20)      728 2023-07-23 06:08:44.000000 inspec-0.5/src/inspec_core/render/test_render.py
+-rw-r--r--   0 kevin      (501) staff       (20)     1751 2023-07-23 05:08:55.000000 inspec-0.5/src/inspec_core/render/types.py
+-rw-r--r--   0 kevin      (501) staff       (20)     6850 2023-07-23 06:08:50.000000 inspec-0.5/src/inspec_core/render/x256.py
+-rw-r--r--   0 kevin      (501) staff       (20)     1973 2023-07-23 06:14:15.000000 inspec-0.5/src/inspec_core/test_spectrogram.py
```

