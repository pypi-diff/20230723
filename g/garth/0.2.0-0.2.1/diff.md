# Comparing `tmp/garth-0.2.0.tar.gz` & `tmp/garth-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "garth-0.2.0.tar", last modified: Sun Jul 23 16:24:58 2023, max compression
+gzip compressed data, was "garth-0.2.1.tar", last modified: Sun Jul 23 16:28:07 2023, max compression
```

## Comparing `garth-0.2.0.tar` & `garth-0.2.1.tar`

### file list

```diff
@@ -1,25 +1,25 @@
--rw-r--r--   0        0        0     1071 2023-07-20 12:44:00.130760 garth-0.2.0/LICENSE
--rw-r--r--   0        0        0     3708 2023-07-22 17:44:18.353928 garth-0.2.0/README.md
--rw-r--r--   0        0        0      188 2023-07-23 16:21:37.236316 garth-0.2.0/garth/__init__.py
--rw-r--r--   0        0        0      913 2023-07-23 13:39:36.444380 garth-0.2.0/garth/auth_token.py
--rw-r--r--   0        0        0      145 2023-07-18 22:32:58.010661 garth-0.2.0/garth/exc.py
--rw-r--r--   0        0        0     4870 2023-07-23 16:06:33.692262 garth-0.2.0/garth/http.py
--rw-r--r--   0        0        0     3552 2023-07-23 16:09:16.949253 garth-0.2.0/garth/sso.py
--rw-r--r--   0        0        0        0 2023-07-16 18:57:56.389343 garth-0.2.0/garth/version.py
--rw-r--r--   0        0        0      733 2023-07-23 16:24:58.828177 garth-0.2.0/pyproject.toml
--rw-r--r--   0        0        0     2386 2023-07-22 11:39:14.617674 garth-0.2.0/tests/cassettes/test_client_get.yaml
--rw-r--r--   0        0        0     2425 2023-07-22 11:39:14.746057 garth-0.2.0/tests/cassettes/test_client_post.yaml
--rw-r--r--   0        0        0   100962 2023-07-22 11:22:15.428262 garth-0.2.0/tests/cassettes/test_client_request.yaml
--rw-r--r--   0        0        0     2331 2023-07-23 16:06:33.706591 garth-0.2.0/tests/cassettes/test_connectapi.yaml
--rw-r--r--   0        0        0     4564 2023-07-23 16:06:33.706751 garth-0.2.0/tests/cassettes/test_connectapi_refresh.yaml
--rw-r--r--   0        0        0     3231 2023-07-23 13:06:17.267462 garth-0.2.0/tests/cassettes/test_exchange.yaml
--rw-r--r--   0        0        0    10962 2023-07-23 13:53:16.232082 garth-0.2.0/tests/cassettes/test_get_username.yaml
--rw-r--r--   0        0        0    50551 2023-07-22 15:27:42.274531 garth-0.2.0/tests/cassettes/test_login_email_password_fail.yaml
--rw-r--r--   0        0        0    91847 2023-07-23 13:50:32.012417 garth-0.2.0/tests/cassettes/test_login_success.yaml
--rw-r--r--   0        0        0     2270 2023-07-23 13:09:36.525519 garth-0.2.0/tests/cassettes/test_refresh.yaml
--rw-r--r--   0        0        0     2963 2023-07-23 13:36:21.976543 garth-0.2.0/tests/cassettes/test_refresh_expired.yaml
--rw-r--r--   0        0        0     2940 2023-07-23 16:06:33.706957 garth-0.2.0/tests/conftest.py
--rw-r--r--   0        0        0     1808 2023-07-23 13:40:52.098938 garth-0.2.0/tests/test_auth_token.py
--rw-r--r--   0        0        0     4314 2023-07-23 16:06:33.707155 garth-0.2.0/tests/test_http.py
--rw-r--r--   0        0        0     2570 2023-07-23 13:18:13.595293 garth-0.2.0/tests/test_sso.py
--rw-r--r--   0        0        0     3955 1970-01-01 00:00:00.000000 garth-0.2.0/PKG-INFO
+-rw-r--r--   0        0        0     1071 2023-07-20 12:44:00.130760 garth-0.2.1/LICENSE
+-rw-r--r--   0        0        0     3708 2023-07-22 17:44:18.353928 garth-0.2.1/README.md
+-rw-r--r--   0        0        0      188 2023-07-23 16:26:05.839179 garth-0.2.1/garth/__init__.py
+-rw-r--r--   0        0        0      913 2023-07-23 13:39:36.444380 garth-0.2.1/garth/auth_token.py
+-rw-r--r--   0        0        0      145 2023-07-18 22:32:58.010661 garth-0.2.1/garth/exc.py
+-rw-r--r--   0        0        0     4870 2023-07-23 16:06:33.692262 garth-0.2.1/garth/http.py
+-rw-r--r--   0        0        0     3552 2023-07-23 16:09:16.949253 garth-0.2.1/garth/sso.py
+-rw-r--r--   0        0        0        0 2023-07-16 18:57:56.389343 garth-0.2.1/garth/version.py
+-rw-r--r--   0        0        0      809 2023-07-23 16:28:07.827793 garth-0.2.1/pyproject.toml
+-rw-r--r--   0        0        0     2386 2023-07-22 11:39:14.617674 garth-0.2.1/tests/cassettes/test_client_get.yaml
+-rw-r--r--   0        0        0     2425 2023-07-22 11:39:14.746057 garth-0.2.1/tests/cassettes/test_client_post.yaml
+-rw-r--r--   0        0        0   100962 2023-07-22 11:22:15.428262 garth-0.2.1/tests/cassettes/test_client_request.yaml
+-rw-r--r--   0        0        0     2331 2023-07-23 16:06:33.706591 garth-0.2.1/tests/cassettes/test_connectapi.yaml
+-rw-r--r--   0        0        0     4564 2023-07-23 16:06:33.706751 garth-0.2.1/tests/cassettes/test_connectapi_refresh.yaml
+-rw-r--r--   0        0        0     3231 2023-07-23 13:06:17.267462 garth-0.2.1/tests/cassettes/test_exchange.yaml
+-rw-r--r--   0        0        0    10962 2023-07-23 13:53:16.232082 garth-0.2.1/tests/cassettes/test_get_username.yaml
+-rw-r--r--   0        0        0    50551 2023-07-22 15:27:42.274531 garth-0.2.1/tests/cassettes/test_login_email_password_fail.yaml
+-rw-r--r--   0        0        0    91847 2023-07-23 13:50:32.012417 garth-0.2.1/tests/cassettes/test_login_success.yaml
+-rw-r--r--   0        0        0     2270 2023-07-23 13:09:36.525519 garth-0.2.1/tests/cassettes/test_refresh.yaml
+-rw-r--r--   0        0        0     2963 2023-07-23 13:36:21.976543 garth-0.2.1/tests/cassettes/test_refresh_expired.yaml
+-rw-r--r--   0        0        0     2940 2023-07-23 16:06:33.706957 garth-0.2.1/tests/conftest.py
+-rw-r--r--   0        0        0     1808 2023-07-23 13:40:52.098938 garth-0.2.1/tests/test_auth_token.py
+-rw-r--r--   0        0        0     4314 2023-07-23 16:06:33.707155 garth-0.2.1/tests/test_http.py
+-rw-r--r--   0        0        0     2570 2023-07-23 13:18:13.595293 garth-0.2.1/tests/test_sso.py
+-rw-r--r--   0        0        0     3955 1970-01-01 00:00:00.000000 garth-0.2.1/PKG-INFO
```

### Comparing `garth-0.2.0/LICENSE` & `garth-0.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/README.md` & `garth-0.2.1/README.md`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/garth/auth_token.py` & `garth-0.2.1/garth/auth_token.py`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/garth/http.py` & `garth-0.2.1/garth/http.py`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/garth/sso.py` & `garth-0.2.1/garth/sso.py`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/pyproject.toml` & `garth-0.2.1/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,31 +1,27 @@
 [project]
 name = "garth"
-version = "0.2.0"
+dynamic = []
 description = "Garmin SSO auth + Connect client"
 authors = [
     { name = "Matin Tamizi", email = "mtamizi@duck.com" },
 ]
 dependencies = [
     "requests>=2.27.0",
 ]
 requires-python = ">=3.10"
 readme = "README.md"
+version = "0.2.1"
 
 [project.license]
 text = "MIT"
 
-[build-system]
-requires = [
-    "pdm-backend",
-]
-build-backend = "pdm.backend"
-
-[tool.pytest.ini_options]
-addopts = "--ignore=__pypackages__ --ignore=tests/cassettes"
+[tool.pdm.version]
+source = "file"
+path = "garth/__init__.py"
 
 [tool.pdm.dev-dependencies]
 dev = [
     "ipython",
     "ipdb",
     "ipykernel",
     "pandas",
@@ -39,7 +35,16 @@
     "types-requests",
 ]
 testing = [
     "coverage",
     "pytest",
     "pytest-vcr>=1.0.2",
 ]
+
+[tool.pytest.ini_options]
+addopts = "--ignore=__pypackages__ --ignore=tests/cassettes"
+
+[build-system]
+requires = [
+    "pdm-backend",
+]
+build-backend = "pdm.backend"
```

### Comparing `garth-0.2.0/tests/cassettes/test_client_get.yaml` & `garth-0.2.1/tests/cassettes/test_client_get.yaml`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/cassettes/test_client_post.yaml` & `garth-0.2.1/tests/cassettes/test_client_post.yaml`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/cassettes/test_client_request.yaml` & `garth-0.2.1/tests/cassettes/test_client_request.yaml`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/cassettes/test_connectapi.yaml` & `garth-0.2.1/tests/cassettes/test_connectapi.yaml`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/cassettes/test_connectapi_refresh.yaml` & `garth-0.2.1/tests/cassettes/test_connectapi_refresh.yaml`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/cassettes/test_exchange.yaml` & `garth-0.2.1/tests/cassettes/test_exchange.yaml`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/cassettes/test_get_username.yaml` & `garth-0.2.1/tests/cassettes/test_get_username.yaml`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/cassettes/test_login_email_password_fail.yaml` & `garth-0.2.1/tests/cassettes/test_login_email_password_fail.yaml`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/cassettes/test_login_success.yaml` & `garth-0.2.1/tests/cassettes/test_login_success.yaml`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/cassettes/test_refresh.yaml` & `garth-0.2.1/tests/cassettes/test_refresh.yaml`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/cassettes/test_refresh_expired.yaml` & `garth-0.2.1/tests/cassettes/test_refresh_expired.yaml`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/conftest.py` & `garth-0.2.1/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/test_auth_token.py` & `garth-0.2.1/tests/test_auth_token.py`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/test_http.py` & `garth-0.2.1/tests/test_http.py`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/tests/test_sso.py` & `garth-0.2.1/tests/test_sso.py`

 * *Files identical despite different names*

### Comparing `garth-0.2.0/PKG-INFO` & `garth-0.2.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: garth
-Version: 0.2.0
+Version: 0.2.1
 Summary: Garmin SSO auth + Connect client
 Author-Email: Matin Tamizi <mtamizi@duck.com>
 License: MIT
 Requires-Python: >=3.10
 Requires-Dist: requests>=2.27.0
 Description-Content-Type: text/markdown
```

