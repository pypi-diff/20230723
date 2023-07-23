# Comparing `tmp/simple_lama_inpainting-0.1.0.tar.gz` & `tmp/simple_lama_inpainting-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "simple_lama_inpainting-0.1.0.tar", last modified: Sat Dec 17 13:33:23 2022, max compression
+gzip compressed data, was "simple_lama_inpainting-0.1.1.tar", max compression
```

## Comparing `simple_lama_inpainting-0.1.0.tar` & `simple_lama_inpainting-0.1.1.tar`

### file list

```diff
@@ -1,23 +1,10 @@
-drwx------   0 enesmsahin  (1003) users      (100)        0 2022-12-17 13:33:23.268564 simple_lama_inpainting-0.1.0/
--rw-------   0 enesmsahin  (1003) users      (100)    11357 2022-12-17 13:12:48.000000 simple_lama_inpainting-0.1.0/LICENSE
--rw-------   0 enesmsahin  (1003) users      (100)    13100 2022-12-17 13:33:23.268564 simple_lama_inpainting-0.1.0/PKG-INFO
--rw-------   0 enesmsahin  (1003) users      (100)     1058 2022-12-17 13:12:48.000000 simple_lama_inpainting-0.1.0/README.md
--rw-------   0 enesmsahin  (1003) users      (100)       84 2022-12-17 13:12:48.000000 simple_lama_inpainting-0.1.0/pyproject.toml
--rw-------   0 enesmsahin  (1003) users      (100)      981 2022-12-17 13:33:23.272564 simple_lama_inpainting-0.1.0/setup.cfg
-drwx------   0 enesmsahin  (1003) users      (100)        0 2022-12-17 13:33:23.268564 simple_lama_inpainting-0.1.0/src/
-drwx------   0 enesmsahin  (1003) users      (100)        0 2022-12-17 13:33:23.268564 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting/
--rw-------   0 enesmsahin  (1003) users      (100)       75 2022-12-17 13:12:48.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting/__init__.py
--rw-------   0 enesmsahin  (1003) users      (100)     1204 2022-12-17 13:26:54.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting/cli.py
-drwx------   0 enesmsahin  (1003) users      (100)        0 2022-12-17 13:33:23.268564 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting/models/
--rw-------   0 enesmsahin  (1003) users      (100)       58 2022-12-17 13:12:48.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting/models/__init__.py
--rw-------   0 enesmsahin  (1003) users      (100)     1315 2022-12-17 13:12:48.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting/models/model.py
-drwx------   0 enesmsahin  (1003) users      (100)        0 2022-12-17 13:33:23.268564 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting/utils/
--rw-------   0 enesmsahin  (1003) users      (100)       82 2022-12-17 13:12:48.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting/utils/__init__.py
--rw-------   0 enesmsahin  (1003) users      (100)     2894 2022-12-17 13:12:48.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting/utils/util.py
-drwx------   0 enesmsahin  (1003) users      (100)        0 2022-12-17 13:33:23.268564 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting.egg-info/
--rw-------   0 enesmsahin  (1003) users      (100)    13100 2022-12-17 13:33:23.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting.egg-info/PKG-INFO
--rw-------   0 enesmsahin  (1003) users      (100)      592 2022-12-17 13:33:23.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting.egg-info/SOURCES.txt
--rw-------   0 enesmsahin  (1003) users      (100)        1 2022-12-17 13:33:23.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting.egg-info/dependency_links.txt
--rw-------   0 enesmsahin  (1003) users      (100)       68 2022-12-17 13:33:23.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting.egg-info/entry_points.txt
--rw-------   0 enesmsahin  (1003) users      (100)       50 2022-12-17 13:33:23.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting.egg-info/requires.txt
--rw-------   0 enesmsahin  (1003) users      (100)       23 2022-12-17 13:33:23.000000 simple_lama_inpainting-0.1.0/src/simple_lama_inpainting.egg-info/top_level.txt
+-rw-r--r--   0        0        0    11357 2023-07-23 07:23:28.922434 simple_lama_inpainting-0.1.1/LICENSE
+-rw-r--r--   0        0        0     1254 2023-07-11 21:55:51.529964 simple_lama_inpainting-0.1.1/README.md
+-rw-r--r--   0        0        0      690 2023-07-23 08:31:15.918958 simple_lama_inpainting-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0       86 2023-07-23 08:31:15.919316 simple_lama_inpainting-0.1.1/simple_lama_inpainting/__init__.py
+-rw-r--r--   0        0        0     1260 2023-07-23 08:31:15.919665 simple_lama_inpainting-0.1.1/simple_lama_inpainting/cli.py
+-rw-r--r--   0        0        0        0 2023-07-23 08:31:15.919734 simple_lama_inpainting-0.1.1/simple_lama_inpainting/models/__init__.py
+-rw-r--r--   0        0        0     1454 2023-07-23 08:31:15.920100 simple_lama_inpainting-0.1.1/simple_lama_inpainting/models/model.py
+-rw-r--r--   0        0        0        0 2023-07-23 08:31:15.920152 simple_lama_inpainting-0.1.1/simple_lama_inpainting/utils/__init__.py
+-rw-r--r--   0        0        0     2972 2023-07-23 08:31:15.920451 simple_lama_inpainting-0.1.1/simple_lama_inpainting/utils/util.py
+-rw-r--r--   0        0        0     1852 1970-01-01 00:00:00.000000 simple_lama_inpainting-0.1.1/PKG-INFO
```

### Comparing `simple_lama_inpainting-0.1.0/LICENSE` & `simple_lama_inpainting-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `simple_lama_inpainting-0.1.0/README.md` & `simple_lama_inpainting-0.1.1/README.md`

 * *Files 11% similar despite different names*

```diff
@@ -1,67 +1,79 @@
 00000000: 2320 7369 6d70 6c65 2d6c 616d 612d 696e  # simple-lama-in
-00000010: 7061 696e 7469 6e67 0a0a 5369 6d70 6c65  painting..Simple
-00000020: 2070 6970 2070 6163 6b61 6765 2066 6f72   pip package for
-00000030: 204c 614d 615b 315d 2069 6e70 6169 6e74   LaMa[1] inpaint
-00000040: 696e 672e 0a0a 2323 2049 6e73 7461 6c6c  ing...## Install
-00000050: 6174 696f 6e0a 6060 600a 7069 7020 696e  ation.```.pip in
-00000060: 7374 616c 6c20 7369 6d70 6c65 2d6c 616d  stall simple-lam
-00000070: 612d 696e 7061 696e 7469 6e67 0a60 6060  a-inpainting.```
-00000080: 0a0a 2323 2055 7361 6765 0a23 2323 2043  ..## Usage.### C
-00000090: 4c49 0a60 6060 0a73 696d 706c 655f 6c61  LI.```.simple_la
-000000a0: 6d61 203c 7061 7468 5f74 6f5f 696e 7075  ma <path_to_inpu
-000000b0: 745f 696d 6167 653e 203c 7061 7468 5f74  t_image> <path_t
-000000c0: 6f5f 6d61 736b 5f69 6d61 6765 3e20 3c70  o_mask_image> <p
-000000d0: 6174 685f 746f 5f6f 7574 7075 745f 696d  ath_to_output_im
-000000e0: 6167 653e 0a60 6060 0a0a 2323 2320 496e  age>.```..### In
-000000f0: 7465 6772 6174 696f 6e20 746f 2059 6f75  tegration to You
-00000100: 7220 436f 6465 0a49 6e70 7574 2066 6f72  r Code.Input for
-00000110: 6d61 7473 3a20 606e 702e 6e64 6172 7261  mats: `np.ndarra
-00000120: 7960 206f 7220 6050 494c 2e49 6d61 6765  y` or `PIL.Image
-00000130: 2e49 6d61 6765 602e 2028 3320 6368 616e  .Image`. (3 chan
-00000140: 6e65 6c20 696e 7075 7420 696d 6167 6520  nel input image 
-00000150: 2620 3120 6368 616e 6e65 6c20 6269 6e61  & 1 channel bina
-00000160: 7279 206d 6173 6b20 696d 6167 6520 7768  ry mask image wh
-00000170: 6572 6520 7069 7865 6c73 2077 6974 6820  ere pixels with 
-00000180: 3235 3520 7769 6c6c 2062 6520 696e 7061  255 will be inpa
-00000190: 696e 7465 6429 2e20 5c0a 4f75 7470 7574  inted). \.Output
-000001a0: 2066 6f72 6d61 743a 2060 5049 4c2e 496d   format: `PIL.Im
-000001b0: 6167 652e 496d 6167 6560 0a60 6060 0a66  age.Image`.```.f
-000001c0: 726f 6d20 7369 6d70 6c65 5f6c 616d 615f  rom simple_lama_
-000001d0: 696e 7061 696e 7469 6e67 2069 6d70 6f72  inpainting impor
-000001e0: 7420 5369 6d70 6c65 4c61 6d61 0a66 726f  t SimpleLama.fro
-000001f0: 6d20 5049 4c20 696d 706f 7274 2049 6d61  m PIL import Ima
-00000200: 6765 0a0a 7369 6d70 6c65 5f6c 616d 6120  ge..simple_lama 
-00000210: 3d20 5369 6d70 6c65 4c61 6d61 2829 0a0a  = SimpleLama()..
-00000220: 696d 675f 7061 7468 203d 2022 696d 6167  img_path = "imag
-00000230: 652e 706e 6722 0a6d 6173 6b5f 7061 7468  e.png".mask_path
-00000240: 203d 2022 6d61 736b 2e70 6e67 220a 0a69   = "mask.png"..i
-00000250: 6d61 6765 203d 2049 6d61 6765 2e6f 7065  mage = Image.ope
-00000260: 6e28 696d 675f 7061 7468 290a 6d61 736b  n(img_path).mask
-00000270: 203d 2049 6d61 6765 2e6f 7065 6e28 6d61   = Image.open(ma
-00000280: 736b 5f70 6174 6829 0a0a 7265 7375 6c74  sk_path)..result
-00000290: 203d 2073 696d 706c 655f 6c61 6d61 2869   = simple_lama(i
-000002a0: 6d61 6765 2c20 6d61 736b 290a 7265 7375  mage, mask).resu
-000002b0: 6c74 2e73 6176 6528 2269 6e70 6169 6e74  lt.save("inpaint
-000002c0: 6564 2e70 6e67 2229 0a60 6060 0a0a 2323  ed.png").```..##
-000002d0: 2053 6f75 7263 6573 0a5b 315d 2053 7576   Sources.[1] Suv
-000002e0: 6f72 6f76 2c20 522e 2c20 4c6f 6761 6368  orov, R., Logach
-000002f0: 6576 612c 2045 2e2c 204d 6173 6869 6b68  eva, E., Mashikh
-00000300: 696e 2c20 412e 2c20 5265 6d69 7a6f 7661  in, A., Remizova
-00000310: 2c20 412e 2c20 4173 6875 6b68 612c 2041  , A., Ashukha, A
-00000320: 2e2c 2053 696c 7665 7374 726f 762c 2041  ., Silvestrov, A
-00000330: 2e2c 204b 6f6e 672c 204e 2e2c 2047 6f6b  ., Kong, N., Gok
-00000340: 612c 2048 2e2c 2050 6172 6b2c 204b 2e2c  a, H., Park, K.,
-00000350: 2026 204c 656d 7069 7473 6b79 2c20 562e   & Lempitsky, V.
-00000360: 2028 3230 3231 292e 2052 6573 6f6c 7574   (2021). Resolut
-00000370: 696f 6e2d 726f 6275 7374 204c 6172 6765  ion-robust Large
-00000380: 204d 6173 6b20 496e 7061 696e 7469 6e67   Mask Inpainting
-00000390: 2077 6974 6820 466f 7572 6965 7220 436f   with Fourier Co
-000003a0: 6e76 6f6c 7574 696f 6e73 2e20 6172 5869  nvolutions. arXi
-000003b0: 7620 7072 6570 7269 6e74 2061 7258 6976  v preprint arXiv
-000003c0: 3a32 3130 392e 3037 3136 312e 205c 0a5b  :2109.07161. \.[
-000003d0: 325d 2068 7474 7073 3a2f 2f67 6974 6875  2] https://githu
-000003e0: 622e 636f 6d2f 7361 6963 2d6d 6461 6c2f  b.com/saic-mdal/
-000003f0: 6c61 6d61 205c 0a5b 335d 2068 7474 7073  lama \.[3] https
-00000400: 3a2f 2f67 6974 6875 622e 636f 6d2f 5361  ://github.com/Sa
-00000410: 6e73 7465 722f 6c61 6d61 2d63 6c65 616e  nster/lama-clean
-00000420: 6572                                     er
+00000010: 7061 696e 7469 6e67 0a0a 3c64 6976 2061  painting..<div a
+00000020: 6c69 676e 3d22 6365 6e74 6572 223e 0a53  lign="center">.S
+00000030: 696d 706c 6520 7069 7020 7061 636b 6167  imple pip packag
+00000040: 6520 666f 7220 4c61 4d61 5b31 5d20 696e  e for LaMa[1] in
+00000050: 7061 696e 7469 6e67 2e3c 6272 3e0a 3c61  painting.<br>.<a
+00000060: 2068 7265 663d 2268 7474 7073 3a2f 2f62   href="https://b
+00000070: 6164 6765 2e66 7572 792e 696f 2f70 792f  adge.fury.io/py/
+00000080: 7369 6d70 6c65 2d6c 616d 612d 696e 7061  simple-lama-inpa
+00000090: 696e 7469 6e67 223e 3c69 6d67 2073 7263  inting"><img src
+000000a0: 3d22 6874 7470 733a 2f2f 6261 6467 652e  ="https://badge.
+000000b0: 6675 7279 2e69 6f2f 7079 2f73 696d 706c  fury.io/py/simpl
+000000c0: 652d 6c61 6d61 2d69 6e70 6169 6e74 696e  e-lama-inpaintin
+000000d0: 672e 7376 6722 2061 6c74 3d22 5079 5049  g.svg" alt="PyPI
+000000e0: 2076 6572 7369 6f6e 2220 6865 6967 6874   version" height
+000000f0: 3d22 3138 223e 3c2f 613e 0a3c 2f64 6976  ="18"></a>.</div
+00000100: 3e0a 0a23 2320 496e 7374 616c 6c61 7469  >..## Installati
+00000110: 6f6e 0a60 6060 0a70 6970 2069 6e73 7461  on.```.pip insta
+00000120: 6c6c 2073 696d 706c 652d 6c61 6d61 2d69  ll simple-lama-i
+00000130: 6e70 6169 6e74 696e 670a 6060 600a 0a23  npainting.```..#
+00000140: 2320 5573 6167 650a 2323 2320 434c 490a  # Usage.### CLI.
+00000150: 6060 600a 7369 6d70 6c65 5f6c 616d 6120  ```.simple_lama 
+00000160: 3c70 6174 685f 746f 5f69 6e70 7574 5f69  <path_to_input_i
+00000170: 6d61 6765 3e20 3c70 6174 685f 746f 5f6d  mage> <path_to_m
+00000180: 6173 6b5f 696d 6167 653e 203c 7061 7468  ask_image> <path
+00000190: 5f74 6f5f 6f75 7470 7574 5f69 6d61 6765  _to_output_image
+000001a0: 3e0a 6060 600a 0a23 2323 2049 6e74 6567  >.```..### Integ
+000001b0: 7261 7469 6f6e 2074 6f20 596f 7572 2043  ration to Your C
+000001c0: 6f64 650a 496e 7075 7420 666f 726d 6174  ode.Input format
+000001d0: 733a 2060 6e70 2e6e 6461 7272 6179 6020  s: `np.ndarray` 
+000001e0: 6f72 2060 5049 4c2e 496d 6167 652e 496d  or `PIL.Image.Im
+000001f0: 6167 6560 2e20 2833 2063 6861 6e6e 656c  age`. (3 channel
+00000200: 2069 6e70 7574 2069 6d61 6765 2026 2031   input image & 1
+00000210: 2063 6861 6e6e 656c 2062 696e 6172 7920   channel binary 
+00000220: 6d61 736b 2069 6d61 6765 2077 6865 7265  mask image where
+00000230: 2070 6978 656c 7320 7769 7468 2032 3535   pixels with 255
+00000240: 2077 696c 6c20 6265 2069 6e70 6169 6e74   will be inpaint
+00000250: 6564 292e 205c 0a4f 7574 7075 7420 666f  ed). \.Output fo
+00000260: 726d 6174 3a20 6050 494c 2e49 6d61 6765  rmat: `PIL.Image
+00000270: 2e49 6d61 6765 600a 6060 6070 7974 686f  .Image`.```pytho
+00000280: 6e0a 6672 6f6d 2073 696d 706c 655f 6c61  n.from simple_la
+00000290: 6d61 5f69 6e70 6169 6e74 696e 6720 696d  ma_inpainting im
+000002a0: 706f 7274 2053 696d 706c 654c 616d 610a  port SimpleLama.
+000002b0: 6672 6f6d 2050 494c 2069 6d70 6f72 7420  from PIL import 
+000002c0: 496d 6167 650a 0a73 696d 706c 655f 6c61  Image..simple_la
+000002d0: 6d61 203d 2053 696d 706c 654c 616d 6128  ma = SimpleLama(
+000002e0: 290a 0a69 6d67 5f70 6174 6820 3d20 2269  )..img_path = "i
+000002f0: 6d61 6765 2e70 6e67 220a 6d61 736b 5f70  mage.png".mask_p
+00000300: 6174 6820 3d20 226d 6173 6b2e 706e 6722  ath = "mask.png"
+00000310: 0a0a 696d 6167 6520 3d20 496d 6167 652e  ..image = Image.
+00000320: 6f70 656e 2869 6d67 5f70 6174 6829 0a6d  open(img_path).m
+00000330: 6173 6b20 3d20 496d 6167 652e 6f70 656e  ask = Image.open
+00000340: 286d 6173 6b5f 7061 7468 290a 0a72 6573  (mask_path)..res
+00000350: 756c 7420 3d20 7369 6d70 6c65 5f6c 616d  ult = simple_lam
+00000360: 6128 696d 6167 652c 206d 6173 6b29 0a72  a(image, mask).r
+00000370: 6573 756c 742e 7361 7665 2822 696e 7061  esult.save("inpa
+00000380: 696e 7465 642e 706e 6722 290a 6060 600a  inted.png").```.
+00000390: 0a23 2320 536f 7572 6365 730a 5b31 5d20  .## Sources.[1] 
+000003a0: 5375 766f 726f 762c 2052 2e2c 204c 6f67  Suvorov, R., Log
+000003b0: 6163 6865 7661 2c20 452e 2c20 4d61 7368  acheva, E., Mash
+000003c0: 696b 6869 6e2c 2041 2e2c 2052 656d 697a  ikhin, A., Remiz
+000003d0: 6f76 612c 2041 2e2c 2041 7368 756b 6861  ova, A., Ashukha
+000003e0: 2c20 412e 2c20 5369 6c76 6573 7472 6f76  , A., Silvestrov
+000003f0: 2c20 412e 2c20 4b6f 6e67 2c20 4e2e 2c20  , A., Kong, N., 
+00000400: 476f 6b61 2c20 482e 2c20 5061 726b 2c20  Goka, H., Park, 
+00000410: 4b2e 2c20 2620 4c65 6d70 6974 736b 792c  K., & Lempitsky,
+00000420: 2056 2e20 2832 3032 3129 2e20 5265 736f   V. (2021). Reso
+00000430: 6c75 7469 6f6e 2d72 6f62 7573 7420 4c61  lution-robust La
+00000440: 7267 6520 4d61 736b 2049 6e70 6169 6e74  rge Mask Inpaint
+00000450: 696e 6720 7769 7468 2046 6f75 7269 6572  ing with Fourier
+00000460: 2043 6f6e 766f 6c75 7469 6f6e 732e 2061   Convolutions. a
+00000470: 7258 6976 2070 7265 7072 696e 7420 6172  rXiv preprint ar
+00000480: 5869 763a 3231 3039 2e30 3731 3631 2e20  Xiv:2109.07161. 
+00000490: 5c0a 5b32 5d20 6874 7470 733a 2f2f 6769  \.[2] https://gi
+000004a0: 7468 7562 2e63 6f6d 2f73 6169 632d 6d64  thub.com/saic-md
+000004b0: 616c 2f6c 616d 6120 5c0a 5b33 5d20 6874  al/lama \.[3] ht
+000004c0: 7470 733a 2f2f 6769 7468 7562 2e63 6f6d  tps://github.com
+000004d0: 2f53 616e 7374 6572 2f6c 616d 612d 636c  /Sanster/lama-cl
+000004e0: 6561 6e65 720a                           eaner.
```

### Comparing `simple_lama_inpainting-0.1.0/src/simple_lama_inpainting/models/model.py` & `simple_lama_inpainting-0.1.1/simple_lama_inpainting/models/model.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,38 +1,44 @@
 import os
 import torch
 import numpy as np
 from PIL import Image
-from simple_lama_inpainting.utils import prepare_img_and_mask, download_model
+from simple_lama_inpainting.utils.util import prepare_img_and_mask, download_model
 
 LAMA_MODEL_URL = os.environ.get(
     "LAMA_MODEL_URL",
-    "https://github.com/enesmsahin/simple-lama-inpainting/releases/download/v0.1.0/big-lama.pt",
+    "https://github.com/enesmsahin/simple-lama-inpainting/releases/download/v0.1.0/big-lama.pt",  # noqa
 )
 
-class SimpleLama():
-    def __init__(self, device=torch.device("cuda" if torch.cuda.is_available() else "cpu")) -> None:
+
+class SimpleLama:
+    def __init__(
+        self,
+        device: torch.device = torch.device(
+            "cuda" if torch.cuda.is_available() else "cpu"
+        ),
+    ) -> None:
         if os.environ.get("LAMA_MODEL"):
             model_path = os.environ.get("LAMA_MODEL")
             if not os.path.exists(model_path):
                 raise FileNotFoundError(
                     f"lama torchscript model not found: {model_path}"
                 )
         else:
             model_path = download_model(LAMA_MODEL_URL)
-        
-        self.model = torch.jit.load(model_path)
+
+        self.model = torch.jit.load(model_path, map_location=device)
         self.model.eval()
         self.model.to(device)
         self.device = device
 
-    def __call__(self, image, mask):
+    def __call__(self, image: Image.Image | np.ndarray, mask: Image.Image | np.ndarray):
         image, mask = prepare_img_and_mask(image, mask, self.device)
 
         with torch.inference_mode():
             inpainted = self.model(image, mask)
 
             cur_res = inpainted[0].permute(1, 2, 0).detach().cpu().numpy()
             cur_res = np.clip(cur_res * 255, 0, 255).astype(np.uint8)
 
             cur_res = Image.fromarray(cur_res)
-            return cur_res
+            return cur_res
```

### Comparing `simple_lama_inpainting-0.1.0/src/simple_lama_inpainting/utils/util.py` & `simple_lama_inpainting-0.1.1/simple_lama_inpainting/utils/util.py`

 * *Files 4% similar despite different names*

```diff
@@ -3,56 +3,66 @@
 import torch
 import numpy as np
 import cv2
 from PIL import Image
 from torch.hub import download_url_to_file, get_dir
 from urllib.parse import urlparse
 
+
+# Source https://github.com/advimman/lama
 def get_image(image):
     if isinstance(image, Image.Image):
         img = np.array(image)
     elif isinstance(image, np.ndarray):
         img = image.copy()
     else:
-        raise Exception(f"Input image should be either PIL Image or numpy array!")
-    
+        raise Exception("Input image should be either PIL Image or numpy array!")
+
     if img.ndim == 3:
-        img = np.transpose(img, (2, 0, 1)) # chw
+        img = np.transpose(img, (2, 0, 1))  # chw
     elif img.ndim == 2:
         img = img[np.newaxis, ...]
 
     assert img.ndim == 3
-    
+
     img = img.astype(np.float32) / 255
     return img
 
+
 def ceil_modulo(x, mod):
     if x % mod == 0:
         return x
     return (x // mod + 1) * mod
 
+
 def scale_image(img, factor, interpolation=cv2.INTER_AREA):
     if img.shape[0] == 1:
         img = img[0]
     else:
         img = np.transpose(img, (1, 2, 0))
 
     img = cv2.resize(img, dsize=None, fx=factor, fy=factor, interpolation=interpolation)
 
     if img.ndim == 2:
         img = img[None, ...]
     else:
         img = np.transpose(img, (2, 0, 1))
     return img
 
+
 def pad_img_to_modulo(img, mod):
     channels, height, width = img.shape
     out_height = ceil_modulo(height, mod)
     out_width = ceil_modulo(width, mod)
-    return np.pad(img, ((0, 0), (0, out_height - height), (0, out_width - width)), mode='symmetric')
+    return np.pad(
+        img,
+        ((0, 0), (0, out_height - height), (0, out_width - width)),
+        mode="symmetric",
+    )
+
 
 def prepare_img_and_mask(image, mask, device, pad_out_to_modulo=8, scale_factor=None):
     out_image = get_image(image)
     out_mask = get_image(mask)
 
     if scale_factor is not None:
         out_image = scale_image(out_image, scale_factor)
@@ -65,15 +75,16 @@
     out_image = torch.from_numpy(out_image).unsqueeze(0).to(device)
     out_mask = torch.from_numpy(out_mask).unsqueeze(0).to(device)
 
     out_mask = (out_mask > 0) * 1
 
     return out_image, out_mask
 
-# Source: https://github.com/Sanster/lama-cleaner/blob/6cfc7c30f1d6428c02e21d153048381923498cac/lama_cleaner/helper.py
+
+# Source: https://github.com/Sanster/lama-cleaner/blob/6cfc7c30f1d6428c02e21d153048381923498cac/lama_cleaner/helper.py # noqa
 def get_cache_path_by_url(url):
     parts = urlparse(url)
     hub_dir = get_dir()
     model_dir = os.path.join(hub_dir, "checkpoints")
     if not os.path.isdir(model_dir):
         os.makedirs(os.path.join(model_dir, "hub", "checkpoints"))
     filename = os.path.basename(parts.path)
@@ -83,8 +94,8 @@
 
 def download_model(url):
     cached_file = get_cache_path_by_url(url)
     if not os.path.exists(cached_file):
         sys.stderr.write('Downloading: "{}" to {}\n'.format(url, cached_file))
         hash_prefix = None
         download_url_to_file(url, cached_file, hash_prefix, progress=True)
-    return cached_file
+    return cached_file
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

