# Comparing `tmp/aioplemmy-0.3.2.tar.gz` & `tmp/aioplemmy-0.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "aioplemmy-0.3.2.tar", last modified: Fri Jul 21 20:05:12 2023, max compression
+gzip compressed data, was "aioplemmy-0.3.3.tar", last modified: Sun Jul 23 10:18:14 2023, max compression
```

## Comparing `aioplemmy-0.3.2.tar` & `aioplemmy-0.3.3.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxrwx   0        0        0        0 2023-07-21 20:05:12.782428 aioplemmy-0.3.2/
--rw-rw-rw-   0        0        0    11568 2023-07-21 14:18:38.000000 aioplemmy-0.3.2/LICENSE
--rw-rw-rw-   0        0        0     4144 2023-07-21 20:05:12.782428 aioplemmy-0.3.2/PKG-INFO
--rw-rw-rw-   0        0        0     3839 2023-07-21 19:56:16.000000 aioplemmy-0.3.2/README.md
-drwxrwxrwx   0        0        0        0 2023-07-21 20:05:12.776430 aioplemmy-0.3.2/aioplemmy/
--rw-rw-rw-   0        0        0      162 2023-07-21 19:51:22.000000 aioplemmy-0.3.2/aioplemmy/__init__.py
--rw-rw-rw-   0        0        0    64328 2023-07-21 19:27:02.000000 aioplemmy-0.3.2/aioplemmy/lemmyhttp.py
--rw-rw-rw-   0        0        0    14608 2023-07-21 14:18:38.000000 aioplemmy-0.3.2/aioplemmy/objects.py
--rw-rw-rw-   0        0        0    17209 2023-07-21 17:43:38.000000 aioplemmy-0.3.2/aioplemmy/responses.py
--rw-rw-rw-   0        0        0      120 2023-07-21 14:18:38.000000 aioplemmy-0.3.2/aioplemmy/version.py
--rw-rw-rw-   0        0        0    18878 2023-07-21 17:49:04.000000 aioplemmy-0.3.2/aioplemmy/views.py
-drwxrwxrwx   0        0        0        0 2023-07-21 20:05:12.781429 aioplemmy-0.3.2/aioplemmy.egg-info/
--rw-rw-rw-   0        0        0     4144 2023-07-21 20:05:12.000000 aioplemmy-0.3.2/aioplemmy.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      351 2023-07-21 20:05:12.000000 aioplemmy-0.3.2/aioplemmy.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-21 20:05:12.000000 aioplemmy-0.3.2/aioplemmy.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-07-21 20:05:12.000000 aioplemmy-0.3.2/aioplemmy.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       29 2023-07-21 20:05:12.000000 aioplemmy-0.3.2/aioplemmy.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-07-21 20:05:12.000000 aioplemmy-0.3.2/aioplemmy.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-21 20:05:12.782428 aioplemmy-0.3.2/setup.cfg
--rw-rw-rw-   0        0        0      930 2023-07-21 19:40:26.000000 aioplemmy-0.3.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 10:18:14.830947 aioplemmy-0.3.3/
+-rw-rw-rw-   0        0        0    11568 2023-07-21 14:18:38.000000 aioplemmy-0.3.3/LICENSE
+-rw-rw-rw-   0        0        0     4144 2023-07-23 10:18:14.829441 aioplemmy-0.3.3/PKG-INFO
+-rw-rw-rw-   0        0        0     3839 2023-07-21 19:56:16.000000 aioplemmy-0.3.3/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 10:18:14.823443 aioplemmy-0.3.3/aioplemmy/
+-rw-rw-rw-   0        0        0      162 2023-07-21 19:51:22.000000 aioplemmy-0.3.3/aioplemmy/__init__.py
+-rw-rw-rw-   0        0        0    64513 2023-07-23 08:54:58.000000 aioplemmy-0.3.3/aioplemmy/lemmyhttp.py
+-rw-rw-rw-   0        0        0    15039 2023-07-23 10:15:48.000000 aioplemmy-0.3.3/aioplemmy/objects.py
+-rw-rw-rw-   0        0        0    17209 2023-07-21 17:43:38.000000 aioplemmy-0.3.3/aioplemmy/responses.py
+-rw-rw-rw-   0        0        0      120 2023-07-23 09:22:29.000000 aioplemmy-0.3.3/aioplemmy/version.py
+-rw-rw-rw-   0        0        0    18878 2023-07-21 17:49:04.000000 aioplemmy-0.3.3/aioplemmy/views.py
+drwxrwxrwx   0        0        0        0 2023-07-23 10:18:14.829441 aioplemmy-0.3.3/aioplemmy.egg-info/
+-rw-rw-rw-   0        0        0     4144 2023-07-23 10:18:14.000000 aioplemmy-0.3.3/aioplemmy.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      351 2023-07-23 10:18:14.000000 aioplemmy-0.3.3/aioplemmy.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 10:18:14.000000 aioplemmy-0.3.3/aioplemmy.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-07-21 20:05:12.000000 aioplemmy-0.3.3/aioplemmy.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       29 2023-07-23 10:18:14.000000 aioplemmy-0.3.3/aioplemmy.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-07-23 10:18:14.000000 aioplemmy-0.3.3/aioplemmy.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 10:18:14.830947 aioplemmy-0.3.3/setup.cfg
+-rw-rw-rw-   0        0        0      930 2023-07-21 19:40:26.000000 aioplemmy-0.3.3/setup.py
```

### Comparing `aioplemmy-0.3.2/LICENSE` & `aioplemmy-0.3.3/LICENSE`

 * *Files identical despite different names*

### Comparing `aioplemmy-0.3.2/PKG-INFO` & `aioplemmy-0.3.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aioplemmy
-Version: 0.3.2
+Version: 0.3.3
 Summary: Python API for LemmyHttp
 Home-page: https://github.com/schicksal-hq/plemmy
 Author: Travis Kessler
 Author-email: travis.j.kessler@gmail.com
 License: Apache License 2.0
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

### Comparing `aioplemmy-0.3.2/README.md` & `aioplemmy-0.3.3/README.md`

 * *Files identical despite different names*

### Comparing `aioplemmy-0.3.2/aioplemmy/lemmyhttp.py` & `aioplemmy-0.3.3/aioplemmy/lemmyhttp.py`

 * *Files 0% similar despite different names*

```diff
@@ -50,30 +50,36 @@
             form = {k: v for k, v in data.items() if v is not None and k != "self"}
         else:
             form = {}
 
         if self.key is not None:
             form["auth"] = self.key
 
-        async with self.client as http:
-            if form_in_params:
-                resp = await getattr(http, method)(f"/api/{API_VERSION}{route}", params=form)
-            else:
-                resp = await getattr(http, method)(f"/api/{API_VERSION}{route}", json=form)
+        if form_in_params:
+            resp = await getattr(self.client, method)(f"/api/{API_VERSION}{route}", params=form)
+        else:
+            resp = await getattr(self.client, method)(f"/api/{API_VERSION}{route}", json=form)
 
-            if resp.status != 200:
-                if resp.content_type == 'application/json':
-                    error_resp = await resp.json(loads=self.de_json)
-                    error = error_resp["error"].upper()
+        if resp.status != 200:
+            if resp.content_type == 'application/json':
+                error_resp = await resp.json(loads=self.de_json)
+                error = error_resp["error"].upper()
 
-                    raise LemmyError(f"[{resp.status}] Lemmy API returned {error} exception", error)
+                raise LemmyError(f"[{resp.status}] Lemmy API returned {error} exception", error)
+            else:
+                maybe_error = (await resp.text())
+                if maybe_error is None:
+                    maybe_error = "Unknown error"
                 else:
-                    raise LemmyError(f"[{resp.status}] Generic error encountered while trying to {method} {route}")
+                    maybe_error = maybe_error.upper()
+
+                raise LemmyError(
+                    f"[{resp.status}] Generic error encountered while trying to {method} {route}: {maybe_error}")
 
-            return await resp.json(loads=self.de_json)
+        return await resp.json(loads=self.de_json)
 
     async def _post_handler(self, endpoint: str, data: Optional[dict] = None) -> dict:
         return await self._fire_request(endpoint, "POST", data, False)
 
     async def _put_handler(self, endpoint: str, data: Optional[dict] = None) -> dict:
         return await self._fire_request(endpoint, "PUT", data, False)
```

### Comparing `aioplemmy-0.3.2/aioplemmy/responses.py` & `aioplemmy-0.3.3/aioplemmy/responses.py`

 * *Files identical despite different names*

### Comparing `aioplemmy-0.3.2/aioplemmy/views.py` & `aioplemmy-0.3.3/aioplemmy/views.py`

 * *Files identical despite different names*

### Comparing `aioplemmy-0.3.2/aioplemmy.egg-info/PKG-INFO` & `aioplemmy-0.3.3/aioplemmy.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aioplemmy
-Version: 0.3.2
+Version: 0.3.3
 Summary: Python API for LemmyHttp
 Home-page: https://github.com/schicksal-hq/plemmy
 Author: Travis Kessler
 Author-email: travis.j.kessler@gmail.com
 License: Apache License 2.0
 Description-Content-Type: text/markdown
 License-File: LICENSE
```

### Comparing `aioplemmy-0.3.2/setup.py` & `aioplemmy-0.3.3/setup.py`

 * *Files identical despite different names*

