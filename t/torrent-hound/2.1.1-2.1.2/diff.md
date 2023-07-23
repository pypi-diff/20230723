# Comparing `tmp/torrent-hound-2.1.1.tar.gz` & `tmp/torrent-hound-2.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "torrent-hound-2.1.1.tar", last modified: Sun Jul 23 15:58:47 2023, max compression
+gzip compressed data, was "torrent-hound-2.1.2.tar", last modified: Sun Jul 23 17:27:23 2023, max compression
```

## Comparing `torrent-hound-2.1.1.tar` & `torrent-hound-2.1.2.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 yash       (501) staff       (20)        0 2023-07-23 15:58:47.525215 torrent-hound-2.1.1/
--rw-r--r--   0 yash       (501) staff       (20)       18 2018-06-15 03:26:44.000000 torrent-hound-2.1.1/MANIFEST.in
--rw-r--r--   0 yash       (501) staff       (20)     2245 2023-07-23 15:58:47.525094 torrent-hound-2.1.1/PKG-INFO
--rw-r--r--   0 yash       (501) staff       (20)     1974 2023-04-22 01:31:31.000000 torrent-hound-2.1.1/README.rst
--rw-r--r--   0 yash       (501) staff       (20)       38 2023-07-23 15:58:47.525264 torrent-hound-2.1.1/setup.cfg
--rw-r--r--   0 yash       (501) staff       (20)      830 2023-07-23 15:57:53.000000 torrent-hound-2.1.1/setup.py
--rwxr--r--   0 yash       (501) staff       (20)    58451 2023-07-23 15:50:23.000000 torrent-hound-2.1.1/torrent-hound
-drwxr-xr-x   0 yash       (501) staff       (20)        0 2023-07-23 15:58:47.524906 torrent-hound-2.1.1/torrent_hound.egg-info/
--rw-r--r--   0 yash       (501) staff       (20)     2245 2023-07-23 15:58:47.000000 torrent-hound-2.1.1/torrent_hound.egg-info/PKG-INFO
--rw-r--r--   0 yash       (501) staff       (20)      229 2023-07-23 15:58:47.000000 torrent-hound-2.1.1/torrent_hound.egg-info/SOURCES.txt
--rw-r--r--   0 yash       (501) staff       (20)        1 2023-07-23 15:58:47.000000 torrent-hound-2.1.1/torrent_hound.egg-info/dependency_links.txt
--rw-r--r--   0 yash       (501) staff       (20)       63 2023-07-23 15:58:47.000000 torrent-hound-2.1.1/torrent_hound.egg-info/requires.txt
--rw-r--r--   0 yash       (501) staff       (20)        1 2023-07-23 15:58:47.000000 torrent-hound-2.1.1/torrent_hound.egg-info/top_level.txt
+drwxr-xr-x   0 yash       (501) staff       (20)        0 2023-07-23 17:27:23.086564 torrent-hound-2.1.2/
+-rw-r--r--   0 yash       (501) staff       (20)       18 2018-06-15 03:26:44.000000 torrent-hound-2.1.2/MANIFEST.in
+-rw-r--r--   0 yash       (501) staff       (20)     2233 2023-07-23 17:27:23.086427 torrent-hound-2.1.2/PKG-INFO
+-rw-r--r--   0 yash       (501) staff       (20)     1962 2023-07-23 17:21:10.000000 torrent-hound-2.1.2/README.rst
+-rw-r--r--   0 yash       (501) staff       (20)       38 2023-07-23 17:27:23.086619 torrent-hound-2.1.2/setup.cfg
+-rw-r--r--   0 yash       (501) staff       (20)      830 2023-07-23 17:23:32.000000 torrent-hound-2.1.2/setup.py
+-rwxr--r--   0 yash       (501) staff       (20)    58390 2023-07-23 17:26:23.000000 torrent-hound-2.1.2/torrent-hound
+drwxr-xr-x   0 yash       (501) staff       (20)        0 2023-07-23 17:27:23.086230 torrent-hound-2.1.2/torrent_hound.egg-info/
+-rw-r--r--   0 yash       (501) staff       (20)     2233 2023-07-23 17:27:23.000000 torrent-hound-2.1.2/torrent_hound.egg-info/PKG-INFO
+-rw-r--r--   0 yash       (501) staff       (20)      229 2023-07-23 17:27:23.000000 torrent-hound-2.1.2/torrent_hound.egg-info/SOURCES.txt
+-rw-r--r--   0 yash       (501) staff       (20)        1 2023-07-23 17:27:23.000000 torrent-hound-2.1.2/torrent_hound.egg-info/dependency_links.txt
+-rw-r--r--   0 yash       (501) staff       (20)       63 2023-07-23 17:27:23.000000 torrent-hound-2.1.2/torrent_hound.egg-info/requires.txt
+-rw-r--r--   0 yash       (501) staff       (20)        1 2023-07-23 17:27:23.000000 torrent-hound-2.1.2/torrent_hound.egg-info/top_level.txt
```

### Comparing `torrent-hound-2.1.1/PKG-INFO` & `torrent-hound-2.1.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: torrent-hound
-Version: 2.1.1
+Version: 2.1.2
 Summary: Search torrents from multiple websites via the CLI
 Home-page: https://github.com/baddymaster/torrent-hound
 Author: Yashovardhan Sharma
 Author-email: yash.s@tuta.io
 License: AGPL-3.0
 Requires-Python: >=3
 
@@ -18,15 +18,14 @@
 
 -  Python 3
 -  bs4
 -  clint
 -  pyperclip
 -  humanize
 -  VeryPrettyTable
--  cfscrape
 
 Installation
 ~~~~~~~~~~~~
 
 Install package and dependencies directly via pip using
 ``pip install torrent-hound``
```

### Comparing `torrent-hound-2.1.1/README.rst` & `torrent-hound-2.1.2/README.rst`

 * *Files 2% similar despite different names*

```diff
@@ -8,15 +8,14 @@
 
 -  Python 3
 -  bs4
 -  clint
 -  pyperclip
 -  humanize
 -  VeryPrettyTable
--  cfscrape
 
 Installation
 ~~~~~~~~~~~~
 
 Install package and dependencies directly via pip using
 ``pip install torrent-hound``
```

### Comparing `torrent-hound-2.1.1/setup.py` & `torrent-hound-2.1.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 def readme():
     with open('README.rst') as f:
         return f.read()
 
 setup(
     name='torrent-hound',          # This is the name of your PyPI-package.
-    version='2.1.1',                 # Update the version number for new releases
+    version='2.1.2',                 # Update the version number for new releases
     scripts=['torrent-hound'],     # The name of your scipt, and also the command you'll be using for calling it
     description='Search torrents from multiple websites via the CLI',
     long_description=readme(),
     python_requires = '>=3',
     url='https://github.com/baddymaster/torrent-hound',
     install_requires=[
         'bs4',
```

### Comparing `torrent-hound-2.1.1/torrent-hound` & `torrent-hound-2.1.2/torrent-hound`

 * *Files 0% similar despite different names*

```diff
@@ -32,15 +32,14 @@
 import webbrowser
 import json
 import humanize
 import traceback
 import random
 import time
 import argparse
-import cfscrape as cfs
 import traceback
 
 defaultQuery, query = 'jason bourne', ''
 results_sky = None
 results_tpb_condensed = None
 results_tpb_api, num_results_tpb_api = None, 0
 results_1337x = None
@@ -376,16 +375,15 @@
     url = baseURL + '/?query=' + search_string
     skytorrents_url = url
     #url = baseURL + '/search/all/' + order_by + '/1/?l=en-us&q=' + search_string
     headers = {'User-Agent': 'Mozilla/5.0 (Windows NT 6.0; WOW64; rv:24.0) Gecko/20100101 Firefox/24.0'}
     tbody = None
     #headers = {'User-Agent': 'Mozilla/5.0'}
     try:
-        scraper = cfs.create_scraper()
-        r = scraper.get(url, headers=headers)
+        r = requests.get(url, headers=headers)
         soup = BeautifulSoup(r.content, "html.parser")
         #print soup
         tbody = soup.find('tbody')
         results_sky = []
 
         trows = tbody.findAll("tr")
         #print len(trows)
```

### Comparing `torrent-hound-2.1.1/torrent_hound.egg-info/PKG-INFO` & `torrent-hound-2.1.2/torrent_hound.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: torrent-hound
-Version: 2.1.1
+Version: 2.1.2
 Summary: Search torrents from multiple websites via the CLI
 Home-page: https://github.com/baddymaster/torrent-hound
 Author: Yashovardhan Sharma
 Author-email: yash.s@tuta.io
 License: AGPL-3.0
 Requires-Python: >=3
 
@@ -18,15 +18,14 @@
 
 -  Python 3
 -  bs4
 -  clint
 -  pyperclip
 -  humanize
 -  VeryPrettyTable
--  cfscrape
 
 Installation
 ~~~~~~~~~~~~
 
 Install package and dependencies directly via pip using
 ``pip install torrent-hound``
```

