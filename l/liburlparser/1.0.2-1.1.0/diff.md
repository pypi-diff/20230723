# Comparing `tmp/liburlparser-1.0.2.tar.gz` & `tmp/liburlparser-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "liburlparser-1.0.2.tar", last modified: Wed Nov  9 12:37:21 2022, max compression
+gzip compressed data, was "liburlparser-1.1.0.tar", last modified: Wed Nov  9 12:37:21 2022, max compression
```

## Comparing `liburlparser-1.0.2.tar` & `liburlparser-1.1.0.tar`

### file list

```diff
@@ -1,37 +1,37 @@
--rw-r--r--   0        0        0      149 2022-11-09 12:37:21.000000 liburlparser-1.0.2/.clang-format
--rw-r--r--   0        0        0     1903 2022-11-09 12:37:21.000000 liburlparser-1.0.2/.github/workflows/wheels.yml
--rw-r--r--   0        0        0      333 2022-11-09 12:37:21.000000 liburlparser-1.0.2/.gitignore
--rw-r--r--   0        0        0        1 2022-11-09 12:37:21.000000 liburlparser-1.0.2/.ruff_cache/.gitignore
--rw-r--r--   0        0        0       43 2022-11-09 12:37:21.000000 liburlparser-1.0.2/.ruff_cache/CACHEDIR.TAG
--rw-r--r--   0        0        0     1117 2022-11-09 12:37:21.000000 liburlparser-1.0.2/.ruff_cache/content/14127504071872449912
--rw-r--r--   0        0        0      231 2022-11-09 12:37:21.000000 liburlparser-1.0.2/.ruff_cache/content/15196995530446509414
--rw-r--r--   0        0        0       95 2022-11-09 12:37:21.000000 liburlparser-1.0.2/.ruff_cache/content/8146325946607679399
--rw-r--r--   0        0        0     4786 2022-11-09 12:37:21.000000 liburlparser-1.0.2/CMakeLists.txt
--rw-r--r--   0        0        0     2182 2022-11-09 12:37:21.000000 liburlparser-1.0.2/LICENSE
--rw-r--r--   0        0        0     6779 2022-11-09 12:37:21.000000 liburlparser-1.0.2/README.md
--rw-r--r--   0        0        0      527 2022-11-09 12:37:21.000000 liburlparser-1.0.2/conda.recipe/meta.yaml
--rw-r--r--   0        0        0      392 2022-11-09 12:37:21.000000 liburlparser-1.0.2/docs/Doxyfile.in
--rw-r--r--   0        0        0     4529 2022-11-09 12:37:21.000000 liburlparser-1.0.2/docs/images/logo/liburlparser-logo-1.svg
--rw-r--r--   0        0        0     4515 2022-11-09 12:37:21.000000 liburlparser-1.0.2/docs/images/logo/liburlparser-logo-2.svg
--rw-r--r--   0        0        0     2517 2022-11-09 12:37:21.000000 liburlparser-1.0.2/examples/common.h
--rw-r--r--   0        0        0     2652 2022-11-09 12:37:21.000000 liburlparser-1.0.2/examples/main.cpp
--rw-r--r--   0        0        0     2303 2022-11-09 12:37:21.000000 liburlparser-1.0.2/include/urlparser.h
--rw-r--r--   0        0        0      482 2022-11-09 12:37:21.000000 liburlparser-1.0.2/noxfile.py
--rw-r--r--   0        0        0     3197 2022-11-09 12:37:21.000000 liburlparser-1.0.2/pyproject.toml
--rw-r--r--   0        0        0     5520 2022-11-09 12:37:21.000000 liburlparser-1.0.2/src/binding/main.cpp
--rw-r--r--   0        0        0      157 2022-11-09 12:37:21.000000 liburlparser-1.0.2/src/liburlparser/__init__.py
--rw-r--r--   0        0        0     1045 2022-11-09 12:37:21.000000 liburlparser-1.0.2/src/liburlparser/__main__.py
--rw-r--r--   0        0        0      887 2022-11-09 12:37:21.000000 liburlparser-1.0.2/src/liburlparser/core.py
--rw-r--r--   0        0        0     4994 2022-11-09 12:37:21.000000 liburlparser-1.0.2/src/psl.cpp
--rw-r--r--   0        0        0     3372 2022-11-09 12:37:21.000000 liburlparser-1.0.2/src/psl.h
--rw-r--r--   0        0        0    26613 2022-11-09 12:37:21.000000 liburlparser-1.0.2/src/url.cpp
--rw-r--r--   0        0        0     8937 2022-11-09 12:37:21.000000 liburlparser-1.0.2/src/url.h
--rw-r--r--   0        0        0     8388 2022-11-09 12:37:21.000000 liburlparser-1.0.2/src/urlparser.cpp
--rw-r--r--   0        0        0      350 2022-11-09 12:37:21.000000 liburlparser-1.0.2/tests/data/host_data.csv
--rw-r--r--   0        0        0      401 2022-11-09 12:37:21.000000 liburlparser-1.0.2/tests/data/url_data.csv
--rw-r--r--   0        0        0        9 2022-11-09 12:37:21.000000 liburlparser-1.0.2/tests/pytest.ini
--rw-r--r--   0        0        0     1473 2022-11-09 12:37:21.000000 liburlparser-1.0.2/tests/test.cpp
--rw-r--r--   0        0        0      535 2022-11-09 12:37:21.000000 liburlparser-1.0.2/tests/test_extra.py
--rw-r--r--   0        0        0      585 2022-11-09 12:37:21.000000 liburlparser-1.0.2/tests/test_host.py
--rw-r--r--   0        0        0      796 2022-11-09 12:37:21.000000 liburlparser-1.0.2/tests/test_url.py
--rw-r--r--   0        0        0     7822 2022-11-09 12:37:21.000000 liburlparser-1.0.2/PKG-INFO
+-rw-r--r--   0        0        0      149 2022-11-09 12:37:21.000000 liburlparser-1.1.0/.clang-format
+-rw-r--r--   0        0        0     2051 2022-11-09 12:37:21.000000 liburlparser-1.1.0/.github/workflows/wheels.yml
+-rw-r--r--   0        0        0      333 2022-11-09 12:37:21.000000 liburlparser-1.1.0/.gitignore
+-rw-r--r--   0        0        0        1 2022-11-09 12:37:21.000000 liburlparser-1.1.0/.ruff_cache/.gitignore
+-rw-r--r--   0        0        0       43 2022-11-09 12:37:21.000000 liburlparser-1.1.0/.ruff_cache/CACHEDIR.TAG
+-rw-r--r--   0        0        0     1117 2022-11-09 12:37:21.000000 liburlparser-1.1.0/.ruff_cache/content/2091015116385545009
+-rw-r--r--   0        0        0       95 2022-11-09 12:37:21.000000 liburlparser-1.1.0/.ruff_cache/content/7852328626281147919
+-rw-r--r--   0        0        0      231 2022-11-09 12:37:21.000000 liburlparser-1.1.0/.ruff_cache/content/9245763955292878600
+-rw-r--r--   0        0        0     4786 2022-11-09 12:37:21.000000 liburlparser-1.1.0/CMakeLists.txt
+-rw-r--r--   0        0        0     2182 2022-11-09 12:37:21.000000 liburlparser-1.1.0/LICENSE
+-rw-r--r--   0        0        0     6779 2022-11-09 12:37:21.000000 liburlparser-1.1.0/README.md
+-rw-r--r--   0        0        0      527 2022-11-09 12:37:21.000000 liburlparser-1.1.0/conda.recipe/meta.yaml
+-rw-r--r--   0        0        0      392 2022-11-09 12:37:21.000000 liburlparser-1.1.0/docs/Doxyfile.in
+-rw-r--r--   0        0        0     4529 2022-11-09 12:37:21.000000 liburlparser-1.1.0/docs/images/logo/liburlparser-logo-1.svg
+-rw-r--r--   0        0        0     4515 2022-11-09 12:37:21.000000 liburlparser-1.1.0/docs/images/logo/liburlparser-logo-2.svg
+-rw-r--r--   0        0        0     2517 2022-11-09 12:37:21.000000 liburlparser-1.1.0/examples/common.h
+-rw-r--r--   0        0        0     2887 2022-11-09 12:37:21.000000 liburlparser-1.1.0/examples/main.cpp
+-rw-r--r--   0        0        0     2478 2022-11-09 12:37:21.000000 liburlparser-1.1.0/include/urlparser.h
+-rw-r--r--   0        0        0      482 2022-11-09 12:37:21.000000 liburlparser-1.1.0/noxfile.py
+-rw-r--r--   0        0        0     3166 2022-11-09 12:37:21.000000 liburlparser-1.1.0/pyproject.toml
+-rw-r--r--   0        0        0     5636 2022-11-09 12:37:21.000000 liburlparser-1.1.0/src/binding/main.cpp
+-rw-r--r--   0        0        0      157 2022-11-09 12:37:21.000000 liburlparser-1.1.0/src/liburlparser/__init__.py
+-rw-r--r--   0        0        0     1045 2022-11-09 12:37:21.000000 liburlparser-1.1.0/src/liburlparser/__main__.py
+-rw-r--r--   0        0        0      887 2022-11-09 12:37:21.000000 liburlparser-1.1.0/src/liburlparser/core.py
+-rw-r--r--   0        0        0     4994 2022-11-09 12:37:21.000000 liburlparser-1.1.0/src/psl.cpp
+-rw-r--r--   0        0        0     3372 2022-11-09 12:37:21.000000 liburlparser-1.1.0/src/psl.h
+-rw-r--r--   0        0        0    26613 2022-11-09 12:37:21.000000 liburlparser-1.1.0/src/url.cpp
+-rw-r--r--   0        0        0     8937 2022-11-09 12:37:21.000000 liburlparser-1.1.0/src/url.h
+-rw-r--r--   0        0        0     9021 2022-11-09 12:37:21.000000 liburlparser-1.1.0/src/urlparser.cpp
+-rw-r--r--   0        0        0      464 2022-11-09 12:37:21.000000 liburlparser-1.1.0/tests/data/host_data.csv
+-rw-r--r--   0        0        0      601 2022-11-09 12:37:21.000000 liburlparser-1.1.0/tests/data/url_data.csv
+-rw-r--r--   0        0        0        9 2022-11-09 12:37:21.000000 liburlparser-1.1.0/tests/pytest.ini
+-rw-r--r--   0        0        0     1473 2022-11-09 12:37:21.000000 liburlparser-1.1.0/tests/test.cpp
+-rw-r--r--   0        0        0      535 2022-11-09 12:37:21.000000 liburlparser-1.1.0/tests/test_extra.py
+-rw-r--r--   0        0        0      616 2022-11-09 12:37:21.000000 liburlparser-1.1.0/tests/test_host.py
+-rw-r--r--   0        0        0      826 2022-11-09 12:37:21.000000 liburlparser-1.1.0/tests/test_url.py
+-rw-r--r--   0        0        0     7822 2022-11-09 12:37:21.000000 liburlparser-1.1.0/PKG-INFO
```

### Comparing `liburlparser-1.0.2/.github/workflows/wheels.yml` & `liburlparser-1.1.0/.github/workflows/wheels.yml`

 * *Files 9% similar despite different names*

```diff
@@ -88,7 +88,12 @@
         path: dist
 
     - uses: pypa/gh-action-pypi-publish@release/v1
       with:
         password: ${{ secrets.PYPI_PASSWORD }}
         user: ${{ secrets.PYPI_USERNAME }}
 
+#    - name: Release
+#      uses: softprops/action-gh-release@v1
+#      if: startsWith(github.ref, 'refs/tags/')
+#      with:
+#        files: dist/*
```

### Comparing `liburlparser-1.0.2/.ruff_cache/content/14127504071872449912` & `liburlparser-1.1.0/.ruff_cache/content/2091015116385545009`

 * *Files 11% similar despite different names*

```diff
@@ -1,70 +1,70 @@
 00000000: 2200 0000 0000 0000 2f67 6974 6875 622f  "......./github/
 00000010: 776f 726b 7370 6163 652f 7372 632f 6c69  workspace/src/li
 00000020: 6275 726c 7061 7273 6572 0300 0000 0000  burlparser......
-00000030: 0000 0b00 0000 0000 0000 5f5f 696e 6974  ..........__init
-00000040: 5f5f 2e70 7909 0abb 6400 0000 0023 938d  __.py...d....#..
-00000050: 30e6 389f 7a89 0100 0001 0000 0000 0000  0.8.z...........
+00000030: 0000 0b00 0000 0000 0000 5f5f 6d61 696e  ..........__main
+00000040: 5f5f 2e70 7930 23bd 6400 0000 001f 41dc  __.py0#.d.....A.
+00000050: 3791 79d1 8289 0100 0001 0000 0000 0000  7.y.............
 00000060: 0015 0000 0000 0000 006c 6962 7572 6c70  .........liburlp
-00000070: 6172 7365 722e 5f5f 696e 6974 5f5f 0600  arser.__init__..
+00000070: 6172 7365 722e 5f5f 6d61 696e 5f5f 0700  arser.__main__..
 00000080: 0000 0000 0000 1600 0000 0000 0000 5f5f  ..............__
 00000090: 6675 7475 7265 5f5f 2e61 6e6e 6f74 6174  future__.annotat
-000000a0: 696f 6e73 1700 0000 2200 0000 1600 0000  ions....".......
-000000b0: 0000 0000 6c69 6275 726c 7061 7273 6572  ....liburlparser
-000000c0: 2e63 6f72 652e 486f 7374 3600 0000 3a00  .core.Host6...:.
-000000d0: 0000 1500 0000 0000 0000 6c69 6275 726c  ..........liburl
-000000e0: 7061 7273 6572 2e63 6f72 652e 5572 6c3c  parser.core.Url<
-000000f0: 0000 003f 0000 0019 0000 0000 0000 006c  ...?...........l
-00000100: 6962 7572 6c70 6172 7365 722e 636f 7265  iburlparser.core
-00000110: 2e5f 5f64 6f63 5f5f 4100 0000 4800 0000  .__doc__A...H...
-00000120: 1d00 0000 0000 0000 6c69 6275 726c 7061  ........liburlpa
-00000130: 7273 6572 2e63 6f72 652e 5f5f 7665 7273  rser.core.__vers
-00000140: 696f 6e5f 5f4a 0000 0055 0000 0015 0000  ion__J...U......
-00000150: 0000 0000 006c 6962 7572 6c70 6172 7365  .....liburlparse
-00000160: 722e 636f 7265 2e70 736c 5700 0000 5a00  r.core.pslW...Z.
-00000170: 0000 0000 0000 0000 0000 0000 0000 0000  ................
-00000180: 0000 0700 0000 0000 0000 636f 7265 2e70  ..........core.p
-00000190: 7909 0abb 6400 0000 0023 938d 30e6 389f  y...d....#..0.8.
-000001a0: 7a89 0100 0001 0000 0000 0000 0011 0000  z...............
-000001b0: 0000 0000 006c 6962 7572 6c70 6172 7365  .....liburlparse
-000001c0: 722e 636f 7265 0900 0000 0000 0000 1600  r.core..........
-000001d0: 0000 0000 0000 5f5f 6675 7475 7265 5f5f  ......__future__
-000001e0: 2e61 6e6e 6f74 6174 696f 6e73 2600 0000  .annotations&...
-000001f0: 3100 0000 0800 0000 0000 0000 7761 726e  1...........warn
-00000200: 696e 6773 3300 0000 4200 0000 0c00 0000  ings3...B.......
-00000210: 0000 0000 7061 7468 6c69 622e 5061 7468  ....pathlib.Path
-00000220: 5700 0000 5b00 0000 0800 0000 0000 0000  W...[...........
-00000230: 7265 7175 6573 7473 5d00 0000 6c00 0000  requests]...l...
-00000240: 1700 0000 0000 0000 6c69 6275 726c 7061  ........liburlpa
-00000250: 7273 6572 2e5f 636f 7265 2e48 6f73 7481  rser._core.Host.
-00000260: 0000 0085 0000 0016 0000 0000 0000 006c  ...............l
-00000270: 6962 7572 6c70 6172 7365 722e 5f63 6f72  iburlparser._cor
-00000280: 652e 5073 6c87 0000 008a 0000 0016 0000  e.Psl...........
-00000290: 0000 0000 006c 6962 7572 6c70 6172 7365  .....liburlparse
-000002a0: 722e 5f63 6f72 652e 5572 6c8c 0000 008f  r._core.Url.....
-000002b0: 0000 001a 0000 0000 0000 006c 6962 7572  ...........libur
-000002c0: 6c70 6172 7365 722e 5f63 6f72 652e 5f5f  lparser._core.__
-000002d0: 646f 635f 5f91 0000 0098 0000 001e 0000  doc__...........
-000002e0: 0000 0000 006c 6962 7572 6c70 6172 7365  .....liburlparse
-000002f0: 722e 5f63 6f72 652e 5f5f 7665 7273 696f  r._core.__versio
-00000300: 6e5f 5f9a 0000 00a5 0000 0000 0000 0000  n__.............
-00000310: 0000 0000 0000 0000 0000 000b 0000 0000  ................
-00000320: 0000 005f 5f6d 6169 6e5f 5f2e 7079 090a  ...__main__.py..
-00000330: bb64 0000 0000 2393 8d30 e638 9f7a 8901  .d....#..0.8.z..
-00000340: 0000 0100 0000 0000 0000 1500 0000 0000  ................
-00000350: 0000 6c69 6275 726c 7061 7273 6572 2e5f  ..liburlparser._
-00000360: 5f6d 6169 6e5f 5f07 0000 0000 0000 0016  _main__.........
-00000370: 0000 0000 0000 005f 5f66 7574 7572 655f  .......__future_
-00000380: 5f2e 616e 6e6f 7461 7469 6f6e 7326 0000  _.annotations&..
-00000390: 0031 0000 0008 0000 0000 0000 0061 7267  .1...........arg
-000003a0: 7061 7273 6533 0000 0042 0000 0003 0000  parse3...B......
-000003b0: 0000 0000 0073 7973 4300 0000 4d00 0000  .....sysC...M...
-000003c0: 1100 0000 0000 0000 6c69 6275 726c 7061  ........liburlpa
-000003d0: 7273 6572 2e48 6f73 745d 0000 0061 0000  rser.Host]...a..
-000003e0: 0010 0000 0000 0000 006c 6962 7572 6c70  .........liburlp
-000003f0: 6172 7365 722e 5572 6c63 0000 0066 0000  arser.Urlc...f..
-00000400: 0014 0000 0000 0000 006c 6962 7572 6c70  .........liburlp
-00000410: 6172 7365 722e 5f5f 646f 635f 5f68 0000  arser.__doc__h..
-00000420: 006f 0000 0018 0000 0000 0000 006c 6962  .o...........lib
-00000430: 7572 6c70 6172 7365 722e 5f5f 7665 7273  urlparser.__vers
-00000440: 696f 6e5f 5f71 0000 007c 0000 0000 0000  ion__q...|......
+000000a0: 696f 6e73 2600 0000 3100 0000 0800 0000  ions&...1.......
+000000b0: 0000 0000 6172 6770 6172 7365 3300 0000  ....argparse3...
+000000c0: 4200 0000 0300 0000 0000 0000 7379 7343  B...........sysC
+000000d0: 0000 004d 0000 0011 0000 0000 0000 006c  ...M...........l
+000000e0: 6962 7572 6c70 6172 7365 722e 486f 7374  iburlparser.Host
+000000f0: 5d00 0000 6100 0000 1000 0000 0000 0000  ]...a...........
+00000100: 6c69 6275 726c 7061 7273 6572 2e55 726c  liburlparser.Url
+00000110: 6300 0000 6600 0000 1400 0000 0000 0000  c...f...........
+00000120: 6c69 6275 726c 7061 7273 6572 2e5f 5f64  liburlparser.__d
+00000130: 6f63 5f5f 6800 0000 6f00 0000 1800 0000  oc__h...o.......
+00000140: 0000 0000 6c69 6275 726c 7061 7273 6572  ....liburlparser
+00000150: 2e5f 5f76 6572 7369 6f6e 5f5f 7100 0000  .__version__q...
+00000160: 7c00 0000 0000 0000 0000 0000 0000 0000  |...............
+00000170: 0000 0000 0b00 0000 0000 0000 5f5f 696e  ............__in
+00000180: 6974 5f5f 2e70 7930 23bd 6400 0000 001f  it__.py0#.d.....
+00000190: 41dc 3791 79d1 8289 0100 0001 0000 0000  A.7.y...........
+000001a0: 0000 0015 0000 0000 0000 006c 6962 7572  ...........libur
+000001b0: 6c70 6172 7365 722e 5f5f 696e 6974 5f5f  lparser.__init__
+000001c0: 0600 0000 0000 0000 1600 0000 0000 0000  ................
+000001d0: 5f5f 6675 7475 7265 5f5f 2e61 6e6e 6f74  __future__.annot
+000001e0: 6174 696f 6e73 1700 0000 2200 0000 1600  ations....".....
+000001f0: 0000 0000 0000 6c69 6275 726c 7061 7273  ......liburlpars
+00000200: 6572 2e63 6f72 652e 486f 7374 3600 0000  er.core.Host6...
+00000210: 3a00 0000 1500 0000 0000 0000 6c69 6275  :...........libu
+00000220: 726c 7061 7273 6572 2e63 6f72 652e 5572  rlparser.core.Ur
+00000230: 6c3c 0000 003f 0000 0019 0000 0000 0000  l<...?..........
+00000240: 006c 6962 7572 6c70 6172 7365 722e 636f  .liburlparser.co
+00000250: 7265 2e5f 5f64 6f63 5f5f 4100 0000 4800  re.__doc__A...H.
+00000260: 0000 1d00 0000 0000 0000 6c69 6275 726c  ..........liburl
+00000270: 7061 7273 6572 2e63 6f72 652e 5f5f 7665  parser.core.__ve
+00000280: 7273 696f 6e5f 5f4a 0000 0055 0000 0015  rsion__J...U....
+00000290: 0000 0000 0000 006c 6962 7572 6c70 6172  .......liburlpar
+000002a0: 7365 722e 636f 7265 2e70 736c 5700 0000  ser.core.pslW...
+000002b0: 5a00 0000 0000 0000 0000 0000 0000 0000  Z...............
+000002c0: 0000 0000 0700 0000 0000 0000 636f 7265  ............core
+000002d0: 2e70 7930 23bd 6400 0000 001f 41dc 3791  .py0#.d.....A.7.
+000002e0: 79d1 8289 0100 0001 0000 0000 0000 0011  y...............
+000002f0: 0000 0000 0000 006c 6962 7572 6c70 6172  .......liburlpar
+00000300: 7365 722e 636f 7265 0900 0000 0000 0000  ser.core........
+00000310: 1600 0000 0000 0000 5f5f 6675 7475 7265  ........__future
+00000320: 5f5f 2e61 6e6e 6f74 6174 696f 6e73 2600  __.annotations&.
+00000330: 0000 3100 0000 0800 0000 0000 0000 7761  ..1...........wa
+00000340: 726e 696e 6773 3300 0000 4200 0000 0c00  rnings3...B.....
+00000350: 0000 0000 0000 7061 7468 6c69 622e 5061  ......pathlib.Pa
+00000360: 7468 5700 0000 5b00 0000 0800 0000 0000  thW...[.........
+00000370: 0000 7265 7175 6573 7473 5d00 0000 6c00  ..requests]...l.
+00000380: 0000 1700 0000 0000 0000 6c69 6275 726c  ..........liburl
+00000390: 7061 7273 6572 2e5f 636f 7265 2e48 6f73  parser._core.Hos
+000003a0: 7481 0000 0085 0000 0016 0000 0000 0000  t...............
+000003b0: 006c 6962 7572 6c70 6172 7365 722e 5f63  .liburlparser._c
+000003c0: 6f72 652e 5073 6c87 0000 008a 0000 0016  ore.Psl.........
+000003d0: 0000 0000 0000 006c 6962 7572 6c70 6172  .......liburlpar
+000003e0: 7365 722e 5f63 6f72 652e 5572 6c8c 0000  ser._core.Url...
+000003f0: 008f 0000 001a 0000 0000 0000 006c 6962  .............lib
+00000400: 7572 6c70 6172 7365 722e 5f63 6f72 652e  urlparser._core.
+00000410: 5f5f 646f 635f 5f91 0000 0098 0000 001e  __doc__.........
+00000420: 0000 0000 0000 006c 6962 7572 6c70 6172  .......liburlpar
+00000430: 7365 722e 5f63 6f72 652e 5f5f 7665 7273  ser._core.__vers
+00000440: 696f 6e5f 5f9a 0000 00a5 0000 0000 0000  ion__...........
 00000450: 0000 0000 0000 0000 0000 0000 00         .............
```

### Comparing `liburlparser-1.0.2/CMakeLists.txt` & `liburlparser-1.1.0/CMakeLists.txt`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/LICENSE` & `liburlparser-1.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/README.md` & `liburlparser-1.1.0/README.md`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/conda.recipe/meta.yaml` & `liburlparser-1.1.0/conda.recipe/meta.yaml`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/docs/images/logo/liburlparser-logo-1.svg` & `liburlparser-1.1.0/docs/images/logo/liburlparser-logo-1.svg`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/docs/images/logo/liburlparser-logo-2.svg` & `liburlparser-1.1.0/docs/images/logo/liburlparser-logo-2.svg`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/examples/common.h` & `liburlparser-1.1.0/examples/common.h`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/examples/main.cpp` & `liburlparser-1.1.0/examples/main.cpp`

 * *Files 10% similar despite different names*

```diff
@@ -69,9 +69,14 @@
     show_attr(url, query);
     show_attr(url, port);
     show_attr(url, fragment);
     show_attr(url, userinfo);
     show_attr(url, params);
     show_attr(url, abspath);
     //
+
+    show(TLD::Url("http://www.google.com").subdomain());
+    show(TLD::Url("http://www.google.com").domain());
+    show(TLD::Url("http://www.google.com", true).subdomain());
+    show(TLD::Url("http://www.google.com", true).domain());
     return 0;
 }
```

### Comparing `liburlparser-1.0.2/include/urlparser.h` & `liburlparser-1.1.0/include/urlparser.h`

 * *Files 13% similar despite different names*

```diff
@@ -6,26 +6,27 @@
 #include <vector>
 
 #ifndef PUBLIC_SUFFIX_LIST_DAT
 #define PUBLIC_SUFFIX_LIST_DAT "public_suffix_list.dat"
 #endif
 
 namespace TLD {
+constexpr bool DEFAULT_IGNORE_WWW = false;
 
 using QueryParams = std::vector<std::string>;
 
 class Host;
 class Url {
    public:
     static bool isPslLoaded() noexcept;
     static std::string extractHost(const std::string& url) noexcept;
 
 
    public:
-    Url(const std::string& url);
+    Url(const std::string& url, const bool ignore_www = DEFAULT_IGNORE_WWW);
     Url(const Url& url);
     Url(Url&& url);
     ~Url();
 
     Url& operator=(const Url&);
     Url& operator=(Url&&);
 
@@ -48,21 +49,21 @@
     class Impl;
     Impl* impl;
     Url(const Impl& url_impl);
 };
 
 class Host {
    public:
-    static Host fromUrl(const std::string& url);
+    static Host fromUrl(const std::string& url, const bool ignore_www = DEFAULT_IGNORE_WWW);
     static void loadPslFromPath(const std::string& filepath);
     static void loadPslFromString(const std::string& filestr);
     static bool isPslLoaded() noexcept;
 
    public:
-    Host(const std::string& host);
+    Host(const std::string& host, const bool ignore_www = DEFAULT_IGNORE_WWW);
     Host(const Host& host);
     Host(Host&& host);
     ~Host();
 
     Host& operator=(const Host&);
     Host& operator=(Host&&);
```

### Comparing `liburlparser-1.0.2/pyproject.toml` & `liburlparser-1.1.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 #requires = ["scikit-build-core>=0.3.3", "nanobind==1.4.0"]
 requires = ["scikit-build-core==0.4.6", "nanobind==1.4.0"]
 build-backend = "scikit_build_core.build"
 
 
 [project]
 name = "liburlparser"
-version = "1.0.2"
+version = "1.1.0"
 description="Fastest Url parser in the world"
 readme = "README.md"
 authors = [
   { name = "Mohammad Raziei", email = "mohammadraziei1375@gmail.com" },
 ]
 requires-python = ">=3.8"
 classifiers = [
@@ -50,15 +50,15 @@
 #cmake.args = ["-DSOME_DEFINE=ON", "-DOTHER=OFF"]
 
 [project.optional-dependencies]
 test = ["pytest"]
 
 
 [tool.scikit-build]
-wheel.expand-macos-universal-tags = true
+#wheel.expand-macos-universal-tags = true
 cmake.verbose = false
 
 
 [tool.pytest.ini_options]
 minversion = "6.0"
 addopts = ["-ra", "--showlocals", "--strict-markers", "--strict-config"]
 xfail_strict = true
@@ -107,10 +107,9 @@
 ]
 flake8-unused-arguments.ignore-variadic-names = true
 isort.required-imports = ["from __future__ import annotations"]
 
 [tool.ruff.per-file-ignores]
 "tests/**" = ["F841", "ARG001", "PT004"]
 "src/**/__main__.py" = ["T20"]
-#"src/**/__init__.py" = ["EXE"]
 "src/**/core.py" = ["ARG001", "F401"]
```

### Comparing `liburlparser-1.0.2/src/binding/main.cpp` & `liburlparser-1.1.0/src/binding/main.cpp`

 * *Files 8% similar despite different names*

```diff
@@ -5,14 +5,15 @@
 #include <string>
 #include "urlparser.h"
 
 #define STRINGIFY(x) #x
 #define MACRO_STRINGIFY(x) STRINGIFY(x)
 
 namespace nb = nanobind;
+using namespace nb::literals;
 
 class Psl{
 public:
     Psl() {};
     std::string url() const {return PUBLIC_SUFFIX_LIST_URL;}
     std::string filename() const {return PUBLIC_SUFFIX_LIST_DAT;}
     void loadFromPath(const std::string& filename) {TLD::Host::loadPslFromPath(filename);}
@@ -72,22 +73,14 @@
     return host_to_dict_minimal(TLD::Host::fromUrl(url));
 }
 inline nb::dict extract(const std::string& host){
     return host_to_dict_minimal(TLD::Host(host));
 }
 
 NB_MODULE(_core, m) {
-//    try{
-//        if (not TLD::Host::isPslLoaded())
-//            TLD::Host::loadPslFromPath(PUBLIC_SUFFIX_LIST_DAT);
-//    }
-//    catch(const std::invalid_argument&) {
-//
-//    }
-
     m.doc() = R"pbdoc(
         nanobind example plugin
         -----------------------
 
         .. currentmodule:: liburlparser
 
         .. autosummary::
@@ -96,36 +89,36 @@
            Url
            Host
     )pbdoc";
     //
     nb::class_<TLD::Host> Host(m, "Host");
     nb::class_<TLD::Url> Url(m, "Url");
 
-    Host.def(nb::init<const std::string&>())
-        .def_static("from_url", &TLD::Host::fromUrl)
-        .def_static("extract_from_url", extract_from_url)
-        .def_static("extract", extract)
+    Host.def(nb::init<const std::string&, const bool>(), nb::arg("hoststr"), nb::arg("ignore_www") = false)
+        .def_static("from_url", &TLD::Host::fromUrl, nb::arg("urlstr"), nb::arg("ignore_www") = false)
+        .def_static("extract_from_url", extract_from_url, nb::arg("urlstr"))
+        .def_static("extract", extract, nb::arg("urlstr"))
         .def_static("load_psl_from_path", &TLD::Host::loadPslFromPath,
                     nb::arg("filepath"))
         .def_static("load_psl_from_string", &TLD::Host::loadPslFromString,
-                    nb::arg("filestr"))
+                    nb::arg("string"))
         .def_static("is_psl_loaded", &TLD::Host::isPslLoaded)
         .def_prop_ro("subdomain", &TLD::Host::subdomain)
         .def_prop_ro("domain", &TLD::Host::domain)
         .def_prop_ro("domain_name", &TLD::Host::domainName)
         .def_prop_ro("suffix", &TLD::Host::suffix)
         .def("to_dict", host_to_dict)
         .def("to_json", host_to_json)
         .def("__str__", &TLD::Host::str)
         .def("__repr__", [](const TLD::Host& host) {
             return "<Host :'" + host.str() + "'>";
         });
 
-    Url.def(nb::init<const std::string&>())
-        .def_static("extract_host", &TLD::Url::extractHost)
+    Url.def(nb::init<const std::string&, const bool>(), nb::arg("urlstr"), nb::arg("ignore_www") = false)
+        .def_static("extract_host", &TLD::Url::extractHost, nb::arg("urlstr"))
         .def_prop_ro("protocol", &TLD::Url::protocol)
         .def_prop_ro("userinfo", &TLD::Url::userinfo)
         .def_prop_ro("host", &TLD::Url::host)
         .def_prop_ro("subdomain", &TLD::Url::subdomain)
         .def_prop_ro("domain", &TLD::Url::domain)
         .def_prop_ro("domain_name", &TLD::Url::domainName)
         .def_prop_ro("suffix", &TLD::Url::suffix)
@@ -142,16 +135,16 @@
 
     nb::class_<Psl> psl(m, "Psl", nb::dynamic_attr());
 
     psl.def(nb::init<>())
        .def_prop_ro("url", &Psl::url)
        .def_prop_ro("filename", &Psl::filename)
        .def("is_loaded", &Psl::isLoaded, "check whether psl is loaded or not")
-       .def("load_from_path", &Psl::loadFromPath, "load PSL from path")
-       .def("load_from_string", &Psl::loadFromString, "load PSL from string")
+       .def("load_from_path", &Psl::loadFromPath, nb::arg("filepath"), "load PSL from path")
+       .def("load_from_string", &Psl::loadFromString, nb::arg("string"), "load PSL from string")
        .def("__repr__", [](const Psl& p) -> std::string {
             return std::string("<PSL : ") + (p.isLoaded() ? "loaded" : "not loaded") + ">";
         });
 
 #ifdef VERSION_INFO
     m.attr("__version__") = MACRO_STRINGIFY(VERSION_INFO);
 #else
```

### Comparing `liburlparser-1.0.2/src/liburlparser/__main__.py` & `liburlparser-1.1.0/src/liburlparser/__main__.py`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/src/liburlparser/core.py` & `liburlparser-1.1.0/src/liburlparser/core.py`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/src/psl.cpp` & `liburlparser-1.1.0/src/psl.cpp`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/src/psl.h` & `liburlparser-1.1.0/src/psl.h`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/src/url.cpp` & `liburlparser-1.1.0/src/url.cpp`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/src/url.h` & `liburlparser-1.1.0/src/url.h`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/src/urlparser.cpp` & `liburlparser-1.1.0/src/urlparser.cpp`

 * *Files 5% similar despite different names*

```diff
@@ -11,33 +11,32 @@
 namespace URL = Url;
 
 /// define Impl class:
 class TLD::Url::Impl : public URL::Url {
     friend class TLD::Url;
 
    public:
-    Impl(const std::string& url);
+    Impl(const std::string& url, const bool ignore_www);
     ~Impl() {}
     std::string str() const noexcept;
     const TLD::Host& host() const noexcept;
 
    protected:
     TLD::Host host_obj;
 };
 
 class TLD::Host::Impl {
     friend class TLD::Host;
-
    public:
     static void loadPslFromPath(const std::string& filepath);
     static void loadPslFromString(const std::string& filestr);
     static bool isPslLoaded() noexcept;
 
    public:
-    Impl(const std::string& host);
+    Impl(const std::string& host, const bool ignore_www);
     ~Impl() {}
 
     const std::string& domain() const noexcept;
     std::string domainName() const noexcept;
     const std::string& subdomain() const noexcept;
     const std::string& suffix() const noexcept;
     const std::string& fulldomain() const noexcept;
@@ -108,38 +107,51 @@
     return TLD::Host::Impl::isPslLoaded();
 }
 bool TLD::Url::isPslLoaded() noexcept {
     return TLD::Host::isPslLoaded();
 }
 ////////////////////////////////////////////////////////////////////
 
-TLD::Host::Impl::Impl(const std::string& host_) : host_(host_) {
+TLD::Host::Impl::Impl(const std::string& host_, const bool ignore_www) : host_(host_) {
     this->suffix_ = TLD::Host::Impl::psl->getTLD(host_);
     size_t suffix_pos = host_.rfind("." + suffix_);
+    size_t subdomain_pos = 0;
     if (suffix_pos == std::string::npos || suffix_pos < 1)
         return;
-    this->domain_ = host_.substr(0, suffix_pos);
+    domain_ = host_.substr(0, suffix_pos);
     size_t domain_pos = domain_.find_last_of(".");
     if (domain_pos != std::string::npos) {
-        this->subdomain_ = domain_.substr(0, domain_pos);
-        this->domain_ = domain_.substr(domain_pos + 1);
+        if (ignore_www) {
+            size_t www_pos = domain_.find("www.");
+            if (www_pos != 0) {
+                if (www_pos != std::string::npos)
+                    return;
+            } else {
+                subdomain_pos = 4;
+            }
+        }
+        if (subdomain_pos < domain_pos)
+            subdomain_ = domain_.substr(subdomain_pos, domain_pos - subdomain_pos);
+        domain_ = domain_.substr(domain_pos + 1);
     }
 }
-TLD::Host::Host(const std::string& url) : impl(new Impl(url)) {}
+TLD::Host::Host(const std::string& url, const bool ignore_www) : impl(new Impl(url, ignore_www)) {}
 TLD::Host::Host(TLD::Host&& host) : impl(host.impl) {
     host.impl = nullptr;
 }
 TLD::Host::~Host() {
     delete impl;
 }
 
-TLD::Url::Impl::Impl(const std::string& url)
-    : URL::Url(url), host_obj(this->host_) {}
+TLD::Url::Impl::Impl(const std::string& url, const bool ignore_www)
+    : URL::Url(url), host_obj(TLD::Host{this->host_, ignore_www}) {}
 // TLD::Url::Impl::~Impl() {}
-TLD::Url::Url(const std::string& url) : impl(new Impl(url)) {}
+TLD::Url::Url(const std::string& url, const bool ignore_www) : impl(new Impl(url, ignore_www)) {
+//    std::cout << "++++++++++++++++++++++++++" << std::endl;
+}
 TLD::Url::Url(TLD::Url&& url) : impl(url.impl) {
     url.impl = nullptr;
 }
 TLD::Url::~Url() {
     delete impl;
 }
 
@@ -212,16 +224,16 @@
 inline std::string TLD::Url::Impl::str() const noexcept {
     return URL::Url::str();
 }
 std::string TLD::Url::str() const noexcept {
     return impl->str();
 }
 
-TLD::Host TLD::Host::fromUrl(const std::string& url) {
-    return TLD::Host(TLD::Url::extractHost(url));// TODO :  write a faster way for finding host_ from url
+TLD::Host TLD::Host::fromUrl(const std::string& url, const bool ignore_www) {
+    return TLD::Host(TLD::Url::extractHost(url), ignore_www);// TODO :  write a faster way for finding host_ from url
 }
 
 TLD::Host::Host(const TLD::Host& host) : impl(new Impl(*host.impl)) {}
 
 ////////////////////////
 
 const std::string& TLD::Url::protocol() const noexcept {
```

### Comparing `liburlparser-1.0.2/tests/test.cpp` & `liburlparser-1.1.0/tests/test.cpp`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/tests/test_extra.py` & `liburlparser-1.1.0/tests/test_extra.py`

 * *Files identical despite different names*

### Comparing `liburlparser-1.0.2/tests/test_host.py` & `liburlparser-1.1.0/tests/test_host.py`

 * *Files 13% similar despite different names*

```diff
@@ -10,12 +10,12 @@
 
 with (Path(__file__).parent / "data" / "host_data.csv").open("r") as f:
     reader = csv.DictReader(f)
     host_data_list = list(reader)
 
 @pytest.mark.parametrize("host_data", host_data_list)
 def test_host(host_data):
-    host = Host.from_url(host_data["url"])
+    host = Host.from_url(host_data["url"], bool(host_data["ignore_www"]))
     assert str(host) == host_data["host"]
     assert host.domain == host_data["domain"]
     assert host.domain_name == host_data["domain_name"]
     assert host.suffix == host_data["suffix"]
```

### Comparing `liburlparser-1.0.2/tests/test_url.py` & `liburlparser-1.1.0/tests/test_url.py`

 * *Files 7% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 
 with (Path(__file__).parent / "data" / "url_data.csv").open("r") as f:
     reader = csv.DictReader(f)
     url_data_list = list(reader)
 
 @pytest.mark.parametrize("url_data", url_data_list)
 def test_url(url_data):
-    url = Url(url_data["url"])
+    url = Url(url_data["url"], bool(url_data["ignore_www"]))
     assert url.protocol == url_data["protocol"]
     assert url.userinfo == url_data["userinfo"]
     assert str(url.host) == url_data["host"]
     assert url.domain == url_data["domain"]
     assert url.domain_name == url_data["domain_name"]
     assert url.suffix == url_data["suffix"]
     assert url.port == int(url_data["port"])
```

### Comparing `liburlparser-1.0.2/PKG-INFO` & `liburlparser-1.1.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: liburlparser
-Version: 1.0.2
+Version: 1.1.0
 Summary: Fastest Url parser in the world
 Author-Email: Mohammad Raziei <mohammadraziei1375@gmail.com>
 Classifier: Development Status :: 4 - Beta
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: C++
 Classifier: Programming Language :: Python :: Implementation :: CPython
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: liburlparser Version: 1.0.2 Summary: Fastest Url
+Metadata-Version: 2.1 Name: liburlparser Version: 1.1.0 Summary: Fastest Url
 parser in the world Author-Email: Mohammad Raziei
 gmail.com> Classifier: Development Status :: 4 - Beta Classifier: License ::
 OSI Approved :: MIT License Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: C++ Classifier: Programming Language ::
 Python :: Implementation :: CPython Classifier: Programming Language :: Python
 :: 3 :: Only Classifier: Programming Language :: Python :: 3.8 Classifier:
 Programming Language :: Python :: 3.9 Classifier: Programming Language ::
```

