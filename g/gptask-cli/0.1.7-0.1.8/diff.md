# Comparing `tmp/gptask_cli-0.1.7.tar.gz` & `tmp/gptask_cli-0.1.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gptask_cli-0.1.7.tar", max compression
+gzip compressed data, was "gptask_cli-0.1.8.tar", max compression
```

## Comparing `gptask_cli-0.1.7.tar` & `gptask_cli-0.1.8.tar`

### file list

```diff
@@ -1,16 +1,16 @@
--rw-r--r--   0        0        0     1075 2023-07-21 04:59:46.922687 gptask_cli-0.1.7/LICENSE
--rw-r--r--   0        0        0     1062 2023-07-21 05:10:41.249397 gptask_cli-0.1.7/README.md
--rw-r--r--   0        0        0      118 2023-07-23 17:54:09.950005 gptask_cli-0.1.7/gptask_cli/.gptask.example/prompts/bug-fixer.gptask
--rw-r--r--   0        0        0      557 2023-07-21 05:12:36.150206 gptask_cli-0.1.7/gptask_cli/.gptask.example/prompts/code-docs.gptask
--rw-r--r--   0        0        0      200 2023-07-21 05:11:01.916225 gptask_cli-0.1.7/gptask_cli/.gptask.example/prompts/code-helper.gptask
--rw-r--r--   0        0        0      189 2023-07-23 17:53:29.637217 gptask_cli-0.1.7/gptask_cli/.gptask.example/prompts/code-refactor.gptask
--rw-r--r--   0        0        0      107 2023-07-23 17:53:41.796618 gptask_cli-0.1.7/gptask_cli/.gptask.example/prompts/code-tester.gptask
--rw-r--r--   0        0        0      185 2023-07-23 04:17:03.127227 gptask_cli-0.1.7/gptask_cli/.gptask.example/prompts/doc-reviewer.gptask
--rw-r--r--   0        0        0       58 2023-07-23 17:55:24.137634 gptask_cli-0.1.7/gptask_cli/.gptask.example/prompts/general.gptask
--rw-r--r--   0        0        0      118 2023-07-23 17:54:36.876406 gptask_cli-0.1.7/gptask_cli/.gptask.example/prompts/security-auditor.gptask
--rw-r--r--   0        0        0     3314 2023-07-23 18:05:08.063493 gptask_cli-0.1.7/gptask_cli/__init__.py
--rw-r--r--   0        0        0     1980 2023-07-23 18:04:00.236248 gptask_cli-0.1.7/gptask_cli/conf.py
--rw-r--r--   0        0        0      854 2023-07-21 04:02:06.937324 gptask_cli-0.1.7/gptask_cli/git_checker.py
--rw-r--r--   0        0        0     1392 2023-07-23 03:58:48.423731 gptask_cli-0.1.7/gptask_cli/openai_gptask.py
--rw-r--r--   0        0        0      430 2023-07-23 18:01:36.283029 gptask_cli-0.1.7/pyproject.toml
--rw-r--r--   0        0        0     1576 1970-01-01 00:00:00.000000 gptask_cli-0.1.7/PKG-INFO
+-rw-r--r--   0        0        0     1075 2023-07-21 04:59:46.922687 gptask_cli-0.1.8/LICENSE
+-rw-r--r--   0        0        0     1062 2023-07-21 05:10:41.249397 gptask_cli-0.1.8/README.md
+-rw-r--r--   0        0        0      118 2023-07-23 17:54:09.950005 gptask_cli-0.1.8/gptask_cli/.gptask.example/prompts/bug-fixer.gptask
+-rw-r--r--   0        0        0      557 2023-07-21 05:12:36.150206 gptask_cli-0.1.8/gptask_cli/.gptask.example/prompts/code-docs.gptask
+-rw-r--r--   0        0        0      200 2023-07-21 05:11:01.916225 gptask_cli-0.1.8/gptask_cli/.gptask.example/prompts/code-helper.gptask
+-rw-r--r--   0        0        0      189 2023-07-23 17:53:29.637217 gptask_cli-0.1.8/gptask_cli/.gptask.example/prompts/code-refactor.gptask
+-rw-r--r--   0        0        0      107 2023-07-23 17:53:41.796618 gptask_cli-0.1.8/gptask_cli/.gptask.example/prompts/code-tester.gptask
+-rw-r--r--   0        0        0      185 2023-07-23 04:17:03.127227 gptask_cli-0.1.8/gptask_cli/.gptask.example/prompts/doc-reviewer.gptask
+-rw-r--r--   0        0        0       58 2023-07-23 17:55:24.137634 gptask_cli-0.1.8/gptask_cli/.gptask.example/prompts/general.gptask
+-rw-r--r--   0        0        0      118 2023-07-23 17:54:36.876406 gptask_cli-0.1.8/gptask_cli/.gptask.example/prompts/security-auditor.gptask
+-rw-r--r--   0        0        0     3314 2023-07-23 18:05:52.971724 gptask_cli-0.1.8/gptask_cli/__init__.py
+-rw-r--r--   0        0        0     1984 2023-07-23 18:05:57.368240 gptask_cli-0.1.8/gptask_cli/conf.py
+-rw-r--r--   0        0        0      854 2023-07-21 04:02:06.937324 gptask_cli-0.1.8/gptask_cli/git_checker.py
+-rw-r--r--   0        0        0     1392 2023-07-23 03:58:48.423731 gptask_cli-0.1.8/gptask_cli/openai_gptask.py
+-rw-r--r--   0        0        0      430 2023-07-23 18:06:11.877720 gptask_cli-0.1.8/pyproject.toml
+-rw-r--r--   0        0        0     1576 1970-01-01 00:00:00.000000 gptask_cli-0.1.8/PKG-INFO
```

### Comparing `gptask_cli-0.1.7/LICENSE` & `gptask_cli-0.1.8/LICENSE`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.7/README.md` & `gptask_cli-0.1.8/README.md`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.7/gptask_cli/.gptask.example/prompts/code-docs.gptask` & `gptask_cli-0.1.8/gptask_cli/.gptask.example/prompts/code-docs.gptask`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.7/gptask_cli/__init__.py` & `gptask_cli-0.1.8/gptask_cli/__init__.py`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.7/gptask_cli/conf.py` & `gptask_cli-0.1.8/gptask_cli/conf.py`

 * *Files 0% similar despite different names*

```diff
@@ -31,15 +31,15 @@
     prompts = {}
     for filename in os.listdir(os.path.expanduser('~/.gptask/prompts')):
         with open(os.path.expanduser('~/.gptask/prompts/' + filename)) as f:
             prompts[filename[:-7]] = f.read()
 
     return prompts
 
-def reload_example_prompts():
+def run_reload_example_prompts():
     examples_dir = os.path.dirname(os.path.realpath(__file__)) + '/.gptask.example/prompts'
     prompts_dir = os.path.expanduser('~/.gptask/prompts')
     import shutil
     for filename in os.listdir(examples_dir):
         shutil.copy(os.path.join(examples_dir, filename), os.path.join(prompts_dir, filename))
 
 def load_key():
```

### Comparing `gptask_cli-0.1.7/gptask_cli/git_checker.py` & `gptask_cli-0.1.8/gptask_cli/git_checker.py`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.7/gptask_cli/openai_gptask.py` & `gptask_cli-0.1.8/gptask_cli/openai_gptask.py`

 * *Files identical despite different names*

### Comparing `gptask_cli-0.1.7/PKG-INFO` & `gptask_cli-0.1.8/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gptask-cli
-Version: 0.1.7
+Version: 0.1.8
 Summary: 
 Author: Calum Bird
 Author-email: calum@trelent.net
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
```

