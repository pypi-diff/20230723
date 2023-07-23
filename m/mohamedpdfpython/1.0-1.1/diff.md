# Comparing `tmp/mohamedpdfpython-1.0.tar.gz` & `tmp/mohamedpdfpython-1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mohamedpdfpython-1.0.tar", last modified: Sun Jul 23 13:59:32 2023, max compression
+gzip compressed data, was "mohamedpdfpython-1.1.tar", last modified: Sun Jul 23 15:04:22 2023, max compression
```

## Comparing `mohamedpdfpython-1.0.tar` & `mohamedpdfpython-1.1.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-07-23 13:59:32.435465 mohamedpdfpython-1.0/
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)    35148 2023-07-23 13:50:00.000000 mohamedpdfpython-1.0/LICENSE
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)      119 2023-07-23 13:59:32.435465 mohamedpdfpython-1.0/PKG-INFO
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)       37 2023-07-23 13:45:32.000000 mohamedpdfpython-1.0/README.md
-drwxr-xr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-07-23 13:59:32.431465 mohamedpdfpython-1.0/mohamedpdfpython.egg-info/
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)      119 2023-07-23 13:59:32.000000 mohamedpdfpython-1.0/mohamedpdfpython.egg-info/PKG-INFO
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)      253 2023-07-23 13:59:32.000000 mohamedpdfpython-1.0/mohamedpdfpython.egg-info/SOURCES.txt
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)        1 2023-07-23 13:59:32.000000 mohamedpdfpython-1.0/mohamedpdfpython.egg-info/dependency_links.txt
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)       10 2023-07-23 13:59:32.000000 mohamedpdfpython-1.0/mohamedpdfpython.egg-info/top_level.txt
-drwxr-xr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-07-23 13:59:32.431465 mohamedpdfpython-1.0/pdfpython/
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)        0 2023-07-23 13:27:18.000000 mohamedpdfpython-1.0/pdfpython/__init__.py
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)        0 2023-07-23 13:28:22.000000 mohamedpdfpython-1.0/pdfpython/pdf2image.py
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)       36 2023-07-23 13:27:45.000000 mohamedpdfpython-1.0/pdfpython/pdf2text.py
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)       38 2023-07-23 13:59:32.435465 mohamedpdfpython-1.0/setup.cfg
--rw-r--r--   0 mohamed   (1000) mohamed   (1000)      226 2023-07-23 13:51:07.000000 mohamedpdfpython-1.0/setup.py
+drwxr-xr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-07-23 15:04:22.954553 mohamedpdfpython-1.1/
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)    35148 2023-07-23 13:50:00.000000 mohamedpdfpython-1.1/LICENSE
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)      155 2023-07-23 15:04:22.954553 mohamedpdfpython-1.1/PKG-INFO
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)       73 2023-07-23 14:07:55.000000 mohamedpdfpython-1.1/README.md
+drwxr-xr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-07-23 15:04:22.950553 mohamedpdfpython-1.1/mohamedpdfpython.egg-info/
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)      155 2023-07-23 15:04:22.000000 mohamedpdfpython-1.1/mohamedpdfpython.egg-info/PKG-INFO
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)      253 2023-07-23 15:04:22.000000 mohamedpdfpython-1.1/mohamedpdfpython.egg-info/SOURCES.txt
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)        1 2023-07-23 15:04:22.000000 mohamedpdfpython-1.1/mohamedpdfpython.egg-info/dependency_links.txt
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)       10 2023-07-23 15:04:22.000000 mohamedpdfpython-1.1/mohamedpdfpython.egg-info/top_level.txt
+drwxr-xr-x   0 mohamed   (1000) mohamed   (1000)        0 2023-07-23 15:04:22.954553 mohamedpdfpython-1.1/pdfpython/
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)        0 2023-07-23 13:27:18.000000 mohamedpdfpython-1.1/pdfpython/__init__.py
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)        0 2023-07-23 13:28:22.000000 mohamedpdfpython-1.1/pdfpython/pdf2image.py
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)       64 2023-07-23 15:03:49.000000 mohamedpdfpython-1.1/pdfpython/pdf2text.py
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)       38 2023-07-23 15:04:22.954553 mohamedpdfpython-1.1/setup.cfg
+-rw-r--r--   0 mohamed   (1000) mohamed   (1000)      226 2023-07-23 15:03:19.000000 mohamedpdfpython-1.1/setup.py
```

### Comparing `mohamedpdfpython-1.0/LICENSE` & `mohamedpdfpython-1.1/LICENSE`

 * *Files identical despite different names*

