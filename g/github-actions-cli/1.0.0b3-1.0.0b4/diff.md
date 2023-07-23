# Comparing `tmp/github_actions_cli-1.0.0b3.tar.gz` & `tmp/github_actions_cli-1.0.0b4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "github_actions_cli-1.0.0b3.tar", max compression
+gzip compressed data, was "github_actions_cli-1.0.0b4.tar", max compression
```

## Comparing `github_actions_cli-1.0.0b3.tar` & `github_actions_cli-1.0.0b4.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0     1500 2023-07-22 16:14:30.465697 github_actions_cli-1.0.0b3/LICENSE
--rw-r--r--   0        0        0     2084 2023-07-22 20:18:09.377125 github_actions_cli-1.0.0b3/README.md
--rw-r--r--   0        0        0        0 2023-07-22 19:45:14.822523 github_actions_cli-1.0.0b3/gha_cli/__init__.py
--rwxr-xr-x   0        0        0     7569 2023-07-23 17:03:29.066332 github_actions_cli-1.0.0b3/gha_cli/cli.py
--rw-r--r--   0        0        0     1530 2023-07-23 17:03:49.850276 github_actions_cli-1.0.0b3/pyproject.toml
--rw-r--r--   0        0        0     3357 1970-01-01 00:00:00.000000 github_actions_cli-1.0.0b3/PKG-INFO
+-rw-r--r--   0        0        0     1500 2023-07-22 16:14:30.465697 github_actions_cli-1.0.0b4/LICENSE
+-rw-r--r--   0        0        0     2084 2023-07-22 20:18:09.377125 github_actions_cli-1.0.0b4/README.md
+-rw-r--r--   0        0        0        0 2023-07-22 19:45:14.822523 github_actions_cli-1.0.0b4/gha_cli/__init__.py
+-rwxr-xr-x   0        0        0     7597 2023-07-23 17:06:45.151604 github_actions_cli-1.0.0b4/gha_cli/cli.py
+-rw-r--r--   0        0        0     1530 2023-07-23 17:06:56.638901 github_actions_cli-1.0.0b4/pyproject.toml
+-rw-r--r--   0        0        0     3357 1970-01-01 00:00:00.000000 github_actions_cli-1.0.0b4/PKG-INFO
```

### Comparing `github_actions_cli-1.0.0b3/LICENSE` & `github_actions_cli-1.0.0b4/LICENSE`

 * *Files identical despite different names*

### Comparing `github_actions_cli-1.0.0b3/README.md` & `github_actions_cli-1.0.0b4/README.md`

 * *Files identical despite different names*

### Comparing `github_actions_cli-1.0.0b3/gha_cli/cli.py` & `github_actions_cli-1.0.0b4/gha_cli/cli.py`

 * *Files 1% similar despite different names*

```diff
@@ -140,14 +140,15 @@
 
 @click.group()
 @click.option('-repo', default='.', help='Repository to analyze')
 @click.option('--github-token', default=os.getenv('GITHUB_TOKEN'),
               help='GitHub token to use, by default will use GITHUB_TOKEN environment variable')
 @click.pass_context
 def cli(ctx, repo: str, github_token: str):
+    ctx.ensure_object(dict)
     ctx.obj['gh'] = GithubActionsTools(github_token)
     ctx.obj['repo'] = repo
 
 
 @cli.command(help='List actions in a workflow')
 @click.option('--dry-run', default=False, help='Do not update, list only')
 @click.option('-commit-msg', default='Update github-actions',
```

### Comparing `github_actions_cli-1.0.0b3/pyproject.toml` & `github_actions_cli-1.0.0b4/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry.scripts]
 github-actions-cli = "gha_cli.cli:cli"
 
 [tool.poetry]
 name = "github-actions-cli"
-version = "1.0.0b3"
+version = "1.0.0b4"
 description = "GitHub Actions CLI - allows updating workflows, etc."
 readme = "README.md"
 keywords = ["GitHub Actions", "CLI"]
 packages = [
     { include = "gha_cli" },
 ]
```

### Comparing `github_actions_cli-1.0.0b3/PKG-INFO` & `github_actions_cli-1.0.0b4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: github-actions-cli
-Version: 1.0.0b3
+Version: 1.0.0b4
 Summary: GitHub Actions CLI - allows updating workflows, etc.
 Home-page: https://github.com/dsoftwareinc/github-actions-cli
 License: BSD-3-Clause
 Keywords: GitHub Actions,CLI
 Author: Daniel Moran
 Author-email: daniel@moransoftware.ca
 Maintainer: Daniel Moran
```

