# Comparing `tmp/mintpdf-1.0.tar.gz` & `tmp/mintpdf-1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mintpdf-1.0.tar", last modified: Fri Jul 21 09:18:19 2023, max compression
+gzip compressed data, was "mintpdf-1.1.tar", last modified: Sun Jul 23 15:10:16 2023, max compression
```

## Comparing `mintpdf-1.0.tar` & `mintpdf-1.1.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 greta      (501) staff       (20)        0 2023-07-21 09:18:19.009456 mintpdf-1.0/
--rw-r--r--   0 greta      (501) staff       (20)    35149 2023-07-21 09:13:10.000000 mintpdf-1.0/LICENSE
--rw-r--r--   0 greta      (501) staff       (20)      109 2023-07-21 09:18:19.009279 mintpdf-1.0/PKG-INFO
--rw-r--r--   0 greta      (501) staff       (20)       36 2023-07-21 09:10:49.000000 mintpdf-1.0/README.md
-drwxr-xr-x   0 greta      (501) staff       (20)        0 2023-07-21 09:18:19.008065 mintpdf-1.0/mintpdf/
--rw-r--r--   0 greta      (501) staff       (20)        0 2023-07-21 08:59:37.000000 mintpdf-1.0/mintpdf/__init__.py
--rw-r--r--   0 greta      (501) staff       (20)        0 2023-07-21 09:02:28.000000 mintpdf-1.0/mintpdf/pdf2image.py
--rw-r--r--   0 greta      (501) staff       (20)       37 2023-07-21 09:00:28.000000 mintpdf-1.0/mintpdf/pdf2text.py
-drwxr-xr-x   0 greta      (501) staff       (20)        0 2023-07-21 09:18:19.009012 mintpdf-1.0/mintpdf.egg-info/
--rw-r--r--   0 greta      (501) staff       (20)      109 2023-07-21 09:18:18.000000 mintpdf-1.0/mintpdf.egg-info/PKG-INFO
--rw-r--r--   0 greta      (501) staff       (20)      211 2023-07-21 09:18:19.000000 mintpdf-1.0/mintpdf.egg-info/SOURCES.txt
--rw-r--r--   0 greta      (501) staff       (20)        1 2023-07-21 09:18:18.000000 mintpdf-1.0/mintpdf.egg-info/dependency_links.txt
--rw-r--r--   0 greta      (501) staff       (20)        8 2023-07-21 09:18:18.000000 mintpdf-1.0/mintpdf.egg-info/top_level.txt
--rw-r--r--   0 greta      (501) staff       (20)       38 2023-07-21 09:18:19.009520 mintpdf-1.0/setup.cfg
--rw-r--r--   0 greta      (501) staff       (20)      219 2023-07-21 09:14:14.000000 mintpdf-1.0/setup.py
+drwxr-xr-x   0 greta      (501) staff       (20)        0 2023-07-23 15:10:16.366119 mintpdf-1.1/
+-rw-r--r--   0 greta      (501) staff       (20)    35149 2023-07-23 15:08:42.000000 mintpdf-1.1/LICENSE
+-rw-r--r--   0 greta      (501) staff       (20)      109 2023-07-23 15:10:16.365899 mintpdf-1.1/PKG-INFO
+-rw-r--r--   0 greta      (501) staff       (20)       36 2023-07-23 15:08:08.000000 mintpdf-1.1/README.md
+drwxr-xr-x   0 greta      (501) staff       (20)        0 2023-07-23 15:10:16.364438 mintpdf-1.1/mintpdf/
+-rw-r--r--   0 greta      (501) staff       (20)        0 2023-07-23 15:03:19.000000 mintpdf-1.1/mintpdf/__init__.py
+-rw-r--r--   0 greta      (501) staff       (20)       37 2023-07-23 15:05:20.000000 mintpdf-1.1/mintpdf/pdf2image.py
+-rw-r--r--   0 greta      (501) staff       (20)       37 2023-07-23 15:04:35.000000 mintpdf-1.1/mintpdf/pdf2text.py
+drwxr-xr-x   0 greta      (501) staff       (20)        0 2023-07-23 15:10:16.365558 mintpdf-1.1/mintpdf.egg-info/
+-rw-r--r--   0 greta      (501) staff       (20)      109 2023-07-23 15:10:16.000000 mintpdf-1.1/mintpdf.egg-info/PKG-INFO
+-rw-r--r--   0 greta      (501) staff       (20)      211 2023-07-23 15:10:16.000000 mintpdf-1.1/mintpdf.egg-info/SOURCES.txt
+-rw-r--r--   0 greta      (501) staff       (20)        1 2023-07-23 15:10:16.000000 mintpdf-1.1/mintpdf.egg-info/dependency_links.txt
+-rw-r--r--   0 greta      (501) staff       (20)        8 2023-07-23 15:10:16.000000 mintpdf-1.1/mintpdf.egg-info/top_level.txt
+-rw-r--r--   0 greta      (501) staff       (20)       38 2023-07-23 15:10:16.366273 mintpdf-1.1/setup.cfg
+-rw-r--r--   0 greta      (501) staff       (20)      220 2023-07-23 15:09:32.000000 mintpdf-1.1/setup.py
```

### Comparing `mintpdf-1.0/LICENSE` & `mintpdf-1.1/LICENSE`

 * *Files identical despite different names*

