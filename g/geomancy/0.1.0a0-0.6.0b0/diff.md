# Comparing `tmp/geomancy-0.1.0a0.tar.gz` & `tmp/geomancy-0.6.0b0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "geomancy-0.1.0a0.tar", last modified: Thu Jul 20 09:41:23 2023, max compression
+gzip compressed data, was "geomancy-0.6.0b0.tar", last modified: Sun Jul 23 20:55:18 2023, max compression
```

## Comparing `geomancy-0.1.0a0.tar` & `geomancy-0.6.0b0.tar`

### file list

```diff
@@ -1,29 +1,48 @@
-drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-20 09:41:23.843379 geomancy-0.1.0a0/
--rw-r--r--   0 jlorieau   (501) staff       (20)     1747 2023-07-19 19:04:50.000000 geomancy-0.1.0a0/.gitignore
--rw-r--r--   0 jlorieau   (501) staff       (20)    35142 2023-07-19 19:00:29.000000 geomancy-0.1.0a0/LICENSE.md
--rw-r--r--   0 jlorieau   (501) staff       (20)      501 2023-07-20 09:41:23.842839 geomancy-0.1.0a0/PKG-INFO
--rw-r--r--   0 jlorieau   (501) staff       (20)      178 2023-07-20 09:21:57.000000 geomancy-0.1.0a0/README.md
-drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-20 09:41:23.837389 geomancy-0.1.0a0/geomancy/
--rw-r--r--   0 jlorieau   (501) staff       (20)       62 2023-07-20 09:41:09.000000 geomancy-0.1.0a0/geomancy/__init__.py
-drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-20 09:41:23.840428 geomancy-0.1.0a0/geomancy/checks/
--rw-r--r--   0 jlorieau   (501) staff       (20)      141 2023-07-19 20:42:53.000000 geomancy-0.1.0a0/geomancy/checks/__init__.py
--rw-r--r--   0 jlorieau   (501) staff       (20)     1684 2023-07-19 21:25:59.000000 geomancy-0.1.0a0/geomancy/checks/base.py
--rw-r--r--   0 jlorieau   (501) staff       (20)     3246 2023-07-19 21:27:07.000000 geomancy-0.1.0a0/geomancy/checks/env.py
--rw-r--r--   0 jlorieau   (501) staff       (20)      215 2023-07-19 19:57:06.000000 geomancy-0.1.0a0/geomancy/checks/utils.py
-drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-20 09:41:23.841078 geomancy-0.1.0a0/geomancy/cli/
--rw-r--r--   0 jlorieau   (501) staff       (20)      117 2023-07-19 19:47:31.000000 geomancy-0.1.0a0/geomancy/cli/__init__.py
--rw-r--r--   0 jlorieau   (501) staff       (20)     1326 2023-07-19 20:08:04.000000 geomancy-0.1.0a0/geomancy/cli/messages.py
-drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-20 09:41:23.841821 geomancy-0.1.0a0/geomancy/constructors/
--rw-r--r--   0 jlorieau   (501) staff       (20)       67 2023-07-19 21:16:17.000000 geomancy-0.1.0a0/geomancy/constructors/__init__.py
--rw-r--r--   0 jlorieau   (501) staff       (20)     2365 2023-07-19 21:25:08.000000 geomancy-0.1.0a0/geomancy/constructors/dict.py
-drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-20 09:41:23.839002 geomancy-0.1.0a0/geomancy.egg-info/
--rw-r--r--   0 jlorieau   (501) staff       (20)      501 2023-07-20 09:41:23.000000 geomancy-0.1.0a0/geomancy.egg-info/PKG-INFO
--rw-r--r--   0 jlorieau   (501) staff       (20)      465 2023-07-20 09:41:23.000000 geomancy-0.1.0a0/geomancy.egg-info/SOURCES.txt
--rw-r--r--   0 jlorieau   (501) staff       (20)        1 2023-07-20 09:41:23.000000 geomancy-0.1.0a0/geomancy.egg-info/dependency_links.txt
--rw-r--r--   0 jlorieau   (501) staff       (20)       36 2023-07-20 09:41:23.000000 geomancy-0.1.0a0/geomancy.egg-info/requires.txt
--rw-r--r--   0 jlorieau   (501) staff       (20)        9 2023-07-20 09:41:23.000000 geomancy-0.1.0a0/geomancy.egg-info/top_level.txt
--rw-r--r--   0 jlorieau   (501) staff       (20)      563 2023-07-20 09:40:28.000000 geomancy-0.1.0a0/pyproject.toml
--rw-r--r--   0 jlorieau   (501) staff       (20)       38 2023-07-20 09:41:23.843590 geomancy-0.1.0a0/setup.cfg
-drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-20 09:41:23.835963 geomancy-0.1.0a0/tests/
-drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-20 09:41:23.842218 geomancy-0.1.0a0/tests/checks/
--rw-r--r--   0 jlorieau   (501) staff       (20)     2543 2023-07-19 21:28:18.000000 geomancy-0.1.0a0/tests/checks/test_env.py
+drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-23 20:55:18.542896 geomancy-0.6.0b0/
+-rw-r--r--   0 jlorieau   (501) staff       (20)      256 2023-07-20 19:04:04.000000 geomancy-0.6.0b0/.editorconfig
+-rw-r--r--   0 jlorieau   (501) staff       (20)     1780 2023-07-20 09:53:51.000000 geomancy-0.6.0b0/.gitignore
+-rw-r--r--   0 jlorieau   (501) staff       (20)    35142 2023-07-19 19:00:29.000000 geomancy-0.6.0b0/LICENSE.md
+-rw-r--r--   0 jlorieau   (501) staff       (20)     6230 2023-07-23 20:55:18.541211 geomancy-0.6.0b0/PKG-INFO
+-rw-r--r--   0 jlorieau   (501) staff       (20)     5883 2023-07-23 20:38:21.000000 geomancy-0.6.0b0/README.md
+-rw-r--r--   0 jlorieau   (501) staff       (20)      587 2023-07-20 19:50:56.000000 geomancy-0.6.0b0/Taskfile.yml
+drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-23 20:55:18.523467 geomancy-0.6.0b0/examples/
+-rw-r--r--   0 jlorieau   (501) staff       (20)     1273 2023-07-23 19:48:55.000000 geomancy-0.6.0b0/examples/geomancy.toml
+-rw-r--r--   0 jlorieau   (501) staff       (20)      512 2023-07-22 13:17:41.000000 geomancy-0.6.0b0/examples/pyproject.toml
+drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-23 20:55:18.525239 geomancy-0.6.0b0/geomancy/
+-rw-r--r--   0 jlorieau   (501) staff       (20)       59 2023-07-23 20:49:04.000000 geomancy-0.6.0b0/geomancy/__description__.txt
+-rw-r--r--   0 jlorieau   (501) staff       (20)      477 2023-07-23 20:49:08.000000 geomancy-0.6.0b0/geomancy/__init__.py
+drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-23 20:55:18.531233 geomancy-0.6.0b0/geomancy/checks/
+-rw-r--r--   0 jlorieau   (501) staff       (20)      257 2023-07-23 18:46:46.000000 geomancy-0.6.0b0/geomancy/checks/__init__.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)    11237 2023-07-23 18:44:11.000000 geomancy-0.6.0b0/geomancy/checks/base.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)     1717 2023-07-23 16:57:03.000000 geomancy-0.6.0b0/geomancy/checks/env.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)     2812 2023-07-23 19:41:18.000000 geomancy-0.6.0b0/geomancy/checks/exec.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)     1549 2023-07-23 16:57:23.000000 geomancy-0.6.0b0/geomancy/checks/path.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)      184 2023-07-23 20:24:18.000000 geomancy-0.6.0b0/geomancy/checks/python.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)     3542 2023-07-23 19:33:47.000000 geomancy-0.6.0b0/geomancy/checks/utils.py
+drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-23 20:55:18.532643 geomancy-0.6.0b0/geomancy/cli/
+-rw-r--r--   0 jlorieau   (501) staff       (20)       42 2023-07-23 11:20:13.000000 geomancy-0.6.0b0/geomancy/cli/__init__.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)     9027 2023-07-23 16:16:44.000000 geomancy-0.6.0b0/geomancy/cli/term.py
+drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-23 20:55:18.534055 geomancy-0.6.0b0/geomancy/config/
+-rw-r--r--   0 jlorieau   (501) staff       (20)      137 2023-07-22 15:14:01.000000 geomancy-0.6.0b0/geomancy/config/__init__.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)     9726 2023-07-22 15:36:57.000000 geomancy-0.6.0b0/geomancy/config/config.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)     5046 2023-07-23 20:54:10.000000 geomancy-0.6.0b0/geomancy/main.py
+drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-23 20:55:18.526996 geomancy-0.6.0b0/geomancy.egg-info/
+-rw-r--r--   0 jlorieau   (501) staff       (20)     6230 2023-07-23 20:55:18.000000 geomancy-0.6.0b0/geomancy.egg-info/PKG-INFO
+-rw-r--r--   0 jlorieau   (501) staff       (20)      858 2023-07-23 20:55:18.000000 geomancy-0.6.0b0/geomancy.egg-info/SOURCES.txt
+-rw-r--r--   0 jlorieau   (501) staff       (20)        1 2023-07-23 20:55:18.000000 geomancy-0.6.0b0/geomancy.egg-info/dependency_links.txt
+-rw-r--r--   0 jlorieau   (501) staff       (20)       47 2023-07-23 20:55:18.000000 geomancy-0.6.0b0/geomancy.egg-info/entry_points.txt
+-rw-r--r--   0 jlorieau   (501) staff       (20)       45 2023-07-23 20:55:18.000000 geomancy-0.6.0b0/geomancy.egg-info/requires.txt
+-rw-r--r--   0 jlorieau   (501) staff       (20)        9 2023-07-23 20:55:18.000000 geomancy-0.6.0b0/geomancy.egg-info/top_level.txt
+-rw-r--r--   0 jlorieau   (501) staff       (20)      703 2023-07-23 20:55:11.000000 geomancy-0.6.0b0/pyproject.toml
+-rw-r--r--   0 jlorieau   (501) staff       (20)       38 2023-07-23 20:55:18.543001 geomancy-0.6.0b0/setup.cfg
+drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-23 20:55:18.534709 geomancy-0.6.0b0/tests/
+drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-23 20:55:18.538630 geomancy-0.6.0b0/tests/checks/
+-rw-r--r--   0 jlorieau   (501) staff       (20)     2968 2023-07-22 17:33:51.000000 geomancy-0.6.0b0/tests/checks/test_base.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)     2665 2023-07-23 16:39:02.000000 geomancy-0.6.0b0/tests/checks/test_env.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)     1171 2023-07-23 19:38:14.000000 geomancy-0.6.0b0/tests/checks/test_exec.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)     2347 2023-07-23 10:43:50.000000 geomancy-0.6.0b0/tests/checks/test_path.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)      828 2023-07-22 11:59:17.000000 geomancy-0.6.0b0/tests/checks/test_utils.py
+drwxr-xr-x   0 jlorieau   (501) staff       (20)        0 2023-07-23 20:55:18.540215 geomancy-0.6.0b0/tests/config/
+-rw-r--r--   0 jlorieau   (501) staff       (20)       73 2023-07-20 16:27:03.000000 geomancy-0.6.0b0/tests/config/config1.toml
+-rw-r--r--   0 jlorieau   (501) staff       (20)     6468 2023-07-22 15:36:00.000000 geomancy-0.6.0b0/tests/config/test_config.py
+-rw-r--r--   0 jlorieau   (501) staff       (20)     1647 2023-07-22 16:20:11.000000 geomancy-0.6.0b0/tests/test_main.py
```

### Comparing `geomancy-0.1.0a0/.gitignore` & `geomancy-0.6.0b0/.gitignore`

 * *Files 7% similar despite different names*

```diff
@@ -121,7 +121,10 @@
 # mypy
 .mypy_cache/
 .dmypy.json
 dmypy.json
 
 # Pyre type checker
 .pyre/
+
+# Taskfile (temp hashes)
+.task/
```

### Comparing `geomancy-0.1.0a0/LICENSE.md` & `geomancy-0.6.0b0/LICENSE.md`

 * *Files identical despite different names*

### Comparing `geomancy-0.1.0a0/pyproject.toml` & `geomancy-0.6.0b0/pyproject.toml`

 * *Files 24% similar despite different names*

```diff
@@ -3,26 +3,32 @@
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "geomancy"
 authors = [
     {name = "Justin Lorieau"},
 ]
-description = "A deployment environment validator"
 readme = "README.md"
 requires-python = ">=3.11"
 classifiers = [
     "Programming Language :: Python :: 3",
     "Development Status :: 3 - Alpha"
     ]
-dynamic = ["version"]
+dynamic = ["version", "description"]
 
 [project.optional-dependencies]
 dev = [
     "pytest>=7.4",
     "twine>=4.0",
+    "black[d]",
     "build"
     ]
 
 [tool.setuptools.dynamic]
 version = {attr = "geomancy.__version__"}
+description = {file = "geomancy/__description__.txt"}
 
+[project.scripts]
+geo = "geomancy.main:main_cli"
+
+[tool.pytest.ini_options]
+addopts = "--doctest-modules"
```

