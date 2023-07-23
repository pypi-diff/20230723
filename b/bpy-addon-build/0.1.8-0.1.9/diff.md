# Comparing `tmp/bpy_addon_build-0.1.8.tar.gz` & `tmp/bpy_addon_build-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bpy_addon_build-0.1.8.tar", max compression
+gzip compressed data, was "bpy_addon_build-0.1.9.tar", max compression
```

## Comparing `bpy_addon_build-0.1.8.tar` & `bpy_addon_build-0.1.9.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0     4770 2023-06-26 06:31:43.813373 bpy_addon_build-0.1.8/bpy_addon_build/__init__.py
--rw-r--r--   0        0        0     1642 2023-06-26 06:57:34.395633 bpy_addon_build-0.1.8/bpy_addon_build/actions.py
--rw-r--r--   0        0        0     1021 2023-06-26 06:24:00.511775 bpy_addon_build-0.1.8/bpy_addon_build/yaml_conf.py
--rw-r--r--   0        0        0      548 2023-06-26 06:26:02.362017 bpy_addon_build-0.1.8/pyproject.toml
--rw-r--r--   0        0        0      730 1970-01-01 00:00:00.000000 bpy_addon_build-0.1.8/PKG-INFO
+-rw-r--r--   0        0        0     5458 2023-07-23 18:36:24.734437 bpy_addon_build-0.1.9/bpy_addon_build/__init__.py
+-rw-r--r--   0        0        0     1644 2023-07-23 18:35:35.169888 bpy_addon_build-0.1.9/bpy_addon_build/actions.py
+-rw-r--r--   0        0        0     1021 2023-06-26 06:24:00.000000 bpy_addon_build-0.1.9/bpy_addon_build/yaml_conf.py
+-rw-r--r--   0        0        0      548 2023-07-23 18:42:36.848348 bpy_addon_build-0.1.9/pyproject.toml
+-rw-r--r--   0        0        0      730 1970-01-01 00:00:00.000000 bpy_addon_build-0.1.9/PKG-INFO
```

### Comparing `bpy_addon_build-0.1.8/bpy_addon_build/__init__.py` & `bpy_addon_build-0.1.9/bpy_addon_build/__init__.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,9 @@
 import os
 import shutil
-import time
 from pathlib import Path
 from typing import List, Optional
 from rich.console import Console
 from docopt import docopt
 
 from . import actions
 from . import yaml_conf
@@ -23,48 +22,49 @@
 # Rich console
 console = Console()
 
 
 USAGE = """
 Usage:
     bpy-addon-build (-h | --help)
-    bpy-addon-build (-b | --during-build) <action> [<file>]
+    bpy-addon-build ((-b | --during-build) <action>) [<file>]
+    bpy-addon-build [<file>] [((-b | --during-build) <action>)] ((-v | --versions) <versions>...)
     bpy-addon-build [<file>]
 
 Options:
   -h --help     Show this screen.
   -b --during-build      Execute a set of actions in addition to the default action
+  -v 
 """
 
 
 # Parse a file from a Path
 def parse_file(file: Path) -> yaml_conf.BpyBuildYaml:
     with open(file, "r") as f:
         yaml_config: yaml_conf.BpyBuildYaml = yaml_conf.BpyBuildYaml(f, file)
         return yaml_config
 
-
 # Main function
 def main():
     args = docopt(USAGE)
     bpy_build_yaml: Path = WORKING_DIR / Path("bpy-build.yaml")
 
     if not args["<file>"]:
         if bpy_build_yaml.exists():
             pass
         else:
-            console.print(
-                "Can't find bpy-build.yaml, maybe pass it directly?", style="bold red"
-            )
+            console.print("Can't find bpy-build.yaml, maybe pass it directly?",
+                          style="bold red")
             return
     else:
         bpy_build_yaml = Path(args["<file>"]).resolve()
 
     yaml_conf = parse_file(bpy_build_yaml)
     build_dir = bpy_build_yaml.parents[0] / Path("build")
+    copy_dir = build_dir / Path(yaml_conf.build_name + "subfolder")
     built_zip = build_dir / Path(yaml_conf.build_name + ".zip")
 
     # Check if the addon folder exists
     if not yaml_conf.addon_folder.exists():
         console.print(
             f"Addon folder {str(yaml_conf.addon_folder)} does not exist!",
             style="bold red",
@@ -95,28 +95,38 @@
                 for action in yaml_conf.during_build["default"]:
                     actions.execute_action(action, inter_dir, console)
             # Perform extra action
             if args["--during-build"] and args["<action>"] in yaml_conf.during_build:
                 for action in yaml_conf.during_build[args["<action>"]]:
                     actions.execute_action(action, inter_dir, console)
         # Rebuild
+        if copy_dir.exists():
+            shutil.rmtree(copy_dir)
+        copy_dir.mkdir()
+        shutil.copytree(inter_dir, copy_dir / Path(yaml_conf.build_name))
         with console.status("[bold green]Building...") as _:
             time.sleep(2)
-            shutil.make_archive(str(build_dir / yaml_conf.build_name), "zip", inter_dir)
+            shutil.make_archive(str(build_dir / yaml_conf.build_name), "zip", copy_dir )
     else:
         # Build addon
+        if copy_dir.exists():
+            shutil.rmtree(copy_dir)
+        copy_dir.mkdir()
+        shutil.copytree(yaml_conf.addon_folder, copy_dir / Path(yaml_conf.build_name))
         with console.status("[bold green]Building...") as _:
-            time.sleep(2)
             shutil.make_archive(
-                str(build_dir / yaml_conf.build_name), "zip", yaml_conf.addon_folder
+                str(build_dir / yaml_conf.build_name), "zip", copy_dir
             )
 
     # Install addon
     with console.status("[bold green] Installing...") as _:
-        for path in map(Path, yaml_conf.install_versions):
+        versions_list = yaml_conf.install_versions
+        if len(args["<versions>"]):
+            versions_list = args["<versions>"]
+        for path in map(Path, versions_list):
             # Expand the ~ in the path
             path = path.expanduser()
             if not path.exists():
                 found: Optional[Path] = next(
                     (
                         Path(test_path.format(str(path))).expanduser()
                         for test_path in BLENDER_ADDON_DIR
@@ -129,15 +139,16 @@
                 else:
                     console.print(
                         f"Path {str(path)} doesn't exist, skipping...",
                         style="bold yellow",
                     )
                     continue
             edited_path: Path = path / Path(yaml_conf.build_name)
+            console.print(f"Installing in {str(path)}", style="bold green")
             shutil.rmtree(edited_path, ignore_errors=True)
             edited_path.mkdir(exist_ok=True)
             shutil.unpack_archive(built_zip, edited_path)
-            time.sleep(1)
+            console.print(f"Installed to {edited_path}")
 
 
 if __name__ == "__main__":
     main()
```

### Comparing `bpy_addon_build-0.1.8/bpy_addon_build/actions.py` & `bpy_addon_build-0.1.9/bpy_addon_build/actions.py`

 * *Files 8% similar despite different names*

```diff
@@ -19,28 +19,28 @@
                 cwd=inter_dir,
                 stdout=subprocess.PIPE,
                 stderr=subprocess.STDOUT,
             )
             console.print(output.stdout.decode("UTF-8"))
 
     elif "create_file" in action:
-        extracted_str = re.search("\((.+?)\)", action)
+        extracted_str = re.search(r"\((.+?)\)", action)
         if not extracted_str:
             console.print(
                 f"Invalid action: {action}, perhaps you forgot parenthesis?",
                 style="bold red",
             )
             quit()
 
         file_path = inter_dir / Path(extracted_str.group(1).replace('"', ""))
         with open(file_path, "w") as f:
             f.write("")
 
     elif "copy_file" in action:
-        extracted_str = re.search("\((.+?)\)", action)
+        extracted_str = re.search(r"\((.+?)\)", action)
         if not extracted_str:
             console.print(
                 f"Invalid action: {action}, perhaps you forgot parenthesis?",
                 style="bold red",
             )
 
         files: List[str] = extracted_str.group(1).split("->")
```

### Comparing `bpy_addon_build-0.1.8/bpy_addon_build/yaml_conf.py` & `bpy_addon_build-0.1.9/bpy_addon_build/yaml_conf.py`

 * *Files identical despite different names*

### Comparing `bpy_addon_build-0.1.8/pyproject.toml` & `bpy_addon_build-0.1.9/pyproject.toml`

 * *Files 23% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "bpy-addon-build"
-version = "0.1.8"
+version = "0.1.9"
 description = "A build system to make building and testing Blender addons 10 times easier"
 authors = ["StandingPad"]
 license = "MIT"
 homepage = "https://github.com/StandingPadAnimations/bpy-build"
 
 [tool.poetry.dependencies]
 python = "^3.7"
```

### Comparing `bpy_addon_build-0.1.8/PKG-INFO` & `bpy_addon_build-0.1.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bpy-addon-build
-Version: 0.1.8
+Version: 0.1.9
 Summary: A build system to make building and testing Blender addons 10 times easier
 Home-page: https://github.com/StandingPadAnimations/bpy-build
 License: MIT
 Author: StandingPad
 Requires-Python: >=3.7,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

