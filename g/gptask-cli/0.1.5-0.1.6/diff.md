# Comparing `tmp/gptask_cli-0.1.5.tar.gz` & `tmp/gptask_cli-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gptask_cli-0.1.5.tar", max compression
+gzip compressed data, was "gptask_cli-0.1.6.tar", max compression
```

## Comparing `gptask_cli-0.1.5.tar` & `gptask_cli-0.1.6.tar`

### file list

```diff
@@ -1,11 +1,16 @@
--rw-r--r--   0        0        0     1075 2023-07-21 04:59:46.922687 gptask_cli-0.1.5/LICENSE
--rw-r--r--   0        0        0     1062 2023-07-21 05:10:41.249397 gptask_cli-0.1.5/README.md
--rw-r--r--   0        0        0      557 2023-07-21 05:12:36.150206 gptask_cli-0.1.5/gptask_cli/.gptask.example/prompts/code-docs.gptask
--rw-r--r--   0        0        0      200 2023-07-21 05:11:01.916225 gptask_cli-0.1.5/gptask_cli/.gptask.example/prompts/code-helper.gptask
--rw-r--r--   0        0        0      186 2023-07-23 03:58:13.775700 gptask_cli-0.1.5/gptask_cli/.gptask.example/prompts/doc-reviewer.gptask
--rw-r--r--   0        0        0     2481 2023-07-23 03:58:58.322966 gptask_cli-0.1.5/gptask_cli/__init__.py
--rw-r--r--   0        0        0     1652 2023-07-21 19:59:21.127330 gptask_cli-0.1.5/gptask_cli/conf.py
--rw-r--r--   0        0        0      854 2023-07-21 04:02:06.937324 gptask_cli-0.1.5/gptask_cli/git_checker.py
--rw-r--r--   0        0        0     1392 2023-07-23 03:58:48.423731 gptask_cli-0.1.5/gptask_cli/openai_gptask.py
--rw-r--r--   0        0        0      374 2023-07-23 03:58:29.166686 gptask_cli-0.1.5/pyproject.toml
--rw-r--r--   0        0        0     1576 1970-01-01 00:00:00.000000 gptask_cli-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0     1075 2023-07-21 04:59:46.922687 gptask_cli-0.1.6/LICENSE
+-rw-r--r--   0        0        0     1062 2023-07-21 05:10:41.249397 gptask_cli-0.1.6/README.md
+-rw-r--r--   0        0        0      118 2023-07-23 17:54:09.950005 gptask_cli-0.1.6/gptask_cli/.gptask.example/prompts/bug-fixer.gptask
+-rw-r--r--   0        0        0      557 2023-07-21 05:12:36.150206 gptask_cli-0.1.6/gptask_cli/.gptask.example/prompts/code-docs.gptask
+-rw-r--r--   0        0        0      200 2023-07-21 05:11:01.916225 gptask_cli-0.1.6/gptask_cli/.gptask.example/prompts/code-helper.gptask
+-rw-r--r--   0        0        0      189 2023-07-23 17:53:29.637217 gptask_cli-0.1.6/gptask_cli/.gptask.example/prompts/code-refactor.gptask
+-rw-r--r--   0        0        0      107 2023-07-23 17:53:41.796618 gptask_cli-0.1.6/gptask_cli/.gptask.example/prompts/code-tester.gptask
+-rw-r--r--   0        0        0      185 2023-07-23 04:17:03.127227 gptask_cli-0.1.6/gptask_cli/.gptask.example/prompts/doc-reviewer.gptask
+-rw-r--r--   0        0        0       58 2023-07-23 17:55:24.137634 gptask_cli-0.1.6/gptask_cli/.gptask.example/prompts/general.gptask
+-rw-r--r--   0        0        0      118 2023-07-23 17:54:36.876406 gptask_cli-0.1.6/gptask_cli/.gptask.example/prompts/security-auditor.gptask
+-rw-r--r--   0        0        0     3085 2023-07-23 17:53:10.231166 gptask_cli-0.1.6/gptask_cli/__init__.py
+-rw-r--r--   0        0        0     1652 2023-07-21 19:59:21.127330 gptask_cli-0.1.6/gptask_cli/conf.py
+-rw-r--r--   0        0        0      854 2023-07-21 04:02:06.937324 gptask_cli-0.1.6/gptask_cli/git_checker.py
+-rw-r--r--   0        0        0     1392 2023-07-23 03:58:48.423731 gptask_cli-0.1.6/gptask_cli/openai_gptask.py
+-rw-r--r--   0        0        0      430 2023-07-23 17:33:59.856589 gptask_cli-0.1.6/pyproject.toml
+-rw-r--r--   0        0        0     1576 1970-01-01 00:00:00.000000 gptask_cli-0.1.6/PKG-INFO
```

### Comparing `gptask_cli-0.1.5/LICENSE` & `gptask_cli-0.1.6/LICENSE`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.5/README.md` & `gptask_cli-0.1.6/README.md`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.5/gptask_cli/.gptask.example/prompts/code-docs.gptask` & `gptask_cli-0.1.6/gptask_cli/.gptask.example/prompts/code-docs.gptask`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.5/gptask_cli/__init__.py` & `gptask_cli-0.1.6/gptask_cli/__init__.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,63 +1,76 @@
 import click
 import os
 import glob
 from gptask_cli.conf import setup, load_prompts
 from gptask_cli.git_checker import is_staged
 from gptask_cli.openai_gptask import run
 
-
 def check_file_staged_status(file, force):
     if not force and is_staged(file.name):
         click.echo(f"File {file.name} has staged changes. Please unstage the file before running gptask.")
         return False
     return True
 
-
 def get_files_to_process(recursive, file):
     if file:
         return [file]
     if recursive:
         return [open(f, 'r') for f in glob.glob(recursive, recursive=True)]
     click.echo("Either a file or directory must be provided.")
     return []
 
-
 def get_prompt_contents(prompt, all_prompts):
     if(".gptask" in prompt):
         return all_prompts[prompt[:-7]]
     else:
         return all_prompts[prompt]
 
+def _print_files(start_path):
+    for root, _, files in os.walk(start_path):
+        for file in files:
+            file_path = os.path.join(root, file)
+            print(f"File Name: {file_path}")
+            with open(file_path, 'r') as f:
+                print(f"File Contents:\n{f.read()}\n")
 
 @click.command()
-@click.option('-v', '--version', is_flag=True, help='Prints the version of gptask')
+@click.version_option()
 @click.option('-p', '--prompt', help='Prompts in ~/.gptask/prompts')
 @click.option('-f', '--force', is_flag=True, help='Force execution even if conditions are not met')
 @click.option('-r', '--recursive', type=click.STRING, help='Directory with files to be processed')
+@click.option('-l', '--print-files', is_flag=True, help='Prints the files to be processed')
+@click.option('-a', '--print-prompts', is_flag=True, help='Prints all available prompts')
 @click.argument('file', type=click.File('r'), required=False)
-def main(version, prompt, force, recursive, file):
-    if version:
-        from gptask_cli import __version__
-        click.echo(__version__)
-        return
+def main(prompt, force, print_files, recursive, print_prompts, file):
     setup()
+    
+    if print_files and recursive:
+        _print_files(recursive)
+        return
+
+    all_prompts = load_prompts()
+    if print_prompts:
+        click.echo("Available prompts:")
+        all_prompts = load_prompts()
+        for key in all_prompts.keys():
+            click.echo(f"  {key}")
+        return
 
     files_to_process = get_files_to_process(recursive, file)
     if not files_to_process:
         return
 
     if not all(check_file_staged_status(f, force) for f in files_to_process):
         return
 
     click.echo(f"The following files will be processed: {[f.name for f in files_to_process]}")
     if not click.confirm("Do you want to continue?", default=True):
         return
 
-    all_prompts = load_prompts()
     if prompt not in all_prompts:
         if prompt is not None:
             click.echo(f"Prompt {prompt} not found")
         click.echo("Available prompts:")
         for key in all_prompts.keys():
             click.echo(f"  {key}")
         return
@@ -68,10 +81,9 @@
         click.echo(f"Using GPT-4 to format (This may take a while): {file.name}")
         file_contents = file.read()
         res = run(prompt_contents, file.name, file_contents)
         with open(file.name, 'w') as f:
             f.write(res)
         file.close()
 
-
 if __name__ == '__main__':
     main()
```

### Comparing `gptask_cli-0.1.5/gptask_cli/conf.py` & `gptask_cli-0.1.6/gptask_cli/conf.py`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.5/gptask_cli/git_checker.py` & `gptask_cli-0.1.6/gptask_cli/git_checker.py`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.5/gptask_cli/openai_gptask.py` & `gptask_cli-0.1.6/gptask_cli/openai_gptask.py`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.5/PKG-INFO` & `gptask_cli-0.1.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gptask-cli
-Version: 0.1.5
+Version: 0.1.6
 Summary: 
 Author: Calum Bird
 Author-email: calum@trelent.net
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
```

