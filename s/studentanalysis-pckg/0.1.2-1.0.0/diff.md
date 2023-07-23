# Comparing `tmp/studentanalysis_pckg-0.1.2.tar.gz` & `tmp/studentanalysis_pckg-1.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "studentanalysis_pckg-0.1.2.tar", last modified: Sun Jul 23 13:34:26 2023, max compression
+gzip compressed data, was "studentanalysis_pckg-1.0.0.tar", last modified: Sun Jul 23 14:07:59 2023, max compression
```

## Comparing `studentanalysis_pckg-0.1.2.tar` & `studentanalysis_pckg-1.0.0.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 13:34:26.947594 studentanalysis_pckg-0.1.2/
--rw-rw-rw-   0        0        0     1128 2023-07-14 16:10:48.000000 studentanalysis_pckg-0.1.2/LICENSE.txt
--rw-rw-rw-   0        0        0      156 2023-07-23 13:34:26.946593 studentanalysis_pckg-0.1.2/PKG-INFO
--rw-rw-rw-   0        0        0     4855 2023-07-23 11:45:47.000000 studentanalysis_pckg-0.1.2/README.md
--rw-rw-rw-   0        0        0       42 2023-07-23 13:34:26.947594 studentanalysis_pckg-0.1.2/setup.cfg
--rw-rw-rw-   0        0        0      349 2023-07-23 13:32:41.000000 studentanalysis_pckg-0.1.2/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:34:26.936591 studentanalysis_pckg-0.1.2/studentanalysis_pckg/
--rw-rw-rw-   0        0        0        0 2023-07-23 13:29:24.000000 studentanalysis_pckg-0.1.2/studentanalysis_pckg/__init__.py
--rw-rw-rw-   0        0        0    20155 2023-07-23 13:12:34.000000 studentanalysis_pckg-0.1.2/studentanalysis_pckg/main.py
--rw-rw-rw-   0        0        0    12461 2023-07-23 12:33:03.000000 studentanalysis_pckg-0.1.2/studentanalysis_pckg/test_main.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:34:26.945593 studentanalysis_pckg-0.1.2/studentanalysis_pckg.egg-info/
--rw-rw-rw-   0        0        0      156 2023-07-23 13:34:26.000000 studentanalysis_pckg-0.1.2/studentanalysis_pckg.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      345 2023-07-23 13:34:26.000000 studentanalysis_pckg-0.1.2/studentanalysis_pckg.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 13:34:26.000000 studentanalysis_pckg-0.1.2/studentanalysis_pckg.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       35 2023-07-23 13:34:26.000000 studentanalysis_pckg-0.1.2/studentanalysis_pckg.egg-info/requires.txt
--rw-rw-rw-   0        0        0       21 2023-07-23 13:34:26.000000 studentanalysis_pckg-0.1.2/studentanalysis_pckg.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 14:07:59.848125 studentanalysis_pckg-1.0.0/
+-rw-rw-rw-   0        0        0     1128 2023-07-14 16:10:48.000000 studentanalysis_pckg-1.0.0/LICENSE.txt
+-rw-rw-rw-   0        0        0      156 2023-07-23 14:07:59.847126 studentanalysis_pckg-1.0.0/PKG-INFO
+-rw-rw-rw-   0        0        0     4855 2023-07-23 11:45:47.000000 studentanalysis_pckg-1.0.0/README.md
+-rw-rw-rw-   0        0        0       42 2023-07-23 14:07:59.848125 studentanalysis_pckg-1.0.0/setup.cfg
+-rw-rw-rw-   0        0        0      349 2023-07-23 14:07:19.000000 studentanalysis_pckg-1.0.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 14:07:59.840618 studentanalysis_pckg-1.0.0/studentanalysis_pckg/
+-rw-rw-rw-   0        0        0        0 2023-07-23 13:29:24.000000 studentanalysis_pckg-1.0.0/studentanalysis_pckg/__init__.py
+-rw-rw-rw-   0        0        0    20155 2023-07-23 13:12:34.000000 studentanalysis_pckg-1.0.0/studentanalysis_pckg/main.py
+-rw-rw-rw-   0        0        0    12461 2023-07-23 12:33:03.000000 studentanalysis_pckg-1.0.0/studentanalysis_pckg/test_main.py
+drwxrwxrwx   0        0        0        0 2023-07-23 14:07:59.846124 studentanalysis_pckg-1.0.0/studentanalysis_pckg.egg-info/
+-rw-rw-rw-   0        0        0      156 2023-07-23 14:07:59.000000 studentanalysis_pckg-1.0.0/studentanalysis_pckg.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      345 2023-07-23 14:07:59.000000 studentanalysis_pckg-1.0.0/studentanalysis_pckg.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 14:07:59.000000 studentanalysis_pckg-1.0.0/studentanalysis_pckg.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       35 2023-07-23 14:07:59.000000 studentanalysis_pckg-1.0.0/studentanalysis_pckg.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       21 2023-07-23 14:07:59.000000 studentanalysis_pckg-1.0.0/studentanalysis_pckg.egg-info/top_level.txt
```

### Comparing `studentanalysis_pckg-0.1.2/LICENSE.txt` & `studentanalysis_pckg-1.0.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `studentanalysis_pckg-0.1.2/README.md` & `studentanalysis_pckg-1.0.0/README.md`

 * *Files identical despite different names*

### Comparing `studentanalysis_pckg-0.1.2/studentanalysis_pckg/main.py` & `studentanalysis_pckg-1.0.0/studentanalysis_pckg/main.py`

 * *Files identical despite different names*

### Comparing `studentanalysis_pckg-0.1.2/studentanalysis_pckg/test_main.py` & `studentanalysis_pckg-1.0.0/studentanalysis_pckg/test_main.py`

 * *Files identical despite different names*

