# Comparing `tmp/hyprshade-0.6.3.tar.gz` & `tmp/hyprshade-0.7.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hyprshade-0.6.3.tar", max compression
+gzip compressed data, was "hyprshade-0.7.0.tar", max compression
```

## Comparing `hyprshade-0.6.3.tar` & `hyprshade-0.7.0.tar`

### file list

```diff
@@ -1,15 +1,15 @@
--rw-r--r--   0        0        0     1065 2023-07-17 17:02:30.069743 hyprshade-0.6.3/LICENSE
--rw-r--r--   0        0        0     2761 2023-07-17 17:02:30.069743 hyprshade-0.6.3/README.md
--rw-r--r--   0        0        0      125 2023-07-17 17:02:30.069743 hyprshade-0.6.3/examples/config.toml
--rw-r--r--   0        0        0        0 2023-07-17 17:02:30.069743 hyprshade-0.6.3/hyprshade/__init__.py
--rw-r--r--   0        0        0       92 2023-07-17 17:02:30.069743 hyprshade-0.6.3/hyprshade/__main__.py
--rw-r--r--   0        0        0     2467 2023-07-17 17:02:30.069743 hyprshade-0.6.3/hyprshade/cli.py
--rw-r--r--   0        0        0     3709 2023-07-17 17:02:30.069743 hyprshade-0.6.3/hyprshade/config.py
--rw-r--r--   0        0        0      483 2023-07-17 17:02:30.069743 hyprshade-0.6.3/hyprshade/constants.py
--rw-r--r--   0        0        0      566 2023-07-17 17:02:30.069743 hyprshade-0.6.3/hyprshade/helpers.py
--rw-r--r--   0        0        0      803 2023-07-17 17:02:30.069743 hyprshade-0.6.3/hyprshade/hyprctl.py
--rw-r--r--   0        0        0      812 2023-07-17 17:02:30.069743 hyprshade-0.6.3/hyprshade/utils.py
--rw-r--r--   0        0        0     1036 2023-07-17 17:02:30.073743 hyprshade-0.6.3/pyproject.toml
--rw-r--r--   0        0        0     1986 2023-07-17 17:02:30.073743 hyprshade-0.6.3/shaders/blue-light-filter.glsl
--rw-r--r--   0        0        0     1276 2023-07-17 17:02:30.073743 hyprshade-0.6.3/shaders/vibrance.glsl
--rw-r--r--   0        0        0     3204 1970-01-01 00:00:00.000000 hyprshade-0.6.3/PKG-INFO
+-rw-r--r--   0        0        0     1065 2023-07-23 17:08:29.643178 hyprshade-0.7.0/LICENSE
+-rw-r--r--   0        0        0     2880 2023-07-23 17:08:29.643178 hyprshade-0.7.0/README.md
+-rw-r--r--   0        0        0      125 2023-07-23 17:08:29.643178 hyprshade-0.7.0/examples/config.toml
+-rw-r--r--   0        0        0        0 2023-07-23 17:08:29.643178 hyprshade-0.7.0/hyprshade/__init__.py
+-rw-r--r--   0        0        0       92 2023-07-23 17:08:29.643178 hyprshade-0.7.0/hyprshade/__main__.py
+-rw-r--r--   0        0        0     2891 2023-07-23 17:08:29.643178 hyprshade-0.7.0/hyprshade/cli.py
+-rw-r--r--   0        0        0     3709 2023-07-23 17:08:29.643178 hyprshade-0.7.0/hyprshade/config.py
+-rw-r--r--   0        0        0      483 2023-07-23 17:08:29.643178 hyprshade-0.7.0/hyprshade/constants.py
+-rw-r--r--   0        0        0      566 2023-07-23 17:08:29.643178 hyprshade-0.7.0/hyprshade/helpers.py
+-rw-r--r--   0        0        0      803 2023-07-23 17:08:29.643178 hyprshade-0.7.0/hyprshade/hyprctl.py
+-rw-r--r--   0        0        0      812 2023-07-23 17:08:29.643178 hyprshade-0.7.0/hyprshade/utils.py
+-rw-r--r--   0        0        0     1036 2023-07-23 17:08:29.643178 hyprshade-0.7.0/pyproject.toml
+-rw-r--r--   0        0        0     1986 2023-07-23 17:08:29.643178 hyprshade-0.7.0/shaders/blue-light-filter.glsl
+-rw-r--r--   0        0        0     1276 2023-07-23 17:08:29.643178 hyprshade-0.7.0/shaders/vibrance.glsl
+-rw-r--r--   0        0        0     3323 1970-01-01 00:00:00.000000 hyprshade-0.7.0/PKG-INFO
```

### Comparing `hyprshade-0.6.3/LICENSE` & `hyprshade-0.7.0/LICENSE`

 * *Files identical despite different names*

### Comparing `hyprshade-0.6.3/README.md` & `hyprshade-0.7.0/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -57,18 +57,27 @@
   install  Install systemd user units
   ls       List available screen shaders
   off      Turn off screen shader
   on       Turn on screen shader
   toggle   Toggle screen shader
 ```
 
-### Adding Shaders
+Commands which take a shader name accept either the basename:
 
-Hyprshade uses the shader files in your `~/.config/hypr/shaders` directory
-(in addition to the ones installed to `/usr/share/hyprshade`) for all of its commands.
+```sh
+hyprshade on blue-light-filter
+```
+
+or a full path name:
+
+```sh
+hyprshade on ~/.config/hypr/shaders/blue-light-filter.glsl
+```
+
+If you provide the basename, Hyprshade searches in `~/.config/hypr/shaders` and `/usr/share/hyprshade`.
 
 ### Scheduling
 
 To have specific shaders enabled during certain periods of the day, you can
 create a config file in either `~/.config/hypr/hyprshade.toml` or `~/.config/hyprshade/config.toml`.
 
 ```toml
```

### Comparing `hyprshade-0.6.3/hyprshade/cli.py` & `hyprshade-0.7.0/hyprshade/cli.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import os
 from datetime import datetime
 from itertools import chain
 from os import path
+from typing import Annotated, Optional
 
 import typer
 
 from .constants import SHADER_DIRS
 from .helpers import resolve_shader_path
 from .hyprctl import clear_screen_shader, get_screen_shader, set_screen_shader
 from .utils import systemd_user_config_home
@@ -25,35 +26,51 @@
 def off() -> int:
     """Turn off screen shader"""
 
     return clear_screen_shader()
 
 
 @app.command()
-def toggle(shader_name_or_path: str) -> int:
-    """Toggle screen shader"""
+def toggle(
+    shader_name_or_path: Annotated[
+        Optional[str], typer.Argument()  # noqa: UP007
+    ] = None
+) -> int:
+    """Toggle screen shader
+
+    If run with no arguments, will infer shader based on schedule.
+    """
+
+    from .config import Config
+
+    shade: str | None
+    if shader_name_or_path is not None:
+        shade = shader_name_or_path
+    else:
+        t = datetime.now().time()
+        shade = Config().to_schedule().find_shade(t)
+        if shade is None:
+            return off()
+    shade = resolve_shader_path(shade)
 
     current_shader = get_screen_shader()
-    if current_shader is not None and path.samefile(
-        resolve_shader_path(shader_name_or_path), current_shader
-    ):
+    if current_shader is not None and path.samefile(shade, current_shader):
         return off()
 
-    return on(shader_name_or_path)
+    return on(shade)
 
 
 @app.command()
 def auto() -> int:
     """Turn on/off screen shader based on schedule"""
 
     from .config import Config
 
     t = datetime.now().time()
-    schedule = Config().to_schedule()
-    shade = schedule.find_shade(t)
+    shade = Config().to_schedule().find_shade(t)
 
     if shade is not None:
         return on(shade)
     return off()
 
 
 @app.command()
```

### Comparing `hyprshade-0.6.3/hyprshade/config.py` & `hyprshade-0.7.0/hyprshade/config.py`

 * *Files identical despite different names*

### Comparing `hyprshade-0.6.3/hyprshade/helpers.py` & `hyprshade-0.7.0/hyprshade/helpers.py`

 * *Files identical despite different names*

### Comparing `hyprshade-0.6.3/hyprshade/hyprctl.py` & `hyprshade-0.7.0/hyprshade/hyprctl.py`

 * *Files identical despite different names*

### Comparing `hyprshade-0.6.3/hyprshade/utils.py` & `hyprshade-0.7.0/hyprshade/utils.py`

 * *Files identical despite different names*

### Comparing `hyprshade-0.6.3/pyproject.toml` & `hyprshade-0.7.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "hyprshade"
-version = "0.6.3"
+version = "0.7.0"
 description = ""
 authors = ["John Bernard <loqusion@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{ include = "hyprshade" }]
 include = ["examples", "shaders"]
```

### Comparing `hyprshade-0.6.3/shaders/blue-light-filter.glsl` & `hyprshade-0.7.0/shaders/blue-light-filter.glsl`

 * *Files identical despite different names*

### Comparing `hyprshade-0.6.3/shaders/vibrance.glsl` & `hyprshade-0.7.0/shaders/vibrance.glsl`

 * *Files identical despite different names*

### Comparing `hyprshade-0.6.3/PKG-INFO` & `hyprshade-0.7.0/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hyprshade
-Version: 0.6.3
+Version: 0.7.0
 Summary: 
 License: MIT
 Author: John Bernard
 Author-email: loqusion@gmail.com
 Requires-Python: >=3.11,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -72,18 +72,27 @@
   install  Install systemd user units
   ls       List available screen shaders
   off      Turn off screen shader
   on       Turn on screen shader
   toggle   Toggle screen shader
 ```
 
-### Adding Shaders
+Commands which take a shader name accept either the basename:
 
-Hyprshade uses the shader files in your `~/.config/hypr/shaders` directory
-(in addition to the ones installed to `/usr/share/hyprshade`) for all of its commands.
+```sh
+hyprshade on blue-light-filter
+```
+
+or a full path name:
+
+```sh
+hyprshade on ~/.config/hypr/shaders/blue-light-filter.glsl
+```
+
+If you provide the basename, Hyprshade searches in `~/.config/hypr/shaders` and `/usr/share/hyprshade`.
 
 ### Scheduling
 
 To have specific shaders enabled during certain periods of the day, you can
 create a config file in either `~/.config/hypr/hyprshade.toml` or `~/.config/hyprshade/config.toml`.
 
 ```toml
```

