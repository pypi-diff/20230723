# Comparing `tmp/PGAPy-2.2.1.tar.gz` & `tmp/PGAPy-2.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PGAPy-2.2.1.tar", last modified: Sun Apr 16 14:30:29 2023, max compression
+gzip compressed data, was "PGAPy-2.2.2.tar", last modified: Sun Jul 23 16:18:44 2023, max compression
```

## Comparing `PGAPy-2.2.1.tar` & `PGAPy-2.2.2.tar`

### file list

```diff
@@ -1,87 +1,88 @@
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.894634 PGAPy-2.2.1/
--rw-r--r--   0 ralf      (1000) priv      (1011)     1306 2020-05-30 13:50:14.000000 PGAPy-2.2.1/COPYING
--rw-r--r--   0 ralf      (1000) priv      (1011)     1093 2022-12-02 20:07:09.000000 PGAPy-2.2.1/MANIFEST.in
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.562634 PGAPy-2.2.1/PGAPy.egg-info/
--rw-r--r--   0 ralf      (1000) priv      (1011)    60061 2023-04-16 14:30:29.000000 PGAPy-2.2.1/PGAPy.egg-info/PKG-INFO
--rw-r--r--   0 ralf      (1000) priv      (1011)     1605 2023-04-16 14:30:29.000000 PGAPy-2.2.1/PGAPy.egg-info/SOURCES.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)        1 2023-04-16 14:30:29.000000 PGAPy-2.2.1/PGAPy.egg-info/dependency_links.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)        4 2023-04-16 14:30:29.000000 PGAPy-2.2.1/PGAPy.egg-info/top_level.txt
--rw-r--r--   0 ralf      (1000) priv      (1011)    60061 2023-04-16 14:30:29.894634 PGAPy-2.2.1/PKG-INFO
--rw-r--r--   0 ralf      (1000) priv      (1011)    80231 2023-04-16 14:30:00.000000 PGAPy-2.2.1/README.html
--rw-r--r--   0 ralf      (1000) priv      (1011)    50931 2023-04-16 14:07:34.000000 PGAPy-2.2.1/README.rst
--rw-r--r--   0 ralf      (1000) priv      (1011)       24 2023-04-16 14:30:01.000000 PGAPy-2.2.1/Version.h
--rw-r--r--   0 ralf      (1000) priv      (1011)       16 2023-04-16 14:30:01.000000 PGAPy-2.2.1/Version.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.622634 PGAPy-2.2.1/examples/
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2197 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/cards.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2333 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/cards_mutate.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2583 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/constraint.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     4085 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/dtlz2.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2608 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/fourbar.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     4508 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/gears.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.638634 PGAPy-2.2.1/examples/gp/
--rw-r--r--   0 ralf      (1000) priv      (1011)     2460 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/gp/README.rst
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    22896 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/gp/gp.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     9217 2022-12-04 15:00:04.000000 PGAPy-2.2.1/examples/gp/opt_integral.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2839 2022-12-04 15:00:37.000000 PGAPy-2.2.1/examples/gp/opt_parity3.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2696 2022-12-04 15:00:57.000000 PGAPy-2.2.1/examples/gp/opt_xor.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     3535 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/hello_world_char.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2455 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/hello_world_int.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2802 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/himmelblau.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     6986 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/magic_prio.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    10362 2023-01-10 11:23:19.000000 PGAPy-2.2.1/examples/magic_square.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     3568 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/minfloat.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2833 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/multi.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     4730 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/namefull.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2290 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/one_max.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.650634 PGAPy-2.2.1/examples/sequence/
--rw-r--r--   0 ralf      (1000) priv      (1011)      821 2022-08-18 16:53:20.000000 PGAPy-2.2.1/examples/sequence/croes.tsp
--rw-r--r--   0 ralf      (1000) priv      (1011)     1090 2022-08-18 16:53:20.000000 PGAPy-2.2.1/examples/sequence/oliver30.tsp
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     5276 2022-08-18 16:53:20.000000 PGAPy-2.2.1/examples/sequence/plot_tour.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)    50389 2022-12-04 14:54:43.000000 PGAPy-2.2.1/examples/sequence/tsp.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2044 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/sort_numbers.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     2704 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/twobar.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     3505 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/vibr.py
--rwxr-xr-x   0 ralf      (1000) priv      (1011)     4775 2022-12-02 19:48:39.000000 PGAPy-2.2.1/examples/xor.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.666634 PGAPy-2.2.1/pga/
--rw-r--r--   0 ralf      (1000) priv      (1011)     1729 2022-12-04 15:02:41.000000 PGAPy-2.2.1/pga/__init__.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     2240 2022-12-04 15:02:17.000000 PGAPy-2.2.1/pga/random.py
--rw-r--r--   0 ralf      (1000) priv      (1011)     3996 2022-12-04 15:25:31.000000 PGAPy-2.2.1/pga/testsupport.py
--rw-r--r--   0 ralf      (1000) priv      (1011)   113947 2023-04-16 13:28:40.000000 PGAPy-2.2.1/pgamodule.c
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.502634 PGAPy-2.2.1/pgapack/
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.670634 PGAPy-2.2.1/pgapack/docs/
--rw-r--r--   0 ralf      (1000) priv      (1011)   555087 2023-04-16 14:30:03.000000 PGAPy-2.2.1/pgapack/docs/user_guide.pdf
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.722634 PGAPy-2.2.1/pgapack/fakempi/
--rw-r--r--   0 ralf      (1000) priv      (1011)     2240 2023-04-16 13:36:21.000000 PGAPy-2.2.1/pgapack/fakempi/mpi.h
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.726634 PGAPy-2.2.1/pgapack/include/
--rw-r--r--   0 ralf      (1000) priv      (1011)    66915 2023-04-16 13:16:47.000000 PGAPy-2.2.1/pgapack/include/pgapack.h
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.874634 PGAPy-2.2.1/pgapack/source/
--rw-r--r--   0 ralf      (1000) priv      (1011)    35224 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/binary.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    26834 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/char.c
--rw-r--r--   0 ralf      (1000) priv      (1011)     9052 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/cmdline.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    69572 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/create.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    20380 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/cross.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    63817 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/debug.c
--rw-r--r--   0 ralf      (1000) priv      (1011)     9804 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/duplcate.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    35572 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/evaluate.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    95299 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/f2c.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    26363 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/fitness.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    61076 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/integer.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    15057 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/linalg.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    10025 2023-04-16 13:36:21.000000 PGAPy-2.2.1/pgapack/source/mpi_stub.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    38056 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/mutation.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    49328 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/parallel.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    32700 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/pga.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    49657 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/pop.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    16516 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/random.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    48411 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/real.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    46980 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/report.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    10171 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/restart.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    34323 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/select.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    13423 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/stop.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    12896 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/system.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    10711 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/user.c
--rw-r--r--   0 ralf      (1000) priv      (1011)    43927 2023-04-16 13:16:48.000000 PGAPy-2.2.1/pgapack/source/utility.c
--rw-r--r--   0 ralf      (1000) priv      (1011)       38 2023-04-16 14:30:29.894634 PGAPy-2.2.1/setup.cfg
--rw-r--r--   0 ralf      (1000) priv      (1011)     8551 2023-04-16 13:18:12.000000 PGAPy-2.2.1/setup.py
-drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-04-16 14:30:29.882634 PGAPy-2.2.1/test/
--rw-r--r--   0 ralf      (1000) priv      (1011)    23792 2022-12-04 15:23:46.000000 PGAPy-2.2.1/test/test_pgapy.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.872483 PGAPy-2.2.2/
+-rw-r--r--   0 ralf      (1000) priv      (1011)     1306 2020-05-30 13:50:14.000000 PGAPy-2.2.2/COPYING
+-rw-r--r--   0 ralf      (1000) priv      (1011)     1093 2022-12-02 20:07:09.000000 PGAPy-2.2.2/MANIFEST.in
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.488483 PGAPy-2.2.2/PGAPy.egg-info/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    52328 2023-07-23 16:18:44.000000 PGAPy-2.2.2/PGAPy.egg-info/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)     1624 2023-07-23 16:18:44.000000 PGAPy-2.2.2/PGAPy.egg-info/SOURCES.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)        1 2023-07-23 16:18:44.000000 PGAPy-2.2.2/PGAPy.egg-info/dependency_links.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)        4 2023-07-23 16:18:44.000000 PGAPy-2.2.2/PGAPy.egg-info/top_level.txt
+-rw-r--r--   0 ralf      (1000) priv      (1011)    52328 2023-07-23 16:18:44.868483 PGAPy-2.2.2/PKG-INFO
+-rw-r--r--   0 ralf      (1000) priv      (1011)    81082 2023-07-23 16:18:33.000000 PGAPy-2.2.2/README.html
+-rw-r--r--   0 ralf      (1000) priv      (1011)    51192 2023-07-23 16:17:03.000000 PGAPy-2.2.2/README.rst
+-rw-r--r--   0 ralf      (1000) priv      (1011)       24 2023-07-23 16:18:33.000000 PGAPy-2.2.2/Version.h
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.544483 PGAPy-2.2.2/examples/
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2197 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/cards.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2333 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/cards_mutate.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2583 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/constraint.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     4085 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/dtlz2.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2608 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/fourbar.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     4508 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/gears.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.564483 PGAPy-2.2.2/examples/gp/
+-rw-r--r--   0 ralf      (1000) priv      (1011)     2460 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/gp/README.rst
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    22896 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/gp/gp.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     9217 2022-12-04 15:00:04.000000 PGAPy-2.2.2/examples/gp/opt_integral.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2839 2022-12-04 15:00:37.000000 PGAPy-2.2.2/examples/gp/opt_parity3.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2696 2022-12-04 15:00:57.000000 PGAPy-2.2.2/examples/gp/opt_xor.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     3535 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/hello_world_char.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2455 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/hello_world_int.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2802 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/himmelblau.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     6986 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/magic_prio.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    10362 2023-01-10 11:23:19.000000 PGAPy-2.2.2/examples/magic_square.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     3568 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/minfloat.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2833 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/multi.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     4730 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/namefull.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2290 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/one_max.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.576483 PGAPy-2.2.2/examples/sequence/
+-rw-r--r--   0 ralf      (1000) priv      (1011)      821 2022-08-18 16:53:20.000000 PGAPy-2.2.2/examples/sequence/croes.tsp
+-rw-r--r--   0 ralf      (1000) priv      (1011)     1090 2022-08-18 16:53:20.000000 PGAPy-2.2.2/examples/sequence/oliver30.tsp
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     5276 2022-08-18 16:53:20.000000 PGAPy-2.2.2/examples/sequence/plot_tour.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)    50389 2022-12-04 14:54:43.000000 PGAPy-2.2.2/examples/sequence/tsp.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2044 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/sort_numbers.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     2704 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/twobar.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     3505 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/vibr.py
+-rwxr-xr-x   0 ralf      (1000) priv      (1011)     4775 2022-12-02 19:48:39.000000 PGAPy-2.2.2/examples/xor.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.592483 PGAPy-2.2.2/pga/
+-rw-r--r--   0 ralf      (1000) priv      (1011)       16 2023-07-23 16:18:33.000000 PGAPy-2.2.2/pga/Version.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     1729 2022-12-04 15:02:41.000000 PGAPy-2.2.2/pga/__init__.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     2240 2022-12-04 15:02:17.000000 PGAPy-2.2.2/pga/random.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)     3996 2022-12-04 15:25:31.000000 PGAPy-2.2.2/pga/testsupport.py
+-rw-r--r--   0 ralf      (1000) priv      (1011)   113947 2023-04-16 13:28:40.000000 PGAPy-2.2.2/pgamodule.c
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.424483 PGAPy-2.2.2/pgapack/
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.596483 PGAPy-2.2.2/pgapack/docs/
+-rw-r--r--   0 ralf      (1000) priv      (1011)   555144 2023-07-23 16:18:37.000000 PGAPy-2.2.2/pgapack/docs/user_guide.pdf
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.696483 PGAPy-2.2.2/pgapack/fakempi/
+-rw-r--r--   0 ralf      (1000) priv      (1011)     2240 2023-04-16 13:36:21.000000 PGAPy-2.2.2/pgapack/fakempi/mpi.h
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.700483 PGAPy-2.2.2/pgapack/include/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    66915 2023-04-16 13:16:47.000000 PGAPy-2.2.2/pgapack/include/pgapack.h
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.852483 PGAPy-2.2.2/pgapack/source/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    35224 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/binary.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    26834 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/char.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)     9052 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/cmdline.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    69572 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/create.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    20380 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/cross.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    63817 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/debug.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)     9804 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/duplcate.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    35572 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/evaluate.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    95299 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/f2c.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    26363 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/fitness.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    61076 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/integer.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    15057 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/linalg.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    10025 2023-04-16 13:36:21.000000 PGAPy-2.2.2/pgapack/source/mpi_stub.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    38056 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/mutation.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    49328 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/parallel.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    32700 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/pga.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    49657 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/pop.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    16516 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/random.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    48411 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/real.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    46980 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/report.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    10171 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/restart.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    34323 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/select.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    13423 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/stop.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    12896 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/system.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    10711 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/user.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)    43927 2023-04-16 13:16:48.000000 PGAPy-2.2.2/pgapack/source/utility.c
+-rw-r--r--   0 ralf      (1000) priv      (1011)     2905 2023-07-23 15:57:14.000000 PGAPy-2.2.2/pyproject.toml
+-rw-r--r--   0 ralf      (1000) priv      (1011)       38 2023-07-23 16:18:44.872483 PGAPy-2.2.2/setup.cfg
+-rw-r--r--   0 ralf      (1000) priv      (1011)     8540 2023-07-23 15:57:35.000000 PGAPy-2.2.2/setup.py
+drwxr-xr-x   0 ralf      (1000) priv      (1011)        0 2023-07-23 16:18:44.860483 PGAPy-2.2.2/test/
+-rw-r--r--   0 ralf      (1000) priv      (1011)    23792 2022-12-04 15:23:46.000000 PGAPy-2.2.2/test/test_pgapy.py
```

### Comparing `PGAPy-2.2.1/COPYING` & `PGAPy-2.2.2/COPYING`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/MANIFEST.in` & `PGAPy-2.2.2/MANIFEST.in`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/PGAPy.egg-info/PKG-INFO` & `PGAPy-2.2.2/PGAPy.egg-info/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,1046 +1,1056 @@
 Metadata-Version: 2.1
 Name: PGAPy
-Version: 2.2.1
+Version: 2.2.2
 Summary: Python wrapper for pgapack, the parallel genetic algorithm library
-Home-page: http://pgapy.sourceforge.net/
+Home-page: https://github.com/schlatterbeck/pgapy
 Author: Ralf Schlatterbeck
-Author-email: rsc@runtux.com
-License: UNKNOWN
-Description: PGAPy: Python Wrapper for PGAPack Parallel Genetic Algorithm Library
-        ====================================================================
-        
-        .. |--| unicode:: U+2013   .. en dash
-        .. |epsilon| unicode:: U+03B5 .. epsilon
-        
-        :Author: Ralf Schlatterbeck <rsc@runtux.com>
-        
-        News
-        ----
-        
-        News 04-2023:
-        
-        - The last build on PyPi was broken for serial installs, it was missing
-          the ``mpi_stub.c`` needed for the serial version. Parallel installs
-          were still possible so I didn't notice, sorry!
-        - Add MPI_Abort to the wrapper, it is called with::
-        
-            pga.MPI_Abort (errcode)
-        
-          See below in secion `Running with MPI`_ how this can be used to abort
-          the MPI run in case of exception in the ``evaluate`` method.
-        
-        News 12-2022: Add regression test and update to new upstream with
-        several bug-fixes. Includes also some bug fixes in wrapper.
-        
-        News 10-2022: Add user defined datatypes. Example in ``examples/gp`` use
-        user defined data types to implement genetic programming (we represent
-        expressions by a tree data structure). This uses the new serialization
-        API in pgapack to transfer a Python pickle representation to peer MPI
-        processes. Also incorporate the latest changes in pgapack which
-        optimizes duplicate checking. This is of interest for large population
-        sizes in the genetic programming examples. Note that the
-        ``gene_difference`` method has been renamed to ``gene_distance``.
-        
-        News 08-2022: Epsilon-constrained optimization and a crossover variant
-        that preserves permutations (so with integer genes the gene can represent
-        a permutation).
-        
-        News 03-2022: Attempt to make this installable on Windows. This involves
-        some workaround in the code because the visual compiler does not support
-        certain C99 constructs.
-        
-        News 01-2022: This version wraps multiple evaluation with NSGA-III (note
-        the additional 'I').
-        
-        News 12-2021: This version wraps multiple evaluation values from your
-        objective function: Now you can return more than one value to either use
-        it for constraints (that must be fulfilled before the objective is
-        optimized) or for multi-objective optimization with the Nondominated
-        Sorting Genetic Algorithm V.2 (NSGA-II). You can combine both,
-        multi-objective optimization and constraints.
-        
-        News: This version wraps the Differential Evolution method (that's quite
-        an old method but is newly implemented in pgapack).
-        
-        Introduction
-        ------------
-        
-        PGAPy is a wrapper for PGAPack, the parallel genetic algorithm library
-        (see `PGAPack Readme`_), a powerfull genetic algorithm library by
-        D. Levine, Mathematics and Computer Science Division Argonne National
-        Laboratory. The library is written in C. PGAPy wraps this library for
-        use with Python. The original PGAPack library is already quite old but
-        is one of the most complete and accurate (and fast, although this is not
-        my major concern when wrapping it to python) genetic algorithm
-        implementations out there with a lot of bells and whistles for
-        experimentation. It also has shown a remarkably small number of bugs
-        over the years. It supports parallel execution via the message
-        passing interface MPI_ in addition to a normal "serial" version. That's
-        why I wanted to use it in Python, too.
-        
-        To get started you need the PGAPack library, although
-        it now comes bundled with PGApy, to install a *parallel* version you
-        currently need a pre-installed PGAPack_ compiled for the MPI library of
-        choice. See `Installation`_ section for details.
-        
-        There currently is not much documentation for PGAPy.
-        You really, absolutely need to read the documentation that comes
-        with PGAPack.
-        The PGAPack user guide is now shipped together with PGAPy. It is
-        installed together with some examples in share/pgapy, wherever the
-        Python installer decides to place this in the final installation
-        (usually ``/usr/local/share`` on Linux).
-        
-        The original PGAPack library can still be downloaded from the PGAPack_
-        ftp site, it is written in ANSI C but will probably not compile against
-        a recent version of MPI_. It will also not work with recent versions of
-        PGAPy. Note that this version is not actively maintained. I've started a
-        `PGAPack fork on github`_ where I've ported the library to the latest
-        version of the MPI_ standard and have fixed some minor inconsistencies
-        in the documentation. I've also implemented some new features, notably
-        enhancements in selection schemes, a new replacement strategy called
-        *restricted tournament replacement* [1]_, [2]_, [4]_ and, more recently,
-        the differential evolution strategy [5]_, [6]_. In addition this version
-        now supports multi objective optimization with NSGA-II [7]_ and
-        many-objective optimization with NSGA-III [8]_, [9]_. It also supports
-        the Epsilon Constraint method [10]_.
-        
-        Note: When using NSGA_III replacement for multi (or many-) objective
-        optimization you need to either
-        
-        - set reference points on the hyperplane intersecting all axes at
-          offset 1. These reference points can be obtained with the convenience
-          function ``pga.das_dennis``, it creates a regular set of reference points
-          using an algorithm originally publised by I. Das and J. E. Dennis [12]_.
-          These points are then passed as the parameter ``reference_points`` to
-          the ``PGA`` constructor.
-        
-          See ``examples/dtlz2.py`` for a usage example and the user guide for
-          the bibliographic reference. The function gets the dimensionality of
-          the objective space (``num_eval`` minus ``num_constraint``) and the
-          number of partition to use.
-        - Or set reference directions (in the objective space) with the
-          ``reference_directions`` parameter, number of partitions for these
-          directions with the ``refdir_partitions`` parameter (see
-          ``das_dennis`` above, this uses Das/Dennis points internally), and a
-          scale factor with the parameter ``refdir_scale``.
-        
-        You can set both, these parameters are not mutually exclusive.
-        
-        I'm mainly testing pgapy on Linux. But I've recently made it run on
-        Windows, too but I'm not very actively testing on Windows. Let me know
-        if you run it on Windows, sucessfully or not sucessfully.
-        
-        As mentioned above, you can find my `PGAPack fork on github`_, this
-        repository has the three upstream releases as versions in git and
-        contains some updates concerning support of newer MPI_ versions and
-        documentation updates.  I've also included patches in the git repository
-        of the Debian maintainer of the package, Dirk Eddelbuettel.
-        I'm actively maintaining that branch, adding new features and bug-fixes.
-        
-        To get you started, I've included some very simple examples in
-        ``examples``, e.g., ``one-max.py`` implements the "Maxbit" example
-        similar to one in the PGAPack documentation. The examples were inspired
-        by the book "Genetic Algorithms in Python" but are written from scratch
-        and don't include any code from the book. The examples illustrates
-        several points:
-        
-        - Your class implementing the genetic algorithm needs to inherit from
-          pga.PGA (pga is the PGAPy wrapper module).
-        - You need to define an evaluation function called ``evaluate`` that
-          returns a sequence of numbers indicating the fitness of the gene given.
-          It gets the parameters ``p`` and ``pop`` that can be used to fetch allele
-          values from the gene using the ``get_allele`` method, for more details
-          refer to the PGAPack documentation. The number of evaluations returned
-          by your function is defined with the constructor parameter
-          ``num_eval``, the default for this parameter is 1. If your evaluation
-          function does not return multiple evaluations (with the default
-          setting of ``num_eval``) you can either return a one-element sequence
-          or a single return value.
-        - When using multiple evaluations, these can either be used for
-          constraints (the default) or for multi-objective optimization. In the
-          latter case, the number of constraints (which by default is one less
-          than the number of evaluations set with the parameter ``num_eval``)
-          must be set to a number that leaves at least two evaluations for
-          objectives. The number of constraints can be set with the parameter
-          ``num_constraint``. When using multi-objective optimization, you need
-          one of the two replacement-types ``PGA_POPREPL_NSGA_II`` or
-          ``PGA_POPREPL_NSGA_III``, set this with the ``pop_replace_type`` parameter.
-        - You *can* define additional functions overriding built-in functions
-          of the PGAPack library, illustrated by the example of
-          ``print_string``.  Note that we could call the original print_string
-          method of our PGA superclass.  In the same way you can implement,
-          e.g., your own crossover method.
-        - The constructor of the class needs to define the Gene type, in the
-          examples we use int and bool built-in datatypes.
-        - The length of the gene needs to be given in the constructor.
-        - We often want to maximize the numbers returned by our evaluation
-          function, set the parameter ``maximize`` to False if you want to
-          minimize.
-        - For non-binary genes we can define an array of init values, each entry
-          containing a sequence with lower and upper bound. The array has to
-          have the length of the gene. Note that the upper bound is *included*
-          in the range of possible values (unlike the python range operator but
-          compatible with the PGAPack definition).
-        - In the constructor of the class we can add parameters of the genetic
-          algorithm. Not all parameters of PGAPack are wrapped yet, currently
-          you would need to consult the sourcecode of PGAPy to find out which
-          parameters are wrapped. In the example we define several print
-          options.
-        - Finally the genetic algorithm is started with the ``run`` method.
-        
-        Naming conventions in PGAPy
-        ---------------------------
-        
-        When you extend PGAPy |--| remember not all functions of PGAPack are
-        wrapped yet and you may need additional functions |--| you should stick to
-        my naming conventions when making changes.
-        The following naming conventions were used for the wrapper:
-        
-        - Constants of PGAPack like ``PGA_REPORT_STRING`` are used as-is in
-          uppercase. These constants can be directly imported from the wrapper
-          module. Not all constants are wrapped so far, if you need more, add
-          them to the constdef array in pgamodule.c and send_ me a patch.
-        - For methods of the pga.PGA class I've removed the ``PGA`` prefix used
-          throughout PGAPack and converted the method to lowercase with
-          underscores between uppercase words in the original function name, so
-          ``PGARun`` becomes ``run``, ``PGACheckStoppingConditions`` becomes
-          ``check_stopping_conditions``. An exception of the lowercase-rule is
-          whenever a name contains "GA" (for "genetic algorithm"), So
-          ``PGASetMaxGAIterValue`` becomes ``max_GA_iter``.
-        - Where possible I've made a single class method where PGAPack needs a
-          separate function for each datatype, so ``PGAGetBinaryAllele``,
-          ``PGAGetCharacterAllele``, ``PGAGetIntegerAllele``, ``PGAGetRealAllele`` all
-          become ``get_allele``. Same holds true for ``set_allele``.
-        - Whenever a name in PGAPack has a "Value" or "Flag" suffix, I've left
-          this out, so ``PGAGetFitnessCmaxValue`` becomes ``fitness_cmax``
-          and ``PGAGetMutationAndCrossoverFlag`` becomes
-          ``mutation_and_crossover``, the only exception to this rule is for the
-          two functions ``PGAGetMutationRealValue`` and
-          ``PGAGetMutationIntegerValue`` which become ``mutation_value`` not
-          just ``mutation``.
-        - Some fields can take multiple values (they are implemented by ORing
-          integer constants, in python they are specified as a list or tuple of
-          constants). These are converted to plural (if not already plural in
-          PGAPack), e.g., ``PGASetStoppingRuleType`` becomes ``stopping_rule_types``.
-        - Internal method names in the wrapper program have a leading PGA\_ |--| so
-          the class method ``set_allele`` is implemented by the C-function
-          ``PGA_set_allele`` in ``pgamodule.c``.
-        
-        Constructor Parameters
-        ----------------------
-        
-        PGAPack_ has a lot of ``PGASet`` and ``PGAGet`` functions for setting
-        parameters. These are reflected in constructor parameters on the one hand
-        and in (typically read-only, but see below) properties of a ``PGA``
-        object on the other hand. The
-        following table gives an overview of all the original PGAPack_ names and
-        the names of the python wrapper. For the PGAPack_ name I've only listed
-        the ``PGASet`` function, in many cases there is a corresponding
-        ``PGAGet`` function. If a corresponding read-only property exists for a
-        constructor parameter this is indicated in the "Prop" column. In some
-        cases properties are missing because no corresponding ``PGAGet`` function
-        is implemented in PGAPack_, in other cases returning a numeric value that
-        has a symbolic constant in PGApy doesn't make much sense.
-        
-        The properties have the same name as the constructor parameter.
-        There are Properties that don't have a corresponding constructor
-        parameter, namely the ``eval_count`` property (returning the count of
-        function evaluations), the
-        ``GA_iter`` property that returns the current GA generation, and the
-        ``mpi_rank`` property that returns the MPI rank of the current process
-        (this is sorted under PGAGetRank).
-        
-        In the type
-        column I'm listing the Python type. If the type is followed by a number,
-        more than one item of that type is specified (a sequence in Python). Some
-        entries contain "sym", these are integer values with a symbolic constant,
-        the value "msym" indicates that several values denoted by a list of
-        symbolic constants can be given. A special case are the
-        ``PGASetRealInitRange``, ``PGASetRealInitPercent``,
-        ``PGASetIntegerInitRange`` functions. These take two values for *each
-        allele* of the gene. In python this is a sequence of 2-tuples.
-        Note that this means that you can have different ranges of allowed values
-        for each allele.
-        
-        The ``num_eval`` property is special: Due to limitations of the C
-        programming language, for multiple evaluations in C the first evaluation
-        is returned as the function return-value of the ``evaluate`` function
-        and all other parameters are returned in an auxiliary array. PGAPack_
-        specifies the number of auxiliary evaluations to be returned. In Python
-        the evaluation function can always return a sequence of evaluation
-        values and the ``num_eval`` is one more than ``PGAGetNumAuxEval`` would
-        return. The default for ``num_eval`` is 1.
-        
-        The first two (mandatory) constructor parameters are the type of the gene
-        (this takes a Python type, e.g., ``bool`` for a binary genome or ``int``
-        for an integer genome) and the length. Note that the ``string_length`` is
-        implicitly set with the ``length`` parameter. The ``string_length`` is
-        also available as the length of the ``PGA`` object using the Python
-        built-in ``len`` function.
-        
-        Some properties can now also be set *during* the run of the optimizer.
-        These currently are ``crossover_prob``, ``epsilon_exponent``,
-        ``multi_obj_precision``, ``p_tournament_prob``, and
-        ``uniform_crossover_prob``. Just assign to the member variable of
-        the optimizer (child of PGA.pga) object.
-        
-        ==================================== ================================= ====== ====
-        PGAPack name                         Constructor parameter             Type   Prop
-        ==================================== ================================= ====== ====
-        ``PGASetCrossoverBoundedFlag``       ``crossover_bounded``             int    yes
-        ``PGASetCrossoverBounceBackFlag``    ``crossover_bounce_back``         int    yes
-        ``PGASetCrossoverSBXEta``            ``crossover_SBX_eta``             float  yes
-        ``PGASetCrossoverSBXOncePerString``  ``crossover_SBX_once_per_string`` int    yes
-        ``PGASetCrossoverProb``              ``crossover_prob``                float  yes
-        ``PGASetCrossoverType``              ``crossover_type``                sym    no
-        ``PGASetDEAuxFactor``                ``DE_aux_factor``                 double yes
-        ``PGASetDECrossoverProb``            ``DE_crossover_prob``             double yes
-        ``PGASetDECrossoverType``            ``DE_crossover_type``             sym    no
-        ``PGASetDEDither``                   ``DE_dither``                     double yes
-        ``PGASetDEDitherPerIndividual``      ``DE_dither_per_individual``      bool   yes
-        ``PGASetDEJitter``                   ``DE_jitter``                     double yes
-        ``PGASetDENumDiffs``                 ``DE_num_diffs``                  int    yes
-        ``PGASetDEProbabilityEO``            ``DE_probability_EO``             double yes
-        ``PGASetDEScaleFactor``              ``DE_scale_factor``               double yes
-        ``PGASetDEVariant``                  ``DE_variant``                    sym    yes
-        ``PGASetEpsilonExponent``            ``epsilon_exponent``              float  yes
-        ``PGASetEpsilonGeneration``          ``epsilon_generation``            int    yes
-        ``PGASetEpsilonTheta``               ``epsilon_theta``                 int    yes
-        ``PGAGetEvalCount``                  ``eval_count``                    int    yes
-        ``PGASetFitnessCmaxValue``           ``fitness_cmax``                  float  yes
-        ``PGASetFitnessMinType``             ``fitness_min_type``              sym    yes
-        ``PGASetFitnessType``                ``fitness_type``                  sym    yes
-        ``PGAIntegerSetFixedEdges``          ``fixed_edges``                          no
-        ``PGAIntegerSetFixedEdges``          ``fixed_edges_symmetric``         bool   no
-        ``PGAGetGAIterValue``                ``GA_iter``                       int    yes
-        ``PGASetIntegerInitPermute``         ``integer_init_permute``          int2   no
-        ``PGASetIntegerInitRange``           ``init``                                 no
-        ``PGASetMaxFitnessRank``             ``max_fitness_rank``              float  yes
-        ``PGASetMaxGAIterValue``             ``max_GA_iter``                   int    yes
-        ``PGASetMaxNoChangeValue``           ``max_no_change``                 int    no
-        ``PGASetMaxSimilarityValue``         ``max_similarity``                int    yes
-        ``PGASetMixingType``                 ``mixing_type``                   sym    no
-        ``PGASetMultiObjPrecision``          ``multi_obj_precision``           int    yes
-        ``PGASetMutationAndCrossoverFlag``   ``mutation_and_crossover``        int    yes
-        ``PGASetMutationBounceBackFlag``     ``mutation_bounce_back``          int    yes
-        ``PGASetMutationBoundedFlag``        ``mutation_bounded``              int    yes
-        ``PGASetMutationIntegerValue``       ``mutation_value``                int    yes
-        ``PGASetMutationOrCrossoverFlag``    ``mutation_or_crossover``         int    yes
-        ``PGASetMutationPolyEta``            ``mutation_poly_eta``             float  yes
-        ``PGASetMutationPolyValue``          ``mutation_poly_value``           float  yes
-        ``PGASetMutationProb``               ``mutation_prob``                 float  yes
-        ``PGASetMutationRealValue``          ``mutation_value``                float  yes
-        ``PGASetMutationType``               ``mutation_type``                 sym    no
-        ``PGASetNoDuplicatesFlag``           ``no_duplicates``                 int    no
-        ``PGASetNumAuxEval``                 ``num_eval``                      int    yes
-        ``PGASetNumConstraint``              ``num_constraint``                int    yes
-        ``PGASetNumReplaceValue``            ``num_replace``                   int    yes
-        ``PGASetPopSize``                    ``pop_size``                      int    yes
-        ``PGASetPopReplaceType``             ``pop_replace_type``              sym    no
-        ``PGASetPrintFrequencyValue``        ``print_frequency``               int    yes
-        ``PGASetPrintOptions``               ``print_options``                 msym   no
-        ``PGASetPTournamentProb``            ``p_tournament_prob``             float  yes
-        ``PGASetRandomizeSelect``            ``randomize_select``              int    yes
-        ``PGASetRandomSeed``                 ``random_seed``                   int    yes
-        ``PGAGetRank``                       ``mpi_rank``                      int    yes
-        ``PGASetRealInitRange``              ``init``                                 no
-        ``PGASetRealInitPercent``            ``init_percent``                         no
-        ``PGASetReferenceDirections``        ``refdir_partitions``             int    no
-        ``PGASetReferenceDirections``        ``refdir_scale``                  double no
-        ``PGASetReferenceDirections``        ``reference_directions``                 no
-        ``PGASetReferencePoints``            ``reference_points``                     no
-        ``PGASetRestartFlag``                ``restart``                       int    yes
-        ``PGASetRestartFrequencyValue``      ``restart_frequency``             int    yes
-        ``PGASetRTRWindowSize``              ``rtr_window_size``               int    yes
-        ``PGASetSelectType``                 ``select_type``                   sym    no
-        ``PGASetStoppingRuleType``           ``stopping_rule_types``           msym   no
-        ``PGASetStringLength``               ``string_length``                 int    yes
-        ``PGASetSumConstraintsFlag``         ``sum_constraints``               int    yes
-        ``PGASetTournamentSize``             ``tournament_size``               int    yes
-        ``PGASetTournamentWithReplacement``  ``tournament_with_replacement``   int    yes
-        ``PGASetTruncationProportion``       ``truncation_proportion``         float  yes
-        ``PGASetUniformCrossoverProb``       ``uniform_crossover_prob``        float  yes
-        ==================================== ================================= ====== ====
-        
-        Note: The mutation_or_crossover and mutation_and_crossover parameters are
-        deprecated, use mixing_type instead!
-        
-        PGA Object Methods
-        ------------------
-        
-        The following are the methods that can be used during the run of the
-        genetic search. The ``run`` method is used to start the search. This can
-        be used, to, e.g., set an allele during hill-climbing in a custom
-        ``endofgen`` method. Note that some methods only apply to certain gene
-        types, e.g. the ``encode_int_`` methods can only be used on binary
-        alleles (they encode an integer value as a binary or gray code
-        representation into the gene). Other methods take or return different
-        types depending on the type of gene, e.g. ``get_allele`` or
-        ``set_allele``, they call different backend functions depending on the
-        gene type. With the ``set_random_seed`` method, the random number
-        generator can be re-seeded. It is usually best to seed the generator
-        once at (before) the beginning by specifying ``random_seed`` in the
-        constructor. For further details consult the user guide.
-        The method ``get_evaluation`` will return a double for a single
-        evaluation and a tuple of double for multiple evaluations (when num_eval
-        is >1)
-        
-        ============================= ================== ===========================
-        Method                        Parameters         Return
-        ============================= ================== ===========================
-        ``check_stopping_conditions``                    True if stop should occur
-        ``encode_int_as_binary``      *p, pop,*          None
-                                      *frm, to, val*
-        ``encode_int_as_gray_code``   *p, pop,*          None
-                                      *frm, to, val*
-        ``encode_real_as_binary``     *p, pop, frm, to*  None
-                                      *l, u, val*
-        ``encode_real_as_gray_code``  *p, pop, frm, to*  None
-                                      *l, u, val*
-        ``euclidian_distance``        *p1, pop1*         float
-                                      *p2, pop2*
-        ``fitness``                   *pop*              None
-        ``get_allele``                *p, pop, index*    allele value
-        ``get_best_index``            *pop*              index of best string
-        ``get_best_report_index``     *pop, idx*         index of best eval with idx
-        ``get_evaluation``            *p, pop*           evaluation of *p*
-        ``get_evaluation_up_to_date`` *p, pop*           True if up-to-date
-        ``get_fitness``               *p, pop*           fitness of *p* (float)
-        ``get_gene``                  *p, pop*           get gene (user data types)
-        ``get_int_from_binary``       *p, pop, frm, to*  int
-        ``get_int_from_gray_code``    *p, pop, frm, to*  int
-        ``get_iteration``                                deprecated, use ``GA_iter``
-        ``get_real_from_binary``      *p, pop,*          float
-                                      *frm, to, l, u*
-        ``get_real_from_gray_code``   *p, pop,*          float
-                                      *frm, to, l, u*
-        ``random01``                                     float between 0 and 1
-        ``random_flip``               *probability*      0 or 1
-        ``random_gaussian``           *mean, stddev*     float
-        ``random_interval``           *l, r*             int between l, r
-        ``random_uniform``            *l, r*             float between l, r
-        ``run``                                          None
-        ``select_next_index``         *pop*              index selected individual
-        ``set_allele``                *p, pop, i, value* None
-        ``set_evaluation``            *p, pop, value*    None
-        ``set_evaluation_up_to_date`` *p, pop, status*   None
-        ``set_gene``                  *p, pop, gen*      set gene (user data types)
-        ``set_random_seed``           *seed*             None (use constructor!)
-        ============================= ================== ===========================
-        
-        User-Methods
-        ------------
-        
-        PGAPack_ has the concept of user functions. These allow customization of
-        different areas of a genetic algorihm. In Python they are implemented as
-        methods that can be changed in a derived class. One of the methods that
-        *must* be implemented in a derived class is the ``evaluate`` function
-        (although technically it is not a user function in PGAPack). It
-        interprets the gene and returns an evaluation value or a sequence of
-        evaluation values if you set the ``num_eval`` constructor parameter.
-        PGAPack_ computes a fitness from the raw evaluation value. For some
-        methods an up-call into the PGA class is possible, for some methods this
-        is not possible (and in most cases not reasonable). Note that for the
-        ``stop_cond`` method, the standard check for stopping conditions can be
-        called with::
-        
-          self.check_stopping_conditions()
-        
-        The following table lists the overridable methods with their parameters
-        (for the function signature the first parameter *self* is omitted). Note
-        that in PGAPack_ there are additional user functions that are needed for
-        user-defined data types which are currently not exposed in Python. In the
-        function signatures *p* denotes the index of the individual and *pop*
-        denotes the population. If more than one individual is specified (e.g.,
-        for crossover) these can be followed by a number. For crossover *c1* and
-        *c2* denote the destination individuals (children). The *propability* for
-        the mutation method is a floating-point value between 0 and 1. Remember
-        to count the number of mutations that happen, and return that value for
-        the mutation method!
-        
-        =================== ============================== ================= =======
-        Method              Call Signature                 Return Value      Up-Call
-        =================== ============================== ================= =======
-        ``check_duplicate`` *p1, pop1, p2, pop2*           True if dupe      no
-        ``stop_cond``                                      True to stop      no
-        ``crossover``       *p1, p2, p_pop, c1, c2, c_pop* None              no
-        ``endofgen``                                       None              no
-        ``evaluate``        *p, pop*                       sequence of float no
-        ``gene_distance``   *p1, pop1, p2, pop2*           float             no
-        ``hash``            *p, pop*                       int               no
-        ``initstring``      *p, pop*                       None              no
-        ``mutation``        *p, pop, propability*          #mutations        no
-        ``pre_eval``        *pop*                          None              no
-        ``print_string``    *file, p, pop*                 None              yes
-        =================== ============================== ================= =======
-        
-        Constants
-        ---------
-        
-        The following PGAPack_ constants are available:
-        
-        ========================== ===========================================
-        Constant                   Description
-        ========================== ===========================================
-        PGA_CROSSOVER_EDGE         Edge crossover for permutations
-        PGA_CROSSOVER_ONEPT        One-point Crossover
-        PGA_CROSSOVER_SBX          Simulated Binary Crossover
-        PGA_CROSSOVER_TWOPT        Two-point Crossover
-        PGA_CROSSOVER_UNIFORM      Uniform Crossover
-        PGA_FITNESSMIN_CMAX        Map fitness by subtracting worst
-        PGA_FITNESSMIN_RECIPROCAL  Map fitness via reciprocal
-        PGA_FITNESS_NORMAL         Linear normalization of fitness
-        PGA_FITNESS_RANKING        Linear fitness ranking
-        PGA_FITNESS_RAW            Identity fitness function
-        PGA_MUTATION_CONSTANT      Mutation by adding/subtracting constant
-        PGA_MUTATION_GAUSSIAN      Mutation by selecting from Gaussian distribution
-        PGA_MUTATION_PERMUTE       Mutation swaps two random genes
-        PGA_MUTATION_POLY          Polynomial Mutation
-        PGA_MUTATION_RANGE         Replace gene with uniform selection from init range
-        PGA_MUTATION_UNIFORM       Mutation uniform from interval
-        PGA_NEWPOP                 Symbolic constant for new population
-        PGA_OLDPOP                 Symbolic constant for old population
-        PGA_POPREPL_BEST           Population replacement best strings
-        PGA_POPREPL_NSGA_II        Use NSGA-II replacement for multi-objective opt.
-        PGA_POPREPL_NSGA_III       Use NSGA-III replacement for multi-objective opt.
-        PGA_POPREPL_PAIRWISE_BEST  Compare same index in old and new population
-        PGA_POPREPL_RANDOM_NOREP   Population replacement random no replacement
-        PGA_POPREPL_RANDOM_REP     Population replacement random with replacement
-        PGA_POPREPL_RTR            Restricted Tournament Replacement
-        PGA_REPORT_AVERAGE         Report average evaluation
-        PGA_REPORT_HAMMING         Report hamming distance
-        PGA_REPORT_OFFLINE         Report offline
-        PGA_REPORT_ONLINE          Report online
-        PGA_REPORT_STRING          Report the string
-        PGA_REPORT_WORST           Report the worst evaluation
-        PGA_SELECT_LINEAR          Return individuals in population order
-        PGA_SELECT_PROPORTIONAL    Fitness-proportional selection
-        PGA_SELECT_PTOURNAMENT     Binary probabilistic tournament selection
-        PGA_SELECT_SUS             Stochastic universal selection
-        PGA_SELECT_TOURNAMENT      Tournament selection
-        PGA_SELECT_TRUNCATION      Truncation selection
-        PGA_STOP_MAXITER           Stop on max iterations
-        PGA_STOP_NOCHANGE          Stop on max number of generations no change
-        PGA_STOP_TOOSIMILAR        Stop when individuals too similar
-        ========================== ===========================================
-        
-        User Defined Data Types
-        -----------------------
-        
-        The latest version of PGAPy features user defined data types. Just
-        define your data type and pass it as the second parameter to the
-        ``PGA`` constructor. The framework will take care of serializing the
-        data when transmitting via ``MPI`` (if you're running a parallel
-        version).
-        
-        If duplicate checking is enabled via the ``no_duplicates`` constructor
-        parameter, your data type needs to define a ``__hash__`` method (unless
-        the python default hash method fulfills your requirements).
-        
-        User defined data types do not use alleles, so the normal ``get_allele``
-        (and ``set_allele``) methods are not available. Instead the full
-        individual can be retrieved with the ``get_gene`` method and set with
-        the ``set_gene`` method.
-        
-        With user data types you need to define the following methods:
-        
-        - ``check_duplicate (self, p1, pop1, p2, pop2)`` if you enable duplicate
-          checking with the crossover parameter ``no_duplicates``. This should
-          return True when the two individuals are duplicates. Use ``get_gene``
-          to retrieve the genes for the individuals ``p1`` and ``p2`` in
-          populations ``pop1`` and ``pop2``.
-        - ``crossover (self, p1, p2, ppop, c1, c2, cpop)`` for crossover
-          operation, use ``get_gene`` for getting the parent genes for the
-          parents ``p1`` and ``p2`` in generation ``ppop`` and use ``set_gene``
-          for setting the child genes ``c1`` and ``c2`` in generation ``cpop``.
-        - ``initstring (self, p, pop)`` for initializing the given string, use
-          ``set_gene`` in that method for setting your object as a gene.
-        - ``mutation (self, p, pop, pm)`` for the mutation operation. This
-          should return the number of mutations performed. If duplicate checking
-          is enabled, the framework will repeatedly call the mutation operator
-          for mutating a duplicate individual into another individual that is no
-          duplicate. This uses the return value of your mutation method. You
-          will enter an endless loop if your mutation operator does not
-          occasionally return an non-zero number of mutatations performed when
-          duplicate checking is enabled. The ``pm`` parameter gives the mutation
-          probability. Use ``get_gene`` for retrieving the individual to be
-          mutated and use ``set_gene`` to update this individual after mutation.
-        - ``print_string (self, file, p, pop)`` to print a gene object, use
-          ``get_gene`` for retrieving the individual to be printed.
-        
-        For these methods it is generally a good idea to never modify an
-        individual in-place: This individual may be repeatedly used in genetic
-        operations (e.g. mutation and crossover), so when modifying it you will
-        produce erroneous results for later genetic operations. To copy a data
-        structure, python's ``deepcopy`` function in the module ``copy`` is
-        usually used.
-        
-        In addition to the methods above you may want to define a stopping rule
-        with a ``stop_cond`` method or override the way a hash is computed using
-        a ``hash`` method. The default for computing a hash is to call
-        ``hash (gene)`` where gene is an object of the user defined data type.
-        Other methods that may be used is an ``endofgen`` method, a
-        ``gene_distance`` method (e.g., when using Restricted Tournament
-        Replacement, with ``PGA_POPREPL_RTR``), or a ``pre_eval`` method.
-        
-        An example with user defined data types is in ``examples/gp``: This
-        implements Genetic Programming with a tree data structure. Note that the
-        ``Node`` class in ``gp.py`` has a ``__hash__`` method that builds a hash
-        over the serialization of the tree (which is the same for individuals
-        with the same tree structure).
-        
-        
-        Missing Features
-        ----------------
-        
-        As already mentioned, not all functions and constants of PGAPack_ are
-        wrapped yet |--| still for many applications the given set should be
-        enough. If you need additional functions, you may want to wrap these and
-        send_ me a patch.
-        
-        Reporting Bugs
-        --------------
-        
-        Please use the `Sourceforge Bug Tracker`_  or the `Github Bug Tracker`_ and
-        
-        - give a short description of what you think is the correct behaviour
-        - give a description of the observed behaviour
-        - tell me exactly what you did.
-        - if you can publish your source code this makes it a lot easier to
-          debug for me
-        
-        .. _`Sourceforge Bug Tracker`:
-            http://sourceforge.net/tracker/?group_id=152022&atid=782852
-        .. _`Github Bug Tracker`:
-            https://github.com/schlatterbeck/pgapy/issues
-        .. _send: mailto:rsc@runtux.com
-        
-        Resources
-        ---------
-        
-        Project information and download from `Sourceforge main page`_
-        
-        .. _`Sourceforge main page`: http://sourceforge.net/projects/pgapy/
-        
-        or checkout from Github_
-        
-        .. _`Github`: http://github.com/schlatterbeck/pgapy
-        
-        or directly install via pypi.
-        
-        Installation
-        ------------
-        
-        PGApy, as the name suggests, supports parallelizing the evaluation
-        function of the genetic algorithm. This uses the Message Passing
-        Interface (MPI_) standard.
-        
-        To install a *serial* version (without parallel programming using MPI_)
-        you can simply install from pypi using ``pip``. Alternatively when you
-        have unpacked or checked out from sources you can install with::
-        
-         python3 setup.py install --prefix=/usr/local
-        
-        If you want a parallel version using an MPI_ (Message-Passing Interface)
-        library you will have to install a parallel version of PGAPack_ first.
-        The easiest way to do this is to use `my pgapack debian package builder`_
-        from github. Clone this repository, check out the branch ``master``,
-        install the build dependencies, they're listed in the file
-        ``debian/control`` and build the debian packages using::
-        
-          dpkg-buildpackage -rfakeroot
-        
-        This builds pgapack debian packages for *all* supported MPI libraries in
-        debian, currently these are ``mpich``, ``openmpi``, and ``lam``. In addition
-        to the MPI libraries a serial version of the pgapack library is also
-        built. Proceed by installing the package pgapack and the MPI backend
-        library of choice. If you don't have a preference for an MPI library,
-        ``libpgapack-openmpi`` is the package that uses the Debians default
-        preferences of an MPI library.
-        
-        Once a parallel version of PGAPack_ is installed, you can install PGApy
-        as follows: You set environment variables for the ``PGA_PARALLEL_VARIANT``
-        (one of ``mpich``, ``openmpi``, or ``lam``) and set the ``PGA_MODULE`` to
-        ``module_from_parallel_install``. Finally you envoke the setup, e.g.::
-        
-         export PGA_PARALLEL_VARIANT=openmpi
-         export PGA_MODULE=module_from_parallel_install
-         python3 setup.py install --prefix=/usr/local
-        
-        Note that the same works with ``pip install``, i.e., after installation
-        of a parallel version of PGAPack_ you can directly install with ``pip``::
-        
-         export PGA_PARALLEL_VARIANT=openmpi
-         export PGA_MODULE=module_from_parallel_install
-         pip install pgapy
-        
-        or alternatively depending on how pip is installed on your system::
-        
-         python3 -m pip install pgapy
-        
-        If your MPI library is installed in a different place you should study
-        the *Extension* configurations in ``setup.py`` to come up with an
-        Extension definition that fits your installation. If your installation
-        is interesting to more people, feel free to submit a patch that adds
-        your Extension-configuration to the standard ``setup.py``.
-        
-        Running with MPI
-        ----------------
-        
-        To run a parallel version with MPI_, a parallel version must be
-        installed, see above in section Installation_.
-        
-        For a serial version, PGAPy makes sure that the otimization is aborted
-        if an exception occurs in the ``evaluate`` function. This is currently not
-        the case for MPI, because the framework currently does not support
-        returning information to the rank-0 MPI leader process. A workaround is
-        as follows: Rename your ``evaluate`` method to ``_evaluate`` and catch
-        exceptions in a new ``evaluate`` method that wraps ``_evaluate``.
-        Call ``MPI_Abort`` if an exception occurs::
-        
-            import traceback
-            import sys
-        
-            ...
-        
-            def evaluate (self, p, pop):
-                try:
-                    return self._evaluate (p, pop)
-                except Exception:
-                    # Optionally log exception here
-                    print (traceback.format_exc ())
-                    pga.MPI_Abort (1)
-                    sys.exit (1)
-        
-        Testing
-        -------
-        
-        For testing |--| preferrably before installation you can build locally::
-        
-            python3 setup.py build_ext --inplace
-        
-        After this you have a ``pga.*.so`` file in the local directory. Now you
-        can run the tests with::
-        
-            python3 -m pytest test
-        
-        This runs all the tests and can take a while. Note that the tests run
-        most of the examples in the ``examples`` directory with different
-        command line parameters where available. To perform several optimization
-        runs in a single (Python-) process, we must call ``MPI_Init``
-        *explicitly* (and not relying on PGAPack_ to call it implicitly). This is
-        because ``MPI_Init`` may be called only once per process. Calling of
-        ``MPI_Init`` and ``MPI_Finalize`` is handled in a fixture in
-        ``test/conftest.py``
-        
-        Coverage
-        ++++++++
-        
-        For the python examples, the coverage can be computed with::
-        
-          python3 -m pytest --cov examples test
-        
-        or more verbose including untested lines with::
-        
-          python3 -m pytest --cov-report term-missing --cov examples test
-        
-        Performing a coverage analysis for the C code in ``pgamodule.c`` is
-        currently possible only on Linux |--| at least, since I'm developing on
-        Linux this is the architecture where I've found out how to perform
-        coverage analysis including the C code.
-        To compile for coverage analysis::
-        
-          export CFLAGS=-coverage
-          python3 setup.py build_ext --inplace
-        
-        This will create a file ending in ``.gcno`` under the ``build`` directory,
-        typically something like ``build/temp.linux-x86_64-3.9`` when using
-        ``python3.9`` on the ``x86_64`` architecture. Running the tests will
-        create statistics data files with ending ``.gcda``. These are data files
-        for the GNU profiler ``gcov``. From these, ``.html`` files can be
-        generated that can be inspected with a browser::
-        
-          lcov --capture --directory . --output-file coverage.info
-          genhtml coverage.info --output-directory coverage_out
-        
-        Note that the ``lcov`` program is part of the linux distribution.
-        
-        Running under MPI
-        +++++++++++++++++
-        
-        The tests can be directly run under MPI. Note that currently the
-        ``--with-mpi`` option of ``pytest`` is *not* supported. This option
-        asumes that the package ``mpi4py`` is used. But ``pgapy`` uses only
-        calls from pgapack, which in turn calls MPI.
-        
-        Running under MPI is done using::
-        
-         mpirun $MPI_OPTIONS python3 -m pytest test
-        
-        The ``MPI_OPTIONS`` can be, e.g.::
-        
-            MPI_OPTIONS=--machinefile ~/.mpi-openmpi --np 8
-        
-        which would use a machine definition file for openmpi in your home
-        directory and eight processes.
-        
-        Running under MPI is especially useful for determining C code coverage.
-        Asuming a parallel version of ``openmpi`` is installed, the code can be
-        compiled with::
-        
-         PGA_PARALLEL_VARIANT=openmpi
-         PGA_MODULE=module_from_parallel_install
-         export CFLAGS=-coverage
-         python3 setup.py build_ext --inplace
-        
-        Note that the coverage analysis uses files in the build directory which
-        need to be present before a parallel version can be started. Otherwise
-        each parallel instance would try to create the coverage files resulting
-        in race conditions. Once the coverage files are in place, the coverage
-        framework ensures proper locking so that no two processes write
-        concurrently to the same coverage files.
-        
-        Creating the coverage files is best achieved by running the tests
-        without MPI first and then running the same version with a number of
-        processes under MPI. Running under MPI shows that the serialization and
-        deserialization code in ``pgamodule.c`` is called.
-        
-        As of this writing we get::
-        
-         Lines:      1423    1475    96.5 %
-         Functions:   131     133    98.5 %
-        
-        
-        References
-        ----------
-        
-        .. [1]  Georges Harik. Finding multiple solutions in problems of bounded
-                difficulty. IlliGAL Report 94002, Illinois Genetic Algorithm Lab,
-                May 1994.
-        .. [2]  Georges R. Harik. Finding multimodal solutions using restricted
-                tournament selection. In Eshelman [3]_, pages 24–31.
-        .. [3]  Larry J. Eshelman, editor. *Proceedings of the 6th International
-                Conference on Genetic Algorithms (ICGA)*. Morgan Kaufmann, July 1995.
-        .. [4]  Martin Pelikan. *Hierarchical Bayesian Optimization Algorithm:
-                Toward a New Generation of Evolutionary Algorithms*, volume 170 of
-                Studies in Fuzziness and Soft Computing.  Springer, 2005.
-        .. [5]  Rainer Storn and Kenneth Price. Differential evolution |--| a simple
-                and efficient heuristic for global optimization over continuous
-                spaces. *Journal of Global Optimization*, 11(4):341–359, December
-                1997.
-        .. [6]  Kenneth V. Price, Rainer M. Storn, and Jouni A. Lampinen.
-                *Differential Evolution: A Practical Approach to Global
-                Optimization.*  Springer, Berlin, Heidelberg, 2005.
-        .. [7]  Kalyanmoy Deb, Amrit Pratap, Sameer Agarwal, and T. Meyarivan. A
-                fast and elitist multiobjective genetic algorithm: NSGA-II. *IEEE
-                Transactions on Evolutionary Computation*, 6(2):182–197, April 2002.
-        .. [8]  Kalyanmoy Deb and Himanshu Jain. An evolutionary many-objective
-                optimization algorithm using reference-point-based nondominated
-                sorting approach, part I: Solving problems with box constraints.
-                *IEEE Transactions on Evolutionary Computation*, 18(4):577–601,
-                August 2014.
-        .. [9]  Himanshu Jain and Kalyanmoy Deb. An evolutionary many-objective
-                optimization algorithm using reference-point-based nondominated
-                sorting approach, part II: Handling constraints and extending to
-                an adaptive approach. *IEEE Transactions on Evolutionary
-                Computation*, 18(4):602–622, August 2014.
-        .. [10] Tetsuyuki Takahama and Setsuko Sakai. Constrained optimization
-                by the |epsilon| constrained differential evolution with an
-                archive and gradient-based mutation. In [11]_.
-        .. [11] *IEEE Congress on Evolutionary Computation (CEC)*. Barcelona,
-                Spain, July 2010.
-        .. [12] Indraneel Das and J. E. Dennis. Normal-boundary intersection: A new
-                method for generating the pareto surface in nonlinear multicriteria
-                optimization problems. SIAM Journal on Optimization, 8(3):631–657,
-                August 1998.
-        
-        Changes
-        -------
-        
-        Version 2.2.1: MPI_Abort
-        
-        - Add MPI_Abort to the wrapper
-        - Include ``mpi_stub.c`` in the release (this is missing if some env
-          variables are set, see above in Installation)
-        
-        Version 2.2: Module directory
-        
-        - Put the pga C-module inside a pga module
-        - Add several python-only modules to pga
-        - pga.__init__ exports everything to this is compatible
-        - pga.random includes a python Random class based on the pgapack random
-          number generator
-        
-        Version 2.1: Regression test
-        
-        - PGAPack bug-fixes discovered during testing
-        - Bug-fixes of python wrapper
-        - Lots of tests with coverage of wrapper C-code > 90%
-        
-        Version 2.0: User defined data types
-        
-        - Implement user defined data types, note that your data type can be
-          variable-size, e.g., a tree data structure. The framework takes care
-          of serializing the data type and transmitting it to a remote MPI
-          process if using a parallel version.
-        - When duplicate checking is enabled with the constructor parameter
-          ``no_duplicates``, the underlying pgapack code now uses a hash table.
-          This means the effort is no longer quadratic in the population size
-          but linear.
-        - Example of Genetic Programming (GP) in the ``examples/gp`` directory
-        - Rename the gene_difference method to gene_distance
-        
-        Version 1.8: Epsilon-constrained optimization
-        
-        - Epsilon-constrained optimization
-        - Precision for printing evals in multi-objective optimization, use this
-          feature for making regression-test work on AMD where a floating-point
-          difference in the 16th or so decimal place made a test fail
-        - Crossover for permutations
-        - Version-numbers: try to match pgapack, we might still diverge in the
-          last digit, though
-        
-        Version 1.2: Many-objective optimization with NSGA-III
-        
-        - Implement NSGA-III
-        
-        Version 1.1.6: Polynomial mutation and simulated binary crossover (SBX)
-        
-        - Simulated binary crossover (SBX)
-        - Polynomial mutation
-        
-        Version 1.1.1-1.1.5: Small PGAPack updates, fixes for non-debian
-        
-        - Fix setup.py for non-debian systems
-        - Update to latest PGAPack with small changes
-        
-        Version 1.1: Add multi-objective optimization with NSGA-II
-        
-        - Wrap latest pgapack version 1.4
-        - This add multi-objective optimization using the Nondominated Sorting
-          Genetic Algorithm version 2 (NSGA-II) by Deb et. al. This makes use of
-          the previously-introduced option to return more than one value in the
-          objective function. To use the feature you need to set the
-          num_constraint parameter to a value that leave some of the function
-          values returned by your evaluation function as objective function
-          values (and not as constraints). See example in examples/multi.py.
-        
-        Version 1.0: Add constraint handling
-        
-        - Wrap latest pgapack version 1.3
-        - This adds auxiliary evaluations. Now your evaluation function can
-          return *multiple* floating-point values as a sequence if you set the
-          num_eval parameter >1 in the constructor. Currently additional
-          evaluation values are used for constraint handling. Constraint values
-          are minimized.  Once they reach zero or a negative value they no
-          longer count: The sum of all positive constraints is the overall
-          constraint violation.  For details see paper by Deb, 2000, see user
-          guide for citation. If you're not using constraints, nothing in your
-          code needs changes.
-        - This release may change the path an optimization takes. So for the
-          same seed of the random number generator you will get a different
-          result, at least if during the search there are individuals with the
-          same evaluation (and different genetic material). This is due to a
-          change of the sort function in pgapack (it switched to a stable sort
-          from the C standard library).
-        
-        Version 0.9: Allow installation of parallel version
-        
-        - Pass argv (or sys.argv) to PGACreate
-        - Add a stanza to setup.py to allow a parallel installation with a given
-          pgapack variant compiled for an MPI library. This currently needs a
-          pre-installed pgapack debian package.
-        
-        Version 0.8: Bugfix in real mutation
-        
-        - Fix a core-dump in the latest pgapack
-        
-        Version 0.7: Major changes in wrapping
-        
-        - Now Differential Evolution is implemented, see the minfloat example
-          and the user guide of pgapack.
-        
-        Version 0.6: Major changes in wrapping
-        
-        - Now the wrapping uses the standard Python recommendations on how to
-          create a custom class.
-        - Update documentation
-        - Rename ``fitness_cmax`` (from ``fitness_cmax_value``)
-        - Better error checking of parameters
-        
-        Version 0.5: Bug-fix release
-        
-        - Now the ``setup.py`` works, previous version had an encoding problem
-        - Wrap some minor new methods
-        - Bug-fix in PGAPack truncation selection
-        
-        Version 0.4: Bundle PGAPack
-        
-        - The PGAPack package is now included as a git submodule. By default we
-          build against this library
-        - License fixes: The module long shipped a ``COPYING`` file that includes
-          the 2-clause BSD license. But the headers of ``setup.py`` and ``pgamodule.c``
-          still included another license. This has been corrected.
-        
-        Version 0.3: Feature enhancements, Bug fixes
-        
-        Port to Python3, Python2 is still supported, license change.
-        
-        - C-Code of wrapper updated to support both, Python2 and Python3
-        - Update documentation
-        - Fix some memory leaks that could result when errors occurred during
-          some callback methods
-        - License change: We now have the 2-clause BSD license (similar to the
-          MPICH license of PGAPack), this used to be LGPL.
-        
-        Version 0.2: Feature enhancements, Bug fixes
-        
-        64 bit support, more PGAPack functions and attributes wrapped,
-        Readme-update: Sourceforge logo, Changes chapter.
-        
-        - Bug-fixes for 64 bit architectures
-        - More functions and attributes of PGAPack wrapped
-        - Add a build-rule to ``setup.py`` to allow building for standard-install
-          of PGAPack |--| this currently needs editing of ``setup.py`` |--| should use
-          autodetect here but this would require that I set up a machine with
-          standard install of PGAPack for testing.
-        - Add Sourceforge logo as required
-        - Add Changes chapter for automagic releases
-        - Add the ``__module__`` string to class ``PGA`` in module ``pga``. Now
-          calling:: ``help (pga)`` in python works as expected, previously no
-          help-text was given for the included module
-        
-        Version 0.1: Initial freshmeat announcement
-        
-        PGAPy is a wrapper for PGAPack, the parallel genetic algorithm library,
-        a powerful genetic algorithm library. PGAPy wraps this library for use
-        with Python. Pgapack is one of the most complete and accurate genetic
-        algorithm implementations out there with a lot of features for
-        experimentation.
-        
-        - Initial Release
-        
-        .. _`PGAPack Readme`:
-           https://github.com/schlatterbeck/pgapack/blob/master/README.rst
-        .. _PGAPack:          http://ftp.mcs.anl.gov/pub/pgapack/
-        .. _`PGAPack fork on github`: https://github.com/schlatterbeck/pgapack
-        .. _MPI: http://mpi-forum.org/
-        .. _`my pgapack debian package builder`:
-            https://github.com/schlatterbeck/debian-pgapack
-        
-Platform: UNKNOWN
+Author-email: Ralf Schlatterbeck <rsc@runtux.com>
+License: BSD License
+Project-URL: Homepage, https://github.com/schlatterbeck/pgapy
+Project-URL: Bug Tracker, https://github.com/schlatterbeck/pgapy/issues
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Education
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: C
 Classifier: Programming Language :: Python
 Classifier: Topic :: Education
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: Topic :: Software Development :: Libraries
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Requires-Python: >=3.7
 Description-Content-Type: text/x-rst
+License-File: COPYING
+
+PGAPy: Python Wrapper for PGAPack Parallel Genetic Algorithm Library
+====================================================================
+
+.. |--| unicode:: U+2013   .. en dash
+.. |epsilon| unicode:: U+03B5 .. epsilon
+
+:Author: Ralf Schlatterbeck <rsc@runtux.com>
+
+News
+----
+
+News 04-2023:
+
+- The last build on PyPi was broken for serial installs, it was missing
+  the ``mpi_stub.c`` needed for the serial version. Parallel installs
+  were still possible so I didn't notice, sorry!
+- Add MPI_Abort to the wrapper, it is called with::
+
+    pga.MPI_Abort (errcode)
+
+  See below in secion `Running with MPI`_ how this can be used to abort
+  the MPI run in case of exception in the ``evaluate`` method.
+
+News 12-2022: Add regression test and update to new upstream with
+several bug-fixes. Includes also some bug fixes in wrapper.
+
+News 10-2022: Add user defined datatypes. Example in ``examples/gp`` use
+user defined data types to implement genetic programming (we represent
+expressions by a tree data structure). This uses the new serialization
+API in pgapack to transfer a Python pickle representation to peer MPI
+processes. Also incorporate the latest changes in pgapack which
+optimizes duplicate checking. This is of interest for large population
+sizes in the genetic programming examples. Note that the
+``gene_difference`` method has been renamed to ``gene_distance``.
+
+News 08-2022: Epsilon-constrained optimization and a crossover variant
+that preserves permutations (so with integer genes the gene can represent
+a permutation).
+
+News 03-2022: Attempt to make this installable on Windows. This involves
+some workaround in the code because the visual compiler does not support
+certain C99 constructs.
+
+News 01-2022: This version wraps multiple evaluation with NSGA-III (note
+the additional 'I').
+
+News 12-2021: This version wraps multiple evaluation values from your
+objective function: Now you can return more than one value to either use
+it for constraints (that must be fulfilled before the objective is
+optimized) or for multi-objective optimization with the Nondominated
+Sorting Genetic Algorithm V.2 (NSGA-II). You can combine both,
+multi-objective optimization and constraints.
+
+News: This version wraps the Differential Evolution method (that's quite
+an old method but is newly implemented in pgapack).
+
+Introduction
+------------
+
+PGAPy is a wrapper for PGAPack, the parallel genetic algorithm library
+(see `PGAPack Readme`_), a powerfull genetic algorithm library by
+D. Levine, Mathematics and Computer Science Division Argonne National
+Laboratory. The library is written in C. PGAPy wraps this library for
+use with Python. The original PGAPack library is already quite old but
+is one of the most complete and accurate (and fast, although this is not
+my major concern when wrapping it to python) genetic algorithm
+implementations out there with a lot of bells and whistles for
+experimentation. It also has shown a remarkably small number of bugs
+over the years. It supports parallel execution via the message
+passing interface MPI_ in addition to a normal "serial" version. That's
+why I wanted to use it in Python, too.
+
+To get started you need the PGAPack library, although
+it now comes bundled with PGApy, to install a *parallel* version you
+currently need a pre-installed PGAPack_ compiled for the MPI library of
+choice. See `Installation`_ section for details.
+
+There currently is not much documentation for PGAPy.
+You really, absolutely need to read the documentation that comes
+with PGAPack.
+The PGAPack user guide is now shipped together with PGAPy. It is
+installed together with some examples in share/pgapy, wherever the
+Python installer decides to place this in the final installation
+(usually ``/usr/local/share`` on Linux).
+
+The original PGAPack library can still be downloaded from the PGAPack_
+ftp site, it is written in ANSI C but will probably not compile against
+a recent version of MPI_. It will also not work with recent versions of
+PGAPy. Note that this version is not actively maintained. I've started a
+`PGAPack fork on github`_ where I've ported the library to the latest
+version of the MPI_ standard and have fixed some minor inconsistencies
+in the documentation. I've also implemented some new features, notably
+enhancements in selection schemes, a new replacement strategy called
+*restricted tournament replacement* [1]_, [2]_, [4]_ and, more recently,
+the differential evolution strategy [5]_, [6]_. In addition this version
+now supports multi objective optimization with NSGA-II [7]_ and
+many-objective optimization with NSGA-III [8]_, [9]_. It also supports
+the Epsilon Constraint method [10]_.
+
+Note: When using NSGA_III replacement for multi (or many-) objective
+optimization you need to either
+
+- set reference points on the hyperplane intersecting all axes at
+  offset 1. These reference points can be obtained with the convenience
+  function ``pga.das_dennis``, it creates a regular set of reference points
+  using an algorithm originally publised by I. Das and J. E. Dennis [12]_.
+  These points are then passed as the parameter ``reference_points`` to
+  the ``PGA`` constructor.
+
+  See ``examples/dtlz2.py`` for a usage example and the user guide for
+  the bibliographic reference. The function gets the dimensionality of
+  the objective space (``num_eval`` minus ``num_constraint``) and the
+  number of partition to use.
+- Or set reference directions (in the objective space) with the
+  ``reference_directions`` parameter, number of partitions for these
+  directions with the ``refdir_partitions`` parameter (see
+  ``das_dennis`` above, this uses Das/Dennis points internally), and a
+  scale factor with the parameter ``refdir_scale``.
+
+You can set both, these parameters are not mutually exclusive.
+
+I'm mainly testing pgapy on Linux. But I've recently made it run on
+Windows, too but I'm not very actively testing on Windows. Let me know
+if you run it on Windows, sucessfully or not sucessfully.
+
+As mentioned above, you can find my `PGAPack fork on github`_, this
+repository has the three upstream releases as versions in git and
+contains some updates concerning support of newer MPI_ versions and
+documentation updates.  I've also included patches in the git repository
+of the Debian maintainer of the package, Dirk Eddelbuettel.
+I'm actively maintaining that branch, adding new features and bug-fixes.
+
+To get you started, I've included some very simple examples in
+``examples``, e.g., ``one-max.py`` implements the "Maxbit" example
+similar to one in the PGAPack documentation. The examples were inspired
+by the book "Genetic Algorithms in Python" but are written from scratch
+and don't include any code from the book. The examples illustrates
+several points:
+
+- Your class implementing the genetic algorithm needs to inherit from
+  pga.PGA (pga is the PGAPy wrapper module).
+- You need to define an evaluation function called ``evaluate`` that
+  returns a sequence of numbers indicating the fitness of the gene given.
+  It gets the parameters ``p`` and ``pop`` that can be used to fetch allele
+  values from the gene using the ``get_allele`` method, for more details
+  refer to the PGAPack documentation. The number of evaluations returned
+  by your function is defined with the constructor parameter
+  ``num_eval``, the default for this parameter is 1. If your evaluation
+  function does not return multiple evaluations (with the default
+  setting of ``num_eval``) you can either return a one-element sequence
+  or a single return value.
+- When using multiple evaluations, these can either be used for
+  constraints (the default) or for multi-objective optimization. In the
+  latter case, the number of constraints (which by default is one less
+  than the number of evaluations set with the parameter ``num_eval``)
+  must be set to a number that leaves at least two evaluations for
+  objectives. The number of constraints can be set with the parameter
+  ``num_constraint``. When using multi-objective optimization, you need
+  one of the two replacement-types ``PGA_POPREPL_NSGA_II`` or
+  ``PGA_POPREPL_NSGA_III``, set this with the ``pop_replace_type`` parameter.
+- You *can* define additional functions overriding built-in functions
+  of the PGAPack library, illustrated by the example of
+  ``print_string``.  Note that we could call the original print_string
+  method of our PGA superclass.  In the same way you can implement,
+  e.g., your own crossover method.
+- The constructor of the class needs to define the Gene type, in the
+  examples we use int and bool built-in datatypes.
+- The length of the gene needs to be given in the constructor.
+- We often want to maximize the numbers returned by our evaluation
+  function, set the parameter ``maximize`` to False if you want to
+  minimize.
+- For non-binary genes we can define an array of init values, each entry
+  containing a sequence with lower and upper bound. The array has to
+  have the length of the gene. Note that the upper bound is *included*
+  in the range of possible values (unlike the python range operator but
+  compatible with the PGAPack definition).
+- In the constructor of the class we can add parameters of the genetic
+  algorithm. Not all parameters of PGAPack are wrapped yet, currently
+  you would need to consult the sourcecode of PGAPy to find out which
+  parameters are wrapped. In the example we define several print
+  options.
+- Finally the genetic algorithm is started with the ``run`` method.
+
+Naming conventions in PGAPy
+---------------------------
+
+When you extend PGAPy |--| remember not all functions of PGAPack are
+wrapped yet and you may need additional functions |--| you should stick to
+my naming conventions when making changes.
+The following naming conventions were used for the wrapper:
+
+- Constants of PGAPack like ``PGA_REPORT_STRING`` are used as-is in
+  uppercase. These constants can be directly imported from the wrapper
+  module. Not all constants are wrapped so far, if you need more, add
+  them to the constdef array in pgamodule.c and send_ me a patch.
+- For methods of the pga.PGA class I've removed the ``PGA`` prefix used
+  throughout PGAPack and converted the method to lowercase with
+  underscores between uppercase words in the original function name, so
+  ``PGARun`` becomes ``run``, ``PGACheckStoppingConditions`` becomes
+  ``check_stopping_conditions``. An exception of the lowercase-rule is
+  whenever a name contains "GA" (for "genetic algorithm"), So
+  ``PGASetMaxGAIterValue`` becomes ``max_GA_iter``.
+- Where possible I've made a single class method where PGAPack needs a
+  separate function for each datatype, so ``PGAGetBinaryAllele``,
+  ``PGAGetCharacterAllele``, ``PGAGetIntegerAllele``, ``PGAGetRealAllele`` all
+  become ``get_allele``. Same holds true for ``set_allele``.
+- Whenever a name in PGAPack has a "Value" or "Flag" suffix, I've left
+  this out, so ``PGAGetFitnessCmaxValue`` becomes ``fitness_cmax``
+  and ``PGAGetMutationAndCrossoverFlag`` becomes
+  ``mutation_and_crossover``, the only exception to this rule is for the
+  two functions ``PGAGetMutationRealValue`` and
+  ``PGAGetMutationIntegerValue`` which become ``mutation_value`` not
+  just ``mutation``.
+- Some fields can take multiple values (they are implemented by ORing
+  integer constants, in python they are specified as a list or tuple of
+  constants). These are converted to plural (if not already plural in
+  PGAPack), e.g., ``PGASetStoppingRuleType`` becomes ``stopping_rule_types``.
+- Internal method names in the wrapper program have a leading PGA\_ |--| so
+  the class method ``set_allele`` is implemented by the C-function
+  ``PGA_set_allele`` in ``pgamodule.c``.
+
+Constructor Parameters
+----------------------
+
+PGAPack_ has a lot of ``PGASet`` and ``PGAGet`` functions for setting
+parameters. These are reflected in constructor parameters on the one hand
+and in (typically read-only, but see below) properties of a ``PGA``
+object on the other hand. The
+following table gives an overview of all the original PGAPack_ names and
+the names of the python wrapper. For the PGAPack_ name I've only listed
+the ``PGASet`` function, in many cases there is a corresponding
+``PGAGet`` function. If a corresponding read-only property exists for a
+constructor parameter this is indicated in the "Prop" column. In some
+cases properties are missing because no corresponding ``PGAGet`` function
+is implemented in PGAPack_, in other cases returning a numeric value that
+has a symbolic constant in PGApy doesn't make much sense.
+
+The properties have the same name as the constructor parameter.
+There are Properties that don't have a corresponding constructor
+parameter, namely the ``eval_count`` property (returning the count of
+function evaluations), the
+``GA_iter`` property that returns the current GA generation, and the
+``mpi_rank`` property that returns the MPI rank of the current process
+(this is sorted under PGAGetRank).
+
+In the type
+column I'm listing the Python type. If the type is followed by a number,
+more than one item of that type is specified (a sequence in Python). Some
+entries contain "sym", these are integer values with a symbolic constant,
+the value "msym" indicates that several values denoted by a list of
+symbolic constants can be given. A special case are the
+``PGASetRealInitRange``, ``PGASetRealInitPercent``,
+``PGASetIntegerInitRange`` functions. These take two values for *each
+allele* of the gene. In python this is a sequence of 2-tuples.
+Note that this means that you can have different ranges of allowed values
+for each allele.
+
+The ``num_eval`` property is special: Due to limitations of the C
+programming language, for multiple evaluations in C the first evaluation
+is returned as the function return-value of the ``evaluate`` function
+and all other parameters are returned in an auxiliary array. PGAPack_
+specifies the number of auxiliary evaluations to be returned. In Python
+the evaluation function can always return a sequence of evaluation
+values and the ``num_eval`` is one more than ``PGAGetNumAuxEval`` would
+return. The default for ``num_eval`` is 1.
+
+The first two (mandatory) constructor parameters are the type of the gene
+(this takes a Python type, e.g., ``bool`` for a binary genome or ``int``
+for an integer genome) and the length. Note that the ``string_length`` is
+implicitly set with the ``length`` parameter. The ``string_length`` is
+also available as the length of the ``PGA`` object using the Python
+built-in ``len`` function.
+
+Some properties can now also be set *during* the run of the optimizer.
+These currently are ``crossover_prob``, ``epsilon_exponent``,
+``multi_obj_precision``, ``p_tournament_prob``, and
+``uniform_crossover_prob``. Just assign to the member variable of
+the optimizer (child of PGA.pga) object.
+
+==================================== ================================= ====== ====
+PGAPack name                         Constructor parameter             Type   Prop
+==================================== ================================= ====== ====
+``PGASetCrossoverBoundedFlag``       ``crossover_bounded``             int    yes
+``PGASetCrossoverBounceBackFlag``    ``crossover_bounce_back``         int    yes
+``PGASetCrossoverSBXEta``            ``crossover_SBX_eta``             float  yes
+``PGASetCrossoverSBXOncePerString``  ``crossover_SBX_once_per_string`` int    yes
+``PGASetCrossoverProb``              ``crossover_prob``                float  yes
+``PGASetCrossoverType``              ``crossover_type``                sym    no
+``PGASetDEAuxFactor``                ``DE_aux_factor``                 double yes
+``PGASetDECrossoverProb``            ``DE_crossover_prob``             double yes
+``PGASetDECrossoverType``            ``DE_crossover_type``             sym    no
+``PGASetDEDither``                   ``DE_dither``                     double yes
+``PGASetDEDitherPerIndividual``      ``DE_dither_per_individual``      bool   yes
+``PGASetDEJitter``                   ``DE_jitter``                     double yes
+``PGASetDENumDiffs``                 ``DE_num_diffs``                  int    yes
+``PGASetDEProbabilityEO``            ``DE_probability_EO``             double yes
+``PGASetDEScaleFactor``              ``DE_scale_factor``               double yes
+``PGASetDEVariant``                  ``DE_variant``                    sym    yes
+``PGASetEpsilonExponent``            ``epsilon_exponent``              float  yes
+``PGASetEpsilonGeneration``          ``epsilon_generation``            int    yes
+``PGASetEpsilonTheta``               ``epsilon_theta``                 int    yes
+``PGAGetEvalCount``                  ``eval_count``                    int    yes
+``PGASetFitnessCmaxValue``           ``fitness_cmax``                  float  yes
+``PGASetFitnessMinType``             ``fitness_min_type``              sym    yes
+``PGASetFitnessType``                ``fitness_type``                  sym    yes
+``PGAIntegerSetFixedEdges``          ``fixed_edges``                          no
+``PGAIntegerSetFixedEdges``          ``fixed_edges_symmetric``         bool   no
+``PGAGetGAIterValue``                ``GA_iter``                       int    yes
+``PGASetIntegerInitPermute``         ``integer_init_permute``          int2   no
+``PGASetIntegerInitRange``           ``init``                                 no
+``PGASetMaxFitnessRank``             ``max_fitness_rank``              float  yes
+``PGASetMaxGAIterValue``             ``max_GA_iter``                   int    yes
+``PGASetMaxNoChangeValue``           ``max_no_change``                 int    no
+``PGASetMaxSimilarityValue``         ``max_similarity``                int    yes
+``PGASetMixingType``                 ``mixing_type``                   sym    no
+``PGASetMultiObjPrecision``          ``multi_obj_precision``           int    yes
+``PGASetMutationAndCrossoverFlag``   ``mutation_and_crossover``        int    yes
+``PGASetMutationBounceBackFlag``     ``mutation_bounce_back``          int    yes
+``PGASetMutationBoundedFlag``        ``mutation_bounded``              int    yes
+``PGASetMutationIntegerValue``       ``mutation_value``                int    yes
+``PGASetMutationOrCrossoverFlag``    ``mutation_or_crossover``         int    yes
+``PGASetMutationPolyEta``            ``mutation_poly_eta``             float  yes
+``PGASetMutationPolyValue``          ``mutation_poly_value``           float  yes
+``PGASetMutationProb``               ``mutation_prob``                 float  yes
+``PGASetMutationRealValue``          ``mutation_value``                float  yes
+``PGASetMutationType``               ``mutation_type``                 sym    no
+``PGASetNoDuplicatesFlag``           ``no_duplicates``                 int    no
+``PGASetNumAuxEval``                 ``num_eval``                      int    yes
+``PGASetNumConstraint``              ``num_constraint``                int    yes
+``PGASetNumReplaceValue``            ``num_replace``                   int    yes
+``PGASetPopSize``                    ``pop_size``                      int    yes
+``PGASetPopReplaceType``             ``pop_replace_type``              sym    no
+``PGASetPrintFrequencyValue``        ``print_frequency``               int    yes
+``PGASetPrintOptions``               ``print_options``                 msym   no
+``PGASetPTournamentProb``            ``p_tournament_prob``             float  yes
+``PGASetRandomizeSelect``            ``randomize_select``              int    yes
+``PGASetRandomSeed``                 ``random_seed``                   int    yes
+``PGAGetRank``                       ``mpi_rank``                      int    yes
+``PGASetRealInitRange``              ``init``                                 no
+``PGASetRealInitPercent``            ``init_percent``                         no
+``PGASetReferenceDirections``        ``refdir_partitions``             int    no
+``PGASetReferenceDirections``        ``refdir_scale``                  double no
+``PGASetReferenceDirections``        ``reference_directions``                 no
+``PGASetReferencePoints``            ``reference_points``                     no
+``PGASetRestartFlag``                ``restart``                       int    yes
+``PGASetRestartFrequencyValue``      ``restart_frequency``             int    yes
+``PGASetRTRWindowSize``              ``rtr_window_size``               int    yes
+``PGASetSelectType``                 ``select_type``                   sym    no
+``PGASetStoppingRuleType``           ``stopping_rule_types``           msym   no
+``PGASetStringLength``               ``string_length``                 int    yes
+``PGASetSumConstraintsFlag``         ``sum_constraints``               int    yes
+``PGASetTournamentSize``             ``tournament_size``               int    yes
+``PGASetTournamentWithReplacement``  ``tournament_with_replacement``   int    yes
+``PGASetTruncationProportion``       ``truncation_proportion``         float  yes
+``PGASetUniformCrossoverProb``       ``uniform_crossover_prob``        float  yes
+==================================== ================================= ====== ====
+
+Note: The mutation_or_crossover and mutation_and_crossover parameters are
+deprecated, use mixing_type instead!
+
+PGA Object Methods
+------------------
+
+The following are the methods that can be used during the run of the
+genetic search. The ``run`` method is used to start the search. This can
+be used, to, e.g., set an allele during hill-climbing in a custom
+``endofgen`` method. Note that some methods only apply to certain gene
+types, e.g. the ``encode_int_`` methods can only be used on binary
+alleles (they encode an integer value as a binary or gray code
+representation into the gene). Other methods take or return different
+types depending on the type of gene, e.g. ``get_allele`` or
+``set_allele``, they call different backend functions depending on the
+gene type. With the ``set_random_seed`` method, the random number
+generator can be re-seeded. It is usually best to seed the generator
+once at (before) the beginning by specifying ``random_seed`` in the
+constructor. For further details consult the user guide.
+The method ``get_evaluation`` will return a double for a single
+evaluation and a tuple of double for multiple evaluations (when num_eval
+is >1)
+
+============================= ================== ===========================
+Method                        Parameters         Return
+============================= ================== ===========================
+``check_stopping_conditions``                    True if stop should occur
+``encode_int_as_binary``      *p, pop,*          None
+                              *frm, to, val*
+``encode_int_as_gray_code``   *p, pop,*          None
+                              *frm, to, val*
+``encode_real_as_binary``     *p, pop, frm, to*  None
+                              *l, u, val*
+``encode_real_as_gray_code``  *p, pop, frm, to*  None
+                              *l, u, val*
+``euclidian_distance``        *p1, pop1*         float
+                              *p2, pop2*
+``fitness``                   *pop*              None
+``get_allele``                *p, pop, index*    allele value
+``get_best_index``            *pop*              index of best string
+``get_best_report_index``     *pop, idx*         index of best eval with idx
+``get_evaluation``            *p, pop*           evaluation of *p*
+``get_evaluation_up_to_date`` *p, pop*           True if up-to-date
+``get_fitness``               *p, pop*           fitness of *p* (float)
+``get_gene``                  *p, pop*           get gene (user data types)
+``get_int_from_binary``       *p, pop, frm, to*  int
+``get_int_from_gray_code``    *p, pop, frm, to*  int
+``get_iteration``                                deprecated, use ``GA_iter``
+``get_real_from_binary``      *p, pop,*          float
+                              *frm, to, l, u*
+``get_real_from_gray_code``   *p, pop,*          float
+                              *frm, to, l, u*
+``random01``                                     float between 0 and 1
+``random_flip``               *probability*      0 or 1
+``random_gaussian``           *mean, stddev*     float
+``random_interval``           *l, r*             int between l, r
+``random_uniform``            *l, r*             float between l, r
+``run``                                          None
+``select_next_index``         *pop*              index selected individual
+``set_allele``                *p, pop, i, value* None
+``set_evaluation``            *p, pop, value*    None
+``set_evaluation_up_to_date`` *p, pop, status*   None
+``set_gene``                  *p, pop, gen*      set gene (user data types)
+``set_random_seed``           *seed*             None (use constructor!)
+============================= ================== ===========================
+
+User-Methods
+------------
+
+PGAPack_ has the concept of user functions. These allow customization of
+different areas of a genetic algorihm. In Python they are implemented as
+methods that can be changed in a derived class. One of the methods that
+*must* be implemented in a derived class is the ``evaluate`` function
+(although technically it is not a user function in PGAPack). It
+interprets the gene and returns an evaluation value or a sequence of
+evaluation values if you set the ``num_eval`` constructor parameter.
+PGAPack_ computes a fitness from the raw evaluation value. For some
+methods an up-call into the PGA class is possible, for some methods this
+is not possible (and in most cases not reasonable). Note that for the
+``stop_cond`` method, the standard check for stopping conditions can be
+called with::
+
+  self.check_stopping_conditions()
+
+The following table lists the overridable methods with their parameters
+(for the function signature the first parameter *self* is omitted). Note
+that in PGAPack_ there are additional user functions that are needed for
+user-defined data types which are currently not exposed in Python. In the
+function signatures *p* denotes the index of the individual and *pop*
+denotes the population. If more than one individual is specified (e.g.,
+for crossover) these can be followed by a number. For crossover *c1* and
+*c2* denote the destination individuals (children). The *propability* for
+the mutation method is a floating-point value between 0 and 1. Remember
+to count the number of mutations that happen, and return that value for
+the mutation method!
+
+=================== ============================== ================= =======
+Method              Call Signature                 Return Value      Up-Call
+=================== ============================== ================= =======
+``check_duplicate`` *p1, pop1, p2, pop2*           True if dupe      no
+``stop_cond``                                      True to stop      no
+``crossover``       *p1, p2, p_pop, c1, c2, c_pop* None              no
+``endofgen``                                       None              no
+``evaluate``        *p, pop*                       sequence of float no
+``gene_distance``   *p1, pop1, p2, pop2*           float             no
+``hash``            *p, pop*                       int               no
+``initstring``      *p, pop*                       None              no
+``mutation``        *p, pop, propability*          #mutations        no
+``pre_eval``        *pop*                          None              no
+``print_string``    *file, p, pop*                 None              yes
+=================== ============================== ================= =======
+
+Constants
+---------
+
+The following PGAPack_ constants are available:
+
+========================== ===========================================
+Constant                   Description
+========================== ===========================================
+PGA_CROSSOVER_EDGE         Edge crossover for permutations
+PGA_CROSSOVER_ONEPT        One-point Crossover
+PGA_CROSSOVER_SBX          Simulated Binary Crossover
+PGA_CROSSOVER_TWOPT        Two-point Crossover
+PGA_CROSSOVER_UNIFORM      Uniform Crossover
+PGA_FITNESSMIN_CMAX        Map fitness by subtracting worst
+PGA_FITNESSMIN_RECIPROCAL  Map fitness via reciprocal
+PGA_FITNESS_NORMAL         Linear normalization of fitness
+PGA_FITNESS_RANKING        Linear fitness ranking
+PGA_FITNESS_RAW            Identity fitness function
+PGA_MUTATION_CONSTANT      Mutation by adding/subtracting constant
+PGA_MUTATION_GAUSSIAN      Mutation by selecting from Gaussian distribution
+PGA_MUTATION_PERMUTE       Mutation swaps two random genes
+PGA_MUTATION_POLY          Polynomial Mutation
+PGA_MUTATION_RANGE         Replace gene with uniform selection from init range
+PGA_MUTATION_UNIFORM       Mutation uniform from interval
+PGA_NEWPOP                 Symbolic constant for new population
+PGA_OLDPOP                 Symbolic constant for old population
+PGA_POPREPL_BEST           Population replacement best strings
+PGA_POPREPL_NSGA_II        Use NSGA-II replacement for multi-objective opt.
+PGA_POPREPL_NSGA_III       Use NSGA-III replacement for multi-objective opt.
+PGA_POPREPL_PAIRWISE_BEST  Compare same index in old and new population
+PGA_POPREPL_RANDOM_NOREP   Population replacement random no replacement
+PGA_POPREPL_RANDOM_REP     Population replacement random with replacement
+PGA_POPREPL_RTR            Restricted Tournament Replacement
+PGA_REPORT_AVERAGE         Report average evaluation
+PGA_REPORT_HAMMING         Report hamming distance
+PGA_REPORT_OFFLINE         Report offline
+PGA_REPORT_ONLINE          Report online
+PGA_REPORT_STRING          Report the string
+PGA_REPORT_WORST           Report the worst evaluation
+PGA_SELECT_LINEAR          Return individuals in population order
+PGA_SELECT_PROPORTIONAL    Fitness-proportional selection
+PGA_SELECT_PTOURNAMENT     Binary probabilistic tournament selection
+PGA_SELECT_SUS             Stochastic universal selection
+PGA_SELECT_TOURNAMENT      Tournament selection
+PGA_SELECT_TRUNCATION      Truncation selection
+PGA_STOP_MAXITER           Stop on max iterations
+PGA_STOP_NOCHANGE          Stop on max number of generations no change
+PGA_STOP_TOOSIMILAR        Stop when individuals too similar
+========================== ===========================================
+
+User Defined Data Types
+-----------------------
+
+The latest version of PGAPy features user defined data types. Just
+define your data type and pass it as the second parameter to the
+``PGA`` constructor. The framework will take care of serializing the
+data when transmitting via ``MPI`` (if you're running a parallel
+version).
+
+If duplicate checking is enabled via the ``no_duplicates`` constructor
+parameter, your data type needs to define a ``__hash__`` method (unless
+the python default hash method fulfills your requirements).
+
+User defined data types do not use alleles, so the normal ``get_allele``
+(and ``set_allele``) methods are not available. Instead the full
+individual can be retrieved with the ``get_gene`` method and set with
+the ``set_gene`` method.
+
+With user data types you need to define the following methods:
+
+- ``check_duplicate (self, p1, pop1, p2, pop2)`` if you enable duplicate
+  checking with the crossover parameter ``no_duplicates``. This should
+  return True when the two individuals are duplicates. Use ``get_gene``
+  to retrieve the genes for the individuals ``p1`` and ``p2`` in
+  populations ``pop1`` and ``pop2``.
+- ``crossover (self, p1, p2, ppop, c1, c2, cpop)`` for crossover
+  operation, use ``get_gene`` for getting the parent genes for the
+  parents ``p1`` and ``p2`` in generation ``ppop`` and use ``set_gene``
+  for setting the child genes ``c1`` and ``c2`` in generation ``cpop``.
+- ``initstring (self, p, pop)`` for initializing the given string, use
+  ``set_gene`` in that method for setting your object as a gene.
+- ``mutation (self, p, pop, pm)`` for the mutation operation. This
+  should return the number of mutations performed. If duplicate checking
+  is enabled, the framework will repeatedly call the mutation operator
+  for mutating a duplicate individual into another individual that is no
+  duplicate. This uses the return value of your mutation method. You
+  will enter an endless loop if your mutation operator does not
+  occasionally return an non-zero number of mutatations performed when
+  duplicate checking is enabled. The ``pm`` parameter gives the mutation
+  probability. Use ``get_gene`` for retrieving the individual to be
+  mutated and use ``set_gene`` to update this individual after mutation.
+- ``print_string (self, file, p, pop)`` to print a gene object, use
+  ``get_gene`` for retrieving the individual to be printed.
+
+For these methods it is generally a good idea to never modify an
+individual in-place: This individual may be repeatedly used in genetic
+operations (e.g. mutation and crossover), so when modifying it you will
+produce erroneous results for later genetic operations. To copy a data
+structure, python's ``deepcopy`` function in the module ``copy`` is
+usually used.
+
+In addition to the methods above you may want to define a stopping rule
+with a ``stop_cond`` method or override the way a hash is computed using
+a ``hash`` method. The default for computing a hash is to call
+``hash (gene)`` where gene is an object of the user defined data type.
+Other methods that may be used is an ``endofgen`` method, a
+``gene_distance`` method (e.g., when using Restricted Tournament
+Replacement, with ``PGA_POPREPL_RTR``), or a ``pre_eval`` method.
+
+An example with user defined data types is in ``examples/gp``: This
+implements Genetic Programming with a tree data structure. Note that the
+``Node`` class in ``gp.py`` has a ``__hash__`` method that builds a hash
+over the serialization of the tree (which is the same for individuals
+with the same tree structure).
+
+
+Missing Features
+----------------
+
+As already mentioned, not all functions and constants of PGAPack_ are
+wrapped yet |--| still for many applications the given set should be
+enough. If you need additional functions, you may want to wrap these and
+send_ me a patch.
+
+Reporting Bugs
+--------------
+
+Please use the `Sourceforge Bug Tracker`_  or the `Github Bug Tracker`_ and
+
+- give a short description of what you think is the correct behaviour
+- give a description of the observed behaviour
+- tell me exactly what you did.
+- if you can publish your source code this makes it a lot easier to
+  debug for me
+
+.. _`Sourceforge Bug Tracker`:
+    http://sourceforge.net/tracker/?group_id=152022&atid=782852
+.. _`Github Bug Tracker`:
+    https://github.com/schlatterbeck/pgapy/issues
+.. _send: mailto:rsc@runtux.com
+
+Resources
+---------
+
+Project information and download from `Sourceforge main page`_
+
+.. _`Sourceforge main page`: http://sourceforge.net/projects/pgapy/
+
+or checkout from Github_
+
+.. _`Github`: http://github.com/schlatterbeck/pgapy
+
+or directly install via pypi.
+
+Installation
+------------
+
+PGApy, as the name suggests, supports parallelizing the evaluation
+function of the genetic algorithm. This uses the Message Passing
+Interface (MPI_) standard.
+
+To install a *serial* version (without parallel programming using MPI_)
+you can simply install from pypi using ``pip``. Alternatively when you
+have unpacked or checked out from sources you can install with::
+
+ python3 setup.py install --prefix=/usr/local
+
+If you want a parallel version using an MPI_ (Message-Passing Interface)
+library you will have to install a parallel version of PGAPack_ first.
+The easiest way to do this is to use `my pgapack debian package builder`_
+from github. Clone this repository, check out the branch ``master``,
+install the build dependencies, they're listed in the file
+``debian/control`` and build the debian packages using::
+
+  dpkg-buildpackage -rfakeroot
+
+This builds pgapack debian packages for *all* supported MPI libraries in
+debian, currently these are ``mpich``, ``openmpi``, and ``lam``. In addition
+to the MPI libraries a serial version of the pgapack library is also
+built. Proceed by installing the package pgapack and the MPI backend
+library of choice. If you don't have a preference for an MPI library,
+``libpgapack-openmpi`` is the package that uses the Debians default
+preferences of an MPI library.
+
+Once a parallel version of PGAPack_ is installed, you can install PGApy
+as follows: You set environment variables for the ``PGA_PARALLEL_VARIANT``
+(one of ``mpich``, ``openmpi``, or ``lam``) and set the ``PGA_MODULE`` to
+``module_from_parallel_install``. Finally you envoke the setup, e.g.::
+
+ export PGA_PARALLEL_VARIANT=openmpi
+ export PGA_MODULE=module_from_parallel_install
+ python3 setup.py install --prefix=/usr/local
+
+Note that the same works with ``pip install``, i.e., after installation
+of a parallel version of PGAPack_ you can directly install with ``pip``::
+
+ export PGA_PARALLEL_VARIANT=openmpi
+ export PGA_MODULE=module_from_parallel_install
+ pip install pgapy
+
+or alternatively depending on how pip is installed on your system::
+
+ python3 -m pip install pgapy
+
+If your MPI library is installed in a different place you should study
+the *Extension* configurations in ``setup.py`` to come up with an
+Extension definition that fits your installation. If your installation
+is interesting to more people, feel free to submit a patch that adds
+your Extension-configuration to the standard ``setup.py``.
+
+Running with MPI
+----------------
+
+To run a parallel version with MPI_, a parallel version must be
+installed, see above in section Installation_.
+
+For a serial version, PGAPy makes sure that the otimization is aborted
+if an exception occurs in the ``evaluate`` function. This is currently not
+the case for MPI, because the framework currently does not support
+returning information to the rank-0 MPI leader process. A workaround is
+as follows: Rename your ``evaluate`` method to ``_evaluate`` and catch
+exceptions in a new ``evaluate`` method that wraps ``_evaluate``.
+Call ``MPI_Abort`` if an exception occurs::
+
+    import traceback
+    import sys
+
+    ...
+
+    def evaluate (self, p, pop):
+        try:
+            return self._evaluate (p, pop)
+        except Exception:
+            # Optionally log exception here
+            print (traceback.format_exc ())
+            pga.MPI_Abort (1)
+            sys.exit (1)
+
+Testing
+-------
+
+For testing |--| preferrably before installation you can build locally::
+
+    python3 setup.py build_ext --inplace
+
+After this you have a ``pga.*.so`` file in the local directory. Now you
+can run the tests with::
+
+    python3 -m pytest test
+
+This runs all the tests and can take a while. Note that the tests run
+most of the examples in the ``examples`` directory with different
+command line parameters where available. To perform several optimization
+runs in a single (Python-) process, we must call ``MPI_Init``
+*explicitly* (and not relying on PGAPack_ to call it implicitly). This is
+because ``MPI_Init`` may be called only once per process. Calling of
+``MPI_Init`` and ``MPI_Finalize`` is handled in a fixture in
+``test/conftest.py``
+
+Coverage
+++++++++
+
+For the python examples, the coverage can be computed with::
+
+  python3 -m pytest --cov examples test
+
+or more verbose including untested lines with::
+
+  python3 -m pytest --cov-report term-missing --cov examples test
+
+Performing a coverage analysis for the C code in ``pgamodule.c`` is
+currently possible only on Linux |--| at least, since I'm developing on
+Linux this is the architecture where I've found out how to perform
+coverage analysis including the C code.
+To compile for coverage analysis::
+
+  export CFLAGS=-coverage
+  python3 setup.py build_ext --inplace
+
+This will create a file ending in ``.gcno`` under the ``build`` directory,
+typically something like ``build/temp.linux-x86_64-3.9`` when using
+``python3.9`` on the ``x86_64`` architecture. Running the tests will
+create statistics data files with ending ``.gcda``. These are data files
+for the GNU profiler ``gcov``. From these, ``.html`` files can be
+generated that can be inspected with a browser::
+
+  lcov --capture --directory . --output-file coverage.info
+  genhtml coverage.info --output-directory coverage_out
+
+Note that the ``lcov`` program is part of the linux distribution.
+
+Running under MPI
++++++++++++++++++
+
+The tests can be directly run under MPI. Note that currently the
+``--with-mpi`` option of ``pytest`` is *not* supported. This option
+asumes that the package ``mpi4py`` is used. But ``pgapy`` uses only
+calls from pgapack, which in turn calls MPI.
+
+Running under MPI is done using::
+
+ mpirun $MPI_OPTIONS python3 -m pytest test
+
+The ``MPI_OPTIONS`` can be, e.g.::
+
+    MPI_OPTIONS=--machinefile ~/.mpi-openmpi --np 8
+
+which would use a machine definition file for openmpi in your home
+directory and eight processes.
+
+Running under MPI is especially useful for determining C code coverage.
+Asuming a parallel version of ``openmpi`` is installed, the code can be
+compiled with::
+
+ PGA_PARALLEL_VARIANT=openmpi
+ PGA_MODULE=module_from_parallel_install
+ export CFLAGS=-coverage
+ python3 setup.py build_ext --inplace
+
+Note that the coverage analysis uses files in the build directory which
+need to be present before a parallel version can be started. Otherwise
+each parallel instance would try to create the coverage files resulting
+in race conditions. Once the coverage files are in place, the coverage
+framework ensures proper locking so that no two processes write
+concurrently to the same coverage files.
+
+Creating the coverage files is best achieved by running the tests
+without MPI first and then running the same version with a number of
+processes under MPI. Running under MPI shows that the serialization and
+deserialization code in ``pgamodule.c`` is called.
+
+As of this writing we get::
+
+ Lines:      1423    1475    96.5 %
+ Functions:   131     133    98.5 %
+
+
+References
+----------
+
+.. [1]  Georges Harik. Finding multiple solutions in problems of bounded
+        difficulty. IlliGAL Report 94002, Illinois Genetic Algorithm Lab,
+        May 1994.
+.. [2]  Georges R. Harik. Finding multimodal solutions using restricted
+        tournament selection. In Eshelman [3]_, pages 24–31.
+.. [3]  Larry J. Eshelman, editor. *Proceedings of the 6th International
+        Conference on Genetic Algorithms (ICGA)*. Morgan Kaufmann, July 1995.
+.. [4]  Martin Pelikan. *Hierarchical Bayesian Optimization Algorithm:
+        Toward a New Generation of Evolutionary Algorithms*, volume 170 of
+        Studies in Fuzziness and Soft Computing.  Springer, 2005.
+.. [5]  Rainer Storn and Kenneth Price. Differential evolution |--| a simple
+        and efficient heuristic for global optimization over continuous
+        spaces. *Journal of Global Optimization*, 11(4):341–359, December
+        1997.
+.. [6]  Kenneth V. Price, Rainer M. Storn, and Jouni A. Lampinen.
+        *Differential Evolution: A Practical Approach to Global
+        Optimization.*  Springer, Berlin, Heidelberg, 2005.
+.. [7]  Kalyanmoy Deb, Amrit Pratap, Sameer Agarwal, and T. Meyarivan. A
+        fast and elitist multiobjective genetic algorithm: NSGA-II. *IEEE
+        Transactions on Evolutionary Computation*, 6(2):182–197, April 2002.
+.. [8]  Kalyanmoy Deb and Himanshu Jain. An evolutionary many-objective
+        optimization algorithm using reference-point-based nondominated
+        sorting approach, part I: Solving problems with box constraints.
+        *IEEE Transactions on Evolutionary Computation*, 18(4):577–601,
+        August 2014.
+.. [9]  Himanshu Jain and Kalyanmoy Deb. An evolutionary many-objective
+        optimization algorithm using reference-point-based nondominated
+        sorting approach, part II: Handling constraints and extending to
+        an adaptive approach. *IEEE Transactions on Evolutionary
+        Computation*, 18(4):602–622, August 2014.
+.. [10] Tetsuyuki Takahama and Setsuko Sakai. Constrained optimization
+        by the |epsilon| constrained differential evolution with an
+        archive and gradient-based mutation. In [11]_.
+.. [11] *IEEE Congress on Evolutionary Computation (CEC)*. Barcelona,
+        Spain, July 2010.
+.. [12] Indraneel Das and J. E. Dennis. Normal-boundary intersection: A new
+        method for generating the pareto surface in nonlinear multicriteria
+        optimization problems. SIAM Journal on Optimization, 8(3):631–657,
+        August 1998.
+
+Changes
+-------
+
+Version 2.2.2: Add pyproject.toml
+
+- Add pyproject.toml -- unfortunately it seems that binary modules
+  cannot currently be described in the pyproject.toml, especially not
+  the variant selection via the environment that is currently
+  implemented in setup.py
+
+Version 2.2.1: MPI_Abort
+
+- Add MPI_Abort to the wrapper
+- Include ``mpi_stub.c`` in the release (this is missing if some env
+  variables are set, see above in Installation)
+
+Version 2.2: Module directory
+
+- Put the pga C-module inside a pga module
+- Add several python-only modules to pga
+- pga.__init__ exports everything to this is compatible
+- pga.random includes a python Random class based on the pgapack random
+  number generator
+
+Version 2.1: Regression test
+
+- PGAPack bug-fixes discovered during testing
+- Bug-fixes of python wrapper
+- Lots of tests with coverage of wrapper C-code > 90%
+
+Version 2.0: User defined data types
+
+- Implement user defined data types, note that your data type can be
+  variable-size, e.g., a tree data structure. The framework takes care
+  of serializing the data type and transmitting it to a remote MPI
+  process if using a parallel version.
+- When duplicate checking is enabled with the constructor parameter
+  ``no_duplicates``, the underlying pgapack code now uses a hash table.
+  This means the effort is no longer quadratic in the population size
+  but linear.
+- Example of Genetic Programming (GP) in the ``examples/gp`` directory
+- Rename the gene_difference method to gene_distance
+
+Version 1.8: Epsilon-constrained optimization
+
+- Epsilon-constrained optimization
+- Precision for printing evals in multi-objective optimization, use this
+  feature for making regression-test work on AMD where a floating-point
+  difference in the 16th or so decimal place made a test fail
+- Crossover for permutations
+- Version-numbers: try to match pgapack, we might still diverge in the
+  last digit, though
+
+Version 1.2: Many-objective optimization with NSGA-III
+
+- Implement NSGA-III
+
+Version 1.1.6: Polynomial mutation and simulated binary crossover (SBX)
+
+- Simulated binary crossover (SBX)
+- Polynomial mutation
+
+Version 1.1.1-1.1.5: Small PGAPack updates, fixes for non-debian
+
+- Fix setup.py for non-debian systems
+- Update to latest PGAPack with small changes
+
+Version 1.1: Add multi-objective optimization with NSGA-II
+
+- Wrap latest pgapack version 1.4
+- This add multi-objective optimization using the Nondominated Sorting
+  Genetic Algorithm version 2 (NSGA-II) by Deb et. al. This makes use of
+  the previously-introduced option to return more than one value in the
+  objective function. To use the feature you need to set the
+  num_constraint parameter to a value that leave some of the function
+  values returned by your evaluation function as objective function
+  values (and not as constraints). See example in examples/multi.py.
+
+Version 1.0: Add constraint handling
+
+- Wrap latest pgapack version 1.3
+- This adds auxiliary evaluations. Now your evaluation function can
+  return *multiple* floating-point values as a sequence if you set the
+  num_eval parameter >1 in the constructor. Currently additional
+  evaluation values are used for constraint handling. Constraint values
+  are minimized.  Once they reach zero or a negative value they no
+  longer count: The sum of all positive constraints is the overall
+  constraint violation.  For details see paper by Deb, 2000, see user
+  guide for citation. If you're not using constraints, nothing in your
+  code needs changes.
+- This release may change the path an optimization takes. So for the
+  same seed of the random number generator you will get a different
+  result, at least if during the search there are individuals with the
+  same evaluation (and different genetic material). This is due to a
+  change of the sort function in pgapack (it switched to a stable sort
+  from the C standard library).
+
+Version 0.9: Allow installation of parallel version
+
+- Pass argv (or sys.argv) to PGACreate
+- Add a stanza to setup.py to allow a parallel installation with a given
+  pgapack variant compiled for an MPI library. This currently needs a
+  pre-installed pgapack debian package.
+
+Version 0.8: Bugfix in real mutation
+
+- Fix a core-dump in the latest pgapack
+
+Version 0.7: Major changes in wrapping
+
+- Now Differential Evolution is implemented, see the minfloat example
+  and the user guide of pgapack.
+
+Version 0.6: Major changes in wrapping
+
+- Now the wrapping uses the standard Python recommendations on how to
+  create a custom class.
+- Update documentation
+- Rename ``fitness_cmax`` (from ``fitness_cmax_value``)
+- Better error checking of parameters
+
+Version 0.5: Bug-fix release
+
+- Now the ``setup.py`` works, previous version had an encoding problem
+- Wrap some minor new methods
+- Bug-fix in PGAPack truncation selection
+
+Version 0.4: Bundle PGAPack
+
+- The PGAPack package is now included as a git submodule. By default we
+  build against this library
+- License fixes: The module long shipped a ``COPYING`` file that includes
+  the 2-clause BSD license. But the headers of ``setup.py`` and ``pgamodule.c``
+  still included another license. This has been corrected.
+
+Version 0.3: Feature enhancements, Bug fixes
+
+Port to Python3, Python2 is still supported, license change.
+
+- C-Code of wrapper updated to support both, Python2 and Python3
+- Update documentation
+- Fix some memory leaks that could result when errors occurred during
+  some callback methods
+- License change: We now have the 2-clause BSD license (similar to the
+  MPICH license of PGAPack), this used to be LGPL.
+
+Version 0.2: Feature enhancements, Bug fixes
+
+64 bit support, more PGAPack functions and attributes wrapped,
+Readme-update: Sourceforge logo, Changes chapter.
+
+- Bug-fixes for 64 bit architectures
+- More functions and attributes of PGAPack wrapped
+- Add a build-rule to ``setup.py`` to allow building for standard-install
+  of PGAPack |--| this currently needs editing of ``setup.py`` |--| should use
+  autodetect here but this would require that I set up a machine with
+  standard install of PGAPack for testing.
+- Add Sourceforge logo as required
+- Add Changes chapter for automagic releases
+- Add the ``__module__`` string to class ``PGA`` in module ``pga``. Now
+  calling:: ``help (pga)`` in python works as expected, previously no
+  help-text was given for the included module
+
+Version 0.1: Initial freshmeat announcement
+
+PGAPy is a wrapper for PGAPack, the parallel genetic algorithm library,
+a powerful genetic algorithm library. PGAPy wraps this library for use
+with Python. Pgapack is one of the most complete and accurate genetic
+algorithm implementations out there with a lot of features for
+experimentation.
+
+- Initial Release
+
+.. _`PGAPack Readme`:
+   https://github.com/schlatterbeck/pgapack/blob/master/README.rst
+.. _PGAPack:          http://ftp.mcs.anl.gov/pub/pgapack/
+.. _`PGAPack fork on github`: https://github.com/schlatterbeck/pgapack
+.. _MPI: http://mpi-forum.org/
+.. _`my pgapack debian package builder`:
+    https://github.com/schlatterbeck/debian-pgapack
```

### Comparing `PGAPy-2.2.1/PGAPy.egg-info/SOURCES.txt` & `PGAPy-2.2.2/PGAPy.egg-info/SOURCES.txt`

 * *Files 3% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 COPYING
 MANIFEST.in
 README.html
 README.rst
 Version.h
-Version.py
 pgamodule.c
+pyproject.toml
 setup.py
 PGAPy.egg-info/PKG-INFO
 PGAPy.egg-info/SOURCES.txt
 PGAPy.egg-info/dependency_links.txt
 PGAPy.egg-info/top_level.txt
 examples/cards.py
 examples/cards_mutate.py
@@ -34,14 +34,15 @@
 examples/gp/opt_integral.py
 examples/gp/opt_parity3.py
 examples/gp/opt_xor.py
 examples/sequence/croes.tsp
 examples/sequence/oliver30.tsp
 examples/sequence/plot_tour.py
 examples/sequence/tsp.py
+pga/Version.py
 pga/__init__.py
 pga/random.py
 pga/testsupport.py
 pgapack/docs/user_guide.pdf
 pgapack/fakempi/mpi.h
 pgapack/include/pgapack.h
 pgapack/source/binary.c
```

### Comparing `PGAPy-2.2.1/PKG-INFO` & `PGAPy-2.2.2/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,1046 +1,1056 @@
 Metadata-Version: 2.1
 Name: PGAPy
-Version: 2.2.1
+Version: 2.2.2
 Summary: Python wrapper for pgapack, the parallel genetic algorithm library
-Home-page: http://pgapy.sourceforge.net/
+Home-page: https://github.com/schlatterbeck/pgapy
 Author: Ralf Schlatterbeck
-Author-email: rsc@runtux.com
-License: UNKNOWN
-Description: PGAPy: Python Wrapper for PGAPack Parallel Genetic Algorithm Library
-        ====================================================================
-        
-        .. |--| unicode:: U+2013   .. en dash
-        .. |epsilon| unicode:: U+03B5 .. epsilon
-        
-        :Author: Ralf Schlatterbeck <rsc@runtux.com>
-        
-        News
-        ----
-        
-        News 04-2023:
-        
-        - The last build on PyPi was broken for serial installs, it was missing
-          the ``mpi_stub.c`` needed for the serial version. Parallel installs
-          were still possible so I didn't notice, sorry!
-        - Add MPI_Abort to the wrapper, it is called with::
-        
-            pga.MPI_Abort (errcode)
-        
-          See below in secion `Running with MPI`_ how this can be used to abort
-          the MPI run in case of exception in the ``evaluate`` method.
-        
-        News 12-2022: Add regression test and update to new upstream with
-        several bug-fixes. Includes also some bug fixes in wrapper.
-        
-        News 10-2022: Add user defined datatypes. Example in ``examples/gp`` use
-        user defined data types to implement genetic programming (we represent
-        expressions by a tree data structure). This uses the new serialization
-        API in pgapack to transfer a Python pickle representation to peer MPI
-        processes. Also incorporate the latest changes in pgapack which
-        optimizes duplicate checking. This is of interest for large population
-        sizes in the genetic programming examples. Note that the
-        ``gene_difference`` method has been renamed to ``gene_distance``.
-        
-        News 08-2022: Epsilon-constrained optimization and a crossover variant
-        that preserves permutations (so with integer genes the gene can represent
-        a permutation).
-        
-        News 03-2022: Attempt to make this installable on Windows. This involves
-        some workaround in the code because the visual compiler does not support
-        certain C99 constructs.
-        
-        News 01-2022: This version wraps multiple evaluation with NSGA-III (note
-        the additional 'I').
-        
-        News 12-2021: This version wraps multiple evaluation values from your
-        objective function: Now you can return more than one value to either use
-        it for constraints (that must be fulfilled before the objective is
-        optimized) or for multi-objective optimization with the Nondominated
-        Sorting Genetic Algorithm V.2 (NSGA-II). You can combine both,
-        multi-objective optimization and constraints.
-        
-        News: This version wraps the Differential Evolution method (that's quite
-        an old method but is newly implemented in pgapack).
-        
-        Introduction
-        ------------
-        
-        PGAPy is a wrapper for PGAPack, the parallel genetic algorithm library
-        (see `PGAPack Readme`_), a powerfull genetic algorithm library by
-        D. Levine, Mathematics and Computer Science Division Argonne National
-        Laboratory. The library is written in C. PGAPy wraps this library for
-        use with Python. The original PGAPack library is already quite old but
-        is one of the most complete and accurate (and fast, although this is not
-        my major concern when wrapping it to python) genetic algorithm
-        implementations out there with a lot of bells and whistles for
-        experimentation. It also has shown a remarkably small number of bugs
-        over the years. It supports parallel execution via the message
-        passing interface MPI_ in addition to a normal "serial" version. That's
-        why I wanted to use it in Python, too.
-        
-        To get started you need the PGAPack library, although
-        it now comes bundled with PGApy, to install a *parallel* version you
-        currently need a pre-installed PGAPack_ compiled for the MPI library of
-        choice. See `Installation`_ section for details.
-        
-        There currently is not much documentation for PGAPy.
-        You really, absolutely need to read the documentation that comes
-        with PGAPack.
-        The PGAPack user guide is now shipped together with PGAPy. It is
-        installed together with some examples in share/pgapy, wherever the
-        Python installer decides to place this in the final installation
-        (usually ``/usr/local/share`` on Linux).
-        
-        The original PGAPack library can still be downloaded from the PGAPack_
-        ftp site, it is written in ANSI C but will probably not compile against
-        a recent version of MPI_. It will also not work with recent versions of
-        PGAPy. Note that this version is not actively maintained. I've started a
-        `PGAPack fork on github`_ where I've ported the library to the latest
-        version of the MPI_ standard and have fixed some minor inconsistencies
-        in the documentation. I've also implemented some new features, notably
-        enhancements in selection schemes, a new replacement strategy called
-        *restricted tournament replacement* [1]_, [2]_, [4]_ and, more recently,
-        the differential evolution strategy [5]_, [6]_. In addition this version
-        now supports multi objective optimization with NSGA-II [7]_ and
-        many-objective optimization with NSGA-III [8]_, [9]_. It also supports
-        the Epsilon Constraint method [10]_.
-        
-        Note: When using NSGA_III replacement for multi (or many-) objective
-        optimization you need to either
-        
-        - set reference points on the hyperplane intersecting all axes at
-          offset 1. These reference points can be obtained with the convenience
-          function ``pga.das_dennis``, it creates a regular set of reference points
-          using an algorithm originally publised by I. Das and J. E. Dennis [12]_.
-          These points are then passed as the parameter ``reference_points`` to
-          the ``PGA`` constructor.
-        
-          See ``examples/dtlz2.py`` for a usage example and the user guide for
-          the bibliographic reference. The function gets the dimensionality of
-          the objective space (``num_eval`` minus ``num_constraint``) and the
-          number of partition to use.
-        - Or set reference directions (in the objective space) with the
-          ``reference_directions`` parameter, number of partitions for these
-          directions with the ``refdir_partitions`` parameter (see
-          ``das_dennis`` above, this uses Das/Dennis points internally), and a
-          scale factor with the parameter ``refdir_scale``.
-        
-        You can set both, these parameters are not mutually exclusive.
-        
-        I'm mainly testing pgapy on Linux. But I've recently made it run on
-        Windows, too but I'm not very actively testing on Windows. Let me know
-        if you run it on Windows, sucessfully or not sucessfully.
-        
-        As mentioned above, you can find my `PGAPack fork on github`_, this
-        repository has the three upstream releases as versions in git and
-        contains some updates concerning support of newer MPI_ versions and
-        documentation updates.  I've also included patches in the git repository
-        of the Debian maintainer of the package, Dirk Eddelbuettel.
-        I'm actively maintaining that branch, adding new features and bug-fixes.
-        
-        To get you started, I've included some very simple examples in
-        ``examples``, e.g., ``one-max.py`` implements the "Maxbit" example
-        similar to one in the PGAPack documentation. The examples were inspired
-        by the book "Genetic Algorithms in Python" but are written from scratch
-        and don't include any code from the book. The examples illustrates
-        several points:
-        
-        - Your class implementing the genetic algorithm needs to inherit from
-          pga.PGA (pga is the PGAPy wrapper module).
-        - You need to define an evaluation function called ``evaluate`` that
-          returns a sequence of numbers indicating the fitness of the gene given.
-          It gets the parameters ``p`` and ``pop`` that can be used to fetch allele
-          values from the gene using the ``get_allele`` method, for more details
-          refer to the PGAPack documentation. The number of evaluations returned
-          by your function is defined with the constructor parameter
-          ``num_eval``, the default for this parameter is 1. If your evaluation
-          function does not return multiple evaluations (with the default
-          setting of ``num_eval``) you can either return a one-element sequence
-          or a single return value.
-        - When using multiple evaluations, these can either be used for
-          constraints (the default) or for multi-objective optimization. In the
-          latter case, the number of constraints (which by default is one less
-          than the number of evaluations set with the parameter ``num_eval``)
-          must be set to a number that leaves at least two evaluations for
-          objectives. The number of constraints can be set with the parameter
-          ``num_constraint``. When using multi-objective optimization, you need
-          one of the two replacement-types ``PGA_POPREPL_NSGA_II`` or
-          ``PGA_POPREPL_NSGA_III``, set this with the ``pop_replace_type`` parameter.
-        - You *can* define additional functions overriding built-in functions
-          of the PGAPack library, illustrated by the example of
-          ``print_string``.  Note that we could call the original print_string
-          method of our PGA superclass.  In the same way you can implement,
-          e.g., your own crossover method.
-        - The constructor of the class needs to define the Gene type, in the
-          examples we use int and bool built-in datatypes.
-        - The length of the gene needs to be given in the constructor.
-        - We often want to maximize the numbers returned by our evaluation
-          function, set the parameter ``maximize`` to False if you want to
-          minimize.
-        - For non-binary genes we can define an array of init values, each entry
-          containing a sequence with lower and upper bound. The array has to
-          have the length of the gene. Note that the upper bound is *included*
-          in the range of possible values (unlike the python range operator but
-          compatible with the PGAPack definition).
-        - In the constructor of the class we can add parameters of the genetic
-          algorithm. Not all parameters of PGAPack are wrapped yet, currently
-          you would need to consult the sourcecode of PGAPy to find out which
-          parameters are wrapped. In the example we define several print
-          options.
-        - Finally the genetic algorithm is started with the ``run`` method.
-        
-        Naming conventions in PGAPy
-        ---------------------------
-        
-        When you extend PGAPy |--| remember not all functions of PGAPack are
-        wrapped yet and you may need additional functions |--| you should stick to
-        my naming conventions when making changes.
-        The following naming conventions were used for the wrapper:
-        
-        - Constants of PGAPack like ``PGA_REPORT_STRING`` are used as-is in
-          uppercase. These constants can be directly imported from the wrapper
-          module. Not all constants are wrapped so far, if you need more, add
-          them to the constdef array in pgamodule.c and send_ me a patch.
-        - For methods of the pga.PGA class I've removed the ``PGA`` prefix used
-          throughout PGAPack and converted the method to lowercase with
-          underscores between uppercase words in the original function name, so
-          ``PGARun`` becomes ``run``, ``PGACheckStoppingConditions`` becomes
-          ``check_stopping_conditions``. An exception of the lowercase-rule is
-          whenever a name contains "GA" (for "genetic algorithm"), So
-          ``PGASetMaxGAIterValue`` becomes ``max_GA_iter``.
-        - Where possible I've made a single class method where PGAPack needs a
-          separate function for each datatype, so ``PGAGetBinaryAllele``,
-          ``PGAGetCharacterAllele``, ``PGAGetIntegerAllele``, ``PGAGetRealAllele`` all
-          become ``get_allele``. Same holds true for ``set_allele``.
-        - Whenever a name in PGAPack has a "Value" or "Flag" suffix, I've left
-          this out, so ``PGAGetFitnessCmaxValue`` becomes ``fitness_cmax``
-          and ``PGAGetMutationAndCrossoverFlag`` becomes
-          ``mutation_and_crossover``, the only exception to this rule is for the
-          two functions ``PGAGetMutationRealValue`` and
-          ``PGAGetMutationIntegerValue`` which become ``mutation_value`` not
-          just ``mutation``.
-        - Some fields can take multiple values (they are implemented by ORing
-          integer constants, in python they are specified as a list or tuple of
-          constants). These are converted to plural (if not already plural in
-          PGAPack), e.g., ``PGASetStoppingRuleType`` becomes ``stopping_rule_types``.
-        - Internal method names in the wrapper program have a leading PGA\_ |--| so
-          the class method ``set_allele`` is implemented by the C-function
-          ``PGA_set_allele`` in ``pgamodule.c``.
-        
-        Constructor Parameters
-        ----------------------
-        
-        PGAPack_ has a lot of ``PGASet`` and ``PGAGet`` functions for setting
-        parameters. These are reflected in constructor parameters on the one hand
-        and in (typically read-only, but see below) properties of a ``PGA``
-        object on the other hand. The
-        following table gives an overview of all the original PGAPack_ names and
-        the names of the python wrapper. For the PGAPack_ name I've only listed
-        the ``PGASet`` function, in many cases there is a corresponding
-        ``PGAGet`` function. If a corresponding read-only property exists for a
-        constructor parameter this is indicated in the "Prop" column. In some
-        cases properties are missing because no corresponding ``PGAGet`` function
-        is implemented in PGAPack_, in other cases returning a numeric value that
-        has a symbolic constant in PGApy doesn't make much sense.
-        
-        The properties have the same name as the constructor parameter.
-        There are Properties that don't have a corresponding constructor
-        parameter, namely the ``eval_count`` property (returning the count of
-        function evaluations), the
-        ``GA_iter`` property that returns the current GA generation, and the
-        ``mpi_rank`` property that returns the MPI rank of the current process
-        (this is sorted under PGAGetRank).
-        
-        In the type
-        column I'm listing the Python type. If the type is followed by a number,
-        more than one item of that type is specified (a sequence in Python). Some
-        entries contain "sym", these are integer values with a symbolic constant,
-        the value "msym" indicates that several values denoted by a list of
-        symbolic constants can be given. A special case are the
-        ``PGASetRealInitRange``, ``PGASetRealInitPercent``,
-        ``PGASetIntegerInitRange`` functions. These take two values for *each
-        allele* of the gene. In python this is a sequence of 2-tuples.
-        Note that this means that you can have different ranges of allowed values
-        for each allele.
-        
-        The ``num_eval`` property is special: Due to limitations of the C
-        programming language, for multiple evaluations in C the first evaluation
-        is returned as the function return-value of the ``evaluate`` function
-        and all other parameters are returned in an auxiliary array. PGAPack_
-        specifies the number of auxiliary evaluations to be returned. In Python
-        the evaluation function can always return a sequence of evaluation
-        values and the ``num_eval`` is one more than ``PGAGetNumAuxEval`` would
-        return. The default for ``num_eval`` is 1.
-        
-        The first two (mandatory) constructor parameters are the type of the gene
-        (this takes a Python type, e.g., ``bool`` for a binary genome or ``int``
-        for an integer genome) and the length. Note that the ``string_length`` is
-        implicitly set with the ``length`` parameter. The ``string_length`` is
-        also available as the length of the ``PGA`` object using the Python
-        built-in ``len`` function.
-        
-        Some properties can now also be set *during* the run of the optimizer.
-        These currently are ``crossover_prob``, ``epsilon_exponent``,
-        ``multi_obj_precision``, ``p_tournament_prob``, and
-        ``uniform_crossover_prob``. Just assign to the member variable of
-        the optimizer (child of PGA.pga) object.
-        
-        ==================================== ================================= ====== ====
-        PGAPack name                         Constructor parameter             Type   Prop
-        ==================================== ================================= ====== ====
-        ``PGASetCrossoverBoundedFlag``       ``crossover_bounded``             int    yes
-        ``PGASetCrossoverBounceBackFlag``    ``crossover_bounce_back``         int    yes
-        ``PGASetCrossoverSBXEta``            ``crossover_SBX_eta``             float  yes
-        ``PGASetCrossoverSBXOncePerString``  ``crossover_SBX_once_per_string`` int    yes
-        ``PGASetCrossoverProb``              ``crossover_prob``                float  yes
-        ``PGASetCrossoverType``              ``crossover_type``                sym    no
-        ``PGASetDEAuxFactor``                ``DE_aux_factor``                 double yes
-        ``PGASetDECrossoverProb``            ``DE_crossover_prob``             double yes
-        ``PGASetDECrossoverType``            ``DE_crossover_type``             sym    no
-        ``PGASetDEDither``                   ``DE_dither``                     double yes
-        ``PGASetDEDitherPerIndividual``      ``DE_dither_per_individual``      bool   yes
-        ``PGASetDEJitter``                   ``DE_jitter``                     double yes
-        ``PGASetDENumDiffs``                 ``DE_num_diffs``                  int    yes
-        ``PGASetDEProbabilityEO``            ``DE_probability_EO``             double yes
-        ``PGASetDEScaleFactor``              ``DE_scale_factor``               double yes
-        ``PGASetDEVariant``                  ``DE_variant``                    sym    yes
-        ``PGASetEpsilonExponent``            ``epsilon_exponent``              float  yes
-        ``PGASetEpsilonGeneration``          ``epsilon_generation``            int    yes
-        ``PGASetEpsilonTheta``               ``epsilon_theta``                 int    yes
-        ``PGAGetEvalCount``                  ``eval_count``                    int    yes
-        ``PGASetFitnessCmaxValue``           ``fitness_cmax``                  float  yes
-        ``PGASetFitnessMinType``             ``fitness_min_type``              sym    yes
-        ``PGASetFitnessType``                ``fitness_type``                  sym    yes
-        ``PGAIntegerSetFixedEdges``          ``fixed_edges``                          no
-        ``PGAIntegerSetFixedEdges``          ``fixed_edges_symmetric``         bool   no
-        ``PGAGetGAIterValue``                ``GA_iter``                       int    yes
-        ``PGASetIntegerInitPermute``         ``integer_init_permute``          int2   no
-        ``PGASetIntegerInitRange``           ``init``                                 no
-        ``PGASetMaxFitnessRank``             ``max_fitness_rank``              float  yes
-        ``PGASetMaxGAIterValue``             ``max_GA_iter``                   int    yes
-        ``PGASetMaxNoChangeValue``           ``max_no_change``                 int    no
-        ``PGASetMaxSimilarityValue``         ``max_similarity``                int    yes
-        ``PGASetMixingType``                 ``mixing_type``                   sym    no
-        ``PGASetMultiObjPrecision``          ``multi_obj_precision``           int    yes
-        ``PGASetMutationAndCrossoverFlag``   ``mutation_and_crossover``        int    yes
-        ``PGASetMutationBounceBackFlag``     ``mutation_bounce_back``          int    yes
-        ``PGASetMutationBoundedFlag``        ``mutation_bounded``              int    yes
-        ``PGASetMutationIntegerValue``       ``mutation_value``                int    yes
-        ``PGASetMutationOrCrossoverFlag``    ``mutation_or_crossover``         int    yes
-        ``PGASetMutationPolyEta``            ``mutation_poly_eta``             float  yes
-        ``PGASetMutationPolyValue``          ``mutation_poly_value``           float  yes
-        ``PGASetMutationProb``               ``mutation_prob``                 float  yes
-        ``PGASetMutationRealValue``          ``mutation_value``                float  yes
-        ``PGASetMutationType``               ``mutation_type``                 sym    no
-        ``PGASetNoDuplicatesFlag``           ``no_duplicates``                 int    no
-        ``PGASetNumAuxEval``                 ``num_eval``                      int    yes
-        ``PGASetNumConstraint``              ``num_constraint``                int    yes
-        ``PGASetNumReplaceValue``            ``num_replace``                   int    yes
-        ``PGASetPopSize``                    ``pop_size``                      int    yes
-        ``PGASetPopReplaceType``             ``pop_replace_type``              sym    no
-        ``PGASetPrintFrequencyValue``        ``print_frequency``               int    yes
-        ``PGASetPrintOptions``               ``print_options``                 msym   no
-        ``PGASetPTournamentProb``            ``p_tournament_prob``             float  yes
-        ``PGASetRandomizeSelect``            ``randomize_select``              int    yes
-        ``PGASetRandomSeed``                 ``random_seed``                   int    yes
-        ``PGAGetRank``                       ``mpi_rank``                      int    yes
-        ``PGASetRealInitRange``              ``init``                                 no
-        ``PGASetRealInitPercent``            ``init_percent``                         no
-        ``PGASetReferenceDirections``        ``refdir_partitions``             int    no
-        ``PGASetReferenceDirections``        ``refdir_scale``                  double no
-        ``PGASetReferenceDirections``        ``reference_directions``                 no
-        ``PGASetReferencePoints``            ``reference_points``                     no
-        ``PGASetRestartFlag``                ``restart``                       int    yes
-        ``PGASetRestartFrequencyValue``      ``restart_frequency``             int    yes
-        ``PGASetRTRWindowSize``              ``rtr_window_size``               int    yes
-        ``PGASetSelectType``                 ``select_type``                   sym    no
-        ``PGASetStoppingRuleType``           ``stopping_rule_types``           msym   no
-        ``PGASetStringLength``               ``string_length``                 int    yes
-        ``PGASetSumConstraintsFlag``         ``sum_constraints``               int    yes
-        ``PGASetTournamentSize``             ``tournament_size``               int    yes
-        ``PGASetTournamentWithReplacement``  ``tournament_with_replacement``   int    yes
-        ``PGASetTruncationProportion``       ``truncation_proportion``         float  yes
-        ``PGASetUniformCrossoverProb``       ``uniform_crossover_prob``        float  yes
-        ==================================== ================================= ====== ====
-        
-        Note: The mutation_or_crossover and mutation_and_crossover parameters are
-        deprecated, use mixing_type instead!
-        
-        PGA Object Methods
-        ------------------
-        
-        The following are the methods that can be used during the run of the
-        genetic search. The ``run`` method is used to start the search. This can
-        be used, to, e.g., set an allele during hill-climbing in a custom
-        ``endofgen`` method. Note that some methods only apply to certain gene
-        types, e.g. the ``encode_int_`` methods can only be used on binary
-        alleles (they encode an integer value as a binary or gray code
-        representation into the gene). Other methods take or return different
-        types depending on the type of gene, e.g. ``get_allele`` or
-        ``set_allele``, they call different backend functions depending on the
-        gene type. With the ``set_random_seed`` method, the random number
-        generator can be re-seeded. It is usually best to seed the generator
-        once at (before) the beginning by specifying ``random_seed`` in the
-        constructor. For further details consult the user guide.
-        The method ``get_evaluation`` will return a double for a single
-        evaluation and a tuple of double for multiple evaluations (when num_eval
-        is >1)
-        
-        ============================= ================== ===========================
-        Method                        Parameters         Return
-        ============================= ================== ===========================
-        ``check_stopping_conditions``                    True if stop should occur
-        ``encode_int_as_binary``      *p, pop,*          None
-                                      *frm, to, val*
-        ``encode_int_as_gray_code``   *p, pop,*          None
-                                      *frm, to, val*
-        ``encode_real_as_binary``     *p, pop, frm, to*  None
-                                      *l, u, val*
-        ``encode_real_as_gray_code``  *p, pop, frm, to*  None
-                                      *l, u, val*
-        ``euclidian_distance``        *p1, pop1*         float
-                                      *p2, pop2*
-        ``fitness``                   *pop*              None
-        ``get_allele``                *p, pop, index*    allele value
-        ``get_best_index``            *pop*              index of best string
-        ``get_best_report_index``     *pop, idx*         index of best eval with idx
-        ``get_evaluation``            *p, pop*           evaluation of *p*
-        ``get_evaluation_up_to_date`` *p, pop*           True if up-to-date
-        ``get_fitness``               *p, pop*           fitness of *p* (float)
-        ``get_gene``                  *p, pop*           get gene (user data types)
-        ``get_int_from_binary``       *p, pop, frm, to*  int
-        ``get_int_from_gray_code``    *p, pop, frm, to*  int
-        ``get_iteration``                                deprecated, use ``GA_iter``
-        ``get_real_from_binary``      *p, pop,*          float
-                                      *frm, to, l, u*
-        ``get_real_from_gray_code``   *p, pop,*          float
-                                      *frm, to, l, u*
-        ``random01``                                     float between 0 and 1
-        ``random_flip``               *probability*      0 or 1
-        ``random_gaussian``           *mean, stddev*     float
-        ``random_interval``           *l, r*             int between l, r
-        ``random_uniform``            *l, r*             float between l, r
-        ``run``                                          None
-        ``select_next_index``         *pop*              index selected individual
-        ``set_allele``                *p, pop, i, value* None
-        ``set_evaluation``            *p, pop, value*    None
-        ``set_evaluation_up_to_date`` *p, pop, status*   None
-        ``set_gene``                  *p, pop, gen*      set gene (user data types)
-        ``set_random_seed``           *seed*             None (use constructor!)
-        ============================= ================== ===========================
-        
-        User-Methods
-        ------------
-        
-        PGAPack_ has the concept of user functions. These allow customization of
-        different areas of a genetic algorihm. In Python they are implemented as
-        methods that can be changed in a derived class. One of the methods that
-        *must* be implemented in a derived class is the ``evaluate`` function
-        (although technically it is not a user function in PGAPack). It
-        interprets the gene and returns an evaluation value or a sequence of
-        evaluation values if you set the ``num_eval`` constructor parameter.
-        PGAPack_ computes a fitness from the raw evaluation value. For some
-        methods an up-call into the PGA class is possible, for some methods this
-        is not possible (and in most cases not reasonable). Note that for the
-        ``stop_cond`` method, the standard check for stopping conditions can be
-        called with::
-        
-          self.check_stopping_conditions()
-        
-        The following table lists the overridable methods with their parameters
-        (for the function signature the first parameter *self* is omitted). Note
-        that in PGAPack_ there are additional user functions that are needed for
-        user-defined data types which are currently not exposed in Python. In the
-        function signatures *p* denotes the index of the individual and *pop*
-        denotes the population. If more than one individual is specified (e.g.,
-        for crossover) these can be followed by a number. For crossover *c1* and
-        *c2* denote the destination individuals (children). The *propability* for
-        the mutation method is a floating-point value between 0 and 1. Remember
-        to count the number of mutations that happen, and return that value for
-        the mutation method!
-        
-        =================== ============================== ================= =======
-        Method              Call Signature                 Return Value      Up-Call
-        =================== ============================== ================= =======
-        ``check_duplicate`` *p1, pop1, p2, pop2*           True if dupe      no
-        ``stop_cond``                                      True to stop      no
-        ``crossover``       *p1, p2, p_pop, c1, c2, c_pop* None              no
-        ``endofgen``                                       None              no
-        ``evaluate``        *p, pop*                       sequence of float no
-        ``gene_distance``   *p1, pop1, p2, pop2*           float             no
-        ``hash``            *p, pop*                       int               no
-        ``initstring``      *p, pop*                       None              no
-        ``mutation``        *p, pop, propability*          #mutations        no
-        ``pre_eval``        *pop*                          None              no
-        ``print_string``    *file, p, pop*                 None              yes
-        =================== ============================== ================= =======
-        
-        Constants
-        ---------
-        
-        The following PGAPack_ constants are available:
-        
-        ========================== ===========================================
-        Constant                   Description
-        ========================== ===========================================
-        PGA_CROSSOVER_EDGE         Edge crossover for permutations
-        PGA_CROSSOVER_ONEPT        One-point Crossover
-        PGA_CROSSOVER_SBX          Simulated Binary Crossover
-        PGA_CROSSOVER_TWOPT        Two-point Crossover
-        PGA_CROSSOVER_UNIFORM      Uniform Crossover
-        PGA_FITNESSMIN_CMAX        Map fitness by subtracting worst
-        PGA_FITNESSMIN_RECIPROCAL  Map fitness via reciprocal
-        PGA_FITNESS_NORMAL         Linear normalization of fitness
-        PGA_FITNESS_RANKING        Linear fitness ranking
-        PGA_FITNESS_RAW            Identity fitness function
-        PGA_MUTATION_CONSTANT      Mutation by adding/subtracting constant
-        PGA_MUTATION_GAUSSIAN      Mutation by selecting from Gaussian distribution
-        PGA_MUTATION_PERMUTE       Mutation swaps two random genes
-        PGA_MUTATION_POLY          Polynomial Mutation
-        PGA_MUTATION_RANGE         Replace gene with uniform selection from init range
-        PGA_MUTATION_UNIFORM       Mutation uniform from interval
-        PGA_NEWPOP                 Symbolic constant for new population
-        PGA_OLDPOP                 Symbolic constant for old population
-        PGA_POPREPL_BEST           Population replacement best strings
-        PGA_POPREPL_NSGA_II        Use NSGA-II replacement for multi-objective opt.
-        PGA_POPREPL_NSGA_III       Use NSGA-III replacement for multi-objective opt.
-        PGA_POPREPL_PAIRWISE_BEST  Compare same index in old and new population
-        PGA_POPREPL_RANDOM_NOREP   Population replacement random no replacement
-        PGA_POPREPL_RANDOM_REP     Population replacement random with replacement
-        PGA_POPREPL_RTR            Restricted Tournament Replacement
-        PGA_REPORT_AVERAGE         Report average evaluation
-        PGA_REPORT_HAMMING         Report hamming distance
-        PGA_REPORT_OFFLINE         Report offline
-        PGA_REPORT_ONLINE          Report online
-        PGA_REPORT_STRING          Report the string
-        PGA_REPORT_WORST           Report the worst evaluation
-        PGA_SELECT_LINEAR          Return individuals in population order
-        PGA_SELECT_PROPORTIONAL    Fitness-proportional selection
-        PGA_SELECT_PTOURNAMENT     Binary probabilistic tournament selection
-        PGA_SELECT_SUS             Stochastic universal selection
-        PGA_SELECT_TOURNAMENT      Tournament selection
-        PGA_SELECT_TRUNCATION      Truncation selection
-        PGA_STOP_MAXITER           Stop on max iterations
-        PGA_STOP_NOCHANGE          Stop on max number of generations no change
-        PGA_STOP_TOOSIMILAR        Stop when individuals too similar
-        ========================== ===========================================
-        
-        User Defined Data Types
-        -----------------------
-        
-        The latest version of PGAPy features user defined data types. Just
-        define your data type and pass it as the second parameter to the
-        ``PGA`` constructor. The framework will take care of serializing the
-        data when transmitting via ``MPI`` (if you're running a parallel
-        version).
-        
-        If duplicate checking is enabled via the ``no_duplicates`` constructor
-        parameter, your data type needs to define a ``__hash__`` method (unless
-        the python default hash method fulfills your requirements).
-        
-        User defined data types do not use alleles, so the normal ``get_allele``
-        (and ``set_allele``) methods are not available. Instead the full
-        individual can be retrieved with the ``get_gene`` method and set with
-        the ``set_gene`` method.
-        
-        With user data types you need to define the following methods:
-        
-        - ``check_duplicate (self, p1, pop1, p2, pop2)`` if you enable duplicate
-          checking with the crossover parameter ``no_duplicates``. This should
-          return True when the two individuals are duplicates. Use ``get_gene``
-          to retrieve the genes for the individuals ``p1`` and ``p2`` in
-          populations ``pop1`` and ``pop2``.
-        - ``crossover (self, p1, p2, ppop, c1, c2, cpop)`` for crossover
-          operation, use ``get_gene`` for getting the parent genes for the
-          parents ``p1`` and ``p2`` in generation ``ppop`` and use ``set_gene``
-          for setting the child genes ``c1`` and ``c2`` in generation ``cpop``.
-        - ``initstring (self, p, pop)`` for initializing the given string, use
-          ``set_gene`` in that method for setting your object as a gene.
-        - ``mutation (self, p, pop, pm)`` for the mutation operation. This
-          should return the number of mutations performed. If duplicate checking
-          is enabled, the framework will repeatedly call the mutation operator
-          for mutating a duplicate individual into another individual that is no
-          duplicate. This uses the return value of your mutation method. You
-          will enter an endless loop if your mutation operator does not
-          occasionally return an non-zero number of mutatations performed when
-          duplicate checking is enabled. The ``pm`` parameter gives the mutation
-          probability. Use ``get_gene`` for retrieving the individual to be
-          mutated and use ``set_gene`` to update this individual after mutation.
-        - ``print_string (self, file, p, pop)`` to print a gene object, use
-          ``get_gene`` for retrieving the individual to be printed.
-        
-        For these methods it is generally a good idea to never modify an
-        individual in-place: This individual may be repeatedly used in genetic
-        operations (e.g. mutation and crossover), so when modifying it you will
-        produce erroneous results for later genetic operations. To copy a data
-        structure, python's ``deepcopy`` function in the module ``copy`` is
-        usually used.
-        
-        In addition to the methods above you may want to define a stopping rule
-        with a ``stop_cond`` method or override the way a hash is computed using
-        a ``hash`` method. The default for computing a hash is to call
-        ``hash (gene)`` where gene is an object of the user defined data type.
-        Other methods that may be used is an ``endofgen`` method, a
-        ``gene_distance`` method (e.g., when using Restricted Tournament
-        Replacement, with ``PGA_POPREPL_RTR``), or a ``pre_eval`` method.
-        
-        An example with user defined data types is in ``examples/gp``: This
-        implements Genetic Programming with a tree data structure. Note that the
-        ``Node`` class in ``gp.py`` has a ``__hash__`` method that builds a hash
-        over the serialization of the tree (which is the same for individuals
-        with the same tree structure).
-        
-        
-        Missing Features
-        ----------------
-        
-        As already mentioned, not all functions and constants of PGAPack_ are
-        wrapped yet |--| still for many applications the given set should be
-        enough. If you need additional functions, you may want to wrap these and
-        send_ me a patch.
-        
-        Reporting Bugs
-        --------------
-        
-        Please use the `Sourceforge Bug Tracker`_  or the `Github Bug Tracker`_ and
-        
-        - give a short description of what you think is the correct behaviour
-        - give a description of the observed behaviour
-        - tell me exactly what you did.
-        - if you can publish your source code this makes it a lot easier to
-          debug for me
-        
-        .. _`Sourceforge Bug Tracker`:
-            http://sourceforge.net/tracker/?group_id=152022&atid=782852
-        .. _`Github Bug Tracker`:
-            https://github.com/schlatterbeck/pgapy/issues
-        .. _send: mailto:rsc@runtux.com
-        
-        Resources
-        ---------
-        
-        Project information and download from `Sourceforge main page`_
-        
-        .. _`Sourceforge main page`: http://sourceforge.net/projects/pgapy/
-        
-        or checkout from Github_
-        
-        .. _`Github`: http://github.com/schlatterbeck/pgapy
-        
-        or directly install via pypi.
-        
-        Installation
-        ------------
-        
-        PGApy, as the name suggests, supports parallelizing the evaluation
-        function of the genetic algorithm. This uses the Message Passing
-        Interface (MPI_) standard.
-        
-        To install a *serial* version (without parallel programming using MPI_)
-        you can simply install from pypi using ``pip``. Alternatively when you
-        have unpacked or checked out from sources you can install with::
-        
-         python3 setup.py install --prefix=/usr/local
-        
-        If you want a parallel version using an MPI_ (Message-Passing Interface)
-        library you will have to install a parallel version of PGAPack_ first.
-        The easiest way to do this is to use `my pgapack debian package builder`_
-        from github. Clone this repository, check out the branch ``master``,
-        install the build dependencies, they're listed in the file
-        ``debian/control`` and build the debian packages using::
-        
-          dpkg-buildpackage -rfakeroot
-        
-        This builds pgapack debian packages for *all* supported MPI libraries in
-        debian, currently these are ``mpich``, ``openmpi``, and ``lam``. In addition
-        to the MPI libraries a serial version of the pgapack library is also
-        built. Proceed by installing the package pgapack and the MPI backend
-        library of choice. If you don't have a preference for an MPI library,
-        ``libpgapack-openmpi`` is the package that uses the Debians default
-        preferences of an MPI library.
-        
-        Once a parallel version of PGAPack_ is installed, you can install PGApy
-        as follows: You set environment variables for the ``PGA_PARALLEL_VARIANT``
-        (one of ``mpich``, ``openmpi``, or ``lam``) and set the ``PGA_MODULE`` to
-        ``module_from_parallel_install``. Finally you envoke the setup, e.g.::
-        
-         export PGA_PARALLEL_VARIANT=openmpi
-         export PGA_MODULE=module_from_parallel_install
-         python3 setup.py install --prefix=/usr/local
-        
-        Note that the same works with ``pip install``, i.e., after installation
-        of a parallel version of PGAPack_ you can directly install with ``pip``::
-        
-         export PGA_PARALLEL_VARIANT=openmpi
-         export PGA_MODULE=module_from_parallel_install
-         pip install pgapy
-        
-        or alternatively depending on how pip is installed on your system::
-        
-         python3 -m pip install pgapy
-        
-        If your MPI library is installed in a different place you should study
-        the *Extension* configurations in ``setup.py`` to come up with an
-        Extension definition that fits your installation. If your installation
-        is interesting to more people, feel free to submit a patch that adds
-        your Extension-configuration to the standard ``setup.py``.
-        
-        Running with MPI
-        ----------------
-        
-        To run a parallel version with MPI_, a parallel version must be
-        installed, see above in section Installation_.
-        
-        For a serial version, PGAPy makes sure that the otimization is aborted
-        if an exception occurs in the ``evaluate`` function. This is currently not
-        the case for MPI, because the framework currently does not support
-        returning information to the rank-0 MPI leader process. A workaround is
-        as follows: Rename your ``evaluate`` method to ``_evaluate`` and catch
-        exceptions in a new ``evaluate`` method that wraps ``_evaluate``.
-        Call ``MPI_Abort`` if an exception occurs::
-        
-            import traceback
-            import sys
-        
-            ...
-        
-            def evaluate (self, p, pop):
-                try:
-                    return self._evaluate (p, pop)
-                except Exception:
-                    # Optionally log exception here
-                    print (traceback.format_exc ())
-                    pga.MPI_Abort (1)
-                    sys.exit (1)
-        
-        Testing
-        -------
-        
-        For testing |--| preferrably before installation you can build locally::
-        
-            python3 setup.py build_ext --inplace
-        
-        After this you have a ``pga.*.so`` file in the local directory. Now you
-        can run the tests with::
-        
-            python3 -m pytest test
-        
-        This runs all the tests and can take a while. Note that the tests run
-        most of the examples in the ``examples`` directory with different
-        command line parameters where available. To perform several optimization
-        runs in a single (Python-) process, we must call ``MPI_Init``
-        *explicitly* (and not relying on PGAPack_ to call it implicitly). This is
-        because ``MPI_Init`` may be called only once per process. Calling of
-        ``MPI_Init`` and ``MPI_Finalize`` is handled in a fixture in
-        ``test/conftest.py``
-        
-        Coverage
-        ++++++++
-        
-        For the python examples, the coverage can be computed with::
-        
-          python3 -m pytest --cov examples test
-        
-        or more verbose including untested lines with::
-        
-          python3 -m pytest --cov-report term-missing --cov examples test
-        
-        Performing a coverage analysis for the C code in ``pgamodule.c`` is
-        currently possible only on Linux |--| at least, since I'm developing on
-        Linux this is the architecture where I've found out how to perform
-        coverage analysis including the C code.
-        To compile for coverage analysis::
-        
-          export CFLAGS=-coverage
-          python3 setup.py build_ext --inplace
-        
-        This will create a file ending in ``.gcno`` under the ``build`` directory,
-        typically something like ``build/temp.linux-x86_64-3.9`` when using
-        ``python3.9`` on the ``x86_64`` architecture. Running the tests will
-        create statistics data files with ending ``.gcda``. These are data files
-        for the GNU profiler ``gcov``. From these, ``.html`` files can be
-        generated that can be inspected with a browser::
-        
-          lcov --capture --directory . --output-file coverage.info
-          genhtml coverage.info --output-directory coverage_out
-        
-        Note that the ``lcov`` program is part of the linux distribution.
-        
-        Running under MPI
-        +++++++++++++++++
-        
-        The tests can be directly run under MPI. Note that currently the
-        ``--with-mpi`` option of ``pytest`` is *not* supported. This option
-        asumes that the package ``mpi4py`` is used. But ``pgapy`` uses only
-        calls from pgapack, which in turn calls MPI.
-        
-        Running under MPI is done using::
-        
-         mpirun $MPI_OPTIONS python3 -m pytest test
-        
-        The ``MPI_OPTIONS`` can be, e.g.::
-        
-            MPI_OPTIONS=--machinefile ~/.mpi-openmpi --np 8
-        
-        which would use a machine definition file for openmpi in your home
-        directory and eight processes.
-        
-        Running under MPI is especially useful for determining C code coverage.
-        Asuming a parallel version of ``openmpi`` is installed, the code can be
-        compiled with::
-        
-         PGA_PARALLEL_VARIANT=openmpi
-         PGA_MODULE=module_from_parallel_install
-         export CFLAGS=-coverage
-         python3 setup.py build_ext --inplace
-        
-        Note that the coverage analysis uses files in the build directory which
-        need to be present before a parallel version can be started. Otherwise
-        each parallel instance would try to create the coverage files resulting
-        in race conditions. Once the coverage files are in place, the coverage
-        framework ensures proper locking so that no two processes write
-        concurrently to the same coverage files.
-        
-        Creating the coverage files is best achieved by running the tests
-        without MPI first and then running the same version with a number of
-        processes under MPI. Running under MPI shows that the serialization and
-        deserialization code in ``pgamodule.c`` is called.
-        
-        As of this writing we get::
-        
-         Lines:      1423    1475    96.5 %
-         Functions:   131     133    98.5 %
-        
-        
-        References
-        ----------
-        
-        .. [1]  Georges Harik. Finding multiple solutions in problems of bounded
-                difficulty. IlliGAL Report 94002, Illinois Genetic Algorithm Lab,
-                May 1994.
-        .. [2]  Georges R. Harik. Finding multimodal solutions using restricted
-                tournament selection. In Eshelman [3]_, pages 24–31.
-        .. [3]  Larry J. Eshelman, editor. *Proceedings of the 6th International
-                Conference on Genetic Algorithms (ICGA)*. Morgan Kaufmann, July 1995.
-        .. [4]  Martin Pelikan. *Hierarchical Bayesian Optimization Algorithm:
-                Toward a New Generation of Evolutionary Algorithms*, volume 170 of
-                Studies in Fuzziness and Soft Computing.  Springer, 2005.
-        .. [5]  Rainer Storn and Kenneth Price. Differential evolution |--| a simple
-                and efficient heuristic for global optimization over continuous
-                spaces. *Journal of Global Optimization*, 11(4):341–359, December
-                1997.
-        .. [6]  Kenneth V. Price, Rainer M. Storn, and Jouni A. Lampinen.
-                *Differential Evolution: A Practical Approach to Global
-                Optimization.*  Springer, Berlin, Heidelberg, 2005.
-        .. [7]  Kalyanmoy Deb, Amrit Pratap, Sameer Agarwal, and T. Meyarivan. A
-                fast and elitist multiobjective genetic algorithm: NSGA-II. *IEEE
-                Transactions on Evolutionary Computation*, 6(2):182–197, April 2002.
-        .. [8]  Kalyanmoy Deb and Himanshu Jain. An evolutionary many-objective
-                optimization algorithm using reference-point-based nondominated
-                sorting approach, part I: Solving problems with box constraints.
-                *IEEE Transactions on Evolutionary Computation*, 18(4):577–601,
-                August 2014.
-        .. [9]  Himanshu Jain and Kalyanmoy Deb. An evolutionary many-objective
-                optimization algorithm using reference-point-based nondominated
-                sorting approach, part II: Handling constraints and extending to
-                an adaptive approach. *IEEE Transactions on Evolutionary
-                Computation*, 18(4):602–622, August 2014.
-        .. [10] Tetsuyuki Takahama and Setsuko Sakai. Constrained optimization
-                by the |epsilon| constrained differential evolution with an
-                archive and gradient-based mutation. In [11]_.
-        .. [11] *IEEE Congress on Evolutionary Computation (CEC)*. Barcelona,
-                Spain, July 2010.
-        .. [12] Indraneel Das and J. E. Dennis. Normal-boundary intersection: A new
-                method for generating the pareto surface in nonlinear multicriteria
-                optimization problems. SIAM Journal on Optimization, 8(3):631–657,
-                August 1998.
-        
-        Changes
-        -------
-        
-        Version 2.2.1: MPI_Abort
-        
-        - Add MPI_Abort to the wrapper
-        - Include ``mpi_stub.c`` in the release (this is missing if some env
-          variables are set, see above in Installation)
-        
-        Version 2.2: Module directory
-        
-        - Put the pga C-module inside a pga module
-        - Add several python-only modules to pga
-        - pga.__init__ exports everything to this is compatible
-        - pga.random includes a python Random class based on the pgapack random
-          number generator
-        
-        Version 2.1: Regression test
-        
-        - PGAPack bug-fixes discovered during testing
-        - Bug-fixes of python wrapper
-        - Lots of tests with coverage of wrapper C-code > 90%
-        
-        Version 2.0: User defined data types
-        
-        - Implement user defined data types, note that your data type can be
-          variable-size, e.g., a tree data structure. The framework takes care
-          of serializing the data type and transmitting it to a remote MPI
-          process if using a parallel version.
-        - When duplicate checking is enabled with the constructor parameter
-          ``no_duplicates``, the underlying pgapack code now uses a hash table.
-          This means the effort is no longer quadratic in the population size
-          but linear.
-        - Example of Genetic Programming (GP) in the ``examples/gp`` directory
-        - Rename the gene_difference method to gene_distance
-        
-        Version 1.8: Epsilon-constrained optimization
-        
-        - Epsilon-constrained optimization
-        - Precision for printing evals in multi-objective optimization, use this
-          feature for making regression-test work on AMD where a floating-point
-          difference in the 16th or so decimal place made a test fail
-        - Crossover for permutations
-        - Version-numbers: try to match pgapack, we might still diverge in the
-          last digit, though
-        
-        Version 1.2: Many-objective optimization with NSGA-III
-        
-        - Implement NSGA-III
-        
-        Version 1.1.6: Polynomial mutation and simulated binary crossover (SBX)
-        
-        - Simulated binary crossover (SBX)
-        - Polynomial mutation
-        
-        Version 1.1.1-1.1.5: Small PGAPack updates, fixes for non-debian
-        
-        - Fix setup.py for non-debian systems
-        - Update to latest PGAPack with small changes
-        
-        Version 1.1: Add multi-objective optimization with NSGA-II
-        
-        - Wrap latest pgapack version 1.4
-        - This add multi-objective optimization using the Nondominated Sorting
-          Genetic Algorithm version 2 (NSGA-II) by Deb et. al. This makes use of
-          the previously-introduced option to return more than one value in the
-          objective function. To use the feature you need to set the
-          num_constraint parameter to a value that leave some of the function
-          values returned by your evaluation function as objective function
-          values (and not as constraints). See example in examples/multi.py.
-        
-        Version 1.0: Add constraint handling
-        
-        - Wrap latest pgapack version 1.3
-        - This adds auxiliary evaluations. Now your evaluation function can
-          return *multiple* floating-point values as a sequence if you set the
-          num_eval parameter >1 in the constructor. Currently additional
-          evaluation values are used for constraint handling. Constraint values
-          are minimized.  Once they reach zero or a negative value they no
-          longer count: The sum of all positive constraints is the overall
-          constraint violation.  For details see paper by Deb, 2000, see user
-          guide for citation. If you're not using constraints, nothing in your
-          code needs changes.
-        - This release may change the path an optimization takes. So for the
-          same seed of the random number generator you will get a different
-          result, at least if during the search there are individuals with the
-          same evaluation (and different genetic material). This is due to a
-          change of the sort function in pgapack (it switched to a stable sort
-          from the C standard library).
-        
-        Version 0.9: Allow installation of parallel version
-        
-        - Pass argv (or sys.argv) to PGACreate
-        - Add a stanza to setup.py to allow a parallel installation with a given
-          pgapack variant compiled for an MPI library. This currently needs a
-          pre-installed pgapack debian package.
-        
-        Version 0.8: Bugfix in real mutation
-        
-        - Fix a core-dump in the latest pgapack
-        
-        Version 0.7: Major changes in wrapping
-        
-        - Now Differential Evolution is implemented, see the minfloat example
-          and the user guide of pgapack.
-        
-        Version 0.6: Major changes in wrapping
-        
-        - Now the wrapping uses the standard Python recommendations on how to
-          create a custom class.
-        - Update documentation
-        - Rename ``fitness_cmax`` (from ``fitness_cmax_value``)
-        - Better error checking of parameters
-        
-        Version 0.5: Bug-fix release
-        
-        - Now the ``setup.py`` works, previous version had an encoding problem
-        - Wrap some minor new methods
-        - Bug-fix in PGAPack truncation selection
-        
-        Version 0.4: Bundle PGAPack
-        
-        - The PGAPack package is now included as a git submodule. By default we
-          build against this library
-        - License fixes: The module long shipped a ``COPYING`` file that includes
-          the 2-clause BSD license. But the headers of ``setup.py`` and ``pgamodule.c``
-          still included another license. This has been corrected.
-        
-        Version 0.3: Feature enhancements, Bug fixes
-        
-        Port to Python3, Python2 is still supported, license change.
-        
-        - C-Code of wrapper updated to support both, Python2 and Python3
-        - Update documentation
-        - Fix some memory leaks that could result when errors occurred during
-          some callback methods
-        - License change: We now have the 2-clause BSD license (similar to the
-          MPICH license of PGAPack), this used to be LGPL.
-        
-        Version 0.2: Feature enhancements, Bug fixes
-        
-        64 bit support, more PGAPack functions and attributes wrapped,
-        Readme-update: Sourceforge logo, Changes chapter.
-        
-        - Bug-fixes for 64 bit architectures
-        - More functions and attributes of PGAPack wrapped
-        - Add a build-rule to ``setup.py`` to allow building for standard-install
-          of PGAPack |--| this currently needs editing of ``setup.py`` |--| should use
-          autodetect here but this would require that I set up a machine with
-          standard install of PGAPack for testing.
-        - Add Sourceforge logo as required
-        - Add Changes chapter for automagic releases
-        - Add the ``__module__`` string to class ``PGA`` in module ``pga``. Now
-          calling:: ``help (pga)`` in python works as expected, previously no
-          help-text was given for the included module
-        
-        Version 0.1: Initial freshmeat announcement
-        
-        PGAPy is a wrapper for PGAPack, the parallel genetic algorithm library,
-        a powerful genetic algorithm library. PGAPy wraps this library for use
-        with Python. Pgapack is one of the most complete and accurate genetic
-        algorithm implementations out there with a lot of features for
-        experimentation.
-        
-        - Initial Release
-        
-        .. _`PGAPack Readme`:
-           https://github.com/schlatterbeck/pgapack/blob/master/README.rst
-        .. _PGAPack:          http://ftp.mcs.anl.gov/pub/pgapack/
-        .. _`PGAPack fork on github`: https://github.com/schlatterbeck/pgapack
-        .. _MPI: http://mpi-forum.org/
-        .. _`my pgapack debian package builder`:
-            https://github.com/schlatterbeck/debian-pgapack
-        
-Platform: UNKNOWN
+Author-email: Ralf Schlatterbeck <rsc@runtux.com>
+License: BSD License
+Project-URL: Homepage, https://github.com/schlatterbeck/pgapy
+Project-URL: Bug Tracker, https://github.com/schlatterbeck/pgapy/issues
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Education
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: C
 Classifier: Programming Language :: Python
 Classifier: Topic :: Education
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: Topic :: Software Development :: Libraries
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Requires-Python: >=3.7
 Description-Content-Type: text/x-rst
+License-File: COPYING
+
+PGAPy: Python Wrapper for PGAPack Parallel Genetic Algorithm Library
+====================================================================
+
+.. |--| unicode:: U+2013   .. en dash
+.. |epsilon| unicode:: U+03B5 .. epsilon
+
+:Author: Ralf Schlatterbeck <rsc@runtux.com>
+
+News
+----
+
+News 04-2023:
+
+- The last build on PyPi was broken for serial installs, it was missing
+  the ``mpi_stub.c`` needed for the serial version. Parallel installs
+  were still possible so I didn't notice, sorry!
+- Add MPI_Abort to the wrapper, it is called with::
+
+    pga.MPI_Abort (errcode)
+
+  See below in secion `Running with MPI`_ how this can be used to abort
+  the MPI run in case of exception in the ``evaluate`` method.
+
+News 12-2022: Add regression test and update to new upstream with
+several bug-fixes. Includes also some bug fixes in wrapper.
+
+News 10-2022: Add user defined datatypes. Example in ``examples/gp`` use
+user defined data types to implement genetic programming (we represent
+expressions by a tree data structure). This uses the new serialization
+API in pgapack to transfer a Python pickle representation to peer MPI
+processes. Also incorporate the latest changes in pgapack which
+optimizes duplicate checking. This is of interest for large population
+sizes in the genetic programming examples. Note that the
+``gene_difference`` method has been renamed to ``gene_distance``.
+
+News 08-2022: Epsilon-constrained optimization and a crossover variant
+that preserves permutations (so with integer genes the gene can represent
+a permutation).
+
+News 03-2022: Attempt to make this installable on Windows. This involves
+some workaround in the code because the visual compiler does not support
+certain C99 constructs.
+
+News 01-2022: This version wraps multiple evaluation with NSGA-III (note
+the additional 'I').
+
+News 12-2021: This version wraps multiple evaluation values from your
+objective function: Now you can return more than one value to either use
+it for constraints (that must be fulfilled before the objective is
+optimized) or for multi-objective optimization with the Nondominated
+Sorting Genetic Algorithm V.2 (NSGA-II). You can combine both,
+multi-objective optimization and constraints.
+
+News: This version wraps the Differential Evolution method (that's quite
+an old method but is newly implemented in pgapack).
+
+Introduction
+------------
+
+PGAPy is a wrapper for PGAPack, the parallel genetic algorithm library
+(see `PGAPack Readme`_), a powerfull genetic algorithm library by
+D. Levine, Mathematics and Computer Science Division Argonne National
+Laboratory. The library is written in C. PGAPy wraps this library for
+use with Python. The original PGAPack library is already quite old but
+is one of the most complete and accurate (and fast, although this is not
+my major concern when wrapping it to python) genetic algorithm
+implementations out there with a lot of bells and whistles for
+experimentation. It also has shown a remarkably small number of bugs
+over the years. It supports parallel execution via the message
+passing interface MPI_ in addition to a normal "serial" version. That's
+why I wanted to use it in Python, too.
+
+To get started you need the PGAPack library, although
+it now comes bundled with PGApy, to install a *parallel* version you
+currently need a pre-installed PGAPack_ compiled for the MPI library of
+choice. See `Installation`_ section for details.
+
+There currently is not much documentation for PGAPy.
+You really, absolutely need to read the documentation that comes
+with PGAPack.
+The PGAPack user guide is now shipped together with PGAPy. It is
+installed together with some examples in share/pgapy, wherever the
+Python installer decides to place this in the final installation
+(usually ``/usr/local/share`` on Linux).
+
+The original PGAPack library can still be downloaded from the PGAPack_
+ftp site, it is written in ANSI C but will probably not compile against
+a recent version of MPI_. It will also not work with recent versions of
+PGAPy. Note that this version is not actively maintained. I've started a
+`PGAPack fork on github`_ where I've ported the library to the latest
+version of the MPI_ standard and have fixed some minor inconsistencies
+in the documentation. I've also implemented some new features, notably
+enhancements in selection schemes, a new replacement strategy called
+*restricted tournament replacement* [1]_, [2]_, [4]_ and, more recently,
+the differential evolution strategy [5]_, [6]_. In addition this version
+now supports multi objective optimization with NSGA-II [7]_ and
+many-objective optimization with NSGA-III [8]_, [9]_. It also supports
+the Epsilon Constraint method [10]_.
+
+Note: When using NSGA_III replacement for multi (or many-) objective
+optimization you need to either
+
+- set reference points on the hyperplane intersecting all axes at
+  offset 1. These reference points can be obtained with the convenience
+  function ``pga.das_dennis``, it creates a regular set of reference points
+  using an algorithm originally publised by I. Das and J. E. Dennis [12]_.
+  These points are then passed as the parameter ``reference_points`` to
+  the ``PGA`` constructor.
+
+  See ``examples/dtlz2.py`` for a usage example and the user guide for
+  the bibliographic reference. The function gets the dimensionality of
+  the objective space (``num_eval`` minus ``num_constraint``) and the
+  number of partition to use.
+- Or set reference directions (in the objective space) with the
+  ``reference_directions`` parameter, number of partitions for these
+  directions with the ``refdir_partitions`` parameter (see
+  ``das_dennis`` above, this uses Das/Dennis points internally), and a
+  scale factor with the parameter ``refdir_scale``.
+
+You can set both, these parameters are not mutually exclusive.
+
+I'm mainly testing pgapy on Linux. But I've recently made it run on
+Windows, too but I'm not very actively testing on Windows. Let me know
+if you run it on Windows, sucessfully or not sucessfully.
+
+As mentioned above, you can find my `PGAPack fork on github`_, this
+repository has the three upstream releases as versions in git and
+contains some updates concerning support of newer MPI_ versions and
+documentation updates.  I've also included patches in the git repository
+of the Debian maintainer of the package, Dirk Eddelbuettel.
+I'm actively maintaining that branch, adding new features and bug-fixes.
+
+To get you started, I've included some very simple examples in
+``examples``, e.g., ``one-max.py`` implements the "Maxbit" example
+similar to one in the PGAPack documentation. The examples were inspired
+by the book "Genetic Algorithms in Python" but are written from scratch
+and don't include any code from the book. The examples illustrates
+several points:
+
+- Your class implementing the genetic algorithm needs to inherit from
+  pga.PGA (pga is the PGAPy wrapper module).
+- You need to define an evaluation function called ``evaluate`` that
+  returns a sequence of numbers indicating the fitness of the gene given.
+  It gets the parameters ``p`` and ``pop`` that can be used to fetch allele
+  values from the gene using the ``get_allele`` method, for more details
+  refer to the PGAPack documentation. The number of evaluations returned
+  by your function is defined with the constructor parameter
+  ``num_eval``, the default for this parameter is 1. If your evaluation
+  function does not return multiple evaluations (with the default
+  setting of ``num_eval``) you can either return a one-element sequence
+  or a single return value.
+- When using multiple evaluations, these can either be used for
+  constraints (the default) or for multi-objective optimization. In the
+  latter case, the number of constraints (which by default is one less
+  than the number of evaluations set with the parameter ``num_eval``)
+  must be set to a number that leaves at least two evaluations for
+  objectives. The number of constraints can be set with the parameter
+  ``num_constraint``. When using multi-objective optimization, you need
+  one of the two replacement-types ``PGA_POPREPL_NSGA_II`` or
+  ``PGA_POPREPL_NSGA_III``, set this with the ``pop_replace_type`` parameter.
+- You *can* define additional functions overriding built-in functions
+  of the PGAPack library, illustrated by the example of
+  ``print_string``.  Note that we could call the original print_string
+  method of our PGA superclass.  In the same way you can implement,
+  e.g., your own crossover method.
+- The constructor of the class needs to define the Gene type, in the
+  examples we use int and bool built-in datatypes.
+- The length of the gene needs to be given in the constructor.
+- We often want to maximize the numbers returned by our evaluation
+  function, set the parameter ``maximize`` to False if you want to
+  minimize.
+- For non-binary genes we can define an array of init values, each entry
+  containing a sequence with lower and upper bound. The array has to
+  have the length of the gene. Note that the upper bound is *included*
+  in the range of possible values (unlike the python range operator but
+  compatible with the PGAPack definition).
+- In the constructor of the class we can add parameters of the genetic
+  algorithm. Not all parameters of PGAPack are wrapped yet, currently
+  you would need to consult the sourcecode of PGAPy to find out which
+  parameters are wrapped. In the example we define several print
+  options.
+- Finally the genetic algorithm is started with the ``run`` method.
+
+Naming conventions in PGAPy
+---------------------------
+
+When you extend PGAPy |--| remember not all functions of PGAPack are
+wrapped yet and you may need additional functions |--| you should stick to
+my naming conventions when making changes.
+The following naming conventions were used for the wrapper:
+
+- Constants of PGAPack like ``PGA_REPORT_STRING`` are used as-is in
+  uppercase. These constants can be directly imported from the wrapper
+  module. Not all constants are wrapped so far, if you need more, add
+  them to the constdef array in pgamodule.c and send_ me a patch.
+- For methods of the pga.PGA class I've removed the ``PGA`` prefix used
+  throughout PGAPack and converted the method to lowercase with
+  underscores between uppercase words in the original function name, so
+  ``PGARun`` becomes ``run``, ``PGACheckStoppingConditions`` becomes
+  ``check_stopping_conditions``. An exception of the lowercase-rule is
+  whenever a name contains "GA" (for "genetic algorithm"), So
+  ``PGASetMaxGAIterValue`` becomes ``max_GA_iter``.
+- Where possible I've made a single class method where PGAPack needs a
+  separate function for each datatype, so ``PGAGetBinaryAllele``,
+  ``PGAGetCharacterAllele``, ``PGAGetIntegerAllele``, ``PGAGetRealAllele`` all
+  become ``get_allele``. Same holds true for ``set_allele``.
+- Whenever a name in PGAPack has a "Value" or "Flag" suffix, I've left
+  this out, so ``PGAGetFitnessCmaxValue`` becomes ``fitness_cmax``
+  and ``PGAGetMutationAndCrossoverFlag`` becomes
+  ``mutation_and_crossover``, the only exception to this rule is for the
+  two functions ``PGAGetMutationRealValue`` and
+  ``PGAGetMutationIntegerValue`` which become ``mutation_value`` not
+  just ``mutation``.
+- Some fields can take multiple values (they are implemented by ORing
+  integer constants, in python they are specified as a list or tuple of
+  constants). These are converted to plural (if not already plural in
+  PGAPack), e.g., ``PGASetStoppingRuleType`` becomes ``stopping_rule_types``.
+- Internal method names in the wrapper program have a leading PGA\_ |--| so
+  the class method ``set_allele`` is implemented by the C-function
+  ``PGA_set_allele`` in ``pgamodule.c``.
+
+Constructor Parameters
+----------------------
+
+PGAPack_ has a lot of ``PGASet`` and ``PGAGet`` functions for setting
+parameters. These are reflected in constructor parameters on the one hand
+and in (typically read-only, but see below) properties of a ``PGA``
+object on the other hand. The
+following table gives an overview of all the original PGAPack_ names and
+the names of the python wrapper. For the PGAPack_ name I've only listed
+the ``PGASet`` function, in many cases there is a corresponding
+``PGAGet`` function. If a corresponding read-only property exists for a
+constructor parameter this is indicated in the "Prop" column. In some
+cases properties are missing because no corresponding ``PGAGet`` function
+is implemented in PGAPack_, in other cases returning a numeric value that
+has a symbolic constant in PGApy doesn't make much sense.
+
+The properties have the same name as the constructor parameter.
+There are Properties that don't have a corresponding constructor
+parameter, namely the ``eval_count`` property (returning the count of
+function evaluations), the
+``GA_iter`` property that returns the current GA generation, and the
+``mpi_rank`` property that returns the MPI rank of the current process
+(this is sorted under PGAGetRank).
+
+In the type
+column I'm listing the Python type. If the type is followed by a number,
+more than one item of that type is specified (a sequence in Python). Some
+entries contain "sym", these are integer values with a symbolic constant,
+the value "msym" indicates that several values denoted by a list of
+symbolic constants can be given. A special case are the
+``PGASetRealInitRange``, ``PGASetRealInitPercent``,
+``PGASetIntegerInitRange`` functions. These take two values for *each
+allele* of the gene. In python this is a sequence of 2-tuples.
+Note that this means that you can have different ranges of allowed values
+for each allele.
+
+The ``num_eval`` property is special: Due to limitations of the C
+programming language, for multiple evaluations in C the first evaluation
+is returned as the function return-value of the ``evaluate`` function
+and all other parameters are returned in an auxiliary array. PGAPack_
+specifies the number of auxiliary evaluations to be returned. In Python
+the evaluation function can always return a sequence of evaluation
+values and the ``num_eval`` is one more than ``PGAGetNumAuxEval`` would
+return. The default for ``num_eval`` is 1.
+
+The first two (mandatory) constructor parameters are the type of the gene
+(this takes a Python type, e.g., ``bool`` for a binary genome or ``int``
+for an integer genome) and the length. Note that the ``string_length`` is
+implicitly set with the ``length`` parameter. The ``string_length`` is
+also available as the length of the ``PGA`` object using the Python
+built-in ``len`` function.
+
+Some properties can now also be set *during* the run of the optimizer.
+These currently are ``crossover_prob``, ``epsilon_exponent``,
+``multi_obj_precision``, ``p_tournament_prob``, and
+``uniform_crossover_prob``. Just assign to the member variable of
+the optimizer (child of PGA.pga) object.
+
+==================================== ================================= ====== ====
+PGAPack name                         Constructor parameter             Type   Prop
+==================================== ================================= ====== ====
+``PGASetCrossoverBoundedFlag``       ``crossover_bounded``             int    yes
+``PGASetCrossoverBounceBackFlag``    ``crossover_bounce_back``         int    yes
+``PGASetCrossoverSBXEta``            ``crossover_SBX_eta``             float  yes
+``PGASetCrossoverSBXOncePerString``  ``crossover_SBX_once_per_string`` int    yes
+``PGASetCrossoverProb``              ``crossover_prob``                float  yes
+``PGASetCrossoverType``              ``crossover_type``                sym    no
+``PGASetDEAuxFactor``                ``DE_aux_factor``                 double yes
+``PGASetDECrossoverProb``            ``DE_crossover_prob``             double yes
+``PGASetDECrossoverType``            ``DE_crossover_type``             sym    no
+``PGASetDEDither``                   ``DE_dither``                     double yes
+``PGASetDEDitherPerIndividual``      ``DE_dither_per_individual``      bool   yes
+``PGASetDEJitter``                   ``DE_jitter``                     double yes
+``PGASetDENumDiffs``                 ``DE_num_diffs``                  int    yes
+``PGASetDEProbabilityEO``            ``DE_probability_EO``             double yes
+``PGASetDEScaleFactor``              ``DE_scale_factor``               double yes
+``PGASetDEVariant``                  ``DE_variant``                    sym    yes
+``PGASetEpsilonExponent``            ``epsilon_exponent``              float  yes
+``PGASetEpsilonGeneration``          ``epsilon_generation``            int    yes
+``PGASetEpsilonTheta``               ``epsilon_theta``                 int    yes
+``PGAGetEvalCount``                  ``eval_count``                    int    yes
+``PGASetFitnessCmaxValue``           ``fitness_cmax``                  float  yes
+``PGASetFitnessMinType``             ``fitness_min_type``              sym    yes
+``PGASetFitnessType``                ``fitness_type``                  sym    yes
+``PGAIntegerSetFixedEdges``          ``fixed_edges``                          no
+``PGAIntegerSetFixedEdges``          ``fixed_edges_symmetric``         bool   no
+``PGAGetGAIterValue``                ``GA_iter``                       int    yes
+``PGASetIntegerInitPermute``         ``integer_init_permute``          int2   no
+``PGASetIntegerInitRange``           ``init``                                 no
+``PGASetMaxFitnessRank``             ``max_fitness_rank``              float  yes
+``PGASetMaxGAIterValue``             ``max_GA_iter``                   int    yes
+``PGASetMaxNoChangeValue``           ``max_no_change``                 int    no
+``PGASetMaxSimilarityValue``         ``max_similarity``                int    yes
+``PGASetMixingType``                 ``mixing_type``                   sym    no
+``PGASetMultiObjPrecision``          ``multi_obj_precision``           int    yes
+``PGASetMutationAndCrossoverFlag``   ``mutation_and_crossover``        int    yes
+``PGASetMutationBounceBackFlag``     ``mutation_bounce_back``          int    yes
+``PGASetMutationBoundedFlag``        ``mutation_bounded``              int    yes
+``PGASetMutationIntegerValue``       ``mutation_value``                int    yes
+``PGASetMutationOrCrossoverFlag``    ``mutation_or_crossover``         int    yes
+``PGASetMutationPolyEta``            ``mutation_poly_eta``             float  yes
+``PGASetMutationPolyValue``          ``mutation_poly_value``           float  yes
+``PGASetMutationProb``               ``mutation_prob``                 float  yes
+``PGASetMutationRealValue``          ``mutation_value``                float  yes
+``PGASetMutationType``               ``mutation_type``                 sym    no
+``PGASetNoDuplicatesFlag``           ``no_duplicates``                 int    no
+``PGASetNumAuxEval``                 ``num_eval``                      int    yes
+``PGASetNumConstraint``              ``num_constraint``                int    yes
+``PGASetNumReplaceValue``            ``num_replace``                   int    yes
+``PGASetPopSize``                    ``pop_size``                      int    yes
+``PGASetPopReplaceType``             ``pop_replace_type``              sym    no
+``PGASetPrintFrequencyValue``        ``print_frequency``               int    yes
+``PGASetPrintOptions``               ``print_options``                 msym   no
+``PGASetPTournamentProb``            ``p_tournament_prob``             float  yes
+``PGASetRandomizeSelect``            ``randomize_select``              int    yes
+``PGASetRandomSeed``                 ``random_seed``                   int    yes
+``PGAGetRank``                       ``mpi_rank``                      int    yes
+``PGASetRealInitRange``              ``init``                                 no
+``PGASetRealInitPercent``            ``init_percent``                         no
+``PGASetReferenceDirections``        ``refdir_partitions``             int    no
+``PGASetReferenceDirections``        ``refdir_scale``                  double no
+``PGASetReferenceDirections``        ``reference_directions``                 no
+``PGASetReferencePoints``            ``reference_points``                     no
+``PGASetRestartFlag``                ``restart``                       int    yes
+``PGASetRestartFrequencyValue``      ``restart_frequency``             int    yes
+``PGASetRTRWindowSize``              ``rtr_window_size``               int    yes
+``PGASetSelectType``                 ``select_type``                   sym    no
+``PGASetStoppingRuleType``           ``stopping_rule_types``           msym   no
+``PGASetStringLength``               ``string_length``                 int    yes
+``PGASetSumConstraintsFlag``         ``sum_constraints``               int    yes
+``PGASetTournamentSize``             ``tournament_size``               int    yes
+``PGASetTournamentWithReplacement``  ``tournament_with_replacement``   int    yes
+``PGASetTruncationProportion``       ``truncation_proportion``         float  yes
+``PGASetUniformCrossoverProb``       ``uniform_crossover_prob``        float  yes
+==================================== ================================= ====== ====
+
+Note: The mutation_or_crossover and mutation_and_crossover parameters are
+deprecated, use mixing_type instead!
+
+PGA Object Methods
+------------------
+
+The following are the methods that can be used during the run of the
+genetic search. The ``run`` method is used to start the search. This can
+be used, to, e.g., set an allele during hill-climbing in a custom
+``endofgen`` method. Note that some methods only apply to certain gene
+types, e.g. the ``encode_int_`` methods can only be used on binary
+alleles (they encode an integer value as a binary or gray code
+representation into the gene). Other methods take or return different
+types depending on the type of gene, e.g. ``get_allele`` or
+``set_allele``, they call different backend functions depending on the
+gene type. With the ``set_random_seed`` method, the random number
+generator can be re-seeded. It is usually best to seed the generator
+once at (before) the beginning by specifying ``random_seed`` in the
+constructor. For further details consult the user guide.
+The method ``get_evaluation`` will return a double for a single
+evaluation and a tuple of double for multiple evaluations (when num_eval
+is >1)
+
+============================= ================== ===========================
+Method                        Parameters         Return
+============================= ================== ===========================
+``check_stopping_conditions``                    True if stop should occur
+``encode_int_as_binary``      *p, pop,*          None
+                              *frm, to, val*
+``encode_int_as_gray_code``   *p, pop,*          None
+                              *frm, to, val*
+``encode_real_as_binary``     *p, pop, frm, to*  None
+                              *l, u, val*
+``encode_real_as_gray_code``  *p, pop, frm, to*  None
+                              *l, u, val*
+``euclidian_distance``        *p1, pop1*         float
+                              *p2, pop2*
+``fitness``                   *pop*              None
+``get_allele``                *p, pop, index*    allele value
+``get_best_index``            *pop*              index of best string
+``get_best_report_index``     *pop, idx*         index of best eval with idx
+``get_evaluation``            *p, pop*           evaluation of *p*
+``get_evaluation_up_to_date`` *p, pop*           True if up-to-date
+``get_fitness``               *p, pop*           fitness of *p* (float)
+``get_gene``                  *p, pop*           get gene (user data types)
+``get_int_from_binary``       *p, pop, frm, to*  int
+``get_int_from_gray_code``    *p, pop, frm, to*  int
+``get_iteration``                                deprecated, use ``GA_iter``
+``get_real_from_binary``      *p, pop,*          float
+                              *frm, to, l, u*
+``get_real_from_gray_code``   *p, pop,*          float
+                              *frm, to, l, u*
+``random01``                                     float between 0 and 1
+``random_flip``               *probability*      0 or 1
+``random_gaussian``           *mean, stddev*     float
+``random_interval``           *l, r*             int between l, r
+``random_uniform``            *l, r*             float between l, r
+``run``                                          None
+``select_next_index``         *pop*              index selected individual
+``set_allele``                *p, pop, i, value* None
+``set_evaluation``            *p, pop, value*    None
+``set_evaluation_up_to_date`` *p, pop, status*   None
+``set_gene``                  *p, pop, gen*      set gene (user data types)
+``set_random_seed``           *seed*             None (use constructor!)
+============================= ================== ===========================
+
+User-Methods
+------------
+
+PGAPack_ has the concept of user functions. These allow customization of
+different areas of a genetic algorihm. In Python they are implemented as
+methods that can be changed in a derived class. One of the methods that
+*must* be implemented in a derived class is the ``evaluate`` function
+(although technically it is not a user function in PGAPack). It
+interprets the gene and returns an evaluation value or a sequence of
+evaluation values if you set the ``num_eval`` constructor parameter.
+PGAPack_ computes a fitness from the raw evaluation value. For some
+methods an up-call into the PGA class is possible, for some methods this
+is not possible (and in most cases not reasonable). Note that for the
+``stop_cond`` method, the standard check for stopping conditions can be
+called with::
+
+  self.check_stopping_conditions()
+
+The following table lists the overridable methods with their parameters
+(for the function signature the first parameter *self* is omitted). Note
+that in PGAPack_ there are additional user functions that are needed for
+user-defined data types which are currently not exposed in Python. In the
+function signatures *p* denotes the index of the individual and *pop*
+denotes the population. If more than one individual is specified (e.g.,
+for crossover) these can be followed by a number. For crossover *c1* and
+*c2* denote the destination individuals (children). The *propability* for
+the mutation method is a floating-point value between 0 and 1. Remember
+to count the number of mutations that happen, and return that value for
+the mutation method!
+
+=================== ============================== ================= =======
+Method              Call Signature                 Return Value      Up-Call
+=================== ============================== ================= =======
+``check_duplicate`` *p1, pop1, p2, pop2*           True if dupe      no
+``stop_cond``                                      True to stop      no
+``crossover``       *p1, p2, p_pop, c1, c2, c_pop* None              no
+``endofgen``                                       None              no
+``evaluate``        *p, pop*                       sequence of float no
+``gene_distance``   *p1, pop1, p2, pop2*           float             no
+``hash``            *p, pop*                       int               no
+``initstring``      *p, pop*                       None              no
+``mutation``        *p, pop, propability*          #mutations        no
+``pre_eval``        *pop*                          None              no
+``print_string``    *file, p, pop*                 None              yes
+=================== ============================== ================= =======
+
+Constants
+---------
+
+The following PGAPack_ constants are available:
+
+========================== ===========================================
+Constant                   Description
+========================== ===========================================
+PGA_CROSSOVER_EDGE         Edge crossover for permutations
+PGA_CROSSOVER_ONEPT        One-point Crossover
+PGA_CROSSOVER_SBX          Simulated Binary Crossover
+PGA_CROSSOVER_TWOPT        Two-point Crossover
+PGA_CROSSOVER_UNIFORM      Uniform Crossover
+PGA_FITNESSMIN_CMAX        Map fitness by subtracting worst
+PGA_FITNESSMIN_RECIPROCAL  Map fitness via reciprocal
+PGA_FITNESS_NORMAL         Linear normalization of fitness
+PGA_FITNESS_RANKING        Linear fitness ranking
+PGA_FITNESS_RAW            Identity fitness function
+PGA_MUTATION_CONSTANT      Mutation by adding/subtracting constant
+PGA_MUTATION_GAUSSIAN      Mutation by selecting from Gaussian distribution
+PGA_MUTATION_PERMUTE       Mutation swaps two random genes
+PGA_MUTATION_POLY          Polynomial Mutation
+PGA_MUTATION_RANGE         Replace gene with uniform selection from init range
+PGA_MUTATION_UNIFORM       Mutation uniform from interval
+PGA_NEWPOP                 Symbolic constant for new population
+PGA_OLDPOP                 Symbolic constant for old population
+PGA_POPREPL_BEST           Population replacement best strings
+PGA_POPREPL_NSGA_II        Use NSGA-II replacement for multi-objective opt.
+PGA_POPREPL_NSGA_III       Use NSGA-III replacement for multi-objective opt.
+PGA_POPREPL_PAIRWISE_BEST  Compare same index in old and new population
+PGA_POPREPL_RANDOM_NOREP   Population replacement random no replacement
+PGA_POPREPL_RANDOM_REP     Population replacement random with replacement
+PGA_POPREPL_RTR            Restricted Tournament Replacement
+PGA_REPORT_AVERAGE         Report average evaluation
+PGA_REPORT_HAMMING         Report hamming distance
+PGA_REPORT_OFFLINE         Report offline
+PGA_REPORT_ONLINE          Report online
+PGA_REPORT_STRING          Report the string
+PGA_REPORT_WORST           Report the worst evaluation
+PGA_SELECT_LINEAR          Return individuals in population order
+PGA_SELECT_PROPORTIONAL    Fitness-proportional selection
+PGA_SELECT_PTOURNAMENT     Binary probabilistic tournament selection
+PGA_SELECT_SUS             Stochastic universal selection
+PGA_SELECT_TOURNAMENT      Tournament selection
+PGA_SELECT_TRUNCATION      Truncation selection
+PGA_STOP_MAXITER           Stop on max iterations
+PGA_STOP_NOCHANGE          Stop on max number of generations no change
+PGA_STOP_TOOSIMILAR        Stop when individuals too similar
+========================== ===========================================
+
+User Defined Data Types
+-----------------------
+
+The latest version of PGAPy features user defined data types. Just
+define your data type and pass it as the second parameter to the
+``PGA`` constructor. The framework will take care of serializing the
+data when transmitting via ``MPI`` (if you're running a parallel
+version).
+
+If duplicate checking is enabled via the ``no_duplicates`` constructor
+parameter, your data type needs to define a ``__hash__`` method (unless
+the python default hash method fulfills your requirements).
+
+User defined data types do not use alleles, so the normal ``get_allele``
+(and ``set_allele``) methods are not available. Instead the full
+individual can be retrieved with the ``get_gene`` method and set with
+the ``set_gene`` method.
+
+With user data types you need to define the following methods:
+
+- ``check_duplicate (self, p1, pop1, p2, pop2)`` if you enable duplicate
+  checking with the crossover parameter ``no_duplicates``. This should
+  return True when the two individuals are duplicates. Use ``get_gene``
+  to retrieve the genes for the individuals ``p1`` and ``p2`` in
+  populations ``pop1`` and ``pop2``.
+- ``crossover (self, p1, p2, ppop, c1, c2, cpop)`` for crossover
+  operation, use ``get_gene`` for getting the parent genes for the
+  parents ``p1`` and ``p2`` in generation ``ppop`` and use ``set_gene``
+  for setting the child genes ``c1`` and ``c2`` in generation ``cpop``.
+- ``initstring (self, p, pop)`` for initializing the given string, use
+  ``set_gene`` in that method for setting your object as a gene.
+- ``mutation (self, p, pop, pm)`` for the mutation operation. This
+  should return the number of mutations performed. If duplicate checking
+  is enabled, the framework will repeatedly call the mutation operator
+  for mutating a duplicate individual into another individual that is no
+  duplicate. This uses the return value of your mutation method. You
+  will enter an endless loop if your mutation operator does not
+  occasionally return an non-zero number of mutatations performed when
+  duplicate checking is enabled. The ``pm`` parameter gives the mutation
+  probability. Use ``get_gene`` for retrieving the individual to be
+  mutated and use ``set_gene`` to update this individual after mutation.
+- ``print_string (self, file, p, pop)`` to print a gene object, use
+  ``get_gene`` for retrieving the individual to be printed.
+
+For these methods it is generally a good idea to never modify an
+individual in-place: This individual may be repeatedly used in genetic
+operations (e.g. mutation and crossover), so when modifying it you will
+produce erroneous results for later genetic operations. To copy a data
+structure, python's ``deepcopy`` function in the module ``copy`` is
+usually used.
+
+In addition to the methods above you may want to define a stopping rule
+with a ``stop_cond`` method or override the way a hash is computed using
+a ``hash`` method. The default for computing a hash is to call
+``hash (gene)`` where gene is an object of the user defined data type.
+Other methods that may be used is an ``endofgen`` method, a
+``gene_distance`` method (e.g., when using Restricted Tournament
+Replacement, with ``PGA_POPREPL_RTR``), or a ``pre_eval`` method.
+
+An example with user defined data types is in ``examples/gp``: This
+implements Genetic Programming with a tree data structure. Note that the
+``Node`` class in ``gp.py`` has a ``__hash__`` method that builds a hash
+over the serialization of the tree (which is the same for individuals
+with the same tree structure).
+
+
+Missing Features
+----------------
+
+As already mentioned, not all functions and constants of PGAPack_ are
+wrapped yet |--| still for many applications the given set should be
+enough. If you need additional functions, you may want to wrap these and
+send_ me a patch.
+
+Reporting Bugs
+--------------
+
+Please use the `Sourceforge Bug Tracker`_  or the `Github Bug Tracker`_ and
+
+- give a short description of what you think is the correct behaviour
+- give a description of the observed behaviour
+- tell me exactly what you did.
+- if you can publish your source code this makes it a lot easier to
+  debug for me
+
+.. _`Sourceforge Bug Tracker`:
+    http://sourceforge.net/tracker/?group_id=152022&atid=782852
+.. _`Github Bug Tracker`:
+    https://github.com/schlatterbeck/pgapy/issues
+.. _send: mailto:rsc@runtux.com
+
+Resources
+---------
+
+Project information and download from `Sourceforge main page`_
+
+.. _`Sourceforge main page`: http://sourceforge.net/projects/pgapy/
+
+or checkout from Github_
+
+.. _`Github`: http://github.com/schlatterbeck/pgapy
+
+or directly install via pypi.
+
+Installation
+------------
+
+PGApy, as the name suggests, supports parallelizing the evaluation
+function of the genetic algorithm. This uses the Message Passing
+Interface (MPI_) standard.
+
+To install a *serial* version (without parallel programming using MPI_)
+you can simply install from pypi using ``pip``. Alternatively when you
+have unpacked or checked out from sources you can install with::
+
+ python3 setup.py install --prefix=/usr/local
+
+If you want a parallel version using an MPI_ (Message-Passing Interface)
+library you will have to install a parallel version of PGAPack_ first.
+The easiest way to do this is to use `my pgapack debian package builder`_
+from github. Clone this repository, check out the branch ``master``,
+install the build dependencies, they're listed in the file
+``debian/control`` and build the debian packages using::
+
+  dpkg-buildpackage -rfakeroot
+
+This builds pgapack debian packages for *all* supported MPI libraries in
+debian, currently these are ``mpich``, ``openmpi``, and ``lam``. In addition
+to the MPI libraries a serial version of the pgapack library is also
+built. Proceed by installing the package pgapack and the MPI backend
+library of choice. If you don't have a preference for an MPI library,
+``libpgapack-openmpi`` is the package that uses the Debians default
+preferences of an MPI library.
+
+Once a parallel version of PGAPack_ is installed, you can install PGApy
+as follows: You set environment variables for the ``PGA_PARALLEL_VARIANT``
+(one of ``mpich``, ``openmpi``, or ``lam``) and set the ``PGA_MODULE`` to
+``module_from_parallel_install``. Finally you envoke the setup, e.g.::
+
+ export PGA_PARALLEL_VARIANT=openmpi
+ export PGA_MODULE=module_from_parallel_install
+ python3 setup.py install --prefix=/usr/local
+
+Note that the same works with ``pip install``, i.e., after installation
+of a parallel version of PGAPack_ you can directly install with ``pip``::
+
+ export PGA_PARALLEL_VARIANT=openmpi
+ export PGA_MODULE=module_from_parallel_install
+ pip install pgapy
+
+or alternatively depending on how pip is installed on your system::
+
+ python3 -m pip install pgapy
+
+If your MPI library is installed in a different place you should study
+the *Extension* configurations in ``setup.py`` to come up with an
+Extension definition that fits your installation. If your installation
+is interesting to more people, feel free to submit a patch that adds
+your Extension-configuration to the standard ``setup.py``.
+
+Running with MPI
+----------------
+
+To run a parallel version with MPI_, a parallel version must be
+installed, see above in section Installation_.
+
+For a serial version, PGAPy makes sure that the otimization is aborted
+if an exception occurs in the ``evaluate`` function. This is currently not
+the case for MPI, because the framework currently does not support
+returning information to the rank-0 MPI leader process. A workaround is
+as follows: Rename your ``evaluate`` method to ``_evaluate`` and catch
+exceptions in a new ``evaluate`` method that wraps ``_evaluate``.
+Call ``MPI_Abort`` if an exception occurs::
+
+    import traceback
+    import sys
+
+    ...
+
+    def evaluate (self, p, pop):
+        try:
+            return self._evaluate (p, pop)
+        except Exception:
+            # Optionally log exception here
+            print (traceback.format_exc ())
+            pga.MPI_Abort (1)
+            sys.exit (1)
+
+Testing
+-------
+
+For testing |--| preferrably before installation you can build locally::
+
+    python3 setup.py build_ext --inplace
+
+After this you have a ``pga.*.so`` file in the local directory. Now you
+can run the tests with::
+
+    python3 -m pytest test
+
+This runs all the tests and can take a while. Note that the tests run
+most of the examples in the ``examples`` directory with different
+command line parameters where available. To perform several optimization
+runs in a single (Python-) process, we must call ``MPI_Init``
+*explicitly* (and not relying on PGAPack_ to call it implicitly). This is
+because ``MPI_Init`` may be called only once per process. Calling of
+``MPI_Init`` and ``MPI_Finalize`` is handled in a fixture in
+``test/conftest.py``
+
+Coverage
+++++++++
+
+For the python examples, the coverage can be computed with::
+
+  python3 -m pytest --cov examples test
+
+or more verbose including untested lines with::
+
+  python3 -m pytest --cov-report term-missing --cov examples test
+
+Performing a coverage analysis for the C code in ``pgamodule.c`` is
+currently possible only on Linux |--| at least, since I'm developing on
+Linux this is the architecture where I've found out how to perform
+coverage analysis including the C code.
+To compile for coverage analysis::
+
+  export CFLAGS=-coverage
+  python3 setup.py build_ext --inplace
+
+This will create a file ending in ``.gcno`` under the ``build`` directory,
+typically something like ``build/temp.linux-x86_64-3.9`` when using
+``python3.9`` on the ``x86_64`` architecture. Running the tests will
+create statistics data files with ending ``.gcda``. These are data files
+for the GNU profiler ``gcov``. From these, ``.html`` files can be
+generated that can be inspected with a browser::
+
+  lcov --capture --directory . --output-file coverage.info
+  genhtml coverage.info --output-directory coverage_out
+
+Note that the ``lcov`` program is part of the linux distribution.
+
+Running under MPI
++++++++++++++++++
+
+The tests can be directly run under MPI. Note that currently the
+``--with-mpi`` option of ``pytest`` is *not* supported. This option
+asumes that the package ``mpi4py`` is used. But ``pgapy`` uses only
+calls from pgapack, which in turn calls MPI.
+
+Running under MPI is done using::
+
+ mpirun $MPI_OPTIONS python3 -m pytest test
+
+The ``MPI_OPTIONS`` can be, e.g.::
+
+    MPI_OPTIONS=--machinefile ~/.mpi-openmpi --np 8
+
+which would use a machine definition file for openmpi in your home
+directory and eight processes.
+
+Running under MPI is especially useful for determining C code coverage.
+Asuming a parallel version of ``openmpi`` is installed, the code can be
+compiled with::
+
+ PGA_PARALLEL_VARIANT=openmpi
+ PGA_MODULE=module_from_parallel_install
+ export CFLAGS=-coverage
+ python3 setup.py build_ext --inplace
+
+Note that the coverage analysis uses files in the build directory which
+need to be present before a parallel version can be started. Otherwise
+each parallel instance would try to create the coverage files resulting
+in race conditions. Once the coverage files are in place, the coverage
+framework ensures proper locking so that no two processes write
+concurrently to the same coverage files.
+
+Creating the coverage files is best achieved by running the tests
+without MPI first and then running the same version with a number of
+processes under MPI. Running under MPI shows that the serialization and
+deserialization code in ``pgamodule.c`` is called.
+
+As of this writing we get::
+
+ Lines:      1423    1475    96.5 %
+ Functions:   131     133    98.5 %
+
+
+References
+----------
+
+.. [1]  Georges Harik. Finding multiple solutions in problems of bounded
+        difficulty. IlliGAL Report 94002, Illinois Genetic Algorithm Lab,
+        May 1994.
+.. [2]  Georges R. Harik. Finding multimodal solutions using restricted
+        tournament selection. In Eshelman [3]_, pages 24–31.
+.. [3]  Larry J. Eshelman, editor. *Proceedings of the 6th International
+        Conference on Genetic Algorithms (ICGA)*. Morgan Kaufmann, July 1995.
+.. [4]  Martin Pelikan. *Hierarchical Bayesian Optimization Algorithm:
+        Toward a New Generation of Evolutionary Algorithms*, volume 170 of
+        Studies in Fuzziness and Soft Computing.  Springer, 2005.
+.. [5]  Rainer Storn and Kenneth Price. Differential evolution |--| a simple
+        and efficient heuristic for global optimization over continuous
+        spaces. *Journal of Global Optimization*, 11(4):341–359, December
+        1997.
+.. [6]  Kenneth V. Price, Rainer M. Storn, and Jouni A. Lampinen.
+        *Differential Evolution: A Practical Approach to Global
+        Optimization.*  Springer, Berlin, Heidelberg, 2005.
+.. [7]  Kalyanmoy Deb, Amrit Pratap, Sameer Agarwal, and T. Meyarivan. A
+        fast and elitist multiobjective genetic algorithm: NSGA-II. *IEEE
+        Transactions on Evolutionary Computation*, 6(2):182–197, April 2002.
+.. [8]  Kalyanmoy Deb and Himanshu Jain. An evolutionary many-objective
+        optimization algorithm using reference-point-based nondominated
+        sorting approach, part I: Solving problems with box constraints.
+        *IEEE Transactions on Evolutionary Computation*, 18(4):577–601,
+        August 2014.
+.. [9]  Himanshu Jain and Kalyanmoy Deb. An evolutionary many-objective
+        optimization algorithm using reference-point-based nondominated
+        sorting approach, part II: Handling constraints and extending to
+        an adaptive approach. *IEEE Transactions on Evolutionary
+        Computation*, 18(4):602–622, August 2014.
+.. [10] Tetsuyuki Takahama and Setsuko Sakai. Constrained optimization
+        by the |epsilon| constrained differential evolution with an
+        archive and gradient-based mutation. In [11]_.
+.. [11] *IEEE Congress on Evolutionary Computation (CEC)*. Barcelona,
+        Spain, July 2010.
+.. [12] Indraneel Das and J. E. Dennis. Normal-boundary intersection: A new
+        method for generating the pareto surface in nonlinear multicriteria
+        optimization problems. SIAM Journal on Optimization, 8(3):631–657,
+        August 1998.
+
+Changes
+-------
+
+Version 2.2.2: Add pyproject.toml
+
+- Add pyproject.toml -- unfortunately it seems that binary modules
+  cannot currently be described in the pyproject.toml, especially not
+  the variant selection via the environment that is currently
+  implemented in setup.py
+
+Version 2.2.1: MPI_Abort
+
+- Add MPI_Abort to the wrapper
+- Include ``mpi_stub.c`` in the release (this is missing if some env
+  variables are set, see above in Installation)
+
+Version 2.2: Module directory
+
+- Put the pga C-module inside a pga module
+- Add several python-only modules to pga
+- pga.__init__ exports everything to this is compatible
+- pga.random includes a python Random class based on the pgapack random
+  number generator
+
+Version 2.1: Regression test
+
+- PGAPack bug-fixes discovered during testing
+- Bug-fixes of python wrapper
+- Lots of tests with coverage of wrapper C-code > 90%
+
+Version 2.0: User defined data types
+
+- Implement user defined data types, note that your data type can be
+  variable-size, e.g., a tree data structure. The framework takes care
+  of serializing the data type and transmitting it to a remote MPI
+  process if using a parallel version.
+- When duplicate checking is enabled with the constructor parameter
+  ``no_duplicates``, the underlying pgapack code now uses a hash table.
+  This means the effort is no longer quadratic in the population size
+  but linear.
+- Example of Genetic Programming (GP) in the ``examples/gp`` directory
+- Rename the gene_difference method to gene_distance
+
+Version 1.8: Epsilon-constrained optimization
+
+- Epsilon-constrained optimization
+- Precision for printing evals in multi-objective optimization, use this
+  feature for making regression-test work on AMD where a floating-point
+  difference in the 16th or so decimal place made a test fail
+- Crossover for permutations
+- Version-numbers: try to match pgapack, we might still diverge in the
+  last digit, though
+
+Version 1.2: Many-objective optimization with NSGA-III
+
+- Implement NSGA-III
+
+Version 1.1.6: Polynomial mutation and simulated binary crossover (SBX)
+
+- Simulated binary crossover (SBX)
+- Polynomial mutation
+
+Version 1.1.1-1.1.5: Small PGAPack updates, fixes for non-debian
+
+- Fix setup.py for non-debian systems
+- Update to latest PGAPack with small changes
+
+Version 1.1: Add multi-objective optimization with NSGA-II
+
+- Wrap latest pgapack version 1.4
+- This add multi-objective optimization using the Nondominated Sorting
+  Genetic Algorithm version 2 (NSGA-II) by Deb et. al. This makes use of
+  the previously-introduced option to return more than one value in the
+  objective function. To use the feature you need to set the
+  num_constraint parameter to a value that leave some of the function
+  values returned by your evaluation function as objective function
+  values (and not as constraints). See example in examples/multi.py.
+
+Version 1.0: Add constraint handling
+
+- Wrap latest pgapack version 1.3
+- This adds auxiliary evaluations. Now your evaluation function can
+  return *multiple* floating-point values as a sequence if you set the
+  num_eval parameter >1 in the constructor. Currently additional
+  evaluation values are used for constraint handling. Constraint values
+  are minimized.  Once they reach zero or a negative value they no
+  longer count: The sum of all positive constraints is the overall
+  constraint violation.  For details see paper by Deb, 2000, see user
+  guide for citation. If you're not using constraints, nothing in your
+  code needs changes.
+- This release may change the path an optimization takes. So for the
+  same seed of the random number generator you will get a different
+  result, at least if during the search there are individuals with the
+  same evaluation (and different genetic material). This is due to a
+  change of the sort function in pgapack (it switched to a stable sort
+  from the C standard library).
+
+Version 0.9: Allow installation of parallel version
+
+- Pass argv (or sys.argv) to PGACreate
+- Add a stanza to setup.py to allow a parallel installation with a given
+  pgapack variant compiled for an MPI library. This currently needs a
+  pre-installed pgapack debian package.
+
+Version 0.8: Bugfix in real mutation
+
+- Fix a core-dump in the latest pgapack
+
+Version 0.7: Major changes in wrapping
+
+- Now Differential Evolution is implemented, see the minfloat example
+  and the user guide of pgapack.
+
+Version 0.6: Major changes in wrapping
+
+- Now the wrapping uses the standard Python recommendations on how to
+  create a custom class.
+- Update documentation
+- Rename ``fitness_cmax`` (from ``fitness_cmax_value``)
+- Better error checking of parameters
+
+Version 0.5: Bug-fix release
+
+- Now the ``setup.py`` works, previous version had an encoding problem
+- Wrap some minor new methods
+- Bug-fix in PGAPack truncation selection
+
+Version 0.4: Bundle PGAPack
+
+- The PGAPack package is now included as a git submodule. By default we
+  build against this library
+- License fixes: The module long shipped a ``COPYING`` file that includes
+  the 2-clause BSD license. But the headers of ``setup.py`` and ``pgamodule.c``
+  still included another license. This has been corrected.
+
+Version 0.3: Feature enhancements, Bug fixes
+
+Port to Python3, Python2 is still supported, license change.
+
+- C-Code of wrapper updated to support both, Python2 and Python3
+- Update documentation
+- Fix some memory leaks that could result when errors occurred during
+  some callback methods
+- License change: We now have the 2-clause BSD license (similar to the
+  MPICH license of PGAPack), this used to be LGPL.
+
+Version 0.2: Feature enhancements, Bug fixes
+
+64 bit support, more PGAPack functions and attributes wrapped,
+Readme-update: Sourceforge logo, Changes chapter.
+
+- Bug-fixes for 64 bit architectures
+- More functions and attributes of PGAPack wrapped
+- Add a build-rule to ``setup.py`` to allow building for standard-install
+  of PGAPack |--| this currently needs editing of ``setup.py`` |--| should use
+  autodetect here but this would require that I set up a machine with
+  standard install of PGAPack for testing.
+- Add Sourceforge logo as required
+- Add Changes chapter for automagic releases
+- Add the ``__module__`` string to class ``PGA`` in module ``pga``. Now
+  calling:: ``help (pga)`` in python works as expected, previously no
+  help-text was given for the included module
+
+Version 0.1: Initial freshmeat announcement
+
+PGAPy is a wrapper for PGAPack, the parallel genetic algorithm library,
+a powerful genetic algorithm library. PGAPy wraps this library for use
+with Python. Pgapack is one of the most complete and accurate genetic
+algorithm implementations out there with a lot of features for
+experimentation.
+
+- Initial Release
+
+.. _`PGAPack Readme`:
+   https://github.com/schlatterbeck/pgapack/blob/master/README.rst
+.. _PGAPack:          http://ftp.mcs.anl.gov/pub/pgapack/
+.. _`PGAPack fork on github`: https://github.com/schlatterbeck/pgapack
+.. _MPI: http://mpi-forum.org/
+.. _`my pgapack debian package builder`:
+    https://github.com/schlatterbeck/debian-pgapack
```

### Comparing `PGAPy-2.2.1/README.html` & `PGAPy-2.2.2/README.html`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 <?xml version="1.0" encoding="utf-8" ?>
 <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
 <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
 <head>
 <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
-<meta name="generator" content="Docutils 0.16: http://docutils.sourceforge.net/" />
+<meta name="generator" content="Docutils 0.19: https://docutils.sourceforge.io/" />
 <title>PGAPy: Python Wrapper for PGAPack Parallel Genetic Algorithm Library</title>
 <meta name="author" content="Ralf Schlatterbeck &lt;rsc&#64;runtux.com&gt;" />
 <style type="text/css">
 
 /*
 :Author: David Goodger
 :Contact: goodger@users.sourceforge.net
@@ -359,26 +359,26 @@
 ftp site, it is written in ANSI C but will probably not compile against
 a recent version of <a class="reference external" href="http://mpi-forum.org/">MPI</a>. It will also not work with recent versions of
 PGAPy. Note that this version is not actively maintained. I've started a
 <a class="reference external" href="https://github.com/schlatterbeck/pgapack">PGAPack fork on github</a> where I've ported the library to the latest
 version of the <a class="reference external" href="http://mpi-forum.org/">MPI</a> standard and have fixed some minor inconsistencies
 in the documentation. I've also implemented some new features, notably
 enhancements in selection schemes, a new replacement strategy called
-<em>restricted tournament replacement</em> <a class="footnote-reference" href="#id11" id="id1">[1]</a>, <a class="footnote-reference" href="#id12" id="id2">[2]</a>, <a class="footnote-reference" href="#id15" id="id3">[4]</a> and, more recently,
-the differential evolution strategy <a class="footnote-reference" href="#id16" id="id4">[5]</a>, <a class="footnote-reference" href="#id17" id="id5">[6]</a>. In addition this version
-now supports multi objective optimization with NSGA-II <a class="footnote-reference" href="#id18" id="id6">[7]</a> and
-many-objective optimization with NSGA-III <a class="footnote-reference" href="#id19" id="id7">[8]</a>, <a class="footnote-reference" href="#id20" id="id8">[9]</a>. It also supports
-the Epsilon Constraint method <a class="footnote-reference" href="#id21" id="id9">[10]</a>.</p>
+<em>restricted tournament replacement</em> <a class="footnote-reference" href="#footnote-1" id="footnote-reference-1">[1]</a>, <a class="footnote-reference" href="#footnote-2" id="footnote-reference-2">[2]</a>, <a class="footnote-reference" href="#footnote-4" id="footnote-reference-3">[4]</a> and, more recently,
+the differential evolution strategy <a class="footnote-reference" href="#footnote-5" id="footnote-reference-4">[5]</a>, <a class="footnote-reference" href="#footnote-6" id="footnote-reference-5">[6]</a>. In addition this version
+now supports multi objective optimization with NSGA-II <a class="footnote-reference" href="#footnote-7" id="footnote-reference-6">[7]</a> and
+many-objective optimization with NSGA-III <a class="footnote-reference" href="#footnote-8" id="footnote-reference-7">[8]</a>, <a class="footnote-reference" href="#footnote-9" id="footnote-reference-8">[9]</a>. It also supports
+the Epsilon Constraint method <a class="footnote-reference" href="#footnote-10" id="footnote-reference-9">[10]</a>.</p>
 <p>Note: When using NSGA_III replacement for multi (or many-) objective
 optimization you need to either</p>
 <ul>
 <li><p class="first">set reference points on the hyperplane intersecting all axes at
 offset 1. These reference points can be obtained with the convenience
 function <tt class="docutils literal">pga.das_dennis</tt>, it creates a regular set of reference points
-using an algorithm originally publised by I. Das and J. E. Dennis <a class="footnote-reference" href="#id24" id="id10">[12]</a>.
+using an algorithm originally publised by I. Das and J. E. Dennis <a class="footnote-reference" href="#footnote-12" id="footnote-reference-10">[12]</a>.
 These points are then passed as the parameter <tt class="docutils literal">reference_points</tt> to
 the <tt class="docutils literal">PGA</tt> constructor.</p>
 <p>See <tt class="docutils literal">examples/dtlz2.py</tt> for a usage example and the user guide for
 the bibliographic reference. The function gets the dimensionality of
 the objective space (<tt class="docutils literal">num_eval</tt> minus <tt class="docutils literal">num_constraint</tt>) and the
 number of partition to use.</p>
 </li>
@@ -1581,116 +1581,123 @@
 Lines:      1423    1475    96.5 %
 Functions:   131     133    98.5 %
 </pre>
 </div>
 </div>
 <div class="section" id="references">
 <h1>References</h1>
-<table class="docutils footnote" frame="void" id="id11" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-1" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id1">[1]</a></td><td>Georges Harik. Finding multiple solutions in problems of bounded
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-1">[1]</a></td><td>Georges Harik. Finding multiple solutions in problems of bounded
 difficulty. IlliGAL Report 94002, Illinois Genetic Algorithm Lab,
 May 1994.</td></tr>
 </tbody>
 </table>
-<table class="docutils footnote" frame="void" id="id12" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-2" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id2">[2]</a></td><td>Georges R. Harik. Finding multimodal solutions using restricted
-tournament selection. In Eshelman <a class="footnote-reference" href="#id14" id="id13">[3]</a>, pages 24–31.</td></tr>
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-2">[2]</a></td><td>Georges R. Harik. Finding multimodal solutions using restricted
+tournament selection. In Eshelman <a class="footnote-reference" href="#footnote-3" id="footnote-reference-11">[3]</a>, pages 24–31.</td></tr>
 </tbody>
 </table>
-<table class="docutils footnote" frame="void" id="id14" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-3" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id13">[3]</a></td><td>Larry J. Eshelman, editor. <em>Proceedings of the 6th International
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-11">[3]</a></td><td>Larry J. Eshelman, editor. <em>Proceedings of the 6th International
 Conference on Genetic Algorithms (ICGA)</em>. Morgan Kaufmann, July 1995.</td></tr>
 </tbody>
 </table>
-<table class="docutils footnote" frame="void" id="id15" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-4" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id3">[4]</a></td><td>Martin Pelikan. <em>Hierarchical Bayesian Optimization Algorithm:
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-3">[4]</a></td><td>Martin Pelikan. <em>Hierarchical Bayesian Optimization Algorithm:
 Toward a New Generation of Evolutionary Algorithms</em>, volume 170 of
 Studies in Fuzziness and Soft Computing.  Springer, 2005.</td></tr>
 </tbody>
 </table>
-<table class="docutils footnote" frame="void" id="id16" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-5" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id4">[5]</a></td><td>Rainer Storn and Kenneth Price. Differential evolution – a simple
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-4">[5]</a></td><td>Rainer Storn and Kenneth Price. Differential evolution – a simple
 and efficient heuristic for global optimization over continuous
 spaces. <em>Journal of Global Optimization</em>, 11(4):341–359, December
 1997.</td></tr>
 </tbody>
 </table>
-<table class="docutils footnote" frame="void" id="id17" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-6" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id5">[6]</a></td><td>Kenneth V. Price, Rainer M. Storn, and Jouni A. Lampinen.
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-5">[6]</a></td><td>Kenneth V. Price, Rainer M. Storn, and Jouni A. Lampinen.
 <em>Differential Evolution: A Practical Approach to Global
 Optimization.</em>  Springer, Berlin, Heidelberg, 2005.</td></tr>
 </tbody>
 </table>
-<table class="docutils footnote" frame="void" id="id18" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-7" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id6">[7]</a></td><td>Kalyanmoy Deb, Amrit Pratap, Sameer Agarwal, and T. Meyarivan. A
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-6">[7]</a></td><td>Kalyanmoy Deb, Amrit Pratap, Sameer Agarwal, and T. Meyarivan. A
 fast and elitist multiobjective genetic algorithm: NSGA-II. <em>IEEE
 Transactions on Evolutionary Computation</em>, 6(2):182–197, April 2002.</td></tr>
 </tbody>
 </table>
-<table class="docutils footnote" frame="void" id="id19" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-8" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id7">[8]</a></td><td>Kalyanmoy Deb and Himanshu Jain. An evolutionary many-objective
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-7">[8]</a></td><td>Kalyanmoy Deb and Himanshu Jain. An evolutionary many-objective
 optimization algorithm using reference-point-based nondominated
 sorting approach, part I: Solving problems with box constraints.
 <em>IEEE Transactions on Evolutionary Computation</em>, 18(4):577–601,
 August 2014.</td></tr>
 </tbody>
 </table>
-<table class="docutils footnote" frame="void" id="id20" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-9" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id8">[9]</a></td><td>Himanshu Jain and Kalyanmoy Deb. An evolutionary many-objective
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-8">[9]</a></td><td>Himanshu Jain and Kalyanmoy Deb. An evolutionary many-objective
 optimization algorithm using reference-point-based nondominated
 sorting approach, part II: Handling constraints and extending to
 an adaptive approach. <em>IEEE Transactions on Evolutionary
 Computation</em>, 18(4):602–622, August 2014.</td></tr>
 </tbody>
 </table>
-<table class="docutils footnote" frame="void" id="id21" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-10" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id9">[10]</a></td><td>Tetsuyuki Takahama and Setsuko Sakai. Constrained optimization
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-9">[10]</a></td><td>Tetsuyuki Takahama and Setsuko Sakai. Constrained optimization
 by the ε constrained differential evolution with an
-archive and gradient-based mutation. In <a class="footnote-reference" href="#id23" id="id22">[11]</a>.</td></tr>
+archive and gradient-based mutation. In <a class="footnote-reference" href="#footnote-11" id="footnote-reference-12">[11]</a>.</td></tr>
 </tbody>
 </table>
-<table class="docutils footnote" frame="void" id="id23" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-11" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id22">[11]</a></td><td><em>IEEE Congress on Evolutionary Computation (CEC)</em>. Barcelona,
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-12">[11]</a></td><td><em>IEEE Congress on Evolutionary Computation (CEC)</em>. Barcelona,
 Spain, July 2010.</td></tr>
 </tbody>
 </table>
-<table class="docutils footnote" frame="void" id="id24" rules="none">
+<table class="docutils footnote" frame="void" id="footnote-12" rules="none">
 <colgroup><col class="label" /><col /></colgroup>
 <tbody valign="top">
-<tr><td class="label"><a class="fn-backref" href="#id10">[12]</a></td><td>Indraneel Das and J. E. Dennis. Normal-boundary intersection: A new
+<tr><td class="label"><a class="fn-backref" href="#footnote-reference-10">[12]</a></td><td>Indraneel Das and J. E. Dennis. Normal-boundary intersection: A new
 method for generating the pareto surface in nonlinear multicriteria
 optimization problems. SIAM Journal on Optimization, 8(3):631–657,
 August 1998.</td></tr>
 </tbody>
 </table>
 </div>
 <div class="section" id="changes">
 <h1>Changes</h1>
+<p>Version 2.2.2: Add pyproject.toml</p>
+<ul class="simple">
+<li>Add pyproject.toml -- unfortunately it seems that binary modules
+cannot currently be described in the pyproject.toml, especially not
+the variant selection via the environment that is currently
+implemented in setup.py</li>
+</ul>
 <p>Version 2.2.1: MPI_Abort</p>
 <ul class="simple">
 <li>Add MPI_Abort to the wrapper</li>
 <li>Include <tt class="docutils literal">mpi_stub.c</tt> in the release (this is missing if some env
 variables are set, see above in Installation)</li>
 </ul>
 <p>Version 2.2: Module directory</p>
```

### Comparing `PGAPy-2.2.1/README.rst` & `PGAPy-2.2.2/README.rst`

 * *Files 0% similar despite different names*

```diff
@@ -846,14 +846,21 @@
         method for generating the pareto surface in nonlinear multicriteria
         optimization problems. SIAM Journal on Optimization, 8(3):631–657,
         August 1998.
 
 Changes
 -------
 
+Version 2.2.2: Add pyproject.toml
+
+- Add pyproject.toml -- unfortunately it seems that binary modules
+  cannot currently be described in the pyproject.toml, especially not
+  the variant selection via the environment that is currently
+  implemented in setup.py
+
 Version 2.2.1: MPI_Abort
 
 - Add MPI_Abort to the wrapper
 - Include ``mpi_stub.c`` in the release (this is missing if some env
   variables are set, see above in Installation)
 
 Version 2.2: Module directory
```

### Comparing `PGAPy-2.2.1/examples/cards.py` & `PGAPy-2.2.2/examples/cards.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/cards_mutate.py` & `PGAPy-2.2.2/examples/cards_mutate.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/constraint.py` & `PGAPy-2.2.2/examples/constraint.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/dtlz2.py` & `PGAPy-2.2.2/examples/dtlz2.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/fourbar.py` & `PGAPy-2.2.2/examples/fourbar.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/gears.py` & `PGAPy-2.2.2/examples/gears.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/gp/README.rst` & `PGAPy-2.2.2/examples/gp/README.rst`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/gp/gp.py` & `PGAPy-2.2.2/examples/gp/gp.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/gp/opt_integral.py` & `PGAPy-2.2.2/examples/gp/opt_integral.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/gp/opt_parity3.py` & `PGAPy-2.2.2/examples/gp/opt_parity3.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/gp/opt_xor.py` & `PGAPy-2.2.2/examples/gp/opt_xor.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/hello_world_char.py` & `PGAPy-2.2.2/examples/hello_world_char.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/hello_world_int.py` & `PGAPy-2.2.2/examples/hello_world_int.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/himmelblau.py` & `PGAPy-2.2.2/examples/himmelblau.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/magic_prio.py` & `PGAPy-2.2.2/examples/magic_prio.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/magic_square.py` & `PGAPy-2.2.2/examples/magic_square.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/minfloat.py` & `PGAPy-2.2.2/examples/minfloat.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/multi.py` & `PGAPy-2.2.2/examples/multi.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/namefull.py` & `PGAPy-2.2.2/examples/namefull.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/one_max.py` & `PGAPy-2.2.2/examples/one_max.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/sequence/croes.tsp` & `PGAPy-2.2.2/examples/sequence/croes.tsp`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/sequence/oliver30.tsp` & `PGAPy-2.2.2/examples/sequence/oliver30.tsp`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/sequence/plot_tour.py` & `PGAPy-2.2.2/examples/sequence/plot_tour.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/sequence/tsp.py` & `PGAPy-2.2.2/examples/sequence/tsp.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/sort_numbers.py` & `PGAPy-2.2.2/examples/sort_numbers.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/twobar.py` & `PGAPy-2.2.2/examples/twobar.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/vibr.py` & `PGAPy-2.2.2/examples/vibr.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/examples/xor.py` & `PGAPy-2.2.2/examples/xor.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pga/__init__.py` & `PGAPy-2.2.2/pga/__init__.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pga/random.py` & `PGAPy-2.2.2/pga/random.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pga/testsupport.py` & `PGAPy-2.2.2/pga/testsupport.py`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgamodule.c` & `PGAPy-2.2.2/pgamodule.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/docs/user_guide.pdf` & `PGAPy-2.2.2/pgapack/docs/user_guide.pdf`

 * *Installing the 'pypdf' Python module from the 'python3-pypdf' package may produce a better output.*

 * *Files 4% similar despite different names*

#### pdftotext {} -

```diff
@@ -2418,15 +2418,14 @@
 • The functions PGAEncodeRealAsBinary, PGAEncodeRealAsGrayCode, PGAEncodeIntegerAsBinary,
 and PGAEncodeIntegerAsGrayCode allow the user’s hill-climbing function to encode integer or real
 numbers as binary or Gray code strings.
 • The functions PGAGetEvaluation and PGASetEvaluation allow the user’s hill-climbing function to get and set evaluation function values, and PGASetEvaluationUpToDateFlag and
 PGAGetEvaluationUpToDateFlag to get and set the flag that indicates whether an evaluation function
 value is up to date. These functions have an optional fifth argument aux, that allows to get or set the
 auxiliary evaluations, see section 4.9.
-
 One way to run a hybrid GA and use PGARun is to use the PGASetUserFunction discussed in Chapter 6
 to specify a user function to be called at the end of each GA iteration. A more flexible approach would be
 for the user to call the high-level PGAPack functions, and their hillclimber to explicitly specify the steps of
 the hybrid GA.
 Figure 8.1 is a version of the Maxbit problem given in Section 2.1. It uses the hill-climbing function
 hillclimb, which is called after the recombination step. It randomly selects a gene to set to one. Note the
 48
@@ -2651,21 +2650,19 @@
 • Fortran does not support command line arguments (Section 4.13).
 • Fortran allows custom usage with native data types (Chapter 6), but not with new data types (Chapter 7).
 • In the MPICH implementation of MPI, the Fortran and C versions of MPI Init are different. If the main
 program is in C, then the C version of MPI Init must be called. If the main program is in Fortran, the
 Fortran version of MPI Init must be called. Therefore, Fortran users of PGAPack with MPICH must
 call MPI Init themselves since PGACreate, which calls MPI Init if users haven’t called it themselves,
 is written in C.
-
 53
 
 • The DEC Alpha and Silicon Graphics Power Challenge, which have 64-bit C pointers and 32-bit Fortran
 integers (but not the Cray T3D which has 64-bit Fortran integers), have additional differences1 . These
 arise because a Fortran integer is too small to hold the address returned by the C interface routine.
-
 – The context variable should be declared integer*8.
 – MPI COMM WORLD should not be passed directly to PGAPack Fortran functions. Instead,
 PGAGetCommunicator should be called to return the address into an integer*8 variable. For
 example
 integer pid
 integer*8 comm
 comm = PGAGetCommunicator(ctx)
@@ -2991,122 +2988,104 @@
 
 Function Bindings
 Symbolic Constants
 PGAPack defines many symbolic constants that are used as arguments to PGAPack functions. These
 constants are the same for both Fortran and C. Below is a list of these constants. These constants are the
 same for both Fortran and C.
 • PGAPack Data Types
-
 – PGA DATATYPE BINARY
 – PGA DATATYPE INTEGER
 – PGA DATATYPE REAL
 – PGA DATATYPE CHARACTER
 – PGA DATATYPE USER
 • String Types
-
 – PGABinary
 – PGAInteger
 – PGAReal
 – PGACharacter
 • Data Types used in PGAError Calls
-
 – PGA INT
 – PGA DOUBLE
 – PGA CHAR
 – PGA VOID
 • True and False
-
 – PGA TRUE
 – PGA FALSE
 • Miscellaneous PGAPack Flags
-
 – PGA FATAL
 – PGA WARNING
 – PGA UNINITIALIZED INT
 61
 
 – PGA UNINITIALIZED DOUBLE
 • PGAPack Temporary and Population Constants
-
 – PGA TEMP1
 – PGA TEMP2
 – PGA OLDPOP
 – PGA NEWPOP
 • Debug Levels
-
 – PGA DEBUG ENTERED
 – PGA DEBUG EXIT
 – PGA DEBUG MALLOC
 – PGA DEBUG PRINTVAR
 – PGA DEBUG SEND
 – PGA DEBUG RECV
 • Direction of Optimization
-
 – PGA MAXIMIZE
 – PGA MINIMIZE
 • Stopping Criteria
-
 – PGA STOP MAXITER
 – PGA STOP NOCHANGE
 – PGA STOP TOOSIMILAR
 • Crossover
-
 – PGA CROSSOVER ONEPT
 – PGA CROSSOVER TWOPT
 – PGA CROSSOVER UNIFORM
 • Fitness
-
 – PGA FITNESS RAW
 – PGA FITNESS NORMAL
 – PGA FITNESS RANKING
 • Fitness Minimization
-
 – PGA FITNESSMIN RECIPROCAL
 – PGA FITNESSMIN CMAX
 • Mutation Type
-
 – PGA MUTATION CONSTANT
 – PGA MUTATION RANGE
 – PGA MUTATION UNIFORM
 – PGA MUTATION GAUSSIAN
 – PGA MUTATION PERMUTE
 62
 
 • Population Replacement
-
 – PGA_POPREPL_BEST
 – PGA_POPREPL_RANDOM_NOREP
 – PGA_POPREPL_RANDOM_REP
 – PGA_POPREPL_RTR
 • Initialization Options
-
 – PGA CINIT LOWER
 – PGA CINIT UPPER
 – PGA CINIT MIXED
 – PGA IINIT PERMUTE
 – PGA IINIT RANGE
 – PGA RINIT PERCENT
 – PGA RINIT RANGE
 • Report Options
-
 – PGA_REPORT_ONLINE
 – PGA_REPORT_OFFLINE
 – PGA_REPORT_GENE_DISTANCE
 – PGA_REPORT_STRING
 – PGA_REPORT_WORST
 – PGA_REPORT_AVERAGE
 • Selection
-
 – PGA_SELECT_PROPORTIONAL
 – PGA_SELECT_SUS
 – PGA_SELECT_TOURNAMENT
 – PGA_SELECT_PTOURNAMENT
 – PGA_SELECT_TRUNCATION
 • User Functions
-
 – PGA_USERFUNCTION_CREATESTRING
 – PGA_USERFUNCTION_MUTATION
 – PGA_USERFUNCTION_CROSSOVER
 – PGA_USERFUNCTION_PRINTSTRING
 – PGA_USERFUNCTION_COPYSTRING
 – PGA_USERFUNCTION_DUPLICATE
 – PGA_USERFUNCTION_INITSTRING
@@ -3794,30 +3773,28 @@
 (with “fake” MPI stub routines and definitions) and the user’s program explicitly includes “real” mpi.h
 or mpif.h header files.
 • If one fails to include mpi.h (or mpif.h) when it should be (such as calling MPI functions directly)
 errors may result. Since pgapack.h includes mpi.h this should not happen in C. The Fortran include
 file, pgapackf.h, however, does not include mpif.h. The user must explicitly include it in every
 subroutine and function that makes MPI calls. Not including mpif.h could result in any of several
 different errors, including
-
 – syntax errors when compiling (for example, MPI COMM WORLD being undefined)
 – general errors in the computed results
 – the program crashing when it calls the undefined subroutine MPI Init
 – general MPI errors such as:
 0 - Error in MPI_COMM_RANK : Invalid communicator
 [0] Aborting program!
 
 75
 
 We have also seen the following error from not including bmpif.h in the main program:
 PGACreate: Invalid value of datatype: 0
 PGAError: Fatal
 • If the ch p4 device in MPICH is used to run on workstations one must have a correct processor group
 file (procgroup). The error message
-
 (ptera-36%)a.out
 p0_18429: p4_error: open error on procgroup file (procgroup): 0
 (ptera-37%)
 may occur if the processor group file is not specified correctly. See the MPICH users guide for more
 details.
 • A common error with the procgroup file when using the ch p4 device in MPICH is to have an incorrect
 path to the executable.
```

### Comparing `PGAPy-2.2.1/pgapack/fakempi/mpi.h` & `PGAPy-2.2.2/pgapack/fakempi/mpi.h`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/include/pgapack.h` & `PGAPy-2.2.2/pgapack/include/pgapack.h`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/binary.c` & `PGAPy-2.2.2/pgapack/source/binary.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/char.c` & `PGAPy-2.2.2/pgapack/source/char.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/cmdline.c` & `PGAPy-2.2.2/pgapack/source/cmdline.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/create.c` & `PGAPy-2.2.2/pgapack/source/create.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/cross.c` & `PGAPy-2.2.2/pgapack/source/cross.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/debug.c` & `PGAPy-2.2.2/pgapack/source/debug.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/duplcate.c` & `PGAPy-2.2.2/pgapack/source/duplcate.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/evaluate.c` & `PGAPy-2.2.2/pgapack/source/evaluate.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/f2c.c` & `PGAPy-2.2.2/pgapack/source/f2c.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/fitness.c` & `PGAPy-2.2.2/pgapack/source/fitness.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/integer.c` & `PGAPy-2.2.2/pgapack/source/integer.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/linalg.c` & `PGAPy-2.2.2/pgapack/source/linalg.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/mpi_stub.c` & `PGAPy-2.2.2/pgapack/source/mpi_stub.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/mutation.c` & `PGAPy-2.2.2/pgapack/source/mutation.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/parallel.c` & `PGAPy-2.2.2/pgapack/source/parallel.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/pga.c` & `PGAPy-2.2.2/pgapack/source/pga.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/pop.c` & `PGAPy-2.2.2/pgapack/source/pop.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/random.c` & `PGAPy-2.2.2/pgapack/source/random.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/real.c` & `PGAPy-2.2.2/pgapack/source/real.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/report.c` & `PGAPy-2.2.2/pgapack/source/report.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/restart.c` & `PGAPy-2.2.2/pgapack/source/restart.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/select.c` & `PGAPy-2.2.2/pgapack/source/select.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/stop.c` & `PGAPy-2.2.2/pgapack/source/stop.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/system.c` & `PGAPy-2.2.2/pgapack/source/system.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/user.c` & `PGAPy-2.2.2/pgapack/source/user.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/pgapack/source/utility.c` & `PGAPy-2.2.2/pgapack/source/utility.c`

 * *Files identical despite different names*

### Comparing `PGAPy-2.2.1/setup.py` & `PGAPy-2.2.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,8 @@
 #!/usr/bin/env python3
-# -*- coding: utf-8 -*-
 # Copyright (C) 2005-23 Dr. Ralf Schlatterbeck Open Source Consulting.
 # Reichergasse 131, A-3411 Weidling.
 # Web: http://www.runtux.com Email: office@runtux.com
 # ****************************************************************************
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are
 # met:
@@ -29,15 +28,15 @@
 # ****************************************************************************
 
 import sys
 from setuptools import setup, Extension
 if sys.version_info.major > 2 :
     from subprocess     import run, PIPE
 try :
-    from Version    import VERSION
+    from pga.Version    import VERSION
 except :
     VERSION = None
 from textwrap       import dedent
 from os             import path, environ
 from glob           import glob
 
 description = []
@@ -165,15 +164,15 @@
                            )
                          , ( 'share/pgapy'
                            , ['pgapack/docs/user_guide.pdf']
                            )
                          ]
     , author           = "Ralf Schlatterbeck"
     , author_email     = "rsc@runtux.com"
-    , url              = "http://pgapy.sourceforge.net/"
+    , url              = "https://github.com/schlatterbeck/pgapy"
     , classifiers      = \
         [ 'Development Status :: 5 - Production/Stable'
         , 'Intended Audience :: Developers'
         , 'Intended Audience :: Education'
         , 'Intended Audience :: Science/Research'
         , 'License :: OSI Approved :: ' + license
         , 'Operating System :: OS Independent'
```

### Comparing `PGAPy-2.2.1/test/test_pgapy.py` & `PGAPy-2.2.2/test/test_pgapy.py`

 * *Files identical despite different names*

