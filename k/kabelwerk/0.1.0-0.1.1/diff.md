# Comparing `tmp/kabelwerk-0.1.0.tar.gz` & `tmp/kabelwerk-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "kabelwerk-0.1.0.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
+gzip compressed data, was "kabelwerk-0.1.1.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
```

## Comparing `kabelwerk-0.1.0.tar` & `kabelwerk-0.1.1.tar`

### file list

```diff
@@ -1,21 +1,31 @@
--rw-r--r--   0        0        0      187 2023-07-13 14:00:56.236623 kabelwerk-0.1.0/.editorconfig
--rw-r--r--   0        0        0      472 2023-07-15 09:30:53.594820 kabelwerk-0.1.0/.github/workflows/test.yml
--rw-r--r--   0        0        0      113 2023-07-13 14:00:56.236623 kabelwerk-0.1.0/.gitignore
--rw-r--r--   0        0        0       83 2023-07-21 15:48:58.848214 kabelwerk-0.1.0/CHANGELOG.rst
--rw-r--r--   0        0        0     1072 2023-07-13 14:00:56.239956 kabelwerk-0.1.0/LICENSE
--rw-r--r--   0        0        0      843 2023-07-21 15:34:58.021931 kabelwerk-0.1.0/README.rst
--rw-r--r--   0        0        0       50 2023-07-20 07:39:51.527036 kabelwerk-0.1.0/kabelwerk/__init__.py
--rw-r--r--   0        0        0       57 2023-07-21 14:47:24.896651 kabelwerk-0.1.0/kabelwerk/api/__init__.py
--rw-r--r--   0        0        0     2391 2023-07-21 13:46:04.812348 kabelwerk-0.1.0/kabelwerk/api/base.py
--rw-r--r--   0        0        0     2699 2023-07-21 14:49:23.393246 kabelwerk-0.1.0/kabelwerk/api/users.py
--rw-r--r--   0        0        0     1626 2023-07-16 20:40:29.644485 kabelwerk-0.1.0/kabelwerk/config.py
--rw-r--r--   0        0        0      733 2023-07-21 08:51:27.770123 kabelwerk-0.1.0/kabelwerk/exceptions.py
--rw-r--r--   0        0        0      602 2023-07-14 12:03:21.165089 kabelwerk-0.1.0/kabelwerk/models.py
--rw-r--r--   0        0        0     1017 2023-07-16 20:42:14.194297 kabelwerk-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     1126 2023-07-16 20:42:18.034291 kabelwerk-0.1.0/requirements.txt
--rw-r--r--   0        0        0        0 2023-07-13 14:22:39.007708 kabelwerk-0.1.0/tests/__init__.py
--rw-r--r--   0        0        0     1111 2023-07-21 11:34:10.039224 kabelwerk-0.1.0/tests/conftest.py
--rw-r--r--   0        0        0     4960 2023-07-21 14:42:07.253569 kabelwerk-0.1.0/tests/test_api_base.py
--rw-r--r--   0        0        0     1684 2023-07-21 14:53:31.346771 kabelwerk-0.1.0/tests/test_api_users.py
--rw-r--r--   0        0        0     1381 2023-07-14 11:35:23.390480 kabelwerk-0.1.0/tests/test_config.py
--rw-r--r--   0        0        0     1786 1970-01-01 00:00:00.000000 kabelwerk-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0      187 2023-07-13 14:00:56.236623 kabelwerk-0.1.1/.editorconfig
+-rw-r--r--   0        0        0      472 2023-07-15 09:30:53.594820 kabelwerk-0.1.1/.github/workflows/test.yml
+-rw-r--r--   0        0        0      134 2023-07-23 12:42:55.108656 kabelwerk-0.1.1/.gitignore
+-rw-r--r--   0        0        0      149 2023-07-23 20:55:42.179252 kabelwerk-0.1.1/CHANGELOG.rst
+-rw-r--r--   0        0        0     1072 2023-07-13 14:00:56.239956 kabelwerk-0.1.1/LICENSE
+-rw-r--r--   0        0        0     1036 2023-07-23 20:50:10.989784 kabelwerk-0.1.1/README.rst
+-rw-r--r--   0        0        0      634 2023-07-23 12:42:55.108656 kabelwerk-0.1.1/docs/Makefile
+-rw-r--r--   0        0        0      299 2023-07-23 14:56:54.527546 kabelwerk-0.1.1/docs/api.rst
+-rw-r--r--   0        0        0     1216 2023-07-23 20:53:42.252784 kabelwerk-0.1.1/docs/conf.py
+-rw-r--r--   0        0        0      306 2023-07-23 20:35:56.200589 kabelwerk-0.1.1/docs/exceptions.rst
+-rw-r--r--   0        0        0     1331 2023-07-23 20:42:37.613704 kabelwerk-0.1.1/docs/index.rst
+-rw-r--r--   0        0        0      800 2023-07-23 12:42:55.108656 kabelwerk-0.1.1/docs/make.bat
+-rw-r--r--   0        0        0       50 2023-07-23 20:54:13.906066 kabelwerk-0.1.1/kabelwerk/__init__.py
+-rw-r--r--   0        0        0      102 2023-07-22 13:08:12.181267 kabelwerk-0.1.1/kabelwerk/api/__init__.py
+-rw-r--r--   0        0        0     2651 2023-07-21 20:37:55.586826 kabelwerk-0.1.1/kabelwerk/api/base.py
+-rw-r--r--   0        0        0     4757 2023-07-23 20:33:18.317197 kabelwerk-0.1.1/kabelwerk/api/rooms.py
+-rw-r--r--   0        0        0     3367 2023-07-23 20:18:56.435431 kabelwerk-0.1.1/kabelwerk/api/users.py
+-rw-r--r--   0        0        0      763 2023-07-22 12:19:54.267414 kabelwerk-0.1.1/kabelwerk/apps.py
+-rw-r--r--   0        0        0     1698 2023-07-22 09:14:56.731801 kabelwerk-0.1.1/kabelwerk/config.py
+-rw-r--r--   0        0        0     1829 2023-07-23 20:41:35.823762 kabelwerk-0.1.1/kabelwerk/exceptions.py
+-rw-r--r--   0        0        0     1357 2023-07-22 12:57:58.879143 kabelwerk-0.1.1/kabelwerk/models.py
+-rw-r--r--   0        0        0      356 2023-07-22 10:35:31.408380 kabelwerk-0.1.1/kabelwerk/utils.py
+-rw-r--r--   0        0        0     1108 2023-07-23 20:57:18.152422 kabelwerk-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0     1956 2023-07-23 12:42:55.108656 kabelwerk-0.1.1/requirements.txt
+-rw-r--r--   0        0        0        0 2023-07-13 14:22:39.007708 kabelwerk-0.1.1/tests/__init__.py
+-rw-r--r--   0        0        0     1111 2023-07-21 20:25:10.958309 kabelwerk-0.1.1/tests/conftest.py
+-rw-r--r--   0        0        0     5834 2023-07-21 20:46:17.235233 kabelwerk-0.1.1/tests/test_api_base.py
+-rw-r--r--   0        0        0     5842 2023-07-23 14:35:28.424661 kabelwerk-0.1.1/tests/test_api_rooms.py
+-rw-r--r--   0        0        0     1786 2023-07-22 09:51:40.321601 kabelwerk-0.1.1/tests/test_api_users.py
+-rw-r--r--   0        0        0     1381 2023-07-14 11:35:23.390480 kabelwerk-0.1.1/tests/test_config.py
+-rw-r--r--   0        0        0     2130 1970-01-01 00:00:00.000000 kabelwerk-0.1.1/PKG-INFO
```

### Comparing `kabelwerk-0.1.0/LICENSE` & `kabelwerk-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `kabelwerk-0.1.0/README.rst` & `kabelwerk-0.1.1/README.rst`

 * *Files 17% similar despite different names*

```diff
@@ -14,14 +14,21 @@
     # usually inside a virtual environment
     pip install kabelwerk
 
 Releases follow semantic versioning. Make sure to check the `CHANGELOG.rst`_
 whenever upgrading to a newer version.
 
 
+Documentation
+=============
+
+Documentation — including API reference and code examples — can be found at
+`docs.kabelwerk.io`_.
+
+
 Licence
 =======
 
 Licensed under the `MIT`_ licence.
 
 
 .. |logo| image:: https://kabelwerk.io/images/logo_256.png
@@ -29,8 +36,10 @@
 
 .. |Kabelwerk| replace:: **Kabelwerk**
 .. _Kabelwerk: https://kabelwerk.io
 
 .. _`Cheese Shop`: https://pypi.org/project/kabelwerk/
 .. _`CHANGELOG.rst`: https://github.com/kabelwerk/sdk-python/blob/master/CHANGELOG.rst
 
+.. _`docs.kabelwerk.io`: https://docs.kabelwerk.io/python/
+
 .. _`MIT`: https://github.com/kabelwerk/sdk-python/blob/master/LICENSE
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `kabelwerk-0.1.0/kabelwerk/api/base.py` & `kabelwerk-0.1.1/kabelwerk/api/base.py`

 * *Files 12% similar despite different names*

```diff
@@ -50,15 +50,15 @@
             json=params,
             timeout=timeout,
         )
 
     except requests.RequestException as error:
         logger.error(f'{log} → {error!s}', exc_info=error)
 
-        raise ConnectionError from error
+        raise ConnectionError(error)
 
     if response.status_code in [200, 201]:
         payload = response.json()
 
         logger.info((
             f'{log} → {response.status_code} {response.reason} {payload!r}'
         ))
@@ -73,18 +73,24 @@
     elif response.status_code == 400:
         payload = response.json()
 
         logger.warning((
             f'{log} → {response.status_code} {response.reason} {payload!r}'
         ))
 
-        raise ValidationError
+        try:
+            field = sorted(payload['errors'].keys())[0]
+            error_message = payload['errors'][field][0]
+        except (IndexError, KeyError):
+            raise ServerError(response)
 
-    elif response.status_code == 401:
+        raise ValidationError(response, field, error_message)
+
+    elif response.status_code in [401, 403]:
         logger.error(f'{log} → {response.status_code} {response.reason}')
 
-        raise AuthenticationError
+        raise AuthenticationError(response)
 
     else:
         logger.error(f'{log} → {response.status_code} {response.reason}')
 
-        raise ServerError
+        raise ServerError(response)
```

### Comparing `kabelwerk-0.1.0/kabelwerk/api/users.py` & `kabelwerk-0.1.1/kabelwerk/api/users.py`

 * *Files 27% similar despite different names*

```diff
@@ -2,30 +2,58 @@
 from kabelwerk.models import User
 
 
 def create_user(*, key, name, hub=None):
     """
     Create a user with the given key and name.
 
-    Return a named tuple with info about the newly created user if the backend
-    accepts the request.
+    All arguments are named arguments.
 
-    Raise a ValidationError if the request is rejected because of invalid
-    input.
 
-    Raise an AuthenticationError if the request is rejected because the
-    authentication token is invalid.
+    Arguments
+    ---------
 
-    Raise a ConnectionError if there is a problem connecting to the Kabelwerk
-    backend or if the request times out.
+    key
+        Your unique ID for this user.
 
-    Raise a ServerError if the Kabelwerk backend fails to handle the request or
-    behaves in an unexpected way.
+    name
+        The user's name.
 
-    All arguments are named arguments.
+    hub
+        The slug identifying the hub in which to create the user. Only set this
+        if you want to create a hub user.
+
+
+    Returns
+    -------
+
+    typing.NamedTuple
+        Info about the newly created user if the backend accepts the request.
+
+
+    Raises
+    ------
+
+    ValidationError
+        If the request is rejected because of invalid input.
+
+    AuthenticationError
+        If the request is rejected because the authentication token is invalid.
+
+    ConnectionError
+        If there is a problem connecting to the Kabelwerk backend or if the
+        request times out.
+
+    ServerError
+        If the Kabelwerk backend fails to handle the request or behaves in an
+        unexpected way.
+
+
+    Examples
+    --------
 
     >>> create_user(key='kusanagi', name='Motoko')
     User(id=42, key='kusanagi', name='Motoko')
 
     >>> create_user(name='Name Only')
     ValidationError
 
@@ -43,30 +71,54 @@
     )
 
 
 def update_user(*, key, name):
     """
     Update the user with the given key.
 
-    Return a named tuple with info about the updated user if the backend
-    accepts the request.
+    All arguments are named arguments.
+
 
-    Raise a ValidationError if the request is rejected because of invalid
-    input.
+    Arguments
+    ---------
 
-    Raise an AuthenticationError if the request is rejected because the
-    authentication token is invalid.
+    key
+        Your unique ID for this user.
 
-    Raise a ConnectionError if there is a problem connecting to the Kabelwerk
-    backend or if the request times out.
+    name
+        The user's name.
 
-    Raise a ServerError if the Kabelwerk backend fails to handle the request or
-    behaves in an unexpected way.
 
-    All arguments are named arguments.
+    Returns
+    -------
+
+    typing.NamedTuple
+        Info about the updated user if the backend accepts the request.
+
+
+    Raises
+    ------
+
+    ValidationError
+        If the request is rejected because of invalid input.
+
+    AuthenticationError
+        If the request is rejected because the authentication token is invalid.
+
+    ConnectionError
+        If there is a problem connecting to the Kabelwerk backend or if the
+        request times out.
+
+    ServerError
+        If the Kabelwerk backend fails to handle the request or behaves in an
+        unexpected way.
+
+
+    Examples
+    --------
 
     >>> update_user(key='kusanagi', name='Motoko')
     User(id=42, key='kusanagi', name='Motoko')
 
     >>> update_user(key='kusanagi', name='')
     ValidationError
 
@@ -82,23 +134,45 @@
     )
 
 
 def delete_user(*, key):
     """
     Delete the user with the given key.
 
-    Raise an AuthenticationError if the request is rejected because the
-    authentication token is invalid.
+    All arguments are named arguments.
 
-    Raise a ConnectionError if there is a problem connecting to the Kabelwerk
-    backend or if the request times out.
 
-    Raise a ServerError if the Kabelwerk backend fails to handle the request or
-    behaves in an unexpected way.
+    Arguments
+    ---------
 
-    All arguments are named arguments.
+    key
+        Your unique ID for this user.
+
+    Returns
+    -------
+
+    None
+
+
+    Raises
+    ------
+
+    AuthenticationError
+        If the request is rejected because the authentication token is invalid.
+
+    ConnectionError
+        If there is a problem connecting to the Kabelwerk backend or if the
+        request times out.
+
+    ServerError
+        If the Kabelwerk backend fails to handle the request or behaves in an
+        unexpected way.
+
+
+    Examples
+    --------
 
     >>> delete_user(key='kusanagi')
     None
 
     """
     make_api_call('DELETE', f'/users/{key}')
```

### Comparing `kabelwerk-0.1.0/kabelwerk/config.py` & `kabelwerk-0.1.1/kabelwerk/config.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,19 +1,20 @@
+import os
 import re
 
 
 """
 The URL of the Kabelwerk backend to connect to.
 """
-KABELWERK_URL = 'hubdemo.kabelwerk.io'
+KABELWERK_URL = os.getenv('KABELWERK_URL', 'hubdemo.kabelwerk.io')
 
 """
 The API token to authenticate the requests to the Kabelwerk API with.
 """
-KABELWERK_API_TOKEN = ''
+KABELWERK_API_TOKEN = os.getenv('KABELWERK_API_TOKEN', '')
 
 
 # the compiled regex used to parse KABELWERK_URL
 _url_regex = re.compile(
     r'^(?P<scheme>(ws|http)s?:\/\/)?(?P<host>[0-9a-z.:-]+)\/?(?P<path>[a-z\/]+)?$',
     flags=re.IGNORECASE,
 )
```

### Comparing `kabelwerk-0.1.0/pyproject.toml` & `kabelwerk-0.1.1/pyproject.toml`

 * *Files 15% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 authors = [
     {name = "Kabelwerk", email = "devs@kabelwerk.io"},
 ]
 
 license = {file = "LICENSE"}
 
 classifiers = [
-    "Development Status :: 1 - Planning",
+    "Development Status :: 2 - Pre-Alpha",
     "Intended Audience :: Developers",
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python :: 3",
     "Topic :: Communications :: Chat",
     "Topic :: Internet :: WWW/HTTP",
 ]
 keywords = ["kabelwerk"]
@@ -32,17 +32,20 @@
 
 [project.optional-dependencies]
 dev = [
     "flit",
     "pip-tools",
     "pytest",
     "responses",
+    "sphinx",
+    "sphinx_rtd_theme",
 ]
 
 [project.urls]
 Home = "https://kabelwerk.io"
 Changelog = "https://github.com/kabelwerk/sdk-python/blob/master/CHANGELOG.rst"
+Documentation = "https://docs.kabelwerk.io/python/"
 Source = "https://github.com/kabelwerk/sdk-python"
 Tracker = "https://github.com/kabelwerk/sdk-python/issues"
 
 [tool.pip-tools]
 all_extras = true
```

### Comparing `kabelwerk-0.1.0/tests/conftest.py` & `kabelwerk-0.1.1/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `kabelwerk-0.1.0/tests/test_api_users.py` & `kabelwerk-0.1.1/tests/test_api_users.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from responses.matchers import json_params_matcher
 
 from kabelwerk.api import create_user, delete_user, update_user
+from kabelwerk.models import User
 
 
 def test_create_user_works(mock_api, mock_response):
     """
     The create_user function should return a User named tuple if the endpoint
     accepts the request.
     """
@@ -19,14 +20,15 @@
     assert len(mock_api.calls) == 1
     assert json_params_matcher({
         'hub': None,
         'key': 'kusanagi',
         'name': 'Motoko',
     })(mock_api.calls[0].request)
 
+    assert isinstance(user, User)
     assert user.id == 2
     assert user.key == 'kusanagi'
     assert user.name == 'Motoko'
 
 
 def test_update_user_works(mock_api, mock_response):
     """
@@ -42,14 +44,15 @@
     user = update_user(key='kusanagi', name='Motoko')
 
     assert len(mock_api.calls) == 1
     assert json_params_matcher({
         'name': 'Motoko',
     })(mock_api.calls[0].request)
 
+    assert isinstance(user, User)
     assert user.id == 2
     assert user.key == 'kusanagi'
     assert user.name == 'Motoko'
 
 
 def test_delete_user_works(mock_api, mock_response):
     """
```

### Comparing `kabelwerk-0.1.0/tests/test_config.py` & `kabelwerk-0.1.1/tests/test_config.py`

 * *Files identical despite different names*

### Comparing `kabelwerk-0.1.0/PKG-INFO` & `kabelwerk-0.1.1/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,26 +1,29 @@
 Metadata-Version: 2.1
 Name: kabelwerk
-Version: 0.1.0
+Version: 0.1.1
 Summary: The Kabelwerk SDK for Python.
 Keywords: kabelwerk
 Author-email: Kabelwerk <devs@kabelwerk.io>
 Description-Content-Type: text/x-rst
-Classifier: Development Status :: 1 - Planning
+Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Topic :: Communications :: Chat
 Classifier: Topic :: Internet :: WWW/HTTP
 Requires-Dist: requests >= 2.31
 Requires-Dist: flit ; extra == "dev"
 Requires-Dist: pip-tools ; extra == "dev"
 Requires-Dist: pytest ; extra == "dev"
 Requires-Dist: responses ; extra == "dev"
+Requires-Dist: sphinx ; extra == "dev"
+Requires-Dist: sphinx_rtd_theme ; extra == "dev"
 Project-URL: Changelog, https://github.com/kabelwerk/sdk-python/blob/master/CHANGELOG.rst
+Project-URL: Documentation, https://docs.kabelwerk.io/python/
 Project-URL: Home, https://kabelwerk.io
 Project-URL: Source, https://github.com/kabelwerk/sdk-python
 Project-URL: Tracker, https://github.com/kabelwerk/sdk-python/issues
 Provides-Extra: dev
 
 |logo|_
 
@@ -38,14 +41,21 @@
     # usually inside a virtual environment
     pip install kabelwerk
 
 Releases follow semantic versioning. Make sure to check the `CHANGELOG.rst`_
 whenever upgrading to a newer version.
 
 
+Documentation
+=============
+
+Documentation — including API reference and code examples — can be found at
+`docs.kabelwerk.io`_.
+
+
 Licence
 =======
 
 Licensed under the `MIT`_ licence.
 
 
 .. |logo| image:: https://kabelwerk.io/images/logo_256.png
@@ -53,9 +63,11 @@
 
 .. |Kabelwerk| replace:: **Kabelwerk**
 .. _Kabelwerk: https://kabelwerk.io
 
 .. _`Cheese Shop`: https://pypi.org/project/kabelwerk/
 .. _`CHANGELOG.rst`: https://github.com/kabelwerk/sdk-python/blob/master/CHANGELOG.rst
 
+.. _`docs.kabelwerk.io`: https://docs.kabelwerk.io/python/
+
 .. _`MIT`: https://github.com/kabelwerk/sdk-python/blob/master/LICENSE
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

