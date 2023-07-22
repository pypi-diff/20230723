# Comparing `tmp/jplaw-0.1.8.tar.gz` & `tmp/jplaw-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "jplaw-0.1.8.tar", last modified: Tue Jul 11 12:54:15 2023, max compression
+gzip compressed data, was "jplaw-0.1.9.tar", last modified: Sat Jul 22 23:11:38 2023, max compression
```

## Comparing `jplaw-0.1.8.tar` & `jplaw-0.1.9.tar`

### file list

```diff
@@ -1,34 +1,34 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-11 12:54:15.261129 jplaw-0.1.8/
--rw-r--r--   0 runner    (1001) docker     (123)     1128 2023-07-11 12:54:04.000000 jplaw-0.1.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     4046 2023-07-11 12:54:15.257128 jplaw-0.1.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3471 2023-07-11 12:54:04.000000 jplaw-0.1.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-11 12:54:15.257128 jplaw-0.1.8/jplaw/
--rw-r--r--   0 runner    (1001) docker     (123)      306 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10966 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/api_paths.py
--rw-r--r--   0 runner    (1001) docker     (123)    11964 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/comment.py
--rw-r--r--   0 runner    (1001) docker     (123)    11595 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/community.py
--rw-r--r--   0 runner    (1001) docker     (123)     2947 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/emoji.py
--rw-r--r--   0 runner    (1001) docker     (123)     3400 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/lemmy.py
--rw-r--r--   0 runner    (1001) docker     (123)    12905 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/post.py
--rw-r--r--   0 runner    (1001) docker     (123)     5981 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/private_message.py
--rw-r--r--   0 runner    (1001) docker     (123)     6217 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/requestor.py
--rw-r--r--   0 runner    (1001) docker     (123)    27141 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/site.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-11 12:54:15.257128 jplaw-0.1.8/jplaw/types/
--rw-r--r--   0 runner    (1001) docker     (123)      461 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/types/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/types/comment_sort_type.py
--rw-r--r--   0 runner    (1001) docker     (123)      115 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/types/http_type.py
--rw-r--r--   0 runner    (1001) docker     (123)      112 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/types/listing_type.py
--rw-r--r--   0 runner    (1001) docker     (123)      899 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/types/modlog_action_type.py
--rw-r--r--   0 runner    (1001) docker     (123)       99 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/types/post_feature_type.py
--rw-r--r--   0 runner    (1001) docker     (123)      138 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/types/registration_mode.py
--rw-r--r--   0 runner    (1001) docker     (123)      310 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/types/search_type.py
--rw-r--r--   0 runner    (1001) docker     (123)      576 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/types/sort_type.py
--rw-r--r--   0 runner    (1001) docker     (123)      173 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/types/subscribed_type.py
--rw-r--r--   0 runner    (1001) docker     (123)    18635 2023-07-11 12:54:04.000000 jplaw-0.1.8/jplaw/user.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-11 12:54:15.257128 jplaw-0.1.8/jplaw.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4046 2023-07-11 12:54:15.000000 jplaw-0.1.8/jplaw.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      630 2023-07-11 12:54:15.000000 jplaw-0.1.8/jplaw.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-11 12:54:15.000000 jplaw-0.1.8/jplaw.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-11 12:54:15.000000 jplaw-0.1.8/jplaw.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      737 2023-07-11 12:54:04.000000 jplaw-0.1.8/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-11 12:54:15.261129 jplaw-0.1.8/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:11:38.269526 jplaw-0.1.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     1128 2023-07-22 23:11:26.000000 jplaw-0.1.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     4237 2023-07-22 23:11:38.269526 jplaw-0.1.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3662 2023-07-22 23:11:26.000000 jplaw-0.1.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:11:38.265526 jplaw-0.1.9/jplaw/
+-rw-r--r--   0 runner    (1001) docker     (123)      306 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10966 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/api_paths.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11964 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/comment.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11595 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/community.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2947 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/emoji.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3400 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/lemmy.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13146 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/post.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5981 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/private_message.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6217 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/requestor.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27141 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/site.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:11:38.269526 jplaw-0.1.9/jplaw/types/
+-rw-r--r--   0 runner    (1001) docker     (123)      461 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/types/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/types/comment_sort_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)      115 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/types/http_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)      112 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/types/listing_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)      899 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/types/modlog_action_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)       99 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/types/post_feature_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)      138 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/types/registration_mode.py
+-rw-r--r--   0 runner    (1001) docker     (123)      310 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/types/search_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)      576 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/types/sort_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)      173 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/types/subscribed_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18881 2023-07-22 23:11:26.000000 jplaw-0.1.9/jplaw/user.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:11:38.269526 jplaw-0.1.9/jplaw.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4237 2023-07-22 23:11:38.000000 jplaw-0.1.9/jplaw.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      630 2023-07-22 23:11:38.000000 jplaw-0.1.9/jplaw.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 23:11:38.000000 jplaw-0.1.9/jplaw.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-22 23:11:38.000000 jplaw-0.1.9/jplaw.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      737 2023-07-22 23:11:26.000000 jplaw-0.1.9/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 23:11:38.269526 jplaw-0.1.9/setup.cfg
```

### Comparing `jplaw-0.1.8/LICENSE` & `jplaw-0.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/PKG-INFO` & `jplaw-0.1.9/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jplaw
-Version: 0.1.8
+Version: 0.1.9
 Summary: A python wrapper for the lemmy HTTP API. Forked from plaw by Benjamin Jablonski (benja810)
 Author-email: Amar Persaud <tehspartaa@gmail.com>
 Project-URL: Homepage, https://github.com/amarpersaud/python-jplaw
 Project-URL: Bug Tracker, https://github.com/amarpersaud/python-jplaw/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -57,14 +57,22 @@
 See [the documentation](https://amarpersaud.github.io/python-jplaw/) for more information on how to use jplaw.
 
 # Roadmap 
 - Work on return types and usability.
 - Work on testing functions and finding / squashing bugs
 
 # Changelog
+### v0.1.9
+- Add blur_nsfw and auto_expand parameters to saveUserSettings
+- Add moderator_view parameter to Post.list()
+
+### v0.1.8
+- Fixes Community.edit()
+- Adds Lemmy.federateCommunity()
+
 
 ### v0.1.7
 - Fix bug with "fixed" boolean values
 
 ### v0.1.6
 - Fixes boolean and Enum parameters
 - Adds show_nsfw to communities
```

### Comparing `jplaw-0.1.8/README.md` & `jplaw-0.1.9/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -43,14 +43,22 @@
 See [the documentation](https://amarpersaud.github.io/python-jplaw/) for more information on how to use jplaw.
 
 # Roadmap 
 - Work on return types and usability.
 - Work on testing functions and finding / squashing bugs
 
 # Changelog
+### v0.1.9
+- Add blur_nsfw and auto_expand parameters to saveUserSettings
+- Add moderator_view parameter to Post.list()
+
+### v0.1.8
+- Fixes Community.edit()
+- Adds Lemmy.federateCommunity()
+
 
 ### v0.1.7
 - Fix bug with "fixed" boolean values
 
 ### v0.1.6
 - Fixes boolean and Enum parameters
 - Adds show_nsfw to communities
```

### Comparing `jplaw-0.1.8/jplaw/api_paths.py` & `jplaw-0.1.9/jplaw/api_paths.py`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/jplaw/comment.py` & `jplaw-0.1.9/jplaw/comment.py`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/jplaw/community.py` & `jplaw-0.1.9/jplaw/community.py`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/jplaw/emoji.py` & `jplaw-0.1.9/jplaw/emoji.py`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/jplaw/lemmy.py` & `jplaw-0.1.9/jplaw/lemmy.py`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/jplaw/post.py` & `jplaw-0.1.9/jplaw/post.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,40 +7,53 @@
 from jplaw.types.listing_type import ListingType
 from jplaw.types.sort_type import SortType
 
 class Post():
     def __init__(self, _req: Requestor):
         self._req = _req
         
-    def list(self, type:ListingType=None, sort:SortType=None, page:int=None, limit:int=None, community_id:int=None, community_name:str=None, saved_only:bool=None, instance:str=None, auth:bool=True):
+    def list(
+        self, 
+        type:ListingType=None, 
+        sort:SortType=None, 
+        page:int=None, 
+        limit:int=None, 
+        community_id:int=None, 
+        community_name:str=None, 
+        saved_only:bool=None, 
+        moderator_view: bool=None,
+        instance:str=None, 
+        auth:bool=True):
         """
         Get a list of posts in a community
         
         Args:
             type (ListingType): Type of post. Optional
             sort (SortType): Sorting Mode. Optional
             page (int): Page number. Optional
             limit (int): Limit for number of posts. Optional
             community_id (int): ID of the community the post is in. Optional
             community_name (str): Name of the community the post is in. Optional
             saved_only (bool): Find posts only from saved posts. Optional
+            moderator_view (bool): Moderator view. Optional
             instance (str): URL of local instance. Optional. Default None uses logged in instance
             auth (str): If true, authenticates using internal token from login. Optional. Default True
         Returns:
             List of posts
         """
         form = {}
         optional = {
             "sort": sort,
             "type": type,
             "community_id": community_id,
             "page": page,
             "limit": limit,
             "community_name": community_name,
-            "saved_only": saved_only
+            "saved_only": saved_only,
+            "moderator_view": moderator_view,
             }
         res = self._req.lemmyRequest("getPosts", instance=instance, form=form, optional=optional, auth=auth)
         return res["posts"]
         
     def get(self, post_id:int=None, comment_id:int=None, instance:str=None, auth:bool=True):
         """
         Get a post by ID
@@ -55,14 +68,15 @@
         """
         form = {}
         optional = {
             "id": post_id,
             "comment_id": comment_id,
             }
         res = self._req.lemmyRequest("getPost", instance=instance, form=form, optional=optional, auth=auth)
+        
         return res["post_view"]
         
     def create(self, community_id:int, title:str=None, body:str=None, remote_url:str=None, honeypot:str=None, nsfw:bool=False, language_id:int=None, instance:str=None):
         """
         Create a post
         
         Args:
```

### Comparing `jplaw-0.1.8/jplaw/private_message.py` & `jplaw-0.1.9/jplaw/private_message.py`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/jplaw/requestor.py` & `jplaw-0.1.9/jplaw/requestor.py`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/jplaw/site.py` & `jplaw-0.1.9/jplaw/site.py`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/jplaw/types/modlog_action_type.py` & `jplaw-0.1.9/jplaw/types/modlog_action_type.py`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/jplaw/types/sort_type.py` & `jplaw-0.1.9/jplaw/types/sort_type.py`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/jplaw/user.py` & `jplaw-0.1.9/jplaw/user.py`

 * *Files 1% similar despite different names*

```diff
@@ -305,14 +305,16 @@
         """
         form={}
         res = self._req.lemmyRequest("markAllAsRead", instance=instance, form=form, auth=True)
         return res
         
     def saveUserSettings(self,
         show_nsfw: bool=None,
+        blur_nsfw: bool=None,
+        auto_expand: bool=None,
         show_scores: bool=None,
         theme: str=None,
         default_sort_type: SortType=None,
         default_listing_type: ListingType=None,
         interface_language: str=None,
         avatar: str=None,
         banner: str=None,
@@ -331,15 +333,17 @@
         open_links_in_new_tab: bool=None,
         instance:str=None):
         """
         Save user settings to account
         
         Args:
             show_nsfw (bool): If NSFW posts and communities should be shown. Optional
-            show_scores (bool) If scores should be shown. Optional
+            show_scores (bool): If scores should be shown. Optional
+            blur_nsfw (bool): If nsfw thumbnails and images should be blurred before opening the image. Optional
+            auto_expand (bool): If true, autoexpand images. Optional.
             theme (str): Site theme. Optional
             default_sort_type (SortType): Sort type for the site. Optional
             default_listing_type (ListingType): Default listing type. Allows viewing Local or All communities. Optional
             interface_language (str): Interface language string. Optional
             avatar (str): URL of avatar. Optional
             banner (str): URL of user banner. Optional
             display_name (str): DIsplay name of the user. Optional
```

### Comparing `jplaw-0.1.8/jplaw.egg-info/PKG-INFO` & `jplaw-0.1.9/jplaw.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jplaw
-Version: 0.1.8
+Version: 0.1.9
 Summary: A python wrapper for the lemmy HTTP API. Forked from plaw by Benjamin Jablonski (benja810)
 Author-email: Amar Persaud <tehspartaa@gmail.com>
 Project-URL: Homepage, https://github.com/amarpersaud/python-jplaw
 Project-URL: Bug Tracker, https://github.com/amarpersaud/python-jplaw/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -57,14 +57,22 @@
 See [the documentation](https://amarpersaud.github.io/python-jplaw/) for more information on how to use jplaw.
 
 # Roadmap 
 - Work on return types and usability.
 - Work on testing functions and finding / squashing bugs
 
 # Changelog
+### v0.1.9
+- Add blur_nsfw and auto_expand parameters to saveUserSettings
+- Add moderator_view parameter to Post.list()
+
+### v0.1.8
+- Fixes Community.edit()
+- Adds Lemmy.federateCommunity()
+
 
 ### v0.1.7
 - Fix bug with "fixed" boolean values
 
 ### v0.1.6
 - Fixes boolean and Enum parameters
 - Adds show_nsfw to communities
```

### Comparing `jplaw-0.1.8/jplaw.egg-info/SOURCES.txt` & `jplaw-0.1.9/jplaw.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `jplaw-0.1.8/pyproject.toml` & `jplaw-0.1.9/pyproject.toml`

 * *Files identical despite different names*

