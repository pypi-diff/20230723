# Comparing `tmp/pathos-0.3.0.tar.gz` & `tmp/pathos-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pathos-0.3.0.tar", last modified: Mon Oct 24 02:47:03 2022, max compression
+gzip compressed data, was "pathos-0.3.1.tar", last modified: Sun Jul 23 11:15:56 2023, max compression
```

## Comparing `pathos-0.3.0.tar` & `pathos-0.3.1.tar`

### file list

```diff
@@ -1,124 +1,128 @@
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:03.066861 pathos-0.3.0/
--rw-r--r--   0 mmckerns   (501) staff       (20)      832 2022-05-16 23:08:58.000000 pathos-0.3.0/.codecov.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)      983 2022-05-16 23:08:58.000000 pathos-0.3.0/.coveragerc
--rw-r--r--   0 mmckerns   (501) staff       (20)       32 2016-12-29 21:27:25.000000 pathos-0.3.0/.gitignore
--rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-05-16 23:08:58.000000 pathos-0.3.0/.readthedocs.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1426 2022-07-02 19:22:02.000000 pathos-0.3.0/.travis.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2022-01-01 16:36:06.000000 pathos-0.3.0/LICENSE
--rw-r--r--   0 mmckerns   (501) staff       (20)      305 2022-07-06 23:18:45.000000 pathos-0.3.0/MANIFEST.in
--rw-r--r--   0 mmckerns   (501) staff       (20)    11250 2022-10-24 02:47:03.067331 pathos-0.3.0/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)    10685 2022-10-24 02:42:35.000000 pathos-0.3.0/README.md
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:02.948556 pathos-0.3.0/applications/
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      705 2022-01-01 16:36:06.000000 pathos-0.3.0/applications/install-pp-1.6.4.2.sh
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      821 2022-01-01 16:36:06.000000 pathos-0.3.0/applications/install-rpyc-3.0.6.sh
--rw-r--r--   0 mmckerns   (501) staff       (20)     4936 2022-01-01 16:36:06.000000 pathos-0.3.0/applications/install_pathos_server.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:02.950600 pathos-0.3.0/docs/
--rw-r--r--   0 mmckerns   (501) staff       (20)      670 2022-05-16 23:08:58.000000 pathos-0.3.0/docs/Makefile
--rw-r--r--   0 mmckerns   (501) staff       (20)      430 2022-05-17 16:07:14.000000 pathos-0.3.0/docs/requirements.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:02.961044 pathos-0.3.0/docs/source/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7529 2022-07-06 23:19:26.000000 pathos-0.3.0/docs/source/conf.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      519 2017-08-23 20:58:27.000000 pathos-0.3.0/docs/source/helpers.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      347 2017-08-23 20:58:27.000000 pathos-0.3.0/docs/source/index.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2017-08-11 19:08:40.000000 pathos-0.3.0/docs/source/pathos.png
--rw-r--r--   0 mmckerns   (501) staff       (20)     4870 2022-09-05 00:00:17.000000 pathos-0.3.0/docs/source/pathos.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      230 2018-05-26 16:11:29.000000 pathos-0.3.0/docs/source/scripts.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      723 2017-08-23 20:58:27.000000 pathos-0.3.0/docs/source/secure.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      284 2017-08-23 20:58:27.000000 pathos-0.3.0/docs/source/xmlrpc.rst
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:02.989899 pathos-0.3.0/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)       88 2016-07-17 18:39:38.000000 pathos-0.3.0/examples/README
--rw-r--r--   0 mmckerns   (501) staff       (20)     2210 2022-06-29 14:26:21.000000 pathos-0.3.0/examples/async_map.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1772 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/mp_class_example.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      993 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/nested.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2668 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/pp_map.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1936 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/secure_copy.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1150 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/secure_hello.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      871 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/simple_tunnel.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      919 2022-06-29 11:23:04.000000 pathos-0.3.0/examples/spawn.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3277 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/sum_primesX.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      937 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/test_mpmap.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1062 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/test_mpmap2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1416 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/test_mpmap3.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1556 2022-06-29 10:56:25.000000 pathos-0.3.0/examples/test_mpmap_dill.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      835 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/test_ppmap.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      806 2022-01-01 16:36:06.000000 pathos-0.3.0/examples/test_ppmap2.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2232 2022-06-29 14:42:36.000000 pathos-0.3.0/examples/test_profile.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1251 2022-06-29 14:47:47.000000 pathos-0.3.0/examples/xmlrpc_server.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:03.006441 pathos-0.3.0/examples2/
--rw-r--r--   0 mmckerns   (501) staff       (20)     1124 2016-07-17 18:39:38.000000 pathos-0.3.0/examples2/README
--rw-r--r--   0 mmckerns   (501) staff       (20)     2235 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/all_scatter_gather.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2361 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/all_scatter_gather2.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      783 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/dejong.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2000 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/optimize.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1889 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/optimize0.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2201 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/optimize_cheby_diffev_map.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2201 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/optimize_cheby_powell_map.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2198 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/optimize_cheby_powell_mpimap.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2314 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/optimize_cheby_powell_mpmap.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2215 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/optimize_cheby_powell_ppmap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2072 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/optimize_helper.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2605 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/optimize_powell.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2167 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/optimize_rosen_powell_map.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1811 2022-01-01 16:36:06.000000 pathos-0.3.0/examples2/poly.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1435 2022-06-29 11:23:15.000000 pathos-0.3.0/examples2/scatter_gather.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:03.046104 pathos-0.3.0/pathos/
--rw-r--r--   0 mmckerns   (501) staff       (20)    12062 2022-10-24 02:47:02.000000 pathos-0.3.0/pathos/__info__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2484 2022-09-04 23:47:50.000000 pathos-0.3.0/pathos/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5962 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      530 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/_ppserver_config.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10140 2022-06-29 14:31:47.000000 pathos-0.3.0/pathos/abstract_launcher.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6763 2022-06-29 11:00:11.000000 pathos-0.3.0/pathos/connection.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11163 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/core.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:03.052084 pathos-0.3.0/pathos/helpers/
--rw-r--r--   0 mmckerns   (501) staff       (20)     1000 2022-06-29 17:20:02.000000 pathos-0.3.0/pathos/helpers/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2665 2022-06-29 17:22:48.000000 pathos-0.3.0/pathos/helpers/mp_helper.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8283 2022-06-29 17:17:55.000000 pathos-0.3.0/pathos/helpers/pp_helper.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1332 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/hosts.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    21343 2022-09-08 00:08:33.000000 pathos-0.3.0/pathos/maps.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2973 2022-09-04 23:44:45.000000 pathos-0.3.0/pathos/mp_map.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8534 2022-06-29 11:19:01.000000 pathos-0.3.0/pathos/multiprocessing.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    17289 2022-06-29 14:52:47.000000 pathos-0.3.0/pathos/parallel.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1258 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/pools.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1948 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/portpicker.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      691 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/pp.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     7647 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/pp_map.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    14136 2022-06-29 14:40:07.000000 pathos-0.3.0/pathos/profile.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      646 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/python.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:03.055487 pathos-0.3.0/pathos/secure/
--rw-r--r--   0 mmckerns   (501) staff       (20)      101 2018-04-17 17:38:40.000000 pathos-0.3.0/pathos/secure/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4369 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/secure/connection.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4194 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/secure/copier.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5139 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/secure/tunnel.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6002 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/selector.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4831 2022-06-29 11:16:40.000000 pathos-0.3.0/pathos/serial.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1987 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/server.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:03.062747 pathos-0.3.0/pathos/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)      507 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      901 2022-07-09 11:09:02.000000 pathos-0.3.0/pathos/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1897 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/tests/test_decorate.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7060 2022-06-29 11:13:13.000000 pathos-0.3.0/pathos/tests/test_join.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2170 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/tests/test_map.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1815 2022-09-05 02:18:29.000000 pathos-0.3.0/pathos/tests/test_maps.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1152 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/tests/test_mp.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1041 2022-01-01 16:36:06.000000 pathos-0.3.0/pathos/tests/test_pp.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4908 2022-06-29 17:26:00.000000 pathos-0.3.0/pathos/tests/test_star.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1754 2022-06-29 14:40:59.000000 pathos-0.3.0/pathos/tests/test_with.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8344 2022-06-29 14:40:47.000000 pathos-0.3.0/pathos/threading.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2369 2022-06-29 14:48:40.000000 pathos-0.3.0/pathos/util.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:03.064188 pathos-0.3.0/pathos/xmlrpc/
--rw-r--r--   0 mmckerns   (501) staff       (20)       55 2018-04-17 17:38:40.000000 pathos-0.3.0/pathos/xmlrpc/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8547 2022-06-29 14:51:29.000000 pathos-0.3.0/pathos/xmlrpc/server.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:03.050140 pathos-0.3.0/pathos.egg-info/
--rw-r--r--   0 mmckerns   (501) staff       (20)    11250 2022-10-24 02:47:02.000000 pathos-0.3.0/pathos.egg-info/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     2527 2022-10-24 02:47:02.000000 pathos-0.3.0/pathos.egg-info/SOURCES.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-24 02:47:02.000000 pathos-0.3.0/pathos.egg-info/dependency_links.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-24 02:47:02.000000 pathos-0.3.0/pathos.egg-info/not-zip-safe
--rw-r--r--   0 mmckerns   (501) staff       (20)       59 2022-10-24 02:47:02.000000 pathos-0.3.0/pathos.egg-info/requires.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        7 2022-10-24 02:47:02.000000 pathos-0.3.0/pathos.egg-info/top_level.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)      166 2022-05-20 09:49:04.000000 pathos-0.3.0/pyproject.toml
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 02:47:03.065698 pathos-0.3.0/scripts/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5962 2022-01-01 16:36:06.000000 pathos-0.3.0/scripts/pathos_connect
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      427 2022-01-01 16:36:06.000000 pathos-0.3.0/scripts/portpicker
--rw-r--r--   0 mmckerns   (501) staff       (20)       62 2022-10-24 02:47:03.068505 pathos-0.3.0/setup.cfg
--rw-r--r--   0 mmckerns   (501) staff       (20)     4732 2022-10-24 02:43:02.000000 pathos-0.3.0/setup.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      276 2022-07-09 11:08:42.000000 pathos-0.3.0/tox.ini
--rw-r--r--   0 mmckerns   (501) staff       (20)     2733 2022-10-24 02:46:26.000000 pathos-0.3.0/version.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.734623 pathos-0.3.1/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      832 2022-05-16 23:08:58.000000 pathos-0.3.1/.codecov.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)      983 2022-05-16 23:08:58.000000 pathos-0.3.1/.coveragerc
+-rw-r--r--   0 mmckerns   (501) staff       (20)       32 2016-12-29 21:27:25.000000 pathos-0.3.1/.gitignore
+-rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-05-16 23:08:58.000000 pathos-0.3.1/.readthedocs.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1757 2023-07-07 03:25:50.000000 pathos-0.3.1/.travis.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2023-02-08 18:06:08.000000 pathos-0.3.1/LICENSE
+-rw-r--r--   0 mmckerns   (501) staff       (20)      305 2022-07-06 23:18:45.000000 pathos-0.3.1/MANIFEST.in
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11328 2023-07-23 11:15:56.734913 pathos-0.3.1/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10712 2023-07-23 11:11:48.000000 pathos-0.3.1/README.md
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.529929 pathos-0.3.1/applications/
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      705 2023-01-17 13:07:04.000000 pathos-0.3.1/applications/install-pp-1.6.4.2.sh
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      821 2023-01-17 13:07:04.000000 pathos-0.3.1/applications/install-rpyc-3.0.6.sh
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4936 2023-01-17 13:07:04.000000 pathos-0.3.1/applications/install_pathos_server.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.537914 pathos-0.3.1/docs/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      670 2022-05-16 23:08:58.000000 pathos-0.3.1/docs/Makefile
+-rw-r--r--   0 mmckerns   (501) staff       (20)      430 2023-07-22 01:40:44.000000 pathos-0.3.1/docs/requirements.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.586799 pathos-0.3.1/docs/source/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.512231 pathos-0.3.1/docs/source/_static/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.606748 pathos-0.3.1/docs/source/_static/css/
+-rw-r--r--   0 mmckerns   (501) staff       (20)       85 2023-07-05 04:41:05.000000 pathos-0.3.1/docs/source/_static/css/custom.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8118 2023-07-05 04:58:27.000000 pathos-0.3.1/docs/source/conf.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      274 2023-02-04 23:56:45.000000 pathos-0.3.1/docs/source/helpers.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      312 2023-07-05 05:54:25.000000 pathos-0.3.1/docs/source/index.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2017-08-11 19:08:40.000000 pathos-0.3.1/docs/source/pathos.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2165 2023-07-05 06:02:34.000000 pathos-0.3.1/docs/source/pathos.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      250 2023-02-04 20:35:47.000000 pathos-0.3.1/docs/source/scripts.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      356 2023-02-04 23:56:05.000000 pathos-0.3.1/docs/source/secure.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      161 2023-02-04 23:57:39.000000 pathos-0.3.1/docs/source/xmlrpc.rst
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.647010 pathos-0.3.1/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)       88 2016-07-17 18:39:38.000000 pathos-0.3.1/examples/README
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2210 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/async_map.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1772 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/mp_class_example.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      993 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/nested.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2668 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/pp_map.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1936 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/secure_copy.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1150 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/secure_hello.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      871 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/simple_tunnel.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      919 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/spawn.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3277 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/sum_primesX.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      937 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/test_mpmap.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1062 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/test_mpmap2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1416 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/test_mpmap3.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1556 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/test_mpmap_dill.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      835 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/test_ppmap.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      806 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/test_ppmap2.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2232 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/test_profile.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1251 2023-01-17 13:07:04.000000 pathos-0.3.1/examples/xmlrpc_server.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.674058 pathos-0.3.1/examples2/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1124 2016-07-17 18:39:38.000000 pathos-0.3.1/examples2/README
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2235 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/all_scatter_gather.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2361 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/all_scatter_gather2.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      783 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/dejong.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2000 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/optimize.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1889 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/optimize0.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2201 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/optimize_cheby_diffev_map.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2201 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/optimize_cheby_powell_map.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2198 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/optimize_cheby_powell_mpimap.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2314 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/optimize_cheby_powell_mpmap.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2215 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/optimize_cheby_powell_ppmap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2072 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/optimize_helper.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2605 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/optimize_powell.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2167 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/optimize_rosen_powell_map.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1811 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/poly.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1435 2023-01-17 13:07:04.000000 pathos-0.3.1/examples2/scatter_gather.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.708556 pathos-0.3.1/pathos/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12089 2023-07-23 11:15:56.000000 pathos-0.3.1/pathos/__info__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2484 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5962 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      530 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/_ppserver_config.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10658 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/abstract_launcher.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6763 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/connection.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11145 2023-02-19 21:08:26.000000 pathos-0.3.1/pathos/core.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.715567 pathos-0.3.1/pathos/helpers/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1000 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/helpers/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2665 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/helpers/mp_helper.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8283 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/helpers/pp_helper.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1336 2023-02-19 20:05:53.000000 pathos-0.3.1/pathos/hosts.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    21385 2023-02-20 04:00:11.000000 pathos-0.3.1/pathos/maps.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2933 2023-02-20 04:04:53.000000 pathos-0.3.1/pathos/mp_map.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10250 2023-06-25 05:17:23.000000 pathos-0.3.1/pathos/multiprocessing.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17473 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/parallel.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1258 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/pools.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1944 2023-02-20 04:05:12.000000 pathos-0.3.1/pathos/portpicker.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      691 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/pp.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     7613 2023-02-20 04:05:42.000000 pathos-0.3.1/pathos/pp_map.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    14136 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/profile.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      646 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/python.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.719333 pathos-0.3.1/pathos/secure/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      447 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/secure/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4369 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/secure/connection.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4194 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/secure/copier.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5139 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/secure/tunnel.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6002 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/selector.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4855 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/serial.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1987 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/server.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.730225 pathos-0.3.1/pathos/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      507 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      901 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1897 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/tests/test_decorate.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7060 2023-01-31 05:18:43.000000 pathos-0.3.1/pathos/tests/test_join.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2170 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/tests/test_map.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1820 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/tests/test_maps.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5647 2023-06-25 03:38:04.000000 pathos-0.3.1/pathos/tests/test_mp.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1041 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/tests/test_pp.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1564 2023-02-12 20:07:11.000000 pathos-0.3.1/pathos/tests/test_random.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4908 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/tests/test_star.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1754 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/tests/test_with.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9015 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/threading.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2369 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/util.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.731913 pathos-0.3.1/pathos/xmlrpc/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      401 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/xmlrpc/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8547 2023-01-17 13:07:04.000000 pathos-0.3.1/pathos/xmlrpc/server.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.713351 pathos-0.3.1/pathos.egg-info/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11328 2023-07-23 11:15:56.000000 pathos-0.3.1/pathos.egg-info/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2590 2023-07-23 11:15:56.000000 pathos-0.3.1/pathos.egg-info/SOURCES.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-23 11:15:56.000000 pathos-0.3.1/pathos.egg-info/dependency_links.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-23 11:15:56.000000 pathos-0.3.1/pathos.egg-info/not-zip-safe
+-rw-r--r--   0 mmckerns   (501) staff       (20)       59 2023-07-23 11:15:56.000000 pathos-0.3.1/pathos.egg-info/requires.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        7 2023-07-23 11:15:56.000000 pathos-0.3.1/pathos.egg-info/top_level.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)      166 2022-05-20 09:49:04.000000 pathos-0.3.1/pyproject.toml
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:15:56.734032 pathos-0.3.1/scripts/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5962 2023-01-17 13:07:04.000000 pathos-0.3.1/scripts/pathos_connect
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      427 2023-01-17 13:07:04.000000 pathos-0.3.1/scripts/portpicker
+-rw-r--r--   0 mmckerns   (501) staff       (20)       62 2023-07-23 11:15:56.737811 pathos-0.3.1/setup.cfg
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4782 2023-07-23 11:11:55.000000 pathos-0.3.1/setup.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      298 2023-07-07 03:22:37.000000 pathos-0.3.1/tox.ini
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3171 2023-07-23 11:15:10.000000 pathos-0.3.1/version.py
```

### Comparing `pathos-0.3.0/.codecov.yml` & `pathos-0.3.1/.codecov.yml`

 * *Files identical despite different names*

### Comparing `pathos-0.3.0/.coveragerc` & `pathos-0.3.1/.coveragerc`

 * *Files identical despite different names*

### Comparing `pathos-0.3.0/LICENSE` & `pathos-0.3.1/LICENSE`

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

### Comparing `pathos-0.3.0/PKG-INFO` & `pathos-0.3.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pathos
-Version: 0.3.0
+Version: 0.3.1
 Summary: parallel graph management and execution in heterogeneous computing
 Home-page: https://github.com/uqfoundation/pathos
 Download-URL: https://pypi.org/project/pathos/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
@@ -20,14 +20,15 @@
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
 License-File: LICENSE
 
@@ -58,19 +59,19 @@
 also enables a single code-base to be maintained instead of requiring
 parallel, serial, and distributed versions of a code. ``pathos`` maps can be
 nested, thus hierarchical heterogeneous computing is possible by merely
 selecting the desired hierarchy of ``map`` and ``pipe`` (``apply``) objects.
 
 The ``pathos`` framework is composed of several interoperating packages:
 
-    - ``dill``: a utility to serialize all of python
+    - ``dill``: serialize all of Python
     - ``pox``: utilities for filesystem exploration and automated builds
     - ``klepto``: persistent caching to memory, disk, or database
-    - ``multiprocess``: better multiprocessing and multithreading in python
-    - ``ppft``: distributed and parallel python
+    - ``multiprocess``: better multiprocessing and multithreading in Python
+    - ``ppft``: distributed and parallel Python
     - ``pyina``: MPI parallel ``map`` and cluster scheduling
     - ``pathos``: graph management and execution in heterogeneous computing
 
 
 About Pathos
 ============
 
@@ -93,39 +94,39 @@
 ``pathos`` provides distributed ``map`` and ``pipe`` algorithms, where a mix of
 local processors and distributed workers can be selected.  ``pathos``
 also provides a very basic automated load balancing service, as well as
 the ability for the user to directly select the resources.
 
 The high-level ``pool.map`` interface, yields a ``map`` implementation that
 hides the RPC internals from the user. With ``pool.map``, the user can launch
-their code in parallel, and as a distributed service, using standard python
+their code in parallel, and as a distributed service, using standard Python
 and without writing a line of server or parallel batch code.
 
 RPC servers and communication in general is known to be insecure.  However,
 instead of attempting to make the RPC communication itself secure, ``pathos``
 provides the ability to automatically wrap any distributes service or
 communication in a ssh-tunnel. Ssh is a universally trusted method.
 Using ssh-tunnels, ``pathos`` has launched several distributed calculations
 on national lab clusters, and to date has performed test calculations
 that utilize node-to-node communication between several national lab clusters
 and a user's laptop.  ``pathos`` allows the user to configure and launch
 at a very atomistic level, through raw access to ssh and scp. 
 
-``pathos`` is the core of a python framework for heterogeneous computing.
+``pathos`` is the core of a Python framework for heterogeneous computing.
 ``pathos`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pathos/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``pathos`` provides a configurable distributed parallel ``map`` interface
 to launching RPC service calls, with:
 
-    - a ``map`` interface that meets and extends the python ``map`` standard
+    - a ``map`` interface that meets and extends the Python ``map`` standard
     - the ability to submit service requests to a selection of servers
     - the ability to tunnel server communications with ssh
 
 The ``pathos`` core is built on low-level communication to remote hosts using
 ssh. The interface to ssh, scp, and ssh-tunneled connections can:
 
     - configure and launch remote processes with ssh
@@ -168,46 +169,45 @@
 Requirements
 ============
 
 ``pathos`` requires:
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
-    - ``pox``, **>=0.3.2**
-    - ``dill``, **>=0.3.6**
-    - ``ppft``, **>=1.7.6.6**
-    - ``multiprocess``, **>=0.70.14**
+    - ``pox``, **>=0.3.3**
+    - ``dill``, **>=0.3.7**
+    - ``ppft``, **>=1.7.6.7**
+    - ``multiprocess``, **>=0.70.15**
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
-http://pathos.rtfd.io. Also see ``pathos.tests`` and ``pathos.examples``
-for a set of scripts that demonstrate the configuration and launching of
-communications with ssh and scp, and demonstrate the configuration and
-execution of jobs in a hierarchical parallel workflow. You can run the test
-suite with ``python -m pathos.tests``. Tunnels and other connections to
-remote servers can be established with the ``pathos_connect`` script (or with
-``python -m pathos``). See ``pathos_connect --help`` for more information.
-``pathos`` also provides a ``portpicker`` script to select an open port
-(also available with ``python -m pathos.portpicker``). The source code is 
-generally well documented, so further questions may be resolved by inspecting
-the code itself.  Please feel free to submit a ticket on github, or ask a
-question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pathos`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+http://pathos.rtfd.io. Also see ``pathos.tests`` and https://github.com/uqfoundation/pathos/tree/master/examples for a set of scripts that demonstrate the
+configuration and launching of communications with ssh and scp, and demonstrate
+the configuration and execution of jobs in a hierarchical parallel workflow.
+You can run the test suite with ``python -m pathos.tests``. Tunnels and other
+connections to remote servers can be established with the ``pathos_connect``
+script (or with ``python -m pathos``). See ``pathos_connect --help`` for more
+information.  ``pathos`` also provides a ``portpicker`` script to select an
+open port (also available with ``python -m pathos.portpicker``). The source
+code is generally well documented, so further questions may be resolved by
+inspecting the code itself.  Please feel free to submit a ticket on github,
+or ask a question on stackoverflow (**@Mike McKerns**). If you would like to
+share how you use ``pathos`` in your work, please send an email (to **mmckerns
+at uqfoundation dot org**).
 
 Important classes and functions are found here:
 
     - ``pathos.abstract_launcher``           [the worker pool API definition]
     - ``pathos.pools``                       [all of the pathos worker pools]
     - ``pathos.core``                        [the high-level command interface] 
     - ``pathos.hosts``                       [the hostname registry interface] 
-    - ``pathos.serial.SerialPool``           [the serial python worker pool]
+    - ``pathos.serial.SerialPool``           [the serial Python worker pool]
     - ``pathos.parallel.ParallelPool``       [the parallelpython worker pool]
     - ``pathos.multiprocessing.ProcessPool`` [the multiprocessing worker pool]
     - ``pathos.threading.ThreadPool``        [the multithreading worker pool]
     - ``pathos.connection.Pipe``             [the launcher base class]
     - ``pathos.secure.Pipe``                 [the secure launcher base class]
     - ``pathos.secure.Copier``               [the secure copier  base class]
     - ``pathos.secure.Tunnel``               [the secure tunnel base class]
```

### Comparing `pathos-0.3.0/README.md` & `pathos-0.3.1/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -24,19 +24,19 @@
 also enables a single code-base to be maintained instead of requiring
 parallel, serial, and distributed versions of a code. ``pathos`` maps can be
 nested, thus hierarchical heterogeneous computing is possible by merely
 selecting the desired hierarchy of ``map`` and ``pipe`` (``apply``) objects.
 
 The ``pathos`` framework is composed of several interoperating packages:
 
-* ``dill``: a utility to serialize all of python
+* ``dill``: serialize all of Python
 * ``pox``: utilities for filesystem exploration and automated builds
 * ``klepto``: persistent caching to memory, disk, or database
-* ``multiprocess``: better multiprocessing and multithreading in python
-* ``ppft``: distributed and parallel python
+* ``multiprocess``: better multiprocessing and multithreading in Python
+* ``ppft``: distributed and parallel Python
 * ``pyina``: MPI parallel ``map`` and cluster scheduling
 * ``pathos``: graph management and execution in heterogeneous computing
 
 
 About Pathos
 ------------
 The ``pathos`` package provides a few basic tools to make parallel and
@@ -58,38 +58,38 @@
 ``pathos`` provides distributed ``map`` and ``pipe`` algorithms, where a mix of
 local processors and distributed workers can be selected.  ``pathos``
 also provides a very basic automated load balancing service, as well as
 the ability for the user to directly select the resources.
 
 The high-level ``pool.map`` interface, yields a ``map`` implementation that
 hides the RPC internals from the user. With ``pool.map``, the user can launch
-their code in parallel, and as a distributed service, using standard python
+their code in parallel, and as a distributed service, using standard Python
 and without writing a line of server or parallel batch code.
 
 RPC servers and communication in general is known to be insecure.  However,
 instead of attempting to make the RPC communication itself secure, ``pathos``
 provides the ability to automatically wrap any distributes service or
 communication in a ssh-tunnel. Ssh is a universally trusted method.
 Using ssh-tunnels, ``pathos`` has launched several distributed calculations
 on national lab clusters, and to date has performed test calculations
 that utilize node-to-node communication between several national lab clusters
 and a user's laptop.  ``pathos`` allows the user to configure and launch
 at a very atomistic level, through raw access to ssh and scp. 
 
-``pathos`` is the core of a python framework for heterogeneous computing.
+``pathos`` is the core of a Python framework for heterogeneous computing.
 ``pathos`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pathos/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 --------------
 ``pathos`` provides a configurable distributed parallel ``map`` interface
 to launching RPC service calls, with:
 
-* a ``map`` interface that meets and extends the python ``map`` standard
+* a ``map`` interface that meets and extends the Python ``map`` standard
 * the ability to submit service requests to a selection of servers
 * the ability to tunnel server communications with ssh
 
 The ``pathos`` core is built on low-level communication to remote hosts using
 ssh. The interface to ssh, scp, and ssh-tunneled connections can:
 
 * configure and launch remote processes with ssh
@@ -133,45 +133,44 @@
 
 Requirements
 ------------
 ``pathos`` requires:
 
 * ``python`` (or ``pypy``), **>=3.7**
 * ``setuptools``, **>=42**
-* ``pox``, **>=0.3.2**
-* ``dill``, **>=0.3.6**
-* ``ppft``, **>=1.7.6.6**
-* ``multiprocess``, **>=0.70.14**
+* ``pox``, **>=0.3.3**
+* ``dill``, **>=0.3.7**
+* ``ppft``, **>=1.7.6.7**
+* ``multiprocess``, **>=0.70.15**
 
 
 More Information
 ----------------
 Probably the best way to get started is to look at the documentation at
-http://pathos.rtfd.io. Also see ``pathos.tests`` and ``pathos.examples``
-for a set of scripts that demonstrate the configuration and launching of
-communications with ssh and scp, and demonstrate the configuration and
-execution of jobs in a hierarchical parallel workflow. You can run the test
-suite with ``python -m pathos.tests``. Tunnels and other connections to
-remote servers can be established with the ``pathos_connect`` script (or with
-``python -m pathos``). See ``pathos_connect --help`` for more information.
-``pathos`` also provides a ``portpicker`` script to select an open port
-(also available with ``python -m pathos.portpicker``). The source code is 
-generally well documented, so further questions may be resolved by inspecting
-the code itself.  Please feel free to submit a ticket on github, or ask a
-question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pathos`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+http://pathos.rtfd.io. Also see ``pathos.tests`` and https://github.com/uqfoundation/pathos/tree/master/examples for a set of scripts that demonstrate the
+configuration and launching of communications with ssh and scp, and demonstrate
+the configuration and execution of jobs in a hierarchical parallel workflow.
+You can run the test suite with ``python -m pathos.tests``. Tunnels and other
+connections to remote servers can be established with the ``pathos_connect``
+script (or with ``python -m pathos``). See ``pathos_connect --help`` for more
+information.  ``pathos`` also provides a ``portpicker`` script to select an
+open port (also available with ``python -m pathos.portpicker``). The source
+code is generally well documented, so further questions may be resolved by
+inspecting the code itself.  Please feel free to submit a ticket on github,
+or ask a question on stackoverflow (**@Mike McKerns**). If you would like to
+share how you use ``pathos`` in your work, please send an email (to **mmckerns
+at uqfoundation dot org**).
 
 Important classes and functions are found here:
 
 * ``pathos.abstract_launcher``           [the worker pool API definition]
 * ``pathos.pools``                       [all of the pathos worker pools]
 * ``pathos.core``                        [the high-level command interface] 
 * ``pathos.hosts``                       [the hostname registry interface] 
-* ``pathos.serial.SerialPool``           [the serial python worker pool]
+* ``pathos.serial.SerialPool``           [the serial Python worker pool]
 * ``pathos.parallel.ParallelPool``       [the parallelpython worker pool]
 * ``pathos.multiprocessing.ProcessPool`` [the multiprocessing worker pool]
 * ``pathos.threading.ThreadPool``        [the multithreading worker pool]
 * ``pathos.connection.Pipe``             [the launcher base class]
 * ``pathos.secure.Pipe``                 [the secure launcher base class]
 * ``pathos.secure.Copier``               [the secure copier  base class]
 * ``pathos.secure.Tunnel``               [the secure tunnel base class]
```

### Comparing `pathos-0.3.0/applications/install-pp-1.6.4.2.sh` & `pathos-0.3.1/applications/install-pp-1.6.4.2.sh`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
   NAME=pp
   VERSION=1.6.4
   REVISION=2
   IDENTIFIER=$NAME-$VERSION.$REVISION
```

### Comparing `pathos-0.3.0/applications/install-rpyc-3.0.6.sh` & `pathos-0.3.1/applications/install-rpyc-3.0.6.sh`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
   NAME=rpyc
   VERSION=3.0
   REVISION=6
   IDENTIFIER=$NAME-$VERSION.$REVISION
```

### Comparing `pathos-0.3.0/applications/install_pathos_server.py` & `pathos-0.3.1/applications/install_pathos_server.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 remote bash-script installation of selected package
 
 Usage: python install_pathos_server.py [package] [version] [hostname] 
     [package] - name of the package to install
```

### Comparing `pathos-0.3.0/docs/Makefile` & `pathos-0.3.1/docs/Makefile`

 * *Files identical despite different names*

### Comparing `pathos-0.3.0/docs/source/conf.py` & `pathos-0.3.1/docs/source/conf.py`

 * *Files 9% similar despite different names*

```diff
@@ -54,24 +54,42 @@
 # source_suffix = ['.rst', '.md']
 source_suffix = '.rst'
 
 # The master toctree document.
 master_doc = 'index'
 
 # General information about the project.
-project = u'pathos'
+project = 'pathos'
 year = datetime.now().year
-copyright = u'%d, The Uncertainty Quantification Foundation' % year
-author = u'Mike McKerns'
+copyright = '%d, The Uncertainty Quantification Foundation' % year
+author = 'Mike McKerns'
 
 # extension config
 github_project_url = "https://github.com/uqfoundation/pathos"
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
@@ -83,15 +101,15 @@
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
@@ -111,57 +129,63 @@
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
     'github_repo': 'pathos',
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
 htmlhelp_basename = 'pathosdoc'
 
 # Logo for sidebar
@@ -188,45 +212,45 @@
     # 'figure_align': 'htbp',
 }
 
 # Grouping the document tree into LaTeX files. List of tuples
 # (source start file, target name, title,
 #  author, documentclass [howto, manual, or own class]).
 latex_documents = [
-    (master_doc, 'pathos.tex', u'pathos Documentation',
-     u'Mike McKerns', 'manual'),
+    (master_doc, 'pathos.tex', 'pathos Documentation',
+     'Mike McKerns', 'manual'),
 ]
 
 
 # -- Options for manual page output ---------------------------------------
 
 # One entry per manual page. List of tuples
 # (source start file, name, description, authors, manual section).
 man_pages = [
-    (master_doc, 'pathos', u'pathos Documentation',
+    (master_doc, 'pathos', 'pathos Documentation',
      [author], 1)
 ]
 
 
 # -- Options for Texinfo output -------------------------------------------
 
 # Grouping the document tree into Texinfo files. List of tuples
 # (source start file, target name, title, author,
 #  dir menu entry, description, category)
 texinfo_documents = [
-    (master_doc, 'pathos', u'pathos Documentation',
+    (master_doc, 'pathos', 'pathos Documentation',
      author, 'pathos', 'Parallel graph management and execution in heterogeneous computing.',
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

### Comparing `pathos-0.3.0/docs/source/pathos.png` & `pathos-0.3.1/docs/source/pathos.png`

 * *Files identical despite different names*

### Comparing `pathos-0.3.0/examples/async_map.py` & `pathos-0.3.1/examples/async_map.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 import time
 import sys
 
 def busy_add(x,y, delay=0.01):
```

### Comparing `pathos-0.3.0/examples/mp_class_example.py` & `pathos-0.3.1/examples/mp_class_example.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Nick Rhinehart (nrhineha @cmu)
 # Copyright (c) 2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 from pathos.pools import ProcessPool, ThreadPool
 import logging
 log = logging.getLogger(__name__)
```

### Comparing `pathos-0.3.0/examples/nested.py` & `pathos-0.3.1/examples/nested.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 def g(x):
   import random
   return int(x * random.random())
```

### Comparing `pathos-0.3.0/examples/pp_map.py` & `pathos-0.3.1/examples/pp_map.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 example of using the 'raw' distributed parallel mapper
 
 To run: python pp_map.py
 """
```

### Comparing `pathos-0.3.0/examples/secure_copy.py` & `pathos-0.3.1/examples/secure_copy.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 example of using the secure copy interface
 
 To run: python secure_copy.py
 """
```

### Comparing `pathos-0.3.0/examples/secure_hello.py` & `pathos-0.3.1/examples/secure_hello.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 example of using the secure launch interface
 
 To run: python secure_hello.py
 """
```

### Comparing `pathos-0.3.0/examples/simple_tunnel.py` & `pathos-0.3.1/examples/simple_tunnel.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 example of building a simple ssh-tunnel
 
 To run: python simple_tunnel.py
 """
```

### Comparing `pathos-0.3.0/examples/spawn.py` & `pathos-0.3.1/examples/spawn.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 demonstrate pathos's spawn2 function
 """
 
 from pathos.util import spawn2, _b, _str
```

### Comparing `pathos-0.3.0/examples/sum_primesX.py` & `pathos-0.3.1/examples/sum_primesX.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Calculate the sum of all primes below given integer n.
 
 Usage: python sum_primesX.py [tunnelport]
     [tunnelport] - the port number(s) of the local ssh tunnel connection,
```

### Comparing `pathos-0.3.0/examples/test_mpmap.py` & `pathos-0.3.1/examples/test_mpmap.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 def host(id):
     import socket
     return "Rank: %d -- %s" % (id, socket.gethostname())
```

### Comparing `pathos-0.3.0/examples/test_mpmap2.py` & `pathos-0.3.1/examples/test_mpmap2.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 def host(id):
     import socket
     return "Rank: %d -- %s" % (id, socket.gethostname())
```

### Comparing `pathos-0.3.0/examples/test_mpmap3.py` & `pathos-0.3.1/examples/test_mpmap3.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 # pickle fails for nested functions
 def adder(augend):
   zero = [0]
   def inner(addend):
```

### Comparing `pathos-0.3.0/examples/test_mpmap_dill.py` & `pathos-0.3.1/examples/test_mpmap_dill.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 import dill
 import pickle #XXX: multiprocessing needs cPickle + copy_reg
 
 dumps = pickle._dumps
```

### Comparing `pathos-0.3.0/examples/test_ppmap.py` & `pathos-0.3.1/examples/test_ppmap.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 from pathos.parallel import stats
 from pathos.parallel import ParallelPool as Pool
 pool = Pool()
```

### Comparing `pathos-0.3.0/examples/test_ppmap2.py` & `pathos-0.3.1/examples/test_ppmap2.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 from pathos.parallel import stats
 from pathos.parallel import ParallelPool as Pool
 pool = Pool()
```

### Comparing `pathos-0.3.0/examples/test_profile.py` & `pathos-0.3.1/examples/test_profile.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 demonstrates use of the pathos profiler
 
 inspired by: http://stackoverflow.com/a/32522579/4646678
 """
```

### Comparing `pathos-0.3.0/examples/xmlrpc_server.py` & `pathos-0.3.1/examples/xmlrpc_server.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 example of building a simple xmlrpc server and proxy,
 and then demonstrate the handling of a few basic requests
 
 To run: python xmlrpc_server.py
```

### Comparing `pathos-0.3.0/examples2/README` & `pathos-0.3.1/examples2/README`

 * *Files identical despite different names*

### Comparing `pathos-0.3.0/examples2/all_scatter_gather.py` & `pathos-0.3.1/examples2/all_scatter_gather.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """example: using the same code with different parallel backends
 
 Requires: development version of pathos, pyina
   http://pypi.python.org/pypi/pathos
   http://pypi.python.org/pypi/pyina
```

### Comparing `pathos-0.3.0/examples2/all_scatter_gather2.py` & `pathos-0.3.1/examples2/all_scatter_gather2.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """example: using the same code with different parallel backends
 
 Requires: development version of pathos, pyina
   http://pypi.python.org/pypi/pathos
   http://pypi.python.org/pypi/pyina
```

### Comparing `pathos-0.3.0/examples2/dejong.py` & `pathos-0.3.1/examples2/dejong.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Rosenbrock's function
 """
 
 from numpy import sum as numpysum
```

### Comparing `pathos-0.3.0/examples2/optimize.py` & `pathos-0.3.1/examples2/optimize.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Minimize the selected model with Powell's method.
 
 Requires: development version of mystic
   http://pypi.python.org/pypi/mystic
```

### Comparing `pathos-0.3.0/examples2/optimize0.py` & `pathos-0.3.1/examples2/optimize0.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Minimize the selected model with Powell's method.
 
 Requires: development version of mystic
   http://pypi.python.org/pypi/mystic
```

### Comparing `pathos-0.3.0/examples2/optimize_cheby_diffev_map.py` & `pathos-0.3.1/examples2/optimize_cheby_diffev_map.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Solve Nth-order Chebyshev polynomial coefficients with Differential Evolution.
 Launch optimizers with python's map.
 
 Requires: development version of mystic, pathos
```

### Comparing `pathos-0.3.0/examples2/optimize_cheby_powell_map.py` & `pathos-0.3.1/examples2/optimize_cheby_powell_map.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Solve Nth-order Chebyshev polynomial coefficients with Powell's method.
 Launch optimizers with python's map.
 
 Requires: development version of mystic, pathos
```

### Comparing `pathos-0.3.0/examples2/optimize_cheby_powell_mpimap.py` & `pathos-0.3.1/examples2/optimize_cheby_powell_mpimap.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Solve Nth-order Chebyshev polynomial coefficients with Powell's method.
 Launch optimizers with mpi4py's map.
 
 Requires: development version of mystic, pyina
```

### Comparing `pathos-0.3.0/examples2/optimize_cheby_powell_mpmap.py` & `pathos-0.3.1/examples2/optimize_cheby_powell_mpmap.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Solve Nth-order Chebyshev polynomial coefficients with Powell's method.
 Launch optimizers with multiprocessing's map.
 
 Requires: development version of mystic, pathos
```

### Comparing `pathos-0.3.0/examples2/optimize_cheby_powell_ppmap.py` & `pathos-0.3.1/examples2/optimize_cheby_powell_ppmap.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Solve Nth-order Chebyshev polynomial coefficients with Powell's method.
 Launch optimizers with parallelpython's map.
 
 Requires: development version of mystic, pathos
```

### Comparing `pathos-0.3.0/examples2/optimize_helper.py` & `pathos-0.3.1/examples2/optimize_helper.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 def fmin_powell(cost, x0, full=1, disp=1, monitor=0):
     """ change default behavior for selected optimizers """
     from mystic.solvers import fmin_powell as solver
     from mystic.monitors import Monitor, VerboseMonitor
```

### Comparing `pathos-0.3.0/examples2/optimize_powell.py` & `pathos-0.3.1/examples2/optimize_powell.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Minimize the selected model with Powell's method.
 
 Requires: development version of mystic, pathos, pyina
   http://pypi.python.org/pypi/mystic
```

### Comparing `pathos-0.3.0/examples2/optimize_rosen_powell_map.py` & `pathos-0.3.1/examples2/optimize_rosen_powell_map.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Minimize the Rosenbrock function with Powell's method.
 Launch optimizers with python's map.
 
 Requires: development version of mystic, pathos
```

### Comparing `pathos-0.3.0/examples2/poly.py` & `pathos-0.3.1/examples2/poly.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 Chebyshev's polynomials
 """
 from numpy import sum as numpysum
 from numpy import asarray
```

### Comparing `pathos-0.3.0/examples2/scatter_gather.py` & `pathos-0.3.1/examples2/scatter_gather.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """example: parallelism in python with mp4py
 
 Run with:
 > $ mpirun -np 2 scatter_gather.py
 """
```

### Comparing `pathos-0.3.0/pathos/__info__.py` & `pathos-0.3.1/pathos/__info__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 '''
 --------------------------------------------------------------------------
 pathos: parallel graph management and execution in heterogeneous computing
 --------------------------------------------------------------------------
 
@@ -32,19 +32,19 @@
 also enables a single code-base to be maintained instead of requiring
 parallel, serial, and distributed versions of a code. ``pathos`` maps can be
 nested, thus hierarchical heterogeneous computing is possible by merely
 selecting the desired hierarchy of ``map`` and ``pipe`` (``apply``) objects.
 
 The ``pathos`` framework is composed of several interoperating packages:
 
-    - ``dill``: a utility to serialize all of python
+    - ``dill``: serialize all of Python
     - ``pox``: utilities for filesystem exploration and automated builds
     - ``klepto``: persistent caching to memory, disk, or database
-    - ``multiprocess``: better multiprocessing and multithreading in python
-    - ``ppft``: distributed and parallel python
+    - ``multiprocess``: better multiprocessing and multithreading in Python
+    - ``ppft``: distributed and parallel Python
     - ``pyina``: MPI parallel ``map`` and cluster scheduling
     - ``pathos``: graph management and execution in heterogeneous computing
 
 
 About Pathos
 ============
 
@@ -67,39 +67,39 @@
 ``pathos`` provides distributed ``map`` and ``pipe`` algorithms, where a mix of
 local processors and distributed workers can be selected.  ``pathos``
 also provides a very basic automated load balancing service, as well as
 the ability for the user to directly select the resources.
 
 The high-level ``pool.map`` interface, yields a ``map`` implementation that
 hides the RPC internals from the user. With ``pool.map``, the user can launch
-their code in parallel, and as a distributed service, using standard python
+their code in parallel, and as a distributed service, using standard Python
 and without writing a line of server or parallel batch code.
 
 RPC servers and communication in general is known to be insecure.  However,
 instead of attempting to make the RPC communication itself secure, ``pathos``
 provides the ability to automatically wrap any distributes service or
 communication in a ssh-tunnel. Ssh is a universally trusted method.
 Using ssh-tunnels, ``pathos`` has launched several distributed calculations
 on national lab clusters, and to date has performed test calculations
 that utilize node-to-node communication between several national lab clusters
 and a user's laptop.  ``pathos`` allows the user to configure and launch
 at a very atomistic level, through raw access to ssh and scp. 
 
-``pathos`` is the core of a python framework for heterogeneous computing.
+``pathos`` is the core of a Python framework for heterogeneous computing.
 ``pathos`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pathos/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``pathos`` provides a configurable distributed parallel ``map`` interface
 to launching RPC service calls, with:
 
-    - a ``map`` interface that meets and extends the python ``map`` standard
+    - a ``map`` interface that meets and extends the Python ``map`` standard
     - the ability to submit service requests to a selection of servers
     - the ability to tunnel server communications with ssh
 
 The ``pathos`` core is built on low-level communication to remote hosts using
 ssh. The interface to ssh, scp, and ssh-tunneled connections can:
 
     - configure and launch remote processes with ssh
@@ -142,46 +142,45 @@
 Requirements
 ============
 
 ``pathos`` requires:
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
-    - ``pox``, **>=0.3.2**
-    - ``dill``, **>=0.3.6**
-    - ``ppft``, **>=1.7.6.6**
-    - ``multiprocess``, **>=0.70.14**
+    - ``pox``, **>=0.3.3**
+    - ``dill``, **>=0.3.7**
+    - ``ppft``, **>=1.7.6.7**
+    - ``multiprocess``, **>=0.70.15**
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
-http://pathos.rtfd.io. Also see ``pathos.tests`` and ``pathos.examples``
-for a set of scripts that demonstrate the configuration and launching of
-communications with ssh and scp, and demonstrate the configuration and
-execution of jobs in a hierarchical parallel workflow. You can run the test
-suite with ``python -m pathos.tests``. Tunnels and other connections to
-remote servers can be established with the ``pathos_connect`` script (or with
-``python -m pathos``). See ``pathos_connect --help`` for more information.
-``pathos`` also provides a ``portpicker`` script to select an open port
-(also available with ``python -m pathos.portpicker``). The source code is 
-generally well documented, so further questions may be resolved by inspecting
-the code itself.  Please feel free to submit a ticket on github, or ask a
-question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pathos`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+http://pathos.rtfd.io. Also see ``pathos.tests`` and https://github.com/uqfoundation/pathos/tree/master/examples for a set of scripts that demonstrate the
+configuration and launching of communications with ssh and scp, and demonstrate
+the configuration and execution of jobs in a hierarchical parallel workflow.
+You can run the test suite with ``python -m pathos.tests``. Tunnels and other
+connections to remote servers can be established with the ``pathos_connect``
+script (or with ``python -m pathos``). See ``pathos_connect --help`` for more
+information.  ``pathos`` also provides a ``portpicker`` script to select an
+open port (also available with ``python -m pathos.portpicker``). The source
+code is generally well documented, so further questions may be resolved by
+inspecting the code itself.  Please feel free to submit a ticket on github,
+or ask a question on stackoverflow (**@Mike McKerns**). If you would like to
+share how you use ``pathos`` in your work, please send an email (to **mmckerns
+at uqfoundation dot org**).
 
 Important classes and functions are found here:
 
     - ``pathos.abstract_launcher``           [the worker pool API definition]
     - ``pathos.pools``                       [all of the pathos worker pools]
     - ``pathos.core``                        [the high-level command interface] 
     - ``pathos.hosts``                       [the hostname registry interface] 
-    - ``pathos.serial.SerialPool``           [the serial python worker pool]
+    - ``pathos.serial.SerialPool``           [the serial Python worker pool]
     - ``pathos.parallel.ParallelPool``       [the parallelpython worker pool]
     - ``pathos.multiprocessing.ProcessPool`` [the multiprocessing worker pool]
     - ``pathos.threading.ThreadPool``        [the multithreading worker pool]
     - ``pathos.connection.Pipe``             [the launcher base class]
     - ``pathos.secure.Pipe``                 [the secure launcher base class]
     - ``pathos.secure.Copier``               [the secure copier  base class]
     - ``pathos.secure.Tunnel``               [the secure tunnel base class]
@@ -217,36 +216,36 @@
     https://uqfoundation.github.io/project/pathos
 
 Please see https://uqfoundation.github.io/project/pathos or
 http://arxiv.org/pdf/1202.1056 for further information.
 
 '''
 
-__version__ = '0.3.0'
+__version__ = '0.3.1'
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

### Comparing `pathos-0.3.0/pathos/__init__.py` & `pathos-0.3.1/pathos/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: June Kim (jkim @caltech)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 # author, version, license, and long description
 try: # the package is installed
     from .__info__ import __version__, __author__, __doc__, __license__
 except: # pragma: no cover
```

### Comparing `pathos-0.3.0/pathos/__main__.py` & `pathos-0.3.1/pathos/__main__.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 connect to the specified machine and start a 'server', 'tunnel', or both
 
 Notes:
     Usage: pathos_connect [hostname] [server] [remoteport] [profile]
```

### Comparing `pathos-0.3.0/pathos/_ppserver_config.py` & `pathos-0.3.1/pathos/_ppserver_config.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """defalut ppserver host and port configuration"""
 
 #tunnelports = ['12345','67890']
 tunnelports = []
```

### Comparing `pathos-0.3.0/pathos/abstract_launcher.py` & `pathos-0.3.1/pathos/abstract_launcher.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 This module contains the base classes for pathos pool and pipe objects,
 and describes the map and pipe interfaces.  A pipe is defined as a
 connection between two 'nodes', where a node is something that does
 work.  A pipe may be a one-way or two-way connection.  A map is defined
@@ -106,14 +106,15 @@
         object.__init__(self)#, *args, **kwds)
         self.__init(*args, **kwds)
         self._id = kwds.get('id', None)
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

### Comparing `pathos-0.3.0/pathos/connection.py` & `pathos-0.3.1/pathos/connection.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/env python
 #
 # Originally from pythia-0.8 pyre.mpi.Launcher.py (svn:danse.us/pyre -r2)
 # Forked by: Mike McKerns (January 2004)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2004-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 This module contains the base class for popen pipes, and describes
 the popen pipe interface. The 'config' method can be overwritten
 for pipe customization. The pipe's 'launch' method can be overwritten
 with a derived pipe's new execution algorithm. See the following for
```

### Comparing `pathos-0.3.0/pathos/core.py` & `pathos-0.3.1/pathos/core.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 high-level programming interface to core pathos utilities
 """
 __all__ = ['copy', 'execute', 'kill', 'getpid', 'getppid', 'getchild', \
            'serve', 'connect', 'randomport']
@@ -22,15 +22,15 @@
 
 def copy(source, destination=None, **kwds):
   '''copy source to (possibly) remote destination
 
 Execute a copy, and return the copier. Use 'kill' to kill the copier, and 
 'pid' to get the process id for the copier.
 
-Inputs:
+Args:
     source      -- path string of source 'file'
     destination -- path string for destination target
   '''
   #XXX: options, background, stdin can be set w/ kwds (also name, launcher)
   if destination is None: destination = os.getcwd()
   from pathos.secure import Copier
   opt = kwds.pop('options', None)
@@ -51,15 +51,15 @@
 def execute(command, host=None, bg=True, **kwds):
   '''execute a command (possibly) on a remote host
 
 Execute a process, and return the launcher. Use 'response' to retrieve the
 response from the executed command. Use 'kill' to kill the launcher, and 'pid'
 to get the process id for the launcher.
 
-Inputs:
+Args:
     command -- command string to be executed
     host    -- hostname of execution target  [default = None (i.e. run locally)]
     bg      -- run as background process?  [default = True]
   '''
   #XXX: options, background, stdin can be set w/ kwds (also name, launcher)
   bg = bool(bg) # overrides 'background'
   if host in [None, '']:
@@ -80,15 +80,15 @@
 
 
 #XXX: add local-only versions of kill and *pid to pox?
 #XXX: use threading.Timer (or sched) to schedule or kill after N seconds?
 def kill(pid, host=None, **kwds):
   '''kill a process (possibly) on a remote host
 
-Inputs:
+Args:
     pid   -- process id
     host  -- hostname where process is running [default = None (i.e. locally)]
   '''
   #XXX: launcher has "kill self" method; use it? note that this is different?
   command = 'kill -n TERM %s' % pid #XXX: use TERM=15 or KILL=9 ?
   getpid(pid, host) # throw error if pid doesn't exist #XXX: bad idea?
   response = execute(command, host, bg=False, **kwds).response()
@@ -117,15 +117,15 @@
 
 This method should only be used as a last-ditch effort to find a process id.
 This method __may__ work when a child has been spawned and the pid was not
 registered... but there's no guarantee.
 
 If target is None, then get the process id of the __main__  python instance.
 
-Inputs:
+Args:
     target -- string name of target process
     host   -- hostname where process is running
     all    -- get all resulting lines from query?  [default = False]
   '''
   if target is None:
     if all:
       target = ''
@@ -166,15 +166,15 @@
 
 
 def getppid(pid=None, host=None, group=False): # find parent of pid
   '''get parent process id (ppid) for the given process
 
 If pid is None, the pid of the __main__  python instance will be used.
 
-Inputs:
+Args:
     pid    -- process id
     host   -- hostname where process is running
     group  -- get parent group id (pgid) instead of direct parent id?
   '''
   if pid is None:
     if host:
       raise OSError('[Error 3] No such process')
@@ -203,15 +203,15 @@
 
 
 def getchild(pid=None, host=None, group=False): # find all children of pid
   '''get all child process ids for the given parent process id (ppid)
 
 If pid is None, the pid of the __main__  python instance will be used.
 
-Inputs:
+Args:
     pid    -- parent process id
     host   -- hostname where process is running
     group  -- get process ids for the parent group id (pgid) instead?
   '''
   if pid is None:
     if host:
       raise OSError('[Error 3] No such process')
@@ -241,15 +241,15 @@
   if exists: return children
   raise OSError('[Errno 3] No such process')
 
 
 def randomport(host=None):
   '''select a open port on a (possibly) remote host
 
-Inputs:
+Args:
     host -- hostname on which to select a open port
   '''
   from pathos.portpicker import randomport
   if not host:
     return randomport()
   from pathos.secure import Pipe
   from pathos.portpicker import __file__ as src
@@ -267,30 +267,30 @@
   # return remote port number
   return rport
 
 
 def connect(host, port=None, through=None):
   '''establish a secure tunnel connection to a remote host at the given port
 
-Inputs:
+Args:
     host     -- hostname to which a tunnel should be established
     port     -- port number (on host) to connect the tunnel to
     through  -- 'tunnel-through' hostname  [default = None]
   '''
   from pathos.secure import Tunnel
   t = Tunnel()
   t.connect(host, port, through)
   return t
 
 
 #FIXME: needs work...
 def serve(server, host=None, port=None, profile='.bash_profile'):
   '''begin serving RPC requests
 
-Inputs:
+Args:
     server: name of RPC server  (i.e. 'ppserver')
     host: hostname on which a server should be launched
     port: port number (on host) that server will accept request at
     profile: file to configure the user's environment [default='.bash_profile']
   '''
   if host is None: #XXX: and...?
     profile = ''
```

### Comparing `pathos-0.3.0/pathos/helpers/__init__.py` & `pathos-0.3.1/pathos/helpers/__init__.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 from . import pp_helper
 from . import mp_helper
 import ppft as parallelpython
```

### Comparing `pathos-0.3.0/pathos/helpers/mp_helper.py` & `pathos-0.3.1/pathos/helpers/mp_helper.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 map helper functions
 """
 # random_state and random_seed copied from mystic.tools
```

### Comparing `pathos-0.3.0/pathos/helpers/pp_helper.py` & `pathos-0.3.1/pathos/helpers/pp_helper.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 try:
     from multiprocess import TimeoutError
     from multiprocess.pool import MapResult as _MapResult
     from multiprocess.pool import ApplyResult as _ApplyResult
```

### Comparing `pathos-0.3.0/pathos/hosts.py` & `pathos-0.3.1/pathos/hosts.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,28 +1,28 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
 # dictionary of known host/profile pairs
 """
 high-level programming interface to pathos host registry
 """
 
 default_profile = '.bash_profile'
 _profiles = { }
 """
 For example, to register two 'known' host profiles:
 
   _profiles = { \
-     'foobar.danse.us':'.profile',
-     'computer.cacr.caltech.edu':'.cshrc',
+     'foobar.danse.us':'.profile', \
+     'computer.cacr.caltech.edu':'.cshrc', \
   }
 """
 
 def get_profile(rhost, assume=True):
   '''get the default $PROFILE for a remote host'''
   if rhost in _profiles:
     return _profiles[rhost]
```

### Comparing `pathos-0.3.0/pathos/maps.py` & `pathos-0.3.1/pathos/maps.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,28 +1,26 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 maps: stand-alone map-like objects using lazy pool instantiation
 """
 
 class Map(object):
 
     def __init__(self, pool=None, *args, **kwds):
         """map instance with internal lazy pool instantiation
 
-    Input:
+    Args:
         pool: pool object (i.e. pathos.pools.ProcessPool)
-
-    Additional Input:
-        args: positional arguments for pool initialization
-        kwds: keyword arguments for pool initialization
+        *args: positional arguments for pool initialization
+        **kwds: keyword arguments for pool initialization
         close: if True, close the pool to any new jobs [Default: False] 
         join: if True, reclaim the pool's closed workers [Default: False]
         clear: if True, delete the pool singleton [Default: False]
 
     NOTE: if a pool object is not provided, a builtins.map will be
         used with the returned iterator cast to a list.
     NOTE: pools from both multiprocess and pathos.pools can be used,
@@ -34,16 +32,16 @@
         In either case, a pool that has been "closed" will throw a
         ValueError if map is then called, and similarly, a ValueError
         will be thrown if join is called before a pool is "closed".
         The major difference is that if a pathos.pool is closed, the
         map instance cannot run new jobs until "clear" is called,
         while a new multiprocess pool will be created each time the
         map is executed. This leads to pathos.pools generally being
-        called with either `clear=True` or `clear=False`, and pools
-        from multprocess either using `close=True` or `join=True` or
+        called with either ``clear=True`` or ``clear=False``, and pools
+        from multprocess either using ``close=True`` or ``join=True`` or
         both. Some hierarchical parallel workflows are not allowed,
         and will result in an error being thrown; however, changing
         close, join, or clear can often remove the error.
         """
         self._clear = kwds.pop('clear', False)
         self._join = kwds.pop('join', self._clear)
         self._close = kwds.pop('close', self._join)
@@ -51,21 +49,21 @@
         self.args = args
         self.kwds = kwds
         self._pool = None
 
     def __call__(self, func, *args, **kwds):
         """instantiate a pool and execute the pool's map
 
-    Input:
+    Args:
         func: function object to map
-        args: positional arguments for map
-        kwds: keyword arguments for map
+        *args: positional arguments for map
+        **kwds: keyword arguments for map
 
     Returns:
-        results from execution of map(func, *args, **kwds)
+        results from execution of ``map(func, *args, **kwds)``
 
     NOTE: initializes a new worker pool with each call
         """
         if self.pool is None: #XXX: args, kwds?
             return list(map(func, *args)) #XXX: iterator or list?
         self._pool = pool = self.pool(*self.args, **self.kwds)
         result = pool.map(func, *args, **kwds)
@@ -119,20 +117,18 @@
 
 
 class Smap(Map):
 
     def __init__(self, pool=None, *args, **kwds):
         """starmap instance with internal lazy pool instantiation
 
-    Input:
+    Args:
         pool: pool object (i.e. pathos.pools.ProcessPool)
-
-    Additional Input:
-        args: positional arguments for pool initialization
-        kwds: keyword arguments for pool initialization
+        *args: positional arguments for pool initialization
+        **kwds: keyword arguments for pool initialization
         close: if True, close the pool to any new jobs [Default: False] 
         join: if True, reclaim the pool's closed workers [Default: False]
         clear: if True, delete the pool singleton [Default: False]
 
     NOTE: if a pool object is not provided, an itertools.starmap will
         be used with the returned iterator cast to a list.
     NOTE: pools from both multiprocess and pathos.pools can be used,
@@ -144,32 +140,32 @@
         In either case, a pool that has been "closed" will throw a
         ValueError if map is then called, and similarly, a ValueError
         will be thrown if join is called before a pool is "closed".
         The major difference is that if a pathos.pool is closed, the
         map instance cannot run new jobs until "clear" is called,
         while a new multiprocess pool will be created each time the
         map is executed. This leads to pathos.pools generally being
-        called with either `clear=True` or `clear=False`, and pools
-        from multprocess either using `close=True` or `join=True` or
+        called with either ``clear=True`` or ``clear=False``, and pools
+        from multprocess either using ``close=True`` or ``join=True`` or
         both. Some hierarchical parallel workflows are not allowed,
         and will result in an error being thrown; however, changing
         close, join, or clear can often remove the error.
         """
         super().__init__(pool, *args, **kwds)
 
     def __call__(self, func, *args, **kwds):
         """instantiate a pool and execute the pool's starmap
 
-    Input:
+    Args:
         func: function object to map
-        args: positional arguments for starmap
-        kwds: keyword arguments for starmap
+        *args: positional arguments for starmap
+        **kwds: keyword arguments for starmap
 
     Returns:
-        results from execution of starmap(func, *args, **kwds)
+        results from execution of ``starmap(func, *args, **kwds)``
 
     NOTE: initializes a new worker pool with each call
         """
         if self.pool is None: #XXX: args, kwds?
             from itertools import starmap
             return list(starmap(func, *args)) #XXX: iterator or list?
         self._pool = pool = self.pool(*self.args, **self.kwds)
@@ -185,56 +181,55 @@
 
 
 class Imap(Map):
 
     def __init__(self, pool=None, *args, **kwds):
         """map iterator with internal lazy pool instantiation
 
-    Input:
+    Args:
         pool: pool object (i.e. pathos.pools.ProcessPool)
-
-    Additional Input:
-        args: positional arguments for pool initialization
-        kwds: keyword arguments for pool initialization
+        *args: positional arguments for pool initialization
+        **kwds: keyword arguments for pool initialization
         close: if True, close the pool to any new jobs [Default: False] 
         join: if True, reclaim the pool's closed workers [Default: False]
         clear: if True, delete the pool singleton [Default: False]
 
-    NOTE: if a pool object is not provided, a builtins.map will be used.
+    NOTE: if a pool object is not provided, a builtins.map will be
+        used.
     NOTE: pools from both multiprocess and pathos.pools can be used,
         however the behavior is slightly different. Pools from both
         pathos and multiprocess have close and join methods, to close
         the pool to new jobs, and to shut down the pool's workers.
         Pools from pathos, however, are launched as singletons, so
         they also include a clear method that deletes the singleton.
         In either case, a pool that has been "closed" will throw a
         ValueError if map is then called, and similarly, a ValueError
         will be thrown if join is called before a pool is "closed".
         The major difference is that if a pathos.pool is closed, the
         map instance cannot run new jobs until "clear" is called,
         while a new multiprocess pool will be created each time the
         map is executed. This leads to pathos.pools generally being
-        called with either `clear=True` or `clear=False`, and pools
-        from multprocess either using `close=True` or `join=True` or
+        called with either ``clear=True`` or ``clear=False``, and pools
+        from multprocess either using ``close=True`` or ``join=True`` or
         both. Some hierarchical parallel workflows are not allowed,
         and will result in an error being thrown; however, changing
         close, join, or clear can often remove the error.
         """
         super().__init__(pool, *args, **kwds)
 
     def __call__(self, func, *args, **kwds):
         """instantiate a pool and execute the pool's map iterator
 
-    Input:
+    Args:
         func: function object to map
-        args: positional arguments for map iterator
-        kwds: keyword arguments for map iterator
+        *args: positional arguments for map iterator
+        **kwds: keyword arguments for map iterator
 
     Returns:
-        results from execution of map(func, *args, **kwds) iterator
+        results from execution of ``map(func, *args, **kwds)`` iterator
 
     NOTE: initializes a new worker pool with each call
         """
         if self.pool is None: #XXX: args, kwds?
             return map(func, *args)
         self._pool = pool = self.pool(*self.args, **self.kwds)
         imap = getattr(pool, 'imap', None)
@@ -248,56 +243,55 @@
 
 
 class Amap(Map):
 
     def __init__(self, pool=None, *args, **kwds):
         """async map instance with internal lazy pool instantiation
 
-    Input:
+    Args:
         pool: pool object (i.e. pathos.pools.ProcessPool)
-
-    Additional Input:
-        args: positional arguments for pool initialization
-        kwds: keyword arguments for pool initialization
+        *args: positional arguments for pool initialization
+        **kwds: keyword arguments for pool initialization
         close: if True, close the pool to any new jobs [Default: False] 
         join: if True, reclaim the pool's closed workers [Default: False]
         clear: if True, delete the pool singleton [Default: False]
 
-    NOTE: if a pool object is not provided, an error is thown.
+    NOTE: if a pool object is not provided, NotImplemented is returned
+        upon use.
     NOTE: pools from both multiprocess and pathos.pools can be used,
         however the behavior is slightly different. Pools from both
         pathos and multiprocess have close and join methods, to close
         the pool to new jobs, and to shut down the pool's workers.
         Pools from pathos, however, are launched as singletons, so
         they also include a clear method that deletes the singleton.
         In either case, a pool that has been "closed" will throw a
         ValueError if map is then called, and similarly, a ValueError
         will be thrown if join is called before a pool is "closed".
         The major difference is that if a pathos.pool is closed, the
         map instance cannot run new jobs until "clear" is called,
         while a new multiprocess pool will be created each time the
         map is executed. This leads to pathos.pools generally being
-        called with either `clear=True` or `clear=False`, and pools
-        from multprocess either using `close=True` or `join=True` or
+        called with either ``clear=True`` or ``clear=False``, and pools
+        from multprocess either using ``close=True`` or ``join=True`` or
         both. Some hierarchical parallel workflows are not allowed,
         and will result in an error being thrown; however, changing
         close, join, or clear can often remove the error.
         """
         super().__init__(pool, *args, **kwds)
 
     def __call__(self, func, *args, **kwds):
         """instantiate a pool and execute the pool's async map
 
-    Input:
+    Args:
         func: function object to map
-        args: positional arguments for async map
-        kwds: keyword arguments for async map
+        *args: positional arguments for async map
+        **kwds: keyword arguments for async map
 
     Returns:
-        results from execution of async map(func, *args, **kwds)
+        results from execution of async ``map(func, *args, **kwds)``
 
     NOTE: initializes a new worker pool with each call
         """
         if self.pool is None: #XXX: args, kwds?
             return NotImplemented
         self._pool = pool = self.pool(*self.args, **self.kwds)
         amap = getattr(pool, 'amap', getattr(pool, 'map_async', None))
@@ -311,56 +305,55 @@
 
 
 class Asmap(Map):
 
     def __init__(self, pool=None, *args, **kwds):
         """async starmap instance with internal lazy pool instantiation
 
-    Input:
+    Args:
         pool: pool object (i.e. pathos.pools.ProcessPool)
-
-    Additional Input:
-        args: positional arguments for pool initialization
-        kwds: keyword arguments for pool initialization
+        *args: positional arguments for pool initialization
+        **kwds: keyword arguments for pool initialization
         close: if True, close the pool to any new jobs [Default: False] 
         join: if True, reclaim the pool's closed workers [Default: False]
         clear: if True, delete the pool singleton [Default: False]
 
-    NOTE: if a pool object is not provided, an error is thown.
+    NOTE: if a pool object is not provided, NotImplemented is returned
+        upon use.
     NOTE: pools from both multiprocess and pathos.pools can be used,
         however the behavior is slightly different. Pools from both
         pathos and multiprocess have close and join methods, to close
         the pool to new jobs, and to shut down the pool's workers.
         Pools from pathos, however, are launched as singletons, so
         they also include a clear method that deletes the singleton.
         In either case, a pool that has been "closed" will throw a
         ValueError if map is then called, and similarly, a ValueError
         will be thrown if join is called before a pool is "closed".
         The major difference is that if a pathos.pool is closed, the
         map instance cannot run new jobs until "clear" is called,
         while a new multiprocess pool will be created each time the
         map is executed. This leads to pathos.pools generally being
-        called with either `clear=True` or `clear=False`, and pools
-        from multprocess either using `close=True` or `join=True` or
+        called with either ``clear=True`` or ``clear=False``, and pools
+        from multprocess either using ``close=True`` or ``join=True`` or
         both. Some hierarchical parallel workflows are not allowed,
         and will result in an error being thrown; however, changing
         close, join, or clear can often remove the error.
         """
         super().__init__(pool, *args, **kwds)
 
     def __call__(self, func, *args, **kwds):
         """instantiate a pool and execute the pool's async starmap
 
-    Input:
+    Args:
         func: function object to map
-        args: positional arguments for async starmap
-        kwds: keyword arguments for async starmap
+        *args: positional arguments for async starmap
+        **kwds: keyword arguments for async starmap
 
     Returns:
-        results from execution of async starmap(func, *args, **kwds)
+        results from execution of async ``starmap(func, *args, **kwds)``
 
     NOTE: initializes a new worker pool with each call
         """
         if self.pool is None: #XXX: args, kwds?
             return NotImplemented
         self._pool = pool = self.pool(*self.args, **self.kwds)
         asmap = getattr(pool, 'asmap', getattr(pool, 'starmap_async', None))
@@ -375,56 +368,55 @@
 
 
 class Uimap(Map):
 
     def __init__(self, pool=None, *args, **kwds):
         """unordered map iterator with internal lazy pool instantiation
 
-    Input:
+    Args:
         pool: pool object (i.e. pathos.pools.ProcessPool)
-
-    Additional Input:
-        args: positional arguments for pool initialization
-        kwds: keyword arguments for pool initialization
+        *args: positional arguments for pool initialization
+        **kwds: keyword arguments for pool initialization
         close: if True, close the pool to any new jobs [Default: False] 
         join: if True, reclaim the pool's closed workers [Default: False]
         clear: if True, delete the pool singleton [Default: False]
 
-    NOTE: if a pool object is not provided, an error is thown.
+    NOTE: if a pool object is not provided, NotImplemented is returned
+        upon use.
     NOTE: pools from both multiprocess and pathos.pools can be used,
         however the behavior is slightly different. Pools from both
         pathos and multiprocess have close and join methods, to close
         the pool to new jobs, and to shut down the pool's workers.
         Pools from pathos, however, are launched as singletons, so
         they also include a clear method that deletes the singleton.
         In either case, a pool that has been "closed" will throw a
         ValueError if map is then called, and similarly, a ValueError
         will be thrown if join is called before a pool is "closed".
         The major difference is that if a pathos.pool is closed, the
         map instance cannot run new jobs until "clear" is called,
         while a new multiprocess pool will be created each time the
         map is executed. This leads to pathos.pools generally being
-        called with either `clear=True` or `clear=False`, and pools
-        from multprocess either using `close=True` or `join=True` or
+        called with either ``clear=True`` or ``clear=False``, and pools
+        from multprocess either using ``close=True`` or ``join=True`` or
         both. Some hierarchical parallel workflows are not allowed,
         and will result in an error being thrown; however, changing
         close, join, or clear can often remove the error.
         """
         super().__init__(pool, *args, **kwds)
 
     def __call__(self, func, *args, **kwds):
         """instantiate a pool and execute the pool's unordered map iterator
 
-    Input:
+    Args:
         func: function object to map
-        args: positional arguments for unordered map iterator
-        kwds: keyword arguments for unordered map iterator
+        *args: positional arguments for unordered map iterator
+        **kwds: keyword arguments for unordered map iterator
 
     Returns:
-        results from execution of unordered map(func, *args, **kwds) iterator
+        results from execution of unordered ``map(func, *args, **kwds)`` iterator
 
     NOTE: initializes a new worker pool with each call
         """
         if self.pool is None: #XXX: args, kwds?
             return NotImplemented
         self._pool = pool = self.pool(*self.args, **self.kwds)
         uimap = getattr(pool, 'uimap', getattr(pool, 'imap_unordered', None))
@@ -438,20 +430,18 @@
 
 
 class Ismap(Map):
 
     def __init__(self, pool=None, *args, **kwds):
         """starmap iterator with internal lazy pool instantiation
 
-    Input:
+    Args:
         pool: pool object (i.e. pathos.pools.ProcessPool)
-
-    Additional Input:
-        args: positional arguments for pool initialization
-        kwds: keyword arguments for pool initialization
+        *args: positional arguments for pool initialization
+        **kwds: keyword arguments for pool initialization
         close: if True, close the pool to any new jobs [Default: False] 
         join: if True, reclaim the pool's closed workers [Default: False]
         clear: if True, delete the pool singleton [Default: False]
 
     NOTE: if a pool object is not provided, an itertools.starmap will
         be used.
     NOTE: pools from both multiprocess and pathos.pools can be used,
@@ -463,32 +453,32 @@
         In either case, a pool that has been "closed" will throw a
         ValueError if map is then called, and similarly, a ValueError
         will be thrown if join is called before a pool is "closed".
         The major difference is that if a pathos.pool is closed, the
         map instance cannot run new jobs until "clear" is called,
         while a new multiprocess pool will be created each time the
         map is executed. This leads to pathos.pools generally being
-        called with either `clear=True` or `clear=False`, and pools
-        from multprocess either using `close=True` or `join=True` or
+        called with either ``clear=True`` or ``clear=False``, and pools
+        from multprocess either using ``close=True`` or ``join=True`` or
         both. Some hierarchical parallel workflows are not allowed,
         and will result in an error being thrown; however, changing
         close, join, or clear can often remove the error.
         """
         super().__init__(pool, *args, **kwds)
 
     def __call__(self, func, *args, **kwds):
         """instantiate a pool and execute the pool's starmap iterator
 
-    Input:
+    Args:
         func: function object to map
-        args: positional arguments for starmap iterator
-        kwds: keyword arguments for starmap iterator
+        *args: positional arguments for starmap iterator
+        **kwds: keyword arguments for starmap iterator
 
     Returns:
-        results from execution of starmap(func, *args, **kwds) iterator
+        results from execution of ``starmap(func, *args, **kwds)`` iterator
 
     NOTE: initializes a new worker pool with each call
         """
         if self.pool is None: #XXX: args, kwds?
             from itertools import starmap
             return starmap(func, *args)
         self._pool = pool = self.pool(*self.args, **self.kwds)
```

### Comparing `pathos-0.3.0/pathos/mp_map.py` & `pathos-0.3.1/pathos/mp_map.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 minimal interface to python's multiprocessing module
 
 Notes:
     This module has been deprecated in favor of ``pathos.pools``.
@@ -21,22 +21,20 @@
 __all__ = ['mp_map']
 
 # backward compatibility
 #FIXME: deprecated... and buggy!  (fails to dill on imap/uimap)
 def mp_map(function, sequence, *args, **kwds):
     '''extend python's parallel map function to multiprocessing
 
-Inputs:
-    function  -- target function
-    sequence  -- sequence to process in parallel
-
-Additional Inputs:
-    nproc     -- number of 'local' cpus to use  [defaut = 'autodetect']
-    type      -- processing type ['blocking', 'non-blocking', 'unordered']
-    threads   -- if True, use threading instead of multiprocessing
+Args:
+    function - target function
+    sequence - sequence to process in parallel
+    nproc - number of 'local' cpus to use  [defaut = 'autodetect']
+    type - processing type ['blocking', 'non-blocking', 'unordered']
+    threads - if True, use threading instead of multiprocessing
     '''
     processes = cpu_count()
     proctype = 'blocking'
     threads = False
     if 'nproc' in kwds:
         processes = kwds['nproc']
         kwds.pop('nproc')
```

### Comparing `pathos-0.3.0/pathos/multiprocessing.py` & `pathos-0.3.1/pathos/threading.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
-This module contains map and pipe interfaces to python's multiprocessing module.
+This module contains map and pipe interfaces to python's threading module.
 
 Pipe methods provided:
     pipe        - blocking communication pipe             [returns: value]
     apipe       - asynchronous communication pipe         [returns: object]
 
 Map methods provided:
     map         - blocking and ordered worker pool        [returns: list]
@@ -18,19 +18,19 @@
     uimap       - non-blocking and unordered worker pool  [returns: iterator]
     amap        - asynchronous worker pool                [returns: object]
 
 
 Usage
 =====
 
-A typical call to a pathos multiprocessing map will roughly follow this example:
+A typical call to a pathos threading map will roughly follow this example:
 
     >>> # instantiate and configure the worker pool
-    >>> from pathos.multiprocessing import ProcessPool
-    >>> pool = ProcessPool(nodes=4)
+    >>> from pathos.threading import ThreadPool
+    >>> pool = ThreadPool(nodes=4)
     >>>
     >>> # do a blocking map on the chosen function
     >>> print(pool.map(pow, [1,2,3,4], [5,6,7,8]))
     >>>
     >>> # do a non-blocking map, then extract the results from the iterator
     >>> results = pool.imap(pow, [1,2,3,4], [5,6,7,8])
     >>> print("...")
@@ -53,142 +53,152 @@
     >>> print(result1.get())
     >>> print(result2.get())
 
 
 Notes
 =====
 
-This worker pool leverages the python's multiprocessing module, and thus
+This worker pool leverages the python's multiprocessing.dummy module, and thus
 has many of the limitations associated with that module. The function f and
 the sequences in args must be serializable. The maps in this worker pool
 have full functionality whether run from a script or in the python
 interpreter, and work reliably for both imported and interactively-defined
-functions. Unlike python's multiprocessing module, pathos.multiprocessing maps
+functions. Unlike python's multiprocessing.dummy module, pathos.threading maps
 can directly utilize functions that require multiple arguments.
 
 """
-__all__ = ['ProcessPool','_ProcessPool']
+__all__ = ['ThreadPool','_ThreadPool']
 
 #FIXME: probably not good enough... should store each instance with a uid
-__STATE = _ProcessPool__STATE = {}
+__STATE = _ThreadPool__STATE = {}
 
 from pathos.abstract_launcher import AbstractWorkerPool
 from pathos.helpers.mp_helper import starargs as star
-from pathos.helpers import cpu_count, freeze_support, ProcessPool as Pool
+from pathos.helpers import cpu_count, ThreadPool as _ThreadPool
 
-# 'forward' compatibility
-_ProcessPool = Pool
-
-class ProcessPool(AbstractWorkerPool):
+class ThreadPool(AbstractWorkerPool):
     """
-Mapper that leverages python's multiprocessing.
+Mapper that leverages python's threading.
     """
     def __init__(self, *args, **kwds):
-        """\nNOTE: if number of nodes is not given, will autodetect processors
+        """\nNOTE: if number of nodes is not given, will autodetect processors.
+\nNOTE: additional keyword input is optional, with:
+    id          - identifier for the pool
+    initializer - function that takes no input, called when node is spawned
+    initargs    - tuple of args for initializers that have args
         """
         hasnodes = 'nodes' in kwds; arglen = len(args)
-        if 'ncpus' in kwds and (hasnodes or arglen):
-            msg = "got multiple values for keyword argument 'ncpus'"
+        if 'nthreads' in kwds and (hasnodes or arglen):
+            msg = "got multiple values for keyword argument 'nthreads'"
             raise TypeError(msg)
         elif hasnodes: #XXX: multiple try/except is faster?
             if arglen:
                 msg = "got multiple values for keyword argument 'nodes'"
                 raise TypeError(msg)
-            kwds['ncpus'] = kwds.pop('nodes')
+            kwds['nthreads'] = kwds.pop('nodes')
         elif arglen:
-            kwds['ncpus'] = args[0]
-        self.__nodes = kwds.get('ncpus', cpu_count())
+            kwds['nthreads'] = args[0]
+        if 'processes' in kwds:
+            if 'nthreads' in kwds:
+                msg = "got multiple values for keyword argument 'processes'"
+                raise TypeError(msg)
+            kwds['nthreads'] = kwds.pop('processes')
+        self.__nodes = kwds.pop('nthreads', cpu_count())
 
         # Create an identifier for the pool
-        self._id = kwds.get('id', None) #'pool'
+        self._id = kwds.pop('id', None) #'threads'
         if self._id is None:
             self._id = self.__nodes
 
+        self._kwds = kwds
+
         # Create a new server if one isn't already initialized
         self._serve()
         return
     if AbstractWorkerPool.__init__.__doc__: __init__.__doc__ = AbstractWorkerPool.__init__.__doc__ + __init__.__doc__
    #def __exit__(self, *args):
    #    self._clear()
    #    return
     def _serve(self, nodes=None): #XXX: should be STATE method; use id
         """Create a new server if one isn't already initialized"""
         if nodes is None: nodes = self.__nodes
         _pool = __STATE.get(self._id, None)
-        if not _pool or nodes != _pool.__nodes:
+        if not _pool or nodes != _pool.__nodes or self._kwds != _pool._kwds:
             self._clear()
-            _pool = Pool(nodes)
+            _pool = _ThreadPool(nodes, **self._kwds)
             _pool.__nodes = nodes
+            _pool._kwds = self._kwds
             __STATE[self._id] = _pool
         return _pool
     def _clear(self): #XXX: should be STATE method; use id
         """Remove server with matching state"""
         _pool = __STATE.get(self._id, None)
-        if _pool and self.__nodes == _pool.__nodes:
+        if _pool and self.__nodes == _pool.__nodes and self._kwds == _pool._kwds:
             _pool.close()
             _pool.join()
             __STATE.pop(self._id, None)
         return #XXX: return _pool?
     clear = _clear
     def map(self, f, *args, **kwds):
         AbstractWorkerPool._AbstractWorkerPool__map(self, f, *args, **kwds)
         _pool = self._serve()
-        return _pool.map(star(f), zip(*args)) # chunksize
+        return _pool.map(star(f), zip(*args), **kwds)
     map.__doc__ = AbstractWorkerPool.map.__doc__
     def imap(self, f, *args, **kwds):
         AbstractWorkerPool._AbstractWorkerPool__imap(self, f, *args, **kwds)
         _pool = self._serve()
-        return _pool.imap(star(f), zip(*args)) # chunksize
+        return _pool.imap(star(f), zip(*args), **kwds)
     imap.__doc__ = AbstractWorkerPool.imap.__doc__
     def uimap(self, f, *args, **kwds):
         AbstractWorkerPool._AbstractWorkerPool__imap(self, f, *args, **kwds)
         _pool = self._serve()
-        return _pool.imap_unordered(star(f), zip(*args)) # chunksize
+        return _pool.imap_unordered(star(f), zip(*args), **kwds)
     uimap.__doc__ = AbstractWorkerPool.uimap.__doc__
     def amap(self, f, *args, **kwds): # register a callback ?
         AbstractWorkerPool._AbstractWorkerPool__map(self, f, *args, **kwds)
         _pool = self._serve()
-        return _pool.map_async(star(f), zip(*args)) # chunksize
+        return _pool.map_async(star(f), zip(*args), **kwds)
     amap.__doc__ = AbstractWorkerPool.amap.__doc__
     ########################################################################
     # PIPES
     def pipe(self, f, *args, **kwds):
        #AbstractWorkerPool._AbstractWorkerPool__pipe(self, f, *args, **kwds)
         _pool = self._serve()
         return _pool.apply(f, args, kwds)
-    pipe.__doc__ = AbstractWorkerPool.pipe.__doc__
+   #pipe.__doc__ = AbstractWorkerPool.pipe.__doc__
     def apipe(self, f, *args, **kwds): # register a callback ?
        #AbstractWorkerPool._AbstractWorkerPool__apipe(self, f, *args, **kwds)
         _pool = self._serve()
         return _pool.apply_async(f, args, kwds)
-    apipe.__doc__ = AbstractWorkerPool.apipe.__doc__
+   #apipe.__doc__ = AbstractWorkerPool.apipe.__doc__
     ########################################################################
     def __repr__(self):
-        mapargs = (self.__class__.__name__, self.ncpus)
-        return "<pool %s(ncpus=%s)>" % mapargs
+        mapargs = (self.__class__.__name__, self.nthreads)
+        return "<pool %s(nthreads=%s)>" % mapargs
     def __get_nodes(self):
         """get the number of nodes used in the map"""
         return self.__nodes
     def __set_nodes(self, nodes):
         """set the number of nodes used in the map"""
         self._serve(nodes)
         self.__nodes = nodes
         return
     ########################################################################
     def restart(self, force=False):
         "restart a closed pool"
         _pool = __STATE.get(self._id, None)
-        if _pool and self.__nodes == _pool.__nodes:
+        if _pool and self.__nodes == _pool.__nodes and self._kwds == _pool._kwds:
             RUN = 0
             if not force:
                 assert _pool._state != RUN
             # essentially, 'clear' and 'serve'
             self._clear()
-            _pool = Pool(self.__nodes)
+            _pool = _ThreadPool(self.__nodes, **self._kwds)
             _pool.__nodes = self.__nodes
+            _pool._kwds = self._kwds
             __STATE[self._id] = _pool
         return _pool
     def close(self):
         "close the pool to any new jobs"
         _pool = __STATE.get(self._id, None)
         if _pool and self.__nodes == _pool.__nodes:
             _pool.close()
@@ -202,19 +212,14 @@
     def join(self):
         "cleanup the closed worker processes"
         _pool = __STATE.get(self._id, None)
         if _pool and self.__nodes == _pool.__nodes:
             _pool.join()
         return
     # interface
-    ncpus = property(__get_nodes, __set_nodes)
+    nthreads = property(__get_nodes, __set_nodes)
     nodes = property(__get_nodes, __set_nodes)
     __state__ = __STATE
     pass
 
 
-# backward compatibility
-from pathos.helpers import ThreadPool
-from pathos.threading import ThreadPool as ThreadingPool
-ProcessingPool = ProcessPool
-
 # EOF
```

### Comparing `pathos-0.3.0/pathos/parallel.py` & `pathos-0.3.1/pathos/parallel.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 # Based on code by Kirk Strauser <kirk@strauser.com>
 # Rev: 1139; Date: 2008-04-16
 # (see license text in pathos.pp_map)
 #
 # Forked by: Mike McKerns (April 2008)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
 # Modified to meet the pathos pool API
 """
 This module contains map and pipe interfaces to the parallelpython (pp) module.
 
@@ -136,16 +136,19 @@
 
 #XXX: should look into parallelpython for 'cluster computing'
 class ParallelPool(AbstractWorkerPool):
     """
 Mapper that leverages parallelpython (i.e. pp) maps.
     """
     def __init__(self, *args, **kwds):
-        """\nNOTE: if number of nodes is not given, will autodetect processors
-NOTE: if a tuple of servers is not provided, defaults to localhost only
+        """\nNOTE: if number of nodes is not given, will autodetect processors.
+\nNOTE: if a tuple of servers is not provided, defaults to localhost only.
+\nNOTE: additional keyword input is optional, with:
+    id          - identifier for the pool
+    servers     - tuple of pp.Servers
         """
         hasnodes = 'nodes' in kwds; arglen = len(args)
         if 'ncpus' in kwds and (hasnodes or arglen):
             msg = "got multiple values for keyword argument 'ncpus'"
             raise TypeError(msg)
         elif hasnodes: #XXX: multiple try/except is faster?
             if arglen:
@@ -219,28 +222,28 @@
         _pool.destroy()
         __STATE.pop(self._id, None)
         self._exiting = False
         return #XXX: return _pool?
     clear = _clear
     def map(self, f, *args, **kwds):
         AbstractWorkerPool._AbstractWorkerPool__map(self, f, *args, **kwds)
-        return list(self.imap(f, *args))
+        return list(self.imap(f, *args)) # chunksize
     map.__doc__ = AbstractWorkerPool.map.__doc__
     def imap(self, f, *args, **kwds):
         AbstractWorkerPool._AbstractWorkerPool__imap(self, f, *args, **kwds)
         def submit(*argz):
             """send a job to the server"""
             _pool = self._serve()
            #print("using %s local workers" % _pool.get_ncpus())
             try:
                 return _pool.submit(f, argz, globals=globals())
             except pp.DestroyedServerError:
                 self._is_alive(None)
         # submit all jobs, then collect results as they become available
-        return (subproc() for subproc in list(builtins.map(submit, *args)))
+        return (subproc() for subproc in list(builtins.map(submit, *args))) # chunksize
     imap.__doc__ = AbstractWorkerPool.imap.__doc__
     def uimap(self, f, *args, **kwds):
         AbstractWorkerPool._AbstractWorkerPool__imap(self, f, *args, **kwds)
         def submit(*argz):
             """send a job to the server"""
             _pool = self._serve()
            #print("using %s local workers" % _pool.get_ncpus())
@@ -256,15 +259,15 @@
                     if job.finished:
                         yield it.pop(i)()
                         break
                 # yield it.pop(0).get()  # wait for the first element?
                 # *subprocess*           # alternately, loop in a subprocess
             return #raise StopIteration
         # submit all jobs, then collect results as they become available
-        return imap_unordered(builtins.map(submit, *args))
+        return imap_unordered(builtins.map(submit, *args)) # chunksize
     uimap.__doc__ = AbstractWorkerPool.uimap.__doc__
     def amap(self, f, *args, **kwds):
         AbstractWorkerPool._AbstractWorkerPool__map(self, f, *args, **kwds)
         def submit(*argz):
             """send a job to the server"""
             _pool = self._serve()
            #print("using %s local workers" % _pool.get_ncpus())
@@ -285,15 +288,15 @@
             _pool = self._serve()
             nodes = _pool.get_ncpus() #NOTE: local only
             #nodes = _pool.get_active_nodes() #XXX: ppft version?
             #nodes = min(j for (i,j) in nodes.items() if i != 'local')
         if not nodes: nodes = 1
         # try to quickly find a small chunksize that gives good results
         maxsize = 2**62 #XXX: HOPEFULLY, this will never be reached...
-        chunksize = 1
+        chunksize = 1 # chunksize
         while chunksize < maxsize:
             chunksize, extra = divmod(length, nodes * elem_size)
             if override: break # the user *wants* to override this loop
             if extra >= length: break # we found something that 'works'
             elem_size = elem_size * 2
         if extra: chunksize += 1
         m = MapResult((chunksize,length))
```

### Comparing `pathos-0.3.0/pathos/pools.py` & `pathos-0.3.1/pathos/pools.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 pools: pools of pathos workers, providing map and pipe constructs
 """
 
 def _clear(type=None):
```

### Comparing `pathos-0.3.0/pathos/portpicker.py` & `pathos-0.3.1/pathos/portpicker.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
 # this script prints out an available port number.
 # adapted from J. Kim & M. McKerns utility functions
 """
 This script prints out an available port number.
@@ -22,15 +22,15 @@
 
     def __init__(self, min=0, max=64*1024):
         '''select a port number from a given range.
 
 The first call will return a random number from the available range,
 and each subsequent call will return the next number in the range.
 
-Inputs:
+Args:
     min -- minimum port number  [default = 0]
     max -- maximum port number  [default = 65536]
         '''
         self.min = min
         self.max = max
         self.first = -1
         self.current = -1
@@ -52,15 +52,15 @@
                 raise RuntimeError( 'Range exhausted' )
             return self.current
         return
 
 def randomport(min=1024, max=65536):
     '''select a random port number
 
-Inputs:
+Args:
     min -- minimum port number  [default = 1024]
     max -- maximum port number  [default = 65536]
     '''
     return portnumber(min, max)()
 
 
 if __name__ == '__main__':
```

### Comparing `pathos-0.3.0/pathos/pp.py` & `pathos-0.3.1/pathos/pp.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
 """
 ``pathos`` interface to the ``pp`` (parallel python) module.
 
 Notes:
```

### Comparing `pathos-0.3.0/pathos/pp_map.py` & `pathos-0.3.1/pathos/pp_map.py`

 * *Files 2% similar despite different names*

```diff
@@ -33,15 +33,15 @@
 # LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN
 # ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
 # POSSIBILITY OF SUCH DAMAGE.
 
 # Forked by: Mike McKerns (April 2008)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 minimal interface to python's ``pp`` (parallel python)  module
 
 Implements a work-alike of the builtin ``map`` function that distributes
 work across many processes.  As it uses ``ppft`` to do the
@@ -141,21 +141,19 @@
     # come available.
     return (subproc() for subproc in map(submit, *a))
 
 
 def pp_map(function, sequence, *args, **kwds):
     '''extend python's parallel map function to parallel python
 
-Inputs:
-    function  -- target function
-    sequence  -- sequence to process in parallel
-
-Additional Inputs:
-    ncpus     -- number of 'local' processors to use  [defaut = 'autodetect']
-    servers   -- available distributed parallel python servers  [default = ()]
+Args:
+    function - target function
+    sequence - sequence to process in parallel
+    ncpus - number of 'local' processors to use  [defaut = 'autodetect']
+    servers - available distributed parallel python servers  [default = ()]
     '''
     procs = None
     servers = ()
     if 'ncpus' in kwds:
       procs = kwds['ncpus']
       kwds.pop('ncpus')
     if 'servers' in kwds:
```

### Comparing `pathos-0.3.0/pathos/profile.py` & `pathos-0.3.1/pathos/profile.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 This module contains functions for profiling in other threads and processes.
 
 Functions for identifying a thread/process:
     process_id   - get the identifier (process id) for the current process
```

### Comparing `pathos-0.3.0/pathos/python.py` & `pathos-0.3.1/pathos/python.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
 """
 ``pathos`` interface to python's (serial) ``map`` functions
 
 Notes:
```

### Comparing `pathos-0.3.0/pathos/secure/connection.py` & `pathos-0.3.1/pathos/secure/connection.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
 # adapted from Mike McKerns' and June Kim's gsl SSHLauncher class
 """
 This module contains the derived class for secure shell (ssh) launchers
 See the following for an example.
```

### Comparing `pathos-0.3.0/pathos/secure/copier.py` & `pathos-0.3.1/pathos/secure/copier.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
 # adapted from Mike McKerns' gsl SCPLauncher class
 """
 This module contains the derived class for launching secure copy (scp)
 commands.  See the following for an example.
```

### Comparing `pathos-0.3.0/pathos/secure/tunnel.py` & `pathos-0.3.1/pathos/secure/tunnel.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
 # adapted from J. Kim & M. McKerns' Tunnel class
 """
 This module contains the base class for secure tunnel connections, and
 describes the pathos tunnel interface.  See the following for an example.
```

### Comparing `pathos-0.3.0/pathos/selector.py` & `pathos-0.3.1/pathos/selector.py`

 * *Files 0% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 #  <LicenseText>
 # 
 #  ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 # 
 # Forked by: Mike McKerns (November 2004)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2004-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 This module implements a selector class, which can be used to dispatch
 events and for event handler wrangling.
 
 """
```

### Comparing `pathos-0.3.0/pathos/serial.py` & `pathos-0.3.1/pathos/serial.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
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

### Comparing `pathos-0.3.0/pathos/server.py` & `pathos-0.3.1/pathos/server.py`

 * *Files 5% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 # <LicenseText>
 #
 # ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 #
 # Forked by: Mike McKerns (January 2004)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2004-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 This module contains the base class for pathos servers, and describes
 the pathos server interface.  If a third-party RPC server is selected,
 such as 'parallel python' (i.e. 'pp') or 'RPyC', direct calls to the
 third-party interface are currently used.
```

### Comparing `pathos-0.3.0/pathos/tests/__main__.py` & `pathos-0.3.1/pathos/tests/__main__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 import glob
 import os
 import sys
 import subprocess as sp
```

### Comparing `pathos-0.3.0/pathos/tests/test_decorate.py` & `pathos-0.3.1/pathos/tests/test_decorate.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 demonstrates pickle/source failure cases with decorators/factories and pp
 """
 
 def __wrap_nested(function, inner_function):
```

### Comparing `pathos-0.3.0/pathos/tests/test_join.py` & `pathos-0.3.1/pathos/tests/test_join.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 from pathos.parallel import *
 from pathos.multiprocessing import *
 from pathos.threading import *
```

### Comparing `pathos-0.3.0/pathos/tests/test_map.py` & `pathos-0.3.1/pathos/tests/test_map.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 import time
 
 verbose = False
 delay = 0.01
```

### Comparing `pathos-0.3.0/pathos/tests/test_maps.py` & `pathos-0.3.1/pathos/tests/test_maps.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 from pathos.maps import *
 from pathos.pools import _ThreadPool as Pool
 
 def squared(x):
```

### Comparing `pathos-0.3.0/pathos/tests/test_pp.py` & `pathos-0.3.1/pathos/tests/test_pp.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 from dill import source
 def run_source(obj):
     _obj = source._wrap(obj)
     assert _obj(1.57) == obj(1.57)
```

### Comparing `pathos-0.3.0/pathos/tests/test_star.py` & `pathos-0.3.1/pathos/tests/test_star.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 import time
 x = list(range(18))
 delay = 0.01
 items = 20
```

### Comparing `pathos-0.3.0/pathos/tests/test_with.py` & `pathos-0.3.1/pathos/tests/test_with.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 PRIMES = [
     112272535095293,
     112582705942171,
     112272535095293,
```

### Comparing `pathos-0.3.0/pathos/util.py` & `pathos-0.3.1/pathos/util.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
 # adapted from J. Kim & M. McKerns utility functions
 """
 utilities for distributed computing
 """
```

### Comparing `pathos-0.3.0/pathos/xmlrpc/server.py` & `pathos-0.3.1/pathos/xmlrpc/server.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 #
 # adapted from J. Kim's XMLRPC server and request handler classes
 """
 This module contains the base class for pathos XML-RPC servers,
 and derives from python's SimpleXMLRPCServer, and the base class
```

### Comparing `pathos-0.3.0/pathos.egg-info/PKG-INFO` & `pathos-0.3.1/pathos.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pathos
-Version: 0.3.0
+Version: 0.3.1
 Summary: parallel graph management and execution in heterogeneous computing
 Home-page: https://github.com/uqfoundation/pathos
 Download-URL: https://pypi.org/project/pathos/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
@@ -20,14 +20,15 @@
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
 License-File: LICENSE
 
@@ -58,19 +59,19 @@
 also enables a single code-base to be maintained instead of requiring
 parallel, serial, and distributed versions of a code. ``pathos`` maps can be
 nested, thus hierarchical heterogeneous computing is possible by merely
 selecting the desired hierarchy of ``map`` and ``pipe`` (``apply``) objects.
 
 The ``pathos`` framework is composed of several interoperating packages:
 
-    - ``dill``: a utility to serialize all of python
+    - ``dill``: serialize all of Python
     - ``pox``: utilities for filesystem exploration and automated builds
     - ``klepto``: persistent caching to memory, disk, or database
-    - ``multiprocess``: better multiprocessing and multithreading in python
-    - ``ppft``: distributed and parallel python
+    - ``multiprocess``: better multiprocessing and multithreading in Python
+    - ``ppft``: distributed and parallel Python
     - ``pyina``: MPI parallel ``map`` and cluster scheduling
     - ``pathos``: graph management and execution in heterogeneous computing
 
 
 About Pathos
 ============
 
@@ -93,39 +94,39 @@
 ``pathos`` provides distributed ``map`` and ``pipe`` algorithms, where a mix of
 local processors and distributed workers can be selected.  ``pathos``
 also provides a very basic automated load balancing service, as well as
 the ability for the user to directly select the resources.
 
 The high-level ``pool.map`` interface, yields a ``map`` implementation that
 hides the RPC internals from the user. With ``pool.map``, the user can launch
-their code in parallel, and as a distributed service, using standard python
+their code in parallel, and as a distributed service, using standard Python
 and without writing a line of server or parallel batch code.
 
 RPC servers and communication in general is known to be insecure.  However,
 instead of attempting to make the RPC communication itself secure, ``pathos``
 provides the ability to automatically wrap any distributes service or
 communication in a ssh-tunnel. Ssh is a universally trusted method.
 Using ssh-tunnels, ``pathos`` has launched several distributed calculations
 on national lab clusters, and to date has performed test calculations
 that utilize node-to-node communication between several national lab clusters
 and a user's laptop.  ``pathos`` allows the user to configure and launch
 at a very atomistic level, through raw access to ssh and scp. 
 
-``pathos`` is the core of a python framework for heterogeneous computing.
+``pathos`` is the core of a Python framework for heterogeneous computing.
 ``pathos`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pathos/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``pathos`` provides a configurable distributed parallel ``map`` interface
 to launching RPC service calls, with:
 
-    - a ``map`` interface that meets and extends the python ``map`` standard
+    - a ``map`` interface that meets and extends the Python ``map`` standard
     - the ability to submit service requests to a selection of servers
     - the ability to tunnel server communications with ssh
 
 The ``pathos`` core is built on low-level communication to remote hosts using
 ssh. The interface to ssh, scp, and ssh-tunneled connections can:
 
     - configure and launch remote processes with ssh
@@ -168,46 +169,45 @@
 Requirements
 ============
 
 ``pathos`` requires:
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
-    - ``pox``, **>=0.3.2**
-    - ``dill``, **>=0.3.6**
-    - ``ppft``, **>=1.7.6.6**
-    - ``multiprocess``, **>=0.70.14**
+    - ``pox``, **>=0.3.3**
+    - ``dill``, **>=0.3.7**
+    - ``ppft``, **>=1.7.6.7**
+    - ``multiprocess``, **>=0.70.15**
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
-http://pathos.rtfd.io. Also see ``pathos.tests`` and ``pathos.examples``
-for a set of scripts that demonstrate the configuration and launching of
-communications with ssh and scp, and demonstrate the configuration and
-execution of jobs in a hierarchical parallel workflow. You can run the test
-suite with ``python -m pathos.tests``. Tunnels and other connections to
-remote servers can be established with the ``pathos_connect`` script (or with
-``python -m pathos``). See ``pathos_connect --help`` for more information.
-``pathos`` also provides a ``portpicker`` script to select an open port
-(also available with ``python -m pathos.portpicker``). The source code is 
-generally well documented, so further questions may be resolved by inspecting
-the code itself.  Please feel free to submit a ticket on github, or ask a
-question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pathos`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+http://pathos.rtfd.io. Also see ``pathos.tests`` and https://github.com/uqfoundation/pathos/tree/master/examples for a set of scripts that demonstrate the
+configuration and launching of communications with ssh and scp, and demonstrate
+the configuration and execution of jobs in a hierarchical parallel workflow.
+You can run the test suite with ``python -m pathos.tests``. Tunnels and other
+connections to remote servers can be established with the ``pathos_connect``
+script (or with ``python -m pathos``). See ``pathos_connect --help`` for more
+information.  ``pathos`` also provides a ``portpicker`` script to select an
+open port (also available with ``python -m pathos.portpicker``). The source
+code is generally well documented, so further questions may be resolved by
+inspecting the code itself.  Please feel free to submit a ticket on github,
+or ask a question on stackoverflow (**@Mike McKerns**). If you would like to
+share how you use ``pathos`` in your work, please send an email (to **mmckerns
+at uqfoundation dot org**).
 
 Important classes and functions are found here:
 
     - ``pathos.abstract_launcher``           [the worker pool API definition]
     - ``pathos.pools``                       [all of the pathos worker pools]
     - ``pathos.core``                        [the high-level command interface] 
     - ``pathos.hosts``                       [the hostname registry interface] 
-    - ``pathos.serial.SerialPool``           [the serial python worker pool]
+    - ``pathos.serial.SerialPool``           [the serial Python worker pool]
     - ``pathos.parallel.ParallelPool``       [the parallelpython worker pool]
     - ``pathos.multiprocessing.ProcessPool`` [the multiprocessing worker pool]
     - ``pathos.threading.ThreadPool``        [the multithreading worker pool]
     - ``pathos.connection.Pipe``             [the launcher base class]
     - ``pathos.secure.Pipe``                 [the secure launcher base class]
     - ``pathos.secure.Copier``               [the secure copier  base class]
     - ``pathos.secure.Tunnel``               [the secure tunnel base class]
```

### Comparing `pathos-0.3.0/pathos.egg-info/SOURCES.txt` & `pathos-0.3.1/pathos.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -20,14 +20,15 @@
 docs/source/helpers.rst
 docs/source/index.rst
 docs/source/pathos.png
 docs/source/pathos.rst
 docs/source/scripts.rst
 docs/source/secure.rst
 docs/source/xmlrpc.rst
+docs/source/_static/css/custom.css
 examples/README
 examples/async_map.py
 examples/mp_class_example.py
 examples/nested.py
 examples/pp_map.py
 examples/secure_copy.py
 examples/secure_hello.py
@@ -98,13 +99,14 @@
 pathos/tests/__main__.py
 pathos/tests/test_decorate.py
 pathos/tests/test_join.py
 pathos/tests/test_map.py
 pathos/tests/test_maps.py
 pathos/tests/test_mp.py
 pathos/tests/test_pp.py
+pathos/tests/test_random.py
 pathos/tests/test_star.py
 pathos/tests/test_with.py
 pathos/xmlrpc/__init__.py
 pathos/xmlrpc/server.py
 scripts/pathos_connect
 scripts/portpicker
```

### Comparing `pathos-0.3.0/scripts/pathos_connect` & `pathos-0.3.1/scripts/pathos_connect`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 """
 connect to the specified machine and start a 'server', 'tunnel', or both
 
 Notes:
     Usage: pathos_connect [hostname] [server] [remoteport] [profile]
```

### Comparing `pathos-0.3.0/setup.py` & `pathos-0.3.1/setup.py`

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
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
 import os
 import sys
 # drop support for older python
 if sys.version_info < (3, 7):
@@ -62,14 +62,15 @@
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
     packages=['pathos','pathos.tests',\
               'pathos.helpers','pathos.secure','pathos.xmlrpc'],
@@ -84,20 +85,20 @@
 # force python-, abi-, and platform-specific naming of bdist_wheel
 class BinaryDistribution(Distribution):
     """Distribution which forces a binary package with platform name"""
     def has_ext_modules(foo):
         return True
 
 # define dependencies
-ppft_version = 'ppft>=1.7.6.6'
-dill_version = 'dill>=0.3.6'
-pox_version = 'pox>=0.3.2'
-mp_version = 'multiprocess>=0.70.14'
-pyina_version = 'pyina>=0.2.6'
-mystic_version = 'mystic>=0.3.9'
+ppft_version = 'ppft>=1.7.6.7'
+dill_version = 'dill>=0.3.7'
+pox_version = 'pox>=0.3.3'
+mp_version = 'multiprocess>=0.70.15'
+pyina_version = 'pyina>=0.2.7'
+mystic_version = 'mystic>=0.4.0'
 # add dependencies
 depend = [ppft_version, dill_version, pox_version, mp_version]
 extras = {'examples': [mystic_version, pyina_version]}
 # update setup kwds
 if has_setuptools:
     setup_kwds.update(
         zip_safe=False,
```

### Comparing `pathos-0.3.0/version.py` & `pathos-0.3.1/version.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pathos/blob/master/LICENSE
 
-__version__ = '0.3.0'
+__version__ = '0.3.1'
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

