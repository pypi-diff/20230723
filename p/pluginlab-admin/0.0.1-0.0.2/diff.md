# Comparing `tmp/pluginlab_admin-0.0.1.tar.gz` & `tmp/pluginlab_admin-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pluginlab_admin-0.0.1.tar", last modified: Sun Jul 23 16:08:45 2023, max compression
+gzip compressed data, was "pluginlab_admin-0.0.2.tar", last modified: Sun Jul 23 16:18:19 2023, max compression
```

## Comparing `pluginlab_admin-0.0.1.tar` & `pluginlab_admin-0.0.2.tar`

### file list

```diff
@@ -1,17 +1,18 @@
-drwxr-xr-x   0 aurelienbrabant   (501) staff       (20)        0 2023-07-23 16:08:45.950632 pluginlab_admin-0.0.1/
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)      140 2023-07-23 16:08:45.950523 pluginlab_admin-0.0.1/PKG-INFO
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)     4730 2023-07-23 16:02:59.000000 pluginlab_admin-0.0.1/README.md
-drwxr-xr-x   0 aurelienbrabant   (501) staff       (20)        0 2023-07-23 16:08:45.949775 pluginlab_admin-0.0.1/pluginlab_admin/
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)       66 2023-07-23 15:50:42.000000 pluginlab_admin-0.0.1/pluginlab_admin/__init__.py
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)      909 2023-07-23 14:10:44.000000 pluginlab_admin-0.0.1/pluginlab_admin/app.py
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)     6337 2023-07-23 14:10:40.000000 pluginlab_admin-0.0.1/pluginlab_admin/auth.py
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)      612 2023-07-23 01:01:56.000000 pluginlab_admin-0.0.1/pluginlab_admin/token_verifier.py
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)      894 2023-07-23 13:09:00.000000 pluginlab_admin-0.0.1/pluginlab_admin/webhook.py
-drwxr-xr-x   0 aurelienbrabant   (501) staff       (20)        0 2023-07-23 16:08:45.950367 pluginlab_admin-0.0.1/pluginlab_admin.egg-info/
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)      140 2023-07-23 16:08:45.000000 pluginlab_admin-0.0.1/pluginlab_admin.egg-info/PKG-INFO
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)      348 2023-07-23 16:08:45.000000 pluginlab_admin-0.0.1/pluginlab_admin.egg-info/SOURCES.txt
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)        1 2023-07-23 16:08:45.000000 pluginlab_admin-0.0.1/pluginlab_admin.egg-info/dependency_links.txt
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)       52 2023-07-23 16:08:45.000000 pluginlab_admin-0.0.1/pluginlab_admin.egg-info/requires.txt
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)       16 2023-07-23 16:08:45.000000 pluginlab_admin-0.0.1/pluginlab_admin.egg-info/top_level.txt
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)       38 2023-07-23 16:08:45.950674 pluginlab_admin-0.0.1/setup.cfg
--rw-r--r--   0 aurelienbrabant   (501) staff       (20)      236 2023-07-23 00:48:16.000000 pluginlab_admin-0.0.1/setup.py
+drwxr-xr-x   0 aurelienbrabant   (501) staff       (20)        0 2023-07-23 16:18:19.831738 pluginlab_admin-0.0.2/
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)       18 2023-07-23 16:14:55.000000 pluginlab_admin-0.0.2/MANIFEST.in
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)      140 2023-07-23 16:18:19.831629 pluginlab_admin-0.0.2/PKG-INFO
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)     4730 2023-07-23 16:02:59.000000 pluginlab_admin-0.0.2/README.md
+drwxr-xr-x   0 aurelienbrabant   (501) staff       (20)        0 2023-07-23 16:18:19.830893 pluginlab_admin-0.0.2/pluginlab_admin/
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)       66 2023-07-23 15:50:42.000000 pluginlab_admin-0.0.2/pluginlab_admin/__init__.py
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)      909 2023-07-23 14:10:44.000000 pluginlab_admin-0.0.2/pluginlab_admin/app.py
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)     6337 2023-07-23 14:10:40.000000 pluginlab_admin-0.0.2/pluginlab_admin/auth.py
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)      612 2023-07-23 01:01:56.000000 pluginlab_admin-0.0.2/pluginlab_admin/token_verifier.py
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)      894 2023-07-23 13:09:00.000000 pluginlab_admin-0.0.2/pluginlab_admin/webhook.py
+drwxr-xr-x   0 aurelienbrabant   (501) staff       (20)        0 2023-07-23 16:18:19.831470 pluginlab_admin-0.0.2/pluginlab_admin.egg-info/
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)      140 2023-07-23 16:18:19.000000 pluginlab_admin-0.0.2/pluginlab_admin.egg-info/PKG-INFO
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)      360 2023-07-23 16:18:19.000000 pluginlab_admin-0.0.2/pluginlab_admin.egg-info/SOURCES.txt
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)        1 2023-07-23 16:18:19.000000 pluginlab_admin-0.0.2/pluginlab_admin.egg-info/dependency_links.txt
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)       52 2023-07-23 16:18:19.000000 pluginlab_admin-0.0.2/pluginlab_admin.egg-info/requires.txt
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)       16 2023-07-23 16:18:19.000000 pluginlab_admin-0.0.2/pluginlab_admin.egg-info/top_level.txt
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)       38 2023-07-23 16:18:19.831776 pluginlab_admin-0.0.2/setup.cfg
+-rw-r--r--   0 aurelienbrabant   (501) staff       (20)      267 2023-07-23 16:18:11.000000 pluginlab_admin-0.0.2/setup.py
```

### Comparing `pluginlab_admin-0.0.1/README.md` & `pluginlab_admin-0.0.2/README.md`

 * *Files identical despite different names*

### Comparing `pluginlab_admin-0.0.1/pluginlab_admin/app.py` & `pluginlab_admin-0.0.2/pluginlab_admin/app.py`

 * *Files identical despite different names*

### Comparing `pluginlab_admin-0.0.1/pluginlab_admin/auth.py` & `pluginlab_admin-0.0.2/pluginlab_admin/auth.py`

 * *Files identical despite different names*

### Comparing `pluginlab_admin-0.0.1/pluginlab_admin/token_verifier.py` & `pluginlab_admin-0.0.2/pluginlab_admin/token_verifier.py`

 * *Files identical despite different names*

### Comparing `pluginlab_admin-0.0.1/pluginlab_admin/webhook.py` & `pluginlab_admin-0.0.2/pluginlab_admin/webhook.py`

 * *Files identical despite different names*

