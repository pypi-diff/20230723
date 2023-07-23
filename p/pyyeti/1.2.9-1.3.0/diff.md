# Comparing `tmp/pyyeti-1.2.9.tar.gz` & `tmp/pyyeti-1.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyyeti-1.2.9.tar", last modified: Sun Jul  2 17:11:44 2023, max compression
+gzip compressed data, was "pyyeti-1.3.0.tar", last modified: Sun Jul 23 21:23:24 2023, max compression
```

## Comparing `pyyeti-1.2.9.tar` & `pyyeti-1.3.0.tar`

### file list

```diff
@@ -1,82 +1,82 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-02 17:11:44.418480 pyyeti-1.2.9/
--rw-r--r--   0 runner    (1001) docker     (123)     1545 2023-07-02 17:11:24.000000 pyyeti-1.2.9/LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)      284 2023-07-02 17:11:24.000000 pyyeti-1.2.9/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-07-02 17:11:44.418480 pyyeti-1.2.9/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     3188 2023-07-02 17:11:24.000000 pyyeti-1.2.9/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       89 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyproject.toml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-02 17:11:44.414480 pyyeti-1.2.9/pyyeti/
--rw-r--r--   0 runner    (1001) docker     (123)     1035 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   106717 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cb.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-02 17:11:44.414480 pyyeti-1.2.9/pyyeti/cla/
--rw-r--r--   0 runner    (1001) docker     (123)      468 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cla/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15100 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cla/_magpct.py
--rw-r--r--   0 runner    (1001) docker     (123)     4520 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cla/_rptext1.py
--rw-r--r--   0 runner    (1001) docker     (123)    36465 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cla/_rptpct1.py
--rw-r--r--   0 runner    (1001) docker     (123)    10341 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cla/_rpttab1.py
--rw-r--r--   0 runner    (1001) docker     (123)    21418 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cla/_utilities.py
--rw-r--r--   0 runner    (1001) docker     (123)    50944 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cla/dr_def.py
--rw-r--r--   0 runner    (1001) docker     (123)    24805 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cla/dr_event.py
--rw-r--r--   0 runner    (1001) docker     (123)   111221 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cla/dr_results.py
--rw-r--r--   0 runner    (1001) docker     (123)    22910 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cla/dr_results_plots.py
--rw-r--r--   0 runner    (1001) docker     (123)     7083 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cla/rel_disp_dtm.py
--rw-r--r--   0 runner    (1001) docker     (123)     3912 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/column_plotter.py
--rw-r--r--   0 runner    (1001) docker     (123)    24119 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/cyclecount.py
--rw-r--r--   0 runner    (1001) docker     (123)    26399 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/datacursor.py
--rw-r--r--   0 runner    (1001) docker     (123)   124529 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/dsp.py
--rw-r--r--   0 runner    (1001) docker     (123)    70785 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/era.py
--rw-r--r--   0 runner    (1001) docker     (123)    42901 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/expmint.py
--rw-r--r--   0 runner    (1001) docker     (123)    29531 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/fdepsd.py
--rw-r--r--   0 runner    (1001) docker     (123)    33689 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/frclim.py
--rw-r--r--   0 runner    (1001) docker     (123)    16400 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/guitools.py
--rw-r--r--   0 runner    (1001) docker     (123)    14662 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/locate.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-02 17:11:44.418480 pyyeti-1.2.9/pyyeti/nastran/
--rw-r--r--   0 runner    (1001) docker     (123)      138 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/nastran/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   131608 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/nastran/bulk.py
--rw-r--r--   0 runner    (1001) docker     (123)   136601 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/nastran/n2p.py
--rw-r--r--   0 runner    (1001) docker     (123)   120906 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/nastran/op2.py
--rw-r--r--   0 runner    (1001) docker     (123)    91322 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/nastran/op4.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-02 17:11:44.418480 pyyeti-1.2.9/pyyeti/ode/
--rw-r--r--   0 runner    (1001) docker     (123)      869 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ode/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18978 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ode/_base_ode_class.py
--rw-r--r--   0 runner    (1001) docker     (123)    39134 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ode/_utilities.py
--rw-r--r--   0 runner    (1001) docker     (123)     9990 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ode/freqdirect.py
--rw-r--r--   0 runner    (1001) docker     (123)    17392 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ode/frf_mode_participation.py
--rw-r--r--   0 runner    (1001) docker     (123)    10055 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ode/solvecdf.py
--rw-r--r--   0 runner    (1001) docker     (123)     5653 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ode/solveexp1.py
--rw-r--r--   0 runner    (1001) docker     (123)    28070 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ode/solveexp2.py
--rw-r--r--   0 runner    (1001) docker     (123)    27500 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ode/solvenewmark.py
--rw-r--r--   0 runner    (1001) docker     (123)    69302 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ode/solveunc.py
--rw-r--r--   0 runner    (1001) docker     (123)     9395 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/pp.py
--rw-r--r--   0 runner    (1001) docker     (123)    43744 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/psd.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-02 17:11:44.418480 pyyeti-1.2.9/pyyeti/rainflow/
--rw-r--r--   0 runner    (1001) docker     (123)      195 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/rainflow/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    13898 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/rainflow/c_rain.c
--rw-r--r--   0 runner    (1001) docker     (123)     6540 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/rainflow/py_rain.py
--rw-r--r--   0 runner    (1001) docker     (123)    74708 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/srs.py
--rw-r--r--   0 runner    (1001) docker     (123)    11892 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ssmodel.py
--rw-r--r--   0 runner    (1001) docker     (123)    14070 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/stats.py
--rw-r--r--   0 runner    (1001) docker     (123)    12371 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/writer.py
--rw-r--r--   0 runner    (1001) docker     (123)    57514 2023-07-02 17:11:24.000000 pyyeti-1.2.9/pyyeti/ytools.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-02 17:11:44.414480 pyyeti-1.2.9/pyyeti.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-07-02 17:11:44.000000 pyyeti-1.2.9/pyyeti.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1596 2023-07-02 17:11:44.000000 pyyeti-1.2.9/pyyeti.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-02 17:11:44.000000 pyyeti-1.2.9/pyyeti.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       29 2023-07-02 17:11:44.000000 pyyeti-1.2.9/pyyeti.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-02 17:11:44.000000 pyyeti-1.2.9/pyyeti.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-02 17:11:44.418480 pyyeti-1.2.9/scripts/
--rwxr-xr-x   0 runner    (1001) docker     (123)      581 2023-07-02 17:11:24.000000 pyyeti-1.2.9/scripts/lsop2
--rwxr-xr-x   0 runner    (1001) docker     (123)      365 2023-07-02 17:11:24.000000 pyyeti-1.2.9/scripts/lsop4
--rw-r--r--   0 runner    (1001) docker     (123)      266 2023-07-02 17:11:44.422480 pyyeti-1.2.9/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     4615 2023-07-02 17:11:24.000000 pyyeti-1.2.9/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-02 17:11:44.410480 pyyeti-1.2.9/tests/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-02 17:11:44.418480 pyyeti-1.2.9/tests/nas2cam_csuper/
--rw-r--r--   0 runner    (1001) docker     (123)     1622 2023-07-02 17:11:24.000000 pyyeti-1.2.9/tests/nas2cam_csuper/inboard.asm
--rw-r--r--   0 runner    (1001) docker     (123)    25840 2023-07-02 17:11:24.000000 pyyeti-1.2.9/tests/nas2cam_csuper/inboard.op4
--rw-r--r--   0 runner    (1001) docker     (123)     4727 2023-07-02 17:11:24.000000 pyyeti-1.2.9/tests/nas2cam_csuper/inboard.pch
--rw-r--r--   0 runner    (1001) docker     (123)    15736 2023-07-02 17:11:24.000000 pyyeti-1.2.9/tests/nas2cam_csuper/nas2cam.op2
--rw-r--r--   0 runner    (1001) docker     (123)   147552 2023-07-02 17:11:24.000000 pyyeti-1.2.9/tests/nas2cam_csuper/nas2cam.op4
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-02 17:11:44.418480 pyyeti-1.2.9/tests/nastran_drm12/
--rw-r--r--   0 runner    (1001) docker     (123)    13464 2023-07-02 17:11:24.000000 pyyeti-1.2.9/tests/nastran_drm12/drm12.op2
--rw-r--r--   0 runner    (1001) docker     (123)    77852 2023-07-02 17:11:24.000000 pyyeti-1.2.9/tests/nastran_drm12/drm12.op4
--rw-r--r--   0 runner    (1001) docker     (123)    17160 2023-07-02 17:11:24.000000 pyyeti-1.2.9/tests/nastran_drm12/inboard_nas2cam.op2
--rw-r--r--   0 runner    (1001) docker     (123)    51624 2023-07-02 17:11:24.000000 pyyeti-1.2.9/tests/nastran_drm12/inboard_nas2cam.op4
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:23:24.011610 pyyeti-1.3.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1545 2023-07-23 21:23:00.000000 pyyeti-1.3.0/LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      284 2023-07-23 21:23:00.000000 pyyeti-1.3.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     4268 2023-07-23 21:23:24.015610 pyyeti-1.3.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3188 2023-07-23 21:23:00.000000 pyyeti-1.3.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       89 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyproject.toml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:23:24.003610 pyyeti-1.3.0/pyyeti/
+-rw-r--r--   0 runner    (1001) docker     (123)     1035 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   106717 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cb.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:23:24.007610 pyyeti-1.3.0/pyyeti/cla/
+-rw-r--r--   0 runner    (1001) docker     (123)      468 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cla/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15100 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cla/_magpct.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4520 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cla/_rptext1.py
+-rw-r--r--   0 runner    (1001) docker     (123)    36465 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cla/_rptpct1.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10341 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cla/_rpttab1.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21418 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cla/_utilities.py
+-rw-r--r--   0 runner    (1001) docker     (123)    50944 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cla/dr_def.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24805 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cla/dr_event.py
+-rw-r--r--   0 runner    (1001) docker     (123)   111221 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cla/dr_results.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22910 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cla/dr_results_plots.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7083 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cla/rel_disp_dtm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3912 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/column_plotter.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24211 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/cyclecount.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26399 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/datacursor.py
+-rw-r--r--   0 runner    (1001) docker     (123)   124529 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/dsp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    70785 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/era.py
+-rw-r--r--   0 runner    (1001) docker     (123)    42901 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/expmint.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29799 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/fdepsd.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33689 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/frclim.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16400 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/guitools.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14662 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/locate.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:23:24.007610 pyyeti-1.3.0/pyyeti/nastran/
+-rw-r--r--   0 runner    (1001) docker     (123)      138 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/nastran/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   131608 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/nastran/bulk.py
+-rw-r--r--   0 runner    (1001) docker     (123)   136601 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/nastran/n2p.py
+-rw-r--r--   0 runner    (1001) docker     (123)   120944 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/nastran/op2.py
+-rw-r--r--   0 runner    (1001) docker     (123)    91322 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/nastran/op4.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:23:24.011610 pyyeti-1.3.0/pyyeti/ode/
+-rw-r--r--   0 runner    (1001) docker     (123)      869 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ode/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18978 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ode/_base_ode_class.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39134 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ode/_utilities.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9990 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ode/freqdirect.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17392 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ode/frf_mode_participation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10055 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ode/solvecdf.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5653 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ode/solveexp1.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28070 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ode/solveexp2.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27500 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ode/solvenewmark.py
+-rw-r--r--   0 runner    (1001) docker     (123)    69302 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ode/solveunc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9395 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/pp.py
+-rw-r--r--   0 runner    (1001) docker     (123)    43788 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/psd.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:23:24.011610 pyyeti-1.3.0/pyyeti/rainflow/
+-rw-r--r--   0 runner    (1001) docker     (123)      195 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/rainflow/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13898 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/rainflow/c_rain.c
+-rw-r--r--   0 runner    (1001) docker     (123)     6540 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/rainflow/py_rain.py
+-rw-r--r--   0 runner    (1001) docker     (123)    74708 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/srs.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11892 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ssmodel.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14070 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12371 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/writer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    57514 2023-07-23 21:23:00.000000 pyyeti-1.3.0/pyyeti/ytools.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:23:24.003610 pyyeti-1.3.0/pyyeti.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4268 2023-07-23 21:23:23.000000 pyyeti-1.3.0/pyyeti.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1596 2023-07-23 21:23:23.000000 pyyeti-1.3.0/pyyeti.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 21:23:23.000000 pyyeti-1.3.0/pyyeti.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       29 2023-07-23 21:23:23.000000 pyyeti-1.3.0/pyyeti.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-23 21:23:23.000000 pyyeti-1.3.0/pyyeti.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:23:24.011610 pyyeti-1.3.0/scripts/
+-rwxr-xr-x   0 runner    (1001) docker     (123)      581 2023-07-23 21:23:00.000000 pyyeti-1.3.0/scripts/lsop2
+-rwxr-xr-x   0 runner    (1001) docker     (123)      365 2023-07-23 21:23:00.000000 pyyeti-1.3.0/scripts/lsop4
+-rw-r--r--   0 runner    (1001) docker     (123)      266 2023-07-23 21:23:24.015610 pyyeti-1.3.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     4661 2023-07-23 21:23:00.000000 pyyeti-1.3.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:23:23.999610 pyyeti-1.3.0/tests/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:23:24.011610 pyyeti-1.3.0/tests/nas2cam_csuper/
+-rw-r--r--   0 runner    (1001) docker     (123)     1622 2023-07-23 21:23:00.000000 pyyeti-1.3.0/tests/nas2cam_csuper/inboard.asm
+-rw-r--r--   0 runner    (1001) docker     (123)    25840 2023-07-23 21:23:00.000000 pyyeti-1.3.0/tests/nas2cam_csuper/inboard.op4
+-rw-r--r--   0 runner    (1001) docker     (123)     4727 2023-07-23 21:23:00.000000 pyyeti-1.3.0/tests/nas2cam_csuper/inboard.pch
+-rw-r--r--   0 runner    (1001) docker     (123)    15736 2023-07-23 21:23:00.000000 pyyeti-1.3.0/tests/nas2cam_csuper/nas2cam.op2
+-rw-r--r--   0 runner    (1001) docker     (123)   147552 2023-07-23 21:23:00.000000 pyyeti-1.3.0/tests/nas2cam_csuper/nas2cam.op4
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 21:23:24.011610 pyyeti-1.3.0/tests/nastran_drm12/
+-rw-r--r--   0 runner    (1001) docker     (123)    13464 2023-07-23 21:23:00.000000 pyyeti-1.3.0/tests/nastran_drm12/drm12.op2
+-rw-r--r--   0 runner    (1001) docker     (123)    77852 2023-07-23 21:23:00.000000 pyyeti-1.3.0/tests/nastran_drm12/drm12.op4
+-rw-r--r--   0 runner    (1001) docker     (123)    17160 2023-07-23 21:23:00.000000 pyyeti-1.3.0/tests/nastran_drm12/inboard_nas2cam.op2
+-rw-r--r--   0 runner    (1001) docker     (123)    51624 2023-07-23 21:23:00.000000 pyyeti-1.3.0/tests/nastran_drm12/inboard_nas2cam.op4
```

### Comparing `pyyeti-1.2.9/LICENSE.txt` & `pyyeti-1.3.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/PKG-INFO` & `pyyeti-1.3.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,24 +1,25 @@
 Metadata-Version: 2.1
 Name: pyyeti
-Version: 1.2.9
+Version: 1.3.0
 Summary: Tools mostly related to structural dynamics
 Home-page: http://github.com/twmacro/pyyeti/
 Author: Tim Widrick
 Author-email: twmacro@gmail.com
 License: BSD
 Platform: any
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: C
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Natural Language :: English
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: OS Independent
 Classifier: Topic :: Scientific/Engineering
```

#### html2text {}

```diff
@@ -1,21 +1,22 @@
-Metadata-Version: 2.1 Name: pyyeti Version: 1.2.9 Summary: Tools mostly related
+Metadata-Version: 2.1 Name: pyyeti Version: 1.3.0 Summary: Tools mostly related
 to structural dynamics Home-page: http://github.com/twmacro/pyyeti/ Author: Tim
 Widrick Author-email: twmacro@gmail.com License: BSD Platform: any Classifier:
 Development Status :: 4 - Beta Classifier: Programming Language :: C
 Classifier: Programming Language :: Python Classifier: Programming Language ::
 Python :: 3.6 Classifier: Programming Language :: Python :: 3.7 Classifier:
 Programming Language :: Python :: 3.8 Classifier: Programming Language ::
 Python :: 3.9 Classifier: Programming Language :: Python :: 3.10 Classifier:
-Programming Language :: Python :: 3 :: Only Classifier: Programming Language ::
-Python :: Implementation :: CPython Classifier: Natural Language :: English
-Classifier: Intended Audience :: Science/Research Classifier: License :: OSI
-Approved :: BSD License Classifier: Operating System :: OS Independent
-Classifier: Topic :: Scientific/Engineering Description-Content-Type: text/
-markdown License-File: LICENSE.txt
+Programming Language :: Python :: 3.11 Classifier: Programming Language ::
+Python :: 3 :: Only Classifier: Programming Language :: Python ::
+Implementation :: CPython Classifier: Natural Language :: English Classifier:
+Intended Audience :: Science/Research Classifier: License :: OSI Approved ::
+BSD License Classifier: Operating System :: OS Independent Classifier: Topic ::
+Scientific/Engineering Description-Content-Type: text/markdown License-File:
+LICENSE.txt
 [Build_Status] [Documentation_Status] [Coverage_Status] [License:_BSD_3-Clause]
                           [PyPI] [Code_style:_black]
 # pyYeti pyYeti has tools mostly related to structural dynamics: * Solve matrix
 equations of motion in the time and frequency domains * Shock response spectrum
 (SRS) * Fatigue damage equivalent power spectral densities (PSD) * Hurty-Craig-
 Bampton model checks * Coupled loads analysis tools * Statistics tools for
 computing k-factors (for tolerance bounds and intervals) and for order
```

### Comparing `pyyeti-1.2.9/README.md` & `pyyeti-1.3.0/README.md`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/__init__.py` & `pyyeti-1.3.0/pyyeti/__init__.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cb.py` & `pyyeti-1.3.0/pyyeti/cb.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cla/_magpct.py` & `pyyeti-1.3.0/pyyeti/cla/_magpct.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cla/_rptext1.py` & `pyyeti-1.3.0/pyyeti/cla/_rptext1.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cla/_rptpct1.py` & `pyyeti-1.3.0/pyyeti/cla/_rptpct1.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cla/_rpttab1.py` & `pyyeti-1.3.0/pyyeti/cla/_rpttab1.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cla/_utilities.py` & `pyyeti-1.3.0/pyyeti/cla/_utilities.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cla/dr_def.py` & `pyyeti-1.3.0/pyyeti/cla/dr_def.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cla/dr_event.py` & `pyyeti-1.3.0/pyyeti/cla/dr_event.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cla/dr_results.py` & `pyyeti-1.3.0/pyyeti/cla/dr_results.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cla/dr_results_plots.py` & `pyyeti-1.3.0/pyyeti/cla/dr_results_plots.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cla/rel_disp_dtm.py` & `pyyeti-1.3.0/pyyeti/cla/rel_disp_dtm.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/column_plotter.py` & `pyyeti-1.3.0/pyyeti/column_plotter.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/cyclecount.py` & `pyyeti-1.3.0/pyyeti/cyclecount.py`

 * *Files 2% similar despite different names*

```diff
@@ -379,14 +379,19 @@
     out_of_bounds : bool; optional
         True if either `mx` or `mn` will fall out of range of the bins
         (according to `right`). Only returned if `check_bounds` is
         True.
 
     Notes
     -----
+    If `mx` and `mn` are equal, they are reset::
+
+        mx = mx + 0.5
+        mn = mn - 0.5
+
     If `bins` is a scalar, this routine tries to mimic the behavior of
     the :func:`pandas.cut` routine::
 
         bb = np.linspace(mn, mx, bins+1)
         p = 0.001 * (mx - mn)
         if right:
             bb[0] -= p
@@ -397,16 +402,14 @@
     returned as is::
 
         bb = np.array(bins)
 
     Raises
     ------
     ValueError
-        If `mx` and `mn` are equal
-    ValueError
         If `bins` is a vector but is not monotonically increasing
 
     Examples
     --------
     >>> from pyyeti import cyclecount
     >>> cyclecount.getbins(4, 12, 4)
     array([  3.992,   6.   ,   8.   ,  10.   ,  12.   ])
@@ -415,15 +418,18 @@
     >>> cyclecount.getbins([1, 2, 3, 4], 12, 4, check_bounds=True)
     (array([1, 2, 3, 4]), True)
     """
     bins = np.atleast_1d(bins)
     if mx < mn:
         mx, mn = mn, mx
     elif mx == mn:
-        raise ValueError("`mx` and `mn` must not be equal")
+        mx = mx + 0.5
+        mn = mn - 0.5
+        # raise ValueError("`mx` and `mn` must not be equal")
+
     if bins.size == 1:
         bins = int(bins)
         bb = np.linspace(mn, mx, bins + 1)
         p = 0.001 * (mx - mn)
         if right:
             bb[0] -= p
         else:
```

### Comparing `pyyeti-1.2.9/pyyeti/datacursor.py` & `pyyeti-1.3.0/pyyeti/datacursor.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/dsp.py` & `pyyeti-1.3.0/pyyeti/dsp.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/era.py` & `pyyeti-1.3.0/pyyeti/era.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/expmint.py` & `pyyeti-1.3.0/pyyeti/expmint.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/fdepsd.py` & `pyyeti-1.3.0/pyyeti/fdepsd.py`

 * *Files 6% similar despite different names*

```diff
@@ -59,17 +59,19 @@
 
 
 def fdepsd(
     sig,
     sr,
     freq,
     Q,
+    *,
     resp="absacce",
-    hpfilter=5.0,
+    detrend=True,
     winends="auto",
+    hpfilter=5.0,
     nbins=300,
     T0=60.0,
     rolloff="lanczos",
     ppc=12,
     parallel="auto",
     maxcpu=14,
     verbose=False,
@@ -95,25 +97,33 @@
         =========    =======================================
          `resp`      Damage is based on
         =========    =======================================
         'absacce'    absolute acceleration [#fde1]_
         'pvelo'      pseudo velocity [#fde2]_
         =========    =======================================
 
-    hpfilter : scalar or None; optional
-        High pass filter frequency; if None, no filtering is done.
-        If filtering is done, it is a 3rd order butterworth via
-        :func:`scipy.signal.lfilter`.
+    detrend : bool; optional
+        If True, `sig` is detrended via :func:`scipy.signal.detrend`.
+        Option is ignored and treated as True if at least one of the
+        `winends` or `hpfilter` options are used. Detrending is done
+        before either of those options.
     winends : None or 'auto' or dictionary; optional
         If None, :func:`pyyeti.dsp.windowends` is not called. If
         'auto', :func:`pyyeti.dsp.windowends` is called to apply a
         0.25 second window or a 50 point window (whichever is smaller)
         to the front. Otherwise, `winends` must be a dictionary of
         arguments that will be passed to :func:`pyyeti.dsp.windowends`
-        (not including `signal`).
+        (not including `signal`). The signal is detrended prior to
+        calling :func:`pyyeti.dsp.windowends`.
+    hpfilter : scalar or None; optional
+        High pass filter frequency; if None, no filtering is done. If
+        filtering is done, it is after detrending and after any
+        `winends` action was taken. The signal is filtered via
+        :func:`scipy.signal.lfilter` using a 3rd order butterworth
+        filter (:func:`scipy.signal.butter`).
     nbins : integer; optional
         The number of amplitude levels at which to count cycles
     T0 : scalar; optional
         Specifies test duration in seconds
     rolloff : string or function or None; optional
         Indicate which method to use to account for the SRS roll off
         when the minimum `ppc` value is not met. Either 'fft' or
@@ -528,33 +538,28 @@
         raise ValueError("`sig` and `freq` must both be 1d arrays")
     if resp not in ("absacce", "pvelo"):
         raise ValueError("`resp` must be 'absacce' or 'pvelo'")
     (coeffunc, methfunc, rollfunc, ptr) = srs._process_inputs(
         resp, "abs", rolloff, "primary"
     )
 
+    if winends == "auto":
+        winends = {"portion": min(int(0.25 * sr), 50, len(sig))}
+
+    if detrend or winends is not None or hpfilter is not None:
+        sig = signal.detrend(sig)
+
+    if winends is not None:
+        sig = dsp.windowends(sig, **winends)
+
     if hpfilter is not None:
         if verbose:
             print(f"High pass filtering @ {hpfilter} Hz")
         b, a = signal.butter(3, hpfilter / (sr / 2), "high")
-        # to try to get rid of filter transient at the beginning:
-        #  - put a 0.25 second buffer on the front (length from
-        #    looking at impulse response)
-        #  - filter
-        #  - chop off buffer
-        n = int(0.25 * sr)
-        sig2 = np.empty(n + sig.size)
-        sig2[:n] = sig[0]
-        sig2[n:] = sig
-        sig = signal.lfilter(b, a, sig2)[n:]
-
-    if winends == "auto":
-        sig = dsp.windowends(sig, min(int(0.25 * sr), 50, len(sig)))
-    elif winends is not None:
-        sig = dsp.windowends(sig, **winends)
+        sig = signal.lfilter(b, a, sig)
 
     mxfrq = freq.max()
     curppc = sr / mxfrq
     if rolloff == "prefilter":
         sig, sr = rollfunc(sig, sr, ppc, mxfrq)
         rollfunc = None
 
@@ -636,15 +641,15 @@
         print()
         print("Computing outputs G1, G2, etc.")
 
     # calculate non-cumulative counts per bin:
     BinCount = np.hstack((Count[:, :-1] - Count[:, 1:], Count[:, -1:]))
 
     # for calculating G2:
-    G2max = Amax ** 2
+    G2max = Amax**2
     for j in range(LF):
         pv = BinAmps[j] >= Amax[j] / 3  # ignore small amp cycles
         if np.any(pv):
             x = BinAmps[j, pv] ** 2
             x2 = G2max[j]
             y = np.log(Count[j, pv])
             y1 = np.log(Count[j, 0])
@@ -668,20 +673,20 @@
         Df4[j] = (BinAmps[j] ** b4).dot(BinCount[j])
         Df8[j] = (BinAmps[j] ** b8).dot(BinCount[j])
         Df12[j] = (BinAmps[j] ** b12).dot(BinCount[j])
 
     N0 = freq * T0
     lnN0 = np.log(N0)
     if resp == "absacce":
-        G1 = Amax ** 2 / (Q * pi * freq * lnN0)
+        G1 = Amax**2 / (Q * pi * freq * lnN0)
         G2 = G2max / (Q * pi * freq * lnN0)
 
         # calculate test-damage indicators for b = 4, 8 and 12:
         Abar = 2 * lnN0
-        Abar2 = Abar ** 2
+        Abar2 = Abar**2
         Dt4 = N0 * 8 - (Abar2 + 4 * Abar + 8)
         sig2_4 = np.sqrt(Df4 / Dt4)
         G4 = sig2_4 / ((Q * pi / 2) * freq)
 
         Abar3 = Abar2 * Abar
         Abar4 = Abar2 * Abar2
         Dt8 = N0 * 384 - (Abar4 + 8 * Abar3 + 48 * Abar2 + 192 * Abar + 384)
@@ -700,15 +705,15 @@
             + 46080
         )
         sig2_12 = (Df12 / Dt12) ** (1 / 6)
         G12 = sig2_12 / ((Q * pi / 2) * freq)
 
         Gmax = np.sqrt(np.vstack((G4, G8, G12)) * (Q * pi * freq * lnN0))
     else:
-        G1 = (Amax ** 2 * 4 * pi * freq) / (Q * lnN0)
+        G1 = (Amax**2 * 4 * pi * freq) / (Q * lnN0)
         G2 = (G2max * 4 * pi * freq) / (Q * lnN0)
 
         Dt4 = 2 * N0
         sig2_4 = np.sqrt(Df4 / Dt4)
         G4 = sig2_4 * ((4 * pi / Q) * freq)
 
         Dt8 = 24 * N0
```

### Comparing `pyyeti-1.2.9/pyyeti/frclim.py` & `pyyeti-1.3.0/pyyeti/frclim.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/guitools.py` & `pyyeti-1.3.0/pyyeti/guitools.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/locate.py` & `pyyeti-1.3.0/pyyeti/locate.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/nastran/bulk.py` & `pyyeti-1.3.0/pyyeti/nastran/bulk.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/nastran/n2p.py` & `pyyeti-1.3.0/pyyeti/nastran/n2p.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/nastran/op2.py` & `pyyeti-1.3.0/pyyeti/nastran/op2.py`

 * *Files 0% similar despite different names*

```diff
@@ -3246,15 +3246,16 @@
                     if verbose:
                         print(f"Reading table {name}...")
                     cstm = o2._rdop2cstm68()
                     bc = np.array(
                         [
                             [+0, 1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0, 1],
                             [-1, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
-                        ]
+                        ],
+                        dtype=float,
                     )
                     cstm = np.vstack((bc, cstm))
                     continue
 
                 if name.find("GEOM1") == 0:
                     if verbose:
                         print(f"Reading table {name}...")
```

### Comparing `pyyeti-1.2.9/pyyeti/nastran/op4.py` & `pyyeti-1.3.0/pyyeti/nastran/op4.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ode/__init__.py` & `pyyeti-1.3.0/pyyeti/ode/__init__.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ode/_base_ode_class.py` & `pyyeti-1.3.0/pyyeti/ode/_base_ode_class.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ode/_utilities.py` & `pyyeti-1.3.0/pyyeti/ode/_utilities.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ode/freqdirect.py` & `pyyeti-1.3.0/pyyeti/ode/freqdirect.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ode/frf_mode_participation.py` & `pyyeti-1.3.0/pyyeti/ode/frf_mode_participation.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ode/solvecdf.py` & `pyyeti-1.3.0/pyyeti/ode/solvecdf.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ode/solveexp1.py` & `pyyeti-1.3.0/pyyeti/ode/solveexp1.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ode/solveexp2.py` & `pyyeti-1.3.0/pyyeti/ode/solveexp2.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ode/solvenewmark.py` & `pyyeti-1.3.0/pyyeti/ode/solvenewmark.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ode/solveunc.py` & `pyyeti-1.3.0/pyyeti/ode/solveunc.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/pp.py` & `pyyeti-1.3.0/pyyeti/pp.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/psd.py` & `pyyeti-1.3.0/pyyeti/psd.py`

 * *Files 1% similar despite different names*

```diff
@@ -910,16 +910,17 @@
     -------
     sig : 1d ndarray
         The time domain signal with properties set to match input PSD
         spectrum. Duration of signal: ``1 / df``.
     sr : scalar
         The sample rate of the signal (``ppc * fstop``)
     time : 1d ndarray; optional
-        Time vector for the signal starting at zero with step of
-        ``1.0 / sr``: ``time = np.arange(len(sig)) / sr``.
+        Time vector for the signal starting at zero with step of ``1.0
+        / sr``: ``time = np.arange(len(sig)) / sr``. Only returned if
+        `gettime` is True.
 
     Notes
     -----
     The following outlines the equations used in this routine.
 
     If :math:`df` is None: :math:`df = fstart / 100`.
```

### Comparing `pyyeti-1.2.9/pyyeti/rainflow/c_rain.c` & `pyyeti-1.3.0/pyyeti/rainflow/c_rain.c`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/rainflow/py_rain.py` & `pyyeti-1.3.0/pyyeti/rainflow/py_rain.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/srs.py` & `pyyeti-1.3.0/pyyeti/srs.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ssmodel.py` & `pyyeti-1.3.0/pyyeti/ssmodel.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/stats.py` & `pyyeti-1.3.0/pyyeti/stats.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/writer.py` & `pyyeti-1.3.0/pyyeti/writer.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti/ytools.py` & `pyyeti-1.3.0/pyyeti/ytools.py`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/pyyeti.egg-info/PKG-INFO` & `pyyeti-1.3.0/pyyeti.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,24 +1,25 @@
 Metadata-Version: 2.1
 Name: pyyeti
-Version: 1.2.9
+Version: 1.3.0
 Summary: Tools mostly related to structural dynamics
 Home-page: http://github.com/twmacro/pyyeti/
 Author: Tim Widrick
 Author-email: twmacro@gmail.com
 License: BSD
 Platform: any
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: C
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Natural Language :: English
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: OS Independent
 Classifier: Topic :: Scientific/Engineering
```

#### html2text {}

```diff
@@ -1,21 +1,22 @@
-Metadata-Version: 2.1 Name: pyyeti Version: 1.2.9 Summary: Tools mostly related
+Metadata-Version: 2.1 Name: pyyeti Version: 1.3.0 Summary: Tools mostly related
 to structural dynamics Home-page: http://github.com/twmacro/pyyeti/ Author: Tim
 Widrick Author-email: twmacro@gmail.com License: BSD Platform: any Classifier:
 Development Status :: 4 - Beta Classifier: Programming Language :: C
 Classifier: Programming Language :: Python Classifier: Programming Language ::
 Python :: 3.6 Classifier: Programming Language :: Python :: 3.7 Classifier:
 Programming Language :: Python :: 3.8 Classifier: Programming Language ::
 Python :: 3.9 Classifier: Programming Language :: Python :: 3.10 Classifier:
-Programming Language :: Python :: 3 :: Only Classifier: Programming Language ::
-Python :: Implementation :: CPython Classifier: Natural Language :: English
-Classifier: Intended Audience :: Science/Research Classifier: License :: OSI
-Approved :: BSD License Classifier: Operating System :: OS Independent
-Classifier: Topic :: Scientific/Engineering Description-Content-Type: text/
-markdown License-File: LICENSE.txt
+Programming Language :: Python :: 3.11 Classifier: Programming Language ::
+Python :: 3 :: Only Classifier: Programming Language :: Python ::
+Implementation :: CPython Classifier: Natural Language :: English Classifier:
+Intended Audience :: Science/Research Classifier: License :: OSI Approved ::
+BSD License Classifier: Operating System :: OS Independent Classifier: Topic ::
+Scientific/Engineering Description-Content-Type: text/markdown License-File:
+LICENSE.txt
 [Build_Status] [Documentation_Status] [Coverage_Status] [License:_BSD_3-Clause]
                           [PyPI] [Code_style:_black]
 # pyYeti pyYeti has tools mostly related to structural dynamics: * Solve matrix
 equations of motion in the time and frequency domains * Shock response spectrum
 (SRS) * Fatigue damage equivalent power spectral densities (PSD) * Hurty-Craig-
 Bampton model checks * Coupled loads analysis tools * Statistics tools for
 computing k-factors (for tolerance bounds and intervals) and for order
```

### Comparing `pyyeti-1.2.9/pyyeti.egg-info/SOURCES.txt` & `pyyeti-1.3.0/pyyeti.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/scripts/lsop2` & `pyyeti-1.3.0/scripts/lsop2`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/setup.py` & `pyyeti-1.3.0/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -29,14 +29,15 @@
     "Programming Language :: C",
     "Programming Language :: Python",
     "Programming Language :: Python :: 3.6",
     "Programming Language :: Python :: 3.7",
     "Programming Language :: Python :: 3.8",
     "Programming Language :: Python :: 3.9",
     "Programming Language :: Python :: 3.10",
+    "Programming Language :: Python :: 3.11",
     "Programming Language :: Python :: 3 :: Only",
     "Programming Language :: Python :: Implementation :: CPython",
     "Natural Language :: English",
     "Intended Audience :: Science/Research",
     "License :: OSI Approved :: BSD License",
     "Operating System :: OS Independent",
     "Topic :: Scientific/Engineering",
@@ -92,15 +93,15 @@
         )
     else:
         kw = {}
 
     install_requires = check_dependencies()
     setup(
         name="pyyeti",
-        version="1.2.9",
+        version="1.3.0",
         url="http://github.com/twmacro/pyyeti/",
         license="BSD",
         author="Tim Widrick",
         install_requires=install_requires,
         author_email="twmacro@gmail.com",
         description=("Tools mostly related to structural dynamics"),
         long_description=long_description,
```

### Comparing `pyyeti-1.2.9/tests/nas2cam_csuper/inboard.asm` & `pyyeti-1.3.0/tests/nas2cam_csuper/inboard.asm`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/tests/nas2cam_csuper/inboard.op4` & `pyyeti-1.3.0/tests/nas2cam_csuper/inboard.op4`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/tests/nas2cam_csuper/inboard.pch` & `pyyeti-1.3.0/tests/nas2cam_csuper/inboard.pch`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/tests/nas2cam_csuper/nas2cam.op2` & `pyyeti-1.3.0/tests/nas2cam_csuper/nas2cam.op2`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/tests/nas2cam_csuper/nas2cam.op4` & `pyyeti-1.3.0/tests/nas2cam_csuper/nas2cam.op4`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/tests/nastran_drm12/drm12.op2` & `pyyeti-1.3.0/tests/nastran_drm12/drm12.op2`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/tests/nastran_drm12/drm12.op4` & `pyyeti-1.3.0/tests/nastran_drm12/drm12.op4`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/tests/nastran_drm12/inboard_nas2cam.op2` & `pyyeti-1.3.0/tests/nastran_drm12/inboard_nas2cam.op2`

 * *Files identical despite different names*

### Comparing `pyyeti-1.2.9/tests/nastran_drm12/inboard_nas2cam.op4` & `pyyeti-1.3.0/tests/nastran_drm12/inboard_nas2cam.op4`

 * *Files identical despite different names*

