# Comparing `tmp/cgpmgr-1.6.tar.gz` & `tmp/cgpmgr-1.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cgpmgr-1.6.tar", last modified: Tue Jul  4 05:28:33 2023, max compression
+gzip compressed data, was "cgpmgr-1.7.tar", last modified: Sun Jul 23 00:17:58 2023, max compression
```

## Comparing `cgpmgr-1.6.tar` & `cgpmgr-1.7.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxr-xr-x   0 pi        (1000) pi        (1000)        0 2023-07-04 05:28:33.150441 cgpmgr-1.6/
--rw-r--r--   0 pi        (1000) pi        (1000)    11342 2021-09-04 14:18:09.000000 cgpmgr-1.6/LICENSE
--rw-r--r--   0 pi        (1000) pi        (1000)      307 2023-07-04 05:28:33.140440 cgpmgr-1.6/PKG-INFO
--rw-r--r--   0 pi        (1000) pi        (1000)     2812 2023-06-05 04:58:21.000000 cgpmgr-1.6/README.md
-drwxr-xr-x   0 pi        (1000) pi        (1000)        0 2023-07-04 05:28:33.120440 cgpmgr-1.6/cgpmgr/
--rwxr-xr-x   0 pi        (1000) pi        (1000)       19 2021-09-05 05:17:17.000000 cgpmgr-1.6/cgpmgr/__init__.py
--rwxr-xr-x   0 pi        (1000) pi        (1000)    31122 2023-07-04 05:26:27.000000 cgpmgr-1.6/cgpmgr/cli.py
-drwxr-xr-x   0 pi        (1000) pi        (1000)        0 2023-07-04 05:28:33.140440 cgpmgr-1.6/cgpmgr.egg-info/
--rw-r--r--   0 pi        (1000) pi        (1000)      307 2023-07-04 05:28:32.000000 cgpmgr-1.6/cgpmgr.egg-info/PKG-INFO
--rw-r--r--   0 pi        (1000) pi        (1000)      241 2023-07-04 05:28:33.000000 cgpmgr-1.6/cgpmgr.egg-info/SOURCES.txt
--rw-r--r--   0 pi        (1000) pi        (1000)        1 2023-07-04 05:28:32.000000 cgpmgr-1.6/cgpmgr.egg-info/dependency_links.txt
--rw-r--r--   0 pi        (1000) pi        (1000)       38 2023-07-04 05:28:32.000000 cgpmgr-1.6/cgpmgr.egg-info/entry_points.txt
--rw-r--r--   0 pi        (1000) pi        (1000)       14 2023-07-04 05:28:32.000000 cgpmgr-1.6/cgpmgr.egg-info/requires.txt
--rw-r--r--   0 pi        (1000) pi        (1000)        7 2023-07-04 05:28:32.000000 cgpmgr-1.6/cgpmgr.egg-info/top_level.txt
--rw-r--r--   0 pi        (1000) pi        (1000)       38 2023-07-04 05:28:33.150441 cgpmgr-1.6/setup.cfg
--rwxr-xr-x   0 pi        (1000) pi        (1000)      478 2023-07-04 05:26:27.000000 cgpmgr-1.6/setup.py
+drwxr-xr-x   0 pi        (1000) pi        (1000)        0 2023-07-23 00:17:58.609625 cgpmgr-1.7/
+-rw-r--r--   0 pi        (1000) pi        (1000)    11342 2021-09-04 14:18:09.000000 cgpmgr-1.7/LICENSE
+-rw-r--r--   0 pi        (1000) pi        (1000)      307 2023-07-23 00:17:58.599625 cgpmgr-1.7/PKG-INFO
+-rw-r--r--   0 pi        (1000) pi        (1000)     2812 2023-06-05 04:58:21.000000 cgpmgr-1.7/README.md
+drwxr-xr-x   0 pi        (1000) pi        (1000)        0 2023-07-23 00:17:58.589625 cgpmgr-1.7/cgpmgr/
+-rwxr-xr-x   0 pi        (1000) pi        (1000)       19 2021-09-05 05:17:17.000000 cgpmgr-1.7/cgpmgr/__init__.py
+-rwxr-xr-x   0 pi        (1000) pi        (1000)    31286 2023-07-23 00:16:20.000000 cgpmgr-1.7/cgpmgr/cli.py
+drwxr-xr-x   0 pi        (1000) pi        (1000)        0 2023-07-23 00:17:58.599625 cgpmgr-1.7/cgpmgr.egg-info/
+-rw-r--r--   0 pi        (1000) pi        (1000)      307 2023-07-23 00:17:58.000000 cgpmgr-1.7/cgpmgr.egg-info/PKG-INFO
+-rw-r--r--   0 pi        (1000) pi        (1000)      241 2023-07-23 00:17:58.000000 cgpmgr-1.7/cgpmgr.egg-info/SOURCES.txt
+-rw-r--r--   0 pi        (1000) pi        (1000)        1 2023-07-23 00:17:58.000000 cgpmgr-1.7/cgpmgr.egg-info/dependency_links.txt
+-rw-r--r--   0 pi        (1000) pi        (1000)       38 2023-07-23 00:17:58.000000 cgpmgr-1.7/cgpmgr.egg-info/entry_points.txt
+-rw-r--r--   0 pi        (1000) pi        (1000)       14 2023-07-23 00:17:58.000000 cgpmgr-1.7/cgpmgr.egg-info/requires.txt
+-rw-r--r--   0 pi        (1000) pi        (1000)        7 2023-07-23 00:17:58.000000 cgpmgr-1.7/cgpmgr.egg-info/top_level.txt
+-rw-r--r--   0 pi        (1000) pi        (1000)       38 2023-07-23 00:17:58.609625 cgpmgr-1.7/setup.cfg
+-rwxr-xr-x   0 pi        (1000) pi        (1000)      478 2023-07-23 00:08:53.000000 cgpmgr-1.7/setup.py
```

### Comparing `cgpmgr-1.6/LICENSE` & `cgpmgr-1.7/LICENSE`

 * *Files identical despite different names*

### Comparing `cgpmgr-1.6/README.md` & `cgpmgr-1.7/README.md`

 * *Files identical despite different names*

### Comparing `cgpmgr-1.6/cgpmgr/cli.py` & `cgpmgr-1.7/cgpmgr/cli.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 """
 Raspberry Pi/Jetson Nano電源管理 拡張基板 RPZ-PowerMGR用コントロールツール
 Indoor Corgi, https://www.indoorcorgielec.com
 GitHub: https://github.com/IndoorCorgi/cgpmgr
-Version 1.6
+Version 1.7
 
 必要環境:
 1) Raspberry Pi OS / Jetson Linux, Python3
 2) I2Cインターフェース
   Raspberry PiでI2Cを有効にする方法
   https://www.indoorcorgielec.com/resources/raspberry-pi/raspberry-pi-i2c/
 3) 電源管理 拡張基板 RPZ-PowerMGR
@@ -77,15 +77,15 @@
 import struct
 import subprocess
 import hashlib
 import smbus2
 import RPi.GPIO as GPIO
 
 i2c_adr = 0x20
-compatible_fw = {1: 6, 2: 3}
+compatible_fw = {1: 7, 2: 4}
 sig2gpio = [0, 16, 17, 26, 27]  # SIG番号とGPIO番号の対応
 dow2str = ['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat']  # スケジュールデータは日曜が1, 土曜が7
 gpio_rst = 7
 gpio_boot = 25
 fw_ver = []
 
 # ファームウェアハッシュ値
@@ -93,18 +93,20 @@
     'cf0d1818ade696bc5b7af150ff4a085266fdc829f196f26ed2ed127b7ba12eb3',  # Ver1.0
     '1a6fdf815b5b23a6e39c79d6b734bfd3bd51ddf59b803912425bfc07504f0d1b',  # Ver1.1
     '5764c3cc8442930997fefcc048e35a8242df9bdcdf5f302ed4fb43f1a4fd8c24',  # Ver1.2
     'a37fe6f36a4e99bab07e3106cb99306d13f88d4c72c68b309a4fd9eb8e4c44e8',  # Ver1.3
     '36313403baab9d50183f17d0f9cea991455baf7b1b0478e1ef8773cee0ea91cc',  # Ver1.4
     'c3f465e5c8e2e004b23d85a6f5846931e106fd8a06715d48e54750c875cfe882',  # Ver1.5
     '6aff47c6ceb831cf48662a71dcc0090b437a6129aa8b29d5bcebb5e0cd46e98b',  # Ver1.6
+    '14fcce2876dc004f5598d50d36eef4898e048197566a5de319ede510019df031',  # Ver1.7
     '0bdb41e819fcd8380a9bf1f551a6a7692bd22bcdb3734580413e4401fa613490',  # Ver2.0
     'f5aa9ab42affd8004238bf1f747d93095b5138602473660eb7965a24d03b167b',  # Ver2.1
     'a49c1fa3c1f540fcbb77d69be4d599791d3a5a88508e7519aaab2c5426f0fb0c',  # Ver2.2
     'c39cc7100644abafd3f69bc0b61304093b4a535097fd637282837ed8fe007821',  # Ver2.3
+    '39498cf80856838cf9676c0e40316d1e7ae283d03179d1d538d1cca992a0e9cc',  # Ver2.4
 ]
 
 
 def cli():
   """
   コマンドラインツールを実行
   """
```

