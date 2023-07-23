# Comparing `tmp/avclass-malicialab-2.8.6.tar.gz` & `tmp/avclass-malicialab-2.8.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "avclass-malicialab-2.8.6.tar", last modified: Thu Jul 20 13:14:13 2023, max compression
+gzip compressed data, was "avclass-malicialab-2.8.7.tar", last modified: Sun Jul 23 08:27:17 2023, max compression
```

## Comparing `avclass-malicialab-2.8.6.tar` & `avclass-malicialab-2.8.7.tar`

### file list

```diff
@@ -1,26 +1,26 @@
-drwxrwxr-x   0 juanca    (1000) juanca    (1000)        0 2023-07-20 13:14:13.035529 avclass-malicialab-2.8.6/
--rw-rw-r--   0 juanca    (1000) juanca    (1000)     1100 2020-09-01 17:16:19.000000 avclass-malicialab-2.8.6/LICENSE
--rw-rw-r--   0 juanca    (1000) juanca    (1000)       23 2023-02-23 10:39:34.000000 avclass-malicialab-2.8.6/MANIFEST.in
--rw-rw-r--   0 juanca    (1000) juanca    (1000)    17117 2023-07-20 13:14:13.035529 avclass-malicialab-2.8.6/PKG-INFO
--rw-rw-r--   0 juanca    (1000) juanca    (1000)    15317 2023-04-10 14:11:52.000000 avclass-malicialab-2.8.6/README.md
-drwxrwxr-x   0 juanca    (1000) juanca    (1000)        0 2023-07-20 13:14:13.031529 avclass-malicialab-2.8.6/avclass/
--rw-rw-r--   0 juanca    (1000) juanca    (1000)      401 2023-02-23 10:09:56.000000 avclass-malicialab-2.8.6/avclass/__init__.py
--rw-rw-r--   0 juanca    (1000) juanca    (1000)    20596 2023-05-05 15:16:06.000000 avclass-malicialab-2.8.6/avclass/common.py
-drwxrwxr-x   0 juanca    (1000) juanca    (1000)        0 2023-07-20 13:14:13.031529 avclass-malicialab-2.8.6/avclass/data/
--rw-rw-r--   0 juanca    (1000) juanca    (1000)     6823 2023-02-23 10:09:56.000000 avclass-malicialab-2.8.6/avclass/data/andropup.expansion
--rw-rw-r--   0 juanca    (1000) juanca    (1000)      308 2023-07-20 10:20:10.000000 avclass-malicialab-2.8.6/avclass/data/default.expansion
--rw-rw-r--   0 juanca    (1000) juanca    (1000)    56730 2023-07-20 13:12:59.000000 avclass-malicialab-2.8.6/avclass/data/default.tagging
--rw-rw-r--   0 juanca    (1000) juanca    (1000)    41678 2023-07-20 13:12:59.000000 avclass-malicialab-2.8.6/avclass/data/default.taxonomy
--rwxrwxr-x   0 juanca    (1000) juanca    (1000)     4202 2023-02-26 07:44:35.000000 avclass-malicialab-2.8.6/avclass/evaluate.py
--rwxrwxr-x   0 juanca    (1000) juanca    (1000)    23609 2023-05-26 13:02:48.000000 avclass-malicialab-2.8.6/avclass/labeler.py
--rwxrwxr-x   0 juanca    (1000) juanca    (1000)     3996 2023-03-04 13:05:26.000000 avclass-malicialab-2.8.6/avclass/misp.py
--rwxrwxr-x   0 juanca    (1000) juanca    (1000)     1704 2023-02-26 07:00:49.000000 avclass-malicialab-2.8.6/avclass/normalize.py
--rwxrwxr-x   0 juanca    (1000) juanca    (1000)    17636 2023-02-23 10:26:36.000000 avclass-malicialab-2.8.6/avclass/update.py
-drwxrwxr-x   0 juanca    (1000) juanca    (1000)        0 2023-07-20 13:14:13.035529 avclass-malicialab-2.8.6/avclass_malicialab.egg-info/
--rw-rw-r--   0 juanca    (1000) juanca    (1000)    17117 2023-07-20 13:14:13.000000 avclass-malicialab-2.8.6/avclass_malicialab.egg-info/PKG-INFO
--rw-rw-r--   0 juanca    (1000) juanca    (1000)      511 2023-07-20 13:14:13.000000 avclass-malicialab-2.8.6/avclass_malicialab.egg-info/SOURCES.txt
--rw-rw-r--   0 juanca    (1000) juanca    (1000)        1 2023-07-20 13:14:13.000000 avclass-malicialab-2.8.6/avclass_malicialab.egg-info/dependency_links.txt
--rw-rw-r--   0 juanca    (1000) juanca    (1000)      162 2023-07-20 13:14:13.000000 avclass-malicialab-2.8.6/avclass_malicialab.egg-info/entry_points.txt
--rw-rw-r--   0 juanca    (1000) juanca    (1000)        8 2023-07-20 13:14:13.000000 avclass-malicialab-2.8.6/avclass_malicialab.egg-info/top_level.txt
--rw-rw-r--   0 juanca    (1000) juanca    (1000)      831 2023-07-20 13:13:46.000000 avclass-malicialab-2.8.6/pyproject.toml
--rw-rw-r--   0 juanca    (1000) juanca    (1000)       38 2023-07-20 13:14:13.035529 avclass-malicialab-2.8.6/setup.cfg
+drwxrwxr-x   0 juanca    (1000) juanca    (1000)        0 2023-07-23 08:27:17.977305 avclass-malicialab-2.8.7/
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)     1100 2020-09-01 17:16:19.000000 avclass-malicialab-2.8.7/LICENSE
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)       23 2023-02-23 10:39:34.000000 avclass-malicialab-2.8.7/MANIFEST.in
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)    17117 2023-07-23 08:27:17.977305 avclass-malicialab-2.8.7/PKG-INFO
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)    15317 2023-04-10 14:11:52.000000 avclass-malicialab-2.8.7/README.md
+drwxrwxr-x   0 juanca    (1000) juanca    (1000)        0 2023-07-23 08:27:17.977305 avclass-malicialab-2.8.7/avclass/
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)      401 2023-02-23 10:09:56.000000 avclass-malicialab-2.8.7/avclass/__init__.py
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)    20596 2023-05-05 15:16:06.000000 avclass-malicialab-2.8.7/avclass/common.py
+drwxrwxr-x   0 juanca    (1000) juanca    (1000)        0 2023-07-23 08:27:17.977305 avclass-malicialab-2.8.7/avclass/data/
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)     6823 2023-02-23 10:09:56.000000 avclass-malicialab-2.8.7/avclass/data/andropup.expansion
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)      308 2023-07-20 10:20:10.000000 avclass-malicialab-2.8.7/avclass/data/default.expansion
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)    56816 2023-07-23 08:23:32.000000 avclass-malicialab-2.8.7/avclass/data/default.tagging
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)    41799 2023-07-23 08:23:32.000000 avclass-malicialab-2.8.7/avclass/data/default.taxonomy
+-rwxrwxr-x   0 juanca    (1000) juanca    (1000)     4202 2023-02-26 07:44:35.000000 avclass-malicialab-2.8.7/avclass/evaluate.py
+-rwxrwxr-x   0 juanca    (1000) juanca    (1000)    23609 2023-05-26 13:02:48.000000 avclass-malicialab-2.8.7/avclass/labeler.py
+-rwxrwxr-x   0 juanca    (1000) juanca    (1000)     3996 2023-03-04 13:05:26.000000 avclass-malicialab-2.8.7/avclass/misp.py
+-rwxrwxr-x   0 juanca    (1000) juanca    (1000)     1704 2023-02-26 07:00:49.000000 avclass-malicialab-2.8.7/avclass/normalize.py
+-rwxrwxr-x   0 juanca    (1000) juanca    (1000)    17636 2023-02-23 10:26:36.000000 avclass-malicialab-2.8.7/avclass/update.py
+drwxrwxr-x   0 juanca    (1000) juanca    (1000)        0 2023-07-23 08:27:17.977305 avclass-malicialab-2.8.7/avclass_malicialab.egg-info/
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)    17117 2023-07-23 08:27:17.000000 avclass-malicialab-2.8.7/avclass_malicialab.egg-info/PKG-INFO
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)      511 2023-07-23 08:27:17.000000 avclass-malicialab-2.8.7/avclass_malicialab.egg-info/SOURCES.txt
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)        1 2023-07-23 08:27:17.000000 avclass-malicialab-2.8.7/avclass_malicialab.egg-info/dependency_links.txt
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)      162 2023-07-23 08:27:17.000000 avclass-malicialab-2.8.7/avclass_malicialab.egg-info/entry_points.txt
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)        8 2023-07-23 08:27:17.000000 avclass-malicialab-2.8.7/avclass_malicialab.egg-info/top_level.txt
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)      831 2023-07-23 08:26:29.000000 avclass-malicialab-2.8.7/pyproject.toml
+-rw-rw-r--   0 juanca    (1000) juanca    (1000)       38 2023-07-23 08:27:17.977305 avclass-malicialab-2.8.7/setup.cfg
```

### Comparing `avclass-malicialab-2.8.6/LICENSE` & `avclass-malicialab-2.8.7/LICENSE`

 * *Files identical despite different names*

### Comparing `avclass-malicialab-2.8.6/PKG-INFO` & `avclass-malicialab-2.8.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: avclass-malicialab
-Version: 2.8.6
+Version: 2.8.7
 Summary: AVClass is a Python package and command line tool to tag / label malware samples.
 Author: MaliciaLab
 License: MIT License
         
         Copyright (c) 2016-2020 MaliciaLab @ IMDEA Software Institute
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `avclass-malicialab-2.8.6/README.md` & `avclass-malicialab-2.8.7/README.md`

 * *Files identical despite different names*

### Comparing `avclass-malicialab-2.8.6/avclass/common.py` & `avclass-malicialab-2.8.7/avclass/common.py`

 * *Files identical despite different names*

### Comparing `avclass-malicialab-2.8.6/avclass/data/andropup.expansion` & `avclass-malicialab-2.8.7/avclass/data/andropup.expansion`

 * *Files identical despite different names*

### Comparing `avclass-malicialab-2.8.6/avclass/data/default.tagging` & `avclass-malicialab-2.8.7/avclass/data/default.tagging`

 * *Files 1% similar despite different names*

```diff
@@ -1673,14 +1673,15 @@
 mairu	mailru
 maklt	renos
 maktub	maktublocker
 malcrypt	packed
 malhome	updtkiller
 maliciousmacro	macro
 maligarnet	tpyn
+maljava	exploit	java
 mallocker	lockscreen
 malob	packed
 malpack	packed
 malpe	corrupted
 mambretor	dcryptor
 manalo	laroux
 mandagore	mandragore
@@ -2569,15 +2570,17 @@
 smssilence	smscatch
 smsstealer	smsspy
 smthief	smsthief
 smtp	spam
 snadapps	typstu
 snafes	synack
 snail	winemmem
+snakekeylogger	snakelogger
 snakeransom	snake
+snakestealer	snakelogger
 snapdo	linkury
 snara	snarasite
 snare	snarasite
 sndapps	typstu
 sneakytrail	installerex
 sniffer	network
 snipsmart	browsefox
@@ -3035,14 +3038,15 @@
 webbora	kraddare
 webcake	browsefox
 webdial	webdialer
 webget	browsefox
 webhook	fasong
 webnav	webnavigator
 webnavigatorbrowser	webnavigator
+webpage	html
 webpick	installerex
 websearch	search
 webtoolbar	toolbar
 webus	robobot
 wedownload	soft32downloader
 weecnaw	netwiredrc
 weenloc	lockscreen
```

### Comparing `avclass-malicialab-2.8.6/avclass/data/default.taxonomy` & `avclass-malicialab-2.8.7/avclass/data/default.taxonomy`

 * *Files 0% similar despite different names*

```diff
@@ -2364,15 +2364,15 @@
 FAM:smspay
 FAM:smsreg
 FAM:smssend
 FAM:smsspy
 FAM:smsthief
 FAM:smszombie
 FAM:snake
-FAM:snakekeylogger
+FAM:snakelogger
 FAM:snaptube
 FAM:snarasite
 FAM:snatch
 FAM:sneepy
 FAM:snifula
 FAM:snojan
 FAM:sobig
@@ -2778,14 +2778,15 @@
 FAM:weiduan
 FAM:wellmess
 FAM:werly
 FAM:westbyte
 FAM:westeal
 FAM:wfpdisabler
 FAM:whenu
+FAM:whispergate
 FAM:whistlesoftware
 FAM:whiteice
 FAM:whitesmoke
 FAM:widdit
 FAM:wificrack
 FAM:wifikill
 FAM:wildneutron
@@ -3027,14 +3028,15 @@
 FILE:packed:nakedpack
 FILE:packed:niceprotect
 FILE:packed:noobyprotect
 FILE:packed:npack
 FILE:packed:nspack
 FILE:packed:obfuscapk
 FILE:packed:obsidium
+FILE:packed:opack
 FILE:packed:orien
 FILE:packed:packman
 FILE:packed:packz
 FILE:packed:pearmor
 FILE:packed:pecompact
 FILE:packed:pecrypt
 FILE:packed:pelock
@@ -3076,15 +3078,14 @@
 FILE:proglang:visualbasic:vbscript
 FILE:shellcode
 FILE:signed
 FILE:signed:fakepublisher
 FILE:signed:invalidcert
 FILE:small
 FILE:testvirus
-FILE:webpage
 GEN:abuse
 GEN:access
 GEN:advml
 GEN:agen
 GEN:apk
 GEN:appl
 GEN:application
@@ -3148,28 +3149,33 @@
 GEN:genome
 GEN:hack
 GEN:heur
 GEN:heuristic
 GEN:high
 GEN:highconfidence
 GEN:igeneric
+GEN:infected
+GEN:insight
 GEN:kcloud
 GEN:load
 GEN:lookslike
+GEN:lowprevalence
 GEN:malagent
 GEN:malcode
 GEN:maldroid
 GEN:malicious
+GEN:maltraffic
 GEN:maltrec
 GEN:malware
 GEN:memscan
 GEN:mlwr
 GEN:moderate
 GEN:multi
 GEN:multiple
+GEN:name
 GEN:normal
 GEN:notsuspicious
 GEN:onion
 GEN:optional
 GEN:other
 GEN:password
 GEN:posible
@@ -3187,26 +3193,29 @@
 GEN:securityrisk
 GEN:siggen
 GEN:singleton
 GEN:software
 GEN:sonar
 GEN:static
 GEN:susp
+GEN:suspbeh
 GEN:suspect
 GEN:suspectcrc
 GEN:suspected
 GEN:suspic
 GEN:suspicious
 GEN:symvt
 GEN:systemhijack
 GEN:threat
+GEN:trafic
 GEN:trojan
 GEN:tscope
 GEN:tsgeneric
 GEN:unavailable
 GEN:unclassified
 GEN:unclassifiedmalware
 GEN:undef
 GEN:undefined
 GEN:unknown
+GEN:unproven
 GEN:variant
 GEN:website
```

### Comparing `avclass-malicialab-2.8.6/avclass/evaluate.py` & `avclass-malicialab-2.8.7/avclass/evaluate.py`

 * *Files identical despite different names*

### Comparing `avclass-malicialab-2.8.6/avclass/labeler.py` & `avclass-malicialab-2.8.7/avclass/labeler.py`

 * *Files identical despite different names*

### Comparing `avclass-malicialab-2.8.6/avclass/misp.py` & `avclass-malicialab-2.8.7/avclass/misp.py`

 * *Files identical despite different names*

### Comparing `avclass-malicialab-2.8.6/avclass/normalize.py` & `avclass-malicialab-2.8.7/avclass/normalize.py`

 * *Files identical despite different names*

### Comparing `avclass-malicialab-2.8.6/avclass/update.py` & `avclass-malicialab-2.8.7/avclass/update.py`

 * *Files identical despite different names*

### Comparing `avclass-malicialab-2.8.6/avclass_malicialab.egg-info/PKG-INFO` & `avclass-malicialab-2.8.7/avclass_malicialab.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: avclass-malicialab
-Version: 2.8.6
+Version: 2.8.7
 Summary: AVClass is a Python package and command line tool to tag / label malware samples.
 Author: MaliciaLab
 License: MIT License
         
         Copyright (c) 2016-2020 MaliciaLab @ IMDEA Software Institute
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `avclass-malicialab-2.8.6/pyproject.toml` & `avclass-malicialab-2.8.7/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "avclass-malicialab"
-version = "2.8.6"
+version = "2.8.7"
 description = "AVClass is a Python package and command line tool to tag / label malware samples."
 readme = "README.md"
 authors = [{ name = "MaliciaLab" }]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
```

