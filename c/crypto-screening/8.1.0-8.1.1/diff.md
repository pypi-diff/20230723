# Comparing `tmp/crypto-screening-8.1.0.tar.gz` & `tmp/crypto-screening-8.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "crypto-screening-8.1.0.tar", last modified: Sat Jul 22 15:57:44 2023, max compression
+gzip compressed data, was "crypto-screening-8.1.1.tar", last modified: Sun Jul 23 13:28:14 2023, max compression
```

## Comparing `crypto-screening-8.1.0.tar` & `crypto-screening-8.1.1.tar`

### file list

```diff
@@ -1,73 +1,73 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.969147 crypto-screening-8.1.0/
--rw-rw-rw-   0        0        0      196 2023-07-22 15:57:44.000000 crypto-screening-8.1.0/MANIFEST.in
--rw-rw-rw-   0        0        0     2059 2023-07-22 15:57:44.969147 crypto-screening-8.1.0/PKG-INFO
--rw-rw-rw-   0        0        0     1238 2023-07-01 07:09:50.000000 crypto-screening-8.1.0/README.md
--rw-rw-rw-   0        0        0    12920 2023-06-23 16:52:27.000000 crypto-screening-8.1.0/build.py
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.926146 crypto-screening-8.1.0/crypto_screening/
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.944115 crypto-screening-8.1.0/crypto_screening/collect/
--rw-rw-rw-   0        0        0    17733 2023-07-22 15:48:11.000000 crypto-screening-8.1.0/crypto_screening/collect/assets.py
--rw-rw-rw-   0        0        0     4773 2023-07-22 15:47:32.000000 crypto-screening-8.1.0/crypto_screening/collect/exchanges.py
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.948146 crypto-screening-8.1.0/crypto_screening/collect/market/
--rw-rw-rw-   0        0        0      235 2023-07-16 14:00:25.000000 crypto-screening-8.1.0/crypto_screening/collect/market/__init__.py
--rw-rw-rw-   0        0        0    19623 2023-07-18 21:23:44.000000 crypto-screening-8.1.0/crypto_screening/collect/market/ohlcv.py
--rw-rw-rw-   0        0        0    17275 2023-07-17 09:43:58.000000 crypto-screening-8.1.0/crypto_screening/collect/market/orderbook.py
--rw-rw-rw-   0        0        0    12533 2023-07-18 21:21:45.000000 crypto-screening-8.1.0/crypto_screening/collect/market/orders.py
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.950147 crypto-screening-8.1.0/crypto_screening/collect/market/state/
--rw-rw-rw-   0        0        0      194 2023-07-16 14:00:21.000000 crypto-screening-8.1.0/crypto_screening/collect/market/state/__init__.py
--rw-rw-rw-   0        0        0    24729 2023-07-20 08:01:55.000000 crypto-screening-8.1.0/crypto_screening/collect/market/state/assets.py
--rw-rw-rw-   0        0        0    16341 2023-07-21 10:15:56.000000 crypto-screening-8.1.0/crypto_screening/collect/market/state/base.py
--rw-rw-rw-   0        0        0    21717 2023-07-20 08:01:55.000000 crypto-screening-8.1.0/crypto_screening/collect/market/state/symbols.py
--rw-rw-rw-   0        0        0    15133 2023-07-18 21:21:06.000000 crypto-screening-8.1.0/crypto_screening/collect/market/trades.py
--rw-rw-rw-   0        0        0    16799 2023-07-20 15:36:57.000000 crypto-screening-8.1.0/crypto_screening/collect/screeners.py
--rw-rw-rw-   0        0        0    19520 2023-07-22 15:47:21.000000 crypto-screening-8.1.0/crypto_screening/collect/symbols.py
--rw-rw-rw-   0        0        0    14801 2023-07-20 08:05:34.000000 crypto-screening-8.1.0/crypto_screening/dataset.py
--rw-rw-rw-   0        0        0     1055 2023-07-22 15:46:14.000000 crypto-screening-8.1.0/crypto_screening/exchanges.py
--rw-rw-rw-   0        0        0     5404 2023-07-14 06:26:34.000000 crypto-screening-8.1.0/crypto_screening/interval.py
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.952145 crypto-screening-8.1.0/crypto_screening/market/
--rw-rw-rw-   0        0        0    15126 2023-07-22 11:30:19.000000 crypto-screening-8.1.0/crypto_screening/market/dynamic.py
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.954147 crypto-screening-8.1.0/crypto_screening/market/foundation/
--rw-rw-rw-   0        0        0    10459 2023-07-22 14:33:35.000000 crypto-screening-8.1.0/crypto_screening/market/foundation/data.py
--rw-rw-rw-   0        0        0      840 2023-07-18 21:26:30.000000 crypto-screening-8.1.0/crypto_screening/market/foundation/protocols.py
--rw-rw-rw-   0        0        0     1200 2023-07-18 21:52:07.000000 crypto-screening-8.1.0/crypto_screening/market/foundation/state.py
--rw-rw-rw-   0        0        0     6957 2023-07-18 21:40:34.000000 crypto-screening-8.1.0/crypto_screening/market/foundation/waiting.py
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.961146 crypto-screening-8.1.0/crypto_screening/market/screeners/
--rw-rw-rw-   0        0        0      519 2023-07-20 15:38:19.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/__init__.py
--rw-rw-rw-   0        0        0    23442 2023-07-22 14:11:45.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/base.py
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.963145 crypto-screening-8.1.0/crypto_screening/market/screeners/callbacks/
--rw-rw-rw-   0        0        0      214 2023-07-22 15:42:32.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/callbacks/__init__.py
--rw-rw-rw-   0        0        0     4116 2023-07-22 15:42:32.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/callbacks/base.py
--rw-rw-rw-   0        0        0     4415 2023-07-22 15:44:08.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/callbacks/database.py
--rw-rw-rw-   0        0        0     5613 2023-07-22 15:44:08.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/callbacks/sockets.py
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.966146 crypto-screening-8.1.0/crypto_screening/market/screeners/collectors/
--rw-rw-rw-   0        0        0      217 2023-07-20 15:09:26.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/collectors/__init__.py
--rw-rw-rw-   0        0        0     6285 2023-07-22 14:19:31.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/collectors/base.py
--rw-rw-rw-   0        0        0     4055 2023-07-22 09:26:50.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/collectors/database.py
--rw-rw-rw-   0        0        0     6164 2023-07-22 15:50:07.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/collectors/sockets.py
--rw-rw-rw-   0        0        0    12308 2023-07-22 15:48:11.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/combined.py
--rw-rw-rw-   0        0        0    10848 2023-07-22 14:02:39.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/container.py
--rw-rw-rw-   0        0        0    10983 2023-07-21 08:58:32.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/database.py
--rw-rw-rw-   0        0        0    22129 2023-07-22 15:48:53.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/ohlcv.py
--rw-rw-rw-   0        0        0    11829 2023-07-22 15:54:41.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/orderbook.py
--rw-rw-rw-   0        0        0    11431 2023-07-22 15:49:37.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/orders.py
--rw-rw-rw-   0        0        0    16942 2023-07-22 15:49:37.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/recorder.py
--rw-rw-rw-   0        0        0    11500 2023-07-22 15:50:19.000000 crypto-screening-8.1.0/crypto_screening/market/screeners/trades.py
--rw-rw-rw-   0        0        0     3832 2023-07-18 21:42:09.000000 crypto-screening-8.1.0/crypto_screening/market/waiting.py
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.918115 crypto-screening-8.1.0/crypto_screening/source/
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.967146 crypto-screening-8.1.0/crypto_screening/source/data/
--rw-rw-rw-   0        0        0   284601 2023-07-21 09:53:03.000000 crypto-screening-8.1.0/crypto_screening/source/data/all_exchanges_symbols.json
--rw-rw-rw-   0        0        0    10361 2023-07-18 17:06:38.000000 crypto-screening-8.1.0/crypto_screening/symbols.py
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.968146 crypto-screening-8.1.0/crypto_screening/utils/
--rw-rw-rw-   0        0        0     1012 2023-07-22 15:52:54.000000 crypto-screening-8.1.0/crypto_screening/utils/base.py
--rw-rw-rw-   0        0        0     2382 2023-06-30 14:15:11.000000 crypto-screening-8.1.0/crypto_screening/utils/process.py
--rw-rw-rw-   0        0        0     3605 2023-07-22 15:45:17.000000 crypto-screening-8.1.0/crypto_screening/validate.py
-drwxrwxrwx   0        0        0        0 2023-07-22 15:57:44.942114 crypto-screening-8.1.0/crypto_screening.egg-info/
--rw-rw-rw-   0        0        0     2059 2023-07-22 15:57:44.000000 crypto-screening-8.1.0/crypto_screening.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     2254 2023-07-22 15:57:44.000000 crypto-screening-8.1.0/crypto_screening.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 15:57:44.000000 crypto-screening-8.1.0/crypto_screening.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      113 2023-07-22 15:57:44.000000 crypto-screening-8.1.0/crypto_screening.egg-info/requires.txt
--rw-rw-rw-   0        0        0       17 2023-07-22 15:57:44.000000 crypto-screening-8.1.0/crypto_screening.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      652 2023-07-22 15:57:44.000000 crypto-screening-8.1.0/pyproject.toml
--rw-rw-rw-   0        0        0      120 2023-07-17 22:21:20.000000 crypto-screening-8.1.0/requirements-dev.txt
--rw-rw-rw-   0        0        0       77 2023-07-17 20:19:29.000000 crypto-screening-8.1.0/requirements.txt
--rw-rw-rw-   0        0        0       42 2023-07-22 15:57:44.969147 crypto-screening-8.1.0/setup.cfg
--rw-rw-rw-   0        0        0     1649 2023-07-22 15:57:22.000000 crypto-screening-8.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.975505 crypto-screening-8.1.1/
+-rw-rw-rw-   0        0        0      196 2023-07-23 13:28:14.000000 crypto-screening-8.1.1/MANIFEST.in
+-rw-rw-rw-   0        0        0     2059 2023-07-23 13:28:14.975505 crypto-screening-8.1.1/PKG-INFO
+-rw-rw-rw-   0        0        0     1238 2023-07-01 07:09:50.000000 crypto-screening-8.1.1/README.md
+-rw-rw-rw-   0        0        0    12920 2023-06-23 16:52:27.000000 crypto-screening-8.1.1/build.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.740275 crypto-screening-8.1.1/crypto_screening/
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.772044 crypto-screening-8.1.1/crypto_screening/collect/
+-rw-rw-rw-   0        0        0    17733 2023-07-22 15:48:11.000000 crypto-screening-8.1.1/crypto_screening/collect/assets.py
+-rw-rw-rw-   0        0        0     4773 2023-07-22 15:47:32.000000 crypto-screening-8.1.1/crypto_screening/collect/exchanges.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.798044 crypto-screening-8.1.1/crypto_screening/collect/market/
+-rw-rw-rw-   0        0        0      235 2023-07-16 14:00:25.000000 crypto-screening-8.1.1/crypto_screening/collect/market/__init__.py
+-rw-rw-rw-   0        0        0    19623 2023-07-18 21:23:44.000000 crypto-screening-8.1.1/crypto_screening/collect/market/ohlcv.py
+-rw-rw-rw-   0        0        0    17275 2023-07-17 09:43:58.000000 crypto-screening-8.1.1/crypto_screening/collect/market/orderbook.py
+-rw-rw-rw-   0        0        0    12533 2023-07-18 21:21:45.000000 crypto-screening-8.1.1/crypto_screening/collect/market/orders.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.821110 crypto-screening-8.1.1/crypto_screening/collect/market/state/
+-rw-rw-rw-   0        0        0      194 2023-07-16 14:00:21.000000 crypto-screening-8.1.1/crypto_screening/collect/market/state/__init__.py
+-rw-rw-rw-   0        0        0    24729 2023-07-20 08:01:55.000000 crypto-screening-8.1.1/crypto_screening/collect/market/state/assets.py
+-rw-rw-rw-   0        0        0    16341 2023-07-21 10:15:56.000000 crypto-screening-8.1.1/crypto_screening/collect/market/state/base.py
+-rw-rw-rw-   0        0        0    21717 2023-07-20 08:01:55.000000 crypto-screening-8.1.1/crypto_screening/collect/market/state/symbols.py
+-rw-rw-rw-   0        0        0    15133 2023-07-18 21:21:06.000000 crypto-screening-8.1.1/crypto_screening/collect/market/trades.py
+-rw-rw-rw-   0        0        0    17755 2023-07-23 13:27:54.000000 crypto-screening-8.1.1/crypto_screening/collect/screeners.py
+-rw-rw-rw-   0        0        0    19520 2023-07-22 15:47:21.000000 crypto-screening-8.1.1/crypto_screening/collect/symbols.py
+-rw-rw-rw-   0        0        0    14801 2023-07-20 08:05:34.000000 crypto-screening-8.1.1/crypto_screening/dataset.py
+-rw-rw-rw-   0        0        0     1055 2023-07-22 15:46:14.000000 crypto-screening-8.1.1/crypto_screening/exchanges.py
+-rw-rw-rw-   0        0        0     5404 2023-07-14 06:26:34.000000 crypto-screening-8.1.1/crypto_screening/interval.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.831148 crypto-screening-8.1.1/crypto_screening/market/
+-rw-rw-rw-   0        0        0    15126 2023-07-22 11:30:19.000000 crypto-screening-8.1.1/crypto_screening/market/dynamic.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.852153 crypto-screening-8.1.1/crypto_screening/market/foundation/
+-rw-rw-rw-   0        0        0    10459 2023-07-22 14:33:35.000000 crypto-screening-8.1.1/crypto_screening/market/foundation/data.py
+-rw-rw-rw-   0        0        0      840 2023-07-18 21:26:30.000000 crypto-screening-8.1.1/crypto_screening/market/foundation/protocols.py
+-rw-rw-rw-   0        0        0     1200 2023-07-18 21:52:07.000000 crypto-screening-8.1.1/crypto_screening/market/foundation/state.py
+-rw-rw-rw-   0        0        0     6957 2023-07-18 21:40:34.000000 crypto-screening-8.1.1/crypto_screening/market/foundation/waiting.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.909860 crypto-screening-8.1.1/crypto_screening/market/screeners/
+-rw-rw-rw-   0        0        0      519 2023-07-20 15:38:19.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/__init__.py
+-rw-rw-rw-   0        0        0    23442 2023-07-22 14:11:45.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/base.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.933535 crypto-screening-8.1.1/crypto_screening/market/screeners/callbacks/
+-rw-rw-rw-   0        0        0      214 2023-07-22 15:42:32.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/callbacks/__init__.py
+-rw-rw-rw-   0        0        0     4116 2023-07-22 15:42:32.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/callbacks/base.py
+-rw-rw-rw-   0        0        0     4415 2023-07-22 15:44:08.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/callbacks/database.py
+-rw-rw-rw-   0        0        0     5613 2023-07-22 15:44:08.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/callbacks/sockets.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.956506 crypto-screening-8.1.1/crypto_screening/market/screeners/collectors/
+-rw-rw-rw-   0        0        0      217 2023-07-20 15:09:26.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/collectors/__init__.py
+-rw-rw-rw-   0        0        0     6285 2023-07-22 14:19:31.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/collectors/base.py
+-rw-rw-rw-   0        0        0     4055 2023-07-22 09:26:50.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/collectors/database.py
+-rw-rw-rw-   0        0        0     6164 2023-07-22 15:50:07.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/collectors/sockets.py
+-rw-rw-rw-   0        0        0    12308 2023-07-22 15:48:11.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/combined.py
+-rw-rw-rw-   0        0        0    10848 2023-07-22 14:02:39.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/container.py
+-rw-rw-rw-   0        0        0    10983 2023-07-21 08:58:32.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/database.py
+-rw-rw-rw-   0        0        0    22129 2023-07-22 15:48:53.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/ohlcv.py
+-rw-rw-rw-   0        0        0    11829 2023-07-22 15:54:41.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/orderbook.py
+-rw-rw-rw-   0        0        0    11431 2023-07-22 15:49:37.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/orders.py
+-rw-rw-rw-   0        0        0    16942 2023-07-22 15:49:37.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/recorder.py
+-rw-rw-rw-   0        0        0    11500 2023-07-22 15:50:19.000000 crypto-screening-8.1.1/crypto_screening/market/screeners/trades.py
+-rw-rw-rw-   0        0        0     3832 2023-07-18 21:42:09.000000 crypto-screening-8.1.1/crypto_screening/market/waiting.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.706243 crypto-screening-8.1.1/crypto_screening/source/
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.961505 crypto-screening-8.1.1/crypto_screening/source/data/
+-rw-rw-rw-   0        0        0   284601 2023-07-21 09:53:03.000000 crypto-screening-8.1.1/crypto_screening/source/data/all_exchanges_symbols.json
+-rw-rw-rw-   0        0        0    10361 2023-07-18 17:06:38.000000 crypto-screening-8.1.1/crypto_screening/symbols.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.974506 crypto-screening-8.1.1/crypto_screening/utils/
+-rw-rw-rw-   0        0        0     1012 2023-07-22 15:52:54.000000 crypto-screening-8.1.1/crypto_screening/utils/base.py
+-rw-rw-rw-   0        0        0     2382 2023-06-30 14:15:11.000000 crypto-screening-8.1.1/crypto_screening/utils/process.py
+-rw-rw-rw-   0        0        0     3605 2023-07-22 15:45:17.000000 crypto-screening-8.1.1/crypto_screening/validate.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:28:14.754071 crypto-screening-8.1.1/crypto_screening.egg-info/
+-rw-rw-rw-   0        0        0     2059 2023-07-23 13:28:14.000000 crypto-screening-8.1.1/crypto_screening.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     2254 2023-07-23 13:28:14.000000 crypto-screening-8.1.1/crypto_screening.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 13:28:14.000000 crypto-screening-8.1.1/crypto_screening.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      113 2023-07-23 13:28:14.000000 crypto-screening-8.1.1/crypto_screening.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       17 2023-07-23 13:28:14.000000 crypto-screening-8.1.1/crypto_screening.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      652 2023-07-23 13:28:14.000000 crypto-screening-8.1.1/pyproject.toml
+-rw-rw-rw-   0        0        0      120 2023-07-17 22:21:20.000000 crypto-screening-8.1.1/requirements-dev.txt
+-rw-rw-rw-   0        0        0       77 2023-07-17 20:19:29.000000 crypto-screening-8.1.1/requirements.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 13:28:14.975505 crypto-screening-8.1.1/setup.cfg
+-rw-rw-rw-   0        0        0     1649 2023-07-23 13:28:12.000000 crypto-screening-8.1.1/setup.py
```

### Comparing `crypto-screening-8.1.0/PKG-INFO` & `crypto-screening-8.1.1/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: crypto-screening
-Version: 8.1.0
+Version: 8.1.1
 Summary: A software for automatically recording real-time crypto exchanges and pairs OHLCV and Orderbook rates.
 Home-page: https://github.com/Shahaf-F-S/crypto-screening
 Author: Shahaf Frank-Shapir
 Author-email: shahaffrs@gmail.com
 License: MIT
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `crypto-screening-8.1.0/README.md` & `crypto-screening-8.1.1/README.md`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/build.py` & `crypto-screening-8.1.1/build.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/collect/assets.py` & `crypto-screening-8.1.1/crypto_screening/collect/assets.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/collect/exchanges.py` & `crypto-screening-8.1.1/crypto_screening/collect/exchanges.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/collect/market/ohlcv.py` & `crypto-screening-8.1.1/crypto_screening/collect/market/ohlcv.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/collect/market/orderbook.py` & `crypto-screening-8.1.1/crypto_screening/collect/market/orderbook.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/collect/market/orders.py` & `crypto-screening-8.1.1/crypto_screening/collect/market/orders.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/collect/market/state/assets.py` & `crypto-screening-8.1.1/crypto_screening/collect/market/state/assets.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/collect/market/state/base.py` & `crypto-screening-8.1.1/crypto_screening/collect/market/state/base.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/collect/market/state/symbols.py` & `crypto-screening-8.1.1/crypto_screening/collect/market/state/symbols.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/collect/market/trades.py` & `crypto-screening-8.1.1/crypto_screening/collect/market/trades.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/collect/screeners.py` & `crypto-screening-8.1.1/crypto_screening/collect/screeners.py`

 * *Files 2% similar despite different names*

```diff
@@ -20,27 +20,28 @@
 __all__ = [
     "matching_screener_signatures",
     "matching_screener_pair",
     "matching_screener_pairs",
     "MarketScreenerSignature",
     "find_screeners",
     "structure_screeners",
-    "live_screeners",
+    "live_nonempty_screeners",
     "remove_empty_screeners",
     "screeners_exchanges_symbols",
     "structure_exchanges_symbols_screeners",
     "structure_exchanges_symbols_screener",
     "gather_screeners",
     "exchanges_symbols_screeners",
     "screeners_to_multiple_symbols_screeners",
     "screeners_to_assets_screeners",
     "screeners_to_symbols_screeners",
     "screeners_to_multiple_assets_screeners",
     "screeners_to_multiple_assets_datasets",
-    "screeners_to_multiple_symbols_datasets"
+    "screeners_to_multiple_symbols_datasets",
+    "nonempty_screeners"
 ]
 
 AssetMatches = Iterable[Iterable[str]]
 
 def matching_screener_pair(
         screener1: BaseScreener,
         screener2: BaseScreener, /, *,
@@ -178,35 +179,66 @@
             )
         )
     # end for
 
     return set(pairs)
 # end matching_screener_signatures
 
-def live_screeners(
+def nonempty_screeners(
         screeners: Iterable[Union[BaseScreener, BaseMarketScreener]]
 ) -> Set[Union[BaseScreener, BaseMarketScreener]]:
     """
     Returns a list of all the live create_screeners.
 
     :param screeners: The create_screeners to search from.
 
     :return: A list the live create_screeners.
     """
 
     return {
         screener for screener in screeners
         if (
-            screener.screening and (
-                isinstance(screener, BaseMarketScreener) or
-                len(screener.market) > 0
+            (
+                isinstance(screener, BaseMarketScreener) and
+                nonempty_screeners(screener.screeners)
+            ) or
+            (
+                (len(screener.market) > 0) and
+                isinstance(screener, BaseScreener)
+            )
+        )
+    }
+# end nonempty_screeners
+
+def live_nonempty_screeners(
+        screeners: Iterable[Union[BaseScreener, BaseMarketScreener]]
+) -> Set[Union[BaseScreener, BaseMarketScreener]]:
+    """
+    Returns a list of all the live create_screeners.
+
+    :param screeners: The create_screeners to search from.
+
+    :return: A list the live create_screeners.
+    """
+
+    return {
+        screener for screener in screeners
+        if (
+            (
+                isinstance(screener, BaseMarketScreener) and
+                live_nonempty_screeners(screener.screeners)
+            ) or
+            (
+                screener.screening and
+                (len(screener.market) > 0) and
+                isinstance(screener, BaseScreener)
             )
         )
     }
-# end live_screeners
+# end live_nonempty_screeners
 
 def structure_screeners(
         screeners: Iterable[BaseScreener]
 ) -> Dict[str, Dict[str, List[BaseScreener]]]:
     """
     Structures the screener objects by exchanges and symbols
```

### Comparing `crypto-screening-8.1.0/crypto_screening/collect/symbols.py` & `crypto-screening-8.1.1/crypto_screening/collect/symbols.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/dataset.py` & `crypto-screening-8.1.1/crypto_screening/dataset.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/exchanges.py` & `crypto-screening-8.1.1/crypto_screening/exchanges.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/interval.py` & `crypto-screening-8.1.1/crypto_screening/interval.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/dynamic.py` & `crypto-screening-8.1.1/crypto_screening/market/dynamic.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/foundation/data.py` & `crypto-screening-8.1.1/crypto_screening/market/foundation/data.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/foundation/protocols.py` & `crypto-screening-8.1.1/crypto_screening/market/foundation/protocols.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/foundation/state.py` & `crypto-screening-8.1.1/crypto_screening/market/foundation/state.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/foundation/waiting.py` & `crypto-screening-8.1.1/crypto_screening/market/foundation/waiting.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/__init__.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/__init__.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/base.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/base.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/callbacks/base.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/callbacks/base.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/callbacks/database.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/callbacks/database.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/callbacks/sockets.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/callbacks/sockets.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/collectors/base.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/collectors/base.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/collectors/database.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/collectors/database.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/collectors/sockets.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/collectors/sockets.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/combined.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/combined.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/container.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/container.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/database.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/database.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/ohlcv.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/ohlcv.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/orderbook.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/orderbook.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/orders.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/orders.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/recorder.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/recorder.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/screeners/trades.py` & `crypto-screening-8.1.1/crypto_screening/market/screeners/trades.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/market/waiting.py` & `crypto-screening-8.1.1/crypto_screening/market/waiting.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/source/data/all_exchanges_symbols.json` & `crypto-screening-8.1.1/crypto_screening/source/data/all_exchanges_symbols.json`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/symbols.py` & `crypto-screening-8.1.1/crypto_screening/symbols.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/utils/base.py` & `crypto-screening-8.1.1/crypto_screening/utils/base.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/utils/process.py` & `crypto-screening-8.1.1/crypto_screening/utils/process.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening/validate.py` & `crypto-screening-8.1.1/crypto_screening/validate.py`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/crypto_screening.egg-info/PKG-INFO` & `crypto-screening-8.1.1/crypto_screening.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: crypto-screening
-Version: 8.1.0
+Version: 8.1.1
 Summary: A software for automatically recording real-time crypto exchanges and pairs OHLCV and Orderbook rates.
 Home-page: https://github.com/Shahaf-F-S/crypto-screening
 Author: Shahaf Frank-Shapir
 Author-email: shahaffrs@gmail.com
 License: MIT
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `crypto-screening-8.1.0/crypto_screening.egg-info/SOURCES.txt` & `crypto-screening-8.1.1/crypto_screening.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `crypto-screening-8.1.0/pyproject.toml` & `crypto-screening-8.1.1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = 'crypto-screening'
-version = '8.1.0'
+version = '8.1.1'
 description = 'A software for automatically recording real-time crypto exchanges and pairs OHLCV and Orderbook rates.'
 classifiers = [
 	'Intended Audience :: Developers',
 	'License :: OSI Approved :: MIT License',
 	'Programming Language :: Python',
 	'Programming Language :: Python :: 3',
 	'Programming Language :: Python :: 3.8',
```

### Comparing `crypto-screening-8.1.0/setup.py` & `crypto-screening-8.1.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -23,15 +23,15 @@
         ],
         include=[
             "crypto_screening/source"
         ],
         requirements="requirements.txt",
         dev_requirements="requirements-dev.txt",
         name='crypto-screening',
-        version='8.1.0',
+        version='8.1.1',
         description=(
             "A software for automatically recording "
             "real-time crypto exchanges and pairs "
             "OHLCV and Orderbook rates."
         ),
         license='MIT',
         author="Shahaf Frank-Shapir",
```

