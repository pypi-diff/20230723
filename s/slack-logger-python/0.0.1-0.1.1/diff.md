# Comparing `tmp/slack-logger-python-0.0.1.tar.gz` & `tmp/slack-logger-python-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "slack-logger-python-0.0.1.tar", last modified: Mon Jul 17 22:34:50 2023, max compression
+gzip compressed data, was "slack-logger-python-0.1.1.tar", last modified: Sun Jul 23 01:00:13 2023, max compression
```

## Comparing `slack-logger-python-0.0.1.tar` & `slack-logger-python-0.1.1.tar`

### file list

```diff
@@ -1,30 +1,32 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-17 22:34:50.791881 slack-logger-python-0.0.1/
--rw-r--r--   0 runner    (1001) docker     (123)      254 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/.envrc
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-17 22:34:50.787881 slack-logger-python-0.0.1/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-17 22:34:50.791881 slack-logger-python-0.0.1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     2685 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/.github/workflows/deploy.yml
--rw-r--r--   0 runner    (1001) docker     (123)     2690 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/.github/workflows/format.yml
--rw-r--r--   0 runner    (1001) docker     (123)     2255 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/.gitignore
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-17 22:34:50.791881 slack-logger-python-0.0.1/.vscode/
--rw-r--r--   0 runner    (1001) docker     (123)      156 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/.vscode/extensions.json
--rw-r--r--   0 runner    (1001) docker     (123)      303 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/.vscode/settings.json
--rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1961 2023-07-17 22:34:50.791881 slack-logger-python-0.0.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      867 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/README.md
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/VERSION
--rw-r--r--   0 runner    (1001) docker     (123)     3107 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       29 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/requirements_dev.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-17 22:34:50.791881 slack-logger-python-0.0.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1363 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/shell.nix
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-17 22:34:50.791881 slack-logger-python-0.0.1/slack_logger/
--rw-r--r--   0 runner    (1001) docker     (123)     5051 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/slack_logger/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-17 22:34:50.791881 slack-logger-python-0.0.1/slack_logger_python.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1961 2023-07-17 22:34:50.000000 slack-logger-python-0.0.1/slack_logger_python.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      487 2023-07-17 22:34:50.000000 slack-logger-python-0.0.1/slack_logger_python.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-17 22:34:50.000000 slack-logger-python-0.0.1/slack_logger_python.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-17 22:34:50.000000 slack-logger-python-0.0.1/slack_logger_python.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-17 22:34:50.000000 slack-logger-python-0.0.1/slack_logger_python.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-17 22:34:50.791881 slack-logger-python-0.0.1/tests/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2276 2023-07-17 22:34:37.000000 slack-logger-python-0.0.1/tests/test_basic.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 01:00:13.627708 slack-logger-python-0.1.1/
+-rw-r--r--   0 runner    (1001) docker     (123)      254 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/.envrc
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 01:00:13.623708 slack-logger-python-0.1.1/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 01:00:13.623708 slack-logger-python-0.1.1/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     2903 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/.github/workflows/deploy.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     2484 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/.github/workflows/format.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/.github/workflows/tagging.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     2255 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/.gitignore
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 01:00:13.623708 slack-logger-python-0.1.1/.vscode/
+-rw-r--r--   0 runner    (1001) docker     (123)      156 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/.vscode/extensions.json
+-rw-r--r--   0 runner    (1001) docker     (123)      303 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/.vscode/settings.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3325 2023-07-23 01:00:13.627708 slack-logger-python-0.1.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2231 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/VERSION
+-rw-r--r--   0 runner    (1001) docker     (123)     3145 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       29 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/requirements_dev.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 01:00:13.627708 slack-logger-python-0.1.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1327 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/shell.nix
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 01:00:13.623708 slack-logger-python-0.1.1/slack_logger/
+-rw-r--r--   0 runner    (1001) docker     (123)    11138 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/slack_logger/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       26 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/slack_logger/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 01:00:13.627708 slack-logger-python-0.1.1/slack_logger_python.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3325 2023-07-23 01:00:13.000000 slack-logger-python-0.1.1/slack_logger_python.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      539 2023-07-23 01:00:13.000000 slack-logger-python-0.1.1/slack_logger_python.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 01:00:13.000000 slack-logger-python-0.1.1/slack_logger_python.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 01:00:13.000000 slack-logger-python-0.1.1/slack_logger_python.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-23 01:00:13.000000 slack-logger-python-0.1.1/slack_logger_python.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 01:00:13.627708 slack-logger-python-0.1.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13056 2023-07-23 01:00:03.000000 slack-logger-python-0.1.1/tests/test_basic.py
```

### Comparing `slack-logger-python-0.0.1/.github/workflows/deploy.yml` & `slack-logger-python-0.1.1/.github/workflows/deploy.yml`

 * *Files 7% similar despite different names*

```diff
@@ -4,17 +4,18 @@
   push:
     branches: [ main ]
     tags: [ v* ]
   pull_request:
     types: [ opened, synchronize ]
   workflow_dispatch:
 
+
 permissions:
-  id-token: write
   contents: read
+  id-token: write
 
 env:
   REGISTRY: ghcr.io
   REPOSITORY: ${{ github.repository }} # <owner/repo>
   MODULE_NAME: slack_logger
   VERSION: ${{ github.ref_type == 'tag' && github.ref_name || github.event.pull_request.head.sha || github.sha  }}
 
@@ -36,63 +37,66 @@
 
       - name: Checkout Source Code
         uses: actions/checkout@c85c95e3d7251135ab7dc9ce3241c5835cc595a9 # pin@v3
         with:
           ref: ${{ github.event.pull_request.head.sha }}
 
       - name: Set up Python
-        uses: actions/setup-python@v3
+        uses: actions/setup-python@3542bca2639a428e1796aaa6a2ffef0c0f575566 # pin@v3
         with:
           python-version: "3.10"
           cache: "pip"
 
       - name: pip | Install Dependencies
         run: pip install -r requirements_dev.txt -r requirements.txt
 
       # The official isort action does not provide any output in the success case
       - name: isort | Import Order Check
         run: isort --check-only --diff --verbose .
 
       - name: black | Format Check
-        uses: psf/black@stable
+        uses: psf/black@193ee766ca496871f93621d6b58d57a6564ff81b # pin@stable
         with:
           options: "--check --diff --verbose"
 
       - name: ruff | Lint Check
         id: lint
-        run: ruff check ${{env.MODULE_NAME}}
+        run: ruff check ${{env.MODULE_NAME}} tests
 
       - name: mypy | Type Check
         run: |
           set -o pipefail
-          mypy ${{env.MODULE_NAME}}
+          mypy ${{env.MODULE_NAME}} tests
+
+      - name: pytest | Run Tests
+        run: |
+          pytest
 
   deploy:
     name: "Deploy"
     runs-on: ubuntu-latest
     timeout-minutes: 15
-    # environment: ${{ github.ref_type == 'tag' && 'prod' || 'dev' }}
-    # TODO:
+    if: github.ref_type == 'tag'
     environment: 'prod'
     needs:
       - check
 
     steps:
       - name: Checkout Source Code
         uses: actions/checkout@c85c95e3d7251135ab7dc9ce3241c5835cc595a9 # pin@v3
         with:
           ref: ${{ github.event.pull_request.head.sha }}
 
       - name: Set up Python
-        uses: actions/setup-python@v3
+        uses: actions/setup-python@3542bca2639a428e1796aaa6a2ffef0c0f575566 # pin@v3
         with:
           python-version: "3.10"
           cache: "pip"
 
       - name: pip | Install Dependencies
         run: pip install build
 
       - name: Build
         run: python -m build
 
       - name: Publish package distributions to PyPI
-        uses: pypa/gh-action-pypi-publish@release/v1
+        uses: pypa/gh-action-pypi-publish@f8c70e705ffc13c3b4d1221169b84f12a75d6ca8 # pin@release/v1
```

### Comparing `slack-logger-python-0.0.1/.github/workflows/format.yml` & `slack-logger-python-0.1.1/.github/workflows/format.yml`

 * *Files 12% similar despite different names*

```diff
@@ -2,72 +2,68 @@
 
 on:
   pull_request:
     types: [ opened ]
   issue_comment:
     types: [ created ]
 
+permissions:
+  contents: write
+
 jobs:
   format:
     name: "Format"
     runs-on: ubuntu-22.04
     if: github.event.issue.pull_request
     steps:
-      - name: Generate github token
-        id: generate-token
-        uses: tibdex/github-app-token@b62528385c34dbc9f38e5f4225ac829252d1ea92 # pin@v1
-        with:
-          app_id: ${{ secrets.GH_APP_ID }}
-          private_key: ${{ secrets.GH_PRIVATE_KEY }}
-
       - uses: khan/pull-request-comment-trigger@edab8d9ba7759221187ef7120592a6fbfada0d18 # pin@v1.1.0
         id: check
         with:
           trigger: '/format'
           reaction: "+1" # Reaction must be one of the reactions here: https://developer.github.com/v3/reactions/#reaction-types
         env:
-          GITHUB_TOKEN: ${{ steps.generate-token.outputs.token }}
+          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
 
-      - uses: actions/checkout@8e5e7e5ab8b370d6c329ec480221332ada57f0ab # pin@v3
+      - uses: actions/checkout@c85c95e3d7251135ab7dc9ce3241c5835cc595a9 # pin@v3
         if: steps.check.outputs.triggered == 'true'
         with:
-          token: ${{ steps.generate-token.outputs.token }}
+          token: ${{ secrets.GITHUB_TOKEN }}
 
       - name: Check out PR
         if: steps.check.outputs.triggered == 'true'
         env:
-          GITHUB_TOKEN: ${{ steps.generate-token.outputs.token }}
+          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
         run: |
           gh pr checkout ${{ github.event.issue.number }}
 
       - name: Set up Python
-        uses: actions/setup-python@v3
+        uses: actions/setup-python@3542bca2639a428e1796aaa6a2ffef0c0f575566 # pin@v3
         if: steps.check.outputs.triggered == 'true'
         with:
           python-version: "3.10"
           cache: "pip"
 
       - name: Install
         if: steps.check.outputs.triggered == 'true'
         run: pip install black isort
 
       - name: Format using black
-        uses: psf/black@stable
+        uses: psf/black@193ee766ca496871f93621d6b58d57a6564ff81b # pin@stable
         if: steps.check.outputs.triggered == 'true'
         with:
           options: "--verbose"
 
       - name: Sort imports using isort
         if: steps.check.outputs.triggered == 'true'
         run: isort --verbose .
 
       - name: Commit changes
         if: steps.check.outputs.triggered == 'true'
         env:
-          GITHUB_TOKEN: ${{ steps.generate-token.outputs.token }}
+          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
         run: |
           git config user.name "GitHub Actions Bot"
           git config user.email "<>"
 
           git status
           git diff --stat
           git commit -am "chore: format code"
@@ -78,8 +74,8 @@
 
       - uses: khan/pull-request-comment-trigger@edab8d9ba7759221187ef7120592a6fbfada0d18 # pin@v1.1.0
         if: failure()
         with:
           trigger: '/format'
           reaction: "confused" # Reaction must be one of the reactions here: https://developer.github.com/v3/reactions/#reaction-types
         env:
-          GITHUB_TOKEN: ${{ steps.generate-token.outputs.token }}
+          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

### Comparing `slack-logger-python-0.0.1/.gitignore` & `slack-logger-python-0.1.1/.gitignore`

 * *Files identical despite different names*

### Comparing `slack-logger-python-0.0.1/LICENSE` & `slack-logger-python-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `slack-logger-python-0.0.1/pyproject.toml` & `slack-logger-python-0.1.1/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -26,14 +26,17 @@
     "Topic :: Internet :: WWW/HTTP",
     "Topic :: Internet :: WWW/HTTP :: Dynamic Content",
     "Topic :: System :: Logging",
 ]
 
 dynamic = ["dependencies", "version"]
 
+[tool.setuptools.package-data]
+slack_logger = ["py.typed"]
+
 [tool.setuptools.dynamic]
 version = {file = "VERSION"}
 dependencies = {file = ["requirements.txt"]}
 
 [[project.authors]]
 name = "GRBurst"
 email = "GRBurst@protonmail.com"
@@ -120,14 +123,12 @@
 disallow_untyped_defs = true
 warn_return_any = true
 warn_unused_configs = true
 
 
 [tool.pytest.ini_options]
 minversion = "6.0"
-addopts = "-ra -s"
+addopts = "-ra --capture=tee-sys"
 log_cli = true
-log_level = "NOTSET"
-capture = false
 testpaths = [
     "tests",
 ]
```

