# Comparing `tmp/refnx-0.1.8.tar.gz` & `tmp/refnx-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/refnx-0.1.8.tar", last modified: Fri Jul 12 03:44:23 2019, max compression
+gzip compressed data, was "dist/refnx-0.1.9.tar", last modified: Sun Aug 18 23:32:25 2019, max compression
```

## Comparing `refnx-0.1.8.tar` & `refnx-0.1.9.tar`

### file list

```diff
@@ -1,300 +1,304 @@
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)       68 2019-01-16 22:34:46.000000 refnx-0.1.8/MANIFEST.in
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      970 2019-07-12 03:44:23.000000 refnx-0.1.8/PKG-INFO
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      710 2019-01-16 22:34:46.000000 refnx-0.1.8/README.md
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/benchmarks/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)       74 2019-01-16 22:34:46.000000 refnx-0.1.8/benchmarks/__init__.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/benchmarks/benchmarks/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-01-16 22:34:46.000000 refnx-0.1.8/benchmarks/benchmarks/__init__.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1710 2019-01-16 22:34:46.000000 refnx-0.1.8/benchmarks/benchmarks/analysis.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2386 2019-01-16 22:34:46.000000 refnx-0.1.8/benchmarks/benchmarks/common.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2367 2019-01-16 22:34:46.000000 refnx-0.1.8/benchmarks/benchmarks/reflect.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1917 2019-01-16 22:34:46.000000 refnx-0.1.8/benchmarks/run.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      370 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/__init__.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/_lib/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      526 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/_lib/__init__.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2959 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/_numdiff.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1303 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/_lib/_testutils.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/_lib/emcee/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1109 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/LICENSE
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      732 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/__init__.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4040 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/autocorr.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/_lib/emcee/backends/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      436 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/backends/__init__.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8198 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/backends/backend.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6656 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/backends/hdf.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    18962 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/ensemble.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      219 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/interruptible_pool.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      229 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/model.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/_lib/emcee/moves/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      483 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/moves/__init__.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1612 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/moves/de.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1543 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/moves/de_snooker.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4020 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/moves/gaussian.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1276 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/moves/kde.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2440 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/moves/mh.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1700 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/moves/move.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4093 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/moves/red_blue.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      970 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/moves/stretch.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1142 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/moves/walk.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      475 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/mpi_pool.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1318 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/pbar.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      497 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/ptsampler.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1992 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/state.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1731 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/emcee/utils.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/_lib/test/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      320 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/_lib/test/test_import.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2412 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/_lib/test/test_util.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8014 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/_lib/util.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/analysis/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      805 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/analysis/__init__.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9244 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/analysis/bounds.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    35031 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/analysis/curvefitter.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4821 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/analysis/model.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    37887 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/analysis/objective.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    23085 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/analysis/parameter.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/analysis/test/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7227 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NISTModels.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6874 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Bennett5.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1718 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/BoxBOD.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7561 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Chwirut1.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3064 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Chwirut2.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2007 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/DanWood.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6770 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/ENSO.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2776 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Eckerle4.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8107 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Gauss1.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8106 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Gauss2.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8108 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Gauss3.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9757 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Hahn1.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5862 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Kirby2.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2948 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Lanczos1.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2605 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Lanczos2.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2577 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Lanczos3.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2322 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/MGH09.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2345 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/MGH10.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3085 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/MGH17.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1858 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Misra1a.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1850 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Misra1b.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1858 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Misra1c.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1845 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Misra1d.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6425 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Models
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7006 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Nelson.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1876 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Rat42.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2093 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Rat43.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2488 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Roszman1.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3031 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/NIST_STRD/Thurber.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    18785 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/c_PLP0011859_q.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    13701 2019-02-03 22:13:25.000000 refnx-0.1.8/refnx/analysis/test/c_PLP0016596.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9704 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/c_PLP0016601.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    10404 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/c_PLP0016607.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5346 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/e361r.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3142 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/e365r.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3119 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/e366r.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5569 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/gauss_data.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   279631 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/analysis/test/resolution_comparison.ipynb
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3416 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/analysis/test/test_bounds.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    19519 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/analysis/test/test_curvefitter.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6203 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/analysis/test/test_globalfitting.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1698 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/analysis/test/test_model.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    16975 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/analysis/test/test_objective.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8980 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/analysis/test/test_parameter.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/dataset/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      247 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/dataset/__init__.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    17236 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/dataset/data1d.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4706 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/dataset/reflectdataset.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/dataset/test/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4181 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/dataset/test/c_PLP0000708.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4961 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/dataset/test/c_PLP0000708.xml
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4221 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/dataset/test/c_PLP0000708_header.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4254 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/dataset/test/c_PLP0000708_header2.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7762 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/dataset/test/c_PLP0033831.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1286 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/dataset/test/coef_c_PLP0000708.xml
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1439 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/dataset/test/d_a.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1601 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/dataset/test/dot.aft
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1607 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/dataset/test/dot.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    13035 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/dataset/test/dot.mft
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    59920 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/dataset/test/dot.out
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2771 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/dataset/test/dot.refl
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8385 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/dataset/test/test_reflectdataset.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reduce/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      638 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/reduce/__init__.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reduce/_app/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      685 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/reduce/_app/__init__.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    11828 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/reduce/_app/model.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4315 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/reduce/_app/plot.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reduce/_app/ui/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2930 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/reduce/_app/ui/event.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6351 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/reduce/_app/ui/manual_beam.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5233 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/reduce/_app/ui/reduction_options.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7731 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/reduce/_app/ui/slim.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9332 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/reduce/_app/view.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reduce/batch_reduce/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6656 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/batch_reduce/reduction.xlt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    17457 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/batchreduction.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4643 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/bounded_splines.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8789 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reduce/event.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    20189 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/reduce/manual_beam_finder.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6939 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/parabolic_motion.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3346 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/peak_utils.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    78697 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/reduce/platypusnexus.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7570 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reduce/rebin.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    23000 2019-05-08 23:53:43.000000 refnx-0.1.8/refnx/reduce/reduce.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reduce/test/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    11596 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/11613_spectrum_slim.txt
--rwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)     7645 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/180706_HA_DG2.xrdml
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reduce/test/DAQ_2012-01-20T21-50-32/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    19505 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/DAQ_2012-01-20T21-50-32/CFG.xml
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reduce/test/DAQ_2012-01-20T21-50-32/DATASET_0/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)  9364033 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/DAQ_2012-01-20T21-50-32/DATASET_0/EOS.bin
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   360889 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/PLP0000708.nx.hdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   361101 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/PLP0000709.nx.hdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   383339 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/PLP0000710.nx.hdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   413263 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/PLP0000711.nx.hdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   374616 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/PLP0011613.nx.hdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   427970 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/PLP0011641.nx.hdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   442664 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/PLP0011658.nx.hdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   427425 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/PLP0038417.nx.hdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   416699 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/PLP0038418.nx.hdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   410684 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/PLP0038420.nx.hdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   423597 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/PLP0038421.nx.hdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3296 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/background_subtract.npy
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5784 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/flood.h5
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    17755 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/parabolic_geometry.pdf
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6069 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/test_batch_reduce.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    18944 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/test_batch_reduction.xls
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5418 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reduce/test/test_event.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2603 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/test_parabolic_motion.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1266 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/test_peak_utils.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    12131 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reduce/test/test_platypusnexus.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9571 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reduce/test/test_rebin.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3568 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/test_reduce.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      425 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/test/test_xray.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7985 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reduce/xray.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reflect/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1040 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/__init__.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reflect/_app/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3002 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/reflect/_app/SLD_calculator_view.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1272 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/_app/__init__.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    10538 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_app/_lipid_leaflet.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5911 2019-07-12 02:02:58.000000 refnx-0.1.8/refnx/reflect/_app/_mcmc.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2922 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/reflect/_app/_optimisation_parameters.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2233 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_app/_spline.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2727 2019-02-05 05:05:00.000000 refnx-0.1.8/refnx/reflect/_app/dataobject.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3384 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/_app/datastore.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2814 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/graphproperties.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   301625 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/icons/Motofit.icns
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    24747 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/TMCL.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    24676 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/TOCL.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      334 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_app/icons/branch-closed.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      197 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_app/icons/branch-end.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      211 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_app/icons/branch-more.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      346 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_app/icons/branch-open.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    25951 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/d31-POPC.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    12104 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/d31-POPE.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    12301 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/d31-POPG.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    27733 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/d31-POPS.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    16829 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/d54-DMPC.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    16050 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/d54-DMPG.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    15537 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/d62-DPPC.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    14565 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/d9-POPC.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    31270 2019-02-04 02:58:12.000000 refnx-0.1.8/refnx/reflect/_app/icons/go.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9224 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/h-DMPC.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9606 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/h-DMPG.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8777 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/h-DPPC.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8847 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/h-POPC.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8813 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/h-POPE.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9245 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/h-POPG.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    10352 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/icons/h-POPS.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      779 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/icons/minus.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7016 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/icons/plus.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   107414 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/icons/scattering.ico
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   131164 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_app/icons/scattering.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5729 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/icons/scatteringevent.svg
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      124 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_app/icons/vline.png
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7482 2019-02-03 22:14:23.000000 refnx-0.1.8/refnx/reflect/_app/lipids.json
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      368 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_app/resources.qrc
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   711044 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_app/resources_rc.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reflect/_app/test/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2159 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/reflect/_app/test/test_app.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      517 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/reflect/_app/test/test_graphproperties.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    41794 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/reflect/_app/treeview_gui_model.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reflect/_app/ui/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5093 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/SLDcalculator.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1722 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/about.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1756 2019-02-05 23:24:39.000000 refnx-0.1.8/refnx/reflect/_app/ui/data_object_selector.ui
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reflect/_app/ui/licences/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2014 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/licences/about
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4842 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/licences/matplotlib
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2327 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/licences/numpy
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1033 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/licences/pyparsing
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    35214 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/licences/pyqt5
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2905 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/licences/python-dateutil
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7684 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/licences/qt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8736 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/licences/scipy
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8832 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_app/ui/lipid_leaflet.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    39713 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/_app/ui/motofit.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    24783 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/_app/ui/optimisation.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3132 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/_app/ui/process_mcmc.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    13114 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/progress.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3487 2019-01-31 04:17:11.000000 refnx-0.1.8/refnx/reflect/_app/ui/qrangedialog.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3842 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/_app/ui/sample_mcmc.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3427 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/_app/ui/spline.ui
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    89825 2019-07-12 02:02:58.000000 refnx-0.1.8/refnx/reflect/_app/view.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    10748 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/reflect/_code_fragment.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    49678 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/_interactive_modeller.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    12144 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/_lipid.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    11137 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/_reflect.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4335 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/interface.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    29722 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/reflect_model.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8321 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/spline.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    44308 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/structure.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/reflect/test/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    18785 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reflect/test/c_PLP0011859_q.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5346 2019-01-23 06:15:42.000000 refnx-0.1.8/refnx/reflect/test/e361r.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1166 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/test/gsmear.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8136 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/test/refl1d.npy
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    25050 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reflect/test/sld_theoretical_R.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    20366 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reflect/test/smeared_theoretical.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1500 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reflect/test/smearingprecision.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2433 2019-02-04 01:10:25.000000 refnx-0.1.8/refnx/reflect/test/test__code_fragment.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3226 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/reflect/test/test__interactive_modeller.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3061 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/reflect/test/test__lipid.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1130 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/test/test_interface.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    23382 2019-06-25 02:03:15.000000 refnx-0.1.8/refnx/reflect/test/test_reflect.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6352 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/test/test_spline.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    11378 2019-07-10 00:55:10.000000 refnx-0.1.8/refnx/reflect/test/test_structure.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    14238 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/reflect/test/theoretical.txt
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/util/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2039 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/util/ErrorProp.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1224 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/util/__init__.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9170 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/util/_resolution_kernel.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    18682 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/util/general.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2395 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/util/nsplice.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      758 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/util/quickplot.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx/util/test/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    32245 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/util/test/PLP0000708.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    33234 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/util/test/PLP0000709.dat
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2431 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/util/test/test_ErrorProp.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1318 2019-05-08 23:53:44.000000 refnx-0.1.8/refnx/util/test/test_general.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3908 2019-01-16 22:34:47.000000 refnx-0.1.8/refnx/util/test/test_nsplice.py
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      227 2019-07-12 03:44:22.000000 refnx-0.1.8/refnx/version.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/refnx.egg-info/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      970 2019-07-12 03:44:22.000000 refnx-0.1.8/refnx.egg-info/PKG-INFO
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8975 2019-07-12 03:44:22.000000 refnx-0.1.8/refnx.egg-info/SOURCES.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)        1 2019-07-12 03:44:22.000000 refnx-0.1.8/refnx.egg-info/dependency_links.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)       67 2019-07-12 03:44:22.000000 refnx-0.1.8/refnx.egg-info/entry_points.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)        1 2019-07-12 03:44:22.000000 refnx-0.1.8/refnx.egg-info/not-zip-safe
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      131 2019-07-12 03:44:22.000000 refnx-0.1.8/refnx.egg-info/requires.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)       17 2019-07-12 03:44:22.000000 refnx-0.1.8/refnx.egg-info/top_level.txt
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)       79 2019-07-12 03:44:23.000000 refnx-0.1.8/setup.cfg
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8555 2019-07-12 03:42:47.000000 refnx-0.1.8/setup.py
-drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-07-12 03:44:23.000000 refnx-0.1.8/src/
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4452 2019-05-08 23:53:44.000000 refnx-0.1.8/src/MyComplex.h
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4992 2019-01-16 22:34:48.000000 refnx-0.1.8/src/_cevent.pyx
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6176 2019-07-10 00:55:10.000000 refnx-0.1.8/src/_creflect.pyx
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      956 2019-06-25 02:03:15.000000 refnx-0.1.8/src/_cutil.pyx
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    14668 2019-07-10 00:55:10.000000 refnx-0.1.8/src/refcalc.cpp
--rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3532 2019-07-10 00:55:10.000000 refnx-0.1.8/src/refcalc.h
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)       68 2019-01-16 22:34:46.000000 refnx-0.1.9/MANIFEST.in
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      970 2019-08-18 23:32:25.000000 refnx-0.1.9/PKG-INFO
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      710 2019-01-16 22:34:46.000000 refnx-0.1.9/README.md
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/benchmarks/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)       74 2019-01-16 22:34:46.000000 refnx-0.1.9/benchmarks/__init__.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/benchmarks/benchmarks/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-01-16 22:34:46.000000 refnx-0.1.9/benchmarks/benchmarks/__init__.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1710 2019-01-16 22:34:46.000000 refnx-0.1.9/benchmarks/benchmarks/analysis.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2386 2019-01-16 22:34:46.000000 refnx-0.1.9/benchmarks/benchmarks/common.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2367 2019-01-16 22:34:46.000000 refnx-0.1.9/benchmarks/benchmarks/reflect.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1917 2019-01-16 22:34:46.000000 refnx-0.1.9/benchmarks/run.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      370 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/__init__.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/_lib/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      526 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/_lib/__init__.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2959 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/_numdiff.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1303 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/_lib/_testutils.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/_lib/emcee/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1109 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/LICENSE
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      732 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/__init__.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4040 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/autocorr.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/_lib/emcee/backends/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      436 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/backends/__init__.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8198 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/backends/backend.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6656 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/backends/hdf.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    18962 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/ensemble.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      219 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/interruptible_pool.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      229 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/model.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/_lib/emcee/moves/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      483 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/moves/__init__.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1612 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/moves/de.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1543 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/moves/de_snooker.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4020 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/moves/gaussian.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1276 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/moves/kde.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2440 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/moves/mh.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1700 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/moves/move.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4093 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/moves/red_blue.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      970 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/moves/stretch.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1142 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/moves/walk.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      475 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/mpi_pool.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1318 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/pbar.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      497 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/ptsampler.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1992 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/state.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1731 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/emcee/utils.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/_lib/test/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      320 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/_lib/test/test_import.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2412 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/_lib/test/test_util.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8016 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/_lib/util.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/analysis/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      805 2019-08-06 06:14:32.000000 refnx-0.1.9/refnx/analysis/__init__.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    10162 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/analysis/bounds.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    35123 2019-08-12 07:16:06.000000 refnx-0.1.9/refnx/analysis/curvefitter.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4821 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/analysis/model.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    37946 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/analysis/objective.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    23085 2019-08-06 06:14:32.000000 refnx-0.1.9/refnx/analysis/parameter.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/analysis/test/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7227 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NISTModels.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6874 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Bennett5.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1718 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/BoxBOD.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7561 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Chwirut1.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3064 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Chwirut2.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2007 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/DanWood.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6770 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/ENSO.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2776 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Eckerle4.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8107 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Gauss1.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8106 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Gauss2.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8108 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Gauss3.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9757 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Hahn1.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5862 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Kirby2.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2948 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Lanczos1.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2605 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Lanczos2.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2577 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Lanczos3.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2322 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/MGH09.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2345 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/MGH10.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3085 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/MGH17.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1858 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Misra1a.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1850 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Misra1b.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1858 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Misra1c.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1845 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Misra1d.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6425 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Models
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7006 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Nelson.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1876 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Rat42.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2093 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Rat43.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2488 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Roszman1.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3031 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/NIST_STRD/Thurber.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    18785 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/c_PLP0011859_q.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    13701 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/analysis/test/c_PLP0016596.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9704 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/c_PLP0016601.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    10404 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/c_PLP0016607.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5346 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/e361r.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3142 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/e365r.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3119 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/e366r.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5569 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/gauss_data.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   279631 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/analysis/test/resolution_comparison.ipynb
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3746 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/analysis/test/test_bounds.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    19519 2019-08-06 06:14:32.000000 refnx-0.1.9/refnx/analysis/test/test_curvefitter.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6203 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/analysis/test/test_globalfitting.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1698 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/analysis/test/test_model.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    16975 2019-08-06 06:14:32.000000 refnx-0.1.9/refnx/analysis/test/test_objective.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8980 2019-08-06 06:14:32.000000 refnx-0.1.9/refnx/analysis/test/test_parameter.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/dataset/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      247 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/dataset/__init__.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    17236 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/dataset/data1d.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4706 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/dataset/reflectdataset.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/dataset/test/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4181 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/dataset/test/c_PLP0000708.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4961 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/dataset/test/c_PLP0000708.xml
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4221 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/dataset/test/c_PLP0000708_header.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4254 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/dataset/test/c_PLP0000708_header2.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7762 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/dataset/test/c_PLP0033831.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1286 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/dataset/test/coef_c_PLP0000708.xml
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1439 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/dataset/test/d_a.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1601 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/dataset/test/dot.aft
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1607 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/dataset/test/dot.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    13035 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/dataset/test/dot.mft
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    59920 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/dataset/test/dot.out
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2771 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/dataset/test/dot.refl
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8385 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/dataset/test/test_reflectdataset.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reduce/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      621 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/__init__.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reduce/_app/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      685 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reduce/_app/__init__.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    11828 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/_app/model.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4315 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reduce/_app/plot.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reduce/_app/ui/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2930 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/_app/ui/event.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6455 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/_app/ui/manual_beam.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5234 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/_app/ui/reduction_options.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7731 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reduce/_app/ui/slim.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9332 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reduce/_app/view.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reduce/batch_reduce/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6656 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/batch_reduce/reduction.xlt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    17457 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/batchreduction.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4643 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/bounded_splines.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8789 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reduce/event.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    21254 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/manual_beam_finder.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6939 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/parabolic_motion.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3346 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/peak_utils.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    79002 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/platypusnexus.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7570 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/rebin.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    23013 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/reduce.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reduce/test/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    11596 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/11613_spectrum_slim.txt
+-rwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)     7645 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/180706_HA_DG2.xrdml
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reduce/test/DAQ_2012-01-20T21-50-32/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    19505 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/DAQ_2012-01-20T21-50-32/CFG.xml
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reduce/test/DAQ_2012-01-20T21-50-32/DATASET_0/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)  9364033 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/DAQ_2012-01-20T21-50-32/DATASET_0/EOS.bin
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   360889 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/PLP0000708.nx.hdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   361101 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/PLP0000709.nx.hdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   383339 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/PLP0000710.nx.hdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   413263 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/PLP0000711.nx.hdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   374616 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/PLP0011613.nx.hdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   427970 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/PLP0011641.nx.hdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   442664 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/PLP0011658.nx.hdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   427425 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/PLP0038417.nx.hdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   416699 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/PLP0038418.nx.hdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   410684 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/PLP0038420.nx.hdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   423597 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/PLP0038421.nx.hdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3296 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/background_subtract.npy
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5784 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/flood.h5
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    17755 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/parabolic_geometry.pdf
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6413 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/test/test_batch_reduce.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    18944 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/test_batch_reduction.xls
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5552 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/test/test_event.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2603 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/test_parabolic_motion.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1266 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/test_peak_utils.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    12359 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/test/test_platypusnexus.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9571 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/test/test_rebin.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4195 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reduce/test/test_reduce.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      425 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/test/test_xray.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7985 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reduce/xray.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reflect/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1365 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/__init__.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reflect/_app/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3002 2019-08-06 06:14:32.000000 refnx-0.1.9/refnx/reflect/_app/SLD_calculator_view.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1272 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/__init__.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    10538 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/_lipid_leaflet.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5911 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/_mcmc.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2922 2019-08-06 06:14:32.000000 refnx-0.1.9/refnx/reflect/_app/_optimisation_parameters.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2233 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/_spline.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2727 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/dataobject.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3384 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/datastore.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2814 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/graphproperties.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reflect/_app/icons/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    43952 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/icons/18_1 Diether PC.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    42995 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/icons/DOTAP.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   301625 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/icons/Motofit.icns
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    24747 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/TMCL.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    24676 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/TOCL.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      334 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/branch-closed.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      197 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/branch-end.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      211 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/branch-more.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      346 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/branch-open.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    25951 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/d31-POPC.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    12104 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/d31-POPE.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    12301 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/d31-POPG.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    27733 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/d31-POPS.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    16829 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/d54-DMPC.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    16050 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/d54-DMPG.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    15537 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/d62-DPPC.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    14565 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/d9-POPC.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    31270 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/go.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9224 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/h-DMPC.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9606 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/h-DMPG.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    50144 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/icons/h-DOPC.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8777 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/h-DPPC.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8847 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/h-POPC.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8813 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/h-POPE.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9245 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/h-POPG.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    10352 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/h-POPS.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      779 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/icons/minus.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7016 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/icons/plus.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   107414 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/icons/scattering.ico
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   131164 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/scattering.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5729 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/icons/scatteringevent.svg
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      124 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/icons/vline.png
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8775 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/lipids.json
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      368 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/resources.qrc
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)   711044 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/resources_rc.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reflect/_app/test/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2159 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/test/test_app.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      517 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/test/test_graphproperties.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    41794 2019-08-06 06:14:32.000000 refnx-0.1.9/refnx/reflect/_app/treeview_gui_model.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reflect/_app/ui/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5093 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/SLDcalculator.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1722 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/about.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1756 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/ui/data_object_selector.ui
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reflect/_app/ui/licences/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2014 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/licences/about
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4842 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/licences/matplotlib
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2327 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/licences/numpy
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1033 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/licences/pyparsing
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    35214 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/licences/pyqt5
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2905 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/licences/python-dateutil
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     7684 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/licences/qt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8736 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/licences/scipy
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8832 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_app/ui/lipid_leaflet.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    39713 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/ui/motofit.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    24783 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/ui/optimisation.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3132 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/ui/process_mcmc.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    13114 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/progress.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3487 2019-01-31 04:17:11.000000 refnx-0.1.9/refnx/reflect/_app/ui/qrangedialog.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3842 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/ui/sample_mcmc.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3427 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/ui/spline.ui
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    89833 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_app/view.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    10748 2019-08-06 06:14:32.000000 refnx-0.1.9/refnx/reflect/_code_fragment.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    49678 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_interactive_modeller.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    12144 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/_lipid.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    14267 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/_reflect.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4335 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/interface.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    31621 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/reflect_model.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8321 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/spline.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    41271 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/structure.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/reflect/test/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    18785 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reflect/test/c_PLP0011859_q.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5346 2019-01-23 06:15:42.000000 refnx-0.1.9/refnx/reflect/test/e361r.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1166 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/test/gsmear.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     8136 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/test/refl1d.npy
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    25050 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reflect/test/sld_theoretical_R.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    20366 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reflect/test/smeared_theoretical.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1500 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reflect/test/smearingprecision.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2433 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/test/test__code_fragment.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3226 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/test/test__interactive_modeller.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3061 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/reflect/test/test__lipid.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1130 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/test/test_interface.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    27327 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/test/test_reflect.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     6352 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/test/test_spline.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    11735 2019-08-09 03:59:55.000000 refnx-0.1.9/refnx/reflect/test/test_structure.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    14238 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/reflect/test/theoretical.txt
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/util/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2039 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/util/ErrorProp.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1224 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/util/__init__.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9170 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/util/_resolution_kernel.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    18682 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/util/general.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2395 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/util/nsplice.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      758 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/util/quickplot.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx/util/test/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    32245 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/util/test/PLP0000708.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    33234 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/util/test/PLP0000709.dat
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     2431 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/util/test/test_ErrorProp.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     1318 2019-07-16 00:32:57.000000 refnx-0.1.9/refnx/util/test/test_general.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3908 2019-01-16 22:34:47.000000 refnx-0.1.9/refnx/util/test/test_nsplice.py
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      227 2019-08-18 23:32:24.000000 refnx-0.1.9/refnx/version.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/refnx.egg-info/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      970 2019-08-18 23:32:24.000000 refnx-0.1.9/refnx.egg-info/PKG-INFO
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9110 2019-08-18 23:32:24.000000 refnx-0.1.9/refnx.egg-info/SOURCES.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)        1 2019-08-18 23:32:24.000000 refnx-0.1.9/refnx.egg-info/dependency_links.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)       67 2019-08-18 23:32:24.000000 refnx-0.1.9/refnx.egg-info/entry_points.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)        1 2019-08-18 23:32:24.000000 refnx-0.1.9/refnx.egg-info/not-zip-safe
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      131 2019-08-18 23:32:24.000000 refnx-0.1.9/refnx.egg-info/requires.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)       17 2019-08-18 23:32:24.000000 refnx-0.1.9/refnx.egg-info/top_level.txt
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      129 2019-08-18 23:32:25.000000 refnx-0.1.9/setup.cfg
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)    10459 2019-08-18 23:30:12.000000 refnx-0.1.9/setup.py
+drwxr-xr-x   0 anz      (219611003) ANSTO\Domain Users (799647625)        0 2019-08-18 23:32:25.000000 refnx-0.1.9/src/
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4452 2019-07-16 00:32:57.000000 refnx-0.1.9/src/MyComplex.h
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     4992 2019-01-16 22:34:48.000000 refnx-0.1.9/src/_cevent.pyx
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     5469 2019-08-09 03:59:55.000000 refnx-0.1.9/src/_creflect.pyx
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)      898 2019-08-12 07:16:06.000000 refnx-0.1.9/src/_cutil.pyx
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3618 2019-08-09 03:59:55.000000 refnx-0.1.9/src/_cyreflect.pyx
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     9026 2019-08-15 00:07:37.000000 refnx-0.1.9/src/refcalc.cpp
+-rw-r--r--   0 anz      (219611003) ANSTO\Domain Users (799647625)     3532 2019-08-09 03:59:55.000000 refnx-0.1.9/src/refcalc.h
```

### Comparing `refnx-0.1.8/PKG-INFO` & `refnx-0.1.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: refnx
-Version: 0.1.8
+Version: 0.1.9
 Summary: Neutron and X-ray Reflectometry Analysis
 Home-page: https://github.com/refnx/refnx
 Author: Andrew Nelson
 Author-email: andyfaff+refnx@gmail.com
 License: BSD
 Project-URL: Bug Tracker, https://github.com/refnx/refnx/issues
 Project-URL: Documentation, https://refnx.readthedocs.io/en/latest/
```

### Comparing `refnx-0.1.8/README.md` & `refnx-0.1.9/README.md`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/benchmarks/benchmarks/analysis.py` & `refnx-0.1.9/benchmarks/benchmarks/analysis.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/benchmarks/benchmarks/common.py` & `refnx-0.1.9/benchmarks/benchmarks/common.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/benchmarks/benchmarks/reflect.py` & `refnx-0.1.9/benchmarks/benchmarks/reflect.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/benchmarks/run.py` & `refnx-0.1.9/benchmarks/run.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/__init__.py` & `refnx-0.1.9/refnx/_lib/__init__.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/_numdiff.py` & `refnx-0.1.9/refnx/_lib/_numdiff.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/_testutils.py` & `refnx-0.1.9/refnx/_lib/_testutils.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/LICENSE` & `refnx-0.1.9/refnx/_lib/emcee/LICENSE`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/__init__.py` & `refnx-0.1.9/refnx/_lib/emcee/__init__.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/autocorr.py` & `refnx-0.1.9/refnx/_lib/emcee/autocorr.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/backends/backend.py` & `refnx-0.1.9/refnx/_lib/emcee/backends/backend.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/backends/hdf.py` & `refnx-0.1.9/refnx/_lib/emcee/backends/hdf.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/ensemble.py` & `refnx-0.1.9/refnx/_lib/emcee/ensemble.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/moves/de.py` & `refnx-0.1.9/refnx/_lib/emcee/moves/de.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/moves/de_snooker.py` & `refnx-0.1.9/refnx/_lib/emcee/moves/de_snooker.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/moves/gaussian.py` & `refnx-0.1.9/refnx/_lib/emcee/moves/gaussian.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/moves/kde.py` & `refnx-0.1.9/refnx/_lib/emcee/moves/kde.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/moves/mh.py` & `refnx-0.1.9/refnx/_lib/emcee/moves/mh.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/moves/move.py` & `refnx-0.1.9/refnx/_lib/emcee/moves/move.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/moves/red_blue.py` & `refnx-0.1.9/refnx/_lib/emcee/moves/red_blue.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/moves/stretch.py` & `refnx-0.1.9/refnx/_lib/emcee/moves/stretch.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/moves/walk.py` & `refnx-0.1.9/refnx/_lib/emcee/moves/walk.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/pbar.py` & `refnx-0.1.9/refnx/_lib/emcee/pbar.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/state.py` & `refnx-0.1.9/refnx/_lib/emcee/state.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/emcee/utils.py` & `refnx-0.1.9/refnx/_lib/emcee/utils.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/test/test_util.py` & `refnx-0.1.9/refnx/_lib/test/test_util.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/_lib/util.py` & `refnx-0.1.9/refnx/_lib/util.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 from multiprocessing import Pool, get_context
 import warnings as _warnings
 import os as _os
 import sys as _sys
 import functools
 from tempfile import mkdtemp
-from collections.abc import Iterable
 from contextlib import contextmanager
 from inspect import getfullargspec as _getargspecf
 
 
 def preserve_cwd(function):
     """
     Ensures that the original working directory is kept when exiting a function
@@ -108,33 +107,35 @@
                     pass
         try:
             self._rmdir(path)
         except OSError:
             pass
 
 
-def flatten(l):
+def flatten(seq):
     """
     Flatten a nested sequence.
 
     Parameters
     ----------
-    l : sequence
+    seq : sequence
         The sequence to flatten
 
     Returns
     -------
     el : generator
-        yields flattened sequences from l
+        yields flattened sequences from seq
     """
-    for el in l:
-        if (isinstance(el, Iterable) and
-                not isinstance(el, (str, bytes))):
+    for el in seq:
+        try:
+            iter(el)
+            if isinstance(el, (str, bytes)):
+                raise TypeError
             yield from flatten(el)
-        else:
+        except TypeError:
             yield el
 
 
 def unique(seq, idfun=id):
     """
     List of unique values in sequence (by object id, not by value).
     Ordering is preserved.
```

### Comparing `refnx-0.1.8/refnx/analysis/__init__.py` & `refnx-0.1.9/refnx/analysis/__init__.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/bounds.py` & `refnx-0.1.9/refnx/analysis/bounds.py`

 * *Files 4% similar despite different names*

```diff
@@ -15,15 +15,15 @@
     def logp(self, value):
         """
         Calculate the log-prior probability of a value with the probability
         distribution.
 
         Parameters
         ----------
-        val : float or np.ndarray
+        val : float or array-like
             variates to calculate the log-probability for
 
         Returns
         -------
         arr : float or np.ndarray
             The log-probabilty corresponding to each of the variates
 
@@ -109,15 +109,15 @@
     def logp(self, val):
         """
         Calculate the log-prior probability of a value with the probability
         distribution.
 
         Parameters
         ----------
-        val : float or np.ndarray
+        val : float or array-like
             variate to calculate the log-probability for
 
         Returns
         -------
         arr : float or np.ndarray
             The log-probabilty corresponding to each of the variates
 
@@ -136,15 +136,15 @@
             values to examine
 
         Returns
         -------
         valid : array-like
             valid values within the support
         """
-        _val = np.asfarray(val)
+        _val = np.asarray(val, dtype=float)
         valid = np.where(np.isfinite(self.logp(_val)),
                          _val,
                          self.rv.rvs(size=_val.shape))
 
         return valid
 
     def rvs(self, size=1, random_state=None):
@@ -206,14 +206,15 @@
         if lb is None:
             lb = -np.inf
         if ub is None:
             ub = np.inf
 
         self._lb = lb
         self._ub = ub
+        self._logprob = 0
         self.rv = None
         self._closed_bounds = False
         self._set_bounds(self._lb, self._ub)
 
     def _set_bounds(self, lb, ub):
         t_lb, t_ub = lb, ub
         self._lb = min(t_lb, t_ub)
@@ -221,16 +222,22 @@
         self._closed_bounds = False
 
         if np.isnan([self._lb, self._ub]).any():
             raise ValueError("Can't set Interval with NaN")
 
         if np.isfinite([self._lb, self._ub]).all():
             self._closed_bounds = True
+            if self._lb == self._ub:
+                self._logprob = 0.
+            else:
+                self._logprob = np.log(1 / (self._ub - self._lb))
+
             self.rv = uniform(self._lb, self._ub - self._lb)
         else:
+            self._logprob = 0.
             self._closed_bounds = False
 
     def __repr__(self):
         lb, ub = self.lb, self.ub
         if np.isneginf(self.lb):
             lb = '-np.inf'
         if np.isinf(self.ub):
@@ -263,23 +270,42 @@
     @ub.setter
     def ub(self, val):
         if val is None:
             val = np.inf
         self._set_bounds(self._lb, val)
 
     def logp(self, val):
-        _val = np.asfarray(val)
-        valid = np.logical_and(self._lb <= _val, _val <= self._ub)
+        """
+        Calculate the log-prior probability of a value with the Interval.
 
-        if self._closed_bounds:
-            # TODO special case where lb==ub==val?
-            prob = np.where(valid, np.log(1 / (self._ub - self._lb)), -np.inf)
-        else:
-            prob = np.where(valid, 0, -np.inf)
-        return prob
+        Parameters
+        ----------
+        val : float or array-like
+            variates to calculate the log-probability for
+
+        Returns
+        -------
+        arr : float or np.ndarray
+            The log-probabilty corresponding to each of the variates
+        """
+        # Special case when val is array-like. We'll assume that it may be
+        # array-like if it has a length. This special casing is done because
+        # a lot of time is spent on the `asarray`, `logical_and` and `where`.
+        # Most of the time val is a single float, so this speedup is
+        # appreciable.
+        if hasattr(val, '__len__'):
+            _val = np.asarray(val, dtype=float)
+            valid = np.logical_and(self._lb <= _val, _val <= self._ub)
+            prob = np.where(valid, self._logprob, -np.inf)
+            return prob
+
+        if self._lb <= val <= self._ub:
+            return self._logprob
+
+        return -np.inf
 
     def valid(self, val):
         """
         Checks whether a parameter value is within the support of the
         Interval. If it isn't then it returns a value that is within the
         support.
         If the Interval is closed (i.e. lower and upper bounds are both
@@ -301,15 +327,15 @@
 
         Examples
         --------
         >>> b = Interval(0, 10)
         >>> b.valid(11.5)
         8.5
         """
-        _val = np.asfarray(val)
+        _val = np.asarray(val, dtype=float)
         if self._closed_bounds:
             valid = np.where(np.isfinite(self.logp(_val)),
                              _val,
                              self.rvs(size=_val.shape))
         else:
             valid = np.where(_val < self._ub, _val, 2 * self._ub - _val)
             valid = np.where(valid > self._lb, valid, 2 * self._lb - valid)
```

### Comparing `refnx-0.1.8/refnx/analysis/curvefitter.py` & `refnx-0.1.9/refnx/analysis/curvefitter.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,14 +13,15 @@
 from refnx.analysis import Objective, Interval, PDF, is_parameter
 from refnx._lib import (unique as f_unique, MapWrapper,
                         possibly_open_file, flatten)
 from refnx._lib.util import getargspec
 
 from refnx._lib import emcee
 from refnx._lib.emcee.state import State
+from refnx._lib.emcee.pbar import get_progress_bar
 
 # PTSampler has been forked into a separate package. Try both places
 _HAVE_PTSAMPLER = False
 PTSampler = type(None)
 
 try:
     from ptemcee.sampler import Sampler as PTSampler
@@ -492,32 +493,30 @@
             if 'thin_by' in sampler_args:
                 kwargs['thin_by'] = nthin
                 kwargs.pop('thin', 0)
 
             # ptemcee returns coords, logpost
             # emcee returns a State object
             if isinstance(self.sampler, PTSampler):
-                for result in self.sampler.sample(self._state.coords,
-                                                  **kwargs):
-                    self._state = State(result[0],
-                                        log_prob=result[1] + result[2],
-                                        random_state=self.sampler._random)
-                    _callback_wrapper(self._state, h=h)
+                with get_progress_bar(verbose, total=steps) as pbar:
+                    for result in (self.sampler.sample(self._state.coords,
+                                                       **kwargs)):
+                        self._state = State(result[0],
+                                            log_prob=result[1] + result[2],
+                                            random_state=self.sampler._random)
+                        _callback_wrapper(self._state, h=h)
+                        pbar.update(1)
             else:
                 for state in self.sampler.sample(self._state,
                                                  **kwargs):
                     self._state = state
                     _callback_wrapper(state, h=h)
 
         self.sampler.pool = None
 
-        # finish off the progress bar
-        if verbose:
-            sys.stdout.write("\n")
-
         # sets parameter value and stderr
         return process_chain(self.objective, self.chain)
 
     def fit(self, method='L-BFGS-B', target='nll', **kws):
         """
         Obtain the maximum log-likelihood, or log-posterior, estimate (mode)
         of the objective. Maximising the log-likelihood is equivalent to
```

### Comparing `refnx-0.1.8/refnx/analysis/model.py` & `refnx-0.1.9/refnx/analysis/model.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/objective.py` & `refnx-0.1.9/refnx/analysis/objective.py`

 * *Files 1% similar despite different names*

```diff
@@ -298,16 +298,15 @@
         varying_parameters : refnx.analysis.Parameters
             The varying Parameter objects allowed to vary during the fit.
 
         """
         # create and return a Parameters object because it has the
         # __array__ method, which allows one to quickly get numerical values.
         p = Parameters()
-        p.data = [param for param in f_unique(flatten(self.parameters))
-                  if param.vary]
+        p.data = list(f_unique(p for p in flatten(self.parameters) if p.vary))
         return p
 
     def _data_transform(self, model=None):
         x = self.data.x
         y = self.data.y
 
         y_err = 1.
@@ -471,15 +470,17 @@
         `self.model.parameters` otherwise they'll be counted more than once.
         The same argument applies to the user specifiable `logp_extra`
         function.
 
         """
         self.setp(pvals)
 
-        logp = np.sum([param.logp() for param in self.varying_parameters()])
+        logp = np.sum([param.logp() for param in
+                       f_unique(p for p in flatten(self.parameters) if
+                                p.vary)])
 
         if not np.isfinite(logp):
             return -np.inf
 
         logp += self.model.logp()
 
         if not np.isfinite(logp):
```

### Comparing `refnx-0.1.8/refnx/analysis/parameter.py` & `refnx-0.1.9/refnx/analysis/parameter.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NISTModels.py` & `refnx-0.1.9/refnx/analysis/test/NISTModels.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Bennett5.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Bennett5.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/BoxBOD.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/BoxBOD.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Chwirut1.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Chwirut1.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Chwirut2.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Chwirut2.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/DanWood.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/DanWood.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/ENSO.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/ENSO.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Eckerle4.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Eckerle4.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Gauss1.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Gauss1.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Gauss2.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Gauss2.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Gauss3.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Gauss3.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Hahn1.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Hahn1.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Kirby2.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Kirby2.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Lanczos1.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Lanczos1.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Lanczos2.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Lanczos2.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Lanczos3.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Lanczos3.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/MGH09.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/MGH09.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/MGH10.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/MGH10.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/MGH17.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/MGH17.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Misra1a.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Misra1a.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Misra1b.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Misra1b.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Misra1c.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Misra1c.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Misra1d.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Misra1d.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Models` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Models`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Nelson.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Nelson.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Rat42.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Rat42.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Rat43.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Rat43.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Roszman1.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Roszman1.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/NIST_STRD/Thurber.dat` & `refnx-0.1.9/refnx/analysis/test/NIST_STRD/Thurber.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/c_PLP0011859_q.txt` & `refnx-0.1.9/refnx/analysis/test/c_PLP0011859_q.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/c_PLP0016596.dat` & `refnx-0.1.9/refnx/analysis/test/c_PLP0016596.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/c_PLP0016601.dat` & `refnx-0.1.9/refnx/analysis/test/c_PLP0016601.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/c_PLP0016607.dat` & `refnx-0.1.9/refnx/analysis/test/c_PLP0016607.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/e361r.txt` & `refnx-0.1.9/refnx/analysis/test/e361r.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/e365r.txt` & `refnx-0.1.9/refnx/analysis/test/e365r.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/e366r.txt` & `refnx-0.1.9/refnx/analysis/test/e366r.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/gauss_data.txt` & `refnx-0.1.9/refnx/analysis/test/gauss_data.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/resolution_comparison.ipynb` & `refnx-0.1.9/refnx/analysis/test/resolution_comparison.ipynb`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/test_bounds.py` & `refnx-0.1.9/refnx/analysis/test/test_bounds.py`

 * *Files 14% similar despite different names*

```diff
@@ -18,21 +18,29 @@
         assert_equal(interval.logp(0), 0)
 
         # semi closed interval
         interval.ub = 1000
         assert_equal(interval.logp(0), 0)
         assert_equal(interval.logp(1001), -np.inf)
 
+        # you should be able to send in multiple values
+        assert_equal(interval.logp(np.array([1., 1002.])),
+                     np.array([0, -np.inf]))
+
         # fully closed interval
         interval.lb = -1000
         assert_equal(interval.logp(-1001), -np.inf)
         assert_equal(interval.lb, -1000)
         assert_equal(interval.ub, 1000)
         assert_equal(interval.logp(0), np.log(1 / 2000.))
 
+        # you should be able to send in multiple values
+        assert_equal(interval.logp(np.array([1., 2.])),
+                     np.array([np.log(1 / 2000.)] * 2))
+
         # try and set lb higher than ub
         interval.lb = 1002
         assert_equal(interval.lb, 1000)
         assert_equal(interval.ub, 1002)
 
         # if val is outside closed range then rvs is used
         vals = interval.valid(np.linspace(990, 1005, 100))
```

### Comparing `refnx-0.1.8/refnx/analysis/test/test_curvefitter.py` & `refnx-0.1.9/refnx/analysis/test/test_curvefitter.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/test_globalfitting.py` & `refnx-0.1.9/refnx/analysis/test/test_globalfitting.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/test_model.py` & `refnx-0.1.9/refnx/analysis/test/test_model.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/test_objective.py` & `refnx-0.1.9/refnx/analysis/test/test_objective.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/analysis/test/test_parameter.py` & `refnx-0.1.9/refnx/analysis/test/test_parameter.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/data1d.py` & `refnx-0.1.9/refnx/dataset/data1d.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/reflectdataset.py` & `refnx-0.1.9/refnx/dataset/reflectdataset.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/c_PLP0000708.dat` & `refnx-0.1.9/refnx/dataset/test/c_PLP0000708.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/c_PLP0000708.xml` & `refnx-0.1.9/refnx/dataset/test/c_PLP0000708.xml`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/c_PLP0000708_header.dat` & `refnx-0.1.9/refnx/dataset/test/c_PLP0000708_header.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/c_PLP0000708_header2.dat` & `refnx-0.1.9/refnx/dataset/test/c_PLP0000708_header2.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/c_PLP0033831.txt` & `refnx-0.1.9/refnx/dataset/test/c_PLP0033831.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/coef_c_PLP0000708.xml` & `refnx-0.1.9/refnx/dataset/test/coef_c_PLP0000708.xml`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/d_a.txt` & `refnx-0.1.9/refnx/dataset/test/d_a.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/dot.aft` & `refnx-0.1.9/refnx/dataset/test/dot.aft`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/dot.dat` & `refnx-0.1.9/refnx/dataset/test/dot.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/dot.mft` & `refnx-0.1.9/refnx/dataset/test/dot.mft`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/dot.out` & `refnx-0.1.9/refnx/dataset/test/dot.out`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/dot.refl` & `refnx-0.1.9/refnx/dataset/test/dot.refl`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/dataset/test/test_reflectdataset.py` & `refnx-0.1.9/refnx/dataset/test/test_reflectdataset.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/__init__.py` & `refnx-0.1.9/refnx/reduce/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from refnx.reduce.reduce import PlatypusReduce, reduce_stitch
 from refnx.reduce.platypusnexus import (catalogue, PlatypusNexus,
                                         number_datafile, basename_datafile,
-                                        datafile_number, Y_PIXEL_SPACING,
-                                        accumulate_HDF_files, Catalogue)
+                                        datafile_number, accumulate_HDF_files,
+                                        Catalogue)
 from refnx.reduce.batchreduction import BatchReducer
 from refnx.reduce.xray import reduce_xrdml
 from refnx._lib._testutils import PytestTester
 from refnx.reduce._app import main, gui
 
 test = PytestTester(__name__)
 del PytestTester
```

### Comparing `refnx-0.1.8/refnx/reduce/_app/__init__.py` & `refnx-0.1.9/refnx/reduce/_app/__init__.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/_app/model.py` & `refnx-0.1.9/refnx/reduce/_app/model.py`

 * *Files 0% similar despite different names*

```diff
@@ -30,15 +30,15 @@
         # reduction and the reflected and direct beam runs
         self.reduction_entries = {}
 
         self.default_reduction_options = {
             'low_wavelength': (2.5, float),
             'high_wavelength': (19, float),
             'rebin_percent': (2., float),
-            'expected_centre': (123., float),
+            'expected_centre': (500., float),
             'manual_beam_find': (False, bool),
             'background_subtraction': (True, bool),
             'monitor_normalisation': (True, bool),
             'save_offspecular': (True, bool),
             'save_spectrum': (True, bool),
             'streamed_reduction': (False, bool)}
```

### Comparing `refnx-0.1.8/refnx/reduce/_app/plot.py` & `refnx-0.1.9/refnx/reduce/_app/plot.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/_app/ui/event.ui` & `refnx-0.1.9/refnx/reduce/_app/ui/event.ui`

 * *Files 0% similar despite different names*

#### Comparing `refnx-0.1.8/refnx/reduce/_app/ui/event.ui` & `refnx-0.1.9/refnx/reduce/_app/ui/event.ui`

```diff
@@ -6,15 +6,15 @@
       <enum>Qt::ApplicationModal</enum>
     </property>
     <property name="geometry">
       <rect>
         <x>0</x>
         <y>0</y>
         <width>400</width>
-        <height>300</height>
+        <height>275</height>
       </rect>
     </property>
     <property name="windowTitle">
       <string>Event mode</string>
     </property>
     <layout class="QGridLayout" name="gridLayout">
       <item row="0" column="0">
```

### Comparing `refnx-0.1.8/refnx/reduce/_app/ui/manual_beam.ui` & `refnx-0.1.9/refnx/reduce/_app/ui/manual_beam.ui`

 * *Files 2% similar despite different names*

#### Comparing `refnx-0.1.8/refnx/reduce/_app/ui/manual_beam.ui` & `refnx-0.1.9/refnx/reduce/_app/ui/manual_beam.ui`

```diff
@@ -6,15 +6,15 @@
       <enum>Qt::ApplicationModal</enum>
     </property>
     <property name="geometry">
       <rect>
         <x>0</x>
         <y>0</y>
         <width>944</width>
-        <height>532</height>
+        <height>511</height>
       </rect>
     </property>
     <property name="windowTitle">
       <string>Manual beam finder</string>
     </property>
     <layout class="QGridLayout" name="gridLayout_2">
       <property name="bottomMargin">
@@ -25,40 +25,40 @@
       </property>
       <item row="3" column="3">
         <widget class="QSpinBox" name="integrate_position">
           <property name="minimum">
             <number>1</number>
           </property>
           <property name="maximum">
-            <number>300</number>
+            <number>1024</number>
           </property>
           <property name="singleStep">
             <number>5</number>
           </property>
           <property name="value">
-            <number>121</number>
+            <number>500</number>
           </property>
         </widget>
       </item>
       <item row="2" column="3">
         <widget class="QSpinBox" name="integrate_width">
           <property name="showGroupSeparator" stdset="0">
             <bool>false</bool>
           </property>
           <property name="minimum">
             <number>5</number>
           </property>
           <property name="maximum">
-            <number>300</number>
+            <number>1000</number>
           </property>
           <property name="singleStep">
             <number>5</number>
           </property>
           <property name="value">
-            <number>50</number>
+            <number>200</number>
           </property>
         </widget>
       </item>
       <item row="2" column="2">
         <widget class="QLabel" name="label_2">
           <property name="text">
             <string>integrate width</string>
@@ -96,18 +96,18 @@
                   <string>centre</string>
                 </property>
               </widget>
             </item>
             <item row="0" column="1">
               <widget class="QDoubleSpinBox" name="true_centre">
                 <property name="maximum">
-                  <double>221.000000000000000</double>
+                  <double>1024.000000000000000</double>
                 </property>
                 <property name="value">
-                  <double>121.000000000000000</double>
+                  <double>500.000000000000000</double>
                 </property>
               </widget>
             </item>
             <item row="1" column="0">
               <widget class="QLabel" name="label_5">
                 <property name="text">
                   <string>fwhm</string>
@@ -115,14 +115,17 @@
               </widget>
             </item>
             <item row="1" column="1">
               <widget class="QDoubleSpinBox" name="true_fwhm">
                 <property name="minimum">
                   <double>0.500000000000000</double>
                 </property>
+                <property name="maximum">
+                  <double>800.000000000000000</double>
+                </property>
                 <property name="value">
                   <double>5.000000000000000</double>
                 </property>
               </widget>
             </item>
           </layout>
         </widget>
```

### Comparing `refnx-0.1.8/refnx/reduce/_app/ui/reduction_options.ui` & `refnx-0.1.9/refnx/reduce/_app/ui/reduction_options.ui`

 * *Files 1% similar despite different names*

#### Comparing `refnx-0.1.8/refnx/reduce/_app/ui/reduction_options.ui` & `refnx-0.1.9/refnx/reduce/_app/ui/reduction_options.ui`

```diff
@@ -3,15 +3,15 @@
   <class>reduction_options</class>
   <widget class="QDialog" name="reduction_options">
     <property name="geometry">
       <rect>
         <x>0</x>
         <y>0</y>
         <width>387</width>
-        <height>414</height>
+        <height>389</height>
       </rect>
     </property>
     <property name="windowTitle">
       <string>reduction options</string>
     </property>
     <layout class="QVBoxLayout" name="verticalLayout">
       <item>
@@ -98,21 +98,21 @@
           <property name="specialValueText">
             <string/>
           </property>
           <property name="decimals">
             <number>2</number>
           </property>
           <property name="maximum">
-            <double>221.000000000000000</double>
+            <double>1024.000000000000000</double>
           </property>
           <property name="singleStep">
             <double>1.000000000000000</double>
           </property>
           <property name="value">
-            <double>123.000000000000000</double>
+            <double>500.000000000000000</double>
           </property>
         </widget>
       </item>
       <item>
         <widget class="QCheckBox" name="background_subtraction">
           <property name="text">
             <string>background subtraction</string>
```

### Comparing `refnx-0.1.8/refnx/reduce/_app/ui/slim.ui` & `refnx-0.1.9/refnx/reduce/_app/ui/slim.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/_app/view.py` & `refnx-0.1.9/refnx/reduce/_app/view.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/batch_reduce/reduction.xlt` & `refnx-0.1.9/refnx/reduce/batch_reduce/reduction.xlt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/batchreduction.py` & `refnx-0.1.9/refnx/reduce/batchreduction.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/bounded_splines.py` & `refnx-0.1.9/refnx/reduce/bounded_splines.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/event.py` & `refnx-0.1.9/refnx/reduce/event.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/manual_beam_finder.py` & `refnx-0.1.9/refnx/reduce/manual_beam_finder.py`

 * *Files 2% similar despite different names*

```diff
@@ -33,24 +33,24 @@
         """
         """
         super(ManualBeamFinder, self).__init__()
         self.dialog = uic.loadUi(os.path.join(UI_LOCATION, 'manual_beam.ui'),
                                  self)
 
         # values for spinboxes
-        self._true_centre = 121.
-        self._true_sd = 5.
+        self._true_centre = 500.
+        self._true_sd = 20.
 
         self._pixels_to_include = 200
-        self._integrate_width = 50
-        self._integrate_position = 121
-        self._low_px = 122
-        self._high_px = 122
-        self._low_bkg = 122
-        self._high_bkg = 122
+        self._integrate_width = 200
+        self._integrate_position = 500
+        self._low_px = 500
+        self._high_px = 501
+        self._low_bkg = 503
+        self._high_bkg = 499
 
         # detector image
         self.detector_image_layout = QtWidgets.QGridLayout(
             self.dialog.detector_image)
         self.detector_image_layout.setObjectName("detector_image_layout")
 
         self.detector_image = DetectorImage(self.dialog.detector_image)
@@ -99,14 +99,21 @@
         n_images = 1
 
         if detector.ndim > 2:
             self.detector = detector[0]
             self.detector_err = detector_err[0]
             n_images = np.size(detector, 0)
 
+        # set min/max values for the detector image GUI. Crashes result
+        # otherwise
+        self.integrate_position.setMaximum(np.size(self.detector, -1) - 1)
+        self.integrate_width.setMaximum(np.size(self.detector, -1) - 1)
+        self.pixels_to_include.setMaximum(np.size(self.detector, 0))
+        self.true_centre.setMaximum(np.size(self.detector, -1))
+
         # guess peak centre from centroid.
         xs = np.sum(self.detector, axis=0)
         self._integrate_position, _ = centroid(xs)
         self.integrate_position.setValue(self._integrate_position)
         self.integrate_width.setValue(self._integrate_width)
 
         self.recalculate_graphs()
@@ -138,16 +145,24 @@
         beam_centre, beam_sd = peak_finder(xs, x=x)[1]
 
         self._true_centre = beam_centre
         self._true_sd = beam_sd
 
         regions = fore_back_region(beam_centre, beam_sd)
         self._low_px, self._high_px, bp = regions
-        self._low_bkg = np.min(bp[0])
-        self._high_bkg = np.max(bp[0])
+
+        # perhaps fore_back_region returned regions that weren't on the
+        # detector
+        self._low_px = np.clip(self._low_px, 0, np.size(self.detector, 1))
+        self._high_px = np.clip(self._high_px, 0, np.size(self.detector, 1))
+
+        # perhaps fore_back_region returned no background pixels
+        if len(bp[0]) > 0:
+            self._low_bkg = np.min(bp[0])
+            self._high_bkg = np.max(bp[0])
 
         self.detector_image.display_image(self.detector, beam_centre,
                                           self._low_px,
                                           self._high_px,
                                           self._low_bkg,
                                           self._high_bkg,
                                           self._pixels_to_include,
@@ -264,16 +279,24 @@
 
     @pyqtSlot(float)
     def on_true_centre_valueChanged(self, val):
         self._true_centre = val
 
         regions = fore_back_region(self._true_centre, self._true_sd)
         self._low_px, self._high_px, bp = regions
-        self._low_bkg = np.min(bp[0])
-        self._high_bkg = np.max(bp[0])
+
+        # perhaps fore_back_region returned regions that weren't on the
+        # detector
+        self._low_px = np.clip(self._low_px, 0, np.size(self.detector, 1))
+        self._high_px = np.clip(self._high_px, 0, np.size(self.detector, 1))
+
+        # perhaps fore_back_region returned no background pixels
+        if len(bp[0]) > 0:
+            self._low_bkg = np.min(bp[0])
+            self._high_bkg = np.max(bp[0])
 
         self.redraw_cross_section_regions()
 
     @pyqtSlot(float)
     def on_true_fwhm_valueChanged(self, val):
         self._true_sd = val / 2.3548
 
@@ -429,18 +452,18 @@
         super(Cross_Section, self).__init__(self.figure)
         self.setParent(parent)
 
         # information for dragging a line
         self._dragging = False
 
         # values for foreground and background regions
-        self._low_px = 112
-        self._high_px = 115
-        self._low_bkg = 110
-        self._high_bkg = 120
+        self._low_px = 500
+        self._high_px = 505
+        self._low_bkg = 490
+        self._high_bkg = 515
         self.line_attrs = {}
 
         self.axes = self.figure.add_axes([0.1, 0.07, 0.95, 0.94])
         self.axes.margins(0.0005)
 
         FigureCanvas.setSizePolicy(self,
                                    QtWidgets.QSizePolicy.Expanding,
```

### Comparing `refnx-0.1.8/refnx/reduce/parabolic_motion.py` & `refnx-0.1.9/refnx/reduce/parabolic_motion.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/peak_utils.py` & `refnx-0.1.9/refnx/reduce/peak_utils.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/platypusnexus.py` & `refnx-0.1.9/refnx/reduce/platypusnexus.py`

 * *Files 0% similar despite different names*

```diff
@@ -24,24 +24,21 @@
                                            parabola)
 from refnx.reduce.event import (events, process_event_stream,
                                 framebins_to_frames)
 from refnx.reduce.rebin import rebin, rebin_along_axis
 from refnx._lib import possibly_open_file
 
 
-# detector y pixel spacing in mm per pixel
-Y_PIXEL_SPACING = 1.177
-
 disc_openings = (60., 10., 25., 60.)
 O_C1d, O_C2d, O_C3d, O_C4d = disc_openings
 O_C1, O_C2, O_C3, O_C4 = np.radians(disc_openings)
 
 DISCRADIUS = 350.
 EXTENT_MULT = 2
-PIXEL_OFFSET = 1
+PIXEL_OFFSET = 4
 
 spectrum_template = """<?xml version="1.0"?>
 <REFroot xmlns="">
 <REFentry time="$time">
 <Title>$title</Title>
 <REFdata axes="lambda" rank="1" type="POINT"\
  spin="UNPOLARISED" dim="$n_spectra">
@@ -202,15 +199,24 @@
             'entry1/instrument/detector/vertical_translation'][:]
         d['original_file_name'] = h5d['entry1/experiment/file_name']
 
         d['scan_axis_name'] = (
             h5d['entry1/data/hmm'].attrs['axes'].decode('utf8').split(':')[0])
         d['scan_axis'] = h5d['entry1/data/%s' % d['scan_axis_name']][:]
 
-        # TODO put HDF file y pixel spacing in here.
+        try:
+            d['y_pixels_per_mm'] = h5d[
+                'entry1/instrument/parameters/y_pixels_per_mm'][:]
+        except KeyError:
+            # older PLP files didn't have y_pixels_per_mm, so use built in
+            # value
+            warnings.warn('Setting default pixel size to 1.177',
+                          RuntimeWarning)
+            d['y_pixels_per_mm'] = np.array([1.177])
+
         self.cat = d
 
     def __getattr__(self, item):
         return self.cat[item]
 
     @property
     def datafile_number(self):
@@ -842,15 +848,15 @@
             # first convert to beam sd, convolve in detector, and expand sd
             # back to total foreground width
             # use average of umb and penumb, the calc assumes a rectangular
             # distribution
             penumb = (np.sqrt((0.289 * 0.5 * (umb + penumb))**2. + 2.2**2) *
                       EXTENT_MULT * 2)
             # we need it in pixels
-            estimated_beam_width[idx] = penumb / Y_PIXEL_SPACING
+            estimated_beam_width[idx] = penumb / cat.y_pixels_per_mm[0]
 
             """
             work out the total flight length
             IMPORTANT: this varies as a function of twotheta. This is
             because the Platypus detector does not move on an arc.
             At high angles chod can be ~ 0.75% different. This is will
             visibly shift fringes.
@@ -907,21 +913,23 @@
 
         m_lambda = 0.5 * (m_lambda_hist[:, 1:] + m_lambda_hist[:, :-1])
         TOF -= t_offset
 
         # gravity correction if direct beam
         if direct:
             # TODO: Correlated Uncertainties?
-            output = correct_for_gravity(detector,
-                                         detector_sd,
-                                         m_lambda,
-                                         self.cat.collimation_distance,
-                                         self.cat.dy,
-                                         lo_wavelength,
-                                         hi_wavelength)
+            output = correct_for_gravity(
+                detector,
+                detector_sd,
+                m_lambda,
+                cat.collimation_distance,
+                cat.dy,
+                lo_wavelength,
+                hi_wavelength,
+                y_pixels_per_mm=cat.y_pixels_per_mm[0])
             detector, detector_sd, m_gravcorrcoefs = output
 
         # where is the specular ridge?
         if peak_pos == -1:
             # you always want to find the beam manually
             ret = manual_beam_find(detector, detector_sd)
             beam_centre, beam_sd, lopx, hipx, bp = ret
@@ -1201,15 +1209,15 @@
         scanpoint : int
             The scanpoint you're interested in
 
         Returns
         -------
         phase_angle, master_opening : float
             The phase angle in degrees, and the angular opening of the master
-            chopper
+            chopper in radians
         """
         cat = self.cat
         master = cat.master
         slave = cat.slave
         disc_phase = cat.phase[scanpoint]
         phase_angle = 0
 
@@ -1795,15 +1803,15 @@
                                        np.arange(y2[i], y3[i] + 1)])
 
     return lopx, hipx, background_pixels
 
 
 def correct_for_gravity(detector, detector_sd, lamda, coll_distance,
                         sample_det, lo_wavelength, hi_wavelength,
-                        theta=0):
+                        theta=0, y_pixels_per_mm=0.284):
     """
     Returns a gravity corrected yt plot, given the data, its associated errors,
     the wavelength corresponding to each of the time bins, and the trajectory
     of the neutrons. Low lambda and high Lambda are wavelength cutoffs to
     ignore.
 
     Parameters
@@ -1821,14 +1829,16 @@
     lo_wavelength : float
         Low wavelength cut off, Angstrom
     hi_wavelength : float
         High wavelength cutoff, Angstrom
     theta : float
         Angle between second collimation slit, first collimation slit, and
         horizontal
+    y_pixels_per_mm: float
+        size of one y pixel on the detector
 
     Returns
     -------
     corrected_data, corrected_data_sd, m_gravcorrcoefs :
         np.ndarray, np.ndarray, np.ndarray
 
         Corrected image. This is a theoretical prediction where the spectral
@@ -1857,28 +1867,28 @@
         hipx = np.searchsorted(lamda[spec], hi_wavelength)
 
         def f(tru_centre):
             deflections = y_deflection(trajectories[lopx: hipx],
                                        neutron_speeds[lopx: hipx],
                                        travel_distance)
 
-            model = 1000. * deflections / Y_PIXEL_SPACING + tru_centre
+            model = 1000. * deflections / y_pixels_per_mm + tru_centre
             diff = model - centroids[lopx: hipx, 0]
             diff = diff[~np.isnan(diff)]
             return diff
 
         # find the beam centre for an infinitely fast neutron
         x0 = np.array([np.nanmean(centroids[lopx: hipx, 0])])
         res = leastsq(f, x0)
         m_gravcorrcoefs[spec] = res[0][0]
 
         total_deflection = 1000. * y_deflection(trajectories,
                                                 neutron_speeds,
                                                 travel_distance)
-        total_deflection /= Y_PIXEL_SPACING
+        total_deflection /= y_pixels_per_mm
 
         x_rebin = x_init.T + total_deflection[:, np.newaxis]
         for wavelength in range(np.size(detector, axis=1)):
             output = rebin(x_init,
                            detector[spec, wavelength],
                            x_rebin[wavelength],
                            y1_sd=detector_sd[spec, wavelength])
```

### Comparing `refnx-0.1.8/refnx/reduce/rebin.py` & `refnx-0.1.9/refnx/reduce/rebin.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/reduce.py` & `refnx-0.1.9/refnx/reduce/reduce.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,16 +1,15 @@
 import string
 from copy import deepcopy
 import os.path
 from time import gmtime, strftime
 
 import numpy as np
 from refnx.reduce.platypusnexus import (PlatypusNexus, ReflectNexus,
-                                        number_datafile,
-                                        Y_PIXEL_SPACING, basename_datafile)
+                                        number_datafile, basename_datafile)
 from refnx.util import ErrorProp as EP
 import refnx.util.general as general
 from refnx.reduce.parabolic_motion import (parabola_line_intersection_point,
                                            find_trajectory)
 from refnx.dataset import ReflectDataset
 from refnx._lib import possibly_open_file
 
@@ -298,14 +297,16 @@
 
         detector_z_difference = (self.reflected_beam.detector_z -
                                  self.direct_beam.detector_z)
 
         beampos_z_difference = (self.reflected_beam.m_beampos -
                                 self.direct_beam.m_beampos)
 
+        Y_PIXEL_SPACING = self.reflected_beam.cat.y_pixels_per_mm[0]
+
         total_z_deflection = (detector_z_difference +
                               beampos_z_difference * Y_PIXEL_SPACING)
 
         if mode in ['FOC', 'POL', 'POLANAL', 'MT']:
             # omega_nom.shape = (N, )
             omega_nom = np.degrees(np.arctan(total_z_deflection /
                                    self.reflected_beam.detector_y) / 2.)
```

### Comparing `refnx-0.1.8/refnx/reduce/test/11613_spectrum_slim.txt` & `refnx-0.1.9/refnx/reduce/test/11613_spectrum_slim.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/180706_HA_DG2.xrdml` & `refnx-0.1.9/refnx/reduce/test/180706_HA_DG2.xrdml`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/DAQ_2012-01-20T21-50-32/CFG.xml` & `refnx-0.1.9/refnx/reduce/test/DAQ_2012-01-20T21-50-32/CFG.xml`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/DAQ_2012-01-20T21-50-32/DATASET_0/EOS.bin` & `refnx-0.1.9/refnx/reduce/test/DAQ_2012-01-20T21-50-32/DATASET_0/EOS.bin`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/PLP0000708.nx.hdf` & `refnx-0.1.9/refnx/reduce/test/PLP0000708.nx.hdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/PLP0000709.nx.hdf` & `refnx-0.1.9/refnx/reduce/test/PLP0000709.nx.hdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/PLP0000710.nx.hdf` & `refnx-0.1.9/refnx/reduce/test/PLP0000710.nx.hdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/PLP0000711.nx.hdf` & `refnx-0.1.9/refnx/reduce/test/PLP0000711.nx.hdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/PLP0011613.nx.hdf` & `refnx-0.1.9/refnx/reduce/test/PLP0011613.nx.hdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/PLP0011641.nx.hdf` & `refnx-0.1.9/refnx/reduce/test/PLP0011641.nx.hdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/PLP0011658.nx.hdf` & `refnx-0.1.9/refnx/reduce/test/PLP0011658.nx.hdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/PLP0038417.nx.hdf` & `refnx-0.1.9/refnx/reduce/test/PLP0038417.nx.hdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/PLP0038418.nx.hdf` & `refnx-0.1.9/refnx/reduce/test/PLP0038418.nx.hdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/PLP0038420.nx.hdf` & `refnx-0.1.9/refnx/reduce/test/PLP0038420.nx.hdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/PLP0038421.nx.hdf` & `refnx-0.1.9/refnx/reduce/test/PLP0038421.nx.hdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/background_subtract.npy` & `refnx-0.1.9/refnx/reduce/test/background_subtract.npy`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/flood.h5` & `refnx-0.1.9/refnx/reduce/test/flood.h5`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/parabolic_geometry.pdf` & `refnx-0.1.9/refnx/reduce/test/parabolic_geometry.pdf`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/test_batch_reduce.py` & `refnx-0.1.9/refnx/reduce/test/test_batch_reduce.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 import os.path
 import os
+import warnings
 import pandas
 import tempfile
 
 from numpy.testing import assert_equal, assert_
 import pytest
 
 from refnx.reduce import BatchReducer
@@ -25,31 +26,39 @@
         return 0
 
     def teardown_method(self):
         os.chdir(self.cwd)
 
     def test_batch_reduce(self):
         filename = os.path.join(self.path, "test_batch_reduction.xls")
-        b = BatchReducer(filename, data_folder=self.path, verbose=False,
-                         persistent=False)
+        # warnings filter for pixel size
+        with warnings.catch_warnings():
+            warnings.simplefilter('ignore', RuntimeWarning)
 
-        b.reduce(show=False)
+            b = BatchReducer(filename, data_folder=self.path, verbose=False,
+                             persistent=False)
+
+            b.reduce(show=False)
 
     def test_batch_reduce_ipython(self):
         filename = os.path.join(self.path, "test_batch_reduction.xls")
 
-        refnx.reduce.batchreduction._have_ipython = False
-        b = BatchReducer(filename, data_folder=self.path, verbose=False,
-                         persistent=False)
-        b.reduce(show=False)
-
-        refnx.reduce.batchreduction._have_ipython = True
-        b = BatchReducer(filename, data_folder=self.path, verbose=False,
-                         persistent=False)
-        b.reduce(show=False)
+        # warnings filter for pixel size
+        with warnings.catch_warnings():
+            warnings.simplefilter('ignore', RuntimeWarning)
+
+            refnx.reduce.batchreduction._have_ipython = False
+            b = BatchReducer(filename, data_folder=self.path, verbose=False,
+                             persistent=False)
+            b.reduce(show=False)
+
+            refnx.reduce.batchreduction._have_ipython = True
+            b = BatchReducer(filename, data_folder=self.path, verbose=False,
+                             persistent=False)
+            b.reduce(show=False)
 
 
 class TestReductionCache(object):
 
     entries = [
         # row, ds, name, fname, entry
         [1, None, "Sample A", "a.dat", (1, 2, 3)],
```

### Comparing `refnx-0.1.8/refnx/reduce/test/test_batch_reduction.xls` & `refnx-0.1.9/refnx/reduce/test/test_batch_reduction.xls`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/test_event.py` & `refnx-0.1.9/refnx/reduce/test/test_event.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,8 +1,10 @@
 import os
+import warnings
+
 import numpy as np
 from numpy.testing import assert_equal
 import refnx.reduce.event as event
 from refnx.reduce.event import events
 from refnx.reduce import PlatypusNexus
 
 try:
@@ -65,16 +67,21 @@
             assert_equal(cyf, f)
             assert_equal(cyt, t)
             assert_equal(cyy, y)
             assert_equal(cyx, x)
 
     def test_event_same_as_detector(self):
         # the detector file should be the same as the event file
-        orig_file = PlatypusNexus(os.path.join(self.path,
-                                               'PLP0011641.nx.hdf'))
+        # warnings filter for pixel size
+        with warnings.catch_warnings():
+            warnings.simplefilter('ignore', RuntimeWarning)
+
+            orig_file = PlatypusNexus(
+                os.path.join(self.path, 'PLP0011641.nx.hdf'))
+
         orig_det = orig_file.cat.detector
         frames = [np.arange(0, 501744)]
         event_det, fb = event.process_event_stream(self.event_list,
                                                    frames,
                                                    orig_file.cat.t_bins,
                                                    orig_file.cat.y_bins,
                                                    orig_file.cat.x_bins)
```

### Comparing `refnx-0.1.8/refnx/reduce/test/test_parabolic_motion.py` & `refnx-0.1.9/refnx/reduce/test/test_parabolic_motion.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/test_peak_utils.py` & `refnx-0.1.9/refnx/reduce/test/test_peak_utils.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/test_platypusnexus.py` & `refnx-0.1.9/refnx/reduce/test/test_platypusnexus.py`

 * *Files 3% similar despite different names*

```diff
@@ -17,18 +17,20 @@
 
 class TestPlatypusNexus(object):
 
     @pytest.fixture(autouse=True)
     def setup_method(self, tmpdir):
         self.pth = os.path.dirname(os.path.abspath(__file__))
 
-        self.f113 = PlatypusNexus(os.path.join(self.pth,
-                                               'PLP0011613.nx.hdf'))
-        self.f641 = PlatypusNexus(os.path.join(self.pth,
-                                               'PLP0011641.nx.hdf'))
+        with warnings.catch_warnings():
+            warnings.simplefilter('ignore', RuntimeWarning)
+            self.f113 = PlatypusNexus(os.path.join(self.pth,
+                                                   'PLP0011613.nx.hdf'))
+            self.f641 = PlatypusNexus(os.path.join(self.pth,
+                                                   'PLP0011641.nx.hdf'))
         self.cwd = os.getcwd()
 
         self.tmpdir = tmpdir.strpath
         os.chdir(self.tmpdir)
         return 0
 
     def teardown_method(self):
@@ -204,31 +206,34 @@
 
     def test_accumulate_files_reduce(self):
         # test by adding a file to itself. Should have smaller stats
         fnames = ['PLP0000708.nx.hdf', 'PLP0000708.nx.hdf']
         pths = [os.path.join(self.pth, fname) for fname in fnames]
         plp.accumulate_HDF_files(pths)
 
-        # it should be processable
-        fadd = PlatypusNexus(os.path.join(os.getcwd(),
-                                          'ADD_PLP0000708.nx.hdf'))
-        fadd.process()
-
-        # it should also be reduceable
-        reducer = PlatypusReduce(os.path.join(self.pth,
-                                              'PLP0000711.nx.hdf'))
-        datasets, reduced = reducer.reduce(os.path.join(os.getcwd(),
-                                           'ADD_PLP0000708.nx.hdf'))
-        assert_('y' in reduced)
-
-        # the error bars should be smaller
-        datasets2, reduced2 = reducer.reduce(os.path.join(self.pth,
-                                                          'PLP0000708.nx.hdf'))
+        with warnings.catch_warnings():
+            warnings.simplefilter('ignore', RuntimeWarning)
+            # it should be processable
+            fadd = PlatypusNexus(os.path.join(os.getcwd(),
+                                              'ADD_PLP0000708.nx.hdf'))
+            fadd.process()
+
+            # it should also be reduceable
+            reducer = PlatypusReduce(os.path.join(self.pth,
+                                                  'PLP0000711.nx.hdf'))
+
+            datasets, reduced = reducer.reduce(os.path.join(os.getcwd(),
+                                               'ADD_PLP0000708.nx.hdf'))
+            assert_('y' in reduced)
+
+            # the error bars should be smaller
+            datasets2, reduced2 = reducer.reduce(
+                os.path.join(self.pth, 'PLP0000708.nx.hdf'))
 
-        assert_(np.all(reduced['y_err'] < reduced2['y_err']))
+            assert_(np.all(reduced['y_err'] < reduced2['y_err']))
 
     def test_manual_beam_find(self):
         # you can specify a function that finds where the specular ridge is.
         def manual_beam_find(detector, detector_sd):
             beam_centre = np.zeros(len(detector))
             beam_sd = np.zeros(len(detector))
             beam_centre += 50
```

### Comparing `refnx-0.1.8/refnx/reduce/test/test_rebin.py` & `refnx-0.1.9/refnx/reduce/test/test_rebin.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reduce/test/test_reduce.py` & `refnx-0.1.9/refnx/reduce/test/test_reduce.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 import os
 import os.path
+import warnings
 import pytest
 
 from numpy.testing import (assert_equal, assert_allclose, assert_)
 import xml.etree.ElementTree as ET
 
 from refnx.reduce import reduce_stitch, PlatypusReduce
 
@@ -20,35 +21,43 @@
         return 0
 
     def teardown_method(self):
         os.chdir(self.cwd)
 
     def test_smoke(self):
         # a quick smoke test to check that the reduction can occur
-        a, fname = reduce_stitch([708, 709, 710], [711, 711, 711],
-                                 data_folder=self.pth, rebin_percent=2)
-        a.save('test1.dat')
+        # warnings filter for pixel size
+        with warnings.catch_warnings():
+            warnings.simplefilter('ignore', RuntimeWarning)
+            a, fname = reduce_stitch([708, 709, 710], [711, 711, 711],
+                                     data_folder=self.pth, rebin_percent=2)
+            a.save('test1.dat')
 
     def test_reduction_method(self):
         # a quick smoke test to check that the reduction can occur
-        a = PlatypusReduce('PLP0000711.nx.hdf', data_folder=self.pth)
+        # warnings filter for pixel size
+        with warnings.catch_warnings():
+            warnings.simplefilter('ignore', RuntimeWarning)
+
+            a = PlatypusReduce('PLP0000711.nx.hdf', data_folder=self.pth)
+
+            # try reduction with the reduce method
+            a.reduce('PLP0000708.nx.hdf', data_folder=self.pth,
+                     rebin_percent=4)
+
+            # try reduction with the __call__ method
+            a('PLP0000708.nx.hdf', data_folder=self.pth, rebin_percent=4)
+
+            # this should also have saved a couple of files in the current
+            # directory
+            assert_(os.path.isfile('./PLP0000708_0.dat'))
+            assert_(os.path.isfile('./PLP0000708_0.xml'))
 
-        # try reduction with the reduce method
-        a.reduce('PLP0000708.nx.hdf', data_folder=self.pth, rebin_percent=4)
-
-        # try reduction with the __call__ method
-        a('PLP0000708.nx.hdf', data_folder=self.pth, rebin_percent=4)
-
-        # this should also have saved a couple of files in the current
-        # directory
-        assert_(os.path.isfile('./PLP0000708_0.dat'))
-        assert_(os.path.isfile('./PLP0000708_0.xml'))
-
-        # try writing offspecular data
-        a.write_offspecular('offspec.xml', 0)
+            # try writing offspecular data
+            a.write_offspecular('offspec.xml', 0)
 
     def test_free_liquids(self):
         # smoke test for free liquids
         a0 = PlatypusReduce('PLP0038418.nx.hdf', data_folder=self.pth)
         a1 = PlatypusReduce('PLP0038417.nx.hdf', data_folder=self.pth)
 
         # try reduction with the reduce method
@@ -56,40 +65,45 @@
                            rebin_percent=4)
         d1, r1 = a1.reduce('PLP0038421.nx.hdf', data_folder=self.pth,
                            rebin_percent=4)
 
     def test_event_reduction(self):
         # check that eventmode reduction can occur, and that there are the
         # correct number of datasets produced.
-        a = PlatypusReduce(
-            os.path.join(self.pth, 'PLP0011613.nx.hdf'))
-
-        a.reduce(os.path.join(self.pth, 'PLP0011641.nx.hdf'),
-                 integrate=0, rebin_percent=2, eventmode=[0, 900, 1800])
-
-        assert_equal(a.y.shape[0], 2)
 
-        # check that two datasets are written out.
-        assert_(os.path.isfile('PLP0011641_0.dat'))
-        assert_(os.path.isfile('PLP0011641_1.dat'))
-
-        # check that the resolutions are pretty much the same
-        assert_allclose(a.x_err[0] / a.x[0],
-                        a.x_err[1] / a.x[1],
-                        atol=0.001)
-
-        # check that the (right?) timestamps are written into the datafile
-        tree = ET.parse(os.path.join(os.getcwd(), 'PLP0011641_1.xml'))
-        tree.find('.//REFentry').attrib['time']
-        # TODO, timestamp is created in the local time stamp of the testing
-        # machine. The following works if reduced with a computer in Australian
-        # EST.
-        # assert_(t == '2012-01-20T22:05:32')
-
-        # # what happens if you have too many frame bins
-        # # you should get the same number of fr
-        # a = PlatypusReduce(
-        #     os.path.join(self.pth, 'PLP0011613.nx.hdf'),
-        #     reflect=os.path.join(self.pth, 'PLP0011641.nx.hdf'),
-        #     integrate=0, rebin_percent=2,
-        #     eventmode=[0, 25200, 27000, 30000])
-        # assert_equal(a.ydata.shape[0], 3)
+        # warnings filter for pixel size
+        with warnings.catch_warnings():
+            warnings.simplefilter('ignore', RuntimeWarning)
+
+            a = PlatypusReduce(
+                os.path.join(self.pth, 'PLP0011613.nx.hdf'))
+
+            a.reduce(os.path.join(self.pth, 'PLP0011641.nx.hdf'),
+                     integrate=0, rebin_percent=2, eventmode=[0, 900, 1800])
+
+            assert_equal(a.y.shape[0], 2)
+
+            # check that two datasets are written out.
+            assert_(os.path.isfile('PLP0011641_0.dat'))
+            assert_(os.path.isfile('PLP0011641_1.dat'))
+
+            # check that the resolutions are pretty much the same
+            assert_allclose(a.x_err[0] / a.x[0],
+                            a.x_err[1] / a.x[1],
+                            atol=0.001)
+
+            # check that the (right?) timestamps are written into the datafile
+            tree = ET.parse(os.path.join(os.getcwd(), 'PLP0011641_1.xml'))
+            tree.find('.//REFentry').attrib['time']
+            # TODO, timestamp is created in the local time stamp of the testing
+            # machine. The following works if reduced with a computer in
+            # Australian EST.
+            # assert_(t == '2012-01-20T22:05:32')
+
+            # # what happens if you have too many frame bins
+            # # you should get the same number of fr
+            # a = PlatypusReduce(
+            #     os.path.join(self.pth, 'PLP0011613.nx.hdf'),
+            #     reflect=os.path.join(self.pth, 'PLP0011641.nx.hdf'),
+            #     integrate=0, rebin_percent=2,
+            #     eventmode=[0, 25200, 27000, 30000])
+            # assert_equal(a.ydata.shape[0], 3)
```

### Comparing `refnx-0.1.8/refnx/reduce/xray.py` & `refnx-0.1.9/refnx/reduce/xray.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/SLD_calculator_view.py` & `refnx-0.1.9/refnx/reflect/_app/SLD_calculator_view.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/__init__.py` & `refnx-0.1.9/refnx/reflect/_app/__init__.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/_lipid_leaflet.py` & `refnx-0.1.9/refnx/reflect/_app/_lipid_leaflet.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/_mcmc.py` & `refnx-0.1.9/refnx/reflect/_app/_mcmc.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/_optimisation_parameters.py` & `refnx-0.1.9/refnx/reflect/_app/_optimisation_parameters.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/_spline.py` & `refnx-0.1.9/refnx/reflect/_app/_spline.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/dataobject.py` & `refnx-0.1.9/refnx/reflect/_app/dataobject.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/datastore.py` & `refnx-0.1.9/refnx/reflect/_app/datastore.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/graphproperties.py` & `refnx-0.1.9/refnx/reflect/_app/graphproperties.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/Motofit.icns` & `refnx-0.1.9/refnx/reflect/_app/icons/Motofit.icns`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/TMCL.png` & `refnx-0.1.9/refnx/reflect/_app/icons/TMCL.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/TOCL.png` & `refnx-0.1.9/refnx/reflect/_app/icons/TOCL.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/d31-POPC.png` & `refnx-0.1.9/refnx/reflect/_app/icons/d31-POPC.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/d31-POPE.png` & `refnx-0.1.9/refnx/reflect/_app/icons/d31-POPE.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/d31-POPG.png` & `refnx-0.1.9/refnx/reflect/_app/icons/d31-POPG.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/d31-POPS.png` & `refnx-0.1.9/refnx/reflect/_app/icons/d31-POPS.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/d54-DMPC.png` & `refnx-0.1.9/refnx/reflect/_app/icons/d54-DMPC.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/d54-DMPG.png` & `refnx-0.1.9/refnx/reflect/_app/icons/d54-DMPG.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/d62-DPPC.png` & `refnx-0.1.9/refnx/reflect/_app/icons/d62-DPPC.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/d9-POPC.png` & `refnx-0.1.9/refnx/reflect/_app/icons/d9-POPC.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/go.png` & `refnx-0.1.9/refnx/reflect/_app/icons/go.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/h-DMPC.png` & `refnx-0.1.9/refnx/reflect/_app/icons/h-DMPC.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/h-DMPG.png` & `refnx-0.1.9/refnx/reflect/_app/icons/h-DMPG.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/h-DPPC.png` & `refnx-0.1.9/refnx/reflect/_app/icons/h-DPPC.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/h-POPC.png` & `refnx-0.1.9/refnx/reflect/_app/icons/h-POPC.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/h-POPE.png` & `refnx-0.1.9/refnx/reflect/_app/icons/h-POPE.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/h-POPG.png` & `refnx-0.1.9/refnx/reflect/_app/icons/h-POPG.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/h-POPS.png` & `refnx-0.1.9/refnx/reflect/_app/icons/h-POPS.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/minus.png` & `refnx-0.1.9/refnx/reflect/_app/icons/minus.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/plus.png` & `refnx-0.1.9/refnx/reflect/_app/icons/plus.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/scattering.ico` & `refnx-0.1.9/refnx/reflect/_app/icons/scattering.ico`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/scattering.png` & `refnx-0.1.9/refnx/reflect/_app/icons/scattering.png`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/icons/scatteringevent.svg` & `refnx-0.1.9/refnx/reflect/_app/icons/scatteringevent.svg`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/lipids.json` & `refnx-0.1.9/refnx/reflect/_app/lipids.json`

 * *Files 3% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.8571428571428571%*

 * *Differences: {'insert': "[(18, OrderedDict([('name', 'h-DOPC'), ('chemical_name', "*

 * *           "'1,2-dioleoyl-sn-glycero-3-phosphocholine'), ('head_formula', 'C10H18O8P1N1'), "*

 * *           "('tail_formula', 'C34H66'), ('references', ['Greenwood et al. Chem Phys Lipids. 2006 "*

 * *           "September ; 143(1-2): 1–10. doi:10.1016/j.chemphyslip.2006.04.002', 'Kucerka et al.  "*

 * *           "J. Membrane Biol. 208, 193 - 202 (2005)', 'Tristram-Nagle et al, Biophysical Journal "*

 * *           "Volume 75 August 1998 917–925']), ('con […]*

```diff
@@ -328,9 +328,64 @@
         "name": "TOCL",
         "references": [
             "For headgroup volume A.L. Boscia et al. (2014) Chem. Phys. Lipids 178: 1 - 10.",
             "For tail volume: DOPC tail volume x2 from: J.F. Nagle and S. Tristram-Nagle (2000) Biochim. Biophys. Acta: Rev. Biomembr. 1469: 159-195"
         ],
         "tail_exchangable": 0,
         "tail_formula": "C68H132"
+    },
+    {
+        "chemical_name": "1,2-dioleoyl-sn-glycero-3-phosphocholine",
+        "conditions": {
+            "ambient": [
+                319,
+                975
+            ]
+        },
+        "head_exchangable": 0,
+        "head_formula": "C10H18O8P1N1",
+        "name": "h-DOPC",
+        "references": [
+            "Greenwood et al. Chem Phys Lipids. 2006 September ; 143(1-2): 1\u201310. doi:10.1016/j.chemphyslip.2006.04.002",
+            "Kucerka et al.  J. Membrane Biol. 208, 193 - 202 (2005)",
+            "Tristram-Nagle et al, Biophysical Journal Volume 75 August 1998 917\u2013925"
+        ],
+        "tail_exchangable": 0,
+        "tail_formula": "C34H66"
+    },
+    {
+        "chemical_name": "Dioleoyl-3-trimethylammonium propane",
+        "conditions": {
+            "ambient": [
+                209.3,
+                975
+            ]
+        },
+        "head_exchangable": 0,
+        "head_formula": "C8H14O4N1",
+        "name": "DOTAP",
+        "references": [
+            "Based on DOPC as for DiEther DOPC"
+        ],
+        "tail_exchangable": 0,
+        "tail_formula": "C34H66"
+    },
+    {
+        "chemical_name": "1,2-di-O-(9Z-octadecenyl)-sn-glycero-3-phosphocholine",
+        "conditions": {
+            "ambient": [
+                291,
+                1092.2
+            ]
+        },
+        "head_exchangable": 0,
+        "head_formula": "C8H18O6N1P1",
+        "name": "18_1 Diether PC",
+        "references": [
+            "Calculations based on DOPC.  Adjustments made to headgroup regions on the basis of MD calculations. No Carbonyl in headgroup.  Therefore add 2 x CH2 to tails, also subtract C=O from HG.",
+            "Armen et al.  Biophysical Journal Volume 75 August 1998 734\u2013744",
+            ""
+        ],
+        "tail_exchangable": 0,
+        "tail_formula": "C36H70"
     }
 ]
```

### Comparing `refnx-0.1.8/refnx/reflect/_app/resources_rc.py` & `refnx-0.1.9/refnx/reflect/_app/resources_rc.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/test/test_app.py` & `refnx-0.1.9/refnx/reflect/_app/test/test_app.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/test/test_graphproperties.py` & `refnx-0.1.9/refnx/reflect/_app/test/test_graphproperties.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/treeview_gui_model.py` & `refnx-0.1.9/refnx/reflect/_app/treeview_gui_model.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/SLDcalculator.ui` & `refnx-0.1.9/refnx/reflect/_app/ui/SLDcalculator.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/about.ui` & `refnx-0.1.9/refnx/reflect/_app/ui/about.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/data_object_selector.ui` & `refnx-0.1.9/refnx/reflect/_app/ui/data_object_selector.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/licences/about` & `refnx-0.1.9/refnx/reflect/_app/ui/licences/about`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/licences/matplotlib` & `refnx-0.1.9/refnx/reflect/_app/ui/licences/matplotlib`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/licences/numpy` & `refnx-0.1.9/refnx/reflect/_app/ui/licences/numpy`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/licences/pyparsing` & `refnx-0.1.9/refnx/reflect/_app/ui/licences/pyparsing`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/licences/pyqt5` & `refnx-0.1.9/refnx/reflect/_app/ui/licences/pyqt5`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/licences/python-dateutil` & `refnx-0.1.9/refnx/reflect/_app/ui/licences/python-dateutil`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/licences/qt` & `refnx-0.1.9/refnx/reflect/_app/ui/licences/qt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/licences/scipy` & `refnx-0.1.9/refnx/reflect/_app/ui/licences/scipy`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/lipid_leaflet.ui` & `refnx-0.1.9/refnx/reflect/_app/ui/lipid_leaflet.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/motofit.ui` & `refnx-0.1.9/refnx/reflect/_app/ui/motofit.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/optimisation.ui` & `refnx-0.1.9/refnx/reflect/_app/ui/optimisation.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/process_mcmc.ui` & `refnx-0.1.9/refnx/reflect/_app/ui/process_mcmc.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/progress.ui` & `refnx-0.1.9/refnx/reflect/_app/ui/progress.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/qrangedialog.ui` & `refnx-0.1.9/refnx/reflect/_app/ui/qrangedialog.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/sample_mcmc.ui` & `refnx-0.1.9/refnx/reflect/_app/ui/sample_mcmc.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/ui/spline.ui` & `refnx-0.1.9/refnx/reflect/_app/ui/spline.ui`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_app/view.py` & `refnx-0.1.9/refnx/reflect/_app/view.py`

 * *Files 0% similar despite different names*

```diff
@@ -1277,16 +1277,16 @@
                 last_time = [time.time()]
 
                 def callback(coords, logprob):
                     completed[0] += 1
                     if (time.time() - last_time[0]) > 2:
                         last_time[0] = time.time()
                         progress.setValue(completed[0])
-                    if progress.wasCanceled():
-                        raise StopIteration("Sampling aborted")
+                        if progress.wasCanceled():
+                            raise StopIteration("Sampling aborted")
 
                 with open(os.path.join(folder, 'steps.chain'), 'w') as f,\
                         get_context('spawn').Pool() as workers:
                     fitter.sample(nsteps, f=f, verbose=True, nthin=nthin,
                                   callback=callback, pool=workers.map)
 
             except StopIteration:
```

### Comparing `refnx-0.1.8/refnx/reflect/_code_fragment.py` & `refnx-0.1.9/refnx/reflect/_code_fragment.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_interactive_modeller.py` & `refnx-0.1.9/refnx/reflect/_interactive_modeller.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_lipid.py` & `refnx-0.1.9/refnx/reflect/_lipid.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/_reflect.py` & `refnx-0.1.9/refnx/reflect/_reflect.py`

 * *Files 18% similar despite different names*

```diff
@@ -143,14 +143,115 @@
     r = (mrtot01 / mrtot00)
     reflectivity = r * np.conj(r)
     reflectivity *= scale
     reflectivity += bkg
     return np.real(np.reshape(reflectivity, qvals.shape))
 
 
+# The following slab contraction code was translated from C code in
+# the refl1d project.
+def _contract_by_area(slabs, dA=0.5):
+    """
+    Shrinks a slab representation to a reduced number of layers. This can
+    reduced calculation times.
+
+    Parameters
+    ----------
+    slabs : array
+        Has shape (N, 5).
+
+            slab[N, 0] - thickness of layer N
+            slab[N, 1] - overall SLD.real of layer N (material AND solvent)
+            slab[N, 2] - overall SLD.imag of layer N (material AND solvent)
+            slab[N, 3] - roughness between layer N and N-1
+            slab[N, 4] - volume fraction of solvent in layer N.
+                         (1 - solvent_volfrac = material_volfrac)
+
+    dA : float
+        Larger values coarsen the profile to a greater extent, and vice versa.
+
+    Returns
+    -------
+    contract_slab : array
+        Contracted slab representation.
+
+    Notes
+    -----
+    The reflectivity profiles from both contracted and un-contracted profiles
+    should be compared to check for accuracy.
+    """
+
+    # In refl1d the first slab is the substrate, the order is reversed here.
+    # In the following code the slabs are traversed from the backing towards
+    # the fronting.
+    newslabs = np.copy(slabs)[::-1]
+    d = newslabs[:, 0]
+    rho = newslabs[:, 1]
+    irho = newslabs[:, 2]
+    sigma = newslabs[:, 3]
+    vfsolv = newslabs[:, 4]
+
+    n = np.size(d, 0)
+    i = newi = 1  # Skip the substrate
+
+    while i < n:
+        # Get ready for the next layer
+        # Accumulation of the first row happens in the inner loop
+        dz = rhoarea = irhoarea = vfsolvarea = 0.
+        rholo = rhohi = rho[i]
+        irholo = irhohi = irho[i]
+
+        # Accumulate slices into layer
+        while True:
+            # Accumulate next slice
+            dz += d[i]
+            rhoarea += d[i] * rho[i]
+            irhoarea += d[i] * irho[i]
+            vfsolvarea += d[i] * vfsolv[i]
+
+            i += 1
+            # If no more slices or sigma != 0, break immediately
+            if i == n or sigma[i - 1] != 0.:
+                break
+
+            # If next slice won't fit, break
+            if rho[i] < rholo:
+                rholo = rho[i]
+            if rho[i] > rhohi:
+                rhohi = rho[i]
+            if (rhohi - rholo) * (dz + d[i]) > dA:
+                break
+
+            if irho[i] < irholo:
+                irholo = irho[i]
+            if irho[i] > irhohi:
+                irhohi = irho[i]
+            if (irhohi - irholo) * (dz + d[i]) > dA:
+                break
+
+        # Save the layer
+        d[newi] = dz
+        if i == n:
+            # printf("contract: adding final sld at %d\n",newi)
+            # Last layer uses surface values
+            rho[newi] = rho[n - 1]
+            irho[newi] = irho[n - 1]
+            vfsolv[newi] = vfsolv[n - 1]
+        else:
+            # Middle layers uses average values
+            rho[newi] = rhoarea / dz
+            irho[newi] = irhoarea / dz
+            sigma[newi] = sigma[i - 1]
+            vfsolv[newi] = vfsolvarea / dz
+        # First layer uses substrate values
+        newi += 1
+
+    return newslabs[:newi][::-1]
+
+
 """
 Polarised Neutron Reflectometry calculation
 """
 
 
 def _pmatrix(kn_u, kn_d, thickness):
     """
```

### Comparing `refnx-0.1.8/refnx/reflect/interface.py` & `refnx-0.1.9/refnx/reflect/interface.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/reflect_model.py` & `refnx-0.1.9/refnx/reflect/reflect_model.py`

 * *Files 2% similar despite different names*

```diff
@@ -26,29 +26,83 @@
 import abc
 import math
 import numbers
 import warnings
 
 import numpy as np
 import scipy
-from scipy.interpolate import InterpolatedUnivariateSpline
+from scipy.interpolate import splrep, splev
+
 
-try:
-    from refnx.reflect import _creflect as refcalc
-except ImportError:
-    print('WARNING, Using slow reflectivity calculation')
-    from refnx.reflect import _reflect as refcalc
 from refnx.analysis import (Parameters, Parameter, possibly_create_parameter)
 
 
 # some definitions for resolution smearing
 _FWHM = 2 * np.sqrt(2 * np.log(2.0))
 _INTLIMIT = 3.5
 
 
+"""
+Implementation notes
+--------------------
+1. For _smeared_abeles_fixed I investigated calculating a master curve,
+   adjacent data points have overlapping resolution kernels. So instead of
+   using e.g. an oversampling factor of 17, one could get away with using
+   a factor of 6. This is because the calculated points can be used to smear
+   more than one datapoint. One can't use Gaussian quadrature, Simpsons rule is
+   needed. Technically the approach works, but turns out to be no faster than
+   the Gaussian quadrature with the x17 oversampling (even if everything is
+   vectorised). There are a couple of reasons: a) calculating the Gaussian
+   weights has to be re-done for all the resolution smearing points for every
+   datapoint. For Gaussian quadrature that calculation only needs to be done
+   once, because the oversampling points are at constant locations around the
+   mean. b) in the implementation I tried the Simpsons rule had to integrate
+   e.g. 700 odd points instead of the fixed 17 for the Gaussin quadrature.
+"""
+
+
+def get_reflect_backend(backend='c'):
+    r"""
+
+    Parameters
+    ----------
+    backend: {'python', 'cython', 'c'}, str
+        The module that calculates the reflectivity. Speed should go in the
+        order cython > c > python. If a particular method is not available the
+        function falls back: cython --> c --> python.
+
+    Returns
+    -------
+    abeles: callable
+        The callable that calculates the reflectivity
+
+    """
+    if backend == 'cython':
+        try:
+            from refnx.reflect import _cyreflect as _cy
+            f = _cy.abeles
+        except ImportError:
+            return get_reflect_backend('c')
+    elif backend == 'c':
+        try:
+            from refnx.reflect import _creflect as _c
+            f = _c.abeles
+        except ImportError:
+            return get_reflect_backend('python')
+    elif backend == 'python':
+        warnings.warn("Using the SLOW reflectivity calculation.")
+        from refnx.reflect import _reflect as _py
+        f = _py.abeles
+
+    return f
+
+
+abeles = get_reflect_backend()
+
+
 class ReflectModel(object):
     r"""
     Parameters
     ----------
     structure : refnx.reflect.Structure
         The interfacial structure.
     scale : float or refnx.analysis.Parameter, optional
@@ -346,15 +400,15 @@
     ...                   [500, -0.5, 0.00001, 3],
     ...                   [0, 6.36, 0, 3]])
     >>> print(reflectivity(q, slabs))
 
     """
     # constant dq/q smearing
     if isinstance(dq, numbers.Real) and float(dq) == 0:
-        return refcalc.abeles(q, slabs, scale=scale, bkg=bkg, threads=threads)
+        return abeles(q, slabs, scale=scale, bkg=bkg, threads=threads)
     elif isinstance(dq, numbers.Real):
         dq = float(dq)
         return (scale *
                 _smeared_abeles_constant(q,
                                          slabs,
                                          dq,
                                          threads=threads)) + bkg
@@ -387,17 +441,17 @@
     # resolution kernel smearing
     elif (isinstance(dq, np.ndarray) and
           dq.ndim == q.ndim + 2 and
           dq.shape[0: q.ndim] == q.shape):
 
         qvals_for_res = dq[:, 0, :]
         # work out the reflectivity at the kernel evaluation points
-        smeared_rvals = refcalc.abeles(qvals_for_res,
-                                       slabs,
-                                       threads=threads)
+        smeared_rvals = abeles(qvals_for_res,
+                               slabs,
+                               threads=threads)
 
         # multiply by probability
         smeared_rvals *= dq[:, 1, :]
 
         # now do simpson integration
         rvals = scipy.integrate.simps(smeared_rvals, x=dq[:, 0, :])
 
@@ -459,15 +513,15 @@
     reflectivity : float
         Model reflectivity multiplied by the probability density function
         evaluated at a given distance, x, away from the mean Q value.
     """
     prefactor = 1 / np.sqrt(2 * np.pi)
     gauss = prefactor * np.exp(-0.5 * x * x)
     localq = q + x * dq / _FWHM
-    return refcalc.abeles(localq, w, threads=threads) * gauss
+    return abeles(localq, w, threads=threads) * gauss
 
 
 def _smeared_abeles_adaptive(qvals, w, dqvals, threads=-1):
     """
     Resolution smearing that uses adaptive Gaussian quadrature integration
     for the convolution.
 
@@ -559,17 +613,17 @@
     vb = qvals + _INTLIMIT * dqvals / _FWHM
 
     va = va[:, np.newaxis]
     vb = vb[:, np.newaxis]
 
     qvals_for_res = ((np.atleast_2d(abscissa) *
                      (vb - va) + vb + va) / 2.)
-    smeared_rvals = refcalc.abeles(qvals_for_res,
-                                   w,
-                                   threads=threads)
+    smeared_rvals = abeles(qvals_for_res,
+                           w,
+                           threads=threads)
 
     smeared_rvals = np.reshape(smeared_rvals,
                                (qvals.size, abscissa.size))
 
     smeared_rvals *= np.atleast_2d(gaussvals * weights)
     return np.sum(smeared_rvals, 1) * _INTLIMIT
 
@@ -594,15 +648,15 @@
     Returns
     -------
     reflectivity: np.ndarray
         The resolution smeared reflectivity
     """
 
     if resolution < 0.5:
-        return refcalc.abeles(q, w, threads=threads)
+        return abeles(q, w, threads=threads)
 
     resolution /= 100
     gaussnum = 51
     gaussgpoint = (gaussnum - 1) / 2
 
     def gauss(x, s):
         return 1. / s / np.sqrt(2 * np.pi) * np.exp(-0.5 * x**2 / s / s)
@@ -619,20 +673,25 @@
     xtemp = np.linspace(start, finish, int(interpnum))
     xlin = np.power(10., xtemp)
 
     # resolution smear over [-4 sigma, 4 sigma]
     gauss_x = np.linspace(-1.7 * resolution, 1.7 * resolution, gaussnum)
     gauss_y = gauss(gauss_x, resolution / _FWHM)
 
-    rvals = refcalc.abeles(xlin, w, threads=threads)
+    rvals = abeles(xlin, w, threads=threads)
     smeared_rvals = np.convolve(rvals, gauss_y, mode='same')
-    interpolator = InterpolatedUnivariateSpline(xlin, smeared_rvals)
+    smeared_rvals *= gauss_x[1] - gauss_x[0]
+
+    # interpolator = InterpolatedUnivariateSpline(xlin, smeared_rvals)
+    #
+    # smeared_output = interpolator(q)
+
+    tck = splrep(xlin, smeared_rvals)
+    smeared_output = splev(q, tck)
 
-    smeared_output = interpolator(q)
-    smeared_output *= gauss_x[1] - gauss_x[0]
     return smeared_output
 
 
 class MixedReflectModel(object):
     r"""
     Calculates an incoherent average of reflectivities from a sequence of
     structures. Such a situation may occur if a sample is not uniform over its
```

### Comparing `refnx-0.1.8/refnx/reflect/spline.py` & `refnx-0.1.9/refnx/reflect/spline.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/structure.py` & `refnx-0.1.9/refnx/reflect/structure.py`

 * *Files 3% similar despite different names*

```diff
@@ -28,19 +28,23 @@
 import numpy as np
 from scipy.stats import norm
 from scipy.interpolate import interp1d
 
 try:
     from refnx.reflect import _creflect as refcalc
 except ImportError:
-    print('WARNING, Using slow reflectivity calculation')
     from refnx.reflect import _reflect as refcalc
+
 from refnx._lib import flatten
 from refnx.analysis import Parameters, Parameter, possibly_create_parameter
 from refnx.reflect.interface import Interface, Erf, Step
+from refnx.reflect.reflect_model import get_reflect_backend
+
+# contracting the SLD profile can greatly speed a reflectivity calculation up.
+contract_by_area = refcalc._contract_by_area
 
 
 class Structure(UserList):
     """
     Represents the interfacial Structure of a reflectometry sample.
     Successive Components are added to the Structure to construct the
     interface.
@@ -296,15 +300,15 @@
             slabs[0, 3] = 0.
 
         if np.any(slabs[:, 4] > 0):
             # overall SLD is a weighted average of the vfs and slds
             slabs[1:-1] = self.overall_sld(slabs[1:-1], self.solvent)
 
         if self.contract > 0:
-            return _contract_by_area(slabs, self.contract)
+            return contract_by_area(slabs, self.contract)
         else:
             return slabs
 
     def _micro_slabs(self, slice_size=0.5):
         """
         Creates a microslab representation of the Structure.
 
@@ -447,15 +451,16 @@
         the overall reflectivity and SLD profile are calculated by
         micro-slicing. Micro-slicing involves calculating the specific SLD
         profile, dividing it up into small-slabs, and calculating the
         reflectivity from those. This normally takes much longer than the
         Nevot-Croce approximation. To speed the calculation up the
         `Structure.contract` property can be used.
         """
-        return refcalc.abeles(q, self.slabs()[..., :4], threads=threads)
+        abeles = get_reflect_backend()
+        return abeles(q, self.slabs()[..., :4], threads=threads)
 
     def sld_profile(self, z=None):
         """
         Calculates an SLD profile, as a function of distance through the
         interface.
 
         Parameters
@@ -942,19 +947,19 @@
         self._parameters.name = self.name
         return self._parameters
 
     def slabs(self, structure=None):
         """
         Slab representation of this component. See :class:`Component.slabs`
         """
-        return np.atleast_2d(np.array([self.thick.value,
-                                       self.sld.real.value,
-                                       self.sld.imag.value,
-                                       self.rough.value,
-                                       self.vfsolv.value]))
+        return np.array([[self.thick.value,
+                          self.sld.real.value,
+                          self.sld.imag.value,
+                          self.rough.value,
+                          self.vfsolv.value]])
 
 
 class Stack(Component, UserList):
     r"""
     A series of Components to be considered as one. When part of a Structure
     the Stack can represent a multilayer by setting the `repeats` attribute.
 
@@ -1249,108 +1254,7 @@
     for i in range(nlayers + 1):
         f = erf_f
         if sigma[i] == 0:
             f = step_f
         sld += delta_rho[i] * f(zed, scale=sigma[i], loc=dist[i])
 
     return zed, sld
-
-
-# The following slab contraction code was translated from C code in
-# the refl1d project.
-def _contract_by_area(slabs, dA=0.5):
-    """
-    Shrinks a slab representation to a reduced number of layers. This can
-    reduced calculation times.
-
-    Parameters
-    ----------
-    slabs : array
-        Has shape (N, 5).
-
-            slab[N, 0] - thickness of layer N
-            slab[N, 1] - overall SLD.real of layer N (material AND solvent)
-            slab[N, 2] - overall SLD.imag of layer N (material AND solvent)
-            slab[N, 3] - roughness between layer N and N-1
-            slab[N, 4] - volume fraction of solvent in layer N.
-                         (1 - solvent_volfrac = material_volfrac)
-
-    dA : float
-        Larger values coarsen the profile to a greater extent, and vice versa.
-
-    Returns
-    -------
-    contract_slab : array
-        Contracted slab representation.
-
-    Notes
-    -----
-    The reflectivity profiles from both contracted and un-contracted profiles
-    should be compared to check for accuracy.
-    """
-
-    # In refl1d the first slab is the substrate, the order is reversed here.
-    # In the following code the slabs are traversed from the backing towards
-    # the fronting.
-    newslabs = np.copy(slabs)[::-1]
-    d = newslabs[:, 0]
-    rho = newslabs[:, 1]
-    irho = newslabs[:, 2]
-    sigma = newslabs[:, 3]
-    vfsolv = newslabs[:, 4]
-
-    n = np.size(d, 0)
-    i = newi = 1  # Skip the substrate
-
-    while i < n:
-        # Get ready for the next layer
-        # Accumulation of the first row happens in the inner loop
-        dz = rhoarea = irhoarea = vfsolvarea = 0.
-        rholo = rhohi = rho[i]
-        irholo = irhohi = irho[i]
-
-        # Accumulate slices into layer
-        while True:
-            # Accumulate next slice
-            dz += d[i]
-            rhoarea += d[i] * rho[i]
-            irhoarea += d[i] * irho[i]
-            vfsolvarea += d[i] * vfsolv[i]
-
-            i += 1
-            # If no more slices or sigma != 0, break immediately
-            if i == n or sigma[i - 1] != 0.:
-                break
-
-            # If next slice won't fit, break
-            if rho[i] < rholo:
-                rholo = rho[i]
-            if rho[i] > rhohi:
-                rhohi = rho[i]
-            if (rhohi - rholo) * (dz + d[i]) > dA:
-                break
-
-            if irho[i] < irholo:
-                irholo = irho[i]
-            if irho[i] > irhohi:
-                irhohi = irho[i]
-            if (irhohi - irholo) * (dz + d[i]) > dA:
-                break
-
-        # Save the layer
-        d[newi] = dz
-        if i == n:
-            # printf("contract: adding final sld at %d\n",newi)
-            # Last layer uses surface values
-            rho[newi] = rho[n - 1]
-            irho[newi] = irho[n - 1]
-            vfsolv[newi] = vfsolv[n - 1]
-        else:
-            # Middle layers uses average values
-            rho[newi] = rhoarea / dz
-            irho[newi] = irhoarea / dz
-            sigma[newi] = sigma[i - 1]
-            vfsolv[newi] = vfsolvarea / dz
-        # First layer uses substrate values
-        newi += 1
-
-    return newslabs[:newi][::-1]
```

### Comparing `refnx-0.1.8/refnx/reflect/test/c_PLP0011859_q.txt` & `refnx-0.1.9/refnx/reflect/test/c_PLP0011859_q.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/e361r.txt` & `refnx-0.1.9/refnx/reflect/test/e361r.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/gsmear.py` & `refnx-0.1.9/refnx/reflect/test/gsmear.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/refl1d.npy` & `refnx-0.1.9/refnx/reflect/test/refl1d.npy`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/sld_theoretical_R.txt` & `refnx-0.1.9/refnx/reflect/test/sld_theoretical_R.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/smeared_theoretical.txt` & `refnx-0.1.9/refnx/reflect/test/smeared_theoretical.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/smearingprecision.py` & `refnx-0.1.9/refnx/reflect/test/smearingprecision.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/test__code_fragment.py` & `refnx-0.1.9/refnx/reflect/test/test__code_fragment.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/test__interactive_modeller.py` & `refnx-0.1.9/refnx/reflect/test/test__interactive_modeller.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/test__lipid.py` & `refnx-0.1.9/refnx/reflect/test/test__lipid.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/test_interface.py` & `refnx-0.1.9/refnx/reflect/test/test_interface.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/test_reflect.py` & `refnx-0.1.9/refnx/reflect/test/test_reflect.py`

 * *Files 10% similar despite different names*

```diff
@@ -9,14 +9,20 @@
 
 try:
     import refnx.reflect._creflect as _creflect
     HAVE_CREFLECT = True
 except ImportError:
     HAVE_CREFLECT = False
 
+try:
+    import refnx.reflect._cyreflect as _cyreflect
+    HAVE_CYREFLECT = True
+except ImportError:
+    HAVE_CYREFLECT = False
+
 # Before removing what appear to be unused imports think twice.
 # Some of the tests use eval, which requires the imports.
 import refnx.reflect._reflect as _reflect
 from refnx.analysis import (Transform, Objective,
                             CurveFitter, Parameter, Interval,
                             Parameters)
 from refnx.reflect import (SLD, ReflectModel, MixedReflectModel,
@@ -88,18 +94,39 @@
 
         # test for non-contiguous Q values
         tempq = self.qvals[0::5]
         assert_(tempq.flags['C_CONTIGUOUS'] is False)
         calc = _creflect.abeles(tempq, self.structure.slabs()[..., :4])
         assert_almost_equal(calc, self.rvals[0::5])
 
+    def test_cy_abeles(self):
+        if not HAVE_CYREFLECT:
+            return
+        # test reflectivity calculation with values generated from Motofit
+        calc = _cyreflect.abeles(self.qvals,
+                                 self.structure.slabs()[..., :4])
+        assert_almost_equal(calc, self.rvals)
+
+        # test for non-contiguous Q values
+        tempq = self.qvals[0::5]
+        assert_(tempq.flags['C_CONTIGUOUS'] is False)
+        calc = _cyreflect.abeles(tempq, self.structure.slabs()[..., :4])
+        assert_almost_equal(calc, self.rvals[0::5])
+
     def test_c_abeles_multithreaded(self):
         _creflect.abeles(self.qvals, self.structure.slabs()[..., :4],
                          threads=4)
 
+    def test_cy_abeles_multithreaded(self):
+        if not HAVE_CYREFLECT:
+            return
+
+        _cyreflect.abeles(self.qvals, self.structure.slabs()[..., :4],
+                          threads=4)
+
     def test_py_abeles(self):
         # test reflectivity calculation with values generated from Motofit
         calc = _reflect.abeles(self.qvals, self.structure.slabs()[..., :4])
         assert_almost_equal(calc, self.rvals)
 
     def test_first_principles(self):
         # Test a first principles reflectivity calculation, rather than
@@ -164,14 +191,44 @@
         # threads = 2 forces the calculation to go through multithreaded calcn,
         # even on single core processor
         calc3 = _creflect.abeles(self.qvals, s, scale=0.5,
                                  bkg=0.1, threads=2)
         assert_almost_equal(calc1, calc2)
         assert_almost_equal(calc1, calc3)
 
+    def test_compare_cy_py_abeles(self):
+        # test python and c/cy are equivalent
+        # but not the same file
+        s = self.structure.slabs()[..., :4]
+
+        if not HAVE_CYREFLECT:
+            return
+
+        # if not TEST_C_REFLECT:
+        #     return
+        assert_(_reflect.__file__ != _cyreflect.__file__)
+
+        calc1 = _reflect.abeles(self.qvals, s)
+        calc2 = _cyreflect.abeles(self.qvals, s)
+        assert_almost_equal(calc1, calc2)
+        calc1 = _reflect.abeles(self.qvals, s, scale=2.)
+        calc2 = _cyreflect.abeles(self.qvals, s, scale=2.)
+        assert_almost_equal(calc1, calc2)
+        calc1 = _reflect.abeles(self.qvals, s, scale=0.5,
+                                bkg=0.1)
+        # threads = 1 is a non-threaded implementation
+        calc2 = _cyreflect.abeles(self.qvals, s, scale=0.5,
+                                  bkg=0.1, threads=1)
+        # threads = 2 forces the calculation to go through multithreaded calcn,
+        # even on single core processor
+        calc3 = _cyreflect.abeles(self.qvals, s, scale=0.5,
+                                  bkg=0.1, threads=2)
+        assert_almost_equal(calc1, calc2)
+        assert_almost_equal(calc1, calc3)
+
     """
     @np.testing.decorators.knownfailure
     def test_cabeles_parallelised(self):
         # I suppose this could fail if someone doesn't have a multicore
         # computer
         if not TEST_C_REFLECT:
             return
@@ -204,39 +261,80 @@
         assert_almost_equal(calc1, calc2)
 
         # test a negative background
         calc1 = _reflect.abeles(self.qvals, layer0, scale=0.99, bkg=-5e-7)
         calc2 = _creflect.abeles(self.qvals, layer0, scale=0.99, bkg=-5e-7)
         assert_almost_equal(calc1, calc2)
 
+    def test_compare_cy_py_abeles0(self):
+        # test two layer system
+        if not HAVE_CYREFLECT:
+            return
+        layer0 = np.array([[0, 2.07, 0.01, 3],
+                           [0, 6.36, 0.1, 3]])
+        calc1 = _reflect.abeles(self.qvals, layer0, scale=0.99, bkg=1e-8)
+        calc2 = _cyreflect.abeles(self.qvals, layer0, scale=0.99, bkg=1e-8)
+        assert_almost_equal(calc1, calc2)
+
+        # test a negative background
+        calc1 = _reflect.abeles(self.qvals, layer0, scale=0.99, bkg=-5e-7)
+        calc2 = _cyreflect.abeles(self.qvals, layer0, scale=0.99, bkg=-5e-7)
+        assert_almost_equal(calc1, calc2)
+
     def test_compare_c_py_abeles2(self):
         # test two layer system
-        # if not TEST_C_REFLECT:
-        #     return
         layer2 = np.array([[0, 2.07, 0.01, 3],
                            [10, 3.47, 0.01, 3],
                            [100, 1.0, 0.01, 4],
                            [0, 6.36, 0.1, 3]])
         calc1 = _reflect.abeles(self.qvals, layer2, scale=0.99, bkg=1e-8)
         calc2 = _creflect.abeles(self.qvals, layer2, scale=0.99, bkg=1e-8)
         assert_almost_equal(calc1, calc2)
 
+    def test_compare_cy_py_abeles2(self):
+        # test two layer system
+        if not HAVE_CYREFLECT:
+            return
+        layer2 = np.array([[0, 2.07, 0.01, 3],
+                           [10, 3.47, 0.01, 3],
+                           [100, 1.0, 0.01, 4],
+                           [0, 6.36, 0.1, 3]])
+        calc1 = _reflect.abeles(self.qvals, layer2, scale=0.99, bkg=1e-8)
+        calc2 = _cyreflect.abeles(self.qvals, layer2, scale=0.99, bkg=1e-8)
+        assert_almost_equal(calc1, calc2)
+
     def test_c_py_abeles_absorption(self):
         # https://github.com/andyfaff/refl1d_analysis/tree/master/notebooks
         q = np.linspace(0.008, 0.05, 500)
         depth = [0, 850, 0]
         rho = [2.067, 4.3, 6.]
         irho_zero = [0., 0.1, 0.]
         refnx_sigma = [np.nan, 35, 5.]
 
         w_zero = np.c_[depth, rho, irho_zero, refnx_sigma]
         py_abeles = _reflect.abeles(q, w_zero)
         c_abeles = _creflect.abeles(q, w_zero)
         assert_almost_equal(py_abeles, c_abeles)
 
+    def test_cy_py_abeles_absorption(self):
+        # https://github.com/andyfaff/refl1d_analysis/tree/master/notebooks
+        if not HAVE_CYREFLECT:
+            return
+
+        q = np.linspace(0.008, 0.05, 500)
+        depth = [0, 850, 0]
+        rho = [2.067, 4.3, 6.]
+        irho_zero = [0., 0.1, 0.]
+        refnx_sigma = [np.nan, 35, 5.]
+
+        w_zero = np.c_[depth, rho, irho_zero, refnx_sigma]
+        py_abeles = _reflect.abeles(q, w_zero)
+        cy_abeles = _cyreflect.abeles(q, w_zero)
+        assert_almost_equal(py_abeles, cy_abeles)
+
     def test_compare_refl1d(self):
         # refl1d calculated with:
         # from refl1d import abeles
         # x = np.linspace(0.005, 0.5, 1001)
         # z = abeles.refl(x / 2,
         #                 [0, 100, 200, 0],
         #                 [2.07, 3.45, 5., 6.],
@@ -252,14 +350,18 @@
         calc1 = _reflect.abeles(x, layers)
         calc2 = _creflect.abeles(x, layers)
         refl1d = np.load(os.path.join(self.pth, 'refl1d.npy'))
 
         assert_almost_equal(calc1, refl1d)
         assert_almost_equal(calc2, refl1d)
 
+        if HAVE_CYREFLECT:
+            calc2 = _cyreflect.abeles(x, layers)
+            assert_almost_equal(calc2, refl1d)
+
     def test_reverse(self):
         # check that the structure reversal works.
         sio2 = SLD(3.47, name='SiO2')
         air = SLD(0, name='air')
         si = SLD(2.07, name='Si')
         structure = si | sio2(100, 3) | air(0, 2)
         structure.reverse_structure = True
@@ -343,44 +445,46 @@
         p0 = np.array([[0, 2.07, 0, 0],
                       [100, 3.47, 0, 3],
                       [500, -0.5, 1e-3, 3],
                       [0, 6.36, 0, 3]])
 
         wf = Wrapper_fn(_reflect.abeles, p0)
         y = map(wf, q)
-        with MapWrapper() as f:
+        with MapWrapper(2) as f:
             z = f(wf, q)
         assert_equal(z, np.array(list(y)))
 
         wf = Wrapper_fn(_creflect.abeles, p0)
         y = map(wf, q)
-        with MapWrapper() as f:
+        with MapWrapper(2) as f:
             z = f(wf, q)
         assert_equal(z, np.array(list(y)))
 
     def test_parallel_objective(self):
         # check that a parallel objective works without issue
         # (it could be possible that parallel evaluation fails at a higher
         #  level in e.g. emcee or in scipy.optimize.differential_evolution)
         model = self.model361
+        model.threads = 2
+
         objective = Objective(model,
                               (self.qvals361, self.rvals361, self.evals361),
                               transform=Transform('logY'))
         p0 = np.array(objective.varying_parameters())
         cov = objective.covar()
         walkers = np.random.multivariate_normal(np.atleast_1d(p0),
                                                 np.atleast_2d(cov),
                                                 size=(100))
         map_logl = np.array(list(map(objective.logl, walkers)))
         map_chi2 = np.array(list(map(objective.chisqr, walkers)))
 
         wf = Wrapper_fn(model.model, p0)
         map_mod = np.array(list(map(wf, walkers)))
 
-        with MapWrapper() as g:
+        with MapWrapper(2) as g:
             mapw_mod = g(wf, walkers)
             mapw_logl = g(objective.logl, walkers)
             mapw_chi2 = g(objective.chisqr, walkers)
         assert_equal(mapw_logl, map_logl)
         assert_equal(mapw_chi2, map_chi2)
         assert_equal(mapw_mod, map_mod)
 
@@ -564,23 +668,23 @@
 
         mixed_model = MixedReflectModel([structure1, structure2], [0.4, 0.6],
                                         bkg=0, dq=0)
 
         assert_equal(mixed_model.scales, np.array([0.4, 0.6]))
         assert_(mixed_model.dq.value == 0)
 
-        assert_equal(mixed_model_y, mixed_model(self.qvals))
+        assert_allclose(mixed_model_y, mixed_model(self.qvals), atol=1e-13)
 
         # test repr of MixedReflectModel
         q = repr(mixed_model)
         r = eval(q)
         assert_equal(r.scales, np.array([0.4, 0.6]))
         assert_(r.dq.value == 0)
 
-        assert_equal(mixed_model_y, r(self.qvals))
+        assert_allclose(mixed_model_y, r(self.qvals), atol=1e-13)
 
     def test_pnr(self):
         # test pnr calculation
         q = np.linspace(0.01, 0.3, 1001)
 
         # use for spin channel PNR calculation
         players = np.array([[0, 0, 0, 0, 0],
```

### Comparing `refnx-0.1.8/refnx/reflect/test/test_spline.py` & `refnx-0.1.9/refnx/reflect/test/test_spline.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/reflect/test/test_structure.py` & `refnx-0.1.9/refnx/reflect/test/test_structure.py`

 * *Files 4% similar despite different names*

```diff
@@ -260,14 +260,24 @@
         slice_structure = _profile_slicer(z, sld, slice_size=0.5)
         slice_structure.contract = 0.02
         slice_reflectivity = slice_structure.reflectivity(q)
         assert_allclose(slice_reflectivity,
                         reflectivity,
                         rtol=5e-3)
 
+        # test cythonized contract_by_area code
+        try:
+            from refnx.reflect._creflect import _contract_by_area as ca2
+            from refnx.reflect._reflect import _contract_by_area as ca
+
+            slabs = slice_structure.slabs()
+            assert_almost_equal(ca2(slabs, 2), ca(slabs, 2))
+        except ImportError:
+            pass
+
     def test_stack(self):
         stk = Stack()
         slabs = stk.slabs(None)
         assert(slabs is None)
 
         si = SLD(2.07)
         sio2 = SLD(3.47)
```

### Comparing `refnx-0.1.8/refnx/reflect/test/theoretical.txt` & `refnx-0.1.9/refnx/reflect/test/theoretical.txt`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/util/ErrorProp.py` & `refnx-0.1.9/refnx/util/ErrorProp.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/util/__init__.py` & `refnx-0.1.9/refnx/util/__init__.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/util/_resolution_kernel.py` & `refnx-0.1.9/refnx/util/_resolution_kernel.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/util/general.py` & `refnx-0.1.9/refnx/util/general.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/util/nsplice.py` & `refnx-0.1.9/refnx/util/nsplice.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/util/quickplot.py` & `refnx-0.1.9/refnx/util/quickplot.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/util/test/PLP0000708.dat` & `refnx-0.1.9/refnx/util/test/PLP0000708.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/util/test/PLP0000709.dat` & `refnx-0.1.9/refnx/util/test/PLP0000709.dat`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/util/test/test_ErrorProp.py` & `refnx-0.1.9/refnx/util/test/test_ErrorProp.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/util/test/test_general.py` & `refnx-0.1.9/refnx/util/test/test_general.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx/util/test/test_nsplice.py` & `refnx-0.1.9/refnx/util/test/test_nsplice.py`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/refnx.egg-info/PKG-INFO` & `refnx-0.1.9/refnx.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: refnx
-Version: 0.1.8
+Version: 0.1.9
 Summary: Neutron and X-ray Reflectometry Analysis
 Home-page: https://github.com/refnx/refnx
 Author: Andrew Nelson
 Author-email: andyfaff+refnx@gmail.com
 License: BSD
 Project-URL: Bug Tracker, https://github.com/refnx/refnx/issues
 Project-URL: Documentation, https://refnx.readthedocs.io/en/latest/
```

### Comparing `refnx-0.1.8/refnx.egg-info/SOURCES.txt` & `refnx-0.1.9/refnx.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -179,14 +179,16 @@
 refnx/reflect/_app/datastore.py
 refnx/reflect/_app/graphproperties.py
 refnx/reflect/_app/lipids.json
 refnx/reflect/_app/resources.qrc
 refnx/reflect/_app/resources_rc.py
 refnx/reflect/_app/treeview_gui_model.py
 refnx/reflect/_app/view.py
+refnx/reflect/_app/icons/18_1 Diether PC.png
+refnx/reflect/_app/icons/DOTAP.png
 refnx/reflect/_app/icons/Motofit.icns
 refnx/reflect/_app/icons/TMCL.png
 refnx/reflect/_app/icons/TOCL.png
 refnx/reflect/_app/icons/branch-closed.png
 refnx/reflect/_app/icons/branch-end.png
 refnx/reflect/_app/icons/branch-more.png
 refnx/reflect/_app/icons/branch-open.png
@@ -197,14 +199,15 @@
 refnx/reflect/_app/icons/d54-DMPC.png
 refnx/reflect/_app/icons/d54-DMPG.png
 refnx/reflect/_app/icons/d62-DPPC.png
 refnx/reflect/_app/icons/d9-POPC.png
 refnx/reflect/_app/icons/go.png
 refnx/reflect/_app/icons/h-DMPC.png
 refnx/reflect/_app/icons/h-DMPG.png
+refnx/reflect/_app/icons/h-DOPC.png
 refnx/reflect/_app/icons/h-DPPC.png
 refnx/reflect/_app/icons/h-POPC.png
 refnx/reflect/_app/icons/h-POPE.png
 refnx/reflect/_app/icons/h-POPG.png
 refnx/reflect/_app/icons/h-POPS.png
 refnx/reflect/_app/icons/minus.png
 refnx/reflect/_app/icons/plus.png
@@ -259,9 +262,10 @@
 refnx/util/test/test_ErrorProp.py
 refnx/util/test/test_general.py
 refnx/util/test/test_nsplice.py
 src/MyComplex.h
 src/_cevent.pyx
 src/_creflect.pyx
 src/_cutil.pyx
+src/_cyreflect.pyx
 src/refcalc.cpp
 src/refcalc.h
```

### Comparing `refnx-0.1.8/setup.py` & `refnx-0.1.9/setup.py`

 * *Files 15% similar despite different names*

```diff
@@ -2,42 +2,49 @@
 # System imports
 from setuptools import setup, Extension, find_packages
 from setuptools.command.test import test as TestCommand
 import os
 import subprocess
 import sys
 import warnings
+import _open_mp_helpers
 
 try:
     from Cython.Distutils import build_ext
 except ImportError:
     USE_CYTHON = False
     warnings.warn(
         "Cython was not found. Slow reflectivity calculations will be used.")
 else:
     USE_CYTHON = True
 
-packages = find_packages()
-try:
-    idx = packages.index('motofit')
-    if idx >= 0:
-        packages.pop(idx)
-except ValueError:
-    pass
+
+# do you want to parallelise things with openmp?
+HAS_OPENMP = _open_mp_helpers.check_openmp_support()
+
 
 # versioning
 MAJOR = 0
 MINOR = 1
-MICRO = 8
+MICRO = 9
 ISRELEASED = True
 VERSION = '%d.%d.%d' % (MAJOR, MINOR, MICRO)
 
 
 # are we on windows, darwin, etc?
 platform = sys.platform
+packages = find_packages()
+try:
+    idx = packages.index('motofit')
+    if idx >= 0:
+        packages.pop(idx)
+    if idx >= 0:
+        packages.pop(idx)
+except ValueError:
+    pass
 
 
 # Return the git revision as a string
 def git_version():
     def _minimal_ext_cmd(cmd):
         # construct minimal environment
         env = {}
@@ -143,15 +150,15 @@
         'Programming Language :: Python :: 3',
         'Topic :: Scientific/Engineering',
         'Topic :: Scientific/Engineering :: Chemistry',
         'Topic :: Scientific/Engineering :: Physics',
         ],
         'packages': packages,
         'include_package_data': True,
-        'setup_requires': ['numpy'],
+        'setup_requires': ['numpy', 'cython'],
         'python_requires': '>=3.5',
         'install_requires': ['numpy', 'scipy'],
         'extras_require': {'all': ['IPython', 'ipywidgets', 'traitlets',
                                    'matplotlib', 'xlrd', 'h5py', 'tqdm',
                                    'pymc3', 'theano', 'ptemcee', 'pandas',
                                    'pyparsing', 'periodictable', 'pyqt']},
         'tests_require': ['pytest', 'uncertainties'],
@@ -184,48 +191,91 @@
 
         if HAS_NUMPY:
             try:
                 numpy_include = np.get_include()
             except AttributeError:
                 numpy_include = np.get_numpy_include()
 
-            # creflect extension module
-            _creflect = Extension(
-                                  name='refnx.reflect._creflect',
-                                  sources=['src/_creflect.pyx',
-                                           'src/refcalc.cpp'],
-                                  include_dirs=[numpy_include],
-                                  language='c++',
-                                  extra_compile_args=[],
-                                  extra_link_args=['-lpthread']
-                                  # libraries=
-                                  # extra_compile_args = "...".split(),
-                                  )
-            ext_modules.append(_creflect)
-
             _cevent = Extension(
                                 name='refnx.reduce._cevent',
                                 sources=['src/_cevent.pyx'],
                                 include_dirs=[numpy_include],
                                 language='c++',
                                 # libraries=
                                 # extra_compile_args = "...".split(),
                                 )
             ext_modules.append(_cevent)
 
             _cutil = Extension(
                                name='refnx._lib._cutil',
                                sources=['src/_cutil.pyx'],
                                include_dirs=[numpy_include],
-                               language='c++',
+                               language='c',
                                # libraries=
                                # extra_compile_args = "...".split(),
                                )
             ext_modules.append(_cutil)
 
+            # creflect extension module
+            _creflect = Extension(
+                name='refnx.reflect._creflect',
+                sources=['src/_creflect.pyx',
+                         'src/refcalc.cpp'],
+                include_dirs=[numpy_include],
+                language='c++',
+                extra_compile_args=['-std=c++11'],
+            )
+            ext_modules.append(_creflect)
+
+            # if we have openmp use pure cython version
+            # openmp should be present on windows, linux
+            #
+            # However, it's not present in Apple Clang. Therefore one has to
+            # jump through hoops to enable it.
+            # It's probably easier to install OpenMP on macOS via homebrew.
+            # However, it's fairly simple to build the OpenMP library, and
+            # installing it into PREFIX=/usr/local
+            #
+            # https://gist.github.com/andyfaff/084005bee32aee83d6b59e843278ab3e
+            #
+            # Instructions for macOS:
+            #
+            # brew install libomp
+            # export CC=clang
+            # export CXX =clang++
+            # export CXXFLAGS="$CXXFLAGS -Xpreprocessor -fopenmp"
+            # export CFLAGS="$CFLAGS -I/usr/local/opt/libomp/include"
+            # export CXXFLAGS="$CXXFLAGS -I/usr/local/opt/libomp/include"
+            # export LDFLAGS="$LDFLAGS -L/usr/local/opt/libomp/lib -lomp"
+            # export DYLD_LIBRARY_PATH =/usr/local/opt/libomp/lib
+
+            if HAS_OPENMP:
+                from numpy.distutils.ccompiler import new_compiler
+                from distutils.sysconfig import customize_compiler
+
+                # cyreflect extension module
+                _cyreflect = Extension(
+                    name='refnx.reflect._cyreflect',
+                    sources=['src/_cyreflect.pyx'],
+                    include_dirs=[numpy_include],
+                    language='c++',
+                    extra_compile_args=[],
+                    extra_link_args=[]
+                    # libraries=
+                    # extra_compile_args = "...".split(),
+                )
+                ccompiler = new_compiler()
+                customize_compiler(ccompiler)
+
+                openmp_flags = _open_mp_helpers.get_openmp_flag(ccompiler)
+                _cyreflect.extra_compile_args += openmp_flags
+                _cyreflect.extra_link_args += openmp_flags
+
+                ext_modules.append(_cyreflect)
+
             # specify min deployment version for macOS
             if platform == 'darwin':
                 for mod in ext_modules:
                     mod.extra_compile_args.append('-mmacosx-version-min=10.9')
 
             info['cmdclass'].update({'build_ext': build_ext})
             info['ext_modules'] = ext_modules
```

### Comparing `refnx-0.1.8/src/MyComplex.h` & `refnx-0.1.9/src/MyComplex.h`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/src/_cevent.pyx` & `refnx-0.1.9/src/_cevent.pyx`

 * *Files identical despite different names*

### Comparing `refnx-0.1.8/src/_creflect.pyx` & `refnx-0.1.9/src/_creflect.pyx`

 * *Files 24% similar despite different names*

```diff
@@ -83,101 +83,79 @@
                   <double*>y.data, <const double*>xtemp.data, threads)
     else:
         reflect(4*nlayers + 8, <const double*>coefs.data, npoints,
                 <double*>y.data, <const double*>xtemp.data)
 
     return y
 
-"""
-cdef extern from "<complex.h>":
-    double complex sqrt(double complex)
-    double complex exp(double complex)
-    double complex conj(double complex)
-    double abs(double)
-
-
-import numpy as np
-cimport numpy as cnp
-cimport cython
-from cython.view cimport array as cvarray
-
-DTYPE = np.float64
-ctypedef cnp.float64_t DTYPE_t
-TINY = 1e-30
-
-@cython.boundscheck(False)
-@cython.cdivision(True)
-def reflect(double[:] x not None,
-            cnp.ndarray[cnp.float64_t, ndim=2] w,
-            double scale=1.0, double bkg=0.):
-    if w.shape[1] != 4 or w.shape[0] < 2:
-        raise ValueError("Parameters for reflection must have shape (>2, 4)")
-    cdef int nlayers = w.shape[0] - 2
-    cdef int npoints = x.shape[0]
-    cdef int layer
-    cdef int i
-    cdef int m
-    cdef double complex M_4PI = 4 * np.pi
-    cdef double complex I = 1j
-    cdef double complex rj, k, k_next, q2, rough, mi00, mi01, mi10, mi11, thick
-    cdef double complex mrtot00, mrtot01, mrtot10, mrtot11, p0, p1, beta, arg
-
-    cdef cnp.ndarray[cnp.complex128_t, ndim=1] y = np.zeros(npoints,
-                             np.complex128)
-    cdef cnp.ndarray[cnp.complex128_t, ndim=1] roughsqr = np.empty(nlayers + 1,
-                             np.complex128)
-
-    cdef cnp.ndarray[cnp.complex128_t, ndim=1] SLD = np.zeros(
-                            (w.shape[0]), np.complex128)
-
-    cdef double[:, :] wbuf = w
-    cdef double complex[:] SLDbuf = SLD
-    cdef double complex[:] roughbuf = roughsqr
-
-    for i in range(1, nlayers + 2):
-        SLDbuf[i] = M_4PI * (wbuf[i, 1] - wbuf[0, 1] +
-                             1j * (abs(wbuf[i, 2]) + TINY)) * 1.e-6
-        roughbuf[i - 1] = -2. * wbuf[i, 3] * wbuf[i, 3]
-
-    for i in range(npoints):
-        q2 = x[i] * x[i] / 4.
-        k = sqrt(q2)
-        for m in range(0, nlayers + 1):
-            k_next = sqrt(q2 - SLDbuf[m + 1])
-            rj = (k - k_next) / (k + k_next) * exp(k * k_next * roughbuf[m])
-
-            if not m:
-                # characteristic matrix for first interface
-                mrtot00 = 1.
-                mrtot01 = rj
-                mrtot11 = 1.
-                mrtot10 = rj
-            else:
-                # work out the beta for the layer
-                thick = wbuf[m, 0]
-                beta = exp(k * thick * I)
-                # this is the characteristic matrix of a layer
-                mi00 = beta
-                mi11 = 1. / beta
-                mi10 = rj * mi00
-                mi01 = rj * mi11
-
-                # matrix multiply
-                p0 = mrtot00 * mi00 + mrtot10 * mi01
-                p1 = mrtot00 * mi10 + mrtot10 * mi11
-                mrtot00 = p0
-                mrtot10 = p1
-
-                p0 = mrtot01 * mi00 + mrtot11 * mi01
-                p1 = mrtot01 * mi10 + mrtot11 * mi11
-
-                mrtot01 = p0
-                mrtot11 = p1
-
-            k = k_next
-
-        y[i] = (mrtot01 / mrtot00)
-        y[i] = y[i] * conj(y[i])
-        y[i] *= scale
-        y[i] += bkg
-    return y.real
-"""
+
+cpdef _contract_by_area(np.ndarray[np.float64_t, ndim=2] slabs, dA=0.5):
+    newslabs = np.copy(slabs)[::-1]
+
+    cdef double [:, :] newslabs_view = newslabs
+    cdef double [:] d = newslabs_view[:, 0]
+    cdef double [:] rho = newslabs_view[:, 1]
+    cdef double [:] irho = newslabs_view[:, 2]
+    cdef double [:] sigma = newslabs[:, 3]
+    cdef double [:] vfsolv = newslabs[:, 4]
+
+    cdef size_t n = np.size(d, 0)
+    cdef size_t i, newi
+    cdef double dz, rhoarea, irhoarea, vfsolvarea, rholo, rhohi, irholo, irhohi
+    cdef double da = float(dA)
+
+    i = 1
+    newi = 1 # skip the substrate
+
+    while i < n:
+        # Get ready for the next layer
+        # Accumulation of the first row happens in the inner loop
+        dz = rhoarea = irhoarea = vfsolvarea = 0.
+        rholo = rhohi = rho[i]
+        irholo = irhohi = irho[i]
+
+        # Accumulate slices into layer
+        while True:
+            # Accumulate next slice
+            dz += d[i]
+            rhoarea += d[i] * rho[i]
+            irhoarea += d[i] * irho[i]
+            vfsolvarea += d[i] * vfsolv[i]
+
+            i += 1
+            # If no more slices or sigma != 0, break immediately
+            if i == n or sigma[i - 1] != 0.:
+                break
+
+            # If next slice won't fit, break
+            if rho[i] < rholo:
+                rholo = rho[i]
+            if rho[i] > rhohi:
+                rhohi = rho[i]
+            if (rhohi - rholo) * (dz + d[i]) > da:
+                break
+
+            if irho[i] < irholo:
+                irholo = irho[i]
+            if irho[i] > irhohi:
+                irhohi = irho[i]
+            if (irhohi - irholo) * (dz + d[i]) > da:
+                break
+
+        # Save the layer
+        d[newi] = dz
+        if i == n:
+            # printf("contract: adding final sld at %d\n",newi)
+            # Last layer uses surface values
+            rho[newi] = rho[n - 1]
+            irho[newi] = irho[n - 1]
+            vfsolv[newi] = vfsolv[n - 1]
+        else:
+            # Middle layers uses average values
+            rho[newi] = rhoarea / dz
+            irho[newi] = irhoarea / dz
+            sigma[newi] = sigma[i - 1]
+            vfsolv[newi] = vfsolvarea / dz
+        # First layer uses substrate values
+        newi += 1
+
+    return newslabs[:newi][::-1]
```

### Comparing `refnx-0.1.8/src/_cutil.pyx` & `refnx-0.1.9/src/_cutil.pyx`

 * *Files 10% similar despite different names*

```diff
@@ -1,12 +1,9 @@
 # cython: language_level=3
 
-from __future__ import division, absolute_import
-import collections.abc
-
 
 def c_flatten(seq):
     """
     Flatten a nested sequence.
 
     Parameters
     ----------
@@ -15,18 +12,20 @@
 
     Returns
     -------
     el : generator
         yields flattened sequences from seq
     """
     for el in seq:
-        if (isinstance(el, collections.abc.Iterable) and
-                not isinstance(el, (str, bytes))):
+        try:
+            iter(el)
+            if isinstance(el, (str, bytes)):
+                raise TypeError
             yield from c_flatten(el)
-        else:
+        except TypeError:
             yield el
 
 
 def c_unique(seq, idfun=id):
     """
     List of unique values in sequence (by object id). Ordering is preserved
     Parameters
```

### Comparing `refnx-0.1.8/src/refcalc.h` & `refnx-0.1.9/src/refcalc.h`

 * *Files identical despite different names*

