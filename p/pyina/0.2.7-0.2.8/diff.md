# Comparing `tmp/pyina-0.2.7.tar.gz` & `tmp/pyina-0.2.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyina-0.2.7.tar", last modified: Mon Oct 24 03:26:24 2022, max compression
+gzip compressed data, was "pyina-0.2.8.tar", last modified: Sun Jul 23 13:45:53 2023, max compression
```

## Comparing `pyina-0.2.7.tar` & `pyina-0.2.8.tar`

### file list

```diff
@@ -1,81 +1,84 @@
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:26:24.560607 pyina-0.2.7/
--rw-r--r--   0 mmckerns   (501) staff       (20)      831 2022-05-16 23:11:05.000000 pyina-0.2.7/.codecov.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)      554 2022-05-16 23:11:05.000000 pyina-0.2.7/.coveragerc
--rw-r--r--   0 mmckerns   (501) staff       (20)       66 2018-04-13 18:06:07.000000 pyina-0.2.7/.gitignore
--rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-05-16 23:11:05.000000 pyina-0.2.7/.readthedocs.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1566 2022-07-02 19:28:11.000000 pyina-0.2.7/.travis.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2022-01-01 16:36:45.000000 pyina-0.2.7/LICENSE
--rw-r--r--   0 mmckerns   (501) staff       (20)      242 2022-10-23 20:18:03.000000 pyina-0.2.7/MANIFEST.in
--rw-r--r--   0 mmckerns   (501) staff       (20)     6908 2022-10-24 03:26:24.560826 pyina-0.2.7/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     6237 2022-10-24 03:04:47.000000 pyina-0.2.7/README.md
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:26:24.514792 pyina-0.2.7/docs/
--rw-r--r--   0 mmckerns   (501) staff       (20)      669 2022-05-16 23:11:05.000000 pyina-0.2.7/docs/Makefile
--rw-r--r--   0 mmckerns   (501) staff       (20)      430 2022-05-17 16:07:19.000000 pyina-0.2.7/docs/requirements.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:26:24.520181 pyina-0.2.7/docs/source/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7806 2022-07-07 20:25:24.000000 pyina-0.2.7/docs/source/conf.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      342 2017-08-23 21:00:09.000000 pyina-0.2.7/docs/source/index.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2017-08-11 19:09:35.000000 pyina-0.2.7/docs/source/pathos.png
--rw-r--r--   0 mmckerns   (501) staff       (20)     1747 2017-09-10 21:37:24.000000 pyina-0.2.7/docs/source/pyina.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)       22 2018-04-13 22:48:30.000000 pyina-0.2.7/docs/source/requirements.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)      350 2018-05-26 16:32:13.000000 pyina-0.2.7/docs/source/scripts.rst
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:26:24.538583 pyina-0.2.7/examples/
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2089 2022-01-01 16:47:47.000000 pyina-0.2.7/examples/hello_mpi4py.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      765 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/hello_pyina.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      899 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/machines_raw.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      631 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/mpd_trace.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3758 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/mpi_bcast.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1314 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/mpi_comm.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1182 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/mpi_simple.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1025 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/mpi_simple2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      579 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/nodes.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1373 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/pypi.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1415 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/pypi_pmap.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1487 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/test_ezmap.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      841 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/test_ezmap1.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1109 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/test_ezmap2.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      828 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/test_ezmap3.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      863 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/test_ezmap4.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1135 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/test_ezmap5.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      910 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/test_ezmap6.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      938 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/test_ezmap7.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      878 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/test_ezmap8.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2224 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/test_launch.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1194 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/test_pmap.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1390 2022-01-01 16:36:45.000000 pyina-0.2.7/examples/which.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:26:24.547663 pyina-0.2.7/pyina/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7770 2022-10-24 03:26:24.000000 pyina-0.2.7/pyina/__info__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1664 2022-07-07 20:27:26.000000 pyina-0.2.7/pyina/__init__.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     4121 2022-01-01 16:36:45.000000 pyina-0.2.7/pyina/__main__.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    14050 2022-10-20 22:03:42.000000 pyina-0.2.7/pyina/ez_map.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    25145 2022-01-01 16:36:45.000000 pyina-0.2.7/pyina/launchers.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1363 2022-01-01 16:36:45.000000 pyina-0.2.7/pyina/mappers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    13465 2022-10-20 22:10:41.000000 pyina-0.2.7/pyina/mpi.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6037 2022-06-29 17:40:32.000000 pyina-0.2.7/pyina/mpi_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3772 2022-01-01 16:36:45.000000 pyina-0.2.7/pyina/mpi_scatter.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    13165 2022-01-01 16:36:45.000000 pyina-0.2.7/pyina/schedulers.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:26:24.557753 pyina-0.2.7/pyina/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)      504 2022-01-01 16:36:45.000000 pyina-0.2.7/pyina/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      900 2022-07-09 11:11:12.000000 pyina-0.2.7/pyina/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2605 2022-10-20 20:02:29.000000 pyina-0.2.7/pyina/tests/test_ezmap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2022-01-01 16:36:45.000000 pyina-0.2.7/pyina/tests/test_map.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1530 2022-01-01 16:36:45.000000 pyina-0.2.7/pyina/tests/test_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      835 2022-01-01 16:36:45.000000 pyina-0.2.7/pyina/tests/test_simple.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4284 2022-01-01 16:36:45.000000 pyina-0.2.7/pyina/tests/test_star.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1633 2022-06-29 17:40:51.000000 pyina-0.2.7/pyina/tests/test_with.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     8080 2022-01-01 16:36:45.000000 pyina-0.2.7/pyina/tools.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:26:24.551098 pyina-0.2.7/pyina.egg-info/
--rw-r--r--   0 mmckerns   (501) staff       (20)     6908 2022-10-24 03:26:24.000000 pyina-0.2.7/pyina.egg-info/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     1461 2022-10-24 03:26:24.000000 pyina-0.2.7/pyina.egg-info/SOURCES.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-24 03:26:24.000000 pyina-0.2.7/pyina.egg-info/dependency_links.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-24 03:26:24.000000 pyina-0.2.7/pyina.egg-info/not-zip-safe
--rw-r--r--   0 mmckerns   (501) staff       (20)       68 2022-10-24 03:26:24.000000 pyina-0.2.7/pyina.egg-info/requires.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        6 2022-10-24 03:26:24.000000 pyina-0.2.7/pyina.egg-info/top_level.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)      308 2022-06-14 09:35:58.000000 pyina-0.2.7/pyproject.toml
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-24 03:26:24.559946 pyina-0.2.7/scripts/
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2141 2022-01-01 16:36:45.000000 pyina-0.2.7/scripts/ezpool
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2150 2022-01-01 16:36:45.000000 pyina-0.2.7/scripts/ezscatter
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1691 2022-01-01 16:36:45.000000 pyina-0.2.7/scripts/mpi_world
--rw-r--r--   0 mmckerns   (501) staff       (20)       62 2022-10-24 03:26:24.561812 pyina-0.2.7/setup.cfg
--rw-r--r--   0 mmckerns   (501) staff       (20)     5860 2022-10-24 03:23:04.000000 pyina-0.2.7/setup.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      304 2022-07-09 11:10:54.000000 pyina-0.2.7/tox.ini
--rw-r--r--   0 mmckerns   (501) staff       (20)     2732 2022-10-24 03:25:11.000000 pyina-0.2.7/version.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 13:45:53.903477 pyina-0.2.8/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      831 2022-05-16 23:11:05.000000 pyina-0.2.8/.codecov.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)      554 2022-05-16 23:11:05.000000 pyina-0.2.8/.coveragerc
+-rw-r--r--   0 mmckerns   (501) staff       (20)       66 2018-04-13 18:06:07.000000 pyina-0.2.8/.gitignore
+-rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-05-16 23:11:05.000000 pyina-0.2.8/.readthedocs.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1795 2023-07-07 03:30:52.000000 pyina-0.2.8/.travis.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2023-02-08 18:06:46.000000 pyina-0.2.8/LICENSE
+-rw-r--r--   0 mmckerns   (501) staff       (20)      242 2022-10-23 20:18:03.000000 pyina-0.2.8/MANIFEST.in
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6897 2023-07-23 13:45:53.903732 pyina-0.2.8/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6310 2023-07-23 11:29:34.000000 pyina-0.2.8/README.md
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 13:45:53.830741 pyina-0.2.8/docs/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      669 2022-05-16 23:11:05.000000 pyina-0.2.8/docs/Makefile
+-rw-r--r--   0 mmckerns   (501) staff       (20)      430 2023-07-22 01:40:55.000000 pyina-0.2.8/docs/requirements.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 13:45:53.837161 pyina-0.2.8/docs/source/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 13:45:53.818363 pyina-0.2.8/docs/source/_static/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 13:45:53.838033 pyina-0.2.8/docs/source/_static/css/
+-rw-r--r--   0 mmckerns   (501) staff       (20)       85 2023-07-05 04:41:16.000000 pyina-0.2.8/docs/source/_static/css/custom.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8395 2023-07-05 04:59:12.000000 pyina-0.2.8/docs/source/conf.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      307 2023-07-05 05:54:41.000000 pyina-0.2.8/docs/source/index.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2017-08-11 19:09:35.000000 pyina-0.2.8/docs/source/pathos.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)      769 2023-02-05 00:23:45.000000 pyina-0.2.8/docs/source/pyina.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)       22 2018-04-13 22:48:30.000000 pyina-0.2.8/docs/source/requirements.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)      356 2023-02-05 00:25:07.000000 pyina-0.2.8/docs/source/scripts.rst
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 13:45:53.866183 pyina-0.2.8/examples/
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2089 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/hello_mpi4py.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      765 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/hello_pyina.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      899 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/machines_raw.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      631 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/mpd_trace.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3758 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/mpi_bcast.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1314 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/mpi_comm.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1182 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/mpi_simple.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1025 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/mpi_simple2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      579 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/nodes.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1373 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/pypi.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1415 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/pypi_pmap.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1487 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/test_ezmap.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      841 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/test_ezmap1.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1109 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/test_ezmap2.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      828 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/test_ezmap3.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      863 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/test_ezmap4.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1135 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/test_ezmap5.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      910 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/test_ezmap6.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      938 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/test_ezmap7.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      878 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/test_ezmap8.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2224 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/test_launch.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1194 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/test_pmap.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1390 2023-01-01 14:49:46.000000 pyina-0.2.8/examples/which.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 13:45:53.880475 pyina-0.2.8/pyina/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7708 2023-07-23 13:45:53.000000 pyina-0.2.8/pyina/__info__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1664 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/__init__.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     4121 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/__main__.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    14050 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/ez_map.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    25145 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/launchers.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1363 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/mappers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13465 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/mpi.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6037 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/mpi_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3772 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/mpi_scatter.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    13165 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/schedulers.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 13:45:53.899833 pyina-0.2.8/pyina/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      504 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      900 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2605 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/tests/test_ezmap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/tests/test_map.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1530 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/tests/test_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      835 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/tests/test_simple.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4284 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/tests/test_star.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1633 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/tests/test_with.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     8080 2023-01-01 14:49:46.000000 pyina-0.2.8/pyina/tools.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 13:45:53.889656 pyina-0.2.8/pyina.egg-info/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6897 2023-07-23 13:45:53.000000 pyina-0.2.8/pyina.egg-info/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1496 2023-07-23 13:45:53.000000 pyina-0.2.8/pyina.egg-info/SOURCES.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-23 13:45:53.000000 pyina-0.2.8/pyina.egg-info/dependency_links.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-23 13:45:53.000000 pyina-0.2.8/pyina.egg-info/not-zip-safe
+-rw-r--r--   0 mmckerns   (501) staff       (20)       68 2023-07-23 13:45:53.000000 pyina-0.2.8/pyina.egg-info/requires.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        6 2023-07-23 13:45:53.000000 pyina-0.2.8/pyina.egg-info/top_level.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)      308 2022-06-14 09:35:58.000000 pyina-0.2.8/pyproject.toml
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 13:45:53.902803 pyina-0.2.8/scripts/
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2141 2023-01-01 14:49:46.000000 pyina-0.2.8/scripts/ezpool
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2150 2023-01-01 14:49:46.000000 pyina-0.2.8/scripts/ezscatter
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1691 2023-01-01 14:49:46.000000 pyina-0.2.8/scripts/mpi_world
+-rw-r--r--   0 mmckerns   (501) staff       (20)       62 2023-07-23 13:45:53.904826 pyina-0.2.8/setup.cfg
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5910 2023-07-23 11:29:42.000000 pyina-0.2.8/setup.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      336 2023-07-07 03:29:42.000000 pyina-0.2.8/tox.ini
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3170 2023-07-23 13:37:49.000000 pyina-0.2.8/version.py
```

### Comparing `pyina-0.2.7/.codecov.yml` & `pyina-0.2.8/.codecov.yml`

 * *Files identical despite different names*

### Comparing `pyina-0.2.7/.coveragerc` & `pyina-0.2.8/.coveragerc`

 * *Files identical despite different names*

### Comparing `pyina-0.2.7/.travis.yml` & `pyina-0.2.8/.travis.yml`

 * *Files 27% similar despite different names*

```diff
@@ -11,27 +11,39 @@
 
         - python: '3.9'
           env:
             - COVERAGE="true"
 
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

### Comparing `pyina-0.2.7/LICENSE` & `pyina-0.2.8/LICENSE`

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

### Comparing `pyina-0.2.7/PKG-INFO` & `pyina-0.2.8/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyina
-Version: 0.2.7
+Version: 0.2.8
 Summary: MPI parallel map and cluster scheduling
 Home-page: https://github.com/uqfoundation/pyina
 Download-URL: https://pypi.org/project/pyina/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
@@ -19,14 +19,15 @@
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
 
@@ -46,37 +47,37 @@
 ``pyina`` currently provides two strategies for executing the parallel-map,
 where a strategy is the algorithm for distributing the work list of
 jobs across the availble nodes.  These strategies can be used *"in-the-raw"*
 (i.e. directly) to provide the map algorithm to a user's own mpi-aware code.
 Further, in ``pyina.mpi`` ``pyina`` provides pipe and map implementations
 (known as *"easy map"*) that hide the MPI internals from the user. With the
 *"easy map"*, the user can launch their code in parallel batch mode -- using
-standard python and without ever having to write a line of MPI code.
+standard Python and without ever having to write a line of MPI code.
 
 There are several ways that a user would typically launch their code in
 parallel -- directly with ``mpirun`` or ``mpiexec``, or through the use of a
 scheduler such as *torque* or *slurm*. ``pyina`` encapsulates several of these
 *"launchers"*, and provides a common interface to the different methods of
 launching a MPI job.
 
-``pyina`` is part of ``pathos``, a python framework for heterogeneous computing.
+``pyina`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``pyina`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pyina/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``pyina`` provides a highly configurable parallel map interface
 to running MPI jobs, with:
 
-    - a map interface that extends the python ``map`` standard
+    - a map interface that extends the Python ``map`` standard
     - the ability to submit batch jobs to a selection of schedulers
     - the ability to customize node and process launch configurations
-    - the ability to launch parallel MPI jobs with standard python
+    - the ability to launch parallel MPI jobs with standard Python
     - ease in selecting different strategies for processing a work list
 
 
 Current Release
 ===============
 
 The latest released version of ``pyina`` is available at:
@@ -114,35 +115,33 @@
 ``pyina`` requires:
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
     - ``cython``, **>=0.29.30**
     - ``numpy``, **>=1.0**
     - ``mpi4py``, **>=1.3**
-    - ``dill``, **>=0.3.6**
-    - ``pox``, **>=0.3.2**
-    - ``pathos``, **>=0.3.0**
+    - ``dill``, **>=0.3.7**
+    - ``pox``, **>=0.3.3**
+    - ``pathos``, **>=0.3.1**
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
-http://pyina.rtfd.io. Also see ``pyina.examples`` and ``pyina.tests``
-for a set of scripts that demonstrate the configuration and launching of
-mpi-based parallel jobs using the *"easy map"* interface. Also see
-``pyina.examples_other`` for a set of scripts that test the more raw
-internals of ``pyina``. You can run the tests with ``python -m pyina.tests``.
-A script is included for querying, setting up, and tearing down an MPI
-environment, see ``python -m pyina`` for more information. The source code
-is generally well documented, so further questions may be resolved by
-inspecting the code itself. Please feel free to submit a ticket on github,
-or ask a question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pyina`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+http://pyina.rtfd.io. Also see https://github.com/uqfoundation/pyina/tree/master/examples and ``pyina.tests`` for a set of scripts that demonstrate the
+configuration and launching of mpi-based parallel jobs using the *"easy map"*
+interface. You can run the tests with ``python -m pyina.tests``. A script is
+included for querying, setting up, and tearing down an MPI environment, see
+``python -m pyina`` for more information. The source code is generally well
+documented, so further questions may be resolved by inspecting the code itself.
+Please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``pyina`` in your work, please send an email (to **mmckerns at uqfoundation dot
+org**).
 
 Important classes and functions are found here:
 
     - ``pyina.mpi``           [the map API definition]
     - ``pyina.schedulers``    [all available schedulers] 
     - ``pyina.launchers``     [all available launchers]
```

### Comparing `pyina-0.2.7/README.md` & `pyina-0.2.8/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -13,41 +13,42 @@
 ``pyina`` currently provides two strategies for executing the parallel-map,
 where a strategy is the algorithm for distributing the work list of
 jobs across the availble nodes.  These strategies can be used *"in-the-raw"*
 (i.e. directly) to provide the map algorithm to a user's own mpi-aware code.
 Further, in ``pyina.mpi`` ``pyina`` provides pipe and map implementations
 (known as *"easy map"*) that hide the MPI internals from the user. With the
 *"easy map"*, the user can launch their code in parallel batch mode -- using
-standard python and without ever having to write a line of MPI code.
+standard Python and without ever having to write a line of MPI code.
 
 There are several ways that a user would typically launch their code in
 parallel -- directly with ``mpirun`` or ``mpiexec``, or through the use of a
 scheduler such as *torque* or *slurm*. ``pyina`` encapsulates several of these
 *"launchers"*, and provides a common interface to the different methods of
 launching a MPI job.
 
-``pyina`` is part of ``pathos``, a python framework for heterogeneous computing.
+``pyina`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``pyina`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pyina/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 --------------
 ``pyina`` provides a highly configurable parallel map interface
 to running MPI jobs, with:
 
-* a map interface that extends the python ``map`` standard
+* a map interface that extends the Python ``map`` standard
 * the ability to submit batch jobs to a selection of schedulers
 * the ability to customize node and process launch configurations
-* the ability to launch parallel MPI jobs with standard python
+* the ability to launch parallel MPI jobs with standard Python
 * ease in selecting different strategies for processing a work list
 
 
 Current Release
 [![Downloads](https://static.pepy.tech/personalized-badge/pyina?period=total&units=international_system&left_color=grey&right_color=blue&left_text=pypi%20downloads)](https://pepy.tech/project/pyina)
+[![Stack Overflow](https://img.shields.io/badge/stackoverflow-get%20help-black.svg)](https://stackoverflow.com/questions/tagged/pyina)
 ---------------
 The latest released version of ``pyina`` is available at:
     https://pypi.org/project/pyina
 
 ``pyina`` is distributed under a 3-clause BSD license.
 
 
@@ -79,34 +80,32 @@
 ``pyina`` requires:
 
 * ``python`` (or ``pypy``), **>=3.7**
 * ``setuptools``, **>=42**
 * ``cython``, **>=0.29.30**
 * ``numpy``, **>=1.0**
 * ``mpi4py``, **>=1.3**
-* ``dill``, **>=0.3.6**
-* ``pox``, **>=0.3.2**
-* ``pathos``, **>=0.3.0**
+* ``dill``, **>=0.3.7**
+* ``pox``, **>=0.3.3**
+* ``pathos``, **>=0.3.1**
 
 
 More Information
 ----------------
 Probably the best way to get started is to look at the documentation at
-http://pyina.rtfd.io. Also see ``pyina.examples`` and ``pyina.tests``
-for a set of scripts that demonstrate the configuration and launching of
-mpi-based parallel jobs using the *"easy map"* interface. Also see
-``pyina.examples_other`` for a set of scripts that test the more raw
-internals of ``pyina``. You can run the tests with ``python -m pyina.tests``.
-A script is included for querying, setting up, and tearing down an MPI
-environment, see ``python -m pyina`` for more information. The source code
-is generally well documented, so further questions may be resolved by
-inspecting the code itself. Please feel free to submit a ticket on github,
-or ask a question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pyina`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+http://pyina.rtfd.io. Also see https://github.com/uqfoundation/pyina/tree/master/examples and ``pyina.tests`` for a set of scripts that demonstrate the
+configuration and launching of mpi-based parallel jobs using the *"easy map"*
+interface. You can run the tests with ``python -m pyina.tests``. A script is
+included for querying, setting up, and tearing down an MPI environment, see
+``python -m pyina`` for more information. The source code is generally well
+documented, so further questions may be resolved by inspecting the code itself.
+Please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``pyina`` in your work, please send an email (to **mmckerns at uqfoundation dot
+org**).
 
 Important classes and functions are found here:
 
 * ``pyina.mpi``           [the map API definition]
 * ``pyina.schedulers``    [all available schedulers] 
 * ``pyina.launchers``     [all available launchers]
```

### Comparing `pyina-0.2.7/docs/Makefile` & `pyina-0.2.8/docs/Makefile`

 * *Files identical despite different names*

### Comparing `pyina-0.2.7/docs/source/conf.py` & `pyina-0.2.8/docs/source/conf.py`

 * *Files 8% similar despite different names*

```diff
@@ -70,24 +70,42 @@
 # source_suffix = ['.rst', '.md']
 source_suffix = '.rst'
 
 # The master toctree document.
 master_doc = 'index'
 
 # General information about the project.
-project = u'pyina'
+project = 'pyina'
 year = datetime.now().year
-copyright = u'%d, The Uncertainty Quantification Foundation' % year
-author = u'Mike McKerns'
+copyright = '%d, The Uncertainty Quantification Foundation' % year
+author = 'Mike McKerns'
 
 # extension config
 github_project_url = "https://github.com/uqfoundation/pyina"
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
@@ -99,15 +117,15 @@
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
@@ -127,57 +145,63 @@
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
     'github_repo': 'pyina',
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
 htmlhelp_basename = 'pyinadoc'
 
 # Logo for sidebar
@@ -204,45 +228,45 @@
     # 'figure_align': 'htbp',
 }
 
 # Grouping the document tree into LaTeX files. List of tuples
 # (source start file, target name, title,
 #  author, documentclass [howto, manual, or own class]).
 latex_documents = [
-    (master_doc, 'pyina.tex', u'pyina Documentation',
-     u'Mike McKerns', 'manual'),
+    (master_doc, 'pyina.tex', 'pyina Documentation',
+     'Mike McKerns', 'manual'),
 ]
 
 
 # -- Options for manual page output ---------------------------------------
 
 # One entry per manual page. List of tuples
 # (source start file, name, description, authors, manual section).
 man_pages = [
-    (master_doc, 'pyina', u'pyina Documentation',
+    (master_doc, 'pyina', 'pyina Documentation',
      [author], 1)
 ]
 
 
 # -- Options for Texinfo output -------------------------------------------
 
 # Grouping the document tree into Texinfo files. List of tuples
 # (source start file, target name, title, author,
 #  dir menu entry, description, category)
 texinfo_documents = [
-    (master_doc, 'pyina', u'pyina Documentation',
+    (master_doc, 'pyina', 'pyina Documentation',
      author, 'pyina', 'MPI parallel map and cluser scheduling.',
      'Miscellaneous'),
 ]
 
 
 
 
 # Example configuration for intersphinx: refer to the Python standard library.
-intersphinx_mapping = {'https://docs.python.org/': None}
+intersphinx_mapping = {'https://docs.python.org/3/': None}
 #    {'python': {'https://docs.python.org/': None},
 #     'mystic': {'https://mystic.readthedocs.io/en/latest/', None},
 #     'pathos': {'https://pathos.readthedocs.io/en/latest/', None},
 #     'pox': {'https://pox.readthedocs.io/en/latest/', None},
 #     'dill': {'https://dill.readthedocs.io/en/latest/', None},
 #     'multiprocess': {'https://multiprocess.readthedocs.io/en/latest/', None},
 #     'ppft': {'https://ppft.readthedocs.io/en/latest/', None},
```

### Comparing `pyina-0.2.7/docs/source/pathos.png` & `pyina-0.2.8/docs/source/pathos.png`

 * *Files identical despite different names*

### Comparing `pyina-0.2.7/examples/hello_mpi4py.py` & `pyina-0.2.8/examples/hello_mpi4py.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 #
 # original source code modifed from mpi4py-1.3.1/demo/helloworld.py
 # helloworld.py: Copyright (c) 2013, Lisandro Dalcin.
 # helloworld.py: All rights reserved.
 """
```

### Comparing `pyina-0.2.7/examples/hello_pyina.py` & `pyina-0.2.8/examples/hello_pyina.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 __doc__ = """
 # get pyina to say 'hello'
 # To run:
```

### Comparing `pyina-0.2.7/examples/machines_raw.py` & `pyina-0.2.8/examples/machines_raw.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 __doc__ = """
 # print rank - hostname info
 # To run:
```

### Comparing `pyina-0.2.7/examples/mpd_trace.py` & `pyina-0.2.8/examples/mpd_trace.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 run some basic tests of the MPI installation
 """
 
 import subprocess
```

### Comparing `pyina-0.2.7/examples/mpi_bcast.py` & `pyina-0.2.8/examples/mpi_bcast.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 doc = """
 A basic demonstration of low-level MPI communication.
 
 To launch:
```

### Comparing `pyina-0.2.7/examples/mpi_comm.py` & `pyina-0.2.8/examples/mpi_comm.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 # simple test of mpi communication
 # To run:
 
 mpiexec -np 4 `which python` test_comm.py
```

### Comparing `pyina-0.2.7/examples/mpi_simple.py` & `pyina-0.2.8/examples/mpi_simple.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 # Testing pyina.mpi.world.recv
 # To run:
 
 mpiexec -np 4 `which python` mpi_simple.py
```

### Comparing `pyina-0.2.7/examples/mpi_simple2.py` & `pyina-0.2.8/examples/mpi_simple2.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 # Testing pyina.mpi.world.bcast
 # To run:
 
 mpiexec -np 4 `which python` mpi_simple2.py
```

### Comparing `pyina-0.2.7/examples/nodes.py` & `pyina-0.2.8/examples/nodes.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 __doc__ = """
 # get all nodes to report
 # To run:
```

### Comparing `pyina-0.2.7/examples/pypi.py` & `pyina-0.2.8/examples/pypi.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 __doc__ = """
 # The standard MPI example, computes the integral 
 # 
 # Integrate[4/(1+x^2),{x,0,1}]
```

### Comparing `pyina-0.2.7/examples/pypi_pmap.py` & `pyina-0.2.8/examples/pypi_pmap.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 __doc__ = """
 # The standard MPI example, computes the integral 
 # 
 # Integrate[4/(1+x^2),{x,0,1}]
```

### Comparing `pyina-0.2.7/examples/test_ezmap.py` & `pyina-0.2.8/examples/test_ezmap.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from pyina.launchers import MpiScatter, MpiPool
 
 def host(id):
     import socket
```

### Comparing `pyina-0.2.7/examples/test_ezmap1.py` & `pyina-0.2.8/examples/test_ezmap1.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from pyina.launchers import MpiScatter
 
 def host(id):
     import socket
```

### Comparing `pyina-0.2.7/examples/test_ezmap2.py` & `pyina-0.2.8/examples/test_ezmap2.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from pyina.launchers import MpiScatter, MpiPool
 
 def play(Q):
     id, l = Q
```

### Comparing `pyina-0.2.7/examples/test_ezmap3.py` & `pyina-0.2.8/examples/test_ezmap3.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from pyina.launchers import Mpi
 
 def host(id):
     import socket
```

### Comparing `pyina-0.2.7/examples/test_ezmap4.py` & `pyina-0.2.8/examples/test_ezmap4.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from pyina.launchers import Mpi
 
 #XXX: should not have to define "func" within mapped function
 #from mystic.models import rosen as func
```

### Comparing `pyina-0.2.7/examples/test_ezmap5.py` & `pyina-0.2.8/examples/test_ezmap5.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from pyina.launchers import Mpi
 
 #XXX:: can fail with NameError: global name 'func' is not defined
 #XXX:: can fail with RuntimeError: maximum recursion depth exceeded
```

### Comparing `pyina-0.2.7/examples/test_ezmap6.py` & `pyina-0.2.8/examples/test_ezmap6.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from pyina.launchers import SerialMapper
 from pyina.schedulers import Torque
 from pyina.mpi import _save, _debug
```

### Comparing `pyina-0.2.7/examples/test_ezmap7.py` & `pyina-0.2.8/examples/test_ezmap7.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from pyina.launchers import Mpi
 from pyina.schedulers import Torque
 from pyina.mpi import _save, _debug
```

### Comparing `pyina-0.2.7/examples/test_ezmap8.py` & `pyina-0.2.8/examples/test_ezmap8.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from pyina.launchers import TorqueMpiPool as Launcher
 from pyina.mpi import _save, _debug
 
 #_debug(True)
```

### Comparing `pyina-0.2.7/examples/test_launch.py` & `pyina-0.2.8/examples/test_launch.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from pyina.mpi import defaults
 from pyina.launchers import SerialMapper, Mpi, TorqueMpi
 from pyina.launchers import all_launches
 from pyina.schedulers import Torque
```

### Comparing `pyina-0.2.7/examples/test_pmap.py` & `pyina-0.2.8/examples/test_pmap.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 doc = """
 # Tests parallel, master-worker. Version 0
 # To run:  (use #nodes >= 2)
```

### Comparing `pyina-0.2.7/examples/which.py` & `pyina-0.2.8/examples/which.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 __doc__ = """
 # check which python mpirun is executing
 # To run (in parallel):
```

### Comparing `pyina-0.2.7/pyina/__info__.py` & `pyina-0.2.8/pyina/__info__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 '''
 ----------------------------------------------
 pyina: MPI parallel map and cluster scheduling
 ----------------------------------------------
 
@@ -21,37 +21,37 @@
 ``pyina`` currently provides two strategies for executing the parallel-map,
 where a strategy is the algorithm for distributing the work list of
 jobs across the availble nodes.  These strategies can be used *"in-the-raw"*
 (i.e. directly) to provide the map algorithm to a user's own mpi-aware code.
 Further, in ``pyina.mpi`` ``pyina`` provides pipe and map implementations
 (known as *"easy map"*) that hide the MPI internals from the user. With the
 *"easy map"*, the user can launch their code in parallel batch mode -- using
-standard python and without ever having to write a line of MPI code.
+standard Python and without ever having to write a line of MPI code.
 
 There are several ways that a user would typically launch their code in
 parallel -- directly with ``mpirun`` or ``mpiexec``, or through the use of a
 scheduler such as *torque* or *slurm*. ``pyina`` encapsulates several of these
 *"launchers"*, and provides a common interface to the different methods of
 launching a MPI job.
 
-``pyina`` is part of ``pathos``, a python framework for heterogeneous computing.
+``pyina`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``pyina`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pyina/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``pyina`` provides a highly configurable parallel map interface
 to running MPI jobs, with:
 
-    - a map interface that extends the python ``map`` standard
+    - a map interface that extends the Python ``map`` standard
     - the ability to submit batch jobs to a selection of schedulers
     - the ability to customize node and process launch configurations
-    - the ability to launch parallel MPI jobs with standard python
+    - the ability to launch parallel MPI jobs with standard Python
     - ease in selecting different strategies for processing a work list
 
 
 Current Release
 ===============
 
 The latest released version of ``pyina`` is available at:
@@ -89,35 +89,33 @@
 ``pyina`` requires:
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
     - ``cython``, **>=0.29.30**
     - ``numpy``, **>=1.0**
     - ``mpi4py``, **>=1.3**
-    - ``dill``, **>=0.3.6**
-    - ``pox``, **>=0.3.2**
-    - ``pathos``, **>=0.3.0**
+    - ``dill``, **>=0.3.7**
+    - ``pox``, **>=0.3.3**
+    - ``pathos``, **>=0.3.1**
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
-http://pyina.rtfd.io. Also see ``pyina.examples`` and ``pyina.tests``
-for a set of scripts that demonstrate the configuration and launching of
-mpi-based parallel jobs using the *"easy map"* interface. Also see
-``pyina.examples_other`` for a set of scripts that test the more raw
-internals of ``pyina``. You can run the tests with ``python -m pyina.tests``.
-A script is included for querying, setting up, and tearing down an MPI
-environment, see ``python -m pyina`` for more information. The source code
-is generally well documented, so further questions may be resolved by
-inspecting the code itself. Please feel free to submit a ticket on github,
-or ask a question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pyina`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+http://pyina.rtfd.io. Also see https://github.com/uqfoundation/pyina/tree/master/examples and ``pyina.tests`` for a set of scripts that demonstrate the
+configuration and launching of mpi-based parallel jobs using the *"easy map"*
+interface. You can run the tests with ``python -m pyina.tests``. A script is
+included for querying, setting up, and tearing down an MPI environment, see
+``python -m pyina`` for more information. The source code is generally well
+documented, so further questions may be resolved by inspecting the code itself.
+Please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``pyina`` in your work, please send an email (to **mmckerns at uqfoundation dot
+org**).
 
 Important classes and functions are found here:
 
     - ``pyina.mpi``           [the map API definition]
     - ``pyina.schedulers``    [all available schedulers] 
     - ``pyina.launchers``     [all available launchers] 
 
@@ -155,36 +153,36 @@
     https://uqfoundation.github.io/project/pathos
 
 Please see https://uqfoundation.github.io/project/pathos or
 http://arxiv.org/pdf/1202.1056 for further information.
 
 '''
 
-__version__ = '0.2.7'
+__version__ = '0.2.8'
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

### Comparing `pyina-0.2.7/pyina/__init__.py` & `pyina-0.2.8/pyina/__init__.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 # author, version, license, and long description
 try: # the package is installed
     from .__info__ import __version__, __author__, __doc__, __license__
 except: # pragma: no cover
```

### Comparing `pyina-0.2.7/pyina/__main__.py` & `pyina-0.2.8/pyina/__main__.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 #
 # helper script to setup your mpi environment
 
 __doc__ = """
 setup/query/kill the MPI environment
```

### Comparing `pyina-0.2.7/pyina/ez_map.py` & `pyina-0.2.8/pyina/ez_map.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 The ez_map function is a helper to parallel_map to further
 simplify parallel programming.  Primarily ez_map provides
 a standard interface for parallel_map, and facilitates
 running parallel jobs with serial python.
```

### Comparing `pyina-0.2.7/pyina/launchers.py` & `pyina-0.2.8/pyina/launchers.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 This module contains prepared launchers for parallel execution, including
 bindings to some common combinations of launchers and schedulers.
 
 Base classes:
```

### Comparing `pyina-0.2.7/pyina/mappers.py` & `pyina-0.2.8/pyina/mappers.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 tiny function wrapper to make ez_map interface for mappers more standard
 
 provides:
  mapper_str = mapper()  interface
```

### Comparing `pyina-0.2.7/pyina/mpi.py` & `pyina-0.2.8/pyina/mpi.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 This module contains the base of map and pipe interfaces to the mpi4py module.
 
 Pipe methods provided:
     ???
```

### Comparing `pyina-0.2.7/pyina/mpi_pool.py` & `pyina-0.2.8/pyina/mpi_pool.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from mpi4py import MPI as mpi
 import dill
 try:
     getattr(mpi,'pickle',getattr(mpi,'_p_pickle',None)).dumps = dill.dumps
```

### Comparing `pyina-0.2.7/pyina/mpi_scatter.py` & `pyina-0.2.8/pyina/mpi_scatter.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from mpi4py import MPI as mpi
 import dill
 try:
     getattr(mpi,'pickle',getattr(mpi,'_p_pickle',None)).dumps = dill.dumps
```

### Comparing `pyina-0.2.7/pyina/schedulers.py` & `pyina-0.2.8/pyina/schedulers.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 This module contains bindings to some common schedulers.
 
 Base classes:
     Scheduler      - base class for cpu cluster scheduling
```

### Comparing `pyina-0.2.7/pyina/tests/__main__.py` & `pyina-0.2.8/pyina/tests/__main__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 import glob
 import os
 import sys
 import subprocess as sp
```

### Comparing `pyina-0.2.7/pyina/tests/test_ezmap.py` & `pyina-0.2.8/pyina/tests/test_ezmap.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 # old-style maps (deprecated)
 
 import time
```

### Comparing `pyina-0.2.7/pyina/tests/test_map.py` & `pyina-0.2.8/pyina/tests/test_map.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 verbose = False
 delay = 0.01
 items = 100
```

### Comparing `pyina-0.2.7/pyina/tests/test_pool.py` & `pyina-0.2.8/pyina/tests/test_pool.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from dill import source, temp
 def run_source(obj):
     _obj = source._wrap(obj)
     assert _obj(1.57) == obj(1.57)
```

### Comparing `pyina-0.2.7/pyina/tests/test_simple.py` & `pyina-0.2.8/pyina/tests/test_simple.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 1997-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 # construct a target function
 def host(id):
     import socket
     return "Rank: %d -- %s" % (id, socket.gethostname())
```

### Comparing `pyina-0.2.7/pyina/tests/test_star.py` & `pyina-0.2.8/pyina/tests/test_star.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 import time
 
 x = range(18)
 delay = 0.01
```

### Comparing `pyina-0.2.7/pyina/tests/test_with.py` & `pyina-0.2.8/pyina/tests/test_with.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 from time import sleep
 
 
 PRIMES = [
```

### Comparing `pyina-0.2.7/pyina/tools.py` & `pyina-0.2.8/pyina/tools.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 Various mpi python tools
 
 Main function exported are::
     - ensure_mpi: make sure the script is called by mpi-enabled python
```

### Comparing `pyina-0.2.7/pyina.egg-info/PKG-INFO` & `pyina-0.2.8/pyina.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyina
-Version: 0.2.7
+Version: 0.2.8
 Summary: MPI parallel map and cluster scheduling
 Home-page: https://github.com/uqfoundation/pyina
 Download-URL: https://pypi.org/project/pyina/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
@@ -19,14 +19,15 @@
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
 
@@ -46,37 +47,37 @@
 ``pyina`` currently provides two strategies for executing the parallel-map,
 where a strategy is the algorithm for distributing the work list of
 jobs across the availble nodes.  These strategies can be used *"in-the-raw"*
 (i.e. directly) to provide the map algorithm to a user's own mpi-aware code.
 Further, in ``pyina.mpi`` ``pyina`` provides pipe and map implementations
 (known as *"easy map"*) that hide the MPI internals from the user. With the
 *"easy map"*, the user can launch their code in parallel batch mode -- using
-standard python and without ever having to write a line of MPI code.
+standard Python and without ever having to write a line of MPI code.
 
 There are several ways that a user would typically launch their code in
 parallel -- directly with ``mpirun`` or ``mpiexec``, or through the use of a
 scheduler such as *torque* or *slurm*. ``pyina`` encapsulates several of these
 *"launchers"*, and provides a common interface to the different methods of
 launching a MPI job.
 
-``pyina`` is part of ``pathos``, a python framework for heterogeneous computing.
+``pyina`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``pyina`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/pyina/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``pyina`` provides a highly configurable parallel map interface
 to running MPI jobs, with:
 
-    - a map interface that extends the python ``map`` standard
+    - a map interface that extends the Python ``map`` standard
     - the ability to submit batch jobs to a selection of schedulers
     - the ability to customize node and process launch configurations
-    - the ability to launch parallel MPI jobs with standard python
+    - the ability to launch parallel MPI jobs with standard Python
     - ease in selecting different strategies for processing a work list
 
 
 Current Release
 ===============
 
 The latest released version of ``pyina`` is available at:
@@ -114,35 +115,33 @@
 ``pyina`` requires:
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
     - ``cython``, **>=0.29.30**
     - ``numpy``, **>=1.0**
     - ``mpi4py``, **>=1.3**
-    - ``dill``, **>=0.3.6**
-    - ``pox``, **>=0.3.2**
-    - ``pathos``, **>=0.3.0**
+    - ``dill``, **>=0.3.7**
+    - ``pox``, **>=0.3.3**
+    - ``pathos``, **>=0.3.1**
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
-http://pyina.rtfd.io. Also see ``pyina.examples`` and ``pyina.tests``
-for a set of scripts that demonstrate the configuration and launching of
-mpi-based parallel jobs using the *"easy map"* interface. Also see
-``pyina.examples_other`` for a set of scripts that test the more raw
-internals of ``pyina``. You can run the tests with ``python -m pyina.tests``.
-A script is included for querying, setting up, and tearing down an MPI
-environment, see ``python -m pyina`` for more information. The source code
-is generally well documented, so further questions may be resolved by
-inspecting the code itself. Please feel free to submit a ticket on github,
-or ask a question on stackoverflow (**@Mike McKerns**).
-If you would like to share how you use ``pyina`` in your work, please send
-an email (to **mmckerns at uqfoundation dot org**).
+http://pyina.rtfd.io. Also see https://github.com/uqfoundation/pyina/tree/master/examples and ``pyina.tests`` for a set of scripts that demonstrate the
+configuration and launching of mpi-based parallel jobs using the *"easy map"*
+interface. You can run the tests with ``python -m pyina.tests``. A script is
+included for querying, setting up, and tearing down an MPI environment, see
+``python -m pyina`` for more information. The source code is generally well
+documented, so further questions may be resolved by inspecting the code itself.
+Please feel free to submit a ticket on github, or ask a question on
+stackoverflow (**@Mike McKerns**). If you would like to share how you use
+``pyina`` in your work, please send an email (to **mmckerns at uqfoundation dot
+org**).
 
 Important classes and functions are found here:
 
     - ``pyina.mpi``           [the map API definition]
     - ``pyina.schedulers``    [all available schedulers] 
     - ``pyina.launchers``     [all available launchers]
```

### Comparing `pyina-0.2.7/pyina.egg-info/SOURCES.txt` & `pyina-0.2.8/pyina.egg-info/SOURCES.txt`

 * *Files 5% similar despite different names*

```diff
@@ -15,14 +15,15 @@
 docs/requirements.txt
 docs/source/conf.py
 docs/source/index.rst
 docs/source/pathos.png
 docs/source/pyina.rst
 docs/source/requirements.txt
 docs/source/scripts.rst
+docs/source/_static/css/custom.css
 examples/hello_mpi4py.py
 examples/hello_pyina.py
 examples/machines_raw.py
 examples/mpd_trace.py
 examples/mpi_bcast.py
 examples/mpi_comm.py
 examples/mpi_simple.py
```

### Comparing `pyina-0.2.7/scripts/ezpool` & `pyina-0.2.8/scripts/ezpool`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 helper script for ``pyina.mpi`` maps using the *'worker pool'* strategy
 
 Notes:
     this uses the same code as ``ezscatter``, but with ``pyina.mpi_pool``.
```

### Comparing `pyina-0.2.7/scripts/ezscatter` & `pyina-0.2.8/scripts/ezscatter`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 """
 helper script for ``pyina.mpi`` maps using the *'scatter gather'* strategy
 
 Notes:
     this uses the same code as ``ezpool``, but with ``pyina.mpi_scatter``.
```

### Comparing `pyina-0.2.7/scripts/mpi_world` & `pyina-0.2.8/scripts/mpi_world`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 #
 # helper script to setup your mpi environment
 
 import pyina.__main__
 from pyina.__main__ import *
```

### Comparing `pyina-0.2.7/setup.py` & `pyina-0.2.8/setup.py`

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
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
 import os
 import sys
 # drop support for older python
 if sys.version_info < (3, 7):
@@ -81,14 +81,15 @@
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
     packages=['pyina','pyina.tests'],
     package_dir={'pyina':'pyina','pyina.tests':'pyina/tests'},
@@ -98,17 +99,17 @@
 # force python-, abi-, and platform-specific naming of bdist_wheel
 class BinaryDistribution(Distribution):
     """Distribution which forces a binary package with platform name"""
     def has_ext_modules(foo):
         return True
 
 # define dependencies
-dill_version = 'dill>=0.3.6'
-pox_version = 'pox>=0.3.2'
-pathos_version = 'pathos>=0.3.0'
+dill_version = 'dill>=0.3.7'
+pox_version = 'pox>=0.3.3'
+pathos_version = 'pathos>=0.3.1'
 mystic_version = 'mystic>=0.4.0'
 cython_version = 'cython>=0.29.30' #XXX: required to build numpy from source
 numpy_version = 'numpy>=1.0'
 mpi4py_version = 'mpi4py>=1.3, !=3.0.2' # segfault 11 on MPI import
 # add dependencies
 depend = [numpy_version, dill_version, pox_version, pathos_version, mpi4py_version]
 extras = {'examples': [mystic_version]}
```

### Comparing `pyina-0.2.7/version.py` & `pyina-0.2.8/version.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/pyina/blob/master/LICENSE
 
-__version__ = '0.2.7'
+__version__ = '0.2.8'
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

