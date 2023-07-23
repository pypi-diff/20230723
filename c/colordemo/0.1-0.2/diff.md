# Comparing `tmp/colordemo-0.1.tar.gz` & `tmp/colordemo-0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "colordemo-0.1.tar", last modified: Sun Jul 23 04:37:06 2023, max compression
+gzip compressed data, was "colordemo-0.2.tar", last modified: Sun Jul 23 05:18:30 2023, max compression
```

## Comparing `colordemo-0.1.tar` & `colordemo-0.2.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0    35147 2023-07-06 06:17:57.182174 colordemo-0.1/COPYING
--rw-r--r--   0        0        0     5154 2023-07-23 04:23:47.388518 colordemo-0.1/README.md
--rw-r--r--   0        0        0     1014 2023-07-23 04:19:34.075191 colordemo-0.1/colordemo/__init__.py
--rwxr-xr-x   0        0        0     5344 2023-07-23 04:19:34.075191 colordemo-0.1/colordemo/__main__.py
--rw-r--r--   0        0        0    13792 2023-07-23 04:24:27.225184 colordemo-0.1/colordemo/color_display.py
--rw-r--r--   0        0        0      820 2023-07-23 04:19:34.075191 colordemo-0.1/colordemo/colors.py
--rw-r--r--   0        0        0    14331 2023-07-23 04:19:34.075191 colordemo-0.1/colordemo/terminal_query.py
--rw-r--r--   0        0        0      837 2023-07-23 04:37:06.465165 colordemo-0.1/pyproject.toml
--rw-r--r--   0        0        0    46337 1970-01-01 00:00:00.000000 colordemo-0.1/PKG-INFO
+-rw-r--r--   0        0        0    35147 2023-07-06 06:17:57.182174 colordemo-0.2/COPYING
+-rw-r--r--   0        0        0     6317 2023-07-23 05:13:53.588444 colordemo-0.2/README.md
+-rw-r--r--   0        0        0     1014 2023-07-23 04:19:34.075191 colordemo-0.2/colordemo/__init__.py
+-rwxr-xr-x   0        0        0     5344 2023-07-23 04:19:34.075191 colordemo-0.2/colordemo/__main__.py
+-rw-r--r--   0        0        0    13792 2023-07-23 04:24:27.225184 colordemo-0.2/colordemo/color_display.py
+-rw-r--r--   0        0        0      820 2023-07-23 04:19:34.075191 colordemo-0.2/colordemo/colors.py
+-rw-r--r--   0        0        0    14331 2023-07-23 04:19:34.075191 colordemo-0.2/colordemo/terminal_query.py
+-rw-r--r--   0        0        0      837 2023-07-23 05:18:30.228437 colordemo-0.2/pyproject.toml
+-rw-r--r--   0        0        0    47500 1970-01-01 00:00:00.000000 colordemo-0.2/PKG-INFO
```

### Comparing `colordemo-0.1/COPYING` & `colordemo-0.2/COPYING`

 * *Files identical despite different names*

### Comparing `colordemo-0.1/README.md` & `colordemo-0.2/README.md`

 * *Files 19% similar despite different names*

```diff
@@ -1,19 +1,58 @@
 # `colordemo`
 
 `colordemo` is a Python package implementing RGB queries on xterm-like
 terminals.  It includes a demo script for presenting terminal color
 schemes, complete with RGB hex codes.
 
-## Usage
+<div align="center">
+    <img src="https://raw.githubusercontent.com/dranjan/python-colordemo/master/examples/colordemo-example.png">
+</div>
 
+## Quick start
+
+There are many ways to run the demo script, and we will briefly describe
+them here. Note that with any of the methods below, the `colordemo`
+tool can accept command-line options. To see which options are available,
+use `--help` with any of the methods, e.g.,
+
+    pipx run colordemo --help
+
+### Using `pipx`
+
+With only an active internet connection and the `pipx` Python utility,
+the script can be run directly without installation:
+
+    pipx run colordemo
+
+Alternatively, it can also be installed explicitly and run that way:
+
+    pipx install colordemo
+    colordemo
+
+### Using `pip`
+
+The package can also be installed and run as a normal Python package
+using `pip` (preferably in a `virtualenv` environment):
+
+    pip install colordemo
+    colordemo
+
+    # Equivalent
     python -m colordemo
 
-    # To see all available options
-    python -m colordemo --help
+### From the source tree
+
+Finally, the script can be run easily from the source tree directly.
+This package has no dependencies besides Python, so no actions are
+needed besides cloning the repository.
+
+    git clone 'git@github.com:dranjan/python-colordemo.git'
+    cd python-colordemo
+    python -m colordemo
 
 ## Overview of functionality
 
 `colordemo` allows you to programmatically determine the RGB values of
 some terminals' ANSI colors (or more colors, if the terminal has them).
 The functions must be run from the terminal whose colors you want to
 determine, and with caveats if within a screen or tmux session (see
```

### Comparing `colordemo-0.1/colordemo/__init__.py` & `colordemo-0.2/colordemo/__init__.py`

 * *Files identical despite different names*

### Comparing `colordemo-0.1/colordemo/__main__.py` & `colordemo-0.2/colordemo/__main__.py`

 * *Files identical despite different names*

### Comparing `colordemo-0.1/colordemo/color_display.py` & `colordemo-0.2/colordemo/color_display.py`

 * *Files identical despite different names*

### Comparing `colordemo-0.1/colordemo/colors.py` & `colordemo-0.2/colordemo/colors.py`

 * *Files identical despite different names*

### Comparing `colordemo-0.1/colordemo/terminal_query.py` & `colordemo-0.2/colordemo/terminal_query.py`

 * *Files identical despite different names*

### Comparing `colordemo-0.1/pyproject.toml` & `colordemo-0.2/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "colordemo"
-version = "0.1"
+version = "0.2"
 description = "RGB queries on xterm-like terminals"
 authors = [
     { name = "Darsh Ranjan", email = "dranjan@berkeley.edu" },
 ]
 readme = "README.md"
 requires-python = ">=3.0"
 dependencies = []
```

### Comparing `colordemo-0.1/PKG-INFO` & `colordemo-0.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: colordemo
-Version: 0.1
+Version: 0.2
 Summary: RGB queries on xterm-like terminals
 Author-Email: Darsh Ranjan <dranjan@berkeley.edu>
 License:                     GNU GENERAL PUBLIC LICENSE
                                Version 3, 29 June 2007
         
          Copyright (C) 2007 Free Software Foundation, Inc. <http://fsf.org/>
          Everyone is permitted to copy and distribute verbatim copies
@@ -689,20 +689,59 @@
 
 # `colordemo`
 
 `colordemo` is a Python package implementing RGB queries on xterm-like
 terminals.  It includes a demo script for presenting terminal color
 schemes, complete with RGB hex codes.
 
-## Usage
+<div align="center">
+    <img src="https://raw.githubusercontent.com/dranjan/python-colordemo/master/examples/colordemo-example.png">
+</div>
 
+## Quick start
+
+There are many ways to run the demo script, and we will briefly describe
+them here. Note that with any of the methods below, the `colordemo`
+tool can accept command-line options. To see which options are available,
+use `--help` with any of the methods, e.g.,
+
+    pipx run colordemo --help
+
+### Using `pipx`
+
+With only an active internet connection and the `pipx` Python utility,
+the script can be run directly without installation:
+
+    pipx run colordemo
+
+Alternatively, it can also be installed explicitly and run that way:
+
+    pipx install colordemo
+    colordemo
+
+### Using `pip`
+
+The package can also be installed and run as a normal Python package
+using `pip` (preferably in a `virtualenv` environment):
+
+    pip install colordemo
+    colordemo
+
+    # Equivalent
     python -m colordemo
 
-    # To see all available options
-    python -m colordemo --help
+### From the source tree
+
+Finally, the script can be run easily from the source tree directly.
+This package has no dependencies besides Python, so no actions are
+needed besides cloning the repository.
+
+    git clone 'git@github.com:dranjan/python-colordemo.git'
+    cd python-colordemo
+    python -m colordemo
 
 ## Overview of functionality
 
 `colordemo` allows you to programmatically determine the RGB values of
 some terminals' ANSI colors (or more colors, if the terminal has them).
 The functions must be run from the terminal whose colors you want to
 determine, and with caveats if within a screen or tmux session (see
```

