# Comparing `tmp/github_actions_cli-1.0.0b1.tar.gz` & `tmp/github_actions_cli-1.0.0b2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "github_actions_cli-1.0.0b1.tar", max compression
+gzip compressed data, was "github_actions_cli-1.0.0b2.tar", max compression
```

## Comparing `github_actions_cli-1.0.0b1.tar` & `github_actions_cli-1.0.0b2.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0     1500 2023-07-22 16:14:30.465697 github_actions_cli-1.0.0b1/LICENSE
--rw-r--r--   0        0        0     1979 2023-07-22 15:58:45.118107 github_actions_cli-1.0.0b1/README.md
--rw-r--r--   0        0        0        0 2023-07-22 16:11:43.145933 github_actions_cli-1.0.0b1/gha-cli/__init__.py
--rw-r--r--   0        0        0     5230 2023-07-22 16:20:18.115830 github_actions_cli-1.0.0b1/gha-cli/ghautils.py
--rw-r--r--   0        0        0     1481 2023-07-22 16:23:56.571392 github_actions_cli-1.0.0b1/pyproject.toml
--rw-r--r--   0        0        0     3366 1970-01-01 00:00:00.000000 github_actions_cli-1.0.0b1/PKG-INFO
+-rw-r--r--   0        0        0     1500 2023-07-22 16:14:30.465697 github_actions_cli-1.0.0b2/LICENSE
+-rw-r--r--   0        0        0     2016 2023-07-22 16:30:30.348267 github_actions_cli-1.0.0b2/README.md
+-rw-r--r--   0        0        0        0 2023-07-22 19:45:14.822523 github_actions_cli-1.0.0b2/gha_cli/__init__.py
+-rwxr-xr-x   0        0        0     5413 2023-07-22 19:40:09.586657 github_actions_cli-1.0.0b2/gha_cli/cli.py
+-rw-r--r--   0        0        0     1513 2023-07-22 19:54:41.913866 github_actions_cli-1.0.0b2/pyproject.toml
+-rw-r--r--   0        0        0     3251 1970-01-01 00:00:00.000000 github_actions_cli-1.0.0b2/PKG-INFO
```

### Comparing `github_actions_cli-1.0.0b1/LICENSE` & `github_actions_cli-1.0.0b2/LICENSE`

 * *Files identical despite different names*

### Comparing `github_actions_cli-1.0.0b1/README.md` & `github_actions_cli-1.0.0b2/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,12 @@
-GitHub Actions Utils
+GitHub Actions CLI
 ====================
 
 The purpose of this tool is to work with your GitHub Actions workflows in your repositories.
+It is complementary to the GitHub CLI.
 
 So far, three main flows are supported:
 
 # List all workflows path and name in a specified repository.
 
 Example:
```

### Comparing `github_actions_cli-1.0.0b1/gha-cli/ghautils.py` & `github_actions_cli-1.0.0b2/gha_cli/cli.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,25 +1,31 @@
+#!/usr/bin/env python3
 import argparse
+import logging
 import os
 from typing import Optional, List, Set, Tuple, Dict
 
 import yaml
 from github import Github, Workflow
 
+logging.basicConfig(level=logging.WARNING)
+logging.getLogger('github.Requester').setLevel(logging.WARNING)
+logger = logging.getLogger()
+
 
 def parse_args() -> argparse.Namespace:
     parser = argparse.ArgumentParser()
     parser.add_argument('repo', help='Repository to analyze')
     parser.add_argument(
         '--github-token', dest='github_token', default=None,
         help='GitHub token to use, by default will use GITHUB_TOKEN environment variable')
     subcommands = parser.add_subparsers(dest='command', required=True)
     list_wfs_cmd_parser = subcommands.add_parser('list-workflows', help='List github workflows')
-    list_wfs_cmd_parser.add_argument('--local-only', action='store_true', dest='local_only',
-                                     help='Show only workflows stored in the repository')
+    list_wfs_cmd_parser.add_argument('--all', action='store_true', dest='external_workflows',
+                                     help='Show external workflows as well')
     list_actions_cmd_parser = subcommands.add_parser('list-actions', help='List actions in a workflow')
     list_actions_cmd_parser.add_argument('workflow_path', help='Workflow path')
     update_gha_cmd_parser = subcommands.add_parser('update', help='Update actions in github workflows')
     update_gha_cmd_parser.add_argument("--dry-run", action='store_true', dest='dryrun', help='List updates only')
     return parser.parse_args()
 
 
@@ -29,20 +35,20 @@
 
     def __init__(self, github_token: Optional[str]):
         github_token = github_token or os.getenv('GITHUB_TOKEN')
         if github_token is None:
             raise ValueError('GITHUB_TOKEN must be set')
         self.client = Github(login_or_token=github_token)
 
-    def get_github_workflows(self, repo_name: str, local_only: bool = False) -> List[Workflow]:
+    def get_github_workflows(self, repo_name: str, external_workflows: bool = False) -> List[Workflow]:
         if repo_name in self.workflows:
             return list(self.workflows[repo_name].values())
         repo = self.client.get_repo(repo_name)
         workflows = list(repo.get_workflows())
-        if local_only:
+        if not external_workflows:
             workflows = list(filter(lambda item: item.path.startswith('.github/'), workflows))
         self.workflows[repo_name] = {wf.path: wf for wf in workflows}
         return workflows
 
     def get_workflow_actions(self, repo_name: str, workflow_path: str) -> Set[str]:
 
         self.get_github_workflows(repo_name)
```

### Comparing `github_actions_cli-1.0.0b1/pyproject.toml` & `github_actions_cli-1.0.0b2/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,20 +1,24 @@
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
+[tool.poetry.scripts]
+github-actions-cli = "gha_cli.cli:run"
+
 [tool.poetry]
 name = "github-actions-cli"
-packages = [
-    { include = "gha-cli" },
-]
-version = "1.0.0b1"
+version = "1.0.0b2"
 description = "GitHub Actions CLI - allows updating workflows, etc."
 readme = "README.md"
 keywords = ["GitHub Actions", "CLI"]
+packages = [
+    { include = "gha_cli" },
+]
+
 authors = [
     "Daniel Moran <daniel@moransoftware.ca>",
 ]
 maintainers = [
     "Daniel Moran <daniel@moransoftware.ca>",
 ]
 license = "BSD-3-Clause"
@@ -35,15 +39,15 @@
 [tool.poetry.urls]
 "Bug Tracker" = "https://github.com/dsoftwareinc/github-actions-cli/issues"
 "Funding" = "https://github.com/sponsors/cunla"
 
 [tool.poetry.dependencies]
 python = "^3.9"
 pygithub = "^1.59"
-pyyaml = { version = "^6.0", optional = true }
+pyyaml = "^6.0"
 
 [tool.poetry.dev-dependencies]
 poetry = "^1.5"
 Flake8-pyproject = "^1.2"
 
 [tool.flake8]
 max-line-length = 119
```

### Comparing `github_actions_cli-1.0.0b1/PKG-INFO` & `github_actions_cli-1.0.0b2/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: github-actions-cli
-Version: 1.0.0b1
+Version: 1.0.0b2
 Summary: GitHub Actions CLI - allows updating workflows, etc.
 Home-page: https://github.com/dsoftwareinc/github-actions-cli
 License: BSD-3-Clause
 Keywords: GitHub Actions,CLI
 Author: Daniel Moran
 Author-email: daniel@moransoftware.ca
 Maintainer: Daniel Moran
@@ -14,30 +14,28 @@
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
 Requires-Dist: pygithub (>=1.59,<2.0)
 Requires-Dist: pyyaml (>=6.0,<7.0)
 Project-URL: Bug Tracker, https://github.com/dsoftwareinc/github-actions-cli/issues
 Project-URL: Documentation, https://github.com/dsoftwareinc/github-actions-cli
 Project-URL: Funding, https://github.com/sponsors/cunla
 Description-Content-Type: text/markdown
 
-GitHub Actions Utils
+GitHub Actions CLI
 ====================
 
 The purpose of this tool is to work with your GitHub Actions workflows in your repositories.
+It is complementary to the GitHub CLI.
 
 So far, three main flows are supported:
 
 # List all workflows path and name in a specified repository.
 
 Example:
```

