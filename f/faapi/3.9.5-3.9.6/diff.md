# Comparing `tmp/faapi-3.9.5.tar.gz` & `tmp/faapi-3.9.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "faapi-3.9.5.tar", max compression
+gzip compressed data, was "faapi-3.9.6.tar", max compression
```

## Comparing `faapi-3.9.5.tar` & `faapi-3.9.6.tar`

### file list

```diff
@@ -1,15 +1,15 @@
--rw-r--r--   0        0        0    13866 2022-11-04 13:46:51.408650 faapi-3.9.5/LICENSE
--rw-r--r--   0        0        0    29741 2022-11-04 13:46:51.408650 faapi-3.9.5/README.md
--rw-r--r--   0        0        0      506 2022-11-04 13:46:51.408650 faapi-3.9.5/faapi/__init__.py
--rw-r--r--   0        0        0       22 2022-11-04 13:46:51.408650 faapi-3.9.5/faapi/__version__.py
--rw-r--r--   0        0        0    13696 2022-11-04 13:46:51.412650 faapi-3.9.5/faapi/base.py
--rw-r--r--   0        0        0     6129 2022-11-04 13:46:51.412650 faapi-3.9.5/faapi/comment.py
--rw-r--r--   0        0        0     2420 2022-11-04 13:46:51.412650 faapi-3.9.5/faapi/connection.py
--rw-r--r--   0        0        0      883 2022-11-04 13:46:51.412650 faapi-3.9.5/faapi/exceptions.py
--rw-r--r--   0        0        0     7565 2022-11-04 13:46:51.412650 faapi-3.9.5/faapi/journal.py
--rw-r--r--   0        0        0    39251 2022-11-04 13:46:51.412650 faapi-3.9.5/faapi/parse.py
--rw-r--r--   0        0        0     9573 2022-11-04 13:46:51.412650 faapi-3.9.5/faapi/submission.py
--rw-r--r--   0        0        0     7857 2022-11-04 13:46:51.412650 faapi-3.9.5/faapi/user.py
--rw-r--r--   0        0        0     1410 2022-11-04 13:46:51.412650 faapi-3.9.5/pyproject.toml
--rw-r--r--   0        0        0    31237 1970-01-01 00:00:00.000000 faapi-3.9.5/setup.py
--rw-r--r--   0        0        0    31338 1970-01-01 00:00:00.000000 faapi-3.9.5/PKG-INFO
+-rw-r--r--   0        0        0    13866 2022-11-18 20:50:43.226128 faapi-3.9.6/LICENSE
+-rw-r--r--   0        0        0    29741 2022-11-18 20:50:43.226128 faapi-3.9.6/README.md
+-rw-r--r--   0        0        0      506 2022-11-18 20:50:43.226128 faapi-3.9.6/faapi/__init__.py
+-rw-r--r--   0        0        0       22 2022-11-18 20:50:43.226128 faapi-3.9.6/faapi/__version__.py
+-rw-r--r--   0        0        0    13716 2022-11-18 20:50:43.230129 faapi-3.9.6/faapi/base.py
+-rw-r--r--   0        0        0     6176 2022-11-18 20:50:43.230129 faapi-3.9.6/faapi/comment.py
+-rw-r--r--   0        0        0     2440 2022-11-18 20:50:43.230129 faapi-3.9.6/faapi/connection.py
+-rw-r--r--   0        0        0      883 2022-11-18 20:50:43.230129 faapi-3.9.6/faapi/exceptions.py
+-rw-r--r--   0        0        0     7605 2022-11-18 20:50:43.230129 faapi-3.9.6/faapi/journal.py
+-rw-r--r--   0        0        0    39329 2022-11-18 20:50:43.230129 faapi-3.9.6/faapi/parse.py
+-rw-r--r--   0        0        0     9613 2022-11-18 20:50:43.230129 faapi-3.9.6/faapi/submission.py
+-rw-r--r--   0        0        0     7897 2022-11-18 20:50:43.230129 faapi-3.9.6/faapi/user.py
+-rw-r--r--   0        0        0     1410 2022-11-18 20:50:43.230129 faapi-3.9.6/pyproject.toml
+-rw-r--r--   0        0        0    31237 1970-01-01 00:00:00.000000 faapi-3.9.6/setup.py
+-rw-r--r--   0        0        0    31338 1970-01-01 00:00:00.000000 faapi-3.9.6/PKG-INFO
```

### Comparing `faapi-3.9.5/LICENSE` & `faapi-3.9.6/LICENSE`

 * *Files identical despite different names*

### Comparing `faapi-3.9.5/README.md` & `faapi-3.9.6/README.md`

 * *Files identical despite different names*

### Comparing `faapi-3.9.5/faapi/base.py` & `faapi-3.9.6/faapi/base.py`

 * *Files 1% similar despite different names*

```diff
@@ -163,29 +163,29 @@
 
         :return: A list of SubmissionPartial objects
         """
         page_parsed: BeautifulSoup = self.get_parsed("/")
         submissions: list[SubmissionPartial] = [SubmissionPartial(f) for f in parse_submission_figures(page_parsed)]
         return sorted({s for s in submissions}, reverse=True)
 
-    def submission(self, submission_id: int, get_file: bool = False, *, chunk_size: int = None
+    def submission(self, submission_id: int, get_file: bool = False, *, chunk_size: Optional[int] = None
                    ) -> tuple[Submission, Optional[bytes]]:
         """
         Fetch a submission and, optionally, its file.
 
         :param submission_id: The ID of the submission.
         :param get_file: Whether to download the submission file.
         :param chunk_size: The chunk_size to be used for the download (does not override get_file).
         :return: A Submission object and a bytes object (if the submission file is downloaded).
         """
         sub: Submission = Submission(self.get_parsed(join_url("view", int(submission_id))))
         sub_file: Optional[bytes] = self.submission_file(sub, chunk_size=chunk_size) if get_file and sub.id else None
         return sub, sub_file
 
-    def submission_file(self, submission: Submission, *, chunk_size: int = None) -> bytes:
+    def submission_file(self, submission: Submission, *, chunk_size: Optional[int] = None) -> bytes:
         """
         Fetch a submission file from a Submission object.
 
         :param submission: A Submission object.
         :param chunk_size: The chunk_size to be used for the download.
         :return: The submission file as a bytes object.
         """
```

### Comparing `faapi-3.9.5/faapi/comment.py` & `faapi-3.9.6/faapi/comment.py`

 * *Files 3% similar despite different names*

```diff
@@ -11,15 +11,16 @@
 
 
 class Comment:
     """
     Contains comment information and references to replies and parent objects.
     """
 
-    def __init__(self, tag: Tag = None, parent: Union[faapi.submission.Submission, faapi.journal.Journal] = None):
+    def __init__(self, tag: Optional[Tag] = None,
+                 parent: Optional[Union[faapi.submission.Submission, faapi.journal.Journal]] = None):
         """
         :param tag: The comment tag from which to parse information
         :param parent: The parent object of the comment
         """
         assert tag is None or isinstance(tag, Tag), _raise_exception(TypeError(f"tag must be {None} or {Tag.__name__}"))
 
         self.comment_tag: Optional[Tag] = tag
@@ -106,15 +107,15 @@
         """
         Compose the full URL to the comment.
 
         :return: The URL to the comment.
         """
         return "" if self.parent is None else f"{self.parent.url}#cid:{self.id}"
 
-    def parse(self, comment_tag: Tag = None):
+    def parse(self, comment_tag: Optional[Tag] = None):
         """
         Parse a comment tag, overrides any information already present in the object.
 
         :param comment_tag: The comment tag from which to parse information
         """
         assert comment_tag is None or isinstance(comment_tag, Tag), \
             _raise_exception(TypeError(f"tag must be {None} or {Tag.__name__}"))
```

### Comparing `faapi-3.9.5/faapi/connection.py` & `faapi-3.9.6/faapi/connection.py`

 * *Files 3% similar despite different names*

```diff
@@ -46,16 +46,16 @@
 
 def get_robots(session: Session) -> RobotFileParser:
     robots: RobotFileParser = RobotFileParser(url := join_url(root, "robots.txt"))
     robots.parse(filter(re_compile(r"^[^#\s].+").match, map(str.strip, session.get(url).text.splitlines())))
     return robots
 
 
-def get(session: CloudflareScraper, path: str, *, timeout: int = None,
-        params: dict[str, Union[str, bytes, int, float]] = None) -> Response:
+def get(session: CloudflareScraper, path: str, *, timeout: Optional[int] = None,
+        params: Optional[dict[str, Union[str, bytes, int, float]]] = None) -> Response:
     return session.get(join_url(root, path), params=params, timeout=timeout)
 
 
 def stream_binary(session: CloudflareScraper, url: str, *, chunk_size: Optional[int] = None,
                   timeout: Optional[int] = None) -> bytes:
     stream: Response = session.get(url, stream=True, timeout=timeout)
     stream.raise_for_status()
```

### Comparing `faapi-3.9.5/faapi/exceptions.py` & `faapi-3.9.6/faapi/exceptions.py`

 * *Files identical despite different names*

### Comparing `faapi-3.9.5/faapi/journal.py` & `faapi-3.9.6/faapi/journal.py`

 * *Files 9% similar despite different names*

```diff
@@ -106,27 +106,27 @@
 
 
 class JournalPartial(JournalBase):
     """
     Contains partial journal information gathered from journals pages.
     """
 
-    def __init__(self, journal_tag: Tag = None):
+    def __init__(self, journal_tag: Optional[Tag] = None):
         """
         :param journal_tag: The tag from which to parse the journal.
         """
         assert journal_tag is None or isinstance(journal_tag, Tag), \
             _raise_exception(TypeError(f"journal_item must be {None} or {Tag.__name__}"))
         self.journal_tag: Optional[Tag] = journal_tag
 
         super(JournalPartial, self).__init__()
 
         self.parse()
 
-    def parse(self, journal_tag: Union[Tag, BeautifulSoup] = None):
+    def parse(self, journal_tag: Optional[Union[Tag, BeautifulSoup]] = None):
         """
         Parse a journal tag, overrides any information already present in the object.
 
         :param journal_tag: The tag from which to parse the journal.
         """
         assert journal_tag is None or isinstance(journal_tag, BeautifulSoup), \
             _raise_exception(TypeError(f"journal_item must be {None} or {BeautifulSoup.__name__}"))
@@ -152,15 +152,15 @@
 
 
 class Journal(JournalBase):
     """
     Contains complete journal information gathered from journal pages, including comments.
     """
 
-    def __init__(self, journal_page: BeautifulSoup = None):
+    def __init__(self, journal_page: Optional[BeautifulSoup] = None):
         """
         :param journal_page: The page from which to parse the journal.
         """
         assert journal_page is None or isinstance(journal_page, BeautifulSoup), \
             _raise_exception(TypeError(f"journal_item must be {None} or {BeautifulSoup.__name__}"))
         self.journal_page: Optional[BeautifulSoup] = journal_page
 
@@ -195,15 +195,15 @@
         """
         The journal footer formatted to BBCode
 
         :return: BBCode footer
         """
         return html_to_bbcode(self.footer)
 
-    def parse(self, journal_page: Union[Tag, BeautifulSoup] = None):
+    def parse(self, journal_page: Optional[Union[Tag, BeautifulSoup]] = None):
         """
         Parse a journal page, overrides any information already present in the object.
 
         :param journal_page: The page from which to parse the journal.
         """
         assert journal_page is None or isinstance(journal_page, BeautifulSoup), \
             _raise_exception(TypeError(f"journal_item must be {None} or {BeautifulSoup.__name__}"))
```

### Comparing `faapi-3.9.5/faapi/parse.py` & `faapi-3.9.6/faapi/parse.py`

 * *Files 1% similar despite different names*

```diff
@@ -343,15 +343,15 @@
 def parse_loggedin_user(page: BeautifulSoup) -> Optional[str]:
     return get_attr(avatar, "alt") if (avatar := page.select_one("img.loggedin_user_avatar")) else None
 
 
 def parse_journal_section(section_tag: Tag) -> dict[str, Any]:
     id_: int = int(section_tag.attrs.get("id", "00000")[4:])
     tag_title: Optional[Tag] = section_tag.select_one("h2")
-    tag_date: Optional[Tag] = section_tag.select_one("span.popup_date")
+    tag_date: Optional[Tag] = section_tag.select_one("div.section-header span.popup_date")
     tag_content: Optional[Tag] = section_tag.select_one("div.journal-body")
     tag_comments: Optional[Tag] = section_tag.select_one("div.section-footer > a > span")
 
     assert id_ != 0, _raise_exception(ParsingError("Missing ID"))
     assert tag_title is not None, _raise_exception(ParsingError("Missing title tag"))
     assert tag_date is not None, _raise_exception(ParsingError("Missing date tag"))
     assert tag_content is not None, _raise_exception(ParsingError("Missing content tag"))
@@ -378,15 +378,15 @@
     }
 
 
 def parse_journal_page(journal_page: BeautifulSoup) -> dict[str, Any]:
     user_info: dict[str, str] = parse_user_folder(journal_page)
     tag_id: Optional[Tag] = journal_page.select_one("meta[property='og:url']")
     tag_title: Optional[Tag] = journal_page.select_one("h2.journal-title")
-    tag_date: Optional[Tag] = journal_page.select_one("span.popup_date")
+    tag_date: Optional[Tag] = journal_page.select_one("div.content div.section-header span.popup_date")
     tag_header: Optional[Tag] = journal_page.select_one("div.journal-header")
     tag_footer: Optional[Tag] = journal_page.select_one("div.journal-footer")
     tag_content: Optional[Tag] = journal_page.select_one("div.journal-content")
     tag_comments: Optional[Tag] = journal_page.select_one("div.section-footer > span")
 
     assert tag_id is not None, _raise_exception(ParsingError("Missing ID tag"))
     assert tag_title is not None, _raise_exception(ParsingError("Missing title tag"))
@@ -479,15 +479,15 @@
     tag_id: Optional[Tag] = sub_page.select_one("meta[property='og:url']")
     tag_sub_info: Optional[Tag] = sub_page.select_one("div.submission-id-sub-container")
 
     assert tag_sub_info is not None, _raise_exception(ParsingError("Missing info tag"))
 
     tag_title: Optional[Tag] = tag_sub_info.select_one("div.submission-title")
     tag_author: Optional[Tag] = sub_page.select_one("div.submission-id-container")
-    tag_date: Optional[Tag] = sub_page.select_one("span.popup_date")
+    tag_date: Optional[Tag] = sub_page.select_one("div.submission-id-container span.popup_date")
     tag_tags: list[Tag] = sub_page.select("section.tags-row a")
     tag_views: Optional[Tag] = sub_page.select_one("div.views span")
     tag_comment_count: Optional[Tag] = sub_page.select_one("section.stats-container div.comments span")
     tag_favorites: Optional[Tag] = sub_page.select_one("div.favorites span")
     tag_rating: Optional[Tag] = sub_page.select_one("div.rating span")
     tag_type: Optional[Tag] = sub_page.select_one("div#submission_page[class^='page-content-type']")
     tag_fav: Optional[Tag] = sub_page.select_one("div.fav > a")
```

### Comparing `faapi-3.9.5/faapi/submission.py` & `faapi-3.9.6/faapi/submission.py`

 * *Files 1% similar despite different names*

```diff
@@ -103,15 +103,15 @@
 
 
 class SubmissionPartial(SubmissionBase):
     """
     Contains partial submission information gathered from submissions pages (gallery, scraps, etc.).
     """
 
-    def __init__(self, submission_figure: Tag = None):
+    def __init__(self, submission_figure: Optional[Tag] = None):
         """
         :param submission_figure: The figure tag from which to parse the submission information.
         """
         assert submission_figure is None or isinstance(submission_figure, Tag), \
             _raise_exception(TypeError(f"submission_figure must be {None} or {BeautifulSoup.__name__}"))
 
         super().__init__()
@@ -127,15 +127,15 @@
         yield "id", self.id
         yield "title", self.title
         yield "author", dict(self.author)
         yield "rating", self.rating
         yield "type", self.type
         yield "thumbnail_url", self.thumbnail_url
 
-    def parse(self, submission_figure: Tag = None):
+    def parse(self, submission_figure: Optional[Tag] = None):
         """
         Parse a submission figure Tag, overrides any information already present in the object.
 
         :param submission_figure: The optional figure tag from which to parse the submission.
         """
         assert submission_figure is None or isinstance(submission_figure, Tag), \
             _raise_exception(TypeError(f"submission_figure must be {None} or {BeautifulSoup.__name__}"))
@@ -155,15 +155,15 @@
 
 
 class Submission(SubmissionBase):
     """
     Contains complete submission information gathered from submission pages, including comments.
     """
 
-    def __init__(self, submission_page: BeautifulSoup = None):
+    def __init__(self, submission_page: Optional[BeautifulSoup] = None):
         """
         :param submission_page: The page from which to parse the submission information.
         """
         assert submission_page is None or isinstance(submission_page, BeautifulSoup), \
             _raise_exception(TypeError(f"submission_page must be {None} or {BeautifulSoup.__name__}"))
 
         super().__init__()
@@ -233,15 +233,15 @@
         """
         The submission footer formatted to BBCode
 
         :return: BBCode footer
         """
         return html_to_bbcode(self.footer)
 
-    def parse(self, submission_page: BeautifulSoup = None):
+    def parse(self, submission_page: Optional[BeautifulSoup] = None):
         """
         Parse a submission page, overrides any information already present in the object.
 
         :param submission_page: The optional page from which to parse the submission.
         """
         assert submission_page is None or isinstance(submission_page, BeautifulSoup), \
             _raise_exception(TypeError(f"submission_page must be {None} or {BeautifulSoup.__name__}"))
```

### Comparing `faapi-3.9.5/faapi/user.py` & `faapi-3.9.6/faapi/user.py`

 * *Files 6% similar despite different names*

```diff
@@ -115,15 +115,15 @@
 
 
 class UserPartial(UserBase):
     """
     Contains partial user information gathered from user folders (gallery, journals, etc.) and submission/journal pages.
     """
 
-    def __init__(self, user_tag: Tag = None):
+    def __init__(self, user_tag: Optional[Tag] = None):
         """
         :param user_tag: The tag from which to parse the user information.
         """
         assert user_tag is None or isinstance(user_tag, Tag), \
             _raise_exception(TypeError(f"user_tag must be {None} or {Tag.__name__}"))
 
         super().__init__()
@@ -138,15 +138,15 @@
     def __iter__(self):
         yield "name", self.name
         yield "status", self.status
         yield "title", self.title
         yield "join_date", self.join_date
         yield "user_icon_url", self.user_icon_url
 
-    def parse(self, user_tag: Tag = None):
+    def parse(self, user_tag: Optional[Tag] = None):
         """
         Parse a user page, overrides any information already present in the object.
 
         :param user_tag: The tag from which to parse the user information.
         """
         assert user_tag is None or isinstance(user_tag, Tag), \
             _raise_exception(TypeError(f"user_tag must be {None} or {Tag.__name__}"))
@@ -164,15 +164,15 @@
 
 
 class User(UserBase):
     """
     Contains complete user information gathered from userpages.
     """
 
-    def __init__(self, user_page: BeautifulSoup = None):
+    def __init__(self, user_page: Optional[BeautifulSoup] = None):
         """
         :param user_page: The page from which to parse the user information.
         """
         assert user_page is None or isinstance(user_page, BeautifulSoup), \
             _raise_exception(TypeError(f"user_page must be {None} or {BeautifulSoup.__name__}"))
 
         super().__init__()
@@ -212,15 +212,15 @@
         """
         The user profile text formatted to BBCode
 
         :return: BBCode profile
         """
         return html_to_bbcode(self.profile)
 
-    def parse(self, user_page: BeautifulSoup = None):
+    def parse(self, user_page: Optional[BeautifulSoup] = None):
         """
         Parse a user page, overrides any information already present in the object.
 
         :param user_page: The page from which to parse the user information.
         """
         assert user_page is None or isinstance(user_page, BeautifulSoup), \
             _raise_exception(TypeError(f"user_page must be {None} or {BeautifulSoup.__name__}"))
```

### Comparing `faapi-3.9.5/pyproject.toml` & `faapi-3.9.6/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "faapi"
-version = "3.9.5"
+version = "3.9.6"
 description = "Python module to implement API-like functionality for the FurAffinity.net website."
 authors = ["Matteo Campinoti <matteo.campinoti94@gmail.com>"]
 license = "EUPL-1.2"
 readme = "README.md"
 homepage = "https://github.com/FurryCoders/FAAPI"
 repository = "https://github.com/FurryCoders/FAAPI"
 classifiers = [
@@ -32,14 +32,14 @@
 lxml = "^4.9.1"
 python-dateutil = "^2.8.2"
 htmlmin = "^0.1.12"
 bbcode = "^1.1.0"
 
 [tool.poetry.group.test.dependencies]
 pytest = "^7.2.0"
-mypy = "^0.982"
+mypy = "^0.991"
 types-beautifulsoup4 = "^4.11.6"
 flake8 = "^5.0.4"
 
 [build-system]
 requires = ["poetry>=0.12"]
 build-backend = "poetry.masonry.api"
```

### Comparing `faapi-3.9.5/setup.py` & `faapi-3.9.6/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -14,15 +14,15 @@
  'htmlmin>=0.1.12,<0.2.0',
  'lxml>=4.9.1,<5.0.0',
  'python-dateutil>=2.8.2,<3.0.0',
  'requests>=2.28.1,<3.0.0']
 
 setup_kwargs = {
     'name': 'faapi',
-    'version': '3.9.5',
+    'version': '3.9.6',
     'description': 'Python module to implement API-like functionality for the FurAffinity.net website.',
     'long_description': '<div align="center">\n\n<img alt="logo" width="400" src="https://raw.githubusercontent.com/FurryCoders/Logos/main/logos/faapi-transparent.png">\n\n# Fur Affinity API\n\nPython library to implement API-like functionality for the [Fur Affinity](https://furaffinity.net) website.\n\n[![](https://img.shields.io/pypi/v/faapi?logo=pypi)](https://pypi.org/project/faapi/)\n[![](https://img.shields.io/pypi/pyversions/faapi?logo=Python)](https://www.python.org)\n\n[![](https://img.shields.io/github/v/tag/FurryCoders/faapi?label=github&sort=date&logo=github&color=blue)](https://github.com/FurryCoders/faapi)\n[![](https://img.shields.io/github/issues/FurryCoders/faapi?logo=github&color=blue)](https://github.com/FurryCoders/FAAPI/issues)\n[![](https://img.shields.io/github/workflow/status/FurryCoders/FAAPI/Test?label=Test&logo=githubactions)](https://github.com/FurryCoders/FAAPI/actions/workflows/test.yml)\n\n</div>\n\n## Requirements\n\nPython 3.9+ is necessary to run this\nlibrary. [<img src="https://python-poetry.org/images/logo-origami.svg" height="12"> Poetry](https://python-poetry.org)\nis used for packaging and dependency management.\n\n## Usage\n\nThe API comprises a main class `FAAPI`, two submission classes `Submission` and `SubmissionPartial`, a journal\nclass `Journal`, and a user class `User`.\n\nOnce `FAAPI` is initialized, its methods can be used to crawl FA and return parsed objects.\n\n```python\nfrom requests.cookies import RequestsCookieJar\nimport faapi\nimport orjson\n\ncookies = RequestsCookieJar()\ncookies.set("a", "38565475-3421-3f21-7f63-3d341339737")\ncookies.set("b", "356f5962-5a60-0922-1c11-65003b70308")\n\napi = faapi.FAAPI(cookies)\nsub, sub_file = api.submission(12345678, get_file=True)\n\nprint(sub.id, sub.title, sub.author, f"{len(sub_file) / 1024:02f}KiB")\n\nwith open(f"{sub.id}.json", "wb") as f:\n    f.write(orjson.dumps(dict(sub)))\n\nwith open(sub.file_url.split("/")[-1], "wb") as f:\n    f.write(sub_file)\n\ngallery, _ = api.gallery("user_name", 1)\nwith open("user_name-gallery.json", "wb") as f:\n    f.write(orjson.dumps(list(map(dict, gallery))))\n```\n\n### robots.txt\n\nAt init, the `FAAPI` object downloads the [robots.txt](https://www.furaffinity.net/robots.txt) file from FA to determine\nthe `Crawl-delay` and `disallow` values set therein. If not set in the robots.txt file, a crawl delay value of 1 second\nis used.\n\nTo respect this value, the default behaviour of the `FAAPI` object is to wait when a get request is made if the last\nrequest was performed more recently then the crawl delay value.\n\nSee under [FAAPI](#faapi) for more details on this behaviour.\n\nFurthermore, any get operation that points to a disallowed path from robots.txt will raise an exception. This check\nshould not be circumvented, and the developer of this library does not take responsibility for violations of the TOS of\nFur Affinity.\n\n### Cookies\n\nTo access protected pages, cookies from an active session are needed. These cookies can be given to the FAAPI object as\na list of dictionaries - each containing a `name` and a `value` field -, or as a `http.cookiejar.CookieJar`\nobject (`requests.cookies.RequestsCookieJar` and other objects inheriting from `CookieJar` are also supported). The\ncookies list should look like the following example:\n\n```python\ncookies = [\n    {"name": "a", "value": "38565475-3421-3f21-7f63-3d3413397537"},\n    {"name": "b", "value": "356f5962-5a60-0922-1c11-65003b703038"},\n]\n```\n\n```python\nfrom requests.cookies import RequestsCookieJar\n\ncookies = RequestsCookieJar()\ncookies.set("a", "38565475-3421-3f21-7f63-3d3413397537")\ncookies.set("b", "356f5962-5a60-0922-1c11-65003b703038")\n```\n\nTo access session cookies, consult the manual of the browser used to log in.\n\n*Note:* it is important to not logout of the session the cookies belong to, otherwise they will no longer work.<br/>\n*Note:* as of April 2022 only cookies `a` and `b` are needed.\n\n### User Agent\n\n`FAAPI` attaches a `User-Agent` header to every request. The user agent string is generated at startup in the following\nformat: `faapi/{library version} Python/{python version} {system name}/{system release}`.\n\n## Objects\n\n### FAAPI\n\nThis is the main object that handles all the calls to scrape pages and get submissions.\n\nIt holds 6 different fields:\n\n* `session: CloudflareScraper` `cfscrape` session used for get requests\n* `robots: urllib.robotparser.RobotFileParser` robots.txt handler\n* `user_agent: str` user agent used by the session (property, cannot be set)\n* `crawl_delay: float` crawl delay from robots.txt (property, cannot be set)\n* `last_get: float` time of last get (UNIX time)\n* `raise_for_unauthorized: bool = True` if set to `True`, raises an exception if a request is made and the resulting\n  page is not from a login session\n* `timeout: int | None = None` requests timeout in seconds for both page requests (e.g. submissions) and files\n\n#### Init\n\n`__init__(cookies: list[dict[str, str]] | CookieJar)`\n\nThe class init has a single argument for the cookies. Cookies must be in the format mentioned above\nin [#Cookies](#cookies).\n\n#### Methods & Properties\n\n* `load_cookies(cookies: list[dict[str, str]] | CookieJar)`<br/>\n  Load new cookies and create a new session.<br/>\n  *Note:* This method removes any cookies currently in use, to update/add single cookies access them from the session\n  object.\n* `handle_delay()`<br/>\n  Handles the crawl delay as set in the robots.txt\n* `check_path(path: str, *, raise_for_disallowed: bool = False) -> bool`<br/>\n  Checks whether a given path is allowed by the robots.txt. If `raise_for_disallowed` is set to `True`\n  a `DisallowedPath` exception is raised on non-allowed paths.\n* `connection_status -> bool`<br/>\n  Returns the status of the connection.\n* `login_status -> bool`<br/>\n  Returns the login status.\n* `get(path: str, **params) -> requests.Response`<br/>\n  This returns a response object containing the result of the get operation on the given URL with the\n  optional `**params` added to it (url provided is considered as path from \'https://www.furaffinity.net/\').\n* `get_parsed(path: str, *, skip_page_check: bool = False, skip_auth_check: bool = False, **params) -> bs4.BeautifulSoup`<br/>\n  Similar to `get()` but returns the parsed HTML from the normal get operation. If the GET request encountered an error,\n  an `HTTPError` exception is raised. If `skip_page_check` is set to `True`, the parsed page is not checked for errors (\n  e.g. non-existing submission). If `skip_auth_check` is set to `True`, the page is not checked for login status.\n* `me() -> User | None`<br/>\n  Returns the logged-in user as a `User` object if the cookies are from a login session.\n* `frontpage() -> list[SubmissionPartial]`<br/>\n  Fetch the latest submissions from Fur Affinity\'s front page.\n* `submission(submission_id: int, get_file: bool = False, *, chunk_size: int = None) -> tuple[Submission, bytes | None]`<br/>\n  Given a submission ID, it returns a `Submission` object containing the various metadata of the submission itself and\n  a `bytes` object with the submission file if `get_file` is passed as `True`. The optional `chunk_size` argument is\n  used for the request; if left to `None` or set to 0 the download is performed directly without streaming.<br/>\n  *Note:* the author `UserPartial` object of the submission does not contain the `join_date` field as it does not appear\n  on submission pages.\n* `submission_file(submission: Submission, *, chunk_size: int = None) -> bytes`<br/>\n  Given a submission object, it downloads its file and returns it as a `bytes` object. The optional `chunk_size`\n  argument is used for the request; if left to `None` or set to 0 the download is performed directly without streaming.\n* `journal(journal_id: int) -> Journal`<br/>\n  Given a journal ID, it returns a `Journal` object containing the various metadata of the journal.\n* `user(user: str) -> User`<br/>\n  Given a username, it returns a `User` object containing information regarding the user.\n* `gallery(user: str, page: int = 1) -> tuple[list[SubmissionPartial], int | None]`<br/>\n  Returns the list of submissions found on a specific gallery page, and the number of the next page. The returned page\n  number is set to `None` if it is the last page.\n* `scraps(user: str, page: int = 1) -> -> tuple[list[SubmissionPartial], int | None]`<br/>\n  Returns the list of submissions found on a specific scraps page, and the number of the next page. The returned page\n  number is set to `None` if it is the last page.\n* `favorites(user: str, page: str = "") -> tuple[list[SubmissionPartial], str | None]`<br/>\n  Downloads a user\'s favorites page. Because of how favorites pages work on FA, the `page` argument (and the one\n  returned) are strings. If the favorites page is the last then a `None` is returned as next page. An empty page\n  value as argument is equivalent to page 1.<br/>\n  *Note:* favorites page "numbers" do not follow any scheme and are only generated server-side.\n* `journals(user: str, page: int = 1) -> -> tuple[list[JournalPartial], int | None]`<br/>\n  Returns the list of submissions found on a specific journals page, and the number of the next page. The returned page\n  number is set to `None` if it is the last page.\n* `watchlist_to(self, user: str, page:int = 1) -> tuple[list[UserPartial], int | None]`<br/>\n  Given a username, returns a list of `UserPartial` objects for each user that is watching the given user and the next\n  page, if it is not the last, in which case a `None` is returned.\n* `watchlist_by(self, user: str, page:int = 1) -> tuple[list[UserPartial], int | None]`<br/>\n  Given a username, returns a list of `UserPartial` objects for each user that is watched by the given user and the next\n  page, if it is not the last, in which case a `None` is returned.\n\n*Note:* The last page returned by the `watchlist_to` and `watchlist_by` may not be correct as Fur Affinity doesn\'t seem\nto have a consistent behaviour when rendering the next page button, as such it is safer to use an external algorithm to\ncheck whether the method is advancing the page but returning the same/no users.\n\n### UserPartial\n\nA stripped-down class that holds basic user information. It is used to hold metadata gathered when parsing a submission,\njournal, gallery, scraps, etc.\n\n* `name: str` display name with capital letters and extra characters such as "_"\n* `status: str` user status (~, !, etc.)\n* `title: str` the user title as it appears on their userpage\n* `join_date: datetime` the date the user joined (defaults to timestamp 0)\n* `user_tag: bs4.element.Tag` the user element used to parse information (placeholder, `UserPartial` is filled\n  externally)\n\n`UserPartial` objects can be directly cast to a dict object and iterated through.\n\nComparison with `UserPartial` can be made with either another `UserPartial` or `User` object (the URL names are\ncompared), or a string (the URL name is compared to the given string).\n\n#### Init\n\n`__init__(user_tag: bs4.element.Tag = None)`\n\nTo initialise the object, an optional `bs4.element.Tag` object is needed containing the user element from a user page or\nuser folder.\n\nIf no `user_tag` is passed then the object fields will remain at their default - empty - value.\n\n#### Methods\n\n* `name_url -> str`<br/>\n  Property method that returns the URL-safe username\n* `url -> str`<br/>\n  Property method that returns the Fur Affinity URL to the user (`https://www.furaffinity.net/user/{name_url}`).\n* `generate_user_icon_url() -> str`<br/>\n  Generates the URl for the current user icon.\n* `parse(user_page: bs4.BeautifulSoup = None)`<br/>\n  Parses the stored user page for metadata. If `user_page` is passed, it overwrites the existing `user_page` value.\n\n### User\n\nThe main class storing all of a user\'s metadata.\n\n* `name: str` display name with capital letters and extra characters such as "_"\n* `status: str` user status (~, !, etc.)\n* `title: str` the user title as it appears on their userpage\n* `join_date: datetime` the date the user joined (defaults to timestamp 0)\n* `profile: str` profile text in HTML format\n* `profile_bbcode: str` profile text in BBCode format\n* `stats: UserStats` user statistics sorted in a `namedtuple` (`views`, `submissions`, `favorites`, `comments_earned`\n  , `comments_made`, `journals`, `watched_by`, `watching`)\n* `info: dict[str, str]` profile information (e.g. "Accepting Trades", "Accepting Commissions", "Character Species",\n  etc.)\n* `contacts: dict[str, str]` contact links (e.g. Twitter, Steam, etc.)\n* `user_icon_url: str` the URL to the user icon\n* `watched: bool` `True` if the user is watched, `False` otherwise\n* `watched_toggle_link: str | None` The link to toggle the watch status (`/watch/` or `/unwatch/` type link)\n* `blocked: bool` `True` if the user is blocked, `False` otherwise\n* `blocked_toggle_link: str | None` The link to toggle the block status (`/block/` or `/unblock/` type link)\n* `user_page: bs4.BeautifulSoup` the user page used to parse the object fields\n\n`User` objects can be directly cast to a dict object and iterated through.\n\nComparison with `User` can be made with either another `User` or `UserPartial` object (the URL names are compared), or a\nstring (the URL name is compared to the given string).\n\n#### Init\n\n`__init__(user_page: bs4.BeautifulSoup = None)`\n\nTo initialise the object, an optional `bs4.BeautifulSoup` object is needed containing the parsed HTML of a submission\npage.\n\nIf no `user_page` is passed then the object fields will remain at their default - empty - value.\n\n#### Methods\n\n* `name_url -> str`<br/>\n  Property method that returns the URL-safe username\n* `url -> str`<br/>\n  Property method that returns the Fur Affinity URL to the user (`https://www.furaffinity.net/user/{name_url}`).\n* `generate_user_icon_url() -> str`<br/>\n  Generates the URl for the current user icon.\n* `parse(user_page: bs4.BeautifulSoup = None)`<br/>\n  Parses the stored user page for metadata. If `user_page` is passed, it overwrites the existing `user_page` value.\n\n### JournalPartial\n\nThis object contains partial information gathered when parsing a journals folder. It contains the following fields:\n\n* `id: int` journal ID\n* `title: str` journal title\n* `date: datetime` upload date as a [`datetime` object](https://docs.python.org/3/library/datetime.html) (defaults to\n  timestamp 0)\n* `author: UserPartial` journal author (filled only if the journal is parsed from a `bs4.BeautifulSoup` page)\n* `stats: JournalStats` journal statistics stored in a named tuple (`comments` (count))\n* `content: str` journal content in HTML format\n* `content_bbcode: str` journal content in BBCode format\n* `mentions: list[str]` the users mentioned in the content (if they were mentioned as links, e.g. `:iconusername:`,\n  `@username`, etc.)\n* `journal_tag: bs4.element.Tag` the journal tag used to parse the object fields\n\n`JournalPartial` objects can be directly cast to a dict object or iterated through.\n\nComparison with `JournalPartial` can be made with either another `JournalPartial` or `Journal` object (the IDs are\ncompared), or an integer (the `JournalPartial.id` value is compared to the given integer).\n\n#### Init\n\n`__init__(journal_tag: bs4.element.Tag = None)`\n\n`Journal` takes one optional parameters: a journal section tag from a journals page.\n\nIf no `journal_tag` is passed then the object fields will remain at their default - empty - value.\n\n#### Methods\n\n* `url -> str`<br/>\n  Property method that returns the Fur Affinity URL to the journal (`https://www.furaffinity.net/journal/{id}`).\n* `parse(journal_item: bs4.element.Tag = None)`<br/>\n  Parses the stored journal tag for information. If `journal_tag` is passed, it overwrites the existing `journal_tag`\n  value.\n\n### Journal\n\nThis object contains full information gathered when parsing a journal page. It contains the same fields\nas `JournalPartial` with the addition of comments:\n\n* `id: int` journal ID\n* `title: str` journal title\n* `date: datetime` upload date as a [`datetime` object](https://docs.python.org/3/library/datetime.html) (defaults to\n  timestamp 0)\n* `author: UserPartial` journal author (filled only if the journal is parsed from a `bs4.BeautifulSoup` page)\n* `stats: JournalStats` journal statistics stored in a named tuple (`comments` (count))\n* `content: str` journal content in HTML format\n* `content_bbcode: str` journal content in BBCode format\n* `header: str` journal header in HTML format (if present)\n* `footer: str` journal footer in HTML format (if present)\n* `mentions: list[str]` the users mentioned in the content (if they were mentioned as links, e.g. `:iconusername:`,\n  `@username`, etc.)\n* `comments: list[Comments]` the comments to the journal, organised in a tree structure\n* `journal_page: bs4.BeautifulSoup` the journal page used to parse the object fields\n\n`Journal` objects can be directly cast to a dict object or iterated through.\n\nComparison with `Journal` can be made with either another `Journal` or `JournalPartial` object (the IDs are compared),\nor an integer (the `Journal.id` value is compared to the given integer).\n\n#### Init\n\n`__init__(journal_page: bs4.BeautifulSoup = None)`\n\n`Journal` takes one optional journal page argument.\n\nIf no `journal_page` is passed then the object fields will remain at their default - empty - value.\n\n#### Methods\n\n* `url -> str`<br/>\n  Property method that returns the Fur Affinity URL to the journal (`https://www.furaffinity.net/journal/{id}`).\n* `parse(journal_page: bs4.BeautifulSoup = None)`<br/>\n  Parses the stored journal tag for information. If `journal_tag` is passed, it overwrites the existing `journal_tag`\n  value.\n\n### SubmissionPartial\n\nThis lightweight submission object is used to contain the information gathered when parsing gallery, scraps, and\nfavorites pages. It contains only the following fields:\n\n* `id: int` submission ID\n* `title: str` submission title\n* `author: UserPartial` submission author (only the `name` field is filled)\n* `rating: str` submission rating [general, mature, adult]\n* `type: str` submission type [text, image, etc...]\n* `thumbnail_url: str` the URL to the submission thumbnail\n* `submission_figure: bs4.element.Tag` the figure tag used to parse the object fields\n\n`SubmissionPartial` objects can be directly cast to a dict object or iterated through.\n\nComparison with `Submission` can be made with either another `SubmissionPartial` or `Submission` object (the IDs are\ncompared), or an integer (the `Submission.id` value is compared to the given integer).\n\n#### Init\n\n`__init__(submission_figure: bs4.element.Tag = None)`\n\nTo initialise the object, an optional `bs4.element.Tag` object is needed containing the parsed HTML of a submission\nfigure tag.\n\nIf no `submission_figure` is passed then the object fields will remain at their default - empty - value.\n\n#### Methods\n\n* `url -> str`<br/>\n  Property method that returns the Fur Affinity URL to the submission (`https://www.furaffinity.net/view/{id}`).\n* `parse(submission_figure: bs4.element.Tag = None)`<br/>\n  Parses the stored submission figure tag for information. If `submission_figure` is passed, it overwrites the\n  existing `submission_figure` value.\n\n### Submission\n\nThe main class that parses and holds submission metadata.\n\n* `id: int` submission ID\n* `title: str` submission title\n* `author: UserPartial` submission author (only the `name`, `title`, and `user_icon_url` fields are filled)\n* `date: datetime` upload date as a [`datetime` object](https://docs.python.org/3/library/datetime.html) (defaults to\n  timestamp 0)\n* `tags: list[str]` tags list\n* `category: str` category\n* `species: str` species\n* `gender: str` gender\n* `rating: str` rating\n* `stats: SubmissionStats` submission statistics stored in a named tuple (`views`, `comments` (count), `favorites`)\n* `type: str` submission type (text, image, etc...)\n* `description: str` description in HTML format\n* `description_bbcode: str` description in BBCode format\n* `footer: str` footer in HTML format\n* `mentions: list[str]` the users mentioned in the description (if they were mentioned as links, e.g. `:iconusername:`,\n  `@username`, etc.)\n* `folder: str` the submission folder (gallery or scraps)\n* `user_folders: list[SubmissionUserFolder]` user folders stored in a list of named tuples (`name`, `url`, `group` (\n  if any))\n* `file_url: str` the URL to the submission file\n* `thumbnail_url: str` the URL to the submission thumbnail\n* `prev: int` the ID of the previous submission (if any)\n* `next: int` the ID of the next submission (if any)\n* `favorite: bool` `True` if the submission is a favorite, `False` otherwise\n* `favorite_toggle_link: str` the link to toggle the favorite status (`/fav/` or `/unfav/` type URL)\n* `comments: list[Comments]` the comments to the submission, organised in a tree structure\n* `submission_page: bs4.BeautifulSoup` the submission page used to parse the object fields\n\n`Submission` objects can be directly cast to a dict object and iterated through.\n\nComparison with `Submission` can be made with either another `Submission` or `SubmissionPartial` object (the IDs are\ncompared), or an integer (the `Submission.id` value is compared to the given integer).\n\n#### Init\n\n`__init__(submission_page: bs4.BeautifulSoup = None)`\n\nTo initialise the object, an optional `bs4.BeautifulSoup` object is needed containing the parsed HTML of a submission\npage.\n\nIf no `submission_page` is passed then the object fields will remain at their default - empty - value.\n\n#### Methods\n\n* `url -> str`<br/>\n  Property method that returns the Fur Affinity URL to the submission (`https://www.furaffinity.net/view/{id}`).\n* `parse(submission_page: bs4.BeautifulSoup = None)`<br/>\n  Parses the stored submission page for metadata. If `submission_page` is passed, it overwrites the\n  existing `submission_page` value.\n\n### Comment\n\nThis object class contains comment metadata and is used to build a tree structure with the comments and their replies.\n\n* `id: int` the comment ID\n* `author: UserPartial` the user who posted the comment\n* `date: datetime` the date the comment was posted\n* `text: str` the comment text in HTML format\n* `text_bbcode: str` the comment text in BBCode format\n* `replies: list[Comment]` list of replies to the comment\n* `reply_to: Comment | int | None` the parent comment, if the comment is a reply. The variable type is `int` only if the\n  comment is parsed outside the parse method of a `Submission` or `Journal` (e.g. by creating a new comment with a\n  comment tag), and when iterating over the parent object (to avoid infinite recursion errors), be it `Submission`\n  , `Journal` or another `Comment`.\n* `edited: bool` `True` if the comment was edited, `False` otherwise\n* `hidden: bool` `True` if the comment was hidden, `False` otherwise (if the comment was hidden, the author and date\n  fields will default to their empty values)\n* `parent: Submission | Journal | None` the `Submission` or `Journal` object the comments are connected to\n* `comment_tag: bs4.element.Tag` the comment tag used to parse the object fields\n\n`Comment` objects can be directly cast to a dict object and iterated through.\n\nComparison with `Comment` can be made with either another comment (the IDs are compared), or an integer (\nthe `Comment.id` value is compared to the given integer).\n\n*Note:* The `__iter__` method of `Comment` objects automatically removes recursion. The `parent` variable is set\nto `None` and `reply_to` is set to the comment\'s ID.<br/>\n*Note:* Because each comment contains the parent `Submission` or `Journal` object (which contains the comment itself)\nand the replied comment object, some iterations may cause infinite recursion errors, for example when using\nthe `copy.deepcopy` function. If such iterations are needed, simply set the `parent` variable to `None` and\nthe `reply_to` variable to `None` or the comment\'s ID (this can be done easily after flattening the comments list\nwith `faapi.comment.flatten_comments`, the comments can then be sorted again with `faapi.comment.sort_comments` which\nwill also restore the `reply_to` values to `Comment` objects).\n\n#### Init\n\n`__init__(self, tag: bs4.element.Tag = None, parent: Submission | Journal = None)`\n\nTo initialise the object, an optional `bs4.element.Tag` object is needed containing the comment tag as taken from a\nsubmission/journal page.\n\nThe optional `parent` argument sets the `parent` variable described above.\n\nIf no `tag` is passed then the object fields will remain at their default - empty - value.\n\n#### Methods\n\n* `url -> str`<br/>\n  Property method that returns the Fur Affinity URL to the comment (\n  e.g. `https://www.furaffinity.net/view/12345678#cid:1234567890`). If the `parent` variable is `None`, the property\n  returns an empty string.\n* `parse(tag: bs4.element.Tag = None)`<br/>\n  Parses the stored tag for metadata. If `tag` is passed, it overwrites the existing `tag` value.\n\n#### Extra Functions\n\nThese extra functions can be used to operate on a list of comments. They only alter the order and structure, but they do\nnot touch any of the metadata.\n\n* `faapi.comment.sort_comments(comments: list[Comment]) -> list[Comment]`<br/>\n  Sorts a list of comments into a tree structure. Replies are overwritten.\n* `faapi.comment.flatten_comments(comments: list[Comment]) -> list[Comment]`<br/>\n  Flattens a list of comments. Replies are not modified.\n\n#### Comment Tree Graphs\n\nUsing the tree structure generated by the library, it is trivial to build a graph visualisation of the comment tree\nusing the [DOT](https://www.graphviz.org/doc/info/lang.html) language.\n\n```python\nsubmission, _ = api.submission(12345678)\ncomments = faapi.comment.flatten_comments(submission.comments)\nwith open("comments.dot", "w") as f:\n    f.write("digraph {\\n")\n    for comment in [c for c in comments if c.reply_to is None]:\n        f.write(f"    parent -> {comment.id}\\n")\n    for comment in comments:\n        for reply in comment.replies:\n            f.write(f"    {comment.id} -> {reply.id}\\n")\n    f.write("}")\n```\n\n```dot\ndigraph {\n    parent -> 157990848\n    parent -> 157993838\n    parent -> 157997294\n    157990848 -> 158014077\n    158014077 -> 158014816\n    158014816 -> 158093180\n    158093180 -> 158097024\n    157993838 -> 157998464\n    157993838 -> 158014126\n    157997294 -> 158014135\n    158014135 -> 158014470\n    158014135 -> 158030074\n    158014470 -> 158093185\n    158030074 -> 158093199\n}\n```\n\n<img alt="comments tree graph" width="400" src="https://quickchart.io/graphviz?graph=digraph%7B%0Aparent-%3E157990848%0Aparent-%3E157993838%0Aparent-%3E157997294%0A157990848-%3E158014077%0A158014077-%3E158014816%0A158014816-%3E158093180%0A158093180-%3E158097024%0A157993838-%3E157998464%0A157993838-%3E158014126%0A157997294-%3E158014135%0A158014135-%3E158014470%0A158014135-%3E158030074%0A158014470-%3E158093185%0A158030074-%3E158093199%0A%7D">\n\n_The graph above was generated with [quickchart.io](https://quickchart.io/documentation/graphviz-api/)_\n\n## BBCode Conversion\n\nUsing the BBCode fields allows to convert between the raw HTMl recovered from Fur Affinity and BBCode tags that follow\nFA\'s guidelines. Conversion from HTML to BBCode covers all known tags and preserves all newlines and spacing.\n\nBBCode text can be converted to Fur Affinity\'s HTMl using the `faapi.parse.bbcode_to_html()` function. The majority of\nsubmissions can be converted back and forth between HTML and BBCode without any information loss, however, the parser\nrules are still a work in progress and there are many edge cases where unusual text and formatting cause the parser to\ngenerate incorrect HTML.\n\n## Exceptions\n\nThe following are the exceptions explicitly raised by the FAAPI functions. The exceptions deriving from `ParsingError`\nare chosen depending on the content of the page. Because Fur Affinity doesn\'t use HTTP status codes besides 404, the\npage is checked against a static list of known error messages/page titles in order to determine the specific error to be\nused. If no match is found, then the `ServerError` (if the page has the "Server Error" title) or the more\ngeneral `NoticeMessage` exceptions are used instead. The actual error message parsed from the page is used as argument\nfor the exceptions, so that it can be analysed when caught.\n\n* `DisallowedPath(Exception)` The path is not allowed by the robots.txt.\n* `Unauthorized(Exception)` The user is not logged-in.\n* `ParsingError(Exception)` An error occurred while parsing the page.\n    * `NonePage(ParsingError)` The parsed page is `None`.\n    * `NotFound(ParsingError)` The resource could not be found (general 404 page or non-existing submission, user, or\n      journal).\n    * `NoTitle(ParsingError)` The parsed paged is missing a title.\n    * `DisabledAccount(ParsingError)` The resource belongs to a disabled account.\n    * `ServerError(ParsingError)` The page contains a server error notice.\n    * `NoticeMessage(ParsingError)` A notice of unknown type was found in the page.\n\n## Beautiful Soup Warnings\n\nWhen parsing some pages or converting HTML to BBCode, the [Beautiful Soup](https://pypi.org/project/beautifulsoup4/)\nlibrary may give some warnings, for example `MarkupResemblesLocatorWarning`. These warnings are left enabled for\nclarity, but can be disabled manually using the `warnings.filterwarnings` function.\n\n## Contributing\n\nAll contributions and suggestions are welcome!\n\nIf you have suggestions for fixes or improvements, you can open an issue with your idea, see [#Issues](#issues) for\ndetails.\n\n## Issues\n\nIf any problem is encountered during usage of the program, an issue can be opened\non [GitHub](https://github.com/FurryCoders/FAAPI/issues).\n\nIssues can also be used to suggest improvements and features.\n\nWhen opening an issue for a problem, please copy the error message and describe the operation in progress when the error\noccurred.\n',
     'author': 'Matteo Campinoti',
     'author_email': 'matteo.campinoti94@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://github.com/FurryCoders/FAAPI',
```

### Comparing `faapi-3.9.5/PKG-INFO` & `faapi-3.9.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: faapi
-Version: 3.9.5
+Version: 3.9.6
 Summary: Python module to implement API-like functionality for the FurAffinity.net website.
 Home-page: https://github.com/FurryCoders/FAAPI
 License: EUPL-1.2
 Author: Matteo Campinoti
 Author-email: matteo.campinoti94@gmail.com
 Requires-Python: >=3.9,<4.0
 Classifier: Development Status :: 5 - Production/Stable
```

