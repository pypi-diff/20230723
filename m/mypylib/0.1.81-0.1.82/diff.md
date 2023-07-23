# Comparing `tmp/mypylib-0.1.81.tar.gz` & `tmp/mypylib-0.1.82.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mypylib-0.1.81.tar", last modified: Sat Jul 15 09:06:35 2023, max compression
+gzip compressed data, was "mypylib-0.1.82.tar", last modified: Sun Jul 23 02:54:43 2023, max compression
```

## Comparing `mypylib-0.1.81.tar` & `mypylib-0.1.82.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxr-xr-x   0 chenwei-ting   (501) staff       (20)        0 2023-07-15 09:06:35.041960 mypylib-0.1.81/
--rw-r--r--   0 chenwei-ting   (501) staff       (20)      373 2023-07-15 09:06:35.041717 mypylib-0.1.81/PKG-INFO
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     3740 2022-08-12 06:28:20.000000 mypylib-0.1.81/README.md
-drwxr-xr-x   0 chenwei-ting   (501) staff       (20)        0 2023-07-15 09:06:35.039149 mypylib-0.1.81/mypylib/
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     3184 2022-07-20 06:07:23.000000 mypylib-0.1.81/mypylib/MP_shioaji_ticks.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)    47319 2023-07-15 09:05:04.000000 mypylib-0.1.81/mypylib/__init__.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     7105 2022-07-25 06:39:45.000000 mypylib-0.1.81/mypylib/binance_copy_bot.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     6342 2022-07-15 14:28:35.000000 mypylib-0.1.81/mypylib/binance_copy_bot_test.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     3421 2022-08-01 06:21:06.000000 mypylib-0.1.81/mypylib/chdbif.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     5368 2023-07-15 09:04:03.000000 mypylib-0.1.81/mypylib/crawler.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     1083 2022-09-13 02:48:34.000000 mypylib-0.1.81/mypylib/crypto.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     5093 2022-08-12 06:28:16.000000 mypylib-0.1.81/mypylib/finmind.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)    87196 2022-06-02 06:59:21.000000 mypylib-0.1.81/mypylib/libexcel.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)    24435 2023-06-01 04:56:52.000000 mypylib-0.1.81/mypylib/mvp.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     1255 2022-06-26 10:52:11.000000 mypylib-0.1.81/mypylib/mytest.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     3588 2022-06-12 10:26:49.000000 mypylib-0.1.81/mypylib/option_test.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)      778 2022-06-02 06:59:21.000000 mypylib-0.1.81/mypylib/shioaji_history_ticks.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     2490 2023-04-11 13:54:33.000000 mypylib-0.1.81/mypylib/shioaji_kline.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     1312 2022-06-02 06:59:21.000000 mypylib-0.1.81/mypylib/shioaji_ticks.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     7649 2023-04-18 13:50:52.000000 mypylib-0.1.81/mypylib/sjtools.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     1464 2022-09-05 05:47:59.000000 mypylib-0.1.81/mypylib/tLineNotify.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     7735 2023-06-01 04:56:52.000000 mypylib-0.1.81/mypylib/ti.py
-drwxr-xr-x   0 chenwei-ting   (501) staff       (20)        0 2023-07-15 09:06:35.041060 mypylib-0.1.81/mypylib/tmpDevelopment/
--rw-r--r--   0 chenwei-ting   (501) staff       (20)        0 2022-07-16 06:27:26.000000 mypylib-0.1.81/mypylib/tmpDevelopment/__init__.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     1074 2022-07-16 07:09:42.000000 mypylib-0.1.81/mypylib/tmpDevelopment/warrant_test.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     2543 2023-04-27 13:08:02.000000 mypylib-0.1.81/mypylib/tplaysound.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     8466 2023-06-19 13:26:50.000000 mypylib-0.1.81/mypylib/tredis.py
--rw-r--r--   0 chenwei-ting   (501) staff       (20)     8217 2023-07-03 23:14:11.000000 mypylib-0.1.81/mypylib/warrant.py
-drwxr-xr-x   0 chenwei-ting   (501) staff       (20)        0 2023-07-15 09:06:35.040573 mypylib-0.1.81/mypylib.egg-info/
--rw-r--r--   0 chenwei-ting   (501) staff       (20)      373 2023-07-15 09:06:34.000000 mypylib-0.1.81/mypylib.egg-info/PKG-INFO
--rw-r--r--   0 chenwei-ting   (501) staff       (20)      673 2023-07-15 09:06:34.000000 mypylib-0.1.81/mypylib.egg-info/SOURCES.txt
--rw-r--r--   0 chenwei-ting   (501) staff       (20)        1 2023-07-15 09:06:34.000000 mypylib-0.1.81/mypylib.egg-info/dependency_links.txt
--rw-r--r--   0 chenwei-ting   (501) staff       (20)        8 2023-07-15 09:06:34.000000 mypylib-0.1.81/mypylib.egg-info/top_level.txt
--rw-r--r--   0 chenwei-ting   (501) staff       (20)       38 2023-07-15 09:06:35.042044 mypylib-0.1.81/setup.cfg
--rw-r--r--   0 chenwei-ting   (501) staff       (20)      846 2022-06-29 14:27:00.000000 mypylib-0.1.81/setup.py
+drwxr-xr-x   0 chenwei-ting   (501) staff       (20)        0 2023-07-23 02:54:43.237051 mypylib-0.1.82/
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)      373 2023-07-23 02:54:43.236732 mypylib-0.1.82/PKG-INFO
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     3740 2022-08-12 06:28:20.000000 mypylib-0.1.82/README.md
+drwxr-xr-x   0 chenwei-ting   (501) staff       (20)        0 2023-07-23 02:54:43.233615 mypylib-0.1.82/mypylib/
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     3184 2022-07-20 06:07:23.000000 mypylib-0.1.82/mypylib/MP_shioaji_ticks.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)    47384 2023-07-23 02:53:53.000000 mypylib-0.1.82/mypylib/__init__.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     7105 2022-07-25 06:39:45.000000 mypylib-0.1.82/mypylib/binance_copy_bot.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     6342 2022-07-15 14:28:35.000000 mypylib-0.1.82/mypylib/binance_copy_bot_test.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     3421 2022-08-01 06:21:06.000000 mypylib-0.1.82/mypylib/chdbif.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     5984 2023-07-22 12:35:23.000000 mypylib-0.1.82/mypylib/crawler.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     1083 2022-09-13 02:48:34.000000 mypylib-0.1.82/mypylib/crypto.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     5093 2022-08-12 06:28:16.000000 mypylib-0.1.82/mypylib/finmind.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)    87196 2022-06-02 06:59:21.000000 mypylib-0.1.82/mypylib/libexcel.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)    24435 2023-06-01 04:56:52.000000 mypylib-0.1.82/mypylib/mvp.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     1255 2022-06-26 10:52:11.000000 mypylib-0.1.82/mypylib/mytest.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     3588 2022-06-12 10:26:49.000000 mypylib-0.1.82/mypylib/option_test.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)      778 2022-06-02 06:59:21.000000 mypylib-0.1.82/mypylib/shioaji_history_ticks.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     2490 2023-04-11 13:54:33.000000 mypylib-0.1.82/mypylib/shioaji_kline.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     1312 2022-06-02 06:59:21.000000 mypylib-0.1.82/mypylib/shioaji_ticks.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     7649 2023-04-18 13:50:52.000000 mypylib-0.1.82/mypylib/sjtools.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     1464 2022-09-05 05:47:59.000000 mypylib-0.1.82/mypylib/tLineNotify.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     7735 2023-06-01 04:56:52.000000 mypylib-0.1.82/mypylib/ti.py
+drwxr-xr-x   0 chenwei-ting   (501) staff       (20)        0 2023-07-23 02:54:43.236009 mypylib-0.1.82/mypylib/tmpDevelopment/
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)        0 2022-07-16 06:27:26.000000 mypylib-0.1.82/mypylib/tmpDevelopment/__init__.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     1074 2022-07-16 07:09:42.000000 mypylib-0.1.82/mypylib/tmpDevelopment/warrant_test.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     2543 2023-04-27 13:08:02.000000 mypylib-0.1.82/mypylib/tplaysound.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     8466 2023-06-19 13:26:50.000000 mypylib-0.1.82/mypylib/tredis.py
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)     8217 2023-07-03 23:14:11.000000 mypylib-0.1.82/mypylib/warrant.py
+drwxr-xr-x   0 chenwei-ting   (501) staff       (20)        0 2023-07-23 02:54:43.235487 mypylib-0.1.82/mypylib.egg-info/
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)      373 2023-07-23 02:54:42.000000 mypylib-0.1.82/mypylib.egg-info/PKG-INFO
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)      673 2023-07-23 02:54:43.000000 mypylib-0.1.82/mypylib.egg-info/SOURCES.txt
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)        1 2023-07-23 02:54:42.000000 mypylib-0.1.82/mypylib.egg-info/dependency_links.txt
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)        8 2023-07-23 02:54:43.000000 mypylib-0.1.82/mypylib.egg-info/top_level.txt
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)       38 2023-07-23 02:54:43.237164 mypylib-0.1.82/setup.cfg
+-rw-r--r--   0 chenwei-ting   (501) staff       (20)      846 2022-06-29 14:27:00.000000 mypylib-0.1.82/setup.py
```

### Comparing `mypylib-0.1.81/README.md` & `mypylib-0.1.82/README.md`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/MP_shioaji_ticks.py` & `mypylib-0.1.82/mypylib/MP_shioaji_ticks.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/__init__.py` & `mypylib-0.1.82/mypylib/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -69,19 +69,20 @@
     '2023/05/22: 0.1.74 mvp() 不繼承 base class。因為shioaji升級的關係。先可以跑再說',
     '2023/06/01: 0.1.75 Apply Carey change',
     '2023/06/15: 0.1.76 Add crawler',
     '2023/06/19: 0.1.77 Not using stupid Redis connection pool',
     '2023/07/05: 0.1.78 cynes api v1 support',
     '2023/07/06: 0.1.79 news crawler little modification',
     '2023/07/12: 0.1.80 修改crawler',
-    '2023/07/15: 0.1.81 修改 crawler 的 user agent，以免被認為是爬蟲'
+    '2023/07/15: 0.1.81 修改 crawler 的 user agent，以免被認為是爬蟲',
+    '2023/07/23: 0.1.82 修改 crawler 的 方法. 支援 page'
 
 }
 
-__version__ = '0.1.81'
+__version__ = '0.1.82'
 
 request_headers = {
     'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/39.0.2171.95 Safari/537.36'
 }
 
 path_cronlog = 'cronlog'
```

### Comparing `mypylib-0.1.81/mypylib/binance_copy_bot.py` & `mypylib-0.1.82/mypylib/binance_copy_bot.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/binance_copy_bot_test.py` & `mypylib-0.1.82/mypylib/binance_copy_bot_test.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/chdbif.py` & `mypylib-0.1.82/mypylib/chdbif.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/crawler.py` & `mypylib-0.1.82/mypylib/crawler.py`

 * *Files 12% similar despite different names*

```diff
@@ -64,66 +64,86 @@
     'fbCommentPluginCount': 0,
     'market': [{'code': '2352', 'name': '佳世達', 'symbol': 'TWS:2352:STOCK'}],
     'categoryName': '台股新聞'}
 """
 
 class crawler_cnyes:
 
-    def __init__(self, version=1):
-        self.datetime_start = datetime.datetime.today()
-        self.datetime_end = datetime.datetime.today()
+    list_source = [
+        {
+            'base_url': 'https://api.cnyes.com',
+            'next_page_url': '/media/api/v1/newslist/category/tw_stock?page=1'
+        },
+        {
+            'base_url': 'https://api.cnyes.com',
+            'next_page_url': '/media/api/v1/newslist/category/tw_stock_news?page=1'
+        },
+        {
+            'base_url': 'https://news.cnyes.com',
+            'next_page_url': '/api/v3/news/category/tw_stock?page=1'
+        }
+
+    ]
 
+    def __init__(self, version=1):
         self.list_news = set()
         self.version = version
 
+
     @logger.catch
     def fetch(self,
               datetime_start: datetime.datetime = datetime.datetime.today().replace(hour=0, minute=0, second=0),
               datetime_end: datetime.datetime = datetime.datetime.today() + datetime.timedelta(days=1)):
 
-        self.datetime_start = datetime_start
-        self.datetime_end = datetime_end
+        startAt = int(datetime_start.timestamp())
+        endday = int(datetime_end.timestamp())
 
-        if self.version == 1:
-            url = f'https://api.cnyes.com/media/api/v1/newslist/category/tw_stock?startAt={int(self.datetime_start.timestamp())}&endAt={int(self.datetime_end.timestamp())}&limit=100'
-        else:
-            url = f'https://news.cnyes.com/api/v3/news/category/tw_stock?startAt={int(self.datetime_start.timestamp())}' \
-                  f'&endAt={int(self.datetime_end.timestamp())}&limit=100'
-        logger.info(url)
-        res = requests.get(url, headers=headers)
-        ret = json.loads(res.text)
-
-        list_news = []
-        for x in ret['items']['data']:
-            # print(x)
-            # for key in x:
-            #     print(key)
-            logger.info(x)
-            title = x['title']
-            str_dt = datetime.datetime.fromtimestamp(x['publishAt'])
-            categoryName = x.get('categoryName', '')
-            if categoryName != '台股新聞':
-                continue
-            stock = ' '.join(x.get('stock', ''))
+        list_news = set()
 
-            logger.info(f'{str_dt} {title}')
-            list_news.append(f'{str_dt} {title} [{categoryName}] {stock}')
+        for source in crawler_cnyes.list_source:
+            base_url = source['base_url']
+            next_page_url = source['next_page_url']
+
+            while True:
+                url = f'{base_url}{next_page_url}&startAt={startAt}&endAt={endday}'
+                # print(url)
+                res = requests.get(url, headers=headers)
+                dict_res = json.loads(res.text)
+                last_page = dict_res['items']['last_page']
+                next_page_url = dict_res['items']['next_page_url']
+                # print(f'總共 {last_page} 頁, Total: {dict_res["items"]["total"]}, from {dict_res["items"]["from"]} - {dict_res["items"]["to"]}')
+                for x in dict_res['items']['data']:
+                    # print(x)
+                    # for key in x:
+                    #     print(key)
+                    # logger.info(x)
+                    title = x['title']
+                    # print(title)
+                    str_dt = datetime.datetime.fromtimestamp(x['publishAt'])
+                    categoryName = x.get('categoryName', '')
+                    if categoryName != '台股新聞':
+                        continue
+                    stock = ' '.join(x.get('stock', ''))
+
+                    # logger.info(f'{str_dt} {title}')
+                    list_news.add(f'{str_dt} {title} [{categoryName}] {stock}')
+
+                if next_page_url is None:
+                    break
 
         return list_news
 
+
     def fetch_new(self):
 
-        self.version = 1
-        ret_v1: list = self.fetch()
-        self.version = 3
-        ret_v3: list = self.fetch()
+        ret: list = self.fetch()
 
         list_news_new = []
 
-        for x in ret_v1 + ret_v3:
+        for x in ret:
             if x not in self.list_news:
                 self.list_news.add(x)
                 list_news_new.append(x)
 
         return list_news_new
```

### Comparing `mypylib-0.1.81/mypylib/crypto.py` & `mypylib-0.1.82/mypylib/crypto.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/finmind.py` & `mypylib-0.1.82/mypylib/finmind.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/libexcel.py` & `mypylib-0.1.82/mypylib/libexcel.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/mvp.py` & `mypylib-0.1.82/mypylib/mvp.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/mytest.py` & `mypylib-0.1.82/mypylib/mytest.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/option_test.py` & `mypylib-0.1.82/mypylib/option_test.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/shioaji_history_ticks.py` & `mypylib-0.1.82/mypylib/shioaji_history_ticks.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/shioaji_kline.py` & `mypylib-0.1.82/mypylib/shioaji_kline.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/shioaji_ticks.py` & `mypylib-0.1.82/mypylib/shioaji_ticks.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/sjtools.py` & `mypylib-0.1.82/mypylib/sjtools.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/tLineNotify.py` & `mypylib-0.1.82/mypylib/tLineNotify.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/ti.py` & `mypylib-0.1.82/mypylib/ti.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/tmpDevelopment/warrant_test.py` & `mypylib-0.1.82/mypylib/tmpDevelopment/warrant_test.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/tplaysound.py` & `mypylib-0.1.82/mypylib/tplaysound.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/tredis.py` & `mypylib-0.1.82/mypylib/tredis.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib/warrant.py` & `mypylib-0.1.82/mypylib/warrant.py`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/mypylib.egg-info/SOURCES.txt` & `mypylib-0.1.82/mypylib.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `mypylib-0.1.81/setup.py` & `mypylib-0.1.82/setup.py`

 * *Files identical despite different names*

