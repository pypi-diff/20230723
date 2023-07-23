# Comparing `tmp/utsav-0.1.tar.gz` & `tmp/utsav-0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "utsav-0.1.tar", last modified: Sun Jul 23 05:58:01 2023, max compression
+gzip compressed data, was "utsav-0.2.tar", last modified: Sun Jul 23 06:06:11 2023, max compression
```

## Comparing `utsav-0.1.tar` & `utsav-0.2.tar`

### file list

```diff
@@ -1,9 +1,9 @@
-drwxr-xr-x   0 ugalab4    (502) staff       (20)        0 2023-07-23 05:58:01.801233 utsav-0.1/
--rw-r--r--   0 ugalab4    (502) staff       (20)       47 2023-07-23 05:58:01.801099 utsav-0.1/PKG-INFO
--rw-r--r--   0 ugalab4    (502) staff       (20)       38 2023-07-23 05:58:01.801273 utsav-0.1/setup.cfg
--rw-r--r--   0 ugalab4    (502) staff       (20)      122 2023-07-23 05:48:56.000000 utsav-0.1/setup.py
-drwxr-xr-x   0 ugalab4    (502) staff       (20)        0 2023-07-23 05:58:01.800923 utsav-0.1/utsav.egg-info/
--rw-r--r--   0 ugalab4    (502) staff       (20)       47 2023-07-23 05:58:01.000000 utsav-0.1/utsav.egg-info/PKG-INFO
--rw-r--r--   0 ugalab4    (502) staff       (20)      124 2023-07-23 05:58:01.000000 utsav-0.1/utsav.egg-info/SOURCES.txt
--rw-r--r--   0 ugalab4    (502) staff       (20)        1 2023-07-23 05:58:01.000000 utsav-0.1/utsav.egg-info/dependency_links.txt
--rw-r--r--   0 ugalab4    (502) staff       (20)        1 2023-07-23 05:58:01.000000 utsav-0.1/utsav.egg-info/top_level.txt
+drwxr-xr-x   0 ugalab4    (502) staff       (20)        0 2023-07-23 06:06:11.303469 utsav-0.2/
+-rw-r--r--   0 ugalab4    (502) staff       (20)       47 2023-07-23 06:06:11.303328 utsav-0.2/PKG-INFO
+-rw-r--r--   0 ugalab4    (502) staff       (20)       38 2023-07-23 06:06:11.303515 utsav-0.2/setup.cfg
+-rw-r--r--   0 ugalab4    (502) staff       (20)      122 2023-07-23 06:05:56.000000 utsav-0.2/setup.py
+drwxr-xr-x   0 ugalab4    (502) staff       (20)        0 2023-07-23 06:06:11.303136 utsav-0.2/utsav.egg-info/
+-rw-r--r--   0 ugalab4    (502) staff       (20)       47 2023-07-23 06:06:11.000000 utsav-0.2/utsav.egg-info/PKG-INFO
+-rw-r--r--   0 ugalab4    (502) staff       (20)      124 2023-07-23 06:06:11.000000 utsav-0.2/utsav.egg-info/SOURCES.txt
+-rw-r--r--   0 ugalab4    (502) staff       (20)        1 2023-07-23 06:06:11.000000 utsav-0.2/utsav.egg-info/dependency_links.txt
+-rw-r--r--   0 ugalab4    (502) staff       (20)        1 2023-07-23 06:06:11.000000 utsav-0.2/utsav.egg-info/top_level.txt
```

