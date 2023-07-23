# Comparing `tmp/github_actions_cli-1.0.0b2.tar.gz` & `tmp/github_actions_cli-1.0.0b3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "github_actions_cli-1.0.0b2.tar", max compression
+gzip compressed data, was "github_actions_cli-1.0.0b3.tar", max compression
```

## Comparing `github_actions_cli-1.0.0b2.tar` & `github_actions_cli-1.0.0b3.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0     1500 2023-07-22 16:14:30.465697 github_actions_cli-1.0.0b2/LICENSE
--rw-r--r--   0        0        0     2016 2023-07-22 16:30:30.348267 github_actions_cli-1.0.0b2/README.md
--rw-r--r--   0        0        0        0 2023-07-22 19:45:14.822523 github_actions_cli-1.0.0b2/gha_cli/__init__.py
--rwxr-xr-x   0        0        0     5413 2023-07-22 19:40:09.586657 github_actions_cli-1.0.0b2/gha_cli/cli.py
--rw-r--r--   0        0        0     1513 2023-07-22 19:54:41.913866 github_actions_cli-1.0.0b2/pyproject.toml
--rw-r--r--   0        0        0     3251 1970-01-01 00:00:00.000000 github_actions_cli-1.0.0b2/PKG-INFO
+-rw-r--r--   0        0        0     1500 2023-07-22 16:14:30.465697 github_actions_cli-1.0.0b3/LICENSE
+-rw-r--r--   0        0        0     2084 2023-07-22 20:18:09.377125 github_actions_cli-1.0.0b3/README.md
+-rw-r--r--   0        0        0        0 2023-07-22 19:45:14.822523 github_actions_cli-1.0.0b3/gha_cli/__init__.py
+-rwxr-xr-x   0        0        0     7569 2023-07-23 17:03:29.066332 github_actions_cli-1.0.0b3/gha_cli/cli.py
+-rw-r--r--   0        0        0     1530 2023-07-23 17:03:49.850276 github_actions_cli-1.0.0b3/pyproject.toml
+-rw-r--r--   0        0        0     3357 1970-01-01 00:00:00.000000 github_actions_cli-1.0.0b3/PKG-INFO
```

### Comparing `github_actions_cli-1.0.0b2/LICENSE` & `github_actions_cli-1.0.0b3/LICENSE`

 * *Files identical despite different names*

### Comparing `github_actions_cli-1.0.0b2/README.md` & `github_actions_cli-1.0.0b3/README.md`

 * *Files 24% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 So far, three main flows are supported:
 
 # List all workflows path and name in a specified repository.
 
 Example:
 
 ```shell
-python ghautils.py cunla/fakeredis list-workflows
+github-actions-cli cunla/fakeredis list-workflows
 ```
 will return:
 
 ```text
 .github/workflows/publish.yml:Upload Python Package
 .github/workflows/test.yml:Unit tests
 dynamic/github-code-scanning/codeql:CodeQL
@@ -24,47 +24,53 @@
 
 # List all actions `uses` in a workflow
 
 Given a repo and a workflow path, return all actions in the workflow.
 
 Example:
 ```shell
-python ghautils.py cunla/fakeredis list-actions .github/workflows/publish.yml
+github-actions-cli cunla/fakeredis list-actions .github/workflows/publish.yml
 ```
 
 Result
 ```text
 pypa/gh-action-pypi-publish@release/v1
 actions/checkout@v3
 actions/setup-python@v4
 ```
 
 # Update all actions in a repository workflow(s)
 Show the latest versions of actions used in a repository workflow.
 
 Example:
 ```shell
-python ghautils.py cunla/fakeredis update
+github-actions-cli cunla/fakeredis update
 ```
 Result:
 ```text
 .github/workflows/publish.yml
   actions/setup-python @ v4     ==> v4.7.0
   pypa/gh-action-pypi-publish @ release/v1      ==> v1.8.8
   actions/checkout @ v3         ==> v3.5.3
 .github/workflows/test.yml
   actions/setup-python @ v4     ==> v4.7.0
   release-drafter/release-drafter @ v5  ==> v5.24.0
   actions/checkout @ v3         ==> v3.5.3
 ```
 
+# Installation
+
+```shell
+pip install github-actions-cli
+```
+
 # Help messages
 
 ```text
-usage: ghautils.py [-h] [--github-token GITHUB_TOKEN] repo {list-workflows,list-actions,update} ...
+usage: github-actions-cli [-h] [--github-token GITHUB_TOKEN] repo {list-workflows,list-actions,update} ...
 
 positional arguments:
   repo                  Repository to analyze
   {list-workflows,list-actions,update}
     list-workflows      List github workflows
     list-actions        List actions in a workflow
     update              Update actions in github workflows
```

### Comparing `github_actions_cli-1.0.0b2/gha_cli/cli.py` & `github_actions_cli-1.0.0b3/gha_cli/cli.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,67 +1,76 @@
 #!/usr/bin/env python3
-import argparse
 import logging
 import os
-from typing import Optional, List, Set, Tuple, Dict
+from typing import Optional, List, Set, Tuple, Dict, Union
 
+import click
 import yaml
 from github import Github, Workflow
 
 logging.basicConfig(level=logging.WARNING)
 logging.getLogger('github.Requester').setLevel(logging.WARNING)
 logger = logging.getLogger()
 
 
-def parse_args() -> argparse.Namespace:
-    parser = argparse.ArgumentParser()
-    parser.add_argument('repo', help='Repository to analyze')
-    parser.add_argument(
-        '--github-token', dest='github_token', default=None,
-        help='GitHub token to use, by default will use GITHUB_TOKEN environment variable')
-    subcommands = parser.add_subparsers(dest='command', required=True)
-    list_wfs_cmd_parser = subcommands.add_parser('list-workflows', help='List github workflows')
-    list_wfs_cmd_parser.add_argument('--all', action='store_true', dest='external_workflows',
-                                     help='Show external workflows as well')
-    list_actions_cmd_parser = subcommands.add_parser('list-actions', help='List actions in a workflow')
-    list_actions_cmd_parser.add_argument('workflow_path', help='Workflow path')
-    update_gha_cmd_parser = subcommands.add_parser('update', help='Update actions in github workflows')
-    update_gha_cmd_parser.add_argument("--dry-run", action='store_true', dest='dryrun', help='List updates only')
-    return parser.parse_args()
-
-
 class GithubActionsTools(object):
     workflows: dict[str, dict[str, Workflow]] = dict()  # repo_name -> [path -> workflow]
-    actions: dict[str, str] = dict()  # action_name -> latest_release_tag
+    actions_latest_release: dict[str, str] = dict()  # action_name@current_release -> latest_release_tag
 
     def __init__(self, github_token: Optional[str]):
         github_token = github_token or os.getenv('GITHUB_TOKEN')
         if github_token is None:
             raise ValueError('GITHUB_TOKEN must be set')
         self.client = Github(login_or_token=github_token)
 
-    def get_github_workflows(self, repo_name: str, external_workflows: bool = False) -> List[Workflow]:
-        if repo_name in self.workflows:
-            return list(self.workflows[repo_name].values())
-        repo = self.client.get_repo(repo_name)
-        workflows = list(repo.get_workflows())
-        if not external_workflows:
-            workflows = list(filter(lambda item: item.path.startswith('.github/'), workflows))
-        self.workflows[repo_name] = {wf.path: wf for wf in workflows}
-        return workflows
+    def is_local_repo(self, repo_name: str) -> bool:
+        return os.path.exists(repo_name)
 
-    def get_workflow_actions(self, repo_name: str, workflow_path: str) -> Set[str]:
+    @staticmethod
+    def list_full_paths(path: str) -> set[str]:
+        return {os.path.join(path, file)
+                for file in os.listdir(path)
+                if file.endswith(('.yml', '.yaml'))}
 
-        self.get_github_workflows(repo_name)
-        if workflow_path not in self.workflows[repo_name]:
-            raise ValueError(f'f{workflow_path} not found in workflows for repository {repo_name}, '
-                             f'possible values: {self.workflows[repo_name].keys()}')
+    def get_github_workflows(self, repo_name: str) -> Set[str]:
+        if repo_name in self.workflows:
+            return set(self.workflows[repo_name].keys())
+        # local
+        if self.is_local_repo(repo_name):
+            return self.list_full_paths(os.path.join(repo_name, '.github', 'workflows'))
+        # Remote
+        repo = self.client.get_repo(repo_name)
+        self.workflows[repo_name] = {
+            wf.path: wf
+            for wf in repo.get_workflows()
+            if wf.path.startswith('.github/')}
+        return set(self.workflows[repo_name].keys())
+
+    def _get_workflow_content(self, repo_name: str, workflow_path: str) -> Union[str, bytes]:
+        workflow_paths = self.get_github_workflows(repo_name)
+
+        if self.is_local_repo(repo_name):
+            if not os.path.exists(workflow_path):
+                click.echo(
+                    f'f{workflow_path} not found in workflows for repository {repo_name}, '
+                    f'possible values: {workflow_paths}', err=True)
+            with open(workflow_path) as f:
+                return f.read()
+
+        if workflow_path not in workflow_paths:
+            click.echo(
+                f'f{workflow_path} not found in workflows for repository {repo_name}, '
+                f'possible values: {workflow_paths}', err=True)
         repo = self.client.get_repo(repo_name)
         workflow_content = repo.get_contents(workflow_path)
-        workflow = yaml.load(workflow_content.decoded_content, Loader=yaml.CLoader)
+        return workflow_content.decoded_content
+
+    def get_workflow_actions(self, repo_name: str, workflow_path: str) -> Set[str]:
+        workflow_content = self._get_workflow_content(repo_name, workflow_path)
+        workflow = yaml.load(workflow_content, Loader=yaml.CLoader)
         res = set()
         for job in workflow.get('jobs', dict()).values():
             for step in job.get('steps', list()):
                 if 'uses' in step:
                     res.add(step['uses'])
         return res
 
@@ -74,48 +83,108 @@
             return None
         repo_name, current_version = action_name.split('@')
         repo = self.client.get_repo(repo_name)
         latest_release = repo.get_latest_release()
         return latest_release.tag_name if latest_release.tag_name != current_version else None
 
     def get_repo_actions_latest(self, repo_name: str) -> Dict[str, List[Tuple[str, str, Optional[str]]]]:
-        workflows = self.get_github_workflows(repo_name)
+        workflow_paths = self.get_github_workflows(repo_name)
         res = dict()
-        for workflow in workflows:
-            if not workflow.path.startswith('.github'):
-                continue
-            res[workflow.path] = list()
-            actions = self.get_workflow_actions(repo_name, workflow.path)
+        for path in workflow_paths:
+            res[path] = list()
+            actions = self.get_workflow_actions(repo_name, path)
             for action in actions:
                 if '@' not in action:
                     continue
                 action_name, curr_version = action.split('@')
-                latest = self.check_for_updates(action)
-                res[workflow.path].append((action_name, curr_version, latest))
+                if action not in self.actions_latest_release:
+                    latest = self.check_for_updates(action)
+                    self.actions_latest_release[action] = latest
+                else:
+                    latest = self.actions_latest_release[action]
+                res[path].append((action_name, curr_version, latest))
+        return res
+
+    def update_actions(
+            self, repo_name: str, workflow_path: str,
+            updates: List[Tuple[str, str, Optional[str]]],
+            commit_msg: str,
+    ) -> None:
+        workflow_content = self._get_workflow_content(repo_name, workflow_path)
+        if isinstance(workflow_content, bytes):
+            workflow_content = workflow_content.decode()
+        for update in updates:
+            if update[2] is None:
+                continue
+            current_action = f'{update[0]}@{update[1]}'
+            latest_action = f'{update[0]}@{update[2]}'
+            workflow_content = workflow_content.replace(current_action, latest_action)
+        self._update_workflow_content(repo_name, workflow_path, workflow_content, commit_msg)
+
+    def _update_workflow_content(
+            self, repo_name: str, workflow_path: str, workflow_content: str, commit_msg: str):
+        if self.is_local_repo(repo_name):
+            with open(workflow_path, 'w') as f:
+                f.write(workflow_content)
+                return
+        # remote
+        repo = self.client.get_repo(repo_name)
+        current_content = repo.get_contents(workflow_path)
+        res = repo.update_file(
+            workflow_path,
+            commit_msg,
+            workflow_content,
+            current_content.sha,
+        )
         return res
 
 
-def run():
-    args = parse_args()
-    gh = GithubActionsTools(args.github_token)
-    gh.check_for_updates('actions/checkout@v2')
-    if args.command == 'list-workflows':
-        workflows = gh.get_github_workflows(args.repo)
-        for workflow in workflows:
-            print(f'{workflow.path}:{workflow.name}')
-    elif args.command == 'list-actions':
-        actions = gh.get_workflow_actions(args.repo, args.workflow_path)
-        for action in actions:
-            print(action)
-    elif args.command == 'update':
-        action_versions = gh.get_repo_actions_latest(args.repo)
-        for wf in action_versions:
-            print(f'{wf}:')
-            for action in action_versions[wf]:
-                s = f'  {action[0]} @ {action[1]}'
-                if action[2]:
-                    s += f' \t==> {action[2]}'
-                print(s)
+@click.group()
+@click.option('-repo', default='.', help='Repository to analyze')
+@click.option('--github-token', default=os.getenv('GITHUB_TOKEN'),
+              help='GitHub token to use, by default will use GITHUB_TOKEN environment variable')
+@click.pass_context
+def cli(ctx, repo: str, github_token: str):
+    ctx.obj['gh'] = GithubActionsTools(github_token)
+    ctx.obj['repo'] = repo
+
+
+@cli.command(help='List actions in a workflow')
+@click.option('--dry-run', default=False, help='Do not update, list only')
+@click.option('-commit-msg', default='Update github-actions',
+              help='Commit msg, only relevant when remote repo')
+@click.pass_context
+def update_actions(ctx, dry_run: bool, commit_msg: str):
+    gh, repo = ctx.obj['gh'], ctx.obj['repo']
+    action_versions = gh.get_repo_actions_latest(repo)
+    for wf in action_versions:
+        click.echo(f'{wf}:')
+        for action in action_versions[wf]:
+            s = f'  {action[0]} @ {action[1]}'
+            if action[2]:
+                s += f' \t==> {action[2]}'
+            click.echo(s)
+    if dry_run:
+        return
+    for wf in action_versions:
+        gh.update_actions(repo, wf, action_versions[wf], commit_msg)
+
+
+@cli.command(help='List actions in a workflow')
+@click.argument('workflow')
+@click.pass_context
+def list_actions(ctx, workflow: str):
+    actions = ctx.obj['gh'].get_workflow_actions(ctx.obj['repo'], workflow)
+    for action in actions:
+        click.echo(action)
+
+
+@cli.command(help='List workflows in repository')
+@click.pass_context
+def list_workflows(ctx):
+    workflow_paths = ctx.obj['gh'].get_github_workflows(ctx.obj['repo'])
+    for path in workflow_paths:
+        click.echo(f'{path}')
 
 
 if __name__ == '__main__':
-    run()
+    cli(obj={})
```

### Comparing `github_actions_cli-1.0.0b2/pyproject.toml` & `github_actions_cli-1.0.0b3/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry.scripts]
-github-actions-cli = "gha_cli.cli:run"
+github-actions-cli = "gha_cli.cli:cli"
 
 [tool.poetry]
 name = "github-actions-cli"
-version = "1.0.0b2"
+version = "1.0.0b3"
 description = "GitHub Actions CLI - allows updating workflows, etc."
 readme = "README.md"
 keywords = ["GitHub Actions", "CLI"]
 packages = [
     { include = "gha_cli" },
 ]
 
@@ -40,14 +40,15 @@
 "Bug Tracker" = "https://github.com/dsoftwareinc/github-actions-cli/issues"
 "Funding" = "https://github.com/sponsors/cunla"
 
 [tool.poetry.dependencies]
 python = "^3.9"
 pygithub = "^1.59"
 pyyaml = "^6.0"
+click = "^8.1.6"
 
 [tool.poetry.dev-dependencies]
 poetry = "^1.5"
 Flake8-pyproject = "^1.2"
 
 [tool.flake8]
 max-line-length = 119
```

### Comparing `github_actions_cli-1.0.0b2/PKG-INFO` & `github_actions_cli-1.0.0b3/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: github-actions-cli
-Version: 1.0.0b2
+Version: 1.0.0b3
 Summary: GitHub Actions CLI - allows updating workflows, etc.
 Home-page: https://github.com/dsoftwareinc/github-actions-cli
 License: BSD-3-Clause
 Keywords: GitHub Actions,CLI
 Author: Daniel Moran
 Author-email: daniel@moransoftware.ca
 Maintainer: Daniel Moran
@@ -16,14 +16,15 @@
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Requires-Dist: click (>=8.1.6,<9.0.0)
 Requires-Dist: pygithub (>=1.59,<2.0)
 Requires-Dist: pyyaml (>=6.0,<7.0)
 Project-URL: Bug Tracker, https://github.com/dsoftwareinc/github-actions-cli/issues
 Project-URL: Documentation, https://github.com/dsoftwareinc/github-actions-cli
 Project-URL: Funding, https://github.com/sponsors/cunla
 Description-Content-Type: text/markdown
 
@@ -36,15 +37,15 @@
 So far, three main flows are supported:
 
 # List all workflows path and name in a specified repository.
 
 Example:
 
 ```shell
-python ghautils.py cunla/fakeredis list-workflows
+github-actions-cli cunla/fakeredis list-workflows
 ```
 will return:
 
 ```text
 .github/workflows/publish.yml:Upload Python Package
 .github/workflows/test.yml:Unit tests
 dynamic/github-code-scanning/codeql:CodeQL
@@ -53,47 +54,53 @@
 
 # List all actions `uses` in a workflow
 
 Given a repo and a workflow path, return all actions in the workflow.
 
 Example:
 ```shell
-python ghautils.py cunla/fakeredis list-actions .github/workflows/publish.yml
+github-actions-cli cunla/fakeredis list-actions .github/workflows/publish.yml
 ```
 
 Result
 ```text
 pypa/gh-action-pypi-publish@release/v1
 actions/checkout@v3
 actions/setup-python@v4
 ```
 
 # Update all actions in a repository workflow(s)
 Show the latest versions of actions used in a repository workflow.
 
 Example:
 ```shell
-python ghautils.py cunla/fakeredis update
+github-actions-cli cunla/fakeredis update
 ```
 Result:
 ```text
 .github/workflows/publish.yml
   actions/setup-python @ v4     ==> v4.7.0
   pypa/gh-action-pypi-publish @ release/v1      ==> v1.8.8
   actions/checkout @ v3         ==> v3.5.3
 .github/workflows/test.yml
   actions/setup-python @ v4     ==> v4.7.0
   release-drafter/release-drafter @ v5  ==> v5.24.0
   actions/checkout @ v3         ==> v3.5.3
 ```
 
+# Installation
+
+```shell
+pip install github-actions-cli
+```
+
 # Help messages
 
 ```text
-usage: ghautils.py [-h] [--github-token GITHUB_TOKEN] repo {list-workflows,list-actions,update} ...
+usage: github-actions-cli [-h] [--github-token GITHUB_TOKEN] repo {list-workflows,list-actions,update} ...
 
 positional arguments:
   repo                  Repository to analyze
   {list-workflows,list-actions,update}
     list-workflows      List github workflows
     list-actions        List actions in a workflow
     update              Update actions in github workflows
```

