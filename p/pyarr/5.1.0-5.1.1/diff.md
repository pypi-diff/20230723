# Comparing `tmp/pyarr-5.1.0.tar.gz` & `tmp/pyarr-5.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyarr-5.1.0.tar", max compression
+gzip compressed data, was "pyarr-5.1.1.tar", max compression
```

## Comparing `pyarr-5.1.0.tar` & `pyarr-5.1.1.tar`

### file list

```diff
@@ -1,21 +1,21 @@
--rw-r--r--   0        0        0     1056 2023-04-18 15:33:45.763792 pyarr-5.1.0/LICENSE
--rw-r--r--   0        0        0     6550 2023-04-18 15:33:45.763792 pyarr-5.1.0/README.md
--rw-r--r--   0        0        0      249 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/__init__.py
--rw-r--r--   0        0        0    32046 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/base.py
--rw-r--r--   0        0        0      101 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/const.py
--rw-r--r--   0        0        0     1081 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/exceptions.py
--rw-r--r--   0        0        0    28051 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/lidarr.py
--rw-r--r--   0        0        0        0 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/models/__init__.py
--rw-r--r--   0        0        0     2592 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/models/common.py
--rw-r--r--   0        0        0     1059 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/models/lidarr.py
--rw-r--r--   0        0        0     1758 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/models/radarr.py
--rw-r--r--   0        0        0     1833 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/models/readarr.py
--rw-r--r--   0        0        0     2057 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/models/sonarr.py
--rw-r--r--   0        0        0        0 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/py.typed
--rw-r--r--   0        0        0    21301 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/radarr.py
--rw-r--r--   0        0        0    31608 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/readarr.py
--rw-r--r--   0        0        0     8346 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/request_handler.py
--rw-r--r--   0        0        0    26503 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/sonarr.py
--rw-r--r--   0        0        0      300 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyarr/types.py
--rw-r--r--   0        0        0     3092 2023-04-18 15:33:45.767792 pyarr-5.1.0/pyproject.toml
--rw-r--r--   0        0        0     7854 1970-01-01 00:00:00.000000 pyarr-5.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1056 2023-07-23 18:56:36.025116 pyarr-5.1.1/LICENSE
+-rw-r--r--   0        0        0     6525 2023-07-23 18:56:36.025116 pyarr-5.1.1/README.md
+-rw-r--r--   0        0        0      249 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/__init__.py
+-rw-r--r--   0        0        0    32046 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/base.py
+-rw-r--r--   0        0        0      101 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/const.py
+-rw-r--r--   0        0        0     1081 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/exceptions.py
+-rw-r--r--   0        0        0    28051 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/lidarr.py
+-rw-r--r--   0        0        0        0 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/models/__init__.py
+-rw-r--r--   0        0        0     2592 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/models/common.py
+-rw-r--r--   0        0        0     1059 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/models/lidarr.py
+-rw-r--r--   0        0        0     1903 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/models/radarr.py
+-rw-r--r--   0        0        0     1833 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/models/readarr.py
+-rw-r--r--   0        0        0     2057 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/models/sonarr.py
+-rw-r--r--   0        0        0        0 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/py.typed
+-rw-r--r--   0        0        0    21301 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/radarr.py
+-rw-r--r--   0        0        0    31608 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/readarr.py
+-rw-r--r--   0        0        0     8346 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/request_handler.py
+-rw-r--r--   0        0        0    26503 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/sonarr.py
+-rw-r--r--   0        0        0      300 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyarr/types.py
+-rw-r--r--   0        0        0     3092 2023-07-23 18:56:36.025116 pyarr-5.1.1/pyproject.toml
+-rw-r--r--   0        0        0     7629 1970-01-01 00:00:00.000000 pyarr-5.1.1/PKG-INFO
```

### Comparing `pyarr-5.1.0/LICENSE` & `pyarr-5.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/README.md` & `pyarr-5.1.1/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -17,15 +17,15 @@
 [![MIT License][license-shield]][license-url]
 [![LinkedIn][linkedin-shield]][linkedin-url]
 
 <!-- PROJECT LOGO -->
 <br />
 <div align="center">
   <a href="https://github.com/totaldebug/pyarr">
-    <img src=".github/img/pyarr.png" alt="Logo">
+    <img src=".github/img/logo.png" alt="Logo">
   </a>
 
   <h3 align="center">Pyarr</h3>
 
   <p align="center">
     A Python library for interacting with the `arr` API's
   </p>
@@ -33,16 +33,14 @@
     <br />
     <a href="https://github.com/totaldebug/pyarr/issues/new?assignees=&labels=type%2Fbug&template=bug_report.yml">Report Bug</a>
     ·
     <a href="https://github.com/totaldebug/pyarr/issues/new?assignees=&labels=type%2Ffeature&template=feature_request.yml">Request Feature</a>
 
 </div>
 
-
-
 <!-- TABLE OF CONTENTS -->
 <details>
   <summary>Table of Contents</summary>
   <ol>
     <li>
       <a href="#about-the-project">About The Project</a>
       <ul>
@@ -57,65 +55,60 @@
     <li><a href="#contributing">Contributing</a></li>
     <li><a href="#license">License</a></li>
     <li><a href="#contact">Contact</a></li>
     <li><a href="#acknowledgments">Acknowledgments</a></li>
   </ol>
 </details>
 
-
-
 <!-- ABOUT THE PROJECT -->
 ## About The Project
 
 A Python library for the following `arr` API's:
 
 * Sonarr
 * Radarr
 * Readarr
 * Lidarr
 
 The library returns results in JSON format for ease of use, this also reduces the risk of failue when the arr APIs are updated.
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
-
 ### Built With
 
 [![python][python]][python-url]
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
 <!-- GETTING STARTED -->
 ## Getting Started
 
-* [QuickStart Guide](https://docs.totaldebug.uk/pyarr/overview/quickstart.html)
+* [QuickStart Guide](https://docs.totaldebug.uk/pyarr/quickstart.html)
 * [Full Documentation](https://docs.totaldebug.uk/pyarr)
 * [Release Notes](https://github.com/totaldebug/pyarr/releases)
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
 ## Features
 
 * Support for multiple Arr APIs
- * Sonarr
- * Radarr
- * Readarr
- * Lidarr
+* Sonarr
+* Radarr
+* Readarr
+* Lidarr
 * Type checking
 
 ## Compatibility
 
 The below versions are based on our last tests, This will be updated as tests fail and updates are published.
 
 | Version | Sonarr | Radarr | Readarr | Lidarr |
 | ------- | ------ | ------ | ------- | ------ |
 | v5.0.0 | from: v3.0.10.1567 | from: v4.3.2.6857 | from: v0.1.4.1596 | from: v1.0.2.2592 |
 
-
-
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
 <!-- ROADMAP -->
 ## Roadmap
 
 See the [feature requests](https://github.com/totaldebug/pyarr/labels/type%2Ffeature) for a full list of requested features.
 
@@ -130,25 +123,23 @@
 <!-- CONTRIBUTING -->
 ## Contributing
 
 Got something you would like to add? check out the contributing guide in the [documentation](https://docs.totaldebug.uk/pyarr/contributing.html)
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
-
 <!-- LICENSE -->
 ## License
 
 [![CC BY-NC-SA 4.0][license-shield]][license-url]
 
 * Copyright © [Total Debug](https://totaldebug.uk).
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
-
 <!-- CONTACT -->
 ## Contact
 
 * [Discord](https://discord.gg/6fmekudc8Q)
 * [Discussions](https://github.com/totaldebug/pyarr/discussions)
 * [Project Link](https://github.com/totaldebug/pyarr)
 
@@ -159,15 +150,14 @@
 
 Below are a list of resources that I used to assist with this project.
 
 * None at this time
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
-
 <!-- MARKDOWN LINKS & IMAGES -->
 <!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
 [release-shield]: https://img.shields.io/github/v/release/totaldebug/pyarr?color=ff7034&label=Release&sort=semver&style=flat-square
 [release-url]: https://github.com/totaldebug/pyarr/releases
 [contributors-shield]: https://img.shields.io/github/contributors/totaldebug/pyarr.svg?style=flat-square
 [contributors-url]: https://github.com/totaldebug/pyarr/graphs/contributors
 [forks-shield]: https://img.shields.io/github/forks/totaldebug/pyarr.svg?style=flat-square
@@ -185,13 +175,12 @@
 [gh-last-release-date]: https://img.shields.io/github/release-date/totaldebug/pyarr?style=flat-square&label=Last%20Release%20Date&logo=github&logoColor=white
 [gh-last-commit]: https://img.shields.io/github/last-commit/totaldebug/pyarr.svg?style=flat-square&logo=github&label=Last%20Commit&logoColor=white
 
 [lines]: https://img.shields.io/tokei/lines/github/totaldebug/pyarr?style=flat-square
 [lines-url]: https://github.com/totaldebug/pyarr
 [code-size]: https://img.shields.io/github/languages/code-size/totaldebug/pyarr?style=flat-square
 
-
 [Sponsor]: https://img.shields.io/badge/sponsor-000?style=flat-square&logo=githubsponsors&logoColor=red
 [Sponsor-url]: https://github.com/sponsors/marksie1988
 
 [python]: https://img.shields.io/badge/Python-blue?style=flat-square&logo=Python&logoColor=white
 [python-url]: https://www.python.org/
```

#### html2text {}

```diff
@@ -26,16 +26,16 @@
   ## About The Project A Python library for the following `arr` API's: * Sonarr
 * Radarr * Readarr * Lidarr The library returns results in JSON format for ease
 of use, this also reduces the risk of failue when the arr APIs are updated.
                                                                   (back_to_top)
 ### Built With [![python][python]][python-url]
                                                                   (back_to_top)
  ## Getting Started * [QuickStart Guide](https://docs.totaldebug.uk/pyarr/
-overview/quickstart.html) * [Full Documentation](https://docs.totaldebug.uk/
-pyarr) * [Release Notes](https://github.com/totaldebug/pyarr/releases)
+quickstart.html) * [Full Documentation](https://docs.totaldebug.uk/pyarr) *
+[Release Notes](https://github.com/totaldebug/pyarr/releases)
                                                                   (back_to_top)
 ## Features * Support for multiple Arr APIs * Sonarr * Radarr * Readarr *
 Lidarr * Type checking ## Compatibility The below versions are based on our
 last tests, This will be updated as tests fail and updates are published. |
 Version | Sonarr | Radarr | Readarr | Lidarr | | ------- | ------ | ------ | --
 ----- | ------ | | v5.0.0 | from: v3.0.10.1567 | from: v4.3.2.6857 | from:
 v0.1.4.1596 | from: v1.0.2.2592 |
```

### Comparing `pyarr-5.1.0/pyarr/base.py` & `pyarr-5.1.1/pyarr/base.py`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/pyarr/exceptions.py` & `pyarr-5.1.1/pyarr/exceptions.py`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/pyarr/lidarr.py` & `pyarr-5.1.1/pyarr/lidarr.py`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/pyarr/models/common.py` & `pyarr-5.1.1/pyarr/models/common.py`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/pyarr/models/lidarr.py` & `pyarr-5.1.1/pyarr/models/lidarr.py`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/pyarr/models/radarr.py` & `pyarr-5.1.1/pyarr/models/radarr.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 from typing import Literal
 
 RadarrCommands = Literal[
     "DownloadedMoviesScan",
     "MissingMoviesSearch",
+    "MoviesSearch",
     "RefreshMovie",
     "RenameMovie",
     "RenameFiles",
     "Backup",
 ]
 """
 Radarr commands.
@@ -19,14 +20,20 @@
 
     Args:
         clientid (int, optional): Download client ID
 
 MissingMoviesSearch:
     Searches for any missing movies
 
+MoviesSearch:
+    Searches for the specified movie or movies
+
+    Args:
+        movieIds (list[int]): ID of Movie or movies
+
 RefreshMovies:
     Refreshes all of the movies, or specific by ID
 
     Args:
         movieid (int, Optional): ID of Movie
 
 RenameMovie:
```

### Comparing `pyarr-5.1.0/pyarr/models/readarr.py` & `pyarr-5.1.1/pyarr/models/readarr.py`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/pyarr/models/sonarr.py` & `pyarr-5.1.1/pyarr/models/sonarr.py`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/pyarr/radarr.py` & `pyarr-5.1.1/pyarr/radarr.py`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/pyarr/readarr.py` & `pyarr-5.1.1/pyarr/readarr.py`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/pyarr/request_handler.py` & `pyarr-5.1.1/pyarr/request_handler.py`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/pyarr/sonarr.py` & `pyarr-5.1.1/pyarr/sonarr.py`

 * *Files identical despite different names*

### Comparing `pyarr-5.1.0/pyproject.toml` & `pyarr-5.1.1/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "pyarr"
-version = "5.1.0"
+version = "5.1.1"
 description = "Synchronous Sonarr, Radarr, Lidarr and Readarr API's for Python"
 authors = ["Steven Marks <marksie1988@users.noreply.github.com>"]
 license = "MIT"
 readme = "README.md"
 keywords = ["sonarr", "radarr", "readarr", "lidarr", "api", "wrapper", "plex"]
 homepage = "https://github.com/totaldebug/pyarr"
 repository = "https://github.com/totaldebug/pyarr"
```

### Comparing `pyarr-5.1.0/PKG-INFO` & `pyarr-5.1.1/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyarr
-Version: 5.1.0
+Version: 5.1.1
 Summary: Synchronous Sonarr, Radarr, Lidarr and Readarr API's for Python
 Home-page: https://github.com/totaldebug/pyarr
 License: MIT
 Keywords: sonarr,radarr,readarr,lidarr,api,wrapper,plex
 Author: Steven Marks
 Author-email: marksie1988@users.noreply.github.com
 Requires-Python: >=3.9,<4.0
@@ -12,18 +12,14 @@
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
-Classifier: Programming Language :: Python :: 3.9
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Requires-Dist: overrides (>=7.3.1,<8.0.0)
 Requires-Dist: requests (>=2.28.2,<3.0.0)
 Requires-Dist: types-requests (>=2.28.11.17,<3.0.0.0)
 Project-URL: Documentation, https://docs.totaldebug.uk/pyarr
 Project-URL: Repository, https://github.com/totaldebug/pyarr
 Description-Content-Type: text/markdown
@@ -47,15 +43,15 @@
 [![MIT License][license-shield]][license-url]
 [![LinkedIn][linkedin-shield]][linkedin-url]
 
 <!-- PROJECT LOGO -->
 <br />
 <div align="center">
   <a href="https://github.com/totaldebug/pyarr">
-    <img src=".github/img/pyarr.png" alt="Logo">
+    <img src=".github/img/logo.png" alt="Logo">
   </a>
 
   <h3 align="center">Pyarr</h3>
 
   <p align="center">
     A Python library for interacting with the `arr` API's
   </p>
@@ -63,16 +59,14 @@
     <br />
     <a href="https://github.com/totaldebug/pyarr/issues/new?assignees=&labels=type%2Fbug&template=bug_report.yml">Report Bug</a>
     ·
     <a href="https://github.com/totaldebug/pyarr/issues/new?assignees=&labels=type%2Ffeature&template=feature_request.yml">Request Feature</a>
 
 </div>
 
-
-
 <!-- TABLE OF CONTENTS -->
 <details>
   <summary>Table of Contents</summary>
   <ol>
     <li>
       <a href="#about-the-project">About The Project</a>
       <ul>
@@ -87,65 +81,60 @@
     <li><a href="#contributing">Contributing</a></li>
     <li><a href="#license">License</a></li>
     <li><a href="#contact">Contact</a></li>
     <li><a href="#acknowledgments">Acknowledgments</a></li>
   </ol>
 </details>
 
-
-
 <!-- ABOUT THE PROJECT -->
 ## About The Project
 
 A Python library for the following `arr` API's:
 
 * Sonarr
 * Radarr
 * Readarr
 * Lidarr
 
 The library returns results in JSON format for ease of use, this also reduces the risk of failue when the arr APIs are updated.
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
-
 ### Built With
 
 [![python][python]][python-url]
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
 <!-- GETTING STARTED -->
 ## Getting Started
 
-* [QuickStart Guide](https://docs.totaldebug.uk/pyarr/overview/quickstart.html)
+* [QuickStart Guide](https://docs.totaldebug.uk/pyarr/quickstart.html)
 * [Full Documentation](https://docs.totaldebug.uk/pyarr)
 * [Release Notes](https://github.com/totaldebug/pyarr/releases)
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
 ## Features
 
 * Support for multiple Arr APIs
- * Sonarr
- * Radarr
- * Readarr
- * Lidarr
+* Sonarr
+* Radarr
+* Readarr
+* Lidarr
 * Type checking
 
 ## Compatibility
 
 The below versions are based on our last tests, This will be updated as tests fail and updates are published.
 
 | Version | Sonarr | Radarr | Readarr | Lidarr |
 | ------- | ------ | ------ | ------- | ------ |
 | v5.0.0 | from: v3.0.10.1567 | from: v4.3.2.6857 | from: v0.1.4.1596 | from: v1.0.2.2592 |
 
-
-
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
 <!-- ROADMAP -->
 ## Roadmap
 
 See the [feature requests](https://github.com/totaldebug/pyarr/labels/type%2Ffeature) for a full list of requested features.
 
@@ -160,25 +149,23 @@
 <!-- CONTRIBUTING -->
 ## Contributing
 
 Got something you would like to add? check out the contributing guide in the [documentation](https://docs.totaldebug.uk/pyarr/contributing.html)
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
-
 <!-- LICENSE -->
 ## License
 
 [![CC BY-NC-SA 4.0][license-shield]][license-url]
 
 * Copyright © [Total Debug](https://totaldebug.uk).
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
-
 <!-- CONTACT -->
 ## Contact
 
 * [Discord](https://discord.gg/6fmekudc8Q)
 * [Discussions](https://github.com/totaldebug/pyarr/discussions)
 * [Project Link](https://github.com/totaldebug/pyarr)
 
@@ -189,15 +176,14 @@
 
 Below are a list of resources that I used to assist with this project.
 
 * None at this time
 
 <p align="right">(<a href="#readme-top">back to top</a>)</p>
 
-
 <!-- MARKDOWN LINKS & IMAGES -->
 <!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
 [release-shield]: https://img.shields.io/github/v/release/totaldebug/pyarr?color=ff7034&label=Release&sort=semver&style=flat-square
 [release-url]: https://github.com/totaldebug/pyarr/releases
 [contributors-shield]: https://img.shields.io/github/contributors/totaldebug/pyarr.svg?style=flat-square
 [contributors-url]: https://github.com/totaldebug/pyarr/graphs/contributors
 [forks-shield]: https://img.shields.io/github/forks/totaldebug/pyarr.svg?style=flat-square
@@ -215,14 +201,13 @@
 [gh-last-release-date]: https://img.shields.io/github/release-date/totaldebug/pyarr?style=flat-square&label=Last%20Release%20Date&logo=github&logoColor=white
 [gh-last-commit]: https://img.shields.io/github/last-commit/totaldebug/pyarr.svg?style=flat-square&logo=github&label=Last%20Commit&logoColor=white
 
 [lines]: https://img.shields.io/tokei/lines/github/totaldebug/pyarr?style=flat-square
 [lines-url]: https://github.com/totaldebug/pyarr
 [code-size]: https://img.shields.io/github/languages/code-size/totaldebug/pyarr?style=flat-square
 
-
 [Sponsor]: https://img.shields.io/badge/sponsor-000?style=flat-square&logo=githubsponsors&logoColor=red
 [Sponsor-url]: https://github.com/sponsors/marksie1988
 
 [python]: https://img.shields.io/badge/Python-blue?style=flat-square&logo=Python&logoColor=white
 [python-url]: https://www.python.org/
```

#### html2text {}

```diff
@@ -1,32 +1,29 @@
-Metadata-Version: 2.1 Name: pyarr Version: 5.1.0 Summary: Synchronous Sonarr,
+Metadata-Version: 2.1 Name: pyarr Version: 5.1.1 Summary: Synchronous Sonarr,
 Radarr, Lidarr and Readarr API's for Python Home-page: https://github.com/
 totaldebug/pyarr License: MIT Keywords:
 sonarr,radarr,readarr,lidarr,api,wrapper,plex Author: Steven Marks Author-
 email: marksie1988@users.noreply.github.com Requires-Python: >=3.9,<4.0
 Classifier: Development Status :: 5 - Production/Stable Classifier: Intended
 Audience :: Developers Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English Classifier: Programming Language ::
 Python :: 3 Classifier: Programming Language :: Python :: 3.9 Classifier:
 Programming Language :: Python :: 3.10 Classifier: Programming Language ::
-Python :: 3.11 Classifier: Programming Language :: Python :: 3 Classifier:
-Programming Language :: Python :: 3.10 Classifier: Programming Language ::
-Python :: 3.11 Classifier: Programming Language :: Python :: 3.9 Classifier:
-Topic :: Software Development :: Libraries :: Python Modules Requires-Dist:
-overrides (>=7.3.1,<8.0.0) Requires-Dist: requests (>=2.28.2,<3.0.0) Requires-
-Dist: types-requests (>=2.28.11.17,<3.0.0.0) Project-URL: Documentation, https:
-//docs.totaldebug.uk/pyarr Project-URL: Repository, https://github.com/
-totaldebug/pyarr Description-Content-Type: text/markdown  [![Release][release-
-shield]][release-url] [![Stargazers][stars-shield]][stars-url] ![codecov]
-[codecov-shield] ![GitHub last release date][gh-last-release-date] ![GitHub
-last commit][gh-last-commit] [![Contributors][contributors-shield]]
-[contributors-url] [![Forks][forks-shield]][forks-url] [![Issues][issues-
-shield]][issues-url] [![Lines of code][lines]][lines-url] ![Code size][code-
-size] [![MIT License][license-shield]][license-url] [![LinkedIn][linkedin-
-shield]][linkedin-url]
+Python :: 3.11 Classifier: Topic :: Software Development :: Libraries :: Python
+Modules Requires-Dist: overrides (>=7.3.1,<8.0.0) Requires-Dist: requests
+(>=2.28.2,<3.0.0) Requires-Dist: types-requests (>=2.28.11.17,<3.0.0.0)
+Project-URL: Documentation, https://docs.totaldebug.uk/pyarr Project-URL:
+Repository, https://github.com/totaldebug/pyarr Description-Content-Type: text/
+markdown  [![Release][release-shield]][release-url] [![Stargazers][stars-
+shield]][stars-url] ![codecov][codecov-shield] ![GitHub last release date][gh-
+last-release-date] ![GitHub last commit][gh-last-commit] [![Contributors]
+[contributors-shield]][contributors-url] [![Forks][forks-shield]][forks-url] [!
+[Issues][issues-shield]][issues-url] [![Lines of code][lines]][lines-url] !
+[Code size][code-size] [![MIT License][license-shield]][license-url] [!
+[LinkedIn][linkedin-shield]][linkedin-url]
                                     [Logo]
                                 **** Pyarr ****
              A Python library for interacting with the `arr` API's
 
 
                          Report_Bug Â· Request_Feature
   Table of Contents
@@ -44,16 +41,16 @@
   ## About The Project A Python library for the following `arr` API's: * Sonarr
 * Radarr * Readarr * Lidarr The library returns results in JSON format for ease
 of use, this also reduces the risk of failue when the arr APIs are updated.
                                                                   (back_to_top)
 ### Built With [![python][python]][python-url]
                                                                   (back_to_top)
  ## Getting Started * [QuickStart Guide](https://docs.totaldebug.uk/pyarr/
-overview/quickstart.html) * [Full Documentation](https://docs.totaldebug.uk/
-pyarr) * [Release Notes](https://github.com/totaldebug/pyarr/releases)
+quickstart.html) * [Full Documentation](https://docs.totaldebug.uk/pyarr) *
+[Release Notes](https://github.com/totaldebug/pyarr/releases)
                                                                   (back_to_top)
 ## Features * Support for multiple Arr APIs * Sonarr * Radarr * Readarr *
 Lidarr * Type checking ## Compatibility The below versions are based on our
 last tests, This will be updated as tests fail and updates are published. |
 Version | Sonarr | Radarr | Readarr | Lidarr | | ------- | ------ | ------ | --
 ----- | ------ | | v5.0.0 | from: v3.0.10.1567 | from: v4.3.2.6857 | from:
 v0.1.4.1596 | from: v1.0.2.2592 |
```

