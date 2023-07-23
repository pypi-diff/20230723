# Comparing `tmp/llm-claude-0.1.0.tar.gz` & `tmp/llm-claude-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "llm-claude-0.1.0.tar", last modified: Mon Jul 17 19:03:52 2023, max compression
+gzip compressed data, was "llm-claude-0.2.0.tar", last modified: Sun Jul 23 10:40:43 2023, max compression
```

## Comparing `llm-claude-0.1.0.tar` & `llm-claude-0.2.0.tar`

### file list

```diff
@@ -1,14 +1,43 @@
-drwxr-xr-x   0 tom        (501) staff       (20)        0 2023-07-17 19:03:52.758383 llm-claude-0.1.0/
--rw-r--r--   0 tom        (501) staff       (20)    11357 2023-07-17 18:19:14.000000 llm-claude-0.1.0/LICENSE
--rw-r--r--   0 tom        (501) staff       (20)       76 2023-07-17 19:03:52.758260 llm-claude-0.1.0/PKG-INFO
--rw-r--r--   0 tom        (501) staff       (20)       73 2023-07-17 18:19:14.000000 llm-claude-0.1.0/README.md
-drwxr-xr-x   0 tom        (501) staff       (20)        0 2023-07-17 19:03:52.758121 llm-claude-0.1.0/llm_claude.egg-info/
--rw-r--r--   0 tom        (501) staff       (20)       76 2023-07-17 19:03:52.000000 llm-claude-0.1.0/llm_claude.egg-info/PKG-INFO
--rw-r--r--   0 tom        (501) staff       (20)      252 2023-07-17 19:03:52.000000 llm-claude-0.1.0/llm_claude.egg-info/SOURCES.txt
--rw-r--r--   0 tom        (501) staff       (20)        1 2023-07-17 19:03:52.000000 llm-claude-0.1.0/llm_claude.egg-info/dependency_links.txt
--rw-r--r--   0 tom        (501) staff       (20)       26 2023-07-17 19:03:52.000000 llm-claude-0.1.0/llm_claude.egg-info/entry_points.txt
--rw-r--r--   0 tom        (501) staff       (20)        6 2023-07-17 19:03:52.000000 llm-claude-0.1.0/llm_claude.egg-info/requires.txt
--rw-r--r--   0 tom        (501) staff       (20)       11 2023-07-17 19:03:52.000000 llm-claude-0.1.0/llm_claude.egg-info/top_level.txt
--rw-r--r--   0 tom        (501) staff       (20)      794 2023-07-17 18:56:40.000000 llm-claude-0.1.0/llm_claude.py
--rw-r--r--   0 tom        (501) staff       (20)      129 2023-07-17 19:01:29.000000 llm-claude-0.1.0/pyproject.toml
--rw-r--r--   0 tom        (501) staff       (20)       38 2023-07-17 19:03:52.758419 llm-claude-0.1.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:43.660306 llm-claude-0.2.0/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 10:40:29.000000 llm-claude-0.2.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2347 2023-07-23 10:40:43.660306 llm-claude-0.2.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1981 2023-07-23 10:40:29.000000 llm-claude-0.2.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:43.656306 llm-claude-0.2.0/llm_claude/
+-rw-r--r--   0 runner    (1001) docker     (123)     1699 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:43.660306 llm-claude-0.2.0/llm_claude/vendored_anthropic/
+-rw-r--r--   0 runner    (1001) docker     (123)     1999 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    46863 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_base_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3889 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_base_exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15329 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)      112 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1285 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7631 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_models.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4846 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_qs.py
+-rw-r--r--   0 runner    (1001) docker     (123)      896 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_resource.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7126 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_streaming.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1186 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_tokenizers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4299 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_types.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:43.660306 llm-claude-0.2.0/llm_claude/vendored_anthropic/_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)     1277 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6787 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_utils/_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9690 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_utils/_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)      128 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)      168 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/pagination.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:43.660306 llm-claude-0.2.0/llm_claude/vendored_anthropic/resources/
+-rw-r--r--   0 runner    (1001) docker     (123)      156 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/resources/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21486 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/resources/completions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:43.660306 llm-claude-0.2.0/llm_claude/vendored_anthropic/types/
+-rw-r--r--   0 runner    (1001) docker     (123)      226 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/types/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      664 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/types/completion.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7015 2023-07-23 10:40:29.000000 llm-claude-0.2.0/llm_claude/vendored_anthropic/types/completion_create_params.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:43.656306 llm-claude-0.2.0/llm_claude.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2347 2023-07-23 10:40:43.000000 llm-claude-0.2.0/llm_claude.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1306 2023-07-23 10:40:43.000000 llm-claude-0.2.0/llm_claude.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 10:40:43.000000 llm-claude-0.2.0/llm_claude.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       26 2023-07-23 10:40:43.000000 llm-claude-0.2.0/llm_claude.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-07-23 10:40:43.000000 llm-claude-0.2.0/llm_claude.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-07-23 10:40:43.000000 llm-claude-0.2.0/llm_claude.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      678 2023-07-23 10:40:29.000000 llm-claude-0.2.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 10:40:43.660306 llm-claude-0.2.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:40:43.660306 llm-claude-0.2.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     2779 2023-07-23 10:40:29.000000 llm-claude-0.2.0/tests/test_llm_claude.py
```

### Comparing `llm-claude-0.1.0/LICENSE` & `llm-claude-0.2.0/LICENSE`

 * *Files identical despite different names*

