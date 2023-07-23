# Comparing `tmp/laspy-2.4.1.tar.gz` & `tmp/laspy-2.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "laspy-2.4.1.tar", last modified: Mon Feb 20 18:23:01 2023, max compression
+gzip compressed data, was "laspy-2.5.0.tar", last modified: Sun Jul 23 18:51:31 2023, max compression
```

## Comparing `laspy-2.4.1.tar` & `laspy-2.5.0.tar`

### file list

```diff
@@ -1,85 +1,104 @@
-drwxrwxrwx   0        0        0        0 2023-02-20 18:23:01.212901 laspy-2.4.1/
--rw-rw-rw-   0        0        0     1565 2022-12-04 20:40:49.000000 laspy-2.4.1/LICENSE.txt
--rw-rw-rw-   0        0        0       68 2022-12-04 20:40:49.000000 laspy-2.4.1/MANIFEST.in
--rw-rw-rw-   0        0        0     2875 2023-02-20 18:23:01.211902 laspy-2.4.1/PKG-INFO
--rw-rw-rw-   0        0        0     1998 2022-12-04 20:40:49.000000 laspy-2.4.1/README.md
-drwxrwxrwx   0        0        0        0 2023-02-20 18:23:00.813901 laspy-2.4.1/laspy/
--rw-rw-rw-   0        0        0      811 2023-02-20 18:21:35.000000 laspy-2.4.1/laspy/__init__.py
--rw-rw-rw-   0        0        0    10547 2023-02-14 20:46:30.000000 laspy-2.4.1/laspy/compression.py
--rw-rw-rw-   0        0        0    29399 2023-02-14 20:46:30.000000 laspy-2.4.1/laspy/copc.py
--rw-rw-rw-   0        0        0      377 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/errors.py
--rw-rw-rw-   0        0        0     1515 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/extradims.py
--rw-rw-rw-   0        0        0      739 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/file.py
--rw-rw-rw-   0        0        0    33109 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/header.py
--rw-rw-rw-   0        0        0     9812 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/lasappender.py
--rw-rw-rw-   0        0        0    14929 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/lasdata.py
--rw-rw-rw-   0        0        0     1749 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/lasmmap.py
--rw-rw-rw-   0        0        0    18250 2023-01-14 10:56:53.000000 laspy-2.4.1/laspy/lasreader.py
--rw-rw-rw-   0        0        0    12268 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/laswriter.py
--rw-rw-rw-   0        0        0    13001 2023-01-14 10:56:53.000000 laspy-2.4.1/laspy/lib.py
-drwxrwxrwx   0        0        0        0 2023-02-20 18:23:00.876901 laspy-2.4.1/laspy/point/
--rw-rw-rw-   0        0        0       99 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/point/__init__.py
--rw-rw-rw-   0        0        0    24831 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/point/dims.py
--rw-rw-rw-   0        0        0     9293 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/point/format.py
--rw-rw-rw-   0        0        0      481 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/point/packing.py
--rw-rw-rw-   0        0        0    13859 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/point/record.py
--rw-rw-rw-   0        0        0       81 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/typehints.py
--rw-rw-rw-   0        0        0     4559 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/utils.py
-drwxrwxrwx   0        0        0        0 2023-02-20 18:23:00.915901 laspy-2.4.1/laspy/vlrs/
--rw-rw-rw-   0        0        0       78 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/vlrs/__init__.py
--rw-rw-rw-   0        0        0     7654 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/vlrs/geotiff.py
--rw-rw-rw-   0        0        0    22111 2023-01-14 10:21:39.000000 laspy-2.4.1/laspy/vlrs/known.py
--rw-rw-rw-   0        0        0     2272 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/vlrs/vlr.py
--rw-rw-rw-   0        0        0     7293 2022-12-04 20:40:49.000000 laspy-2.4.1/laspy/vlrs/vlrlist.py
-drwxrwxrwx   0        0        0        0 2023-02-20 18:23:00.836903 laspy-2.4.1/laspy.egg-info/
--rw-rw-rw-   0        0        0     2875 2023-02-20 18:23:00.000000 laspy-2.4.1/laspy.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1671 2023-02-20 18:23:00.000000 laspy-2.4.1/laspy.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-02-20 18:23:00.000000 laspy-2.4.1/laspy.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2022-12-11 12:39:51.000000 laspy-2.4.1/laspy.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0      207 2023-02-20 18:23:00.000000 laspy-2.4.1/laspy.egg-info/requires.txt
--rw-rw-rw-   0        0        0        6 2023-02-20 18:23:00.000000 laspy-2.4.1/laspy.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       95 2022-12-04 20:40:49.000000 laspy-2.4.1/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-02-20 18:23:01.212901 laspy-2.4.1/setup.cfg
--rw-rw-rw-   0        0        0     1747 2023-01-14 10:56:53.000000 laspy-2.4.1/setup.py
-drwxrwxrwx   0        0        0        0 2023-02-20 18:23:01.082900 laspy-2.4.1/tests/
--rw-rw-rw-   0        0        0        0 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/__init__.py
--rw-rw-rw-   0        0        0     3920 2023-01-14 10:21:39.000000 laspy-2.4.1/tests/conftest.py
-drwxrwxrwx   0        0        0        0 2023-02-20 18:23:01.208902 laspy-2.4.1/tests/data/
--rw-rw-rw-   0        0        0    32381 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/1_4_w_evlr.las
--rw-rw-rw-   0        0        0     8948 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/1_4_w_evlr.laz
--rw-rw-rw-   0        0        0     4962 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/autzen.las
--rw-rw-rw-   0        0        0     4970 2023-01-14 10:21:39.000000 laspy-2.4.1/tests/data/autzen_geo_proj.las
--rw-rw-rw-   0        0        0   603353 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/autzen_trim.laz
--rw-rw-rw-   0        0        0    29084 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/extra.laz
--rw-rw-rw-   0        0        0    66354 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/extrabytes.las
--rw-rw-rw-   0        0        0    59344 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/plane.laz
--rw-rw-rw-   0        0        0    33684 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/simple.copc.laz
--rw-rw-rw-   0        0        0    36437 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/simple.las
--rw-rw-rw-   0        0        0    18217 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/simple.laz
--rw-rw-rw-   0        0        0    30047 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/simple1_1.las
--rw-rw-rw-   0        0        0    62888 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/simple1_3.las
--rw-rw-rw-   0        0        0   814388 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/simple1_4.las
--rw-rw-rw-   0        0        0    32305 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/test1_4.las
--rw-rw-rw-   0        0        0      511 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/unregistered_extra_bytes.las
--rw-rw-rw-   0        0        0   299359 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/data/vegetation_1_3.las
--rw-rw-rw-   0        0        0     5396 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_append_mode.py
--rw-rw-rw-   0        0        0     3985 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_chunk_read_write.py
--rw-rw-rw-   0        0        0    11882 2023-01-14 10:21:39.000000 laspy-2.4.1/tests/test_common.py
--rw-rw-rw-   0        0        0     1209 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_constants.py
--rw-rw-rw-   0        0        0      883 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_conversion.py
--rw-rw-rw-   0        0        0     5807 2023-01-14 10:56:53.000000 laspy-2.4.1/tests/test_copc.py
--rw-rw-rw-   0        0        0     4876 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_creation.py
--rw-rw-rw-   0        0        0     5163 2023-01-14 10:21:39.000000 laspy-2.4.1/tests/test_crs.py
--rw-rw-rw-   0        0        0    12693 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_extrabytes.py
--rw-rw-rw-   0        0        0     5399 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_field_views.py
--rw-rw-rw-   0        0        0     9464 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_header.py
--rw-rw-rw-   0        0        0      465 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_las_1_1.py
--rw-rw-rw-   0        0        0    26124 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_laspy.py
--rw-rw-rw-   0        0        0      296 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_mmap.py
--rw-rw-rw-   0        0        0     1899 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_modif_1_2.py
--rw-rw-rw-   0        0        0     1596 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_modif_1_4.py
--rw-rw-rw-   0        0        0     2979 2023-01-14 10:56:53.000000 laspy-2.4.1/tests/test_non_seekable.py
--rw-rw-rw-   0        0        0      503 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_point_format.py
--rw-rw-rw-   0        0        0     5907 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_reading_1_2.py
--rw-rw-rw-   0        0        0     7786 2023-01-14 10:56:53.000000 laspy-2.4.1/tests/test_reading_1_4.py
--rw-rw-rw-   0        0        0     2418 2022-12-04 20:40:49.000000 laspy-2.4.1/tests/test_vlrs.py
+drwxr-xr-x   0 thomas    (1000) thomas    (1000)        0 2023-07-23 18:51:31.621985 laspy-2.5.0/
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     1538 2021-12-18 17:55:00.000000 laspy-2.5.0/LICENSE.txt
+-rw-r--r--   0 thomas    (1000) thomas    (1000)       65 2022-06-28 22:25:20.000000 laspy-2.5.0/MANIFEST.in
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     2764 2023-07-23 18:51:31.621985 laspy-2.5.0/PKG-INFO
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     1915 2022-09-04 19:53:14.000000 laspy-2.5.0/README.md
+drwxr-xr-x   0 thomas    (1000) thomas    (1000)        0 2023-07-23 18:51:31.597985 laspy-2.5.0/laspy/
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      811 2023-07-23 17:16:38.000000 laspy-2.5.0/laspy/__init__.py
+drwxr-xr-x   0 thomas    (1000) thomas    (1000)        0 2023-07-23 18:51:31.600985 laspy-2.5.0/laspy/_compression/
+-rw-r--r--   0 thomas    (1000) thomas    (1000)        0 2023-04-17 20:35:19.000000 laspy-2.5.0/laspy/_compression/__init__.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     2427 2023-04-19 21:00:42.000000 laspy-2.5.0/laspy/_compression/backend.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      461 2023-04-17 20:35:19.000000 laspy-2.5.0/laspy/_compression/format.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     4325 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/_compression/laszipbackend.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      932 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/_compression/lazbackend.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     9754 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/_compression/lazrsbackend.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     8272 2023-04-17 20:35:19.000000 laspy-2.5.0/laspy/_compression/selection.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      254 2023-04-17 20:35:19.000000 laspy-2.5.0/laspy/_pointappender.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      613 2023-04-17 20:35:19.000000 laspy-2.5.0/laspy/_pointreader.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      920 2023-04-17 20:35:19.000000 laspy-2.5.0/laspy/_pointwriter.py
+drwxr-xr-x   0 thomas    (1000) thomas    (1000)        0 2023-07-23 18:51:31.600985 laspy-2.5.0/laspy/cli/
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     5749 2023-07-10 08:39:10.000000 laspy-2.5.0/laspy/cli/copc.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      410 2023-07-10 09:37:23.000000 laspy-2.5.0/laspy/cli/main.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      307 2023-04-17 20:35:19.000000 laspy-2.5.0/laspy/compression.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    28560 2023-06-24 07:08:30.000000 laspy-2.5.0/laspy/copc.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      351 2021-12-18 17:55:00.000000 laspy-2.5.0/laspy/errors.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     1449 2021-12-18 17:55:00.000000 laspy-2.5.0/laspy/extradims.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      723 2021-12-18 17:55:00.000000 laspy-2.5.0/laspy/file.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    32940 2023-07-14 10:23:23.000000 laspy-2.5.0/laspy/header.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     4732 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/lasappender.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    14482 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/lasdata.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     1691 2021-12-18 17:55:00.000000 laspy-2.5.0/laspy/lasmmap.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    13509 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/lasreader.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     6877 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/laswriter.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    12984 2023-06-24 05:55:29.000000 laspy-2.5.0/laspy/lib.py
+drwxr-xr-x   0 thomas    (1000) thomas    (1000)        0 2023-07-23 18:51:31.601985 laspy-2.5.0/laspy/point/
+-rw-r--r--   0 thomas    (1000) thomas    (1000)       97 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/point/__init__.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    24032 2023-06-24 07:08:30.000000 laspy-2.5.0/laspy/point/dims.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     9023 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/point/format.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      462 2022-12-04 00:00:55.000000 laspy-2.5.0/laspy/point/packing.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    13472 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/point/record.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)       77 2021-12-18 17:55:00.000000 laspy-2.5.0/laspy/typehints.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     4402 2022-12-04 00:00:55.000000 laspy-2.5.0/laspy/utils.py
+drwxr-xr-x   0 thomas    (1000) thomas    (1000)        0 2023-07-23 18:51:31.602985 laspy-2.5.0/laspy/vlrs/
+-rw-r--r--   0 thomas    (1000) thomas    (1000)       75 2022-05-01 12:07:55.000000 laspy-2.5.0/laspy/vlrs/__init__.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     7403 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/vlrs/geotiff.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    21984 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/vlrs/known.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     2184 2023-04-15 15:38:48.000000 laspy-2.5.0/laspy/vlrs/vlr.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     7077 2023-04-19 20:29:59.000000 laspy-2.5.0/laspy/vlrs/vlrlist.py
+drwxr-xr-x   0 thomas    (1000) thomas    (1000)        0 2023-07-23 18:51:31.598985 laspy-2.5.0/laspy.egg-info/
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     2764 2023-07-23 18:51:31.000000 laspy-2.5.0/laspy.egg-info/PKG-INFO
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     2144 2023-07-23 18:51:31.000000 laspy-2.5.0/laspy.egg-info/SOURCES.txt
+-rw-r--r--   0 thomas    (1000) thomas    (1000)        1 2023-07-23 18:51:31.000000 laspy-2.5.0/laspy.egg-info/dependency_links.txt
+-rw-r--r--   0 thomas    (1000) thomas    (1000)       46 2023-07-23 18:51:31.000000 laspy-2.5.0/laspy.egg-info/entry_points.txt
+-rw-r--r--   0 thomas    (1000) thomas    (1000)        1 2021-12-18 17:55:18.000000 laspy-2.5.0/laspy.egg-info/not-zip-safe
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      246 2023-07-23 18:51:31.000000 laspy-2.5.0/laspy.egg-info/requires.txt
+-rw-r--r--   0 thomas    (1000) thomas    (1000)        6 2023-07-23 18:51:31.000000 laspy-2.5.0/laspy.egg-info/top_level.txt
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      124 2023-04-19 20:29:59.000000 laspy-2.5.0/pyproject.toml
+-rw-r--r--   0 thomas    (1000) thomas    (1000)       38 2023-07-23 18:51:31.622985 laspy-2.5.0/setup.cfg
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     1847 2023-07-10 08:39:10.000000 laspy-2.5.0/setup.py
+drwxr-xr-x   0 thomas    (1000) thomas    (1000)        0 2023-07-23 18:51:31.607985 laspy-2.5.0/tests/
+-rw-r--r--   0 thomas    (1000) thomas    (1000)        0 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/__init__.py
+drwxr-xr-x   0 thomas    (1000) thomas    (1000)        0 2023-07-23 18:51:31.607985 laspy-2.5.0/tests/cli/
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     3062 2023-07-10 09:37:23.000000 laspy-2.5.0/tests/cli/test_info.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     3805 2023-05-08 18:05:24.000000 laspy-2.5.0/tests/conftest.py
+drwxr-xr-x   0 thomas    (1000) thomas    (1000)        0 2023-07-23 18:51:31.620985 laspy-2.5.0/tests/data/
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    32381 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/1_4_w_evlr.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     8948 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/1_4_w_evlr.laz
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     4962 2022-04-24 11:45:17.000000 laspy-2.5.0/tests/data/autzen.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     4970 2023-02-22 10:26:26.000000 laspy-2.5.0/tests/data/autzen_geo_proj.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)   603353 2022-12-04 00:00:55.000000 laspy-2.5.0/tests/data/autzen_trim.laz
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    29084 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/extra.laz
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    66354 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/extrabytes.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)   763642 2023-06-24 07:08:30.000000 laspy-2.5.0/tests/data/file_with_both_wkt_and_geotiff_vlrs.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    59344 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/plane.laz
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    33684 2022-12-04 00:00:55.000000 laspy-2.5.0/tests/data/simple.copc.laz
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    36437 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/simple.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    18217 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/simple.laz
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    30047 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/simple1_1.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    62888 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/simple1_3.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)   814388 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/simple1_4.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    33716 2023-06-24 07:08:30.000000 laspy-2.5.0/tests/data/simple_with_page.copc.laz
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    32305 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/test1_4.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      511 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/unregistered_extra_bytes.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)   299359 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/data/vegetation_1_3.las
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     5237 2023-04-19 20:29:59.000000 laspy-2.5.0/tests/test_append_mode.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     3873 2022-12-04 00:00:55.000000 laspy-2.5.0/tests/test_chunk_read_write.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    12128 2023-07-10 17:05:57.000000 laspy-2.5.0/tests/test_common.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     1171 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/test_constants.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      859 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/test_conversion.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     6005 2023-06-24 07:08:30.000000 laspy-2.5.0/tests/test_copc.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     4696 2023-04-19 20:29:59.000000 laspy-2.5.0/tests/test_creation.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     6255 2023-06-24 07:08:30.000000 laspy-2.5.0/tests/test_crs.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    12315 2023-04-19 20:29:59.000000 laspy-2.5.0/tests/test_extrabytes.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     5197 2023-04-19 20:29:59.000000 laspy-2.5.0/tests/test_field_views.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    10969 2023-07-14 10:23:23.000000 laspy-2.5.0/tests/test_header.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      443 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/test_las_1_1.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)    25434 2022-12-04 00:00:55.000000 laspy-2.5.0/tests/test_laspy.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      284 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/test_mmap.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     1822 2023-04-17 21:23:04.000000 laspy-2.5.0/tests/test_modif_1_2.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     1531 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/test_modif_1_4.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     2891 2023-04-19 20:29:59.000000 laspy-2.5.0/tests/test_non_seekable.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)      486 2021-12-18 17:55:00.000000 laspy-2.5.0/tests/test_point_format.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     5666 2023-04-19 20:29:59.000000 laspy-2.5.0/tests/test_reading_1_2.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     7534 2023-04-19 20:29:59.000000 laspy-2.5.0/tests/test_reading_1_4.py
+-rw-r--r--   0 thomas    (1000) thomas    (1000)     2344 2022-12-04 00:00:55.000000 laspy-2.5.0/tests/test_vlrs.py
```

### Comparing `laspy-2.4.1/LICENSE.txt` & `laspy-2.5.0/LICENSE.txt`

 * *Ordering differences only*

 * *Files 12% similar despite different names*

```diff
@@ -1,28 +1,28 @@
-laspy License
-==============================================================================
-Copyright (c) 2012, Grant Brown, grant.brown73 at gmail.com
-Copyright (c) 2012, Howard Butler, hobu.inc at gmail.com
-Copyright (c) 2020, Thomas Montaigu, thomas.montaigu@laposte.net
-
-All rights reserved.
-
-Redistribution and use in source and binary forms, with or without
-modification, are permitted provided that the following conditions are met:
-
-* Redistributions of source code must retain the above copyright notice, this
-  list of conditions and the following disclaimer.
-* Redistributions in binary form must reproduce the above copyright notice,
-  this list of conditions and the following disclaimer in the documentation
-  and/or other materials provided with the distribution.
-
-THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
-AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
-IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
-DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
-FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
-DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
-SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
-CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
-OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
-OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
+laspy License
+==============================================================================
+Copyright (c) 2012, Grant Brown, grant.brown73 at gmail.com
+Copyright (c) 2012, Howard Butler, hobu.inc at gmail.com
+Copyright (c) 2020, Thomas Montaigu, thomas.montaigu@laposte.net
+
+All rights reserved.
+
+Redistribution and use in source and binary forms, with or without
+modification, are permitted provided that the following conditions are met:
+
+* Redistributions of source code must retain the above copyright notice, this
+  list of conditions and the following disclaimer.
+* Redistributions in binary form must reproduce the above copyright notice,
+  this list of conditions and the following disclaimer in the documentation
+  and/or other materials provided with the distribution.
+
+THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
+AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
+IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
+DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
+FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
+DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
+SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
+CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
+OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
+OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
```

### Comparing `laspy-2.4.1/PKG-INFO` & `laspy-2.5.0/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,111 +1,109 @@
-Metadata-Version: 2.1
-Name: laspy
-Version: 2.4.1
-Summary: Native Python ASPRS LAS read/write library
-Home-page: https://github.com/laspy/laspy
-Author: Grant Brown, Thomas Montaigu
-Author-email: grant.brown73@gmail.com, thomas.montaigu@laposte.net
-License: BSD
-Keywords: gis lidar las
-Platform: UNKNOWN
-Classifier: Development Status :: 5 - Production/Stable
-Classifier: Intended Audience :: Developers
-Classifier: Intended Audience :: Science/Research
-Classifier: License :: OSI Approved :: BSD License
-Classifier: Operating System :: OS Independent
-Classifier: Programming Language :: Python
-Classifier: Topic :: Scientific/Engineering :: GIS
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-Provides-Extra: dev
-Provides-Extra: lazrs
-Provides-Extra: laszip
-Provides-Extra: pyproj
-Provides-Extra: requests
-License-File: LICENSE.txt
-
-# Laspy
-
-Laspy is a python library for reading, modifying and creating LAS LiDAR
-files.
-
-Laspy is compatible with Python  3.7+.
-
-## Features
-
-- LAS support.
-- LAZ support via `lazrs` or `laszip` backend.
-- LAS/LAZ streamed/chunked reading/writting.
-- [COPC] support over files.
-- [COPC] support over https with `requests` package.
-- CRS support via `pyproj` package.
-
-
-[COPC]: https://github.com/copcio/copcio.github.io
-
-
-## Examples
-
-Directly read and write las
-```Python
-import laspy
-
-las = laspy.read('filename.las')
-las.points = las.points[las.classification == 2]
-las.write('ground.laz')
-```
-
-
-Open data to inspect header (opening only reads the header and vlrs)
-
-```Python
-import laspy
-
-with laspy.open('filename.las') as f:
-    print(f"Point format:       {f.header.point_format}")
-    print(f"Number of points:   {f.header.point_count}")
-    print(f"Number of vlrs:     {len(f.header.vlrs)}")
-```
-Use the 'chunked' reading & writing features
-
-```Python
-import laspy
-
-with laspy.open('big.laz') as input_las:
-    with laspy.open('ground.laz', mode="w", header=input_las.header) as ground_las:
-        for points in input_las.chunk_iterator(2_000_000):
-            ground_las.write_points(points[points.classification == 2])
-
-```
-
-Appending points to existing file
-
-```Python
-import laspy
-
-with laspy.open('big.laz') as input_las:
-    with laspy.open('ground.laz', mode="a") as ground_las:
-        for points in input_las.chunk_iterator(2_000_000):
-            ground_las.append_points(points[points.classification == 2])
-```
-
-API Documentation and tutorials are available at
-[ReadTheDocs](https://laspy.readthedocs.io/en/latest/).
-
-## Installation
-
-Laspy can be installed either with `pip`:
-
-```
-pip install laspy # without LAZ support
-# Or
-pip install laspy[laszip] # with LAZ support via LASzip
-# Or
-pip install laspy[lazrs] # with LAZ support via lazrs
-```
-
-## Changelog
-
-See [CHANGELOG.md](CHANGELOG.md)
-
-
+Metadata-Version: 2.1
+Name: laspy
+Version: 2.5.0
+Summary: Native Python ASPRS LAS read/write library
+Home-page: https://github.com/laspy/laspy
+Author: Grant Brown, Thomas Montaigu
+Author-email: grant.brown73@gmail.com, thomas.montaigu@laposte.net
+License: BSD
+Keywords: gis lidar las
+Classifier: Development Status :: 5 - Production/Stable
+Classifier: Intended Audience :: Developers
+Classifier: Intended Audience :: Science/Research
+Classifier: License :: OSI Approved :: BSD License
+Classifier: Operating System :: OS Independent
+Classifier: Programming Language :: Python
+Classifier: Topic :: Scientific/Engineering :: GIS
+Requires-Python: >=3.7
+Description-Content-Type: text/markdown
+Provides-Extra: dev
+Provides-Extra: lazrs
+Provides-Extra: laszip
+Provides-Extra: pyproj
+Provides-Extra: requests
+Provides-Extra: cli
+License-File: LICENSE.txt
+
+# Laspy
+
+Laspy is a python library for reading, modifying and creating LAS LiDAR
+files.
+
+Laspy is compatible with Python  3.7+.
+
+## Features
+
+- LAS support.
+- LAZ support via `lazrs` or `laszip` backend.
+- LAS/LAZ streamed/chunked reading/writting.
+- [COPC] support over files.
+- [COPC] support over https with `requests` package.
+- CRS support via `pyproj` package.
+
+
+[COPC]: https://github.com/copcio/copcio.github.io
+
+
+## Examples
+
+Directly read and write las
+```Python
+import laspy
+
+las = laspy.read('filename.las')
+las.points = las.points[las.classification == 2]
+las.write('ground.laz')
+```
+
+
+Open data to inspect header (opening only reads the header and vlrs)
+
+```Python
+import laspy
+
+with laspy.open('filename.las') as f:
+    print(f"Point format:       {f.header.point_format}")
+    print(f"Number of points:   {f.header.point_count}")
+    print(f"Number of vlrs:     {len(f.header.vlrs)}")
+```
+Use the 'chunked' reading & writing features
+
+```Python
+import laspy
+
+with laspy.open('big.laz') as input_las:
+    with laspy.open('ground.laz', mode="w", header=input_las.header) as ground_las:
+        for points in input_las.chunk_iterator(2_000_000):
+            ground_las.write_points(points[points.classification == 2])
+
+```
+
+Appending points to existing file
+
+```Python
+import laspy
+
+with laspy.open('big.laz') as input_las:
+    with laspy.open('ground.laz', mode="a") as ground_las:
+        for points in input_las.chunk_iterator(2_000_000):
+            ground_las.append_points(points[points.classification == 2])
+```
+
+API Documentation and tutorials are available at
+[ReadTheDocs](https://laspy.readthedocs.io/en/latest/).
+
+## Installation
+
+Laspy can be installed either with `pip`:
+
+```
+pip install laspy # without LAZ support
+# Or
+pip install laspy[laszip] # with LAZ support via LASzip
+# Or
+pip install laspy[lazrs] # with LAZ support via lazrs
+```
+
+## Changelog
+
+See [CHANGELOG.md](CHANGELOG.md)
```

### Comparing `laspy-2.4.1/README.md` & `laspy-2.5.0/README.md`

 * *Ordering differences only*

 * *Files 21% similar despite different names*

```diff
@@ -1,83 +1,83 @@
-# Laspy
-
-Laspy is a python library for reading, modifying and creating LAS LiDAR
-files.
-
-Laspy is compatible with Python  3.7+.
-
-## Features
-
-- LAS support.
-- LAZ support via `lazrs` or `laszip` backend.
-- LAS/LAZ streamed/chunked reading/writting.
-- [COPC] support over files.
-- [COPC] support over https with `requests` package.
-- CRS support via `pyproj` package.
-
-
-[COPC]: https://github.com/copcio/copcio.github.io
-
-
-## Examples
-
-Directly read and write las
-```Python
-import laspy
-
-las = laspy.read('filename.las')
-las.points = las.points[las.classification == 2]
-las.write('ground.laz')
-```
-
-
-Open data to inspect header (opening only reads the header and vlrs)
-
-```Python
-import laspy
-
-with laspy.open('filename.las') as f:
-    print(f"Point format:       {f.header.point_format}")
-    print(f"Number of points:   {f.header.point_count}")
-    print(f"Number of vlrs:     {len(f.header.vlrs)}")
-```
-Use the 'chunked' reading & writing features
-
-```Python
-import laspy
-
-with laspy.open('big.laz') as input_las:
-    with laspy.open('ground.laz', mode="w", header=input_las.header) as ground_las:
-        for points in input_las.chunk_iterator(2_000_000):
-            ground_las.write_points(points[points.classification == 2])
-
-```
-
-Appending points to existing file
-
-```Python
-import laspy
-
-with laspy.open('big.laz') as input_las:
-    with laspy.open('ground.laz', mode="a") as ground_las:
-        for points in input_las.chunk_iterator(2_000_000):
-            ground_las.append_points(points[points.classification == 2])
-```
-
-API Documentation and tutorials are available at
-[ReadTheDocs](https://laspy.readthedocs.io/en/latest/).
-
-## Installation
-
-Laspy can be installed either with `pip`:
-
-```
-pip install laspy # without LAZ support
-# Or
-pip install laspy[laszip] # with LAZ support via LASzip
-# Or
-pip install laspy[lazrs] # with LAZ support via lazrs
-```
-
-## Changelog
-
-See [CHANGELOG.md](CHANGELOG.md)
+# Laspy
+
+Laspy is a python library for reading, modifying and creating LAS LiDAR
+files.
+
+Laspy is compatible with Python  3.7+.
+
+## Features
+
+- LAS support.
+- LAZ support via `lazrs` or `laszip` backend.
+- LAS/LAZ streamed/chunked reading/writting.
+- [COPC] support over files.
+- [COPC] support over https with `requests` package.
+- CRS support via `pyproj` package.
+
+
+[COPC]: https://github.com/copcio/copcio.github.io
+
+
+## Examples
+
+Directly read and write las
+```Python
+import laspy
+
+las = laspy.read('filename.las')
+las.points = las.points[las.classification == 2]
+las.write('ground.laz')
+```
+
+
+Open data to inspect header (opening only reads the header and vlrs)
+
+```Python
+import laspy
+
+with laspy.open('filename.las') as f:
+    print(f"Point format:       {f.header.point_format}")
+    print(f"Number of points:   {f.header.point_count}")
+    print(f"Number of vlrs:     {len(f.header.vlrs)}")
+```
+Use the 'chunked' reading & writing features
+
+```Python
+import laspy
+
+with laspy.open('big.laz') as input_las:
+    with laspy.open('ground.laz', mode="w", header=input_las.header) as ground_las:
+        for points in input_las.chunk_iterator(2_000_000):
+            ground_las.write_points(points[points.classification == 2])
+
+```
+
+Appending points to existing file
+
+```Python
+import laspy
+
+with laspy.open('big.laz') as input_las:
+    with laspy.open('ground.laz', mode="a") as ground_las:
+        for points in input_las.chunk_iterator(2_000_000):
+            ground_las.append_points(points[points.classification == 2])
+```
+
+API Documentation and tutorials are available at
+[ReadTheDocs](https://laspy.readthedocs.io/en/latest/).
+
+## Installation
+
+Laspy can be installed either with `pip`:
+
+```
+pip install laspy # without LAZ support
+# Or
+pip install laspy[laszip] # with LAZ support via LASzip
+# Or
+pip install laspy[lazrs] # with LAZ support via lazrs
+```
+
+## Changelog
+
+See [CHANGELOG.md](CHANGELOG.md)
```

### Comparing `laspy-2.4.1/laspy/__init__.py` & `laspy-2.5.0/laspy/__init__.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,23 +1,23 @@
-__version__ = "2.4.1"
+__version__ = "2.5.0"
 
 import logging
 
-from . import errors, vlrs, file
-from .copc import CopcReader, Bounds
+from . import errors, file, vlrs
+from .copc import Bounds, CopcReader
 from .errors import LaspyException
-from .laswriter import LasWriter
+from .header import LasHeader
+from .lasdata import LasData
 from .lasreader import LasReader
-from .lib import LazBackend, DecompressionSelection, convert
+from .laswriter import LasWriter
+from .lib import DecompressionSelection, LazBackend, convert
 from .lib import create_las as create
 from .lib import mmap_las as mmap
 from .lib import open_las as open
 from .lib import read_las as read
-from .point import PointFormat, ExtraBytesParams, DimensionKind, DimensionInfo
-from .point.record import PackedPointRecord, ScaleAwarePointRecord
+from .point import DimensionInfo, DimensionKind, ExtraBytesParams, PointFormat
 from .point.dims import supported_point_formats, supported_versions
 from .point.format import lost_dimensions
-from .header import LasHeader
-from .lasdata import LasData
+from .point.record import PackedPointRecord, ScaleAwarePointRecord
 from .vlrs import VLR
 
 logging.getLogger(__name__).addHandler(logging.NullHandler())
```

### Comparing `laspy-2.4.1/laspy/compression.py` & `laspy-2.5.0/laspy/_compression/selection.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,298 +1,229 @@
-""" The functions related to the LAZ format (compressed LAS)
-"""
-import enum
-from typing import Tuple
-
-import laspy
-
-
-class LazBackend(enum.Enum):
-    """Supported backends for reading and writing LAS/LAZ"""
-
-    # type_hint = Union[LazBackend, Iterable[LazBackend]]
-
-    LazrsParallel = 0
-    """lazrs in multi-thread mode"""
-    Lazrs = 1
-    """lazrs in single-thread mode"""
-    Laszip = 2
-    """laszip backend"""
-
-    def is_available(self) -> bool:
-        """Returns true if the backend is available"""
-        if self == LazBackend.Lazrs or self == LazBackend.LazrsParallel:
-            try:
-                import lazrs
-            except ModuleNotFoundError:
-                return False
-            else:
-                return True
-        elif self == LazBackend.Laszip:
-            try:
-                import laszip
-            except ModuleNotFoundError:
-                return False
-            else:
-                return True
-        else:
-            return False
-
-    @staticmethod
-    def detect_available() -> Tuple["LazBackend", ...]:
-        """Returns a tuple containing the available backends in the current
-        python environment
-        """
-        available_backends = []
-
-        if LazBackend.LazrsParallel.is_available():
-            available_backends.append(LazBackend.LazrsParallel)
-            available_backends.append(LazBackend.Lazrs)
-
-        if LazBackend.Laszip.is_available():
-            available_backends.append(LazBackend.Laszip)
-
-        return tuple(available_backends)
-
-
-def decompress_and_skip_methods(wrapped_enum):
-    """This decorator is to be applied on an enum.IntFlag class
-
-    It will add to this enum some methods:
-
-    - set(self, flag_name) -> Self => to easily set a flag
-    - unset(self, flag_name) -> Self => to easily unset a flag
-    - is_set(self, flag_name) -> bool => to easily check if a flag is set
-
-
-    If will also add for each flag member (as long as their name is uppercase)
-    the following methods
-
-    - decompress_$flag(self) -> Self
-    - skip_$flag(self) -> Self
-
-
-    # Example
-
-    @load_and_skip_methods
-    class Color(IntFlag):
-        RED = 1
-        GREEN = 2
-        BLUE = 4
-
-
-    will generate (ellipsis to keep it short)
-
-    class Color(IntFlag):
-        RED = 1
-        GREEN = 2
-
-    def _set(self, mask): ...
-
-    def _unset(self, mask): ...
-
-    def is_set(self, mask): ...
-
-
-    def decompress_red(self) -> Color: ...
-    def decompress_red(self) -> Color : ...
-    def is_set_red(self) -> Color : ...
-    def load_green(self) -> Color: ...
-    def skip_green(self) -> Color: ...
-    def is_set_green(self) -> Color : ...
-    """
-
-    def set_method(self, mask) -> wrapped_enum:
-        return self | mask
-
-    def unset_method(self, mask) -> wrapped_enum:
-        return self & (~mask)
-
-    def is_set_method(self, mask) -> bool:
-        return (self & mask) != 0
-
-    setattr(wrapped_enum, "_set", set_method)
-    setattr(wrapped_enum, "_unset", unset_method)
-    setattr(wrapped_enum, "is_set", is_set_method)
-
-    def define_skip_method(mask_member_name: str):
-        def skip_method(self):
-            return self._unset(getattr(self, mask_member_name))
-
-        return skip_method
-
-    def define_decompress_method(mask_member_name: str):
-        def decompress_method(self):
-            return self._set(getattr(self, mask_member_name))
-
-        return decompress_method
-
-    def define_is_set_method(mask_member_name: str):
-        def is_set_method(self):
-            return self.is_set(getattr(self, mask_member_name))
-
-        return is_set_method
-
-    for member in dir(wrapped_enum):
-        if not member.isupper():
-            continue
-
-        load_name = f"decompress_{member.lower()}"
-        skip_name = f"skip_{member.lower()}"
-        is_set_name = f"is_set_{member.lower()}"
-
-        setattr(wrapped_enum, load_name, define_decompress_method(member))
-        setattr(wrapped_enum, skip_name, define_skip_method(member))
-        setattr(wrapped_enum, is_set_name, define_is_set_method(member))
-
-    return wrapped_enum
-
-
-@decompress_and_skip_methods
-class DecompressionSelection(enum.IntFlag):
-    """
-    Holds which fields to decompress  or not.
-
-    Only used for files with version >= 1.4 && point format id >= 6.
-
-    Ignored on other cases.
-
-
-    Each flag in the enum has a corresponding ``decompress_$name`` and
-    ``skip_$name`` methods to easily create a selection.
-
-    >>> import laspy
-    >>> # Creating a selection that decompresses the base + z field
-    >>> selection = laspy.DecompressionSelection.base().decompress_z()
-    >>> selection.is_set(laspy.DecompressionSelection.Z)
-    True
-    >>> selection.is_set(laspy.DecompressionSelection.INTENSITY)
-    False
-
-    >>> # Creating a selection that decompresses all fields but the intensity
-    >>> selection = laspy.DecompressionSelection.all().skip_intensity()
-    >>> selection.is_set(laspy.DecompressionSelection.INTENSITY)
-    False
-    >>> selection.is_set(laspy.DecompressionSelection.Z)
-    True
-
-
-    .. versionadded:: 2.4
-
-    """
-
-    #: Flag to decompress x, y, return number, number of returns and scanner channel
-    XY_RETURNS_CHANNEL = enum.auto()
-    #: Flag to decompress z
-    Z = enum.auto()
-    #: Flag to decompress the classification
-    CLASSIFICATION = enum.auto()
-    #: Flag to decompress the classification flags (withheld, key point, overlap, etc)
-    FLAGS = enum.auto()
-    #: Flag to decompress the intensity
-    INTENSITY = enum.auto()
-    #: Flag to decompress the scan angle
-    SCAN_ANGLE = enum.auto()
-    #: Flag to decompress the user data
-    USER_DATA = enum.auto()
-    #: Flag to decompress the point source id
-    POINT_SOURCE_ID = enum.auto()
-    #: Flag to decompress the gps time
-    GPS_TIME = enum.auto()
-    #: Flag to decompress the red, green, blue
-    RGB = enum.auto()
-    #: Flag to decompress the nir
-    NIR = enum.auto()
-    #: Flag to decompress the wavepacket
-    WAVEPACKET = enum.auto()
-    #: Flag to decompress all the extra bytes
-    ALL_EXTRA_BYTES = enum.auto()
-
-    @classmethod
-    def all(cls) -> "DecompressionSelection":
-        """Returns a selection where all fields will be decompressed"""
-
-        selection = cls.base()
-        for flag in cls:
-            selection = selection._set(flag)
-
-        return selection
-
-    @classmethod
-    def base(cls) -> "DecompressionSelection":
-        """
-        Returns a decompression selection where only the base
-        x, y, return number, number of returns and scanner channel will be decompressed
-        """
-        return cls.xy_returns_channel()
-
-    @classmethod
-    def xy_returns_channel(cls) -> "DecompressionSelection":
-        """
-        Returns a decompression selection where only the base
-        x, y, return number, number of returns and scanner channel will be decompressed
-        """
-        return cls.XY_RETURNS_CHANNEL
-
-    def to_lazrs(self) -> "lazrs.DecompressionSelection":
-        import lazrs
-
-        variant_mapping = {
-            DecompressionSelection.XY_RETURNS_CHANNEL: lazrs.SELECTIVE_DECOMPRESS_XY_RETURNS_CHANNEL,
-            DecompressionSelection.Z: lazrs.SELECTIVE_DECOMPRESS_Z,
-            DecompressionSelection.CLASSIFICATION: lazrs.SELECTIVE_DECOMPRESS_CLASSIFICATION,
-            DecompressionSelection.FLAGS: lazrs.SELECTIVE_DECOMPRESS_FLAGS,
-            DecompressionSelection.INTENSITY: lazrs.SELECTIVE_DECOMPRESS_INTENSITY,
-            DecompressionSelection.SCAN_ANGLE: lazrs.SELECTIVE_DECOMPRESS_SCAN_ANGLE,
-            DecompressionSelection.USER_DATA: lazrs.SELECTIVE_DECOMPRESS_USER_DATA,
-            DecompressionSelection.POINT_SOURCE_ID: lazrs.SELECTIVE_DECOMPRESS_POINT_SOURCE_ID,
-            DecompressionSelection.GPS_TIME: lazrs.SELECTIVE_DECOMPRESS_GPS_TIME,
-            DecompressionSelection.RGB: lazrs.SELECTIVE_DECOMPRESS_RGB,
-            DecompressionSelection.NIR: lazrs.SELECTIVE_DECOMPRESS_NIR,
-            DecompressionSelection.WAVEPACKET: lazrs.SELECTIVE_DECOMPRESS_WAVEPACKET,
-            DecompressionSelection.ALL_EXTRA_BYTES: lazrs.SELECTIVE_DECOMPRESS_ALL_EXTRA_BYTES,
-        }
-        lazrs_selection = lazrs.SELECTIVE_DECOMPRESS_XY_RETURNS_CHANNEL
-        for variant in DecompressionSelection:
-            lazrs_selection |= variant_mapping[variant] if self.is_set(variant) else 0
-
-        return lazrs.DecompressionSelection(lazrs_selection)
-
-    def to_laszip(self) -> int:
-        import laszip
-
-        variant_mapping = {
-            DecompressionSelection.XY_RETURNS_CHANNEL: laszip.DECOMPRESS_SELECTIVE_CHANNEL_RETURNS_XY,
-            DecompressionSelection.Z: laszip.DECOMPRESS_SELECTIVE_Z,
-            DecompressionSelection.CLASSIFICATION: laszip.DECOMPRESS_SELECTIVE_CLASSIFICATION,
-            DecompressionSelection.FLAGS: laszip.DECOMPRESS_SELECTIVE_FLAGS,
-            DecompressionSelection.INTENSITY: laszip.DECOMPRESS_SELECTIVE_INTENSITY,
-            DecompressionSelection.SCAN_ANGLE: laszip.DECOMPRESS_SELECTIVE_SCAN_ANGLE,
-            DecompressionSelection.USER_DATA: laszip.DECOMPRESS_SELECTIVE_USER_DATA,
-            DecompressionSelection.POINT_SOURCE_ID: laszip.DECOMPRESS_SELECTIVE_POINT_SOURCE,
-            DecompressionSelection.GPS_TIME: laszip.DECOMPRESS_SELECTIVE_GPS_TIME,
-            DecompressionSelection.RGB: laszip.DECOMPRESS_SELECTIVE_RGB,
-            DecompressionSelection.NIR: laszip.DECOMPRESS_SELECTIVE_NIR,
-            DecompressionSelection.WAVEPACKET: laszip.DECOMPRESS_SELECTIVE_WAVEPACKET,
-            DecompressionSelection.ALL_EXTRA_BYTES: laszip.DECOMPRESS_SELECTIVE_EXTRA_BYTES,
-        }
-        laszip_selection = laszip.DECOMPRESS_SELECTIVE_CHANNEL_RETURNS_XY
-        for variant in DecompressionSelection:
-            laszip_selection |= variant_mapping[variant] if self.is_set(variant) else 0
-
-        return laszip_selection
-
-
-def is_point_format_compressed(point_format_id: int) -> bool:
-    compression_bit_7 = (point_format_id & 0x80) >> 7
-    compression_bit_6 = (point_format_id & 0x40) >> 6
-    if not compression_bit_6 and compression_bit_7:
-        return True
-    return False
-
-
-def compressed_id_to_uncompressed(point_format_id: int) -> int:
-    return point_format_id & 0x3F
-
-
-def uncompressed_id_to_compressed(point_format_id: int) -> int:
-    return (2**7) | point_format_id
+import enum
+
+
+def decompress_and_skip_methods(wrapped_enum):
+    """This decorator is to be applied on an enum.IntFlag class
+
+    It will add to this enum some methods:
+
+    - set(self, flag_name) -> Self => to easily set a flag
+    - unset(self, flag_name) -> Self => to easily unset a flag
+    - is_set(self, flag_name) -> bool => to easily check if a flag is set
+
+
+    If will also add for each flag member (as long as their name is uppercase)
+    the following methods
+
+    - decompress_$flag(self) -> Self
+    - skip_$flag(self) -> Self
+
+
+    # Example
+
+    @load_and_skip_methods
+    class Color(IntFlag):
+        RED = 1
+        GREEN = 2
+        BLUE = 4
+
+
+    will generate (ellipsis to keep it short)
+
+    class Color(IntFlag):
+        RED = 1
+        GREEN = 2
+
+    def _set(self, mask): ...
+
+    def _unset(self, mask): ...
+
+    def is_set(self, mask): ...
+
+
+    def decompress_red(self) -> Color: ...
+    def decompress_red(self) -> Color : ...
+    def is_set_red(self) -> Color : ...
+    def load_green(self) -> Color: ...
+    def skip_green(self) -> Color: ...
+    def is_set_green(self) -> Color : ...
+    """
+
+    def set_method(self, mask) -> wrapped_enum:
+        return self | mask
+
+    def unset_method(self, mask) -> wrapped_enum:
+        return self & (~mask)
+
+    def is_set_method(self, mask) -> bool:
+        return (self & mask) != 0
+
+    setattr(wrapped_enum, "_set", set_method)
+    setattr(wrapped_enum, "_unset", unset_method)
+    setattr(wrapped_enum, "is_set", is_set_method)
+
+    def define_skip_method(mask_member_name: str):
+        def skip_method(self):
+            return self._unset(getattr(self, mask_member_name))
+
+        return skip_method
+
+    def define_decompress_method(mask_member_name: str):
+        def decompress_method(self):
+            return self._set(getattr(self, mask_member_name))
+
+        return decompress_method
+
+    def define_is_set_method(mask_member_name: str):
+        def is_set_method(self):
+            return self.is_set(getattr(self, mask_member_name))
+
+        return is_set_method
+
+    for member in dir(wrapped_enum):
+        if not member.isupper():
+            continue
+
+        load_name = f"decompress_{member.lower()}"
+        skip_name = f"skip_{member.lower()}"
+        is_set_name = f"is_set_{member.lower()}"
+
+        setattr(wrapped_enum, load_name, define_decompress_method(member))
+        setattr(wrapped_enum, skip_name, define_skip_method(member))
+        setattr(wrapped_enum, is_set_name, define_is_set_method(member))
+
+    return wrapped_enum
+
+
+@decompress_and_skip_methods
+class DecompressionSelection(enum.IntFlag):
+    """
+    Holds which fields to decompress  or not.
+
+    Only used for files with version >= 1.4 && point format id >= 6.
+
+    Ignored on other cases.
+
+
+    Each flag in the enum has a corresponding ``decompress_$name`` and
+    ``skip_$name`` methods to easily create a selection.
+
+    >>> import laspy
+    >>> # Creating a selection that decompresses the base + z field
+    >>> selection = laspy.DecompressionSelection.base().decompress_z()
+    >>> selection.is_set(laspy.DecompressionSelection.Z)
+    True
+    >>> selection.is_set(laspy.DecompressionSelection.INTENSITY)
+    False
+
+    >>> # Creating a selection that decompresses all fields but the intensity
+    >>> selection = laspy.DecompressionSelection.all().skip_intensity()
+    >>> selection.is_set(laspy.DecompressionSelection.INTENSITY)
+    False
+    >>> selection.is_set(laspy.DecompressionSelection.Z)
+    True
+
+
+    .. versionadded:: 2.4
+
+    """
+
+    #: Flag to decompress x, y, return number, number of returns and scanner channel
+    XY_RETURNS_CHANNEL = enum.auto()
+    #: Flag to decompress z
+    Z = enum.auto()
+    #: Flag to decompress the classification
+    CLASSIFICATION = enum.auto()
+    #: Flag to decompress the classification flags (withheld, key point, overlap, etc)
+    FLAGS = enum.auto()
+    #: Flag to decompress the intensity
+    INTENSITY = enum.auto()
+    #: Flag to decompress the scan angle
+    SCAN_ANGLE = enum.auto()
+    #: Flag to decompress the user data
+    USER_DATA = enum.auto()
+    #: Flag to decompress the point source id
+    POINT_SOURCE_ID = enum.auto()
+    #: Flag to decompress the gps time
+    GPS_TIME = enum.auto()
+    #: Flag to decompress the red, green, blue
+    RGB = enum.auto()
+    #: Flag to decompress the nir
+    NIR = enum.auto()
+    #: Flag to decompress the wavepacket
+    WAVEPACKET = enum.auto()
+    #: Flag to decompress all the extra bytes
+    ALL_EXTRA_BYTES = enum.auto()
+
+    @classmethod
+    def all(cls) -> "DecompressionSelection":
+        """Returns a selection where all fields will be decompressed"""
+
+        selection = cls.base()
+        for flag in cls:
+            selection = selection._set(flag)
+
+        return selection
+
+    @classmethod
+    def base(cls) -> "DecompressionSelection":
+        """
+        Returns a decompression selection where only the base
+        x, y, return number, number of returns and scanner channel will be decompressed
+        """
+        return cls.xy_returns_channel()
+
+    @classmethod
+    def xy_returns_channel(cls) -> "DecompressionSelection":
+        """
+        Returns a decompression selection where only the base
+        x, y, return number, number of returns and scanner channel will be decompressed
+        """
+        return cls.XY_RETURNS_CHANNEL
+
+    def to_lazrs(self) -> "lazrs.DecompressionSelection":
+        import lazrs
+
+        variant_mapping = {
+            DecompressionSelection.XY_RETURNS_CHANNEL: lazrs.SELECTIVE_DECOMPRESS_XY_RETURNS_CHANNEL,
+            DecompressionSelection.Z: lazrs.SELECTIVE_DECOMPRESS_Z,
+            DecompressionSelection.CLASSIFICATION: lazrs.SELECTIVE_DECOMPRESS_CLASSIFICATION,
+            DecompressionSelection.FLAGS: lazrs.SELECTIVE_DECOMPRESS_FLAGS,
+            DecompressionSelection.INTENSITY: lazrs.SELECTIVE_DECOMPRESS_INTENSITY,
+            DecompressionSelection.SCAN_ANGLE: lazrs.SELECTIVE_DECOMPRESS_SCAN_ANGLE,
+            DecompressionSelection.USER_DATA: lazrs.SELECTIVE_DECOMPRESS_USER_DATA,
+            DecompressionSelection.POINT_SOURCE_ID: lazrs.SELECTIVE_DECOMPRESS_POINT_SOURCE_ID,
+            DecompressionSelection.GPS_TIME: lazrs.SELECTIVE_DECOMPRESS_GPS_TIME,
+            DecompressionSelection.RGB: lazrs.SELECTIVE_DECOMPRESS_RGB,
+            DecompressionSelection.NIR: lazrs.SELECTIVE_DECOMPRESS_NIR,
+            DecompressionSelection.WAVEPACKET: lazrs.SELECTIVE_DECOMPRESS_WAVEPACKET,
+            DecompressionSelection.ALL_EXTRA_BYTES: lazrs.SELECTIVE_DECOMPRESS_ALL_EXTRA_BYTES,
+        }
+        lazrs_selection = lazrs.SELECTIVE_DECOMPRESS_XY_RETURNS_CHANNEL
+        for variant in DecompressionSelection:
+            lazrs_selection |= variant_mapping[variant] if self.is_set(variant) else 0
+
+        return lazrs.DecompressionSelection(lazrs_selection)
+
+    def to_laszip(self) -> int:
+        import laszip
+
+        variant_mapping = {
+            DecompressionSelection.XY_RETURNS_CHANNEL: laszip.DECOMPRESS_SELECTIVE_CHANNEL_RETURNS_XY,
+            DecompressionSelection.Z: laszip.DECOMPRESS_SELECTIVE_Z,
+            DecompressionSelection.CLASSIFICATION: laszip.DECOMPRESS_SELECTIVE_CLASSIFICATION,
+            DecompressionSelection.FLAGS: laszip.DECOMPRESS_SELECTIVE_FLAGS,
+            DecompressionSelection.INTENSITY: laszip.DECOMPRESS_SELECTIVE_INTENSITY,
+            DecompressionSelection.SCAN_ANGLE: laszip.DECOMPRESS_SELECTIVE_SCAN_ANGLE,
+            DecompressionSelection.USER_DATA: laszip.DECOMPRESS_SELECTIVE_USER_DATA,
+            DecompressionSelection.POINT_SOURCE_ID: laszip.DECOMPRESS_SELECTIVE_POINT_SOURCE,
+            DecompressionSelection.GPS_TIME: laszip.DECOMPRESS_SELECTIVE_GPS_TIME,
+            DecompressionSelection.RGB: laszip.DECOMPRESS_SELECTIVE_RGB,
+            DecompressionSelection.NIR: laszip.DECOMPRESS_SELECTIVE_NIR,
+            DecompressionSelection.WAVEPACKET: laszip.DECOMPRESS_SELECTIVE_WAVEPACKET,
+            DecompressionSelection.ALL_EXTRA_BYTES: laszip.DECOMPRESS_SELECTIVE_EXTRA_BYTES,
+        }
+        laszip_selection = laszip.DECOMPRESS_SELECTIVE_CHANNEL_RETURNS_XY
+        for variant in DecompressionSelection:
+            laszip_selection |= variant_mapping[variant] if self.is_set(variant) else 0
+
+        return laszip_selection
```

### Comparing `laspy-2.4.1/laspy/copc.py` & `laspy-2.5.0/laspy/copc.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,888 +1,890 @@
-import io
-import multiprocessing
-import struct
-from concurrent.futures import ThreadPoolExecutor
-from math import ceil, log2
-from dataclasses import dataclass
-from operator import attrgetter
-from queue import Queue, SimpleQueue
-from threading import Thread
-from typing import List, Union, Dict, Optional, Tuple, Iterator
-
-try:
-    import requests
-except ModuleNotFoundError:
-    requests = None
-else:
-    from requests.adapters import HTTPAdapter
-    from requests.packages.urllib3.util.retry import Retry
-
-
-try:
-    import lazrs
-except ModuleNotFoundError:
-    lazrs = None
-
-import numpy as np
-
-from .errors import LaspyException, LazError
-from .header import LasHeader
-from .point.record import PackedPointRecord, ScaleAwarePointRecord
-from .vlrs.known import BaseKnownVLR
-from .compression import DecompressionSelection
-
-DEFAULT_HTTP_WORKERS_NUM = multiprocessing.cpu_count() * 5
-
-
-def requests_retry_session(
-    retries=3,
-    backoff_factor=0.3,
-    status_forcelist=(500, 502, 504),
-    session=None,
-):
-    session = session or requests.Session()
-    retry = Retry(
-        total=retries,
-        read=retries,
-        connect=retries,
-        backoff_factor=backoff_factor,
-        status_forcelist=status_forcelist,
-    )
-    adapter = HTTPAdapter(max_retries=retry)
-    session.mount("http://", adapter)
-    session.mount("https://", adapter)
-    return session
-
-
-# Multi-Range bytes are a thing, and could be used to query
-# all needed chunks in one request, however it does not seems well supported by servers
-# (eg AWS S3) so we don't try to use it
-#
-# We could try to test if the server support multi range bytes
-# https://docs.python-requests.org/en/latest/user/advanced/#body-content-workflow
-
-
-class HttpRangeStream:
-    """
-    class used to mimic file-object interface for HTTP endpoints.
-
-    This works by using Range-Requests.
-    """
-
-    def __init__(self, url: str) -> None:
-        if requests is None:
-            raise LaspyException(
-                "HTTP support requires the 'requests' package to be installed"
-            )
-        self.url = url
-        self.range_start = 0
-        self.session = requests_retry_session()
-
-    def seek(self, pos, whence=io.SEEK_SET):
-        if whence != io.SEEK_SET:
-            raise RuntimeError("Only SEEK_SET is supported")
-
-        if pos < 0:
-            raise RuntimeError("pos must be >= 0")
-
-        self.range_start = pos
-
-    def read(self, n) -> bytes:
-        if n == 0:
-            return b""
-
-        range_end = self.range_start + n - 1
-        headers = {"Range": f"bytes={self.range_start}-{range_end}"}
-
-        r = self.session.get(self.url, headers=headers)
-
-        r.raise_for_status()
-
-        self.range_start += n
-
-        return r.content
-
-    def tell(self) -> int:
-        return self.range_start
-
-    def close(self):
-        self.session.close()
-
-    def __enter__(self):
-        return self
-
-    def __exit__(self, *args, **kwargs):
-        self.close()
-
-
-class CopcInfoVlr(BaseKnownVLR):
-    def __init__(self):
-        super().__init__()
-
-        # Actual (unscaled) coordinate of the center of the octree
-        self.center = np.zeros(3, dtype=np.float64)
-
-        # Perpendicular distance from the center to any side of the root node.
-        self.halfsize = 0.0
-
-        # Space between points at the root node.
-        # This value is halved at each octree level
-        self.spacing = 0.0
-
-        # Where to find the first hierarchy page in the file
-        self.hierarchy_root_offset = 0
-
-        # The `page_size` of the root page
-        self.hierarchy_root_size = 0
-
-        self.gps_min = 0.0
-        self.gps_max = 0.0
-
-    @staticmethod
-    def official_user_id():
-        return "copc"
-
-    @staticmethod
-    def official_record_ids():
-        return (1,)
-
-    def record_data_bytes(self):
-        raise NotImplementedError("Writing COPC is not supported")
-
-    def parse_record_data(self, record_data_bytes: bytes):
-        stream = io.BytesIO(record_data_bytes)
-        for i in range(3):
-            self.center[i] = struct.unpack("<d", stream.read(8))[0]
-
-        self.halfsize = struct.unpack("<d", stream.read(8))[0]
-        self.spacing = struct.unpack("<d", stream.read(8))[0]
-
-        self.hierarchy_root_offset = struct.unpack("<Q", stream.read(8))[0]
-        self.hierarchy_root_size = struct.unpack("<Q", stream.read(8))[0]
-
-        self.gps_min = struct.unpack("<d", stream.read(8))[0]
-        self.gps_max = struct.unpack("<d", stream.read(8))[0]
-
-
-@dataclass
-class Bounds:
-    mins: np.ndarray
-    maxs: np.ndarray
-
-    def overlaps(self, other: "Bounds") -> bool:
-        return bool(np.all((self.mins <= other.maxs) & (self.maxs >= other.mins)))
-
-    def ensure_3d(self, mins: np.ndarray, maxs: np.ndarray) -> "Bounds":
-        new_mins = np.zeros(3, dtype=np.float64)
-        new_maxs = np.zeros(3, dtype=np.float64)
-
-        new_mins[: len(self.mins)] = self.mins[:]
-        new_mins[len(self.mins) :] = mins[len(self.mins) :]
-        new_maxs[: len(self.maxs)] = self.maxs[:]
-        new_maxs[len(self.maxs) :] = maxs[len(self.maxs) :]
-
-        return Bounds(new_mins, new_maxs)
-
-
-class VoxelKey:
-    """
-    Represents the `VoxelKey` struct of the COPC Specification
-    """
-
-    __slots__ = ["level", "x", "y", "z"]
-    unpacker = struct.Struct("<iiii")
-
-    def __init__(self) -> None:
-        # <0 means invalid
-        self.level = -1
-        self.x = 0
-        self.y = 0
-        self.z = 0
-
-    @classmethod
-    def from_bytes(cls, data: bytes):
-        key = cls()
-        key.level, key.x, key.y, key.z = cls.unpacker.unpack(data)
-        return key
-
-    def child(self, dir: int) -> "VoxelKey":
-        key = VoxelKey()
-        key.level = self.level + 1
-        key.x = (self.x << 1) | (dir & 0x1)
-        key.y = (self.y << 1) | ((dir >> 1) & 0x1)
-        key.z = (self.z << 1) | ((dir >> 2) & 0x1)
-        return key
-
-    def childs(self) -> Iterator["VoxelKey"]:
-        return (self.child(i) for i in range(8))
-
-    def bounds(self, root_bounds: Bounds) -> Bounds:
-        # In an octree every cell is a cube
-        side_size = (root_bounds.maxs[0] - root_bounds.mins[0]) / 2**self.level
-        mins = root_bounds.mins + (np.array([self.x, self.y, self.z]) * side_size)
-        maxs = root_bounds.mins + (
-            np.array([self.x + 1, self.y + 1, self.z + 1]) * side_size
-        )
-
-        return Bounds(mins, maxs)
-
-    def __hash__(self):
-        return hash((self.level, self.x, self.y, self.z))
-
-    def __eq__(self, other: "VoxelKey") -> bool:
-        return (
-            self.level == other.level
-            and self.x == other.x
-            and self.y == other.y
-            and self.z == other.z
-        )
-
-    def __repr__(self) -> str:
-        return f"VoxelKey(level={self.level}, x={self.x}, y={self.y}, z={self.z})"
-
-
-class Entry:
-    """
-    Represents the `Entry` struct of the COPC Specification
-    """
-
-    __slots__ = ("key", "offset", "byte_size", "point_count")
-
-    unpacker = struct.Struct("<Qii")
-
-    def __init__(self) -> None:
-        self.key = VoxelKey()
-        # if point count > 0, offset to LAZ chunk
-        # elif point count == -1, offset to a child hierarchy page
-        # elif point count == 0, 0
-        self.offset = 0
-
-        # if point count > 0, size of the LAZ chunk
-        # elif point count == -1, size of the hierarchy page
-        # elif point count == 0, 0
-        self.byte_size = 0
-
-        # if > 0, number of points in the chunk
-        # if == -1, the info for this entry is in another page (see offset)
-        # 0 no point data exists for this key
-        self.point_count = 0
-
-    @classmethod
-    def from_bytes(cls, data: bytes) -> "Entry":
-        entry = cls()
-
-        key_bytes, rest = data[: VoxelKey.unpacker.size], data[VoxelKey.unpacker.size :]
-        entry.key = VoxelKey.from_bytes(key_bytes)
-        entry.offset, entry.byte_size, entry.point_count = cls.unpacker.unpack(rest)
-
-        return entry
-
-    def __repr__(self) -> str:
-        return f"Entry(key={self.key}, offset={self.offset}, byte_size={self.byte_size}, point_count={self.point_count}"
-
-
-class HierarchyPage:
-    """
-    Represents the `HierarchyPage` struct of the COPC Specification
-    """
-
-    def __init__(self) -> None:
-        self.entries: Dict[VoxelKey, Entry] = {}
-
-    @classmethod
-    def from_bytes(cls, data: bytes) -> "HierarchyPage":
-        page = cls()
-
-        entry_size = Entry.unpacker.size + VoxelKey.unpacker.size
-        num_entries = len(data) // entry_size
-
-        for i in range(num_entries):
-            entry_bytes = data[i * entry_size : (i + 1) * entry_size]
-            entry = Entry.from_bytes(entry_bytes)
-            page.entries[entry.key] = entry
-        return page
-
-
-class CopcHierarchyVlr(BaseKnownVLR):
-    """ "
-    Hierarchy VLR from COPC Specification
-    """
-
-    def __init__(self) -> None:
-        self.data: bytes = b""
-        self.root_page = HierarchyPage()
-
-    @staticmethod
-    def official_user_id():
-        return "copc"
-
-    @staticmethod
-    def official_record_ids():
-        return (1000,)
-
-    def record_data_bytes(self):
-        raise NotImplementedError("Writing COPC is not supported")
-
-    def parse_record_data(self, record_data_bytes: bytes):
-        # We just save the bytes as to parse them we need some
-        # info from the CopcInfoVlr
-        self.bytes = record_data_bytes
-
-
-class OctreeNode:
-    """Our 'custom' type to build an octree from COPC hierarchy page"""
-
-    def __init__(self) -> None:
-        self.key = VoxelKey()
-        # The bounds this node represents, in file's coordinate
-        self.bounds = Bounds(np.zeros(3), np.zeros(3))
-        # Offset to start of corresponding LAZ chunk for this node
-        self.offset = 0
-        # Number of bytes the corresponding LAZ chunk has
-        self.byte_size = 0
-        # Number of LAS points contained in this node
-        self.point_count = 0
-        # Childs of this node, since its an octree, there
-        # are at most 8 childs
-        self.childs: List[OctreeNode] = []
-
-    def remove_child(self, child: "OctreeNode") -> None:
-        idx = self.childs.index(child)
-        del self.childs[idx]
-
-    def __repr__(self) -> str:
-        return f"OctreeNode(key={self.key})"
-
-
-def load_octree_for_query(
-    source,
-    info: CopcInfoVlr,
-    hierarchy_page: HierarchyPage,
-    query_bounds: Optional[Bounds] = None,
-    level_range: Optional[range] = None,
-) -> List[OctreeNode]:
-    """
-    Loads the nodes of the COPC octree from the `source` that
-    satisfies the parameters `query_bounds` and `level_range`.
-
-    It returns the root node of the loaded 'sub-octree'
-    """
-    root_bounds = Bounds(
-        mins=info.center - info.halfsize,
-        maxs=info.center + info.halfsize,
-    )
-
-    root_node = OctreeNode()
-    root_node.key.level = 0
-
-    satisfying_nodes = []
-    nodes_to_load: List[OctreeNode] = [root_node]
-    while nodes_to_load:
-        current_node = nodes_to_load.pop()
-        current_node.bounds = current_node.key.bounds(root_bounds)
-
-        is_in_bounds = query_bounds is None or current_node.bounds.overlaps(
-            query_bounds
-        )
-
-        if not is_in_bounds:
-            continue
-
-        if level_range is not None and current_node.key.level >= level_range.stop:
-            continue
-
-        try:
-            entry = hierarchy_page.entries[current_node.key]
-        except KeyError:
-            continue
-
-        # get the info of the node
-        if entry.point_count == -1:
-            source.seek(entry.offset)
-            page_bytes = source.read(entry.byte_size)
-            page = HierarchyPage.from_bytes(page_bytes)
-            hierarchy_page.entries.update(page.entries)
-            nodes_to_load.insert(0, current_node)
-        elif entry.point_count != 0:
-            current_node.offset = entry.offset
-            current_node.byte_size = entry.byte_size
-            current_node.point_count = entry.point_count
-
-            for child_key in current_node.key.childs():
-                child_node = OctreeNode()
-                child_node.key = child_key
-                current_node.childs.append(child_node)
-                nodes_to_load.append(child_node)
-
-        is_in_level = level_range is None or current_node.key.level in level_range
-        if is_in_level:
-            satisfying_nodes.append(current_node)
-
-    return satisfying_nodes
-
-
-class ChunkIter:
-    """
-    Simple iterator that returns slices to chunks of byte.
-    """
-
-    def __init__(self, buffer: bytearray):
-        self.buffer = memoryview(buffer)
-
-    def next(self, size: int):
-        slc = self.buffer[:size]
-        self.buffer = self.buffer[size:]
-        return slc
-
-
-class HttpFetcherThread(Thread):
-    def __init__(self, url: str, query_queue: Queue, result_queue: SimpleQueue) -> None:
-        super().__init__()
-        self.url = url
-        self.query_queue = query_queue
-        self.result_queue = result_queue
-
-    def run(self) -> None:
-        with HttpRangeStream(self.url) as http_reader:
-            while not self.query_queue.empty():
-                offset, size = self.query_queue.get()
-                try:
-                    http_reader.seek(offset)
-                    data = http_reader.read(size)
-                    self.result_queue.put((data, offset))
-                except Exception as e:
-                    self.result_queue.put(e)
-                finally:
-                    self.query_queue.task_done()
-
-
-def http_queue_strategy(
-    source: HttpRangeStream,
-    byte_queries: List[Tuple[int, int]],
-    out_compressed_bytes: bytearray,
-    num_threads: int,
-) -> None:
-    query_queue = Queue()
-    result_queue = SimpleQueue()
-
-    for query in byte_queries:
-        query_queue.put(query)
-
-    for _ in range(min(len(byte_queries), num_threads)):
-        HttpFetcherThread(source.url, query_queue, result_queue).start()
-
-    query_queue.join()
-
-    results = []
-    while not result_queue.empty():
-        result = result_queue.get()
-        if isinstance(result, Exception):
-            raise result
-        results.append(result)
-    results.sort(key=lambda x: x[1])
-
-    citer = ChunkIter(out_compressed_bytes)
-    for group_bytes, _ in results:
-        cc = citer.next(len(group_bytes))
-        cc[:] = group_bytes
-
-
-def http_thread_executor_strategy(
-    source: HttpRangeStream,
-    byte_queries: List[Tuple[int, int]],
-    out_compressed_bytes: bytearray,
-    num_threads: int,
-) -> None:
-
-    # HTTP queries are more of a bottle neck
-    # so we want to fetch multiple chunks at the same time
-    with ThreadPoolExecutor(max_workers=num_threads) as downloader_pool:
-
-        def fetch_data_job(source, offset, size):
-            source.seek(offset)
-            return source.read(size)
-
-        jobs = []
-        for offset, size in byte_queries:
-            jobs.append(
-                downloader_pool.submit(
-                    fetch_data_job,
-                    HttpRangeStream(source.url),
-                    offset,
-                    size,
-                )
-            )
-
-        # results = [future.result() for future in concurrent.futures.as_completed(jobs)]
-        # results.sort(key=lambda x: x[1])
-        # for group_bytes, _ in results:
-        #     cc = citer.next(len(group_bytes))
-        #     cc[:] = np.frombuffer(group_bytes, np.uint8)
-
-        # We don't use concurrent.futures.as_completed
-        # as we need to keep the order
-        citer = ChunkIter(out_compressed_bytes)
-        for future in jobs:
-            group_bytes = future.result()
-            cc = citer.next(len(group_bytes))
-            cc[:] = group_bytes
-
-
-class CopcReader:
-    """
-    Class allowing to do queries over a `COPC`_ LAZ
-
-    In short, COPC files are LAZ 1.4 files organized in a particular way
-    (Octree) making it possible to do spatial queries
-    as well as queries with a level of details.
-
-    CopcReader **requires** the ``lazrz`` backend to work.
-
-    Optionaly, if ``requests`` is installed, CopcReader can handle
-    Copc files that are on a remote HTTP server
-
-    This class *only* reads COPC files, it does not support normal
-    LAS/LAZ files.
-
-    To create an instance of it you'll likely
-    want to use the :meth:`.CopcReader.open` constructor
-
-
-    .. versionadded:: 2.2
-
-    .. _COPC: https://github.com/copcio/copcio.github.io
-    """
-
-    def __init__(
-        self,
-        stream,
-        close_fd: bool = True,
-        http_num_threads: int = DEFAULT_HTTP_WORKERS_NUM,
-        _http_strategy: str = "queue",
-        decompression_selection: DecompressionSelection = DecompressionSelection.all(),
-    ):
-        """
-        Creates a CopcReader.
-
-        Parameters
-        ---------
-
-        stream: the stream from where data can be read.
-                It must have the following file object methods:
-                read, seek, tell
-
-        http_num_threads: int, optional, default num cpu * 5
-            Number of worker threads to do concurent HTTP requests,
-            ignored when reading non-HTTP file
-
-        close_fd: optional, default bool
-            Whether the stream/file object shall be closed, this only work
-            when using the CopcReader in a with statement.
-
-        decompression_selection: DecompressionSelection,
-            see :func:`laspy.open`
-
-
-
-        .. versionadded:: 2.4
-            The ``decompression_selection`` parameter.
-        """
-        if lazrs is None:
-            raise LazError("COPC support requires the 'lazrs' backend")
-        self.source = stream
-        self.close_fd = close_fd
-        self.http_num_threads = http_num_threads
-        self.http_strategy = _http_strategy
-        self.decompression_selection: lazrs.DecompressionSelection = (
-            decompression_selection.to_lazrs()
-        )
-
-        self.header = LasHeader.read_from(self.source)
-
-        self.copc_info: CopcInfoVlr = self.header.vlrs[0]
-        if not isinstance(self.copc_info, CopcInfoVlr):
-            copc_info_exists = any(
-                isinstance(vlr, CopcInfoVlr) for vlr in self.header.vlrs
-            )
-            if copc_info_exists:
-                raise LaspyException(
-                    "This file is not a valid COPC, "
-                    "it does have a COPC VLR, however it is not the first VLR "
-                    "as it should"
-                )
-            else:
-                raise LaspyException(
-                    "This file is not a valid COPC, " "it does not have a COPC VLR"
-                )
-
-        if self.copc_info.hierarchy_root_offset < self.header.offset_to_point_data:
-            self.hierarchy = self.header.vlrs.extract("CopcHierarchyVlr")[0]
-        else:
-            # TODO maybe we could read the whole EVLR's byte
-            # so we could load the octree without having any more requests to do
-            # since everything would be in memory
-            self.source.seek(self.copc_info.hierarchy_root_offset)
-            # This only contains the record_data_bytes
-            root_hierarchy_vlr_bytes = self.source.read(
-                self.copc_info.hierarchy_root_size
-            )
-            hierarchy = CopcHierarchyVlr()
-            hierarchy.parse_record_data(root_hierarchy_vlr_bytes)
-
-        self.laszip_vlr = self.header.vlrs.pop(self.header.vlrs.index("LasZipVlr"))
-
-        self.source.seek(self.copc_info.hierarchy_root_offset)
-        root_page_bytes = self.source.read(self.copc_info.hierarchy_root_size)
-        # At first the hierary only contains the root page entries
-        # but it will get updated as the queries may need more pages
-        self.root_page = HierarchyPage.from_bytes(root_page_bytes)
-
-    @classmethod
-    def open(
-        cls,
-        uri: str,
-        http_num_threads: int = DEFAULT_HTTP_WORKERS_NUM,
-        _http_strategy: str = "queue",
-        decompression_selection: DecompressionSelection = DecompressionSelection.all(),
-    ) -> "CopcReader":
-        """
-        Opens the COPC file.
-
-
-        Parameters
-        ----------
-        uri: str, uri of the COPC file.
-            Supported uri are:
-
-                - 'local' files accesible with a path.
-                - HTTP / HTTPS endpoints. The pyhon package ``requests`` is
-                  required in order to be able to work with HTTP endpoints.
-
-        http_num_threads: int, optional, default num cpu * 5
-            Number of worker threads to do concurent HTTP requests,
-            ignored when reading non-HTTP file
-
-        decompression_selection: DecompressionSelection,
-            see :func:`laspy.open`
-
-
-        Opening a local file
-
-        .. code-block:: Python
-
-            from laspy import CopcReader
-
-            with CopcReader.open("some_file.laz") as reader:
-                ...
-
-        Opening a file on a remite HTTP server
-        (``requests`` package required)
-
-        .. code-block:: Python
-
-            from laspy import CopcReader
-
-            url = "https://s3.amazonaws.com/hobu-lidar/autzen-classified.copc.laz"
-            with CopcReader.open(url) as reader:
-                ...
-
-
-
-        .. versionadded:: 2.4
-            The ``decompression_selection`` parameter.
-        """
-        uri = str(uri)
-        if uri.startswith("http"):
-            source = HttpRangeStream(uri)
-        else:
-            source = open(uri, mode="rb")
-
-        return cls(
-            source,
-            http_num_threads=http_num_threads,
-            decompression_selection=decompression_selection,
-        )
-
-    def query(
-        self,
-        bounds: Optional[Bounds] = None,
-        resolution: Optional[Union[float, int]] = None,
-        level: Optional[Union[int, range]] = None,
-    ) -> ScaleAwarePointRecord:
-        """ "
-        Query the COPC file to retrieve the points matching the
-        requested bounds and level.
-
-        Parameters
-        ----------
-        bounds: Bounds, optional, default None
-                The bounds for which you wish to aquire points.
-                If None, the whole file's bounds will be considered
-                2D bounds are suported, (No point will be filtered on its Z coordinate)
-
-        resolution: float or int, optional, default None
-                Limits the octree levels to be queried in order to have
-                a point cloud with the requested resolution.
-
-                - The unit is the one of the data.
-
-                - If None, the resulting cloud will be at the
-                  full resolution offered by the COPC source
-
-                - Mutually exclusive with level parameter
-
-        level: int or range, optional, default None
-               The level of detail (LOD).
-
-               - If None, all LOD are going to be considered
-               - If it is an int, only points that are of the requested LOD
-                 will be returned.
-               - If it is a range, points for which the LOD is within the range
-                 will be returned
-        """
-
-        if resolution is not None and level is not None:
-            raise ValueError("Cannot specify both level and resolution")
-        elif resolution is not None and level is None:
-            level_max = max(1, ceil(log2(self.copc_info.spacing / resolution)) + 1)
-            level = range(0, level_max)
-
-        if isinstance(level, int):
-            level = range(level, level + 1)
-
-        if bounds is not None:
-            bounds = bounds.ensure_3d(self.header.mins, self.header.maxs)
-
-        nodes = load_octree_for_query(
-            self.source,
-            self.copc_info,
-            self.root_page,
-            query_bounds=bounds,
-            level_range=level,
-        )
-        # print("num nodes to query:", len(nodes));
-        points = self._fetch_and_decrompress_points_of_nodes(nodes)
-
-        if bounds is not None:
-            MINS = np.round(
-                (bounds.mins - self.header.offsets) / self.header.scales
-            ).astype(np.int32)
-            MAXS = np.round(
-                (bounds.maxs - self.header.offsets) / self.header.scales
-            ).astype(np.int32)
-            x_keep = (MINS[0] <= points.X) & (points.X <= MAXS[0])
-            y_keep = (MINS[1] <= points.Y) & (points.Y <= MAXS[1])
-            z_keep = (MINS[2] <= points.Z) & (points.Z <= MAXS[2])
-
-            # using scaled coordinates
-            # x, y, z = np.array(points.x), np.array(points.y), np.array(points.z)
-            # x_keep = (bounds.mins[0] <= x) & (x <= bounds.maxs[0])
-            # y_keep = (bounds.mins[1] <= y) & (y <= bounds.maxs[1])
-            # z_keep = (bounds.mins[2] <= z) & (z <= bounds.maxs[2])
-
-            keep_mask = x_keep & y_keep & z_keep
-            points.array = points.array[keep_mask].copy()
-        return points
-
-    def spatial_query(self, bounds: Bounds) -> ScaleAwarePointRecord:
-        return self.query(bounds=bounds, level=None)
-
-    def level_query(self, level: Union[int, range]) -> ScaleAwarePointRecord:
-        return self.query(bounds=None, level=level)
-
-    def _fetch_and_decrompress_points_of_nodes(
-        self, nodes_to_read: List[OctreeNode]
-    ) -> ScaleAwarePointRecord:
-        if not nodes_to_read:
-            return ScaleAwarePointRecord.empty(header=self.header)
-
-        # Group together contiguous nodes
-        # so that we minimize the number of
-        # read requests (seek + read) / http requests
-        nodes_to_read = sorted(nodes_to_read, key=attrgetter("offset"))
-        grouped_nodes: List[List[OctreeNode]] = []
-        current_group: List[OctreeNode] = []
-        last_node_end = nodes_to_read[0].offset
-        for node in nodes_to_read:
-            if node.offset == last_node_end:
-                current_group.append(node)
-                last_node_end += node.byte_size
-            else:
-                grouped_nodes.append(current_group)
-                current_group = [node]
-                last_node_end = node.offset + node.byte_size
-        if current_group:
-            grouped_nodes.append(current_group)
-
-        compressed_bytes, num_points, chunk_table = self._fetch_all_chunks(
-            grouped_nodes
-        )
-        points_array = np.zeros(
-            num_points * self.header.point_format.size, dtype=np.uint8
-        )
-
-        lazrs.decompress_points_with_chunk_table(
-            compressed_bytes,
-            self.laszip_vlr.record_data,
-            points_array,
-            chunk_table,
-            self.decompression_selection,
-        )
-        r = PackedPointRecord.from_buffer(points_array, self.header.point_format)
-        points = ScaleAwarePointRecord(
-            r.array, r.point_format, self.header.scales, self.header.offsets
-        )
-
-        return points
-
-    def _fetch_all_chunks(
-        self, grouped_nodes: List[List[OctreeNode]]
-    ) -> Tuple[bytearray, int, List[Tuple[int, int]]]:
-
-        num_points = 0
-        num_compressed_bytes = 0
-        chunk_table: List[Tuple[int, int]] = []
-        byte_queries: List[Tuple[int, int]] = []
-        for group in grouped_nodes:
-            num_compressed_group_bytes = 0
-            for node in group:
-                chunk_table.append((node.point_count, node.byte_size))
-                num_compressed_group_bytes += node.byte_size
-                num_points += node.point_count
-
-            num_compressed_bytes += num_compressed_group_bytes
-            byte_queries.append((group[0].offset, num_compressed_group_bytes))
-
-        compressed_bytes = bytearray(num_compressed_bytes)
-
-        if isinstance(self.source, HttpRangeStream):
-            if self.http_strategy == "queue":
-                http_queue_strategy(
-                    self.source, byte_queries, compressed_bytes, self.http_num_threads
-                )
-            else:
-                http_thread_executor_strategy(
-                    self.source, byte_queries, compressed_bytes, self.http_num_threads
-                )
-
-        elif hasattr(self.source, "readinto"):
-            citer = ChunkIter(compressed_bytes)
-            for offset, size in byte_queries:
-                self.source.seek(offset)
-                cc = citer.next(size)
-                self.source.readinto(cc)
-        else:
-            citer = ChunkIter(compressed_bytes)
-            for offset, size in byte_queries:
-                self.source.seek(offset)
-                cc = citer.next(size)
-                cc[:] = self.source.read(size)
-
-        return compressed_bytes, num_points, chunk_table
-
-    def __enter__(self) -> "CopcReader":
-        return self
-
-    def __exit__(self, _exc_type, _exc_val, _exc_tb) -> None:
-        if self.close_fd:
-            self.source.close()
+import io
+import multiprocessing
+import struct
+from concurrent.futures import ThreadPoolExecutor
+from dataclasses import dataclass
+from math import ceil, log2
+from operator import attrgetter
+from queue import Queue, SimpleQueue
+from threading import Thread
+from typing import Dict, Iterator, List, Optional, Tuple, Union
+
+try:
+    import requests
+except ModuleNotFoundError:
+    requests = None
+else:
+    from requests.adapters import HTTPAdapter
+    from requests.packages.urllib3.util.retry import Retry
+
+
+try:
+    import lazrs
+except ModuleNotFoundError:
+    lazrs = None
+
+import numpy as np
+
+from .compression import DecompressionSelection
+from .errors import LaspyException, LazError
+from .header import LasHeader
+from .point.record import PackedPointRecord, ScaleAwarePointRecord
+from .vlrs.known import BaseKnownVLR
+
+DEFAULT_HTTP_WORKERS_NUM = multiprocessing.cpu_count() * 5
+
+
+def requests_retry_session(
+    retries=3,
+    backoff_factor=0.3,
+    status_forcelist=(500, 502, 504),
+    session=None,
+):
+    session = session or requests.Session()
+    retry = Retry(
+        total=retries,
+        read=retries,
+        connect=retries,
+        backoff_factor=backoff_factor,
+        status_forcelist=status_forcelist,
+    )
+    adapter = HTTPAdapter(max_retries=retry)
+    session.mount("http://", adapter)
+    session.mount("https://", adapter)
+    return session
+
+
+# Multi-Range bytes are a thing, and could be used to query
+# all needed chunks in one request, however it does not seems well supported by servers
+# (eg AWS S3) so we don't try to use it
+#
+# We could try to test if the server support multi range bytes
+# https://docs.python-requests.org/en/latest/user/advanced/#body-content-workflow
+
+
+class HttpRangeStream:
+    """
+    class used to mimic file-object interface for HTTP endpoints.
+
+    This works by using Range-Requests.
+    """
+
+    def __init__(self, url: str) -> None:
+        if requests is None:
+            raise LaspyException(
+                "HTTP support requires the 'requests' package to be installed"
+            )
+        self.url = url
+        self.range_start = 0
+        self.session = requests_retry_session()
+
+    def seek(self, pos, whence=io.SEEK_SET):
+        if whence != io.SEEK_SET:
+            raise RuntimeError("Only SEEK_SET is supported")
+
+        if pos < 0:
+            raise RuntimeError("pos must be >= 0")
+
+        self.range_start = pos
+
+    def read(self, n) -> bytes:
+        if n == 0:
+            return b""
+
+        range_end = self.range_start + n - 1
+        headers = {"Range": f"bytes={self.range_start}-{range_end}"}
+
+        r = self.session.get(self.url, headers=headers)
+
+        r.raise_for_status()
+
+        self.range_start += n
+
+        return r.content
+
+    def tell(self) -> int:
+        return self.range_start
+
+    def close(self):
+        self.session.close()
+
+    def __enter__(self):
+        return self
+
+    def __exit__(self, *args, **kwargs):
+        self.close()
+
+
+class CopcInfoVlr(BaseKnownVLR):
+    def __init__(self):
+        super().__init__()
+
+        # Actual (unscaled) coordinate of the center of the octree
+        self.center = np.zeros(3, dtype=np.float64)
+
+        # Perpendicular distance from the center to any side of the root node.
+        self.halfsize = 0.0
+
+        # Space between points at the root node.
+        # This value is halved at each octree level
+        self.spacing = 0.0
+
+        # Where to find the first hierarchy page in the file
+        self.hierarchy_root_offset = 0
+
+        # The `page_size` of the root page
+        self.hierarchy_root_size = 0
+
+        self.gps_min = 0.0
+        self.gps_max = 0.0
+
+    @staticmethod
+    def official_user_id():
+        return "copc"
+
+    @staticmethod
+    def official_record_ids():
+        return (1,)
+
+    def record_data_bytes(self):
+        raise NotImplementedError("Writing COPC is not supported")
+
+    def parse_record_data(self, record_data_bytes: bytes):
+        stream = io.BytesIO(record_data_bytes)
+        for i in range(3):
+            self.center[i] = struct.unpack("<d", stream.read(8))[0]
+
+        self.halfsize = struct.unpack("<d", stream.read(8))[0]
+        self.spacing = struct.unpack("<d", stream.read(8))[0]
+
+        self.hierarchy_root_offset = struct.unpack("<Q", stream.read(8))[0]
+        self.hierarchy_root_size = struct.unpack("<Q", stream.read(8))[0]
+
+        self.gps_min = struct.unpack("<d", stream.read(8))[0]
+        self.gps_max = struct.unpack("<d", stream.read(8))[0]
+
+
+@dataclass
+class Bounds:
+    mins: np.ndarray
+    maxs: np.ndarray
+
+    def overlaps(self, other: "Bounds") -> bool:
+        return bool(np.all((self.mins <= other.maxs) & (self.maxs >= other.mins)))
+
+    def ensure_3d(self, mins: np.ndarray, maxs: np.ndarray) -> "Bounds":
+        new_mins = np.zeros(3, dtype=np.float64)
+        new_maxs = np.zeros(3, dtype=np.float64)
+
+        new_mins[: len(self.mins)] = self.mins[:]
+        new_mins[len(self.mins) :] = mins[len(self.mins) :]
+        new_maxs[: len(self.maxs)] = self.maxs[:]
+        new_maxs[len(self.maxs) :] = maxs[len(self.maxs) :]
+
+        return Bounds(new_mins, new_maxs)
+
+
+class VoxelKey:
+    """
+    Represents the `VoxelKey` struct of the COPC Specification
+    """
+
+    __slots__ = ["level", "x", "y", "z"]
+    unpacker = struct.Struct("<iiii")
+
+    def __init__(self) -> None:
+        # <0 means invalid
+        self.level = -1
+        self.x = 0
+        self.y = 0
+        self.z = 0
+
+    @classmethod
+    def from_bytes(cls, data: bytes):
+        key = cls()
+        key.level, key.x, key.y, key.z = cls.unpacker.unpack(data)
+        return key
+
+    def child(self, dir: int) -> "VoxelKey":
+        key = VoxelKey()
+        key.level = self.level + 1
+        key.x = (self.x << 1) | (dir & 0x1)
+        key.y = (self.y << 1) | ((dir >> 1) & 0x1)
+        key.z = (self.z << 1) | ((dir >> 2) & 0x1)
+        return key
+
+    def childs(self) -> Iterator["VoxelKey"]:
+        return (self.child(i) for i in range(8))
+
+    def bounds(self, root_bounds: Bounds) -> Bounds:
+        # In an octree every cell is a cube
+        side_size = (root_bounds.maxs[0] - root_bounds.mins[0]) / 2**self.level
+        mins = root_bounds.mins + (np.array([self.x, self.y, self.z]) * side_size)
+        maxs = root_bounds.mins + (
+            np.array([self.x + 1, self.y + 1, self.z + 1]) * side_size
+        )
+
+        return Bounds(mins, maxs)
+
+    def __hash__(self):
+        return hash((self.level, self.x, self.y, self.z))
+
+    def __eq__(self, other: "VoxelKey") -> bool:
+        return (
+            self.level == other.level
+            and self.x == other.x
+            and self.y == other.y
+            and self.z == other.z
+        )
+
+    def __repr__(self) -> str:
+        return f"VoxelKey(level={self.level}, x={self.x}, y={self.y}, z={self.z})"
+
+
+class Entry:
+    """
+    Represents the `Entry` struct of the COPC Specification
+    """
+
+    __slots__ = ("key", "offset", "byte_size", "point_count")
+
+    unpacker = struct.Struct("<Qii")
+
+    def __init__(self) -> None:
+        self.key = VoxelKey()
+        # if point count > 0, offset to LAZ chunk
+        # elif point count == -1, offset to a child hierarchy page
+        # elif point count == 0, 0
+        self.offset = 0
+
+        # if point count > 0, size of the LAZ chunk
+        # elif point count == -1, size of the hierarchy page
+        # elif point count == 0, 0
+        self.byte_size = 0
+
+        # if > 0, number of points in the chunk
+        # if == -1, the info for this entry is in another page (see offset)
+        # 0 no point data exists for this key
+        self.point_count = 0
+
+    @classmethod
+    def from_bytes(cls, data: bytes) -> "Entry":
+        entry = cls()
+
+        key_bytes, rest = data[: VoxelKey.unpacker.size], data[VoxelKey.unpacker.size :]
+        entry.key = VoxelKey.from_bytes(key_bytes)
+        entry.offset, entry.byte_size, entry.point_count = cls.unpacker.unpack(rest)
+
+        return entry
+
+    def __repr__(self) -> str:
+        return f"Entry(key={self.key}, offset={self.offset}, byte_size={self.byte_size}, point_count={self.point_count})"
+
+
+class HierarchyPage:
+    """
+    Represents the `HierarchyPage` struct of the COPC Specification
+    """
+
+    def __init__(self) -> None:
+        self.entries: Dict[VoxelKey, Entry] = {}
+
+    @classmethod
+    def from_bytes(cls, data: bytes) -> "HierarchyPage":
+        page = cls()
+
+        entry_size = Entry.unpacker.size + VoxelKey.unpacker.size
+        num_entries = len(data) // entry_size
+
+        for i in range(num_entries):
+            entry_bytes = data[i * entry_size : (i + 1) * entry_size]
+            entry = Entry.from_bytes(entry_bytes)
+            page.entries[entry.key] = entry
+        return page
+
+
+class CopcHierarchyVlr(BaseKnownVLR):
+    """ "
+    Hierarchy VLR from COPC Specification
+    """
+
+    def __init__(self) -> None:
+        super().__init__()
+        self.data: bytes = b""
+        self.root_page = HierarchyPage()
+
+    @staticmethod
+    def official_user_id():
+        return "copc"
+
+    @staticmethod
+    def official_record_ids():
+        return (1000,)
+
+    def record_data_bytes(self):
+        raise NotImplementedError("Writing COPC is not supported")
+
+    def parse_record_data(self, record_data_bytes: bytes):
+        # We just save the bytes as to parse them we need some
+        # info from the CopcInfoVlr
+        self.bytes = record_data_bytes
+
+
+class OctreeNode:
+    """Our 'custom' type to build an octree from COPC hierarchy page"""
+
+    def __init__(self) -> None:
+        self.key = VoxelKey()
+        # The bounds this node represents, in file's coordinate
+        self.bounds = Bounds(np.zeros(3), np.zeros(3))
+        # Offset to start of corresponding LAZ chunk for this node
+        self.offset = 0
+        # Number of bytes the corresponding LAZ chunk has
+        self.byte_size = 0
+        # Number of LAS points contained in this node
+        self.point_count = 0
+        # Childs of this node, since its an octree, there
+        # are at most 8 childs
+        self.childs: List[OctreeNode] = []
+
+    def remove_child(self, child: "OctreeNode") -> None:
+        idx = self.childs.index(child)
+        del self.childs[idx]
+
+    def __repr__(self) -> str:
+        return f"OctreeNode(key={self.key})"
+
+
+def load_octree_for_query(
+    source,
+    info: CopcInfoVlr,
+    hierarchy_page: HierarchyPage,
+    query_bounds: Optional[Bounds] = None,
+    level_range: Optional[range] = None,
+) -> List[OctreeNode]:
+    """
+    Loads the nodes of the COPC octree from the `source` that
+    satisfies the parameters `query_bounds` and `level_range`.
+
+    It returns the root node of the loaded 'sub-octree'
+    """
+    root_bounds = Bounds(
+        mins=info.center - info.halfsize,
+        maxs=info.center + info.halfsize,
+    )
+
+    root_node = OctreeNode()
+    root_node.key.level = 0
+
+    satisfying_nodes = []
+    nodes_to_load: List[OctreeNode] = [root_node]
+    while nodes_to_load:
+        current_node = nodes_to_load.pop()
+        current_node.bounds = current_node.key.bounds(root_bounds)
+
+        is_in_bounds = query_bounds is None or current_node.bounds.overlaps(
+            query_bounds
+        )
+
+        if not is_in_bounds:
+            continue
+
+        if level_range is not None and current_node.key.level >= level_range.stop:
+            continue
+
+        try:
+            entry = hierarchy_page.entries[current_node.key]
+        except KeyError:
+            continue
+
+        # get the info of the node
+        if entry.point_count == -1:
+            source.seek(entry.offset)
+            page_bytes = source.read(entry.byte_size)
+            page = HierarchyPage.from_bytes(page_bytes)
+            hierarchy_page.entries.update(page.entries)
+            nodes_to_load.insert(0, current_node)
+            continue
+        elif entry.point_count != 0:
+            current_node.offset = entry.offset
+            current_node.byte_size = entry.byte_size
+            current_node.point_count = entry.point_count
+
+            for child_key in current_node.key.childs():
+                child_node = OctreeNode()
+                child_node.key = child_key
+                current_node.childs.append(child_node)
+                nodes_to_load.append(child_node)
+
+        is_in_level = level_range is None or current_node.key.level in level_range
+        if is_in_level:
+            satisfying_nodes.append(current_node)
+
+    return satisfying_nodes
+
+
+class ChunkIter:
+    """
+    Simple iterator that returns slices to chunks of byte.
+    """
+
+    def __init__(self, buffer: bytearray):
+        self.buffer = memoryview(buffer)
+
+    def next(self, size: int):
+        slc = self.buffer[:size]
+        self.buffer = self.buffer[size:]
+        return slc
+
+
+class HttpFetcherThread(Thread):
+    def __init__(self, url: str, query_queue: Queue, result_queue: SimpleQueue) -> None:
+        super().__init__()
+        self.url = url
+        self.query_queue = query_queue
+        self.result_queue = result_queue
+
+    def run(self) -> None:
+        with HttpRangeStream(self.url) as http_reader:
+            while not self.query_queue.empty():
+                offset, size = self.query_queue.get()
+                try:
+                    http_reader.seek(offset)
+                    data = http_reader.read(size)
+                    self.result_queue.put((data, offset))
+                except Exception as e:
+                    self.result_queue.put(e)
+                finally:
+                    self.query_queue.task_done()
+
+
+def http_queue_strategy(
+    source: HttpRangeStream,
+    byte_queries: List[Tuple[int, int]],
+    out_compressed_bytes: bytearray,
+    num_threads: int,
+) -> None:
+    query_queue = Queue()
+    result_queue = SimpleQueue()
+
+    for query in byte_queries:
+        query_queue.put(query)
+
+    for _ in range(min(len(byte_queries), num_threads)):
+        HttpFetcherThread(source.url, query_queue, result_queue).start()
+
+    query_queue.join()
+
+    results = []
+    while not result_queue.empty():
+        result = result_queue.get()
+        if isinstance(result, Exception):
+            raise result
+        results.append(result)
+    results.sort(key=lambda x: x[1])
+
+    citer = ChunkIter(out_compressed_bytes)
+    for group_bytes, _ in results:
+        cc = citer.next(len(group_bytes))
+        cc[:] = group_bytes
+
+
+def http_thread_executor_strategy(
+    source: HttpRangeStream,
+    byte_queries: List[Tuple[int, int]],
+    out_compressed_bytes: bytearray,
+    num_threads: int,
+) -> None:
+
+    # HTTP queries are more of a bottle neck
+    # so we want to fetch multiple chunks at the same time
+    with ThreadPoolExecutor(max_workers=num_threads) as downloader_pool:
+
+        def fetch_data_job(source, offset, size):
+            source.seek(offset)
+            return source.read(size)
+
+        jobs = []
+        for offset, size in byte_queries:
+            jobs.append(
+                downloader_pool.submit(
+                    fetch_data_job,
+                    HttpRangeStream(source.url),
+                    offset,
+                    size,
+                )
+            )
+
+        # results = [future.result() for future in concurrent.futures.as_completed(jobs)]
+        # results.sort(key=lambda x: x[1])
+        # for group_bytes, _ in results:
+        #     cc = citer.next(len(group_bytes))
+        #     cc[:] = np.frombuffer(group_bytes, np.uint8)
+
+        # We don't use concurrent.futures.as_completed
+        # as we need to keep the order
+        citer = ChunkIter(out_compressed_bytes)
+        for future in jobs:
+            group_bytes = future.result()
+            cc = citer.next(len(group_bytes))
+            cc[:] = group_bytes
+
+
+class CopcReader:
+    """
+    Class allowing to do queries over a `COPC`_ LAZ
+
+    In short, COPC files are LAZ 1.4 files organized in a particular way
+    (Octree) making it possible to do spatial queries
+    as well as queries with a level of details.
+
+    CopcReader **requires** the ``lazrz`` backend to work.
+
+    Optionaly, if ``requests`` is installed, CopcReader can handle
+    Copc files that are on a remote HTTP server
+
+    This class *only* reads COPC files, it does not support normal
+    LAS/LAZ files.
+
+    To create an instance of it you'll likely
+    want to use the :meth:`.CopcReader.open` constructor
+
+
+    .. versionadded:: 2.2
+
+    .. _COPC: https://github.com/copcio/copcio.github.io
+    """
+
+    def __init__(
+        self,
+        stream,
+        close_fd: bool = True,
+        http_num_threads: int = DEFAULT_HTTP_WORKERS_NUM,
+        _http_strategy: str = "queue",
+        decompression_selection: DecompressionSelection = DecompressionSelection.all(),
+    ):
+        """
+        Creates a CopcReader.
+
+        Parameters
+        ---------
+
+        stream: the stream from where data can be read.
+                It must have the following file object methods:
+                read, seek, tell
+
+        http_num_threads: int, optional, default num cpu * 5
+            Number of worker threads to do concurent HTTP requests,
+            ignored when reading non-HTTP file
+
+        close_fd: optional, default bool
+            Whether the stream/file object shall be closed, this only work
+            when using the CopcReader in a with statement.
+
+        decompression_selection: DecompressionSelection,
+            see :func:`laspy.open`
+
+
+
+        .. versionadded:: 2.4
+            The ``decompression_selection`` parameter.
+        """
+        if lazrs is None:
+            raise LazError("COPC support requires the 'lazrs' backend")
+        self.source = stream
+        self.close_fd = close_fd
+        self.http_num_threads = http_num_threads
+        self.http_strategy = _http_strategy
+        self.decompression_selection: lazrs.DecompressionSelection = (
+            decompression_selection.to_lazrs()
+        )
+
+        self.header = LasHeader.read_from(self.source)
+
+        self.copc_info: CopcInfoVlr = self.header.vlrs[0]
+        if not isinstance(self.copc_info, CopcInfoVlr):
+            copc_info_exists = any(
+                isinstance(vlr, CopcInfoVlr) for vlr in self.header.vlrs
+            )
+            if copc_info_exists:
+                raise LaspyException(
+                    "This file is not a valid COPC, "
+                    "it does have a COPC VLR, however it is not the first VLR "
+                    "as it should"
+                )
+            else:
+                raise LaspyException(
+                    "This file is not a valid COPC, " "it does not have a COPC VLR"
+                )
+
+        if self.copc_info.hierarchy_root_offset < self.header.offset_to_point_data:
+            self.hierarchy = self.header.vlrs.extract("CopcHierarchyVlr")[0]
+        else:
+            # TODO maybe we could read the whole EVLR's byte
+            # so we could load the octree without having any more requests to do
+            # since everything would be in memory
+            self.source.seek(self.copc_info.hierarchy_root_offset)
+            # This only contains the record_data_bytes
+            root_hierarchy_vlr_bytes = self.source.read(
+                self.copc_info.hierarchy_root_size
+            )
+            hierarchy = CopcHierarchyVlr()
+            hierarchy.parse_record_data(root_hierarchy_vlr_bytes)
+
+        self.laszip_vlr = self.header.vlrs.pop(self.header.vlrs.index("LasZipVlr"))
+
+        self.source.seek(self.copc_info.hierarchy_root_offset)
+        root_page_bytes = self.source.read(self.copc_info.hierarchy_root_size)
+        # At first the hierary only contains the root page entries
+        # but it will get updated as the queries may need more pages
+        self.root_page = HierarchyPage.from_bytes(root_page_bytes)
+
+    @classmethod
+    def open(
+        cls,
+        uri: str,
+        http_num_threads: int = DEFAULT_HTTP_WORKERS_NUM,
+        _http_strategy: str = "queue",
+        decompression_selection: DecompressionSelection = DecompressionSelection.all(),
+    ) -> "CopcReader":
+        """
+        Opens the COPC file.
+
+
+        Parameters
+        ----------
+        uri: str, uri of the COPC file.
+            Supported uri are:
+
+                - 'local' files accesible with a path.
+                - HTTP / HTTPS endpoints. The pyhon package ``requests`` is
+                  required in order to be able to work with HTTP endpoints.
+
+        http_num_threads: int, optional, default num cpu * 5
+            Number of worker threads to do concurent HTTP requests,
+            ignored when reading non-HTTP file
+
+        decompression_selection: DecompressionSelection,
+            see :func:`laspy.open`
+
+
+        Opening a local file
+
+        .. code-block:: Python
+
+            from laspy import CopcReader
+
+            with CopcReader.open("some_file.laz") as reader:
+                ...
+
+        Opening a file on a remite HTTP server
+        (``requests`` package required)
+
+        .. code-block:: Python
+
+            from laspy import CopcReader
+
+            url = "https://s3.amazonaws.com/hobu-lidar/autzen-classified.copc.laz"
+            with CopcReader.open(url) as reader:
+                ...
+
+
+
+        .. versionadded:: 2.4
+            The ``decompression_selection`` parameter.
+        """
+        uri = str(uri)
+        if uri.startswith("http"):
+            source = HttpRangeStream(uri)
+        else:
+            source = open(uri, mode="rb")
+
+        return cls(
+            source,
+            http_num_threads=http_num_threads,
+            decompression_selection=decompression_selection,
+        )
+
+    def query(
+        self,
+        bounds: Optional[Bounds] = None,
+        resolution: Optional[Union[float, int]] = None,
+        level: Optional[Union[int, range]] = None,
+    ) -> ScaleAwarePointRecord:
+        """ "
+        Query the COPC file to retrieve the points matching the
+        requested bounds and level.
+
+        Parameters
+        ----------
+        bounds: Bounds, optional, default None
+                The bounds for which you wish to aquire points.
+                If None, the whole file's bounds will be considered
+                2D bounds are suported, (No point will be filtered on its Z coordinate)
+
+        resolution: float or int, optional, default None
+                Limits the octree levels to be queried in order to have
+                a point cloud with the requested resolution.
+
+                - The unit is the one of the data.
+
+                - If None, the resulting cloud will be at the
+                  full resolution offered by the COPC source
+
+                - Mutually exclusive with level parameter
+
+        level: int or range, optional, default None
+               The level of detail (LOD).
+
+               - If None, all LOD are going to be considered
+               - If it is an int, only points that are of the requested LOD
+                 will be returned.
+               - If it is a range, points for which the LOD is within the range
+                 will be returned
+        """
+
+        if resolution is not None and level is not None:
+            raise ValueError("Cannot specify both level and resolution")
+        elif resolution is not None and level is None:
+            level_max = max(1, ceil(log2(self.copc_info.spacing / resolution)) + 1)
+            level = range(0, level_max)
+
+        if isinstance(level, int):
+            level = range(level, level + 1)
+
+        if bounds is not None:
+            bounds = bounds.ensure_3d(self.header.mins, self.header.maxs)
+
+        nodes = load_octree_for_query(
+            self.source,
+            self.copc_info,
+            self.root_page,
+            query_bounds=bounds,
+            level_range=level,
+        )
+        # print("num nodes to query:", len(nodes));
+        points = self._fetch_and_decrompress_points_of_nodes(nodes)
+
+        if bounds is not None:
+            MINS = np.round(
+                (bounds.mins - self.header.offsets) / self.header.scales
+            ).astype(np.int32)
+            MAXS = np.round(
+                (bounds.maxs - self.header.offsets) / self.header.scales
+            ).astype(np.int32)
+            x_keep = (MINS[0] <= points.X) & (points.X <= MAXS[0])
+            y_keep = (MINS[1] <= points.Y) & (points.Y <= MAXS[1])
+            z_keep = (MINS[2] <= points.Z) & (points.Z <= MAXS[2])
+
+            # using scaled coordinates
+            # x, y, z = np.array(points.x), np.array(points.y), np.array(points.z)
+            # x_keep = (bounds.mins[0] <= x) & (x <= bounds.maxs[0])
+            # y_keep = (bounds.mins[1] <= y) & (y <= bounds.maxs[1])
+            # z_keep = (bounds.mins[2] <= z) & (z <= bounds.maxs[2])
+
+            keep_mask = x_keep & y_keep & z_keep
+            points.array = points.array[keep_mask].copy()
+        return points
+
+    def spatial_query(self, bounds: Bounds) -> ScaleAwarePointRecord:
+        return self.query(bounds=bounds, level=None)
+
+    def level_query(self, level: Union[int, range]) -> ScaleAwarePointRecord:
+        return self.query(bounds=None, level=level)
+
+    def _fetch_and_decrompress_points_of_nodes(
+        self, nodes_to_read: List[OctreeNode]
+    ) -> ScaleAwarePointRecord:
+        if not nodes_to_read:
+            return ScaleAwarePointRecord.empty(header=self.header)
+
+        # Group together contiguous nodes
+        # so that we minimize the number of
+        # read requests (seek + read) / http requests
+        nodes_to_read = sorted(nodes_to_read, key=attrgetter("offset"))
+        grouped_nodes: List[List[OctreeNode]] = []
+        current_group: List[OctreeNode] = []
+        last_node_end = nodes_to_read[0].offset
+        for node in nodes_to_read:
+            if node.offset == last_node_end:
+                current_group.append(node)
+                last_node_end += node.byte_size
+            else:
+                grouped_nodes.append(current_group)
+                current_group = [node]
+                last_node_end = node.offset + node.byte_size
+        if current_group:
+            grouped_nodes.append(current_group)
+
+        compressed_bytes, num_points, chunk_table = self._fetch_all_chunks(
+            grouped_nodes
+        )
+        points_array = np.zeros(
+            num_points * self.header.point_format.size, dtype=np.uint8
+        )
+
+        lazrs.decompress_points_with_chunk_table(
+            compressed_bytes,
+            self.laszip_vlr.record_data,
+            points_array,
+            chunk_table,
+            self.decompression_selection,
+        )
+        r = PackedPointRecord.from_buffer(points_array, self.header.point_format)
+        points = ScaleAwarePointRecord(
+            r.array, r.point_format, self.header.scales, self.header.offsets
+        )
+
+        return points
+
+    def _fetch_all_chunks(
+        self, grouped_nodes: List[List[OctreeNode]]
+    ) -> Tuple[bytearray, int, List[Tuple[int, int]]]:
+
+        num_points = 0
+        num_compressed_bytes = 0
+        chunk_table: List[Tuple[int, int]] = []
+        byte_queries: List[Tuple[int, int]] = []
+        for group in grouped_nodes:
+            num_compressed_group_bytes = 0
+            for node in group:
+                chunk_table.append((node.point_count, node.byte_size))
+                num_compressed_group_bytes += node.byte_size
+                num_points += node.point_count
+
+            num_compressed_bytes += num_compressed_group_bytes
+            byte_queries.append((group[0].offset, num_compressed_group_bytes))
+
+        compressed_bytes = bytearray(num_compressed_bytes)
+
+        if isinstance(self.source, HttpRangeStream):
+            if self.http_strategy == "queue":
+                http_queue_strategy(
+                    self.source, byte_queries, compressed_bytes, self.http_num_threads
+                )
+            else:
+                http_thread_executor_strategy(
+                    self.source, byte_queries, compressed_bytes, self.http_num_threads
+                )
+
+        elif hasattr(self.source, "readinto"):
+            citer = ChunkIter(compressed_bytes)
+            for offset, size in byte_queries:
+                self.source.seek(offset)
+                cc = citer.next(size)
+                self.source.readinto(cc)
+        else:
+            citer = ChunkIter(compressed_bytes)
+            for offset, size in byte_queries:
+                self.source.seek(offset)
+                cc = citer.next(size)
+                cc[:] = self.source.read(size)
+
+        return compressed_bytes, num_points, chunk_table
+
+    def __enter__(self) -> "CopcReader":
+        return self
+
+    def __exit__(self, _exc_type, _exc_val, _exc_tb) -> None:
+        if self.close_fd:
+            self.source.close()
```

### Comparing `laspy-2.4.1/laspy/file.py` & `laspy-2.5.0/laspy/file.py`

 * *Ordering differences only*

 * *Files 27% similar despite different names*

```diff
@@ -1,16 +1,16 @@
-from . import errors
-
-
-class File:
-    def __init__(self, *args, **kwargs) -> None:
-        raise errors.LaspyException(
-            """You are using laspy 2.0, which has several improvements over 1.x
-            but with several breaking changes.
-            To stay on laspy 1.x: `pip install laspy<2.0.0`
-            
-            In short:
-              - To read a file do: las = laspy.read('somefile.laz')
-              - To create a new LAS data do: las = laspy.create(point_format=2, file_version='1.2')
-              - To write a file previously read or created: las.write('somepath.las')
-            See the documentation for more information about the changes https://laspy.readthedocs.io/en/latest/"""
-        )
+from . import errors
+
+
+class File:
+    def __init__(self, *args, **kwargs) -> None:
+        raise errors.LaspyException(
+            """You are using laspy 2.0, which has several improvements over 1.x
+            but with several breaking changes.
+            To stay on laspy 1.x: `pip install laspy<2.0.0`
+            
+            In short:
+              - To read a file do: las = laspy.read('somefile.laz')
+              - To create a new LAS data do: las = laspy.create(point_format=2, file_version='1.2')
+              - To write a file previously read or created: las.write('somepath.las')
+            See the documentation for more information about the changes https://laspy.readthedocs.io/en/latest/"""
+        )
```

### Comparing `laspy-2.4.1/laspy/lasdata.py` & `laspy-2.5.0/laspy/lasdata.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,447 +1,447 @@
-import logging
-import pathlib
-import typing
-from copy import deepcopy
-from typing import Union, Optional, List, Sequence, overload, BinaryIO, Iterable
-
-import numpy as np
-
-from . import errors
-from .compression import LazBackend
-from .header import LasHeader
-from .laswriter import LasWriter
-from .point import record, dims, ExtraBytesParams, PointFormat
-from .point.dims import ScaledArrayView, SubFieldView, OLD_LASPY_NAMES
-from .point.record import DimensionNameValidity
-from .vlrs.vlrlist import VLRList
-
-logger = logging.getLogger(__name__)
-
-
-class LasData:
-    """Class synchronizing all the moving parts of LAS files.
-
-    It connects the point record, header, vlrs together.
-
-    To access points dimensions using this class you have two possibilities
-
-    .. code:: python
-
-        las = laspy.read('some_file.las')
-        las.classification
-        # or
-        las['classification']
-    """
-
-    def __init__(
-        self,
-        header: LasHeader,
-        points: Optional[
-            Union[record.PackedPointRecord, record.ScaleAwarePointRecord]
-        ] = None,
-    ) -> None:
-        if points is None:
-            points = record.ScaleAwarePointRecord.zeros(
-                header.point_count, header=header
-            )
-        if points.point_format != header.point_format:
-            raise errors.LaspyException("Incompatible Point Formats")
-        if isinstance(points, record.PackedPointRecord):
-            points = record.ScaleAwarePointRecord(
-                points.array,
-                header.point_format,
-                scales=header.scales,
-                offsets=header.offsets,
-            )
-        else:
-            assert np.all(header.scales, points.scales)
-            assert np.all(header.offsets, points.offsets)
-        self.__dict__["_points"] = points
-        self.points: record.ScaleAwarePointRecord
-        self.header: LasHeader = header
-
-    @property
-    def point_format(self) -> PointFormat:
-        """Shortcut to get the point format"""
-        return self.points.point_format
-
-    @property
-    def xyz(self) -> np.ndarray:
-        """Returns a **new** 2D numpy array with the x,y,z coordinates
-
-        >>> import laspy
-        >>> las = laspy.read("tests/data/simple.las")
-        >>> xyz = las.xyz
-        >>> xyz.ndim
-        2
-        >>> xyz.shape
-        (1065, 3)
-        >>> np.all(xyz[..., 0] == las.x)
-        True
-        """
-        return np.vstack((self.x, self.y, self.z)).transpose()
-
-    @xyz.setter
-    def xyz(self, value) -> None:
-        self.points[("x", "y", "z")] = value
-
-    @property
-    def points(self) -> record.PackedPointRecord:
-        """Returns the point record"""
-        return self._points
-
-    @points.setter
-    def points(self, new_points: record.PackedPointRecord) -> None:
-        if new_points.point_format != self.point_format:
-            raise errors.IncompatibleDataFormat(
-                "Cannot set points with a different point format, convert first"
-            )
-        self._points = new_points
-        self.update_header()
-        # make sure both point format point to the same object
-        self._points.point_format = self.header.point_format
-
-    @property
-    def vlrs(self) -> VLRList:
-        return self.header.vlrs
-
-    @vlrs.setter
-    def vlrs(self, vlrs) -> None:
-        self.header.vlrs = vlrs
-
-    @property
-    def evlrs(self) -> Optional[VLRList]:
-        return self.header.evlrs
-
-    @evlrs.setter
-    def evlrs(self, evlrs: VLRList) -> None:
-        self.header.evlrs = evlrs
-
-    def add_extra_dim(self, params: ExtraBytesParams) -> None:
-        """Adds a new extra dimension to the point record
-
-        .. note::
-
-            If you plan on adding multiple extra dimensions,
-            prefer :meth:`.add_extra_dims` as it will
-            save re-allocations and data copy
-
-        Parameters
-        ----------
-        params : ExtraBytesParams
-            parameters of the new extra dimension to add
-
-        """
-        self.add_extra_dims([params])
-
-    def add_extra_dims(self, params: List[ExtraBytesParams]) -> None:
-        """Add multiple extra dimensions at once
-
-        Parameters
-        ----------
-
-        params: list of parameters of the new extra dimensions to add
-        """
-        self.header.add_extra_dims(params)
-        new_point_record = record.ScaleAwarePointRecord.zeros(
-            len(self.points), header=self.header
-        )
-        new_point_record.copy_fields_from(self.points)
-        self.points = new_point_record
-
-    def remove_extra_dims(self, names: Iterable[str]) -> None:
-        """Remove multiple extra dimensions from this object
-
-        Parameters
-        ----------
-
-        names: iterable,
-            names of the extra dimensions to be removed
-
-
-        Raises
-        ------
-
-        LaspyException: if you try to remove an extra dimension that do not exist.
-
-        """
-        extra_dimension_names = list(self.point_format.extra_dimension_names)
-        not_extra_dimension = [
-            name for name in names if name not in extra_dimension_names
-        ]
-        if not_extra_dimension:
-            raise errors.LaspyException(
-                f"'{not_extra_dimension}' are not extra dimensions and cannot be removed"
-            )
-
-        self.header.remove_extra_dims(names)
-        new_point_record = record.ScaleAwarePointRecord.zeros(
-            len(self.points), header=self.header
-        )
-        new_point_record.copy_fields_from(self.points)
-        self.points = new_point_record
-
-    def remove_extra_dim(self, name: str) -> None:
-        """Remove an extra dimensions from this object
-
-        .. note::
-
-             If you plan on removing multiple extra dimensions,
-             prefer :meth:`.remove_extra_dims` as it will
-             save re-allocations and data copy
-
-        Parameters
-        ----------
-
-        name: str,
-            name of the extra dimension to be removed
-
-
-        Raises
-        ------
-
-        LaspyException: if you try to remove an extra dimension that do not exist.
-
-        """
-        self.remove_extra_dims([name])
-
-    def update_header(self) -> None:
-        """Update the information stored in the header
-        to be in sync with the actual data.
-
-        This method is called automatically when you save a file using
-        :meth:`laspy.lasdatas.base.LasBase.write`
-        """
-        self.header.update(self.points)
-        self.header.point_format_id = self.points.point_format.id
-        self.header.point_data_record_length = self.points.point_size
-
-        if self.header.version.minor >= 4:
-            if self.evlrs is not None:
-                self.header.number_of_evlrs = len(self.evlrs)
-            self.header.start_of_waveform_data_packet_record = 0
-            # TODO
-            # if len(self.vlrs.get("WktCoordinateSystemVlr")) == 1:
-            #     self.header.global_encoding.wkt = 1
-        else:
-            self.header.number_of_evlrs = 0
-
-    @overload
-    def write(
-        self,
-        destination: str,
-        laz_backend: Optional[Union[LazBackend, Sequence[LazBackend]]] = ...,
-    ) -> None:
-        ...
-
-    @overload
-    def write(
-        self,
-        destination: BinaryIO,
-        do_compress: Optional[bool] = ...,
-        laz_backend: Optional[Union[LazBackend, Sequence[LazBackend]]] = ...,
-    ) -> None:
-        ...
-
-    def write(self, destination, do_compress=None, laz_backend=None):
-        """Writes to a stream or file
-
-        .. note::
-
-            When destination is a string, it will be interpreted as the path were the file should be written to,
-            and whether the file will be compressed depends on the extension used (case insensitive):
-
-                - .laz -> compressed
-                - .las -> uncompressed
-
-            And the do_compress option will be ignored
-
-
-        Parameters
-        ----------
-        destination: str or file object
-            filename or stream to write to
-        do_compress: bool, optional
-            Flags to indicate if you want to compress the data
-        laz_backend: optional, the laz backend to use
-            By default, laspy detect available backends
-        """
-        if isinstance(destination, (str, pathlib.Path)):
-            do_compress = pathlib.Path(destination).suffix.lower() == ".laz"
-
-            with open(destination, mode="wb+") as out:
-                self._write_to(out, do_compress=do_compress, laz_backend=laz_backend)
-        else:
-            self._write_to(
-                destination, do_compress=do_compress, laz_backend=laz_backend
-            )
-
-    def _write_to(
-        self,
-        out_stream: BinaryIO,
-        do_compress: Optional[bool] = None,
-        laz_backend: Optional[Union[LazBackend, Sequence[LazBackend]]] = None,
-    ) -> None:
-        with LasWriter(
-            out_stream,
-            self.header,
-            do_compress=do_compress,
-            closefd=False,
-            laz_backend=laz_backend,
-        ) as writer:
-            writer.write_points(self.points)
-            if self.header.version.minor >= 4 and self.evlrs is not None:
-                writer.write_evlrs(self.evlrs)
-
-    def change_scaling(self, scales=None, offsets=None) -> None:
-        """This changes the scales and/or offset used for the x,y,z
-        dimensions.
-
-        It recomputes the internal, non-scaled X,Y,Z dimensions
-        to match the new scales and offsets.
-
-        It also updates the header with the new values of scales and offsets.
-
-        Parameters
-        ----------
-        scales: optional
-                New scales to be used. If not provided, the scales won't change.
-        offsets: optional
-                 New offsets to be used. If not provided, the offsets won't change.
-
-        Example
-        -------
-
-        >>> import laspy
-        >>> header = laspy.LasHeader()
-        >>> header.scales = np.array([0.1, 0.1, 0.1])
-        >>> header.offsets = np.array([0, 0 ,0])
-
-        >>> las = laspy.LasData(header=header)
-        >>> las.x = [10.0]
-        >>> las.y = [20.0]
-        >>> las.z = [30.0]
-
-        >>> # X = (x - x_offset) / x_scale
-        >>> assert np.all(las.xyz == [[10.0, 20., 30]])
-        >>> assert np.all(las.X == [100])
-        >>> assert np.all(las.Y == [200])
-        >>> assert np.all(las.Z == [300])
-
-        We change the scales (only changing x_scale here)
-        but not the offsets.
-
-        The xyz coordinates (double) are the same (minus possible rounding with actual coordinates)
-        However the integer coordinates changed
-
-        >>> las.change_scaling(scales=[0.01, 0.1, 0.1])
-        >>> assert np.all(las.xyz == [[10.0, 20., 30]])
-        >>> assert np.all(las.X == [1000])
-        >>> assert np.all(las.Y == [200])
-        >>> assert np.all(las.Z == [300])
-
-        Same idea if we change the offsets, the xyz do not change
-        but XYZ does
-
-        >>> las.change_scaling(offsets=[0, 10, 15])
-        >>> assert np.all(las.xyz == [[10.0, 20., 30]])
-        >>> assert np.all(las.X == [1000])
-        >>> assert np.all(las.Y == [100])
-        >>> assert np.all(las.Z == [150])
-        """
-        self.points.change_scaling(scales, offsets)
-
-        if scales is not None:
-            self.header.scales = scales
-        if offsets is not None:
-            self.header.offsets = offsets
-
-    def __getattr__(self, item):
-        """Automatically called by Python when the attribute
-        named 'item' is no found. We use this function to forward the call the
-        point record. This is the mechanism used to allow the users to access
-        the points dimensions directly through a LasData.
-
-        Parameters
-        ----------
-        item: str
-            name of the attribute, should be a dimension name
-
-        Returns
-        -------
-        The requested dimension if it exists
-
-        """
-        try:
-            return self.points[item]
-        except ValueError:
-            raise AttributeError(
-                f"{self.__class__.__name__} object has no attribute '{item}'"
-            ) from None
-
-    def __setattr__(self, key, value):
-        """This is called on every access to an attribute of the instance.
-        Again we use this to forward the call the the points record
-
-        But this time checking if the key is actually a dimension name
-        so that an error is raised if the user tries to set a valid
-        LAS dimension even if it is not present in the field.
-        eg: user tries to set the red field of a file with point format 0:
-        an error is raised
-        """
-        if key in ("x", "y", "z"):
-            # It is possible that user created a `LasData` object
-            # via `laspy.create`, and changed the headers offsets and scales
-            # values afterwards. So we need to sync the points's record.
-            self.points.offsets = self.header.offsets
-            self.points.scales = self.header.scales
-            self.points[key] = value
-            return
-
-        name_validity = self.points.validate_dimension_name(key)
-        if name_validity == DimensionNameValidity.Valid:
-            self[key] = value
-        elif name_validity == DimensionNameValidity.Unsupported:
-            raise ValueError(
-                f"Point format {self.point_format} does not support {key} dimension"
-            )
-        else:
-            super().__setattr__(key, value)
-
-    @typing.overload
-    def __getitem__(
-        self, item: Union[str, List[str]]
-    ) -> Union[np.ndarray, ScaledArrayView, SubFieldView]:
-        ...
-
-    @typing.overload
-    def __getitem__(self, item: Union[int, typing.Iterable[int], slice]) -> "LasData":
-        ...
-
-    def __getitem__(self, item):
-        try:
-            item_is_list_of_str = all(isinstance(el, str) for el in iter(item))
-        except TypeError:
-            item_is_list_of_str = False
-
-        if isinstance(item, str) or item_is_list_of_str:
-            return self.points[item]
-        else:
-            las = LasData(deepcopy(self.header), points=self.points[item])
-            las.update_header()
-            return las
-
-    def __setitem__(self, key, value):
-        self.points[key] = value
-
-    def __len__(self):
-        return len(self.points)
-
-    def __repr__(self) -> str:
-        return "<LasData({}.{}, point fmt: {}, {} points, {} vlrs)>".format(
-            self.header.version.major,
-            self.header.version.minor,
-            self.points.point_format,
-            len(self.points),
-            len(self.vlrs),
-        )
+import logging
+import pathlib
+import typing
+from copy import deepcopy
+from typing import BinaryIO, Iterable, List, Optional, Sequence, Union, overload
+
+import numpy as np
+
+from . import errors
+from .compression import LazBackend
+from .header import LasHeader
+from .laswriter import LasWriter
+from .point import ExtraBytesParams, PointFormat, dims, record
+from .point.dims import OLD_LASPY_NAMES, ScaledArrayView, SubFieldView
+from .point.record import DimensionNameValidity
+from .vlrs.vlrlist import VLRList
+
+logger = logging.getLogger(__name__)
+
+
+class LasData:
+    """Class synchronizing all the moving parts of LAS files.
+
+    It connects the point record, header, vlrs together.
+
+    To access points dimensions using this class you have two possibilities
+
+    .. code:: python
+
+        las = laspy.read('some_file.las')
+        las.classification
+        # or
+        las['classification']
+    """
+
+    def __init__(
+        self,
+        header: LasHeader,
+        points: Optional[
+            Union[record.PackedPointRecord, record.ScaleAwarePointRecord]
+        ] = None,
+    ) -> None:
+        if points is None:
+            points = record.ScaleAwarePointRecord.zeros(
+                header.point_count, header=header
+            )
+        if points.point_format != header.point_format:
+            raise errors.LaspyException("Incompatible Point Formats")
+        if isinstance(points, record.PackedPointRecord):
+            points = record.ScaleAwarePointRecord(
+                points.array,
+                header.point_format,
+                scales=header.scales,
+                offsets=header.offsets,
+            )
+        else:
+            assert np.all(header.scales, points.scales)
+            assert np.all(header.offsets, points.offsets)
+        self.__dict__["_points"] = points
+        self.points: record.ScaleAwarePointRecord
+        self.header: LasHeader = header
+
+    @property
+    def point_format(self) -> PointFormat:
+        """Shortcut to get the point format"""
+        return self.points.point_format
+
+    @property
+    def xyz(self) -> np.ndarray:
+        """Returns a **new** 2D numpy array with the x,y,z coordinates
+
+        >>> import laspy
+        >>> las = laspy.read("tests/data/simple.las")
+        >>> xyz = las.xyz
+        >>> xyz.ndim
+        2
+        >>> xyz.shape
+        (1065, 3)
+        >>> np.all(xyz[..., 0] == las.x)
+        True
+        """
+        return np.vstack((self.x, self.y, self.z)).transpose()
+
+    @xyz.setter
+    def xyz(self, value) -> None:
+        self.points[("x", "y", "z")] = value
+
+    @property
+    def points(self) -> record.PackedPointRecord:
+        """Returns the point record"""
+        return self._points
+
+    @points.setter
+    def points(self, new_points: record.PackedPointRecord) -> None:
+        if new_points.point_format != self.point_format:
+            raise errors.IncompatibleDataFormat(
+                "Cannot set points with a different point format, convert first"
+            )
+        self._points = new_points
+        self.update_header()
+        # make sure both point format point to the same object
+        self._points.point_format = self.header.point_format
+
+    @property
+    def vlrs(self) -> VLRList:
+        return self.header.vlrs
+
+    @vlrs.setter
+    def vlrs(self, vlrs) -> None:
+        self.header.vlrs = vlrs
+
+    @property
+    def evlrs(self) -> Optional[VLRList]:
+        return self.header.evlrs
+
+    @evlrs.setter
+    def evlrs(self, evlrs: VLRList) -> None:
+        self.header.evlrs = evlrs
+
+    def add_extra_dim(self, params: ExtraBytesParams) -> None:
+        """Adds a new extra dimension to the point record
+
+        .. note::
+
+            If you plan on adding multiple extra dimensions,
+            prefer :meth:`.add_extra_dims` as it will
+            save re-allocations and data copy
+
+        Parameters
+        ----------
+        params : ExtraBytesParams
+            parameters of the new extra dimension to add
+
+        """
+        self.add_extra_dims([params])
+
+    def add_extra_dims(self, params: List[ExtraBytesParams]) -> None:
+        """Add multiple extra dimensions at once
+
+        Parameters
+        ----------
+
+        params: list of parameters of the new extra dimensions to add
+        """
+        self.header.add_extra_dims(params)
+        new_point_record = record.ScaleAwarePointRecord.zeros(
+            len(self.points), header=self.header
+        )
+        new_point_record.copy_fields_from(self.points)
+        self.points = new_point_record
+
+    def remove_extra_dims(self, names: Iterable[str]) -> None:
+        """Remove multiple extra dimensions from this object
+
+        Parameters
+        ----------
+
+        names: iterable,
+            names of the extra dimensions to be removed
+
+
+        Raises
+        ------
+
+        LaspyException: if you try to remove an extra dimension that do not exist.
+
+        """
+        extra_dimension_names = list(self.point_format.extra_dimension_names)
+        not_extra_dimension = [
+            name for name in names if name not in extra_dimension_names
+        ]
+        if not_extra_dimension:
+            raise errors.LaspyException(
+                f"'{not_extra_dimension}' are not extra dimensions and cannot be removed"
+            )
+
+        self.header.remove_extra_dims(names)
+        new_point_record = record.ScaleAwarePointRecord.zeros(
+            len(self.points), header=self.header
+        )
+        new_point_record.copy_fields_from(self.points)
+        self.points = new_point_record
+
+    def remove_extra_dim(self, name: str) -> None:
+        """Remove an extra dimensions from this object
+
+        .. note::
+
+             If you plan on removing multiple extra dimensions,
+             prefer :meth:`.remove_extra_dims` as it will
+             save re-allocations and data copy
+
+        Parameters
+        ----------
+
+        name: str,
+            name of the extra dimension to be removed
+
+
+        Raises
+        ------
+
+        LaspyException: if you try to remove an extra dimension that do not exist.
+
+        """
+        self.remove_extra_dims([name])
+
+    def update_header(self) -> None:
+        """Update the information stored in the header
+        to be in sync with the actual data.
+
+        This method is called automatically when you save a file using
+        :meth:`laspy.lasdatas.base.LasBase.write`
+        """
+        self.header.update(self.points)
+        self.header.point_format_id = self.points.point_format.id
+        self.header.point_data_record_length = self.points.point_size
+
+        if self.header.version.minor >= 4:
+            if self.evlrs is not None:
+                self.header.number_of_evlrs = len(self.evlrs)
+            self.header.start_of_waveform_data_packet_record = 0
+            # TODO
+            # if len(self.vlrs.get("WktCoordinateSystemVlr")) == 1:
+            #     self.header.global_encoding.wkt = 1
+        else:
+            self.header.number_of_evlrs = 0
+
+    @overload
+    def write(
+        self,
+        destination: str,
+        laz_backend: Optional[Union[LazBackend, Sequence[LazBackend]]] = ...,
+    ) -> None:
+        ...
+
+    @overload
+    def write(
+        self,
+        destination: BinaryIO,
+        do_compress: Optional[bool] = ...,
+        laz_backend: Optional[Union[LazBackend, Sequence[LazBackend]]] = ...,
+    ) -> None:
+        ...
+
+    def write(self, destination, do_compress=None, laz_backend=None):
+        """Writes to a stream or file
+
+        .. note::
+
+            When destination is a string, it will be interpreted as the path were the file should be written to,
+            and whether the file will be compressed depends on the extension used (case insensitive):
+
+                - .laz -> compressed
+                - .las -> uncompressed
+
+            And the do_compress option will be ignored
+
+
+        Parameters
+        ----------
+        destination: str or file object
+            filename or stream to write to
+        do_compress: bool, optional
+            Flags to indicate if you want to compress the data
+        laz_backend: optional, the laz backend to use
+            By default, laspy detect available backends
+        """
+        if isinstance(destination, (str, pathlib.Path)):
+            do_compress = pathlib.Path(destination).suffix.lower() == ".laz"
+
+            with open(destination, mode="wb+") as out:
+                self._write_to(out, do_compress=do_compress, laz_backend=laz_backend)
+        else:
+            self._write_to(
+                destination, do_compress=do_compress, laz_backend=laz_backend
+            )
+
+    def _write_to(
+        self,
+        out_stream: BinaryIO,
+        do_compress: Optional[bool] = None,
+        laz_backend: Optional[Union[LazBackend, Sequence[LazBackend]]] = None,
+    ) -> None:
+        with LasWriter(
+            out_stream,
+            self.header,
+            do_compress=do_compress,
+            closefd=False,
+            laz_backend=laz_backend,
+        ) as writer:
+            writer.write_points(self.points)
+            if self.header.version.minor >= 4 and self.evlrs is not None:
+                writer.write_evlrs(self.evlrs)
+
+    def change_scaling(self, scales=None, offsets=None) -> None:
+        """This changes the scales and/or offset used for the x,y,z
+        dimensions.
+
+        It recomputes the internal, non-scaled X,Y,Z dimensions
+        to match the new scales and offsets.
+
+        It also updates the header with the new values of scales and offsets.
+
+        Parameters
+        ----------
+        scales: optional
+                New scales to be used. If not provided, the scales won't change.
+        offsets: optional
+                 New offsets to be used. If not provided, the offsets won't change.
+
+        Example
+        -------
+
+        >>> import laspy
+        >>> header = laspy.LasHeader()
+        >>> header.scales = np.array([0.1, 0.1, 0.1])
+        >>> header.offsets = np.array([0, 0 ,0])
+
+        >>> las = laspy.LasData(header=header)
+        >>> las.x = [10.0]
+        >>> las.y = [20.0]
+        >>> las.z = [30.0]
+
+        >>> # X = (x - x_offset) / x_scale
+        >>> assert np.all(las.xyz == [[10.0, 20., 30]])
+        >>> assert np.all(las.X == [100])
+        >>> assert np.all(las.Y == [200])
+        >>> assert np.all(las.Z == [300])
+
+        We change the scales (only changing x_scale here)
+        but not the offsets.
+
+        The xyz coordinates (double) are the same (minus possible rounding with actual coordinates)
+        However the integer coordinates changed
+
+        >>> las.change_scaling(scales=[0.01, 0.1, 0.1])
+        >>> assert np.all(las.xyz == [[10.0, 20., 30]])
+        >>> assert np.all(las.X == [1000])
+        >>> assert np.all(las.Y == [200])
+        >>> assert np.all(las.Z == [300])
+
+        Same idea if we change the offsets, the xyz do not change
+        but XYZ does
+
+        >>> las.change_scaling(offsets=[0, 10, 15])
+        >>> assert np.all(las.xyz == [[10.0, 20., 30]])
+        >>> assert np.all(las.X == [1000])
+        >>> assert np.all(las.Y == [100])
+        >>> assert np.all(las.Z == [150])
+        """
+        self.points.change_scaling(scales, offsets)
+
+        if scales is not None:
+            self.header.scales = scales
+        if offsets is not None:
+            self.header.offsets = offsets
+
+    def __getattr__(self, item):
+        """Automatically called by Python when the attribute
+        named 'item' is no found. We use this function to forward the call the
+        point record. This is the mechanism used to allow the users to access
+        the points dimensions directly through a LasData.
+
+        Parameters
+        ----------
+        item: str
+            name of the attribute, should be a dimension name
+
+        Returns
+        -------
+        The requested dimension if it exists
+
+        """
+        try:
+            return self.points[item]
+        except ValueError:
+            raise AttributeError(
+                f"{self.__class__.__name__} object has no attribute '{item}'"
+            ) from None
+
+    def __setattr__(self, key, value):
+        """This is called on every access to an attribute of the instance.
+        Again we use this to forward the call the the points record
+
+        But this time checking if the key is actually a dimension name
+        so that an error is raised if the user tries to set a valid
+        LAS dimension even if it is not present in the field.
+        eg: user tries to set the red field of a file with point format 0:
+        an error is raised
+        """
+        if key in ("x", "y", "z"):
+            # It is possible that user created a `LasData` object
+            # via `laspy.create`, and changed the headers offsets and scales
+            # values afterwards. So we need to sync the points's record.
+            self.points.offsets = self.header.offsets
+            self.points.scales = self.header.scales
+            self.points[key] = value
+            return
+
+        name_validity = self.points.validate_dimension_name(key)
+        if name_validity == DimensionNameValidity.Valid:
+            self[key] = value
+        elif name_validity == DimensionNameValidity.Unsupported:
+            raise ValueError(
+                f"Point format {self.point_format} does not support {key} dimension"
+            )
+        else:
+            super().__setattr__(key, value)
+
+    @typing.overload
+    def __getitem__(
+        self, item: Union[str, List[str]]
+    ) -> Union[np.ndarray, ScaledArrayView, SubFieldView]:
+        ...
+
+    @typing.overload
+    def __getitem__(self, item: Union[int, typing.Iterable[int], slice]) -> "LasData":
+        ...
+
+    def __getitem__(self, item):
+        try:
+            item_is_list_of_str = all(isinstance(el, str) for el in iter(item))
+        except TypeError:
+            item_is_list_of_str = False
+
+        if isinstance(item, str) or item_is_list_of_str:
+            return self.points[item]
+        else:
+            las = LasData(deepcopy(self.header), points=self.points[item])
+            las.update_header()
+            return las
+
+    def __setitem__(self, key, value):
+        self.points[key] = value
+
+    def __len__(self):
+        return len(self.points)
+
+    def __repr__(self) -> str:
+        return "<LasData({}.{}, point fmt: {}, {} points, {} vlrs)>".format(
+            self.header.version.major,
+            self.header.version.minor,
+            self.points.point_format,
+            len(self.points),
+            len(self.vlrs),
+        )
```

### Comparing `laspy-2.4.1/laspy/lasmmap.py` & `laspy-2.5.0/laspy/lasmmap.py`

 * *Ordering differences only*

 * *Files 16% similar despite different names*

```diff
@@ -1,58 +1,58 @@
-import io
-import mmap
-
-from . import lasdata
-from .header import LasHeader
-from .point import record
-from .typehints import PathLike
-
-WHOLE_FILE = 0
-
-
-class LasMMAP(lasdata.LasData):
-    """Memory map a LAS file.
-    It works like a regular LasData however the data is not actually read in memory,
-
-    Access to dimensions are made directly from the file itself, changes made to the points
-    are directly reflected in the mmap file.
-
-    Vlrs cannot be modified.
-
-    This can be useful if you want to be able to process a big LAS file
-
-    .. note::
-        A LAZ (compressed LAS) cannot be mmapped
-    """
-
-    def __init__(self, filename: PathLike) -> None:
-        fileref = open(filename, mode="r+b")
-
-        m = mmap.mmap(fileref.fileno(), length=WHOLE_FILE, access=mmap.ACCESS_WRITE)
-        header = LasHeader.read_from(m)
-        if header.are_points_compressed:
-            raise ValueError("Cannot mmap a compressed LAZ file")
-
-        points_data = record.PackedPointRecord.from_buffer(
-            m,
-            header.point_format,
-            count=header.point_count,
-            offset=header.offset_to_point_data,
-        )
-        super().__init__(header=header, points=points_data)
-
-        self.fileref, self.mmap = fileref, m
-        self.mmap.seek(0, io.SEEK_SET)
-
-    def close(self) -> None:
-        # These need to be set to None, so that
-        # mmap.close() does not give an error because
-        # there are still exported pointers
-        self._points = None
-        self.mmap.close()
-        self.fileref.close()
-
-    def __enter__(self) -> "LasMMAP":
-        return self
-
-    def __exit__(self, exc_type, exc_val, exc_tb) -> None:
-        self.close()
+import io
+import mmap
+
+from . import lasdata
+from .header import LasHeader
+from .point import record
+from .typehints import PathLike
+
+WHOLE_FILE = 0
+
+
+class LasMMAP(lasdata.LasData):
+    """Memory map a LAS file.
+    It works like a regular LasData however the data is not actually read in memory,
+
+    Access to dimensions are made directly from the file itself, changes made to the points
+    are directly reflected in the mmap file.
+
+    Vlrs cannot be modified.
+
+    This can be useful if you want to be able to process a big LAS file
+
+    .. note::
+        A LAZ (compressed LAS) cannot be mmapped
+    """
+
+    def __init__(self, filename: PathLike) -> None:
+        fileref = open(filename, mode="r+b")
+
+        m = mmap.mmap(fileref.fileno(), length=WHOLE_FILE, access=mmap.ACCESS_WRITE)
+        header = LasHeader.read_from(m)
+        if header.are_points_compressed:
+            raise ValueError("Cannot mmap a compressed LAZ file")
+
+        points_data = record.PackedPointRecord.from_buffer(
+            m,
+            header.point_format,
+            count=header.point_count,
+            offset=header.offset_to_point_data,
+        )
+        super().__init__(header=header, points=points_data)
+
+        self.fileref, self.mmap = fileref, m
+        self.mmap.seek(0, io.SEEK_SET)
+
+    def close(self) -> None:
+        # These need to be set to None, so that
+        # mmap.close() does not give an error because
+        # there are still exported pointers
+        self._points = None
+        self.mmap.close()
+        self.fileref.close()
+
+    def __enter__(self) -> "LasMMAP":
+        return self
+
+    def __exit__(self, exc_type, exc_val, exc_tb) -> None:
+        self.close()
```

### Comparing `laspy-2.4.1/laspy/lib.py` & `laspy-2.5.0/laspy/lib.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,407 +1,422 @@
-""" 'Entry point' of the library, Contains the various functions meant to be
-used directly by a user
-"""
-import copy
-import io
-import logging
-import os
-from pathlib import Path
-from typing import Union, Optional
-
-from .compression import LazBackend, DecompressionSelection
-from .errors import LaspyException
-from .header import LasHeader, Version
-from .lasappender import LasAppender
-from .lasdata import LasData
-from .lasmmap import LasMMAP
-from .lasreader import LasReader
-from .laswriter import LasWriter
-from .point import dims, record, PointFormat
-from .vlrs.vlrlist import VLRList
-
-logger = logging.getLogger(__name__)
-
-
-def open_las(
-    source,
-    mode="r",
-    closefd=True,
-    laz_backend=None,
-    header=None,
-    do_compress=None,
-    encoding_errors: str = "strict",
-    read_evlrs: bool = True,
-    decompression_selection: DecompressionSelection = DecompressionSelection.all(),
-) -> Union[LasReader, LasWriter, LasAppender]:
-    """The laspy.open opens a LAS/LAZ file in one of the 3 supported
-    mode:
-
-     - "r" => Reading => a :class:`laspy.LasReader` will be returned
-     - "w" => Writing => a :class:`laspy.LasWriter` will be returned
-     - "a" => Appending => a :class:`laspy.LasAppender` will be returned
-
-
-    When opening a file in 'w' mode, a header (:class:`laspy.LasHeader`)
-    is required
-
-        >>> with open_las('tests/data/simple.las') as f:
-        ...     print(f.header.point_format.id)
-        3
-
-
-        >>> f = open('tests/data/simple.las', mode='rb')
-        >>> with open_las(f,closefd=False) as flas:
-        ...     print(flas.header)
-        <LasHeader(1.2, <PointFormat(3, 0 bytes of extra dims)>)>
-        >>> f.closed
-        False
-        >>> f.close()
-        >>> f.closed
-        True
-
-
-        >>> f = open('tests/data/simple.las', mode='rb')
-        >>> with open_las(f) as flas:
-        ...    las = flas.read()
-        >>> f.closed
-        True
-
-    Parameters
-    ----------
-    source: str or bytes or io.BytesIO
-        if source is a str it must be a filename
-
-    mode: Optional, the mode to open the file:
-        - "r" for reading (default)
-        - "w" for writing
-        - "a" for appending
-
-    laz_backend: Optional, laspy.LazBackend, the LAZ backend to use to handle decompression/compression
-
-        By default available backends are detected, see LazBackend to see the
-        preference order when multiple backends are available
-
-    header: The header to use when opening in write mode.
-
-    do_compress: optional, bool, only meaningful in writing mode:
-        - None (default) guess if compression is needed using the file extension
-          or if a laz_backend was explicitely provided
-        - True compresses the file
-        - False do not compress the file
-
-    closefd: optional, bool, True by default
-        Whether the stream/file object shall be closed, this only work
-        when using open_las in a with statement. An exception is raised if
-        closefd is specified and the source is a filename
-
-    encoding_errors: str, default 'strict'
-        Only used in writing and appending mode.
-        How encoding errors should be treated.
-        Possible values and their explanation can be seen here:
-        https://docs.python.org/3/library/codecs.html#error-handlers.
-
-    read_evlrs: bool, default True
-            Only applies to 'r' mode.
-
-            If True the evlrs will be read during the __init__ / file opening
-            along with the LasHeader.
-
-            It is fine for most of the cases,
-            but can be problematic when opening file from a data stream like
-            AWS S3 as EVLRs are located at the end of the files, thus
-            will require to pull the whole file.
-
-            Does nothing if the input file does not support
-            EVLRs
-
-    decompression_selection: DecompressionSelection, default All
-        Only applies to 'r' mode and for files which suport selective decompression
-        (version >= 1.4 and point format id >= 6), ignored otherwise.
-
-        Allows to select which fields should be decompressed or not, allowing to save time
-        by not decompressing unused fields.
-
-        By default all fields are decompressed
-
-    .. versionadded:: 2.4
-        The ``read_evlrs`` and ``decompression_selection`` parameters.
-    """
-    if mode == "r":
-        if header is not None:
-            raise LaspyException(
-                "header argument is not used when opening in read mode, "
-                "did you meant to open in write mode ?"
-            )
-        if do_compress is not None:
-            raise LaspyException(
-                "do_compress argument is not used when opening in read mode, "
-                "did you meant to open in write mode ?"
-            )
-        if isinstance(source, (str, Path)):
-            stream = open(source, mode="rb", closefd=closefd)
-        elif isinstance(source, bytes):
-            stream = io.BytesIO(source)
-        else:
-            stream = source
-        return LasReader(
-            stream,
-            closefd=closefd,
-            laz_backend=laz_backend,
-            read_evlrs=read_evlrs,
-            decompression_selection=decompression_selection,
-        )
-    elif mode == "w":
-        if header is None:
-            raise ValueError("A header is needed when opening a file for writing")
-
-        if isinstance(source, (str, Path)):
-            if do_compress is None:
-                do_compress = os.path.splitext(source)[1].lower() == ".laz"
-            stream = open(source, mode="wb+", closefd=closefd)
-        elif isinstance(source, bytes):
-            stream = io.BytesIO(source)
-        else:
-            assert source.seekable()
-            stream = source
-
-        return LasWriter(
-            stream,
-            header=header,
-            do_compress=do_compress,
-            laz_backend=laz_backend,
-            closefd=closefd,
-            encoding_errors=encoding_errors,
-        )
-    elif mode == "a":
-        if isinstance(source, (str, Path)):
-            stream = open(source, mode="rb+", closefd=closefd)
-        elif isinstance(source, bytes):
-            stream = io.BytesIO(source)
-        else:
-            stream = source
-        return LasAppender(
-            stream,
-            closefd=closefd,
-            laz_backend=laz_backend,
-            encoding_errors=encoding_errors,
-        )
-
-    else:
-        raise ValueError(f"Unknown mode '{mode}'")
-
-
-def read_las(
-    source,
-    closefd=True,
-    laz_backend=LazBackend.detect_available(),
-    decompression_selection: DecompressionSelection = DecompressionSelection.all(),
-):
-    """Entry point for reading las data in laspy
-
-    Reads the whole file into memory.
-
-    >>> las = read_las("tests/data/simple.las")
-    >>> las.classification
-    <SubFieldView([1 1 1 ... 1 1 1])>
-
-    Parameters
-    ----------
-    source : str or io.BytesIO
-        The source to read data from
-
-    laz_backend: Optional, the backend to use when the file is as LAZ file.
-                 By default laspy will find the backend to use by itself.
-                 Use if you want a specific backend to be used
-
-    closefd: bool
-            if True and the source is a stream, the function will close it
-            after it is done reading
-
-    decompression_selection: DecompressionSelection,
-        see :func:`laspy.open`
-
-
-    Returns
-    -------
-    laspy.LasData
-        The object you can interact with to get access to the LAS points & VLRs
-
-
-    .. versionadded:: 2.4
-        The ``decompression_selection`` parameter.
-    """
-    with open_las(
-        source,
-        closefd=closefd,
-        laz_backend=laz_backend,
-        decompression_selection=decompression_selection,
-    ) as reader:
-        return reader.read()
-
-
-def mmap_las(filename):
-    """MMap a file, much like laspy did"""
-    return LasMMAP(filename)
-
-
-def create_las(
-    *,
-    point_format: Optional[Union[int, PointFormat]] = None,
-    file_version: Optional[Union[str, Version]] = None,
-):
-    """Function to create a new empty las data object
-
-    .. note::
-
-        If you provide both point_format and file_version
-        an exception will be raised if they are not compatible
-
-    >>> las = create_las(point_format=6,file_version="1.2")
-    Traceback (most recent call last):
-     ...
-    laspy.errors.LaspyException: Point format 6 is not compatible with file version 1.2
-
-
-    If you provide only the point_format the file_version will automatically
-    selected for you.
-
-    >>> las = create_las(point_format=0)
-    >>> las.header.version == '1.2'
-    True
-
-    >>> las = create_las(point_format=PointFormat(6))
-    >>> las.header.version == '1.4'
-    True
-
-
-    Parameters
-    ----------
-    point_format:
-        The point format you want the created file to have
-
-    file_version:
-        The las version you want the created las to have
-
-    Returns
-    -------
-    laspy.lasdatas.base.LasBase
-       A new las data object
-
-    """
-    header = LasHeader(point_format=point_format, version=file_version)
-    return LasData(header=header)
-
-
-def convert(source_las, *, point_format_id=None, file_version=None):
-    """Converts a Las from one point format to another
-    Automatically upgrades the file version if source file version is not compatible with
-    the new point_format_id
-
-
-    convert to point format 0
-
-    >>> las = read_las('tests/data/simple.las')
-    >>> las.header.version
-    Version(major=1, minor=2)
-    >>> las = convert(las, point_format_id=0)
-    >>> las.header.point_format.id
-    0
-    >>> str(las.header.version)
-    '1.2'
-
-    convert to point format 6, which need version >= 1.4
-    then convert back to point format 0, version is not downgraded
-
-    >>> las = read_las('tests/data/simple.las')
-    >>> str(las.header.version)
-    '1.2'
-    >>> las = convert(las, point_format_id=6)
-    >>> las.header.point_format.id
-    6
-    >>> str(las.header.version)
-    '1.4'
-    >>> las = convert(las, point_format_id=0)
-    >>> str(las.header.version)
-    '1.4'
-
-    an exception is raised if the requested point format is not compatible
-    with the file version
-
-    >>> las = read_las('tests/data/simple.las')
-    >>> convert(las, point_format_id=6, file_version='1.2')
-    Traceback (most recent call last):
-     ...
-    laspy.errors.LaspyException: Point format 6 is not compatible with file version 1.2
-
-    Parameters
-    ----------
-    source_las : laspy.lasdatas.base.LasBase
-        The source data to be converted
-
-    point_format_id : int, optional
-        The new point format id (the default is None, which won't change the source format id)
-
-    file_version : str, optional,
-        The new file version. None by default which means that the file_version
-        may be upgraded for compatibility with the new point_format. The file version will not
-        be downgraded.
-
-    Returns
-    -------
-        laspy.lasdatas.base.LasBase
-    """
-    if point_format_id is None:
-        point_format_id = source_las.point_format.id
-
-    if file_version is None:
-        file_version = max(
-            str(source_las.header.version),
-            dims.preferred_file_version_for_point_format(point_format_id),
-        )
-    else:
-        file_version = str(file_version)
-        dims.raise_if_version_not_compatible_with_fmt(point_format_id, file_version)
-
-    version = Version.from_str(file_version)
-
-    point_format = PointFormat(point_format_id)
-    point_format.dimensions.extend(source_las.point_format.extra_dimensions)
-
-    header = copy.deepcopy(source_las.header)
-    header.set_version_and_point_format(version, point_format)
-
-    if source_las.evlrs is not None:
-        evlrs = VLRList(source_las.evlrs.copy())
-    else:
-        evlrs = None
-
-    points = record.PackedPointRecord.from_point_record(
-        source_las.points, header.point_format
-    )
-    las = LasData(header=header, points=points)
-
-    if file_version < "1.4" and evlrs is not None and evlrs:
-        logger.warning(
-            "The source contained {} EVLRs,"
-            " they will be lost as version {} doest not support them".format(
-                len(evlrs), file_version
-            )
-        )
-    else:
-        las.evlrs = evlrs
-
-    return las
-
-
-def write_then_read_again(
-    las, do_compress=False, laz_backend=LazBackend.detect_available()
-):
-    """writes the given las into memory using BytesIO and
-    reads it again, returning the newly read file.
-
-    Mostly used for testing purposes, without having to write to disk
-    """
-    out = io.BytesIO()
-    las.write(out, do_compress=do_compress, laz_backend=laz_backend)
-    out.seek(0)
-    return read_las(out)
+""" 'Entry point' of the library, Contains the various functions meant to be
+used directly by a user
+"""
+import copy
+import io
+import logging
+import os
+from pathlib import Path
+from typing import Optional, Union
+
+from .compression import DecompressionSelection, LazBackend
+from .errors import LaspyException
+from .header import LasHeader, Version
+from .lasappender import LasAppender
+from .lasdata import LasData
+from .lasmmap import LasMMAP
+from .lasreader import LasReader
+from .laswriter import LasWriter
+from .point import PointFormat, dims, record
+from .vlrs.vlrlist import VLRList
+
+logger = logging.getLogger(__name__)
+
+
+def open_las(
+    source,
+    mode="r",
+    closefd=True,
+    laz_backend=None,
+    header=None,
+    do_compress=None,
+    encoding_errors: str = "strict",
+    read_evlrs: bool = True,
+    decompression_selection: DecompressionSelection = DecompressionSelection.all(),
+) -> Union[LasReader, LasWriter, LasAppender]:
+    """The laspy.open opens a LAS/LAZ file in one of the 3 supported
+    mode:
+
+     - "r" => Reading => a :class:`laspy.LasReader` will be returned
+     - "w" => Writing => a :class:`laspy.LasWriter` will be returned
+     - "a" => Appending => a :class:`laspy.LasAppender` will be returned
+
+
+    When opening a file in 'w' mode, a header (:class:`laspy.LasHeader`)
+    is required
+
+        >>> with open_las('tests/data/simple.las') as f:
+        ...     print(f.header.point_format.id)
+        3
+
+
+        >>> f = open('tests/data/simple.las', mode='rb')
+        >>> with open_las(f,closefd=False) as flas:
+        ...     print(flas.header)
+        <LasHeader(1.2, <PointFormat(3, 0 bytes of extra dims)>)>
+        >>> f.closed
+        False
+        >>> f.close()
+        >>> f.closed
+        True
+
+
+        >>> f = open('tests/data/simple.las', mode='rb')
+        >>> with open_las(f) as flas:
+        ...    las = flas.read()
+        >>> f.closed
+        True
+
+    Parameters
+    ----------
+    source: str or bytes or io.BytesIO
+        if source is a str it must be a filename
+
+    mode: Optional, the mode to open the file:
+        - "r" for reading (default)
+        - "w" for writing
+        - "a" for appending
+
+    laz_backend: Optional, laspy.LazBackend, the LAZ backend to use to handle decompression/compression
+
+        By default available backends are detected, see LazBackend to see the
+        preference order when multiple backends are available
+
+    header: The header to use when opening in write mode.
+
+    do_compress: optional, bool, only meaningful in writing mode:
+        - None (default) guess if compression is needed using the file extension
+          or if a laz_backend was explicitely provided
+        - True compresses the file
+        - False do not compress the file
+
+    closefd: optional, bool, True by default
+        Whether the stream/file object shall be closed, this only work
+        when using open_las in a with statement. An exception is raised if
+        closefd is specified and the source is a filename
+
+    encoding_errors: str, default 'strict'
+        Only used in writing and appending mode.
+        How encoding errors should be treated.
+        Possible values and their explanation can be seen here:
+        https://docs.python.org/3/library/codecs.html#error-handlers.
+
+    read_evlrs: bool, default True
+            Only applies to 'r' mode.
+
+            If True the evlrs will be read during the __init__ / file opening
+            along with the LasHeader.
+
+            It is fine for most of the cases,
+            but can be problematic when opening file from a data stream like
+            AWS S3 as EVLRs are located at the end of the files, thus
+            will require to pull the whole file.
+
+            Does nothing if the input file does not support
+            EVLRs
+
+    decompression_selection: DecompressionSelection, default All
+        Only applies to 'r' mode and for files which suport selective decompression
+        (version >= 1.4 and point format id >= 6), ignored otherwise.
+
+        Allows to select which fields should be decompressed or not, allowing to save time
+        by not decompressing unused fields.
+
+        By default all fields are decompressed
+
+    .. versionadded:: 2.4
+        The ``read_evlrs`` and ``decompression_selection`` parameters.
+    """
+    if mode == "r":
+        if header is not None:
+            raise LaspyException(
+                "header argument is not used when opening in read mode, "
+                "did you meant to open in write mode ?"
+            )
+        if do_compress is not None:
+            raise LaspyException(
+                "do_compress argument is not used when opening in read mode, "
+                "did you meant to open in write mode ?"
+            )
+        if isinstance(source, (str, Path)):
+            stream = open(source, mode="rb", closefd=closefd)
+        elif isinstance(source, bytes):
+            stream = io.BytesIO(source)
+        else:
+            stream = source
+        try:
+            return LasReader(
+                stream,
+                closefd=closefd,
+                laz_backend=laz_backend,
+                read_evlrs=read_evlrs,
+                decompression_selection=decompression_selection,
+            )
+        except:
+            if closefd:
+                stream.close()
+            raise
+    elif mode == "w":
+        if header is None:
+            raise ValueError("A header is needed when opening a file for writing")
+
+        if isinstance(source, (str, Path)):
+            if do_compress is None:
+                do_compress = os.path.splitext(source)[1].lower() == ".laz"
+            stream = open(source, mode="wb+", closefd=closefd)
+        elif isinstance(source, bytes):
+            stream = io.BytesIO(source)
+        else:
+            assert source.seekable()
+            stream = source
+
+        try:
+            return LasWriter(
+                stream,
+                header=header,
+                do_compress=do_compress,
+                laz_backend=laz_backend,
+                closefd=closefd,
+                encoding_errors=encoding_errors,
+            )
+        except:
+            if closefd:
+                stream.close()
+            raise
+    elif mode == "a":
+        if isinstance(source, (str, Path)):
+            stream = open(source, mode="rb+", closefd=closefd)
+        elif isinstance(source, bytes):
+            stream = io.BytesIO(source)
+        else:
+            stream = source
+
+        try:
+            return LasAppender(
+                stream,
+                closefd=closefd,
+                laz_backend=laz_backend,
+                encoding_errors=encoding_errors,
+            )
+        except:
+            if closefd:
+                stream.close()
+            raise
+    else:
+        raise ValueError(f"Unknown mode '{mode}'")
+
+
+def read_las(
+    source,
+    closefd=True,
+    laz_backend=LazBackend.detect_available(),
+    decompression_selection: DecompressionSelection = DecompressionSelection.all(),
+):
+    """Entry point for reading las data in laspy
+
+    Reads the whole file into memory.
+
+    >>> las = read_las("tests/data/simple.las")
+    >>> las.classification
+    <SubFieldView([1 1 1 ... 1 1 1])>
+
+    Parameters
+    ----------
+    source : str or io.BytesIO
+        The source to read data from
+
+    laz_backend: Optional, the backend to use when the file is as LAZ file.
+                 By default laspy will find the backend to use by itself.
+                 Use if you want a specific backend to be used
+
+    closefd: bool
+            if True and the source is a stream, the function will close it
+            after it is done reading
+
+    decompression_selection: DecompressionSelection,
+        see :func:`laspy.open`
+
+
+    Returns
+    -------
+    laspy.LasData
+        The object you can interact with to get access to the LAS points & VLRs
+
+
+    .. versionadded:: 2.4
+        The ``decompression_selection`` parameter.
+    """
+    with open_las(
+        source,
+        closefd=closefd,
+        laz_backend=laz_backend,
+        decompression_selection=decompression_selection,
+    ) as reader:
+        return reader.read()
+
+
+def mmap_las(filename):
+    """MMap a file, much like laspy did"""
+    return LasMMAP(filename)
+
+
+def create_las(
+    *,
+    point_format: Optional[Union[int, PointFormat]] = None,
+    file_version: Optional[Union[str, Version]] = None,
+):
+    """Function to create a new empty las data object
+
+    .. note::
+
+        If you provide both point_format and file_version
+        an exception will be raised if they are not compatible
+
+    >>> las = create_las(point_format=6,file_version="1.2")
+    Traceback (most recent call last):
+     ...
+    laspy.errors.LaspyException: Point format 6 is not compatible with file version 1.2
+
+
+    If you provide only the point_format the file_version will automatically
+    selected for you.
+
+    >>> las = create_las(point_format=0)
+    >>> las.header.version == '1.2'
+    True
+
+    >>> las = create_las(point_format=PointFormat(6))
+    >>> las.header.version == '1.4'
+    True
+
+
+    Parameters
+    ----------
+    point_format:
+        The point format you want the created file to have
+
+    file_version:
+        The las version you want the created las to have
+
+    Returns
+    -------
+    laspy.lasdatas.base.LasBase
+       A new las data object
+
+    """
+    header = LasHeader(point_format=point_format, version=file_version)
+    return LasData(header=header)
+
+
+def convert(source_las, *, point_format_id=None, file_version=None):
+    """Converts a Las from one point format to another
+    Automatically upgrades the file version if source file version is not compatible with
+    the new point_format_id
+
+
+    convert to point format 0
+
+    >>> las = read_las('tests/data/simple.las')
+    >>> las.header.version
+    Version(major=1, minor=2)
+    >>> las = convert(las, point_format_id=0)
+    >>> las.header.point_format.id
+    0
+    >>> str(las.header.version)
+    '1.2'
+
+    convert to point format 6, which need version >= 1.4
+    then convert back to point format 0, version is not downgraded
+
+    >>> las = read_las('tests/data/simple.las')
+    >>> str(las.header.version)
+    '1.2'
+    >>> las = convert(las, point_format_id=6)
+    >>> las.header.point_format.id
+    6
+    >>> str(las.header.version)
+    '1.4'
+    >>> las = convert(las, point_format_id=0)
+    >>> str(las.header.version)
+    '1.4'
+
+    an exception is raised if the requested point format is not compatible
+    with the file version
+
+    >>> las = read_las('tests/data/simple.las')
+    >>> convert(las, point_format_id=6, file_version='1.2')
+    Traceback (most recent call last):
+     ...
+    laspy.errors.LaspyException: Point format 6 is not compatible with file version 1.2
+
+    Parameters
+    ----------
+    source_las : laspy.lasdatas.base.LasBase
+        The source data to be converted
+
+    point_format_id : int, optional
+        The new point format id (the default is None, which won't change the source format id)
+
+    file_version : str, optional,
+        The new file version. None by default which means that the file_version
+        may be upgraded for compatibility with the new point_format. The file version will not
+        be downgraded.
+
+    Returns
+    -------
+        laspy.lasdatas.base.LasBase
+    """
+    if point_format_id is None:
+        point_format_id = source_las.point_format.id
+
+    if file_version is None:
+        file_version = max(
+            str(source_las.header.version),
+            dims.preferred_file_version_for_point_format(point_format_id),
+        )
+    else:
+        file_version = str(file_version)
+        dims.raise_if_version_not_compatible_with_fmt(point_format_id, file_version)
+
+    version = Version.from_str(file_version)
+
+    point_format = PointFormat(point_format_id)
+    point_format.dimensions.extend(source_las.point_format.extra_dimensions)
+
+    header = copy.deepcopy(source_las.header)
+    header.set_version_and_point_format(version, point_format)
+
+    if source_las.evlrs is not None:
+        evlrs = VLRList(source_las.evlrs.copy())
+    else:
+        evlrs = None
+
+    points = record.PackedPointRecord.from_point_record(
+        source_las.points, header.point_format
+    )
+    las = LasData(header=header, points=points)
+
+    if file_version < "1.4" and evlrs is not None and evlrs:
+        logger.warning(
+            "The source contained {} EVLRs,"
+            " they will be lost as version {} doest not support them".format(
+                len(evlrs), file_version
+            )
+        )
+    else:
+        las.evlrs = evlrs
+
+    return las
+
+
+def write_then_read_again(
+    las, do_compress=False, laz_backend=LazBackend.detect_available()
+):
+    """writes the given las into memory using BytesIO and
+    reads it again, returning the newly read file.
+
+    Mostly used for testing purposes, without having to write to disk
+    """
+    out = io.BytesIO()
+    las.write(out, do_compress=do_compress, laz_backend=laz_backend)
+    out.seek(0)
+    return read_las(out)
```

### Comparing `laspy-2.4.1/laspy/point/format.py` & `laspy-2.5.0/laspy/point/format.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,270 +1,270 @@
-from itertools import zip_longest, takewhile
-from typing import Optional, Iterable, Union, Type, List
-
-import numpy as np
-
-from . import dims
-from ..errors import LaspyException
-
-Number = Union[np.number, float, int]
-
-
-class ExtraBytesParams:
-    """All parameters needed to create extra bytes"""
-
-    def __init__(
-        self,
-        name: str,
-        type: Union[str, np.dtype, Type[np.uint8]],
-        description: str = "",
-        offsets: Optional[Iterable[Number]] = None,
-        scales: Optional[Iterable[Number]] = None,
-    ) -> None:
-        self.name = name
-        """ The name of the extra dimension """
-        if isinstance(type, str):
-            # Work around numpy deprecating support
-            # for '1type' strings
-            n = "".join(takewhile(lambda c: c.isdigit(), type))
-            if n == "1":
-                type = type[1:]
-
-        self.type = np.dtype(type)
-        """ The type of the extra dimension """
-        self.description = description
-        """ A description of the extra dimension """
-        self.offsets = np.array(offsets) if offsets is not None else offsets
-        """ The offsets to use if its a 'scaled dimension', can be none """
-        self.scales = np.array(scales) if scales is not None else scales
-        """ The scales to use if its a 'scaled dimension', can be none """
-
-
-class PointFormat:
-    """Class that contains the informations about the dimensions that forms a PointFormat.
-
-    A PointFormat has 'standard' dimensions (dimensions defined in the LAS standard, each
-    point format has its set of dimensions), but it can also have extra (non-standard) dimensions
-    defined by the user)
-
-    >>> fmt = PointFormat(3)
-    >>> all(dim.is_standard for dim in fmt.dimensions)
-    True
-    >>> dim = fmt.dimension_by_name("classification") # or fmt["classification"]
-    >>> dim.max
-    31
-    >>> dim.min
-    0
-    >>> dim.num_bits
-    5
-
-    """
-
-    def __init__(
-        self,
-        point_format_id: int,
-    ):
-        """
-        Parameters
-        ----------
-        point_format_id: int
-            point format id
-        """
-        self.id: int = point_format_id
-        self.dimensions: List[dims.DimensionInfo] = []
-        composed_dims = dims.COMPOSED_FIELDS[self.id]
-        for dim_name in dims.ALL_POINT_FORMATS_DIMENSIONS[self.id]:
-            try:
-                sub_fields = composed_dims[dim_name]
-            except KeyError:
-                dimension = dims.DimensionInfo.from_dtype(
-                    dim_name, dims.DIMENSIONS_TO_TYPE[dim_name], is_standard=True
-                )
-                self.dimensions.append(dimension)
-            else:
-                for sub_field in sub_fields:
-                    dimension = dims.DimensionInfo.from_bitmask(
-                        sub_field.name, sub_field.mask, is_standard=True
-                    )
-                    self.dimensions.append(dimension)
-
-    @property
-    def standard_dimensions(self) -> Iterable[dims.DimensionInfo]:
-        """Returns an iterable of the standard dimensions
-
-        >>> fmt = PointFormat(0)
-        >>> standard_dims = list(fmt.standard_dimensions)
-        >>> len(standard_dims)
-        15
-        >>> standard_dims[4].name
-        'return_number'
-
-
-        """
-        return (dim for dim in self.dimensions if dim.is_standard)
-
-    @property
-    def extra_dimensions(self) -> Iterable[dims.DimensionInfo]:
-        return (dim for dim in self.dimensions if dim.is_standard is False)
-
-    @property
-    def dimension_names(self) -> Iterable[str]:
-        """Returns the names of the dimensions contained in the point format"""
-        return (dim.name for dim in self.dimensions)
-
-    @property
-    def standard_dimension_names(self) -> Iterable[str]:
-        """Returns the names of the extra dimensions in this point format"""
-        return (dim.name for dim in self.standard_dimensions)
-
-    @property
-    def extra_dimension_names(self) -> Iterable[str]:
-        """Returns the names of the extra dimensions in this point format"""
-        return (dim.name for dim in self.extra_dimensions)
-
-    @property
-    def size(self) -> int:
-        """Returns the number of bytes (standard + extra) a point takes
-
-        >>> PointFormat(3).size
-        34
-
-        >>> fmt = PointFormat(3)
-        >>> fmt.add_extra_dimension(ExtraBytesParams("codification", "uint64"))
-        >>> fmt.size
-        42
-        """
-        return int(sum(dim.num_bits for dim in self.dimensions) // 8)
-
-    @property
-    def num_standard_bytes(self) -> int:
-        """Returns the number of bytes used by standard dims
-
-        >>> fmt = PointFormat(3)
-        >>> fmt.add_extra_dimension(ExtraBytesParams("codification", "uint64"))
-        >>> fmt.num_standard_bytes
-        34
-        """
-        return int(sum(dim.num_bits for dim in self.standard_dimensions) // 8)
-
-    @property
-    def num_extra_bytes(self) -> int:
-        """Returns the number of extra bytes
-
-        >>> fmt = PointFormat(3)
-        >>> fmt.add_extra_dimension(ExtraBytesParams("codification", "uint64"))
-        >>> fmt.num_extra_bytes
-        8
-        """
-        return int(sum(dim.num_bits for dim in self.extra_dimensions) // 8)
-
-    @property
-    def has_waveform_packet(self):
-        """Returns True if the point format has waveform packet dimensions"""
-        dimensions = set(self.dimension_names)
-        return all(name in dimensions for name in dims.WAVEFORM_FIELDS_NAMES)
-
-    def dimension_by_name(self, name: str) -> dims.DimensionInfo:
-        """Returns the dimension info for the dimension by name
-
-        ValueError is raised if the dimension does not exist un the point format
-
-        >>> info = PointFormat(2).dimension_by_name('number_of_returns')
-        >>> info.name == 'number_of_returns'
-        True
-        >>> info.num_bits == 3
-        True
-
-
-        >>> info = PointFormat(2).dimension_by_name('gps_time')
-        Traceback (most recent call last):
-        ...
-        ValueError: Dimension 'gps_time' does not exist
-        """
-        for dim in self.dimensions:
-            if dim.name == name:
-                return dim
-        raise ValueError(f"Dimension '{name}' does not exist")
-
-    def add_extra_dimension(self, param: ExtraBytesParams) -> None:
-        """Add an extra, user-defined dimension"""
-        dim_info = dims.DimensionInfo.from_extra_bytes_param(param)
-        # todo: this should be checked in extra bytes param ctor
-        if (
-            dim_info.num_elements > 3
-            and dim_info.kind != dims.DimensionKind.UnsignedInteger
-        ):
-            raise LaspyException("Extra Dimensions do not support more than 3 elements")
-        self.dimensions.append(dim_info)
-
-    def remove_extra_dimension(self, name: str) -> None:
-        dimensions = [
-            dim for dim in self.dimensions if dim.name == name and not dim.is_standard
-        ]
-
-        try:
-            dimension = dimensions[0]
-        except IndexError:
-            if name in self.standard_dimension_names:
-                raise LaspyException(
-                    f"The dimension named '{name}' is not an extra dimension, "
-                    "so it cannot be removed"
-                )
-            else:
-                raise LaspyException(
-                    f"'No extra dimension named '{name}' exist"
-                ) from None
-
-        self.dimensions = [dim for dim in self.dimensions if dim is not dimension]
-
-    def dtype(self):
-        """Returns the numpy.dtype used to store the point records in a numpy array
-
-        .. note::
-
-            The dtype corresponds to the dtype with sub_fields *packed* into their
-            composed fields
-
-        """
-        dtype = dims.ALL_POINT_FORMATS_DTYPE[self.id]
-        descr = dtype.descr
-        for extra_dim in self.extra_dimensions:
-            descr.append((extra_dim.name, extra_dim.type_str()))
-        return np.dtype(descr)
-
-    def __getitem__(self, item):
-        if isinstance(item, str):
-            return self.dimension_by_name(item)
-        return self.dimensions[item]
-
-    def __eq__(self, other):
-        if self.id != other.id:
-            return False
-
-        for my_eb, ot_eb in zip_longest(self.extra_dimensions, other.extra_dimensions):
-            if my_eb is None or ot_eb is None:
-                return False
-
-            if my_eb != ot_eb:
-                return False
-
-        return True
-
-    def __repr__(self):
-        return "<PointFormat({}, {} bytes of extra dims)>".format(
-            self.id, self.num_extra_bytes
-        )
-
-
-def lost_dimensions(point_fmt_in, point_fmt_out):
-    """Returns a list of the names of the dimensions that will be lost
-    when converting from point_fmt_in to point_fmt_out
-    """
-
-    dimensions_in = set(PointFormat(point_fmt_in).dimension_names)
-    dimensions_out = set(PointFormat(point_fmt_out).dimension_names)
-
-    completely_lost = []
-    for dim_name in dimensions_in:
-        if dim_name not in dimensions_out:
-            completely_lost.append(dim_name)
-    return completely_lost
+from itertools import takewhile, zip_longest
+from typing import Iterable, List, Optional, Type, Union
+
+import numpy as np
+
+from ..errors import LaspyException
+from . import dims
+
+Number = Union[np.number, float, int]
+
+
+class ExtraBytesParams:
+    """All parameters needed to create extra bytes"""
+
+    def __init__(
+        self,
+        name: str,
+        type: Union[str, np.dtype, Type[np.uint8]],
+        description: str = "",
+        offsets: Optional[Iterable[Number]] = None,
+        scales: Optional[Iterable[Number]] = None,
+    ) -> None:
+        self.name = name
+        """ The name of the extra dimension """
+        if isinstance(type, str):
+            # Work around numpy deprecating support
+            # for '1type' strings
+            n = "".join(takewhile(lambda c: c.isdigit(), type))
+            if n == "1":
+                type = type[1:]
+
+        self.type = np.dtype(type)
+        """ The type of the extra dimension """
+        self.description = description
+        """ A description of the extra dimension """
+        self.offsets = np.array(offsets) if offsets is not None else offsets
+        """ The offsets to use if its a 'scaled dimension', can be none """
+        self.scales = np.array(scales) if scales is not None else scales
+        """ The scales to use if its a 'scaled dimension', can be none """
+
+
+class PointFormat:
+    """Class that contains the informations about the dimensions that forms a PointFormat.
+
+    A PointFormat has 'standard' dimensions (dimensions defined in the LAS standard, each
+    point format has its set of dimensions), but it can also have extra (non-standard) dimensions
+    defined by the user)
+
+    >>> fmt = PointFormat(3)
+    >>> all(dim.is_standard for dim in fmt.dimensions)
+    True
+    >>> dim = fmt.dimension_by_name("classification") # or fmt["classification"]
+    >>> dim.max
+    31
+    >>> dim.min
+    0
+    >>> dim.num_bits
+    5
+
+    """
+
+    def __init__(
+        self,
+        point_format_id: int,
+    ):
+        """
+        Parameters
+        ----------
+        point_format_id: int
+            point format id
+        """
+        self.id: int = point_format_id
+        self.dimensions: List[dims.DimensionInfo] = []
+        composed_dims = dims.COMPOSED_FIELDS[self.id]
+        for dim_name in dims.ALL_POINT_FORMATS_DIMENSIONS[self.id]:
+            try:
+                sub_fields = composed_dims[dim_name]
+            except KeyError:
+                dimension = dims.DimensionInfo.from_dtype(
+                    dim_name, dims.DIMENSIONS_TO_TYPE[dim_name], is_standard=True
+                )
+                self.dimensions.append(dimension)
+            else:
+                for sub_field in sub_fields:
+                    dimension = dims.DimensionInfo.from_bitmask(
+                        sub_field.name, sub_field.mask, is_standard=True
+                    )
+                    self.dimensions.append(dimension)
+
+    @property
+    def standard_dimensions(self) -> Iterable[dims.DimensionInfo]:
+        """Returns an iterable of the standard dimensions
+
+        >>> fmt = PointFormat(0)
+        >>> standard_dims = list(fmt.standard_dimensions)
+        >>> len(standard_dims)
+        15
+        >>> standard_dims[4].name
+        'return_number'
+
+
+        """
+        return (dim for dim in self.dimensions if dim.is_standard)
+
+    @property
+    def extra_dimensions(self) -> Iterable[dims.DimensionInfo]:
+        return (dim for dim in self.dimensions if dim.is_standard is False)
+
+    @property
+    def dimension_names(self) -> Iterable[str]:
+        """Returns the names of the dimensions contained in the point format"""
+        return (dim.name for dim in self.dimensions)
+
+    @property
+    def standard_dimension_names(self) -> Iterable[str]:
+        """Returns the names of the extra dimensions in this point format"""
+        return (dim.name for dim in self.standard_dimensions)
+
+    @property
+    def extra_dimension_names(self) -> Iterable[str]:
+        """Returns the names of the extra dimensions in this point format"""
+        return (dim.name for dim in self.extra_dimensions)
+
+    @property
+    def size(self) -> int:
+        """Returns the number of bytes (standard + extra) a point takes
+
+        >>> PointFormat(3).size
+        34
+
+        >>> fmt = PointFormat(3)
+        >>> fmt.add_extra_dimension(ExtraBytesParams("codification", "uint64"))
+        >>> fmt.size
+        42
+        """
+        return int(sum(dim.num_bits for dim in self.dimensions) // 8)
+
+    @property
+    def num_standard_bytes(self) -> int:
+        """Returns the number of bytes used by standard dims
+
+        >>> fmt = PointFormat(3)
+        >>> fmt.add_extra_dimension(ExtraBytesParams("codification", "uint64"))
+        >>> fmt.num_standard_bytes
+        34
+        """
+        return int(sum(dim.num_bits for dim in self.standard_dimensions) // 8)
+
+    @property
+    def num_extra_bytes(self) -> int:
+        """Returns the number of extra bytes
+
+        >>> fmt = PointFormat(3)
+        >>> fmt.add_extra_dimension(ExtraBytesParams("codification", "uint64"))
+        >>> fmt.num_extra_bytes
+        8
+        """
+        return int(sum(dim.num_bits for dim in self.extra_dimensions) // 8)
+
+    @property
+    def has_waveform_packet(self):
+        """Returns True if the point format has waveform packet dimensions"""
+        dimensions = set(self.dimension_names)
+        return all(name in dimensions for name in dims.WAVEFORM_FIELDS_NAMES)
+
+    def dimension_by_name(self, name: str) -> dims.DimensionInfo:
+        """Returns the dimension info for the dimension by name
+
+        ValueError is raised if the dimension does not exist un the point format
+
+        >>> info = PointFormat(2).dimension_by_name('number_of_returns')
+        >>> info.name == 'number_of_returns'
+        True
+        >>> info.num_bits == 3
+        True
+
+
+        >>> info = PointFormat(2).dimension_by_name('gps_time')
+        Traceback (most recent call last):
+        ...
+        ValueError: Dimension 'gps_time' does not exist
+        """
+        for dim in self.dimensions:
+            if dim.name == name:
+                return dim
+        raise ValueError(f"Dimension '{name}' does not exist")
+
+    def add_extra_dimension(self, param: ExtraBytesParams) -> None:
+        """Add an extra, user-defined dimension"""
+        dim_info = dims.DimensionInfo.from_extra_bytes_param(param)
+        # todo: this should be checked in extra bytes param ctor
+        if (
+            dim_info.num_elements > 3
+            and dim_info.kind != dims.DimensionKind.UnsignedInteger
+        ):
+            raise LaspyException("Extra Dimensions do not support more than 3 elements")
+        self.dimensions.append(dim_info)
+
+    def remove_extra_dimension(self, name: str) -> None:
+        dimensions = [
+            dim for dim in self.dimensions if dim.name == name and not dim.is_standard
+        ]
+
+        try:
+            dimension = dimensions[0]
+        except IndexError:
+            if name in self.standard_dimension_names:
+                raise LaspyException(
+                    f"The dimension named '{name}' is not an extra dimension, "
+                    "so it cannot be removed"
+                )
+            else:
+                raise LaspyException(
+                    f"'No extra dimension named '{name}' exist"
+                ) from None
+
+        self.dimensions = [dim for dim in self.dimensions if dim is not dimension]
+
+    def dtype(self):
+        """Returns the numpy.dtype used to store the point records in a numpy array
+
+        .. note::
+
+            The dtype corresponds to the dtype with sub_fields *packed* into their
+            composed fields
+
+        """
+        dtype = dims.ALL_POINT_FORMATS_DTYPE[self.id]
+        descr = dtype.descr
+        for extra_dim in self.extra_dimensions:
+            descr.append((extra_dim.name, extra_dim.type_str()))
+        return np.dtype(descr)
+
+    def __getitem__(self, item):
+        if isinstance(item, str):
+            return self.dimension_by_name(item)
+        return self.dimensions[item]
+
+    def __eq__(self, other):
+        if self.id != other.id:
+            return False
+
+        for my_eb, ot_eb in zip_longest(self.extra_dimensions, other.extra_dimensions):
+            if my_eb is None or ot_eb is None:
+                return False
+
+            if my_eb != ot_eb:
+                return False
+
+        return True
+
+    def __repr__(self):
+        return "<PointFormat({}, {} bytes of extra dims)>".format(
+            self.id, self.num_extra_bytes
+        )
+
+
+def lost_dimensions(point_fmt_in, point_fmt_out):
+    """Returns a list of the names of the dimensions that will be lost
+    when converting from point_fmt_in to point_fmt_out
+    """
+
+    dimensions_in = set(PointFormat(point_fmt_in).dimension_names)
+    dimensions_out = set(PointFormat(point_fmt_out).dimension_names)
+
+    completely_lost = []
+    for dim_name in dimensions_in:
+        if dim_name not in dimensions_out:
+            completely_lost.append(dim_name)
+    return completely_lost
```

### Comparing `laspy-2.4.1/laspy/utils.py` & `laspy-2.5.0/laspy/utils.py`

 * *Ordering differences only*

 * *Files 18% similar despite different names*

```diff
@@ -1,157 +1,157 @@
-from typing import BinaryIO, Union
-
-
-def encode_to_null_terminated(string: str, codec: str = "utf-8") -> bytes:
-    """
-    >>> encode_to_null_terminated("las files are cool")
-    b'las files are cool\\x00'
-
-    >>> encode_to_null_terminated("")
-    b'\\x00'
-    """
-    b = string.encode(codec)
-    if not b or b[-1] != 0:
-        b += b"\0"
-    return b
-
-
-def read_string(
-    stream: BinaryIO, length: int, encoding: str = "ascii "
-) -> Union[str, bytes]:
-    """
-    Reads `length` bytes from the stream, and tries to decode it.
-    If the decoding succeeds, returns the `str`. Otherwise the raw bytes
-    are returned.
-    """
-    raw_string = stream.read(length)
-    first_null_byte_pos = raw_string.find(b"\0")
-    if first_null_byte_pos >= 0:
-        raw_string = raw_string[:first_null_byte_pos]
-
-    try:
-        return raw_string.decode(encoding)
-    except UnicodeDecodeError:
-        return raw_string
-
-
-def write_as_c_string(
-    stream: BinaryIO,
-    string: Union[str, bytes],
-    max_length: int,
-    encoding: str = "ascii",
-    encoding_errors: str = "strict",
-) -> bool:
-    """
-    Writes the string or bytes as a 'C' string to the stream.
-
-    A 'C' string is null terminated, so this function writes the null
-    terminator.
-
-    It will always write `max_length` bytes to the stream,
-    so the input data may be null padded or truncated.
-    """
-    raw_bytes = get_bytes_from_string(string, encoding, encoding_errors)
-    raw_bytes, was_truncated = null_pad_bytes(
-        raw_bytes, max_length, null_terminate=True
-    )
-    stream.write(raw_bytes)
-
-    return was_truncated
-
-
-def write_string(
-    stream: BinaryIO,
-    string: Union[str, bytes],
-    max_length: int,
-    encoding: str = "ascii",
-    encoding_errors: str = "strict",
-) -> bool:
-    """
-    Writes the string or bytes as a 'C' string to the stream.
-
-    Written data is not null terminated.
-
-    It will always write `max_length` bytes to the stream,
-    so the input data may be null padded or truncated.
-    """
-    raw_bytes = get_bytes_from_string(string, encoding, encoding_errors)
-    raw_bytes, was_truncated = null_pad_bytes(
-        raw_bytes, max_length, null_terminate=False
-    )
-    stream.write(raw_bytes)
-
-    return was_truncated
-
-
-def get_bytes_from_string(
-    string: Union[str, bytes], encoding: str, encoding_errors: str
-) -> bytes:
-    if isinstance(string, str):
-        raw_bytes = string.encode(encoding, errors=encoding_errors)
-    else:
-        # check that the bytes are valid for the given encoding
-        _ = string.decode(encoding, errors=encoding_errors)
-        raw_bytes = string
-
-    return raw_bytes
-
-
-def null_pad_bytes(
-    raw_bytes: bytes, max_length: int, null_terminate: bool = True
-) -> (bytes, bool):
-    """
-    Returns a byte string of `max_length` bytes.
-
-    If the input bytes is shorter then the output will be null padded.
-
-    If the input bytes is longer it will be truncated.
-
-    If null_terminate is True, then the last byte is guaranteed to be a null
-    byte (and the out string sill has `max_length` bytes).
-
-    >>> null_pad_bytes(b'abcd', 5)
-    (b'abcd\\x00', False)
-
-    # input has 4 bytes, and must be 4 bytes long
-    # but since null_terminate is True its guaranteed to be null terminated,
-    # the last byte will be truncated
-    >>> null_pad_bytes(b'abcd', 4)
-    (b'abc\\x00', True)
-
-    # Same setup, but don't null terminate
-    >>> null_pad_bytes(b'abcd', 4, null_terminate=False)
-    (b'abcd', False)
-
-    >>> null_pad_bytes(b'abcdef', 4)
-    (b'abc\\x00', True)
-
-    >>> null_pad_bytes(b'abcdef', 4, null_terminate=False)
-    (b'abcd', True)
-
-    >>> null_pad_bytes(b'abcd', 10)
-    (b'abcd\\x00\\x00\\x00\\x00\\x00\\x00', False)
-
-    >>> null_pad_bytes(b'abcdabcd', 5)
-    (b'abcd\\x00', True)
-
-    >>> null_pad_bytes(b'abcde\\x00', 8)
-    (b'abcde\\x00\\x00\\x00', False)
-
-    >>> null_pad_bytes(b'abcde\\x00z', 8)
-    (b'abcde\\x00\\x00\\x00', True)
-    """
-    was_truncated = False
-
-    null_pos = raw_bytes.find(b"\0")
-    if null_pos != -1:
-        was_truncated = null_pos != len(raw_bytes) - 1
-        raw_bytes = raw_bytes[:null_pos]
-
-    if len(raw_bytes) >= max_length + (not null_terminate):
-        raw_bytes = raw_bytes[: max_length - 1 + (not null_terminate)]
-        was_truncated = True
-
-    # This will effectively null pad
-    raw_bytes = raw_bytes.ljust(max_length, b"\0")
-
-    return raw_bytes, was_truncated
+from typing import BinaryIO, Union
+
+
+def encode_to_null_terminated(string: str, codec: str = "utf-8") -> bytes:
+    """
+    >>> encode_to_null_terminated("las files are cool")
+    b'las files are cool\\x00'
+
+    >>> encode_to_null_terminated("")
+    b'\\x00'
+    """
+    b = string.encode(codec)
+    if not b or b[-1] != 0:
+        b += b"\0"
+    return b
+
+
+def read_string(
+    stream: BinaryIO, length: int, encoding: str = "ascii "
+) -> Union[str, bytes]:
+    """
+    Reads `length` bytes from the stream, and tries to decode it.
+    If the decoding succeeds, returns the `str`. Otherwise the raw bytes
+    are returned.
+    """
+    raw_string = stream.read(length)
+    first_null_byte_pos = raw_string.find(b"\0")
+    if first_null_byte_pos >= 0:
+        raw_string = raw_string[:first_null_byte_pos]
+
+    try:
+        return raw_string.decode(encoding)
+    except UnicodeDecodeError:
+        return raw_string
+
+
+def write_as_c_string(
+    stream: BinaryIO,
+    string: Union[str, bytes],
+    max_length: int,
+    encoding: str = "ascii",
+    encoding_errors: str = "strict",
+) -> bool:
+    """
+    Writes the string or bytes as a 'C' string to the stream.
+
+    A 'C' string is null terminated, so this function writes the null
+    terminator.
+
+    It will always write `max_length` bytes to the stream,
+    so the input data may be null padded or truncated.
+    """
+    raw_bytes = get_bytes_from_string(string, encoding, encoding_errors)
+    raw_bytes, was_truncated = null_pad_bytes(
+        raw_bytes, max_length, null_terminate=True
+    )
+    stream.write(raw_bytes)
+
+    return was_truncated
+
+
+def write_string(
+    stream: BinaryIO,
+    string: Union[str, bytes],
+    max_length: int,
+    encoding: str = "ascii",
+    encoding_errors: str = "strict",
+) -> bool:
+    """
+    Writes the string or bytes as a 'C' string to the stream.
+
+    Written data is not null terminated.
+
+    It will always write `max_length` bytes to the stream,
+    so the input data may be null padded or truncated.
+    """
+    raw_bytes = get_bytes_from_string(string, encoding, encoding_errors)
+    raw_bytes, was_truncated = null_pad_bytes(
+        raw_bytes, max_length, null_terminate=False
+    )
+    stream.write(raw_bytes)
+
+    return was_truncated
+
+
+def get_bytes_from_string(
+    string: Union[str, bytes], encoding: str, encoding_errors: str
+) -> bytes:
+    if isinstance(string, str):
+        raw_bytes = string.encode(encoding, errors=encoding_errors)
+    else:
+        # check that the bytes are valid for the given encoding
+        _ = string.decode(encoding, errors=encoding_errors)
+        raw_bytes = string
+
+    return raw_bytes
+
+
+def null_pad_bytes(
+    raw_bytes: bytes, max_length: int, null_terminate: bool = True
+) -> (bytes, bool):
+    """
+    Returns a byte string of `max_length` bytes.
+
+    If the input bytes is shorter then the output will be null padded.
+
+    If the input bytes is longer it will be truncated.
+
+    If null_terminate is True, then the last byte is guaranteed to be a null
+    byte (and the out string sill has `max_length` bytes).
+
+    >>> null_pad_bytes(b'abcd', 5)
+    (b'abcd\\x00', False)
+
+    # input has 4 bytes, and must be 4 bytes long
+    # but since null_terminate is True its guaranteed to be null terminated,
+    # the last byte will be truncated
+    >>> null_pad_bytes(b'abcd', 4)
+    (b'abc\\x00', True)
+
+    # Same setup, but don't null terminate
+    >>> null_pad_bytes(b'abcd', 4, null_terminate=False)
+    (b'abcd', False)
+
+    >>> null_pad_bytes(b'abcdef', 4)
+    (b'abc\\x00', True)
+
+    >>> null_pad_bytes(b'abcdef', 4, null_terminate=False)
+    (b'abcd', True)
+
+    >>> null_pad_bytes(b'abcd', 10)
+    (b'abcd\\x00\\x00\\x00\\x00\\x00\\x00', False)
+
+    >>> null_pad_bytes(b'abcdabcd', 5)
+    (b'abcd\\x00', True)
+
+    >>> null_pad_bytes(b'abcde\\x00', 8)
+    (b'abcde\\x00\\x00\\x00', False)
+
+    >>> null_pad_bytes(b'abcde\\x00z', 8)
+    (b'abcde\\x00\\x00\\x00', True)
+    """
+    was_truncated = False
+
+    null_pos = raw_bytes.find(b"\0")
+    if null_pos != -1:
+        was_truncated = null_pos != len(raw_bytes) - 1
+        raw_bytes = raw_bytes[:null_pos]
+
+    if len(raw_bytes) >= max_length + (not null_terminate):
+        raw_bytes = raw_bytes[: max_length - 1 + (not null_terminate)]
+        was_truncated = True
+
+    # This will effectively null pad
+    raw_bytes = raw_bytes.ljust(max_length, b"\0")
+
+    return raw_bytes, was_truncated
```

### Comparing `laspy-2.4.1/laspy/vlrs/geotiff.py` & `laspy-2.5.0/laspy/vlrs/geotiff.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,251 +1,251 @@
-import logging
-import warnings
-from collections import namedtuple
-from copy import copy
-from typing import Tuple, Optional, List
-
-from . import vlrlist
-from .known import (
-    GeoAsciiParamsVlr,
-    GeoKeyDirectoryVlr,
-    GeoKeyEntryStruct,
-    GeoDoubleParamsVlr,
-)
-
-try:
-    import pyproj
-except ModuleNotFoundError:
-    pass
-
-
-logger = logging.getLogger(__name__)
-
-
-# GeoTIFF Configuration GeoKeys
-"""
-GeoTIFF defined CS Model Type Codes:
-   ModelTypeProjected   = 1   /* Projection Coordinate System         */
-   ModelTypeGeographic  = 2   /* Geographic latitude-longitude System */
-   ModelTypeGeocentric  = 3   /* Geocentric (X,Y,Z) Coordinate System */
-
-Notes:
-   1. ModelTypeGeographic and ModelTypeProjected
-      correspond to the FGDC metadata Geographic and
-      Planar-Projected coordinate system types.
-
-http://geotiff.maptools.org/spec/geotiff6.html#6.3.1.1
-"""
-ModelTypeProjected = 1
-ModelTypeGeographic = 2
-GTModelTypeGeoKey = GeoKeyEntryStruct(
-    id=1024,
-    tiff_tag_location=0,
-    count=1,
-)
-"""
-Values:
-0 => Undefined
-1 => RasterPixelIsArea
-2 => RasterPixelIsPoint
-
-http://geotiff.maptools.org/spec/geotiff6.html#6.3.1.2
-"""
-GTRasterTypeGeoKey = GeoKeyEntryStruct(
-    id=1025,
-    tiff_tag_location=0,
-    count=1,
-)
-"""
-'ASCII reference to published documentation on the overall configuration
-of this GeoTIFF file.'
-"""
-GTCitationGeoKey = GeoKeyEntryStruct(
-    id=1026,
-    tiff_tag_location=GeoAsciiParamsVlr.official_record_ids()[0],
-)
-
-# Geographic CS Parameter GeoKeys
-
-GeographicTypeGeoKey = GeoKeyEntryStruct(
-    id=2048,
-    tiff_tag_location=0,
-    count=1,
-)
-
-"""
-General citation and reference for all Geographic CS parameters.
-"""
-GeogCitationGeoKey = GeoKeyEntryStruct(
-    id=2049,
-    tiff_tag_location=GeoAsciiParamsVlr.official_record_ids()[0],
-)
-
-# Projected CS Parameter GeoKeys
-
-ProjectedCSTypeGeoKey = GeoKeyEntryStruct(
-    id=3072,
-    tiff_tag_location=0,
-    count=1,
-)
-
-"""
-'ASCII reference to published documentation on the 
-Projected Coordinate System particularly if this is a "user-defined" PCS'
-"""
-PCSCitationGeoKey = GeoKeyEntryStruct(
-    id=3073,
-    tiff_tag_location=GeoAsciiParamsVlr.official_record_ids()[0],
-)
-
-# Geographic CS Parameter GeoKeys
-
-
-def create_geotiff_projection_vlrs(
-    crs: "pyproj.CRS",
-) -> Tuple[GeoKeyDirectoryVlr, GeoAsciiParamsVlr]:
-    # 'Cookbook' from the geotiff spec
-    # http://geotiff.maptools.org/spec/geotiff2.7.html#2.7
-
-    if crs.is_projected:
-        model_key = copy(GTModelTypeGeoKey)
-        model_key.value_offset = ModelTypeProjected
-
-        epsg_code = crs.to_epsg()
-        if epsg_code is None:
-            raise RuntimeError("Projected CRS without epsg is not supported")
-
-        projected_crs_key = copy(ProjectedCSTypeGeoKey)
-        projected_crs_key.value_offset = epsg_code
-
-        # Citation Keys for which data is stored in the Ascii Param
-        pcs_citation = crs.name.encode("ascii")
-
-        ascii_params = b"|".join([pcs_citation])
-
-        pcs_citation_key = copy(PCSCitationGeoKey)
-        pcs_citation_key.value_offset = 0
-        pcs_citation_key.count = len(pcs_citation)
-
-        keys = [model_key, projected_crs_key, pcs_citation_key]
-        geo_key_vlr = GeoKeyDirectoryVlr()
-        geo_key_vlr.geo_keys_header.number_of_keys = len(keys)
-        geo_key_vlr.geo_keys = keys
-
-        ascii_vlr = GeoAsciiParamsVlr()
-        ascii_vlr.strings = [ascii_params.decode("ascii")]
-
-        return geo_key_vlr, ascii_vlr
-    if crs.is_geographic or crs.is_geocentric:
-        model_key = copy(GTModelTypeGeoKey)
-        model_key.value_offset = ModelTypeGeographic
-
-        epsg_code = crs.to_epsg()
-        if epsg_code is None:
-            raise RuntimeError("Geographic CRS without epsg is not supported")
-
-        geographic_crs_key = copy(GeographicTypeGeoKey)
-        geographic_crs_key.value_offset = epsg_code
-
-        geodetic_citation = crs.geodetic_crs.name.encode("ascii")
-        ascii_params = b"|".join([geodetic_citation])
-
-        geodetic_citation_key = copy(GeogCitationGeoKey)
-        geodetic_citation_key.value_offset = 0
-        geodetic_citation_key.count = len(geodetic_citation)
-
-        keys = [model_key, geographic_crs_key, geodetic_citation_key]
-        geo_key_vlr = GeoKeyDirectoryVlr()
-        geo_key_vlr.geo_keys_header.number_of_keys = len(keys)
-        geo_key_vlr.geo_keys = keys
-
-        ascii_vlr = GeoAsciiParamsVlr()
-        ascii_vlr.strings = [ascii_params.decode("ascii")]
-        return geo_key_vlr, ascii_vlr
-
-    else:
-        raise RuntimeError(f"CRS of type {crs.type_name} is not supported")
-
-
-GeoTiffKey = namedtuple("GeoTiffKey", ("id", "value"))
-
-
-def parse_geo_tiff_keys_from_vlrs(vlr_list: vlrlist.VLRList) -> List[GeoTiffKey]:
-    """Gets the 3 GeoTiff vlrs from the vlr_list and parse them into
-    a nicer structure
-    Parameters
-    ----------
-    vlr_list: laspy.vrls.vlrslist.VLRList list of vlrs from a las file
-    Raises
-    ------
-        IndexError if any of the needed GeoTiffVLR is not found in the list
-    Returns
-    -------
-    List of GeoTiff keys parsed from the VLRs
-    """
-    warnings.warn(
-        f"parse_geo_tiff_keys_from_vlrs is deprecated, if you want the CRS/SRS from "
-        "GeoTiff's VLR install pyproj and use `LasHead.parse_crs()`",
-        DeprecationWarning,
-    )
-    geo_key_dir = vlr_list.get_by_id(
-        GeoKeyDirectoryVlr.official_user_id(), GeoKeyDirectoryVlr.official_record_ids()
-    )[0]
-
-    try:
-        geo_doubles = vlr_list.get_by_id(
-            GeoDoubleParamsVlr.official_user_id(),
-            GeoDoubleParamsVlr.official_record_ids(),
-        )[0]
-    except IndexError:
-        geo_doubles = None
-
-    try:
-        geo_ascii = vlr_list.get_by_id(
-            GeoAsciiParamsVlr.official_user_id(),
-            GeoAsciiParamsVlr.official_record_ids(),
-        )[0]
-    except IndexError:
-        geo_ascii = None
-    return parse_geo_tiff(geo_key_dir, geo_doubles, geo_ascii)
-
-
-def parse_geo_tiff(
-    key_dir_vlr: GeoKeyDirectoryVlr,
-    double_vlr: Optional[GeoDoubleParamsVlr],
-    ascii_vlr: Optional[GeoAsciiParamsVlr],
-) -> List[GeoTiffKey]:
-    warnings.warn(
-        f"parse_geo_tiff_keys_from_vlrs is deprecated, if you want the CRS/SRS from "
-        "GeoTiff's VLR install pyproj and use `LasHead.parse_crs()`",
-        DeprecationWarning,
-    )
-    """Parses the GeoTiff VLRs information into nicer structs"""
-    geotiff_keys = []
-
-    for k in key_dir_vlr.geo_keys:
-        if k.tiff_tag_location == 0:
-            value = k.value_offset
-        elif k.tiff_tag_location == 34736:
-            if double_vlr is None:
-                raise RuntimeError(
-                    "Geotiff tag location points to GeoDoubleParams, "
-                    "but it does not exists"
-                )
-            value = double_vlr.doubles[k.value_offset]
-        elif k.tiff_tag_location == 34737:
-            if ascii_vlr is None:
-                raise RuntimeError(
-                    "Geotiff tag location points to GeoAsciiParams, "
-                    "but it does not exists"
-                )
-            value = ascii_vlr.string(k.value_offset, k.count)
-        else:
-            logger.warning(
-                "GeoTiffKey with unknown tiff tag location ({})".format(
-                    k.tiff_tag_location
-                )
-            )
-            continue
-
-        geotiff_keys.append(GeoTiffKey(k.id, value))
-    return geotiff_keys
+import logging
+import warnings
+from collections import namedtuple
+from copy import copy
+from typing import List, Optional, Tuple
+
+from . import vlrlist
+from .known import (
+    GeoAsciiParamsVlr,
+    GeoDoubleParamsVlr,
+    GeoKeyDirectoryVlr,
+    GeoKeyEntryStruct,
+)
+
+try:
+    import pyproj
+except ModuleNotFoundError:
+    pass
+
+
+logger = logging.getLogger(__name__)
+
+
+# GeoTIFF Configuration GeoKeys
+"""
+GeoTIFF defined CS Model Type Codes:
+   ModelTypeProjected   = 1   /* Projection Coordinate System         */
+   ModelTypeGeographic  = 2   /* Geographic latitude-longitude System */
+   ModelTypeGeocentric  = 3   /* Geocentric (X,Y,Z) Coordinate System */
+
+Notes:
+   1. ModelTypeGeographic and ModelTypeProjected
+      correspond to the FGDC metadata Geographic and
+      Planar-Projected coordinate system types.
+
+http://geotiff.maptools.org/spec/geotiff6.html#6.3.1.1
+"""
+ModelTypeProjected = 1
+ModelTypeGeographic = 2
+GTModelTypeGeoKey = GeoKeyEntryStruct(
+    id=1024,
+    tiff_tag_location=0,
+    count=1,
+)
+"""
+Values:
+0 => Undefined
+1 => RasterPixelIsArea
+2 => RasterPixelIsPoint
+
+http://geotiff.maptools.org/spec/geotiff6.html#6.3.1.2
+"""
+GTRasterTypeGeoKey = GeoKeyEntryStruct(
+    id=1025,
+    tiff_tag_location=0,
+    count=1,
+)
+"""
+'ASCII reference to published documentation on the overall configuration
+of this GeoTIFF file.'
+"""
+GTCitationGeoKey = GeoKeyEntryStruct(
+    id=1026,
+    tiff_tag_location=GeoAsciiParamsVlr.official_record_ids()[0],
+)
+
+# Geographic CS Parameter GeoKeys
+
+GeographicTypeGeoKey = GeoKeyEntryStruct(
+    id=2048,
+    tiff_tag_location=0,
+    count=1,
+)
+
+"""
+General citation and reference for all Geographic CS parameters.
+"""
+GeogCitationGeoKey = GeoKeyEntryStruct(
+    id=2049,
+    tiff_tag_location=GeoAsciiParamsVlr.official_record_ids()[0],
+)
+
+# Projected CS Parameter GeoKeys
+
+ProjectedCSTypeGeoKey = GeoKeyEntryStruct(
+    id=3072,
+    tiff_tag_location=0,
+    count=1,
+)
+
+"""
+'ASCII reference to published documentation on the 
+Projected Coordinate System particularly if this is a "user-defined" PCS'
+"""
+PCSCitationGeoKey = GeoKeyEntryStruct(
+    id=3073,
+    tiff_tag_location=GeoAsciiParamsVlr.official_record_ids()[0],
+)
+
+# Geographic CS Parameter GeoKeys
+
+
+def create_geotiff_projection_vlrs(
+    crs: "pyproj.CRS",
+) -> Tuple[GeoKeyDirectoryVlr, GeoAsciiParamsVlr]:
+    # 'Cookbook' from the geotiff spec
+    # http://geotiff.maptools.org/spec/geotiff2.7.html#2.7
+
+    if crs.is_projected:
+        model_key = copy(GTModelTypeGeoKey)
+        model_key.value_offset = ModelTypeProjected
+
+        epsg_code = crs.to_epsg()
+        if epsg_code is None:
+            raise RuntimeError("Projected CRS without epsg is not supported")
+
+        projected_crs_key = copy(ProjectedCSTypeGeoKey)
+        projected_crs_key.value_offset = epsg_code
+
+        # Citation Keys for which data is stored in the Ascii Param
+        pcs_citation = crs.name.encode("ascii")
+
+        ascii_params = b"|".join([pcs_citation])
+
+        pcs_citation_key = copy(PCSCitationGeoKey)
+        pcs_citation_key.value_offset = 0
+        pcs_citation_key.count = len(pcs_citation)
+
+        keys = [model_key, projected_crs_key, pcs_citation_key]
+        geo_key_vlr = GeoKeyDirectoryVlr()
+        geo_key_vlr.geo_keys_header.number_of_keys = len(keys)
+        geo_key_vlr.geo_keys = keys
+
+        ascii_vlr = GeoAsciiParamsVlr()
+        ascii_vlr.strings = [ascii_params.decode("ascii")]
+
+        return geo_key_vlr, ascii_vlr
+    if crs.is_geographic or crs.is_geocentric:
+        model_key = copy(GTModelTypeGeoKey)
+        model_key.value_offset = ModelTypeGeographic
+
+        epsg_code = crs.to_epsg()
+        if epsg_code is None:
+            raise RuntimeError("Geographic CRS without epsg is not supported")
+
+        geographic_crs_key = copy(GeographicTypeGeoKey)
+        geographic_crs_key.value_offset = epsg_code
+
+        geodetic_citation = crs.geodetic_crs.name.encode("ascii")
+        ascii_params = b"|".join([geodetic_citation])
+
+        geodetic_citation_key = copy(GeogCitationGeoKey)
+        geodetic_citation_key.value_offset = 0
+        geodetic_citation_key.count = len(geodetic_citation)
+
+        keys = [model_key, geographic_crs_key, geodetic_citation_key]
+        geo_key_vlr = GeoKeyDirectoryVlr()
+        geo_key_vlr.geo_keys_header.number_of_keys = len(keys)
+        geo_key_vlr.geo_keys = keys
+
+        ascii_vlr = GeoAsciiParamsVlr()
+        ascii_vlr.strings = [ascii_params.decode("ascii")]
+        return geo_key_vlr, ascii_vlr
+
+    else:
+        raise RuntimeError(f"CRS of type {crs.type_name} is not supported")
+
+
+GeoTiffKey = namedtuple("GeoTiffKey", ("id", "value"))
+
+
+def parse_geo_tiff_keys_from_vlrs(vlr_list: vlrlist.VLRList) -> List[GeoTiffKey]:
+    """Gets the 3 GeoTiff vlrs from the vlr_list and parse them into
+    a nicer structure
+    Parameters
+    ----------
+    vlr_list: laspy.vrls.vlrslist.VLRList list of vlrs from a las file
+    Raises
+    ------
+        IndexError if any of the needed GeoTiffVLR is not found in the list
+    Returns
+    -------
+    List of GeoTiff keys parsed from the VLRs
+    """
+    warnings.warn(
+        f"parse_geo_tiff_keys_from_vlrs is deprecated, if you want the CRS/SRS from "
+        "GeoTiff's VLR install pyproj and use `LasHead.parse_crs()`",
+        DeprecationWarning,
+    )
+    geo_key_dir = vlr_list.get_by_id(
+        GeoKeyDirectoryVlr.official_user_id(), GeoKeyDirectoryVlr.official_record_ids()
+    )[0]
+
+    try:
+        geo_doubles = vlr_list.get_by_id(
+            GeoDoubleParamsVlr.official_user_id(),
+            GeoDoubleParamsVlr.official_record_ids(),
+        )[0]
+    except IndexError:
+        geo_doubles = None
+
+    try:
+        geo_ascii = vlr_list.get_by_id(
+            GeoAsciiParamsVlr.official_user_id(),
+            GeoAsciiParamsVlr.official_record_ids(),
+        )[0]
+    except IndexError:
+        geo_ascii = None
+    return parse_geo_tiff(geo_key_dir, geo_doubles, geo_ascii)
+
+
+def parse_geo_tiff(
+    key_dir_vlr: GeoKeyDirectoryVlr,
+    double_vlr: Optional[GeoDoubleParamsVlr],
+    ascii_vlr: Optional[GeoAsciiParamsVlr],
+) -> List[GeoTiffKey]:
+    warnings.warn(
+        f"parse_geo_tiff_keys_from_vlrs is deprecated, if you want the CRS/SRS from "
+        "GeoTiff's VLR install pyproj and use `LasHead.parse_crs()`",
+        DeprecationWarning,
+    )
+    """Parses the GeoTiff VLRs information into nicer structs"""
+    geotiff_keys = []
+
+    for k in key_dir_vlr.geo_keys:
+        if k.tiff_tag_location == 0:
+            value = k.value_offset
+        elif k.tiff_tag_location == 34736:
+            if double_vlr is None:
+                raise RuntimeError(
+                    "Geotiff tag location points to GeoDoubleParams, "
+                    "but it does not exists"
+                )
+            value = double_vlr.doubles[k.value_offset]
+        elif k.tiff_tag_location == 34737:
+            if ascii_vlr is None:
+                raise RuntimeError(
+                    "Geotiff tag location points to GeoAsciiParams, "
+                    "but it does not exists"
+                )
+            value = ascii_vlr.string(k.value_offset, k.count)
+        else:
+            logger.warning(
+                "GeoTiffKey with unknown tiff tag location ({})".format(
+                    k.tiff_tag_location
+                )
+            )
+            continue
+
+        geotiff_keys.append(GeoTiffKey(k.id, value))
+    return geotiff_keys
```

### Comparing `laspy-2.4.1/laspy/vlrs/known.py` & `laspy-2.5.0/laspy/vlrs/known.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,692 +1,696 @@
-""" The definition of the VLR Header, VLR, the KnownVLRs
- are in this module.
-
- A KnownVLR is a VLR for which we know how to parse its record_data
-"""
-import abc
-import ctypes
-import logging
-import struct
-from typing import List, Optional, Any, Tuple, Dict, TypeVar, Type
-from copy import copy
-
-import numpy as np
-
-from .vlr import BaseVLR, VLR
-from ..extradims import (
-    get_dtype_for_extra_dim,
-)
-from ..point.format import ExtraBytesParams
-from ..utils import encode_to_null_terminated
-
-abstractmethod = abc.abstractmethod
-
-logger = logging.getLogger(__name__)
-
-NULL_BYTE = b"\0"
-
-
-GeoKeyDirectoryType = TypeVar("GeoKeyDirectoryType", bound="GeoKeyDirectoryVlr")
-GeoAsciiParamsType = TypeVar("GeoAsciiParamsType", bound="GeoAsciiParamsVlr")
-
-
-class IKnownVLR(abc.ABC):
-    """Interface that any KnownVLR must implement.
-    A KnownVLR is a VLR for which we know how to parse its record_data
-
-    Implementing this interfaces allows to automatically call the
-    right parser for the right VLR when reading them.
-    """
-
-    @staticmethod
-    @abstractmethod
-    def official_user_id() -> str:
-        """Shall return the official user_id as described in the documentation"""
-        pass
-
-    @staticmethod
-    @abstractmethod
-    def official_record_ids() -> Tuple[int, ...]:
-        """Shall return the official record_id for the VLR
-
-        .. note::
-
-            Even if the VLR has one record_id, the return type must be a tuple
-
-        Returns
-        -------
-        tuple of int
-            The record_ids this VLR type can have
-        """
-        pass
-
-    @abstractmethod
-    def record_data_bytes(self) -> bytes:
-        """Shall return the bytes corresponding to the record_data part of the VLR
-        as they should be written in the file.
-
-        Returns
-        -------
-        bytes
-            The bytes of the vlr's record_data
-
-        """
-        pass
-
-    @abstractmethod
-    def parse_record_data(self, record_data: bytes) -> None:
-        """Shall parse the given record_data into a user-friendlier structure
-
-        Parameters
-        ----------
-        record_data: bytes
-            The record_data bytes read from the file
-
-        """
-        pass
-
-
-class BaseKnownVLR(BaseVLR, IKnownVLR, abc.ABC):
-    """Base Class to factorize common code between the different type of Known VLRs"""
-
-    def __init__(self, record_id=None, description=""):
-        super().__init__(
-            self.official_user_id(),
-            self.official_record_ids()[0] if record_id is None else record_id,
-            description,
-        )
-
-    @classmethod
-    def from_raw(cls, raw: VLR):
-        know_vlr = cls()
-        know_vlr._description = raw.description
-        know_vlr.parse_record_data(raw.record_data)
-        return know_vlr
-
-
-class ClassificationLookupVlr(BaseKnownVLR):
-    """This vlr maps class numbers to short descriptions / names
-
-    >>> lookup = ClassificationLookupVlr()
-    >>> lookup[0] = "never_classified"
-    >>> lookup[2] = "ground"
-    >>> lookup[0]
-    'never_classified'
-    """
-
-    _lookup_struct = struct.Struct("<B15s")
-
-    def __init__(self):
-        super().__init__(description="Classification Lookup")
-        self.lookups: Dict[int, str] = {}
-
-    def parse_record_data(self, record_data: bytes) -> None:
-        for class_id, desc in struct.iter_unpack("<B15s", record_data):
-            # index using desc[i:i+1], because desc[i] gives an int, and we want a byte
-            description = b"".join(
-                desc[i : i + 1]
-                for i in range(len(desc))
-                if desc[i : i + 1].isalnum() or desc[i : i + 1] == b" "
-            ).decode()
-            self.lookups[class_id] = description
-
-    def record_data_bytes(self) -> bytes:
-        def lookup_converter(lookup_dict):
-            for class_id, description in lookup_dict.items():
-                description_bytes = description.encode("ascii")
-                if len(description_bytes) > 15:
-                    raise ValueError(
-                        "decription ({}) is to long ({} bytes), it must not exceed 15 bytes when encoded".format(
-                            description, len(description_bytes)
-                        )
-                    )
-                yield class_id, description_bytes
-
-        return b"".join(
-            self._lookup_struct.pack(class_id, desc)
-            for class_id, desc in lookup_converter(self.lookups)
-        )
-
-    def __getitem__(self, class_id: int) -> str:
-        return self.lookups[class_id]
-
-    def __setitem__(self, class_id: int, description: str):
-        if class_id not in range(256):
-            raise ValueError("Class id {} is not in range [0, 255]".format(class_id))
-
-        self.lookups[class_id] = description
-
-    @staticmethod
-    def official_user_id() -> str:
-        return "LASF_Spec"
-
-    @staticmethod
-    def official_record_ids() -> Tuple[int, ...]:
-        return (0,)
-
-
-class LasZipVlr(BaseKnownVLR):
-    """Contains the information needed by laszip (or any other laz backend)
-    to compress the point records.
-    """
-
-    def __init__(self, data: bytes) -> None:
-        super().__init__(description="http://laszip.org")
-        self.record_data = data
-
-    def parse_record_data(self, record_data: bytes) -> None:
-        # Only laz backends know how to parse this
-        pass
-
-    def record_data_bytes(self) -> bytes:
-        return self.record_data
-
-    @staticmethod
-    def official_user_id() -> str:
-        return "laszip encoded"
-
-    @staticmethod
-    def official_record_ids() -> Tuple[int, ...]:
-        return (22204,)
-
-    @classmethod
-    def from_raw(cls, raw_vlr):
-        return cls(raw_vlr.record_data)
-
-
-class ExtraBytesStruct(ctypes.LittleEndianStructure):
-    _pack_ = 1
-    _fields_ = [
-        ("reserved", ctypes.c_uint8 * 2),
-        ("data_type", ctypes.c_uint8),
-        ("options", ctypes.c_uint8),
-        ("name", ctypes.c_char * 32),
-        ("unused", ctypes.c_uint8 * 4),
-        ("_no_data", (ctypes.c_byte * 8) * 3),
-        ("_min", (ctypes.c_byte * 8) * 3),
-        ("_max", (ctypes.c_byte * 8) * 3),
-        ("_scale", ctypes.c_double * 3),
-        ("_offset", ctypes.c_double * 3),
-        ("description", ctypes.c_char * 32),
-    ]
-
-    _uint64t_struct = struct.Struct("<Q")
-    _int64t_struct = struct.Struct("<q")
-    _double_struct = struct.Struct("<d")
-
-    NO_DATA_BIT_MASK = 0b000_0001
-    MIN_BIT_MASK = 0b0000_0010
-    MAX_BIT_MASK = 0b0000_0100
-    SCALE_BIT_MASK = 0b000_1000
-    OFFSET_BIT_MASK = 0b0001_0000
-
-    def _parse_special_property(self, name) -> np.ndarray:
-        return np.frombuffer(getattr(self, name), dtype=self.dtype())
-
-    @property
-    def no_data(self):
-        return self._parse_special_property("_no_data")
-
-    @property
-    def min(self):
-        return self._parse_special_property("_min")
-
-    @property
-    def max(self):
-        return self._parse_special_property("_max")
-
-    @property
-    def offset(self) -> Optional[Any]:
-        if self.options & self.OFFSET_BIT_MASK != 0:
-            return self._offset
-        return None
-
-    @offset.setter
-    def offset(self, value):
-        if value is None:
-            self.options &= ~self.OFFSET_BIT_MASK
-        else:
-            num_elements = self.num_elements()
-            self._offset[:num_elements] = value[:num_elements]
-            self.options |= self.OFFSET_BIT_MASK
-
-    @property
-    def scale(self):
-        if self.options & self.SCALE_BIT_MASK != 0:
-            return self._scale
-        return None
-
-    @scale.setter
-    def scale(self, value):
-        if value is None:
-            self.options &= ~self.SCALE_BIT_MASK
-        else:
-            num_elements = self.num_elements()
-            self._scale[:num_elements] = value[:num_elements]
-            self.options |= self.SCALE_BIT_MASK
-
-    def format_name(self):
-        return self.name.rstrip(NULL_BYTE).decode()
-
-    def dtype(self) -> np.dtype:
-        if self.data_type == 0:
-            if self.options == 1:
-                # numpy says doing '1u1' is deprecated
-                return np.dtype("u1")
-            return np.dtype(f"{self.options}u1")
-        return get_dtype_for_extra_dim(self.data_type)
-
-    def num_elements(self) -> int:
-        if self.data_type == 0:
-            return self.options
-        elif self.data_type <= 10:
-            return 1
-        elif self.data_type <= 20:
-            return 2
-        else:
-            return 3
-
-    @staticmethod
-    def size():
-        return ctypes.sizeof(ExtraBytesStruct)
-
-    def __repr__(self):
-        return "<ExtraBytesStruct({}, {}, {})>".format(
-            self.format_name(), self.data_type, self.description
-        )
-
-
-class ExtraBytesVlr(BaseKnownVLR):
-    def __init__(self):
-        super().__init__(description="Extra Bytes Record")
-        self.extra_bytes_structs: List[ExtraBytesStruct] = []
-
-    def parse_record_data(self, data):
-        if (len(data) % ExtraBytesStruct.size()) != 0:
-            raise ValueError(
-                "Data length of ExtraBytes vlr must be a multiple of {}".format(
-                    ExtraBytesStruct.size()
-                )
-            )
-        num_extra_bytes_structs = len(data) // ExtraBytesStruct.size()
-        self.extra_bytes_structs = [None] * num_extra_bytes_structs
-        for i in range(num_extra_bytes_structs):
-            self.extra_bytes_structs[i] = ExtraBytesStruct.from_buffer_copy(
-                data[ExtraBytesStruct.size() * i : ExtraBytesStruct.size() * (i + 1)]
-            )
-
-    def record_data_bytes(self):
-        return b"".join(
-            bytes(extra_struct) for extra_struct in self.extra_bytes_structs
-        )
-
-    def type_of_extra_dims(self) -> List[ExtraBytesParams]:
-        dim_info_list: List[ExtraBytesParams] = []
-        for eb_struct in self.extra_bytes_structs:
-            num_elements = eb_struct.num_elements()
-
-            scales = eb_struct.scale
-            offsets = eb_struct.offset
-
-            if scales is not None or offsets is not None:
-                # If one of scales or offsets is defined,
-                # we expect the other to be as well
-                # so set default scales or offsets
-                if offsets is None:
-                    offsets = np.zeros(num_elements, np.float64)
-                else:
-                    offsets = np.array(offsets[:num_elements])
-
-                if scales is None:
-                    scales = np.ones(num_elements, np.float64)
-                else:
-                    scales = np.array(scales[:num_elements])
-
-            dim_info_list.append(
-                ExtraBytesParams(
-                    eb_struct.format_name(),
-                    eb_struct.dtype(),
-                    description=eb_struct.description.rstrip(NULL_BYTE).decode(),
-                    scales=scales,
-                    offsets=offsets,
-                )
-            )
-        return dim_info_list
-
-    def __repr__(self):
-        return "<ExtraBytesVlr(extra bytes structs: {})>".format(
-            len(self.extra_bytes_structs)
-        )
-
-    @staticmethod
-    def official_user_id():
-        return "LASF_Spec"
-
-    @staticmethod
-    def official_record_ids():
-        return (4,)
-
-
-class WaveformPacketStruct(ctypes.LittleEndianStructure):
-    _pack_ = 1
-    _fields_ = [
-        ("bits_per_sample", ctypes.c_ubyte),
-        ("waveform_compression_type", ctypes.c_ubyte),
-        ("number_of_samples", ctypes.c_uint32),
-        ("temporal_sample_spacing", ctypes.c_uint32),
-        ("digitizer_gain", ctypes.c_double),
-        ("digitizer_offset", ctypes.c_double),
-    ]
-
-    @staticmethod
-    def size():
-        return ctypes.sizeof(WaveformPacketStruct)
-
-
-class WaveformPacketVlr(BaseKnownVLR):
-    def __init__(self, record_id, description=""):
-        super().__init__(record_id=record_id, description=description)
-        self.parsed_record = None
-
-    def parse_record_data(self, record_data):
-        self.parsed_record = WaveformPacketStruct.from_buffer_copy(record_data)
-
-    def record_data_bytes(self):
-        return bytes(self.parsed_record)
-
-    @staticmethod
-    def official_record_ids():
-        return range(100, 356)
-
-    @staticmethod
-    def official_user_id():
-        return "LASF_Spec"
-
-    @classmethod
-    def from_raw(cls, raw_vlr):
-        vlr = cls(
-            raw_vlr.header.record_id, description=raw_vlr.header.description.decode()
-        )
-        vlr.description = raw_vlr.header.description
-        vlr.parse_record_data(raw_vlr.record_data)
-        return vlr
-
-
-class GeoKeyEntryStruct(ctypes.LittleEndianStructure):
-    _pack_ = 1
-    _fields_ = [
-        # Id of the key
-        #
-        # Ids are broken down in sub domains:
-        # [    0,  1023]       Reserved
-        # [ 1024,  2047]       GeoTIFF Configuration Keys
-        # [ 2048,  3071]       Geographic/Geocentric CS Parameter Keys
-        # [ 3072,  4095]       Projected CS Parameter Keys
-        # [ 4096,  5119]       Vertical CS Parameter Keys
-        # [ 5120, 32767]       Reserved
-        # [32768, 65535]       Private use
-        ("id", ctypes.c_uint16),
-        # Where to find the data for the key:
-        # 0 => The _actual_ value is stored directly in the "value_offset" member
-        # Otherwise, the tiff tag location is the record_id of the VLR in which the value is stored.
-        # In the case of LAS files the 2 possible values are `34736`, `34737`.
-        ("tiff_tag_location", ctypes.c_uint16),
-        # Number of values in the key.
-        # Implied to be `1` if `tiff_tag_location` is 0
-        ("count", ctypes.c_uint16),
-        # Depending on `tiff_tag_location`, this contains either
-        # the value itself _or_ the offset in the record_data of the containing VLR
-        ("value_offset", ctypes.c_uint16),
-    ]
-
-    @staticmethod
-    def size():
-        return ctypes.sizeof(GeoKeysHeaderStructs)
-
-    def __repr__(self):
-        return "<GeoKey(Id: {}, Location: {}, count: {}, offset: {})>".format(
-            self.id, self.tiff_tag_location, self.count, self.value_offset
-        )
-
-
-class GeoKeysHeaderStructs(ctypes.LittleEndianStructure):
-    _pack_ = 1
-    _fields_ = [
-        ("key_directory_version", ctypes.c_uint16),
-        ("key_revision", ctypes.c_uint16),
-        ("minor_revision", ctypes.c_uint16),
-        ("number_of_keys", ctypes.c_uint16),
-    ]
-
-    def __init__(self):
-        super().__init__(
-            key_directory_version=1, key_revision=1, minor_revision=0, number_of_keys=0
-        )
-
-    @staticmethod
-    def size():
-        return ctypes.sizeof(GeoKeysHeaderStructs)
-
-    def __repr__(self):
-        return "<GeoKeysHeader(vers: {}, rev:{}, minor: {}, num_keys: {})>".format(
-            self.key_directory_version,
-            self.key_revision,
-            self.minor_revision,
-            self.number_of_keys,
-        )
-
-
-class GeoKeyDirectoryVlr(BaseKnownVLR):
-    def __init__(self):
-        super().__init__(description="GeoTIFF GeoKeyDirectoryTag")
-        self.geo_keys_header = GeoKeysHeaderStructs()
-        self.geo_keys = [GeoKeyEntryStruct()]
-
-    def parse_record_data(self, record_data):
-        record_data = bytearray(record_data)
-        header_data = record_data[: ctypes.sizeof(GeoKeysHeaderStructs)]
-        self.geo_keys_header = GeoKeysHeaderStructs.from_buffer(header_data)
-        self.geo_keys = []
-        keys_data = record_data[GeoKeysHeaderStructs.size() :]
-        num_keys = (
-            len(record_data[GeoKeysHeaderStructs.size() :]) // GeoKeyEntryStruct.size()
-        )
-        if num_keys != self.geo_keys_header.number_of_keys:
-            self.geo_keys_header.number_of_keys = num_keys
-
-        for i in range(self.geo_keys_header.number_of_keys):
-            data = keys_data[
-                (i * GeoKeyEntryStruct.size()) : (i + 1) * GeoKeyEntryStruct.size()
-            ]
-            self.geo_keys.append(GeoKeyEntryStruct.from_buffer(data))
-
-    def record_data_bytes(self):
-        b = bytes(self.geo_keys_header)
-        b += b"".join(map(bytes, self.geo_keys))
-        return b
-
-    def parse_crs(self):
-        import pyproj
-
-        # TODO import is done here to avoid cyclic import,
-        # this should probably be fixed
-        from .geotiff import ProjectedCSTypeGeoKey, GeographicTypeGeoKey
-
-        geographic_cs = None
-        projected_cs = None
-        for key in self.geo_keys:
-            if key.id == ProjectedCSTypeGeoKey.id:
-                projected_cs = pyproj.CRS.from_epsg(key.value_offset)
-            elif key.id == GeographicTypeGeoKey.id:
-                geographic_cs = pyproj.CRS.from_epsg(key.value_offset)
-
-        # Projected Coordinate Systems take precedence since,
-        # if they are present, the Geographic CS is probably
-        # redundant and the positioning information in the LAS
-        # file is projected.
-        return projected_cs or geographic_cs
-
-    def __repr__(self):
-        return "<{}({} geo_keys)>".format(self.__class__.__name__, len(self.geo_keys))
-
-    @staticmethod
-    def official_user_id():
-        return "LASF_Projection"
-
-    @staticmethod
-    def official_record_ids():
-        return (34735,)
-
-
-class GeoDoubleParamsVlr(BaseKnownVLR):
-    """
-    Stores all of the `double` valued GeoKeys.
-    """
-
-    def __init__(self):
-        super().__init__(description="GeoTIFF GeoDoubleParamsTag")
-        self.doubles = []
-
-    def parse_record_data(self, record_data):
-        sizeof_double = ctypes.sizeof(ctypes.c_double)
-        if len(record_data) % sizeof_double != 0:
-            raise ValueError(
-                "GeoDoubleParams record data length () is not a multiple of sizeof(double) ()".format(
-                    len(record_data), sizeof_double
-                )
-            )
-        record_data = bytearray(record_data)
-        num_doubles = len(record_data) // sizeof_double
-        for i in range(num_doubles):
-            b = record_data[i * sizeof_double : (i + 1) * sizeof_double]
-            self.doubles.append(ctypes.c_double.from_buffer(b))
-
-    def record_data_bytes(self):
-        return b"".join(map(bytes, self.doubles))
-
-    def __repr__(self):
-        return "<GeoDoubleParamsVlr({})>".format(self.doubles)
-
-    @staticmethod
-    def official_user_id():
-        return "LASF_Projection"
-
-    @staticmethod
-    def official_record_ids():
-        return (34736,)
-
-
-class GeoAsciiParamsVlr(BaseKnownVLR):
-    """
-    Stores all of the `ASCII` valued GeoKeys.
-
-    From GeoTIFF's spec:
-    To avoid problems with naive tiff dump programs the separator between geokeys is not
-    the null-terminator `\0` but `|`.
-
-    """
-
-    def __init__(self):
-        super().__init__(description="GeoTIFF GeoAsciiParamsTag")
-        self.strings = []
-
-    def parse_record_data(self, record_data):
-        self.strings = [s.decode("ascii") for s in record_data.split(NULL_BYTE)]
-        self.rd = record_data
-
-    def record_data_bytes(self):
-        return NULL_BYTE.join(s.encode("ascii") for s in self.strings)
-
-    def __repr__(self):
-        return "<GeoAsciiParamsVlr({})>".format(self.strings)
-
-    @staticmethod
-    def official_user_id():
-        return "LASF_Projection"
-
-    @staticmethod
-    def official_record_ids():
-        return (34737,)
-
-
-class WktMathTransformVlr(BaseKnownVLR):
-    """
-    From the Spec:
-        Note that the math transform WKT record is added for completeness, and a coordinate system WKT
-        may or may not require a math transform WKT record
-
-    """
-
-    def __init__(self):
-        super().__init__(description="")
-        self.string = ""
-
-    def _encode_string(self):
-        return encode_to_null_terminated(self.string, codec="utf-8")
-
-    def parse_record_data(self, record_data):
-        self.string = record_data.decode("utf-8").rstrip("\0")
-
-    def record_data_bytes(self):
-        return self._encode_string()
-
-    @staticmethod
-    def official_user_id():
-        return "LASF_Projection"
-
-    @staticmethod
-    def official_record_ids():
-        return (2111,)
-
-
-class WktCoordinateSystemVlr(BaseKnownVLR):
-    """Replaces Coordinates Reference System for new las files (point fmt >= 5)
-    "LAS is not using the “ESRI WKT”
-    """
-
-    def __init__(self, wkt_string=""):
-        super().__init__(description="OGC Transformation Record")
-        self.string = wkt_string
-
-    def _encode_string(self):
-        return encode_to_null_terminated(self.string, codec="utf-8")
-
-    def parse_record_data(self, record_data):
-        self.string = record_data.decode("utf-8").rstrip("\0")
-
-    def record_data_bytes(self):
-        return self._encode_string()
-
-    def parse_crs(self):
-        import pyproj
-
-        return pyproj.CRS.from_wkt(self.string)
-
-    @staticmethod
-    def official_user_id():
-        return "LASF_Projection"
-
-    @staticmethod
-    def official_record_ids():
-        return (2112,)
-
-
-def vlr_factory(vlr: VLR):
-    """Given a vlr tries to find its corresponding KnownVLR class
-    that can parse its data.
-    If no KnownVLR implementation is found, returns the input vlr unchanged
-    """
-    user_id = vlr.user_id
-    known_vlrs = BaseKnownVLR.__subclasses__()
-    for known_vlr in known_vlrs:
-        if (
-            known_vlr.official_user_id() == user_id
-            and vlr.record_id in known_vlr.official_record_ids()
-        ):
-            try:
-                return known_vlr.from_raw(vlr)
-            except Exception as err:
-                logger.warning(f"Failed to parse {known_vlr}: {err}")
-                return vlr
-
-    return vlr
+""" The definition of the VLR Header, VLR, the KnownVLRs
+ are in this module.
+
+ A KnownVLR is a VLR for which we know how to parse its record_data
+"""
+import abc
+import ctypes
+import logging
+import struct
+from copy import copy
+from typing import Any, Dict, List, Optional, Tuple, Type, TypeVar
+
+import numpy as np
+
+from ..extradims import get_dtype_for_extra_dim
+from ..point.format import ExtraBytesParams
+from ..utils import encode_to_null_terminated
+from .vlr import VLR, BaseVLR
+
+abstractmethod = abc.abstractmethod
+
+logger = logging.getLogger(__name__)
+
+NULL_BYTE = b"\0"
+
+
+GeoKeyDirectoryType = TypeVar("GeoKeyDirectoryType", bound="GeoKeyDirectoryVlr")
+GeoAsciiParamsType = TypeVar("GeoAsciiParamsType", bound="GeoAsciiParamsVlr")
+
+
+class IKnownVLR(abc.ABC):
+    """Interface that any KnownVLR must implement.
+    A KnownVLR is a VLR for which we know how to parse its record_data
+
+    Implementing this interfaces allows to automatically call the
+    right parser for the right VLR when reading them.
+    """
+
+    @staticmethod
+    @abstractmethod
+    def official_user_id() -> str:
+        """Shall return the official user_id as described in the documentation"""
+        pass
+
+    @staticmethod
+    @abstractmethod
+    def official_record_ids() -> Tuple[int, ...]:
+        """Shall return the official record_id for the VLR
+
+        .. note::
+
+            Even if the VLR has one record_id, the return type must be a tuple
+
+        Returns
+        -------
+        tuple of int
+            The record_ids this VLR type can have
+        """
+        pass
+
+    @abstractmethod
+    def record_data_bytes(self) -> bytes:
+        """Shall return the bytes corresponding to the record_data part of the VLR
+        as they should be written in the file.
+
+        Returns
+        -------
+        bytes
+            The bytes of the vlr's record_data
+
+        """
+        pass
+
+    @abstractmethod
+    def parse_record_data(self, record_data: bytes) -> None:
+        """Shall parse the given record_data into a user-friendlier structure
+
+        Parameters
+        ----------
+        record_data: bytes
+            The record_data bytes read from the file
+
+        """
+        pass
+
+
+class BaseKnownVLR(BaseVLR, IKnownVLR, abc.ABC):
+    """Base Class to factorize common code between the different type of Known VLRs"""
+
+    def __init__(self, record_id=None, description=""):
+        super().__init__(
+            self.official_user_id(),
+            self.official_record_ids()[0] if record_id is None else record_id,
+            description,
+        )
+
+    @classmethod
+    def from_raw(cls, raw: VLR):
+        know_vlr = cls()
+        know_vlr._description = raw.description
+        know_vlr.parse_record_data(raw.record_data)
+        return know_vlr
+
+
+class ClassificationLookupVlr(BaseKnownVLR):
+    """This vlr maps class numbers to short descriptions / names
+
+    >>> lookup = ClassificationLookupVlr()
+    >>> lookup[0] = "never_classified"
+    >>> lookup[2] = "ground"
+    >>> lookup[0]
+    'never_classified'
+    """
+
+    _lookup_struct = struct.Struct("<B15s")
+
+    def __init__(self):
+        super().__init__(description="Classification Lookup")
+        self.lookups: Dict[int, str] = {}
+
+    def parse_record_data(self, record_data: bytes) -> None:
+        for class_id, desc in struct.iter_unpack("<B15s", record_data):
+            # index using desc[i:i+1], because desc[i] gives an int, and we want a byte
+            description = b"".join(
+                desc[i : i + 1]
+                for i in range(len(desc))
+                if desc[i : i + 1].isalnum() or desc[i : i + 1] == b" "
+            ).decode()
+            self.lookups[class_id] = description
+
+    def record_data_bytes(self) -> bytes:
+        def lookup_converter(lookup_dict):
+            for class_id, description in lookup_dict.items():
+                description_bytes = description.encode("ascii")
+                if len(description_bytes) > 15:
+                    raise ValueError(
+                        "decription ({}) is to long ({} bytes), it must not exceed 15 bytes when encoded".format(
+                            description, len(description_bytes)
+                        )
+                    )
+                yield class_id, description_bytes
+
+        return b"".join(
+            self._lookup_struct.pack(class_id, desc)
+            for class_id, desc in lookup_converter(self.lookups)
+        )
+
+    def __getitem__(self, class_id: int) -> str:
+        return self.lookups[class_id]
+
+    def __setitem__(self, class_id: int, description: str):
+        if class_id not in range(256):
+            raise ValueError("Class id {} is not in range [0, 255]".format(class_id))
+
+        self.lookups[class_id] = description
+
+    @staticmethod
+    def official_user_id() -> str:
+        return "LASF_Spec"
+
+    @staticmethod
+    def official_record_ids() -> Tuple[int, ...]:
+        return (0,)
+
+
+class LasZipVlr(BaseKnownVLR):
+    """Contains the information needed by laszip (or any other laz backend)
+    to compress the point records.
+    """
+
+    def __init__(self, data: bytes) -> None:
+        super().__init__(description="http://laszip.org")
+        self.record_data = data
+
+    def parse_record_data(self, record_data: bytes) -> None:
+        # Only laz backends know how to parse this
+        pass
+
+    def record_data_bytes(self) -> bytes:
+        return self.record_data
+
+    @staticmethod
+    def official_user_id() -> str:
+        return "laszip encoded"
+
+    @staticmethod
+    def official_record_ids() -> Tuple[int, ...]:
+        return (22204,)
+
+    @classmethod
+    def from_raw(cls, raw_vlr):
+        return cls(raw_vlr.record_data)
+
+
+class ExtraBytesStruct(ctypes.LittleEndianStructure):
+    _pack_ = 1
+    _fields_ = [
+        ("reserved", ctypes.c_uint8 * 2),
+        ("data_type", ctypes.c_uint8),
+        ("options", ctypes.c_uint8),
+        ("name", ctypes.c_char * 32),
+        ("unused", ctypes.c_uint8 * 4),
+        ("_no_data", (ctypes.c_byte * 8) * 3),
+        ("_min", (ctypes.c_byte * 8) * 3),
+        ("_max", (ctypes.c_byte * 8) * 3),
+        ("_scale", ctypes.c_double * 3),
+        ("_offset", ctypes.c_double * 3),
+        ("description", ctypes.c_char * 32),
+    ]
+
+    _uint64t_struct = struct.Struct("<Q")
+    _int64t_struct = struct.Struct("<q")
+    _double_struct = struct.Struct("<d")
+
+    NO_DATA_BIT_MASK = 0b000_0001
+    MIN_BIT_MASK = 0b0000_0010
+    MAX_BIT_MASK = 0b0000_0100
+    SCALE_BIT_MASK = 0b000_1000
+    OFFSET_BIT_MASK = 0b0001_0000
+
+    def _parse_special_property(self, name) -> np.ndarray:
+        return np.frombuffer(getattr(self, name), dtype=self.dtype())
+
+    @property
+    def no_data(self):
+        return self._parse_special_property("_no_data")
+
+    @property
+    def min(self):
+        return self._parse_special_property("_min")
+
+    @property
+    def max(self):
+        return self._parse_special_property("_max")
+
+    @property
+    def offset(self) -> Optional[Any]:
+        if self.options & self.OFFSET_BIT_MASK != 0:
+            return self._offset
+        return None
+
+    @offset.setter
+    def offset(self, value):
+        if value is None:
+            self.options &= ~self.OFFSET_BIT_MASK
+        else:
+            num_elements = self.num_elements()
+            self._offset[:num_elements] = value[:num_elements]
+            self.options |= self.OFFSET_BIT_MASK
+
+    @property
+    def scale(self):
+        if self.options & self.SCALE_BIT_MASK != 0:
+            return self._scale
+        return None
+
+    @scale.setter
+    def scale(self, value):
+        if value is None:
+            self.options &= ~self.SCALE_BIT_MASK
+        else:
+            num_elements = self.num_elements()
+            self._scale[:num_elements] = value[:num_elements]
+            self.options |= self.SCALE_BIT_MASK
+
+    def format_name(self):
+        return self.name.rstrip(NULL_BYTE).decode()
+
+    def dtype(self) -> np.dtype:
+        if self.data_type == 0:
+            if self.options == 1:
+                # numpy says doing '1u1' is deprecated
+                return np.dtype("u1")
+            return np.dtype(f"{self.options}u1")
+        return get_dtype_for_extra_dim(self.data_type)
+
+    def num_elements(self) -> int:
+        if self.data_type == 0:
+            return self.options
+        elif self.data_type <= 10:
+            return 1
+        elif self.data_type <= 20:
+            return 2
+        else:
+            return 3
+
+    @staticmethod
+    def size():
+        return ctypes.sizeof(ExtraBytesStruct)
+
+    def __repr__(self):
+        return "<ExtraBytesStruct({}, {}, {})>".format(
+            self.format_name(), self.data_type, self.description
+        )
+
+
+class ExtraBytesVlr(BaseKnownVLR):
+    def __init__(self):
+        super().__init__(description="Extra Bytes Record")
+        self.extra_bytes_structs: List[ExtraBytesStruct] = []
+
+    def parse_record_data(self, data):
+        if (len(data) % ExtraBytesStruct.size()) != 0:
+            raise ValueError(
+                "Data length of ExtraBytes vlr must be a multiple of {}".format(
+                    ExtraBytesStruct.size()
+                )
+            )
+        num_extra_bytes_structs = len(data) // ExtraBytesStruct.size()
+        self.extra_bytes_structs = [None] * num_extra_bytes_structs
+        for i in range(num_extra_bytes_structs):
+            self.extra_bytes_structs[i] = ExtraBytesStruct.from_buffer_copy(
+                data[ExtraBytesStruct.size() * i : ExtraBytesStruct.size() * (i + 1)]
+            )
+
+    def record_data_bytes(self):
+        return b"".join(
+            bytes(extra_struct) for extra_struct in self.extra_bytes_structs
+        )
+
+    def type_of_extra_dims(self) -> List[ExtraBytesParams]:
+        dim_info_list: List[ExtraBytesParams] = []
+        for eb_struct in self.extra_bytes_structs:
+            num_elements = eb_struct.num_elements()
+
+            scales = eb_struct.scale
+            offsets = eb_struct.offset
+
+            if scales is not None or offsets is not None:
+                # If one of scales or offsets is defined,
+                # we expect the other to be as well
+                # so set default scales or offsets
+                if offsets is None:
+                    offsets = np.zeros(num_elements, np.float64)
+                else:
+                    offsets = np.array(offsets[:num_elements])
+
+                if scales is None:
+                    scales = np.ones(num_elements, np.float64)
+                else:
+                    scales = np.array(scales[:num_elements])
+
+            dim_info_list.append(
+                ExtraBytesParams(
+                    eb_struct.format_name(),
+                    eb_struct.dtype(),
+                    description=eb_struct.description.rstrip(NULL_BYTE).decode(),
+                    scales=scales,
+                    offsets=offsets,
+                )
+            )
+        return dim_info_list
+
+    def __repr__(self):
+        return "<ExtraBytesVlr(extra bytes structs: {})>".format(
+            len(self.extra_bytes_structs)
+        )
+
+    @staticmethod
+    def official_user_id():
+        return "LASF_Spec"
+
+    @staticmethod
+    def official_record_ids():
+        return (4,)
+
+
+class WaveformPacketStruct(ctypes.LittleEndianStructure):
+    _pack_ = 1
+    _fields_ = [
+        ("bits_per_sample", ctypes.c_ubyte),
+        ("waveform_compression_type", ctypes.c_ubyte),
+        ("number_of_samples", ctypes.c_uint32),
+        ("temporal_sample_spacing", ctypes.c_uint32),
+        ("digitizer_gain", ctypes.c_double),
+        ("digitizer_offset", ctypes.c_double),
+    ]
+
+    @staticmethod
+    def size():
+        return ctypes.sizeof(WaveformPacketStruct)
+
+
+class WaveformPacketVlr(BaseKnownVLR):
+    def __init__(self, record_id, description=""):
+        super().__init__(record_id=record_id, description=description)
+        self.parsed_record = None
+
+    def parse_record_data(self, record_data):
+        self.parsed_record = WaveformPacketStruct.from_buffer_copy(record_data)
+
+    def record_data_bytes(self):
+        return bytes(self.parsed_record)
+
+    @staticmethod
+    def official_record_ids():
+        return range(100, 356)
+
+    @staticmethod
+    def official_user_id():
+        return "LASF_Spec"
+
+    @classmethod
+    def from_raw(cls, raw_vlr):
+        vlr = cls(
+            raw_vlr.header.record_id, description=raw_vlr.header.description.decode()
+        )
+        vlr.description = raw_vlr.header.description
+        vlr.parse_record_data(raw_vlr.record_data)
+        return vlr
+
+
+class GeoKeyEntryStruct(ctypes.LittleEndianStructure):
+    _pack_ = 1
+    _fields_ = [
+        # Id of the key
+        #
+        # Ids are broken down in sub domains:
+        # [    0,  1023]       Reserved
+        # [ 1024,  2047]       GeoTIFF Configuration Keys
+        # [ 2048,  3071]       Geographic/Geocentric CS Parameter Keys
+        # [ 3072,  4095]       Projected CS Parameter Keys
+        # [ 4096,  5119]       Vertical CS Parameter Keys
+        # [ 5120, 32767]       Reserved
+        # [32768, 65535]       Private use
+        ("id", ctypes.c_uint16),
+        # Where to find the data for the key:
+        # 0 => The _actual_ value is stored directly in the "value_offset" member
+        # Otherwise, the tiff tag location is the record_id of the VLR in which the value is stored.
+        # In the case of LAS files the 2 possible values are `34736`, `34737`.
+        ("tiff_tag_location", ctypes.c_uint16),
+        # Number of values in the key.
+        # Implied to be `1` if `tiff_tag_location` is 0
+        ("count", ctypes.c_uint16),
+        # Depending on `tiff_tag_location`, this contains either
+        # the value itself _or_ the offset in the record_data of the containing VLR
+        ("value_offset", ctypes.c_uint16),
+    ]
+
+    @staticmethod
+    def size():
+        return ctypes.sizeof(GeoKeysHeaderStructs)
+
+    def __repr__(self):
+        return "<GeoKey(Id: {}, Location: {}, count: {}, offset: {})>".format(
+            self.id, self.tiff_tag_location, self.count, self.value_offset
+        )
+
+
+class GeoKeysHeaderStructs(ctypes.LittleEndianStructure):
+    _pack_ = 1
+    _fields_ = [
+        ("key_directory_version", ctypes.c_uint16),
+        ("key_revision", ctypes.c_uint16),
+        ("minor_revision", ctypes.c_uint16),
+        ("number_of_keys", ctypes.c_uint16),
+    ]
+
+    def __init__(self):
+        super().__init__(
+            key_directory_version=1, key_revision=1, minor_revision=0, number_of_keys=0
+        )
+
+    @staticmethod
+    def size():
+        return ctypes.sizeof(GeoKeysHeaderStructs)
+
+    def __repr__(self):
+        return "<GeoKeysHeader(vers: {}, rev:{}, minor: {}, num_keys: {})>".format(
+            self.key_directory_version,
+            self.key_revision,
+            self.minor_revision,
+            self.number_of_keys,
+        )
+
+
+class GeoKeyDirectoryVlr(BaseKnownVLR):
+    def __init__(self):
+        super().__init__(description="GeoTIFF GeoKeyDirectoryTag")
+        self.geo_keys_header = GeoKeysHeaderStructs()
+        self.geo_keys = [GeoKeyEntryStruct()]
+
+    def parse_record_data(self, record_data):
+        record_data = bytearray(record_data)
+        header_data = record_data[: ctypes.sizeof(GeoKeysHeaderStructs)]
+        self.geo_keys_header = GeoKeysHeaderStructs.from_buffer(header_data)
+        self.geo_keys = []
+        keys_data = record_data[GeoKeysHeaderStructs.size() :]
+        num_keys = (
+            len(record_data[GeoKeysHeaderStructs.size() :]) // GeoKeyEntryStruct.size()
+        )
+        if num_keys != self.geo_keys_header.number_of_keys:
+            self.geo_keys_header.number_of_keys = num_keys
+
+        for i in range(self.geo_keys_header.number_of_keys):
+            data = keys_data[
+                (i * GeoKeyEntryStruct.size()) : (i + 1) * GeoKeyEntryStruct.size()
+            ]
+            self.geo_keys.append(GeoKeyEntryStruct.from_buffer(data))
+
+    def record_data_bytes(self):
+        b = bytes(self.geo_keys_header)
+        b += b"".join(map(bytes, self.geo_keys))
+        return b
+
+    def parse_crs(self):
+        import pyproj
+
+        # TODO import is done here to avoid cyclic import,
+        # this should probably be fixed
+        from .geotiff import GeographicTypeGeoKey, ProjectedCSTypeGeoKey
+
+        geographic_cs = None
+        projected_cs = None
+        for key in self.geo_keys:
+            if key.id == ProjectedCSTypeGeoKey.id:
+                if 1024 <= key.value_offset <= 32766:
+                    # http://docs.opengeospatial.org/is/19-008r4/19-008r4.html#_requirements_class_projectedcrsgeokey
+                    # "ProjectedCRSGeoKey values in the range 1024-32766 SHALL be EPSG Projected CRS Codes"
+                    projected_cs = pyproj.CRS.from_epsg(key.value_offset)
+            elif key.id == GeographicTypeGeoKey.id:
+                # http://docs.opengeospatial.org/is/19-008r4/19-008r4.html#_requirements_class_geodeticcrsgeokey
+                # GeodeticCRSGeoKey values in the range 1024-32766 SHALL be EPSG geographic 2D or geocentric CRS codes
+                if 1024 <= key.value_offset <= 32766:
+                    geographic_cs = pyproj.CRS.from_epsg(key.value_offset)
+
+        # Projected Coordinate Systems take precedence since,
+        # if they are present, the Geographic CS is probably
+        # redundant and the positioning information in the LAS
+        # file is projected.
+        return projected_cs or geographic_cs
+
+    def __repr__(self):
+        return "<{}({} geo_keys)>".format(self.__class__.__name__, len(self.geo_keys))
+
+    @staticmethod
+    def official_user_id():
+        return "LASF_Projection"
+
+    @staticmethod
+    def official_record_ids():
+        return (34735,)
+
+
+class GeoDoubleParamsVlr(BaseKnownVLR):
+    """
+    Stores all of the `double` valued GeoKeys.
+    """
+
+    def __init__(self):
+        super().__init__(description="GeoTIFF GeoDoubleParamsTag")
+        self.doubles = []
+
+    def parse_record_data(self, record_data):
+        sizeof_double = ctypes.sizeof(ctypes.c_double)
+        if len(record_data) % sizeof_double != 0:
+            raise ValueError(
+                "GeoDoubleParams record data length () is not a multiple of sizeof(double) ()".format(
+                    len(record_data), sizeof_double
+                )
+            )
+        record_data = bytearray(record_data)
+        num_doubles = len(record_data) // sizeof_double
+        for i in range(num_doubles):
+            b = record_data[i * sizeof_double : (i + 1) * sizeof_double]
+            self.doubles.append(ctypes.c_double.from_buffer(b))
+
+    def record_data_bytes(self):
+        return b"".join(map(bytes, self.doubles))
+
+    def __repr__(self):
+        return "<GeoDoubleParamsVlr({})>".format(self.doubles)
+
+    @staticmethod
+    def official_user_id():
+        return "LASF_Projection"
+
+    @staticmethod
+    def official_record_ids():
+        return (34736,)
+
+
+class GeoAsciiParamsVlr(BaseKnownVLR):
+    """
+    Stores all of the `ASCII` valued GeoKeys.
+
+    From GeoTIFF's spec:
+    To avoid problems with naive tiff dump programs the separator between geokeys is not
+    the null-terminator `\0` but `|`.
+
+    """
+
+    def __init__(self):
+        super().__init__(description="GeoTIFF GeoAsciiParamsTag")
+        self.strings = []
+
+    def parse_record_data(self, record_data):
+        self.strings = [s.decode("ascii") for s in record_data.split(NULL_BYTE)]
+        self.rd = record_data
+
+    def record_data_bytes(self):
+        return NULL_BYTE.join(s.encode("ascii") for s in self.strings)
+
+    def __repr__(self):
+        return "<GeoAsciiParamsVlr({})>".format(self.strings)
+
+    @staticmethod
+    def official_user_id():
+        return "LASF_Projection"
+
+    @staticmethod
+    def official_record_ids():
+        return (34737,)
+
+
+class WktMathTransformVlr(BaseKnownVLR):
+    """
+    From the Spec:
+        Note that the math transform WKT record is added for completeness, and a coordinate system WKT
+        may or may not require a math transform WKT record
+
+    """
+
+    def __init__(self):
+        super().__init__(description="")
+        self.string = ""
+
+    def _encode_string(self):
+        return encode_to_null_terminated(self.string, codec="utf-8")
+
+    def parse_record_data(self, record_data):
+        self.string = record_data.decode("utf-8").rstrip("\0")
+
+    def record_data_bytes(self):
+        return self._encode_string()
+
+    @staticmethod
+    def official_user_id():
+        return "LASF_Projection"
+
+    @staticmethod
+    def official_record_ids():
+        return (2111,)
+
+
+class WktCoordinateSystemVlr(BaseKnownVLR):
+    """Replaces Coordinates Reference System for new las files (point fmt >= 5)
+    "LAS is not using the “ESRI WKT”
+    """
+
+    def __init__(self, wkt_string=""):
+        super().__init__(description="OGC Transformation Record")
+        self.string = wkt_string
+
+    def _encode_string(self):
+        return encode_to_null_terminated(self.string, codec="utf-8")
+
+    def parse_record_data(self, record_data):
+        self.string = record_data.decode("utf-8").rstrip("\0")
+
+    def record_data_bytes(self):
+        return self._encode_string()
+
+    def parse_crs(self):
+        import pyproj
+
+        return pyproj.CRS.from_wkt(self.string)
+
+    @staticmethod
+    def official_user_id():
+        return "LASF_Projection"
+
+    @staticmethod
+    def official_record_ids():
+        return (2112,)
+
+
+def vlr_factory(vlr: VLR):
+    """Given a vlr tries to find its corresponding KnownVLR class
+    that can parse its data.
+    If no KnownVLR implementation is found, returns the input vlr unchanged
+    """
+    user_id = vlr.user_id
+    known_vlrs = BaseKnownVLR.__subclasses__()
+    for known_vlr in known_vlrs:
+        if (
+            known_vlr.official_user_id() == user_id
+            and vlr.record_id in known_vlr.official_record_ids()
+        ):
+            try:
+                return known_vlr.from_raw(vlr)
+            except Exception as err:
+                logger.warning(f"Failed to parse {known_vlr}: {err}")
+                return vlr
+
+    return vlr
```

### Comparing `laspy-2.4.1/laspy/vlrs/vlr.py` & `laspy-2.5.0/laspy/vlrs/vlr.py`

 * *Ordering differences only*

 * *Files 24% similar despite different names*

```diff
@@ -1,88 +1,88 @@
-from abc import ABC, abstractmethod
-from typing import Union
-
-
-class IVLR(ABC):
-    @property
-    @abstractmethod
-    def user_id(self) -> str:
-        ...
-
-    @property
-    @abstractmethod
-    def record_id(self) -> int:
-        ...
-
-    @property
-    @abstractmethod
-    def description(self) -> Union[str, bytes]:
-        ...
-
-    @abstractmethod
-    def record_data_bytes(self) -> bytes:
-        ...
-
-
-class BaseVLR(IVLR, ABC):
-    def __init__(self, user_id, record_id, description=""):
-        self._user_id: str = user_id
-        self._record_id: int = record_id
-        self._description: Union[str, bytes] = description
-
-    @property
-    def user_id(self) -> str:
-        """
-        The user id
-        """
-        return self._user_id
-
-    @property
-    def record_id(self) -> int:
-        """
-        The record id
-        """
-        return self._record_id
-
-    @property
-    def description(self) -> Union[str, bytes]:
-        """
-        The description, cannot exceed 32 bytes
-        """
-        return self._description
-
-
-class VLR(BaseVLR):
-    """
-    >>> import laspy
-    >>> my_vlr = laspy.VLR(
-    ... user_id="MyUserId",
-    ... record_id=0,
-    ... description="An Example VLR",
-    ... record_data=int(42).to_bytes(8, byteorder='little'),
-    ... )
-    >>> my_vlr.user_id
-    'MyUserId'
-    >>> int.from_bytes(my_vlr.record_data, byteorder='little')
-    42
-    """
-
-    def __init__(self, user_id, record_id, description="", record_data=b""):
-        super().__init__(user_id, record_id, description=description)
-        #: The record_data as bytes, length cannot exceed 65_535
-        self.record_data: bytes = record_data
-
-    def record_data_bytes(self) -> bytes:
-        return self.record_data
-
-    def __eq__(self, other):
-        return (
-            self.record_id == other.record_id
-            and self.user_id == other.user_id
-            and self.description == other.description
-            and self.record_data == other.record_data
-        )
-
-    def __repr__(self):
-        return "<{}(user_id: '{}', record_id: '{}', data len: {})>".format(
-            self.__class__.__name__, self.user_id, self.record_id, len(self.record_data)
-        )
+from abc import ABC, abstractmethod
+from typing import Union
+
+
+class IVLR(ABC):
+    @property
+    @abstractmethod
+    def user_id(self) -> str:
+        ...
+
+    @property
+    @abstractmethod
+    def record_id(self) -> int:
+        ...
+
+    @property
+    @abstractmethod
+    def description(self) -> Union[str, bytes]:
+        ...
+
+    @abstractmethod
+    def record_data_bytes(self) -> bytes:
+        ...
+
+
+class BaseVLR(IVLR, ABC):
+    def __init__(self, user_id, record_id, description=""):
+        self._user_id: str = user_id
+        self._record_id: int = record_id
+        self._description: Union[str, bytes] = description
+
+    @property
+    def user_id(self) -> str:
+        """
+        The user id
+        """
+        return self._user_id
+
+    @property
+    def record_id(self) -> int:
+        """
+        The record id
+        """
+        return self._record_id
+
+    @property
+    def description(self) -> Union[str, bytes]:
+        """
+        The description, cannot exceed 32 bytes
+        """
+        return self._description
+
+
+class VLR(BaseVLR):
+    """
+    >>> import laspy
+    >>> my_vlr = laspy.VLR(
+    ... user_id="MyUserId",
+    ... record_id=0,
+    ... description="An Example VLR",
+    ... record_data=int(42).to_bytes(8, byteorder='little'),
+    ... )
+    >>> my_vlr.user_id
+    'MyUserId'
+    >>> int.from_bytes(my_vlr.record_data, byteorder='little')
+    42
+    """
+
+    def __init__(self, user_id, record_id, description="", record_data=b""):
+        super().__init__(user_id, record_id, description=description)
+        #: The record_data as bytes, length cannot exceed 65_535
+        self.record_data: bytes = record_data
+
+    def record_data_bytes(self) -> bytes:
+        return self.record_data
+
+    def __eq__(self, other):
+        return (
+            self.record_id == other.record_id
+            and self.user_id == other.user_id
+            and self.description == other.description
+            and self.record_data == other.record_data
+        )
+
+    def __repr__(self):
+        return "<{}(user_id: '{}', record_id: '{}', data len: {})>".format(
+            self.__class__.__name__, self.user_id, self.record_id, len(self.record_data)
+        )
```

### Comparing `laspy-2.4.1/laspy/vlrs/vlrlist.py` & `laspy-2.5.0/laspy/vlrs/vlrlist.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,216 +1,216 @@
-import logging
-from typing import BinaryIO, List
-
-import numpy as np
-
-from .known import vlr_factory, IKnownVLR
-from .vlr import VLR
-from ..utils import read_string, write_as_c_string
-
-logger = logging.getLogger(__name__)
-
-RESERVED_LEN = 2
-USER_ID_LEN = 16
-DESCRIPTION_LEN = 32
-
-
-class VLRList(list):
-    """Class responsible for managing the vlrs"""
-
-    def __init__(self, *args, **kwargs):
-        super().__init__(*args, **kwargs)
-
-    def index(self, value, start: int = 0, stop: int = None) -> int:
-        if stop is None:
-            stop = len(self)
-        if isinstance(value, str):
-            for i, vlr in enumerate(self[start:stop]):
-                if vlr.__class__.__name__ == value:
-                    return i + start
-            raise ValueError(f"VLR '{value}' could not be found in the list")
-        else:
-            return super().index(value, start, stop)
-
-    def get_by_id(self, user_id="", record_ids=(None,)):
-        """Function to get vlrs by user_id and/or record_ids.
-        Always returns a list even if only one vlr matches the user_id and record_id
-
-        >>> import laspy
-        >>> from laspy.vlrs.known import ExtraBytesVlr, WktCoordinateSystemVlr
-        >>> las = laspy.read("tests/data/extrabytes.las")
-        >>> las.vlrs
-        [<ExtraBytesVlr(extra bytes structs: 5)>]
-        >>> las.vlrs.get(WktCoordinateSystemVlr.official_user_id())
-        []
-        >>> las.vlrs.get(WktCoordinateSystemVlr.official_user_id())[0]
-        Traceback (most recent call last):
-        IndexError: list index out of range
-        >>> las.vlrs.get_by_id(ExtraBytesVlr.official_user_id())
-        [<ExtraBytesVlr(extra bytes structs: 5)>]
-        >>> las.vlrs.get_by_id(ExtraBytesVlr.official_user_id())[0]
-        <ExtraBytesVlr(extra bytes structs: 5)>
-
-        Parameters
-        ----------
-        user_id: str, optional
-                 the user id
-        record_ids: iterable of int, optional
-                    THe record ids of the vlr(s) you wish to get
-
-        Returns
-        -------
-        :py:class:`list`
-            a list of vlrs matching the user_id and records_ids
-
-        """
-        return [
-            vlr
-            for vlr in self
-            if (user_id == "" or vlr.user_id == user_id)
-            and (record_ids == (None,) or vlr.record_id in record_ids)
-        ]
-
-    def get(self, vlr_type: str) -> List[IKnownVLR]:
-        """Returns the list of vlrs of the requested type
-        Always returns a list even if there is only one VLR of type vlr_type.
-
-        >>> import laspy
-        >>> las = laspy.read("tests/data/extrabytes.las")
-        >>> las.vlrs
-        [<ExtraBytesVlr(extra bytes structs: 5)>]
-        >>> las.vlrs.get("WktCoordinateSystemVlr")
-        []
-        >>> las.vlrs.get("WktCoordinateSystemVlr")[0]
-        Traceback (most recent call last):
-        IndexError: list index out of range
-        >>> las.vlrs.get('ExtraBytesVlr')
-        [<ExtraBytesVlr(extra bytes structs: 5)>]
-        >>> las.vlrs.get('ExtraBytesVlr')[0]
-        <ExtraBytesVlr(extra bytes structs: 5)>
-
-
-        Parameters
-        ----------
-        vlr_type: str
-                  the class name of the vlr
-
-        Returns
-        -------
-        :py:class:`list`
-            a List of vlrs matching the user_id and records_ids
-
-        """
-        return [v for v in self if v.__class__.__name__ == vlr_type]
-
-    def extract(self, vlr_type: str) -> List[IKnownVLR]:
-        """Returns the list of vlrs of the requested type
-        The difference with get is that the returned vlrs will be removed from the list
-
-        Parameters
-        ----------
-        vlr_type: str
-                  the class name of the vlr
-
-        Returns
-        -------
-        list
-            a List of vlrs matching the user_id and records_ids
-
-        """
-        kept_vlrs, extracted_vlrs = [], []
-        for vlr in self:
-            if vlr.__class__.__name__ == vlr_type:
-                extracted_vlrs.append(vlr)
-            else:
-                kept_vlrs.append(vlr)
-        self.clear()
-        self.extend(kept_vlrs)
-        return extracted_vlrs
-
-    def __repr__(self):
-        return "[{}]".format(", ".join(repr(vlr) for vlr in self))
-
-    @classmethod
-    def read_from(
-        cls, data_stream: BinaryIO, num_to_read: int, extended: bool = False
-    ) -> "VLRList":
-        """Reads vlrs and parse them if possible from the stream
-
-        Parameters
-        ----------
-        data_stream : io.BytesIO
-                      stream to read from
-        num_to_read : int
-                      number of vlrs to be read
-
-        extended : bool
-                      whether the vlrs are regular vlr or extended vlr
-
-        Returns
-        -------
-        laspy.vlrs.vlrlist.VLRList
-            List of vlrs
-
-        """
-        vlrlist = cls()
-        for _ in range(num_to_read):
-            data_stream.read(RESERVED_LEN)
-            user_id = data_stream.read(USER_ID_LEN).split(b"\0")[0].decode()
-            record_id = int.from_bytes(
-                data_stream.read(2), byteorder="little", signed=False
-            )
-            if extended:
-                record_data_len = int.from_bytes(
-                    data_stream.read(8), byteorder="little", signed=False
-                )
-            else:
-                record_data_len = int.from_bytes(
-                    data_stream.read(2), byteorder="little", signed=False
-                )
-            description = read_string(data_stream, DESCRIPTION_LEN)
-            record_data_bytes = data_stream.read(record_data_len)
-
-            vlr = VLR(user_id, record_id, description, record_data_bytes)
-
-            vlrlist.append(vlr_factory(vlr))
-
-        return vlrlist
-
-    def write_to(
-        self,
-        stream: BinaryIO,
-        as_extended: bool = False,
-        encoding_errors: str = "strict",
-    ) -> int:
-        bytes_written = 0
-        for vlr in self:
-            record_data = vlr.record_data_bytes()
-
-            stream.write(b"\0\0")
-            write_as_c_string(stream, vlr.user_id, USER_ID_LEN)
-            stream.write(vlr.record_id.to_bytes(2, byteorder="little", signed=False))
-            if as_extended:
-                stream.write(
-                    len(record_data).to_bytes(8, byteorder="little", signed=False)
-                )
-            else:
-                max_length = np.iinfo("uint16").max
-                if len(record_data) > max_length:
-                    raise ValueError(
-                        f"VLR record_date length ({len(record_data)}) exceeds the maximum length ({max_length})"
-                    )
-                stream.write(
-                    len(record_data).to_bytes(2, byteorder="little", signed=False)
-                )
-            write_as_c_string(
-                stream,
-                vlr.description,
-                DESCRIPTION_LEN,
-                encoding_errors=encoding_errors,
-            )
-            stream.write(record_data)
-
-            bytes_written += 54 if not as_extended else 60
-            bytes_written += len(record_data)
-
-        return bytes_written
+import logging
+from typing import BinaryIO, List
+
+import numpy as np
+
+from ..utils import read_string, write_as_c_string
+from .known import IKnownVLR, vlr_factory
+from .vlr import VLR
+
+logger = logging.getLogger(__name__)
+
+RESERVED_LEN = 2
+USER_ID_LEN = 16
+DESCRIPTION_LEN = 32
+
+
+class VLRList(list):
+    """Class responsible for managing the vlrs"""
+
+    def __init__(self, *args, **kwargs):
+        super().__init__(*args, **kwargs)
+
+    def index(self, value, start: int = 0, stop: int = None) -> int:
+        if stop is None:
+            stop = len(self)
+        if isinstance(value, str):
+            for i, vlr in enumerate(self[start:stop]):
+                if vlr.__class__.__name__ == value:
+                    return i + start
+            raise ValueError(f"VLR '{value}' could not be found in the list")
+        else:
+            return super().index(value, start, stop)
+
+    def get_by_id(self, user_id="", record_ids=(None,)):
+        """Function to get vlrs by user_id and/or record_ids.
+        Always returns a list even if only one vlr matches the user_id and record_id
+
+        >>> import laspy
+        >>> from laspy.vlrs.known import ExtraBytesVlr, WktCoordinateSystemVlr
+        >>> las = laspy.read("tests/data/extrabytes.las")
+        >>> las.vlrs
+        [<ExtraBytesVlr(extra bytes structs: 5)>]
+        >>> las.vlrs.get(WktCoordinateSystemVlr.official_user_id())
+        []
+        >>> las.vlrs.get(WktCoordinateSystemVlr.official_user_id())[0]
+        Traceback (most recent call last):
+        IndexError: list index out of range
+        >>> las.vlrs.get_by_id(ExtraBytesVlr.official_user_id())
+        [<ExtraBytesVlr(extra bytes structs: 5)>]
+        >>> las.vlrs.get_by_id(ExtraBytesVlr.official_user_id())[0]
+        <ExtraBytesVlr(extra bytes structs: 5)>
+
+        Parameters
+        ----------
+        user_id: str, optional
+                 the user id
+        record_ids: iterable of int, optional
+                    THe record ids of the vlr(s) you wish to get
+
+        Returns
+        -------
+        :py:class:`list`
+            a list of vlrs matching the user_id and records_ids
+
+        """
+        return [
+            vlr
+            for vlr in self
+            if (user_id == "" or vlr.user_id == user_id)
+            and (record_ids == (None,) or vlr.record_id in record_ids)
+        ]
+
+    def get(self, vlr_type: str) -> List[IKnownVLR]:
+        """Returns the list of vlrs of the requested type
+        Always returns a list even if there is only one VLR of type vlr_type.
+
+        >>> import laspy
+        >>> las = laspy.read("tests/data/extrabytes.las")
+        >>> las.vlrs
+        [<ExtraBytesVlr(extra bytes structs: 5)>]
+        >>> las.vlrs.get("WktCoordinateSystemVlr")
+        []
+        >>> las.vlrs.get("WktCoordinateSystemVlr")[0]
+        Traceback (most recent call last):
+        IndexError: list index out of range
+        >>> las.vlrs.get('ExtraBytesVlr')
+        [<ExtraBytesVlr(extra bytes structs: 5)>]
+        >>> las.vlrs.get('ExtraBytesVlr')[0]
+        <ExtraBytesVlr(extra bytes structs: 5)>
+
+
+        Parameters
+        ----------
+        vlr_type: str
+                  the class name of the vlr
+
+        Returns
+        -------
+        :py:class:`list`
+            a List of vlrs matching the user_id and records_ids
+
+        """
+        return [v for v in self if v.__class__.__name__ == vlr_type]
+
+    def extract(self, vlr_type: str) -> List[IKnownVLR]:
+        """Returns the list of vlrs of the requested type
+        The difference with get is that the returned vlrs will be removed from the list
+
+        Parameters
+        ----------
+        vlr_type: str
+                  the class name of the vlr
+
+        Returns
+        -------
+        list
+            a List of vlrs matching the user_id and records_ids
+
+        """
+        kept_vlrs, extracted_vlrs = [], []
+        for vlr in self:
+            if vlr.__class__.__name__ == vlr_type:
+                extracted_vlrs.append(vlr)
+            else:
+                kept_vlrs.append(vlr)
+        self.clear()
+        self.extend(kept_vlrs)
+        return extracted_vlrs
+
+    def __repr__(self):
+        return "[{}]".format(", ".join(repr(vlr) for vlr in self))
+
+    @classmethod
+    def read_from(
+        cls, data_stream: BinaryIO, num_to_read: int, extended: bool = False
+    ) -> "VLRList":
+        """Reads vlrs and parse them if possible from the stream
+
+        Parameters
+        ----------
+        data_stream : io.BytesIO
+                      stream to read from
+        num_to_read : int
+                      number of vlrs to be read
+
+        extended : bool
+                      whether the vlrs are regular vlr or extended vlr
+
+        Returns
+        -------
+        laspy.vlrs.vlrlist.VLRList
+            List of vlrs
+
+        """
+        vlrlist = cls()
+        for _ in range(num_to_read):
+            data_stream.read(RESERVED_LEN)
+            user_id = data_stream.read(USER_ID_LEN).split(b"\0")[0].decode()
+            record_id = int.from_bytes(
+                data_stream.read(2), byteorder="little", signed=False
+            )
+            if extended:
+                record_data_len = int.from_bytes(
+                    data_stream.read(8), byteorder="little", signed=False
+                )
+            else:
+                record_data_len = int.from_bytes(
+                    data_stream.read(2), byteorder="little", signed=False
+                )
+            description = read_string(data_stream, DESCRIPTION_LEN)
+            record_data_bytes = data_stream.read(record_data_len)
+
+            vlr = VLR(user_id, record_id, description, record_data_bytes)
+
+            vlrlist.append(vlr_factory(vlr))
+
+        return vlrlist
+
+    def write_to(
+        self,
+        stream: BinaryIO,
+        as_extended: bool = False,
+        encoding_errors: str = "strict",
+    ) -> int:
+        bytes_written = 0
+        for vlr in self:
+            record_data = vlr.record_data_bytes()
+
+            stream.write(b"\0\0")
+            write_as_c_string(stream, vlr.user_id, USER_ID_LEN)
+            stream.write(vlr.record_id.to_bytes(2, byteorder="little", signed=False))
+            if as_extended:
+                stream.write(
+                    len(record_data).to_bytes(8, byteorder="little", signed=False)
+                )
+            else:
+                max_length = np.iinfo("uint16").max
+                if len(record_data) > max_length:
+                    raise ValueError(
+                        f"VLR record_date length ({len(record_data)}) exceeds the maximum length ({max_length})"
+                    )
+                stream.write(
+                    len(record_data).to_bytes(2, byteorder="little", signed=False)
+                )
+            write_as_c_string(
+                stream,
+                vlr.description,
+                DESCRIPTION_LEN,
+                encoding_errors=encoding_errors,
+            )
+            stream.write(record_data)
+
+            bytes_written += 54 if not as_extended else 60
+            bytes_written += len(record_data)
+
+        return bytes_written
```

### Comparing `laspy-2.4.1/laspy.egg-info/PKG-INFO` & `laspy-2.5.0/laspy.egg-info/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,111 +1,109 @@
-Metadata-Version: 2.1
-Name: laspy
-Version: 2.4.1
-Summary: Native Python ASPRS LAS read/write library
-Home-page: https://github.com/laspy/laspy
-Author: Grant Brown, Thomas Montaigu
-Author-email: grant.brown73@gmail.com, thomas.montaigu@laposte.net
-License: BSD
-Keywords: gis lidar las
-Platform: UNKNOWN
-Classifier: Development Status :: 5 - Production/Stable
-Classifier: Intended Audience :: Developers
-Classifier: Intended Audience :: Science/Research
-Classifier: License :: OSI Approved :: BSD License
-Classifier: Operating System :: OS Independent
-Classifier: Programming Language :: Python
-Classifier: Topic :: Scientific/Engineering :: GIS
-Requires-Python: >=3.7
-Description-Content-Type: text/markdown
-Provides-Extra: dev
-Provides-Extra: lazrs
-Provides-Extra: laszip
-Provides-Extra: pyproj
-Provides-Extra: requests
-License-File: LICENSE.txt
-
-# Laspy
-
-Laspy is a python library for reading, modifying and creating LAS LiDAR
-files.
-
-Laspy is compatible with Python  3.7+.
-
-## Features
-
-- LAS support.
-- LAZ support via `lazrs` or `laszip` backend.
-- LAS/LAZ streamed/chunked reading/writting.
-- [COPC] support over files.
-- [COPC] support over https with `requests` package.
-- CRS support via `pyproj` package.
-
-
-[COPC]: https://github.com/copcio/copcio.github.io
-
-
-## Examples
-
-Directly read and write las
-```Python
-import laspy
-
-las = laspy.read('filename.las')
-las.points = las.points[las.classification == 2]
-las.write('ground.laz')
-```
-
-
-Open data to inspect header (opening only reads the header and vlrs)
-
-```Python
-import laspy
-
-with laspy.open('filename.las') as f:
-    print(f"Point format:       {f.header.point_format}")
-    print(f"Number of points:   {f.header.point_count}")
-    print(f"Number of vlrs:     {len(f.header.vlrs)}")
-```
-Use the 'chunked' reading & writing features
-
-```Python
-import laspy
-
-with laspy.open('big.laz') as input_las:
-    with laspy.open('ground.laz', mode="w", header=input_las.header) as ground_las:
-        for points in input_las.chunk_iterator(2_000_000):
-            ground_las.write_points(points[points.classification == 2])
-
-```
-
-Appending points to existing file
-
-```Python
-import laspy
-
-with laspy.open('big.laz') as input_las:
-    with laspy.open('ground.laz', mode="a") as ground_las:
-        for points in input_las.chunk_iterator(2_000_000):
-            ground_las.append_points(points[points.classification == 2])
-```
-
-API Documentation and tutorials are available at
-[ReadTheDocs](https://laspy.readthedocs.io/en/latest/).
-
-## Installation
-
-Laspy can be installed either with `pip`:
-
-```
-pip install laspy # without LAZ support
-# Or
-pip install laspy[laszip] # with LAZ support via LASzip
-# Or
-pip install laspy[lazrs] # with LAZ support via lazrs
-```
-
-## Changelog
-
-See [CHANGELOG.md](CHANGELOG.md)
-
-
+Metadata-Version: 2.1
+Name: laspy
+Version: 2.5.0
+Summary: Native Python ASPRS LAS read/write library
+Home-page: https://github.com/laspy/laspy
+Author: Grant Brown, Thomas Montaigu
+Author-email: grant.brown73@gmail.com, thomas.montaigu@laposte.net
+License: BSD
+Keywords: gis lidar las
+Classifier: Development Status :: 5 - Production/Stable
+Classifier: Intended Audience :: Developers
+Classifier: Intended Audience :: Science/Research
+Classifier: License :: OSI Approved :: BSD License
+Classifier: Operating System :: OS Independent
+Classifier: Programming Language :: Python
+Classifier: Topic :: Scientific/Engineering :: GIS
+Requires-Python: >=3.7
+Description-Content-Type: text/markdown
+Provides-Extra: dev
+Provides-Extra: lazrs
+Provides-Extra: laszip
+Provides-Extra: pyproj
+Provides-Extra: requests
+Provides-Extra: cli
+License-File: LICENSE.txt
+
+# Laspy
+
+Laspy is a python library for reading, modifying and creating LAS LiDAR
+files.
+
+Laspy is compatible with Python  3.7+.
+
+## Features
+
+- LAS support.
+- LAZ support via `lazrs` or `laszip` backend.
+- LAS/LAZ streamed/chunked reading/writting.
+- [COPC] support over files.
+- [COPC] support over https with `requests` package.
+- CRS support via `pyproj` package.
+
+
+[COPC]: https://github.com/copcio/copcio.github.io
+
+
+## Examples
+
+Directly read and write las
+```Python
+import laspy
+
+las = laspy.read('filename.las')
+las.points = las.points[las.classification == 2]
+las.write('ground.laz')
+```
+
+
+Open data to inspect header (opening only reads the header and vlrs)
+
+```Python
+import laspy
+
+with laspy.open('filename.las') as f:
+    print(f"Point format:       {f.header.point_format}")
+    print(f"Number of points:   {f.header.point_count}")
+    print(f"Number of vlrs:     {len(f.header.vlrs)}")
+```
+Use the 'chunked' reading & writing features
+
+```Python
+import laspy
+
+with laspy.open('big.laz') as input_las:
+    with laspy.open('ground.laz', mode="w", header=input_las.header) as ground_las:
+        for points in input_las.chunk_iterator(2_000_000):
+            ground_las.write_points(points[points.classification == 2])
+
+```
+
+Appending points to existing file
+
+```Python
+import laspy
+
+with laspy.open('big.laz') as input_las:
+    with laspy.open('ground.laz', mode="a") as ground_las:
+        for points in input_las.chunk_iterator(2_000_000):
+            ground_las.append_points(points[points.classification == 2])
+```
+
+API Documentation and tutorials are available at
+[ReadTheDocs](https://laspy.readthedocs.io/en/latest/).
+
+## Installation
+
+Laspy can be installed either with `pip`:
+
+```
+pip install laspy # without LAZ support
+# Or
+pip install laspy[laszip] # with LAZ support via LASzip
+# Or
+pip install laspy[lazrs] # with LAZ support via lazrs
+```
+
+## Changelog
+
+See [CHANGELOG.md](CHANGELOG.md)
```

### Comparing `laspy-2.4.1/setup.py` & `laspy-2.5.0/setup.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,54 +1,59 @@
-from setuptools import setup, find_packages
-
-with open("README.md") as f:
-    readme = f.read()
-
-__version__ = None
-# Get __version without importing
-with open("laspy/__init__.py", "r") as fp:
-    # get and exec just the line which looks like "__version__ = '0.9.4'"
-    exec(next(line for line in fp if "__version__" in line))
-
-setup(
-    name="laspy",
-    version=__version__,
-    description="Native Python ASPRS LAS read/write library",
-    license="BSD",
-    keywords="gis lidar las",
-    author="Grant Brown, Thomas Montaigu",
-    author_email="grant.brown73@gmail.com, thomas.montaigu@laposte.net",
-    url="https://github.com/laspy/laspy",
-    long_description=readme,
-    long_description_content_type="text/markdown",
-    packages=find_packages(exclude=("tests",)),
-    python_requires=">=3.7",
-    install_requires=["numpy"],
-    extras_require={
-        "dev": [
-            "pytest",
-            "coverage",
-            "sphinx",
-            "sphinx-rtd-theme",
-            "nox",
-            "black==22.3.0",
-            "pytest-benchmark",
-            "m2r2",
-            "rangehttpserver",
-        ],
-        "lazrs": ["lazrs>=0.5.0, < 0.6.0"],
-        "laszip": ["laszip >= 0.2.1, < 0.3.0"],
-        "pyproj": ["pyproj"],
-        "requests": ["requests"],
-    },
-    include_package_data=True,
-    zip_safe=False,
-    classifiers=[
-        "Development Status :: 5 - Production/Stable",
-        "Intended Audience :: Developers",
-        "Intended Audience :: Science/Research",
-        "License :: OSI Approved :: BSD License",
-        "Operating System :: OS Independent",
-        "Programming Language :: Python",
-        "Topic :: Scientific/Engineering :: GIS",
-    ],
-)
+from setuptools import find_packages, setup
+
+with open("README.md") as f:
+    readme = f.read()
+
+__version__ = None
+# Get __version without importing
+with open("laspy/__init__.py", "r") as fp:
+    # get and exec just the line which looks like "__version__ = '0.9.4'"
+    exec(next(line for line in fp if "__version__" in line))
+
+setup(
+    name="laspy",
+    version=__version__,
+    description="Native Python ASPRS LAS read/write library",
+    license="BSD",
+    keywords="gis lidar las",
+    author="Grant Brown, Thomas Montaigu",
+    author_email="grant.brown73@gmail.com, thomas.montaigu@laposte.net",
+    url="https://github.com/laspy/laspy",
+    long_description=readme,
+    long_description_content_type="text/markdown",
+    packages=find_packages(exclude=("tests",)),
+    python_requires=">=3.7",
+    install_requires=["numpy"],
+    extras_require={
+        "dev": [
+            "pytest",
+            "coverage",
+            "sphinx",
+            "sphinx-rtd-theme",
+            "nox",
+            "black==22.3.0",
+            "pytest-benchmark",
+            "m2r2",
+            "rangehttpserver",
+            "isort==5.11.5",
+        ],
+        "lazrs": ["lazrs>=0.5.0, < 0.6.0"],
+        "laszip": ["laszip >= 0.2.1, < 0.3.0"],
+        "pyproj": ["pyproj"],
+        "requests": ["requests"],
+        "cli": ["typer[all] >= 0.8.0 "],
+    },
+    entry_points={
+        "console_scripts": ["laspy=laspy.cli.main:main"],
+    },
+    include_package_data=True,
+    zip_safe=False,
+    classifiers=[
+        "Development Status :: 5 - Production/Stable",
+        "Intended Audience :: Developers",
+        "Intended Audience :: Science/Research",
+        "License :: OSI Approved :: BSD License",
+        "Operating System :: OS Independent",
+        "Programming Language :: Python",
+        "Topic :: Scientific/Engineering :: GIS",
+    ],
+)
```

### Comparing `laspy-2.4.1/tests/conftest.py` & `laspy-2.5.0/tests/conftest.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,150 +1,153 @@
-from pathlib import Path
-
-import pytest
-
-import laspy
-
-SIMPLE_LAS_FILE_PATH = Path(__file__).parent / "data" / "simple.las"
-VEGETATION1_3_LAS_FILE_PATH = Path(__file__).parent / "data" / "vegetation_1_3.las"
-TEST1_4_LAS_FILE_PATH = Path(__file__).parent / "data" / "test1_4.las"
-EXTRA_BYTES_LAS_FILE_PATH = Path(__file__).parent / "data" / "extrabytes.las"
-LAS_1_4_WITH_EVLRS_FILE_PATH = Path(__file__).parent / "data" / "1_4_w_evlr.las"
-
-SIMPLE_LAZ_FILE_PATH = Path(__file__).parent / "data" / "simple.laz"
-EXTRA_BYTES_LAZ_FILE_PATH = Path(__file__).parent / "data" / "extra.laz"
-PLANE_LAZ_FILE_PATH = Path(__file__).parent / "data" / "plane.laz"
-AUTZEN_FILE_PATH = Path(__file__).parent / "data" / "autzen.las"
-AUTZEN_GEO_PROJ_FILE_PATH = Path(__file__).parent / "data" / "autzen_geo_proj.las"
-LAZ_1_4_WITH_EVLRS_FILE_PATH = Path(__file__).parent / "data" / "1_4_w_evlr.laz"
-
-UNREGISTERED_EXTRA_BYTES_LAS = (
-    Path(__file__).parent / "data" / "unregistered_extra_bytes.las"
-)
-
-ALL_LAS_FILE_PATH = [
-    SIMPLE_LAS_FILE_PATH,
-    VEGETATION1_3_LAS_FILE_PATH,
-    TEST1_4_LAS_FILE_PATH,
-    EXTRA_BYTES_LAS_FILE_PATH,
-]
-
-ALL_LAZ_FILE_PATH = [
-    SIMPLE_LAZ_FILE_PATH,
-    EXTRA_BYTES_LAZ_FILE_PATH,
-    PLANE_LAZ_FILE_PATH,
-]
-
-ALL_LAZ_BACKEND = laspy.LazBackend.detect_available()
-
-SUPPORTED_SINGULAR_EXTRA_BYTES_TYPE = [
-    "u1",
-    "u2",
-    "u4",
-    "u8",
-    "i1",
-    "i2",
-    "i4",
-    "i8",
-    "f4",
-    "f8",
-    "uint8",
-    "uint16",
-    "uint32",
-    "uint64",
-    "int8",
-    "int16",
-    "int32",
-    "int64",
-    "float32",
-    "float64",
-]
-
-SUPPORTED_ARRAY_2_EXTRA_BYTES_TYPE = [
-    f"2{base_type}" for base_type in SUPPORTED_SINGULAR_EXTRA_BYTES_TYPE
-]
-
-SUPPORTED_ARRAY_3_EXTRA_BYTES_TYPE = [
-    f"3{base_type}" for base_type in SUPPORTED_SINGULAR_EXTRA_BYTES_TYPE
-]
-
-SUPPORTED_EXTRA_BYTES_TYPE = (
-    SUPPORTED_SINGULAR_EXTRA_BYTES_TYPE
-    + SUPPORTED_ARRAY_2_EXTRA_BYTES_TYPE
-    + SUPPORTED_ARRAY_3_EXTRA_BYTES_TYPE
-)
-
-
-class NonSeekableStream:
-    """
-    Fake non stream / file object which simulates a file object
-    on which we cannot seek
-    """
-
-    def __init__(self, inner):
-        self.inner = inner
-
-    def read(self, n):
-        return self.inner.read(n)
-
-    def seekable(self):
-        return False
-
-
-@pytest.fixture()
-def simple_las_path():
-    return SIMPLE_LAS_FILE_PATH
-
-
-@pytest.fixture(params=SUPPORTED_EXTRA_BYTES_TYPE)
-def extra_bytes_params(request):
-    return laspy.ExtraBytesParams(
-        name="just_a_name", type=request.param, description="laspy test ExtraBytes"
-    )
-
-
-@pytest.fixture(params=[EXTRA_BYTES_LAS_FILE_PATH, EXTRA_BYTES_LAZ_FILE_PATH], ids=repr)
-def las_file_path_with_extra_bytes(request):
-    if request.param.suffix == ".laz" and len(laspy.LazBackend.detect_available()) == 0:
-        return pytest.skip("No Laz Backend")
-    else:
-        return request.param
-
-
-@pytest.fixture(params=ALL_LAS_FILE_PATH, ids=repr)
-def las_file_path(request):
-    return request.param
-
-
-@pytest.fixture(params=ALL_LAZ_FILE_PATH, ids=repr)
-def laz_file_path(request):
-    if len(laspy.LazBackend.detect_available()) == 0:
-        return pytest.skip("No Laz Backend")
-    return request.param
-
-
-@pytest.fixture(params=ALL_LAS_FILE_PATH + ALL_LAZ_FILE_PATH, ids=repr)
-def file_path(request):
-    if len(laspy.LazBackend.detect_available()) == 0:
-        return pytest.skip("No Laz Backend")
-    return request.param
-
-
-@pytest.fixture(
-    params=ALL_LAZ_BACKEND
-    if ALL_LAZ_BACKEND
-    else [pytest.mark.skip("No Laz Backend installed")]
-)
-def laz_backend(request):
-    return request.param
-
-
-def all_las_file_path():
-    return all_las_file_path()
-
-
-@pytest.fixture()
-def mmapped_file_path(tmp_path):
-    import shutil
-
-    copied_file = shutil.copy(SIMPLE_LAS_FILE_PATH, tmp_path)
-    yield copied_file
+from pathlib import Path
+
+import pytest
+
+import laspy
+
+SIMPLE_LAS_FILE_PATH = Path(__file__).parent / "data" / "simple.las"
+VEGETATION1_3_LAS_FILE_PATH = Path(__file__).parent / "data" / "vegetation_1_3.las"
+TEST1_4_LAS_FILE_PATH = Path(__file__).parent / "data" / "test1_4.las"
+EXTRA_BYTES_LAS_FILE_PATH = Path(__file__).parent / "data" / "extrabytes.las"
+LAS_1_4_WITH_EVLRS_FILE_PATH = Path(__file__).parent / "data" / "1_4_w_evlr.las"
+
+SIMPLE_LAZ_FILE_PATH = Path(__file__).parent / "data" / "simple.laz"
+EXTRA_BYTES_LAZ_FILE_PATH = Path(__file__).parent / "data" / "extra.laz"
+PLANE_LAZ_FILE_PATH = Path(__file__).parent / "data" / "plane.laz"
+AUTZEN_FILE_PATH = Path(__file__).parent / "data" / "autzen.las"
+AUTZEN_GEO_PROJ_FILE_PATH = Path(__file__).parent / "data" / "autzen_geo_proj.las"
+LAZ_1_4_WITH_EVLRS_FILE_PATH = Path(__file__).parent / "data" / "1_4_w_evlr.laz"
+
+UNREGISTERED_EXTRA_BYTES_LAS = (
+    Path(__file__).parent / "data" / "unregistered_extra_bytes.las"
+)
+
+ALL_LAS_FILE_PATH = [
+    SIMPLE_LAS_FILE_PATH,
+    VEGETATION1_3_LAS_FILE_PATH,
+    TEST1_4_LAS_FILE_PATH,
+    EXTRA_BYTES_LAS_FILE_PATH,
+]
+
+ALL_LAZ_FILE_PATH = [
+    SIMPLE_LAZ_FILE_PATH,
+    EXTRA_BYTES_LAZ_FILE_PATH,
+    PLANE_LAZ_FILE_PATH,
+]
+
+ALL_LAZ_BACKEND = laspy.LazBackend.detect_available()
+
+SUPPORTED_SINGULAR_EXTRA_BYTES_TYPE = [
+    "u1",
+    "u2",
+    "u4",
+    "u8",
+    "i1",
+    "i2",
+    "i4",
+    "i8",
+    "f4",
+    "f8",
+    "uint8",
+    "uint16",
+    "uint32",
+    "uint64",
+    "int8",
+    "int16",
+    "int32",
+    "int64",
+    "float32",
+    "float64",
+]
+
+SUPPORTED_ARRAY_2_EXTRA_BYTES_TYPE = [
+    f"2{base_type}" for base_type in SUPPORTED_SINGULAR_EXTRA_BYTES_TYPE
+]
+
+SUPPORTED_ARRAY_3_EXTRA_BYTES_TYPE = [
+    f"3{base_type}" for base_type in SUPPORTED_SINGULAR_EXTRA_BYTES_TYPE
+]
+
+SUPPORTED_EXTRA_BYTES_TYPE = (
+    SUPPORTED_SINGULAR_EXTRA_BYTES_TYPE
+    + SUPPORTED_ARRAY_2_EXTRA_BYTES_TYPE
+    + SUPPORTED_ARRAY_3_EXTRA_BYTES_TYPE
+)
+
+
+class NonSeekableStream:
+    """
+    Fake non stream / file object which simulates a file object
+    on which we cannot seek
+    """
+
+    def __init__(self, inner):
+        self.inner = inner
+
+    def read(self, n):
+        return self.inner.read(n)
+
+    def seekable(self):
+        return False
+
+    def close(self):
+        pass
+
+
+@pytest.fixture()
+def simple_las_path():
+    return SIMPLE_LAS_FILE_PATH
+
+
+@pytest.fixture(params=SUPPORTED_EXTRA_BYTES_TYPE)
+def extra_bytes_params(request):
+    return laspy.ExtraBytesParams(
+        name="just_a_name", type=request.param, description="laspy test ExtraBytes"
+    )
+
+
+@pytest.fixture(params=[EXTRA_BYTES_LAS_FILE_PATH, EXTRA_BYTES_LAZ_FILE_PATH], ids=repr)
+def las_file_path_with_extra_bytes(request):
+    if request.param.suffix == ".laz" and len(laspy.LazBackend.detect_available()) == 0:
+        return pytest.skip("No Laz Backend")
+    else:
+        return request.param
+
+
+@pytest.fixture(params=ALL_LAS_FILE_PATH, ids=repr)
+def las_file_path(request):
+    return request.param
+
+
+@pytest.fixture(params=ALL_LAZ_FILE_PATH, ids=repr)
+def laz_file_path(request):
+    if len(laspy.LazBackend.detect_available()) == 0:
+        return pytest.skip("No Laz Backend")
+    return request.param
+
+
+@pytest.fixture(params=ALL_LAS_FILE_PATH + ALL_LAZ_FILE_PATH, ids=repr)
+def file_path(request):
+    if len(laspy.LazBackend.detect_available()) == 0:
+        return pytest.skip("No Laz Backend")
+    return request.param
+
+
+@pytest.fixture(
+    params=ALL_LAZ_BACKEND
+    if ALL_LAZ_BACKEND
+    else [pytest.mark.skip("No Laz Backend installed")]
+)
+def laz_backend(request):
+    return request.param
+
+
+def all_las_file_path():
+    return all_las_file_path()
+
+
+@pytest.fixture()
+def mmapped_file_path(tmp_path):
+    import shutil
+
+    copied_file = shutil.copy(SIMPLE_LAS_FILE_PATH, tmp_path)
+    yield copied_file
```

### Comparing `laspy-2.4.1/tests/data/1_4_w_evlr.las` & `laspy-2.5.0/tests/data/1_4_w_evlr.las`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/1_4_w_evlr.laz` & `laspy-2.5.0/tests/data/1_4_w_evlr.laz`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/autzen.las` & `laspy-2.5.0/tests/data/autzen.las`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/autzen_geo_proj.las` & `laspy-2.5.0/tests/data/autzen_geo_proj.las`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/autzen_trim.laz` & `laspy-2.5.0/tests/data/autzen_trim.laz`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/extra.laz` & `laspy-2.5.0/tests/data/extra.laz`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/extrabytes.las` & `laspy-2.5.0/tests/data/extrabytes.las`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/plane.laz` & `laspy-2.5.0/tests/data/plane.laz`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/simple.copc.laz` & `laspy-2.5.0/tests/data/simple.copc.laz`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/simple.las` & `laspy-2.5.0/tests/data/simple.las`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/simple.laz` & `laspy-2.5.0/tests/data/simple.laz`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/simple1_1.las` & `laspy-2.5.0/tests/data/simple1_1.las`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/simple1_3.las` & `laspy-2.5.0/tests/data/simple1_3.las`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/simple1_4.las` & `laspy-2.5.0/tests/data/simple1_4.las`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/test1_4.las` & `laspy-2.5.0/tests/data/test1_4.las`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/data/vegetation_1_3.las` & `laspy-2.5.0/tests/data/vegetation_1_3.las`

 * *Files identical despite different names*

### Comparing `laspy-2.4.1/tests/test_append_mode.py` & `laspy-2.5.0/tests/test_append_mode.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,159 +1,159 @@
-import io
-import os
-
-import pytest
-
-import laspy
-from tests.test_common import simple_laz
-from typing import List, Tuple
-from tests.conftest import NonSeekableStream
-from laspy import LasHeader, ScaleAwarePointRecord, LasData
-from pathlib import Path
-
-
-def test_append(file_path):
-    """
-    Test appending
-    """
-    if file_path.suffix == ".laz" and not laspy.LazBackend.Lazrs.is_available():
-        pytest.skip("Only Lazrs backed supports appending")
-    append_self_and_check(file_path)
-
-
-def test_raises_for_laszip_backend():
-    with pytest.raises(laspy.LaspyException):
-        with laspy.open(simple_laz, mode="a", laz_backend=laspy.LazBackend.Laszip):
-            ...
-
-
-def test_append_las_with_evlrs():
-    las = append_self_and_check(os.path.dirname(__file__) + "/data/1_4_w_evlr.las")
-
-    expected_evlr = laspy.VLR(
-        user_id="pylastest", record_id=42, description="just a test evlr"
-    )
-    expected_evlr.record_data = b"Test 1 2 ... 1 2"
-
-    assert len(las.evlrs) == 1
-    evlr = las.evlrs[0]
-    assert evlr.description == expected_evlr.description
-    assert evlr.record_id == expected_evlr.record_id
-    assert evlr.user_id == expected_evlr.user_id
-    assert evlr.record_data == expected_evlr.record_data
-
-
-@pytest.mark.skipif(
-    not laspy.LazBackend.Lazrs.is_available(), reason="Lazrs is not installed"
-)
-def test_append_laz_with_evlrs():
-    las = append_self_and_check(os.path.dirname(__file__) + "/data/1_4_w_evlr.laz")
-
-    expected_evlr = laspy.VLR(
-        user_id="pylastest", record_id=42, description="just a test evlr"
-    )
-    expected_evlr.record_data = b"Test 1 2 ... 1 2"
-
-    assert len(las.evlrs) == 1
-    evlr = las.evlrs[0]
-    assert evlr.description == expected_evlr.description
-    assert evlr.record_id == expected_evlr.record_id
-    assert evlr.user_id == expected_evlr.user_id
-    assert evlr.record_data == expected_evlr.record_data
-
-
-def append_self_and_check(las_path_fixture):
-    with open(las_path_fixture, mode="rb") as f:
-        file = io.BytesIO(f.read())
-    las = laspy.read(las_path_fixture)
-    print(las.vlrs)
-    with laspy.open(file, mode="a", closefd=False) as laz_file:
-        laz_file.append_points(las.points)
-    file.seek(0, io.SEEK_SET)
-    rlas = laspy.read(file)
-    assert rlas.header.point_count == 2 * las.header.point_count
-    assert rlas.points[: rlas.header.point_count // 2] == las.points
-    assert rlas.points[rlas.header.point_count // 2 :] == las.points
-
-    return rlas
-
-
-def test_trying_to_append_in_non_seekable_raises():
-    with pytest.raises(TypeError):
-        with open(simple_laz, mode="rb") as f:
-            stream = NonSeekableStream(f)
-            with laspy.open(stream, mode="a") as lasf:
-                pass
-
-
-@pytest.mark.parametrize(
-    "points_read_counts",
-    [
-        [-1],
-        [1, -1],
-        [49_999, -1],
-        [50_000, -1],
-        [50_001, -1],
-    ],
-)
-@pytest.mark.skipif(
-    not laspy.LazBackend.Lazrs.is_available(), reason="Lazrs is not installed"
-)
-def test_write_then_append_produces_valid_cloud(points_read_counts: List[int]) -> None:
-    """
-    In this test we read a LAZ file into chunks dictated by `points_read_counts`,
-    then we reconstruct it by first writting the first chunk into a new file using write mode
-    then we append the remaining chunks to that newly created file.
-
-    At the end the input file and the one we patchworked must be the same
-    """
-
-    def iter_points(
-        points_list: List[ScaleAwarePointRecord],
-    ) -> Tuple[ScaleAwarePointRecord, slice]:
-        """
-        Returns a tuple that associates each point record in the input list
-        with the slice to be used to recover the same chunk from
-        the input file.
-        """
-        offset: int = 0
-
-        for points in points_list:
-            yield points, slice(offset, offset + len(points))
-            offset += len(points)
-
-    def check_write_append_read(
-        points_list: List[ScaleAwarePointRecord], header: LasHeader
-    ) -> None:
-        """
-        Implements the logic of first using write mode for the first
-        chunk, then appending the remaining chunks.
-
-        Checks result at the end
-        """
-        with io.BytesIO() as tmp_output:
-            with laspy.open(
-                tmp_output, "w", header=header, closefd=False, do_compress=True
-            ) as las_writer:
-                las_writer.write_points(points_list[0])
-
-            for points in points_list[1:]:
-                tmp_output.seek(0)
-                if points:
-                    with laspy.open(tmp_output, "a", closefd=False) as las_appender:
-                        las_appender.append_points(points)
-
-            tmp_output.seek(0)
-            final_cloud: LasData = laspy.read(tmp_output)
-
-            for points, selector in iter_points(points_list):
-                assert final_cloud.points[selector] == points
-
-    input_cloud_path = Path(__file__).parent / "data" / "autzen_trim.laz"
-
-    with laspy.open(input_cloud_path) as las_reader:
-        points_list: List[ScaleAwarePointRecord] = [
-            las_reader.read_points(points_read_count)
-            for points_read_count in points_read_counts
-        ]
-
-    check_write_append_read(points_list, las_reader.header)
+import io
+import os
+from pathlib import Path
+from typing import List, Tuple
+
+import pytest
+
+import laspy
+from laspy import LasData, LasHeader, ScaleAwarePointRecord
+from tests.conftest import NonSeekableStream
+from tests.test_common import simple_laz
+
+
+def test_append(file_path):
+    """
+    Test appending
+    """
+    if file_path.suffix == ".laz" and not laspy.LazBackend.Lazrs.is_available():
+        pytest.skip("Only Lazrs backed supports appending")
+    append_self_and_check(file_path)
+
+
+def test_raises_for_laszip_backend():
+    with pytest.raises(laspy.LaspyException):
+        with laspy.open(simple_laz, mode="a", laz_backend=laspy.LazBackend.Laszip):
+            ...
+
+
+def test_append_las_with_evlrs():
+    las = append_self_and_check(os.path.dirname(__file__) + "/data/1_4_w_evlr.las")
+
+    expected_evlr = laspy.VLR(
+        user_id="pylastest", record_id=42, description="just a test evlr"
+    )
+    expected_evlr.record_data = b"Test 1 2 ... 1 2"
+
+    assert len(las.evlrs) == 1
+    evlr = las.evlrs[0]
+    assert evlr.description == expected_evlr.description
+    assert evlr.record_id == expected_evlr.record_id
+    assert evlr.user_id == expected_evlr.user_id
+    assert evlr.record_data == expected_evlr.record_data
+
+
+@pytest.mark.skipif(
+    not laspy.LazBackend.Lazrs.is_available(), reason="Lazrs is not installed"
+)
+def test_append_laz_with_evlrs():
+    las = append_self_and_check(os.path.dirname(__file__) + "/data/1_4_w_evlr.laz")
+
+    expected_evlr = laspy.VLR(
+        user_id="pylastest", record_id=42, description="just a test evlr"
+    )
+    expected_evlr.record_data = b"Test 1 2 ... 1 2"
+
+    assert len(las.evlrs) == 1
+    evlr = las.evlrs[0]
+    assert evlr.description == expected_evlr.description
+    assert evlr.record_id == expected_evlr.record_id
+    assert evlr.user_id == expected_evlr.user_id
+    assert evlr.record_data == expected_evlr.record_data
+
+
+def append_self_and_check(las_path_fixture):
+    with open(las_path_fixture, mode="rb") as f:
+        file = io.BytesIO(f.read())
+    las = laspy.read(las_path_fixture)
+    print(las.vlrs)
+    with laspy.open(file, mode="a", closefd=False) as laz_file:
+        laz_file.append_points(las.points)
+    file.seek(0, io.SEEK_SET)
+    rlas = laspy.read(file)
+    assert rlas.header.point_count == 2 * las.header.point_count
+    assert rlas.points[: rlas.header.point_count // 2] == las.points
+    assert rlas.points[rlas.header.point_count // 2 :] == las.points
+
+    return rlas
+
+
+def test_trying_to_append_in_non_seekable_raises():
+    with pytest.raises(TypeError):
+        with open(simple_laz, mode="rb") as f:
+            stream = NonSeekableStream(f)
+            with laspy.open(stream, mode="a") as lasf:
+                pass
+
+
+@pytest.mark.parametrize(
+    "points_read_counts",
+    [
+        [-1],
+        [1, -1],
+        [49_999, -1],
+        [50_000, -1],
+        [50_001, -1],
+    ],
+)
+@pytest.mark.skipif(
+    not laspy.LazBackend.Lazrs.is_available(), reason="Lazrs is not installed"
+)
+def test_write_then_append_produces_valid_cloud(points_read_counts: List[int]) -> None:
+    """
+    In this test we read a LAZ file into chunks dictated by `points_read_counts`,
+    then we reconstruct it by first writting the first chunk into a new file using write mode
+    then we append the remaining chunks to that newly created file.
+
+    At the end the input file and the one we patchworked must be the same
+    """
+
+    def iter_points(
+        points_list: List[ScaleAwarePointRecord],
+    ) -> Tuple[ScaleAwarePointRecord, slice]:
+        """
+        Returns a tuple that associates each point record in the input list
+        with the slice to be used to recover the same chunk from
+        the input file.
+        """
+        offset: int = 0
+
+        for points in points_list:
+            yield points, slice(offset, offset + len(points))
+            offset += len(points)
+
+    def check_write_append_read(
+        points_list: List[ScaleAwarePointRecord], header: LasHeader
+    ) -> None:
+        """
+        Implements the logic of first using write mode for the first
+        chunk, then appending the remaining chunks.
+
+        Checks result at the end
+        """
+        with io.BytesIO() as tmp_output:
+            with laspy.open(
+                tmp_output, "w", header=header, closefd=False, do_compress=True
+            ) as las_writer:
+                las_writer.write_points(points_list[0])
+
+            for points in points_list[1:]:
+                tmp_output.seek(0)
+                if points:
+                    with laspy.open(tmp_output, "a", closefd=False) as las_appender:
+                        las_appender.append_points(points)
+
+            tmp_output.seek(0)
+            final_cloud: LasData = laspy.read(tmp_output)
+
+            for points, selector in iter_points(points_list):
+                assert final_cloud.points[selector] == points
+
+    input_cloud_path = Path(__file__).parent / "data" / "autzen_trim.laz"
+
+    with laspy.open(input_cloud_path) as las_reader:
+        points_list: List[ScaleAwarePointRecord] = [
+            las_reader.read_points(points_read_count)
+            for points_read_count in points_read_counts
+        ]
+
+    check_write_append_read(points_list, las_reader.header)
```

### Comparing `laspy-2.4.1/tests/test_chunk_read_write.py` & `laspy-2.5.0/tests/test_chunk_read_write.py`

 * *Ordering differences only*

 * *Files 23% similar despite different names*

```diff
@@ -1,112 +1,112 @@
-"""
-Tests related to the 'chunked' reading and writing
-"""
-import io
-import math
-
-import numpy as np
-import pytest
-
-import laspy
-
-
-def check_chunked_reading_gives_expected_points(
-    groundtruth_las: laspy.LasData, reader: laspy.LasReader, iter_size: int
-):
-    """Checks that the points read by the reader are the same as groundtruth points."""
-    assert groundtruth_las.point_format == reader.header.point_format
-    for i, points in enumerate(reader.chunk_iterator(iter_size)):
-        expected_points = groundtruth_las.points[i * iter_size : (i + 1) * iter_size]
-        for dim_name in points.array.dtype.names:
-            assert np.allclose(
-                expected_points[dim_name], points[dim_name]
-            ), f"{dim_name} not equal"
-
-
-def test_chunked_las_reading_gives_expected_points(las_file_path):
-    """
-    Test chunked LAS reading
-    """
-    with laspy.open(las_file_path) as las_reader:
-        with laspy.open(las_file_path) as reader:
-            las = las_reader.read()
-            check_chunked_reading_gives_expected_points(las, reader, iter_size=50)
-
-
-def test_chunked_laz_reading_gives_expected_points(laz_file_path, laz_backend):
-    """
-    Test LAZ reading in chunked mode with different backends
-    """
-    with laspy.open(laz_file_path) as las_reader:
-        with laspy.open(laz_file_path, laz_backend=laz_backend) as laz_reader:
-            expected_las = las_reader.read()
-            check_chunked_reading_gives_expected_points(
-                expected_las, laz_reader, iter_size=50
-            )
-
-
-@pytest.mark.parametrize("backend", laspy.LazBackend.detect_available() + (None,))
-def test_chunked_writing_gives_expected_points(file_path, backend):
-    """
-    Write in chunked mode then test that the points are correct
-    """
-    original_las = laspy.read(file_path)
-    iter_size = 51
-
-    do_compress = True if backend is not None else False
-
-    with io.BytesIO() as tmp_output:
-        with laspy.open(
-            tmp_output,
-            mode="w",
-            closefd=False,
-            header=original_las.header,
-            do_compress=do_compress,
-            laz_backend=backend,
-        ) as las:
-            for i in range(int(math.ceil(len(original_las.points) / iter_size))):
-                original_points = original_las.points[
-                    i * iter_size : (i + 1) * iter_size
-                ]
-                las.write_points(original_points)
-
-        tmp_output.seek(0)
-        with laspy.open(tmp_output, closefd=False) as reader:
-            check_chunked_reading_gives_expected_points(original_las, reader, iter_size)
-
-
-@pytest.mark.parametrize("backend", laspy.LazBackend.detect_available() + (None,))
-def test_chunked_dimension_modification(file_path, backend):
-    """
-    Test that when using chunked mode, if we modify the values in the chunks
-    before writing them the values are actually modified.
-    """
-
-    mem_dest = io.BytesIO()
-
-    # Read of file in chunked mode modify some values before writing them
-    # to a new file
-    with laspy.open(file_path, laz_backend=backend) as reader:
-        with laspy.open(
-            mem_dest, mode="w", laz_backend=backend, header=reader.header, closefd=False
-        ) as dest:
-            for points in reader.chunk_iterator(50):
-                # try a sub field
-                points.classification += 1
-                # try a normal field
-                points.user_data += 2
-                # try a scaled field
-                points.x += 10.0
-
-                dest.write_points(points)
-
-    mem_dest.seek(0)
-
-    # Prepare out ground truth
-    ground_truth_las = laspy.read(file_path)
-    ground_truth_las.classification += 1
-    ground_truth_las.user_data += 2
-    ground_truth_las.x += 10.0
-
-    reader = laspy.open(mem_dest, laz_backend=backend)
-    check_chunked_reading_gives_expected_points(ground_truth_las, reader, 42)
+"""
+Tests related to the 'chunked' reading and writing
+"""
+import io
+import math
+
+import numpy as np
+import pytest
+
+import laspy
+
+
+def check_chunked_reading_gives_expected_points(
+    groundtruth_las: laspy.LasData, reader: laspy.LasReader, iter_size: int
+):
+    """Checks that the points read by the reader are the same as groundtruth points."""
+    assert groundtruth_las.point_format == reader.header.point_format
+    for i, points in enumerate(reader.chunk_iterator(iter_size)):
+        expected_points = groundtruth_las.points[i * iter_size : (i + 1) * iter_size]
+        for dim_name in points.array.dtype.names:
+            assert np.allclose(
+                expected_points[dim_name], points[dim_name]
+            ), f"{dim_name} not equal"
+
+
+def test_chunked_las_reading_gives_expected_points(las_file_path):
+    """
+    Test chunked LAS reading
+    """
+    with laspy.open(las_file_path) as las_reader:
+        with laspy.open(las_file_path) as reader:
+            las = las_reader.read()
+            check_chunked_reading_gives_expected_points(las, reader, iter_size=50)
+
+
+def test_chunked_laz_reading_gives_expected_points(laz_file_path, laz_backend):
+    """
+    Test LAZ reading in chunked mode with different backends
+    """
+    with laspy.open(laz_file_path) as las_reader:
+        with laspy.open(laz_file_path, laz_backend=laz_backend) as laz_reader:
+            expected_las = las_reader.read()
+            check_chunked_reading_gives_expected_points(
+                expected_las, laz_reader, iter_size=50
+            )
+
+
+@pytest.mark.parametrize("backend", laspy.LazBackend.detect_available() + (None,))
+def test_chunked_writing_gives_expected_points(file_path, backend):
+    """
+    Write in chunked mode then test that the points are correct
+    """
+    original_las = laspy.read(file_path)
+    iter_size = 51
+
+    do_compress = True if backend is not None else False
+
+    with io.BytesIO() as tmp_output:
+        with laspy.open(
+            tmp_output,
+            mode="w",
+            closefd=False,
+            header=original_las.header,
+            do_compress=do_compress,
+            laz_backend=backend,
+        ) as las:
+            for i in range(int(math.ceil(len(original_las.points) / iter_size))):
+                original_points = original_las.points[
+                    i * iter_size : (i + 1) * iter_size
+                ]
+                las.write_points(original_points)
+
+        tmp_output.seek(0)
+        with laspy.open(tmp_output, closefd=False) as reader:
+            check_chunked_reading_gives_expected_points(original_las, reader, iter_size)
+
+
+@pytest.mark.parametrize("backend", laspy.LazBackend.detect_available() + (None,))
+def test_chunked_dimension_modification(file_path, backend):
+    """
+    Test that when using chunked mode, if we modify the values in the chunks
+    before writing them the values are actually modified.
+    """
+
+    mem_dest = io.BytesIO()
+
+    # Read of file in chunked mode modify some values before writing them
+    # to a new file
+    with laspy.open(file_path, laz_backend=backend) as reader:
+        with laspy.open(
+            mem_dest, mode="w", laz_backend=backend, header=reader.header, closefd=False
+        ) as dest:
+            for points in reader.chunk_iterator(50):
+                # try a sub field
+                points.classification += 1
+                # try a normal field
+                points.user_data += 2
+                # try a scaled field
+                points.x += 10.0
+
+                dest.write_points(points)
+
+    mem_dest.seek(0)
+
+    # Prepare out ground truth
+    ground_truth_las = laspy.read(file_path)
+    ground_truth_las.classification += 1
+    ground_truth_las.user_data += 2
+    ground_truth_las.x += 10.0
+
+    reader = laspy.open(mem_dest, laz_backend=backend)
+    check_chunked_reading_gives_expected_points(ground_truth_las, reader, 42)
```

### Comparing `laspy-2.4.1/tests/test_common.py` & `laspy-2.5.0/tests/test_common.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,402 +1,426 @@
-from pathlib import Path
-
-import numpy as np
-import pytest
-
-import laspy
-from laspy.lib import write_then_read_again
-from . import conftest
-
-simple_las = conftest.SIMPLE_LAS_FILE_PATH
-simple_laz = conftest.SIMPLE_LAZ_FILE_PATH
-vegetation1_3_las = conftest.VEGETATION1_3_LAS_FILE_PATH
-test1_4_las = conftest.TEST1_4_LAS_FILE_PATH
-extra_bytes_las = conftest.EXTRA_BYTES_LAS_FILE_PATH
-extra_bytes_laz = conftest.EXTRA_BYTES_LAZ_FILE_PATH
-plane_laz = conftest.PLANE_LAZ_FILE_PATH
-autzen_las = conftest.AUTZEN_FILE_PATH
-autzen_geo_proj_las = conftest.AUTZEN_GEO_PROJ_FILE_PATH
-
-if not laspy.LazBackend.detect_available():
-    do_compression = [False]
-    all_file_paths = [simple_las, vegetation1_3_las, test1_4_las, extra_bytes_las]
-else:
-    do_compression = [False, True]
-    all_file_paths = [
-        simple_las,
-        simple_laz,
-        vegetation1_3_las,
-        test1_4_las,
-        plane_laz,
-        extra_bytes_laz,
-        extra_bytes_las,
-    ]
-
-
-@pytest.fixture(params=all_file_paths)
-def las(request):
-    return laspy.read(request.param)
-
-
-@pytest.fixture(params=[simple_las, vegetation1_3_las])
-def all_las_but_1_4(request):
-    return laspy.read(request.param)
-
-
-@pytest.fixture(params=[simple_las, vegetation1_3_las, test1_4_las, extra_bytes_las])
-def las_path_fixture(request):
-    return request.param
-
-
-@pytest.fixture(params=[simple_laz, extra_bytes_laz, plane_laz])
-def all_laz_path(request):
-    return request.param
-
-
-def dim_does_not_exists(las, dim_name):
-    try:
-        _ = getattr(las, dim_name)
-    except AttributeError:
-        return True
-    return False
-
-
-def dim_does_exists(las, dim_name):
-    try:
-        _ = getattr(las, dim_name)
-    except AttributeError:
-        return False
-    return True
-
-
-def test_change_format(las):
-    in_version = las.header.version
-
-    las = laspy.convert(las, point_format_id=2)
-    las = write_then_read_again(las)
-    assert las.points.point_format.id == 2
-    assert las.header.point_format.id == 2
-    assert las.header.version == in_version
-    assert dim_does_not_exists(las, "gps_time")
-
-    las = laspy.convert(las, point_format_id=1)
-    las = write_then_read_again(las)
-    assert las.points.point_format.id == 1
-    assert las.header.point_format.id == 1
-    assert las.header.version == in_version
-    assert dim_does_not_exists(las, "red")
-    assert dim_does_not_exists(las, "green")
-    assert dim_does_not_exists(las, "blue")
-
-    las = laspy.convert(las, point_format_id=0)
-    las = write_then_read_again(las)
-    assert las.points.point_format.id == 0
-    assert las.header.point_format.id == 0
-    assert las.header.version == in_version
-    assert dim_does_not_exists(las, "red")
-    assert dim_does_not_exists(las, "green")
-    assert dim_does_not_exists(las, "blue")
-    assert dim_does_not_exists(las, "gps_time")
-
-    las = laspy.convert(las, point_format_id=8)
-    las = write_then_read_again(las)
-    assert str(las.header.version) == "1.4"
-    assert las.points.point_format.id == 8
-    assert las.header.point_format.id == 8
-    assert dim_does_exists(las, "red")
-    assert dim_does_exists(las, "green")
-    assert dim_does_exists(las, "blue")
-    assert dim_does_exists(las, "nir")
-
-    las = laspy.convert(las, point_format_id=7)
-    las = write_then_read_again(las)
-    assert str(las.header.version) == "1.4"
-    assert las.points.point_format.id == 7
-    assert las.header.point_format.id == 7
-    assert dim_does_exists(las, "red")
-    assert dim_does_exists(las, "green")
-    assert dim_does_exists(las, "blue")
-    assert dim_does_not_exists(las, "nir")
-
-    las = laspy.convert(las, point_format_id=6)
-    las = write_then_read_again(las)
-    assert str(las.header.version) == "1.4"
-    assert las.points.point_format.id == 6
-    assert las.header.point_format.id == 6
-    assert dim_does_not_exists(las, "red")
-    assert dim_does_not_exists(las, "green")
-    assert dim_does_not_exists(las, "blue")
-    assert dim_does_not_exists(las, "nir")
-
-
-def test_rw_all_set_one(las):
-    for dim_name in las.point_format.dimension_names:
-        las[dim_name][:] = 1
-
-    for dim_name in las.point_format.dimension_names:
-        assert np.alltrue(las[dim_name] == 1), "{} not equal".format(dim_name)
-
-    las2 = write_then_read_again(las)
-
-    for dim_name in las.point_format.dimension_names:
-        assert np.alltrue(las[dim_name] == las2[dim_name]), "{} not equal".format(
-            dim_name
-        )
-
-
-def test_coords_do_not_break(las):
-    xs, ys, zs = las.x, las.y, las.z
-
-    las.x = xs
-    las.y = ys
-    las.z = zs
-
-    assert np.allclose(xs, las.x)
-    assert np.allclose(ys, las.y)
-    assert np.allclose(zs, las.z)
-
-
-def test_coords_when_setting_offsets_and_scales(las):
-    new_las = laspy.create()
-
-    new_las.header.offsets = las.header.offsets
-    new_las.header.scales = las.header.scales
-
-    new_las.x = las.x
-    new_las.y = las.y
-    new_las.z = las.z
-
-    assert np.allclose(las.x, new_las.x)
-    assert np.allclose(las.y, new_las.y)
-    assert np.allclose(las.z, new_las.z)
-
-
-def test_coords_when_using_create_from_header(las):
-    new_las = laspy.LasData(las.header)
-
-    new_las.x = las.x
-    new_las.y = las.y
-    new_las.z = las.z
-
-    assert np.allclose(las.x, new_las.x)
-    assert np.allclose(las.y, new_las.y)
-    assert np.allclose(las.z, new_las.z)
-
-
-def test_slicing(las):
-    las.points = las.points[len(las.points) // 2 :]
-
-
-@pytest.mark.parametrize("do_compress", do_compression)
-def test_can_write_then_re_read_files(las, do_compress):
-    _las = write_then_read_again(las, do_compress=do_compress)
-
-
-def test_point_record_setitem_scaled_view():
-    las = laspy.read(simple_las)
-    las.add_extra_dim(
-        laspy.ExtraBytesParams(
-            "lol", "uint64", scales=np.array([2.0]), offsets=np.array([0.0])
-        )
-    )
-
-    new_values = np.ones(len(las.points)) * 4
-    las.lol = new_values
-
-    assert np.allclose(las.lol, new_values)
-
-
-def test_laspy_file_raises():
-    with pytest.raises(laspy.errors.LaspyException):
-        laspy.file.File("some path")
-
-
-def test_lasdata_setitem_xyz_with_2d_array():
-    las = laspy.read(simple_las)
-
-    xyz = np.ones(len(las), dtype="3f8")
-    xyz[..., 1] = 2.0
-    xyz[..., 2] = 3.0
-
-    las[["x", "y", "z"]] = xyz
-
-    assert np.all(las.x == xyz[..., 0])
-    assert np.all(las.y == xyz[..., 1])
-    assert np.all(las.z == xyz[..., 2])
-
-
-def test_lasdata_setitem_xyz_with_structured_array():
-    las = laspy.read(simple_las)
-
-    xyz = np.ones(len(las), dtype=[("x", "f8"), ("y", "f8"), ("z", "f8")])
-    xyz["y"] = 2.0
-    xyz["z"] = 3.0
-
-    las[["x", "y", "z"]] = xyz
-
-    assert np.all(las.x == xyz["x"])
-    assert np.all(las.y == xyz["y"])
-    assert np.all(las.z == xyz["z"])
-
-
-def test_lasdata_setitem_one_dimension():
-    las = laspy.read(simple_las)
-
-    las[["x"]] = np.ones(len(las), "f8") * 17.0
-    assert np.all(las.x == 17.0)
-
-
-def test_lasdata_setitem_works_with_subfields():
-    las = laspy.read(simple_las)
-
-    new_values = np.ones(
-        len(las), dtype=[("classification", "u1"), ("return_number", "u1")]
-    )
-    new_values["classification"] = 23
-    new_values["return_number"] = 2
-
-    las[["classification", "return_number"]] = new_values
-    assert np.all(las.classification == 23)
-    assert np.all(las.return_number == 2)
-
-
-def test_las_data_getitem_indices():
-    las = laspy.read(simple_las)
-    las.classification[:] = 0
-
-    indices = np.array([1, 2, 3, 4])
-    sliced_las = las[indices]
-    sliced_las.classification[:] = 1
-
-    assert np.all(sliced_las.classification == 1)
-    # We expect sliced_las to give us a copy,
-    # So original las is no modified
-    assert np.all(las.classification == 0)
-
-
-def test_las_data_getitem_slice():
-    las = laspy.read(simple_las)
-    las.classification[:] = 0
-
-    sliced_las = las[0:10]
-    sliced_las.classification[:] = 1
-
-    assert np.all(sliced_las.classification == 1)
-    # Slicing does not trigger, advanced indexing
-    # so the underlying array is not a copy
-    # https://numpy.org/doc/stable/reference/arrays.indexing.html
-    assert np.all(las.classification[:10] == 1)
-    assert np.all(las.classification[10:] == 0)
-
-
-def test_change_scaling():
-    """Check our change scaling method.
-
-    We expect the scaled x,y,z not to change
-    while the unscaled (integers) X,Y,Z should change.
-    """
-    hdr = laspy.LasHeader()
-    hdr.offsets = np.array([0.0, 0.0, 0.0])
-    hdr.scales = np.array([1.0, 1.0, 1.0])
-
-    las = laspy.LasData(hdr)
-
-    las["x"] = np.array([1, 2, 3, 4])
-    las["y"] = np.array([1, 2, 3, 4])
-    las["z"] = np.array([1, 2, 3, 4])
-
-    assert np.all(las.x == [1, 2, 3, 4])
-    assert np.all(las.y == [1, 2, 3, 4])
-    assert np.all(las.z == [1, 2, 3, 4])
-
-    assert np.all(las.X == [1, 2, 3, 4])
-    assert np.all(las.Y == [1, 2, 3, 4])
-    assert np.all(las.Z == [1, 2, 3, 4])
-
-    saved_offsets = las.header.offsets.copy()
-    las.change_scaling(scales=[0.5, 0.1, 0.01])
-
-    assert np.all(las.header.scales == [0.5, 0.1, 0.01])
-    assert np.all(las.header.offsets == saved_offsets)
-
-    assert np.all(las.x == [1, 2, 3, 4])
-    assert np.all(las.y == [1, 2, 3, 4])
-    assert np.all(las.z == [1, 2, 3, 4])
-
-    assert np.all(las.X == [2, 4, 6, 8])
-    assert np.all(las.Y == [10, 20, 30, 40])
-    assert np.all(las.Z == [100, 200, 300, 400])
-
-    saved_scales = las.header.scales.copy()
-    las.change_scaling(offsets=[1, 20, 30])
-
-    assert np.all(las.header.scales == saved_scales)
-    assert np.all(las.header.offsets == [1, 20, 30])
-
-    assert np.all(las.x == [1, 2, 3, 4])
-    assert np.all(las.y == [1, 2, 3, 4])
-    assert np.all(las.z == [1, 2, 3, 4])
-
-    assert np.all(las.X == [0, 2, 4, 6])
-    assert np.all(las.Y == [-190, -180, -170, -160])
-    assert np.all(las.Z == [-2900, -2800, -2700, -2600])
-
-
-def test_setting_x_y_z_on_las_data():
-    """
-    The goal of this test if to make sure that when setting the `x`,`y` and `z`
-    attribute of a LasData object, the X,Y,Z version of the coordinates
-    are properly set in the inner point record
-    """
-    las = laspy.read(simple_las)
-
-    new_las = laspy.create()
-
-    new_las.x = las.x
-    new_las.y = las.y
-    new_las.z = las.z
-
-    assert np.all(new_las.x == las.x)
-    assert np.all(new_las.X == las.X)
-    assert np.all(new_las.y == las.y)
-    assert np.all(new_las.Y == las.Y)
-    assert np.all(new_las.z == las.z)
-    assert np.all(new_las.Z == las.Z)
-
-    new_las = laspy.lib.write_then_read_again(new_las)
-
-    assert np.all(new_las.x == las.x)
-    assert np.all(new_las.X == las.X)
-    assert np.all(new_las.y == las.y)
-    assert np.all(new_las.Y == las.Y)
-    assert np.all(new_las.z == las.z)
-    assert np.all(new_las.Z == las.Z)
-
-
-def test_setting_xyz_on_las_data():
-    """
-    The goal of this test if to make sure that when setting the `xyz`
-    attribute of a LasData object, the X,Y,Z version of the coordinates
-    are properly set in the inner point record
-    """
-    las = laspy.read(simple_las)
-
-    new_las = laspy.create()
-
-    new_las.xyz = las.xyz
-
-    assert np.all(new_las.x == las.x)
-    assert np.all(new_las.X == las.X)
-    assert np.all(new_las.y == las.y)
-    assert np.all(new_las.Y == las.Y)
-    assert np.all(new_las.z == las.z)
-    assert np.all(new_las.Z == las.Z)
-
-    new_las = laspy.lib.write_then_read_again(new_las)
-
-    assert np.all(new_las.x == las.x)
-    assert np.all(new_las.X == las.X)
-    assert np.all(new_las.y == las.y)
-    assert np.all(new_las.Y == las.Y)
-    assert np.all(new_las.z == las.z)
-    assert np.all(new_las.Z == las.Z)
+import io
+from pathlib import Path
+
+import numpy as np
+import pytest
+
+import laspy
+from laspy.lib import write_then_read_again
+
+from . import conftest
+
+simple_las = conftest.SIMPLE_LAS_FILE_PATH
+simple_laz = conftest.SIMPLE_LAZ_FILE_PATH
+vegetation1_3_las = conftest.VEGETATION1_3_LAS_FILE_PATH
+test1_4_las = conftest.TEST1_4_LAS_FILE_PATH
+extra_bytes_las = conftest.EXTRA_BYTES_LAS_FILE_PATH
+extra_bytes_laz = conftest.EXTRA_BYTES_LAZ_FILE_PATH
+plane_laz = conftest.PLANE_LAZ_FILE_PATH
+autzen_las = conftest.AUTZEN_FILE_PATH
+autzen_geo_proj_las = conftest.AUTZEN_GEO_PROJ_FILE_PATH
+
+if not laspy.LazBackend.detect_available():
+    do_compression = [False]
+    all_file_paths = [simple_las, vegetation1_3_las, test1_4_las, extra_bytes_las]
+else:
+    do_compression = [False, True]
+    all_file_paths = [
+        simple_las,
+        simple_laz,
+        vegetation1_3_las,
+        test1_4_las,
+        plane_laz,
+        extra_bytes_laz,
+        extra_bytes_las,
+    ]
+
+
+@pytest.fixture(params=all_file_paths)
+def las(request):
+    return laspy.read(request.param)
+
+
+@pytest.fixture(params=[simple_las, vegetation1_3_las])
+def all_las_but_1_4(request):
+    return laspy.read(request.param)
+
+
+@pytest.fixture(params=[simple_las, vegetation1_3_las, test1_4_las, extra_bytes_las])
+def las_path_fixture(request):
+    return request.param
+
+
+@pytest.fixture(params=[simple_laz, extra_bytes_laz, plane_laz])
+def all_laz_path(request):
+    return request.param
+
+
+def dim_does_not_exists(las, dim_name):
+    try:
+        _ = getattr(las, dim_name)
+    except AttributeError:
+        return True
+    return False
+
+
+def dim_does_exists(las, dim_name):
+    try:
+        _ = getattr(las, dim_name)
+    except AttributeError:
+        return False
+    return True
+
+
+def test_change_format(las):
+    in_version = las.header.version
+
+    las = laspy.convert(las, point_format_id=2)
+    las = write_then_read_again(las)
+    assert las.points.point_format.id == 2
+    assert las.header.point_format.id == 2
+    assert las.header.version == in_version
+    assert dim_does_not_exists(las, "gps_time")
+
+    las = laspy.convert(las, point_format_id=1)
+    las = write_then_read_again(las)
+    assert las.points.point_format.id == 1
+    assert las.header.point_format.id == 1
+    assert las.header.version == in_version
+    assert dim_does_not_exists(las, "red")
+    assert dim_does_not_exists(las, "green")
+    assert dim_does_not_exists(las, "blue")
+
+    las = laspy.convert(las, point_format_id=0)
+    las = write_then_read_again(las)
+    assert las.points.point_format.id == 0
+    assert las.header.point_format.id == 0
+    assert las.header.version == in_version
+    assert dim_does_not_exists(las, "red")
+    assert dim_does_not_exists(las, "green")
+    assert dim_does_not_exists(las, "blue")
+    assert dim_does_not_exists(las, "gps_time")
+
+    las = laspy.convert(las, point_format_id=8)
+    las = write_then_read_again(las)
+    assert str(las.header.version) == "1.4"
+    assert las.points.point_format.id == 8
+    assert las.header.point_format.id == 8
+    assert dim_does_exists(las, "red")
+    assert dim_does_exists(las, "green")
+    assert dim_does_exists(las, "blue")
+    assert dim_does_exists(las, "nir")
+
+    las = laspy.convert(las, point_format_id=7)
+    las = write_then_read_again(las)
+    assert str(las.header.version) == "1.4"
+    assert las.points.point_format.id == 7
+    assert las.header.point_format.id == 7
+    assert dim_does_exists(las, "red")
+    assert dim_does_exists(las, "green")
+    assert dim_does_exists(las, "blue")
+    assert dim_does_not_exists(las, "nir")
+
+    las = laspy.convert(las, point_format_id=6)
+    las = write_then_read_again(las)
+    assert str(las.header.version) == "1.4"
+    assert las.points.point_format.id == 6
+    assert las.header.point_format.id == 6
+    assert dim_does_not_exists(las, "red")
+    assert dim_does_not_exists(las, "green")
+    assert dim_does_not_exists(las, "blue")
+    assert dim_does_not_exists(las, "nir")
+
+
+def test_rw_all_set_one(las):
+    for dim_name in las.point_format.dimension_names:
+        las[dim_name][:] = 1
+
+    for dim_name in las.point_format.dimension_names:
+        assert np.alltrue(las[dim_name] == 1), "{} not equal".format(dim_name)
+
+    las2 = write_then_read_again(las)
+
+    for dim_name in las.point_format.dimension_names:
+        assert np.alltrue(las[dim_name] == las2[dim_name]), "{} not equal".format(
+            dim_name
+        )
+
+
+def test_coords_do_not_break(las):
+    xs, ys, zs = las.x, las.y, las.z
+
+    las.x = xs
+    las.y = ys
+    las.z = zs
+
+    assert np.allclose(xs, las.x)
+    assert np.allclose(ys, las.y)
+    assert np.allclose(zs, las.z)
+
+
+def test_coords_when_setting_offsets_and_scales(las):
+    new_las = laspy.create()
+
+    new_las.header.offsets = las.header.offsets
+    new_las.header.scales = las.header.scales
+
+    new_las.x = las.x
+    new_las.y = las.y
+    new_las.z = las.z
+
+    assert np.allclose(las.x, new_las.x)
+    assert np.allclose(las.y, new_las.y)
+    assert np.allclose(las.z, new_las.z)
+
+
+def test_coords_when_using_create_from_header(las):
+    new_las = laspy.LasData(las.header)
+
+    new_las.x = las.x
+    new_las.y = las.y
+    new_las.z = las.z
+
+    assert np.allclose(las.x, new_las.x)
+    assert np.allclose(las.y, new_las.y)
+    assert np.allclose(las.z, new_las.z)
+
+
+def test_slicing(las):
+    las.points = las.points[len(las.points) // 2 :]
+
+
+@pytest.mark.parametrize("do_compress", do_compression)
+def test_can_write_then_re_read_files(las, do_compress):
+    _las = write_then_read_again(las, do_compress=do_compress)
+
+
+def test_point_record_setitem_scaled_view():
+    las = laspy.read(simple_las)
+    las.add_extra_dim(
+        laspy.ExtraBytesParams(
+            "lol", "uint64", scales=np.array([2.0]), offsets=np.array([0.0])
+        )
+    )
+
+    new_values = np.ones(len(las.points)) * 4
+    las.lol = new_values
+
+    assert np.allclose(las.lol, new_values)
+
+
+def test_laspy_file_raises():
+    with pytest.raises(laspy.errors.LaspyException):
+        laspy.file.File("some path")
+
+
+def test_lasdata_setitem_xyz_with_2d_array():
+    las = laspy.read(simple_las)
+
+    xyz = np.ones(len(las), dtype="3f8")
+    xyz[..., 1] = 2.0
+    xyz[..., 2] = 3.0
+
+    las[["x", "y", "z"]] = xyz
+
+    assert np.all(las.x == xyz[..., 0])
+    assert np.all(las.y == xyz[..., 1])
+    assert np.all(las.z == xyz[..., 2])
+
+
+def test_lasdata_setitem_xyz_with_structured_array():
+    las = laspy.read(simple_las)
+
+    xyz = np.ones(len(las), dtype=[("x", "f8"), ("y", "f8"), ("z", "f8")])
+    xyz["y"] = 2.0
+    xyz["z"] = 3.0
+
+    las[["x", "y", "z"]] = xyz
+
+    assert np.all(las.x == xyz["x"])
+    assert np.all(las.y == xyz["y"])
+    assert np.all(las.z == xyz["z"])
+
+
+def test_lasdata_setitem_one_dimension():
+    las = laspy.read(simple_las)
+
+    las[["x"]] = np.ones(len(las), "f8") * 17.0
+    assert np.all(las.x == 17.0)
+
+
+def test_lasdata_setitem_works_with_subfields():
+    las = laspy.read(simple_las)
+
+    new_values = np.ones(
+        len(las), dtype=[("classification", "u1"), ("return_number", "u1")]
+    )
+    new_values["classification"] = 23
+    new_values["return_number"] = 2
+
+    las[["classification", "return_number"]] = new_values
+    assert np.all(las.classification == 23)
+    assert np.all(las.return_number == 2)
+
+
+def test_las_data_getitem_indices():
+    las = laspy.read(simple_las)
+    las.classification[:] = 0
+
+    indices = np.array([1, 2, 3, 4])
+    sliced_las = las[indices]
+    sliced_las.classification[:] = 1
+
+    assert np.all(sliced_las.classification == 1)
+    # We expect sliced_las to give us a copy,
+    # So original las is no modified
+    assert np.all(las.classification == 0)
+
+
+def test_las_data_getitem_slice():
+    las = laspy.read(simple_las)
+    las.classification[:] = 0
+
+    sliced_las = las[0:10]
+    sliced_las.classification[:] = 1
+
+    assert np.all(sliced_las.classification == 1)
+    # Slicing does not trigger, advanced indexing
+    # so the underlying array is not a copy
+    # https://numpy.org/doc/stable/reference/arrays.indexing.html
+    assert np.all(las.classification[:10] == 1)
+    assert np.all(las.classification[10:] == 0)
+
+
+def test_change_scaling():
+    """Check our change scaling method.
+
+    We expect the scaled x,y,z not to change
+    while the unscaled (integers) X,Y,Z should change.
+    """
+    hdr = laspy.LasHeader()
+    hdr.offsets = np.array([0.0, 0.0, 0.0])
+    hdr.scales = np.array([1.0, 1.0, 1.0])
+
+    las = laspy.LasData(hdr)
+
+    las["x"] = np.array([1, 2, 3, 4])
+    las["y"] = np.array([1, 2, 3, 4])
+    las["z"] = np.array([1, 2, 3, 4])
+
+    assert np.all(las.x == [1, 2, 3, 4])
+    assert np.all(las.y == [1, 2, 3, 4])
+    assert np.all(las.z == [1, 2, 3, 4])
+
+    assert np.all(las.X == [1, 2, 3, 4])
+    assert np.all(las.Y == [1, 2, 3, 4])
+    assert np.all(las.Z == [1, 2, 3, 4])
+
+    saved_offsets = las.header.offsets.copy()
+    las.change_scaling(scales=[0.5, 0.1, 0.01])
+
+    assert np.all(las.header.scales == [0.5, 0.1, 0.01])
+    assert np.all(las.header.offsets == saved_offsets)
+
+    assert np.all(las.x == [1, 2, 3, 4])
+    assert np.all(las.y == [1, 2, 3, 4])
+    assert np.all(las.z == [1, 2, 3, 4])
+
+    assert np.all(las.X == [2, 4, 6, 8])
+    assert np.all(las.Y == [10, 20, 30, 40])
+    assert np.all(las.Z == [100, 200, 300, 400])
+
+    saved_scales = las.header.scales.copy()
+    las.change_scaling(offsets=[1, 20, 30])
+
+    assert np.all(las.header.scales == saved_scales)
+    assert np.all(las.header.offsets == [1, 20, 30])
+
+    assert np.all(las.x == [1, 2, 3, 4])
+    assert np.all(las.y == [1, 2, 3, 4])
+    assert np.all(las.z == [1, 2, 3, 4])
+
+    assert np.all(las.X == [0, 2, 4, 6])
+    assert np.all(las.Y == [-190, -180, -170, -160])
+    assert np.all(las.Z == [-2900, -2800, -2700, -2600])
+
+
+def test_setting_x_y_z_on_las_data():
+    """
+    The goal of this test if to make sure that when setting the `x`,`y` and `z`
+    attribute of a LasData object, the X,Y,Z version of the coordinates
+    are properly set in the inner point record
+    """
+    las = laspy.read(simple_las)
+
+    new_las = laspy.create()
+
+    new_las.x = las.x
+    new_las.y = las.y
+    new_las.z = las.z
+
+    assert np.all(new_las.x == las.x)
+    assert np.all(new_las.X == las.X)
+    assert np.all(new_las.y == las.y)
+    assert np.all(new_las.Y == las.Y)
+    assert np.all(new_las.z == las.z)
+    assert np.all(new_las.Z == las.Z)
+
+    new_las = laspy.lib.write_then_read_again(new_las)
+
+    assert np.all(new_las.x == las.x)
+    assert np.all(new_las.X == las.X)
+    assert np.all(new_las.y == las.y)
+    assert np.all(new_las.Y == las.Y)
+    assert np.all(new_las.z == las.z)
+    assert np.all(new_las.Z == las.Z)
+
+
+def test_setting_xyz_on_las_data():
+    """
+    The goal of this test if to make sure that when setting the `xyz`
+    attribute of a LasData object, the X,Y,Z version of the coordinates
+    are properly set in the inner point record
+    """
+    las = laspy.read(simple_las)
+
+    new_las = laspy.create()
+
+    new_las.xyz = las.xyz
+
+    assert np.all(new_las.x == las.x)
+    assert np.all(new_las.X == las.X)
+    assert np.all(new_las.y == las.y)
+    assert np.all(new_las.Y == las.Y)
+    assert np.all(new_las.z == las.z)
+    assert np.all(new_las.Z == las.Z)
+
+    new_las = laspy.lib.write_then_read_again(new_las)
+
+    assert np.all(new_las.x == las.x)
+    assert np.all(new_las.X == las.X)
+    assert np.all(new_las.y == las.y)
+    assert np.all(new_las.Y == las.Y)
+    assert np.all(new_las.z == las.z)
+    assert np.all(new_las.Z == las.Z)
+
+
+def test_input_is_properly_closed_if_opening_fails():
+    data = io.BytesIO()
+    assert data.closed is False
+
+    # This failed because file is empty
+    # so its the LasReader.__init__ that fails to read the header
+    # We should still close the input in that case
+    with pytest.raises(laspy.errors.LaspyException):
+        _ = laspy.read(data)
+
+    assert data.closed is True
+
+    # Same but with closefd = False, meaning we should not close
+    data = io.BytesIO()
+    assert data.closed is False
+
+    with pytest.raises(laspy.errors.LaspyException):
+        _ = laspy.read(data, closefd=False)
+
+    assert data.closed is False
```

### Comparing `laspy-2.4.1/tests/test_constants.py` & `laspy-2.5.0/tests/test_constants.py`

 * *Ordering differences only*

 * *Files 20% similar despite different names*

```diff
@@ -1,38 +1,38 @@
-import laspy
-from laspy import PointFormat
-
-
-def test_lost_dims():
-    assert set(laspy.point.format.lost_dimensions(3, 0)) == {
-        "red",
-        "green",
-        "blue",
-        "gps_time",
-    }
-    assert set(laspy.point.format.lost_dimensions(2, 0)) == {"red", "green", "blue"}
-    assert set(laspy.point.format.lost_dimensions(1, 0)) == {"gps_time"}
-
-    assert set(laspy.point.format.lost_dimensions(0, 0)) == set()
-    assert set(laspy.point.format.lost_dimensions(0, 1)) == set()
-    assert set(laspy.point.format.lost_dimensions(0, 2)) == set()
-    assert set(laspy.point.format.lost_dimensions(0, 3)) == set()
-
-
-def test_has_waveform():
-    for i in (4, 5, 9, 10):
-        assert PointFormat(
-            i
-        ).has_waveform_packet, "Point format {} should have waveform".format(i)
-
-    for i in (0, 1, 2, 3, 6, 7, 8):
-        assert not PointFormat(
-            i
-        ).has_waveform_packet, "Point format {} should not have waveform".format(i)
-
-
-def test_extra_bytes_struct_size():
-    assert laspy.vlrs.known.ExtraBytesStruct.size() == 192
-
-
-def test_waveform_packet_struct_size():
-    assert laspy.vlrs.known.WaveformPacketStruct.size() == 26
+import laspy
+from laspy import PointFormat
+
+
+def test_lost_dims():
+    assert set(laspy.point.format.lost_dimensions(3, 0)) == {
+        "red",
+        "green",
+        "blue",
+        "gps_time",
+    }
+    assert set(laspy.point.format.lost_dimensions(2, 0)) == {"red", "green", "blue"}
+    assert set(laspy.point.format.lost_dimensions(1, 0)) == {"gps_time"}
+
+    assert set(laspy.point.format.lost_dimensions(0, 0)) == set()
+    assert set(laspy.point.format.lost_dimensions(0, 1)) == set()
+    assert set(laspy.point.format.lost_dimensions(0, 2)) == set()
+    assert set(laspy.point.format.lost_dimensions(0, 3)) == set()
+
+
+def test_has_waveform():
+    for i in (4, 5, 9, 10):
+        assert PointFormat(
+            i
+        ).has_waveform_packet, "Point format {} should have waveform".format(i)
+
+    for i in (0, 1, 2, 3, 6, 7, 8):
+        assert not PointFormat(
+            i
+        ).has_waveform_packet, "Point format {} should not have waveform".format(i)
+
+
+def test_extra_bytes_struct_size():
+    assert laspy.vlrs.known.ExtraBytesStruct.size() == 192
+
+
+def test_waveform_packet_struct_size():
+    assert laspy.vlrs.known.WaveformPacketStruct.size() == 26
```

### Comparing `laspy-2.4.1/tests/test_conversion.py` & `laspy-2.5.0/tests/test_conversion.py`

 * *Ordering differences only*

 * *Files 8% similar despite different names*

```diff
@@ -1,24 +1,24 @@
-import numpy as np
-import pytest
-
-import laspy
-from laspy.lib import write_then_read_again
-
-
-@pytest.mark.parametrize("target_point_format_id", [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
-def test_point_format_conversion_copies_field_values(file_path, target_point_format_id):
-    original = laspy.read(file_path)
-    converted = laspy.convert(original, point_format_id=target_point_format_id)
-    converted = write_then_read_again(converted)
-
-    converted_dimension_names = set(converted.point_format.dimension_names)
-    dimension_expected_to_be_kept = [
-        dim_name
-        for dim_name in original.point_format.dimension_names
-        if dim_name in converted_dimension_names
-    ]
-
-    for dim_name in dimension_expected_to_be_kept:
-        assert np.allclose(
-            converted[dim_name], original[dim_name]
-        ), "{} not equal".format(dim_name)
+import numpy as np
+import pytest
+
+import laspy
+from laspy.lib import write_then_read_again
+
+
+@pytest.mark.parametrize("target_point_format_id", [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
+def test_point_format_conversion_copies_field_values(file_path, target_point_format_id):
+    original = laspy.read(file_path)
+    converted = laspy.convert(original, point_format_id=target_point_format_id)
+    converted = write_then_read_again(converted)
+
+    converted_dimension_names = set(converted.point_format.dimension_names)
+    dimension_expected_to_be_kept = [
+        dim_name
+        for dim_name in original.point_format.dimension_names
+        if dim_name in converted_dimension_names
+    ]
+
+    for dim_name in dimension_expected_to_be_kept:
+        assert np.allclose(
+            converted[dim_name], original[dim_name]
+        ), "{} not equal".format(dim_name)
```

### Comparing `laspy-2.4.1/tests/test_extrabytes.py` & `laspy-2.5.0/tests/test_extrabytes.py`

 * *Ordering differences only*

 * *Files 11% similar despite different names*

```diff
@@ -1,378 +1,378 @@
-"""
-Tests related to extra bytes
-"""
-
-import numpy as np
-import pytest
-
-import laspy
-from laspy.lib import write_then_read_again
-from tests.conftest import (
-    UNREGISTERED_EXTRA_BYTES_LAS,
-    EXTRA_BYTES_LAS_FILE_PATH,
-    SIMPLE_LAS_FILE_PATH,
-)
-
-
-def test_read_example_extra_bytes_las(las_file_path_with_extra_bytes):
-    """
-    Test that we can read the files with extra bytes with have as examples
-    """
-    las = laspy.read(las_file_path_with_extra_bytes)
-    expected_names = [
-        "Colors",
-        "Reserved",
-        "Flags",
-        "Intensity",
-        "Time",
-    ]
-    assert expected_names == list(las.point_format.extra_dimension_names)
-
-
-def test_read_write_example_extra_bytes_file(las_file_path_with_extra_bytes):
-    """
-    Test that we can write extra bytes without problem
-    """
-    original = laspy.read(las_file_path_with_extra_bytes)
-    las = write_then_read_again(original)
-
-    for name in original.point_format.dimension_names:
-        assert np.allclose(las[name], original[name])
-
-
-def test_adding_extra_bytes_keeps_values_of_all_existing_fields(
-    extra_bytes_params, simple_las_path
-):
-    """
-    Test that when extra bytes are added, the existing fields keep their
-    values and then we don't somehow drop them
-    """
-    las = laspy.read(simple_las_path)
-    las.add_extra_dim(extra_bytes_params)
-
-    original = laspy.read(simple_las_path)
-
-    for name in original.point_format.dimension_names:
-        assert np.allclose(las[name], original[name])
-
-
-def test_creating_extra_bytes(extra_bytes_params, simple_las_path):
-    """
-    Test that we can create extra byte dimensions for each
-    data type. And they can be written then read.
-    """
-    las = laspy.read(simple_las_path)
-    las.add_extra_dim(extra_bytes_params)
-
-    assert np.allclose(las[extra_bytes_params.name], 0)
-
-    las[extra_bytes_params.name][:] = 42
-    assert np.allclose(las[extra_bytes_params.name], 42)
-
-    las = write_then_read_again(las)
-    assert np.allclose(las[extra_bytes_params.name], 42)
-
-
-def test_creating_scaled_extra_bytes(extra_bytes_params, simple_las_path):
-    las = laspy.read(simple_las_path)
-
-    if extra_bytes_params.type.ndim == 1:
-        num_elements = extra_bytes_params.type.shape[0]
-    else:
-        num_elements = 1
-
-    params = laspy.ExtraBytesParams(
-        extra_bytes_params.name,
-        extra_bytes_params.type,
-        offsets=np.array([2.0] * num_elements),
-        scales=np.array([1.0] * num_elements),
-    )
-    las.add_extra_dim(params)
-
-    assert np.allclose(las[extra_bytes_params.name], 2.0)
-
-    las[params.name][:] = 42.0
-    assert np.allclose(las[extra_bytes_params.name], 42.0)
-
-    las = write_then_read_again(las)
-    assert np.allclose(las[extra_bytes_params.name], 42.0)
-
-
-def test_scaled_extra_byte_array_type(simple_las_path):
-    """
-    To make sure we handle scaled extra bytes
-    """
-    las = laspy.read(simple_las_path)
-
-    las.add_extra_dim(
-        laspy.ExtraBytesParams(
-            name="test_dim",
-            type="3int32",
-            scales=np.array([1.0, 2.0, 3.0], np.float64),
-            offsets=np.array([10.0, 20.0, 30.0], np.float64),
-        )
-    )
-
-    assert np.allclose(las.test_dim[..., 0], 10.0)
-    assert np.allclose(las.test_dim[..., 1], 20.0)
-    assert np.allclose(las.test_dim[..., 2], 30.0)
-
-    las.test_dim[..., 0][:] = 42.0
-    las.test_dim[..., 1][:] = 82.0
-    las.test_dim[..., 2][:] = 123.0
-
-    assert np.allclose(las.test_dim[..., 0], 42.0)
-    assert np.allclose(las.test_dim[..., 1], 82.0)
-    assert np.allclose(las.test_dim[..., 2], 123.0)
-
-    las = write_then_read_again(las)
-    assert np.allclose(las.test_dim[..., 0], 42.0)
-    assert np.allclose(las.test_dim[..., 1], 82.0)
-    assert np.allclose(las.test_dim[..., 2], 123.0)
-
-
-def test_extra_bytes_description_is_ok(extra_bytes_params, simple_las_path):
-    """
-    Test that the description in ok
-    """
-    las = laspy.read(simple_las_path)
-    las.add_extra_dim(extra_bytes_params)
-
-    extra_dim_info = list(las.point_format.extra_dimensions)
-    assert len(extra_dim_info) == 1
-    assert extra_dim_info[0].description == extra_bytes_params.description
-
-    las = write_then_read_again(las)
-
-    extra_dim_info = list(las.point_format.extra_dimensions)
-    assert len(extra_dim_info) == 1
-    assert extra_dim_info[0].description == extra_bytes_params.description
-
-
-def test_extra_bytes_with_spaces_in_name(simple_las_path):
-    """
-    Test that we can create extra bytes with spaces in their name
-    and that they can be accessed using __getitem__ ( [] )
-    as de normal '.name' won't work
-    """
-    las = laspy.read(simple_las_path)
-    las.add_extra_dim(laspy.ExtraBytesParams(name="Name With Spaces", type="int32"))
-
-    assert np.alltrue(las["Name With Spaces"] == 0)
-    las["Name With Spaces"][:] = 789_464
-
-    las = write_then_read_again(las)
-    np.alltrue(las["Name With Spaces"] == 789_464)
-
-
-def test_conversion_keeps_eb(las_file_path_with_extra_bytes):
-    """
-    Test that converting point format does not lose extra bytes
-    """
-    original = laspy.read(las_file_path_with_extra_bytes)
-    converted_las = laspy.convert(original, point_format_id=0)
-
-    assert len(list(original.point_format.extra_dimension_names)) == 5
-    assert list(converted_las.point_format.extra_dimension_names) == list(
-        original.point_format.extra_dimension_names
-    )
-    for name in converted_las.point_format.extra_dimension_names:
-        assert np.allclose(converted_las[name], original[name])
-
-    converted_las = laspy.lib.write_then_read_again(converted_las)
-    assert list(converted_las.point_format.extra_dimension_names) == list(
-        original.point_format.extra_dimension_names
-    )
-    for name in converted_las.point_format.extra_dimension_names:
-        assert np.allclose(converted_las[name], original[name])
-
-
-def test_creating_bytes_with_name_too_long(simple_las_path):
-    """
-    Test error thrown when creating extra bytes with a name that is too long
-    """
-    las = laspy.read(simple_las_path)
-    with pytest.raises(ValueError) as error:
-        las.add_extra_dim(
-            laspy.ExtraBytesParams(
-                name="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non risus",
-                type="int32",
-            )
-        )
-
-    assert str(error.value) == "bytes too long (70, maximum length 32)"
-
-
-def test_creating_bytes_with_description_too_long(simple_las_path):
-    """
-    Test error thrown when creating extra bytes with a name that is too long
-    """
-    las = laspy.read(simple_las_path)
-    with pytest.raises(ValueError) as error:
-        las.add_extra_dim(
-            laspy.ExtraBytesParams(
-                name="a fine name",
-                type="int32",
-                description="Lorem ipsum dolor sit amet, consectetur adipiscing elit."
-                " Sed non risus",
-            )
-        )
-
-    assert str(error.value) == "bytes too long (70, maximum length 32)"
-
-
-def test_creating_extra_byte_with_invalid_type(simple_las_path):
-    """
-    Test the error message when creating extra bytes with invalid type
-    """
-    las = laspy.read(simple_las_path)
-    with pytest.raises(TypeError):
-        las.add_extra_dim(laspy.ExtraBytesParams("just_a_test", "i16"))
-
-
-def test_cant_create_scaled_extra_bytes_without_both_offsets_and_scales():
-    las = laspy.create()
-    with pytest.raises(ValueError):
-        las.add_extra_dim(
-            laspy.ExtraBytesParams("must fail", "int64", scales=np.array([0.1]))
-        )
-
-    with pytest.raises(ValueError):
-        las.add_extra_dim(
-            laspy.ExtraBytesParams("must fail", "int64", offsets=np.array([0.1]))
-        )
-
-
-@pytest.mark.parametrize("num_elements", [1, 2, 3])
-def test_cant_create_scaled_extra_bytes_with_offsets_array_smaller(num_elements):
-    las = laspy.create()
-    with pytest.raises(ValueError) as error:
-        las.add_extra_dim(
-            laspy.ExtraBytesParams(
-                "must fail",
-                f"{num_elements}int64",
-                scales=np.array([0.1] * num_elements),
-                offsets=np.array([0.0] * (num_elements - 1)),
-            )
-        )
-    assert (
-        str(error.value)
-        == f"len(offsets) ({num_elements - 1}) is not the same as the number of elements ({num_elements})"
-    )
-
-
-@pytest.mark.parametrize("num_elements", [1, 2, 3])
-def test_cant_create_scaled_extra_bytes_with_scales_array_smaller(num_elements):
-    las = laspy.create()
-    with pytest.raises(ValueError) as error:
-        las.add_extra_dim(
-            laspy.ExtraBytesParams(
-                "must fail",
-                f"{num_elements}int64",
-                scales=np.array([0.1] * (num_elements - 1)),
-                offsets=np.array([0.0] * num_elements),
-            )
-        )
-    assert (
-        str(error.value)
-        == f"len(scales) ({num_elements - 1}) is not the same as the number of elements ({num_elements})"
-    )
-
-
-def test_handle_unregistered_extra_bytes():
-    # Test that if the point size in the header is bigger
-    # than the expected point size of the point format
-    # and no extra bytes vlr is present, we can still read and
-    # write the file
-
-    def check_file(las):
-        assert las.point_format.id == 6
-        assert las.point_format.size == 34
-        assert las.point_format.num_extra_bytes == 4
-        assert np.all(las.x == np.array([1, 2, 3, 4]))
-        assert np.all(las.y == np.array([1, 2, 3, 4]))
-        assert np.all(las.z == np.array([1, 2, 3, 4]))
-        assert list(las.point_format.extra_dimension_names) == ["ExtraBytes"]
-        assert las.vlrs == []
-
-    las = laspy.read(UNREGISTERED_EXTRA_BYTES_LAS)
-    check_file(las)
-
-    las = laspy.lib.write_then_read_again(las)
-    check_file(las)
-
-
-def test_remove_standard_dimension_fails():
-    """
-    Test we cannot remove non-extra dimension
-    """
-    las = laspy.read(SIMPLE_LAS_FILE_PATH)
-    for name in las.point_format.standard_dimension_names:
-        with pytest.raises(laspy.LaspyException):
-            las.remove_extra_dims(name)
-
-
-def test_remove_all_extra_dimensions():
-    """
-    Test that if we remove all extra bytes of a file,
-    the values of standard fields are not altered
-
-    This also test that writing files from which we deleted extra bytes works
-    """
-    las = laspy.read(EXTRA_BYTES_LAS_FILE_PATH)
-
-    extra_dimension_names = list(las.point_format.extra_dimension_names)
-    assert len(extra_dimension_names) > 0, (
-        "If the input file has no extra dimension, " "this test is useless"
-    )
-
-    copied_standard_values = [
-        (name, np.copy(las[name])) for name in las.point_format.standard_dimension_names
-    ]
-
-    las.remove_extra_dims(extra_dimension_names)
-
-    for name, copied_value in copied_standard_values:
-        assert np.all(las[name] == copied_value)
-
-    new_las = laspy.lib.write_then_read_again(las)
-    assert new_las.point_format == las.point_format
-    for name, copied_value in copied_standard_values:
-        assert np.all(new_las[name] == copied_value)
-
-
-def test_remove_some_extra_dimensions():
-    """
-    Test that if we remove some extra bytes of a file,
-    the values of standard fields as well as kept extra bytes are not altered
-
-    This also test that writing files from which we deleted extra bytes works
-    """
-    las = laspy.read(EXTRA_BYTES_LAS_FILE_PATH)
-
-    extra_dimension_names = list(las.point_format.extra_dimension_names)
-    assert len(extra_dimension_names) > 0, (
-        "If the input file has no extra dimension, " "this test is useless"
-    )
-
-    extra_dimensions_to_keep = ["Colors", "Time"]
-    dims_to_copy = (
-        list(las.point_format.standard_dimension_names) + extra_dimensions_to_keep
-    )
-    copied_standard_values = [(name, np.copy(las[name])) for name in dims_to_copy]
-
-    extra_dims_to_remove = [
-        name
-        for name in las.point_format.extra_dimension_names
-        if name not in extra_dimensions_to_keep
-    ]
-
-    las.remove_extra_dims(extra_dims_to_remove)
-
-    for name, copied_value in copied_standard_values:
-        assert np.all(las[name] == copied_value)
-
-    new_las = laspy.lib.write_then_read_again(las)
-    assert new_las.point_format == las.point_format
-    for name, copied_value in copied_standard_values:
-        assert np.all(new_las[name] == copied_value)
+"""
+Tests related to extra bytes
+"""
+
+import numpy as np
+import pytest
+
+import laspy
+from laspy.lib import write_then_read_again
+from tests.conftest import (
+    EXTRA_BYTES_LAS_FILE_PATH,
+    SIMPLE_LAS_FILE_PATH,
+    UNREGISTERED_EXTRA_BYTES_LAS,
+)
+
+
+def test_read_example_extra_bytes_las(las_file_path_with_extra_bytes):
+    """
+    Test that we can read the files with extra bytes with have as examples
+    """
+    las = laspy.read(las_file_path_with_extra_bytes)
+    expected_names = [
+        "Colors",
+        "Reserved",
+        "Flags",
+        "Intensity",
+        "Time",
+    ]
+    assert expected_names == list(las.point_format.extra_dimension_names)
+
+
+def test_read_write_example_extra_bytes_file(las_file_path_with_extra_bytes):
+    """
+    Test that we can write extra bytes without problem
+    """
+    original = laspy.read(las_file_path_with_extra_bytes)
+    las = write_then_read_again(original)
+
+    for name in original.point_format.dimension_names:
+        assert np.allclose(las[name], original[name])
+
+
+def test_adding_extra_bytes_keeps_values_of_all_existing_fields(
+    extra_bytes_params, simple_las_path
+):
+    """
+    Test that when extra bytes are added, the existing fields keep their
+    values and then we don't somehow drop them
+    """
+    las = laspy.read(simple_las_path)
+    las.add_extra_dim(extra_bytes_params)
+
+    original = laspy.read(simple_las_path)
+
+    for name in original.point_format.dimension_names:
+        assert np.allclose(las[name], original[name])
+
+
+def test_creating_extra_bytes(extra_bytes_params, simple_las_path):
+    """
+    Test that we can create extra byte dimensions for each
+    data type. And they can be written then read.
+    """
+    las = laspy.read(simple_las_path)
+    las.add_extra_dim(extra_bytes_params)
+
+    assert np.allclose(las[extra_bytes_params.name], 0)
+
+    las[extra_bytes_params.name][:] = 42
+    assert np.allclose(las[extra_bytes_params.name], 42)
+
+    las = write_then_read_again(las)
+    assert np.allclose(las[extra_bytes_params.name], 42)
+
+
+def test_creating_scaled_extra_bytes(extra_bytes_params, simple_las_path):
+    las = laspy.read(simple_las_path)
+
+    if extra_bytes_params.type.ndim == 1:
+        num_elements = extra_bytes_params.type.shape[0]
+    else:
+        num_elements = 1
+
+    params = laspy.ExtraBytesParams(
+        extra_bytes_params.name,
+        extra_bytes_params.type,
+        offsets=np.array([2.0] * num_elements),
+        scales=np.array([1.0] * num_elements),
+    )
+    las.add_extra_dim(params)
+
+    assert np.allclose(las[extra_bytes_params.name], 2.0)
+
+    las[params.name][:] = 42.0
+    assert np.allclose(las[extra_bytes_params.name], 42.0)
+
+    las = write_then_read_again(las)
+    assert np.allclose(las[extra_bytes_params.name], 42.0)
+
+
+def test_scaled_extra_byte_array_type(simple_las_path):
+    """
+    To make sure we handle scaled extra bytes
+    """
+    las = laspy.read(simple_las_path)
+
+    las.add_extra_dim(
+        laspy.ExtraBytesParams(
+            name="test_dim",
+            type="3int32",
+            scales=np.array([1.0, 2.0, 3.0], np.float64),
+            offsets=np.array([10.0, 20.0, 30.0], np.float64),
+        )
+    )
+
+    assert np.allclose(las.test_dim[..., 0], 10.0)
+    assert np.allclose(las.test_dim[..., 1], 20.0)
+    assert np.allclose(las.test_dim[..., 2], 30.0)
+
+    las.test_dim[..., 0][:] = 42.0
+    las.test_dim[..., 1][:] = 82.0
+    las.test_dim[..., 2][:] = 123.0
+
+    assert np.allclose(las.test_dim[..., 0], 42.0)
+    assert np.allclose(las.test_dim[..., 1], 82.0)
+    assert np.allclose(las.test_dim[..., 2], 123.0)
+
+    las = write_then_read_again(las)
+    assert np.allclose(las.test_dim[..., 0], 42.0)
+    assert np.allclose(las.test_dim[..., 1], 82.0)
+    assert np.allclose(las.test_dim[..., 2], 123.0)
+
+
+def test_extra_bytes_description_is_ok(extra_bytes_params, simple_las_path):
+    """
+    Test that the description in ok
+    """
+    las = laspy.read(simple_las_path)
+    las.add_extra_dim(extra_bytes_params)
+
+    extra_dim_info = list(las.point_format.extra_dimensions)
+    assert len(extra_dim_info) == 1
+    assert extra_dim_info[0].description == extra_bytes_params.description
+
+    las = write_then_read_again(las)
+
+    extra_dim_info = list(las.point_format.extra_dimensions)
+    assert len(extra_dim_info) == 1
+    assert extra_dim_info[0].description == extra_bytes_params.description
+
+
+def test_extra_bytes_with_spaces_in_name(simple_las_path):
+    """
+    Test that we can create extra bytes with spaces in their name
+    and that they can be accessed using __getitem__ ( [] )
+    as de normal '.name' won't work
+    """
+    las = laspy.read(simple_las_path)
+    las.add_extra_dim(laspy.ExtraBytesParams(name="Name With Spaces", type="int32"))
+
+    assert np.alltrue(las["Name With Spaces"] == 0)
+    las["Name With Spaces"][:] = 789_464
+
+    las = write_then_read_again(las)
+    np.alltrue(las["Name With Spaces"] == 789_464)
+
+
+def test_conversion_keeps_eb(las_file_path_with_extra_bytes):
+    """
+    Test that converting point format does not lose extra bytes
+    """
+    original = laspy.read(las_file_path_with_extra_bytes)
+    converted_las = laspy.convert(original, point_format_id=0)
+
+    assert len(list(original.point_format.extra_dimension_names)) == 5
+    assert list(converted_las.point_format.extra_dimension_names) == list(
+        original.point_format.extra_dimension_names
+    )
+    for name in converted_las.point_format.extra_dimension_names:
+        assert np.allclose(converted_las[name], original[name])
+
+    converted_las = laspy.lib.write_then_read_again(converted_las)
+    assert list(converted_las.point_format.extra_dimension_names) == list(
+        original.point_format.extra_dimension_names
+    )
+    for name in converted_las.point_format.extra_dimension_names:
+        assert np.allclose(converted_las[name], original[name])
+
+
+def test_creating_bytes_with_name_too_long(simple_las_path):
+    """
+    Test error thrown when creating extra bytes with a name that is too long
+    """
+    las = laspy.read(simple_las_path)
+    with pytest.raises(ValueError) as error:
+        las.add_extra_dim(
+            laspy.ExtraBytesParams(
+                name="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non risus",
+                type="int32",
+            )
+        )
+
+    assert str(error.value) == "bytes too long (70, maximum length 32)"
+
+
+def test_creating_bytes_with_description_too_long(simple_las_path):
+    """
+    Test error thrown when creating extra bytes with a name that is too long
+    """
+    las = laspy.read(simple_las_path)
+    with pytest.raises(ValueError) as error:
+        las.add_extra_dim(
+            laspy.ExtraBytesParams(
+                name="a fine name",
+                type="int32",
+                description="Lorem ipsum dolor sit amet, consectetur adipiscing elit."
+                " Sed non risus",
+            )
+        )
+
+    assert str(error.value) == "bytes too long (70, maximum length 32)"
+
+
+def test_creating_extra_byte_with_invalid_type(simple_las_path):
+    """
+    Test the error message when creating extra bytes with invalid type
+    """
+    las = laspy.read(simple_las_path)
+    with pytest.raises(TypeError):
+        las.add_extra_dim(laspy.ExtraBytesParams("just_a_test", "i16"))
+
+
+def test_cant_create_scaled_extra_bytes_without_both_offsets_and_scales():
+    las = laspy.create()
+    with pytest.raises(ValueError):
+        las.add_extra_dim(
+            laspy.ExtraBytesParams("must fail", "int64", scales=np.array([0.1]))
+        )
+
+    with pytest.raises(ValueError):
+        las.add_extra_dim(
+            laspy.ExtraBytesParams("must fail", "int64", offsets=np.array([0.1]))
+        )
+
+
+@pytest.mark.parametrize("num_elements", [1, 2, 3])
+def test_cant_create_scaled_extra_bytes_with_offsets_array_smaller(num_elements):
+    las = laspy.create()
+    with pytest.raises(ValueError) as error:
+        las.add_extra_dim(
+            laspy.ExtraBytesParams(
+                "must fail",
+                f"{num_elements}int64",
+                scales=np.array([0.1] * num_elements),
+                offsets=np.array([0.0] * (num_elements - 1)),
+            )
+        )
+    assert (
+        str(error.value)
+        == f"len(offsets) ({num_elements - 1}) is not the same as the number of elements ({num_elements})"
+    )
+
+
+@pytest.mark.parametrize("num_elements", [1, 2, 3])
+def test_cant_create_scaled_extra_bytes_with_scales_array_smaller(num_elements):
+    las = laspy.create()
+    with pytest.raises(ValueError) as error:
+        las.add_extra_dim(
+            laspy.ExtraBytesParams(
+                "must fail",
+                f"{num_elements}int64",
+                scales=np.array([0.1] * (num_elements - 1)),
+                offsets=np.array([0.0] * num_elements),
+            )
+        )
+    assert (
+        str(error.value)
+        == f"len(scales) ({num_elements - 1}) is not the same as the number of elements ({num_elements})"
+    )
+
+
+def test_handle_unregistered_extra_bytes():
+    # Test that if the point size in the header is bigger
+    # than the expected point size of the point format
+    # and no extra bytes vlr is present, we can still read and
+    # write the file
+
+    def check_file(las):
+        assert las.point_format.id == 6
+        assert las.point_format.size == 34
+        assert las.point_format.num_extra_bytes == 4
+        assert np.all(las.x == np.array([1, 2, 3, 4]))
+        assert np.all(las.y == np.array([1, 2, 3, 4]))
+        assert np.all(las.z == np.array([1, 2, 3, 4]))
+        assert list(las.point_format.extra_dimension_names) == ["ExtraBytes"]
+        assert las.vlrs == []
+
+    las = laspy.read(UNREGISTERED_EXTRA_BYTES_LAS)
+    check_file(las)
+
+    las = laspy.lib.write_then_read_again(las)
+    check_file(las)
+
+
+def test_remove_standard_dimension_fails():
+    """
+    Test we cannot remove non-extra dimension
+    """
+    las = laspy.read(SIMPLE_LAS_FILE_PATH)
+    for name in las.point_format.standard_dimension_names:
+        with pytest.raises(laspy.LaspyException):
+            las.remove_extra_dims(name)
+
+
+def test_remove_all_extra_dimensions():
+    """
+    Test that if we remove all extra bytes of a file,
+    the values of standard fields are not altered
+
+    This also test that writing files from which we deleted extra bytes works
+    """
+    las = laspy.read(EXTRA_BYTES_LAS_FILE_PATH)
+
+    extra_dimension_names = list(las.point_format.extra_dimension_names)
+    assert len(extra_dimension_names) > 0, (
+        "If the input file has no extra dimension, " "this test is useless"
+    )
+
+    copied_standard_values = [
+        (name, np.copy(las[name])) for name in las.point_format.standard_dimension_names
+    ]
+
+    las.remove_extra_dims(extra_dimension_names)
+
+    for name, copied_value in copied_standard_values:
+        assert np.all(las[name] == copied_value)
+
+    new_las = laspy.lib.write_then_read_again(las)
+    assert new_las.point_format == las.point_format
+    for name, copied_value in copied_standard_values:
+        assert np.all(new_las[name] == copied_value)
+
+
+def test_remove_some_extra_dimensions():
+    """
+    Test that if we remove some extra bytes of a file,
+    the values of standard fields as well as kept extra bytes are not altered
+
+    This also test that writing files from which we deleted extra bytes works
+    """
+    las = laspy.read(EXTRA_BYTES_LAS_FILE_PATH)
+
+    extra_dimension_names = list(las.point_format.extra_dimension_names)
+    assert len(extra_dimension_names) > 0, (
+        "If the input file has no extra dimension, " "this test is useless"
+    )
+
+    extra_dimensions_to_keep = ["Colors", "Time"]
+    dims_to_copy = (
+        list(las.point_format.standard_dimension_names) + extra_dimensions_to_keep
+    )
+    copied_standard_values = [(name, np.copy(las[name])) for name in dims_to_copy]
+
+    extra_dims_to_remove = [
+        name
+        for name in las.point_format.extra_dimension_names
+        if name not in extra_dimensions_to_keep
+    ]
+
+    las.remove_extra_dims(extra_dims_to_remove)
+
+    for name, copied_value in copied_standard_values:
+        assert np.all(las[name] == copied_value)
+
+    new_las = laspy.lib.write_then_read_again(las)
+    assert new_las.point_format == las.point_format
+    for name, copied_value in copied_standard_values:
+        assert np.all(new_las[name] == copied_value)
```

### Comparing `laspy-2.4.1/tests/test_field_views.py` & `laspy-2.5.0/tests/test_field_views.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,202 +1,202 @@
-import numpy as np
-import pytest
-
-import laspy
-from laspy.point.dims import SubFieldView, ScaledArrayView
-
-
-def test_sub_field_view_behaves_like_array():
-    """This function is used to test if the SubFieldView class
-    works & has an API that is similar to np.ndarray
-    """
-    array = np.zeros(10, np.uint8)
-
-    field = SubFieldView(array, 0b0000_0010)
-
-    assert len(field) == 10
-    assert np.all(field == 0)
-    assert np.all(field[:] == 0)
-
-    assert field.max() == 0
-    assert np.max(field) == 0
-    assert field.min() == 0
-    assert np.min(field) == 0
-    assert np.min(field) == field.min()
-    assert np.max(field) == field.max()
-
-    field[:] = 1
-    assert np.all(field == 1)
-    assert np.all(field[:] == 1)
-
-    assert field.max() == 1
-    assert np.max(field) == 1
-    assert field.min() == 1
-    assert np.min(field) == 1
-
-    assert np.all(field > 0)
-    assert not np.all(field < 0)
-    assert np.all(field >= 1)
-    assert np.all(field <= 1)
-
-    # check that the real array is properly modified
-    assert np.all(array == 2)
-
-    with pytest.raises(OverflowError):
-        field[4] = 2
-
-    assert np.mean(field) == 1
-
-
-def test_array_view_int_index_return_singular_elements():
-    a = np.array([1, 2, 3, 4], np.int32)
-    s = SubFieldView(a, 0x00_00_00_FF)
-
-    for i in range(len(s)):
-        assert type(s[i]) in (np.int32, np.int64)
-        assert a[i] == s[i]
-
-    s = ScaledArrayView(a, scale=2.0, offset=0.0)
-    for i in range(len(s)):
-        assert type(s[i]) == np.float64
-        assert (a[i] * 2.0) == s[i]
-
-
-def test_scaled_array_view_ellipsis_indexing(simple_las_path):
-    las = laspy.read(simple_las_path)
-
-    las.add_extra_dim(
-        laspy.ExtraBytesParams(
-            name="test_dim",
-            type="3int32",
-            scales=np.array([1.0, 2.0, 3.0], np.float64),
-            offsets=np.array([10.0, 20.0, 30.0], np.float64),
-        )
-    )
-
-    # Query all the points in the 2nd dimension
-    assert np.all(las.test_dim[..., 2] == 30.0)
-
-    # Query the 10 nth point, we expect all its dimensions
-    assert np.all(las.test_dim[10, ...] == [10.0, 20.0, 30.0])
-
-
-def test_scaled_array_view_indexing_with_array_or_list(simple_las_path):
-    las = laspy.read(simple_las_path)
-
-    las.add_extra_dim(
-        laspy.ExtraBytesParams(
-            name="test_dim",
-            type="3int32",
-            scales=np.array([1.0, 2.0, 3.0], np.float64),
-            offsets=np.array([10.0, 20.0, 30.0], np.float64),
-        )
-    )
-
-    d = las.test_dim[[0, 1, 10, 12]]
-    assert d.ndim == 2
-    assert d.shape == (4, 3)
-    assert np.all(d[..., 0] == 10.0)
-    assert np.all(d[..., 1] == 20.0)
-    assert np.all(d[..., 2] == 30.0)
-
-    d2 = las.test_dim[np.array([0, 1, 10, 12])]
-    assert np.all(d == d2)
-
-
-def test_sub_field_view_with_self(simple_las_path):
-    las = laspy.read(simple_las_path)
-
-    rn = np.array(las.return_number)
-    order = np.argsort(las.return_number)[::-1]
-
-    las.return_number[:] = las.return_number[order]
-
-    assert np.all(las.return_number == rn[order])
-
-
-def test_can_use_array_func_with_list(simple_las_path):
-    las = laspy.read(simple_las_path)
-
-    np.concatenate([las.return_number, las.classification])
-    np.concatenate([las.x, las.y])
-
-
-def test_sub_field_as_array():
-    array = np.zeros(10, np.uint8)
-    field = SubFieldView(array, 0b0000_0010)
-
-    cpy = np.array(field)
-
-    cpy[:] = 1
-    assert np.all(cpy == 1)
-    assert np.all(field != 1)
-
-    cpy[:] = 17
-
-    with pytest.raises(OverflowError):
-        field[:] = cpy[:]
-
-    # Here we just test that this can run,
-    # We had an error about with our __array__ signature
-    cpy[:] = field[:]
-    assert np.all(cpy == field)
-
-
-def test_scaled_array_view():
-    array = np.zeros(10, np.int32)
-    x = ScaledArrayView(array, 0.01, 10)
-
-    assert np.max(x) == 10.0
-    assert np.min(x) == 10.0
-    assert np.min(x) == x.min()
-    assert np.max(x) == x.max()
-
-    assert np.all(x > 0.0)
-    assert np.all(x < 18.0)
-    assert np.all(x == 10.0)
-    assert np.all(x != 17.0)
-
-    assert np.mean(x) == 10.0
-
-    x[:] = 155.0
-    x[9] = 42.0
-    assert np.all(x[2:5] == 155.0)
-    assert x[9] == 42.0
-
-    with pytest.raises(OverflowError):
-        x[8] = np.finfo(np.float64).max
-
-
-def test_array_views_on_empty_things():
-    """
-    Test that __setitem__ of the Array views do not fail
-    when the value is an empty array / sequence,
-    to match the behaviour of numpy array
-    """
-    array = np.zeros(0, np.int32)
-    x = ScaledArrayView(array, 0.01, 10)
-    # This shall not fail
-    x[:] = np.zeros(0)
-
-    array = np.zeros(0, np.uint8)
-    field = SubFieldView(array, 0b0000_0010)
-    # This shall not fail
-    field[:] = np.zeros(0)
-
-
-def test_scaled_point_record_set_x_y_z():
-    record = laspy.ScaleAwarePointRecord.zeros(
-        5, point_format=laspy.PointFormat(3), scales=[1.0] * 3, offsets=[0.0] * 3
-    )
-
-    assert np.all(record.x == 0.0)
-    assert np.all(record.y == 0.0)
-    assert np.all(record.z == 0.0)
-
-    record.x = 17.0
-    record.y = 17.12
-    record.z = np.array([293090.812739] * len(record))
-
-    assert np.all(record.x == 17.0)
-    assert np.all(record.y == 17.12)
-    assert np.all(record.z == 293090.812739)
+import numpy as np
+import pytest
+
+import laspy
+from laspy.point.dims import ScaledArrayView, SubFieldView
+
+
+def test_sub_field_view_behaves_like_array():
+    """This function is used to test if the SubFieldView class
+    works & has an API that is similar to np.ndarray
+    """
+    array = np.zeros(10, np.uint8)
+
+    field = SubFieldView(array, 0b0000_0010)
+
+    assert len(field) == 10
+    assert np.all(field == 0)
+    assert np.all(field[:] == 0)
+
+    assert field.max() == 0
+    assert np.max(field) == 0
+    assert field.min() == 0
+    assert np.min(field) == 0
+    assert np.min(field) == field.min()
+    assert np.max(field) == field.max()
+
+    field[:] = 1
+    assert np.all(field == 1)
+    assert np.all(field[:] == 1)
+
+    assert field.max() == 1
+    assert np.max(field) == 1
+    assert field.min() == 1
+    assert np.min(field) == 1
+
+    assert np.all(field > 0)
+    assert not np.all(field < 0)
+    assert np.all(field >= 1)
+    assert np.all(field <= 1)
+
+    # check that the real array is properly modified
+    assert np.all(array == 2)
+
+    with pytest.raises(OverflowError):
+        field[4] = 2
+
+    assert np.mean(field) == 1
+
+
+def test_array_view_int_index_return_singular_elements():
+    a = np.array([1, 2, 3, 4], np.int32)
+    s = SubFieldView(a, 0x00_00_00_FF)
+
+    for i in range(len(s)):
+        assert type(s[i]) in (np.int32, np.int64)
+        assert a[i] == s[i]
+
+    s = ScaledArrayView(a, scale=2.0, offset=0.0)
+    for i in range(len(s)):
+        assert type(s[i]) == np.float64
+        assert (a[i] * 2.0) == s[i]
+
+
+def test_scaled_array_view_ellipsis_indexing(simple_las_path):
+    las = laspy.read(simple_las_path)
+
+    las.add_extra_dim(
+        laspy.ExtraBytesParams(
+            name="test_dim",
+            type="3int32",
+            scales=np.array([1.0, 2.0, 3.0], np.float64),
+            offsets=np.array([10.0, 20.0, 30.0], np.float64),
+        )
+    )
+
+    # Query all the points in the 2nd dimension
+    assert np.all(las.test_dim[..., 2] == 30.0)
+
+    # Query the 10 nth point, we expect all its dimensions
+    assert np.all(las.test_dim[10, ...] == [10.0, 20.0, 30.0])
+
+
+def test_scaled_array_view_indexing_with_array_or_list(simple_las_path):
+    las = laspy.read(simple_las_path)
+
+    las.add_extra_dim(
+        laspy.ExtraBytesParams(
+            name="test_dim",
+            type="3int32",
+            scales=np.array([1.0, 2.0, 3.0], np.float64),
+            offsets=np.array([10.0, 20.0, 30.0], np.float64),
+        )
+    )
+
+    d = las.test_dim[[0, 1, 10, 12]]
+    assert d.ndim == 2
+    assert d.shape == (4, 3)
+    assert np.all(d[..., 0] == 10.0)
+    assert np.all(d[..., 1] == 20.0)
+    assert np.all(d[..., 2] == 30.0)
+
+    d2 = las.test_dim[np.array([0, 1, 10, 12])]
+    assert np.all(d == d2)
+
+
+def test_sub_field_view_with_self(simple_las_path):
+    las = laspy.read(simple_las_path)
+
+    rn = np.array(las.return_number)
+    order = np.argsort(las.return_number)[::-1]
+
+    las.return_number[:] = las.return_number[order]
+
+    assert np.all(las.return_number == rn[order])
+
+
+def test_can_use_array_func_with_list(simple_las_path):
+    las = laspy.read(simple_las_path)
+
+    np.concatenate([las.return_number, las.classification])
+    np.concatenate([las.x, las.y])
+
+
+def test_sub_field_as_array():
+    array = np.zeros(10, np.uint8)
+    field = SubFieldView(array, 0b0000_0010)
+
+    cpy = np.array(field)
+
+    cpy[:] = 1
+    assert np.all(cpy == 1)
+    assert np.all(field != 1)
+
+    cpy[:] = 17
+
+    with pytest.raises(OverflowError):
+        field[:] = cpy[:]
+
+    # Here we just test that this can run,
+    # We had an error about with our __array__ signature
+    cpy[:] = field[:]
+    assert np.all(cpy == field)
+
+
+def test_scaled_array_view():
+    array = np.zeros(10, np.int32)
+    x = ScaledArrayView(array, 0.01, 10)
+
+    assert np.max(x) == 10.0
+    assert np.min(x) == 10.0
+    assert np.min(x) == x.min()
+    assert np.max(x) == x.max()
+
+    assert np.all(x > 0.0)
+    assert np.all(x < 18.0)
+    assert np.all(x == 10.0)
+    assert np.all(x != 17.0)
+
+    assert np.mean(x) == 10.0
+
+    x[:] = 155.0
+    x[9] = 42.0
+    assert np.all(x[2:5] == 155.0)
+    assert x[9] == 42.0
+
+    with pytest.raises(OverflowError):
+        x[8] = np.finfo(np.float64).max
+
+
+def test_array_views_on_empty_things():
+    """
+    Test that __setitem__ of the Array views do not fail
+    when the value is an empty array / sequence,
+    to match the behaviour of numpy array
+    """
+    array = np.zeros(0, np.int32)
+    x = ScaledArrayView(array, 0.01, 10)
+    # This shall not fail
+    x[:] = np.zeros(0)
+
+    array = np.zeros(0, np.uint8)
+    field = SubFieldView(array, 0b0000_0010)
+    # This shall not fail
+    field[:] = np.zeros(0)
+
+
+def test_scaled_point_record_set_x_y_z():
+    record = laspy.ScaleAwarePointRecord.zeros(
+        5, point_format=laspy.PointFormat(3), scales=[1.0] * 3, offsets=[0.0] * 3
+    )
+
+    assert np.all(record.x == 0.0)
+    assert np.all(record.y == 0.0)
+    assert np.all(record.z == 0.0)
+
+    record.x = 17.0
+    record.y = 17.12
+    record.z = np.array([293090.812739] * len(record))
+
+    assert np.all(record.x == 17.0)
+    assert np.all(record.y == 17.12)
+    assert np.all(record.z == 293090.812739)
```

### Comparing `laspy-2.4.1/tests/test_header.py` & `laspy-2.5.0/tests/test_header.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,297 +1,350 @@
-import io
-from datetime import date
-
-import pytest
-import numpy as np
-
-import laspy
-from laspy import LasHeader
-from laspy.lib import write_then_read_again
-from tests import test_common
-
-all_las_but_1_4 = test_common.all_las_but_1_4
-
-
-def test_number_of_points_return_is_updated(all_las_but_1_4):
-    las = all_las_but_1_4
-
-    nb_points = len(las.points)
-    nb_slice = 3
-
-    r = las.return_number
-
-    for i in reversed(range(nb_slice)):
-        r[i * (nb_points // nb_slice) : (i + 1) * (nb_points // nb_slice)] = i + 1
-
-    las = test_common.write_then_read_again(las)
-
-    assert (
-        tuple(las.header.number_of_points_by_return[:nb_slice])
-        == (nb_points // nb_slice,) * nb_slice
-    )
-    assert tuple(las.header.number_of_points_by_return[nb_slice:]) == (0,) * (
-        len(las.header.number_of_points_by_return) - nb_slice
-    )
-
-
-def test_nb_points_return_1_4():
-    las = laspy.read(test_common.test1_4_las)
-
-    r = las.return_number
-
-    for i in range(15):
-        r[i] = i + 1
-
-    r[15:] = 15
-
-    las = test_common.write_then_read_again(las)
-
-    assert tuple(las.header.number_of_points_by_return) == ((1,) * 14) + (
-        len(las.points) - 14,
-    )
-
-
-def test_header_copy():
-    import copy
-
-    las = laspy.read(test_common.simple_las)
-    header_copy = copy.copy(las.header)
-
-    assert header_copy.point_format.id == las.header.point_format.id
-    assert header_copy.version == las.header.version
-
-    header_copy.point_format_id = 0
-    assert header_copy.point_format_id != las.header.point_format.id
-    assert header_copy.version == las.header.version
-
-
-def test_set_uuid():
-    import uuid
-
-    las = laspy.read(test_common.simple_las)
-    u = uuid.uuid4()
-    las.header.uuid = u
-    las = test_common.write_then_read_again(las)
-    assert las.header.uuid == u
-
-
-def test_set_offsets():
-    header = laspy.header.LasHeader()
-    header.offsets = [0.5, 0.6, 0.7]
-
-    assert 0.5 == header.x_offset
-    assert 0.6 == header.y_offset
-    assert 0.7 == header.z_offset
-    assert [0.5, 0.6, 0.7] == list(header.offsets)
-
-
-def test_set_scales():
-    header = laspy.header.LasHeader()
-    header.scales = [0.001, 0.001, 0.01]
-
-    assert 0.001 == header.x_scale
-    assert 0.001 == header.y_scale
-    assert 0.01 == header.z_scale
-    assert [0.001, 0.001, 0.01] == list(header.scales)
-
-
-def test_set_maxs():
-    header = laspy.header.LasHeader()
-    values = [42.0, 1337.42, 553.3]
-    header.maxs = values
-
-    assert values[0] == header.x_max
-    assert values[1] == header.y_max
-    assert values[2] == header.z_max
-    assert values == list(header.maxs)
-
-
-def test_set_mins():
-    header = laspy.header.LasHeader()
-    values = [42.0, 1337.42, 553.3]
-    header.mins = values
-
-    assert values[0] == header.x_min
-    assert values[1] == header.y_min
-    assert values[2] == header.z_min
-    assert values == list(header.mins)
-
-
-def test_point_count_stays_synchronized():
-    las = laspy.read(test_common.simple_las)
-    assert las.header.point_count == len(las.points)
-
-    las.points = las.points[:120]
-    assert 120 == las.header.point_count
-    assert las.header.point_count == len(las.points)
-
-
-def test_header_date():
-    las = laspy.read(test_common.extra_bytes_las)
-    with io.BytesIO() as out:
-        las.header.write_to(out)
-        out.seek(0)
-        header_2 = LasHeader.read_from(out)
-
-    expected_date = date(year=2015, month=2, day=22)
-    assert las.header.creation_date == expected_date
-    assert las.header.creation_date == header_2.creation_date
-
-
-def test_set_vlrs_header():
-    """
-    Test that when setting the vlrs of a header,
-    if the given vlr list has an extra bytes vlr,
-    the header does not take it, as this header is specific
-    """
-    las = laspy.read(test_common.extra_bytes_las)
-
-    # test that it exists
-    _ = las.vlrs.index("ExtraBytesVlr")
-
-    hdr = laspy.LasHeader()
-    hdr.vlrs = las.vlrs
-    # Now it should not be in the hdr vlrs
-    with pytest.raises(ValueError):
-        _ = hdr.vlrs.index("ExtraBytesVlr")
-    # but still in the original list
-    _ = las.vlrs.index("ExtraBytesVlr")
-
-
-def test_extra_header_bytes():
-    las = laspy.read(test_common.simple_las)
-
-    extra_bytes = "Some extra bytes between header and VLRs".encode()
-    las.header.extra_header_bytes = extra_bytes
-    assert las.header.extra_header_bytes == extra_bytes
-
-    las = write_then_read_again(las)
-    assert las.header.extra_header_bytes == extra_bytes
-
-
-def test_extra_vlr_bytes():
-    las = laspy.read(test_common.simple_las)
-
-    extra_bytes = "Some extra bytes between VLRs and start of points".encode()
-    las.header.extra_vlr_bytes = extra_bytes
-    assert las.header.extra_vlr_bytes == extra_bytes
-
-    las = write_then_read_again(las)
-    assert las.header.extra_vlr_bytes == extra_bytes
-
-
-def test_header_update_after_slicing():
-    """Test that after slicing a LasData and after its header was
-    updated, its header's bound correctly reflect the new points.
-    """
-    las = laspy.read(test_common.simple_las)
-
-    def dim_min_max_from_header(header, dim_name):
-        if dim_name == "x":
-            return header.x_min, header.x_max
-
-        if dim_name == "y":
-            return header.y_min, header.y_max
-
-        if dim_name == "z":
-            return header.z_min, header.z_max
-
-        raise RuntimeError(f"Bad dim name {dim_name}")
-
-    for dim in ("x", "y", "z"):
-        values = las[dim]
-
-        old_min, old_max = dim_min_max_from_header(las.header, dim)
-        size = old_max - old_min
-        new_max = old_min + (size * 0.75)
-        new_min = old_min + (size * 0.25)
-
-        mask = (new_min < values) & (values < new_max)
-        las.points = las.points[mask]
-
-        values = las[dim]
-
-        new_header_min, new_header_max = dim_min_max_from_header(las.header, dim)
-        assert (
-            new_header_max == values.max()
-        ), "Header max value does not correspond to actual max value"
-        assert (
-            new_header_min == values.min()
-        ), "Header min value does not correspond to actual min value"
-        assert new_header_min > old_min
-        assert new_header_max < old_max
-
-
-def test_header_update_setting_points_on_new_las():
-    """Internally, when updating the header, its mins and maxs will temporarily be set
-    to f64::max_value and f64::min_value. This test is to make sure those value are
-    truly temporary. Even when setting the points to an empty record
-    """
-    las = laspy.read(test_common.simple_las)
-
-    new_las = laspy.create(
-        point_format=las.header.point_format, file_version=las.header.version
-    )
-    assert np.all(new_las.header.mins == [0.0, 0.0, 0.0])
-    assert np.all(new_las.header.maxs == [0.0, 0.0, 0.0])
-    assert np.sum(new_las.header.number_of_points_by_return) == 0
-
-    new_las.points = laspy.PackedPointRecord.empty(new_las.point_format)
-    assert np.all(new_las.header.mins == [0.0, 0.0, 0.0])
-    assert np.all(new_las.header.maxs == [0.0, 0.0, 0.0])
-    assert np.sum(new_las.header.number_of_points_by_return) == 0
-
-    new_las.points = las.points.copy()
-    assert np.all(new_las.header.mins == las.header.mins)
-    assert np.all(new_las.header.maxs == las.header.maxs)
-    assert np.all(
-        new_las.header.number_of_points_by_return
-        == las.header.number_of_points_by_return
-    )
-
-
-def test_header_min_max_chunk_mode():
-    """Test that when writing a file using 'chunk mode' the header`s bounds are correct"""
-    las = laspy.read(test_common.simple_las)
-    header = laspy.LasHeader(
-        point_format=las.header.point_format, version=las.header.version
-    )
-    with io.BytesIO() as stream:
-        with laspy.open(stream, mode="w", header=header, closefd=False) as writer:
-            # We intenionally write the file in two write_points call
-            writer.write_points(las.points[: len(las.points) // 2])
-            writer.write_points(las.points[len(las.points) // 2 :])
-
-        stream.seek(0)
-        new_las = laspy.read(stream)
-        assert np.all(new_las.header.maxs == las.header.maxs)
-        assert np.all(new_las.header.mins == las.header.mins)
-
-
-def test_update_header_empty_las_data():
-    """Test updating the header on and empyt las, and writing
-    an empyt las produces correct bounds values in header
-
-    """
-    las = laspy.create()
-    las.update_header()
-
-    assert np.all(las.header.mins == [0.0, 0.0, 0.0])
-    assert np.all(las.header.maxs == [0.0, 0.0, 0.0])
-    assert np.sum(las.header.number_of_points_by_return) == 0
-
-    las = write_then_read_again(las)
-    assert np.all(las.header.mins == [0.0, 0.0, 0.0])
-    assert np.all(las.header.maxs == [0.0, 0.0, 0.0])
-    assert np.sum(las.header.number_of_points_by_return) == 0
-
-    header = laspy.LasHeader()
-    with io.BytesIO() as stream:
-        with laspy.open(stream, mode="w", header=header, closefd=False) as writer:
-            # We intenionally don't write points
-            pass
-        stream.seek(0)
-        new_las = laspy.read(stream)
-        assert np.all(new_las.header.mins == [0.0, 0.0, 0.0])
-        assert np.all(new_las.header.maxs == [0.0, 0.0, 0.0])
-        assert np.sum(new_las.header.number_of_points_by_return) == 0
+import copy
+import io
+from datetime import date
+
+import numpy as np
+import pytest
+
+import laspy
+from laspy import LasHeader
+from laspy.lib import write_then_read_again
+from tests import test_common
+
+all_las_but_1_4 = test_common.all_las_but_1_4
+
+
+def test_number_of_points_return_is_updated(all_las_but_1_4):
+    las = all_las_but_1_4
+
+    nb_points = len(las.points)
+    nb_slice = 3
+
+    r = las.return_number
+
+    for i in reversed(range(nb_slice)):
+        r[i * (nb_points // nb_slice) : (i + 1) * (nb_points // nb_slice)] = i + 1
+
+    las = test_common.write_then_read_again(las)
+
+    assert (
+        tuple(las.header.number_of_points_by_return[:nb_slice])
+        == (nb_points // nb_slice,) * nb_slice
+    )
+    assert tuple(las.header.number_of_points_by_return[nb_slice:]) == (0,) * (
+        len(las.header.number_of_points_by_return) - nb_slice
+    )
+
+
+def test_nb_points_return_1_4():
+    las = laspy.read(test_common.test1_4_las)
+
+    r = las.return_number
+
+    for i in range(15):
+        r[i] = i + 1
+
+    r[15:] = 15
+
+    las = test_common.write_then_read_again(las)
+
+    assert tuple(las.header.number_of_points_by_return) == ((1,) * 14) + (
+        len(las.points) - 14,
+    )
+
+
+def test_header_copy():
+    las = laspy.read(test_common.simple_las)
+    header_copy = copy.copy(las.header)
+
+    assert header_copy.point_format.id == las.header.point_format.id
+    assert header_copy.version == las.header.version
+
+    header_copy.point_format_id = 0
+    assert header_copy.point_format_id != las.header.point_format.id
+    assert header_copy.version == las.header.version
+
+
+def test_set_uuid():
+    import uuid
+
+    las = laspy.read(test_common.simple_las)
+    u = uuid.uuid4()
+    las.header.uuid = u
+    las = test_common.write_then_read_again(las)
+    assert las.header.uuid == u
+
+
+def test_set_offsets():
+    header = laspy.header.LasHeader()
+    header.offsets = [0.5, 0.6, 0.7]
+
+    assert 0.5 == header.x_offset
+    assert 0.6 == header.y_offset
+    assert 0.7 == header.z_offset
+    assert [0.5, 0.6, 0.7] == list(header.offsets)
+
+
+def test_set_scales():
+    header = laspy.header.LasHeader()
+    header.scales = [0.001, 0.001, 0.01]
+
+    assert 0.001 == header.x_scale
+    assert 0.001 == header.y_scale
+    assert 0.01 == header.z_scale
+    assert [0.001, 0.001, 0.01] == list(header.scales)
+
+
+def test_set_maxs():
+    header = laspy.header.LasHeader()
+    values = [42.0, 1337.42, 553.3]
+    header.maxs = values
+
+    assert values[0] == header.x_max
+    assert values[1] == header.y_max
+    assert values[2] == header.z_max
+    assert values == list(header.maxs)
+
+
+def test_set_mins():
+    header = laspy.header.LasHeader()
+    values = [42.0, 1337.42, 553.3]
+    header.mins = values
+
+    assert values[0] == header.x_min
+    assert values[1] == header.y_min
+    assert values[2] == header.z_min
+    assert values == list(header.mins)
+
+
+def test_point_count_stays_synchronized():
+    las = laspy.read(test_common.simple_las)
+    assert las.header.point_count == len(las.points)
+
+    las.points = las.points[:120]
+    assert 120 == las.header.point_count
+    assert las.header.point_count == len(las.points)
+
+
+def test_header_date():
+    las = laspy.read(test_common.extra_bytes_las)
+    with io.BytesIO() as out:
+        las.header.write_to(out)
+        out.seek(0)
+        header_2 = LasHeader.read_from(out)
+
+    expected_date = date(year=2015, month=2, day=22)
+    assert las.header.creation_date == expected_date
+    assert las.header.creation_date == header_2.creation_date
+
+
+def test_set_vlrs_header():
+    """
+    Test that when setting the vlrs of a header,
+    if the given vlr list has an extra bytes vlr,
+    the header does not take it, as this header is specific
+    """
+    las = laspy.read(test_common.extra_bytes_las)
+
+    # test that it exists
+    _ = las.vlrs.index("ExtraBytesVlr")
+
+    hdr = laspy.LasHeader()
+    hdr.vlrs = las.vlrs
+    # Now it should not be in the hdr vlrs
+    with pytest.raises(ValueError):
+        _ = hdr.vlrs.index("ExtraBytesVlr")
+    # but still in the original list
+    _ = las.vlrs.index("ExtraBytesVlr")
+
+
+def test_extra_header_bytes():
+    las = laspy.read(test_common.simple_las)
+
+    extra_bytes = "Some extra bytes between header and VLRs".encode()
+    las.header.extra_header_bytes = extra_bytes
+    assert las.header.extra_header_bytes == extra_bytes
+
+    las = write_then_read_again(las)
+    assert las.header.extra_header_bytes == extra_bytes
+
+
+def test_extra_vlr_bytes():
+    las = laspy.read(test_common.simple_las)
+
+    extra_bytes = "Some extra bytes between VLRs and start of points".encode()
+    las.header.extra_vlr_bytes = extra_bytes
+    assert las.header.extra_vlr_bytes == extra_bytes
+
+    las = write_then_read_again(las)
+    assert las.header.extra_vlr_bytes == extra_bytes
+
+
+def test_header_update_after_slicing():
+    """Test that after slicing a LasData and after its header was
+    updated, its header's bound correctly reflect the new points.
+    """
+    las = laspy.read(test_common.simple_las)
+
+    def dim_min_max_from_header(header, dim_name):
+        if dim_name == "x":
+            return header.x_min, header.x_max
+
+        if dim_name == "y":
+            return header.y_min, header.y_max
+
+        if dim_name == "z":
+            return header.z_min, header.z_max
+
+        raise RuntimeError(f"Bad dim name {dim_name}")
+
+    for dim in ("x", "y", "z"):
+        values = las[dim]
+
+        old_min, old_max = dim_min_max_from_header(las.header, dim)
+        size = old_max - old_min
+        new_max = old_min + (size * 0.75)
+        new_min = old_min + (size * 0.25)
+
+        mask = (new_min < values) & (values < new_max)
+        las.points = las.points[mask]
+
+        values = las[dim]
+
+        new_header_min, new_header_max = dim_min_max_from_header(las.header, dim)
+        assert (
+            new_header_max == values.max()
+        ), "Header max value does not correspond to actual max value"
+        assert (
+            new_header_min == values.min()
+        ), "Header min value does not correspond to actual min value"
+        assert new_header_min > old_min
+        assert new_header_max < old_max
+
+
+def test_header_update_setting_points_on_new_las():
+    """Internally, when updating the header, its mins and maxs will temporarily be set
+    to f64::max_value and f64::min_value. This test is to make sure those value are
+    truly temporary. Even when setting the points to an empty record
+    """
+    las = laspy.read(test_common.simple_las)
+
+    new_las = laspy.create(
+        point_format=las.header.point_format, file_version=las.header.version
+    )
+    assert np.all(new_las.header.mins == [0.0, 0.0, 0.0])
+    assert np.all(new_las.header.maxs == [0.0, 0.0, 0.0])
+    assert np.sum(new_las.header.number_of_points_by_return) == 0
+
+    new_las.points = laspy.PackedPointRecord.empty(new_las.point_format)
+    assert np.all(new_las.header.mins == [0.0, 0.0, 0.0])
+    assert np.all(new_las.header.maxs == [0.0, 0.0, 0.0])
+    assert np.sum(new_las.header.number_of_points_by_return) == 0
+
+    new_las.points = las.points.copy()
+    assert np.all(new_las.header.mins == las.header.mins)
+    assert np.all(new_las.header.maxs == las.header.maxs)
+    assert np.all(
+        new_las.header.number_of_points_by_return
+        == las.header.number_of_points_by_return
+    )
+
+
+def test_writing_does_not_reset_customly_set_data():
+    """If the user does set a data in a LasHeader,
+    the writer should not change it to date.today
+    """
+
+    DATE = date(year=1990, month=11, day=21)
+
+    las = laspy.read(test_common.simple_las)
+    assert las.header.creation_date != DATE
+
+    new_header = laspy.LasHeader(
+        version=las.header.version, point_format=las.header.point_format
+    )
+
+    assert new_header.creation_date == date.today()
+    new_header.creation_date = DATE
+    assert new_header.creation_date == DATE
+
+    new_las = laspy.LasData(header=new_header, points=las.points)
+    read_new_las = write_then_read_again(new_las)
+    assert read_new_las.header.date == DATE
+    assert new_las.header.date == DATE
+
+
+def test_not_setting_date_in_new_header_resets_to_date_today():
+    las = laspy.read(test_common.simple_las)
+
+    new_header = laspy.LasHeader(
+        version=las.header.version, point_format=las.header.point_format
+    )
+    assert new_header.creation_date == date.today()
+
+    new_las = laspy.LasData(header=new_header, points=las.points)
+    read_new_las = write_then_read_again(new_las)
+    assert read_new_las.header.date == date.today()
+    assert new_header.creation_date == date.today()
+
+
+def test_writing_when_creation_date_is_None():
+    las = laspy.read(test_common.simple_las)
+
+    new_header = laspy.LasHeader(
+        version=las.header.version, point_format=las.header.point_format
+    )
+    assert new_header.creation_date == date.today()
+    new_header.creation_date = None
+    assert new_header.creation_date is None
+
+    new_las = laspy.LasData(header=new_header, points=las.points)
+    read_new_las = write_then_read_again(new_las)
+    assert read_new_las.header.creation_date == date.today()
+    assert new_header.creation_date is None
+
+
+def test_header_min_max_chunk_mode():
+    """Test that when writing a file using 'chunk mode' the header`s bounds are correct"""
+    las = laspy.read(test_common.simple_las)
+    header = laspy.LasHeader(
+        point_format=las.header.point_format, version=las.header.version
+    )
+    with io.BytesIO() as stream:
+        with laspy.open(stream, mode="w", header=header, closefd=False) as writer:
+            # We intenionally write the file in two write_points call
+            writer.write_points(las.points[: len(las.points) // 2])
+            writer.write_points(las.points[len(las.points) // 2 :])
+
+        stream.seek(0)
+        new_las = laspy.read(stream)
+        assert np.all(new_las.header.maxs == las.header.maxs)
+        assert np.all(new_las.header.mins == las.header.mins)
+
+
+def test_update_header_empty_las_data():
+    """Test updating the header on and empyt las, and writing
+    an empyt las produces correct bounds values in header
+
+    """
+    las = laspy.create()
+    las.update_header()
+
+    assert np.all(las.header.mins == [0.0, 0.0, 0.0])
+    assert np.all(las.header.maxs == [0.0, 0.0, 0.0])
+    assert np.sum(las.header.number_of_points_by_return) == 0
+
+    las = write_then_read_again(las)
+    assert np.all(las.header.mins == [0.0, 0.0, 0.0])
+    assert np.all(las.header.maxs == [0.0, 0.0, 0.0])
+    assert np.sum(las.header.number_of_points_by_return) == 0
+
+    header = laspy.LasHeader()
+    with io.BytesIO() as stream:
+        with laspy.open(stream, mode="w", header=header, closefd=False) as writer:
+            # We intenionally don't write points
+            pass
+        stream.seek(0)
+        new_las = laspy.read(stream)
+        assert np.all(new_las.header.mins == [0.0, 0.0, 0.0])
+        assert np.all(new_las.header.maxs == [0.0, 0.0, 0.0])
+        assert np.sum(new_las.header.number_of_points_by_return) == 0
```

### Comparing `laspy-2.4.1/tests/test_laspy.py` & `laspy-2.5.0/tests/test_laspy.py`

 * *Ordering differences only*

 * *Files 14% similar despite different names*

```diff
@@ -1,690 +1,690 @@
-import os
-import time
-import unittest
-from uuid import UUID
-
-import numpy as np
-import pytest
-
-import laspy
-
-
-def flip_bit(x):
-    return 1 * (x == 0)
-
-
-class LasReaderTestCase(unittest.TestCase):
-    simple = os.path.join(os.path.dirname(__file__), "data", "simple.las")
-    tempfile = "junk.las"
-
-    def setUp(self):
-        self.FileObject = laspy.read(self.simple)
-        LasFile = self.FileObject
-        self.X = list(LasFile.X)
-        self.Y = list(LasFile.Y)
-        self.Z = list(LasFile.Z)
-        self.intensity = list(LasFile.intensity)
-        self.flag_byte = list(LasFile.flag_byte)
-        self.return_num = list(LasFile.return_num)
-        self.num_returns = list(LasFile.num_returns)
-        self.scan_dir_flag = list(LasFile.scan_dir_flag)
-        self.edge_flight_line = list(LasFile.edge_flight_line)
-        self.raw_classification = list(LasFile.raw_classification)
-        self.classification = list(LasFile.classification)
-        self.synthetic = list(LasFile.synthetic)
-        self.key_point = list(LasFile.key_point)
-        self.withheld = list(LasFile.withheld)
-        self.scan_angle_rank = list(LasFile.scan_angle_rank)
-        self.user_data = list(LasFile.user_data)
-        self.pt_src_id = list(LasFile.pt_src_id)
-        ## The following conditional code is redundant for
-        ## simple.las, which of course has only one pt. format.
-        ## Perhaps find several other files?
-        if LasFile.header.point_format.id in (1, 2, 3, 4, 5):
-            self.gps_time = list(LasFile.gps_time)
-        if LasFile.header.point_format.id in (2, 3, 5):
-            self.red = list(LasFile.red)
-            self.green = list(LasFile.green)
-            self.blue = list(LasFile.blue)
-        if LasFile.header.point_format.id in (4, 5):
-            self.wave_form_packet_Desc_index = list(LasFile.wave_packet_desc_index)
-            self.byte_offset_to_waveform = list(LasFile.byte_offset_to_waveform)
-            self.waveform_packet_size = list(LasFile.waveform_packet_size)
-            self.return_point_waveform_loc = list(LasFile.return_point_waveform_loc)
-            self.x_t = list(LasFile.x_t)
-            self.y_t = list(LasFile.y_t)
-            self.z_t = list(LasFile.z_t)
-
-        self.p1 = LasFile.points[100]
-        self.p2 = LasFile.points[976]
-
-        self.idx1 = 100
-        self.idx2 = 976
-
-    def test_x(self):
-        """Fetch and test X dimension"""
-        self.assertEqual(self.p1.X, 63666106, self.X[self.idx1])
-        self.assertEqual(self.p2.X, 63714022, self.X[self.idx2])
-
-    def test_y(self):
-        """Fetch and test Y dimension"""
-        self.assertEqual(self.p1.Y, 84985413, self.Y[self.idx1])
-        self.assertEqual(self.p2.Y, 85318232, self.Y[self.idx2])
-
-    def test_z(self):
-        """Fetch and test Z dimension"""
-        self.assertEqual(self.p1.Z, 42490, self.Z[self.idx1])
-        self.assertEqual(self.p2.Z, 42306, self.Z[self.idx2])
-
-    def test_intensity(self):
-        """Fetch and test intensity dimension"""
-        self.assertEqual(self.p1.intensity, 233, self.intensity[self.idx1])
-        self.assertEqual(self.p2.intensity, 1, self.intensity[self.idx2])
-
-    def test_bit_flags(self):
-        """Fetch and test the binary flags associated with flag_byte dimension"""
-        self.assertEqual(self.p1.flag_byte, self.flag_byte[self.idx1])
-        self.assertEqual(self.p2.flag_byte, self.flag_byte[self.idx2])
-        self.assertEqual(self.p1.return_num, self.return_num[self.idx1], 1)
-        self.assertEqual(self.p2.return_num, self.return_num[self.idx2], 2)
-        self.assertEqual(self.p1.num_returns, self.num_returns[self.idx1], 1)
-        self.assertEqual(self.p2.num_returns, self.num_returns[self.idx2], 2)
-        self.assertEqual(self.p1.scan_dir_flag, self.scan_dir_flag[self.idx1], 0)
-        self.assertEqual(self.p2.scan_dir_flag, self.scan_dir_flag[self.idx2], 1)
-        self.assertEqual(self.p1.edge_flight_line, self.edge_flight_line[self.idx1], 0)
-        self.assertEqual(self.p2.edge_flight_line, self.edge_flight_line[self.idx2], 0)
-
-    def test_scan_angle_rank(self):
-        """Fetch and test scan_angle_rank dimension"""
-        self.assertEqual(self.p1.scan_angle_rank, 2, self.scan_angle_rank[self.idx1])
-        self.assertEqual(self.p2.scan_angle_rank, 12, self.scan_angle_rank[self.idx2])
-
-    def test_raw_classification(self):
-        """Fetch and test the dimension of raw_classification bytes"""
-        self.assertEqual(
-            self.p1.raw_classification, 1, self.raw_classification[self.idx1]
-        )
-        self.assertEqual(
-            self.p2.raw_classification, 2, self.raw_classification[self.idx2]
-        )
-
-    def test_ptstrcid(self):
-        """Fetch and test pt_src_id dimension"""
-        self.assertEqual(self.p1.pt_src_id, 7328, self.pt_src_id[self.idx1])
-        self.assertEqual(self.p2.pt_src_id, 7334, self.pt_src_id[self.idx2])
-
-    def test_GPSTime(self):
-        """Fetch and test gps_time dimension"""
-        self.assertTrue(
-            self.p1.gps_time - 2 * 246504.221932 + self.gps_time[self.idx1] < 0.00001
-        )
-        self.assertTrue(
-            self.p2.gps_time - 2 * 249774.658254 + self.gps_time[self.idx2] < 0.00001
-        )
-
-    def test_red(self):
-        """Fetch and test red dimension"""
-        self.assertEqual(self.p1.red, 92, self.red[self.idx1])
-        self.assertEqual(self.p2.red, 94, self.red[self.idx2])
-
-    def test_green(self):
-        """Fetch and test green dimension"""
-        self.assertEqual(self.p1.green, 100, self.green[self.idx1])
-        self.assertEqual(self.p2.green, 84, self.green[self.idx2])
-
-    def test_blue(self):
-        """Fetch and test blue dimension"""
-        self.assertEqual(self.p1.blue, 110, self.blue[self.idx1])
-        self.assertEqual(self.p2.blue, 94, self.blue[self.idx2])
-
-
-class LasWriterTestCase(unittest.TestCase):
-    simple = os.path.join(os.path.dirname(__file__), "data", "simple.las")
-    tempfile = "writer.las"
-    output_tempfile = "writer_output.las"
-
-    def setUp(self):
-        self.FileObject = laspy.read(self.simple)
-
-    def test_x(self):
-        """Writing and testing X dimenson"""
-        X = self.FileObject.X + 1
-        self.FileObject.X = X
-        X2 = self.FileObject.X
-        self.assertTrue(np.all(X == X2))
-
-        scaled_x = self.FileObject.x
-        self.FileObject.x = scaled_x
-        self.assertTrue(np.all(scaled_x == self.FileObject.x))
-
-    def test_y(self):
-        """Writing and testing Y dimension"""
-        Y = self.FileObject.Y + 1
-        self.FileObject.Y = Y
-        Y2 = self.FileObject.Y
-        self.assertTrue(np.all(Y == Y2))
-
-        scaled_y = self.FileObject.y
-        self.FileObject.y = scaled_y
-        self.assertTrue(np.all(scaled_y == self.FileObject.y))
-
-    def test_z(self):
-        """Writing and testing Z dimension"""
-        Z = self.FileObject.Z + 1
-        self.FileObject.Z = Z
-        Z2 = self.FileObject.Z
-        self.assertTrue(np.all(Z == Z2))
-
-        scaled_z = self.FileObject.z
-        self.FileObject.z = scaled_z
-        self.assertTrue(np.all(scaled_z == self.FileObject.z))
-
-    def test_intensity(self):
-        """Writing and testing intensity dimension"""
-        i = self.FileObject.intensity + 1
-        self.FileObject.intensity = i
-        i2 = self.FileObject.intensity
-        self.assertTrue(np.all(i == i2))
-
-    def test_return_num(self):
-        """Writing and testing return_num dimension"""
-        rn = self.FileObject.return_num + 1
-        self.FileObject.return_num = rn
-        rn2 = self.FileObject.return_num
-        self.assertTrue(np.all(rn == rn2))
-
-    def test_overflow_return_num(self):
-        """Testing overflow handling"""
-        rn = self.FileObject.return_num + 100000
-        with self.assertRaises(OverflowError):
-            self.FileObject.return_num = rn
-
-    def test_num_returns(self):
-        """Writing and testing num_returns dimension"""
-        nr = self.FileObject.num_returns + 1
-        self.FileObject.num_returns = nr
-        nr2 = self.FileObject.num_returns
-        self.assertTrue(np.all(nr == nr2))
-
-    def test_scan_dir_flag(self):
-        """Writing and testing scan_dir_flag dimension"""
-        sdf = np.array([flip_bit(x) for x in self.FileObject.scan_dir_flag])
-        self.FileObject.scan_dir_flag = sdf
-        sdf2 = self.FileObject.scan_dir_flag
-        self.assertTrue(np.all(sdf == sdf2))
-
-    def test_edge_flight_line(self):
-        """Writing and testing edge_flight_line dimension"""
-        efl = np.array([flip_bit(x) for x in self.FileObject.edge_flight_line])
-        self.FileObject.edge_flight_line = efl
-        efl2 = self.FileObject.edge_flight_line
-        self.assertTrue(np.all(efl == efl2))
-
-    def test_classification(self):
-        """Writing and testing classification byte."""
-        c1 = self.FileObject.classification + 1
-        self.FileObject.classification = c1
-        c2 = self.FileObject.classification
-        self.assertTrue(np.all(c1 == c2))
-
-    def test_synthetic(self):
-        """Writing and testing synthetic"""
-        s1 = flip_bit(self.FileObject.synthetic)
-        self.FileObject.synthetic = s1
-        s2 = self.FileObject.synthetic
-        self.assertTrue(np.all(s1 == s2))
-
-    def test_key_point(self):
-        """Writing and testing key point"""
-        k1 = flip_bit(self.FileObject.key_point)
-        self.FileObject.key_point = k1
-        k2 = self.FileObject.key_point
-        self.assertTrue(np.all(k1 == k2))
-
-    def test_withheld(self):
-        """Writing and testing withheld"""
-        w1 = flip_bit(self.FileObject.withheld)
-        self.FileObject.withheld = w1
-        w2 = self.FileObject.withheld
-        self.assertTrue(np.all(w1 == w2))
-
-    def test_scan_angle_rank(self):
-        """Writing and testing scan angle rank"""
-        ar1 = self.FileObject.scan_angle_rank
-        ar1[ar1 >= 1] -= 1
-        self.FileObject.scan_angle_rank = ar1
-        ar2 = self.FileObject.scan_angle_rank
-        self.assertTrue(np.all(ar1 == ar2))
-
-    def test_user_data(self):
-        """Writing and testing user data"""
-        ud1 = self.FileObject.user_data + 1
-        self.FileObject.user_data = ud1
-        ud2 = self.FileObject.user_data
-        self.assertTrue(np.all(ud1 == ud2))
-
-    def test_pt_src_id(self):
-        """Writing and testing point source id"""
-        p1 = self.FileObject.user_data + 1
-        self.FileObject.user_data = p1
-        p2 = self.FileObject.user_data
-        self.assertTrue(np.all(p1 == p2))
-
-    def test_gps_time(self):
-        """Writing and testing gps time"""
-        g1 = self.FileObject.gps_time + 1.0
-        self.FileObject.gps_time = g1
-        g2 = self.FileObject.gps_time
-        self.assertTrue(np.all(g1 == g2))
-
-    def test_red(self):
-        """Writing and testing red"""
-        r1 = self.FileObject.red + 1
-        self.FileObject.red = r1
-        r2 = self.FileObject.red
-        self.assertTrue(np.all(r1 == r2))
-
-    def test_green(self):
-        """Writing and testing green"""
-        g1 = self.FileObject.green + 1
-        self.FileObject.green = g1
-        g2 = self.FileObject.green
-        self.assertTrue(np.all(g1 == g2))
-
-    def test_blue(self):
-        """Writing and testing blue"""
-        b1 = self.FileObject.blue + 1
-        self.FileObject.blue = b1
-        b2 = self.FileObject.blue
-        self.assertTrue(np.all(b1 == b2))
-
-    # def test_vlr_defined_dimensions2(self):
-    #     """Testing VLR defined dimension API"""
-    #     File2 = File.File(self.output_tempfile, mode="w", header=self.FileObject.header)
-    #     File2.define_new_dimension("test_dimension", 5, "This is a test.")
-    #     File2.X = self.FileObject.X
-    #     self.assertTrue(File2.test_dimension[500] == 0)
-    #     File2.close(ignore_header_changes=True)
-
-    def tearDown(self):
-        self.FileObject.write(self.output_tempfile)
-        really_remove(self.output_tempfile)
-
-
-class LasHeaderWriterTestCase(unittest.TestCase):
-    simple = os.path.join(os.path.dirname(__file__), "data", "simple.las")
-    simple14 = os.path.join(os.path.dirname(__file__), "data", "simple1_4.las")
-    tempfile = os.path.abspath("headerwriter.las")
-    tempfile2 = os.path.abspath("headerwriter2.las")
-
-    def setUp(self):
-        self.las = laspy.read(self.simple)
-
-    def test_file_src(self):
-        """Testing file_src"""
-        f1 = self.las.header.file_source_id + 1
-        self.las.header.file_source_id = f1
-        f2 = self.las.header.file_source_id
-        assert f1 == f2
-
-    @pytest.mark.skip(reason="API changed")
-    def test_uuid(self):
-        """Testing uuid"""
-        guid = self.las.header.guid
-        guid2 = self.las.header.project_id
-        self.assertEqual(guid, guid2)
-        newGuid = UUID(bytes=b"1" * 16)
-        self.las.header.guid = newGuid
-        newGuid2 = self.las.header.get_guid()
-        self.assertEqual(newGuid, newGuid2)
-
-    def test_versions(self):
-        """Testing Versions"""
-        assert self.las.header.version.major == 1
-        with self.assertRaises(AttributeError):
-            self.las.header.version.major = 2
-
-    def test_system_id(self):
-        """Testing System ID"""
-        sys1 = self.las.header.system_identifier
-        sys1 = "1234567891" + sys1[10:]
-        self.las.header.system_identifier = sys1
-        sys2 = self.las.header.system_identifier
-        assert sys1 == sys2
-
-    def test_software_id(self):
-        """ "Testing Software ID"""
-        s1 = self.las.header.generating_software
-        s1 = "1234567" + s1[7:]
-        self.las.header.generating_software = s1
-        s2 = self.las.header.generating_software
-        assert s1 == s2
-        # with self.assertRaises(laspy.LaspyException):
-        #     self.las.header.generating_software = "123"
-        # with self.assertRaises(laspy.LaspyException):
-        #     self.las.header.generating_software = "1" * 100
-
-    def test_date(self):
-        """Testing Date"""
-        d1 = self.las.header.creation_date
-        assert d1 is None
-        from datetime import datetime
-
-        d2 = datetime(2007, 12, 10)
-        self.las.header.creation_date = d2
-        d3 = self.las.header.creation_date
-        self.assertEqual(d2, d3)
-
-    def test_point_recs_by_return(self):
-        """Testing point records by return"""
-        r1 = self.las.header.number_of_points_by_return + 1
-        self.las.header.number_of_points_by_return = r1
-        r2 = self.las.header.number_of_points_by_return
-        assert np.all(r1 == r2)
-
-    def test_min_max_update(self):
-        """Testing the update min/max function"""
-        x = self.las.X
-        x[0] = max(x) + 1
-        y = self.las.Y
-        y[0] = max(y) + 1
-        z = self.las.Z
-        z[0] = max(z) + 1
-        self.las.X = x
-        self.las.Y = y
-        self.las.Z = z
-        self.las.update_header()
-        file_max = self.las.header.maxs
-        assert np.all(file_max == [self.las.x[0], self.las.y[0], self.las.z[0]])
-
-    def test_histogram(self):
-        """Testing the update_histogram functon"""
-        h1 = self.las.header.number_of_points_by_return
-        self.las.update_header()
-        h2 = self.las.header.number_of_points_by_return
-        assert np.all(h1 == h2)
-
-    def test_offset(self):
-        """Testing offset"""
-        o1 = self.las.header.offsets
-        o1[0] += 1
-        self.las.header.offsets = o1
-        o2 = self.las.header.offsets
-        assert np.all(o1 == o2)
-
-    def test_scale(self):
-        """Testing Scale"""
-        s1 = self.las.header.scales
-        s1[0] += 1
-        self.las.header.scales = s1
-        s2 = self.las.header.scales
-        assert np.all(s1 == s2)
-
-
-class LasWriteModeTestCase(unittest.TestCase):
-    simple = os.path.join(os.path.dirname(__file__), "data", "simple.las")
-    tempfile = "write-mode.las"
-    output_tempfile = "write-mode-output.las"
-
-    def setUp(self):
-        self.File1 = laspy.read(self.simple)
-
-    def test_using_barebones_header(self):
-        """Testing file creation using barebones header"""
-        header = laspy.LasHeader()
-
-        File2 = laspy.LasData(header)
-
-        self.assertTrue(File2.header.version == "1.2")
-
-        X = self.File1.X
-        Y = self.File1.Y
-        Z = self.File1.Z
-        File2.X = X
-        File2.Y = Y
-        File2.Z = Z
-
-        File2.write(self.output_tempfile)
-        File2 = laspy.read(self.output_tempfile)
-
-        self.assertTrue(np.all(X == File2.X))
-        self.assertTrue(np.all(Y == File2.Y))
-        self.assertTrue(np.all(Z == File2.Z))
-
-    def test_using_existing_header(self):
-        """Test file creation using an existing header"""
-        File2 = laspy.LasData(self.File1.header)
-        X = self.File1.X
-        Y = self.File1.Y
-        Z = self.File1.Z
-        File2.X = X
-        File2.Y = Y
-        File2.Z = Z
-
-        File2.write(self.output_tempfile)
-        File2 = laspy.read(self.output_tempfile)
-
-        self.assertTrue(np.all(X == File2.X))
-        self.assertTrue(np.all(Y == File2.Y))
-        self.assertTrue(np.all(Z == File2.Z))
-
-    def tearDown(self):
-        really_remove(self.output_tempfile)
-
-
-class LasV_13TestCase(unittest.TestCase):
-    simple = os.path.join(os.path.dirname(__file__), "data", "simple1_3.las")
-    output_tempfile = "v13-output.las"
-
-    def setUp(self):
-        self.File1 = laspy.read(self.simple)
-
-    def test_glob_encode(self):
-        """Testing v1.3 Global Encoding"""
-        old = self.File1.header.global_encoding.gps_time_type
-        assert old == laspy.header.GpsTimeType.WEEK_TIME
-        self.File1.header.global_encoding.gps_time_type = (
-            laspy.header.GpsTimeType.STANDARD
-        )
-        assert (
-            self.File1.header.global_encoding.gps_time_type
-            == laspy.header.GpsTimeType.STANDARD
-        )
-
-        self.File1.header.global_encoding.gps_time_type = (
-            laspy.header.GpsTimeType.WEEK_TIME
-        )
-        assert (
-            self.File1.header.global_encoding.gps_time_type
-            == laspy.header.GpsTimeType.WEEK_TIME
-        )
-
-        File2 = laspy.LasData(self.File1.header)
-        File2.write(self.output_tempfile)
-        File2 = laspy.read(self.output_tempfile)
-
-        self.assertEqual(
-            self.File1.header.global_encoding.waveform_data_packets_internal,
-            File2.header.global_encoding.waveform_data_packets_internal,
-        )
-        self.assertEqual(
-            self.File1.header.global_encoding.waveform_data_packets_external,
-            File2.header.global_encoding.waveform_data_packets_external,
-        )
-        self.assertEqual(
-            self.File1.header.global_encoding.synthetic_return_numbers,
-            File2.header.global_encoding.synthetic_return_numbers,
-        )
-
-    def test_wave_packet_desc_index(self):
-        """Testing wave_packet_desc_index."""
-        test1 = self.File1.wave_packet_desc_index
-        File2 = laspy.LasData(self.File1.header)
-        File2.points = self.File1.points
-        assert np.all(test1 == File2.wave_packet_desc_index)
-
-    def test_byte_offset_to_waveform_data(self):
-        """Testing byte_offset_to_waveform_data"""
-        test1 = self.File1.byte_offset_to_waveform_data
-        File2 = laspy.LasData(self.File1.header)
-        File2.points = self.File1.points
-        assert np.all(test1 == File2.byte_offset_to_waveform_data)
-
-    def test_waveform_packet_size(self):
-        """Testing waveform_packet_size"""
-        test1 = self.File1.waveform_packet_size
-        File2 = laspy.LasData(self.File1.header)
-        File2.points = self.File1.points.copy()
-        assert np.all(test1 == File2.waveform_packet_size)
-
-    def test_return_point_waveform_loc(self):
-        """Testing return_point_waveform_loc"""
-        test1 = self.File1.return_point_waveform_loc
-        File2 = laspy.LasData(self.File1.header)
-        File2.points = self.File1.points.copy()
-        assert np.all(test1 == File2.return_point_waveform_loc)
-        File2.return_point_waveform_loc += 1
-        assert np.all(test1 != File2.return_point_waveform_loc)
-
-    def test_x_t(self):
-        """Testing x_t"""
-        test1 = self.File1.x_t
-        File2 = laspy.LasData(self.File1.header)
-        File2.points = self.File1.points.copy()
-        assert np.all(test1 == File2.x_t)
-        File2.x_t += 1
-        assert np.all(test1 != File2.x_t)
-
-    def test_y_t(self):
-        """Testing y_t"""
-        test1 = self.File1.y_t
-        File2 = laspy.LasData(self.File1.header)
-        File2.points = self.File1.points.copy()
-        np.all(test1 == File2.y_t)
-        File2.y_t += 1
-        assert np.all(test1 != File2.y_t)
-
-    def test_z_t(self):
-        """Testing z_t"""
-        test1 = self.File1.z_t
-        File2 = laspy.LasData(self.File1.header)
-        File2.points = self.File1.points.copy()
-        np.all(test1 == File2.z_t)
-        File2.z_t += 1
-        np.all(test1 != File2.z_t)
-
-    def tearDown(self):
-        really_remove(self.output_tempfile)
-
-
-class LasV_14TestCase(unittest.TestCase):
-    simple = os.path.join(os.path.dirname(__file__), "data", "simple1_4.las")
-    tempfile = "v14.las"
-    output_tempfile = "v14-output.las"
-
-    def setUp(self):
-        self.File1 = laspy.read(self.simple)
-
-    def test_glob_encode(self):
-        """Testing v1.4 Global Encoding"""
-        old = self.File1.header.global_encoding.gps_time_type
-        assert old == laspy.header.GpsTimeType.WEEK_TIME
-        self.File1.header.global_encoding.gps_time_type = (
-            laspy.header.GpsTimeType.STANDARD
-        )
-        assert (
-            self.File1.header.global_encoding.gps_time_type
-            == laspy.header.GpsTimeType.STANDARD
-        )
-
-        File2 = laspy.LasData(self.File1.header)
-        self.assertEqual(
-            self.File1.header.global_encoding.waveform_data_packets_internal,
-            File2.header.global_encoding.waveform_data_packets_internal,
-        )
-        self.assertEqual(
-            self.File1.header.global_encoding.waveform_data_packets_external,
-            File2.header.global_encoding.waveform_data_packets_external,
-        )
-        self.assertEqual(
-            self.File1.header.global_encoding.synthetic_return_numbers,
-            File2.header.global_encoding.synthetic_return_numbers,
-        )
-
-    def test_glob_encode_bits(self):
-        b1 = self.File1.header.global_encoding.gps_time_type
-        b2 = self.File1.header.global_encoding.waveform_data_packets_internal
-        b3 = self.File1.header.global_encoding.waveform_data_packets_external
-        b4 = self.File1.header.global_encoding.synthetic_return_numbers
-        b5 = self.File1.header.global_encoding.wkt
-
-        bf1 = 1 - int(b1)
-        bf2 = 1 - int(b2)
-        bf3 = 1 - int(b3)
-        bf4 = 1 - int(b4)
-        bf5 = 1 - int(b5)
-
-        self.File1.header.global_encoding.gps_time_type = bf1
-        self.File1.header.global_encoding.waveform_data_packets_internal = bf2
-        self.File1.header.global_encoding.waveform_data_packets_external = bf3
-        self.File1.header.global_encoding.synthetic_return_numbers = bf4
-        self.File1.header.global_encoding.wkt = bf5
-
-        assert self.File1.header.global_encoding.gps_time_type == bf1
-        assert self.File1.header.global_encoding.waveform_data_packets_internal == bf2
-        assert self.File1.header.global_encoding.waveform_data_packets_external == bf3
-        assert self.File1.header.global_encoding.synthetic_return_numbers == bf4
-        assert self.File1.header.global_encoding.wkt == bf5
-
-    def test_classification_variables(self):
-        """Testing v1.4 classification support"""
-        classification = self.File1.classification
-        classification_flags = self.File1.classification_flags
-        scanner_channel = self.File1.scanner_channel
-        scan_dir_flag = self.File1.scan_dir_flag
-        edge_flight_line = self.File1.edge_flight_line
-
-        return_num = self.File1.return_num
-        num_returns = self.File1.num_returns
-
-        File2 = laspy.LasData(self.File1.header)
-        File2.classification = classification
-        File2.classification_flags = classification_flags
-        File2.scan_dir_flag = scan_dir_flag
-        File2.scanner_channel = scanner_channel
-        File2.edge_flight_line = edge_flight_line
-        File2.return_num = return_num
-        File2.num_returns = num_returns
-
-        File2.write(self.output_tempfile)
-        File2 = laspy.read(self.output_tempfile)
-
-        assert np.all(num_returns == File2.num_returns)
-        assert np.all(return_num == File2.return_num)
-        assert np.all(edge_flight_line == File2.edge_flight_line)
-        assert np.all(scan_dir_flag == File2.scan_dir_flag)
-        assert np.all(classification_flags == File2.classification_flags)
-        assert np.all(classification == File2.classification)
-        assert np.all(scanner_channel == File2.scanner_channel)
-
-    def tearDown(self):
-        really_remove(self.output_tempfile)
-
-
-def really_remove(path, max_=1):
-    """
-    Hack for Windows when quickly creating and deleting files.
-    os.remove can return when Windows still thinks the file exists.
-    When trying to re-create the file with the same name, a PermissionError occurs.
-    :param path: path to remove
-    :param max_: max seconds to wait
-    """
-    wait = 0.01
-    while os.path.exists(path):
-        try:
-            os.remove(path)
-        except WindowsError:
-            time.sleep(wait)
-            max_ -= wait
-            if max_ <= 0:
-                break
+import os
+import time
+import unittest
+from uuid import UUID
+
+import numpy as np
+import pytest
+
+import laspy
+
+
+def flip_bit(x):
+    return 1 * (x == 0)
+
+
+class LasReaderTestCase(unittest.TestCase):
+    simple = os.path.join(os.path.dirname(__file__), "data", "simple.las")
+    tempfile = "junk.las"
+
+    def setUp(self):
+        self.FileObject = laspy.read(self.simple)
+        LasFile = self.FileObject
+        self.X = list(LasFile.X)
+        self.Y = list(LasFile.Y)
+        self.Z = list(LasFile.Z)
+        self.intensity = list(LasFile.intensity)
+        self.flag_byte = list(LasFile.flag_byte)
+        self.return_num = list(LasFile.return_num)
+        self.num_returns = list(LasFile.num_returns)
+        self.scan_dir_flag = list(LasFile.scan_dir_flag)
+        self.edge_flight_line = list(LasFile.edge_flight_line)
+        self.raw_classification = list(LasFile.raw_classification)
+        self.classification = list(LasFile.classification)
+        self.synthetic = list(LasFile.synthetic)
+        self.key_point = list(LasFile.key_point)
+        self.withheld = list(LasFile.withheld)
+        self.scan_angle_rank = list(LasFile.scan_angle_rank)
+        self.user_data = list(LasFile.user_data)
+        self.pt_src_id = list(LasFile.pt_src_id)
+        ## The following conditional code is redundant for
+        ## simple.las, which of course has only one pt. format.
+        ## Perhaps find several other files?
+        if LasFile.header.point_format.id in (1, 2, 3, 4, 5):
+            self.gps_time = list(LasFile.gps_time)
+        if LasFile.header.point_format.id in (2, 3, 5):
+            self.red = list(LasFile.red)
+            self.green = list(LasFile.green)
+            self.blue = list(LasFile.blue)
+        if LasFile.header.point_format.id in (4, 5):
+            self.wave_form_packet_Desc_index = list(LasFile.wave_packet_desc_index)
+            self.byte_offset_to_waveform = list(LasFile.byte_offset_to_waveform)
+            self.waveform_packet_size = list(LasFile.waveform_packet_size)
+            self.return_point_waveform_loc = list(LasFile.return_point_waveform_loc)
+            self.x_t = list(LasFile.x_t)
+            self.y_t = list(LasFile.y_t)
+            self.z_t = list(LasFile.z_t)
+
+        self.p1 = LasFile.points[100]
+        self.p2 = LasFile.points[976]
+
+        self.idx1 = 100
+        self.idx2 = 976
+
+    def test_x(self):
+        """Fetch and test X dimension"""
+        self.assertEqual(self.p1.X, 63666106, self.X[self.idx1])
+        self.assertEqual(self.p2.X, 63714022, self.X[self.idx2])
+
+    def test_y(self):
+        """Fetch and test Y dimension"""
+        self.assertEqual(self.p1.Y, 84985413, self.Y[self.idx1])
+        self.assertEqual(self.p2.Y, 85318232, self.Y[self.idx2])
+
+    def test_z(self):
+        """Fetch and test Z dimension"""
+        self.assertEqual(self.p1.Z, 42490, self.Z[self.idx1])
+        self.assertEqual(self.p2.Z, 42306, self.Z[self.idx2])
+
+    def test_intensity(self):
+        """Fetch and test intensity dimension"""
+        self.assertEqual(self.p1.intensity, 233, self.intensity[self.idx1])
+        self.assertEqual(self.p2.intensity, 1, self.intensity[self.idx2])
+
+    def test_bit_flags(self):
+        """Fetch and test the binary flags associated with flag_byte dimension"""
+        self.assertEqual(self.p1.flag_byte, self.flag_byte[self.idx1])
+        self.assertEqual(self.p2.flag_byte, self.flag_byte[self.idx2])
+        self.assertEqual(self.p1.return_num, self.return_num[self.idx1], 1)
+        self.assertEqual(self.p2.return_num, self.return_num[self.idx2], 2)
+        self.assertEqual(self.p1.num_returns, self.num_returns[self.idx1], 1)
+        self.assertEqual(self.p2.num_returns, self.num_returns[self.idx2], 2)
+        self.assertEqual(self.p1.scan_dir_flag, self.scan_dir_flag[self.idx1], 0)
+        self.assertEqual(self.p2.scan_dir_flag, self.scan_dir_flag[self.idx2], 1)
+        self.assertEqual(self.p1.edge_flight_line, self.edge_flight_line[self.idx1], 0)
+        self.assertEqual(self.p2.edge_flight_line, self.edge_flight_line[self.idx2], 0)
+
+    def test_scan_angle_rank(self):
+        """Fetch and test scan_angle_rank dimension"""
+        self.assertEqual(self.p1.scan_angle_rank, 2, self.scan_angle_rank[self.idx1])
+        self.assertEqual(self.p2.scan_angle_rank, 12, self.scan_angle_rank[self.idx2])
+
+    def test_raw_classification(self):
+        """Fetch and test the dimension of raw_classification bytes"""
+        self.assertEqual(
+            self.p1.raw_classification, 1, self.raw_classification[self.idx1]
+        )
+        self.assertEqual(
+            self.p2.raw_classification, 2, self.raw_classification[self.idx2]
+        )
+
+    def test_ptstrcid(self):
+        """Fetch and test pt_src_id dimension"""
+        self.assertEqual(self.p1.pt_src_id, 7328, self.pt_src_id[self.idx1])
+        self.assertEqual(self.p2.pt_src_id, 7334, self.pt_src_id[self.idx2])
+
+    def test_GPSTime(self):
+        """Fetch and test gps_time dimension"""
+        self.assertTrue(
+            self.p1.gps_time - 2 * 246504.221932 + self.gps_time[self.idx1] < 0.00001
+        )
+        self.assertTrue(
+            self.p2.gps_time - 2 * 249774.658254 + self.gps_time[self.idx2] < 0.00001
+        )
+
+    def test_red(self):
+        """Fetch and test red dimension"""
+        self.assertEqual(self.p1.red, 92, self.red[self.idx1])
+        self.assertEqual(self.p2.red, 94, self.red[self.idx2])
+
+    def test_green(self):
+        """Fetch and test green dimension"""
+        self.assertEqual(self.p1.green, 100, self.green[self.idx1])
+        self.assertEqual(self.p2.green, 84, self.green[self.idx2])
+
+    def test_blue(self):
+        """Fetch and test blue dimension"""
+        self.assertEqual(self.p1.blue, 110, self.blue[self.idx1])
+        self.assertEqual(self.p2.blue, 94, self.blue[self.idx2])
+
+
+class LasWriterTestCase(unittest.TestCase):
+    simple = os.path.join(os.path.dirname(__file__), "data", "simple.las")
+    tempfile = "writer.las"
+    output_tempfile = "writer_output.las"
+
+    def setUp(self):
+        self.FileObject = laspy.read(self.simple)
+
+    def test_x(self):
+        """Writing and testing X dimenson"""
+        X = self.FileObject.X + 1
+        self.FileObject.X = X
+        X2 = self.FileObject.X
+        self.assertTrue(np.all(X == X2))
+
+        scaled_x = self.FileObject.x
+        self.FileObject.x = scaled_x
+        self.assertTrue(np.all(scaled_x == self.FileObject.x))
+
+    def test_y(self):
+        """Writing and testing Y dimension"""
+        Y = self.FileObject.Y + 1
+        self.FileObject.Y = Y
+        Y2 = self.FileObject.Y
+        self.assertTrue(np.all(Y == Y2))
+
+        scaled_y = self.FileObject.y
+        self.FileObject.y = scaled_y
+        self.assertTrue(np.all(scaled_y == self.FileObject.y))
+
+    def test_z(self):
+        """Writing and testing Z dimension"""
+        Z = self.FileObject.Z + 1
+        self.FileObject.Z = Z
+        Z2 = self.FileObject.Z
+        self.assertTrue(np.all(Z == Z2))
+
+        scaled_z = self.FileObject.z
+        self.FileObject.z = scaled_z
+        self.assertTrue(np.all(scaled_z == self.FileObject.z))
+
+    def test_intensity(self):
+        """Writing and testing intensity dimension"""
+        i = self.FileObject.intensity + 1
+        self.FileObject.intensity = i
+        i2 = self.FileObject.intensity
+        self.assertTrue(np.all(i == i2))
+
+    def test_return_num(self):
+        """Writing and testing return_num dimension"""
+        rn = self.FileObject.return_num + 1
+        self.FileObject.return_num = rn
+        rn2 = self.FileObject.return_num
+        self.assertTrue(np.all(rn == rn2))
+
+    def test_overflow_return_num(self):
+        """Testing overflow handling"""
+        rn = self.FileObject.return_num + 100000
+        with self.assertRaises(OverflowError):
+            self.FileObject.return_num = rn
+
+    def test_num_returns(self):
+        """Writing and testing num_returns dimension"""
+        nr = self.FileObject.num_returns + 1
+        self.FileObject.num_returns = nr
+        nr2 = self.FileObject.num_returns
+        self.assertTrue(np.all(nr == nr2))
+
+    def test_scan_dir_flag(self):
+        """Writing and testing scan_dir_flag dimension"""
+        sdf = np.array([flip_bit(x) for x in self.FileObject.scan_dir_flag])
+        self.FileObject.scan_dir_flag = sdf
+        sdf2 = self.FileObject.scan_dir_flag
+        self.assertTrue(np.all(sdf == sdf2))
+
+    def test_edge_flight_line(self):
+        """Writing and testing edge_flight_line dimension"""
+        efl = np.array([flip_bit(x) for x in self.FileObject.edge_flight_line])
+        self.FileObject.edge_flight_line = efl
+        efl2 = self.FileObject.edge_flight_line
+        self.assertTrue(np.all(efl == efl2))
+
+    def test_classification(self):
+        """Writing and testing classification byte."""
+        c1 = self.FileObject.classification + 1
+        self.FileObject.classification = c1
+        c2 = self.FileObject.classification
+        self.assertTrue(np.all(c1 == c2))
+
+    def test_synthetic(self):
+        """Writing and testing synthetic"""
+        s1 = flip_bit(self.FileObject.synthetic)
+        self.FileObject.synthetic = s1
+        s2 = self.FileObject.synthetic
+        self.assertTrue(np.all(s1 == s2))
+
+    def test_key_point(self):
+        """Writing and testing key point"""
+        k1 = flip_bit(self.FileObject.key_point)
+        self.FileObject.key_point = k1
+        k2 = self.FileObject.key_point
+        self.assertTrue(np.all(k1 == k2))
+
+    def test_withheld(self):
+        """Writing and testing withheld"""
+        w1 = flip_bit(self.FileObject.withheld)
+        self.FileObject.withheld = w1
+        w2 = self.FileObject.withheld
+        self.assertTrue(np.all(w1 == w2))
+
+    def test_scan_angle_rank(self):
+        """Writing and testing scan angle rank"""
+        ar1 = self.FileObject.scan_angle_rank
+        ar1[ar1 >= 1] -= 1
+        self.FileObject.scan_angle_rank = ar1
+        ar2 = self.FileObject.scan_angle_rank
+        self.assertTrue(np.all(ar1 == ar2))
+
+    def test_user_data(self):
+        """Writing and testing user data"""
+        ud1 = self.FileObject.user_data + 1
+        self.FileObject.user_data = ud1
+        ud2 = self.FileObject.user_data
+        self.assertTrue(np.all(ud1 == ud2))
+
+    def test_pt_src_id(self):
+        """Writing and testing point source id"""
+        p1 = self.FileObject.user_data + 1
+        self.FileObject.user_data = p1
+        p2 = self.FileObject.user_data
+        self.assertTrue(np.all(p1 == p2))
+
+    def test_gps_time(self):
+        """Writing and testing gps time"""
+        g1 = self.FileObject.gps_time + 1.0
+        self.FileObject.gps_time = g1
+        g2 = self.FileObject.gps_time
+        self.assertTrue(np.all(g1 == g2))
+
+    def test_red(self):
+        """Writing and testing red"""
+        r1 = self.FileObject.red + 1
+        self.FileObject.red = r1
+        r2 = self.FileObject.red
+        self.assertTrue(np.all(r1 == r2))
+
+    def test_green(self):
+        """Writing and testing green"""
+        g1 = self.FileObject.green + 1
+        self.FileObject.green = g1
+        g2 = self.FileObject.green
+        self.assertTrue(np.all(g1 == g2))
+
+    def test_blue(self):
+        """Writing and testing blue"""
+        b1 = self.FileObject.blue + 1
+        self.FileObject.blue = b1
+        b2 = self.FileObject.blue
+        self.assertTrue(np.all(b1 == b2))
+
+    # def test_vlr_defined_dimensions2(self):
+    #     """Testing VLR defined dimension API"""
+    #     File2 = File.File(self.output_tempfile, mode="w", header=self.FileObject.header)
+    #     File2.define_new_dimension("test_dimension", 5, "This is a test.")
+    #     File2.X = self.FileObject.X
+    #     self.assertTrue(File2.test_dimension[500] == 0)
+    #     File2.close(ignore_header_changes=True)
+
+    def tearDown(self):
+        self.FileObject.write(self.output_tempfile)
+        really_remove(self.output_tempfile)
+
+
+class LasHeaderWriterTestCase(unittest.TestCase):
+    simple = os.path.join(os.path.dirname(__file__), "data", "simple.las")
+    simple14 = os.path.join(os.path.dirname(__file__), "data", "simple1_4.las")
+    tempfile = os.path.abspath("headerwriter.las")
+    tempfile2 = os.path.abspath("headerwriter2.las")
+
+    def setUp(self):
+        self.las = laspy.read(self.simple)
+
+    def test_file_src(self):
+        """Testing file_src"""
+        f1 = self.las.header.file_source_id + 1
+        self.las.header.file_source_id = f1
+        f2 = self.las.header.file_source_id
+        assert f1 == f2
+
+    @pytest.mark.skip(reason="API changed")
+    def test_uuid(self):
+        """Testing uuid"""
+        guid = self.las.header.guid
+        guid2 = self.las.header.project_id
+        self.assertEqual(guid, guid2)
+        newGuid = UUID(bytes=b"1" * 16)
+        self.las.header.guid = newGuid
+        newGuid2 = self.las.header.get_guid()
+        self.assertEqual(newGuid, newGuid2)
+
+    def test_versions(self):
+        """Testing Versions"""
+        assert self.las.header.version.major == 1
+        with self.assertRaises(AttributeError):
+            self.las.header.version.major = 2
+
+    def test_system_id(self):
+        """Testing System ID"""
+        sys1 = self.las.header.system_identifier
+        sys1 = "1234567891" + sys1[10:]
+        self.las.header.system_identifier = sys1
+        sys2 = self.las.header.system_identifier
+        assert sys1 == sys2
+
+    def test_software_id(self):
+        """ "Testing Software ID"""
+        s1 = self.las.header.generating_software
+        s1 = "1234567" + s1[7:]
+        self.las.header.generating_software = s1
+        s2 = self.las.header.generating_software
+        assert s1 == s2
+        # with self.assertRaises(laspy.LaspyException):
+        #     self.las.header.generating_software = "123"
+        # with self.assertRaises(laspy.LaspyException):
+        #     self.las.header.generating_software = "1" * 100
+
+    def test_date(self):
+        """Testing Date"""
+        d1 = self.las.header.creation_date
+        assert d1 is None
+        from datetime import datetime
+
+        d2 = datetime(2007, 12, 10)
+        self.las.header.creation_date = d2
+        d3 = self.las.header.creation_date
+        self.assertEqual(d2, d3)
+
+    def test_point_recs_by_return(self):
+        """Testing point records by return"""
+        r1 = self.las.header.number_of_points_by_return + 1
+        self.las.header.number_of_points_by_return = r1
+        r2 = self.las.header.number_of_points_by_return
+        assert np.all(r1 == r2)
+
+    def test_min_max_update(self):
+        """Testing the update min/max function"""
+        x = self.las.X
+        x[0] = max(x) + 1
+        y = self.las.Y
+        y[0] = max(y) + 1
+        z = self.las.Z
+        z[0] = max(z) + 1
+        self.las.X = x
+        self.las.Y = y
+        self.las.Z = z
+        self.las.update_header()
+        file_max = self.las.header.maxs
+        assert np.all(file_max == [self.las.x[0], self.las.y[0], self.las.z[0]])
+
+    def test_histogram(self):
+        """Testing the update_histogram functon"""
+        h1 = self.las.header.number_of_points_by_return
+        self.las.update_header()
+        h2 = self.las.header.number_of_points_by_return
+        assert np.all(h1 == h2)
+
+    def test_offset(self):
+        """Testing offset"""
+        o1 = self.las.header.offsets
+        o1[0] += 1
+        self.las.header.offsets = o1
+        o2 = self.las.header.offsets
+        assert np.all(o1 == o2)
+
+    def test_scale(self):
+        """Testing Scale"""
+        s1 = self.las.header.scales
+        s1[0] += 1
+        self.las.header.scales = s1
+        s2 = self.las.header.scales
+        assert np.all(s1 == s2)
+
+
+class LasWriteModeTestCase(unittest.TestCase):
+    simple = os.path.join(os.path.dirname(__file__), "data", "simple.las")
+    tempfile = "write-mode.las"
+    output_tempfile = "write-mode-output.las"
+
+    def setUp(self):
+        self.File1 = laspy.read(self.simple)
+
+    def test_using_barebones_header(self):
+        """Testing file creation using barebones header"""
+        header = laspy.LasHeader()
+
+        File2 = laspy.LasData(header)
+
+        self.assertTrue(File2.header.version == "1.2")
+
+        X = self.File1.X
+        Y = self.File1.Y
+        Z = self.File1.Z
+        File2.X = X
+        File2.Y = Y
+        File2.Z = Z
+
+        File2.write(self.output_tempfile)
+        File2 = laspy.read(self.output_tempfile)
+
+        self.assertTrue(np.all(X == File2.X))
+        self.assertTrue(np.all(Y == File2.Y))
+        self.assertTrue(np.all(Z == File2.Z))
+
+    def test_using_existing_header(self):
+        """Test file creation using an existing header"""
+        File2 = laspy.LasData(self.File1.header)
+        X = self.File1.X
+        Y = self.File1.Y
+        Z = self.File1.Z
+        File2.X = X
+        File2.Y = Y
+        File2.Z = Z
+
+        File2.write(self.output_tempfile)
+        File2 = laspy.read(self.output_tempfile)
+
+        self.assertTrue(np.all(X == File2.X))
+        self.assertTrue(np.all(Y == File2.Y))
+        self.assertTrue(np.all(Z == File2.Z))
+
+    def tearDown(self):
+        really_remove(self.output_tempfile)
+
+
+class LasV_13TestCase(unittest.TestCase):
+    simple = os.path.join(os.path.dirname(__file__), "data", "simple1_3.las")
+    output_tempfile = "v13-output.las"
+
+    def setUp(self):
+        self.File1 = laspy.read(self.simple)
+
+    def test_glob_encode(self):
+        """Testing v1.3 Global Encoding"""
+        old = self.File1.header.global_encoding.gps_time_type
+        assert old == laspy.header.GpsTimeType.WEEK_TIME
+        self.File1.header.global_encoding.gps_time_type = (
+            laspy.header.GpsTimeType.STANDARD
+        )
+        assert (
+            self.File1.header.global_encoding.gps_time_type
+            == laspy.header.GpsTimeType.STANDARD
+        )
+
+        self.File1.header.global_encoding.gps_time_type = (
+            laspy.header.GpsTimeType.WEEK_TIME
+        )
+        assert (
+            self.File1.header.global_encoding.gps_time_type
+            == laspy.header.GpsTimeType.WEEK_TIME
+        )
+
+        File2 = laspy.LasData(self.File1.header)
+        File2.write(self.output_tempfile)
+        File2 = laspy.read(self.output_tempfile)
+
+        self.assertEqual(
+            self.File1.header.global_encoding.waveform_data_packets_internal,
+            File2.header.global_encoding.waveform_data_packets_internal,
+        )
+        self.assertEqual(
+            self.File1.header.global_encoding.waveform_data_packets_external,
+            File2.header.global_encoding.waveform_data_packets_external,
+        )
+        self.assertEqual(
+            self.File1.header.global_encoding.synthetic_return_numbers,
+            File2.header.global_encoding.synthetic_return_numbers,
+        )
+
+    def test_wave_packet_desc_index(self):
+        """Testing wave_packet_desc_index."""
+        test1 = self.File1.wave_packet_desc_index
+        File2 = laspy.LasData(self.File1.header)
+        File2.points = self.File1.points
+        assert np.all(test1 == File2.wave_packet_desc_index)
+
+    def test_byte_offset_to_waveform_data(self):
+        """Testing byte_offset_to_waveform_data"""
+        test1 = self.File1.byte_offset_to_waveform_data
+        File2 = laspy.LasData(self.File1.header)
+        File2.points = self.File1.points
+        assert np.all(test1 == File2.byte_offset_to_waveform_data)
+
+    def test_waveform_packet_size(self):
+        """Testing waveform_packet_size"""
+        test1 = self.File1.waveform_packet_size
+        File2 = laspy.LasData(self.File1.header)
+        File2.points = self.File1.points.copy()
+        assert np.all(test1 == File2.waveform_packet_size)
+
+    def test_return_point_waveform_loc(self):
+        """Testing return_point_waveform_loc"""
+        test1 = self.File1.return_point_waveform_loc
+        File2 = laspy.LasData(self.File1.header)
+        File2.points = self.File1.points.copy()
+        assert np.all(test1 == File2.return_point_waveform_loc)
+        File2.return_point_waveform_loc += 1
+        assert np.all(test1 != File2.return_point_waveform_loc)
+
+    def test_x_t(self):
+        """Testing x_t"""
+        test1 = self.File1.x_t
+        File2 = laspy.LasData(self.File1.header)
+        File2.points = self.File1.points.copy()
+        assert np.all(test1 == File2.x_t)
+        File2.x_t += 1
+        assert np.all(test1 != File2.x_t)
+
+    def test_y_t(self):
+        """Testing y_t"""
+        test1 = self.File1.y_t
+        File2 = laspy.LasData(self.File1.header)
+        File2.points = self.File1.points.copy()
+        np.all(test1 == File2.y_t)
+        File2.y_t += 1
+        assert np.all(test1 != File2.y_t)
+
+    def test_z_t(self):
+        """Testing z_t"""
+        test1 = self.File1.z_t
+        File2 = laspy.LasData(self.File1.header)
+        File2.points = self.File1.points.copy()
+        np.all(test1 == File2.z_t)
+        File2.z_t += 1
+        np.all(test1 != File2.z_t)
+
+    def tearDown(self):
+        really_remove(self.output_tempfile)
+
+
+class LasV_14TestCase(unittest.TestCase):
+    simple = os.path.join(os.path.dirname(__file__), "data", "simple1_4.las")
+    tempfile = "v14.las"
+    output_tempfile = "v14-output.las"
+
+    def setUp(self):
+        self.File1 = laspy.read(self.simple)
+
+    def test_glob_encode(self):
+        """Testing v1.4 Global Encoding"""
+        old = self.File1.header.global_encoding.gps_time_type
+        assert old == laspy.header.GpsTimeType.WEEK_TIME
+        self.File1.header.global_encoding.gps_time_type = (
+            laspy.header.GpsTimeType.STANDARD
+        )
+        assert (
+            self.File1.header.global_encoding.gps_time_type
+            == laspy.header.GpsTimeType.STANDARD
+        )
+
+        File2 = laspy.LasData(self.File1.header)
+        self.assertEqual(
+            self.File1.header.global_encoding.waveform_data_packets_internal,
+            File2.header.global_encoding.waveform_data_packets_internal,
+        )
+        self.assertEqual(
+            self.File1.header.global_encoding.waveform_data_packets_external,
+            File2.header.global_encoding.waveform_data_packets_external,
+        )
+        self.assertEqual(
+            self.File1.header.global_encoding.synthetic_return_numbers,
+            File2.header.global_encoding.synthetic_return_numbers,
+        )
+
+    def test_glob_encode_bits(self):
+        b1 = self.File1.header.global_encoding.gps_time_type
+        b2 = self.File1.header.global_encoding.waveform_data_packets_internal
+        b3 = self.File1.header.global_encoding.waveform_data_packets_external
+        b4 = self.File1.header.global_encoding.synthetic_return_numbers
+        b5 = self.File1.header.global_encoding.wkt
+
+        bf1 = 1 - int(b1)
+        bf2 = 1 - int(b2)
+        bf3 = 1 - int(b3)
+        bf4 = 1 - int(b4)
+        bf5 = 1 - int(b5)
+
+        self.File1.header.global_encoding.gps_time_type = bf1
+        self.File1.header.global_encoding.waveform_data_packets_internal = bf2
+        self.File1.header.global_encoding.waveform_data_packets_external = bf3
+        self.File1.header.global_encoding.synthetic_return_numbers = bf4
+        self.File1.header.global_encoding.wkt = bf5
+
+        assert self.File1.header.global_encoding.gps_time_type == bf1
+        assert self.File1.header.global_encoding.waveform_data_packets_internal == bf2
+        assert self.File1.header.global_encoding.waveform_data_packets_external == bf3
+        assert self.File1.header.global_encoding.synthetic_return_numbers == bf4
+        assert self.File1.header.global_encoding.wkt == bf5
+
+    def test_classification_variables(self):
+        """Testing v1.4 classification support"""
+        classification = self.File1.classification
+        classification_flags = self.File1.classification_flags
+        scanner_channel = self.File1.scanner_channel
+        scan_dir_flag = self.File1.scan_dir_flag
+        edge_flight_line = self.File1.edge_flight_line
+
+        return_num = self.File1.return_num
+        num_returns = self.File1.num_returns
+
+        File2 = laspy.LasData(self.File1.header)
+        File2.classification = classification
+        File2.classification_flags = classification_flags
+        File2.scan_dir_flag = scan_dir_flag
+        File2.scanner_channel = scanner_channel
+        File2.edge_flight_line = edge_flight_line
+        File2.return_num = return_num
+        File2.num_returns = num_returns
+
+        File2.write(self.output_tempfile)
+        File2 = laspy.read(self.output_tempfile)
+
+        assert np.all(num_returns == File2.num_returns)
+        assert np.all(return_num == File2.return_num)
+        assert np.all(edge_flight_line == File2.edge_flight_line)
+        assert np.all(scan_dir_flag == File2.scan_dir_flag)
+        assert np.all(classification_flags == File2.classification_flags)
+        assert np.all(classification == File2.classification)
+        assert np.all(scanner_channel == File2.scanner_channel)
+
+    def tearDown(self):
+        really_remove(self.output_tempfile)
+
+
+def really_remove(path, max_=1):
+    """
+    Hack for Windows when quickly creating and deleting files.
+    os.remove can return when Windows still thinks the file exists.
+    When trying to re-create the file with the same name, a PermissionError occurs.
+    :param path: path to remove
+    :param max_: max seconds to wait
+    """
+    wait = 0.01
+    while os.path.exists(path):
+        try:
+            os.remove(path)
+        except WindowsError:
+            time.sleep(wait)
+            max_ -= wait
+            if max_ <= 0:
+                break
```

### Comparing `laspy-2.4.1/tests/test_modif_1_2.py` & `laspy-2.5.0/tests/test_modif_1_2.py`

 * *Ordering differences only*

 * *Files 16% similar despite different names*

```diff
@@ -1,77 +1,77 @@
-import numpy as np
-import pytest
-
-import laspy
-from tests.test_common import (
-    do_compression,
-    simple_las,
-    simple_laz,
-    write_then_read_again,
-)
-
-
-@pytest.fixture(
-    params=[simple_las, simple_laz]
-    if laspy.LazBackend.detect_available()
-    else [simple_las]
-)
-def las(request):
-    return laspy.read(request.param)
-
-
-def test_classification_overflows(las):
-    c = las.classification
-    with pytest.raises(OverflowError):
-        c[0] = 54
-
-
-@pytest.mark.parametrize("do_compress", do_compression)
-def test_classification_change(las, do_compress):
-    c = las.classification
-    c[:] = 10
-
-    las.classification = c
-    assert np.allclose(c, las.classification)
-
-    las = write_then_read_again(las, do_compress=do_compress)
-    assert np.allclose(c, las.classification)
-
-
-@pytest.mark.parametrize("do_compress", do_compression)
-def test_synthetic_change(las, do_compress):
-    s = las.synthetic
-    s[:] = False
-    s[17] = True
-
-    las.synthetic = s
-    assert np.allclose(s, las.synthetic)
-    las = write_then_read_again(las, do_compress=do_compress)
-
-    assert np.allclose(s, las.synthetic)
-
-
-@pytest.mark.parametrize("do_compress", do_compression)
-def test_key_point_change(las, do_compress):
-    kp = las.key_point
-    kp[:] = False
-    kp[25] = True
-
-    las.key_point = kp
-    assert np.allclose(kp, las.key_point)
-
-    las = write_then_read_again(las, do_compress=do_compress)
-    assert np.allclose(kp, las.key_point)
-
-
-@pytest.mark.parametrize("do_compress", do_compression)
-def test_withheld_changes(las, do_compress):
-    withheld = las.withheld
-    withheld[:] = False
-    withheld[180] = True
-
-    las.withheld = withheld
-    assert np.allclose(withheld, las.withheld)
-
-    las = write_then_read_again(las, do_compress=do_compress)
-
-    assert np.allclose(withheld, las.withheld)
+import numpy as np
+import pytest
+
+import laspy
+from tests.test_common import (
+    do_compression,
+    simple_las,
+    simple_laz,
+    write_then_read_again,
+)
+
+
+@pytest.fixture(
+    params=[simple_las, simple_laz]
+    if laspy.LazBackend.detect_available()
+    else [simple_las]
+)
+def las(request):
+    return laspy.read(request.param)
+
+
+def test_classification_overflows(las):
+    c = las.classification
+    with pytest.raises(OverflowError):
+        c[0] = 54
+
+
+@pytest.mark.parametrize("do_compress", do_compression)
+def test_classification_change(las, do_compress):
+    c = las.classification
+    c[:] = 10
+
+    las.classification = c
+    assert np.allclose(c, las.classification)
+
+    las = write_then_read_again(las, do_compress=do_compress)
+    assert np.allclose(c, las.classification)
+
+
+@pytest.mark.parametrize("do_compress", do_compression)
+def test_synthetic_change(las, do_compress):
+    s = las.synthetic
+    s[:] = False
+    s[17] = True
+
+    las.synthetic = s
+    assert np.allclose(s, las.synthetic)
+    las = write_then_read_again(las, do_compress=do_compress)
+
+    assert np.allclose(s, las.synthetic)
+
+
+@pytest.mark.parametrize("do_compress", do_compression)
+def test_key_point_change(las, do_compress):
+    kp = las.key_point
+    kp[:] = False
+    kp[25] = True
+
+    las.key_point = kp
+    assert np.allclose(kp, las.key_point)
+
+    las = write_then_read_again(las, do_compress=do_compress)
+    assert np.allclose(kp, las.key_point)
+
+
+@pytest.mark.parametrize("do_compress", do_compression)
+def test_withheld_changes(las, do_compress):
+    withheld = las.withheld
+    withheld[:] = False
+    withheld[180] = True
+
+    las.withheld = withheld
+    assert np.allclose(withheld, las.withheld)
+
+    las = write_then_read_again(las, do_compress=do_compress)
+
+    assert np.allclose(withheld, las.withheld)
```

### Comparing `laspy-2.4.1/tests/test_modif_1_4.py` & `laspy-2.5.0/tests/test_modif_1_4.py`

 * *Ordering differences only*

 * *Files 19% similar despite different names*

```diff
@@ -1,65 +1,65 @@
-import numpy as np
-import pytest
-
-import laspy
-from laspy import LazBackend
-from tests.test_common import test1_4_las, write_then_read_again
-
-
-@pytest.fixture(scope="session")
-def las():
-    return laspy.read(test1_4_las)
-
-
-@pytest.fixture(params=LazBackend.detect_available())
-def laz_backend(request):
-    return request.param
-
-
-def test_classification(las):
-    las.classification[:] = 234
-    assert np.alltrue(las.classification == 234)
-
-    res = write_then_read_again(las)
-
-    assert np.alltrue(las.classification == res.classification)
-
-
-def test_intensity(las):
-    las.intensity[:] = 89
-    assert np.alltrue(las.intensity == 89)
-    res = write_then_read_again(las)
-
-    assert np.alltrue(las.intensity == res.intensity)
-
-
-def test_writing_las_with_evlrs():
-    las = laspy.read(test1_4_las)
-    assert las.evlrs == []
-
-    evlr = laspy.VLR(
-        user_id="test",
-        record_id=42,
-        description="Just a test",
-        record_data=b"And so he grinds his own hands",
-    )
-    las.evlrs.append(evlr)
-
-    las_1 = write_then_read_again(las, do_compress=False)
-    assert las_1.evlrs == [evlr]
-
-
-def test_writing_laz_with_evlrs(laz_backend):
-    las = laspy.read(test1_4_las)
-    assert las.evlrs == []
-
-    evlr = laspy.VLR(
-        user_id="test",
-        record_id=42,
-        description="Just a test",
-        record_data=b"And so he grinds he own hands",
-    )
-    las.evlrs.append(evlr)
-
-    las_1 = write_then_read_again(las, do_compress=True, laz_backend=laz_backend)
-    assert las_1.evlrs == [evlr]
+import numpy as np
+import pytest
+
+import laspy
+from laspy import LazBackend
+from tests.test_common import test1_4_las, write_then_read_again
+
+
+@pytest.fixture(scope="session")
+def las():
+    return laspy.read(test1_4_las)
+
+
+@pytest.fixture(params=LazBackend.detect_available())
+def laz_backend(request):
+    return request.param
+
+
+def test_classification(las):
+    las.classification[:] = 234
+    assert np.alltrue(las.classification == 234)
+
+    res = write_then_read_again(las)
+
+    assert np.alltrue(las.classification == res.classification)
+
+
+def test_intensity(las):
+    las.intensity[:] = 89
+    assert np.alltrue(las.intensity == 89)
+    res = write_then_read_again(las)
+
+    assert np.alltrue(las.intensity == res.intensity)
+
+
+def test_writing_las_with_evlrs():
+    las = laspy.read(test1_4_las)
+    assert las.evlrs == []
+
+    evlr = laspy.VLR(
+        user_id="test",
+        record_id=42,
+        description="Just a test",
+        record_data=b"And so he grinds his own hands",
+    )
+    las.evlrs.append(evlr)
+
+    las_1 = write_then_read_again(las, do_compress=False)
+    assert las_1.evlrs == [evlr]
+
+
+def test_writing_laz_with_evlrs(laz_backend):
+    las = laspy.read(test1_4_las)
+    assert las.evlrs == []
+
+    evlr = laspy.VLR(
+        user_id="test",
+        record_id=42,
+        description="Just a test",
+        record_data=b"And so he grinds he own hands",
+    )
+    las.evlrs.append(evlr)
+
+    las_1 = write_then_read_again(las, do_compress=True, laz_backend=laz_backend)
+    assert las_1.evlrs == [evlr]
```

### Comparing `laspy-2.4.1/tests/test_reading_1_2.py` & `laspy-2.5.0/tests/test_reading_1_2.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,228 +1,225 @@
-import io
-import os
-
-import numpy as np
-import pytest
-
-import laspy
-from tests.test_common import (
-    simple_las,
-    simple_laz,
-)
-
-
-@pytest.fixture(
-    params=[simple_las, simple_laz]
-    if laspy.LazBackend.detect_available()
-    else [simple_las],
-    scope="session",
-)
-def read_simple(request):
-    return laspy.read(request.param)
-
-
-@pytest.fixture()
-def open_simple():
-    return open(simple_las, mode="rb")
-
-
-@pytest.fixture()
-def read_uncompressed():
-    return laspy.read(simple_laz)
-
-
-@pytest.fixture()
-def get_header():
-    with laspy.open(simple_las) as fin:
-        return fin.header
-
-
-def test_header(get_header):
-    header = get_header
-    assert header.file_source_id == 0
-    assert header.version.major == 1
-    assert header.version.minor == 2
-    assert header.system_identifier == ""
-    assert header.generating_software == "TerraScan"
-    assert header.creation_date is None
-    assert header.offset_to_point_data == 227
-    assert len(header.vlrs) == 0
-    assert header.point_format.id == 3
-    assert header.point_format.size == 34
-    assert header.point_count == 1065
-    assert tuple(header.number_of_points_by_return[:5]) == (925, 114, 21, 5, 0)
-    assert header.x_scale == 0.01
-    assert header.y_scale == 0.01
-    assert header.z_scale == 0.01
-    assert header.x_offset == 0
-    assert header.y_offset == 0
-    assert header.z_offset == 0
-    assert header.x_max == pytest.approx(638982.55)
-    assert header.x_min == pytest.approx(635619.85)
-    assert header.y_max == pytest.approx(853535.43)
-    assert header.y_min == pytest.approx(848899.70)
-    assert header.z_max == pytest.approx(586.38)
-    assert header.z_min == pytest.approx(406.59)
-
-
-def test_no_vlr_for_simple(read_simple):
-    f = read_simple
-    assert f.vlrs == []
-
-
-def test_every_byte_has_been_read(open_simple):
-    fp = open_simple
-    _ = laspy.read(fp, closefd=False)
-    assert fp.tell() == os.path.getsize(simple_las)
-    fp.close()
-
-
-def test_unscaled_x(read_simple):
-    f = read_simple
-    assert f.X.max() == 63898255
-    assert f.X.min() == 63561985
-
-
-def test_unscaled_y(read_simple):
-    f = read_simple
-    assert f.Y.max() == 85353543
-    assert f.Y.min() == 84889970
-
-
-def test_unscaled_z(read_simple):
-    f = read_simple
-    assert f.Z.max() == 58638
-    assert f.Z.min() == 40659
-
-
-def test_intensity(read_simple):
-    f = read_simple
-    assert f.intensity.max() == 254
-    assert f.intensity.min() == 0
-
-
-def test_return_number(read_simple):
-    f = read_simple
-    assert f.return_number.max() == 4
-    assert f.return_number.min() == 1
-
-
-def test_number_of_returns(read_simple):
-    f = read_simple
-    assert f.number_of_returns.max() == 4
-    assert f.number_of_returns.min() == 1
-
-
-def test_edge_of_flight_line(read_simple):
-    f = read_simple
-    assert f.edge_of_flight_line.max() == 0
-    assert f.edge_of_flight_line.min() == 0
-
-
-def test_scan_direction_flag(read_simple):
-    f = read_simple
-    assert f.scan_direction_flag.max() == 1
-    assert f.scan_direction_flag.min() == 0
-
-
-def test_scan_angle_rank(read_simple):
-    f = read_simple
-    assert f.scan_angle_rank.max() == 18
-    assert f.scan_angle_rank.min() == -19
-
-
-def test_classification_max_min(read_simple):
-    f = read_simple
-    assert f.classification.max() == 2
-    assert f.classification.min() == 1
-
-
-def test_classification_count(read_simple):
-    f = read_simple
-    uniques, counts = np.unique(f.classification, return_counts=True)
-    assert np.all(uniques == [1, 2])
-    assert counts[0] == 789  # class code 1
-    assert counts[1] == 276  # class code 2
-
-
-def test_user_data(read_simple):
-    f = read_simple
-    assert f.user_data.max() == 149
-    assert f.user_data.min() == 117
-
-
-def test_point_source_id(read_simple):
-    f = read_simple
-    assert f.point_source_id.max() == 7334
-    assert f.point_source_id.min() == 7326
-
-
-def test_gps_time(read_simple):
-    f = read_simple
-    assert f.gps_time.max() == pytest.approx(249783.162158)
-    assert f.gps_time.min() == pytest.approx(245370.417075)
-
-
-def test_red(read_simple):
-    f = read_simple
-    assert f.red.max() == 249
-    assert f.red.min() == 39
-
-
-def test_green(read_simple):
-    f = read_simple
-    assert f.green.max() == 239
-    assert f.green.min() == 57
-
-
-def test_blue(read_simple):
-    f = read_simple
-    assert f.blue.max() == 249
-    assert f.blue.min() == 56
-
-
-@pytest.mark.skipif(
-    len(laspy.LazBackend.detect_available()) == 0, reason="No Laz Backend installed"
-)
-def test_decompression_is_same_as_uncompressed():
-    u_las = laspy.read(simple_las)
-    c_las = laspy.read(simple_laz)
-
-    u_point_buffer = bytes(u_las.points.memoryview())
-    c_points_buffer = bytes(c_las.points.memoryview())
-
-    assert u_point_buffer == c_points_buffer
-
-
-def check_seeking_works(las_reader: laspy.LasReader):
-    p1 = las_reader.read_points(10)
-
-    idx = las_reader.seek(5)
-    assert idx == 5
-
-    p2 = las_reader.read_points(5)
-    assert p1[5:] == p2
-
-    idx = las_reader.seek(-5, io.SEEK_CUR)
-    assert idx == 5
-    p2 = las_reader.read_points(5)
-    assert p1[5:] == p2
-
-    rest = las_reader.read_points(-1)
-    assert len(rest) == las_reader.header.point_count - 10
-
-    idx = las_reader.seek(-150, io.SEEK_END)
-    assert idx == las_reader.header.point_count - 150
-    p2 = las_reader.read_points(-1)
-    assert p2 == rest[-150:]
-
-
-def test_seek_las(las_file_path):
-    with laspy.open(las_file_path) as reader:
-        check_seeking_works(reader)
-
-
-@pytest.mark.parametrize("laz_backend", laspy.LazBackend.detect_available())
-def test_seek_laz(laz_file_path, laz_backend):
-    with laspy.open(laz_file_path, laz_backend=laz_backend) as reader:
-        check_seeking_works(reader)
+import io
+import os
+
+import numpy as np
+import pytest
+
+import laspy
+from tests.test_common import simple_las, simple_laz
+
+
+@pytest.fixture(
+    params=[simple_las, simple_laz]
+    if laspy.LazBackend.detect_available()
+    else [simple_las],
+    scope="session",
+)
+def read_simple(request):
+    return laspy.read(request.param)
+
+
+@pytest.fixture()
+def open_simple():
+    return open(simple_las, mode="rb")
+
+
+@pytest.fixture()
+def read_uncompressed():
+    return laspy.read(simple_laz)
+
+
+@pytest.fixture()
+def get_header():
+    with laspy.open(simple_las) as fin:
+        return fin.header
+
+
+def test_header(get_header):
+    header = get_header
+    assert header.file_source_id == 0
+    assert header.version.major == 1
+    assert header.version.minor == 2
+    assert header.system_identifier == ""
+    assert header.generating_software == "TerraScan"
+    assert header.creation_date is None
+    assert header.offset_to_point_data == 227
+    assert len(header.vlrs) == 0
+    assert header.point_format.id == 3
+    assert header.point_format.size == 34
+    assert header.point_count == 1065
+    assert tuple(header.number_of_points_by_return[:5]) == (925, 114, 21, 5, 0)
+    assert header.x_scale == 0.01
+    assert header.y_scale == 0.01
+    assert header.z_scale == 0.01
+    assert header.x_offset == 0
+    assert header.y_offset == 0
+    assert header.z_offset == 0
+    assert header.x_max == pytest.approx(638982.55)
+    assert header.x_min == pytest.approx(635619.85)
+    assert header.y_max == pytest.approx(853535.43)
+    assert header.y_min == pytest.approx(848899.70)
+    assert header.z_max == pytest.approx(586.38)
+    assert header.z_min == pytest.approx(406.59)
+
+
+def test_no_vlr_for_simple(read_simple):
+    f = read_simple
+    assert f.vlrs == []
+
+
+def test_every_byte_has_been_read(open_simple):
+    fp = open_simple
+    _ = laspy.read(fp, closefd=False)
+    assert fp.tell() == os.path.getsize(simple_las)
+    fp.close()
+
+
+def test_unscaled_x(read_simple):
+    f = read_simple
+    assert f.X.max() == 63898255
+    assert f.X.min() == 63561985
+
+
+def test_unscaled_y(read_simple):
+    f = read_simple
+    assert f.Y.max() == 85353543
+    assert f.Y.min() == 84889970
+
+
+def test_unscaled_z(read_simple):
+    f = read_simple
+    assert f.Z.max() == 58638
+    assert f.Z.min() == 40659
+
+
+def test_intensity(read_simple):
+    f = read_simple
+    assert f.intensity.max() == 254
+    assert f.intensity.min() == 0
+
+
+def test_return_number(read_simple):
+    f = read_simple
+    assert f.return_number.max() == 4
+    assert f.return_number.min() == 1
+
+
+def test_number_of_returns(read_simple):
+    f = read_simple
+    assert f.number_of_returns.max() == 4
+    assert f.number_of_returns.min() == 1
+
+
+def test_edge_of_flight_line(read_simple):
+    f = read_simple
+    assert f.edge_of_flight_line.max() == 0
+    assert f.edge_of_flight_line.min() == 0
+
+
+def test_scan_direction_flag(read_simple):
+    f = read_simple
+    assert f.scan_direction_flag.max() == 1
+    assert f.scan_direction_flag.min() == 0
+
+
+def test_scan_angle_rank(read_simple):
+    f = read_simple
+    assert f.scan_angle_rank.max() == 18
+    assert f.scan_angle_rank.min() == -19
+
+
+def test_classification_max_min(read_simple):
+    f = read_simple
+    assert f.classification.max() == 2
+    assert f.classification.min() == 1
+
+
+def test_classification_count(read_simple):
+    f = read_simple
+    uniques, counts = np.unique(f.classification, return_counts=True)
+    assert np.all(uniques == [1, 2])
+    assert counts[0] == 789  # class code 1
+    assert counts[1] == 276  # class code 2
+
+
+def test_user_data(read_simple):
+    f = read_simple
+    assert f.user_data.max() == 149
+    assert f.user_data.min() == 117
+
+
+def test_point_source_id(read_simple):
+    f = read_simple
+    assert f.point_source_id.max() == 7334
+    assert f.point_source_id.min() == 7326
+
+
+def test_gps_time(read_simple):
+    f = read_simple
+    assert f.gps_time.max() == pytest.approx(249783.162158)
+    assert f.gps_time.min() == pytest.approx(245370.417075)
+
+
+def test_red(read_simple):
+    f = read_simple
+    assert f.red.max() == 249
+    assert f.red.min() == 39
+
+
+def test_green(read_simple):
+    f = read_simple
+    assert f.green.max() == 239
+    assert f.green.min() == 57
+
+
+def test_blue(read_simple):
+    f = read_simple
+    assert f.blue.max() == 249
+    assert f.blue.min() == 56
+
+
+@pytest.mark.skipif(
+    len(laspy.LazBackend.detect_available()) == 0, reason="No Laz Backend installed"
+)
+def test_decompression_is_same_as_uncompressed():
+    u_las = laspy.read(simple_las)
+    c_las = laspy.read(simple_laz)
+
+    u_point_buffer = bytes(u_las.points.memoryview())
+    c_points_buffer = bytes(c_las.points.memoryview())
+
+    assert u_point_buffer == c_points_buffer
+
+
+def check_seeking_works(las_reader: laspy.LasReader):
+    p1 = las_reader.read_points(10)
+
+    idx = las_reader.seek(5)
+    assert idx == 5
+
+    p2 = las_reader.read_points(5)
+    assert p1[5:] == p2
+
+    idx = las_reader.seek(-5, io.SEEK_CUR)
+    assert idx == 5
+    p2 = las_reader.read_points(5)
+    assert p1[5:] == p2
+
+    rest = las_reader.read_points(-1)
+    assert len(rest) == las_reader.header.point_count - 10
+
+    idx = las_reader.seek(-150, io.SEEK_END)
+    assert idx == las_reader.header.point_count - 150
+    p2 = las_reader.read_points(-1)
+    assert p2 == rest[-150:]
+
+
+def test_seek_las(las_file_path):
+    with laspy.open(las_file_path) as reader:
+        check_seeking_works(reader)
+
+
+@pytest.mark.parametrize("laz_backend", laspy.LazBackend.detect_available())
+def test_seek_laz(laz_file_path, laz_backend):
+    with laspy.open(laz_file_path, laz_backend=laz_backend) as reader:
+        check_seeking_works(reader)
```

### Comparing `laspy-2.4.1/tests/test_reading_1_4.py` & `laspy-2.5.0/tests/test_reading_1_4.py`

 * *Ordering differences only*

 * *Files 23% similar despite different names*

```diff
@@ -1,252 +1,252 @@
-from pathlib import Path
-
-import numpy as np
-import pytest
-import os
-
-import laspy
-from laspy import LazBackend
-from tests.test_common import test1_4_las
-
-
-@pytest.fixture()
-def file():
-    return laspy.read(test1_4_las)
-
-
-def test_unscaled_x(file):
-    assert file.X.max() == 1751224820
-    assert file.X.min() == 1320803567
-
-
-def test_unscaled_y(file):
-    assert file.Y.max() == -860121188
-    assert file.Y.min() == -864646690
-
-
-def test_unscaled_z(file):
-    assert file.Z.max() == -1745638014
-    assert file.Z.min() == -1751937981
-
-
-def test_intensity(file):
-    assert file.intensity.max() == 68
-    assert file.intensity.min() == 2
-
-
-def test_return_number(file):
-    assert file.return_number.max() == 4
-    assert file.return_number.min() == 1
-
-
-def test_number_of_returns(file):
-    assert file.number_of_returns.max() == 4
-    assert file.number_of_returns.min() == 1
-
-
-def test_edge_of_flight_line(file):
-    assert file.edge_of_flight_line.max() == 1
-    assert file.edge_of_flight_line.min() == 0
-
-
-def scan_direction_flag(file):
-    assert file.scan_direction_flag.max() == 1
-    assert file.scan_direction_flag.min() == 0
-
-
-def test_classification(file):
-    assert file.classification.max() == 2
-    assert file.classification.min() == 2
-
-
-def test_scan_angle_rank(file):
-    assert file.scan_angle.max() == 3173
-    assert file.scan_angle.min() == 1837
-
-
-def test_user_data(file):
-    assert file.user_data.max() == 0
-    assert file.user_data.min() == 0
-
-
-def test_point_source_id(file):
-    assert file.point_source_id.max() == 202
-    assert file.point_source_id.min() == 202
-
-
-def test_gps_time(file):
-    assert file.gps_time.max() == pytest.approx(83177420.601045)
-    assert file.gps_time.min() == pytest.approx(83177420.534005)
-
-
-def test_scanner_channel(file):
-    assert file.scanner_channel.max() == 0
-    assert file.scanner_channel.min() == 0
-
-
-def test_we_read_evlrs_when_simply_opening():
-    file_with_evlrs = os.path.dirname(__file__) + "/data/1_4_w_evlr.las"
-    expected_evlrs = laspy.VLR(
-        user_id="pylastest",
-        record_id=42,
-        description="just a test evlr",
-        record_data=b"Test 1 2 ... 1 2",
-    )
-    with laspy.open(file_with_evlrs) as reader:
-        assert reader.evlrs == [expected_evlrs]
-
-
-def test_we_dont_read_evlrs_when_opening_if_user_does_not_want():
-    file_with_evlrs = os.path.dirname(__file__) + "/data/1_4_w_evlr.las"
-    with laspy.open(file_with_evlrs, read_evlrs=False) as reader:
-        assert reader.evlrs is None
-
-
-def test_reader_read_reads_evlrs_even_if_skipped_at_opening():
-    file_with_evlrs = os.path.dirname(__file__) + "/data/1_4_w_evlr.las"
-    expected_evlrs = [
-        laspy.VLR(
-            user_id="pylastest",
-            record_id=42,
-            description="just a test evlr",
-            record_data=b"Test 1 2 ... 1 2",
-        )
-    ]
-    with laspy.open(file_with_evlrs, read_evlrs=False) as reader:
-        assert reader.evlrs is None
-        las = reader.read()
-        assert las.evlrs == expected_evlrs
-        assert reader.evlrs == expected_evlrs
-
-
-@pytest.mark.parametrize(
-    "file,backend",
-    [
-        ("/data/1_4_w_evlr.las", None),
-        pytest.param(
-            "/data/1_4_w_evlr.laz",
-            LazBackend.Laszip,
-            marks=pytest.mark.skipif(
-                not LazBackend.Laszip.is_available(), reason="laszip is not installed"
-            ),
-        ),
-        pytest.param(
-            "/data/1_4_w_evlr.laz",
-            LazBackend.Lazrs,
-            marks=pytest.mark.skipif(
-                not LazBackend.Lazrs.is_available(), reason="lazrs is not installed"
-            ),
-        ),
-        pytest.param(
-            "/data/1_4_w_evlr.laz",
-            LazBackend.LazrsParallel,
-            marks=pytest.mark.skipif(
-                not LazBackend.LazrsParallel.is_available(),
-                reason="lazrs is not installed",
-            ),
-        ),
-    ],
-)
-def test_manually_reading_evlrs(file, backend):
-    # The goal is to test we can read evlrs
-    # in between reading points, as reading evlrs
-    # will require to seek to them, so this is to make sure
-    # we correctly reseek to the previous position
-    # and that we can continue to read points
-
-    file_with_evlrs = os.path.dirname(__file__) + file
-    expected_evlrs = [
-        laspy.VLR(
-            user_id="pylastest",
-            record_id=42,
-            description="just a test evlr",
-            record_data=b"Test 1 2 ... 1 2",
-        )
-    ]
-
-    expected_points = laspy.read(file_with_evlrs, laz_backend=backend).points
-
-    with laspy.open(file_with_evlrs, read_evlrs=False, laz_backend=backend) as reader:
-        points = laspy.ScaleAwarePointRecord.empty(header=reader.header)
-
-        assert reader.evlrs is None
-
-        chunk_size = 100
-
-        iter = reader.chunk_iterator(chunk_size)
-        chunk1 = next(iter)
-        assert np.alltrue(chunk1 == expected_points[:chunk_size])
-
-        reader.read_evlrs()
-        assert reader.evlrs == expected_evlrs
-
-        for i, chunk in enumerate(iter):
-            assert np.alltrue(
-                chunk == expected_points[(i + 1) * chunk_size : (i + 2) * chunk_size]
-            )
-
-
-@pytest.mark.parametrize(
-    "backend",
-    [
-        pytest.param(
-            laspy.LazBackend.Laszip,
-            marks=pytest.mark.skipif(
-                not laspy.LazBackend.Laszip.is_available(),
-                reason="Laszip not installed",
-            ),
-        ),
-        pytest.param(
-            laspy.LazBackend.Lazrs,
-            marks=pytest.mark.skipif(
-                not laspy.LazBackend.Lazrs.is_available(), reason="lazrs not installed"
-            ),
-        ),
-        pytest.param(
-            laspy.LazBackend.LazrsParallel,
-            marks=pytest.mark.skipif(
-                not laspy.LazBackend.Lazrs.is_available(), reason="lazrs not installed"
-            ),
-        ),
-    ],
-)
-def test_selective_decompression(backend):
-    # We only decompress X,Y, return number, number of returns, intensity
-    selection = laspy.DecompressionSelection.base().decompress_intensity()
-
-    simple1_4 = Path(__file__).parent / "data" / "1_4_w_evlr.laz"
-
-    fully_decompressed_laz = laspy.read(simple1_4, laz_backend=backend)
-    partially_decompressed_laz = laspy.read(
-        simple1_4, laz_backend=backend, decompression_selection=selection
-    )
-
-    assert fully_decompressed_laz.point_format.id >= 6
-
-    assert np.all(fully_decompressed_laz.X == partially_decompressed_laz.X)
-    assert np.all(fully_decompressed_laz.Y == partially_decompressed_laz.Y)
-    assert np.all(
-        fully_decompressed_laz.return_number == partially_decompressed_laz.return_number
-    )
-    assert np.all(
-        fully_decompressed_laz.number_of_returns
-        == partially_decompressed_laz.number_of_returns
-    )
-    assert np.all(
-        fully_decompressed_laz.intensity == partially_decompressed_laz.intensity
-    )
-
-    # This is the chunk size of the chunks inside the .laz
-    chunk_size = 50_000
-    # In selective decompression, the bytes which are not decompressed are set to the value
-    # of the first point of the LAZ chunk
-    for i in range((len(fully_decompressed_laz) // chunk_size) + 1):
-        start, end = i, (i + 1) * chunk_size
-        assert np.all(
-            # 12
-            fully_decompressed_laz.classification[start]
-            == partially_decompressed_laz.classification[start:end]
-        )
-        assert np.all(
-            fully_decompressed_laz.Z[start] == partially_decompressed_laz.Z[start:end]
-        )
+import os
+from pathlib import Path
+
+import numpy as np
+import pytest
+
+import laspy
+from laspy import LazBackend
+from tests.test_common import test1_4_las
+
+
+@pytest.fixture()
+def file():
+    return laspy.read(test1_4_las)
+
+
+def test_unscaled_x(file):
+    assert file.X.max() == 1751224820
+    assert file.X.min() == 1320803567
+
+
+def test_unscaled_y(file):
+    assert file.Y.max() == -860121188
+    assert file.Y.min() == -864646690
+
+
+def test_unscaled_z(file):
+    assert file.Z.max() == -1745638014
+    assert file.Z.min() == -1751937981
+
+
+def test_intensity(file):
+    assert file.intensity.max() == 68
+    assert file.intensity.min() == 2
+
+
+def test_return_number(file):
+    assert file.return_number.max() == 4
+    assert file.return_number.min() == 1
+
+
+def test_number_of_returns(file):
+    assert file.number_of_returns.max() == 4
+    assert file.number_of_returns.min() == 1
+
+
+def test_edge_of_flight_line(file):
+    assert file.edge_of_flight_line.max() == 1
+    assert file.edge_of_flight_line.min() == 0
+
+
+def scan_direction_flag(file):
+    assert file.scan_direction_flag.max() == 1
+    assert file.scan_direction_flag.min() == 0
+
+
+def test_classification(file):
+    assert file.classification.max() == 2
+    assert file.classification.min() == 2
+
+
+def test_scan_angle_rank(file):
+    assert file.scan_angle.max() == 3173
+    assert file.scan_angle.min() == 1837
+
+
+def test_user_data(file):
+    assert file.user_data.max() == 0
+    assert file.user_data.min() == 0
+
+
+def test_point_source_id(file):
+    assert file.point_source_id.max() == 202
+    assert file.point_source_id.min() == 202
+
+
+def test_gps_time(file):
+    assert file.gps_time.max() == pytest.approx(83177420.601045)
+    assert file.gps_time.min() == pytest.approx(83177420.534005)
+
+
+def test_scanner_channel(file):
+    assert file.scanner_channel.max() == 0
+    assert file.scanner_channel.min() == 0
+
+
+def test_we_read_evlrs_when_simply_opening():
+    file_with_evlrs = os.path.dirname(__file__) + "/data/1_4_w_evlr.las"
+    expected_evlrs = laspy.VLR(
+        user_id="pylastest",
+        record_id=42,
+        description="just a test evlr",
+        record_data=b"Test 1 2 ... 1 2",
+    )
+    with laspy.open(file_with_evlrs) as reader:
+        assert reader.evlrs == [expected_evlrs]
+
+
+def test_we_dont_read_evlrs_when_opening_if_user_does_not_want():
+    file_with_evlrs = os.path.dirname(__file__) + "/data/1_4_w_evlr.las"
+    with laspy.open(file_with_evlrs, read_evlrs=False) as reader:
+        assert reader.evlrs is None
+
+
+def test_reader_read_reads_evlrs_even_if_skipped_at_opening():
+    file_with_evlrs = os.path.dirname(__file__) + "/data/1_4_w_evlr.las"
+    expected_evlrs = [
+        laspy.VLR(
+            user_id="pylastest",
+            record_id=42,
+            description="just a test evlr",
+            record_data=b"Test 1 2 ... 1 2",
+        )
+    ]
+    with laspy.open(file_with_evlrs, read_evlrs=False) as reader:
+        assert reader.evlrs is None
+        las = reader.read()
+        assert las.evlrs == expected_evlrs
+        assert reader.evlrs == expected_evlrs
+
+
+@pytest.mark.parametrize(
+    "file,backend",
+    [
+        ("/data/1_4_w_evlr.las", None),
+        pytest.param(
+            "/data/1_4_w_evlr.laz",
+            LazBackend.Laszip,
+            marks=pytest.mark.skipif(
+                not LazBackend.Laszip.is_available(), reason="laszip is not installed"
+            ),
+        ),
+        pytest.param(
+            "/data/1_4_w_evlr.laz",
+            LazBackend.Lazrs,
+            marks=pytest.mark.skipif(
+                not LazBackend.Lazrs.is_available(), reason="lazrs is not installed"
+            ),
+        ),
+        pytest.param(
+            "/data/1_4_w_evlr.laz",
+            LazBackend.LazrsParallel,
+            marks=pytest.mark.skipif(
+                not LazBackend.LazrsParallel.is_available(),
+                reason="lazrs is not installed",
+            ),
+        ),
+    ],
+)
+def test_manually_reading_evlrs(file, backend):
+    # The goal is to test we can read evlrs
+    # in between reading points, as reading evlrs
+    # will require to seek to them, so this is to make sure
+    # we correctly reseek to the previous position
+    # and that we can continue to read points
+
+    file_with_evlrs = os.path.dirname(__file__) + file
+    expected_evlrs = [
+        laspy.VLR(
+            user_id="pylastest",
+            record_id=42,
+            description="just a test evlr",
+            record_data=b"Test 1 2 ... 1 2",
+        )
+    ]
+
+    expected_points = laspy.read(file_with_evlrs, laz_backend=backend).points
+
+    with laspy.open(file_with_evlrs, read_evlrs=False, laz_backend=backend) as reader:
+        points = laspy.ScaleAwarePointRecord.empty(header=reader.header)
+
+        assert reader.evlrs is None
+
+        chunk_size = 100
+
+        iter = reader.chunk_iterator(chunk_size)
+        chunk1 = next(iter)
+        assert np.alltrue(chunk1 == expected_points[:chunk_size])
+
+        reader.read_evlrs()
+        assert reader.evlrs == expected_evlrs
+
+        for i, chunk in enumerate(iter):
+            assert np.alltrue(
+                chunk == expected_points[(i + 1) * chunk_size : (i + 2) * chunk_size]
+            )
+
+
+@pytest.mark.parametrize(
+    "backend",
+    [
+        pytest.param(
+            laspy.LazBackend.Laszip,
+            marks=pytest.mark.skipif(
+                not laspy.LazBackend.Laszip.is_available(),
+                reason="Laszip not installed",
+            ),
+        ),
+        pytest.param(
+            laspy.LazBackend.Lazrs,
+            marks=pytest.mark.skipif(
+                not laspy.LazBackend.Lazrs.is_available(), reason="lazrs not installed"
+            ),
+        ),
+        pytest.param(
+            laspy.LazBackend.LazrsParallel,
+            marks=pytest.mark.skipif(
+                not laspy.LazBackend.Lazrs.is_available(), reason="lazrs not installed"
+            ),
+        ),
+    ],
+)
+def test_selective_decompression(backend):
+    # We only decompress X,Y, return number, number of returns, intensity
+    selection = laspy.DecompressionSelection.base().decompress_intensity()
+
+    simple1_4 = Path(__file__).parent / "data" / "1_4_w_evlr.laz"
+
+    fully_decompressed_laz = laspy.read(simple1_4, laz_backend=backend)
+    partially_decompressed_laz = laspy.read(
+        simple1_4, laz_backend=backend, decompression_selection=selection
+    )
+
+    assert fully_decompressed_laz.point_format.id >= 6
+
+    assert np.all(fully_decompressed_laz.X == partially_decompressed_laz.X)
+    assert np.all(fully_decompressed_laz.Y == partially_decompressed_laz.Y)
+    assert np.all(
+        fully_decompressed_laz.return_number == partially_decompressed_laz.return_number
+    )
+    assert np.all(
+        fully_decompressed_laz.number_of_returns
+        == partially_decompressed_laz.number_of_returns
+    )
+    assert np.all(
+        fully_decompressed_laz.intensity == partially_decompressed_laz.intensity
+    )
+
+    # This is the chunk size of the chunks inside the .laz
+    chunk_size = 50_000
+    # In selective decompression, the bytes which are not decompressed are set to the value
+    # of the first point of the LAZ chunk
+    for i in range((len(fully_decompressed_laz) // chunk_size) + 1):
+        start, end = i, (i + 1) * chunk_size
+        assert np.all(
+            # 12
+            fully_decompressed_laz.classification[start]
+            == partially_decompressed_laz.classification[start:end]
+        )
+        assert np.all(
+            fully_decompressed_laz.Z[start] == partially_decompressed_laz.Z[start:end]
+        )
```

### Comparing `laspy-2.4.1/tests/test_vlrs.py` & `laspy-2.5.0/tests/test_vlrs.py`

 * *Ordering differences only*

 * *Files 13% similar despite different names*

```diff
@@ -1,74 +1,74 @@
-import io
-from pathlib import Path
-
-import pytest
-
-import laspy
-from tests import test_common
-
-
-def test_adding_classification_lookup():
-    simple = laspy.read(test_common.simple_las)
-    classification_lookup = laspy.vlrs.known.ClassificationLookupVlr()
-
-    assert len(classification_lookup.lookups) == 0
-    classification_lookup[20] = "computer"
-    assert len(classification_lookup.lookups) == 1
-    classification_lookup[17] = "car"
-
-    simple.vlrs.append(classification_lookup)
-
-    simple = test_common.write_then_read_again(simple)
-    classification_lookups = simple.vlrs.get("ClassificationLookupVlr")[0]
-
-    assert classification_lookups[20] == "computer"
-    assert classification_lookups[17] == "car"
-
-
-def test_lookup_out_of_range():
-    classification_lookup = laspy.vlrs.known.ClassificationLookupVlr()
-    with pytest.raises(ValueError):
-        classification_lookup[541] = "LiquidWater"
-
-    with pytest.raises(ValueError):
-        classification_lookup[-42] = "SolidWater"
-
-
-def test_adding_extra_bytes_vlr_by_hand():
-    """
-    Test that if someone adds an ExtraBytesVlr by himself
-    without having matching extra bytes in the point record, the
-    ExtraByteVlr is removed before writing
-    """
-
-    simple = laspy.read(test_common.simple_las)
-    ebvlr = laspy.vlrs.known.ExtraBytesVlr()
-    ebs = laspy.vlrs.known.ExtraBytesStruct(data_type=3, name="Fake".encode())
-    ebvlr.extra_bytes_structs.append(ebs)
-    simple.vlrs.append(ebvlr)
-    assert len(simple.vlrs.get("ExtraBytesVlr")) == 1
-
-    las = laspy.lib.write_then_read_again(simple)
-    assert simple.points.point_size == las.points.point_size
-    assert len(las.vlrs.get("ExtraBytesVlr")) == 0
-
-
-def test_geokey_parsing_does_not_require_optional_params():
-    las = laspy.read(str(Path(__file__).parent / "data/simple1_3.las"))
-    geo_keys = laspy.vlrs.geotiff.parse_geo_tiff_keys_from_vlrs(las.vlrs)
-    assert len(geo_keys) == 6
-
-
-def test_cannot_write_vlrs_with_more_than_uint16_max_bytes():
-    las = laspy.read(test_common.simple_las)
-    big_junk_vlr = laspy.VLR(
-        user_id="LASPY_ID",
-        record_id=0,
-        description="A VLR full of junk data",
-        record_data=b"1" * (65_535 + 1),
-    )
-    las.vlrs.append(big_junk_vlr)
-
-    with pytest.raises(ValueError):
-        with io.BytesIO() as output:
-            las.write(output)
+import io
+from pathlib import Path
+
+import pytest
+
+import laspy
+from tests import test_common
+
+
+def test_adding_classification_lookup():
+    simple = laspy.read(test_common.simple_las)
+    classification_lookup = laspy.vlrs.known.ClassificationLookupVlr()
+
+    assert len(classification_lookup.lookups) == 0
+    classification_lookup[20] = "computer"
+    assert len(classification_lookup.lookups) == 1
+    classification_lookup[17] = "car"
+
+    simple.vlrs.append(classification_lookup)
+
+    simple = test_common.write_then_read_again(simple)
+    classification_lookups = simple.vlrs.get("ClassificationLookupVlr")[0]
+
+    assert classification_lookups[20] == "computer"
+    assert classification_lookups[17] == "car"
+
+
+def test_lookup_out_of_range():
+    classification_lookup = laspy.vlrs.known.ClassificationLookupVlr()
+    with pytest.raises(ValueError):
+        classification_lookup[541] = "LiquidWater"
+
+    with pytest.raises(ValueError):
+        classification_lookup[-42] = "SolidWater"
+
+
+def test_adding_extra_bytes_vlr_by_hand():
+    """
+    Test that if someone adds an ExtraBytesVlr by himself
+    without having matching extra bytes in the point record, the
+    ExtraByteVlr is removed before writing
+    """
+
+    simple = laspy.read(test_common.simple_las)
+    ebvlr = laspy.vlrs.known.ExtraBytesVlr()
+    ebs = laspy.vlrs.known.ExtraBytesStruct(data_type=3, name="Fake".encode())
+    ebvlr.extra_bytes_structs.append(ebs)
+    simple.vlrs.append(ebvlr)
+    assert len(simple.vlrs.get("ExtraBytesVlr")) == 1
+
+    las = laspy.lib.write_then_read_again(simple)
+    assert simple.points.point_size == las.points.point_size
+    assert len(las.vlrs.get("ExtraBytesVlr")) == 0
+
+
+def test_geokey_parsing_does_not_require_optional_params():
+    las = laspy.read(str(Path(__file__).parent / "data/simple1_3.las"))
+    geo_keys = laspy.vlrs.geotiff.parse_geo_tiff_keys_from_vlrs(las.vlrs)
+    assert len(geo_keys) == 6
+
+
+def test_cannot_write_vlrs_with_more_than_uint16_max_bytes():
+    las = laspy.read(test_common.simple_las)
+    big_junk_vlr = laspy.VLR(
+        user_id="LASPY_ID",
+        record_id=0,
+        description="A VLR full of junk data",
+        record_data=b"1" * (65_535 + 1),
+    )
+    las.vlrs.append(big_junk_vlr)
+
+    with pytest.raises(ValueError):
+        with io.BytesIO() as output:
+            las.write(output)
```

