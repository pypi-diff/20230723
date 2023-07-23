# Comparing `tmp/reddit_user_to_sqlite-0.4.1.tar.gz` & `tmp/reddit_user_to_sqlite-0.4.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "reddit_user_to_sqlite-0.4.1.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
+gzip compressed data, was "reddit_user_to_sqlite-0.4.2.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
```

## Comparing `reddit_user_to_sqlite-0.4.1.tar` & `reddit_user_to_sqlite-0.4.2.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1071 2023-05-01 03:22:25.344837 reddit_user_to_sqlite-0.4.1/LICENSE
--rw-r--r--   0        0        0     7209 2023-06-15 05:47:17.749668 reddit_user_to_sqlite-0.4.1/README.md
--rw-r--r--   0        0        0     1397 2023-06-25 19:00:21.510210 reddit_user_to_sqlite-0.4.1/pyproject.toml
--rw-r--r--   0        0        0        0 2023-05-01 03:19:48.457234 reddit_user_to_sqlite-0.4.1/reddit_user_to_sqlite/__init__.py
--rw-r--r--   0        0        0     5914 2023-06-19 00:28:14.225335 reddit_user_to_sqlite-0.4.1/reddit_user_to_sqlite/cli.py
--rw-r--r--   0        0        0     1759 2023-06-25 18:59:52.228184 reddit_user_to_sqlite-0.4.1/reddit_user_to_sqlite/csv_helpers.py
--rw-r--r--   0        0        0     1110 2023-06-15 05:44:28.477262 reddit_user_to_sqlite-0.4.1/reddit_user_to_sqlite/helpers.py
--rw-r--r--   0        0        0     4760 2023-06-15 05:44:28.477491 reddit_user_to_sqlite-0.4.1/reddit_user_to_sqlite/reddit_api.py
--rw-r--r--   0        0        0     6222 2023-06-15 05:44:28.477747 reddit_user_to_sqlite-0.4.1/reddit_user_to_sqlite/sqlite_helpers.py
--rw-r--r--   0        0        0     8587 1970-01-01 00:00:00.000000 reddit_user_to_sqlite-0.4.1/PKG-INFO
+-rw-r--r--   0        0        0     1071 2023-05-01 03:22:25.344837 reddit_user_to_sqlite-0.4.2/LICENSE
+-rw-r--r--   0        0        0     7030 2023-06-28 07:05:22.651227 reddit_user_to_sqlite-0.4.2/README.md
+-rw-r--r--   0        0        0     1443 2023-07-23 04:36:17.624804 reddit_user_to_sqlite-0.4.2/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-05-01 03:19:48.457234 reddit_user_to_sqlite-0.4.2/reddit_user_to_sqlite/__init__.py
+-rw-r--r--   0        0        0     5974 2023-07-23 04:30:46.155146 reddit_user_to_sqlite-0.4.2/reddit_user_to_sqlite/cli.py
+-rw-r--r--   0        0        0     1759 2023-06-25 18:59:52.228184 reddit_user_to_sqlite-0.4.2/reddit_user_to_sqlite/csv_helpers.py
+-rw-r--r--   0        0        0     1110 2023-06-15 05:44:28.477262 reddit_user_to_sqlite-0.4.2/reddit_user_to_sqlite/helpers.py
+-rw-r--r--   0        0        0     6633 2023-07-23 04:32:51.799664 reddit_user_to_sqlite-0.4.2/reddit_user_to_sqlite/reddit_api.py
+-rw-r--r--   0        0        0     6190 2023-07-22 06:54:48.272908 reddit_user_to_sqlite-0.4.2/reddit_user_to_sqlite/sqlite_helpers.py
+-rw-r--r--   0        0        0     8408 1970-01-01 00:00:00.000000 reddit_user_to_sqlite-0.4.2/PKG-INFO
```

### Comparing `reddit_user_to_sqlite-0.4.1/LICENSE` & `reddit_user_to_sqlite-0.4.2/LICENSE`

 * *Files identical despite different names*

### Comparing `reddit_user_to_sqlite-0.4.1/README.md` & `reddit_user_to_sqlite-0.4.2/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -56,15 +56,15 @@
 
 Then, add the recommended plugins (for rendering timestamps and markdown):
 
 ```bash
 pipx inject datasette datasette-render-markdown datasette-render-timestamps
 ```
 
-Finally, create a `metadata.json` file with the following:
+Finally, create a `metadata.json` file next to your `reddit.db` with the following:
 
 ```json
 {
   "databases": {
     "reddit": {
       "tables": {
         "comments": {
@@ -172,14 +172,9 @@
 
 In your virtual environment, a simple `pytest` should run the unit test suite. You can also run `pyright` for type checking.
 
 ### Releasing New Versions
 
 > these notes are mostly for myself (or other contributors)
 
-0. ensure tests pass (`tox -p`)
-1. install release tooling (`pip install -e '.[release]'`)
-2. build the package (`python -m build`)
-3. upload the release (`python -m twine upload dist/*`)
-   1. give your username as `__token__`
-   2. give your password as your stored API key
-   3. If you're getting invalid password, verify that `~/.pypirc` is empty
+1. Run `just release` while your venv is active
+2. paste the stored API key (If you're getting invalid password, verify that `~/.pypirc` is empty)
```

### Comparing `reddit_user_to_sqlite-0.4.1/pyproject.toml` & `reddit_user_to_sqlite-0.4.2/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "reddit-user-to-sqlite"
-version = "0.4.1"
+version = "0.4.2"
 
 authors = [{ name = "David Brownman", email = "beamneocube@gmail.com" }]
 description = "Create a SQLite database containing data pulled from Reddit about a single user."
 readme = "README.md"
 license = { file = "LICENSE" }
 
 requires-python = ">=3.9"
@@ -24,15 +24,15 @@
   "requests==2.29.0",
   "tqdm==4.65.0",
 ]
 
 [project.optional-dependencies]
 test = ["pytest==7.3.1", "responses==0.23.1"]
 release = ["twine==4.0.2", "build==0.10.0"]
-ci = ["black==23.3.0", "isort==5.12.0", "pyright==1.1.309"]
+ci = ["black==23.3.0", "pyright==1.1.318", "ruff==0.0.277"]
 
 [project.urls]
 "Homepage" = "https://github.com/xavdid/reddit-user-to-sqlite"
 "Bug Tracker" = "https://github.com/xavdid/reddit-user-to-sqlite/issues"
 "Author" = "https://xavd.id"
 "Changelog" = "https://github.com/xavdid/reddit-user-to-sqlite/blob/main/CHANGELOG.md"
 
@@ -42,9 +42,10 @@
 [build-system]
 requires = ["flit_core>=3.4"]
 build-backend = "flit_core.buildapi"
 
 # needed so the LSP performs typechecking
 [tool.pyright]
 
-[tool.isort]
-profile = "black"
+[tool.ruff]
+select = ["E", "F", "I001"] # defaults & isort
+ignore = ["E501"]
```

### Comparing `reddit_user_to_sqlite-0.4.1/reddit_user_to_sqlite/cli.py` & `reddit_user_to_sqlite-0.4.2/reddit_user_to_sqlite/cli.py`

 * *Files 4% similar despite different names*

```diff
@@ -71,21 +71,21 @@
     """
     if own data is true, requires a username to save. Otherwise, will add a placeholder
     (for external data)
     """
     new_comment_ids = load_unsaved_ids_from_file(
         db, archive_path, "comments", prefix=tables_prefix
     )
-    click.echo("\nFetching info about your comments")
+    click.echo(f"\nFetching info about {'your' if own_data else 'saved'} comments")
     comments = cast(list[Comment], load_info(new_comment_ids))
 
     post_ids = load_unsaved_ids_from_file(
         db, archive_path, "posts", prefix=tables_prefix
     )
-    click.echo("\nFetching info about your posts")
+    click.echo(f"\nFetching info about {'your' if own_data else 'saved'} posts")
     posts = cast(list[Post], load_info(post_ids))
 
     username = None
     user_fullname = None
 
     if own_data:
         # find the username, first from any of the loaded comments/posts
```

### Comparing `reddit_user_to_sqlite-0.4.1/reddit_user_to_sqlite/csv_helpers.py` & `reddit_user_to_sqlite-0.4.2/reddit_user_to_sqlite/csv_helpers.py`

 * *Files identical despite different names*

### Comparing `reddit_user_to_sqlite-0.4.1/reddit_user_to_sqlite/helpers.py` & `reddit_user_to_sqlite-0.4.2/reddit_user_to_sqlite/helpers.py`

 * *Files identical despite different names*

### Comparing `reddit_user_to_sqlite-0.4.1/reddit_user_to_sqlite/reddit_api.py` & `reddit_user_to_sqlite-0.4.2/reddit_user_to_sqlite/reddit_api.py`

 * *Files 19% similar despite different names*

```diff
@@ -8,23 +8,24 @@
     TypedDict,
     TypeVar,
     Union,
     cast,
     final,
 )
 
-if TYPE_CHECKING:
-    from typing import NotRequired
-
+import click
 import requests
 from tqdm import tqdm, trange
 
 from reddit_user_to_sqlite.helpers import batched
 
-USER_AGENT = "reddit-to-sqlite"
+if TYPE_CHECKING:
+    from typing import NotRequired
+
+USER_AGENT = "reddit-user-to-sqlite"
 
 
 class SubredditFragment(TypedDict):
     ## SUBREDDIT
     # "consoledeals"
     subreddit: str
     # ID
@@ -109,108 +110,166 @@
 
 @final
 class ResourceWrapper(TypedDict):
     kind: str
     data: Union[Comment, Post]
 
 
+class SuccessResponse(TypedDict):
+    kind: Literal["Listing", "t2"]
+
+
 @final
-class ResponseBody(TypedDict):
+class PagedResponseBody(TypedDict):
     before: Optional[str]
     after: Optional[str]
     modhash: str
     geo_filter: str
     dist: int
     children: Sequence[ResourceWrapper]
 
 
 @final
-class SuccessResponse(TypedDict):
-    data: ResponseBody
-    kind: Literal["Listing"]
+class PagedResponse(SuccessResponse):
+    data: PagedResponseBody
+
+
+@final
+class UserData(TypedDict):
+    id: str
+
+
+@final
+class UserResponse(SuccessResponse):
+    data: UserData
 
 
 @final
 class ErorrResponse(TypedDict):
     message: str
     error: int
 
 
-# max page size is 100
+ErrorHeaders = TypedDict(
+    "ErrorHeaders",
+    {
+        "x-ratelimit-used": str,
+        "x-ratelimit-remaining": str,
+        "x-ratelimit-reset": str,
+    },
+)
+
+# max API page size is 100
 PAGE_SIZE = 100
 
 
-def _raise_reddit_error(response):
-    if "error" in response:
+class RedditRateLimitException(Exception):
+    """
+    more info: https://support.reddithelp.com/hc/en-us/articles/16160319875092-Reddit-Data-API-Wiki
+    """
+
+    def __init__(self, headers: ErrorHeaders) -> None:
+        super().__init__("Rate limited by Reddit")
+
+        self.used = int(headers["x-ratelimit-used"])
+        self.remaining = int(headers["x-ratelimit-remaining"])
+        self.window_total = self.used + self.remaining
+        self.reset_after_seconds = int(headers["x-ratelimit-reset"])
+
+    @property
+    def stats(self) -> str:
+        return f"Used {self.used}/{self.window_total} requests (resets in {self.reset_after_seconds} seconds)"
+
+
+def _unwrap_response_and_raise(response: requests.Response):
+    result = response.json()
+
+    if "error" in result:
+        if result["error"] == 429:
+            raise RedditRateLimitException(cast(ErrorHeaders, response.headers))
+
         raise ValueError(
-            f'Received API error from Reddit (code {response["error"]}): {response["message"]}'
+            f'Received API error from Reddit (code {result["error"]}): {result["message"]}'
         )
 
+    return result
+
 
-def _call_reddit_api(
-    url: str, params: Optional[dict[str, Any]] = None
-) -> SuccessResponse:
-    response = requests.get(
-        url,
-        {"limit": PAGE_SIZE, "raw_json": 1, **(params or {})},
-        headers={"user-agent": USER_AGENT},
-    ).json()
+def _call_reddit_api(url: str, params: Optional[dict[str, Any]] = None):
+    return _unwrap_response_and_raise(
+        requests.get(
+            url,
+            {"raw_json": 1, "limit": PAGE_SIZE, **(params or {})},  # type: ignore
+            headers={"user-agent": USER_AGENT},
+        )
+    )
 
-    _raise_reddit_error(response)
 
-    return response
+def _rate_limit_message(e: RedditRateLimitException) -> str:
+    return f"Rate limited by reddit; try again in {e.reset_after_seconds} seconds. Until then, saving what we have"
 
 
 def _load_paged_resource(resource: Literal["comments", "submitted"], username: str):
+    """
+    handles paging logic for arbitrary-length queries with an "after" param
+    """
     result = []
     after = None
     # max number of pages we can fetch
     for _ in trange(10):
-        response = _call_reddit_api(
-            f"https://www.reddit.com/user/{username}/{resource}.json",
-            params={"after": after},
-        )
-        result += [c["data"] for c in response["data"]["children"]]
-        after = response["data"]["after"]
-
-        if len(response["data"]["children"]) < PAGE_SIZE:
+        try:
+            response: PagedResponse = _call_reddit_api(
+                f"https://www.reddit.com/user/{username}/{resource}.json",
+                params={"after": after},
+            )
+
+            result += [c["data"] for c in response["data"]["children"]]
+            after = response["data"]["after"]
+            if len(response["data"]["children"]) < PAGE_SIZE:
+                break
+        except RedditRateLimitException as e:
+            click.echo(_rate_limit_message(e), err=True)
             break
 
     return result
 
 
 def load_comments_for_user(username: str) -> list[Comment]:
     return _load_paged_resource("comments", username)
 
 
 def load_posts_for_user(username: str) -> list[Post]:
     return _load_paged_resource("submitted", username)
 
 
 def load_info(resources: Sequence[str]) -> list[Union[Comment, Post]]:
+    """
+    calls the `/info` endpoint to fetch data about a sequence of resources that include the type prefix
+    """
     result = []
-
     for batch in batched(
         tqdm(resources, disable=bool(os.environ.get("DISABLE_PROGRESS"))), PAGE_SIZE
     ):
-        response = _call_reddit_api(
-            "https://www.reddit.com/api/info.json", params={"id": ",".join(batch)}
-        )
-        result += [c["data"] for c in response["data"]["children"]]
+        try:
+            response: PagedResponse = _call_reddit_api(
+                "https://www.reddit.com/api/info.json",
+                params={"id": ",".join(batch)},
+            )
+            result += [c["data"] for c in response["data"]["children"]]
+        except RedditRateLimitException as e:
+            click.echo(_rate_limit_message(e), err=True)
+            break
 
     return result
 
 
 def get_user_id(username: str) -> str:
-    response = requests.get(
-        f"https://www.reddit.com/user/{username}/about.json",
-        headers={"user-agent": USER_AGENT},
-    ).json()
-
-    _raise_reddit_error(response)
+    response: UserResponse = _call_reddit_api(
+        f"https://www.reddit.com/user/{username}/about.json"
+    )
 
     return response["data"]["id"]
 
 
 T = TypeVar("T", Comment, Post)
```

### Comparing `reddit_user_to_sqlite-0.4.1/reddit_user_to_sqlite/sqlite_helpers.py` & `reddit_user_to_sqlite-0.4.2/reddit_user_to_sqlite/sqlite_helpers.py`

 * *Files 3% similar despite different names*

```diff
@@ -169,15 +169,14 @@
         "title": post["title"],
         "text": post["selftext"],
         "external_url": "" if "reddit.com" in post["url"] else post["url"],
         "user": post["author_fullname"][3:],
         "subreddit": post["subreddit_id"][3:],
         "permalink": f'https://old.reddit.com{post["permalink"]}',
         "upvote_ratio": post["upvote_ratio"],
-        "score": post["score"],
         "num_awards": post["total_awards_received"],
         "is_removed": int(post["selftext"] == "[removed]"),
     }
 
 
 def upsert_posts(
     db: Database, posts: Iterable[Post], table_prefix: Optional[PrefixType] = None
```

### Comparing `reddit_user_to_sqlite-0.4.1/PKG-INFO` & `reddit_user_to_sqlite-0.4.2/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: reddit-user-to-sqlite
-Version: 0.4.1
+Version: 0.4.2
 Summary: Create a SQLite database containing data pulled from Reddit about a single user.
 Keywords: sqlite,reddit,dogsheep
 Author-email: David Brownman <beamneocube@gmail.com>
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
 Classifier: Programming Language :: Python :: 3
 Classifier: Development Status :: 3 - Alpha
@@ -13,16 +13,16 @@
 Classifier: Operating System :: OS Independent
 Classifier: Natural Language :: English
 Requires-Dist: sqlite-utils==3.32.1
 Requires-Dist: click==8.1.3
 Requires-Dist: requests==2.29.0
 Requires-Dist: tqdm==4.65.0
 Requires-Dist: black==23.3.0 ; extra == "ci"
-Requires-Dist: isort==5.12.0 ; extra == "ci"
-Requires-Dist: pyright==1.1.309 ; extra == "ci"
+Requires-Dist: pyright==1.1.318 ; extra == "ci"
+Requires-Dist: ruff==0.0.277 ; extra == "ci"
 Requires-Dist: twine==4.0.2 ; extra == "release"
 Requires-Dist: build==0.10.0 ; extra == "release"
 Requires-Dist: pytest==7.3.1 ; extra == "test"
 Requires-Dist: responses==0.23.1 ; extra == "test"
 Project-URL: Author, https://xavd.id
 Project-URL: Bug Tracker, https://github.com/xavdid/reddit-user-to-sqlite/issues
 Project-URL: Changelog, https://github.com/xavdid/reddit-user-to-sqlite/blob/main/CHANGELOG.md
@@ -89,15 +89,15 @@
 
 Then, add the recommended plugins (for rendering timestamps and markdown):
 
 ```bash
 pipx inject datasette datasette-render-markdown datasette-render-timestamps
 ```
 
-Finally, create a `metadata.json` file with the following:
+Finally, create a `metadata.json` file next to your `reddit.db` with the following:
 
 ```json
 {
   "databases": {
     "reddit": {
       "tables": {
         "comments": {
@@ -205,15 +205,10 @@
 
 In your virtual environment, a simple `pytest` should run the unit test suite. You can also run `pyright` for type checking.
 
 ### Releasing New Versions
 
 > these notes are mostly for myself (or other contributors)
 
-0. ensure tests pass (`tox -p`)
-1. install release tooling (`pip install -e '.[release]'`)
-2. build the package (`python -m build`)
-3. upload the release (`python -m twine upload dist/*`)
-   1. give your username as `__token__`
-   2. give your password as your stored API key
-   3. If you're getting invalid password, verify that `~/.pypirc` is empty
+1. Run `just release` while your venv is active
+2. paste the stored API key (If you're getting invalid password, verify that `~/.pypirc` is empty)
```

