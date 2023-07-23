# Comparing `tmp/chartfactor-jlab-ext-4.1.8.tar.gz` & `tmp/chartfactor-jlab-ext-4.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chartfactor-jlab-ext-4.1.8.tar", last modified: Fri May 26 22:51:58 2023, max compression
+gzip compressed data, was "chartfactor-jlab-ext-4.1.9.tar", last modified: Mon Jun  5 19:26:13 2023, max compression
```

## Comparing `chartfactor-jlab-ext-4.1.8.tar` & `chartfactor-jlab-ext-4.1.9.tar`

### file list

```diff
@@ -1,47 +1,47 @@
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:58.650082 chartfactor-jlab-ext-4.1.8/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1506 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.8/LICENSE
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      379 2022-09-08 23:50:12.000000 chartfactor-jlab-ext-4.1.8/MANIFEST.in
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     2905 2023-05-26 22:51:58.649911 chartfactor-jlab-ext-4.1.8/PKG-INFO
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1861 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.8/README.md
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:58.644425 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     6148 2023-04-06 16:48:24.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/.DS_Store
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      318 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/__init__.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      441 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/_version.py
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:58.644778 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     2342 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/package.json
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:58.647199 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    15480 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/100.7e3a5f4a20c0f69ea729.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     2669 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/223.a93208f6436a19e928eb.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      852 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/223.a93208f6436a19e928eb.js.LICENSE.txt
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    70526 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/486.ea74e810f4cf66ad8b28.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      336 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/486.ea74e810f4cf66ad8b28.js.LICENSE.txt
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     7250 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/568.dbf10b6f5d4cdc795fa9.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     3373 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/747.b46981187fdb90cccf38.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    85623 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/813.05d4b12c6f2c4f7d9c5b.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      219 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/813.05d4b12c6f2c4f7d9c5b.js.LICENSE.txt
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     7856 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/remoteEntry.e2d2ee7fd18234900432.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      163 2023-05-26 22:51:56.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/style.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    20796 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/third-party-licenses.json
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:58.648063 chartfactor-jlab-ext-4.1.8/chartfactor_jlab_ext.egg-info/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     2905 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor_jlab_ext.egg-info/PKG-INFO
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1436 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor_jlab_ext.egg-info/SOURCES.txt
--rw-r--r--   0 jorgealarcon   (501) staff       (20)        1 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor_jlab_ext.egg-info/dependency_links.txt
--rw-r--r--   0 jorgealarcon   (501) staff       (20)        1 2023-05-26 22:51:50.000000 chartfactor-jlab-ext-4.1.8/chartfactor_jlab_ext.egg-info/not-zip-safe
--rw-r--r--   0 jorgealarcon   (501) staff       (20)       56 2023-05-26 22:51:58.000000 chartfactor-jlab-ext-4.1.8/chartfactor_jlab_ext.egg-info/top_level.txt
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      201 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.8/install.json
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:58.649107 chartfactor-jlab-ext-4.1.8/lib/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     9591 2022-06-24 19:57:03.000000 chartfactor-jlab-ext-4.1.8/lib/cfs.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1675 2022-06-15 14:46:17.000000 chartfactor-jlab-ext-4.1.8/lib/commons.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      877 2022-06-15 14:46:17.000000 chartfactor-jlab-ext-4.1.8/lib/index.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1969 2022-06-17 17:26:57.000000 chartfactor-jlab-ext-4.1.8/lib/model.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      828 2022-05-26 22:15:14.000000 chartfactor-jlab-ext-4.1.8/lib/runner.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     2642 2022-05-26 22:15:14.000000 chartfactor-jlab-ext-4.1.8/lib/storage-utils.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     2198 2023-05-26 22:51:39.000000 chartfactor-jlab-ext-4.1.8/package.json
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      145 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.8/pyproject.toml
--rw-r--r--   0 jorgealarcon   (501) staff       (20)       38 2023-05-26 22:51:58.650136 chartfactor-jlab-ext-4.1.8/setup.cfg
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     2636 2022-09-08 23:50:12.000000 chartfactor-jlab-ext-4.1.8/setup.py
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:58.649677 chartfactor-jlab-ext-4.1.8/style/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.8/style/base.css
--rw-r--r--   0 jorgealarcon   (501) staff       (20)       25 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.8/style/index.css
--rw-r--r--   0 jorgealarcon   (501) staff       (20)       21 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.8/style/index.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)   259094 2022-06-07 13:33:05.000000 chartfactor-jlab-ext-4.1.8/yarn.lock
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:26:13.404478 chartfactor-jlab-ext-4.1.9/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1506 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.9/LICENSE
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      379 2022-09-08 23:50:12.000000 chartfactor-jlab-ext-4.1.9/MANIFEST.in
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     2905 2023-06-05 19:26:13.404300 chartfactor-jlab-ext-4.1.9/PKG-INFO
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1861 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.9/README.md
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:26:13.400796 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     6148 2023-04-06 16:48:24.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/.DS_Store
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      318 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/__init__.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      441 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/_version.py
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:26:13.401010 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     2342 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/package.json
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:26:13.402433 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    15480 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/100.7e3a5f4a20c0f69ea729.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     2669 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/223.a93208f6436a19e928eb.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      852 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/223.a93208f6436a19e928eb.js.LICENSE.txt
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    70526 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/486.ea74e810f4cf66ad8b28.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      336 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/486.ea74e810f4cf66ad8b28.js.LICENSE.txt
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     7251 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/568.2d2c02a3c2936fe59387.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     3373 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/747.b46981187fdb90cccf38.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    85623 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/813.05d4b12c6f2c4f7d9c5b.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      219 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/813.05d4b12c6f2c4f7d9c5b.js.LICENSE.txt
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     7858 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/remoteEntry.e714bbed80066b576564.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      163 2023-06-05 19:26:11.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/style.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    20796 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/third-party-licenses.json
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:26:13.403027 chartfactor-jlab-ext-4.1.9/chartfactor_jlab_ext.egg-info/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     2905 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor_jlab_ext.egg-info/PKG-INFO
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1436 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor_jlab_ext.egg-info/SOURCES.txt
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)        1 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor_jlab_ext.egg-info/dependency_links.txt
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)        1 2023-06-05 19:26:05.000000 chartfactor-jlab-ext-4.1.9/chartfactor_jlab_ext.egg-info/not-zip-safe
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)       56 2023-06-05 19:26:13.000000 chartfactor-jlab-ext-4.1.9/chartfactor_jlab_ext.egg-info/top_level.txt
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      201 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.9/install.json
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:26:13.403641 chartfactor-jlab-ext-4.1.9/lib/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     9591 2022-06-24 19:57:03.000000 chartfactor-jlab-ext-4.1.9/lib/cfs.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1675 2022-06-15 14:46:17.000000 chartfactor-jlab-ext-4.1.9/lib/commons.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      877 2022-06-15 14:46:17.000000 chartfactor-jlab-ext-4.1.9/lib/index.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1969 2022-06-17 17:26:57.000000 chartfactor-jlab-ext-4.1.9/lib/model.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      828 2022-05-26 22:15:14.000000 chartfactor-jlab-ext-4.1.9/lib/runner.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     2642 2022-05-26 22:15:14.000000 chartfactor-jlab-ext-4.1.9/lib/storage-utils.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     2198 2023-06-05 19:25:54.000000 chartfactor-jlab-ext-4.1.9/package.json
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      145 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.9/pyproject.toml
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)       38 2023-06-05 19:26:13.404519 chartfactor-jlab-ext-4.1.9/setup.cfg
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     2636 2022-09-08 23:50:12.000000 chartfactor-jlab-ext-4.1.9/setup.py
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:26:13.404101 chartfactor-jlab-ext-4.1.9/style/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.9/style/base.css
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)       25 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.9/style/index.css
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)       21 2022-02-15 22:26:32.000000 chartfactor-jlab-ext-4.1.9/style/index.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)   259094 2022-06-07 13:33:05.000000 chartfactor-jlab-ext-4.1.9/yarn.lock
```

### Comparing `chartfactor-jlab-ext-4.1.8/LICENSE` & `chartfactor-jlab-ext-4.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/PKG-INFO` & `chartfactor-jlab-ext-4.1.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chartfactor-jlab-ext
-Version: 4.1.8
+Version: 4.1.9
 Summary: Run chartfactor-py python commands in Jupyter Lab Kernels
 Home-page: https://github.com/Aktiun/chartfactor-jlab-ext
 Author: Aktiun
 Author-email: info@aktiun.com
 License: BSD-3-Clause
 Keywords: Jupyter,JupyterLab,JupyterLab3
 Platform: Linux
```

### Comparing `chartfactor-jlab-ext-4.1.8/README.md` & `chartfactor-jlab-ext-4.1.9/README.md`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/.DS_Store` & `chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/.DS_Store`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/package.json` & `chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/package.json`

 * *Files 2% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.972953216374269%*

 * *Differences: {"'jupyterlab'": "{'_build': {'load': 'static/remoteEntry.e714bbed80066b576564.js'}}",*

 * * "'version'": "'4.1.9'"}*

```diff
@@ -26,15 +26,15 @@
         "lib/**/*.{d.ts,eot,gif,html,jpg,js,js.map,json,png,svg,woff2,ttf}",
         "style/**/*.{css,js,eot,gif,html,jpg,json,png,svg,woff2,ttf}"
     ],
     "homepage": "https://github.com/Aktiun/chartfactor-jlab-ext",
     "jupyterlab": {
         "_build": {
             "extension": "./extension",
-            "load": "static/remoteEntry.e2d2ee7fd18234900432.js",
+            "load": "static/remoteEntry.e714bbed80066b576564.js",
             "style": "./style"
         },
         "extension": true,
         "outputDir": "chartfactor-jlab-ext/labextension"
     },
     "keywords": [
         "jupyter",
@@ -69,9 +69,9 @@
     },
     "sideEffects": [
         "style/*.css",
         "style/index.js"
     ],
     "style": "style/index.css",
     "styleModule": "style/index.js",
-    "version": "4.1.8"
+    "version": "4.1.9"
 }
```

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/100.7e3a5f4a20c0f69ea729.js` & `chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/100.7e3a5f4a20c0f69ea729.js`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/223.a93208f6436a19e928eb.js` & `chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/223.a93208f6436a19e928eb.js`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/223.a93208f6436a19e928eb.js.LICENSE.txt` & `chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/223.a93208f6436a19e928eb.js.LICENSE.txt`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/486.ea74e810f4cf66ad8b28.js` & `chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/486.ea74e810f4cf66ad8b28.js`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/568.dbf10b6f5d4cdc795fa9.js` & `chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/568.2d2c02a3c2936fe59387.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -18,15 +18,15 @@
                     return null === o && void 0 !== t ? t : o
                 };
             var c = o(797);
             const r = (e = null, t, o) => {
                 const s = o.currentWidget;
                 return !!e && !1 !== e.activate && s && t.shell.activateById(s.id), s
             };
-            var d = o(123);
+            var d = o(779);
             class l {
                 constructor(e, t) {
                     this.app = e, this.notebook = t, this.kernel = null, window.syncWithStudio = !0, window.currentApp = this.app, window.currentNotebook = this.notebook, window.souldDisplaySaveMessage = !0
                 }
                 createTempIframe(e = "https://chartfactor.com/studio/jupyter.html", t, o) {
                     let s = document.getElementById(t.id);
                     if (s) o(t, s);
@@ -167,17 +167,17 @@
                 }
             }
         },
         568: (e, t, o) => {
             o.r(t), o.d(t, {
                 default: () => r
             });
-            var s = o(123),
-                a = o(33),
-                n = o(573);
+            var s = o(779),
+                a = o(764),
+                n = o(612);
             const i = o(788).Z,
                 c = o(774).Z,
                 r = [{
                     id: "chartfactor_jlab_ext",
                     autoStart: !0,
                     requires: [s.INotebookTracker, a.ICommandPalette, n.IRenderMimeRegistry],
                     activate: function(e, t, o, s) {
```

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/747.b46981187fdb90cccf38.js` & `chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/747.b46981187fdb90cccf38.js`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/813.05d4b12c6f2c4f7d9c5b.js` & `chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/813.05d4b12c6f2c4f7d9c5b.js`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/remoteEntry.e2d2ee7fd18234900432.js` & `chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/remoteEntry.e714bbed80066b576564.js`

 * *Files 6% similar despite different names*

#### js-beautify {}

```diff
@@ -1,11 +1,11 @@
 var _JUPYTERLAB;
 (() => {
     "use strict";
-    var e, r, t, a, n, o, i, l, f, d, u, s, c, h, p, b, v, m, g = {
+    var e, r, t, a, n, o, i, l, f, u, d, s, c, h, p, b, v, m, g = {
             547: (e, r, t) => {
                 var a = {
                         "./index": () => t.e(568).then((() => () => t(568))),
                         "./extension": () => t.e(568).then((() => () => t(568))),
                         "./style": () => t.e(747).then((() => () => t(747)))
                     },
                     n = (e, r) => (t.R = r, r = t.o(a, e) ? a[e]() : Promise.resolve().then((() => {
@@ -49,42 +49,42 @@
         })
     }, w.f = {}, w.e = e => Promise.all(Object.keys(w.f).reduce(((r, t) => (w.f[t](e, r), r)), [])), w.u = e => e + "." + {
         100: "7e3a5f4a20c0f69ea729",
         223: "a93208f6436a19e928eb",
         271: "6e361e59632f15ffe513",
         456: "320b2a08bbe0354d4e5c",
         486: "ea74e810f4cf66ad8b28",
-        568: "dbf10b6f5d4cdc795fa9",
+        568: "2d2c02a3c2936fe59387",
         747: "b46981187fdb90cccf38",
         813: "05d4b12c6f2c4f7d9c5b"
     } [e] + ".js?v=" + {
         100: "7e3a5f4a20c0f69ea729",
         223: "a93208f6436a19e928eb",
         271: "6e361e59632f15ffe513",
         456: "320b2a08bbe0354d4e5c",
         486: "ea74e810f4cf66ad8b28",
-        568: "dbf10b6f5d4cdc795fa9",
+        568: "2d2c02a3c2936fe59387",
         747: "b46981187fdb90cccf38",
         813: "05d4b12c6f2c4f7d9c5b"
     } [e], w.g = function() {
         if ("object" == typeof globalThis) return globalThis;
         try {
             return this || new Function("return this")()
         } catch (e) {
             if ("object" == typeof window) return window
         }
     }(), w.o = (e, r) => Object.prototype.hasOwnProperty.call(e, r), e = {}, r = "chartfactor_jlab_ext:", w.l = (t, a, n, o) => {
         if (e[t]) e[t].push(a);
         else {
             var i, l;
             if (void 0 !== n)
-                for (var f = document.getElementsByTagName("script"), d = 0; d < f.length; d++) {
-                    var u = f[d];
-                    if (u.getAttribute("src") == t || u.getAttribute("data-webpack") == r + n) {
-                        i = u;
+                for (var f = document.getElementsByTagName("script"), u = 0; u < f.length; u++) {
+                    var d = f[u];
+                    if (d.getAttribute("src") == t || d.getAttribute("data-webpack") == r + n) {
+                        i = d;
                         break
                     }
                 }
             i || (l = !0, (i = document.createElement("script")).charset = "utf-8", i.timeout = 120, w.nc && i.setAttribute("nonce", w.nc), i.setAttribute("data-webpack", r + n), i.src = t), e[t] = [a];
             var s = (r, a) => {
                     i.onerror = i.onload = null, clearTimeout(c);
                     var n = e[t];
@@ -120,15 +120,15 @@
                         (!l || !l.loaded && (!a != !l.eager ? a : i > l.from)) && (n[r] = {
                             get: t,
                             from: i,
                             eager: !!a
                         })
                     },
                     f = [];
-                return "default" === t && (l("@phosphor/disposable", "1.10.1", (() => w.e(223).then((() => () => w(223))))), l("chartfactor_jlab_ext", "4.1.8", (() => w.e(568).then((() => () => w(568))))), l("jupyterlab_toastify", "4.2.1", (() => Promise.all([w.e(813), w.e(271)]).then((() => () => w(813))))), l("lodash", "4.17.21", (() => w.e(486).then((() => () => w(486)))))), e[t] = f.length ? Promise.all(f).then((() => e[t] = 1)) : 1
+                return "default" === t && (l("@phosphor/disposable", "1.10.1", (() => w.e(223).then((() => () => w(223))))), l("chartfactor_jlab_ext", "4.1.9", (() => w.e(568).then((() => () => w(568))))), l("jupyterlab_toastify", "4.2.1", (() => Promise.all([w.e(813), w.e(271)]).then((() => () => w(813))))), l("lodash", "4.17.21", (() => w.e(486).then((() => () => w(486)))))), e[t] = f.length ? Promise.all(f).then((() => e[t] = 1)) : 1
             }
         }
     })(), (() => {
         var e;
         w.g.importScripts && (e = w.g.location + "");
         var r = w.g.document;
         if (!e && r && (r.currentScript && (e = r.currentScript.src), !e)) {
@@ -177,31 +177,31 @@
     }, o = (e, r) => {
         if (0 in e) {
             r = t(r);
             var a = e[0],
                 n = a < 0;
             n && (a = -a - 1);
             for (var i = 0, l = 1, f = !0;; l++, i++) {
-                var d, u, s = l < e.length ? (typeof e[l])[0] : "";
-                if (i >= r.length || "o" == (u = (typeof(d = r[i]))[0])) return !f || ("u" == s ? l > a && !n : "" == s != n);
-                if ("u" == u) {
+                var u, d, s = l < e.length ? (typeof e[l])[0] : "";
+                if (i >= r.length || "o" == (d = (typeof(u = r[i]))[0])) return !f || ("u" == s ? l > a && !n : "" == s != n);
+                if ("u" == d) {
                     if (!f || "u" != s) return !1
                 } else if (f)
-                    if (s == u)
+                    if (s == d)
                         if (l <= a) {
-                            if (d != e[l]) return !1
+                            if (u != e[l]) return !1
                         } else {
-                            if (n ? d > e[l] : d < e[l]) return !1;
-                            d != e[l] && (f = !1)
+                            if (n ? u > e[l] : u < e[l]) return !1;
+                            u != e[l] && (f = !1)
                         }
                 else if ("s" != s && "n" != s) {
                     if (n || l <= a) return !1;
                     f = !1, l--
                 } else {
-                    if (l <= a || u < s != n) return !1;
+                    if (l <= a || d < s != n) return !1;
                     f = !1
                 } else "s" != s && "n" != s && (f = !1, l--)
             }
         }
         var c = [],
             h = c.pop.bind(c);
         for (i = 1; i < e.length; i++) {
@@ -212,42 +212,42 @@
     }, i = (e, r) => {
         var t = w.S[e];
         if (!t || !w.o(t, r)) throw new Error("Shared module " + r + " doesn't exist in shared scope " + e);
         return t
     }, l = (e, r) => {
         var t = e[r];
         return Object.keys(t).reduce(((e, r) => !e || !t[e].loaded && a(e, r) ? r : e), 0)
-    }, f = (e, r, t, a) => "Unsatisfied version " + t + " from " + (t && e[r][t].from) + " of shared singleton module " + r + " (required " + n(a) + ")", d = (e, r, t, a) => {
+    }, f = (e, r, t, a) => "Unsatisfied version " + t + " from " + (t && e[r][t].from) + " of shared singleton module " + r + " (required " + n(a) + ")", u = (e, r, t, a) => {
         var n = l(e, t);
         return o(a, n) || "undefined" != typeof console && console.warn && console.warn(f(e, t, n, a)), s(e[t][n])
-    }, u = (e, r, t) => {
+    }, d = (e, r, t) => {
         var n = e[r];
         return (r = Object.keys(n).reduce(((e, r) => !o(t, r) || e && !a(e, r) ? e : r), 0)) && n[r]
     }, s = e => (e.loaded = 1, e.get()), h = (c = e => function(r, t, a, n) {
         var o = w.I(r);
         return o && o.then ? o.then(e.bind(e, r, w.S[r], t, a, n)) : e(r, w.S[r], t, a, n)
-    })(((e, r, t, a) => (i(e, t), d(r, 0, t, a)))), p = c(((e, r, t, a, n) => {
-        var o = r && w.o(r, t) && u(r, t, a);
+    })(((e, r, t, a) => (i(e, t), u(r, 0, t, a)))), p = c(((e, r, t, a, n) => {
+        var o = r && w.o(r, t) && d(r, t, a);
         return o ? s(o) : n()
     })), b = {}, v = {
-        33: () => h("default", "@jupyterlab/apputils", [1, 3, 6, 3]),
-        123: () => h("default", "@jupyterlab/notebook", [1, 3, 6, 3]),
         138: () => p("default", "@phosphor/disposable", [1, 1, 3, 1], (() => w.e(223).then((() => () => w(223))))),
         439: () => p("default", "lodash", [1, 4, 17, 21], (() => w.e(486).then((() => () => w(486))))),
-        573: () => h("default", "@jupyterlab/rendermime", [1, 3, 6, 3]),
+        612: () => h("default", "@jupyterlab/rendermime", [1, 3, 6, 4]),
+        764: () => h("default", "@jupyterlab/apputils", [1, 3, 6, 4]),
+        779: () => h("default", "@jupyterlab/notebook", [1, 3, 6, 4]),
         797: () => p("default", "jupyterlab_toastify", [1, 4, 2, 1], (() => Promise.all([w.e(813), w.e(271)]).then((() => () => w(813))))),
         840: () => h("default", "@lumino/signaling", [1, 1, 10, 0]),
         918: () => h("default", "@lumino/algorithm", [1, 1, 9, 0]),
         271: () => h("default", "react", [1, 17, 0, 1]),
         456: () => h("default", "react-dom", [1, 17, 0, 1])
     }, m = {
         223: [840, 918],
         271: [271],
         456: [456],
-        568: [33, 123, 138, 439, 573, 797]
+        568: [138, 439, 612, 764, 779, 797]
     }, w.f.consumes = (e, r) => {
         w.o(m, e) && m[e].forEach((e => {
             if (w.o(b, e)) return r.push(b[e]);
             var t = r => {
                     b[e] = 0, w.m[e] = t => {
                         delete w.c[e], t.exports = r()
                     }
```

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor-jlab-ext/labextension/static/third-party-licenses.json` & `chartfactor-jlab-ext-4.1.9/chartfactor-jlab-ext/labextension/static/third-party-licenses.json`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor_jlab_ext.egg-info/PKG-INFO` & `chartfactor-jlab-ext-4.1.9/chartfactor_jlab_ext.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chartfactor-jlab-ext
-Version: 4.1.8
+Version: 4.1.9
 Summary: Run chartfactor-py python commands in Jupyter Lab Kernels
 Home-page: https://github.com/Aktiun/chartfactor-jlab-ext
 Author: Aktiun
 Author-email: info@aktiun.com
 License: BSD-3-Clause
 Keywords: Jupyter,JupyterLab,JupyterLab3
 Platform: Linux
```

### Comparing `chartfactor-jlab-ext-4.1.8/chartfactor_jlab_ext.egg-info/SOURCES.txt` & `chartfactor-jlab-ext-4.1.9/chartfactor_jlab_ext.egg-info/SOURCES.txt`

 * *Files 10% similar despite different names*

```diff
@@ -11,19 +11,19 @@
 chartfactor-jlab-ext/_version.py
 chartfactor-jlab-ext/labextension/package.json
 chartfactor-jlab-ext/labextension/static/100.7e3a5f4a20c0f69ea729.js
 chartfactor-jlab-ext/labextension/static/223.a93208f6436a19e928eb.js
 chartfactor-jlab-ext/labextension/static/223.a93208f6436a19e928eb.js.LICENSE.txt
 chartfactor-jlab-ext/labextension/static/486.ea74e810f4cf66ad8b28.js
 chartfactor-jlab-ext/labextension/static/486.ea74e810f4cf66ad8b28.js.LICENSE.txt
-chartfactor-jlab-ext/labextension/static/568.dbf10b6f5d4cdc795fa9.js
+chartfactor-jlab-ext/labextension/static/568.2d2c02a3c2936fe59387.js
 chartfactor-jlab-ext/labextension/static/747.b46981187fdb90cccf38.js
 chartfactor-jlab-ext/labextension/static/813.05d4b12c6f2c4f7d9c5b.js
 chartfactor-jlab-ext/labextension/static/813.05d4b12c6f2c4f7d9c5b.js.LICENSE.txt
-chartfactor-jlab-ext/labextension/static/remoteEntry.e2d2ee7fd18234900432.js
+chartfactor-jlab-ext/labextension/static/remoteEntry.e714bbed80066b576564.js
 chartfactor-jlab-ext/labextension/static/style.js
 chartfactor-jlab-ext/labextension/static/third-party-licenses.json
 chartfactor_jlab_ext.egg-info/PKG-INFO
 chartfactor_jlab_ext.egg-info/SOURCES.txt
 chartfactor_jlab_ext.egg-info/dependency_links.txt
 chartfactor_jlab_ext.egg-info/not-zip-safe
 chartfactor_jlab_ext.egg-info/top_level.txt
```

### Comparing `chartfactor-jlab-ext-4.1.8/lib/cfs.js` & `chartfactor-jlab-ext-4.1.9/lib/cfs.js`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/lib/commons.js` & `chartfactor-jlab-ext-4.1.9/lib/commons.js`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/lib/index.js` & `chartfactor-jlab-ext-4.1.9/lib/index.js`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/lib/model.js` & `chartfactor-jlab-ext-4.1.9/lib/model.js`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/lib/runner.js` & `chartfactor-jlab-ext-4.1.9/lib/runner.js`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/lib/storage-utils.js` & `chartfactor-jlab-ext-4.1.9/lib/storage-utils.js`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/package.json` & `chartfactor-jlab-ext-4.1.9/package.json`

 * *Files 1% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9736842105263158%*

 * *Differences: {"'version'": "'4.1.9'"}*

```diff
@@ -64,9 +64,9 @@
     },
     "sideEffects": [
         "style/*.css",
         "style/index.js"
     ],
     "style": "style/index.css",
     "styleModule": "style/index.js",
-    "version": "4.1.8"
+    "version": "4.1.9"
 }
```

### Comparing `chartfactor-jlab-ext-4.1.8/setup.py` & `chartfactor-jlab-ext-4.1.9/setup.py`

 * *Files identical despite different names*

### Comparing `chartfactor-jlab-ext-4.1.8/yarn.lock` & `chartfactor-jlab-ext-4.1.9/yarn.lock`

 * *Files identical despite different names*

