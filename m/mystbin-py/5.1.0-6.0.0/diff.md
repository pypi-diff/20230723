# Comparing `tmp/mystbin_py-5.1.0.tar.gz` & `tmp/mystbin_py-6.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mystbin_py-5.1.0.tar", max compression
+gzip compressed data, was "mystbin_py-6.0.0.tar", max compression
```

## Comparing `mystbin_py-5.1.0.tar` & `mystbin_py-6.0.0.tar`

### file list

```diff
@@ -1,14 +1,13 @@
--rwxr-xr-x   0        0        0     1063 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/LICENSE
--rwxr-xr-x   0        0        0     2896 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/README.md
--rwxr-xr-x   0        0        0     1547 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/mystbin/__init__.py
--rw-r--r--   0        0        0     6733 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/mystbin/client.py
--rw-r--r--   0        0        0     1737 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/mystbin/errors.py
--rw-r--r--   0        0        0    10710 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/mystbin/http.py
--rw-r--r--   0        0        0     4707 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/mystbin/paste.py
--rwxr-xr-x   0        0        0        0 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/mystbin/py.typed
--rw-r--r--   0        0        0     1149 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/mystbin/types/__init__.py
--rw-r--r--   0        0        0     1613 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/mystbin/types/responses.py
--rw-r--r--   0        0        0     2248 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/mystbin/utils.py
--rwxr-xr-x   0        0        0     2205 2022-12-13 11:39:08.450371 mystbin_py-5.1.0/pyproject.toml
--rw-r--r--   0        0        0     4036 1970-01-01 00:00:00.000000 mystbin_py-5.1.0/setup.py
--rw-r--r--   0        0        0     4221 1970-01-01 00:00:00.000000 mystbin_py-5.1.0/PKG-INFO
+-rwxr-xr-x   0        0        0     1063 2023-07-21 11:45:52.554451 mystbin_py-6.0.0/LICENSE
+-rwxr-xr-x   0        0        0     2854 2023-07-23 18:47:43.503227 mystbin_py-6.0.0/README.md
+-rwxr-xr-x   0        0        0     1547 2023-07-23 18:59:34.053690 mystbin_py-6.0.0/mystbin/__init__.py
+-rwxr-xr-x   0        0        0     6382 2023-07-23 18:36:56.781690 mystbin_py-6.0.0/mystbin/client.py
+-rwxr-xr-x   0        0        0     1738 2023-07-21 11:50:11.686218 mystbin_py-6.0.0/mystbin/errors.py
+-rwxr-xr-x   0        0        0    10885 2023-07-23 18:21:32.231992 mystbin_py-6.0.0/mystbin/http.py
+-rwxr-xr-x   0        0        0     4715 2023-07-23 18:23:13.509501 mystbin_py-6.0.0/mystbin/paste.py
+-rwxr-xr-x   0        0        0        0 2023-07-21 11:45:52.554451 mystbin_py-6.0.0/mystbin/py.typed
+-rwxr-xr-x   0        0        0     1149 2023-07-21 11:45:52.554451 mystbin_py-6.0.0/mystbin/types/__init__.py
+-rwxr-xr-x   0        0        0     1613 2023-07-21 11:50:11.694218 mystbin_py-6.0.0/mystbin/types/responses.py
+-rwxr-xr-x   0        0        0     2263 2023-07-21 11:45:52.558451 mystbin_py-6.0.0/mystbin/utils.py
+-rwxr-xr-x   0        0        0     2147 2023-07-23 18:59:22.461519 mystbin_py-6.0.0/pyproject.toml
+-rw-r--r--   0        0        0     4186 1970-01-01 00:00:00.000000 mystbin_py-6.0.0/PKG-INFO
```

### Comparing `mystbin_py-5.1.0/LICENSE` & `mystbin_py-6.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `mystbin_py-5.1.0/README.md` & `mystbin_py-6.0.0/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 <div align="center">
     <h1>Mystbin.py!</h1>
     <a href='https://mystbinpy.readthedocs.io/en/latest/?badge=latest'>
         <img src='https://readthedocs.org/projects/mystbinpy/badge/?version=latest' alt='Documentation Status' />
     </a>
-    <a href='https://github.com/PythonistaGuild/mystbin.py/workflows/Code%20Linting'>
-        <img src='https://github.com/PythonistaGuild/mystbin.py/workflows/Code%20Linting/badge.svg?branch=main' alt='Linting status' />
+    <a href='https://github.com/PythonistaGuild/mystbin.py/actions/workflows/coverage_and_lint.yaml'>
+        <img src='https://github.com/PythonistaGuild/mystbin.py/workflows/Type%20Coverage%20and%20Linting/badge.svg?branch=main' alt='Linting status' />
     </a>
-    <a href='https://github.com/PythonistaGuild/mystbin.py/workflows/Build'>
+    <a href='https://github.com/PythonistaGuild/mystbin.py/actions/workflows/build.yaml'>
         <img src='https://github.com/PythonistaGuild/mystbin.py/workflows/Build/badge.svg' alt='Build status' />
     </a>
 </div>
 <br>
 
 A small simple wrapper around the [Mystb.in](https://mystb.in/) API. API docs can be found [here](https://api.mystb.in/docs).
 
@@ -39,42 +39,43 @@
 
 Installing from source:
 ```shell
 python -m pip install git+https://github.com/PythonistaGuild/mystbin.py.git
 ```
 
 ### Usage examples
-Since the project is considered multi-sync, it will work in a sync/async environment, see the optional dependency of `requests` below.
 
 ```py
 # async example - it will default to async
 import mystbin
 
-mystbin_client = mystbin.Client()
+client = mystbin.Client()
 
 paste = await client.create_paste(filename="Hello.txt", content="Hello there!")
+# we also support passing a mystbin.File directly to the `file=` kwarg!
+
 str(paste)
 >>> 'https://mystb.in/<your generated ID>'
 
-get_paste = await mystbin_client.get_paste("<your generated ID>")
+get_paste = await client.get_paste("<your generated ID>")
 get_paste.files[0].content
 >>> "Hello there!"
 
 get_paste.created_at
 >>> datetime.datetime(2020, 10, 6, 10, 53, 57, 556741)
 ```
 
 Or if you want to create a paste with multiple files...
 ```py
 import mystbin
 
 file = mystbin.File(filename="File1.txt", content="Hello there!")
 file2 = mystbin.File(filename="test.py", content="print('hello!')")
 
-paste = await client.create_multifile_paste(files=[file, file2])
+paste = await client.create_paste(files=[file, file2])
 
 for file in paste.files:
     print(file.content)
 
 >>> "Hello there!"
 >>> "print('hello!')"
 ```
```

#### html2text {}

```diff
@@ -9,22 +9,21 @@
 pastes. - [ ] - Editing pastes. - Pending design work. - [x] - Deleting pastes.
 - [x] - Getting pastes. - [ ] - User endpoints. - [ ] - Sync client. - This one
 will take some time as I have no motivation to do it, but PRs are welcome if
 others want to do it. ### Installation This project will be on [PyPI](https://
 pypi.org/project/mystbin.py/) as a stable release, you can always find that
 there. Installing via `pip`: ```shell python -m pip install -U mystbin.py ```
 Installing from source: ```shell python -m pip install git+https://github.com/
-PythonistaGuild/mystbin.py.git ``` ### Usage examples Since the project is
-considered multi-sync, it will work in a sync/async environment, see the
-optional dependency of `requests` below. ```py # async example - it will
-default to async import mystbin mystbin_client = mystbin.Client() paste = await
-client.create_paste(filename="Hello.txt", content="Hello there!") str(paste)
->>> 'https://mystb.in/' get_paste = await mystbin_client.get_paste("")
-get_paste.files[0].content >>> "Hello there!" get_paste.created_at >>>
-datetime.datetime(2020, 10, 6, 10, 53, 57, 556741) ``` Or if you want to create
-a paste with multiple files... ```py import mystbin file = mystbin.File
-(filename="File1.txt", content="Hello there!") file2 = mystbin.File
-(filename="test.py", content="print('hello!')") paste = await
-client.create_multifile_paste(files=[file, file2]) for file in paste.files:
-print(file.content) >>> "Hello there!" >>> "print('hello!')" ``` If you have
-any question please feel free to join the Pythonista Discord server:
+PythonistaGuild/mystbin.py.git ``` ### Usage examples ```py # async example -
+it will default to async import mystbin client = mystbin.Client() paste = await
+client.create_paste(filename="Hello.txt", content="Hello there!") # we also
+support passing a mystbin.File directly to the `file=` kwarg! str(paste) >>>
+'https://mystb.in/' get_paste = await client.get_paste("") get_paste.files
+[0].content >>> "Hello there!" get_paste.created_at >>> datetime.datetime(2020,
+10, 6, 10, 53, 57, 556741) ``` Or if you want to create a paste with multiple
+files... ```py import mystbin file = mystbin.File(filename="File1.txt",
+content="Hello there!") file2 = mystbin.File(filename="test.py", content="print
+('hello!')") paste = await client.create_paste(files=[file, file2]) for file in
+paste.files: print(file.content) >>> "Hello there!" >>> "print('hello!')" ```
+If you have any question please feel free to join the Pythonista Discord
+server:
 [Discord_Server]
```

### Comparing `mystbin_py-5.1.0/mystbin/__init__.py` & `mystbin_py-6.0.0/mystbin/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -36,8 +36,8 @@
     major: int
     minor: int
     micro: int
     releaselevel: Literal["alpha", "beta", "candidate", "final"]
     serial: int
 
 
-version_info: VersionInfo = VersionInfo(major=5, minor=1, micro=0, releaselevel="final", serial=0)
+version_info: VersionInfo = VersionInfo(major=6, minor=0, micro=0, releaselevel="final", serial=0)
```

### Comparing `mystbin_py-5.1.0/mystbin/client.py` & `mystbin_py-6.0.0/mystbin/client.py`

 * *Files 16% similar despite different names*

```diff
@@ -19,15 +19,15 @@
 FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
 DEALINGS IN THE SOFTWARE.
 """
 
 from __future__ import annotations
 
 import datetime
-from typing import Optional
+from typing import List, Optional, Sequence, overload
 
 import aiohttp
 
 from .http import HTTPClient
 from .paste import File, Paste
 from .utils import require_authentication
 
@@ -42,173 +42,169 @@
         self.http: HTTPClient = HTTPClient(token=token, session=session)
 
     async def close(self) -> None:
         """|coro|
 
         Closes the internal HTTP session and this client.
         """
-        if self.http._session:
-            await self.http._session.close()
+        await self.http.close()
 
+    @overload
     async def create_paste(
         self,
         *,
         filename: str,
         content: str,
+        file: None = ...,
+        files: None = ...,
+        password: Optional[str] = ...,
+        expires: Optional[datetime.datetime] = ...,
+    ) -> Paste:
+        ...
+
+    @overload
+    async def create_paste(
+        self,
+        *,
+        filename: None = ...,
+        content: None = ...,
+        file: File,
+        files: None = ...,
+        password: Optional[str] = ...,
+        expires: Optional[datetime.datetime] = ...,
+    ) -> Paste:
+        ...
+
+    @overload
+    async def create_paste(
+        self,
+        *,
+        filename: None = ...,
+        content: None = ...,
+        file: None = ...,
+        files: Sequence[File],
+        password: Optional[str] = ...,
+        expires: Optional[datetime.datetime] = ...,
+    ) -> Paste:
+        ...
+
+    async def create_paste(
+        self,
+        *,
+        filename: Optional[str] = None,
+        content: Optional[str] = None,
+        file: Optional[File] = None,
+        files: Optional[Sequence[File]] = None,
         password: Optional[str] = None,
         expires: Optional[datetime.datetime] = None,
     ) -> Paste:
         """|coro|
 
         Create a single file paste on mystb.in.
 
         Parameters
         -----------
-        filename: :class:`str`
+        filename: Optional[:class:`str`]
             The filename to create.
-        content: :class:`str`
+        content: Optional[:class:`str`]
             The content of the file you are creating.
+        file: Optional[:class:`~mystbin.File`]
+            The pre-created file you wish to upload.
+        files: Optional[List[:class:`~mystbin.File`]]
+            The pre-creates list of files you wish to upload.
         password: Optional[:class:`str`]
             The password of the paste, if any.
         expires: Optional[:class:`datetime.datetime`]
             When the paste expires, if any.
 
+        Raises
+        -------
+        :exc:`ValueError`
+            A bad combinarion of singular and plural pastes were passed.
+
         Returns
         --------
         :class:`mystbin.Paste`
             The paste that was created.
-        """
-        file = File(filename=filename, content=content)
-        data = await self.http._create_paste(file=file, password=password, expires=expires)
-        return Paste._from_data(data)
 
-    async def create_multifile_paste(
-        self, *, files: list[File], password: Optional[str] = None, expires: Optional[datetime.datetime] = None
-    ) -> Paste:
-        """|coro|
 
-        Create a paste with multiple files on mystb.in.
+        ..note::
+            Passing combinations of both singular and plural files is not supports and will raise an exception.
+            Internally the order of precesence is ``files`` > ``file`` > ``filename and content``.
+        """
+        if (filename and content) and file:
+            raise ValueError("Cannot provide both `file` and `filename`/`content`")
+
+        resolved_files: Sequence[File] = []
+        if filename and content:
+            resolved_files = [File(filename=filename, content=content)]
+        elif file:
+            resolved_files = [file]
 
-        Parameters
-        ------------
-        files: list[:class:`mystbin.File`]
-            A list of files to create on mystbin.
-        password: Optional[:class:`str`]
-            The password for this paste, if any.
-        expires: Optional[:class:`datetime.datetime`]
-            When this paste expires, if any.
+        if resolved_files and files:
+            raise ValueError("Cannot provide both singular and plural files.")
 
-        Returns
-        --------
-        :class:`mystbin.Paste`
-            The paste that was created.
-        """
-        data = await self.http._create_paste(files=files, password=password, expires=expires)
-        return Paste._from_data(data)
+        resolved_files = files or resolved_files
+
+        data = await self.http.create_paste(files=resolved_files, password=password, expires=expires)
+        return Paste.from_data(data)
 
     @require_authentication
     async def delete_paste(self, paste_id: str, /) -> None:
         """|coro|
 
         Delete a paste.
 
         Parameters
         -----------
         paste_id: :class:`str`
             The paste to delete.
         """
-        await self.http._delete_pastes(paste_ids=[paste_id])
+        await self.http.delete_pastes(paste_ids=[paste_id])
 
     @require_authentication
-    async def delete_pastes(self, paste_ids: list[str], /) -> None:
+    async def delete_pastes(self, paste_ids: List[str], /) -> None:
         """|coro|
 
         Delete multiple pastes.
 
         Parameters
         -----------
-        paste_ids: list[:class:`str`]
+        paste_ids: List[:class:`str`]
             The pastes to delete.
         """
-        await self.http._delete_pastes(paste_ids=paste_ids)
+        await self.http.delete_pastes(paste_ids=paste_ids)
 
     async def get_paste(self, paste_id: str, *, password: Optional[str] = None) -> Paste:
         """|coro|
 
         Fetch a paste.
 
         Parameters
         -----------
         paste_id: :class:`str`
             The paste id to fetch.
         password: Optional[:class:`str`]
             The password of the paste, if any.
         """
-        data = await self.http._get_paste(paste_id=paste_id, password=password)
-        return Paste._from_data(data)
-
-    # @overload
-    # async def edit_paste(self, paste_id: str, *, new_content: str, new_filename: ..., new_expires: ...) -> None:
-    #     ...
-
-    # @overload
-    # async def edit_paste(self, paste_id: str, *, new_content: ..., new_filename: str, new_expires: ...) -> None:
-    #     ...
-
-    # @overload
-    # async def edit_paste(
-    #     self, paste_id: str, *, new_content: ..., new_filename: ..., new_expires: datetime.datetime
-    # ) -> None:
-    #     ...
-
-    # @overload
-    # async def edit_paste(self, paste_id: str, *, new_content: str, new_filename: str, new_expires: ...) -> None:
-    #     ...
-
-    # @overload
-    # async def edit_paste(
-    #     self, paste_id: str, *, new_content: str, new_filename: ..., new_expires: datetime.datetime
-    # ) -> None:
-    #     ...
-
-    # @overload
-    # async def edit_paste(
-    #     self, paste_id: str, *, new_content: ..., new_filename: str, new_expires: datetime.datetime
-    # ) -> None:
-    #     ...
-
-    # @overload
-    # async def edit_paste(
-    #     self, paste_id: str, *, new_content: str, new_filename: str, new_expires: datetime.datetime
-    # ) -> None:
-    #     ...
-
-    # @require_authentication
-    # async def edit_paste(
-    #     self,
-    #     paste_id: str,
-    #     *,
-    #     new_content: Optional[str] = MISSING,
-    #     new_filename: Optional[str] = MISSING,
-    #     new_expires: Optional[datetime.datetime] = MISSING,
-    # ) -> None:
-    #     await self.http._edit_paste(paste_id, new_content=new_content, new_filename=new_filename, new_expires=new_expires)
+        data = await self.http.get_paste(paste_id=paste_id, password=password)
+        return Paste.from_data(data)
 
     @require_authentication
-    async def get_user_pastes(self, *, limit: int = 100) -> list[Paste]:
+    async def get_user_pastes(self, *, limit: int = 100) -> List[Paste]:
         """|coro|
 
         Get all pastes belonging to the current authenticated user.
 
         Parameters
         -----------
         limit: :class:`int`
             The amount of pastes to fetch. Defaults to ``100``.
 
         Returns
         --------
-        list[:class:`Paste`]
+        List[:class:`Paste`]
             The pastes that were fetched.
         """
-        data = await self.http._get_my_pastes(limit=limit)
+        data = await self.http.get_my_pastes(limit=limit)
 
-        return [Paste._from_data(x) for x in data]
+        return [Paste.from_data(x) for x in data]
```

### Comparing `mystbin_py-5.1.0/mystbin/errors.py` & `mystbin_py-6.0.0/mystbin/errors.py`

 * *Files 4% similar despite different names*

```diff
@@ -17,14 +17,15 @@
 AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
 FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
 DEALINGS IN THE SOFTWARE.
 """
 import aiohttp
 
+
 __all__ = (
     "APIException",
     "AuthenticationRequired",
 )
 
 
 class APIException(Exception):
```

### Comparing `mystbin_py-5.1.0/mystbin/http.py` & `mystbin_py-6.0.0/mystbin/http.py`

 * *Files 3% similar despite different names*

```diff
@@ -29,16 +29,18 @@
 import sys
 import weakref
 from typing import (
     TYPE_CHECKING,
     Any,
     ClassVar,
     Coroutine,
+    Dict,
     Literal,
     Optional,
+    Sequence,
     Type,
     TypeVar,
     Union,
 )
 from urllib.parse import quote as _uriquote
 
 import aiohttp
@@ -55,28 +57,28 @@
 
     T = TypeVar("T")
     Response = Coroutine[None, None, T]
     MU = TypeVar("MU", bound="MaybeUnlock")
     BE = TypeVar("BE", bound=BaseException)
     from .types.responses import EditPasteResponse, PasteResponse
 
-HTTPVerb = Literal["GET", "POST", "PUT", "DELETE", "PATCH"]
+SupportedHTTPVerb = Literal["GET", "POST", "PUT", "DELETE", "PATCH"]
 
 LOGGER: logging.Logger = logging.getLogger(__name__)
 
 __all__ = ("HTTPClient",)
 
 
 def _clean_dt(dt: datetime.datetime) -> str:
     dt = dt.astimezone(datetime.timezone.utc)
 
     return dt.isoformat()
 
 
-async def json_or_text(response: aiohttp.ClientResponse, /) -> Union[dict[str, Any], str]:
+async def json_or_text(response: aiohttp.ClientResponse, /) -> Union[Dict[str, Any], str]:
     """A quick method to parse a `aiohttp.ClientResponse` and test if it's json or text."""
     text = await response.text(encoding="utf-8")
     try:
         if response.headers["content-type"] == "application/json":
             try:
                 return json.loads(text)
             except json.JSONDecodeError:
@@ -113,16 +115,16 @@
         "verb",
         "path",
         "url",
     )
 
     API_BASE: ClassVar[str] = "https://api.mystb.in"
 
-    def __init__(self, verb: HTTPVerb, path: str, **params: Any) -> None:
-        self.verb: HTTPVerb = verb
+    def __init__(self, verb: SupportedHTTPVerb, path: str, **params: Any) -> None:
+        self.verb: SupportedHTTPVerb = verb
         self.path: str = path
         url = self.API_BASE + path
         if params:
             url = url.format_map({k: _uriquote(v) if isinstance(v, str) else v for k, v in params.items()})
         self.url: str = url
 
 
@@ -134,18 +136,22 @@
         "_locks",
         "user_agent",
     )
 
     def __init__(self, *, token: Optional[str], session: Optional[aiohttp.ClientSession] = None) -> None:
         self._token: Optional[str] = token
         self._session: Optional[aiohttp.ClientSession] = session
-        self._locks: weakref.WeakValueDictionary = weakref.WeakValueDictionary()
+        self._locks: weakref.WeakValueDictionary[str, asyncio.Lock] = weakref.WeakValueDictionary()
         user_agent = "mystbin.py (https://github.com/PythonistaGuild/mystbin.py {0}) Python/{1[0]}.{1[1]} aiohttp/{2}"
         self.user_agent: str = user_agent.format(__version__, sys.version_info, aiohttp.__version__)
 
+    async def close(self) -> None:
+        if self._session:
+            await self._session.close()
+
     async def _generate_session(self) -> aiohttp.ClientSession:
         self._session = aiohttp.ClientSession()
         return self._session
 
     async def request(self, route: Route, **kwargs: Any) -> Any:
         if self._session is None:
             self._session = await self._generate_session()
@@ -233,71 +239,71 @@
                 if response.status >= 500:
                     raise APIException(response=response, status_code=response.status)
 
                 raise APIException(response=response, status_code=response.status)
 
             raise RuntimeError("Unreachable code in HTTP handling.")
 
-    def _create_paste(
+    def create_paste(
         self,
         *,
         file: Optional[File] = None,
-        files: Optional[list[File]] = None,
+        files: Optional[Sequence[File]] = None,
         password: Optional[str],
         expires: Optional[datetime.datetime],
     ) -> Response[PasteResponse]:
         route = Route("PUT", "/paste")
 
-        json_: dict[str, Any] = {}
+        json_: Dict[str, Any] = {}
         if file:
-            json_["files"] = [file._to_dict()]
+            json_["files"] = [file.to_dict()]
         elif files:
-            json_["files"] = [f._to_dict() for f in files]
+            json_["files"] = [f.to_dict() for f in files]
 
         if password:
             json_["password"] = password
         if expires:
             json_["expires"] = _clean_dt(expires)
 
         return self.request(route=route, json=json_)
 
-    def _delete_paste(self, *, paste_id: str) -> Response[None]:
-        return self._delete_pastes(paste_ids=[paste_id])
+    def delete_paste(self, *, paste_id: str) -> Response[None]:
+        return self.delete_pastes(paste_ids=[paste_id])
 
-    def _delete_pastes(self, *, paste_ids: list[str]) -> Response[None]:
+    def delete_pastes(self, *, paste_ids: Sequence[str]) -> Response[None]:
         route = Route("DELETE", "/paste")
         return self.request(route=route, json={"pastes": paste_ids})
 
-    def _get_paste(self, *, paste_id: str, password: Optional[str]) -> Response[PasteResponse]:
+    def get_paste(self, *, paste_id: str, password: Optional[str]) -> Response[PasteResponse]:
         route = Route("GET", "/paste/{paste_id}", paste_id=paste_id)
 
         if password:
             return self.request(route=route, params={"password": password})
         return self.request(route=route)
 
-    def _edit_paste(
+    def edit_paste(
         self,
         paste_id: str,
         *,
         new_content: str = MISSING,
         new_filename: str = MISSING,
         new_expires: datetime.datetime = MISSING,
     ) -> Response[EditPasteResponse]:
         route = Route("PATCH", "/paste/{paste_id}", paste_id=paste_id)
 
-        json_: dict[str, Any] = {}
+        json_: Dict[str, Any] = {}
 
         if new_content is not MISSING:
             json_["new_content"] = new_content
 
         if new_filename is not MISSING:
             json_["new_filename"] = new_filename
 
         if new_expires is not MISSING:
             json_["new_expires"] = _clean_dt(new_expires)
 
         return self.request(route, json=json_)
 
-    def _get_my_pastes(self, *, limit: int) -> Response[list[PasteResponse]]:
+    def get_my_pastes(self, *, limit: int) -> Response[Sequence[PasteResponse]]:
         route = Route("GET", "/pastes/@me")
 
         return self.request(route, params={limit: limit})
```

### Comparing `mystbin_py-5.1.0/mystbin/paste.py` & `mystbin_py-6.0.0/mystbin/paste.py`

 * *Files 2% similar despite different names*

```diff
@@ -19,15 +19,15 @@
 FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
 DEALINGS IN THE SOFTWARE.
 """
 
 from __future__ import annotations
 
 import datetime
-from typing import TYPE_CHECKING, Any, Optional
+from typing import TYPE_CHECKING, Any, Dict, List, Optional
 
 
 if TYPE_CHECKING:
     from typing_extensions import Self
 
     from mystbin.types.responses import FileResponse, PasteResponse
 
@@ -72,26 +72,26 @@
         return self._lines_of_code
 
     @property
     def character_count(self) -> int:
         return self._character_count
 
     @classmethod
-    def _from_data(cls, payload: FileResponse, /) -> Self:
+    def from_data(cls, payload: FileResponse, /) -> Self:
         self = cls(
             content=payload["content"],
             filename=payload["filename"],
         )
         self._lines_of_code = payload["loc"]
         self._character_count = payload["charcount"]
 
         return self
 
-    def _to_dict(self) -> dict[str, Any]:
-        ret: dict[str, Any] = {"content": self.content, "filename": self.filename}
+    def to_dict(self) -> Dict[str, Any]:
+        ret: Dict[str, Any] = {"content": self.content, "filename": self.filename}
 
         return ret
 
 
 class Paste:
     _last_edited: Optional[datetime.datetime]
     _expires: Optional[datetime.datetime]
@@ -101,15 +101,15 @@
 
     Attributes
     -----------
     id: :class:`str`
         The ID of this paste.
     created_at: :class:`datetime.datetime`
         When this paste was created in UTC.
-    files: list[:class:`mystbin.File`]
+    files: List[:class:`mystbin.File`]
         The list of files within this Paste.
     """
 
     __slots__ = (
         "id",
         "author_id",
         "created_at",
@@ -121,15 +121,15 @@
     )
 
     def __init__(
         self,
         *,
         id: str,
         created_at: str,
-        files: list[File],
+        files: List[File],
     ) -> None:
         self.id: str = id
         self.created_at: datetime.datetime = datetime.datetime.fromisoformat(created_at)
         self.files: list[File] = files
 
     def __str__(self) -> str:
         return self.url
@@ -150,16 +150,16 @@
         return self._expires
 
     @property
     def views(self) -> Optional[int]:
         return self._views
 
     @classmethod
-    def _from_data(cls, payload: PasteResponse, /) -> Self:
-        files = [File._from_data(data) for data in payload["files"]]
+    def from_data(cls, payload: PasteResponse, /) -> Self:
+        files = [File.from_data(data) for data in payload["files"]]
         self = cls(
             id=payload["id"],
             created_at=payload["created_at"],
             files=files,
         )
         self._views = payload.get("views")
         last_edited = payload.get("last_edited")
```

### Comparing `mystbin_py-5.1.0/mystbin/types/__init__.py` & `mystbin_py-6.0.0/mystbin/types/__init__.py`

 * *Files identical despite different names*

### Comparing `mystbin_py-5.1.0/mystbin/types/responses.py` & `mystbin_py-6.0.0/mystbin/types/responses.py`

 * *Ordering differences only*

 * *Files 1% similar despite different names*

```diff
@@ -17,16 +17,16 @@
 AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
 FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER
 DEALINGS IN THE SOFTWARE.
 """
 
 from __future__ import annotations
-from datetime import datetime
 
+from datetime import datetime
 from typing import Optional, TypedDict
 
 
 __all__ = (
     "FileResponse",
     "PasteResponse",
 )
```

### Comparing `mystbin_py-5.1.0/mystbin/utils.py` & `mystbin_py-6.0.0/mystbin/utils.py`

 * *Files 4% similar despite different names*

```diff
@@ -36,24 +36,24 @@
 
 __all__ = ("MISSING", "require_authentication")
 
 
 class _MissingSentinel:
     __slots__ = ()
 
-    def __eq__(self, other) -> bool:
+    def __eq__(self, other: object) -> bool:
         return False
 
     def __bool__(self) -> bool:
         return False
 
     def __hash__(self) -> int:
         return 0
 
-    def __repr__(self):
+    def __repr__(self) -> str:
         return "..."
 
 
 MISSING: Any = _MissingSentinel()
 
 
 def require_authentication(func: Callable[Concatenate[C, B], T]) -> Callable[Concatenate[C, B], T]:
```

### Comparing `mystbin_py-5.1.0/pyproject.toml` & `mystbin_py-6.0.0/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,24 +1,26 @@
 [tool.poetry]
 name = "mystbin-py"
-version = "5.1.0"
+version = "6.0.0"
 description = "A small simple wrapper around the mystb.in API."
 authors = ["AbstractUmbra <Umbra@AbstractUmbra.dev>"]
 license = "MIT"
 readme = "README.md"
 homepage = "https://github.com/PythonistaGuild/mystbin.py"
 repository = "https://github.com/PythonistaGuild/mystbin.py"
 keywords = ["mystbin",  "paste"]
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Intended Audience :: Developers",
     "Natural Language :: English",
     "Operating System :: OS Independent",
+    "Programming Language :: Python :: 3.8",
     "Programming Language :: Python :: 3.9",
     "Programming Language :: Python :: 3.10",
+    "Programming Language :: Python :: 3.11",
     "Topic :: Internet",
     "Typing :: Typed",
 ]
 include = [
     "LICENSE"
 ]
 packages = [
@@ -27,57 +29,56 @@
     { include = "mystbin/py.typed" }
 ]
 
 [tool.poetry.urls]
 "Issue Tracker" = "https://github.com/PythonistaGuild/mystbin.py/issues"
 
 [tool.poetry.dependencies]
-python = "^3.9"
-aiohttp = "^3.7.4"
-requests = {version = "^2.24.0", optional = true}
+python = "^3.8"
+aiohttp = [
+    { version = "^3.8" },
+    { version = "^3.8", markers = "extra == 'speed'", extras= ["speedups"]},
+]
+
 sphinx = { version = "^4.0.0", optional = true }
 sphinxcontrib-trio = { version = "*", optional = true }
 furo = { version = "*", optional = true }
-
-[tool.poetry.dev-dependencies]
-black = "*"
+pytz = { version = "*", optional = true, python="<3.9" }
 
 [tool.poetry.extras]
-requests = ["requests"]
+speed = ["aiohttp"]
 docs = ["sphinx", "sphinxcontrib-trio", "furo"]
 
+[tool.poetry.group.speedups.dependencies]
+aiohttp = { version = "^3.8", extras = ["speedups"] }
+
+[tool.poetry.group.docs.dependencies]
+sphinx = "*"
+sphinxcontrib-trio = "*"
+furo = "*"
+
+[tool.poetry.group.dev.dependencies]
+black = "*"
+isort = "*"
+
 [tool.poetry.scripts]
 version = 'mystbin.__main__:show_version'
 
 [tool.black]
 line-length = 125
-target-version = ["py39"]
+target-version = ["py38"]
 
 [tool.isort]
 profile = "black"
 src_paths = ["mystbin"]
 lines_after_imports = 2
 
 [tool.pyright]
 ignore = ["docs/conf.py"]
 include = ["mystbin/**/*.py"]
 useLibraryCodeForTypes = true
-typeCheckingMode = "basic"
-pythonVersion = "3.9"
-strictListInference = true
-strictDictionaryInference = true
-strictSetInference = true
-strictParameterNoneValue = true
-reportMissingImports = "error"
-reportUnusedImport = "error"
-reportUnusedClass = "error"
-reportUnusedFunction = "error"
-reportUnusedVariable = "error"
-reportUnusedExpression = "error"
-reportGeneralTypeIssues = "error"
-reportDuplicateImport = "error"
-reportUntypedFunctionDecorator = "error"
-reportUnnecessaryTypeIgnoreComment = "warning"
+typeCheckingMode = "strict"
+pythonVersion = "3.8"
 
 [build-system]
 requires = ["poetry>=1.0"]
 build-backend = "poetry.masonry.api"
```

### Comparing `mystbin_py-5.1.0/setup.py` & `mystbin_py-6.0.0/PKG-INFO`

 * *Files 23% similar despite different names*

```diff
@@ -1,42 +1,122 @@
-# -*- coding: utf-8 -*-
-from setuptools import setup
+Metadata-Version: 2.1
+Name: mystbin-py
+Version: 6.0.0
+Summary: A small simple wrapper around the mystb.in API.
+Home-page: https://github.com/PythonistaGuild/mystbin.py
+License: MIT
+Keywords: mystbin,paste
+Author: AbstractUmbra
+Author-email: Umbra@AbstractUmbra.dev
+Requires-Python: >=3.8,<4.0
+Classifier: Intended Audience :: Developers
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Natural Language :: English
+Classifier: Operating System :: OS Independent
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
+Classifier: Topic :: Internet
+Classifier: Typing :: Typed
+Provides-Extra: docs
+Provides-Extra: speed
+Requires-Dist: aiohttp (>=3.8,<4.0) ; extra == "speed"
+Requires-Dist: aiohttp[speedups] (>=3.8,<4.0) ; extra == "speed"
+Requires-Dist: furo ; extra == "docs"
+Requires-Dist: pytz ; python_version < "3.9"
+Requires-Dist: sphinx (>=4.0.0,<5.0.0) ; extra == "docs"
+Requires-Dist: sphinxcontrib-trio ; extra == "docs"
+Project-URL: Issue Tracker, https://github.com/PythonistaGuild/mystbin.py/issues
+Project-URL: Repository, https://github.com/PythonistaGuild/mystbin.py
+Description-Content-Type: text/markdown
+
+<div align="center">
+    <h1>Mystbin.py!</h1>
+    <a href='https://mystbinpy.readthedocs.io/en/latest/?badge=latest'>
+        <img src='https://readthedocs.org/projects/mystbinpy/badge/?version=latest' alt='Documentation Status' />
+    </a>
+    <a href='https://github.com/PythonistaGuild/mystbin.py/actions/workflows/coverage_and_lint.yaml'>
+        <img src='https://github.com/PythonistaGuild/mystbin.py/workflows/Type%20Coverage%20and%20Linting/badge.svg?branch=main' alt='Linting status' />
+    </a>
+    <a href='https://github.com/PythonistaGuild/mystbin.py/actions/workflows/build.yaml'>
+        <img src='https://github.com/PythonistaGuild/mystbin.py/workflows/Build/badge.svg' alt='Build status' />
+    </a>
+</div>
+<br>
+
+A small simple wrapper around the [Mystb.in](https://mystb.in/) API. API docs can be found [here](https://api.mystb.in/docs).
+
+Documentation for this wrapper can be found [here](https://mystbinpy.readthedocs.io/en/stable/).
+If you want the docs for the `main` branch, those can be found [here](https://mystbinpy.readthedocs.io/en/latest/).
+
+----------
+### Features
+
+- [x] - Creating pastes.
+- [ ] - Editing pastes.
+    - Pending design work.
+- [x] - Deleting pastes.
+- [x] - Getting pastes.
+- [ ] - User endpoints.
+- [ ] - Sync client.
+  - This one will take some time as I have no motivation to do it, but PRs are welcome if others want to do it.
+
+### Installation
+This project will be on [PyPI](https://pypi.org/project/mystbin.py/) as a stable release, you can always find that there.
+
+Installing via `pip`:
+```shell
+python -m pip install -U mystbin.py
+```
+
+Installing from source:
+```shell
+python -m pip install git+https://github.com/PythonistaGuild/mystbin.py.git
+```
+
+### Usage examples
+
+```py
+# async example - it will default to async
+import mystbin
+
+client = mystbin.Client()
+
+paste = await client.create_paste(filename="Hello.txt", content="Hello there!")
+# we also support passing a mystbin.File directly to the `file=` kwarg!
+
+str(paste)
+>>> 'https://mystb.in/<your generated ID>'
+
+get_paste = await client.get_paste("<your generated ID>")
+get_paste.files[0].content
+>>> "Hello there!"
+
+get_paste.created_at
+>>> datetime.datetime(2020, 10, 6, 10, 53, 57, 556741)
+```
+
+Or if you want to create a paste with multiple files...
+```py
+import mystbin
+
+file = mystbin.File(filename="File1.txt", content="Hello there!")
+file2 = mystbin.File(filename="test.py", content="print('hello!')")
+
+paste = await client.create_paste(files=[file, file2])
+
+for file in paste.files:
+    print(file.content)
+
+>>> "Hello there!"
+>>> "print('hello!')"
+```
+
+If you have any question please feel free to join the Pythonista Discord server:
+<div align="left">
+    <a href="https://discord.gg/RAKc3HF">
+        <img src="https://discordapp.com/api/guilds/490948346773635102/widget.png?style=banner2" alt="Discord Server"/>
+    </a>
+</div>
 
-packages = \
-['mystbin', 'mystbin.types']
-
-package_data = \
-{'': ['*']}
-
-modules = \
-['py']
-install_requires = \
-['aiohttp>=3.7.4,<4.0.0']
-
-extras_require = \
-{'docs': ['sphinx>=4.0.0,<5.0.0', 'sphinxcontrib-trio', 'furo'],
- 'requests': ['requests>=2.24.0,<3.0.0']}
-
-entry_points = \
-{'console_scripts': ['version = mystbin.__main__:show_version']}
-
-setup_kwargs = {
-    'name': 'mystbin-py',
-    'version': '5.1.0',
-    'description': 'A small simple wrapper around the mystb.in API.',
-    'long_description': '<div align="center">\n    <h1>Mystbin.py!</h1>\n    <a href=\'https://mystbinpy.readthedocs.io/en/latest/?badge=latest\'>\n        <img src=\'https://readthedocs.org/projects/mystbinpy/badge/?version=latest\' alt=\'Documentation Status\' />\n    </a>\n    <a href=\'https://github.com/PythonistaGuild/mystbin.py/workflows/Code%20Linting\'>\n        <img src=\'https://github.com/PythonistaGuild/mystbin.py/workflows/Code%20Linting/badge.svg?branch=main\' alt=\'Linting status\' />\n    </a>\n    <a href=\'https://github.com/PythonistaGuild/mystbin.py/workflows/Build\'>\n        <img src=\'https://github.com/PythonistaGuild/mystbin.py/workflows/Build/badge.svg\' alt=\'Build status\' />\n    </a>\n</div>\n<br>\n\nA small simple wrapper around the [Mystb.in](https://mystb.in/) API. API docs can be found [here](https://api.mystb.in/docs).\n\nDocumentation for this wrapper can be found [here](https://mystbinpy.readthedocs.io/en/stable/).\nIf you want the docs for the `main` branch, those can be found [here](https://mystbinpy.readthedocs.io/en/latest/).\n\n----------\n### Features\n\n- [x] - Creating pastes.\n- [ ] - Editing pastes.\n    - Pending design work.\n- [x] - Deleting pastes.\n- [x] - Getting pastes.\n- [ ] - User endpoints.\n- [ ] - Sync client.\n  - This one will take some time as I have no motivation to do it, but PRs are welcome if others want to do it.\n\n### Installation\nThis project will be on [PyPI](https://pypi.org/project/mystbin.py/) as a stable release, you can always find that there.\n\nInstalling via `pip`:\n```shell\npython -m pip install -U mystbin.py\n```\n\nInstalling from source:\n```shell\npython -m pip install git+https://github.com/PythonistaGuild/mystbin.py.git\n```\n\n### Usage examples\nSince the project is considered multi-sync, it will work in a sync/async environment, see the optional dependency of `requests` below.\n\n```py\n# async example - it will default to async\nimport mystbin\n\nmystbin_client = mystbin.Client()\n\npaste = await client.create_paste(filename="Hello.txt", content="Hello there!")\nstr(paste)\n>>> \'https://mystb.in/<your generated ID>\'\n\nget_paste = await mystbin_client.get_paste("<your generated ID>")\nget_paste.files[0].content\n>>> "Hello there!"\n\nget_paste.created_at\n>>> datetime.datetime(2020, 10, 6, 10, 53, 57, 556741)\n```\n\nOr if you want to create a paste with multiple files...\n```py\nimport mystbin\n\nfile = mystbin.File(filename="File1.txt", content="Hello there!")\nfile2 = mystbin.File(filename="test.py", content="print(\'hello!\')")\n\npaste = await client.create_multifile_paste(files=[file, file2])\n\nfor file in paste.files:\n    print(file.content)\n\n>>> "Hello there!"\n>>> "print(\'hello!\')"\n```\n\nIf you have any question please feel free to join the Pythonista Discord server:\n<div align="left">\n    <a href="https://discord.gg/RAKc3HF">\n        <img src="https://discordapp.com/api/guilds/490948346773635102/widget.png?style=banner2" alt="Discord Server"/>\n    </a>\n</div>\n',
-    'author': 'AbstractUmbra',
-    'author_email': 'Umbra@AbstractUmbra.dev',
-    'maintainer': 'None',
-    'maintainer_email': 'None',
-    'url': 'https://github.com/PythonistaGuild/mystbin.py',
-    'packages': packages,
-    'package_data': package_data,
-    'py_modules': modules,
-    'install_requires': install_requires,
-    'extras_require': extras_require,
-    'entry_points': entry_points,
-    'python_requires': '>=3.9,<4.0',
-}
-
-
-setup(**setup_kwargs)
```

#### html2text {}

```diff
@@ -1,47 +1,47 @@
-# -*- coding: utf-8 -*- from setuptools import setup packages = \ ['mystbin',
-'mystbin.types'] package_data = \ {'': ['*']} modules = \ ['py']
-install_requires = \ ['aiohttp>=3.7.4,<4.0.0'] extras_require = \ {'docs':
-['sphinx>=4.0.0,<5.0.0', 'sphinxcontrib-trio', 'furo'], 'requests':
-['requests>=2.24.0,<3.0.0']} entry_points = \ {'console_scripts': ['version =
-mystbin.__main__:show_version']} setup_kwargs = { 'name': 'mystbin-py',
-'version': '5.1.0', 'description': 'A small simple wrapper around the mystb.in
-API.', 'long_description': '
-                                      \n
+Metadata-Version: 2.1 Name: mystbin-py Version: 6.0.0 Summary: A small simple
+wrapper around the mystb.in API. Home-page: https://github.com/PythonistaGuild/
+mystbin.py License: MIT Keywords: mystbin,paste Author: AbstractUmbra Author-
+email: Umbra@AbstractUmbra.dev Requires-Python: >=3.8,<4.0 Classifier: Intended
+Audience :: Developers Classifier: License :: OSI Approved :: MIT License
+Classifier: Natural Language :: English Classifier: Operating System :: OS
+Independent Classifier: Programming Language :: Python :: 3 Classifier:
+Programming Language :: Python :: 3.8 Classifier: Programming Language ::
+Python :: 3.9 Classifier: Programming Language :: Python :: 3.10 Classifier:
+Programming Language :: Python :: 3.11 Classifier: Topic :: Internet
+Classifier: Typing :: Typed Provides-Extra: docs Provides-Extra: speed
+Requires-Dist: aiohttp (>=3.8,<4.0) ; extra == "speed" Requires-Dist: aiohttp
+[speedups] (>=3.8,<4.0) ; extra == "speed" Requires-Dist: furo ; extra ==
+"docs" Requires-Dist: pytz ; python_version < "3.9" Requires-Dist: sphinx
+(>=4.0.0,<5.0.0) ; extra == "docs" Requires-Dist: sphinxcontrib-trio ; extra ==
+"docs" Project-URL: Issue Tracker, https://github.com/PythonistaGuild/
+mystbin.py/issues Project-URL: Repository, https://github.com/PythonistaGuild/
+mystbin.py Description-Content-Type: text/markdown
                            ****** Mystbin.py! ******
-                    \n \n_'_/>\n\n \n_'_/>\n\n \n_'_/>\n\n
-\n
-\n\nA small simple wrapper around the [Mystb.in](https://mystb.in/) API. API
-docs can be found [here](https://api.mystb.in/docs).\n\nDocumentation for this
-wrapper can be found [here](https://mystbinpy.readthedocs.io/en/stable/).\nIf
-you want the docs for the `main` branch, those can be found [here](https://
-mystbinpy.readthedocs.io/en/latest/).\n\n----------\n### Features\n\n- [x] -
-Creating pastes.\n- [ ] - Editing pastes.\n - Pending design work.\n- [x] -
-Deleting pastes.\n- [x] - Getting pastes.\n- [ ] - User endpoints.\n- [ ] -
-Sync client.\n - This one will take some time as I have no motivation to do it,
-but PRs are welcome if others want to do it.\n\n### Installation\nThis project
-will be on [PyPI](https://pypi.org/project/mystbin.py/) as a stable release,
-you can always find that there.\n\nInstalling via `pip`:\n```shell\npython -
-m pip install -U mystbin.py\n```\n\nInstalling from source:\n```shell\npython -
-m pip install git+https://github.com/PythonistaGuild/mystbin.py.git\n```\n\n###
-Usage examples\nSince the project is considered multi-sync, it will work in a
-sync/async environment, see the optional dependency of `requests`
-below.\n\n```py\n# async example - it will default to async\nimport
-mystbin\n\nmystbin_client = mystbin.Client()\n\npaste = await
-client.create_paste(filename="Hello.txt", content="Hello there!")\nstr
-(paste)\n>>> \'https://mystb.in/\'\n\nget_paste = await
-mystbin_client.get_paste("")\nget_paste.files[0].content\n>>> "Hello
-there!"\n\nget_paste.created_at\n>>> datetime.datetime(2020, 10, 6, 10, 53, 57,
-556741)\n```\n\nOr if you want to create a paste with multiple
-files...\n```py\nimport mystbin\n\nfile = mystbin.File(filename="File1.txt",
-content="Hello there!")\nfile2 = mystbin.File(filename="test.py",
-content="print(\'hello!\')")\n\npaste = await client.create_multifile_paste
-(files=[file, file2])\n\nfor file in paste.files:\n print(file.content)\n\n>>>
-"Hello there!"\n>>> "print(\'hello!\')"\n```\n\nIf you have any question please
-feel free to join the Pythonista Discord server:\n
-\n \n_[Discord_Server]\n\n
-\n', 'author': 'AbstractUmbra', 'author_email': 'Umbra@AbstractUmbra.dev',
-'maintainer': 'None', 'maintainer_email': 'None', 'url': 'https://github.com/
-PythonistaGuild/mystbin.py', 'packages': packages, 'package_data':
-package_data, 'py_modules': modules, 'install_requires': install_requires,
-'extras_require': extras_require, 'entry_points': entry_points,
-'python_requires': '>=3.9,<4.0', } setup(**setup_kwargs)
+            [Documentation_Status] [Linting_status] [Build_status]
+
+A small simple wrapper around the [Mystb.in](https://mystb.in/) API. API docs
+can be found [here](https://api.mystb.in/docs). Documentation for this wrapper
+can be found [here](https://mystbinpy.readthedocs.io/en/stable/). If you want
+the docs for the `main` branch, those can be found [here](https://
+mystbinpy.readthedocs.io/en/latest/). ---------- ### Features - [x] - Creating
+pastes. - [ ] - Editing pastes. - Pending design work. - [x] - Deleting pastes.
+- [x] - Getting pastes. - [ ] - User endpoints. - [ ] - Sync client. - This one
+will take some time as I have no motivation to do it, but PRs are welcome if
+others want to do it. ### Installation This project will be on [PyPI](https://
+pypi.org/project/mystbin.py/) as a stable release, you can always find that
+there. Installing via `pip`: ```shell python -m pip install -U mystbin.py ```
+Installing from source: ```shell python -m pip install git+https://github.com/
+PythonistaGuild/mystbin.py.git ``` ### Usage examples ```py # async example -
+it will default to async import mystbin client = mystbin.Client() paste = await
+client.create_paste(filename="Hello.txt", content="Hello there!") # we also
+support passing a mystbin.File directly to the `file=` kwarg! str(paste) >>>
+'https://mystb.in/' get_paste = await client.get_paste("") get_paste.files
+[0].content >>> "Hello there!" get_paste.created_at >>> datetime.datetime(2020,
+10, 6, 10, 53, 57, 556741) ``` Or if you want to create a paste with multiple
+files... ```py import mystbin file = mystbin.File(filename="File1.txt",
+content="Hello there!") file2 = mystbin.File(filename="test.py", content="print
+('hello!')") paste = await client.create_paste(files=[file, file2]) for file in
+paste.files: print(file.content) >>> "Hello there!" >>> "print('hello!')" ```
+If you have any question please feel free to join the Pythonista Discord
+server:
+[Discord_Server]
```

