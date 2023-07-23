# Comparing `tmp/noether-0.1.3.tar.gz` & `tmp/noether-1.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/noether-0.1.3.tar", last modified: Thu Nov  5 16:23:11 2020, max compression
+gzip compressed data, was "noether-1.0.0.tar", last modified: Sun Jul 23 17:13:55 2023, max compression
```

## Comparing `noether-0.1.3.tar` & `noether-1.0.0.tar`

### file list

```diff
@@ -1,53 +1,77 @@
-drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2020-11-05 16:23:11.300900 noether-0.1.3/
--rw-r--r--   0 yunruse    (501) staff       (20)     4917 2020-11-05 16:23:11.300487 noether-0.1.3/PKG-INFO
--rw-r--r--   0 yunruse    (501) staff       (20)     3617 2020-11-05 16:17:17.000000 noether-0.1.3/README.md
-drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2020-11-05 16:23:11.283202 noether-0.1.3/noether/
--rw-r--r--   0 yunruse    (501) staff       (20)     1345 2020-11-05 16:17:17.000000 noether-0.1.3/noether/__init__.py
--rw-r--r--   0 yunruse    (501) staff       (20)       88 2020-09-26 15:11:56.000000 noether-0.1.3/noether/__main__.py
--rw-r--r--   0 yunruse    (501) staff       (20)     3236 2020-11-05 16:17:17.000000 noether-0.1.3/noether/conf.py
--rw-r--r--   0 yunruse    (501) staff       (20)     2173 2020-11-05 16:17:17.000000 noether-0.1.3/noether/display.py
--rw-r--r--   0 yunruse    (501) staff       (20)     5792 2020-11-05 16:17:17.000000 noether-0.1.3/noether/fraction.py
--rw-r--r--   0 yunruse    (501) staff       (20)     6115 2020-11-05 16:17:17.000000 noether-0.1.3/noether/graphing.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1720 2020-11-05 16:17:17.000000 noether-0.1.3/noether/helpers.py
--rw-r--r--   0 yunruse    (501) staff       (20)      232 2020-09-26 15:33:32.000000 noether-0.1.3/noether/locale.py
--rw-r--r--   0 yunruse    (501) staff       (20)     2450 2020-09-26 15:33:33.000000 noether-0.1.3/noether/matrix.py
--rw-r--r--   0 yunruse    (501) staff       (20)     4856 2020-09-26 15:33:34.000000 noether-0.1.3/noether/particles.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1783 2020-09-26 15:33:35.000000 noether-0.1.3/noether/repr.py
-drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2020-11-05 16:23:11.287662 noether-0.1.3/noether/statistics/
--rw-r--r--   0 yunruse    (501) staff       (20)       67 2020-09-22 12:13:35.000000 noether-0.1.3/noether/statistics/__init__.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1409 2020-09-22 12:13:35.000000 noether-0.1.3/noether/statistics/distcatalogue.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1583 2020-09-22 12:13:35.000000 noether-0.1.3/noether/statistics/distribution.py
--rw-r--r--   0 yunruse    (501) staff       (20)      155 2020-09-22 12:13:35.000000 noether-0.1.3/noether/statistics/functions.py
-drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2020-11-05 16:23:11.291948 noether-0.1.3/noether/unit/
--rw-r--r--   0 yunruse    (501) staff       (20)      282 2020-09-26 15:41:37.000000 noether-0.1.3/noether/unit/__init__.py
-drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2020-11-05 16:23:11.299996 noether-0.1.3/noether/unit/catalogue/
--rw-r--r--   0 yunruse    (501) staff       (20)     2161 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/catalogue/__init__.py
--rw-r--r--   0 yunruse    (501) staff       (20)      446 2020-09-26 15:33:41.000000 noether-0.1.3/noether/unit/catalogue/cgs.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1675 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/catalogue/constants.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1040 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/catalogue/conventional.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1265 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/catalogue/data.py
--rw-r--r--   0 yunruse    (501) staff       (20)     3425 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/catalogue/dimensions.py
--rw-r--r--   0 yunruse    (501) staff       (20)     3146 2020-09-26 15:34:27.000000 noether-0.1.3/noether/unit/catalogue/fundamental.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1708 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/catalogue/historical.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1410 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/catalogue/imperial.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1852 2020-09-26 15:34:27.000000 noether-0.1.3/noether/unit/catalogue/planck.py
--rw-r--r--   0 yunruse    (501) staff       (20)     2081 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/catalogue/scientific.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1227 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/catalogue/si.py
--rw-r--r--   0 yunruse    (501) staff       (20)       94 2020-09-26 15:33:50.000000 noether-0.1.3/noether/unit/catalogue/systems.py
--rw-r--r--   0 yunruse    (501) staff       (20)     2057 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/catalogue/unusual.py
--rw-r--r--   0 yunruse    (501) staff       (20)     4918 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/dimension.py
--rw-r--r--   0 yunruse    (501) staff       (20)     2329 2020-09-26 15:35:18.000000 noether-0.1.3/noether/unit/function.py
--rw-r--r--   0 yunruse    (501) staff       (20)      905 2020-09-26 15:35:12.000000 noether-0.1.3/noether/unit/maths.py
--rw-r--r--   0 yunruse    (501) staff       (20)    10509 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/measure.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1365 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/spectrum.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1215 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/unit.py
--rw-r--r--   0 yunruse    (501) staff       (20)      620 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/unit_chained.py
--rw-r--r--   0 yunruse    (501) staff       (20)     1976 2020-11-05 16:17:17.000000 noether-0.1.3/noether/unit/unit_system.py
-drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2020-11-05 16:23:11.285177 noether-0.1.3/noether.egg-info/
--rwxrwxrwx   0 yunruse    (501) staff       (20)     4917 2020-11-05 16:23:11.000000 noether-0.1.3/noether.egg-info/PKG-INFO
--rwxrwxrwx   0 yunruse    (501) staff       (20)     1223 2020-11-05 16:23:11.000000 noether-0.1.3/noether.egg-info/SOURCES.txt
--rwxrwxrwx   0 yunruse    (501) staff       (20)        1 2020-11-05 16:23:11.000000 noether-0.1.3/noether.egg-info/dependency_links.txt
--rwxrwxrwx   0 yunruse    (501) staff       (20)       18 2020-11-05 16:23:11.000000 noether-0.1.3/noether.egg-info/requires.txt
--rwxrwxrwx   0 yunruse    (501) staff       (20)        8 2020-11-05 16:23:11.000000 noether-0.1.3/noether.egg-info/top_level.txt
--rw-r--r--   0 yunruse    (501) staff       (20)       38 2020-11-05 16:23:11.301037 noether-0.1.3/setup.cfg
--rw-r--r--   0 yunruse    (501) staff       (20)      967 2020-11-05 16:17:17.000000 noether-0.1.3/setup.py
+drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2023-07-23 17:13:55.263338 noether-1.0.0/
+-rw-r--r--   0 yunruse    (501) staff       (20)     1064 2023-07-23 11:11:28.000000 noether-1.0.0/LICENSE.txt
+-rw-r--r--   0 yunruse    (501) staff       (20)     3473 2023-07-23 17:13:55.262670 noether-1.0.0/PKG-INFO
+-rw-r--r--   0 yunruse    (501) staff       (20)     2899 2023-07-23 17:11:56.000000 noether-1.0.0/README.md
+drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2023-07-23 17:13:55.179701 noether-1.0.0/noether/
+-rw-r--r--   0 yunruse    (501) staff       (20)     3760 2023-07-23 11:11:28.000000 noether-1.0.0/noether/Multiplication.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      119 2023-07-23 11:11:28.000000 noether-1.0.0/noether/__init__.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2164 2023-07-23 11:11:28.000000 noether-1.0.0/noether/__main__.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1430 2023-07-23 11:11:28.000000 noether-1.0.0/noether/_tokenizers.py
+drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2023-07-23 17:13:55.191361 noether-1.0.0/noether/catalogue/
+-rw-r--r--   0 yunruse    (501) staff       (20)     1140 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/__init__.py
+drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2023-07-23 17:13:55.196982 noether-1.0.0/noether/catalogue/conventional/
+-rw-r--r--   0 yunruse    (501) staff       (20)      145 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/conventional/__init__.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2872 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/conventional/conventional.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2425 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/conventional/imperial.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      634 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/conventional/typographic.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     5950 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/dimensions.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1048 2023-07-23 16:18:14.000000 noether-1.0.0/noether/catalogue/fundamental.py
+drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2023-07-23 17:13:55.206439 noether-1.0.0/noether/catalogue/historic/
+-rw-r--r--   0 yunruse    (501) staff       (20)      110 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/historic/__init__.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2485 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/historic/ancient_greek.units.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     4233 2023-07-23 17:13:44.000000 noether-1.0.0/noether/catalogue/historic/ancient_greek_.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      567 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/historic/mts.units.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      792 2023-07-23 17:13:44.000000 noether-1.0.0/noether/catalogue/historic/mts_.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      456 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/historic/scientific.py
+drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2023-07-23 17:13:55.212544 noether-1.0.0/noether/catalogue/humorous/
+-rw-r--r--   0 yunruse    (501) staff       (20)       73 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/humorous/__init__.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2377 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/humorous/fictional.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      820 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/humorous/potrzebie.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1080 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/humorous/unusual.py
+drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2023-07-23 17:13:55.222058 noether-1.0.0/noether/catalogue/info/
+-rw-r--r--   0 yunruse    (501) staff       (20)       97 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/info/__init__.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2610 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/info/comparison.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      282 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/info/dimension.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2152 2023-07-23 16:35:16.000000 noether-1.0.0/noether/catalogue/info/spectrum.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      355 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/info/unit_context.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      476 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/info/unit_value.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2304 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/prefixes.py
+drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2023-07-23 17:13:55.238716 noether-1.0.0/noether/catalogue/scientific/
+-rw-r--r--   0 yunruse    (501) staff       (20)     2804 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/scientific/CODATA.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      216 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/scientific/__init__.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1354 2023-07-23 16:12:45.000000 noether-1.0.0/noether/catalogue/scientific/astronomy.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1640 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/scientific/cgs.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      290 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/scientific/climate.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      752 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/scientific/constants.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1803 2023-07-23 16:20:54.000000 noether-1.0.0/noether/catalogue/scientific/data.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2411 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/scientific/essential.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2797 2023-07-23 11:11:28.000000 noether-1.0.0/noether/catalogue/scientific/si.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     4883 2023-07-23 11:11:28.000000 noether-1.0.0/noether/config.py
+drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2023-07-23 17:13:55.254302 noether-1.0.0/noether/core/
+-rw-r--r--   0 yunruse    (501) staff       (20)     3934 2023-07-23 11:11:28.000000 noether-1.0.0/noether/core/Catalogue.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     3940 2023-07-23 16:32:04.000000 noether-1.0.0/noether/core/Dimension.py
+-rw-r--r--   0 yunruse    (501) staff       (20)    12450 2023-07-23 16:31:59.000000 noether-1.0.0/noether/core/Measure.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      471 2023-07-23 11:11:28.000000 noether-1.0.0/noether/core/MeasureInfo.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1293 2023-07-23 11:11:28.000000 noether-1.0.0/noether/core/MeasureRelative.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1652 2023-07-23 11:11:28.000000 noether-1.0.0/noether/core/Prefix.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     4752 2023-07-23 16:37:02.000000 noether-1.0.0/noether/core/Unit.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1179 2023-07-23 11:11:28.000000 noether-1.0.0/noether/core/UnitSet.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1898 2023-07-23 11:11:28.000000 noether-1.0.0/noether/core/_DisplayHandler.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      271 2023-07-23 11:11:28.000000 noether-1.0.0/noether/core/__init__.py
+drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2023-07-23 17:13:55.261368 noether-1.0.0/noether/core/units/
+-rw-r--r--   0 yunruse    (501) staff       (20)     1257 2023-07-23 11:11:28.000000 noether-1.0.0/noether/core/units/AffineUnit.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1524 2023-07-23 11:11:28.000000 noether-1.0.0/noether/core/units/GeometricUnit.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2002 2023-07-23 16:31:44.000000 noether-1.0.0/noether/core/units/LinearUnit.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      516 2023-07-23 11:11:28.000000 noether-1.0.0/noether/core/units/PrefixedUnit.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      180 2023-07-23 11:11:28.000000 noether-1.0.0/noether/core/units/__init__.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     2020 2023-07-23 16:40:01.000000 noether-1.0.0/noether/display.py
+-rw-r--r--   0 yunruse    (501) staff       (20)      974 2023-07-23 11:11:28.000000 noether-1.0.0/noether/errors.py
+-rw-r--r--   0 yunruse    (501) staff       (20)     1576 2023-07-23 11:11:28.000000 noether-1.0.0/noether/helpers.py
+drwxr-xr-x   0 yunruse    (501) staff       (20)        0 2023-07-23 17:13:55.185640 noether-1.0.0/noether.egg-info/
+-rw-r--r--   0 yunruse    (501) staff       (20)     3473 2023-07-23 17:13:55.000000 noether-1.0.0/noether.egg-info/PKG-INFO
+-rw-r--r--   0 yunruse    (501) staff       (20)     2045 2023-07-23 17:13:55.000000 noether-1.0.0/noether.egg-info/SOURCES.txt
+-rw-r--r--   0 yunruse    (501) staff       (20)        1 2023-07-23 17:13:55.000000 noether-1.0.0/noether.egg-info/dependency_links.txt
+-rw-r--r--   0 yunruse    (501) staff       (20)        8 2023-07-23 17:13:55.000000 noether-1.0.0/noether.egg-info/top_level.txt
+-rw-r--r--   0 yunruse    (501) staff       (20)      301 2023-07-23 11:11:28.000000 noether-1.0.0/pyproject.toml
+-rw-r--r--   0 yunruse    (501) staff       (20)       38 2023-07-23 17:13:55.263541 noether-1.0.0/setup.cfg
+-rw-r--r--   0 yunruse    (501) staff       (20)      807 2023-07-23 17:09:31.000000 noether-1.0.0/setup.py
```

### Comparing `noether-0.1.3/noether/unit/dimension.py` & `noether-1.0.0/noether/config.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,168 +1,184 @@
-"""Noether: Measure Dimension"""
+'''
+TOML configuration.
+'''
 
-import bisect
-from collections import namedtuple
-from numbers import Number, Real
+from typing import Generic, TypeVar
+from dataclasses import dataclass
 
-from ..conf import conf
-from ..helpers import intify
-from ..display import superscript
+import json
+import os
+from pathlib import Path
+import toml
+import warnings
 
-_BaseDimension = namedtuple(
-    "_BaseDimension", "order name symbol display_unit".split())
-# TODO: enforce Fraction, rather than float, on dimension exponent
+from .errors import ConfigWarning
+from .helpers import get_dot_config
 
+CONF_FILE = get_dot_config() / 'noether.toml'
 
-class Dimension(dict):
-    """Dimension of a unit. Inherently immutible."""
-    _dimensions_display = list()  # self-ordering
-    _dimensions_map = dict()
+ConfigType = TypeVar('ConfigType', bool, str, int)
 
-    # Name registry (such that generated Dimensions map)
-    _names = dict()
 
-    def __init__(self, value=None, **kw):
-        value = value or dict()
+@dataclass
+class ConfigOption(Generic[ConfigType]):
+    name: str
+    default: ConfigType
+    type: type
+    help: str = ""
 
-        if isinstance(value, dict):
-            value = value
-        elif isinstance(value, Unit):
-            value = value.dim
-
-        value.update(kw)
-        dims = value.copy()
-
-        for name, exp in value.items():
-            if not exp:
-                del dims[name]
-            if name not in self._dimensions_map:
-                raise ValueError(
-                    "Unknown dimension {!r}. Did you register it with .new?"
-                    .format(name))
-
-        dict.__init__(self, dims)
-
-    @classmethod
-    def new(cls, name, dimsym, unitsym, order=500):
-        """
-        Generate a new dimension.
-
-        Requires a name, dimension symbol and fundamental unit symbol.
-        """
-        base = _BaseDimension(order, name, dimsym, unitsym)
-        bisect.insort_left(cls._dimensions_display, base)
-        cls._dimensions_map[name] = base
-        return cls({name: 1})
-
-    # Immutability
-
-    def __setitem__(self, name, value):
-        raise TypeError(
-            '{!r} object does not support item assignment'.format(type(self).__name__))
-
-    def __delitem__(self, name):
-        raise TypeError(
-            '{!r} object does not support item deletion'.format(type(self).__name__))
-
-    def __hash__(self):
-        return hash(tuple(sorted(self.items())))
+    @property
+    def category(self):
+        return self.name.split('_', 1)[0]
 
     @property
-    def names(self):
-        return self._names.get(self, list())
+    def at_import(self):
+        return self.category.isupper()
 
-    def addName(self, name):
-        name = name.replace('_', ' ')
-        if self not in self._names:
-            self._names[self] = list()
-        self._names[self].append(name)
-
-    # Reproduction
-
-    def as_fundamental(self, as_units=True):
-        dims = []
-        for _, name, dim_sym, unit_sym in self._dimensions_display:
-            sym = unit_sym if as_units else dim_sym
-            exp = self.get(name, 0)
-            if exp == 0:
-                continue
-            elif exp != 1:
-                sym += superscript(exp, conf.unicode_exponent)
-            dims.append(sym)
 
-        return "·".join(dims)
+def ConfigProperty(option: ConfigOption):
+    def getter(self: Config):
+        if option.name in self._config:
+            return self._config[option.name]
+        return option.default
+
+    def setter(self: Config, value):
+        typ = option.type
+        if not isinstance(value, typ):
+            raise TypeError(
+                f"conf.{option.name} must be {option.type.__name__},"
+                f" not {type(value).__name__}")
+        self._config[option.name] = value
+
+        if option.at_import:
+            warnings.warn(
+                'This change will only apply after doing conf.save() and reloading.',
+                ConfigWarning, stacklevel=2,
+            )
+
+    def deleter(self: Config):
+        if option.name in self._config:
+            del self._config[option.name]
+    return property(getter, setter, deleter)
+
+
+class Config:
+    _config: dict
+    options: dict[str, ConfigOption] = dict()
 
-    def __str__(self):
-        return self.as_fundamental(as_units=False)
+    @classmethod
+    def register(
+        cls,
+        key: str,
+        default: ConfigType,
+        help: str | None = None,
+        typ: type | None = None,
+    ):
+        option = ConfigOption(
+            key, default,
+            typ or type(default), help or ""
+        )
+        cls.options[key] = option
+        setattr(cls, key, ConfigProperty(option))
+        return key
+
+    def __init__(
+        self,
+        value: dict | None = None,
+        **kwargs,
+    ):
+        self._config = {
+            k: v.default
+            for k, v in self.options.items()}
+        self._config.update(value or {})
+        self._config.update(kwargs)
+
+    def _show_in_repr(self, k: str, v):
+        if k not in self.options:
+            return True
+        return bool(v != self.options[k].default)
 
     def __repr__(self):
-        if not self:
-            return 'dimensionless'
-        exponents = sorted(list(self.items()),
-                           key=lambda q: (q[1] < 0, abs(q[1])))
-        string = '1' if exponents[0][1] < 0 else ''
-        for dim, exp in exponents:
-            if string:
-                string += ' / ' if exp < 0 else ' * '
-            aexp = abs(exp)
-            if aexp == 1/2:
-                string += 'sqrt('+dim+')'
-                continue
-            string += dim
-            if aexp != 1:
-                string += '**' + str(aexp)
-        return string
-
-    # Operations
-
-    def __bool__(self):
-        return not all(i == 0 for i in self.values())
-
-    def __pow__(self, exp):
-        if isinstance(exp, Real):
-            return Dimension({k: intify(v * exp) for k, v in self.items()})
-        else:
-            raise TypeError("Cannot raise dimension to non-real exponent")
-
-    def _cmp(self, other):
-        """Check and attempt to match other unit to Dimension"""
-        if isinstance(other, Number):
-            return Dimension()
-        if isinstance(other, Dimension):
-            return other
-        elif isinstance(other, Unit):
-            return other.dim
+        return 'Config({})'.format(', '.join(
+            f'{k}={v}' for k, v in self._config.items()
+            if self._show_in_repr(k, v)
+        ))
+
+    def _get_defaults(self):
+        for k in self.options:
+            self._config.setdefault(k, self.options[k].default)
+
+    def reset(self):
+        for k in self.options:
+            self._config[k] = self.options[k].default
+
+    # % Attributes
+
+    def get(self, key: str):
+        if key in self._config:
+            return self._config[key]
+        elif key in self.options:
+            return self.options[key].default
         else:
-            raise TypeError("Cannot operate on Dimension with {}".format(
-                type(other).__name__))
-
-    def __mul__(self, other, op=+1):
-        other = self._cmp(other)
-        names = set(self.keys()).union(set(other.keys()))
-        return Dimension(
-            {n: self.get(n, 0) + op * other.get(n, 0)
-             for n in names})
-
-    def __truediv__(self, other):
-        return self.__mul__(other, -1)
-
-    def __rtruediv__(self, exp):
-        return self._cmp(exp) / self
-
-    __rmul__ = __mul__
-    __pos__ = __neg__ = lambda s: s
-
-    def check_linear(self, other):
-        other = self._cmp(other)
-        if self == other:
-            return self
-        else:
-            raise ValueError(
-                "Cannot add or subtract inequal dimensions {} and {}".
-                format(self, other))
-
-    __sub__ = __rsub__ = __add__ = __radd__ = check_linear
+            raise KeyError('Unknown config key', key)
 
+    # % IO
 
-# avoid import-loop
-from .unit import Unit  # noqa
+    def categories(self):
+        cats: dict[str, list[str]] = dict()
+        for name in sorted(self.options.keys()):
+            cat, name = name.split('_', 1)
+            cats.setdefault(cat, [])
+            cats[cat].append(name)
+        return cats
+
+    def __str__(self, help=True):
+        self._get_defaults()
+
+        string = ""
+        for cat_name, names in self.categories().items():
+            string += f"\n\n[{cat_name}]"
+
+            for name in names:
+                fullname = f'{cat_name}_{name}'
+                value = self.get(fullname)
+                desc = self.options[fullname].help.strip()
+                if help:
+                    string += "\n"
+                    for l in desc.split('\n'):
+                        string += f'# {l}\n'
+                value = json.dumps(value)
+                string += f'{name} = {value}'
+
+        return string.strip()
+
+    def save(self, path: Path = CONF_FILE, help=True):
+        os.makedirs(path.parent, exist_ok=True)
+        with open(path, 'w') as f:
+            f.write(self.__str__(help))
+
+    def _load(self, path: Path = CONF_FILE):
+        with open(path) as f:
+            new = toml.load(f)
+
+        for cat_name, cat in new.items():
+            for name, value in cat.items():
+                fullname = f'{cat_name}_{name}'
+                self._config[fullname] = value
+
+    def _remove_unused_keys(self):
+        for name in list(self._config):
+            if name not in self.options:
+                warnings.warn(
+                    f"Unknown config option {name!r}.",
+                    ConfigWarning, stacklevel=4
+                )
+                del self._config[name]
+
+    def load(self, path: Path = CONF_FILE):
+        self._load(path)
+        self._remove_unused_keys()
+
+
+conf = Config()
+if CONF_FILE.is_file():
+    conf._load(CONF_FILE)
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `noether-0.1.3/setup.py` & `noether-1.0.0/setup.py`

 * *Files 17% similar despite different names*

```diff
@@ -3,29 +3,25 @@
 with open("README.md", "r") as f:
     long_description = f.read()
 
 packages = setuptools.find_packages()
 
 setuptools.setup(
     name="noether",
-    version="0.1.3",
+    version="1.0.0",
     author="Mia yun Ruse",
     author_email="mia@yunru.se",
     description="Work with physical measurements and constants",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/yunruse/noether",
-    project_urls={
-        "Bug Tracker": "https://www.notion.so/yunruse/714348466a284bd1b0d1942c81688579",
-    },
     packages=packages,
     classifiers=[
         "Programming Language :: Python :: 3",
         "Operating System :: OS Independent",
         "License :: OSI Approved",
         "Topic :: Scientific/Engineering",
-        "Development Status :: 3 - Alpha",
+        "Development Status :: 4 - Beta",
     ],
     keywords="physics unit measure constant measurement uncertainty",
-    python_requires='>=3.6',
-    install_requires=["nestedtext>=1.0.0"],
+    python_requires='>=3.10'
 )
```

