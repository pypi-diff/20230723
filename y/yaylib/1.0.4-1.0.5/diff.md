# Comparing `tmp/yaylib-1.0.4.tar.gz` & `tmp/yaylib-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "yaylib-1.0.4.tar", last modified: Sat Jul 22 09:15:23 2023, max compression
+gzip compressed data, was "yaylib-1.0.5.tar", last modified: Sun Jul 23 06:21:11 2023, max compression
```

## Comparing `yaylib-1.0.4.tar` & `yaylib-1.0.5.tar`

### file list

```diff
@@ -1,44 +1,44 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 09:15:23.303621 yaylib-1.0.4/
--rw-rw-rw-   0        0        0     1096 2023-07-09 07:25:01.000000 yaylib-1.0.4/LICENSE
--rw-rw-rw-   0        0        0    10828 2023-07-22 09:15:23.302615 yaylib-1.0.4/PKG-INFO
--rw-rw-rw-   0        0        0     9964 2023-07-18 08:52:45.000000 yaylib-1.0.4/README.md
--rw-rw-rw-   0        0        0       42 2023-07-22 09:15:23.303621 yaylib-1.0.4/setup.cfg
--rw-rw-rw-   0        0        0     1584 2023-07-21 11:06:20.000000 yaylib-1.0.4/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-22 09:15:23.254603 yaylib-1.0.4/tests/
--rw-rw-rw-   0        0        0     1335 2023-07-09 07:25:01.000000 yaylib-1.0.4/tests/test_call.py
--rw-rw-rw-   0        0        0     1935 2023-07-09 07:25:01.000000 yaylib-1.0.4/tests/test_cassandra.py
--rw-rw-rw-   0        0        0     1335 2023-07-09 07:25:01.000000 yaylib-1.0.4/tests/test_chat.py
--rw-rw-rw-   0        0        0     1337 2023-07-09 07:25:01.000000 yaylib-1.0.4/tests/test_group.py
--rw-rw-rw-   0        0        0     1335 2023-07-09 07:25:01.000000 yaylib-1.0.4/tests/test_misc.py
--rw-rw-rw-   0        0        0     3723 2023-07-09 07:25:01.000000 yaylib-1.0.4/tests/test_post.py
--rw-rw-rw-   0        0        0     2028 2023-07-09 07:25:01.000000 yaylib-1.0.4/tests/test_review.py
--rw-rw-rw-   0        0        0     1339 2023-07-09 07:25:01.000000 yaylib-1.0.4/tests/test_thread.py
--rw-rw-rw-   0        0        0     1335 2023-07-09 07:25:01.000000 yaylib-1.0.4/tests/test_user.py
-drwxrwxrwx   0        0        0        0 2023-07-22 09:15:23.265092 yaylib-1.0.4/yaylib/
--rw-rw-rw-   0        0        0      664 2023-07-21 11:06:20.000000 yaylib-1.0.4/yaylib/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-22 09:15:23.301608 yaylib-1.0.4/yaylib/api/
--rw-rw-rw-   0        0        0      697 2023-07-09 07:25:01.000000 yaylib-1.0.4/yaylib/api/__init__.py
--rw-rw-rw-   0        0        0    10255 2023-07-19 13:28:39.000000 yaylib-1.0.4/yaylib/api/api.py
--rw-rw-rw-   0        0        0     9431 2023-07-18 11:05:38.000000 yaylib-1.0.4/yaylib/api/call.py
--rw-rw-rw-   0        0        0     2699 2023-07-18 08:52:45.000000 yaylib-1.0.4/yaylib/api/cassandra.py
--rw-rw-rw-   0        0        0    15017 2023-07-21 11:06:20.000000 yaylib-1.0.4/yaylib/api/chat.py
--rw-rw-rw-   0        0        0    23695 2023-07-18 08:52:45.000000 yaylib-1.0.4/yaylib/api/group.py
--rw-rw-rw-   0        0        0     8224 2023-07-20 07:15:23.000000 yaylib-1.0.4/yaylib/api/login.py
--rw-rw-rw-   0        0        0     7417 2023-07-18 08:52:45.000000 yaylib-1.0.4/yaylib/api/misc.py
--rw-rw-rw-   0        0        0    33686 2023-07-22 09:13:37.000000 yaylib-1.0.4/yaylib/api/post.py
--rw-rw-rw-   0        0        0     4488 2023-07-18 08:52:45.000000 yaylib-1.0.4/yaylib/api/review.py
--rw-rw-rw-   0        0        0     5945 2023-07-18 08:52:45.000000 yaylib-1.0.4/yaylib/api/thread.py
--rw-rw-rw-   0        0        0    23744 2023-07-19 12:23:37.000000 yaylib-1.0.4/yaylib/api/user.py
--rw-rw-rw-   0        0        0    86548 2023-07-21 11:06:20.000000 yaylib-1.0.4/yaylib/client.py
--rw-rw-rw-   0        0        0    19309 2023-07-22 09:15:14.000000 yaylib-1.0.4/yaylib/config.py
--rw-rw-rw-   0        0        0     2131 2023-07-18 08:52:45.000000 yaylib-1.0.4/yaylib/errors.py
--rw-rw-rw-   0        0        0    56113 2023-07-21 11:49:21.000000 yaylib-1.0.4/yaylib/models.py
--rw-rw-rw-   0        0        0    34292 2023-07-21 11:34:08.000000 yaylib-1.0.4/yaylib/responses.py
--rw-rw-rw-   0        0        0     4473 2023-07-20 07:15:24.000000 yaylib-1.0.4/yaylib/utils.py
--rw-rw-rw-   0        0        0     9374 2023-07-21 12:27:01.000000 yaylib-1.0.4/yaylib/websocket.py
-drwxrwxrwx   0        0        0        0 2023-07-22 09:15:23.283775 yaylib-1.0.4/yaylib.egg-info/
--rw-rw-rw-   0        0        0    10828 2023-07-22 09:15:23.000000 yaylib-1.0.4/yaylib.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      741 2023-07-22 09:15:23.000000 yaylib-1.0.4/yaylib.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 09:15:23.000000 yaylib-1.0.4/yaylib.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       73 2023-07-22 09:15:23.000000 yaylib-1.0.4/yaylib.egg-info/requires.txt
--rw-rw-rw-   0        0        0        7 2023-07-22 09:15:23.000000 yaylib-1.0.4/yaylib.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 06:21:11.943815 yaylib-1.0.5/
+-rw-rw-rw-   0        0        0     1096 2023-07-09 07:25:01.000000 yaylib-1.0.5/LICENSE
+-rw-rw-rw-   0        0        0    10828 2023-07-23 06:21:11.943815 yaylib-1.0.5/PKG-INFO
+-rw-rw-rw-   0        0        0     9964 2023-07-18 08:52:45.000000 yaylib-1.0.5/README.md
+-rw-rw-rw-   0        0        0       42 2023-07-23 06:21:11.945118 yaylib-1.0.5/setup.cfg
+-rw-rw-rw-   0        0        0     1584 2023-07-21 11:06:20.000000 yaylib-1.0.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 06:21:11.905046 yaylib-1.0.5/tests/
+-rw-rw-rw-   0        0        0     1335 2023-07-09 07:25:01.000000 yaylib-1.0.5/tests/test_call.py
+-rw-rw-rw-   0        0        0     1935 2023-07-09 07:25:01.000000 yaylib-1.0.5/tests/test_cassandra.py
+-rw-rw-rw-   0        0        0     1335 2023-07-09 07:25:01.000000 yaylib-1.0.5/tests/test_chat.py
+-rw-rw-rw-   0        0        0     1337 2023-07-09 07:25:01.000000 yaylib-1.0.5/tests/test_group.py
+-rw-rw-rw-   0        0        0     1335 2023-07-09 07:25:01.000000 yaylib-1.0.5/tests/test_misc.py
+-rw-rw-rw-   0        0        0     3723 2023-07-09 07:25:01.000000 yaylib-1.0.5/tests/test_post.py
+-rw-rw-rw-   0        0        0     2028 2023-07-09 07:25:01.000000 yaylib-1.0.5/tests/test_review.py
+-rw-rw-rw-   0        0        0     1339 2023-07-09 07:25:01.000000 yaylib-1.0.5/tests/test_thread.py
+-rw-rw-rw-   0        0        0     1335 2023-07-09 07:25:01.000000 yaylib-1.0.5/tests/test_user.py
+drwxrwxrwx   0        0        0        0 2023-07-23 06:21:11.913358 yaylib-1.0.5/yaylib/
+-rw-rw-rw-   0        0        0      664 2023-07-21 11:06:20.000000 yaylib-1.0.5/yaylib/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 06:21:11.942810 yaylib-1.0.5/yaylib/api/
+-rw-rw-rw-   0        0        0      697 2023-07-09 07:25:01.000000 yaylib-1.0.5/yaylib/api/__init__.py
+-rw-rw-rw-   0        0        0    10255 2023-07-19 13:28:39.000000 yaylib-1.0.5/yaylib/api/api.py
+-rw-rw-rw-   0        0        0     9429 2023-07-23 06:18:02.000000 yaylib-1.0.5/yaylib/api/call.py
+-rw-rw-rw-   0        0        0     2699 2023-07-18 08:52:45.000000 yaylib-1.0.5/yaylib/api/cassandra.py
+-rw-rw-rw-   0        0        0    15017 2023-07-21 11:06:20.000000 yaylib-1.0.5/yaylib/api/chat.py
+-rw-rw-rw-   0        0        0    23695 2023-07-18 08:52:45.000000 yaylib-1.0.5/yaylib/api/group.py
+-rw-rw-rw-   0        0        0     8224 2023-07-20 07:15:23.000000 yaylib-1.0.5/yaylib/api/login.py
+-rw-rw-rw-   0        0        0     7417 2023-07-18 08:52:45.000000 yaylib-1.0.5/yaylib/api/misc.py
+-rw-rw-rw-   0        0        0    33686 2023-07-22 09:13:37.000000 yaylib-1.0.5/yaylib/api/post.py
+-rw-rw-rw-   0        0        0     4488 2023-07-18 08:52:45.000000 yaylib-1.0.5/yaylib/api/review.py
+-rw-rw-rw-   0        0        0     5945 2023-07-18 08:52:45.000000 yaylib-1.0.5/yaylib/api/thread.py
+-rw-rw-rw-   0        0        0    23744 2023-07-19 12:23:37.000000 yaylib-1.0.5/yaylib/api/user.py
+-rw-rw-rw-   0        0        0    86548 2023-07-21 11:06:20.000000 yaylib-1.0.5/yaylib/client.py
+-rw-rw-rw-   0        0        0    19309 2023-07-23 06:21:04.000000 yaylib-1.0.5/yaylib/config.py
+-rw-rw-rw-   0        0        0     2131 2023-07-18 08:52:45.000000 yaylib-1.0.5/yaylib/errors.py
+-rw-rw-rw-   0        0        0    56113 2023-07-21 11:49:21.000000 yaylib-1.0.5/yaylib/models.py
+-rw-rw-rw-   0        0        0    34292 2023-07-21 11:34:08.000000 yaylib-1.0.5/yaylib/responses.py
+-rw-rw-rw-   0        0        0     4473 2023-07-20 07:15:24.000000 yaylib-1.0.5/yaylib/utils.py
+-rw-rw-rw-   0        0        0     9374 2023-07-21 12:27:01.000000 yaylib-1.0.5/yaylib/websocket.py
+drwxrwxrwx   0        0        0        0 2023-07-23 06:21:11.930194 yaylib-1.0.5/yaylib.egg-info/
+-rw-rw-rw-   0        0        0    10828 2023-07-23 06:21:11.000000 yaylib-1.0.5/yaylib.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      741 2023-07-23 06:21:11.000000 yaylib-1.0.5/yaylib.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 06:21:11.000000 yaylib-1.0.5/yaylib.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       73 2023-07-23 06:21:11.000000 yaylib-1.0.5/yaylib.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        7 2023-07-23 06:21:11.000000 yaylib-1.0.5/yaylib.egg-info/top_level.txt
```

### Comparing `yaylib-1.0.4/LICENSE` & `yaylib-1.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/PKG-INFO` & `yaylib-1.0.5/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yaylib
-Version: 1.0.4
+Version: 1.0.5
 Summary: This Python package provides an easy-to-use interface for accessing data from Yay! (https://yay.space/). With this API Client, you can retrieve user profiles, posts, comments, and other content from Yay!, as well as perform common tasks like liking and commenting on posts.
 Home-page: https://github.com/qvco/yaylib
 Download-URL: https://github.com/qvco/yaylib
 Author: Qvco, Konn
 Author-email: nikola.desuga@gmail.com
 Maintainer: Qvco, Konn
 Maintainer-email: nikola.desuga@gmail.com
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: yaylib Version: 1.0.4 Summary: This Python package
+Metadata-Version: 2.1 Name: yaylib Version: 1.0.5 Summary: This Python package
 provides an easy-to-use interface for accessing data from Yay! (https://
 yay.space/). With this API Client, you can retrieve user profiles, posts,
 comments, and other content from Yay!, as well as perform common tasks like
 liking and commenting on posts. Home-page: https://github.com/qvco/yaylib
 Download-URL: https://github.com/qvco/yaylib Author: Qvco, Konn Author-email:
 nikola.desuga@gmail.com Maintainer: Qvco, Konn Maintainer-email:
 nikola.desuga@gmail.com License: MIT Keywords:
```

### Comparing `yaylib-1.0.4/README.md` & `yaylib-1.0.5/README.md`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/setup.py` & `yaylib-1.0.5/setup.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/tests/test_call.py` & `yaylib-1.0.5/tests/test_call.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/tests/test_cassandra.py` & `yaylib-1.0.5/tests/test_cassandra.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/tests/test_chat.py` & `yaylib-1.0.5/tests/test_chat.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/tests/test_group.py` & `yaylib-1.0.5/tests/test_group.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/tests/test_misc.py` & `yaylib-1.0.5/tests/test_misc.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/tests/test_post.py` & `yaylib-1.0.5/tests/test_post.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/tests/test_review.py` & `yaylib-1.0.5/tests/test_review.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/tests/test_thread.py` & `yaylib-1.0.5/tests/test_thread.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/tests/test_user.py` & `yaylib-1.0.5/tests/test_user.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/__init__.py` & `yaylib-1.0.5/yaylib/__init__.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/api/__init__.py` & `yaylib-1.0.5/yaylib/api/__init__.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/api/api.py` & `yaylib-1.0.5/yaylib/api/api.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/api/call.py` & `yaylib-1.0.5/yaylib/api/call.py`

 * *Files 1% similar despite different names*

```diff
@@ -200,15 +200,15 @@
         - call_id: int - (required)
         - user_ids: List[int] - (required)
 
     """
     response = self._make_request(
         "POST",
         endpoint=f"{Endpoints.CALLS_V1}/conference_calls/{call_id}/invite",
-        payload={"call_id": call_id, "user_ids[]": user_ids},
+        payload={"call_id": call_id, "user_ids": user_ids},
         access_token=access_token,
     )
     self.logger.info("Invited users to call.")
     return response
 
 
 def invite_users_to_chat_call(
```

### Comparing `yaylib-1.0.4/yaylib/api/cassandra.py` & `yaylib-1.0.5/yaylib/api/cassandra.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/api/chat.py` & `yaylib-1.0.5/yaylib/api/chat.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/api/group.py` & `yaylib-1.0.5/yaylib/api/group.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/api/login.py` & `yaylib-1.0.5/yaylib/api/login.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/api/misc.py` & `yaylib-1.0.5/yaylib/api/misc.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/api/post.py` & `yaylib-1.0.5/yaylib/api/post.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/api/review.py` & `yaylib-1.0.5/yaylib/api/review.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/api/thread.py` & `yaylib-1.0.5/yaylib/api/thread.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/api/user.py` & `yaylib-1.0.5/yaylib/api/user.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/client.py` & `yaylib-1.0.5/yaylib/client.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/config.py` & `yaylib-1.0.5/yaylib/config.py`

 * *Files 0% similar despite different names*

```diff
@@ -22,15 +22,15 @@
 SOFTWARE.
 """
 
 from enum import Enum
 
 
 class Configs:
-    YAYLIB_VERSION = "1.0.4"
+    YAYLIB_VERSION = "1.0.5"
     YAY_API_VERSION = "3.20"
     YAY_VERSION_NAME = "3.20.1"
     YAY_API_VERSION_KEY = "d4420f4943bebe2831c20b2b4cb4a8c1"
     YAY_API_KEY = "ccd59ee269c01511ba763467045c115779fcae3050238a252f1bd1a4b65cfec6"
     YAY_SHARED_KEY = "yayZ1"
     YAY_STORE_KEY = "yayZ1payment"
     AGORA_APP_ID = "79046b8c9be54945b7f10a4d128d5395"
```

### Comparing `yaylib-1.0.4/yaylib/errors.py` & `yaylib-1.0.5/yaylib/errors.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/models.py` & `yaylib-1.0.5/yaylib/models.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/responses.py` & `yaylib-1.0.5/yaylib/responses.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/utils.py` & `yaylib-1.0.5/yaylib/utils.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib/websocket.py` & `yaylib-1.0.5/yaylib/websocket.py`

 * *Files identical despite different names*

### Comparing `yaylib-1.0.4/yaylib.egg-info/PKG-INFO` & `yaylib-1.0.5/yaylib.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yaylib
-Version: 1.0.4
+Version: 1.0.5
 Summary: This Python package provides an easy-to-use interface for accessing data from Yay! (https://yay.space/). With this API Client, you can retrieve user profiles, posts, comments, and other content from Yay!, as well as perform common tasks like liking and commenting on posts.
 Home-page: https://github.com/qvco/yaylib
 Download-URL: https://github.com/qvco/yaylib
 Author: Qvco, Konn
 Author-email: nikola.desuga@gmail.com
 Maintainer: Qvco, Konn
 Maintainer-email: nikola.desuga@gmail.com
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: yaylib Version: 1.0.4 Summary: This Python package
+Metadata-Version: 2.1 Name: yaylib Version: 1.0.5 Summary: This Python package
 provides an easy-to-use interface for accessing data from Yay! (https://
 yay.space/). With this API Client, you can retrieve user profiles, posts,
 comments, and other content from Yay!, as well as perform common tasks like
 liking and commenting on posts. Home-page: https://github.com/qvco/yaylib
 Download-URL: https://github.com/qvco/yaylib Author: Qvco, Konn Author-email:
 nikola.desuga@gmail.com Maintainer: Qvco, Konn Maintainer-email:
 nikola.desuga@gmail.com License: MIT Keywords:
```

### Comparing `yaylib-1.0.4/yaylib.egg-info/SOURCES.txt` & `yaylib-1.0.5/yaylib.egg-info/SOURCES.txt`

 * *Files identical despite different names*

