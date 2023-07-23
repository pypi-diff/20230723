# Comparing `tmp/xgorn-api-1.0.3.tar.gz` & `tmp/xgorn-api-1.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "xgorn-api-1.0.3.tar", last modified: Thu Jul  6 03:31:58 2023, max compression
+gzip compressed data, was "xgorn-api-1.0.4.tar", last modified: Sun Jul 23 06:12:59 2023, max compression
```

## Comparing `xgorn-api-1.0.3.tar` & `xgorn-api-1.0.4.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-06 03:31:58.649206 xgorn-api-1.0.3/
--rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-07-06 03:31:44.000000 xgorn-api-1.0.3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2029 2023-07-06 03:31:58.649206 xgorn-api-1.0.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      837 2023-07-06 03:31:44.000000 xgorn-api-1.0.3/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-06 03:31:58.649206 xgorn-api-1.0.3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2862 2023-07-06 03:31:44.000000 xgorn-api-1.0.3/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-06 03:31:58.645206 xgorn-api-1.0.3/xgorn_api/
--rw-r--r--   0 runner    (1001) docker     (123)     1162 2023-07-06 03:31:44.000000 xgorn-api-1.0.3/xgorn_api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2143 2023-07-06 03:31:44.000000 xgorn-api-1.0.3/xgorn_api/api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-06 03:31:58.649206 xgorn-api-1.0.3/xgorn_api/features/
--rw-r--r--   0 runner    (1001) docker     (123)     1226 2023-07-06 03:31:44.000000 xgorn-api-1.0.3/xgorn_api/features/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1437 2023-07-06 03:31:44.000000 xgorn-api-1.0.3/xgorn_api/features/bypass.py
--rw-r--r--   0 runner    (1001) docker     (123)     1327 2023-07-06 03:31:44.000000 xgorn-api-1.0.3/xgorn_api/features/music.py
--rw-r--r--   0 runner    (1001) docker     (123)     3037 2023-07-06 03:31:44.000000 xgorn-api-1.0.3/xgorn_api/features/scrape.py
--rw-r--r--   0 runner    (1001) docker     (123)     1385 2023-07-06 03:31:44.000000 xgorn-api-1.0.3/xgorn_api/features/translate.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-06 03:31:58.645206 xgorn-api-1.0.3/xgorn_api.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2029 2023-07-06 03:31:58.000000 xgorn-api-1.0.3/xgorn_api.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      378 2023-07-06 03:31:58.000000 xgorn-api-1.0.3/xgorn_api.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-06 03:31:58.000000 xgorn-api-1.0.3/xgorn_api.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-06 03:31:58.000000 xgorn-api-1.0.3/xgorn_api.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-06 03:31:58.000000 xgorn-api-1.0.3/xgorn_api.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:12:59.261268 xgorn-api-1.0.4/
+-rw-r--r--   0 runner    (1001) docker     (123)     1063 2023-07-23 06:12:32.000000 xgorn-api-1.0.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2029 2023-07-23 06:12:59.261268 xgorn-api-1.0.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      837 2023-07-23 06:12:32.000000 xgorn-api-1.0.4/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 06:12:59.261268 xgorn-api-1.0.4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2862 2023-07-23 06:12:32.000000 xgorn-api-1.0.4/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:12:59.261268 xgorn-api-1.0.4/xgorn_api/
+-rw-r--r--   0 runner    (1001) docker     (123)     1162 2023-07-23 06:12:32.000000 xgorn-api-1.0.4/xgorn_api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2143 2023-07-23 06:12:32.000000 xgorn-api-1.0.4/xgorn_api/api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:12:59.261268 xgorn-api-1.0.4/xgorn_api/features/
+-rw-r--r--   0 runner    (1001) docker     (123)     1226 2023-07-23 06:12:32.000000 xgorn-api-1.0.4/xgorn_api/features/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1437 2023-07-23 06:12:32.000000 xgorn-api-1.0.4/xgorn_api/features/bypass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1327 2023-07-23 06:12:32.000000 xgorn-api-1.0.4/xgorn_api/features/music.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3421 2023-07-23 06:12:32.000000 xgorn-api-1.0.4/xgorn_api/features/scrape.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1541 2023-07-23 06:12:32.000000 xgorn-api-1.0.4/xgorn_api/features/translate.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:12:59.261268 xgorn-api-1.0.4/xgorn_api.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2029 2023-07-23 06:12:59.000000 xgorn-api-1.0.4/xgorn_api.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      378 2023-07-23 06:12:59.000000 xgorn-api-1.0.4/xgorn_api.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 06:12:59.000000 xgorn-api-1.0.4/xgorn_api.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 06:12:59.000000 xgorn-api-1.0.4/xgorn_api.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-23 06:12:59.000000 xgorn-api-1.0.4/xgorn_api.egg-info/top_level.txt
```

### Comparing `xgorn-api-1.0.3/LICENSE` & `xgorn-api-1.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `xgorn-api-1.0.3/PKG-INFO` & `xgorn-api-1.0.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: xgorn-api
-Version: 1.0.3
+Version: 1.0.4
 Summary: API Interface for api.xgorn.pp.ua
 Home-page: https://github.com/X-Gorn/xgorn-api
 Author: xgorn
 License: MIT
 Project-URL: Web, https://api.xgorn.pp.ua
 Project-URL: Documentation, https://api.xgorn.pp.ua/docs
 Keywords: api scraper bypasser translator client library python
```

### Comparing `xgorn-api-1.0.3/README.md` & `xgorn-api-1.0.4/README.md`

 * *Files identical despite different names*

### Comparing `xgorn-api-1.0.3/setup.py` & `xgorn-api-1.0.4/setup.py`

 * *Files identical despite different names*

### Comparing `xgorn-api-1.0.3/xgorn_api/__init__.py` & `xgorn-api-1.0.4/xgorn_api/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -18,8 +18,8 @@
 #  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 #  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 #  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 #  SOFTWARE.
 
 from .api import NoidAPI
 
-__version__ = '1.0.3'
+__version__ = '1.0.4'
```

### Comparing `xgorn-api-1.0.3/xgorn_api/api.py` & `xgorn-api-1.0.4/xgorn_api/api.py`

 * *Files identical despite different names*

### Comparing `xgorn-api-1.0.3/xgorn_api/features/__init__.py` & `xgorn-api-1.0.4/xgorn_api/features/__init__.py`

 * *Files identical despite different names*

### Comparing `xgorn-api-1.0.3/xgorn_api/features/bypass.py` & `xgorn-api-1.0.4/xgorn_api/features/bypass.py`

 * *Files identical despite different names*

### Comparing `xgorn-api-1.0.3/xgorn_api/features/music.py` & `xgorn-api-1.0.4/xgorn_api/features/music.py`

 * *Files identical despite different names*

### Comparing `xgorn-api-1.0.3/xgorn_api/features/scrape.py` & `xgorn-api-1.0.4/xgorn_api/features/scrape.py`

 * *Files 22% similar despite different names*

```diff
@@ -22,50 +22,59 @@
 
 class Scrape:
     
     def __init__(self, api):
         self.api = api
     
     def tiktok(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/tiktok', url=url)
+        return self.api.make_request('post', '/scrape/tiktok', url=url)
     
     def facebook(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/facebook', url=url)
+        return self.api.make_request('post', '/scrape/facebook', url=url)
     
     def instagram(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/instagram', url=url)
+        return self.api.make_request('post', '/scrape/instagram', url=url)
     
     def instagramv2(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/instagramv2', url=url)
+        return self.api.make_request('post', '/scrape/instagramv2', url=url)
 
     def twitter(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/twitter', url=url)
+        return self.api.make_request('post', '/scrape/twitter', url=url)
     
     def twitterv2(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/twitterv2', url=url)
+        return self.api.make_request('post', '/scrape/twitterv2', url=url)
     
     def likee(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/likee', url=url)
+        return self.api.make_request('post', '/scrape/likee', url=url)
     
     def pinterest(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/pinterest', url=url)
+        return self.api.make_request('post', '/scrape/pinterest', url=url)
     
     def pinterestv2(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/pinterestv2', url=url)
+        return self.api.make_request('post', '/scrape/pinterestv2', url=url)
     
     def terabox(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/terabox', url=url)
+        return self.api.make_request('post', '/scrape/terabox', url=url)
     
     def gofile(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/gofile', url=url)
+        return self.api.make_request('post', '/scrape/gofile', url=url)
     
     def krakenfiles(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/krakenfiles', url=url)
+        return self.api.make_request('post', '/scrape/krakenfiles', url=url)
     
     def yifysubtitles(self, imdb_id: str, lang: str) -> dict:
-        return self.api.make_request('get', '/scrape/yifysubtitles', imdb_id=imdb_id, lang=lang)
+        return self.api.make_request('post', '/scrape/yifysubtitles', imdb_id=imdb_id, lang=lang)
     
     def filelions(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/filelions', url=url)
+        return self.api.make_request('post', '/scrape/filelions', url=url)
     
     def streamwish(self, url: str) -> dict:
-        return self.api.make_request('get', '/scrape/streamwish', url=url)
+        return self.api.make_request('post', '/scrape/streamwish', url=url)
+
+    def icons8(self, url: str) -> dict:
+        return self.api.make_request('post', '/scrape/icons8', url=url)
+    
+    def readlightnovel(self, title: str) -> dict:
+        return self.api.make_request('post', '/scrape/readlightnovel', title=title)
+    
+    def reddit(self, url: str) -> dict:
+        return self.api.make_request('post', '/scrape/reddit', url=url)
```

### Comparing `xgorn-api-1.0.3/xgorn_api/features/translate.py` & `xgorn-api-1.0.4/xgorn_api/features/translate.py`

 * *Files 16% similar despite different names*

```diff
@@ -22,8 +22,11 @@
 
 class Translate:
     
     def __init__(self, api):
         self.api = api
     
     def srt(self, file: str, source_lang: str, dest_lang: str) -> dict:
-        return self.api.make_request('post', '/translate/srt', file=file, source_lang=source_lang, dest_lang=dest_lang)
+        return self.api.make_request('post', '/translate/srt', file=file, source_lang=source_lang, dest_lang=dest_lang)
+    
+    def html(self, html_text: str, lang: str) -> dict:
+        return self.api.make_request('post', '/translate/html', html_text=html_text, lang=lang)
```

### Comparing `xgorn-api-1.0.3/xgorn_api.egg-info/PKG-INFO` & `xgorn-api-1.0.4/xgorn_api.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: xgorn-api
-Version: 1.0.3
+Version: 1.0.4
 Summary: API Interface for api.xgorn.pp.ua
 Home-page: https://github.com/X-Gorn/xgorn-api
 Author: xgorn
 License: MIT
 Project-URL: Web, https://api.xgorn.pp.ua
 Project-URL: Documentation, https://api.xgorn.pp.ua/docs
 Keywords: api scraper bypasser translator client library python
```

