# Comparing `tmp/pyntweb-0.2.8.tar.gz` & `tmp/pyntweb-0.2.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyntweb-0.2.8.tar", last modified: Sat Jul 22 13:20:08 2023, max compression
+gzip compressed data, was "pyntweb-0.2.9.tar", last modified: Sat Jul 22 13:50:37 2023, max compression
```

## Comparing `pyntweb-0.2.8.tar` & `pyntweb-0.2.9.tar`

### file list

```diff
@@ -1,33 +1,33 @@
-drwxr-xr-x   0 mrybs     (1000) mrybs     (1000)        0 2023-07-22 13:20:08.955130 pyntweb-0.2.8/
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)    35149 2023-07-21 15:15:13.000000 pyntweb-0.2.8/LICENSE
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      677 2023-07-22 13:20:08.955130 pyntweb-0.2.8/PKG-INFO
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      550 2023-07-21 15:15:13.000000 pyntweb-0.2.8/README.md
-drwxr-xr-x   0 mrybs     (1000) mrybs     (1000)        0 2023-07-22 13:20:08.951797 pyntweb-0.2.8/ntcss/
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      208 2023-07-21 15:15:13.000000 pyntweb-0.2.8/ntcss/__init__.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)       24 2023-07-21 15:15:13.000000 pyntweb-0.2.8/ntcss/const.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)     5462 2023-07-21 15:15:13.000000 pyntweb-0.2.8/ntcss/ntml_parser.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      467 2023-07-21 15:15:13.000000 pyntweb-0.2.8/ntcss/ntmlc.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)    13667 2023-07-21 15:15:13.000000 pyntweb-0.2.8/ntcss/tran.py
-drwxr-xr-x   0 mrybs     (1000) mrybs     (1000)        0 2023-07-22 13:20:08.951797 pyntweb-0.2.8/ntml/
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      208 2023-07-21 15:15:13.000000 pyntweb-0.2.8/ntml/__init__.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)       24 2023-07-21 15:15:13.000000 pyntweb-0.2.8/ntml/const.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)     2561 2023-07-21 15:15:13.000000 pyntweb-0.2.8/ntml/errors.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)     5670 2023-07-22 13:19:37.000000 pyntweb-0.2.8/ntml/ntml_parser.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      467 2023-07-21 15:15:13.000000 pyntweb-0.2.8/ntml/ntmlc.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)    13738 2023-07-21 20:03:45.000000 pyntweb-0.2.8/ntml/tran.py
-drwxr-xr-x   0 mrybs     (1000) mrybs     (1000)        0 2023-07-22 13:20:08.955130 pyntweb-0.2.8/pyntweb.egg-info/
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      677 2023-07-22 13:20:08.000000 pyntweb-0.2.8/pyntweb.egg-info/PKG-INFO
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      500 2023-07-22 13:20:08.000000 pyntweb-0.2.8/pyntweb.egg-info/SOURCES.txt
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)        1 2023-07-22 13:20:08.000000 pyntweb-0.2.8/pyntweb.egg-info/dependency_links.txt
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)        1 2023-07-21 15:18:26.000000 pyntweb-0.2.8/pyntweb.egg-info/not-zip-safe
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)       18 2023-07-22 13:20:08.000000 pyntweb-0.2.8/pyntweb.egg-info/requires.txt
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)       20 2023-07-22 13:20:08.000000 pyntweb-0.2.8/pyntweb.egg-info/top_level.txt
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      784 2023-07-22 13:20:05.000000 pyntweb-0.2.8/pyproject.toml
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)       38 2023-07-22 13:20:08.955130 pyntweb-0.2.8/setup.cfg
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      869 2023-07-22 13:20:03.000000 pyntweb-0.2.8/setup.py
-drwxr-xr-x   0 mrybs     (1000) mrybs     (1000)        0 2023-07-22 13:20:08.955130 pyntweb-0.2.8/webfalco/
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      228 2023-07-21 15:15:13.000000 pyntweb-0.2.8/webfalco/__init__.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)       24 2023-07-21 15:15:13.000000 pyntweb-0.2.8/webfalco/const.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)     5524 2023-07-21 15:15:13.000000 pyntweb-0.2.8/webfalco/lrparser.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)    13667 2023-07-21 15:15:13.000000 pyntweb-0.2.8/webfalco/tran.py
--rw-r--r--   0 mrybs     (1000) mrybs     (1000)      467 2023-07-21 15:15:13.000000 pyntweb-0.2.8/webfalco/webfalcoc.py
+drwxr-xr-x   0 mrybs     (1000) mrybs     (1000)        0 2023-07-22 13:50:37.276384 pyntweb-0.2.9/
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)    35149 2023-07-21 15:15:13.000000 pyntweb-0.2.9/LICENSE
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      677 2023-07-22 13:50:37.276384 pyntweb-0.2.9/PKG-INFO
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      550 2023-07-21 15:15:13.000000 pyntweb-0.2.9/README.md
+drwxr-xr-x   0 mrybs     (1000) mrybs     (1000)        0 2023-07-22 13:50:37.273051 pyntweb-0.2.9/ntcss/
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      208 2023-07-21 15:15:13.000000 pyntweb-0.2.9/ntcss/__init__.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)       24 2023-07-21 15:15:13.000000 pyntweb-0.2.9/ntcss/const.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)     5462 2023-07-21 15:15:13.000000 pyntweb-0.2.9/ntcss/ntml_parser.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      467 2023-07-21 15:15:13.000000 pyntweb-0.2.9/ntcss/ntmlc.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)    13667 2023-07-21 15:15:13.000000 pyntweb-0.2.9/ntcss/tran.py
+drwxr-xr-x   0 mrybs     (1000) mrybs     (1000)        0 2023-07-22 13:50:37.276384 pyntweb-0.2.9/ntml/
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      208 2023-07-21 15:15:13.000000 pyntweb-0.2.9/ntml/__init__.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)       24 2023-07-21 15:15:13.000000 pyntweb-0.2.9/ntml/const.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)     2561 2023-07-21 15:15:13.000000 pyntweb-0.2.9/ntml/errors.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)     5670 2023-07-22 13:19:37.000000 pyntweb-0.2.9/ntml/ntml_parser.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      467 2023-07-21 15:15:13.000000 pyntweb-0.2.9/ntml/ntmlc.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)    14994 2023-07-22 13:49:32.000000 pyntweb-0.2.9/ntml/tran.py
+drwxr-xr-x   0 mrybs     (1000) mrybs     (1000)        0 2023-07-22 13:50:37.276384 pyntweb-0.2.9/pyntweb.egg-info/
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      677 2023-07-22 13:50:37.000000 pyntweb-0.2.9/pyntweb.egg-info/PKG-INFO
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      500 2023-07-22 13:50:37.000000 pyntweb-0.2.9/pyntweb.egg-info/SOURCES.txt
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)        1 2023-07-22 13:50:37.000000 pyntweb-0.2.9/pyntweb.egg-info/dependency_links.txt
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)        1 2023-07-21 15:18:26.000000 pyntweb-0.2.9/pyntweb.egg-info/not-zip-safe
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)       18 2023-07-22 13:50:37.000000 pyntweb-0.2.9/pyntweb.egg-info/requires.txt
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)       20 2023-07-22 13:50:37.000000 pyntweb-0.2.9/pyntweb.egg-info/top_level.txt
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      784 2023-07-22 13:28:45.000000 pyntweb-0.2.9/pyproject.toml
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)       38 2023-07-22 13:50:37.276384 pyntweb-0.2.9/setup.cfg
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      869 2023-07-22 13:28:42.000000 pyntweb-0.2.9/setup.py
+drwxr-xr-x   0 mrybs     (1000) mrybs     (1000)        0 2023-07-22 13:50:37.276384 pyntweb-0.2.9/webfalco/
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      228 2023-07-21 15:15:13.000000 pyntweb-0.2.9/webfalco/__init__.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)       24 2023-07-21 15:15:13.000000 pyntweb-0.2.9/webfalco/const.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)     5524 2023-07-21 15:15:13.000000 pyntweb-0.2.9/webfalco/lrparser.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)    13667 2023-07-21 15:15:13.000000 pyntweb-0.2.9/webfalco/tran.py
+-rw-r--r--   0 mrybs     (1000) mrybs     (1000)      467 2023-07-21 15:15:13.000000 pyntweb-0.2.9/webfalco/webfalcoc.py
```

### Comparing `pyntweb-0.2.8/LICENSE` & `pyntweb-0.2.9/LICENSE`

 * *Files identical despite different names*

### Comparing `pyntweb-0.2.8/PKG-INFO` & `pyntweb-0.2.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,7 +1,7 @@
 Metadata-Version: 2.1
 Name: pyntweb
-Version: 0.2.8
+Version: 0.2.9
 Summary: NTWeb - это экосистема компиляторов, которая планирует прийти на замену существующим в web стандартам: HTML, CSS, JS. На данный момент код на её языках переводится в традиционные языки web, так же традиционные языки нативно поддерживаются в самом кодеПосесите оффициальную группу проекта: https://t.me/+ft6pYhYcqtk3NDdi
 Author-email: talismanchet@vk.com
 License: GNU GPL 3.0
 License-File: LICENSE
```

### Comparing `pyntweb-0.2.8/README.md` & `pyntweb-0.2.9/README.md`

 * *Files identical despite different names*

### Comparing `pyntweb-0.2.8/ntcss/ntml_parser.py` & `pyntweb-0.2.9/ntcss/ntml_parser.py`

 * *Files identical despite different names*

### Comparing `pyntweb-0.2.8/ntcss/tran.py` & `pyntweb-0.2.9/ntcss/tran.py`

 * *Files identical despite different names*

### Comparing `pyntweb-0.2.8/ntml/errors.py` & `pyntweb-0.2.9/ntml/errors.py`

 * *Files identical despite different names*

### Comparing `pyntweb-0.2.8/ntml/ntml_parser.py` & `pyntweb-0.2.9/ntml/ntml_parser.py`

 * *Files identical despite different names*

### Comparing `pyntweb-0.2.8/ntml/tran.py` & `pyntweb-0.2.9/webfalco/tran.py`

 * *Files 1% similar despite different names*

```diff
@@ -76,16 +76,14 @@
     "hld":       {"tag": "div"},
     "ulist":     {"tag": "ul"},
     "ul":        {"tag": "ul"},
     "olist":     {"tag": "ol"},
     "ol":        {"tag": "ol"},
     "item":      {"tag": "li"},
     "li":        {"tag": "li"},
-    "select":    {"tag": "select"},
-    "option":    {"tag": "option"}
 }
 
 
 class Meta:
     """
     Class for storing meta data
     """
```

### Comparing `pyntweb-0.2.8/pyntweb.egg-info/PKG-INFO` & `pyntweb-0.2.9/pyntweb.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,7 +1,7 @@
 Metadata-Version: 2.1
 Name: pyntweb
-Version: 0.2.8
+Version: 0.2.9
 Summary: NTWeb - это экосистема компиляторов, которая планирует прийти на замену существующим в web стандартам: HTML, CSS, JS. На данный момент код на её языках переводится в традиционные языки web, так же традиционные языки нативно поддерживаются в самом кодеПосесите оффициальную группу проекта: https://t.me/+ft6pYhYcqtk3NDdi
 Author-email: talismanchet@vk.com
 License: GNU GPL 3.0
 License-File: LICENSE
```

### Comparing `pyntweb-0.2.8/pyproject.toml` & `pyntweb-0.2.9/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "pyntweb"
-version = "0.2.8"
+version = "0.2.9"
 description = "NTWeb - это экосистема компиляторов, которая планирует прийти на замену существующим в web стандартам: HTML, CSS, JS. На данный момент код на её языках переводится в традиционные языки web, так же традиционные языки нативно поддерживаются в самом коде."
 authors = ["Talisman Chet <talismanchet@vk.com>"]
 license = "GNU GPL 3.0"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.10"
```

### Comparing `pyntweb-0.2.8/setup.py` & `pyntweb-0.2.9/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 """
 setup.py
 """
 
 from setuptools import setup
 
 setup(name='pyntweb',
-      version='0.2.8',
+      version='0.2.9',
       description='''
 NTWeb - это экосистема компиляторов, которая планирует прийти на замену существующим в web стандартам: 
 HTML, CSS, JS. На данный момент код на её языках переводится в традиционные языки web, так же 
 традиционные языки нативно поддерживаются в самом коде
 
 Посесите оффициальную группу проекта: https://t.me/+ft6pYhYcqtk3NDdi'''.replace("\n", ""),
       packages=['ntml', 'webfalco', 'ntcss'],
```

### Comparing `pyntweb-0.2.8/webfalco/lrparser.py` & `pyntweb-0.2.9/webfalco/lrparser.py`

 * *Files identical despite different names*

### Comparing `pyntweb-0.2.8/webfalco/tran.py` & `pyntweb-0.2.9/ntml/tran.py`

 * *Files 5% similar despite different names*

```diff
@@ -29,61 +29,95 @@
 rels: dict = {
     "style": "stylesheet",
     "favicon": "icon",
     "script": "script"
 }
 
 meals: dict = {
-    "body":      {"tag": "body"},
-    "bold":      {"tag": "b"},
-    "b":         {"tag": "b"},
-    "italic":    {"tag": "i"},
-    "i":         {"tag": "i"},
-    "underline": {"tag": "u"},
-    "u":         {"tag": "u"},
-    "strikeout": {"tag": "s"},
-    "s":         {"tag": "s"},
-    "block":     {"tag": "div"},
-    "bl":        {"tag": "div"},
-    "text":      {"tag": "p"},
-    "t":         {"tag": "p"},
-    "input":     {"tag": "input"},
-    "inp":       {"tag": "input"},
-    "h1":        {"tag": "h1"},
-    "h2":        {"tag": "h2"},
-    "h3":        {"tag": "h3"},
-    "h4":        {"tag": "h4"},
-    "ht1":       {"tag": "h1"},
-    "ht2":       {"tag": "h2"},
-    "ht3":       {"tag": "h3"},
-    "ht4":       {"tag": "h4"},
-    "link":      {"tag": "a"},
-    "ln":        {"tag": "a"},
-    "image":     {"tag": "image"},
-    "img":       {"tag": "image"},
-    "cd":        {"tag": "div"},
-    "code":      {"tag": "div"},
-    "form":      {"tag": "form"},
-    "f":         {"tag": "form"},
-    "table":     {"tag": "table"},
-    "tab":       {"tag": "table"},
-    "tr":        {"tag": "tr"},
-    "td":        {"tag": "td"},
-    "script":    {"tag": "script"},
-    "scr":       {"tag": "script"},
-    "btn":       {"tag": "button"},
-    "button":    {"tag": "button"},
-    "holder":    {"tag": "div"},
-    "hld":       {"tag": "div"},
-    "ulist":     {"tag": "ul"},
-    "ul":        {"tag": "ul"},
-    "olist":     {"tag": "ol"},
-    "ol":        {"tag": "ol"},
-    "item":      {"tag": "li"},
-    "li":        {"tag": "li"},
+    "body":       {"tag": "body"},
+    "bold":       {"tag": "b"},
+    "b":          {"tag": "b"},
+    "italic":     {"tag": "i"},
+    "i":          {"tag": "i"},
+    "underline":  {"tag": "u"},
+    "u":          {"tag": "u"},
+    "strikeout":  {"tag": "s"},
+    "s":          {"tag": "s"},
+    "block":      {"tag": "div"},
+    "bl":         {"tag": "div"},
+    "text":       {"tag": "p"},
+    "t":          {"tag": "p"},
+    "sub":        {"tag": "sub"},
+    "sup":        {"tag": "sup"},
+    "super":      {"tag": "super"},
+    "textbox":    {"tag": "textbox"},
+    "input":      {"tag": "input"},
+    "inp":        {"tag": "input"},
+    "textarea":   {"text": "textarea"},
+    "h1":         {"tag": "h1"},
+    "h2":         {"tag": "h2"},
+    "h3":         {"tag": "h3"},
+    "h4":         {"tag": "h4"},
+    "ht1":        {"tag": "h1"},
+    "ht2":        {"tag": "h2"},
+    "ht3":        {"tag": "h3"},
+    "ht4":        {"tag": "h4"},
+    "link":       {"tag": "a"},
+    "ln":         {"tag": "a"},
+    "image":      {"tag": "image"},
+    "img":        {"tag": "image"},
+    "cd":         {"tag": "div"},
+    "code":       {"tag": "div"},
+    "form":       {"tag": "form"},
+    "f":          {"tag": "form"},
+    "table":      {"tag": "table"},
+    "tab":        {"tag": "table"},
+    "tr":         {"tag": "tr"},
+    "td":         {"tag": "td"},
+    "script":     {"tag": "script"},
+    "scr":        {"tag": "script"},
+    "btn":        {"tag": "button"},
+    "button":     {"tag": "button"},
+    "holder":     {"tag": "div"},
+    "hld":        {"tag": "div"},
+    "ulist":      {"tag": "ul"},
+    "ul":         {"tag": "ul"},
+    "olist":      {"tag": "ol"},
+    "ol":         {"tag": "ol"},
+    "item":       {"tag": "li"},
+    "li":         {"tag": "li"},
+    "select":     {"tag": "select"},
+    "optiongroup":{"tag": "optgroup"}
+    "option":     {"tag": "option"},
+    "canvas":     {"tag": "canvas"},
+    "wrapper":    {"tag": "wrapper", "props": {"styles": "display: block;"}},
+    "audio":      {"tag": "audio"},
+    "music":      {"tag": "audio"},
+    "sound":      {"tag": "audio"},
+    "video":      {"tag": "video"},
+    "track":      {"tag": "track"}
+    "mediatrack": {"tag": "track"},
+    "details":    {"tag": "details"},
+    "summary":    {"tag": "summary"},
+    "figure":     {"tag": "figure"},
+    "header":     {"tag": "header"},
+    "footer":     {"tag": "footer"},
+    "insert":     {"tag": "ins"},
+    "label":      {"tag": "label"},
+    "frame":      {"tag": "iframe"},
+    "keyboard":   {"tag": "kbd"},
+    "map":        {"tag": "map"},
+    "area":       {"tag": "area"},
+    "mark":       {"tag": "mark"},
+    "noscript":   {"tag": "noscript"},
+    "object":     {"tag": "object"},
+    "progressbar":{"tag": "progress"},
+    "quote":      {"tag": "q"},
+    "small":      {"tag": "small"},
+    "variable":   {"tag": "var"}        
 }
 
 
 class Meta:
     """
     Class for storing meta data
     """
```

