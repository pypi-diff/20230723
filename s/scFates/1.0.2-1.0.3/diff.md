# Comparing `tmp/scFates-1.0.2.tar.gz` & `tmp/scFates-1.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "scFates-1.0.2.tar", last modified: Fri Apr 28 04:41:41 2023, max compression
+gzip compressed data, was "scFates-1.0.3.tar", last modified: Sun Jul 23 15:53:01 2023, max compression
```

## Comparing `scFates-1.0.2.tar` & `scFates-1.0.3.tar`

### file list

```diff
@@ -1,75 +1,75 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 04:41:41.503832 scFates-1.0.2/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 04:41:41.495832 scFates-1.0.2/.git/
--rw-r--r--   0 runner    (1001) docker     (123)     4037 2023-04-28 04:41:34.000000 scFates-1.0.2/.git/FETCH_HEAD
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-04-28 04:41:34.000000 scFates-1.0.2/.git/HEAD
--rw-r--r--   0 runner    (1001) docker     (123)      357 2023-04-28 04:41:31.000000 scFates-1.0.2/.git/config
--rwxr-xr-x   0 runner    (1001) docker     (123)       73 2023-04-28 04:41:31.000000 scFates-1.0.2/.git/description
--rw-r--r--   0 runner    (1001) docker     (123)     8179 2023-04-28 04:41:40.000000 scFates-1.0.2/.git/index
--rw-r--r--   0 runner    (1001) docker     (123)     1518 2023-04-28 04:41:34.000000 scFates-1.0.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       40 2023-04-28 04:41:34.000000 scFates-1.0.2/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     7243 2023-04-28 04:41:41.503832 scFates-1.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5983 2023-04-28 04:41:34.000000 scFates-1.0.2/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      298 2023-04-28 04:41:34.000000 scFates-1.0.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      377 2023-04-28 04:41:34.000000 scFates-1.0.2/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 04:41:41.495832 scFates-1.0.2/scFates/
--rw-r--r--   0 runner    (1001) docker     (123)      330 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 04:41:41.495832 scFates-1.0.2/scFates/datasets/
--rw-r--r--   0 runner    (1001) docker     (123)       93 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/datasets/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2421 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/datasets/_datasets.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 04:41:41.495832 scFates-1.0.2/scFates/get/
--rw-r--r--   0 runner    (1001) docker     (123)       49 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/get/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4706 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/get/get.py
--rw-r--r--   0 runner    (1001) docker     (123)     4770 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/logging.py
--rw-r--r--   0 runner    (1001) docker     (123)       27 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/pl.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 04:41:41.499832 scFates-1.0.2/scFates/plot/
--rw-r--r--   0 runner    (1001) docker     (123)      578 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3225 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/binned_pseudotime_meta.py
--rw-r--r--   0 runner    (1001) docker     (123)     2651 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/covariate.py
--rw-r--r--   0 runner    (1001) docker     (123)     3669 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/dendrogram.py
--rw-r--r--   0 runner    (1001) docker     (123)    26836 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/features.py
--rw-r--r--   0 runner    (1001) docker     (123)     1738 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/linearity_deviation.py
--rw-r--r--   0 runner    (1001) docker     (123)    11554 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/matrix.py
--rw-r--r--   0 runner    (1001) docker     (123)     3191 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/milestones.py
--rw-r--r--   0 runner    (1001) docker     (123)     4383 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/module_inclusion.py
--rw-r--r--   0 runner    (1001) docker     (123)     6127 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/modules.py
--rw-r--r--   0 runner    (1001) docker     (123)     6071 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/palette_tools.py
--rw-r--r--   0 runner    (1001) docker     (123)     3459 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/palettes.py
--rw-r--r--   0 runner    (1001) docker     (123)    11154 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/slide_cors.py
--rw-r--r--   0 runner    (1001) docker     (123)     6592 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/synchro_path.py
--rw-r--r--   0 runner    (1001) docker     (123)      675 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/test_association.py
--rw-r--r--   0 runner    (1001) docker     (123)     2186 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/test_fork.py
--rw-r--r--   0 runner    (1001) docker     (123)    23631 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/trajectory.py
--rw-r--r--   0 runner    (1001) docker     (123)     8744 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/plot/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)       36 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/pp.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 04:41:41.499832 scFates-1.0.2/scFates/preprocessing/
--rw-r--r--   0 runner    (1001) docker     (123)      102 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/preprocessing/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5667 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/preprocessing/diffusion.py
--rw-r--r--   0 runner    (1001) docker     (123)    12183 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/preprocessing/pagoda2.py
--rw-r--r--   0 runner    (1001) docker     (123)      935 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/settings.py
--rw-r--r--   0 runner    (1001) docker     (123)       28 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tl.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 04:41:41.503832 scFates-1.0.2/scFates/tools/
--rw-r--r--   0 runner    (1001) docker     (123)      900 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    25763 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/bifurcation_tools.py
--rw-r--r--   0 runner    (1001) docker     (123)     3426 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/cluster.py
--rw-r--r--   0 runner    (1001) docker     (123)     5499 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/conversion.py
--rw-r--r--   0 runner    (1001) docker     (123)    24925 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/correlation_tools.py
--rw-r--r--   0 runner    (1001) docker     (123)     9233 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/covariate.py
--rw-r--r--   0 runner    (1001) docker     (123)    15863 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/dendrogram.py
--rw-r--r--   0 runner    (1001) docker     (123)     6174 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/fit.py
--rw-r--r--   0 runner    (1001) docker     (123)    26318 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/graph_fitting.py
--rw-r--r--   0 runner    (1001) docker     (123)    23466 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/graph_operations.py
--rw-r--r--   0 runner    (1001) docker     (123)     5920 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/linearity_deviation.py
--rw-r--r--   0 runner    (1001) docker     (123)    16352 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/pseudotime.py
--rw-r--r--   0 runner    (1001) docker     (123)    12796 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/root.py
--rw-r--r--   0 runner    (1001) docker     (123)    12473 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/slide_cors.py
--rw-r--r--   0 runner    (1001) docker     (123)    13851 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/test_association.py
--rw-r--r--   0 runner    (1001) docker     (123)     6787 2023-04-28 04:41:34.000000 scFates-1.0.2/scFates/tools/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-28 04:41:41.495832 scFates-1.0.2/scFates.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     7243 2023-04-28 04:41:41.000000 scFates-1.0.2/scFates.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1591 2023-04-28 04:41:41.000000 scFates-1.0.2/scFates.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-28 04:41:41.000000 scFates-1.0.2/scFates.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-28 04:41:41.000000 scFates-1.0.2/scFates.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      377 2023-04-28 04:41:41.000000 scFates-1.0.2/scFates.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-04-28 04:41:41.000000 scFates-1.0.2/scFates.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-28 04:41:41.503832 scFates-1.0.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1383 2023-04-28 04:41:34.000000 scFates-1.0.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:53:01.735619 scFates-1.0.3/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:53:01.711619 scFates-1.0.3/.git/
+-rw-r--r--   0 runner    (1001) docker     (123)     4133 2023-07-23 15:52:51.000000 scFates-1.0.3/.git/FETCH_HEAD
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-23 15:52:51.000000 scFates-1.0.3/.git/HEAD
+-rw-r--r--   0 runner    (1001) docker     (123)      357 2023-07-23 15:52:48.000000 scFates-1.0.3/.git/config
+-rwxr-xr-x   0 runner    (1001) docker     (123)       73 2023-07-23 15:52:48.000000 scFates-1.0.3/.git/description
+-rw-r--r--   0 runner    (1001) docker     (123)     8179 2023-07-23 15:53:00.000000 scFates-1.0.3/.git/index
+-rw-r--r--   0 runner    (1001) docker     (123)     1518 2023-07-23 15:52:51.000000 scFates-1.0.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       40 2023-07-23 15:52:51.000000 scFates-1.0.3/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     7243 2023-07-23 15:53:01.735619 scFates-1.0.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5983 2023-07-23 15:52:51.000000 scFates-1.0.3/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      298 2023-07-23 15:52:51.000000 scFates-1.0.3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      377 2023-07-23 15:52:51.000000 scFates-1.0.3/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:53:01.715619 scFates-1.0.3/scFates/
+-rw-r--r--   0 runner    (1001) docker     (123)      330 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:53:01.719619 scFates-1.0.3/scFates/datasets/
+-rw-r--r--   0 runner    (1001) docker     (123)       93 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/datasets/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2421 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/datasets/_datasets.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:53:01.719619 scFates-1.0.3/scFates/get/
+-rw-r--r--   0 runner    (1001) docker     (123)       49 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/get/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4706 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/get/get.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4770 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/logging.py
+-rw-r--r--   0 runner    (1001) docker     (123)       27 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/pl.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:53:01.727619 scFates-1.0.3/scFates/plot/
+-rw-r--r--   0 runner    (1001) docker     (123)      578 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3225 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/binned_pseudotime_meta.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2651 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/covariate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3669 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/dendrogram.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26836 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/features.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1738 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/linearity_deviation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11554 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/matrix.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3191 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/milestones.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4383 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/module_inclusion.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6127 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/modules.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6071 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/palette_tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3459 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/palettes.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11154 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/slide_cors.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6592 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/synchro_path.py
+-rw-r--r--   0 runner    (1001) docker     (123)      675 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/test_association.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2186 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/test_fork.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23631 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/trajectory.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8744 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/plot/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)       36 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/pp.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:53:01.727619 scFates-1.0.3/scFates/preprocessing/
+-rw-r--r--   0 runner    (1001) docker     (123)      102 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/preprocessing/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5667 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/preprocessing/diffusion.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12183 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/preprocessing/pagoda2.py
+-rw-r--r--   0 runner    (1001) docker     (123)      935 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/settings.py
+-rw-r--r--   0 runner    (1001) docker     (123)       28 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tl.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:53:01.735619 scFates-1.0.3/scFates/tools/
+-rw-r--r--   0 runner    (1001) docker     (123)      900 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25763 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/bifurcation_tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3427 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/cluster.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5499 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/conversion.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24925 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/correlation_tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9233 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/covariate.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15863 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/dendrogram.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6174 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/fit.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26318 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/graph_fitting.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23466 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/graph_operations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5920 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/linearity_deviation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16352 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/pseudotime.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12796 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/root.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12473 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/slide_cors.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13851 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/test_association.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6787 2023-07-23 15:52:51.000000 scFates-1.0.3/scFates/tools/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:53:01.719619 scFates-1.0.3/scFates.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     7243 2023-07-23 15:53:01.000000 scFates-1.0.3/scFates.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1591 2023-07-23 15:53:01.000000 scFates-1.0.3/scFates.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 15:53:01.000000 scFates-1.0.3/scFates.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 15:53:01.000000 scFates-1.0.3/scFates.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      377 2023-07-23 15:53:01.000000 scFates-1.0.3/scFates.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-23 15:53:01.000000 scFates-1.0.3/scFates.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 15:53:01.735619 scFates-1.0.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1383 2023-07-23 15:52:51.000000 scFates-1.0.3/setup.py
```

### Comparing `scFates-1.0.2/.git/FETCH_HEAD` & `scFates-1.0.3/.git/FETCH_HEAD`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 e4fac12ae38b9bb4565871f49f4a849679fc26cc		branch 'dev' of https://github.com/LouisFaure/scFates
 9b9d74b16117809e950be566092b65d022bc0cbd		branch 'linecount' of https://github.com/LouisFaure/scFates
-be90fd511f3190d3636deadf4a73d111e01bebc0		branch 'master' of https://github.com/LouisFaure/scFates
+002f7abf97681cfe5ef0905a078362189ab8e888		branch 'master' of https://github.com/LouisFaure/scFates
 0b82601658eff1b96251232ca58a882ac4be93b8		branch 'v0.2.2dev' of https://github.com/LouisFaure/scFates
 3ea1889f03309e73dd252d0b26faff07bc9a33f0		branch 'v0.2.3dev' of https://github.com/LouisFaure/scFates
 1f99b3d34b9a66e528d4b7704dfa6b210186fa14		branch 'v0.2.4dev' of https://github.com/LouisFaure/scFates
 7c5c19ba9c082136f1d3fea1d7178c0e7b3c41a6		branch 'v0.2.5dev' of https://github.com/LouisFaure/scFates
 b5d12d54deb5709c1a8ba0a549b11a60be499052		branch 'v0.2.6dev' of https://github.com/LouisFaure/scFates
 5a0795e8fb30316fd6d1015b644362103a277c94		branch 'v0.2.7dev' of https://github.com/LouisFaure/scFates
 079a1e36997ad9edf89d4f5bd6c10b79db73f8a6		branch 'v0.3.0dev' of https://github.com/LouisFaure/scFates
@@ -35,7 +35,8 @@
 f3d71daaedb1edf74a1096a4bad147349432480a		tag 'v0.8.0' of https://github.com/LouisFaure/scFates
 fe0af4fff73fa68f48f83ce351e66203fa613b18		tag 'v0.8.1' of https://github.com/LouisFaure/scFates
 d17aceb4b5284ffa148454108547ea684d075b82		tag 'v0.9.0' of https://github.com/LouisFaure/scFates
 cd5b51394f5295ea88b21a5475d0d138ac085307		tag 'v0.9.1' of https://github.com/LouisFaure/scFates
 975763811789135b3bb54cf87e6e1a0b53675d77		tag 'v1.0.0' of https://github.com/LouisFaure/scFates
 ea40f4240997a21f22c49ef223dd05aa705a0f2d		tag 'v1.0.1' of https://github.com/LouisFaure/scFates
 be90fd511f3190d3636deadf4a73d111e01bebc0		tag 'v1.0.2' of https://github.com/LouisFaure/scFates
+002f7abf97681cfe5ef0905a078362189ab8e888		tag 'v1.0.3' of https://github.com/LouisFaure/scFates
```

### Comparing `scFates-1.0.2/LICENSE` & `scFates-1.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/PKG-INFO` & `scFates-1.0.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: scFates
-Version: 1.0.2
+Version: 1.0.3
 Summary: scanpy compatible python suite for fast tree inference and advanced pseudotime downstream analysis
 Home-page: https://github.com/LouisFaure/scFates
 Author: Louis Faure
 Author-email: 
 License: UNKNOWN
 Description: [![PyPI](https://img.shields.io/pypi/v/scFates.svg)](https://pypi.python.org/pypi/scFates/)
         [![DOI](https://img.shields.io/badge/DOI-10.1093/bioinformatics/btac746-blue)](https://doi.org/10.1093/bioinformatics/btac746)
```

### Comparing `scFates-1.0.2/README.md` & `scFates-1.0.3/README.md`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/datasets/_datasets.py` & `scFates-1.0.3/scFates/datasets/_datasets.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/get/get.py` & `scFates-1.0.3/scFates/get/get.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/logging.py` & `scFates-1.0.3/scFates/logging.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/__init__.py` & `scFates-1.0.3/scFates/plot/__init__.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/binned_pseudotime_meta.py` & `scFates-1.0.3/scFates/plot/binned_pseudotime_meta.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/covariate.py` & `scFates-1.0.3/scFates/plot/covariate.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/dendrogram.py` & `scFates-1.0.3/scFates/plot/dendrogram.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/features.py` & `scFates-1.0.3/scFates/plot/features.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/linearity_deviation.py` & `scFates-1.0.3/scFates/plot/linearity_deviation.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/matrix.py` & `scFates-1.0.3/scFates/plot/matrix.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/milestones.py` & `scFates-1.0.3/scFates/plot/milestones.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/module_inclusion.py` & `scFates-1.0.3/scFates/plot/module_inclusion.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/modules.py` & `scFates-1.0.3/scFates/plot/modules.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/palette_tools.py` & `scFates-1.0.3/scFates/plot/palette_tools.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/palettes.py` & `scFates-1.0.3/scFates/plot/palettes.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/slide_cors.py` & `scFates-1.0.3/scFates/plot/slide_cors.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/synchro_path.py` & `scFates-1.0.3/scFates/plot/synchro_path.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/test_association.py` & `scFates-1.0.3/scFates/plot/test_association.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/test_fork.py` & `scFates-1.0.3/scFates/plot/test_fork.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/trajectory.py` & `scFates-1.0.3/scFates/plot/trajectory.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/plot/utils.py` & `scFates-1.0.3/scFates/plot/utils.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/preprocessing/diffusion.py` & `scFates-1.0.3/scFates/preprocessing/diffusion.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/preprocessing/pagoda2.py` & `scFates-1.0.3/scFates/preprocessing/pagoda2.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/settings.py` & `scFates-1.0.3/scFates/settings.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/__init__.py` & `scFates-1.0.3/scFates/tools/__init__.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/bifurcation_tools.py` & `scFates-1.0.3/scFates/tools/bifurcation_tools.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/cluster.py` & `scFates-1.0.3/scFates/tools/cluster.py`

 * *Files 1% similar despite different names*

```diff
@@ -111,11 +111,11 @@
         adata_s.obs["leiden"] = pd.Categorical(
             values=groups.astype("U"),
             categories=natsorted(map(str, np.unique(groups))),
         )
     else:
         sc.tl.leiden(adata_s, resolution=resolution)
 
-    adata.var["cluters"] = adata_s.obs.leiden
+    adata.var["clusters"] = adata_s.obs.leiden
 
     logg.info("    finished", time=True, end=" " if settings.verbosity > 2 else "\n")
     logg.hint("added \n" "    .var['cluters'] identified modules.")
```

### Comparing `scFates-1.0.2/scFates/tools/conversion.py` & `scFates-1.0.3/scFates/tools/conversion.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/correlation_tools.py` & `scFates-1.0.3/scFates/tools/correlation_tools.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/covariate.py` & `scFates-1.0.3/scFates/tools/covariate.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/dendrogram.py` & `scFates-1.0.3/scFates/tools/dendrogram.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/fit.py` & `scFates-1.0.3/scFates/tools/fit.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/graph_fitting.py` & `scFates-1.0.3/scFates/tools/graph_fitting.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/graph_operations.py` & `scFates-1.0.3/scFates/tools/graph_operations.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/linearity_deviation.py` & `scFates-1.0.3/scFates/tools/linearity_deviation.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/pseudotime.py` & `scFates-1.0.3/scFates/tools/pseudotime.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/root.py` & `scFates-1.0.3/scFates/tools/root.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/slide_cors.py` & `scFates-1.0.3/scFates/tools/slide_cors.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/test_association.py` & `scFates-1.0.3/scFates/tools/test_association.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates/tools/utils.py` & `scFates-1.0.3/scFates/tools/utils.py`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/scFates.egg-info/PKG-INFO` & `scFates-1.0.3/scFates.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: scFates
-Version: 1.0.2
+Version: 1.0.3
 Summary: scanpy compatible python suite for fast tree inference and advanced pseudotime downstream analysis
 Home-page: https://github.com/LouisFaure/scFates
 Author: Louis Faure
 Author-email: 
 License: UNKNOWN
 Description: [![PyPI](https://img.shields.io/pypi/v/scFates.svg)](https://pypi.python.org/pypi/scFates/)
         [![DOI](https://img.shields.io/badge/DOI-10.1093/bioinformatics/btac746-blue)](https://doi.org/10.1093/bioinformatics/btac746)
```

### Comparing `scFates-1.0.2/scFates.egg-info/SOURCES.txt` & `scFates-1.0.3/scFates.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `scFates-1.0.2/setup.py` & `scFates-1.0.3/setup.py`

 * *Files identical despite different names*

