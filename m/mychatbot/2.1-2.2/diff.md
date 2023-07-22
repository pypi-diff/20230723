# Comparing `tmp/mychatbot-2.1.tar.gz` & `tmp/mychatbot-2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mychatbot-2.1.tar", last modified: Sat Jul 22 22:41:56 2023, max compression
+gzip compressed data, was "mychatbot-2.2.tar", last modified: Sat Jul 22 22:53:52 2023, max compression
```

## Comparing `mychatbot-2.1.tar` & `mychatbot-2.2.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 22:41:56.564557 mychatbot-2.1/
--rw-r--r--   0 kunal      (501) staff       (20)       51 2023-07-22 22:41:56.564435 mychatbot-2.1/PKG-INFO
-drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 22:41:56.563525 mychatbot-2.1/mychatbot/
--rw-r--r--   0 kunal      (501) staff       (20)        0 2023-07-22 19:42:40.000000 mychatbot-2.1/mychatbot/__init__.py
--rw-r--r--   0 kunal      (501) staff       (20)      506 2023-07-22 21:53:46.000000 mychatbot-2.1/mychatbot/ai.py
-drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 22:41:56.564268 mychatbot-2.1/mychatbot.egg-info/
--rw-r--r--   0 kunal      (501) staff       (20)       51 2023-07-22 22:41:56.000000 mychatbot-2.1/mychatbot.egg-info/PKG-INFO
--rw-r--r--   0 kunal      (501) staff       (20)      210 2023-07-22 22:41:56.000000 mychatbot-2.1/mychatbot.egg-info/SOURCES.txt
--rw-r--r--   0 kunal      (501) staff       (20)        1 2023-07-22 22:41:56.000000 mychatbot-2.1/mychatbot.egg-info/dependency_links.txt
--rw-r--r--   0 kunal      (501) staff       (20)        8 2023-07-22 22:41:56.000000 mychatbot-2.1/mychatbot.egg-info/requires.txt
--rw-r--r--   0 kunal      (501) staff       (20)       10 2023-07-22 22:41:56.000000 mychatbot-2.1/mychatbot.egg-info/top_level.txt
--rw-r--r--   0 kunal      (501) staff       (20)       38 2023-07-22 22:41:56.564593 mychatbot-2.1/setup.cfg
--rw-r--r--   0 kunal      (501) staff       (20)      185 2023-07-22 22:41:44.000000 mychatbot-2.1/setup.py
+drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 22:53:52.067520 mychatbot-2.2/
+-rw-r--r--   0 kunal      (501) staff       (20)       51 2023-07-22 22:53:52.067383 mychatbot-2.2/PKG-INFO
+drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 22:53:52.066275 mychatbot-2.2/mychatbot/
+-rw-r--r--   0 kunal      (501) staff       (20)        0 2023-07-22 19:42:40.000000 mychatbot-2.2/mychatbot/__init__.py
+-rw-r--r--   0 kunal      (501) staff       (20)     1410 2023-07-22 22:52:32.000000 mychatbot-2.2/mychatbot/ai.py
+drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 22:53:52.067197 mychatbot-2.2/mychatbot.egg-info/
+-rw-r--r--   0 kunal      (501) staff       (20)       51 2023-07-22 22:53:52.000000 mychatbot-2.2/mychatbot.egg-info/PKG-INFO
+-rw-r--r--   0 kunal      (501) staff       (20)      210 2023-07-22 22:53:52.000000 mychatbot-2.2/mychatbot.egg-info/SOURCES.txt
+-rw-r--r--   0 kunal      (501) staff       (20)        1 2023-07-22 22:53:52.000000 mychatbot-2.2/mychatbot.egg-info/dependency_links.txt
+-rw-r--r--   0 kunal      (501) staff       (20)        8 2023-07-22 22:53:52.000000 mychatbot-2.2/mychatbot.egg-info/requires.txt
+-rw-r--r--   0 kunal      (501) staff       (20)       10 2023-07-22 22:53:52.000000 mychatbot-2.2/mychatbot.egg-info/top_level.txt
+-rw-r--r--   0 kunal      (501) staff       (20)       38 2023-07-22 22:53:52.067564 mychatbot-2.2/setup.cfg
+-rw-r--r--   0 kunal      (501) staff       (20)      185 2023-07-22 22:53:09.000000 mychatbot-2.2/setup.py
```

