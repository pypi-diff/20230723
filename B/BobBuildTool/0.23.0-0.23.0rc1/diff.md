# Comparing `tmp/BobBuildTool-0.23.0.tar.gz` & `tmp/BobBuildTool-0.23.0rc1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "BobBuildTool-0.23.0.tar", last modified: Sun Jul 23 09:41:47 2023, max compression
+gzip compressed data, was "BobBuildTool-0.23.0rc1.tar", last modified: Fri Jul  7 20:03:25 2023, max compression
```

## Comparing `BobBuildTool-0.23.0.tar` & `BobBuildTool-0.23.0rc1.tar`

### file list

```diff
@@ -1,177 +1,177 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.842764 BobBuildTool-0.23.0/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.826764 BobBuildTool-0.23.0/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.830764 BobBuildTool-0.23.0/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     4953 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/.github/workflows/workflow.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      103 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      125 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/.readthedocs.yaml
--rw-r--r--   0 runner    (1001) docker     (123)    35498 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       88 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     2523 2023-07-23 09:41:47.842764 BobBuildTool-0.23.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1750 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/README.md
--rwxr-xr-x   0 runner    (1001) docker     (123)      345 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/bob
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/bob.cmd
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.830764 BobBuildTool-0.23.0/contrib/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.830764 BobBuildTool-0.23.0/contrib/bash-completion/
--rw-r--r--   0 runner    (1001) docker     (123)    13471 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/contrib/bash-completion/bob
--rw-r--r--   0 runner    (1001) docker     (123)     3537 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/contrib/cleanup-recipes.awk
--rwxr-xr-x   0 runner    (1001) docker     (123)     1480 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/contrib/create-release.sh
--rwxr-xr-x   0 runner    (1001) docker     (123)      551 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/contrib/notify.sh
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.830764 BobBuildTool-0.23.0/contrib/plugins/
--rw-r--r--   0 runner    (1001) docker     (123)     3880 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/contrib/plugins/jenkins-cobertura.py
--rw-r--r--   0 runner    (1001) docker     (123)      886 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/contrib/plugins/override.py
--rw-r--r--   0 runner    (1001) docker     (123)     2334 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/contrib/plugins/path-fmt.py
--rw-r--r--   0 runner    (1001) docker     (123)     1811 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/contrib/sandbox.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.830764 BobBuildTool-0.23.0/doc/
--rw-r--r--   0 runner    (1001) docker     (123)    52308 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/BOB_Logo.png
--rw-r--r--   0 runner    (1001) docker     (123)    51445 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/BOB_Logo.svg
--rw-r--r--   0 runner    (1001) docker     (123)     6750 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/Makefile
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.830764 BobBuildTool-0.23.0/doc/_build/
--rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/_build/.gitignore
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.830764 BobBuildTool-0.23.0/doc/_static/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/_static/.gitkeep
--rw-r--r--   0 runner    (1001) docker     (123)   218324 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/_static/d3.v4.min.js
--rw-r--r--   0 runner    (1001) docker     (123)    25786 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/_static/sandbox.html
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.830764 BobBuildTool-0.23.0/doc/_templates/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/_templates/.gitkeep
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.834764 BobBuildTool-0.23.0/doc/cheatsheet/
--rw-r--r--   0 runner    (1001) docker     (123)    67229 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/cheatsheet/bob_cheatsheet.pdf
--rw-r--r--   0 runner    (1001) docker     (123)     9819 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/cheatsheet/bob_cheatsheet.tex
--rw-r--r--   0 runner    (1001) docker     (123)    11668 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)     1456 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/glossary.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.834764 BobBuildTool-0.23.0/doc/images/
--rw-r--r--   0 runner    (1001) docker     (123)   129885 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/images/jenkins.odg
--rw-r--r--   0 runner    (1001) docker     (123)    48173 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/images/jenkins.png
--rw-r--r--   0 runner    (1001) docker     (123)    10648 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/images/overview.odg
--rw-r--r--   0 runner    (1001) docker     (123)    17248 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/images/overview.png
--rw-r--r--   0 runner    (1001) docker     (123)    28093 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/images/recipe-flow.odg
--rw-r--r--   0 runner    (1001) docker     (123)    80846 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/images/recipe-flow.png
--rw-r--r--   0 runner    (1001) docker     (123)    47205 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/images/sandbox_graph.png
--rw-r--r--   0 runner    (1001) docker     (123)    18826 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/images/variant-management.odg
--rw-r--r--   0 runner    (1001) docker     (123)    19985 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/images/variant-management.png
--rw-r--r--   0 runner    (1001) docker     (123)     1677 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)     7807 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/installation.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.834764 BobBuildTool-0.23.0/doc/manpages/
--rw-r--r--   0 runner    (1001) docker     (123)     7193 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-archive.rst
--rw-r--r--   0 runner    (1001) docker     (123)    10832 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-build-dev.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-build.rst
--rw-r--r--   0 runner    (1001) docker     (123)     3915 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-clean.rst
--rw-r--r--   0 runner    (1001) docker     (123)     3231 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-dev.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2323 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-graph.rst
--rw-r--r--   0 runner    (1001) docker     (123)      579 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-init.rst
--rw-r--r--   0 runner    (1001) docker     (123)    25086 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-jenkins.rst
--rw-r--r--   0 runner    (1001) docker     (123)     3614 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-ls.rst
--rw-r--r--   0 runner    (1001) docker     (123)     6393 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-project.rst
--rw-r--r--   0 runner    (1001) docker     (123)      681 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-query-meta.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1546 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-query-path.rst
--rw-r--r--   0 runner    (1001) docker     (123)      561 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-query-recipe.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1169 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-query-scm.rst
--rw-r--r--   0 runner    (1001) docker     (123)     3448 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-show.rst
--rw-r--r--   0 runner    (1001) docker     (123)     6536 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob-status.rst
--rw-r--r--   0 runner    (1001) docker     (123)     3595 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bob.rst
--rw-r--r--   0 runner    (1001) docker     (123)    14703 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/bobpaths.rst
--rw-r--r--   0 runner    (1001) docker     (123)      298 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)      481 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manpages/std-opt-cfg.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.834764 BobBuildTool-0.23.0/doc/manual/
--rw-r--r--   0 runner    (1001) docker     (123)     9298 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manual/audit-trail.rst
--rw-r--r--   0 runner    (1001) docker     (123)    14381 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manual/concepts.rst
--rw-r--r--   0 runner    (1001) docker     (123)   113499 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manual/configuration.rst
--rw-r--r--   0 runner    (1001) docker     (123)    14016 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manual/extending.rst
--rw-r--r--   0 runner    (1001) docker     (123)      160 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manual/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2702 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manual/introduction.rst
--rw-r--r--   0 runner    (1001) docker     (123)    24650 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/manual/policies.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.838764 BobBuildTool-0.23.0/doc/releases/
--rw-r--r--   0 runner    (1001) docker     (123)     8403 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/0.13.rst
--rw-r--r--   0 runner    (1001) docker     (123)    12628 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/0.14.rst
--rw-r--r--   0 runner    (1001) docker     (123)    14335 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/0.15.rst
--rw-r--r--   0 runner    (1001) docker     (123)    10360 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/0.16.rst
--rw-r--r--   0 runner    (1001) docker     (123)     8909 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/0.17.rst
--rw-r--r--   0 runner    (1001) docker     (123)    10097 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/0.18.rst
--rw-r--r--   0 runner    (1001) docker     (123)     5697 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/0.19.rst
--rw-r--r--   0 runner    (1001) docker     (123)     4171 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/0.20.rst
--rw-r--r--   0 runner    (1001) docker     (123)     4056 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/0.21.rst
--rw-r--r--   0 runner    (1001) docker     (123)     7641 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/0.22.rst
--rw-r--r--   0 runner    (1001) docker     (123)     5571 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/0.23.rst
--rw-r--r--   0 runner    (1001) docker     (123)      155 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/releases/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.838764 BobBuildTool-0.23.0/doc/tutorial/
--rw-r--r--   0 runner    (1001) docker     (123)    14015 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/tutorial/compile.rst
--rw-r--r--   0 runner    (1001) docker     (123)      110 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/tutorial/create.rst
--rw-r--r--   0 runner    (1001) docker     (123)     4509 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/tutorial/fingerprints.rst
--rw-r--r--   0 runner    (1001) docker     (123)      116 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/tutorial/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)    21009 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/doc/tutorial/jenkins.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.830764 BobBuildTool-0.23.0/pym/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.838764 BobBuildTool-0.23.0/pym/BobBuildTool.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2523 2023-07-23 09:41:47.000000 BobBuildTool-0.23.0/pym/BobBuildTool.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3743 2023-07-23 09:41:47.000000 BobBuildTool-0.23.0/pym/BobBuildTool.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 09:41:47.000000 BobBuildTool-0.23.0/pym/BobBuildTool.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       40 2023-07-23 09:41:47.000000 BobBuildTool-0.23.0/pym/BobBuildTool.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 09:41:47.000000 BobBuildTool-0.23.0/pym/BobBuildTool.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       65 2023-07-23 09:41:47.000000 BobBuildTool-0.23.0/pym/BobBuildTool.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        4 2023-07-23 09:41:47.000000 BobBuildTool-0.23.0/pym/BobBuildTool.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.842764 BobBuildTool-0.23.0/pym/bob/
--rw-r--r--   0 runner    (1001) docker     (123)     2425 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    44506 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/archive.py
--rw-r--r--   0 runner    (1001) docker     (123)    12425 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/audit.py
--rw-r--r--   0 runner    (1001) docker     (123)    85560 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/builder.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.842764 BobBuildTool-0.23.0/pym/bob/cmds/
--rw-r--r--   0 runner    (1001) docker     (123)      109 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18385 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/archive.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.842764 BobBuildTool-0.23.0/pym/bob/cmds/build/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/build/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    17812 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/build/build.py
--rw-r--r--   0 runner    (1001) docker     (123)    10130 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/build/clean.py
--rw-r--r--   0 runner    (1001) docker     (123)     5502 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/build/project.py
--rw-r--r--   0 runner    (1001) docker     (123)     6089 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/build/query.py
--rw-r--r--   0 runner    (1001) docker     (123)     6013 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/build/state.py
--rw-r--r--   0 runner    (1001) docker     (123)    12802 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/build/status.py
--rw-r--r--   0 runner    (1001) docker     (123)    18805 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/graph.py
--rw-r--r--   0 runner    (1001) docker     (123)     1248 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/help.py
--rw-r--r--   0 runner    (1001) docker     (123)     3244 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/invoke.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.842764 BobBuildTool-0.23.0/pym/bob/cmds/jenkins/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/jenkins/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9158 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/jenkins/exec.py
--rw-r--r--   0 runner    (1001) docker     (123)     7051 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/jenkins/intermediate.py
--rw-r--r--   0 runner    (1001) docker     (123)    71466 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/jenkins/jenkins.py
--rw-r--r--   0 runner    (1001) docker     (123)    12745 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/misc.py
--rw-r--r--   0 runner    (1001) docker     (123)    11195 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/cmds/show.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.842764 BobBuildTool-0.23.0/pym/bob/develop/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/develop/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2094 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/develop/make.py
--rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/develop/version.py
--rw-r--r--   0 runner    (1001) docker     (123)     1971 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/errors.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.842764 BobBuildTool-0.23.0/pym/bob/generators/
--rw-r--r--   0 runner    (1001) docker     (123)    18796 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/generators/EclipseCdtGenerator.py
--rw-r--r--   0 runner    (1001) docker     (123)    25601 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/generators/QtCreatorGenerator.py
--rw-r--r--   0 runner    (1001) docker     (123)    17143 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/generators/VisualStudio.py
--rw-r--r--   0 runner    (1001) docker     (123)     6296 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/generators/VisualStudioCode.py
--rw-r--r--   0 runner    (1001) docker     (123)      640 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/generators/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    13744 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/generators/common.py
--rw-r--r--   0 runner    (1001) docker     (123)   163100 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/input.py
--rw-r--r--   0 runner    (1001) docker     (123)    20672 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/intermediate.py
--rw-r--r--   0 runner    (1001) docker     (123)    22681 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/invoker.py
--rw-r--r--   0 runner    (1001) docker     (123)    28532 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/languages.py
--rw-r--r--   0 runner    (1001) docker     (123)    35323 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/pathspec.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.842764 BobBuildTool-0.23.0/pym/bob/scm/
--rw-r--r--   0 runner    (1001) docker     (123)     2201 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/scm/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7383 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/scm/cvs.py
--rw-r--r--   0 runner    (1001) docker     (123)    46137 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/scm/git.py
--rw-r--r--   0 runner    (1001) docker     (123)     7205 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/scm/imp.py
--rw-r--r--   0 runner    (1001) docker     (123)    13226 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/scm/scm.py
--rw-r--r--   0 runner    (1001) docker     (123)     7781 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/scm/svn.py
--rw-r--r--   0 runner    (1001) docker     (123)    18112 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/scm/url.py
--rw-r--r--   0 runner    (1001) docker     (123)     9640 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/scripts.py
--rw-r--r--   0 runner    (1001) docker     (123)    12637 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/share.py
--rw-r--r--   0 runner    (1001) docker     (123)    26804 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/state.py
--rw-r--r--   0 runner    (1001) docker     (123)    19736 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/stringparser.py
--rw-r--r--   0 runner    (1001) docker     (123)    20653 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/tty.py
--rw-r--r--   0 runner    (1001) docker     (123)    26836 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/pym/bob/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)      144 2023-07-23 09:41:47.000000 BobBuildTool-0.23.0/pym/bob/version.py
--rw-r--r--   0 runner    (1001) docker     (123)      108 2023-07-23 09:41:47.846764 BobBuildTool-0.23.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     5587 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.830764 BobBuildTool-0.23.0/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:41:47.842764 BobBuildTool-0.23.0/src/namespace-sandbox/
--rw-r--r--   0 runner    (1001) docker     (123)    23824 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/src/namespace-sandbox/namespace-sandbox.c
--rw-r--r--   0 runner    (1001) docker     (123)     1268 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/src/namespace-sandbox/network-tools.c
--rw-r--r--   0 runner    (1001) docker     (123)      791 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/src/namespace-sandbox/network-tools.h
--rw-r--r--   0 runner    (1001) docker     (123)     1742 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/src/namespace-sandbox/process-tools.c
--rw-r--r--   0 runner    (1001) docker     (123)     2432 2023-07-23 09:41:34.000000 BobBuildTool-0.23.0/src/namespace-sandbox/process-tools.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.571699 BobBuildTool-0.23.0rc1/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.551699 BobBuildTool-0.23.0rc1/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.551699 BobBuildTool-0.23.0rc1/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     4953 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/.github/workflows/workflow.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      103 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      125 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/.readthedocs.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)    35498 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       88 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     2526 2023-07-07 20:03:25.571699 BobBuildTool-0.23.0rc1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1750 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/README.md
+-rwxr-xr-x   0 runner    (1001) docker     (123)      345 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/bob
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/bob.cmd
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.551699 BobBuildTool-0.23.0rc1/contrib/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.551699 BobBuildTool-0.23.0rc1/contrib/bash-completion/
+-rw-r--r--   0 runner    (1001) docker     (123)    13471 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/contrib/bash-completion/bob
+-rw-r--r--   0 runner    (1001) docker     (123)     3537 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/contrib/cleanup-recipes.awk
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1480 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/contrib/create-release.sh
+-rwxr-xr-x   0 runner    (1001) docker     (123)      551 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/contrib/notify.sh
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.551699 BobBuildTool-0.23.0rc1/contrib/plugins/
+-rw-r--r--   0 runner    (1001) docker     (123)     3880 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/contrib/plugins/jenkins-cobertura.py
+-rw-r--r--   0 runner    (1001) docker     (123)      886 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/contrib/plugins/override.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2334 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/contrib/plugins/path-fmt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1811 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/contrib/sandbox.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.555699 BobBuildTool-0.23.0rc1/doc/
+-rw-r--r--   0 runner    (1001) docker     (123)    52308 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/BOB_Logo.png
+-rw-r--r--   0 runner    (1001) docker     (123)    51445 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/BOB_Logo.svg
+-rw-r--r--   0 runner    (1001) docker     (123)     6750 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/Makefile
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.555699 BobBuildTool-0.23.0rc1/doc/_build/
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/_build/.gitignore
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.555699 BobBuildTool-0.23.0rc1/doc/_static/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/_static/.gitkeep
+-rw-r--r--   0 runner    (1001) docker     (123)   218324 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/_static/d3.v4.min.js
+-rw-r--r--   0 runner    (1001) docker     (123)    25786 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/_static/sandbox.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.555699 BobBuildTool-0.23.0rc1/doc/_templates/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/_templates/.gitkeep
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.555699 BobBuildTool-0.23.0rc1/doc/cheatsheet/
+-rw-r--r--   0 runner    (1001) docker     (123)    67229 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/cheatsheet/bob_cheatsheet.pdf
+-rw-r--r--   0 runner    (1001) docker     (123)     9819 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/cheatsheet/bob_cheatsheet.tex
+-rw-r--r--   0 runner    (1001) docker     (123)    11668 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1456 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/glossary.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.559699 BobBuildTool-0.23.0rc1/doc/images/
+-rw-r--r--   0 runner    (1001) docker     (123)   129885 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/images/jenkins.odg
+-rw-r--r--   0 runner    (1001) docker     (123)    48173 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/images/jenkins.png
+-rw-r--r--   0 runner    (1001) docker     (123)    10648 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/images/overview.odg
+-rw-r--r--   0 runner    (1001) docker     (123)    17248 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/images/overview.png
+-rw-r--r--   0 runner    (1001) docker     (123)    28093 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/images/recipe-flow.odg
+-rw-r--r--   0 runner    (1001) docker     (123)    80846 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/images/recipe-flow.png
+-rw-r--r--   0 runner    (1001) docker     (123)    47205 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/images/sandbox_graph.png
+-rw-r--r--   0 runner    (1001) docker     (123)    18826 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/images/variant-management.odg
+-rw-r--r--   0 runner    (1001) docker     (123)    19985 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/images/variant-management.png
+-rw-r--r--   0 runner    (1001) docker     (123)     1677 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     7807 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/installation.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.559699 BobBuildTool-0.23.0rc1/doc/manpages/
+-rw-r--r--   0 runner    (1001) docker     (123)     7193 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-archive.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    10832 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-build-dev.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-build.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     3915 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-clean.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     3231 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-dev.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2323 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-graph.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      579 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-init.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    25086 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-jenkins.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     3614 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-ls.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     6393 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-project.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      681 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-query-meta.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1546 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-query-path.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      561 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-query-recipe.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1169 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-query-scm.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     3448 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-show.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     6536 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob-status.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     3595 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bob.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    14703 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/bobpaths.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      298 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      481 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manpages/std-opt-cfg.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.563699 BobBuildTool-0.23.0rc1/doc/manual/
+-rw-r--r--   0 runner    (1001) docker     (123)     9298 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manual/audit-trail.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    14381 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manual/concepts.rst
+-rw-r--r--   0 runner    (1001) docker     (123)   113499 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manual/configuration.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    14016 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manual/extending.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manual/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2702 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manual/introduction.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    24650 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/manual/policies.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.563699 BobBuildTool-0.23.0rc1/doc/releases/
+-rw-r--r--   0 runner    (1001) docker     (123)     8403 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/0.13.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    12628 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/0.14.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    14335 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/0.15.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    10360 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/0.16.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     8909 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/0.17.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    10097 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/0.18.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     5697 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/0.19.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     4171 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/0.20.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     4056 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/0.21.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     7641 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/0.22.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     5571 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/0.23.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      155 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/releases/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.563699 BobBuildTool-0.23.0rc1/doc/tutorial/
+-rw-r--r--   0 runner    (1001) docker     (123)    14015 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/tutorial/compile.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      110 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/tutorial/create.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     4509 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/tutorial/fingerprints.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      116 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/tutorial/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    21009 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/doc/tutorial/jenkins.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.551699 BobBuildTool-0.23.0rc1/pym/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.563699 BobBuildTool-0.23.0rc1/pym/BobBuildTool.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2526 2023-07-07 20:03:25.000000 BobBuildTool-0.23.0rc1/pym/BobBuildTool.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3743 2023-07-07 20:03:25.000000 BobBuildTool-0.23.0rc1/pym/BobBuildTool.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-07 20:03:25.000000 BobBuildTool-0.23.0rc1/pym/BobBuildTool.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       40 2023-07-07 20:03:25.000000 BobBuildTool-0.23.0rc1/pym/BobBuildTool.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-07 20:03:25.000000 BobBuildTool-0.23.0rc1/pym/BobBuildTool.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       65 2023-07-07 20:03:25.000000 BobBuildTool-0.23.0rc1/pym/BobBuildTool.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        4 2023-07-07 20:03:25.000000 BobBuildTool-0.23.0rc1/pym/BobBuildTool.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.567699 BobBuildTool-0.23.0rc1/pym/bob/
+-rw-r--r--   0 runner    (1001) docker     (123)     2425 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    44506 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/archive.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12425 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/audit.py
+-rw-r--r--   0 runner    (1001) docker     (123)    85560 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/builder.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.567699 BobBuildTool-0.23.0rc1/pym/bob/cmds/
+-rw-r--r--   0 runner    (1001) docker     (123)      109 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18385 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/archive.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.567699 BobBuildTool-0.23.0rc1/pym/bob/cmds/build/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/build/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17812 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/build/build.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10130 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/build/clean.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5502 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/build/project.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6089 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/build/query.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6013 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/build/state.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12802 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/build/status.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18805 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/graph.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1248 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/help.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3244 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/invoke.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.571699 BobBuildTool-0.23.0rc1/pym/bob/cmds/jenkins/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/jenkins/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9158 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/jenkins/exec.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7051 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/jenkins/intermediate.py
+-rw-r--r--   0 runner    (1001) docker     (123)    71466 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/jenkins/jenkins.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12745 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/misc.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11195 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/cmds/show.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.571699 BobBuildTool-0.23.0rc1/pym/bob/develop/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/develop/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2094 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/develop/make.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/develop/version.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1971 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/errors.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.571699 BobBuildTool-0.23.0rc1/pym/bob/generators/
+-rw-r--r--   0 runner    (1001) docker     (123)    18796 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/generators/EclipseCdtGenerator.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25601 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/generators/QtCreatorGenerator.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17143 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/generators/VisualStudio.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6296 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/generators/VisualStudioCode.py
+-rw-r--r--   0 runner    (1001) docker     (123)      640 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/generators/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13744 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/generators/common.py
+-rw-r--r--   0 runner    (1001) docker     (123)   163100 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/input.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20672 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/intermediate.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22681 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/invoker.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28532 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/languages.py
+-rw-r--r--   0 runner    (1001) docker     (123)    35323 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/pathspec.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.571699 BobBuildTool-0.23.0rc1/pym/bob/scm/
+-rw-r--r--   0 runner    (1001) docker     (123)     2201 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/scm/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7383 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/scm/cvs.py
+-rw-r--r--   0 runner    (1001) docker     (123)    46137 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/scm/git.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7205 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/scm/imp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13226 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/scm/scm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7781 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/scm/svn.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18112 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/scm/url.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9640 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/scripts.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12637 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/share.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26804 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/state.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19736 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/stringparser.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20653 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/tty.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26836 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/pym/bob/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)      147 2023-07-07 20:03:25.000000 BobBuildTool-0.23.0rc1/pym/bob/version.py
+-rw-r--r--   0 runner    (1001) docker     (123)      108 2023-07-07 20:03:25.571699 BobBuildTool-0.23.0rc1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     5587 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.551699 BobBuildTool-0.23.0rc1/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 20:03:25.571699 BobBuildTool-0.23.0rc1/src/namespace-sandbox/
+-rw-r--r--   0 runner    (1001) docker     (123)    23824 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/src/namespace-sandbox/namespace-sandbox.c
+-rw-r--r--   0 runner    (1001) docker     (123)     1268 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/src/namespace-sandbox/network-tools.c
+-rw-r--r--   0 runner    (1001) docker     (123)      791 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/src/namespace-sandbox/network-tools.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1742 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/src/namespace-sandbox/process-tools.c
+-rw-r--r--   0 runner    (1001) docker     (123)     2432 2023-07-07 20:03:11.000000 BobBuildTool-0.23.0rc1/src/namespace-sandbox/process-tools.h
```

### Comparing `BobBuildTool-0.23.0/.github/workflows/workflow.yaml` & `BobBuildTool-0.23.0rc1/.github/workflows/workflow.yaml`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/LICENSE` & `BobBuildTool-0.23.0rc1/LICENSE`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/PKG-INFO` & `BobBuildTool-0.23.0rc1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BobBuildTool
-Version: 0.23.0
+Version: 0.23.0rc1
 Summary: Functional cross platform build-automation tool
 Home-page: https://bobbuildtool.github.io/
 Download-URL: https://github.com/BobBuildTool/bob/releases
 Author: Jan Klötzke
 Author-email: jan@kloetzke.net
 License: GPLv3+
 Keywords: bob build-automation build-system
```

### Comparing `BobBuildTool-0.23.0/README.md` & `BobBuildTool-0.23.0rc1/README.md`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/contrib/bash-completion/bob` & `BobBuildTool-0.23.0rc1/contrib/bash-completion/bob`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/contrib/cleanup-recipes.awk` & `BobBuildTool-0.23.0rc1/contrib/cleanup-recipes.awk`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/contrib/create-release.sh` & `BobBuildTool-0.23.0rc1/contrib/create-release.sh`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/contrib/notify.sh` & `BobBuildTool-0.23.0rc1/contrib/notify.sh`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/contrib/plugins/jenkins-cobertura.py` & `BobBuildTool-0.23.0rc1/contrib/plugins/jenkins-cobertura.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/contrib/plugins/override.py` & `BobBuildTool-0.23.0rc1/contrib/plugins/override.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/contrib/plugins/path-fmt.py` & `BobBuildTool-0.23.0rc1/contrib/plugins/path-fmt.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/contrib/sandbox.rst` & `BobBuildTool-0.23.0rc1/contrib/sandbox.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/BOB_Logo.png` & `BobBuildTool-0.23.0rc1/doc/BOB_Logo.png`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/BOB_Logo.svg` & `BobBuildTool-0.23.0rc1/doc/BOB_Logo.svg`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/Makefile` & `BobBuildTool-0.23.0rc1/doc/Makefile`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/_static/d3.v4.min.js` & `BobBuildTool-0.23.0rc1/doc/_static/d3.v4.min.js`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/_static/sandbox.html` & `BobBuildTool-0.23.0rc1/doc/_static/sandbox.html`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/cheatsheet/bob_cheatsheet.pdf` & `BobBuildTool-0.23.0rc1/doc/cheatsheet/bob_cheatsheet.pdf`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/cheatsheet/bob_cheatsheet.tex` & `BobBuildTool-0.23.0rc1/doc/cheatsheet/bob_cheatsheet.tex`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/conf.py` & `BobBuildTool-0.23.0rc1/doc/conf.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/glossary.rst` & `BobBuildTool-0.23.0rc1/doc/glossary.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/images/jenkins.odg` & `BobBuildTool-0.23.0rc1/doc/images/jenkins.odg`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/images/jenkins.png` & `BobBuildTool-0.23.0rc1/doc/images/jenkins.png`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/images/overview.odg` & `BobBuildTool-0.23.0rc1/doc/images/overview.odg`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/images/overview.png` & `BobBuildTool-0.23.0rc1/doc/images/overview.png`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/images/recipe-flow.odg` & `BobBuildTool-0.23.0rc1/doc/images/recipe-flow.odg`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/images/recipe-flow.png` & `BobBuildTool-0.23.0rc1/doc/images/recipe-flow.png`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/images/sandbox_graph.png` & `BobBuildTool-0.23.0rc1/doc/images/sandbox_graph.png`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/images/variant-management.odg` & `BobBuildTool-0.23.0rc1/doc/images/variant-management.odg`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/images/variant-management.png` & `BobBuildTool-0.23.0rc1/doc/images/variant-management.png`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/index.rst` & `BobBuildTool-0.23.0rc1/doc/index.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/installation.rst` & `BobBuildTool-0.23.0rc1/doc/installation.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-archive.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-archive.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-build-dev.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-build-dev.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-build.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-build.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-clean.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-clean.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-dev.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-dev.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-graph.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-graph.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-init.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-init.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-jenkins.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-jenkins.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-ls.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-ls.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-project.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-project.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-query-meta.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-query-meta.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-query-path.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-query-path.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-query-recipe.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-query-recipe.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-query-scm.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-query-scm.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-show.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-show.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob-status.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob-status.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bob.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bob.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manpages/bobpaths.rst` & `BobBuildTool-0.23.0rc1/doc/manpages/bobpaths.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manual/audit-trail.rst` & `BobBuildTool-0.23.0rc1/doc/manual/audit-trail.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manual/concepts.rst` & `BobBuildTool-0.23.0rc1/doc/manual/concepts.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manual/configuration.rst` & `BobBuildTool-0.23.0rc1/doc/manual/configuration.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manual/extending.rst` & `BobBuildTool-0.23.0rc1/doc/manual/extending.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manual/introduction.rst` & `BobBuildTool-0.23.0rc1/doc/manual/introduction.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/manual/policies.rst` & `BobBuildTool-0.23.0rc1/doc/manual/policies.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/releases/0.13.rst` & `BobBuildTool-0.23.0rc1/doc/releases/0.13.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/releases/0.14.rst` & `BobBuildTool-0.23.0rc1/doc/releases/0.14.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/releases/0.15.rst` & `BobBuildTool-0.23.0rc1/doc/releases/0.15.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/releases/0.16.rst` & `BobBuildTool-0.23.0rc1/doc/releases/0.16.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/releases/0.17.rst` & `BobBuildTool-0.23.0rc1/doc/releases/0.17.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/releases/0.18.rst` & `BobBuildTool-0.23.0rc1/doc/releases/0.18.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/releases/0.19.rst` & `BobBuildTool-0.23.0rc1/doc/releases/0.19.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/releases/0.20.rst` & `BobBuildTool-0.23.0rc1/doc/releases/0.20.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/releases/0.21.rst` & `BobBuildTool-0.23.0rc1/doc/releases/0.21.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/releases/0.22.rst` & `BobBuildTool-0.23.0rc1/doc/releases/0.22.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/releases/0.23.rst` & `BobBuildTool-0.23.0rc1/doc/releases/0.23.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/tutorial/compile.rst` & `BobBuildTool-0.23.0rc1/doc/tutorial/compile.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/tutorial/fingerprints.rst` & `BobBuildTool-0.23.0rc1/doc/tutorial/fingerprints.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/doc/tutorial/jenkins.rst` & `BobBuildTool-0.23.0rc1/doc/tutorial/jenkins.rst`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/BobBuildTool.egg-info/PKG-INFO` & `BobBuildTool-0.23.0rc1/pym/BobBuildTool.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: BobBuildTool
-Version: 0.23.0
+Version: 0.23.0rc1
 Summary: Functional cross platform build-automation tool
 Home-page: https://bobbuildtool.github.io/
 Download-URL: https://github.com/BobBuildTool/bob/releases
 Author: Jan Klötzke
 Author-email: jan@kloetzke.net
 License: GPLv3+
 Keywords: bob build-automation build-system
```

### Comparing `BobBuildTool-0.23.0/pym/BobBuildTool.egg-info/SOURCES.txt` & `BobBuildTool-0.23.0rc1/pym/BobBuildTool.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/__init__.py` & `BobBuildTool-0.23.0rc1/pym/bob/__init__.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/archive.py` & `BobBuildTool-0.23.0rc1/pym/bob/archive.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/audit.py` & `BobBuildTool-0.23.0rc1/pym/bob/audit.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/builder.py` & `BobBuildTool-0.23.0rc1/pym/bob/builder.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/archive.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/archive.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/build/build.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/build/build.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/build/clean.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/build/clean.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/build/project.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/build/project.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/build/query.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/build/query.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/build/state.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/build/state.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/build/status.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/build/status.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/graph.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/graph.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/help.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/help.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/invoke.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/invoke.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/jenkins/exec.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/jenkins/exec.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/jenkins/intermediate.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/jenkins/intermediate.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/jenkins/jenkins.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/jenkins/jenkins.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/misc.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/misc.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/cmds/show.py` & `BobBuildTool-0.23.0rc1/pym/bob/cmds/show.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/develop/make.py` & `BobBuildTool-0.23.0rc1/pym/bob/develop/make.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/develop/version.py` & `BobBuildTool-0.23.0rc1/pym/bob/develop/version.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/errors.py` & `BobBuildTool-0.23.0rc1/pym/bob/errors.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/generators/EclipseCdtGenerator.py` & `BobBuildTool-0.23.0rc1/pym/bob/generators/EclipseCdtGenerator.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/generators/QtCreatorGenerator.py` & `BobBuildTool-0.23.0rc1/pym/bob/generators/QtCreatorGenerator.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/generators/VisualStudio.py` & `BobBuildTool-0.23.0rc1/pym/bob/generators/VisualStudio.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/generators/VisualStudioCode.py` & `BobBuildTool-0.23.0rc1/pym/bob/generators/VisualStudioCode.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/generators/__init__.py` & `BobBuildTool-0.23.0rc1/pym/bob/generators/__init__.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/generators/common.py` & `BobBuildTool-0.23.0rc1/pym/bob/generators/common.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/input.py` & `BobBuildTool-0.23.0rc1/pym/bob/input.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/intermediate.py` & `BobBuildTool-0.23.0rc1/pym/bob/intermediate.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/invoker.py` & `BobBuildTool-0.23.0rc1/pym/bob/invoker.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/languages.py` & `BobBuildTool-0.23.0rc1/pym/bob/languages.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/pathspec.py` & `BobBuildTool-0.23.0rc1/pym/bob/pathspec.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/scm/__init__.py` & `BobBuildTool-0.23.0rc1/pym/bob/scm/__init__.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/scm/cvs.py` & `BobBuildTool-0.23.0rc1/pym/bob/scm/cvs.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/scm/git.py` & `BobBuildTool-0.23.0rc1/pym/bob/scm/git.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/scm/imp.py` & `BobBuildTool-0.23.0rc1/pym/bob/scm/imp.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/scm/scm.py` & `BobBuildTool-0.23.0rc1/pym/bob/scm/scm.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/scm/svn.py` & `BobBuildTool-0.23.0rc1/pym/bob/scm/svn.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/scm/url.py` & `BobBuildTool-0.23.0rc1/pym/bob/scm/url.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/scripts.py` & `BobBuildTool-0.23.0rc1/pym/bob/scripts.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/share.py` & `BobBuildTool-0.23.0rc1/pym/bob/share.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/state.py` & `BobBuildTool-0.23.0rc1/pym/bob/state.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/stringparser.py` & `BobBuildTool-0.23.0rc1/pym/bob/stringparser.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/tty.py` & `BobBuildTool-0.23.0rc1/pym/bob/tty.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/pym/bob/utils.py` & `BobBuildTool-0.23.0rc1/pym/bob/utils.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/setup.py` & `BobBuildTool-0.23.0rc1/setup.py`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/src/namespace-sandbox/namespace-sandbox.c` & `BobBuildTool-0.23.0rc1/src/namespace-sandbox/namespace-sandbox.c`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/src/namespace-sandbox/network-tools.c` & `BobBuildTool-0.23.0rc1/src/namespace-sandbox/network-tools.c`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/src/namespace-sandbox/network-tools.h` & `BobBuildTool-0.23.0rc1/src/namespace-sandbox/network-tools.h`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/src/namespace-sandbox/process-tools.c` & `BobBuildTool-0.23.0rc1/src/namespace-sandbox/process-tools.c`

 * *Files identical despite different names*

### Comparing `BobBuildTool-0.23.0/src/namespace-sandbox/process-tools.h` & `BobBuildTool-0.23.0rc1/src/namespace-sandbox/process-tools.h`

 * *Files identical despite different names*

