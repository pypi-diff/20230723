# Comparing `tmp/dantro-0.19.1.tar.gz` & `tmp/dantro-0.19.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dantro-0.19.1.tar", last modified: Tue Jul 18 11:59:50 2023, max compression
+gzip compressed data, was "dantro-0.19.2.tar", last modified: Sun Jul 23 15:19:22 2023, max compression
```

## Comparing `dantro-0.19.1.tar` & `dantro-0.19.2.tar`

### file list

```diff
@@ -1,109 +1,109 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.521653 dantro-0.19.1/
--rw-rw-rw-   0 root         (0) root         (0)    35149 2023-07-18 11:59:39.000000 dantro-0.19.1/COPYING
--rw-rw-rw-   0 root         (0) root         (0)     7633 2023-07-18 11:59:39.000000 dantro-0.19.1/COPYING.LESSER
--rw-r--r--   0 root         (0) root         (0)     3269 2023-07-18 11:59:50.521653 dantro-0.19.1/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)    15686 2023-07-18 11:59:39.000000 dantro-0.19.1/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.507653 dantro-0.19.1/dantro/
--rw-rw-rw-   0 root         (0) root         (0)     1005 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)      889 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/_copy.py
--rw-rw-rw-   0 root         (0) root         (0)    30886 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/_dag_utils.py
--rw-rw-rw-   0 root         (0) root         (0)      922 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/_hash.py
--rw-rw-rw-   0 root         (0) root         (0)    14740 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/_import_tools.py
--rw-rw-rw-   0 root         (0) root         (0)     7267 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/_registry.py
--rw-rw-rw-   0 root         (0) root         (0)     9390 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/_yaml.py
--rw-rw-rw-   0 root         (0) root         (0)    15796 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/abc.py
--rw-rw-rw-   0 root         (0) root         (0)    44192 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/base.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.508653 dantro-0.19.1/dantro/cfg/
--rw-rw-rw-   0 root         (0) root         (0)    22040 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/cfg/base_plots.yml
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.510653 dantro-0.19.1/dantro/containers/
--rw-rw-rw-   0 root         (0) root         (0)      545 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/containers/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     3675 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/containers/_registry.py
--rw-rw-rw-   0 root         (0) root         (0)     3223 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/containers/general.py
--rw-rw-rw-   0 root         (0) root         (0)     1302 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/containers/link.py
--rw-rw-rw-   0 root         (0) root         (0)     3409 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/containers/numeric.py
--rw-rw-rw-   0 root         (0) root         (0)     3489 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/containers/path.py
--rw-rw-rw-   0 root         (0) root         (0)    13561 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/containers/xr.py
--rw-rw-rw-   0 root         (0) root         (0)   131976 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/dag.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.512653 dantro-0.19.1/dantro/data_loaders/
--rw-rw-rw-   0 root         (0) root         (0)     2963 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_loaders/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     6739 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_loaders/_registry.py
--rw-rw-rw-   0 root         (0) root         (0)     3786 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_loaders/fspath.py
--rw-rw-rw-   0 root         (0) root         (0)    19584 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_loaders/hdf5.py
--rw-rw-rw-   0 root         (0) root         (0)     2009 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_loaders/numpy.py
--rw-rw-rw-   0 root         (0) root         (0)     4230 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_loaders/pandas.py
--rw-rw-rw-   0 root         (0) root         (0)     1180 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_loaders/pickle.py
--rw-rw-rw-   0 root         (0) root         (0)      993 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_loaders/text.py
--rw-rw-rw-   0 root         (0) root         (0)     3442 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_loaders/xarray.py
--rw-rw-rw-   0 root         (0) root         (0)     2165 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_loaders/yaml.py
--rw-rw-rw-   0 root         (0) root         (0)    64943 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_mngr.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.513653 dantro-0.19.1/dantro/data_ops/
--rw-rw-rw-   0 root         (0) root         (0)      454 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_ops/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     1817 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_ops/_base_ops.py
--rw-rw-rw-   0 root         (0) root         (0)     2807 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_ops/apply.py
--rw-rw-rw-   0 root         (0) root         (0)    28398 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_ops/arr_ops.py
--rw-rw-rw-   0 root         (0) root         (0)     2716 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_ops/ctrl_ops.py
--rw-rw-rw-   0 root         (0) root         (0)    16700 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_ops/db.py
--rw-rw-rw-   0 root         (0) root         (0)     8250 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_ops/db_tools.py
--rw-rw-rw-   0 root         (0) root         (0)     9010 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_ops/expr_ops.py
--rw-rw-rw-   0 root         (0) root         (0)     3947 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/data_ops/hooks.py
--rw-rw-rw-   0 root         (0) root         (0)    12931 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/exceptions.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.515653 dantro-0.19.1/dantro/groups/
--rw-rw-rw-   0 root         (0) root         (0)      601 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/groups/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     3497 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/groups/_registry.py
--rw-rw-rw-   0 root         (0) root         (0)     2787 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/groups/dirpath.py
--rw-rw-rw-   0 root         (0) root         (0)    38203 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/groups/graph.py
--rw-rw-rw-   0 root         (0) root         (0)    46441 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/groups/labelled.py
--rw-rw-rw-   0 root         (0) root         (0)     5143 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/groups/ordered.py
--rw-rw-rw-   0 root         (0) root         (0)    25069 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/groups/psp.py
--rw-rw-rw-   0 root         (0) root         (0)     2500 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/groups/time_series.py
--rw-rw-rw-   0 root         (0) root         (0)     1899 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/logging.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.516653 dantro-0.19.1/dantro/mixins/
--rw-rw-rw-   0 root         (0) root         (0)      613 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/mixins/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)    13225 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/mixins/base.py
--rw-rw-rw-   0 root         (0) root         (0)     3054 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/mixins/general.py
--rw-rw-rw-   0 root         (0) root         (0)     6696 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/mixins/indexing.py
--rw-rw-rw-   0 root         (0) root         (0)     7862 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/mixins/numeric.py
--rw-rw-rw-   0 root         (0) root         (0)     7694 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/mixins/proxy_support.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.517653 dantro-0.19.1/dantro/plot/
--rw-rw-rw-   0 root         (0) root         (0)      295 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)    10615 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/_cfg.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.517653 dantro-0.19.1/dantro/plot/creators/
--rw-rw-rw-   0 root         (0) root         (0)      556 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/creators/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)    45845 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/creators/base.py
--rw-rw-rw-   0 root         (0) root         (0)    37576 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/creators/psp.py
--rw-rw-rw-   0 root         (0) root         (0)    24018 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/creators/pyplot.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.519653 dantro-0.19.1/dantro/plot/funcs/
--rw-rw-rw-   0 root         (0) root         (0)      248 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/funcs/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)    10598 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/funcs/_multiplot.py
--rw-rw-rw-   0 root         (0) root         (0)     2886 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/funcs/_utils.py
--rw-rw-rw-   0 root         (0) root         (0)     1445 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/funcs/basic.py
--rw-rw-rw-   0 root         (0) root         (0)    53862 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/funcs/generic.py
--rw-rw-rw-   0 root         (0) root         (0)     9313 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/funcs/graph.py
--rw-rw-rw-   0 root         (0) root         (0)     6939 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/funcs/multiplot.py
--rw-rw-rw-   0 root         (0) root         (0)    90275 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/plot_helper.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.520653 dantro-0.19.1/dantro/plot/utils/
--rw-rw-rw-   0 root         (0) root         (0)      220 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/utils/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     3870 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/utils/_file_writer.py
--rw-rw-rw-   0 root         (0) root         (0)    41637 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/utils/color_mngr.py
--rw-rw-rw-   0 root         (0) root         (0)    11758 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/utils/mpl.py
--rw-rw-rw-   0 root         (0) root         (0)    13223 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot/utils/plot_func.py
--rw-rw-rw-   0 root         (0) root         (0)    58440 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/plot_mngr.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.520653 dantro-0.19.1/dantro/proxy/
--rw-rw-rw-   0 root         (0) root         (0)      142 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/proxy/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)     6545 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/proxy/hdf5.py
--rw-rw-rw-   0 root         (0) root         (0)    23632 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/tools.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.521653 dantro-0.19.1/dantro/utils/
--rw-rw-rw-   0 root         (0) root         (0)      315 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/utils/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)    21012 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/utils/coords.py
--rw-rw-rw-   0 root         (0) root         (0)     7146 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/utils/link.py
--rw-rw-rw-   0 root         (0) root         (0)    15838 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/utils/nx.py
--rw-rw-rw-   0 root         (0) root         (0)    16382 2023-07-18 11:59:39.000000 dantro-0.19.1/dantro/utils/ordereddict.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-18 11:59:50.508653 dantro-0.19.1/dantro.egg-info/
--rw-r--r--   0 root         (0) root         (0)     3269 2023-07-18 11:59:50.000000 dantro-0.19.1/dantro.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     2301 2023-07-18 11:59:50.000000 dantro-0.19.1/dantro.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-07-18 11:59:50.000000 dantro-0.19.1/dantro.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)      375 2023-07-18 11:59:50.000000 dantro-0.19.1/dantro.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)        7 2023-07-18 11:59:50.000000 dantro-0.19.1/dantro.egg-info/top_level.txt
--rw-rw-rw-   0 root         (0) root         (0)     1723 2023-07-18 11:59:39.000000 dantro-0.19.1/pyproject.toml
--rw-r--r--   0 root         (0) root         (0)       38 2023-07-18 11:59:50.521653 dantro-0.19.1/setup.cfg
--rw-rw-rw-   0 root         (0) root         (0)     6068 2023-07-18 11:59:39.000000 dantro-0.19.1/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.557327 dantro-0.19.2/
+-rw-rw-rw-   0 root         (0) root         (0)    35149 2023-07-23 15:19:12.000000 dantro-0.19.2/COPYING
+-rw-rw-rw-   0 root         (0) root         (0)     7633 2023-07-23 15:19:12.000000 dantro-0.19.2/COPYING.LESSER
+-rw-r--r--   0 root         (0) root         (0)     3269 2023-07-23 15:19:22.557327 dantro-0.19.2/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)    15802 2023-07-23 15:19:12.000000 dantro-0.19.2/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.542327 dantro-0.19.2/dantro/
+-rw-rw-rw-   0 root         (0) root         (0)     1005 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      889 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/_copy.py
+-rw-rw-rw-   0 root         (0) root         (0)    30886 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/_dag_utils.py
+-rw-rw-rw-   0 root         (0) root         (0)      922 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/_hash.py
+-rw-rw-rw-   0 root         (0) root         (0)    14740 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/_import_tools.py
+-rw-rw-rw-   0 root         (0) root         (0)     7267 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/_registry.py
+-rw-rw-rw-   0 root         (0) root         (0)     4012 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/_yaml.py
+-rw-rw-rw-   0 root         (0) root         (0)    15796 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/abc.py
+-rw-rw-rw-   0 root         (0) root         (0)    44192 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/base.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.543327 dantro-0.19.2/dantro/cfg/
+-rw-rw-rw-   0 root         (0) root         (0)    22040 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/cfg/base_plots.yml
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.545327 dantro-0.19.2/dantro/containers/
+-rw-rw-rw-   0 root         (0) root         (0)      545 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/containers/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     3675 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/containers/_registry.py
+-rw-rw-rw-   0 root         (0) root         (0)     3223 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/containers/general.py
+-rw-rw-rw-   0 root         (0) root         (0)     1302 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/containers/link.py
+-rw-rw-rw-   0 root         (0) root         (0)     3409 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/containers/numeric.py
+-rw-rw-rw-   0 root         (0) root         (0)     3489 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/containers/path.py
+-rw-rw-rw-   0 root         (0) root         (0)    13561 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/containers/xr.py
+-rw-rw-rw-   0 root         (0) root         (0)   131976 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/dag.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.547327 dantro-0.19.2/dantro/data_loaders/
+-rw-rw-rw-   0 root         (0) root         (0)     2963 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_loaders/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     6700 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_loaders/_registry.py
+-rw-rw-rw-   0 root         (0) root         (0)     3786 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_loaders/fspath.py
+-rw-rw-rw-   0 root         (0) root         (0)    19584 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_loaders/hdf5.py
+-rw-rw-rw-   0 root         (0) root         (0)     2009 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_loaders/numpy.py
+-rw-rw-rw-   0 root         (0) root         (0)     4230 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_loaders/pandas.py
+-rw-rw-rw-   0 root         (0) root         (0)     1180 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_loaders/pickle.py
+-rw-rw-rw-   0 root         (0) root         (0)      993 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_loaders/text.py
+-rw-rw-rw-   0 root         (0) root         (0)     3442 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_loaders/xarray.py
+-rw-rw-rw-   0 root         (0) root         (0)     2150 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_loaders/yaml.py
+-rw-rw-rw-   0 root         (0) root         (0)    64940 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_mngr.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.548327 dantro-0.19.2/dantro/data_ops/
+-rw-rw-rw-   0 root         (0) root         (0)      454 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_ops/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     1817 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_ops/_base_ops.py
+-rw-rw-rw-   0 root         (0) root         (0)     2807 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_ops/apply.py
+-rw-rw-rw-   0 root         (0) root         (0)    28398 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_ops/arr_ops.py
+-rw-rw-rw-   0 root         (0) root         (0)     2716 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_ops/ctrl_ops.py
+-rw-rw-rw-   0 root         (0) root         (0)    16700 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_ops/db.py
+-rw-rw-rw-   0 root         (0) root         (0)     8250 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_ops/db_tools.py
+-rw-rw-rw-   0 root         (0) root         (0)     9010 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_ops/expr_ops.py
+-rw-rw-rw-   0 root         (0) root         (0)     3947 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/data_ops/hooks.py
+-rw-rw-rw-   0 root         (0) root         (0)    12058 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/exceptions.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.550327 dantro-0.19.2/dantro/groups/
+-rw-rw-rw-   0 root         (0) root         (0)      601 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/groups/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     3497 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/groups/_registry.py
+-rw-rw-rw-   0 root         (0) root         (0)     2787 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/groups/dirpath.py
+-rw-rw-rw-   0 root         (0) root         (0)    38203 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/groups/graph.py
+-rw-rw-rw-   0 root         (0) root         (0)    46441 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/groups/labelled.py
+-rw-rw-rw-   0 root         (0) root         (0)     5143 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/groups/ordered.py
+-rw-rw-rw-   0 root         (0) root         (0)    25069 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/groups/psp.py
+-rw-rw-rw-   0 root         (0) root         (0)     2500 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/groups/time_series.py
+-rw-rw-rw-   0 root         (0) root         (0)     1899 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/logging.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.551327 dantro-0.19.2/dantro/mixins/
+-rw-rw-rw-   0 root         (0) root         (0)      613 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/mixins/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)    13225 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/mixins/base.py
+-rw-rw-rw-   0 root         (0) root         (0)     3054 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/mixins/general.py
+-rw-rw-rw-   0 root         (0) root         (0)     6696 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/mixins/indexing.py
+-rw-rw-rw-   0 root         (0) root         (0)     7862 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/mixins/numeric.py
+-rw-rw-rw-   0 root         (0) root         (0)     7694 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/mixins/proxy_support.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.552327 dantro-0.19.2/dantro/plot/
+-rw-rw-rw-   0 root         (0) root         (0)      295 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)    10615 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/_cfg.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.553327 dantro-0.19.2/dantro/plot/creators/
+-rw-rw-rw-   0 root         (0) root         (0)      556 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/creators/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)    45845 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/creators/base.py
+-rw-rw-rw-   0 root         (0) root         (0)    37576 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/creators/psp.py
+-rw-rw-rw-   0 root         (0) root         (0)    24018 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/creators/pyplot.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.554327 dantro-0.19.2/dantro/plot/funcs/
+-rw-rw-rw-   0 root         (0) root         (0)      248 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/funcs/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)    10598 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/funcs/_multiplot.py
+-rw-rw-rw-   0 root         (0) root         (0)     2886 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/funcs/_utils.py
+-rw-rw-rw-   0 root         (0) root         (0)     1445 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/funcs/basic.py
+-rw-rw-rw-   0 root         (0) root         (0)    53862 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/funcs/generic.py
+-rw-rw-rw-   0 root         (0) root         (0)     9313 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/funcs/graph.py
+-rw-rw-rw-   0 root         (0) root         (0)     6939 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/funcs/multiplot.py
+-rw-rw-rw-   0 root         (0) root         (0)    90275 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/plot_helper.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.555327 dantro-0.19.2/dantro/plot/utils/
+-rw-rw-rw-   0 root         (0) root         (0)      220 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/utils/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     3870 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/utils/_file_writer.py
+-rw-rw-rw-   0 root         (0) root         (0)    41637 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/utils/color_mngr.py
+-rw-rw-rw-   0 root         (0) root         (0)    11758 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/utils/mpl.py
+-rw-rw-rw-   0 root         (0) root         (0)    13223 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot/utils/plot_func.py
+-rw-rw-rw-   0 root         (0) root         (0)    58440 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/plot_mngr.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.556327 dantro-0.19.2/dantro/proxy/
+-rw-rw-rw-   0 root         (0) root         (0)      142 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/proxy/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     6545 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/proxy/hdf5.py
+-rw-rw-rw-   0 root         (0) root         (0)    23632 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/tools.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.557327 dantro-0.19.2/dantro/utils/
+-rw-rw-rw-   0 root         (0) root         (0)      315 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/utils/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)    21012 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/utils/coords.py
+-rw-rw-rw-   0 root         (0) root         (0)     7146 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/utils/link.py
+-rw-rw-rw-   0 root         (0) root         (0)    15838 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/utils/nx.py
+-rw-rw-rw-   0 root         (0) root         (0)    16382 2023-07-23 15:19:12.000000 dantro-0.19.2/dantro/utils/ordereddict.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:19:22.543327 dantro-0.19.2/dantro.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     3269 2023-07-23 15:19:22.000000 dantro-0.19.2/dantro.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     2301 2023-07-23 15:19:22.000000 dantro-0.19.2/dantro.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-07-23 15:19:22.000000 dantro-0.19.2/dantro.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)      382 2023-07-23 15:19:22.000000 dantro-0.19.2/dantro.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)        7 2023-07-23 15:19:22.000000 dantro-0.19.2/dantro.egg-info/top_level.txt
+-rw-rw-rw-   0 root         (0) root         (0)     1723 2023-07-23 15:19:12.000000 dantro-0.19.2/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-07-23 15:19:22.557327 dantro-0.19.2/setup.cfg
+-rw-rw-rw-   0 root         (0) root         (0)     6115 2023-07-23 15:19:12.000000 dantro-0.19.2/setup.py
```

### Comparing `dantro-0.19.1/COPYING` & `dantro-0.19.2/COPYING`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/COPYING.LESSER` & `dantro-0.19.2/COPYING.LESSER`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/PKG-INFO` & `dantro-0.19.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dantro
-Version: 0.19.1
+Version: 0.19.2
 Summary: Handle, transform, and visualize hierarchically structured data
 Home-page: https://gitlab.com/utopia-project/dantro
 Author: dantro developers
 Author-email: dantro-dev@iup.uni.heidelberg.de
 License: LGPL-3.0-or-later
 Classifier: Intended Audience :: Science/Research
 Classifier: Programming Language :: Python :: 3.8
```

### Comparing `dantro-0.19.1/README.md` & `dantro-0.19.2/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -73,14 +73,15 @@
 | [h5netcdf][h5netcdf]          | h5py-based netcdf backend |
 | [matplotlib][matplotlib]      | For data visualization |
 | [seaborn][seaborn]            | For advanced data visualization |
 | [networkx][networkx]          | For network visualization |
 | [dill][dill]                  | For advanced pickling |
 | [ruamel.yaml][ruamelyaml]     | For parsing YAML configuration files |
 | [paramspace][paramspace]      | For dictionary- or YAML-based parameter spaces |
+| [yayaml][yayaml]              | Working conveniently with YAML files |
 
 If not specified further, dantro does not impose lower or upper bounds on package versions.
 Effectively, dantro works with the latest versions of all dependencies and the scheduled CI jobs make sure that combination continues working.
 
 In case you have trouble with dependencies, make sure you have the most recent version of dantro installed.
 
 
@@ -302,14 +303,15 @@
 [sympy]: https://www.sympy.org/
 [matplotlib]: https://matplotlib.org
 [seaborn]: https://seaborn.pydata.org
 [networkx]: https://networkx.github.io
 [ruamelyaml]: https://yaml.readthedocs.io/en/latest/
 [dill]: https://pypi.org/project/dill/
 [paramspace]: https://pypi.org/project/paramspace/
+[yayaml]: https://pypi.org/project/yayaml/
 
 [pytest]: https://pytest.org/en/latest/
 [pytest-cov]: https://pytest-cov.readthedocs.io/en/latest/
 [tox]: https://tox.readthedocs.io/en/latest/
 [sphinx]: https://www.sphinx-doc.org/
 [sphinx-book-theme]: https://sphinx-book-theme.readthedocs.io/en/latest/
 [pre-commit]: https://pre-commit.com
```

### Comparing `dantro-0.19.1/dantro/__init__.py` & `dantro-0.19.2/dantro/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 
 Together, these stages constitute a **data processing pipeline**:
 an automated sequence of predefined, configurable operations.
 
 See :ref:`the user manual <welcome>` for more information.
 """
 
-__version__ = "0.19.1"
+__version__ = "0.19.2"
 """Package version"""
 
 # Set up the root logger such that the logging configuration is applied
 from .logging import getLogger as _getLogger
 
 _log = _getLogger(__name__)
```

### Comparing `dantro-0.19.1/dantro/_copy.py` & `dantro-0.19.2/dantro/_copy.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/_dag_utils.py` & `dantro-0.19.2/dantro/_dag_utils.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/_hash.py` & `dantro-0.19.2/dantro/_hash.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/_import_tools.py` & `dantro-0.19.2/dantro/_import_tools.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/_registry.py` & `dantro-0.19.2/dantro/_registry.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/abc.py` & `dantro-0.19.2/dantro/abc.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/base.py` & `dantro-0.19.2/dantro/base.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/cfg/base_plots.yml` & `dantro-0.19.2/dantro/cfg/base_plots.yml`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/containers/__init__.py` & `dantro-0.19.2/dantro/containers/__init__.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/containers/_registry.py` & `dantro-0.19.2/dantro/containers/_registry.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/containers/general.py` & `dantro-0.19.2/dantro/containers/general.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/containers/link.py` & `dantro-0.19.2/dantro/containers/link.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/containers/numeric.py` & `dantro-0.19.2/dantro/containers/numeric.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/containers/path.py` & `dantro-0.19.2/dantro/containers/path.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/containers/xr.py` & `dantro-0.19.2/dantro/containers/xr.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/dag.py` & `dantro-0.19.2/dantro/dag.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_loaders/__init__.py` & `dantro-0.19.2/dantro/data_loaders/__init__.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_loaders/_registry.py` & `dantro-0.19.2/dantro/data_loaders/_registry.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,17 +1,16 @@
 """Implements registration of data loaders, including a decorator to ensure
 correct loader function signature (which also automatically keeps track of the
 data loader function).
 """
 
 import logging
-from typing import Any, Dict, Optional, Union
+from typing import Callable, List
 
 from .._registry import ObjectRegistry as _ObjectRegistry
-from ..exceptions import *
 
 log = logging.getLogger(__name__)
 
 LOAD_FUNC_PREFIX: str = "_load_"
 """The prefix that all load functions need to start with"""
 
 # -----------------------------------------------------------------------------
```

### Comparing `dantro-0.19.1/dantro/data_loaders/fspath.py` & `dantro-0.19.2/dantro/data_loaders/fspath.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_loaders/hdf5.py` & `dantro-0.19.2/dantro/data_loaders/hdf5.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_loaders/numpy.py` & `dantro-0.19.2/dantro/data_loaders/numpy.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_loaders/pandas.py` & `dantro-0.19.2/dantro/data_loaders/pandas.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_loaders/pickle.py` & `dantro-0.19.2/dantro/data_loaders/pickle.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_loaders/text.py` & `dantro-0.19.2/dantro/data_loaders/text.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_loaders/xarray.py` & `dantro-0.19.2/dantro/data_loaders/xarray.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_loaders/yaml.py` & `dantro-0.19.2/dantro/data_loaders/yaml.py`

 * *Files 13% similar despite different names*

```diff
@@ -10,49 +10,49 @@
 
 # -----------------------------------------------------------------------------
 
 
 class YamlLoaderMixin:
     """Supplies functionality to load YAML files in the
     :py:class:`~dantro.data_mngr.DataManager`.
-    Uses the :py:func:`dantro._yaml.load_yml` function for loading the files.
+    Uses the :py:func:`yayaml.io.load_yml` function for loading the files.
     """
 
     @add_loader(TargetCls=MutableMappingContainer, register_aliases=["yml"])
     def _load_yaml(
         filepath: str, *, TargetCls: type, **load_kwargs
     ) -> MutableMappingContainer:
         """Load a YAML file from the given path and create a container to
         store that data in.
-        Uses the :py:func:`dantro._yaml.load_yml` function for loading.
+        Uses the :py:func:`yayaml.io.load_yml` function for loading.
 
         Args:
             filepath (str): Where to load the YAML file from
             TargetCls (type): The class constructor
-            **load_kwargs: Passed on to :py:func:`dantro._yaml.load_yml`
+            **load_kwargs: Passed on to :py:func:`yayaml.io.load_yml`
 
         Returns
             MutableMappingContainer: The loaded YAML content as a container
         """
         d = load_yml(filepath, **load_kwargs)
         return TargetCls(data=d, attrs=dict(filepath=filepath))
 
     @add_loader(TargetCls=ObjectContainer, register_aliases=["yml_to_object"])
     def _load_yaml_to_object(
         filepath: str, *, TargetCls: type, **load_kwargs
     ) -> ObjectContainer:
         """Load a YAML file from the given path and create a container to
         store that data in.
 
-        Uses the :py:func:`dantro._yaml.load_yml` function for loading.
+        Uses the :py:func:`yayaml.io.load_yml` function for loading.
 
         Args:
             filepath (str): Where to load the YAML file from
             TargetCls (type): The class constructor
-            **load_kwargs: Passed on to :py:func:`dantro._yaml.load_yml`
+            **load_kwargs: Passed on to :py:func:`yayaml.io.load_yml`
 
         Returns:
             ObjectContainer: The loaded YAML content as an ObjectContainer
         """
         # NOTE Implementation is the same as above, but the TargetCls is not!
         d = load_yml(filepath, **load_kwargs)
         return TargetCls(data=d, attrs=dict(filepath=filepath))
```

### Comparing `dantro-0.19.1/dantro/data_mngr.py` & `dantro-0.19.2/dantro/data_mngr.py`

 * *Files 0% similar despite different names*

```diff
@@ -196,15 +196,15 @@
                 a relative path, it is considered relative to the current
                 working directory.
             name (str, optional): which name to give to the DataManager. If no
                 name is given, the data directories basename will be used
             load_cfg (Union[dict, str], optional): The base configuration used
                 for loading data. If a string is given, assumes it to be the
                 path to a YAML file and loads it using the
-                :py:func:`~dantro._yaml.load_yml` function. If None is given,
+                :py:func:`~yayaml.io.load_yml` function. If None is given,
                 it can still be supplied to the
                 :py:meth:`~dantro.data_mngr.DataManager.load` method later on.
             out_dir (Union[str, bool], optional): where output is written to.
                 If this is given as a relative path, it is considered relative
                 to the ``data_dir``. A formatting operation with the keys
                 ``timestamp`` and ``name`` is performed on this, where the
                 latter is the name of the data manager. If set to False, no
```

### Comparing `dantro-0.19.1/dantro/data_ops/_base_ops.py` & `dantro-0.19.2/dantro/data_ops/_base_ops.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_ops/apply.py` & `dantro-0.19.2/dantro/data_ops/apply.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_ops/arr_ops.py` & `dantro-0.19.2/dantro/data_ops/arr_ops.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_ops/ctrl_ops.py` & `dantro-0.19.2/dantro/data_ops/ctrl_ops.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_ops/db.py` & `dantro-0.19.2/dantro/data_ops/db.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_ops/db_tools.py` & `dantro-0.19.2/dantro/data_ops/db_tools.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_ops/expr_ops.py` & `dantro-0.19.2/dantro/data_ops/expr_ops.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/data_ops/hooks.py` & `dantro-0.19.2/dantro/data_ops/hooks.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/exceptions.py` & `dantro-0.19.2/dantro/exceptions.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,41 +1,12 @@
 """Custom dantro exception classes."""
 
 import inspect
 from difflib import get_close_matches as _get_close_matches
-from typing import Callable, List, Tuple
-
-# -----------------------------------------------------------------------------
-
-
-def raise_improved_exception(
-    exc: Exception,
-    *,
-    hints: List[Tuple[Callable, str]] = [],
-) -> None:
-    """Improves the given exception by appending one or multiple hint messages.
-
-    The ``hints`` argument should be a list of 2-tuples, consisting of a unary
-    matching function, expecting the exception as only argument, and a hint
-    that is part of the new error message.
-    """
-    matching_hints = []
-    for match_func, hint in hints:
-        if match_func(exc):
-            matching_hints.append(hint)
-
-    if matching_hints:
-        _hints = "\n".join(f"  - {h}" for h in matching_hints)
-        raise type(exc)(
-            str(exc) + f"\n\nHint(s) how to resolve this:\n{_hints}"
-        ) from exc
-
-    # Re-raise the active exception
-    raise
-
+from typing import Tuple
 
 # -----------------------------------------------------------------------------
 
 
 class DantroError(Exception):
     """Base class for all dantro-related errors"""
```

### Comparing `dantro-0.19.1/dantro/groups/__init__.py` & `dantro-0.19.2/dantro/groups/__init__.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/groups/_registry.py` & `dantro-0.19.2/dantro/groups/_registry.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/groups/dirpath.py` & `dantro-0.19.2/dantro/groups/dirpath.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/groups/graph.py` & `dantro-0.19.2/dantro/groups/graph.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/groups/labelled.py` & `dantro-0.19.2/dantro/groups/labelled.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/groups/ordered.py` & `dantro-0.19.2/dantro/groups/ordered.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/groups/psp.py` & `dantro-0.19.2/dantro/groups/psp.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/groups/time_series.py` & `dantro-0.19.2/dantro/groups/time_series.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/logging.py` & `dantro-0.19.2/dantro/logging.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/mixins/__init__.py` & `dantro-0.19.2/dantro/mixins/__init__.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/mixins/base.py` & `dantro-0.19.2/dantro/mixins/base.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/mixins/general.py` & `dantro-0.19.2/dantro/mixins/general.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/mixins/indexing.py` & `dantro-0.19.2/dantro/mixins/indexing.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/mixins/numeric.py` & `dantro-0.19.2/dantro/mixins/numeric.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/mixins/proxy_support.py` & `dantro-0.19.2/dantro/mixins/proxy_support.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/_cfg.py` & `dantro-0.19.2/dantro/plot/_cfg.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/creators/__init__.py` & `dantro-0.19.2/dantro/plot/creators/__init__.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/creators/base.py` & `dantro-0.19.2/dantro/plot/creators/base.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/creators/psp.py` & `dantro-0.19.2/dantro/plot/creators/psp.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/creators/pyplot.py` & `dantro-0.19.2/dantro/plot/creators/pyplot.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/funcs/_multiplot.py` & `dantro-0.19.2/dantro/plot/funcs/_multiplot.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/funcs/_utils.py` & `dantro-0.19.2/dantro/plot/funcs/_utils.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/funcs/basic.py` & `dantro-0.19.2/dantro/plot/funcs/basic.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/funcs/generic.py` & `dantro-0.19.2/dantro/plot/funcs/generic.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/funcs/graph.py` & `dantro-0.19.2/dantro/plot/funcs/graph.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/funcs/multiplot.py` & `dantro-0.19.2/dantro/plot/funcs/multiplot.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/plot_helper.py` & `dantro-0.19.2/dantro/plot/plot_helper.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/utils/_file_writer.py` & `dantro-0.19.2/dantro/plot/utils/_file_writer.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/utils/color_mngr.py` & `dantro-0.19.2/dantro/plot/utils/color_mngr.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/utils/mpl.py` & `dantro-0.19.2/dantro/plot/utils/mpl.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot/utils/plot_func.py` & `dantro-0.19.2/dantro/plot/utils/plot_func.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/plot_mngr.py` & `dantro-0.19.2/dantro/plot_mngr.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/proxy/hdf5.py` & `dantro-0.19.2/dantro/proxy/hdf5.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/tools.py` & `dantro-0.19.2/dantro/tools.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/utils/coords.py` & `dantro-0.19.2/dantro/utils/coords.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/utils/link.py` & `dantro-0.19.2/dantro/utils/link.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/utils/nx.py` & `dantro-0.19.2/dantro/utils/nx.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro/utils/ordereddict.py` & `dantro-0.19.2/dantro/utils/ordereddict.py`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/dantro.egg-info/PKG-INFO` & `dantro-0.19.2/dantro.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dantro
-Version: 0.19.1
+Version: 0.19.2
 Summary: Handle, transform, and visualize hierarchically structured data
 Home-page: https://gitlab.com/utopia-project/dantro
 Author: dantro developers
 Author-email: dantro-dev@iup.uni.heidelberg.de
 License: LGPL-3.0-or-later
 Classifier: Intended Audience :: Science/Research
 Classifier: Programming Language :: Python :: 3.8
```

### Comparing `dantro-0.19.1/dantro.egg-info/SOURCES.txt` & `dantro-0.19.2/dantro.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/pyproject.toml` & `dantro-0.19.2/pyproject.toml`

 * *Files identical despite different names*

### Comparing `dantro-0.19.1/setup.py` & `dantro-0.19.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -15,14 +15,17 @@
     "h5py",
     "h5netcdf",          # A more capable, h5py-based netcdf backend
     "matplotlib",
     "seaborn",
     "networkx",
     "ruamel.yaml",
     "dill",              # For faster and more powerful pickling
+    #
+    # first-party packages
+    "yayaml",
     "paramspace",
 ]
 # NOTE When changing any of the dependencies, make sure to update the table of
 #      dependencies in README.md.
 #      When adding a NEW dependency, make sure to denote it in the isort
 #      configuration, see pyproject.toml.
```

