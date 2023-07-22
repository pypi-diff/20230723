# Comparing `tmp/unigui-1.9.0.tar.gz` & `tmp/unigui-1.9.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/unigui-1.9.0.tar", last modified: Fri Jul 21 11:09:12 2023, max compression
+gzip compressed data, was "dist/unigui-1.9.1.tar", last modified: Sat Jul 22 23:32:35 2023, max compression
```

## Comparing `unigui-1.9.0.tar` & `unigui-1.9.1.tar`

### file list

```diff
@@ -1,52 +1,52 @@
-drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-21 11:09:12.000000 unigui-1.9.0/
-drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui/
--rw-rw-r--   0 george    (1000) george    (1000)     8595 2023-07-21 05:14:03.000000 unigui-1.9.0/unigui/guielements.py
--rw-rw-r--   0 george    (1000) george    (1000)     2644 2023-07-21 08:53:12.000000 unigui-1.9.0/unigui/server.py
--rw-rw-r--   0 george    (1000) george    (1000)      108 2023-07-21 04:22:38.000000 unigui-1.9.0/unigui/__init__.py
--rw-rw-r--   0 george    (1000) george    (1000)     4801 2023-07-21 10:35:37.000000 unigui-1.9.0/unigui/autotest.py
--rw-r--r--   0 george    (1000) george    (1000)     2490 2023-07-21 10:20:58.000000 unigui-1.9.0/unigui/utils.py
--rw-rw-r--   0 george    (1000) george    (1000)     5587 2023-07-19 22:23:17.000000 unigui-1.9.0/unigui/reloader.py
--rw-rw-r--   0 george    (1000) george    (1000)     8110 2023-07-21 04:21:24.000000 unigui-1.9.0/unigui/users.py
-drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui/web/
--rw-rw-r--   0 george    (1000) george    (1000)    64483 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/favicon.ico
-drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui/web/css/
--rw-rw-r--   0 george    (1000) george    (1000)   220628 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/css/vendor.191faa77.css
--rw-rw-r--   0 george    (1000) george    (1000)        0 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/css/app.31d6cfe0.css
--rw-rw-r--   0 george    (1000) george    (1000)    37826 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/css/vendor.191faa77.css.gz
--rw-rw-r--   0 george    (1000) george    (1000)     3296 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/css/615.3024385a.css
-drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui/web/icons/
--rw-rw-r--   0 george    (1000) george    (1000)     9643 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/icons/favicon-96x96.png
--rw-rw-r--   0 george    (1000) george    (1000)      859 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/icons/favicon-16x16.png
--rw-rw-r--   0 george    (1000) george    (1000)     2039 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/icons/favicon-32x32.png
--rw-rw-r--   0 george    (1000) george    (1000)    12324 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/icons/favicon-128x128.png
-drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui/web/fonts/
--rw-rw-r--   0 george    (1000) george    (1000)   128616 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/fonts/flUhRq6tzZclQEJ-Vdg-IuiaDsNcIhQ8tQ.c5371cfb.woff2
--rw-rw-r--   0 george    (1000) george    (1000)   164912 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/fonts/flUhRq6tzZclQEJ-Vdg-IuiaDsNa.4d73cb90.woff
--rw-rw-r--   0 george    (1000) george    (1000)    20344 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/fonts/KFOmCnqEu92Fr1Mu4mxM.f1e2a767.woff
--rw-rw-r--   0 george    (1000) george    (1000)    20416 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/fonts/KFOlCnqEu92Fr1MmSU5fBBc-.c2f7ab22.woff
--rw-rw-r--   0 george    (1000) george    (1000)    20408 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/fonts/KFOlCnqEu92Fr1MmWUlfBBc-.77ecb942.woff
--rw-rw-r--   0 george    (1000) george    (1000)    20424 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/fonts/KFOlCnqEu92Fr1MmYUtfBBc-.f5677eb2.woff
--rw-rw-r--   0 george    (1000) george    (1000)    20544 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/fonts/KFOlCnqEu92Fr1MmEU9fBBc-.48af7707.woff
--rw-rw-r--   0 george    (1000) george    (1000)    20436 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/fonts/KFOkCnqEu92Fr1MmgVxIIzQ.68bb21d0.woff
-drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui/web/js/
--rw-rw-r--   0 george    (1000) george    (1000)    46024 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/js/615.04cc6ad4.js
--rw-rw-r--   0 george    (1000) george    (1000)     6560 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/js/430.591e9a73.js
--rw-rw-r--   0 george    (1000) george    (1000)  1434072 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/js/vendor.3076c5e7.js
--rw-rw-r--   0 george    (1000) george    (1000)     5868 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/js/app.fb1ab18a.js
--rw-rw-r--   0 george    (1000) george    (1000)    14198 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/js/615.04cc6ad4.js.gz
--rw-rw-r--   0 george    (1000) george    (1000)   469734 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/js/vendor.3076c5e7.js.gz
--rw-rw-r--   0 george    (1000) george    (1000)      763 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/js/193.283445be.js
--rw-rw-r--   0 george    (1000) george    (1000)      907 2023-07-21 10:44:37.000000 unigui-1.9.0/unigui/web/index.html
--rw-r--r--   0 george    (1000) george    (1000)     1073 2020-12-06 13:19:46.000000 unigui-1.9.0/LICENSE
--rw-rw-r--   0 george    (1000) george    (1000)      630 2023-07-21 11:08:25.000000 unigui-1.9.0/setup.py
--rw-rw-r--   0 george    (1000) george    (1000)    19239 2023-07-21 11:09:12.000000 unigui-1.9.0/PKG-INFO
--rw-rw-r--   0 george    (1000) george    (1000)       38 2023-07-21 11:09:12.000000 unigui-1.9.0/setup.cfg
--rw-rw-r--   0 george    (1000) george    (1000)    18934 2023-07-17 14:52:22.000000 unigui-1.9.0/README.md
--rw-rw-r--   0 george    (1000) george    (1000)       43 2021-04-23 05:55:14.000000 unigui-1.9.0/MANIFEST.in
-drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui.egg-info/
--rw-rw-r--   0 george    (1000) george    (1000)       54 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui.egg-info/requires.txt
--rw-r--r--   0 george    (1000) george    (1000)        1 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui.egg-info/dependency_links.txt
--rw-r--r--   0 george    (1000) george    (1000)    19239 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui.egg-info/PKG-INFO
--rw-r--r--   0 george    (1000) george    (1000)        1 2020-12-06 17:27:14.000000 unigui-1.9.0/unigui.egg-info/not-zip-safe
--rw-r--r--   0 george    (1000) george    (1000)     1348 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui.egg-info/SOURCES.txt
--rw-r--r--   0 george    (1000) george    (1000)        7 2023-07-21 11:09:12.000000 unigui-1.9.0/unigui.egg-info/top_level.txt
+drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-22 23:32:35.000000 unigui-1.9.1/
+drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui/
+-rw-rw-r--   0 george    (1000) george    (1000)     8640 2023-07-21 16:29:57.000000 unigui-1.9.1/unigui/guielements.py
+-rw-rw-r--   0 george    (1000) george    (1000)     2700 2023-07-21 15:52:14.000000 unigui-1.9.1/unigui/server.py
+-rw-rw-r--   0 george    (1000) george    (1000)      108 2023-07-21 04:22:38.000000 unigui-1.9.1/unigui/__init__.py
+-rw-rw-r--   0 george    (1000) george    (1000)     4772 2023-07-21 16:20:46.000000 unigui-1.9.1/unigui/autotest.py
+-rw-r--r--   0 george    (1000) george    (1000)     2490 2023-07-21 10:20:58.000000 unigui-1.9.1/unigui/utils.py
+-rw-rw-r--   0 george    (1000) george    (1000)     5587 2023-07-19 22:23:17.000000 unigui-1.9.1/unigui/reloader.py
+-rw-rw-r--   0 george    (1000) george    (1000)     8110 2023-07-21 04:21:24.000000 unigui-1.9.1/unigui/users.py
+drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui/web/
+-rw-rw-r--   0 george    (1000) george    (1000)    64483 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/favicon.ico
+drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui/web/css/
+-rw-rw-r--   0 george    (1000) george    (1000)     2691 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/css/9.44b298e4.css
+-rw-rw-r--   0 george    (1000) george    (1000)   220628 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/css/vendor.191faa77.css
+-rw-rw-r--   0 george    (1000) george    (1000)        0 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/css/app.31d6cfe0.css
+-rw-rw-r--   0 george    (1000) george    (1000)    37826 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/css/vendor.191faa77.css.gz
+drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui/web/icons/
+-rw-rw-r--   0 george    (1000) george    (1000)     9643 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/icons/favicon-96x96.png
+-rw-rw-r--   0 george    (1000) george    (1000)      859 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/icons/favicon-16x16.png
+-rw-rw-r--   0 george    (1000) george    (1000)     2039 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/icons/favicon-32x32.png
+-rw-rw-r--   0 george    (1000) george    (1000)    12324 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/icons/favicon-128x128.png
+drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui/web/fonts/
+-rw-rw-r--   0 george    (1000) george    (1000)   128616 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/fonts/flUhRq6tzZclQEJ-Vdg-IuiaDsNcIhQ8tQ.c5371cfb.woff2
+-rw-rw-r--   0 george    (1000) george    (1000)   164912 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/fonts/flUhRq6tzZclQEJ-Vdg-IuiaDsNa.4d73cb90.woff
+-rw-rw-r--   0 george    (1000) george    (1000)    20344 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/fonts/KFOmCnqEu92Fr1Mu4mxM.f1e2a767.woff
+-rw-rw-r--   0 george    (1000) george    (1000)    20416 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/fonts/KFOlCnqEu92Fr1MmSU5fBBc-.c2f7ab22.woff
+-rw-rw-r--   0 george    (1000) george    (1000)    20408 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/fonts/KFOlCnqEu92Fr1MmWUlfBBc-.77ecb942.woff
+-rw-rw-r--   0 george    (1000) george    (1000)    20424 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/fonts/KFOlCnqEu92Fr1MmYUtfBBc-.f5677eb2.woff
+-rw-rw-r--   0 george    (1000) george    (1000)    20544 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/fonts/KFOlCnqEu92Fr1MmEU9fBBc-.48af7707.woff
+-rw-rw-r--   0 george    (1000) george    (1000)    20436 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/fonts/KFOkCnqEu92Fr1MmgVxIIzQ.68bb21d0.woff
+drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui/web/js/
+-rw-rw-r--   0 george    (1000) george    (1000)  1434158 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/js/vendor.18cce91f.js
+-rw-rw-r--   0 george    (1000) george    (1000)     6560 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/js/430.591e9a73.js
+-rw-rw-r--   0 george    (1000) george    (1000)     5860 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/js/app.c7c500ce.js
+-rw-rw-r--   0 george    (1000) george    (1000)    14595 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/js/9.100130f6.js.gz
+-rw-rw-r--   0 george    (1000) george    (1000)   469773 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/js/vendor.18cce91f.js.gz
+-rw-rw-r--   0 george    (1000) george    (1000)    47791 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/js/9.100130f6.js
+-rw-rw-r--   0 george    (1000) george    (1000)      763 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/js/193.283445be.js
+-rw-rw-r--   0 george    (1000) george    (1000)      907 2023-07-22 22:58:02.000000 unigui-1.9.1/unigui/web/index.html
+-rw-r--r--   0 george    (1000) george    (1000)     1073 2020-12-06 13:19:46.000000 unigui-1.9.1/LICENSE
+-rw-rw-r--   0 george    (1000) george    (1000)      630 2023-07-22 23:30:56.000000 unigui-1.9.1/setup.py
+-rw-rw-r--   0 george    (1000) george    (1000)    19239 2023-07-22 23:32:35.000000 unigui-1.9.1/PKG-INFO
+-rw-rw-r--   0 george    (1000) george    (1000)       38 2023-07-22 23:32:35.000000 unigui-1.9.1/setup.cfg
+-rw-rw-r--   0 george    (1000) george    (1000)    18934 2023-07-17 14:52:22.000000 unigui-1.9.1/README.md
+-rw-rw-r--   0 george    (1000) george    (1000)       43 2021-04-23 05:55:14.000000 unigui-1.9.1/MANIFEST.in
+drwxrwxr-x   0 george    (1000) george    (1000)        0 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui.egg-info/
+-rw-rw-r--   0 george    (1000) george    (1000)       54 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui.egg-info/requires.txt
+-rw-r--r--   0 george    (1000) george    (1000)        1 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui.egg-info/dependency_links.txt
+-rw-r--r--   0 george    (1000) george    (1000)    19239 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui.egg-info/PKG-INFO
+-rw-r--r--   0 george    (1000) george    (1000)        1 2020-12-06 17:27:14.000000 unigui-1.9.1/unigui.egg-info/not-zip-safe
+-rw-r--r--   0 george    (1000) george    (1000)     1342 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui.egg-info/SOURCES.txt
+-rw-r--r--   0 george    (1000) george    (1000)        7 2023-07-22 23:32:35.000000 unigui-1.9.1/unigui.egg-info/top_level.txt
```

### Comparing `unigui-1.9.0/unigui/guielements.py` & `unigui-1.9.1/unigui/guielements.py`

 * *Files 3% similar despite different names*

```diff
@@ -10,19 +10,14 @@
             self.changed = args[2]
         for key in kwargs.keys():            
             self.add(key, kwargs[key]) 
         
     def add(self, attr, value):
         setattr(self, attr, value) 
 
-    def check(self,*attr_names):
-        for name in attr_names:
-            if not hasattr(self,name):
-                raise AttributeError(name, self)
-
     def mutate(self, obj):
         self.__dict__ = obj.__dict__    
 
     def accept(self, value):
         if hasattr(self, 'changed'):
             self.changed(self, value)
         else:
@@ -109,20 +104,24 @@
         self.type='graph'
         if not hasattr(self,'value'):
             self.value = graph_default_value
         if not hasattr(self,'minwidth'):
             self.minwidth = 600.0              
         if not hasattr(self,'minheight'):
             self.minheight = 600.0              
-        self.check('nodes', 'edges')
+        if not hasattr(self, 'nodes'):
+            self.nodes = []
+        if not hasattr(self, 'edges'):
+            self.edges = []
 
 class Switch(Gui):
     def __init__(self, *args, **kwargs):
         super().__init__(*args, **kwargs)
-        self.check('value')        
+        if not hasattr(self,'value'):
+            self.value = False
 
 list_types = ['toggles','list','dropdown']
 
 class Select(Gui):
     def __init__(self, *args, **kwargs):
         super().__init__(*args, **kwargs)
         if not hasattr(self,'options'):             
@@ -175,15 +174,16 @@
         new_row[0] = search
     table.rows.append(new_row)
     return new_row
 
 class Table(Gui):
     def __init__(self, *args, **kwargs):
         super().__init__(*args, **kwargs)             
-        self.check('headers')
+        if not hasattr(self,'headers'):
+            self.headers = []
         if not hasattr(self,'type'):
             self.type = 'table'
         if not hasattr(self,'value'):
             self.value = None
         if not hasattr(self,'rows'):
             self.rows = []
         if not hasattr(self,'value'):
@@ -209,22 +209,21 @@
 class Block(Gui):
     def __init__(self, *args, **kwargs):        
         self.name = args[0]        
         self.type = 'block'
         self.value = list(args[1:])
         for key in kwargs.keys():            
             self.add(key, kwargs[key])        
-        self.check()
 
     def check(self):
         ch_names = set()        
         for child in utils.flatten(self.value):            
             if child.name in ch_names:                        
-                raise Exception(f'Error: the block {self.name} contains a duplicated name {child.name}!')                        
-            ch_names.add(child.name)            
+                return f'The block {self.name} contains a duplicated element name "{child.name}"!'                        
+            ch_names.add(child.name)                
 
 class Dialog:  
     def __init__(self, name, callback, *content, buttons = ['Ok', 'Cancel'], icon = 'not_listed_location'):
         self.name = name
         self.callback = callback  
         self.type = 'dialog'         
         self.buttons = buttons
@@ -243,10 +242,12 @@
             self.add(key, kwargs[key])   
         self.type = 'screen'
 
     def check(self):
         bl_names = set()        
         for bl in utils.flatten(self.blocks):                                    
             if bl.name in bl_names:
-                raise Exception(f'Error: the screen {self.name} contains a duplicated name {bl.name}!')                
+                return (f'The screen {self.name} contains a duplicated block name {bl.name}!')                
             bl_names.add(bl.name)
-            bl.check()    
+            errstr = bl.check()    
+            if errstr:
+                return errstr
```

### Comparing `unigui-1.9.0/unigui/server.py` & `unigui-1.9.1/unigui/server.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from aiohttp import web, WSMsgType
 from .users import *
 from pathlib import Path
 from .reloader import empty_app 
-from .autotest import recorder, jsonString
+from .autotest import recorder, jsonString, run_tests
 from config import port, upload_dir
 from .utils import app_dir
 import traceback
 
 async def post_handler(request):
     reader = await request.multipart()
     field = await reader.next()   
@@ -65,16 +65,19 @@
     return ws       
 
 def start(appname = '', user_type = User, http_handlers = []):
     if appname:
         config.appname = appname
 
     User.UserType = user_type    
-    http_handlers.insert(0, web.get('/ws', websocket_handler))
-        
+
+    if config.autotest:
+        run_tests()
+
+    http_handlers.insert(0, web.get('/ws', websocket_handler))        
     for h in [web.static(f'/{config.upload_dir}', f"/{app_dir}/{upload_dir}"), 
         web.get('/{tail:.*}', static_serve), web.post('/', post_handler)]:
         http_handlers.append(h)
 
     print(f'Start {appname} server on {port} port..')    
     app = web.Application()
     app.add_routes(http_handlers)
```

### Comparing `unigui-1.9.0/unigui/autotest.py` & `unigui-1.9.1/unigui/autotest.py`

 * *Files 6% similar despite different names*

```diff
@@ -31,113 +31,114 @@
 logfile = config.logfile
 handlers = [logging.FileHandler(logfile), logging.StreamHandler()] if logfile else []
 logging.basicConfig(level = logging.WARNING, format = format, handlers = handlers)
 
 record_file = None
 ignored_1message = False
 record_buffer = []
+comparator = Compare().check
 
 def jsonString(obj):
     pretty = config.pretty_print
     return toJson(obj, 2 if pretty else 0, pretty)
 
 def recorder(msg, response):
     if record_file:
         global ignored_1message, record_buffer
         if ignored_1message:            
             record_buffer.append(f"{jsonString(msg)},\
                 \n{'null' if response is None else jsonString(response)}\n")
         else: #start for setting screen
             record_buffer.append(jsonString(['root', User.last_user.screen_module.name]))
-            ignored_1message = True
+            ignored_1message = True    
 
-if config.autotest:
+def obj2pyjson(obj):
+    return json.loads(jsonpickle.encode(obj,unpicklable=False))
+
+def test(filename, user):
+    filepath = f'{testdir}{divpath}{filename}'
+    file = open(filepath, "r") 
+    data = json.loads(file.read())
+    for message in data:
+        if isinstance(message, list):
+            result = user.result4message(message)
+            response = user.prepare_result(result)
+            user_message = message
+        else:
+            diff = comparator(obj2pyjson(response), message)
+            if diff != NO_DIFF:
+                err = diff.get('_message')
+                if not err:
+                    err = diff['type']['_message']
+                print(f"\nTest {filename} is failed on message {user_message}!\n {err}\n")
+                return False
+    return True
+
+test_name = Edit('Name test file', '', focus = True)
+rewrite = Switch('Overwrite existing', False, type = 'check')
+
+def button_clicked(x,y):
+    test_name.value = ''
+    test_name.complete = smart_complete(os.listdir(testdir))
+    return Dialog('Create autotest..', ask_create_test, test_name, rewrite)
+
+def stop_recording(_, x):
+    global record_file, record_buffer, button
+    button.mode = None
+    button.changed = button_clicked
+    button.tooltip = 'Create autotest'
+    with open(record_file, mode='w') as file:    
+        content = ',\n'.join(record_buffer)
+        file.write(f"[\n{content}]")
+    test_name = record_file
+    record_file = None
+    return Info(f'Test {test_name} is created.', button)
+
+def create_test(fname):
+    fname = f'{testdir}/{fname}'
     if not os.path.exists(testdir):
         os.makedirs(testdir)
-    user = User()
-    user.load()
-    comparator = Compare()
+    if os.path.exists(fname) and not rewrite.value:
+        return Warning(f'Test file {fname} already exists!')              
+    global record_file, ignored_1message, record_buffer
+    record_file = fname
+    button.mode = 'red'   
+    button.tooltip = 'Stop test recording'
+    button.changed = stop_recording
+    ignored_1message = False
+    record_buffer = []
+    return Info('Recording is running.. ',button)     
+
+def ask_create_test(_, bname):
+    if bname == 'Ok':            
+        return create_test(test_name.value) if test_name.value else\
+            Warning('Test file name is not defined!')
 
-    def obj2pyjson(obj):
-        return json.loads(jsonpickle.encode(obj,unpicklable=False))
-
-    def test(filename):
-        filepath = f'{testdir}{divpath}{filename}'
-        file = open(filepath, "r") 
-        data = json.loads(file.read())
-        for message in data:
-            if isinstance(message, list):
-                result = user.result4message(message)
-                response = user.prepare_result(result)
-                user_message = message
-            else:
-                diff = comparator.check(obj2pyjson(response), message)
-                if diff != NO_DIFF:
-                    err = diff.get('_message')
-                    if not err:
-                        err = diff['type']['_message']
-                    print(f"\nTest {filename} is failed on message {user_message}!\n {err}\n")
-                    return False
-        return True
-
-    test_name = Edit('Name test file', '', focus = True)
-    rewrite = Switch('Overwrite existing', False, type = 'check')
-
-    def button_clicked(x,y):
-        test_name.value = ''
-        test_name.complete = smart_complete(os.listdir(testdir))
-        return Dialog('Create autotest..', ask_create_test, test_name, rewrite)
-
-    def stop_recording(_, x):
-        global record_file, record_buffer, button
-        button.mode = None
-        button.changed = button_clicked
-        button.tooltip = 'Create autotest'
-        with open(record_file, mode='w') as file:    
-            content = ',\n'.join(record_buffer)
-            file.write(f"[\n{content}]")
-        test_name = record_file
-        record_file = None
-        return Info(f'Test {test_name} is created.', button)
-
-    def create_test(fname):
-        fname = f'{testdir}/{fname}'
-        if not os.path.exists(testdir):
-            os.makedirs(testdir)
-        if os.path.exists(fname) and not rewrite.value:
-            return Warning(f'Test file {fname} already exists!')              
-        global record_file, ignored_1message, record_buffer
-        record_file = fname
-        button.mode = 'red'   
-        button.tooltip = 'Stop recording test'
-        button.changed = stop_recording
-        ignored_1message = False
-        record_buffer = []
-        return button     
-
-    def ask_create_test(_, bname):
-        if bname == 'Ok':            
-            return create_test(test_name.value) if test_name.value else\
-                Warning('Test file name is not defined!')
-
-    button = Button('_Add test', button_clicked, 
-            icon='data_saver_on', tooltip='Create autotest')
-                                    
-    User.toolbar.append(button)
+button = Button('_Add test', button_clicked, 
+        icon='data_saver_on', tooltip='Create autotest')
     
-    #run all
+def run_tests():
+    user = User.UserType()
+    user.load()
+
+    for module in user.screens:
+        teststr = module.screen.check()
+        if teststr:
+            print(f'Detected error in screen {module.__file__}:\n{teststr}')
     files = config.autotest
     ok = True
     process = False
     for file in os.listdir(testdir):
         if not os.path.isdir(file) and (files == '*' or file in files):
             process = True
-            if not test(file):
+            if not test(file,user):
                 ok = False
     if process and ok:
         print('-----Autotests successfully passed.-----')
 
-
+    if not os.path.exists(testdir):
+        os.makedirs(testdir)                                
+    User.toolbar.append(button)
```

### Comparing `unigui-1.9.0/unigui/utils.py` & `unigui-1.9.1/unigui/utils.py`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/reloader.py` & `unigui-1.9.1/unigui/reloader.py`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/users.py` & `unigui-1.9.1/unigui/users.py`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/favicon.ico` & `unigui-1.9.1/unigui/web/favicon.ico`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/css/vendor.191faa77.css` & `unigui-1.9.1/unigui/web/css/vendor.191faa77.css`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/css/vendor.191faa77.css.gz` & `unigui-1.9.1/unigui/web/css/vendor.191faa77.css.gz`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/icons/favicon-96x96.png` & `unigui-1.9.1/unigui/web/icons/favicon-96x96.png`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/icons/favicon-16x16.png` & `unigui-1.9.1/unigui/web/icons/favicon-16x16.png`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/icons/favicon-32x32.png` & `unigui-1.9.1/unigui/web/icons/favicon-32x32.png`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/icons/favicon-128x128.png` & `unigui-1.9.1/unigui/web/icons/favicon-128x128.png`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/fonts/flUhRq6tzZclQEJ-Vdg-IuiaDsNcIhQ8tQ.c5371cfb.woff2` & `unigui-1.9.1/unigui/web/fonts/flUhRq6tzZclQEJ-Vdg-IuiaDsNcIhQ8tQ.c5371cfb.woff2`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/fonts/flUhRq6tzZclQEJ-Vdg-IuiaDsNa.4d73cb90.woff` & `unigui-1.9.1/unigui/web/fonts/flUhRq6tzZclQEJ-Vdg-IuiaDsNa.4d73cb90.woff`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/fonts/KFOmCnqEu92Fr1Mu4mxM.f1e2a767.woff` & `unigui-1.9.1/unigui/web/fonts/KFOmCnqEu92Fr1Mu4mxM.f1e2a767.woff`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/fonts/KFOlCnqEu92Fr1MmSU5fBBc-.c2f7ab22.woff` & `unigui-1.9.1/unigui/web/fonts/KFOlCnqEu92Fr1MmSU5fBBc-.c2f7ab22.woff`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/fonts/KFOlCnqEu92Fr1MmWUlfBBc-.77ecb942.woff` & `unigui-1.9.1/unigui/web/fonts/KFOlCnqEu92Fr1MmWUlfBBc-.77ecb942.woff`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/fonts/KFOlCnqEu92Fr1MmYUtfBBc-.f5677eb2.woff` & `unigui-1.9.1/unigui/web/fonts/KFOlCnqEu92Fr1MmYUtfBBc-.f5677eb2.woff`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/fonts/KFOlCnqEu92Fr1MmEU9fBBc-.48af7707.woff` & `unigui-1.9.1/unigui/web/fonts/KFOlCnqEu92Fr1MmEU9fBBc-.48af7707.woff`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/fonts/KFOkCnqEu92Fr1MmgVxIIzQ.68bb21d0.woff` & `unigui-1.9.1/unigui/web/fonts/KFOkCnqEu92Fr1MmgVxIIzQ.68bb21d0.woff`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/js/615.04cc6ad4.js` & `unigui-1.9.1/unigui/web/js/9.100130f6.js`

 * *Files 9% similar despite different names*

#### js-beautify {}

```diff
@@ -1,119 +1,144 @@
 "use strict";
 (globalThis["webpackChunkuniqua"] = globalThis["webpackChunkuniqua"] || []).push([
-    [615], {
-        9615: (e, t, a) => {
+    [9], {
+        6009: (e, t, a) => {
             a.r(t), a.d(t, {
-                default: () => sa
+                default: () => la
             });
-            var l = a(3673),
-                s = a(2323);
-            const i = (0, l._)("div", {
-                    class: "q-pa-lg"
+            var s = a(3673),
+                l = a(2323);
+            const i = (0, s._)("div", {
+                    class: "q-pa-md"
                 }, null, -1),
-                n = (0, l._)("div", {
-                    class: "q-pa-lg"
+                n = (0, s._)("div", {
+                    class: "q-pa-md"
                 }, null, -1);
 
             function o(e, t, a, o, d, r) {
-                const c = (0, l.up)("q-item-label"),
-                    h = (0, l.up)("element"),
-                    u = (0, l.up)("q-tab"),
-                    p = (0, l.up)("q-tabs"),
-                    g = (0, l.up)("q-toolbar"),
-                    m = (0, l.up)("q-header"),
-                    f = (0, l.up)("zone"),
-                    y = (0, l.up)("q-page"),
-                    w = (0, l.up)("q-page-container"),
-                    b = (0, l.up)("q-layout");
-                return (0, l.wg)(), (0, l.j4)(b, {
+                const c = (0, s.up)("q-item-label"),
+                    h = (0, s.up)("element"),
+                    u = (0, s.up)("q-tab"),
+                    p = (0, s.up)("q-tabs"),
+                    g = (0, s.up)("q-space"),
+                    m = (0, s.up)("q-tooltip"),
+                    f = (0, s.up)("q-btn"),
+                    y = (0, s.up)("q-toolbar"),
+                    w = (0, s.up)("q-header"),
+                    b = (0, s.up)("zone"),
+                    k = (0, s.up)("q-page"),
+                    v = (0, s.up)("q-page-container"),
+                    x = (0, s.up)("q-layout");
+                return (0, s.wg)(), (0, s.j4)(x, {
                     view: "lHh Lpr lFf"
                 }, {
-                    default: (0, l.w5)((() => [(0, l.Wm)(m, {
-                        elevated: ""
+                    default: (0, s.w5)((() => [(0, s.Wm)(w, {
+                        elevated: "",
+                        class: (0, l.C_)({
+                            "bg-deep-purple-9": e.Dark.isActive
+                        })
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Wm)(g, null, {
-                            default: (0, l.w5)((() => [(0, l.Wm)(c, {
+                        default: (0, s.w5)((() => [(0, s.Wm)(y, null, {
+                            default: (0, s.w5)((() => [(0, s.Wm)(c, {
                                 class: "text-h5"
                             }, {
-                                default: (0, l.w5)((() => [(0, l.Uk)((0, s.zw)(e.screen.header ? e.screen.header : ""), 1)])),
+                                default: (0, s.w5)((() => [(0, s.Uk)((0, l.zw)(e.screen.header ? e.screen.header : ""), 1)])),
                                 _: 1
-                            }), i, ((0, l.wg)(!0), (0, l.iD)(l.HY, null, (0, l.Ko)(e.screen.toolbar, (t => ((0, l.wg)(), (0, l.j4)(h, {
-                                class: "q-ma-xs bg-blue-5",
+                            }), i, ((0, s.wg)(!0), (0, s.iD)(s.HY, null, (0, s.Ko)(e.screen.toolbar, (t => ((0, s.wg)(), (0, s.j4)(h, {
+                                class: (0, l.C_)(["q-ma-xs", {
+                                    "bg-blue-grey-7": e.Dark.isActive,
+                                    "bg-blue-5": !e.Dark.isActive
+                                }]),
                                 data: t,
                                 pdata: e.tooldata
-                            }, null, 8, ["data", "pdata"])))), 256)), n, (0, l.Wm)(p, {
-                                class: "text-teal",
+                            }, null, 8, ["class", "data", "pdata"])))), 256)), n, (0, s.Wm)(p, {
+                                class: "bold-tabs",
                                 align: "center",
                                 "inline-label": "",
                                 dense: "",
                                 modelValue: e.tab,
                                 "onUpdate:modelValue": t[0] || (t[0] = t => e.tab = t),
                                 style: {
                                     float: "center"
                                 }
                             }, {
-                                default: (0, l.w5)((() => [((0, l.wg)(!0), (0, l.iD)(l.HY, null, (0, l.Ko)(e.menu, (t => ((0, l.wg)(), (0, l.iD)("div", null, [t.icon ? ((0, l.wg)(), (0, l.j4)(u, {
+                                default: (0, s.w5)((() => [((0, s.wg)(!0), (0, s.iD)(s.HY, null, (0, s.Ko)(e.menu, (t => ((0, s.wg)(), (0, s.iD)("div", null, [t.icon ? ((0, s.wg)(), (0, s.j4)(u, {
                                     key: 0,
                                     class: "justify-center text-white shadow-2",
                                     "no-caps": "",
                                     name: t.name,
                                     icon: t.icon,
                                     label: t.name,
                                     onClick: a => e.tabclick(t.name)
-                                }, null, 8, ["name", "icon", "label", "onClick"])) : (0, l.kq)("", !0), t.icon ? (0, l.kq)("", !0) : ((0, l.wg)(), (0, l.j4)(u, {
+                                }, null, 8, ["name", "icon", "label", "onClick"])) : (0, s.kq)("", !0), t.icon ? (0, s.kq)("", !0) : ((0, s.wg)(), (0, s.j4)(u, {
                                     key: 1,
                                     class: "justify-center text-white shadow-2",
                                     "no-caps": "",
                                     name: t.name,
                                     label: t.name,
                                     onClick: a => e.tabclick(t.name)
                                 }, null, 8, ["name", "label", "onClick"]))])))), 256))])),
                                 _: 1
-                            }, 8, ["modelValue"])])),
+                            }, 8, ["modelValue"]), (0, s.Wm)(g), (0, s.Wm)(f, {
+                                "no-caps": "",
+                                dense: "",
+                                round: "",
+                                icon: e.Dark.isActive ? "light_mode" : "dark_mode",
+                                onClick: t[1] || (t[1] = t => e.Dark.set(!e.Dark.isActive))
+                            }, {
+                                default: (0, s.w5)((() => [(0, s.Wm)(m, {
+                                    class: "text-body2"
+                                }, {
+                                    default: (0, s.w5)((() => [(0, s.Uk)("Dark/Light mode")])),
+                                    _: 1
+                                })])),
+                                _: 1
+                            }, 8, ["icon"])])),
                             _: 1
                         })])),
                         _: 1
-                    }), (0, l.Wm)(w, null, {
-                        default: (0, l.w5)((() => [(0, l.Wm)(y, {
+                    }, 8, ["class"]), (0, s.Wm)(v, {
+                        class: "content"
+                    }, {
+                        default: (0, s.w5)((() => [(0, s.Wm)(k, {
                             class: "flex justify-center centers"
                         }, {
-                            default: (0, l.w5)((() => [(0, l.Wm)(f, {
+                            default: (0, s.w5)((() => [(0, s.Wm)(b, {
                                 data: e.screen.blocks,
                                 ref: "page"
                             }, null, 8, ["data"])])),
                             _: 1
                         })])),
                         _: 1
                     })])),
                     _: 1
                 })
             }
 
             function d(e, t, a, i, n, o) {
-                const d = (0, l.up)("q-icon"),
-                    r = (0, l.up)("q-item-section"),
-                    c = (0, l.up)("q-item-label"),
-                    h = (0, l.up)("q-item");
-                return (0, l.wg)(), (0, l.j4)(h, {
+                const d = (0, s.up)("q-icon"),
+                    r = (0, s.up)("q-item-section"),
+                    c = (0, s.up)("q-item-label"),
+                    h = (0, s.up)("q-item");
+                return (0, s.wg)(), (0, s.j4)(h, {
                     clickable: "",
                     tag: "a",
                     target: "_blank",
                     onClick: e.send
                 }, {
-                    default: (0, l.w5)((() => [(0, l.Wm)(r, {
+                    default: (0, s.w5)((() => [(0, s.Wm)(r, {
                         avatar: ""
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Wm)(d, {
+                        default: (0, s.w5)((() => [(0, s.Wm)(d, {
                             name: e.icon
                         }, null, 8, ["name"])])),
                         _: 1
-                    }), (0, l.Wm)(r, null, {
-                        default: (0, l.w5)((() => [(0, l.Wm)(c, null, {
-                            default: (0, l.w5)((() => [(0, l.Uk)((0, s.zw)(e.name), 1)])),
+                    }), (0, s.Wm)(r, null, {
+                        default: (0, s.w5)((() => [(0, s.Wm)(c, null, {
+                            default: (0, s.w5)((() => [(0, s.Uk)((0, l.zw)(e.name), 1)])),
                             _: 1
                         })])),
                         _: 1
                     })])),
                     _: 1
                 }, 8, ["onClick"])
             }
@@ -134,276 +159,277 @@
                 return `height: ${t}px; width: ${a}px`
             }
             const b = window.location.host,
                 k = `${window.location.protocol}//${b}`;
             console.log(k);
             const v = !1;
             let C = {},
-                q = {},
-                _ = {};
+                _ = {},
+                q = {};
 
-            function j(e) {
+            function A(e) {
                 p = new WebSocket(v ? "ws://localhost:8000/ws" : `ws://${b}/ws`), p.onopen = () => e.statusConnect = !0, p.onmessage = t => {
                     g && console.log("incoming message", t.data), e.processMessage(JSON.parse(t.data))
                 }, p.onerror = t => e.error(t), p.onclose = t => {
                     t.wasClean ? e.info("Connection was finished by the server.") : e.error("Connection suddenly closed!"), e.statusConnect = !1, g && console.info("close code : " + t.code + " reason: " + t.reason)
                 }, h = e
             }
 
-            function S(e) {
+            function D(e) {
                 console.log("sended", e), p.send(JSON.stringify(e))
             }
-            let z, A = 0,
-                Z = !0;
+            let S, j = 0,
+                z = !0;
 
-            function $(e) {
-                Z = e, e || (_ = {})
+            function Z(e) {
+                z = e, e || (q = {})
             }
 
-            function D(e, t) {
-                if (Z) {
-                    let t = _[e];
-                    if (t) return t.styleSize;
-                    Z = !1
+            function $(e) {
+                if (z) {
+                    let t = e.pdata ? `${e.data.name}@${e.pdata.name}` : `_scroll@${e.data.name}`,
+                        a = q[t];
+                    if (a) return a.styleSize;
+                    z = !1
                 }
-                return w(t)
+                return w(e.data)
             }
 
-            function M(e, t, a, l = "complete") {
-                let s = ++A,
-                    i = [e.pdata.name, e.data.name, l, t, s];
-                S(i), u[s] = a
+            function M(e, t, a, s = "complete") {
+                let l = ++j,
+                    i = [e.pdata.name, e.data.name, s, t, l];
+                D(i), u[l] = a
             }
 
             function V() {
-                C = {}, _ = q, Z = !0, q = {}
+                C = {}, q = _, z = !0, _ = {}
             }
 
             function E(e, t) {
                 Object.assign(e.data, t), e.updated = t.value, e.value = t.value
             }
 
-            function K(e) {
+            function W(e) {
                 for (let t of e) {
                     let e = t.path;
                     if (e.length > 1) {
                         e.reverse();
                         let a = e.join("@"),
-                            l = q[a];
-                        E(l, t.data)
+                            s = _[a];
+                        E(s, t.data)
                     } else {
                         let a = C[e[0]];
                         Object.assign(a.data, t.data)
                     }
                 }
             }
 
-            function W(e) {
+            function K(e) {
                 "string" == typeof e.value ? h.error(e.value) : u[e.id](e.value), delete u[e.id]
             }
 
-            function O(e) {
+            function Q(e) {
                 let t = [];
-                for (let l of e) l instanceof Array ? t.push(l) : t.push([l]);
+                for (let s of e) s instanceof Array ? t.push(s) : t.push([s]);
                 let a = t.shift();
                 return t.reduce(((e, t) => e.flatMap((e => t.map((t => e instanceof Array ? [...e, t] : [e, t]))))), a)
             }
 
-            function Q() {
-                for (let [e, t] of Object.entries(q)) t.expanding && (t.styleSize = w(t.data));
-                (0, l.Y3)((() => {
+            function O() {
+                for (let [e, t] of Object.entries(_)) t.expanding && (t.styleSize = w(t.data));
+                (0, s.Y3)((() => {
                     requestAnimationFrame((() => {
                         requestAnimationFrame((() => {
                             U()
                         }))
                     }))
                 }))
             }
-            let H = (0, c.debounce)(Q, 200);
+            let H = (0, c.debounce)(O, 200);
 
             function U(e) {
-                Array.isArray(e) && (e = null), z && (z.disconnect(), z = null), g && console.log("------------------recalc design");
+                Array.isArray(e) && (e = null), S && (S.disconnect(), S = null), g && console.log("------------------recalc design");
                 const t = N(e),
                     a = F(e);
-                for (let [l, s] of Object.entries(t)) {
-                    let e = q[l];
-                    const [t, i] = a[l];
+                for (let [s, l] of Object.entries(t)) {
+                    let e = _[s];
+                    const [t, i] = a[s];
                     let n, o = e.geom().el,
                         d = e.pdata ? e.pdata.name : e.name,
                         r = C[d];
                     for (let a of r.data.value.slice(1))
                         if (Array.isArray(a)) {
                             if (a.find((t => t.name == e.data.name))) {
                                 let e = a[a.length - 1],
                                     t = `${e.name}@${d}`;
-                                n = q[t];
+                                n = _[t];
                                 break
                             }
                         } else if (a.name == e.data.name) {
                         n = e;
                         break
                     }
                     let c = r.data.width ? r.data.width - o.clientWidth - t : r.$el.getBoundingClientRect().right - (n ? n.geom().right : e.geom().right);
                     c /= i;
-                    let h = l.startsWith("_scroll@") ? e.geom().inner.clientHeight : o.clientHeight;
-                    e.styleSize = `height: ${h+s}px; width: ${o.clientWidth+c+t}px;`
+                    let h = s.startsWith("_scroll@") ? e.geom().inner.clientHeight : o.clientHeight;
+                    e.styleSize = `height: ${h+l}px; width: ${o.clientWidth+c+t}px;`
                 }
             }
 
             function N(e) {
                 const t = h.screen.blocks;
                 let a = window.innerHeight;
-                a += 5;
-                let l = {},
-                    s = new Map,
+                a += 14;
+                let s = {},
+                    l = new Map,
                     i = {};
                 for (let [d, r] of Object.entries(C)) i[r.name] = r.$el.getBoundingClientRect().height;
                 let n = [];
                 for (let d of t) {
                     const e = [];
                     let t = d instanceof Array,
-                        o = t ? O(d) : [
+                        o = t ? Q(d) : [
                             [d]
                         ];
                     for (let a of o) {
                         let e = 0;
-                        for (let t of a) e += i[t.name] + 8;
+                        for (let t of a) e += i[t.name] + 12;
                         n.push([e, a])
                     }
                     n.sort(((e, t) => e[0] > t[0] ? -1 : e[0] == t[0] ? 0 : 1));
-                    for (let l of n) {
-                        let t = l[1];
+                    for (let s of n) {
+                        let t = s[1];
                         (0, r.hu)(Array.isArray(t));
                         const i = [];
-                        for (let [e, a] of Object.entries(q))
+                        for (let [e, a] of Object.entries(_))
                             if (a.expanding_height) {
-                                let [l, n] = e.split("@");
+                                let [s, n] = e.split("@");
                                 if (t.find((e => e.name == n))) {
                                     let e = !0;
                                     const t = a.geom();
-                                    for (let [l, n] of i.entries()) {
+                                    for (let [s, n] of i.entries()) {
                                         let o = n.geom();
                                         if (n !== a && o.top == t.top) {
-                                            o.scrollHeight < t.scrollHeight && (i[l] = a), e = !1, s.set(a.fullname, n.fullname);
+                                            o.scrollHeight < t.scrollHeight && (i[s] = a), e = !1, l.set(a.fullname, n.fullname);
                                             break
                                         }
                                     }
                                     e && i.push(a)
                                 }
-                            } i.length && e.push([a - l[0] - 64, i])
+                            } i.length && e.push([a - s[0] - 64, i])
                     }
-                    for (let [a, s] of e) {
-                        s.sort(((e, t) => e.geom().scrollHeight < t.geom().scrollHeight));
-                        let e = s.length;
-                        for (let i of s) i.fullname in l && (e--, a -= l[i.fullname]);
+                    for (let [a, l] of e) {
+                        l.sort(((e, t) => e.geom().scrollHeight < t.geom().scrollHeight));
+                        let e = l.length;
+                        for (let i of l) i.fullname in s && (e--, a -= s[i.fullname]);
                         let t = 0;
-                        for (let i of s)
-                            if (!(i.fullname in l)) {
-                                let s, n = a / e;
-                                if (1 == e) s = n;
-                                else if (s = Math.floor(n), n - s) {
-                                    t += n - s;
+                        for (let i of l)
+                            if (!(i.fullname in s)) {
+                                let l, n = a / e;
+                                if (1 == e) l = n;
+                                else if (l = Math.floor(n), n - l) {
+                                    t += n - l;
                                     let e = Math.round(t) - t;
-                                    e < .001 && e > -.001 && (s += Math.round(t), t = 0)
+                                    e < .001 && e > -.001 && (l += Math.round(t), t = 0)
                                 }
-                                "docviewer" == i.type ? l[i.fullname] = s + 4 : l[i.fullname] = s
+                                "docviewer" == i.type ? s[i.fullname] = l + 4 : s[i.fullname] = l
                             }
                     }
                 }
-                let o = Array.from(s.entries());
-                o.sort(((e, t) => e[0] in l || e[1] in l ? -1 : 1));
-                for (let [d, r] of o) r in l ? l[d] = l[r] : l[r] = l[d];
-                return l
+                let o = Array.from(l.entries());
+                o.sort(((e, t) => e[0] in s || e[1] in s ? -1 : 1));
+                for (let [d, r] of o) r in s ? s[d] = s[r] : s[r] = s[d];
+                return s
             }
 
             function F(e) {
                 e = null;
                 const t = e ? [e] : h.screen.blocks;
                 let a = window.innerWidth - 15,
-                    l = [],
-                    s = {};
+                    s = [],
+                    l = {};
                 for (let o of t)
-                    if (0 == l.length)
+                    if (0 == s.length)
                         if (Array.isArray(o))
-                            for (let e of o) l.push(Array.isArray(e) ? e : [e]);
-                        else l = [
+                            for (let e of o) s.push(Array.isArray(e) ? e : [e]);
+                        else s = [
                             [o]
                         ];
                 else {
                     let e = [];
                     if (Array.isArray(o))
                         for (let t of o)
-                            for (let a of l) e.push(Array.isArray(t) ? a.concat(t) : [...a, t]);
+                            for (let a of s) e.push(Array.isArray(t) ? a.concat(t) : [...a, t]);
                     else
-                        for (let t of l) e.push([...t, o]);
-                    l = e
+                        for (let t of s) e.push([...t, o]);
+                    s = e
                 }
-                l.sort(((e, t) => e.length > t.length ? -1 : e.length == t.length ? 0 : 1));
+                s.sort(((e, t) => e.length > t.length ? -1 : e.length == t.length ? 0 : 1));
                 const i = [];
                 let n = new Map;
-                for (let o of l) {
+                for (let o of s) {
                     let e = Array.isArray(o) ? o[o.length - 1] : o,
                         t = C[e.name].$el.getBoundingClientRect().right;
                     e = Array.isArray(o) ? o[0] : o;
-                    let l = C[e.name].$el.getBoundingClientRect().left,
-                        s = a - t + l - 10;
+                    let s = C[e.name].$el.getBoundingClientRect().left,
+                        l = a - t + s - 10;
                     const d = [];
-                    for (let [a, i] of Object.entries(q))
+                    for (let [a, i] of Object.entries(_))
                         if (i.expanding_width) {
                             let e = a.split("@")[1];
                             if (o.find((t => t.name == e))) {
                                 let e = !0,
                                     t = i.geom().left;
-                                for (let [a, l] of d.entries())
-                                    if (l !== i && l.geom().left == t) {
-                                        l.geom().scrollWidth < i.geom().scrollWidth ? (d[a] = i, n.set(l.fullname, i.fullname)) : n.set(i.fullname, l.fullname), e = !1;
+                                for (let [a, s] of d.entries())
+                                    if (s !== i && s.geom().left == t) {
+                                        s.geom().scrollWidth < i.geom().scrollWidth ? (d[a] = i, n.set(s.fullname, i.fullname)) : n.set(i.fullname, s.fullname), e = !1;
                                         break
                                     } e && d.push(i)
                             }
-                        } d.length && i.push([s, d])
+                        } d.length && i.push([l, d])
                 }
                 for (let [o, d] of i) {
                     d.sort(((e, t) => e.geom().scrollWidth - t.geom().scrollWidth));
                     let e = d.length,
                         t = {};
                     for (let a = 0; a < d.length; a++) {
-                        let l = d[a],
-                            i = l.parent_name,
-                            n = i || l.name;
-                        if (t[n] ? t[n]++ : t[n] = 1, n = l.parent_name, n) {
+                        let s = d[a],
+                            i = s.parent_name,
+                            n = i || s.name;
+                        if (t[n] ? t[n]++ : t[n] = 1, n = s.parent_name, n) {
                             let e = C[n];
                             if (e.data.width) {
                                 let t = a + 1,
                                     i = d[t];
                                 if (i && i.parent_name != n) {
-                                    let t = l.geom().right - l.geom().left,
+                                    let t = s.geom().right - s.geom().left,
                                         a = e.data.width - t;
-                                    s[l.fullname] = [a, 1]
+                                    l[s.fullname] = [a, 1]
                                 }
                             }
                         }
-                        let r = s[l.fullname];
+                        let r = l[s.fullname];
                         r && (e--, o -= r[0] / r[1])
                     }
                     for (let a of d) {
-                        let l = s[a.fullname];
-                        if (void 0 === l) {
-                            let l = a.pdata ? a.pdata.name : a.name;
-                            s[a.fullname] = [Math.floor(o / e), t[l]]
+                        let s = l[a.fullname];
+                        if (void 0 === s) {
+                            let s = a.pdata ? a.pdata.name : a.name;
+                            l[a.fullname] = [Math.floor(o / e), t[s]]
                         }
                     }
                 }
-                for (let [o, d] of n.entries()) d in s ? s[o] = s[d] : s[d] = s[o];
-                return s
+                for (let [o, d] of n.entries()) d in l ? l[o] = l[d] : l[d] = l[o];
+                return l
             }
-            const T = (0, l.aZ)({
+            const T = (0, s.aZ)({
                 name: "menubar",
                 methods: {
                     send() {
-                        S(["root", this.name])
+                        D(["root", this.name])
                     }
                 },
                 props: {
                     name: {
                         type: String,
                         required: !0
                     },
@@ -428,657 +454,707 @@
                 QItem: R.Z,
                 QItemSection: I.Z,
                 QIcon: L.Z,
                 QItemLabel: B.Z
             });
             const ee = {
                     key: 0,
-                    class: "row q-col-gutter-sm q-py-sm"
+                    class: "row q-col-gutter-xs q-py-xs"
                 },
                 te = {
-                    class: "q-col-gutter-sm"
+                    class: "q-col-gutter-xs"
                 },
                 ae = {
                     key: 0,
-                    class: "column q-col-gutter-sm"
+                    class: "column q-col-gutter-xs"
                 };
 
-            function le(e, t, a, s, i, n) {
-                const o = (0, l.up)("zone", !0),
-                    d = (0, l.up)("block");
-                return e.data instanceof Array ? ((0, l.wg)(), (0, l.iD)("div", ee, [((0, l.wg)(!0), (0, l.iD)(l.HY, null, (0, l.Ko)(e.data, (e => ((0, l.wg)(), (0, l.iD)("div", te, [e instanceof Array ? ((0, l.wg)(), (0, l.iD)("div", ae, [((0, l.wg)(!0), (0, l.iD)(l.HY, null, (0, l.Ko)(e, (e => ((0, l.wg)(), (0, l.j4)(o, {
+            function se(e, t, a, l, i, n) {
+                const o = (0, s.up)("zone", !0),
+                    d = (0, s.up)("block");
+                return e.data instanceof Array ? ((0, s.wg)(), (0, s.iD)("div", ee, [((0, s.wg)(!0), (0, s.iD)(s.HY, null, (0, s.Ko)(e.data, (e => ((0, s.wg)(), (0, s.iD)("div", te, [e instanceof Array ? ((0, s.wg)(), (0, s.iD)("div", ae, [((0, s.wg)(!0), (0, s.iD)(s.HY, null, (0, s.Ko)(e, (e => ((0, s.wg)(), (0, s.j4)(o, {
+                    class: "q-col-gutter-xs q-py-xs",
                     data: e
-                }, null, 8, ["data"])))), 256))])) : ((0, l.wg)(), (0, l.j4)(d, {
+                }, null, 8, ["data"])))), 256))])) : ((0, s.wg)(), (0, s.j4)(d, {
                     key: 1,
                     data: e
-                }, null, 8, ["data"]))])))), 256))])) : ((0, l.wg)(), (0, l.j4)(d, {
+                }, null, 8, ["data"]))])))), 256))])) : ((0, s.wg)(), (0, s.j4)(d, {
                     key: 1,
                     data: e.data
                 }, null, 8, ["data"]))
             }
-            const se = {
+            const le = {
                     class: "row"
                 },
-                ie = {
-                    key: 2,
-                    class: "q-ma-sm",
-                    style: {
-                        "font-size": "18px"
-                    }
-                },
-                ne = ["data", "pdata"],
-                oe = {
+                ie = ["data", "pdata"],
+                ne = {
                     key: 0,
                     class: "row"
                 },
-                de = ["data", "pdata"],
-                re = {
+                oe = ["data", "pdata"],
+                de = {
                     key: 0,
                     class: "row"
                 };
 
-            function ce(e, t, a, i, n, o) {
-                const d = (0, l.up)("element"),
-                    r = (0, l.up)("q-icon"),
-                    c = (0, l.up)("q-scroll-area"),
-                    h = (0, l.up)("q-card");
-                return (0, l.wg)(), (0, l.j4)(h, {
+            function re(e, t, a, i, n, o) {
+                const d = (0, s.up)("element"),
+                    r = (0, s.up)("q-icon"),
+                    c = (0, s.up)("q-scroll-area"),
+                    h = (0, s.up)("q-card");
+                return (0, s.wg)(), (0, s.j4)(h, {
                     class: "my-card q-ma-xs"
                 }, {
-                    default: (0, l.w5)((() => [(0, l._)("div", se, [e.data.logo ? ((0, l.wg)(), (0, l.j4)(d, {
+                    default: (0, s.w5)((() => [(0, s._)("div", le, [e.data.logo ? ((0, s.wg)(), (0, s.j4)(d, {
                         key: 0,
+                        class: "q-ma-sm",
                         data: e.data.logo,
                         pdata: e.data
-                    }, null, 8, ["data", "pdata"])) : e.data.icon ? ((0, l.wg)(), (0, l.j4)(r, {
+                    }, null, 8, ["data", "pdata"])) : e.data.icon ? ((0, s.wg)(), (0, s.j4)(r, {
                         key: 1,
+                        class: "q-mt-sm",
                         size: "sm",
                         name: e.data.icon
-                    }, null, 8, ["name"])) : (0, l.kq)("", !0), "_" != e.name[0] ? ((0, l.wg)(), (0, l.iD)("p", ie, (0, s.zw)(e.name), 1)) : (0, l.kq)("", !0), ((0, l.wg)(!0), (0, l.iD)(l.HY, null, (0, l.Ko)(e.tops, (t => ((0, l.wg)(), (0, l.j4)(d, {
+                    }, null, 8, ["name"])) : (0, s.kq)("", !0), "_" != e.name[0] ? ((0, s.wg)(), (0, s.iD)("p", {
+                        key: 2,
+                        class: (0, l.C_)(["q-ma-sm", {
+                            "text-info": e.Dark.isActive,
+                            "text-cyan-10": !e.Dark.isActive
+                        }]),
+                        style: {
+                            "font-size": "18px"
+                        }
+                    }, (0, l.zw)(e.name), 3)) : (0, s.kq)("", !0), ((0, s.wg)(!0), (0, s.iD)(s.HY, null, (0, s.Ko)(e.tops, (t => ((0, s.wg)(), (0, s.j4)(d, {
                         class: "q-ma-xs",
                         data: t,
                         pdata: e.data
-                    }, null, 8, ["data", "pdata"])))), 256))]), e.data.scroll ? ((0, l.wg)(), (0, l.j4)(c, {
+                    }, null, 8, ["data", "pdata"])))), 256))]), e.data.scroll ? ((0, s.wg)(), (0, s.j4)(c, {
                         key: 0,
-                        style: (0, s.j5)(e.styleSize),
+                        style: (0, l.j5)(e.styleSize),
                         "thumb-style": e.thumbStyle,
                         "bar-style": e.barStyle
                     }, {
-                        default: (0, l.w5)((() => [((0, l.wg)(!0), (0, l.iD)(l.HY, null, (0, l.Ko)(e.data.value.slice(1), (t => ((0, l.wg)(), (0, l.iD)("div", {
+                        default: (0, s.w5)((() => [((0, s.wg)(!0), (0, s.iD)(s.HY, null, (0, s.Ko)(e.data.value.slice(1), (t => ((0, s.wg)(), (0, s.iD)("div", {
                             class: "column",
                             data: t,
                             pdata: e.data
-                        }, [t instanceof Array ? ((0, l.wg)(), (0, l.iD)("div", oe, [((0, l.wg)(!0), (0, l.iD)(l.HY, null, (0, l.Ko)(t, (t => ((0, l.wg)(), (0, l.j4)(d, {
+                        }, [t instanceof Array ? ((0, s.wg)(), (0, s.iD)("div", ne, [((0, s.wg)(!0), (0, s.iD)(s.HY, null, (0, s.Ko)(t, (t => ((0, s.wg)(), (0, s.j4)(d, {
                             class: "q-ma-xs",
                             data: t,
                             pdata: e.data
-                        }, null, 8, ["data", "pdata"])))), 256))])) : ((0, l.wg)(), (0, l.j4)(d, {
+                        }, null, 8, ["data", "pdata"])))), 256))])) : ((0, s.wg)(), (0, s.j4)(d, {
                             key: 1,
                             class: "q-ma-xs",
                             data: t,
                             pdata: e.data
-                        }, null, 8, ["data", "pdata"]))], 8, ne)))), 256))])),
+                        }, null, 8, ["data", "pdata"]))], 8, ie)))), 256))])),
                         _: 1
-                    }, 8, ["style", "thumb-style", "bar-style"])) : ((0, l.wg)(!0), (0, l.iD)(l.HY, {
+                    }, 8, ["style", "thumb-style", "bar-style"])) : ((0, s.wg)(!0), (0, s.iD)(s.HY, {
                         key: 1
-                    }, (0, l.Ko)(e.data.value.slice(1), (t => ((0, l.wg)(), (0, l.iD)("div", {
+                    }, (0, s.Ko)(e.data.value.slice(1), (t => ((0, s.wg)(), (0, s.iD)("div", {
                         class: "column",
                         data: t,
                         pdata: e.data
-                    }, [t instanceof Array ? ((0, l.wg)(), (0, l.iD)("div", re, [((0, l.wg)(!0), (0, l.iD)(l.HY, null, (0, l.Ko)(t, (t => ((0, l.wg)(), (0, l.j4)(d, {
+                    }, [t instanceof Array ? ((0, s.wg)(), (0, s.iD)("div", de, [((0, s.wg)(!0), (0, s.iD)(s.HY, null, (0, s.Ko)(t, (t => ((0, s.wg)(), (0, s.j4)(d, {
                         class: "q-ma-xs",
                         data: t,
                         pdata: e.data
-                    }, null, 8, ["data", "pdata"])))), 256))])) : ((0, l.wg)(), (0, l.j4)(d, {
+                    }, null, 8, ["data", "pdata"])))), 256))])) : ((0, s.wg)(), (0, s.j4)(d, {
                         key: 1,
                         class: "q-ma-xs",
                         data: t,
                         pdata: e.data
-                    }, null, 8, ["data", "pdata"]))], 8, de)))), 256))])),
+                    }, null, 8, ["data", "pdata"]))], 8, oe)))), 256))])),
                     _: 1
                 })
             }
-            var he = a(8880);
-            const ue = e => ((0, l.dD)("data-v-9259610c"), e = e(), (0, l.Cn)(), e),
-                pe = {
-                    key: 4
-                },
-                ge = ["width", "height"],
-                me = ["src"],
-                fe = {
+            var ce = a(8880);
+            const he = e => ((0, s.dD)("data-v-591efd84"), e = e(), (0, s.Cn)(), e),
+                ue = {
+                    key: 4,
+                    class: "{'bg-blue-grey-9': Dark.isActive}"
+                },
+                pe = ["width", "height"],
+                ge = ["src"],
+                me = {
                     key: 17,
                     class: "web-camera-container"
                 },
-                ye = {
+                fe = {
                     class: "camera-button"
                 },
-                we = {
+                ye = {
                     key: 0
                 },
-                be = {
+                we = {
                     key: 1
                 },
-                ke = {
+                be = {
                     class: "camera-loading"
                 },
-                ve = ue((() => (0, l._)("ul", {
+                ke = he((() => (0, s._)("ul", {
                     class: "loader-circle"
-                }, [(0, l._)("li"), (0, l._)("li"), (0, l._)("li")], -1))),
-                xe = [ve],
+                }, [(0, s._)("li"), (0, s._)("li"), (0, s._)("li")], -1))),
+                ve = [ke],
+                xe = ["height"],
                 Ce = ["height"],
-                qe = ["height"],
                 _e = {
                     key: 1,
                     class: "camera-shoot"
                 },
-                je = ue((() => (0, l._)("img", {
+                qe = he((() => (0, s._)("img", {
                     src: "https://img.icons8.com/material-outlined/50/000000/camera--v2.png"
                 }, null, -1))),
-                Se = [je],
-                ze = {
+                Ae = [qe],
+                De = {
                     key: 2,
                     class: "camera-download"
                 };
 
-            function Ae(e, t, a, i, n, o) {
-                const d = (0, l.up)("q-icon"),
-                    r = (0, l.up)("q-img"),
-                    c = (0, l.up)("q-badge"),
-                    h = (0, l.up)("q-select"),
-                    u = (0, l.up)("q-checkbox"),
-                    p = (0, l.up)("q-toggle"),
-                    g = (0, l.up)("q-btn"),
-                    m = (0, l.up)("q-btn-toggle"),
-                    f = (0, l.up)("utable"),
-                    y = (0, l.up)("linechart"),
-                    w = (0, l.up)("q-input"),
-                    b = (0, l.up)("q-tree"),
-                    k = (0, l.up)("q-scroll-area"),
-                    v = (0, l.up)("q-separator"),
-                    x = (0, l.up)("q-uploader"),
-                    C = (0, l.up)("cgraph"),
-                    q = (0, l.up)("q-tooltip"),
-                    _ = (0, l.up)("q-spinner-puff");
-                return "image" == e.type ? ((0, l.wg)(), (0, l.j4)(r, {
+            function Se(e, t, a, i, n, o) {
+                const d = (0, s.up)("q-icon"),
+                    r = (0, s.up)("q-img"),
+                    c = (0, s.up)("q-badge"),
+                    h = (0, s.up)("q-select"),
+                    u = (0, s.up)("q-checkbox"),
+                    p = (0, s.up)("q-toggle"),
+                    g = (0, s.up)("q-btn"),
+                    m = (0, s.up)("q-btn-toggle"),
+                    f = (0, s.up)("utable"),
+                    y = (0, s.up)("linechart"),
+                    w = (0, s.up)("q-input"),
+                    b = (0, s.up)("q-tree"),
+                    k = (0, s.up)("q-scroll-area"),
+                    v = (0, s.up)("q-separator"),
+                    x = (0, s.up)("q-uploader"),
+                    C = (0, s.up)("cgraph"),
+                    _ = (0, s.up)("q-tooltip"),
+                    q = (0, s.up)("q-spinner-puff");
+                return "image" == e.type ? ((0, s.wg)(), (0, s.j4)(r, {
                     key: 0,
                     src: e.data.name,
                     "spinner-color": "blue",
-                    onClick: (0, he.iM)(e.switchValue, ["stop"]),
+                    onClick: (0, ce.iM)(e.switchValue, ["stop"]),
                     fit: "cover",
-                    style: (0, s.j5)(e.elemSize)
+                    style: (0, l.j5)(e.elemSize)
                 }, {
-                    default: (0, l.w5)((() => [e.data.header ? ((0, l.wg)(), (0, l.iD)("div", {
+                    default: (0, s.w5)((() => [e.data.header ? ((0, s.wg)(), (0, s.iD)("div", {
                         key: 0,
                         class: "absolute-bottom-right text-subtitle2 custom-caption",
-                        onClick: t[0] || (t[0] = (0, he.iM)(((...t) => e.lens && e.lens(...t)), ["stop"]))
-                    }, (0, s.zw)(e.data.header), 1)) : (0, l.kq)("", !0), e.value ? ((0, l.wg)(), (0, l.j4)(d, {
+                        onClick: t[0] || (t[0] = (0, ce.iM)(((...t) => e.lens && e.lens(...t)), ["stop"]))
+                    }, (0, l.zw)(e.data.header), 1)) : (0, s.kq)("", !0), e.value ? ((0, s.wg)(), (0, s.j4)(d, {
                         key: 1,
                         class: "absolute all-pointer-events",
                         size: "32px",
                         name: "check_circle",
                         color: "light-blue-2",
                         style: {
                             "font-size": "2em",
                             top: "8px",
                             left: "8px"
                         }
-                    })) : (0, l.kq)("", !0)])),
+                    })) : (0, s.kq)("", !0)])),
                     _: 1
-                }, 8, ["src", "onClick", "style"])) : "select" == e.type ? ((0, l.wg)(), (0, l.j4)(h, {
+                }, 8, ["src", "onClick", "style"])) : "select" == e.type ? ((0, s.wg)(), (0, s.j4)(h, {
                     key: 1,
                     "transition-show": "flip-up",
                     "transition-hide": "flip-down",
                     dense: "",
                     modelValue: e.value,
                     "onUpdate:modelValue": t[1] || (t[1] = t => e.value = t),
                     options: e.data.options
-                }, (0, l.Nv)({
+                }, (0, s.Nv)({
                     _: 2
                 }, [e.showname ? {
                     name: "prepend",
-                    fn: (0, l.w5)((() => [(0, l.Wm)(c, {
+                    fn: (0, s.w5)((() => [(0, s.Wm)(c, {
                         color: "secondary"
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Uk)((0, s.zw)(e.name), 1)])),
+                        default: (0, s.w5)((() => [(0, s.Uk)((0, l.zw)(e.name), 1)])),
                         _: 1
                     })])),
                     key: "0"
-                } : void 0]), 1032, ["modelValue", "options"])) : "check" == e.type ? ((0, l.wg)(), (0, l.j4)(u, {
+                } : void 0]), 1032, ["modelValue", "options"])) : "check" == e.type ? ((0, s.wg)(), (0, s.j4)(u, {
                     key: 2,
                     "left-label": "",
                     modelValue: e.value,
                     "onUpdate:modelValue": t[2] || (t[2] = t => e.value = t),
                     label: e.nameLabel,
                     "checked-icon": "task_alt",
                     "unchecked-icon": "highlight_off"
-                }, null, 8, ["modelValue", "label"])) : "switch" == e.type ? ((0, l.wg)(), (0, l.j4)(p, {
+                }, null, 8, ["modelValue", "label"])) : "switch" == e.type ? ((0, s.wg)(), (0, s.j4)(p, {
                     key: 3,
                     modelValue: e.value,
                     "onUpdate:modelValue": t[3] || (t[3] = t => e.value = t),
                     color: "primary",
                     label: e.nameLabel,
                     "left-label": ""
-                }, null, 8, ["modelValue", "label"])) : "radio" == e.type ? ((0, l.wg)(), (0, l.iD)("div", pe, [e.showname ? ((0, l.wg)(), (0, l.j4)(g, {
+                }, null, 8, ["modelValue", "label"])) : "radio" == e.type ? ((0, s.wg)(), (0, s.iD)("div", ue, [e.showname ? ((0, s.wg)(), (0, s.j4)(g, {
                     key: 0,
                     ripple: !1,
-                    color: "secondary",
+                    color: "indigo-10",
                     disable: "",
                     label: e.name,
                     "no-caps": ""
-                }, null, 8, ["label"])) : (0, l.kq)("", !0), (0, l.Wm)(m, {
+                }, null, 8, ["label"])) : (0, s.kq)("", !0), (0, s.Wm)(m, {
                     modelValue: e.value,
                     "onUpdate:modelValue": t[4] || (t[4] = t => e.value = t),
                     "no-caps": "",
                     options: e.data.options.map((e => ({
                         label: e,
                         value: e
                     })))
-                }, null, 8, ["modelValue", "options"])])) : "table" == e.type ? ((0, l.wg)(), (0, l.j4)(f, {
+                }, null, 8, ["modelValue", "options"])])) : "table" == e.type ? ((0, s.wg)(), (0, s.j4)(f, {
                     key: 5,
                     data: e.data,
                     pdata: e.pdata,
                     styleSize: e.styleSize
-                }, null, 8, ["data", "pdata", "styleSize"])) : "linechart" == e.type ? ((0, l.wg)(), (0, l.j4)(y, {
+                }, null, 8, ["data", "pdata", "styleSize"])) : "linechart" == e.type ? ((0, s.wg)(), (0, s.j4)(y, {
                     key: 6,
                     data: e.data,
                     pdata: e.pdata,
                     styleSize: e.styleSize
-                }, null, 8, ["data", "pdata", "styleSize"])) : "edit" == e.type ? ((0, l.wg)(), (0, l.j4)(w, {
+                }, null, 8, ["data", "pdata", "styleSize"])) : "edit" == e.type ? ((0, s.wg)(), (0, s.j4)(w, {
                     key: 7,
                     modelValue: e.value,
                     "onUpdate:modelValue": t[5] || (t[5] = t => e.value = t),
                     label: e.name,
                     ref: "inputRef",
                     autogrow: e.data.autogrow,
                     dense: "",
-                    onKeyup: (0, he.D2)(e.pressedEnter, ["enter"]),
+                    onKeyup: (0, ce.D2)(e.pressedEnter, ["enter"]),
                     readonly: !1 === e.data.edit
-                }, null, 8, ["modelValue", "label", "autogrow", "onKeyup", "readonly"])) : "number" == e.type ? ((0, l.wg)(), (0, l.j4)(w, {
+                }, null, 8, ["modelValue", "label", "autogrow", "onKeyup", "readonly"])) : "number" == e.type ? ((0, s.wg)(), (0, s.j4)(w, {
                     key: 8,
                     modelValue: e.value,
                     "onUpdate:modelValue": t[6] || (t[6] = t => e.value = t),
                     modelModifiers: {
                         number: !0
                     },
                     label: e.name,
                     ref: "inputRef",
                     dense: "",
-                    onKeyup: (0, he.D2)(e.pressedEnter, ["enter"]),
+                    onKeyup: (0, ce.D2)(e.pressedEnter, ["enter"]),
                     type: "number",
                     readonly: !1 === e.data.edit
-                }, null, 8, ["modelValue", "label", "onKeyup", "readonly"])) : "autoedit" == e.type ? ((0, l.wg)(), (0, l.j4)(h, {
+                }, null, 8, ["modelValue", "label", "onKeyup", "readonly"])) : "autoedit" == e.type ? ((0, s.wg)(), (0, s.j4)(h, {
                     key: 9,
                     dense: "",
                     modelValue: e.value,
                     "onUpdate:modelValue": t[7] || (t[7] = t => e.value = t),
                     "use-input": "",
                     "hide-selected": "",
                     borderless: "",
                     outlined: "",
                     "hide-bottom-space": "",
                     "fill-input": "",
                     "input-debounce": "0",
                     options: e.options,
                     onFilter: e.complete,
                     label: e.name,
-                    onKeyup: (0, he.D2)(e.pressedEnter, ["enter"])
-                }, null, 8, ["modelValue", "options", "onFilter", "label", "onKeyup"])) : "tree" == e.type || "list" == e.type ? ((0, l.wg)(), (0, l.j4)(k, {
+                    onKeyup: (0, ce.D2)(e.pressedEnter, ["enter"])
+                }, null, 8, ["modelValue", "options", "onFilter", "label", "onKeyup"])) : "tree" == e.type || "list" == e.type ? ((0, s.wg)(), (0, s.j4)(k, {
                     key: 10,
-                    style: (0, s.j5)(e.styleSize),
+                    style: (0, l.j5)(e.styleSize),
                     "thumb-style": e.thumbStyle,
                     "bar-style": e.barStyle
                 }, {
-                    default: (0, l.w5)((() => [(0, l.Wm)(b, {
+                    default: (0, s.w5)((() => [(0, s.Wm)(b, {
                         nodes: e.treeNodes,
                         dense: e.data.dense,
                         selected: e.value,
                         "onUpdate:selected": t[8] || (t[8] = t => e.value = t),
                         expanded: e.expandedKeys,
                         "onUpdate:expanded": t[9] || (t[9] = t => e.expandedKeys = t),
                         "node-key": "label",
                         "default-expand-all": "",
                         "selected-color": "blue-10"
                     }, null, 8, ["nodes", "dense", "selected", "expanded"])])),
                     _: 1
-                }, 8, ["style", "thumb-style", "bar-style"])) : "docviewer" == e.type ? (0, l.wy)(((0, l.wg)(), (0, l.iD)("textarea", {
+                }, 8, ["style", "thumb-style", "bar-style"])) : "docviewer" == e.type ? (0, s.wy)(((0, s.wg)(), (0, s.iD)("textarea", {
                     key: 11,
-                    class: "textarea",
+                    class: (0, l.C_)(["textarea", {
+                        "bg-grey-10": e.Dark.isActive,
+                        "text-white": e.Dark.isActive
+                    }]),
                     "onUpdate:modelValue": t[10] || (t[10] = t => e.value = t),
                     filled: "",
                     type: "textarea",
-                    style: (0, s.j5)(e.elemSize)
-                }, null, 4)), [
-                    [he.nr, e.value]
-                ]) : "line" == e.type ? ((0, l.wg)(), (0, l.j4)(v, {
+                    style: (0, l.j5)(e.elemSize)
+                }, null, 6)), [
+                    [ce.nr, e.value]
+                ]) : "line" == e.type ? ((0, s.wg)(), (0, s.j4)(v, {
                     key: 12,
                     color: "green"
-                })) : "video" == e.type ? ((0, l.wg)(), (0, l.iD)("video", {
+                })) : "video" == e.type ? ((0, s.wg)(), (0, s.iD)("video", {
                     width: e.data.width,
                     height: e.data.height,
                     key: e.data.src,
                     controls: ""
-                }, [(0, l._)("source", {
+                }, [(0, s._)("source", {
                     src: e.data.src,
                     type: "video/mp4"
-                }, null, 8, me)], 8, ge)) : "uploader" == e.type ? ((0, l.wg)(), (0, l.j4)(x, {
+                }, null, 8, ge)], 8, pe)) : "uploader" == e.type ? ((0, s.wg)(), (0, s.j4)(x, {
                     key: 14,
                     label: e.name,
                     "auto-upload": "",
                     thumbnails: "",
                     url: e.host_path,
                     onUploaded: e.updateDom,
                     onAdded: e.onAdded,
-                    style: (0, s.j5)(e.elemSize),
+                    style: (0, l.j5)(e.elemSize),
                     ref: "uploaderRef",
-                    flat: ""
-                }, null, 8, ["label", "url", "onUploaded", "onAdded", "style"])) : "image_uploader" == e.type ? ((0, l.wg)(), (0, l.j4)(x, {
+                    flat: "",
+                    class: (0, l.C_)({
+                        "bg-grey-9": e.Dark.isActive
+                    })
+                }, null, 8, ["label", "url", "onUploaded", "onAdded", "style", "class"])) : "image_uploader" == e.type ? ((0, s.wg)(), (0, s.j4)(x, {
                     key: 15,
                     label: e.name,
                     "auto-upload": "",
                     thumbnails: "",
                     url: e.host_path,
                     onUploaded: e.updateDom,
                     onAdded: e.onAdded,
                     ref: "uploaderRef",
-                    flat: ""
-                }, null, 8, ["label", "url", "onUploaded", "onAdded"])) : "graph" == e.type ? ((0, l.wg)(), (0, l.j4)(C, {
+                    flat: "",
+                    class: (0, l.C_)({
+                        "bg-grey-10": e.Dark.isActive
+                    }),
+                    color: e.Dark.isActive ? "purple-10" : "blue"
+                }, null, 8, ["label", "url", "onUploaded", "onAdded", "class", "color"])) : "graph" == e.type ? ((0, s.wg)(), (0, s.j4)(C, {
                     key: 16,
                     data: e.data,
                     pdata: e.pdata,
                     styleSize: e.elemSize
-                }, null, 8, ["data", "pdata", "styleSize"])) : "camera" == e.type ? ((0, l.wg)(), (0, l.iD)("div", fe, [(0, l._)("div", ye, [(0, l._)("button", {
-                    class: (0, s.C_)(["button is-rounded", {
+                }, null, 8, ["data", "pdata", "styleSize"])) : "camera" == e.type ? ((0, s.wg)(), (0, s.iD)("div", me, [(0, s._)("div", fe, [(0, s._)("button", {
+                    class: (0, l.C_)(["button is-rounded", {
                         "is-primary": !e.isCameraOpen,
                         "is-danger": e.isCameraOpen
                     }]),
                     type: "button",
                     onClick: t[11] || (t[11] = (...t) => e.toggleCamera && e.toggleCamera(...t))
-                }, [e.isCameraOpen ? ((0, l.wg)(), (0, l.iD)("span", be, "Close Camera")) : ((0, l.wg)(), (0, l.iD)("span", we, "Open Camera"))], 2)]), (0, l.wy)((0, l._)("div", ke, xe, 512), [
-                    [he.F8, e.isCameraOpen && e.isLoading]
-                ]), e.isCameraOpen ? (0, l.wy)(((0, l.wg)(), (0, l.iD)("div", {
+                }, [e.isCameraOpen ? ((0, s.wg)(), (0, s.iD)("span", we, "Close Camera")) : ((0, s.wg)(), (0, s.iD)("span", ye, "Open Camera"))], 2)]), (0, s.wy)((0, s._)("div", be, ve, 512), [
+                    [ce.F8, e.isCameraOpen && e.isLoading]
+                ]), e.isCameraOpen ? (0, s.wy)(((0, s.wg)(), (0, s.iD)("div", {
                     key: 0,
-                    class: (0, s.C_)(["camera-box", {
+                    class: (0, l.C_)(["camera-box", {
                         flash: e.isShotPhoto
                     }])
-                }, [(0, l._)("div", {
-                    class: (0, s.C_)(["camera-shutter", {
+                }, [(0, s._)("div", {
+                    class: (0, l.C_)(["camera-shutter", {
                         flash: e.isShotPhoto
                     }])
-                }, null, 2), (0, l.wy)((0, l._)("video", {
+                }, null, 2), (0, s.wy)((0, s._)("video", {
                     ref: "camera",
                     width: 450,
                     height: 337.5,
                     autoplay: ""
-                }, null, 8, Ce), [
-                    [he.F8, !e.isPhotoTaken]
-                ]), (0, l.wy)((0, l._)("canvas", {
+                }, null, 8, xe), [
+                    [ce.F8, !e.isPhotoTaken]
+                ]), (0, s.wy)((0, s._)("canvas", {
                     id: "photoTaken",
                     ref: "canvas",
                     width: 450,
                     height: 337.5
-                }, null, 8, qe), [
-                    [he.F8, e.isPhotoTaken]
+                }, null, 8, Ce), [
+                    [ce.F8, e.isPhotoTaken]
                 ])], 2)), [
-                    [he.F8, !e.isLoading]
-                ]) : (0, l.kq)("", !0), e.isCameraOpen && !e.isLoading ? ((0, l.wg)(), (0, l.iD)("div", _e, [(0, l._)("button", {
+                    [ce.F8, !e.isLoading]
+                ]) : (0, s.kq)("", !0), e.isCameraOpen && !e.isLoading ? ((0, s.wg)(), (0, s.iD)("div", _e, [(0, s._)("button", {
                     class: "button",
                     type: "button",
                     onClick: t[12] || (t[12] = (...t) => e.takePhoto && e.takePhoto(...t))
-                }, Se)])) : (0, l.kq)("", !0), e.isPhotoTaken && e.isCameraOpen ? ((0, l.wg)(), (0, l.iD)("div", ze, [(0, l.Wm)(g, {
+                }, Ae)])) : (0, s.kq)("", !0), e.isPhotoTaken && e.isCameraOpen ? ((0, s.wg)(), (0, s.iD)("div", De, [(0, s.Wm)(g, {
                     onClick: e.downloadImage,
                     label: "Send"
-                }, null, 8, ["onClick"])])) : (0, l.kq)("", !0)])) : "" != e.showname ? ((0, l.wg)(), (0, l.j4)(g, {
+                }, null, 8, ["onClick"])])) : (0, s.kq)("", !0)])) : "" != e.showname ? ((0, s.wg)(), (0, s.j4)(g, {
                     key: 18,
                     "no-caps": "",
+                    class: (0, l.C_)({
+                        "bg-blue-grey-9": e.Dark.isActive
+                    }),
                     label: e.name,
                     icon: e.data.icon,
                     onClick: e.sendValue
                 }, {
-                    default: (0, l.w5)((() => [e.data.tooltip ? ((0, l.wg)(), (0, l.j4)(q, {
+                    default: (0, s.w5)((() => [e.data.tooltip ? ((0, s.wg)(), (0, s.j4)(_, {
                         key: 0,
                         class: "text-body2"
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Uk)((0, s.zw)(e.data.tooltip), 1)])),
+                        default: (0, s.w5)((() => [(0, s.Uk)((0, l.zw)(e.data.tooltip), 1)])),
                         _: 1
-                    })) : (0, l.kq)("", !0)])),
+                    })) : (0, s.kq)("", !0)])),
                     _: 1
-                }, 8, ["label", "icon", "onClick"])) : e.data.mode ? ((0, l.wg)(), (0, l.j4)(g, {
+                }, 8, ["class", "label", "icon", "onClick"])) : e.data.mode ? ((0, s.wg)(), (0, s.j4)(g, {
                     key: 20,
                     "no-caps": "",
                     dense: "",
+                    round: "",
+                    class: (0, l.C_)({
+                        "bg-grey-9": e.Dark.isActive
+                    }),
                     onClick: e.sendValue
                 }, {
-                    default: (0, l.w5)((() => [(0, l.Wm)(_, {
+                    default: (0, s.w5)((() => [(0, s.Wm)(q, {
                         color: e.data.mode
-                    }, null, 8, ["color"]), e.data.tooltip ? ((0, l.wg)(), (0, l.j4)(q, {
+                    }, null, 8, ["color"]), e.data.tooltip ? ((0, s.wg)(), (0, s.j4)(_, {
                         key: 0,
                         class: "text-body2"
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Uk)((0, s.zw)(e.data.tooltip), 1)])),
+                        default: (0, s.w5)((() => [(0, s.Uk)((0, l.zw)(e.data.tooltip), 1)])),
                         _: 1
-                    })) : (0, l.kq)("", !0)])),
+                    })) : (0, s.kq)("", !0)])),
                     _: 1
-                }, 8, ["onClick"])) : ((0, l.wg)(), (0, l.j4)(g, {
+                }, 8, ["class", "onClick"])) : ((0, s.wg)(), (0, s.j4)(g, {
                     key: 19,
                     "no-caps": "",
                     dense: "",
+                    round: "",
+                    class: (0, l.C_)({
+                        "bg-grey-9": e.Dark.isActive
+                    }),
                     icon: e.data.icon,
                     onClick: e.sendValue
                 }, {
-                    default: (0, l.w5)((() => [e.data.tooltip ? ((0, l.wg)(), (0, l.j4)(q, {
+                    default: (0, s.w5)((() => [e.data.tooltip ? ((0, s.wg)(), (0, s.j4)(_, {
                         key: 0,
                         class: "text-body2"
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Uk)((0, s.zw)(e.data.tooltip), 1)])),
+                        default: (0, s.w5)((() => [(0, s.Uk)((0, l.zw)(e.data.tooltip), 1)])),
                         _: 1
-                    })) : (0, l.kq)("", !0)])),
+                    })) : (0, s.kq)("", !0)])),
                     _: 1
-                }, 8, ["icon", "onClick"]))
+                }, 8, ["class", "icon", "onClick"]))
             }
-            const Ze = {
+            const je = {
                     key: 0
                 },
-                $e = {
+                ze = {
                     class: "row"
                 },
-                De = ["onClick"];
+                Ze = ["onClick"];
 
-            function Me(e, t, a, i, n, o) {
-                const d = (0, l.up)("q-icon"),
-                    r = (0, l.up)("q-tooltip"),
-                    c = (0, l.up)("q-input"),
-                    h = (0, l.up)("q-btn"),
-                    u = (0, l.up)("q-th"),
-                    p = (0, l.up)("q-tr"),
-                    g = (0, l.up)("q-checkbox"),
-                    m = (0, l.up)("q-select"),
-                    f = (0, l.up)("q-td"),
-                    y = (0, l.up)("q-table");
-                return (0, l.wg)(), (0, l.j4)(y, {
-                    class: "my-sticky-virtscroll-table",
+            function $e(e, t, a, i, n, o) {
+                const d = (0, s.up)("q-icon"),
+                    r = (0, s.up)("q-tooltip"),
+                    c = (0, s.up)("q-input"),
+                    h = (0, s.up)("q-btn"),
+                    u = (0, s.up)("q-th"),
+                    p = (0, s.up)("q-tr"),
+                    g = (0, s.up)("q-checkbox"),
+                    m = (0, s.up)("q-select"),
+                    f = (0, s.up)("q-td"),
+                    y = (0, s.up)("q-table");
+                return (0, s.wg)(), (0, s.j4)(y, {
                     "virtual-scroll": "",
                     dense: e.data.dense,
-                    style: (0, s.j5)(e.styleSize),
+                    style: (0, l.j5)(e.styleSize),
                     flat: "",
                     filter: e.search,
                     ref: "table",
                     virtualScrollSliceSize: "60",
                     "rows-per-page-options": [0],
                     "virtual-scroll-sticky-size-start": 48,
                     "row-key": "iiid",
                     title: e.name,
                     rows: e.rows,
                     columns: e.columns,
                     selection: e.singleMode ? "single" : "multiple",
                     selected: e.selected,
                     "onUpdate:selected": t[2] || (t[2] = t => e.selected = t)
                 }, {
-                    "top-right": (0, l.w5)((() => [!1 !== e.data.tools ? ((0, l.wg)(), (0, l.iD)("div", Ze, [(0, l._)("div", $e, [(0, l.Wm)(c, {
+                    "top-right": (0, s.w5)((() => [!1 !== e.data.tools ? ((0, s.wg)(), (0, s.iD)("div", je, [(0, s._)("div", ze, [(0, s.Wm)(c, {
                         modelValue: e.search,
                         "onUpdate:modelValue": t[1] || (t[1] = t => e.search = t),
                         label: "Search",
                         dense: "",
                         ref: "searchField"
-                    }, (0, l.Nv)({
-                        append: (0, l.w5)((() => ["" != e.search ? ((0, l.wg)(), (0, l.j4)(d, {
+                    }, (0, s.Nv)({
+                        append: (0, s.w5)((() => ["" != e.search ? ((0, s.wg)(), (0, s.j4)(d, {
                             key: 0,
                             class: "cursor-pointer",
                             name: "close",
                             size: "xs",
                             onClick: t[0] || (t[0] = t => {
                                 e.search = "", e.$refs.searchField.focus()
                             })
                         }, {
-                            default: (0, l.w5)((() => [(0, l.Wm)(r, {
+                            default: (0, s.w5)((() => [(0, s.Wm)(r, {
                                 class: "text-body2"
                             }, {
-                                default: (0, l.w5)((() => [(0, l.Uk)("Reset search")])),
+                                default: (0, s.w5)((() => [(0, s.Uk)("Reset search ")])),
                                 _: 1
                             })])),
                             _: 1
-                        })) : (0, l.kq)("", !0)])),
+                        })) : (0, s.kq)("", !0)])),
                         _: 2
                     }, ["" == e.search ? {
                         name: "prepend",
-                        fn: (0, l.w5)((() => [(0, l.Wm)(d, {
+                        fn: (0, s.w5)((() => [(0, s.Wm)(d, {
                             name: "search",
                             size: "xs"
                         })])),
                         key: "0"
-                    } : void 0]), 1032, ["modelValue"]), (0, l._)("div", null, [(0, l.Wm)(h, {
+                    } : void 0]), 1032, ["modelValue"]), (0, s._)("div", null, [(0, s.Wm)(h, {
+                        class: (0, l.C_)(["q-ml-xs", {
+                            "bg-cyan-10": e.Dark.isActive
+                        }]),
                         dense: "",
                         rounded: "",
                         icon: "select_all",
                         "no-caps": "",
                         onClick: e.showSelected
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Wm)(r, {
+                        default: (0, s.w5)((() => [(0, s.Wm)(r, {
                             class: "text-body2"
                         }, {
-                            default: (0, l.w5)((() => [(0, l.Uk)("Show selected")])),
+                            default: (0, s.w5)((() => [(0, s.Uk)("Show selected ")])),
                             _: 1
                         })])),
                         _: 1
-                    }, 8, ["onClick"]), (0, l.Wm)(h, {
+                    }, 8, ["class", "onClick"]), (0, s.Wm)(h, {
+                        class: (0, l.C_)(["q-ml-xs", {
+                            "bg-cyan-10": e.Dark.isActive
+                        }]),
                         dense: "",
                         rounded: "",
                         icon: "deselect",
                         "no-caps": "",
                         onClick: e.deselectAll
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Wm)(r, {
+                        default: (0, s.w5)((() => [(0, s.Wm)(r, {
                             class: "text-body2"
                         }, {
-                            default: (0, l.w5)((() => [(0, l.Uk)("Deselect all")])),
+                            default: (0, s.w5)((() => [(0, s.Uk)("Deselect all")])),
                             _: 1
                         })])),
                         _: 1
-                    }, 8, ["onClick"]), "delete" in e.data ? ((0, l.wg)(), (0, l.j4)(h, {
+                    }, 8, ["class", "onClick"]), "delete" in e.data ? ((0, s.wg)(), (0, s.j4)(h, {
                         key: 0,
+                        class: (0, l.C_)(["q-ml-xs", {
+                            "bg-cyan-10": e.Dark.isActive
+                        }]),
                         dense: "",
                         rounded: "",
                         icon: "delete_forever",
                         "no-caps": "",
                         onClick: e.delSelected
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Wm)(r, {
+                        default: (0, s.w5)((() => [(0, s.Wm)(r, {
                             class: "text-body2"
                         }, {
-                            default: (0, l.w5)((() => [(0, l.Uk)("Delete selected")])),
+                            default: (0, s.w5)((() => [(0, s.Uk)("Delete selected")])),
                             _: 1
                         })])),
                         _: 1
-                    }, 8, ["onClick"])) : (0, l.kq)("", !0), !1 !== e.data.multimode ? ((0, l.wg)(), (0, l.j4)(h, {
+                    }, 8, ["class", "onClick"])) : (0, s.kq)("", !0), !1 !== e.data.multimode ? ((0, s.wg)(), (0, s.j4)(h, {
                         key: 1,
+                        class: (0, l.C_)(["q-ml-xs", {
+                            "bg-cyan-10": e.Dark.isActive
+                        }]),
                         dense: "",
                         rounded: "",
                         icon: e.singleMode ? "looks_one" : "grain",
                         "no-caps": "",
                         onClick: e.switchMode
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Wm)(r, {
+                        default: (0, s.w5)((() => [(0, s.Wm)(r, {
                             class: "text-body2"
                         }, {
-                            default: (0, l.w5)((() => [(0, l.Uk)("Multi-single select mode")])),
+                            default: (0, s.w5)((() => [(0, s.Uk)("Multi-single select mode")])),
                             _: 1
                         })])),
                         _: 1
-                    }, 8, ["icon", "onClick"])) : (0, l.kq)("", !0), e.editable ? ((0, l.wg)(), (0, l.j4)(h, {
+                    }, 8, ["class", "icon", "onClick"])) : (0, s.kq)("", !0), e.editable ? ((0, s.wg)(), (0, s.j4)(h, {
                         key: 2,
+                        class: (0, l.C_)(["q-ml-xs", {
+                            "bg-cyan-10": e.Dark.isActive
+                        }]),
                         dense: "",
                         rounded: "",
                         icon: e.editMode ? "cancel" : "edit",
                         "no-caps": "",
                         onClick: e.switchEdit
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Wm)(r, {
+                        default: (0, s.w5)((() => [(0, s.Wm)(r, {
                             class: "text-body2"
                         }, {
-                            default: (0, l.w5)((() => [(0, l.Uk)("Edit mode")])),
+                            default: (0, s.w5)((() => [(0, s.Uk)("Edit mode")])),
                             _: 1
                         })])),
                         _: 1
-                    }, 8, ["icon", "onClick"])) : (0, l.kq)("", !0), e.editable && "append" in e.data ? ((0, l.wg)(), (0, l.j4)(h, {
+                    }, 8, ["class", "icon", "onClick"])) : (0, s.kq)("", !0), e.editable && "append" in e.data ? ((0, s.wg)(), (0, s.j4)(h, {
                         key: 3,
+                        class: (0, l.C_)(["q-ml-xs", {
+                            "bg-cyan-10": e.Dark.isActive
+                        }]),
                         dense: "",
                         rounded: "",
                         icon: "add",
                         "no-caps": "",
                         onClick: e.append
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Wm)(r, {
+                        default: (0, s.w5)((() => [(0, s.Wm)(r, {
                             class: "text-body2"
                         }, {
-                            default: (0, l.w5)((() => [(0, l.Uk)("Add a new row")])),
+                            default: (0, s.w5)((() => [(0, s.Uk)("Add a new row")])),
                             _: 1
                         })])),
                         _: 1
-                    }, 8, ["onClick"])) : (0, l.kq)("", !0), "view" in e.data ? ((0, l.wg)(), (0, l.j4)(h, {
+                    }, 8, ["class", "onClick"])) : (0, s.kq)("", !0), "view" in e.data ? ((0, s.wg)(), (0, s.j4)(h, {
                         key: 4,
+                        class: (0, l.C_)(["q-ml-xs", {
+                            "bg-cyan-10": e.Dark.isActive
+                        }]),
                         dense: "",
                         rounded: "",
                         icon: "insights",
                         "no-caps": "",
                         onClick: e.chart
                     }, {
-                        default: (0, l.w5)((() => [(0, l.Wm)(r, {
+                        default: (0, s.w5)((() => [(0, s.Wm)(r, {
                             class: "text-body2"
                         }, {
-                            default: (0, l.w5)((() => [(0, l.Uk)("Draw the chart")])),
+                            default: (0, s.w5)((() => [(0, s.Uk)("Draw the chart")])),
                             _: 1
                         })])),
                         _: 1
-                    }, 8, ["onClick"])) : (0, l.kq)("", !0)])])])) : (0, l.kq)("", !0)])),
-                    header: (0, l.w5)((e => [(0, l.Wm)(p, {
-                        props: e
+                    }, 8, ["class", "onClick"])) : (0, s.kq)("", !0)])])])) : (0, s.kq)("", !0)])),
+                    header: (0, s.w5)((t => [(0, s.Wm)(p, {
+                        props: t
                     }, {
-                        default: (0, l.w5)((() => [((0, l.wg)(!0), (0, l.iD)(l.HY, null, (0, l.Ko)(e.cols, (t => ((0, l.wg)(), (0, l.j4)(u, {
-                            class: "text-italic text-purple",
-                            key: t.name,
-                            props: e
+                        default: (0, s.w5)((() => [((0, s.wg)(!0), (0, s.iD)(s.HY, null, (0, s.Ko)(t.cols, (a => ((0, s.wg)(), (0, s.j4)(u, {
+                            class: (0, l.C_)(["text-italic", {
+                                "text-grey-9": !e.Dark.isActive,
+                                "text-teal-3": e.Dark.isActive
+                            }]),
+                            key: a.name,
+                            props: t
                         }, {
-                            default: (0, l.w5)((() => [(0, l.Uk)((0, s.zw)(t.label), 1)])),
+                            default: (0, s.w5)((() => [(0, s.Uk)((0, l.zw)(a.label), 1)])),
                             _: 2
-                        }, 1032, ["props"])))), 128))])),
+                        }, 1032, ["class", "props"])))), 128))])),
                         _: 2
                     }, 1032, ["props"])])),
-                    body: (0, l.w5)((t => [(0, l.Wm)(p, {
+                    body: (0, s.w5)((t => [(0, s.Wm)(p, {
                         props: t,
                         onClick: e => t.selected = !t.selected
                     }, {
-                        default: (0, l.w5)((() => [((0, l.wg)(!0), (0, l.iD)(l.HY, null, (0, l.Ko)(e.columns, ((a, i) => ((0, l.wg)(), (0, l.j4)(f, {
+                        default: (0, s.w5)((() => [((0, s.wg)(!0), (0, s.iD)(s.HY, null, (0, s.Ko)(e.columns, ((a, i) => ((0, s.wg)(), (0, s.j4)(f, {
                             key: a.name,
                             props: t
                         }, {
-                            default: (0, l.w5)((() => ["boolean" == typeof t.row[a.name] ? ((0, l.wg)(), (0, l.j4)(g, {
+                            default: (0, s.w5)((() => ["boolean" == typeof t.row[a.name] ? ((0, s.wg)(), (0, s.j4)(g, {
                                 key: 0,
                                 modelValue: t.row[a.name],
-                                "onUpdate:modelValue": [e => t.row[a.name] = e, l => e.change_switcher(t.row, a.name, i)],
+                                "onUpdate:modelValue": [e => t.row[a.name] = e, s => e.change_switcher(t.row, a.name, i)],
                                 dense: "",
                                 disable: !e.editMode
-                            }, null, 8, ["modelValue", "onUpdate:modelValue", "disable"])) : e.editMode && "complete" in e.data && i == e.cedit && e.redit == t.row.iiid ? ((0, l.wg)(), (0, l.j4)(m, {
+                            }, null, 8, ["modelValue", "onUpdate:modelValue", "disable"])) : e.editMode && "complete" in e.data && i == e.cedit && e.redit == t.row.iiid ? ((0, s.wg)(), (0, s.j4)(m, {
                                 key: 1,
                                 dense: "",
                                 "model-value": t.row[a.name],
                                 "use-input": "",
                                 "hide-selected": "",
                                 "fill-input": "",
                                 autofocus: "",
@@ -1086,106 +1162,108 @@
                                 borderless: "",
                                 onInputValue: e.change,
                                 "hide-dropdown-icon": "",
                                 "input-debounce": "0",
                                 options: e.options,
                                 onFilter: e.complete,
                                 onKeydown: e.keyInput
-                            }, null, 8, ["model-value", "onInputValue", "options", "onFilter", "onKeydown"])) : e.editMode && i == e.cedit && e.redit == t.row.iiid ? ((0, l.wg)(), (0, l.j4)(c, {
+                            }, null, 8, ["model-value", "onInputValue", "options", "onFilter", "onKeydown"])) : e.editMode && i == e.cedit && e.redit == t.row.iiid ? ((0, s.wg)(), (0, s.j4)(c, {
                                 key: 2,
                                 modelValue: t.row[a.name],
                                 "onUpdate:modelValue": [e => t.row[a.name] = e, e.change],
                                 dense: "",
                                 onKeydown: e.keyInput,
                                 autofocus: ""
-                            }, null, 8, ["modelValue", "onUpdate:modelValue", "onKeydown"])) : ((0, l.wg)(), (0, l.iD)("div", {
+                            }, null, 8, ["modelValue", "onUpdate:modelValue", "onKeydown"])) : ((0, s.wg)(), (0, s.iD)("div", {
                                 key: 3,
                                 onClick: a => e.select(t.row.iiid, i)
-                            }, (0, s.zw)(t.row[a.name]), 9, De))])),
+                            }, (0, l.zw)(t.row[a.name]), 9, Ze))])),
                             _: 2
                         }, 1032, ["props"])))), 128))])),
                         _: 2
                     }, 1032, ["props", "onClick"])])),
                     _: 1
                 }, 8, ["dense", "style", "filter", "title", "rows", "columns", "selection", "selected"])
             }
-            var Ve = a(1959);
+            var Me = a(1959),
+                Ve = a(9058);
 
             function Ee(e, t) {
                 return e.length === t.length && e.every(((e, a) => e.iiid == t[a].iiid))
             }
-            const Ke = (0, l.aZ)({
+            const We = (0, s.aZ)({
                 name: "utable",
                 setup(e) {
                     const {
                         data: t,
                         pdata: a
-                    } = (0, Ve.BK)(e);
-                    let s = (0, l.Fl)((() => {
+                    } = (0, Me.BK)(e);
+                    let l = (0, s.Fl)((() => {
                             let e = [],
                                 a = t.value;
-                            const l = a.headers,
-                                s = l.length,
+                            const s = a.headers,
+                                l = s.length,
                                 i = a.rows,
                                 n = i.length;
                             for (var o = 0; o < n; o++) {
                                 const t = {},
                                     a = i[o];
-                                for (var d = 0; d < s; d++) t[l[d]] = a[d];
+                                for (var d = 0; d < l; d++) t[s[d]] = a[d];
                                 t.iiid = o, e.push(t)
                             }
                             return e
                         })),
                         i = () => {
                             let e = t.value,
-                                a = null === e.value || 0 == s.value.length ? [] : Array.isArray(e.value) ? e.value.map((e => s.value[e])) : [s.value[e.value]];
+                                a = null === e.value || 0 == l.value.length ? [] : Array.isArray(e.value) ? e.value.map((e => l.value[e])) : [l.value[e.value]];
                             return a
                         },
                         n = i(),
-                        o = (0, Ve.iH)(n),
-                        d = (0, Ve.iH)(n),
-                        r = (0, Ve.iH)(!Array.isArray(t.value.value)),
-                        c = (e, l) => {
-                            S([a.value.name, t.value.name, e, l])
+                        o = (0, Me.iH)(n),
+                        d = (0, Me.iH)(n),
+                        r = (0, Me.iH)(!Array.isArray(t.value.value)),
+                        c = (e, s) => {
+                            D([a.value.name, t.value.name, e, s])
                         },
-                        h = (0, l.Fl)((() => r.value ? d.value.length > 0 ? d.value[0].iiid : null : d.value.map((e => e.iiid)))),
-                        u = (0, l.Fl)((() => t.value.value));
-                    return (0, l.YP)(s, ((e, t) => {
+                        h = (0, s.Fl)((() => r.value ? d.value.length > 0 ? d.value[0].iiid : null : d.value.map((e => e.iiid)))),
+                        u = (0, s.Fl)((() => t.value.value));
+                    return (0, s.YP)(l, ((e, t) => {
                         d.value = i(), o.value = d.value
-                    })), (0, l.YP)(t, ((e, a) => {
+                    })), (0, s.YP)(t, ((e, a) => {
                         g && console.log("data update", a.name), d.value = i(), o.value = d.value, r.value = !Array.isArray(t.value.value)
                     })), {
-                        rows: s,
+                        rows: l,
                         value: h,
                         selected: d,
                         singleMode: r,
                         sendMessage: c,
                         datavalue: u,
                         updated: o
                     }
                 },
                 data() {
                     return {
+                        Dark: Ve.Z,
                         search: "",
                         editMode: !1,
                         options: [],
                         cedit: null
                     }
                 },
                 methods: {
                     select(e, t) {
                         this.editMode && (this.cedit = t, g && console.log("selected", e, this.cedit))
                     },
                     change_switcher(e, t, a) {
                         if (console.log(e, t, a, e[t]), this.editMode) {
                             this.cedit = a;
-                            const l = e.iiid;
-                            let s = this.data.rows;
-                            s[l][a] = e[t], this.sendMessage("modify", [e[t],
-                                [l, a]
+                            const s = e.iiid;
+                            let l = this.data.rows;
+                            l[s][a] = e[t], this.sendMessage("modify", [e[t],
+                                [s, a]
                             ])
                         }
                     },
                     change(e) {
                         if (g && console.log("changed", this.data.headers[this.cedit], e), this.editMode && this.selected.length) {
                             const t = this.selected[0].iiid;
                             let a = this.data.rows;
@@ -1246,17 +1324,17 @@
                             this.options = e
                         }))))
                     },
                     append() {
                         let e = this.data.rows,
                             t = e.length,
                             a = this;
-                        M(this, [t, this.search], (function(l) {
-                            if (!Array.isArray(l)) return h.error(l);
-                            g && console.log("added row", l), a.search = "", e.push(l), setTimeout((() => {
+                        M(this, [t, this.search], (function(s) {
+                            if (!Array.isArray(s)) return h.error(s);
+                            g && console.log("added row", s), a.search = "", e.push(s), setTimeout((() => {
                                 let e = a.rows;
                                 a.selected = [e[t]], a.showSelected(), a.editMode || a.switchEdit(), a.select(e[t], 0)
                             }), 100)
                         }), "append")
                     },
                     showSelected() {
                         let e = this.$refs.table;
@@ -1322,46 +1400,46 @@
                 },
                 props: {
                     data: Object,
                     pdata: Object,
                     styleSize: String
                 }
             });
-            var We = a(9267),
-                Oe = a(4842),
-                Qe = a(8870),
+            var Ke = a(9267),
+                Qe = a(4842),
+                Oe = a(8870),
                 He = a(2165),
                 Ue = a(8186),
                 Ne = a(2414),
                 Fe = a(3884),
                 Te = a(5735),
                 Pe = a(7208);
-            const Re = (0, P.Z)(Ke, [
-                    ["render", Me]
+            const Re = (0, P.Z)(We, [
+                    ["render", $e]
                 ]),
                 Ie = Re;
-            X()(Ke, "components", {
-                QTable: We.Z,
-                QInput: Oe.Z,
+            X()(We, "components", {
+                QTable: Ke.Z,
+                QInput: Qe.Z,
                 QIcon: L.Z,
-                QTooltip: Qe.Z,
+                QTooltip: Oe.Z,
                 QBtn: He.Z,
                 QTr: Ue.Z,
                 QTh: Ne.Z,
                 QTd: Fe.Z,
                 QCheckbox: Te.Z,
                 QSelect: Pe.Z
             });
             const Le = ["nodes", "edges"];
 
             function Be(e, t, a, i, n, o) {
-                return (0, l.wg)(), (0, l.iD)("div", {
+                return (0, s.wg)(), (0, s.iD)("div", {
                     nodes: e.nodes,
                     edges: e.edges,
-                    style: (0, s.j5)(e.styleSize),
+                    style: (0, l.j5)(e.styleSize),
                     ref: "cy"
                 }, null, 12, Le)
             }
             var Ye = a(2393),
                 Xe = a.n(Ye);
             const Ge = Xe().stylesheet().selector("node").css({
                     content: "data(id)",
@@ -1371,15 +1449,16 @@
                     "background-color": "#ff5555",
                     "border-color": "#ff5555",
                     "font-size": "14px"
                 }).selector("node[label]").css({
                     label: "data(label)",
                     "text-valign": "bottom",
                     "text-halign": "center",
-                    "font-size": "14px"
+                    "font-size": "14px",
+                    color: "#4DB6AC"
                 }).selector("edge").css({
                     label: "data(label)",
                     "curve-style": "bezier",
                     "target-arrow-shape": "triangle",
                     width: 4,
                     "line-color": "#4286f4",
                     "target-arrow-color": "#4286f4",
@@ -1403,15 +1482,15 @@
 
             function et(e, t) {
                 if (e.length != t.length) return !0;
                 for (let a = 0; a < e.length; a++)
                     if (e[a].id != t[a].id || e[a].label != t[a].label) return !0;
                 return !1
             }
-            const tt = (0, l.aZ)({
+            const tt = (0, s.aZ)({
                     name: "cgraph",
                     props: {
                         data: Object,
                         pdata: Object,
                         styleSize: String
                     },
                     data() {
@@ -1437,39 +1516,39 @@
                                     nodes: this.nodes,
                                     edges: this.edges
                                 },
                                 style: this.style
                             }),
                             t = this.value.nodes;
                         this.selectedNodes = t || [];
-                        for (let s of this.selectedNodes) e.nodes("[id='" + s + "']").addClass("selected");
+                        for (let l of this.selectedNodes) e.nodes("[id='" + l + "']").addClass("selected");
                         let a = this.value.edges;
                         this.selectedEdges = a || [];
-                        for (let s of this.selectedEdges) e.edges("[id='" + s + "']").addClass("highlighted");
+                        for (let l of this.selectedEdges) e.edges("[id='" + l + "']").addClass("highlighted");
                         this.cy = e;
-                        let l = this;
+                        let s = this;
                         e.on("tap", "node", (t => {
                             const a = t.target;
                             if (a.hasClass("selected")) {
                                 a.removeClass("selected");
                                 let e = a.id();
-                                l.selectedNodes = l.shiftKey ? l.selectedNodes.filter((t => t !== e)) : []
-                            } else !l.shiftKey && l.selectedEdges.length > 0 && (e.$(".selected").removeClass("selected"), l.selectedEdges = []), a.addClass("selected"), l.selectedNodes.push(a.id());
-                            l.sendMessage("changed", {
-                                nodes: l.selectedNodes,
-                                edges: l.selectedEdges
+                                s.selectedNodes = s.shiftKey ? s.selectedNodes.filter((t => t !== e)) : []
+                            } else !s.shiftKey && s.selectedEdges.length > 0 && (e.$(".selected").removeClass("selected"), s.selectedEdges = []), a.addClass("selected"), s.selectedNodes.push(a.id());
+                            s.sendMessage("changed", {
+                                nodes: s.selectedNodes,
+                                edges: s.selectedEdges
                             })
                         })), e.on("click", (function(t) {
                             let a = t.target;
                             if ("id" in a && (a === e || "edges" == t.target.group())) {
-                                l.shiftKey || e.edges().removeClass("highlighted");
+                                s.shiftKey || e.edges().removeClass("highlighted");
                                 let t = a.id();
-                                l.selectedEdges.includes(t) ? (l.selectedEdges = l.shiftKey ? l.selectedEdges.filter((e => e != t)) : [], e.edges("[id='" + t + "']").removeClass("highlighted")) : (e.edges("[id='" + t + "']").addClass("highlighted"), l.shiftKey ? l.selectedEdges.push(t) : l.selectedEdges = [t]), l.sendMessage("changed", {
-                                    nodes: l.selectedNodes,
-                                    edges: l.selectedEdges
+                                s.selectedEdges.includes(t) ? (s.selectedEdges = s.shiftKey ? s.selectedEdges.filter((e => e != t)) : [], e.edges("[id='" + t + "']").removeClass("highlighted")) : (e.edges("[id='" + t + "']").addClass("highlighted"), s.shiftKey ? s.selectedEdges.push(t) : s.selectedEdges = [t]), s.sendMessage("changed", {
+                                    nodes: s.selectedNodes,
+                                    edges: s.selectedEdges
                                 })
                             }
                         }))
                     },
                     computed: {
                         nodes() {
                             return this.data.nodes.map((e => ({
@@ -1485,27 +1564,27 @@
                         },
                         value() {
                             return this.data.value
                         }
                     },
                     methods: {
                         sendMessage(e, t) {
-                            S([this.pdata["name"], this.data["name"], e, t])
+                            D([this.pdata["name"], this.data["name"], e, t])
                         },
                         handleKeyDown(e) {
                             "Shift" == e.key && (this.shiftKey = !0)
                         },
                         handleKeyUp(e) {
                             "Shift" == e.key && (this.shiftKey = !1)
                         },
                         showClusterNode(e) {
                             const t = e.data("cluster"),
                                 a = this.cy.nodes(`[cluster='${t}']`),
-                                l = this.cy.nodes(`#${t}`);
-                            l.data("isClusterNode", !0), l.animate({
+                                s = this.cy.nodes(`#${t}`);
+                            s.data("isClusterNode", !0), s.animate({
                                 position: {
                                     x: e.position("x"),
                                     y: e.position("y")
                                 },
                                 width: a.boundingBox().w,
                                 height: a.boundingBox().h,
                                 duration: 300
@@ -1556,16 +1635,16 @@
                                 t.length && a.$(".highlighted").removeClass("highlighted");
                                 for (let t of e) a.edges("[id='" + t + "']").addClass("highlighted")
                             }
                         },
                         data: {
                             handler(e, t) {
                                 let a = e.value,
-                                    l = !1;
-                                if (void 0 !== a.nodes && this.selectedNodes != a.nodes && (this.selectedNodes = a.nodes), et(e.nodes, this.oldNodes) && (l = !0, this.oldNodes = e.nodes), void 0 !== a.edges && this.selectedEdges !== a.edges && (this.selectedEdges = a.edges), et(e.edges, this.oldEdges) && (l = !0, this.oldEdges = e.edges), l && null != this.cy) {
+                                    s = !1;
+                                if (void 0 !== a.nodes && this.selectedNodes != a.nodes && (this.selectedNodes = a.nodes), et(e.nodes, this.oldNodes) && (s = !0, this.oldNodes = e.nodes), void 0 !== a.edges && this.selectedEdges !== a.edges && (this.selectedEdges = a.edges), et(e.edges, this.oldEdges) && (s = !0, this.oldEdges = e.edges), s && null != this.cy) {
                                     this.cy.json({
                                         elements: {
                                             nodes: this.nodes,
                                             edges: this.edges
                                         }
                                     });
                                     let e = this.data.method;
@@ -1585,22 +1664,22 @@
                             this.cy.layout(e).run()
                         }
                     }
                 }),
                 at = (0, P.Z)(tt, [
                     ["render", Be]
                 ]),
-                lt = at;
+                st = at;
 
-            function st(e, t, a, i, n, o) {
-                const d = (0, l.up)("v-chart");
-                return (0, l.wg)(), (0, l.j4)(d, {
+            function lt(e, t, a, i, n, o) {
+                const d = (0, s.up)("v-chart");
+                return (0, s.wg)(), (0, s.j4)(d, {
                     ref: "chart",
                     option: n.options,
-                    style: (0, s.j5)(a.styleSize),
+                    style: (0, l.j5)(a.styleSize),
                     autoresize: !0
                 }, null, 8, ["option", "style"])
             }
             var it = a(7559),
                 nt = a(4447),
                 ot = a(1006),
                 dt = a(3526),
@@ -1629,15 +1708,18 @@
                             $q: e,
                             model: !1,
                             options: {
                                 responsive: !0,
                                 maintainAspectRatio: !1,
                                 legend: {
                                     data: [],
-                                    bottom: 10
+                                    bottom: 10,
+                                    textStyle: {
+                                        color: "#4DD0E1"
+                                    }
                                 },
                                 tooltip: {
                                     trigger: "axis",
                                     position: function(e) {
                                         return [e[0], "10%"]
                                     }
                                 },
@@ -1674,16 +1756,16 @@
                         }
                     },
                     methods: {
                         clicked(e) {
                             alert("!");
                             var t = [e.offsetX, e.offsetY],
                                 a = myChart.convertFromPixel("grid", t),
-                                l = myChart.getModel().get("xAxis")[0].data[a[0]];
-                            console.log(l)
+                                s = myChart.getModel().get("xAxis")[0].data[a[0]];
+                            console.log(s)
                         },
                         calcSeries() {
                             this.options.toolbox.feature.mySwitcher = {
                                 show: !0,
                                 title: "Switch view to the table",
                                 icon: "image:M0 2a2 2 0 0 1 2-2h12a2 2 0 0 1 2 2v12a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2V2zm15 2h-4v3h4V4zm0 4h-4v3h4V8zm0 4h-4v3h3a1 1 0 0 0 1-1v-2zm-5 3v-3H6v3h4zm-5 0v-3H1v2a1 1 0 0 0 1 1h3zm-4-4h4V8H1v3zm0-4h4V4H1v3zm5-3v3h4V4H6zm4 4H6v3h4V8z",
                                 onclick: () => {
@@ -1691,67 +1773,67 @@
                                     e.type = "table"
                                 }
                             };
                             let e = this.data.view,
                                 t = this.data.headers;
                             "_" != this.data.name[0] && (this.options.title.text = this.data.name);
                             let a = e.split("-"),
-                                l = a[1].split(",");
-                            l.unshift(a[0]);
-                            let s = [];
-                            for (let n = 0; n < l.length; n++) l[n] = "i" == l[n] ? -1 : parseInt(l[n]), s.push([]), n && (this.options.series.push({
-                                name: t[l[n]],
+                                s = a[1].split(",");
+                            s.unshift(a[0]);
+                            let l = [];
+                            for (let n = 0; n < s.length; n++) s[n] = "i" == s[n] ? -1 : parseInt(s[n]), l.push([]), n && (this.options.series.push({
+                                name: t[s[n]],
                                 type: "line",
                                 symbol: "none",
                                 sampling: "lttb",
                                 itemStyle: {
                                     color: ft[n]
                                 },
-                                data: s[n]
-                            }), this.options.legend.data.push(t[l[n]]));
-                            this.options.xAxis.data = s[0];
+                                data: l[n]
+                            }), this.options.legend.data.push(t[s[n]]));
+                            this.options.xAxis.data = l[0];
                             let i = this.data.rows;
                             for (let n = 0; n < i.length; n++)
-                                for (let e = 0; e < l.length; e++) s[e].push(-1 == l[e] ? n : i[n][l[e]]);
+                                for (let e = 0; e < s.length; e++) l[e].push(-1 == s[e] ? n : i[n][s[e]]);
                             this.$refs.chart.setOption(this.options), this.$refs.chart.chart.on("click", (e => alert("!")))
                         }
                     },
                     mounted() {
                         this.calcSeries()
                     }
                 },
                 wt = (0, P.Z)(yt, [
-                    ["render", st]
+                    ["render", lt]
                 ]),
                 bt = wt;
 
             function kt(e) {
                 let t = new FormData;
                 t.append("image", e);
                 let a = new XMLHttpRequest;
                 a.open("POST", k, !0), a.onload = function() {
                     200 === this.status ? console.log(this.response) : console.error(a)
                 }, a.send(t)
             }
-            const vt = (0, l.aZ)({
+            const vt = (0, s.aZ)({
                 name: "element",
                 components: {
                     utable: Ie,
-                    cgraph: lt,
+                    cgraph: st,
                     linechart: bt
                 },
                 methods: {
                     log(e) {
                         console.log(e)
                     },
                     onAdded(e) {
                         0 !== e.length && (0 !== this.fileArr.length ? (this.$refs.uploaderRef.removeFile(this.fileArr[0]), this.fileArr.splice(0, 1, e[0])) : this.fileArr.push(e[0]))
                     },
                     sendMessage(e, t) {
-                        S([this.pdata["name"], this.data["name"], e, t])
+                        D([this.pdata["name"], this.data["name"], e, t])
                     },
                     pressedEnter() {
                         "update" in this.data && this.sendMessage("update", this.value)
                     },
                     updateDom(e) {
                         let t = e.files.length;
                         t && this.sendMessage("changed", e.xhr.responseText)
@@ -1814,36 +1896,37 @@
                         return e.getBoundingClientRect()
                     },
                     geom() {
                         let e = "clientHeight" in this.$el ? this.$el : this.$el.nextElementSibling;
                         e || (e = this.$el.previousElementSibling, e = "clientHeight" in e ? e : e.nextElementSibling);
                         let t = this.type;
                         const a = "docviewer" == t || "graph" == t || "linechart" == t ? e : e.querySelector("table" == t ? ".scroll" : ".q-tree"),
-                            l = e.getBoundingClientRect();
+                            s = e.getBoundingClientRect();
                         return {
                             el: e,
                             inner: a,
-                            left: l.left,
-                            right: l.right,
-                            top: l.top,
+                            left: s.left,
+                            right: s.right,
+                            top: s.top,
                             scrollHeight: a.scrollHeight,
                             scrollWidth: a.scrollWidth
                         }
                     }
                 },
                 updated() {
-                    q[this.fullname] = this
+                    _[this.fullname] = this
                 },
                 mounted() {
-                    q[this.fullname] = this, this.data.focus && this.$refs.inputRef.$el.focus()
+                    _[this.fullname] = this, this.data.focus && this.$refs.inputRef.$el.focus()
                 },
                 data() {
                     return {
+                        Dark: Ve.Z,
                         value: this.data.value,
-                        styleSize: D(`${this.data.name}@${this.pdata.name}`, this.data),
+                        styleSize: $(this),
                         host_path: k,
                         options: [],
                         expandedKeys: [],
                         thumbStyle: {
                             right: "4px",
                             borderRadius: "7px",
                             backgroundColor: "#027be3",
@@ -1915,25 +1998,25 @@
                     treeNodes() {
                         var e = [];
                         if ("list" == this.type) return this.data.options.map((e => ({
                             label: e,
                             children: []
                         })));
                         var t = {};
-                        for (const [s, i] of Object.entries(this.data.options)) {
-                            var a = t[s];
+                        for (const [l, i] of Object.entries(this.data.options)) {
+                            var a = t[l];
                             if (a || (a = {
-                                    label: s,
+                                    label: l,
                                     children: []
-                                }, t[s] = a), i) {
-                                var l = t[i];
-                                l || (l = {
+                                }, t[l] = a), i) {
+                                var s = t[i];
+                                s || (s = {
                                     label: i,
                                     children: []
-                                }, t[i] = l), l.children.push(a)
+                                }, t[i] = s), s.children.push(a)
                             } else e.push(a)
                         }
                         return e
                     }
                 },
                 props: {
                     data: {
@@ -1953,56 +2036,57 @@
                         Array.isArray(e) || (e = [0, 0]);
                         let t = this.$refs.inputRef.$el;
                         t.focus();
                         let a = t.getElementsByTagName("textarea");
                         0 == a.length && (a = t.getElementsByTagName("input")), a[0].setSelectionRange(e[0], e[1])
                     },
                     data(e, t) {
-                        this.styleSize || (this.styleSize = finitStyle(this.data)), this.value = this.data.value, this.updated = this.value, q[this.fullname] = this
+                        this.styleSize || (this.styleSize = finitStyle(this.data)), this.value = this.data.value, this.updated = this.value, _[this.fullname] = this
                     }
                 }
             });
             var xt = a(4027),
                 Ct = a(9721),
-                qt = a(8886),
-                _t = a(8761),
-                jt = a(1232),
-                St = a(5551),
-                zt = a(5869),
-                At = a(1745),
-                Zt = a(8430);
-            const $t = (0, P.Z)(vt, [
-                    ["render", Ae],
-                    ["__scopeId", "data-v-9259610c"]
+                _t = a(8886),
+                qt = a(8761),
+                At = a(1232),
+                Dt = a(5551),
+                St = a(5869),
+                jt = a(1745),
+                zt = a(8430);
+            const Zt = (0, P.Z)(vt, [
+                    ["render", Se],
+                    ["__scopeId", "data-v-591efd84"]
                 ]),
-                Dt = $t;
+                $t = Zt;
             X()(vt, "components", {
                 QImg: xt.Z,
                 QIcon: L.Z,
                 QSelect: Pe.Z,
                 QBadge: Ct.Z,
                 QCheckbox: Te.Z,
-                QToggle: qt.Z,
+                QToggle: _t.Z,
                 QBtn: He.Z,
-                QBtnToggle: _t.Z,
-                QInput: Oe.Z,
-                QScrollArea: jt.Z,
-                QTree: St.Z,
-                QSeparator: zt.Z,
-                QUploader: At.Z,
-                QTooltip: Qe.Z,
-                QSpinnerPuff: Zt.Z
+                QBtnToggle: qt.Z,
+                QInput: Qe.Z,
+                QScrollArea: At.Z,
+                QTree: Dt.Z,
+                QSeparator: St.Z,
+                QUploader: jt.Z,
+                QTooltip: Oe.Z,
+                QSpinnerPuff: zt.Z
             });
-            const Mt = (0, l.aZ)({
+            const Mt = (0, s.aZ)({
                 name: "block",
                 components: {
-                    element: Dt
+                    element: $t
                 },
                 data() {
                     return {
+                        Dark: Ve.Z,
                         styleSize: y,
                         thumbStyle: {
                             right: "4px",
                             borderRadius: "7px",
                             backgroundColor: "#027be3",
                             width: "4px",
                             opacity: .75
@@ -2032,15 +2116,15 @@
                             top: a.top,
                             scrollHeight: window.innerHeight,
                             scrollWidth: window.innerWidth
                         }
                     }
                 },
                 mounted() {
-                    C[this.name] = this, this.expanding && (q[this.fullname] = this)
+                    C[this.name] = this, this.expanding && (_[this.fullname] = this)
                 },
                 computed: {
                     name() {
                         return this.data.name
                     },
                     fullname() {
                         return `_scroll@${this.name}`
@@ -2066,94 +2150,94 @@
                     data: {
                         type: Object,
                         required: !0
                     }
                 },
                 watch: {
                     data(e) {
-                        g && console.log("data update", this.name), C[this.name] = this, this.expanding && (this.styleSize = D(this.fullname, this.data), q[this.fullname] = this)
+                        g && console.log("data update", this.name), C[this.name] = this, this.expanding && (this.styleSize = $(this), _[this.fullname] = this)
                     }
                 }
             });
             var Vt = a(151);
             const Et = (0, P.Z)(Mt, [
-                    ["render", ce]
+                    ["render", re]
                 ]),
-                Kt = Et;
+                Wt = Et;
 
-            function Wt() {
-                let e = Z && q.size == _.size;
+            function Kt() {
+                let e = z && _.size == q.size;
                 if (e)
-                    for (let [t, a] of Object.entries(q))
-                        if (!_[t]) {
+                    for (let [t, a] of Object.entries(_))
+                        if (!q[t]) {
                             e = !1;
                             break
-                        } e || (U(), (0, l.Y3)((() => {
+                        } e || (U(), (0, s.Y3)((() => {
                     requestAnimationFrame((() => {
                         requestAnimationFrame((() => {
                             h.visible(!0)
                         }))
                     }))
                 })))
             }
             X()(Mt, "components", {
                 QCard: Vt.Z,
                 QIcon: L.Z,
-                QScrollArea: jt.Z
+                QScrollArea: At.Z
             });
-            const Ot = (0, l.aZ)({
+            const Qt = (0, s.aZ)({
                     name: "zone",
                     components: {
-                        block: Kt
+                        block: Wt
                     },
                     props: {
                         data: Object
                     },
                     updated(e) {
-                        (0, l.Y3)((() => {
+                        (0, s.Y3)((() => {
                             requestAnimationFrame((() => {
-                                requestAnimationFrame(Wt)
+                                requestAnimationFrame(Kt)
                             }))
                         }))
                     }
                 }),
-                Qt = (0, P.Z)(Ot, [
-                    ["render", le]
+                Ot = (0, P.Z)(Qt, [
+                    ["render", se]
                 ]),
-                Ht = Qt,
+                Ht = Ot,
                 Ut = {
                     class: "row q-gutter-sm row-md"
                 };
 
             function Nt(e, t, a, i, n, o) {
-                const d = (0, l.up)("block"),
-                    r = (0, l.up)("q-item-label"),
-                    c = (0, l.up)("q-space"),
-                    h = (0, l.up)("q-btn"),
-                    u = (0, l.up)("q-card"),
-                    p = (0, l.up)("q-dialog");
-                return (0, l.wg)(), (0, l.j4)(p, {
+                const d = (0, s.up)("block"),
+                    r = (0, s.up)("q-item-label"),
+                    c = (0, s.up)("q-space"),
+                    h = (0, s.up)("q-btn"),
+                    u = (0, s.up)("q-card"),
+                    p = (0, s.up)("q-dialog");
+                return (0, s.wg)(), (0, s.j4)(p, {
                     ref: "dialog",
                     onHide: o.onDialogHide,
-                    onKeyup: (0, he.D2)(o.pressedEnter, ["enter"])
+                    onKeyup: (0, ce.D2)(o.pressedEnter, ["enter"])
                 }, {
-                    default: (0, l.w5)((() => [(0, l.Wm)(u, {
+                    default: (0, s.w5)((() => [(0, s.Wm)(u, {
                         class: "q-dialog-plugin q-pa-md items-start q-gutter-md",
                         bordered: "",
-                        style: (0, s.j5)(a.data.internal ? "width: 800px; max-width: 80vw;" : "")
+                        style: (0, l.j5)(a.data.internal ? "width: 800px; max-width: 80vw;" : "")
                     }, {
-                        default: (0, l.w5)((() => [a.data ? ((0, l.wg)(), (0, l.j4)(d, {
+                        default: (0, s.w5)((() => [a.data ? ((0, s.wg)(), (0, s.j4)(d, {
                             key: 0,
                             data: a.data
-                        }, null, 8, ["data"])) : (0, l.kq)("", !0), (0, l.Wm)(r, {
+                        }, null, 8, ["data"])) : (0, s.kq)("", !0), (0, s.Wm)(r, {
                             class: "text-h6"
                         }, {
-                            default: (0, l.w5)((() => [(0, l.Uk)((0, s.zw)(a.data.text ? a.data.text : ""), 1)])),
+                            default: (0, s.w5)((() => [(0, s.Uk)((0, l.zw)(a.data.text ? a.data.text : ""), 1)])),
                             _: 1
-                        }), (0, l._)("div", Ut, [(0, l.Wm)(c), ((0, l.wg)(!0), (0, l.iD)(l.HY, null, (0, l.Ko)(a.buttons, (e => ((0, l.wg)(), (0, l.j4)(h, {
+                        }), (0, s._)("div", Ut, [(0, s.Wm)(c), ((0, s.wg)(!0), (0, s.iD)(s.HY, null, (0, s.Ko)(a.buttons, (e => ((0, s.wg)(), (0, s.j4)(h, {
                             class: "col-md-3",
                             label: e,
                             color: a.buttons[0] == e ? "primary" : "secondary",
                             onClick: t => o.sendMessage(e)
                         }, null, 8, ["label", "color", "onClick"])))), 256))])])),
                         _: 1
                     }, 8, ["style"])])),
@@ -2162,23 +2246,23 @@
             }
             const Ft = {
                 props: {
                     data: Object,
                     buttons: Array
                 },
                 components: {
-                    block: Kt
+                    block: Wt
                 },
                 emits: ["ok", "hide"],
                 methods: {
                     show() {
                         this.$refs.dialog.show()
                     },
                     sendMessage(e) {
-                        this.data.internal || S([this.data["name"], e]), this.hide()
+                        this.data.internal || D([this.data["name"], e]), this.hide()
                     },
                     hide() {
                         this.$refs.dialog.hide()
                     },
                     onDialogHide() {
                         this.$emit("hide")
                     },
@@ -2203,108 +2287,110 @@
                 QDialog: Tt.Z,
                 QCard: Vt.Z,
                 QItemLabel: B.Z,
                 QSpace: Pt.Z,
                 QBtn: He.Z
             });
             let Lt = null;
-            const Bt = (0, l.aZ)({
+            const Bt = (0, s.aZ)({
                 name: "MainLayout",
                 data() {
                     return {
                         leftDrawerOpen: !1,
+                        Dark: Ve.Z,
                         menu: [],
                         tab: "",
                         tooldata: {
                             name: "toolbar"
                         },
                         localServer: !0,
                         statusConnect: !1,
                         screen: {
                             blocks: []
-                        }
+                        },
+                        visibility: !1
                     }
                 },
                 components: {
                     menubar: J,
                     zone: Ht,
-                    element: Dt
+                    element: $t
                 },
                 created() {
-                    j(this)
+                    A(this)
                 },
                 unmounted() {
                     window.removeEventListener("resize", this.onResize)
                 },
                 methods: {
                     toggleLeftDrawer() {
                         this.leftDrawerOpen = !this.leftDrawerOpen
                     },
                     tabclick(e) {
-                        S(["root", e])
+                        D(["root", e])
                     },
                     visible(e) {
-                        this.$refs.page.$el.style.visibility = e ? "" : "hidden"
+                        this.$refs.page.$el.style.visibility = e ? "" : "hidden", this.visibility = e
                     },
                     onResize(e) {
                         g && console.log("window has been resized", window.innerHeight, window.innerWidth), H()
                     },
                     lens(e) {
                         let t = {
                                 title: "Photo lens",
                                 message: e.text,
                                 cancel: !0,
                                 persistent: !0,
                                 component: It
                             },
                             {
                                 height: a,
-                                ...l
+                                ...s
                             } = e;
-                        l.width = 750;
-                        let s = {
+                        s.width = 750;
+                        let l = {
                             name: `Picture lens of ${e.name}`,
                             value: [
-                                [], l
+                                [], s
                             ],
                             internal: !0
                         };
                         t.componentProps = {
-                            data: s,
+                            data: l,
                             buttons: ["Close"]
                         }, this.$q.dialog(t)
                     },
                     notify(e, t) {
                         let a = t,
-                            l = {
+                            s = {
                                 message: e,
                                 type: t,
                                 position: "top",
                                 icon: a
                             };
-                        "progress" == t ? null == Lt ? (l = {
+                        "progress" == t ? null == Lt ? (s = {
                             group: !1,
                             timeout: 0,
                             spinner: !0,
                             type: "info",
                             message: e || "Progress..",
                             position: "top",
                             color: "secondary"
-                        }, Lt = this.$q.notify(l)) : null == e ? (Lt(), Lt = null) : (l = {
+                        }, Lt = this.$q.notify(s)) : null == e ? (Lt(), Lt = null) : (s = {
                             caption: e
-                        }, Lt(l)) : ("error" == t && l.type, this.$q.notify(l))
+                        }, Lt(s)) : ("error" == t && s.type, this.$q.notify(s))
                     },
                     error(e) {
                         this.notify(e, "error")
                     },
                     info(e) {
                         this.notify(e, "info")
                     },
                     processMessage(e) {
-                        if ("screen" == e.type) V(), this.screen.name != e.name && ($(!1), this.visible(!1)), this.screen = e, this.menu = e.menu.map((e => ({
+                        if ("screen" == e.type) V(), this.screen.name != e.name && (Z(!1), this.visible(!1)), this.screen = e, this.menu = e.menu.map((e => ({
                             name: e[0],
                             icon: e[1],
                             order: e[2]
                         }))), this.tab = this.screen.name;
                         else if ("dialog" == e.type) {
                             let t = {
                                 title: e.name,
@@ -2312,17 +2398,17 @@
                                 cancel: !0,
                                 persistent: !0
                             };
                             t.component = It, t.componentProps = {
                                 data: e.content ? e.content : e,
                                 buttons: e.buttons
                             }, this.$q.dialog(t)
-                        } else if ("answer" == e.type) W(e);
+                        } else if ("answer" == e.type) K(e);
                         else {
-                            e.updates && K(e.updates);
+                            e.updates && W(e.updates);
                             let t = !1;
                             ["error", "progress", "warning", "info"].includes(e.type) && (this.notify(e.value, e.type), t = !0), t || e.updates || (this.error("Invalid data came from the server! Look the console."), console.log(`Invalid data came from the server! ${e}`))
                         }
                         Lt && "progress" != e.type && this.notify(null, "progress")
                     }
                 },
                 mounted() {
@@ -2332,25 +2418,27 @@
             var Yt = a(9214),
                 Xt = a(3812),
                 Gt = a(9570),
                 Jt = a(7547),
                 ea = a(3269),
                 ta = a(2652),
                 aa = a(4379);
-            const la = (0, P.Z)(Bt, [
+            const sa = (0, P.Z)(Bt, [
                     ["render", o]
                 ]),
-                sa = la;
+                la = sa;
             X()(Bt, "components", {
                 QLayout: Yt.Z,
                 QHeader: Xt.Z,
                 QToolbar: Gt.Z,
                 QBtn: He.Z,
                 QItemLabel: B.Z,
                 QTabs: Jt.Z,
                 QTab: ea.Z,
+                QSpace: Pt.Z,
+                QTooltip: Oe.Z,
                 QPageContainer: ta.Z,
                 QPage: aa.Z
             })
         }
     }
 ]);
```

### Comparing `unigui-1.9.0/unigui/web/js/430.591e9a73.js` & `unigui-1.9.1/unigui/web/js/430.591e9a73.js`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/js/vendor.3076c5e7.js` & `unigui-1.9.1/unigui/web/js/vendor.18cce91f.js`

 * *Files 0% similar despite different names*

#### js-beautify {}

```diff
@@ -14193,19 +14193,19 @@
                         void 0 !== e.config.iconMapFn && (this.iconMapFn = e.config.iconMapFn), e.iconSet = this.__icons, (0, i.g)(e, "iconMapFn", (() => this.iconMapFn), (e => {
                             this.iconMapFn = e
                         })), !0 === this.__installed ? void 0 !== t && this.set(t) : this.set(t || o)
                     }
                 }),
                 s = a
         },
-        8242: (e, t, n) => {
+        112: (e, t, n) => {
             "use strict";
             n.d(t, {
-                $: () => M,
-                Z: () => I
+                $: () => T,
+                Z: () => E
             });
             var r = n(8880),
                 i = n(4688),
                 o = (n(71), n(2002)),
                 a = n(4716),
                 s = n(9405);
             const l = ["sm", "md", "lg", "xl"],
@@ -14277,157 +14277,122 @@
                             }, this.setDebounce = e => {
                                 void 0 !== d && r.removeEventListener("resize", d, u), d = e > 0 ? (0, s.Z)(this.__update, e) : this.__update, r.addEventListener("resize", d, u)
                             }, this.setDebounce(f), 0 !== Object.keys(h).length ? (this.setSizes(h), h = void 0) : this.__update(), !0 === c && "xs" === this.name && document.body.classList.add("screen--xs")
                         };
                         !0 === i.uX.value ? t.push(p) : p()
                     }
                 });
+            var d = n(9058),
+                h = n(6583),
+                f = n(9111);
             n(5363);
-            const d = (0, o.Z)({
-                    isActive: !1,
-                    mode: !1
-                }, {
-                    __media: void 0,
-                    set(e) {
-                        d.mode = e, "auto" === e ? (void 0 === d.__media && (d.__media = window.matchMedia("(prefers-color-scheme: dark)"), d.__updateMedia = () => {
-                            d.set("auto")
-                        }, d.__media.addListener(d.__updateMedia)), e = d.__media.matches) : void 0 !== d.__media && (d.__media.removeListener(d.__updateMedia), d.__media = void 0), d.isActive = !0 === e, document.body.classList.remove("body--" + (!0 === e ? "light" : "dark")), document.body.classList.add("body--" + (!0 === e ? "dark" : "light"))
-                    },
-                    toggle() {
-                        d.set(!1 === d.isActive)
-                    },
-                    install({
-                        $q: e,
-                        onSSRHydrated: t,
-                        ssrContext: n
-                    }) {
-                        const {
-                            dark: r
-                        } = e.config;
-                        if (e.dark = this, !0 === this.__installed && void 0 === r) return;
-                        this.isActive = !0 === r;
-                        const o = void 0 !== r && r;
-                        if (!0 === i.uX.value) {
-                            const e = e => {
-                                    this.__fromSSR = e
-                                },
-                                n = this.set;
-                            this.set = e, e(o), t.push((() => {
-                                this.set = n, this.set(this.__fromSSR)
-                            }))
-                        } else this.set(o)
-                    }
-                }),
-                h = d;
-            var f = n(6583),
-                p = n(9111);
 
-            function v(e, t, n = document.body) {
+            function p(e, t, n = document.body) {
                 if ("string" !== typeof e) throw new TypeError("Expected a string as propName");
                 if ("string" !== typeof t) throw new TypeError("Expected a string as value");
                 if (!(n instanceof Element)) throw new TypeError("Expected a DOM element");
                 n.style.setProperty(`--q-${e}`, t)
             }
-            var g = n(1436);
+            var v = n(1436);
 
-            function m(e) {
+            function g(e) {
                 return !0 === e.ios ? "ios" : !0 === e.android ? "android" : void 0
             }
 
-            function y({
+            function m({
                 is: e,
                 has: t,
                 within: n
             }, r) {
                 const i = [!0 === e.desktop ? "desktop" : "mobile", (!1 === t.touch ? "no-" : "") + "touch"];
                 if (!0 === e.mobile) {
-                    const t = m(e);
+                    const t = g(e);
                     void 0 !== t && i.push("platform-" + t)
                 }
                 if (!0 === e.nativeMobile) {
                     const t = e.nativeMobileWrapper;
                     i.push(t), i.push("native-mobile"), !0 !== e.ios || void 0 !== r[t] && !1 === r[t].iosStatusBarPadding || i.push("q-ios-padding")
                 } else !0 === e.electron ? i.push("electron") : !0 === e.bex && i.push("bex");
                 return !0 === n.iframe && i.push("within-iframe"), i
             }
 
-            function b() {
+            function y() {
                 const {
                     is: e
                 } = i.Lp, t = document.body.className, n = new Set(t.replace(/ {2}/g, " ").split(" "));
                 if (void 0 !== i.aG) n.delete("desktop"), n.add("platform-ios"), n.add("mobile");
                 else if (!0 !== e.nativeMobile && !0 !== e.electron && !0 !== e.bex)
                     if (!0 === e.desktop) n.delete("mobile"), n.delete("platform-ios"), n.delete("platform-android"), n.add("desktop");
                     else if (!0 === e.mobile) {
                     n.delete("desktop"), n.add("mobile");
-                    const t = m(e);
+                    const t = g(e);
                     void 0 !== t ? (n.add(`platform-${t}`), n.delete("platform-" + ("ios" === t ? "android" : "ios"))) : (n.delete("platform-ios"), n.delete("platform-android"))
                 }!0 === i.Lp.has.touch && (n.delete("no-touch"), n.add("touch")), !0 === i.Lp.within.iframe && n.add("within-iframe");
                 const r = Array.from(n).join(" ");
                 t !== r && (document.body.className = r)
             }
 
-            function _(e) {
-                for (const t in e) v(t, e[t])
+            function b(e) {
+                for (const t in e) p(t, e[t])
             }
-            const x = {
+            const _ = {
                 install(e) {
                     if (!0 !== this.__installed) {
-                        if (!0 === i.uX.value) b();
+                        if (!0 === i.uX.value) y();
                         else {
                             const {
                                 $q: t
                             } = e;
-                            void 0 !== t.config.brand && _(t.config.brand);
-                            const n = y(i.Lp, t.config);
+                            void 0 !== t.config.brand && b(t.config.brand);
+                            const n = m(i.Lp, t.config);
                             document.body.classList.add.apply(document.body.classList, n)
-                        }!0 === i.Lp.is.ios && document.body.addEventListener("touchstart", a.ZT), window.addEventListener("keydown", g.ZK, !0)
+                        }!0 === i.Lp.is.ios && document.body.addEventListener("touchstart", a.ZT), window.addEventListener("keydown", v.ZK, !0)
                     }
                 }
             };
-            var w = n(9409),
-                S = n(2547),
-                k = n(5578),
-                C = n(2162);
-            const T = [i.ZP, x, h, c, f.Z, p.Z, w.Z];
+            var x = n(9409),
+                w = n(2547),
+                S = n(5578),
+                k = n(2162);
+            const C = [i.ZP, _, d.Z, c, h.Z, f.Z, x.Z];
 
-            function M(e, t) {
+            function T(e, t) {
                 const n = (0, r.ri)(e);
                 n.config.globalProperties = t.config.globalProperties;
                 const {
                     reload: i,
                     ...o
                 } = t._context;
                 return Object.assign(n._context, o), n
             }
 
-            function D(e, t) {
+            function M(e, t) {
                 t.forEach((t => {
                     t.install(e), t.__installed = !0
                 }))
             }
 
-            function E(e, t, n) {
-                e.config.globalProperties.$q = n.$q, e.provide(S.Ng, n.$q), D(n, T), void 0 !== t.components && Object.values(t.components).forEach((t => {
-                    !0 === (0, C.Kn)(t) && void 0 !== t.name && e.component(t.name, t)
+            function D(e, t, n) {
+                e.config.globalProperties.$q = n.$q, e.provide(w.Ng, n.$q), M(n, C), void 0 !== t.components && Object.values(t.components).forEach((t => {
+                    !0 === (0, k.Kn)(t) && void 0 !== t.name && e.component(t.name, t)
                 })), void 0 !== t.directives && Object.values(t.directives).forEach((t => {
-                    !0 === (0, C.Kn)(t) && void 0 !== t.name && e.directive(t.name, t)
-                })), void 0 !== t.plugins && D(n, Object.values(t.plugins).filter((e => "function" === typeof e.install && !1 === T.includes(e)))), !0 === i.uX.value && (n.$q.onSSRHydrated = () => {
+                    !0 === (0, k.Kn)(t) && void 0 !== t.name && e.directive(t.name, t)
+                })), void 0 !== t.plugins && M(n, Object.values(t.plugins).filter((e => "function" === typeof e.install && !1 === C.includes(e)))), !0 === i.uX.value && (n.$q.onSSRHydrated = () => {
                     n.onSSRHydrated.forEach((e => {
                         e()
                     })), n.$q.onSSRHydrated = () => {}
                 })
             }
-            const I = function(e, t = {}) {
+            const E = function(e, t = {}) {
                 const n = {
                     version: "2.12.2"
                 };
-                !1 === k.Uf ? (void 0 !== t.config && Object.assign(k.w6, t.config), n.config = {
-                    ...k.w6
-                }, (0, k.tP)()) : n.config = t.config || {}, E(e, t, {
+                !1 === S.Uf ? (void 0 !== t.config && Object.assign(S.w6, t.config), n.config = {
+                    ...S.w6
+                }, (0, S.tP)()) : n.config = t.config || {}, D(e, t, {
                     parentApp: e,
                     $q: n,
                     lang: t.lang,
                     iconSet: t.iconSet,
                     onSSRHydrated: []
                 })
             }
@@ -14555,14 +14520,59 @@
                         ssrContext: n
                     }) {
                         e.lang = a.__langPack, a.__langConfig = e.config.lang, !0 === this.__installed ? void 0 !== t && this.set(t) : this.set(t || i)
                     }
                 }),
                 s = a
         },
+        9058: (e, t, n) => {
+            "use strict";
+            n.d(t, {
+                Z: () => a
+            });
+            n(5363);
+            var r = n(2002),
+                i = n(4688);
+            const o = (0, r.Z)({
+                    isActive: !1,
+                    mode: !1
+                }, {
+                    __media: void 0,
+                    set(e) {
+                        o.mode = e, "auto" === e ? (void 0 === o.__media && (o.__media = window.matchMedia("(prefers-color-scheme: dark)"), o.__updateMedia = () => {
+                            o.set("auto")
+                        }, o.__media.addListener(o.__updateMedia)), e = o.__media.matches) : void 0 !== o.__media && (o.__media.removeListener(o.__updateMedia), o.__media = void 0), o.isActive = !0 === e, document.body.classList.remove("body--" + (!0 === e ? "light" : "dark")), document.body.classList.add("body--" + (!0 === e ? "dark" : "light"))
+                    },
+                    toggle() {
+                        o.set(!1 === o.isActive)
+                    },
+                    install({
+                        $q: e,
+                        onSSRHydrated: t,
+                        ssrContext: n
+                    }) {
+                        const {
+                            dark: r
+                        } = e.config;
+                        if (e.dark = this, !0 === this.__installed && void 0 === r) return;
+                        this.isActive = !0 === r;
+                        const o = void 0 !== r && r;
+                        if (!0 === i.uX.value) {
+                            const e = e => {
+                                    this.__fromSSR = e
+                                },
+                                n = this.set;
+                            this.set = e, e(o), t.push((() => {
+                                this.set = n, this.set(this.__fromSSR)
+                            }))
+                        } else this.set(o)
+                    }
+                }),
+                a = o
+        },
         5597: (e, t, n) => {
             "use strict";
             n.d(t, {
                 Z: () => F
             });
             var r = n(3673),
                 i = n(1959),
@@ -14972,15 +14982,15 @@
                     }), () => (0, r.h)(o.Z, {
                         ref: d,
                         onHide: R
                     }, H)
                 }
             });
             n(71);
-            var O = n(8242),
+            var O = n(112),
                 L = n(8144);
 
             function R(e, t) {
                 for (const n in t) "spinner" !== n && Object(t[n]) === t[n] ? (e[n] = Object(e[n]) !== e[n] ? {} : {
                     ...e[n]
                 }, R(e[n], t[n])) : e[n] = t[n]
             }
@@ -15124,15 +15134,15 @@
                         }, (0, u.pf)(t.default, s))])
                     }
                 }
             });
             var d = n(2165),
                 h = n(6833),
                 f = (n(4716), n(8144)),
-                p = n(8242),
+                p = n(112),
                 v = n(2162);
             let g = 0;
             const m = {},
                 y = {},
                 b = {},
                 _ = {},
                 x = /^\s*$/,
@@ -16452,15 +16462,15 @@
             }
         },
         9592: (e, t, n) => {
             "use strict";
             n.d(t, {
                 Z: () => a
             });
-            var r = n(8242),
+            var r = n(112),
                 i = n(9111),
                 o = n(9409);
             const a = {
                 version: "2.12.2",
                 install: r.Z,
                 lang: i.Z,
                 iconSet: o.Z
```

### Comparing `unigui-1.9.0/unigui/web/js/app.fb1ab18a.js` & `unigui-1.9.1/unigui/web/js/app.c7c500ce.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -22,15 +22,15 @@
                         ["render", l]
                     ]),
                     d = c;
                 var p = r(3340),
                     f = r(8339);
                 const h = [{
                         path: "/",
-                        component: () => Promise.all([r.e(736), r.e(615)]).then(r.bind(r, 9615)),
+                        component: () => Promise.all([r.e(736), r.e(9)]).then(r.bind(r, 6009)),
                         children: [{
                             path: "",
                             component: () => Promise.all([r.e(736), r.e(430)]).then(r.bind(r, 6430))
                         }]
                     }, {
                         path: "/:catchAll(.*)*",
                         component: () => Promise.all([r.e(736), r.e(193)]).then(r.bind(r, 2193))
@@ -158,25 +158,25 @@
                 get: t[n]
             })
         }
     })(), (() => {
         r.f = {}, r.e = e => Promise.all(Object.keys(r.f).reduce(((t, n) => (r.f[n](e, t), t)), []))
     })(), (() => {
         r.u = e => "js/" + e + "." + {
+            9: "100130f6",
             193: "283445be",
-            430: "591e9a73",
-            615: "04cc6ad4"
+            430: "591e9a73"
         } [e] + ".js"
     })(), (() => {
         r.miniCssF = e => "css/" + ({
             143: "app",
             736: "vendor"
         } [e] || e) + "." + {
+            9: "44b298e4",
             143: "31d6cfe0",
-            615: "3024385a",
             736: "191faa77"
         } [e] + ".css"
     })(), (() => {
         r.g = function() {
             if ("object" === typeof globalThis) return globalThis;
             try {
                 return this || new Function("return this")()
@@ -260,15 +260,15 @@
                 e(n, l, o, a)
             })),
             o = {
                 143: 0
             };
         r.f.miniCss = (e, t) => {
             var r = {
-                615: 1
+                9: 1
             };
             o[e] ? t.push(o[e]) : 0 !== o[e] && r[e] && t.push(o[e] = n(e).then((() => {
                 o[e] = 0
             }), (t => {
                 throw delete o[e], t
             })))
         }
```

### Comparing `unigui-1.9.0/unigui/web/js/193.283445be.js` & `unigui-1.9.1/unigui/web/js/193.283445be.js`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui/web/index.html` & `unigui-1.9.1/unigui/web/index.html`

 * *Files 4% similar despite different names*

```diff
@@ -1 +1 @@
-<!DOCTYPE html><html><head><title>Unigui</title><meta charset=utf-8><meta name=description content="Unigui on Quasar"><meta name=format-detection content="telephone=no"><meta name=msapplication-tap-highlight content=no><meta name=viewport content="user-scalable=no,initial-scale=1,maximum-scale=1,minimum-scale=1,width=device-width"><link rel=icon type=image/png sizes=128x128 href=icons/favicon-128x128.png><link rel=icon type=image/png sizes=96x96 href=icons/favicon-96x96.png><link rel=icon type=image/png sizes=32x32 href=icons/favicon-32x32.png><link rel=icon type=image/png sizes=16x16 href=icons/favicon-16x16.png><link rel=icon type=image/ico href=favicon.ico><script defer src=js/vendor.3076c5e7.js></script><script defer src=js/app.fb1ab18a.js></script><link href=css/vendor.191faa77.css rel=stylesheet><link href=css/app.31d6cfe0.css rel=stylesheet></head><body><div id=q-app></div></body></html>
+<!DOCTYPE html><html><head><title>Unigui</title><meta charset=utf-8><meta name=description content="Unigui on Quasar"><meta name=format-detection content="telephone=no"><meta name=msapplication-tap-highlight content=no><meta name=viewport content="user-scalable=no,initial-scale=1,maximum-scale=1,minimum-scale=1,width=device-width"><link rel=icon type=image/png sizes=128x128 href=icons/favicon-128x128.png><link rel=icon type=image/png sizes=96x96 href=icons/favicon-96x96.png><link rel=icon type=image/png sizes=32x32 href=icons/favicon-32x32.png><link rel=icon type=image/png sizes=16x16 href=icons/favicon-16x16.png><link rel=icon type=image/ico href=favicon.ico><script defer src=js/vendor.18cce91f.js></script><script defer src=js/app.c7c500ce.js></script><link href=css/vendor.191faa77.css rel=stylesheet><link href=css/app.31d6cfe0.css rel=stylesheet></head><body><div id=q-app></div></body></html>
```

### Comparing `unigui-1.9.0/LICENSE` & `unigui-1.9.1/LICENSE`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/setup.py` & `unigui-1.9.1/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 from setuptools import setup, find_packages
  
 setup(name='unigui',
-      version='1.9.0',      
+      version='1.9.1',      
       license='MIT',
       author='Georgii Dernovyi',
       author_email='g.dernovoy@gmail.com',
       description='Unigui - Universal GUI Framework and protocol',
       packages=find_packages(exclude=['tests']),
       long_description=open('README.md').read(),
       long_description_content_type="text/markdown",
```

### Comparing `unigui-1.9.0/PKG-INFO` & `unigui-1.9.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: unigui
-Version: 1.9.0
+Version: 1.9.1
 Summary: Unigui - Universal GUI Framework and protocol
 Home-page: https://github.com/Claus1/unigui
 Author: Georgii Dernovyi
 Author-email: g.dernovoy@gmail.com
 License: MIT
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
```

### Comparing `unigui-1.9.0/README.md` & `unigui-1.9.1/README.md`

 * *Files identical despite different names*

### Comparing `unigui-1.9.0/unigui.egg-info/PKG-INFO` & `unigui-1.9.1/unigui.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: unigui
-Version: 1.9.0
+Version: 1.9.1
 Summary: Unigui - Universal GUI Framework and protocol
 Home-page: https://github.com/Claus1/unigui
 Author: Georgii Dernovyi
 Author-email: g.dernovoy@gmail.com
 License: MIT
 Platform: UNKNOWN
 Description-Content-Type: text/markdown
```

### Comparing `unigui-1.9.0/unigui.egg-info/SOURCES.txt` & `unigui-1.9.1/unigui.egg-info/SOURCES.txt`

 * *Files 5% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 unigui.egg-info/SOURCES.txt
 unigui.egg-info/dependency_links.txt
 unigui.egg-info/not-zip-safe
 unigui.egg-info/requires.txt
 unigui.egg-info/top_level.txt
 unigui/web/favicon.ico
 unigui/web/index.html
-unigui/web/css/615.3024385a.css
+unigui/web/css/9.44b298e4.css
 unigui/web/css/app.31d6cfe0.css
 unigui/web/css/vendor.191faa77.css
 unigui/web/css/vendor.191faa77.css.gz
 unigui/web/fonts/KFOkCnqEu92Fr1MmgVxIIzQ.68bb21d0.woff
 unigui/web/fonts/KFOlCnqEu92Fr1MmEU9fBBc-.48af7707.woff
 unigui/web/fonts/KFOlCnqEu92Fr1MmSU5fBBc-.c2f7ab22.woff
 unigui/web/fonts/KFOlCnqEu92Fr1MmWUlfBBc-.77ecb942.woff
@@ -31,12 +31,12 @@
 unigui/web/fonts/flUhRq6tzZclQEJ-Vdg-IuiaDsNcIhQ8tQ.c5371cfb.woff2
 unigui/web/icons/favicon-128x128.png
 unigui/web/icons/favicon-16x16.png
 unigui/web/icons/favicon-32x32.png
 unigui/web/icons/favicon-96x96.png
 unigui/web/js/193.283445be.js
 unigui/web/js/430.591e9a73.js
-unigui/web/js/615.04cc6ad4.js
-unigui/web/js/615.04cc6ad4.js.gz
-unigui/web/js/app.fb1ab18a.js
-unigui/web/js/vendor.3076c5e7.js
-unigui/web/js/vendor.3076c5e7.js.gz
+unigui/web/js/9.100130f6.js
+unigui/web/js/9.100130f6.js.gz
+unigui/web/js/app.c7c500ce.js
+unigui/web/js/vendor.18cce91f.js
+unigui/web/js/vendor.18cce91f.js.gz
```

