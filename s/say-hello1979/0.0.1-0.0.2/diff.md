# Comparing `tmp/say_hello1979-0.0.1.tar.gz` & `tmp/say_hello1979-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "say_hello1979-0.0.1.tar", last modified: Sun Jul 23 01:26:17 2023, max compression
+gzip compressed data, was "say_hello1979-0.0.2.tar", last modified: Sun Jul 23 01:49:10 2023, max compression
```

## Comparing `say_hello1979-0.0.1.tar` & `say_hello1979-0.0.2.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxrwxr-x   0 reza      (1000) reza      (1000)        0 2023-07-23 01:26:17.808101 say_hello1979-0.0.1/
--rw-rw-r--   0 reza      (1000) reza      (1000)       80 2023-07-23 01:26:17.808101 say_hello1979-0.0.1/PKG-INFO
-drwxrwxr-x   0 reza      (1000) reza      (1000)        0 2023-07-23 01:26:17.804101 say_hello1979-0.0.1/say_hello1979/
--rw-rw-r--   0 reza      (1000) reza      (1000)       29 2023-07-22 20:38:01.000000 say_hello1979-0.0.1/say_hello1979/__init__.py
--rw-rw-r--   0 reza      (1000) reza      (1000)       36 2023-07-22 20:37:23.000000 say_hello1979-0.0.1/say_hello1979/hello.py
-drwxrwxr-x   0 reza      (1000) reza      (1000)        0 2023-07-23 01:26:17.808101 say_hello1979-0.0.1/say_hello1979.egg-info/
--rw-rw-r--   0 reza      (1000) reza      (1000)       80 2023-07-23 01:26:17.000000 say_hello1979-0.0.1/say_hello1979.egg-info/PKG-INFO
--rw-rw-r--   0 reza      (1000) reza      (1000)      241 2023-07-23 01:26:17.000000 say_hello1979-0.0.1/say_hello1979.egg-info/SOURCES.txt
--rw-rw-r--   0 reza      (1000) reza      (1000)        1 2023-07-23 01:26:17.000000 say_hello1979-0.0.1/say_hello1979.egg-info/dependency_links.txt
--rw-rw-r--   0 reza      (1000) reza      (1000)        1 2023-07-23 01:26:09.000000 say_hello1979-0.0.1/say_hello1979.egg-info/not-zip-safe
--rw-rw-r--   0 reza      (1000) reza      (1000)       14 2023-07-23 01:26:17.000000 say_hello1979-0.0.1/say_hello1979.egg-info/top_level.txt
--rw-rw-r--   0 reza      (1000) reza      (1000)       38 2023-07-23 01:26:17.808101 say_hello1979-0.0.1/setup.cfg
--rw-rw-r--   0 reza      (1000) reza      (1000)      193 2023-07-23 01:25:44.000000 say_hello1979-0.0.1/setup.py
+drwxrwxr-x   0 reza      (1000) reza      (1000)        0 2023-07-23 01:49:10.029838 say_hello1979-0.0.2/
+-rw-rw-r--   0 reza      (1000) reza      (1000)       80 2023-07-23 01:49:10.029838 say_hello1979-0.0.2/PKG-INFO
+drwxrwxr-x   0 reza      (1000) reza      (1000)        0 2023-07-23 01:49:10.029838 say_hello1979-0.0.2/say_hello1979/
+-rw-rw-r--   0 reza      (1000) reza      (1000)       30 2023-07-23 01:43:39.000000 say_hello1979-0.0.2/say_hello1979/__init__.py
+-rw-rw-r--   0 reza      (1000) reza      (1000)       36 2023-07-22 20:37:23.000000 say_hello1979-0.0.2/say_hello1979/hello.py
+drwxrwxr-x   0 reza      (1000) reza      (1000)        0 2023-07-23 01:49:10.029838 say_hello1979-0.0.2/say_hello1979.egg-info/
+-rw-rw-r--   0 reza      (1000) reza      (1000)       80 2023-07-23 01:49:09.000000 say_hello1979-0.0.2/say_hello1979.egg-info/PKG-INFO
+-rw-rw-r--   0 reza      (1000) reza      (1000)      241 2023-07-23 01:49:09.000000 say_hello1979-0.0.2/say_hello1979.egg-info/SOURCES.txt
+-rw-rw-r--   0 reza      (1000) reza      (1000)        1 2023-07-23 01:49:09.000000 say_hello1979-0.0.2/say_hello1979.egg-info/dependency_links.txt
+-rw-rw-r--   0 reza      (1000) reza      (1000)        1 2023-07-23 01:49:09.000000 say_hello1979-0.0.2/say_hello1979.egg-info/not-zip-safe
+-rw-rw-r--   0 reza      (1000) reza      (1000)       14 2023-07-23 01:49:09.000000 say_hello1979-0.0.2/say_hello1979.egg-info/top_level.txt
+-rw-rw-r--   0 reza      (1000) reza      (1000)       38 2023-07-23 01:49:10.029838 say_hello1979-0.0.2/setup.cfg
+-rw-rw-r--   0 reza      (1000) reza      (1000)      193 2023-07-23 01:44:39.000000 say_hello1979-0.0.2/setup.py
```

