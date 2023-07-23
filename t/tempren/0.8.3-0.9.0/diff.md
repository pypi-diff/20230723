# Comparing `tmp/tempren-0.8.3.tar.gz` & `tmp/tempren-0.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tempren-0.8.3.tar", max compression
+gzip compressed data, was "tempren-0.9.0.tar", max compression
```

## Comparing `tempren-0.8.3.tar` & `tempren-0.9.0.tar`

### file list

```diff
@@ -1,37 +1,37 @@
--rw-r--r--   0        0        0    35149 2023-02-25 11:38:38.421471 tempren-0.8.3/LICENSE
--rw-r--r--   0        0        0     4970 2023-02-25 11:38:38.421471 tempren-0.8.3/README.md
--rw-r--r--   0        0        0     1632 2023-02-25 11:38:38.421471 tempren-0.8.3/pyproject.toml
--rw-r--r--   0        0        0       22 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/__init__.py
--rwxr-xr-x   0        0        0    20400 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/cli.py
--rw-r--r--   0        0        0     3214 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/file_filters.py
--rw-r--r--   0        0        0     1696 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/file_sorters.py
--rw-r--r--   0        0        0     6577 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/filesystem.py
--rw-r--r--   0        0        0     2061 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/path_generator.py
--rw-r--r--   0        0        0    12457 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/pipeline.py
--rw-r--r--   0        0        0        0 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/tags/__init__.py
--rw-r--r--   0        0        0     2937 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/tags/audio.py
--rw-r--r--   0        0        0    14834 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/tags/core.py
--rw-r--r--   0        0        0     1291 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/tags/filesystem.py
--rw-r--r--   0        0        0     3008 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/tags/gpx.py
--rw-r--r--   0        0        0     1881 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/tags/hash.py
--rw-r--r--   0        0        0     5725 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/tags/image.py
--rw-r--r--   0        0        0     6585 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/tags/text.py
--rw-r--r--   0        0        0     3088 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/tags/video.py
--rw-r--r--   0        0        0        0 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/__init__.py
--rw-r--r--   0        0        0     1064 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/TagTemplateLexer.g4
--rw-r--r--   0        0        0     6080 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/TagTemplateLexer.interp
--rw-r--r--   0        0        0    20134 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/TagTemplateLexer.py
--rw-r--r--   0        0        0      326 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/TagTemplateLexer.tokens
--rw-r--r--   0        0        0     1184 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/TagTemplateParser.g4
--rw-r--r--   0        0        0     4296 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/TagTemplateParser.interp
--rw-r--r--   0        0        0    39550 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/TagTemplateParser.py
--rw-r--r--   0        0        0      326 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/TagTemplateParser.tokens
--rw-r--r--   0        0        0     1811 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/TagTemplateParserVisitor.py
--rw-r--r--   0        0        0        0 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/__init__.py
--rwxr-xr-x   0        0        0      261 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/generate.sh
--rwxr-xr-x   0        0        0      266 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/grammar/generate_for_grun.sh
--rw-r--r--   0        0        0     1209 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/path_generators.py
--rw-r--r--   0        0        0    19686 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/tree_builder.py
--rw-r--r--   0        0        0    11754 2023-02-25 11:38:38.421471 tempren-0.8.3/tempren/template/tree_elements.py
--rw-r--r--   0        0        0     6328 1970-01-01 00:00:00.000000 tempren-0.8.3/setup.py
--rw-r--r--   0        0        0     6665 1970-01-01 00:00:00.000000 tempren-0.8.3/PKG-INFO
+-rw-r--r--   0        0        0    35149 2023-02-25 11:38:44.066713 tempren-0.9.0/LICENSE
+-rw-r--r--   0        0        0     4970 2023-02-25 11:38:44.066713 tempren-0.9.0/README.md
+-rw-r--r--   0        0        0     1632 2023-02-25 11:38:44.066713 tempren-0.9.0/pyproject.toml
+-rw-r--r--   0        0        0       22 2023-02-25 11:38:44.066713 tempren-0.9.0/tempren/__init__.py
+-rwxr-xr-x   0        0        0    20400 2023-02-25 11:38:44.066713 tempren-0.9.0/tempren/cli.py
+-rw-r--r--   0        0        0     3214 2023-02-25 11:38:44.066713 tempren-0.9.0/tempren/file_filters.py
+-rw-r--r--   0        0        0     1696 2023-02-25 11:38:44.066713 tempren-0.9.0/tempren/file_sorters.py
+-rw-r--r--   0        0        0     6577 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/filesystem.py
+-rw-r--r--   0        0        0     2061 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/path_generator.py
+-rw-r--r--   0        0        0    12457 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/pipeline.py
+-rw-r--r--   0        0        0        0 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/tags/__init__.py
+-rw-r--r--   0        0        0     2937 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/tags/audio.py
+-rw-r--r--   0        0        0    14834 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/tags/core.py
+-rw-r--r--   0        0        0     1291 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/tags/filesystem.py
+-rw-r--r--   0        0        0     3008 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/tags/gpx.py
+-rw-r--r--   0        0        0     1881 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/tags/hash.py
+-rw-r--r--   0        0        0     5725 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/tags/image.py
+-rw-r--r--   0        0        0     6585 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/tags/text.py
+-rw-r--r--   0        0        0     3088 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/tags/video.py
+-rw-r--r--   0        0        0        0 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/__init__.py
+-rw-r--r--   0        0        0     1064 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/TagTemplateLexer.g4
+-rw-r--r--   0        0        0     6080 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/TagTemplateLexer.interp
+-rw-r--r--   0        0        0    20134 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/TagTemplateLexer.py
+-rw-r--r--   0        0        0      326 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/TagTemplateLexer.tokens
+-rw-r--r--   0        0        0     1184 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/TagTemplateParser.g4
+-rw-r--r--   0        0        0     4296 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/TagTemplateParser.interp
+-rw-r--r--   0        0        0    39550 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/TagTemplateParser.py
+-rw-r--r--   0        0        0      326 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/TagTemplateParser.tokens
+-rw-r--r--   0        0        0     1811 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/TagTemplateParserVisitor.py
+-rw-r--r--   0        0        0        0 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/__init__.py
+-rwxr-xr-x   0        0        0      261 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/generate.sh
+-rwxr-xr-x   0        0        0      266 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/grammar/generate_for_grun.sh
+-rw-r--r--   0        0        0     1209 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/path_generators.py
+-rw-r--r--   0        0        0    19686 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/tree_builder.py
+-rw-r--r--   0        0        0    11754 2023-02-25 11:38:44.070713 tempren-0.9.0/tempren/template/tree_elements.py
+-rw-r--r--   0        0        0     6328 1970-01-01 00:00:00.000000 tempren-0.9.0/setup.py
+-rw-r--r--   0        0        0     6665 1970-01-01 00:00:00.000000 tempren-0.9.0/PKG-INFO
```

### Comparing `tempren-0.8.3/LICENSE` & `tempren-0.9.0/LICENSE`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/README.md` & `tempren-0.9.0/README.md`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/pyproject.toml` & `tempren-0.9.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "tempren"
-version = "0.8.3"
+version = "0.9.0"
 description = "Template-based renaming utility"
 readme = "README.md"
 license = "GPL-3.0-or-later"
 authors = ["Paweł Żukowski <p.z.idlecode@gmail.com>"]
 homepage = "https://github.com/idle-code/tempren"
 keywords = ["batch-renaming", "cli", "filename"]
 classifiers = [
```

### Comparing `tempren-0.8.3/tempren/cli.py` & `tempren-0.9.0/tempren/cli.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/file_filters.py` & `tempren-0.9.0/tempren/file_filters.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/file_sorters.py` & `tempren-0.9.0/tempren/file_sorters.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/filesystem.py` & `tempren-0.9.0/tempren/filesystem.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/path_generator.py` & `tempren-0.9.0/tempren/path_generator.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/pipeline.py` & `tempren-0.9.0/tempren/pipeline.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/tags/audio.py` & `tempren-0.9.0/tempren/tags/audio.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/tags/core.py` & `tempren-0.9.0/tempren/tags/core.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/tags/filesystem.py` & `tempren-0.9.0/tempren/tags/filesystem.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/tags/gpx.py` & `tempren-0.9.0/tempren/tags/gpx.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/tags/hash.py` & `tempren-0.9.0/tempren/tags/hash.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/tags/image.py` & `tempren-0.9.0/tempren/tags/image.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/tags/text.py` & `tempren-0.9.0/tempren/tags/text.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/tags/video.py` & `tempren-0.9.0/tempren/tags/video.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/template/grammar/TagTemplateLexer.g4` & `tempren-0.9.0/tempren/template/grammar/TagTemplateLexer.g4`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/template/grammar/TagTemplateLexer.interp` & `tempren-0.9.0/tempren/template/grammar/TagTemplateLexer.interp`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/template/grammar/TagTemplateLexer.py` & `tempren-0.9.0/tempren/template/grammar/TagTemplateLexer.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/template/grammar/TagTemplateParser.g4` & `tempren-0.9.0/tempren/template/grammar/TagTemplateParser.g4`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/template/grammar/TagTemplateParser.interp` & `tempren-0.9.0/tempren/template/grammar/TagTemplateParser.interp`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/template/grammar/TagTemplateParser.py` & `tempren-0.9.0/tempren/template/grammar/TagTemplateParser.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/template/grammar/TagTemplateParserVisitor.py` & `tempren-0.9.0/tempren/template/grammar/TagTemplateParserVisitor.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/template/path_generators.py` & `tempren-0.9.0/tempren/template/path_generators.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/template/tree_builder.py` & `tempren-0.9.0/tempren/template/tree_builder.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/tempren/template/tree_elements.py` & `tempren-0.9.0/tempren/template/tree_elements.py`

 * *Files identical despite different names*

### Comparing `tempren-0.8.3/setup.py` & `tempren-0.9.0/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -24,15 +24,15 @@
 {'video': ['pymediainfo>=5.1.0,<6.0.0']}
 
 entry_points = \
 {'console_scripts': ['tempren = tempren.cli:throwing_main']}
 
 setup_kwargs = {
     'name': 'tempren',
-    'version': '0.8.3',
+    'version': '0.9.0',
     'description': 'Template-based renaming utility',
     'long_description': '# Tempren - template-based file renaming utility\n\n![run-tests](https://github.com/idle-code/tempren/actions/workflows/run-tests.yml/badge.svg)\n[![codecov](https://codecov.io/gh/idle-code/tempren/branch/develop/graph/badge.svg?token=1CR2PX6GYB)](https://codecov.io/gh/idle-code/tempren)\n[![Maintainability](https://api.codeclimate.com/v1/badges/d67f6ebe698b79d75279/maintainability)](https://codeclimate.com/github/idle-code/tempren/maintainability)\n[![PyPI version](https://badge.fury.io/py/tempren.svg)](https://badge.fury.io/py/tempren)\n[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/idle-code/tempren/develop.svg)](https://results.pre-commit.ci/latest/github/idle-code/tempren/develop)\n\n`tempren` is a powerful file renaming utility that uses flexible template expressions to create new file paths and names.\nNew file paths can be based on original filename, created independently or from the underlying file\'s tags.\nRich library of built-in tag extraction modules helps with tagging many common file types.\n\n## Features\n- Template-based filename/path generation\n- Audio/Video/Images/etc metadata extraction\n- Configurable, metadata-based file selection (filtering)\n- Metadata-based sorting\n\n## Installation\nCurrently only PyPI installation is supported, just run following command:\n```commandline\n$ pip install [--user] tempren\n```\n\n## Documentation\n[Manual](MANUAL.md) gives a tour of all `tempren` features and (until quickstart is created) should work as a guide.\n\n<!--\n## [Quickstart](QUICKSTART.md)\nFor quick, five-minute introduction to the most of `tempren` features please refer to the [quickstart](QUICKSTART.md) page.\nYou can also take a look on the following examples.\n-->\n\n## Examples\n**Note: When experimenting on your own please use `--dry-run` flag!** \\\n**Tempren will not override your files by default but invalid template can mangle their names.**\n\n<details>\n<summary>Cleaning up names for sensitive (e.g. FAT32) filesystems</summary>\n\n```commandline\n$ tempren --recursive --name "%Strip(){%Base()|%Unidecode()|%Sanitize()|%Collapse()}%Ext()" ./Some\\ OST/\nRenamed: Disk 1/14 - 接近.flac\n     to: Disk 1/14 - Jie Jin.flac\nRenamed: Disk 1/02 - なつのあお.flac\n     to: Disk 1/02 - natsunoao.flac\nRenamed: Disk 1/11 - 灯火-re.flac\n     to: Disk 1/11 - Deng Huo -re.flac\nRenamed: Disk 1/05 - 記録.flac\n     to: Disk 1/05 - Ji Lu.flac\nRenamed: Disk 1/10 - むかしむかし、あるところに.flac\n     to: Disk 1/10 - mukashimukashi, arutokoroni.flac\nRenamed: Disk 1/09 - 阿良句のテーマ(ハイ).flac\n     to: Disk 1/09 - A Liang Ju notema(hai).flac\n...\n```\n</details>\n\n<details>\n<summary>Adding resolution to the image files</summary>\n\n```commandline\n$ tempren --name "%Base()_%Image.Width()x%Image.Height()%Ext()" ~/Pictures/Wallpapers\nRenamed: 0sa5yfiskqr21.jpg\n     to: 0sa5yfiskqr21_3728x4660.jpg\nRenamed: rkgjq6883fp81.jpg\n     to: rkgjq6883fp81_3024x4032.jpg\nRenamed: lcrkvphf28911.jpg\n     to: lcrkvphf28911_4016x4684.jpg\nRenamed: y6nzcv55k3851.jpg\n     to: y6nzcv55k3851_3784x5670.jpg\nRenamed: 1211740803547.jpg\n     to: 1211740803547_1200x1109.jpg\n...\n```\n</details>\n\n<details>\n<summary>Sorting files into directories based on their MIME type</summary>\n\n```commandline\n$ tempren -d --path "%Capitalize(){%Mime(subtype)}/%Name()" ~/Downloads\nRenamed: dotnet-install.sh\n     to: X-shellscript/dotnet-install.sh\nRenamed: openrgb_0.7_amd64_buster_6128731.deb\n     to: Vnd.debian.binary-package/openrgb_0.7_amd64_buster_6128731.deb\nRenamed: prometheus-2.26.0.linux-amd64.tar.gz\n     to: Gzip/prometheus-2.26.0.linux-amd64.tar.gz\nRenamed: nldb remote.zip\n     to: Zip/nldb remote.zip\nRenamed: artifacts.zip\n     to: Zip/artifacts.zip\nRenamed: 2021-06-11_12-09-34.webm\n     to: X-matroska/2021-06-11_12-09-34.webm\nRenamed: antlr-4.9.2-complete.jar\n     to: Java-archive/antlr-4.9.2-complete.jar\n...\n```\n</details>\n\n<details>\n<summary>Adding checksums to the names of the audio files</summary>\n\n```commandline\n$ tempren --filter-template "%IsMime(\'audio\')" --name "%Base() [%Upper(){%Crc32()}]%Ext()" ./Roger\\ Subirana\\ Mata\\ -\\ Point\\ of\\ no\\ return\nRenamed: 10-169205-Roger Subirana Mata-Island of light.mp3\n     to: 10-169205-Roger Subirana Mata-Island of light [08E46C33].mp3\nRenamed: 12-169207-Roger Subirana Mata-Tales of trees.mp3\n     to: 12-169207-Roger Subirana Mata-Tales of trees [33EFEC5E].mp3\nRenamed: 11-169206-Roger Subirana Mata-Requiem.mp3\n     to: 11-169206-Roger Subirana Mata-Requiem [5E48759B].mp3\nRenamed: 05-168950-Roger Subirana Mata-The mask.mp3\n     to: 05-168950-Roger Subirana Mata-The mask [045DBC19].mp3\nRenamed: 03-168948-Roger Subirana Mata-Thryst.mp3\n     to: 03-168948-Roger Subirana Mata-Thryst [5D23E43B].mp3\n...\n```\n</details>\n\n\n## Contributing\nIf you noticed a bug or have an idea for a new tag please open an issue with appropriate tags.\nIf you would like to contribute to the development you can visit [contributing page](CONTRIBUTING.md) designed specially for that.\n',
     'author': 'Paweł Żukowski',
     'author_email': 'p.z.idlecode@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://github.com/idle-code/tempren',
```

### Comparing `tempren-0.8.3/PKG-INFO` & `tempren-0.9.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tempren
-Version: 0.8.3
+Version: 0.9.0
 Summary: Template-based renaming utility
 Home-page: https://github.com/idle-code/tempren
 License: GPL-3.0-or-later
 Keywords: batch-renaming,cli,filename
 Author: Paweł Żukowski
 Author-email: p.z.idlecode@gmail.com
 Requires-Python: >=3.8,<4.0
```

