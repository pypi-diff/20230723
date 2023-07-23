# Comparing `tmp/ldanansi-1.1.1.tar.gz` & `tmp/ldanansi-1.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ldanansi-1.1.1.tar", last modified: Sat Jul 22 23:27:27 2023, max compression
+gzip compressed data, was "ldanansi-1.1.2.tar", last modified: Sun Jul 23 07:47:47 2023, max compression
```

## Comparing `ldanansi-1.1.1.tar` & `ldanansi-1.1.2.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 trevormaseleme   (502) staff       (20)        0 2023-07-22 23:27:27.545748 ldanansi-1.1.1/
--rw-r--r--   0 trevormaseleme   (502) staff       (20)     1072 2023-07-03 08:19:40.000000 ldanansi-1.1.1/LICENSE
--rw-r--r--   0 trevormaseleme   (502) staff       (20)      485 2023-07-22 23:27:27.545453 ldanansi-1.1.1/PKG-INFO
--rw-r--r--   0 trevormaseleme   (502) staff       (20)      807 2023-07-07 07:34:03.000000 ldanansi-1.1.1/README.md
-drwxr-xr-x   0 trevormaseleme   (502) staff       (20)        0 2023-07-22 23:27:27.539009 ldanansi-1.1.1/idanansi/
--rw-r--r--   0 trevormaseleme   (502) staff       (20)        0 2023-07-22 16:22:36.000000 ldanansi-1.1.1/idanansi/__init__.py
--rw-r--r--   0 trevormaseleme   (502) staff       (20)     5774 2023-07-22 22:59:18.000000 ldanansi-1.1.1/idanansi/blackjack.py
--rw-r--r--   0 trevormaseleme   (502) staff       (20)      317 2023-07-04 08:46:21.000000 ldanansi-1.1.1/idanansi/card.py
--rw-r--r--   0 trevormaseleme   (502) staff       (20)      695 2023-07-22 22:58:47.000000 ldanansi-1.1.1/idanansi/deck.py
--rw-r--r--   0 trevormaseleme   (502) staff       (20)       59 2023-07-22 19:28:29.000000 ldanansi-1.1.1/idanansi/game.py
--rw-r--r--   0 trevormaseleme   (502) staff       (20)     1939 2023-07-22 22:59:06.000000 ldanansi-1.1.1/idanansi/high_low.py
-drwxr-xr-x   0 trevormaseleme   (502) staff       (20)        0 2023-07-22 23:27:27.541309 ldanansi-1.1.1/ldanansi.egg-info/
--rw-r--r--   0 trevormaseleme   (502) staff       (20)      485 2023-07-22 23:27:27.000000 ldanansi-1.1.1/ldanansi.egg-info/PKG-INFO
--rw-r--r--   0 trevormaseleme   (502) staff       (20)      386 2023-07-22 23:27:27.000000 ldanansi-1.1.1/ldanansi.egg-info/SOURCES.txt
--rw-r--r--   0 trevormaseleme   (502) staff       (20)        1 2023-07-22 23:27:27.000000 ldanansi-1.1.1/ldanansi.egg-info/dependency_links.txt
--rw-r--r--   0 trevormaseleme   (502) staff       (20)       15 2023-07-22 23:27:27.000000 ldanansi-1.1.1/ldanansi.egg-info/top_level.txt
--rw-r--r--   0 trevormaseleme   (502) staff       (20)       38 2023-07-22 23:27:27.545861 ldanansi-1.1.1/setup.cfg
--rw-r--r--   0 trevormaseleme   (502) staff       (20)      556 2023-07-22 23:26:58.000000 ldanansi-1.1.1/setup.py
-drwxr-xr-x   0 trevormaseleme   (502) staff       (20)        0 2023-07-22 23:27:27.544615 ldanansi-1.1.1/tests/
--rw-r--r--   0 trevormaseleme   (502) staff       (20)      128 2023-07-04 09:01:41.000000 ldanansi-1.1.1/tests/1_sanity_test.py
--rw-r--r--   0 trevormaseleme   (502) staff       (20)        0 2023-07-03 08:19:40.000000 ldanansi-1.1.1/tests/__init__.py
--rw-r--r--   0 trevormaseleme   (502) staff       (20)      394 2023-07-22 23:13:31.000000 ldanansi-1.1.1/tests/test_blackjack_game.py
--rw-r--r--   0 trevormaseleme   (502) staff       (20)      136 2023-07-04 09:20:40.000000 ldanansi-1.1.1/tests/test_card.py
--rw-r--r--   0 trevormaseleme   (502) staff       (20)     1021 2023-07-22 23:16:26.000000 ldanansi-1.1.1/tests/test_high_low_game.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:47:47.990605 ldanansi-1.1.2/
+-rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-07-23 07:47:35.000000 ldanansi-1.1.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      385 2023-07-23 07:47:47.990605 ldanansi-1.1.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      807 2023-07-23 07:47:35.000000 ldanansi-1.1.2/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:47:47.990605 ldanansi-1.1.2/idanansi/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:47:35.000000 ldanansi-1.1.2/idanansi/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5774 2023-07-23 07:47:35.000000 ldanansi-1.1.2/idanansi/blackjack.py
+-rw-r--r--   0 runner    (1001) docker     (123)      317 2023-07-23 07:47:35.000000 ldanansi-1.1.2/idanansi/card.py
+-rw-r--r--   0 runner    (1001) docker     (123)      695 2023-07-23 07:47:35.000000 ldanansi-1.1.2/idanansi/deck.py
+-rw-r--r--   0 runner    (1001) docker     (123)       59 2023-07-23 07:47:35.000000 ldanansi-1.1.2/idanansi/game.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1939 2023-07-23 07:47:35.000000 ldanansi-1.1.2/idanansi/high_low.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:47:47.990605 ldanansi-1.1.2/ldanansi.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      385 2023-07-23 07:47:47.000000 ldanansi-1.1.2/ldanansi.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      386 2023-07-23 07:47:47.000000 ldanansi-1.1.2/ldanansi.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 07:47:47.000000 ldanansi-1.1.2/ldanansi.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-23 07:47:47.000000 ldanansi-1.1.2/ldanansi.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 07:47:47.990605 ldanansi-1.1.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      503 2023-07-23 07:47:35.000000 ldanansi-1.1.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:47:47.990605 ldanansi-1.1.2/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      128 2023-07-23 07:47:35.000000 ldanansi-1.1.2/tests/1_sanity_test.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:47:35.000000 ldanansi-1.1.2/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      394 2023-07-23 07:47:35.000000 ldanansi-1.1.2/tests/test_blackjack_game.py
+-rw-r--r--   0 runner    (1001) docker     (123)      136 2023-07-23 07:47:35.000000 ldanansi-1.1.2/tests/test_card.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1021 2023-07-23 07:47:35.000000 ldanansi-1.1.2/tests/test_high_low_game.py
```

### Comparing `ldanansi-1.1.1/LICENSE` & `ldanansi-1.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `ldanansi-1.1.1/README.md` & `ldanansi-1.1.2/README.md`

 * *Files identical despite different names*

### Comparing `ldanansi-1.1.1/idanansi/blackjack.py` & `ldanansi-1.1.2/idanansi/blackjack.py`

 * *Files identical despite different names*

### Comparing `ldanansi-1.1.1/idanansi/deck.py` & `ldanansi-1.1.2/idanansi/deck.py`

 * *Files identical despite different names*

### Comparing `ldanansi-1.1.1/idanansi/high_low.py` & `ldanansi-1.1.2/idanansi/high_low.py`

 * *Files identical despite different names*

### Comparing `ldanansi-1.1.1/tests/test_high_low_game.py` & `ldanansi-1.1.2/tests/test_high_low_game.py`

 * *Files identical despite different names*

