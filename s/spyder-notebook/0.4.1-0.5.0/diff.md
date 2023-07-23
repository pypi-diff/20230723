# Comparing `tmp/spyder-notebook-0.4.1.tar.gz` & `tmp/spyder-notebook-0.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "spyder-notebook-0.4.1.tar", last modified: Fri Apr  7 12:18:30 2023, max compression
+gzip compressed data, was "spyder-notebook-0.5.0.tar", last modified: Sun Jul 23 12:20:15 2023, max compression
```

## Comparing `spyder-notebook-0.4.1.tar` & `spyder-notebook-0.5.0.tar`

### file list

```diff
@@ -1,96 +1,384 @@
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.702907 spyder-notebook-0.4.1/
--rw-r--r--   0 jitse     (1000) jitse     (1000)    32380 2023-04-07 12:13:19.000000 spyder-notebook-0.4.1/CHANGELOG.md
--rw-r--r--   0 jitse     (1000) jitse     (1000)     1302 2023-03-22 21:00:49.000000 spyder-notebook-0.4.1/LICENSE
--rw-r--r--   0 jitse     (1000) jitse     (1000)      402 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/MANIFEST.in
--rw-r--r--   0 jitse     (1000) jitse     (1000)     4705 2023-04-07 12:18:30.702907 spyder-notebook-0.4.1/PKG-INFO
--rw-r--r--   0 jitse     (1000) jitse     (1000)     4108 2023-03-02 18:35:01.000000 spyder-notebook-0.4.1/README.md
--rw-r--r--   0 jitse     (1000) jitse     (1000)      755 2023-02-05 14:13:01.000000 spyder-notebook-0.4.1/runtests.py
--rw-r--r--   0 jitse     (1000) jitse     (1000)       38 2023-04-07 12:18:30.702907 spyder-notebook-0.4.1/setup.cfg
--rw-r--r--   0 jitse     (1000) jitse     (1000)     3241 2023-04-07 11:43:03.000000 spyder-notebook-0.4.1/setup.py
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      461 2023-03-22 21:00:49.000000 spyder-notebook-0.4.1/spyder_notebook/__init__.py
--rw-r--r--   0 jitse     (1000) jitse     (1000)       92 2023-04-07 12:15:19.000000 spyder-notebook-0.4.1/spyder_notebook/_version.py
--rw-r--r--   0 jitse     (1000) jitse     (1000)      971 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/config.py
--rw-r--r--   0 jitse     (1000) jitse     (1000)     1260 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/confpage.py
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.690907 spyder-notebook-0.4.1/spyder_notebook/locale/de/
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/de/LC_MESSAGES/
--rw-r--r--   0 jitse     (1000) jitse     (1000)     3533 2023-02-21 20:41:03.000000 spyder-notebook-0.4.1/spyder_notebook/locale/de/LC_MESSAGES/spyder_notebook.mo
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.690907 spyder-notebook-0.4.1/spyder_notebook/locale/es/
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/es/LC_MESSAGES/
--rw-r--r--   0 jitse     (1000) jitse     (1000)     3163 2023-02-21 20:41:03.000000 spyder-notebook-0.4.1/spyder_notebook/locale/es/LC_MESSAGES/spyder_notebook.mo
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.690907 spyder-notebook-0.4.1/spyder_notebook/locale/fr/
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/fr/LC_MESSAGES/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      553 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/locale/fr/LC_MESSAGES/spyder_notebook.mo
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.690907 spyder-notebook-0.4.1/spyder_notebook/locale/hr/
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/hr/LC_MESSAGES/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      630 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/locale/hr/LC_MESSAGES/spyder_notebook.mo
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.690907 spyder-notebook-0.4.1/spyder_notebook/locale/hu/
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/hu/LC_MESSAGES/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      557 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/locale/hu/LC_MESSAGES/spyder_notebook.mo
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.690907 spyder-notebook-0.4.1/spyder_notebook/locale/ja/
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/ja/LC_MESSAGES/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      549 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/locale/ja/LC_MESSAGES/spyder_notebook.mo
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.690907 spyder-notebook-0.4.1/spyder_notebook/locale/pl/
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/pl/LC_MESSAGES/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      700 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/locale/pl/LC_MESSAGES/spyder_notebook.mo
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.690907 spyder-notebook-0.4.1/spyder_notebook/locale/pt_BR/
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/pt_BR/LC_MESSAGES/
--rw-r--r--   0 jitse     (1000) jitse     (1000)     3148 2023-02-21 20:41:03.000000 spyder-notebook-0.4.1/spyder_notebook/locale/pt_BR/LC_MESSAGES/spyder_notebook.mo
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/ru/
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/ru/LC_MESSAGES/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      720 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/locale/ru/LC_MESSAGES/spyder_notebook.mo
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/zh_CN/
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/locale/zh_CN/LC_MESSAGES/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      562 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/locale/zh_CN/LC_MESSAGES/spyder_notebook.mo
--rw-r--r--   0 jitse     (1000) jitse     (1000)     3268 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/notebookplugin.py
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook/server/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      211 2023-02-15 11:49:49.000000 spyder-notebook-0.4.1/spyder_notebook/server/__init__.py
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.698907 spyder-notebook-0.4.1/spyder_notebook/server/build/
--rw-r--r--   0 jitse     (1000) jitse     (1000)   428744 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/1.bundle.js
--rw-r--r--   0 jitse     (1000) jitse     (1000)     3379 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/2.bundle.js
--rw-r--r--   0 jitse     (1000) jitse     (1000)   165742 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/674f50d287a8c48dc19ba404d20fe713.eot
--rw-r--r--   0 jitse     (1000) jitse     (1000)   444379 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/912ec66d7572ff821749319396470bde.svg
--rw-r--r--   0 jitse     (1000) jitse     (1000)    77160 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/af7ae505a9eed503f8b8e6982036873e.woff2
--rw-r--r--   0 jitse     (1000) jitse     (1000)   165548 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/b06871f281fee6b241d60582ae9369b9.ttf
--rw-r--r--   0 jitse     (1000) jitse     (1000)  4023125 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/bundle.js
--rw-r--r--   0 jitse     (1000) jitse     (1000)    27911 2023-04-07 12:18:18.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/commands.js
--rw-r--r--   0 jitse     (1000) jitse     (1000)    16858 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/fcad2f97acb3c868bd1ca7629d36d80e.svg
--rw-r--r--   0 jitse     (1000) jitse     (1000)    98024 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/fee66e712a8a08eef5805a46892932ad.woff
--rw-r--r--   0 jitse     (1000) jitse     (1000)     4664 2023-04-07 12:18:18.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/index.js
--rw-r--r--   0 jitse     (1000) jitse     (1000)     2270 2023-04-07 12:18:18.000000 spyder-notebook-0.4.1/spyder_notebook/server/build/tooltip.js
--rw-r--r--   0 jitse     (1000) jitse     (1000)      386 2023-03-22 21:00:49.000000 spyder-notebook-0.4.1/spyder_notebook/server/dark-theme-hack.css
--rw-r--r--   0 jitse     (1000) jitse     (1000)      622 2023-03-22 21:00:49.000000 spyder-notebook-0.4.1/spyder_notebook/server/index.css
--rw-r--r--   0 jitse     (1000) jitse     (1000)      641 2023-03-22 21:00:49.000000 spyder-notebook-0.4.1/spyder_notebook/server/index.html
--rw-r--r--   0 jitse     (1000) jitse     (1000)     3003 2023-04-06 15:01:53.000000 spyder-notebook-0.4.1/spyder_notebook/server/main.py
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.698907 spyder-notebook-0.4.1/spyder_notebook/tests/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      817 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/tests/test_config.py
--rw-r--r--   0 jitse     (1000) jitse     (1000)    15676 2023-03-22 21:00:49.000000 spyder-notebook-0.4.1/spyder_notebook/tests/test_plugin.py
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.698907 spyder-notebook-0.4.1/spyder_notebook/utils/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      350 2023-02-05 14:13:01.000000 spyder-notebook-0.4.1/spyder_notebook/utils/__init__.py
--rw-r--r--   0 jitse     (1000) jitse     (1000)      241 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/utils/localization.py
--rw-r--r--   0 jitse     (1000) jitse     (1000)    13004 2023-04-06 15:01:53.000000 spyder-notebook-0.4.1/spyder_notebook/utils/servermanager.py
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.698907 spyder-notebook-0.4.1/spyder_notebook/utils/templates/
--rwxr-xr-x   0 jitse     (1000) jitse     (1000)    16050 2023-04-06 15:01:53.000000 spyder-notebook-0.4.1/spyder_notebook/utils/templates/welcome-dark.html
--rw-r--r--   0 jitse     (1000) jitse     (1000)    15935 2023-04-06 15:01:53.000000 spyder-notebook-0.4.1/spyder_notebook/utils/templates/welcome.html
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.698907 spyder-notebook-0.4.1/spyder_notebook/utils/tests/
--rwxr-xr-x   0 jitse     (1000) jitse     (1000)    10038 2023-04-06 15:01:53.000000 spyder-notebook-0.4.1/spyder_notebook/utils/tests/test_servermanager.py
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.702907 spyder-notebook-0.4.1/spyder_notebook/widgets/
--rw-r--r--   0 jitse     (1000) jitse     (1000)      348 2023-02-05 14:13:01.000000 spyder-notebook-0.4.1/spyder_notebook/widgets/__init__.py
--rw-r--r--   0 jitse     (1000) jitse     (1000)    16231 2023-03-22 21:00:49.000000 spyder-notebook-0.4.1/spyder_notebook/widgets/client.py
--rw-r--r--   0 jitse     (1000) jitse     (1000)     2049 2023-02-11 22:17:54.000000 spyder-notebook-0.4.1/spyder_notebook/widgets/dom.py
--rwxr-xr-x   0 jitse     (1000) jitse     (1000)     3942 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/widgets/example_app.py
--rw-r--r--   0 jitse     (1000) jitse     (1000)    13613 2023-04-06 15:01:53.000000 spyder-notebook-0.4.1/spyder_notebook/widgets/main_widget.py
--rwxr-xr-x   0 jitse     (1000) jitse     (1000)    16672 2023-04-06 15:01:53.000000 spyder-notebook-0.4.1/spyder_notebook/widgets/notebooktabwidget.py
--rwxr-xr-x   0 jitse     (1000) jitse     (1000)     4344 2023-02-05 14:13:44.000000 spyder-notebook-0.4.1/spyder_notebook/widgets/serverinfo.py
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.702907 spyder-notebook-0.4.1/spyder_notebook/widgets/tests/
--rw-r--r--   0 jitse     (1000) jitse     (1000)     4083 2023-03-22 21:00:49.000000 spyder-notebook-0.4.1/spyder_notebook/widgets/tests/test_client.py
--rwxr-xr-x   0 jitse     (1000) jitse     (1000)     7799 2023-03-22 21:00:49.000000 spyder-notebook-0.4.1/spyder_notebook/widgets/tests/test_notebooktabwidget.py
--rwxr-xr-x   0 jitse     (1000) jitse     (1000)     2511 2023-04-06 15:01:53.000000 spyder-notebook-0.4.1/spyder_notebook/widgets/tests/test_serverinfo.py
-drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-04-07 12:18:30.694907 spyder-notebook-0.4.1/spyder_notebook.egg-info/
--rw-r--r--   0 jitse     (1000) jitse     (1000)     4705 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook.egg-info/PKG-INFO
--rw-r--r--   0 jitse     (1000) jitse     (1000)     2576 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook.egg-info/SOURCES.txt
--rw-r--r--   0 jitse     (1000) jitse     (1000)        1 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook.egg-info/dependency_links.txt
--rw-r--r--   0 jitse     (1000) jitse     (1000)       74 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook.egg-info/entry_points.txt
--rw-r--r--   0 jitse     (1000) jitse     (1000)       95 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook.egg-info/requires.txt
--rw-r--r--   0 jitse     (1000) jitse     (1000)       33 2023-04-07 12:18:30.000000 spyder-notebook-0.4.1/spyder_notebook.egg-info/top_level.txt
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.553721 spyder-notebook-0.5.0/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    34212 2023-07-23 00:09:44.000000 spyder-notebook-0.5.0/CHANGELOG.md
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     1286 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/LICENSE
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      403 2023-07-23 12:02:03.000000 spyder-notebook-0.5.0/MANIFEST.in
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4705 2023-07-23 12:20:15.553721 spyder-notebook-0.5.0/PKG-INFO
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4108 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/README.md
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      755 2023-02-05 14:13:01.000000 spyder-notebook-0.5.0/runtests.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)       38 2023-07-23 12:20:15.553721 spyder-notebook-0.5.0/setup.cfg
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3223 2023-07-22 23:28:28.000000 spyder-notebook-0.5.0/setup.py
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      857 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/spyder_notebook/__init__.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)       92 2023-07-23 11:42:47.000000 spyder-notebook-0.5.0/spyder_notebook/_version.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      971 2023-02-05 14:13:44.000000 spyder-notebook-0.5.0/spyder_notebook/config.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     1260 2023-02-05 14:13:44.000000 spyder-notebook-0.5.0/spyder_notebook/confpage.py
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/locale/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/locale/de/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/locale/de/LC_MESSAGES/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3658 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/locale/de/LC_MESSAGES/spyder_notebook.mo
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/locale/es/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/locale/es/LC_MESSAGES/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     2796 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/locale/es/LC_MESSAGES/spyder_notebook.mo
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/locale/fr/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/locale/fr/LC_MESSAGES/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      553 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/locale/fr/LC_MESSAGES/spyder_notebook.mo
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/locale/hr/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/locale/hr/LC_MESSAGES/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      630 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/locale/hr/LC_MESSAGES/spyder_notebook.mo
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/locale/hu/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/locale/hu/LC_MESSAGES/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      557 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/locale/hu/LC_MESSAGES/spyder_notebook.mo
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/locale/ja/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/locale/ja/LC_MESSAGES/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      549 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/locale/ja/LC_MESSAGES/spyder_notebook.mo
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/locale/pl/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/locale/pl/LC_MESSAGES/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      700 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/locale/pl/LC_MESSAGES/spyder_notebook.mo
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/locale/pt_BR/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/locale/pt_BR/LC_MESSAGES/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3493 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/locale/pt_BR/LC_MESSAGES/spyder_notebook.mo
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/locale/ru/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/locale/ru/LC_MESSAGES/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      720 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/locale/ru/LC_MESSAGES/spyder_notebook.mo
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/locale/zh_CN/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/locale/zh_CN/LC_MESSAGES/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      562 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/locale/zh_CN/LC_MESSAGES/spyder_notebook.mo
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3212 2023-07-22 23:30:14.000000 spyder-notebook-0.5.0/spyder_notebook/notebookplugin.py
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/server/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      211 2023-02-15 11:49:49.000000 spyder-notebook-0.5.0/spyder_notebook/server/__init__.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      257 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/spyder_notebook/server/__main__.py
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/server/app/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/server/app/build/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/server/app/build/themes/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.521721 spyder-notebook-0.5.0/spyder_notebook/server/app/build/themes/@jupyterlab/
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/server/app/build/themes/@jupyterlab/theme-dark-extension/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    17760 2023-07-23 12:20:10.000000 spyder-notebook-0.5.0/spyder_notebook/server/app/build/themes/@jupyterlab/theme-dark-extension/index.css
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook/server/app/build/themes/@jupyterlab/theme-light-extension/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    16493 2023-07-23 12:20:10.000000 spyder-notebook-0.5.0/spyder_notebook/server/app/build/themes/@jupyterlab/theme-light-extension/index.css
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3194 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/spyder_notebook/server/main.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     1503 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/spyder_notebook/server/notebook-template.html
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.549721 spyder-notebook-0.5.0/spyder_notebook/server/static/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    34160 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/1cb1c39ea642f26a4dfe.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9600 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/26683bf201fb258a2237.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5464 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/30e889b58cbc51adfbb0.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    15944 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/32792104b5ef69eded90.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    20832 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/355254db9ca10a09a3b5.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     1116 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/36e0d72d8a7afc696a3e.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   203030 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/373c04fd2418f5c77eea.eot
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5148 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/3bc6ecaae7ecf6f8d7f8.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    40808 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/3de784d07b9fa8f104c1.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   101648 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/3f6d3488cf65374f6f67.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     1368 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/481e39042508ae313a60.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3244 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/5cda41563a095bd70c78.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    22340 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/721921bab0d001ebff02.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     1136 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/72bc573386dd1d48c5bb.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    34034 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/79d088064beb3826054f.eot
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    21480 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/870673df72e70f87c91a.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    34464 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/88b98cad3688915e50da.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    76736 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/8ea8791754915a898a31.woff2
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    19776 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/8ea8dbb1b02e6f730f55.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   918991 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/9674eb1bd55047179038.svg
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    78268 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/9834b82ad26e2a37583d.woff2
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     1885 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/_8883-_5fa1-_1b46-_2abd-_0836.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    19360 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/a009bea404f7a500ded4.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   747927 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/a3b9817780214caf01e8.svg
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9908 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/af04542b29eaac04550a.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   202744 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/af6397503fcefbd61397.ttf
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    11852 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/af96f67d7accf5fd2a4a.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    12660 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/b418136e3b384baaadec.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   144714 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/be0a084962d8066884f7.svg
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    37590 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/build_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   257114 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5792 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/c49810b53ecc0d87d802.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    17604 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/c56da8d69f1a0208b8e0.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    16276 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/cb9e9e693192413cde2b.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   133988 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/cda59d6efffa685830fd.ttf
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   134294 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/e4299464e7b012968eed.eot
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    13224 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/e42a88444448ac3d6054.woff2
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    33736 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/e8711bbb871afd8e9dea.ttf
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    89988 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/f9217f66874b0c01cd8c.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    14628 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/fc6ddf5df402b263cfb1.woff
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7541 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_lang-json_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6178 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_lang-wast_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5401 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_apl_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3067 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_asciiarmor_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9152 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_asn1_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     8537 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_asterisk_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     2931 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_brainfuck_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3488 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_cmake_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    11185 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_cobol_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    10534 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_coffeescript_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5598 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_commonlisp_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7566 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_cypher_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     8408 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_d_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     2006 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_diff_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    11047 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_dockerfile_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5555 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_dtd_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    11141 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_dylan_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5741 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_ebnf_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9545 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_ecl_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4626 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_eiffel_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5988 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_elm_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9648 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_factor_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5429 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_fcl_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5803 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_forth_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9807 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_fortran_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    11252 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_gas_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6899 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_go_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9313 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_groovy_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9251 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_haskell_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3297 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_http_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6710 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_jinja2_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     8261 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_livescript_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6867 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_lua_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6428 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_mathematica_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4668 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_mbox_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    10919 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_mirc_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    10124 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_mllike_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6700 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_modelica_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7813 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_mscgen_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6318 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_mumps_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    11072 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_nginx_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6397 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_ntriples_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5448 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_octave_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7644 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_oz_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5217 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_pascal_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6206 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_pig_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3048 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_properties_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3127 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_protobuf_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     8393 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_puppet_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7826 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_q_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7635 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_r_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4570 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_rpm_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    11816 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_ruby_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6350 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_shell_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5151 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_sieve_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5484 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_smalltalk_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3339 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_solr_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7872 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_sparql_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3913 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_spreadsheet_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     8753 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_stex_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     8577 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_swift_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5821 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_tcl_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     8824 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_tiddlywiki_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9437 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_tiki_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3801 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_toml_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3179 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_troff_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9703 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_ttcn-cfg_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    10517 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_ttcn_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5659 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_turtle_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9660 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_vb_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7015 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_velocity_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7568 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_vhdl_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7032 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_webidl_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6161 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_yacas_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4569 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_yaml_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4617 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_codemirror_legacy-modes_mode_z80_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6451 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyter-notebook_docmanager-extension_lib_index_js-_e4b40.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6451 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyter-notebook_docmanager-extension_lib_index_js-_e4b41.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4192 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyter-notebook_documentsearch-extension_lib_index_js-_32b90.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4192 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyter-notebook_documentsearch-extension_lib_index_js-_32b91.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     8237 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyter-notebook_help-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    14218 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyter-notebook_ui-components_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4611 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_cell-toolbar-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    12684 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_celltags-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    10889 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_completer-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    10106 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_htmlviewer-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    16232 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_htmlviewer_lib_index_js-_f0bb0.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    16232 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_htmlviewer_lib_index_js-_f0bb1.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9308 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_hub-extension_lib_index_js-_9dda0.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9308 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_hub-extension_lib_index_js-_9dda1.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    11638 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_imageviewer-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    13198 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_imageviewer_lib_index_js-_afb90.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    13198 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_imageviewer_lib_index_js-_afb91.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4650 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_javascript-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7707 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_json-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5553 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_markedparser-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    10722 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_mathjax-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5515 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_nbformat_lib_index_js-_a6f70.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     5515 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_nbformat_lib_index_js-_a6f71.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9285 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_pdf-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    13364 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_property-inspector_lib_index_js-_90690.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    13364 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_property-inspector_lib_index_js-_90691.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6978 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_rendermime-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     1683 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_rendermime-interfaces_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3347 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_theme-dark-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3360 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_theme-light-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    11921 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_tooltip_lib_index_js-_d1c70.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    11921 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_tooltip_lib_index_js-_d1c71.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    11080 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_translation-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     3267 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_ui-components-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9222 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_jupyterlab_vega5-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7269 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_lumino_disposable_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     8242 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_lumino_keyboard_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     7598 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_lumino_properties_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9215 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_mathjax-full_js_mathjax_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    10388 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_mathjax-full_js_util_Options_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6629 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/node_modules_process_browser_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6660 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/packages_application-extension_lib_index_js-_90450.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     6660 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/packages_application-extension_lib_index_js-_90451.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   170833 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_autocomplete_dist_index_js-node_modules_lezer_lr_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    88348 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_commands_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   111075 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_lang-cpp_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    35592 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_lang-css_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    56584 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_lang-html_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    46770 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_lang-java_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   102602 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_lang-javascript_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   108950 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_lang-markdown_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   107893 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_lang-php_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    71985 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_lang-python_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    77183 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_lang-rust_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    45059 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_lang-sql_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    25029 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_lang-xml_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   108331 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_language_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    42827 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_clike_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    19460 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_clojure_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    13265 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_crystal_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    44777 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_css_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    19531 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_erlang_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    13733 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_gherkin_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    18343 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_haxe_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    15522 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_idl_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    41098 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_javascript_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    12430 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_julia_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    14518 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_nsis_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    31649 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_perl_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    13593 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_powershell_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    16191 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_python_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    15221 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_sas_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    13562 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_scheme_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    49821 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_sql_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    44130 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_stylus_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    14413 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_textile_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    14803 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_vbscript_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    24045 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_verilog_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    17016 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_legacy-modes_mode_xquery_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    57618 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_search_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   585046 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_codemirror_view_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    66298 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_fast-deep-equal_index_js-node_modules_json-schema-traverse_index_js-node-057f3c.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    46184 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyter-notebook_application-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)  1039276 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyter-notebook_application-extension_style_index_js-node_modules_jupyt-7c11f7.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    42632 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyter-notebook_application_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    24589 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyter-notebook_notebook-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    87145 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyter_ydoc_lib_index_js-node_modules_process_browser_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    65325 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_application-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   117692 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_application_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    35930 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_application_lib_mimerenderers_js-node_modules_jupyterlab_appl-fdcfe8.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   146227 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_apputils-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   684647 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_apputils_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    21206 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_cell-toolbar_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   155086 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_cells_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    44736 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_codeeditor_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    20938 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_codemirror-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   404138 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_codemirror_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   106502 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_completer_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    62765 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_console_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    95087 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_coreutils_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    47796 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_debugger-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   255058 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_debugger_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   419423 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_debugger_lib_panels_variables_gridpanel_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    52170 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_docmanager-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    80126 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_docmanager_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   106978 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_docregistry_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    15457 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_documentsearch-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    69870 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_documentsearch_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    58595 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_filebrowser-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   189164 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_filebrowser_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    88266 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_fileeditor-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    59831 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_fileeditor_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   284183 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_json-extension_lib_component_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    18242 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_launcher_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    34884 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_logconsole_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    33781 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_lsp-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   360406 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_lsp_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    35395 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_mainmenu-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    38403 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_mainmenu_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    15817 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_metadataform-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    29514 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_metadataform_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   161641 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_notebook-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   408495 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_notebook_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    47339 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_observables_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    59675 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_outputarea_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   111820 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_rendermime_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    17290 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_running_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   312806 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_services_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   400161 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_settingregistry_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    82326 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_shortcuts-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    27185 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_statedb_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    28515 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_statusbar_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    15306 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_toc-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    54057 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_toc_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    16126 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_tooltip-extension_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    36200 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_translation_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   705900 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_jupyterlab_ui-components_lib_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    79999 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lezer_common_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    30691 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lezer_highlight_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   114787 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lib0_buffer_js-node_modules_lib0_encoding_js-node_modules_lib0_observabl-50dfe2.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   198998 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lodash-es__baseClone_js-node_modules_lodash-es_get_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    49615 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lodash-es_has_js-node_modules_lodash-es_hasIn_js-node_modules_lodash-es_-930c1c.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    83073 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lumino_algorithm_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    80996 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lumino_application_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    40333 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lumino_commands_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    19970 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lumino_coreutils_dist_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    17562 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lumino_domutils_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    37389 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lumino_dragdrop_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    32321 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lumino_messaging_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    20949 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lumino_polling_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    21540 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lumino_signaling_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    27016 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lumino_virtualdom_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   551610 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_lumino_widgets_dist_index_es6_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    84092 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_marked_lib_marked_esm_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    27354 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_a11y_assistive-mml_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    17105 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_adaptors_browserAdaptor_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   118351 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_core_MathItem_js-node_modules_mathjax-full_js_core_MmlTr-144bb4.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    32398 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_core_MmlTree_MmlFactory_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   129649 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_core_MmlTree_MmlNodes_mo_js-node_modules_mathjax-full_js-e92534.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    89680 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_handlers_html_HTMLHandler_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   450064 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_input_tex_AllPackages_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   126224 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_input_tex_Configuration_js-node_modules_mathjax-full_js_-8c4c26.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   154837 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_input_tex_ParseOptions_js-node_modules_mathjax-full_js_i-0c5d92.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    37081 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_input_tex_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    33875 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_input_tex_require_RequireConfiguration_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   234379 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_output_chtml_fonts_tex_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   465381 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_output_chtml_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    33543 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_mathjax-full_js_ui_safe_SafeHandler_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)  1078623 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_react-dom_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    21903 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_react-toastify_dist_react-toastify_esm_mjs.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    92046 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_react_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   327447 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_regexp-match-indices_index_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   575730 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_rjsf_utils_dist_utils_esm_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   320313 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_rjsf_validator-ajv8_dist_validator-ajv8_esm_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)  3384152 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_vega-embed_build_vega-embed_module_js.bundle.js
+-rw-r--r--   0 jitse     (1000) jitse     (1000)   366817 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook/server/static/vendors-node_modules_yjs_dist_yjs_mjs.bundle.js
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.549721 spyder-notebook-0.5.0/spyder_notebook/tests/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      817 2023-04-29 21:10:29.000000 spyder-notebook-0.5.0/spyder_notebook/tests/test_config.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     8125 2023-07-22 23:30:14.000000 spyder-notebook-0.5.0/spyder_notebook/tests/test_plugin.py
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.549721 spyder-notebook-0.5.0/spyder_notebook/utils/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      350 2023-02-05 14:13:01.000000 spyder-notebook-0.5.0/spyder_notebook/utils/__init__.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      241 2023-02-05 14:13:44.000000 spyder-notebook-0.5.0/spyder_notebook/utils/localization.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    14226 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/spyder_notebook/utils/servermanager.py
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.549721 spyder-notebook-0.5.0/spyder_notebook/utils/templates/
+-rwxr-xr-x   0 jitse     (1000) jitse     (1000)    16050 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/spyder_notebook/utils/templates/welcome-dark.html
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    15935 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/spyder_notebook/utils/templates/welcome.html
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.549721 spyder-notebook-0.5.0/spyder_notebook/utils/tests/
+-rwxr-xr-x   0 jitse     (1000) jitse     (1000)     9910 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/spyder_notebook/utils/tests/test_servermanager.py
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.553721 spyder-notebook-0.5.0/spyder_notebook/widgets/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)      348 2023-02-05 14:13:01.000000 spyder-notebook-0.5.0/spyder_notebook/widgets/__init__.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    16346 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/spyder_notebook/widgets/client.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     2049 2023-02-11 22:17:54.000000 spyder-notebook-0.5.0/spyder_notebook/widgets/dom.py
+-rwxr-xr-x   0 jitse     (1000) jitse     (1000)     3942 2023-02-05 14:13:44.000000 spyder-notebook-0.5.0/spyder_notebook/widgets/example_app.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    13830 2023-07-22 23:30:14.000000 spyder-notebook-0.5.0/spyder_notebook/widgets/main_widget.py
+-rwxr-xr-x   0 jitse     (1000) jitse     (1000)    17725 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/widgets/notebooktabwidget.py
+-rwxr-xr-x   0 jitse     (1000) jitse     (1000)     4344 2023-02-05 14:13:44.000000 spyder-notebook-0.5.0/spyder_notebook/widgets/serverinfo.py
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.553721 spyder-notebook-0.5.0/spyder_notebook/widgets/tests/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4079 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/spyder_notebook/widgets/tests/test_client.py
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     9534 2023-06-29 13:39:11.000000 spyder-notebook-0.5.0/spyder_notebook/widgets/tests/test_main_widget.py
+-rwxr-xr-x   0 jitse     (1000) jitse     (1000)     7927 2023-07-22 23:29:27.000000 spyder-notebook-0.5.0/spyder_notebook/widgets/tests/test_notebooktabwidget.py
+-rwxr-xr-x   0 jitse     (1000) jitse     (1000)     2511 2023-06-29 13:39:07.000000 spyder-notebook-0.5.0/spyder_notebook/widgets/tests/test_serverinfo.py
+drwxr-xr-x   0 jitse     (1000) jitse     (1000)        0 2023-07-23 12:20:15.525721 spyder-notebook-0.5.0/spyder_notebook.egg-info/
+-rw-r--r--   0 jitse     (1000) jitse     (1000)     4705 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook.egg-info/PKG-INFO
+-rw-r--r--   0 jitse     (1000) jitse     (1000)    28935 2023-07-23 12:20:15.000000 spyder-notebook-0.5.0/spyder_notebook.egg-info/SOURCES.txt
+-rw-r--r--   0 jitse     (1000) jitse     (1000)        1 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook.egg-info/dependency_links.txt
+-rw-r--r--   0 jitse     (1000) jitse     (1000)       74 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook.egg-info/entry_points.txt
+-rw-r--r--   0 jitse     (1000) jitse     (1000)       84 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook.egg-info/requires.txt
+-rw-r--r--   0 jitse     (1000) jitse     (1000)       33 2023-07-23 12:20:14.000000 spyder-notebook-0.5.0/spyder_notebook.egg-info/top_level.txt
```

### Comparing `spyder-notebook-0.4.1/CHANGELOG.md` & `spyder-notebook-0.5.0/CHANGELOG.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,7 +1,27 @@
+## Version 0.5.0 (2023/07/24)
+
+This version is based on version 7 of Jupyter Notebook and version 4 of Jupyter Lab, thus profiting of many years of progress in Jupyter.
+
+### Mew Feature
+
+* Base the plugin on Jupyter Notebook v7 ([Issue 330](https://github.com/spyder-ide/spyder-notebook/issues/330), [Issue 400](https://github.com/spyder-ide/spyder-notebook/issues/400), [Issue 401](https://github.com/spyder-ide/spyder-notebook/issues/401), [Issue 402](https://github.com/spyder-ide/spyder-notebook/issues/402), [Issue 414](https://github.com/spyder-ide/spyder-notebook/issues/414), [PR 396](https://github.com/spyder-ide/spyder-notebook/pull/396), [PR 415](https://github.com/spyder-ide/spyder-notebook/pull/415), [PR 419](https://github.com/spyder-ide/spyder-notebook/pull/419), [PR 420](https://github.com/spyder-ide/spyder-notebook/pull/420), [PR 429](https://github.com/spyder-ide/spyder-notebook/pull/429))
+
+### Bug Fixes
+
+* Handle NotJSONError when closing a notebook tab ([Issue 432](https://github.com/spyder-ide/spyder-notebook/issues/432), [PR 437](https://github.com/spyder-ide/spyder-notebook/pull/437))
+* Ensure that the precise connection file is used when opening a console ([Issue 421](https://github.com/spyder-ide/spyder-notebook/issues/421), [PR 422](https://github.com/spyder-ide/spyder-notebook/pull/422))
+
+### Maintenance
+
+* Update translations ([PR 430](https://github.com/spyder-ide/spyder-notebook/pull/430))
+* Update GitHub test action ([PR 413](https://github.com/spyder-ide/spyder-notebook/pull/413))
+* Prepare for Spyder v6 ([Issue 278](https://github.com/spyder-ide/spyder-notebook/issues/278), [Issue 423](https://github.com/spyder-ide/spyder-notebook/issues/423), [PR 417](https://github.com/spyder-ide/spyder-notebook/pull/417), [PR 438](https://github.com/spyder-ide/spyder-notebook/pull/438))
+
+
 ## Version 0.4.1 (2023/04/07)
 
 ### Bug Fixes
 
 * Plugin now works when installed in a venv on Windows ([Issue 398](https://github.com/spyder-ide/spyder-notebook/issues/398), [PR 408](https://github.com/spyder-ide/spyder-notebook/pull/408))
 * Require Spyder version 5.4.3, which fixes a bug causing notebooks and other HTML content not to display on some Linux computers ([Issue 386](https://github.com/spyder-ide/spyder-notebook/issues/386), [PR 410](https://github.com/spyder-ide/spyder-notebook/pull/410))
 * Add New/Open Notebook items back to the notebook context menu ([Issue 404](https://github.com/spyder-ide/spyder-notebook/issues/404), [Issue 174](https://github.com/spyder-ide/spyder-notebook/issues/174), [PR 409](https://github.com/spyder-ide/spyder-notebook/pull/409))
```

### Comparing `spyder-notebook-0.4.1/LICENSE` & `spyder-notebook-0.5.0/LICENSE`

 * *Files 17% similar despite different names*

```diff
@@ -20,10 +20,10 @@
 OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 SOFTWARE.
 
 
 Server License
 ==============
 
-The files in the directory spyder_notebook/server are adapted from an example
-of the Jupyter Project and licensed under the revised BSD license. See the
+The files in the directory spyder_notebook/server are adapted from
+Jupyter Notebook and licensed under the BSD 3-Clause License. See the
 file spyder_notebook/server/LICENSE for details.
```

### Comparing `spyder-notebook-0.4.1/PKG-INFO` & `spyder-notebook-0.5.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spyder-notebook
-Version: 0.4.1
+Version: 0.5.0
 Summary: Jupyter notebook integration with Spyder
 Home-page: https://github.com/spyder-ide/spyder-notebook
 Author: Spyder Development Team
 License: MIT
 Keywords: spyder jupyter notebook
 Classifier: Development Status :: 4 - Beta
 Classifier: Framework :: Jupyter
```

### Comparing `spyder-notebook-0.4.1/README.md` & `spyder-notebook-0.5.0/README.md`

 * *Files identical despite different names*

### Comparing `spyder-notebook-0.4.1/runtests.py` & `spyder-notebook-0.5.0/runtests.py`

 * *Files identical despite different names*

### Comparing `spyder-notebook-0.4.1/setup.py` & `spyder-notebook-0.5.0/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -68,21 +68,20 @@
         print("\nERROR: Server components are missing!! Please run "
               "'python setup.py sdist' first.\n")
         sys.exit(1)
 
 
 REQUIREMENTS = [
     'spyder>=5.4.3,<6',
-    'jinja2',
-    'jupyter_core',
     'nbformat',
-    'notebook>=4.3',
+    'notebook>=7,<8',
     'qtpy',
     'qdarkstyle',
     'requests',
+    'tornado',
     'traitlets'
 ]
 
 
 with open('README.md', 'r') as f:
     DESCRIPTION = f.read()
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/config.py` & `spyder-notebook-0.5.0/spyder_notebook/config.py`

 * *Files identical despite different names*

### Comparing `spyder-notebook-0.4.1/spyder_notebook/confpage.py` & `spyder-notebook-0.5.0/spyder_notebook/confpage.py`

 * *Files identical despite different names*

### Comparing `spyder-notebook-0.4.1/spyder_notebook/locale/de/LC_MESSAGES/spyder_notebook.mo` & `spyder-notebook-0.5.0/spyder_notebook/locale/pt_BR/LC_MESSAGES/spyder_notebook.mo`

 * *Files 21% similar despite different names*

#### msgunfmt {}

```diff
@@ -1,154 +1,153 @@
 msgid ""
 msgstr ""
 "Project-Id-Version: spyder-notebook\n"
-"POT-Creation-Date: 2021-01-16 12:42+0000\n"
-"PO-Revision-Date: 2021-01-16 15:56\n"
+"POT-Creation-Date: 2023-07-02 16:37+0100\n"
+"PO-Revision-Date: 2023-07-02 16:21\n"
 "Last-Translator: \n"
-"Language-Team: German\n"
+"Language-Team: Portuguese, Brazilian\n"
 "MIME-Version: 1.0\n"
 "Content-Type: text/plain; charset=UTF-8\n"
 "Content-Transfer-Encoding: 8bit\n"
 "Generated-By: pygettext.py 1.5\n"
 "Plural-Forms: nplurals=2; plural=(n != 1);\n"
 "X-Crowdin-Project: spyder-notebook\n"
 "X-Crowdin-Project-ID: 381803\n"
-"X-Crowdin-Language: de\n"
+"X-Crowdin-Language: pt-BR\n"
 "X-Crowdin-File: /master/spyder_notebook/locale/spyder_notebook.pot\n"
 "X-Crowdin-File-ID: 17\n"
-"Language: de_DE\n"
+"Language: pt_BR\n"
 
 msgid "<b>{0}</b> has been modified.<br>Do you want to save changes?"
-msgstr "<b>{0}</b> wurde geändert.<br>Möchten Sie die Änderungen speichern?"
+msgstr "<b>{0}</b> foi modificado.<br>Deseja salvar as alterações?"
 
 msgid "An error occurred while starting the kernel"
-msgstr "Beim Starten des Kernels ist ein Fehler aufgetreten"
+msgstr "Um erro ocorreu enquanto o kernel era inicializado"
 
 msgid "Clear this list"
-msgstr "Diese Liste leeren"
+msgstr "Limpar esta lista"
 
 msgid "Connecting to kernel..."
-msgstr "Verbindungsaufbau mit Kernel..."
+msgstr "Conectando ao kernel..."
 
 msgid "Error"
-msgstr "Fehler"
+msgstr "Erro"
 
 msgid "Error opening console"
-msgstr "Fehler beim Öffnen der Konsole"
+msgstr "Erro ao abrir o console"
 
 msgid "Error while reading {}<p>{}"
-msgstr "Fehler beim Lesen {}<p>{}"
+msgstr "Erro ao ler {}<p>{}"
 
 msgid "Error while writing {}<p>{}"
-msgstr "Fehler beim Schreiben {}<p>{}"
+msgstr "Erro ao escrever {}<p>{}"
 
 msgid "File Error"
-msgstr "Dateifehler"
+msgstr "Erro de Arquivo"
 
 msgid "Finished"
-msgstr "Fertig"
+msgstr "Finalizado"
+
+msgid "Interface"
+msgstr "Inteface"
 
 msgid "Jupyter notebooks"
-msgstr "Jupyter-Notebooks"
+msgstr "Notebooks do Jupyter"
 
 msgid "New notebook"
-msgstr "Neues Notebook"
+msgstr "Novo notebook"
 
 msgid "Notebook"
 msgstr "Notebook"
 
 msgid "Notebook dir:"
-msgstr "Notebook Verzeichnis:"
+msgstr "Diretório do Notebook:"
 
 msgid "Notebook server info"
-msgstr "Notebook Serverinformationen"
+msgstr "Informação do servidor Notebook"
 
 msgid "Notebook theme"
-msgstr "Notebook-Thema"
+msgstr "Tema do Notebook"
 
 msgid "Open a new notebook"
-msgstr "Neues Notebook öffnen"
+msgstr "Abrir um novo notebook"
 
 msgid "Open console"
-msgstr "Konsole öffnen"
+msgstr "Abrir console"
 
 msgid "Open notebook"
-msgstr "Notebook öffnen"
+msgstr "Abrir notebook"
 
 msgid "Open recent"
-msgstr "Letzte öffnen"
+msgstr "Abrir recente"
 
 msgid "Open..."
-msgstr "Öffnen..."
-
-msgid "Options"
-msgstr "Optionen"
+msgstr "Abrir..."
 
 msgid "Process ID:"
-msgstr "Prozesskennung:"
+msgstr "ID do processo:"
 
 msgid "Python interpreter:"
-msgstr "Python-Interpreter:"
+msgstr "Interpretador Python:"
 
 msgid "Refresh"
-msgstr "Aktualisieren"
+msgstr "Atualizar"
 
 msgid "Running"
-msgstr "Läuft"
+msgstr "Executando"
 
 msgid "Save as..."
-msgstr "Speichern unter..."
+msgstr "Salvar como..."
 
 msgid "Save changes"
-msgstr "Änderungen speichern"
+msgstr "Salvar alterações"
 
 msgid "Save notebook"
-msgstr "Notebook speichern"
+msgstr "Salvar notebook"
 
 msgid "Server error"
-msgstr "Serverfehler"
+msgstr "Erro no servidor"
 
 msgid "Server info..."
-msgstr "Serverinformationen..."
+msgstr "Informações do servidor..."
 
 msgid ""
 "Spyder could not get a list of sessions from the Jupyter Notebook server. "
 "Message: {}"
 msgstr ""
-"Spyder konnte keine Liste der Sitzungen vom Jupyter-Notebook-Server "
-"erhalten. Nachricht: {}"
+"O Spyder não conseguiu obter uma lista de sessões do servidor do Notebook "
+"Jupyter. Mensagem: {}"
 
 msgid ""
 "Spyder could not get a list of sessions from the Jupyter Notebook server. "
 "Status code: {}"
 msgstr ""
-"Spyder konnte keine Liste der Sitzungen vom Jupyter-Notebook-Server abrufen. "
-"Statuscode: {}"
+"O Spyder não conseguiu obter uma lista de sessões do servidor do Notebook "
+"Jupyter. Código de Status: {}"
 
 msgid "Starting up"
-msgstr "Inbetriebnahme"
+msgstr "Iniciando"
 
 msgid "State:"
-msgstr "Status:"
+msgstr "Estado:"
 
 msgid ""
 "The Jupyter Notebook server failed to shutdown the kernel associated with "
 "this notebook. If you want to shut it down, you'll have to close Spyder."
 msgstr ""
-"Der Jupyter-Notebook-Server konnte den mit diesem Notebook verbundenen "
-"Kernel nicht herunterfahren. Falls Sie ihn herunterfahren möchten, müssen "
-"Sie Spyder schließen."
+"O servidor do Jupyter Notebook falhou ao desligar o kernel associado a ele. "
+"Se você quiser desligá-lo terá que fechar o Spyder."
+
+msgid ""
+"The Spyder Notebook server failed to start or it is taking too much time to "
+"do it. Please select 'Server info' in the plugin's option menu to check for "
+"errors."
+msgstr ""
+"O servidor Notebook Spyder falhou ao iniciar ou está demorando muito para "
+"fazê-lo. Por favor, selecione ''Informações do servidor' no meu Opções para "
+"verificar se há erros."
 
 msgid "There is no kernel associated to this notebook."
-msgstr "Mit diesem Notebook ist kein Kernel verknüpft."
+msgstr "Não há kernel associado a este notebook."
 
 msgid "Timed out"
-msgstr "Zeit überschritten"
-
-msgid ""
-"You are working with Qt4 and in order to use this plugin you need to have "
-"Qt5.<br><br>Please update your Qt and/or PyQt packages to meet this "
-"requirement."
-msgstr ""
-"Sie arbeiten mit Qt4 und um dieses Plugin verwenden zu können, benötigen Sie "
-"Qt5. <br> <br> Bitte aktualisieren Sie Ihre Qt- und / oder PyQt Pakete, um "
-"diese Anforderung zu erfüllen."
+msgstr "Tempo esgotado"
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/locale/es/LC_MESSAGES/spyder_notebook.mo` & `spyder-notebook-0.5.0/spyder_notebook/locale/es/LC_MESSAGES/spyder_notebook.mo`

 * *Files 20% similar despite different names*

#### msgunfmt {}

```diff
@@ -1,12 +1,12 @@
 msgid ""
 msgstr ""
 "Project-Id-Version: spyder-notebook\n"
-"POT-Creation-Date: 2021-01-16 12:42+0000\n"
-"PO-Revision-Date: 2021-01-16 13:16\n"
+"POT-Creation-Date: 2023-07-02 16:37+0100\n"
+"PO-Revision-Date: 2023-07-02 16:21\n"
 "Last-Translator: \n"
 "Language-Team: Spanish\n"
 "MIME-Version: 1.0\n"
 "Content-Type: text/plain; charset=UTF-8\n"
 "Content-Transfer-Encoding: 8bit\n"
 "Generated-By: pygettext.py 1.5\n"
 "Plural-Forms: nplurals=2; plural=(n != 1);\n"
@@ -73,17 +73,14 @@
 
 msgid "Open recent"
 msgstr "Abrir reciente"
 
 msgid "Open..."
 msgstr "Abrir..."
 
-msgid "Options"
-msgstr "Opciones"
-
 msgid "Process ID:"
 msgstr "ID de proceso:"
 
 msgid "Refresh"
 msgstr "Actualizar"
 
 msgid "Running"
@@ -125,16 +122,7 @@
 "notebook. Si desea apagarlo, tendrá que cerrar Spyder."
 
 msgid "There is no kernel associated to this notebook."
 msgstr "No hay ningún núcleo asociado a este notebook."
 
 msgid "Timed out"
 msgstr "Tiempo de espera agotado"
-
-msgid ""
-"You are working with Qt4 and in order to use this plugin you need to have "
-"Qt5.<br><br>Please update your Qt and/or PyQt packages to meet this "
-"requirement."
-msgstr ""
-"Estás trabajando con Qt4 y para poder usar este plugin necesitas tener Qt5."
-"<br><br>Por favor, actualice sus paquetes Qt y/o PyQt para cumplir con este "
-"requisito."
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/locale/fr/LC_MESSAGES/spyder_notebook.mo` & `spyder-notebook-0.5.0/spyder_notebook/locale/zh_CN/LC_MESSAGES/spyder_notebook.mo`

 * *Format-specific differences are supported for Gettext message catalogues but no file-specific differences were detected; falling back to a binary diff. file(1) reports: GNU message catalog (little endian), revision 0.0, 1 message, Project-Id-Version: spyder-notebook*

 * *Files 12% similar despite different names*

```diff
@@ -1,35 +1,36 @@
 00000000: de12 0495 0000 0000 0100 0000 1c00 0000  ................
 00000010: 2400 0000 0000 0000 0000 0000 0000 0000  $...............
-00000020: 2c00 0000 fb01 0000 2d00 0000 0050 726f  ,.......-....Pro
+00000020: 2c00 0000 0402 0000 2d00 0000 0050 726f  ,.......-....Pro
 00000030: 6a65 6374 2d49 642d 5665 7273 696f 6e3a  ject-Id-Version:
 00000040: 2073 7079 6465 722d 6e6f 7465 626f 6f6b   spyder-notebook
 00000050: 0a50 4f54 2d43 7265 6174 696f 6e2d 4461  .POT-Creation-Da
-00000060: 7465 3a20 3230 3231 2d30 312d 3136 2031  te: 2021-01-16 1
-00000070: 323a 3432 2b30 3030 300a 504f 2d52 6576  2:42+0000.PO-Rev
-00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3231  ision-Date: 2021
-00000090: 2d30 312d 3136 2031 333a 3136 0a4c 6173  -01-16 13:16.Las
+00000060: 7465 3a20 3230 3233 2d30 372d 3032 2031  te: 2023-07-02 1
+00000070: 363a 3337 2b30 3130 300a 504f 2d52 6576  6:37+0100.PO-Rev
+00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3233  ision-Date: 2023
+00000090: 2d30 372d 3032 2031 363a 3231 0a4c 6173  -07-02 16:21.Las
 000000a0: 742d 5472 616e 736c 6174 6f72 3a20 0a4c  t-Translator: .L
-000000b0: 616e 6775 6167 652d 5465 616d 3a20 4672  anguage-Team: Fr
-000000c0: 656e 6368 0a4d 494d 452d 5665 7273 696f  ench.MIME-Versio
-000000d0: 6e3a 2031 2e30 0a43 6f6e 7465 6e74 2d54  n: 1.0.Content-T
-000000e0: 7970 653a 2074 6578 742f 706c 6169 6e3b  ype: text/plain;
-000000f0: 2063 6861 7273 6574 3d55 5446 2d38 0a43   charset=UTF-8.C
-00000100: 6f6e 7465 6e74 2d54 7261 6e73 6665 722d  ontent-Transfer-
-00000110: 456e 636f 6469 6e67 3a20 3862 6974 0a47  Encoding: 8bit.G
-00000120: 656e 6572 6174 6564 2d42 793a 2070 7967  enerated-By: pyg
-00000130: 6574 7465 7874 2e70 7920 312e 350a 506c  ettext.py 1.5.Pl
-00000140: 7572 616c 2d46 6f72 6d73 3a20 6e70 6c75  ural-Forms: nplu
-00000150: 7261 6c73 3d32 3b20 706c 7572 616c 3d28  rals=2; plural=(
-00000160: 6e20 3e20 3129 3b0a 582d 4372 6f77 6469  n > 1);.X-Crowdi
-00000170: 6e2d 5072 6f6a 6563 743a 2073 7079 6465  n-Project: spyde
-00000180: 722d 6e6f 7465 626f 6f6b 0a58 2d43 726f  r-notebook.X-Cro
-00000190: 7764 696e 2d50 726f 6a65 6374 2d49 443a  wdin-Project-ID:
-000001a0: 2033 3831 3830 330a 582d 4372 6f77 6469   381803.X-Crowdi
-000001b0: 6e2d 4c61 6e67 7561 6765 3a20 6672 0a58  n-Language: fr.X
-000001c0: 2d43 726f 7764 696e 2d46 696c 653a 202f  -Crowdin-File: /
-000001d0: 6d61 7374 6572 2f73 7079 6465 725f 6e6f  master/spyder_no
-000001e0: 7465 626f 6f6b 2f6c 6f63 616c 652f 7370  tebook/locale/sp
-000001f0: 7964 6572 5f6e 6f74 6562 6f6f 6b2e 706f  yder_notebook.po
-00000200: 740a 582d 4372 6f77 6469 6e2d 4669 6c65  t.X-Crowdin-File
-00000210: 2d49 443a 2031 370a 4c61 6e67 7561 6765  -ID: 17.Language
-00000220: 3a20 6672 5f46 520a 00                   : fr_FR..
+000000b0: 616e 6775 6167 652d 5465 616d 3a20 4368  anguage-Team: Ch
+000000c0: 696e 6573 6520 5369 6d70 6c69 6669 6564  inese Simplified
+000000d0: 0a4d 494d 452d 5665 7273 696f 6e3a 2031  .MIME-Version: 1
+000000e0: 2e30 0a43 6f6e 7465 6e74 2d54 7970 653a  .0.Content-Type:
+000000f0: 2074 6578 742f 706c 6169 6e3b 2063 6861   text/plain; cha
+00000100: 7273 6574 3d55 5446 2d38 0a43 6f6e 7465  rset=UTF-8.Conte
+00000110: 6e74 2d54 7261 6e73 6665 722d 456e 636f  nt-Transfer-Enco
+00000120: 6469 6e67 3a20 3862 6974 0a47 656e 6572  ding: 8bit.Gener
+00000130: 6174 6564 2d42 793a 2070 7967 6574 7465  ated-By: pygette
+00000140: 7874 2e70 7920 312e 350a 506c 7572 616c  xt.py 1.5.Plural
+00000150: 2d46 6f72 6d73 3a20 6e70 6c75 7261 6c73  -Forms: nplurals
+00000160: 3d31 3b20 706c 7572 616c 3d30 3b0a 582d  =1; plural=0;.X-
+00000170: 4372 6f77 6469 6e2d 5072 6f6a 6563 743a  Crowdin-Project:
+00000180: 2073 7079 6465 722d 6e6f 7465 626f 6f6b   spyder-notebook
+00000190: 0a58 2d43 726f 7764 696e 2d50 726f 6a65  .X-Crowdin-Proje
+000001a0: 6374 2d49 443a 2033 3831 3830 330a 582d  ct-ID: 381803.X-
+000001b0: 4372 6f77 6469 6e2d 4c61 6e67 7561 6765  Crowdin-Language
+000001c0: 3a20 7a68 2d43 4e0a 582d 4372 6f77 6469  : zh-CN.X-Crowdi
+000001d0: 6e2d 4669 6c65 3a20 2f6d 6173 7465 722f  n-File: /master/
+000001e0: 7370 7964 6572 5f6e 6f74 6562 6f6f 6b2f  spyder_notebook/
+000001f0: 6c6f 6361 6c65 2f73 7079 6465 725f 6e6f  locale/spyder_no
+00000200: 7465 626f 6f6b 2e70 6f74 0a58 2d43 726f  tebook.pot.X-Cro
+00000210: 7764 696e 2d46 696c 652d 4944 3a20 3137  wdin-File-ID: 17
+00000220: 0a4c 616e 6775 6167 653a 207a 685f 434e  .Language: zh_CN
+00000230: 0a00                                     ..
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/locale/hr/LC_MESSAGES/spyder_notebook.mo` & `spyder-notebook-0.5.0/spyder_notebook/locale/hr/LC_MESSAGES/spyder_notebook.mo`

 * *Format-specific differences are supported for Gettext message catalogues but no file-specific differences were detected; falling back to a binary diff. file(1) reports: GNU message catalog (little endian), revision 0.0, 1 message, Project-Id-Version: spyder-notebook*

 * *Files 8% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 00000000: de12 0495 0000 0000 0100 0000 1c00 0000  ................
 00000010: 2400 0000 0000 0000 0000 0000 0000 0000  $...............
 00000020: 2c00 0000 4802 0000 2d00 0000 0050 726f  ,...H...-....Pro
 00000030: 6a65 6374 2d49 642d 5665 7273 696f 6e3a  ject-Id-Version:
 00000040: 2073 7079 6465 722d 6e6f 7465 626f 6f6b   spyder-notebook
 00000050: 0a50 4f54 2d43 7265 6174 696f 6e2d 4461  .POT-Creation-Da
-00000060: 7465 3a20 3230 3231 2d30 312d 3136 2031  te: 2021-01-16 1
-00000070: 323a 3432 2b30 3030 300a 504f 2d52 6576  2:42+0000.PO-Rev
-00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3231  ision-Date: 2021
-00000090: 2d30 312d 3136 2031 333a 3136 0a4c 6173  -01-16 13:16.Las
+00000060: 7465 3a20 3230 3233 2d30 372d 3032 2031  te: 2023-07-02 1
+00000070: 363a 3337 2b30 3130 300a 504f 2d52 6576  6:37+0100.PO-Rev
+00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3233  ision-Date: 2023
+00000090: 2d30 372d 3032 2031 363a 3231 0a4c 6173  -07-02 16:21.Las
 000000a0: 742d 5472 616e 736c 6174 6f72 3a20 0a4c  t-Translator: .L
 000000b0: 616e 6775 6167 652d 5465 616d 3a20 4372  anguage-Team: Cr
 000000c0: 6f61 7469 616e 0a4d 494d 452d 5665 7273  oatian.MIME-Vers
 000000d0: 696f 6e3a 2031 2e30 0a43 6f6e 7465 6e74  ion: 1.0.Content
 000000e0: 2d54 7970 653a 2074 6578 742f 706c 6169  -Type: text/plai
 000000f0: 6e3b 2063 6861 7273 6574 3d55 5446 2d38  n; charset=UTF-8
 00000100: 0a43 6f6e 7465 6e74 2d54 7261 6e73 6665  .Content-Transfe
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/locale/hu/LC_MESSAGES/spyder_notebook.mo` & `spyder-notebook-0.5.0/spyder_notebook/locale/hu/LC_MESSAGES/spyder_notebook.mo`

 * *Format-specific differences are supported for Gettext message catalogues but no file-specific differences were detected; falling back to a binary diff. file(1) reports: GNU message catalog (little endian), revision 0.0, 1 message, Project-Id-Version: spyder-notebook*

 * *Files 9% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 00000000: de12 0495 0000 0000 0100 0000 1c00 0000  ................
 00000010: 2400 0000 0000 0000 0000 0000 0000 0000  $...............
 00000020: 2c00 0000 ff01 0000 2d00 0000 0050 726f  ,.......-....Pro
 00000030: 6a65 6374 2d49 642d 5665 7273 696f 6e3a  ject-Id-Version:
 00000040: 2073 7079 6465 722d 6e6f 7465 626f 6f6b   spyder-notebook
 00000050: 0a50 4f54 2d43 7265 6174 696f 6e2d 4461  .POT-Creation-Da
-00000060: 7465 3a20 3230 3231 2d30 312d 3136 2031  te: 2021-01-16 1
-00000070: 323a 3432 2b30 3030 300a 504f 2d52 6576  2:42+0000.PO-Rev
-00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3231  ision-Date: 2021
-00000090: 2d30 312d 3136 2031 333a 3136 0a4c 6173  -01-16 13:16.Las
+00000060: 7465 3a20 3230 3233 2d30 372d 3032 2031  te: 2023-07-02 1
+00000070: 363a 3337 2b30 3130 300a 504f 2d52 6576  6:37+0100.PO-Rev
+00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3233  ision-Date: 2023
+00000090: 2d30 372d 3032 2031 363a 3231 0a4c 6173  -07-02 16:21.Las
 000000a0: 742d 5472 616e 736c 6174 6f72 3a20 0a4c  t-Translator: .L
 000000b0: 616e 6775 6167 652d 5465 616d 3a20 4875  anguage-Team: Hu
 000000c0: 6e67 6172 6961 6e0a 4d49 4d45 2d56 6572  ngarian.MIME-Ver
 000000d0: 7369 6f6e 3a20 312e 300a 436f 6e74 656e  sion: 1.0.Conten
 000000e0: 742d 5479 7065 3a20 7465 7874 2f70 6c61  t-Type: text/pla
 000000f0: 696e 3b20 6368 6172 7365 743d 5554 462d  in; charset=UTF-
 00000100: 380a 436f 6e74 656e 742d 5472 616e 7366  8.Content-Transf
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/locale/pl/LC_MESSAGES/spyder_notebook.mo` & `spyder-notebook-0.5.0/spyder_notebook/locale/ru/LC_MESSAGES/spyder_notebook.mo`

 * *Format-specific differences are supported for Gettext message catalogues but no file-specific differences were detected; falling back to a binary diff. file(1) reports: GNU message catalog (little endian), revision 0.0, 1 message, Project-Id-Version: spyder-notebook*

 * *Files 26% similar despite different names*

```diff
@@ -1,44 +1,45 @@
 00000000: de12 0495 0000 0000 0100 0000 1c00 0000  ................
 00000010: 2400 0000 0000 0000 0000 0000 0000 0000  $...............
-00000020: 2c00 0000 8e02 0000 2d00 0000 0050 726f  ,.......-....Pro
+00000020: 2c00 0000 a202 0000 2d00 0000 0050 726f  ,.......-....Pro
 00000030: 6a65 6374 2d49 642d 5665 7273 696f 6e3a  ject-Id-Version:
 00000040: 2073 7079 6465 722d 6e6f 7465 626f 6f6b   spyder-notebook
 00000050: 0a50 4f54 2d43 7265 6174 696f 6e2d 4461  .POT-Creation-Da
-00000060: 7465 3a20 3230 3231 2d30 312d 3136 2031  te: 2021-01-16 1
-00000070: 323a 3432 2b30 3030 300a 504f 2d52 6576  2:42+0000.PO-Rev
-00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3231  ision-Date: 2021
-00000090: 2d30 312d 3136 2031 333a 3136 0a4c 6173  -01-16 13:16.Las
+00000060: 7465 3a20 3230 3233 2d30 372d 3032 2031  te: 2023-07-02 1
+00000070: 363a 3337 2b30 3130 300a 504f 2d52 6576  6:37+0100.PO-Rev
+00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3233  ision-Date: 2023
+00000090: 2d30 372d 3032 2031 363a 3231 0a4c 6173  -07-02 16:21.Las
 000000a0: 742d 5472 616e 736c 6174 6f72 3a20 0a4c  t-Translator: .L
-000000b0: 616e 6775 6167 652d 5465 616d 3a20 506f  anguage-Team: Po
-000000c0: 6c69 7368 0a4d 494d 452d 5665 7273 696f  lish.MIME-Versio
-000000d0: 6e3a 2031 2e30 0a43 6f6e 7465 6e74 2d54  n: 1.0.Content-T
-000000e0: 7970 653a 2074 6578 742f 706c 6169 6e3b  ype: text/plain;
-000000f0: 2063 6861 7273 6574 3d55 5446 2d38 0a43   charset=UTF-8.C
-00000100: 6f6e 7465 6e74 2d54 7261 6e73 6665 722d  ontent-Transfer-
-00000110: 456e 636f 6469 6e67 3a20 3862 6974 0a47  Encoding: 8bit.G
-00000120: 656e 6572 6174 6564 2d42 793a 2070 7967  enerated-By: pyg
-00000130: 6574 7465 7874 2e70 7920 312e 350a 506c  ettext.py 1.5.Pl
-00000140: 7572 616c 2d46 6f72 6d73 3a20 6e70 6c75  ural-Forms: nplu
-00000150: 7261 6c73 3d34 3b20 706c 7572 616c 3d28  rals=4; plural=(
-00000160: 6e3d 3d31 203f 2030 203a 2028 6e25 3130  n==1 ? 0 : (n%10
-00000170: 3e3d 3220 2626 206e 2531 303c 3d34 2920  >=2 && n%10<=4) 
-00000180: 2626 2028 6e25 3130 303c 3132 207c 7c20  && (n%100<12 || 
-00000190: 6e25 3130 303e 3134 2920 3f20 3120 3a20  n%100>14) ? 1 : 
-000001a0: 6e21 3d31 2026 2620 286e 2531 303e 3d30  n!=1 && (n%10>=0
-000001b0: 2026 2620 6e25 3130 3c3d 3129 207c 7c20   && n%10<=1) || 
-000001c0: 286e 2531 303e 3d35 2026 2620 6e25 3130  (n%10>=5 && n%10
-000001d0: 3c3d 3929 207c 7c20 286e 2531 3030 3e3d  <=9) || (n%100>=
-000001e0: 3132 2026 2620 6e25 3130 303c 3d31 3429  12 && n%100<=14)
-000001f0: 203f 2032 203a 2033 293b 0a58 2d43 726f   ? 2 : 3);.X-Cro
-00000200: 7764 696e 2d50 726f 6a65 6374 3a20 7370  wdin-Project: sp
-00000210: 7964 6572 2d6e 6f74 6562 6f6f 6b0a 582d  yder-notebook.X-
-00000220: 4372 6f77 6469 6e2d 5072 6f6a 6563 742d  Crowdin-Project-
-00000230: 4944 3a20 3338 3138 3033 0a58 2d43 726f  ID: 381803.X-Cro
-00000240: 7764 696e 2d4c 616e 6775 6167 653a 2070  wdin-Language: p
-00000250: 6c0a 582d 4372 6f77 6469 6e2d 4669 6c65  l.X-Crowdin-File
-00000260: 3a20 2f6d 6173 7465 722f 7370 7964 6572  : /master/spyder
-00000270: 5f6e 6f74 6562 6f6f 6b2f 6c6f 6361 6c65  _notebook/locale
-00000280: 2f73 7079 6465 725f 6e6f 7465 626f 6f6b  /spyder_notebook
-00000290: 2e70 6f74 0a58 2d43 726f 7764 696e 2d46  .pot.X-Crowdin-F
-000002a0: 696c 652d 4944 3a20 3137 0a4c 616e 6775  ile-ID: 17.Langu
-000002b0: 6167 653a 2070 6c5f 504c 0a00            age: pl_PL..
+000000b0: 616e 6775 6167 652d 5465 616d 3a20 5275  anguage-Team: Ru
+000000c0: 7373 6961 6e0a 4d49 4d45 2d56 6572 7369  ssian.MIME-Versi
+000000d0: 6f6e 3a20 312e 300a 436f 6e74 656e 742d  on: 1.0.Content-
+000000e0: 5479 7065 3a20 7465 7874 2f70 6c61 696e  Type: text/plain
+000000f0: 3b20 6368 6172 7365 743d 5554 462d 380a  ; charset=UTF-8.
+00000100: 436f 6e74 656e 742d 5472 616e 7366 6572  Content-Transfer
+00000110: 2d45 6e63 6f64 696e 673a 2038 6269 740a  -Encoding: 8bit.
+00000120: 4765 6e65 7261 7465 642d 4279 3a20 7079  Generated-By: py
+00000130: 6765 7474 6578 742e 7079 2031 2e35 0a50  gettext.py 1.5.P
+00000140: 6c75 7261 6c2d 466f 726d 733a 206e 706c  lural-Forms: npl
+00000150: 7572 616c 733d 343b 2070 6c75 7261 6c3d  urals=4; plural=
+00000160: 2828 6e25 3130 3d3d 3120 2626 206e 2531  ((n%10==1 && n%1
+00000170: 3030 213d 3131 2920 3f20 3020 3a20 2828  00!=11) ? 0 : ((
+00000180: 6e25 3130 203e 3d20 3220 2626 206e 2531  n%10 >= 2 && n%1
+00000190: 3020 3c3d 3420 2626 2028 6e25 3130 3020  0 <=4 && (n%100 
+000001a0: 3c20 3132 207c 7c20 6e25 3130 3020 3e20  < 12 || n%100 > 
+000001b0: 3134 2929 203f 2031 203a 2028 286e 2531  14)) ? 1 : ((n%1
+000001c0: 3020 3d3d 2030 207c 7c20 286e 2531 3020  0 == 0 || (n%10 
+000001d0: 3e3d 2035 2026 2620 6e25 3130 203c 3d39  >= 5 && n%10 <=9
+000001e0: 2929 207c 7c20 286e 2531 3030 203e 3d20  )) || (n%100 >= 
+000001f0: 3131 2026 2620 6e25 3130 3020 3c3d 2031  11 && n%100 <= 1
+00000200: 3429 2920 3f20 3220 3a20 3329 293b 0a58  4)) ? 2 : 3));.X
+00000210: 2d43 726f 7764 696e 2d50 726f 6a65 6374  -Crowdin-Project
+00000220: 3a20 7370 7964 6572 2d6e 6f74 6562 6f6f  : spyder-noteboo
+00000230: 6b0a 582d 4372 6f77 6469 6e2d 5072 6f6a  k.X-Crowdin-Proj
+00000240: 6563 742d 4944 3a20 3338 3138 3033 0a58  ect-ID: 381803.X
+00000250: 2d43 726f 7764 696e 2d4c 616e 6775 6167  -Crowdin-Languag
+00000260: 653a 2072 750a 582d 4372 6f77 6469 6e2d  e: ru.X-Crowdin-
+00000270: 4669 6c65 3a20 2f6d 6173 7465 722f 7370  File: /master/sp
+00000280: 7964 6572 5f6e 6f74 6562 6f6f 6b2f 6c6f  yder_notebook/lo
+00000290: 6361 6c65 2f73 7079 6465 725f 6e6f 7465  cale/spyder_note
+000002a0: 626f 6f6b 2e70 6f74 0a58 2d43 726f 7764  book.pot.X-Crowd
+000002b0: 696e 2d46 696c 652d 4944 3a20 3137 0a4c  in-File-ID: 17.L
+000002c0: 616e 6775 6167 653a 2072 755f 5255 0a00  anguage: ru_RU..
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/locale/ru/LC_MESSAGES/spyder_notebook.mo` & `spyder-notebook-0.5.0/spyder_notebook/locale/ja/LC_MESSAGES/spyder_notebook.mo`

 * *Format-specific differences are supported for Gettext message catalogues but no file-specific differences were detected; falling back to a binary diff. file(1) reports: GNU message catalog (little endian), revision 0.0, 1 message, Project-Id-Version: spyder-notebook*

 * *Files 21% similar despite different names*

```diff
@@ -1,45 +1,35 @@
 00000000: de12 0495 0000 0000 0100 0000 1c00 0000  ................
 00000010: 2400 0000 0000 0000 0000 0000 0000 0000  $...............
-00000020: 2c00 0000 a202 0000 2d00 0000 0050 726f  ,.......-....Pro
+00000020: 2c00 0000 f701 0000 2d00 0000 0050 726f  ,.......-....Pro
 00000030: 6a65 6374 2d49 642d 5665 7273 696f 6e3a  ject-Id-Version:
 00000040: 2073 7079 6465 722d 6e6f 7465 626f 6f6b   spyder-notebook
 00000050: 0a50 4f54 2d43 7265 6174 696f 6e2d 4461  .POT-Creation-Da
-00000060: 7465 3a20 3230 3231 2d30 312d 3136 2031  te: 2021-01-16 1
-00000070: 323a 3432 2b30 3030 300a 504f 2d52 6576  2:42+0000.PO-Rev
-00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3231  ision-Date: 2021
-00000090: 2d30 312d 3136 2031 333a 3136 0a4c 6173  -01-16 13:16.Las
+00000060: 7465 3a20 3230 3233 2d30 372d 3032 2031  te: 2023-07-02 1
+00000070: 363a 3337 2b30 3130 300a 504f 2d52 6576  6:37+0100.PO-Rev
+00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3233  ision-Date: 2023
+00000090: 2d30 372d 3032 2031 363a 3231 0a4c 6173  -07-02 16:21.Las
 000000a0: 742d 5472 616e 736c 6174 6f72 3a20 0a4c  t-Translator: .L
-000000b0: 616e 6775 6167 652d 5465 616d 3a20 5275  anguage-Team: Ru
-000000c0: 7373 6961 6e0a 4d49 4d45 2d56 6572 7369  ssian.MIME-Versi
-000000d0: 6f6e 3a20 312e 300a 436f 6e74 656e 742d  on: 1.0.Content-
-000000e0: 5479 7065 3a20 7465 7874 2f70 6c61 696e  Type: text/plain
-000000f0: 3b20 6368 6172 7365 743d 5554 462d 380a  ; charset=UTF-8.
-00000100: 436f 6e74 656e 742d 5472 616e 7366 6572  Content-Transfer
-00000110: 2d45 6e63 6f64 696e 673a 2038 6269 740a  -Encoding: 8bit.
-00000120: 4765 6e65 7261 7465 642d 4279 3a20 7079  Generated-By: py
-00000130: 6765 7474 6578 742e 7079 2031 2e35 0a50  gettext.py 1.5.P
-00000140: 6c75 7261 6c2d 466f 726d 733a 206e 706c  lural-Forms: npl
-00000150: 7572 616c 733d 343b 2070 6c75 7261 6c3d  urals=4; plural=
-00000160: 2828 6e25 3130 3d3d 3120 2626 206e 2531  ((n%10==1 && n%1
-00000170: 3030 213d 3131 2920 3f20 3020 3a20 2828  00!=11) ? 0 : ((
-00000180: 6e25 3130 203e 3d20 3220 2626 206e 2531  n%10 >= 2 && n%1
-00000190: 3020 3c3d 3420 2626 2028 6e25 3130 3020  0 <=4 && (n%100 
-000001a0: 3c20 3132 207c 7c20 6e25 3130 3020 3e20  < 12 || n%100 > 
-000001b0: 3134 2929 203f 2031 203a 2028 286e 2531  14)) ? 1 : ((n%1
-000001c0: 3020 3d3d 2030 207c 7c20 286e 2531 3020  0 == 0 || (n%10 
-000001d0: 3e3d 2035 2026 2620 6e25 3130 203c 3d39  >= 5 && n%10 <=9
-000001e0: 2929 207c 7c20 286e 2531 3030 203e 3d20  )) || (n%100 >= 
-000001f0: 3131 2026 2620 6e25 3130 3020 3c3d 2031  11 && n%100 <= 1
-00000200: 3429 2920 3f20 3220 3a20 3329 293b 0a58  4)) ? 2 : 3));.X
-00000210: 2d43 726f 7764 696e 2d50 726f 6a65 6374  -Crowdin-Project
-00000220: 3a20 7370 7964 6572 2d6e 6f74 6562 6f6f  : spyder-noteboo
-00000230: 6b0a 582d 4372 6f77 6469 6e2d 5072 6f6a  k.X-Crowdin-Proj
-00000240: 6563 742d 4944 3a20 3338 3138 3033 0a58  ect-ID: 381803.X
-00000250: 2d43 726f 7764 696e 2d4c 616e 6775 6167  -Crowdin-Languag
-00000260: 653a 2072 750a 582d 4372 6f77 6469 6e2d  e: ru.X-Crowdin-
-00000270: 4669 6c65 3a20 2f6d 6173 7465 722f 7370  File: /master/sp
-00000280: 7964 6572 5f6e 6f74 6562 6f6f 6b2f 6c6f  yder_notebook/lo
-00000290: 6361 6c65 2f73 7079 6465 725f 6e6f 7465  cale/spyder_note
-000002a0: 626f 6f6b 2e70 6f74 0a58 2d43 726f 7764  book.pot.X-Crowd
-000002b0: 696e 2d46 696c 652d 4944 3a20 3137 0a4c  in-File-ID: 17.L
-000002c0: 616e 6775 6167 653a 2072 755f 5255 0a00  anguage: ru_RU..
+000000b0: 616e 6775 6167 652d 5465 616d 3a20 4a61  anguage-Team: Ja
+000000c0: 7061 6e65 7365 0a4d 494d 452d 5665 7273  panese.MIME-Vers
+000000d0: 696f 6e3a 2031 2e30 0a43 6f6e 7465 6e74  ion: 1.0.Content
+000000e0: 2d54 7970 653a 2074 6578 742f 706c 6169  -Type: text/plai
+000000f0: 6e3b 2063 6861 7273 6574 3d55 5446 2d38  n; charset=UTF-8
+00000100: 0a43 6f6e 7465 6e74 2d54 7261 6e73 6665  .Content-Transfe
+00000110: 722d 456e 636f 6469 6e67 3a20 3862 6974  r-Encoding: 8bit
+00000120: 0a47 656e 6572 6174 6564 2d42 793a 2070  .Generated-By: p
+00000130: 7967 6574 7465 7874 2e70 7920 312e 350a  ygettext.py 1.5.
+00000140: 506c 7572 616c 2d46 6f72 6d73 3a20 6e70  Plural-Forms: np
+00000150: 6c75 7261 6c73 3d31 3b20 706c 7572 616c  lurals=1; plural
+00000160: 3d30 3b0a 582d 4372 6f77 6469 6e2d 5072  =0;.X-Crowdin-Pr
+00000170: 6f6a 6563 743a 2073 7079 6465 722d 6e6f  oject: spyder-no
+00000180: 7465 626f 6f6b 0a58 2d43 726f 7764 696e  tebook.X-Crowdin
+00000190: 2d50 726f 6a65 6374 2d49 443a 2033 3831  -Project-ID: 381
+000001a0: 3830 330a 582d 4372 6f77 6469 6e2d 4c61  803.X-Crowdin-La
+000001b0: 6e67 7561 6765 3a20 6a61 0a58 2d43 726f  nguage: ja.X-Cro
+000001c0: 7764 696e 2d46 696c 653a 202f 6d61 7374  wdin-File: /mast
+000001d0: 6572 2f73 7079 6465 725f 6e6f 7465 626f  er/spyder_notebo
+000001e0: 6f6b 2f6c 6f63 616c 652f 7370 7964 6572  ok/locale/spyder
+000001f0: 5f6e 6f74 6562 6f6f 6b2e 706f 740a 582d  _notebook.pot.X-
+00000200: 4372 6f77 6469 6e2d 4669 6c65 2d49 443a  Crowdin-File-ID:
+00000210: 2031 370a 4c61 6e67 7561 6765 3a20 6a61   17.Language: ja
+00000220: 5f4a 500a 00                             _JP..
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/locale/zh_CN/LC_MESSAGES/spyder_notebook.mo` & `spyder-notebook-0.5.0/spyder_notebook/locale/pl/LC_MESSAGES/spyder_notebook.mo`

 * *Format-specific differences are supported for Gettext message catalogues but no file-specific differences were detected; falling back to a binary diff. file(1) reports: GNU message catalog (little endian), revision 0.0, 1 message, Project-Id-Version: spyder-notebook*

 * *Files 26% similar despite different names*

```diff
@@ -1,36 +1,44 @@
 00000000: de12 0495 0000 0000 0100 0000 1c00 0000  ................
 00000010: 2400 0000 0000 0000 0000 0000 0000 0000  $...............
-00000020: 2c00 0000 0402 0000 2d00 0000 0050 726f  ,.......-....Pro
+00000020: 2c00 0000 8e02 0000 2d00 0000 0050 726f  ,.......-....Pro
 00000030: 6a65 6374 2d49 642d 5665 7273 696f 6e3a  ject-Id-Version:
 00000040: 2073 7079 6465 722d 6e6f 7465 626f 6f6b   spyder-notebook
 00000050: 0a50 4f54 2d43 7265 6174 696f 6e2d 4461  .POT-Creation-Da
-00000060: 7465 3a20 3230 3231 2d30 312d 3136 2031  te: 2021-01-16 1
-00000070: 323a 3432 2b30 3030 300a 504f 2d52 6576  2:42+0000.PO-Rev
-00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3231  ision-Date: 2021
-00000090: 2d30 312d 3136 2031 333a 3136 0a4c 6173  -01-16 13:16.Las
+00000060: 7465 3a20 3230 3233 2d30 372d 3032 2031  te: 2023-07-02 1
+00000070: 363a 3337 2b30 3130 300a 504f 2d52 6576  6:37+0100.PO-Rev
+00000080: 6973 696f 6e2d 4461 7465 3a20 3230 3233  ision-Date: 2023
+00000090: 2d30 372d 3032 2031 363a 3231 0a4c 6173  -07-02 16:21.Las
 000000a0: 742d 5472 616e 736c 6174 6f72 3a20 0a4c  t-Translator: .L
-000000b0: 616e 6775 6167 652d 5465 616d 3a20 4368  anguage-Team: Ch
-000000c0: 696e 6573 6520 5369 6d70 6c69 6669 6564  inese Simplified
-000000d0: 0a4d 494d 452d 5665 7273 696f 6e3a 2031  .MIME-Version: 1
-000000e0: 2e30 0a43 6f6e 7465 6e74 2d54 7970 653a  .0.Content-Type:
-000000f0: 2074 6578 742f 706c 6169 6e3b 2063 6861   text/plain; cha
-00000100: 7273 6574 3d55 5446 2d38 0a43 6f6e 7465  rset=UTF-8.Conte
-00000110: 6e74 2d54 7261 6e73 6665 722d 456e 636f  nt-Transfer-Enco
-00000120: 6469 6e67 3a20 3862 6974 0a47 656e 6572  ding: 8bit.Gener
-00000130: 6174 6564 2d42 793a 2070 7967 6574 7465  ated-By: pygette
-00000140: 7874 2e70 7920 312e 350a 506c 7572 616c  xt.py 1.5.Plural
-00000150: 2d46 6f72 6d73 3a20 6e70 6c75 7261 6c73  -Forms: nplurals
-00000160: 3d31 3b20 706c 7572 616c 3d30 3b0a 582d  =1; plural=0;.X-
-00000170: 4372 6f77 6469 6e2d 5072 6f6a 6563 743a  Crowdin-Project:
-00000180: 2073 7079 6465 722d 6e6f 7465 626f 6f6b   spyder-notebook
-00000190: 0a58 2d43 726f 7764 696e 2d50 726f 6a65  .X-Crowdin-Proje
-000001a0: 6374 2d49 443a 2033 3831 3830 330a 582d  ct-ID: 381803.X-
-000001b0: 4372 6f77 6469 6e2d 4c61 6e67 7561 6765  Crowdin-Language
-000001c0: 3a20 7a68 2d43 4e0a 582d 4372 6f77 6469  : zh-CN.X-Crowdi
-000001d0: 6e2d 4669 6c65 3a20 2f6d 6173 7465 722f  n-File: /master/
-000001e0: 7370 7964 6572 5f6e 6f74 6562 6f6f 6b2f  spyder_notebook/
-000001f0: 6c6f 6361 6c65 2f73 7079 6465 725f 6e6f  locale/spyder_no
-00000200: 7465 626f 6f6b 2e70 6f74 0a58 2d43 726f  tebook.pot.X-Cro
-00000210: 7764 696e 2d46 696c 652d 4944 3a20 3137  wdin-File-ID: 17
-00000220: 0a4c 616e 6775 6167 653a 207a 685f 434e  .Language: zh_CN
-00000230: 0a00                                     ..
+000000b0: 616e 6775 6167 652d 5465 616d 3a20 506f  anguage-Team: Po
+000000c0: 6c69 7368 0a4d 494d 452d 5665 7273 696f  lish.MIME-Versio
+000000d0: 6e3a 2031 2e30 0a43 6f6e 7465 6e74 2d54  n: 1.0.Content-T
+000000e0: 7970 653a 2074 6578 742f 706c 6169 6e3b  ype: text/plain;
+000000f0: 2063 6861 7273 6574 3d55 5446 2d38 0a43   charset=UTF-8.C
+00000100: 6f6e 7465 6e74 2d54 7261 6e73 6665 722d  ontent-Transfer-
+00000110: 456e 636f 6469 6e67 3a20 3862 6974 0a47  Encoding: 8bit.G
+00000120: 656e 6572 6174 6564 2d42 793a 2070 7967  enerated-By: pyg
+00000130: 6574 7465 7874 2e70 7920 312e 350a 506c  ettext.py 1.5.Pl
+00000140: 7572 616c 2d46 6f72 6d73 3a20 6e70 6c75  ural-Forms: nplu
+00000150: 7261 6c73 3d34 3b20 706c 7572 616c 3d28  rals=4; plural=(
+00000160: 6e3d 3d31 203f 2030 203a 2028 6e25 3130  n==1 ? 0 : (n%10
+00000170: 3e3d 3220 2626 206e 2531 303c 3d34 2920  >=2 && n%10<=4) 
+00000180: 2626 2028 6e25 3130 303c 3132 207c 7c20  && (n%100<12 || 
+00000190: 6e25 3130 303e 3134 2920 3f20 3120 3a20  n%100>14) ? 1 : 
+000001a0: 6e21 3d31 2026 2620 286e 2531 303e 3d30  n!=1 && (n%10>=0
+000001b0: 2026 2620 6e25 3130 3c3d 3129 207c 7c20   && n%10<=1) || 
+000001c0: 286e 2531 303e 3d35 2026 2620 6e25 3130  (n%10>=5 && n%10
+000001d0: 3c3d 3929 207c 7c20 286e 2531 3030 3e3d  <=9) || (n%100>=
+000001e0: 3132 2026 2620 6e25 3130 303c 3d31 3429  12 && n%100<=14)
+000001f0: 203f 2032 203a 2033 293b 0a58 2d43 726f   ? 2 : 3);.X-Cro
+00000200: 7764 696e 2d50 726f 6a65 6374 3a20 7370  wdin-Project: sp
+00000210: 7964 6572 2d6e 6f74 6562 6f6f 6b0a 582d  yder-notebook.X-
+00000220: 4372 6f77 6469 6e2d 5072 6f6a 6563 742d  Crowdin-Project-
+00000230: 4944 3a20 3338 3138 3033 0a58 2d43 726f  ID: 381803.X-Cro
+00000240: 7764 696e 2d4c 616e 6775 6167 653a 2070  wdin-Language: p
+00000250: 6c0a 582d 4372 6f77 6469 6e2d 4669 6c65  l.X-Crowdin-File
+00000260: 3a20 2f6d 6173 7465 722f 7370 7964 6572  : /master/spyder
+00000270: 5f6e 6f74 6562 6f6f 6b2f 6c6f 6361 6c65  _notebook/locale
+00000280: 2f73 7079 6465 725f 6e6f 7465 626f 6f6b  /spyder_notebook
+00000290: 2e70 6f74 0a58 2d43 726f 7764 696e 2d46  .pot.X-Crowdin-F
+000002a0: 696c 652d 4944 3a20 3137 0a4c 616e 6775  ile-ID: 17.Langu
+000002b0: 6167 653a 2070 6c5f 504c 0a00            age: pl_PL..
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/notebookplugin.py` & `spyder-notebook-0.5.0/spyder_notebook/notebookplugin.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,46 +1,45 @@
 # -*- coding: utf-8 -*-
 #
 # Copyright (c) Spyder Project Contributors
 # Licensed under the terms of the MIT License
 
 """Notebook plugin."""
 
-# Qt imports
-from qtpy.QtCore import Signal
+# Standard library imports
+import logging
+import os.path as osp
 
 # Spyder imports
 from spyder.api.plugins import Plugins, SpyderDockablePlugin
 from spyder.api.plugin_registration.decorators import (
     on_plugin_available, on_plugin_teardown)
 
 # Local imports
 from spyder_notebook.config import CONF_DEFAULTS, CONF_VERSION
 from spyder_notebook.confpage import NotebookConfigPage
 from spyder_notebook.widgets.main_widget import NotebookMainWidget
 from spyder_notebook.utils.localization import _
 
+logger = logging.getLogger(__name__)
+
 
 class NotebookPlugin(SpyderDockablePlugin):
     """Spyder Notebook plugin."""
 
     NAME = 'notebook'
     REQUIRES = [Plugins.Preferences]
     OPTIONAL = [Plugins.IPythonConsole]
     TABIFY = [Plugins.Editor]
     CONF_SECTION = NAME
     CONF_DEFAULTS = CONF_DEFAULTS
     CONF_VERSION = CONF_VERSION
     WIDGET_CLASS = NotebookMainWidget
     CONF_WIDGET_CLASS = NotebookConfigPage
 
-    # ---- Signals
-    # ------------------------------------------------------------------------
-    focus_changed = Signal()
-
     # ---- SpyderDockablePlugin API
     # ------------------------------------------------------------------------
     @staticmethod
     def get_name():
         """Return plugin name."""
         title = _('Notebook')
         return title
@@ -50,16 +49,16 @@
         return _("Work with Jupyter notebooks inside Spyder.")
 
     def get_icon(self):
         """Return plugin icon."""
         return self.create_icon('notebook')
 
     def on_initialize(self):
-        """Register plugin in Spyder's main window."""
-        self.focus_changed.connect(self.main.plugin_focus_changed)
+        """Set up the plugin; does nothing."""
+        pass
 
     @on_plugin_available(plugin=Plugins.Preferences)
     def on_preferences_available(self):
         preferences = self.get_plugin(Plugins.Preferences)
         preferences.register_plugin_preferences(self)
 
     @on_plugin_available(plugin=Plugins.IPythonConsole)
@@ -81,14 +80,15 @@
         self.get_widget().open_previous_session()
 
     # ------ Public API -------------------------------------------------------
     def open_notebook(self, filenames=None):
         self.get_widget().open_notebook(filenames)
 
     # ------ Private API ------------------------------------------------------
-    def _open_console(self, kernel_id, tab_name):
+    def _open_console(self, connection_file, tab_name):
         """Open an IPython console as requested."""
+        logger.info(f'Opening console with {connection_file=}')
         ipyconsole = self.get_plugin(Plugins.IPythonConsole)
-        ipyconsole.create_client_for_kernel(kernel_id)
+        ipyconsole.create_client_for_kernel(connection_file)
         ipyclient = ipyconsole.get_current_client()
         ipyclient.allow_rename = False
         ipyconsole.rename_client_tab(ipyclient, tab_name)
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/server/main.py` & `spyder-notebook-0.5.0/spyder_notebook/server/main.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,88 +1,98 @@
 # Copyright (c) Jupyter Development Team, Spyder Project Contributors.
 # Distributed under the terms of the Modified BSD License.
 
 """Entry point for server rendering notebooks for Spyder."""
 
 import os
-from jinja2 import FileSystemLoader
-from notebook.base.handlers import IPythonHandler, FileFindHandler
-from notebook.notebookapp import aliases, flags, NotebookApp
-from notebook.utils import url_path_join as ujoin
-from traitlets import Bool, Dict, Unicode
+from notebook.app import (
+    aliases, flags, JupyterNotebookApp, NotebookBaseHandler)
+from tornado import web
+from traitlets import default, Bool, Unicode
 
 HERE = os.path.dirname(__file__)
 
-aliases['info-file'] = 'SpyderNotebookServer.info_file_cmdline'
+aliases['info-file'] = 'SpyderNotebookApp.info_file_cmdline'
 
 flags['dark'] = (
-    {'SpyderNotebookServer': {'dark_theme': True}},
+    {'SpyderNotebookApp': {'dark_theme': True}},
     'Use dark theme when rendering notebooks'
 )
 
-class NotebookHandler(IPythonHandler):
-    """
-    Serve a notebook file from the filesystem in the notebook interface
-    """
-
-    def get(self, filename):
-        """Get the main page for the application's interface."""
-        # Options set here can be read with PageConfig.getOption
-        config_data = {
-            # Use camelCase here, since that's what the lab components expect
-            'baseUrl': self.base_url,
-            'token': self.settings['token'],
-            'darkTheme': self.settings['dark_theme'],
-            'notebookPath': filename,
-            'frontendUrl': ujoin(self.base_url, 'static/'),
-            # FIXME: Don't use a CDN here
-            'mathjaxUrl': 'https://cdnjs.cloudflare.com/ajax/libs/mathjax/'
-                          '2.7.5/MathJax.js',
-            'mathjaxConfig': "TeX-AMS_CHTML-full,Safe"
-        }
-        return self.write(
-            self.render_template(
-                'index.html',
-                static=self.static_url,
-                base_url=self.base_url,
-                config_data=config_data
-            )
-        )
-
-    def get_template(self, name):
-        loader = FileSystemLoader(HERE)
-        return loader.load(self.settings['jinja2_env'], name)
 
+class SpyderNotebookHandler(NotebookBaseHandler):
+    """A notebook page handler for Spyder."""
 
-class SpyderNotebookServer(NotebookApp):
-    """Server rendering notebooks in HTML and serving them over HTTP."""
+    def get_page_config(self):
+        page_config = super().get_page_config()
+        page_config['darkTheme'] = self.extensionapp.dark_theme
+        page_config['disabledExtensions'] = [
+            # Remove editor-related items from Settings menu
+            '@jupyterlab/fileeditor-extension',
+            # Remove items Open JupyterLab and File Browser from View menu
+            '@jupyter-notebook/application-extension:pages',
+            # Remove toolbar button Interface > Open With JupyterLab
+            '@jupyter-notebook/lab-extension:interface-switcher',
+            # Remove Launch Jupyter Notebook File Browser from Help menu
+            '@jupyter-notebook/lab-extension:launch-tree'
+        ]
+        return page_config
+
+    @web.authenticated
+    def get(self, path=None):
+        """Get the notebook page."""
+        tpl = self.render_template(
+            'notebook-template.html', page_config=self.get_page_config())
+        return self.write(tpl)
+
+
+class SpyderNotebookApp(JupyterNotebookApp):
+    """The Spyder notebook server extension app."""
 
-    flags = Dict(flags)
-    aliases = Dict(aliases)
+    name = 'spyder_notebook'
+    file_url_prefix = "/spyder-notebooks"
+
+    flags = dict(flags)
+    aliases = dict(aliases)
 
     dark_theme = Bool(
         False, config=True,
         help='Whether to use dark theme when rendering notebooks')
 
+    flags = flags
+
     info_file_cmdline = Unicode(
         '', config=True,
         help='Name of file in Jupyter runtime dir with connection info')
 
-    def init_webapp(self):
-        """Initialize tornado webapp and httpserver."""
-        self.tornado_settings['dark_theme'] = self.dark_theme
-        if self.info_file_cmdline:
-            self.info_file = os.path.join(
-                self.runtime_dir, self.info_file_cmdline)
-
-        super().init_webapp()
-
-        default_handlers = [
-            (ujoin(self.base_url, r'/notebook/(.*)'), NotebookHandler),
-            (ujoin(self.base_url, r"/static/(.*)"), FileFindHandler,
-                {'path': os.path.join(HERE, 'build')})
-        ]
-        self.web_app.add_handlers('.*$', default_handlers)
+    @default('static_dir')
+    def _default_static_dir(self):
+        return os.path.join(HERE, 'static')
+
+    @default('templates_dir')
+    def _default_templates_dir(self):
+        return HERE
+
+    def initialize_handlers(self):
+        """Initialize handlers."""
+        self.handlers.append(('/spyder-notebooks(.*)', SpyderNotebookHandler))
+        super().initialize_handlers()
+
+    @classmethod
+    def _load_jupyter_server_extension(cls, serverapp):
+        """
+        Overridden to propagate `info-file` command line parameter.
+
+        If the `info-file` command line parameter is given, then prepend the
+        Jupyter runtime directory and use the resulting path to store the
+        server info file.
+        """
+        extension = super()._load_jupyter_server_extension(serverapp)
+        if extension.info_file_cmdline:
+            serverapp.info_file = os.path.join(
+                serverapp.runtime_dir, extension.info_file_cmdline)
+        return extension
 
+main = SpyderNotebookApp.launch_instance
 
-if __name__ == '__main__':
-    SpyderNotebookServer.launch_instance()
+if __name__ == "__main__":
+    main()
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/tests/test_config.py` & `spyder-notebook-0.5.0/spyder_notebook/tests/test_config.py`

 * *Files identical despite different names*

### Comparing `spyder-notebook-0.4.1/spyder_notebook/utils/servermanager.py` & `spyder-notebook-0.5.0/spyder_notebook/utils/servermanager.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,15 +15,16 @@
 import sys
 
 # Qt imports
 from qtpy.QtCore import QObject, QProcess, QProcessEnvironment, QTimer, Signal
 
 # Third-party imports
 from jupyter_core.paths import jupyter_runtime_dir
-from notebook import notebookapp
+from jupyter_server import serverapp
+from tornado.httpclient import HTTPClientError
 
 # Spyder imports
 from spyder.config.base import DEV, get_home_dir, get_module_path
 
 
 # Kernel specification to use in notebook server
 KERNELSPEC = 'spyder.plugins.ipythonconsole.utils.kernelspec.SpyderKernelSpec'
@@ -200,21 +201,22 @@
         logger.debug('Starting new notebook server for %s', nbdir)
         process = QProcess(None)
         serverscript = osp.join(osp.dirname(__file__), '../server/main.py')
         serverscript = osp.normpath(serverscript)
         my_pid = os.getpid()
         server_index = len(self.servers) + 1
         info_file = f'spynbserver-{my_pid}-{server_index}.json'
-        arguments = [serverscript, '--no-browser',
+        arguments = ['-m', 'spyder_notebook.server', '--no-browser',
                      f'--info-file={info_file}',
                      f'--notebook-dir={nbdir}',
-                     '--NotebookApp.password=',
+                     '--ServerApp.password=',
                      f'--KernelSpecManager.kernel_spec_class={KERNELSPEC}']
         if self.dark_theme:
             arguments.append('--dark')
+
         logger.debug('Arguments: %s', repr(arguments))
 
         if DEV:
             env = QProcessEnvironment.systemEnvironment()
             env.insert('PYTHONPATH', osp.dirname(get_module_path('spyder')))
             process.setProcessEnvironment(env)
 
@@ -261,16 +263,17 @@
 
         runtime_dir = jupyter_runtime_dir()
         filename = osp.join(runtime_dir, server_process.info_file)
 
         try:
             with open(filename, encoding='utf-8') as f:
                 server_info = json.load(f)
-        except OSError:  # E.g., file does not exist
-            logger.debug(f'OSError when opening {filename}')
+        except (OSError, json.JSONDecodeError):
+            # E.g., file does not (yet) exist or is still being written
+            logger.debug(f'Error when opening {filename}')
             delay = datetime.datetime.now() - server_process.starttime
             if delay > datetime.timedelta(seconds=SERVER_TIMEOUT_DELAY):
                 logger.debug('Notebook server for %s timed out',
                              server_process.notebook_dir)
                 server_process.state = ServerState.TIMED_OUT
                 self.sig_server_timed_out.emit(server_process)
             else:
@@ -281,24 +284,53 @@
 
         logger.debug('Server for %s started', server_process.notebook_dir)
         server_process.state = ServerState.RUNNING
         server_process.server_info = server_info
         self.sig_server_started.emit(server_process)
 
     def shutdown_all_servers(self):
-        """Shutdown all running servers."""
+        """
+        Shutdown all servers.
+
+        Disconnect all signals of the server process and try to shutdown the
+        server nicely. However, if the server is still starting up, or if
+        shutting down nicely does not work, then kill the server process.
+        """
         for server in self.servers:
+            process = server.process
+            process.readyReadStandardOutput.disconnect()
+            process.errorOccurred.disconnect()
+            process.finished.disconnect()
+
             if server.state == ServerState.RUNNING:
                 logger.debug('Shutting down notebook server for %s',
                              server.notebook_dir)
-                server.process.errorOccurred.disconnect()
-                server.process.finished.disconnect()
-                notebookapp.shutdown_server(server.server_info)
+
+                try:
+                    serverapp.shutdown_server(server.server_info, log=logger)
+                except HTTPClientError as err:
+                    # No response received, typically due to time out
+                    if err.code == 599:
+                        logger.warning('Ignoring HTTPClientError '
+                                       'with code = 599')
+                    else:
+                        raise
+                except ConnectionError as err:
+                    logger.warning(f'Ignoring {err}')
+                server.state = ServerState.FINISHED
+
+            if server.state == ServerState.STARTING:
+                process.kill()
                 server.state = ServerState.FINISHED
 
+            if process.state() != QProcess.NotRunning:
+                # Should not be necessary, but make sure that process is killed
+                process.kill()
+
+
     def read_server_output(self, server_process):
         """
         Read the output of the notebook server process.
 
         This function is connected to the QProcess.readyReadStandardOutput
         signal. It reads the contents of the standard output channel of the
         server process and stores it in `server_process.output`. The standard
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/utils/templates/welcome-dark.html` & `spyder-notebook-0.5.0/spyder_notebook/utils/templates/welcome-dark.html`

 * *Files identical despite different names*

### Comparing `spyder-notebook-0.4.1/spyder_notebook/utils/templates/welcome.html` & `spyder-notebook-0.5.0/spyder_notebook/utils/templates/welcome.html`

 * *Files identical despite different names*

### Comparing `spyder-notebook-0.4.1/spyder_notebook/utils/tests/test_servermanager.py` & `spyder-notebook-0.5.0/spyder_notebook/utils/tests/test_servermanager.py`

 * *Files 2% similar despite different names*

```diff
@@ -73,17 +73,19 @@
     else:
         mock_start.assert_not_called()
 
 
 @pytest.mark.parametrize(('dark', 'under_home'),
                          [(True, True), (False, True), (False, False)])
 def test_start_server(mocker, dark, under_home):
-    """Test that .start_server() starts a process with the correct script file,
-    notebook dir, and dark argument; that it stores the server process in
-    `.servers`; and that it calls ._check_server_running()."""
+    """
+    Test that .start_server() starts a process with the correct arguments,
+    that it stores the server process in `.servers`; and that it calls
+    ._check_server_running().
+    """
     serverManager = ServerManager(dark)
     mock_check = mocker.patch.object(serverManager, '_check_server_started')
     mock_QProcess = mocker.patch(
         'spyder_notebook.utils.servermanager.QProcess', spec=QProcess)
     mocker.patch(
         'spyder_notebook.utils.servermanager.get_home_dir', return_value='foo')
     if under_home:
@@ -93,16 +95,14 @@
         filename = osp.join('notfoo', 'bar', 'ham.ipynb')
         nbdir = osp.join('notfoo', 'bar')
 
     serverManager.start_server(filename, '/ham/interpreter')
 
     mock_QProcess.return_value.start.assert_called_once()
     args = mock_QProcess.return_value.start.call_args[0]
-    import spyder_notebook.server.main
-    assert args[1][0] == spyder_notebook.server.main.__file__
     assert '--notebook-dir={}'.format(nbdir) in args[1]
     assert ('--dark' in args[1]) == dark
     assert len(serverManager.servers) == 1
     assert serverManager.servers[0].process == mock_QProcess.return_value
     assert serverManager.servers[0].notebook_dir == nbdir
     mock_check.assert_called_once()
 
@@ -191,15 +191,15 @@
     assert server_process.state == ServerState.ERROR
 
 
 def test_shutdown_all_servers(mocker):
     """Test that .shutdown_all_servers() does shutdown all running servers,
     but not servers in another state."""
     mock_shutdown = mocker.patch(
-        'spyder_notebook.utils.servermanager.notebookapp.shutdown_server')
+        'spyder_notebook.utils.servermanager.serverapp.shutdown_server')
     server1 = ServerProcess(
         mocker.Mock(spec=QProcess), '', '', '', state=ServerState.RUNNING,
         server_info=mocker.Mock(dict))
     server2 = ServerProcess(
         mocker.Mock(spec=QProcess), '', '', '', state=ServerState.ERROR,
         server_info=mocker.Mock(dict))
     serverManager = ServerManager()
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/widgets/client.py` & `spyder-notebook-0.5.0/spyder_notebook/widgets/client.py`

 * *Files 2% similar despite different names*

```diff
@@ -3,21 +3,22 @@
 # Copyright (c) Spyder Project Contributors
 # Licensed under the terms of the MIT License
 
 """Qt widgets for the notebook."""
 
 # Standard library imports
 import json
+import logging
 import os
 import os.path as osp
 from string import Template
 import sys
 
 # Third-party imports
-from notebook.utils import url_path_join, url_escape
+from jupyter_server.utils import url_path_join, url_escape
 import qstylizer
 from qtpy.QtCore import QEvent, QUrl, Qt, Signal
 from qtpy.QtGui import QColor, QFontMetrics, QFont
 from qtpy.QtWebEngineWidgets import (QWebEnginePage, QWebEngineSettings,
                                      QWebEngineView, WEBENGINE)
 from qtpy.QtWidgets import (QApplication, QMenu, QFrame, QVBoxLayout,
                             QMessageBox)
@@ -46,14 +47,16 @@
 TEMPLATES_PATH = osp.join(
     PLUGINS_PATH, 'ipythonconsole', 'assets', 'templates')
 
 BLANK = open(osp.join(TEMPLATES_PATH, 'blank.html')).read()
 LOADING = open(osp.join(TEMPLATES_PATH, 'loading.html')).read()
 KERNEL_ERROR = open(osp.join(TEMPLATES_PATH, 'kernel_error.html')).read()
 
+logger = logging.getLogger(__name__)
+
 
 # -----------------------------------------------------------------------------
 # Widgets
 # -----------------------------------------------------------------------------
 class WebViewInBrowser(QWebEngineView):
     """
     WebView which opens document in an external browser.
@@ -309,38 +312,39 @@
         token_url = url + '?token={}'.format(self.token)
         return token_url
 
     def register(self, server_info):
         """Register attributes that can be computed with the server info."""
         # Path relative to the server directory
         self.path = os.path.relpath(self.filename,
-                                    start=server_info['notebook_dir'])
+                                    start=server_info['root_dir'])
 
         # Replace backslashes on Windows
         if os.name == 'nt':
             self.path = self.path.replace('\\', '/')
 
         # Server url to send requests to
         self.server_url = server_info['url']
 
         # Server token
         self.token = server_info['token']
 
-        url = url_path_join(self.server_url, 'notebook',
+        url = url_path_join(self.server_url, 'spyder-notebooks',
                             url_escape(self.path))
 
         # Set file url to load this notebook
         self.file_url = self.add_token(url)
 
     def go_to(self, url_or_text):
         """Go to page URL."""
         if isinstance(url_or_text, str):
             url = QUrl(url_or_text)
         else:
             url = url_or_text
+        logger.debug(f'Going to URL {url_or_text}')
         self.notebookwidget.load(url)
 
     def load_notebook(self):
         """Load the associated notebook."""
         self.go_to(self.file_url)
 
     def get_filename(self):
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/widgets/dom.py` & `spyder-notebook-0.5.0/spyder_notebook/widgets/dom.py`

 * *Files identical despite different names*

### Comparing `spyder-notebook-0.4.1/spyder_notebook/widgets/example_app.py` & `spyder-notebook-0.5.0/spyder_notebook/widgets/example_app.py`

 * *Files identical despite different names*

### Comparing `spyder-notebook-0.4.1/spyder_notebook/widgets/main_widget.py` & `spyder-notebook-0.5.0/spyder_notebook/widgets/main_widget.py`

 * *Files 3% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 # Licensed under the terms of the MIT License
 # (see LICENSE.txt for details)
 
 # Standard library imports
 import os.path as osp
 
 # Third-party imports
+from jupyter_core.paths import jupyter_runtime_dir
 from qtpy.QtCore import Signal
 from qtpy.QtWidgets import QMessageBox, QVBoxLayout
 
 # Spyder imports
 from spyder.api.widgets.main_widget import PluginMainWidget
 from spyder.config.gui import is_dark_interface
 from spyder.utils.switcher import shorten_paths
@@ -55,16 +56,16 @@
 
     sig_open_console_requested = Signal(str, str)
     """
     Request to open an IPython console associated to a notebook.
 
     Parameters
     -----------
-    kernel_id: str
-        Id of the kernel to open a console for.
+    connection_file: str
+        Name of the connection file for the kernel to open a console for.
     tab_name: str
         Tab name to set for the created console.
     """
 
     def __init__(self, name, plugin, parent):
         """Widget constructor."""
         super().__init__(name, plugin, parent)
@@ -323,16 +324,18 @@
             QMessageBox.critical(
                 self,
                 _('Error opening console'),
                 _('There is no kernel associated to this notebook.')
             )
             return
 
+        connection_file = f'kernel-{kernel_id}.json'
+        connection_file = osp.join(jupyter_runtime_dir(), connection_file)
         self.sig_open_console_requested.emit(
-            kernel_id,
+            connection_file,
             client.get_short_name()
         )
 
     def view_servers(self):
         """Display server info."""
         dialog = ServerInfoDialog(self.server_manager.servers, parent=self)
         dialog.show()
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/widgets/notebooktabwidget.py` & `spyder-notebook-0.5.0/spyder_notebook/widgets/notebooktabwidget.py`

 * *Files 5% similar despite different names*

```diff
@@ -6,14 +6,15 @@
 """File implementing NotebookTabWidget."""
 
 # Standard library imports
 import logging
 import os
 import os.path as osp
 import sys
+import time
 
 # Qt imports
 from qtpy.compat import getopenfilenames, getsavefilename
 from qtpy.QtCore import QEventLoop, QTimer
 from qtpy.QtWidgets import QMessageBox
 
 # Third-party imports
@@ -47,14 +48,46 @@
 
 # How often to wait for that time
 WAIT_SAVE_ITERATIONS = 20
 
 logger = logging.getLogger(__name__)
 
 
+def remove_file_retry_if_in_use(filename):
+    """
+    Remove file, retrying if file is in use
+
+    On non-Windows systems, a file which is in use by another process can be
+    removed without problems. However, on Windows, attempting to remove a file
+    which is in use by another process raises an error.
+
+    Thus, this function simply removes the file on non-Windows systems.
+    On Windows sytems, if removing the file raises an error indicating that
+    the file is in use by another process, this function waits half a
+    second in that case and tries again. After three attempts, it gives up.
+
+    Parameters
+    ----------
+    filename : str
+        Name of file which should be deleted
+    """
+    if sys.platform != 'win32':
+        os.remove(filename)
+    else:
+        for attempt in range(3):
+            try:
+                os.remove(filename)
+                break
+            except PermissionError as error:
+                if error.winerror == 32:  # File is in use
+                    time.sleep(0.5)
+                else:
+                    raise
+
+
 class NotebookTabWidget(Tabs, SpyderConfigurationAccessor):
     """
     Tabbed widget whose tabs display notebooks.
 
     This is the main widget of the notebook plugin.
 
     Attributes
@@ -161,15 +194,15 @@
         client = NotebookClient(self, filename, self.actions)
         self.add_tab(client)
         interpreter = self.get_interpreter()
         server_info = self.server_manager.get_server(
             filename, interpreter, start=True)
         if server_info:
             logger.debug('Using existing server at %s',
-                         server_info['notebook_dir'])
+                         server_info['root_dir'])
             client.register(server_info)
             client.load_notebook()
         return client
 
     def get_interpreter(self):
         """
         Return the Python interpreter to be used in notebooks.
@@ -241,18 +274,15 @@
             if save_before_close:
                 filename = self.save_notebook(client)
             client.shutdown_kernel()
         client.close()
 
         # Delete notebook file if it is in temporary directory
         if filename.startswith(get_temp_dir()):
-            try:
-                os.remove(filename)
-            except EnvironmentError:
-                pass
+            remove_file_retry_if_in_use(filename)
 
         # Note: notebook index may have changed after closing related widgets
         self.removeTab(self.indexOf(client))
         self.maybe_create_welcome_client()
         return filename
 
     def save_notebook(self, client):
@@ -314,15 +344,15 @@
             wait_save = QEventLoop()
             QTimer.singleShot(WAIT_SAVE_DELAY, wait_save.quit)
             wait_save.exec_()
 
             # Try reading the file
             try:
                 nb_contents = nbformat.read(filename, as_version=4)
-            except FileNotFoundError:
+            except (FileNotFoundError, nbformat.reader.NotJSONError):
                 continue
 
             # If empty, we are done
             if (len(nb_contents['cells']) == 0
                     or len(nb_contents['cells'][0]['source']) == 0):
                 return True
             else:
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/widgets/serverinfo.py` & `spyder-notebook-0.5.0/spyder_notebook/widgets/serverinfo.py`

 * *Files identical despite different names*

### Comparing `spyder-notebook-0.4.1/spyder_notebook/widgets/tests/test_client.py` & `spyder-notebook-0.5.0/spyder_notebook/widgets/tests/test_client.py`

 * *Files 4% similar despite different names*

```diff
@@ -37,15 +37,15 @@
 @pytest.fixture
 def plugin(plugin_without_server):
     """
     Construct mock plugin with NotebookClient with server registered.
 
     Use `plugin.client` to access the client.
     """
-    server_info = {'notebook_dir': '/path/notebooks',
+    server_info = {'root_dir': '/path/notebooks',
                    'url': 'fake_url',
                    'token': 'fake_token'}
     plugin_without_server.client.register(server_info)
     return plugin_without_server
 
 
 def test_notebookwidget_create_window(plugin, mocker, qtbot):
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/widgets/tests/test_notebooktabwidget.py` & `spyder-notebook-0.5.0/spyder_notebook/widgets/tests/test_notebooktabwidget.py`

 * *Files 2% similar despite different names*

```diff
@@ -8,27 +8,28 @@
 # Standard library imports
 import collections
 import os.path as osp
 
 # Third party imports
 import pytest
 from qtpy.QtWidgets import QMessageBox
+from nbformat.reader import NotJSONError
 
 # Local imports
 from spyder_notebook.utils.servermanager import ServerManager
 from spyder_notebook.widgets.notebooktabwidget import (
     NotebookTabWidget, WAIT_SAVE_ITERATIONS)
 
 
 @pytest.fixture
 def tabwidget(mocker, qtbot):
     """Create an empty NotebookTabWidget which does not start up servers."""
     def fake_get_server(filename, interpreter, start):
         return collections.defaultdict(
-            str, filename=filename, notebook_dir=osp.dirname(filename))
+            str, filename=filename, root_dir=osp.dirname(filename))
 
     mocker.patch(
         'spyder_notebook.widgets.notebooktabwidget.WAIT_SAVE_DELAY', 1)
     fake_server_manager = mocker.Mock(
         spec=ServerManager, get_server=fake_get_server)
     widget = NotebookTabWidget(None, fake_server_manager)
     qtbot.addWidget(widget)
@@ -134,23 +135,24 @@
 
     result = tabwidget.wait_and_check_if_empty('ham.ipynb')
 
     mock_read.assert_called_once()
     assert result is False
 
 
-def test_wait_and_check_if_empty_with_delay(mocker, tabwidget):
+@pytest.mark.parametrize('exception', [FileNotFoundError, NotJSONError])
+def test_wait_and_check_if_empty_with_delay(mocker, tabwidget, exception):
     """Test that .wait_and_check_if_empty() on an empty notebook tries to read
-    it, and when that fails because the file does not exist, it tries again to
-    read it. When the read succeeds the second time and the notebook turns out
-    to be empty, the function returns True."""
+    it, and when that fails because the file does not exist or is not JSON, it
+    tries again to read it. When the read succeeds the second time and the
+    notebook turns out to be empty, the function returns True."""
     contents = {'cells': []}
     mock_read = mocker.patch(
         'spyder_notebook.widgets.notebooktabwidget.nbformat.read',
-        side_effect=[FileNotFoundError, contents])
+        side_effect=[exception, contents])
 
     result = tabwidget.wait_and_check_if_empty('ham.ipynb')
 
     assert mock_read.call_count == 2
     assert result is True
```

### Comparing `spyder-notebook-0.4.1/spyder_notebook/widgets/tests/test_serverinfo.py` & `spyder-notebook-0.5.0/spyder_notebook/widgets/tests/test_serverinfo.py`

 * *Files identical despite different names*

### Comparing `spyder-notebook-0.4.1/spyder_notebook.egg-info/PKG-INFO` & `spyder-notebook-0.5.0/spyder_notebook.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spyder-notebook
-Version: 0.4.1
+Version: 0.5.0
 Summary: Jupyter notebook integration with Spyder
 Home-page: https://github.com/spyder-ide/spyder-notebook
 Author: Spyder Development Team
 License: MIT
 Keywords: spyder jupyter notebook
 Classifier: Development Status :: 4 - Beta
 Classifier: Framework :: Jupyter
```

