# Comparing `tmp/django_azure_ad_auth_redux-1.5.22.tar.gz` & `tmp/django_azure_ad_auth_redux-1.5.23.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django_azure_ad_auth_redux-1.5.22.tar", max compression
+gzip compressed data, was "django_azure_ad_auth_redux-1.5.23.tar", max compression
```

## Comparing `django_azure_ad_auth_redux-1.5.22.tar` & `django_azure_ad_auth_redux-1.5.23.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     1588 2023-07-21 18:20:38.857349 django_azure_ad_auth_redux-1.5.22/LICENSE
--rw-r--r--   0        0        0     1610 2023-07-21 17:45:48.627893 django_azure_ad_auth_redux-1.5.22/README.md
--rw-r--r--   0        0        0      632 2023-07-22 21:51:37.579987 django_azure_ad_auth_redux-1.5.22/azure_ad_auth/__init__.py
--rw-r--r--   0        0        0     3736 2023-07-21 18:57:34.242612 django_azure_ad_auth_redux-1.5.22/azure_ad_auth/backends.py
--rw-r--r--   0        0        0      186 2023-07-21 18:29:17.765056 django_azure_ad_auth_redux-1.5.22/azure_ad_auth/urls.py
--rw-r--r--   0        0        0     3861 2023-07-22 21:51:18.635933 django_azure_ad_auth_redux-1.5.22/azure_ad_auth/utils.py
--rw-r--r--   0        0        0     1744 2023-07-21 18:53:49.464263 django_azure_ad_auth_redux-1.5.22/azure_ad_auth/views.py
--rw-r--r--   0        0        0     5536 2023-07-22 21:51:30.793036 django_azure_ad_auth_redux-1.5.22/pyproject.toml
--rw-r--r--   0        0        0     2951 1970-01-01 00:00:00.000000 django_azure_ad_auth_redux-1.5.22/PKG-INFO
+-rw-r--r--   0        0        0     1588 2023-07-21 18:20:38.857349 django_azure_ad_auth_redux-1.5.23/LICENSE
+-rw-r--r--   0        0        0     1610 2023-07-21 17:45:48.627893 django_azure_ad_auth_redux-1.5.23/README.md
+-rw-r--r--   0        0        0      632 2023-07-22 22:10:47.044487 django_azure_ad_auth_redux-1.5.23/azure_ad_auth/__init__.py
+-rw-r--r--   0        0        0     3736 2023-07-21 18:57:34.242612 django_azure_ad_auth_redux-1.5.23/azure_ad_auth/backends.py
+-rw-r--r--   0        0        0      186 2023-07-21 18:29:17.765056 django_azure_ad_auth_redux-1.5.23/azure_ad_auth/urls.py
+-rw-r--r--   0        0        0     3862 2023-07-22 22:10:56.240049 django_azure_ad_auth_redux-1.5.23/azure_ad_auth/utils.py
+-rw-r--r--   0        0        0     1744 2023-07-21 18:53:49.464263 django_azure_ad_auth_redux-1.5.23/azure_ad_auth/views.py
+-rw-r--r--   0        0        0     5536 2023-07-22 22:10:39.266393 django_azure_ad_auth_redux-1.5.23/pyproject.toml
+-rw-r--r--   0        0        0     2951 1970-01-01 00:00:00.000000 django_azure_ad_auth_redux-1.5.23/PKG-INFO
```

### Comparing `django_azure_ad_auth_redux-1.5.22/LICENSE` & `django_azure_ad_auth_redux-1.5.23/LICENSE`

 * *Files identical despite different names*

### Comparing `django_azure_ad_auth_redux-1.5.22/README.md` & `django_azure_ad_auth_redux-1.5.23/README.md`

 * *Files identical despite different names*

### Comparing `django_azure_ad_auth_redux-1.5.22/azure_ad_auth/__init__.py` & `django_azure_ad_auth_redux-1.5.23/azure_ad_auth/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 __version_info__ = {
     "major": 1,
     "minor": 5,
-    "micro": 22,
+    "micro": 23,
     "releaselevel": "final",
     "serial": 11,
 }
 
 
 def get_version(short=False):
     assert __version_info__["releaselevel"] in ("alpha", "beta", "final")  # noqa: S101
```

### Comparing `django_azure_ad_auth_redux-1.5.22/azure_ad_auth/backends.py` & `django_azure_ad_auth_redux-1.5.23/azure_ad_auth/backends.py`

 * *Files identical despite different names*

### Comparing `django_azure_ad_auth_redux-1.5.22/azure_ad_auth/utils.py` & `django_azure_ad_auth_redux-1.5.23/azure_ad_auth/utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -90,15 +90,15 @@
     except Exception:  # TODO - which ones exactly?
         keys = []
     return keys
 
 
 def get_token_payload(token=None, audience=CLIENT_ID, nonce=None):
     headers = jwt.get_unverified_header(token)
-    algorithm = header.get("alg", "RS256")
+    algorithm = headers.get("alg", "RS256")
     for key in get_public_keys():
         try:
             payload = jwt.decode(
                 token,
                 key=key,
                 audience=audience,
                 algorithms=[algorithm],
```

### Comparing `django_azure_ad_auth_redux-1.5.22/azure_ad_auth/views.py` & `django_azure_ad_auth_redux-1.5.23/azure_ad_auth/views.py`

 * *Files identical despite different names*

### Comparing `django_azure_ad_auth_redux-1.5.22/pyproject.toml` & `django_azure_ad_auth_redux-1.5.23/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "django-azure-ad-auth-redux"
-version = "1.5.22"
+version = "1.5.23"
 description="Authenticate users using Azure Active Directory."
 authors = ["Scott Sharkey <scott.sharkey@rsginc.com>"]
 license = "MIT"
 packages = [{include = "azure_ad_auth"}]
 readme = "README.md"
 repository = "https://github.com/lanshark/django-azure-ad-auth-redux"
 homepage = "https://github.com/lanshark/django-azure-ad-auth-redux"
```

### Comparing `django_azure_ad_auth_redux-1.5.22/PKG-INFO` & `django_azure_ad_auth_redux-1.5.23/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-azure-ad-auth-redux
-Version: 1.5.22
+Version: 1.5.23
 Summary: Authenticate users using Azure Active Directory.
 Home-page: https://github.com/lanshark/django-azure-ad-auth-redux
 License: MIT
 Keywords: Python, Active Directory, Django
 Author: Scott Sharkey
 Author-email: scott.sharkey@rsginc.com
 Requires-Python: >=3.10,<3.12
```

