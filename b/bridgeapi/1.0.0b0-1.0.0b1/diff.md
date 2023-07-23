# Comparing `tmp/bridgeapi-1.0.0b0.tar.gz` & `tmp/bridgeapi-1.0.0b1.tar.gz`

## Comparing `bridgeapi-1.0.0b0.tar` & `bridgeapi-1.0.0b1.tar`

### file list

```diff
@@ -1,11 +1,13 @@
--rw-r--r--   0        0        0      133 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b0/src/bridgeapi/__about__.py
--rw-r--r--   0        0        0      227 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b0/src/bridgeapi/__init__.py
--rw-r--r--   0        0        0    19018 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b0/src/bridgeapi/client.py
--rw-r--r--   0        0        0     1237 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b0/src/bridgeapi/client_base.py
--rw-r--r--   0        0        0     1261 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b0/src/bridgeapi/exceptions.py
--rw-r--r--   0        0        0     9351 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b0/src/bridgeapi/models.py
--rw-r--r--   0        0        0      109 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b0/tests/__init__.py
--rw-r--r--   0        0        0     1101 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b0/LICENSE.txt
--rw-r--r--   0        0        0      485 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b0/README.md
--rw-r--r--   0        0        0     3173 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b0/pyproject.toml
--rw-r--r--   0        0        0     1486 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b0/PKG-INFO
+-rw-r--r--   0        0        0      133 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/src/bridgeapi/__about__.py
+-rw-r--r--   0        0        0      227 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/src/bridgeapi/__init__.py
+-rw-r--r--   0        0        0     1237 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/src/bridgeapi/base_client.py
+-rw-r--r--   0        0        0    16352 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/src/bridgeapi/client.py
+-rw-r--r--   0        0        0     1261 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/src/bridgeapi/exceptions.py
+-rw-r--r--   0        0        0     8186 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/src/bridgeapi/models.py
+-rw-r--r--   0        0        0      109 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/tests/__init__.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/tests/test_base_client.py
+-rw-r--r--   0        0        0     3158 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/.gitignore
+-rw-r--r--   0        0        0     1101 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/LICENSE.txt
+-rw-r--r--   0        0        0     4778 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/README.md
+-rw-r--r--   0        0        0     3089 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/pyproject.toml
+-rw-r--r--   0        0        0     5632 2020-02-02 00:00:00.000000 bridgeapi-1.0.0b1/PKG-INFO
```

### Comparing `bridgeapi-1.0.0b0/src/bridgeapi/client.py` & `bridgeapi-1.0.0b1/src/bridgeapi/client.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,33 +1,8 @@
 """Clients for the Bridge API (https://bridgeapi.io).
-
-API endpoints are split between two clients:
-* `AppClient` handles all application-scoped endpoints, that don't depend on a user
-  being authenticated. It only needs (client_id, client_secret) credentials to
-  communicate with the API.
-* `UserClient` handles user-scoped endpoints, those that are specific to a user and
-  require an access token and the `Authorization` header to communicate with the API.
-  It needs (user_email, user_password) credentials, in addition to the same client
-  credentials as `AppClient`.
-
-Examples:
-    ```python
-    from bridgeapi import AppClient, UserClient
-
-    app_client = AppClient("CLIENT_ID", "CLIENT_SECRET")
-    print(app_client.list_banks())
-    print(app_client.list_users())
-    print(app_client.create_user("john@doe.com", "password"))
-
-    user_client = UserClient("CLIENT_ID", "CLIENT_SECRET", "john@doe.com", "password")
-    print(user_client.list_items())
-    print(user_client.connect_item())
-    print(user_client.list_accounts())
-    print(user_client.list_transactions())
-    ```
 """
 
 # TODO (20230719):
 # * Handle return code of endpoints (200, 202, 204)
 # * Check presence of language header
 # * Add doc and links to Bridge API doc
 # * Sections left to implement:
@@ -38,15 +13,15 @@
 #   * Account check: user-scoped
 #   * Subscriptions: user-scoped, requires sales team activation
 
 import datetime as dt
 
 import requests
 
-from bridgeapi.client_base import ClientBase
+from bridgeapi.base_client import BaseClient
 from bridgeapi.exceptions import UserAuthenticationError
 from bridgeapi.models import (
     Account,
     Bank,
     BankCapability,
     BridgeConnectUrl,
     Category,
@@ -58,15 +33,22 @@
     Transaction,
     User,
     UserAuthInfo,
     UserEmailValidation,
 )
 
 
-class AppClient(ClientBase):
+class AppClient(BaseClient):
+    """Bridge API client for application-scoped endpoints (not linked to a user context).
+
+    Args:
+        client_id (str): Client ID from application credentials.
+        client_secret (str): Client secret from application credentials.
+    """
+
     # Banks endpoints
     def list_banks(
         self,
         countries: str | list[str] | None = None,
         capabilities: BankCapability | list[BankCapability] | None = None,
         after: str | None = None,
         limit: int | None = None,
@@ -149,76 +131,17 @@
 
     def get_category(self, category_id: int, language: str | None = None) -> Category:
         headers = {"Accept-Language": language}
         response = self._request("GET", f"categories/{category_id}", headers=headers)
         return Category.from_response(response)
 
 
-class UserClient(ClientBase):
+class UserClient(BaseClient):
     """Bridge API client for user-scoped endpoints.
 
-    The simplest usage is to let `UserClient` handle all the authorization lifecyle. It
-    will automatically obtain an access token and renew it when it expires (after 2
-    hours):
-
-    ```python
-    user_client = UserClient("CLIENT_ID", "CLIENT_SECRET", "john@doe.com", "password")
-    print(user_client.list_items())  # OK
-
-    # 2+ hours later
-    print(user_client.list_items())  # OK
-    ```
-
-    If you wish to manage the user authorization lifecycle yourself, pass
-    `auto_renew=False` at creation. You will need to call `.renew_auth()` manually:
-
-    ```python
-    user_client = UserClient(
-        "CLIENT_ID", "CLIENT_SECRET", "john@doe.com", "password", auto_renew=False
-    )
-    print(user_client.is_authenticated())  # False
-    user_client.list_items()  # UserAuthenticationError
-
-    user_client.renew_auth()
-    print(user_client.is_authenticated())  # True
-    print(user_client.list_items())  # OK
-
-    # 2+ hours later
-    print(user_client.is_authenticated())  # False
-    user_client.renew_auth()
-    print(user_client.is_authenticated())  # True
-    ```
-
-    Additionally, if you are managing user tokens externally and persisting them to
-    external storage, you can provide them at creation as well:
-
-    ```python
-    user_client = UserClient(
-        "CLIENT_ID",
-        "CLIENT_SECRET",
-        "john@doe.com",
-        "password",
-        user_uuid="uuid",
-        access_token="token",
-        expires_at="yyyy-mm-dd HH:MM:SS",
-        auto_renew=False,
-    )
-    print(user_client.is_authenticated())  # True
-    user_client.list_items()  # OK
-
-    # Generate and store new authorization info
-    auth_info = user_client.renew_auth()
-    store_user_auth_to_db(
-        user_email=auth_info.user.email,
-        user_uuid=auth_info.user.uuid,
-        access_token=auth_info.access_token,
-        expires_at=auth_info.expires_at,
-    )
-    ```
-
     Args:
         client_id (str): Client ID from application credentials.
         client_secret (str): Client secret from application credentials.
         user_email (str): User email from user credentials.
         user_password (str): User password from user credentials.
         user_uuid (str or None, default None): User UUID, if managing auth tokens
             externally.
```

### Comparing `bridgeapi-1.0.0b0/src/bridgeapi/client_base.py` & `bridgeapi-1.0.0b1/src/bridgeapi/base_client.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from urllib.parse import urljoin
 
 import requests
 
 from bridgeapi.exceptions import RequestError
 
 
-class ClientBase:
+class BaseClient:
     base_url = "https://api.bridgeapi.io/v2/"
     api_version = "2021-06-01"
 
     def __init__(self, client_id: str, client_secret: str):
         self.client_id = client_id
         self.client_secret = client_secret
         self.session = requests.Session()
```

### Comparing `bridgeapi-1.0.0b0/src/bridgeapi/exceptions.py` & `bridgeapi-1.0.0b1/src/bridgeapi/exceptions.py`

 * *Files identical despite different names*

### Comparing `bridgeapi-1.0.0b0/src/bridgeapi/models.py` & `bridgeapi-1.0.0b1/src/bridgeapi/models.py`

 * *Files 17% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 from typing import Generic, Literal, TypeVar
 from uuid import UUID
 
 import requests
 from pydantic import BaseModel, HttpUrl, PrivateAttr, constr
 from pydantic.generics import GenericModel
 
-from bridgeapi.client_base import ClientBase
+from bridgeapi.base_client import BaseClient
 from bridgeapi.exceptions import PaginationError
 
 BaseModelT = TypeVar("BaseModelT", bound="BridgeBaseModel")
 
 
 class BridgeBaseModel(BaseModel):
     """Base model for all API resources. Allows storing the API response object along
@@ -40,57 +40,25 @@
 
 
 class Pagination(BaseModel):
     next_uri: str | None = None
 
 
 class PaginatedResult(BridgeBaseModel, GenericModel, Generic[_T]):
-    """Container storing results of a paginated API call.
-
-    When calling a list API endpoint, the first page of results is returned. Existence
-    of more pages can be checked with `.has_more()`. Subsequent pages can be retrieved
-    by calling `.next_page()`:
-
-    ```python
-    from bridgeapi import AppClient
-
-    app_client = AppClient("CLIENT_ID", "CLIENT_SECRET")
-    banks = app_client.list_banks(limit=2)
-    print(banks.resources)  # List of 2 Bank instances
-
-    print(banks.has_more())  # True
-    banks = banks.next_page()
-    print(banks.resources)  # List of 2 other Bank instances
-    ```
-
-    The entire list of objects can be retrieved by calling `.fetch_all()` on the first
-    page returned by the API. Attempting to call it on a subsequent page will result
-    in an error. Beware of potentially large collections, you may exceed API or memory
-    limits, or wait for a long time. You may want to increase the `limit` parameter.
-
-    ```python
-    from bridgeapi import AppClient
-
-    app_client = AppClient("CLIENT_ID", "CLIENT_SECRET")
-    banks = app_client.list_banks(limit=100)
-    print(banks.fetch_all())  # List of all banks
-
-    banks.next_page().fetch_all()  # PaginationError
-    ```
-    """
+    """Container storing results of a paginated API call."""
 
     resources: list[_T]
     pagination: Pagination
 
-    _client: "ClientBase" = PrivateAttr()
+    _client: "BaseClient" = PrivateAttr()
     _page_number: int = PrivateAttr()
 
     @classmethod
     def from_response(
-        cls, response: requests.Response, client: "ClientBase", page_number: int = 0
+        cls, response: requests.Response, client: "BaseClient", page_number: int = 0
     ) -> "PaginatedResult[_T]":
         result = cls.parse_obj(response.json())
         result._response = response
         result._client = client
         result._page_number = page_number
         return result
```

### Comparing `bridgeapi-1.0.0b0/LICENSE.txt` & `bridgeapi-1.0.0b1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `bridgeapi-1.0.0b0/pyproject.toml` & `bridgeapi-1.0.0b1/pyproject.toml`

 * *Files 9% similar despite different names*

```diff
@@ -3,37 +3,34 @@
 build-backend = "hatchling.build"
 
 [project]
 name = "bridgeapi"
 dynamic = ["version"]
 description = 'Client for the Bridge open banking API aggregator'
 readme = "README.md"
-requires-python = ">=3.7"
+requires-python = ">=3.10"  # Not before 3.10 because we use new the union types syntax
 license = "MIT"
 keywords = []
 authors = [
-  { name = "Alexandre Marty", email = "alexandre@marty.in" },
+  { name = "Alexandre Marty", email = "contact@marty.in" },
 ]
 classifiers = [
   "Development Status :: 4 - Beta",
   "Programming Language :: Python",
-  "Programming Language :: Python :: 3.7",
-  "Programming Language :: Python :: 3.8",
-  "Programming Language :: Python :: 3.9",
   "Programming Language :: Python :: 3.10",
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = ["pydantic", "requests"]
 
 [project.urls]
-Documentation = "https://github.com/unknown/bridgeapi#readme"
-Issues = "https://github.com/unknown/bridgeapi/issues"
-Source = "https://github.com/unknown/bridgeapi"
+Documentation = "https://gitlab.com/alex-marty/bridgeapi"
+Issues = "https://gitlab.com/alex-marty/bridgeapi/-/issues"
+Source = "https://gitlab.com/alex-marty/bridgeapi"
 
 [tool.hatch.version]
 path = "src/bridgeapi/__about__.py"
 
 [tool.hatch.envs.default]
 dependencies = [
   "coverage[toml]>=6.5",
@@ -48,15 +45,15 @@
 ]
 cov = [
   "test-cov",
   "cov-report",
 ]
 
 [[tool.hatch.envs.all.matrix]]
-python = ["3.7", "3.8", "3.9", "3.10", "3.11"]
+python = ["3.10", "3.11"]
 
 [tool.hatch.envs.lint]
 detached = true
 dependencies = [
   "black>=23.1.0",
   "mypy>=1.0.0",
   "ruff>=0.0.243",
@@ -74,20 +71,20 @@
 ]
 all = [
   "style",
   "typing",
 ]
 
 [tool.black]
-target-version = ["py37"]
+target-version = ["py310"]
 line-length = 99
 skip-string-normalization = true
 
 [tool.ruff]
-target-version = "py37"
+target-version = "py310"
 line-length = 99
 select = [
   "A",
   "ARG",
   "B",
   "C",
   "DTZ",
```

