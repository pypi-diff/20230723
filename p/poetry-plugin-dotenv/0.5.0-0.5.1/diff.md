# Comparing `tmp/poetry_plugin_dotenv-0.5.0.tar.gz` & `tmp/poetry_plugin_dotenv-0.5.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "poetry_plugin_dotenv-0.5.0.tar", max compression
+gzip compressed data, was "poetry_plugin_dotenv-0.5.1.tar", max compression
```

## Comparing `poetry_plugin_dotenv-0.5.0.tar` & `poetry_plugin_dotenv-0.5.1.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0     1077 2023-06-02 19:26:20.715203 poetry_plugin_dotenv-0.5.0/LICENSE
--rw-r--r--   0        0        0     8640 2023-06-02 19:26:20.715203 poetry_plugin_dotenv-0.5.0/README.md
--rw-r--r--   0        0        0     5555 2023-06-02 19:26:42.763749 poetry_plugin_dotenv-0.5.0/pyproject.toml
--rw-r--r--   0        0        0      699 2023-06-02 19:26:42.683747 poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/__init__.py
--rw-r--r--   0        0        0      335 2023-06-02 19:26:20.719203 poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/dotenv/__init__.py
--rw-r--r--   0        0        0     5235 2023-06-02 19:26:20.719203 poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/dotenv/core.py
--rw-r--r--   0        0        0     5983 2023-06-02 19:26:20.719203 poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/dotenv/parsers.py
--rw-r--r--   0        0        0     1445 2023-06-02 19:26:20.719203 poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/dotenv/variables.py
--rw-r--r--   0        0        0     3469 2023-06-02 19:26:20.719203 poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/plugin.py
--rw-r--r--   0        0        0        0 2023-06-02 19:26:20.719203 poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/py.typed
--rw-r--r--   0        0        0    10577 1970-01-01 00:00:00.000000 poetry_plugin_dotenv-0.5.0/PKG-INFO
+-rw-r--r--   0        0        0     1077 2023-07-22 22:05:45.441478 poetry_plugin_dotenv-0.5.1/LICENSE
+-rw-r--r--   0        0        0     8943 2023-07-22 22:05:45.441478 poetry_plugin_dotenv-0.5.1/README.md
+-rw-r--r--   0        0        0     5721 2023-07-22 22:05:45.445478 poetry_plugin_dotenv-0.5.1/pyproject.toml
+-rw-r--r--   0        0        0      699 2023-07-22 22:05:45.445478 poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/__init__.py
+-rw-r--r--   0        0        0      335 2023-07-22 22:05:45.445478 poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/dotenv/__init__.py
+-rw-r--r--   0        0        0     5235 2023-07-22 22:05:45.445478 poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/dotenv/core.py
+-rw-r--r--   0        0        0     5983 2023-07-22 22:05:45.445478 poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/dotenv/parsers.py
+-rw-r--r--   0        0        0     1445 2023-07-22 22:05:45.445478 poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/dotenv/variables.py
+-rw-r--r--   0        0        0     3469 2023-07-22 22:05:45.445478 poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/plugin.py
+-rw-r--r--   0        0        0        0 2023-07-22 22:05:45.445478 poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/py.typed
+-rw-r--r--   0        0        0    10880 1970-01-01 00:00:00.000000 poetry_plugin_dotenv-0.5.1/PKG-INFO
```

### Comparing `poetry_plugin_dotenv-0.5.0/LICENSE` & `poetry_plugin_dotenv-0.5.1/LICENSE`

 * *Files identical despite different names*

### Comparing `poetry_plugin_dotenv-0.5.0/README.md` & `poetry_plugin_dotenv-0.5.1/README.md`

 * *Files 14% similar despite different names*

```diff
@@ -25,16 +25,16 @@
 <p align="center">
     <a href="https://github.com/psf/black">
         <img alt="black" src="https://img.shields.io/badge/code_style-black-black.svg?logo=windowsterminal">
     </a>
     <a href="https://pycqa.github.io/isort/index.html">
         <img alt="isort" src="https://img.shields.io/badge/imports-isort-black.svg?logo=windowsterminal">
     </a>
-    <a href="https://wemake-python-stylegui.de/en/latest/index.html">
-        <img alt="wemake" src="https://img.shields.io/badge/style-wemake-black.svg?logo=windowsterminal">
+    <a href="https://beta.ruff.rs/docs/">
+        <img alt="ruff" src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/charliermarsh/ruff/main/assets/badge/v2.json">
     </a>
     <a href="https://mypy.readthedocs.io/en/stable/index.html">
         <img alt="mypy" src="https://img.shields.io/badge/mypy-checked-success.svg?logo=python">
     </a>
     <a href="https://github.com/semantic-release/semantic-release">
         <img alt="semantic_release" src="https://img.shields.io/badge/semantic_release-angular-e10079?logo=semantic-release">
     </a>
@@ -70,14 +70,17 @@
     </a>
     <a href="https://pypi.org/project/poetry-plugin-dotenv">
         <img alt="downloads" src="https://img.shields.io/pypi/dm/poetry-plugin-dotenv?logo=pypi">
     </a>
     <a href="https://github.com/volopivoshenko/poetry-plugin-dotenv/">
         <img alt="stars" src="https://img.shields.io/github/stars/volopivoshenko/poetry-plugin-dotenv?logo=github">
     </a>
+    <a href="https://wakatime.com/badge/user/9862508c-0a86-427a-929c-46186f2d191a/project/36344bbb-7f11-4dcd-a36d-e54c81551119">
+        <img alt="wakatime" src="https://wakatime.com/badge/user/9862508c-0a86-427a-929c-46186f2d191a/project/36344bbb-7f11-4dcd-a36d-e54c81551119.svg">
+    </a>
 </p>
 
 <p align="center">
     <a href="https://github.com/volopivoshenko/poetry-plugin-dotenv/issues">
         <img alt="issues" src="https://img.shields.io/github/issues/volopivoshenko/poetry-plugin-dotenv?logo=github">
     </a>
     <a href="https://github.com/volopivoshenko/poetry-plugin-dotenv/issues">
```

#### html2text {}

```diff
@@ -1,12 +1,12 @@
                                     [logo]
                 [license] [python] [pypi] [release] [numpydoc]
-              [black] [isort] [wemake] [mypy] [semantic_release]
+               [black] [isort] [ruff] [mypy] [semantic_release]
           [dependabot] [CI] [CD] [CodeQL] [Dependency_Review] [wheel]
-                 [coverage] [codeclimate] [downloads] [stars]
+            [coverage] [codeclimate] [downloads] [stars] [wakatime]
               [issues] [issues] [pr] [pr] [contributors] [commit]
              [buymeacoffee] [standwithukraine] [standwithukraine]
 - [ð® Overview](#-overview) - [âï¸ Installation](#ï¸-installation) -
 [ð©ð»âð» Usage](#-usage) # ð® Overview `poetry-plugin-dotenv` - is
 the plugin that automatically loads environment variables from a dotenv file
 into the environment before `poetry` commands are run. **This plugin doesn't
 have any dependencies, but therefore it also supports features that `python-
```

### Comparing `poetry_plugin_dotenv-0.5.0/pyproject.toml` & `poetry_plugin_dotenv-0.5.1/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "poetry-plugin-dotenv"
-version = "0.5.0"
+version = "0.5.1"
 description = "poetry-plugin-dotenv - is the plugin that automatically loads environment variables from a dotenv file into the environment before poetry commands are run."
 license = "MIT"
 authors = ["Volodymyr Pivoshenko <volodymyr.pivoshenko@gmail.com>"]
 maintainers = ["Volodymyr Pivoshenko <volodymyr.pivoshenko@gmail.com>"]
 keywords = [
     "python",
     "pypi",
@@ -49,60 +49,65 @@
 "Say Thanks!" = "https://www.buymeacoffee.com/volopivoshenko"
 
 [tool.poetry.dependencies]
 python = ">=3.8.1,<4.0"
 poetry = "^1.5.1"
 
 [tool.poetry.group.dev.dependencies]
-pre-commit = "^3.3.1"
-poethepoet = "^0.20.0"
-ipython = "^8.12.0"
+pre-commit = "^3.3.3"
+poethepoet = ">=0.20,<0.22"
 ipdb = "^0.13.13"
-nitpick = "^0.33.1"
+nitpick = "^0.33.2"
 
 [tool.poetry.group.formatters.dependencies]
 isort = "^5.12.0"
 black = "^23.3.0"
-pyupgrade = "^3.4.0"
-yesqa = "^1.4.0"
+pyupgrade = "^3.7.0"
+yesqa = "^1.5.0"
 
 [tool.poetry.group.linters.dependencies]
-mypy = "^1.3.0"
-ruff = "^0.0.270"
-deptry = "^0.11.0"
+mypy = "^1.4.0"
+ruff = "^0.0.275"
+deptry = "^0.12.0"
 memestra = "^0.2.1"
-codespell = "^2.2.4"
+codespell = "^2.2.5"
 
 [tool.poetry.group.tests.dependencies]
-pytest = "^7.3.1"
+pytest = "^7.4.0"
 xdoctest = "^1.1.1"
 pytest-lazy-fixture = "^0.6.3"
 pytest-codeblocks = "^0.16.1"
-pytest-mock = "^3.10.0"
+pytest-mock = "^3.11.1"
 pytest-cov = "^4.1.0"
 pytest-sugar = "^0.9.7"
 coverage = { version = "^7.2.7", extras = ["toml"] }
 sh = "^2.0.4"
 
 [tool.poetry.group.ci.dependencies]
-python-semantic-release = "^7.34.3"
+python-semantic-release = "8.0.3"
 
 [tool.poetry.plugins."poetry.application.plugin"]
 poetry-plugin-dotenv = "poetry_plugin_dotenv.plugin:DotenvPlugin"
 
 [tool.semantic_release]
 branch = "main"
 changelog_file = "CHANGELOG.md"
 build_command = "poetry build"
 dist_path = "dist"
 upload_to_repository = false
 upload_to_release = true
 remove_dist = false
-version_toml = "pyproject.toml:tool.poetry.version"
+version_toml = ["pyproject.toml:tool.poetry.version"]
 version_variable = ["src/poetry_plugin_dotenv/__init__.py:__version__"]
+commit_author = "github-actions <github-actions@github.com>"
+
+[tool.semantic_release.commit_parser_options]
+major_tags = ["feat"]
+minor_tags = ["fix", "perf"]
+patch_tags = ["docs"]
 
 [tool.nitpick]
 style = "github://volopivoshenko/cookiecutter-poetry/nitpick/nitpick.toml"
 
 [tool.isort]
 profile = "black"
 line_length = 100
```

### Comparing `poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/__init__.py` & `poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/__init__.py`

 * *Files identical despite different names*

### Comparing `poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/dotenv/core.py` & `poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/dotenv/core.py`

 * *Files identical despite different names*

### Comparing `poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/dotenv/parsers.py` & `poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/dotenv/parsers.py`

 * *Files identical despite different names*

### Comparing `poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/dotenv/variables.py` & `poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/dotenv/variables.py`

 * *Files identical despite different names*

### Comparing `poetry_plugin_dotenv-0.5.0/src/poetry_plugin_dotenv/plugin.py` & `poetry_plugin_dotenv-0.5.1/src/poetry_plugin_dotenv/plugin.py`

 * *Files identical despite different names*

### Comparing `poetry_plugin_dotenv-0.5.0/PKG-INFO` & `poetry_plugin_dotenv-0.5.1/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: poetry-plugin-dotenv
-Version: 0.5.0
+Version: 0.5.1
 Summary: poetry-plugin-dotenv - is the plugin that automatically loads environment variables from a dotenv file into the environment before poetry commands are run.
 Home-page: https://github.com/volopivoshenko/poetry-plugin-dotenv
 License: MIT
 Keywords: python,pypi,poetry,plugin,plugins,poetry-plugin,poetry-plugins,env,dotenv,cross-platform,hacktoberfest
 Author: Volodymyr Pivoshenko
 Author-email: volodymyr.pivoshenko@gmail.com
 Maintainer: Volodymyr Pivoshenko
@@ -62,16 +62,16 @@
 <p align="center">
     <a href="https://github.com/psf/black">
         <img alt="black" src="https://img.shields.io/badge/code_style-black-black.svg?logo=windowsterminal">
     </a>
     <a href="https://pycqa.github.io/isort/index.html">
         <img alt="isort" src="https://img.shields.io/badge/imports-isort-black.svg?logo=windowsterminal">
     </a>
-    <a href="https://wemake-python-stylegui.de/en/latest/index.html">
-        <img alt="wemake" src="https://img.shields.io/badge/style-wemake-black.svg?logo=windowsterminal">
+    <a href="https://beta.ruff.rs/docs/">
+        <img alt="ruff" src="https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/charliermarsh/ruff/main/assets/badge/v2.json">
     </a>
     <a href="https://mypy.readthedocs.io/en/stable/index.html">
         <img alt="mypy" src="https://img.shields.io/badge/mypy-checked-success.svg?logo=python">
     </a>
     <a href="https://github.com/semantic-release/semantic-release">
         <img alt="semantic_release" src="https://img.shields.io/badge/semantic_release-angular-e10079?logo=semantic-release">
     </a>
@@ -107,14 +107,17 @@
     </a>
     <a href="https://pypi.org/project/poetry-plugin-dotenv">
         <img alt="downloads" src="https://img.shields.io/pypi/dm/poetry-plugin-dotenv?logo=pypi">
     </a>
     <a href="https://github.com/volopivoshenko/poetry-plugin-dotenv/">
         <img alt="stars" src="https://img.shields.io/github/stars/volopivoshenko/poetry-plugin-dotenv?logo=github">
     </a>
+    <a href="https://wakatime.com/badge/user/9862508c-0a86-427a-929c-46186f2d191a/project/36344bbb-7f11-4dcd-a36d-e54c81551119">
+        <img alt="wakatime" src="https://wakatime.com/badge/user/9862508c-0a86-427a-929c-46186f2d191a/project/36344bbb-7f11-4dcd-a36d-e54c81551119.svg">
+    </a>
 </p>
 
 <p align="center">
     <a href="https://github.com/volopivoshenko/poetry-plugin-dotenv/issues">
         <img alt="issues" src="https://img.shields.io/github/issues/volopivoshenko/poetry-plugin-dotenv?logo=github">
     </a>
     <a href="https://github.com/volopivoshenko/poetry-plugin-dotenv/issues">
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: poetry-plugin-dotenv Version: 0.5.0 Summary:
+Metadata-Version: 2.1 Name: poetry-plugin-dotenv Version: 0.5.1 Summary:
 poetry-plugin-dotenv - is the plugin that automatically loads environment
 variables from a dotenv file into the environment before poetry commands are
 run. Home-page: https://github.com/volopivoshenko/poetry-plugin-dotenv License:
 MIT Keywords: python,pypi,poetry,plugin,plugins,poetry-plugin,poetry-
 plugins,env,dotenv,cross-platform,hacktoberfest Author: Volodymyr Pivoshenko
 Author-email: volodymyr.pivoshenko@gmail.com Maintainer: Volodymyr Pivoshenko
 Maintainer-email: volodymyr.pivoshenko@gmail.com Requires-Python: >=3.8.1,<4.0
@@ -22,17 +22,17 @@
 github.com/volopivoshenko/poetry-plugin-dotenv/issues Project-URL: Repository,
 https://github.com/volopivoshenko/poetry-plugin-dotenv Project-URL: Releases,
 https://github.com/volopivoshenko/poetry-plugin-dotenv/releases Project-URL:
 Say Thanks!, https://www.buymeacoffee.com/volopivoshenko Description-Content-
 Type: text/markdown
                                     [logo]
                 [license] [python] [pypi] [release] [numpydoc]
-              [black] [isort] [wemake] [mypy] [semantic_release]
+               [black] [isort] [ruff] [mypy] [semantic_release]
           [dependabot] [CI] [CD] [CodeQL] [Dependency_Review] [wheel]
-                 [coverage] [codeclimate] [downloads] [stars]
+            [coverage] [codeclimate] [downloads] [stars] [wakatime]
               [issues] [issues] [pr] [pr] [contributors] [commit]
              [buymeacoffee] [standwithukraine] [standwithukraine]
 - [ð® Overview](#-overview) - [âï¸ Installation](#ï¸-installation) -
 [ð©ð»âð» Usage](#-usage) # ð® Overview `poetry-plugin-dotenv` - is
 the plugin that automatically loads environment variables from a dotenv file
 into the environment before `poetry` commands are run. **This plugin doesn't
 have any dependencies, but therefore it also supports features that `python-
```

