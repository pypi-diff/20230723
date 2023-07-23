# Comparing `tmp/energon_prometheus_exporter-0.0.1.tar.gz` & `tmp/energon_prometheus_exporter-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "energon_prometheus_exporter-0.0.1.tar", last modified: Wed Jul 19 00:40:31 2023, max compression
+gzip compressed data, was "energon_prometheus_exporter-0.0.2.tar", last modified: Sun Jul 23 06:12:31 2023, max compression
```

## Comparing `energon_prometheus_exporter-0.0.1.tar` & `energon_prometheus_exporter-0.0.2.tar`

### file list

```diff
@@ -1,30 +1,30 @@
-drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-19 00:40:31.156629 energon_prometheus_exporter-0.0.1/
--rw-rw-r--   0 matteo    (1000) matteo    (1000)     1074 2023-07-19 00:17:29.000000 energon_prometheus_exporter-0.0.1/LICENSE
--rw-rw-r--   0 matteo    (1000) matteo    (1000)     5999 2023-07-19 00:40:31.156629 energon_prometheus_exporter-0.0.1/PKG-INFO
--rw-rw-r--   0 matteo    (1000) matteo    (1000)     5259 2023-07-18 23:51:24.000000 energon_prometheus_exporter-0.0.1/README.md
--rw-rw-r--   0 matteo    (1000) matteo    (1000)      793 2023-07-19 00:19:24.000000 energon_prometheus_exporter-0.0.1/pyproject.toml
--rw-rw-r--   0 matteo    (1000) matteo    (1000)       38 2023-07-19 00:40:31.156629 energon_prometheus_exporter-0.0.1/setup.cfg
-drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-19 00:40:31.152629 energon_prometheus_exporter-0.0.1/src/
-drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-19 00:40:31.152629 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/
--rw-rw-r--   0 matteo    (1000) matteo    (1000)        0 2023-07-18 23:48:13.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/__ init __.py
-drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-19 00:40:31.152629 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/drivers/
--rw-rw-r--   0 matteo    (1000) matteo    (1000)     1912 2023-07-18 17:47:19.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/drivers/UM25C.py
--rw-rw-r--   0 matteo    (1000) matteo    (1000)        0 2023-07-18 17:47:19.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/drivers/__ init __.py
--rw-rw-r--   0 matteo    (1000) matteo    (1000)      402 2023-07-18 17:47:19.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/drivers/constants.py
--rw-rw-r--   0 matteo    (1000) matteo    (1000)     4304 2023-07-19 00:38:20.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/drivers/driver.py
--rw-rw-r--   0 matteo    (1000) matteo    (1000)     2845 2023-07-19 00:38:30.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/drivers/utils.py
-drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-19 00:40:31.156629 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/
--rw-rw-r--   0 matteo    (1000) matteo    (1000)        0 2023-07-18 17:47:19.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/__ init __.py
--rw-rw-r--   0 matteo    (1000) matteo    (1000)    11050 2023-07-19 00:37:10.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/general_model.py
--rw-rw-r--   0 matteo    (1000) matteo    (1000)    11948 2023-07-19 00:37:25.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/jetson_agx_orin.py
--rw-rw-r--   0 matteo    (1000) matteo    (1000)    10812 2023-07-19 00:37:37.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/jetson_agx_xavier.py
--rw-rw-r--   0 matteo    (1000) matteo    (1000)     5843 2023-07-19 00:37:45.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/jetson_nano_dev_kit.py
--rw-rw-r--   0 matteo    (1000) matteo    (1000)     6246 2023-07-19 00:37:48.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/jetson_xavier_dev_kit.py
--rw-rw-r--   0 matteo    (1000) matteo    (1000)     4770 2023-07-19 00:37:53.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/ubuntu_64.py
--rw-rw-r--   0 matteo    (1000) matteo    (1000)    11639 2023-07-19 00:23:03.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/prometheus_exporter.py
-drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-19 00:40:31.152629 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter.egg-info/
--rw-rw-r--   0 matteo    (1000) matteo    (1000)     5999 2023-07-19 00:40:31.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter.egg-info/PKG-INFO
--rw-rw-r--   0 matteo    (1000) matteo    (1000)     1067 2023-07-19 00:40:31.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter.egg-info/SOURCES.txt
--rw-rw-r--   0 matteo    (1000) matteo    (1000)        1 2023-07-19 00:40:31.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter.egg-info/dependency_links.txt
--rw-rw-r--   0 matteo    (1000) matteo    (1000)       40 2023-07-19 00:40:31.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter.egg-info/requires.txt
--rw-rw-r--   0 matteo    (1000) matteo    (1000)       28 2023-07-19 00:40:31.000000 energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter.egg-info/top_level.txt
+drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-23 06:12:31.321730 energon_prometheus_exporter-0.0.2/
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)     1074 2023-07-19 00:17:29.000000 energon_prometheus_exporter-0.0.2/LICENSE
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)     6137 2023-07-23 06:12:31.321730 energon_prometheus_exporter-0.0.2/PKG-INFO
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)     5397 2023-07-19 00:45:09.000000 energon_prometheus_exporter-0.0.2/README.md
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)      793 2023-07-23 06:12:25.000000 energon_prometheus_exporter-0.0.2/pyproject.toml
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)       38 2023-07-23 06:12:31.321730 energon_prometheus_exporter-0.0.2/setup.cfg
+drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-23 06:12:31.321730 energon_prometheus_exporter-0.0.2/src/
+drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-23 06:12:31.321730 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)        0 2023-07-18 23:48:13.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/__ init __.py
+drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-23 06:12:31.321730 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/drivers/
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)     1912 2023-07-18 17:47:19.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/drivers/UM25C.py
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)        0 2023-07-18 17:47:19.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/drivers/__ init __.py
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)      402 2023-07-18 17:47:19.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/drivers/constants.py
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)     4304 2023-07-19 00:38:20.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/drivers/driver.py
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)     2845 2023-07-19 00:38:30.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/drivers/utils.py
+drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-23 06:12:31.321730 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)        0 2023-07-18 17:47:19.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/__ init __.py
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)    11192 2023-07-23 06:09:12.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/general_model.py
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)    11948 2023-07-19 00:37:25.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/jetson_agx_orin.py
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)    10812 2023-07-19 00:37:37.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/jetson_agx_xavier.py
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)     5843 2023-07-19 00:37:45.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/jetson_nano_dev_kit.py
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)     6246 2023-07-19 00:37:48.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/jetson_xavier_dev_kit.py
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)     4770 2023-07-19 00:37:53.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/ubuntu_64.py
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)    14408 2023-07-23 06:07:50.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/prometheus_exporter.py
+drwxrwxr-x   0 matteo    (1000) matteo    (1000)        0 2023-07-23 06:12:31.321730 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter.egg-info/
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)     6137 2023-07-23 06:12:31.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter.egg-info/PKG-INFO
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)     1067 2023-07-23 06:12:31.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter.egg-info/SOURCES.txt
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)        1 2023-07-23 06:12:31.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter.egg-info/dependency_links.txt
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)       40 2023-07-23 06:12:31.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter.egg-info/requires.txt
+-rw-rw-r--   0 matteo    (1000) matteo    (1000)       28 2023-07-23 06:12:31.000000 energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter.egg-info/top_level.txt
```

### Comparing `energon_prometheus_exporter-0.0.1/LICENSE` & `energon_prometheus_exporter-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `energon_prometheus_exporter-0.0.1/PKG-INFO` & `energon_prometheus_exporter-0.0.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 00000000: 4d65 7461 6461 7461 2d56 6572 7369 6f6e  Metadata-Version
 00000010: 3a20 322e 310a 4e61 6d65 3a20 656e 6572  : 2.1.Name: ener
 00000020: 676f 6e5f 7072 6f6d 6574 6865 7573 5f65  gon_prometheus_e
 00000030: 7870 6f72 7465 720a 5665 7273 696f 6e3a  xporter.Version:
-00000040: 2030 2e30 2e31 0a53 756d 6d61 7279 3a20   0.0.1.Summary: 
+00000040: 2030 2e30 2e32 0a53 756d 6d61 7279 3a20   0.0.2.Summary: 
 00000050: 456e 6572 676f 6e20 6973 2061 2050 726f  Energon is a Pro
 00000060: 6d65 7468 6575 7320 636f 6d70 6c69 616e  metheus complian
 00000070: 7420 7379 7374 656d 206d 6f6e 6974 6f72  t system monitor
 00000080: 696e 6720 746f 6f6c 732c 2069 7420 666f  ing tools, it fo
 00000090: 6375 7365 7320 6f6e 2074 6865 2065 6e65  cuses on the ene
 000000a0: 7267 7920 636f 6e73 756d 7074 696f 6e20  rgy consumption 
 000000b0: 616e 6420 7265 736f 7572 6365 2075 7361  and resource usa
@@ -161,215 +161,224 @@
 00000a00: 7920 6060 6020 666f 7220 7275 6e6e 696e  y ``` for runnin
 00000a10: 6720 6120 7369 6e67 6c65 206d 6574 7269  g a single metri
 00000a20: 6320 7363 616e 3b0a 2d20 5275 6e3a 2060  c scan;.- Run: `
 00000a30: 6060 2073 7564 6f20 7079 7468 6f6e 3320  `` sudo python3 
 00000a40: 7072 6f6d 6574 6865 7573 5f65 7870 6f72  prometheus_expor
 00000a50: 7465 722e 7079 2060 6060 2066 6f72 2072  ter.py ``` for r
 00000a60: 756e 6e69 6e67 2074 6865 2070 726f 6d65  unning the prome
-00000a70: 7468 6575 7320 6578 706f 7274 6572 3b0a  theus exporter;.
-00000a80: 0a23 2323 2320 5769 7468 2070 6970 2069  .#### With pip i
-00000a90: 6e73 7461 6c6c 0a2d 2060 6060 2070 6970  nstall.- ``` pip
-00000aa0: 3320 696e 7374 616c 6c20 456e 6572 676f  3 install Energo
-00000ab0: 6e2d 5072 6f6d 6574 6865 7573 2d65 7870  n-Prometheus-exp
-00000ac0: 6f72 7465 7220 6060 603b 0a2d 2060 6060  orter ```;.- ```
-00000ad0: 2066 726f 6d20 456e 6572 676f 6e5f 5072   from Energon_Pr
-00000ae0: 6f6d 6574 6865 7573 5f65 7870 6f72 7465  ometheus_exporte
-00000af0: 7220 696d 706f 7274 2063 6f6e 7374 616e  r import constan
-00000b00: 7473 6060 600a 0a54 6865 2061 7070 6c69  ts```..The appli
-00000b10: 6361 7469 6f6e 2072 6571 7569 7265 7320  cation requires 
-00000b20: 7375 646f 2070 7269 7669 6c65 6765 7320  sudo privileges 
-00000b30: 746f 2061 6363 6573 7320 746f 2073 6f6d  to access to som
-00000b40: 6520 7379 7374 656d 2066 696c 6573 2e0a  e system files..
-00000b50: 596f 7520 6361 6e20 7374 696c 6c20 7275  You can still ru
-00000b60: 6e20 7468 6520 6170 706c 6963 6174 696f  n the applicatio
-00000b70: 6e20 7769 7468 6f75 7420 7375 646f 2070  n without sudo p
-00000b80: 7269 7669 6c65 6765 7320 6275 7420 736f  rivileges but so
-00000b90: 6d65 206d 6574 7269 6373 2077 696c 6c20  me metrics will 
-00000ba0: 6e6f 7420 6265 2061 7661 696c 6162 6c65  not be available
-00000bb0: 2e0a 0a23 2320 4375 7272 656e 746c 7920  ...## Currently 
-00000bc0: 7375 7070 6f72 7465 6420 6665 6174 7572  supported featur
-00000bd0: 6573 3a0a 416c 6c20 6d65 7472 6963 7320  es:.All metrics 
-00000be0: 6e61 6d65 7320 6172 6520 636f 6d70 6c69  names are compli
-00000bf0: 6174 2077 6974 6820 7072 6f6d 6574 6865  at with promethe
-00000c00: 7573 2073 7065 6369 6669 6361 7469 6f6e  us specification
-00000c10: 7320 6173 2064 6573 6372 6962 6564 2069  s as described i
-00000c20: 6e20 5b68 7474 7073 3a2f 2f70 726f 6d65  n [https://prome
-00000c30: 7468 6575 732e 696f 2f64 6f63 732f 7072  theus.io/docs/pr
-00000c40: 6163 7469 6365 732f 6e61 6d69 6e67 2f5d  actices/naming/]
-00000c50: 2e0a 0a23 2323 2045 6e65 7267 7920 6d65  ...### Energy me
-00000c60: 7472 6963 733a 0a2d 2065 6e65 7267 6f6e  trics:.- energon
-00000c70: 5f64 6576 6963 655f 696e 666f 3a20 6465  _device_info: de
-00000c80: 7669 6365 2069 6e66 6f72 6d61 7469 6f6e  vice information
-00000c90: 3b0a 2d20 656e 6572 676f 6e5f 746f 7461  ;.- energon_tota
-00000ca0: 6c5f 696e 5f70 6f77 6572 5f6d 573a 2063  l_in_power_mW: c
-00000cb0: 7572 7265 6e74 2074 6f74 616c 2070 6f77  urrent total pow
-00000cc0: 6572 2063 6f6e 7375 6d70 7469 6f6e 2069  er consumption i
-00000cd0: 6e20 6d69 6c6c 6977 6174 7473 3b0a 2d20  n milliwatts;.- 
-00000ce0: 656e 6572 676f 6e5f 6370 755f 696e 5f70  energon_cpu_in_p
-00000cf0: 6f77 6572 5f6d 573a 2063 7572 7265 6e74  ower_mW: current
-00000d00: 2063 7075 2070 6f77 6572 2063 6f6e 7375   cpu power consu
-00000d10: 6d70 7469 6f6e 2069 6e20 6d69 6c6c 6977  mption in milliw
-00000d20: 6174 7473 3b0a 2d20 656e 6572 676f 6e5f  atts;.- energon_
-00000d30: 6770 755f 696e 5f70 6f77 6572 5f6d 573a  gpu_in_power_mW:
-00000d40: 2063 7572 7265 6e74 2067 7075 2070 6f77   current gpu pow
-00000d50: 6572 2063 6f6e 7375 6d70 7469 6f6e 2069  er consumption i
-00000d60: 6e20 6d69 6c6c 6977 6174 7473 3b0a 2d20  n milliwatts;.- 
-00000d70: 656e 6572 676f 6e5f 746f 7461 6c5f 696e  energon_total_in
-00000d80: 5f76 6f6c 7461 6765 5f6d 563a 2063 7572  _voltage_mV: cur
-00000d90: 7265 6e74 2074 6f74 616c 2076 6f6c 7461  rent total volta
-00000da0: 6765 2069 6e20 6d69 6c6c 6976 6f6c 7473  ge in millivolts
-00000db0: 3b0a 2d20 656e 6572 676f 6e5f 6370 755f  ;.- energon_cpu_
-00000dc0: 696e 5f76 6f6c 7461 6765 5f6d 563a 2063  in_voltage_mV: c
-00000dd0: 7572 7265 6e74 2063 7075 2076 6f6c 7461  urrent cpu volta
-00000de0: 6765 2069 6e20 6d69 6c6c 6976 6f6c 7473  ge in millivolts
-00000df0: 3b0a 2d20 656e 6572 676f 6e5f 6770 755f  ;.- energon_gpu_
-00000e00: 696e 5f76 6f6c 7461 6765 5f6d 563a 2063  in_voltage_mV: c
-00000e10: 7572 7265 6e74 2067 7075 2076 6f6c 7461  urrent gpu volta
-00000e20: 6765 2069 6e20 6d69 6c6c 6976 6f6c 7473  ge in millivolts
-00000e30: 3b0a 2d20 656e 6572 676f 6e5f 6261 7474  ;.- energon_batt
-00000e40: 6572 795f 7065 7263 656e 7461 6765 3a20  ery_percentage: 
-00000e50: 6375 7272 656e 7420 6261 7474 6572 7920  current battery 
-00000e60: 7065 7263 656e 7461 6765 2e0a 0a23 2323  percentage...###
-00000e70: 2055 5342 2054 6573 7465 7220 554d 3235   USB Tester UM25
-00000e80: 4320 5553 4220 4d65 7465 7220 5465 7374  C USB Meter Test
-00000e90: 6572 206d 6574 7269 6373 3a0a 4e2e 422e  er metrics:.N.B.
-00000ea0: 204f 6e6c 7920 6966 2072 6561 6c20 7365   Only if real se
-00000eb0: 6e73 6f72 2069 7320 636f 6e6e 6563 7465  nsor is connecte
-00000ec0: 6421 0a2d 2065 6e65 7267 6f6e 5f74 6f74  d!.- energon_tot
-00000ed0: 616c 5f61 6374 7561 6c5f 7761 7474 733a  al_actual_watts:
-00000ee0: 2074 6f74 616c 2061 6374 7561 6c20 706f   total actual po
-00000ef0: 7765 7220 636f 6e73 756d 7074 696f 6e20  wer consumption 
-00000f00: 696e 2077 6174 7473 3b0a 2d20 656e 6572  in watts;.- ener
-00000f10: 676f 6e5f 746f 7461 6c5f 6163 7475 616c  gon_total_actual
-00000f20: 5f76 6f6c 7473 3a20 746f 7461 6c20 6163  _volts: total ac
-00000f30: 7475 616c 2076 6f6c 7461 6765 2069 6e20  tual voltage in 
-00000f40: 766f 6c74 733b 0a2d 2065 6e65 7267 6f6e  volts;.- energon
-00000f50: 5f74 6f74 616c 5f61 6374 7561 6c5f 616d  _total_actual_am
-00000f60: 7073 3a20 746f 7461 6c20 6163 7475 616c  ps: total actual
-00000f70: 2063 7572 7265 6e74 2069 6e20 616d 7073   current in amps
-00000f80: 2e0a 0a23 2323 204e 6574 776f 726b 206d  ...### Network m
-00000f90: 6574 7269 6373 3a0a 466f 7220 6561 6368  etrics:.For each
-00000fa0: 2069 6e74 6572 6661 6365 5f6e 616d 650a   interface_name.
-00000fb0: 2d20 6e65 7477 6f72 6b5f 6d65 7472 6963  - network_metric
-00000fc0: 735f 5b69 6e74 6572 6661 6365 5f6e 616d  s_[interface_nam
-00000fd0: 655d 5f72 785f 7061 636b 6574 733a 2072  e]_rx_packets: r
-00000fe0: 6563 6569 7665 6420 7061 636b 6574 733b  eceived packets;
-00000ff0: 0a2d 206e 6574 776f 726b 5f6d 6574 7269  .- network_metri
-00001000: 6373 5f5b 696e 7465 7266 6163 655f 6e61  cs_[interface_na
-00001010: 6d65 5d5f 7278 5f62 7974 6573 3a20 7265  me]_rx_bytes: re
-00001020: 6365 6976 6564 2062 7974 6573 3b0a 2d20  ceived bytes;.- 
-00001030: 6e65 7477 6f72 6b5f 6d65 7472 6963 735f  network_metrics_
-00001040: 5b69 6e74 6572 6661 6365 5f6e 616d 655d  [interface_name]
-00001050: 5f72 785f 6572 726f 7273 3a20 7265 6365  _rx_errors: rece
-00001060: 6976 6564 2065 7272 6f72 733b 0a2d 206e  ived errors;.- n
-00001070: 6574 776f 726b 5f6d 6574 7269 6373 5f5b  etwork_metrics_[
-00001080: 696e 7465 7266 6163 655f 6e61 6d65 5d5f  interface_name]_
-00001090: 7278 5f64 726f 7070 6564 3a20 7265 6365  rx_dropped: rece
-000010a0: 6976 6564 2064 726f 7070 6564 2070 6163  ived dropped pac
-000010b0: 6b65 7473 3b0a 2d20 6e65 7477 6f72 6b5f  kets;.- network_
-000010c0: 6d65 7472 6963 735f 5b69 6e74 6572 6661  metrics_[interfa
-000010d0: 6365 5f6e 616d 655d 5f74 785f 7061 636b  ce_name]_tx_pack
-000010e0: 6574 733a 2074 7261 6e73 6d69 7474 6564  ets: transmitted
-000010f0: 2070 6163 6b65 7473 3b0a 2d20 6e65 7477   packets;.- netw
-00001100: 6f72 6b5f 6d65 7472 6963 735f 5b69 6e74  ork_metrics_[int
-00001110: 6572 6661 6365 5f6e 616d 655d 5f74 785f  erface_name]_tx_
-00001120: 6279 7465 733a 2074 7261 736d 6974 7465  bytes: trasmitte
-00001130: 6420 6279 7465 733b 0a2d 206e 6574 776f  d bytes;.- netwo
-00001140: 726b 5f6d 6574 7269 6373 5f5b 696e 7465  rk_metrics_[inte
-00001150: 7266 6163 655f 6e61 6d65 5d5f 7478 5f65  rface_name]_tx_e
-00001160: 7272 6f72 733a 2074 7261 6e73 6d69 7474  rrors: transmitt
-00001170: 6564 2065 7272 6f72 733b 0a2d 206e 6574  ed errors;.- net
-00001180: 776f 726b 5f6d 6574 7269 6373 5f5b 696e  work_metrics_[in
-00001190: 7465 7266 6163 655f 6e61 6d65 5d5f 7478  terface_name]_tx
-000011a0: 5f64 726f 7070 6564 3a20 7472 616e 736d  _dropped: transm
-000011b0: 6974 7465 6420 6472 6f70 7065 6420 7061  itted dropped pa
-000011c0: 636b 6574 732e 0a0a 2323 2320 4370 7520  ckets...### Cpu 
-000011d0: 7573 6167 653a 0a46 6f72 2065 6163 6820  usage:.For each 
-000011e0: 636f 7265 5f6e 756d 6265 720a 2d20 656e  core_number.- en
-000011f0: 6572 676f 6e5f 6370 755f 5b63 6f72 655f  ergon_cpu_[core_
-00001200: 6e75 6d62 6572 5d5f 4d48 7a3a 2063 7075  number]_MHz: cpu
-00001210: 2066 7265 7175 656e 6379 2069 6e20 4d48   frequency in MH
-00001220: 7a20 666f 7220 636f 7265 205b 636f 7265  z for core [core
-00001230: 5f6e 756d 6265 725d 3b0a 2d20 656e 6572  _number];.- ener
-00001240: 676f 6e5f 6370 755f 5b63 6f72 655f 6e75  gon_cpu_[core_nu
-00001250: 6d62 6572 5d5f 7573 6167 655f 7065 7263  mber]_usage_perc
-00001260: 656e 7461 6765 3a20 4350 5520 7573 6167  entage: CPU usag
-00001270: 6520 6173 2025 2066 6f72 2063 6f72 6520  e as % for core 
-00001280: 5b63 6f72 655f 6e75 6d62 6572 5d2e 0a54  [core_number]..T
-00001290: 6f74 616c 0a2d 2065 6e65 7267 6f6e 5f63  otal.- energon_c
-000012a0: 7075 5f74 6f74 616c 5f75 7361 6765 5f70  pu_total_usage_p
-000012b0: 6572 6365 6e74 6167 653a 2074 6f74 616c  ercentage: total
-000012c0: 2043 5055 2075 7361 6765 2061 7320 252e   CPU usage as %.
-000012d0: 0a0a 2323 2320 5374 6f72 6167 653a 0a46  ..### Storage:.F
-000012e0: 6f72 2065 6163 6820 6176 6169 6c61 626c  or each availabl
-000012f0: 6520 5b73 746f 7261 6765 5f64 6576 6963  e [storage_devic
-00001300: 655d 0a2d 2065 6e65 7267 6f6e 5f73 746f  e].- energon_sto
-00001310: 7261 6765 5f5b 7374 6f72 6167 655f 6465  rage_[storage_de
-00001320: 7669 6365 5d5f 746f 7461 6c5f 6279 7465  vice]_total_byte
-00001330: 733a 2074 6f74 616c 2062 7974 6573 2066  s: total bytes f
-00001340: 6f72 2073 746f 7261 6765 205b 7374 6f72  or storage [stor
-00001350: 6167 655f 6465 7669 6365 5d3b 0a2d 2065  age_device];.- e
-00001360: 6e65 7267 6f6e 5f73 746f 7261 6765 5f5b  nergon_storage_[
-00001370: 7374 6f72 6167 655f 6465 7669 6365 5d5f  storage_device]_
-00001380: 7573 6564 5f62 7974 6573 3a20 7573 6564  used_bytes: used
-00001390: 2062 7974 6573 2066 6f72 2073 746f 7261   bytes for stora
-000013a0: 6765 205b 7374 6f72 6167 655f 6465 7669  ge [storage_devi
-000013b0: 6365 5d3b 0a2d 2065 6e65 7267 6f6e 5f73  ce];.- energon_s
-000013c0: 746f 7261 6765 5f5b 7374 6f72 6167 655f  torage_[storage_
-000013d0: 6465 7669 6365 5d5f 6176 6169 6c61 626c  device]_availabl
-000013e0: 655f 6279 7465 733a 2061 7661 696c 6162  e_bytes: availab
-000013f0: 6c65 2062 7974 6573 2066 6f72 2073 746f  le bytes for sto
-00001400: 7261 6765 205b 7374 6f72 6167 655f 6465  rage [storage_de
-00001410: 7669 6365 5d3b 0a2d 2065 6e65 7267 6f6e  vice];.- energon
-00001420: 5f73 746f 7261 6765 5f5b 7374 6f72 6167  _storage_[storag
-00001430: 655f 6465 7669 6365 5d5f 7065 7263 656e  e_device]_percen
-00001440: 745f 7573 6564 5f70 6572 6365 6e74 6167  t_used_percentag
-00001450: 653a 2073 746f 7261 6765 2075 7361 6765  e: storage usage
-00001460: 2070 6572 6365 6e74 6167 6520 666f 7220   percentage for 
-00001470: 7374 6f72 6167 6520 5b73 746f 7261 6765  storage [storage
-00001480: 5f64 6576 6963 655d 2e0a 546f 7461 6c0a  _device]..Total.
-00001490: 2d20 656e 6572 676f 6e5f 7374 6f72 6167  - energon_storag
-000014a0: 655f 746f 7461 6c5f 6279 7465 733a 2074  e_total_bytes: t
-000014b0: 6f74 616c 2073 746f 7261 6765 2069 6e20  otal storage in 
-000014c0: 6279 7465 733b 0a2d 2065 6e65 7267 6f6e  bytes;.- energon
-000014d0: 5f73 746f 7261 6765 5f75 7365 645f 6279  _storage_used_by
-000014e0: 7465 733a 2074 6f74 616c 2075 7365 6420  tes: total used 
-000014f0: 7374 6f72 6167 6520 696e 2062 7974 6573  storage in bytes
-00001500: 3b0a 2d20 656e 6572 676f 6e5f 7374 6f72  ;.- energon_stor
-00001510: 6167 655f 6176 6169 6c61 626c 655f 6279  age_available_by
-00001520: 7465 733a 2074 6f74 616c 2061 7661 696c  tes: total avail
-00001530: 6162 6c65 2073 746f 7261 6765 2069 6e20  able storage in 
-00001540: 6279 7465 733b 0a2d 2065 6e65 7267 6f6e  bytes;.- energon
-00001550: 5f73 746f 7261 6765 5f70 6572 6365 6e74  _storage_percent
-00001560: 5f75 7365 645f 7065 7263 656e 7461 6765  _used_percentage
-00001570: 3a20 5374 6f72 6167 6520 7573 6167 6520  : Storage usage 
-00001580: 7065 7263 656e 7461 6765 2e0a 0a23 2323  percentage...###
-00001590: 2052 616d 2075 7361 6765 3a0a 2d20 656e   Ram usage:.- en
-000015a0: 6572 676f 6e5f 7261 6d5f 746f 7461 6c5f  ergon_ram_total_
-000015b0: 6279 7465 733a 2074 6f74 616c 2072 616d  bytes: total ram
-000015c0: 2069 6e20 6279 7465 733b 0a2d 2065 6e65   in bytes;.- ene
-000015d0: 7267 6f6e 5f72 616d 5f75 7365 645f 6279  rgon_ram_used_by
-000015e0: 7465 733a 2074 6f74 616c 2075 7365 6420  tes: total used 
-000015f0: 7261 6d20 696e 2062 7974 6573 3b0a 2d20  ram in bytes;.- 
-00001600: 656e 6572 676f 6e5f 7261 6d5f 6176 6169  energon_ram_avai
-00001610: 6c61 626c 655f 6279 7465 733a 2074 6f74  lable_bytes: tot
-00001620: 616c 2061 7661 696c 6162 6c65 2072 616d  al available ram
-00001630: 2069 6e20 6279 7465 733b 0a2d 2065 6e65   in bytes;.- ene
-00001640: 7267 6f6e 5f72 616d 5f75 7365 645f 7065  rgon_ram_used_pe
-00001650: 7263 656e 7461 6765 3a20 7261 6d20 7573  rcentage: ram us
-00001660: 6167 6520 7065 7263 656e 7461 6765 2e0a  age percentage..
-00001670: 0a23 2323 2047 5055 206d 6574 7269 6373  .### GPU metrics
-00001680: 3a0a 2d20 656e 6572 676f 6e5f 6770 755f  :.- energon_gpu_
-00001690: 746f 7461 6c5f 7573 6167 655f 7065 7263  total_usage_perc
-000016a0: 656e 7461 6765 3a20 746f 7461 6c20 4750  entage: total GP
-000016b0: 5520 7573 6167 6520 6173 2025 2e0a 0a23  U usage as %...#
-000016c0: 2323 2054 656d 7065 7261 7475 7265 206d  ## Temperature m
-000016d0: 6574 7269 6373 3a0a 466f 7220 6561 6368  etrics:.For each
-000016e0: 2061 7661 696c 6162 6c65 205b 7465 6d70   available [temp
-000016f0: 6572 6174 7572 655f 7365 6e73 6f72 5d0a  erature_sensor].
-00001700: 2d20 656e 6572 676f 6e5f 7465 6d70 6572  - energon_temper
-00001710: 6174 7572 655f 5b74 656d 7065 7261 7475  ature_[temperatu
-00001720: 7265 5f73 656e 736f 725d 5f6d 433a 2074  re_sensor]_mC: t
-00001730: 656d 7065 7261 7475 7265 2069 6e20 6d69  emperature in mi
-00001740: 6c6c 6943 656c 7369 7573 2066 6f72 2073  lliCelsius for s
-00001750: 656e 736f 7220 5b74 656d 7065 7261 7475  ensor [temperatu
-00001760: 7265 5f73 656e 736f 725d 2e0a 0a0a 0a    re_sensor].....
+00000a70: 7468 6575 7320 6578 706f 7274 6572 206f  theus exporter o
+00000a80: 6e20 6465 6661 756c 7420 706f 7274 2039  n default port 9
+00000a90: 3837 373b 0a0a 2323 2323 2057 6974 6820  877;..#### With 
+00000aa0: 7069 7020 696e 7374 616c 6c0a 2d20 6060  pip install.- ``
+00000ab0: 6020 7069 7033 2069 6e73 7461 6c6c 2045  ` pip3 install E
+00000ac0: 6e65 7267 6f6e 2d50 726f 6d65 7468 6575  nergon-Prometheu
+00000ad0: 732d 6578 706f 7274 6572 2060 6060 3b0a  s-exporter ```;.
+00000ae0: 6060 6020 0a66 726f 6d20 656e 6572 676f  ``` .from energo
+00000af0: 6e5f 7072 6f6d 6574 6865 7573 5f65 7870  n_prometheus_exp
+00000b00: 6f72 7465 722e 7072 6f6d 6574 6865 7573  orter.prometheus
+00000b10: 5f65 7870 6f72 7465 7220 696d 706f 7274  _exporter import
+00000b20: 2045 6e65 7267 6f6e 5072 6f6d 6574 6865   EnergonPromethe
+00000b30: 7573 4578 706f 7274 6572 200a 7365 7276  usExporter .serv
+00000b40: 6572 5f65 7870 6f72 7465 7220 3d20 456e  er_exporter = En
+00000b50: 6572 676f 6e50 726f 6d65 7468 6575 7345  ergonPrometheusE
+00000b60: 7870 6f72 7465 7228 4445 5349 5245 445f  xporter(DESIRED_
+00000b70: 504f 5254 290a 7365 7276 6572 5f65 7870  PORT).server_exp
+00000b80: 6f72 7465 722e 7275 6e28 290a 6060 600a  orter.run().```.
+00000b90: 0a54 6865 2061 7070 6c69 6361 7469 6f6e  .The application
+00000ba0: 2072 6571 7569 7265 7320 7375 646f 2070   requires sudo p
+00000bb0: 7269 7669 6c65 6765 7320 746f 2061 6363  rivileges to acc
+00000bc0: 6573 7320 746f 2073 6f6d 6520 7379 7374  ess to some syst
+00000bd0: 656d 2066 696c 6573 2e0a 596f 7520 6361  em files..You ca
+00000be0: 6e20 7374 696c 6c20 7275 6e20 7468 6520  n still run the 
+00000bf0: 6170 706c 6963 6174 696f 6e20 7769 7468  application with
+00000c00: 6f75 7420 7375 646f 2070 7269 7669 6c65  out sudo privile
+00000c10: 6765 7320 6275 7420 736f 6d65 206d 6574  ges but some met
+00000c20: 7269 6373 2077 696c 6c20 6e6f 7420 6265  rics will not be
+00000c30: 2061 7661 696c 6162 6c65 2e0a 0a23 2320   available...## 
+00000c40: 4375 7272 656e 746c 7920 7375 7070 6f72  Currently suppor
+00000c50: 7465 6420 6665 6174 7572 6573 3a0a 416c  ted features:.Al
+00000c60: 6c20 6d65 7472 6963 7320 6e61 6d65 7320  l metrics names 
+00000c70: 6172 6520 636f 6d70 6c69 6174 2077 6974  are compliat wit
+00000c80: 6820 7072 6f6d 6574 6865 7573 2073 7065  h prometheus spe
+00000c90: 6369 6669 6361 7469 6f6e 7320 6173 2064  cifications as d
+00000ca0: 6573 6372 6962 6564 2069 6e20 5b68 7474  escribed in [htt
+00000cb0: 7073 3a2f 2f70 726f 6d65 7468 6575 732e  ps://prometheus.
+00000cc0: 696f 2f64 6f63 732f 7072 6163 7469 6365  io/docs/practice
+00000cd0: 732f 6e61 6d69 6e67 2f5d 2e0a 0a23 2323  s/naming/]...###
+00000ce0: 2045 6e65 7267 7920 6d65 7472 6963 733a   Energy metrics:
+00000cf0: 0a2d 2065 6e65 7267 6f6e 5f64 6576 6963  .- energon_devic
+00000d00: 655f 696e 666f 3a20 6465 7669 6365 2069  e_info: device i
+00000d10: 6e66 6f72 6d61 7469 6f6e 3b0a 2d20 656e  nformation;.- en
+00000d20: 6572 676f 6e5f 746f 7461 6c5f 696e 5f70  ergon_total_in_p
+00000d30: 6f77 6572 5f6d 573a 2063 7572 7265 6e74  ower_mW: current
+00000d40: 2074 6f74 616c 2070 6f77 6572 2063 6f6e   total power con
+00000d50: 7375 6d70 7469 6f6e 2069 6e20 6d69 6c6c  sumption in mill
+00000d60: 6977 6174 7473 3b0a 2d20 656e 6572 676f  iwatts;.- energo
+00000d70: 6e5f 6370 755f 696e 5f70 6f77 6572 5f6d  n_cpu_in_power_m
+00000d80: 573a 2063 7572 7265 6e74 2063 7075 2070  W: current cpu p
+00000d90: 6f77 6572 2063 6f6e 7375 6d70 7469 6f6e  ower consumption
+00000da0: 2069 6e20 6d69 6c6c 6977 6174 7473 3b0a   in milliwatts;.
+00000db0: 2d20 656e 6572 676f 6e5f 6770 755f 696e  - energon_gpu_in
+00000dc0: 5f70 6f77 6572 5f6d 573a 2063 7572 7265  _power_mW: curre
+00000dd0: 6e74 2067 7075 2070 6f77 6572 2063 6f6e  nt gpu power con
+00000de0: 7375 6d70 7469 6f6e 2069 6e20 6d69 6c6c  sumption in mill
+00000df0: 6977 6174 7473 3b0a 2d20 656e 6572 676f  iwatts;.- energo
+00000e00: 6e5f 746f 7461 6c5f 696e 5f76 6f6c 7461  n_total_in_volta
+00000e10: 6765 5f6d 563a 2063 7572 7265 6e74 2074  ge_mV: current t
+00000e20: 6f74 616c 2076 6f6c 7461 6765 2069 6e20  otal voltage in 
+00000e30: 6d69 6c6c 6976 6f6c 7473 3b0a 2d20 656e  millivolts;.- en
+00000e40: 6572 676f 6e5f 6370 755f 696e 5f76 6f6c  ergon_cpu_in_vol
+00000e50: 7461 6765 5f6d 563a 2063 7572 7265 6e74  tage_mV: current
+00000e60: 2063 7075 2076 6f6c 7461 6765 2069 6e20   cpu voltage in 
+00000e70: 6d69 6c6c 6976 6f6c 7473 3b0a 2d20 656e  millivolts;.- en
+00000e80: 6572 676f 6e5f 6770 755f 696e 5f76 6f6c  ergon_gpu_in_vol
+00000e90: 7461 6765 5f6d 563a 2063 7572 7265 6e74  tage_mV: current
+00000ea0: 2067 7075 2076 6f6c 7461 6765 2069 6e20   gpu voltage in 
+00000eb0: 6d69 6c6c 6976 6f6c 7473 3b0a 2d20 656e  millivolts;.- en
+00000ec0: 6572 676f 6e5f 6261 7474 6572 795f 7065  ergon_battery_pe
+00000ed0: 7263 656e 7461 6765 3a20 6375 7272 656e  rcentage: curren
+00000ee0: 7420 6261 7474 6572 7920 7065 7263 656e  t battery percen
+00000ef0: 7461 6765 2e0a 0a23 2323 2055 5342 2054  tage...### USB T
+00000f00: 6573 7465 7220 554d 3235 4320 5553 4220  ester UM25C USB 
+00000f10: 4d65 7465 7220 5465 7374 6572 206d 6574  Meter Tester met
+00000f20: 7269 6373 3a0a 4e2e 422e 204f 6e6c 7920  rics:.N.B. Only 
+00000f30: 6966 2072 6561 6c20 7365 6e73 6f72 2069  if real sensor i
+00000f40: 7320 636f 6e6e 6563 7465 6421 0a2d 2065  s connected!.- e
+00000f50: 6e65 7267 6f6e 5f74 6f74 616c 5f61 6374  nergon_total_act
+00000f60: 7561 6c5f 7761 7474 733a 2074 6f74 616c  ual_watts: total
+00000f70: 2061 6374 7561 6c20 706f 7765 7220 636f   actual power co
+00000f80: 6e73 756d 7074 696f 6e20 696e 2077 6174  nsumption in wat
+00000f90: 7473 3b0a 2d20 656e 6572 676f 6e5f 746f  ts;.- energon_to
+00000fa0: 7461 6c5f 6163 7475 616c 5f76 6f6c 7473  tal_actual_volts
+00000fb0: 3a20 746f 7461 6c20 6163 7475 616c 2076  : total actual v
+00000fc0: 6f6c 7461 6765 2069 6e20 766f 6c74 733b  oltage in volts;
+00000fd0: 0a2d 2065 6e65 7267 6f6e 5f74 6f74 616c  .- energon_total
+00000fe0: 5f61 6374 7561 6c5f 616d 7073 3a20 746f  _actual_amps: to
+00000ff0: 7461 6c20 6163 7475 616c 2063 7572 7265  tal actual curre
+00001000: 6e74 2069 6e20 616d 7073 2e0a 0a23 2323  nt in amps...###
+00001010: 204e 6574 776f 726b 206d 6574 7269 6373   Network metrics
+00001020: 3a0a 466f 7220 6561 6368 2069 6e74 6572  :.For each inter
+00001030: 6661 6365 5f6e 616d 650a 2d20 6e65 7477  face_name.- netw
+00001040: 6f72 6b5f 6d65 7472 6963 735f 5b69 6e74  ork_metrics_[int
+00001050: 6572 6661 6365 5f6e 616d 655d 5f72 785f  erface_name]_rx_
+00001060: 7061 636b 6574 733a 2072 6563 6569 7665  packets: receive
+00001070: 6420 7061 636b 6574 733b 0a2d 206e 6574  d packets;.- net
+00001080: 776f 726b 5f6d 6574 7269 6373 5f5b 696e  work_metrics_[in
+00001090: 7465 7266 6163 655f 6e61 6d65 5d5f 7278  terface_name]_rx
+000010a0: 5f62 7974 6573 3a20 7265 6365 6976 6564  _bytes: received
+000010b0: 2062 7974 6573 3b0a 2d20 6e65 7477 6f72   bytes;.- networ
+000010c0: 6b5f 6d65 7472 6963 735f 5b69 6e74 6572  k_metrics_[inter
+000010d0: 6661 6365 5f6e 616d 655d 5f72 785f 6572  face_name]_rx_er
+000010e0: 726f 7273 3a20 7265 6365 6976 6564 2065  rors: received e
+000010f0: 7272 6f72 733b 0a2d 206e 6574 776f 726b  rrors;.- network
+00001100: 5f6d 6574 7269 6373 5f5b 696e 7465 7266  _metrics_[interf
+00001110: 6163 655f 6e61 6d65 5d5f 7278 5f64 726f  ace_name]_rx_dro
+00001120: 7070 6564 3a20 7265 6365 6976 6564 2064  pped: received d
+00001130: 726f 7070 6564 2070 6163 6b65 7473 3b0a  ropped packets;.
+00001140: 2d20 6e65 7477 6f72 6b5f 6d65 7472 6963  - network_metric
+00001150: 735f 5b69 6e74 6572 6661 6365 5f6e 616d  s_[interface_nam
+00001160: 655d 5f74 785f 7061 636b 6574 733a 2074  e]_tx_packets: t
+00001170: 7261 6e73 6d69 7474 6564 2070 6163 6b65  ransmitted packe
+00001180: 7473 3b0a 2d20 6e65 7477 6f72 6b5f 6d65  ts;.- network_me
+00001190: 7472 6963 735f 5b69 6e74 6572 6661 6365  trics_[interface
+000011a0: 5f6e 616d 655d 5f74 785f 6279 7465 733a  _name]_tx_bytes:
+000011b0: 2074 7261 736d 6974 7465 6420 6279 7465   trasmitted byte
+000011c0: 733b 0a2d 206e 6574 776f 726b 5f6d 6574  s;.- network_met
+000011d0: 7269 6373 5f5b 696e 7465 7266 6163 655f  rics_[interface_
+000011e0: 6e61 6d65 5d5f 7478 5f65 7272 6f72 733a  name]_tx_errors:
+000011f0: 2074 7261 6e73 6d69 7474 6564 2065 7272   transmitted err
+00001200: 6f72 733b 0a2d 206e 6574 776f 726b 5f6d  ors;.- network_m
+00001210: 6574 7269 6373 5f5b 696e 7465 7266 6163  etrics_[interfac
+00001220: 655f 6e61 6d65 5d5f 7478 5f64 726f 7070  e_name]_tx_dropp
+00001230: 6564 3a20 7472 616e 736d 6974 7465 6420  ed: transmitted 
+00001240: 6472 6f70 7065 6420 7061 636b 6574 732e  dropped packets.
+00001250: 0a0a 2323 2320 4370 7520 7573 6167 653a  ..### Cpu usage:
+00001260: 0a46 6f72 2065 6163 6820 636f 7265 5f6e  .For each core_n
+00001270: 756d 6265 720a 2d20 656e 6572 676f 6e5f  umber.- energon_
+00001280: 6370 755f 5b63 6f72 655f 6e75 6d62 6572  cpu_[core_number
+00001290: 5d5f 4d48 7a3a 2063 7075 2066 7265 7175  ]_MHz: cpu frequ
+000012a0: 656e 6379 2069 6e20 4d48 7a20 666f 7220  ency in MHz for 
+000012b0: 636f 7265 205b 636f 7265 5f6e 756d 6265  core [core_numbe
+000012c0: 725d 3b0a 2d20 656e 6572 676f 6e5f 6370  r];.- energon_cp
+000012d0: 755f 5b63 6f72 655f 6e75 6d62 6572 5d5f  u_[core_number]_
+000012e0: 7573 6167 655f 7065 7263 656e 7461 6765  usage_percentage
+000012f0: 3a20 4350 5520 7573 6167 6520 6173 2025  : CPU usage as %
+00001300: 2066 6f72 2063 6f72 6520 5b63 6f72 655f   for core [core_
+00001310: 6e75 6d62 6572 5d2e 0a54 6f74 616c 0a2d  number]..Total.-
+00001320: 2065 6e65 7267 6f6e 5f63 7075 5f74 6f74   energon_cpu_tot
+00001330: 616c 5f75 7361 6765 5f70 6572 6365 6e74  al_usage_percent
+00001340: 6167 653a 2074 6f74 616c 2043 5055 2075  age: total CPU u
+00001350: 7361 6765 2061 7320 252e 0a0a 2323 2320  sage as %...### 
+00001360: 5374 6f72 6167 653a 0a46 6f72 2065 6163  Storage:.For eac
+00001370: 6820 6176 6169 6c61 626c 6520 5b73 746f  h available [sto
+00001380: 7261 6765 5f64 6576 6963 655d 0a2d 2065  rage_device].- e
+00001390: 6e65 7267 6f6e 5f73 746f 7261 6765 5f5b  nergon_storage_[
+000013a0: 7374 6f72 6167 655f 6465 7669 6365 5d5f  storage_device]_
+000013b0: 746f 7461 6c5f 6279 7465 733a 2074 6f74  total_bytes: tot
+000013c0: 616c 2062 7974 6573 2066 6f72 2073 746f  al bytes for sto
+000013d0: 7261 6765 205b 7374 6f72 6167 655f 6465  rage [storage_de
+000013e0: 7669 6365 5d3b 0a2d 2065 6e65 7267 6f6e  vice];.- energon
+000013f0: 5f73 746f 7261 6765 5f5b 7374 6f72 6167  _storage_[storag
+00001400: 655f 6465 7669 6365 5d5f 7573 6564 5f62  e_device]_used_b
+00001410: 7974 6573 3a20 7573 6564 2062 7974 6573  ytes: used bytes
+00001420: 2066 6f72 2073 746f 7261 6765 205b 7374   for storage [st
+00001430: 6f72 6167 655f 6465 7669 6365 5d3b 0a2d  orage_device];.-
+00001440: 2065 6e65 7267 6f6e 5f73 746f 7261 6765   energon_storage
+00001450: 5f5b 7374 6f72 6167 655f 6465 7669 6365  _[storage_device
+00001460: 5d5f 6176 6169 6c61 626c 655f 6279 7465  ]_available_byte
+00001470: 733a 2061 7661 696c 6162 6c65 2062 7974  s: available byt
+00001480: 6573 2066 6f72 2073 746f 7261 6765 205b  es for storage [
+00001490: 7374 6f72 6167 655f 6465 7669 6365 5d3b  storage_device];
+000014a0: 0a2d 2065 6e65 7267 6f6e 5f73 746f 7261  .- energon_stora
+000014b0: 6765 5f5b 7374 6f72 6167 655f 6465 7669  ge_[storage_devi
+000014c0: 6365 5d5f 7065 7263 656e 745f 7573 6564  ce]_percent_used
+000014d0: 5f70 6572 6365 6e74 6167 653a 2073 746f  _percentage: sto
+000014e0: 7261 6765 2075 7361 6765 2070 6572 6365  rage usage perce
+000014f0: 6e74 6167 6520 666f 7220 7374 6f72 6167  ntage for storag
+00001500: 6520 5b73 746f 7261 6765 5f64 6576 6963  e [storage_devic
+00001510: 655d 2e0a 546f 7461 6c0a 2d20 656e 6572  e]..Total.- ener
+00001520: 676f 6e5f 7374 6f72 6167 655f 746f 7461  gon_storage_tota
+00001530: 6c5f 6279 7465 733a 2074 6f74 616c 2073  l_bytes: total s
+00001540: 746f 7261 6765 2069 6e20 6279 7465 733b  torage in bytes;
+00001550: 0a2d 2065 6e65 7267 6f6e 5f73 746f 7261  .- energon_stora
+00001560: 6765 5f75 7365 645f 6279 7465 733a 2074  ge_used_bytes: t
+00001570: 6f74 616c 2075 7365 6420 7374 6f72 6167  otal used storag
+00001580: 6520 696e 2062 7974 6573 3b0a 2d20 656e  e in bytes;.- en
+00001590: 6572 676f 6e5f 7374 6f72 6167 655f 6176  ergon_storage_av
+000015a0: 6169 6c61 626c 655f 6279 7465 733a 2074  ailable_bytes: t
+000015b0: 6f74 616c 2061 7661 696c 6162 6c65 2073  otal available s
+000015c0: 746f 7261 6765 2069 6e20 6279 7465 733b  torage in bytes;
+000015d0: 0a2d 2065 6e65 7267 6f6e 5f73 746f 7261  .- energon_stora
+000015e0: 6765 5f70 6572 6365 6e74 5f75 7365 645f  ge_percent_used_
+000015f0: 7065 7263 656e 7461 6765 3a20 5374 6f72  percentage: Stor
+00001600: 6167 6520 7573 6167 6520 7065 7263 656e  age usage percen
+00001610: 7461 6765 2e0a 0a23 2323 2052 616d 2075  tage...### Ram u
+00001620: 7361 6765 3a0a 2d20 656e 6572 676f 6e5f  sage:.- energon_
+00001630: 7261 6d5f 746f 7461 6c5f 6279 7465 733a  ram_total_bytes:
+00001640: 2074 6f74 616c 2072 616d 2069 6e20 6279   total ram in by
+00001650: 7465 733b 0a2d 2065 6e65 7267 6f6e 5f72  tes;.- energon_r
+00001660: 616d 5f75 7365 645f 6279 7465 733a 2074  am_used_bytes: t
+00001670: 6f74 616c 2075 7365 6420 7261 6d20 696e  otal used ram in
+00001680: 2062 7974 6573 3b0a 2d20 656e 6572 676f   bytes;.- energo
+00001690: 6e5f 7261 6d5f 6176 6169 6c61 626c 655f  n_ram_available_
+000016a0: 6279 7465 733a 2074 6f74 616c 2061 7661  bytes: total ava
+000016b0: 696c 6162 6c65 2072 616d 2069 6e20 6279  ilable ram in by
+000016c0: 7465 733b 0a2d 2065 6e65 7267 6f6e 5f72  tes;.- energon_r
+000016d0: 616d 5f75 7365 645f 7065 7263 656e 7461  am_used_percenta
+000016e0: 6765 3a20 7261 6d20 7573 6167 6520 7065  ge: ram usage pe
+000016f0: 7263 656e 7461 6765 2e0a 0a23 2323 2047  rcentage...### G
+00001700: 5055 206d 6574 7269 6373 3a0a 2d20 656e  PU metrics:.- en
+00001710: 6572 676f 6e5f 6770 755f 746f 7461 6c5f  ergon_gpu_total_
+00001720: 7573 6167 655f 7065 7263 656e 7461 6765  usage_percentage
+00001730: 3a20 746f 7461 6c20 4750 5520 7573 6167  : total GPU usag
+00001740: 6520 6173 2025 2e0a 0a23 2323 2054 656d  e as %...### Tem
+00001750: 7065 7261 7475 7265 206d 6574 7269 6373  perature metrics
+00001760: 3a0a 466f 7220 6561 6368 2061 7661 696c  :.For each avail
+00001770: 6162 6c65 205b 7465 6d70 6572 6174 7572  able [temperatur
+00001780: 655f 7365 6e73 6f72 5d0a 2d20 656e 6572  e_sensor].- ener
+00001790: 676f 6e5f 7465 6d70 6572 6174 7572 655f  gon_temperature_
+000017a0: 5b74 656d 7065 7261 7475 7265 5f73 656e  [temperature_sen
+000017b0: 736f 725d 5f6d 433a 2074 656d 7065 7261  sor]_mC: tempera
+000017c0: 7475 7265 2069 6e20 6d69 6c6c 6943 656c  ture in milliCel
+000017d0: 7369 7573 2066 6f72 2073 656e 736f 7220  sius for sensor 
+000017e0: 5b74 656d 7065 7261 7475 7265 5f73 656e  [temperature_sen
+000017f0: 736f 725d 2e0a 0a0a 0a                   sor].....
```

### Comparing `energon_prometheus_exporter-0.0.1/README.md` & `energon_prometheus_exporter-0.0.2/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -115,215 +115,224 @@
 00000720: 6020 666f 7220 7275 6e6e 696e 6720 6120  ` for running a 
 00000730: 7369 6e67 6c65 206d 6574 7269 6320 7363  single metric sc
 00000740: 616e 3b0a 2d20 5275 6e3a 2060 6060 2073  an;.- Run: ``` s
 00000750: 7564 6f20 7079 7468 6f6e 3320 7072 6f6d  udo python3 prom
 00000760: 6574 6865 7573 5f65 7870 6f72 7465 722e  etheus_exporter.
 00000770: 7079 2060 6060 2066 6f72 2072 756e 6e69  py ``` for runni
 00000780: 6e67 2074 6865 2070 726f 6d65 7468 6575  ng the prometheu
-00000790: 7320 6578 706f 7274 6572 3b0a 0a23 2323  s exporter;..###
-000007a0: 2320 5769 7468 2070 6970 2069 6e73 7461  # With pip insta
-000007b0: 6c6c 0a2d 2060 6060 2070 6970 3320 696e  ll.- ``` pip3 in
-000007c0: 7374 616c 6c20 456e 6572 676f 6e2d 5072  stall Energon-Pr
-000007d0: 6f6d 6574 6865 7573 2d65 7870 6f72 7465  ometheus-exporte
-000007e0: 7220 6060 603b 0a2d 2060 6060 2066 726f  r ```;.- ``` fro
-000007f0: 6d20 456e 6572 676f 6e5f 5072 6f6d 6574  m Energon_Promet
-00000800: 6865 7573 5f65 7870 6f72 7465 7220 696d  heus_exporter im
-00000810: 706f 7274 2063 6f6e 7374 616e 7473 6060  port constants``
-00000820: 600a 0a54 6865 2061 7070 6c69 6361 7469  `..The applicati
-00000830: 6f6e 2072 6571 7569 7265 7320 7375 646f  on requires sudo
-00000840: 2070 7269 7669 6c65 6765 7320 746f 2061   privileges to a
-00000850: 6363 6573 7320 746f 2073 6f6d 6520 7379  ccess to some sy
-00000860: 7374 656d 2066 696c 6573 2e0a 596f 7520  stem files..You 
-00000870: 6361 6e20 7374 696c 6c20 7275 6e20 7468  can still run th
-00000880: 6520 6170 706c 6963 6174 696f 6e20 7769  e application wi
-00000890: 7468 6f75 7420 7375 646f 2070 7269 7669  thout sudo privi
-000008a0: 6c65 6765 7320 6275 7420 736f 6d65 206d  leges but some m
-000008b0: 6574 7269 6373 2077 696c 6c20 6e6f 7420  etrics will not 
-000008c0: 6265 2061 7661 696c 6162 6c65 2e0a 0a23  be available...#
-000008d0: 2320 4375 7272 656e 746c 7920 7375 7070  # Currently supp
-000008e0: 6f72 7465 6420 6665 6174 7572 6573 3a0a  orted features:.
-000008f0: 416c 6c20 6d65 7472 6963 7320 6e61 6d65  All metrics name
-00000900: 7320 6172 6520 636f 6d70 6c69 6174 2077  s are compliat w
-00000910: 6974 6820 7072 6f6d 6574 6865 7573 2073  ith prometheus s
-00000920: 7065 6369 6669 6361 7469 6f6e 7320 6173  pecifications as
-00000930: 2064 6573 6372 6962 6564 2069 6e20 5b68   described in [h
-00000940: 7474 7073 3a2f 2f70 726f 6d65 7468 6575  ttps://prometheu
-00000950: 732e 696f 2f64 6f63 732f 7072 6163 7469  s.io/docs/practi
-00000960: 6365 732f 6e61 6d69 6e67 2f5d 2e0a 0a23  ces/naming/]...#
-00000970: 2323 2045 6e65 7267 7920 6d65 7472 6963  ## Energy metric
-00000980: 733a 0a2d 2065 6e65 7267 6f6e 5f64 6576  s:.- energon_dev
-00000990: 6963 655f 696e 666f 3a20 6465 7669 6365  ice_info: device
-000009a0: 2069 6e66 6f72 6d61 7469 6f6e 3b0a 2d20   information;.- 
-000009b0: 656e 6572 676f 6e5f 746f 7461 6c5f 696e  energon_total_in
-000009c0: 5f70 6f77 6572 5f6d 573a 2063 7572 7265  _power_mW: curre
-000009d0: 6e74 2074 6f74 616c 2070 6f77 6572 2063  nt total power c
-000009e0: 6f6e 7375 6d70 7469 6f6e 2069 6e20 6d69  onsumption in mi
-000009f0: 6c6c 6977 6174 7473 3b0a 2d20 656e 6572  lliwatts;.- ener
-00000a00: 676f 6e5f 6370 755f 696e 5f70 6f77 6572  gon_cpu_in_power
-00000a10: 5f6d 573a 2063 7572 7265 6e74 2063 7075  _mW: current cpu
-00000a20: 2070 6f77 6572 2063 6f6e 7375 6d70 7469   power consumpti
-00000a30: 6f6e 2069 6e20 6d69 6c6c 6977 6174 7473  on in milliwatts
-00000a40: 3b0a 2d20 656e 6572 676f 6e5f 6770 755f  ;.- energon_gpu_
-00000a50: 696e 5f70 6f77 6572 5f6d 573a 2063 7572  in_power_mW: cur
-00000a60: 7265 6e74 2067 7075 2070 6f77 6572 2063  rent gpu power c
-00000a70: 6f6e 7375 6d70 7469 6f6e 2069 6e20 6d69  onsumption in mi
-00000a80: 6c6c 6977 6174 7473 3b0a 2d20 656e 6572  lliwatts;.- ener
-00000a90: 676f 6e5f 746f 7461 6c5f 696e 5f76 6f6c  gon_total_in_vol
-00000aa0: 7461 6765 5f6d 563a 2063 7572 7265 6e74  tage_mV: current
-00000ab0: 2074 6f74 616c 2076 6f6c 7461 6765 2069   total voltage i
-00000ac0: 6e20 6d69 6c6c 6976 6f6c 7473 3b0a 2d20  n millivolts;.- 
-00000ad0: 656e 6572 676f 6e5f 6370 755f 696e 5f76  energon_cpu_in_v
-00000ae0: 6f6c 7461 6765 5f6d 563a 2063 7572 7265  oltage_mV: curre
-00000af0: 6e74 2063 7075 2076 6f6c 7461 6765 2069  nt cpu voltage i
-00000b00: 6e20 6d69 6c6c 6976 6f6c 7473 3b0a 2d20  n millivolts;.- 
-00000b10: 656e 6572 676f 6e5f 6770 755f 696e 5f76  energon_gpu_in_v
-00000b20: 6f6c 7461 6765 5f6d 563a 2063 7572 7265  oltage_mV: curre
-00000b30: 6e74 2067 7075 2076 6f6c 7461 6765 2069  nt gpu voltage i
-00000b40: 6e20 6d69 6c6c 6976 6f6c 7473 3b0a 2d20  n millivolts;.- 
-00000b50: 656e 6572 676f 6e5f 6261 7474 6572 795f  energon_battery_
-00000b60: 7065 7263 656e 7461 6765 3a20 6375 7272  percentage: curr
-00000b70: 656e 7420 6261 7474 6572 7920 7065 7263  ent battery perc
-00000b80: 656e 7461 6765 2e0a 0a23 2323 2055 5342  entage...### USB
-00000b90: 2054 6573 7465 7220 554d 3235 4320 5553   Tester UM25C US
-00000ba0: 4220 4d65 7465 7220 5465 7374 6572 206d  B Meter Tester m
-00000bb0: 6574 7269 6373 3a0a 4e2e 422e 204f 6e6c  etrics:.N.B. Onl
-00000bc0: 7920 6966 2072 6561 6c20 7365 6e73 6f72  y if real sensor
-00000bd0: 2069 7320 636f 6e6e 6563 7465 6421 0a2d   is connected!.-
-00000be0: 2065 6e65 7267 6f6e 5f74 6f74 616c 5f61   energon_total_a
-00000bf0: 6374 7561 6c5f 7761 7474 733a 2074 6f74  ctual_watts: tot
-00000c00: 616c 2061 6374 7561 6c20 706f 7765 7220  al actual power 
-00000c10: 636f 6e73 756d 7074 696f 6e20 696e 2077  consumption in w
-00000c20: 6174 7473 3b0a 2d20 656e 6572 676f 6e5f  atts;.- energon_
-00000c30: 746f 7461 6c5f 6163 7475 616c 5f76 6f6c  total_actual_vol
-00000c40: 7473 3a20 746f 7461 6c20 6163 7475 616c  ts: total actual
-00000c50: 2076 6f6c 7461 6765 2069 6e20 766f 6c74   voltage in volt
-00000c60: 733b 0a2d 2065 6e65 7267 6f6e 5f74 6f74  s;.- energon_tot
-00000c70: 616c 5f61 6374 7561 6c5f 616d 7073 3a20  al_actual_amps: 
-00000c80: 746f 7461 6c20 6163 7475 616c 2063 7572  total actual cur
-00000c90: 7265 6e74 2069 6e20 616d 7073 2e0a 0a23  rent in amps...#
-00000ca0: 2323 204e 6574 776f 726b 206d 6574 7269  ## Network metri
-00000cb0: 6373 3a0a 466f 7220 6561 6368 2069 6e74  cs:.For each int
-00000cc0: 6572 6661 6365 5f6e 616d 650a 2d20 6e65  erface_name.- ne
-00000cd0: 7477 6f72 6b5f 6d65 7472 6963 735f 5b69  twork_metrics_[i
-00000ce0: 6e74 6572 6661 6365 5f6e 616d 655d 5f72  nterface_name]_r
-00000cf0: 785f 7061 636b 6574 733a 2072 6563 6569  x_packets: recei
-00000d00: 7665 6420 7061 636b 6574 733b 0a2d 206e  ved packets;.- n
-00000d10: 6574 776f 726b 5f6d 6574 7269 6373 5f5b  etwork_metrics_[
-00000d20: 696e 7465 7266 6163 655f 6e61 6d65 5d5f  interface_name]_
-00000d30: 7278 5f62 7974 6573 3a20 7265 6365 6976  rx_bytes: receiv
-00000d40: 6564 2062 7974 6573 3b0a 2d20 6e65 7477  ed bytes;.- netw
-00000d50: 6f72 6b5f 6d65 7472 6963 735f 5b69 6e74  ork_metrics_[int
-00000d60: 6572 6661 6365 5f6e 616d 655d 5f72 785f  erface_name]_rx_
-00000d70: 6572 726f 7273 3a20 7265 6365 6976 6564  errors: received
-00000d80: 2065 7272 6f72 733b 0a2d 206e 6574 776f   errors;.- netwo
-00000d90: 726b 5f6d 6574 7269 6373 5f5b 696e 7465  rk_metrics_[inte
-00000da0: 7266 6163 655f 6e61 6d65 5d5f 7278 5f64  rface_name]_rx_d
-00000db0: 726f 7070 6564 3a20 7265 6365 6976 6564  ropped: received
-00000dc0: 2064 726f 7070 6564 2070 6163 6b65 7473   dropped packets
-00000dd0: 3b0a 2d20 6e65 7477 6f72 6b5f 6d65 7472  ;.- network_metr
-00000de0: 6963 735f 5b69 6e74 6572 6661 6365 5f6e  ics_[interface_n
-00000df0: 616d 655d 5f74 785f 7061 636b 6574 733a  ame]_tx_packets:
-00000e00: 2074 7261 6e73 6d69 7474 6564 2070 6163   transmitted pac
-00000e10: 6b65 7473 3b0a 2d20 6e65 7477 6f72 6b5f  kets;.- network_
-00000e20: 6d65 7472 6963 735f 5b69 6e74 6572 6661  metrics_[interfa
-00000e30: 6365 5f6e 616d 655d 5f74 785f 6279 7465  ce_name]_tx_byte
-00000e40: 733a 2074 7261 736d 6974 7465 6420 6279  s: trasmitted by
-00000e50: 7465 733b 0a2d 206e 6574 776f 726b 5f6d  tes;.- network_m
-00000e60: 6574 7269 6373 5f5b 696e 7465 7266 6163  etrics_[interfac
-00000e70: 655f 6e61 6d65 5d5f 7478 5f65 7272 6f72  e_name]_tx_error
-00000e80: 733a 2074 7261 6e73 6d69 7474 6564 2065  s: transmitted e
-00000e90: 7272 6f72 733b 0a2d 206e 6574 776f 726b  rrors;.- network
-00000ea0: 5f6d 6574 7269 6373 5f5b 696e 7465 7266  _metrics_[interf
-00000eb0: 6163 655f 6e61 6d65 5d5f 7478 5f64 726f  ace_name]_tx_dro
-00000ec0: 7070 6564 3a20 7472 616e 736d 6974 7465  pped: transmitte
-00000ed0: 6420 6472 6f70 7065 6420 7061 636b 6574  d dropped packet
-00000ee0: 732e 0a0a 2323 2320 4370 7520 7573 6167  s...### Cpu usag
-00000ef0: 653a 0a46 6f72 2065 6163 6820 636f 7265  e:.For each core
-00000f00: 5f6e 756d 6265 720a 2d20 656e 6572 676f  _number.- energo
-00000f10: 6e5f 6370 755f 5b63 6f72 655f 6e75 6d62  n_cpu_[core_numb
-00000f20: 6572 5d5f 4d48 7a3a 2063 7075 2066 7265  er]_MHz: cpu fre
-00000f30: 7175 656e 6379 2069 6e20 4d48 7a20 666f  quency in MHz fo
-00000f40: 7220 636f 7265 205b 636f 7265 5f6e 756d  r core [core_num
-00000f50: 6265 725d 3b0a 2d20 656e 6572 676f 6e5f  ber];.- energon_
-00000f60: 6370 755f 5b63 6f72 655f 6e75 6d62 6572  cpu_[core_number
-00000f70: 5d5f 7573 6167 655f 7065 7263 656e 7461  ]_usage_percenta
-00000f80: 6765 3a20 4350 5520 7573 6167 6520 6173  ge: CPU usage as
-00000f90: 2025 2066 6f72 2063 6f72 6520 5b63 6f72   % for core [cor
-00000fa0: 655f 6e75 6d62 6572 5d2e 0a54 6f74 616c  e_number]..Total
-00000fb0: 0a2d 2065 6e65 7267 6f6e 5f63 7075 5f74  .- energon_cpu_t
-00000fc0: 6f74 616c 5f75 7361 6765 5f70 6572 6365  otal_usage_perce
-00000fd0: 6e74 6167 653a 2074 6f74 616c 2043 5055  ntage: total CPU
-00000fe0: 2075 7361 6765 2061 7320 252e 0a0a 2323   usage as %...##
-00000ff0: 2320 5374 6f72 6167 653a 0a46 6f72 2065  # Storage:.For e
-00001000: 6163 6820 6176 6169 6c61 626c 6520 5b73  ach available [s
-00001010: 746f 7261 6765 5f64 6576 6963 655d 0a2d  torage_device].-
-00001020: 2065 6e65 7267 6f6e 5f73 746f 7261 6765   energon_storage
-00001030: 5f5b 7374 6f72 6167 655f 6465 7669 6365  _[storage_device
-00001040: 5d5f 746f 7461 6c5f 6279 7465 733a 2074  ]_total_bytes: t
-00001050: 6f74 616c 2062 7974 6573 2066 6f72 2073  otal bytes for s
-00001060: 746f 7261 6765 205b 7374 6f72 6167 655f  torage [storage_
-00001070: 6465 7669 6365 5d3b 0a2d 2065 6e65 7267  device];.- energ
-00001080: 6f6e 5f73 746f 7261 6765 5f5b 7374 6f72  on_storage_[stor
-00001090: 6167 655f 6465 7669 6365 5d5f 7573 6564  age_device]_used
-000010a0: 5f62 7974 6573 3a20 7573 6564 2062 7974  _bytes: used byt
-000010b0: 6573 2066 6f72 2073 746f 7261 6765 205b  es for storage [
-000010c0: 7374 6f72 6167 655f 6465 7669 6365 5d3b  storage_device];
-000010d0: 0a2d 2065 6e65 7267 6f6e 5f73 746f 7261  .- energon_stora
-000010e0: 6765 5f5b 7374 6f72 6167 655f 6465 7669  ge_[storage_devi
-000010f0: 6365 5d5f 6176 6169 6c61 626c 655f 6279  ce]_available_by
-00001100: 7465 733a 2061 7661 696c 6162 6c65 2062  tes: available b
-00001110: 7974 6573 2066 6f72 2073 746f 7261 6765  ytes for storage
-00001120: 205b 7374 6f72 6167 655f 6465 7669 6365   [storage_device
-00001130: 5d3b 0a2d 2065 6e65 7267 6f6e 5f73 746f  ];.- energon_sto
-00001140: 7261 6765 5f5b 7374 6f72 6167 655f 6465  rage_[storage_de
-00001150: 7669 6365 5d5f 7065 7263 656e 745f 7573  vice]_percent_us
-00001160: 6564 5f70 6572 6365 6e74 6167 653a 2073  ed_percentage: s
-00001170: 746f 7261 6765 2075 7361 6765 2070 6572  torage usage per
-00001180: 6365 6e74 6167 6520 666f 7220 7374 6f72  centage for stor
-00001190: 6167 6520 5b73 746f 7261 6765 5f64 6576  age [storage_dev
-000011a0: 6963 655d 2e0a 546f 7461 6c0a 2d20 656e  ice]..Total.- en
-000011b0: 6572 676f 6e5f 7374 6f72 6167 655f 746f  ergon_storage_to
-000011c0: 7461 6c5f 6279 7465 733a 2074 6f74 616c  tal_bytes: total
-000011d0: 2073 746f 7261 6765 2069 6e20 6279 7465   storage in byte
-000011e0: 733b 0a2d 2065 6e65 7267 6f6e 5f73 746f  s;.- energon_sto
-000011f0: 7261 6765 5f75 7365 645f 6279 7465 733a  rage_used_bytes:
-00001200: 2074 6f74 616c 2075 7365 6420 7374 6f72   total used stor
-00001210: 6167 6520 696e 2062 7974 6573 3b0a 2d20  age in bytes;.- 
-00001220: 656e 6572 676f 6e5f 7374 6f72 6167 655f  energon_storage_
-00001230: 6176 6169 6c61 626c 655f 6279 7465 733a  available_bytes:
-00001240: 2074 6f74 616c 2061 7661 696c 6162 6c65   total available
-00001250: 2073 746f 7261 6765 2069 6e20 6279 7465   storage in byte
-00001260: 733b 0a2d 2065 6e65 7267 6f6e 5f73 746f  s;.- energon_sto
-00001270: 7261 6765 5f70 6572 6365 6e74 5f75 7365  rage_percent_use
-00001280: 645f 7065 7263 656e 7461 6765 3a20 5374  d_percentage: St
-00001290: 6f72 6167 6520 7573 6167 6520 7065 7263  orage usage perc
-000012a0: 656e 7461 6765 2e0a 0a23 2323 2052 616d  entage...### Ram
-000012b0: 2075 7361 6765 3a0a 2d20 656e 6572 676f   usage:.- energo
-000012c0: 6e5f 7261 6d5f 746f 7461 6c5f 6279 7465  n_ram_total_byte
-000012d0: 733a 2074 6f74 616c 2072 616d 2069 6e20  s: total ram in 
-000012e0: 6279 7465 733b 0a2d 2065 6e65 7267 6f6e  bytes;.- energon
-000012f0: 5f72 616d 5f75 7365 645f 6279 7465 733a  _ram_used_bytes:
-00001300: 2074 6f74 616c 2075 7365 6420 7261 6d20   total used ram 
-00001310: 696e 2062 7974 6573 3b0a 2d20 656e 6572  in bytes;.- ener
-00001320: 676f 6e5f 7261 6d5f 6176 6169 6c61 626c  gon_ram_availabl
-00001330: 655f 6279 7465 733a 2074 6f74 616c 2061  e_bytes: total a
-00001340: 7661 696c 6162 6c65 2072 616d 2069 6e20  vailable ram in 
-00001350: 6279 7465 733b 0a2d 2065 6e65 7267 6f6e  bytes;.- energon
-00001360: 5f72 616d 5f75 7365 645f 7065 7263 656e  _ram_used_percen
-00001370: 7461 6765 3a20 7261 6d20 7573 6167 6520  tage: ram usage 
-00001380: 7065 7263 656e 7461 6765 2e0a 0a23 2323  percentage...###
-00001390: 2047 5055 206d 6574 7269 6373 3a0a 2d20   GPU metrics:.- 
-000013a0: 656e 6572 676f 6e5f 6770 755f 746f 7461  energon_gpu_tota
-000013b0: 6c5f 7573 6167 655f 7065 7263 656e 7461  l_usage_percenta
-000013c0: 6765 3a20 746f 7461 6c20 4750 5520 7573  ge: total GPU us
-000013d0: 6167 6520 6173 2025 2e0a 0a23 2323 2054  age as %...### T
-000013e0: 656d 7065 7261 7475 7265 206d 6574 7269  emperature metri
-000013f0: 6373 3a0a 466f 7220 6561 6368 2061 7661  cs:.For each ava
-00001400: 696c 6162 6c65 205b 7465 6d70 6572 6174  ilable [temperat
-00001410: 7572 655f 7365 6e73 6f72 5d0a 2d20 656e  ure_sensor].- en
-00001420: 6572 676f 6e5f 7465 6d70 6572 6174 7572  ergon_temperatur
-00001430: 655f 5b74 656d 7065 7261 7475 7265 5f73  e_[temperature_s
-00001440: 656e 736f 725d 5f6d 433a 2074 656d 7065  ensor]_mC: tempe
-00001450: 7261 7475 7265 2069 6e20 6d69 6c6c 6943  rature in milliC
-00001460: 656c 7369 7573 2066 6f72 2073 656e 736f  elsius for senso
-00001470: 7220 5b74 656d 7065 7261 7475 7265 5f73  r [temperature_s
-00001480: 656e 736f 725d 2e0a 0a0a 0a              ensor].....
+00000790: 7320 6578 706f 7274 6572 206f 6e20 6465  s exporter on de
+000007a0: 6661 756c 7420 706f 7274 2039 3837 373b  fault port 9877;
+000007b0: 0a0a 2323 2323 2057 6974 6820 7069 7020  ..#### With pip 
+000007c0: 696e 7374 616c 6c0a 2d20 6060 6020 7069  install.- ``` pi
+000007d0: 7033 2069 6e73 7461 6c6c 2045 6e65 7267  p3 install Energ
+000007e0: 6f6e 2d50 726f 6d65 7468 6575 732d 6578  on-Prometheus-ex
+000007f0: 706f 7274 6572 2060 6060 3b0a 6060 6020  porter ```;.``` 
+00000800: 0a66 726f 6d20 656e 6572 676f 6e5f 7072  .from energon_pr
+00000810: 6f6d 6574 6865 7573 5f65 7870 6f72 7465  ometheus_exporte
+00000820: 722e 7072 6f6d 6574 6865 7573 5f65 7870  r.prometheus_exp
+00000830: 6f72 7465 7220 696d 706f 7274 2045 6e65  orter import Ene
+00000840: 7267 6f6e 5072 6f6d 6574 6865 7573 4578  rgonPrometheusEx
+00000850: 706f 7274 6572 200a 7365 7276 6572 5f65  porter .server_e
+00000860: 7870 6f72 7465 7220 3d20 456e 6572 676f  xporter = Energo
+00000870: 6e50 726f 6d65 7468 6575 7345 7870 6f72  nPrometheusExpor
+00000880: 7465 7228 4445 5349 5245 445f 504f 5254  ter(DESIRED_PORT
+00000890: 290a 7365 7276 6572 5f65 7870 6f72 7465  ).server_exporte
+000008a0: 722e 7275 6e28 290a 6060 600a 0a54 6865  r.run().```..The
+000008b0: 2061 7070 6c69 6361 7469 6f6e 2072 6571   application req
+000008c0: 7569 7265 7320 7375 646f 2070 7269 7669  uires sudo privi
+000008d0: 6c65 6765 7320 746f 2061 6363 6573 7320  leges to access 
+000008e0: 746f 2073 6f6d 6520 7379 7374 656d 2066  to some system f
+000008f0: 696c 6573 2e0a 596f 7520 6361 6e20 7374  iles..You can st
+00000900: 696c 6c20 7275 6e20 7468 6520 6170 706c  ill run the appl
+00000910: 6963 6174 696f 6e20 7769 7468 6f75 7420  ication without 
+00000920: 7375 646f 2070 7269 7669 6c65 6765 7320  sudo privileges 
+00000930: 6275 7420 736f 6d65 206d 6574 7269 6373  but some metrics
+00000940: 2077 696c 6c20 6e6f 7420 6265 2061 7661   will not be ava
+00000950: 696c 6162 6c65 2e0a 0a23 2320 4375 7272  ilable...## Curr
+00000960: 656e 746c 7920 7375 7070 6f72 7465 6420  ently supported 
+00000970: 6665 6174 7572 6573 3a0a 416c 6c20 6d65  features:.All me
+00000980: 7472 6963 7320 6e61 6d65 7320 6172 6520  trics names are 
+00000990: 636f 6d70 6c69 6174 2077 6974 6820 7072  compliat with pr
+000009a0: 6f6d 6574 6865 7573 2073 7065 6369 6669  ometheus specifi
+000009b0: 6361 7469 6f6e 7320 6173 2064 6573 6372  cations as descr
+000009c0: 6962 6564 2069 6e20 5b68 7474 7073 3a2f  ibed in [https:/
+000009d0: 2f70 726f 6d65 7468 6575 732e 696f 2f64  /prometheus.io/d
+000009e0: 6f63 732f 7072 6163 7469 6365 732f 6e61  ocs/practices/na
+000009f0: 6d69 6e67 2f5d 2e0a 0a23 2323 2045 6e65  ming/]...### Ene
+00000a00: 7267 7920 6d65 7472 6963 733a 0a2d 2065  rgy metrics:.- e
+00000a10: 6e65 7267 6f6e 5f64 6576 6963 655f 696e  nergon_device_in
+00000a20: 666f 3a20 6465 7669 6365 2069 6e66 6f72  fo: device infor
+00000a30: 6d61 7469 6f6e 3b0a 2d20 656e 6572 676f  mation;.- energo
+00000a40: 6e5f 746f 7461 6c5f 696e 5f70 6f77 6572  n_total_in_power
+00000a50: 5f6d 573a 2063 7572 7265 6e74 2074 6f74  _mW: current tot
+00000a60: 616c 2070 6f77 6572 2063 6f6e 7375 6d70  al power consump
+00000a70: 7469 6f6e 2069 6e20 6d69 6c6c 6977 6174  tion in milliwat
+00000a80: 7473 3b0a 2d20 656e 6572 676f 6e5f 6370  ts;.- energon_cp
+00000a90: 755f 696e 5f70 6f77 6572 5f6d 573a 2063  u_in_power_mW: c
+00000aa0: 7572 7265 6e74 2063 7075 2070 6f77 6572  urrent cpu power
+00000ab0: 2063 6f6e 7375 6d70 7469 6f6e 2069 6e20   consumption in 
+00000ac0: 6d69 6c6c 6977 6174 7473 3b0a 2d20 656e  milliwatts;.- en
+00000ad0: 6572 676f 6e5f 6770 755f 696e 5f70 6f77  ergon_gpu_in_pow
+00000ae0: 6572 5f6d 573a 2063 7572 7265 6e74 2067  er_mW: current g
+00000af0: 7075 2070 6f77 6572 2063 6f6e 7375 6d70  pu power consump
+00000b00: 7469 6f6e 2069 6e20 6d69 6c6c 6977 6174  tion in milliwat
+00000b10: 7473 3b0a 2d20 656e 6572 676f 6e5f 746f  ts;.- energon_to
+00000b20: 7461 6c5f 696e 5f76 6f6c 7461 6765 5f6d  tal_in_voltage_m
+00000b30: 563a 2063 7572 7265 6e74 2074 6f74 616c  V: current total
+00000b40: 2076 6f6c 7461 6765 2069 6e20 6d69 6c6c   voltage in mill
+00000b50: 6976 6f6c 7473 3b0a 2d20 656e 6572 676f  ivolts;.- energo
+00000b60: 6e5f 6370 755f 696e 5f76 6f6c 7461 6765  n_cpu_in_voltage
+00000b70: 5f6d 563a 2063 7572 7265 6e74 2063 7075  _mV: current cpu
+00000b80: 2076 6f6c 7461 6765 2069 6e20 6d69 6c6c   voltage in mill
+00000b90: 6976 6f6c 7473 3b0a 2d20 656e 6572 676f  ivolts;.- energo
+00000ba0: 6e5f 6770 755f 696e 5f76 6f6c 7461 6765  n_gpu_in_voltage
+00000bb0: 5f6d 563a 2063 7572 7265 6e74 2067 7075  _mV: current gpu
+00000bc0: 2076 6f6c 7461 6765 2069 6e20 6d69 6c6c   voltage in mill
+00000bd0: 6976 6f6c 7473 3b0a 2d20 656e 6572 676f  ivolts;.- energo
+00000be0: 6e5f 6261 7474 6572 795f 7065 7263 656e  n_battery_percen
+00000bf0: 7461 6765 3a20 6375 7272 656e 7420 6261  tage: current ba
+00000c00: 7474 6572 7920 7065 7263 656e 7461 6765  ttery percentage
+00000c10: 2e0a 0a23 2323 2055 5342 2054 6573 7465  ...### USB Teste
+00000c20: 7220 554d 3235 4320 5553 4220 4d65 7465  r UM25C USB Mete
+00000c30: 7220 5465 7374 6572 206d 6574 7269 6373  r Tester metrics
+00000c40: 3a0a 4e2e 422e 204f 6e6c 7920 6966 2072  :.N.B. Only if r
+00000c50: 6561 6c20 7365 6e73 6f72 2069 7320 636f  eal sensor is co
+00000c60: 6e6e 6563 7465 6421 0a2d 2065 6e65 7267  nnected!.- energ
+00000c70: 6f6e 5f74 6f74 616c 5f61 6374 7561 6c5f  on_total_actual_
+00000c80: 7761 7474 733a 2074 6f74 616c 2061 6374  watts: total act
+00000c90: 7561 6c20 706f 7765 7220 636f 6e73 756d  ual power consum
+00000ca0: 7074 696f 6e20 696e 2077 6174 7473 3b0a  ption in watts;.
+00000cb0: 2d20 656e 6572 676f 6e5f 746f 7461 6c5f  - energon_total_
+00000cc0: 6163 7475 616c 5f76 6f6c 7473 3a20 746f  actual_volts: to
+00000cd0: 7461 6c20 6163 7475 616c 2076 6f6c 7461  tal actual volta
+00000ce0: 6765 2069 6e20 766f 6c74 733b 0a2d 2065  ge in volts;.- e
+00000cf0: 6e65 7267 6f6e 5f74 6f74 616c 5f61 6374  nergon_total_act
+00000d00: 7561 6c5f 616d 7073 3a20 746f 7461 6c20  ual_amps: total 
+00000d10: 6163 7475 616c 2063 7572 7265 6e74 2069  actual current i
+00000d20: 6e20 616d 7073 2e0a 0a23 2323 204e 6574  n amps...### Net
+00000d30: 776f 726b 206d 6574 7269 6373 3a0a 466f  work metrics:.Fo
+00000d40: 7220 6561 6368 2069 6e74 6572 6661 6365  r each interface
+00000d50: 5f6e 616d 650a 2d20 6e65 7477 6f72 6b5f  _name.- network_
+00000d60: 6d65 7472 6963 735f 5b69 6e74 6572 6661  metrics_[interfa
+00000d70: 6365 5f6e 616d 655d 5f72 785f 7061 636b  ce_name]_rx_pack
+00000d80: 6574 733a 2072 6563 6569 7665 6420 7061  ets: received pa
+00000d90: 636b 6574 733b 0a2d 206e 6574 776f 726b  ckets;.- network
+00000da0: 5f6d 6574 7269 6373 5f5b 696e 7465 7266  _metrics_[interf
+00000db0: 6163 655f 6e61 6d65 5d5f 7278 5f62 7974  ace_name]_rx_byt
+00000dc0: 6573 3a20 7265 6365 6976 6564 2062 7974  es: received byt
+00000dd0: 6573 3b0a 2d20 6e65 7477 6f72 6b5f 6d65  es;.- network_me
+00000de0: 7472 6963 735f 5b69 6e74 6572 6661 6365  trics_[interface
+00000df0: 5f6e 616d 655d 5f72 785f 6572 726f 7273  _name]_rx_errors
+00000e00: 3a20 7265 6365 6976 6564 2065 7272 6f72  : received error
+00000e10: 733b 0a2d 206e 6574 776f 726b 5f6d 6574  s;.- network_met
+00000e20: 7269 6373 5f5b 696e 7465 7266 6163 655f  rics_[interface_
+00000e30: 6e61 6d65 5d5f 7278 5f64 726f 7070 6564  name]_rx_dropped
+00000e40: 3a20 7265 6365 6976 6564 2064 726f 7070  : received dropp
+00000e50: 6564 2070 6163 6b65 7473 3b0a 2d20 6e65  ed packets;.- ne
+00000e60: 7477 6f72 6b5f 6d65 7472 6963 735f 5b69  twork_metrics_[i
+00000e70: 6e74 6572 6661 6365 5f6e 616d 655d 5f74  nterface_name]_t
+00000e80: 785f 7061 636b 6574 733a 2074 7261 6e73  x_packets: trans
+00000e90: 6d69 7474 6564 2070 6163 6b65 7473 3b0a  mitted packets;.
+00000ea0: 2d20 6e65 7477 6f72 6b5f 6d65 7472 6963  - network_metric
+00000eb0: 735f 5b69 6e74 6572 6661 6365 5f6e 616d  s_[interface_nam
+00000ec0: 655d 5f74 785f 6279 7465 733a 2074 7261  e]_tx_bytes: tra
+00000ed0: 736d 6974 7465 6420 6279 7465 733b 0a2d  smitted bytes;.-
+00000ee0: 206e 6574 776f 726b 5f6d 6574 7269 6373   network_metrics
+00000ef0: 5f5b 696e 7465 7266 6163 655f 6e61 6d65  _[interface_name
+00000f00: 5d5f 7478 5f65 7272 6f72 733a 2074 7261  ]_tx_errors: tra
+00000f10: 6e73 6d69 7474 6564 2065 7272 6f72 733b  nsmitted errors;
+00000f20: 0a2d 206e 6574 776f 726b 5f6d 6574 7269  .- network_metri
+00000f30: 6373 5f5b 696e 7465 7266 6163 655f 6e61  cs_[interface_na
+00000f40: 6d65 5d5f 7478 5f64 726f 7070 6564 3a20  me]_tx_dropped: 
+00000f50: 7472 616e 736d 6974 7465 6420 6472 6f70  transmitted drop
+00000f60: 7065 6420 7061 636b 6574 732e 0a0a 2323  ped packets...##
+00000f70: 2320 4370 7520 7573 6167 653a 0a46 6f72  # Cpu usage:.For
+00000f80: 2065 6163 6820 636f 7265 5f6e 756d 6265   each core_numbe
+00000f90: 720a 2d20 656e 6572 676f 6e5f 6370 755f  r.- energon_cpu_
+00000fa0: 5b63 6f72 655f 6e75 6d62 6572 5d5f 4d48  [core_number]_MH
+00000fb0: 7a3a 2063 7075 2066 7265 7175 656e 6379  z: cpu frequency
+00000fc0: 2069 6e20 4d48 7a20 666f 7220 636f 7265   in MHz for core
+00000fd0: 205b 636f 7265 5f6e 756d 6265 725d 3b0a   [core_number];.
+00000fe0: 2d20 656e 6572 676f 6e5f 6370 755f 5b63  - energon_cpu_[c
+00000ff0: 6f72 655f 6e75 6d62 6572 5d5f 7573 6167  ore_number]_usag
+00001000: 655f 7065 7263 656e 7461 6765 3a20 4350  e_percentage: CP
+00001010: 5520 7573 6167 6520 6173 2025 2066 6f72  U usage as % for
+00001020: 2063 6f72 6520 5b63 6f72 655f 6e75 6d62   core [core_numb
+00001030: 6572 5d2e 0a54 6f74 616c 0a2d 2065 6e65  er]..Total.- ene
+00001040: 7267 6f6e 5f63 7075 5f74 6f74 616c 5f75  rgon_cpu_total_u
+00001050: 7361 6765 5f70 6572 6365 6e74 6167 653a  sage_percentage:
+00001060: 2074 6f74 616c 2043 5055 2075 7361 6765   total CPU usage
+00001070: 2061 7320 252e 0a0a 2323 2320 5374 6f72   as %...### Stor
+00001080: 6167 653a 0a46 6f72 2065 6163 6820 6176  age:.For each av
+00001090: 6169 6c61 626c 6520 5b73 746f 7261 6765  ailable [storage
+000010a0: 5f64 6576 6963 655d 0a2d 2065 6e65 7267  _device].- energ
+000010b0: 6f6e 5f73 746f 7261 6765 5f5b 7374 6f72  on_storage_[stor
+000010c0: 6167 655f 6465 7669 6365 5d5f 746f 7461  age_device]_tota
+000010d0: 6c5f 6279 7465 733a 2074 6f74 616c 2062  l_bytes: total b
+000010e0: 7974 6573 2066 6f72 2073 746f 7261 6765  ytes for storage
+000010f0: 205b 7374 6f72 6167 655f 6465 7669 6365   [storage_device
+00001100: 5d3b 0a2d 2065 6e65 7267 6f6e 5f73 746f  ];.- energon_sto
+00001110: 7261 6765 5f5b 7374 6f72 6167 655f 6465  rage_[storage_de
+00001120: 7669 6365 5d5f 7573 6564 5f62 7974 6573  vice]_used_bytes
+00001130: 3a20 7573 6564 2062 7974 6573 2066 6f72  : used bytes for
+00001140: 2073 746f 7261 6765 205b 7374 6f72 6167   storage [storag
+00001150: 655f 6465 7669 6365 5d3b 0a2d 2065 6e65  e_device];.- ene
+00001160: 7267 6f6e 5f73 746f 7261 6765 5f5b 7374  rgon_storage_[st
+00001170: 6f72 6167 655f 6465 7669 6365 5d5f 6176  orage_device]_av
+00001180: 6169 6c61 626c 655f 6279 7465 733a 2061  ailable_bytes: a
+00001190: 7661 696c 6162 6c65 2062 7974 6573 2066  vailable bytes f
+000011a0: 6f72 2073 746f 7261 6765 205b 7374 6f72  or storage [stor
+000011b0: 6167 655f 6465 7669 6365 5d3b 0a2d 2065  age_device];.- e
+000011c0: 6e65 7267 6f6e 5f73 746f 7261 6765 5f5b  nergon_storage_[
+000011d0: 7374 6f72 6167 655f 6465 7669 6365 5d5f  storage_device]_
+000011e0: 7065 7263 656e 745f 7573 6564 5f70 6572  percent_used_per
+000011f0: 6365 6e74 6167 653a 2073 746f 7261 6765  centage: storage
+00001200: 2075 7361 6765 2070 6572 6365 6e74 6167   usage percentag
+00001210: 6520 666f 7220 7374 6f72 6167 6520 5b73  e for storage [s
+00001220: 746f 7261 6765 5f64 6576 6963 655d 2e0a  torage_device]..
+00001230: 546f 7461 6c0a 2d20 656e 6572 676f 6e5f  Total.- energon_
+00001240: 7374 6f72 6167 655f 746f 7461 6c5f 6279  storage_total_by
+00001250: 7465 733a 2074 6f74 616c 2073 746f 7261  tes: total stora
+00001260: 6765 2069 6e20 6279 7465 733b 0a2d 2065  ge in bytes;.- e
+00001270: 6e65 7267 6f6e 5f73 746f 7261 6765 5f75  nergon_storage_u
+00001280: 7365 645f 6279 7465 733a 2074 6f74 616c  sed_bytes: total
+00001290: 2075 7365 6420 7374 6f72 6167 6520 696e   used storage in
+000012a0: 2062 7974 6573 3b0a 2d20 656e 6572 676f   bytes;.- energo
+000012b0: 6e5f 7374 6f72 6167 655f 6176 6169 6c61  n_storage_availa
+000012c0: 626c 655f 6279 7465 733a 2074 6f74 616c  ble_bytes: total
+000012d0: 2061 7661 696c 6162 6c65 2073 746f 7261   available stora
+000012e0: 6765 2069 6e20 6279 7465 733b 0a2d 2065  ge in bytes;.- e
+000012f0: 6e65 7267 6f6e 5f73 746f 7261 6765 5f70  nergon_storage_p
+00001300: 6572 6365 6e74 5f75 7365 645f 7065 7263  ercent_used_perc
+00001310: 656e 7461 6765 3a20 5374 6f72 6167 6520  entage: Storage 
+00001320: 7573 6167 6520 7065 7263 656e 7461 6765  usage percentage
+00001330: 2e0a 0a23 2323 2052 616d 2075 7361 6765  ...### Ram usage
+00001340: 3a0a 2d20 656e 6572 676f 6e5f 7261 6d5f  :.- energon_ram_
+00001350: 746f 7461 6c5f 6279 7465 733a 2074 6f74  total_bytes: tot
+00001360: 616c 2072 616d 2069 6e20 6279 7465 733b  al ram in bytes;
+00001370: 0a2d 2065 6e65 7267 6f6e 5f72 616d 5f75  .- energon_ram_u
+00001380: 7365 645f 6279 7465 733a 2074 6f74 616c  sed_bytes: total
+00001390: 2075 7365 6420 7261 6d20 696e 2062 7974   used ram in byt
+000013a0: 6573 3b0a 2d20 656e 6572 676f 6e5f 7261  es;.- energon_ra
+000013b0: 6d5f 6176 6169 6c61 626c 655f 6279 7465  m_available_byte
+000013c0: 733a 2074 6f74 616c 2061 7661 696c 6162  s: total availab
+000013d0: 6c65 2072 616d 2069 6e20 6279 7465 733b  le ram in bytes;
+000013e0: 0a2d 2065 6e65 7267 6f6e 5f72 616d 5f75  .- energon_ram_u
+000013f0: 7365 645f 7065 7263 656e 7461 6765 3a20  sed_percentage: 
+00001400: 7261 6d20 7573 6167 6520 7065 7263 656e  ram usage percen
+00001410: 7461 6765 2e0a 0a23 2323 2047 5055 206d  tage...### GPU m
+00001420: 6574 7269 6373 3a0a 2d20 656e 6572 676f  etrics:.- energo
+00001430: 6e5f 6770 755f 746f 7461 6c5f 7573 6167  n_gpu_total_usag
+00001440: 655f 7065 7263 656e 7461 6765 3a20 746f  e_percentage: to
+00001450: 7461 6c20 4750 5520 7573 6167 6520 6173  tal GPU usage as
+00001460: 2025 2e0a 0a23 2323 2054 656d 7065 7261   %...### Tempera
+00001470: 7475 7265 206d 6574 7269 6373 3a0a 466f  ture metrics:.Fo
+00001480: 7220 6561 6368 2061 7661 696c 6162 6c65  r each available
+00001490: 205b 7465 6d70 6572 6174 7572 655f 7365   [temperature_se
+000014a0: 6e73 6f72 5d0a 2d20 656e 6572 676f 6e5f  nsor].- energon_
+000014b0: 7465 6d70 6572 6174 7572 655f 5b74 656d  temperature_[tem
+000014c0: 7065 7261 7475 7265 5f73 656e 736f 725d  perature_sensor]
+000014d0: 5f6d 433a 2074 656d 7065 7261 7475 7265  _mC: temperature
+000014e0: 2069 6e20 6d69 6c6c 6943 656c 7369 7573   in milliCelsius
+000014f0: 2066 6f72 2073 656e 736f 7220 5b74 656d   for sensor [tem
+00001500: 7065 7261 7475 7265 5f73 656e 736f 725d  perature_sensor]
+00001510: 2e0a 0a0a 0a                             .....
```

### Comparing `energon_prometheus_exporter-0.0.1/pyproject.toml` & `energon_prometheus_exporter-0.0.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "energon_prometheus_exporter"
-version = "0.0.1"
+version = "0.0.2"
 authors = [
   { name="Matteo Mendula", email="mattemendu@gmail.com" },
 ]
 dependencies = [
 	"prometheus_client==0.17.0",
 	"PyBluez==0.30",
 ]
```

### Comparing `energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/drivers/UM25C.py` & `energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/drivers/UM25C.py`

 * *Files identical despite different names*

### Comparing `energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/drivers/driver.py` & `energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/drivers/driver.py`

 * *Files identical despite different names*

### Comparing `energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/drivers/utils.py` & `energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/drivers/utils.py`

 * *Files identical despite different names*

### Comparing `energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/general_model.py` & `energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/general_model.py`

 * *Files 2% similar despite different names*

```diff
@@ -49,30 +49,32 @@
             self.network_metrics[interface_name]["tx_dropped"] = constants.ERROR_WHILE_READING_VALUE if tx_dropped["error"] else utils.parseToFloat(tx_dropped["out_value"])
 
     def set_link_quality(self):
         self.set_network_interfaces()
         self.link_quality = {}
         self.link_quality["_keys"] = []
 
-        for interface_name in self.network_interfaces:
-            if not interface_name.startswith("w"):
+        for _interface_name in self.network_interfaces:
+            if not _interface_name.startswith("w"):
                 continue
+
+            interface_name = utils.clean_metric_name_to_prometheus_format(_interface_name)
             
             link_quality = utils.run_command_and_get_output("iwconfig " + interface_name)
             data = {}
             if not link_quality["error"] and len(link_quality["out_value"]) > 0:
                 self.link_quality["_keys"].append(interface_name)
                 rows = link_quality["out_value"].split("\n")
                 for row in rows:
                     _row = row.strip()
                     if _row.startswith("Link Quality"):
-                        data["link_quality"] = _row.split("=")[1].split(" ")[0] # x/70
-                        data["signal_level"] = _row.split("=")[2].split(" ")[0] # dBm
+                        data["link_quality"] = _row.split("=")[1].split(" ")[0].split("/")[0]   # x/70
+                        data["signal_level"] = _row.split("=")[2].split(" ")[0]                 # dBm
                     if _row.startswith("Bit Rate"):
-                        data["bit_rate"] = _row.split("=")[1].split(" ")[0]     # Mb/s
+                        data["bit_rate"] = _row.split("=")[1].split(" ")[0]                     # Mb/s
 
             self.link_quality[interface_name] = constants.ERROR_WHILE_READING_VALUE if link_quality["error"] else data
 
         return self.link_quality
 
     def set_energy_metrics(self):
         pass
```

### Comparing `energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/jetson_agx_orin.py` & `energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/jetson_agx_orin.py`

 * *Files identical despite different names*

### Comparing `energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/jetson_agx_xavier.py` & `energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/jetson_agx_xavier.py`

 * *Files identical despite different names*

### Comparing `energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/jetson_nano_dev_kit.py` & `energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/jetson_nano_dev_kit.py`

 * *Files identical despite different names*

### Comparing `energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/jetson_xavier_dev_kit.py` & `energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/jetson_xavier_dev_kit.py`

 * *Files identical despite different names*

### Comparing `energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter/models/ubuntu_64.py` & `energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter/models/ubuntu_64.py`

 * *Files identical despite different names*

### Comparing `energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter.egg-info/PKG-INFO` & `energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 00000000: 4d65 7461 6461 7461 2d56 6572 7369 6f6e  Metadata-Version
 00000010: 3a20 322e 310a 4e61 6d65 3a20 656e 6572  : 2.1.Name: ener
 00000020: 676f 6e2d 7072 6f6d 6574 6865 7573 2d65  gon-prometheus-e
 00000030: 7870 6f72 7465 720a 5665 7273 696f 6e3a  xporter.Version:
-00000040: 2030 2e30 2e31 0a53 756d 6d61 7279 3a20   0.0.1.Summary: 
+00000040: 2030 2e30 2e32 0a53 756d 6d61 7279 3a20   0.0.2.Summary: 
 00000050: 456e 6572 676f 6e20 6973 2061 2050 726f  Energon is a Pro
 00000060: 6d65 7468 6575 7320 636f 6d70 6c69 616e  metheus complian
 00000070: 7420 7379 7374 656d 206d 6f6e 6974 6f72  t system monitor
 00000080: 696e 6720 746f 6f6c 732c 2069 7420 666f  ing tools, it fo
 00000090: 6375 7365 7320 6f6e 2074 6865 2065 6e65  cuses on the ene
 000000a0: 7267 7920 636f 6e73 756d 7074 696f 6e20  rgy consumption 
 000000b0: 616e 6420 7265 736f 7572 6365 2075 7361  and resource usa
@@ -161,215 +161,224 @@
 00000a00: 7920 6060 6020 666f 7220 7275 6e6e 696e  y ``` for runnin
 00000a10: 6720 6120 7369 6e67 6c65 206d 6574 7269  g a single metri
 00000a20: 6320 7363 616e 3b0a 2d20 5275 6e3a 2060  c scan;.- Run: `
 00000a30: 6060 2073 7564 6f20 7079 7468 6f6e 3320  `` sudo python3 
 00000a40: 7072 6f6d 6574 6865 7573 5f65 7870 6f72  prometheus_expor
 00000a50: 7465 722e 7079 2060 6060 2066 6f72 2072  ter.py ``` for r
 00000a60: 756e 6e69 6e67 2074 6865 2070 726f 6d65  unning the prome
-00000a70: 7468 6575 7320 6578 706f 7274 6572 3b0a  theus exporter;.
-00000a80: 0a23 2323 2320 5769 7468 2070 6970 2069  .#### With pip i
-00000a90: 6e73 7461 6c6c 0a2d 2060 6060 2070 6970  nstall.- ``` pip
-00000aa0: 3320 696e 7374 616c 6c20 456e 6572 676f  3 install Energo
-00000ab0: 6e2d 5072 6f6d 6574 6865 7573 2d65 7870  n-Prometheus-exp
-00000ac0: 6f72 7465 7220 6060 603b 0a2d 2060 6060  orter ```;.- ```
-00000ad0: 2066 726f 6d20 456e 6572 676f 6e5f 5072   from Energon_Pr
-00000ae0: 6f6d 6574 6865 7573 5f65 7870 6f72 7465  ometheus_exporte
-00000af0: 7220 696d 706f 7274 2063 6f6e 7374 616e  r import constan
-00000b00: 7473 6060 600a 0a54 6865 2061 7070 6c69  ts```..The appli
-00000b10: 6361 7469 6f6e 2072 6571 7569 7265 7320  cation requires 
-00000b20: 7375 646f 2070 7269 7669 6c65 6765 7320  sudo privileges 
-00000b30: 746f 2061 6363 6573 7320 746f 2073 6f6d  to access to som
-00000b40: 6520 7379 7374 656d 2066 696c 6573 2e0a  e system files..
-00000b50: 596f 7520 6361 6e20 7374 696c 6c20 7275  You can still ru
-00000b60: 6e20 7468 6520 6170 706c 6963 6174 696f  n the applicatio
-00000b70: 6e20 7769 7468 6f75 7420 7375 646f 2070  n without sudo p
-00000b80: 7269 7669 6c65 6765 7320 6275 7420 736f  rivileges but so
-00000b90: 6d65 206d 6574 7269 6373 2077 696c 6c20  me metrics will 
-00000ba0: 6e6f 7420 6265 2061 7661 696c 6162 6c65  not be available
-00000bb0: 2e0a 0a23 2320 4375 7272 656e 746c 7920  ...## Currently 
-00000bc0: 7375 7070 6f72 7465 6420 6665 6174 7572  supported featur
-00000bd0: 6573 3a0a 416c 6c20 6d65 7472 6963 7320  es:.All metrics 
-00000be0: 6e61 6d65 7320 6172 6520 636f 6d70 6c69  names are compli
-00000bf0: 6174 2077 6974 6820 7072 6f6d 6574 6865  at with promethe
-00000c00: 7573 2073 7065 6369 6669 6361 7469 6f6e  us specification
-00000c10: 7320 6173 2064 6573 6372 6962 6564 2069  s as described i
-00000c20: 6e20 5b68 7474 7073 3a2f 2f70 726f 6d65  n [https://prome
-00000c30: 7468 6575 732e 696f 2f64 6f63 732f 7072  theus.io/docs/pr
-00000c40: 6163 7469 6365 732f 6e61 6d69 6e67 2f5d  actices/naming/]
-00000c50: 2e0a 0a23 2323 2045 6e65 7267 7920 6d65  ...### Energy me
-00000c60: 7472 6963 733a 0a2d 2065 6e65 7267 6f6e  trics:.- energon
-00000c70: 5f64 6576 6963 655f 696e 666f 3a20 6465  _device_info: de
-00000c80: 7669 6365 2069 6e66 6f72 6d61 7469 6f6e  vice information
-00000c90: 3b0a 2d20 656e 6572 676f 6e5f 746f 7461  ;.- energon_tota
-00000ca0: 6c5f 696e 5f70 6f77 6572 5f6d 573a 2063  l_in_power_mW: c
-00000cb0: 7572 7265 6e74 2074 6f74 616c 2070 6f77  urrent total pow
-00000cc0: 6572 2063 6f6e 7375 6d70 7469 6f6e 2069  er consumption i
-00000cd0: 6e20 6d69 6c6c 6977 6174 7473 3b0a 2d20  n milliwatts;.- 
-00000ce0: 656e 6572 676f 6e5f 6370 755f 696e 5f70  energon_cpu_in_p
-00000cf0: 6f77 6572 5f6d 573a 2063 7572 7265 6e74  ower_mW: current
-00000d00: 2063 7075 2070 6f77 6572 2063 6f6e 7375   cpu power consu
-00000d10: 6d70 7469 6f6e 2069 6e20 6d69 6c6c 6977  mption in milliw
-00000d20: 6174 7473 3b0a 2d20 656e 6572 676f 6e5f  atts;.- energon_
-00000d30: 6770 755f 696e 5f70 6f77 6572 5f6d 573a  gpu_in_power_mW:
-00000d40: 2063 7572 7265 6e74 2067 7075 2070 6f77   current gpu pow
-00000d50: 6572 2063 6f6e 7375 6d70 7469 6f6e 2069  er consumption i
-00000d60: 6e20 6d69 6c6c 6977 6174 7473 3b0a 2d20  n milliwatts;.- 
-00000d70: 656e 6572 676f 6e5f 746f 7461 6c5f 696e  energon_total_in
-00000d80: 5f76 6f6c 7461 6765 5f6d 563a 2063 7572  _voltage_mV: cur
-00000d90: 7265 6e74 2074 6f74 616c 2076 6f6c 7461  rent total volta
-00000da0: 6765 2069 6e20 6d69 6c6c 6976 6f6c 7473  ge in millivolts
-00000db0: 3b0a 2d20 656e 6572 676f 6e5f 6370 755f  ;.- energon_cpu_
-00000dc0: 696e 5f76 6f6c 7461 6765 5f6d 563a 2063  in_voltage_mV: c
-00000dd0: 7572 7265 6e74 2063 7075 2076 6f6c 7461  urrent cpu volta
-00000de0: 6765 2069 6e20 6d69 6c6c 6976 6f6c 7473  ge in millivolts
-00000df0: 3b0a 2d20 656e 6572 676f 6e5f 6770 755f  ;.- energon_gpu_
-00000e00: 696e 5f76 6f6c 7461 6765 5f6d 563a 2063  in_voltage_mV: c
-00000e10: 7572 7265 6e74 2067 7075 2076 6f6c 7461  urrent gpu volta
-00000e20: 6765 2069 6e20 6d69 6c6c 6976 6f6c 7473  ge in millivolts
-00000e30: 3b0a 2d20 656e 6572 676f 6e5f 6261 7474  ;.- energon_batt
-00000e40: 6572 795f 7065 7263 656e 7461 6765 3a20  ery_percentage: 
-00000e50: 6375 7272 656e 7420 6261 7474 6572 7920  current battery 
-00000e60: 7065 7263 656e 7461 6765 2e0a 0a23 2323  percentage...###
-00000e70: 2055 5342 2054 6573 7465 7220 554d 3235   USB Tester UM25
-00000e80: 4320 5553 4220 4d65 7465 7220 5465 7374  C USB Meter Test
-00000e90: 6572 206d 6574 7269 6373 3a0a 4e2e 422e  er metrics:.N.B.
-00000ea0: 204f 6e6c 7920 6966 2072 6561 6c20 7365   Only if real se
-00000eb0: 6e73 6f72 2069 7320 636f 6e6e 6563 7465  nsor is connecte
-00000ec0: 6421 0a2d 2065 6e65 7267 6f6e 5f74 6f74  d!.- energon_tot
-00000ed0: 616c 5f61 6374 7561 6c5f 7761 7474 733a  al_actual_watts:
-00000ee0: 2074 6f74 616c 2061 6374 7561 6c20 706f   total actual po
-00000ef0: 7765 7220 636f 6e73 756d 7074 696f 6e20  wer consumption 
-00000f00: 696e 2077 6174 7473 3b0a 2d20 656e 6572  in watts;.- ener
-00000f10: 676f 6e5f 746f 7461 6c5f 6163 7475 616c  gon_total_actual
-00000f20: 5f76 6f6c 7473 3a20 746f 7461 6c20 6163  _volts: total ac
-00000f30: 7475 616c 2076 6f6c 7461 6765 2069 6e20  tual voltage in 
-00000f40: 766f 6c74 733b 0a2d 2065 6e65 7267 6f6e  volts;.- energon
-00000f50: 5f74 6f74 616c 5f61 6374 7561 6c5f 616d  _total_actual_am
-00000f60: 7073 3a20 746f 7461 6c20 6163 7475 616c  ps: total actual
-00000f70: 2063 7572 7265 6e74 2069 6e20 616d 7073   current in amps
-00000f80: 2e0a 0a23 2323 204e 6574 776f 726b 206d  ...### Network m
-00000f90: 6574 7269 6373 3a0a 466f 7220 6561 6368  etrics:.For each
-00000fa0: 2069 6e74 6572 6661 6365 5f6e 616d 650a   interface_name.
-00000fb0: 2d20 6e65 7477 6f72 6b5f 6d65 7472 6963  - network_metric
-00000fc0: 735f 5b69 6e74 6572 6661 6365 5f6e 616d  s_[interface_nam
-00000fd0: 655d 5f72 785f 7061 636b 6574 733a 2072  e]_rx_packets: r
-00000fe0: 6563 6569 7665 6420 7061 636b 6574 733b  eceived packets;
-00000ff0: 0a2d 206e 6574 776f 726b 5f6d 6574 7269  .- network_metri
-00001000: 6373 5f5b 696e 7465 7266 6163 655f 6e61  cs_[interface_na
-00001010: 6d65 5d5f 7278 5f62 7974 6573 3a20 7265  me]_rx_bytes: re
-00001020: 6365 6976 6564 2062 7974 6573 3b0a 2d20  ceived bytes;.- 
-00001030: 6e65 7477 6f72 6b5f 6d65 7472 6963 735f  network_metrics_
-00001040: 5b69 6e74 6572 6661 6365 5f6e 616d 655d  [interface_name]
-00001050: 5f72 785f 6572 726f 7273 3a20 7265 6365  _rx_errors: rece
-00001060: 6976 6564 2065 7272 6f72 733b 0a2d 206e  ived errors;.- n
-00001070: 6574 776f 726b 5f6d 6574 7269 6373 5f5b  etwork_metrics_[
-00001080: 696e 7465 7266 6163 655f 6e61 6d65 5d5f  interface_name]_
-00001090: 7278 5f64 726f 7070 6564 3a20 7265 6365  rx_dropped: rece
-000010a0: 6976 6564 2064 726f 7070 6564 2070 6163  ived dropped pac
-000010b0: 6b65 7473 3b0a 2d20 6e65 7477 6f72 6b5f  kets;.- network_
-000010c0: 6d65 7472 6963 735f 5b69 6e74 6572 6661  metrics_[interfa
-000010d0: 6365 5f6e 616d 655d 5f74 785f 7061 636b  ce_name]_tx_pack
-000010e0: 6574 733a 2074 7261 6e73 6d69 7474 6564  ets: transmitted
-000010f0: 2070 6163 6b65 7473 3b0a 2d20 6e65 7477   packets;.- netw
-00001100: 6f72 6b5f 6d65 7472 6963 735f 5b69 6e74  ork_metrics_[int
-00001110: 6572 6661 6365 5f6e 616d 655d 5f74 785f  erface_name]_tx_
-00001120: 6279 7465 733a 2074 7261 736d 6974 7465  bytes: trasmitte
-00001130: 6420 6279 7465 733b 0a2d 206e 6574 776f  d bytes;.- netwo
-00001140: 726b 5f6d 6574 7269 6373 5f5b 696e 7465  rk_metrics_[inte
-00001150: 7266 6163 655f 6e61 6d65 5d5f 7478 5f65  rface_name]_tx_e
-00001160: 7272 6f72 733a 2074 7261 6e73 6d69 7474  rrors: transmitt
-00001170: 6564 2065 7272 6f72 733b 0a2d 206e 6574  ed errors;.- net
-00001180: 776f 726b 5f6d 6574 7269 6373 5f5b 696e  work_metrics_[in
-00001190: 7465 7266 6163 655f 6e61 6d65 5d5f 7478  terface_name]_tx
-000011a0: 5f64 726f 7070 6564 3a20 7472 616e 736d  _dropped: transm
-000011b0: 6974 7465 6420 6472 6f70 7065 6420 7061  itted dropped pa
-000011c0: 636b 6574 732e 0a0a 2323 2320 4370 7520  ckets...### Cpu 
-000011d0: 7573 6167 653a 0a46 6f72 2065 6163 6820  usage:.For each 
-000011e0: 636f 7265 5f6e 756d 6265 720a 2d20 656e  core_number.- en
-000011f0: 6572 676f 6e5f 6370 755f 5b63 6f72 655f  ergon_cpu_[core_
-00001200: 6e75 6d62 6572 5d5f 4d48 7a3a 2063 7075  number]_MHz: cpu
-00001210: 2066 7265 7175 656e 6379 2069 6e20 4d48   frequency in MH
-00001220: 7a20 666f 7220 636f 7265 205b 636f 7265  z for core [core
-00001230: 5f6e 756d 6265 725d 3b0a 2d20 656e 6572  _number];.- ener
-00001240: 676f 6e5f 6370 755f 5b63 6f72 655f 6e75  gon_cpu_[core_nu
-00001250: 6d62 6572 5d5f 7573 6167 655f 7065 7263  mber]_usage_perc
-00001260: 656e 7461 6765 3a20 4350 5520 7573 6167  entage: CPU usag
-00001270: 6520 6173 2025 2066 6f72 2063 6f72 6520  e as % for core 
-00001280: 5b63 6f72 655f 6e75 6d62 6572 5d2e 0a54  [core_number]..T
-00001290: 6f74 616c 0a2d 2065 6e65 7267 6f6e 5f63  otal.- energon_c
-000012a0: 7075 5f74 6f74 616c 5f75 7361 6765 5f70  pu_total_usage_p
-000012b0: 6572 6365 6e74 6167 653a 2074 6f74 616c  ercentage: total
-000012c0: 2043 5055 2075 7361 6765 2061 7320 252e   CPU usage as %.
-000012d0: 0a0a 2323 2320 5374 6f72 6167 653a 0a46  ..### Storage:.F
-000012e0: 6f72 2065 6163 6820 6176 6169 6c61 626c  or each availabl
-000012f0: 6520 5b73 746f 7261 6765 5f64 6576 6963  e [storage_devic
-00001300: 655d 0a2d 2065 6e65 7267 6f6e 5f73 746f  e].- energon_sto
-00001310: 7261 6765 5f5b 7374 6f72 6167 655f 6465  rage_[storage_de
-00001320: 7669 6365 5d5f 746f 7461 6c5f 6279 7465  vice]_total_byte
-00001330: 733a 2074 6f74 616c 2062 7974 6573 2066  s: total bytes f
-00001340: 6f72 2073 746f 7261 6765 205b 7374 6f72  or storage [stor
-00001350: 6167 655f 6465 7669 6365 5d3b 0a2d 2065  age_device];.- e
-00001360: 6e65 7267 6f6e 5f73 746f 7261 6765 5f5b  nergon_storage_[
-00001370: 7374 6f72 6167 655f 6465 7669 6365 5d5f  storage_device]_
-00001380: 7573 6564 5f62 7974 6573 3a20 7573 6564  used_bytes: used
-00001390: 2062 7974 6573 2066 6f72 2073 746f 7261   bytes for stora
-000013a0: 6765 205b 7374 6f72 6167 655f 6465 7669  ge [storage_devi
-000013b0: 6365 5d3b 0a2d 2065 6e65 7267 6f6e 5f73  ce];.- energon_s
-000013c0: 746f 7261 6765 5f5b 7374 6f72 6167 655f  torage_[storage_
-000013d0: 6465 7669 6365 5d5f 6176 6169 6c61 626c  device]_availabl
-000013e0: 655f 6279 7465 733a 2061 7661 696c 6162  e_bytes: availab
-000013f0: 6c65 2062 7974 6573 2066 6f72 2073 746f  le bytes for sto
-00001400: 7261 6765 205b 7374 6f72 6167 655f 6465  rage [storage_de
-00001410: 7669 6365 5d3b 0a2d 2065 6e65 7267 6f6e  vice];.- energon
-00001420: 5f73 746f 7261 6765 5f5b 7374 6f72 6167  _storage_[storag
-00001430: 655f 6465 7669 6365 5d5f 7065 7263 656e  e_device]_percen
-00001440: 745f 7573 6564 5f70 6572 6365 6e74 6167  t_used_percentag
-00001450: 653a 2073 746f 7261 6765 2075 7361 6765  e: storage usage
-00001460: 2070 6572 6365 6e74 6167 6520 666f 7220   percentage for 
-00001470: 7374 6f72 6167 6520 5b73 746f 7261 6765  storage [storage
-00001480: 5f64 6576 6963 655d 2e0a 546f 7461 6c0a  _device]..Total.
-00001490: 2d20 656e 6572 676f 6e5f 7374 6f72 6167  - energon_storag
-000014a0: 655f 746f 7461 6c5f 6279 7465 733a 2074  e_total_bytes: t
-000014b0: 6f74 616c 2073 746f 7261 6765 2069 6e20  otal storage in 
-000014c0: 6279 7465 733b 0a2d 2065 6e65 7267 6f6e  bytes;.- energon
-000014d0: 5f73 746f 7261 6765 5f75 7365 645f 6279  _storage_used_by
-000014e0: 7465 733a 2074 6f74 616c 2075 7365 6420  tes: total used 
-000014f0: 7374 6f72 6167 6520 696e 2062 7974 6573  storage in bytes
-00001500: 3b0a 2d20 656e 6572 676f 6e5f 7374 6f72  ;.- energon_stor
-00001510: 6167 655f 6176 6169 6c61 626c 655f 6279  age_available_by
-00001520: 7465 733a 2074 6f74 616c 2061 7661 696c  tes: total avail
-00001530: 6162 6c65 2073 746f 7261 6765 2069 6e20  able storage in 
-00001540: 6279 7465 733b 0a2d 2065 6e65 7267 6f6e  bytes;.- energon
-00001550: 5f73 746f 7261 6765 5f70 6572 6365 6e74  _storage_percent
-00001560: 5f75 7365 645f 7065 7263 656e 7461 6765  _used_percentage
-00001570: 3a20 5374 6f72 6167 6520 7573 6167 6520  : Storage usage 
-00001580: 7065 7263 656e 7461 6765 2e0a 0a23 2323  percentage...###
-00001590: 2052 616d 2075 7361 6765 3a0a 2d20 656e   Ram usage:.- en
-000015a0: 6572 676f 6e5f 7261 6d5f 746f 7461 6c5f  ergon_ram_total_
-000015b0: 6279 7465 733a 2074 6f74 616c 2072 616d  bytes: total ram
-000015c0: 2069 6e20 6279 7465 733b 0a2d 2065 6e65   in bytes;.- ene
-000015d0: 7267 6f6e 5f72 616d 5f75 7365 645f 6279  rgon_ram_used_by
-000015e0: 7465 733a 2074 6f74 616c 2075 7365 6420  tes: total used 
-000015f0: 7261 6d20 696e 2062 7974 6573 3b0a 2d20  ram in bytes;.- 
-00001600: 656e 6572 676f 6e5f 7261 6d5f 6176 6169  energon_ram_avai
-00001610: 6c61 626c 655f 6279 7465 733a 2074 6f74  lable_bytes: tot
-00001620: 616c 2061 7661 696c 6162 6c65 2072 616d  al available ram
-00001630: 2069 6e20 6279 7465 733b 0a2d 2065 6e65   in bytes;.- ene
-00001640: 7267 6f6e 5f72 616d 5f75 7365 645f 7065  rgon_ram_used_pe
-00001650: 7263 656e 7461 6765 3a20 7261 6d20 7573  rcentage: ram us
-00001660: 6167 6520 7065 7263 656e 7461 6765 2e0a  age percentage..
-00001670: 0a23 2323 2047 5055 206d 6574 7269 6373  .### GPU metrics
-00001680: 3a0a 2d20 656e 6572 676f 6e5f 6770 755f  :.- energon_gpu_
-00001690: 746f 7461 6c5f 7573 6167 655f 7065 7263  total_usage_perc
-000016a0: 656e 7461 6765 3a20 746f 7461 6c20 4750  entage: total GP
-000016b0: 5520 7573 6167 6520 6173 2025 2e0a 0a23  U usage as %...#
-000016c0: 2323 2054 656d 7065 7261 7475 7265 206d  ## Temperature m
-000016d0: 6574 7269 6373 3a0a 466f 7220 6561 6368  etrics:.For each
-000016e0: 2061 7661 696c 6162 6c65 205b 7465 6d70   available [temp
-000016f0: 6572 6174 7572 655f 7365 6e73 6f72 5d0a  erature_sensor].
-00001700: 2d20 656e 6572 676f 6e5f 7465 6d70 6572  - energon_temper
-00001710: 6174 7572 655f 5b74 656d 7065 7261 7475  ature_[temperatu
-00001720: 7265 5f73 656e 736f 725d 5f6d 433a 2074  re_sensor]_mC: t
-00001730: 656d 7065 7261 7475 7265 2069 6e20 6d69  emperature in mi
-00001740: 6c6c 6943 656c 7369 7573 2066 6f72 2073  lliCelsius for s
-00001750: 656e 736f 7220 5b74 656d 7065 7261 7475  ensor [temperatu
-00001760: 7265 5f73 656e 736f 725d 2e0a 0a0a 0a    re_sensor].....
+00000a70: 7468 6575 7320 6578 706f 7274 6572 206f  theus exporter o
+00000a80: 6e20 6465 6661 756c 7420 706f 7274 2039  n default port 9
+00000a90: 3837 373b 0a0a 2323 2323 2057 6974 6820  877;..#### With 
+00000aa0: 7069 7020 696e 7374 616c 6c0a 2d20 6060  pip install.- ``
+00000ab0: 6020 7069 7033 2069 6e73 7461 6c6c 2045  ` pip3 install E
+00000ac0: 6e65 7267 6f6e 2d50 726f 6d65 7468 6575  nergon-Prometheu
+00000ad0: 732d 6578 706f 7274 6572 2060 6060 3b0a  s-exporter ```;.
+00000ae0: 6060 6020 0a66 726f 6d20 656e 6572 676f  ``` .from energo
+00000af0: 6e5f 7072 6f6d 6574 6865 7573 5f65 7870  n_prometheus_exp
+00000b00: 6f72 7465 722e 7072 6f6d 6574 6865 7573  orter.prometheus
+00000b10: 5f65 7870 6f72 7465 7220 696d 706f 7274  _exporter import
+00000b20: 2045 6e65 7267 6f6e 5072 6f6d 6574 6865   EnergonPromethe
+00000b30: 7573 4578 706f 7274 6572 200a 7365 7276  usExporter .serv
+00000b40: 6572 5f65 7870 6f72 7465 7220 3d20 456e  er_exporter = En
+00000b50: 6572 676f 6e50 726f 6d65 7468 6575 7345  ergonPrometheusE
+00000b60: 7870 6f72 7465 7228 4445 5349 5245 445f  xporter(DESIRED_
+00000b70: 504f 5254 290a 7365 7276 6572 5f65 7870  PORT).server_exp
+00000b80: 6f72 7465 722e 7275 6e28 290a 6060 600a  orter.run().```.
+00000b90: 0a54 6865 2061 7070 6c69 6361 7469 6f6e  .The application
+00000ba0: 2072 6571 7569 7265 7320 7375 646f 2070   requires sudo p
+00000bb0: 7269 7669 6c65 6765 7320 746f 2061 6363  rivileges to acc
+00000bc0: 6573 7320 746f 2073 6f6d 6520 7379 7374  ess to some syst
+00000bd0: 656d 2066 696c 6573 2e0a 596f 7520 6361  em files..You ca
+00000be0: 6e20 7374 696c 6c20 7275 6e20 7468 6520  n still run the 
+00000bf0: 6170 706c 6963 6174 696f 6e20 7769 7468  application with
+00000c00: 6f75 7420 7375 646f 2070 7269 7669 6c65  out sudo privile
+00000c10: 6765 7320 6275 7420 736f 6d65 206d 6574  ges but some met
+00000c20: 7269 6373 2077 696c 6c20 6e6f 7420 6265  rics will not be
+00000c30: 2061 7661 696c 6162 6c65 2e0a 0a23 2320   available...## 
+00000c40: 4375 7272 656e 746c 7920 7375 7070 6f72  Currently suppor
+00000c50: 7465 6420 6665 6174 7572 6573 3a0a 416c  ted features:.Al
+00000c60: 6c20 6d65 7472 6963 7320 6e61 6d65 7320  l metrics names 
+00000c70: 6172 6520 636f 6d70 6c69 6174 2077 6974  are compliat wit
+00000c80: 6820 7072 6f6d 6574 6865 7573 2073 7065  h prometheus spe
+00000c90: 6369 6669 6361 7469 6f6e 7320 6173 2064  cifications as d
+00000ca0: 6573 6372 6962 6564 2069 6e20 5b68 7474  escribed in [htt
+00000cb0: 7073 3a2f 2f70 726f 6d65 7468 6575 732e  ps://prometheus.
+00000cc0: 696f 2f64 6f63 732f 7072 6163 7469 6365  io/docs/practice
+00000cd0: 732f 6e61 6d69 6e67 2f5d 2e0a 0a23 2323  s/naming/]...###
+00000ce0: 2045 6e65 7267 7920 6d65 7472 6963 733a   Energy metrics:
+00000cf0: 0a2d 2065 6e65 7267 6f6e 5f64 6576 6963  .- energon_devic
+00000d00: 655f 696e 666f 3a20 6465 7669 6365 2069  e_info: device i
+00000d10: 6e66 6f72 6d61 7469 6f6e 3b0a 2d20 656e  nformation;.- en
+00000d20: 6572 676f 6e5f 746f 7461 6c5f 696e 5f70  ergon_total_in_p
+00000d30: 6f77 6572 5f6d 573a 2063 7572 7265 6e74  ower_mW: current
+00000d40: 2074 6f74 616c 2070 6f77 6572 2063 6f6e   total power con
+00000d50: 7375 6d70 7469 6f6e 2069 6e20 6d69 6c6c  sumption in mill
+00000d60: 6977 6174 7473 3b0a 2d20 656e 6572 676f  iwatts;.- energo
+00000d70: 6e5f 6370 755f 696e 5f70 6f77 6572 5f6d  n_cpu_in_power_m
+00000d80: 573a 2063 7572 7265 6e74 2063 7075 2070  W: current cpu p
+00000d90: 6f77 6572 2063 6f6e 7375 6d70 7469 6f6e  ower consumption
+00000da0: 2069 6e20 6d69 6c6c 6977 6174 7473 3b0a   in milliwatts;.
+00000db0: 2d20 656e 6572 676f 6e5f 6770 755f 696e  - energon_gpu_in
+00000dc0: 5f70 6f77 6572 5f6d 573a 2063 7572 7265  _power_mW: curre
+00000dd0: 6e74 2067 7075 2070 6f77 6572 2063 6f6e  nt gpu power con
+00000de0: 7375 6d70 7469 6f6e 2069 6e20 6d69 6c6c  sumption in mill
+00000df0: 6977 6174 7473 3b0a 2d20 656e 6572 676f  iwatts;.- energo
+00000e00: 6e5f 746f 7461 6c5f 696e 5f76 6f6c 7461  n_total_in_volta
+00000e10: 6765 5f6d 563a 2063 7572 7265 6e74 2074  ge_mV: current t
+00000e20: 6f74 616c 2076 6f6c 7461 6765 2069 6e20  otal voltage in 
+00000e30: 6d69 6c6c 6976 6f6c 7473 3b0a 2d20 656e  millivolts;.- en
+00000e40: 6572 676f 6e5f 6370 755f 696e 5f76 6f6c  ergon_cpu_in_vol
+00000e50: 7461 6765 5f6d 563a 2063 7572 7265 6e74  tage_mV: current
+00000e60: 2063 7075 2076 6f6c 7461 6765 2069 6e20   cpu voltage in 
+00000e70: 6d69 6c6c 6976 6f6c 7473 3b0a 2d20 656e  millivolts;.- en
+00000e80: 6572 676f 6e5f 6770 755f 696e 5f76 6f6c  ergon_gpu_in_vol
+00000e90: 7461 6765 5f6d 563a 2063 7572 7265 6e74  tage_mV: current
+00000ea0: 2067 7075 2076 6f6c 7461 6765 2069 6e20   gpu voltage in 
+00000eb0: 6d69 6c6c 6976 6f6c 7473 3b0a 2d20 656e  millivolts;.- en
+00000ec0: 6572 676f 6e5f 6261 7474 6572 795f 7065  ergon_battery_pe
+00000ed0: 7263 656e 7461 6765 3a20 6375 7272 656e  rcentage: curren
+00000ee0: 7420 6261 7474 6572 7920 7065 7263 656e  t battery percen
+00000ef0: 7461 6765 2e0a 0a23 2323 2055 5342 2054  tage...### USB T
+00000f00: 6573 7465 7220 554d 3235 4320 5553 4220  ester UM25C USB 
+00000f10: 4d65 7465 7220 5465 7374 6572 206d 6574  Meter Tester met
+00000f20: 7269 6373 3a0a 4e2e 422e 204f 6e6c 7920  rics:.N.B. Only 
+00000f30: 6966 2072 6561 6c20 7365 6e73 6f72 2069  if real sensor i
+00000f40: 7320 636f 6e6e 6563 7465 6421 0a2d 2065  s connected!.- e
+00000f50: 6e65 7267 6f6e 5f74 6f74 616c 5f61 6374  nergon_total_act
+00000f60: 7561 6c5f 7761 7474 733a 2074 6f74 616c  ual_watts: total
+00000f70: 2061 6374 7561 6c20 706f 7765 7220 636f   actual power co
+00000f80: 6e73 756d 7074 696f 6e20 696e 2077 6174  nsumption in wat
+00000f90: 7473 3b0a 2d20 656e 6572 676f 6e5f 746f  ts;.- energon_to
+00000fa0: 7461 6c5f 6163 7475 616c 5f76 6f6c 7473  tal_actual_volts
+00000fb0: 3a20 746f 7461 6c20 6163 7475 616c 2076  : total actual v
+00000fc0: 6f6c 7461 6765 2069 6e20 766f 6c74 733b  oltage in volts;
+00000fd0: 0a2d 2065 6e65 7267 6f6e 5f74 6f74 616c  .- energon_total
+00000fe0: 5f61 6374 7561 6c5f 616d 7073 3a20 746f  _actual_amps: to
+00000ff0: 7461 6c20 6163 7475 616c 2063 7572 7265  tal actual curre
+00001000: 6e74 2069 6e20 616d 7073 2e0a 0a23 2323  nt in amps...###
+00001010: 204e 6574 776f 726b 206d 6574 7269 6373   Network metrics
+00001020: 3a0a 466f 7220 6561 6368 2069 6e74 6572  :.For each inter
+00001030: 6661 6365 5f6e 616d 650a 2d20 6e65 7477  face_name.- netw
+00001040: 6f72 6b5f 6d65 7472 6963 735f 5b69 6e74  ork_metrics_[int
+00001050: 6572 6661 6365 5f6e 616d 655d 5f72 785f  erface_name]_rx_
+00001060: 7061 636b 6574 733a 2072 6563 6569 7665  packets: receive
+00001070: 6420 7061 636b 6574 733b 0a2d 206e 6574  d packets;.- net
+00001080: 776f 726b 5f6d 6574 7269 6373 5f5b 696e  work_metrics_[in
+00001090: 7465 7266 6163 655f 6e61 6d65 5d5f 7278  terface_name]_rx
+000010a0: 5f62 7974 6573 3a20 7265 6365 6976 6564  _bytes: received
+000010b0: 2062 7974 6573 3b0a 2d20 6e65 7477 6f72   bytes;.- networ
+000010c0: 6b5f 6d65 7472 6963 735f 5b69 6e74 6572  k_metrics_[inter
+000010d0: 6661 6365 5f6e 616d 655d 5f72 785f 6572  face_name]_rx_er
+000010e0: 726f 7273 3a20 7265 6365 6976 6564 2065  rors: received e
+000010f0: 7272 6f72 733b 0a2d 206e 6574 776f 726b  rrors;.- network
+00001100: 5f6d 6574 7269 6373 5f5b 696e 7465 7266  _metrics_[interf
+00001110: 6163 655f 6e61 6d65 5d5f 7278 5f64 726f  ace_name]_rx_dro
+00001120: 7070 6564 3a20 7265 6365 6976 6564 2064  pped: received d
+00001130: 726f 7070 6564 2070 6163 6b65 7473 3b0a  ropped packets;.
+00001140: 2d20 6e65 7477 6f72 6b5f 6d65 7472 6963  - network_metric
+00001150: 735f 5b69 6e74 6572 6661 6365 5f6e 616d  s_[interface_nam
+00001160: 655d 5f74 785f 7061 636b 6574 733a 2074  e]_tx_packets: t
+00001170: 7261 6e73 6d69 7474 6564 2070 6163 6b65  ransmitted packe
+00001180: 7473 3b0a 2d20 6e65 7477 6f72 6b5f 6d65  ts;.- network_me
+00001190: 7472 6963 735f 5b69 6e74 6572 6661 6365  trics_[interface
+000011a0: 5f6e 616d 655d 5f74 785f 6279 7465 733a  _name]_tx_bytes:
+000011b0: 2074 7261 736d 6974 7465 6420 6279 7465   trasmitted byte
+000011c0: 733b 0a2d 206e 6574 776f 726b 5f6d 6574  s;.- network_met
+000011d0: 7269 6373 5f5b 696e 7465 7266 6163 655f  rics_[interface_
+000011e0: 6e61 6d65 5d5f 7478 5f65 7272 6f72 733a  name]_tx_errors:
+000011f0: 2074 7261 6e73 6d69 7474 6564 2065 7272   transmitted err
+00001200: 6f72 733b 0a2d 206e 6574 776f 726b 5f6d  ors;.- network_m
+00001210: 6574 7269 6373 5f5b 696e 7465 7266 6163  etrics_[interfac
+00001220: 655f 6e61 6d65 5d5f 7478 5f64 726f 7070  e_name]_tx_dropp
+00001230: 6564 3a20 7472 616e 736d 6974 7465 6420  ed: transmitted 
+00001240: 6472 6f70 7065 6420 7061 636b 6574 732e  dropped packets.
+00001250: 0a0a 2323 2320 4370 7520 7573 6167 653a  ..### Cpu usage:
+00001260: 0a46 6f72 2065 6163 6820 636f 7265 5f6e  .For each core_n
+00001270: 756d 6265 720a 2d20 656e 6572 676f 6e5f  umber.- energon_
+00001280: 6370 755f 5b63 6f72 655f 6e75 6d62 6572  cpu_[core_number
+00001290: 5d5f 4d48 7a3a 2063 7075 2066 7265 7175  ]_MHz: cpu frequ
+000012a0: 656e 6379 2069 6e20 4d48 7a20 666f 7220  ency in MHz for 
+000012b0: 636f 7265 205b 636f 7265 5f6e 756d 6265  core [core_numbe
+000012c0: 725d 3b0a 2d20 656e 6572 676f 6e5f 6370  r];.- energon_cp
+000012d0: 755f 5b63 6f72 655f 6e75 6d62 6572 5d5f  u_[core_number]_
+000012e0: 7573 6167 655f 7065 7263 656e 7461 6765  usage_percentage
+000012f0: 3a20 4350 5520 7573 6167 6520 6173 2025  : CPU usage as %
+00001300: 2066 6f72 2063 6f72 6520 5b63 6f72 655f   for core [core_
+00001310: 6e75 6d62 6572 5d2e 0a54 6f74 616c 0a2d  number]..Total.-
+00001320: 2065 6e65 7267 6f6e 5f63 7075 5f74 6f74   energon_cpu_tot
+00001330: 616c 5f75 7361 6765 5f70 6572 6365 6e74  al_usage_percent
+00001340: 6167 653a 2074 6f74 616c 2043 5055 2075  age: total CPU u
+00001350: 7361 6765 2061 7320 252e 0a0a 2323 2320  sage as %...### 
+00001360: 5374 6f72 6167 653a 0a46 6f72 2065 6163  Storage:.For eac
+00001370: 6820 6176 6169 6c61 626c 6520 5b73 746f  h available [sto
+00001380: 7261 6765 5f64 6576 6963 655d 0a2d 2065  rage_device].- e
+00001390: 6e65 7267 6f6e 5f73 746f 7261 6765 5f5b  nergon_storage_[
+000013a0: 7374 6f72 6167 655f 6465 7669 6365 5d5f  storage_device]_
+000013b0: 746f 7461 6c5f 6279 7465 733a 2074 6f74  total_bytes: tot
+000013c0: 616c 2062 7974 6573 2066 6f72 2073 746f  al bytes for sto
+000013d0: 7261 6765 205b 7374 6f72 6167 655f 6465  rage [storage_de
+000013e0: 7669 6365 5d3b 0a2d 2065 6e65 7267 6f6e  vice];.- energon
+000013f0: 5f73 746f 7261 6765 5f5b 7374 6f72 6167  _storage_[storag
+00001400: 655f 6465 7669 6365 5d5f 7573 6564 5f62  e_device]_used_b
+00001410: 7974 6573 3a20 7573 6564 2062 7974 6573  ytes: used bytes
+00001420: 2066 6f72 2073 746f 7261 6765 205b 7374   for storage [st
+00001430: 6f72 6167 655f 6465 7669 6365 5d3b 0a2d  orage_device];.-
+00001440: 2065 6e65 7267 6f6e 5f73 746f 7261 6765   energon_storage
+00001450: 5f5b 7374 6f72 6167 655f 6465 7669 6365  _[storage_device
+00001460: 5d5f 6176 6169 6c61 626c 655f 6279 7465  ]_available_byte
+00001470: 733a 2061 7661 696c 6162 6c65 2062 7974  s: available byt
+00001480: 6573 2066 6f72 2073 746f 7261 6765 205b  es for storage [
+00001490: 7374 6f72 6167 655f 6465 7669 6365 5d3b  storage_device];
+000014a0: 0a2d 2065 6e65 7267 6f6e 5f73 746f 7261  .- energon_stora
+000014b0: 6765 5f5b 7374 6f72 6167 655f 6465 7669  ge_[storage_devi
+000014c0: 6365 5d5f 7065 7263 656e 745f 7573 6564  ce]_percent_used
+000014d0: 5f70 6572 6365 6e74 6167 653a 2073 746f  _percentage: sto
+000014e0: 7261 6765 2075 7361 6765 2070 6572 6365  rage usage perce
+000014f0: 6e74 6167 6520 666f 7220 7374 6f72 6167  ntage for storag
+00001500: 6520 5b73 746f 7261 6765 5f64 6576 6963  e [storage_devic
+00001510: 655d 2e0a 546f 7461 6c0a 2d20 656e 6572  e]..Total.- ener
+00001520: 676f 6e5f 7374 6f72 6167 655f 746f 7461  gon_storage_tota
+00001530: 6c5f 6279 7465 733a 2074 6f74 616c 2073  l_bytes: total s
+00001540: 746f 7261 6765 2069 6e20 6279 7465 733b  torage in bytes;
+00001550: 0a2d 2065 6e65 7267 6f6e 5f73 746f 7261  .- energon_stora
+00001560: 6765 5f75 7365 645f 6279 7465 733a 2074  ge_used_bytes: t
+00001570: 6f74 616c 2075 7365 6420 7374 6f72 6167  otal used storag
+00001580: 6520 696e 2062 7974 6573 3b0a 2d20 656e  e in bytes;.- en
+00001590: 6572 676f 6e5f 7374 6f72 6167 655f 6176  ergon_storage_av
+000015a0: 6169 6c61 626c 655f 6279 7465 733a 2074  ailable_bytes: t
+000015b0: 6f74 616c 2061 7661 696c 6162 6c65 2073  otal available s
+000015c0: 746f 7261 6765 2069 6e20 6279 7465 733b  torage in bytes;
+000015d0: 0a2d 2065 6e65 7267 6f6e 5f73 746f 7261  .- energon_stora
+000015e0: 6765 5f70 6572 6365 6e74 5f75 7365 645f  ge_percent_used_
+000015f0: 7065 7263 656e 7461 6765 3a20 5374 6f72  percentage: Stor
+00001600: 6167 6520 7573 6167 6520 7065 7263 656e  age usage percen
+00001610: 7461 6765 2e0a 0a23 2323 2052 616d 2075  tage...### Ram u
+00001620: 7361 6765 3a0a 2d20 656e 6572 676f 6e5f  sage:.- energon_
+00001630: 7261 6d5f 746f 7461 6c5f 6279 7465 733a  ram_total_bytes:
+00001640: 2074 6f74 616c 2072 616d 2069 6e20 6279   total ram in by
+00001650: 7465 733b 0a2d 2065 6e65 7267 6f6e 5f72  tes;.- energon_r
+00001660: 616d 5f75 7365 645f 6279 7465 733a 2074  am_used_bytes: t
+00001670: 6f74 616c 2075 7365 6420 7261 6d20 696e  otal used ram in
+00001680: 2062 7974 6573 3b0a 2d20 656e 6572 676f   bytes;.- energo
+00001690: 6e5f 7261 6d5f 6176 6169 6c61 626c 655f  n_ram_available_
+000016a0: 6279 7465 733a 2074 6f74 616c 2061 7661  bytes: total ava
+000016b0: 696c 6162 6c65 2072 616d 2069 6e20 6279  ilable ram in by
+000016c0: 7465 733b 0a2d 2065 6e65 7267 6f6e 5f72  tes;.- energon_r
+000016d0: 616d 5f75 7365 645f 7065 7263 656e 7461  am_used_percenta
+000016e0: 6765 3a20 7261 6d20 7573 6167 6520 7065  ge: ram usage pe
+000016f0: 7263 656e 7461 6765 2e0a 0a23 2323 2047  rcentage...### G
+00001700: 5055 206d 6574 7269 6373 3a0a 2d20 656e  PU metrics:.- en
+00001710: 6572 676f 6e5f 6770 755f 746f 7461 6c5f  ergon_gpu_total_
+00001720: 7573 6167 655f 7065 7263 656e 7461 6765  usage_percentage
+00001730: 3a20 746f 7461 6c20 4750 5520 7573 6167  : total GPU usag
+00001740: 6520 6173 2025 2e0a 0a23 2323 2054 656d  e as %...### Tem
+00001750: 7065 7261 7475 7265 206d 6574 7269 6373  perature metrics
+00001760: 3a0a 466f 7220 6561 6368 2061 7661 696c  :.For each avail
+00001770: 6162 6c65 205b 7465 6d70 6572 6174 7572  able [temperatur
+00001780: 655f 7365 6e73 6f72 5d0a 2d20 656e 6572  e_sensor].- ener
+00001790: 676f 6e5f 7465 6d70 6572 6174 7572 655f  gon_temperature_
+000017a0: 5b74 656d 7065 7261 7475 7265 5f73 656e  [temperature_sen
+000017b0: 736f 725d 5f6d 433a 2074 656d 7065 7261  sor]_mC: tempera
+000017c0: 7475 7265 2069 6e20 6d69 6c6c 6943 656c  ture in milliCel
+000017d0: 7369 7573 2066 6f72 2073 656e 736f 7220  sius for sensor 
+000017e0: 5b74 656d 7065 7261 7475 7265 5f73 656e  [temperature_sen
+000017f0: 736f 725d 2e0a 0a0a 0a                   sor].....
```

### Comparing `energon_prometheus_exporter-0.0.1/src/energon_prometheus_exporter.egg-info/SOURCES.txt` & `energon_prometheus_exporter-0.0.2/src/energon_prometheus_exporter.egg-info/SOURCES.txt`

 * *Files identical despite different names*

