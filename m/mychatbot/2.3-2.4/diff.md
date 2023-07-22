# Comparing `tmp/mychatbot-2.3.tar.gz` & `tmp/mychatbot-2.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mychatbot-2.3.tar", last modified: Sat Jul 22 22:57:50 2023, max compression
+gzip compressed data, was "mychatbot-2.4.tar", last modified: Sat Jul 22 23:07:31 2023, max compression
```

## Comparing `mychatbot-2.3.tar` & `mychatbot-2.4.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 22:57:50.916752 mychatbot-2.3/
--rw-r--r--   0 kunal      (501) staff       (20)       51 2023-07-22 22:57:50.916636 mychatbot-2.3/PKG-INFO
-drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 22:57:50.915708 mychatbot-2.3/mychatbot/
--rw-r--r--   0 kunal      (501) staff       (20)        0 2023-07-22 19:42:40.000000 mychatbot-2.3/mychatbot/__init__.py
--rw-r--r--   0 kunal      (501) staff       (20)     1410 2023-07-22 22:52:32.000000 mychatbot-2.3/mychatbot/ai.py
-drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 22:57:50.916461 mychatbot-2.3/mychatbot.egg-info/
--rw-r--r--   0 kunal      (501) staff       (20)       51 2023-07-22 22:57:50.000000 mychatbot-2.3/mychatbot.egg-info/PKG-INFO
--rw-r--r--   0 kunal      (501) staff       (20)      210 2023-07-22 22:57:50.000000 mychatbot-2.3/mychatbot.egg-info/SOURCES.txt
--rw-r--r--   0 kunal      (501) staff       (20)        1 2023-07-22 22:57:50.000000 mychatbot-2.3/mychatbot.egg-info/dependency_links.txt
--rw-r--r--   0 kunal      (501) staff       (20)        8 2023-07-22 22:57:50.000000 mychatbot-2.3/mychatbot.egg-info/requires.txt
--rw-r--r--   0 kunal      (501) staff       (20)       10 2023-07-22 22:57:50.000000 mychatbot-2.3/mychatbot.egg-info/top_level.txt
--rw-r--r--   0 kunal      (501) staff       (20)       38 2023-07-22 22:57:50.916788 mychatbot-2.3/setup.cfg
--rw-r--r--   0 kunal      (501) staff       (20)      185 2023-07-22 22:57:33.000000 mychatbot-2.3/setup.py
+drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 23:07:31.091549 mychatbot-2.4/
+-rw-r--r--   0 kunal      (501) staff       (20)       51 2023-07-22 23:07:31.091424 mychatbot-2.4/PKG-INFO
+drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 23:07:31.090491 mychatbot-2.4/mychatbot/
+-rw-r--r--   0 kunal      (501) staff       (20)        0 2023-07-22 19:42:40.000000 mychatbot-2.4/mychatbot/__init__.py
+-rw-r--r--   0 kunal      (501) staff       (20)     1411 2023-07-22 23:07:11.000000 mychatbot-2.4/mychatbot/ai.py
+drwxr-xr-x   0 kunal      (501) staff       (20)        0 2023-07-22 23:07:31.091247 mychatbot-2.4/mychatbot.egg-info/
+-rw-r--r--   0 kunal      (501) staff       (20)       51 2023-07-22 23:07:31.000000 mychatbot-2.4/mychatbot.egg-info/PKG-INFO
+-rw-r--r--   0 kunal      (501) staff       (20)      210 2023-07-22 23:07:31.000000 mychatbot-2.4/mychatbot.egg-info/SOURCES.txt
+-rw-r--r--   0 kunal      (501) staff       (20)        1 2023-07-22 23:07:31.000000 mychatbot-2.4/mychatbot.egg-info/dependency_links.txt
+-rw-r--r--   0 kunal      (501) staff       (20)        8 2023-07-22 23:07:31.000000 mychatbot-2.4/mychatbot.egg-info/requires.txt
+-rw-r--r--   0 kunal      (501) staff       (20)       10 2023-07-22 23:07:31.000000 mychatbot-2.4/mychatbot.egg-info/top_level.txt
+-rw-r--r--   0 kunal      (501) staff       (20)       38 2023-07-22 23:07:31.091588 mychatbot-2.4/setup.cfg
+-rw-r--r--   0 kunal      (501) staff       (20)      185 2023-07-22 23:06:59.000000 mychatbot-2.4/setup.py
```

### Comparing `mychatbot-2.3/mychatbot/ai.py` & `mychatbot-2.4/mychatbot/ai.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,16 +3,16 @@
 token = "YQiLtpIxwMX_V3gqKce011fmUyY9L_KCvlyUITEhuhTLUa7RmNPGUwC8ta-nvEhwfuOi6A."
 
 def print_banner():
     banner_text = r"""
    __  __         ___ _         _     ___      _                                       
  |  \/  |_  _   / __| |_  __ _| |_  | _ ) ___| |_                                     
  | |\/| | || | | (__| ' \/ _` |  _| | _ \/ _ \  _|                                    
- |_|  |_|\_, |  \___|_||_\__,_|\__| |___/\___/\__|                                    
-         |__/              ___        _ _____    ___             _  __              _ 
+ |_|  |_|__, |  \___|_||_\__,_|\__| |___/\___/\__|                                    
+         |___/              ___        _ _____    ___             _  __              _ 
                           | _ )_  _  (_)_   _|  / __|_  _ _  _  | |/ /  _ _ _  __ _| |
                           | _ \ || | | | | |   | (_ | || | || | | ' < || | ' \/ _` | |
                           |___/\_, | |_| |_|    \___|\_,_|\_, | |_|\_\_,_|_||_\__,_|_|
                                |__/                       |__/                        
     """
     print("\033[1m" + banner_text + "\033[0m")
```

