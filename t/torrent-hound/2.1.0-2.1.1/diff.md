# Comparing `tmp/torrent-hound-2.1.0.tar.gz` & `tmp/torrent-hound-2.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "torrent-hound-2.1.0.tar", last modified: Sat Apr 22 14:40:40 2023, max compression
+gzip compressed data, was "torrent-hound-2.1.1.tar", last modified: Sun Jul 23 15:58:47 2023, max compression
```

## Comparing `torrent-hound-2.1.0.tar` & `torrent-hound-2.1.1.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 yashovardhan   (501) staff       (20)        0 2023-04-22 14:40:40.993059 torrent-hound-2.1.0/
--rw-r--r--   0 yashovardhan   (501) staff       (20)       18 2018-06-15 03:26:44.000000 torrent-hound-2.1.0/MANIFEST.in
--rw-r--r--   0 yashovardhan   (501) staff       (20)     2245 2023-04-22 14:40:40.992577 torrent-hound-2.1.0/PKG-INFO
--rw-r--r--   0 yashovardhan   (501) staff       (20)     1974 2023-04-22 01:31:31.000000 torrent-hound-2.1.0/README.rst
--rw-r--r--   0 yashovardhan   (501) staff       (20)       38 2023-04-22 14:40:40.993412 torrent-hound-2.1.0/setup.cfg
--rw-r--r--   0 yashovardhan   (501) staff       (20)      830 2023-04-22 14:39:22.000000 torrent-hound-2.1.0/setup.py
--rwxr--r--   0 yashovardhan   (501) staff       (20)    58285 2023-04-22 14:40:11.000000 torrent-hound-2.1.0/torrent-hound
-drwxr-xr-x   0 yashovardhan   (501) staff       (20)        0 2023-04-22 14:40:40.991681 torrent-hound-2.1.0/torrent_hound.egg-info/
--rw-r--r--   0 yashovardhan   (501) staff       (20)     2245 2023-04-22 14:40:40.000000 torrent-hound-2.1.0/torrent_hound.egg-info/PKG-INFO
--rw-r--r--   0 yashovardhan   (501) staff       (20)      229 2023-04-22 14:40:40.000000 torrent-hound-2.1.0/torrent_hound.egg-info/SOURCES.txt
--rw-r--r--   0 yashovardhan   (501) staff       (20)        1 2023-04-22 14:40:40.000000 torrent-hound-2.1.0/torrent_hound.egg-info/dependency_links.txt
--rw-r--r--   0 yashovardhan   (501) staff       (20)       63 2023-04-22 14:40:40.000000 torrent-hound-2.1.0/torrent_hound.egg-info/requires.txt
--rw-r--r--   0 yashovardhan   (501) staff       (20)        1 2023-04-22 14:40:40.000000 torrent-hound-2.1.0/torrent_hound.egg-info/top_level.txt
+drwxr-xr-x   0 yash       (501) staff       (20)        0 2023-07-23 15:58:47.525215 torrent-hound-2.1.1/
+-rw-r--r--   0 yash       (501) staff       (20)       18 2018-06-15 03:26:44.000000 torrent-hound-2.1.1/MANIFEST.in
+-rw-r--r--   0 yash       (501) staff       (20)     2245 2023-07-23 15:58:47.525094 torrent-hound-2.1.1/PKG-INFO
+-rw-r--r--   0 yash       (501) staff       (20)     1974 2023-04-22 01:31:31.000000 torrent-hound-2.1.1/README.rst
+-rw-r--r--   0 yash       (501) staff       (20)       38 2023-07-23 15:58:47.525264 torrent-hound-2.1.1/setup.cfg
+-rw-r--r--   0 yash       (501) staff       (20)      830 2023-07-23 15:57:53.000000 torrent-hound-2.1.1/setup.py
+-rwxr--r--   0 yash       (501) staff       (20)    58451 2023-07-23 15:50:23.000000 torrent-hound-2.1.1/torrent-hound
+drwxr-xr-x   0 yash       (501) staff       (20)        0 2023-07-23 15:58:47.524906 torrent-hound-2.1.1/torrent_hound.egg-info/
+-rw-r--r--   0 yash       (501) staff       (20)     2245 2023-07-23 15:58:47.000000 torrent-hound-2.1.1/torrent_hound.egg-info/PKG-INFO
+-rw-r--r--   0 yash       (501) staff       (20)      229 2023-07-23 15:58:47.000000 torrent-hound-2.1.1/torrent_hound.egg-info/SOURCES.txt
+-rw-r--r--   0 yash       (501) staff       (20)        1 2023-07-23 15:58:47.000000 torrent-hound-2.1.1/torrent_hound.egg-info/dependency_links.txt
+-rw-r--r--   0 yash       (501) staff       (20)       63 2023-07-23 15:58:47.000000 torrent-hound-2.1.1/torrent_hound.egg-info/requires.txt
+-rw-r--r--   0 yash       (501) staff       (20)        1 2023-07-23 15:58:47.000000 torrent-hound-2.1.1/torrent_hound.egg-info/top_level.txt
```

### Comparing `torrent-hound-2.1.0/PKG-INFO` & `torrent-hound-2.1.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: torrent-hound
-Version: 2.1.0
+Version: 2.1.1
 Summary: Search torrents from multiple websites via the CLI
 Home-page: https://github.com/baddymaster/torrent-hound
 Author: Yashovardhan Sharma
 Author-email: yash.s@tuta.io
 License: AGPL-3.0
 Requires-Python: >=3
```

### Comparing `torrent-hound-2.1.0/README.rst` & `torrent-hound-2.1.1/README.rst`

 * *Files identical despite different names*

### Comparing `torrent-hound-2.1.0/setup.py` & `torrent-hound-2.1.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 def readme():
     with open('README.rst') as f:
         return f.read()
 
 setup(
     name='torrent-hound',          # This is the name of your PyPI-package.
-    version='2.1.0',                 # Update the version number for new releases
+    version='2.1.1',                 # Update the version number for new releases
     scripts=['torrent-hound'],     # The name of your scipt, and also the command you'll be using for calling it
     description='Search torrents from multiple websites via the CLI',
     long_description=readme(),
     python_requires = '>=3',
     url='https://github.com/baddymaster/torrent-hound',
     install_requires=[
         'bs4',
```

### Comparing `torrent-hound-2.1.0/torrent-hound` & `torrent-hound-2.1.1/torrent-hound`

 * *Files 0% similar despite different names*

```diff
@@ -293,40 +293,43 @@
     url_1337x = url
     
     headers = {'User-Agent': 'Mozilla/5.0 (Windows NT 6.0; WOW64; rv:24.0) Gecko/20100101 Firefox/24.0'}
     response = requests.get(url, headers=headers)
     soup = BeautifulSoup(response.text, 'html.parser')
     results_1337x = []
     
-    table = soup.find('table', {'class': 'table-list'})
-    rows = table.tbody.find_all('tr')
-    for row in rows[:limit]:
-        row_data = {}
-        name_col = row.find('td', {'class': 'coll-1 name'})
-        row_data['name'] = name_col.a.next_sibling.text
-        row_data['link'] = baseURL + name_col.a.next_sibling['href']
-        row_data['seeders'] = int(row.find('td', {'class': 'coll-2 seeds'}).text.strip())
-        row_data['leechers'] = int(row.find('td', {'class': 'coll-3 leeches'}).text.strip())
-        try:
-            row_data['ratio'] = format( (float(row_data['seeders'])/float(row_data['leechers'])), '.1f' )
-        except ZeroDivisionError:
-            row_data['ratio'] = 'inf'
-        row_data['time'] = row.find('td', {'class': 'coll-date'}).text.strip()
-        size_col = row.find('td', {'class': 'coll-4'})
-        if size_col:
-            row_data['size'] = size_col.contents[0].strip()
-        else:
-            row_data['size'] = ''
-        # uploader_col = row.find('td', {'class': 'coll-5'})
-        # if uploader_col:
-        #     row_data['uploader'] = uploader_col.contents[0].text.strip()
-        # else:
-        #     row_data['uploader'] = ''
-        row_data['magnet'] = extract_magnet_link_1337x(row_data['link'])
-        results_1337x.append(row_data)
+    try:
+        table = soup.find('table', {'class': 'table-list'})
+        rows = table.tbody.find_all('tr')
+        for row in rows[:limit]:
+            row_data = {}
+            name_col = row.find('td', {'class': 'coll-1 name'})
+            row_data['name'] = name_col.a.next_sibling.text
+            row_data['link'] = baseURL + name_col.a.next_sibling['href']
+            row_data['seeders'] = int(row.find('td', {'class': 'coll-2 seeds'}).text.strip())
+            row_data['leechers'] = int(row.find('td', {'class': 'coll-3 leeches'}).text.strip())
+            try:
+                row_data['ratio'] = format( (float(row_data['seeders'])/float(row_data['leechers'])), '.1f' )
+            except ZeroDivisionError:
+                row_data['ratio'] = 'inf'
+            row_data['time'] = row.find('td', {'class': 'coll-date'}).text.strip()
+            size_col = row.find('td', {'class': 'coll-4'})
+            if size_col:
+                row_data['size'] = size_col.contents[0].strip()
+            else:
+                row_data['size'] = ''
+            # uploader_col = row.find('td', {'class': 'coll-5'})
+            # if uploader_col:
+            #     row_data['uploader'] = uploader_col.contents[0].text.strip()
+            # else:
+            #     row_data['uploader'] = ''
+            row_data['magnet'] = extract_magnet_link_1337x(row_data['link'])
+            results_1337x.append(row_data)
+    except AttributeError as e:
+        print(colored.magenta("[1337x] Error : No results found"))
     return results_1337x
 
 def pretty_print_top_results_1337x(limit=10):
     global results_1337x, num_results_tpb_api, num_results
     table_1337x = VeryPrettyTable(left_padding_width=0, right_padding_width=0, padding_width=0)
     no_str = str(colored.red('No'))
     name_str = str(colored.red('Torrent Name'))
@@ -1117,23 +1120,20 @@
         results_rarbg = None
         results_tpb_api = None
         results_sky = None
         results_1337x = None
         results = None
         results_tpb_condensed = None
 
-    print(colored.magenta("Searching RARBG..."), end='')
-    if results_rarbg == None or results_rarbg == []:
-        results_rarbg = searchRarbg(query, quiet_mode=quiet_mode)
-    print(colored.green("Done."))
-    #     print 'R searching...'
-    # else:
-    #     print 'R not searching...'
-    # print 'Results R : '
-    # print results_rarbg
+    ## Search RARBG 
+    # print(colored.magenta("Searching RARBG..."), end='')
+    # if results_rarbg == None or results_rarbg == []:
+    #     results_rarbg = searchRarbg(query, quiet_mode=quiet_mode)
+    # print(colored.green("Done."))
+    results_rarbg = []
 
     # if results_tpb_api == None or results_tpb_api == []:
     #     if tpb_retries < max_tpb_retries:
     #         results_tpb_api = searchPirateBayWithAPI(query, quiet_mode=quiet_mode)
     #         results = results_tpb_api
     #         tpb_retries += 1
     #     else:
@@ -1178,15 +1178,18 @@
 def printCombinedTopResults():
     global num_results, num_results_rarbg
     num_results_rarbg = print_top_results_rarbg(10)
     num_results = print_top_results(10)
 
 def prettyPrintCombinedTopResults():
     global num_results, num_results_rarbg, num_results_sky, num_results_tpb_api, num_results_1337x
-    num_results_rarbg = pretty_print_top_results_rarbg(10)
+    
+    #num_results_rarbg = pretty_print_top_results_rarbg(10)
+    num_results_rarbg = 0
+    
     num_results = pretty_print_top_results_piratebay(10)
     #num_results_tpb_api = pretty_print_top_results_piratebay_api(10)
     #num_results = num_results_tpb_api
 
     #num_results_sky = pretty_print_top_results_skytorrents(10)
     num_results_1337x = pretty_print_top_results_1337x(10)
```

### Comparing `torrent-hound-2.1.0/torrent_hound.egg-info/PKG-INFO` & `torrent-hound-2.1.1/torrent_hound.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: torrent-hound
-Version: 2.1.0
+Version: 2.1.1
 Summary: Search torrents from multiple websites via the CLI
 Home-page: https://github.com/baddymaster/torrent-hound
 Author: Yashovardhan Sharma
 Author-email: yash.s@tuta.io
 License: AGPL-3.0
 Requires-Python: >=3
```

