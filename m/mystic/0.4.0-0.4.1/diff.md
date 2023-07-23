# Comparing `tmp/mystic-0.4.0.tar.gz` & `tmp/mystic-0.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mystic-0.4.0.tar", last modified: Mon Oct 24 03:07:41 2022, max compression
+gzip compressed data, was "mystic-0.4.1.tar", last modified: Sun Jul 23 18:23:29 2023, max compression
```

## Comparing `mystic-0.4.0.tar` & `mystic-0.4.1.tar`

### file list

```diff
@@ -1,407 +1,429 @@
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.426929 mystic-0.4.0/
--rw-r--r--   0 mmckerns   (501) staff       (20)      832 2022-05-16 23:11:32.000000 mystic-0.4.0/.codecov.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1289 2022-07-02 19:55:09.000000 mystic-0.4.0/.coveragerc
--rw-r--r--   0 mmckerns   (501) staff       (20)       32 2016-12-30 20:13:16.000000 mystic-0.4.0/.gitignore
--rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-05-16 23:11:32.000000 mystic-0.4.0/.readthedocs.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1897 2022-07-02 19:48:23.000000 mystic-0.4.0/.travis.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2022-01-01 16:48:27.000000 mystic-0.4.0/LICENSE
--rw-r--r--   0 mmckerns   (501) staff       (20)      362 2022-07-07 20:50:01.000000 mystic-0.4.0/MANIFEST.in
--rw-r--r--   0 mmckerns   (501) staff       (20)    14066 2022-10-24 03:07:41.427271 mystic-0.4.0/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)    13141 2022-10-24 03:04:38.000000 mystic-0.4.0/README.md
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.000603 mystic-0.4.0/docs/
--rw-r--r--   0 mmckerns   (501) staff       (20)      670 2022-05-16 23:11:32.000000 mystic-0.4.0/docs/Makefile
--rw-r--r--   0 mmckerns   (501) staff       (20)      430 2022-05-17 16:08:11.000000 mystic-0.4.0/docs/requirements.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.009604 mystic-0.4.0/docs/source/
--rw-r--r--   0 mmckerns   (501) staff       (20)      324 2021-06-15 21:25:26.000000 mystic-0.4.0/docs/source/cache.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)     8066 2022-07-07 20:50:27.000000 mystic-0.4.0/docs/source/conf.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      347 2017-08-23 20:56:51.000000 mystic-0.4.0/docs/source/index.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)     2153 2021-06-21 19:53:41.000000 mystic-0.4.0/docs/source/math.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)     1993 2017-08-11 19:10:02.000000 mystic-0.4.0/docs/source/models.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)     8679 2021-06-21 23:30:45.000000 mystic-0.4.0/docs/source/mystic.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)    70951 2017-08-11 19:10:02.000000 mystic-0.4.0/docs/source/mystic2.png
--rw-r--r--   0 mmckerns   (501) staff       (20)      853 2018-05-26 16:31:47.000000 mystic-0.4.0/docs/source/scripts.rst
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.147229 mystic-0.4.0/examples/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.149085 mystic-0.4.0/examples/DATA/
--rw-r--r--   0 mmckerns   (501) staff       (20)     1765 2015-09-18 17:11:54.000000 mystic-0.4.0/examples/DATA/g1.pts
--rw-r--r--   0 mmckerns   (501) staff       (20)     1765 2015-09-18 17:11:54.000000 mystic-0.4.0/examples/DATA/g2.pts
--rw-r--r--   0 mmckerns   (501) staff       (20)     4142 2017-06-12 06:20:44.000000 mystic-0.4.0/examples/NOTES
--rw-r--r--   0 mmckerns   (501) staff       (20)     2375 2016-11-08 22:43:09.000000 mystic-0.4.0/examples/README
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1892 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/TEST_ffitPP.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1458 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/TEST_ffitPP2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1483 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/TEST_ffitPP2_b.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3115 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/TEST_ffitPP_b.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3377 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/buckshot_example06.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1560 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/cg_rosenbrock.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1259 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/constraint1_example01.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1763 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/constraint2_example01.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1535 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/constraint3_example01.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      881 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example01.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1477 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example02.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1308 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example03.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1908 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example04.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1215 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example05.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2315 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example06.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2279 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example07.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3229 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example08.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3500 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example09.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3122 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example10.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     4414 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example11.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3239 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/example12.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2780 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/ezmap_desolve.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2794 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/ezmap_desolve_rosen.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1107 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/forward_model.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2018 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/gplot_test_ffit.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3239 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/lattice_example06.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1066 2022-06-30 23:53:24.000000 mystic-0.4.0/examples/metropolis.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1064 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/mpl_corana.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2777 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/mpmap_desolve.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2661 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/mpmap_desolve_rosen.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1315 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/raw_chebyshev8.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1229 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/raw_chebyshev8b.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      906 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/raw_rosen.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1855 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/restart_solver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8087 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/rosetta_mogi.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5395 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/rosetta_parabola.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3756 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_circle.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3075 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_circle_dual.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2111 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_corana.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1822 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_dejong3.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1863 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_dejong4.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1626 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_dejong5.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2913 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_ffit.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2372 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_ffit2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1618 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_ffitB.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1079 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_ffitC.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1184 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_ffitD.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2711 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_fosc3d.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2608 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_getCost.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1999 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_griewangk.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3536 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_lorentzian.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3351 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_lorentzian2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     5298 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_mogi.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2943 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_mogi2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1824 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_mogi3.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2432 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_mogi4.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      785 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_mogi_basin.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1557 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_peaks.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3716 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_rosenbrock.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2111 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_rosenbrock2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2227 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_rosenbrock3.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2290 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_rosenbrock3b.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      953 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_scem.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3274 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_svc1.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3955 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_svc2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2578 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_svr1.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2636 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_svr2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2694 2022-06-30 23:52:30.000000 mystic-0.4.0/examples/test_twistedgaussian.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1461 2022-06-30 23:55:07.000000 mystic-0.4.0/examples/test_twistedgaussian2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2403 2022-06-30 23:54:18.000000 mystic-0.4.0/examples/test_twistedgaussian3.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3082 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_wavy.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2284 2022-01-01 16:48:27.000000 mystic-0.4.0/examples/test_zimmermann.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.201810 mystic-0.4.0/examples2/
--rw-r--r--   0 mmckerns   (501) staff       (20)      697 2016-11-08 22:43:09.000000 mystic-0.4.0/examples2/README
--rw-r--r--   0 mmckerns   (501) staff       (20)     3361 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/beam.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1127 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/boolean.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1684 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/constrained_scipy.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4139 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/crypta.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4035 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/crypto.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1796 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/cvxlp.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1685 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/cvxqp.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1234 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/cvxqp_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      957 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/cvxqp_alt2.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1998 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/datafit.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2755 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/eq10.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3584 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/eq20.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1865 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g01.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2161 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g01_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1638 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g01_alt2.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2035 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g02.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1551 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g02_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1582 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g02_alt2.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2174 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g03.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1529 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g03_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2412 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g04.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1998 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g05.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2120 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g05_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1674 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g06.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1532 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g06_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2410 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g07.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2309 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g07_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1657 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g08.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1480 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g08_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1977 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g09.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1830 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g09_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1908 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g10.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1990 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g10_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1637 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g11.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1473 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g11_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2151 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g12.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2066 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/g13.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1769 2022-03-12 12:17:04.000000 mystic-0.4.0/examples2/g13_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3227 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/hotel_pricing.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6079 2022-01-01 16:51:02.000000 mystic-0.4.0/examples2/inequalities.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2827 2022-01-01 16:49:11.000000 mystic-0.4.0/examples2/inout_constrain.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2884 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/integer_inequalities.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1668 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/integer_programming.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1904 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/integer_programming_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3745 2022-03-11 16:10:05.000000 mystic-0.4.0/examples2/knapsack.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3058 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/least_square.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2447 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/lp.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1759 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/max_percentle.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1443 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/no_solution.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1305 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/no_solution2.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1421 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/no_solution3.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3517 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/olympic.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1792 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/optqp.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1281 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/optqp_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      996 2022-08-27 17:13:46.000000 mystic-0.4.0/examples2/or_constraint.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1413 2022-02-20 18:39:29.000000 mystic-0.4.0/examples2/output_constrain.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2498 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/polyfit.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1483 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/qp_inequality.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1878 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/root.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1370 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/slack_variable.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1766 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/slsqp.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1721 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/slsqp2.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1992 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/slsqp3.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1799 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/spring.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1823 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/spring_alt.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1880 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/vessel.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1764 2022-01-01 16:48:27.000000 mystic-0.4.0/examples2/vessel_alt.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.258628 mystic-0.4.0/examples3/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.261003 mystic-0.4.0/examples3/DATA/
--rw-r--r--   0 mmckerns   (501) staff       (20)     1765 2016-09-01 15:48:30.000000 mystic-0.4.0/examples3/DATA/g1.pts
--rw-r--r--   0 mmckerns   (501) staff       (20)     1765 2016-09-01 15:48:30.000000 mystic-0.4.0/examples3/DATA/g2.pts
--rw-r--r--   0 mmckerns   (501) staff       (20)     2722 2022-09-14 23:20:38.000000 mystic-0.4.0/examples3/README
--rw-r--r--   0 mmckerns   (501) staff       (20)     1011 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/collapse_bounds.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7807 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/collapse_measures.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2019 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/collapse_solver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1913 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/constrained_sklearn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    13628 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/dataset.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    16274 2022-04-22 00:05:34.000000 mystic-0.4.0/examples3/estimator.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1210 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/hyperopt_sklearn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10561 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/interpolator.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8359 2022-09-30 00:50:15.000000 mystic-0.4.0/examples3/misc.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    16067 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/ml.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1731 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/noisy.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    21791 2022-10-06 23:27:56.000000 mystic-0.4.0/examples3/ouq.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2077 2022-10-06 23:27:56.000000 mystic-0.4.0/examples3/ouq_.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    32226 2022-09-07 17:11:52.000000 mystic-0.4.0/examples3/ouq_models.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11653 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/plotter.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1216 2022-01-01 16:49:17.000000 mystic-0.4.0/examples3/sampler_pandas.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8997 2022-09-30 00:58:29.000000 mystic-0.4.0/examples3/spec3D.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8975 2022-09-30 00:50:42.000000 mystic-0.4.0/examples3/spec5D.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    13797 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/surface.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2244 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/surrogate.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1371 2022-09-05 21:10:29.000000 mystic-0.4.0/examples3/test_3D_ub_c0mean.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1883 2022-09-05 22:40:20.000000 mystic-0.4.0/examples3/test_3D_ub_mean.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1889 2022-09-05 22:40:51.000000 mystic-0.4.0/examples3/test_3D_ub_pof.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1733 2022-09-05 22:17:50.000000 mystic-0.4.0/examples3/test_5D_ub_c0mean.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2291 2022-09-05 22:41:13.000000 mystic-0.4.0/examples3/test_5D_ub_mean.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4195 2022-09-07 17:41:25.000000 mystic-0.4.0/examples3/test_error.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2405 2022-09-05 22:43:39.000000 mystic-0.4.0/examples3/test_expected.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4362 2022-09-05 23:00:39.000000 mystic-0.4.0/examples3/test_expected_error1.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5279 2022-09-05 23:01:07.000000 mystic-0.4.0/examples3/test_expected_error1GP.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4982 2022-09-05 23:01:21.000000 mystic-0.4.0/examples3/test_expected_error1ML.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4617 2022-09-05 23:01:29.000000 mystic-0.4.0/examples3/test_expected_error2.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2022-09-06 03:38:59.000000 mystic-0.4.0/examples3/test_expected_error2GP.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5237 2022-09-05 23:01:54.000000 mystic-0.4.0/examples3/test_expected_error2ML.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4180 2022-09-05 23:02:02.000000 mystic-0.4.0/examples3/test_expected_error3.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5317 2022-09-05 23:06:41.000000 mystic-0.4.0/examples3/test_glb_expected.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5297 2022-09-05 23:07:31.000000 mystic-0.4.0/examples3/test_gub_expected.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1247 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/test_improve_score.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5286 2022-09-05 23:07:56.000000 mystic-0.4.0/examples3/test_llb_expected.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5306 2022-09-05 23:08:05.000000 mystic-0.4.0/examples3/test_lub_expected.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5194 2022-09-05 23:09:03.000000 mystic-0.4.0/examples3/test_lub_expected0.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6359 2022-09-05 23:12:22.000000 mystic-0.4.0/examples3/test_lub_expected_error0.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6470 2022-09-05 23:12:29.000000 mystic-0.4.0/examples3/test_lub_expected_error1.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7880 2022-09-05 23:12:35.000000 mystic-0.4.0/examples3/test_lub_expected_error1GP.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7587 2022-09-05 23:12:42.000000 mystic-0.4.0/examples3/test_lub_expected_error1ML.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6731 2022-09-05 23:12:48.000000 mystic-0.4.0/examples3/test_lub_expected_error2a.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6764 2022-09-05 23:12:54.000000 mystic-0.4.0/examples3/test_lub_expected_error2b.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7680 2022-09-05 23:13:00.000000 mystic-0.4.0/examples3/test_lub_expected_error2bGP.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7383 2022-09-05 23:13:05.000000 mystic-0.4.0/examples3/test_lub_expected_error2bML.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6285 2022-09-05 23:11:04.000000 mystic-0.4.0/examples3/test_lub_expected_error3.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2730 2022-09-05 22:39:49.000000 mystic-0.4.0/examples3/test_pof.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7351 2022-06-29 22:41:57.000000 mystic-0.4.0/examples3/test_searcher.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7488 2022-06-29 22:42:19.000000 mystic-0.4.0/examples3/test_searcher2.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1241 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/test_sparsity.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6248 2022-06-29 22:42:30.000000 mystic-0.4.0/examples3/test_surface.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3545 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/test_svc1.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     4229 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/test_svc2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3095 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/test_svr1.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2989 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/test_svr2.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2659 2022-01-01 16:48:27.000000 mystic-0.4.0/examples3/toys.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.284149 mystic-0.4.0/examples4/
--rw-r--r--   0 mmckerns   (501) staff       (20)     6547 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/MM2_surrogate_diam_batchgrid.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5696 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/MM_surrogate_diam.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6538 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/MPI2_surrogate_diam_batchgrid.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5639 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/MPI_surrogate_diam.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7101 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/MPI_surrogate_diam_batchgrid.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6769 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/MPI_surrogate_diam_scatter.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7239 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/MSUB_surrogate_diam_batchgrid.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5697 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/PP_surrogate_diam.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6631 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/QSUB2_surrogate_diam_batchgrid.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7232 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/QSUB_surrogate_diam_batchgrid.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1518 2016-11-08 22:43:09.000000 mystic-0.4.0/examples4/README
--rw-r--r--   0 mmckerns   (501) staff       (20)     4775 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/TEST.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4786 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/TEST2.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5058 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/TEST3.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5058 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/TEST3b.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8316 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/TEST_surrogate_McD.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10016 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/TEST_surrogate_cut.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5524 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/TEST_surrogate_diam.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6688 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/TEST_surrogate_diam_batchgrid.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6416 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/TEST_surrogate_diam_scatter.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    13943 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/TEST_surrogate_samples.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11630 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/TEST_surrogate_smartcut.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1915 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/pool_helper.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2244 2022-01-01 16:48:27.000000 mystic-0.4.0/examples4/surrogate.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.292160 mystic-0.4.0/examples5/
--rw-r--r--   0 mmckerns   (501) staff       (20)      485 2016-11-08 22:43:09.000000 mystic-0.4.0/examples5/README
--rw-r--r--   0 mmckerns   (501) staff       (20)     9447 2022-01-01 16:48:27.000000 mystic-0.4.0/examples5/TEST4d_OUQ_surrogate_diam.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7143 2022-01-01 16:48:27.000000 mystic-0.4.0/examples5/TEST_OUQ_surrogate_diam.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2244 2022-03-15 00:40:29.000000 mystic-0.4.0/examples5/surrogate.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7586 2022-03-15 00:40:03.000000 mystic-0.4.0/examples5/test_3D_ub_c0mean.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7573 2022-03-15 00:40:03.000000 mystic-0.4.0/examples5/test_3D_ub_mean.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7590 2022-03-15 00:40:03.000000 mystic-0.4.0/examples5/test_3D_ub_pof.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8491 2022-03-15 00:40:03.000000 mystic-0.4.0/examples5/test_5D_ub_c0mean.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8476 2022-03-15 00:40:03.000000 mystic-0.4.0/examples5/test_5D_ub_mean.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2659 2022-03-15 00:42:04.000000 mystic-0.4.0/examples5/toys.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.344285 mystic-0.4.0/mystic/
--rw-r--r--   0 mmckerns   (501) staff       (20)    14800 2022-10-24 03:07:40.000000 mystic-0.4.0/mystic/__info__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2179 2022-07-07 20:57:00.000000 mystic-0.4.0/mystic/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      488 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1461 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/_counter.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3554 2022-06-30 18:57:19.000000 mystic-0.4.0/mystic/_genSow.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    67139 2022-06-30 22:18:43.000000 mystic-0.4.0/mystic/_scipy060optimize.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    10011 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/_scipyoptimize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1948 2022-07-01 00:23:10.000000 mystic-0.4.0/mystic/_signal.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    39951 2022-06-30 22:24:26.000000 mystic-0.4.0/mystic/_symbolic.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    31812 2022-06-30 22:51:22.000000 mystic-0.4.0/mystic/abstract_ensemble_solver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10143 2022-06-30 22:53:17.000000 mystic-0.4.0/mystic/abstract_launcher.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     8727 2022-09-05 18:38:06.000000 mystic-0.4.0/mystic/abstract_map_solver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    12675 2022-04-28 23:09:18.000000 mystic-0.4.0/mystic/abstract_sampler.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    49636 2022-10-11 00:02:14.000000 mystic-0.4.0/mystic/abstract_solver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8124 2022-09-29 16:55:00.000000 mystic-0.4.0/mystic/bounds.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.351071 mystic-0.4.0/mystic/cache/
--rw-r--r--   0 mmckerns   (501) staff       (20)     3863 2022-04-22 00:05:18.000000 mystic-0.4.0/mystic/cache/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8771 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/cache/archive.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2070 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/cache/function.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    19997 2022-06-30 22:35:57.000000 mystic-0.4.0/mystic/collapse.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    53592 2022-06-30 22:55:14.000000 mystic-0.4.0/mystic/constraints.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11013 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/coupler.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    39968 2022-09-05 18:34:58.000000 mystic-0.4.0/mystic/differential_evolution.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    23886 2022-09-05 18:40:30.000000 mystic-0.4.0/mystic/ensemble.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4590 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/filters.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    10678 2022-05-16 23:11:32.000000 mystic-0.4.0/mystic/forward_model.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1492 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/helputil.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1257 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/linesearch.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3744 2022-06-30 22:14:49.000000 mystic-0.4.0/mystic/mask.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.366948 mystic-0.4.0/mystic/math/
--rw-r--r--   0 mmckerns   (501) staff       (20)     3085 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/math/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9952 2022-06-30 22:50:30.000000 mystic-0.4.0/mystic/math/_rbf.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4487 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/math/approx.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2263 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/math/compressed.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    75604 2022-09-29 18:52:50.000000 mystic-0.4.0/mystic/math/discrete.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    24676 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/math/distance.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7357 2022-07-01 00:04:38.000000 mystic-0.4.0/mystic/math/grid.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5067 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/math/integrate.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    33963 2022-09-05 21:30:05.000000 mystic-0.4.0/mystic/math/interpolate.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    27109 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/math/legacydata.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    75552 2022-09-29 18:55:09.000000 mystic-0.4.0/mystic/math/measures.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1096 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/math/poly.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10440 2022-09-26 21:58:09.000000 mystic-0.4.0/mystic/math/samples.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9178 2022-07-01 00:17:54.000000 mystic-0.4.0/mystic/math/stats.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      838 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/metropolis.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.383459 mystic-0.4.0/mystic/models/
--rw-r--r--   0 mmckerns   (501) staff       (20)     3692 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      568 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1155 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/_model_helper.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6309 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/abstract_model.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3433 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/br8.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4652 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/circle.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9971 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/dejong.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4787 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/functions.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2773 2022-06-30 23:56:02.000000 mystic-0.4.0/mystic/models/lorentzian.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2601 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/mogi.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/nag.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    13418 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/pohlheim.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5785 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/poly.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2639 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/schittkowski.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7116 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/storn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1854 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/venkataraman.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3180 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/wavy.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3654 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/models/wolfram.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    24803 2022-10-06 18:09:03.000000 mystic-0.4.0/mystic/monitors.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9710 2022-07-01 00:31:01.000000 mystic-0.4.0/mystic/munge.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    19849 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/penalty.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4831 2022-06-30 17:41:48.000000 mystic-0.4.0/mystic/pools.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2744 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/python_map.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1673 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/samplers.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     8057 2022-07-01 00:19:02.000000 mystic-0.4.0/mystic/scemtools.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    40090 2022-10-11 00:08:33.000000 mystic-0.4.0/mystic/scipy_optimize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    56390 2022-09-15 15:32:22.000000 mystic-0.4.0/mystic/scripts.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    14940 2022-06-30 22:54:08.000000 mystic-0.4.0/mystic/search.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4308 2022-10-19 17:04:42.000000 mystic-0.4.0/mystic/solvers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11624 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/strategy.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    68667 2022-07-01 00:30:34.000000 mystic-0.4.0/mystic/support.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2357 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/svc.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     6264 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/svr.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    63431 2022-08-25 15:27:33.000000 mystic-0.4.0/mystic/symbolic.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    21996 2022-09-29 15:27:02.000000 mystic-0.4.0/mystic/termination.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.420449 mystic-0.4.0/mystic/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)      507 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      901 2022-07-09 11:12:59.000000 mystic-0.4.0/mystic/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)   526305 2016-08-17 19:08:51.000000 mystic-0.4.0/mystic/tests/_log.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3910 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/check_SOW.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3539 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_1d2d_expect.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3346 2022-01-01 16:49:28.000000 mystic-0.4.0/mystic/tests/test_boundsconstrained.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      786 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_cache.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    13707 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_collapse.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3320 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_collapsed.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4571 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_combined.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6684 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_compound_termination.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6289 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_constraints.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1215 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_converters.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4017 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_coupler.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10725 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_dirac_measure.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4745 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_expectation.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      905 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_impose.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7268 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_method_order.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1907 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_moments.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3517 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_normalize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3820 2022-09-02 20:13:19.000000 mystic-0.4.0/mystic/tests/test_samples.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4738 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_samplestats.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9873 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_solver_best_performance.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4878 2022-06-30 19:01:20.000000 mystic-0.4.0/mystic/tests/test_solver_compare.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4962 2022-04-24 18:35:57.000000 mystic-0.4.0/mystic/tests/test_solver_constraints.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11051 2022-06-30 20:23:20.000000 mystic-0.4.0/mystic/tests/test_solver_sanity.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5007 2022-06-29 18:19:48.000000 mystic-0.4.0/mystic/tests/test_solver_state.py
--rw-r--r--   0 mmckerns   (501) staff       (20)   140483 2022-06-30 20:22:53.000000 mystic-0.4.0/mystic/tests/test_solver_suite.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4644 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_symbolic.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1196 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_symbolic_abs.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6437 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_symbolic_basic.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5881 2022-06-30 19:00:42.000000 mystic-0.4.0/mystic/tests/test_symbolic_solve.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8540 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_termination.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1910 2022-01-01 16:48:27.000000 mystic-0.4.0/mystic/tests/test_vectorize.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    34175 2022-10-06 18:02:45.000000 mystic-0.4.0/mystic/tools.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.348716 mystic-0.4.0/mystic.egg-info/
--rw-r--r--   0 mmckerns   (501) staff       (20)    14066 2022-10-24 03:07:40.000000 mystic-0.4.0/mystic.egg-info/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     9839 2022-10-24 03:07:40.000000 mystic-0.4.0/mystic.egg-info/SOURCES.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-24 03:07:40.000000 mystic-0.4.0/mystic.egg-info/dependency_links.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-24 03:07:40.000000 mystic-0.4.0/mystic.egg-info/not-zip-safe
--rw-r--r--   0 mmckerns   (501) staff       (20)      152 2022-10-24 03:07:40.000000 mystic-0.4.0/mystic.egg-info/requires.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        7 2022-10-24 03:07:40.000000 mystic-0.4.0/mystic.egg-info/top_level.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)      308 2022-06-14 09:34:35.000000 mystic-0.4.0/pyproject.toml
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:07:41.426222 mystic-0.4.0/scripts/
--rw-r--r--   0 mmckerns   (501) staff       (20)      506 2022-01-01 16:48:27.000000 mystic-0.4.0/scripts/mystic_collapse_plotter
--rw-r--r--   0 mmckerns   (501) staff       (20)      488 2022-01-01 16:48:27.000000 mystic-0.4.0/scripts/mystic_log_reader
--rw-r--r--   0 mmckerns   (501) staff       (20)      568 2022-01-01 16:48:27.000000 mystic-0.4.0/scripts/mystic_model_plotter
--rw-r--r--   0 mmckerns   (501) staff       (20)      499 2022-01-01 16:48:27.000000 mystic-0.4.0/scripts/support_convergence
--rw-r--r--   0 mmckerns   (501) staff       (20)      493 2022-01-01 16:48:27.000000 mystic-0.4.0/scripts/support_hypercube
--rw-r--r--   0 mmckerns   (501) staff       (20)      520 2022-01-01 16:48:27.000000 mystic-0.4.0/scripts/support_hypercube_measures
--rw-r--r--   0 mmckerns   (501) staff       (20)      520 2022-01-01 16:48:27.000000 mystic-0.4.0/scripts/support_hypercube_scenario
--rw-r--r--   0 mmckerns   (501) staff       (20)       62 2022-10-24 03:07:41.428827 mystic-0.4.0/setup.cfg
--rw-r--r--   0 mmckerns   (501) staff       (20)     5530 2022-10-24 03:04:13.000000 mystic-0.4.0/setup.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      653 2022-07-09 11:12:45.000000 mystic-0.4.0/tox.ini
--rw-r--r--   0 mmckerns   (501) staff       (20)     2733 2022-10-24 03:06:26.000000 mystic-0.4.0/version.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.287034 mystic-0.4.1/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      832 2022-05-16 23:11:32.000000 mystic-0.4.1/.codecov.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1289 2022-07-02 19:55:09.000000 mystic-0.4.1/.coveragerc
+-rw-r--r--   0 mmckerns   (501) staff       (20)       32 2016-12-30 20:13:16.000000 mystic-0.4.1/.gitignore
+-rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-05-16 23:11:32.000000 mystic-0.4.1/.readthedocs.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2126 2023-07-07 03:33:05.000000 mystic-0.4.1/.travis.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2023-02-08 18:06:04.000000 mystic-0.4.1/LICENSE
+-rw-r--r--   0 mmckerns   (501) staff       (20)      362 2022-07-07 20:50:01.000000 mystic-0.4.1/MANIFEST.in
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15565 2023-07-23 18:23:29.287316 mystic-0.4.1/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)    14719 2023-07-23 18:19:14.000000 mystic-0.4.1/README.md
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:28.823980 mystic-0.4.1/docs/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      670 2022-05-16 23:11:32.000000 mystic-0.4.1/docs/Makefile
+-rw-r--r--   0 mmckerns   (501) staff       (20)      430 2023-07-22 01:41:08.000000 mystic-0.4.1/docs/requirements.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:28.836602 mystic-0.4.1/docs/source/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:28.809482 mystic-0.4.1/docs/source/_static/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:28.837597 mystic-0.4.1/docs/source/_static/css/
+-rw-r--r--   0 mmckerns   (501) staff       (20)       85 2023-03-15 11:54:23.000000 mystic-0.4.1/docs/source/_static/css/custom.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)      257 2023-03-14 01:01:16.000000 mystic-0.4.1/docs/source/cache.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8757 2023-07-05 04:50:08.000000 mystic-0.4.1/docs/source/conf.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      312 2023-07-05 01:19:40.000000 mystic-0.4.1/docs/source/index.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1509 2023-02-04 20:11:12.000000 mystic-0.4.1/docs/source/math.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1497 2023-02-04 20:13:19.000000 mystic-0.4.1/docs/source/models.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4018 2023-07-05 02:03:00.000000 mystic-0.4.1/docs/source/mystic.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)    70951 2017-08-11 19:10:02.000000 mystic-0.4.1/docs/source/mystic2.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1043 2023-02-04 20:19:09.000000 mystic-0.4.1/docs/source/scripts.rst
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:28.909482 mystic-0.4.1/examples/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:28.910670 mystic-0.4.1/examples/DATA/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1765 2015-09-18 17:11:54.000000 mystic-0.4.1/examples/DATA/g1.pts
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1765 2015-09-18 17:11:54.000000 mystic-0.4.1/examples/DATA/g2.pts
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4142 2017-06-12 06:20:44.000000 mystic-0.4.1/examples/NOTES
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2375 2016-11-08 22:43:09.000000 mystic-0.4.1/examples/README
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1892 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/TEST_ffitPP.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1458 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/TEST_ffitPP2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1483 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/TEST_ffitPP2_b.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3048 2023-01-17 22:11:00.000000 mystic-0.4.1/examples/TEST_ffitPP_b.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3377 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/buckshot_example06.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1560 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/cg_rosenbrock.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1259 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/constraint1_example01.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1763 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/constraint2_example01.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1535 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/constraint3_example01.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      881 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/example01.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1477 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/example02.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1308 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/example03.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1908 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/example04.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1215 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/example05.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2315 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/example06.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2279 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/example07.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3229 2023-02-16 00:16:23.000000 mystic-0.4.1/examples/example08.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3500 2023-02-16 00:16:30.000000 mystic-0.4.1/examples/example09.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3122 2023-02-16 00:16:35.000000 mystic-0.4.1/examples/example10.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     4414 2023-02-16 00:16:43.000000 mystic-0.4.1/examples/example11.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3239 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/example12.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2780 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/ezmap_desolve.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2794 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/ezmap_desolve_rosen.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1107 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/forward_model.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2018 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/gplot_test_ffit.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3239 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/lattice_example06.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1066 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/metropolis.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1064 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/mpl_corana.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2777 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/mpmap_desolve.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2661 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/mpmap_desolve_rosen.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1315 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/raw_chebyshev8.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1229 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/raw_chebyshev8b.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      906 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/raw_rosen.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1855 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/restart_solver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8087 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/rosetta_mogi.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5395 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/rosetta_parabola.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3756 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_circle.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3075 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_circle_dual.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2111 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_corana.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1822 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_dejong3.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1863 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_dejong4.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1626 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_dejong5.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2913 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_ffit.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2372 2023-02-16 00:24:03.000000 mystic-0.4.1/examples/test_ffit2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1618 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_ffitB.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1079 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_ffitC.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1184 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_ffitD.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2711 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_fosc3d.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2608 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_getCost.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1999 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_griewangk.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3536 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_lorentzian.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3351 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_lorentzian2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     5298 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_mogi.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2943 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_mogi2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1824 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_mogi3.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2432 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_mogi4.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      785 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_mogi_basin.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1557 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_peaks.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3716 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_rosenbrock.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2111 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_rosenbrock2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2227 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_rosenbrock3.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2290 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_rosenbrock3b.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      953 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_scem.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3274 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_svc1.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3955 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_svc2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2578 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_svr1.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2636 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_svr2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2694 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_twistedgaussian.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1461 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_twistedgaussian2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2403 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_twistedgaussian3.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3082 2023-01-01 14:50:24.000000 mystic-0.4.1/examples/test_wavy.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2284 2023-01-01 14:50:25.000000 mystic-0.4.1/examples/test_zimmermann.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.018398 mystic-0.4.1/examples2/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      697 2016-11-08 22:43:09.000000 mystic-0.4.1/examples2/README
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3361 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/beam.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1127 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/boolean.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1684 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/constrained_scipy.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4139 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/crypta.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4035 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/crypto.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1796 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/cvxlp.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1685 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/cvxqp.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1234 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/cvxqp_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      957 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/cvxqp_alt2.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1998 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/datafit.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2755 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/eq10.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3584 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/eq20.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1865 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g01.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2161 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g01_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1638 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g01_alt2.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2035 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g02.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1559 2023-07-04 04:38:38.000000 mystic-0.4.1/examples2/g02_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1582 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g02_alt2.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2174 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g03.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1529 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g03_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2412 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g04.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1998 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g05.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2120 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g05_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1674 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g06.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1532 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g06_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2410 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g07.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2309 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g07_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1657 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g08.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1480 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g08_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1977 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g09.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1830 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g09_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1908 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g10.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1990 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g10_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1637 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g11.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1473 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g11_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2151 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g12.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2066 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g13.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1769 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/g13_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3227 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/hotel_pricing.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6079 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/inequalities.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2827 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/inout_constrain.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2884 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/integer_inequalities.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1668 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/integer_programming.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1904 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/integer_programming_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3745 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/knapsack.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3058 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/least_square.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2447 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/lp.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1759 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/max_percentle.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1443 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/no_solution.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1305 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/no_solution2.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1421 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/no_solution3.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3517 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/olympic.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1792 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/optqp.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1281 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/optqp_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1001 2023-01-01 14:51:21.000000 mystic-0.4.1/examples2/or_constraint.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1418 2023-01-01 14:51:27.000000 mystic-0.4.1/examples2/output_constrain.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2498 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/polyfit.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1483 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/qp_inequality.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1878 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/root.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1370 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/slack_variable.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1766 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/slsqp.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1721 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/slsqp2.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1992 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/slsqp3.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1799 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/spring.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1823 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/spring_alt.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1880 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/vessel.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1764 2023-01-01 14:50:24.000000 mystic-0.4.1/examples2/vessel_alt.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.095867 mystic-0.4.1/examples3/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.102733 mystic-0.4.1/examples3/DATA/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1765 2016-09-01 15:48:30.000000 mystic-0.4.1/examples3/DATA/g1.pts
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1765 2016-09-01 15:48:30.000000 mystic-0.4.1/examples3/DATA/g2.pts
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3226 2022-12-22 04:39:25.000000 mystic-0.4.1/examples3/README
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1011 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/collapse_bounds.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7807 2023-02-16 02:13:31.000000 mystic-0.4.1/examples3/collapse_measures.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2019 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/collapse_solver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1913 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/constrained_sklearn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13603 2023-01-20 22:53:49.000000 mystic-0.4.1/examples3/dataset.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2879 2023-01-01 14:51:35.000000 mystic-0.4.1/examples3/emulators.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    16231 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/estimator.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1210 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/hyperopt_sklearn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10552 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/interpolator.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8431 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/misc.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9800 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/misc3.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9793 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/misc3b.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6351 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/misc4.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7055 2023-01-25 13:16:25.000000 mystic-0.4.1/examples3/misc6.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    16067 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/ml.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1731 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/noisy.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38150 2023-07-19 06:29:16.000000 mystic-0.4.1/examples3/ouq.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2077 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/ouq_.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    32226 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/ouq_models.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11653 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/plotter.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1216 2023-02-16 00:48:13.000000 mystic-0.4.1/examples3/sampler_pandas.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8997 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/spec3D.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8975 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/spec5D.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13797 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/surface.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2244 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/surrogate.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1371 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_3D_ub_c0mean.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1883 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_3D_ub_mean.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1889 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_3D_ub_pof.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1733 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_5D_ub_c0mean.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2291 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_5D_ub_mean.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3036 2023-01-01 14:53:44.000000 mystic-0.4.1/examples3/test_cache.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4195 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_error.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2560 2023-01-01 14:51:32.000000 mystic-0.4.1/examples3/test_expect.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2408 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_expected.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4362 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_expected_error1.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5279 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_expected_error1GP.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4982 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_expected_error1ML.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4617 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_expected_error2.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_expected_error2GP.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5237 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_expected_error2ML.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4180 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_expected_error3.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5317 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_glb_expected.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5297 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_gub_expected.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1247 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_improve_score.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5286 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_llb_expected.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5306 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_lub_expected.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5194 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_lub_expected0.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6359 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_lub_expected_error0.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6470 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_lub_expected_error1.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7880 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_lub_expected_error1GP.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7587 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_lub_expected_error1ML.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6731 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_lub_expected_error2a.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6764 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_lub_expected_error2b.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7680 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_lub_expected_error2bGP.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7383 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_lub_expected_error2bML.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6285 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_lub_expected_error3.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2730 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_pof.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7351 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_searcher.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7488 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_searcher2.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1241 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_sparsity.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6248 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_surface.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3545 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_svc1.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     4229 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_svc2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3095 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_svr1.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2989 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/test_svr2.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2659 2023-01-01 14:50:24.000000 mystic-0.4.1/examples3/toys.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5398 2023-01-01 14:53:56.000000 mystic-0.4.1/examples3/xrd_design3.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5400 2023-01-01 14:54:05.000000 mystic-0.4.1/examples3/xrd_design3b.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5285 2023-01-01 14:54:15.000000 mystic-0.4.1/examples3/xrd_design4.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5388 2023-01-01 14:54:29.000000 mystic-0.4.1/examples3/xrd_design6.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1886 2023-01-01 15:01:07.000000 mystic-0.4.1/examples3/xrd_opt3.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1885 2023-01-01 15:01:12.000000 mystic-0.4.1/examples3/xrd_opt4.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1889 2023-01-01 15:01:19.000000 mystic-0.4.1/examples3/xrd_opt6.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2444 2023-04-01 20:41:33.000000 mystic-0.4.1/examples3/xrd_optML3.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2446 2023-04-01 20:41:29.000000 mystic-0.4.1/examples3/xrd_optML4.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1735 2023-01-01 14:55:21.000000 mystic-0.4.1/examples3/xrd_plot_db.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      824 2023-01-01 14:55:36.000000 mystic-0.4.1/examples3/xrd_size_db.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.123736 mystic-0.4.1/examples4/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6547 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/MM2_surrogate_diam_batchgrid.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5696 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/MM_surrogate_diam.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6538 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/MPI2_surrogate_diam_batchgrid.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5639 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/MPI_surrogate_diam.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7101 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/MPI_surrogate_diam_batchgrid.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6769 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/MPI_surrogate_diam_scatter.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7239 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/MSUB_surrogate_diam_batchgrid.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5697 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/PP_surrogate_diam.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6631 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/QSUB2_surrogate_diam_batchgrid.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7232 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/QSUB_surrogate_diam_batchgrid.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1518 2016-11-08 22:43:09.000000 mystic-0.4.1/examples4/README
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4775 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/TEST.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4786 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/TEST2.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5058 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/TEST3.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5058 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/TEST3b.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8316 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/TEST_surrogate_McD.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10016 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/TEST_surrogate_cut.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5524 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/TEST_surrogate_diam.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6688 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/TEST_surrogate_diam_batchgrid.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6416 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/TEST_surrogate_diam_scatter.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13943 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/TEST_surrogate_samples.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11630 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/TEST_surrogate_smartcut.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1915 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/pool_helper.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2244 2023-01-01 14:50:24.000000 mystic-0.4.1/examples4/surrogate.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.132797 mystic-0.4.1/examples5/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      485 2016-11-08 22:43:09.000000 mystic-0.4.1/examples5/README
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9447 2023-01-01 14:50:24.000000 mystic-0.4.1/examples5/TEST4d_OUQ_surrogate_diam.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7143 2023-01-01 14:50:24.000000 mystic-0.4.1/examples5/TEST_OUQ_surrogate_diam.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2244 2023-01-01 14:50:24.000000 mystic-0.4.1/examples5/surrogate.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7586 2023-01-01 14:50:24.000000 mystic-0.4.1/examples5/test_3D_ub_c0mean.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7573 2023-01-01 14:50:24.000000 mystic-0.4.1/examples5/test_3D_ub_mean.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7590 2023-01-01 14:50:24.000000 mystic-0.4.1/examples5/test_3D_ub_pof.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8491 2023-01-01 14:50:24.000000 mystic-0.4.1/examples5/test_5D_ub_c0mean.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8476 2023-01-01 14:50:24.000000 mystic-0.4.1/examples5/test_5D_ub_mean.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2659 2023-01-01 14:50:24.000000 mystic-0.4.1/examples5/toys.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.177333 mystic-0.4.1/mystic/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    16243 2023-07-23 18:23:28.000000 mystic-0.4.1/mystic/__info__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2224 2023-02-06 03:52:01.000000 mystic-0.4.1/mystic/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      488 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1461 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/_counter.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3554 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/_genSow.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    67139 2023-02-16 00:29:11.000000 mystic-0.4.1/mystic/_scipy060optimize.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    10011 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/_scipyoptimize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1948 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/_signal.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    39883 2023-07-04 17:59:38.000000 mystic-0.4.1/mystic/_symbolic.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    34016 2023-03-19 12:33:06.000000 mystic-0.4.1/mystic/abstract_ensemble_solver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10658 2023-01-17 22:27:19.000000 mystic-0.4.1/mystic/abstract_launcher.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     4803 2023-01-17 22:11:07.000000 mystic-0.4.1/mystic/abstract_map_solver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13480 2023-07-22 01:38:36.000000 mystic-0.4.1/mystic/abstract_sampler.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    51337 2023-03-24 23:36:14.000000 mystic-0.4.1/mystic/abstract_solver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8598 2023-03-13 01:18:54.000000 mystic-0.4.1/mystic/bounds.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.190318 mystic-0.4.1/mystic/cache/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3863 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/cache/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8771 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/cache/archive.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2070 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/cache/function.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    19997 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/collapse.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    57435 2023-03-13 11:54:34.000000 mystic-0.4.1/mystic/constraints.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10992 2023-03-13 04:05:59.000000 mystic-0.4.1/mystic/coupler.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    40479 2023-03-18 20:41:55.000000 mystic-0.4.1/mystic/differential_evolution.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    23886 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/ensemble.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4680 2023-03-13 01:16:32.000000 mystic-0.4.1/mystic/filters.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    10678 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/forward_model.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1492 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/helputil.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1257 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/linesearch.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3744 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/mask.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.200765 mystic-0.4.1/mystic/math/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3085 2023-03-13 12:23:00.000000 mystic-0.4.1/mystic/math/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9952 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/math/_rbf.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4487 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/math/approx.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2263 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/math/compressed.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    75652 2023-07-04 04:36:42.000000 mystic-0.4.1/mystic/math/discrete.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24684 2023-07-04 04:37:13.000000 mystic-0.4.1/mystic/math/distance.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7365 2023-07-04 04:36:54.000000 mystic-0.4.1/mystic/math/grid.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5022 2023-01-17 21:38:40.000000 mystic-0.4.1/mystic/math/integrate.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38642 2023-03-12 13:35:19.000000 mystic-0.4.1/mystic/math/interpolate.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    27589 2023-03-18 19:24:39.000000 mystic-0.4.1/mystic/math/legacydata.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    75572 2023-07-04 04:36:10.000000 mystic-0.4.1/mystic/math/measures.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1477 2023-03-18 19:53:11.000000 mystic-0.4.1/mystic/math/poly.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10440 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/math/samples.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9178 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/math/stats.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      838 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/metropolis.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.220204 mystic-0.4.1/mystic/models/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3692 2023-03-04 20:57:50.000000 mystic-0.4.1/mystic/models/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      568 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/models/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1155 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/models/_model_helper.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6358 2023-03-04 20:59:49.000000 mystic-0.4.1/mystic/models/abstract_model.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3488 2023-03-04 21:01:42.000000 mystic-0.4.1/mystic/models/br8.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6284 2023-03-04 20:32:46.000000 mystic-0.4.1/mystic/models/circle.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10121 2023-03-04 21:11:57.000000 mystic-0.4.1/mystic/models/dejong.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4787 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/models/functions.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2842 2023-03-04 20:49:21.000000 mystic-0.4.1/mystic/models/lorentzian.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2629 2023-03-04 21:33:27.000000 mystic-0.4.1/mystic/models/mogi.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2226 2023-03-04 21:34:21.000000 mystic-0.4.1/mystic/models/nag.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13704 2023-03-04 21:38:35.000000 mystic-0.4.1/mystic/models/pohlheim.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6174 2023-03-04 21:45:41.000000 mystic-0.4.1/mystic/models/poly.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2673 2023-03-04 21:53:06.000000 mystic-0.4.1/mystic/models/schittkowski.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7213 2023-03-04 21:55:10.000000 mystic-0.4.1/mystic/models/storn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1886 2023-03-04 21:56:08.000000 mystic-0.4.1/mystic/models/venkataraman.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3228 2023-03-04 21:56:58.000000 mystic-0.4.1/mystic/models/wavy.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3711 2023-03-04 21:58:35.000000 mystic-0.4.1/mystic/models/wolfram.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24820 2023-03-17 01:31:20.000000 mystic-0.4.1/mystic/monitors.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    16773 2023-02-16 03:56:45.000000 mystic-0.4.1/mystic/munge.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    19849 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/penalty.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4855 2023-01-17 22:28:19.000000 mystic-0.4.1/mystic/pools.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2286 2023-01-17 22:17:53.000000 mystic-0.4.1/mystic/python_map.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1673 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/samplers.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     8057 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/scemtools.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    40593 2023-03-18 20:42:37.000000 mystic-0.4.1/mystic/scipy_optimize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    79651 2023-03-17 02:32:18.000000 mystic-0.4.1/mystic/scripts.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    14792 2023-03-13 11:58:09.000000 mystic-0.4.1/mystic/search.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4467 2023-03-18 20:11:20.000000 mystic-0.4.1/mystic/solvers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11624 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/strategy.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    69355 2023-07-04 04:37:42.000000 mystic-0.4.1/mystic/support.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2426 2023-03-06 00:56:04.000000 mystic-0.4.1/mystic/svc.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     6264 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/svr.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    63841 2023-07-04 18:01:17.000000 mystic-0.4.1/mystic/symbolic.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    22017 2023-03-13 04:13:02.000000 mystic-0.4.1/mystic/termination.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.280883 mystic-0.4.1/mystic/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      507 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      901 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)   526305 2016-08-17 19:08:51.000000 mystic-0.4.1/mystic/tests/_log.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3910 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/check_SOW.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3539 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_1d2d_expect.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3346 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_boundsconstrained.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      786 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_cache.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13707 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_collapse.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3320 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_collapsed.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4571 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_combined.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6684 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_compound_termination.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6289 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_constraints.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1215 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_converters.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4017 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_coupler.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10725 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_dirac_measure.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4780 2023-03-13 11:27:38.000000 mystic-0.4.1/mystic/tests/test_expectation.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      905 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_impose.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7268 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_method_order.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1907 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_moments.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3517 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_normalize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3825 2023-01-01 14:51:39.000000 mystic-0.4.1/mystic/tests/test_samples.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4738 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_samplestats.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9873 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_solver_best_performance.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4878 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_solver_compare.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4962 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_solver_constraints.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11051 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_solver_sanity.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5007 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_solver_state.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)   140483 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_solver_suite.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4644 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_symbolic.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1196 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_symbolic_abs.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6437 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_symbolic_basic.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5881 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_symbolic_solve.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8540 2023-01-01 14:50:24.000000 mystic-0.4.1/mystic/tests/test_termination.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1910 2023-07-04 04:00:57.000000 mystic-0.4.1/mystic/tests/test_vectorize.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    34325 2023-03-13 03:46:59.000000 mystic-0.4.1/mystic/tools.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.185110 mystic-0.4.1/mystic.egg-info/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15565 2023-07-23 18:23:28.000000 mystic-0.4.1/mystic.egg-info/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10317 2023-07-23 18:23:28.000000 mystic-0.4.1/mystic.egg-info/SOURCES.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-23 18:23:28.000000 mystic-0.4.1/mystic.egg-info/dependency_links.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-23 18:23:28.000000 mystic-0.4.1/mystic.egg-info/not-zip-safe
+-rw-r--r--   0 mmckerns   (501) staff       (20)      152 2023-07-23 18:23:28.000000 mystic-0.4.1/mystic.egg-info/requires.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        7 2023-07-23 18:23:28.000000 mystic-0.4.1/mystic.egg-info/top_level.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)      308 2023-02-12 21:49:37.000000 mystic-0.4.1/pyproject.toml
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 18:23:29.286617 mystic-0.4.1/scripts/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      506 2023-01-01 14:50:25.000000 mystic-0.4.1/scripts/mystic_collapse_plotter
+-rw-r--r--   0 mmckerns   (501) staff       (20)      497 2023-01-25 05:18:10.000000 mystic-0.4.1/scripts/mystic_log_converter
+-rw-r--r--   0 mmckerns   (501) staff       (20)      488 2023-01-25 05:18:17.000000 mystic-0.4.1/scripts/mystic_log_reader
+-rw-r--r--   0 mmckerns   (501) staff       (20)      568 2023-01-01 14:50:25.000000 mystic-0.4.1/scripts/mystic_model_plotter
+-rw-r--r--   0 mmckerns   (501) staff       (20)      499 2023-01-01 14:50:25.000000 mystic-0.4.1/scripts/support_convergence
+-rw-r--r--   0 mmckerns   (501) staff       (20)      493 2023-01-01 14:50:25.000000 mystic-0.4.1/scripts/support_hypercube
+-rw-r--r--   0 mmckerns   (501) staff       (20)      520 2023-01-01 14:50:25.000000 mystic-0.4.1/scripts/support_hypercube_measures
+-rw-r--r--   0 mmckerns   (501) staff       (20)      520 2023-01-01 14:50:25.000000 mystic-0.4.1/scripts/support_hypercube_scenario
+-rw-r--r--   0 mmckerns   (501) staff       (20)       62 2023-07-23 18:23:29.288222 mystic-0.4.1/setup.cfg
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5630 2023-07-23 18:19:22.000000 mystic-0.4.1/setup.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      798 2023-07-07 03:32:02.000000 mystic-0.4.1/tox.ini
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3171 2023-07-23 18:20:25.000000 mystic-0.4.1/version.py
```

### Comparing `mystic-0.4.0/.codecov.yml` & `mystic-0.4.1/.codecov.yml`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/.coveragerc` & `mystic-0.4.1/.coveragerc`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/.travis.yml` & `mystic-0.4.1/.travis.yml`

 * *Files 7% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-dist: focal
+dist: jammy
 language: python
 
 matrix:
     include:
         - python: '3.7'
           env:
 
@@ -14,28 +14,40 @@
             - COVERAGE="true"
             - MATPLOTLIB="true"
             - SYMPY="true"
             - SCIPY="true"
 
         - python: '3.10'
           env:
+
+        - python: '3.11'
+          env:
             - CYTHON="true" # numpy source build
 
-        - python: '3.11-dev'
+        - python: '3.12-dev'
           env:
             - CYTHON="true" # numpy source build
             - DILL="master"
             - KLEPTO="master"
 
-        - python: 'pypy3.7-7.3.5' # most recent
-          dist: bionic
+        - python: 'pypy3.7-7.3.9'
+          env:
+
+        - python: 'pypy3.8-7.3.9' # at 7.3.11
+          env:
+
+        - python: 'pypy3.9-7.3.9' # at 7.3.12
+          env:
+
+        - python: 'pypy3.10-7.3.12'
           env:
 
     allow_failures:
-        - python: '3.11-dev'
+        - python: '3.12-dev'
+        - python: 'pypy3.10-7.3.12' # CI missing
     fast_finish: true
 
 cache:
     pip: true
 
 before_install:
     - set -e  # fail on any error
```

### Comparing `mystic-0.4.0/LICENSE` & `mystic-0.4.1/LICENSE`

 * *Files 5% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 Copyright (c) 2004-2016 California Institute of Technology.
-Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
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

### Comparing `mystic-0.4.0/PKG-INFO` & `mystic-0.4.1/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: mystic
-Version: 0.4.0
-Summary: highly-constrained non-convex optimization and uncertainty quantification
+Version: 0.4.1
+Summary: constrained nonlinear optimization for scientific machine learning, UQ, and AI
 Home-page: https://github.com/uqfoundation/mystic
 Download-URL: https://pypi.org/project/mystic/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
 License: BSD-3-Clause
@@ -20,27 +20,28 @@
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Software Development
 Requires-Python: >=3.7
 Provides-Extra: math
 Provides-Extra: parallel
 Provides-Extra: plotting
 License-File: LICENSE
 
----------------------------------------------------------------------------------
-mystic: highly-constrained non-convex optimization and uncertainty quantification
----------------------------------------------------------------------------------
+--------------------------------------------------------------------------------------
+mystic: constrained nonlinear optimization for scientific machine learning, UQ, and AI
+--------------------------------------------------------------------------------------
 
 About Mystic
 ============
 
 The ``mystic`` framework provides a collection of optimization algorithms
 and tools that allows the user to more robustly (and easily) solve hard
 optimization problems. All optimization algorithms included in ``mystic``
@@ -59,23 +60,40 @@
 be easily swapped without the user having to write any new code. ``mystic``
 solvers all conform to a solver API, thus also have common method calls
 to configure and launch an optimization job. For more details, see
 ``mystic.abstract_solver``. The API also makes it easy to bind a favorite
 3rd party solver into the ``mystic`` framework.
 
 Optimization algorithms in ``mystic`` can accept parameter constraints,
-either in the form of penaties (which "penalize" regions of solution
-space that violate the constraints), or as constraints (which "constrain" 
-the solver to only search in regions of solution space where the
-constraints are respected), or both. ``mystic`` provides a large 
-selection of constraints, including probabistic and dimensionally
+as "soft constraints" (i.e. ``penalties``, which "penalize" regions of
+solution space that violate the constraints), or as "hard constraints"
+(i.e. ``constraints``, which constrain the solver to only search in regions
+of space where the constraints are respected), or both. ``mystic`` provides
+a large selection of constraints, including probabistic and dimensionally
 reducing constraints. By providing a robust interface designed to
 enable the user to easily configure and control solvers, ``mystic``
 greatly reduces the barrier to solving hard optimization problems.
 
+Sampling, interpolation, and statistics in ``mystic`` are all designed
+to seamlessly couple with constrained optimization to facilitate
+scientific machine learning, uncertainty quantification, adaptive
+sampling, nonlinear interpolation, and artificial intelligence.
+``mystic`` can convert systems of equalities and inequalities to
+hard or soft constraints using methods in ``mystic.symbolic``.
+With ``mystic.constraints.vectorize``, constraints can be converted
+to kernel transforms for use in machine learning. Similarly, ``mystic``
+provides tools for accurately producing emulators on an irregular grid
+using ``mystic.math.interpolate``, which includes methods for solving
+for gradients and Hessians. ``mystic.samplers`` use optimizers to
+drive adaptive sampling toward the first and second order critical points
+of the response surface, yielding highly-informative training data sets
+and ensuring emulator accuracy. ``mystic.math.discrete`` defines
+constrained discrete probability measures, which can be used in
+constrained statistical optimization and learning.
+
 ``mystic`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/mystic/issues, with a legacy list maintained at https://uqfoundation.github.io/project/mystic/query.
 
 
 Major Features
 ==============
 
@@ -120,15 +138,15 @@
 Installation
 ============
 
 ``mystic`` can be installed with ``pip``::
 
     $ pip install mystic
 
-To include optional scientific python support, with ``scipy``, install::
+To include optional scientific Python support, with ``scipy``, install::
 
     $ pip install mystic[math]
 
 To include optional plotting support with ``matplotlib``, install::
 
     $ pip install mystic[plotting]
 
@@ -144,91 +162,90 @@
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
     - ``cython``, **>=0.29.30**
     - ``numpy``, **>=1.0**
     - ``sympy``, **>=0.6.7**
     - ``mpmath``, **>=0.19**
-    - ``dill``, **>=0.3.6**
-    - ``klepto``, **>=0.2.3**
+    - ``dill``, **>=0.3.7**
+    - ``klepto``, **>=0.2.4**
 
 Optional requirements:
 
     - ``matplotlib``, **>=0.91**
     - ``scipy``, **>=0.6.0**
-    - ``pathos``, **>=0.3.0**
-    - ``pyina``, **>=0.2.6**
+    - ``pathos``, **>=0.3.1**
+    - ``pyina``, **>=0.2.8**
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://mystic.rtfd.io. Also see ``mystic.tests`` for a set of scripts that
 demonstrate several of the many features of the ``mystic`` framework.
 You can run the test suite with ``python -m mystic.tests``. There are
 several plotting scripts that are installed with ``mystic``, primary of which
 are ``mystic_log_reader`` (also available with ``python -m mystic``) and the
 ``mystic_model_plotter`` (also available with ``python -m mystic.models``).
 There are several other plotting scripts that come with ``mystic``, and they
-are detailed elsewhere in the documentation.  See ``mystic.examples`` for
-examples that demonstrate the basic use cases for configuration and launching
-of optimization jobs using one of the sample models provided in
-``mystic.models``. Many of the included examples are standard optimization
-test problems. The use of constraints and penalties are detailed in
-``mystic.examples2``, while more advanced features leveraging ensemble solvers
-and dimensional collapse are found in ``mystic.examples3``. The scripts in
-``mystic.examples4`` demonstrate leveraging ``pathos`` for parallel computing,
-as well as demonstrate some auto-partitioning schemes. ``mystic`` has the
-ability to work in product measure space, and the scripts in
-``mystic.examples5`` show to work with product measures.  The source code is
-generally well documented, so further questions may be resolved by inspecting
-the code itself.  Please feel free to submit a ticket on github, or ask a
-question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``mystic`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+are detailed elsewhere in the documentation.  See https://github.com/uqfoundation/mystic/tree/master/examples for examples that demonstrate the basic use
+cases for configuration and launching of optimization jobs using one of the
+sample models provided in ``mystic.models``. Many of the included examples
+are standard optimization test problems. The use of constraints and penalties
+are detailed in https://github.com/uqfoundation/mystic/tree/master/examples2 while more advanced features leveraging ensemble solvers, machine learning,
+uncertainty quantification, and dimensional collapse are found in https://github.com/uqfoundation/mystic/tree/master/examples3. The scripts in https://github.com/uqfoundation/mystic/tree/master/examples4 demonstrate leveraging ``pathos``
+for parallel computing, as well as demonstrate some auto-partitioning schemes.
+``mystic`` has the ability to work in product measure space, and the scripts in
+https://github.com/uqfoundation/mystic/tree/master/examples5 show how to work
+with product measures at a low level. The source code is generally well
+documented, so further questions may be resolved by inspecting the code itself.
+Please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``mystic`` in your work, please send an email (to **mmckerns at uqfoundation
+dot org**).
 
 Instructions on building a new model are in ``mystic.models.abstract_model``.
 ``mystic`` provides base classes for two types of models:
 
     - ``AbstractFunction``   [evaluates ``f(x)`` for given evaluation points ``x``]
     - ``AbstractModel``      [generates ``f(x,p)`` for given coefficients ``p``]
 
 ``mystic`` also provides some convienence functions to help you build a
 model instance and a cost function instance on-the-fly. For more
 information, see ``mystic.forward_model``.  It is, however, not necessary
 to use base classes or the model builder in building your own model or
-cost function, as any standard python function can be used as long as it
+cost function, as any standard Python function can be used as long as it
 meets the basic ``AbstractFunction`` interface of ``cost = f(x)``.
 
 All ``mystic`` solvers are highly configurable, and provide a robust set of
 methods to help customize the solver for your particular optimization
 problem. For each solver, a minimal (``scipy.optimize``) interface is also
 provided for users who prefer to configure and launch their solvers as a
 single function call. For more information, see ``mystic.abstract_solver``
 for the solver API, and each of the individual solvers for their minimal
 functional interface.
 
 ``mystic`` enables solvers to use parallel computing whenever the user provides
-a replacement for the (serial) python ``map`` function.  ``mystic`` includes a
+a replacement for the (serial) Python ``map`` function.  ``mystic`` includes a
 sample ``map`` in ``mystic.python_map`` that mirrors the behavior of the
-built-in python ``map``, and a ``pool`` in ``mystic.pools`` that provides ``map``
+built-in Python ``map``, and a ``pool`` in ``mystic.pools`` that provides ``map``
 functions using the ``pathos`` (i.e. ``multiprocessing``) interface. ``mystic``
 solvers are designed to utilize distributed and parallel tools provided by
 the ``pathos`` package. For more information, see ``mystic.abstract_map_solver``,
 ``mystic.abstract_ensemble_solver``, and the ``pathos`` documentation at
 http://pathos.rtfd.io.
 
 Important classes and functions are found here:
 
     - ``mystic.solvers``                  [solver optimization algorithms]
     - ``mystic.termination``              [solver termination conditions]
     - ``mystic.strategy``                 [solver population mutation strategies]
     - ``mystic.monitors``                 [optimization monitors]
-    - ``mystic.symbolic``                 [symbolic math in constaints]
+    - ``mystic.symbolic``                 [symbolic math in constraints]
     - ``mystic.constraints``              [constraints functions]
     - ``mystic.penalty``                  [penalty functions]
     - ``mystic.collapse``                 [checks for dimensional collapse]
     - ``mystic.coupler``                  [decorators for function coupling]
     - ``mystic.pools``                    [parallel worker pool interface]
     - ``mystic.munge``                    [file readers and writers]
     - ``mystic.scripts``                  [model and convergence plotting]
@@ -264,14 +281,15 @@
     - ``mystic.models.abstract_model``    [the model API definition]
 
 ``mystic`` also provides several convience scripts that are used to visualize
 models, convergence, and support on the hypercube. These scripts are installed
 to a directory on the user's ``$PATH``, and thus can be run from anywhere:
 
     - ``mystic_log_reader``               [parameter and cost convergence]
+    - ``mystic_log_converter``            [logfile format converter]
     - ``mystic_collapse_plotter``         [convergence and dimensional collapse]
     - ``mystic_model_plotter``            [model surfaces and solver trajectory]
     - ``support_convergence``             [convergence plots for measures]
     - ``support_hypercube``               [parameter support on the hypercube]
     - ``support_hypercube_measures``      [measure support on the hypercube]
     - ``support_hypercube_scenario``      [scenario support on the hypercube]
```

### Comparing `mystic-0.4.0/README.md` & `mystic-0.4.1/README.md`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 mystic
 ======
-highly-constrained non-convex optimization and uncertainty quantification
+constrained nonlinear optimization for scientific machine learning, UQ, and AI
 
 About Mystic
 ------------
 The ``mystic`` framework provides a collection of optimization algorithms
 and tools that allows the user to more robustly (and easily) solve hard
 optimization problems. All optimization algorithms included in ``mystic``
 provide workflow at the fitting layer, not just access to the algorithms
@@ -22,23 +22,40 @@
 be easily swapped without the user having to write any new code. ``mystic``
 solvers all conform to a solver API, thus also have common method calls
 to configure and launch an optimization job. For more details, see
 ``mystic.abstract_solver``. The API also makes it easy to bind a favorite
 3rd party solver into the ``mystic`` framework.
 
 Optimization algorithms in ``mystic`` can accept parameter constraints,
-either in the form of penaties (which "penalize" regions of solution
-space that violate the constraints), or as constraints (which "constrain" 
-the solver to only search in regions of solution space where the
-constraints are respected), or both. ``mystic`` provides a large 
-selection of constraints, including probabistic and dimensionally
+as "soft constraints" (i.e. ``penalties``, which "penalize" regions of
+solution space that violate the constraints), or as "hard constraints"
+(i.e. ``constraints``, which constrain the solver to only search in regions
+of space where the constraints are respected), or both. ``mystic`` provides
+a large selection of constraints, including probabistic and dimensionally
 reducing constraints. By providing a robust interface designed to
 enable the user to easily configure and control solvers, ``mystic``
 greatly reduces the barrier to solving hard optimization problems.
 
+Sampling, interpolation, and statistics in ``mystic`` are all designed
+to seamlessly couple with constrained optimization to facilitate
+scientific machine learning, uncertainty quantification, adaptive
+sampling, nonlinear interpolation, and artificial intelligence.
+``mystic`` can convert systems of equalities and inequalities to
+hard or soft constraints using methods in ``mystic.symbolic``.
+With ``mystic.constraints.vectorize``, constraints can be converted
+to kernel transforms for use in machine learning. Similarly, ``mystic``
+provides tools for accurately producing emulators on an irregular grid
+using ``mystic.math.interpolate``, which includes methods for solving
+for gradients and Hessians. ``mystic.samplers`` use optimizers to
+drive adaptive sampling toward the first and second order critical points
+of the response surface, yielding highly-informative training data sets
+and ensuring emulator accuracy. ``mystic.math.discrete`` defines
+constrained discrete probability measures, which can be used in
+constrained statistical optimization and learning.
+
 ``mystic`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/mystic/issues, with a legacy list maintained at https://uqfoundation.github.io/project/mystic/query.
 
 
 Major Features
 --------------
 ``mystic`` provides a stock set of configurable, controllable solvers with:
@@ -57,14 +74,15 @@
 * easily generate a model (several standard test models are included)
 * configure and auto-generate a cost function from a model
 * configure an ensemble of solvers to perform a specific task
 
 
 Current Release
 [![Downloads](https://static.pepy.tech/personalized-badge/mystic?period=total&units=international_system&left_color=grey&right_color=blue&left_text=pypi%20downloads)](https://pepy.tech/project/mystic)
+[![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/mystic?color=blue&label=conda%20downloads)](https://anaconda.org/conda-forge/mystic)
 [![Stack Overflow](https://img.shields.io/badge/stackoverflow-get%20help-black.svg)](https://stackoverflow.com/questions/tagged/mystic)
 ---------------
 The latest released version of ``mystic`` is available from:
     https://pypi.org/project/mystic
 
 ``mystic`` is distributed under a 3-clause BSD license.
 
@@ -83,15 +101,15 @@
 
 Installation
 ------------
 ``mystic`` can be installed with ``pip``::
 
     $ pip install mystic
 
-To include optional scientific python support, with ``scipy``, install::
+To include optional scientific Python support, with ``scipy``, install::
 
     $ pip install mystic[math]
 
 To include optional plotting support with ``matplotlib``, install::
 
     $ pip install mystic[plotting]
 
@@ -106,90 +124,89 @@
 
 * ``python`` (or ``pypy``), **>=3.7**
 * ``setuptools``, **>=42**
 * ``cython``, **>=0.29.30**
 * ``numpy``, **>=1.0**
 * ``sympy``, **>=0.6.7**
 * ``mpmath``, **>=0.19**
-* ``dill``, **>=0.3.6**
-* ``klepto``, **>=0.2.3**
+* ``dill``, **>=0.3.7**
+* ``klepto``, **>=0.2.4**
 
 Optional requirements:
 
 * ``matplotlib``, **>=0.91**
 * ``scipy``, **>=0.6.0**
-* ``pathos``, **>=0.3.0**
-* ``pyina``, **>=0.2.6**
+* ``pathos``, **>=0.3.1**
+* ``pyina``, **>=0.2.8**
 
 
 More Information
 ----------------
 Probably the best way to get started is to look at the documentation at
 http://mystic.rtfd.io. Also see ``mystic.tests`` for a set of scripts that
 demonstrate several of the many features of the ``mystic`` framework.
 You can run the test suite with ``python -m mystic.tests``. There are
 several plotting scripts that are installed with ``mystic``, primary of which
 are ``mystic_log_reader`` (also available with ``python -m mystic``) and the
 ``mystic_model_plotter`` (also available with ``python -m mystic.models``).
 There are several other plotting scripts that come with ``mystic``, and they
-are detailed elsewhere in the documentation.  See ``mystic.examples`` for
-examples that demonstrate the basic use cases for configuration and launching
-of optimization jobs using one of the sample models provided in
-``mystic.models``. Many of the included examples are standard optimization
-test problems. The use of constraints and penalties are detailed in
-``mystic.examples2``, while more advanced features leveraging ensemble solvers
-and dimensional collapse are found in ``mystic.examples3``. The scripts in
-``mystic.examples4`` demonstrate leveraging ``pathos`` for parallel computing,
-as well as demonstrate some auto-partitioning schemes. ``mystic`` has the
-ability to work in product measure space, and the scripts in
-``mystic.examples5`` show to work with product measures.  The source code is
-generally well documented, so further questions may be resolved by inspecting
-the code itself.  Please feel free to submit a ticket on github, or ask a
-question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``mystic`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+are detailed elsewhere in the documentation.  See https://github.com/uqfoundation/mystic/tree/master/examples for examples that demonstrate the basic use
+cases for configuration and launching of optimization jobs using one of the
+sample models provided in ``mystic.models``. Many of the included examples
+are standard optimization test problems. The use of constraints and penalties
+are detailed in https://github.com/uqfoundation/mystic/tree/master/examples2 while more advanced features leveraging ensemble solvers, machine learning,
+uncertainty quantification, and dimensional collapse are found in https://github.com/uqfoundation/mystic/tree/master/examples3. The scripts in https://github.com/uqfoundation/mystic/tree/master/examples4 demonstrate leveraging ``pathos``
+for parallel computing, as well as demonstrate some auto-partitioning schemes.
+``mystic`` has the ability to work in product measure space, and the scripts in
+https://github.com/uqfoundation/mystic/tree/master/examples5 show how to work
+with product measures at a low level. The source code is generally well
+documented, so further questions may be resolved by inspecting the code itself.
+Please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``mystic`` in your work, please send an email (to **mmckerns at uqfoundation
+dot org**).
 
 Instructions on building a new model are in ``mystic.models.abstract_model``.
 ``mystic`` provides base classes for two types of models:
 
 * ``AbstractFunction``   [evaluates ``f(x)`` for given evaluation points ``x``]
 * ``AbstractModel``      [generates ``f(x,p)`` for given coefficients ``p``]
 
 ``mystic`` also provides some convienence functions to help you build a
 model instance and a cost function instance on-the-fly. For more
 information, see ``mystic.forward_model``.  It is, however, not necessary
 to use base classes or the model builder in building your own model or
-cost function, as any standard python function can be used as long as it
+cost function, as any standard Python function can be used as long as it
 meets the basic ``AbstractFunction`` interface of ``cost = f(x)``.
 
 All ``mystic`` solvers are highly configurable, and provide a robust set of
 methods to help customize the solver for your particular optimization
 problem. For each solver, a minimal (``scipy.optimize``) interface is also
 provided for users who prefer to configure and launch their solvers as a
 single function call. For more information, see ``mystic.abstract_solver``
 for the solver API, and each of the individual solvers for their minimal
 functional interface.
 
 ``mystic`` enables solvers to use parallel computing whenever the user provides
-a replacement for the (serial) python ``map`` function.  ``mystic`` includes a
+a replacement for the (serial) Python ``map`` function.  ``mystic`` includes a
 sample ``map`` in ``mystic.python_map`` that mirrors the behavior of the
-built-in python ``map``, and a ``pool`` in ``mystic.pools`` that provides ``map``
+built-in Python ``map``, and a ``pool`` in ``mystic.pools`` that provides ``map``
 functions using the ``pathos`` (i.e. ``multiprocessing``) interface. ``mystic``
 solvers are designed to utilize distributed and parallel tools provided by
 the ``pathos`` package. For more information, see ``mystic.abstract_map_solver``,
 ``mystic.abstract_ensemble_solver``, and the ``pathos`` documentation at
 http://pathos.rtfd.io.
 
 Important classes and functions are found here:
 
 * ``mystic.solvers``                  [solver optimization algorithms]
 * ``mystic.termination``              [solver termination conditions]
 * ``mystic.strategy``                 [solver population mutation strategies]
 * ``mystic.monitors``                 [optimization monitors]
-* ``mystic.symbolic``                 [symbolic math in constaints]
+* ``mystic.symbolic``                 [symbolic math in constraints]
 * ``mystic.constraints``              [constraints functions]
 * ``mystic.penalty``                  [penalty functions]
 * ``mystic.collapse``                 [checks for dimensional collapse]
 * ``mystic.coupler``                  [decorators for function coupling]
 * ``mystic.pools``                    [parallel worker pool interface]
 * ``mystic.munge``                    [file readers and writers]
 * ``mystic.scripts``                  [model and convergence plotting]
@@ -225,14 +242,15 @@
 * ``mystic.models.abstract_model``    [the model API definition]
 
 ``mystic`` also provides several convience scripts that are used to visualize
 models, convergence, and support on the hypercube. These scripts are installed
 to a directory on the user's ``$PATH``, and thus can be run from anywhere:
 
 * ``mystic_log_reader``               [parameter and cost convergence]
+* ``mystic_log_converter``            [logfile format converter]
 * ``mystic_collapse_plotter``         [convergence and dimensional collapse]
 * ``mystic_model_plotter``            [model surfaces and solver trajectory]
 * ``support_convergence``             [convergence plots for measures]
 * ``support_hypercube``               [parameter support on the hypercube]
 * ``support_hypercube_measures``      [measure support on the hypercube]
 * ``support_hypercube_scenario``      [scenario support on the hypercube]
```

### Comparing `mystic-0.4.0/docs/Makefile` & `mystic-0.4.1/docs/Makefile`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/docs/source/conf.py` & `mystic-0.4.1/docs/source/conf.py`

 * *Files 10% similar despite different names*

```diff
@@ -20,14 +20,15 @@
 from datetime import datetime
 import sys
 scripts = os.path.abspath('../../scripts')
 sys.path.insert(0, scripts)
 try:
     os.symlink(scripts+os.sep+'mystic_collapse_plotter', scripts+os.sep+'_mystic_collapse_plotter.py')
     os.symlink(scripts+os.sep+'mystic_log_reader', scripts+os.sep+'_mystic_log_reader.py')
+    os.symlink(scripts+os.sep+'mystic_log_converter', scripts+os.sep+'_mystic_log_converter.py')
     os.symlink(scripts+os.sep+'mystic_model_plotter', scripts+os.sep+'_mystic_model_plotter.py')
     os.symlink(scripts+os.sep+'support_convergence', scripts+os.sep+'_support_convergence.py')
     os.symlink(scripts+os.sep+'support_hypercube', scripts+os.sep+'_support_hypercube.py')
     os.symlink(scripts+os.sep+'support_hypercube_measures', scripts+os.sep+'_support_hypercube_measures.py')
     os.symlink(scripts+os.sep+'support_hypercube_scenario', scripts+os.sep+'_support_hypercube_scenario.py')
 except:
     pass
@@ -59,24 +60,42 @@
 # source_suffix = ['.rst', '.md']
 source_suffix = '.rst'
 
 # The master toctree document.
 master_doc = 'index'
 
 # General information about the project.
-project = u'mystic'
+project = 'mystic'
 year = datetime.now().year
-copyright = u'%d, The Uncertainty Quantification Foundation' % year
-author = u'Mike McKerns'
+copyright = '%d, The Uncertainty Quantification Foundation' % year
+author = 'Mike McKerns'
 
 # extension config
 github_project_url = "https://github.com/uqfoundation/mystic"
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
@@ -88,15 +107,15 @@
 release = version
 
 # The language for content autogenerated by Sphinx. Refer to documentation
 # for a list of supported languages.
 #
 # This is also used if you do content translation via gettext catalogs.
 # Usually you set "language" from the command line for these cases.
-language = None
+language = 'en'
 
 # List of patterns, relative to source directory, that match files and
 # directories to ignore when looking for source files.
 # This patterns also effect to html_static_path and html_extra_path
 exclude_patterns = []
 
 # The name of the Pygments (syntax highlighting) style to use.
@@ -116,57 +135,63 @@
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
     'github_user': 'uqfoundation',
     'github_repo': 'mystic',
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
 htmlhelp_basename = 'mysticdoc'
 
 # Logo for sidebar
@@ -193,45 +218,45 @@
     # 'figure_align': 'htbp',
 }
 
 # Grouping the document tree into LaTeX files. List of tuples
 # (source start file, target name, title,
 #  author, documentclass [howto, manual, or own class]).
 latex_documents = [
-    (master_doc, 'mystic.tex', u'mystic Documentation',
-     u'Mike McKerns', 'manual'),
+    (master_doc, 'mystic.tex', 'mystic Documentation',
+     'Mike McKerns', 'manual'),
 ]
 
 
 # -- Options for manual page output ---------------------------------------
 
 # One entry per manual page. List of tuples
 # (source start file, name, description, authors, manual section).
 man_pages = [
-    (master_doc, 'mystic', u'mystic Documentation',
+    (master_doc, 'mystic', 'mystic Documentation',
      [author], 1)
 ]
 
 
 # -- Options for Texinfo output -------------------------------------------
 
 # Grouping the document tree into Texinfo files. List of tuples
 # (source start file, target name, title, author,
 #  dir menu entry, description, category)
 texinfo_documents = [
-    (master_doc, 'mystic', u'mystic Documentation',
-     author, 'mystic', 'Highly-constrained non-convex optimization and uncertainty quantification.',
+    (master_doc, 'mystic', 'mystic Documentation',
+     author, 'mystic', 'Constrained nonlinear optimization for scientific machine learning, UQ, and AI.',
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

### Comparing `mystic-0.4.0/docs/source/mystic2.png` & `mystic-0.4.1/docs/source/mystic2.png`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/examples/DATA/g1.pts` & `mystic-0.4.1/examples/DATA/g1.pts`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/examples/DATA/g2.pts` & `mystic-0.4.1/examples/DATA/g2.pts`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/examples/NOTES` & `mystic-0.4.1/examples/NOTES`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/examples/README` & `mystic-0.4.1/examples/README`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/examples/TEST_ffitPP.py` & `mystic-0.4.1/examples/TEST_ffitPP.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Same as test_ffit.py
 but uses DifferentialEvolutionSolver2 instead.
 
 Note:
```

### Comparing `mystic-0.4.0/examples/TEST_ffitPP2.py` & `mystic-0.4.1/examples/TEST_ffitPP2.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Testing the polynomial fitting problem of [1] using scipy's Nelder-Mead algorithm.
 
 Reference:
```

### Comparing `mystic-0.4.0/examples/TEST_ffitPP2_b.py` & `mystic-0.4.1/examples/TEST_ffitPP2_b.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Testing the polynomial fitting problem of [1] using scipy's Nelder-Mead algorithm.
 
 Reference:
```

### Comparing `mystic-0.4.0/examples/TEST_ffitPP_b.py` & `mystic-0.4.1/examples/TEST_ffitPP_b.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Same as test_ffit.py
 but uses DifferentialEvolutionSolver2 instead.
 
 Note:
@@ -43,28 +43,26 @@
     if px<0: result += px*px
 
     return result
 
 
 def main(servers,ncpus):
     from mystic.solvers import DifferentialEvolutionSolver2
-   #from pathos.pools import ProcessPool as Pool
     from pathos.pools import ParallelPool as Pool
 
     solver = DifferentialEvolutionSolver2(ND, NP)
-    solver.SetMapper(Pool().map)
+    solver.SetMapper(Pool(ncpus, servers=servers).map)
     solver.SetRandomInitialPoints(min = [-100.0]*ND, max = [100.0]*ND)
     solver.SetEvaluationLimits(generations=MAX_GENERATIONS)
     solver.SetGenerationMonitor(VerboseMonitor(30))
     solver.enable_signal_handler()
   
     strategy = Best1Exp
     #strategy = Best1Bin
 
-    solver.SelectServers(servers,ncpus)
     solver.Solve(ChebyshevCost, termination=VTR(0.01), strategy=strategy, \
                  CrossProbability=1.0, ScalingFactor=0.9 , \
                  sigint_callback=plot_solution)
 
     solution = solver.Solution()
 
     return solution
```

### Comparing `mystic-0.4.0/examples/buckshot_example06.py` & `mystic-0.4.1/examples/buckshot_example06.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Solve 8th-order Chebyshev polynomial coefficients with Powell's method.
     - Uses BuckshotSolver to provide 'pseudo-global' optimization
     - Plot of fitting to Chebyshev polynomial.
```

### Comparing `mystic-0.4.0/examples/cg_rosenbrock.py` & `mystic-0.4.1/examples/cg_rosenbrock.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 See test_rosenbrock.py.
 
 This one uses Scipy's CG (Polak-Ribiere) plus viz via matplotlib
```

### Comparing `mystic-0.4.0/examples/constraint1_example01.py` & `mystic-0.4.1/examples/constraint1_example01.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Minimize Rosenbrock's Function with Powell's method.
 
 Demonstrates:
```

### Comparing `mystic-0.4.0/examples/constraint2_example01.py` & `mystic-0.4.1/examples/constraint2_example01.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Minimize Rosenbrock's Function with Powell's method.
 
 Demonstrates:
```

### Comparing `mystic-0.4.0/examples/constraint3_example01.py` & `mystic-0.4.1/examples/constraint3_example01.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Minimize Rosenbrock's Function with Powell's method.
 
 Demonstrates:
```

### Comparing `mystic-0.4.0/examples/example01.py` & `mystic-0.4.1/examples/example01.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Minimize Rosenbrock's Function with Powell's method.
 
 Demonstrates:
```

### Comparing `mystic-0.4.0/examples/example02.py` & `mystic-0.4.1/examples/example02.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Minimize Rosenbrock's Function with Nelder-Mead.
     - Plot of Rosenbrock's function minimum.
```

### Comparing `mystic-0.4.0/examples/example03.py` & `mystic-0.4.1/examples/example03.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Minimize Rosenbrock's Function with Nelder-Mead.
     - Plot of parameter convergence to function minimum.
```

### Comparing `mystic-0.4.0/examples/example04.py` & `mystic-0.4.1/examples/example04.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Minimize Rosenbrock's Function with Nelder-Mead.
     - Dynamic plot of parameter convergence to function minimum.
```

### Comparing `mystic-0.4.0/examples/example05.py` & `mystic-0.4.1/examples/example05.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Minimize Rosenbrock's Function with Powell's method.
     - Dynamic print of parameter convergence to function minimum.
```

### Comparing `mystic-0.4.0/examples/example06.py` & `mystic-0.4.1/examples/example06.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Solve 8th-order Chebyshev polynomial coefficients with Powell's method.
     - Plot of fitting to Chebyshev polynomial.
```

### Comparing `mystic-0.4.0/examples/example07.py` & `mystic-0.4.1/examples/example07.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Solve 8th-order Chebyshev polynomial coefficients with DE.
     - Plot of fitting to Chebyshev polynomial.
```

### Comparing `mystic-0.4.0/examples/example08.py` & `mystic-0.4.1/examples/example08.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Solve 8th-order Chebyshev polynomial coefficients with DE.
     - Callable plot of fitting to Chebyshev polynomial.
     - Monitor Chi-Squared for Chebyshev polynomial.
@@ -91,15 +91,15 @@
                  CrossProbability=1.0, ScalingFactor=0.9, \
                  sigint_callback=plot_solution)
     solution = solver.Solution()
 
     # use monitor to retrieve results information
     iterations = len(stepmon)
     cost = stepmon.y[-1]
-    print("Generation %d has best Chi-Squared: %f" % (iterations, cost))
+    print("Generation %d has best Chi-Squared: %s" % (iterations, cost))
 
     # use pretty print for polynomials
     print(poly1d(solution))
 
     # compare solution with actual 8th-order Chebyshev coefficients
     print("\nActual Coefficients:\n %s\n" % poly1d(chebyshev8coeffs))
```

### Comparing `mystic-0.4.0/examples/example09.py` & `mystic-0.4.1/examples/example09.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Solve 8th-order Chebyshev polynomial coefficients with DE.
     - Callable plot of fitting to Chebyshev polynomial.
     - Monitor Chi-Squared for Chebyshev polynomial.
@@ -98,15 +98,15 @@
                  CrossProbability=0.8, ScalingFactor=0.5, \
                  sigint_callback=plot_solution)
     solution = solver.Solution()
 
     # use monitor to retrieve results information
     iterations = len(stepmon)
     cost = stepmon.y[-1]
-    print("Generation %d has best Chi-Squared: %f" % (iterations, cost))
+    print("Generation %d has best Chi-Squared: %s" % (iterations, cost))
 
     # use pretty print for polynomials
     print(poly1d(solution))
 
     # compare solution with actual 8th-order Chebyshev coefficients
     print("\nActual Coefficients:\n %s\n" % poly1d(chebyshev8coeffs))
```

### Comparing `mystic-0.4.0/examples/example10.py` & `mystic-0.4.1/examples/example10.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Solve 8th-order Chebyshev polynomial coefficients with DE.
     - Plot (x2) of convergence to Chebyshev polynomial.
     - Monitor (x2) Chi-Squared for Chebyshev polynomial.
@@ -82,15 +82,15 @@
     solver.Solve(chebyshev8cost, termination=VTR(0.01), strategy=Best1Exp, \
                  CrossProbability=1.0, ScalingFactor=0.9)
     solution = solver.bestSolution
 
     # get solved coefficients and Chi-Squared (from solver members)
     iterations = solver.generations
     cost = solver.bestEnergy
-    print("Generation %d has best Chi-Squared: %f" % (iterations, cost))
+    print("Generation %d has best Chi-Squared: %s" % (iterations, cost))
     print("Solved Coefficients:\n %s\n" % poly1d(solver.bestSolution))
 
     # plot convergence of coefficients per iteration
     plot_frame('iterations')
     plot_params(stepmon)
     getch()
```

### Comparing `mystic-0.4.0/examples/example11.py` & `mystic-0.4.1/examples/example11.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Solve 8th-order Chebyshev polynomial coefficients with Nelder-Mead.
     - Callable plot of fitting to Chebyshev polynomial.
     - Plot (x2) of convergence to Chebyshev polynomial.
@@ -122,15 +122,15 @@
     solver.Solve(chebyshev8cost, termination=CRT(1e-4,1e-4), \
                  sigint_callback=plot_solution)
     solution = solver.bestSolution
 
     # get solved coefficients and Chi-Squared (from solver members)
     iterations = solver.generations
     cost = solver.bestEnergy
-    print("Generation %d has best Chi-Squared: %f" % (iterations, cost))
+    print("Generation %d has best Chi-Squared: %s" % (iterations, cost))
     print("Solved Coefficients:\n %s\n" % poly1d(solver.bestSolution))
 
     # compare solution with actual 8th-order Chebyshev coefficients
     print("Actual Coefficients:\n %s\n" % poly1d(chebyshev8coeffs))
 
     # plot solution versus exact coefficients
     plot_solution(solution)
```

### Comparing `mystic-0.4.0/examples/example12.py` & `mystic-0.4.1/examples/example12.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Solve 5th-order polynomial coefficients with Powell's method.
     - Plot of fitting to 5th-order polynomial.
```

### Comparing `mystic-0.4.0/examples/ezmap_desolve.py` & `mystic-0.4.1/examples/ezmap_desolve.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 # Adapted from parallel_desolve.py
 
 __doc__ = """
 # Tests MPI version of Storn and Price's Polynomial 'Fitting' Problem,
```

### Comparing `mystic-0.4.0/examples/ezmap_desolve_rosen.py` & `mystic-0.4.1/examples/ezmap_desolve_rosen.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 # Adapted from parallel_desolve.py
 
 __doc__ = """
 # Tests MPI version of Storn and Price's Polynomial 'Fitting' Problem,
```

### Comparing `mystic-0.4.0/examples/forward_model.py` & `mystic-0.4.1/examples/forward_model.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 forward_model example
 """
 from mystic.forward_model import *
```

### Comparing `mystic-0.4.0/examples/gplot_test_ffit.py` & `mystic-0.4.1/examples/gplot_test_ffit.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Adapted from DETest.py by Patrick Hung
 
 Sets up Storn and Price's Polynomial 'Fitting' Problem.
```

### Comparing `mystic-0.4.0/examples/lattice_example06.py` & `mystic-0.4.1/examples/lattice_example06.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example:
     - Solve 8th-order Chebyshev polynomial coefficients with Powell's method.
     - Uses LatticeSolver to provide 'pseudo-global' optimization
     - Plot of fitting to Chebyshev polynomial.
```

### Comparing `mystic-0.4.0/examples/metropolis.py` & `mystic-0.4.1/examples/metropolis.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 exercises the Metropolis-Hastings algorithm
 """
 
 from mystic.metropolis import metropolis_hastings
```

### Comparing `mystic-0.4.0/examples/mpl_corana.py` & `mystic-0.4.1/examples/mpl_corana.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Testing the Corana parabola in 1D. Requires matplotlib.
 """
 
 import matplotlib.pyplot as plt, numpy, mystic
```

### Comparing `mystic-0.4.0/examples/mpmap_desolve.py` & `mystic-0.4.1/examples/mpmap_desolve.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 # Adapted from parallel_desolve.py
 
 __doc__ = """
 # Tests MP version of Storn and Price's Polynomial 'Fitting' Problem.
```

### Comparing `mystic-0.4.0/examples/mpmap_desolve_rosen.py` & `mystic-0.4.1/examples/mpmap_desolve_rosen.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 # Adapted from parallel_desolve.py
 
 __doc__ = """
 # Tests MP version of Storn and Price's Polynomial 'Fitting' Problem.
```

### Comparing `mystic-0.4.0/examples/raw_chebyshev8.py` & `mystic-0.4.1/examples/raw_chebyshev8.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
  
 """ NOTE:
 due to pickling issues, cost function is provided w/o using a factory method.
 also, a local import of 'polyeval' avoides a NameError.
 """
```

### Comparing `mystic-0.4.0/examples/raw_chebyshev8b.py` & `mystic-0.4.1/examples/raw_chebyshev8b.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
  
 """ NOTE:
 due to pickling issues, cost function is provided w/o using a factory method.
 (same as chebyshev8.py, except uses global target,polyeval,poly1d)
 """
```

### Comparing `mystic-0.4.0/examples/raw_rosen.py` & `mystic-0.4.1/examples/raw_rosen.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 """ NOTE:
 rosen rewritten as a pickleable function
 """
```

### Comparing `mystic-0.4.0/examples/restart_solver.py` & `mystic-0.4.1/examples/restart_solver.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.solvers import DifferentialEvolutionSolver
 from mystic.solvers import NelderMeadSimplexSolver
 from mystic.termination import VTR, ChangeOverGeneration, When, Or
 from mystic.monitors import VerboseMonitor
```

### Comparing `mystic-0.4.0/examples/rosetta_mogi.py` & `mystic-0.4.1/examples/rosetta_mogi.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example use of Forward Mogi Model
 in mystic and PARK optimization frameworks.
 (built for mystic "trunk" and with park-1.2)
```

### Comparing `mystic-0.4.0/examples/rosetta_parabola.py` & `mystic-0.4.1/examples/rosetta_parabola.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Example use of Forward Poly Model
 in mystic and PARK optimization frameworks.
 (built for mystic "trunk" and with park-1.2)
```

### Comparing `mystic-0.4.0/examples/test_circle.py` & `mystic-0.4.1/examples/test_circle.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Given a set of points in the plane, find the smallest circle
 that contains them. (using DE and scipy.fmin)
 
 Requires:
```

### Comparing `mystic-0.4.0/examples/test_circle_dual.py` & `mystic-0.4.1/examples/test_circle_dual.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Solve the dual form of test_circle.py.
 
 Given a set of points in the plane, find the smallest circle
 that contains them.
```

### Comparing `mystic-0.4.0/examples/test_corana.py` & `mystic-0.4.1/examples/test_corana.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Sets up Corana's parabola. This is problem 6 of testbed 1 in [1].
 
 Exact answer: Min = 0 @ abs(x_j) < 0.05 for all j.
```

### Comparing `mystic-0.4.0/examples/test_dejong3.py` & `mystic-0.4.1/examples/test_dejong3.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Sets up De Jong's Third function. This is problem 3 of testbed 1 in [1].
 
 Note: The function as defined by Eq.8 of [1] seems incomplete.
```

### Comparing `mystic-0.4.0/examples/test_dejong4.py` & `mystic-0.4.1/examples/test_dejong4.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Sets up De Jong's Fourth function. This is problem 4 of testbed 1 in [1].
 
 This is function fitting "with noise."
 Reference:
```

### Comparing `mystic-0.4.0/examples/test_dejong5.py` & `mystic-0.4.1/examples/test_dejong5.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Sets up De Jong's Fifth function. This is problem 5 of testbed 1 in [1].
 
 Exact answer: Min = 0 @ (-32, -32)
```

### Comparing `mystic-0.4.0/examples/test_ffit.py` & `mystic-0.4.1/examples/test_ffit.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Adapted from DETest.py by Patrick Hung
 
 Sets up Storn and Price's Polynomial 'Fitting' Problem.
```

### Comparing `mystic-0.4.0/examples/test_ffit2.py` & `mystic-0.4.1/examples/test_ffit2.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Sets up Storn and Price's Polynomial 'Fitting' Problem for ChebyshevT16
 
 Reference:
 
@@ -61,15 +61,15 @@
   
     print("\nsolved: ")
     print(poly1d(solution))
     print("\ntarget: ")
     print(poly1d(Chebyshev16))
    #print("actual coefficients vs computed:")
    #for actual,computed in zip(Chebyshev16, solution):
-   #    print("%f %f" % (actual, computed))
+   #    print("%s %s" % (actual, computed))
 
     plot_solution(solution, Chebyshev16)
 
 
 if __name__ == '__main__':
     from timeit import Timer
     t = Timer("main()", "from __main__ import main")
```

### Comparing `mystic-0.4.0/examples/test_ffitB.py` & `mystic-0.4.1/examples/test_ffitB.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Same as test_ffit.py
 but uses DifferentialEvolutionSolver2 instead.
 
 Note:
```

### Comparing `mystic-0.4.0/examples/test_ffitC.py` & `mystic-0.4.1/examples/test_ffitC.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Testing the polynomial fitting problem of [1] using scipy's Nelder-Mead algorithm.
 
 Reference:
```

### Comparing `mystic-0.4.0/examples/test_ffitD.py` & `mystic-0.4.1/examples/test_ffitD.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Same as test_ffitB.py
 but using the 'one-liner' solver interface.
 
 Reference:
```

### Comparing `mystic-0.4.0/examples/test_fosc3d.py` & `mystic-0.4.1/examples/test_fosc3d.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Adapted from The Mathematica Guidebook, Numerics.
 
 """
```

### Comparing `mystic-0.4.0/examples/test_getCost.py` & `mystic-0.4.1/examples/test_getCost.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 test_getCost.py
 Example to demonstrate use of CostFactory
 """
```

### Comparing `mystic-0.4.0/examples/test_griewangk.py` & `mystic-0.4.1/examples/test_griewangk.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Sets up Griewangk's function. This is problem 7 of testbed 1 in [1].
 
 Solution: Min of 0 @ Vector[0]
```

### Comparing `mystic-0.4.0/examples/test_lorentzian.py` & `mystic-0.4.1/examples/test_lorentzian.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Alternate fitting of a lorentzian peak (see test_lorentzian2.py)
 """
 
 import matplotlib.pyplot as plt, matplotlib
```

### Comparing `mystic-0.4.0/examples/test_lorentzian2.py` & `mystic-0.4.1/examples/test_lorentzian2.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Same as test_lorentzian, but with n being a fitted variable
 
 This is MUCH faster than test_lorentzian because the cost function no
 longer has to do an "integral" as an intermediate step
```

### Comparing `mystic-0.4.0/examples/test_mogi.py` & `mystic-0.4.1/examples/test_mogi.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Tests a single mogi fitting. 
 
 Script is pretty crude right now.
```

### Comparing `mystic-0.4.0/examples/test_mogi2.py` & `mystic-0.4.1/examples/test_mogi2.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Two mogi sources. Similar to test_mogi.py. (See that one first)
 
 Reference:
```

### Comparing `mystic-0.4.0/examples/test_mogi3.py` & `mystic-0.4.1/examples/test_mogi3.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 One mogi source, similar to test_mogi, but uses
 CostFactory objects
 
 """
```

### Comparing `mystic-0.4.0/examples/test_mogi4.py` & `mystic-0.4.1/examples/test_mogi4.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Similar to test_mogi2 (two sources) (See that one first)
 """
 
 from test_mogi2 import params0, params1, stations, data, data_z, ND, NP, plot_sol, plot_noisy_data, MAX_GENERATIONS, ForwardMogiFactory
```

### Comparing `mystic-0.4.0/examples/test_mogi_basin.py` & `mystic-0.4.1/examples/test_mogi_basin.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Similar to test_mogi.py
 but using scipy's basinhopping algorithm
 """
```

### Comparing `mystic-0.4.0/examples/test_peaks.py` & `mystic-0.4.1/examples/test_peaks.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Testing the 'Peaks" Function.
 
 (tests VTR when minimum has negative value)
 """
```

### Comparing `mystic-0.4.0/examples/test_rosenbrock.py` & `mystic-0.4.1/examples/test_rosenbrock.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Testing Rosenbrock's Function.
 
 This is a very popular function for testing minimization algorithm.
 The following provides tests for both bounded and unbounded minimization
```

### Comparing `mystic-0.4.0/examples/test_rosenbrock2.py` & `mystic-0.4.1/examples/test_rosenbrock2.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 example of using NelderMeadSimplexSolver on the rosenbrock function
 """
 
 from mystic.models import rosen
```

### Comparing `mystic-0.4.0/examples/test_rosenbrock3.py` & `mystic-0.4.1/examples/test_rosenbrock3.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 example of using PowellDirectionalSolver on the rosenbrock function
 """
 
 from mystic.models import rosen
```

### Comparing `mystic-0.4.0/examples/test_rosenbrock3b.py` & `mystic-0.4.1/examples/test_rosenbrock3b.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 example of using DifferentialEvolutionSolver on the rosenbrock function
 """
 
 from mystic.models import rosen
```

### Comparing `mystic-0.4.0/examples/test_scem.py` & `mystic-0.4.1/examples/test_scem.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Tests functionality of misc. functions in scem.py
 """
 
 from mystic.scemtools import *
```

### Comparing `mystic-0.4.0/examples/test_svc1.py` & `mystic-0.4.1/examples/test_svc1.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Support Vector Classification. Example 1
 """
 
 from numpy import *
```

### Comparing `mystic-0.4.0/examples/test_svc2.py` & `mystic-0.4.1/examples/test_svc2.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Support Vector Classification. Example 2.
 
 using meristem data from data files
 """
```

### Comparing `mystic-0.4.0/examples/test_svr1.py` & `mystic-0.4.1/examples/test_svr1.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Support Vector Regression. Example 1
 """
 
 from numpy import *
```

### Comparing `mystic-0.4.0/examples/test_svr2.py` & `mystic-0.4.1/examples/test_svr2.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Support Vector Regression. Example 2
 """
 
 from numpy import *
```

### Comparing `mystic-0.4.0/examples/test_twistedgaussian.py` & `mystic-0.4.1/examples/test_twistedgaussian.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 The Twisted Gausssian in
 "Shuffled Complex Evolution Metropolis" Algoritm of Vrugt et al. [1]
 
 Reference:
```

### Comparing `mystic-0.4.0/examples/test_twistedgaussian2.py` & `mystic-0.4.1/examples/test_twistedgaussian2.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 In test_twistedgaussian, we compared SCEM (one chain) with metropolis.
 
 Now we will use n-chain SCEM .
 """
```

### Comparing `mystic-0.4.0/examples/test_twistedgaussian3.py` & `mystic-0.4.1/examples/test_twistedgaussian3.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 In test_twistedgaussian, we compared SCEM (one chain) with metropolis.
 
 Now we will use n-chain SCEM / in parallel.
 """
```

### Comparing `mystic-0.4.0/examples/test_wavy.py` & `mystic-0.4.1/examples/test_wavy.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 test some simple multi-minima functions, such as |x + 3 sin[x]|
 """
 
 from mystic.solvers import DifferentialEvolutionSolver2 as DifferentialEvolutionSolver
```

### Comparing `mystic-0.4.0/examples/test_zimmermann.py` & `mystic-0.4.1/examples/test_zimmermann.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Sets up Zimmermann's problem. This is problem 8 of testbed 1 in [1] and [2].
 
 Solution: Min of 0 @ Vector[0]
```

### Comparing `mystic-0.4.0/examples2/README` & `mystic-0.4.1/examples2/README`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/examples2/beam.py` & `mystic-0.4.1/examples2/beam.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 "Welded Beam Design"
 
 def objective(x):
     x0,x1,x2,x3 = x
     return 1.10471*x0**2*x1 + 0.04811*x2*x3*(14.0 + x1)
```

### Comparing `mystic-0.4.0/examples2/boolean.py` & `mystic-0.4.1/examples2/boolean.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Maximization with a boolean variable and constraints.
 
 Maximize:
     sum_{i=1}^{n-1} sum_{j=i+1}^{n} w_{ij} x_{i} x_{j}
```

### Comparing `mystic-0.4.0/examples2/constrained_scipy.py` & `mystic-0.4.1/examples2/constrained_scipy.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
   Example applying mystic to scipy.optimize
 
   Minimize:
             f(x) = 3*A + 1e-6*A**3 + 2*B + 2e-6/(3*B**3) + C**2
```

### Comparing `mystic-0.4.0/examples2/crypta.py` & `mystic-0.4.1/examples2/crypta.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # Example in google/or-tools
 # https://github.com/google/or-tools/blob/master/examples/python/crypta.py
 # with Copyright 2010 Hakan Kjellerstrand hakank@bonetmail.com
 # and disclamer as stated at the above reference link.
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
   Cryptarithmetic puzzle in Google CP Solver.
 
   Prolog benchmark problem
   '''
```

### Comparing `mystic-0.4.0/examples2/crypto.py` & `mystic-0.4.1/examples2/crypto.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # Example in google/or-tools
 # https://github.com/google/or-tools/blob/master/examples/python/crypto.py
 # with Copyright 2010 Hakan Kjellerstrand hakank@bonetmail.com
 # and disclamer as stated at the above reference link.
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
   Crypto problem in Google CP Solver.
 
   Prolog benchmark problem
   '''
```

### Comparing `mystic-0.4.0/examples2/cvxlp.py` & `mystic-0.4.1/examples2/cvxlp.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # Problem definition:
 # Example in reference documentation for cvxopt
 # http://cvxopt.org/examples/tutorial/lp.html
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
     Minimize: f = 2*x[0] + 1*x[1]
 
     Subject to:  -1*x[0] + 1*x[1] <= 1
                   1*x[0] + 1*x[1] >= 2
```

### Comparing `mystic-0.4.0/examples2/cvxqp.py` & `mystic-0.4.1/examples2/cvxqp.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # Problem definition:
 # Example in reference documentation for cvxopt
 # http://cvxopt.org/examples/tutorial/qp.html
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
     Minimize: f = 2*x[0]**2 + x[1]**2 + x[0]*x[1] + x[0] + x[1]
 
     Subject to:     x[0] >= 0
                            x[1] >= 0
```

### Comparing `mystic-0.4.0/examples2/cvxqp_alt.py` & `mystic-0.4.1/examples2/cvxqp_alt.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # Problem definition:
 # Example in reference documentation for cvxopt
 # http://cvxopt.org/examples/tutorial/qp.html
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from cvxqp import objective, bounds, xs, ys
     
 from mystic.penalty import quadratic_equality
 from mystic.constraints import with_penalty
```

### Comparing `mystic-0.4.0/examples2/cvxqp_alt2.py` & `mystic-0.4.1/examples2/cvxqp_alt2.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # Problem definition:
 # Example in reference documentation for cvxopt
 # http://cvxopt.org/examples/tutorial/qp.html
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from cvxqp import objective, bounds, xs, ys
 
 from mystic.math.measures import normalize
```

### Comparing `mystic-0.4.0/examples2/datafit.py` & `mystic-0.4.1/examples2/datafit.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # Problem definition:
 # Example in reference documentation for scipy.optimze
 # http://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.curve_fit.html
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
     Fit parameters to noisy data:
                y(x) ~ a * exp(-b * x) + c
 
     where:
```

### Comparing `mystic-0.4.0/examples2/eq10.py` & `mystic-0.4.1/examples2/eq10.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # Example in google/or-tools
 # https://github.com/google/or-tools/blob/master/examples/python/ex10.py
 # with Copyright 2010 Hakan Kjellerstrand hakank@bonetmail.com
 # and disclamer as stated at the above reference link.
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
   Eq 10 in Google CP Solver.
 
   Standard benchmark problem.
 """
```

### Comparing `mystic-0.4.0/examples2/eq20.py` & `mystic-0.4.1/examples2/eq20.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # Example in google/or-tools
 # https://github.com/google/or-tools/blob/master/examples/python/ex20.py
 # with Copyright 2010 Hakan Kjellerstrand hakank@bonetmail.com
 # and disclamer as stated at the above reference link.
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
   Eq 20 in Google CP Solver.
 
   Standard benchmark problem.
 """
```

### Comparing `mystic-0.4.0/examples2/g01.py` & `mystic-0.4.1/examples2/g01.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     return 5*sum(x[:4]) - 5*sum([xi**2 for xi in x[:4]]) - sum(x[4:])
 
 bounds = [(0,1)]*9 + [(0,100)]*3 + [(0,1)]
```

### Comparing `mystic-0.4.0/examples2/g01_alt.py` & `mystic-0.4.1/examples2/g01_alt.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g01 import objective, bounds, xs, ys
 
 from mystic.constraints import as_constraint
 from mystic.penalty import quadratic_inequality
```

### Comparing `mystic-0.4.0/examples2/g01_alt2.py` & `mystic-0.4.1/examples2/g01_alt2.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g01 import objective, bounds, xs, ys
 from g01_alt import penalty1, penalty2, penalty3, penalty4, penalty5, \
                     penalty6, penalty7, penalty8, penalty9
```

### Comparing `mystic-0.4.0/examples2/g02.py` & `mystic-0.4.1/examples2/g02.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     from numpy import abs, sum, cos, product, sqrt
     sum_jx = 0.0
     for j in range(len(x)): sum_jx = sum_jx + (j+1) * x[j]**2
```

### Comparing `mystic-0.4.0/examples2/g02_alt.py` & `mystic-0.4.1/examples2/g02_alt.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,25 +7,25 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g02 import objective, bounds, xs, ys
 
 from mystic.constraints import as_constraint
 from mystic.penalty import quadratic_inequality
 
 def penalty1(x): # <= 0.0
-    from numpy import product
+    from numpy import prod as product
     return -product(x) + 0.75
 
 def penalty2(x): # <= 0.0
     from numpy import sum
     return sum(x) - 7.5*len(x)
 
 @quadratic_inequality(penalty1)
```

### Comparing `mystic-0.4.0/examples2/g02_alt2.py` & `mystic-0.4.1/examples2/g02_alt2.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g02 import objective, bounds, xs, ys
 from g02_alt import penalty1, penalty2, quadratic_inequality
 
 from mystic.math.measures import impose_product, impose_sum
```

### Comparing `mystic-0.4.0/examples2/g03.py` & `mystic-0.4.1/examples2/g03.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     from numpy import prod, sqrt
     n = len(x)
     return -sqrt(n)*n * prod(x)
```

### Comparing `mystic-0.4.0/examples2/g03_alt.py` & `mystic-0.4.1/examples2/g03_alt.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g03 import objective, bounds, xs, ys
 
 from mystic.penalty import quadratic_equality
 from mystic.constraints import with_penalty
```

### Comparing `mystic-0.4.0/examples2/g04.py` & `mystic-0.4.1/examples2/g04.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     x0,x1,x2,x3,x4 = x #XXX: allow x != 5?
     return 5.3578547*x2**2 + 0.8356891*x0*x4 + 37.293239*x0 - 40792.141
```

### Comparing `mystic-0.4.0/examples2/g05.py` & `mystic-0.4.1/examples2/g05.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     x0,x1,x2,x3 = x
     return 3*x0 + 1.e-6*x0**3 + 2*x1 + 2.e-6/3*x1**3
```

### Comparing `mystic-0.4.0/examples2/g05_alt.py` & `mystic-0.4.1/examples2/g05_alt.py`

 * *Files 4% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g05 import objective, bounds, xs, ys
 
 from mystic.constraints import as_constraint
 from mystic.penalty import quadratic_inequality, quadratic_equality
```

### Comparing `mystic-0.4.0/examples2/g06.py` & `mystic-0.4.1/examples2/g06.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     x0,x1 = x
     return (x0 - 10)**3 + (x1 - 20)**3
```

### Comparing `mystic-0.4.0/examples2/g06_alt.py` & `mystic-0.4.1/examples2/g06_alt.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g06 import objective, bounds, xs, ys
 
 from mystic.constraints import as_constraint
 from mystic.penalty import quadratic_inequality
```

### Comparing `mystic-0.4.0/examples2/g07.py` & `mystic-0.4.1/examples2/g07.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     x0,x1,x2,x3,x4,x5,x6,x7,x8,x9 = x
     return x0**2 + x1**2 + x0*x1 - 14*x0 - 16*x1 + (x2-10)**2 + \
            4*(x3-5)**2 + (x4-3)**2 + 2*(x5-1)**2 + 5*x6**2 + \
```

### Comparing `mystic-0.4.0/examples2/g07_alt.py` & `mystic-0.4.1/examples2/g07_alt.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g07 import objective, bounds, xs, ys
 
 from mystic.constraints import as_constraint
 from mystic.penalty import quadratic_inequality
```

### Comparing `mystic-0.4.0/examples2/g08.py` & `mystic-0.4.1/examples2/g08.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     x0,x1 = x
     from math import sin, pi
     return -(sin(2*pi*x0)**3 * sin(2*pi*x1)) / (x0**3 * (x0 + x1))
```

### Comparing `mystic-0.4.0/examples2/g08_alt.py` & `mystic-0.4.1/examples2/g08_alt.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g08 import objective, bounds, xs, ys
 
 from mystic.constraints import as_constraint
 from mystic.penalty import quadratic_inequality
```

### Comparing `mystic-0.4.0/examples2/g09.py` & `mystic-0.4.1/examples2/g09.py`

 * *Files 7% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     x0,x1,x2,x3,x4,x5,x6 = x
     return (x0-10)**2 + 5*(x1-12)**2 + x2**4 + 3*(x3-11)**2 + \
            10*x4**6 + 7*x5**2 + x6**4 - 4*x5*x6 - 10*x5 - 8*x6
```

### Comparing `mystic-0.4.0/examples2/g09_alt.py` & `mystic-0.4.1/examples2/g09_alt.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g09 import objective, bounds, xs, ys
 
 from mystic.constraints import as_constraint
 from mystic.penalty import quadratic_inequality
```

### Comparing `mystic-0.4.0/examples2/g10.py` & `mystic-0.4.1/examples2/g10.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     x0,x1,x2,x3,x4,x5,x6,x7 = x
     return x0 + x1 + x2
```

### Comparing `mystic-0.4.0/examples2/g10_alt.py` & `mystic-0.4.1/examples2/g10_alt.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g10 import objective, bounds, xs, ys
 
 from mystic.constraints import as_constraint
 from mystic.penalty import quadratic_inequality
```

### Comparing `mystic-0.4.0/examples2/g11.py` & `mystic-0.4.1/examples2/g11.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     x0,x1 = x
     return x0**2 + (x1 - 1)**2
```

### Comparing `mystic-0.4.0/examples2/g11_alt.py` & `mystic-0.4.1/examples2/g11_alt.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g11 import objective, bounds, xs, xs_, ys
 
 from mystic.penalty import quadratic_equality
 from mystic.constraints import with_penalty
```

### Comparing `mystic-0.4.0/examples2/g12.py` & `mystic-0.4.1/examples2/g12.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     x0,x1,x2 = x
     return 1.0 - 0.01*((x0 - 5)**2 + (x1 - 5)**2 + (x2 - 5)**2)
```

### Comparing `mystic-0.4.0/examples2/g13.py` & `mystic-0.4.1/examples2/g13.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 def objective(x):
     from numpy import exp, product
     return exp(product(x))
```

### Comparing `mystic-0.4.0/examples2/g13_alt.py` & `mystic-0.4.1/examples2/g13_alt.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from g13 import objective, bounds, xs, _xs, x_s, xs_, ys
 
 from mystic.constraints import as_constraint
 from mystic.penalty import quadratic_equality
```

### Comparing `mystic-0.4.0/examples2/hotel_pricing.py` & `mystic-0.4.1/examples2/hotel_pricing.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Problem definition and original response:
 # https://stackoverflow.com/q/48088516/2379433
 # https://stackoverflow.com/a/48494431/2379433
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Maximize:
 
   sum_{i=1 to max i} P_i O_i
```

### Comparing `mystic-0.4.0/examples2/inequalities.py` & `mystic-0.4.1/examples2/inequalities.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2021-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2021-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import mystic.symbolic as ms
 from mystic.constraints import and_ as _and, or_ as _or
 from mystic.coupler import and_, or_
```

### Comparing `mystic-0.4.0/examples2/inout_constrain.py` & `mystic-0.4.1/examples2/inout_constrain.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Problem definition and original response:
 # https://stackoverflow.com/q/67560280/2379433
 # https://stackoverflow.com/a/67571398/2379433
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2021-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2021-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Objective:
     MIN (1500 * x0) + (625 * x1) + (100 * x2)
 
 Constraints:
```

### Comparing `mystic-0.4.0/examples2/integer_inequalities.py` & `mystic-0.4.1/examples2/integer_inequalities.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/env python
 #
 # Problem definition and original response:
 # https://stackoverflow.com/q/59813985/2379433
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 solve:
      a system of inequalities (defined below) with unknowns xi,
      where i = range(1,11)
```

### Comparing `mystic-0.4.0/examples2/integer_programming.py` & `mystic-0.4.1/examples2/integer_programming.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # Example in google/or-tools
 # https://github.com/google/or-tools/blob/master/examples/python/integer_programming.py
 # with Copyright 2010-2013 Google
 # and disclamer as stated at the above reference link.
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
   Integer programming example
 
   Minimize:
             f(x) = x0 + 2*x1
```

### Comparing `mystic-0.4.0/examples2/integer_programming_alt.py` & `mystic-0.4.1/examples2/integer_programming_alt.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # Example in google/or-tools
 # https://github.com/google/or-tools/blob/master/examples/python/integer_programming.py
 # with Copyright 2010-2013 Google
 # and disclamer as stated at the above reference link.
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from integer_programming import objective, bounds, xs, ys
 # bounds = [(0,11)]*2  #XXX: MOD = range(11) instead of LARGE
 
 from mystic.penalty import quadratic_inequality, quadratic_equality
```

### Comparing `mystic-0.4.0/examples2/knapsack.py` & `mystic-0.4.1/examples2/knapsack.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 # 
 # Problem definition and original response:
 # https://stackoverflow.com/q/69655167
 # https://stackoverflow.com/a/69885831
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2021-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2021-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 Solve a bounded knapsack problem.
 
 Maximize:
   profit = SUM_i (quantity_i * profit_i)
```

### Comparing `mystic-0.4.0/examples2/least_square.py` & `mystic-0.4.1/examples2/least_square.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # Example in google/or-tools
 # https://github.com/google/or-tools/blob/master/examples/python/least_square.py
 # with Copyright 2011 Hakan Kjellerstrand hakank@bonetmail.com
 # and disclamer as stated at the above reference link.
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
   Least square optimization problem in Google or-tools.
 
   Solving a fourth grade least square equation.
```

### Comparing `mystic-0.4.0/examples2/lp.py` & `mystic-0.4.1/examples2/lp.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # Problem definition:
 # Example in reference documentation for scipy.optimize.linprog.
 # http://docs.scipy.org/doc/scipy-dev/reference/optimize.linprog-simplex.html
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
     Minimize: f = -1*x[0] + 4*x[1]
 
     Subject to: -3*x[0] + 1*x[1] <= 6
                  1*x[0] + 2*x[1] <= 4
```

### Comparing `mystic-0.4.0/examples2/max_percentle.py` & `mystic-0.4.1/examples2/max_percentle.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Problem definition and original response:
 # https://stackoverflow.com/q/21765794/2379433
 # https://stackoverflow.com/a/43162017/2379433
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 solve:
      max [5th percentile of (ui_T*X), i in 1 to M]
 
 such that:
```

### Comparing `mystic-0.4.0/examples2/no_solution.py` & `mystic-0.4.1/examples2/no_solution.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Problem definition and original response:
 # https://stackoverflow.com/q/12942153/2379433
 # https://stackoverflow.com/a/43173143/2379433
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 Attempt to solve equations with no solution, using unconstrained optimization.
 
 The equations are:
     (x-x1)^2 + (y-y1)^2 - r1^2 = 0
```

### Comparing `mystic-0.4.0/examples2/no_solution2.py` & `mystic-0.4.1/examples2/no_solution2.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Problem definition and original response:
 # https://stackoverflow.com/q/12942153/2379433
 # https://stackoverflow.com/a/43173143/2379433
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 Attempt to solve equations with no solution, using penaltys.
 
 The equations are:
     (x-x1)^2 + (y-y1)^2 - r1^2 = 0
```

### Comparing `mystic-0.4.0/examples2/no_solution3.py` & `mystic-0.4.1/examples2/no_solution3.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Problem definition and original response:
 # https://stackoverflow.com/q/12942153/2379433
 # https://stackoverflow.com/a/43173143/2379433
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 Attempt to solve equations with no solution, with a constrained search.
 
 The equations are:
     (x-x1)^2 + (y-y1)^2 - r1^2 = 0
```

### Comparing `mystic-0.4.0/examples2/olympic.py` & `mystic-0.4.1/examples2/olympic.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # Example in google/or-tools
 # https://github.com/google/or-tools/blob/master/examples/python/olympic.py
 # with Copyright 2010 Hakan Kjellerstrand hakank@bonetmail.com
 # and disclamer as stated at the above reference link.
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
   Olympic puzzle in Google CP Solver.
 
   Prolog benchmark problem
   '''
```

### Comparing `mystic-0.4.0/examples2/optqp.py` & `mystic-0.4.1/examples2/optqp.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # Problem definition:
 # Example in reference documentation for scipy.optimize
 # http://docs.scipy.org/doc/scipy/reference/tutorial/optimize.html
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
     Maximize: f = 2*x[0]*x[1] + 2*x[0] - x[0]**2 - 2*x[1]**2
   
     Subject to:    x[0]**3 - x[1] == 0
                              x[1] >= 1
```

### Comparing `mystic-0.4.0/examples2/optqp_alt.py` & `mystic-0.4.1/examples2/optqp_alt.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # Problem definition:
 # Example in reference documentation for scipy.optimize
 # http://docs.scipy.org/doc/scipy/reference/tutorial/optimize.html
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from optqp import _objective, bounds, xs, ys
 
 from mystic.penalty import quadratic_equality
 from mystic.constraints import with_penalty
```

### Comparing `mystic-0.4.0/examples2/or_constraint.py` & `mystic-0.4.1/examples2/or_constraint.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 find the maximum of y = x0 * f(x1), where:
 
 f(x) = 1 - 2**(-x)/2
 x0 * x1 < 100
```

### Comparing `mystic-0.4.0/examples2/output_constrain.py` & `mystic-0.4.1/examples2/output_constrain.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/env python
 #
 # Problem definition and original response:
 # https://stackoverflow.com/a/71197490/2379433
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Minimize y = f(x):
   where y > g(x)
 
   with f(x) = x0^(sin(x0)) + x1^4 + 6x1^3 - 5x1^2 - 40x1 + 35
```

### Comparing `mystic-0.4.0/examples2/polyfit.py` & `mystic-0.4.1/examples2/polyfit.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
     Fit linear and quadratic polynomial to noisy data:
                y(x) ~ a + b * x   --or--   y(x) ~ a + b * x + c * x**2
 
     where:
```

### Comparing `mystic-0.4.0/examples2/qp_inequality.py` & `mystic-0.4.1/examples2/qp_inequality.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Problem definition and original response:
 # https://stackoverflow.com/a/17025929/2379433
 # https://stackoverflow.com/a/32906273/2379433
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Maximize: f = 2*x[0]*x[1] + 2*x[0] - x[0]**2 - 2*x[1]**2
 
 Subject to: -2*x[0] + 2*x[1] <= -2
              2*x[0] - 4*x[1] <= 0
```

### Comparing `mystic-0.4.0/examples2/root.py` & `mystic-0.4.1/examples2/root.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
     Solve:
                 3*x[0] - cos(x[1]*x[2]) + a = 0
   x[0]**2 - 81*(x[1]+.1)**2 + sin(x[2]) + b = 0
               exp(-x[0]*x[1]) + 20*x[2] + c = 0
```

### Comparing `mystic-0.4.0/examples2/slack_variable.py` & `mystic-0.4.1/examples2/slack_variable.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Minimization with a slack variable and penalty.
 """
 from mystic.solvers import diffev2, fmin_powell
 from mystic.penalty import quadratic_inequality
```

### Comparing `mystic-0.4.0/examples2/slsqp.py` & `mystic-0.4.1/examples2/slsqp.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # Problem definition:
 # Example from stack overflow.
 # http://stackoverflow.com/questions/17009774
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
     Minimize: f = x[0]**2 + 4*x[1]**2 - 32*x[1] + 64
 
     Subject to: x[0] + 1*x[1] <= 7
                -x[0] + 2*x[1] <= 4
```

### Comparing `mystic-0.4.0/examples2/slsqp2.py` & `mystic-0.4.1/examples2/slsqp2.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # Problem definition:
 # Example from stack overflow.
 # http://stackoverflow.com/questions/23476152
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
     Minimize: f = x[0]**2 + x[1]**2
 
     Subject to: x[0]**2 - x[1] <= 0
                -x[0] - x[1]**2 == -2
```

### Comparing `mystic-0.4.0/examples2/slsqp3.py` & `mystic-0.4.1/examples2/slsqp3.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # Problem definition:
 # Example in reference documentation for scipy.optimize.slsqp.
 # http://docs.scipy.org/doc/scipy-0.10.0/reference/tutorial/optimize.html
 # 
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
     Maximize: f = 2*x[0]*x[1] + 2*x[0] - x[0]**2 - 2*x[1]**2
 
     Subject to: -2*x[0] + 2*x[1] <= -2
                  2*x[0] - 4*x[1] <= 0
```

### Comparing `mystic-0.4.0/examples2/spring.py` & `mystic-0.4.1/examples2/spring.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 "a Tension-Compression String"
 
 def objective(x):
     x0,x1,x2 = x
     return x0**2 * x1 * (x2 + 2)
```

### Comparing `mystic-0.4.0/examples2/spring_alt.py` & `mystic-0.4.1/examples2/spring_alt.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 "a Tension-Compression String"
 
 from spring import objective, bounds, xs, ys
 
 from mystic.constraints import as_constraint
```

### Comparing `mystic-0.4.0/examples2/vessel.py` & `mystic-0.4.1/examples2/vessel.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 "Pressure Vessel Design"
 
 def objective(x):
     x0,x1,x2,x3 = x
     return 0.6224*x0*x2*x3 + 1.7781*x1*x2**2 + 3.1661*x0**2*x3 + 19.84*x0**2*x2
```

### Comparing `mystic-0.4.0/examples2/vessel_alt.py` & `mystic-0.4.1/examples2/vessel_alt.py`

 * *Files 5% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 # 
 # Original Matlab code written by A. Hedar (Nov. 23, 2005)
 # http://www-optima.amp.i.kyoto-u.ac.jp/member/student/hedar/Hedar_files/go.htm
 # and ported to Python by Mike McKerns (December 2014)
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 "Pressure Vessel Design"
 
 from vessel import objective, bounds, xs, ys
 
 from mystic.constraints import as_constraint
```

### Comparing `mystic-0.4.0/examples3/DATA/g1.pts` & `mystic-0.4.1/examples3/DATA/g1.pts`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/examples3/DATA/g2.pts` & `mystic-0.4.1/examples3/DATA/g2.pts`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/examples3/README` & `mystic-0.4.1/examples3/README`

 * *Files 6% similar despite different names*

```diff
@@ -17,37 +17,45 @@
   - `pof` denotes a probability of failure calculation
   - `searcher` denotes optimizer-driven discovery of all extrema [DEPRECATED]
   - `sklearn` denotes mystic extensions/interface to sklearn
   - `surface` denotes optimizer-driven surface interpolation [DEPRECATED]
   - `svc` denotes use of support vectors in classification
   - `svr` denotes use of support vectors in regression
   - `sparsity` denotes use of the sparsity sampler
+  - `xrd` denotes the lattice parameter toy model
 
 OUQ calculations:
   - test_*_ub_*: find upper bound on (mean of input/output, or PoF) [examples5]
   - test_error*: find model error
-  - test_expected*: find expected value
-  - test_expected_error* find expected error
+  - test_expect: find expected value
+  - test_expected*: find bound on expected value
+  - test_expected_error* find bound on expected error
   - test_glb*: find greatest lower bound
   - test_gub*: find greatest upper bound
   - test_llb*: find least lower bound
   - test_lub*: find least upper bound
   - test_pof: find probability of failure (PoF)
+  - xrd_design*: find average and bounds on expected value and bounds
 
 Miscellaneous:
- - test_improve_score: workflow to retry/update sklearn estimators
+  - test_cache: demonstrate use and customization of mystic.cache
+  - test_improve_score: workflow to retry/update sklearn estimators
+  - xrd_opt*: find minimum using ensemble optimization
+  - xrd_optML*: find minimum using iterative surrogate improvement
+  - xrd_*_db: inspect expected value databases generated with xrd_design*
 
 External dependencies:
   - examples with "svc", "svr", or "sparsity" in the name require `matplotlib`.
   - examples with "surface" and "searcher" require `scipy` and `matplotlib`.
   - examples with "pandas" require `pandas` and `matplotlib`.
   - otherwise, assume `sklearn` and `matplotlib` are required.
 
-In-place dependencies for ouq*:
+In-place dependencies for ouq* calculations:
   - dataset: extensions on dataset operations
+  - emulators: toy models emulating XRD calculations
   - estimator: high-level OUQ estimator (requires sklearn)
   - interpolator: high-level OUQ interpolator
   - misc: miscellaneous constraints and definitions for OUQ calculation
   - ml: lower-level interface to sklearn, used by estimator
   - noisy: add noise for OUQ noisy model
   - plotter: high-level interface to plotting learned surrogates
   - spec*: same as misc, used in test_*_ub_* OUQ calculations
```

### Comparing `mystic-0.4.0/examples3/collapse_bounds.py` & `mystic-0.4.1/examples3/collapse_bounds.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.solvers import DifferentialEvolutionSolver
 from mystic.models import rosen
 from mystic.tools import solver_bounds
 from mystic.termination import ChangeOverGeneration as COG, Or, CollapseCost
```

### Comparing `mystic-0.4.0/examples3/collapse_measures.py` & `mystic-0.4.1/examples3/collapse_measures.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2010-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 debug = False
 verbose = True
 MINMAX = -1  ## NOTE: sup = maximize = -1; inf = minimize = 1
 #######################################################################
```

### Comparing `mystic-0.4.0/examples3/collapse_solver.py` & `mystic-0.4.1/examples3/collapse_solver.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Lan Huong Nguyen (lanhuong @stanford)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2012-2015 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.termination import Or, CollapseAt, CollapseAs
 from mystic.termination import ChangeOverGeneration as COG
 #from mystic.termination import VTRChangeOverGeneration as COG
```

### Comparing `mystic-0.4.0/examples3/constrained_sklearn.py` & `mystic-0.4.1/examples3/constrained_sklearn.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
   Example applying mystic to sklearn
 
   Use a linear regression to fit sparse data generated from:
             f(x) = a*x3**3 + b*x2**2 + c*x1 + d*x0
```

### Comparing `mystic-0.4.0/examples3/dataset.py` & `mystic-0.4.1/examples3/dataset.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 calculate graphical distance of (interpolated) function from a dataset 
 converters for klepto.archives.dir_archive and mystic.math.legacydata.dataset
 read (params,cost) from LoggingMonitor archive or klepto.archive.dir_archive
 """
@@ -178,16 +178,15 @@
 def read_logfile(filename):
     """read 'parameters' and 'cost' from LoggingMonitor archive
 
     Inputs:
       filename: str path to location of klepto.archives.dir_archive
     """
     from mystic.munge import read_trajectories
-    param, param, cost = read_trajectories(filename)
-    return param, cost
+    return read_trajectories(filename, iter=False)
 
 
 # reader for archive(s)
 def read_archive(filename, axis=None): #NOTE: could return iterators
     """read 'parameters' and 'cost' from klepto.dir_archive
 
     Inputs:
```

### Comparing `mystic-0.4.0/examples3/estimator.py` & `mystic-0.4.1/examples3/estimator.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 a function/surface estimator
   - initalize with x (and z)
   - can downsample and/or add noise
   - learns with sklearn interface (internally)
@@ -179,16 +179,15 @@
           However, if any of the relevant hyperparameters for the estimator
           or the transform are provided, then those parameters will override
           the hyperparameters used in the relevant instance. Hyperparameters
           intended for the tranform should be passed as a dict named 'xfopt',
           while hyperparameters for the estimator can be given directly as
           keyword arguments.
         """
-        import numpy as np
-        #import warnings
+        import warnings
         #from sklearn.exceptions import ConvergenceWarning
         #warnings.simplefilter('ignore', ConvergenceWarning)
         #warnings.simplefilter('ignore', RuntimeWarning)
         _map = kwds.pop('map', map)
         learner = self._configure(kwds)
         axis = self.args.get('axis', None)
         # apply kwds to instantiate transform and estimator
@@ -202,32 +201,32 @@
                     fs = function.__axis__
                     if axis is None:
                         if hasattr(args[0], '__len__'):
                             return tuple(zt(fi(*args)) for fi in fs)
                         return tuple(fi(*args) for fi in fs)
                     return fs[axis](*args)
                 def learn_ax(i):
-                    import numpy as np
+                    import warnings
                     from sklearn.base import clone
                     estimator = clone(learner.estimator)
                     transform = clone(learner.transform)
                     from mystic.math.interpolate import _getaxis
                     from ml import Estimator as Learner
                     func = Learner(estimator, transform)
-                    with np.warnings.catch_warnings(): #FIXME: enable warn=True
-                        np.warnings.filterwarnings('ignore')
+                    with warnings.catch_warnings(): #FIXME: enable warn=True
+                        warnings.filterwarnings('ignore')
                         func = func.train(x, _getaxis(z, i))
                     return func
                 function.__axis__ = list(_map(learn_ax, range(len(z[0]))))
                 return function
         else:
             from mystic.math.interpolate import _getaxis
             z = _getaxis(z, axis)
-        with np.warnings.catch_warnings(): #FIXME: enable warn=True
-            np.warnings.filterwarnings('ignore')
+        with warnings.catch_warnings(): #FIXME: enable warn=True
+            warnings.filterwarnings('ignore')
             function = learner.train(x, z)
         function.__axis__ = axis
         return function
 
     def Train(self, **kwds): #XXX: better take a strategy?
         """train data (x,z) to generate response function z=f(*x)
```

### Comparing `mystic-0.4.0/examples3/hyperopt_sklearn.py` & `mystic-0.4.1/examples3/hyperopt_sklearn.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 "Hyperparameter optimization"
 
 from sklearn.svm import SVR
 from sklearn.datasets import load_iris
 from sklearn.model_selection import train_test_split as tts
```

### Comparing `mystic-0.4.0/examples3/interpolator.py` & `mystic-0.4.1/examples3/interpolator.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 a function/surface interpolator
   - initalize with x (and z)
   - can downsample and/or add noise
   - interpolates with "interp.interp"
@@ -140,18 +140,18 @@
           'nearest','cubic','inverse','gaussian','quintic','thin_plate').
 
         NOTE:
           additional keyword arguments (epsilon, smooth, norm) are avaiable
           for use with a Rbf interpolator. See mystic.math.interpolate.Rbf
           for more details.
         """
-        import numpy as np
+        import warnings
         from mystic.math.interpolate import interpf
-        with np.warnings.catch_warnings():
-            np.warnings.filterwarnings('ignore')
+        with warnings.catch_warnings():
+            warnings.filterwarnings('ignore')
             f = interpf(x, z, **kwds)
         return f
 
 
     def Interpolate(self, **kwds): #XXX: better take a strategy?
         """interpolate data (x,z) to generate response function z=f(*x)
```

### Comparing `mystic-0.4.0/examples3/misc.py` & `mystic-0.4.1/examples3/misc.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 misc user-defined items (solver configuration, moment constraints)
 """
 from mystic.solvers import DifferentialEvolutionSolver2
 from mystic.monitors import VerboseMonitor, Monitor
@@ -23,14 +23,16 @@
              map=None, # don't use SetMapper
              stepmon=VerboseMonitor(1, label='output'), # monitor config
              #evalmon=Monitor(), # monitor config (re-initialized in solve)
              # kwds to pass directly to Solve(objective, **opt)
              opts=opts,
             )
 
+# kwds for sampling
+kwds = dict(npts=500, ipts=None, itol=1e-8, iter=5)
 
 from mystic.math.discrete import product_measure
 from mystic.math import almostEqual as almost
 from mystic.constraints import and_, integers
 from mystic.coupler import outer, additive
 
 # lower and upper bound for parameters and weights
```

### Comparing `mystic-0.4.0/examples3/ml.py` & `mystic-0.4.1/examples3/ml.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2019-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2019-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 mahine learning containers and assorted tools
 """
 
 import numpy as np
```

### Comparing `mystic-0.4.0/examples3/noisy.py` & `mystic-0.4.1/examples3/noisy.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 functions to add noise to function inputs or outputs
 """
 
 import numpy as np
```

### Comparing `mystic-0.4.0/examples3/ouq_.py` & `mystic-0.4.1/examples3/ouq_.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 OUQ classes for calculating bounds on statistical quantities
 """
 from mystic.math.discrete import product_measure
 from ouq import BaseOUQ
```

### Comparing `mystic-0.4.0/examples3/ouq_models.py` & `mystic-0.4.1/examples3/ouq_models.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 model objects (and helper functions) to be used with OUQ classes
 '''
 #FIXME: hardwired to multivalue function
 #FIXME: dict_archive('truth', cached=False) does not cache (is empty)
```

### Comparing `mystic-0.4.0/examples3/plotter.py` & `mystic-0.4.1/examples3/plotter.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 plotter for data (x,z) and response surface function(*x)
   - initalize with x and z (and function)
   - interpolate if function is not provided
   - can downsample
```

### Comparing `mystic-0.4.0/examples3/sampler_pandas.py` & `mystic-0.4.1/examples3/sampler_pandas.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2021-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2021-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from ouq_models import WrapModel
 from mystic.models import rosen
 
 # generate a sampled dataset for the model
```

### Comparing `mystic-0.4.0/examples3/spec3D.py` & `mystic-0.4.1/examples3/spec3D.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 misc user-defined items (solver configuration, moment constraints)
 """
 from mystic.solvers import DifferentialEvolutionSolver2
 from mystic.monitors import VerboseMonitor, Monitor
```

### Comparing `mystic-0.4.0/examples3/spec5D.py` & `mystic-0.4.1/examples3/spec5D.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 misc user-defined items (solver configuration, moment constraints)
 """
 from mystic.solvers import DifferentialEvolutionSolver2
 from mystic.monitors import VerboseMonitor, Monitor
```

### Comparing `mystic-0.4.0/examples3/surface.py` & `mystic-0.4.1/examples3/surface.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2010-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 an interpolator
   - initalize with objective f(x) (and 'Sampler' object)
   - can attach a monitor and/or archiver
   - can sample points (using the Sampler)
```

### Comparing `mystic-0.4.0/examples3/surrogate.py` & `mystic-0.4.1/examples3/surrogate.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2015 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 """Original matlab code:
 
 function A=marc_surr(x)
 h=x(1)*25.4*10^(-3);
```

### Comparing `mystic-0.4.0/examples3/test_3D_ub_c0mean.py` & `mystic-0.4.1/examples3/test_3D_ub_c0mean.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 calculate upper bound on mean value of 0th input
 
 Test function is y = F(x), where:
   F is defined in surrogate.py
```

### Comparing `mystic-0.4.0/examples3/test_3D_ub_mean.py` & `mystic-0.4.1/examples3/test_3D_ub_mean.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 # 
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 calculate upper bound on expected value
 
 Test function is y = F(x), where:
   F is defined in surrogate.py
```

### Comparing `mystic-0.4.0/examples3/test_3D_ub_pof.py` & `mystic-0.4.1/examples3/test_3D_ub_pof.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 # 
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 calculate upper bound on probability of failure
 
 Test function is y = F(x), where:
   F is defined in surrogate.py
```

### Comparing `mystic-0.4.0/examples3/test_5D_ub_c0mean.py` & `mystic-0.4.1/examples3/test_5D_ub_c0mean.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 calculate upper bound on mean value of 0th input
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_5D_ub_mean.py` & `mystic-0.4.1/examples3/test_5D_ub_mean.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 calculate upper bound on expected value
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_error.py` & `mystic-0.4.1/examples3/test_error.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate error for actively learned/interpolated models
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_expected.py` & `mystic-0.4.1/examples3/test_expected.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 calculate upper bound on expected value
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
@@ -37,27 +37,29 @@
     #from toys import function5x3 as toy; nx = 5; ny = 3
     #from toys import cost5x1 as toy; nx = 5; ny = 1
     #from toys import function5x1 as toy; nx = 5; ny = 1
     #from toys import cost5 as toy; nx = 5; ny = None
     from toys import function5 as toy; nx = 5; ny = None
     Ns = 25
 
+    # build a model representing 'truth'
+    nargs = dict(nx=nx, ny=ny, rnd=False)
+    model = WrapModel('model', toy, **nargs)
+
+    # set the bounds
+    bnd = MeasureBounds(xlb, xub, n=npts, wlb=wlb, wub=wub)
+
     try: # parallel maps
         from pathos.maps import Map
         from pathos.pools import ProcessPool, ThreadPool, _ThreadPool
         pmap = Map(ProcessPool) if Ns else Map() # for sampling
         param['map'] = Map(ThreadPool) # for objective
         if ny: param['axmap'] = Map(_ThreadPool, join=True) # for multi-axis
     except ImportError:
         pmap = None
 
-    # build a model representing 'truth'
-    nargs = dict(nx=nx, ny=ny, rnd=False)
-    model = WrapModel('model', toy, **nargs)
-
     # calculate upper bound on expected value, where x[0] has uncertainty
-    bnd = MeasureBounds((0,1,0,0,0),(1,10,10,10,10), n=npts, wlb=wlb, wub=wub)
     b = ExpectedValue(model, bnd, constraint=scons, cvalid=is_cons, samples=Ns, map=pmap)
     b.upper_bound(axis=None, **param)
     print("upper bound per axis:")
     for axis,solver in b._upper.items():
         print("%s: %s @ %s" % (axis, -solver.bestEnergy, solver.bestSolution))
```

### Comparing `mystic-0.4.0/examples3/test_expected_error1.py` & `mystic-0.4.1/examples3/test_expected_error1.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate lower and upper bound on expected Error on |truth - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_expected_error1GP.py` & `mystic-0.4.1/examples3/test_expected_error1GP.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate lower and upper bound on expected Error on |truth - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_expected_error1ML.py` & `mystic-0.4.1/examples3/test_expected_error1ML.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate lower and upper bound on expected Error on |truth - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_expected_error2.py` & `mystic-0.4.1/examples3/test_expected_error2.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate lower and upper bound on expected Error on |model - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_expected_error2GP.py` & `mystic-0.4.1/examples3/test_expected_error2GP.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate lower and upper bound on expected Error on |model - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_expected_error2ML.py` & `mystic-0.4.1/examples3/test_expected_error2ML.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate lower and upper bound on expected Error on |model - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_expected_error3.py` & `mystic-0.4.1/examples3/test_expected_error3.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate lower and upper bound on expected Error on |truth - model|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_glb_expected.py` & `mystic-0.4.1/examples3/test_glb_expected.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for greatest lower bound of ExpectedValue on model
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_gub_expected.py` & `mystic-0.4.1/examples3/test_gub_expected.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for greatest upper bound of ExpectedValue on model
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_improve_score.py` & `mystic-0.4.1/examples3/test_improve_score.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 demonstrate iterative improvement of R^2 score for an ANN model
 '''
 from ml import *
```

### Comparing `mystic-0.4.0/examples3/test_llb_expected.py` & `mystic-0.4.1/examples3/test_llb_expected.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least lower bound of ExpectedValue on model
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_lub_expected.py` & `mystic-0.4.1/examples3/test_lub_expected.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least upper bound of ExpectedValue on model
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_lub_expected0.py` & `mystic-0.4.1/examples3/test_lub_expected0.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least upper bound of ExpectedValue on model
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_lub_expected_error0.py` & `mystic-0.4.1/examples3/test_lub_expected_error0.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least upper bound of Error on |truth - model|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_lub_expected_error1.py` & `mystic-0.4.1/examples3/test_lub_expected_error1.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least upper bound of Error on |truth - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_lub_expected_error1GP.py` & `mystic-0.4.1/examples3/test_lub_expected_error1GP.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least upper bound of Error on |truth - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_lub_expected_error1ML.py` & `mystic-0.4.1/examples3/test_lub_expected_error1ML.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least upper bound of Error on |truth - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_lub_expected_error2a.py` & `mystic-0.4.1/examples3/test_lub_expected_error2a.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least upper bound of Error on |model - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_lub_expected_error2b.py` & `mystic-0.4.1/examples3/test_lub_expected_error2b.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least upper bound of Error on |model - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_lub_expected_error2bGP.py` & `mystic-0.4.1/examples3/test_lub_expected_error2bGP.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least upper bound of Error on |model - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_lub_expected_error2bML.py` & `mystic-0.4.1/examples3/test_lub_expected_error2bML.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least upper bound of Error on |model - surrogate|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_lub_expected_error3.py` & `mystic-0.4.1/examples3/test_lub_expected_error3.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 hyperparameter tuning for least upper bound of Error on |truth - model|
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_pof.py` & `mystic-0.4.1/examples3/test_pof.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 calculate upper bound on probability of failure
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples3/test_searcher.py` & `mystic-0.4.1/examples3/test_searcher.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2010-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 example of using a global searcher to find all extrema (and rough interpolation)
 """
 
 from mystic.search import Searcher
```

### Comparing `mystic-0.4.0/examples3/test_searcher2.py` & `mystic-0.4.1/examples3/test_searcher2.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2010-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 example of using a global searcher for interpolation
 """
 
 from mystic.search import Searcher
```

### Comparing `mystic-0.4.0/examples3/test_sparsity.py` & `mystic-0.4.1/examples3/test_sparsity.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2019-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2019-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 finds npts that are rtol dist away from legacy data
 """
 #XXX: could make similar that uses partitioning (based on monitor.y) ?
 #XXX: could make similar that first samples, then uses hole-filling ?
```

### Comparing `mystic-0.4.0/examples3/test_surface.py` & `mystic-0.4.1/examples3/test_surface.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2010-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 an example of using an interpolator within a surface object
 """ #XXX: use interpolator, plotter, and sampler (instead of Surface)?
 
 from surface import Surface
```

### Comparing `mystic-0.4.0/examples3/test_svc1.py` & `mystic-0.4.1/examples3/test_svc1.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Support Vector Classification. Example 1
 """
 
 from numpy import *
```

### Comparing `mystic-0.4.0/examples3/test_svc2.py` & `mystic-0.4.1/examples3/test_svc2.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Support Vector Classification. Example 2.
 
 using meristem data from data files
 """
```

### Comparing `mystic-0.4.0/examples3/test_svr1.py` & `mystic-0.4.1/examples3/test_svr1.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Support Vector Regression. Example 1
 
 Minimize:
     0.5*x'Qx + b'*x
```

### Comparing `mystic-0.4.0/examples3/test_svr2.py` & `mystic-0.4.1/examples3/test_svr2.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Support Vector Regression. Example 2
 """
 #FIXME: works if x is a 1D array, should allow x as a 2D array
 from numpy import *
```

### Comparing `mystic-0.4.0/examples3/toys.py` & `mystic-0.4.1/examples3/toys.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 test functions, including those with multivalued returns and the axis keyword
 """
 
 def function5x3(x):
```

### Comparing `mystic-0.4.0/examples4/MM2_surrogate_diam_batchgrid.py` & `mystic-0.4.1/examples4/MM2_surrogate_diam_batchgrid.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use fmin solver
 #######################################################################
```

### Comparing `mystic-0.4.0/examples4/MM_surrogate_diam.py` & `mystic-0.4.1/examples4/MM_surrogate_diam.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use DE solver, use mpi, F-F' calculation
 #######################################################################
```

### Comparing `mystic-0.4.0/examples4/MPI2_surrogate_diam_batchgrid.py` & `mystic-0.4.1/examples4/MPI2_surrogate_diam_batchgrid.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use fmin solver
 #######################################################################
```

### Comparing `mystic-0.4.0/examples4/MPI_surrogate_diam.py` & `mystic-0.4.1/examples4/MPI_surrogate_diam.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use DE solver, use mpi, F-F' calculation
 #######################################################################
```

### Comparing `mystic-0.4.0/examples4/MPI_surrogate_diam_batchgrid.py` & `mystic-0.4.1/examples4/MPI_surrogate_diam_batchgrid.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.math.grid import gridpts
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
```

### Comparing `mystic-0.4.0/examples4/MPI_surrogate_diam_scatter.py` & `mystic-0.4.1/examples4/MPI_surrogate_diam_scatter.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.math.grid import samplepts
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
```

### Comparing `mystic-0.4.0/examples4/MSUB_surrogate_diam_batchgrid.py` & `mystic-0.4.1/examples4/MSUB_surrogate_diam_batchgrid.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.math.grid import gridpts
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
```

### Comparing `mystic-0.4.0/examples4/PP_surrogate_diam.py` & `mystic-0.4.1/examples4/PP_surrogate_diam.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use DE solver, use mpi, F-F' calculation
 #######################################################################
```

### Comparing `mystic-0.4.0/examples4/QSUB2_surrogate_diam_batchgrid.py` & `mystic-0.4.1/examples4/QSUB2_surrogate_diam_batchgrid.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use fmin solver
 #######################################################################
```

### Comparing `mystic-0.4.0/examples4/QSUB_surrogate_diam_batchgrid.py` & `mystic-0.4.1/examples4/QSUB_surrogate_diam_batchgrid.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.math.grid import gridpts
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
```

### Comparing `mystic-0.4.0/examples4/README` & `mystic-0.4.1/examples4/README`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/examples4/TEST.py` & `mystic-0.4.1/examples4/TEST.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use DE solver, don't use mpi, F-F' calculation
 # (similar to concentration.in)
```

### Comparing `mystic-0.4.0/examples4/TEST2.py` & `mystic-0.4.1/examples4/TEST2.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use DE solver, don't use mpi, F-F' calculation
 # (similar to concentration.in)
```

### Comparing `mystic-0.4.0/examples4/TEST3.py` & `mystic-0.4.1/examples4/TEST3.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use DE solver, don't use mpi, F-F' calculation
 # (similar to concentration.in)
```

### Comparing `mystic-0.4.0/examples4/TEST3b.py` & `mystic-0.4.1/examples4/TEST3b.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use DE solver, don't use mpi, F-F' calculation
 # (similar to concentration.in)
```

### Comparing `mystic-0.4.0/examples4/TEST_surrogate_McD.py` & `mystic-0.4.1/examples4/TEST_surrogate_McD.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use DE solver, don't use mpi, F-F' calculation
 # (similar to concentration.in)
```

### Comparing `mystic-0.4.0/examples4/TEST_surrogate_cut.py` & `mystic-0.4.1/examples4/TEST_surrogate_cut.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 DEBUG = False
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use DE solver, don't use mpi, F-F' calculation
```

### Comparing `mystic-0.4.0/examples4/TEST_surrogate_diam.py` & `mystic-0.4.1/examples4/TEST_surrogate_diam.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
 # hard-wired: use DE solver, don't use mpi, F-F' calculation
 #######################################################################
```

### Comparing `mystic-0.4.0/examples4/TEST_surrogate_diam_batchgrid.py` & `mystic-0.4.1/examples4/TEST_surrogate_diam_batchgrid.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.math.grid import gridpts
 
 
 #######################################################################
```

### Comparing `mystic-0.4.0/examples4/TEST_surrogate_diam_scatter.py` & `mystic-0.4.1/examples4/TEST_surrogate_diam_scatter.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.math.grid import samplepts
 
 
 #######################################################################
```

### Comparing `mystic-0.4.0/examples4/TEST_surrogate_samples.py` & `mystic-0.4.1/examples4/TEST_surrogate_samples.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 DEBUG = False
 PER_AI = True # if True, generate random_samples on each Ai
 MCZERO = False # if True, McD[i] == 0 when STATUS[i] = SUCCESS
 #######################################################################
```

### Comparing `mystic-0.4.0/examples4/TEST_surrogate_smartcut.py` & `mystic-0.4.1/examples4/TEST_surrogate_smartcut.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 DEBUG = True
 MCZERO = True # if True, McD[i] == 0 when STATUS[i] = SUCCESS
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
```

### Comparing `mystic-0.4.0/examples4/pool_helper.py` & `mystic-0.4.1/examples4/pool_helper.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 # MPI config
 #nnodes = 4   # = npop
 nnodes = '4:core4:ppn=1'   # = npop
```

### Comparing `mystic-0.4.0/examples4/surrogate.py` & `mystic-0.4.1/examples4/surrogate.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 """Original matlab code:
 
 function A=marc_surr(x)
 h=x(1)*25.4*10^(-3);
```

### Comparing `mystic-0.4.0/examples5/TEST4d_OUQ_surrogate_diam.py` & `mystic-0.4.1/examples5/TEST4d_OUQ_surrogate_diam.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2010-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 debug = False
 MINMAX = -1  ## NOTE: sup = maximize = -1; inf = minimize = 1
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
```

### Comparing `mystic-0.4.0/examples5/TEST_OUQ_surrogate_diam.py` & `mystic-0.4.1/examples5/TEST_OUQ_surrogate_diam.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2010-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 debug = False
 MINMAX = -1  ## NOTE: sup = maximize = -1; inf = minimize = 1
 #######################################################################
 # scaling and mpi info; also optimizer configuration parameters
```

### Comparing `mystic-0.4.0/examples5/surrogate.py` & `mystic-0.4.1/examples5/surrogate.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2015 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 """Original matlab code:
 
 function A=marc_surr(x)
 h=x(1)*25.4*10^(-3);
```

### Comparing `mystic-0.4.0/examples5/test_3D_ub_c0mean.py` & `mystic-0.4.1/examples5/test_3D_ub_c0mean.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate upper bound on mean value of 0th input
 
 Test function is y = F(x), where:
   F is defined in surrogate.py
```

### Comparing `mystic-0.4.0/examples5/test_3D_ub_mean.py` & `mystic-0.4.1/examples5/test_3D_ub_mean.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate upper bound on expected value
 
 Test function is y = F(x), where:
   F is defined in surrogate.py
```

### Comparing `mystic-0.4.0/examples5/test_3D_ub_pof.py` & `mystic-0.4.1/examples5/test_3D_ub_pof.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate upper bound on probability of failure
 
 Test function is y = F(x), where:
   F is defined in surrogate.py
```

### Comparing `mystic-0.4.0/examples5/test_5D_ub_c0mean.py` & `mystic-0.4.1/examples5/test_5D_ub_c0mean.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate upper bound on mean value of 0th input
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples5/test_5D_ub_mean.py` & `mystic-0.4.1/examples5/test_5D_ub_mean.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 calculate upper bound on expected value
 
 Test function is y = F(x), where:
   y0 = x0 + x1 * | x2 * x3**2 - (x4 / x1)**2 |**.5
```

### Comparing `mystic-0.4.0/examples5/toys.py` & `mystic-0.4.1/examples5/toys.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 test functions, including those with multivalued returns and the axis keyword
 """
 
 def function5x3(x):
```

### Comparing `mystic-0.4.0/mystic/__info__.py` & `mystic-0.4.1/mystic/__info__.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
----------------------------------------------------------------------------------
-mystic: highly-constrained non-convex optimization and uncertainty quantification
----------------------------------------------------------------------------------
+--------------------------------------------------------------------------------------
+mystic: constrained nonlinear optimization for scientific machine learning, UQ, and AI
+--------------------------------------------------------------------------------------
 
 About Mystic
 ============
 
 The ``mystic`` framework provides a collection of optimization algorithms
 and tools that allows the user to more robustly (and easily) solve hard
 optimization problems. All optimization algorithms included in ``mystic``
@@ -30,23 +30,40 @@
 be easily swapped without the user having to write any new code. ``mystic``
 solvers all conform to a solver API, thus also have common method calls
 to configure and launch an optimization job. For more details, see
 ``mystic.abstract_solver``. The API also makes it easy to bind a favorite
 3rd party solver into the ``mystic`` framework.
 
 Optimization algorithms in ``mystic`` can accept parameter constraints,
-either in the form of penaties (which "penalize" regions of solution
-space that violate the constraints), or as constraints (which "constrain" 
-the solver to only search in regions of solution space where the
-constraints are respected), or both. ``mystic`` provides a large 
-selection of constraints, including probabistic and dimensionally
+as "soft constraints" (i.e. ``penalties``, which "penalize" regions of
+solution space that violate the constraints), or as "hard constraints"
+(i.e. ``constraints``, which constrain the solver to only search in regions
+of space where the constraints are respected), or both. ``mystic`` provides
+a large selection of constraints, including probabistic and dimensionally
 reducing constraints. By providing a robust interface designed to
 enable the user to easily configure and control solvers, ``mystic``
 greatly reduces the barrier to solving hard optimization problems.
 
+Sampling, interpolation, and statistics in ``mystic`` are all designed
+to seamlessly couple with constrained optimization to facilitate
+scientific machine learning, uncertainty quantification, adaptive
+sampling, nonlinear interpolation, and artificial intelligence.
+``mystic`` can convert systems of equalities and inequalities to
+hard or soft constraints using methods in ``mystic.symbolic``.
+With ``mystic.constraints.vectorize``, constraints can be converted
+to kernel transforms for use in machine learning. Similarly, ``mystic``
+provides tools for accurately producing emulators on an irregular grid
+using ``mystic.math.interpolate``, which includes methods for solving
+for gradients and Hessians. ``mystic.samplers`` use optimizers to
+drive adaptive sampling toward the first and second order critical points
+of the response surface, yielding highly-informative training data sets
+and ensuring emulator accuracy. ``mystic.math.discrete`` defines
+constrained discrete probability measures, which can be used in
+constrained statistical optimization and learning.
+
 ``mystic`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/mystic/issues, with a legacy list maintained at https://uqfoundation.github.io/project/mystic/query.
 
 
 Major Features
 ==============
 
@@ -91,15 +108,15 @@
 Installation
 ============
 
 ``mystic`` can be installed with ``pip``::
 
     $ pip install mystic
 
-To include optional scientific python support, with ``scipy``, install::
+To include optional scientific Python support, with ``scipy``, install::
 
     $ pip install mystic[math]
 
 To include optional plotting support with ``matplotlib``, install::
 
     $ pip install mystic[plotting]
 
@@ -115,91 +132,90 @@
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
     - ``cython``, **>=0.29.30**
     - ``numpy``, **>=1.0**
     - ``sympy``, **>=0.6.7**
     - ``mpmath``, **>=0.19**
-    - ``dill``, **>=0.3.6**
-    - ``klepto``, **>=0.2.3**
+    - ``dill``, **>=0.3.7**
+    - ``klepto``, **>=0.2.4**
 
 Optional requirements:
 
     - ``matplotlib``, **>=0.91**
     - ``scipy``, **>=0.6.0**
-    - ``pathos``, **>=0.3.0**
-    - ``pyina``, **>=0.2.6**
+    - ``pathos``, **>=0.3.1**
+    - ``pyina``, **>=0.2.8**
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://mystic.rtfd.io. Also see ``mystic.tests`` for a set of scripts that
 demonstrate several of the many features of the ``mystic`` framework.
 You can run the test suite with ``python -m mystic.tests``. There are
 several plotting scripts that are installed with ``mystic``, primary of which
 are ``mystic_log_reader`` (also available with ``python -m mystic``) and the
 ``mystic_model_plotter`` (also available with ``python -m mystic.models``).
 There are several other plotting scripts that come with ``mystic``, and they
-are detailed elsewhere in the documentation.  See ``mystic.examples`` for
-examples that demonstrate the basic use cases for configuration and launching
-of optimization jobs using one of the sample models provided in
-``mystic.models``. Many of the included examples are standard optimization
-test problems. The use of constraints and penalties are detailed in
-``mystic.examples2``, while more advanced features leveraging ensemble solvers
-and dimensional collapse are found in ``mystic.examples3``. The scripts in
-``mystic.examples4`` demonstrate leveraging ``pathos`` for parallel computing,
-as well as demonstrate some auto-partitioning schemes. ``mystic`` has the
-ability to work in product measure space, and the scripts in
-``mystic.examples5`` show to work with product measures.  The source code is
-generally well documented, so further questions may be resolved by inspecting
-the code itself.  Please feel free to submit a ticket on github, or ask a
-question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``mystic`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+are detailed elsewhere in the documentation.  See https://github.com/uqfoundation/mystic/tree/master/examples for examples that demonstrate the basic use
+cases for configuration and launching of optimization jobs using one of the
+sample models provided in ``mystic.models``. Many of the included examples
+are standard optimization test problems. The use of constraints and penalties
+are detailed in https://github.com/uqfoundation/mystic/tree/master/examples2 while more advanced features leveraging ensemble solvers, machine learning,
+uncertainty quantification, and dimensional collapse are found in https://github.com/uqfoundation/mystic/tree/master/examples3. The scripts in https://github.com/uqfoundation/mystic/tree/master/examples4 demonstrate leveraging ``pathos``
+for parallel computing, as well as demonstrate some auto-partitioning schemes.
+``mystic`` has the ability to work in product measure space, and the scripts in
+https://github.com/uqfoundation/mystic/tree/master/examples5 show how to work
+with product measures at a low level. The source code is generally well
+documented, so further questions may be resolved by inspecting the code itself.
+Please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``mystic`` in your work, please send an email (to **mmckerns at uqfoundation
+dot org**).
 
 Instructions on building a new model are in ``mystic.models.abstract_model``.
 ``mystic`` provides base classes for two types of models:
 
     - ``AbstractFunction``   [evaluates ``f(x)`` for given evaluation points ``x``]
     - ``AbstractModel``      [generates ``f(x,p)`` for given coefficients ``p``]
 
 ``mystic`` also provides some convienence functions to help you build a
 model instance and a cost function instance on-the-fly. For more
 information, see ``mystic.forward_model``.  It is, however, not necessary
 to use base classes or the model builder in building your own model or
-cost function, as any standard python function can be used as long as it
+cost function, as any standard Python function can be used as long as it
 meets the basic ``AbstractFunction`` interface of ``cost = f(x)``.
 
 All ``mystic`` solvers are highly configurable, and provide a robust set of
 methods to help customize the solver for your particular optimization
 problem. For each solver, a minimal (``scipy.optimize``) interface is also
 provided for users who prefer to configure and launch their solvers as a
 single function call. For more information, see ``mystic.abstract_solver``
 for the solver API, and each of the individual solvers for their minimal
 functional interface.
 
 ``mystic`` enables solvers to use parallel computing whenever the user provides
-a replacement for the (serial) python ``map`` function.  ``mystic`` includes a
+a replacement for the (serial) Python ``map`` function.  ``mystic`` includes a
 sample ``map`` in ``mystic.python_map`` that mirrors the behavior of the
-built-in python ``map``, and a ``pool`` in ``mystic.pools`` that provides ``map``
+built-in Python ``map``, and a ``pool`` in ``mystic.pools`` that provides ``map``
 functions using the ``pathos`` (i.e. ``multiprocessing``) interface. ``mystic``
 solvers are designed to utilize distributed and parallel tools provided by
 the ``pathos`` package. For more information, see ``mystic.abstract_map_solver``,
 ``mystic.abstract_ensemble_solver``, and the ``pathos`` documentation at
 http://pathos.rtfd.io.
 
 Important classes and functions are found here:
 
     - ``mystic.solvers``                  [solver optimization algorithms]
     - ``mystic.termination``              [solver termination conditions]
     - ``mystic.strategy``                 [solver population mutation strategies]
     - ``mystic.monitors``                 [optimization monitors]
-    - ``mystic.symbolic``                 [symbolic math in constaints]
+    - ``mystic.symbolic``                 [symbolic math in constraints]
     - ``mystic.constraints``              [constraints functions]
     - ``mystic.penalty``                  [penalty functions]
     - ``mystic.collapse``                 [checks for dimensional collapse]
     - ``mystic.coupler``                  [decorators for function coupling]
     - ``mystic.pools``                    [parallel worker pool interface]
     - ``mystic.munge``                    [file readers and writers]
     - ``mystic.scripts``                  [model and convergence plotting]
@@ -235,14 +251,15 @@
     - ``mystic.models.abstract_model``    [the model API definition]
 
 ``mystic`` also provides several convience scripts that are used to visualize
 models, convergence, and support on the hypercube. These scripts are installed
 to a directory on the user's ``$PATH``, and thus can be run from anywhere:
 
     - ``mystic_log_reader``               [parameter and cost convergence]
+    - ``mystic_log_converter``            [logfile format converter]
     - ``mystic_collapse_plotter``         [convergence and dimensional collapse]
     - ``mystic_model_plotter``            [model surfaces and solver trajectory]
     - ``support_convergence``             [convergence plots for measures]
     - ``support_hypercube``               [parameter support on the hypercube]
     - ``support_hypercube_measures``      [measure support on the hypercube]
     - ``support_hypercube_scenario``      [scenario support on the hypercube]
 
@@ -266,36 +283,36 @@
     https://uqfoundation.github.io/project/mystic
 
 Please see https://uqfoundation.github.io/project/mystic or
 http://arxiv.org/pdf/1202.1056 for further information.
 
 '''
 
-__version__ = '0.4.0'
+__version__ = '0.4.1'
 __author__ = 'Mike McKerns'
 
 __license__ = '''
 Copyright (c) 2004-2016 California Institute of Technology.
-Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
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

### Comparing `mystic-0.4.0/mystic/__init__.py` & `mystic-0.4.1/mystic/__init__.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 # author, version, license, and long description
 try: # the package is installed
     from .__info__ import __version__, __author__, __doc__, __license__
 except: # pragma: no cover
@@ -23,15 +23,16 @@
     __license__ = "\n%s" % __license__
     __doc__ = get_readme_as_rst(os.path.join(parent, 'README.md'))
     del os, sys, parent, get_license_text, get_readme_as_rst
 
 
 __all__ = ['solvers','termination','strategy','munge','tools','support', \
            'penalty','coupler','symbolic','monitors','license','citation', \
-           'constraints','model_plotter','log_reader','collapse_plotter']
+           'constraints','model_plotter','log_reader','collapse_plotter', \
+           'log_converter']
 
 # solvers
 import mystic.solvers as solvers
 
 # strategies, termination conditions
 import mystic.termination as termination
 import mystic.strategy as strategy
@@ -44,15 +45,15 @@
 
 # monitors, function wrappers, and other tools
 import mystic.monitors as monitors
 import mystic.munge as munge
 import mystic.tools as tools
 
 # scripts
-from mystic.scripts import model_plotter, log_reader, collapse_plotter
+from mystic.scripts import model_plotter, log_reader, collapse_plotter, log_converter
 import mystic.support as support
 
 # backward compatibility
 from mystic.tools import *
 
 
 def license():
```

### Comparing `mystic-0.4.0/mystic/_counter.py` & `mystic-0.4.1/mystic/_counter.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 # Inspired by https://stackoverflow.com/a/21681534
 """
 a multiprocessing-friendly counter
 """
```

### Comparing `mystic-0.4.0/mystic/_genSow.py` & `mystic-0.4.1/mystic/_genSow.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """a helper class for the CustomMonitor function"""
 
 class genSow(object):
     """
 a configurable Monitor generator
```

### Comparing `mystic-0.4.0/mystic/_scipy060optimize.py` & `mystic-0.4.1/mystic/_scipy060optimize.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 # You may copy and use this module as you see fit with no
 # guarantee implied provided you keep this notice in all copies.
 # *****END NOTICE************
 #
 # Forked by: Mike McKerns (February 2009)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """local copy of scipy.optimize"""
 
 #__all__ = ['fmin', 'fmin_powell', 'fmin_ncg', 'fmin_cg', 'fmin_bfgs',
 #           'fminbound','brent', 'golden','bracket','rosen','rosen_der',
 #           'rosen_hess', 'rosen_hess_prod', 'brute', 'approx_fprime',
@@ -283,15 +283,15 @@
     elif iterations >= maxiter:
         warnflag = 2
         if disp:
             print("Warning: Maximum number of iterations has been exceeded")
     else:
         if disp:
             print("Optimization terminated successfully.")
-            print("         Current function value: %f" % fval)
+            print("         Current function value: %s" % fval)
             print("         Iterations: %d" % iterations)
             print("         Function evaluations: %d" % fcalls[0])
 
 
     if full_output:
         retlist = x, fval, iterations, fcalls[0], warnflag
         if retall:
@@ -776,31 +776,31 @@
                  * sk[numpy.newaxis,:]
 
     if disp or full_output:
         fval = old_fval
     if warnflag == 2:
         if disp:
             print("Warning: Desired error not necessarily achieved due to precision loss")
-            print("         Current function value: %f" % fval)
+            print("         Current function value: %s" % fval)
             print("         Iterations: %d" % k)
             print("         Function evaluations: %d" % func_calls[0])
             print("         Gradient evaluations: %d" % grad_calls[0])
 
     elif k >= maxiter:
         warnflag = 1
         if disp:
             print("Warning: Maximum number of iterations has been exceeded")
-            print("         Current function value: %f" % fval)
+            print("         Current function value: %s" % fval)
             print("         Iterations: %d" % k)
             print("         Function evaluations: %d" % func_calls[0])
             print("         Gradient evaluations: %d" % grad_calls[0])
     else:
         if disp:
             print("Optimization terminated successfully.")
-            print("         Current function value: %f" % fval)
+            print("         Current function value: %s" % fval)
             print("         Iterations: %d" % k)
             print("         Function evaluations: %d" % func_calls[0])
             print("         Gradient evaluations: %d" % grad_calls[0])
 
     if full_output:
         retlist = xk, fval, gfk, Hk, func_calls[0], grad_calls[0], warnflag
         if retall:
@@ -944,31 +944,31 @@
 
 
     if disp or full_output:
         fval = old_fval
     if warnflag == 2:
         if disp:
             print("Warning: Desired error not necessarily achieved due to precision loss")
-            print("         Current function value: %f" % fval)
+            print("         Current function value: %s" % fval)
             print("         Iterations: %d" % k)
             print("         Function evaluations: %d" % func_calls[0])
             print("         Gradient evaluations: %d" % grad_calls[0])
 
     elif k >= maxiter:
         warnflag = 1
         if disp:
             print("Warning: Maximum number of iterations has been exceeded")
-            print("         Current function value: %f" % fval)
+            print("         Current function value: %s" % fval)
             print("         Iterations: %d" % k)
             print("         Function evaluations: %d" % func_calls[0])
             print("         Gradient evaluations: %d" % grad_calls[0])
     else:
         if disp:
             print("Optimization terminated successfully.")
-            print("         Current function value: %f" % fval)
+            print("         Current function value: %s" % fval)
             print("         Iterations: %d" % k)
             print("         Function evaluations: %d" % func_calls[0])
             print("         Gradient evaluations: %d" % grad_calls[0])
 
 
     if full_output:
         retlist = xk, fval, func_calls[0], grad_calls[0], warnflag
@@ -1142,24 +1142,24 @@
 
     if disp or full_output:
         fval = old_fval
     if k >= maxiter:
         warnflag = 1
         if disp:
             print("Warning: Maximum number of iterations has been exceeded")
-            print("         Current function value: %f" % fval)
+            print("         Current function value: %s" % fval)
             print("         Iterations: %d" % k)
             print("         Function evaluations: %d" % fcalls[0])
             print("         Gradient evaluations: %d" % gcalls[0])
             print("         Hessian evaluations: %d" % hcalls)
     else:
         warnflag = 0
         if disp:
             print("Optimization terminated successfully.")
-            print("         Current function value: %f" % fval)
+            print("         Current function value: %s" % fval)
             print("         Iterations: %d" % k)
             print("         Function evaluations: %d" % fcalls[0])
             print("         Gradient evaluations: %d" % gcalls[0])
             print("         Hessian evaluations: %d" % hcalls)
 
     if full_output:
         retlist = xk, fval, fcalls[0], gcalls[0], hcalls, warnflag
@@ -1886,15 +1886,15 @@
     elif iter >= maxiter:
         warnflag = 2
         if disp:
             print("Warning: Maximum number of iterations has been exceeded")
     else:
         if disp:
             print("Optimization terminated successfully.")
-            print("         Current function value: %f" % fval)
+            print("         Current function value: %s" % fval)
             print("         Iterations: %d" % iter)
             print("         Function evaluations: %d" % fcalls[0])
 
     x = squeeze(x)
 
     if full_output:
         retlist = x, fval, direc, iter, fcalls[0], warnflag
```

### Comparing `mystic-0.4.0/mystic/_scipyoptimize.py` & `mystic-0.4.1/mystic/_scipyoptimize.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 # You may copy and use this module as you see fit with no
 # guarantee implied provided you keep this notice in all copies.
 # *****END NOTICE************
 #
 # Forked by: Mike McKerns (February 2009)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """modified algorithms from local copy of scipy.optimize"""
 
 #__all__ = ['fmin', 'fmin_powell', 'fmin_ncg', 'fmin_cg', 'fmin_bfgs',
 #           'fminbound','brent', 'golden','bracket','rosen','rosen_der',
 #           'rosen_hess', 'rosen_hess_prod', 'brute', 'approx_fprime',
```

### Comparing `mystic-0.4.0/mystic/_signal.py` & `mystic-0.4.1/mystic/_signal.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2006-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''a signal handler for a mystic solver instance'''
 
 # pull from the signal module
 from signal import *
```

### Comparing `mystic-0.4.0/mystic/_symbolic.py` & `mystic-0.4.1/mystic/_symbolic.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 # The following code attempts to construct something like:
 # >>> from sympy import Eq, Symbol
 # >>> from sympy import solve as symsol
 # >>> x0 = Symbol('x0')
@@ -24,40 +24,39 @@
 def _classify_variables(constraints, variables='x', nvars=None): 
     """Takes a string of constraint equations and determines which variables
 are dependent, independent, and unconstrained. Assumes there are no duplicate
 equations. Returns a dictionary with keys: 'dependent', 'independent', and
 'unconstrained', and with values that enumerate the variables that match
 each variable type.
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
         equation per line. Constraints must be equality constraints only.
-        Standard python syntax should be followed (with the math and numpy
-        modules already imported).
-
-    For example:
-        >>> constraints = '''
-        ...     x0 = x4**2
-        ...     x2 = x3 + x4'''
-        >>> _classify_variables(constraints, nvars=5)
-        {'dependent':['x0','x2'], 'independent':['x3','x4'], 'unconstrained':['x1']}
-        >>> constraints = '''
-        ...     x0 = x4**2
-        ...     x4 - x3 = 0.
-        ...     x4 - x0 = x2'''
-        >>> _classify_variables(constraints, nvars=5)
-        {'dependent': ['x0','x2','x4'], 'independent': ['x3'], 'unconstrained': ['x1']}
-
-Additional Inputs:
-    nvars -- number of variables. Includes variables not explicitly
-        given by the constraint equations (e.g. 'x1' in the example above).
-    variables -- desired variable name. Default is 'x'. A list of variable
+        Standard python syntax should be followed (the ``math`` and ``numpy``
+        modules are already imported).
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
+    nvars (int, default=None): number of variables. Includes variables not
+        explicitly stated in the constraints (e.g. ``x1`` in the example below).
+
+Examples:
+    >>> constraints = '''
+    ...     x0 = x4**2
+    ...     x2 = x3 + x4'''
+    >>> _classify_variables(constraints, nvars=5)
+    {'dependent':['x0','x2'], 'independent':['x3','x4'], 'unconstrained':['x1']}
+
+    >>> constraints = '''
+    ...     x0 = x4**2
+    ...     x4 - x3 = 0.
+    ...     x4 - x0 = x2'''
+    >>> _classify_variables(constraints, nvars=5)
+    {'dependent': ['x0','x2','x4'], 'independent': ['x3'], 'unconstrained': ['x1']}
 """
     if ">" in constraints or "<" in constraints:
         raise NotImplementedError("cannot classify inequalities") 
 
     from mystic.symbolic import replace_variables, get_variables
     #XXX: use solve? or first if not in form xi = ... ?
     if list_or_tuple_or_ndarray(variables):
@@ -140,45 +139,44 @@
 
 def _prepare_sympy(constraints, variables='x', nvars=None):
     """Parse an equation string and prepare input for sympy. Returns a tuple
 of sympy-specific input: (code for variable declaration, left side of equation
 string, right side of equation string, list of variables, and the number of
 sympy equations).
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
         equation per line. Constraints must be equality constraints only.
-        Standard python syntax should be followed (with the math and numpy
-        modules already imported).
-
-    For example:
-        >>> constraints = '''
-        ...     x0 = x4**2
-        ...     x4 - x3 = 0.
-        ...     x4 - x0 = x2'''
-        >>> code, lhs, rhs, vars, neqn = _prepare_sympy(constraints, nvars=5)
-        >>> print(code)
-        x0=Symbol('x0')
-        x1=Symbol('x1')
-        x2=Symbol('x2')
-        x3=Symbol('x3')
-        x4=Symbol('x4')
-        rand = Symbol('rand')
-        >>> print("%s %s" % (lhs, rhs))
-        ['x0 ', 'x4 - x3 ', 'x4 - x0 '] [' x4**2', ' 0.', ' x2']
-        >>> print("%s in %s eqns" % (vars, neqn))
-        x0,x1,x2,x3,x4, in 3 eqns
-
-Additional Inputs:
-    nvars -- number of variables. Includes variables not explicitly
-        given by the constraint equations (e.g. 'x1' in the example above).
-    variables -- desired variable name. Default is 'x'. A list of variable
+        Standard python syntax should be followed (the ``math`` and ``numpy``
+        modules are already imported).
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
+    nvars (int, default=None): number of variables. Includes variables not
+        explicitly stated in the constraints (e.g. ``x1`` in the example below).
+
+Examples:
+    >>> constraints = '''
+    ...     x0 = x4**2
+    ...     x4 - x3 = 0.
+    ...     x4 - x0 = x2'''
+    >>> code, lhs, rhs, vars, neqn = _prepare_sympy(constraints, nvars=5)
+    >>> print(code)
+    x0=Symbol('x0')
+    x1=Symbol('x1')
+    x2=Symbol('x2')
+    x3=Symbol('x3')
+    x4=Symbol('x4')
+    rand = Symbol('rand')
+    >>> print("%s %s" % (lhs, rhs))
+    ['x0 ', 'x4 - x3 ', 'x4 - x0 '] [' x4**2', ' 0.', ' x2']
+    >>> print("%s in %s eqns" % (vars, neqn))
+    x0,x1,x2,x3,x4, in 3 eqns
+
 """
     if ">" in constraints or "<" in constraints:
         raise NotImplementedError("cannot simplify inequalities") 
 
     from mystic.symbolic import replace_variables, get_variables
     #XXX: if constraints contain x0,x1,x3 for 'x', should x2 be in code,xlist?
     if list_or_tuple_or_ndarray(variables):
@@ -229,49 +227,44 @@
     code += "rand = Symbol('rand')\n"
     return code, left, right, xlist, neqns
 
 
 def _solve_single(constraint, variables='x', target=None, **kwds):
     """Solve a symbolic constraints equation for a single variable.
 
-Inputs:
-    constraint -- a string of symbolic constraints. Only a single constraint
+Args:
+    constraint (str): a string of symbolic constraints. Only a single constraint
         equation should be provided, and must be an equality constraint. 
-        Standard python syntax should be followed (with the math and numpy
-        modules already imported).
-
-    For example:
-        >>> equation = "x1 - 3. = x0*x2"
-        >>> print(_solve_single(equation))
-        x0 = -(3.0 - x1)/x2
-
-Additional Inputs:
-    variables -- desired variable name. Default is 'x'. A list of variable
+        Standard python syntax should be followed (the ``math`` and ``numpy``
+        modules are already imported).
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
-    target -- list providing the order for which the variables will be solved.
-        By default, increasing order is used.
-
-    For example:
-        >>> equation = "x1 - 3. = x0*x2"
-        >>> print(_solve_single(equation, target='x1'))
-        x1 = 3.0 + x0*x2
-
-Further Inputs:
-    locals -- a dictionary of additional variables used in the symbolic
+    target (list[str], default=None): list providing the order for which the
+        variables will be solved. By default, increasing order is used.
+    locals (dict, default={}): additional variables used in the symbolic
         constraints equations, and their desired values.
-    simplest -- if True, simplify all but polynomials order >= 3 [False]
-    rational -- if True, recast floats as rationals during solve [False]
-    sequence -- if True, solve sequentially and not as a matrix [False]
-    implicit -- if True, solve implicitly (with sin, cos, ...) [False]
-    check -- if False, skip minimal testing (divide_by_zero, ...) [True]
-    permute -- if True, return all permutations [False]
-    warn -- if True, don't suppress warnings [True]
-    verbose -- if True, print debug information [False]
+    simplest (bool, default=False): simplify all but polynomials order >= 3
+    rational (bool, default=False): recast floats as rationals during solve
+    sequence (bool, default=False): solve sequentially and not as a matrix
+    implicit (bool, default=False): solve implicitly (with sin, cos, ...)
+    check (bool, default=True): perform validity testing (divide_by_zero, ...)
+    permute (bool, default=False): return all permutations (*expensive*)
+    warn (bool, default=True): if True, don't suppress warnings
+    verbose (bool, default=False): print debug information
+
+Examples:
+    >>> equation = "x1 - 3. = x0*x2"
+    >>> print(_solve_single(equation))
+    x0 = -(3.0 - x1)/x2
+
+    >>> equation = "x1 - 3. = x0*x2"
+    >>> print(_solve_single(equation, target='x1'))
+    x1 = 3.0 + x0*x2
 """ #XXX: an very similar version of this code is found in _solve_linear XXX#
     # for now, we abort on multi-line equations or inequalities
     if len(constraint.replace('==','=').split('=')) != 2:
         raise NotImplementedError("requires a single valid equation") 
     if ">" in constraint or "<" in constraint:
         raise NotImplementedError("cannot simplify inequalities") 
 
@@ -320,15 +313,15 @@
     if nvars is not None: ndim = nvars
 
     # create function to replace "_" with original variables
     def restore(variables, mystring):
         if list_or_tuple_or_ndarray(variables):
             vars = get_variables(mystring,'_')
             indices = [int(v.strip('_')) for v in vars]
-            for i in range(len(vars)):
+            for i in reversed(range(len(vars))):
                 mystring = mystring.replace(vars[i],variables[indices[i]])
         return mystring
 
     # default is _locals with sympy imported
     _locals = {}
     locals = kwds['locals'] if 'locals' in kwds else None
     if locals is None: locals = {}
@@ -342,14 +335,15 @@
     except ImportError: # Equation will not be simplified."
         if warn: print("Warning: sympy not installed.")
         return constraint
 
     # default is _locals with numpy and math imported
     # numpy throws an 'AttributeError', but math passes error to sympy
     code = """from numpy import *; from math import *;""" # prefer math
+    code += """from builtins import *;""" # don't overload builtins
     code += """from numpy import mean as average;""" # use np.mean not average
     code += """from numpy import var as variance;""" # look like mystic.math
     code += """from numpy import ptp as spread;"""   # look like mystic.math
     code = compile(code, '<string>', 'exec')
     exec(code, _locals)
     _locals.update(dict(symsol_kwds=kwarg))
     _locals.update(locals) #XXX: allow this?
@@ -421,57 +415,52 @@
         return '' if sol and not sol.strip() else sol
     return tuple(solns)
 
 
 def _solve_linear(constraints, variables='x', target=None, **kwds):
     """Solve a system of symbolic linear constraints equations.
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
         equation per line. Constraints must be equality constraints only.
-        Standard python syntax should be followed (with the math and numpy
-        modules already imported).
-
-    For example:
-        >>> constraints = '''
-        ...     x0 - x2 = 2.
-        ...     x2 = x3*2.'''
-        >>> print(_solve_linear(constraints))
-        x2 = 2.0*x3
-        x0 = 2.0 + 2.0*x3
-
-Additional Inputs:
-    variables -- desired variable name. Default is 'x'. A list of variable
+        Standard python syntax should be followed (the ``math`` and ``numpy``
+        modules are already imported).
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
-    target -- list providing the order for which the variables will be solved.
-        If there are "N" constraint equations, the first "N" variables given
-        will be selected as the dependent variables. By default, increasing
-        order is used.
-
-    For example:
-        >>> constraints = '''
-        ...     x0 - x2 = 2.
-        ...     x2 = x3*2.'''
-        >>> print(_solve_linear(constraints, target=['x3','x2']))
-        x3 = -1.0 + 0.5*x0
-        x2 = -2.0 + x0
-
-Further Inputs:
-    locals -- a dictionary of additional variables used in the symbolic
+    target (list[str], default=None): list providing the order for which the
+        variables will be solved. If there are N constraint equations, the
+        first N variables given will be selected as the dependent variables.
+        By default, increasing order is used.
+    locals (dict, default={}): additional variables used in the symbolic
         constraints equations, and their desired values.
-    simplest -- if True, simplify all but polynomials order >= 3 [False]
-    rational -- if True, recast floats as rationals during solve [False]
-    sequence -- if True, solve sequentially and not as a matrix [False]
-    implicit -- if True, solve implicitly (with sin, cos, ...) [False]
-    check -- if False, skip minimal testing (divide_by_zero, ...) [True]
-    permute -- if True, return all permutations [False]
-    warn -- if True, don't suppress warnings [True]
-    verbose -- if True, print debug information [False]
+    simplest (bool, default=False): simplify all but polynomials order >= 3
+    rational (bool, default=False): recast floats as rationals during solve
+    sequence (bool, default=False): solve sequentially and not as a matrix
+    implicit (bool, default=False): solve implicitly (with sin, cos, ...)
+    check (bool, default=True): perform validity testing (divide_by_zero, ...)
+    permute (bool, default=False): return all permutations (*expensive*)
+    warn (bool, default=True): if True, don't suppress warnings
+    verbose (bool, default=False): print debug information
+
+Examples:
+    >>> constraints = '''
+    ...     x0 - x2 = 2.
+    ...     x2 = x3*2.'''
+    >>> print(_solve_linear(constraints))
+    x2 = 2.0*x3
+    x0 = 2.0 + 2.0*x3
+
+    >>> constraints = '''
+    ...     x0 - x2 = 2.
+    ...     x2 = x3*2.'''
+    >>> print(_solve_linear(constraints, target=['x3','x2']))
+    x3 = -1.0 + 0.5*x0
+    x2 = -2.0 + x0
 """
     nvars = None
     permute = False # if True, return all permutations
     warn = True  # if True, don't suppress warnings
     verbose = False  # if True, print debug info
     simplest = False # if True, simplify all but polynomials order >= 3
     rational = False # if True, recast floats as rationals during solve
@@ -514,15 +503,15 @@
     if nvars is not None: ndim = nvars
 
     # create function to replace "_" with original variables
     def restore(variables, mystring):
         if list_or_tuple_or_ndarray(variables):
             vars = get_variables(mystring,'_')
             indices = [int(v.strip('_')) for v in vars]
-            for i in range(len(vars)):
+            for i in reversed(range(len(vars))):
                 mystring = mystring.replace(vars[i],variables[indices[i]])
         return mystring
 
     # default is _locals with sympy imported
     _locals = {}
     locals = kwds['locals'] if 'locals' in kwds else None
     if locals is None: locals = {}
@@ -537,14 +526,15 @@
     except ImportError: # Equation will not be simplified."
         if warn: print("Warning: sympy not installed.")
         return constraints
 
     # default is _locals with numpy and math imported
     # numpy throws an 'AttributeError', but math passes error to sympy
     code = """from numpy import *; from math import *;""" # prefer math
+    code += """from builtins import *;""" # don't overload builtins
     code += """from numpy import mean as average;""" # use np.mean not average
     code += """from numpy import var as variance;""" # look like mystic.math
     code += """from numpy import ptp as spread;"""   # look like mystic.math
     code = compile(code, '<string>', 'exec')
     exec(code, _locals)
     _locals.update(dict(symsol_kwds=kwarg))
     _locals.update(locals) #XXX: allow this?
@@ -635,63 +625,59 @@
 #           stringperms.append(permstring.rstrip())
 #   return tuple(stringperms)
 
 
 def solve(constraints, variables='x', target=None, **kwds):
     """Solve a system of symbolic constraints equations.
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
         equation per line. Constraints must be equality constraints only.
-        Standard python syntax should be followed (with the math and numpy
-        modules already imported).
-
-    For example:
-        >>> constraints = '''
-        ...     x0 - x2 = 2.
-        ...     x2 = x3*2.'''
-        >>> print(solve(constraints))
-        x2 = 2.0*x3
-        x0 = 2.0 + 2.0*x3
-        >>> constraints = '''
-        ...     spread([x0,x1]) - 1.0 = mean([x0,x1])   
-        ...     mean([x0,x1,x2]) = x2'''
-        >>> print(solve(constraints))
-        x0 = -0.5 + 0.5*x2
-        x1 = 0.5 + 1.5*x2
-
-Additional Inputs:
-    variables -- desired variable name. Default is 'x'. A list of variable
+        Standard python syntax should be followed (the ``math`` and ``numpy``
+        modules are already imported).
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
-    target -- list providing the order for which the variables will be solved.
-        If there are "N" constraint equations, the first "N" variables given
-        will be selected as the dependent variables. By default, increasing
-        order is used.
-
-    For example:
-        >>> constraints = '''
-        ...     x0 - x2 = 2.
-        ...     x2 = x3*2.'''
-        >>> print(solve(constraints, target=['x3','x2']))
-        x3 = -1.0 + 0.5*x0
-        x2 = -2.0 + x0
-
-Further Inputs:
-    locals -- a dictionary of additional variables used in the symbolic
+    target (list[str], default=None): list providing the order for which the
+        variables will be solved. If there are N constraint equations, the
+        first N variables given will be selected as the dependent variables.
+        By default, increasing order is used.
+    locals (dict, default={}): additional variables used in the symbolic
         constraints equations, and their desired values.
-    simplest -- if True, simplify all but polynomials order >= 3 [False]
-    rational -- if True, recast floats as rationals during solve [False]
-    sequence -- if True, solve sequentially and not as a matrix [False]
-    implicit -- if True, solve implicitly (with sin, cos, ...) [False]
-    check -- if False, skip minimal testing (divide_by_zero, ...) [True]
-    permute -- if True, return all permutations [False]
-    warn -- if True, don't suppress warnings [False]
-    verbose -- if True, print debug information [False]
+    simplest (bool, default=False): simplify all but polynomials order >= 3
+    rational (bool, default=False): recast floats as rationals during solve
+    sequence (bool, default=False): solve sequentially and not as a matrix
+    implicit (bool, default=False): solve implicitly (with sin, cos, ...)
+    check (bool, default=True): perform validity testing (divide_by_zero, ...)
+    permute (bool, default=False): return all permutations (*expensive*)
+    warn (bool, default=False): if True, don't suppress warnings
+    verbose (bool, default=False): print debug information
+
+Examples:
+    >>> constraints = '''
+    ...     x0 - x2 = 2.
+    ...     x2 = x3*2.'''
+    >>> print(solve(constraints))
+    x2 = 2.0*x3
+    x0 = 2.0 + 2.0*x3
+
+    >>> constraints = '''
+    ...     spread([x0,x1]) - 1.0 = mean([x0,x1])   
+    ...     mean([x0,x1,x2]) = x2'''
+    >>> print(solve(constraints))
+    x0 = -0.5 + 0.5*x2
+    x1 = 0.5 + 1.5*x2
+
+    >>> constraints = '''
+    ...     x0 - x2 = 2.
+    ...     x2 = x3*2.'''
+    >>> print(solve(constraints, target=['x3','x2']))
+    x3 = -1.0 + 0.5*x0
+    x2 = -2.0 + x0
 """
     kwds['warn'] = kwds.get('warn', False)
     try:
         if len(constraints.replace('==','=').split('=')) <= 2:
             soln = _solve_single(constraints, variables=variables, \
                                  target=target, **kwds)
             # for corner case where has something like: '0*xN'
@@ -711,60 +697,56 @@
     return soln
 
 
 def _solve_nonlinear(constraints, variables='x', target=None, **kwds):
     """Build a constraints function given a string of nonlinear constraints.
 Returns a constraints function. 
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
         equation per line. Constraints must be equality constraints only.
-        Standard python syntax should be followed (with the math and numpy
-        modules already imported).
-
-    For example:
-        >>> constraints = '''x1 = x3*3. + x0*x2'''
-        >>> print(_solve_nonlinear(constraints))
-        x0 = (x1 - 3.0*x3)/x2
-        >>> constraints = '''
-        ...     spread([x0,x1]) - 1.0 = mean([x0,x1])   
-        ...     mean([x0,x1,x2]) = x2'''
-        >>> print(_solve_nonlinear(constraints))
-        x0 = -0.5 + 0.5*x2
-        x1 = 0.5 + 1.5*x2
-
-Additional Inputs:
-    variables -- desired variable name. Default is 'x'. A list of variable
+        Standard python syntax should be followed (the ``math`` and ``numpy``
+        modules are already imported).
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
-    target -- list providing the order for which the variables will be solved.
-        If there are "N" constraint equations, the first "N" variables given
-        will be selected as the dependent variables. By default, increasing
-        order is used.
-
-    For example:
-        >>> constraints = '''
-        ...     spread([x0,x1]) - 1.0 = mean([x0,x1])   
-        ...     mean([x0,x1,x2]) = x2'''
-        >>> print(_solve_nonlinear(constraints, target=['x1']))
-        x1 = -0.833333333333333 + 0.166666666666667*x2
-        x0 = -0.5 + 0.5*x2
-
-Further Inputs:
-    locals -- a dictionary of additional variables used in the symbolic
+    target (list[str], default=None): list providing the order for which the
+        variables will be solved. If there are N constraint equations, the
+        first N variables given will be selected as the dependent variables.
+        By default, increasing order is used.
+    locals (dict, default={}): additional variables used in the symbolic
         constraints equations, and their desired values.
-    simplest -- if True, simplify all but polynomials order >= 3 [False]
-    rational -- if True, recast floats as rationals during solve [False]
-    sequence -- if True, solve sequentially and not as a matrix [False]
-    implicit -- if True, solve implicitly (with sin, cos, ...) [False]
-    check -- if False, skip minimal testing (divide_by_zero, ...) [True]
-    permute -- if True, return all permutations [False]
-    warn -- if True, don't suppress warnings [True]
-    verbose -- if True, print debug information [False]
+    simplest (bool, default=False): simplify all but polynomials order >= 3
+    rational (bool, default=False): recast floats as rationals during solve
+    sequence (bool, default=False): solve sequentially and not as a matrix
+    implicit (bool, default=False): solve implicitly (with sin, cos, ...)
+    check (bool, default=True): perform validity testing (divide_by_zero, ...)
+    permute (bool, default=False): return all permutations (*expensive*)
+    warn (bool, default=True): if True, don't suppress warnings
+    verbose (bool, default=False): print debug information
+
+Examples:
+    >>> constraints = '''x1 = x3*3. + x0*x2'''
+    >>> print(_solve_nonlinear(constraints))
+    x0 = (x1 - 3.0*x3)/x2
+
+    >>> constraints = '''
+    ...     spread([x0,x1]) - 1.0 = mean([x0,x1])   
+    ...     mean([x0,x1,x2]) = x2'''
+    >>> print(_solve_nonlinear(constraints))
+    x0 = -0.5 + 0.5*x2
+    x1 = 0.5 + 1.5*x2
+
+    >>> constraints = '''
+    ...     spread([x0,x1]) - 1.0 = mean([x0,x1])   
+    ...     mean([x0,x1,x2]) = x2'''
+    >>> print(_solve_nonlinear(constraints, target=['x1']))
+    x1 = -0.833333333333333 + 0.166666666666667*x2
+    x0 = -0.5 + 0.5*x2
 """
     nvars = None
     permute = False # if True, return all permutations
     warn = True  # if True, don't suppress warnings
     verbose = False # if True, print details from _classify_variables
     simplest = False # if True, simplify all but polynomials order >= 3
     rational = False # if True, recast floats as rationals during solve
@@ -803,15 +785,15 @@
     if nvars is not None: ndim = nvars
 
     # create function to replace "_" with original variables
     def restore(variables, mystring):
         if list_or_tuple_or_ndarray(variables):
             vars = get_variables(mystring,'_')
             indices = [int(v.strip('_')) for v in vars]
-            for i in range(len(vars)):
+            for i in reversed(range(len(vars))):
                 mystring = mystring.replace(vars[i],variables[indices[i]])
         return mystring
 
     locals = kwds['locals'] if 'locals' in kwds else None
     if locals is None: locals = {}
 
     eqns = constraints.splitlines()
```

### Comparing `mystic-0.4.0/mystic/abstract_ensemble_solver.py` & `mystic-0.4.1/mystic/abstract_ensemble_solver.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 # Abstract Ensemble Solver Class
 """
 This module contains the base class for launching several mystic solvers
 instances -- utilizing a parallel ``map`` function to enable parallel
@@ -167,24 +167,32 @@
     def __total_iters(self):
         """total number of iterations"""
         return sum(self._all_iters)
 
     def SetNestedSolver(self, solver):
         """set the nested solver
 
-input::
-    - solver: a mystic solver instance (e.g. NelderMeadSimplexSolver(3) )"""
+Args:
+    solver (solver): a solver instance (e.g. ``NelderMeadSimplexSolver(3)``)
+
+Returns:
+    None
+        """
         self._solver = solver
         return
 
     def __get_solver_instance(self, reset=False):
         """ensure the solver is a solver instance
 
-input::
-    - reset: if reset is True, reset the monitor instances"""
+Args:
+    reset (bool, default=False): reset the monitor instances
+
+Returns:
+    a nested solver instance
+        """
         solver = self._solver
 
         # if a configured solver is not given, then build one of the given type
         from mystic.abstract_solver import AbstractSolver
         if isinstance(solver, AbstractSolver): # is a configured solver instance
             return solver
         if not hasattr(solver, "Solve"):       # is an Error...
@@ -216,68 +224,101 @@
         if self._reducer: #XXX: always, settable, or sync'd ?
             solver.SetReducer(self._reducer, arraylike=True)
         solver.SetObjective(self._cost[1], self._cost[2])
         solver.SetSaveFrequency(self._saveiter, self._state)
         return solver
 
     def SetInitialPoints(self, x0, radius=0.05):
-        """Set Initial Points with Guess (x0)
+        """Set Initial Points with Guess (``x0``)
 
-input::
-    - x0: must be a sequence of length self.nDim
-    - radius: generate random points within [-radius*x0, radius*x0]
-        for i!=0 when a simplex-type initial guess in required
+Args:
+    x0 (list[float]): a sequence of length ``self.nDim``
+    radius (float): generate random points within ``[-radius*x0, radius*x0]``
+        for ``i!=0`` when a simplex-type initial guess is required
 
-*** this method must be overwritten ***"""
+Returns:
+    None
+
+NOTE:
+    *** this method must be overwritten ***"""
         raise NotImplementedError("must be overwritten...")
     
     def SetRandomInitialPoints(self, min=None, max=None):
         """Generate Random Initial Points within given Bounds
 
-input::
-    - min, max: must be a sequence of length self.nDim
-    - each min[i] should be <= the corresponding max[i]
+Args:
+    min (list[float], default=None): lower bounds, list of length ``self.nDim``
+    max (list[float], default=None): upper bounds, list of length ``self.nDim``
 
-*** this method must be overwritten ***"""
+Returns:
+    None
+
+Notes:
+    - each ``min[i]`` must be less than or equal to the corresponding ``max[i]``
+
+NOTE:
+    *** this method must be overwritten ***"""
         raise NotImplementedError("must be overwritten...")
 
     def SetMultinormalInitialPoints(self, mean, var=None):
         """Generate Initial Points from Multivariate Normal.
 
-input::
-    - mean must be a sequence of length self.nDim
-    - var can be...
-        None: -> it becomes the identity
-        scalar: -> var becomes scalar * I
-        matrix: -> the variance matrix. must be the right size!
+Args:
+    mean (list[float]): mean values, list of length ``self.nDim``
+    var (ndarray[float,float], default=None): covariance matrix
+
+Returns:
+    None
+
+Notes:
+    - ``var`` must be symmetric, positive-semidefinite, and length ``self.nDim``
+    - if ``var`` is None, then ``var`` becomes the Identity matrix, ``I``
+    - if ``var`` is a scalar, then ``var`` is set to ``var * I``
 
-*** this method must be overwritten ***"""
+NOTE:
+    *** this method must be overwritten ***"""
         raise NotImplementedError("must be overwritten...")
 
     def SetSampledInitialPoints(self, dist=None):
         """Generate Random Initial Points from Distribution (dist)
 
-input::
-    - dist: a mystic.math.Distribution instance
+Args:
+    dist (Distribution, default=None): a mystic.math.Distribution instance
 
-*** this method must be overwritten ***"""
+Returns:
+    None
+
+Notes:
+    - if ``dist`` is None, use a uniform distribution in the interval ``[0, 1)``
+
+NOTE:
+    *** this method must be overwritten ***"""
         raise NotImplementedError("must be overwritten...")
 
     def Terminated(self, disp=False, info=False, termination=None, all=None):
         """check if the solver meets the given termination conditions
 
-Input::
-    - disp = if True, print termination statistics and/or warnings
-    - info = if True, return termination message (instead of boolean)
-    - termination = termination conditions to check against
-    - all = if True, get results for all solvers; if False, only check 'best'
-
-Notes::
-    If no termination conditions are given, the solver's stored
-    termination conditions will be used.
+Args:
+    disp (bool, default=False): print termination statistics and/or warnings
+    info (bool, default=False): return termination message (instead of boolean)
+    termination (termination, default=None): termination conditions to check
+    all (bool, default=None): check results for all solvers
+
+Returns:
+    information about the state of the solver termination (see Notes)
+
+Notes:
+    - ``all`` can be one of ``{True, False, None}``
+    - if ``all`` is True, return a list checking termination for each solver
+    - if ``all`` is None, check whether all solvers have terminated
+    - if ``all`` is False, check if the 'best' solver terminated
+    - if ``info`` is False, return a bool regarding the termination
+    - if ``info`` is True, return an informative string about the termination,
+      or a list of strings (depending on the value of ``all``)
+    - if ``termination`` is None, the solver's stored termination is be used
         """
         if disp in ['verbose', 'all']: verbose = True
         else: verbose = False
         no = '' if info else False
         if all is True:
             end = [no if s is None else s.Terminated(verbose, info, termination) for s in self._allSolvers]
             return end
@@ -309,15 +350,15 @@
                 print("Warning: Maximum number of iterations has been exceeded")
         elif solver._EARLYEXIT: #XXX: self or solver ?
             msg = sig
             if disp:
                 print("Warning: Optimization terminated with signal interrupt.")
         elif msg and disp:
             print("Optimization terminated successfully.")
-            print("         Current function value: %f" % solver.bestEnergy)
+            print("         Current function value: %s" % solver.bestEnergy)
             print("         Iterations: %d" % solver.generations)
             print("         Function evaluations: %d" % solver._fcalls[0])
             print("         Total function evaluations: %d" % self._total_evals)
 
         if info:
             return msg
         return bool(msg)
@@ -333,30 +374,35 @@
             dist = Distribution(dist) #XXX: or throw error?
         self._dist = dist #FIXME: accept a list of Distributions
         return
 
     def _InitialPoints(self):
         """Generate a grid of starting points for the ensemble of optimizers
 
-*** this method must be overwritten ***"""
+NOTE:
+    *** this method must be overwritten ***"""
         raise NotImplementedError("a sampling algorithm was not provided")
 
     def _is_new(self):
         """determine if solver has been run or not"""
         return not any(self._allSolvers)
 
     def _is_best(self):
         """get the id of the bestSolver"""
         return getattr(self._bestSolver, 'id', None)
 
     def __init_allSolvers(self, reset=False):
-        """populate NestedSolver state to allSolvers
+        """populate ``NestedSolver`` state to ``allSolvers``
+
+Args:
+    reset (bool, default=False): reset the monitor instances
 
-input::
-    - reset: if reset is True, reset the monitor instances"""
+Returns:
+    returns a list of solver instances
+        """
         # get the nested solver instance
         solver = self._AbstractEnsembleSolver__get_solver_instance(reset)
 
         # configure inputs for each solver
         from copy import deepcopy as _copy
         at = self.id if self.id else 0  #XXX start at self.id?
         #at = max((getattr(i, 'id', self.id) or 0) for i in self._allSolvers)
@@ -435,18 +481,31 @@
         self.energy_history = None
         self.solution_history = None
         return
 
     def Collapsed(self, disp=False, info=False, all=None):
         """check if the solver meets the given collapse conditions
 
-Input::
-    - disp = if True, print details about the solver state at collapse
-    - info = if True, return collapsed state (instead of boolean)
-    - all = if True, get results for all solvers; if False, only check 'best'
+Args:
+    disp (bool, default=False): print details about the solver state at collapse
+    info (bool, default=False): return collapsed state (instead of boolean)
+    all (bool, default=None): check results for all solvers
+
+Returns:
+    information about the state of the solver collapse (see Notes)
+
+Notes:
+    - ``all`` can be one of ``{True, False, all, any}``
+    - if ``all`` is True, check if all solvers have collapsed
+    - if ``all`` is any (or None), check if any solver has collapsed
+    - if ``all`` is all, check if all solvers have the same collapse
+    - if ``all`` is False, check if the 'best' solver collapsed
+    - if ``info`` is False, return a bool regarding the collapse
+    - if ``info`` is True, return an informative string about the collapse,
+      or a list of strings (depending on the value of ``all``)
 """ #FIXME: how handle collapse of base solver, mask of base solver...?
         _all = __builtins__['all']
         if all is None: all = any #FIXME: what should default be???
         elif all not in (any, _all, True, False): # may be np.all or np.any
             name = getattr(all, '__name__', '')
             if name == 'any': all = any
             elif name == 'all': all = _all
@@ -515,37 +574,46 @@
         self._AbstractEnsembleSolver__update_state()
         if self._bestSolver:
             return self._bestSolver.Collapsed(disp, info)
         return super(AbstractEnsembleSolver, self).Collapsed(disp, info)
 
     def Collapse(self, disp=False): #FIXME #TODO
         """if solver has terminated by collapse, apply the collapse
-        (unless both collapse and "stop" are simultaneously satisfied)
 
-input::
-    - disp: if True, print details about the solver state at collapse
+Args:
+    disp (bool, default=False): print details about the solver state at collapse
+
+Returns:
+    a dict of ``{info: collapse}``, where ``info`` is collapse termination info
+
+Notes:
+    - collapse must be triggered by calling this method, unless both the
+      "collapse" termination and a "stop" termination are simultaneously
+      satisfied.
 
-note::
-    updates the solver's termination conditions and constraints
+NOTE:
+   *** this method is not implemented and returns False ***
         """
         return False
 
     def _Step(self, cost=None, ExtraArgs=None, **kwds):
         """perform a single optimization iteration
 
-input::
-    - cost is the objective function, of the form y = cost(x, *ExtraArgs),
-      where x is a candidate solution, and ExtraArgs is the tuple of positional
-      arguments required to evaluate the objective.
+Args:
+    cost (func, default=None): objective, of form ``y = cost(x, *ExtraArgs)``,
+      where ``x`` is a candidate solution vector
+    ExtraArgs (tuple, default=None): tuple of positional arguments required to
+      evaluate the objective
 
-note::
-    ExtraArgs needs to be a *tuple* of extra arguments.
+Returns:
+    None
 
-    This method accepts additional args that are specific for the current
-    solver, as detailed in the `_process_inputs` method.
+Notes:
+    - This method accepts additional ``kwds`` that are specific for the current
+      solver, as detailed in the ``_process_inputs`` method.
         """
         # process and activate input settings
         kwds['step'] = True  #XXX: once Step is taken, step=True thereafter
         settings = self._process_inputs(kwds)
         #(hardwired: due to python exec'ing to locals())
         disp = settings['disp'] if 'disp' in settings else False
         echo = settings['callback'] if 'callback' in settings else None
@@ -604,30 +672,30 @@
         return
 
     def _process_inputs(self, kwds):
         """process and activate input settings
 
 Args:
     callback (func, default=None): function to call after each iteration. The
-        interface is ``callback(xk)``, with xk the current parameter vector.
+        interface is ``callback(xk)``, with ``xk`` the current parameter vector.
     disp (bool, default=False): if True, print convergence messages.
+    EvaluationMonitor (monitor, default=None): a monitor instance to capture
+        each evaluation of cost.
+    StepMonitor (monitor, default=None): a monitor instance to capture each
+        iteration's best results.
+    penalty (penalty, default=None): function of the form: ``y' = penalty(xk)``,
+        with ``y = cost(xk) + y'`` and ``xk`` is the current parameter vector.
+    constraints (constraint, default=None): function of the form:
+        ``xk' = constraints(xk)``, where ``xk`` is the current parameter vector.
+    step (bool, default=False): if True, enable ``Step`` within the ensemble.
 
-Additional Args:
-    EvaluationMonitor: a monitor instance to capture each evaluation of cost.
-    StepMonitor: a monitor instance to capture each iteration's best results.
-    penalty: a function of the form: y' = penalty(xk), with y = cost(xk) + y',
-        where xk is the current parameter vector.
-    constraints: a function of the form: xk' = constraints(xk), where xk is
-        the current parameter vector.
-    step (bool, default=False): if True, enable Step within the ensemble.
-
-Note:
-   The additional args are 'sticky', in that once they are given, they remain
-   set until they are explicitly changed. Conversely, the args are not sticky,
-   and are thus set for a one-time use.
+Notes:
+    - ``callback`` and ``disp`` are 'sticky', in that once they are given, they
+      remain set until they are explicitly changed. Conversely, the other inputs
+      are not sticky, and are thus set for a one-time use.
         """
         #allow for inputs that don't conform to AbstractSolver interface
         #NOTE: not sticky: callback, disp
         #NOTE: sticky: EvaluationMonitor, StepMonitor, penalty, constraints
         #NOTE: sticky: step
         settings = super(AbstractEnsembleSolver, self)._process_inputs(kwds)
         settings.update({
@@ -643,20 +711,20 @@
     cost (func): the function to be minimized: ``y = cost(x)``.
     ExtraArgs (tuple): tuple of extra arguments for ``cost``.
     settings (dict): optimizer settings (produced by _process_inputs)
 
 Returns:
     None
 
-Note:
-    Optimizer settings for ensemble solvers include the `step` keyword,
-    which enables the Step menthod within the ensemble. By default, ensemble
-    solvers run to completion (i.e. Solve), for efficiency. Using `Step`
-    enables the ensemble to communicate state between members of the ensemble
-    at each iteration.
+Notes:
+    - Optimizer settings for ensemble solvers include the ``step`` keyword,
+      which causes the ``Step`` method to be used. By default, ensemble
+      solvers run to completion (i.e. ``Solve``), for efficiency. Using ``Step``
+      enables the ensemble to communicate state between members of the ensemble
+      at each iteration, which may slow execution.
         """
         #FIXME: 'step' is undocumented (in Solve)
         #NOTE: if Step once, will ensure always uses step=True, unless...
         #TODO: if step=False passed after Step taken... this is still TODO!
         step = settings['step'] if 'step' in settings else False
         if step: #FIXME: use abstract_solver _Solve
             super(AbstractEnsembleSolver, self)._Solve(cost, ExtraArgs, **settings)
```

### Comparing `mystic-0.4.0/mystic/abstract_launcher.py` & `mystic-0.4.1/mystic/abstract_launcher.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 This module contains the base classes for pathos pool and pipe objects,
 and describes the map and pipe interfaces.  A pipe is defined as a
 connection between two 'nodes', where a node is something that does
 work.  A pipe may be a one-way or two-way connection.  A map is defined
@@ -101,32 +101,33 @@
 Other class members:
     scatter     - True, if uses 'scatter-gather' (instead of 'worker-pool')
     source      - False, if minimal use of TemporaryFiles is desired
     timeout	- number of seconds to wait for return value from scheduler
         """
         object.__init__(self)#, *args, **kwds)
         self.__init(*args, **kwds)
-        self._id = None
+        self._id = kwds.get('id', None)
         return
     def __enter__(self):
         return self
     def __exit__(self, *args):
+        #self.clear()
         return
     def __init(self, *args, **kwds):
         """default filter for __init__ inputs
         """
         # allow default arg for 'nodes', but not if in kwds
         if len(args):
             try:
                 nodes = kwds['nodes']
                 msg = "got multiple values for keyword argument 'nodes'"
                 raise TypeError(msg)
             except KeyError:
                 nodes = args[0]
-        else: nodes = kwds['nodes'] if 'nodes' in kwds else self.__nodes
+        else: nodes = kwds.get('nodes', self.__nodes)
         try: self.nodes = nodes
         except TypeError: pass  # then self.nodes is read-only
         return
     def __map(self, f, *args, **kwds):
         """default filter for map inputs
         """
         # barf if given keywords
@@ -188,48 +189,54 @@
        #return #XXX: return _pool? (i.e. pop)
     def map(self, f, *args, **kwds):
         """run a batch of jobs with a blocking and ordered map
 
 Returns a list of results of applying the function f to the items of
 the argument sequence(s). If more than one sequence is given, the
 function is called with an argument list consisting of the corresponding
-item of each sequence.
+item of each sequence. Some maps accept the `chunksize` keyword, which
+causes the sequence to be split into tasks of approximately the given size.
         """
        #self.__map(f, *args, **kwds)
         raise NotImplementedError
     def imap(self, f, *args, **kwds):
         """run a batch of jobs with a non-blocking and ordered map
 
 Returns a list iterator of results of applying the function f to the items
 of the argument sequence(s). If more than one sequence is given, the
 function is called with an argument list consisting of the corresponding
-item of each sequence.
+item of each sequence. Some maps accept the `chunksize` keyword, which
+causes the sequence to be split into tasks of approximately the given size.
         """
        #self.__imap(f, *args, **kwds)
         raise NotImplementedError
     def uimap(self, f, *args, **kwds):
         """run a batch of jobs with a non-blocking and unordered map
 
 Returns a list iterator of results of applying the function f to the items
 of the argument sequence(s). If more than one sequence is given, the
 function is called with an argument list consisting of the corresponding
 item of each sequence. The order of the resulting sequence is not guaranteed.
+Some maps accept the `chunksize` keyword, which causes the sequence to be
+split into tasks of approximately the given size.
         """
        #self.__imap(f, *args, **kwds)
         raise NotImplementedError
     def amap(self, f, *args, **kwds):
         """run a batch of jobs with an asynchronous map
 
 Returns a results object which containts the results of applying the
 function f to the items of the argument sequence(s). If more than one
 sequence is given, the function is called with an argument list consisting
 of the corresponding item of each sequence. To retrieve the results, call
 the get() method on the returned results object. The call to get() is
 blocking, until all results are retrieved. Use the ready() method on the
-result object to check if all results are ready.
+result object to check if all results are ready. Some maps accept the
+`chunksize` keyword, which causes the sequence to be split into tasks of
+approximately the given size.
         """
        #self.__map(f, *args, **kwds)
         raise NotImplementedError
     ########################################################################
     # PIPES
     def pipe(self, f, *args, **kwds):
         """submit a job and block until results are available
```

### Comparing `mystic-0.4.0/mystic/abstract_sampler.py` & `mystic-0.4.1/mystic/abstract_sampler.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,58 +1,35 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2019-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2019-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 This module contains the base class for mystic samplers, and describes
 the mystic sampler interface.
 """
-__all__  = ['AbstractSampler']
+__all__ = ['AbstractSampler']
 
-"""
-# utility functions
-_reset_sampler: reset all
-_reset_solved: reset all solved
-_sample(reset): reset all/stop/none, then step
-
-# use cases to manage evals/iters
-_restart_all_without_step: _reset_sampler
-_restart_solved_without_step: _reset_solved
-_restart_all_then_step: _sample(reset=True)
-_restart_solved_then_step: _sample(reset=None)
-_step_without_restart: _sample(reset=False)
-
-# options
-_restart_if_solved(solved): (* = 'all' if all else 'solved')
-  . all: if all stop, _restart_*_then_step
-  . True: if best stop, _restart_*_then_step
-  . any: if any stop, _restart_*_then_step 
-  . False: if none stop, _restart_*_then_step
-  . None: _step_without_restart
-"""
 
 class AbstractSampler(object): # derived class per sampling algorithm
     """
 AbstractSampler base class for optimizer-directed samplers
     """
     def __init__(self, bounds, model, npts=None, **kwds):
         """
-        Inputs:
-         bounds -- list[tuples]: (lower,upper) bound for each model input
-         model -- function: y = model(x), where x is an input parameter vector
-         npts -- int: number of points to sample the model
-
-        NOTE:
-          additional keywords (evalmon, stepmon, maxiter, maxfun, dist,
-          saveiter, state, termination, constraints, penalty, reducer,
-          solver, tightrange, cliprange) are available for use.
-          See mystic.ensemble for more details.
-        """
+Args:
+  bounds (list[tuples]): (lower,upper) bound for each model input
+  model (function): ``y = model(x)``, where ``x`` is an input parameter vector
+  npts (int, default=None): number of points to sample the model
+  **kwds (dict, default={}): keywords for the underlying ensemble of solvers;
+    ``(evalmon, stepmon, maxiter, maxfun, dist, saveiter, state, termination,
+    constraints, penalty, reducer, solver, id, map, tightrange, cliprange)``
+    are available for use. See ``mystic.ensemble`` for more details.
+        """ #FIXME: added 'id' and 'map'
         self._bounds = bounds
         self._model = model #FIXME: if None, interpolate
         self._npts = npts
 
         self._evalmon = kwds.pop('evalmon', None)
         if self._evalmon is None:
             from mystic.monitors import Null
@@ -66,23 +43,25 @@
         s.SetStrictRanges(*zip(*bounds), **kwd)
         #s.SetObjective(memo) #model) #XXX: ExtraArgs: axis ???
         s.SetObjective(model) #FIXME: ensure cached model
 
         # apply additional kwds
         solver = self._kwds['solver']
         if solver is not None: s.SetNestedSolver(solver)
+        s.id = self._kwds['id']
         s.SetDistribution(self._kwds['dist'])
         s.SetEvaluationLimits(self._kwds['maxiter'], self._kwds['maxfun'])
         s.SetSaveFrequency(self._kwds['saveiter'], self._kwds['state'])
         termination = self._kwds['termination']
         if termination is not None: s.SetTermination(termination) #XXX:?
         s.SetConstraints(self._kwds['constraints'])
         s.SetPenalty(self._kwds['penalty'])
         s.SetReducer(self._kwds['reducer'], arraylike=True)
         s.SetGenerationMonitor(self._kwds['stepmon']) #XXX: use self._stepmon?
+        s.SetMapper(self._kwds['map']) #TODO: close/join/clear after Solve?
 
         # pass a copy of the monitor to all instances
         import copy
         m = copy.deepcopy(self._evalmon) #XXX: no change with direct reference
         s.SetEvaluationMonitor(m)
         self._sampler = s
         self._npts = s._npts
@@ -132,16 +111,20 @@
         s._AbstractEnsembleSolver__update_state()
         return
 
 
     def _sample(self, reset=False):#, **kwds):
         """collect a sample for each member in the ensemble
 
-        Inputs:
-         reset: if True, reset all before sampling; if None, reset terminated
+Args:
+  reset (bool, default=False): reset all solvers before sampling; alternately,
+    if ``reset`` is None, then only reset the terminated solvers
+
+Returns:
+  None
         """
         #NOTE: sample(reset_all) is like _sample(reset), with None <=> False
         s = self._sampler
         m = self._evalmon
 
         _eval = s._all_evals
         _iter = s._all_iters
@@ -167,29 +150,32 @@
             self._iters[i] += t
         return termination
 
 
     def sample(self, if_terminated=None, reset_all=True):#, **kwds):
         """sample npts using vectorized solvers
 
-        Input:
-         if_terminated: the amount of termination [all,True,any,False,None]
-         reset_all: action to take when if_terminated is met [True,False,None]
-
-        Note:
-         When if_terminated is all, reset if all solvers are terminated.
-         When if_terminated is any, reset if any solvers are terminated.
-         When if_terminated is True, reset if the best solver is terminated.
-         When if_terminated is False, reset if no solvers are terminated.
-         When if_terminated is None, reset regardless of termination [default].
-
-        Note:
-         If reset_all is True, reset all solvers if if_terminated is satisfied.
-         If reset_all is False, similarly reset only the terminated solvers.
-         If reset_all is None, never reset.
+Args:
+  if_terminated (bool, default=None): the amount of termination; must be one
+    of ``{all, True, any, False, None}``
+  reset_all (bool, default=True): action to take when ``if_terminated`` is met;
+    must be one of ``{True, False, None}``
+
+Returns:
+  None
+
+Notes:
+  - When ``if_terminated`` is None, reset regardless of termination.
+  - When ``if_terminated`` is True, reset if the best solver is terminated.
+  - When ``if_terminated`` is False, reset if no solvers are terminated.
+  - When ``if_terminated`` is all, reset if all solvers are terminated.
+  - When ``if_terminated`` is any, reset if any solvers are terminated.
+  - If ``reset_all`` is None, never reset.
+  - If ``reset_all`` is True, reset all solvers if ``if_terminated`` is met.
+  - If ``reset_all`` is False, similarly reset only the terminated solvers.
         """
         if type(reset_all) is bool:
             s = self._sampler
             if if_terminated is None: # reset regardless
                 return self._sample(reset=(True if reset_all else None))#, **kwds)
             if not if_terminated in (all, True, any, False):
                 msg = "%s not in (all, True, any, False, None)" % if_terminated
@@ -202,35 +188,40 @@
                 return self._sample(reset=(True if reset_all else None))#, **kwds)
             # othewise just take a step
             return self._sample(reset=False)#, **kwds)
         return self._sample(reset=False)#, **kwds)
 
 
     def sample_until(self, iters=None, evals=None, terminated=None, **kwds):
-        """sample until one of the three given conditions is met:
-        (iters() >= iters) or (evals() >= evals) or (# terminated > terminated)
+        """sample until one of the stop conditions are met
 
-        Input:
-         iters -- int: maximum number of iterations [default = inf]
-         evals -- int: maximum number of evaluations [default = inf]
-         terminated -- int: maximum number of stopped solvers [default = inf]
-
-        Additional Input:
-         if_terminated: the amount of termination [all,True,any,False,None]
-         reset_all: action to take when if_terminated is met [True,False,None]
-
-        Note:
-         The default sampler configuration is to always reset (reset_all=True).
-         If termination != None, the default is never reset (reset_all=None).
-         A limit has to be provided for either iters, evals, or termination.
-
-        Note:
-         terminated - {all: all, True: best, any: 1, False: 0, None: inf, N: N}
-         if_terminated - {all: all, True: best, any: 1, False: 0, None: always}
-         reset_all - {True: reset all, False: reset solved, None: never reset}
+Possible stop conditions are:
+  - solver iterations ``iters()`` equals or exceeds ``iters``
+  - solver evaluations ``evals()`` equals or exceeds ``evals``
+  - number of terminated solvers equals or exceeds ``terminated``
+
+Args:
+  iters (int, default=inf): maximum number of iterations
+  evals (int, default=inf): maximum number of evaluations
+  terminated (int, default=inf): maximum number of terminated solvers
+  if_terminated (bool, default=None): the amount of termination; must be one
+    of ``{all, True, any, False, None}``
+  reset_all (bool, default=True): action to take when ``if_terminated`` is met;
+    must be one of ``{True, False, None}``
+
+Notes:
+  - The default sampler configuration is to always reset (``reset_all=True``)
+  - If ``termination != None``, the default is never reset (``reset_all=None``)
+  - A limit for at least one of ``(iters, evals, termination)`` must be set.
+  - ``terminated`` may also be one of ``{all, True, any, False, None}``, where
+    ``{all: 'all', True: 'best', any: '1', False: '0', None: 'inf', N: 'N'}``
+  - ``if_terminated`` may be one of ``{all, True, any, False, None}``, where
+    ``{all: 'all', True: 'best', any: '1', False: '0', None: 'always'}``
+  - ``reset_all`` may be one of ``{True, False, None}``, where ``{True: 'reset
+    all', False: 'reset solved', None: 'never reset'}``
         """
         from numpy import inf, all as all_, any as any_
         if evals is None:
             evals = inf
         if iters is None:
             iters = inf
         if terminated is None:
@@ -269,46 +260,71 @@
         ###stop = self.terminated(**kwds)
         while self.iters() < iters and self.evals() < evals and (not self.terminated(all=False) if (terminated is True) else (sum(self.terminated(all=True)) < terminated)): #FIXME: sometimes limiting iters stops very late
             stop = self.sample(if_stop, reset)#, **kwds)
         return### stop
 
 
     def evals(self, all=False): #XXX: None?
-        """get the number of function evaluations
+        """get the total number of function evaluations
 
-        Input:
-          all -- bool: if True, get evals from the entire ensemble
+Args:
+  all (bool, default=False): report the ``evals`` for each ensemble member
         """
         if all:
             return self._evals
         return sum(self._evals)
 
 
     def iters(self, all=False): #XXX: None?
-        """get the number of solver iterations
+        """get the total number of solver iterations
 
-        Input:
-          all -- bool: if True, get iters from the entire ensemble
+Args:
+  all (bool, default=False): report the ``iters`` for each ensemble member
         """
         if all:
             return self._iters
         return sum(self._iters)
 
 
     def terminated(self, *args, **kwds): #FIXME: confusing wrt if_terminated?
-        """
-        Input:
-         all, disp, info
+        """check if termination conditions have been met
 
-        Note:
-         all - {True: show all, False: best terminated, None: all terminated}
-         disp - {True: show details, False: show less, 'verbose': show more}
-         info - {True: return info string, False: return bool}
+Args:
+  disp (bool, default=False): print termination statistics and/or warnings
+  info (bool, default=False): return termination message (instead of boolean)
+  all (bool, default=None): get results for all solvers, else get the 'best'
+
+Notes:
+  - ``disp`` expects a bool, but can also take ``'verbose'`` for more verbosity 
+  - ``all``, by default (i.e. None), will show only the terminated solvers
         """
         _all = kwds.get('all', None)
         if _all not in (True, False, None):
             msg = 'all = %s, must be one of (True, False, None)' % getattr(_all, '__name__', _all)
             raise ValueError(msg)
         kwds['all'] = _all
         return self._sampler.Terminated(*args, **kwds)
 
 
+"""
+### Notes ###
+
+# utility functions
+_reset_sampler: reset all
+_reset_solved: reset all solved
+_sample(reset): reset all/stop/none, then step
+
+# use cases to manage evals/iters
+_restart_all_without_step: _reset_sampler
+_restart_solved_without_step: _reset_solved
+_restart_all_then_step: _sample(reset=True)
+_restart_solved_then_step: _sample(reset=None)
+_step_without_restart: _sample(reset=False)
+
+# options
+_restart_if_solved(solved): (* = 'all' if all else 'solved')
+. all: if all stop, _restart_*_then_step
+. True: if best stop, _restart_*_then_step
+. any: if any stop, _restart_*_then_step 
+. False: if none stop, _restart_*_then_step
+. None: _step_without_restart
+"""
```

### Comparing `mystic-0.4.0/mystic/abstract_solver.py` & `mystic-0.4.1/mystic/abstract_solver.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 ## Abstract Solver Class
 # derived from Patrick Hung's original DifferentialEvolutionSolver
 """
 This module contains the base class for mystic solvers, and describes
@@ -334,15 +334,15 @@
 additional input::
     - tight (bool): if True, apply bounds concurrent with other constraints
     - clip (bool): if True, bounding constraints will clip exterior values
 
 note::
     SetStrictRanges(None) will remove strict range constraints
 
-notes::
+note::
     By default, the bounds are coupled to the other constraints with a coupler
     (e.g. ``mystic.coupler.outer``), and not applied concurrently (i.e. with
     ``mystic.constraints.and_``). Using a coupler favors speed over robustness,
     and relies on the user to formulate the constraints so they do not conflict
     with imposing the bounds.
 
 note::
@@ -458,20 +458,24 @@
         if at: return x_
         # clip x0 within bounds
         x_ = x_ != x0
         x0[x_] = random.uniform(self._strictMin,self._strictMax)[x_]
         return x0
 
     def SetInitialPoints(self, x0, radius=0.05):
-        """Set Initial Points with Guess (x0)
+        """Set Initial Points with Guess (``x0``)
 
-input::
-    - x0: must be a sequence of length self.nDim
-    - radius: generate random points within [-radius*x0, radius*x0]
-        for i!=0 when a simplex-type initial guess in required"""
+Args:
+    x0 (list[float]): a sequence of length ``self.nDim``
+    radius (float): generate random points within ``[-radius*x0, radius*x0]``
+        for ``i!=0`` when a simplex-type initial guess is required
+
+Returns:
+    None
+        """
         x0 = asfarray(x0)
         rank = len(x0.shape)
         if rank == 0:
             x0.shape = (1,)
             rank = 1
         if not -1 < rank < 2:
             raise ValueError("Initial guess must be a scalar or rank-1 sequence.")
@@ -492,17 +496,24 @@
         self.SetRandomInitialPoints(min,max)
         #stick initial values in population[i], i=0
         self.population[0][:] = x0.tolist()
     
     def SetRandomInitialPoints(self, min=None, max=None):
         """Generate Random Initial Points within given Bounds
 
-input::
-    - min, max: must be a sequence of length self.nDim
-    - each min[i] should be <= the corresponding max[i]"""
+Args:
+    min (list[float], default=None): lower bounds, list of length ``self.nDim``
+    max (list[float], default=None): upper bounds, list of length ``self.nDim``
+
+Returns:
+    None
+
+Notes:
+    - each ``min[i]`` must be less than or equal to the corresponding ``max[i]``
+        """
         if min is None: min = self._defaultMin
         if max is None: max = self._defaultMax
        #if numpy.any(( asarray(min) > asarray(max) ),0):
        #    raise ValueError, "each min[i] must be <= the corresponding max[i]"
         if len(min) != self.nDim or len(max) != self.nDim:
             raise ValueError("bounds array must be length %s" % self.nDim)
         # when 'some' of the bounds are given as 'None', replace with default
@@ -513,20 +524,25 @@
         for i in range(len(self.population)):
             for j in range(self.nDim):
                 self.population[i][j] = random.uniform(min[j],max[j])
 
     def SetMultinormalInitialPoints(self, mean, var=None):
         """Generate Initial Points from Multivariate Normal.
 
-input::
-    - mean must be a sequence of length self.nDim
-    - var can be...
-        None: -> it becomes the identity
-        scalar: -> var becomes scalar * I
-        matrix: -> the variance matrix. must be the right size!
+Args:
+    mean (list[float]): mean values, list of length ``self.nDim``
+    var (ndarray[float,float], default=None): covariance matrix
+
+Returns:
+    None
+
+Notes:
+    - ``var`` must be symmetric, positive-semidefinite, and length ``self.nDim``
+    - if ``var`` is None, then ``var`` becomes the Identity matrix, ``I``
+    - if ``var`` is a scalar, then ``var`` is set to ``var * I``
         """
         from mystic.tools import random_state
         rng = random_state(module='numpy.random')
         assert(len(mean) == self.nDim)
         if var is None:
             var = numpy.eye(self.nDim)
         else:
@@ -539,17 +555,23 @@
         for i in range(len(self.population)):
             self.population[i] = rng.multivariate_normal(mean, var).tolist()
         return
 
     def SetSampledInitialPoints(self, dist=None):
         """Generate Random Initial Points from Distribution (dist)
 
-input::
-    - dist: a mystic.math.Distribution instance
-"""
+Args:
+    dist (Distribution, default=None): a mystic.math.Distribution instance
+
+Returns:
+    None
+
+Notes:
+    - if ``dist`` is None, use a uniform distribution in the interval ``[0, 1)``
+        """
         from mystic.math import Distribution
         _dist = Distribution()
         if dist is None:
             dist = _dist
         elif type(_dist) not in dist.__class__.mro():
             dist = Distribution(dist) #XXX: or throw error?
         for i in range(self.nPop): #FIXME: accept a list of Distributions
@@ -613,20 +635,23 @@
             else:
                 self._maxfun = "*"
         return
 
     def _SetEvaluationLimits(self, iterscale=None, evalscale=None):
         """set the evaluation limits
 
-input::
-    - iterscale and evalscale are integers used to set the maximum iteration
+Args:
+    iterscale (int, default=10): scale factor for iteration upper limit
+    evalscale (int, default=1000): scale factor for evaluation upper limit
+
+Notes:
+    - ``iterscale`` and ``evalscale`` are used to set the maximum iteration
       and evaluation limits, respectively. The new limit is defined as
-      limit = (nDim * nPop * scale) + count, where count is the number
-      of existing iterations or evaluations, respectively. The default for
-      iterscale is 10, while the default for evalscale is 1000.
+      ``limit = (nDim * nPop * scale) + count``, where ``count`` is the number
+      of existing iterations or evaluations, respectively.
         """
         if iterscale is None: iterscale = 10
         if evalscale is None: evalscale = 1000
         N = len(self.population[0]) # usually self.nDim
         # if SetEvaluationLimits not applied, use the solver default
         if self._maxiter is None:
             self._maxiter = N * self.nPop * iterscale
@@ -637,22 +662,26 @@
         elif self._maxfun == "*":
             self._maxfun = (N * self.nPop * evalscale) + self.evaluations
         return
 
     def Terminated(self, disp=False, info=False, termination=None, **kwds):
         """check if the solver meets the given termination conditions
 
-Input::
-    - disp = if True, print termination statistics and/or warnings
-    - info = if True, return termination message (instead of boolean)
-    - termination = termination conditions to check against
-
-Notes::
-    If no termination conditions are given, the solver's stored
-    termination conditions will be used.
+Args:
+    disp (bool, default=False): print termination statistics and/or warnings
+    info (bool, default=False): return termination message (instead of boolean)
+    termination (termination, default=None): termination conditions to check
+
+Returns:
+    information about the state of the solver termination (see Notes)
+
+Notes:
+    - if ``info`` is False, return a bool regarding the termination
+    - if ``info`` is True, return an informative string about the termination
+    - if ``termination`` is None, the solver's stored termination is be used
         """
         if termination is None:
             termination = self._termination
         # ensure evaluation limits have been imposed
         self._SetEvaluationLimits()
         # check for termination messages
         msg = termination(self, info=True)
@@ -672,15 +701,15 @@
                 print("Warning: Maximum number of iterations has been exceeded")
         elif self._EARLYEXIT:
             msg = sig
             if disp:
                 print("Warning: Optimization terminated with signal interrupt.")
         elif msg and disp:
             print("Optimization terminated successfully.")
-            print("         Current function value: %f" % self.bestEnergy)
+            print("         Current function value: %s" % self.bestEnergy)
             print("         Iterations: %d" % self.generations)
             print("         Function evaluations: %d" % self._fcalls[0])
 
         if info:
             return msg
         return bool(msg)
 
@@ -716,32 +745,40 @@
             return
         # get cost and args if None was given
         if cost is None: cost = _raw
         args = _args if ExtraArgs is None else ExtraArgs
         args = () if args is None else args
         # quick validation check (so doesn't screw up internals)
         if not isvalid(cost, [0]*self.nDim, *args):
-            try: name = cost.__name__
+            try: call = cost.__call__
             except AttributeError: # raise new error for non-callables
                 cost(*args)
             validate(cost, None, *args)
            #val = len(args) + 1  #XXX: 'klepto.validate' for better error?
            #msg = '%s() invalid number of arguments (%d given)' % (name, val)
            #raise TypeError(msg)
         # hold on to the 'raw' cost function
         self._cost = (None, cost, ExtraArgs)
         self._live = False
         return
 
     def Collapsed(self, disp=False, info=False):
         """check if the solver meets the given collapse conditions
 
-Input::
-    - disp: if True, print details about the solver state at collapse
-    - info: if True, return collapsed state (instead of boolean)"""
+Args:
+    disp (bool, default=False): print details about the solver state at collapse
+    info (bool, default=False): return collapsed state (instead of boolean)
+
+Returns:
+    information about the state of the solver collapse (see Notes)
+
+Notes:
+    - if ``info`` is False, return a bool regarding the collapse
+    - if ``info`` is True, return an informative string about the collapse
+        """
         stop = getattr(self, '__stop__', self.Terminated(info=True))
         import mystic.collapse as ct
         collapses = ct.collapsed(stop) or dict()
         if collapses and disp:
             for (k,v) in collapses.items():
                 print("         %s: %s" % (k.split()[0],v))
            #print("# Collapse at: Generation", self._stepmon._step-1, \
@@ -804,21 +841,26 @@
         if npts: #XXX: faster/better if comes first or last?
             conditions += [cn.impose_measure( npts, [collapses[k] for k in collapses if k.startswith('CollapsePosition')], [collapses[k] for k in collapses if k.startswith('CollapseWeight')] )]
         # get updated constraints
         return to.chain(*conditions)(self._constraints)
 
     def Collapse(self, disp=False):
         """if solver has terminated by collapse, apply the collapse
-        (unless both collapse and "stop" are simultaneously satisfied)
 
-input::
-    - disp: if True, print details about the solver state at collapse
+Args:
+    disp (bool, default=False): print details about the solver state at collapse
 
-note::
-    updates the solver's termination conditions and constraints
+Returns:
+    a dict of ``{info: collapse}``, where ``info`` is collapse termination info
+
+Notes:
+    - updates the solver's termination conditions and constraints
+    - collapse must be triggered by calling this method, unless both the
+      "collapse" termination and a "stop" termination are simultaneously
+      satisfied.
         """
        #XXX: return True for "collapse and continue" and False otherwise?
         collapses = self.__get_collapses(disp)
         if collapses: # then stomach a bunch of module imports (yuck)
             state, termination = self.__collapse_termination(collapses)
             constraints = self.__collapse_constraints(state, collapses)
             # update termination and constraints in solver
@@ -838,18 +880,23 @@
         else: # delay update until _bootstrap
             self.Finalize()
         return
 
     def _decorate_objective(self, cost, ExtraArgs=None):
         """decorate the cost function with bounds, penalties, monitors, etc
 
-input::
-    - cost is the objective function, of the form y = cost(x, *ExtraArgs),
-      where x is a candidate solution, and ExtraArgs is the tuple of positional
-      arguments required to evaluate the objective."""
+Args:
+    cost (func): objective, of form ``y = cost(x, *ExtraArgs)``, where ``x``
+      is a candidate solution vector
+    ExtraArgs (tuple, default=None): tuple of positional arguments required to
+      evaluate the objective
+
+Returns:
+    decorated objective function
+        """
         #print("@%r %r %r" % (cost, ExtraArgs, max))
         evalmon = self._evalmon
         raw = cost
         if ExtraArgs is None: ExtraArgs = ()
         self._fcalls, cost = wrap_function(cost, ExtraArgs, evalmon)
         if self._useStrictRange:
             indx = list(self.popEnergy).index(self.bestEnergy)
@@ -885,20 +932,29 @@
         # 'wrap' the 'new' cost function with _decorate
         self.SetObjective(cost, ExtraArgs)
         return self._decorate_objective(*self._cost[1:])
 
     def _Step(self, cost=None, ExtraArgs=None, **kwds):
         """perform a single optimization iteration
 
-input::
-    - cost is the objective function, of the form y = cost(x, *ExtraArgs),
-      where x is a candidate solution, and ExtraArgs is the tuple of positional
-      arguments required to evaluate the objective.
+Args:
+    cost (func, default=None): objective, of form ``y = cost(x, *ExtraArgs)``,
+      where ``x`` is a candidate solution vector
+    ExtraArgs (tuple, default=None): tuple of positional arguments required to
+      evaluate the objective
 
-*** this method must be overwritten ***"""
+Returns:
+    None
+
+Notes:
+    - This method accepts additional ``kwds`` that are specific for the current
+      solver, as detailed in the ``_process_inputs`` method.
+
+NOTE:
+    *** this method must be overwritten ***"""
         raise NotImplementedError("an optimization algorithm was not provided")
 
     def SaveSolver(self, filename=None, **kwds):
         """save solver state to a restart file
 
 input::
     - filename: string of full filepath for the restart file
@@ -957,29 +1013,29 @@
         return
 
     def _process_inputs(self, kwds):
         """process and activate input settings
 
 Args:
     callback (func, default=None): function to call after each iteration. The
-        interface is ``callback(xk)``, with xk the current parameter vector.
+        interface is ``callback(xk)``, with ``xk`` the current parameter vector.
     disp (bool, default=False): if True, print convergence messages.
+    EvaluationMonitor (monitor, default=None): a monitor instance to capture
+        each evaluation of cost.
+    StepMonitor (monitor, default=None): a monitor instance to capture each
+        iteration's best results.
+    penalty (penalty, default=None): function of the form: ``y' = penalty(xk)``,
+        with ``y = cost(xk) + y'`` and ``xk`` is the current parameter vector.
+    constraints (constraint, default=None): function of the form:
+        ``xk' = constraints(xk)``, where ``xk`` is the current parameter vector.
 
-Additional Args:
-    EvaluationMonitor: a monitor instance to capture each evaluation of cost.
-    StepMonitor: a monitor instance to capture each iteration's best results.
-    penalty: a function of the form: y' = penalty(xk), with y = cost(xk) + y',
-        where xk is the current parameter vector.
-    constraints: a function of the form: xk' = constraints(xk), where xk is
-        the current parameter vector.
-
-Note:
-   The additional args are 'sticky', in that once they are given, they remain
-   set until they are explicitly changed. Conversely, the args are not sticky,
-   and are thus set for a one-time use.
+Notes:
+    - ``callback`` and ``disp`` are 'sticky', in that once they are given, they
+      remain set until they are explicitly changed. Conversely, the other inputs
+      are not sticky, and are thus set for a one-time use.
         """
         #allow for inputs that don't conform to AbstractSolver interface
         #NOTE: not sticky: callback, disp
         #NOTE: sticky: EvaluationMonitor, StepMonitor, penalty, constraints
         settings = \
        {'callback':None,     #user-supplied function, called after each step
         'disp':0}            #non-zero to print convergence messages
@@ -1009,24 +1065,22 @@
         interface is ``callback(xk)``, with xk the current parameter vector.
     disp (bool, default=False): if True, print convergence messages.
 
 Returns:
     None
 
 Notes:
-    To run the solver until termination, call ``Solve()``. Alternately, use
-    ``Terminated()`` as the stop condition in a while loop over ``Step``.
-
-    If the algorithm does not meet the given termination conditions after
-    the call to ``Step``, the solver may be left in an "out-of-sync" state.
-    When abandoning an non-terminated solver, one should call ``Finalize()``
-    to make sure the solver is fully returned to a "synchronized" state.
-
-    This method accepts additional args that are specific for the current
-    solver, as detailed in the `_process_inputs` method.
+    - To run the solver until termination, call ``Solve()``. Alternately, use
+      ``Terminated()`` as the stop condition in a while loop over ``Step``.
+    - If the algorithm does not meet the given termination conditions after
+      the call to ``Step``, the solver may be left in an "out-of-sync" state.
+      When abandoning an non-terminated solver, one should call ``Finalize()``
+      to make sure the solver is fully returned to a "synchronized" state.
+    - This method accepts additional args that are specific for the current
+      solver, as detailed in the ``_process_inputs`` method.
         """
         if 'disp' in kwds:
             disp = bool(kwds['disp'])#; del kwds['disp']
         else: disp = False
 
         # register: cost, termination, ExtraArgs
         cost = self._bootstrap_objective(cost, ExtraArgs)
@@ -1052,15 +1106,15 @@
 
     def _Solve(self, cost, ExtraArgs, **settings):
         """Run the optimizer to termination, using the given settings.
 
 Args:
     cost (func): the function to be minimized: ``y = cost(x)``.
     ExtraArgs (tuple): tuple of extra arguments for ``cost``.
-    settings (dict): optimizer settings (produced by _process_inputs)
+    settings (dict): optimizer settings (produced by ``_process_inputs``)
 
 Returns:
     None
         """
         disp = settings['disp'] if 'disp' in settings else False
 
         # the main optimization loop
```

### Comparing `mystic-0.4.0/mystic/bounds.py` & `mystic-0.4.1/mystic/bounds.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 cartesian bounds and measure bounds instances
 """
 __all__ = ['Bounds','MeasureBounds']
 
@@ -20,25 +20,25 @@
     bounds is a tuple of (lower, upper) bound
 
     additionally, one can specify:
         - xlb: lower bound
         - xub: upper bound
         - n: repeat
 
-    For example:
+    Examples:
         >>> b = Bounds(7, 8, n=2)
         >>> b.xlb, b.xub
         (7, 8)
         >>> b()
         [(7, 8), (7, 8)]
         >>> b.lower
         [7, 7]
         >>> b.upper
         [8, 8]
-        >>> 
+
         >>> c = Bounds((0,1),(3,4), n=2)
         >>> c()
         [(0, 3), (0, 3), (1, 4), (1, 4)]
         """
         self.n = kwds.pop('n', 1)
         self.wub = None # 1.0
         self.wlb = None # 1.0
@@ -74,14 +74,19 @@
         if hasattr(self.xub, '__len__') and not hasattr(self.n, '__len__'):
             self.n = len(self.xub) * (self.n,)
         # single xlb,xub stretched to n
         elif hasattr(self.n, '__len__') and not hasattr(self.xub, '__len__'):
             self.xub = len(self.n) * (self.xub,)
             self.xlb = len(self.n) * (self.xlb,)
 
+    def __len__(self):
+        "get length of list of tuples of (lower, upper) bounds"
+        n = (self.n,) if not hasattr(self.n, '__len__') else self.n
+        return sum(n)
+
     def __lower(self):
         "get list of lower bounds"
         n = (self.n,) if not hasattr(self.n, '__len__') else self.n
         xlb = (self.xlb,) if not hasattr(self.xlb, '__len__') else self.xlb
         return list(flatten(i*[j] for i,j in zip(n,xlb)))
 
     def __upper(self):
@@ -91,14 +96,15 @@
         return list(flatten(i*[j] for i,j in zip(n,xub)))
 
     def __call__(self):
         "get list of tuples of (lower, upper) bounds"
         return list(zip(self.lower, self.upper))
 
     def __add__(self, other): #FIXME: create new Bounds instance
+        "add the contents of self and the given other bounds"
         if not isinstance(other, Bounds):
             return NotImplemented
         return self() + other()
 
     def __set_lower(self, lb):
         return NotImplemented
 
@@ -129,35 +135,35 @@
     additionally, one can specify:
         - wlb: weight lower bound
         - wub: weight upper bound
         - xlb: lower bound
         - xub: upper bound
         - n: repeat
 
-    For example:
+    Examples:
         >>> b = MeasureBounds(7, 8, n=2)
         >>> b.wlb, b.wub
         (0, 1)
         >>> b.xlb, b.xub
         (7, 8)
         >>> b()
         [(0, 1), (0, 1), (7, 8), (7, 8)]
         >>> b.lower
         [0, 0, 7, 7]
         >>> b.upper
         [1, 1, 8, 8]
-        >>> 
+
         >>> c = MeasureBounds((0,1),(4,5), n=1, wlb=(0,1), wub=(2,3))
         >>> c.lower
         [0, 0, 1, 1]
         >>> c.upper
         [2, 4, 3, 5]
         >>> c()
         [(0, 2), (0, 4), (1, 3), (1, 5)]
-        >>> 
+
         >>> c = MeasureBounds((0,1),(4,5), n=2)
         >>> c()
         [(0, 1), (0, 1), (0, 4), (0, 4), (0, 1), (0, 1), (1, 5), (1, 5)]
         """
         super(MeasureBounds, self).__init__(*bounds, **kwds)
         self.wub = kwds.pop('wub', 1)
         self.wlb = kwds.pop('wlb', 0)
@@ -171,21 +177,27 @@
             self.wlb = len(self.xlb) * (self.wlb,)
             self.wub = len(self.xub) * (self.wub,)
         elif hasattr(self.wlb, '__len__') and not hasattr(self.xlb, '__len__'):
             self.n = len(self.wlb) * (self.n,)
             self.xlb = len(self.wlb) * (self.xlb,)
             self.xub = len(self.wub) * (self.xub,)
 
+    def __len__(self):
+        "get length of list of tuples of (lower, upper) bounds"
+        return 2 * super(MeasureBounds, self).__len__()
+
     def __lower(self):
+        "get list of lower bounds"
         n = (self.n,) if not hasattr(self.n, '__len__') else self.n
         wlb = (self.wlb,) if not hasattr(self.wlb, '__len__') else self.wlb
         xlb = (self.xlb,) if not hasattr(self.xlb, '__len__') else self.xlb
         return list(flatten(i*[j] + i*[k] for i,j,k in zip(n,wlb,xlb)))
 
     def __upper(self):
+        "get list of upper bounds"
         n = (self.n,) if not hasattr(self.n, '__len__') else self.n
         wub = (self.wub,) if not hasattr(self.wub, '__len__') else self.wub
         xub = (self.xub,) if not hasattr(self.xub, '__len__') else self.xub
         return list(flatten(i*[j] + i*[k] for i,j,k in zip(n,wub,xub)))
 
     def __wlower(self):
         n = (self.n,) if not hasattr(self.n, '__len__') else self.n
@@ -204,14 +216,15 @@
 
     def __xupper(self):
         n = (self.n,) if not hasattr(self.n, '__len__') else self.n
         xub = (self.xub,) if not hasattr(self.xub, '__len__') else self.xub
         return list(flatten(i*[k] for i,k in zip(n,xub)))
 
     def __add__(self, other): #FIXME: create new MeasureBounds instance
+        "add the contents of self and the given other bounds"
         if not isinstance(other, Bounds):
             return NotImplemented
         return self() + other()
 
     def __set_lower(self, lb):
         return NotImplemented
```

### Comparing `mystic-0.4.0/mystic/cache/__init__.py` & `mystic-0.4.1/mystic/cache/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''decorators for caching function outputs, with function inputs as the keys,
 and interactors for reading and writing to databases of functions and data.
 
 several klepto.cache strategies are included here for backward compatability;
 please also see the klepto package for available archives (i.e. dir_archive,
```

### Comparing `mystic-0.4.0/mystic/cache/archive.py` & `mystic-0.4.1/mystic/cache/archive.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2019-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2019-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''klepto archive readers and writers, for functions and data
 '''
 from klepto.archives import (dict_archive, dir_archive, file_archive,
                              hdf_archive, hdfdir_archive, null_archive,
                              sql_archive, sqltable_archive)
```

### Comparing `mystic-0.4.0/mystic/cache/function.py` & `mystic-0.4.1/mystic/cache/function.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2019-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2019-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''higher-level readers and writers for stored functions
 '''
 
 __all__ = ['db','write','read']
```

### Comparing `mystic-0.4.0/mystic/collapse.py` & `mystic-0.4.1/mystic/collapse.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Lan Huong Nguyen (lanhuong @stanford)
 # Copyright (c) 2012-2015 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import mystic.monitors as _m
 inf = _m.numpy.inf
 
 ##### parameter collapse detectors #####
```

### Comparing `mystic-0.4.0/mystic/constraints.py` & `mystic-0.4.1/mystic/constraints.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,44 +1,48 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """Tools for building and applying constraints and penalties.
 """
 
 __all__ = ['with_penalty','with_constraint','as_penalty','as_constraint',
            'with_mean','with_variance','with_std','with_spread','normalized',
-           'issolution','solve','discrete','integers','near_integers',
-           'unique','has_unique','impose_unique','bounded','impose_bounds',
-           'impose_as','impose_at','impose_measure','impose_position',
-           'impose_weight','and_','or_','not_','vectorize','boundsconstrain']
+           'issolution','solve','discrete','integers','rounded','precision',
+           'near_integers','unique','has_unique','impose_unique','bounded',
+           'impose_bounds','impose_as','impose_at','impose_measure',
+           'impose_position','impose_weight','and_','or_','not_','vectorize',
+           'boundsconstrain']
 
 from mystic.math.measures import *
 from mystic.math import almostEqual
 
 def vectorize(constraint, axis=1):
-    """vectorize a constraint for 2D input, `x' = k(x)` where `x` is 2D
+    """vectorize a 1D constraint function ``x' = c(x)`` for 2D input and output
 
-    Input:
-        constraint -- a mystic constraint, c, where `x' = c(x)`, `x` is a list
-        axis -- axis to apply constraints to, must be 0 or 1 (default is 1)
-
-    Output:
-        transform -- a transform function, k, where `x' = k(x)`, `x` is 2D array
+    Args:
+        constraint (function): a function ``c``, where ``x' = c(x)`` with ``x``
+          and ``x'`` lists of the same length
+        axis (int, default=1): index of the axis of ``x`` to apply constraints;
+          must be either 0 or 1
+
+    Returns:
+        a function ``k``, where ``x' = k(x)`` with ``x`` and ``x'`` 2D arrays
+          of the same shape
 
     Notes:
-        Produces a constraints function that is of the form required by
-        sklearn.preprocessing.FunctionTransformer(func=transform).
-        Input to the tranform is a 2D numpy array of shape (samples, features).
+        - Produces a ``transform`` function that is of the form required by
+          ``sklearn.preprocessing.FunctionTransformer(func=transform)``, and
+          takes a ``numpy`` array of shape ``(samples, features)`` as input.
 
-    For example:
+    Examples:
         >>> from mystic.constraints import (impose_bounds, integers,
         ...                                 with_mean, and_)
         >>> cons = and_(impose_bounds([(0,5),(7,10)])(lambda x:x),
         ...             integers()(lambda x:x), with_mean(6.0)(lambda x:x))
         >>> import numpy as np
         >>> data = np.random.randn(6,4)
         >>> c = vectorize(cons, axis=0)
@@ -88,15 +92,15 @@
 
 def with_penalty(ptype, *args, **kwds):
     """convert a condition to a penalty function of the chosen type
 
 condition f(x) is satisfied when f(x) == 0.0 for equality constraints
 and f(x) <= 0.0 for inequality constraints. ptype is a mystic.penalty type.
 
-    For example:
+Examples:
     >>> @with_penalty(quadratic_equality, kwds={'target':5.0})
     ... def penalty(x, target):
     ...   return mean(x) - target
     >>> 
     >>> penalty([1,2,3,4,5])
     400.0
     >>> penalty([3,4,5,6,7])
@@ -115,15 +119,15 @@
 #XXX: better: wrap_constraint( constraint, func, ctype=inner) ?
 def with_constraint(ctype, *args, **kwds): #XXX: is this *at all* useful?
     """convert a set transformation to a constraints solver of the chosen type
 
 transformation f(x) is a mapping between x and x', where x' = f(x).
 ctype is a mystic.coupler type [inner, outer, inner_proxy, outer_proxy].
 
-    For example:
+Examples:
     >>> @with_constraint(inner, kwds={'target':5.0})
     ... def constraint(x, target):
     ...   return impose_mean(target, x)
     ... 
     >>> x = constraint([1,2,3,4,5])
     >>> print(x)
     [3.0, 4.0, 5.0, 6.0, 7.0]
@@ -158,15 +162,15 @@
 Inputs:
     target -- the target mean
 
 A constraints function takes an iterable x as input, returning a modified x.
 This function is an "outer" coupling of "impose_mean" onto another constraints
 function c(x), such that:  x' = impose_mean(target, c(x)).
 
-    For example:
+Examples:
     >>> @with_mean(5.0)
     ... def constraint(x):
     ...   x[-1] = x[0]
     ...   return x
     ... 
     >>> x = constraint([1,2,3,4])
     >>> print(x)
@@ -192,15 +196,15 @@
 Inputs:
     target -- the target variance
 
 A constraints function takes an iterable x as input, returning a modified x.
 This function is an "outer" coupling of "impose_variance" onto another
 constraints function c(x), such that:  x' = impose_variance(target, c(x)).
 
-    For example:
+Examples:
     >>> @with_variance(1.0)
     ... def constraint(x):
     ...   x[-1] = x[0]
     ...   return x
     ... 
     >>> x = constraint([1,2,3])
     >>> print(x)
@@ -226,15 +230,15 @@
 Inputs:
     target -- the target standard deviation
 
 A constraints function takes an iterable x as input, returning a modified x.
 This function is an "outer" coupling of "impose_std" onto another
 constraints function c(x), such that:  x' = impose_std(target, c(x)).
 
-    For example:
+Examples:
     >>> @with_std(1.0)
     ... def constraint(x):
     ...   x[-1] = x[0]
     ...   return x
     ... 
     >>> x = constraint([1,2,3])
     >>> print(x)
@@ -251,15 +255,15 @@
 Inputs:
     target -- the target range
 
 A constraints function takes an iterable x as input, returning a modified x.
 This function is an "outer" coupling of "impose_spread" onto another constraints
 function c(x), such that:  x' = impose_spread(target, c(x)).
 
-    For example:
+Examples:
     >>> @with_spread(10.0)
     ... def constraint(x):
     ...   return [i**2 for i in x]
     ... 
     >>> x = constraint([1,2,3,4])
     >>> print(x)
     [3.1666666666666665, 5.1666666666666661, 8.5, 13.166666666666666]
@@ -285,15 +289,15 @@
 Inputs:
     mass -- the target sum of normalized weights
 
 A constraints function takes an iterable x as input, returning a modified x.
 This function is an "outer" coupling of "normalize" onto another constraints
 function c(x), such that:  x' = normalize(c(x), mass).
 
-    For example:
+Examples:
     >>> @normalized()
     ... def constraint(x):
     ...   return x
     ... 
     >>> constraint([1,2,3])
     [0.16666666666666666, 0.33333333333333331, 0.5]
     """
@@ -313,24 +317,24 @@
     """Returns whether the guess is a solution to the constraints
 
 Input:
     constraints -- a constraints solver function or a penalty function
     guess -- list of parameter values proposed to solve the constraints
     tol -- residual error magnitude for which constraints are considered solved
 
-    For example:
+Examples:
     >>> @normalized()
     ... def constraint(x):
     ...   return x
     ... 
     >>> constraint([.5,.5])
     [0.5, 0.5]
     >>> issolution(constraint, [.5,.5])
     True
-    >>> 
+
     >>> from mystic.penalty import quadratic_inequality
     >>> @quadratic_inequality(lambda x: x[0] - x[1] + 10)
     ... def penalty(x):
     ...   return 0.0
     ... 
     >>> penalty([-10,.5])
     0.0
@@ -687,27 +691,29 @@
 from numpy import shape, broadcast, empty, atleast_1d
 #from random import sample, choice
 def discrete(samples, index=None):
     """impose a discrete set of input values for the selected function
 
 The function's input will be mapped to the given discrete set
 
->>> @discrete([1.0, 2.0])
-... def identity(x):
-...     return x
-
->>> identity([0.123, 1.789, 4.000])
-[1.0, 2.0, 2.0]
-
->>> @discrete([1,3,5,7], index=(0,3))
-... def squared(x):
-....    return [i**2 for i in x]
+Examples:
+    >>> @discrete([1.0, 2.0])
+    ... def identity(x):
+    ...     return x
+    ...
+    >>> identity([0.123, 1.789, 4.000])
+    [1.0, 2.0, 2.0]
 
->>> squared([0,2,4,6,8,10])
-[1, 4, 16, 25, 64, 100]"""
+    >>> @discrete([1,3,5,7], index=(0,3))
+    ... def squared(x):
+    ...     return [i**2 for i in x]
+    ...
+    >>> squared([0,2,4,6,8,10])
+    [1, 4, 16, 25, 64, 100]
+    """
     samples = [asarray(samples)]
     samples[0].sort()
     if isinstance(index, int): index = (index,)
     index = [index]
 
     #XXX: refactor to use points_factory(samples)
     def _points(alist):
@@ -784,27 +790,29 @@
 def integers(ints=True, index=None):
     """impose the set of integers (by rounding) for the given function
 
 The function's input will be mapped to the ints, where:
   - if ints is True, return results as ints; otherwise, use floats
   - if index tuple provided, only round at the given indices
 
->>> @integers()
-... def identity(x):
-...     return x
-
->>> identity([0.123, 1.789, 4.000])
-[0, 2, 4]
-
->>> @integers(ints=float, index=(0,3,4))
-... def squared(x):
-....    return [i**2 for i in x]
-
->>> squared([0.12, 0.12, 4.01, 4.01, 8, 8])
-[0.0, 0.0144, 16.080099999999998, 16.0, 64.0, 64.0]"""
+Examples:
+  >>> @integers()
+  ... def identity(x):
+  ...     return x
+  ...
+  >>> identity([0.123, 1.789, 4.000])
+  [0, 2, 4]
+
+  >>> @integers(ints=float, index=(0,3,4))
+  ... def squared(x):
+  ...     return [i**2 for i in x]
+  ...
+  >>> squared([0.12, 0.12, 4.01, 4.01, 8, 8])
+  [0.0, 0.0144, 16.080099999999998, 16.0, 64.0, 64.0]
+    """
     #HACK: allow ints=False or ints=int
     _ints = [(int if ints else float) if isinstance(ints, bool) else ints]
     if isinstance(index, int): index = (index,)
     index = [index]
 
     def _index(alist=None):
         index[0] = alist
@@ -833,48 +841,173 @@
             return f(xtype(xp), *args, **kwds)
         func.index = _index
         func.type = _type
         return func
     return dec
 
 
+def rounded(digits=None, index=None):
+    """rounded inputs for the given function
+
+The function's input will be mapped to the given precision, where:
+  - digits is an int that sets the rounding precision (can be negative)
+  - if index tuple provided, only round at the given indices
+
+Examples:
+  >>> @rounded()
+  ... def identity(x):
+  ...     return x
+  ...
+  >>> identity([0.123, 1.789, 4.000])
+  [0.0, 2.0, 4.0]
+
+  >>> @rounded(digits=1, index=(0,3,4))
+  ... def squared(x):
+  ...     return [i**2 for i in x]
+  ...
+  >>> squared([123.45, 123.45, 4.01, 4.01, 0.012, 0.012])
+  [15227.560000000001, 15239.9025, 16.080099999999998, 16.0, 0.0, 0.000144]
+
+  >>> @rounded(digits=-1, index=(0,3,4))
+  ... def square(x):
+  ...     return [i**2 for i in x]
+  ...
+  >>> square([123.45, 123.45, 4.01, 4.01, 0.012, 0.012])
+  [14400.0, 15239.9025, 16.080099999999998, 0.0, 0.0, 0.000144]
+    """
+    digits = [digits or 0]
+    if isinstance(index, int): index = (index,)
+    index = [index]
+
+    def _index(alist=None):
+        index[0] = alist
+
+    def _digits(aint=None):
+        digits[0] = aint or 0
+
+    def dec(f):
+        def func(x,*args,**kwds):
+            if isinstance(x, ndarray): xtype = asarray
+            else: xtype = type(x)
+            xp = round(x, digits[0])
+            if index[0] is None:
+                mask = ones(xp.size, dtype=bool)
+            else:
+                mask = zeros(xp.size, dtype=bool)
+                try: mask[sorted(index[0], key=abs)] = True
+                except IndexError: pass
+            xp = choose(mask, (x,xp)).astype(float)
+            return f(xtype(xp), *args, **kwds)
+        func.index = _index
+        func.digits = _digits
+        return func
+    return dec
+
+
+def precision(digits=None, index=None):
+    """rounded outputs for the given function
+
+The function's output will be mapped to the given precision, where:
+  - digits is an int that sets the rounding precision (can be negative)
+  - if index tuple provided, only round at the given indices
+
+Examples:
+  >>> @precision()
+  ... def identity(x):
+  ...     return x
+  ...
+  >>> identity([0.123, 1.789, 4.000])
+  [0.0, 2.0, 4.0]
+
+  >>> @precision(digits=1, index=(0,3,4))
+  ... def squared(x):
+  ...     return [i**2 for i in x]
+  ...
+  >>> squared([123.45, 123.45, 4.01, 4.01, 0.012, 0.012])
+  [15239.9, 15239.9025, 16.080099999999998, 16.1, 0.0, 0.000144]
+
+  >>> @precision(digits=-1, index=(0,3,4))
+  ... def square(x):
+  ...     return [i**2 for i in x]
+  ...
+  >>> square([123.45, 123.45, 4.01, 4.01, 0.012, 0.012])
+  [15240.0, 15239.9025, 16.080099999999998, 20.0, 0.0, 0.000144]
+    """
+    digits = [digits or 0]
+    if isinstance(index, int): index = (index,)
+    index = [index]
+
+    def _index(alist=None):
+        index[0] = alist
+
+    def _digits(aint=None):
+        digits[0] = aint or 0
+
+    def dec(f):
+        def func(x,*args,**kwds):
+            fx = f(x, *args, **kwds)
+            if isinstance(fx, ndarray): xtype = asarray
+            else: xtype = type(fx)
+            y = round(fx, digits[0])
+            if index[0] is None:
+                mask = ones(y.size, dtype=bool)
+            else:
+                mask = zeros(y.size, dtype=bool)
+                try: mask[sorted(index[0], key=abs)] = True
+                except IndexError: pass
+            y = choose(mask, (fx,y))#.astype(float)
+            return xtype(y)
+        func.index = _index
+        func.digits = _digits
+        return func
+    return dec
+
+
 from random import randrange, shuffle
 def unique(seq, full=None):
     """replace the duplicate values with unique values in 'full'
 
     If full is a type (int or float), then unique values of the given type
     are selected from range(min(seq),max(seq)). If full is a dict of
     {'min':min, 'max':max}, then unique floats are selected from
     range(min(seq),max(seq)). If full is a sequence (list or set), then
     unique values are selected from the given sequence. 
 
-    For example:
-    >>> unique([1,2,3,1,2,4], range(11))
-    [1, 2, 3, 9, 8, 4]
-    >>> unique([1,2,3,1,2,9], range(11))
-    [1, 2, 3, 8, 5, 9]
-    >>> try:
-    ...     unique([1,2,3,1,2,13], range(11))
-    ... except ValueError:
-    ...     pass
-    ...
-    >>>
-    >>> unique([1,2,3,1,2,4], {'min':0, 'max':11})
-    [1, 2, 3, 4.175187820357143, 2.5407265707465716, 4]
-    >>> unique([1,2,3,1,2,4], {'min':0, 'max':11, 'type':int})
-    [1, 2, 3, 6, 8, 4]
-    >>> unique([1,2,3,1,2,4], float)
-    [1, 2, 3, 1.012375036824941, 3.9821250727509905, 4]
-    >>> unique([1,2,3,1,2,10], int)
-    [1, 2, 3, 9, 6, 10]
-    >>> try:
-    ...     unique([1,2,3,1,2,4], int)
-    ... except ValueError:
-    ...     pass
-    ...
+    Examples:
+      >>> unique([1,2,3,1,2,4], range(11))
+      [1, 2, 3, 9, 8, 4]
+
+      >>> unique([1,2,3,1,2,9], range(11))
+      [1, 2, 3, 8, 5, 9]
+
+      >>> try:
+      ...     unique([1,2,3,1,2,13], range(11))
+      ...     raise Exception
+      ... except ValueError:
+      ...     pass
+      ...
+
+      >>> unique([1,2,3,1,2,4], {'min':0, 'max':11})
+      [1, 2, 3, 4.175187820357143, 2.5407265707465716, 4]
+
+      >>> unique([1,2,3,1,2,4], {'min':0, 'max':11, 'type':int})
+      [1, 2, 3, 6, 8, 4]
+
+      >>> unique([1,2,3,1,2,4], float)
+      [1, 2, 3, 1.012375036824941, 3.9821250727509905, 4]
+
+      >>> unique([1,2,3,1,2,10], int)
+      [1, 2, 3, 9, 6, 10]
+
+      >>> try:
+      ...     unique([1,2,3,1,2,4], int)
+      ...     raise Exception
+      ... except ValueError:
+      ...     pass
+      ...
     """
     unique = set()
     # replace all duplicates with 'None'
     seq = [x if x not in unique and not unique.add(x) else None for x in seq]
     lseq = len(seq)
     # check type if full not specified
     if full is None:
@@ -934,63 +1067,62 @@
 
 
 #XXX: enable impose_unique on selected members of x? (see constraints.integers)
 
 def impose_unique(seq=None):
     """ensure all values are unique and found in the given set
 
-    For example:
-    >>> @impose_unique(range(11))
-    ... def doit(x):
-    ...     return x
-    ... 
-    >>> doit([1,2,3,1,2,4])
-    [1, 2, 3, 9, 8, 4]
-    >>> doit([1,2,3,1,2,10])
-    [1, 2, 3, 8, 5, 10]
-    >>> try:
-    ...     doit([1,2,3,1,2,13])
-    ... except ValueError:
-    ...     print("Bad Input")
-    ...
-    Bad Input
+    Examples:
+      >>> @impose_unique(range(11))
+      ... def doit(x):
+      ...     return x
+      ... 
+      >>> doit([1,2,3,1,2,4])
+      [1, 2, 3, 9, 8, 4]
+      >>> doit([1,2,3,1,2,10])
+      [1, 2, 3, 8, 5, 10]
+      >>> try:
+      ...     doit([1,2,3,1,2,13])
+      ...     raise Exception
+      ... except ValueError:
+      ...     pass
+      ...
 """
     def dec(f):
         def func(x,*args,**kwds):
             return f(unique(x, seq),*args,**kwds)
         return func
     return dec
 
 from numpy import array, intersect1d, inf, isnan, where, choose, clip as _clip
 from numpy.random import uniform, choice
 def bounded(seq, bounds, index=None, clip=True, nearest=True):
     """bound a sequence by bounds = [min,max]
 
-    For example:
-    >>> sequence = [0.123, 1.244, -4.755, 10.731, 6.207]
-    >>> 
-    >>> bounded(sequence, (0,5))
-    array([0.123, 1.244, 0.   , 5.   , 5.   ])
-    >>> 
-    >>> bounded(sequence, (0,5), index=(0,2,4))
-    array([ 0.123,  1.244,  0.   , 10.731,  5.   ])
-    >>> 
-    >>> bounded(sequence, (0,5), clip=False)
-    array([0.123     , 1.244     , 3.46621839, 1.44469038, 4.88937466])
-    >>> 
-    >>> bounds = [(0,5),(7,10)]
-    >>> my.constraints.bounded(sequence, bounds)
-    array([ 0.123,  1.244,  0.   , 10.   ,  7.   ])
-    >>> my.constraints.bounded(sequence, bounds, nearest=False)
-    array([ 0.123,  1.244,  7.   , 10.   ,  5.   ])
-    >>> my.constraints.bounded(sequence, bounds, nearest=False, clip=False) 
-    array([0.123     , 1.244     , 0.37617154, 8.79013111, 7.40864242])
-    >>> my.constraints.bounded(sequence, bounds, clip=False)
-    array([0.123     , 1.244     , 2.38186577, 7.41374049, 9.14662911])
-    >>> 
+    Examples:
+      >>> sequence = [0.123, 1.244, -4.755, 10.731, 6.207]
+      >>> 
+      >>> bounded(sequence, (0,5))
+      array([0.123, 1.244, 0.   , 5.   , 5.   ])
+      >>> 
+      >>> bounded(sequence, (0,5), index=(0,2,4))
+      array([ 0.123,  1.244,  0.   , 10.731,  5.   ])
+      >>> 
+      >>> bounded(sequence, (0,5), clip=False)
+      array([0.123     , 1.244     , 3.46621839, 1.44469038, 4.88937466])
+      >>> 
+      >>> bounds = [(0,5),(7,10)]
+      >>> my.constraints.bounded(sequence, bounds)
+      array([ 0.123,  1.244,  0.   , 10.   ,  7.   ])
+      >>> my.constraints.bounded(sequence, bounds, nearest=False)
+      array([ 0.123,  1.244,  7.   , 10.   ,  5.   ])
+      >>> my.constraints.bounded(sequence, bounds, nearest=False, clip=False) 
+      array([0.123     , 1.244     , 0.37617154, 8.79013111, 7.40864242])
+      >>> my.constraints.bounded(sequence, bounds, clip=False)
+      array([0.123     , 1.244     , 2.38186577, 7.41374049, 9.14662911])
 """
     seq = array(seq) #XXX: asarray?
     if bounds is None or not bounds: return seq
     if isinstance(index, int): index = (index,)
     if not hasattr(bounds[0], '__len__'): bounds = (bounds,)
     bounds = asfarray(bounds).T  # is [(min,min,...),(max,max,...)]
     # convert None to -inf or inf
@@ -1018,67 +1150,67 @@
     else: # randomly choose a value in one of the intervals
         seq[at] = choose(choice(len(bounds.T), size=at.shape), [uniform(0,1, size=at.shape) * (hi - lo) + lo for (lo,hi) in bounds.T])
     return seq
 
 def impose_bounds(bounds, index=None, clip=True, nearest=True):
     """generate a function where bounds=[min,max] on a sequence are imposed
 
-    For example:
-    >>> sequence = [0.123, 1.244, -4.755, 10.731, 6.207]
-    >>> 
-    >>> @impose_bounds((0,5))       
-    ... def simple(x):
-    ...   return x
-    ... 
-    >>> simple(sequence)
-    [0.123, 1.244, 0.0, 5.0, 5.0]
-    >>> 
-    >>> @impose_bounds((0,5), index=(0,2,4))
-    ... def double(x):
-    ...   return [i*2 for i in x]
-    ... 
-    >>> double(sequence)
-    [0.246, 2.488, 0.0, 21.462, 10.0]
-    >>> 
-    >>> @impose_bounds((0,5), index=(0,2,4), clip=False)
-    ... def square(x):
-    ...   return [i*i for i in x]
-    ... 
-    >>> square(sequence)
-    [0.015129, 1.547536, 14.675791119810688, 115.154361, 1.399551896073788]
-    >>> 
-    >>> @impose_bounds([(0,5),(7,10)])
-    ... def simple(x):
-    ...   return x
-    ... 
-    >>> simple(sequence)
-    [0.123, 1.244, 0.0, 10.0, 7.0]
-    >>> 
-    >>> @impose_bounds([(0,5),(7,10)], nearest=False)
-    ... def simple(x):
-    ...   return x
-    ... 
-    >>> simple(sequence)
-    [0.123, 1.244, 0.0, 5.0, 5.0]
-    >>> simple(sequence)
-    [0.123, 1.244, 7.0, 10.0, 5.0]
-    >>> 
-    >>> @impose_bounds({0:(0,5), 2:(0,5), 4:[(0,5),(7,10)]})
-    ... def simple(x):
-    ...   return x
-    ... 
-    >>> simple(sequence)
-    [0.123, 1.244, 0.0, 10.731, 7.0]
-    >>>
-    >>> @impose_bounds({0:(0,5), 2:(0,5), 4:[(0,5),(7,10)]}, index=(0,2)) 
-    ... def simple(x):
-    ...   return x
-    ... 
-    >>> simple(sequence)
-    [0.123, 1.244, 0.0, 10.731, 6.207]
+    Examples:
+      >>> sequence = [0.123, 1.244, -4.755, 10.731, 6.207]
+      >>> 
+      >>> @impose_bounds((0,5))       
+      ... def simple(x):
+      ...   return x
+      ... 
+      >>> simple(sequence)
+      [0.123, 1.244, 0.0, 5.0, 5.0]
+      >>> 
+      >>> @impose_bounds((0,5), index=(0,2,4))
+      ... def double(x):
+      ...   return [i*2 for i in x]
+      ... 
+      >>> double(sequence)
+      [0.246, 2.488, 0.0, 21.462, 10.0]
+      >>> 
+      >>> @impose_bounds((0,5), index=(0,2,4), clip=False)
+      ... def square(x):
+      ...   return [i*i for i in x]
+      ... 
+      >>> square(sequence)
+      [0.015129, 1.547536, 14.675791119810688, 115.154361, 1.399551896073788]
+      >>> 
+      >>> @impose_bounds([(0,5),(7,10)])
+      ... def simple(x):
+      ...   return x
+      ... 
+      >>> simple(sequence)
+      [0.123, 1.244, 0.0, 10.0, 7.0]
+      >>> 
+      >>> @impose_bounds([(0,5),(7,10)], nearest=False)
+      ... def simple(x):
+      ...   return x
+      ... 
+      >>> simple(sequence)
+      [0.123, 1.244, 0.0, 5.0, 5.0]
+      >>> simple(sequence)
+      [0.123, 1.244, 7.0, 10.0, 5.0]
+      >>> 
+      >>> @impose_bounds({0:(0,5), 2:(0,5), 4:[(0,5),(7,10)]})
+      ... def simple(x):
+      ...   return x
+      ... 
+      >>> simple(sequence)
+      [0.123, 1.244, 0.0, 10.731, 7.0]
+      >>>
+      >>> @impose_bounds({0:(0,5), 2:(0,5), 4:[(0,5),(7,10)]}, index=(0,2)) 
+      ... def simple(x):
+      ...   return x
+      ... 
+      >>> simple(sequence)
+      [0.123, 1.244, 0.0, 10.731, 6.207]
     """
     ### bounds is a dict, index filters the dict
     ### keys of bounds are the index, if index=None apply to all
     ### *but* if bounds is given as list (of tuples), apply to seleted index
     if isinstance(index, int): index = (index,)
     # bounds are list, index is tuple => {i:bounds} for each i in index
     if type(bounds) is not dict:
@@ -1202,26 +1334,26 @@
 
 functions are expected to take a single argument, a n-dimensional list or array,
 where the mask will be applied to the input array.
 
 operations within a single mask are unordered. If a specific ordering of
 operations is required, apply multiple masks in the desired order.
 
-For example,
+Examples:
     >>> @_impose_as({0:1, 2:(3,10)})
     ... def same(x):
     ...     return x
     ... 
     >>> same([0,1,2,3,4,5])
     [1, 1, 13, 3, 4, 5]
     >>> same([-1,-2,-3])
     [-2, -2, -3]
     >>> same([-1,-2,-3,-4])
     [-2, -2, 6, -4]
-    >>> 
+
     >>> @_impose_as({1:2})
     ... @_impose_as({0:1})
     ... def doit(x):
     ...     return [i+1 for i in x]
     ... 
     >>> doit([0,1,2,3,4,5])
     [3, 3, 3, 4, 5, 6]
@@ -1239,26 +1371,26 @@
 
 mask should be a set of tuples of positional index and tracked index,
 where the tuple should contain two different integers. The mask will be
 applied to the input, before the decorated function is called.
 
 The offset is applied to the second member of the tuple, and can accumulate.
 
-For example,
+Examples:
     >>> @impose_as([(0,1),(3,1),(4,5),(5,6),(5,7)])
     ... def same(x):
     ...   return x
     ... 
     >>> same([9,8,7,6,5,4,3,2,1])
     [9, 9, 7, 9, 5, 5, 5, 5, 1]
     >>> same([0,1,0,1])
     [0, 0, 0, 0]
     >>> same([-1,-2,-3,-4,-5,-6,-7])
     [-1, -1, -3, -1, -5, -5, -5]
-    >>> 
+
     >>> @impose_as([(0,1),(3,1),(4,5),(5,6),(5,7)], 10)
     ... def doit(x):
     ...   return x
     ... 
     >>> doit([9,8,7,6,5,4,3,2,1])
     [9, 19, 7, 9, 5, 15, 25, 25, 1]
     >>> doit([0,1,0,1])
@@ -1298,26 +1430,26 @@
 
 def impose_at(index, target=0.0):
     """generate a function, where some input is set to the target
 
 index should be a set of indices to be fixed at the target. The target
 can either be a single value (e.g. float), or a list of values.
 
-For example,
+Examples:
     >>> @impose_at([1,3,4,5,7], -99)
     ... def same(x):
     ...   return x
     ... 
     >>> same([1,1,1,1,1,1,1])
     [1, -99, 1, -99, -99, -99, 1]
     >>> same([1,1,1,1])
     [1, -99, 1, -99]
     >>> same([1,1])
     [1, -99]
-    >>> 
+
     >>> @impose_at([1,3,4,5,7], [0,2,4,6])
     ... def doit(x):
     ...   return x
     ... 
     >>> doit([1,1,1,1,1,1,1])
     [1, 0, 1, 2, 4, 6, 1]
     >>> doit([1,1,1,1])
@@ -1381,15 +1513,15 @@
 same value, and the weight from the second index in the pair will be removed
 and added to the weight of the first index
 
 noweight is a dict of collapses, or a tuple of dicts of collapses.
 a noweight collapse is a dict of {measure: {indices}), where the
 indices are where the measure will be constrained to have zero weight
 
-For example,
+Examples:
     >>> pos = {0: {(0,1)}, 1:{(0,2)}}
     >>> wts = {0: {1}, 1: {1, 2}}
     >>> npts = (3,3)
     >>> 
     >>> @impose_measure(npts, pos)
     ... def same(x):
     ...   return x
@@ -1410,15 +1542,14 @@
     >>> 
     >>> @impose_measure(npts, pos, wts)
     ... def both(x):
     ...   return x
     ... 
     >>> both([1./3, 1./3, 1./3, 1., 2., 3., 1./3, 1./3, 1./3, 1., 2., 3.])
     [0.66666666666666663, 0.0, 0.33333333333333331, 1.3333333333333335, 1.3333333333333335, 3.3333333333333335, 1.0, 0.0, 0.0, 2.0, 3.0, 2.0]
-    >>> 
     """
     # takes a dict of collapses, or a tuple of dicts of collapses
     if type(tracking) is dict: tracking = (tracking,)
     if type(noweight) is dict: noweight = (noweight,)
     def dec(f):
         def func(x, *args, **kwds):
             # populate a product measure with params
@@ -1449,51 +1580,49 @@
 
 tracking is a dict of collapses, or a tuple of dicts of collapses.
 a tracking collapse is a dict of {measure: {pairs of indices}}, where the
 pairs of indices are where the positions will be constrained to have the
 same value, and the weight from the second index in the pair will be removed
 and added to the weight of the first index
 
-For example,
+Examples:
     >>> pos = {0: {(0,1)}, 1:{(0,2)}}
     >>> npts = (3,3)
     >>> 
     >>> @impose_position(npts, pos)
     ... def same(x):
     ...   return x
     ... 
     >>> same([.5, 0., .5, 2., 4., 6., .25, .5, .25, 6., 4., 2.])
     [0.5, 0.0, 0.5, 2.0, 2.0, 6.0, 0.5, 0.5, 0.0, 5.0, 3.0, 5.0]
     >>> same([1./3, 1./3, 1./3, 1., 2., 3., 1./3, 1./3, 1./3, 1., 2., 3.])
     [0.6666666666666666, 0.0, 0.3333333333333333, 1.3333333333333335, 1.3333333333333335, 3.3333333333333335, 0.6666666666666666, 0.3333333333333333, 0.0, 1.6666666666666667, 2.666666666666667, 1.6666666666666667]
-    >>> 
     """
     return impose_measure(npts, tracking, {})
 
 
 def impose_weight(npts, noweight):
     """generate a function, that constrains measure weights
 
 npts is a tuple of the product_measure dimensionality
 
 noweight is a dict of collapses, or a tuple of dicts of collapses.
 a noweight collapse is a dict of {measure: {indices}), where the
 indices are where the measure will be constrained to have zero weight
 
-For example,
+Examples:
     >>> wts = {0: {1}, 1: {1, 2}}
     >>> npts = (3,3)
     >>> 
     >>> @impose_weight(npts, wts)
     ... def doit(x):
     ...   return x
     ... 
     >>> doit([.5, 0., .5, 2., 4., 6., .25, .5, .25, 6., 4., 2.])
     [0.5, 0.0, 0.5, 2.0, 4.0, 6.0, 1.0, 0.0, 0.0, 4.0, 2.0, 0.0]
     >>> doit([1./3, 1./3, 1./3, 1., 2., 3., 1./3, 1./3, 1./3, 1., 2., 3.])
     [0.5, 0.0, 0.5, 1.0, 2.0, 3.0, 1.0, 0.0, 0.0, 2.0, 3.0, 4.0]
-    >>> 
     """
     return impose_measure(npts, {}, noweight)
 
 
 # EOF
```

### Comparing `mystic-0.4.0/mystic/coupler.py` & `mystic-0.4.1/mystic/coupler.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Function Couplers
 
 These methods can be used to couple two functions together,
 and represent some common patterns found in applying constraints
@@ -19,15 +19,15 @@
 
 def outer(outer=lambda x:x, args=None, kwds=None):
     """wrap a function around another function: convert y = f(x) to y' = c(f(x))
 
 This is a useful function for nesting one constraint in another constraint.
 A constraints function takes an iterable x as input, returning a modified x.
 
-    For example:
+Examples:
     >>> def squared(x):
     ...   return x**2             
     ... 
     >>> # equivalent to: ((x+1)**2) 
     >>> @outer(squared)
     ... def constrain(x):
     ...   return x+1
@@ -50,15 +50,15 @@
     """nest a function within another function: convert y = f(x) to y' = f(c(x))
 
 This is a useful function for nesting one constraint in another constraint.
 A constraints function takes an iterable x as input, returning a modified x.
 The "inner" coupler is utilized by mystic.solvers to bind constraints to a cost
 function; thus the constraints are imposed every cost function evaluation.
 
-    For example:
+Examples:
     >>> def squared(x):
     ...   return x**2             
     ... 
     >>> # equivalent to: ((x**2)+1) 
     >>> @inner(squared)
     ... def constrain(x):
     ...   return x+1
@@ -137,15 +137,15 @@
 def additive(penalty=lambda x:0.0, args=None, kwds=None):
     """penalize a function with another function: y = f(x) to y' = f(x) + p(x)
     
 This is useful, for example, in penalizing a cost function where the constraints
 are violated; thus, the satisfying the constraints will be preferred at every
 cost function evaluation.
 
-    For example:
+Examples:
     >>> def squared(x):
     ...   return x**2             
     ... 
     >>> # equivalent to: (x+1) + (x**2) 
     >>> @additive(squared)
     ... def constrain(x):
     ...   return x+1
```

### Comparing `mystic-0.4.0/mystic/differential_evolution.py` & `mystic-0.4.1/mystic/differential_evolution.py`

 * *Files 3% similar despite different names*

```diff
@@ -22,15 +22,15 @@
 ## adapted to AbstractSolver interface by Mike McKerns
 ##
 ## modified for AbstractMapSolver interface by Mike McKerns
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2006-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 """
 Solvers
 =======
 
@@ -189,44 +189,50 @@
 #           elif self.trialSolution[i] > max[i]:
 #               self.trialSolution[i] = random.uniform(base[i],max[i])
 #       return
 
     def UpdateGenealogyRecords(self, id, newchild):
         """create an in-memory log of the genealogy of the population
 
-Input::
-    - id: (int) the index of the candidate in the population matrix
-    - newchild: (list[float]) a new trialSolution
+Args:
+    id (int): the index of the candidate in the population matrix
+    newchild (list[float]): a new trialSolution
         """
         self.genealogy[id].append(newchild)
         return
 
     def SetConstraints(self, constraints):
         """apply a constraints function to the optimization
 
-input::
-    - a constraints function of the form: xk' = constraints(xk),
-      where xk is the current parameter vector. Ideally, this function
+Args:
+    constraints (function): function of the form: ``xk' = constraints(xk)``,
+      where ``xk`` is the current parameter vector. Ideally, this function
       is constructed so the parameter vector it passes to the cost function
-      will satisfy the desired (i.e. encoded) constraints."""
+      will satisfy the desired (i.e. encoded) constraints.
+        """
         if not constraints:
             self._constraints = lambda x: x
         elif not isinstance(constraints, _Callable):
             raise TypeError("'%s' is not a callable function" % constraints)
         else: #XXX: check for format: x' = constraints(x) ?
             self._constraints = constraints
         return # doesn't use wrap_nested
 
     def _decorate_objective(self, cost, ExtraArgs=None):
         """decorate the cost function with bounds, penalties, monitors, etc
 
-input::
-    - cost is the objective function, of the form y = cost(x, *ExtraArgs),
-      where x is a candidate solution, and ExtraArgs is the tuple of positional
-      arguments required to evaluate the objective."""
+Args:
+    cost (func): objective, of form ``y = cost(x, *ExtraArgs)``, where ``x``
+      is a candidate solution vector
+    ExtraArgs (tuple, default=None): tuple of positional arguments required to
+      evaluate the objective
+
+Returns:
+    decorated objective function
+        """
         #print("@%r %r %r" % (cost, ExtraArgs, max))
         evalmon = self._evalmon
         raw = cost
         if ExtraArgs is None: ExtraArgs = ()
         self._fcalls, cost = wrap_function(cost, ExtraArgs, evalmon)
         if self._useStrictRange:
             indx = list(self.popEnergy).index(self.bestEnergy)
@@ -242,24 +248,26 @@
         self._cost = (cost, raw, ExtraArgs)
         self._live = True
         return cost
 
     def _Step(self, cost=None, ExtraArgs=None, **kwds):
         """perform a single optimization iteration
 
-input::
-    - cost is the objective function, of the form y = cost(x, *ExtraArgs),
-      where x is a candidate solution, and ExtraArgs is the tuple of positional
-      arguments required to evaluate the objective.
+Args:
+    cost (func, default=None): objective, of form ``y = cost(x, *ExtraArgs)``,
+      where ``x`` is a candidate solution vector
+    ExtraArgs (tuple, default=None): tuple of positional arguments required to
+      evaluate the objective
 
-note::
-    ExtraArgs needs to be a *tuple* of extra arguments.
+Returns:
+    None
 
-    This method accepts additional args that are specific for the current
-    solver, as detailed in the `_process_inputs` method.
+Notes:
+    - This method accepts additional ``kwds`` that are specific for the current
+      solver, as detailed in the ``_process_inputs`` method.
         """
         # process and activate input settings
         settings = self._process_inputs(kwds)
         #(hardwired: due to python exec'ing to locals())
         callback = settings['callback'] if 'callback' in settings else None
         disp = settings['disp'] if 'disp' in settings else False
         strategy = settings['strategy'] if 'strategy' in settings else self.strategy
@@ -325,35 +333,36 @@
         if init: self._termination(self) #XXX: at generation 0 or always?
         return #XXX: call Terminated ?
 
     def _process_inputs(self, kwds):
         """process and activate input settings
 
 Args:
-    callback (func, default=None): function to call after each iteration. The
-        interface is ``callback(xk)``, with xk the current parameter vector.
+    callback (function, default=None): function called after each iteration. The
+        interface is ``callback(xk)``, with ``xk`` the current parameter vector.
     disp (bool, default=False): if True, print convergence messages.
-
-Additional Args:
-    EvaluationMonitor: a monitor instance to capture each evaluation of cost.
-    StepMonitor: a monitor instance to capture each iteration's best results.
-    penalty: a function of the form: y' = penalty(xk), with y = cost(xk) + y',
-        where xk is the current parameter vector.
-    constraints: a function of the form: xk' = constraints(xk), where xk is
-        the current parameter vector.
-    strategy (strategy, default=Best1Bin): the mutation strategy for generating        new trial solutions.
+    EvaluationMonitor (monitor, default=None): a monitor instance to capture
+        each evaluation of cost.
+    StepMonitor (monitor, default=None): a monitor instance to capture each
+        iteration's best results.
+    penalty (penalty, default=None): function of the form: ``y' = penalty(xk)``,
+        with ``y = cost(xk) + y'`` and ``xk`` is the current parameter vector.
+    constraints (constraint, default=None): function of the form:
+        ``xk' = constraints(xk)``, where ``xk`` is the current parameter vector.
+    strategy (strategy, default=Best1Bin): the mutation strategy for generating
+        new trial solutions.
     CrossProbability (float, default=0.9): the probability of cross-parameter
         mutations.
     ScalingFactor (float, default=0.8): multiplier for mutations on the trial
         solution.
 
-Note:
-   The additional args are 'sticky', in that once they are given, they remain
-   set until they are explicitly changed. Conversely, the args are not sticky,
-   and are thus set for a one-time use.
+Notes:
+    ``callback`` and ``disp`` are 'sticky', in that once they are given, they
+    remain set until they are explicitly changed. Conversely, the other inputs
+    are not sticky, and are thus set for a one-time use.
         """
         #allow for inputs that don't conform to AbstractSolver interface
         #NOTE: not sticky: callback, disp
         #NOTE: sticky: EvaluationMonitor, StepMonitor, penalty, constraints
         #NOTE: sticky: strategy, CrossProbability, ScalingFactor
         settings = super(DifferentialEvolutionSolver, self)._process_inputs(kwds)
         from mystic import strategy
@@ -373,25 +382,25 @@
     def Solve(self, cost=None, termination=None, ExtraArgs=None, **kwds):
         """Minimize a function using differential evolution.
 
 Uses a differential evolution algorithm to find the minimum of a function of
 one or more variables.
 
 Args:
-    cost (func, default=None): the function to be minimized: ``y = cost(x)``.
+    cost (function, default=None): function to be minimized: ``y = cost(x)``.
     termination (termination, default=None): termination conditions.
     ExtraArgs (tuple, default=None): extra arguments for cost.
     strategy (strategy, default=Best1Bin): the mutation strategy for generating        new trial solutions.
     CrossProbability (float, default=0.9): the probability of cross-parameter
         mutations.
     ScalingFactor (float, default=0.8): multiplier for mutations on the trial
         solution.
-    sigint_callback (func, default=None): callback function for signal handler.
-    callback (func, default=None): function to call after each iteration. The
-        interface is ``callback(xk)``, with xk the current parameter vector.
+    sigint_callback (function, default=None): signal handler callback function.
+    callback (function, default=None): function called after each iteration. The
+        interface is ``callback(xk)``, with ``xk`` the current parameter vector.
     disp (bool, default=False): if True, print convergence messages.
 
 Returns:
     None
         """
         super(DifferentialEvolutionSolver, self).Solve(cost, termination,\
                                                        ExtraArgs, **kwds)
@@ -406,63 +415,68 @@
 Alternate implementation: 
     - utilizes a map-reduce interface, extensible to parallel computing
     - both a current and a next generation are kept, while the current
       generation is invariant during the main DE logic
     """
     def __init__(self, dim, NP=4):
         """
-Takes two initial inputs: 
-    dim  -- dimensionality of the problem
-    NP   -- size of the trial solution population. [requires: NP >= 4]
-
-All important class members are inherited from AbstractSolver.
+Args: 
+    dim (int): dimensionality of the problem
+    NP (int, default=4): size of the trial solution population, with ``NP >= 4``
         """
+        #All important class members are inherited from AbstractSolver.
         NP = max(NP, dim, 4) #XXX: raise Error if npop <= 4?
         super(DifferentialEvolutionSolver2, self).__init__(dim, npop=NP)
         self.genealogy     = [ [] for j in range(NP)]
         self.scale         = 0.8
         self.probability   = 0.9
         self.strategy      = 'Best1Bin'
         ftol = 5e-3
         from mystic.termination import VTRChangeOverGeneration
         self._termination = VTRChangeOverGeneration(ftol)
         
     def UpdateGenealogyRecords(self, id, newchild):
         """create an in-memory log of the genealogy of the population
 
-Input::
-    - id: (int) the index of the candidate in the population matrix
-    - newchild: (list[float]) a new trialSolution
+Args:
+    id (int): the index of the candidate in the population matrix
+    newchild (list[float]): a new trialSolution
         """
         self.genealogy[id].append(newchild)
         return
 
     def SetConstraints(self, constraints):
         """apply a constraints function to the optimization
 
-input::
-    - a constraints function of the form: xk' = constraints(xk),
-      where xk is the current parameter vector. Ideally, this function
+Args:
+    constraints (function): function of the form: ``xk' = constraints(xk)``,
+      where ``xk`` is the current parameter vector. Ideally, this function
       is constructed so the parameter vector it passes to the cost function
-      will satisfy the desired (i.e. encoded) constraints."""
+      will satisfy the desired (i.e. encoded) constraints.
+        """
         if not constraints:
             self._constraints = lambda x: x
         elif not isinstance(constraints, _Callable):
             raise TypeError("'%s' is not a callable function" % constraints)
         else: #XXX: check for format: x' = constraints(x) ?
             self._constraints = constraints
         return # doesn't use wrap_nested
 
     def _decorate_objective(self, cost, ExtraArgs=None):
         """decorate the cost function with bounds, penalties, monitors, etc
 
-input::
-    - cost is the objective function, of the form y = cost(x, *ExtraArgs),
-      where x is a candidate solution, and ExtraArgs is the tuple of positional
-      arguments required to evaluate the objective."""
+Args:
+    cost (func): objective, of form ``y = cost(x, *ExtraArgs)``, where ``x``
+      is a candidate solution vector
+    ExtraArgs (tuple, default=None): tuple of positional arguments required to
+      evaluate the objective
+
+Returns:
+    decorated objective function
+        """
         #print("@%r %r %r" % (cost, ExtraArgs, max))
         raw = cost
         if ExtraArgs is None: ExtraArgs = ()
         from mystic.python_map import python_map
         if self._map != python_map:
             #FIXME: EvaluationMonitor fails for MPI, throws error for 'pp'
             from mystic.monitors import Null
@@ -483,24 +497,26 @@
         self._cost = (cost, raw, ExtraArgs)
         self._live = True
         return cost
 
     def _Step(self, cost=None, ExtraArgs=None, **kwds):
         """perform a single optimization iteration
 
-input::
-    - cost is the objective function, of the form y = cost(x, *ExtraArgs),
-      where x is a candidate solution, and ExtraArgs is the tuple of positional
-      arguments required to evaluate the objective.
+Args:
+    cost (func, default=None): objective, of form ``y = cost(x, *ExtraArgs)``,
+      where ``x`` is a candidate solution vector
+    ExtraArgs (tuple, default=None): tuple of positional arguments required to
+      evaluate the objective
 
-note::
-    ExtraArgs needs to be a *tuple* of extra arguments.
+Returns:
+    None
 
-    This method accepts additional args that are specific for the current
-    solver, as detailed in the `_process_inputs` method.
+Notes:
+    - This method accepts additional ``kwds`` that are specific for the current
+      solver, as detailed in the ``_process_inputs`` method.
         """
         # process and activate input settings
         settings = self._process_inputs(kwds)
         #(hardwired: due to python exec'ing to locals())
         callback = settings['callback'] if 'callback' in settings else None
         disp = settings['disp'] if 'disp' in settings else False
         strategy = settings['strategy'] if 'strategy' in settings else self.strategy
@@ -572,35 +588,36 @@
         if init: self._termination(self) #XXX: at generation 0 or always?
         return #XXX: call Terminated ?
 
     def _process_inputs(self, kwds):
         """process and activate input settings
 
 Args:
-    callback (func, default=None): function to call after each iteration. The
-        interface is ``callback(xk)``, with xk the current parameter vector.
+    callback (function, default=None): function called after each iteration. The
+        interface is ``callback(xk)``, with ``xk`` the current parameter vector.
     disp (bool, default=False): if True, print convergence messages.
-
-Additional Args:
-    EvaluationMonitor: a monitor instance to capture each evaluation of cost.
-    StepMonitor: a monitor instance to capture each iteration's best results.
-    penalty: a function of the form: y' = penalty(xk), with y = cost(xk) + y',
-        where xk is the current parameter vector.
-    constraints: a function of the form: xk' = constraints(xk), where xk is
-        the current parameter vector.
-    strategy (strategy, default=Best1Bin): the mutation strategy for generating        new trial solutions.
+    EvaluationMonitor (monitor, default=None): a monitor instance to capture
+        each evaluation of cost.
+    StepMonitor (monitor, default=None): a monitor instance to capture each
+        iteration's best results.
+    penalty (penalty, default=None): function of the form: ``y' = penalty(xk)``,
+        with ``y = cost(xk) + y'`` and ``xk`` is the current parameter vector.
+    constraints (constraint, default=None): function of the form:
+        ``xk' = constraints(xk)``, where ``xk`` is the current parameter vector.
+    strategy (strategy, default=Best1Bin): the mutation strategy for generating
+        new trial solutions.
     CrossProbability (float, default=0.9): the probability of cross-parameter
         mutations.
     ScalingFactor (float, default=0.8): multiplier for mutations on the trial
         solution.
 
-Note:
-   The additional args are 'sticky', in that once they are given, they remain
-   set until they are explicitly changed. Conversely, the args are not sticky,
-   and are thus set for a one-time use.
+Notes:
+    ``callback`` and ``disp`` are 'sticky', in that once they are given, they
+    remain set until they are explicitly changed. Conversely, the other inputs
+    are not sticky, and are thus set for a one-time use.
         """
         #allow for inputs that don't conform to AbstractSolver interface
         #NOTE: not sticky: callback, disp
         #NOTE: sticky: EvaluationMonitor, StepMonitor, penalty, constraints
         #NOTE: sticky: strategy, CrossProbability, ScalingFactor
         settings = super(DifferentialEvolutionSolver2, self)._process_inputs(kwds)
         from mystic import strategy
@@ -621,25 +638,25 @@
         """Minimize a function using differential evolution.
 
 Uses a differential evolution algorithm to find the minimum of a function of
 one or more variables. This implementation holds the current generation
 invariant until the end of each iteration.
 
 Args:
-    cost (func, default=None): the function to be minimized: ``y = cost(x)``.
+    cost (function, default=None): function to be minimized: ``y = cost(x)``.
     termination (termination, default=None): termination conditions.
     ExtraArgs (tuple, default=None): extra arguments for cost.
     strategy (strategy, default=Best1Bin): the mutation strategy for generating        new trial solutions.
     CrossProbability (float, default=0.9): the probability of cross-parameter
         mutations.
     ScalingFactor (float, default=0.8): multiplier for mutations on the trial
         solution.
-    sigint_callback (func, default=None): callback function for signal handler.
-    callback (func, default=None): function to call after each iteration. The
-        interface is ``callback(xk)``, with xk the current parameter vector.
+    sigint_callback (function, default=None): signal handler callback function.
+    callback (function, default=None): function called after each iteration. The
+        interface is ``callback(xk)``, with ``xk`` the current parameter vector.
     disp (bool, default=False): if True, print convergence messages.
 
 Returns:
     None
         """
         super(DifferentialEvolutionSolver2, self).Solve(cost, termination,\
                                                         ExtraArgs, **kwds)
@@ -651,15 +668,15 @@
             full_output=0,disp=1,retall=0,callback=None,**kwds):
     """Minimize a function using Storn & Price's differential evolution.
 
 Uses Storn & Prices's differential evolution algorithm to find the minimum of a
 function of one or more variables. Mimics a ``scipy.optimize`` style interface.
 
 Args:
-    cost (func): the function or method to be minimized: ``y = cost(x)``.
+    cost (function): the function or method to be minimized: ``y = cost(x)``.
     x0 (ndarray): the initial guess parameter vector ``x`` if desired start
         is a single point, otherwise takes a list of (min,max) bounds that
         define a region from which random initial points are drawn.
     npop (int, default=4): size of the trial solution population.
     args (tuple, default=()): extra arguments for cost.
     bounds (list(tuple), default=None): list of pairs of bounds (min,max),
         one for each parameter.
@@ -669,30 +686,30 @@
     maxiter (int, default=None): the maximum number of iterations to perform.
     maxfun (int, default=None): the maximum number of function evaluations.
     cross (float, default=0.9): the probability of cross-parameter mutations.
     scale (float, default=0.8): multiplier for mutations on the trial solution.
     full_output (bool, default=False): True if fval and warnflag are desired.
     disp (bool, default=True): if True, print convergence messages.
     retall (bool, default=False): True if allvecs is desired.
-    callback (func, default=None): function to call after each iteration. The
-        interface is ``callback(xk)``, with xk the current parameter vector.
+    callback (function, default=None): function called after each iteration. The
+        interface is ``callback(xk)``, with ``xk`` the current parameter vector.
     handler (bool, default=False): if True, enable handling interrupt signals.
     id (int, default=None): the ``id`` of the solver used in logging.
     strategy (strategy, default=None): override the default mutation strategy.
     itermon (monitor, default=None): override the default GenerationMonitor.
     evalmon (monitor, default=None): override the default EvaluationMonitor.
-    constraints (func, default=None): a function ``xk' = constraints(xk)``,
-        where xk is the current parameter vector, and xk' is a parameter
+    constraints (function, default=None): function ``xk' = constraints(xk)``,
+        where ``xk`` is the current parameter vector, and ``xk'`` is a parameter
         vector that satisfies the encoded constraints.
-    penalty (func, default=None): a function ``y = penalty(xk)``, where xk is
-        the current parameter vector, and ``y' == 0`` when the encoded
+    penalty (function, default=None): function ``y = penalty(xk)``, where ``xk``
+        is the current parameter vector, and ``y' == 0`` when the encoded
         constraints are satisfied (and ``y' > 0`` otherwise).
     tightrange (bool, default=None): impose bounds and constraints concurrently.
     cliprange (bool, default=None): bounding constraints clip exterior values.
-    map (func, default=None): a (parallel) map instance ``y = map(f, x)``.
+    map (function, default=None): a (parallel) map instance ``y = map(f, x)``.
 
 Returns:
     ``(xopt, {fopt, iter, funcalls, warnflag}, {allvecs})``
 
 Notes:
     - xopt (*ndarray*): the minimizer of the cost function
     - fopt (*float*): value of cost function at minimum: ``fopt = cost(xopt)``
@@ -716,15 +733,15 @@
            full_output=0,disp=1,retall=0,callback=None,**kwds):
     """Minimize a function using differential evolution.
 
 Uses a differential evolution algorithm to find the minimum of a function of
 one or more variables. Mimics a ``scipy.optimize`` style interface.
 
 Args:
-    cost (func): the function or method to be minimized: ``y = cost(x)``.
+    cost (function): the function or method to be minimized: ``y = cost(x)``.
     x0 (ndarray): the initial guess parameter vector ``x`` if desired start
         is a single point, otherwise takes a list of (min,max) bounds that
         define a region from which random initial points are drawn.
     npop (int, default=4): size of the trial solution population.
     args (tuple, default=()): extra arguments for cost.
     bounds (list(tuple), default=None): list of pairs of bounds (min,max),
         one for each parameter.
@@ -734,30 +751,30 @@
     maxiter (int, default=None): the maximum number of iterations to perform.
     maxfun (int, default=None): the maximum number of function evaluations.
     cross (float, default=0.9): the probability of cross-parameter mutations.
     scale (float, default=0.8): multiplier for mutations on the trial solution.
     full_output (bool, default=False): True if fval and warnflag are desired.
     disp (bool, default=True): if True, print convergence messages.
     retall (bool, default=False): True if allvecs is desired.
-    callback (func, default=None): function to call after each iteration. The
-        interface is ``callback(xk)``, with xk the current parameter vector.
+    callback (function, default=None): function called after each iteration. The
+        interface is ``callback(xk)``, with ``xk`` the current parameter vector.
     handler (bool, default=False): if True, enable handling interrupt signals.
     id (int, default=None): the ``id`` of the solver used in logging.
     strategy (strategy, default=None): override the default mutation strategy.
     itermon (monitor, default=None): override the default GenerationMonitor.
     evalmon (monitor, default=None): override the default EvaluationMonitor.
-    constraints (func, default=None): a function ``xk' = constraints(xk)``,
-        where xk is the current parameter vector, and xk' is a parameter
+    constraints (function, default=None): function ``xk' = constraints(xk)``,
+        where ``xk`` is the current parameter vector, and ``xk'`` is a parameter
         vector that satisfies the encoded constraints.
-    penalty (func, default=None): a function ``y = penalty(xk)``, where xk is
-        the current parameter vector, and ``y' == 0`` when the encoded
+    penalty (function, default=None): function ``y = penalty(xk)``, where ``xk``
+        is the current parameter vector, and ``y' == 0`` when the encoded
         constraints are satisfied (and ``y' > 0`` otherwise).
     tightrange (bool, default=None): impose bounds and constraints concurrently.
     cliprange (bool, default=None): bounding constraints clip exterior values.
-    map (func, default=None): a (parallel) map instance ``y = map(f, x)``.
+    map (function, default=None): a (parallel) map instance ``y = map(f, x)``.
 
 Returns:
     ``(xopt, {fopt, iter, funcalls, warnflag}, {allvecs})``
 
 Notes:
     - xopt (*ndarray*): the minimizer of the cost function
     - fopt (*float*): value of cost function at minimum: ``fopt = cost(xopt)``
@@ -838,15 +855,15 @@
     elif iterations >= solver._maxiter:
         warnflag = 2
         if disp:
             print("Warning: Maximum number of iterations has been exceeded")
     else:
         if disp:
             print("Optimization terminated successfully.")
-            print("         Current function value: %f" % fval)
+            print("         Current function value: %s" % fval)
             print("         Iterations: %d" % iterations)
             print("         Function evaluations: %d" % fcalls)
 
     if full_output:
         retlist = x, fval, iterations, fcalls, warnflag
         if retall:
             retlist += (allvecs,)
```

### Comparing `mystic-0.4.0/mystic/ensemble.py` & `mystic-0.4.1/mystic/ensemble.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Solvers
 =======
 
 This module contains a collection of optimization routines that use "map"
```

### Comparing `mystic-0.4.0/mystic/filters.py` & `mystic-0.4.1/mystic/filters.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Input/output 'filters'
 """
 
 # 'filters'
@@ -46,38 +46,38 @@
 
     cx: mystic.constraint function where x' = cx(x) and x is parameter array
     cy: mystic.constraint function where [y'] = cy([y]) and y is cost array
 
     returns a masking function for (x,y) data or monitors, where
     list[bool] = mask(x,y), with True where constraints are satisfied
 
-    For example:
-    >>> mon = Monitor()
-    >>> mon([0.0,0.5,1.0],2)
-    >>> mon([2.0,3.0,4.0],3)
-    >>> mon([4.0,5.0,6.0],4)
-    >>> mon([5.0,5.5,6.5],6)
-    >>> 
-    >>> @impose_bounds((0,5))
-    ... def inputs(x):
-    ...   return x
-    ... 
-    >>> generate_mask(inputs)(mon)
-    [True, True, False, False]
-    >>> generate_mask(y=inputs)(mon)
-    [True, True, True, False]
-    >>>
-    >>> @integers()
-    ... def identity(x):
-    ...   return x
-    ... 
-    >>> generate_mask(identity)(mon)
-    [False, True, True, False]
-    >>> generate_mask(y=identity)(mon)
-    [True, True, True, True]
+    Examples:
+      >>> mon = Monitor()
+      >>> mon([0.0,0.5,1.0],2)
+      >>> mon([2.0,3.0,4.0],3)
+      >>> mon([4.0,5.0,6.0],4)
+      >>> mon([5.0,5.5,6.5],6)
+      >>> 
+      >>> @impose_bounds((0,5))
+      ... def inputs(x):
+      ...   return x
+      ... 
+      >>> generate_mask(inputs)(mon)
+      [True, True, False, False]
+      >>> generate_mask(y=inputs)(mon)
+      [True, True, True, False]
+      >>>
+      >>> @integers()
+      ... def identity(x):
+      ...   return x
+      ... 
+      >>> generate_mask(identity)(mon)
+      [False, True, True, False]
+      >>> generate_mask(y=identity)(mon)
+      [True, True, True, True]
     """
     def func(x, z=None):
         _x = getattr(x, '_x', x)
         _y = x._y if z is None else z
         _x = _x.tolist() if hasattr(_x, 'tolist') else _x
         _y = _y.tolist() if hasattr(_y, 'tolist') else _y
         from numpy import ones_like
@@ -94,40 +94,40 @@
     """generate a data filter from a data masking function
 
     mask: masking function (built with generate_mask) or a boolean mask
 
     returns a function that filters (x,y) or a monitor, based on the given mask
     x',y' = filter(x,y), where filter removes values where mask is False
 
-    For example:
-    >>> mon = Monitor()
-    >>> mon([0.0,0.5,1.0],2)
-    >>> mon([2.0,3.0,4.0],3)
-    >>> mon([4.0,5.0,6.0],4)
-    >>> mon([5.0,5.5,6.5],6)
-    >>> 
-    >>> @impose_bounds((0,5))
-    ... def inputs(x):
-    ...   return x
-    ... 
-    >>> m = generate_filter(generate_mask(inputs))(mon)
-    >>> m._x
-    [[0.0, 0.5, 1.0], [2.0, 3.0, 4.0]]
-    >>> m._y
-    [2, 3]
-    >>>
-    >>> @integers()
-    ... def identity(x):
-    ...   return x
-    ... 
-    >>> m = generate_filter(generate_mask(identity))(mon)
-    >>> m._x
-    [[2.0, 3.0, 4.0], [4.0, 5.0, 6.0]]
-    >>> m._y
-    [3, 4]
+    Examples:
+      >>> mon = Monitor()
+      >>> mon([0.0,0.5,1.0],2)
+      >>> mon([2.0,3.0,4.0],3)
+      >>> mon([4.0,5.0,6.0],4)
+      >>> mon([5.0,5.5,6.5],6)
+      >>> 
+      >>> @impose_bounds((0,5))
+      ... def inputs(x):
+      ...   return x
+      ... 
+      >>> m = generate_filter(generate_mask(inputs))(mon)
+      >>> m._x
+      [[0.0, 0.5, 1.0], [2.0, 3.0, 4.0]]
+      >>> m._y
+      [2, 3]
+      >>>
+      >>> @integers()
+      ... def identity(x):
+      ...   return x
+      ... 
+      >>> m = generate_filter(generate_mask(identity))(mon)
+      >>> m._x
+      [[2.0, 3.0, 4.0], [4.0, 5.0, 6.0]]
+      >>> m._y
+      [3, 4]
     """
     def func(x, z=None):
         if not hasattr(mask, '__call__'):
             _mask = mask
         else:
             _mask = mask(x, z)
         if z is None and hasattr(x, '_x') and hasattr(x, '_y'):
```

### Comparing `mystic-0.4.0/mystic/forward_model.py` & `mystic-0.4.1/mystic/forward_model.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 This module contains classes that aid in constructing cost functions.
 Cost function can easily be created by hand; however, mystic also
 provides an automated method that allows the dynamic wrapping of 
 forward models into cost function objects.
```

### Comparing `mystic-0.4.0/mystic/helputil.py` & `mystic-0.4.1/mystic/helputil.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Tools for prettifying help
 
 Some of following code is taken from Ka-Ping Yee's pydoc module
 """
```

### Comparing `mystic-0.4.0/mystic/linesearch.py` & `mystic-0.4.1/mystic/linesearch.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 # You may copy and use this module as you see fit with no
 # guarantee implied provided you keep this notice in all copies.
 # *****END NOTICE************
 #
 # Forked by: Mike McKerns (February 2009)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2009-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """ local copy of scipy.optimize.linesearch """
 
 def line_search(f, myfprime, xk, pk, gfk, old_fval, old_old_fval,
                 args=(), c1=1e-4, c2=0.9, amax=50):
```

### Comparing `mystic-0.4.0/mystic/mask.py` & `mystic-0.4.1/mystic/mask.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Lan Huong Nguyen (lanhuong @stanford)
 # Copyright (c) 2012-2015 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import mystic.termination as _term
 
 def get_mask(condition): #FIXME: gets None if is None *and* if no mask
     '''get mask from termination condition'''
```

### Comparing `mystic-0.4.0/mystic/math/__init__.py` & `mystic-0.4.1/mystic/math/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 math: mathematical functions and tools for use in mystic
 
 
 Functions
```

### Comparing `mystic-0.4.0/mystic/math/_rbf.py` & `mystic-0.4.1/mystic/math/_rbf.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 # rbf.py module by John Travers, Robert Hetland, and Travis Oliphant
 #
 # Forked by: Mike McKerns (October 2018)
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """rbf - Radial basis functions for interpolation/smoothing scattered Nd data.
 """
 #
 # original documentation/license (below)
 """
```

### Comparing `mystic-0.4.0/mystic/math/approx.py` & `mystic-0.4.1/mystic/math/approx.py`

 * *Files 4% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # almostEqual is a repackaging of numpy.allclose, but at different 'tol'
 # approx_equal is similar to almostEqual, and can be treated as deprecated
 #
 # Forked by: Mike McKerns (May 2010)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2010-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 tools for measuring equality
 """
 
 def _float_approx_equal(x, y, tol=1e-18, rel=1e-7):
```

### Comparing `mystic-0.4.0/mystic/math/compressed.py` & `mystic-0.4.1/mystic/math/compressed.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 helpers for compressed format for measures
 """
 
 __oct2bin_lookup = {'0': '000', '1': '001', '2': '010', '3': '011',\
```

### Comparing `mystic-0.4.0/mystic/math/discrete.py` & `mystic-0.4.1/mystic/math/discrete.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Classes for discrete measure data objects.
 Includes point_mass, measure, product_measure, and scenario classes.
 """
 # Adapted from seesaw2d.py in branches/UQ/math/examples2/ 
@@ -451,15 +451,15 @@
   def __set_mean(self, center_masses):
     [i._measure__set_mean(center_masses[m]) for (m,i) in enumerate(self)]
    #for i in range(len(center_masses)):
    #  self[i].center_mass = center_masses[i]
     return
 
   def __n(self):
-    from numpy import product
+    from numpy import prod as product
     return product(self.pts)
 
   def support_index(self, tol=0):
     """get the indices where there is support (i.e. non-zero weight)
 
 Args:
     tol (float, default=0.0): tolerance, where any ``weight <= tol`` is zero
@@ -480,15 +480,15 @@
     the list of positions with support
 """
     from .measures import support
     return support(self.positions, self.weights, tol)
 
   def __weights(self):
     from mystic.math.measures import _pack
-    from numpy import product
+    from numpy import prod as product
     weights = _pack(self.wts)
     _weights = []
     for wts in weights:
       _weights.append(product(wts))
     return _weights
 
   def __positions(self):
@@ -766,45 +766,45 @@
   # for i in range(self.npts):
   #   #if f(self.positions[i]) > 0.0:  #NOTE: f(x) > 0.0 yields prob of success
   #   if f(self.positions[i]) <= 0.0:  #NOTE: f(x) <= 0.0 yields prob of failure
   #     u += self.weights[i]
   # return u  #XXX: does this need to be normalized?
 
   def sampled_minimum(self, f, npts=10000, map=None):
-    """use sampling to calculate ess_minimum for a given function
+    """use sampling to calculate minimum for the support for a given function
 
 Args:
     f (func): a function that takes a list and returns a number
     npts (int, default=10000): the number of point masses sampled from the
         underlying discrete measures
     map (func, default=builtins.map): the mapping function
 
 Returns:
-    the sampled ess_minimum, a float
+    the sampled ``ess_minimum``, a float
 
 Notes:
     - the function ``f`` should take a list of ``positions`` (for example,
       ``scenario.positions`` or ``product_measure.positions``) and return a
       single value (e.g. 0.0)
 """
     from mystic.math.samples import _minimum_given_samples
     pts = self.sampled_support(npts)
     return _minimum_given_samples(f, pts, map)
 
   def sampled_ptp(self, f, npts=10000, map=None):
-    """use sampling to calculate ess_|maximum - minimum| for a given function
+    """use sampling to calculate spread for the support for a given function
 
 Args:
     f (func): a function that takes a list and returns a number
     npts (int, default=10000): the number of point masses sampled from the
         underlying discrete measures
     map (func, default=builtins.map): the mapping function
 
 Returns:
-    the sampled |ess_maximum - ess_minimum|, a float
+    the sampled ``|ess_maximum - ess_minimum|``, a float
 
 Notes:
     - the function ``f`` should take a list of ``positions`` (for example,
       ``scenario.positions`` or ``product_measure.positions``) and return a
       single value (e.g. 0.0)
 """
     from mystic.math.samples import _ptp_given_samples
@@ -850,24 +850,24 @@
       single value (e.g. 0.0)
 """
     from mystic.math.samples import _variance_given_samples
     pts = self.sampled_support(npts)
     return _variance_given_samples(f, pts, map)
 
   def sampled_maximum(self, f, npts=10000, map=None):
-    """use sampling to calculate ess_maximum for a given function
+    """use sampling to calculate maximum for the support for a given function
 
 Args:
     f (func): a function that takes a list and returns a number
     npts (int, default=10000): the number of point masses sampled from the
         underlying discrete measures
     map (func, default=builtins.map): the mapping function
 
 Returns:
-    the ess_maximum, a float
+    the ``ess_maximum``, a float
 
 Notes:
     - the function ``f`` should take a list of ``positions`` (for example,
       ``scenario.positions`` or ``product_measure.positions``) and return a
       single value (e.g. 0.0)
 """
     from mystic.math.samples import _maximum_given_samples
@@ -1431,15 +1431,15 @@
 # creators and destructors from parameter list
 
 def _mimic(samples, weights):
   """Generate a product_measure object from a list of N product measure
 positions and a list of N weights. The resulting product measure will
 mimic the original product measure's statistics, but be larger in size.
 
-For example:
+Examples:
     >>> smp = [[-6,3,6],[-2,4],[1]]
     >>> wts = [[.4,.2,.4],[.5,.5],[1.]]
     >>> c = compose(samples, weights)
     >>> d = _mimic(c.positions, c.weights)
     >>> c[0].center_mass == d[0].center_mass
     True
     >>> c[1].range == d[1].range
```

### Comparing `mystic-0.4.0/mystic/math/distance.py` & `mystic-0.4.1/mystic/math/distance.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 distances and norms for the legacy data module
 """
 debug = False 
 
@@ -87,15 +87,15 @@
   #FIXME: merge with lipschitz cone (distance/contains)
   from numpy import sum, asarray
   d = absolute_distance(x,xp) #XXX: ,dmin=2)
   return sum(L * d.T, axis=-1).T
 
 def _npts(*x):
   """get len(product measure), given lengths of each underlying measure"""
-  from numpy import product
+  from numpy import prod as product
   return product(x)
 
 def _get_xy(points):
   """extract the list of positions and the list of values for given points"""
   from numpy import asarray
   if hasattr(points, 'coords'):
     x  = points.coords
```

### Comparing `mystic-0.4.0/mystic/math/grid.py` & `mystic-0.4.1/mystic/math/grid.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 tools for generating points on a grid
 """
 
 def gridpts(q, dist=None):
@@ -150,15 +150,15 @@
     dim = nfact = len(result)
     prime = nfact == 1
     if ndim: result += [1] * (ndim - (nfact // ndim));  dim = ndim
     elif ones: result += [1] # add some 'randomness' by adding a "1"
     # if ones, mix in the 1s; otherwise, only use 1s when ndim < len(result)
     if ones: result = sorted(result, key=lambda v: random())
     else: result[:nfact] = sorted(result[:nfact], key=lambda v: random())
-    from numpy import product
+    from numpy import prod as product
     result = [product(result[i::dim]) for i in range(dim)]
     # if not ones, now needs a full sort to sort in the 1s
     if not ones: result = sorted(result, key=lambda v: random())
     elif not ndim and 1 in result: result.remove(1) # remove the added "1"
     # if it's a prime, then do N-1 if exact=False
     if not exact and N > 3 and prime:
         result = randomly_bin(N-1, ndim, ones)
```

### Comparing `mystic-0.4.0/mystic/math/integrate.py` & `mystic-0.4.1/mystic/math/integrate.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 math tools related to integration
 """
 
 # INTEGRATE #
@@ -119,15 +119,15 @@
     2. http://en.wikipedia.org/wiki/Monte_Carlo_integration
     3. http://math.fullerton.edu/mathews/n2003/MonteCarloMod.html
 """
   from mystic.math.stats import volume
   from mystic.math.samples import random_samples
   vol = volume(lb, ub)
   x = [random_samples(lb, ub, npts=1) for k in range(1, n+1)]
-  r = map(f, x)  #FIXME: , nnodes=nnodes, launcher=launcher)
+  r = map(f, x)
   s = sum(r)[0]
   I = (vol/n)*s
   return float(I)
 
 
 # ALTERNATE: STATISTICS SPECIAL CASES #
 def __uniform_integrated_mean(lb,ub):
```

### Comparing `mystic-0.4.0/mystic/math/interpolate.py` & `mystic-0.4.1/mystic/math/interpolate.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """functions related to interpolation
 1-D and n-D interpolation, building a grid of points, calculating gradients
 """
 #XXX: interpf produces f(*x) and gradient takes f(*x), use f(x) instead?
 #XXX: make interpolation more accurate, at least on the given data points?
@@ -13,37 +13,37 @@
 
 from mystic.math import _rbf
 Rbf = _rbf.Rbf
 
 def extrapolate(x, z=None, method=None, mins=None, maxs=None, **kwds):
     '''extrapolate a bounding-box for the given points
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
-      z: an array of shape (npts,)
-      method: a function f(x) to generate new points; if None, use f(x) = nan
-      mins: a list of floats defining minima of the bounding box, or None
-      maxs: a list of floats defining maxima of the bounding box, or None
-      all: if True, include the initial (x,z) points in the return
-
-    Output:
-      a tuple of (x,z) containing the requested boundbox points
-
-    NOTE:
-      if z is None, return a tuple (x,) with the requested boundbox points.
-
-    NOTE:
-      if mins is None, then use the minima found in x. Similarly for maxs.
-
-    NOTE:
-      method can take a function, None, a boolean, or a string. If method is
-      True, interpolate a cost function using interpf with method='thin_plate'
-      (or 'rbf' if scipy is not found). If method is False, return the original
-      input. Alternately, method can be any one of ('rbf','linear','cubic',
-      'nearest','inverse','gaussian','multiquadric','quintic','thin_plate').
+    Args:
+      x (ndarray): an input array of shape ``(npts, dim)`` or ``(npts,)``
+      z (ndarray, default=None): an output array of shape ``(npts,)``
+      method (function, default=None): evaluate as ``z = f(x)`` for new ``x``
+      mins (list[float], default=None): list of the minima of the bounding box
+      maxs (list[float], default=None): list of the maxima of the bounding box
+      all (bool, default=True): include initial ``(x,z)`` points in the return
+
+    Returns:
+      a tuple of ``(x,z)`` containing the requested boundbox points
+
+    Notes:
+      - if ``z`` is None, return the tuple ``(x,)`` at the requested boundbox
+        points.
+      - if ``mins`` is None, then use the minima found in ``x``. Similarly for
+        ``maxs``.
+      - ``method`` can take a function, None, a bool, or a string. If ``method``
+        is True, interpolate a cost function using ``interpf`` with
+        ``method='thin_plate'`` (or ``'rbf'`` if ``scipy`` is not found).
+        If ``method`` is False, return the original input. Alternately,
+        ``method`` can be any one of ``('rbf', 'linear', 'cubic', 'nearest',
+        'inverse', 'gaussian', 'multiquadric', 'quintic', 'thin_plate')``.
+        If ``method`` is None, return ``nan`` upon new input.
     '''
     kwds.setdefault('all', True)
     import numpy as np
     output = True
     if z is None:
         z = np.nan * np.ones(len(x))
         output = False
@@ -66,27 +66,27 @@
     z = np.array(mon._y, dtype=ztype) if ztype else mon._y
     return (x,z) if output else x
 
 
 def _boundbox(monitor, fx=None, mins=None, maxs=None, **kwds):
     '''produce a bounding-box to facilitate interpolation at the given points
 
-    Input:
-      monitor: a mystic monitor instance
-      fx: a function f(x) to evaluate at new points; if None, use f(x) = nan
-      mins: a list of floats defining minima of the bounding box, or None
-      maxs: a list of floats defining maxima of the bounding box, or None
-      all: if True, include the initial monitor points in the return
+    Args:
+      monitor (monitor): a mystic monitor instance of existing points
+      fx (function, default=None): evaluate as ``z = f(x)`` for new ``x``
+      mins (list[float], default=None): list of the minima of the bounding box
+      maxs (list[float], default=None): list of the maxima of the bounding box
+      all (bool, default=True): include initial ``monitor`` points in the return
 
-    Output:
+    Returns:
       a mystic monitor instance containing the requested boundbox points
 
-    NOTE:
-      if mins is None, then use the minima found in the monitor instance.
-      Similarly for maxs.
+    Notes:
+      - if ``mins`` is None, then use the minima found in the ``monitor``.
+        Similarly for ``maxs``.
     '''
     all = kwds['all'] if 'all' in kwds else False
 
     import numpy as np
     f = (lambda x: np.nan) if fx is None else fx
 
     from mystic.monitors import Monitor                #XXX: copy or not?
@@ -117,57 +117,74 @@
     del mins, maxs, x
     return mon + _mon if all else _mon #XXX: or mon.extend(_mon)?
 
 
 def _sort(x, y=None, param=0):
     '''sort x (and y, if provided) by the given parameter
 
-    For example:
-    >>> _sort([[1,5,9],[7,8,3],[4,2,6]], param=0)
-    array([[1, 5, 9],
-           [4, 2, 6],
-           [7, 8, 3]])
-    >>> _sort([[1,5,9],[7,8,3],[4,2,6]], param=1)
-    array([[4, 2, 6],
-           [1, 5, 9],
-           [7, 8, 3]])
-    >>> _sort([[1,5,9],[7,8,3],[4,2,6]], [4,3,2])
-    (array([[1, 5, 9],
-           [4, 2, 6],
-           [7, 8, 3]]), array([4, 2, 3]))
-    >>>
+    Args:
+      x (ndarray): an array of shape ``(npts, nparam)``
+      y (ndarray, default=None): an array of shape ``(npts,)``
+      param (int, default=0): index of ``nparam`` upon which to sort
+
+    Returns:
+      sorted ``x``, or tuple of sorted ``(x,y)`` if ``y`` is provided
+
+    Examples:
+      >>> _sort([[1,5,9],[7,8,3],[4,2,6]], param=0)
+      array([[1, 5, 9],
+             [4, 2, 6],
+             [7, 8, 3]])
+
+      >>> _sort([[1,5,9],[7,8,3],[4,2,6]], param=1)
+      array([[4, 2, 6],
+             [1, 5, 9],
+             [7, 8, 3]])
+
+      >>> _sort([[1,5,9],[7,8,3],[4,2,6]], [4,3,2])
+      (array([[1, 5, 9],
+             [4, 2, 6],
+             [7, 8, 3]]), array([4, 2, 3]))
     '''
     import numpy as np
     x = np.asarray(x)
     i = np.argsort(x, axis=0)[:, param]
     if y is None:
         return x[i]
     y = np.asarray(y)
     return x[i],y[i]
 
 
 def _isin(i, x):
-    '''check if i is in x, where i is an iterable'''
+    '''check if i is in iterable x
+
+    Args:
+      i (ndarray): an array of shape ``(npts,)``, or a scalar value
+      x (ndarray): an array of shape ``(npts, nparam)`` or higher dimension
+
+    Returns:
+      True, if ``x`` contains ``i``
+    '''
     import numpy as np
     x = np.asarray(x) #XXX: doesn't verify that i is iterable
     if x.ndim == 1: #FIXME: expects i not nessarily an iterable
         return np.equal(i,x).any()
     return np.equal(i,x).all(axis=-1).any()
 
 
 def _to_objective(function):
-    '''convert f(*xargs, **kwds) to f(x, *args, **kwds) where xargs=x+args
+    '''convert ``f(*xargs, **kwds)`` to ``f(x, *args, **kwds)``, where ``xargs = x + args``
 
-    Input:
-      objective: a function of the form f(*xargs, **kwds)
+    Args:
+      function (function): a function of the form ``f(*xargs, **kwds)``
 
-    Output:
-      a function of the form f(x, *args, **kwds)
+    Returns:
+      a function of the form ``f(x, *args, **kwds)``
 
-    For example:
+    Examples:
       >>> @_to_objective
       ... def cost(x,y,z):
       ...   return x+y+z
       ... 
       >>> x = [1,2,3]
       >>> cost(x)
       6
@@ -175,24 +192,24 @@
     def objective(x, *args, **kwds):
         return function(*(tuple(x)+args), **kwds)
     objective.__doc__ = function.__doc__
     return objective
 
 
 def _to_function(objective, ndim=None):
-    '''convert f(x, *args, **kwds) to f(*xargs, **kwds) where xargs=x+args
+    '''convert ``f(x, *args, **kwds)`` to ``f(*xargs, **kwds)``, where ``xargs = x + args``
 
-    Input:
-      objective: a function of the form f(x, *args, **kwds)
-      ndim: an int, if provided, is the length of x in f(x, *args, **kwds)
+    Args:
+      objective (function): a function of the form ``f(x, *args, **kwds)``
+      ndim (int, default=None): the length of ``x`` in ``f(x, *args, **kwds)``
 
-    Output:
-      a function of the form f(*xargs, **kwds)
+    Returns:
+      a function of the form ``f(*xargs, **kwds)``
 
-    For example:
+    Examples:
       >>> @_to_function
       ... def model(x):
       ...   return sum(x)
       ... 
       >>> model(1,2,3)
       6
     '''
@@ -204,51 +221,82 @@
         def function(*args, **kwds):
             return obj(args[:ndim], *args[ndim:], **kwds)
     function.__doc__ = objective.__doc__
     return function
 
 
 def _array(x): #XXX: remove?
-    '''convert lists or values to numpy arrays''' 
+    '''convert lists or values to numpy arrays
+
+    Args:
+      x (list): a list of values (or a scalar value)
+
+    Returns:
+      ``x`` cast as a ``numpy`` array (or ``numpy`` scalar)
+    ''' 
     import numpy as np
     return np.asarray(x)
 
 
 def _nonarray(x): #XXX: move to tools?
-    '''convert arrays (or lists of arrays) to values or (lists of values)''' 
+    '''convert arrays (or lists of arrays) to values or (lists of values)
+
+    Args:
+      x (ndarray): an array of values (or a ``numpy`` scalar)
+
+    Returns:
+      ``x`` cast as a list (or a scalar value)
+    ''' 
     return x.tolist() if hasattr(x, 'dtype') else ([i.tolist() for i in x] if hasattr(x, '__len__') else x)
 
 
 def _to_nonarray(f): #XXX: move to tools?
-    '''return a function where the return does not contain numpy arrays'''
+    '''return a function where the return does not contain numpy arrays
+
+    Args:
+      f (function): a callable that returns an array (or scalar)
+
+    Returns:
+      a function with the return value of ``f`` cast as a list (or scalar)
+    '''
     def func(*args, **kwds):
         return _nonarray(f(*args, **kwds))
     #func.__name__ = f.__name__ #XXX: do name-mangling?
     #func.__doc__ = f.__doc__ #XXX: append that no arrays are returned?
     return func
 
 
 def _to_array(f): #XXX: move to tools?
-    '''return a function where the return is a numpy array'''
+    '''return a function where the return is a numpy array
+
+    Args:
+      f (function): a callable that returns a list (or scalar)
+
+    Returns:
+      a function with the return value of ``f`` cast as an array (or scalar)
+    '''
     def func(*args, **kwds):
         return _array(f(*args, **kwds))
     return func
 
 
 def _unique(x, z=None, sort=False, index=False): #XXX: move to tools?
     '''return the unique values of x, and corresponding z (if provided)
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
-      z: an array of shape (npts,)
-      sort: boolean, if True, return arrays sorted on x [default=True]
-      index: boolean, if True, also return an index array that recovers x
-
-    Output:
-      unique (potentially sorted) x, and z (if provided) and/or index
+    Args:
+      x (ndarray): an input array of shape ``(npts, dim)`` or ``(npts,)``
+      z (ndarray, default=None): an ouput array of shape ``(npts,)``
+      sort (bool, default=False): if True, return arrays sorted on ``x``
+      index (bool, default=False): also return an index array to recover ``x``
+
+    Returns:
+      an array of the unique elements of ``x``, or a tuple ``(x, z)`` if ``z``
+      is provided. If ``index`` is True, also return an array of indicies that
+      can be used to recover the original ``x`` array. If ``sort`` is True,
+      the returned arrays will be sorted on ``x``.
     ''' # avoid LinAlgError when interpolating
     import numpy as np
     x,i,v = np.unique(x, return_index=True, return_inverse=True, axis=0)
     if not z is None: z = np.asarray(z)[i]
     if not sort:
         i = i.argsort()
         x = x[i]
@@ -261,134 +309,143 @@
         return (x, z, v) if (not z is None) else (x,v)
     return (x, z) if (not z is None) else x
 
 
 def sort_axes(*axes, **kwds):
     '''sort axes along the selected primary axis
 
-    Input:
-      axes: a tuple of arrays of points along each axis
-      axis: an integer corresponding to the axis upon which to sort
+    Args:
+      axes (tuple[ndarray]): a tuple of arrays of points along each axis
+      axis (int, default=0): index of the axis upon which to sort
 
-    Output:
-      a tuple of arrays sorted with regard to the selected axis
+    Returns:
+      a tuple of arrays sorted with respect to the selected axis
     ''' #NOTE: last entry might be 'values' (i.e. f(x))
     import numpy as np
     #XXX: add an option (or new function) for monotonic increasing?
     # instead of string matching, use dict lookup
     axes = np.asarray(axes)
     axis = kwds['axis'] if 'axis' in kwds else 0
     i = axes[axis].argsort()
     return tuple(ax[i] for ax in axes)
 
 
 def axes(mins, maxs, npts=None):
     '''generate a tuple of arrays defining axes on a grid, given bounds
 
-    Input:
-      mins: a tuple of lower bounds for coordinates on the grid
-      maxs: a tuple of upper bounds for coordinates on the grid
-      npts: a tuple of grid shape, or integer number or points on grid
+    Args:
+      mins (tuple[float]): lower bounds for coordinates on the grid
+      maxs (tuple[float]): upper bounds for coordinates on the grid
+      npts (tuple[int]): number of grid points per axis, or integer if equal
 
-    Output:
+    Returns:
       a tuple of arrays defining the axes of the coordinate grid
 
-    NOTE:
-      If npts is not provided, a default of 50 points in each direction is used.
+    Notes:
+      If ``npts`` is None, a default of 50 points in each direction is used.
     ''' #NOTE: ensures all axes will be ordered (monotonically increasing)
     import numpy as np
     if not hasattr(mins, '__len__'):
         mins = (mins,)
     if not hasattr(maxs, '__len__'):
         maxs = (maxs,)
     if npts is None: npts = 50**len(mins) #XXX: better default?
     if not hasattr(npts, '__len__'):
         npts = (max(int(npts**(1./len(mins))),1),)*len(mins)
     return tuple(np.linspace(*r) for r in zip(mins,maxs,npts))
 
 
 def _swapvals(x, i):
-    '''swap values from column 0 with column i'''
+    '''swap values from column 0 in ``x`` with column i
+
+    Args:
+      x (ndarray): an array of shape ``(npts, ndim)``
+      i (int): index of column to swap with column 0
+
+    Returns:
+      an array where the indicated columns have been swapped
+    '''
     x = np.asarray(x).T
     x[[0,i]] = x[[i,0]]
     return x.T
 
 
 def _axes(x):
-    '''convert measured data 'x' to a tuple of 'axes'
+    '''convert array of measured points ``x`` to a tuple of coordinate axes
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
+    Args:
+      x (ndarray): an array of shape ``(npts, dim)`` or ``(npts,)``
 
-    Output:
-      a tuple of arrays (x0, ..., xm), where m = dim-1 and len(xi) = npts
+    Returns:
+      tuple of arrays ``(x0, ..., xm)`` with ``m = dim-1`` and length ``npts``
     '''
     import numpy as np
     x = np.asarray(x)
     if x.ndim == 1:
         return (x,)
     return tuple(x.T)
 
 
 def grid(*axes):
     '''generate tuple of (irregular) coordinate grids, given coordinate axes
 
-    Input:
-      axes: a tuple of arrays defining the axes of the coordinate grid
+    Args:
+      axes (tuple[ndarray]): arrays defining the axes of the coordinate grid
 
-    Output:
-      the resulting coordinate grid
+    Returns:
+      a tuple of ndarrays representing the resulting coordinate grid
     '''
     import numpy as np #FIXME: fails large len(axes)
     return tuple(np.meshgrid(*axes, indexing='ij'))
 
 
 def _noisy(x, scale=1e-8): #XXX: move to tools?
-    '''add random gaussian noise of the given scale, or None if scale=None
+    '''add random gaussian noise of the given scale, or None if ``scale=None``
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
+    Args:
+      x (ndarray): an array of shape ``(npts, dim)`` or ``(npts,)``
+      scale (float, default=1e-8): amplitude of the additive gaussian noise
 
-    Output:
-      an array of shape (npts, dim) or (npts,), where noise has been added
+    Returns:
+      array of shape ``(npts, dim)`` or ``(npts,)``, where noise has been added
     '''
     import numpy as np
     return x if not scale else x + np.random.normal(scale=scale, size=x.shape)
 
 
 def interpolate(x, z, xgrid, method=None, extrap=False, arrays=True, **kwds):
-    '''interpolate to find z = f(x) sampled at points defined by xgrid
+    '''interpolate to find ``z = f(x)`` sampled at points defined by ``xgrid``
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
-      z: an array of shape (npts,)
-      xgrid: (irregular) coordinate grid on which to sample z = f(x)
-      method: string for kind of interpolator
-      extrap: if True, extrapolate a bounding box (can reduce # of nans)
-      arrays: if True, z = f(x) is a numpy array; otherwise don't return arrays
-
-    Output:
-      interpolated points on a grid, where z = f(x) has been sampled on xgrid
-
-    NOTE:
-      if scipy is not installed, will use np.interp for 1D (non-rbf),
-      or mystic's rbf otherwise. default method is 'nearest' for
-      1D and 'linear' otherwise. method can be one of ('rbf','linear','cubic',
-      'nearest','inverse','gaussian','multiquadric','quintic','thin_plate').
-
-    NOTE:
-      if extrap is True, extrapolate using interpf with method='thin_plate'
-      (or 'rbf' if scipy is not found). Alternately, any one of ('rbf',
-      'linear','cubic','nearest','inverse','gaussian','multiquadric',
-      'quintic','thin_plate') can be used. If extrap is a cost function
-      z = f(x), then directly use it in the extrapolation.
-
-    NOTE:
-      additional keyword arguments (epsilon, smooth, norm) are avaiable for use
-      with a Rbf interpolator. See mystic.math.interpolate.Rbf for more details.
+    Args:
+      x (ndarray): an input array of shape ``(npts, dim)`` or ``(npts,)``
+      z (ndarray): an output array of shape ``(npts,)``
+      xgrid (ndarray): irregular coordinate grid on which to sample ``z = f(x)``
+      method (str, default=None): string name of the kind of interpolator
+      extrap (bool, default=False): if True, extrapolate a bounding box
+      arrays (bool, default=True): return ``z = f(x)`` as a numpy array
+
+    Returns:
+      interpolated points, where ``z = f(x)`` is sampled on ``xgrid``
+
+    Notes:
+      - if ``scipy`` is not installed, will use ``numpy.interp`` for 1D
+        (non-rbf), or ``rbf`` from ``mystic`` otherwise. Default method is
+        ``'nearest'`` for 1D, and is ``'linear'`` otherwise. ``method`` can
+        be one of ``('rbf', 'linear', 'cubic', 'nearest', 'inverse',
+        'gaussian', 'multiquadric', 'quintic', 'thin_plate')``.
+      - if ``extrap`` is True, extrapolate using ``interpf`` with 
+        ``method='thin_plate'`` (or ``'rbf'`` if ``scipy`` is not installed).
+        Alternately, any one of ``('rbf', 'linear', 'cubic', 'nearest',
+        'inverse', 'gaussian', 'multiquadric', 'quintic', 'thin_plate')`` can
+        be used. If ``extrap`` is a cost function ``z = f(x)``, then directly
+        use it in the extrapolation. Using extrapolation can reduce the number
+        of ``nan``.
+      - additional keyword arguments ``(epsilon, smooth, norm)`` are avaiable
+        for use with a Rbf interpolator. See ``mystic.math.interpolate.Rbf``
+        for more details.
     '''
     if arrays:
         _f, _fx = _to_array, _array
     else:
         _f, _fx = _to_nonarray, _nonarray
     x,z = extrapolate(x,z,method=extrap)
     x,z = _unique(x,z,sort=True)
@@ -417,42 +474,42 @@
     # method = 'nearest' -> NearestNDInterpolator
     # method = 'cubic' -> (1D: spline; 2D: CloughTocher2DInterpolator)
     return _fx(si.griddata(x, z, xgrid, method=method))#, rescale=False)
     #XXX: should the extrapolated points be removed?
 
 
 def _interpf(x, z, method=None, extrap=False, arrays=False, **kwds):
-    '''interpolate to find f, where z = f(*x)
+    '''interpolate to produce function ``f``, where ``z = f(*x)``
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
-      z: an array of shape (npts,)
-      method: string for kind of interpolator
-      extrap: if True, extrapolate a bounding box (can reduce # of nans)
-      arrays: if True, z = f(*x) is a numpy array; otherwise don't use arrays
-
-    Output:
-      interpolated function f, where z = f(*x)
-
-    NOTE:
-      if scipy is not installed, will use np.interp for 1D (non-rbf),
-      or mystic's rbf otherwise. default method is 'nearest' for
-      1D and 'linear' otherwise. method can be one of ('rbf','linear','cubic',
-      'nearest','inverse','gaussian','multiquadric','quintic','thin_plate').
-
-    NOTE:
-      if extrap is True, extrapolate using interpf with method='thin_plate'
-      (or 'rbf' if scipy is not found). Alternately, any one of ('rbf',
-      'linear','cubic','nearest','inverse','gaussian','multiquadric',
-      'quintic','thin_plate') can be used. If extrap is a cost function
-      z = f(x), then directly use it in the extrapolation.
-
-    NOTE:
-      additional keyword arguments (epsilon, smooth, norm) are avaiable for use
-      with a Rbf interpolator. See mystic.math.interpolate.Rbf for more details.
+    Args:
+      x (ndarray): an input array of shape ``(npts, dim)`` or ``(npts,)``
+      z (ndarray): an output array of shape ``(npts,)``
+      method (str, default=None): string name of the kind of interpolator
+      extrap (bool, default=False): if True, extrapolate a bounding box
+      arrays (bool, default=False): return ``z = f(*x)`` as a numpy array
+
+    Returns:
+      interpolated function ``f``, where ``z = f(*x)``
+
+    Notes:
+      - if ``scipy`` is not installed, will use ``numpy.interp`` for 1D
+        (non-rbf), or ``rbf`` from ``mystic`` otherwise. Default method is
+        ``'nearest'`` for 1D, and is ``'linear'`` otherwise. ``method`` can
+        be one of ``('rbf', 'linear', 'cubic', 'nearest', 'inverse',
+        'gaussian', 'multiquadric', 'quintic', 'thin_plate')``.
+      - if ``extrap`` is True, extrapolate using ``interpf`` with 
+        ``method='thin_plate'`` (or ``'rbf'`` if ``scipy`` is not installed).
+        Alternately, any one of ``('rbf', 'linear', 'cubic', 'nearest',
+        'inverse', 'gaussian', 'multiquadric', 'quintic', 'thin_plate')`` can
+        be used. If ``extrap`` is a cost function ``z = f(x)``, then directly
+        use it in the extrapolation. Using extrapolation can reduce the number
+        of ``nan``.
+      - additional keyword arguments ``(epsilon, smooth, norm)`` are avaiable
+        for use with a Rbf interpolator. See ``mystic.math.interpolate.Rbf``
+        for more details.
     ''' #XXX: return f(*x) or f(x)?
     if arrays:
         _f, _fx = _to_array, _array
     else:
         _f, _fx = _to_nonarray, _nonarray
     if len(x) > len(z): # if len(x) < len(z), points are dropped
         x = x[:len(z)]  # drop points
@@ -488,17 +545,20 @@
     #    return lambda xn: _fx(si.spline(x, z, xn))
     return _f(si.CloughTocher2DInterpolator(x, z, rescale=False))
 
 
 def _getaxis(z, axis):
     """get the selected axis of the multi-valued array
 
-    Inputs:
-      z: an array of shape (npts, N)
-      axis: int, the desired index the multi-valued array [0,N]
+    Args:
+      z (ndarray): an array of shape ``(npts, N)``
+      axis (int): index of the desired column of the multi-valued array ``z``
+
+    Returns:
+      array of shape ``(npts,)`` corresponding to the selected column of ``z``
     """
     if len(z) and not hasattr(z[0], '__len__'):
         msg = "cannot get axis=%s for single-valued array" % axis
         raise ValueError(msg)
     if axis is None:
         axis = slice(None)
     elif len(z) and axis >= len(z[0]):
@@ -510,45 +570,46 @@
     # select values corresponding to axis
     if type(z) not in (list, tuple):
         return z[:,axis]
     return type(z)(i[axis] for i in z)
 
 
 def interpf(x, z, method=None, extrap=False, arrays=False, **kwds):
-    '''interpolate (x,z) to generate f, where z=f(*x)
+    '''interpolate ``(x,z)`` to generate ``f``, where ``z = f(*x)``
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
-      z: an array of shape (npts, N)
-      method: string for kind of interpolator
-      extrap: if True, extrapolate a bounding box (can reduce # of nans)
-      arrays: if True, z = f(*x) is a numpy array; otherwise don't use arrays
-      axis: int in [0,N], the axis of z to interpolate (all, by default)
-      axmap: map instance, to execute each axis in parallel (None, by default)
-
-    Output:
-      interpolated function f, where z=f(*x)
-
-    NOTE:
-      if scipy is not installed, will use np.interp for 1D (non-rbf),
-      or mystic's rbf otherwise. default method is 'nearest' for
-      1D and 'linear' otherwise. method can be one of ('rbf','linear','cubic',
-      'nearest','inverse','gaussian','multiquadric','quintic','thin_plate').
-
-    NOTE:
-      if extrap is True, extrapolate using interpf with method='thin_plate'
-      (or 'rbf' if scipy is not found). Alternately, any one of ('rbf',
-      'linear','cubic','nearest','inverse','gaussian','multiquadric',
-      'quintic','thin_plate') can be used. If extrap is a cost function
-      z = f(x), then directly use it in the extrapolation.
-
-    NOTE:
-      additional keyword arguments (epsilon, smooth, norm) are avaiable
-      for use with a Rbf interpolator. See mystic.math.interpolate.Rbf
-      for more details.
+    Args:
+      x (ndarray): an input array of shape ``(npts, dim)`` or ``(npts,)``
+      z (ndarray): an output array of shape ``(npts, N)``
+      method (str, default=None): string name of the kind of interpolator
+      extrap (bool, default=False): if True, extrapolate a bounding box
+      arrays (bool, default=False): return ``z = f(*x)`` as a numpy array
+      axis (int, default=None): index of ``z`` upon which to interpolate
+      axmap: (map, default=None): map instance to execute each axis in parallel
+
+    Returns:
+      interpolated function ``f``, where ``z = f(*x)``
+
+    Notes:
+      - if ``axis`` is None, then interpolate using all indicies of ``z``
+      - if ``axmap`` is None, then use the (sequential) map from ``builtins``
+      - if ``scipy`` is not installed, will use ``numpy.interp`` for 1D
+        (non-rbf), or ``rbf`` from ``mystic`` otherwise. Default method is
+        ``'nearest'`` for 1D, and is ``'linear'`` otherwise. ``method`` can
+        be one of ``('rbf', 'linear', 'cubic', 'nearest', 'inverse',
+        'gaussian', 'multiquadric', 'quintic', 'thin_plate')``.
+      - if ``extrap`` is True, extrapolate using ``interpf`` with 
+        ``method='thin_plate'`` (or ``'rbf'`` if ``scipy`` is not installed).
+        Alternately, any one of ``('rbf', 'linear', 'cubic', 'nearest',
+        'inverse', 'gaussian', 'multiquadric', 'quintic', 'thin_plate')`` can
+        be used. If ``extrap`` is a cost function ``z = f(x)``, then directly
+        use it in the extrapolation. Using extrapolation can reduce the number
+        of ``nan``.
+      - additional keyword arguments ``(epsilon, smooth, norm)`` are avaiable
+        for use with a Rbf interpolator. See ``mystic.math.interpolate.Rbf``
+        for more details.
     '''
     axis = kwds.get('axis', None)
     _map = kwds.get('axmap', kwds.get('map', map)) # backward compatibility
     if _map is None: _map = map
     _kwd = dict(method=method, extrap=extrap, arrays=arrays)
     if 'norm' in kwds: _kwd['norm'] = kwds.pop('norm')
     if 'smooth' in kwds: _kwd['smooth'] = kwds.pop('smooth')
@@ -575,67 +636,69 @@
             #function.__axis__ = [interpf(x, z, axis=ax, **_kwd) for ax,val in enumerate(z[0])]
             return function
     else:
         z = _getaxis(z, axis)
     #XXX: what if dataset is empty? (i.e. len(data.values) == 0)
     #NOTE: the following is the same as Interpolator(...)._interpolate(...)
     import numpy as np
-    with np.warnings.catch_warnings():
-        np.warnings.filterwarnings('ignore')
+    import warnings
+    with warnings.catch_warnings():
+        warnings.filterwarnings('ignore')
         function = _interpf(x, z, **_kwd)
     # from mystic.math.interpolate import _to_objective
     # function = _to_objective(function)
     function.__axis__ = axis #XXX: bad idea: list of funcs, or int/None ?
     return function
 
 
 def _gradient(x, grid):
-    '''find gradient of f(x), sampled on the coordinate grid defined by x
-
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
-      grid: (irregular) coordinate grid of z = f(x), with axes = _axes(x)
-
-    Output:
-      list of length dim (or array in 1D), gradient of the points on grid
+    '''find gradient of ``f(x)`` sampled on the coordinate grid defined by ``x``
 
-    NOTE:
-      output will be of the form (dim,)+grid.shape
+    Args:
+      x (ndarray): an array of shape ``(npts, dim)`` or ``(npts,)``
+      grid (ndarray): irregular coordinate grid generated from ``z = f(x)``
+
+    Returns:
+      list of length ``dim`` for the gradient of the points on grid
+
+    Notes:
+      - output will be of the form ``(dim,) + grid.shape``.
+      - gradient on the grid calculated using tuple generated with ``_axes(x)``
     ''' #XXX: can unique be used in this function?
     import numpy as np
     err = np.seterr(all='ignore') # silence warnings (division by nan)
     z = np.gradient(grid, *_axes(x))
     np.seterr(**err)
     return z #XXX: for (N,1) & (N,), should return a tuple?
 
 
 def _fprime(x, fx, method=None, extrap=False, **kwds):
-    '''find gradient of fx at x, where fx is a function z=fx(x)
+    '''find gradient of ``fx`` at ``x``, with ``fx`` a function ``z = fx(x)``
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
-      fx: a function, z = fx(x)
-      method: string for kind of gradient method
-      extrap: if True, extrapolate a bounding box (can reduce # of nans)
-      new: if True, include the extrapolated points in the output
-
-    Output:
-      array of dimensions x.shape, gradient of the points at (x,fx)
-
-    NOTE:
-      if method is 'approx' (the default) use mystic's approx_fprime,
-      which uses a local gradient approximation; other choices are
-      'symbolic', which uses mpmath.diff if installed.
-
-    NOTE:
-      if extrap is True, extrapolate using interpf with method='thin_plate'
-      (or 'rbf' if scipy is not found). Alternately, any one of ('rbf',
-      'linear','cubic','nearest','inverse','gaussian','multiquadric',
-      'quintic','thin_plate') can be used. If extrap is a cost function
-      z = f(x), then directly use it in the extrapolation.
+    Args:
+      x (ndarray): an array of shape ``(npts, dim)`` or ``(npts,)``
+      fx (function): a function of form ``z = fx(x)``
+      method (str, default=None): string name of the kind of gradient method
+      extrap (bool, default=False): if True, extrapolate a bounding box
+      new (bool, default=False): include the extrapolated points in the output
+
+    Returns:
+      array of dimensions ``x.shape``, gradient of the points at ``(x,fx)``
+
+    Notes:
+      - if method is ``'approx'`` (the default), use ``approx_fprime`` from
+        ``mystic``, which uses a local gradient approximation; other choices
+        are ``'symbolic'``, which uses ``mpmath.diff`` if installed.
+      - if ``extrap`` is True, extrapolate using ``interpf`` with 
+        ``method='thin_plate'`` (or ``'rbf'`` if ``scipy`` is not installed).
+        Alternately, any one of ``('rbf', 'linear', 'cubic', 'nearest',
+        'inverse', 'gaussian', 'multiquadric', 'quintic', 'thin_plate')`` can
+        be used. If ``extrap`` is a cost function ``z = f(x)``, then directly
+        use it in the extrapolation. Using extrapolation can reduce the number
+        of ``nan``.
     '''
     slc = slice(None,None) if kwds.get('new', False) else slice(None,len(x))
     import numpy as np
     if extrap:
         x = extrapolate(x)
     x,i = _unique(x, index=True)
     if method is None or method == 'approx':
@@ -657,44 +720,43 @@
     np.seterr(**err)
     return z[i][slc]
     #XXX: should the extrapolated points be removed?
 
 
 #XXX: take f(*x) or f(x)?
 def gradient(x, fx, method=None, approx=True, extrap=False, **kwds):
-    '''find gradient of fx at x, where fx is a function z=fx(*x) or an array z
+    '''find gradient of ``fx`` at ``x``, with ``fx`` a function ``z = fx(*x)`` or an array ``z``
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
-      fx: an array of shape (npts,) **or** a function, z = fx(*x)
-      method: string for kind of interpolator
-      approx: if True, use local approximation method
-      extrap: if True, extrapolate a bounding box (can reduce # of nans)
-      new: if True, include the extrapolated points in the output
-
-    Output:
-      array of dimensions x.shape, gradient of the points at (x,fx)
-
-    NOTE:
-      if approx is True, use mystic's approx_fprime, which uses a local
-      gradient approximation; otherwise use numpy's gradient method which
-      performs a more memory-intensive calcuation on a grid.
-
-    NOTE:
-      if scipy is not installed, will use np.interp for 1D (non-rbf),
-      or mystic's rbf otherwise. default method is 'nearest' for
-      1D and 'linear' otherwise. method can be one of ('rbf','linear','cubic',
-      'nearest','inverse','gaussian','multiquadric','quintic','thin_plate').
-
-    NOTE:
-      if extrap is True, extrapolate using interpf with method='thin_plate'
-      (or 'rbf' if scipy is not found). Alternately, any one of ('rbf',
-      'linear','cubic','nearest','inverse','gaussian','multiquadric',
-      'quintic','thin_plate') can be used. If extrap is a cost function
-      z = f(x), then directly use it in the extrapolation.
+    Args:
+      x (ndarray): an array of shape ``(npts, dim)`` or ``(npts,)``
+      fx (ndarray): array of shape ``(npts,)`` **or** function ``z = f(*x)``
+      method (str, default=None): string name of the kind of gradient method
+      approx (bool, default=True): if True, use local approximation method
+      extrap (bool, default=False): if True, extrapolate a bounding box
+      new (bool, default=False): include the extrapolated points in the output
+
+    Returns:
+      array of dimensions ``x.shape``, gradient of the points at ``(x,fx)``
+
+    Notes:
+      - if ``approx`` is True, use ``approx_fprime`` from ``mystic``, which
+        uses a local gradient approximation; otherwise use ``gradient`` from
+        ``numpy``, which performs a memory-intensive calculation on a grid.
+      - if ``scipy`` is not installed, will use ``numpy.interp`` for 1D
+        (non-rbf), or ``rbf`` from ``mystic`` otherwise. Default method is
+        ``'nearest'`` for 1D, and is ``'linear'`` otherwise. ``method`` can
+        be one of ``('rbf', 'linear', 'cubic', 'nearest', 'inverse',
+        'gaussian', 'multiquadric', 'quintic', 'thin_plate')``.
+      - if ``extrap`` is True, extrapolate using ``interpf`` with 
+        ``method='thin_plate'`` (or ``'rbf'`` if ``scipy`` is not installed).
+        Alternately, any one of ``('rbf', 'linear', 'cubic', 'nearest',
+        'inverse', 'gaussian', 'multiquadric', 'quintic', 'thin_plate')`` can
+        be used. If ``extrap`` is a cost function ``z = f(x)``, then directly
+        use it in the extrapolation. Using extrapolation can reduce the number
+        of ``nan``.
     ''' #NOTE: uses 'unique' in all cases
     #XXX: nice to have a test for smoothness, worth exploring?
     slc = slice(None,None) if kwds.get('new', False) else slice(None,len(x))
     import numpy as np
     if not hasattr(fx, '__call__'):
         x, fx = extrapolate(x, fx, method=extrap)
         fx = _interpf(x, fx, method=method)
@@ -716,28 +778,29 @@
     idx = np.diag_indices(*x.shape)
     return np.array([j[idx] for j in gfx]).T[i][slc]
     #XXX: should the extrapolated points be removed?
 
 
 # SEE: https://stackoverflow.com/questions/31206443
 def _hessian(x, grid):
-    '''find hessian of f(x), sampled on the coordinate grid defined by x
+    '''find hessian of ``f(x)``, sampled on the coordinate grid defined by ``x``
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
-      grid: (irregular) coordinate grid of z = f(x), with axes = _axes(x)
-
-    Output:
-      array of shape indicated in NOTE, hessian of the points on grid
-
-    NOTE:
-      output will be of the form (dim,dim)+grid.shape, where output hess[i,j]
-      corresponds to the second derivative z_{i,j} with i,j in range(dim).
-      For a 1D array x, output will be a 1D array of the same length.
-      The hessian is calculated using finite differences.
+    Args:
+      x (ndarray): an array of shape ``(npts, dim)`` or ``(npts,)``
+      grid (ndarray): irregular coordinate grid generated from ``z = f(x)``
+
+    Returns:
+      array of shape indicated in Notes, the hessian of the points on grid
+
+    Notes:
+      - Output will be of the form ``(dim,dim) + grid.shape``, where the output
+        ``hess[i,j]`` corresponds to the second derivative ``z_{i,j}`` with
+        ``i,j`` in ``range(dim)``. For a 1D array ``x``, the output will be a
+        1D array of the same length. The hessian is calculated using finite
+        differences.
     ''' #XXX: can unique be used in this function?
     import numpy as np
     x =  np.asarray(x)
     hess = np.empty((grid.ndim, grid.ndim) + grid.shape, dtype=grid.dtype)
     if grid.ndim == 1: #XXX: is (1,1,N) really desirable when x is (N,1)?
         hess[0,0] = _gradient(x, _gradient(x, grid))
         return hess.ravel() if x.ndim == 1 else hess
@@ -746,56 +809,52 @@
         for l, grad_kl in enumerate(_gradient(x, grad_k)):
             hess[k,l] = grad_kl
     return hess
 
 
 #XXX: take f(*x) or f(x)?
 def hessian(x, fx, method=None, approx=True, extrap=False, **kwds):
-    '''find hessian of fx at x, where fx is a function z=fx(*x) or an array z
+    '''find hessian of ``fx`` at ``x``, with ``fx`` a function ``z = fx(*x)`` or an array ``z``
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
-      fx: an array of shape (npts,) **or** a function, z = fx(*x)
-      method: string for kind of interpolator
-      approx: if True, use local approximation method
-      extrap: if True, extrapolate a bounding box (can reduce # of nans)
-      new: if True, include the extrapolated points in the output
-
-    Output:
-      array of shape indicated in NOTE, hessian of the points at (x,fx)
-
-    NOTE:
-      output will be of the form x.shape+(dim,), where hess[:,i,j]
-      corresponds to the second derivative z_{i,j} with i,j in range(dim).
-      For a 1D array x, output will be a 1D array of the same length.
-      
-    NOTE:
-      if approx is True, first use interpolation to build gradient functions
-      in each direction, then use mystic's approx_fprime, which uses a local
-      gradient approximation; otherwise use numpy's gradient method which
-      performs a more memory-intensive calcuation on a grid.
-
-    NOTE:
-      if scipy is not installed, will use np.interp for 1D (non-rbf),
-      or mystic's rbf otherwise. default method is 'nearest' for
-      1D and 'linear' otherwise. method can be one of ('rbf','linear','cubic',
-      'nearest','inverse','gaussian','multiquadric','quintic','thin_plate').
-
-    NOTE:
-      method string can provide either one or two methods (i.e. 'rbf
-      or 'rbf, cubic'), where if two methods are provided, the first
-      will be used to interpolate f(x) and the second will be used to
-      interpolate the gradient of f(x).
-
-    NOTE:
-      if extrap is True, extrapolate using interpf with method='thin_plate'
-      (or 'rbf' if scipy is not found). Alternately, any one of ('rbf',
-      'linear','cubic','nearest','inverse','gaussian','multiquadric',
-      'quintic','thin_plate') can be used. If extrap is a cost function
-      z = f(x), then directly use it in the extrapolation.
+    Args:
+      x (ndarray): an array of shape ``(npts, dim)`` or ``(npts,)``
+      fx (ndarray): array of shape ``(npts,)`` **or** function ``z = f(*x)``
+      method (str, default=None): string name of the kind of interpolator
+      approx (bool, default=True): if True, use local approximation method
+      extrap (bool, default=False): if True, extrapolate a bounding box
+      new (bool, default=False): include the extrapolated points in the output
+
+    Returns:
+      array of shape indicated in Notes, the hessian of the points at ``(x,fx)``
+
+    Notes:
+      - output will be of the form ``x.shape + (dim,)``, where ``hess[:,i,j]``
+        corresponds to the second derivative ``z_{i,j}`` with ``i,j`` in
+        ``range(dim)``. For a 1D array ``x``, output will be a 1D array of
+        the same length.
+      - if ``approx`` is True, first use interpolation to build gradient
+        functions in each direction, then use ``approx_fprime`` from ``mystic``,
+        which uses a local gradient approximation; otherwise use ``gradient``
+        from ``numpy``, which performs a memory-intensive calcuation on a grid.
+      - if ``scipy`` is not installed, will use ``numpy.interp`` for 1D
+        (non-rbf), or ``rbf`` from ``mystic`` otherwise. Default method is
+        ``'nearest'`` for 1D, and is ``'linear'`` otherwise. ``method`` can
+        be one of ``('rbf', 'linear', 'cubic', 'nearest', 'inverse',
+        'gaussian', 'multiquadric', 'quintic', 'thin_plate')``.
+      - method string can provide either one or two methods (i.e. ``'rbf'``
+        or ``'rbf, cubic'``), where if two methods are provided, the first
+        will be used to interpolate ``f(x)`` and the second will be used to
+        interpolate the gradient of ``f(x)``.
+      - if ``extrap`` is True, extrapolate using ``interpf`` with 
+        ``method='thin_plate'`` (or ``'rbf'`` if ``scipy`` is not installed).
+        Alternately, any one of ``('rbf', 'linear', 'cubic', 'nearest',
+        'inverse', 'gaussian', 'multiquadric', 'quintic', 'thin_plate')`` can
+        be used. If ``extrap`` is a cost function ``z = f(x)``, then directly
+        use it in the extrapolation. Using extrapolation can reduce the number
+        of ``nan``.
     ''' #NOTE: uses 'unique' in all cases
     slc = slice(None,None) if kwds.get('new', False) else slice(None,len(x))
     import numpy as np
     if method is None:
         method = (None,)
     else: #NOTE: accepts either 'one', 'one, two' or 'one; two'
         method = [s.strip() for s in method.replace(';',',').split(',')]
@@ -826,45 +885,44 @@
         hess.shape = x.shape #XXX: if (N,1), is (N,1,1) or (N,1) right shape?
         return hess[i][slc]
     idx = np.diag_indices(*x.shape)
     return np.array([[k[idx] for k in j] for j in hess]).T[i][slc] #XXX: shape?
 
 
 def hessian_diagonal(x, fx, method=None, approx=True, extrap=False, **kwds):
-    '''find hessian diagonal of fx at x, with fx a function z=fx(*x) or array z
+    '''find hessian diagonal of ``fx`` at ``x``, with ``fx`` a function ``z = fx(*x)`` or an array ``z``
 
-    Input:
-      x: an array of shape (npts, dim) or (npts,)
-      fx: an array of shape (npts,) **or** a function, z = fx(*x)
-      method: string for kind of interpolator
-      approx: if True, use local approximation method
-      extrap: if True, extrapolate a bounding box (can reduce # of nans)
-      new: if True, include the extrapolated points in the output
-
-    Output:
-      array of dimensions x.shape, hessian diagonal of the points at (x,fx)
-
-    NOTE:
-      if approx is True, first use interpolation to build gradient functions
-      in each direction, then use mystic's approx_fprime, which uses a local
-      gradient approximation; otherwise use numpy's gradient method which
-      performs a more memory-intensive calcuation on a grid.
-
-    NOTE:
-      if scipy is not installed, will use np.interp for 1D (non-rbf),
-      or mystic's rbf otherwise. default method is 'nearest' for
-      1D and 'linear' otherwise. method can be one of ('rbf','linear','cubic',
-      'nearest','inverse','gaussian','multiquadric','quintic','thin_plate').
-
-    NOTE:
-      if extrap is True, extrapolate using interpf with method='thin_plate'
-      (or 'rbf' if scipy is not found). Alternately, any one of ('rbf',
-      'linear','cubic','nearest','inverse','gaussian','multiquadric',
-      'quintic','thin_plate') can be used. If extrap is a cost function
-      z = f(x), then directly use it in the extrapolation.
+    Args:
+      x (ndarray): an array of shape ``(npts, dim)`` or ``(npts,)``
+      fx (ndarray): array of shape ``(npts,)`` **or** function ``z = f(*x)``
+      method (str, default=None): string name of the kind of interpolator
+      approx (bool, default=True): if True, use local approximation method
+      extrap (bool, default=False): if True, extrapolate a bounding box
+      new (bool, default=False): include the extrapolated points in the output
+
+    Returns:
+      array of dimensions ``x.shape``, the hessian diagonal of the points at ``(x,fx)``
+
+    Notes:
+      - if ``approx`` is True, first use interpolation to build gradient
+        functions in each direction, then use ``approx_fprime`` from ``mystic``,
+        which uses a local gradient approximation; otherwise use ``gradient``
+        from ``numpy``, which performs a memory-intensive calcuation on a grid.
+      - if ``scipy`` is not installed, will use ``numpy.interp`` for 1D
+        (non-rbf), or ``rbf`` from ``mystic`` otherwise. Default method is
+        ``'nearest'`` for 1D, and is ``'linear'`` otherwise. ``method`` can
+        be one of ``('rbf', 'linear', 'cubic', 'nearest', 'inverse',
+        'gaussian', 'multiquadric', 'quintic', 'thin_plate')``.
+      - if ``extrap`` is True, extrapolate using ``interpf`` with 
+        ``method='thin_plate'`` (or ``'rbf'`` if ``scipy`` is not installed).
+        Alternately, any one of ``('rbf', 'linear', 'cubic', 'nearest',
+        'inverse', 'gaussian', 'multiquadric', 'quintic', 'thin_plate')`` can
+        be used. If ``extrap`` is a cost function ``z = f(x)``, then directly
+        use it in the extrapolation. Using extrapolation can reduce the number
+        of ``nan``.
     '''
     hess = hessian(x, fx, method, extrap=extrap, **kwds)
     if hess.ndim != 3: # (i.e. is 1 or 2)
         return hess
     import numpy as np
     x = np.asarray(x)
     return np.array([hess[:,i,i] for i in range(x.ndim+1)]).T
```

### Comparing `mystic-0.4.0/mystic/math/legacydata.py` & `mystic-0.4.1/mystic/math/legacydata.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,46 +1,52 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 data structures for legacy data observations of lipschitz functions
 """
+__all__ = ['NULLSLOPE', '_fails', 'datapoint', 'dataset', 'lipschitzcone',
+           'point', 'save_dataset', 'load_dataset']
+
 from numpy import inf, asarray
 NULLSLOPE = inf
 
 def _fails(filter, data=None):
   """filter a data array for failures using a boolean filter
 
-  Inputs:
-    filter -- a list of booleans (same size as data)
-    data -- a list of data points
+Args:
+  filter (list): a list of booleans (same size as data) to filter the data
+  data (list, default=None): a list of data points
+
+Returns:
+  filtered list of data points
 
-  Notes:
-    if data=None, return the pairs of indices where data fails
+Notes:
+  - if ``data`` is None, return the pairs of indices where data fails
   """
   from numpy import where, asarray
   failures = asarray(where(filter == False)).T
   # if data not given, then return indices for failure
   if not data: return failures
   # otherwise, return the list of 'bad' points
   failures = set( failures.flat )
   return asarray([data[i] for i in failures])
 
 class lipschitzcone(list):
   """ Lipschitz double cone around a data point, with vertex and slope
 
- queries:
+ queries::
   vertex -- coordinates of lipschitz cone vertex
   slopes -- lipschitz slopes for the cone (should be same dimension as 'vertex')
 
- methods:
+ methods::
   contains -- return True if a given point is within the cone
   distance -- sum of lipschitz-weighted distance between a point and the vertex
 """
 
   def __init__(self, datapoint, slopes=None):
     self.vertex = datapoint
     if not slopes: slopes = [NULLSLOPE]*len(self.vertex.position)
@@ -69,20 +75,20 @@
     return abs(y - G) <= self.distance(point)
 
   pass
 
 class point(object):
   """ n-d data point with position and value but no id (i.e. 'raw')
 
- queries:
+ queries::
   p.value   --  returns value
   p.position  --  returns position
   p.rms  --  returns the square root of sum of squared position
 
- settings:
+ settings::
   p.value = v1  --  set the value
   p.position = (x1, x2, ..., xn)  --  set the position
 """
 
   def __init__(self, position, value):
     self.value = value
     self.position = position
@@ -139,23 +145,23 @@
 
   pass
 
 
 class datapoint(object):
   """ n-d data point with position and value 
 
- queries:
+ queries::
   p.value   --  returns value
   p.position  --  returns position
 
- settings:
+ settings::
   p.value = v1  --  set the value
   p.position = (x1, x2, ..., xn)  --  set the position
 
- notes:
+ notes::
   a datapoint can have an assigned id and cone;
   also has utilities for comparison against other
   datapoints (intended for use in a dataset)
 """
 
   __hash_id = id  # save a copy of the builtin id function
 
@@ -261,39 +267,39 @@
 
   pass
 
 class dataset(list):  #FIXME: should just accept datapoints
   """ a collection of data points
   s = dataset([point1, point2, ..., pointN])
 
- queries:
+ queries::
   s.values  --  returns list of values
   s.coords  --  returns list of positions
   s.ids  --  returns list of ids
   s.raw  --  returns list of points
   s.npts  --  returns the number of points
   s.lipschitz  --  returns list of lipschitz constants
 
- settings:
+ settings::
   s.lipschitz = [s1, s2, ..., sn]  --  sets lipschitz constants
 
- methods:
+ methods::
   short  -- check for shortness with respect to given data (or self)
   valid  -- check for validity with respect to given model
   update  -- update the positions and values in the dataset 
   load  -- load a list of positions and a list of values to the dataset 
   fetch  -- fetch the list of positions and the list of values in the dataset
   intersection  -- return the set intersection between self and query
   filter  -- return dataset entries where mask array is True 
   has_id  -- return True where dataset ids are in query
   has_position  -- return True where dataset coords are in query
   has_point  -- return True where dataset points are in query
   has_datapoint  -- return True where dataset entries are in query
 
- notes:
+ notes::
   - datapoints should not be edited; except possibly for id
   - assumes that s.n = len(s.coords) == len(s.values)
   - all datapoints in a dataset should have the same cone.slopes
 """
   # - when datapoint added to dataset, SHOULD build cone from dataset.lipschitz
   #   dataset.__set_id should check 'dataset.contains(id)', so no duplicate ids
 
@@ -513,16 +519,19 @@
   def intersection(self, query):
     "return the set intersection between self and query"
     return dataset(set(self).intersection(query))
 
   def filter(self, mask): #XXX: assumes len(mask) = len(self); mask[i] is bool
     """return dataset entries where mask array is True 
 
-Inputs:
-    mask -- a boolean array of the same length as dataset
+Args:
+    mask (ndarray[bool]): a boolean array of the same length as dataset
+
+Returns:
+    the filtered dataset
 """
     from numpy import array, where
     _self = array(self)
     return dataset(_self[where(mask)])
 
   def __data(self):
     return list(self)
@@ -593,18 +602,25 @@
 
 
 #######################################################
 # legacy data file IO
 #######################################################
 
 def load_dataset(filename, filter=None):
-  """ read dataset from selected file
+  """read dataset from selected file
 
-  filename -- string name of dataset file
-  filter -- tuple of points to select ('False' to ignore filter stored in file)
+Args:
+  filename (str): filepath of dataset file
+  filter (tuple, default=None): points to select
+
+Returns:
+  the stored ``mystic.math.legacydata.dataset``
+
+Notes:
+  - if `filter`` is False, ignore the filter stored in ``filename``
 """
   from os.path import split, splitext
   name = splitext(split(filename)[-1])[0]  # default name is filename
   lipschitz = None
   f = open(filename,"r")
   file = f.read()
   f.close()
@@ -643,18 +659,22 @@
   mydataset.__name__ = name
   mydataset.lipschitz = lipschitz
   return mydataset
 
 def save_dataset(data, filename='dataset.txt', filter=None, new=True):
   """ save dataset to selected file
 
-  data -- data set
-  filename -- string name of dataset file
-  filter -- tuple, filter to apply to dataset upon reading
-  new -- boolean, False if appending to existing file
+Args:
+  data (dataset): a ``mystic.math.legacydata.dataset``
+  filename (str, default='dataset.txt'): filepath of dataset file
+  filter (tuple, default=None): filter to apply to dataset upon reading
+  new (bool, default=True): if False, append to existing file
+
+Returns:
+  None
 """
   import datetime
   if new: ind = 'w'
   else: ind = 'a'
   file = open(filename, ind)
   file.write("# %s\n" % datetime.datetime.now().ctime() )
   if data.__name__: file.write('# data name: "%s"\n' % data.__name__ )
```

### Comparing `mystic-0.4.0/mystic/math/measures.py` & `mystic-0.4.1/mystic/math/measures.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Methods to support discrete measures
 """
 # what about sample_unsafe ?
 from mystic.math.stats import *
@@ -1695,19 +1695,21 @@
     """set all weights not appearing in 'index' to zero
 
 Inputs:
     samples -- a list of sample points
     weights -- a list of sample weights
     index -- a list of desired support indices (weights will be non-zero)
 
-For example:
+Examples:
     >>> impose_support([0,1],[1,2,3,4,5],[.2,.2,.2,.2,.2])
     ([2.5, 3.5, 4.5, 5.5, 6.5], [0.5, 0.5, 0.0, 0.0, 0.0])
+
     >>> impose_support([0,1,2,3],[1,2,3,4,5],[.2,.2,.2,.2,.2])
     ([1.5, 2.5, 3.5, 4.5, 5.5], [0.25, 0.25, 0.25, 0.25, 0.0])
+
     >>> impose_support([4],[1,2,3,4,5],[.2,.2,.2,.2,.2])
     ([-1.0, 0.0, 1.0, 2.0, 3.0], [0.0, 0.0, 0.0, 0.0, 1.0])
 
 Notes: is 'mean-preserving' for samples and 'norm-preserving' for weights
 """
     if index is None: index = range(len(weights))
     # allow negative indexing
@@ -1725,17 +1727,18 @@
 
 Inputs:
     samples -- a list of sample points
     weights -- a list of sample weights
     index -- a list of indices where weight is to be zero
     nullable -- if False, avoid null weights by reweighting non-index weights
 
-For example:
+Examples:
     >>> impose_unweighted([0,1,2],[1,2,3,4,5],[.2,.2,.2,.2,.2])
     ([-0.5, 0.5, 1.5, 2.5, 3.5], [0.0, 0.0, 0.0, 0.5, 0.5])
+
     >>> impose_unweighted([3,4],[1,2,3,4,5],[.2,.2,.2,.2,.2])
     ([2.0, 3.0, 4.0, 5.0, 6.0], [0.33333333333333331, 0.33333333333333331, 0.33333333333333331, 0.0, 0.0])
 
 Notes: is 'mean-preserving' for samples and 'norm-preserving' for weights
 """
     if index is None: index = ()
     # allow negative indexing
@@ -1756,17 +1759,18 @@
 with samples[j] = samples[i].
 
 Inputs:
     samples -- a list of sample points
     weights -- a list of sample weights
     pairs -- set of tuples of indices (i,j) where collapse occurs
 
-For example:
+Examples:
     >>> impose_collapse({(0,1),(0,2)},[1,2,3,4,5],[.2,.2,.2,.2,.2])
     ([1.5999999999999996, 1.5999999999999996, 1.5999999999999996, 4.5999999999999996, 5.5999999999999996], [0.6000000000000001, 0.0, 0.0, 0.2, 0.2])
+
     >>> impose_collapse({(0,1),(3,4)},[1,2,3,4,5],[.2,.2,.2,.2,.2])
     ([1.3999999999999999, 1.3999999999999999, 3.3999999999999999, 4.4000000000000004, 4.4000000000000004], [0.4, 0.0, 0.2, 0.4, 0.0])
 
 Notes: is 'mean-preserving' for samples and 'norm-preserving' for weights
 """
     samples, weights = list(samples), list(weights) # don't edit inputs
     m = mean(samples, weights)
@@ -1808,15 +1812,15 @@
 
 Inputs:
     mass -- target product of weights
     weights -- a list of sample weights
     zsum -- use counterbalance when mass = 0.0
     zmass -- member scaling when mass = 0.0
 """
-  from numpy import product
+  from numpy import prod as product
   weights = asarray(list(weights)) #XXX: faster to use x = array(x, copy=True) ?
   w = float(product(weights))
   n = len(weights)
   if not w:  #XXX: is this the best behavior?
     from numpy import inf
     return list(weights * inf)  # protect against ZeroDivision
   if float(mass):
@@ -1846,32 +1850,32 @@
 def _pack(samples):
   """'pack' a list of discrete measure sample points 
 into a list of product measure sample points
 
 Inputs:
     samples -- a list of sample points for N discrete measures
 
-For example:
-  >>> _pack([[1,2,3], [4,5], [6,7]])
-  [(1,4,6), (2,4,6), (3,4,6), (1,5,6), (2,5,6), (3,5,6), \
-   (1,4,7), (2,4,7), (3,4,7), (1,5,7), (2,5,7), (3,5,7)]
+Examples:
+    >>> _pack([[1,2,3], [4,5], [6,7]])
+    [(1,4,6), (2,4,6), (3,4,6), (1,5,6), (2,5,6), (3,5,6), \
+     (1,4,7), (2,4,7), (3,4,7), (1,5,7), (2,5,7), (3,5,7)]
 """
- #from numpy import product, array, ones
+ #from numpy import prod as product, array, ones
  #ndim = len(samples)
  #npts = [len(s) for s in samples]
  #z = []
  #for i in range(ndim):
  #  tmp = list(array([n*ones(product(npts[:i])) for n in samples[i]]).flatten())
  #  z.append( product(npts[i+1:])*tmp )
  #del tmp
  #zT = []
  #for i in range(len(z[0])):
  #  zT.append( tuple([y.pop(0) for y in z]) )
  #return zT
-# from numpy import product, array, ones
+# from numpy import prod as product, array, ones
 # ndim = len(samples)
 # npts = [len(s) for s in samples]
 # z = ones((ndim, product(npts)))  # z.T of what's needed
 # for i in range(ndim):
 #   tmp = list(array([n*ones(product(npts[:i])) for n in samples[i]]).flatten())
 #   z[i] = product(npts[i+1:])*tmp
 # return [tuple(i) for i in z.T]
@@ -1893,21 +1897,21 @@
   """'unpack' a list of product measure sample points 
 into a list of discrete measure sample points
 
 Inputs:
     samples -- a list of sample points for a product measure
     npts -- a tuple of dimensions of the target discrete measure
 
-For example:
-  >>> _unpack( [(1,4,6), (2,4,6), (3,4,6), (1,5,6), (2,5,6), (3,5,6), \
-  ...           (1,4,7), (2,4,7), (3,4,7), (1,5,7), (2,5,7), (3,5,7)], (3,2,2) \
-  ...        )
-  [[1,2,3], [4,5], [6,7]]
+Examples:
+    >>> _unpack([(1,4,6), (2,4,6), (3,4,6), (1,5,6), (2,5,6), (3,5,6), \
+    ...          (1,4,7), (2,4,7), (3,4,7), (1,5,7), (2,5,7), (3,5,7)], (3,2,2)\
+    ...        )
+    [[1,2,3], [4,5], [6,7]]
 """
-# from numpy import product, array
+# from numpy import prod as product, array
 # ndim = len(npts)
 # z = []
 # for i in range(ndim):
 #   tmp = array(samples[:int(len(samples)/product(npts[i+1:]))]).T[i]
 #   z.append( list(tmp[::int(product(npts[:i]))]) )
 # return z
   _samples = []
@@ -1930,15 +1934,15 @@
 def _flat(params):
   """
 converts a nested parameter list into flat parameter list
 
 Inputs:
     params -- a nested list of weights or positions
 
-For example:
+Examples:
     >>> par = [['x','x','x'], ['y','y'], ['z']]
     >>> _flat(par)
     ['x','x','x','y','y','z']
 """
   from mystic.tools import flatten
   return list(flatten(params))
 
@@ -1947,15 +1951,15 @@
   """
 converts a flat parameter list into nested parameter list
 
 Inputs:
     params -- a flat list of weights or positions
     npts -- a tuple describing the shape of the target list
 
-For example:
+Examples:
     >>> nx = 3;  ny = 2;  nz = 1
     >>> par = ['x']*nx + ['y']*ny + ['z']*nz
     >>> _nested(par, (nx,ny,nz))
     [['x','x','x'], ['y','y'], ['z']]
 """
   coords = []
   ind = 0
@@ -1970,15 +1974,15 @@
 splits a flat parameter list into a list of weights and a list of positions;
 weights and positions are expected to have the same dimensions (given by npts)
 
 Inputs:
     params -- a flat list of weights and positions (formatted as noted below)
     npts -- a tuple describing the shape of the target lists
 
-For example:
+Examples:
     >>> nx = 3;  ny = 2;  nz = 1
     >>> par = ['wx']*nx + ['x']*nx + ['wy']*ny + ['y']*ny + ['wz']*nz + ['z']*nz
     >>> weights, positions = _nested_split(par, (nx,ny,nz))
     >>> weights
     [['wx','wx','wx'], ['wy','wy'], ['wz']]
     >>> positions
     [['x','x','x'], ['y','y'], ['z']]
@@ -2000,15 +2004,15 @@
 and a flat list of positions;  weights and positions are expected
 to have the same dimensions (given by npts)
 
 Inputs:
     params -- a flat list of weights and positions (formatted as noted below)
     npts -- a tuple describing the shape of the target lists
 
-For example:
+Examples:
     >>> nx = 3;  ny = 2;  nz = 1
     >>> par = ['wx']*nx + ['x']*nx + ['wy']*ny + ['y']*ny + ['wz']*nz + ['z']*nz
     >>> weights, positions = split_param(par, (nx,ny,nz))
     >>> weights
     ['wx','wx','wx','wy','wy','wz']
     >>> positions
     ['x','x','x','y','y','z']
```

### Comparing `mystic-0.4.0/mystic/math/poly.py` & `mystic-0.4.1/mystic/math/poly.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,32 +1,48 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 tools for polynomial functions
 """
-from numpy import asarray
-from numpy import poly1d as npoly1d
+#__all__ = ['polyeval', 'poly1d']
 
 def polyeval(coeffs, x):
-    """takes list of coefficients & evaluation points, returns f(x)
-thus, [a3, a2, a1, a0] yields  a3 x^3 + a2 x^2 + a1 x^1 + a0"""
+    """evaluate the polynomial defined by coeffs at evaluation points, x
+
+thus, ``[a3, a2, a1, a0]`` yields ``a3 x^3 + a2 x^2 + a1 x^1 + a0``
+
+Args:
+    coeffs (list[float]): polynomial coefficients
+    x (array[float]): array of points to evaluate the polynomial
+
+Returns:
+    array of evaluations of the polynomial
+
+Examples:
+    >>> x = numpy.array([1, 2, 3, 4, 5])
+    >>> polyeval([1, 0, 0], x)
+    array([ 1,  4,  9, 16, 25])
+    >>> polyeval([0, 1, -1], x)
+    array([0, 1, 2, 3, 4])
+    """
     # The effect is this:
     #    return reduce(lambda x1, x2: x1 * x + x2, coeffs, 0)
     # However, the for loop used below is faster by about 50%.
+#   from numpy import asarray
 #   x = asarray(x) #FIXME: converting to numpy.array slows by 10x
     val = 0*x
     for c in coeffs:
        val = c + val*x #FIXME: requires x to be a numpy.array
     return val
 
 def poly1d(coeff):
-    """generates a 1-D polynomial instance from a list of coefficients
-using numpy.poly1d(coeffs)"""
+    """generate a 1-D polynomial instance from a list of coefficients"""
+    from numpy import poly1d as npoly1d
     return npoly1d(coeff)
 
 
 # End of file
```

### Comparing `mystic-0.4.0/mystic/math/samples.py` & `mystic-0.4.1/mystic/math/samples.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 tools related to sampling
 """
 # These functions are consolidated and adapted from samples.py and cut.py in 
 # branches/UQ/math/ for general use.
```

### Comparing `mystic-0.4.0/mystic/math/stats.py` & `mystic-0.4.1/mystic/math/stats.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 shortcut (?) math tools related to statistics;
 also, math tools related to gaussian distributions
 """
 import math
```

### Comparing `mystic-0.4.0/mystic/metropolis.py` & `mystic-0.4.1/mystic/metropolis.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Implements a simple version of the Metropolis-Hastings algorithm
 """
```

### Comparing `mystic-0.4.0/mystic/models/__init__.py` & `mystic-0.4.1/mystic/models/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 models: sample models and functions prepared for use in mystic
 
 
 Functions
```

### Comparing `mystic-0.4.0/mystic/models/__main__.py` & `mystic-0.4.1/mystic/models/__main__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Jean-Christophe Fillion-Robin (jchris.fillionr @kitware.com)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic import model_plotter
 
 __doc__ = model_plotter.__doc__
```

### Comparing `mystic-0.4.0/mystic/models/_model_helper.py` & `mystic-0.4.1/mystic/models/_model_helper.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 chebyshev2coeffs = [2., 0., -1.]
 chebyshev4coeffs = [8., 0., -8., 0., 1.]
 chebyshev6coeffs = [32., 0., -48., 0., 18., 0., -1.]
 chebyshev8coeffs = [128., 0., -256., 0., 160., 0., -32., 0., 1.]
```

### Comparing `mystic-0.4.0/mystic/models/abstract_model.py` & `mystic-0.4.1/mystic/models/abstract_model.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,21 +1,23 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Base classes for mystic's provided models::
     AbstractFunction   -- evaluates f(x) for given evaluation points x
     AbstractModel      -- generates f(x,p) for given coefficients p
 
 """
+__all__ = ['AbstractFunction', 'AbstractModel']
+
 from numpy import sum as numpysum
 from mystic.forward_model import CostFactory as CF
 
 class AbstractFunction(object):
     """
 Base class for mystic functions
```

### Comparing `mystic-0.4.0/mystic/models/br8.py` & `mystic-0.4.1/mystic/models/br8.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,22 +1,24 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Bevington & Robinson's model of dual exponential decay
 
 References:
     1. "Data Reduction and Error Analysis for the Physical Sciences",
        Bevington & Robinson, Second Edition, McGraw-Hill, New York (1992).
 """
+__all__ = ['BevingtonDecay', 'decay', 'data', 'cost']
+
 from .abstract_model import AbstractModel
 
 from numpy import array, asarray
 from numpy import sum as numpysum
 from numpy import exp, sqrt
 from mystic.forward_model import CostFactory as CF
```

### Comparing `mystic-0.4.0/mystic/models/dejong.py` & `mystic-0.4.1/mystic/models/dejong.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 __doc__ = _doc = """
 This is part of Storn's "Differential Evolution" test suite, as defined
 in [2], with 'De Jong' function definitions drawn from [3].
 
 References:
@@ -17,14 +17,17 @@
     2. Storn, R. and Price, K. "Differential Evolution - A Simple and
        Efficient Heuristic for Global Optimization over Continuous Spaces"
        TR-95-012, ICSI, 1995. http://www.icsi.berkeley.edu/~storn/TR-95-012.pdf
     3. Ingber, L. and Rosen, B. "Genetic Algorithms and Very Fast
        Simulated Reannealing: A Comparison" J. of Mathematical and Computer
        Modeling 16(11), 87-100, 1992.
 """
+__all__ = ['Sphere', 'Rosenbrock', 'Step', 'Quartic', 'Shekel', 'sphere',
+           'rosen', 'step', 'quartic', 'shekel', 'rosen0der', 'rosen1dir']
+
 from .abstract_model import AbstractFunction
 
 from numpy import sum as numpysum
 from numpy import asarray, transpose, inf, ones_like
 from numpy import zeros_like, diag, zeros, atleast_1d
 from math import floor
 import random
```

### Comparing `mystic-0.4.0/mystic/models/functions.py` & `mystic-0.4.1/mystic/models/functions.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 convert bound instances into functions
 """
 # from dejong import sphere, rosen, step, quartic, shekel
 def sphere(x):
```

### Comparing `mystic-0.4.0/mystic/models/lorentzian.py` & `mystic-0.4.1/mystic/models/lorentzian.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,21 +1,23 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Lorentzian peak model
 
 References:
     None
 """
+__all__ = ['Lorentzian', 'lorentzian', 'gendata', 'histogram']
+
 from .abstract_model import AbstractModel
 
 from numpy import sum as numpysum
 from numpy import array, pi, asarray, arange
 import random
 
 class Lorentzian(AbstractModel):
@@ -45,15 +47,15 @@
 
     pass
  
 
 # prepared instances
 lorentzian = Lorentzian()
 
-def gendata(params,xmin,xmax,npts=4000):
+def gendata(params, xmin, xmax, npts=4000):
     """Generate a lorentzian dataset of npts between [min,max] from given params"""
     F = lorentzian.ForwardFactory
     def gensample(F, xmin, xmax):
         from numpy import arange
         import random
         a = arange(xmin, xmax, (xmax-xmin)/200.)
         ymin = 0
@@ -65,15 +67,15 @@
             if t2 < t3:
                 return t1
     fwd = F(params)
     return array([gensample(fwd, xmin,xmax) for i in range(npts)])
 
 # probably shouldn't be in here...
 from numpy import histogram as numpyhisto
-def histogram(data,binwidth, xmin,xmax):
+def histogram(data, binwidth, xmin, xmax):
     """generate bin-centered histogram of provided data
 return bins of given binwidth (and histogram) generated between [xmin,xmax]"""
     bins = arange(xmin,xmax, binwidth)
     binsc = bins + (0.5 * binwidth)
     try: #FIXME: use updated numpy.histogram
         histo = numpyhisto(data, bins, new=False)[0]
     except:
```

### Comparing `mystic-0.4.0/mystic/models/mogi.py` & `mystic-0.4.1/mystic/models/mogi.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,24 +1,26 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Mogi's model of surface displacements from a point spherical source in an
 elastic half space
 
 References:
     1. Mogi, K. "Relations between the eruptions of various
        volcanoes and the deformations of the ground surfaces around them", 
        Bull. Earthquake. Res. Inst., 36, 99-134, 1958.
 """
+__all__ = ['Mogi', 'mogi']
+
 from .abstract_model import AbstractModel
 
 from numpy import sum as numpysum
 from numpy import array, pi
 
 class Mogi(AbstractModel):
     """
```

### Comparing `mystic-0.4.0/mystic/models/nag.py` & `mystic-0.4.1/mystic/models/nag.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,23 +1,25 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 __doc__ = _doc = """
 This is drawn from examples in the NAG Library, with the 'peaks' function
 definition found in [1].
 
 References:
     1. Numerical Algorithms Group, "NAG Library", Oxford UK, Mark 24,
        2013. http://www.nag.co.uk/numeric/CL/nagdoc_cl24/pdf/E05/e05jbc.pdf
 """
+__all__ = ['Peaks', 'peaks']
+
 from .abstract_model import AbstractFunction
 
 from math import exp
 
 class Peaks(AbstractFunction):
     __doc__ = \
     """a peaks function generator
```

### Comparing `mystic-0.4.0/mystic/models/pohlheim.py` & `mystic-0.4.1/mystic/models/pohlheim.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 __doc__ = _doc = """
 This is part of Pohlheim's "GEATbx" test suite in [1], with function
 definitions drawn from [1], [2], [3], [4], [5], [6], and [7].
 
 References:
@@ -26,14 +26,19 @@
        Thesis, U. Louisville, Louisville KY, 1990.
     7. Goldstein, A.A. and Price, I.F. "On Descent from Local Minima",
        Math. Comput., (25) 115, 1971.
 """
 #   8. Dixon, L.C.W. and Szego, G.P. "The Optimization Problem: An
 #      Introduction", in "Toward Global Optimization II", North Holland,
 #      New York, 1978.
+__all__ = ['Schwefel', 'HyperEllipsoid', 'Rastrigin', 'DifferentPowers',
+           'Ackley', 'Michalewicz', 'Michalewicz', 'Branins', 'Easom',
+           'GoldsteinPrice', 'schwefel', 'ellipsoid', 'rastrigin', 'powers',
+           'ackley', 'michal', 'branins', 'easom', 'goldstein']
+
 from .abstract_model import AbstractFunction
 
 from math import sin, cos, sqrt, pi, exp
 
 class Schwefel(AbstractFunction):
     __doc__ = \
     """a Schwefel's function generator
```

### Comparing `mystic-0.4.0/mystic/models/poly.py` & `mystic-0.4.1/mystic/models/poly.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 1d model representation for polynomials
 
 References:
     1. Storn, R. and Price, K. "Differential Evolution - A Simple and
@@ -15,14 +15,21 @@
        Journal of Global Optimization 11: 341-359, 1997.
     2. Storn, R. and Price, K. "Differential Evolution - A Simple and
        Efficient Heuristic for Global Optimization over Continuous Spaces"
        TR-95-012, ICSI, 1995. http://www.icsi.berkeley.edu/~storn/TR-95-012.pdf
     3. Storn, R. "Constrained Optimization" Dr. Dobb's Journal, May,
        119-123, 1995.
 """
+__all__ = ['Polynomial', 'Chebyshev', 'poly', 'chebyshev2', 'chebyshev4',
+           'chebyshev6', 'chrbyshev8', 'chebyshev16', 'chebyshev2cost',
+           'chebyshev4cost', 'chebyshev6cost', 'chrbyshev8cost',
+           'chebyshev16cost', 'chebyshev2coeffs', 'chebyshev4coeffs',
+           'chebyshev6coeffs', 'chrbyshev8coeffs', 'chebyshev16coeffs',
+           'chebyshevcostfactory']
+
 from .abstract_model import AbstractModel
 
 from numpy import sum as numpysum
 from numpy import asarray
 from mystic.math import polyeval, poly1d
```

### Comparing `mystic-0.4.0/mystic/models/schittkowski.py` & `mystic-0.4.1/mystic/models/schittkowski.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,27 +1,29 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 __doc__ = _doc = """
 This is part of Hock and Schittkowski's test suite in [1], with function
 definitions drawn from [1] and [2].
 
 References:
     1. Hock, W. and Schittkowski, K. "Test Examples for Nonlinear Programming
        Codes", Lecture Notes in Economics and Mathematical Systems, Vol. 187,
        Springer, 1981. http://www.ai7.uni-bayreuth.de/test_problem_coll.pdf
     2. Paviani, D.A. "A new method for the solution of the general
        nonlinear programming problem", Ph.D. dissertation, The University
        of Texas, Austin, TX, 1969.
 """
+__all__ = ['Paviani', 'paviani']
+
 from .abstract_model import AbstractFunction
 
 from math import sin, cos, sqrt, pi, exp, log
 from numpy import inf
 
 class Paviani(AbstractFunction):
     __doc__ = \
```

### Comparing `mystic-0.4.0/mystic/models/storn.py` & `mystic-0.4.1/mystic/models/storn.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 __doc__ = _doc = """
 This is part of Storn's "Differential Evolution" test suite, as defined
 in [2], with 'Corana' function definitions drawn from [3,4], 'Griewangk'
 function definitions drawn from [5], and 'Zimmermann' function definitions
 drawn from [6].
@@ -25,14 +25,17 @@
        "Minimizing Multimodal Functions of Continuous Variables with the
        'Simulated Annealing Algorithm'" ACM Transactions on Mathematical
        Software, March, 272-280, 1987.
     5. Griewangk, A.O. "Generalized Descent for Global Optimization"
        Journal of Optimization Theory and Applications 34: 11-39, 1981.
     6. Zimmermann, W. "Operations Research" Oldenbourg Munchen, Wien, 1990.
 """
+__all__ = ['Corana', 'Griewangk', 'Zimmermann', 'corana', 'griewangk',
+           'zimmermann']
+
 from .abstract_model import AbstractFunction
 
 from numpy import asarray
 from math import pow, cos, sqrt
 from numpy import sign, floor
 
 class Corana(AbstractFunction):
```

### Comparing `mystic-0.4.0/mystic/models/venkataraman.py` & `mystic-0.4.1/mystic/models/venkataraman.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,23 +1,25 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 __doc__ = _doc = """
 This is drawn from examples in Applied Optimization with MATLAB programming,
 with the function definition found in [1].
 
 References:
     1. Venkataraman, P. "Applied Optimization with MATLAB Programming",
        John Wiley and Sons, Hoboken NJ, 2nd Edition, 2009.
 """
+__all__ = ['Sinc', 'venkat91']
+
 from .abstract_model import AbstractFunction
 
 from math import sin
 
 class Sinc(AbstractFunction):
     __doc__ = \
     """a Venkataraman's sinc function generator
```

### Comparing `mystic-0.4.0/mystic/models/wavy.py` & `mystic-0.4.1/mystic/models/wavy.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,22 +1,24 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 __doc__ = _doc = """
 Multi-minima example functions with vector outputs, which require
 a 'reducing' function to provide scalar return values.
 
 References:
     None
 """
+__all__ = ['Wavy1', 'Wavy2', 'wavy1', 'wavy2']
+
 from .abstract_model import AbstractFunction
 
 from numpy import absolute as abs
 from numpy import asarray
 from numpy import sin, pi
 
 class Wavy1(AbstractFunction): #XXX: not a standard test function...?
```

### Comparing `mystic-0.4.0/mystic/models/wolfram.py` & `mystic-0.4.1/mystic/models/wolfram.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,26 +1,28 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 __doc__ = _doc = """
 This is drawn from Mathematica's example suites, with the 'fOsc3D'
 function definition found in [1], and the 'XXX' function found in [2].
 
 References:
     1. Trott, M. "The Mathematica GuideBook for Numerics", Springer-Verlag,
        New York, 2006.
     2. Champion, B. and Strzebonski, A. "Wolfram Mathematica Tutorial
        Collection on Constrained Optimization", Wolfram Research, USA, 2008.
        http://reference.wolfram.com/language/guide/Optimization.html
 """
+__all__ = ['fOsc3D', 'NMinimize51', 'fosc3d', 'nmin51']
+
 from .abstract_model import AbstractFunction
 
 from math import sin, exp
 
 class fOsc3D(AbstractFunction):
     __doc__ = \
     """a fOsc3D function generator
```

### Comparing `mystic-0.4.0/mystic/monitors.py` & `mystic-0.4.1/mystic/monitors.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 # Null was adapted (and bugfixed) from the python cookbook
 """
 monitors: callable class instances that record data
 
@@ -94,16 +94,16 @@
     def __setattr__(self, name, value): return self
     def __delattr__(self, name): return self
     def __len__(self): return 0
     def __getnewargs__(self): return ()
     def __getitem__(self, y): return self
     def __setitem__(self, i, y): return
     def min(self): return self
+    def info(self, message): return
 # comply with monitor interface (are these the best responses?)
-Null.info = Null()
 Null.k = None
 Null.x = Null._x = ()
 Null.y = Null._y = ()
 Null._id = ()
 Null._npts = None
 Null.label = None
 
@@ -384,37 +384,37 @@
         return
     def __call__(self, x, y, id=None, best=0, k=False):
         super(VerboseMonitor,self).__call__(x, y, id, k=k)
         if self._yinterval is not numpy.inf and \
            int((self._step-1) % self._yinterval) == 0:
             if not list_or_tuple_or_ndarray(y):
                 who = ''
-                y = " %f" % self._ik(self._y[-1], k)
+                y = " %s" % self._ik(self._y[-1], k)
             elif self._all:
                 who = ''
                 y = " %s" % self._ik(self._y[-1], k)
             else:
                 who = ' best'
-                y = " %f" % self._ik(self._y[-1][best], k)
-            msg = "Generation %d has%s %s:%s" % (self._step-1,who,self.label,y)
-            if id is not None: msg = "[id: %d] " % (id) + msg
+                y = " %s" % self._ik(self._y[-1][best], k)
+            msg = "Generation %s has%s %s:%s" % (self._step-1,who,self.label,y)
+            if id is not None: msg = "[id: %s] " % (id) + msg
             print(msg)
         if self._xinterval is not numpy.inf and \
            int((self._step-1) % self._xinterval) == 0:
             if not list_or_tuple_or_ndarray(x):
                 who = ''
-                x = " %f" % self._x[-1]
+                x = " %s" % self._x[-1]
             elif self._all:
                 who = ''
                 x = "\n %s" % self._x[-1]
             else:
                 who = ' best'
                 x = "\n %s" % self._x[-1][best]
-            msg = "Generation %d has%s fit parameters:%s" % (self._step-1,who,x)
-            if id is not None: msg = "[id: %d] " % (id) + msg
+            msg = "Generation %s has%s fit parameters:%s" % (self._step-1,who,x)
+            if id is not None: msg = "[id: %s] " % (id) + msg
             print(msg)
         return
     pass
 
 class LoggingMonitor(Monitor):
     """A basic Monitor that writes to a file at specified intervals.
 
@@ -448,31 +448,31 @@
         return
     def __call__(self, x, y, id=None, best=0, k=False):
         self._file = open(self._filename,'a')
         super(LoggingMonitor,self).__call__(x, y, id, k=k)
         if self._yinterval is not numpy.inf and \
            int((self._step-1) % self._yinterval) == 0:
             if not list_or_tuple_or_ndarray(y):
-                y = "%f" % self._ik(self._y[-1], k)
+                y = "%s" % self._ik(self._y[-1], k)
             elif self._all:
                 y = "%s" % self._ik(self._y[-1], k)
             else:
-                y = "%f" % self._ik(self._y[-1][best], k)
+                y = "%s" % self._ik(self._y[-1][best], k)
             if not list_or_tuple_or_ndarray(x):
-                x = "[%f]" % self._x[-1]
+                x = "[%s]" % self._x[-1]
             elif self._all:
                 xa = self._x[-1]
                 if not list_or_tuple_or_ndarray(xa):
-                  x = "[%f]" % xa
+                  x = "[%s]" % xa
                 else:
                   x = "%s" % xa
             else:
                 xb = self._x[-1][best]
                 if not list_or_tuple_or_ndarray(xb):
-                  x = "[%f]" % xb
+                  x = "[%s]" % xb
                 else:
                   x = "%s" % xb
             step = [self._step-1]
             if id is not None: step.append(id)
             self._file.write("  %s     %s   %s\n" % (tuple(step), y, x))
         self._file.close()
         return
@@ -510,37 +510,37 @@
         return
     def __call__(self, x, y, id=None, best=0, k=False):
         super(VerboseLoggingMonitor,self).__call__(x, y, id, best, k=k)
         if self._vyinterval is not numpy.inf and \
            int((self._step-1) % self._vyinterval) == 0:
             if not list_or_tuple_or_ndarray(y):
                 who = ''
-                y = " %f" % self._ik(self._y[-1], k)
+                y = " %s" % self._ik(self._y[-1], k)
             elif self._all:
                 who = ''
                 y = " %s" % self._ik(self._y[-1], k)
             else:
                 who = ' best'
-                y = " %f" % self._ik(self._y[-1][best], k)
-            msg = "Generation %d has%s %s:%s" % (self._step-1,who,self.label,y)
-            if id is not None: msg = "[id: %d] " % (id) + msg
+                y = " %s" % self._ik(self._y[-1][best], k)
+            msg = "Generation %s has%s %s:%s" % (self._step-1,who,self.label,y)
+            if id is not None: msg = "[id: %s] " % (id) + msg
             print(msg)
         if self._vxinterval is not numpy.inf and \
            int((self._step-1) % self._vxinterval) == 0:
             if not list_or_tuple_or_ndarray(x):
                 who = ''
-                x = " %f" % self._x[-1]
+                x = " %s" % self._x[-1]
             elif self._all:
                 who = ''
                 x = "\n %s" % self._x[-1]
             else:
                 who = ' best'
                 x = "\n %s" % self._x[-1][best]
-            msg = "Generation %d has%s fit parameters:%s" % (self._step-1,who,x)
-            if id is not None: msg = "[id: %d] " % (id) + msg
+            msg = "Generation %s has%s fit parameters:%s" % (self._step-1,who,x)
+            if id is not None: msg = "[id: %s] " % (id) + msg
             print(msg)
         return
     def __reduce__(self):
         interval = self._yinterval
         yint = self._vyinterval
         xint = self._vxinterval
         filename = self._filename
```

### Comparing `mystic-0.4.0/mystic/penalty.py` & `mystic-0.4.1/mystic/penalty.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 penalty methods: methods used to convert a function into a penalty function
 
 Suppose a given condition ``f(x)`` is satisfied when ``f(x) == 0.0``
 for equality constraints, and ``f(x) <= 0.0`` for inequality constraints.
```

### Comparing `mystic-0.4.0/mystic/pools.py` & `mystic-0.4.1/mystic/pools.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 This module contains map and pipe interfaces to standard (i.e. serial) python.
 
 Pipe methods provided:
     pipe        - blocking communication pipe             [returns: value]
@@ -68,20 +68,20 @@
     """
     # interface (no __init__)
     _exiting = False
 
     def map(self, f, *args, **kwds):
        #AbstractWorkerPool._AbstractWorkerPool__map(self, f, *args, **kwds)
         if self._exiting: self._is_alive()
-        return _map(f, *args)#, **kwds)
+        return _map(f, *args)#, **kwds) # chunksize
     map.__doc__ = AbstractWorkerPool.map.__doc__
     def imap(self, f, *args, **kwds):
        #AbstractWorkerPool._AbstractWorkerPool__imap(self, f, *args, **kwds)
         if self._exiting: self._is_alive()
-        return _imap(f, *args)#, **kwds)
+        return _imap(f, *args)#, **kwds) # chunksize
     imap.__doc__ = AbstractWorkerPool.imap.__doc__
     ########################################################################
     # PIPES
     def pipe(self, f, *args, **kwds):
        #AbstractWorkerPool._AbstractWorkerPool__pipe(self, f, *args, **kwds)
         if self._exiting: self._is_alive()
         return _apply(f, args, kwds)
```

### Comparing `mystic-0.4.0/mystic/python_map.py` & `mystic-0.4.1/mystic/python_map.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Defaults for mapper and launcher. These should be available as a minimal
 (dependency-free) pure-python install from ``pathos``::
 
     serial_launcher -- syntax for standard python execution
@@ -46,27 +46,17 @@
     mydict.update(kdict)
     str = """ %(python)s %(program)s %(progargs)s""" % mydict
     return str
 
 def python_map(func, *arglist, **kwds):
     """maps function *func* across arguments *arglist*.
 
-Provides the standard python map function, however also accepts *kwds* in
-order to conform with the (deprecated) ``pyina.ez_map`` interface.
-
-Notes:
-    The following *kwds* used in ``ez_map`` are accepted, but disabled:
-        * nodes -- the number of parallel nodes
-        * launcher -- the launcher object
-        * scheduler -- the scheduler object
-        * mapper -- the mapper object
-        * timelimit -- string representation of maximum run time (e.g. '00:02')
-        * queue -- string name of selected queue (e.g. 'normal')
+Provides the standard python map interface as a function; however returns
+returns a list instead of a map iterator and accepts (and ignores) kwds.
 """
-   #print("ignoring: %s" % kwds)  #XXX: should allow use of **kwds
     result = list(map(func, *arglist)) #     see pathos.pyina.ez_map
     return result
 
 def worker_pool():
     """use the 'worker pool' strategy; hence one job is allocated to each
 worker, and the next new work item is provided when a node completes its work
 """
```

### Comparing `mystic-0.4.0/mystic/samplers.py` & `mystic-0.4.1/mystic/samplers.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2019-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2019-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 samplers: optimizer-guided directed sampling
 """
 __all__  = ['LatticeSampler','BuckshotSampler','SparsitySampler']
```

### Comparing `mystic-0.4.0/mystic/scemtools.py` & `mystic-0.4.1/mystic/scemtools.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Implements the "Shuffled Complex Evolution Metropolis" Algoritm
 of Vrugt et al. [1]
```

### Comparing `mystic-0.4.0/mystic/scipy_optimize.py` & `mystic-0.4.1/mystic/scipy_optimize.py`

 * *Files 3% similar despite different names*

```diff
@@ -14,15 +14,15 @@
 #
 # updated solvers to scipy version 1.1.0
 # by Mike McKerns
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 """
 Solvers
 =======
 
@@ -120,16 +120,17 @@
         xtol, ftol = 1e-4, 1e-4
         from mystic.termination import CandidateRelativeTolerance as CRT
         self._termination = CRT(xtol,ftol)
 
     def _setSimplexWithinRangeBoundary(self, radius=None):
         """ensure that initial simplex is set within bounds
 
-Input::
-    - radius: size of the initial simplex [default=0.05]"""
+Args:
+    radius (float, default=0.05): size of the initial simplex
+        """
         x0 = self.population[0]
         #code modified from park-1.2/park/simplex.py (version 1257)
         if self._useStrictRange:
             x0 = self._clipGuessWithinRangeBoundary(x0)
 
         if radius is None: radius = 0.05 # nonzdelt=0.05 from scipy-0.9
         val = x0*(1+radius)
@@ -163,31 +164,39 @@
      #  xtol = tol
         self.population[0] = x0
         return val
 
     def _SetEvaluationLimits(self, iterscale=200, evalscale=200):
         """set the evaluation limits
 
-input::
-    - iterscale and evalscale are integers used to set the maximum iteration
+Args:
+    iterscale (int, default=200): scale factor for iteration upper limit
+    evalscale (int, default=200): scale factor for evaluation upper limit
+
+Notes:
+    - ``iterscale`` and ``evalscale`` are used to set the maximum iteration
       and evaluation limits, respectively. The new limit is defined as
-      limit = (nDim * nPop * scale) + count, where count is the number
-      of existing iterations or evaluations, respectively. The default for
-      iterscale is 200, and the default for evalscale is also 200.
+      ``limit = (nDim * nPop * scale) + count``, where ``count`` is the number
+      of existing iterations or evaluations, respectively.
         """
         super(NelderMeadSimplexSolver, self)._SetEvaluationLimits(iterscale,evalscale)
         return
 
     def _decorate_objective(self, cost, ExtraArgs=None):
         """decorate the cost function with bounds, penalties, monitors, etc
 
-input::
-    - cost is the objective function, of the form y = cost(x, *ExtraArgs),
-      where x is a candidate solution, and ExtraArgs is the tuple of positional
-      arguments required to evaluate the objective."""
+Args:
+    cost (func): objective, of form ``y = cost(x, *ExtraArgs)``, where ``x``
+      is a candidate solution vector
+    ExtraArgs (tuple, default=None): tuple of positional arguments required to
+      evaluate the objective
+
+Returns:
+    decorated objective function
+        """
         #print("@%r %r %r" % (cost, ExtraArgs, max))
         evalmon = self._evalmon
         raw = cost
         if ExtraArgs is None: ExtraArgs = ()
         self._fcalls, cost = wrap_function(cost, ExtraArgs, evalmon)
         if self._useStrictRange:
             if self.generations:
@@ -210,24 +219,26 @@
         self._cost = (cost, raw, ExtraArgs)
         self._live = True
         return cost
 
     def _Step(self, cost=None, ExtraArgs=None, **kwds):
         """perform a single optimization iteration
 
-input::
-    - cost is the objective function, of the form y = cost(x, *ExtraArgs),
-      where x is a candidate solution, and ExtraArgs is the tuple of positional
-      arguments required to evaluate the objective.
+Args:
+    cost (func, default=None): objective, of form ``y = cost(x, *ExtraArgs)``,
+      where ``x`` is a candidate solution vector
+    ExtraArgs (tuple, default=None): tuple of positional arguments required to
+      evaluate the objective
 
-note::
-    ExtraArgs needs to be a *tuple* of extra arguments.
+Returns:
+    None
 
-    This method accepts additional args that are specific for the current
-    solver, as detailed in the `_process_inputs` method.
+Notes:
+    - This method accepts additional ``kwds`` that are specific for the current
+      solver, as detailed in the ``_process_inputs`` method.
         """
         # process and activate input settings
         settings = self._process_inputs(kwds)
         #(hardwired: due to python exec'ing to locals())
         callback = settings['callback'] if 'callback' in settings else None
         disp = settings['disp'] if 'disp' in settings else False
         radius = settings['radius'] if 'radius' in settings else self.radius
@@ -356,32 +367,32 @@
         return #XXX: call Terminated ?
 
     def _process_inputs(self, kwds):
         """process and activate input settings
 
 Args:
     callback (func, default=None): function to call after each iteration. The
-        interface is ``callback(xk)``, with xk the current parameter vector.
+        interface is ``callback(xk)``, with ``xk`` the current parameter vector.
     disp (bool, default=False): if True, print convergence messages.
-
-Additional Args:
-    EvaluationMonitor: a monitor instance to capture each evaluation of cost.
-    StepMonitor: a monitor instance to capture each iteration's best results.
-    penalty: a function of the form: y' = penalty(xk), with y = cost(xk) + y',
-        where xk is the current parameter vector.
-    constraints: a function of the form: xk' = constraints(xk), where xk is
-        the current parameter vector.
+    EvaluationMonitor (monitor, default=None): a monitor instance to capture
+        each evaluation of cost.
+    StepMonitor (monitor, default=None): a monitor instance to capture each
+        iteration's best results.
+    penalty (penalty, default=None): function of the form: ``y' = penalty(xk)``,
+        with ``y = cost(xk) + y'`` and ``xk`` is the current parameter vector.
+    constraints (constraint, default=None): function of the form:
+        ``xk' = constraints(xk)``, where ``xk`` is the current parameter vector.
     radius (float, default=0.05): percentage change for initial simplex values.
     adaptive (bool, default=False): adapt algorithm parameters to the
         dimensionality of the initial parameter vector ``x``.
 
-Note:
-   The additional args are 'sticky', in that once they are given, they remain
-   set until they are explicitly changed. Conversely, the args are not sticky,
-   and are thus set for a one-time use.
+Notes:
+    - ``callback`` and ``disp`` are 'sticky', in that once they are given, they
+      remain set until they are explicitly changed. Conversely, the other inputs
+      are not sticky, and are thus set for a one-time use.
         """
         #allow for inputs that don't conform to AbstractSolver interface
         #NOTE: not sticky: callback, disp
         #NOTE: sticky: EvaluationMonitor, StepMonitor, penalty, constraints
         #NOTE: sticky: radius, adaptive
         settings = super(NelderMeadSimplexSolver, self)._process_inputs(kwds)
         settings.update({
@@ -468,15 +479,15 @@
     ``(xopt, {fopt, iter, funcalls, warnflag}, {allvecs})``
 
 Notes:
     - xopt (*ndarray*): the minimizer of the cost function
     - fopt (*float*): value of cost function at minimum: ``fopt = cost(xopt)``
     - iter (*int*): number of iterations
     - funcalls (*int*): number of function calls
-    - warnflag (*int*): warning flag:
+    - warnflag (*int*): warning flag
         - ``1 : Maximum number of function evaluations``
         - ``2 : Maximum number of iterations``
     - allvecs (*list*): a list of solutions at each iteration
     """
     handler = kwds['handler'] if 'handler' in kwds else False
 
     from mystic.monitors import Monitor
@@ -577,37 +588,42 @@
     def __generations(self):
         """get the number of iterations"""
         return max(0,len(self.energy_history)-1)  #XXX: slower for k=-1 ?
 
     def _SetEvaluationLimits(self, iterscale=1000, evalscale=1000):
         """set the evaluation limits
 
-input::
-    - iterscale and evalscale are integers used to set the maximum iteration
+Args:
+    iterscale (int, default=1000): scale factor for iteration upper limit
+    evalscale (int, default=1000): scale factor for evaluation upper limit
+
+Notes:
+    - ``iterscale`` and ``evalscale`` are used to set the maximum iteration
       and evaluation limits, respectively. The new limit is defined as
-      limit = (nDim * nPop * scale) + count, where count is the number
-      of existing iterations or evaluations, respectively. The default for
-      iterscale is 1000, and the default for evalscale is also 1000.
+      ``limit = (nDim * nPop * scale) + count``, where ``count`` is the number
+      of existing iterations or evaluations, respectively.
         """
         super(PowellDirectionalSolver, self)._SetEvaluationLimits(iterscale,evalscale)
         return
 
     def _Step(self, cost=None, ExtraArgs=None, **kwds):
         """perform a single optimization iteration
 
-input::
-    - cost is the objective function, of the form y = cost(x, *ExtraArgs),
-      where x is a candidate solution, and ExtraArgs is the tuple of positional
-      arguments required to evaluate the objective.
+Args:
+    cost (func, default=None): objective, of form ``y = cost(x, *ExtraArgs)``,
+      where ``x`` is a candidate solution vector
+    ExtraArgs (tuple, default=None): tuple of positional arguments required to
+      evaluate the objective
 
-note::
-    ExtraArgs needs to be a *tuple* of extra arguments.
+Returns:
+    None
 
-    This method accepts additional args that are specific for the current
-    solver, as detailed in the `_process_inputs` method.
+Notes:
+    - This method accepts additional ``kwds`` that are specific for the current
+      solver, as detailed in the ``_process_inputs`` method.
         """
         # process and activate input settings
         settings = self._process_inputs(kwds)
         #(hardwired: due to python exec'ing to locals())
         callback = settings['callback'] if 'callback' in settings else None
         disp = settings['disp'] if 'disp' in settings else False
         xtol = settings['xtol'] if 'xtol' in settings else self.xtol
@@ -737,32 +753,32 @@
         return
 
     def _process_inputs(self, kwds):
         """process and activate input settings
 
 Args:
     callback (func, default=None): function to call after each iteration. The
-        interface is ``callback(xk)``, with xk the current parameter vector.
+        interface is ``callback(xk)``, with ``xk`` the current parameter vector.
     disp (bool, default=False): if True, print convergence messages.
-
-Additional Args:
-    EvaluationMonitor: a monitor instance to capture each evaluation of cost.
-    StepMonitor: a monitor instance to capture each iteration's best results.
-    penalty: a function of the form: y' = penalty(xk), with y = cost(xk) + y',
-        where xk is the current parameter vector.
-    constraints: a function of the form: xk' = constraints(xk), where xk is
-        the current parameter vector.
+    EvaluationMonitor (monitor, default=None): a monitor instance to capture
+        each evaluation of cost.
+    StepMonitor (monitor, default=None): a monitor instance to capture each
+        iteration's best results.
+    penalty (penalty, default=None): function of the form: ``y' = penalty(xk)``,
+        with ``y = cost(xk) + y'`` and ``xk`` is the current parameter vector.
+    constraints (constraint, default=None): function of the form:
+        ``xk' = constraints(xk)``, where ``xk`` is the current parameter vector.
     direc (tuple, default=None): the initial direction set.
     xtol (float, default=1e-4): line-search error tolerance.
     imax (float, default=500): line-search maximum iterations.
 
-Note:
-   The additional args are 'sticky', in that once they are given, they remain
-   set until they are explicitly changed. Conversely, the args are not sticky,
-   and are thus set for a one-time use.
+Notes:
+    - ``callback`` and ``disp`` are 'sticky', in that once they are given, they
+      remain set until they are explicitly changed. Conversely, the other inputs
+      are not sticky, and are thus set for a one-time use.
         """
         #allow for inputs that don't conform to AbstractSolver interface
         #NOTE: not sticky: callback, disp
         #NOTE: sticky: EvaluationMonitor, StepMonitor, penalty, constraints
         #NOTE: sticky: imax, xtol, direc
         settings = super(PowellDirectionalSolver, self)._process_inputs(kwds)
         settings.update({\
@@ -861,15 +877,15 @@
     ``(xopt, {fopt, iter, funcalls, warnflag, direc}, {allvecs})``
 
 Notes:
     - xopt (*ndarray*): the minimizer of the cost function
     - fopt (*float*): value of cost function at minimum: ``fopt = cost(xopt)``
     - iter (*int*): number of iterations
     - funcalls (*int*): number of function calls
-    - warnflag (*int*): warning flag:
+    - warnflag (*int*): warning flag
         - ``1 : Maximum number of function evaluations``
         - ``2 : Maximum number of iterations``
     - direc (*tuple*): the current direction set
     - allvecs (*list*): a list of solutions at each iteration
     """
     #FIXME: need to resolve "direc"
     #        - should just pass 'direc', and then hands-off ?  How return it ?
```

### Comparing `mystic-0.4.0/mystic/scripts.py` & `mystic-0.4.1/mystic/scripts.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,26 +1,554 @@
 from collections.abc import Callable as _Callable
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Jean-Christophe Fillion-Robin (jchris.fillionr @kitware.com)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 __doc__ = """
 functional interfaces for mystic's visual analytics scripts
 """
 
-__all__ = ['model_plotter','log_reader','collapse_plotter']
+__all__ = ['model_plotter','log_reader','collapse_plotter','log_converter']
 
 # globals
 __quit = False
 
 
+def _get_ext(file_type):
+    """get extension corresponding to ('support', 'logfile', or archive type)
+
+    file_type: one of ('logfile', 'support', or archive type)
+    """
+    import klepto.archives as kl
+    if file_type == 'support': ext = '.py'
+    elif file_type == 'logfile': ext = '.txt'
+    elif file_type in ('file_archive','dir_archive'): ext = '.db'
+    elif file_type in (kl.file_archive,kl.dir_archive): ext = '.db'
+    elif file_type in ('hdf_archive','hdfdir_archive'): ext = '.h5'
+    elif file_type in (kl.hdf_archive,kl.hdfdir_archive): ext = '.h5'
+    elif file_type in ('sql_archive','sqltable_archive'): ext = '.sql'
+    elif file_type in (kl.sql_archive,kl.sqltable_archive): ext = '.sql'
+    else: ext = '' #XXX: only gets here if is a new archive type
+    return ext
+
+
+def _type_existing(readpath, format=None):
+    """determine type ('logfile', 'support', or archive type) from readpath
+
+    readpath: the string path to the stored trajectories
+    format: type ('logfile', 'support', or klepto.archive type) of readpath
+    """
+    import os
+    if not os.path.exists(readpath):
+        msg = "File not found at: {0}".format(readpath)
+        raise FileNotFoundError(msg)
+    if _issupport(readpath, guess=False):
+        file_in = 'support'
+        if format not in ['support', None]:
+            msg = "{0} format invalid for {1}".format(format, readpath)
+            raise ValueError(msg)
+    elif _islogfile(readpath, guess=False):
+        file_in = 'logfile'
+        if format not in ['logfile', None]:
+            msg = "{0} format invalid for {1}".format(format, readpath)
+            raise ValueError(msg)
+    else:
+        if format is None:
+            file_in = _archive_inferred(readpath) #XXX: guess based on extension
+        else:
+            if format in ['logfile', 'support']:
+                msg = "{0} format invalid for {1}".format(format, readpath)
+                raise ValueError(msg)
+            file_in = _type_inferred(readpath, format)
+    return file_in
+
+
+def _type_inferred(writepath=None, format=None):
+    """guess ('logfile', 'support', or archive type) from format and writepath
+
+    writepath: the string path at which to write the trajectories
+    format: type ('logfile', 'support', or klepto.archive type) for writepath
+    """
+    if writepath is None:
+        if format is None:
+            msg = 'either a format or writepath must be provided'
+            raise ValueError(msg)
+    if format is None:
+        import os
+        guess = not os.path.exists(writepath)
+        if _issupport(writepath, guess=guess):
+            file_out = 'support'
+        elif _islogfile(writepath, guess=guess):
+            file_out = 'logfile'
+        else:
+            file_out = _archive_inferred(writepath) #FIXME: is always guess
+    else:
+        import klepto.archives as kl
+        archives = kl.__all__[:]
+        [archives.remove(i) for i in ('cache','dict_archive','null_archive')]
+        if format in ['support','logfile'] + [kl.__dict__[a] for a in archives]:
+            file_out = format
+        elif format in archives:
+            file_out = kl.__dict__[format]
+        else:
+            msg = 'unknown archive format: {0}'.format(format)
+            raise ValueError(msg)
+    return file_out
+
+
+def _archive_inferred(archivepath):
+    """return archive class object, inferred from the archivepath extension
+
+    archivepath: the string file path to the archive
+    """
+    import os
+    import klepto.archives as ka
+    SQL_EXT = ('.sql','.sqlite','.mdf')
+    ext = os.path.splitext(archivepath)[-1]
+    if ext in SQL_EXT or 'sql' in ext or ext.startswith(('.sq','.mysq','.pg','.post')):
+        return ka.sqltable_archive if _isdir(archivepath) else ka.sql_archive
+    HDF_EXT = ('.hdf','.h5','.hdf5')
+    if ext in HDF_EXT or 'hdf' in ext or ext.startswith('.h'):
+        return ka.hdfdir_archive if _isdir(archivepath) else ka.hdf_archive
+    #DBX_EXT = ('.db','.ar','.klp','.txt')
+    return ka.dir_archive if _isdir(archivepath) else ka.file_archive
+
+
+def _logfile_to_support(logfile, support=None): #.txt -> .py
+    """convert logfile to support file
+
+    logfile: the string path to the 3-column log file to read
+    support: the str path at which to write the support file
+
+    logfile is written with a LoggingMonitor [extension should be .txt]
+    support is read with read_history [extension should be .py]
+
+    if support is None, support name will be derived from logfile
+    """
+    if support is None:
+        import os
+        support = os.path.splitext(os.path.basename(logfile))[0]+'.py'
+    from mystic.monitors import Monitor
+    from mystic.munge import logfile_reader, write_support_file
+    m = Monitor()
+    step, m._x, m._y = logfile_reader(logfile, iter=True)
+    if len(step) and len(step[0]) > 1:
+        m._id = [j for i,j in step]
+    write_support_file(m, support)
+    return
+
+
+def _support_to_logfile(support, logfile=None): #.py -> .txt
+    """convert support file to log file
+
+    support: the str path to the importable support file
+    logfile: the string path to the 3-column log file to write
+
+    logfile is written with a LoggingMonitor [extension should be .txt]
+    support is read with read_history [extension should be .py]
+
+    if logfile is None, logfile name will be derived from support file
+    """
+    if logfile is None:
+        import os
+        logfile = os.path.splitext(os.path.basename(support))[0]+'.txt'
+    import numpy as np
+    from mystic.munge import read_import
+    from mystic.monitors import LoggingMonitor
+    ids,params,cost = read_import(support,'id','params','cost')
+    params = np.array(params).reshape(len(params),-1).T.tolist()
+    if not hasattr(ids, '__len__'): #XXX: ids is not 'processed'
+        ids = [ids]*len(cost)
+    id = max(set(ids)) or 0
+    if not isinstance(id, int): id = 0
+    m = [LoggingMonitor(filename=logfile) for i in range(id + 1)]
+    if ids is None or isinstance(ids, int):
+        [m[ids or 0](p,c,id=ids) for (p,c) in zip(params,cost)]
+    elif id == 0: #NOTE: ids could be non-int
+        [m[0](p,c,id=i) for (p,c,i) in zip(params,cost,ids)]
+    else: #NOTE: m[None] -> m[0]
+        [m[i or 0](p,c,id=i) for (p,c,i) in zip(params,cost,ids)]
+    return
+
+
+def _archive_to_logfile(archive, logfile=None, type=None, iter=False):
+    """convert cached archive to log file
+
+    archive: the str path to the archive to read
+    logfile: the string path to the 3-column log file to write
+    type: the klepto archive type
+    iter: if True, include (iter,ids) tuple in archive keys
+
+    logfile is written with a LoggingMonitor [extension should be .txt]
+    archive is read with mystic.cache.archive.read [extension is .db, .h5, ...]
+
+    if logfile is None, logfile name will be derived from archive
+    if type is None, type will be derived from extension of archive
+    if iter is False, archive doesn't preserve "repeat" entries in log
+    (however, if iter is True, archive format is incompatible with mystic.cache)
+    """ #FIXME: iter=True should be default, and used in mystic.cache
+    import os
+    if not os.path.exists(archive):
+        msg = "File not found at: {0}".format(archive)
+        raise FileNotFoundError(msg)
+    if logfile is None:
+        logfile = os.path.splitext(os.path.basename(archive))[0]+'.txt'
+    import mystic.cache as mc
+    from mystic.monitors import LoggingMonitor
+    source = mc.archive.read(archive, type=type)
+    cost = list(source.values())
+    if iter:
+        step, params = list(zip(*source.keys()))
+        params = list(list(k) for k in params)
+        step = [i[-1] if len(i) == 2 else None for i in step]
+        id = max(set(step)) or 0
+        if not isinstance(id, int): id = 0
+        m = [LoggingMonitor(filename=logfile) for i in range(id + 1)]
+        if id == 0: #NOTE: ids could be non-int
+            [m[i or 0](p,c,id=i) for (p,c,i) in zip(params,cost,step)]
+        else:
+            [m[i or 0](p,c,id=i) for (p,c,i) in zip(params,cost,step)]
+    else:
+        params = list(list(k) for k in source.keys())
+        step = [None]*len(cost)
+        # no ids, so only write with a single monitor
+        m = LoggingMonitor(filename=logfile)
+        [m(p,c) for (p,c) in zip(params,cost)]
+    return
+
+
+def _archive_to_support(archive, support=None, type=None, iter=False):
+    """convert cached archive to support file
+
+    archive: the str path to the archive to read
+    support: the str path at which to write the support file
+    type: the klepto archive type
+    iter: if True, include (iter,ids) tuple in archive keys
+
+    archive is read with mystic.cache.archive.read [extension is .db, .h5, ...]
+    support is read with read_history [extension should be .py]
+
+    if support is None, support name will be derived from archive
+    if type is None, type will be derived from extension of archive
+    if iter is False, archive doesn't preserve "repeat" entries in log
+    (however, if iter is True, archive format is incompatible with mystic.cache)
+    """ #FIXME: iter=True should be default, and used in mystic.cache
+    import os
+    if not os.path.exists(archive):
+        msg = "File not found at: {0}".format(archive)
+        raise FileNotFoundError(msg)
+    if support is None:
+        support = os.path.splitext(os.path.basename(archive))[0]+'.py'
+    import mystic.cache as mc
+    source = mc.archive.read(archive, type=type)
+    from mystic.monitors import Monitor
+    from mystic.munge import write_support_file
+    m = Monitor()
+    if iter:
+        m._id, m._x = list(zip(*source.keys()))
+        m._x = list(list(k) for k in m._x)
+        m._id = [i[-1] if len(i) == 2 else None for i in m._id]
+    else:
+        m._x = list(list(k) for k in source.keys())
+    m._y = list(source.values())
+    write_support_file(m, support)
+    return
+
+
+def _logfile_to_archive(logfile, archive=None, type=None, iter=False):
+    """convert log file to cached archive
+
+    archive: the str path to the archive to read
+    logfile: the string path to the 3-column log file to write
+    type: the klepto archive type
+    iter: if True, include (iter,ids) tuple in archive keys
+
+    archive is read with mystic.cache.archive.read [extension is .db, .h5, ...]
+    logfile is written with a LoggingMonitor [extension should be .txt]
+
+    if archive is None, archive name will be derived from logfile
+    if type is None, type will be derived from extension of archive
+    if iter is False, archive doesn't preserve "repeat" entries in log
+    (however, if iter is True, archive format is incompatible with mystic.cache)
+    """ #FIXME: iter=True should be default, and used in mystic.cache
+    try:
+        type_out = _type_inferred(archive, format=type)
+    except ValueError:
+        type_out = ''
+    if isinstance(type_out, str): # then oops... use the default
+        import klepto.archives as kl
+        type_out = kl.dir_archive if _isdir(archive) else kl.file_archive
+    if archive is None:
+        import os
+        ext = _get_ext(type_out)
+        archive = os.path.splitext(os.path.basename(logfile))[0]+ext
+    from mystic.munge import logfile_reader
+    import mystic.cache as mc
+    a = mc.archive.read(archive, type=type_out)
+    func = mc.cached(archive=a)(lambda param,**kwds: kwds['cost'])
+    if iter:
+        step, params, cost = logfile_reader(logfile, iter=True)
+        [func((i,tuple(p)), cost=c) for (i,p,c) in zip(step,params,cost)]
+    else:
+        params, cost = logfile_reader(logfile, iter=False)
+        [func(p, cost=c) for (p,c) in zip(params,cost)]
+    return
+
+
+def _support_to_archive(support, archive=None, type=None, iter=False):
+    """convert support file to cached archive
+
+    support: the str path to read the support file
+    archive: the str path at which to write the archive
+    type: the klepto archive type
+    iter: if True, include (iter,ids) tuple in archive keys
+
+    support is read with read_history [extension should be .py]
+    archive is read with mystic.cache.archive.read [extension is .db, .h5, ...]
+
+    if archive is None, archive name will be derived from support
+    if type is None, type will be derived from extension of archive
+    if iter is False, archive doesn't preserve "repeat" entries in log
+    (however, if iter is True, archive format is incompatible with mystic.cache)
+    """ #FIXME: iter=True should be default, and used in mystic.cache
+    try:
+        type_out = _type_inferred(archive, format=type)
+    except ValueError:
+        type_out = ''
+    if isinstance(type_out, str): # then oops... use the default
+        import klepto.archives as kl
+        type_out = kl.dir_archive if _isdir(archive) else kl.file_archive
+    if archive is None:
+        import os
+        ext = _get_ext(type_out)
+        archive = os.path.splitext(os.path.basename(support))[0]+ext
+    import numpy as np
+    from mystic.munge import read_import
+    import mystic.cache as mc
+    a = mc.archive.read(archive, type=type_out)
+    func = mc.cached(archive=a)(lambda param,**kwds: kwds['cost'])
+    if iter:
+        step,params,cost = read_import(support,'id''params','cost')
+        params = np.array(params).reshape(len(params),-1).T.tolist()
+        [func((i,tuple(p)), cost=c) for (i,p,c) in zip(step,params,cost)]
+    else:
+        params,cost = read_import(support,'params','cost')
+        params = np.array(params).reshape(len(params),-1).T.tolist()
+        [func(p, cost=c) for (p,c) in zip(params,cost)]
+    return
+
+
+def _islogfile(filepath, guess=True):
+    """return True if the filepath refers to a LoggingMonitor logfile
+
+    is False if filepath doesn't exist, or guess based on filepath extension
+    """
+    if _issupport(filepath, guess): return False
+    if _isdir(filepath, guess=False): return False
+    import os
+    if os.path.exists(filepath):
+        from mystic.munge import logfile_reader
+        try:
+            logfile_reader(filepath)
+            return True
+        except: # SyntaxError, UnicodeDecodeError
+            return False
+    # file DNE, so guess from the extension
+    LOG_EXT = ('.txt','.log','.mon')
+    ext = os.path.splitext(filepath)[-1]
+    if ext in LOG_EXT or 'log' in ext or 'mon' in ext: return True
+    #DBX_EXT = ('.db','.ar','.klp','')
+    return False
+
+
+def _issupport(filepath, guess=True):
+    """return True if the filepath refers to a file written in 'support' format
+
+    is False if filepath doesn't exist, or guess based on filepath extension
+    """
+    import os
+    if os.path.exists(filepath):
+        from mystic.munge import read_raw_file
+        try:
+            return not read_raw_file(filepath).count(None)
+        except RuntimeError:
+            return False
+    if not guess: return False
+    return os.path.splitext(filepath)[-1].startswith('.py')
+
+
+def _isarchive(filepath, guess=True):
+    """return True if the filepath refers to a cached archive
+
+    is False if filepath doesn't exist, or guess based on filepath extension
+    """
+    if _issupport(filepath, guess): return False
+    if _islogfile(filepath, guess): return False
+    return guess #XXX: by default
+
+
+def _isdir(filepath, guess=True):
+    """return True if the filepath refers to a directory
+
+    is False if filepath doesn't exist, or guess based on filepath extension
+    """
+    import os
+    if os.path.exists(filepath):
+        if os.path.islink(filepath):
+            filepath = os.readline(filepath)
+        return os.path.isdir(filepath)
+    if not guess: return False
+    # file DNE, so guess it's a file if it has an extension
+    return not os.path.splitext(filepath)[-1]
+
+
+def log_converter(readpath, writepath=None, **kwds):
+    """
+convert between cached archives, convergence logfiles, and support logfiles
+
+Available from the command shell as::
+
+    mystic_log_converter readpath (writepath) [options]
+
+or as a function call::
+
+    mystic.log_converter(readpath, writepath=None, **options)
+
+Args:
+    readpath (str): path of the logfile (e.g ``paramlog.py``).
+    writepath (str, default=None): path of converted file (e.g. ``log.txt``).
+
+Returns:
+    None
+
+Notes:
+    - If *writepath* is None, write file with derived name to current directory.
+    - The option *format* takes a string name of the file format at writepath.
+      Available formats are ('logfile', 'support', or a klepto.archive type).
+"""
+    import shlex
+    from io import StringIO
+    global __quit
+    __quit = False
+    _iter = False #FIXME: if True, breaks current format of mystic.cache
+    #FIXME: if False, archive doesn't store (iter,ids), thus no repeated points
+
+    instance = None
+    # handle the special case where list is provided by sys.argv
+    if isinstance(readpath, (list,tuple)) and not kwds:
+        cmdargs = readpath # (above is used by script to parse command line)
+    elif isinstance(readpath, str) and not kwds:
+        cmdargs = shlex.split(readpath)
+    # 'everything else' is essentially the functional interface
+    else:
+        cmdargs = kwds.get('kwds', '')
+        if not cmdargs:
+            format = kwds.get('format', None)
+
+            # process "commandline" arguments
+            cmdargs = ''
+            cmdargs += '' if format is None else '--format={} '.format(format)
+        else:
+            cmdargs = ' ' + cmdargs
+        if isinstance(readpath, str):
+            cmdargs = readpath.split() + shlex.split(cmdargs)
+        else: # special case of passing in monitor instance
+            instance = readpath
+            cmdargs = shlex.split(cmdargs)
+
+    #XXX: replace with 'argparse'?
+    from optparse import OptionParser
+    def _exit(self, errno=None, msg=None):
+      global __quit
+      __quit = True
+      if errno or msg:
+        msg = msg.split(': error: ')[-1].strip()
+        raise IOError(msg)
+    OptionParser.exit = _exit
+
+    parser = OptionParser(usage=log_converter.__doc__.split('\n\nOptions:')[0])
+    parser.add_option("-f","--format",action="store",dest="format",\
+                      metavar="STR",default=None,
+                      help="format of convergence archive to write")
+
+#   import sys
+#   if 'mystic_log_converter.py' not in sys.argv:
+    f = StringIO()
+    parser.print_help(file=f)
+    f.seek(0)
+    if 'Options:' not in log_converter.__doc__:
+      log_converter.__doc__ += '\nOptions:%s' % f.read().split('Options:')[-1]
+    f.close()
+
+    try:
+      parsed_opts, parsed_args = parser.parse_args(cmdargs)
+    except UnboundLocalError:
+      pass
+    if __quit: return
+
+    try: # get path to archive to read
+      if instance:
+        raise NotImplementedError("cannot read monitor or file object")
+      else:
+        readpath = parsed_args[0]
+    except:
+      raise IOError("please provide path to read convergence log")
+
+    try: # get the path of the archive to write
+      writepath = parsed_args[1]  # e.g. 'log.txt'
+      if "None" == writepath: writepath = None
+    except:
+      writepath = None
+
+    try: # format of the archive to write
+      format = parsed_opts.format  # e.g. 'logfile'
+      if "None" == format: format = None
+    except:
+      format = None
+
+    #TODO: enable read-and-write of monitor, _iter as option, other options?
+    if isinstance(format, str) and "archive" in format:
+        import klepto.archives as kl
+        format = kl.__dict__[format]
+    file_in = _type_existing(readpath)
+    #if isinstance(file_in, str): # logfile or support
+    file_out = _type_inferred(writepath, format=format)
+    #else: # readpath is archive, so redo with format hint
+    #    file_in = _type_inferred(readpath, format=format)
+    #    file_out = _type_inferred(writepath)
+    # writepath in curdir, base derived from readpath name, with new format
+    if writepath is None:
+        import os
+        ext = _get_ext(file_out)
+        writepath = os.path.splitext(os.path.basename(readpath))[0]+ext
+    type_in = type_out = None
+    if not isinstance(file_in, str):
+        file_in,type_in = 'archive',file_in
+    if not isinstance(file_out, str):
+        file_out,type_out = 'archive',file_out
+    if file_in == file_out:
+        if file_in == 'archive':
+            msg = 'either a logfile or a support file is required'
+        else:
+            msg = 'file types cannot be identical'
+        raise TypeError(msg)
+    convert = eval("_{0}_to_{1}".format(file_in,file_out))
+    if type_in:
+        convert(readpath, writepath, type=type_in, iter=_iter)
+    elif type_out:
+        convert(readpath, writepath, type=type_out, iter=_iter)
+    else:
+        convert(readpath, writepath)
+    return
+
+
 def _visual_filter(bounds, x, z=None, rtol=1e-8, ptol=1e-8):
     """apply a visual filter specified by bounds to the data within the monitor
 
     bounds: a string specifying bounds (e.g. "0:1:.1, 0:1:.1, .5, .5, .5")
     x: an array of shape (npts, params) with one param per bound
     z: an array of shape (npts,) of cost
     rtol: float (or list[float]) of max distance beyond range defined in bounds
@@ -118,25 +646,27 @@
     """get params and cost from the given source
 
 source is the name of the trajectory logfile (or solver instance)
 if provided, ids are the list of 'run ids' to select
     """
     try: # if it's a logfile, it might be multi-id
         from mystic.munge import read_trajectories
-        step, param, cost = read_trajectories(source)
-        if not step: step = [(i,) for i in range(len(cost))]
-    except: # it's not a logfile, so read and return
+        step, param, cost = read_trajectories(source, iter=True)
+    except: # it's not a logfile, so read and convert from support format
         from mystic.munge import read_history
-        param, cost = read_history(source)
-        return [param],[cost]
+        step, param, cost = read_history(source, iter=True)
+        import numpy as np
+        param = np.array(param).reshape(len(param),-1).T.tolist()
 
     # split (i,id) into iteration and id
-    multinode = len(step[0]) - 1 if step else 0 #XXX: no step info, so give up
+    if step: #XXX: ignore non-intger ids
+        multinode = len(step[0]) - 1 if isinstance(step[0][-1], int) else 0
+    else: multinode = 0 #XXX: no step info, so give up
     if multinode: id = [(i[1] or 0) for i in step]
-    else: id = [0 for i in step]
+    else: id = [0 for i in step] #FIXME: hardwired to 0
 
     if ids is not None:
         maxid = max(id)+1
         ids = [(maxid+i if i < 0 else i) for i in ids]
 
     params = [[] for i in range(max(id) + 1)]
     costs = [[] for i in range(len(params))]
@@ -174,20 +704,21 @@
 
 def _parse_tol(tol, select=None):
     """parse 'tol' string into 'selected' and 'masked'
 
 tol specifies the max distance from the plotted surface to plotted data
 select contains the dimension specifications on which to plot
 
-For example,
+Examples:
     >>> selected, masked = _parse_tol(".05, .1, .1, .5", [0,3])
     >>> selected
     (.05, .5)
     >>> masked
     (.1, .1)
+
     >>> selected, masked = _parse_tol(".1")
     >>> selected
     .1
     >>> masked
     .1
     """
     if tol is None:
@@ -206,15 +737,15 @@
 def _parse_input(option):
     """parse 'option' string into 'select', 'axes', and 'mask'
 
 select contains the dimension specifications on which to plot
 axes holds the indices of the parameters selected to plot
 mask is a dictionary of the parameter indices and fixed values
 
-For example,
+Examples:
     >>> select, axes, mask = _parse_input("-1:10:.1, 0.0, 5.0, -50:50:.5")
     >>> select
     [0, 3]
     >>> axes
     "-1:10:.1, -50:50:.5"
     >>> mask
     {1: 0.0, 2: 5.0}
@@ -949,15 +1480,15 @@
         return fig #XXX: better?: fig.axes if len(fig.axes) > 1 else ax
     else:
         fig.savefig(out)
 
 
 def collapse_plotter(filename, **kwds):
     r"""
-generate cost convergence rate plots from file written with ``write_support_file``
+generate convergence plots of | cost - cost_min | from convergence logfile
 
 Available from the command shell as::
 
     mystic_collapse_plotter filename [options]
 
 or as a function call::
 
@@ -971,14 +1502,16 @@
 
 Notes:
     - The option *dots* takes a boolean, and will show data points in the plot.
     - The option *linear* takes a boolean, and will plot in a linear scale.
     - The option *out* takes a string of the filepath for the generated plot.
       If ``out = True``, return the Figure object instead of generating a plot.
     - The option *iter* takes an integer of the largest iteration to plot.
+    - The option *legend* takes a boolean, and will display the legend.
+    - The option *nid* takes an integer of the nth simultaneous points to plot.
     - The option *label* takes a label string. For example, ``label = "y"``
       will label the plot with a 'y', while ``label = " log-cost,
       $ log_{10}(\hat{P} - \hat{P}_{max})$"`` will label the y-axis with
       standard LaTeX math formatting. Note that the leading space is required,
       and that the text is aligned along the axis.
     - The option *col* takes a string of comma-separated integers indicating
       iteration numbers where parameter collapse has occurred. If a second set
@@ -1003,26 +1536,30 @@
         cmdargs = kwds.get('kwds', '')
         if not cmdargs:
             out = kwds.get('out', None)
             dots = kwds.get('dots', False)
            #line = kwds.get('line', False)
             linear = kwds.get('linear', False)
             iter = kwds.get('iter', None)
+            legend = kwds.get('legend', False)
+            nid = kwds.get('nid', None)
             label = kwds.get('label', None)
             col = kwds.get('col', None)
 
             if isinstance(out, bool): _out, out = out, None
 
             # process "commandline" arguments
             cmdargs = ''
             cmdargs += '' if out is None else '--out={} '.format(out)
             cmdargs += '' if dots == False else '--dots '
             cmdargs += '' if linear == False else '--linear '
            #cmdargs += '' if line == False else '--line '
             cmdargs += '' if iter is None else '--iter={} '.format(iter)
+            cmdargs += '' if legend == False else '--legend '
+            cmdargs += '' if nid is None else '--nid={} '.format(nid)
             cmdargs += '' if label == None else '--label={} '.format(label)
             cmdargs += '' if col is None else '--col="{}" '.format(col)
         else:
             cmdargs = ' ' + cmdargs
         if isinstance(filename, str):
             cmdargs = filename.split() + shlex.split(cmdargs)
         else: # special case of passing in monitor instance
@@ -1048,14 +1585,19 @@
                       default=False,help="plot y-axis in linear scale")
     parser.add_option("-u","--out",action="store",dest="out",\
                       metavar="STR",default=None,
                       help="filepath to save generated plot")
     parser.add_option("-i","--iter",action="store",dest="stop",\
                       metavar="STR",default=":",
                       help="string for smallest:largest iterations to plot")
+    parser.add_option("-n","--nid",action="store",dest="id",\
+                      metavar="INT",default=None,
+                      help="id # of the nth simultaneous points to plot")
+    parser.add_option("-g","--legend",action="store_true",dest="legend",\
+                      default=False,help="show the legend")
     parser.add_option("-l","--label",action="store",dest="label",\
                       metavar="STR",default="",\
                       help="string to assign label to y-axis")
     parser.add_option("-c","--col",action="store",dest="collapse",\
                       metavar="STR",default="",
                       help="string to indicate collapse indices")
 #   import sys
@@ -1100,76 +1642,128 @@
 
     try: # select which iteration to stop plotting at
       stop = parsed_opts.stop  # format is "1:10:1"
       stop = stop if ":" in stop else (stop+":" if "-" in stop else ":"+stop)
     except:
       stop = ":"
 
+    try: # select which 'id' to plot results for
+      runs = (int(parsed_opts.id),) #XXX: allow selecting more than one id ?
+    except:
+      runs = None # i.e. 'all' **or** use id=0, which should be 'best' energy ?
+
     try: # select collapse boundaries to plot
       collapse = parsed_opts.collapse.split(';')  # format is "2, 3; 4, 5, 6; 7"
       collapse = [eval("(%s,)" % i) if i.strip() else () for i in collapse]
     except:
       collapse = []
 
     # read file
     from mystic.munge import read_history
-    params, cost = read_history(filename)
+    step, params, cost = read_history(filename, iter=True)
 
     # ignore everything after 'stop'
-    locals = dict(cost=cost, params=params)
+    locals = dict(step=step, cost=cost, params=params)
+    step = eval('step[%s]' % stop, locals)
     cost = eval('cost[%s]' % stop, locals)
     params = eval('params[%s]' % stop, locals)
     del locals
 
+    # split (i,id) into iteration and id
+    if step: #XXX: ignore non-intger ids
+      multinode = len(step[0]) - 1 if isinstance(step[0][-1], int) else 0
+    else: multinode = 0 #XXX: no step info, so give up
+    iter = [i[0] for i in step]
+    if multinode:
+      id = [i[1] for i in step]
+    else:
+      id = [0 for i in step]
+
+    if runs is not None:
+      maxid = max(id)+1
+      runs = [maxid+i if i < 0 else i for i in runs]
+      if not set(id).intersection(runs):
+        raise IOError("please provide a valid id")
+
+    results = [[] for i in range(max(id) + 1)]
+
+    # populate results for each id with the corresponding (iter,cost)
+    for i in range(len(id)):
+      if runs is None or id[i] in runs: # take only the selected 'id'
+        results[id[i]].append((iter[i],cost[i]))
+
+    # build list of cost convergences for each id
+    cost_conv = []; iter_conv = []
+    for i in range(len(results)):
+      if len(results[i]):
+        cost_conv.append([results[i][j][1] for j in range(len(results[i]))])
+        iter_conv.append([results[i][j][0] for j in range(len(results[i]))])
+      else:
+        cost_conv.append([])
+        iter_conv.append([])
+
+    #print("iter_conv = %s" % iter_conv)
+    #print("cost_conv = %s" % cost_conv)
+
     # get the minimum cost
     import numpy as np
-    cost_min = min(cost)
+    cost_min = min(cost) #XXX: scale min per id? or vs global min???
 
-    # convert to log scale
-    x = np.arange(len(cost))
-    settings = np.seterr(all='ignore')
-    if parsed_opts.linear:
-      y = np.array(cost)
-     #y = np.abs(cost_min - np.array(cost))
-    else:
-      y = np.log10(np.abs(cost_min - np.array(cost)))
-    np.seterr(**settings)
+    colors = ['orange','red','brown','pink']
+    linestyles = ['--','-.',':','-']
 
     import matplotlib.pyplot as plt
     fig = plt.figure()
-    plt.plot(x, y, linestyle=style, marker=mark, markersize=1)
 
-    colors = ['orange','red','brown','pink']
-    linestyles = ['--','-.',':','-']
+    #NOTE: uses min(cost) of each nid
+    for i in range(len(cost_conv)):
+      if runs is None or i in runs:
+        tag = "%d" % i
+
+        # convert to log scale
+        #x = np.arange(len(cost))
+        x = iter_conv[i]
+        settings = np.seterr(all='ignore')
+        y = np.array(cost_conv[i])
+        ymin = min(y) if y.size else cost_min #avoids error when empty
+        if not parsed_opts.linear:
+          y = np.log10(np.abs(ymin - y))
+        else:
+          y = np.abs(ymin - y)
+        np.seterr(**settings)
+
+        plt.plot(x, y, label="%s" % tag, linestyle=style, marker=mark, markersize=1)
 
     for param,color,style in zip(collapse,colors,linestyles):
       for clps in set(param):
         plt.axvline(x=clps, ymin=-10, ymax=1, linestyle=style, linewidth=param.count(clps), color=color)
 
     if label:
         #plt.title('convergence rate')
         plt.xlabel('iteration number, $n$')
         plt.ylabel(label)
         #plt.ylabel('$log-error,\; log_{10}(\hat{P} - \hat{P}_{max})$')
 
+    if parsed_opts.legend: plt.legend()
+
     # process inputs
     if _out: out = _out
     if out: out = _out or out
 
     if not out:
         plt.show()
     elif out is True:
         return fig #XXX: better?: fig.axes if len(fig.axes) > 1 else ax
     else:
         fig.savefig(out)
 
 
 def log_reader(filename, **kwds):
     """
-plot parameter convergence from file written with ``LoggingMonitor``
+generate parameter convergence plot from convergence logfile
 
 Available from the command shell as::
 
     mystic_log_reader filename [options]
 
 or as a function call::
 
@@ -1187,15 +1781,16 @@
     - The option *dots* takes a boolean, and will show data points in the plot.
     - The option *line* takes a boolean, and will connect the data with a line.
     - The option *iter* takes an integer of the largest iteration to plot.
     - The option *legend* takes a boolean, and will display the legend.
     - The option *nid* takes an integer of the nth simultaneous points to plot.
     - The option *param* takes an indicator string. The indicator string is
       built from comma-separated array slices. For example, ``param = ":"``
-      will plot all parameters.  Alternatively, ``param = ":2, 3:"`` will plot      all parameters except for the third parameter, while ``param = "0"``
+      will plot all parameters.  Alternatively, ``param = ":2, 3:"`` will plot
+      all parameters except for the third parameter, while ``param = "0"``
       will only plot the first parameter.
 """
     import shlex
     from io import StringIO
     global __quit
     __quit = False
     _out = False
@@ -1349,31 +1944,32 @@
     #   Legend is different for list versus [list1,...]
     #   Plot should be discontinuous for (i,) then (0,)
 
     # parse file contents to get (i,id), cost, and parameters
     try:
         instance = instance if instance else filename
         from mystic.munge import read_trajectories
-        step, param, cost = read_trajectories(instance)
-        if not step: step = [(i,) for i in range(len(cost))]
+        step, param, cost = read_trajectories(instance, iter=True)
     except SyntaxError:
         from mystic.munge import read_raw_file
         read_raw_file(filename)
         msg = "incompatible file format, try 'support_convergence %s'" % filename
         raise SyntaxError(msg)
 
     # ignore everything after 'stop'
     locals = dict(step=step, cost=cost, param=param)
     step = eval('step[%s]' % stop, locals)
     cost = eval('cost[%s]' % stop, locals)
     param = eval('param[%s]' % stop, locals)
     del locals
 
     # split (i,id) into iteration and id
-    multinode = len(step[0]) - 1  if step else 0 #XXX: no step info, so give up
+    if step: #XXX: ignore non-intger ids
+      multinode = len(step[0]) - 1 if isinstance(step[0][-1], int) else 0
+    else: multinode = 0 #XXX: no step info, so give up
     iter = [i[0] for i in step]
     if multinode:
       id = [i[1] for i in step]
     else:
       id = [0 for i in step]
 
     # build the list of selected parameters
@@ -1449,14 +2045,17 @@
 # initialize doc
 try: log_reader()
 except TypeError:
     pass
 try: model_plotter()
 except TypeError:
     pass
+try: log_converter()
+except TypeError:
+    pass
 try: collapse_plotter()
 except TypeError:
     pass
 
 
 
 if __name__ == '__main__':
```

### Comparing `mystic-0.4.0/mystic/search.py` & `mystic-0.4.1/mystic/search.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 a global searcher
 """
 #FIXME: refactor to use mystic.samplers (and code in _workflow)
 
@@ -49,28 +49,28 @@
    #    _solve - spray multiple seekers
 
     def __init__(self, npts=4, retry=1, tol=8, memtol=1, memsize=None,
                        map=None, archive=None, cache=None, sprayer=None,
                        seeker=None, traj=False, disp=False, repeat=0):
         """searcher, which searches for all minima of a response surface
 
-        Input:
-          npts - number of solvers in the ensemble
-          retry - max consectutive retries w/o a cache 'miss'
-          tol - rounding precision for the minima comparator
-          memtol - rounding precision for memoization
-          memsize - maximum size of cache to hold in memory
-          map - map used for spawning solvers in the ensemble
-          archive - the sampled point archive(s)
-          cache - the trajectory cache(s)
-          sprayer - the mystic.ensemble instance
-          seeker - the mystic.solvers instance
-          traj - if True, save the parameter trajectories
-          disp - if True, be verbose
-          repeat - number of times to repeat the search
+    Input:
+      npts - number of solvers in the ensemble
+      retry - max consectutive retries w/o a cache 'miss'
+      tol - rounding precision for the minima comparator
+      memtol - rounding precision for memoization
+      memsize - maximum size of cache to hold in memory
+      map - map used for spawning solvers in the ensemble
+      archive - the sampled point archive(s)
+      cache - the trajectory cache(s)
+      sprayer - the mystic.ensemble instance
+      seeker - the mystic.solvers instance
+      traj - if True, save the parameter trajectories
+      disp - if True, be verbose
+      repeat - number of times to repeat the search
         """
         #XXX: better not to use klepto as default? just dict and false cache?
         from klepto.archives import dict_archive as _archive
         from mystic.solvers import BuckshotSolver #XXX: or SparsitySolver?
         from mystic.solvers import PowellDirectionalSolver
         from mystic.pools import SerialPool as Pool
         from builtins import map as _map
@@ -203,26 +203,26 @@
         self.disp = bool(disp)
         return
 
     #FIXME: instead, take a configured solver?
     def Search(self, model, bounds, stop=None, traj=None, disp=None, **kwds):
         """use an ensemble of optimizers to search for all minima
 
-        Inputs:
-          model - function z=f(x) to be used as the objective of the Searcher
-          bounds - tuple of floats (min,max), bounds on the search region
-          stop - termination condition
-          traj - klepto.archive to store sampled points
-          disp - if True, be verbose
-          monitor - mystic.monitor instance to store parameter trajectories
-          evalmon - mystic.monitor instance to store parameter evaluations
-          penalty - mystic.penalty instance of the form y' = k*p(x)
-          constraints - mystic.constraints instance of the form x' = c(x)
-          tightrange - if True, apply bounds concurrent with other constraints
-          cliprange - if True, bounding constraints will clip exterior values
+    Input:
+      model - function z=f(x) to be used as the objective of the Searcher
+      bounds - tuple of floats (min,max), bounds on the search region
+      stop - termination condition
+      traj - klepto.archive to store sampled points
+      disp - if True, be verbose
+      monitor - mystic.monitor instance to store parameter trajectories
+      evalmon - mystic.monitor instance to store parameter evaluations
+      penalty - mystic.penalty instance of the form y' = k*p(x)
+      constraints - mystic.constraints instance of the form x' = c(x)
+      tightrange - if True, apply bounds concurrent with other constraints
+      cliprange - if True, bounding constraints will clip exterior values
         """
         self.traj = self.traj if traj is None else traj
         self.disp = self.disp if disp is None else disp
         self._configure(model, bounds, stop, **kwds)
         sid = 0  # keep track of which solver is which across multiple runs
         run = -1
         while run < self.repeat: # stop after repeat 'runs'
@@ -242,61 +242,61 @@
 
         #NOTE: traj & disp are sticky
         return
 
     def Reset(self, cache=None, inv=None):
         """clear the trajectory cache of sampled points
 
-        Input:
-          cache - the trajectory cache(s)
-          inv - if True, reset the cache for the inverse of the objective
+    Input:
+      cache - the trajectory cache(s)
+      inv - if True, reset the cache for the inverse of the objective
         """
         if cache is None: self.cache.clear() #XXX: clear the archive?
         self.cache = self.cache if cache is None else cache
         [self._allSolvers.pop() for i in range(len(self._allSolvers))]
         if inv is not None: self._inv = inv
 
     def Values(self, unique=False, all=False):
         """return the sequence of stored response surface outputs
 
-        Input:
-          unique: if True, only return unique values
-          all: if True, return all sampled values (not just trajectory values)
+    Input:
+      unique: if True, only return unique values
+      all: if True, return all sampled values (not just trajectory values)
 
-        Output:
-          a list of stored response surface outputs
+    Returns:
+      a list of stored response surface outputs
         """
         archive = self.archive if all else self.cache
         vals = archive.values()
         new = set()
         return [v for v in vals if v not in new and not new.add(v)] if unique else list(vals)
 
     def Coordinates(self, unique=False, all=False):
         """return the sequence of stored model parameter input values
 
-        Input:
-          unique: if True, only return unique values
-          all: if True, return all sampled inputs (not just trajectory inputs)
+    Input:
+      unique: if True, only return unique values
+      all: if True, return all sampled inputs (not just trajectory inputs)
 
-        Output:
-          a list of parameter trajectories
+    Returns:
+      a list of parameter trajectories
         """
         archive = self.archive if all else self.cache
         keys = archive.keys()
         new = set()
         return [k for k in keys if k not in new and not new.add(k)] if unique else list(keys)
 
     def Minima(self, tol=None): #XXX: unique?
         """return a dict of (coordinates,values) of all discovered minima
 
-        Input:
-          tol: tolerance within which to consider a point a minima
+    Input:
+      tol: tolerance within which to consider a point a minima
 
-        Output:
-          a dict of (coordinates,values) of all discovered minima
+    Returns:
+      a dict of (coordinates,values) of all discovered minima
         """
         if tol is None: tol=self.tol
         data = self.cache
         _min = max if self._inv else min
         _min = _min(data.values())
         return dict((k,v) for (k,v) in data.items() if round(v, tol) == round(_min, tol))
 
@@ -320,23 +320,23 @@
         """return tuple (iteration, coordinates, cost) of all trajectories
         """
         mon = '_evalmon' if all else '_stepmon'
         from mystic.munge import read_trajectories
         if not self.traj:
             try: #NOTE: FRAGILE (if absolute path is not used)
                 filename = getattr(self.solver, mon)._filename
-                step, param, cost = read_trajectories(filename)
+                step, param, cost = read_trajectories(filename, iter=True)
             except AttributeError:
                 msg = "a LoggingMonitor or UseTrajectories is required"
                 raise RuntimeError(msg)
         else:
             step = []; cost = []; param = [];
             for sprayer in self._allSolvers:  #XXX: slow? better thread.map?
                 for seeker in sprayer._allSolvers:
-                    values = read_trajectories(getattr(seeker,mon))
+                    values = read_trajectories(getattr(seeker,mon), iter=True)
                     step.extend(values[0])
                     param.extend(values[1])
                     cost.extend(values[2])
         #XXX: (not from archive, so) if self._inv: use -cost
         return step, param, cost
 
     def Samples(self, all=False):
```

### Comparing `mystic-0.4.0/mystic/solvers.py` & `mystic-0.4.1/mystic/solvers.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 solvers: minimal and expanded interfaces for optimization algorithms
 
 
 Standard Interface
@@ -58,14 +58,15 @@
     - ``mystic.scipy_optimize``           [scipy local-search solvers]
     - ``mystic.ensemble``                 [pseudo-global solvers]
 
 or the API documentation found here:
     - ``mystic.abstract_solver``          [the solver API definition]
     - ``mystic.abstract_map_solver``      [the parallel solver API]
     - ``mystic.abstract_ensemble_solver`` [the ensemble solver API]
+
 """
 # global optimizers
 from mystic.differential_evolution import DifferentialEvolutionSolver
 from mystic.differential_evolution import DifferentialEvolutionSolver2
 from mystic.differential_evolution import diffev, diffev2
 
 # pseudo-global optimizers
@@ -78,15 +79,23 @@
 from mystic.scipy_optimize import NelderMeadSimplexSolver
 from mystic.scipy_optimize import PowellDirectionalSolver
 from mystic.scipy_optimize import fmin, fmin_powell
 
 
 # load a solver from a restart file
 def LoadSolver(filename=None, **kwds):
-    """load solver state from a restart file"""
+    """load solver state from a restart file
+
+Args:
+    filename (str, default=None): path of solver restart file
+    **kwds (dict, default={}): solver state overrides
+
+Returns:
+    solver instance
+    """
     if filename is None:
         filename = kwds['_state'] if '_state' in kwds else None
     #XXX: only allow a list override keys (lookup values from self)
 #   if filename is None: filename = self._state
 #   if filename is None:
 #       solver = self
 #   else:
```

### Comparing `mystic-0.4.0/mystic/strategy.py` & `mystic-0.4.1/mystic/strategy.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 # Differential Evolution Strategies adapted from DESolver.py by Patrick Hung
 """
 Differential Evolution Strategies
```

### Comparing `mystic-0.4.0/mystic/support.py` & `mystic-0.4.1/mystic/support.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 __doc__ = """
 functional interfaces for mystic's visual diagnistics for support files
 """
 
 __all__ = ['convergence', 'hypercube', 'hypercube_measures', \
@@ -27,15 +27,15 @@
   n (int): number of plots
 
 Returns:
   tuple ``(i,j)`` of ``i`` rows ``j`` columns, where ``i*j`` is roughly ``n``
   """
   from mystic.tools import factor
   allfactors = list(factor(n))
-  from numpy import product
+  from numpy import prod as product
   cand = [1] + [product(allfactors[:i+1]) for i in range(len(allfactors))]
  #return cand[-1], n/cand[-1]
   best = [cand[len(cand)//2], n//cand[len(cand)//2]]
   best.sort(reverse=True)
   return tuple(best)
 # if len(cand)%2:
 #   return cand[len(cand)/2], cand[len(cand)/2]
@@ -407,16 +407,21 @@
     except UnboundLocalError:
         pass
     if __quit: return
 
     # get the name of the parameter log file
     if instance is None:
         instance = parsed_args[0]
-    from mystic.munge import read_history
-    params, cost = read_history(instance)
+    from mystic.munge import read_history, _reduce_ids
+    ids, params, cost = read_history(instance, iter=True)
+
+    # convert ids to a list of ints
+    ids = _reduce_ids(ids)
+    if ids.count(None) == len(ids): #XXX: 1-D, replace None with 0
+        ids = [0]*len(ids)
 
     if parsed_opts.cost: # also plot the cost
        #exec "from {file} import cost".format(file=file)
         pass
     else:
         cost = None
 
@@ -462,23 +467,33 @@
         if isinstance(select[i], int): select[i] = str(select[i])
         if select[i] == '-1': select[i] = 'len(params)-1:len(params)'
         elif not select[i].count(':'):
             select[i] += ':' + str(int(select[i])+1)
 
     # take only the first 'step' iterations
     params = [var[:step] for var in params]
+    ids = ids[:step]
     if cost:
         cost = cost[:step]
 
     # take only the selected 'id'
-    if id != None:
-        param = []
-        for j in range(len(params)):
-            param.append([p[id] for p in params[j]])
-        params = param[:]
+    if ids and not isinstance(ids[0], int):
+        ids = [0]*len(ids)
+    if id != None: #XXX: use mystic.scripts._get_history? 
+        from numpy import where, array
+        ids = where(array(ids) == id)[0]
+        for k in range(len(params)):
+            params[k] = [j for i,j in enumerate(params[k]) if i in ids]
+        if cost:
+            cost = [j for i,j in enumerate(cost) if i in ids]
+        ids = [id]*len(ids)
+    else:
+        if len(set(ids)) > 1: #FIXME: enable plot of all ids
+            msg = "select `nid`, or try mystic_log_reader"
+            raise ValueError(msg)
 
     # handle special case where only plot the cost
     if cost and len(select) == 1 and select[0].endswith(':0'):
         dim1,dim2 = best_dimensions(1)
 
         import matplotlib.pyplot as plt
         fig = plt.figure()
@@ -699,15 +714,15 @@
         pass
     if __quit: return
 
     # get the name of the parameter log file
     if instance is None:
         instance = parsed_args[0]
     from mystic.munge import read_history
-    params, _cost = read_history(instance)
+    params, _cost = read_history(instance, iter=False)
     # would be nice to use meta = ['wx','wx2','x','x2','wy',...]
     # exec "from {file} import meta".format(file=file)
 
     try: # select the bounds
         bounds = parsed_opts.bounds.split(",")  # format is "60:105, 0:30, 2.1:2.8"
         bounds = [tuple(float(j) for j in i.split(':')) for i in bounds]
     except:
@@ -1033,15 +1048,15 @@
         pass
     if __quit: return
 
     # get the name of the parameter log file
     if instance is None:
         instance = parsed_args[0]
     from mystic.munge import read_history
-    params, _cost = read_history(instance)
+    params, _cost = read_history(instance, iter=False)
     # would be nice to use meta = ['wx','wx2','x','x2','wy',...]
     # exec "from {file} import meta".format(file=file)
 
     try: # path of plot output file
       out = parsed_opts.out  # e.g. 'myplot.png'
       if "None" == out: out = None
     except:
@@ -1418,15 +1433,15 @@
         pass
     if __quit: return
 
     # get the name of the parameter log file
     if instance is None:
         instance = parsed_args[0]
     from mystic.munge import read_history
-    params, _cost = read_history(instance)
+    params, _cost = read_history(instance, iter=False)
     # would be nice to use meta = ['wx','wx2','x','x2','wy',...]
     # exec "from {file} import meta".format(file=file)
 
     from mystic.math.discrete import scenario
     from mystic.math.legacydata import dataset
     try: # select whether to plot the cones
         cones = parsed_opts.cones
```

### Comparing `mystic-0.4.0/mystic/svc.py` & `mystic-0.4.1/mystic/svc.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,18 +1,19 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Simple utility functions for SV-classifications
 """
+__all__ = ['KernelMatrix', 'WeightVector', 'SupportVectors', 'Bias']
 
 from numpy import multiply, asarray, dot, transpose, sum
 
 def KernelMatrix(X, k=dot): #XXX: generalized dot/inner product?  K(X,Y)?
     "inner product of X with self, using k as elementwise product function"
     # the following is tensordot(X,X,axes=(-1,-1)), with dot --> k
     # 3-clause BSD (see: v1.7.2 http://docs.scipy.org/doc/numpy/license.html)
```

### Comparing `mystic-0.4.0/mystic/svr.py` & `mystic-0.4.1/mystic/svr.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Simple utility functions for SV-Regressions
 """
 import numpy as np
 import mystic.math.distance as _distance
```

### Comparing `mystic-0.4.0/mystic/symbolic.py` & `mystic-0.4.1/mystic/symbolic.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2010-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 # originally coded by Alta Fang, 2010
 # refactored by Mike McKerns, 2012
 """Tools for working with symbolic constraints.
 """
@@ -24,29 +24,30 @@
 
 
 # XXX: another function for the inverse... symbolic to matrix? (good for scipy)
 def linear_symbolic(A=None, b=None, G=None, h=None, variables=None):
     """convert linear equality and inequality constraints from matrices to a 
 symbolic string of the form required by mystic's constraint parser.
 
-Inputs:
-    A -- (ndarray) matrix of coefficients of linear equality constraints
-    b -- (ndarray) vector of solutions of linear equality constraints
-    G -- (ndarray) matrix of coefficients of linear inequality constraints
-    h -- (ndarray) vector of solutions of linear inequality constraints
-    variables -- (list[str]) list of variable names
-
-    NOTE: if variables=None, then variables = ['x0', 'x1', ...];
-          if variables='y', then variables = ['y0', 'y1', ...];
-          otherwise use the explicit list of variables provided.
+Args:
+    A (ndarray, default=None): matrix of coefficients of equality constraints
+    b (ndarray, default=None): vector of solutions of equality constraints
+    G (ndarray, default=None): matrix of coefficients of inequality constraints
+    h (ndarray, default=None): vector of solutions of inequality constraints
+    variables (list[str], default=None): list of variable names
+
+Notes:
+    if ``variables=None``, then ``variables = ['x0', 'x1', ...]``;
+    if ``variables='y'``, then ``variables = ['y0', 'y1', ...]``;
+    otherwise use the explicit list of variables provided.
 
-    NOTE: Must provide A and b; G and h; or A, b, G, and h;
-          where Ax = b and Gx <= h. 
+    Must provide ``A, b``, ``G, h``, or ``A, b, G, h``;
+    where ``Ax = b`` and ``Gx <= h``. 
 
-    For example:
+Examples:
     >>> A = [[3., 4., 5.],
     ...      [1., 6., -9.]]
     >>> b = [0., 0.]
     >>> G = [1., 0., 0.]
     >>> h = [5.]
     >>> print(linear_symbolic(A,b,G,h))
     1.0*x0 + 0.0*x1 + 0.0*x2 <= 5.0
@@ -122,24 +123,25 @@
     totalconstraints = ineqstring + eqstring
     return totalconstraints 
 
 
 def symbolic_bounds(min, max, variables=None):
     """convert min,max to symbolic string for use in mystic's constraint parser
 
-Inputs:
-    min -- (list[float]) list of lower bounds
-    max -- (list[float]) list of upper bounds
-    variables -- (list[str]) list of variable names
-
-    NOTE: if variables=None, then variables = ['x0', 'x1', ...];
-          if variables='y', then variables = ['y0', 'y1', ...];
-          otherwise use the explicit list of variables provided.
+Args:
+    min (list[float]): list of lower bounds
+    max (list[float]): list of upper bounds
+    variables (list[str], default=None): list of variable names
+
+Notes:
+    if ``variables=None``, then ``variables = ['x0', 'x1', ...]``;
+    if ``variables='y'``, then ``variables = ['y0', 'y1', ...]``;
+    otherwise use the explicit list of variables provided.
 
-    For example:
+Examples:
     >>> eqn = symbolic_bounds(min=[-10,None], max=[10,69], variables='y')
     >>> print(eqn)
     y0 >= -10.0
     y0 <= 10.0
     y1 <= 69.0
 
     >>> eqn = symbolic_bounds(min=[-1,-2], max=[1,2], variables=list('AB'))
@@ -198,40 +200,40 @@
     return '<=' if cmp == '>=' else '<' if cmp == '>' else \
            '>=' if cmp == '<=' else '>' if cmp == '<' else cmp
 
 
 def flip(equation, bounds=False):
     """flip the inequality in the equation (i.e. '<' to '>'), if one exists
 
-Inputs:
-    equation -- an equation string; can be an equality or inequality
-    bounds -- if True, ensure set boundaries are respected (i.e. '<' to '>=')
+Args:
+    equation (str): an equation string; can be an equality or inequality
+    bounds (bool, default=False): maintain set boundaries (i.e. '<' to '>=')
 """
     cmp = comparator(equation)
     return _flip(cmp, bounds).join(equation.split(cmp)) if cmp else equation
 
 
 #FIXME: if 'cycle=True', do all permutations (and select shortest)?
 #FIXME: should be better, currently only condenses exact matches
 def condense(*equations, **kwds):
     """condense tuples of equations to the simplest representation
 
-Inputs:
-    equations -- tuples of inequalities or equalities
+Args:
+    equations (tuple[str]): tuples of inequalities or equalities
+    verbose (bool, default=False): if True, print diagnostic information
 
-    For example:
+Examples:
     >>> condense(('C <= 0', 'B <= 0'), ('C <= 0', 'B >= 0'))
     [('C <= 0',)]
+
     >>> condense(('C <= 0', 'B <= 0'), ('C >= 0', 'B <= 0'))
     [('B <= 0',)]
+
     >>> condense(('C <= 0', 'B <= 0'), ('C >= 0', 'B >= 0'))
     [('C <= 0', 'B <= 0'), ('C >= 0', 'B >= 0')]
-
-Additional Inputs:
-    verbose -- if True, print diagnostic information. Default is False.
 """
     verbose = kwds['verbose'] if 'verbose' in kwds else False
     result, miss = [],[]
     skip = set()
     found = False
     for i,u in enumerate(equations):
         if i in skip: continue
@@ -327,19 +329,19 @@
         return variable[1:-1]
     return variable
 
 
 def flat(equation, subs=None):
     """flatten equation by replacing expressions in parenthesis with a marker
 
-Inputs:
-    equation -- a symbolic equation string, with no more than one line, and
-        following standard python syntax.
-    subs -- a dict of {marker: sub-string} of replacements made, where marker
-        will be of the form '$0$', '$1$', etc.
+Args:
+    equation (str): a symbolic equation string, with no more than one line,
+        and following standard python syntax.
+    subs (dict, default=None): dict of ``{marker: sub-string}`` of replacements
+        made, where marker will be of the form ``'$0$'``, ``'$1$'``, etc.
     """
     eqn = _enclosed(equation)
     for i,e in enumerate(eqn):
         marker = '$%s$' % i
         # find the enclosed expression
         _e = e[e.find('(')+1:-1]
         if not subs is None:
@@ -355,20 +357,21 @@
     import re
     return [''.join(i).strip('/') for i in re.findall(r'(/\s*[\(\$\w\)]+)(\*\*[\(\$\w\)]+)?', equation)]
 
 
 def denominator(equation, variables=None):
     """find denominators containing the given variables in an equation
 
-Inputs:
-    equation -- a symbolic equation string, with no more than one line.
+Args:
+    equation (str): a symbolic equation string, with no more than one line.
         Equation can be an equality or inequality, and must follow standard
-        python syntax (with the math and numpy modules already imported).
-    variables -- a variable base string (e.g. 'x' = 'x0','x1',...), or
-        a list of variable name strings (e.g. ['x','y','z0']). Default is 'x'.
+        python syntax (the ``math`` and ``numpy`` modules are already imported).
+    variables (str, defaut=None): base string (e.g. ``'x'`` = 'x0','x1',...),
+        or a list of variable name strings (e.g. ``['x','y','z0']``).
+        Default is ``'x'``.
     """
     if variables is None: variables = 'x'
     # deal with the lhs and rhs separately
     cmp = comparator(equation)
     if cmp:
         res,equation = equation.split(cmp,1)
         res = set(denominator(res, variables))
@@ -418,24 +421,22 @@
     return res + _res
 
 
 #XXX: if error=False, should return None? or ???
 def equals(before, after, vals=None, **kwds):
     """check if equations before and after are equal at the given vals
 
-Inputs:
-    before -- an equation string
-    after -- an equation string
-    vals -- a dict with variable names as keys and floats as values
-
-Additional Inputs:
-    variables -- a list of variable names
-    locals -- a dict with variable names as keys and 'fixed' values
-    error -- if False, ZeroDivisionError evaluates as None
-    variants -- a list of ints to use as variants for fractional powers
+Args:
+    before (str): an equation string
+    after (str): an equation string
+    vals (dict, default=None): dict with variable names as keys and float values
+    variables (list[str], default='x'): a list of variable names
+    locals (dict, default={}): dict with variable names as keys and fixed values
+    error (bool, default=True): if False, ZeroDivisionError evaluates as None
+    variants (list[int], default=None): list of variants for fractional powers
 """ #verbose -- print debug messages
     errors = kwds['error'] if 'error' in kwds else True#XXX: default of False?
     variants = kwds['variants'] if 'variants' in kwds else None
     #verbose = kwds['verbose'] if 'verbose' in kwds else False
     vars = kwds['variables'] if 'variables' in kwds else 'x'
     _vars = get_variables(after, vars)
     locals = kwds['locals'] if 'locals' in kwds else None
@@ -556,25 +557,23 @@
 
 def absval(constraints, **kwds):
     """rewrite a system of symbolic constraints without using absolute value.
 
 Returns a system of equations where 'abs' has been replaced with the
 equivalent conditional algebraic expressions.
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
-        equation per line. Standard python syntax should be followed (with
-        the math and numpy modules already imported).
-
-Additional Inputs:
-    all -- boolean to return all simplifications due to absolute values.
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
+        equation per line. Standard python syntax should be followed (the
+        ``math`` and ``numpy`` modules are already imported).
+    all (bool, default=False): return all simplifications due to absolute values
         If all is True, return all possible simplifications due to absolute
-        value being used in one or more of the equations. The default is
-        False, returning only one possible simplification.
-    verbose -- if True, print debug information [False]
+        value being used in one or more of the equations. If False, return
+        only one possible simplification.
+    verbose (bool, default=False): if True, print debug information.
 """
     import random
     import itertools as it
     all = kwds['all'] if 'all' in kwds else False
     verbose = kwds['verbose'] if 'verbose' in kwds else False
     abs_ = 'abs('
     eqns = [([''.join((i,j)) for i,j in zip(*_absval(e.strip(), **kwds))] if abs_ in e else [e.strip()]) for e in constraints.strip().split(NL)]
@@ -587,77 +586,79 @@
 #FIXME: should not fail at ZeroDivisionError (what should it do there?)
 #FIXME: should order better (e.g. C > 0; B == C - 5; A > B + 2)
 def _simplify(constraints, variables='x', target=None, **kwds):
     """simplify a system of symbolic constraints equations.
 
 Returns a system of equations where a single variable has been isolated on
 the left-hand side of each constraints equation, thus all constraints are
-of the form "x_i = f(x)".
+of the form ``x_i = f(x)``.
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
-        equation per line. Standard python syntax should be followed (with
-        the math and numpy modules already imported).
-
-    For example:
-        >>> constraints = '''
-        ...     x0 - x2 <= 2.
-        ...     x2 = x3*2.'''
-        >>> print(simplify(constraints))
-        x0 <= x2 + 2.0
-        x2 = 2.0*x3
-        >>> constraints = '''
-        ...     x0 - x1 - 1.0 = mean([x0,x1])   
-        ...     mean([x0,x1,x2]) >= x2'''
-        >>> print(simplify(constraints))
-        x0 = 3.0*x1 + 2.0
-        x0 >= -x1 + 2*x2
-
-Additional Inputs:
-    variables -- desired variable name. Default is 'x'. A list of variable
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
+        equation per line. Standard python syntax should be followed (the
+        ``math`` and ``numpy`` modules are already imported).
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
-    target -- list providing the order for which the variables will be solved.
-        If there are "N" constraint equations, the first "N" variables given
-        will be selected as the dependent variables. By default, increasing
-        order is used.
-
-Further Inputs:
-    locals -- a dictionary of additional variables used in the symbolic
+    target (list[str], default=None): list providing the order for which the
+        variables will be solved. If there are N constraint equations, the
+        first N variables given will be selected as the dependent variables.
+        By default, increasing order is used.
+    locals (dict, default={}): additional variables used in the symbolic
         constraints equations, and their desired values.
-    cycle -- boolean to cycle the order for which the variables are solved.
+    cycle (bool, default=False): cycle the order for which variables are solved.
         If cycle is True, there should be more variety on the left-hand side
         of the simplified equations. By default, the variables do not cycle.
-    all -- boolean to return all simplifications due to negative values.
+    all (bool, default=False): return all simplifications due to negatives.
         When dividing by a possibly negative variable, an inequality may flip,
         thus creating alternate simplifications. If all is True, return all
         possible simplifications due to negative values in an inequalty.
         The default is False, returning only one possible simplification.
-    simplest -- if True, simplify all but polynomials order >= 3 [False]
-    rational -- if True, recast floats as rationals during solve [False]
-    sequence -- if True, solve sequentially and not as a matrix [False]
-    implicit -- if True, solve implicitly (with sin, cos, ...) [False]
-    check -- if False, skip minimal testing (divide_by_zero, ...) [True]
-    permute -- if True, return all permutations [False]
-    warn -- if True, don't suppress warnings [False]
-    verbose -- if True, print debug information [False]
+    simplest (bool, default=False): simplify all but polynomials order >= 3
+    rational (bool, default=False): recast floats as rationals during solve
+    sequence (bool, default=False): solve sequentially and not as a matrix
+    implicit (bool, default=False): solve implicitly (with sin, cos, ...)
+    check (bool, default=True): perform validity testing (divide_by_zero, ...)
+    permute (bool, default=False): return all permutations (*expensive*)
+    warn (bool, default=False): if True, don't suppress warnings
+    verbose (bool, default=False): print debug information
+
+Notes:
+    By default, the top-level namespace of ``numpy`` and ``math`` are
+    imported into ``locals``.
+
+Examples:
+    >>> constraints = '''
+    ...     x0 - x2 <= 2.
+    ...     x2 = x3*2.'''
+    >>> print(simplify(constraints))
+    x0 <= x2 + 2.0
+    x2 = 2.0*x3
+
+    >>> constraints = '''
+    ...     x0 - x1 - 1.0 = mean([x0,x1])   
+    ...     mean([x0,x1,x2]) >= x2'''
+    >>> print(simplify(constraints))
+    x0 = 3.0*x1 + 2.0
+    x0 >= -x1 + 2*x2
 """
     ### undocumented ###
    #rand -- random number generator [default: random.random]
    #error -- if False, ZeroDivisionError evaluates as None [default: True]
     ####################
     all = kwds['all'] if 'all' in kwds else False
     import random
     import itertools as it
     locals = kwds['locals'] if 'locals' in kwds else {} #XXX: HACK _locals
     _locals = {}
     # default is _locals with numpy and math imported
     # numpy throws an 'AttributeError', but math passes error to sympy
     code = """from numpy import *; from math import *;""" # prefer math
+    code += """from builtins import *;""" # don't overload builtins
     code += """from numpy import mean as average;""" # use np.mean not average
     code += """from numpy import var as variance;""" # look like mystic.math
     code += """from numpy import ptp as spread;"""   # look like mystic.math
     code += """_sqrt = lambda x:x**.5;""" # 'domain error' to 'negative power'
     code = compile(code, '<string>', 'exec')
     exec(code, _locals)
     _locals.update(locals)
@@ -810,40 +811,37 @@
 simplify.__doc__ = _simplify.__doc__
 
 
 def replace_variables(constraints, variables=None, markers='$'):
     """replace variables in constraints string with a marker.
 Returns a modified constraints string.
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
         equation per line. Constraints can be equality and/or inequality
-        constraints. Standard python syntax should be followed (with the
-        math and numpy modules already imported).
-    variables -- list of variable name strings. The variable names will
-        be replaced in the order that they are provided, where if the
-        default marker "$i" is used, the first variable will be replaced
-        with "$0", the second with "$1", and so on.
-
-    For example:
-        >>> variables = ['spam', 'eggs']
-        >>> constraints = '''spam + eggs - 42'''
-        >>> print(replace_variables(constraints, variables, 'x'))
-        'x0 + x1 - 42'
-
-Additional Inputs:
-    markers -- desired variable name. Default is '$'. A list of variable
+        constraints. Standard python syntax should be followed (the ``math``
+        and ``numpy`` modules are already imported).
+    variables (list[str], default=None): list of variable name strings.
+        The variable names will be replaced in the order that they are
+        provided. If the default marker ``"$i"`` is used, the first variable
+        will be replaced with ``"$0"``, the second with ``"$1"``, and so on.
+    markers (str, default='$'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base.
 
-    For example:
-        >>> variables = ['x1','x2','x3']
-        >>> constraints = "min(x1*x2) - sin(x3)"
-        >>> print(replace_variables(constraints, variables, ['x','y','z']))
-        'min(x*y) - sin(z)'
+Examples:
+    >>> variables = ['spam', 'eggs']
+    >>> constraints = '''spam + eggs - 42'''
+    >>> print(replace_variables(constraints, variables, 'x'))
+    'x0 + x1 - 42'
+
+    >>> variables = ['x1','x2','x3']
+    >>> constraints = "min(x1*x2) - sin(x3)"
+    >>> print(replace_variables(constraints, variables, ['x','y','z']))
+    'min(x*y) - sin(z)'
 """
     if variables is None: variables = []
     elif isinstance(variables, str): variables = list((variables,))
 
     # substitite one list of strings for another
     if list_or_tuple_or_ndarray(markers):
         equations = replace_variables(constraints,variables,'_')
@@ -880,40 +878,37 @@
         constraints = constraints.replace(variables[i], marker + str(i))
     return constraints.replace(marker, markers)
 
 
 def get_variables(constraints, variables='x'):
     """extract a list of the string variable names from constraints string
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
         equation per line. Constraints can be equality and/or inequality
-        constraints. Standard python syntax should be followed (with the
-        math and numpy modules already imported).
-
-    For example:
-        >>> constraints = '''
-        ...     x1 + x2 = x3*4
-        ...     x3 = x2*x4'''
-        >>> get_variables(constraints)
-        ['x1', 'x2', 'x3', 'x4'] 
-
-Additional Inputs:
-    variables -- desired variable name. Default is 'x'. A list of variable
+        constraints. Standard python syntax should be followed (the ``math``
+        and ``numpy`` modules are already imported).
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
 
-    For example:
-        >>> constraints = '''              
-        ...     y = min(u,v) - z*sin(x)
-        ...     z = x**2 + 1.0 
-        ...     u = v*z'''
-        >>> get_variables(constraints, list('pqrstuvwxyz'))
-        ['u', 'v', 'x', 'y', 'z']
+Examples:
+    >>> constraints = '''
+    ...     x1 + x2 = x3*4
+    ...     x3 = x2*x4'''
+    >>> get_variables(constraints)
+    ['x1', 'x2', 'x3', 'x4'] 
+
+    >>> constraints = '''              
+    ...     y = min(u,v) - z*sin(x)
+    ...     z = x**2 + 1.0 
+    ...     u = v*z'''
+    >>> get_variables(constraints, list('pqrstuvwxyz'))
+    ['u', 'v', 'x', 'y', 'z']
 """
     if list_or_tuple_or_ndarray(variables):
         equations = replace_variables(constraints,variables,'_')
         vars = get_variables(equations,'_')
         indices = [int(v.strip('_')) for v in vars]
         varnamelist = []
         from numpy import sort
@@ -933,35 +928,33 @@
     return varnamelist
 
 
 def penalty_parser(constraints, variables='x', nvars=None):
     """parse symbolic constraints into penalty constraints.
 Returns a tuple of inequality constraints and a tuple of equality constraints.
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
         equation per line. Constraints can be equality and/or inequality
-        constraints. Standard python syntax should be followed (with the
-        math and numpy modules already imported).
-
-    For example:
-        >>> constraints = '''
-        ...     x2 = x0/2.
-        ...     x0 >= 0.'''
-        >>> penalty_parser(constraints, nvars=3)
-        (('-(x[0] - (0.))',), ('x[2] - (x[0]/2.)',))
-
-Additional Inputs:
-    nvars -- number of variables. Includes variables not explicitly
-        given by the constraint equations (e.g. 'x2' in the example above).
-    variables -- desired variable name. Default is 'x'. A list of variable
+        constraints. Standard python syntax should be followed (the ``math``
+        and ``numpy`` modules are already imported).
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
-    """
+    nvars (int, default=None): number of variables. Includes variables not
+        explicitly stated in the constraints (e.g. ``x1`` in the example below).
+
+Examples:
+    >>> constraints = '''
+    ...     x2 = x0/2.
+    ...     x0 >= 0.'''
+    >>> penalty_parser(constraints, nvars=3)
+    (('-(x[0] - (0.))',), ('x[2] - (x[0]/2.)',))
+"""
    #from mystic.tools import src
    #ndim = len(get_variables(src(func), variables))
     if list_or_tuple_or_ndarray(variables):
         if nvars is not None: variables = variables[:nvars]
         constraints = replace_variables(constraints, variables)
         varname = '$'
         ndim = len(variables)
@@ -1029,34 +1022,32 @@
     return tuple(ineqconstraints), tuple(eqconstraints)
 
 
 def constraints_parser(constraints, variables='x', nvars=None):
     """parse symbolic constraints into a tuple of constraints solver equations.
 The left-hand side of each constraint must be simplified to support assignment.
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
         equation per line. Constraints can be equality and/or inequality
-        constraints. Standard python syntax should be followed (with the
-        math and numpy modules already imported).
-
-    For example:
-        >>> constraints = '''
-        ...     x2 = x0/2.
-        ...     x0 >= 0.'''
-        >>> constraints_parser(constraints, nvars=3)
-        ('x[2] = x[0]/2.', 'x[0] = max(0., x[0])')
-
-Additional Inputs:
-    nvars -- number of variables. Includes variables not explicitly
-        given by the constraint equations (e.g. 'x2' in the example above).
-    variables -- desired variable name. Default is 'x'. A list of variable
+        constraints. Standard python syntax should be followed (the ``math``
+        and ``numpy`` modules are already imported).
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
+    nvars (int, default=None): number of variables. Includes variables not
+        explicitly stated in the constraints (e.g. ``x1`` in the example below).
+
+Examples:
+    >>> constraints = '''
+    ...     x2 = x0/2.
+    ...     x0 >= 0.'''
+    >>> constraints_parser(constraints, nvars=3)
+    ('x[2] = x[0]/2.', 'x[0] = max(0., x[0])')
     """
    #from mystic.tools import src
    #ndim = len(get_variables(src(func), variables))
     if list_or_tuple_or_ndarray(variables):
         if nvars is not None: variables = variables[:nvars]
         constraints = replace_variables(constraints, variables)
         varname = '$'
@@ -1166,49 +1157,51 @@
 
     return tuple(reversed(parsed))
 
 
 def generate_conditions(constraints, variables='x', nvars=None, locals=None):
     """generate penalty condition functions from a set of constraint strings
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
         equation per line. Constraints can be equality and/or inequality
-        constraints. Standard python syntax should be followed (with the
-        math and numpy modules already imported).
-
-    NOTE: Alternately, constraints may be a tuple of strings of symbolic
-          constraints. Will return a tuple of penalty condition functions.
-
-    For example:
-        >>> constraints = '''
-        ...     x0**2 = 2.5*x3 - 5.0
-        ...     exp(x2/x0) >= 7.0'''
-        >>> ineqf,eqf = generate_conditions(constraints, nvars=4)
-        >>> print(ineqf[0].__doc__)
-        '-(exp(x[2]/x[0]) - (7.0))'
-        >>> ineqf[0]([1,0,1,0])
-        4.2817181715409554
-        >>> print(eqf[0].__doc__)
-        'x[0]**2 - (2.5*x[3] - 5.0)'
-        >>> eqf[0]([1,0,1,0])
-        6.0
-
-Additional Inputs:
-    nvars -- number of variables. Includes variables not explicitly
-        given by the constraint equations (e.g. 'x2' in the example above).
-    variables -- desired variable name. Default is 'x'. A list of variable
+        constraints. Standard python syntax should be followed (the ``math``
+        and ``numpy`` modules are already imported).
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
-    locals -- a dictionary of additional variables used in the symbolic
-        constraints equations, and their desired values.  Default is
-        {'tol': 1e-15, 'rel': 1e-15}, where 'tol' and 'rel' are the absolute
-        and relative difference from the extremal value in a given inequality.
-        For more details, see `mystic.math.tolerance`.
+    nvars (int, default=None): number of variables. Includes variables not
+        explicitly stated in the constraints (e.g. ``x1`` in the example below).
+    locals (dict, default=None): additional variables used in the symbolic
+        constraints equations, and their desired values. Default is
+        ``{'tol': 1e-15, 'rel': 1e-15}``, where ``'tol'`` and ``'rel'`` are
+        the absolute and relative difference from the extremal value in a
+        given inequality. For more details, see ``mystic.math.tolerance``.
+
+Notes:
+    Alternately, ``constraints`` may be a tuple of strings of symbolic
+    constraints. Will return a tuple of penalty condition functions.
+
+    By default, the top-level namespace of ``numpy`` and ``math`` are
+    imported into ``locals``.
+
+Examples:
+    >>> constraints = '''
+    ...     x0**2 = 2.5*x3 - 5.0
+    ...     exp(x2/x0) >= 7.0'''
+    >>> ineqf,eqf = generate_conditions(constraints, nvars=4)
+    >>> print(ineqf[0].__doc__)
+    '-(exp(x[2]/x[0]) - (7.0))'
+    >>> ineqf[0]([1,0,1,0])
+    4.2817181715409554
+    >>> print(eqf[0].__doc__)
+    'x[0]**2 - (2.5*x[3] - 5.0)'
+    >>> eqf[0]([1,0,1,0])
+    6.0
 """
     if not isinstance(constraints, str):
         return tuple(generate_conditions(constraint, variables, nvars, locals) for constraint in constraints)
 
     ineqconstraints, eqconstraints = penalty_parser(constraints, \
                                       variables=variables, nvars=nvars)
 
@@ -1218,14 +1211,15 @@
     locals['rel'] = rel = locals['rel'] if 'rel' in locals else 1e-15
     if tol < 0 or rel < 0:
         msg = 'math domain error'
         raise ValueError(msg)
     # default is globals with numpy and math imported
     globals = {}
     code = """from math import *; from numpy import *;"""
+    code += """from builtins import *;""" # don't overload builtins
     code += """from numpy import mean as average;""" # use np.mean not average
    #code += """from mystic.math.measures import spread, variance, mean;"""
     code += """from mystic.math import tolerance as _tol;"""
     code = compile(code, '<string>', 'exec')
     exec(code, globals)
     globals.update(locals) #XXX: allow this?
     
@@ -1253,50 +1247,52 @@
     return tuple(results['inequality']), tuple(results['equality'])
    #return results
 
 
 def generate_solvers(constraints, variables='x', nvars=None, locals=None):
     """generate constraints solver functions from a set of constraint strings
 
-Inputs:
-    constraints -- a string of symbolic constraints, with one constraint
+Args:
+    constraints (str): a string of symbolic constraints, with one constraint
         equation per line. Constraints can be equality and/or inequality
-        constraints. Standard python syntax should be followed (with the
-        math and numpy modules already imported). The left-hand side of
+        constraints. Standard python syntax should be followed (the ``math``
+        and ``numpy`` modules are already imported). The left-hand side of
         each equation must be simplified to support assignment.
-
-    NOTE: Alternately, constraints may be a tuple of strings of symbolic
-          constraints. Will return a tuple of constraint solver functions.
-
-    For example:
-        >>> constraints = '''
-        ...     x2 = x0/2.
-        ...     x0 >= 0.'''
-        >>> solv = generate_solvers(constraints, nvars=3)
-        >>> print(solv[0].__doc__)
-        'x[2] = x[0]/2.'
-        >>> solv[0]([1,2,3])
-        [1, 2, 0.5]
-        >>> print(solv[1].__doc__)
-        'x[0] = max(0., x[0])'
-        >>> solv[1]([-1,2,3])
-        [0.0, 2, 3]
-
-Additional Inputs:
-    nvars -- number of variables. Includes variables not explicitly
-        given by the constraint equations (e.g. 'x2' in the example above).
-    variables -- desired variable name. Default is 'x'. A list of variable
+    variables (str, default='x'): desired variable name. A list of variable
         name strings is also accepted for when desired variable names
         don't have the same base, and can include variables that are not
         found in the constraints equation string.
-    locals -- a dictionary of additional variables used in the symbolic
-        constraints equations, and their desired values.  Default is
-        {'tol': 1e-15, 'rel': 1e-15}, where 'tol' and 'rel' are the absolute
-        and relative difference from the extremal value in a given inequality.
-        For more details, see `mystic.math.tolerance`.
+    nvars (int, default=None): number of variables. Includes variables not
+        explicitly stated in the constraints (e.g. ``x1`` in the example below).
+    locals (dict, default=None): additional variables used in the symbolic
+        constraints equations, and their desired values. Default is
+        ``{'tol': 1e-15, 'rel': 1e-15}``, where ``'tol'`` and ``'rel'`` are
+        the absolute and relative difference from the extremal value in a
+        given inequality. For more details, see ``mystic.math.tolerance``.
+
+Notes:
+    Alternately, ``constraints`` may be a tuple of strings of symbolic
+    constraints. Will return a tuple of constraint solver functions.
+
+    By default, the top-level namespace of ``numpy`` and ``math`` are
+    imported into ``locals``.
+
+Examples:
+    >>> constraints = '''
+    ...     x2 = x0/2.
+    ...     x0 >= 0.'''
+    >>> solv = generate_solvers(constraints, nvars=3)
+    >>> print(solv[0].__doc__)
+    'x[2] = x[0]/2.'
+    >>> solv[0]([1,2,3])
+    [1, 2, 0.5]
+    >>> print(solv[1].__doc__)
+    'x[0] = max(0., x[0])'
+    >>> solv[1]([-1,2,3])
+    [0.0, 2, 3]
 """
     if not isinstance(constraints, str):
         return tuple(generate_solvers(constraint, variables, nvars, locals) for constraint in constraints)
 
     _constraints = constraints_parser(constraints, \
                                       variables=variables, nvars=nvars)
 
@@ -1306,14 +1302,15 @@
     locals['rel'] = rel = locals['rel'] if 'rel' in locals else 1e-15
     if tol < 0 or rel < 0:
         msg = 'math domain error'
         raise ValueError(msg)
     # default is globals with numpy and math imported
     globals = {}
     code = """from math import *; from numpy import *;"""
+    code += """from builtins import *;""" # don't overload builtins
     code += """from numpy import mean as average;""" # use np.mean not average
     code += """from mystic.math.measures import spread, variance, mean;"""
     code += """from mystic.math.measures import impose_spread, impose_mean;"""
     code += """from mystic.math.measures import impose_sum, impose_product;"""
     code += """from mystic.math.measures import impose_variance;"""
     code += """from mystic.math import tolerance as _tol;"""
     code = compile(code, '<string>', 'exec')
@@ -1444,15 +1441,15 @@
     Otherwise, apply the constraints concurrently using a constraints coupler.
 
 Warning:
     This constraint generator doesn't check for conflicts in conditions, but
     simply applies conditions in the given order. This constraint generator
     assumes that a single variable has been isolated on the left-hand side
     of each constraints equation, thus all constraints are of the form
-    "x_i = f(x)". This solver picks speed over robustness, and relies on
+    ``x_i = f(x)``. This solver picks speed over robustness, and relies on
     the user to formulate the constraints so that they do not conflict.
 
 Examples:
     >>> constraints = '''
     ...     x0 = cos(x1) + 2.
     ...     x1 = x2*2.'''
     >>> solv = generate_solvers(constraints)
```

### Comparing `mystic-0.4.0/mystic/termination.py` & `mystic-0.4.1/mystic/termination.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Copyright (c) 2010-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 Factories that provide termination conditions for a mystic.solver
 """
 
 import numpy
@@ -63,18 +63,19 @@
 
 Terminates when the given condition is satisfied."""
   def __new__(self, arg):
     """
 Takes a termination condition:
     arg    -- termination condition
 
-Usage:
+Example:
     >>> from mystic.termination import When, VTR
     >>> term = When( VTR() )
-    >>> term(solver)  # where solver is a mystic.solver instance"""
+    >>> term(solver)  # where solver is a mystic.solver instance
+    """
     if isinstance(arg, tuple) and len(arg) == 1: arg = arg[0] # for pickling
     #XXX: need better filter on inputs
     if getattr(arg, '__module__', None) != self.__module__:
       raise TypeError("'%s' object is not a condition" % arg.__class__.__name__)
     if not getattr(arg, '__len__', None): arg = [arg]
     return tuple.__new__(self, arg)
 
@@ -108,18 +109,19 @@
 
 Terminates when all given conditions are satisfied."""
   def __new__(self, *args):
     """
 Takes one or more termination conditions:
     args   -- tuple of termination conditions
 
-Usage:
+Example:
     >>> from mystic.termination import And, VTR, ChangeOverGeneration
     >>> term = And( VTR(), ChangeOverGeneration() )
-    >>> term(solver)  # where solver is a mystic.solver instance"""
+    >>> term(solver)  # where solver is a mystic.solver instance
+    """
     if isinstance(args, tuple) and len(args) == 1: args = args[0] # for pickling
     #XXX: need better filter on inputs
     if not getattr(args, '__len__', None): args = [args]
     #XXX: check if every arg in args has __module__ == self.__module__ ?
     return tuple.__new__(self, args)
 
   def __repr__(self):
@@ -131,18 +133,19 @@
 
 Terminates when any of the given conditions are satisfied."""
   def __new__(self, *args):
     """
 Takes one or more termination conditions:
     args   -- tuple of termination conditions
 
-Usage:
+Example:
     >>> from mystic.termination import Or, VTR, ChangeOverGeneration
     >>> term = Or( VTR(), ChangeOverGeneration() )
-    >>> term(solver)  # where solver is a mystic.solver instance"""
+    >>> term(solver)  # where solver is a mystic.solver instance
+    """
     if isinstance(args, tuple) and len(args) == 1: args = args[0] # for pickling
     #XXX: need better filter on inputs
     if not getattr(args, '__len__', None): args = [args]
     #XXX: check if every arg in args has __module__ == self.__module__ ?
     return tuple.__new__(self, args)
 
   def __call__(self, solver, info=False):
```

### Comparing `mystic-0.4.0/mystic/tests/__main__.py` & `mystic-0.4.1/mystic/tests/__main__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import glob
 import os
 import sys
 import subprocess as sp
```

### Comparing `mystic-0.4.0/mystic/tests/_log.py` & `mystic-0.4.1/mystic/tests/_log.py`

 * *Files identical despite different names*

### Comparing `mystic-0.4.0/mystic/tests/check_SOW.py` & `mystic-0.4.1/mystic/tests/check_SOW.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.munge import write_support_file, write_converge_file, write_raw_file
 ## FIXME: 'converge' and 'raw' files are virtually unused and unsupported
 
 def test0(monitor):
```

### Comparing `mystic-0.4.0/mystic/tests/test_1d2d_expect.py` & `mystic-0.4.1/mystic/tests/test_1d2d_expect.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.math.measures import *
 from mystic.math.discrete import *
 from mystic.math import almostEqual
 def f(x): return sum(x)/len(x)
```

### Comparing `mystic-0.4.0/mystic/tests/test_boundsconstrained.py` & `mystic-0.4.1/mystic/tests/test_boundsconstrained.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2021-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2021-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import numpy as np
 import mystic as my
 import mystic.symbolic as ms
 import mystic.constraints as mc
```

### Comparing `mystic-0.4.0/mystic/tests/test_cache.py` & `mystic-0.4.1/mystic/tests/test_cache.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import mystic.cache as mc
 import mystic.models as mm
 
 # basic interaction with an archive
```

### Comparing `mystic-0.4.0/mystic/tests/test_collapse.py` & `mystic-0.4.1/mystic/tests/test_collapse.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import mystic.collapse as ct
 import numpy as np
 import mystic as my
 m = my.monitors._load('_log.py')
```

### Comparing `mystic-0.4.0/mystic/tests/test_collapsed.py` & `mystic-0.4.1/mystic/tests/test_collapsed.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import mystic.collapse as ct
 import mystic.mask as ma
 import mystic as my
 m = my.monitors._load('_log.py')
```

### Comparing `mystic-0.4.0/mystic/tests/test_combined.py` & `mystic-0.4.1/mystic/tests/test_combined.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 '''
 combine several penalty conditions to build a single constraint solver,
 then show examples of using (and_, or_, not_) for penalties and constraints
 '''
```

### Comparing `mystic-0.4.0/mystic/tests/test_compound_termination.py` & `mystic-0.4.1/mystic/tests/test_compound_termination.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 """
 Tests of factories that enable verbose and compound termination conditions
 """
 disp = 0
```

### Comparing `mystic-0.4.0/mystic/tests/test_constraints.py` & `mystic-0.4.1/mystic/tests/test_constraints.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.constraints import *
 from mystic.penalty import quadratic_equality
 from mystic.coupler import inner
 from mystic.math import almostEqual
```

### Comparing `mystic-0.4.0/mystic/tests/test_converters.py` & `mystic-0.4.1/mystic/tests/test_converters.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 test _to_function and _to_objective in cost and gradient calculations
 """
 
 import numpy as np
```

### Comparing `mystic-0.4.0/mystic/tests/test_coupler.py` & `mystic-0.4.1/mystic/tests/test_coupler.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.coupler import *
 from mystic.math import almostEqual
 
 def test_outer():
```

### Comparing `mystic-0.4.0/mystic/tests/test_dirac_measure.py` & `mystic-0.4.1/mystic/tests/test_dirac_measure.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 # Adapted from seesaw2d.py in branches/UQ/math/examples2/ 
 # For usage example, see seesaw2d_inf_example.py .
 """
 TESTS for Dirac measure data objects.
```

### Comparing `mystic-0.4.0/mystic/tests/test_expectation.py` & `mystic-0.4.1/mystic/tests/test_expectation.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,49 +1,49 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """
 test imposing the expectation for a function f by optimization
 """
 debug = False
 
 from mystic.math import almostEqual
 from math import pi, cos, tanh
 import random
 
-def ballistic_limit(h,a):
+def ballistic_limit(h, a):
   """calculate ballistic limit
 
-  Inputs:
-    - h = thickness
-    - a = obliquity
+  Parameters:
+    h (float): thickness
+    a (float): obliquity
 
-  Outputs:
-    - v_bl = velocity (ballistic limit)
+  Returns:
+    velocity at the ballistic limit
 """
  #assumes h,a have been scaled:
  #h = x[0] * 25.4 * 1e-3
  #a = x[1] * pi/180.0
   Ho = 0.5794
   s = 1.4004
   n = 0.4482
   return Ho * ( h / cos(a)**n )**s
 
 def marc_surr(x):
   """calculate perforation area using a tanh-based model surrogate
 
-  Inputs:
-    - x = [thickness, obliquity, speed]
+  Parameters:
+    x (list[float]): an iterable of [thickness, obliquity, speed]
 
-  Outputs:
-    - A = perforation area
+  Returns:
+    perforation area
 """
 # h = thickness = [60,105]
 # a = obliquity = [0,30]
 # v = speed = [2.1,2.8]
   h = x[0] * 25.4 * 1e-3
   a = x[1] * pi/180.0
   v = x[2]
```

### Comparing `mystic-0.4.0/mystic/tests/test_impose.py` & `mystic-0.4.1/mystic/tests/test_impose.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.math.measures import *
 from mystic.math import almostEqual
 
 def test_impose_reweighted_mean():
```

### Comparing `mystic-0.4.0/mystic/tests/test_method_order.py` & `mystic-0.4.1/mystic/tests/test_method_order.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.models import rosen
 from mystic.solvers import *
 from mystic.termination import VTRChangeOverGeneration
 from mystic.monitors import VerboseMonitor, Monitor
```

### Comparing `mystic-0.4.0/mystic/tests/test_moments.py` & `mystic-0.4.1/mystic/tests/test_moments.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import mystic.math.measures as mo
 from numpy import nan, isnan
 x = [1,2,3,4,5]
 y = [1,2,3,4,5,6]
```

### Comparing `mystic-0.4.0/mystic/tests/test_normalize.py` & `mystic-0.4.1/mystic/tests/test_normalize.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import numpy as np
 import mystic.math.measures as mm
 x = np.arange(1., 5)
 y = np.array([-1., -2, 0, 3])
```

### Comparing `mystic-0.4.0/mystic/tests/test_samples.py` & `mystic-0.4.1/mystic/tests/test_samples.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 try:
   import multiprocess as mp
   p = mp.Pool()
   pmap = p.map
```

### Comparing `mystic-0.4.0/mystic/tests/test_samplestats.py` & `mystic-0.4.1/mystic/tests/test_samplestats.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import numpy as np
 from mystic.math.measures import _k
```

### Comparing `mystic-0.4.0/mystic/tests/test_solver_best_performance.py` & `mystic-0.4.1/mystic/tests/test_solver_best_performance.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """Test Mystic's performance on some benchmark problems, with Mystic's settings
 adjusted to achieve the best results.
 """
 from mystic.monitors import Monitor
 from mystic.math import almostEqual
```

### Comparing `mystic-0.4.0/mystic/tests/test_solver_compare.py` & `mystic-0.4.1/mystic/tests/test_solver_compare.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 try:
   from scipy.optimize import fmin, fmin_powell
   HAS_SCIPY = True
 except ImportError:
```

### Comparing `mystic-0.4.0/mystic/tests/test_solver_constraints.py` & `mystic-0.4.1/mystic/tests/test_solver_constraints.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.constraints import *
 from mystic.solvers import *
 from mystic.math import almostEqual
 from mystic.tools import random_seed
```

### Comparing `mystic-0.4.0/mystic/tests/test_solver_sanity.py` & `mystic-0.4.1/mystic/tests/test_solver_sanity.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """A sanity test suite for Mystic solvers."""
 # should report clock-time, # of iterations, and # of function evaluations
 
 import sys
 from io import StringIO
```

### Comparing `mystic-0.4.0/mystic/tests/test_solver_state.py` & `mystic-0.4.1/mystic/tests/test_solver_state.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.solvers import DifferentialEvolutionSolver
 from mystic.solvers import NelderMeadSimplexSolver, PowellDirectionalSolver
 from mystic.termination import VTR, ChangeOverGeneration, When, Or
 from mystic.models import rosen
```

### Comparing `mystic-0.4.0/mystic/tests/test_solver_suite.py` & `mystic-0.4.1/mystic/tests/test_solver_suite.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """A test suite for Mystic solvers.
 Note: VTR termination with default tolerance shouldn't work for functions 
 whose value at the minimum is negative!
 Also, the two differential evolution solvers are global, while the other solvers
 are local optimizers."""
```

### Comparing `mystic-0.4.0/mystic/tests/test_symbolic.py` & `mystic-0.4.1/mystic/tests/test_symbolic.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.symbolic import *
 from mystic.math import almostEqual
 from mystic.constraints import as_constraint
```

### Comparing `mystic-0.4.0/mystic/tests/test_symbolic_abs.py` & `mystic-0.4.1/mystic/tests/test_symbolic_abs.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import mystic.symbolic as ms
 
 
 if __name__ == '__main__':
```

### Comparing `mystic-0.4.0/mystic/tests/test_symbolic_basic.py` & `mystic-0.4.1/mystic/tests/test_symbolic_basic.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2010-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #
 # coded by Alta Fang, 2010
 """
 A few basic symbolic constraints tests, but in no way a comprehensive suite.
 """
 from numpy import asarray
```

### Comparing `mystic-0.4.0/mystic/tests/test_symbolic_solve.py` & `mystic-0.4.1/mystic/tests/test_symbolic_solve.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2019-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2019-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.symbolic import denominator, _solve_zeros, equals, simplify, flip
 from mystic import random_seed
 random_seed(123) #FIXME: should be commented out
```

### Comparing `mystic-0.4.0/mystic/tests/test_termination.py` & `mystic-0.4.1/mystic/tests/test_termination.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Alta Fang (altafang @caltech and alta @princeton)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 """test termination conditions. (defaults listed below)
 
 VTR(tolerance = 0.005)
 ChangeOverGeneration(tolerance = 1e-6, generations = 30)
 NormalizedChangeOverGeneration(tolerance = 1e-4, generations = 10)
```

### Comparing `mystic-0.4.0/mystic/tests/test_vectorize.py` & `mystic-0.4.1/mystic/tests/test_vectorize.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2020-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2020-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.constraints import *
 
 def _symbolic():
     import mystic.symbolic as ms
```

### Comparing `mystic-0.4.0/mystic/tools.py` & `mystic-0.4.1/mystic/tools.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Patrick Hung (patrickh @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 #
 # flatten was adapted from the python cookbook
 # wrap_function was adapted from numpy
 # wrap_bounds was adapted from park
 """
@@ -236,16 +236,24 @@
     return isinstance(x, (list, tuple))
 
 def list_or_tuple_or_ndarray(x): # set, ...?
     "True if x is a list, tuple, or a ndarray"
     import numpy
     return isinstance(x, (list, tuple, numpy.ndarray))
 
+def is_ndarray(x):
+    "True if x is a ndarray"
+    return hasattr(x, 'tolist')
+
+def is_zero_d_ndarray(x):
+    "True if x is a zero-dimensional ndarray"
+    return hasattr(x, 'tolist') and not x.shape
+
 def listify(x):
-    "recursivly convert all members of a sequence to a list"
+    "recursively convert all members of a sequence to a list"
     if not isiterable(x): return x
     if x is iter(x): return listify(list(x))
     try: # e.g. if array(1)
         if x.ndim == 0: return x.flatten()[0]
     except Exception: pass
     return [listify(i) for i in x]
 
@@ -253,15 +261,15 @@
     "flatten a sequence; returns a ndarray"
     import numpy
     return numpy.array(list(flatten(sequence, maxlev, list_or_tuple_or_ndarray, lev)))
 
 def flatten(sequence, maxlev=999, to_expand=list_or_tuple, lev=0):
     """flatten a sequence; returns original sequence type
 
-For example:
+Examples:
     >>> A = [1,2,3,[4,5,6],7,[8,[9]]]
     >>> 
     >>> # Flatten.
     >>> flatten(A)
     [1, 2, 3, 4, 5, 6, 7, 8, 9]
     >>> 
     >>> # Flatten only one level deep.
@@ -271,15 +279,14 @@
     >>> # Flatten twice. 
     >>> flatten(A,2)
     [1, 2, 3, 4, 5, 6, 7, 8, 9]
     >>> 
     >>> # Flatten zero levels deep (i.e. don't flatten).
     >>> flatten(A,0)
     [1, 2, 3, [4, 5, 6], 7, [8, [9]]]
-
     """
     for item in sequence:
         if lev < maxlev and to_expand(item):
             for subitem in flatten(item, maxlev, to_expand, lev+1):
                  yield subitem
         else:
             yield item
@@ -442,41 +449,42 @@
         return reduce(reducer_function, x)
     return _reduce
 
 
 def reduced(reducer=None, arraylike=False):
     """apply a reducer function to reduce output to a single value
 
-For example:
+Examples:
     >>> @reduced(lambda x,y: x)
     ... def first(x):
     ...   return x
     ... 
     >>> first([1,2,3])
     1
-    >>> 
+
     >>> @reduced(min)
     ... def minimum(x):
     ...   return x
     ... 
     >>> minimum([3,2,1])
     1
+
     >>> @reduced(lambda x,y: x+y)
     ... def add(x):
     ...   return x
     ... 
     >>> add([1,2,3])
     6
+
     >>> @reduced(sum, arraylike=True)
     ... def added(x):
     ...   return x
     ... 
     >>> added([1,2,3])
     6
-
     """
     if reducer is None:
         reducer = lambda x: x
         arraylike = True
     def dec(f):
         if arraylike:
             def func(*args, **kwds):
@@ -496,15 +504,15 @@
 
 def insert_missing(x, missing=None):
     """return a sequence with the 'missing' elements inserted
 
 missing should be a dictionary of positional index and a value (e.g. {0:1.0}),
 where keys must be integers, and values can be any object (typically a float).
 
-For example:
+Examples:
     >>> insert_missing([1,2,4], missing={0:10, 3:-1})
     [10, 1, 2, -1, 4]
     """
     import dill
     if missing is None: _mask = {}
     elif isinstance(missing, str): _mask = eval('{%s}' % missing)
     else: _mask = missing
@@ -540,22 +548,22 @@
 where keys must be integers, and values can be any object (typically a float).
 
 functions are expected to take a single argument, a n-dimensional list or array,
 where the mask will be applied to the input array.  Hence, instead of masking
 the inputs, the function is "masked".  Conceptually, f(mask(x)) ==> f'(x),
 instead of f(mask(x)) ==> f(x').
 
-For example:
+Examples:
     >>> @masked({0:10,3:-1})
     ... def same(x):
     ...     return x
     ...
     >>> same([1,2,3])
     [10, 1, 2, -1, 3]
-    >>> 
+
     >>> @masked({0:10,3:-1})
     ... def foo(x):
             w,x,y,z = x # requires a lenth-4 sequence
     ...     return w+x+y+z
     ...
     >>> foo([-5,2])     # produces [10,-5,2,-1]
     6
@@ -575,15 +583,15 @@
 
 mask should be a dictionary of the positional index and a value (e.g. {0:1.0}),
 where keys must be integers, and values can be any object (typically a float).
 
 functions are expected to take a single argument, a n-dimensional list or array,
 where the mask will be applied to the input array.
 
-For example:
+Examples:
     >>> @partial({0:10,3:-1})
     ... def same(x):
     ...     return x
     ...
     >>> same([-5,9])
     [10, 9]
     >>> same([0,1,2,3,4])
@@ -612,15 +620,15 @@
 
 functions are expected to take a single argument, a n-dimensional list or array,
 where the mask will be applied to the input array.
 
 operations within a single mask are unordered. If a specific ordering of
 operations is required, apply multiple masks in the desired order.
 
-For example:
+Examples:
     >>> @synchronized({0:1,3:-1})
     ... def same(x):
     ...     return x
     ...
     >>> same([-5,9])
     [9, 9]
     >>> same([0,1,2,3,4])
@@ -675,22 +683,22 @@
     x[mask] = 0.0
     return x.tolist()
 
 
 def suppressed(tol=1e-8, exit=False, clip=True):
     """generate a function, where values less than tol are suppressed
 
-For example:
+Examples:
     >>> @suppressed(1e-8)
     ... def square(x):
     ...     return [i**2 for i in x]
     ... 
     >>> square([1e-8, 2e-8, 1e-9])
     [1.00000000e-16, 4.00000000e-16, 0.00000000e+00]
-    >>> 
+
     >>> from mystic.math.measures import normalize
     >>> @suppressed(1e-8, exit=True, clip=False)
     ... def norm(x):
     ...     return normalize(x, mass=1)
     ... 
     >>> norm([1e-8, 2e-8, 1e-16, 5e-9])
     [0.28571428585034014, 0.5714285707482993, 0.0, 0.14285714340136055]
@@ -736,15 +744,15 @@
              return cfmult * CF(*args,**kwargs)
     return _
 
 
 def chain(*decorators):
     """chain together decorators into a single decorator
 
-For example:
+Examples:
     >>> wm = with_mean(5.0)
     >>> wv = with_variance(5.0)
     >>> 
     >>> @chain(wm, wv)  
     ... def doit(x):
     ...     return x
     ... 
@@ -758,17 +766,18 @@
         return f
     return dec
 
 
 def connected(pairs):
     """generate dict of connected members of a set of tuples (pairs)
 
-For example:
+Examples:
     >>> connected({(0,3),(4,2),(3,1),(4,5),(2,6)})
     {0: set([1, 3]), 4: set([2, 5, 6])}
+
     >>> connected({(0,3),(3,1),(4,5),(2,6)})
     {0: set([1, 3]), 2: set([6]), 4: set([5])}}
 """
     collapse = {}
     #XXX: any vectorized way to do this?
     for i,j in pairs: #XXX: sorted(sorted(pair) for pair in pairs): # ordering?
         found = False
@@ -781,15 +790,15 @@
             collapse[i] = set((j,))
     return collapse
 
 
 def unpair(pairs):
     '''convert a 1D array of N pairs to two 1D arrays of N values
 
-For example:
+Examples:
     >>> unpair([(a0,b0),(a1,b1),(a2,b2)])
     [a0,a1,a2],[b0,b1,b2]
     '''
     from numpy import asarray
     pairsT = asarray(pairs).transpose()
     return [i.tolist() for i in pairsT]
```

### Comparing `mystic-0.4.0/mystic.egg-info/PKG-INFO` & `mystic-0.4.1/mystic.egg-info/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: mystic
-Version: 0.4.0
-Summary: highly-constrained non-convex optimization and uncertainty quantification
+Version: 0.4.1
+Summary: constrained nonlinear optimization for scientific machine learning, UQ, and AI
 Home-page: https://github.com/uqfoundation/mystic
 Download-URL: https://pypi.org/project/mystic/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
 License: BSD-3-Clause
@@ -20,27 +20,28 @@
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Software Development
 Requires-Python: >=3.7
 Provides-Extra: math
 Provides-Extra: parallel
 Provides-Extra: plotting
 License-File: LICENSE
 
----------------------------------------------------------------------------------
-mystic: highly-constrained non-convex optimization and uncertainty quantification
----------------------------------------------------------------------------------
+--------------------------------------------------------------------------------------
+mystic: constrained nonlinear optimization for scientific machine learning, UQ, and AI
+--------------------------------------------------------------------------------------
 
 About Mystic
 ============
 
 The ``mystic`` framework provides a collection of optimization algorithms
 and tools that allows the user to more robustly (and easily) solve hard
 optimization problems. All optimization algorithms included in ``mystic``
@@ -59,23 +60,40 @@
 be easily swapped without the user having to write any new code. ``mystic``
 solvers all conform to a solver API, thus also have common method calls
 to configure and launch an optimization job. For more details, see
 ``mystic.abstract_solver``. The API also makes it easy to bind a favorite
 3rd party solver into the ``mystic`` framework.
 
 Optimization algorithms in ``mystic`` can accept parameter constraints,
-either in the form of penaties (which "penalize" regions of solution
-space that violate the constraints), or as constraints (which "constrain" 
-the solver to only search in regions of solution space where the
-constraints are respected), or both. ``mystic`` provides a large 
-selection of constraints, including probabistic and dimensionally
+as "soft constraints" (i.e. ``penalties``, which "penalize" regions of
+solution space that violate the constraints), or as "hard constraints"
+(i.e. ``constraints``, which constrain the solver to only search in regions
+of space where the constraints are respected), or both. ``mystic`` provides
+a large selection of constraints, including probabistic and dimensionally
 reducing constraints. By providing a robust interface designed to
 enable the user to easily configure and control solvers, ``mystic``
 greatly reduces the barrier to solving hard optimization problems.
 
+Sampling, interpolation, and statistics in ``mystic`` are all designed
+to seamlessly couple with constrained optimization to facilitate
+scientific machine learning, uncertainty quantification, adaptive
+sampling, nonlinear interpolation, and artificial intelligence.
+``mystic`` can convert systems of equalities and inequalities to
+hard or soft constraints using methods in ``mystic.symbolic``.
+With ``mystic.constraints.vectorize``, constraints can be converted
+to kernel transforms for use in machine learning. Similarly, ``mystic``
+provides tools for accurately producing emulators on an irregular grid
+using ``mystic.math.interpolate``, which includes methods for solving
+for gradients and Hessians. ``mystic.samplers`` use optimizers to
+drive adaptive sampling toward the first and second order critical points
+of the response surface, yielding highly-informative training data sets
+and ensuring emulator accuracy. ``mystic.math.discrete`` defines
+constrained discrete probability measures, which can be used in
+constrained statistical optimization and learning.
+
 ``mystic`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/mystic/issues, with a legacy list maintained at https://uqfoundation.github.io/project/mystic/query.
 
 
 Major Features
 ==============
 
@@ -120,15 +138,15 @@
 Installation
 ============
 
 ``mystic`` can be installed with ``pip``::
 
     $ pip install mystic
 
-To include optional scientific python support, with ``scipy``, install::
+To include optional scientific Python support, with ``scipy``, install::
 
     $ pip install mystic[math]
 
 To include optional plotting support with ``matplotlib``, install::
 
     $ pip install mystic[plotting]
 
@@ -144,91 +162,90 @@
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
     - ``cython``, **>=0.29.30**
     - ``numpy``, **>=1.0**
     - ``sympy``, **>=0.6.7**
     - ``mpmath``, **>=0.19**
-    - ``dill``, **>=0.3.6**
-    - ``klepto``, **>=0.2.3**
+    - ``dill``, **>=0.3.7**
+    - ``klepto``, **>=0.2.4**
 
 Optional requirements:
 
     - ``matplotlib``, **>=0.91**
     - ``scipy``, **>=0.6.0**
-    - ``pathos``, **>=0.3.0**
-    - ``pyina``, **>=0.2.6**
+    - ``pathos``, **>=0.3.1**
+    - ``pyina``, **>=0.2.8**
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://mystic.rtfd.io. Also see ``mystic.tests`` for a set of scripts that
 demonstrate several of the many features of the ``mystic`` framework.
 You can run the test suite with ``python -m mystic.tests``. There are
 several plotting scripts that are installed with ``mystic``, primary of which
 are ``mystic_log_reader`` (also available with ``python -m mystic``) and the
 ``mystic_model_plotter`` (also available with ``python -m mystic.models``).
 There are several other plotting scripts that come with ``mystic``, and they
-are detailed elsewhere in the documentation.  See ``mystic.examples`` for
-examples that demonstrate the basic use cases for configuration and launching
-of optimization jobs using one of the sample models provided in
-``mystic.models``. Many of the included examples are standard optimization
-test problems. The use of constraints and penalties are detailed in
-``mystic.examples2``, while more advanced features leveraging ensemble solvers
-and dimensional collapse are found in ``mystic.examples3``. The scripts in
-``mystic.examples4`` demonstrate leveraging ``pathos`` for parallel computing,
-as well as demonstrate some auto-partitioning schemes. ``mystic`` has the
-ability to work in product measure space, and the scripts in
-``mystic.examples5`` show to work with product measures.  The source code is
-generally well documented, so further questions may be resolved by inspecting
-the code itself.  Please feel free to submit a ticket on github, or ask a
-question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``mystic`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+are detailed elsewhere in the documentation.  See https://github.com/uqfoundation/mystic/tree/master/examples for examples that demonstrate the basic use
+cases for configuration and launching of optimization jobs using one of the
+sample models provided in ``mystic.models``. Many of the included examples
+are standard optimization test problems. The use of constraints and penalties
+are detailed in https://github.com/uqfoundation/mystic/tree/master/examples2 while more advanced features leveraging ensemble solvers, machine learning,
+uncertainty quantification, and dimensional collapse are found in https://github.com/uqfoundation/mystic/tree/master/examples3. The scripts in https://github.com/uqfoundation/mystic/tree/master/examples4 demonstrate leveraging ``pathos``
+for parallel computing, as well as demonstrate some auto-partitioning schemes.
+``mystic`` has the ability to work in product measure space, and the scripts in
+https://github.com/uqfoundation/mystic/tree/master/examples5 show how to work
+with product measures at a low level. The source code is generally well
+documented, so further questions may be resolved by inspecting the code itself.
+Please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``mystic`` in your work, please send an email (to **mmckerns at uqfoundation
+dot org**).
 
 Instructions on building a new model are in ``mystic.models.abstract_model``.
 ``mystic`` provides base classes for two types of models:
 
     - ``AbstractFunction``   [evaluates ``f(x)`` for given evaluation points ``x``]
     - ``AbstractModel``      [generates ``f(x,p)`` for given coefficients ``p``]
 
 ``mystic`` also provides some convienence functions to help you build a
 model instance and a cost function instance on-the-fly. For more
 information, see ``mystic.forward_model``.  It is, however, not necessary
 to use base classes or the model builder in building your own model or
-cost function, as any standard python function can be used as long as it
+cost function, as any standard Python function can be used as long as it
 meets the basic ``AbstractFunction`` interface of ``cost = f(x)``.
 
 All ``mystic`` solvers are highly configurable, and provide a robust set of
 methods to help customize the solver for your particular optimization
 problem. For each solver, a minimal (``scipy.optimize``) interface is also
 provided for users who prefer to configure and launch their solvers as a
 single function call. For more information, see ``mystic.abstract_solver``
 for the solver API, and each of the individual solvers for their minimal
 functional interface.
 
 ``mystic`` enables solvers to use parallel computing whenever the user provides
-a replacement for the (serial) python ``map`` function.  ``mystic`` includes a
+a replacement for the (serial) Python ``map`` function.  ``mystic`` includes a
 sample ``map`` in ``mystic.python_map`` that mirrors the behavior of the
-built-in python ``map``, and a ``pool`` in ``mystic.pools`` that provides ``map``
+built-in Python ``map``, and a ``pool`` in ``mystic.pools`` that provides ``map``
 functions using the ``pathos`` (i.e. ``multiprocessing``) interface. ``mystic``
 solvers are designed to utilize distributed and parallel tools provided by
 the ``pathos`` package. For more information, see ``mystic.abstract_map_solver``,
 ``mystic.abstract_ensemble_solver``, and the ``pathos`` documentation at
 http://pathos.rtfd.io.
 
 Important classes and functions are found here:
 
     - ``mystic.solvers``                  [solver optimization algorithms]
     - ``mystic.termination``              [solver termination conditions]
     - ``mystic.strategy``                 [solver population mutation strategies]
     - ``mystic.monitors``                 [optimization monitors]
-    - ``mystic.symbolic``                 [symbolic math in constaints]
+    - ``mystic.symbolic``                 [symbolic math in constraints]
     - ``mystic.constraints``              [constraints functions]
     - ``mystic.penalty``                  [penalty functions]
     - ``mystic.collapse``                 [checks for dimensional collapse]
     - ``mystic.coupler``                  [decorators for function coupling]
     - ``mystic.pools``                    [parallel worker pool interface]
     - ``mystic.munge``                    [file readers and writers]
     - ``mystic.scripts``                  [model and convergence plotting]
@@ -264,14 +281,15 @@
     - ``mystic.models.abstract_model``    [the model API definition]
 
 ``mystic`` also provides several convience scripts that are used to visualize
 models, convergence, and support on the hypercube. These scripts are installed
 to a directory on the user's ``$PATH``, and thus can be run from anywhere:
 
     - ``mystic_log_reader``               [parameter and cost convergence]
+    - ``mystic_log_converter``            [logfile format converter]
     - ``mystic_collapse_plotter``         [convergence and dimensional collapse]
     - ``mystic_model_plotter``            [model surfaces and solver trajectory]
     - ``support_convergence``             [convergence plots for measures]
     - ``support_hypercube``               [parameter support on the hypercube]
     - ``support_hypercube_measures``      [measure support on the hypercube]
     - ``support_hypercube_scenario``      [scenario support on the hypercube]
```

### Comparing `mystic-0.4.0/mystic.egg-info/SOURCES.txt` & `mystic-0.4.1/mystic.egg-info/SOURCES.txt`

 * *Files 6% similar despite different names*

```diff
@@ -17,14 +17,15 @@
 docs/source/conf.py
 docs/source/index.rst
 docs/source/math.rst
 docs/source/models.rst
 docs/source/mystic.rst
 docs/source/mystic2.png
 docs/source/scripts.rst
+docs/source/_static/css/custom.css
 examples/NOTES
 examples/README
 examples/TEST_ffitPP.py
 examples/TEST_ffitPP2.py
 examples/TEST_ffitPP2_b.py
 examples/TEST_ffitPP_b.py
 examples/buckshot_example06.py
@@ -167,18 +168,23 @@
 examples2/vessel_alt.py
 examples3/README
 examples3/collapse_bounds.py
 examples3/collapse_measures.py
 examples3/collapse_solver.py
 examples3/constrained_sklearn.py
 examples3/dataset.py
+examples3/emulators.py
 examples3/estimator.py
 examples3/hyperopt_sklearn.py
 examples3/interpolator.py
 examples3/misc.py
+examples3/misc3.py
+examples3/misc3b.py
+examples3/misc4.py
+examples3/misc6.py
 examples3/ml.py
 examples3/noisy.py
 examples3/ouq.py
 examples3/ouq_.py
 examples3/ouq_models.py
 examples3/plotter.py
 examples3/sampler_pandas.py
@@ -187,15 +193,17 @@
 examples3/surface.py
 examples3/surrogate.py
 examples3/test_3D_ub_c0mean.py
 examples3/test_3D_ub_mean.py
 examples3/test_3D_ub_pof.py
 examples3/test_5D_ub_c0mean.py
 examples3/test_5D_ub_mean.py
+examples3/test_cache.py
 examples3/test_error.py
+examples3/test_expect.py
 examples3/test_expected.py
 examples3/test_expected_error1.py
 examples3/test_expected_error1GP.py
 examples3/test_expected_error1ML.py
 examples3/test_expected_error2.py
 examples3/test_expected_error2GP.py
 examples3/test_expected_error2ML.py
@@ -221,14 +229,25 @@
 examples3/test_sparsity.py
 examples3/test_surface.py
 examples3/test_svc1.py
 examples3/test_svc2.py
 examples3/test_svr1.py
 examples3/test_svr2.py
 examples3/toys.py
+examples3/xrd_design3.py
+examples3/xrd_design3b.py
+examples3/xrd_design4.py
+examples3/xrd_design6.py
+examples3/xrd_opt3.py
+examples3/xrd_opt4.py
+examples3/xrd_opt6.py
+examples3/xrd_optML3.py
+examples3/xrd_optML4.py
+examples3/xrd_plot_db.py
+examples3/xrd_size_db.py
 examples3/DATA/g1.pts
 examples3/DATA/g2.pts
 examples4/MM2_surrogate_diam_batchgrid.py
 examples4/MM_surrogate_diam.py
 examples4/MPI2_surrogate_diam_batchgrid.py
 examples4/MPI_surrogate_diam.py
 examples4/MPI_surrogate_diam_batchgrid.py
@@ -377,13 +396,14 @@
 mystic/tests/test_symbolic.py
 mystic/tests/test_symbolic_abs.py
 mystic/tests/test_symbolic_basic.py
 mystic/tests/test_symbolic_solve.py
 mystic/tests/test_termination.py
 mystic/tests/test_vectorize.py
 scripts/mystic_collapse_plotter
+scripts/mystic_log_converter
 scripts/mystic_log_reader
 scripts/mystic_model_plotter
 scripts/support_convergence
 scripts/support_hypercube
 scripts/support_hypercube_measures
 scripts/support_hypercube_scenario
```

### Comparing `mystic-0.4.0/scripts/mystic_model_plotter` & `mystic-0.4.1/scripts/mystic_model_plotter`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Jean-Christophe Fillion-Robin (jchris.fillionr @kitware.com)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic import model_plotter
 
 __doc__ = model_plotter.__doc__
```

### Comparing `mystic-0.4.0/scripts/support_hypercube_measures` & `mystic-0.4.1/scripts/support_hypercube_measures`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.support import hypercube_measures
 
 __doc__ = hypercube_measures.__doc__
```

### Comparing `mystic-0.4.0/scripts/support_hypercube_scenario` & `mystic-0.4.1/scripts/support_hypercube_scenario`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 from mystic.support import hypercube_scenario
 
 __doc__ = hypercube_scenario.__doc__
```

### Comparing `mystic-0.4.0/setup.py` & `mystic-0.4.1/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
 import os
 import sys
 # drop support for older python
 if sys.version_info < (3, 7):
@@ -36,15 +36,15 @@
     Distribution = object
     has_setuptools = False
 
 # build the 'setup' call
 setup_kwds = dict(
     name='mystic',
     version=__version__,
-    description='highly-constrained non-convex optimization and uncertainty quantification',
+    description='constrained nonlinear optimization for scientific machine learning, UQ, and AI',
     long_description = README.strip(),
     author = __author__,
     author_email = AUTHOR_EMAIL,
     maintainer = __author__,
     maintainer_email = AUTHOR_EMAIL,
     license = 'BSD-3-Clause',
     platforms = ['Linux', 'Windows', 'Mac'],
@@ -62,25 +62,27 @@
         'Intended Audience :: Science/Research',
         'License :: OSI Approved :: BSD License',
         'Programming Language :: Python :: 3',
         'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3.10',
+        'Programming Language :: Python :: 3.11',
         'Programming Language :: Python :: Implementation :: CPython',
         'Programming Language :: Python :: Implementation :: PyPy',
         'Topic :: Scientific/Engineering',
         'Topic :: Software Development',
     ],
     packages = ['mystic','mystic.models','mystic.math','mystic.cache',
                 'mystic.tests'],
     package_dir = {'mystic':'mystic','mystic.models':'mystic/models',
                    'mystic.math':'mystic/math','mystic.cache':'mystic/cache',
                    'mystic.tests':'mystic/tests'},
     scripts=['scripts/mystic_log_reader',
+             'scripts/mystic_log_converter',
              'scripts/mystic_model_plotter',
              'scripts/mystic_collapse_plotter',
              'scripts/support_convergence',
              'scripts/support_hypercube',
              'scripts/support_hypercube_measures',
              'scripts/support_hypercube_scenario'],
 )
@@ -88,18 +90,18 @@
 # force python-, abi-, and platform-specific naming of bdist_wheel
 class BinaryDistribution(Distribution):
     """Distribution which forces a binary package with platform name"""
     def has_ext_modules(foo):
         return True
 
 # define dependencies
-dill_version = 'dill>=0.3.6'
-klepto_version = 'klepto>=0.2.3'
-pathos_version = 'pathos>=0.3.0'
-pyina_version = 'pyina>=0.2.6'
+dill_version = 'dill>=0.3.7'
+klepto_version = 'klepto>=0.2.4'
+pathos_version = 'pathos>=0.3.1'
+pyina_version = 'pyina>=0.2.8'
 cython_version = 'cython>=0.29.30' #XXX: required to build numpy from source
 numpy_version = 'numpy>=1.0'
 sympy_version = 'sympy>=0.6.7'#, <0.7.4'
 scipy_version = 'scipy>=0.6.0'
 mpmath_version = 'mpmath>=0.19'
 matplotlib_version = 'matplotlib>=0.91' #XXX: kiwisolver-1.3.0
 # add dependencies
```

### Comparing `mystic-0.4.0/tox.ini` & `mystic-0.4.1/tox.ini`

 * *Files 13% similar despite different names*

```diff
@@ -2,30 +2,36 @@
 skip_missing_interpreters=
     True
 envlist =
     py37-numpy12-sympy11
     py38-numpy12-sympy11
     py39-numpy12-sympy11
     py310-numpy12-sympy11
+    py311-numpy12-sympy11
+    py312-numpy12-sympy11
     pypy37-numpy12-sympy11
     pypy38-numpy12-sympy11
     pypy39-numpy12-sympy11
+    pypy310-numpy12-sympy11
 
 [testenv]
 setenv =
     PYTHONHASHSEED = 0
     recreate = True
 basepython = 
     py37: python3.7
     py38: python3.8
     py39: python3.9
     py310: python3.10
+    py311: python3.11
+    py312: python3.12
     pypy37: pypy37
     pypy38: pypy38
     pypy39: pypy39
+    pypy310: pypy310
 deps =
 #   scipy
     numpy12: numpy>=1.0
     sympy11: sympy>=0.6.7
     dill
     klepto
 whitelist_externals =
```

### Comparing `mystic-0.4.0/version.py` & `mystic-0.4.1/version.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/mystic/blob/master/LICENSE
 
-__version__ = '0.4.0'
+__version__ = '0.4.1'
 __author__ = 'Mike McKerns'
 __contact__ = 'mmckerns@uqfoundation.org'
 
 
 def get_license_text(filepath):
     "open the LICENSE file and read the contents"
     try:
@@ -34,14 +34,21 @@
                 continue
             elif skip and line.startswith('    http'):
                 README += '\n' + line
             elif line.startswith('* '):
                 README += line.replace('* ','    - ',1)
             elif line.startswith('-'):
                 README += line.replace('-','=') + '\n'
+            elif line.startswith('!['): # image
+                alt,img = line.split('](',1)
+                if img.startswith('docs'): # relative path
+                    img = img.split('docs/source/',1)[-1] # make is in docs
+                README += '.. image:: ' + img.replace(')','')
+                README += '   :alt: ' + alt.replace('![','') + '\n'
+            #elif ')[http' in line: # alt text link (`text <http://url>`_)
             else:
                 README += line
                 skip = line.endswith(':\n')
         fh.close()
     except:
         README = ''
     return README
@@ -57,15 +64,15 @@
         license: the module's license contents
     """
     import os
     infofile = os.path.join(dirpath, '%s/__info__.py' % modulename)
     header = '''#!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/%s/blob/master/LICENSE
 ''' % modulename #XXX: author and email are hardwired in the header
     doc = info.get('doc', None)
     version = info.get('version', None)
     author = info.get('author', None)
     license = info.get('license', None)
```

