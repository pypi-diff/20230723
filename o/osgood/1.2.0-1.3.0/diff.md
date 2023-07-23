# Comparing `tmp/osgood-1.2.0.tar.gz` & `tmp/osgood-1.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "osgood-1.2.0.tar", last modified: Sat Apr 22 23:04:54 2023, max compression
+gzip compressed data, was "osgood-1.3.0.tar", last modified: Sun Jul 23 20:17:22 2023, max compression
```

## Comparing `osgood-1.2.0.tar` & `osgood-1.3.0.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxr-xr-x   0 tolyosgood   (501) staff       (20)        0 2023-04-22 23:04:54.877479 osgood-1.2.0/
--rw-r--r--   0 tolyosgood   (501) staff       (20)     1064 2023-04-01 13:42:12.000000 osgood-1.2.0/LICENSE
--rw-r--r--   0 tolyosgood   (501) staff       (20)      793 2023-04-22 23:04:54.877262 osgood-1.2.0/PKG-INFO
--rw-r--r--   0 tolyosgood   (501) staff       (20)      266 2023-04-01 13:42:12.000000 osgood-1.2.0/README.md
-drwxr-xr-x   0 tolyosgood   (501) staff       (20)        0 2023-04-22 23:04:54.875806 osgood-1.2.0/osgood/
--rw-r--r--   0 tolyosgood   (501) staff       (20)       86 2023-04-01 14:27:32.000000 osgood-1.2.0/osgood/__init__.py
--rw-r--r--   0 tolyosgood   (501) staff       (20)     2265 2023-04-01 14:27:32.000000 osgood-1.2.0/osgood/base.py
-drwxr-xr-x   0 tolyosgood   (501) staff       (20)        0 2023-04-22 23:04:54.876621 osgood-1.2.0/osgood.egg-info/
--rw-r--r--   0 tolyosgood   (501) staff       (20)      793 2023-04-22 23:04:54.000000 osgood-1.2.0/osgood.egg-info/PKG-INFO
--rw-r--r--   0 tolyosgood   (501) staff       (20)      205 2023-04-22 23:04:54.000000 osgood-1.2.0/osgood.egg-info/SOURCES.txt
--rw-r--r--   0 tolyosgood   (501) staff       (20)        1 2023-04-22 23:04:54.000000 osgood-1.2.0/osgood.egg-info/dependency_links.txt
--rw-r--r--   0 tolyosgood   (501) staff       (20)        7 2023-04-22 23:04:54.000000 osgood-1.2.0/osgood.egg-info/top_level.txt
--rw-r--r--   0 tolyosgood   (501) staff       (20)      601 2023-04-22 23:03:04.000000 osgood-1.2.0/pyproject.toml
--rw-r--r--   0 tolyosgood   (501) staff       (20)       38 2023-04-22 23:04:54.877549 osgood-1.2.0/setup.cfg
-drwxr-xr-x   0 tolyosgood   (501) staff       (20)        0 2023-04-22 23:04:54.876786 osgood-1.2.0/tests/
--rw-r--r--   0 tolyosgood   (501) staff       (20)     1095 2023-04-01 14:27:32.000000 osgood-1.2.0/tests/test_base.py
+drwxr-xr-x   0 tolyosgood   (501) staff       (20)        0 2023-07-23 20:17:22.512580 osgood-1.3.0/
+-rw-r--r--   0 tolyosgood   (501) staff       (20)     1064 2023-04-01 13:42:12.000000 osgood-1.3.0/LICENSE
+-rw-r--r--   0 tolyosgood   (501) staff       (20)     1754 2023-07-23 20:17:22.512409 osgood-1.3.0/PKG-INFO
+-rw-r--r--   0 tolyosgood   (501) staff       (20)     1227 2023-07-23 20:16:49.000000 osgood-1.3.0/README.md
+drwxr-xr-x   0 tolyosgood   (501) staff       (20)        0 2023-07-23 20:17:22.511288 osgood-1.3.0/osgood/
+-rw-r--r--   0 tolyosgood   (501) staff       (20)      115 2023-07-23 20:14:36.000000 osgood-1.3.0/osgood/__init__.py
+-rw-r--r--   0 tolyosgood   (501) staff       (20)     3347 2023-07-23 20:14:36.000000 osgood-1.3.0/osgood/base.py
+drwxr-xr-x   0 tolyosgood   (501) staff       (20)        0 2023-07-23 20:17:22.511998 osgood-1.3.0/osgood.egg-info/
+-rw-r--r--   0 tolyosgood   (501) staff       (20)     1754 2023-07-23 20:17:22.000000 osgood-1.3.0/osgood.egg-info/PKG-INFO
+-rw-r--r--   0 tolyosgood   (501) staff       (20)      205 2023-07-23 20:17:22.000000 osgood-1.3.0/osgood.egg-info/SOURCES.txt
+-rw-r--r--   0 tolyosgood   (501) staff       (20)        1 2023-07-23 20:17:22.000000 osgood-1.3.0/osgood.egg-info/dependency_links.txt
+-rw-r--r--   0 tolyosgood   (501) staff       (20)        7 2023-07-23 20:17:22.000000 osgood-1.3.0/osgood.egg-info/top_level.txt
+-rw-r--r--   0 tolyosgood   (501) staff       (20)      632 2023-07-23 20:14:36.000000 osgood-1.3.0/pyproject.toml
+-rw-r--r--   0 tolyosgood   (501) staff       (20)       38 2023-07-23 20:17:22.512638 osgood-1.3.0/setup.cfg
+drwxr-xr-x   0 tolyosgood   (501) staff       (20)        0 2023-07-23 20:17:22.512131 osgood-1.3.0/tests/
+-rw-r--r--   0 tolyosgood   (501) staff       (20)     2018 2023-07-23 20:14:36.000000 osgood-1.3.0/tests/test_base.py
```

### Comparing `osgood-1.2.0/LICENSE` & `osgood-1.3.0/LICENSE`

 * *Files identical despite different names*

