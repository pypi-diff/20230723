# Comparing `tmp/nonebot_plugin_mystool-1.0.1.tar.gz` & `tmp/nonebot_plugin_mystool-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nonebot_plugin_mystool-1.0.1.tar", max compression
+gzip compressed data, was "nonebot_plugin_mystool-1.1.0.tar", max compression
```

## Comparing `nonebot_plugin_mystool-1.0.1.tar` & `nonebot_plugin_mystool-1.1.0.tar`

### file list

```diff
@@ -1,20 +1,20 @@
--rw-r--r--   0        0        0     1065 2023-06-25 11:38:30.508511 nonebot_plugin_mystool-1.0.1/LICENSE
--rw-r--r--   0        0        0     4016 2023-06-25 11:38:30.508511 nonebot_plugin_mystool-1.0.1/README.md
--rw-r--r--   0        0        0     1317 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/pyproject.toml
--rw-r--r--   0        0        0     2056 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/__init__.py
--rw-r--r--   0        0        0     4438 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/address.py
--rw-r--r--   0        0        0    12132 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/data_model.py
--rw-r--r--   0        0        0    21256 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/exchange.py
--rw-r--r--   0        0        0    11767 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/game_sign_api.py
--rw-r--r--   0        0        0     5467 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/good_image.py
--rw-r--r--   0        0        0     1959 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/help.py
--rw-r--r--   0        0        0     9516 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/login.py
--rw-r--r--   0        0        0    21993 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/myb_missions_api.py
--rw-r--r--   0        0        0    23451 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/plan.py
--rw-r--r--   0        0        0    10768 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/plugin_data.py
--rw-r--r--   0        0        0     8858 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/setting.py
--rw-r--r--   0        0        0    62920 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/simple_api.py
--rw-r--r--   0        0        0     2244 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/user_check.py
--rw-r--r--   0        0        0    11313 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/user_data.py
--rw-r--r--   0        0        0    10283 2023-06-25 11:38:30.512511 nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/utils.py
--rw-r--r--   0        0        0     5394 1970-01-01 00:00:00.000000 nonebot_plugin_mystool-1.0.1/PKG-INFO
+-rw-r--r--   0        0        0     1065 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/LICENSE
+-rw-r--r--   0        0        0     3825 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/README.md
+-rw-r--r--   0        0        0     1322 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/pyproject.toml
+-rw-r--r--   0        0        0     2158 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/__init__.py
+-rw-r--r--   0        0        0     4434 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/address.py
+-rw-r--r--   0        0        0    13805 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/data_model.py
+-rw-r--r--   0        0        0    22678 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/exchange.py
+-rw-r--r--   0        0        0    11757 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/game_sign_api.py
+-rw-r--r--   0        0        0     5463 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/good_image.py
+-rw-r--r--   0        0        0     1955 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/help.py
+-rw-r--r--   0        0        0     9662 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/login.py
+-rw-r--r--   0        0        0    21935 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/myb_missions_api.py
+-rw-r--r--   0        0        0    31387 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/plan.py
+-rw-r--r--   0        0        0    12627 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/plugin_data.py
+-rw-r--r--   0        0        0    10171 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/setting.py
+-rw-r--r--   0        0        0    70861 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/simple_api.py
+-rw-r--r--   0        0        0     2630 2023-07-23 06:23:42.383677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/user_check.py
+-rw-r--r--   0        0        0    11480 2023-07-23 06:23:42.387677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/user_data.py
+-rw-r--r--   0        0        0     9648 2023-07-23 06:23:42.387677 nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/utils.py
+-rw-r--r--   0        0        0     5199 1970-01-01 00:00:00.000000 nonebot_plugin_mystool-1.1.0/PKG-INFO
```

### Comparing `nonebot_plugin_mystool-1.0.1/LICENSE` & `nonebot_plugin_mystool-1.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `nonebot_plugin_mystool-1.0.1/README.md` & `nonebot_plugin_mystool-1.1.0/README.md`

 * *Files 14% similar despite different names*

```diff
@@ -47,205 +47,194 @@
 000002e0: 2d50 524f 2f6e 6f6e 6562 6f74 2d70 6c75  -PRO/nonebot-plu
 000002f0: 6769 6e2d 6d79 7354 6f6f 6c3f 7374 796c  gin-mysTool?styl
 00000300: 653d 666f 722d 7468 652d 6261 6467 6522  e=for-the-badge"
 00000310: 3e0a 3c2f 6469 763e 0a0a 2320 6d79 7354  >.</div>..# mysT
 00000320: 6f6f 6c20 2d20 e7b1 b3e6 b8b8 e7a4 bee8  ool - ..........
 00000330: be85 e58a a9e5 b7a5 e585 b7e6 8f92 e4bb  ................
 00000340: b60a 0a23 2320 f09f 93a3 20e6 9bb4 e696  ...## .... .....
-00000350: b0e5 8685 e5ae b90a 0a23 2323 2032 3032  .........### 202
-00000360: 332e 362e 3233 202d 2076 312e 302e 310a  3.6.23 - v1.0.1.
-00000370: 2d20 e4bf aee5 a48d e697 a0e6 b395 e5af  - ..............
-00000380: bce5 87ba 436f 6f6b 6965 73e7 9a84 e997  ....Cookies.....
-00000390: aee9 a298 0a2d 20e4 bfae e5a4 8de5 9ba0  .....- .........
-000003a0: e7bc bae5 b091 e58f 82e9 878f e8b4 a8e5  ................
-000003b0: 8f98 e4bb aae6 95b0 e68d aee8 808c e5af  ................
-000003c0: bce8 87b4 e4b8 8de6 96ad e68f 90e9 8692  ................
-000003d0: e79a 8442 7567 0a2d 20e4 bfae e5a4 8de8  ...Bug.- .......
-000003e0: b4a6 e58f b7e8 aebe e7bd aee4 b8ad e6b8  ................
-000003f0: b8e6 888f e7ad bee5 88b0 e5bc 80e5 90af  ................
-00000400: 2fe5 85b3 e997 ade7 8ab6 e680 81e5 ae9e  /...............
-00000410: e999 85e5 afb9 e5ba 94e7 9a84 e698 afe7  ................
-00000420: b1b3 e6b8 b8e5 b881 e4bb bbe5 8aa1 e79a  ................
-00000430: 8442 7567 2023 3132 3120 6279 2040 7878  .Bug #121 by @xx
-00000440: 7467 3636 360a 0a0a 2323 2320 3230 3233  tg666...### 2023
-00000450: 2e36 2e32 3320 2d20 7631 2e30 2e30 0a23  .6.23 - v1.0.0.#
-00000460: 2323 2320 7631 2e30 2e30 0a2d 20e4 bfae  ### v1.0.0.- ...
-00000470: e5a4 8d57 696e 646f 7773 2c20 6d61 634f  ...Windows, macO
-00000480: 53e5 a49a e8bf 9be7 a88b e794 9fe6 8890  S...............
-00000490: e595 86e5 9381 e59b bee7 8987 e5a4 b1e8  ................
-000004a0: b4a5 e79a 84e9 97ae e9a2 9820 5b23 3132  ........... [#12
-000004b0: 305d 2868 7474 7073 3a2f 2f67 6974 6875  0](https://githu
-000004c0: 622e 636f 6d2f 4c6a 7a64 2d50 524f 2f6e  b.com/Ljzd-PRO/n
-000004d0: 6f6e 6562 6f74 2d70 6c75 6769 6e2d 6d79  onebot-plugin-my
-000004e0: 7374 6f6f 6c2f 7075 6c6c 2f31 3230 2920  stool/pull/120) 
-000004f0: 6279 2040 4e69 6768 742d 7374 6172 732d  by @Night-stars-
-00000500: 310a 0a23 2323 2320 7631 2e30 2e30 2d62  1..#### v1.0.0-b
-00000510: 6574 612e 320a 2d20 e694 afe6 8c81 e4bd  eta.2.- ........
-00000520: bfe7 94a8 e4ba bae6 9cba e9aa 8ce8 af81  ................
-00000530: e689 93e7 a081 e5b9 b3e5 8fb0 e5a4 84e7  ................
-00000540: 9086 e4ba bae6 9cba e9aa 8ce8 af81 e4bb  ................
-00000550: bbe5 8aa1 205b 2331 3139 5d28 6874 7470  .... [#119](http
-00000560: 733a 2f2f 6769 7468 7562 2e63 6f6d 2f4c  s://github.com/L
-00000570: 6a7a 642d 5052 4f2f 6e6f 6e65 626f 742d  jzd-PRO/nonebot-
-00000580: 706c 7567 696e 2d6d 7973 746f 6f6c 2f70  plugin-mystool/p
-00000590: 756c 6c2f 3131 3929 2062 7920 404e 6967  ull/119) by @Nig
-000005a0: 6874 2d73 7461 7273 2d31 0a2d 20e5 8e9f  ht-stars-1.- ...
-000005b0: e7a5 9ee4 bebf e7ac bae8 8eb7 e58f 96e5  ................
-000005c0: a4b1 e8b4 a5e6 97b6 e69b b4e6 8da2 e4b8  ................
-000005d0: bae4 bdbf e794 a8e7 b1b3 e6b8 b8e7 a4be  ................
-000005e0: 694f 53e5 b08f e7bb 84e4 bbb6 4150 49e8  iOS.........API.
-000005f0: 8eb7 e58f 9620 5b23 3131 395d 2868 7474  ..... [#119](htt
-00000600: 7073 3a2f 2f67 6974 6875 622e 636f 6d2f  ps://github.com/
-00000610: 4c6a 7a64 2d50 524f 2f6e 6f6e 6562 6f74  Ljzd-PRO/nonebot
-00000620: 2d70 6c75 6769 6e2d 6d79 7374 6f6f 6c2f  -plugin-mystool/
-00000630: 7075 6c6c 2f31 3139 2920 6279 2040 4e69  pull/119) by @Ni
-00000640: 6768 742d 7374 6172 732d 310a 2d20 e4bf  ght-stars-1.- ..
-00000650: aee5 a48d e58e 9fe7 a59e e4be bfe7 acba  ................
-00000660: e592 8ce8 aea8 e8ae bae5 8cba e7ad bee5  ................
-00000670: 88b0 e58f afe8 83bd e59b a0e4 b8ba 4453  ..............DS
-00000680: e697 a0e6 9588 e880 8ce5 a4b1 e8b4 a5e7  ................
-00000690: 9a84 e997 aee9 a298 0a0a 2323 2323 2076  ..........#### v
-000006a0: 312e 302e 302d 6265 7461 2e31 0a2d 20e5  1.0.0-beta.1.- .
-000006b0: a4a7 e987 8fe7 9a84 e4bb a3e7 a081 e987  ................
-000006c0: 8de6 9e84 efbc 8ce5 8c85 e68b ace7 b1b3  ................
-000006d0: e6b8 b8e7 a4be 4150 49e7 9a84 e5ae a2e6  ......API.......
-000006e0: 88b7 e7ab afe5 ae9e e78e b0e3 8081 e794  ................
-000006f0: a8e6 88b7 e695 b0e6 8dae e79b b8e5 85b3  ................
-00000700: e380 81e6 8f92 e4bb b6e9 858d e7bd aee7  ................
-00000710: 9bb8 e585 b3e3 8081 4150 49e7 9bb8 e585  ........API.....
-00000720: b3e6 95b0 e68d aee6 a8a1 e59e 8b0a 2d20  ..............- 
-00000730: e4bb 8ee6 98be e7a4 bae7 94a8 e688 b7e8  ................
-00000740: b4a6 e58f b7e7 bb91 e5ae 9ae7 9a84 e689  ................
-00000750: 8be6 9cba e58f b7e6 94b9 e4b8 bae6 98be  ................
-00000760: e7a4 bae8 b4a6 e58f b7e7 9a84 e7b1 b3e6  ................
-00000770: b8b8 e7a4 be49 440a 2d20 e8ae bee7 bdae  .....ID.- ......
-00000780: e380 81e5 8591 e68d a2e8 aea1 e588 92e5  ................
-00000790: 8a9f e883 bde6 94af e68c 81e7 bea4 e881  ................
-000007a0: 8ae4 bdbf e794 a80a 2d20 e799 bbe9 9986  ........- ......
-000007b0: e7bb 91e5 ae9a e58f aae9 9c80 e8a6 81e8  ................
-000007c0: bf9b e8a1 8ce4 b880 e6ac a1e7 9fad e4bf  ................
-000007d0: a1e9 aa8c e8af 810a 2d20 e794 a8e6 88b7  ........- ......
-000007e0: e695 b0e6 8dae e696 87e4 bbb6 e380 81e6  ................
-000007f0: 8f92 e4bb b6e9 858d e7bd aee6 9687 e4bb  ................
-00000800: b620 2a2a e6a0 bce5 bc8f e69b b4e6 96b0  . **............
-00000810: efbc 8ce4 b88e 2076 312e 302e 3020 e4b9  ...... v1.0.0 ..
-00000820: 8be5 898d e79a 84e7 8988 e69c ace4 b88d  ................
-00000830: e585 bce5 aeb9 2a2a 0a2d 20e4 bfae e5a4  ......**.- .....
-00000840: 8de6 b7bb e58a a0e5 8591 e68d a2e4 bbbb  ................
-00000850: e58a a1e6 97b6 e587 bae7 8eb0 e79a 8455  ...............U
-00000860: 4944 e4b8 8de5 ad98 e59c a8e9 9499 e8af  ID..............
-00000870: af0a 2d20 e4bf aee5 a48d e595 86e5 9381  ..- ............
-00000880: e59b bee7 8987 e794 9fe6 8890 e5ae 8ce6  ................
-00000890: 898d e58f 91e5 87ba e590 8ee5 8fb0 e6ad  ................
-000008a0: a3e5 9ca8 e794 9fe6 8890 e68f 90e7 a4ba  ................
-000008b0: e79a 84e9 97ae e9a2 980a 2d20 e5bc 82e5  ..........- ....
-000008c0: b8b8 e68d 95e8 8eb7 e69b b4e5 8aa0 e587  ................
-000008d0: 86e7 a1ae 0a2d 20e6 94b9 e8bf 9be4 ba86  .....- .........
-000008e0: e4b8 80e4 ba9b e696 87e6 9cac 0a0a 2323  ..............##
-000008f0: 2320 3230 3233 2e35 2e31 3820 2d20 7630  # 2023.5.18 - v0
-00000900: 2e32 2e39 0a2d 20e5 a49a e8bf 9be7 a88b  .2.9.- .........
-00000910: e794 9fe6 8890 e595 86e5 9381 e59b bee7  ................
-00000920: 8987 efbc 88e5 a49a e6a0 b8ef bc89 efbc  ................
-00000930: 8ce5 8aa0 e5bf abe5 9bbe e789 87e7 949f  ................
-00000940: e688 90e9 809f e5ba a60a 2d20 e4bf aee5  ..........- ....
-00000950: a48d e983 a8e5 8886 e595 86e5 9381 e585  ................
-00000960: 91e6 8da2 e697 b6e9 97b4 e994 99e8 afaf  ................
-00000970: e79a 84e9 97ae e9a2 98ef bc88 e5a6 82e7  ................
-00000980: b1b3 e6b8 b8e7 a4be e595 86e5 9381 e699  ................
-00000990: 9ae4 ba86 e4b8 80e5 91a8 efbc 890a 0a23  ...............#
-000009a0: 2323 2032 3032 332e 352e 3420 2d20 7630  ## 2023.5.4 - v0
-000009b0: 2e32 2e38 0a2d 20e5 a29e e58a a0e5 afb9  .2.8.- .........
-000009c0: e698 9fe7 a9b9 e993 81e9 8193 e79a 84e7  ................
-000009d0: adbe e588 b0e5 8a9f e883 bde7 9a84 e694  ................
-000009e0: afe6 8c81 202d 205b 2338 395d 2868 7474  .... - [#89](htt
-000009f0: 7073 3a2f 2f67 6974 6875 622e 636f 6d2f  ps://github.com/
-00000a00: 4c6a 7a64 2d50 524f 2f6e 6f6e 6562 6f74  Ljzd-PRO/nonebot
-00000a10: 2d70 6c75 6769 6e2d 6d79 7374 6f6f 6c2f  -plugin-mystool/
-00000a20: 7075 6c6c 2f38 3929 2062 7920 4061 7961  pull/89) by @aya
-00000a30: 6b61 7375 6b69 0a2d 20e4 bfae e5a4 8de6  kasuki.- .......
-00000a40: 8f92 e4bb b6e5 91bd e4bb a4e4 bc98 e585  ................
-00000a50: 88e5 baa6 e997 aee9 a298 202d 205b 2338  .......... - [#8
-00000a60: 385d 2868 7474 7073 3a2f 2f67 6974 6875  8](https://githu
-00000a70: 622e 636f 6d2f 4c6a 7a64 2d50 524f 2f6e  b.com/Ljzd-PRO/n
-00000a80: 6f6e 6562 6f74 2d70 6c75 6769 6e2d 6d79  onebot-plugin-my
-00000a90: 7374 6f6f 6c2f 7075 6c6c 2f38 3829 2062  stool/pull/88) b
-00000aa0: 7920 4061 7961 6b61 7375 6b69 0a2d 20e9  y @ayakasuki.- .
-00000ab0: 83a8 e588 86e6 9687 e69c ace9 9499 e8af  ................
-00000ac0: afe4 bfae e6ad a320 2d20 5b23 3930 5d28  ....... - [#90](
-00000ad0: 6874 7470 733a 2f2f 6769 7468 7562 2e63  https://github.c
-00000ae0: 6f6d 2f4c 6a7a 642d 5052 4f2f 6e6f 6e65  om/Ljzd-PRO/none
-00000af0: 626f 742d 706c 7567 696e 2d6d 7973 746f  bot-plugin-mysto
-00000b00: 6f6c 2f70 756c 6c2f 3930 2920 6279 2040  ol/pull/90) by @
-00000b10: 626c 6163 6b2d 7a65 726f 3335 380a 0a23  black-zero358..#
-00000b20: 2320 e58a 9fe8 83bd e592 8ce7 89b9 e680  # ..............
-00000b30: a70a 0a2d 20e7 9fad e4bf a1e9 aa8c e8af  ...- ...........
-00000b40: 81e7 99bb e5bd 95ef bc8c e585 8de6 8a93  ................
-00000b50: e58c 85e8 8eb7 e58f 9620 436f 6f6b 6965  ......... Cookie
-00000b60: 0a2d 20e8 87aa e58a a8e5 ae8c e688 90e6  .- .............
-00000b70: af8f e697 a5e7 b1b3 e6b8 b8e5 b881 e4bb  ................
-00000b80: bbe5 8aa1 0a2d 20e8 87aa e58a a8e8 bf9b  .....- .........
-00000b90: e8a1 8ce6 b8b8 e688 8fe7 adbe e588 b00a  ................
-00000ba0: 2d20 e58f afe5 88b6 e5ae 9ae7 b1b3 e6b8  - ..............
-00000bb0: b8e5 b881 e595 86e5 9381 e585 91e6 8da2  ................
-00000bc0: e8ae a1e5 8892 efbc 8ce5 88b0 e782 b9e5  ................
-00000bd0: 8591 e68d a20a 2d20 e58f afe6 94af e68c  ......- ........
-00000be0: 81e5 a49a e4b8 aa20 5151 20e8 b4a6 e58f  ....... QQ .....
-00000bf0: b7ef bc8c e6af 8fe4 b8aa 2051 5120 e8b4  .......... QQ ..
-00000c00: a6e5 8fb7 e58f afe7 bb91 e5ae 9ae5 a49a  ................
-00000c10: e4b8 aae7 b1b3 e593 88e6 b8b8 e8b4 a6e6  ................
-00000c20: 88b7 0a2d 2051 5120 e68e a8e9 8081 e689  ...- QQ ........
-00000c30: a7e8 a18c e7bb 93e6 9e9c e980 9ae7 9fa5  ................
-00000c40: 0a2d 20e5 8e9f e7a5 9ee6 a091 e884 82e3  .- .............
-00000c50: 8081 e6b4 9ee5 a4a9 e5ae 9de9 92b1 e380  ................
-00000c60: 81e8 b4a8 e987 8fe5 8f82 e58f 98e4 bbaa  ................
-00000c70: e5b7 b2e6 bba1 e697 b6e6 8ea8 e980 81e9  ................
-00000c80: 809a e79f a50a 0a23 2320 e4bd bfe7 94a8  .......## ......
-00000c90: e8af b4e6 988e 0a0a 2323 2320 f09f 9ba0  ........### ....
-00000ca0: efb8 8f20 4e6f 6e65 426f 7432 20e6 9cba  ... NoneBot2 ...
-00000cb0: e599 a8e4 baba e983 a8e7 bdb2 e592 8ce6  ................
-00000cc0: 8f92 e4bb b6e5 ae89 e8a3 850a 0ae8 afb7  ................
-00000cd0: e69f a5e7 9c8b 202d 3e20 5bf0 9f94 9749  ...... -> [....I
-00000ce0: 6e73 7461 6c6c 6174 696f 6e5d 2868 7474  nstallation](htt
-00000cf0: 7073 3a2f 2f67 6974 6875 622e 636f 6d2f  ps://github.com/
-00000d00: 4c6a 7a64 2d50 524f 2f6e 6f6e 6562 6f74  Ljzd-PRO/nonebot
-00000d10: 2d70 6c75 6769 6e2d 6d79 7374 6f6f 6c2f  -plugin-mystool/
-00000d20: 7769 6b69 2f49 6e73 7461 6c6c 6174 696f  wiki/Installatio
-00000d30: 6e29 0a0a 2323 2320 f09f 9396 20e6 8f92  n)..### .... ...
-00000d40: e4bb b6e5 85b7 e4bd 93e4 bdbf e794 a8e8  ................
-00000d50: afb4 e698 8e0a 0ae8 afb7 e69f a5e7 9c8b  ................
-00000d60: 202d 3e20 5bf0 9f94 9757 696b 6920 e696   -> [....Wiki ..
-00000d70: 87e6 a1a3 5d28 6874 7470 733a 2f2f 6769  ....](https://gi
-00000d80: 7468 7562 2e63 6f6d 2f4c 6a7a 642d 5052  thub.com/Ljzd-PR
-00000d90: 4f2f 6e6f 6e65 626f 742d 706c 7567 696e  O/nonebot-plugin
-00000da0: 2d6d 7973 746f 6f6c 2f77 696b 6929 0a0a  -mystool/wiki)..
-00000db0: 2323 2320 e29d 9320 e88e b7e5 8f96 e68f  ### ... ........
-00000dc0: 92e4 bbb6 e5b8 aee5 8aa9 e4bf a1e6 81af  ................
-00000dd0: 0a0a 2323 2323 20e6 8f92 e4bb b6e5 91bd  ..#### .........
-00000de0: e4bb a40a 0a60 6060 0a2f e5b8 aee5 8aa9  .....```./......
-00000df0: 0a60 6060 0a0a 3e20 e29a a0ef b88f 20e6  .```..> ...... .
-00000e00: b3a8 e684 8f20 e6ad a4e5 a484 e6b2 a1e6  ..... ..........
-00000e10: 9c89 e4bd bfe7 94a8 205b f09f 9497 20e6  ........ [.... .
-00000e20: 8f92 e4bb b6e5 91bd e4bb a4e5 a4b4 5d28  ..............](
-00000e30: 6874 7470 733a 2f2f 6769 7468 7562 2e63  https://github.c
-00000e40: 6f6d 2f4c 6a7a 642d 5052 4f2f 6e6f 6e65  om/Ljzd-PRO/none
-00000e50: 626f 742d 706c 7567 696e 2d6d 7973 746f  bot-plugin-mysto
-00000e60: 6f6c 2f77 696b 692f 436f 6e66 6967 7572  ol/wiki/Configur
-00000e70: 6174 696f 6e2d 436f 6e66 6967 2363 6f6d  ation-Config#com
-00000e80: 6d61 6e64 7374 6172 7429 0a0a 2323 20e5  mandstart)..## .
-00000e90: 85b6 e4bb 960a 0a23 2323 205b f09f 9383  .......### [....
-00000ea0: e6ba 90e7 a081 e8af b4e6 988e 5d28 6874  ............](ht
-00000eb0: 7470 733a 2f2f 6769 7468 7562 2e63 6f6d  tps://github.com
-00000ec0: 2f4c 6a7a 642d 5052 4f2f 6e6f 6e65 626f  /Ljzd-PRO/nonebo
-00000ed0: 742d 706c 7567 696e 2d6d 7973 746f 6f6c  t-plugin-mystool
-00000ee0: 2f77 696b 692f 536f 7572 6365 2d53 7472  /wiki/Source-Str
-00000ef0: 7563 7475 7265 290a 2323 2320 e980 82e9  ucture).### ....
-00000f00: 858d 205b e7bb aae5 b1b1 e79c 9fe5 afbb  .. [............
-00000f10: 426f 745d 2868 7474 7073 3a2f 2f67 6974  Bot](https://git
-00000f20: 6875 622e 636f 6d2f 4869 6269 4b69 6572  hub.com/HibiKier
-00000f30: 2f7a 6865 6e78 756e 5f62 6f74 2920 e79a  /zhenxun_bot) ..
-00000f40: 84e5 8886 e694 af0a 2d20 6874 7470 733a  ........- https:
-00000f50: 2f2f 6769 7468 7562 2e63 6f6d 2f4d 5754  //github.com/MWT
-00000f60: 4a43 2f7a 6865 6e78 756e 2d70 6c75 6769  JC/zhenxun-plugi
-00000f70: 6e2d 6d79 7374 6f6f 6c0a 2d20 6874 7470  n-mystool.- http
-00000f80: 733a 2f2f 6769 7468 7562 2e63 6f6d 2f61  s://github.com/a
-00000f90: 7961 6b61 7375 6b69 2f6e 6f6e 6562 6f74  yakasuki/nonebot
-00000fa0: 2d70 6c75 6769 6e2d 6d79 7374 6f6f 6c0a  -plugin-mystool.
+00000350: b0e5 8685 e5ae b90a 2323 2320 3230 3233  ........### 2023
+00000360: 2e37 2e32 3320 2d20 7631 2e31 2e30 0a2d  .7.23 - v1.1.0.-
+00000370: 20e5 a29e e58a a0e5 b4a9 e59d 8fef bc9a   ...............
+00000380: e698 9fe7 a9b9 e993 81e9 8193 e79a 84e4  ................
+00000390: bebf e7ac bae5 8a9f e883 bd20 2331 3430  ........... #140
+000003a0: 2023 3134 3320 6279 2040 4a6f 7365 616e   #143 by @Josean
+000003b0: 646c 7575 6520 4052 656d 6944 7265 0a20  dluue @RemiDre. 
+000003c0: 2020 203e 20e8 afb4 e698 8ee6 9687 e6a1     > ...........
+000003d0: a3ef bc9a 5bf0 9f94 97e6 989f e7a9 b9e9  ....[...........
+000003e0: 9381 e981 93e5 ae9e e697 b6e4 bebf e7ac  ................
+000003f0: ba5d 2868 7474 7073 3a2f 2f67 6974 6875  .](https://githu
+00000400: 622e 636f 6d2f 4c6a 7a64 2d50 524f 2f6e  b.com/Ljzd-PRO/n
+00000410: 6f6e 6562 6f74 2d70 6c75 6769 6e2d 6d79  onebot-plugin-my
+00000420: 7374 6f6f 6c2f 7769 6b69 2f49 6e66 6f72  stool/wiki/Infor
+00000430: 6d61 7469 6f6e 2d53 7461 7252 6169 6c53  mation-StarRailS
+00000440: 7461 7475 7329 0a2d 20e4 bfae e5a4 8de6  tatus).- .......
+00000450: af8f e5b0 8fe6 97b6 e983 bde5 8f91 e980  ................
+00000460: 81e4 bebf e7ac bae9 809a e79f a5e7 9a84  ................
+00000470: 4275 6720 2331 3335 0a2d 20e4 baba e69c  Bug #135.- .....
+00000480: bae9 aa8c e8af 81e6 8993 e7a0 81e5 b9b3  ................
+00000490: e58f b0e6 94af e68c 81e8 87aa e5ae 9ae4  ................
+000004a0: b989 4a53 4f4e e586 85e5 aeb9 2023 3133  ..JSON...... #13
+000004b0: 330a 2020 2020 3e20 e8af b4e6 988e e696  3.    > ........
+000004c0: 87e6 a1a3 efbc 9a5b f09f 9497 6765 6574  .......[....geet
+000004d0: 6573 745f 6a73 6f6e 5d28 6874 7470 733a  est_json](https:
+000004e0: 2f2f 6769 7468 7562 2e63 6f6d 2f4c 6a7a  //github.com/Ljz
+000004f0: 642d 5052 4f2f 6e6f 6e65 626f 742d 706c  d-PRO/nonebot-pl
+00000500: 7567 696e 2d6d 7973 746f 6f6c 2f77 696b  ugin-mystool/wik
+00000510: 692f 436f 6e66 6967 7572 6174 696f 6e2d  i/Configuration-
+00000520: 5072 6566 6572 656e 6365 2367 6565 7465  Preference#geete
+00000530: 7374 5f6a 736f 6e29 0a2d 20e4 bfae e5a4  st_json).- .....
+00000540: 8de5 9586 e593 81e5 8591 e68d a241 5049  .............API
+00000550: 2023 3131 300a 2d20 e4b8 8de5 9ca8 e5a5   #110.- ........
+00000560: bde5 8f8b e588 97e8 a1a8 e79a 84e7 94a8  ................
+00000570: e688 b7e6 95b0 e68d aee5 9ca8 e588 a0e9  ................
+00000580: 99a4 e589 8de5 b086 e8bf 9be8 a18c e5a4  ................
+00000590: 87e4 bbbd 2023 3132 390a 2020 2020 3e20  .... #129.    > 
+000005a0: e5a4 87e4 bbbd e79b aee5 bd95 efbc 9a60  ...............`
+000005b0: 6461 7461 2f6e 6f6e 6562 6f74 5f70 6c75  data/nonebot_plu
+000005c0: 6769 6e5f 6d79 7374 6f6f 6c2f 6465 6c65  gin_mystool/dele
+000005d0: 7465 6455 7365 7273 600a 2d20 e998 b2e6  tedUsers`.- ....
+000005e0: ada2 e59b a0e6 8f92 e4bb b6e6 95b0 e68d  ................
+000005f0: aee6 9687 e4bb b6e4 b8ad e9bb 98e8 aea4  ................
+00000600: e5ad 98e5 9ca8 2064 6576 6963 655f 636f  ...... device_co
+00000610: 6e66 6967 2c20 7361 6c74 5f63 6f6e 6669  nfig, salt_confi
+00000620: 6720 e880 8ce5 afbc e887 b4e6 9bb4 e696  g ..............
+00000630: b0e5 908e e9bb 98e8 aea4 e985 8de7 bdae  ................
+00000640: e8a2 abe5 8e9f e985 8de7 bdae e8a6 86e7  ................
+00000650: 9b96 e79a 84e9 97ae e9a2 980a 2d20 e88b  ............- ..
+00000660: a5e9 9c80 e8a6 81e4 bfae e694 b920 6465  ............. de
+00000670: 7669 6365 5f63 6f6e 6669 6720 e985 8de7  vice_config ....
+00000680: bdae efbc 8ce4 bfae e694 b9e5 908e e8bf  ................
+00000690: 98e8 aebe e7bd aee6 8f92 e4bb b6e6 95b0  ................
+000006a0: e68d aee6 9687 e4bb b6e4 b8ad 2070 7265  ............ pre
+000006b0: 6665 7265 6e63 652e 6f76 6572 7269 6465  ference.override
+000006c0: 5f64 6576 6963 655f 616e 645f 7361 6c74  _device_and_salt
+000006d0: 20e4 b8ba 2074 7275 6520 e4bb a5e8 a686   ... true ......
+000006e0: e79b 96e9 bb98 e8ae a4e5 80bc 0a20 2020  .............   
+000006f0: 203e 20e8 afb4 e698 8ee6 9687 e6a1 a3ef   > .............
+00000700: bc9a 0a20 2020 203e 202d 205b f09f 9497  ...    > - [....
+00000710: e7bd 91e7 bb9c e8af b7e6 b182 e8ae bee5  ................
+00000720: a487 e4bf a1e6 81af 2060 636c 6173 7320  ........ `class 
+00000730: 4465 7669 6365 436f 6e66 6967 605d 2868  DeviceConfig`](h
+00000740: 7474 7073 3a2f 2f67 6974 6875 622e 636f  ttps://github.co
+00000750: 6d2f 4c6a 7a64 2d50 524f 2f6e 6f6e 6562  m/Ljzd-PRO/noneb
+00000760: 6f74 2d70 6c75 6769 6e2d 6d79 7374 6f6f  ot-plugin-mystoo
+00000770: 6c2f 7769 6b69 2f43 6f6e 6669 6775 7261  l/wiki/Configura
+00000780: 7469 6f6e 2d44 6576 6963 6543 6f6e 6669  tion-DeviceConfi
+00000790: 6729 0a20 2020 203e 202d 205b f09f 9497  g).    > - [....
+000007a0: 6f76 6572 7269 6465 5f64 6576 6963 655f  override_device_
+000007b0: 616e 645f 7361 6c74 5d28 6874 7470 733a  and_salt](https:
+000007c0: 2f2f 6769 7468 7562 2e63 6f6d 2f4c 6a7a  //github.com/Ljz
+000007d0: 642d 5052 4f2f 6e6f 6e65 626f 742d 706c  d-PRO/nonebot-pl
+000007e0: 7567 696e 2d6d 7973 746f 6f6c 2f77 696b  ugin-mystool/wik
+000007f0: 692f 436f 6e66 6967 7572 6174 696f 6e2d  i/Configuration-
+00000800: 5072 6566 6572 656e 6365 236f 7665 7272  Preference#overr
+00000810: 6964 655f 6465 7669 6365 5f61 6e64 5f73  ide_device_and_s
+00000820: 616c 7429 0a2d 20e5 9ca8 e585 91e6 8da2  alt).- .........
+00000830: e5bc 80e5 a78b e590 8ee7 9a84 e4b8 80e6  ................
+00000840: aeb5 e697 b6e9 97b4 e586 85e4 b88d e696  ................
+00000850: ade5 b09d e8af 95e5 8591 e68d a2ef bc8c  ................
+00000860: e79b b4e5 88b0 e688 90e5 8a9f 2023 3131  ............ #11
+00000870: 300a 2d20 e585 91e6 8da2 e5bc 80e5 a78b  0.- ............
+00000880: e590 8ee5 b086 e4b8 8de4 bc9a e5bb b6e8  ................
+00000890: bf9f e585 91e6 8da2 efbc 8ce7 94a8 e688  ................
+000008a0: b7e6 95b0 e68d aee6 9687 e4bb b6e4 b8ad  ................
+000008b0: 2060 7072 6566 6572 656e 6365 2e65 7863   `preference.exc
+000008c0: 6861 6e67 655f 6c61 7465 6e63 7960 20e5  hange_latency` .
+000008d0: b086 e4bd 9ce4 b8ba e590 8ce4 b880 e7ba  ................
+000008e0: bfe7 a88b e4b8 8be6 af8f e4b8 aae5 8591  ................
+000008f0: e68d a2e8 afb7 e6b1 82e4 b98b e997 b4e7  ................
+00000900: 9a84 e697 b6e9 97b4 e997 b4e9 9a94 2023  .............. #
+00000910: 3131 300a 2d20 e585 91e6 8da2 e8af b7e6  110.- ..........
+00000920: b182 e697 a5e5 bf97 e586 85e5 aeb9 e5a2  ................
+00000930: 9ee5 8aa0 e4ba 86e5 8f91 e980 81e8 afb7  ................
+00000940: e6b1 82e6 97b6 e79a 84e6 97b6 e997 b4e6  ................
+00000950: 88b3 0a0a 2323 2320 3230 3233 2e36 2e32  ....### 2023.6.2
+00000960: 3320 2d20 7631 2e30 2e31 0a2d 20e4 bfae  3 - v1.0.1.- ...
+00000970: e5a4 8de6 97a0 e6b3 95e5 afbc e587 ba43  ...............C
+00000980: 6f6f 6b69 6573 e79a 84e9 97ae e9a2 980a  ookies..........
+00000990: 2d20 e4bf aee5 a48d e59b a0e7 bcba e5b0  - ..............
+000009a0: 91e5 8f82 e987 8fe8 b4a8 e58f 98e4 bbaa  ................
+000009b0: e695 b0e6 8dae e880 8ce5 afbc e887 b4e4  ................
+000009c0: b88d e696 ade6 8f90 e986 92e7 9a84 4275  ..............Bu
+000009d0: 670a 2d20 e4bf aee5 a48d e8b4 a6e5 8fb7  g.- ............
+000009e0: e8ae bee7 bdae e4b8 ade6 b8b8 e688 8fe7  ................
+000009f0: adbe e588 b0e5 bc80 e590 af2f e585 b3e9  .........../....
+00000a00: 97ad e78a b6e6 8081 e5ae 9ee9 9985 e5af  ................
+00000a10: b9e5 ba94 e79a 84e6 98af e7b1 b3e6 b8b8  ................
+00000a20: e5b8 81e4 bbbb e58a a1e7 9a84 4275 6720  ............Bug 
+00000a30: 2331 3231 2062 7920 4078 7874 6736 3636  #121 by @xxtg666
+00000a40: 0a0a 2323 20e5 8a9f e883 bde5 928c e789  ..## ...........
+00000a50: b9e6 80a7 0a0a 2d20 e79f ade4 bfa1 e9aa  ......- ........
+00000a60: 8ce8 af81 e799 bbe5 bd95 efbc 8ce5 858d  ................
+00000a70: e68a 93e5 8c85 e88e b7e5 8f96 2043 6f6f  ............ Coo
+00000a80: 6b69 650a 2d20 e887 aae5 8aa8 e5ae 8ce6  kie.- ..........
+00000a90: 8890 e6af 8fe6 97a5 e7b1 b3e6 b8b8 e5b8  ................
+00000aa0: 81e4 bbbb e58a a10a 2d20 e887 aae5 8aa8  ........- ......
+00000ab0: e8bf 9be8 a18c e6b8 b8e6 888f e7ad bee5  ................
+00000ac0: 88b0 0a2d 20e5 8faf e588 b6e5 ae9a e7b1  ...- ...........
+00000ad0: b3e6 b8b8 e5b8 81e5 9586 e593 81e5 8591  ................
+00000ae0: e68d a2e8 aea1 e588 92ef bc8c e588 b0e7  ................
+00000af0: 82b9 e585 91e6 8da2 efbc 88e5 9ba0 e58a  ................
+00000b00: a0e5 85a5 e4ba 86e4 baba e69c bae9 aa8c  ................
+00000b10: e8af 81ef bc8c e688 90e5 8a9f e78e 87e8  ................
+00000b20: be83 e4bd 8eef bc89 0a2d 20e5 8faf e694  .........- .....
+00000b30: afe6 8c81 e5a4 9ae4 b8aa 2051 5120 e8b4  .......... QQ ..
+00000b40: a6e5 8fb7 efbc 8ce6 af8f e4b8 aa20 5151  ............. QQ
+00000b50: 20e8 b4a6 e58f b7e5 8faf e7bb 91e5 ae9a   ...............
+00000b60: e5a4 9ae4 b8aa e7b1 b3e5 9388 e6b8 b8e8  ................
+00000b70: b4a6 e688 b70a 2d20 5151 20e6 8ea8 e980  ......- QQ .....
+00000b80: 81e6 89a7 e8a1 8ce7 bb93 e69e 9ce9 809a  ................
+00000b90: e79f a50a 2d20 e58e 9fe7 a59e e380 81e5  ....- ..........
+00000ba0: b4a9 e59d 8fef bc9a e698 9fe7 a9b9 e993  ................
+00000bb0: 81e9 8193 e78a b6e6 8081 e4be bfe7 acba  ................
+00000bc0: e980 9ae7 9fa5 0a0a 2323 20e4 bdbf e794  ........## .....
+00000bd0: a8e8 afb4 e698 8e0a 0a23 2323 20f0 9f9b  .........### ...
+00000be0: a0ef b88f 204e 6f6e 6542 6f74 3220 e69c  .... NoneBot2 ..
+00000bf0: bae5 99a8 e4ba bae9 83a8 e7bd b2e5 928c  ................
+00000c00: e68f 92e4 bbb6 e5ae 89e8 a385 0a0a e8af  ................
+00000c10: b7e6 9fa5 e79c 8b20 2d3e 205b f09f 9497  ....... -> [....
+00000c20: 496e 7374 616c 6c61 7469 6f6e 5d28 6874  Installation](ht
+00000c30: 7470 733a 2f2f 6769 7468 7562 2e63 6f6d  tps://github.com
+00000c40: 2f4c 6a7a 642d 5052 4f2f 6e6f 6e65 626f  /Ljzd-PRO/nonebo
+00000c50: 742d 706c 7567 696e 2d6d 7973 746f 6f6c  t-plugin-mystool
+00000c60: 2f77 696b 692f 496e 7374 616c 6c61 7469  /wiki/Installati
+00000c70: 6f6e 290a 0a23 2323 20f0 9f93 9620 e68f  on)..### .... ..
+00000c80: 92e4 bbb6 e585 b7e4 bd93 e4bd bfe7 94a8  ................
+00000c90: e8af b4e6 988e 0a0a e8af b7e6 9fa5 e79c  ................
+00000ca0: 8b20 2d3e 205b f09f 9497 5769 6b69 20e6  . -> [....Wiki .
+00000cb0: 9687 e6a1 a35d 2868 7474 7073 3a2f 2f67  .....](https://g
+00000cc0: 6974 6875 622e 636f 6d2f 4c6a 7a64 2d50  ithub.com/Ljzd-P
+00000cd0: 524f 2f6e 6f6e 6562 6f74 2d70 6c75 6769  RO/nonebot-plugi
+00000ce0: 6e2d 6d79 7374 6f6f 6c2f 7769 6b69 290a  n-mystool/wiki).
+00000cf0: 0a23 2323 20e2 9d93 20e8 8eb7 e58f 96e6  .### ... .......
+00000d00: 8f92 e4bb b6e5 b8ae e58a a9e4 bfa1 e681  ................
+00000d10: af0a 0a23 2323 2320 e68f 92e4 bbb6 e591  ...#### ........
+00000d20: bde4 bba4 0a0a 6060 600a 2fe5 b8ae e58a  ......```./.....
+00000d30: a90a 6060 600a 0a3e 20e2 9aa0 efb8 8f20  ..```..> ...... 
+00000d40: e6b3 a8e6 848f 20e6 ada4 e5a4 84e6 b2a1  ...... .........
+00000d50: e69c 89e4 bdbf e794 a820 5bf0 9f94 9720  ......... [.... 
+00000d60: e68f 92e4 bbb6 e591 bde4 bba4 e5a4 b45d  ...............]
+00000d70: 2868 7474 7073 3a2f 2f67 6974 6875 622e  (https://github.
+00000d80: 636f 6d2f 4c6a 7a64 2d50 524f 2f6e 6f6e  com/Ljzd-PRO/non
+00000d90: 6562 6f74 2d70 6c75 6769 6e2d 6d79 7374  ebot-plugin-myst
+00000da0: 6f6f 6c2f 7769 6b69 2f43 6f6e 6669 6775  ool/wiki/Configu
+00000db0: 7261 7469 6f6e 2d43 6f6e 6669 6723 636f  ration-Config#co
+00000dc0: 6d6d 616e 6473 7461 7274 290a 0a23 2320  mmandstart)..## 
+00000dd0: e585 b6e4 bb96 0a0a 2323 2320 5bf0 9f93  ........### [...
+00000de0: 83e6 ba90 e7a0 81e8 afb4 e698 8e5d 2868  .............](h
+00000df0: 7474 7073 3a2f 2f67 6974 6875 622e 636f  ttps://github.co
+00000e00: 6d2f 4c6a 7a64 2d50 524f 2f6e 6f6e 6562  m/Ljzd-PRO/noneb
+00000e10: 6f74 2d70 6c75 6769 6e2d 6d79 7374 6f6f  ot-plugin-mystoo
+00000e20: 6c2f 7769 6b69 2f53 6f75 7263 652d 5374  l/wiki/Source-St
+00000e30: 7275 6374 7572 6529 0a23 2323 20e9 8082  ructure).### ...
+00000e40: e985 8d20 5be7 bbaa e5b1 b1e7 9c9f e5af  ... [...........
+00000e50: bb42 6f74 5d28 6874 7470 733a 2f2f 6769  .Bot](https://gi
+00000e60: 7468 7562 2e63 6f6d 2f48 6962 694b 6965  thub.com/HibiKie
+00000e70: 722f 7a68 656e 7875 6e5f 626f 7429 20e7  r/zhenxun_bot) .
+00000e80: 9a84 e588 86e6 94af 0a2d 2068 7474 7073  .........- https
+00000e90: 3a2f 2f67 6974 6875 622e 636f 6d2f 4d57  ://github.com/MW
+00000ea0: 544a 432f 7a68 656e 7875 6e2d 706c 7567  TJC/zhenxun-plug
+00000eb0: 696e 2d6d 7973 746f 6f6c 0a2d 2068 7474  in-mystool.- htt
+00000ec0: 7073 3a2f 2f67 6974 6875 622e 636f 6d2f  ps://github.com/
+00000ed0: 6179 616b 6173 756b 692f 6e6f 6e65 626f  ayakasuki/nonebo
+00000ee0: 742d 706c 7567 696e 2d6d 7973 746f 6f6c  t-plugin-mystool
+00000ef0: 0a                                       .
```

### Comparing `nonebot_plugin_mystool-1.0.1/pyproject.toml` & `nonebot_plugin_mystool-1.1.0/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "nonebot-plugin-mystool"
-version = "v1.0.1"
+version = "v1.1.0"
 description = "NoneBot2插件|米游社工具-每日米游币任务、游戏签到、商品兑换、免抓包登录、原神树脂提醒"
 license = "MIT"
 authors = [
   "Ljzd-PRO <ljzd@office.ljzd-pro.ml>",
   "Everything0519 <598139245@qq.com>"
 ]
 readme = "README.md"
@@ -23,15 +23,15 @@
 ]
 
 [tool.poetry.dependencies]
 python = ">=3.9,<4.0"
 httpx = "^0.24.1"
 nonebot_plugin_apscheduler = ">=0.2.0"
 ntplib = "^0.4.0"
-Pillow = "^9.5.0"
+Pillow = ">=9.5,<11.0"
 requests = "^2.31.0"
 nonebot_adapter_onebot = "^2.2.3"
 tenacity = "^8.2.2"
 
 [tool.poetry.urls]
 "Bug Tracker" = "https://github.com/Ljzd-PRO/nonebot-plugin-mystool/issues"
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/__init__.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/__init__.py`

 * *Files 9% similar despite different names*

```diff
@@ -11,15 +11,16 @@
     usage="""
     \n🔐 {HEAD}登录 ➢ 登录绑定米游社账户\
     \n📦 {HEAD}地址 ➢ 设置收货地址ID\
     \n🗓️ {HEAD}签到 ➢ 手动进行游戏签到\
     \n📅 {HEAD}任务 ➢ 手动执行米游币任务\
     \n🛒 {HEAD}兑换 ➢ 米游币商品兑换相关\
     \n🎁 {HEAD}商品 ➢ 查看米游币商品信息(商品ID)\
-    \n📊 {HEAD}便笺 ➢ 查看原神实时便笺(原神树脂、洞天财瓮等)\
+    \n📊 {HEAD}原神便笺 ➢ 查看原神实时便笺(原神树脂、洞天财瓮等)\
+    \n📊 {HEAD}铁道便笺 ➢ 查看星穹铁道实时便笺(开拓力、每日实训等)\
     \n⚙️ {HEAD}设置 ➢ 设置是否开启通知、每日任务等相关选项\
     \n🔑 {HEAD}账号设置 ➢ 设置设备平台、是否开启每日计划任务、频道任务\
     \n🔔 {HEAD}通知设置 ➢ 设置是否开启每日米游币任务、游戏签到的结果通知\
     \n🖨️ {HEAD}导出Cookies ➢ 导出绑定的米游社账号的Cookies数据\
     \n📖 {HEAD}帮助 ➢ 查看帮助信息\
     \n🔍 {HEAD}帮助 <功能名> ➢ 查看目标功能详细说明\
     \n⚠️你的数据将经过机器人服务器，请确定你信任服务器所有者再使用。\
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/address.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/address.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 from nonebot.params import Arg, ArgPlainText, T_State
 
 from .plugin_data import PluginDataManager, write_plugin_data
 from .simple_api import get_address
 from .user_data import UserAccount
 from .utils import COMMAND_BEGIN
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
 
 address_matcher = on_command(_conf.preference.command_start + '地址', priority=4, block=True)
 
 address_matcher.name = '地址'
 address_matcher.usage = '跟随指引，获取地址ID，用于兑换米游币商品。在获取地址ID前，如果你还没有设置米游社收获地址，请前往官网或App设置'
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/data_model.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/data_model.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 """
 ### 米游社API的客户端调用所用的数据模型
 """
 import inspect
 import time
 from abc import abstractmethod
+from datetime import datetime
 from typing import Optional, Literal, NamedTuple, no_type_check, Union, Dict, Any, TypeVar, Tuple
 
 from pydantic import BaseModel
 
 
 class BaseModelWithSetter(BaseModel):
     """
@@ -374,14 +375,58 @@
             else:
                 return f"{self.transformer['recovery_time']['Day']} 天" \
                        f"{self.transformer['recovery_time']['Hour']} 小时 {self.transformer['recovery_time']['Minute']} 分钟"
         except KeyError:
             return None
 
 
+class StarRailBoard(BaseModel):
+    """
+    崩铁实时便笺数据 (从米游社内相关页面API的返回数据初始化)
+    """
+    current_stamina: int
+    """当前开拓力"""
+    max_stamina: int
+    """最大开拓力"""
+    stamina_recover_time: int
+    """剩余体力恢复时间"""
+    current_train_score: int
+    """当前每日实训值"""
+    max_train_score: int
+    """最大每日实训值"""
+    current_rogue_score: int
+    """当前模拟宇宙积分"""
+    max_rogue_score: int
+    """最大模拟宇宙积分"""
+    accepted_expedition_num: int
+    """已接受委托数量"""
+    total_expedition_num: int
+    """最大委托数量"""
+    has_signed: bool
+    """当天是否签到"""
+
+    @property
+    def stamina_recover_text(self):
+        """
+        剩余体力恢复文本
+        """
+        try:
+            if not self.stamina_recover_time:
+                return '体力未获得'
+            elif self.stamina_recover_time == 0:
+                return '体力已准备就绪'
+            else:
+                return datetime.fromtimestamp(int(time.time()) + self.stamina_recover_time)
+                # m, s = divmod(self.stamina_recover_time, 60)
+                # h, m = divmod(m, 60) 
+                # return f"{h} 小时 {m} 分钟 {s} 秒"
+        except KeyError:
+            return None
+
+
 class BaseApiStatus(BaseModel):
     """
     API返回结果基类
     """
     success = False
     """成功"""
     network_error = False
@@ -465,22 +510,38 @@
     """
     米游币任务 返回结果
     """
     failed_getting_post = False
     """获取文章失败"""
 
 
+class GetFpStatus(BaseApiStatus):
+    """
+    兑换操作 返回结果
+    """
+    invalid_arguments = False
+    """参数错误"""
+
+
 class GenshinBoardStatus(BaseApiStatus):
     """
     原神实时便笺 返回结果
     """
     no_genshin_account = False
     """用户没有任何原神账户"""
 
 
+class StarRailBoardStatus(BaseApiStatus):
+    """
+    星铁实时便笺 返回结果
+    """
+    no_starrail_account = False
+    """用户没有任何星铁账户"""
+
+
 GeetestResult = NamedTuple("GeetestResult", validate=str, seccode=str)
 """人机验证结果数据"""
 
 
 class GeetestResultV4(BaseModel):
     """
     GEETEST GT4 人机验证结果数据
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/exchange.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/exchange.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 """
 ### 米游社商品兑换前端以及计划任务相关
 """
 import asyncio
 import io
 import os
+import random
 import threading
 import time
 from datetime import datetime
 from multiprocessing import Manager
 from multiprocessing.pool import Pool
 from multiprocessing.synchronize import Lock
 from typing import List, Union, Callable, Any, Tuple, Optional, Dict
@@ -21,19 +22,20 @@
 from nonebot.matcher import Matcher
 from nonebot.params import ArgStr, ArgPlainText, T_State, CommandArg, Command
 from nonebot_plugin_apscheduler import scheduler
 
 from .data_model import Good, GameRecord, ExchangeStatus
 from .good_image import game_list_to_image
 from .plugin_data import PluginDataManager, write_plugin_data
-from .simple_api import get_game_record, get_good_detail, get_good_list, good_exchange_sync
+from .simple_api import get_game_record, get_good_detail, get_good_list, good_exchange_sync, get_device_fp, \
+    good_exchange
 from .user_data import UserAccount, ExchangePlan, ExchangeResult
-from .utils import NtpTime, COMMAND_BEGIN, logger, get_last_command_sep
+from .utils import COMMAND_BEGIN, logger, get_last_command_sep
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
 _driver = nonebot.get_driver()
 
 myb_exchange_plan = on_command(f"{_conf.preference.command_start}兑换",
                                aliases={(f"{_conf.preference.command_start}兑换", "+"),
                                         (f"{_conf.preference.command_start}兑换", "-")},
                                priority=5, block=True)
 myb_exchange_plan.name = "兑换"
@@ -224,14 +226,20 @@
         plan = ExchangePlan(good=good, address=account.address, game_record=record, account=account)
     else:
         plan = ExchangePlan(good=good, address=account.address, account=account)
     if plan in user.exchange_plans:
         await matcher.finish('⚠️您已经配置过该商品的兑换哦！')
     else:
         user.exchange_plans.add(plan)
+        if not plan.account.device_fp:
+            logger.info(f"账号 {plan.account.bbs_uid} 未设置 device_fp，正在获取...")
+            fp_status, plan.account.device_fp = await get_device_fp(plan.account.device_id_ios)
+            if not fp_status:
+                await matcher.send(
+                    '⚠️从服务器获取device_fp失败！兑换时将在本地生成device_fp。你也可以尝试重新添加兑换计划。')
         write_plugin_data()
 
     # 初始化兑换任务
     finished.setdefault(plan, [])
     for i in range(_conf.preference.exchange_thread_count):
         scheduler.add_job(
             good_exchange_sync,
@@ -376,44 +384,65 @@
                         user.exchange_plans.remove(plan)
                     except KeyError:
                         pass
                     else:
                         write_plugin_data()
 
 
+async def exchange_begin(plan: ExchangePlan):
+    """
+    到点后执行兑换
+
+    :param plan: 兑换计划
+    """
+    duration = 0
+    random_x, random_y = _conf.preference.exchange_latency
+    exchange_status, exchange_result = ExchangeStatus(), None
+
+    # 在兑换开始后的一段时间内，不断尝试兑换，直到成功（因为太早兑换可能被认定不在兑换时间）
+    while duration < _conf.preference.exchange_duration:
+        latency = random.uniform(random_x, random_y)
+        time.sleep(latency)
+        exchange_status, exchange_result = await good_exchange(plan)
+        if exchange_status and exchange_result.result:
+            break
+        duration += latency
+    return exchange_status, exchange_result
+
+
 @_driver.on_startup
 async def _():
     """
     启动机器人时自动初始化兑换任务
     """
     for user_id, user in _conf.users.items():
         plans = user.exchange_plans
         for plan in plans:
             good_detail_status, good = await get_good_detail(plan.good)
-            if good_detail_status.good_not_existed or good.time < NtpTime.time():
+            if good_detail_status.good_not_existed or good.time < time.time():
                 # 若商品不存在则删除
                 # 若重启时兑换超时则删除该兑换
                 user.exchange_plans.remove(plan)
                 write_plugin_data()
                 continue
             else:
                 finished.setdefault(plan, [])
                 for i in range(_conf.preference.exchange_thread_count):
                     scheduler.add_job(
-                        good_exchange_sync,
+                        exchange_begin,
                         "date",
                         id=f"exchange-plan-{hash(plan)}-{i}",
                         replace_existing=True,
                         args=(plan,),
                         run_date=datetime.fromtimestamp(good.time),
                         max_instances=_conf.preference.exchange_thread_count
                     )
 
 
-def image_process(game: str, lock: Lock):
+def image_process(game: str, lock: Lock = None):
     """
     生成并保存图片的进程函数
 
     :param game: 游戏名
     :param lock: 进程锁
     :return: 生成成功或无商品返回True，否则返回False
     """
@@ -452,17 +481,21 @@
             if name.startswith(date):
                 if is_auto:
                     return
             # 删除旧图片
             if name.endswith('.jpg'):
                 os.remove(os.path.join(root, name))
 
-    lock: Lock = Manager().Lock()
-    with Pool() as pool:
+    if _conf.good_list_image_config.MULTI_PROCESS:
+        lock: Lock = Manager().Lock()
+        with Pool() as pool:
+            for game in "bh3", "hk4e", "bh2", "hkrpg", "nxx", "bbs":
+                pool.apply_async(image_process,
+                                 args=(game, lock),
+                                 callback=callback)
+            pool.close()
+            pool.join()
+    else:
         for game in "bh3", "hk4e", "bh2", "hkrpg", "nxx", "bbs":
-            pool.apply_async(image_process,
-                             args=(game, lock),
-                             callback=callback)
-        pool.close()
-        pool.join()
+            image_process(game)
 
     logger.info(f"{_conf.preference.log_head}已完成所有分区的商品列表图片生成")
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/game_sign_api.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/game_sign_api.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 from .data_model import GameRecord, BaseApiStatus, Award, GameSignInfo, GeetestResult
 from .plugin_data import PluginDataManager
 from .simple_api import ApiResultHandler, HEADERS_API_TAKUMI_MOBILE, is_incorrect_return, device_login, device_save
 from .user_data import UserAccount
 from .utils import logger, generate_ds, \
     get_async_retry, get_validate
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
 
 
 class BaseGameSign:
     """
     游戏签到基类
     """
     NAME = ""
@@ -159,15 +159,15 @@
             headers["x-rpc-device_name"] = _conf.device_config.X_RPC_DEVICE_NAME_ANDROID
             headers["x-rpc-channel"] = _conf.device_config.X_RPC_CHANNEL_ANDROID
             headers["x-rpc-sys_version"] = _conf.device_config.X_RPC_SYS_VERSION_ANDROID
             headers["x-rpc-client_type"] = "2"
             headers.pop("x-rpc-platform")
             await device_login(self.account)
             await device_save(self.account)
-            headers["DS"] = generate_ds(platform="android")
+            headers["DS"] = generate_ds(data=content)
 
         challenge = ""
         """人机验证任务 challenge"""
         geetest_result = GeetestResult("", "")
         """人机验证结果"""
 
         try:
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/good_image.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/good_image.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 from PIL import Image, ImageDraw, ImageFont
 
 from .data_model import Good
 from .plugin_data import PluginDataManager, DATA_PATH
 from .simple_api import get_good_detail
 from .utils import (get_file, logger, get_async_retry)
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
 
 FONT_URL = os.path.join(
     _conf.preference.github_proxy,
     "https://github.com/adobe-fonts/source-han-sans/releases/download/2.004R/SourceHanSansHWSC.zip")
 TEMP_FONT_PATH = DATA_PATH / "temp" / "font.zip"
 FONT_SAVE_PATH = DATA_PATH / "SourceHanSansHWSC-Regular.otf"
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/help.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/help.py`

 * *Files 10% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 from nonebot.adapters.onebot.v11.message import Message
 from nonebot.matcher import Matcher
 from nonebot.params import Arg, CommandArg
 
 from .plugin_data import PluginDataManager
 from .utils import PLUGIN, COMMAND_BEGIN
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
 
 helper = on_command(_conf.preference.command_start + "help",
                     priority=1,
                     aliases={_conf.preference.command_start + "帮助"},
                     block=True)
 
 helper.name = '帮助'
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/login.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/login.py`

 * *Files 7% similar despite different names*

```diff
@@ -8,19 +8,19 @@
 from nonebot.adapters.onebot.v11 import PrivateMessageEvent, GroupMessageEvent, Message
 from nonebot.internal.matcher import Matcher
 from nonebot.internal.params import Arg
 from nonebot.params import ArgPlainText, T_State
 
 from .plugin_data import PluginDataManager, write_plugin_data
 from .simple_api import get_login_ticket_by_captcha, get_multi_token_by_login_ticket, get_stoken_v2_by_v1, \
-    get_ltoken_by_stoken, get_cookie_token_by_stoken
+    get_ltoken_by_stoken, get_cookie_token_by_stoken, get_device_fp
 from .user_data import UserAccount, UserData
 from .utils import logger, COMMAND_BEGIN
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
 
 get_cookie = on_command(_conf.preference.command_start + '登录', priority=4, block=True)
 get_cookie.name = '登录'
 get_cookie.usage = '跟随指引，通过电话获取短信方式绑定米游社账户，配置完成后会自动开启签到、米游币任务，后续可制定米游币自动兑换计划。'
 
 
 @get_cookie.handle()
@@ -76,14 +76,18 @@
             if not account or not account.cookies:
                 user.accounts.update({
                     cookies.bbs_uid: UserAccount(phone_number=phone_number, cookies=cookies)
                 })
                 account = user.accounts[cookies.bbs_uid]
             else:
                 account.cookies.update(cookies)
+            if not account.device_id_ios:
+                fp_status, account.device_fp = await get_device_fp(account.device_id_ios)
+                if fp_status:
+                    logger.info(f"用户 {cookies.bbs_uid} 成功获取 device_fp: {account.device_fp}")
             write_plugin_data()
 
             # 2. 通过 login_ticket 获取 stoken 和 ltoken
             if login_status or account:
                 login_status, cookies = await get_multi_token_by_login_ticket(account.cookies)
                 if login_status:
                     logger.info(f"用户 {phone_number} 成功获取 stoken: {cookies.stoken}")
@@ -108,15 +112,14 @@
                             login_status, cookies = await get_cookie_token_by_stoken(account.cookies,
                                                                                      account.device_id_ios)
                             if login_status:
                                 logger.info(f"用户 {phone_number} 成功获取 cookie_token: {cookies.cookie_token}")
                                 account.cookies.update(cookies)
                                 write_plugin_data()
 
-                                # TODO 2023/04/12 此处如果可以模拟App的登录操作，再标记为登录完成，更安全
                                 logger.info(f"{_conf.preference.log_head}米游社账户 {phone_number} 绑定成功")
                                 await get_cookie.finish(f"🎉米游社账户 {phone_number} 绑定成功")
 
         if not login_status:
             notice_text = "⚠️登录失败："
             if login_status.incorrect_captcha:
                 notice_text += "验证码错误！"
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/myb_missions_api.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/myb_missions_api.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,77 +11,78 @@
     MissionState
 from .plugin_data import PluginDataManager
 from .simple_api import ApiResultHandler, is_incorrect_return
 from .user_data import UserAccount
 from .utils import logger, generate_ds, \
     get_async_retry
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
+device_config = PluginDataManager.device_config
 
 URL_SIGN = "https://bbs-api.mihoyo.com/apihub/app/api/signIn"
 URL_GET_POST = "https://bbs-api.miyoushe.com/post/api/feeds/posts?fresh_action=1&gids={}&is_first_initialize=false" \
                "&last_id="
 URL_READ = "https://bbs-api.miyoushe.com/post/api/getPostFull?post_id={}"
 URL_LIKE = "https://bbs-api.miyoushe.com/apihub/sapi/upvotePost"
 URL_SHARE = "https://bbs-api.miyoushe.com/apihub/api/getShareConf?entity_id={}&entity_type=1"
 URL_MISSION = "https://api-takumi.mihoyo.com/apihub/wapi/getMissions?point_sn=myb"
 URL_MISSION_STATE = "https://api-takumi.mihoyo.com/apihub/wapi/getUserMissionsState?point_sn=myb"
 HEADERS_BASE = {
     "Host": "bbs-api.miyoushe.com",
     "Referer": "https://app.mihoyo.com",
-    'User-Agent': _conf.device_config.USER_AGENT_ANDROID_OTHER,
-    "x-rpc-app_version": _conf.device_config.X_RPC_APP_VERSION,
-    "x-rpc-channel": _conf.device_config.X_RPC_CHANNEL_ANDROID,
+    'User-Agent': device_config.USER_AGENT_ANDROID_OTHER,
+    "x-rpc-app_version": device_config.X_RPC_APP_VERSION,
+    "x-rpc-channel": device_config.X_RPC_CHANNEL_ANDROID,
     "x-rpc-client_type": "2",
     "x-rpc-device_id": None,
-    "x-rpc-device_model": _conf.device_config.X_RPC_DEVICE_MODEL_ANDROID,
-    "x-rpc-device_name": _conf.device_config.X_RPC_DEVICE_NAME_ANDROID,
-    "x-rpc-sys_version": _conf.device_config.X_RPC_SYS_VERSION_ANDROID,
+    "x-rpc-device_model": device_config.X_RPC_DEVICE_MODEL_ANDROID,
+    "x-rpc-device_name": device_config.X_RPC_DEVICE_NAME_ANDROID,
+    "x-rpc-sys_version": device_config.X_RPC_SYS_VERSION_ANDROID,
     "Accept-Encoding": "gzip",
     "Connection": "Keep-Alive",
     "DS": None
 }
 HEADERS_MISSION = {
     "Host": "api-takumi.mihoyo.com",
     "Origin": "https://webstatic.mihoyo.com",
     "Connection": "keep-alive",
     "Accept": "application/json, text/plain, */*",
-    "User-Agent": _conf.device_config.USER_AGENT_MOBILE,
+    "User-Agent": device_config.USER_AGENT_MOBILE,
     "Accept-Language": "zh-CN,zh-Hans;q=0.9",
     "Referer": "https://webstatic.mihoyo.com/",
     "Accept-Encoding": "gzip, deflate, br"
 }
 HEADERS_GET_POSTS = {
     "Host": "bbs-api.miyoushe.com",
     "Accept": "*/*",
     "x-rpc-client_type": "1",
     "x-rpc-device_id": None,
-    "x-rpc-channel": _conf.device_config.X_RPC_CHANNEL,
+    "x-rpc-channel": device_config.X_RPC_CHANNEL,
     "Accept-Language": "zh-CN,zh-Hans;q=0.9",
     "Accept-Encoding": "gzip, deflate, br",
-    "x-rpc-sys_version": _conf.device_config.X_RPC_SYS_VERSION,
+    "x-rpc-sys_version": device_config.X_RPC_SYS_VERSION,
     "Referer": "https://app.mihoyo.com",
-    "x-rpc-device_name": _conf.device_config.X_RPC_DEVICE_NAME_MOBILE,
-    "x-rpc-app_version": _conf.device_config.X_RPC_APP_VERSION,
-    "User-Agent": _conf.device_config.USER_AGENT_OTHER,
+    "x-rpc-device_name": device_config.X_RPC_DEVICE_NAME_MOBILE,
+    "x-rpc-app_version": device_config.X_RPC_APP_VERSION,
+    "User-Agent": device_config.USER_AGENT_OTHER,
     "Connection": "keep-alive"
 }
 
 # 旧的API
 HEADERS_OLD = {
     "Host": "bbs-api.mihoyo.com",
     "Referer": "https://app.mihoyo.com",
-    'User-Agent': _conf.device_config.USER_AGENT_ANDROID_OTHER,
+    'User-Agent': device_config.USER_AGENT_ANDROID_OTHER,
     "x-rpc-app_version": "2.36.1",
-    "x-rpc-channel": _conf.device_config.X_RPC_CHANNEL_ANDROID,
+    "x-rpc-channel": device_config.X_RPC_CHANNEL_ANDROID,
     "x-rpc-client_type": "2",
     "x-rpc-device_id": None,
-    "x-rpc-device_model": _conf.device_config.X_RPC_DEVICE_MODEL_ANDROID,
-    "x-rpc-device_name": _conf.device_config.X_RPC_DEVICE_NAME_ANDROID,
-    "x-rpc-sys_version": _conf.device_config.X_RPC_SYS_VERSION_ANDROID,
+    "x-rpc-device_model": device_config.X_RPC_DEVICE_MODEL_ANDROID,
+    "x-rpc-device_name": device_config.X_RPC_DEVICE_NAME_ANDROID,
+    "x-rpc-sys_version": device_config.X_RPC_SYS_VERSION_ANDROID,
     "Accept-Encoding": "gzip",
     "Connection": "Keep-Alive",
     "DS": None
 }
 
 
 class BaseMission:
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/plan.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/plan.py`

 * *Files 14% similar despite different names*

```diff
@@ -11,18 +11,18 @@
                                          PrivateMessageEvent, GroupMessageEvent)
 from nonebot_plugin_apscheduler import scheduler
 
 from .exchange import generate_image
 from .game_sign_api import BaseGameSign
 from .myb_missions_api import BaseMission, get_missions_state
 from .plugin_data import PluginDataManager, write_plugin_data
-from .simple_api import genshin_board, get_game_record
+from .simple_api import genshin_board, get_game_record, StarRail_board
 from .utils import get_file, logger, COMMAND_BEGIN
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
 
 manually_game_sign = on_command(_conf.preference.command_start + '签到', priority=5, block=True)
 manually_game_sign.name = '签到'
 manually_game_sign.usage = '手动进行游戏签到，查看本次签到奖励及本月签到天数'
 
 
 @manually_game_sign.handle()
@@ -52,16 +52,25 @@
     user = _conf.users.get(event.user_id)
     if not user or not user.accounts:
         await manually_game_sign.finish(f"⚠️你尚未绑定米游社账户，请先使用『{COMMAND_BEGIN}登录』进行登录")
     await manually_game_sign.send("⏳开始执行米游币任务...")
     await perform_bbs_sign(bot=bot, qq=event.user_id, is_auto=False, group_event=event)
 
 
-manually_resin_check = on_command(_conf.preference.command_start + '便笺', priority=5, block=True)
-manually_resin_check.name = '便笺'
+manually_resin_check = on_command(
+    _conf.preference.command_start + '原神便笺',
+    aliases={
+        _conf.preference.command_start + '便笺',
+        _conf.preference.command_start + '便签',
+        _conf.preference.command_start + '原神便签',
+    },
+    priority=5,
+    block=True
+)
+manually_resin_check.name = '原神便笺'
 manually_resin_check.usage = '手动查看原神实时便笺，即原神树脂、洞天财瓮等信息'
 has_checked = {}
 for user in _conf.users.values():
     for account in user.accounts.values():
         if account.enable_resin:
             has_checked[account.bbs_uid] = has_checked.get(account.bbs_uid,
                                                            {"resin": False, "coin": False, "transformer": False})
@@ -75,14 +84,45 @@
     bot = get_bot(str(event.self_id))
     user = _conf.users.get(event.user_id)
     if not user or not user.accounts:
         await manually_game_sign.finish(f"⚠️你尚未绑定米游社账户，请先使用『{COMMAND_BEGIN}登录』进行登录")
     await resin_check(bot=bot, qq=event.user_id, is_auto=False, group_event=event)
 
 
+manually_resin_check_sr = on_command(
+    _conf.preference.command_start + '星穹铁道便笺',
+    aliases={
+        _conf.preference.command_start + '铁道便笺',
+        _conf.preference.command_start + '铁道便签',
+    },
+    priority=5,
+    block=True
+)
+manually_resin_check_sr.name = '星穹铁道便笺'
+manually_resin_check_sr.usage = '手动查看星穹铁道实时便笺，即开拓力、每日实训、每周模拟宇宙积分等信息'
+for user in _conf.users.values():
+    for account in user.accounts.values():
+        if account.enable_resin:
+            has_checked[account.bbs_uid] = has_checked.get(account.bbs_uid,
+                                                           {"stamina": False, "train_score": False,
+                                                            "rogue_score": False})
+
+
+@manually_resin_check_sr.handle()
+async def _(event: Union[GroupMessageEvent, PrivateMessageEvent]):
+    """
+    手动查看星穹铁道便笺（sr）
+    """
+    bot = get_bot(str(event.self_id))
+    user = _conf.users.get(event.user_id)
+    if not user or not user.accounts:
+        await manually_game_sign.finish(f"⚠️你尚未绑定米游社账户，请先使用『{COMMAND_BEGIN}登录』进行登录")
+    await resin_check_sr(bot=bot, qq=event.user_id, is_auto=False, group_event=event)
+
+
 async def perform_game_sign(bot: Bot, qq: int, is_auto: bool,
                             group_event: Union[GroupMessageEvent, PrivateMessageEvent, None] = None):
     """
     执行游戏签到函数，并发送给用户签到消息。
 
     :param bot: Bot实例
     :param qq: 用户QQ号
@@ -399,27 +439,142 @@
                         else:
                             has_checked[account.bbs_uid]['transformer'] = True
                             msg += '❕您的参量质变仪已准备就绪\n\n'
                     else:
                         has_checked[account.bbs_uid]['transformer'] = False
                         return
                 else:
-                    has_checked[account.bbs_uid]['transformer'] = False
+                    has_checked[account.bbs_uid]['transformer'] = True
             msg += "❖实时便笺❖" \
                    f"\n⏳树脂数量：{board.current_resin} / 160" \
                    f"\n🕰️探索派遣：{board.current_expedition_num} / {board.max_expedition_num}" \
                    f"\n📅每日委托：{4 - board.finished_task_num} 个任务未完成" \
                    f"\n💰洞天财瓮：{board.current_home_coin} / {board.max_home_coin}" \
                    f"\n🎰参量质变仪：{board.transformer_text if board.transformer else 'N/A'}"
             if group_event:
                 await bot.send(event=group_event, at_sender=True, message=msg)
             else:
                 await bot.send_private_msg(user_id=qq, message=msg)
 
 
+async def resin_check_sr(bot: Bot, qq: int, is_auto: bool,
+                         group_event: Union[GroupMessageEvent, PrivateMessageEvent, None] = None):
+    """
+    查看星铁实时便笺函数，并发送给用户任务执行消息。
+
+    :param bot: Bot实例
+    :param qq: 用户QQ号
+    :param is_auto: True为自动检查，False为用户手动调用该功能
+    :param group_event: 若为群消息触发，则为群消息事件，否则为None
+    """
+    if isinstance(group_event, PrivateMessageEvent):
+        group_event = None
+    global has_checked
+    user = _conf.users[qq]
+    for account in user.accounts.values():
+        if account.enable_resin:
+            has_checked[account.bbs_uid] = has_checked.get(account.bbs_uid,
+                                                           {"stamina": False, "train_score": False,
+                                                            "rogue_score": False})
+        if (account.enable_resin and is_auto) or not is_auto:
+            starrail_board_status, board = await StarRail_board(account)
+            logger.info(starrail_board_status)
+            if not starrail_board_status:
+                if starrail_board_status.login_expired:
+                    if not is_auto:
+                        if group_event:
+                            await bot.send(event=group_event, at_sender=True,
+                                           message=f'⚠️账户 {account.bbs_uid} 登录失效，请重新登录')
+                        else:
+                            await bot.send_private_msg(user_id=qq,
+                                                       message=f'⚠️账户 {account.bbs_uid} 登录失效，请重新登录')
+                if starrail_board_status.no_starrail_account:
+                    if not is_auto:
+                        if group_event:
+                            await bot.send(event=group_event, at_sender=True,
+                                           message=f'⚠️账户 {account.bbs_uid} 没有绑定任何星铁账户，请绑定后再重试')
+                        else:
+                            await bot.send_private_msg(user_id=qq,
+                                                       message=f'⚠️账户 {account.bbs_uid} 没有绑定任何星铁账户，请绑定后再重试')
+                        account.enable_resin = False
+                        write_plugin_data()
+                        continue
+                if not is_auto:
+                    if group_event:
+                        await bot.send(event=group_event, at_sender=True,
+                                       message=f'⚠️账户 {account.bbs_uid} 获取实时便笺请求失败，你可以手动前往App查看')
+                    else:
+                        await bot.send_private_msg(user_id=qq,
+                                                   message=f'⚠️账户 {account.bbs_uid} 获取实时便笺请求失败，你可以手动前往App查看')
+                continue
+            if starrail_board_status.need_verify:
+                if group_event:
+                    await bot.send(event=group_event, at_sender=True,
+                                   message='⚠️遇到验证码正在尝试绕过')
+                else:
+                    await bot.send_private_msg(user_id=qq,
+                                               message='⚠️遇到验证码正在尝试绕过')
+            msg = ''
+            # 手动查询体力时，无需判断是否溢出
+            if not is_auto:
+                pass
+            else:
+                # 体力溢出提醒
+                if board.current_stamina == 180:
+                    # 防止重复提醒
+                    if has_checked[account.bbs_uid]['stamina']:
+                        return
+                    else:
+                        has_checked[account.bbs_uid]['stamina'] = True
+                        msg += '❕您的开拓力已经满啦\n'
+                else:
+                    has_checked[account.bbs_uid]['stamina'] = False
+                # 每日实训状态提醒
+                if board.current_train_score == board.max_train_score:
+                    # 防止重复提醒
+                    if has_checked[account.bbs_uid]['train_score']:
+                        return
+                    else:
+                        has_checked[account.bbs_uid]['train_score'] = True
+                        msg += '❕您的每日实训已完成\n'
+                else:
+                    has_checked[account.bbs_uid]['train_score'] = False
+                # 每周模拟宇宙积分提醒
+                if board.current_rogue_score == board.max_rogue_score:
+                    # 防止重复提醒
+                    if has_checked[account.bbs_uid]['rogue_score']:
+                        return
+                    else:
+                        has_checked[account.bbs_uid]['rogue_score'] = True
+                        msg += '❕您的模拟宇宙积分已经打满了\n\n'
+                else:
+                    has_checked[account.bbs_uid]['rogue_score'] = False
+                    return
+            msg += "❖星穹铁道实时便笺❖" \
+                   f"\n⏳开拓力数量：{board.current_stamina} / 180" \
+                   f"\n⏱开拓力将在{board.stamina_recover_text}回满" \
+                   f"\n📒每日实训：{board.current_train_score} / {board.max_train_score}" \
+                   f"\n📅每日委托：{board.accepted_expedition_num} / 4" \
+                   f"\n🌌模拟宇宙：{board.current_rogue_score} / {board.max_rogue_score}"
+            if not is_auto:
+                if group_event:
+                    await bot.send(event=group_event, at_sender=True, message=msg)
+                else:
+                    await bot.send_private_msg(user_id=qq, message=msg)
+            else:
+                if board.current_stamina >= account.user_stamina_threshold:
+
+                    if group_event:
+                        await bot.send(event=group_event, at_sender=True, message=msg)
+                    else:
+                        await bot.send_private_msg(user_id=qq, message=msg)
+                else:
+                    logger.info(f"崩铁实时便笺：账户 {account.bbs_uid} 开拓力:{board.current_stamina},未满足推送条件")
+
+
 @scheduler.scheduled_job("cron", hour='0', minute='0', id="daily_goodImg_update")
 def daily_update():
     """
     每日图片生成函数
     """
     logger.info(f"{_conf.preference.log_head}后台开始生成每日商品图片")
     threading.Thread(target=generate_image).start()
@@ -449,7 +604,8 @@
 async def auto_resin_check():
     """
     自动查看实时便笺
     """
     bot = get_bot()
     for qq in _conf.users:
         await resin_check(bot=bot, qq=qq, is_auto=True)
+        await resin_check_sr(bot=bot, qq=qq, is_auto=True)
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/plugin_data.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/plugin_data.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,42 +1,46 @@
 """
 ### 插件数据相关
 """
+import json
 import os
 from datetime import time, timedelta
 from json import JSONDecodeError
 from pathlib import Path
 from typing import Union, Optional, Tuple, Any, Dict, TYPE_CHECKING, AbstractSet, \
     Mapping
 
 from loguru import logger
-from pydantic import BaseModel, ValidationError, BaseSettings, validator
+from pydantic import BaseModel, ValidationError, BaseSettings, validator, Extra
 
 from .user_data import UserData, UserAccount
 
-VERSION = "v1.0.1"
+VERSION = "v1.1.0"
 """程序当前版本"""
 
 ROOT_PATH = Path(__name__).parent.absolute()
 '''NoneBot2 机器人根目录'''
 
 DATA_PATH = ROOT_PATH / "data" / "nonebot-plugin-mystool"
 '''插件数据保存目录'''
 
 PLUGIN_DATA_PATH = DATA_PATH / "plugin_data.json"
 """插件数据文件默认路径"""
 
+DELETED_USERS_PATH = DATA_PATH / "deletedUsers"
+"""已删除用户数据文件默认备份目录"""
+
 if TYPE_CHECKING:
     IntStr = Union[int, str]
     DictStrAny = Dict[str, Any]
     AbstractSetIntStr = AbstractSet[IntStr]
     MappingIntStrAny = Mapping[IntStr, Any]
 
 
-class Preference(BaseSettings):
+class Preference(BaseSettings, extra=Extra.ignore):
     """
     偏好设置
     """
     github_proxy: Optional[str] = "https://ghproxy.com/"
     """GitHub加速代理 最终会拼接在原GitHub链接前面"""
     enable_connection_test: bool = True
     """是否开启连接测试"""
@@ -44,24 +48,22 @@
     """连接测试间隔（单位：秒）"""
     timeout: float = 10
     """网络请求超时时间（单位：秒）"""
     max_retry_times: Optional[int] = 3
     """最大网络请求重试次数"""
     retry_interval: float = 2
     """网络请求重试间隔（单位：秒）（除兑换请求外）"""
-    enable_ntp_sync: Optional[bool] = True
-    """是否开启NTP时间同步（将调整实际发出兑换请求的时间，而不是修改系统时间）"""
-    ntp_server: Optional[str] = "ntp.aliyun.com"
-    """NTP服务器地址"""
     timezone: Optional[str] = "Asia/Shanghai"
     """兑换时所用的时区"""
     exchange_thread_count: int = 2
     """兑换线程数"""
-    exchange_latency: Tuple[float, float] = (0, 0.35)
-    """兑换时间延迟随机范围（单位：秒）（防止因为发出请求的时间过于精准而被服务器认定为非人工操作）"""
+    exchange_latency: Tuple[float, float] = (0, 0.5)
+    """同一线程下，每个兑换请求之间的间隔时间"""
+    exchange_duration: float = 5
+    """兑换持续时间随机范围（单位：秒）"""
     enable_log_output: bool = True
     """是否保存日志"""
     log_head: str = ""
     '''日志开头字符串(只有把插件放进plugins目录手动加载时才需要设置)'''
     log_path: Optional[Path] = DATA_PATH / "mystool.log"
     """日志保存路径"""
     log_rotation: Union[str, int, time, timedelta] = "1 week"
@@ -82,33 +84,35 @@
     '''任务操作冷却时间(如米游币任务)'''
     plan_time: str = "00:30"
     '''每日自动签到和米游社任务的定时任务执行时间，格式为HH:MM'''
     resin_interval: int = 60
     '''每次检查原神便笺间隔，单位为分钟'''
     geetest_url: Optional[str]
     '''极验Geetest人机验证打码接口URL'''
+    geetest_json: Optional[Dict[str, Any]] = {
+        "gt": "{gt}",
+        "challenge": "{challenge}"
+    }
+    '''极验Geetest人机验证打码API发送的JSON数据 `{gt}`, `{challenge}` 为占位符'''
+    override_device_and_salt: bool = False
+    """是否读取插件数据文件中的 device_config 设备配置 和 salt_config 配置而不是默认配置（一般情况不建议开启）"""
 
     @validator("log_path", allow_reuse=True)
     def _(cls, v: Optional[Path]):
         absolute_path = v.absolute()
         if not os.path.exists(absolute_path) or not os.path.isfile(absolute_path):
             absolute_parent = absolute_path.parent
             try:
                 os.makedirs(absolute_parent, exist_ok=True)
             except PermissionError:
                 logger.warning(f"程序没有创建日志目录 {absolute_parent} 的权限")
         elif not os.access(absolute_path, os.W_OK):
             logger.warning(f"程序没有写入日志文件 {absolute_path} 的权限")
         return v
 
-    class Config:
-        # TODO: env_prefix = "..."  # 环境变量前缀
-        #   使用 nonebot2 的 环境变量规范
-        ...
-
 
 class GoodListImageConfig(BaseModel):
     """
     商品列表输出图片设置
     """
     ICON_SIZE: Tuple[int, int] = (600, 600)
     '''商品预览图在最终结果图中的大小'''
@@ -127,19 +131,21 @@
     开源字体 Source Han Sans 思源黑体
     https://github.com/adobe-fonts/source-han-sans
     '''
     FONT_SIZE: int = 50
     '''字体大小'''
     SAVE_PATH: Path = DATA_PATH
     '''商品列表图片缓存目录'''
+    MULTI_PROCESS: bool = True
+    '''是否使用多进程生成图片（如果生成图片时崩溃，可尝试关闭此选项）'''
 
 
 class SaltConfig(BaseSettings):
     """
-    生成Headers - DS所用salt值
+    生成Headers - DS所用salt值，非必要请勿修改
     """
     SALT_IOS: str = "ulInCDohgEs557j0VsPDYnQaaz6KJcv5"
     '''生成Headers iOS DS所需的salt'''
     SALT_ANDROID: str = "n0KjuIrKgLHh08LWSCYP0WXlVXaYvV64"
     '''生成Headers Android DS所需的salt'''
     SALT_DATA: str = "t0qEgfub6cvueAPgR5m9aQWWVciEer7v"
     '''Android 设备传入content生成 DS 所需的 salt'''
@@ -150,23 +156,23 @@
     class Config(Preference.Config):
         pass
 
 
 class DeviceConfig(BaseSettings):
     """
     设备信息
-    DS算法与设备信息有关联，非必要请勿修改
+    Headers所用的各种数据，非必要请勿修改
     """
-    USER_AGENT_MOBILE: str = "Mozilla/5.0 (iPhone; CPU iPhone OS 15_4 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) miHoYoBBS/2.42.1"
+    USER_AGENT_MOBILE: str = "Mozilla/5.0 (iPhone; CPU iPhone OS 15_4 like Mac OS X) AppleWebKit/605.1.15 (KHTML, like Gecko) miHoYoBBS/2.54.1"
     '''移动端 User-Agent(Mozilla UA)'''
     USER_AGENT_PC: str = "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/16.0 Safari/605.1.15"
     '''桌面端 User-Agent(Mozilla UA)'''
     USER_AGENT_OTHER: str = "Hyperion/275 CFNetwork/1402.0.8 Darwin/22.2.0"
     '''获取用户 ActionTicket 时Headers所用的 User-Agent'''
-    USER_AGENT_ANDROID: str = "Mozilla/5.0 (Linux; Android 11; MI 8 SE Build/RQ3A.211001.001; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/104.0.5112.97 Mobile Safari/537.36 miHoYoBBS/2.36.1"
+    USER_AGENT_ANDROID: str = "Mozilla/5.0 (Linux; Android 11; MI 8 SE Build/RQ3A.211001.001; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/104.0.5112.97 Mobile Safari/537.36 miHoYoBBS/2.54.1"
     '''安卓端 User-Agent(Mozilla UA)'''
     USER_AGENT_ANDROID_OTHER: str = "okhttp/4.9.3"
     '''安卓端 User-Agent(专用于米游币任务等)'''
     USER_AGENT_WIDGET: str = "WidgetExtension/231 CFNetwork/1390 Darwin/22.0.0"
     '''iOS 小组件 User-Agent(原神实时便笺)'''
 
     X_RPC_DEVICE_MODEL_MOBILE: str = "iPhone10,2"
@@ -189,15 +195,15 @@
     '''安卓端 x-rpc-sys_version'''
 
     X_RPC_CHANNEL: str = "appstore"
     '''Headers所用的 x-rpc-channel'''
     X_RPC_CHANNEL_ANDROID: str = "miyousheluodi"
     '''安卓端 x-rpc-channel'''
 
-    X_RPC_APP_VERSION: str = "2.28.1"
+    X_RPC_APP_VERSION: str = "2.54.1"
     '''Headers所用的 x-rpc-app_version'''
     X_RPC_PLATFORM: str = "ios"
     '''Headers所用的 x-rpc-platform'''
     UA: str = "\".Not/A)Brand\";v=\"99\", \"Microsoft Edge\";v=\"103\", \"Chromium\";v=\"103\""
     '''Headers所用的 sec-ch-ua'''
     UA_PLATFORM: str = "\"macOS\""
     '''Headers所用的 sec-ch-ua-platform'''
@@ -221,38 +227,58 @@
     '''所有用户数据'''
 
     class Config:
         json_encoders = UserAccount.Config.json_encoders
 
 
 class PluginDataManager:
-    plugin_data_obj = PluginData()
+    plugin_data = PluginData()
+    device_config = DeviceConfig()
     """加载出的插件数据对象"""
 
     @classmethod
     def load_plugin_data(cls):
         """
         加载插件数据文件
         """
         if os.path.exists(PLUGIN_DATA_PATH) and os.path.isfile(PLUGIN_DATA_PATH):
             try:
-                new_model = PluginData.parse_file(PLUGIN_DATA_PATH)
-                for attr in new_model.__fields__:
-                    PluginDataManager.plugin_data_obj.__setattr__(attr, new_model.__getattribute__(attr))
+                with open(PLUGIN_DATA_PATH, "r") as f:
+                    device_config_dict = json.load(f)["device_config"]
+                device_config_from_file = DeviceConfig.parse_obj(device_config_dict)
+                for attr in device_config_from_file.__fields__:
+                    cls.device_config.__setattr__(attr, device_config_from_file.__getattribute__(attr))
+
+                plugin_data_from_file = PluginData.parse_file(PLUGIN_DATA_PATH)
+                for attr in plugin_data_from_file.__fields__:
+                    cls.plugin_data.__setattr__(attr, plugin_data_from_file.__getattribute__(attr))
             except (ValidationError, JSONDecodeError):
                 logger.exception(f"读取插件数据文件失败，请检查插件数据文件 {PLUGIN_DATA_PATH} 格式是否正确")
                 raise
             except:
                 logger.exception(
                     f"读取插件数据文件失败，请检查插件数据文件 {PLUGIN_DATA_PATH} 是否存在且有权限读取和写入")
                 raise
+            else:
+                if not cls.plugin_data.preference.override_device_and_salt:
+                    default_device_config = DeviceConfig()
+                    default_salt_config = SaltConfig()
+                    if cls.plugin_data.device_config != default_device_config \
+                            or cls.plugin_data.salt_config != default_salt_config:
+                        cls.plugin_data.device_config = default_device_config
+                        cls.plugin_data.salt_config = default_salt_config
+                        logger.warning("检测到设备信息配置 device_config 或 salt_config 使用了非默认值，"
+                                       "如果你修改过这些配置，需要设置 preference.override_device_and_salt 为 True 以覆盖默认值并生效。"
+                                       "如果继续，将可能保存默认值到插件数据文件。")
+                else:
+                    logger.info("已开启覆写 device_config 和 salt_config，将读取插件数据文件中的配置以覆写默认配置")
         else:
-            plugin_data = PluginData()
+            plugin_data_from_file = PluginData()
             try:
-                str_data = plugin_data.json(indent=4)
+                str_data = plugin_data_from_file.json(indent=4)
                 with open(PLUGIN_DATA_PATH, "w", encoding="utf-8") as f:
                     f.write(str_data)
             except (AttributeError, TypeError, ValueError, PermissionError):
                 logger.exception(f"创建插件数据文件失败，请检查是否有权限读取和写入 {PLUGIN_DATA_PATH}")
                 raise
             logger.info(f"插件数据文件 {PLUGIN_DATA_PATH} 不存在，已创建默认插件数据文件。")
 
@@ -263,15 +289,15 @@
 def write_plugin_data(data: PluginData = None):
     """
     写入插件数据文件
 
     :param data: 配置对象
     """
     if data is None:
-        data = PluginDataManager.plugin_data_obj
+        data = PluginDataManager.plugin_data
     try:
         str_data = data.json(indent=4)
     except (AttributeError, TypeError, ValueError):
         logger.exception("数据对象序列化失败，可能是数据类型错误")
         return False
     with open(PLUGIN_DATA_PATH, "w", encoding="utf-8") as f:
         f.write(str_data)
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/setting.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/setting.py`

 * *Files 18% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 from nonebot.params import Arg, ArgPlainText, T_State
 
 from .myb_missions_api import BaseMission
 from .plugin_data import PluginDataManager, write_plugin_data
 from .user_data import UserAccount
 from .utils import COMMAND_BEGIN
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
 
 setting = on_command(_conf.preference.command_start + '设置', priority=4, block=True)
 setting.name = "设置"
 setting.usage = '如需配置是否开启每日任务、设备平台、频道任务等相关选项，请使用『{HEAD}账号设置』命令。' \
                 '\n如需设置米游币任务和游戏签到后是否进行QQ通知，请使用『{HEAD}通知设置』命令。'
 
 
@@ -77,17 +77,19 @@
     platform_show = "iOS" if account.platform == "ios" else "安卓"
     user_setting += f"\n3️⃣ 设备平台：{platform_show}"
 
     # 筛选出用户数据中的missionGame对应的游戏全称
     user_setting += "\n\n4️⃣ 执行米游币任务的频道：" + \
                     "\n- " + "、".join(map(lambda x: f"『{x.NAME}』", account.mission_games))
     user_setting += f"\n\n5️⃣ 原神树脂恢复提醒：{'开' if account.enable_resin else '关'}"
-    user_setting += "\n6️⃣⚠️删除账户数据"
+    user_setting += f"\n6️⃣更改崩铁便笺开拓力提醒阈值 \
+                            当前提醒阈值：{account.user_stamina_threshold}"
+    user_setting += "\n7️⃣⚠️删除账户数据"
 
-    await account_setting.send(user_setting + '\n\n您要更改哪一项呢？请发送 1 / 2 / 3 / 4 / 5 / 6'
+    await account_setting.send(user_setting + '\n\n您要更改哪一项呢？请发送 1 / 2 / 3 / 4 / 5 / 6 / 7'
                                               '\n🚪发送“退出”即可退出')
 
 
 @account_setting.got('arg')
 async def _(event: Union[PrivateMessageEvent, GroupMessageEvent], state: T_State, arg=ArgPlainText('arg')):
     """
     根据所选更改相应账户的相应设置
@@ -119,49 +121,73 @@
         await account_setting.send(
             "请发送你想要执行米游币任务的频道："
             "\n❕多个频道请用空格分隔，如 “原神 崩坏3 大别野”"
             "\n\n可选的频道："
             f"\n- {games_show}"
             "\n\n🚪发送“退出”即可退出"
         )
+        state["setting_item"] = "mission_games"
     elif arg == '5':
         account.enable_resin = not account.enable_resin
         write_plugin_data()
-        await account_setting.finish(f"📅原神树脂恢复提醒已 {'✅开启' if account.enable_resin else '❌关闭'}")
+        await account_setting.finish(f"📅原神、星穹铁道便笺提醒已 {'✅开启' if account.enable_resin else '❌关闭'}")
     elif arg == '6':
+        await account_setting.send(
+            "请输入想要所需阈值数字："
+            "支持输入[0,180]"
+            "\n\n🚪发送“退出”即可退出"
+        )
+        state["setting_item"] = "threshold"
+    elif arg == '7':
         state["prepare_to_delete"] = True
         await account_setting.reject(f"⚠️确认删除账号 {account.phone_number} ？发送 \"确认删除\" 以确定。")
     elif arg == '确认删除' and state["prepare_to_delete"]:
         user_account.pop(account.bbs_uid)
         write_plugin_data()
         await account_setting.finish(f"已删除账号 {account.phone_number} 的数据")
     else:
         await account_setting.reject("⚠️您的输入有误，请重新输入")
 
 
-@account_setting.got('missionGame')
-async def _(_: Union[PrivateMessageEvent, GroupMessageEvent], state: T_State, arg=ArgPlainText('missionGame')):
+@account_setting.got('setting_arg')
+async def _(_: Union[PrivateMessageEvent, GroupMessageEvent], state: T_State, arg=ArgPlainText('setting_arg')):
     arg = arg.strip()
     if arg == '退出':
         await account_setting.finish('🚪已成功退出')
     account: UserAccount = state['account']
-    games_input = arg.split()
-    mission_games = set()
-    for game in games_input:
-        game_filter = filter(lambda x: x.NAME == game, BaseMission.AVAILABLE_GAMES)
-        game_obj = next(game_filter, None)
-        if game_obj is None:
-            await account_setting.reject("⚠️您的输入有误，请重新输入")
+
+    if state["setting_item"] == "threshold":
+        try:
+            stamina_threshold = int(arg)
+        except ValueError:
+            await account_setting.reject("⚠️请输入有效的数字。")
         else:
-            mission_games.add(game_obj)
+            if 0 <= stamina_threshold <= 180:
+                # 输入有效的数字范围，将 stamina_threshold 赋值为输入的整数
+                account.user_stamina_threshold = stamina_threshold
+                write_plugin_data()
+                await account_setting.finish(f"更改崩铁便笺开拓力提醒阈值成功，当前提醒阈值：{stamina_threshold}")
+            else:
+                await account_setting.reject("⚠️输入的数字范围应在 0 到 180 之间。")
+
+    elif state["setting_item"] == "mission_games":
+        games_input = arg.split()
+        mission_games = set()
+        for game in games_input:
+            game_filter = filter(lambda x: x.NAME == game, BaseMission.AVAILABLE_GAMES)
+            game_obj = next(game_filter, None)
+            if game_obj is None:
+                await account_setting.reject("⚠️您的输入有误，请重新输入")
+            else:
+                mission_games.add(game_obj)
 
-    account.mission_games = mission_games
-    write_plugin_data()
-    arg = arg.replace(" ", "、")
-    await account_setting.finish(f"💬执行米游币任务的频道已更改为『{arg}』")
+        account.mission_games = mission_games
+        write_plugin_data()
+        arg = arg.replace(" ", "、")
+        await account_setting.finish(f"💬执行米游币任务的频道已更改为『{arg}』")
 
 
 global_setting = on_command(_conf.preference.command_start + '通知设置', priority=5, block=True)
 global_setting.name = "通知设置"
 global_setting.usage = "设置每日签到后是否进行QQ通知"
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/simple_api.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/simple_api.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,27 +1,30 @@
 """
 ### 米游社一些简单API相关
 """
+import time
 from typing import List, Optional, Tuple, Dict, Any, Union, Type
 from urllib.parse import urlencode
 
 import httpx
 import tenacity
 from pydantic import ValidationError, BaseModel
 from requests.utils import dict_from_cookiejar
 
 from .data_model import GameRecord, GameInfo, Good, Address, BaseApiStatus, MmtData, GeetestResult, \
     GetCookieStatus, \
-    CreateMobileCaptchaStatus, GetGoodDetailStatus, ExchangeStatus, GeetestResultV4, GenshinBoard, GenshinBoardStatus
+    CreateMobileCaptchaStatus, GetGoodDetailStatus, ExchangeStatus, GeetestResultV4, GenshinBoard, GenshinBoardStatus, \
+    GetFpStatus, StarRailBoardStatus, StarRailBoard
 from .plugin_data import PluginDataManager
 from .user_data import UserAccount, BBSCookies, ExchangePlan, ExchangeResult
 from .utils import generate_device_id, logger, generate_ds, \
-    NtpTime, get_async_retry
+    get_async_retry, generate_seed_id, generate_fp_locally
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
+device_config = PluginDataManager.device_config
 
 URL_LOGIN_TICKET_BY_CAPTCHA = "https://webapi.account.mihoyo.com/Api/login_by_mobilecaptcha"
 URL_LOGIN_TICKET_BY_PASSWORD = "https://webapi.account.mihoyo.com/Api/login_by_password"
 URL_MULTI_TOKEN_BY_LOGIN_TICKET = "https://api-takumi.mihoyo.com/auth/api/getMultiTokenByLoginTicket?login_ticket={0}&token_types=3&uid={1}"
 URL_COOKIE_TOKEN_BY_CAPTCHA = "https://api-takumi.mihoyo.com/account/auth/api/webLoginByMobile"
 URL_COOKIE_TOKEN_BY_STOKEN = "https://passport-api.mihoyo.com/account/auth/api/getCookieAccountInfoBySToken"
 URL_LTOKEN_BY_STOKEN = "https://passport-api.mihoyo.com/account/auth/api/getLTokenBySToken"
@@ -31,38 +34,41 @@
 URL_GAME_LIST = "https://bbs-api.mihoyo.com/apihub/api/getGameList"
 URL_MYB = "https://api-takumi.mihoyo.com/common/homutreasure/v1/web/user/point?app_id=1&point_sn=myb"
 URL_DEVICE_LOGIN = "https://bbs-api.mihoyo.com/apihub/api/deviceLogin"
 URL_DEVICE_SAVE = "https://bbs-api.mihoyo.com/apihub/api/saveDevice"
 URL_GOOD_LIST = "https://api-takumi.mihoyo.com/mall/v1/web/goods/list?app_id=1&point_sn=myb&page_size=20&page={" \
                 "page}&game={game} "
 URL_CHECK_GOOD = "https://api-takumi.mihoyo.com/mall/v1/web/goods/detail?app_id=1&point_sn=myb&goods_id={}"
-URL_EXCHANGE = "https://api-takumi.mihoyo.com/mall/v1/web/goods/exchange"
+URL_EXCHANGE = "https://api-takumi.miyoushe.com/mall/v1/web/goods/exchange"
 URL_ADDRESS = "https://api-takumi.mihoyo.com/account/address/list?t={}"
 URL_REGISTRABLE = "https://webapi.account.mihoyo.com/Api/is_mobile_registrable?mobile={mobile}&t={t}"
 URL_CREATE_MMT = "https://webapi.account.mihoyo.com/Api/create_mmt?scene_type=1&now={now}&reason=user.mihoyo.com%2523%252Flogin%252Fcaptcha&action_type=login_by_mobile_captcha&t={t}"
 URL_CREATE_MOBILE_CAPTCHA = "https://webapi.account.mihoyo.com/Api/create_mobile_captcha"
 URL_GET_USER_INFO = "https://bbs-api.miyoushe.com/user/api/getUserFullInfo?uid={uid}"
+URL_GET_DEVICE_FP = "https://public-data-api.mihoyo.com/device-fp/api/getFp"
 URL_GENSHIN_STATUS_WIDGET = "https://api-takumi-record.mihoyo.com/game_record/app/card/api/getWidgetData?game_id=2"
 URL_GENSHEN_STATUS_BBS = "https://api-takumi-record.mihoyo.com/game_record/app/genshin/api/dailyNote"
 URL_GENSHEN_STATUS_WIDGET = "https://api-takumi-record.mihoyo.com/game_record/genshin/aapi/widget/v2"
+URL_STARRAIL_STATUS_BBS = "https://api-takumi-record.mihoyo.com/game_record/app/hkrpg/api/note"
+URL_STARRAIL_STATUS_WIDGET = "https://api-takumi-record.mihoyo.com/game_record/app/hkrpg/aapi/widget"
 
 HEADERS_WEBAPI = {
     "Host": "webapi.account.mihoyo.com",
     "Connection": "keep-alive",
-    "sec-ch-ua": _conf.device_config.UA,
+    "sec-ch-ua": device_config.UA,
     "DNT": "1",
-    "x-rpc-device_model": _conf.device_config.X_RPC_DEVICE_MODEL_PC,
+    "x-rpc-device_model": device_config.X_RPC_DEVICE_MODEL_PC,
     "sec-ch-ua-mobile": "?0",
-    "User-Agent": _conf.device_config.USER_AGENT_PC,
+    "User-Agent": device_config.USER_AGENT_PC,
     "x-rpc-device_id": None,
     "Accept": "application/json, text/plain, */*",
-    "x-rpc-device_name": _conf.device_config.X_RPC_DEVICE_NAME_PC,
+    "x-rpc-device_name": device_config.X_RPC_DEVICE_NAME_PC,
     "Content-Type": "application/x-www-form-urlencoded; charset=UTF-8",
     "x-rpc-client_type": "4",
-    "sec-ch-ua-platform": _conf.device_config.UA_PLATFORM,
+    "sec-ch-ua-platform": device_config.UA_PLATFORM,
     "Origin": "https://user.mihoyo.com",
     "Sec-Fetch-Site": "same-site",
     "Sec-Fetch-Mode": "cors",
     "Sec-Fetch-Dest": "empty",
     "Referer": "https://user.mihoyo.com/",
     "Accept-Encoding": "gzip, deflate, br",
     "Accept-Language": "zh-CN,zh;q=0.9,en;q=0.8,en-GB;q=0.7,en-US;q=0.6"
@@ -74,122 +80,122 @@
     # "x-rpc-device_fp": "",
     "x-rpc-client_type": "1",
     "x-rpc-device_id": None,
     # "x-rpc-app_id": "bll8iq97cem8",
     "Accept-Language": "zh-CN,zh-Hans;q=0.9",
     "x-rpc-game_biz": "bbs_cn",
     "Accept-Encoding": "gzip, deflate, br",
-    "x-rpc-device_model": _conf.device_config.X_RPC_DEVICE_MODEL_MOBILE,
-    "User-Agent": _conf.device_config.USER_AGENT_OTHER,
-    "x-rpc-device_name": _conf.device_config.X_RPC_DEVICE_NAME_MOBILE,
-    "x-rpc-app_version": _conf.device_config.X_RPC_APP_VERSION,
+    "x-rpc-device_model": device_config.X_RPC_DEVICE_MODEL_MOBILE,
+    "User-Agent": device_config.USER_AGENT_OTHER,
+    "x-rpc-device_name": device_config.X_RPC_DEVICE_NAME_MOBILE,
+    "x-rpc-app_version": device_config.X_RPC_APP_VERSION,
     # 抓包时 "2.47.1"
 
     "x-rpc-sdk_version": "1.6.1",
     "Connection": "keep-alive",
-    "x-rpc-sys_version": _conf.device_config.X_RPC_SYS_VERSION
+    "x-rpc-sys_version": device_config.X_RPC_SYS_VERSION
 }
 HEADERS_API_TAKUMI_PC = {
     "Host": "api-takumi.mihoyo.com",
     "Content-Type": "application/json;charset=utf-8",
     "Origin": "https://bbs.mihoyo.com",
     "Accept-Encoding": "gzip, deflate, br",
     "Connection": "keep-alive",
     "Accept": "application/json, text/plain, */*",
-    "User-Agent": _conf.device_config.USER_AGENT_PC,
+    "User-Agent": device_config.USER_AGENT_PC,
     "Referer": "https://bbs.mihoyo.com/",
     "Accept-Language": "zh-CN,zh-Hans;q=0.9"
 }
 HEADERS_API_TAKUMI_MOBILE = {
     "Host": "api-takumi.mihoyo.com",
-    "x-rpc-device_model": _conf.device_config.X_RPC_DEVICE_MODEL_MOBILE,
-    "User-Agent": _conf.device_config.USER_AGENT_MOBILE,
+    "x-rpc-device_model": device_config.X_RPC_DEVICE_MODEL_MOBILE,
+    "User-Agent": device_config.USER_AGENT_MOBILE,
     "Referer": "https://webstatic.mihoyo.com/",
-    "x-rpc-device_name": _conf.device_config.X_RPC_DEVICE_NAME_MOBILE,
+    "x-rpc-device_name": device_config.X_RPC_DEVICE_NAME_MOBILE,
     "Origin": "https://webstatic.mihoyo.com",
     "Connection": "keep-alive",
-    "x-rpc-channel": _conf.device_config.X_RPC_CHANNEL,
-    "x-rpc-app_version": _conf.device_config.X_RPC_APP_VERSION,
+    "x-rpc-channel": device_config.X_RPC_CHANNEL,
+    "x-rpc-app_version": device_config.X_RPC_APP_VERSION,
     "Accept-Language": "zh-CN,zh-Hans;q=0.9",
     "x-rpc-device_id": None,
     "x-rpc-client_type": "5",
     "Accept": "application/json, text/plain, */*",
     "Content-Type": "application/json;charset=utf-8",
     "Accept-Encoding": "gzip, deflate, br",
-    "x-rpc-sys_version": _conf.device_config.X_RPC_SYS_VERSION,
-    "x-rpc-platform": _conf.device_config.X_RPC_PLATFORM,
+    "x-rpc-sys_version": device_config.X_RPC_SYS_VERSION,
+    "x-rpc-platform": device_config.X_RPC_PLATFORM,
     "DS": None
 }
 HEADERS_GAME_RECORD = {
     "Host": "api-takumi-record.mihoyo.com",
     "Origin": "https://webstatic.mihoyo.com",
     "Connection": "keep-alive",
     "Accept": "application/json, text/plain, */*",
-    "User-Agent": _conf.device_config.USER_AGENT_MOBILE,
+    "User-Agent": device_config.USER_AGENT_MOBILE,
     "Accept-Language": "zh-CN,zh-Hans;q=0.9",
     "Referer": "https://webstatic.mihoyo.com/",
     "Accept-Encoding": "gzip, deflate, br"
 }
 HEADERS_GAME_LIST = {
     "Host": "bbs-api.mihoyo.com",
     "DS": None,
     "Accept": "*/*",
     "x-rpc-device_id": generate_device_id(),
     "x-rpc-client_type": "1",
-    "x-rpc-channel": _conf.device_config.X_RPC_CHANNEL,
+    "x-rpc-channel": device_config.X_RPC_CHANNEL,
     "Accept-Language": "zh-CN,zh-Hans;q=0.9",
     "Accept-Encoding": "gzip, deflate, br",
-    "x-rpc-sys_version": _conf.device_config.X_RPC_SYS_VERSION,
+    "x-rpc-sys_version": device_config.X_RPC_SYS_VERSION,
     "Referer": "https://app.mihoyo.com",
-    "x-rpc-device_name": _conf.device_config.X_RPC_DEVICE_NAME_MOBILE,
-    "x-rpc-app_version": _conf.device_config.X_RPC_APP_VERSION,
-    "User-Agent": _conf.device_config.USER_AGENT_OTHER,
+    "x-rpc-device_name": device_config.X_RPC_DEVICE_NAME_MOBILE,
+    "x-rpc-app_version": device_config.X_RPC_APP_VERSION,
+    "User-Agent": device_config.USER_AGENT_OTHER,
     "Connection": "keep-alive",
-    "x-rpc-device_model": _conf.device_config.X_RPC_DEVICE_MODEL_MOBILE
+    "x-rpc-device_model": device_config.X_RPC_DEVICE_MODEL_MOBILE
 }
 HEADERS_MYB = {
     "Host": "api-takumi.mihoyo.com",
     "Origin": "https://webstatic.mihoyo.com",
     "Connection": "keep-alive",
     "Accept": "application/json, text/plain, */*",
-    "User-Agent": _conf.device_config.USER_AGENT_MOBILE,
+    "User-Agent": device_config.USER_AGENT_MOBILE,
     "Accept-Language": "zh-CN,zh-Hans;q=0.9",
     "Referer": "https://webstatic.mihoyo.com/",
     "Accept-Encoding": "gzip, deflate, br"
 }
 HEADERS_DEVICE = {
     "DS": None,
     "x-rpc-client_type": "2",
-    "x-rpc-app_version": _conf.device_config.X_RPC_APP_VERSION,
-    "x-rpc-sys_version": _conf.device_config.X_RPC_SYS_VERSION_ANDROID,
-    "x-rpc-channel": _conf.device_config.X_RPC_CHANNEL_ANDROID,
+    "x-rpc-app_version": device_config.X_RPC_APP_VERSION,
+    "x-rpc-sys_version": device_config.X_RPC_SYS_VERSION_ANDROID,
+    "x-rpc-channel": device_config.X_RPC_CHANNEL_ANDROID,
     "x-rpc-device_id": None,
-    "x-rpc-device_name": _conf.device_config.X_RPC_DEVICE_NAME_ANDROID,
-    "x-rpc-device_model": _conf.device_config.X_RPC_DEVICE_MODEL_ANDROID,
+    "x-rpc-device_name": device_config.X_RPC_DEVICE_NAME_ANDROID,
+    "x-rpc-device_model": device_config.X_RPC_DEVICE_MODEL_ANDROID,
     "Referer": "https://app.mihoyo.com",
     "Content-Type": "application/json; charset=UTF-8",
     "Host": "bbs-api.mihoyo.com",
     "Connection": "Keep-Alive",
     "Accept-Encoding": "gzip",
-    "User-Agent": _conf.device_config.USER_AGENT_ANDROID_OTHER
+    "User-Agent": device_config.USER_AGENT_ANDROID_OTHER
 }
 HEADERS_GOOD_LIST = {
     "Host":
         "api-takumi.mihoyo.com",
     "Accept":
         "application/json, text/plain, */*",
     "Origin":
         "https://user.mihoyo.com",
     "Connection":
         "keep-alive",
     "x-rpc-device_id": generate_device_id(),
     "x-rpc-client_type":
         "5",
     "User-Agent":
-        _conf.device_config.USER_AGENT_MOBILE,
+        device_config.USER_AGENT_MOBILE,
     "Referer":
         "https://user.mihoyo.com/",
     "Accept-Language":
         "zh-CN,zh-Hans;q=0.9",
     "Accept-Encoding":
         "gzip, deflate, br"
 }
@@ -199,74 +205,103 @@
     "Accept-Encoding":
         "gzip, deflate, br",
     "Accept-Language":
         "zh-CN,zh-Hans;q=0.9",
     "Connection":
         "keep-alive",
     "Content-Type":
-        "application/json;charset=utf-8",
+        "application/json",
     "Host":
-        "api-takumi.mihoyo.com",
+        "api-takumi.miyoushe.com",
+    "Origin":
+        "https://webstatic.miyoushe.com",
+    "Referer":
+        "https://webstatic.miyoushe.com/",
     "User-Agent":
-        _conf.device_config.USER_AGENT_MOBILE,
+        device_config.USER_AGENT_MOBILE,
     "x-rpc-app_version":
-        _conf.device_config.X_RPC_APP_VERSION,
+        device_config.X_RPC_APP_VERSION,
     "x-rpc-channel":
         "appstore",
     "x-rpc-client_type":
         "1",
+    "x-rpc-verify_key":
+        "bll8iq97cem8",
+    "x-rpc-device_fp": None,
     "x-rpc-device_id": None,
     "x-rpc-device_model":
-        _conf.device_config.X_RPC_DEVICE_MODEL_MOBILE,
+        device_config.X_RPC_DEVICE_MODEL_MOBILE,
     "x-rpc-device_name":
-        _conf.device_config.X_RPC_DEVICE_NAME_MOBILE,
+        device_config.X_RPC_DEVICE_NAME_MOBILE,
     "x-rpc-sys_version":
-        _conf.device_config.X_RPC_SYS_VERSION
+        device_config.X_RPC_SYS_VERSION
 }
 HEADERS_ADDRESS = {
     "Host": "api-takumi.mihoyo.com",
     "Accept": "application/json, text/plain, */*",
     "Origin": "https://user.mihoyo.com",
     "Connection": "keep-alive",
     "x-rpc-device_id": None,
     "x-rpc-client_type": "5",
-    "User-Agent": _conf.device_config.USER_AGENT_MOBILE,
+    "User-Agent": device_config.USER_AGENT_MOBILE,
     "Referer": "https://user.mihoyo.com/",
     "Accept-Language": "zh-CN,zh-Hans;q=0.9",
     "Accept-Encoding": "gzip, deflate, br"
 }
 HEADERS_GENSHIN_STATUS_WIDGET = {
     "Host": "api-takumi-record.mihoyo.com",
     "DS": None,
     "Accept": "*/*",
     "x-rpc-device_id": None,
     "x-rpc-client_type": "1",
     "x-rpc-channel": "appstore",
     "Accept-Language": "zh-CN,zh-Hans;q=0.9",
     "Accept-Encoding": "gzip, deflate, br",
-    "x-rpc-device_model": _conf.device_config.X_RPC_DEVICE_MODEL_MOBILE,
+    "x-rpc-device_model": device_config.X_RPC_DEVICE_MODEL_MOBILE,
     "Referer": "https://app.mihoyo.com",
-    "x-rpc-device_name": _conf.device_config.X_RPC_DEVICE_NAME_MOBILE,
-    "x-rpc-app_version": _conf.device_config.X_RPC_APP_VERSION,
-    "User-Agent": _conf.device_config.USER_AGENT_WIDGET,
+    "x-rpc-device_name": device_config.X_RPC_DEVICE_NAME_MOBILE,
+    "x-rpc-app_version": device_config.X_RPC_APP_VERSION,
+    "User-Agent": device_config.USER_AGENT_WIDGET,
     "Connection": "keep-alive",
-    "x-rpc-sys_version": _conf.device_config.X_RPC_SYS_VERSION
+    "x-rpc-sys_version": device_config.X_RPC_SYS_VERSION
 }
 HEADERS_GENSHIN_STATUS_BBS = {
     "DS": None,
     "x-rpc-device_id": None,
     "Accept": "application/json,text/plain,*/*",
     "Origin": "https://webstatic.mihoyo.com",
-    "User-agent": _conf.device_config.USER_AGENT_ANDROID,
+    "User-agent": device_config.USER_AGENT_ANDROID,
     "Referer": "https://webstatic.mihoyo.com/",
-    "x-rpc-app_version": _conf.device_config.X_RPC_APP_VERSION,
+    "x-rpc-app_version": device_config.X_RPC_APP_VERSION,
     "X-Requested-With": "com.mihoyo.hyperion",
     "x-rpc-client_type": "5"
 }
 
+HEADERS_STARRAIL_STATUS_WIDGET = {
+    "Accept": "*/*",
+    "Accept-Encoding": "gzip, deflate, br",
+    "Accept-Language": "zh-CN,zh-Hans;q=0.9",
+    "User-Agent": device_config.USER_AGENT_WIDGET,
+
+    # "DS": None,
+    "Referer": "https://app.mihoyo.com",
+    "x-rpc-app_version": device_config.X_RPC_APP_VERSION,
+    "x-rpc-channel": device_config.X_RPC_CHANNEL,
+    "x-rpc-client_type": "2",
+    "x-rpc-page": '',
+    "x-rpc-device_fp": '',
+    "x-rpc-device_id": '',
+    "x-rpc-device_model": device_config.X_RPC_DEVICE_MODEL_MOBILE,
+    "x-rpc-device_name": device_config.X_RPC_DEVICE_NAME_MOBILE,
+    "x-rpc-sys_version": device_config.X_RPC_SYS_VERSION,
+
+    "Connection": "keep-alive",
+    "Host": "api-takumi-record.mihoyo.com"
+}
+
 IncorrectReturn = (KeyError, TypeError, AttributeError, IndexError, ValidationError)
 """米游社API返回数据无效会触发的异常组合"""
 
 
 def is_incorrect_return(exception: Exception, *addition_exceptions: Type[Exception]) -> bool:
     """
     判断是否是米游社API返回数据无效的异常
@@ -438,17 +473,17 @@
     """
     设备登录(deviceLogin)(适用于安卓设备)
 
     :param account: 用户账户数据
     :param retry: 是否允许重试
     """
     data = {
-        "app_version": _conf.device_config.X_RPC_APP_VERSION,
+        "app_version": device_config.X_RPC_APP_VERSION,
         "device_id": account.device_id_android,
-        "device_name": _conf.device_config.X_RPC_DEVICE_NAME_ANDROID,
+        "device_name": device_config.X_RPC_DEVICE_NAME_ANDROID,
         "os_version": "30",
         "platform": "Android",
         "registration_id": "1a0018970a5c00e814d"
     }
     headers = HEADERS_DEVICE.copy()
     headers["x-rpc-device_id"] = account.device_id_android
     try:
@@ -483,17 +518,17 @@
     """
     设备保存(saveDevice)(适用于安卓设备)
 
     :param account: 用户账户数据
     :param retry: 是否允许重试
     """
     data = {
-        "app_version": _conf.device_config.X_RPC_APP_VERSION,
+        "app_version": device_config.X_RPC_APP_VERSION,
         "device_id": account.device_id_android,
-        "device_name": _conf.device_config.X_RPC_DEVICE_NAME_ANDROID,
+        "device_name": device_config.X_RPC_DEVICE_NAME_ANDROID,
         "os_version": "30",
         "platform": "Android",
         "registration_id": "1a0018970a5c00e814d"
     }
     headers = HEADERS_DEVICE.copy()
     headers["x-rpc-device_id"] = account.device_id_android
     try:
@@ -632,15 +667,15 @@
     headers = HEADERS_ADDRESS.copy()
     headers["x-rpc-device_id"] = account.device_id_ios
     try:
         async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.get(URL_ADDRESS.format(
-                        round(NtpTime.time() * 1000)), headers=headers,
+                        round(time.time() * 1000)), headers=headers,
                         cookies=account.cookies.dict(v2_stoken=True, cookie_type=True),
                         timeout=_conf.preference.timeout)
                     api_result = ApiResultHandler(res.json())
                     if api_result.login_expired:
                         logger.info(
                             f"获取地址数据 - 用户 {account.bbs_uid} 登录失效")
                         logger.debug(f"网络请求返回: {res.text}")
@@ -671,15 +706,15 @@
     device_id = generate_device_id()
     headers["x-rpc-device_id"] = device_id
 
     async def request():
         """
         发送请求的闭包函数
         """
-        time_now = round(NtpTime.time() * 1000)
+        time_now = round(time.time() * 1000)
         # await client.options(URL_REGISTRABLE.format(mobile=phone_number, t=time_now),
         #                      headers=headers, timeout=conf.preference.timeout)
         return await client.get(URL_REGISTRABLE.format(mobile=phone_number, t=time_now),
                                 headers=headers, timeout=_conf.preference.timeout)
 
     try:
         async for attempt in get_async_retry(retry):
@@ -723,15 +758,15 @@
     if use_v4:
         headers.setdefault("x-rpc-source", "accountWebsite")
 
     async def request():
         """
         发送请求的闭包函数
         """
-        time_now = round(NtpTime.time() * 1000)
+        time_now = round(time.time() * 1000)
         # await client.options(URL_CREATE_MMT.format(now=time_now, t=time_now),
         #                      headers=headers, timeout=conf.preference.timeout)
         return await client.get(URL_CREATE_MMT.format(now=time_now, t=time_now),
                                 headers=headers, timeout=_conf.preference.timeout)
 
     try:
         async for attempt in get_async_retry(retry):
@@ -779,25 +814,25 @@
     if use_v4 and isinstance(geetest_result, GeetestResultV4):
         geetest_v4_data = geetest_result.dict(skip_defaults=True)
         content = {
             "action_type": "login",
             "mmt_key": mmt_data.mmt_key,
             "geetest_v4_data": str(geetest_v4_data).replace("'", '"'),
             "mobile": str(phone_number),
-            "t": str(round(NtpTime.time() * 1000))
+            "t": str(round(time.time() * 1000))
         }
     else:
         content = {
             "action_type": "login",
             "mmt_key": mmt_data.mmt_key,
             "geetest_challenge": mmt_data.challenge,
             "geetest_validate": geetest_result.validate,
             "geetest_seccode": geetest_result.seccode,
             "mobile": phone_number,
-            "t": round(NtpTime.time() * 1000)
+            "t": round(time.time() * 1000)
         }
 
     async def request():
         """
         发送请求的闭包函数
         """
         return await client.post(URL_CREATE_MOBILE_CAPTCHA,
@@ -851,15 +886,15 @@
 
     headers = HEADERS_WEBAPI.copy()
     headers["x-rpc-device_id"] = generate_device_id()
     params = {
         "mobile": phone_number,
         "mobile_captcha": captcha,
         "source": "user.mihoyo.com",
-        "t": round(NtpTime.time() * 1000),
+        "t": round(time.time() * 1000),
     }
     encoded_params = urlencode(params)
 
     async def request():
         """
         发送请求的闭包函数
         """
@@ -1012,15 +1047,15 @@
         "password": password,
         "is_crypto": False,
         "mmt_key": mmt_data.mmt_key,
         "geetest_challenge": mmt_data.challenge,
         "geetest_validate": geetest_result.validate,
         "geetest_seccode": geetest_result.seccode,
         "source": "user.mihoyo.com",
-        "t": round(NtpTime.time() * 1000)
+        "t": round(time.time() * 1000)
     }
     encoded_params = urlencode(params)
     try:
         async for attempt in get_async_retry(retry):
             with attempt:
                 async with httpx.AsyncClient() as client:
                     res = await client.post(
@@ -1194,123 +1229,187 @@
             logger.debug(f"网络请求返回: {res.text}")
             return GetCookieStatus(incorrect_return=True), None
         else:
             logger.exception("通过 stoken 获取 ltoken: 网络请求失败")
             return GetCookieStatus(network_error=True), None
 
 
+async def get_device_fp(device_id: str, retry: bool = True) -> Tuple[GetFpStatus, Optional[str]]:
+    """
+    获取 x-rpc-device_fp
+
+    :param device_id: x-rpc-device_id 的值
+    :param retry: 是否允许重试
+
+    >>> import asyncio
+    >>> coroutine = get_device_fp(generate_device_id())
+    >>> assert asyncio.new_event_loop().run_until_complete(coroutine)[0].success is True
+    """
+    content = {
+        "seed_id": generate_seed_id(),
+        "device_id": device_id.lower(),
+        "platform": "5",
+        "seed_time": str(int(time.time() * 1000)),
+        "ext_fields": "{\"userAgent\":\"Mozilla\/5.0 (iPhone; CPU iPhone OS 16_2 like Mac OS X) AppleWebKit\/605.1.15 "
+                      f"(KHTML, like Gecko) miHoYoBBS\/{device_config.X_RPC_APP_VERSION}\",\"browserScreenSize"
+                      "\":243750,\"maxTouchPoints\":5,"
+                      "\"isTouchSupported\":true,\"browserLanguage\":\"zh-CN\",\"browserPlat\":\"iPhone\","
+                      "\"browserTimeZone\":\"Asia\/Shanghai\",\"webGlRender\":\"Apple GPU\",\"webGlVendor\":\"Apple "
+                      "Inc.\",\"numOfPlugins\":0,\"listOfPlugins\":\"unknown\",\"screenRatio\":3,"
+                      "\"deviceMemory\":\"unknown\",\"hardwareConcurrency\":\"4\",\"cpuClass\":\"unknown\","
+                      "\"ifNotTrack\":\"unknown\",\"ifAdBlock\":0,\"hasLiedResolution\":1,\"hasLiedOs\":0,"
+                      "\"hasLiedBrowser\":0}",
+        "app_name": "account_cn",
+        "device_fp": generate_fp_locally()
+    }
+    try:
+        async for attempt in get_async_retry(retry):
+            with attempt:
+                async with httpx.AsyncClient() as client:
+                    res = await client.post(
+                        URL_GET_DEVICE_FP,
+                        json=content,
+                        timeout=_conf.preference.timeout
+                    )
+                api_result = ApiResultHandler(res.json())
+                if api_result.data["code"] == 403 or api_result.data["msg"] == "传入的参数有误":
+                    logger.error("传入的参数有误")
+                    return GetFpStatus(invalid_arguments=True), None
+                elif api_result.success:
+                    device_fp = api_result.data["device_fp"]
+                    if not device_fp:
+                        logger.error("获取 x-rpc-device_fp: 服务器返回的 device_fp 为空")
+                        return GetFpStatus(incorrect_return=True), None
+                    return GetFpStatus(success=True), device_fp
+
+    except tenacity.RetryError as e:
+        if is_incorrect_return(e):
+            logger.exception("获取 x-rpc-device_fp: 服务器没有正确返回")
+            logger.debug(f"网络请求返回: {res.text}")
+            return GetFpStatus(incorrect_return=True), None
+        else:
+            logger.exception("获取 x-rpc-device_fp: 网络请求失败")
+            return GetFpStatus(network_error=True), None
+
+
 async def good_exchange(plan: ExchangePlan) -> Tuple[ExchangeStatus, Optional[ExchangeResult]]:
     """
     执行米游币商品兑换
 
     :param plan: 兑换计划
     """
     headers = HEADERS_EXCHANGE
     headers["x-rpc-device_id"] = plan.account.device_id_ios
+    headers["x-rpc-device_fp"] = plan.account.device_fp or generate_fp_locally()
     content = {
         "app_id": 1,
         "point_sn": "myb",
         "goods_id": plan.good.goods_id,
-        "exchange_num": 1,
+        "exchange_num": 1
     }
     if plan.address is not None:
         content.setdefault("address_id", plan.address.id)
     if plan.game_record is not None:
         content.setdefault("uid", plan.game_record.game_role_id)
         # 例: cn_gf01
         content.setdefault("region", plan.game_record.region)
         # 例: hk4e_cn
         content.setdefault("game_biz", plan.good.game_biz)
+    start_time = 0
     try:
+        start_time = time.time()
         async with httpx.AsyncClient() as client:
             res = await client.post(
                 URL_EXCHANGE, headers=headers, json=content,
-                cookies=plan.account.cookies.dict(v2_stoken=True, cookie_type=True),
+                cookies=plan.account.cookies.dict(cookie_type=True),
                 timeout=_conf.preference.timeout)
         api_result = ApiResultHandler(res.json())
         if api_result.login_expired:
             logger.info(
-                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 登录失效")
+                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 登录失效 - 请求发送时间: {start_time}")
             logger.debug(f"网络请求返回: {res.text}")
             return ExchangeStatus(login_expired=True), None
         if api_result.success:
             logger.info(
-                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 兑换成功！可以自行确认。")
+                f"米游币商品兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 兑换成功！可以自行确认 - 请求发送时间: {start_time}")
             logger.debug(f"网络请求返回: {res.text}")
             return ExchangeStatus(success=True), ExchangeResult(result=True, return_data=res.json(), plan=plan)
         else:
             logger.info(
-                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 兑换失败，可以自行确认。")
+                f"米游币商品兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 兑换失败，可以自行确认 - 请求发送时间: {start_time}")
             logger.debug(f"网络请求返回: {res.text}")
             return ExchangeStatus(success=True), ExchangeResult(result=False, return_data=res.json(), plan=plan)
     except Exception as e:
         if is_incorrect_return(e):
             logger.error(
-                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 服务器没有正确返回")
+                f"米游币商品兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 服务器没有正确返回 - 请求发送时间: {start_time}")
             logger.debug(f"网络请求返回: {res.text}")
             return ExchangeStatus(incorrect_return=True), None
         else:
             logger.exception(
-                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 请求失败")
+                f"米游币商品兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 请求失败 - 请求发送时间: {start_time}")
             return ExchangeStatus(network_error=True), None
 
 
 def good_exchange_sync(plan: ExchangePlan) -> Tuple[ExchangeStatus, Optional[ExchangeResult]]:
     """
     执行米游币商品兑换
 
     :param plan: 兑换计划
     """
     headers = HEADERS_EXCHANGE
     headers["x-rpc-device_id"] = plan.account.device_id_ios
+    headers["x-rpc-device_fp"] = plan.account.device_fp or generate_fp_locally()
     content = {
         "app_id": 1,
         "point_sn": "myb",
         "goods_id": plan.good.goods_id,
-        "exchange_num": 1,
+        "exchange_num": 1
     }
     if plan.address is not None:
         content.setdefault("address_id", plan.address.id)
     if plan.game_record is not None:
         content.setdefault("uid", plan.game_record.game_role_id)
         # 例: cn_gf01
         content.setdefault("region", plan.game_record.region)
         # 例: hk4e_cn
         content.setdefault("game_biz", plan.good.game_biz)
+    start_time = 0
     try:
+        start_time = time.time()
         with httpx.Client() as client:
             res = client.post(
                 URL_EXCHANGE, headers=headers, json=content,
-                cookies=plan.account.cookies.dict(v2_stoken=True, cookie_type=True),
+                cookies=plan.account.cookies.dict(cookie_type=True),
                 timeout=_conf.preference.timeout)
         api_result = ApiResultHandler(res.json())
         if api_result.login_expired:
             logger.info(
-                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 登录失效")
+                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 登录失效 - 请求发送时间: {start_time}")
             logger.debug(f"网络请求返回: {res.text}")
             return ExchangeStatus(login_expired=True), None
         if api_result.success:
             logger.info(
-                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 兑换成功！可以自行确认。")
+                f"米游币商品兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 兑换成功！可以自行确认 - 请求发送时间: {start_time}")
             logger.debug(f"网络请求返回: {res.text}")
             return ExchangeStatus(success=True), ExchangeResult(result=True, return_data=res.json(), plan=plan)
         else:
             logger.info(
-                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 兑换失败，可以自行确认。")
+                f"米游币商品兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 兑换失败，可以自行确认 - 请求发送时间: {start_time}")
             logger.debug(f"网络请求返回: {res.text}")
             return ExchangeStatus(success=True), ExchangeResult(result=False, return_data=res.json(), plan=plan)
     except Exception as e:
         if is_incorrect_return(e):
             logger.error(
-                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 服务器没有正确返回")
+                f"米游币商品兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 服务器没有正确返回 - 请求发送时间: {start_time}")
             logger.debug(f"网络请求返回: {res.text}")
             return ExchangeStatus(incorrect_return=True), None
         else:
             logger.exception(
-                f"米游币商品兑换 - 执行兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 请求失败")
+                f"米游币商品兑换: 用户 {plan.account.bbs_uid} 商品 {plan.good.goods_id} 请求失败 - 请求发送时间: {start_time}")
             return ExchangeStatus(network_error=True), None
 
 
 async def genshin_board(account: UserAccount) -> Tuple[
     Union[BaseApiStatus, GenshinBoardStatus], Optional[GenshinBoard]]:
     """
     获取原神实时便笺
@@ -1381,7 +1480,76 @@
                     logger.debug(f"网络请求返回: {res.text}")
                     return GenshinBoardStatus(incorrect_return=True), None
                 else:
                     logger.exception(f"原神实时便笺: 请求失败")
                     return GenshinBoardStatus(network_error=True), None
     if flag:
         return GenshinBoardStatus(no_genshin_account=True), None
+
+
+async def StarRail_board(account: UserAccount) -> Tuple[
+    Union[BaseApiStatus, StarRailBoardStatus], Optional[StarRailBoard]]:
+    """
+    获取崩铁实时便笺
+
+    :param account: 用户账户数据
+    """
+    game_record_status, records = await get_game_record(account)
+    logger.info(f"genshin_board game_record_status : {game_record_status}")
+    logger.info(f"genshin_board records : {records}")
+    if not game_record_status:
+        return game_record_status, None
+    game_list_status, game_list = await get_game_list()
+    if not game_list_status:
+        return game_list_status, None
+    game_filter = filter(lambda x: x.en_name == 'sr', game_list)
+    game_info = next(game_filter, None)
+    if not game_info:
+        return StarRailBoardStatus(no_starrail_account=True), None
+    else:
+        game_id = game_info.id
+    flag = True
+    for record in records:
+        if record.game_id == game_id:
+            try:
+                flag = False
+                headers = HEADERS_STARRAIL_STATUS_WIDGET.copy()
+
+                url = f"{URL_STARRAIL_STATUS_WIDGET}"
+                async for attempt in get_async_retry(False):
+                    with attempt:
+                        headers["DS"] = generate_ds(data={})
+                        async with httpx.AsyncClient() as client:
+
+                            cookies = account.cookies.dict(v2_stoken=True, cookie_type=True)
+                            logger.info(f"StarRail_board headers :  {headers}")
+                            logger.info(f"StarRail_board cookies :  {cookies}")
+                            res = await client.get(url, headers=headers,
+                                                   cookies=cookies,
+                                                   timeout=_conf.preference.timeout)
+                        api_result = ApiResultHandler(res.json())
+                        logger.info(f"simple_api StarRail_board api_result : {api_result}")
+                        if api_result.login_expired:
+                            logger.info(
+                                f"崩铁实时便笺: 用户 {account.bbs_uid} 登录失效")
+                            logger.debug(f"网络请求返回: {res.text}")
+                            return StarRailBoardStatus(login_expired=True), None
+
+                        if api_result.invalid_ds:
+                            logger.info(
+                                f"崩铁实时便笺: 用户 {account.bbs_uid} DS 校验失败")
+                            logger.debug(f"网络请求返回: {res.text}")
+                        if api_result.retcode == 1034:
+                            logger.info(
+                                f"崩铁实时便笺: 用户 {account.bbs_uid} 可能被验证码阻拦")
+                            logger.debug(f"网络请求返回: {res.text}")
+                        return StarRailBoardStatus(success=True), StarRailBoard.parse_obj(api_result.data)
+            except tenacity.RetryError as e:
+                if is_incorrect_return(e):
+                    logger.exception("崩铁实时便笺: 服务器没有正确返回")
+                    logger.debug(f"网络请求返回: {res.text}")
+                    return StarRailBoardStatus(incorrect_return=True), None
+                else:
+                    logger.exception("崩铁实时便笺: 请求失败")
+                    return StarRailBoardStatus(network_error=True), None
+    if flag:
+        return StarRailBoardStatus(no_starrail_account=True), None
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/user_check.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/user_check.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,21 +1,23 @@
 """
 ### QQ好友相关
 """
 import asyncio
+import json
+import os
 
 from nonebot import get_driver, on_request
 from nonebot.adapters.onebot.v11 import (Bot, FriendRequestEvent,
                                          GroupRequestEvent, RequestEvent)
 from nonebot_plugin_apscheduler import scheduler
 
-from .plugin_data import PluginDataManager, write_plugin_data
+from .plugin_data import PluginDataManager, write_plugin_data, DELETED_USERS_PATH
 from .utils import logger
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
 _driver = get_driver()
 friendRequest = on_request(priority=1, block=True)
 
 
 @friendRequest.handle()
 async def _(bot: Bot, event: RequestEvent):
     command_start = list(get_driver().config.command_start)[0]
@@ -41,16 +43,24 @@
     """
     logger.info(f'{_conf.preference.log_head}正在检查好友列表...')
     friend_list = await bot.get_friend_list()
     for user in _conf.users:
         user_filter = filter(lambda x: x["user_id"] == user, friend_list)
         friend = next(user_filter, None)
         if not friend:
-            logger.info(f'{_conf.preference.log_head}用户 {user} 不在好友列表内，已删除其数据')
-            _conf.users.pop(user)
+            if not os.path.exists(DELETED_USERS_PATH):
+                os.mkdir(DELETED_USERS_PATH)
+            json.dump(
+                _conf.users.pop(user),
+                open(DELETED_USERS_PATH / f"{user}.json", "w"),
+                ensure_ascii=False,
+                indent=4
+            )
             write_plugin_data()
+            logger.info(f'{_conf.preference.log_head}用户 {user} 不在好友列表内，'
+                        f'已删除其数据，并备份至 {DELETED_USERS_PATH / f"{user}.json"}')
 
 
 @_driver.on_bot_connect
 async def _(bot: Bot):
     scheduler.add_job(id='check_friend', replace_existing=True,
                       trigger="cron", hour='23', minute='59', func=check_friend_list, args=(bot,))
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/user_data.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/user_data.py`

 * *Files 2% similar despite different names*

```diff
@@ -211,25 +211,29 @@
     address: Optional[Address]
     """收货地址"""
 
     device_id_ios: str
     """iOS设备用 deviceID"""
     device_id_android: str
     """安卓设备用 deviceID"""
+    device_fp: Optional[str]
+    """iOS设备用 deviceFp"""
 
     enable_mission: bool = True
     '''是否开启米游币任务计划'''
     enable_game_sign: bool = True
     '''是否开启米游社游戏签到计划'''
     enable_resin: bool = True
     '''是否开启原神树脂提醒'''
     platform: Literal["ios", "android"] = "ios"
     '''设备平台'''
     mission_games: Set[type] = {}
     '''在哪些板块执行米游币任务计划'''
+    user_stamina_threshold: Optional[int] = 0
+    '''崩铁便笺体力提醒阈值，0为一直提醒'''
 
     def __init__(self, **data: Any):
         if not data.get("device_id_ios") or not data.get("device_id_android"):
             from .utils import generate_device_id
             if not data.get("device_id_ios"):
                 data.setdefault("device_id_ios", generate_device_id())
             if not data.get("device_id_android"):
```

### Comparing `nonebot_plugin_mystool-1.0.1/src/nonebot_plugin_mystool/utils.py` & `nonebot_plugin_mystool-1.1.0/src/nonebot_plugin_mystool/utils.py`

 * *Files 6% similar despite different names*

```diff
@@ -11,26 +11,25 @@
                     Union, Optional)
 from urllib.parse import urlencode
 
 import httpx
 import nonebot
 import nonebot.log
 import nonebot.plugin
-import ntplib
 import tenacity
 from nonebot.internal.matcher import Matcher
 from nonebot.log import logger
 
 from .data_model import GeetestResult
-from .plugin_data import PluginDataManager
+from .plugin_data import PluginDataManager, Preference
 
 if TYPE_CHECKING:
     from loguru import Logger
 
-_conf = PluginDataManager.plugin_data_obj
+_conf = PluginDataManager.plugin_data
 
 
 class CommandBegin:
     """
     命令开头字段
     （包括例如'/'和插件命令起始字段例如'mystool'）
     已重写__str__方法
@@ -113,52 +112,14 @@
     return tenacity.AsyncRetrying(
         stop=custom_attempt_times(retry),
         retry=tenacity.retry_if_exception_type(BaseException),
         wait=tenacity.wait_fixed(_conf.preference.retry_interval),
     )
 
 
-class NtpTime:
-    """
-    NTP时间校准相关
-    """
-    time_offset = 0
-    """本地时间与互联网时间的偏差"""
-
-    @classmethod
-    def sync(cls):
-        """
-        校准时间
-        """
-        if _conf.preference.enable_ntp_sync:
-            if not _conf.preference.ntp_server:
-                logger.error("开启了互联网时间校对，但未配置NTP服务器 preference.ntp_server，放弃时间同步")
-                return False
-            try:
-                for attempt in get_async_retry(True):
-                    with attempt:
-                        cls.time_offset = ntplib.NTPClient().request(
-                            _conf.preference.ntp_server).tx_time - time.time()
-            except tenacity.RetryError:
-                logger.exception("校对互联网时间失败，改为使用本地时间")
-                return False
-            logger.info("互联网时间校对完成")
-            return True
-        else:
-            logger.info("未开启互联网时间校对，跳过时间同步")
-            return True
-
-    @classmethod
-    def time(cls) -> float:
-        """
-        获取校准后的时间（如果校准成功）
-        """
-        return time.time() + cls.time_offset
-
-
 def generate_device_id() -> str:
     """
     生成随机的x-rpc-device_id
     """
     return str(uuid.uuid4()).upper()
 
 
@@ -203,15 +164,15 @@
     """
     if data is None and params is None or \
             salt is not None and salt != _conf.salt_config.SALT_PROD:
         if platform == "ios":
             salt = salt or _conf.salt_config.SALT_IOS
         else:
             salt = salt or _conf.salt_config.SALT_ANDROID
-        t = str(int(NtpTime.time()))
+        t = str(int(time.time()))
         a = "".join(random.sample(
             string.ascii_lowercase + string.digits, 6))
         re = hashlib.md5(
             f"salt={salt}&t={t}&r={a}".encode()).hexdigest()
         return f"{t},{a},{re}"
     else:
         if params:
@@ -244,18 +205,18 @@
     使用打码平台获取人机验证validate
 
     :param gt: 验证码gt
     :param challenge: challenge
     :param retry: 是否允许重试
     :return: 如果配置了平台URL，且 gt, challenge 不为空，返回 GeetestResult
     """
-    content = {
-        "gt": gt,
-        "challenge": challenge
-    }
+    content = _conf.preference.geetest_json or Preference().geetest_json
+    for key, value in content.items():
+        if isinstance(value, str):
+            content[key] = value.format(gt=gt, challenge=challenge)
 
     if gt and challenge and _conf.preference.geetest_url:
         try:
             async for attempt in get_async_retry(retry):
                 with attempt:
                     async with httpx.AsyncClient() as client:
                         res = await client.post(
@@ -267,14 +228,34 @@
                         return GeetestResult(validate=geetest_data['data']['validate'], seccode="")
         except tenacity.RetryError:
             logger.exception(f"{_conf.preference.log_head}获取人机验证validate失败")
     else:
         return GeetestResult("", "")
 
 
+def generate_seed_id(length: int = 8) -> str:
+    """
+    生成随机的 seed_id（即长度为8的十六进制数）
+
+    :param length: 16进制数长度
+    """
+    max_num = int("FF" * length, 16)
+    return hex(random.randint(0, max_num))[2:]
+
+
+def generate_fp_locally(length: int = 13):
+    """
+    于本地生成 device_fp
+
+    :param length: device_fp 长度
+    """
+    characters = string.digits + "abcdef"
+    return ''.join(random.choices(characters, k=length))
+
+
 async def get_file(url: str, retry: bool = True):
     """
     下载文件
 
     :param url: 文件URL
     :param retry: 是否允许重试
     :return: 文件数据
```

### Comparing `nonebot_plugin_mystool-1.0.1/PKG-INFO` & `nonebot_plugin_mystool-1.1.0/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 Metadata-Version: 2.1
 Name: nonebot-plugin-mystool
-Version: 1.0.1
+Version: 1.1.0
 Summary: NoneBot2插件|米游社工具-每日米游币任务、游戏签到、商品兑换、免抓包登录、原神树脂提醒
 Home-page: https://github.com/Ljzd-PRO/nonebot-plugin-mystool
 License: MIT
 Keywords: bot,qq,qqbot,onebotv11,onebot,nonebot2,nonebot,mihoyo,mihoyobbs
 Author: Ljzd-PRO
 Author-email: ljzd@office.ljzd-pro.ml
 Requires-Python: >=3.9,<4.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Requires-Dist: Pillow (>=9.5.0,<10.0.0)
+Requires-Dist: Pillow (>=9.5,<11.0)
 Requires-Dist: httpx (>=0.24.1,<0.25.0)
 Requires-Dist: nonebot_adapter_onebot (>=2.2.3,<3.0.0)
 Requires-Dist: nonebot_plugin_apscheduler (>=0.2.0)
 Requires-Dist: ntplib (>=0.4.0,<0.5.0)
 Requires-Dist: requests (>=2.31.0,<3.0.0)
 Requires-Dist: tenacity (>=8.2.2,<9.0.0)
 Project-URL: Bug Tracker, https://github.com/Ljzd-PRO/nonebot-plugin-mystool/issues
@@ -40,59 +40,46 @@
   <img alt="最新发行版" src="https://img.shields.io/github/v/release/Ljzd-PRO/nonebot-plugin-mysTool?logo=python&style=for-the-badge">
   <img alt="最后提交" src="https://img.shields.io/github/last-commit/Ljzd-PRO/nonebot-plugin-mysTool?style=for-the-badge">
 </div>
 
 # mysTool - 米游社辅助工具插件
 
 ## 📣 更新内容
+### 2023.7.23 - v1.1.0
+- 增加崩坏：星穹铁道的便笺功能 #140 #143 by @Joseandluue @RemiDre
+    > 说明文档：[🔗星穹铁道实时便笺](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/wiki/Information-StarRailStatus)
+- 修复每小时都发送便笺通知的Bug #135
+- 人机验证打码平台支持自定义JSON内容 #133
+    > 说明文档：[🔗geetest_json](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/wiki/Configuration-Preference#geetest_json)
+- 修复商品兑换API #110
+- 不在好友列表的用户数据在删除前将进行备份 #129
+    > 备份目录：`data/nonebot_plugin_mystool/deletedUsers`
+- 防止因插件数据文件中默认存在 device_config, salt_config 而导致更新后默认配置被原配置覆盖的问题
+- 若需要修改 device_config 配置，修改后还设置插件数据文件中 preference.override_device_and_salt 为 true 以覆盖默认值
+    > 说明文档：
+    > - [🔗网络请求设备信息 `class DeviceConfig`](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/wiki/Configuration-DeviceConfig)
+    > - [🔗override_device_and_salt](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/wiki/Configuration-Preference#override_device_and_salt)
+- 在兑换开始后的一段时间内不断尝试兑换，直到成功 #110
+- 兑换开始后将不会延迟兑换，用户数据文件中 `preference.exchange_latency` 将作为同一线程下每个兑换请求之间的时间间隔 #110
+- 兑换请求日志内容增加了发送请求时的时间戳
 
 ### 2023.6.23 - v1.0.1
 - 修复无法导出Cookies的问题
 - 修复因缺少参量质变仪数据而导致不断提醒的Bug
 - 修复账号设置中游戏签到开启/关闭状态实际对应的是米游币任务的Bug #121 by @xxtg666
 
-
-### 2023.6.23 - v1.0.0
-#### v1.0.0
-- 修复Windows, macOS多进程生成商品图片失败的问题 [#120](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/pull/120) by @Night-stars-1
-
-#### v1.0.0-beta.2
-- 支持使用人机验证打码平台处理人机验证任务 [#119](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/pull/119) by @Night-stars-1
-- 原神便笺获取失败时更换为使用米游社iOS小组件API获取 [#119](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/pull/119) by @Night-stars-1
-- 修复原神便笺和讨论区签到可能因为DS无效而失败的问题
-
-#### v1.0.0-beta.1
-- 大量的代码重构，包括米游社API的客户端实现、用户数据相关、插件配置相关、API相关数据模型
-- 从显示用户账号绑定的手机号改为显示账号的米游社ID
-- 设置、兑换计划功能支持群聊使用
-- 登陆绑定只需要进行一次短信验证
-- 用户数据文件、插件配置文件 **格式更新，与 v1.0.0 之前的版本不兼容**
-- 修复添加兑换任务时出现的UID不存在错误
-- 修复商品图片生成完才发出后台正在生成提示的问题
-- 异常捕获更加准确
-- 改进了一些文本
-
-### 2023.5.18 - v0.2.9
-- 多进程生成商品图片（多核），加快图片生成速度
-- 修复部分商品兑换时间错误的问题（如米游社商品晚了一周）
-
-### 2023.5.4 - v0.2.8
-- 增加对星穹铁道的签到功能的支持 - [#89](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/pull/89) by @ayakasuki
-- 修复插件命令优先度问题 - [#88](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/pull/88) by @ayakasuki
-- 部分文本错误修正 - [#90](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/pull/90) by @black-zero358
-
 ## 功能和特性
 
 - 短信验证登录，免抓包获取 Cookie
 - 自动完成每日米游币任务
 - 自动进行游戏签到
-- 可制定米游币商品兑换计划，到点兑换
+- 可制定米游币商品兑换计划，到点兑换（因加入了人机验证，成功率较低）
 - 可支持多个 QQ 账号，每个 QQ 账号可绑定多个米哈游账户
 - QQ 推送执行结果通知
-- 原神树脂、洞天宝钱、质量参变仪已满时推送通知
+- 原神、崩坏：星穹铁道状态便笺通知
 
 ## 使用说明
 
 ### 🛠️ NoneBot2 机器人部署和插件安装
 
 请查看 -> [🔗Installation](https://github.com/Ljzd-PRO/nonebot-plugin-mystool/wiki/Installation)
```

