# Comparing `tmp/klepto-0.2.3.tar.gz` & `tmp/klepto-0.2.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "klepto-0.2.3.tar", last modified: Sun Oct 23 22:59:13 2022, max compression
+gzip compressed data, was "klepto-0.2.4.tar", last modified: Sat Jul 22 23:57:42 2023, max compression
```

## Comparing `klepto-0.2.3.tar` & `klepto-0.2.4.tar`

### file list

```diff
@@ -1,65 +1,68 @@
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:59:13.597144 klepto-0.2.3/
--rw-r--r--   0 mmckerns   (501) staff       (20)      832 2022-05-16 22:44:02.000000 klepto-0.2.3/.codecov.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)      561 2022-05-16 22:44:02.000000 klepto-0.2.3/.coveragerc
--rw-r--r--   0 mmckerns   (501) staff       (20)       32 2017-01-02 10:21:24.000000 klepto-0.2.3/.gitignore
--rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-05-16 22:44:10.000000 klepto-0.2.3/.readthedocs.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1569 2022-07-02 18:51:23.000000 klepto-0.2.3/.travis.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2022-01-01 16:25:56.000000 klepto-0.2.3/LICENSE
--rw-r--r--   0 mmckerns   (501) staff       (20)      185 2022-07-06 22:17:30.000000 klepto-0.2.3/MANIFEST.in
--rw-r--r--   0 mmckerns   (501) staff       (20)     6914 2022-10-23 22:59:13.597428 klepto-0.2.3/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     6363 2022-10-23 22:55:52.000000 klepto-0.2.3/README.md
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:59:13.552137 klepto-0.2.3/docs/
--rw-r--r--   0 mmckerns   (501) staff       (20)      544 2022-05-12 20:37:05.000000 klepto-0.2.3/docs/Makefile
--rw-r--r--   0 mmckerns   (501) staff       (20)      430 2022-05-17 16:06:58.000000 klepto-0.2.3/docs/requirements.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:59:13.555978 klepto-0.2.3/docs/source/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7258 2022-07-06 22:23:09.000000 klepto-0.2.3/docs/source/conf.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      379 2017-08-23 20:54:48.000000 klepto-0.2.3/docs/source/index.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)     1299 2017-08-23 20:54:48.000000 klepto-0.2.3/docs/source/klepto.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2017-08-11 19:08:04.000000 klepto-0.2.3/docs/source/pathos.png
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:59:13.573714 klepto-0.2.3/klepto/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7667 2022-10-23 22:59:13.000000 klepto-0.2.3/klepto/__info__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1560 2022-07-06 22:31:23.000000 klepto-0.2.3/klepto/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2502 2022-06-27 01:50:05.000000 klepto-0.2.3/klepto/_abc.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    98541 2022-09-13 21:05:52.000000 klepto-0.2.3/klepto/_archives.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    54628 2022-06-27 01:52:35.000000 klepto-0.2.3/klepto/_cache.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    20347 2022-06-27 01:53:47.000000 klepto-0.2.3/klepto/_inspect.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    15843 2022-06-27 01:20:31.000000 klepto-0.2.3/klepto/_pickle.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11354 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/archives.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4604 2022-06-27 01:54:55.000000 klepto-0.2.3/klepto/crypto.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    14059 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/keymaps.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7240 2022-06-27 01:11:02.000000 klepto-0.2.3/klepto/rounding.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    57290 2022-06-27 01:55:06.000000 klepto-0.2.3/klepto/safe.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:59:13.596469 klepto-0.2.3/klepto/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)      507 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      901 2022-07-09 10:46:47.000000 klepto-0.2.3/klepto/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      517 2022-07-02 18:53:47.000000 klepto-0.2.3/klepto/tests/cleanup_basic.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1138 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/test_alchemy.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5761 2022-04-21 22:00:24.000000 klepto-0.2.3/klepto/tests/test_basic.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      835 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/test_bigdata.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7511 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/test_cache.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5154 2022-06-26 21:58:35.000000 klepto-0.2.3/klepto/tests/test_cache_info.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3201 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/test_cachekeys.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1178 2022-06-27 01:01:20.000000 klepto-0.2.3/klepto/tests/test_chaining.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2539 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/test_crypto.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2203 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/test_frame.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3675 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/test_hdf.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7967 2022-06-27 00:49:25.000000 klepto-0.2.3/klepto/tests/test_ignore.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3102 2022-06-27 01:03:10.000000 klepto-0.2.3/klepto/tests/test_keymaps.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      649 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/test_pickles.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3304 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/test_readwrite.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2501 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/test_rounding.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4197 2022-06-27 00:59:00.000000 klepto-0.2.3/klepto/tests/test_validate.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3384 2022-01-01 16:25:56.000000 klepto-0.2.3/klepto/tests/test_workflow.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1259 2022-06-27 01:56:40.000000 klepto-0.2.3/klepto/tools.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:59:13.578422 klepto-0.2.3/klepto.egg-info/
--rw-r--r--   0 mmckerns   (501) staff       (20)     6914 2022-10-23 22:59:13.000000 klepto-0.2.3/klepto.egg-info/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     1252 2022-10-23 22:59:13.000000 klepto-0.2.3/klepto.egg-info/SOURCES.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-23 22:59:13.000000 klepto-0.2.3/klepto.egg-info/dependency_links.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-23 22:59:13.000000 klepto-0.2.3/klepto.egg-info/not-zip-safe
--rw-r--r--   0 mmckerns   (501) staff       (20)      127 2022-10-23 22:59:13.000000 klepto-0.2.3/klepto.egg-info/requires.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        7 2022-10-23 22:59:13.000000 klepto-0.2.3/klepto.egg-info/top_level.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)      166 2022-05-20 09:48:49.000000 klepto-0.2.3/pyproject.toml
--rw-r--r--   0 mmckerns   (501) staff       (20)       62 2022-10-23 22:59:13.598689 klepto-0.2.3/setup.cfg
--rw-r--r--   0 mmckerns   (501) staff       (20)     4785 2022-10-23 22:55:14.000000 klepto-0.2.3/setup.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      400 2022-07-09 10:48:03.000000 klepto-0.2.3/tox.ini
--rw-r--r--   0 mmckerns   (501) staff       (20)     2733 2022-10-23 22:58:52.000000 klepto-0.2.3/version.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 23:57:42.230781 klepto-0.2.4/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      832 2022-05-16 22:44:02.000000 klepto-0.2.4/.codecov.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)      561 2022-05-16 22:44:02.000000 klepto-0.2.4/.coveragerc
+-rw-r--r--   0 mmckerns   (501) staff       (20)       32 2017-01-02 10:21:24.000000 klepto-0.2.4/.gitignore
+-rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-05-16 22:44:10.000000 klepto-0.2.4/.readthedocs.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1806 2023-07-07 03:08:38.000000 klepto-0.2.4/.travis.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2023-02-08 18:05:55.000000 klepto-0.2.4/LICENSE
+-rw-r--r--   0 mmckerns   (501) staff       (20)      185 2022-07-06 22:17:30.000000 klepto-0.2.4/MANIFEST.in
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6965 2023-07-22 23:57:42.231061 klepto-0.2.4/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6365 2023-07-22 22:38:34.000000 klepto-0.2.4/README.md
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 23:57:42.159156 klepto-0.2.4/docs/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      544 2022-05-12 20:37:05.000000 klepto-0.2.4/docs/Makefile
+-rw-r--r--   0 mmckerns   (501) staff       (20)      430 2023-07-22 01:39:25.000000 klepto-0.2.4/docs/requirements.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 23:57:42.163717 klepto-0.2.4/docs/source/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 23:57:42.147820 klepto-0.2.4/docs/source/_static/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 23:57:42.165518 klepto-0.2.4/docs/source/_static/css/
+-rw-r--r--   0 mmckerns   (501) staff       (20)       85 2023-07-05 04:40:26.000000 klepto-0.2.4/docs/source/_static/css/custom.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7847 2023-07-05 04:57:42.000000 klepto-0.2.4/docs/source/conf.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      300 2023-07-05 05:54:11.000000 klepto-0.2.4/docs/source/index.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      566 2023-02-04 19:38:36.000000 klepto-0.2.4/docs/source/klepto.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2017-08-11 19:08:04.000000 klepto-0.2.4/docs/source/pathos.png
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 23:57:42.189938 klepto-0.2.4/klepto/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7667 2023-07-22 23:57:42.000000 klepto-0.2.4/klepto/__info__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1560 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2502 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/_abc.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    99698 2023-07-17 01:46:20.000000 klepto-0.2.4/klepto/_archives.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    54628 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/_cache.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    20693 2023-03-25 00:43:06.000000 klepto-0.2.4/klepto/_inspect.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15843 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/_pickle.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11387 2023-02-20 18:05:08.000000 klepto-0.2.4/klepto/archives.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4508 2023-06-14 00:17:54.000000 klepto-0.2.4/klepto/crypto.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    14059 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/keymaps.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7240 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/rounding.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    57290 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/safe.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 23:57:42.229909 klepto-0.2.4/klepto/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      507 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      901 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      517 2022-07-02 18:53:47.000000 klepto-0.2.4/klepto/tests/cleanup_basic.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2721 2023-07-16 02:39:17.000000 klepto-0.2.4/klepto/tests/test_alchemy.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5761 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_basic.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      835 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_bigdata.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7511 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_cache.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5154 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_cache_info.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3201 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_cachekeys.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1178 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_chaining.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2539 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_crypto.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2203 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_frame.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3675 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_hdf.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7967 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_ignore.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3102 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_keymaps.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      649 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_pickles.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3304 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_readwrite.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2501 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_rounding.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7205 2023-03-25 01:29:43.000000 klepto-0.2.4/klepto/tests/test_validate.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3384 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tests/test_workflow.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1259 2023-01-01 13:11:19.000000 klepto-0.2.4/klepto/tools.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 23:57:42.195198 klepto-0.2.4/klepto.egg-info/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6965 2023-07-22 23:57:42.000000 klepto-0.2.4/klepto.egg-info/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1287 2023-07-22 23:57:42.000000 klepto-0.2.4/klepto.egg-info/SOURCES.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-22 23:57:42.000000 klepto-0.2.4/klepto.egg-info/dependency_links.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-22 23:57:41.000000 klepto-0.2.4/klepto.egg-info/not-zip-safe
+-rw-r--r--   0 mmckerns   (501) staff       (20)      127 2023-07-22 23:57:42.000000 klepto-0.2.4/klepto.egg-info/requires.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        7 2023-07-22 23:57:42.000000 klepto-0.2.4/klepto.egg-info/top_level.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)      166 2022-05-20 09:48:49.000000 klepto-0.2.4/pyproject.toml
+-rw-r--r--   0 mmckerns   (501) staff       (20)       62 2023-07-22 23:57:42.232032 klepto-0.2.4/setup.cfg
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4835 2023-07-22 23:54:47.000000 klepto-0.2.4/setup.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      428 2023-07-07 03:06:09.000000 klepto-0.2.4/tox.ini
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3171 2023-07-22 22:42:49.000000 klepto-0.2.4/version.py
```

### Comparing `klepto-0.2.3/.codecov.yml` & `klepto-0.2.4/.codecov.yml`

 * *Files identical despite different names*

### Comparing `klepto-0.2.3/.coveragerc` & `klepto-0.2.4/.coveragerc`

 * *Files identical despite different names*

### Comparing `klepto-0.2.3/LICENSE` & `klepto-0.2.4/LICENSE`

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

### Comparing `klepto-0.2.3/PKG-INFO` & `klepto-0.2.4/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: klepto
-Version: 0.2.3
+Version: 0.2.4
 Summary: persistent caching to memory, disk, or database
 Home-page: https://github.com/uqfoundation/klepto
 Download-URL: https://pypi.org/project/klepto/#files
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
 Classifier: Topic :: Database
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Software Development
 Requires-Python: >=3.7
 Provides-Extra: archives
@@ -37,34 +38,34 @@
 -------------------------------------------------------
 klepto: persistent caching to memory, disk, or database
 -------------------------------------------------------
 
 About Klepto
 ============
 
-``klepto`` extends python's ``lru_cache`` to utilize different keymaps and
+``klepto`` extends Python's ``lru_cache`` to utilize different keymaps and
 alternate caching algorithms, such as ``lfu_cache`` and ``mru_cache``.
 While caching is meant for fast access to saved results, ``klepto`` also
 has archiving capabilities, for longer-term storage. ``klepto`` uses a
 simple dictionary-sytle interface for all caches and archives, and all
-caches can be applied to any python function as a decorator. Keymaps
+caches can be applied to any Python function as a decorator. Keymaps
 are algorithms for converting a function's input signature to a unique
 dictionary, where the function's results are the dictionary value.
 Thus for ``y = f(x)``, ``y`` will be stored in ``cache[x]`` (e.g. ``{x:y}``).
 
 ``klepto`` provides both standard and *"safe"* caching, where *"safe"* caches
 are slower but can recover from hashing errors. ``klepto`` is intended
 to be used for distributed and parallel computing, where several of
 the keymaps serialize the stored objects. Caches and archives are
 intended to be read/write accessible from different threads and
 processes. ``klepto`` enables a user to decorate a function, save the
 results to a file or database archive, close the interpreter,
 start a new session, and reload the function and it's cache.
 
-``klepto`` is part of ``pathos``, a python framework for heterogeneous computing.
+``klepto`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``klepto`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/klepto/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
@@ -86,18 +87,18 @@
     - ``hdfdir_archive`` - a dictionary-style interface to a folder of hdf5 files
     - ``hdf_archive`` - a dictionary-style interface to a hdf5 file
     - ``dict_archive`` - a dictionary with an archive interface
     - ``null_archive`` - a dictionary-style interface to a dummy archive 
 
 ``klepto`` provides the following keymaps:
 
-    - ``keymap`` - keys are raw python objects
-    - ``hashmap`` - keys are a hash for the python object
-    - ``stringmap`` - keys are the python object cast as a string
-    - ``picklemap`` - keys are the serialized python object
+    - ``keymap`` - keys are raw Python objects
+    - ``hashmap`` - keys are a hash for the Python object
+    - ``stringmap`` - keys are the Python object cast as a string
+    - ``picklemap`` - keys are the serialized Python object
 
 ``klepto`` also includes a few useful decorators providing:
 
     - simple, shallow, or deep rounding of function arguments
     - cryptographic key generation, with masking of selected arguments
 
 
@@ -140,22 +141,22 @@
 Requirements
 ============
 
 ``klepto`` requires:
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
-    - ``dill``, **>=0.3.6**
-    - ``pox``, **>=0.3.2**
+    - ``dill``, **>=0.3.7**
+    - ``pox``, **>=0.3.3**
 
 Optional requirements:
 
     - ``h5py``, **>=2.8.0**
     - ``pandas``, **>=0.17.0**
-    - ``sqlalchemy``, **>=0.8.4**
+    - ``sqlalchemy``, **>=1.4.0**
     - ``jsonpickle``, **>=0.9.6**
     - ``cloudpickle``, **>=0.5.2**
 
 
 More Information
 ================
```

### Comparing `klepto-0.2.3/README.md` & `klepto-0.2.4/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,33 +1,33 @@
 klepto
-====
+======
 persistent caching to memory, disk, or database
 
 About Klepto
 ------------
-``klepto`` extends python's ``lru_cache`` to utilize different keymaps and
+``klepto`` extends Python's ``lru_cache`` to utilize different keymaps and
 alternate caching algorithms, such as ``lfu_cache`` and ``mru_cache``.
 While caching is meant for fast access to saved results, ``klepto`` also
 has archiving capabilities, for longer-term storage. ``klepto`` uses a
 simple dictionary-sytle interface for all caches and archives, and all
-caches can be applied to any python function as a decorator. Keymaps
+caches can be applied to any Python function as a decorator. Keymaps
 are algorithms for converting a function's input signature to a unique
 dictionary, where the function's results are the dictionary value.
 Thus for ``y = f(x)``, ``y`` will be stored in ``cache[x]`` (e.g. ``{x:y}``).
 
 ``klepto`` provides both standard and *"safe"* caching, where *"safe"* caches
 are slower but can recover from hashing errors. ``klepto`` is intended
 to be used for distributed and parallel computing, where several of
 the keymaps serialize the stored objects. Caches and archives are
 intended to be read/write accessible from different threads and
 processes. ``klepto`` enables a user to decorate a function, save the
 results to a file or database archive, close the interpreter,
 start a new session, and reload the function and it's cache.
 
-``klepto`` is part of ``pathos``, a python framework for heterogeneous computing.
+``klepto`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``klepto`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/klepto/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 --------------
 ``klepto`` has standard and *"safe"* variants of the following:
@@ -48,18 +48,18 @@
 * ``hdfdir_archive`` - a dictionary-style interface to a folder of hdf5 files
 * ``hdf_archive`` - a dictionary-style interface to a hdf5 file
 * ``dict_archive`` - a dictionary with an archive interface
 * ``null_archive`` - a dictionary-style interface to a dummy archive 
 
 ``klepto`` provides the following keymaps:
 
-* ``keymap`` - keys are raw python objects
-* ``hashmap`` - keys are a hash for the python object
-* ``stringmap`` - keys are the python object cast as a string
-* ``picklemap`` - keys are the serialized python object
+* ``keymap`` - keys are raw Python objects
+* ``hashmap`` - keys are a hash for the Python object
+* ``stringmap`` - keys are the Python object cast as a string
+* ``picklemap`` - keys are the serialized Python object
 
 ``klepto`` also includes a few useful decorators providing:
 
 * simple, shallow, or deep rounding of function arguments
 * cryptographic key generation, with masking of selected arguments
 
 
@@ -103,22 +103,22 @@
 
 Requirements
 ------------
 ``klepto`` requires:
 
 * ``python`` (or ``pypy``), **>=3.7**
 * ``setuptools``, **>=42**
-* ``dill``, **>=0.3.6**
-* ``pox``, **>=0.3.2**
+* ``dill``, **>=0.3.7**
+* ``pox``, **>=0.3.3**
 
 Optional requirements:
 
 * ``h5py``, **>=2.8.0**
 * ``pandas``, **>=0.17.0**
-* ``sqlalchemy``, **>=0.8.4**
+* ``sqlalchemy``, **>=1.4.0**
 * ``jsonpickle``, **>=0.9.6**
 * ``cloudpickle``, **>=0.5.2**
 
 
 More Information
 ----------------
 Probably the best way to get started is to look at the documentation at
```

### Comparing `klepto-0.2.3/docs/Makefile` & `klepto-0.2.4/docs/Makefile`

 * *Files identical despite different names*

### Comparing `klepto-0.2.3/docs/source/conf.py` & `klepto-0.2.4/docs/source/conf.py`

 * *Files 10% similar despite different names*

```diff
@@ -48,24 +48,42 @@
 # source_suffix = ['.rst', '.md']
 source_suffix = '.rst'
 
 # The master toctree document.
 master_doc = 'index'
 
 # General information about the project.
-project = u'klepto'
+project = 'klepto'
 year = datetime.now().year
-copyright = u'%d, The Uncertainty Quantification Foundation' % year
-author = u'Mike McKerns'
+copyright = '%d, The Uncertainty Quantification Foundation' % year
+author = 'Mike McKerns'
 
 # extension config
 github_project_url = "https://github.com/uqfoundation/klepto"
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
@@ -77,15 +95,15 @@
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
@@ -105,57 +123,63 @@
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
     'github_repo': 'klepto',
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
 htmlhelp_basename = 'kleptodoc'
 
 # Logo for sidebar
@@ -182,45 +206,45 @@
     # 'figure_align': 'htbp',
 }
 
 # Grouping the document tree into LaTeX files. List of tuples
 # (source start file, target name, title,
 #  author, documentclass [howto, manual, or own class]).
 latex_documents = [
-    (master_doc, 'klepto.tex', u'klepto Documentation',
-     u'Mike McKerns', 'manual'),
+    (master_doc, 'klepto.tex', 'klepto Documentation',
+     'Mike McKerns', 'manual'),
 ]
 
 
 # -- Options for manual page output ---------------------------------------
 
 # One entry per manual page. List of tuples
 # (source start file, name, description, authors, manual section).
 man_pages = [
-    (master_doc, 'klepto', u'klepto Documentation',
+    (master_doc, 'klepto', 'klepto Documentation',
      [author], 1)
 ]
 
 
 # -- Options for Texinfo output -------------------------------------------
 
 # Grouping the document tree into Texinfo files. List of tuples
 # (source start file, target name, title, author,
 #  dir menu entry, description, category)
 texinfo_documents = [
-    (master_doc, 'klepto', u'klepto Documentation',
+    (master_doc, 'klepto', 'klepto Documentation',
      author, 'klepto', 'Persistent caching to memory, disk, or database.',
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

### Comparing `klepto-0.2.3/docs/source/pathos.png` & `klepto-0.2.4/docs/source/pathos.png`

 * *Files identical despite different names*

### Comparing `klepto-0.2.3/klepto/__info__.py` & `klepto-0.2.4/klepto/__info__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,41 +1,41 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 '''
 -------------------------------------------------------
 klepto: persistent caching to memory, disk, or database
 -------------------------------------------------------
 
 About Klepto
 ============
 
-``klepto`` extends python's ``lru_cache`` to utilize different keymaps and
+``klepto`` extends Python's ``lru_cache`` to utilize different keymaps and
 alternate caching algorithms, such as ``lfu_cache`` and ``mru_cache``.
 While caching is meant for fast access to saved results, ``klepto`` also
 has archiving capabilities, for longer-term storage. ``klepto`` uses a
 simple dictionary-sytle interface for all caches and archives, and all
-caches can be applied to any python function as a decorator. Keymaps
+caches can be applied to any Python function as a decorator. Keymaps
 are algorithms for converting a function's input signature to a unique
 dictionary, where the function's results are the dictionary value.
 Thus for ``y = f(x)``, ``y`` will be stored in ``cache[x]`` (e.g. ``{x:y}``).
 
 ``klepto`` provides both standard and *"safe"* caching, where *"safe"* caches
 are slower but can recover from hashing errors. ``klepto`` is intended
 to be used for distributed and parallel computing, where several of
 the keymaps serialize the stored objects. Caches and archives are
 intended to be read/write accessible from different threads and
 processes. ``klepto`` enables a user to decorate a function, save the
 results to a file or database archive, close the interpreter,
 start a new session, and reload the function and it's cache.
 
-``klepto`` is part of ``pathos``, a python framework for heterogeneous computing.
+``klepto`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``klepto`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/klepto/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
@@ -57,18 +57,18 @@
     - ``hdfdir_archive`` - a dictionary-style interface to a folder of hdf5 files
     - ``hdf_archive`` - a dictionary-style interface to a hdf5 file
     - ``dict_archive`` - a dictionary with an archive interface
     - ``null_archive`` - a dictionary-style interface to a dummy archive 
 
 ``klepto`` provides the following keymaps:
 
-    - ``keymap`` - keys are raw python objects
-    - ``hashmap`` - keys are a hash for the python object
-    - ``stringmap`` - keys are the python object cast as a string
-    - ``picklemap`` - keys are the serialized python object
+    - ``keymap`` - keys are raw Python objects
+    - ``hashmap`` - keys are a hash for the Python object
+    - ``stringmap`` - keys are the Python object cast as a string
+    - ``picklemap`` - keys are the serialized Python object
 
 ``klepto`` also includes a few useful decorators providing:
 
     - simple, shallow, or deep rounding of function arguments
     - cryptographic key generation, with masking of selected arguments
 
 
@@ -111,22 +111,22 @@
 Requirements
 ============
 
 ``klepto`` requires:
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
-    - ``dill``, **>=0.3.6**
-    - ``pox``, **>=0.3.2**
+    - ``dill``, **>=0.3.7**
+    - ``pox``, **>=0.3.3**
 
 Optional requirements:
 
     - ``h5py``, **>=2.8.0**
     - ``pandas``, **>=0.17.0**
-    - ``sqlalchemy``, **>=0.8.4**
+    - ``sqlalchemy``, **>=1.4.0**
     - ``jsonpickle``, **>=0.9.6**
     - ``cloudpickle``, **>=0.5.2**
 
 
 More Information
 ================
 
@@ -152,36 +152,36 @@
     https://uqfoundation.github.io/project/pathos
 
 Please see https://uqfoundation.github.io/project/pathos or
 http://arxiv.org/pdf/1202.1056 for further information.
 
 '''
 
-__version__ = '0.2.3'
+__version__ = '0.2.4'
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

### Comparing `klepto-0.2.3/klepto/__init__.py` & `klepto-0.2.4/klepto/__init__.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 # author, version, license, and long description
 try: # the package is installed
     from .__info__ import __version__, __author__, __doc__, __license__
 except: # pragma: no cover
```

### Comparing `klepto-0.2.3/klepto/_abc.py` & `klepto-0.2.4/klepto/_abc.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2021-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2021-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 """
 base class for archive to memory, file, or database
 """
 class archive(dict):
     """dictionary with an archive interface"""
```

### Comparing `klepto-0.2.3/klepto/_archives.py` & `klepto-0.2.4/klepto/_archives.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,47 +1,44 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 """
 custom caching dict, which archives results to memory, file, or database
 """
 import os
 import sys
 import shutil
 from random import random
 from pickle import PROTO, STOP
 from collections.abc import KeysView, ValuesView, ItemsView
-import imp
-try:
-  imp.find_module('sqlalchemy')
+from importlib import util as imp
+if imp.find_spec('sqlalchemy'):
   sql = True
   def __import_sql__():
       global sql
       import sqlalchemy as sql
-except ImportError:
+else:
   sql = None
-try:
-  imp.find_module('h5py')
+if imp.find_spec('h5py'):
   hdf = True
   def __import_hdf__():
       global hdf, np
       import h5py as hdf
-except ImportError:
+else:
   hdf = None
-try:
-  imp.find_module('pandas')
+if imp.find_spec('pandas'):
   pandas = True
   def __import_pandas__():
       global pandas
       import pandas
-except ImportError:
+else:
   pandas = None
 import json
 import dill
 from dill.source import getimportable
 from pox import mkdir, rmtree, walk
 from ._abc import archive
 from .crypto import hash
@@ -117,16 +114,16 @@
 
 
 class cache(dict):
     """dictionary augmented with an archive backend"""
     def __init__(self, *args, **kwds):
         """initialize a dictionary with an archive backend
 
-    Additional Inputs:
-        archive: instance of archive object
+    Args:
+        archive (archive, default=null_archive()): instance of archive object
         """
         self.__swap__ = null_archive()
         self.__archive__ = kwds.pop('archive', null_archive())
         dict.__init__(self, *args, **kwds)
        #self.__state__ = {}
         return
     def __repr__(self):
@@ -288,30 +285,29 @@
 
 
 class dir_archive(archive):
     """dictionary-style interface to a folder of files"""
     def __init__(self, dirname=None, serialized=True, compression=0, permissions=None, **kwds):
         """initialize a file folder with a synchronized dictionary interface
 
-    Inputs:
-        dirname: name of the root archive directory [default: memo]
-        serialized: if True, pickle file contents; otherwise save python objects
-        compression: compression level (0 to 9) [default: 0 (no compression)]
-        permissions: octal representing read/write permissions [default: 0o775]
-        memmode: access mode for files, one of {None, 'r+', 'r', 'w+', 'c'}
-        memsize: approximate size (in MB) of cache for in-memory compression
-        protocol: pickling protocol [default: None (use the default protocol)]
+    Args:
+        dirname (str, default='memo'): path of the archive root directory
+        serialized (bool, default=True): save python objects in pickled files
+        compression (int, default=0): compression level (0 to 9), 0 is None
+        permissions (octal, default=0o775): read/write permission indicator
+        memmode (str, default=None): mode, one of ``{None, 'r+', 'r', 'w+', 'c'}``
+        memsize (int, default=100): size (MB) of cache for in-memory compression
+        protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
         """
         #XXX: if compression or mode is given, use joblib-style pickling
         #     (ignoring 'serialized'); else if serialized, use dill unless
         #     fast=True (then use joblib-style pickling), or protocol='json'
         #     (then use json-style pickling). If not serialized, then write
         #     raw objects and load objects with import. Also, if fast=True
         #     and protocol='json', the use protocol=None. #FIXME: needs doc
-        """dirname = full filepath"""
         if dirname is None: #FIXME: default root as /tmp or something better
             dirname = 'memo' #FIXME: need better default
         # set state
         self.__state__ = {
             # undocumented: True=joblib-style, False=dill-style pickling
             'fast': kwds.get('fast', False),
             # settings
@@ -443,15 +439,15 @@
         except:
             memo = {}
         res = memo.pop(key, *value)
         return res
     pop.__doc__ = dict.pop.__doc__
     def popitem(self):
         key = self.__iter__()
-        try: key = key.next()
+        try: key = next(key)
         except StopIteration: raise KeyError("popitem(): dictionary is empty")
         return (key, self.pop(key))
     popitem.__doc__ = dict.popitem.__doc__
     def setdefault(self, key, *value):
         res = self.get(key, *value)
         self.__setitem__(key, res)
         return res
@@ -643,20 +639,19 @@
 
 
 class file_archive(archive):
     """dictionary-style interface to a file"""
     def __init__(self, filename=None, serialized=True, **kwds): # False
         """initialize a file with a synchronized dictionary interface
 
-    Inputs:
-        filename: name of the file backend [default: memo.pkl or memo.py]
-        serialized: if True, pickle file contents; otherwise save python objects
-        protocol: pickling protocol [default: None (use the default protocol)]
+    Args:
+        filename (str, default='memo.pkl'): path of the file archive
+        serialized (bool, default=True): save python objects in pickled file
+        protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
         """
-        """filename = full filepath"""
         #FIXME: (needs doc) if protocol='json', use the json serializer
         protocol = kwds.get('protocol', None)
         if filename is None: #XXX: need better default filename?
             if serialized:
                 filename = 'memo.json' if type(protocol) is str else 'memo.pkl'
             else: filename = 'memo.py'
         elif not serialized and not filename.endswith(('.py','.pyc','.pyo','.pyd')): filename = filename+'.py'
@@ -876,18 +871,18 @@
       in the current directory, database='sqlite:///foo.db'.  To use a mysql
       database 'foo' on localhost, database='mysql://user:pass@localhost/foo'.
       For postgresql, use database='postgresql://user:pass@localhost/foo'. 
       When connecting to sqlite, the default database is ':memory:'; otherwise,
       the default database is 'defaultdb'.  Allows keyword options for database
       configuration, such as connection pooling.
 
-      Inputs:
-          database: url of the database backend [default: sqlite:///:memory:]
-          serialized: if True, pickle table contents; otherwise cast as strings
-          protocol: pickling protocol [default: None (use the default protocol)]
+      Args:
+          database (str, default=None): database url (see above note)
+          serialized (bool, default=True): save objects as pickled strings
+          protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
           """
           #FIXME: (needs doc) if protocol='json', use the json serializer
           __import_sql__()
           # create database, if doesn't exist
           if database is None: database = 'sqlite:///:memory:'
           elif database == 'sqlite:///': database = 'sqlite:///:memory:'
           _database = database
@@ -906,34 +901,39 @@
               'serialized': bool(kwds.pop('serialized', True)),
               'id': _database,
               'protocol': kwds.pop('protocol', dill.DEFAULT_PROTOCOL),
               # preserve other settings (for copy)
               'config': kwds.pop('config', kwds.copy())
           } #XXX: _engine and _metadata (and _key and _val) also __state__ ?
           # get engine
+          kwds['future'] = True # 1.4 & 2.0
           if dbname == ':memory:':
               self._engine = sql.create_engine(url, **kwds)
           elif _database.startswith('sqlite'):
               self._engine = sql.create_engine(_database, **kwds)
           else:
-              self._engine = sql.create_engine(url) #XXX: **kwds ?
+              self._engine = sql.create_engine(url, future=True) #XXX: **kwds ?
               try:
-                  conn = self._engine.connect()
+                  self._conn = self._engine.connect()
                   if _database.startswith('postgres'):
-                      conn.connection.connection.set_isolation_level(0)
-                  conn.execute("CREATE DATABASE %s;" % dbname)
-              except Exception: pass
+                      self._conn.connection.connection.set_isolation_level(0)
+                  self._conn.execute(sql.text("CREATE DATABASE %s;" % dbname))
+                  self._conn.commit()
+              except Exception: self._conn = None
               finally:
                   if _database.startswith('postgres'):
-                      conn.connection.connection.set_isolation_level(1)
+                      self._conn.connection.connection.set_isolation_level(1)
               try:
-                  self._engine.execute("USE %s;" % dbname)
+                  if self._conn is None: self._conn = self._engine.connect()
+                  self._conn.execute(sql.text("USE %s;" % dbname))
+                  self._conn.commit()
               except Exception:
                   pass
               self._engine = sql.create_engine(_database, **kwds)
+          self._conn = self._engine.connect()
           # table internals
           self._metadata = sql.MetaData()
           self._key = 'Kkeyqwg907' # primary key name
           self._val = 'Kvalmol142' # object storage name
           # discover all tables #FIXME: with matching self._key
           keys = self._keys()
           [self._mktable(key) for key in keys]
@@ -944,30 +944,33 @@
 
       EXPERIMENTAL: For certain database engines, this may not work due
       to permission issues. Caller may need to be connected as a superuser
       and database owner.
           """
           _database = self.__state__['id']
           url, dbname = _database.rsplit('/', 1)
-          self._engine = sql.create_engine(url)
+          self._engine = sql.create_engine(url, future=True) # 1.4 & 2.0
           try:
-              conn = self._engine.connect()
+              self._conn = self._engine.connect()
               if _database.startswith('postgres'):
                   # these two commands require superuser privs
-                  conn.execute("update pg_database set datallowconn = 'false' WHERE datname = '%s';" % dbname)
-                  conn.execute("SELECT pg_terminate_backend(pid) FROM pg_stat_activity WHERE datname = '%s';" % dbname) # 'pid' used in postgresql >= 9.2
-                  conn.connection.connection.set_isolation_level(0)
-              conn.execute("DROP DATABASE %s;" % dbname) # must be db owner
+                  self._conn.execute(sql.text("update pg_database set datallowconn = 'false' WHERE datname = '%s';" % dbname))
+                  self._conn.commit()
+                  self._conn.execute(sql.text("SELECT pg_terminate_backend(pid) FROM pg_stat_activity WHERE datname = '%s';" % dbname)) # 'pid' used in postgresql >= 9.2
+                  self._conn.commit()
+                  self._conn.connection.connection.set_isolation_level(0)
+              self._conn.execute(sql.text("DROP DATABASE %s;" % dbname)) # must be db owner
+              self._conn.commit()
               if _database.startswith('postgres'):
-                  conn.connection.connection.set_isolation_level(1)
+                  self._conn.connection.connection.set_isolation_level(1)
           except Exception:
               dbpath = _database.split('///')[-1]
               if os.path.exists(dbpath): # else fail silently
                   os.remove(dbpath)
-          self._metadata = self._engine = None # self.__state__['table']=None
+          self._metadata = self._engine = self._conn = None # self.__state__['table']=None
           return
       def __asdict__(self):
           """build a dictionary containing the archive contents"""
           keys = self._keys()
           return dict((key,self.__getitem__(key)) for key in keys)
       #FIXME: missing __cmp__, __...__
       def __eq__(self, y):
@@ -984,19 +987,19 @@
           table = self._gettable(key)
           self._metadata.remove(table)
           table.drop(self._engine) #XXX: optionally delete data ?
           return
       __delitem__.__doc__ = dict.__delitem__.__doc__
       def __getitem__(self, key): #XXX: value is table['key','key']; slow?
           table = self._gettable(key)
-          query = sql.select([table],table.c[self._key] == self._key)#XXX: slow?
-          row = self._engine.execute(query).fetchone()
+          query = sql.select(table).where(table.c[self._key] == self._key)#XXX: slow?
+          row = self._conn.execute(query).fetchone()
           if row is None:
               raise RuntimeError("primary key for '%s' not found" % key)
-          return row[self._val]
+          return row._mapping[self._val]
       __getitem__.__doc__ = dict.__getitem__.__doc__
       def __repr__(self):
           return "sql_archive('%s', %s, cached=False)" % (self.name, self.__asdict__())
       __repr__.__doc__ = dict.__repr__.__doc__
       def __setitem__(self, key, value): #XXX: _setkey is part of _mktable
           value = {self._val: value}
           try:
@@ -1004,15 +1007,16 @@
               query = table.update().where(table.c[self._key] == self._key)
               values = value
           except KeyError:
               table = self._mktable(key)
               query = table.insert()
               values = {self._key: self._key}
               values.update(value)
-          self._engine.execute(query.values(**values))
+          self._conn.execute(query.values(**values))
+          self._conn.commit()
           return
       __setitem__.__doc__ = dict.__setitem__.__doc__
       def clear(self):
          #self._metadata.drop_all()
           for key in self._keys():
               try: self.__delitem__(key) #XXX: optionally delete data ?
               except: pass #XXX: don't catch ?
@@ -1066,15 +1070,15 @@
           except:
               memo = {}
           res = memo.pop(key, *value)
           return res
       pop.__doc__ = dict.pop.__doc__
       def popitem(self):
           key = self.__iter__()
-          try: key = key.next()
+          try: key = next(key)
           except StopIteration: raise KeyError("popitem(): dictionary is empty")
           return (key, self.pop(key))
       popitem.__doc__ = dict.popitem.__doc__
       def setdefault(self, key, *value):
           res = self.get(key, *value)
           self.__setitem__(key, res)
           return res
@@ -1119,15 +1123,16 @@
           # if you are here... raise a KeyError
           tables = {}
           return tables[table]
       def _keys(self, meta=False):
           "get a list of tables in the database" #FIXME: with matching self._key
           if meta: return self._metadata.tables.keys()
           # look at all the tables in the database
-          names = self._engine.table_names()
+          inspector = sql.inspect(self._engine)
+          names = inspector.get_table_names()
           names = [str(name) for name in names]
           # clean up metadata by removing stale tables
           tables = set(self._metadata.tables.keys()) - set(names) #XXX: slow?
           tables = [self._gettable(key, meta=True) for key in tables]
           [self._metadata.remove(key) for key in tables]
           return names
       def _tables(self, meta=False):
@@ -1160,19 +1165,19 @@
       in the current directory, database='sqlite:///foo.db'.  To use a mysql
       database 'foo' on localhost, database='mysql://user:pass@localhost/foo'.
       For postgresql, use database='postgresql://user:pass@localhost/foo'. 
       When connecting to sqlite, the default database is ':memory:'; otherwise,
       the default database is 'defaultdb'.  Allows keyword options for database
       configuration, such as connection pooling.
 
-      Inputs:
-          database: url of the database backend [default: sqlite:///:memory:]
-          table: name of the associated database table [default: 'memo']
-          serialized: if True, pickle table contents; otherwise cast as strings
-          protocol: pickling protocol [default: None (use the default protocol)]
+      Args:
+          database (str, default=None): database url (see above note)
+          table (str, default='memo'): name of the associated database table
+          serialized (bool, default=True): save objects as pickled strings
+          protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
           """
           #FIXME: (needs doc) if protocol='json', use the json serializer
           __import_sql__()
           if table is None: table = 'memo' #XXX: better random unique id ?
           # create database, if doesn't exist
           if database is None: database = 'sqlite:///:memory:'
           elif database == 'sqlite:///': database = 'sqlite:///:memory:'
@@ -1194,34 +1199,39 @@
               'root': _database,
               'id': table,
               'protocol': kwds.pop('protocol', dill.DEFAULT_PROTOCOL),
               # preserve other settings (for copy)
               'config': kwds.pop('config', kwds.copy())
           } #XXX: _engine and _metadata (and _key and _val) also __state__ ?
           # get engine
+          kwds['future'] = True # 1.4 & 2.0
           if dbname == ':memory:':
               self._engine = sql.create_engine(url, **kwds)
           elif _database.startswith('sqlite'):
               self._engine = sql.create_engine(_database, **kwds)
           else:
-              self._engine = sql.create_engine(url) #XXX: **kwds ?
+              self._engine = sql.create_engine(url, future=True) #XXX: **kwds ?
               try:
-                  conn = self._engine.connect()
+                  self._conn = self._engine.connect()
                   if _database.startswith('postgres'):
-                      conn.connection.connection.set_isolation_level(0)
-                  conn.execute("CREATE DATABASE %s;" % dbname)
-              except Exception: pass
+                      self._conn.connection.connection.set_isolation_level(0)
+                  self._conn.execute(sql.text("CREATE DATABASE %s;" % dbname))
+                  self._conn.commit()
+              except Exception: self._conn = None
               finally:
                   if _database.startswith('postgres'):
-                      conn.connection.connection.set_isolation_level(1)
+                      self._conn.connection.connection.set_isolation_level(1)
               try:
-                  self._engine.execute("USE %s;" % dbname)
+                  if self._conn is None: self._conn = self._engine.connect()
+                  self._conn.execute(sql.text("USE %s;" % dbname))
+                  self._conn.commit()
               except Exception:
                   pass
               self._engine = sql.create_engine(_database, **kwds)
+          self._conn = self._engine.connect()
           # prepare to create table
           self._metadata = sql.MetaData()
           self._key = 'Kkey' # primary key name
           self._val = 'Kval' # object storage name
           keytype = sql.String(255) #XXX: other better fixed size?
           if self.__state__['serialized']:
               proto = self.__state__['protocol']
@@ -1253,50 +1263,55 @@
           if not bool(kwds.get('database', False)):
               self.__state__['id'].drop(self._engine) #XXX: or delete data ?
               self._metadata.remove(self.__state__['id'])
               self._metadata = self._engine = self.__state__['id'] = None
               return
           _database = self.__state__['root']
           url, dbname = _database.rsplit('/', 1)
-          self._engine = sql.create_engine(url)
+          self._engine = sql.create_engine(url, future=True) # 1.4 & 2.0
           try:
-              conn = self._engine.connect()
+              self._conn = self._engine.connect()
               if _database.startswith('postgres'):
                   # these two commands require superuser privs
-                  conn.execute("update pg_database set datallowconn = 'false' WHERE datname = '%s';" % dbname)
-                  conn.execute("SELECT pg_terminate_backend(pid) FROM pg_stat_activity WHERE datname = '%s';" % dbname) # 'pid' used in postgresql >= 9.2
-                  conn.connection.connection.set_isolation_level(0)
-              conn.execute("DROP DATABASE %s;" % dbname) # must be db owner
+                  self._conn.execute(sql.text("update pg_database set datallowconn = 'false' WHERE datname = '%s';" % dbname))
+                  self._conn.commit()
+                  self._conn.execute(sql.text("SELECT pg_terminate_backend(pid) FROM pg_stat_activity WHERE datname = '%s';" % dbname)) # 'pid' used in postgresql >= 9.2
+                  self._conn.commit()
+                  self._conn.connection.connection.set_isolation_level(0)
+              self._conn.execute(sql.text("DROP DATABASE %s;" % dbname)) # must be db owner
+              self._conn.commit()
               if _database.startswith('postgres'):
-                  conn.connection.connection.set_isolation_level(1)
+                  self._conn.connection.connection.set_isolation_level(1)
           except Exception:
               dbpath = _database.split('///')[-1]
               if os.path.exists(dbpath): # else fail silently
                   os.remove(dbpath)
-          self._metadata = self._engine = self.__state__['id'] = None
+          self._metadata = self._engine = self._conn = self.__state__['id'] = None
           return
       def __len__(self):
-          query = self.__state__['id'].count()
-          return int(self._engine.execute(query).scalar())
+          from sqlalchemy import orm
+          session = orm.sessionmaker(bind=self._engine, future=True)() # 1.4 & 2.0
+          return int(session.query(self.__state__['id']).count())
       def __contains__(self, key):
-          query = sql.select([self._key], self._key == key)
-          row = self._engine.execute(query).fetchone()
+          query = sql.select(self._key).where(self._key == key)
+          row = self._conn.execute(query).fetchone()
           return row is not None
       __contains__.__doc__ = dict.__contains__.__doc__
       def __setitem__(self, key, value):
           value = {self._val: value} #XXX: force into single item dict...?
           table = self.__state__['id']
           if key in self:
               values = value
               query = table.update().where(self._key == key)
           else:
               values = {self._key.name: key}
               values.update(value)
               query = table.insert()
-          self._engine.execute(query.values(**values))
+          self._conn.execute(query.values(**values))
+          self._conn.commit()
           return
       __setitem__.__doc__ = dict.__setitem__.__doc__
       #FIXME: missing __cmp__, __...__
       def __eq__(self, y):
           try:
               if y.__module__ != self.__module__: return NotImplemented
               return self.__asdict__() == y.__asdict__() #XXX: faster than get?
@@ -1318,41 +1333,43 @@
           try: self.pop(key) #FIXME: faster without value lookup
           except KeyError:
               memo = {}
               memo.__delitem__(key)
           return
       __delitem__.__doc__ = dict.__delitem__.__doc__
       def __getitem__(self, key):
-          query = sql.select([self.__state__['id']], self._key == key)
-          row = self._engine.execute(query).fetchone()
+          query = sql.select(self.__state__['id']).where(self._key == key)
+          row = self._conn.execute(query).fetchone()
           if row is None: raise KeyError(key)
-          return row[self._val]
+          return row._mapping[self._val]
       __getitem__.__doc__ = dict.__getitem__.__doc__
       def __iter__(self): #XXX: should be dictionary-keyiterator
-          query = sql.select([self._key])
-          result = self._engine.execute(query)
+          query = sql.select(self._key)
+          result = self._conn.execute(query)
           for row in result:
               yield row[0]
       __iter__.__doc__ = dict.__iter__.__doc__
       def get(self, key, value=None):
-          query = sql.select([self.__state__['id']], self._key == key)
-          row = self._engine.execute(query).fetchone()
+          query = sql.select(self.__state__['id']).where(self._key == key)
+          row = self._conn.execute(query).fetchone()
           if row != None:
-              _value = row[self._val]
+              _value = row._mapping[self._val]
           else: _value = value
           return _value
       get.__doc__ = dict.get.__doc__
       def clear(self):
           query = self.__state__['id'].delete()
-          self._engine.execute(query)
+          self._conn.execute(query)
+          self._conn.commit()
           return
       clear.__doc__ = dict.clear.__doc__
      #def insert(self, d): #XXX: don't allow this method, or hide ?
      #    query = self.__state__['id'].insert(d)
-     #    self._engine.execute(query)
+     #    self._conn.execute(query)
+     #    self._conn.commit()
      #    return
       def copy(self, name=None): #XXX: always None? or allow other settings?
           "D.copy(name) -> a copy of D, with a new archive at the given name"
           if name is None: name = self.name
           else: pass #FIXME: copy database/table instead of do update below
           db,table = _sqlname(name)
           #FIXME: should reference, not copy
@@ -1387,39 +1404,40 @@
           memo = self.fromkeys(self.keys()) # 'shadow' dict
           [memo.pop(k) for k in keys]
           return [self.pop(k) for k in keys]
       def pop(self, key, *value):
           L = len(value)
           if L > 1:
               raise TypeError("pop expected at most 2 arguments, got %s" % str(L+1))
-          query = sql.select([self.__state__['id']], self._key == key)
-          row = self._engine.execute(query).fetchone()
+          query = sql.select(self.__state__['id']).where(self._key == key)
+          row = self._conn.execute(query).fetchone()
           if row != None:
-              _value = row[self._val]
+              _value = row._mapping[self._val]
           else:
               if not L: raise KeyError(key)
               _value = value[0]
-          query = sql.delete(self.__state__['id'], self._key == key)
-          self._engine.execute(query)
+          query = sql.delete(self.__state__['id']).where(self._key == key)
+          self._conn.execute(query)
+          self._conn.commit()
           return _value
       pop.__doc__ = dict.pop.__doc__
       def popitem(self):
           key = self.__iter__()
-          try: key = key.next()
+          try: key = next(key)
           except StopIteration: raise KeyError("popitem(): dictionary is empty")
           return (key, self.pop(key))
       popitem.__doc__ = dict.popitem.__doc__
       def setdefault(self, key, *value):
           L = len(value)
           if L > 1:
               raise TypeError("setvalue expected at most 2 arguments, got %s" % str(L+1))
-          query = sql.select([self.__state__['id']], self._key == key)
-          row = self._engine.execute(query).fetchone()
+          query = sql.select(self.__state__['id']).where(self._key == key)
+          row = self._conn.execute(query).fetchone()
           if row != None:
-              _value = row[self._val]
+              _value = row._mapping[self._val]
           else:
               if not L: _value = None
               else: _value = value[0]
               self.__setitem__(key, _value)
           return _value
       setdefault.__doc__ = dict.setdefault.__doc__
       def update(self, adict, **kwds):
@@ -1454,17 +1472,17 @@
       selected database url. For example, to use a sqlite database 'foo.db'
       in the current directory, database='sqlite:///foo.db'.  To use a mysql
       or postgresql database, sqlalchemy must be installed.  When connecting
       to sqlite, the default database is ':memory:'.  Storable values are
       limited to strings, integers, floats, and other basic objects.  To store
       functions, classes, and similar constructs, sqlalchemy must be installed.
 
-      Inputs:
-          database: url of the database backend [default: sqlite:///:memory:]
-          table: name of the associated database table [default: 'memo']
+      Args:
+          database (str, default=None): database url (see above note)
+          table (str, default='memo'): name of the associated database table
           """
           import sqlite3 as db
           if table is None: table = 'memo'
           # create database, if doesn't exist
           if database is None: database = 'sqlite:///:memory:'
           elif database == 'sqlite:///': database = 'sqlite:///:memory:'
           _database = database
@@ -1628,15 +1646,15 @@
           sql = "delete from %s where argstr = ?" % self.__state__['id']
           self._engine.execute(sql, (key,))
           self._conn.commit()
           return _value 
       pop.__doc__ = dict.pop.__doc__
       def popitem(self):
           key = self.__iter__()
-          try: key = key.next()
+          try: key = next(key)
           except StopIteration: raise KeyError("popitem(): dictionary is empty")
           return (key, self.pop(key))
       popitem.__doc__ = dict.popitem.__doc__
       def setdefault(self, key, *value):
           L = len(value)
           if L > 1:
               raise TypeError("setvalue expected at most 2 arguments, got %s" % str(L+1))
@@ -1678,19 +1696,19 @@
 
 if hdf:
   class hdf_archive(archive):
       """dictionary-style interface to a hdf5 file"""
       def __init__(self, filename=None, serialized=True, **kwds):
           """initialize a hdf5 file with a synchronized dictionary interface
 
-      Inputs:
-          filename: name of the file backend [default: memo.hdf5]
-          serialized: if True, pickle hdf entries; otherwise save python objects
-          protocol: pickling protocol [default: None (use the default protocol)]
-          meta: if True, store as file root metadata; otherwise store in datasets
+      Args:
+          filename (str, default='memo.hdf5'): path of the file archive
+          serialized (bool, default=True): pickle saved python objects
+          protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
+          meta (bool, default=False): store in root metadata (not in dataset)
           """
           #FIXME: (needs doc) if protocol='json', use the json serializer
           __import_hdf__()
           if filename is None: filename = 'memo.hdf5'
           elif not filename.endswith(('.hdf5','.hdf','.h5')): filename = filename+'.hdf5'
           # set state
           meta = kwds.get('meta', False)
@@ -1958,20 +1976,20 @@
       pass
 
   class hdfdir_archive(archive):
       """dictionary-style interface to a folder of hdf5 files"""
       def __init__(self, dirname=None, serialized=True, **kwds):
           """initialize a hdf5 file with a synchronized dictionary interface
 
-      Inputs:
-          dirname: name of the root archive directory [default: memo]
-          serialized: if True, pickle hdf entries; otherwise save python objects
-          permissions: octal representing read/write permissions [default: 0o775]
-          protocol: pickling protocol [default: None (use the default protocol)]
-          meta: if True, store as file root metadata; otherwise store in datasets
+      Args:
+          dirname (str, default='memo'): path of the archive root directory
+          serialized (bool, default=True): pickle saved python objects
+          permissions (octal, default=0o775): read/write permission indicator
+          protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
+          meta (bool, default=False): store in root metadata (not in dataset)
           """
           #FIXME: (needs doc) if protocol='json', use the json serializer
           __import_hdf__()
           if dirname is None: #FIXME: default root as /tmp or something better
               dirname = 'memo' #FIXME: need better default
           # set state
           meta = kwds.get('meta', False)
@@ -2083,15 +2101,15 @@
           except:
               memo = {}
           res = memo.pop(key, *value)
           return res
       pop.__doc__ = dict.pop.__doc__
       def popitem(self):
           key = self.__iter__()
-          try: key = key.next()
+          try: key = next(key)
           except StopIteration: raise KeyError("popitem(): dictionary is empty")
           return (key, self.pop(key))
       popitem.__doc__ = dict.popitem.__doc__
       def setdefault(self, key, *value):
           res = self.get(key, *value)
           self.__setitem__(key, res)
           return res
```

### Comparing `klepto-0.2.3/klepto/_cache.py` & `klepto-0.2.4/klepto/_cache.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #
 # code inspired by Raymond Hettinger's LFU and LRU cache decorators
 # on http://code.activestate.com/recipes/498245-lru-and-lfu-cache-decorators
 # and subsequent forks as well as the version available in python3.3
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 """
 a selection of caching decorators
 """
 from functools import update_wrapper, partial
 from klepto.archives import cache as archive_dict
```

### Comparing `klepto-0.2.3/klepto/_inspect.py` & `klepto-0.2.4/klepto/_inspect.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 #FIXME: klepto's caches ignore names/index, however ignore should be in keymap
 
 import inspect
 from klepto.tools import IS_PYPY
@@ -82,16 +82,19 @@
     identified = False
     if not inspect.ismethod(func) and not inspect.isfunction(func):
         try: # then it could be a partial...
             p_args = func.args           # list of default arg values
             p_kwds = func.keywords or {} # dict of default kwd values
             func = func.func
             identified = True
-        except AttributeError: #XXX: anything else to try? No? Give up.
-            pass
+        except AttributeError:
+            if hasattr(func, '__call__') and not hasattr(func, '__name__'):
+                func = func.__call__ # treat callable instance as __call__
+            else: #XXX: anything else to try? No? Give up.
+                pass
     if not identified:
         p_args = ()
         p_kwds = {}
 
     FULL_ARGS = hasattr(inspect, 'getfullargspec')
     try:
         if FULL_ARGS: arg_spec = inspect.getfullargspec(func)
@@ -193,16 +196,19 @@
         try: # then it could be a partial...
             p_args = func.args           # list of default arg values
             p_kwds = func.keywords or {} # dict of default kwd values
             p_named,p_defaults = signature(func.func, markup=False, variadic=False)
             func = func.func
             p_required = set(p_named) - set(p_defaults)
             identified = True
-        except AttributeError: #XXX: anything else to try? No? Give up.
-            pass
+        except AttributeError:
+            if hasattr(func, '__call__') and not hasattr(func, '__name__'):
+                func = func.__call__ # treat callable instance as __call__
+            else: #XXX: anything else to try? No? Give up.
+                pass
     if not identified:
         p_args = p_named = ()
         p_kwds = p_defaults = {}
         p_required = set()
 
     # get bad args/kwds from markup
     bad_args = set(i.strip('!') for i in named if i.startswith('!'))
```

### Comparing `klepto-0.2.3/klepto/_pickle.py` & `klepto-0.2.4/klepto/_pickle.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 # Author: Gael Varoquaux <gael dot varoquaux at normalesup dot org>
 # Copyright (c) 2009 Gael Varoquaux
 # License: BSD Style, 3 clauses.
 
 # Forked by: Mike McKerns (December 2013)
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 """
 Utilities for fast persistence of big data, with optional compression.
 """
 
 import traceback
```

### Comparing `klepto-0.2.3/klepto/archives.py` & `klepto-0.2.4/klepto/archives.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 """
 custom caching dict, which archives results to memory, file, or database
 """
 from ._archives import cache, archive
 from ._archives import dict_archive as _dict_archive
@@ -23,18 +23,18 @@
            'file_archive','sql_archive','sqltable_archive',\
            'hdf_archive','hdfdir_archive']
 
 class dict_archive(_dict_archive):
     def __new__(dict_archive, name=None, dict=None, cached=True, **kwds):
         """initialize a dictionary with an in-memory dictionary archive backend
 
-    Inputs:
-        name: (optional) identifier string [default: None]
-        dict: initial dictionary to seed the archive
-        cached: if True, use an in-memory cache interface to the archive
+    Args:
+        name (str, default=None): (optional) identifier string
+        dict (dict, default={}): initial dictionary to seed the archive
+        cached (bool, default=True): interact through an in-memory cache
         """
         if dict is None: dict = {}
         archive = _dict_archive()
         archive.__state__['id'] = None if name is None else str(name)
         if cached: archive = cache(archive=archive)
         archive.update(dict)
         return archive
@@ -48,18 +48,18 @@
         return _from_frame(dataframe)
     pass
 
 class null_archive(_null_archive):
     def __new__(null_archive, name=None, dict=None, cached=True, **kwds):
         """initialize a dictionary with a permanently-empty archive backend
 
-    Inputs:
-        name: (optional) identifier string [default: None]
-        dict: initial dictionary to seed the archive
-        cached: if True, use an in-memory cache interface to the archive
+    Args:
+        name (str, default=None): (optional) identifier string
+        dict (dict, default={}): initial dictionary to seed the archive
+        cached (bool, default=True): interact through an in-memory cache
         """
         if dict is None: dict = {}
         archive = _null_archive()
         archive.__state__['id'] = None if name is None else str(name)
         if cached: archive = cache(archive=archive)
         archive.update(dict)
         return archive
@@ -73,24 +73,24 @@
         return _from_frame(dataframe)
     pass
 
 class dir_archive(_dir_archive):
     def __new__(dir_archive, name=None, dict=None, cached=True, **kwds):
         """initialize a dictionary with a file-folder archive backend
 
-    Inputs:
-        name: name of the root archive directory [default: memo]
-        dict: initial dictionary to seed the archive
-        cached: if True, use an in-memory cache interface to the archive
-        serialized: if True, pickle file contents; otherwise save python objects
-        compression: compression level (0 to 9) [default: 0 (no compression)]
-        permissions: octal representing read/write permissions [default: 0o775]
-        memmode: access mode for files, one of {None, 'r+', 'r', 'w+', 'c'}
-        memsize: approximate size (in MB) of cache for in-memory compression
-        protocol: pickling protocol [default: None (use the default protocol)]
+    Args:
+        name (str, default='memo'): path of the archive root directory
+        dict (dict, default={}): initial dictionary to seed the archive
+        cached (bool, default=True): interact through an in-memory cache
+        serialized (bool, default=True): save python objects in pickled files
+        compression (int, default=0): compression level (0 to 9), 0 is None
+        permissions (octal, default=0o775): read/write permission indicator
+        memmode (str, default=None): mode, one of ``{None, 'r+', 'r', 'w+', 'c'}``
+        memsize (int, default=100): size (MB) of cache for in-memory compression
+        protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
         """
         if dict is None: dict = {}
         archive = _dir_archive(name, **kwds)
         if cached: archive = cache(archive=archive)
         archive.update(dict)
         return archive
 
@@ -103,20 +103,20 @@
         return _from_frame(dataframe)
     pass
 
 class file_archive(_file_archive):
     def __new__(file_archive, name=None, dict=None, cached=True, **kwds):
         """initialize a dictionary with a single file archive backend
 
-    Inputs:
-        name: name of the file archive [default: memo.pkl or memo.py]
-        dict: initial dictionary to seed the archive
-        cached: if True, use an in-memory cache interface to the archive
-        serialized: if True, pickle file contents; otherwise save python objects
-        protocol: pickling protocol [default: None (use the default protocol)]
+    Args:
+        name (str, default='memo.pkl'): path of the file archive
+        dict (dict, default={}): initial dictionary to seed the archive
+        cached (bool, default=True): interact through an in-memory cache
+        serialized (bool, default=True): save python objects in pickled file
+        protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
         """
         if dict is None: dict = {}
         archive = _file_archive(name, **kwds)
         if cached: archive = cache(archive=archive)
         archive.update(dict)
         return archive
 
@@ -143,20 +143,20 @@
     database?table=tablename; for example, name='sqlite:///foo.db?table=bar'.
     If not provided, the default tablename is 'memo'. If sqlalchemy is not
     installed, storable values are limited to strings, integers, floats, and
     other basic objects. If sqlalchemy is installed, additional keyword
     options can provide database configuration, such as connection pooling.
     To use a mysql or postgresql database, sqlalchemy must be installed.
 
-    Inputs:
-        name: url for the sql database and table [default: (see note above)]
-        dict: initial dictionary to seed the archive
-        cached: if True, use an in-memory cache interface to the archive
-        serialized: if True, pickle table contents; otherwise cast as strings
-        protocol: pickling protocol [default: None (use the default protocol)]
+    Args:
+        name (str, default=None): url for database table (see above note)
+        dict (dict, default={}): initial dictionary to seed the archive
+        cached (bool, default=True): interact through an in-memory cache
+        serialized (bool, default=True): save objects as pickled strings
+        protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
         """
         if dict is None: dict = {}
         db, table = _sqlname(name)
         archive = _sqltable_archive(db, table, **kwds)
         if cached: archive = cache(archive=archive)
         archive.update(dict)
         return archive
@@ -182,20 +182,20 @@
     When connecting to sqlite, the default database is ':memory:'; otherwise,
     the default database is 'defaultdb'. If sqlalchemy is not installed,
     storable values are limited to strings, integers, floats, and other
     basic objects. If sqlalchemy is installed, additional keyword options
     can provide database configuration, such as connection pooling.
     To use a mysql or postgresql database, sqlalchemy must be installed.
 
-    Inputs:
-        name: url for the sql database [default: (see note above)]
-        dict: initial dictionary to seed the archive
-        cached: if True, use an in-memory cache interface to the archive
-        serialized: if True, pickle table contents; otherwise cast as strings
-        protocol: pickling protocol [default: None (use the default protocol)]
+    Args:
+        name (str, default=None): database url (see above note)
+        dict (dict, default={}): initial dictionary to seed the archive
+        cached (bool, default=True): interact through an in-memory cache
+        serialized (bool, default=True): save objects as pickled strings
+        protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
         """
         if dict is None: dict = {}
         archive = _sql_archive(name, **kwds)
         if cached: archive = cache(archive=archive)
         archive.update(dict)
         return archive
 
@@ -208,22 +208,22 @@
         return _from_frame(dataframe)
     pass
 
 class hdfdir_archive(_hdfdir_archive):
     def __new__(hdfdir_archive, name=None, dict=None, cached=True, **kwds):
         """initialize a dictionary with a hdf5 file-folder archive backend
 
-    Inputs:
-        name: name of the root archive directory [default: memo]
-        dict: initial dictionary to seed the archive
-        cached: if True, use an in-memory cache interface to the archive
-        serialized: if True, pickle file contents; otherwise save python objects
-        permissions: octal representing read/write permissions [default: 0o775]
-        protocol: pickling protocol [default: None (use the default protocol)]
-        meta: if True, store as file root metadata; otherwise store in datasets
+    Args:
+        name (str, default='memo'): path of the archive root directory
+        dict (dict, default={}): initial dictionary to seed the archive
+        cached (bool, default=True): interact through an in-memory cache
+        serialized (bool, default=True): pickle saved python objects
+        permissions (octal, default=0o775): read/write permission indicator
+        protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
+        meta (bool, default=False): store in root metadata (not in dataset)
         """
         if dict is None: dict = {}
         archive = _hdfdir_archive(name, **kwds)
         if cached: archive = cache(archive=archive)
         archive.update(dict)
         return archive
 
@@ -236,21 +236,21 @@
         return _from_frame(dataframe)
     pass
 
 class hdf_archive(_hdf_archive):
     def __new__(hdf_archive, name=None, dict=None, cached=True, **kwds):
         """initialize a dictionary with a single hdf5 file archive backend
 
-    Inputs:
-        name: name of the hdf file archive [default: memo.hdf5]
-        dict: initial dictionary to seed the archive
-        cached: if True, use an in-memory cache interface to the archive
-        serialized: if True, pickle file contents; otherwise save python objects
-        protocol: pickling protocol [default: None (use the default protocol)]
-        meta: if True, store as file root metadata; otherwise store in datasets
+    Args:
+        name (str, default='memo.hdf5'): path of the file archive
+        dict (dict, default={}): initial dictionary to seed the archive
+        cached (bool, default=True): interact through an in-memory cache
+        serialized (bool, default=True): pickle saved python objects
+        protocol (int, default=DEFAULT_PROTOCOL): pickling protocol
+        meta (bool, default=False): store in root metadata (not in dataset)
         """
         if dict is None: dict = {}
         archive = _hdf_archive(name, **kwds)
         if cached: archive = cache(archive=archive)
         archive.update(dict)
         return archive
```

### Comparing `klepto-0.2.3/klepto/crypto.py` & `klepto-0.2.4/klepto/crypto.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 import os
 import sys
 import hashlib
 import pkgutil
@@ -84,26 +84,19 @@
 
 string.encodings = encodings
 
 
 def serializers(): #FIXME: could be much smarter
     """return a tuple of string names of serializers"""
     serializers = (None, 'pickle', 'json', 'dill')
-    try:
-        import imp
-        imp.find_module('cloudpickle')
+    from importlib import util as imp
+    if imp.find_spec('cloudpickle'):
         serializers += ('cloudpickle',)
-    except ImportError:
-        pass
-    try:
-        import imp
-        imp.find_module('jsonpickle')
+    if imp.find_spec('jsonpickle'):
         serializers += ('jsonpickle',)
-    except ImportError:
-        pass
     return serializers
 
 
 def pickle(object, serializer=None, **kwds):
     """pickle an object (to a string)
 
     serializer: name of pickler module with a 'dumps' method
```

### Comparing `klepto-0.2.3/klepto/keymaps.py` & `klepto-0.2.4/klepto/keymaps.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 """
 custom 'keymaps' for generating dictionary keys from function input signatures
 """
 
 __all__ = ['SENTINEL','NOSENTINEL','keymap','hashmap','stringmap','picklemap']
```

### Comparing `klepto-0.2.3/klepto/rounding.py` & `klepto-0.2.4/klepto/rounding.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 """
 decorators that provide rounding
 """
 
 __all__ = ['deep_round', 'shallow_round', 'simple_round']
```

### Comparing `klepto-0.2.3/klepto/safe.py` & `klepto-0.2.4/klepto/safe.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 # code inspired by Raymond Hettinger's LFU and LRU cache decorators
 # on http://code.activestate.com/recipes/498245-lru-and-lfu-cache-decorators
 # and subsequent forks as well as the version available in python3.3
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 """
 'safe' versions of selected caching decorators
 
 If a hashing error occurs, the cached function will be evaluated.
 """
```

### Comparing `klepto-0.2.3/klepto/tests/__main__.py` & `klepto-0.2.4/klepto/tests/__main__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 import glob
 import os
 import sys
 import subprocess as sp
```

### Comparing `klepto-0.2.3/klepto/tests/cleanup_basic.py` & `klepto-0.2.4/klepto/tests/cleanup_basic.py`

 * *Files identical despite different names*

### Comparing `klepto-0.2.3/klepto/tests/test_basic.py` & `klepto-0.2.4/klepto/tests/test_basic.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 from klepto.safe import lru_cache as memoized
 from random import choice, seed
 
 N = 30
```

### Comparing `klepto-0.2.3/klepto/tests/test_bigdata.py` & `klepto-0.2.4/klepto/tests/test_bigdata.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 from klepto.keymaps import *
 h = hashmap(algorithm='md5')
 p = picklemap(serializer='dill')
 hp = p + h
```

### Comparing `klepto-0.2.3/klepto/tests/test_cache.py` & `klepto-0.2.4/klepto/tests/test_cache.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 """
 The decorator should produce the behavior as displayed in the following:
 
 >>> s = Spam()
 >>> s.eggs()
```

### Comparing `klepto-0.2.3/klepto/tests/test_cache_info.py` & `klepto-0.2.4/klepto/tests/test_cache_info.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 """
 test speed and effectiveness of a selection of cache algorithms
 """
 
 from klepto.archives import file_archive
```

### Comparing `klepto-0.2.3/klepto/tests/test_cachekeys.py` & `klepto-0.2.4/klepto/tests/test_cachekeys.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2014-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 from klepto import inf_cache as memoized
 from klepto.archives import *
 from klepto.keymaps import picklemap
```

### Comparing `klepto-0.2.3/klepto/tests/test_chaining.py` & `klepto-0.2.4/klepto/tests/test_chaining.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 import sys
 from klepto.keymaps import *
 from klepto.crypto import *
 h = hashmap(algorithm='md5')
```

### Comparing `klepto-0.2.3/klepto/tests/test_crypto.py` & `klepto-0.2.4/klepto/tests/test_crypto.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 from klepto.crypto import *
 from klepto.tools import _b
 from klepto.keymaps import *
```

### Comparing `klepto-0.2.3/klepto/tests/test_frame.py` & `klepto-0.2.4/klepto/tests/test_frame.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2019-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2019-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 import klepto as kl
 
 def test_roundtrip(archive):
     db = archive
```

### Comparing `klepto-0.2.3/klepto/tests/test_hdf.py` & `klepto-0.2.4/klepto/tests/test_hdf.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 from klepto.safe import lru_cache as memoized
 from random import choice, seed
 
 N = 100
```

### Comparing `klepto-0.2.3/klepto/tests/test_ignore.py` & `klepto-0.2.4/klepto/tests/test_ignore.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 import sys
 from functools import partial
 from klepto.keymaps import hashmap
 from klepto import NULL
```

### Comparing `klepto-0.2.3/klepto/tests/test_keymaps.py` & `klepto-0.2.4/klepto/tests/test_keymaps.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 from klepto.keymaps import *
 from dill import dumps, loads
 
 args = (1,2); kwds = {"a":3, "b":4}
```

### Comparing `klepto-0.2.3/klepto/tests/test_pickles.py` & `klepto-0.2.4/klepto/tests/test_pickles.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 import dill
 import klepto
 
 @klepto.lru_cache()
```

### Comparing `klepto-0.2.3/klepto/tests/test_readwrite.py` & `klepto-0.2.4/klepto/tests/test_readwrite.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 from klepto.archives import dir_archive
 from pox import rmtree
 
 def test_foo():
```

### Comparing `klepto-0.2.3/klepto/tests/test_rounding.py` & `klepto-0.2.4/klepto/tests/test_rounding.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 from klepto.rounding import *
 
 def test_deep_round():
     @deep_round(tol=1)
```

### Comparing `klepto-0.2.3/klepto/tests/test_workflow.py` & `klepto-0.2.4/klepto/tests/test_workflow.py`

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
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
 from klepto.keymaps import hashmap
 from klepto import lru_cache as memoize
 from klepto import inf_cache
 from klepto import keygen
```

### Comparing `klepto-0.2.3/klepto/tools.py` & `klepto-0.2.4/klepto/tools.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 """
 Assorted python tools
 
 Main functions exported are:: 
     - isiterable: check if an object is iterable
```

### Comparing `klepto-0.2.3/klepto.egg-info/PKG-INFO` & `klepto-0.2.4/klepto.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: klepto
-Version: 0.2.3
+Version: 0.2.4
 Summary: persistent caching to memory, disk, or database
 Home-page: https://github.com/uqfoundation/klepto
 Download-URL: https://pypi.org/project/klepto/#files
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
 Classifier: Topic :: Database
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Software Development
 Requires-Python: >=3.7
 Provides-Extra: archives
@@ -37,34 +38,34 @@
 -------------------------------------------------------
 klepto: persistent caching to memory, disk, or database
 -------------------------------------------------------
 
 About Klepto
 ============
 
-``klepto`` extends python's ``lru_cache`` to utilize different keymaps and
+``klepto`` extends Python's ``lru_cache`` to utilize different keymaps and
 alternate caching algorithms, such as ``lfu_cache`` and ``mru_cache``.
 While caching is meant for fast access to saved results, ``klepto`` also
 has archiving capabilities, for longer-term storage. ``klepto`` uses a
 simple dictionary-sytle interface for all caches and archives, and all
-caches can be applied to any python function as a decorator. Keymaps
+caches can be applied to any Python function as a decorator. Keymaps
 are algorithms for converting a function's input signature to a unique
 dictionary, where the function's results are the dictionary value.
 Thus for ``y = f(x)``, ``y`` will be stored in ``cache[x]`` (e.g. ``{x:y}``).
 
 ``klepto`` provides both standard and *"safe"* caching, where *"safe"* caches
 are slower but can recover from hashing errors. ``klepto`` is intended
 to be used for distributed and parallel computing, where several of
 the keymaps serialize the stored objects. Caches and archives are
 intended to be read/write accessible from different threads and
 processes. ``klepto`` enables a user to decorate a function, save the
 results to a file or database archive, close the interpreter,
 start a new session, and reload the function and it's cache.
 
-``klepto`` is part of ``pathos``, a python framework for heterogeneous computing.
+``klepto`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``klepto`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/klepto/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
@@ -86,18 +87,18 @@
     - ``hdfdir_archive`` - a dictionary-style interface to a folder of hdf5 files
     - ``hdf_archive`` - a dictionary-style interface to a hdf5 file
     - ``dict_archive`` - a dictionary with an archive interface
     - ``null_archive`` - a dictionary-style interface to a dummy archive 
 
 ``klepto`` provides the following keymaps:
 
-    - ``keymap`` - keys are raw python objects
-    - ``hashmap`` - keys are a hash for the python object
-    - ``stringmap`` - keys are the python object cast as a string
-    - ``picklemap`` - keys are the serialized python object
+    - ``keymap`` - keys are raw Python objects
+    - ``hashmap`` - keys are a hash for the Python object
+    - ``stringmap`` - keys are the Python object cast as a string
+    - ``picklemap`` - keys are the serialized Python object
 
 ``klepto`` also includes a few useful decorators providing:
 
     - simple, shallow, or deep rounding of function arguments
     - cryptographic key generation, with masking of selected arguments
 
 
@@ -140,22 +141,22 @@
 Requirements
 ============
 
 ``klepto`` requires:
 
     - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
-    - ``dill``, **>=0.3.6**
-    - ``pox``, **>=0.3.2**
+    - ``dill``, **>=0.3.7**
+    - ``pox``, **>=0.3.3**
 
 Optional requirements:
 
     - ``h5py``, **>=2.8.0**
     - ``pandas``, **>=0.17.0**
-    - ``sqlalchemy``, **>=0.8.4**
+    - ``sqlalchemy``, **>=1.4.0**
     - ``jsonpickle``, **>=0.9.6**
     - ``cloudpickle``, **>=0.5.2**
 
 
 More Information
 ================
```

### Comparing `klepto-0.2.3/klepto.egg-info/SOURCES.txt` & `klepto-0.2.4/klepto.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -13,14 +13,15 @@
 version.py
 docs/Makefile
 docs/requirements.txt
 docs/source/conf.py
 docs/source/index.rst
 docs/source/klepto.rst
 docs/source/pathos.png
+docs/source/_static/css/custom.css
 klepto/__info__.py
 klepto/__init__.py
 klepto/_abc.py
 klepto/_archives.py
 klepto/_cache.py
 klepto/_inspect.py
 klepto/_pickle.py
```

### Comparing `klepto-0.2.3/setup.py` & `klepto-0.2.4/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2013-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
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
         'Topic :: Database',
         'Topic :: Scientific/Engineering',
         'Topic :: Software Development',
     ],
     packages = ['klepto','klepto.tests'],
@@ -80,19 +81,19 @@
 class BinaryDistribution(Distribution):
     """Distribution which forces a binary package with platform name"""
     def has_ext_modules(foo):
         return True
 
 # define dependencies
 sysversion = sys.version_info[:3]
-dill_version = 'dill>=0.3.6'
-pox_version = 'pox>=0.3.2'
+dill_version = 'dill>=0.3.7'
+pox_version = 'pox>=0.3.3'
 jsonpickle_version = 'jsonpickle>=0.9.6'
 cloudpickle_version = 'cloudpickle>=0.5.2'
-sqlalchemy_version = 'sqlalchemy>=0.8.4'
+sqlalchemy_version = 'sqlalchemy>=1.4.0'
 h5py_version = 'h5py>=2.8.0'
 if sysversion < (3,7,1):
     pandas_version = 'pandas>=0.17.0, <1.2.0'
 else:
     pandas_version = 'pandas>=0.17.0'
 # add dependencies
 depend = [pox_version, dill_version]
```

### Comparing `klepto-0.2.3/version.py` & `klepto-0.2.4/version.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/klepto/blob/master/LICENSE
 
-__version__ = '0.2.3'
+__version__ = '0.2.4'
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

