# Comparing `tmp/tubeup-2023.7.23.tar.gz` & `tmp/tubeup-28.5.2023.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tubeup-2023.7.23.tar", last modified: Sun Jul 23 21:20:52 2023, max compression
+gzip compressed data, was "tubeup-28.5.2023.tar", last modified: Sun May 28 22:42:49 2023, max compression
```

## Comparing `tubeup-2023.7.23.tar` & `tubeup-28.5.2023.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxrwxr-x   0 vxbinaca  (1000) vxbinaca  (1000)        0 2023-07-23 21:20:52.556399 tubeup-2023.7.23/
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)    35122 2021-09-28 02:31:45.000000 tubeup-2023.7.23/LICENSE
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      261 2023-07-23 21:20:52.556399 tubeup-2023.7.23/PKG-INFO
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)    10312 2023-05-28 22:41:06.000000 tubeup-2023.7.23/README.md
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      233 2023-07-23 21:20:52.556399 tubeup-2023.7.23/setup.cfg
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      756 2023-07-23 21:19:21.000000 tubeup-2023.7.23/setup.py
-drwxrwxr-x   0 vxbinaca  (1000) vxbinaca  (1000)        0 2023-07-23 21:20:52.556399 tubeup-2023.7.23/tubeup/
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)    24200 2023-05-28 22:41:06.000000 tubeup-2023.7.23/tubeup/TubeUp.py
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)       27 2023-07-23 21:20:30.000000 tubeup-2023.7.23/tubeup/__init__.py
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)     4671 2023-01-02 22:16:20.000000 tubeup-2023.7.23/tubeup/__main__.py
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      634 2021-09-28 02:31:45.000000 tubeup-2023.7.23/tubeup/utils.py
-drwxrwxr-x   0 vxbinaca  (1000) vxbinaca  (1000)        0 2023-07-23 21:20:52.556399 tubeup-2023.7.23/tubeup.egg-info/
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      261 2023-07-23 21:20:52.000000 tubeup-2023.7.23/tubeup.egg-info/PKG-INFO
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      289 2023-07-23 21:20:52.000000 tubeup-2023.7.23/tubeup.egg-info/SOURCES.txt
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)        1 2023-07-23 21:20:52.000000 tubeup-2023.7.23/tubeup.egg-info/dependency_links.txt
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)       49 2023-07-23 21:20:52.000000 tubeup-2023.7.23/tubeup.egg-info/entry_points.txt
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)       54 2023-07-23 21:20:52.000000 tubeup-2023.7.23/tubeup.egg-info/requires.txt
--rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)        7 2023-07-23 21:20:52.000000 tubeup-2023.7.23/tubeup.egg-info/top_level.txt
+drwxrwxr-x   0 vxbinaca  (1000) vxbinaca  (1000)        0 2023-05-28 22:42:49.780250 tubeup-28.5.2023/
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)    35122 2021-09-28 02:31:45.000000 tubeup-28.5.2023/LICENSE
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      261 2023-05-28 22:42:49.780250 tubeup-28.5.2023/PKG-INFO
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)    10312 2023-05-28 22:41:06.000000 tubeup-28.5.2023/README.md
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      233 2023-05-28 22:42:49.780250 tubeup-28.5.2023/setup.cfg
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      763 2023-01-02 22:16:20.000000 tubeup-28.5.2023/setup.py
+drwxrwxr-x   0 vxbinaca  (1000) vxbinaca  (1000)        0 2023-05-28 22:42:49.776250 tubeup-28.5.2023/tubeup/
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)    24200 2023-05-28 22:41:06.000000 tubeup-28.5.2023/tubeup/TubeUp.py
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)       26 2023-05-28 22:42:40.000000 tubeup-28.5.2023/tubeup/__init__.py
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)     4671 2023-01-02 22:16:20.000000 tubeup-28.5.2023/tubeup/__main__.py
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      634 2021-09-28 02:31:45.000000 tubeup-28.5.2023/tubeup/utils.py
+drwxrwxr-x   0 vxbinaca  (1000) vxbinaca  (1000)        0 2023-05-28 22:42:49.780250 tubeup-28.5.2023/tubeup.egg-info/
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      261 2023-05-28 22:42:49.000000 tubeup-28.5.2023/tubeup.egg-info/PKG-INFO
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)      289 2023-05-28 22:42:49.000000 tubeup-28.5.2023/tubeup.egg-info/SOURCES.txt
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)        1 2023-05-28 22:42:49.000000 tubeup-28.5.2023/tubeup.egg-info/dependency_links.txt
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)       49 2023-05-28 22:42:49.000000 tubeup-28.5.2023/tubeup.egg-info/entry_points.txt
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)       61 2023-05-28 22:42:49.000000 tubeup-28.5.2023/tubeup.egg-info/requires.txt
+-rw-rw-r--   0 vxbinaca  (1000) vxbinaca  (1000)        7 2023-05-28 22:42:49.000000 tubeup-28.5.2023/tubeup.egg-info/top_level.txt
```

### Comparing `tubeup-2023.7.23/LICENSE` & `tubeup-28.5.2023/LICENSE`

 * *Files identical despite different names*

### Comparing `tubeup-2023.7.23/README.md` & `tubeup-28.5.2023/README.md`

 * *Files identical despite different names*

### Comparing `tubeup-2023.7.23/setup.py` & `tubeup-28.5.2023/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -21,13 +21,13 @@
     ],
     entry_points={
         'console_scripts': [
             'tubeup = tubeup.__main__:main',
         ],
     },
     install_requires=[
-        'internetarchive',
+        'internetarchive==3.0.2',
         'urllib3==1.26.13',
         'docopt==0.6.2',
         'yt-dlp',
     ]
 )
```

### Comparing `tubeup-2023.7.23/tubeup/TubeUp.py` & `tubeup-28.5.2023/tubeup/TubeUp.py`

 * *Files identical despite different names*

### Comparing `tubeup-2023.7.23/tubeup/__main__.py` & `tubeup-28.5.2023/tubeup/__main__.py`

 * *Files identical despite different names*

### Comparing `tubeup-2023.7.23/tubeup/utils.py` & `tubeup-28.5.2023/tubeup/utils.py`

 * *Files identical despite different names*

