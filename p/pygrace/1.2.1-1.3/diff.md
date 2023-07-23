# Comparing `tmp/pygrace-1.2.1.tar.gz` & `tmp/pygrace-1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pygrace-1.2.1.tar", last modified: Sat Jan 14 23:20:56 2023, max compression
+gzip compressed data, was "pygrace-1.3.tar", last modified: Sun Jul 23 19:56:41 2023, max compression
```

## Comparing `pygrace-1.2.1.tar` & `pygrace-1.3.tar`

### file list

```diff
@@ -1,123 +1,125 @@
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.848237 pygrace-1.2.1/
--rw-r--r--   0 mmckerns   (501) staff       (20)      833 2023-01-14 00:16:34.000000 pygrace-1.2.1/.codecov.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1282 2023-01-14 00:16:34.000000 pygrace-1.2.1/.coveragerc
--rw-r--r--   0 mmckerns   (501) staff       (20)       35 2023-01-14 00:16:34.000000 pygrace-1.2.1/.gitignore
--rw-r--r--   0 mmckerns   (501) staff       (20)      285 2023-01-14 00:16:34.000000 pygrace-1.2.1/.readthedocs.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1721 2023-01-14 19:28:09.000000 pygrace-1.2.1/.travis.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1821 2023-01-14 00:16:12.000000 pygrace-1.2.1/LICENSE
--rw-r--r--   0 mmckerns   (501) staff       (20)      242 2023-01-14 00:16:12.000000 pygrace-1.2.1/MANIFEST.in
--rw-r--r--   0 mmckerns   (501) staff       (20)     9724 2023-01-14 23:20:56.848625 pygrace-1.2.1/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     8935 2023-01-14 23:19:49.000000 pygrace-1.2.1/README.md
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.689707 pygrace-1.2.1/docs/
--rw-r--r--   0 mmckerns   (501) staff       (20)      671 2023-01-14 00:17:21.000000 pygrace-1.2.1/docs/Makefile
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.702582 pygrace-1.2.1/docs/diagrams/
--rw-r--r--   0 mmckerns   (501) staff       (20)    55624 2023-01-14 13:12:41.000000 pygrace-1.2.1/docs/diagrams/cheatsheet.pdf
--rw-r--r--   0 mmckerns   (501) staff       (20)    60235 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/diagrams/crow_diagram.pdf
--rw-r--r--   0 mmckerns   (501) staff       (20)    39358 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/diagrams/crow_diagram.svg
--rw-r--r--   0 mmckerns   (501) staff       (20)   121545 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/diagrams/diagram.big.graph
--rw-r--r--   0 mmckerns   (501) staff       (20)   123372 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/diagrams/diagram.graph
--rw-r--r--   0 mmckerns   (501) staff       (20)    47673 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/diagrams/diagram.pdf
--rw-r--r--   0 mmckerns   (501) staff       (20)      430 2023-01-14 00:17:21.000000 pygrace-1.2.1/docs/requirements.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.735509 pygrace-1.2.1/docs/source/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.745000 pygrace-1.2.1/docs/source/_static/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5618 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/source/_static/00_helloworld.png
--rw-r--r--   0 mmckerns   (501) staff       (20)    11570 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/source/_static/05_colorplot.png
--rw-r--r--   0 mmckerns   (501) staff       (20)    16494 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/source/_static/08_latexlabels.png
--rw-r--r--   0 mmckerns   (501) staff       (20)     4442 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/source/_static/cos.png
--rw-r--r--   0 mmckerns   (501) staff       (20)    50265 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/source/_static/crow_diagram.png
--rw-r--r--   0 mmckerns   (501) staff       (20)     4624 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/source/_static/histoPlot.png
--rw-r--r--   0 mmckerns   (501) staff       (20)     4448 2023-01-14 00:15:34.000000 pygrace-1.2.1/docs/source/_static/sin.png
--rw-r--r--   0 mmckerns   (501) staff       (20)      338 2023-01-14 00:17:48.000000 pygrace-1.2.1/docs/source/colorbrewer.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)     7472 2023-01-14 00:17:48.000000 pygrace-1.2.1/docs/source/conf.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1870 2023-01-14 00:17:48.000000 pygrace-1.2.1/docs/source/extensions.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      352 2023-01-14 00:17:48.000000 pygrace-1.2.1/docs/source/index.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      749 2023-01-14 00:17:48.000000 pygrace-1.2.1/docs/source/interactive.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)    11570 2023-01-14 00:17:48.000000 pygrace-1.2.1/docs/source/pygrace.png
--rw-r--r--   0 mmckerns   (501) staff       (20)     2794 2023-01-14 00:17:48.000000 pygrace-1.2.1/docs/source/pygrace.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      144 2023-01-14 00:17:48.000000 pygrace-1.2.1/docs/source/scripts.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)     1008 2023-01-14 00:17:48.000000 pygrace-1.2.1/docs/source/styles.rst
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.763328 pygrace-1.2.1/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)      849 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/00_helloworld.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      968 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/01_singleplot.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3753 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/02_multiplot.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1677 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/03_simplesubclass.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1447 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/04_classy.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3173 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/05_colorplot.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2074 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/06_logautoscale.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2449 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/07_panels.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2444 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/08_latexlabels.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2846 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/09_datasets.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3443 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/10_dataset_features.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1558 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/11_network.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      882 2023-01-14 13:11:18.000000 pygrace-1.2.1/examples/12_cheatsheet.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4828 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/13_directed_network.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1210 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/14_phylogenetic_tree.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      358 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1083 2023-01-14 17:17:28.000000 pygrace-1.2.1/examples/clean_examples.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2023-01-14 00:18:22.000000 pygrace-1.2.1/examples/example_tools.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.773054 pygrace-1.2.1/examples/interactive/
--rw-r--r--   0 mmckerns   (501) staff       (20)     2284 2023-01-14 00:19:19.000000 pygrace-1.2.1/examples/interactive/grace.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      686 2023-01-14 00:19:19.000000 pygrace-1.2.1/examples/interactive/grace_prompt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1480 2023-01-14 00:19:19.000000 pygrace-1.2.1/examples/interactive/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      902 2023-01-14 00:19:19.000000 pygrace-1.2.1/examples/interactive/project.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      586 2023-01-14 00:19:19.000000 pygrace-1.2.1/examples/interactive/prompt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3090 2023-01-14 17:37:10.000000 pygrace-1.2.1/examples/test_examples.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.813973 pygrace-1.2.1/pygrace/
--rw-r--r--   0 mmckerns   (501) staff       (20)    10541 2023-01-14 23:20:56.000000 pygrace-1.2.1/pygrace/__info__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2140 2023-01-14 06:02:51.000000 pygrace-1.2.1/pygrace/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    16263 2023-01-14 00:20:15.000000 pygrace-1.2.1/pygrace/axis.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    25742 2023-01-14 00:20:15.000000 pygrace-1.2.1/pygrace/base.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7751 2023-01-14 00:20:15.000000 pygrace-1.2.1/pygrace/colors.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    15661 2023-01-14 00:20:15.000000 pygrace-1.2.1/pygrace/dataset.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    12243 2023-01-14 00:20:15.000000 pygrace-1.2.1/pygrace/drawing_objects.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.826970 pygrace-1.2.1/pygrace/extensions/
--rw-r--r--   0 mmckerns   (501) staff       (20)      358 2023-01-14 00:20:29.000000 pygrace-1.2.1/pygrace/extensions/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    15165 2023-01-14 00:20:29.000000 pygrace-1.2.1/pygrace/extensions/colorbar.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2580 2023-01-14 00:20:29.000000 pygrace-1.2.1/pygrace/extensions/distribution.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2988 2023-01-14 00:20:29.000000 pygrace-1.2.1/pygrace/extensions/latex_string.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      462 2023-01-14 00:20:29.000000 pygrace-1.2.1/pygrace/extensions/multi_grace.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    20989 2023-01-14 00:20:29.000000 pygrace-1.2.1/pygrace/extensions/multi_plot.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    24816 2023-01-14 00:20:29.000000 pygrace-1.2.1/pygrace/extensions/network.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11356 2023-01-14 00:20:29.000000 pygrace-1.2.1/pygrace/extensions/panel.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2361 2023-01-14 00:20:29.000000 pygrace-1.2.1/pygrace/extensions/table.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7228 2023-01-14 00:20:29.000000 pygrace-1.2.1/pygrace/extensions/tree.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1514 2023-01-14 00:20:15.000000 pygrace-1.2.1/pygrace/fonts.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      520 2023-01-14 00:20:15.000000 pygrace-1.2.1/pygrace/grace.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    29419 2023-01-14 00:20:15.000000 pygrace-1.2.1/pygrace/graph.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.834860 pygrace-1.2.1/pygrace/interactive/
--rw-r--r--   0 mmckerns   (501) staff       (20)      735 2023-01-14 00:20:48.000000 pygrace-1.2.1/pygrace/interactive/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8959 2023-01-14 00:20:48.000000 pygrace-1.2.1/pygrace/interactive/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    20421 2023-01-14 00:20:48.000000 pygrace-1.2.1/pygrace/interactive/project.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    13475 2023-01-14 00:20:48.000000 pygrace-1.2.1/pygrace/interactive/session.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2610 2023-01-14 00:20:15.000000 pygrace-1.2.1/pygrace/parser.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      431 2023-01-14 00:20:15.000000 pygrace-1.2.1/pygrace/plot.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    13729 2023-01-14 00:20:15.000000 pygrace-1.2.1/pygrace/project.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.838349 pygrace-1.2.1/pygrace/styles/
--rw-r--r--   0 mmckerns   (501) staff       (20)      358 2023-01-14 00:21:22.000000 pygrace-1.2.1/pygrace/styles/__init__.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.841961 pygrace-1.2.1/pygrace/styles/colorbrewer/
--rw-r--r--   0 mmckerns   (501) staff       (20)      358 2023-01-14 00:21:39.000000 pygrace-1.2.1/pygrace/styles/colorbrewer/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    39028 2023-01-14 00:15:34.000000 pygrace-1.2.1/pygrace/styles/colorbrewer/colorbrewer.dat
--rw-r--r--   0 mmckerns   (501) staff       (20)    12720 2023-01-14 00:21:39.000000 pygrace-1.2.1/pygrace/styles/colorbrewer/colorbrewer.py
--rw-r--r--   0 mmckerns   (501) staff       (20)   143700 2023-01-14 00:15:34.000000 pygrace-1.2.1/pygrace/styles/colorbrewer/colorbrewer_swatches.pdf
--rw-r--r--   0 mmckerns   (501) staff       (20)     8042 2023-01-14 00:21:22.000000 pygrace-1.2.1/pygrace/styles/el.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2421 2023-01-14 00:21:22.000000 pygrace-1.2.1/pygrace/styles/journals.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8287 2023-01-14 00:21:22.000000 pygrace-1.2.1/pygrace/styles/metra.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.846457 pygrace-1.2.1/pygrace/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)      569 2023-01-14 00:21:06.000000 pygrace-1.2.1/pygrace/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      904 2023-01-14 00:21:06.000000 pygrace-1.2.1/pygrace/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    14704 2023-01-14 18:41:06.000000 pygrace-1.2.1/pygrace/tests/test_interactive.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      796 2023-01-14 18:01:52.000000 pygrace-1.2.1/pygrace/tests/test_templates.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.817960 pygrace-1.2.1/pygrace.egg-info/
--rw-r--r--   0 mmckerns   (501) staff       (20)     9724 2023-01-14 23:20:56.000000 pygrace-1.2.1/pygrace.egg-info/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     2758 2023-01-14 23:20:56.000000 pygrace-1.2.1/pygrace.egg-info/SOURCES.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-01-14 23:20:56.000000 pygrace-1.2.1/pygrace.egg-info/dependency_links.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-01-14 23:20:56.000000 pygrace-1.2.1/pygrace.egg-info/not-zip-safe
--rw-r--r--   0 mmckerns   (501) staff       (20)       24 2023-01-14 23:20:56.000000 pygrace-1.2.1/pygrace.egg-info/requires.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        8 2023-01-14 23:20:56.000000 pygrace-1.2.1/pygrace.egg-info/top_level.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)      308 2023-01-14 00:16:12.000000 pygrace-1.2.1/pyproject.toml
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-01-14 23:20:56.847392 pygrace-1.2.1/scripts/
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2532 2023-01-14 00:19:43.000000 pygrace-1.2.1/scripts/pygrace_cdf
--rw-r--r--   0 mmckerns   (501) staff       (20)       62 2023-01-14 23:20:56.850806 pygrace-1.2.1/setup.cfg
--rw-r--r--   0 mmckerns   (501) staff       (20)     5155 2023-01-14 00:16:12.000000 pygrace-1.2.1/setup.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      622 2023-01-14 00:16:12.000000 pygrace-1.2.1/tox.ini
--rw-r--r--   0 mmckerns   (501) staff       (20)     3167 2023-01-14 23:18:58.000000 pygrace-1.2.1/version.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.430112 pygrace-1.3/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      833 2023-01-14 00:16:34.000000 pygrace-1.3/.codecov.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1282 2023-01-14 00:16:34.000000 pygrace-1.3/.coveragerc
+-rw-r--r--   0 mmckerns   (501) staff       (20)       35 2023-01-14 00:16:34.000000 pygrace-1.3/.gitignore
+-rw-r--r--   0 mmckerns   (501) staff       (20)      285 2023-01-14 00:16:34.000000 pygrace-1.3/.readthedocs.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1740 2023-07-07 03:28:37.000000 pygrace-1.3/.travis.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1821 2023-02-08 18:06:21.000000 pygrace-1.3/LICENSE
+-rw-r--r--   0 mmckerns   (501) staff       (20)      242 2023-01-14 00:16:12.000000 pygrace-1.3/MANIFEST.in
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9771 2023-07-23 19:56:41.430448 pygrace-1.3/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9150 2023-03-10 04:04:09.000000 pygrace-1.3/README.md
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.265977 pygrace-1.3/docs/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      671 2023-01-14 00:17:21.000000 pygrace-1.3/docs/Makefile
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.279116 pygrace-1.3/docs/diagrams/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    55624 2023-01-14 13:12:41.000000 pygrace-1.3/docs/diagrams/cheatsheet.pdf
+-rw-r--r--   0 mmckerns   (501) staff       (20)    60235 2023-01-14 00:15:34.000000 pygrace-1.3/docs/diagrams/crow_diagram.pdf
+-rw-r--r--   0 mmckerns   (501) staff       (20)    39358 2023-01-14 00:15:34.000000 pygrace-1.3/docs/diagrams/crow_diagram.svg
+-rw-r--r--   0 mmckerns   (501) staff       (20)   121545 2023-01-14 00:15:34.000000 pygrace-1.3/docs/diagrams/diagram.big.graph
+-rw-r--r--   0 mmckerns   (501) staff       (20)   123372 2023-01-14 00:15:34.000000 pygrace-1.3/docs/diagrams/diagram.graph
+-rw-r--r--   0 mmckerns   (501) staff       (20)    47673 2023-01-14 00:15:34.000000 pygrace-1.3/docs/diagrams/diagram.pdf
+-rw-r--r--   0 mmckerns   (501) staff       (20)      430 2023-07-22 01:41:01.000000 pygrace-1.3/docs/requirements.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.292541 pygrace-1.3/docs/source/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.321468 pygrace-1.3/docs/source/_static/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5618 2023-01-14 00:15:34.000000 pygrace-1.3/docs/source/_static/00_helloworld.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11570 2023-01-14 00:15:34.000000 pygrace-1.3/docs/source/_static/05_colorplot.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)    16494 2023-01-14 00:15:34.000000 pygrace-1.3/docs/source/_static/08_latexlabels.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4442 2023-01-14 00:15:34.000000 pygrace-1.3/docs/source/_static/cos.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)    50265 2023-01-14 00:15:34.000000 pygrace-1.3/docs/source/_static/crow_diagram.png
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.324191 pygrace-1.3/docs/source/_static/css/
+-rw-r--r--   0 mmckerns   (501) staff       (20)       85 2023-07-05 04:41:26.000000 pygrace-1.3/docs/source/_static/css/custom.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4624 2023-01-14 00:15:34.000000 pygrace-1.3/docs/source/_static/histoPlot.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4448 2023-01-14 00:15:34.000000 pygrace-1.3/docs/source/_static/sin.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)      215 2023-02-05 00:20:50.000000 pygrace-1.3/docs/source/colorbrewer.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8061 2023-07-05 04:59:03.000000 pygrace-1.3/docs/source/conf.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      893 2023-02-05 00:14:42.000000 pygrace-1.3/docs/source/extensions.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      317 2023-07-05 05:54:37.000000 pygrace-1.3/docs/source/index.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      382 2023-02-05 00:15:36.000000 pygrace-1.3/docs/source/interactive.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11570 2023-01-14 00:17:48.000000 pygrace-1.3/docs/source/pygrace.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1310 2023-07-05 06:06:45.000000 pygrace-1.3/docs/source/pygrace.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      153 2023-02-05 00:19:23.000000 pygrace-1.3/docs/source/scripts.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      512 2023-07-05 06:06:35.000000 pygrace-1.3/docs/source/styles.rst
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.359841 pygrace-1.3/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      849 2023-01-14 00:18:22.000000 pygrace-1.3/examples/00_helloworld.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      968 2023-01-14 00:18:22.000000 pygrace-1.3/examples/01_singleplot.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3753 2023-01-14 00:18:22.000000 pygrace-1.3/examples/02_multiplot.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1677 2023-01-14 00:18:22.000000 pygrace-1.3/examples/03_simplesubclass.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1447 2023-01-14 00:18:22.000000 pygrace-1.3/examples/04_classy.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3173 2023-01-14 00:18:22.000000 pygrace-1.3/examples/05_colorplot.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2074 2023-01-14 00:18:22.000000 pygrace-1.3/examples/06_logautoscale.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2449 2023-01-14 00:18:22.000000 pygrace-1.3/examples/07_panels.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2444 2023-01-14 00:18:22.000000 pygrace-1.3/examples/08_latexlabels.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2846 2023-01-14 00:18:22.000000 pygrace-1.3/examples/09_datasets.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3443 2023-01-14 00:18:22.000000 pygrace-1.3/examples/10_dataset_features.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1558 2023-01-14 00:18:22.000000 pygrace-1.3/examples/11_network.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      882 2023-01-14 13:11:18.000000 pygrace-1.3/examples/12_cheatsheet.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4828 2023-01-14 00:18:22.000000 pygrace-1.3/examples/13_directed_network.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1210 2023-01-14 00:18:22.000000 pygrace-1.3/examples/14_phylogenetic_tree.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      358 2023-01-14 00:18:22.000000 pygrace-1.3/examples/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1083 2023-01-14 17:17:28.000000 pygrace-1.3/examples/clean_examples.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2023-01-14 00:18:22.000000 pygrace-1.3/examples/example_tools.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.365235 pygrace-1.3/examples/interactive/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2284 2023-01-14 00:19:19.000000 pygrace-1.3/examples/interactive/grace.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      686 2023-01-14 00:19:19.000000 pygrace-1.3/examples/interactive/grace_prompt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1480 2023-01-14 00:19:19.000000 pygrace-1.3/examples/interactive/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      902 2023-01-14 00:19:19.000000 pygrace-1.3/examples/interactive/project.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      586 2023-01-14 00:19:19.000000 pygrace-1.3/examples/interactive/prompt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3090 2023-01-14 17:37:10.000000 pygrace-1.3/examples/test_examples.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.383144 pygrace-1.3/pygrace/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10615 2023-07-23 19:56:41.000000 pygrace-1.3/pygrace/__info__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2140 2023-01-14 06:02:51.000000 pygrace-1.3/pygrace/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    16263 2023-01-14 00:20:15.000000 pygrace-1.3/pygrace/axis.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    25742 2023-01-14 00:20:15.000000 pygrace-1.3/pygrace/base.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7751 2023-01-14 00:20:15.000000 pygrace-1.3/pygrace/colors.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15661 2023-01-14 00:20:15.000000 pygrace-1.3/pygrace/dataset.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12243 2023-01-14 00:20:15.000000 pygrace-1.3/pygrace/drawing_objects.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.407147 pygrace-1.3/pygrace/extensions/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      358 2023-01-14 00:20:29.000000 pygrace-1.3/pygrace/extensions/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15165 2023-01-14 00:20:29.000000 pygrace-1.3/pygrace/extensions/colorbar.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2580 2023-01-14 00:20:29.000000 pygrace-1.3/pygrace/extensions/distribution.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2988 2023-01-14 00:20:29.000000 pygrace-1.3/pygrace/extensions/latex_string.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      462 2023-01-14 00:20:29.000000 pygrace-1.3/pygrace/extensions/multi_grace.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    20989 2023-01-14 00:20:29.000000 pygrace-1.3/pygrace/extensions/multi_plot.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24816 2023-01-14 00:20:29.000000 pygrace-1.3/pygrace/extensions/network.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11356 2023-01-14 00:20:29.000000 pygrace-1.3/pygrace/extensions/panel.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2361 2023-01-14 00:20:29.000000 pygrace-1.3/pygrace/extensions/table.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7228 2023-01-14 00:20:29.000000 pygrace-1.3/pygrace/extensions/tree.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1514 2023-01-14 00:20:15.000000 pygrace-1.3/pygrace/fonts.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      520 2023-01-14 00:20:15.000000 pygrace-1.3/pygrace/grace.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    29419 2023-01-14 00:20:15.000000 pygrace-1.3/pygrace/graph.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.411003 pygrace-1.3/pygrace/interactive/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      735 2023-01-14 00:20:48.000000 pygrace-1.3/pygrace/interactive/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8959 2023-01-14 00:20:48.000000 pygrace-1.3/pygrace/interactive/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    20421 2023-01-14 00:20:48.000000 pygrace-1.3/pygrace/interactive/project.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13475 2023-01-14 00:20:48.000000 pygrace-1.3/pygrace/interactive/session.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2610 2023-01-14 00:20:15.000000 pygrace-1.3/pygrace/parser.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      431 2023-01-14 00:20:15.000000 pygrace-1.3/pygrace/plot.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13729 2023-01-14 00:20:15.000000 pygrace-1.3/pygrace/project.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.414677 pygrace-1.3/pygrace/styles/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      358 2023-01-14 00:21:22.000000 pygrace-1.3/pygrace/styles/__init__.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.418710 pygrace-1.3/pygrace/styles/colorbrewer/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      358 2023-01-14 00:21:39.000000 pygrace-1.3/pygrace/styles/colorbrewer/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    39028 2023-01-14 00:15:34.000000 pygrace-1.3/pygrace/styles/colorbrewer/colorbrewer.dat
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12720 2023-01-14 00:21:39.000000 pygrace-1.3/pygrace/styles/colorbrewer/colorbrewer.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)   143700 2023-01-14 00:15:34.000000 pygrace-1.3/pygrace/styles/colorbrewer/colorbrewer_swatches.pdf
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8042 2023-01-14 00:21:22.000000 pygrace-1.3/pygrace/styles/el.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2421 2023-01-14 00:21:22.000000 pygrace-1.3/pygrace/styles/journals.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8287 2023-01-14 00:21:22.000000 pygrace-1.3/pygrace/styles/metra.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.426210 pygrace-1.3/pygrace/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      569 2023-01-14 00:21:06.000000 pygrace-1.3/pygrace/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      904 2023-01-14 00:21:06.000000 pygrace-1.3/pygrace/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    14704 2023-01-14 18:41:06.000000 pygrace-1.3/pygrace/tests/test_interactive.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      796 2023-01-14 18:01:52.000000 pygrace-1.3/pygrace/tests/test_templates.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.389784 pygrace-1.3/pygrace.egg-info/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9771 2023-07-23 19:56:41.000000 pygrace-1.3/pygrace.egg-info/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2793 2023-07-23 19:56:41.000000 pygrace-1.3/pygrace.egg-info/SOURCES.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-23 19:56:41.000000 pygrace-1.3/pygrace.egg-info/dependency_links.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-23 19:56:40.000000 pygrace-1.3/pygrace.egg-info/not-zip-safe
+-rw-r--r--   0 mmckerns   (501) staff       (20)       24 2023-07-23 19:56:41.000000 pygrace-1.3/pygrace.egg-info/requires.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        8 2023-07-23 19:56:41.000000 pygrace-1.3/pygrace.egg-info/top_level.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)      308 2023-01-14 00:16:12.000000 pygrace-1.3/pyproject.toml
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 19:56:41.428122 pygrace-1.3/scripts/
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2532 2023-01-14 00:19:43.000000 pygrace-1.3/scripts/pygrace_cdf
+-rw-r--r--   0 mmckerns   (501) staff       (20)       62 2023-07-23 19:56:41.431387 pygrace-1.3/setup.cfg
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5128 2023-02-20 18:54:04.000000 pygrace-1.3/setup.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      663 2023-07-07 03:27:30.000000 pygrace-1.3/tox.ini
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3165 2023-07-23 19:55:48.000000 pygrace-1.3/version.py
```

### Comparing `pygrace-1.2.1/.codecov.yml` & `pygrace-1.3/.codecov.yml`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/.coveragerc` & `pygrace-1.3/.coveragerc`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/.travis.yml` & `pygrace-1.3/.travis.yml`

 * *Files 12% similar despite different names*

```diff
@@ -12,36 +12,37 @@
         - python: '3.9'
           env:
             - COVERAGE="true"
 
         - python: '3.10'
           env:
 
-        - python: '3.11-dev'
+        - python: '3.11'
           env:
             - CYTHON="true" # numpy source build
 
         - python: '3.12-dev'
           env:
             - CYTHON="true" # numpy source build
 
         - python: 'pypy3.7-7.3.9'
           env:
 
-        - python: 'pypy3.8-7.3.9'
+        - python: 'pypy3.8-7.3.9' # at 7.3.11
           env:
 
-        - python: 'pypy3.9-7.3.9'
+        - python: 'pypy3.9-7.3.9' # at 7.3.12
+          env:
+
+        - python: 'pypy3.10-7.3.12'
           env:
 
     allow_failures:
         - python: '3.12-dev'
-        - python: 'pypy3.7-7.3.9'
-        - python: 'pypy3.8-7.3.9'
-        - python: 'pypy3.9-7.3.9'
+        - python: 'pypy3.10-7.3.12' # CI missing
     fast_finish: true
 
 cache:
     pip: true
 
 before_install: #NOTE: DISPLAY-related tests don't break build on Travis
     - sudo apt-get -y install xorg openbox grace # DISPLAY=:0.0 xmgrace #Can't open display; Failed initializing GUI, exiting
```

### Comparing `pygrace-1.2.1/LICENSE` & `pygrace-1.3/LICENSE`

 * *Files 6% similar despite different names*

```diff
@@ -5,22 +5,22 @@
 
 This software is available subject to the conditions and terms laid
 out below. By downloading and using this software you are agreeing
 to the following conditions.
 
 Redistribution and use in source and binary forms, with or without
 modification, are permitted provided that the following conditions
-are met::
+are met:
 
-    - Redistribution of source code must retain the above copyright
+    - Redistributions of source code must retain the above copyright
       notice, this list of conditions and the following disclaimer.
 
-    - Redistribution in binary form must reproduce the above copyright
+    - Redistributions in binary form must reproduce the above copyright
       notice, this list of conditions and the following disclaimer in the
-      documentations and/or other materials provided with the distribution.
+      documentation and/or other materials provided with the distribution.
 
     - Neither the names of the copyright holders nor the names of any of
       the contributors may be used to endorse or promote products derived
       from this software without specific prior written permission.
 
 THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
 "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED
```

### Comparing `pygrace-1.2.1/PKG-INFO` & `pygrace-1.3/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: pygrace
-Version: 1.2.1
-Summary: Python interface to xmgrace and xmgrace project files
+Version: 1.3
+Summary: Python bindings to xmgrace
 Home-page: https://github.com/uqfoundation/pygrace
 Download-URL: https://pypi.org/project/pygrace/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
 License: BSD-3-Clause
@@ -27,41 +27,41 @@
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Software Development
 Requires-Python: >=3.7
 License-File: LICENSE
 
-------------------------------------
-pygrace: Python bindings to xmgrace.
-------------------------------------
+-----------------------------------
+pygrace: Python bindings to xmgrace
+-----------------------------------
 
 About Pygrace
 =============
 
-``pygrace`` was designed to enable the construction and use of ``xmgrace`` projects from python.  ``pygrace`` provides a collection of classes that serve as editable templates for elements of a xmgrace project. The inheritance structure of ``pygrace`` mirrors the structure of ``xmgrace``.
+``pygrace`` was designed to enable the construction and use of ``xmgrace`` projects from Python.  ``pygrace`` provides a collection of classes that serve as editable templates for elements of a xmgrace project. The inheritance structure of ``pygrace`` mirrors the structure of ``xmgrace``.
 
 ``pygrace`` ``Project`` objects are used to construct and save ``xmgrace`` project files (.agr). ``Project`` files capture the state of a ``xmgrace`` session, including the figures, settings, and current variables.
 
 .. image:: https://github.com/uqfoundation/pygrace/raw/master/docs/source/_static/crow_diagram.png
    :alt: pygrace project
 
 A more detailed diagram of all the attributes of ``pygrace`` template objects can be found at https://github.com/uqfoundation/pygrace/blob/master/docs/diagrams/diagram.pdf, while a handy cheatsheet of the methods and attributes of each ``pygrace`` template class can be found at https://github.com/uqfoundation/pygrace/blob/master/docs/diagrams/cheatsheet.pdf. This cheatsheet can be dynamically generated through use of the ``write_cheatsheet`` method, available from the ``Project`` class.
 
 ``pygrace`` is in active development, so any user feedback, bug reports, comments, or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pygrace/issues, with a legacy list maintained at https://github.com/pygrace/pygrace/issues.
 
 
 Major Features
 ==============
 
-``pygrace`` provides an object-oriented python interface for the efficient construction of ``xmgrace`` projects (e.g. highly-customizable publication-quality single and multi-figure plots). ``pygrace`` provides:
+``pygrace`` provides an object-oriented Python interface for the efficient construction of ``xmgrace`` projects (e.g. highly-customizable publication-quality single and multi-figure plots). ``pygrace`` provides:
 
-    - an object-relational mapping from python objects to a ``xmgrace`` project
-    - an interactive python-based ``grace>`` prompt for ``xmgrace`` commands
-    - a set of high-level python functions for drawing ``xmgrace`` ``Graphs``
+    - an object-relational mapping from Python objects to a ``xmgrace`` project
+    - an interactive Python-based ``grace>`` prompt for ``xmgrace`` commands
+    - a set of high-level Python functions for drawing ``xmgrace`` ``Graphs``
 
 Current Release
 ===============
 
 The latest released version of ``pygrace`` is available from:
 
     https://pypi.org/project/pygrace
@@ -162,15 +162,15 @@
 
 
 we can also work in an interactive xmgrace session::
 
     >>> from pygrace import grace
     >>> pg = grace()
 
-use xmgrace methods directly from the python interpreter::
+use xmgrace methods directly from the Python interpreter::
 
     >>> import numpy as np
     >>> x = np.arange(21) * np.pi/10
     >>> pg.plot(x, np.sin(x))
 
 .. image:: https://github.com/uqfoundation/pygrace/raw/master/docs/source/_static/sin.png
    :alt: sin
@@ -207,15 +207,15 @@
     >>> pg.who('x')
     array([0.        , 0.31415927, 0.62831853, 0.9424778 , 1.25663706,
            1.57079633, 1.88495559, 2.19911486, 2.51327412, 2.82743339,
            3.14159265, 3.45575192, 3.76991118, 4.08407045, 4.39822972,
            4.71238898, 5.02654825, 5.34070751, 5.65486678, 5.96902604,
            6.28318531])
 
-get variables back into python from xmgrace::
+get variables back into Python from xmgrace::
 
     >>> cosx = pg.get('y')
 
 use shortcuts for put, eval, and get::
 
     >>> pg.z = 0.5
     >>> pg('print(z)')
@@ -243,28 +243,29 @@
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://pygrace.rtfd.io. Also see ``pygrace.tests`` for a set of scripts that
-demonstrate several of the many features of ``pygrace``.
-You can run the test suite with ``python -m pygrace.tests``. 
-Also see ``pygrace.examples`` for examples that demonstrate the construction
-of ``xmgrace`` project files (.agr). ``pygrace.examples.interactive`` includes
-examples of using ``python`` to interact with a live ``xmgrace`` session.
-The source code is relatively well documented, so some questions may be resolved by inspecting the code itself.  However, please feel free to submit a ticket on github, or ask a question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pygrace`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+demonstrate several of the many features of ``pygrace``. You can run the test
+suite with ``python -m pygrace.tests``. Also see https://github.com/uqfoundation/pygrace/tree/master/examples for examples that demonstrate the construction
+of ``xmgrace`` project files (.agr). https://github.com/uqfoundation/pygrace/tree/master/examples/interactive includes examples of using ``python`` to interact
+with a live ``xmgrace`` session. The source code is relatively well documented,
+so some questions may be resolved by inspecting the code itself.  However,
+please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``pygrace`` in your work, please send an email (to **mmckerns at uqfoundation
+dot org**).
 
 
 Citation 
 ========
 
 If you use ``pygrace`` to do research that leads to publication, we ask that you
 acknowledge use of ``pygrace`` by citing the following in your publication::
 
     Michael McKerns, Dean Malmgren, Mike Stringer, and Daniel Stouffer,
-    "pygrace: python bindings to xmgrace", 2005- ;
+    "pygrace: Python bindings to xmgrace", 2005- ;
     https://github.com/uqfoundation/pygrace
 
 Please see https://pygrace.github.io/ for further information on an earlier version of ``pygrace`` developed by Dean Malmgren, Mike Stringer, and members of the Amaral Lab, and later maintained by Daniel Stouffer and members of the Stouffer Lab. This code has been merged into the original ``pygrace`` developed by Mike McKerns.
```

### Comparing `pygrace-1.2.1/README.md` & `pygrace-1.3/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -1,34 +1,35 @@
 pygrace
 =======
-Python bindings to xmgrace.
+Python bindings to xmgrace
 
 About Pygrace
 -------------
-``pygrace`` was designed to enable the construction and use of ``xmgrace`` projects from python.  ``pygrace`` provides a collection of classes that serve as editable templates for elements of a xmgrace project. The inheritance structure of ``pygrace`` mirrors the structure of ``xmgrace``.
+``pygrace`` was designed to enable the construction and use of ``xmgrace`` projects from Python.  ``pygrace`` provides a collection of classes that serve as editable templates for elements of a xmgrace project. The inheritance structure of ``pygrace`` mirrors the structure of ``xmgrace``.
 
 ``pygrace`` ``Project`` objects are used to construct and save ``xmgrace`` project files (.agr). ``Project`` files capture the state of a ``xmgrace`` session, including the figures, settings, and current variables.
 
 ![pygrace project](https://github.com/uqfoundation/pygrace/raw/master/docs/source/_static/crow_diagram.png)
 
 A more detailed diagram of all the attributes of ``pygrace`` template objects can be found at https://github.com/uqfoundation/pygrace/blob/master/docs/diagrams/diagram.pdf, while a handy cheatsheet of the methods and attributes of each ``pygrace`` template class can be found at https://github.com/uqfoundation/pygrace/blob/master/docs/diagrams/cheatsheet.pdf. This cheatsheet can be dynamically generated through use of the ``write_cheatsheet`` method, available from the ``Project`` class.
 
 ``pygrace`` is in active development, so any user feedback, bug reports, comments, or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pygrace/issues, with a legacy list maintained at https://github.com/pygrace/pygrace/issues.
 
 
 Major Features
 --------------
-``pygrace`` provides an object-oriented python interface for the efficient construction of ``xmgrace`` projects (e.g. highly-customizable publication-quality single and multi-figure plots). ``pygrace`` provides:
+``pygrace`` provides an object-oriented Python interface for the efficient construction of ``xmgrace`` projects (e.g. highly-customizable publication-quality single and multi-figure plots). ``pygrace`` provides:
 
-* an object-relational mapping from python objects to a ``xmgrace`` project
-* an interactive python-based ``grace>`` prompt for ``xmgrace`` commands
-* a set of high-level python functions for drawing ``xmgrace`` ``Graphs``
+* an object-relational mapping from Python objects to a ``xmgrace`` project
+* an interactive Python-based ``grace>`` prompt for ``xmgrace`` commands
+* a set of high-level Python functions for drawing ``xmgrace`` ``Graphs``
 
 Current Release
 [![Downloads](https://static.pepy.tech/personalized-badge/pygrace?period=total&units=international_system&left_color=grey&right_color=blue&left_text=pypi%20downloads)](https://pepy.tech/project/pygrace)
+[![Stack Overflow](https://img.shields.io/badge/stackoverflow-get%20help-black.svg)](https://stackoverflow.com/questions/tagged/pygrace)
 ---------------
 The latest released version of ``pygrace`` is available from:
     https://pypi.org/project/pygrace
 
 ``pygrace`` is distributed under a 3-clause BSD license.
 
 Development Version
@@ -120,15 +121,15 @@
 
 
 we can also work in an interactive xmgrace session::
 
     >>> from pygrace import grace
     >>> pg = grace()
 
-use xmgrace methods directly from the python interpreter::
+use xmgrace methods directly from the Python interpreter::
 
     >>> import numpy as np
     >>> x = np.arange(21) * np.pi/10
     >>> pg.plot(x, np.sin(x))
 
 ![sin](https://github.com/uqfoundation/pygrace/raw/master/docs/source/_static/sin.png)
 
@@ -162,15 +163,15 @@
     >>> pg.who('x')
     array([0.        , 0.31415927, 0.62831853, 0.9424778 , 1.25663706,
            1.57079633, 1.88495559, 2.19911486, 2.51327412, 2.82743339,
            3.14159265, 3.45575192, 3.76991118, 4.08407045, 4.39822972,
            4.71238898, 5.02654825, 5.34070751, 5.65486678, 5.96902604,
            6.28318531])
 
-get variables back into python from xmgrace::
+get variables back into Python from xmgrace::
 
     >>> cosx = pg.get('y')
 
 use shortcuts for put, eval, and get::
 
     >>> pg.z = 0.5
     >>> pg('print(z)')
@@ -197,27 +198,28 @@
     >>> pg = grace(project='histoPlot.agr')
 
 
 More Information
 ----------------
 Probably the best way to get started is to look at the documentation at
 http://pygrace.rtfd.io. Also see ``pygrace.tests`` for a set of scripts that
-demonstrate several of the many features of ``pygrace``.
-You can run the test suite with ``python -m pygrace.tests``. 
-Also see ``pygrace.examples`` for examples that demonstrate the construction
-of ``xmgrace`` project files (.agr). ``pygrace.examples.interactive`` includes
-examples of using ``python`` to interact with a live ``xmgrace`` session.
-The source code is relatively well documented, so some questions may be resolved by inspecting the code itself.  However, please feel free to submit a ticket on github, or ask a question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pygrace`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+demonstrate several of the many features of ``pygrace``. You can run the test
+suite with ``python -m pygrace.tests``. Also see https://github.com/uqfoundation/pygrace/tree/master/examples for examples that demonstrate the construction
+of ``xmgrace`` project files (.agr). https://github.com/uqfoundation/pygrace/tree/master/examples/interactive includes examples of using ``python`` to interact
+with a live ``xmgrace`` session. The source code is relatively well documented,
+so some questions may be resolved by inspecting the code itself.  However,
+please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``pygrace`` in your work, please send an email (to **mmckerns at uqfoundation
+dot org**).
 
 
 Citation 
 --------
 If you use ``pygrace`` to do research that leads to publication, we ask that you
 acknowledge use of ``pygrace`` by citing the following in your publication::
 
     Michael McKerns, Dean Malmgren, Mike Stringer, and Daniel Stouffer,
-    "pygrace: python bindings to xmgrace", 2005- ;
+    "pygrace: Python bindings to xmgrace", 2005- ;
     https://github.com/uqfoundation/pygrace
 
 Please see https://pygrace.github.io/ for further information on an earlier version of ``pygrace`` developed by Dean Malmgren, Mike Stringer, and members of the Amaral Lab, and later maintained by Daniel Stouffer and members of the Stouffer Lab. This code has been merged into the original ``pygrace`` developed by Mike McKerns.
```

### Comparing `pygrace-1.2.1/docs/Makefile` & `pygrace-1.3/docs/Makefile`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/diagrams/cheatsheet.pdf` & `pygrace-1.3/docs/diagrams/cheatsheet.pdf`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/diagrams/crow_diagram.pdf` & `pygrace-1.3/docs/diagrams/crow_diagram.pdf`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/diagrams/crow_diagram.svg` & `pygrace-1.3/docs/diagrams/crow_diagram.svg`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/diagrams/diagram.big.graph` & `pygrace-1.3/docs/diagrams/diagram.big.graph`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/diagrams/diagram.graph` & `pygrace-1.3/docs/diagrams/diagram.graph`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/diagrams/diagram.pdf` & `pygrace-1.3/docs/diagrams/diagram.pdf`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/source/_static/00_helloworld.png` & `pygrace-1.3/docs/source/_static/00_helloworld.png`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/source/_static/05_colorplot.png` & `pygrace-1.3/docs/source/_static/05_colorplot.png`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/source/_static/08_latexlabels.png` & `pygrace-1.3/docs/source/_static/08_latexlabels.png`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/source/_static/cos.png` & `pygrace-1.3/docs/source/_static/cos.png`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/source/_static/crow_diagram.png` & `pygrace-1.3/docs/source/_static/crow_diagram.png`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/source/_static/histoPlot.png` & `pygrace-1.3/docs/source/_static/histoPlot.png`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/source/_static/sin.png` & `pygrace-1.3/docs/source/_static/sin.png`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/docs/source/conf.py` & `pygrace-1.3/docs/source/conf.py`

 * *Files 7% similar despite different names*

```diff
@@ -53,24 +53,42 @@
 # source_suffix = ['.rst', '.md']
 source_suffix = '.rst'
 
 # The master toctree document.
 master_doc = 'index'
 
 # General information about the project.
-project = u'pygrace'
+project = 'pygrace'
 year = datetime.now().year
-copyright = u'%d, The Uncertainty Quantification Foundation' % year
-author = u'Mike McKerns'
+copyright = '%d, The Uncertainty Quantification Foundation' % year
+author = 'Mike McKerns'
 
 # extension config
 github_project_url = "https://github.com/uqfoundation/pygrace"
 autoclass_content = 'both'
+autodoc_default_options = {
+    'members': True,
+    'undoc-members': True,
+    'private-members': True,
+    'special-members': True,
+    'show-inheritance': True,
+    'imported-members': True,
+    'exclude-members': (
+        '__dict__,'
+        '__slots__,'
+        '__weakref__,'
+        '__module__,'
+        '_abc_impl,'
+        '__init__,'
+        '__annotations__,'
+        '__dataclass_fields__,'
+    )
+}
 autodoc_typehints = 'description'
-napoleon_include_init_with_doc = True
+autodoc_typehints_format = 'short'
 napoleon_include_private_with_doc = False
 napoleon_include_special_with_doc = True
 napoleon_use_ivar = True
 napoleon_use_param = True
 
 # The version info for the project you're documenting, acts as replacement for
 # |version| and |release|, also used in various other places throughout the
@@ -110,57 +128,63 @@
 on_rtd = os.environ.get('READTHEDOCS', None) == 'True'
 
 # The theme to use for HTML and HTML Help pages.  See the documentation for
 # a list of builtin themes.
 #
 if not on_rtd:
     html_theme = 'alabaster' #'bizstyle'
+    html_css_files = ['css/custom.css',]
    #import sphinx_rtd_theme
    #html_theme = 'sphinx_rtd_theme'
    #html_theme_path = [sphinx_rtd_theme.get_html_theme_path()]
 
 # Theme options are theme-specific and customize the look and feel of a theme
 # further.  For a list of options available for each theme, see the
 # documentation.
 #
 html_theme_options = {
     'github_user': 'pygrace',
     'github_repo': 'pygrace',
     'github_button': False,
     'github_banner': True,
     'travis_button': True,
+    'codecov_button': True,
+    'donate_url': 'http://uqfoundation.org/pages/donate.html',
     'gratipay_user': False,  # username
     'extra_nav_links': {'Module Index': 'py-modindex.html'},
 #   'show_related': True,
+#   'globaltoc_collapse': True,
+    'globaltoc_maxdepth': 4,
     'show_powered_by': False
 }
 
 # Add any paths that contain custom static files (such as style sheets) here,
 # relative to this directory. They are copied after the builtin static files,
 # so a file named "default.css" will overwrite the builtin "default.css".
 html_static_path = ['_static']
 
 # Custom sidebar templates, must be a dictionary that maps document names
 # to template names.
 #
 # This is required for the alabaster theme
 # refs: http://alabaster.readthedocs.io/en/latest/installation.html#sidebars
-#if html_theme == 'alabaster':
+if on_rtd:
+    toc_style = 'localtoc.html', # display the toctree
+else:
+    toc_style = 'globaltoc.html', # collapse the toctree
 html_sidebars = {
     '**': [
         'about.html',
+        'donate.html',
+        'searchbox.html',
 #       'navigation.html',
-        'localtoc.html', # display the toctree
+        toc_style, # defined above
         'relations.html', # needs 'show_related':True option to display
-        'searchbox.html',
-        'donate.html', # needs 'gratipay_user':<uname> option to display
     ]
 }
-#FIXME: donate / UQFoundation (home/github)
-
 
 # -- Options for HTMLHelp output ------------------------------------------
 
 # Output file base name for HTML help builder.
 htmlhelp_basename = 'pygracedoc'
 
 # Logo for sidebar
@@ -187,45 +211,45 @@
     # 'figure_align': 'htbp',
 }
 
 # Grouping the document tree into LaTeX files. List of tuples
 # (source start file, target name, title,
 #  author, documentclass [howto, manual, or own class]).
 latex_documents = [
-    (master_doc, 'pygrace.tex', u'pygrace Documentation',
-     u'Mike McKerns', 'manual'),
+    (master_doc, 'pygrace.tex', 'pygrace Documentation',
+     'Mike McKerns', 'manual'),
 ]
 
 
 # -- Options for manual page output ---------------------------------------
 
 # One entry per manual page. List of tuples
 # (source start file, name, description, authors, manual section).
 man_pages = [
-    (master_doc, 'pygrace', u'pygrace Documentation',
+    (master_doc, 'pygrace', 'pygrace Documentation',
      [author], 1)
 ]
 
 
 # -- Options for Texinfo output -------------------------------------------
 
 # Grouping the document tree into Texinfo files. List of tuples
 # (source start file, target name, title, author,
 #  dir menu entry, description, category)
 texinfo_documents = [
-    (master_doc, 'pygrace', u'pygrace Documentation',
+    (master_doc, 'pygrace', 'pygrace Documentation',
      author, 'pygrace', 'Python interface to xmgrace and xmgrace project files.',
      'Miscellaneous'),
 ]
 
 
 
 
 # Example configuration for intersphinx: refer to the Python standard library.
-intersphinx_mapping = {'https://docs.python.org/': None}
+intersphinx_mapping = {'https://docs.python.org/3/': None}
 #    {'python': {'https://docs.python.org/': None},
 #     'mystic': {'https://mystic.readthedocs.io/en/latest/', None},
 #     'pyina': {'https://pyina.readthedocs.io/en/latest/', None},
 #     'pox': {'https://pox.readthedocs.io/en/latest/', None},
 #     'dill': {'https://dill.readthedocs.io/en/latest/', None},
 #     'multiprocess': {'https://multiprocess.readthedocs.io/en/latest/', None},
 #     'ppft': {'https://ppft.readthedocs.io/en/latest/', None},
```

### Comparing `pygrace-1.2.1/docs/source/pygrace.png` & `pygrace-1.3/docs/source/pygrace.png`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/00_helloworld.py` & `pygrace-1.3/examples/00_helloworld.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/01_singleplot.py` & `pygrace-1.3/examples/01_singleplot.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/02_multiplot.py` & `pygrace-1.3/examples/02_multiplot.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/03_simplesubclass.py` & `pygrace-1.3/examples/03_simplesubclass.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/04_classy.py` & `pygrace-1.3/examples/04_classy.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/05_colorplot.py` & `pygrace-1.3/examples/05_colorplot.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/06_logautoscale.py` & `pygrace-1.3/examples/06_logautoscale.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/07_panels.py` & `pygrace-1.3/examples/07_panels.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/08_latexlabels.py` & `pygrace-1.3/examples/08_latexlabels.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/09_datasets.py` & `pygrace-1.3/examples/09_datasets.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/10_dataset_features.py` & `pygrace-1.3/examples/10_dataset_features.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/11_network.py` & `pygrace-1.3/examples/11_network.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/12_cheatsheet.py` & `pygrace-1.3/examples/12_cheatsheet.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/13_directed_network.py` & `pygrace-1.3/examples/13_directed_network.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/14_phylogenetic_tree.py` & `pygrace-1.3/examples/14_phylogenetic_tree.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/clean_examples.py` & `pygrace-1.3/examples/clean_examples.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/example_tools.py` & `pygrace-1.3/examples/example_tools.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/interactive/grace.py` & `pygrace-1.3/examples/interactive/grace.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/interactive/grace_prompt.py` & `pygrace-1.3/examples/interactive/grace_prompt.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/interactive/process.py` & `pygrace-1.3/examples/interactive/process.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/interactive/project.py` & `pygrace-1.3/examples/interactive/project.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/interactive/prompt.py` & `pygrace-1.3/examples/interactive/prompt.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/examples/test_examples.py` & `pygrace-1.3/examples/test_examples.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/__info__.py` & `pygrace-1.3/pygrace/__info__.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,41 +1,41 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pygrace/blob/master/LICENSE
 '''
-------------------------------------
-pygrace: Python bindings to xmgrace.
-------------------------------------
+-----------------------------------
+pygrace: Python bindings to xmgrace
+-----------------------------------
 
 About Pygrace
 =============
 
-``pygrace`` was designed to enable the construction and use of ``xmgrace`` projects from python.  ``pygrace`` provides a collection of classes that serve as editable templates for elements of a xmgrace project. The inheritance structure of ``pygrace`` mirrors the structure of ``xmgrace``.
+``pygrace`` was designed to enable the construction and use of ``xmgrace`` projects from Python.  ``pygrace`` provides a collection of classes that serve as editable templates for elements of a xmgrace project. The inheritance structure of ``pygrace`` mirrors the structure of ``xmgrace``.
 
 ``pygrace`` ``Project`` objects are used to construct and save ``xmgrace`` project files (.agr). ``Project`` files capture the state of a ``xmgrace`` session, including the figures, settings, and current variables.
 
 .. image:: https://github.com/uqfoundation/pygrace/raw/master/docs/source/_static/crow_diagram.png
    :alt: pygrace project
 
 A more detailed diagram of all the attributes of ``pygrace`` template objects can be found at https://github.com/uqfoundation/pygrace/blob/master/docs/diagrams/diagram.pdf, while a handy cheatsheet of the methods and attributes of each ``pygrace`` template class can be found at https://github.com/uqfoundation/pygrace/blob/master/docs/diagrams/cheatsheet.pdf. This cheatsheet can be dynamically generated through use of the ``write_cheatsheet`` method, available from the ``Project`` class.
 
 ``pygrace`` is in active development, so any user feedback, bug reports, comments, or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pygrace/issues, with a legacy list maintained at https://github.com/pygrace/pygrace/issues.
 
 
 Major Features
 ==============
 
-``pygrace`` provides an object-oriented python interface for the efficient construction of ``xmgrace`` projects (e.g. highly-customizable publication-quality single and multi-figure plots). ``pygrace`` provides:
+``pygrace`` provides an object-oriented Python interface for the efficient construction of ``xmgrace`` projects (e.g. highly-customizable publication-quality single and multi-figure plots). ``pygrace`` provides:
 
-    - an object-relational mapping from python objects to a ``xmgrace`` project
-    - an interactive python-based ``grace>`` prompt for ``xmgrace`` commands
-    - a set of high-level python functions for drawing ``xmgrace`` ``Graphs``
+    - an object-relational mapping from Python objects to a ``xmgrace`` project
+    - an interactive Python-based ``grace>`` prompt for ``xmgrace`` commands
+    - a set of high-level Python functions for drawing ``xmgrace`` ``Graphs``
 
 Current Release
 ===============
 
 The latest released version of ``pygrace`` is available from:
 
     https://pypi.org/project/pygrace
@@ -136,15 +136,15 @@
 
 
 we can also work in an interactive xmgrace session::
 
     >>> from pygrace import grace
     >>> pg = grace()
 
-use xmgrace methods directly from the python interpreter::
+use xmgrace methods directly from the Python interpreter::
 
     >>> import numpy as np
     >>> x = np.arange(21) * np.pi/10
     >>> pg.plot(x, np.sin(x))
 
 .. image:: https://github.com/uqfoundation/pygrace/raw/master/docs/source/_static/sin.png
    :alt: sin
@@ -181,15 +181,15 @@
     >>> pg.who('x')
     array([0.        , 0.31415927, 0.62831853, 0.9424778 , 1.25663706,
            1.57079633, 1.88495559, 2.19911486, 2.51327412, 2.82743339,
            3.14159265, 3.45575192, 3.76991118, 4.08407045, 4.39822972,
            4.71238898, 5.02654825, 5.34070751, 5.65486678, 5.96902604,
            6.28318531])
 
-get variables back into python from xmgrace::
+get variables back into Python from xmgrace::
 
     >>> cosx = pg.get('y')
 
 use shortcuts for put, eval, and get::
 
     >>> pg.z = 0.5
     >>> pg('print(z)')
@@ -217,60 +217,61 @@
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://pygrace.rtfd.io. Also see ``pygrace.tests`` for a set of scripts that
-demonstrate several of the many features of ``pygrace``.
-You can run the test suite with ``python -m pygrace.tests``. 
-Also see ``pygrace.examples`` for examples that demonstrate the construction
-of ``xmgrace`` project files (.agr). ``pygrace.examples.interactive`` includes
-examples of using ``python`` to interact with a live ``xmgrace`` session.
-The source code is relatively well documented, so some questions may be resolved by inspecting the code itself.  However, please feel free to submit a ticket on github, or ask a question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pygrace`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+demonstrate several of the many features of ``pygrace``. You can run the test
+suite with ``python -m pygrace.tests``. Also see https://github.com/uqfoundation/pygrace/tree/master/examples for examples that demonstrate the construction
+of ``xmgrace`` project files (.agr). https://github.com/uqfoundation/pygrace/tree/master/examples/interactive includes examples of using ``python`` to interact
+with a live ``xmgrace`` session. The source code is relatively well documented,
+so some questions may be resolved by inspecting the code itself.  However,
+please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``pygrace`` in your work, please send an email (to **mmckerns at uqfoundation
+dot org**).
 
 
 Citation 
 ========
 
 If you use ``pygrace`` to do research that leads to publication, we ask that you
 acknowledge use of ``pygrace`` by citing the following in your publication::
 
     Michael McKerns, Dean Malmgren, Mike Stringer, and Daniel Stouffer,
-    "pygrace: python bindings to xmgrace", 2005- ;
+    "pygrace: Python bindings to xmgrace", 2005- ;
     https://github.com/uqfoundation/pygrace
 
 Please see https://pygrace.github.io/ for further information on an earlier version of ``pygrace`` developed by Dean Malmgren, Mike Stringer, and members of the Amaral Lab, and later maintained by Daniel Stouffer and members of the Stouffer Lab. This code has been merged into the original ``pygrace`` developed by Mike McKerns.
 '''
 
-__version__ = '1.2.1'
+__version__ = '1.3'
 __author__ = 'Mike McKerns'
 
 __license__ = '''
 Copyright (c) 2004-2016 California Institute of Technology.
 Copyright (c) 2013 Daniel Stouffer.
 Copyright (c) 2023 The Uncertainty Quantification Foundation.
 All rights reserved.
 
 This software is available subject to the conditions and terms laid
 out below. By downloading and using this software you are agreeing
 to the following conditions.
 
 Redistribution and use in source and binary forms, with or without
 modification, are permitted provided that the following conditions
-are met::
+are met:
 
-    - Redistribution of source code must retain the above copyright
+    - Redistributions of source code must retain the above copyright
       notice, this list of conditions and the following disclaimer.
 
-    - Redistribution in binary form must reproduce the above copyright
+    - Redistributions in binary form must reproduce the above copyright
       notice, this list of conditions and the following disclaimer in the
-      documentations and/or other materials provided with the distribution.
+      documentation and/or other materials provided with the distribution.
 
     - Neither the names of the copyright holders nor the names of any of
       the contributors may be used to endorse or promote products derived
       from this software without specific prior written permission.
 
 THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
 "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED
```

### Comparing `pygrace-1.2.1/pygrace/__init__.py` & `pygrace-1.3/pygrace/__init__.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/axis.py` & `pygrace-1.3/pygrace/axis.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/base.py` & `pygrace-1.3/pygrace/base.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/colors.py` & `pygrace-1.3/pygrace/colors.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/dataset.py` & `pygrace-1.3/pygrace/dataset.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/drawing_objects.py` & `pygrace-1.3/pygrace/drawing_objects.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/extensions/colorbar.py` & `pygrace-1.3/pygrace/extensions/colorbar.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/extensions/distribution.py` & `pygrace-1.3/pygrace/extensions/distribution.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/extensions/latex_string.py` & `pygrace-1.3/pygrace/extensions/latex_string.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/extensions/multi_plot.py` & `pygrace-1.3/pygrace/extensions/multi_plot.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/extensions/network.py` & `pygrace-1.3/pygrace/extensions/network.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/extensions/panel.py` & `pygrace-1.3/pygrace/extensions/panel.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/extensions/table.py` & `pygrace-1.3/pygrace/extensions/table.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/extensions/tree.py` & `pygrace-1.3/pygrace/extensions/tree.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/fonts.py` & `pygrace-1.3/pygrace/fonts.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/grace.py` & `pygrace-1.3/pygrace/grace.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/graph.py` & `pygrace-1.3/pygrace/graph.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/interactive/__init__.py` & `pygrace-1.3/pygrace/interactive/__init__.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/interactive/process.py` & `pygrace-1.3/pygrace/interactive/process.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/interactive/project.py` & `pygrace-1.3/pygrace/interactive/project.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/interactive/session.py` & `pygrace-1.3/pygrace/interactive/session.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/parser.py` & `pygrace-1.3/pygrace/parser.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/project.py` & `pygrace-1.3/pygrace/project.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/styles/colorbrewer/colorbrewer.dat` & `pygrace-1.3/pygrace/styles/colorbrewer/colorbrewer.dat`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/styles/colorbrewer/colorbrewer.py` & `pygrace-1.3/pygrace/styles/colorbrewer/colorbrewer.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/styles/colorbrewer/colorbrewer_swatches.pdf` & `pygrace-1.3/pygrace/styles/colorbrewer/colorbrewer_swatches.pdf`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/styles/el.py` & `pygrace-1.3/pygrace/styles/el.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/styles/journals.py` & `pygrace-1.3/pygrace/styles/journals.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/styles/metra.py` & `pygrace-1.3/pygrace/styles/metra.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/tests/__init__.py` & `pygrace-1.3/pygrace/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/tests/__main__.py` & `pygrace-1.3/pygrace/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/tests/test_interactive.py` & `pygrace-1.3/pygrace/tests/test_interactive.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace/tests/test_templates.py` & `pygrace-1.3/pygrace/tests/test_templates.py`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/pygrace.egg-info/PKG-INFO` & `pygrace-1.3/pygrace.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: pygrace
-Version: 1.2.1
-Summary: Python interface to xmgrace and xmgrace project files
+Version: 1.3
+Summary: Python bindings to xmgrace
 Home-page: https://github.com/uqfoundation/pygrace
 Download-URL: https://pypi.org/project/pygrace/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
 License: BSD-3-Clause
@@ -27,41 +27,41 @@
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Software Development
 Requires-Python: >=3.7
 License-File: LICENSE
 
-------------------------------------
-pygrace: Python bindings to xmgrace.
-------------------------------------
+-----------------------------------
+pygrace: Python bindings to xmgrace
+-----------------------------------
 
 About Pygrace
 =============
 
-``pygrace`` was designed to enable the construction and use of ``xmgrace`` projects from python.  ``pygrace`` provides a collection of classes that serve as editable templates for elements of a xmgrace project. The inheritance structure of ``pygrace`` mirrors the structure of ``xmgrace``.
+``pygrace`` was designed to enable the construction and use of ``xmgrace`` projects from Python.  ``pygrace`` provides a collection of classes that serve as editable templates for elements of a xmgrace project. The inheritance structure of ``pygrace`` mirrors the structure of ``xmgrace``.
 
 ``pygrace`` ``Project`` objects are used to construct and save ``xmgrace`` project files (.agr). ``Project`` files capture the state of a ``xmgrace`` session, including the figures, settings, and current variables.
 
 .. image:: https://github.com/uqfoundation/pygrace/raw/master/docs/source/_static/crow_diagram.png
    :alt: pygrace project
 
 A more detailed diagram of all the attributes of ``pygrace`` template objects can be found at https://github.com/uqfoundation/pygrace/blob/master/docs/diagrams/diagram.pdf, while a handy cheatsheet of the methods and attributes of each ``pygrace`` template class can be found at https://github.com/uqfoundation/pygrace/blob/master/docs/diagrams/cheatsheet.pdf. This cheatsheet can be dynamically generated through use of the ``write_cheatsheet`` method, available from the ``Project`` class.
 
 ``pygrace`` is in active development, so any user feedback, bug reports, comments, or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pygrace/issues, with a legacy list maintained at https://github.com/pygrace/pygrace/issues.
 
 
 Major Features
 ==============
 
-``pygrace`` provides an object-oriented python interface for the efficient construction of ``xmgrace`` projects (e.g. highly-customizable publication-quality single and multi-figure plots). ``pygrace`` provides:
+``pygrace`` provides an object-oriented Python interface for the efficient construction of ``xmgrace`` projects (e.g. highly-customizable publication-quality single and multi-figure plots). ``pygrace`` provides:
 
-    - an object-relational mapping from python objects to a ``xmgrace`` project
-    - an interactive python-based ``grace>`` prompt for ``xmgrace`` commands
-    - a set of high-level python functions for drawing ``xmgrace`` ``Graphs``
+    - an object-relational mapping from Python objects to a ``xmgrace`` project
+    - an interactive Python-based ``grace>`` prompt for ``xmgrace`` commands
+    - a set of high-level Python functions for drawing ``xmgrace`` ``Graphs``
 
 Current Release
 ===============
 
 The latest released version of ``pygrace`` is available from:
 
     https://pypi.org/project/pygrace
@@ -162,15 +162,15 @@
 
 
 we can also work in an interactive xmgrace session::
 
     >>> from pygrace import grace
     >>> pg = grace()
 
-use xmgrace methods directly from the python interpreter::
+use xmgrace methods directly from the Python interpreter::
 
     >>> import numpy as np
     >>> x = np.arange(21) * np.pi/10
     >>> pg.plot(x, np.sin(x))
 
 .. image:: https://github.com/uqfoundation/pygrace/raw/master/docs/source/_static/sin.png
    :alt: sin
@@ -207,15 +207,15 @@
     >>> pg.who('x')
     array([0.        , 0.31415927, 0.62831853, 0.9424778 , 1.25663706,
            1.57079633, 1.88495559, 2.19911486, 2.51327412, 2.82743339,
            3.14159265, 3.45575192, 3.76991118, 4.08407045, 4.39822972,
            4.71238898, 5.02654825, 5.34070751, 5.65486678, 5.96902604,
            6.28318531])
 
-get variables back into python from xmgrace::
+get variables back into Python from xmgrace::
 
     >>> cosx = pg.get('y')
 
 use shortcuts for put, eval, and get::
 
     >>> pg.z = 0.5
     >>> pg('print(z)')
@@ -243,28 +243,29 @@
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://pygrace.rtfd.io. Also see ``pygrace.tests`` for a set of scripts that
-demonstrate several of the many features of ``pygrace``.
-You can run the test suite with ``python -m pygrace.tests``. 
-Also see ``pygrace.examples`` for examples that demonstrate the construction
-of ``xmgrace`` project files (.agr). ``pygrace.examples.interactive`` includes
-examples of using ``python`` to interact with a live ``xmgrace`` session.
-The source code is relatively well documented, so some questions may be resolved by inspecting the code itself.  However, please feel free to submit a ticket on github, or ask a question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pygrace`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+demonstrate several of the many features of ``pygrace``. You can run the test
+suite with ``python -m pygrace.tests``. Also see https://github.com/uqfoundation/pygrace/tree/master/examples for examples that demonstrate the construction
+of ``xmgrace`` project files (.agr). https://github.com/uqfoundation/pygrace/tree/master/examples/interactive includes examples of using ``python`` to interact
+with a live ``xmgrace`` session. The source code is relatively well documented,
+so some questions may be resolved by inspecting the code itself.  However,
+please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``pygrace`` in your work, please send an email (to **mmckerns at uqfoundation
+dot org**).
 
 
 Citation 
 ========
 
 If you use ``pygrace`` to do research that leads to publication, we ask that you
 acknowledge use of ``pygrace`` by citing the following in your publication::
 
     Michael McKerns, Dean Malmgren, Mike Stringer, and Daniel Stouffer,
-    "pygrace: python bindings to xmgrace", 2005- ;
+    "pygrace: Python bindings to xmgrace", 2005- ;
     https://github.com/uqfoundation/pygrace
 
 Please see https://pygrace.github.io/ for further information on an earlier version of ``pygrace`` developed by Dean Malmgren, Mike Stringer, and members of the Amaral Lab, and later maintained by Daniel Stouffer and members of the Stouffer Lab. This code has been merged into the original ``pygrace`` developed by Mike McKerns.
```

### Comparing `pygrace-1.2.1/pygrace.egg-info/SOURCES.txt` & `pygrace-1.3/pygrace.egg-info/SOURCES.txt`

 * *Files 0% similar despite different names*

```diff
@@ -31,14 +31,15 @@
 docs/source/_static/00_helloworld.png
 docs/source/_static/05_colorplot.png
 docs/source/_static/08_latexlabels.png
 docs/source/_static/cos.png
 docs/source/_static/crow_diagram.png
 docs/source/_static/histoPlot.png
 docs/source/_static/sin.png
+docs/source/_static/css/custom.css
 examples/00_helloworld.py
 examples/01_singleplot.py
 examples/02_multiplot.py
 examples/03_simplesubclass.py
 examples/04_classy.py
 examples/05_colorplot.py
 examples/06_logautoscale.py
```

### Comparing `pygrace-1.2.1/scripts/pygrace_cdf` & `pygrace-1.3/scripts/pygrace_cdf`

 * *Files identical despite different names*

### Comparing `pygrace-1.2.1/setup.py` & `pygrace-1.3/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -40,15 +40,15 @@
     Distribution = object
     has_setuptools = False
 
 # build the 'setup' call
 setup_kwds = dict(
     name='pygrace',
     version=__version__,
-    description='Python interface to xmgrace and xmgrace project files',
+    description='Python bindings to xmgrace',
     long_description = README.strip(),
     author = __author__,
     author_email = AUTHOR_EMAIL,
     maintainer = __author__,
     maintainer_email = AUTHOR_EMAIL,
     license = 'BSD-3-Clause',
     platforms = ['Linux', 'Mac'],
```

### Comparing `pygrace-1.2.1/tox.ini` & `pygrace-1.3/tox.ini`

 * *Files 19% similar despite different names*

```diff
@@ -7,14 +7,15 @@
     py39-numpy12
     py310-numpy12
     py311-numpy12
     py312-numpy12
     pypy37-numpy12
     pypy38-numpy12
     pypy39-numpy12
+    pypy310-numpy12
 
 [testenv]
 setenv =
     PYTHONHASHSEED = 0
     recreate = True
 basepython = 
     py37: python3.7
@@ -22,14 +23,15 @@
     py39: python3.9
     py310: python3.10
     py311: python3.11
     py312: python3.12
     pypy37: pypy37
     pypy38: pypy38
     pypy39: pypy39
+    pypy310: pypy310
 deps =
     numpy12: numpy>=1.0
 whitelist_externals =
 #   bash
 commands =
     {envpython} -m pip install .
     {envpython} pygrace/tests/__main__.py
```

### Comparing `pygrace-1.2.1/version.py` & `pygrace-1.3/version.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pygrace/blob/master/LICENSE
 
-__version__ = '1.2.1'
+__version__ = '1.3'
 __author__ = 'Mike McKerns'
 __contact__ = 'mmckerns@uqfoundation.org'
 
 
 def get_license_text(filepath):
     "open the LICENSE file and read the contents"
     try:
```

