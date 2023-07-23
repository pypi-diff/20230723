# Comparing `tmp/gptask_cli-0.1.2.tar.gz` & `tmp/gptask_cli-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gptask_cli-0.1.2.tar", max compression
+gzip compressed data, was "gptask_cli-0.1.5.tar", max compression
```

## Comparing `gptask_cli-0.1.2.tar` & `gptask_cli-0.1.5.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0     1075 2023-07-21 04:59:46.922687 gptask_cli-0.1.2/LICENSE
--rw-r--r--   0        0        0     1062 2023-07-21 05:10:41.249397 gptask_cli-0.1.2/README.md
--rw-r--r--   0        0        0      557 2023-07-21 05:12:36.150206 gptask_cli-0.1.2/gptask_cli/.gptask.example/prompts/code-docs.gptask
--rw-r--r--   0        0        0      200 2023-07-21 05:11:01.916225 gptask_cli-0.1.2/gptask_cli/.gptask.example/prompts/code-helper.gptask
--rw-r--r--   0        0        0      200 2023-07-21 02:46:48.450542 gptask_cli-0.1.2/gptask_cli/.gptask.example/prompts/doc-reviewer.gptask
--rw-r--r--   0        0        0     2362 2023-07-21 19:18:03.945032 gptask_cli-0.1.2/gptask_cli/__init__.py
--rw-r--r--   0        0        0     1652 2023-07-21 03:11:44.343105 gptask_cli-0.1.2/gptask_cli/conf.py
--rw-r--r--   0        0        0      854 2023-07-21 04:02:06.937324 gptask_cli-0.1.2/gptask_cli/git_checker.py
--rw-r--r--   0        0        0     1323 2023-07-21 04:11:38.921828 gptask_cli-0.1.2/gptask_cli/openai_gptask.py
--rw-r--r--   0        0        0      374 2023-07-21 19:18:08.154597 gptask_cli-0.1.2/pyproject.toml
--rw-r--r--   0        0        0     1576 1970-01-01 00:00:00.000000 gptask_cli-0.1.2/PKG-INFO
+-rw-r--r--   0        0        0     1075 2023-07-21 04:59:46.922687 gptask_cli-0.1.5/LICENSE
+-rw-r--r--   0        0        0     1062 2023-07-21 05:10:41.249397 gptask_cli-0.1.5/README.md
+-rw-r--r--   0        0        0      557 2023-07-21 05:12:36.150206 gptask_cli-0.1.5/gptask_cli/.gptask.example/prompts/code-docs.gptask
+-rw-r--r--   0        0        0      200 2023-07-21 05:11:01.916225 gptask_cli-0.1.5/gptask_cli/.gptask.example/prompts/code-helper.gptask
+-rw-r--r--   0        0        0      186 2023-07-23 03:58:13.775700 gptask_cli-0.1.5/gptask_cli/.gptask.example/prompts/doc-reviewer.gptask
+-rw-r--r--   0        0        0     2481 2023-07-23 03:58:58.322966 gptask_cli-0.1.5/gptask_cli/__init__.py
+-rw-r--r--   0        0        0     1652 2023-07-21 19:59:21.127330 gptask_cli-0.1.5/gptask_cli/conf.py
+-rw-r--r--   0        0        0      854 2023-07-21 04:02:06.937324 gptask_cli-0.1.5/gptask_cli/git_checker.py
+-rw-r--r--   0        0        0     1392 2023-07-23 03:58:48.423731 gptask_cli-0.1.5/gptask_cli/openai_gptask.py
+-rw-r--r--   0        0        0      374 2023-07-23 03:58:29.166686 gptask_cli-0.1.5/pyproject.toml
+-rw-r--r--   0        0        0     1576 1970-01-01 00:00:00.000000 gptask_cli-0.1.5/PKG-INFO
```

### Comparing `gptask_cli-0.1.2/LICENSE` & `gptask_cli-0.1.5/LICENSE`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.2/README.md` & `gptask_cli-0.1.5/README.md`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.2/gptask_cli/.gptask.example/prompts/code-docs.gptask` & `gptask_cli-0.1.5/gptask_cli/.gptask.example/prompts/code-docs.gptask`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.2/gptask_cli/__init__.py` & `gptask_cli-0.1.5/gptask_cli/__init__.py`

 * *Files 18% similar despite different names*

```diff
@@ -26,20 +26,24 @@
     if(".gptask" in prompt):
         return all_prompts[prompt[:-7]]
     else:
         return all_prompts[prompt]
 
 
 @click.command()
+@click.option('-v', '--version', is_flag=True, help='Prints the version of gptask')
 @click.option('-p', '--prompt', help='Prompts in ~/.gptask/prompts')
 @click.option('-f', '--force', is_flag=True, help='Force execution even if conditions are not met')
 @click.option('-r', '--recursive', type=click.STRING, help='Directory with files to be processed')
-@click.version_option(version='0.1.2', prog_name='gptask-cli')  # Add this line
 @click.argument('file', type=click.File('r'), required=False)
-def main(prompt, force, recursive, file):
+def main(version, prompt, force, recursive, file):
+    if version:
+        from gptask_cli import __version__
+        click.echo(__version__)
+        return
     setup()
 
     files_to_process = get_files_to_process(recursive, file)
     if not files_to_process:
         return
 
     if not all(check_file_staged_status(f, force) for f in files_to_process):
```

### Comparing `gptask_cli-0.1.2/gptask_cli/conf.py` & `gptask_cli-0.1.5/gptask_cli/conf.py`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.2/gptask_cli/git_checker.py` & `gptask_cli-0.1.5/gptask_cli/git_checker.py`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.2/gptask_cli/openai_gptask.py` & `gptask_cli-0.1.5/gptask_cli/openai_gptask.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 import os
 import openai
-from gptask.conf import load_prompts, load_key
+from gptask_cli.conf import load_key
 
 system_prompt = "You are a helpful coding assistant who helps users with their code. Given an instruction, and an associated code file, return a helpful response. Follow the user's instruction carefully, and let them override this instruction if necessary."
 
 def init():
     openai.api_key = load_key()
 
 def run(prompt: str, file_name: str, file: str, model: str = "gpt-4"):
     if ('OPENAI_API_KEY' not in os.environ):
         init()
-
+    seperator = "<------------------------------------>"
     user_prompt = f"""{file}
-<------------------------------------>
+{seperator}
 Using the contents above for {file_name} please following the following instructions: {prompt}
 Please only show me the output, no explanation.
 """
     assistant_helper_prompt = f"""
 Sure I will just show you the output with my modified changes.
 """
     response = openai.ChatCompletion.create(
@@ -34,8 +34,10 @@
                 'role': 'assistant',
                 'content': assistant_helper_prompt
             }
         ],
         temperature=0.0,
     )
     
-    return response.choices[0].message.content
+    res: str= response.choices[0].message.content
+    res.replace(seperator, '')
+    return res
```

### Comparing `gptask_cli-0.1.2/PKG-INFO` & `gptask_cli-0.1.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gptask-cli
-Version: 0.1.2
+Version: 0.1.5
 Summary: 
 Author: Calum Bird
 Author-email: calum@trelent.net
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
```

