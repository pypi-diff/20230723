# Comparing `tmp/RapidMangaDL-0.2.1.tar.gz` & `tmp/RapidMangaDL-0.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "RapidMangaDL-0.2.1.tar", last modified: Thu Jul 20 09:58:03 2023, max compression
+gzip compressed data, was "RapidMangaDL-0.2.2.tar", last modified: Sun Jul 23 12:39:23 2023, max compression
```

## Comparing `RapidMangaDL-0.2.1.tar` & `RapidMangaDL-0.2.2.tar`

### file list

```diff
@@ -1,48 +1,49 @@
-drwxrwxrwx   0        0        0        0 2023-07-20 09:58:03.137079 RapidMangaDL-0.2.1/
--rw-rw-rw-   0        0        0     1104 2023-07-19 04:26:03.000000 RapidMangaDL-0.2.1/LICENSE
--rw-rw-rw-   0        0        0     6943 2023-07-20 09:58:03.125075 RapidMangaDL-0.2.1/PKG-INFO
--rw-rw-rw-   0        0        0     5516 2023-07-19 07:59:23.000000 RapidMangaDL-0.2.1/README.md
-drwxrwxrwx   0        0        0        0 2023-07-20 09:58:02.964963 RapidMangaDL-0.2.1/RapidMangaDL.egg-info/
--rw-rw-rw-   0        0        0     6943 2023-07-20 09:58:02.000000 RapidMangaDL-0.2.1/RapidMangaDL.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1078 2023-07-20 09:58:02.000000 RapidMangaDL-0.2.1/RapidMangaDL.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-20 09:58:02.000000 RapidMangaDL-0.2.1/RapidMangaDL.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       48 2023-07-20 09:58:02.000000 RapidMangaDL-0.2.1/RapidMangaDL.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      281 2023-07-20 09:58:02.000000 RapidMangaDL-0.2.1/RapidMangaDL.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-07-20 09:58:02.000000 RapidMangaDL-0.2.1/RapidMangaDL.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     2195 2023-07-19 06:16:58.000000 RapidMangaDL-0.2.1/cx_setup.py
-drwxrwxrwx   0        0        0        0 2023-07-20 09:58:03.002517 RapidMangaDL-0.2.1/manga_dl/
--rw-rw-rw-   0        0        0      106 2023-07-19 10:39:30.000000 RapidMangaDL-0.2.1/manga_dl/__init__.py
--rw-rw-rw-   0        0        0     6817 2023-07-20 08:33:10.000000 RapidMangaDL-0.2.1/manga_dl/app.py
--rw-rw-rw-   0        0        0     7955 2023-07-20 09:53:12.000000 RapidMangaDL-0.2.1/manga_dl/main.py
--rw-rw-rw-   0        0        0    30183 2023-07-20 07:56:05.000000 RapidMangaDL-0.2.1/manga_dl/manga.py
-drwxrwxrwx   0        0        0        0 2023-07-20 09:58:03.023513 RapidMangaDL-0.2.1/manga_dl/manga_sources/
--rw-rw-rw-   0        0        0      547 2023-07-19 18:07:13.000000 RapidMangaDL-0.2.1/manga_dl/manga_sources/__init__.py
--rw-rw-rw-   0        0        0     4385 2023-07-20 08:52:31.000000 RapidMangaDL-0.2.1/manga_dl/manga_sources/base_source.py
--rw-rw-rw-   0        0        0    19432 2023-07-20 08:56:48.000000 RapidMangaDL-0.2.1/manga_dl/manga_sources/source1.py
--rw-rw-rw-   0        0        0    12656 2023-07-18 17:22:33.000000 RapidMangaDL-0.2.1/manga_dl/manga_sources/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-20 09:58:03.069514 RapidMangaDL-0.2.1/manga_dl/public/
--rw-rw-rw-   0        0        0   232918 2023-07-11 11:05:36.000000 RapidMangaDL-0.2.1/manga_dl/public/bootstrap530.css
--rw-rw-rw-   0        0        0    80427 2023-07-11 11:07:47.000000 RapidMangaDL-0.2.1/manga_dl/public/bootstrap530.js
--rw-rw-rw-   0        0        0    65212 2023-07-10 06:53:05.000000 RapidMangaDL-0.2.1/manga_dl/public/error.png
--rw-rw-rw-   0        0        0    86663 2023-07-11 11:07:20.000000 RapidMangaDL-0.2.1/manga_dl/public/jquery321.js
--rw-rw-rw-   0        0        0   215111 2023-07-11 11:38:35.000000 RapidMangaDL-0.2.1/manga_dl/public/loading-fast.gif
--rw-rw-rw-   0        0        0     6806 2023-07-19 11:21:29.000000 RapidMangaDL-0.2.1/manga_dl/public/manga.js
--rw-rw-rw-   0        0        0     3407 2023-07-19 11:51:16.000000 RapidMangaDL-0.2.1/manga_dl/public/search.js
--rw-rw-rw-   0        0        0     4075 2023-07-16 08:35:36.000000 RapidMangaDL-0.2.1/manga_dl/public/style.css
-drwxrwxrwx   0        0        0        0 2023-07-20 09:58:03.086544 RapidMangaDL-0.2.1/manga_dl/templates/
--rw-rw-rw-   0        0        0     3699 2023-07-14 18:32:29.000000 RapidMangaDL-0.2.1/manga_dl/templates/chapter.html
--rw-rw-rw-   0        0        0     3200 2023-07-16 13:24:25.000000 RapidMangaDL-0.2.1/manga_dl/templates/layout.html
--rw-rw-rw-   0        0        0    13075 2023-07-18 16:19:30.000000 RapidMangaDL-0.2.1/manga_dl/templates/manga.html
--rw-rw-rw-   0        0        0     2287 2023-07-16 14:00:18.000000 RapidMangaDL-0.2.1/manga_dl/templates/search.html
-drwxrwxrwx   0        0        0        0 2023-07-20 09:58:03.118077 RapidMangaDL-0.2.1/manga_dl/tools/
--rw-rw-rw-   0        0        0      183 2023-07-17 14:00:50.000000 RapidMangaDL-0.2.1/manga_dl/tools/__init__.py
--rw-rw-rw-   0        0        0     8192 2023-07-13 14:27:12.000000 RapidMangaDL-0.2.1/manga_dl/tools/create_pdf.py
--rw-rw-rw-   0        0        0     9652 2023-07-17 09:15:36.000000 RapidMangaDL-0.2.1/manga_dl/tools/download.py
--rw-rw-rw-   0        0        0     6321 2023-07-19 11:55:56.000000 RapidMangaDL-0.2.1/manga_dl/tools/downloader2.py
--rw-rw-rw-   0        0        0     8588 2023-07-14 13:14:30.000000 RapidMangaDL-0.2.1/manga_dl/tools/downloader3.py
--rw-rw-rw-   0        0        0      188 2023-07-16 05:40:17.000000 RapidMangaDL-0.2.1/manga_dl/tools/exceptions.py
--rw-rw-rw-   0        0        0     7137 2023-07-17 14:19:26.000000 RapidMangaDL-0.2.1/manga_dl/tools/flask_cloudflared.py
--rw-rw-rw-   0        0        0     1308 2023-07-18 07:58:37.000000 RapidMangaDL-0.2.1/manga_dl/tools/models.py
--rw-rw-rw-   0        0        0     9560 2023-07-19 18:17:35.000000 RapidMangaDL-0.2.1/manga_dl/tools/utils.py
--rw-rw-rw-   0        0        0       42 2023-07-20 09:58:03.137079 RapidMangaDL-0.2.1/setup.cfg
--rw-rw-rw-   0        0        0     2189 2023-07-20 09:57:40.000000 RapidMangaDL-0.2.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:39:23.056045 RapidMangaDL-0.2.2/
+-rw-rw-rw-   0        0        0     1104 2023-07-19 04:26:03.000000 RapidMangaDL-0.2.2/LICENSE
+-rw-rw-rw-   0        0        0     6945 2023-07-23 12:39:23.055046 RapidMangaDL-0.2.2/PKG-INFO
+-rw-rw-rw-   0        0        0     5516 2023-07-23 12:14:35.000000 RapidMangaDL-0.2.2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 12:39:22.525810 RapidMangaDL-0.2.2/RapidMangaDL.egg-info/
+-rw-rw-rw-   0        0        0     6945 2023-07-23 12:39:22.000000 RapidMangaDL-0.2.2/RapidMangaDL.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1112 2023-07-23 12:39:22.000000 RapidMangaDL-0.2.2/RapidMangaDL.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 12:39:22.000000 RapidMangaDL-0.2.2/RapidMangaDL.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       48 2023-07-23 12:39:22.000000 RapidMangaDL-0.2.2/RapidMangaDL.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0      295 2023-07-23 12:39:22.000000 RapidMangaDL-0.2.2/RapidMangaDL.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 12:39:22.000000 RapidMangaDL-0.2.2/RapidMangaDL.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     2195 2023-07-19 06:16:58.000000 RapidMangaDL-0.2.2/cx_setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:39:22.590343 RapidMangaDL-0.2.2/manga_dl/
+-rw-rw-rw-   0        0        0      106 2023-07-19 10:39:30.000000 RapidMangaDL-0.2.2/manga_dl/__init__.py
+-rw-rw-rw-   0        0        0     7195 2023-07-23 10:27:14.000000 RapidMangaDL-0.2.2/manga_dl/app.py
+-rw-rw-rw-   0        0        0     8308 2023-07-23 10:17:27.000000 RapidMangaDL-0.2.2/manga_dl/main.py
+-rw-rw-rw-   0        0        0    30776 2023-07-23 06:22:54.000000 RapidMangaDL-0.2.2/manga_dl/manga.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:39:22.628344 RapidMangaDL-0.2.2/manga_dl/manga_sources/
+-rw-rw-rw-   0        0        0      615 2023-07-23 11:57:18.000000 RapidMangaDL-0.2.2/manga_dl/manga_sources/__init__.py
+-rw-rw-rw-   0        0        0     6955 2023-07-23 06:06:38.000000 RapidMangaDL-0.2.2/manga_dl/manga_sources/base_source.py
+-rw-rw-rw-   0        0        0    20194 2023-07-23 10:58:45.000000 RapidMangaDL-0.2.2/manga_dl/manga_sources/source1.py
+-rw-rw-rw-   0        0        0     9640 2023-07-23 11:59:54.000000 RapidMangaDL-0.2.2/manga_dl/manga_sources/source2.py
+-rw-rw-rw-   0        0        0    14406 2023-07-23 10:28:35.000000 RapidMangaDL-0.2.2/manga_dl/manga_sources/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:39:22.843959 RapidMangaDL-0.2.2/manga_dl/public/
+-rw-rw-rw-   0        0        0   232918 2023-07-11 11:05:36.000000 RapidMangaDL-0.2.2/manga_dl/public/bootstrap530.css
+-rw-rw-rw-   0        0        0    80427 2023-07-11 11:07:47.000000 RapidMangaDL-0.2.2/manga_dl/public/bootstrap530.js
+-rw-rw-rw-   0        0        0    65212 2023-07-10 06:53:05.000000 RapidMangaDL-0.2.2/manga_dl/public/error.png
+-rw-rw-rw-   0        0        0    86663 2023-07-11 11:07:20.000000 RapidMangaDL-0.2.2/manga_dl/public/jquery321.js
+-rw-rw-rw-   0        0        0   215111 2023-07-11 11:38:35.000000 RapidMangaDL-0.2.2/manga_dl/public/loading-fast.gif
+-rw-rw-rw-   0        0        0     8748 2023-07-23 11:52:48.000000 RapidMangaDL-0.2.2/manga_dl/public/manga.js
+-rw-rw-rw-   0        0        0     3407 2023-07-19 11:51:16.000000 RapidMangaDL-0.2.2/manga_dl/public/search.js
+-rw-rw-rw-   0        0        0     4075 2023-07-16 08:35:36.000000 RapidMangaDL-0.2.2/manga_dl/public/style.css
+drwxrwxrwx   0        0        0        0 2023-07-23 12:39:22.902501 RapidMangaDL-0.2.2/manga_dl/templates/
+-rw-rw-rw-   0        0        0     4243 2023-07-23 10:14:40.000000 RapidMangaDL-0.2.2/manga_dl/templates/chapter.html
+-rw-rw-rw-   0        0        0     3200 2023-07-16 13:24:25.000000 RapidMangaDL-0.2.2/manga_dl/templates/layout.html
+-rw-rw-rw-   0        0        0    13076 2023-07-23 11:08:07.000000 RapidMangaDL-0.2.2/manga_dl/templates/manga.html
+-rw-rw-rw-   0        0        0     2287 2023-07-16 14:00:18.000000 RapidMangaDL-0.2.2/manga_dl/templates/search.html
+drwxrwxrwx   0        0        0        0 2023-07-23 12:39:23.051052 RapidMangaDL-0.2.2/manga_dl/tools/
+-rw-rw-rw-   0        0        0      183 2023-07-17 14:00:50.000000 RapidMangaDL-0.2.2/manga_dl/tools/__init__.py
+-rw-rw-rw-   0        0        0     8192 2023-07-13 14:27:12.000000 RapidMangaDL-0.2.2/manga_dl/tools/create_pdf.py
+-rw-rw-rw-   0        0        0     9652 2023-07-17 09:15:36.000000 RapidMangaDL-0.2.2/manga_dl/tools/download.py
+-rw-rw-rw-   0        0        0     7272 2023-07-23 09:35:52.000000 RapidMangaDL-0.2.2/manga_dl/tools/downloader2.py
+-rw-rw-rw-   0        0        0     8588 2023-07-14 13:14:30.000000 RapidMangaDL-0.2.2/manga_dl/tools/downloader3.py
+-rw-rw-rw-   0        0        0      188 2023-07-16 05:40:17.000000 RapidMangaDL-0.2.2/manga_dl/tools/exceptions.py
+-rw-rw-rw-   0        0        0     7137 2023-07-17 14:19:26.000000 RapidMangaDL-0.2.2/manga_dl/tools/flask_cloudflared.py
+-rw-rw-rw-   0        0        0     1308 2023-07-18 07:58:37.000000 RapidMangaDL-0.2.2/manga_dl/tools/models.py
+-rw-rw-rw-   0        0        0    10732 2023-07-23 11:03:24.000000 RapidMangaDL-0.2.2/manga_dl/tools/utils.py
+-rw-rw-rw-   0        0        0       42 2023-07-23 12:39:23.057045 RapidMangaDL-0.2.2/setup.cfg
+-rw-rw-rw-   0        0        0     2189 2023-07-23 12:30:34.000000 RapidMangaDL-0.2.2/setup.py
```

### Comparing `RapidMangaDL-0.2.1/LICENSE` & `RapidMangaDL-0.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/PKG-INFO` & `RapidMangaDL-0.2.2/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: RapidMangaDL
-Version: 0.2.1
+Version: 0.2.2
 Summary: Swiftly download manga from multiple sources.
 Home-page: https://github.com/shhossain/RapidMangaDL
 Author: sifat
 Author-email: hossain0338@gmail.com
 License: MIT
 Project-URL: Documentation, https://github.com/shhossain/RapidMangaDL
 Project-URL: Issue Tracker, https://github.com/shhossain/RapidMangaDL/issues
@@ -31,33 +31,31 @@
 License-File: LICENSE
 
 # RapidMangaDL (Manga Downloader)
 
 RapidMangaDL is a Python package that allows you to swiftly download manga from various sources. It offers multiple ways to interact with the application, including a Command Line Interface (CLI) and an Interactive CLI with a text-based prompt. Additionally, it comes with a web-based GUI to provide a user-friendly experience.
 [Suppoted Sources](/sources.md)
 
-## Installation
-
-You can download windows executable from [Latest Release](https://github.com/shhossain/RapidMangaDL/releases/latest)
-
-Or you can use `pip`:
 
+## Installation
+- Install [Python](https://www.python.org/downloads/) (3.6 or higher)
+- Go to terminal and run the following command
 ```bash
 pip install RapidMangaDL
 ```
 
 # Features
 
 Download manga from multiple sources with great speed.
 Three different ways to interact with the application: CLI, Interactive CLI, and Web-based GUI.
 Select specific chapters or a custom range for downloading.
 Choose between downloading the manga in EPUB or PDF format.
 Customize the quality of the images (10 to 100).
 
-# Interactive CLI 
+# Interactive CLI
 
 The Interactive CLI mode provides a user-friendly prompt to search for a manga, select chapters, specify the format, and set image quality.
 
 To start the Interactive CLI mode, simply run:
 
 ```bash
 manga-dl
@@ -104,28 +102,28 @@
   mode                  Mode to run (choices: gui, prompt, cli) [Web ui, Interactive CLI, CLI]
 
 optional arguments:
   -h, --help            show this help message and exit
   -s QUERY, --query QUERY
                         Search for a manga (This will move to interactive mode with the search results)
   -m MANGA, --manga MANGA
-                        Manga to download 
+                        Manga to download
                         Examples:
                         -m https://manganato.com/manga-az963307 (most reliable)
                         -m manga-id (from web gui something like this managato_uq971673)
                         -m manga-title (Match by similarity, not relaiable)
   -ss SOURCE, --source SOURCE
-                        Source to download from (Examples: -ss manganato | -ss mangakakalot | -ss manganelo | -ss mangasee123) 
+                        Source to download from (Examples: -ss manganato | -ss mangakakalot | -ss manganelo | -ss mangasee123)
   -c CHAPTERS, --chapters CHAPTERS
                         Chapters to download
-                          Examples: 
+                          Examples:
                           -c 1-10 | -c 1,2,3 | -c 1-10, 20-30 | -c 1-10, 20-30, 40, 50, 60-70 | -c latest 10 | -c Chapter 1, Chapter 2 |
                           -c https://manganato.com/manga-az963307/chapter-1-https://manganato.com/manga-az963307/chapter-2
                           -c last (last 5 chapters)
-                          
+
   -ex EXCLUDE, --exclude EXCLUDE
                         Chapters to exclude (same rules apply as --chapters)
   -f {epub,pdf}, --format {epub,pdf}
                         Format to download (choices: epub, pdf)
   -q QUALITY, --quality QUALITY
                         Quality of images (10-100)
   --host HOST           Host address of the server (default: 127.0.0.1)
@@ -159,15 +157,14 @@
 mangas = Manga.search("one piece")
 manga = mangas[0]
 manga.set_info()
 
 print(manga.title)
 ```
 
-
 Selecting chapters
 
 ```python
 
 manga.select_chapters("1-10")
 # or
 manga.select_chapters("1,2,3,4,5,6,7,8,9,10")
@@ -201,7 +198,11 @@
 ```python
 from manga_dl import app
 
 app.run()
 # or
 app.run(host="localhost", port=80) # app is a Flask app
 ```
+
+
+# Contributing
+See [CONTRIBUTING.md](CONTRIBUTING.md)
```

### Comparing `RapidMangaDL-0.2.1/README.md` & `RapidMangaDL-0.2.2/README.md`

 * *Files 16% similar despite different names*

```diff
@@ -1,31 +1,29 @@
 # RapidMangaDL (Manga Downloader)
 
 RapidMangaDL is a Python package that allows you to swiftly download manga from various sources. It offers multiple ways to interact with the application, including a Command Line Interface (CLI) and an Interactive CLI with a text-based prompt. Additionally, it comes with a web-based GUI to provide a user-friendly experience.
 [Suppoted Sources](/sources.md)
 
-## Installation
-
-You can download windows executable from [Latest Release](https://github.com/shhossain/RapidMangaDL/releases/latest)
-
-Or you can use `pip`:
 
+## Installation
+- Install [Python](https://www.python.org/downloads/) (3.6 or higher)
+- Go to terminal and run the following command
 ```bash
 pip install RapidMangaDL
 ```
 
 # Features
 
 Download manga from multiple sources with great speed.
 Three different ways to interact with the application: CLI, Interactive CLI, and Web-based GUI.
 Select specific chapters or a custom range for downloading.
 Choose between downloading the manga in EPUB or PDF format.
 Customize the quality of the images (10 to 100).
 
-# Interactive CLI 
+# Interactive CLI
 
 The Interactive CLI mode provides a user-friendly prompt to search for a manga, select chapters, specify the format, and set image quality.
 
 To start the Interactive CLI mode, simply run:
 
 ```bash
 manga-dl
@@ -72,28 +70,28 @@
   mode                  Mode to run (choices: gui, prompt, cli) [Web ui, Interactive CLI, CLI]
 
 optional arguments:
   -h, --help            show this help message and exit
   -s QUERY, --query QUERY
                         Search for a manga (This will move to interactive mode with the search results)
   -m MANGA, --manga MANGA
-                        Manga to download 
+                        Manga to download
                         Examples:
                         -m https://manganato.com/manga-az963307 (most reliable)
                         -m manga-id (from web gui something like this managato_uq971673)
                         -m manga-title (Match by similarity, not relaiable)
   -ss SOURCE, --source SOURCE
-                        Source to download from (Examples: -ss manganato | -ss mangakakalot | -ss manganelo | -ss mangasee123) 
+                        Source to download from (Examples: -ss manganato | -ss mangakakalot | -ss manganelo | -ss mangasee123)
   -c CHAPTERS, --chapters CHAPTERS
                         Chapters to download
-                          Examples: 
+                          Examples:
                           -c 1-10 | -c 1,2,3 | -c 1-10, 20-30 | -c 1-10, 20-30, 40, 50, 60-70 | -c latest 10 | -c Chapter 1, Chapter 2 |
                           -c https://manganato.com/manga-az963307/chapter-1-https://manganato.com/manga-az963307/chapter-2
                           -c last (last 5 chapters)
-                          
+
   -ex EXCLUDE, --exclude EXCLUDE
                         Chapters to exclude (same rules apply as --chapters)
   -f {epub,pdf}, --format {epub,pdf}
                         Format to download (choices: epub, pdf)
   -q QUALITY, --quality QUALITY
                         Quality of images (10-100)
   --host HOST           Host address of the server (default: 127.0.0.1)
@@ -127,15 +125,14 @@
 mangas = Manga.search("one piece")
 manga = mangas[0]
 manga.set_info()
 
 print(manga.title)
 ```
 
-
 Selecting chapters
 
 ```python
 
 manga.select_chapters("1-10")
 # or
 manga.select_chapters("1,2,3,4,5,6,7,8,9,10")
@@ -169,7 +166,11 @@
 ```python
 from manga_dl import app
 
 app.run()
 # or
 app.run(host="localhost", port=80) # app is a Flask app
 ```
+
+
+# Contributing
+See [CONTRIBUTING.md](CONTRIBUTING.md)
```

### Comparing `RapidMangaDL-0.2.1/RapidMangaDL.egg-info/PKG-INFO` & `RapidMangaDL-0.2.2/RapidMangaDL.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: RapidMangaDL
-Version: 0.2.1
+Version: 0.2.2
 Summary: Swiftly download manga from multiple sources.
 Home-page: https://github.com/shhossain/RapidMangaDL
 Author: sifat
 Author-email: hossain0338@gmail.com
 License: MIT
 Project-URL: Documentation, https://github.com/shhossain/RapidMangaDL
 Project-URL: Issue Tracker, https://github.com/shhossain/RapidMangaDL/issues
@@ -31,33 +31,31 @@
 License-File: LICENSE
 
 # RapidMangaDL (Manga Downloader)
 
 RapidMangaDL is a Python package that allows you to swiftly download manga from various sources. It offers multiple ways to interact with the application, including a Command Line Interface (CLI) and an Interactive CLI with a text-based prompt. Additionally, it comes with a web-based GUI to provide a user-friendly experience.
 [Suppoted Sources](/sources.md)
 
-## Installation
-
-You can download windows executable from [Latest Release](https://github.com/shhossain/RapidMangaDL/releases/latest)
-
-Or you can use `pip`:
 
+## Installation
+- Install [Python](https://www.python.org/downloads/) (3.6 or higher)
+- Go to terminal and run the following command
 ```bash
 pip install RapidMangaDL
 ```
 
 # Features
 
 Download manga from multiple sources with great speed.
 Three different ways to interact with the application: CLI, Interactive CLI, and Web-based GUI.
 Select specific chapters or a custom range for downloading.
 Choose between downloading the manga in EPUB or PDF format.
 Customize the quality of the images (10 to 100).
 
-# Interactive CLI 
+# Interactive CLI
 
 The Interactive CLI mode provides a user-friendly prompt to search for a manga, select chapters, specify the format, and set image quality.
 
 To start the Interactive CLI mode, simply run:
 
 ```bash
 manga-dl
@@ -104,28 +102,28 @@
   mode                  Mode to run (choices: gui, prompt, cli) [Web ui, Interactive CLI, CLI]
 
 optional arguments:
   -h, --help            show this help message and exit
   -s QUERY, --query QUERY
                         Search for a manga (This will move to interactive mode with the search results)
   -m MANGA, --manga MANGA
-                        Manga to download 
+                        Manga to download
                         Examples:
                         -m https://manganato.com/manga-az963307 (most reliable)
                         -m manga-id (from web gui something like this managato_uq971673)
                         -m manga-title (Match by similarity, not relaiable)
   -ss SOURCE, --source SOURCE
-                        Source to download from (Examples: -ss manganato | -ss mangakakalot | -ss manganelo | -ss mangasee123) 
+                        Source to download from (Examples: -ss manganato | -ss mangakakalot | -ss manganelo | -ss mangasee123)
   -c CHAPTERS, --chapters CHAPTERS
                         Chapters to download
-                          Examples: 
+                          Examples:
                           -c 1-10 | -c 1,2,3 | -c 1-10, 20-30 | -c 1-10, 20-30, 40, 50, 60-70 | -c latest 10 | -c Chapter 1, Chapter 2 |
                           -c https://manganato.com/manga-az963307/chapter-1-https://manganato.com/manga-az963307/chapter-2
                           -c last (last 5 chapters)
-                          
+
   -ex EXCLUDE, --exclude EXCLUDE
                         Chapters to exclude (same rules apply as --chapters)
   -f {epub,pdf}, --format {epub,pdf}
                         Format to download (choices: epub, pdf)
   -q QUALITY, --quality QUALITY
                         Quality of images (10-100)
   --host HOST           Host address of the server (default: 127.0.0.1)
@@ -159,15 +157,14 @@
 mangas = Manga.search("one piece")
 manga = mangas[0]
 manga.set_info()
 
 print(manga.title)
 ```
 
-
 Selecting chapters
 
 ```python
 
 manga.select_chapters("1-10")
 # or
 manga.select_chapters("1,2,3,4,5,6,7,8,9,10")
@@ -201,7 +198,11 @@
 ```python
 from manga_dl import app
 
 app.run()
 # or
 app.run(host="localhost", port=80) # app is a Flask app
 ```
+
+
+# Contributing
+See [CONTRIBUTING.md](CONTRIBUTING.md)
```

### Comparing `RapidMangaDL-0.2.1/RapidMangaDL.egg-info/SOURCES.txt` & `RapidMangaDL-0.2.2/RapidMangaDL.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -11,14 +11,15 @@
 manga_dl/__init__.py
 manga_dl/app.py
 manga_dl/main.py
 manga_dl/manga.py
 manga_dl/manga_sources/__init__.py
 manga_dl/manga_sources/base_source.py
 manga_dl/manga_sources/source1.py
+manga_dl/manga_sources/source2.py
 manga_dl/manga_sources/utils.py
 manga_dl/public/bootstrap530.css
 manga_dl/public/bootstrap530.js
 manga_dl/public/error.png
 manga_dl/public/jquery321.js
 manga_dl/public/loading-fast.gif
 manga_dl/public/manga.js
```

### Comparing `RapidMangaDL-0.2.1/cx_setup.py` & `RapidMangaDL-0.2.2/cx_setup.py`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/app.py` & `RapidMangaDL-0.2.2/manga_dl/app.py`

 * *Files 5% similar despite different names*

```diff
@@ -122,15 +122,15 @@
             results = [i.to_json() for i in mangas]
         else:
             suc = False
             error = "No query provided"
     except Exception as e:
         suc = False
         error = "Unknown error"
-        logger.error(f"Error getting search results: {e}", exc_info=True)
+        logger.error(f"Error getting search results: {e}")
 
     data = {
         "success": suc,
         "results": results,
     }
 
     if error:
@@ -197,29 +197,29 @@
     }
     return jsonify(data)
 
 
 @app.route("/api/manga/imgs", methods=["POST"])
 def manga_chapter_img():
     data = request.get_json()
-
     manga_id = data["manga_id"]
     chapter_id = data["chapter_id"]
 
     sdata = {
         "success": True,
         "imgs": [],
     }
 
     manga = Manga.from_id(manga_id)
     chapter = None
     for c in manga.chapters:
         if c.eqal_id(chapter_id):
             chapter = c
             break
+        
     if not chapter:
         sdata["success"] = False
         sdata["message"] = "Chapter not found"
         return jsonify(sdata)
 
     else:
         if chapter.source.use_selenium_in_get_chapter_img_urls:
@@ -233,15 +233,28 @@
         return jsonify(sdata)
 
 
 @app.route("/api/img_url/<url>", methods=["GET"])
 def img_url(url):
     url = url_decode(url)
     parse = urlparse(url)
-    headers["referer"] = f"{parse.scheme}://{parse.netloc}"
+    headers["Referer"] = f"{parse.scheme}://{parse.netloc}"
+
+    urlpath = Downloader.download_one(url, headers=headers, download_dir=temp_dir)
+
+    with open(urlpath.filepath, "rb") as f:
+        return f.read(), 200, {"Content-Type": "image/jpeg"}
+
+
+@app.route("/api/img_url", methods=["POST"])
+def img_url_post():
+    data = request.get_json()
+    url = data["url"]
+    referer = data["referer"]
+    headers["Referer"] = referer
 
     urlpath = Downloader.download_one(url, headers=headers, download_dir=temp_dir)
 
     with open(urlpath.filepath, "rb") as f:
         return f.read(), 200, {"Content-Type": "image/jpeg"}
```

### Comparing `RapidMangaDL-0.2.1/manga_dl/main.py` & `RapidMangaDL-0.2.2/manga_dl/main.py`

 * *Files 4% similar despite different names*

```diff
@@ -5,19 +5,19 @@
 import sys
 import logging
 
 sys.path.append(os.path.dirname(os.path.dirname(os.path.abspath(__file__))))
 
 try:
     from app import app
-    from tools import logger, run_with_cloudflared
+    from tools import logger, run_with_cloudflared, get_app_path
     from manga import Manga
 except ImportError:
     from manga_dl.app import app
-    from manga_dl.tools import logger, run_with_cloudflared
+    from manga_dl.tools import logger, run_with_cloudflared, get_app_path
     from manga_dl.manga import Manga
 
 
 from pytimedinput import timedInput
 
 
 helps = {
@@ -59,19 +59,19 @@
     # show total chapters
     print(f"Total chapters: {manga.total_chapters}")
     # ask if user wants to download all chapters or a range
     choice = qs.select(
         "Download all chapters or a range?", choices=["All", "Select", "Custom"]
     ).ask()
     if choice == "Select":
-        # show all chapters
+        title_dict = {f"{chapter.title} ({chapter.id[-3:]})": chapter for i, chapter in enumerate(manga.chapters)}
         chapters = qs.checkbox(
-            "Select chapters:", choices=[chapter.title for chapter in manga.chapters]
+            "Select chapters:", choices=list(title_dict.keys())
         ).ask()
-        manga.select_chapters(chapters)
+        manga.select_chapters([title_dict[chapter] for chapter in chapters])
     elif choice == "Custom":
         # show example of custom input
         print(helps["chapters"].replace("-c ", ""))
         print(helps["exclude"])
         print("Full Example:\n\t 1-10, 20-30, 40, 50, 60-70 -ex 2,3,4")
         # ask for custom input
         custom = qs.text("Enter custom input:").ask()
@@ -94,19 +94,24 @@
         default="100",
         validate=lambda x: True
         if x.isdigit() and int(x) in range(1, 101)
         else "Must be a number between 1-100",
     ).ask()
     quality = int(quality)
     # download
+    path = get_app_path()
     for choice in choices:
         if choice == "epub":
-            manga.create_epub(quality=quality)
+            path = manga.create_epub(quality=quality)
         elif choice == "pdf":
-            manga.create_pdf(quality=quality)
+            path = manga.create_pdf(quality=quality)
+    
+    path = os.path.dirname(path)
+    os.system(f'start {os.path.realpath(path)}')
+            
     # ask if user wants to download another manga
     choice = qs.select("Download another manga?", choices=["Yes", "No"]).ask()
     if choice == "Yes":
         prompt()
     else:
         print("Goodbye!")
 
@@ -119,14 +124,15 @@
         manga = Manga.autodetect(args.manga, args.source)
         logger.info(f"Detected manga: {manga.title} ({manga.source.current_domain})")
         answer, _ = timedInput("Continue? (y/n): ", timeout=3)
         if answer is None or answer.lower() == "n":
             print("Exiting...")
             sys.exit(0)
 
+        print(f"Total chapters: {manga.total_chapters}")
         manga.select_chapters(args.chapters, exclude=args.exclude)
 
         quality = max(10, min(100, args.quality))
         logger.info(f"Quality: {quality}")
 
         if not args.format:
             args.format = "epub"
@@ -156,15 +162,15 @@
         default="prompt",
     )
     parser.add_argument("-s", "--query", help="Search for a manga")
     parser.add_argument("-m", "--manga", help=helps["manga"])
     parser.add_argument(
         "-ss", "--source", help="Select source if multiple sources are found"
     )
-    parser.add_argument("-c", "--chapters", help=helps["chapters"])
+    parser.add_argument("-c", "--chapters", help=helps["chapters"], default="latest 10")
     parser.add_argument("-ex", "--exclude", help=helps["exclude"])
     parser.add_argument(
         "-f",
         "--format",
         choices=["epub", "pdf"],
         help="Format to download epub or pdf",
     )
@@ -226,15 +232,15 @@
     try:
         parser()
     except KeyboardInterrupt:
         print("Exiting...")
         print("Goodbye!")
         sys.exit(0)
     except Exception as e:
-        logger.error(f"Unexpected error occured {e}",)
+        logger.error(f"Unexpected error occured {e}")
         logger.info(
             "Rest assured, all downloaded files are automatically cached. Run the program again to continue downloading."
         )
         print("Exiting...")
         sys.exit(1)
```

### Comparing `RapidMangaDL-0.2.1/manga_dl/manga.py` & `RapidMangaDL-0.2.2/manga_dl/manga.py`

 * *Files 10% similar despite different names*

```diff
@@ -20,65 +20,42 @@
 from tools import (
     Downloader,
     PDFChapter,
     PDF,
     create_failure_image,
     get_file_name,
     URLFile,
-    replace_unimportant,
     logger,
-    txt_split,
     tqdm,
     driver_manager as manager,
     get_app_path,
     share_progress_bar,
 )
 
 from tools.exceptions import MangaNotFound
 
-from manga_sources import Chapter, MangaInfo, BaseSource, get_source, sources  # type: ignore
-
-# except Exception as e:
-#     from manga_dl.tools import (
-#         Downloader,
-#         PDFChapter,
-#         PDF,
-#         create_failure_image,
-#         get_file_name,
-#         URLFile,
-#         replace_unimportant,
-#         logger,
-#         http_split,
-#         tqdm,
-#         driver_manager as manager,
-#         get_app_path,
-#         share_progress_bar,
-#     )
-
-#     from manga_dl.tools.exceptions import MangaNotFound
-#     from manga_dl.manga_sources import (
-#         Chapter,
-#         MangaInfo,
-#         BaseSource,
-#         get_source,
-#         sources,
-#     )
+from manga_sources import Chapter, MangaInfo, BaseSource, get_source, sources
 
 
 app_path = get_app_path()
-temp_dir = os.path.join(app_path, "temp")
+temp_dir = os.path.join(app_path, "tmp")
 os.environ["TEMP_DIR"] = os.environ.get("TEMP_DIR", temp_dir)
 temp_dir = os.environ["TEMP_DIR"]
 if not os.path.exists(temp_dir):
     os.makedirs(temp_dir)
 
 
+class classproperty(property):
+    def __get__(self, cls, owner):
+        return classmethod(self.fget).__get__(None, owner)()  # type: ignore
+
+
 class Manga:
     """
-    Manga object
+    Manga
 
     Atributes:
     ----------
     url: str -> url of the manga
     source: Source -> Source object (see)
     id: str -> id of the manga
     title: str -> title of the manga
@@ -124,17 +101,34 @@
         self._save_chapters_str = ""
         self._pbar = None
         self._quality = 100
         # self._manager = FileManager()
 
         self.check_temp_dir()
 
-    def clear_temp_dir(self):
-        shutil.rmtree(self.temp_dir)
-        os.makedirs(self.temp_dir)
+    @staticmethod
+    def clear_cache():
+        """
+        Clears all cache
+        """
+
+        temp_dir = os.environ.get("TEMP_DIR", "tmp")
+        if os.path.exists(temp_dir):
+            shutil.rmtree(temp_dir)
+        os.makedirs(temp_dir)
+
+    @classproperty
+    def cache_path(cls):
+        return os.path.abspath(os.environ.get("TEMP_DIR", "tmp"))
+    
+    @classproperty
+    def save_path(cls):
+        return os.path.join(get_app_path(), "Downloads")
+    
+    
 
     @property
     def genre(self) -> str:
         return ", ".join(self.genres)
 
     @property
     def artist(self) -> str:
@@ -205,15 +199,17 @@
                 return cls(s.id_to_url(id))
         raise MangaNotFound(f"Could not find manga with id: {id}")
 
     @classmethod
     def autodetect(cls, inp, source: str = "") -> "Manga":
         if isinstance(inp, str):
             if "http" in inp:
-                return cls(inp)
+                manga = cls(inp)
+                manga.set_info()
+                return manga
             else:
                 most_likely = None
                 mangas = Manga.search(inp)
                 # find most likely with title with fuzz
                 ratio = 0
                 for manga in mangas:
                     if source:
@@ -384,14 +380,15 @@
 
                 text += f"{query},"
 
         text = text.strip()
         if text[-1] == "-" or text[-1] == ",":
             text = text[:-1]
 
+        
         exps = [x.strip() for x in text.split(",")]
         inputs = [x.replace(" ", "") for x in exps if x]
 
         int_range = re.compile(r"(\d+)-(\d+)")
         id_range_exists = re.compile(r"-ID_")
         http_range_exists = re.compile(r"-https?://")
         last_pat = re.compile(r"(last|latest)(\d+)?")
@@ -408,21 +405,21 @@
         for inp in inputs:
             irm = int_range.match(inp)
             if irm:
                 start = int(irm.group(1)) - 1
                 end = int(irm.group(2)) - 1
 
                 if start < 0 or end < 0:
-                    print("Invalid range", inp)
+                    logger.error("Invalid range", inp)
                     continue
                 if start > end:
-                    print("Invalid range", inp)
+                    logger.error("Invalid range", inp)
                     continue
                 if end >= len(chapters):
-                    print("Invalid range", inp)
+                    logger.error("Invalid range", inp)
 
                 matches.extend(chapters[start : end + 1])
                 continue
 
             idm = id_range_exists.search(inp)
             if idm:
                 parts = inp.split("-ID_")
@@ -430,78 +427,77 @@
                     s = parts[0].replace("ID_", "")
                     e = parts[1]
                     if s in id_dict and e in id_dict:
                         start = id_dict[s]
                         end = id_dict[e]
                         matches.extend(chapters[start : end + 1])
                     else:
-                        print(f"ID not found: {s} or {e}")
+                        logger.error(f"ID not found: {s} or {e}")
                 else:
-                    print(f"Invalid ID Range: {inp}")
+                    logger.error(f"Invalid ID Range: {inp}")
                 continue
 
             httpm = http_range_exists.search(inp)
             if httpm:
                 parts = inp.split("-http")
                 if len(parts) == 2:
                     s = parts[0]
                     e = "http" + parts[1]
                     if s in url_dict and e in url_dict:
                         start = url_dict[s]
                         end = url_dict[e]
                         matches.extend(chapters[start : end + 1])
                     else:
-                        print(f"URL not found: {s} or {e}")
+                        logger.error(f"URL not found: {s} or {e}")
                 else:
-                    print(f"Invalid URL Range: {inp}")
+                    logger.error(f"Invalid URL Range: {inp}")
                 continue
 
             lastm = last_pat.match(inp)
             if lastm:
-                start = -1
                 end = int(lastm.group(2)) if lastm.group(2) else 5
-                matches.extend(chapters[start:end])
+                matches.extend(chapters[-end:])
                 continue
 
             ism = int_single.match(inp)
             if ism:
                 start = int(ism.group(0)) - 1
                 end = start
 
                 if start < 0:
-                    print("Invalid chapter", inp)
+                    logger.error("Invalid chapter", inp)
                     continue
                 if start >= len(chapters):
-                    print("Invalid chapter", inp)
+                    logger.error("Invalid chapter", inp)
                     continue
 
                 matches.append(chapters[start])
 
                 continue
 
             idsm = id_single.match(inp)
             if idsm:
                 s = idsm.group(1)
                 if s in id_dict:
                     start = id_dict[s]
                     end = start
                     matches.append(chapters[start])
                 else:
-                    print(f"Invalid ID: {s}")
+                    logger.error(f"Invalid ID: {s}")
                 continue
 
             httpm = http_single.match(inp)
             if httpm:
                 s = httpm.group(0)
                 if s in url_dict:
                     start = url_dict[s]
                     end = start
                     matches.append(chapters[start])
                 else:
-                    print(f"Invalid URL: {s}")
+                    logger.error(f"Invalid URL: {s}")
                 continue
 
         if matches:
             return matches
         else:
             return []
 
@@ -510,16 +506,16 @@
         if len(selected_chapters) < 4:
             return ",".join([i.short_name for i in selected_chapters])
         else:
             return f"{selected_chapters[0].short_name}-{selected_chapters[-1].short_name}_total_{len(selected_chapters)}"
 
     def select_chapters(
         self,
-        selected: Union[str, int, Chapter, None],
-        exclude: Union[str, int, Chapter, None] = None,
+        selected: Union[str, int, Chapter, None, list[Union[str, int, Chapter]]],
+        exclude: Union[str, int, Chapter, None, list[Union[str, int, Chapter]]] = None,
         smerge="and",
         emerge="and",
     ):
         """
         Selects the chapters to download
 
         Parameters
@@ -535,24 +531,35 @@
             >>> manga.select_chapters("1,2,3")
             >>> manga.select_chapters("1,2,3-5", exclude="4")
             >>> manga.select_chapters("1,2,3-5", exclude="4,5")
             >>> manga.select_chapters("https://manganato.com/manga-aa123456/chapter-1-https://manganato.com/manga-aa123456/chapter-2")
         """
 
         self.set_info()
+        if isinstance(selected, list):
+            if isinstance(selected[0], Chapter):
+                self.chapters = selected  # type: ignore
+                logger.info(f"Selected {len(self.chapters)} chapters")
+                self._save_chapters_str = (
+                    f"{self._get_save_chapters_str(self.chapters)}"  # type: ignore
+                )
+                return self.chapters
 
         chapters = self.chapters_exists(selected, chapters=self.chapters, merger=smerge)
 
         if exclude:
             selected_excluded_chapters = self.chapters_exists(
                 exclude, chapters=self.chapters, merger=emerge
             )
             chapters = [i for i in chapters if i not in selected_excluded_chapters]
 
-        self.chapters = list(set(chapters))
+        chapters_dict = {i.id: i for i in self.chapters}
+        chapters = [chapters_dict[i.id] for i in chapters]
+        self.chapters = chapters
+        
         self._save_chapters_str = f"{self._get_save_chapters_str(self.chapters)}"
 
         logger.info(f"Selected {len(self.chapters)} chapters")
         return self.chapters
 
     def lower_quality(self, filename: str, quality: int):
         # add quality to filename
@@ -570,15 +577,15 @@
             img = Image.open(path)
             if img.mode != "RGB":
                 img = img.convert("RGB")
 
             img.save(qpath, optimize=True, quality=quality)
             img.close()
         except Exception as e:
-            logger.error(f"Error lowering quality: {e}", exc_info=True)
+            logger.error(f"Error lowering quality: {e}")
             logger.info(f"Saving image without lowering quality")
             shutil.copy(path, qpath)
 
         return filename, qfilename
 
     def create_failure_image(self, url):
         filename = get_file_name(f"{url}-error.png", True)
@@ -629,15 +636,15 @@
                     for future in cf.as_completed(futures):
                         bar.update(1)
                         share_progress_bar(len(self.chapters), bar.n, bar.desc)
 
         else:
             if not manager.chromedriver_installed:
                 logger.error(
-                    f"You need chrome to download from {self.source.current_domain}"
+                    f"You need chrome to download for {self.source.current_domain}"
                 )
                 logger.error("Please install chrome and try again")
                 sys.exit(1)
 
             logger.info(
                 "Using Selenium to get chapter img urls (this may take a while)"
             )
@@ -670,32 +677,32 @@
                 share_progress_bar(len(iurls), 0, "Retrying failed images")
 
             with Downloader(iurls, self.headers, self.temp_dir) as downloader:
                 downloaded_files, failed_urls = downloader.download()
 
             if downloaded_files:
                 downloaded_files, failed_files = self.check_imgs(downloaded_files)
-
                 self.remove_files([i[1] for i in failed_files])
-
                 checked_files.extend(downloaded_files)
 
                 iurls = [i[0] for i in failed_files] + failed_urls
 
             else:
                 iurls = failed_urls
 
         if iurls:
             logger.error(f"Total failed images: {len(iurls)}. Try again later")
             logger.info("Continuing with failed images")
 
-        failed_files = [
-            URLFile(i, os.path.join(self.temp_dir, self.create_failure_image(i)))
-            for i in iurls
-        ]
+
+        failed_files = []
+        with cf.ThreadPoolExecutor() as executor:
+            for result in executor.map(self.create_failure_image, iurls):
+                failed_files.append(result)
+
 
         all_files: list[URLFile] = checked_files + failed_files
 
         for img_url, dlfile in all_files:
             img_url_to_chapter[img_url].add_file((img_url, dlfile))
 
         for chapter in self.chapters:
@@ -728,15 +735,15 @@
         items = []
         for chapter in self.chapters:
             title = chapter.title
             ch_id = chapter.id
             filenames = chapter.img_filenames
             if isinstance(book, epub.EpubBook):
                 epub_chapter = epub.EpubHtml(
-                    title=ch_id, file_name=f"{ch_id}.xhtml", lang="en"
+                    title=title, file_name=f"{ch_id}.xhtml", lang="en"
                 )
 
                 epub_chapter.content = self.chapter_template(title, filenames)
                 book.add_item(epub_chapter)
                 items.append(epub_chapter)
 
                 for filename in filenames:
```

### Comparing `RapidMangaDL-0.2.1/manga_dl/manga_sources/__init__.py` & `RapidMangaDL-0.2.2/manga_dl/manga_sources/__init__.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,14 +1,17 @@
 from .source1 import MangaNato, Bato, ONEkissmanga, BaseSource, Chapter, MangaInfo
+from .source2 import MangaKakalot # Error getting chapter imgs
 
 sources = [MangaNato, Bato, ONEkissmanga]
 
+
 class SourceNotFound(Exception):
     pass
 
+
 def all_domains() -> list[str]:
     return [domain for source in sources for domain in source.all_domains()]
 
 
 def get_source(url: str) -> BaseSource:
     for source in sources:
         if source.is_valid(url):
```

### Comparing `RapidMangaDL-0.2.1/manga_dl/manga_sources/source1.py` & `RapidMangaDL-0.2.2/manga_dl/manga_sources/source1.py`

 * *Files 2% similar despite different names*

```diff
@@ -6,33 +6,33 @@
 import os
 
 sys.path.append(os.path.dirname(os.path.dirname(os.path.abspath(__file__))))
 
 from selenium.webdriver.common.by import By
 
 
-from tools.utils import logger
+from tools.utils import logger, Driver
 from tools.exceptions import MangaNotFound, InvalidMangaUrl
 from bs4 import BeautifulSoup
 from fake_headers import Headers
 import re
 from urllib.parse import quote_plus
 from .base_source import BaseSource
 from .utils import MangaInfo, Chapter, scraper, static_exists, exists
 
 
 class MangaNato(BaseSource):
     domain = "manganato.com"
     alternate_domains = ["chapmanganato.com"]
+    manga_format = "https://{alternate_domains[0]}/manga-{ID}"
 
     def __init__(self, url: str):
         url = MangaNato.valid_url(url)
         super().__init__(url)
-        self.headers["referer"] = f"https://{self.alternate_domains[0]}/"
-
+        self.headers["Referer"] = f"https://{self.alternate_domains[0]}/"
 
     @staticmethod
     def valid_url(url: str) -> str:
         parse = urlparse(url)
         parts = parse.path.replace("//", "/").split("/")[1:]
 
         if len(parts) == 1:
@@ -85,19 +85,14 @@
     @property
     def _id(self) -> str:
         url = self.url
         if self.url.endswith("/"):
             url = self.url[:-1]
         return url.split("/")[-1].replace("manga-", "")
 
-
-    @classmethod
-    def id_to_url(cls,id: str) -> str:
-        return super().id_to_url(id).replace(cls.domain, cls.alternate_domains[0]).replace("manga/", "manga-")
-
     @exists
     def get_info(self) -> MangaInfo:
         try:
             res = scraper.get(self.url)
             soup = BeautifulSoup(res.text, "html.parser")  # type: ignore
 
             # story-info-left
@@ -199,39 +194,37 @@
                 f"Error getting chapter images for {chapter_url}: {e}",
             )
             imgs = []
 
         return imgs
 
 
-
 class ONEkissmanga(BaseSource):
     domain = "1stkissmanga.me"
     alternate_domains = ["1stkissmanga.com", "1stkissmanga.io"]
 
     def __init__(self, url: str):
         super().__init__(url)
 
     @property
     def _id(self) -> str:
         parts = self.url.split("/")
         return parts[-1] or parts[-2]
 
-
     @staticmethod
     @static_exists("https://1stkissmanga.me/wp-admin/admin-ajax.php")
     def search(query: str) -> list[MangaInfo]:
         search_url = "https://1stkissmanga.me/wp-admin/admin-ajax.php"
         data = {"action": "wp-manga-search-manga", "title": query}
         results = []
         try:
             headers = Headers().generate()
             headers.update(
                 {
-                    "referer": "https://1stkissmanga.me/",
+                    "Referer": "https://1stkissmanga.me/",
                     "x-requested-with": "XMLHttpRequest",
                     "content-type": "application/x-www-form-urlencoded;",
                     "origin": "https://1stkissmanga.me",
                 }
             )
 
             res = scraper.post(search_url, data=data, headers=headers)
@@ -324,33 +317,33 @@
             imgs = []
 
         return imgs
 
 
 class Bato(BaseSource):
     domain = "bato.to"
-    alternate_domains = ["battwo.com", "batotwo.com", "batotoo.com", "mto.to", "comiko.net", "mangatoto.com"]
+    alternate_domains = [
+        "battwo.com",
+        "batotwo.com",
+        "batotoo.com",
+        "mto.to",
+        "comiko.net",
+        "mangatoto.com",
+    ]
+    manga_format = "https://{domain}/series/{ID.replace('_', '/')}"
 
     def __init__(self, url: str):
         super().__init__(url)
         self.use_selenium_in_get_chapter_img_urls = True
 
-
     @property
     def _id(self) -> str:
         parts = self.url.split("/")
         return "_".join(parts[-2:])
 
-
-    @staticmethod
-    def id_to_url(id: str) -> str:
-        return (
-            f"https://{Bato.domain}/series/{id.replace('bato_', '').replace('_', '/')}"
-        )
-
     @staticmethod
     @static_exists("https://bato.to/search")
     def search(query: str) -> list[MangaInfo]:
         url = "https://bato.to/search?word=" + quote_plus(query)
 
         results = []
         try:
@@ -408,14 +401,38 @@
                 results.append(m)
 
         except Exception as e:
             logger.error(f"Error searching for {query} in {Bato.domain}: {e}")
 
         return results
 
+    @staticmethod
+    def parse_views(txt) -> str:
+        pat = re.compile(r"(\d+\.?\d*)([KMBT]?)")
+        matches = pat.findall(txt)
+        if not matches:
+            return txt
+        else:
+            total = 0
+            for m in matches:
+                num = float(m[0])
+                if m[1] == "K":
+                    num *= 1000
+                elif m[1] == "M":
+                    num *= 1000000
+                elif m[1] == "B":
+                    num *= 1000000000
+                elif m[1] == "T":
+                    num *= 1000000000000
+
+                total += num
+            # convert to k
+            total = int(total / 1000)
+            return f"{total}K"
+
     @exists
     def get_info(self) -> MangaInfo:
         try:
             res = scraper.get(self.url)
             soup = BeautifulSoup(res.text, "html.parser")
 
             # .attr-cover
@@ -483,14 +500,15 @@
                 views: str = ""
                 date: str = ""
                 if extra:
                     views = extra.select("span i")  # type: ignore
                     views = " ".join([i.text for i in views])  # type: ignore
                     date = extra.select_one("i.ps-3").text.strip()  # type: ignore
 
+                views = Bato.parse_views(views)
                 chapters.append(
                     Chapter(
                         title=chtitle, url=link, views=views, date=date, source=self
                     )
                 )
 
             m = MangaInfo(title=title, url=self.url)
@@ -510,25 +528,34 @@
         except Exception as e:
             logger.error(f"Error getting manga info for {self.url}: {e}")
             raise MangaNotFound(f"Manga not found: {self.url}")
 
     @exists
     def get_chapter_img_urls(self, chapter_url: str, **kw) -> list[str]:
         results = []
+        got_driver = False
+        driver: Driver = kw.get("driver", None)
         for i in range(2):
             try:
-                driver = kw.get("driver", None)
                 if not driver:
-                    raise Exception(f"Cannot get img urls in {Bato.domain} without driver")
+                    raise Exception(
+                        f"Cannot get img urls in {self.domain} without driver"
+                    )
+
+                got_driver = True
+
                 driver.get(chapter_url)
                 imgs = driver.find_elements(By.XPATH, "//div[@id='viewer']//img")
                 for img in imgs:
                     results.append(img.get_attribute("src"))
-                    
+
                 if results:
                     break
             except Exception as e:
                 logger.error(f"Error getting chapter image urls for {chapter_url}: {e}")
 
+        if got_driver:
+            driver.usable = True
+
         if "pbar" in kw:
             kw["pbar"].update(1)
         return results
```

### Comparing `RapidMangaDL-0.2.1/manga_dl/manga_sources/utils.py` & `RapidMangaDL-0.2.2/manga_dl/manga_sources/utils.py`

 * *Files 16% similar despite different names*

```diff
@@ -161,17 +161,15 @@
 
         if url2.endswith("/"):
             url2 = url2[:-1]
 
         return url1 == url2
 
     def eqal_id(self, other: Union["Chapter", str]) -> bool:
-        id1 = self.id
-        id2 = other.id if isinstance(other, Chapter) else self.source.chapter_id(other)
-        return id1 == id2
+        return self.id == other
 
     @property
     def short_name(self):
         # if number in title, retun it or short title
         if self.title:
             if re.search(r"\d+", self.title):
                 # return number
@@ -247,14 +245,15 @@
             self.views = value
         elif index == 3:
             self.date = value
 
     def to_json(self):
         return {
             "url": self.url,
+            "id": self.id,
             "title": self.title,
             "views": self.views,
             "date": self.date,
             "source": self.source.to_json(),
         }
 
     @classmethod
@@ -267,36 +266,87 @@
             data["title"],
             data["views"],
             data["date"],
         )
 
 
 class MangaInfo:
-    def __init__(self, title: str, url: str):
+    """
+    MangaInfo class
+
+    Attributes:
+        title (str): Title of the manga
+        url (str): Url of the manga
+        cover_url (str): Url of the cover image
+        alternative_titles (list): List of alternative titles
+        authors (list): List of authors
+        status (str): Status of the manga
+        genres (list): List of genres
+        description (str): Description of the manga
+        chapters (list): List of chapters
+        total_chapters (int): Total chapters
+        last_chapter (str): Last chapter
+        rank (str): Rank of the manga
+        original_language (str): Original language of the manga
+        translated_language (str): Translated language of the manga
+        artists (list): List of artists
+        last_updated (str): Last updated date
+        views (str): Total views
+        rating (str): Rating of the manga
+        tags (list): List of tags
+        type (str): Type of the manga
+        total_comments (str): Total comments
+        total_bookmarked (str): Total bookmarked
+    """
+
+    def __init__(
+        self,
+        title: str,
+        url: str,
+        cover_url: str = "",
+        alternative_titles: list = [],
+        authors: list = [],
+        status: str = "",
+        genres: list = [],
+        description: str = "",
+        chapters: list = [],
+        last_chapter: str = "",
+        rank: str = "",
+        original_language: str = "",
+        translated_language: str = "",
+        artists: list = [],
+        last_updated: str = "",
+        views: str = "",
+        rating: str = "",
+        tags: list = [],
+        type: str = "",
+        total_comments: str = "",
+        total_bookmarked: str = "",
+    ):
         self.title = title
         self.url = url
-        self.cover_url = ""
-        self.alternative_titles = []
-        self.authors = []
-        self.status = ""
-        self.genres = []
-        self.description = ""
-        self.chapters: list[Chapter] = []
-        self.last_chapter = ""
-        self.rank = ""
-        self.original_language = ""
-        self.translated_language = ""
-        self.artists = []
-        self.last_updated = ""
-        self.views = ""
-        self.rating = ""
-        self.tags = []
-        self.type = ""
-        self.total_comments = ""
-        self.total_bookmarked = ""
+        self.cover_url = cover_url
+        self.alternative_titles = alternative_titles
+        self.authors = authors
+        self.status = status
+        self.genres = genres
+        self.description = description
+        self.chapters: list = chapters
+        self.last_chapter = last_chapter
+        self.rank = rank
+        self.original_language = original_language
+        self.translated_language = translated_language
+        self.artists = artists
+        self.last_updated = last_updated
+        self.views = views
+        self.rating = rating
+        self.tags = tags
+        self.type = type
+        self.total_comments = total_comments
+        self.total_bookmarked = total_bookmarked
 
     @classmethod
     def from_json(cls, data):
         info = cls(data["title"], data["url"])
         info.cover_url = data.get("cover_url", "")
         info.alternative_titles = data.get("alternative_titles", [])
         info.authors = data.get("authors", [])
```

### Comparing `RapidMangaDL-0.2.1/manga_dl/public/bootstrap530.css` & `RapidMangaDL-0.2.2/manga_dl/public/bootstrap530.css`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/public/bootstrap530.js` & `RapidMangaDL-0.2.2/manga_dl/public/bootstrap530.js`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/public/error.png` & `RapidMangaDL-0.2.2/manga_dl/public/error.png`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/public/jquery321.js` & `RapidMangaDL-0.2.2/manga_dl/public/jquery321.js`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/public/loading-fast.gif` & `RapidMangaDL-0.2.2/manga_dl/public/loading-fast.gif`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/public/manga.js` & `RapidMangaDL-0.2.2/manga_dl/public/manga.js`

 * *Files 20% similar despite different names*

#### js-beautify {}

```diff
@@ -17,16 +17,72 @@
     } else {
         views = parseFloat(views);
     }
     return views;
 }
 
 function getTime(str) {
-    const date = new Date(str);
-    return date.getTime();
+    let time = null;
+    if (str.includes("ago")) {
+        // change a year ago or a day ago, etc to 1 year ago or 1 day ago
+        const replacers = {
+            "a year ago": "1 year ago",
+            "a day ago": "1 day ago",
+            "an hour ago": "1 hour ago",
+            "a minute ago": "1 minute ago",
+            "a second ago": "1 second ago",
+            "just now": "1 second ago",
+        };
+
+        for (const [key, value] of Object.entries(replacers)) {
+            // convert to lower case
+            const lowerStr = str.toLowerCase();
+            if (lowerStr.includes(key)) {
+                str = str.replace(key, value);
+                break;
+            }
+        }
+
+        const ago = parseInt(str, 10);
+        if (!isNaN(ago)) {
+            // if days,hours,minutes,seconds ago
+            const currentDate = new Date();
+            if (str.includes("year")) {
+                currentDate.setFullYear(currentDate.getFullYear() - ago);
+            } else if (str.includes("days")) {
+                currentDate.setDate(currentDate.getDate() - ago);
+            } else if (str.includes("hours")) {
+                currentDate.setHours(currentDate.getHours() - ago);
+            } else if (str.includes("min")) {
+                currentDate.setMinutes(currentDate.getMinutes() - ago);
+            } else if (str.includes("sec")) {
+                currentDate.setSeconds(currentDate.getSeconds() - ago);
+            }
+            time = currentDate.getTime();
+        }
+    } else if (str.includes("Today")) {
+        const hoursAgo = parseInt(relativeTime, 10);
+        if (!isNaN(hoursAgo)) {
+            const currentDate = new Date();
+            currentDate.setHours(currentDate.getHours() - hoursAgo);
+            time = currentDate.getTime();
+        }
+    } else if (str.includes("Yesterday")) {
+        const hoursAgo = parseInt(relativeTime, 10);
+        if (!isNaN(hoursAgo)) {
+            const currentDate = new Date();
+            currentDate.setHours(currentDate.getHours() - hoursAgo);
+            time = currentDate.getTime();
+        }
+    } else {
+        const date = new Date(str);
+        time = date.getTime();
+    }
+
+    return isNaN(time) ? 0 : time;
 }
 
 // if click on the image show the modal
 $("#slider-items").on("click", ".carousel-item", function() {
     // get the image src
     const src = $(this).find("img").attr("src");
     // set the image src to the modal
@@ -106,15 +162,17 @@
     value = `${value}%`;
     $("#progress").css("width", value);
     $("#progress").text(progress.desc);
     $("#progress-value").text(value);
     if (value == "100%") {
         $("#downloadBtn").find("span").text("Download");
     } else {
-        $("#downloadBtn").find("span").text(`${progress.desc} ${value} ${progress.current}/${progress.total}`);
+        $("#downloadBtn")
+            .find("span")
+            .text(`${progress.desc} ${value} ${progress.current}/${progress.total}`);
     }
 
     console.log("Changing progress", value);
 }
 
 function updateProgress() {
     $.ajax({
```

### Comparing `RapidMangaDL-0.2.1/manga_dl/public/search.js` & `RapidMangaDL-0.2.2/manga_dl/public/search.js`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/public/style.css` & `RapidMangaDL-0.2.2/manga_dl/public/style.css`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/templates/chapter.html` & `RapidMangaDL-0.2.2/manga_dl/templates/chapter.html`

 * *Files 26% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 {% extends "layout.html" %} {% block content %}
 <br />
-<h3>{{ chapter.title }} <span id="manga-title">{{ manga.title }}</span></h3>
+<h3>{{ chapter.title }} <a id="manga-title" href="/manga/{{ manga.id }}">{{ manga.title }}</a></h3>
 <br />
 
 <!-- select option for chapters -->
 <div class="row">
   <div class="col-md-12">
     <div class="d-flex justify-content-between">
       <select class="form-select" id="chapters">
@@ -119,37 +119,62 @@
 
 
 {% endblock %} {% block scripts %}
 <script>
   document.title = "{{ manga.title }} - {{ chapter.title }}";
 
   // on click manga-title
-  $("#manga-title").on("click", function () {
-    window.location.href = "/manga/" + "{{ manga.id }}";
-  });
+  // $("#manga-title").on("click", function () {
+  //   window.location.href = "/manga/" + "{{ manga.id }}";
+  // });
 
   const imgs = document.querySelectorAll("img");
 
   function url_encode(s) {
     return s
       .split("")
       .map((i) => i.charCodeAt(0))
       .join("-");
   }
 
+  const referer = "{{ manga.headers['Referer'] }}";
+
+
+
   imgs.forEach(async (img) => {
     const url = img.alt;
 
     // /api/img_url/<url>
-    fetch(`/api/img_url/${url_encode(url)}`)
-      .then((res) => res.blob())
-      .then((data) => {
-        const url = URL.createObjectURL(data);
-        img.src = url;
-      });
+    // fetch(`/api/img_url/${url_encode(url)}`)
+    //   .then((res) => res.blob())
+    //   .then((data) => {
+    //     const url = URL.createObjectURL(data);
+    //     img.src = url;
+    //   });
+
+    // post 
+    try {
+      const res = await fetch("/api/img_url", {
+      method: "POST",
+      headers: {
+        "Content-Type": "application/json",
+      },
+      body: JSON.stringify({ url: url, referer: referer }),
+    });
+    
+    const data = await res.blob();
+    
+    const url2 = URL.createObjectURL(data);
+    img.src = url2;
+    }
+    catch (err) {
+      img.src = "/public/error.png";
+    }
+    
+
   });
 
   $("#chapters").change(function () {
     const url = $(this).val();
     window.location.href = url;
   });
 </script>
```

### Comparing `RapidMangaDL-0.2.1/manga_dl/templates/layout.html` & `RapidMangaDL-0.2.2/manga_dl/templates/layout.html`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/templates/manga.html` & `RapidMangaDL-0.2.2/manga_dl/templates/manga.html`

 * *Files 2% similar despite different names*

```diff
@@ -297,14 +297,16 @@
 
 {% endblock %} {% block scripts %}
 <script src="/public/manga.js"></script>
 <script>
   document.title = "{{ manga.title }}";
   const mangaID = "{{ manga.id }}";
 
+  $("#sort").click();
+
  async function setFaviconFromImageUrl(imageUrl) {
   const canvas = document.createElement('canvas');
   const ctx = canvas.getContext('2d');
   const img = new Image();
 
   img.crossOrigin = 'anonymous';
   img.onload = function() {
@@ -363,26 +365,24 @@
     ...sortedChapters.slice(
       Math.floor(totalChapters / 2),
       Math.floor(totalChapters / 2 + 2)
     ),
     ...sortedChapters.slice(-1),
   ];
 
-  const topChapterIDs = topChapters.map((chapter) => {
-    return chapter.id;
-  });
+  const topChapterIds = topChapters.map((chapter) => chapter.id);
 
   let flag = true;
-  topChapterIds.forEach(async (chapterID) => {
+  topChapterIds.forEach((chapter_id) => {
     const id = "{{ manga.id | safe}}";
     const url = "/api/manga/imgs";
     $.ajax({
       type: "POST",
       url: url,
-      data: JSON.stringify({ manga_id: id, chapter_id: chapterID }),
+      data: JSON.stringify({ manga_id: id, chapter_id: chapter_id }),
       contentType: "application/json",
       dataType: "json",
       success: function (data) {
         if (data.success) {
           const imgs = data.imgs;
 
           // random select img from middle of array
```

### Comparing `RapidMangaDL-0.2.1/manga_dl/templates/search.html` & `RapidMangaDL-0.2.2/manga_dl/templates/search.html`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/tools/create_pdf.py` & `RapidMangaDL-0.2.2/manga_dl/tools/create_pdf.py`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/tools/download.py` & `RapidMangaDL-0.2.2/manga_dl/tools/download.py`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/tools/downloader2.py` & `RapidMangaDL-0.2.2/manga_dl/tools/downloader2.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,8 +1,10 @@
 import os
+import shutil
+import re
 import json
 import logging
 from multiprocessing import Manager
 import hashlib
 import aiofiles
 import requests
 from fake_headers import Headers
@@ -37,62 +39,81 @@
         headers=None,
         download_dir=None,
         check_exists=True,
         jpg_compress=True,
     ):
         self.urls = urls
         self.headers = headers or Headers().generate()
-        self.download_dir = download_dir or os.path.join(os.getcwd(), "downloads")
+        self.download_dir = download_dir or os.path.join(os.getcwd(), "tmp")
         if not os.path.exists(self.download_dir):
             os.mkdir(self.download_dir)
 
         self.downloaded_files = Manager().list()
         self.failed_urls = Manager().list()
         self.current_progress = 0
         self.total_urls = len(urls)
 
-    def get_filename(self, url):
-        return hashlib.sha1(url.encode()).hexdigest() + ".jpg"
+    @staticmethod
+    def is_file(url):
+        # check if url is not a url
+        if not re.match(r"^https?://", url):
+            if os.path.exists(url) or os.path.exists(compress_file_path(url)):
+                return True
+        return False
 
     async def download_file(self, session: aiohttp.ClientSession, url: str, pbar):
-        filename = self.get_filename(url)
-        filepath = os.path.join(self.download_dir, filename)
+        url = url.strip()
+        if not self.is_file(url):
+            filename = get_file_name(url)
+            filepath = os.path.join(self.download_dir, filename)
+        else:
+            filepath = url
+
+        # print("Downloading", url, filepath)
+
         cmp_filepath = compress_file_path(filepath)
+        isCompressed = False
+        isFileExists = False
         if os.path.exists(filepath):
-            self.downloaded_files.append(URLFile(url, filepath))
+            isFileExists = True
 
         elif os.path.exists(cmp_filepath):
-            self.downloaded_files.append(URLFile(url, cmp_filepath))
+            isFileExists = True
+            filepath = cmp_filepath
+            isCompressed = True
 
-        else:
+        failed = False
+        if not isFileExists:
             tmp_path = filepath + ".tmp"
             try:
                 timeout = aiohttp.ClientTimeout(
                     total=auto_scaled_divide(self.total_urls)
                 )
                 async with session.get(url, timeout=timeout) as response:
                     async with aiofiles.open(tmp_path, mode="wb") as f:
                         async for chunk in response.content.iter_chunked(1024 * 1024):
                             if chunk:
                                 await f.write(chunk)
+                shutil.move(tmp_path, filepath)
+            except Exception as e:
+                logging.error(f"Failed to download {url}: {e}")
+                self.failed_urls.append(url)
+                failed = True
 
-                os.rename(tmp_path, filepath)
-                compressed = jpeg_compress(filepath, cmp_filepath)
-                if compressed:
-                    os.remove(filepath)
-                    filepath = cmp_filepath
-                else:
-                    raise Exception(f"Failed to compress {filepath}")
+        if not isCompressed and not failed:
+            compressed = jpeg_compress(filepath, cmp_filepath)
+            if compressed:
+                os.remove(filepath)
+                filepath = cmp_filepath
+            else:
+                logger.error(f"Failed to compress {filepath} {url}")
 
-                self.downloaded_files.append(URLFile(url, filepath))
+        if not failed:
+            self.downloaded_files.append(URLFile(url, filepath))
 
-            except Exception as e:
-                print(f"Failed to download {url}: {e}")
-                self.failed_urls.append(url)
-                return
         pbar.update(1)
         share_progress_bar(pbar.total, pbar.n, pbar.desc)
         self.total_urls -= 1
 
     async def download_all(self):
         with tqdm(total=len(self.urls), desc="Downloading") as pbar:
             timeout = aiohttp.ClientTimeout(total=auto_scaled_divide(self.total_urls))
@@ -102,42 +123,62 @@
                 tasks = []
                 for url in self.urls:
                     task = asyncio.create_task(self.download_file(session, url, pbar))
                     tasks.append(task)
                 await asyncio.gather(*tasks)
 
     @staticmethod
-    def download_one(url, headers, download_dir):
-        filename = get_file_name(url)
-        filepath = os.path.join(download_dir, filename)
+    def download_one(url, headers, download_dir) -> URLFile:
+        url = url.strip()
+        if not Downloader.is_file(url):
+            filename = get_file_name(url)
+            filepath = os.path.join(download_dir, filename)
+        else:
+            filepath = url
+
         cmp_filepath = compress_file_path(filepath)
+        isCompressed = False
+        isFileExists = False
         if os.path.exists(filepath):
-            return URLFile(url, filepath)
+            isFileExists = True
+
         elif os.path.exists(cmp_filepath):
-            return URLFile(url, cmp_filepath)
+            isFileExists = True
+            filepath = cmp_filepath
+            isCompressed = True
 
-        else:
+        failed = False
+        if not isFileExists:
             try:
                 response = requests.get(url, headers=headers)
                 with open(filepath, "wb") as f:
                     for chunk in response.iter_content(chunk_size=1024 * 1024):
                         if chunk:
                             f.write(chunk)
-                compressed = jpeg_compress(filepath, cmp_filepath)
-                if compressed:
-                    os.remove(filepath)
-                    filepath = cmp_filepath
-                return URLFile(url, filepath)
+
             except Exception as e:
                 logging.error(f"Failed to download {url}: {e}")
-                filepath = os.path.join(download_dir, get_file_name(f"{url}_failed"))
-                if not os.path.exists(filepath):
-                    create_failure_image(filepath, url)
+                failed = True
 
-                return URLFile(url, filepath)
+        if not isCompressed and not failed:
+            compressed = jpeg_compress(filepath, cmp_filepath)
+            if compressed:
+                os.remove(filepath)
+                filepath = cmp_filepath
+            else:
+                logger.error(f"Failed to compress {filepath} {url}")
+
+        if not failed:
+            return URLFile(url, filepath)
+        else:
+            filepath = os.path.join(download_dir, get_file_name(f"{url}_failed"))
+            if not os.path.exists(filepath):
+                create_failure_image(filepath, url)
+
+            return URLFile(url, filepath)
 
     def delete_tmp_files(self):
         for file in os.listdir(self.download_dir):
             if file.endswith(".tmp"):
                 safe_remove(os.path.join(self.download_dir, file))
 
     def download(self) -> tuple[list[URLFile], list[str]]:
```

### Comparing `RapidMangaDL-0.2.1/manga_dl/tools/downloader3.py` & `RapidMangaDL-0.2.2/manga_dl/tools/downloader3.py`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/tools/flask_cloudflared.py` & `RapidMangaDL-0.2.2/manga_dl/tools/flask_cloudflared.py`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/tools/models.py` & `RapidMangaDL-0.2.2/manga_dl/tools/models.py`

 * *Files identical despite different names*

### Comparing `RapidMangaDL-0.2.1/manga_dl/tools/utils.py` & `RapidMangaDL-0.2.2/manga_dl/tools/utils.py`

 * *Files 6% similar despite different names*

```diff
@@ -26,15 +26,14 @@
 import chromedriver_autoinstaller
 
 
 _utils_path = os.path.dirname(os.path.abspath(__file__))
 error_img_path = os.path.join(os.path.dirname(_utils_path), "public", "error.png")
 
 
-
 def share_progress_bar(total_size: float, current_value: float, desc: str = ""):
     os.environ["PROGRESS_BAR"] = json.dumps(
         {"total": total_size, "current": current_value, "desc": desc}
     )
 
 
 # get a path for appdata
@@ -91,16 +90,18 @@
         levelname = record.levelname
         message = record.msg
         color = self._colors.get(levelname, "")
         message = f"{color}{message}{colorama.Fore.RESET}"
         record.msg = message
         return super().format(record)
 
+
 _logger: list[logging.Logger] = []
 
+
 def get_logger() -> logging.Logger:
     if _logger:
         return _logger[0]
     else:
         logger_name = os.environ.get("LOGGER_NAME", "manga")
         logging_level = os.environ.get("LOGGING_LEVEL", "DEBUG")
         logger = logging.getLogger(logger_name)
@@ -118,16 +119,18 @@
             logger.addHandler(file_handler)
             logger.addHandler(stream_handler)
 
         logger.propagate = False
         _logger.append(logger)
         return logger
 
+
 logger = get_logger()
 
+
 def create_failure_image(failure_path, url):
     img = Image.open(error_img_path)
 
     # add url in the 80% of height and centered
     draw = ImageDraw.Draw(img)
     font = ImageFont.truetype("arial.ttf", 40)
 
@@ -201,21 +204,28 @@
     rest = []
     for p in parts[1:]:
         rest.append(f"{split}{p}")
     return [url1] + rest
 
 
 class Driver(webdriver.Chrome):
-    def __init__(self, options, *args, **kwargs):
+    def __init__(self, options:webdriver.ChromeOptions, *args, **kwargs):
         self.options = options
         self.args = args
         self.kwargs = kwargs
         self.running = False
         self.usable = True
         self._init = False
+    
+    def add_option(self, option):
+        self.options.add_argument(option)
+    
+    def remove_option(self, option):
+        self.options._arguments.remove(option) if option in self.options._arguments else None
+    
 
     def init(self):
         super().__init__(options=self.options, *self.args, **self.kwargs)
         self.running = True
 
     def get(self, url):
         if not self._init:
@@ -231,26 +241,34 @@
         if driver_count == -1:
             driver_count = (os.cpu_count() or 2) // 2
 
         self.driver_count = driver_count
         self.manager: dict[str, Driver] = {}
         self.chromedriver_installed = True
 
+        self._chromedrive_checked = False
+        self._quited = False
+
+        self.lock = threading.Lock()
+
+    def check_for_chromedriver(self):
+        if self._chromedrive_checked:
+            return
+
         if os.environ.get("DRIVER_INSTALLATION_CHECKED", "0") == "0":
             try:
                 chromedriver_autoinstaller.install()
             except Exception as e:
                 self.chromedriver_installed = False
                 logger.error(f"Looks like chrome is not installed: {e}")
             os.environ["DRIVER_INSTALLATION_CHECKED"] = "1"
-
-            
-        self.lock = threading.Lock()
+        self._chromedrive_checked = True
 
     def create_driver(self):
+        self.check_for_chromedriver()
         return Driver(self.driver_options)
 
     def total_running(self):
         total = 0
         for key, value in self.manager.items():
             if value.running:
                 total += 1
@@ -263,61 +281,80 @@
         return None, None
 
     @property
     def driver_options(self):
         options = webdriver.ChromeOptions()
         options.add_argument("--headless")
         options.add_argument("--blink-settings=imagesEnabled=false")
+        options.add_argument("--disable-extensions")
         options.add_argument("--no-sandbox")
         options.add_argument("--disable-dev-shm-usage")
+        # options.add_argument("start-maximized")
+        # options.add_experimental_option("excludeSwitches", ["enable-automation"])
+        # options.add_experimental_option('useAutomationExtension', False)
 
         return options
 
     def get_driver(self) -> tuple[str, webdriver.Chrome]:
         with self.lock:
             return self.wait_for_driver()
 
     def wait_for_driver(self) -> tuple[str, webdriver.Chrome]:
         while True:
+            ky, dr = self.get_usable()
+            if ky:
+                return ky, dr # type: ignore
+            
             total = self.total_running()
             if total < self.driver_count:
                 key = get_hash(str(uuid4()))
                 driver = self.create_driver()
                 driver.usable = False
                 self.manager[key] = driver
                 return key, driver
-            else:
-                ky, dr = self.get_usable()
-                if ky is not None:
-                    return ky, dr  # type: ignore
+            
             time.sleep(0.1)
 
     def release_driver(self, key: str):
         with self.lock:
             if key in self.manager:
                 self.manager[key].usable = True
 
     def _quit(self):
         logger.info("Quitting drivers...")
 
+        flag = False
         for key, value in self.manager.items():
-            value.close()
+            try:
+                value.quit()
+            except Exception as e:
+                logger.error(f"Error while quitting driver {key}: {e}")
+                flag = True
+        
+        if flag:
+            logger.error("Drivers quited with errors")
+        else:
+            logger.info("Drivers quited successfully")
 
-        logger.info("Drivers quit successfully")
         self.manager = {}
+        self._quited = False
 
     def quit(self) -> threading.Thread:
+        if self._quited:
+            return None # type: ignore
+        
         t = threading.Thread(target=self._quit)
         t.daemon = True
         t.start()
+        self._quited = True
         return t
 
 
 @atexit.register
 def quit_drivers():
     try:
         driver_manager.quit()
     except Exception as e:
         logger.error(f"Error while quitting drivers: {e}")
 
-driver_manager = DriverManager(2)
 
+driver_manager = DriverManager(2)
```

### Comparing `RapidMangaDL-0.2.1/setup.py` & `RapidMangaDL-0.2.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 # setup.py
 from setuptools import setup, find_packages
 
 
 package_name = "RapidMangaDL"
-package_version = "0.2.1"
+package_version = "0.2.2"
 package_description = "Swiftly download manga from multiple sources."
 package_author = "sifat"
 package_author_email = "hossain0338@gmail.com"
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
```

