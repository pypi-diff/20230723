# Comparing `tmp/Print_Tricks_And_More_Alpha-0.3.80-py3-none-any.whl.zip` & `tmp/Print_Tricks_And_More_Alpha-0.3.82-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 154338 bytes, number of entries: 7
--rw-rw-rw-  2.0 fat   316905 b- defN 23-Jul-23 07:45 print_tricks/__init__.py
+Zip file size: 154349 bytes, number of entries: 7
+-rw-rw-rw-  2.0 fat   316905 b- defN 23-Jul-23 08:11 print_tricks/__init__.py
 -rw-rw-rw-  2.0 fat   315963 b- defN 23-Jul-23 05:23 print_tricks/print_tricks_debugger.py
--rw-rw-rw-  2.0 fat       36 b- defN 23-Jul-23 03:50 print_tricks/test.py
--rw-rw-rw-  2.0 fat      464 b- defN 23-Jul-23 07:45 Print_Tricks_And_More_Alpha-0.3.80.dist-info/METADATA
--rw-rw-rw-  2.0 fat       92 b- defN 23-Jul-23 07:45 Print_Tricks_And_More_Alpha-0.3.80.dist-info/WHEEL
--rw-rw-rw-  2.0 fat       13 b- defN 23-Jul-23 07:45 Print_Tricks_And_More_Alpha-0.3.80.dist-info/top_level.txt
--rw-rw-r--  2.0 fat      635 b- defN 23-Jul-23 07:45 Print_Tricks_And_More_Alpha-0.3.80.dist-info/RECORD
-7 files, 634108 bytes uncompressed, 153198 bytes compressed:  75.8%
+-rw-rw-rw-  2.0 fat       53 b- defN 23-Jul-23 08:10 print_tricks/test.py
+-rw-rw-rw-  2.0 fat      464 b- defN 23-Jul-23 08:11 Print_Tricks_And_More_Alpha-0.3.82.dist-info/METADATA
+-rw-rw-rw-  2.0 fat       92 b- defN 23-Jul-23 08:11 Print_Tricks_And_More_Alpha-0.3.82.dist-info/WHEEL
+-rw-rw-rw-  2.0 fat       13 b- defN 23-Jul-23 08:11 Print_Tricks_And_More_Alpha-0.3.82.dist-info/top_level.txt
+-rw-rw-r--  2.0 fat      635 b- defN 23-Jul-23 08:11 Print_Tricks_And_More_Alpha-0.3.82.dist-info/RECORD
+7 files, 634125 bytes uncompressed, 153209 bytes compressed:  75.8%
```

## zipnote {}

```diff
@@ -3,20 +3,20 @@
 
 Filename: print_tricks/print_tricks_debugger.py
 Comment: 
 
 Filename: print_tricks/test.py
 Comment: 
 
-Filename: Print_Tricks_And_More_Alpha-0.3.80.dist-info/METADATA
+Filename: Print_Tricks_And_More_Alpha-0.3.82.dist-info/METADATA
 Comment: 
 
-Filename: Print_Tricks_And_More_Alpha-0.3.80.dist-info/WHEEL
+Filename: Print_Tricks_And_More_Alpha-0.3.82.dist-info/WHEEL
 Comment: 
 
-Filename: Print_Tricks_And_More_Alpha-0.3.80.dist-info/top_level.txt
+Filename: Print_Tricks_And_More_Alpha-0.3.82.dist-info/top_level.txt
 Comment: 
 
-Filename: Print_Tricks_And_More_Alpha-0.3.80.dist-info/RECORD
+Filename: Print_Tricks_And_More_Alpha-0.3.82.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## print_tricks/__init__.py

```diff
@@ -2,15 +2,15 @@
 00000010: 2323 2323 2323 2323 2323 2323 2323 2323  ################
 00000020: 2323 2323 2323 2323 2323 2323 2323 2323  ################
 00000030: 2323 2323 2323 2323 2323 2323 2323 2323  ################
 00000040: 2323 2323 2323 2323 2323 2323 0d0a 2323  ############..##
 00000050: 2323 2323 2323 2323 2323 2323 2323 2323  ################
 00000060: 2323 2323 2323 2050 7269 6e74 2054 7269  ###### Print Tri
 00000070: 636b 7320 2620 4d6f 7265 202d 2076 6572  cks & More - ver
-00000080: 7369 6f6e 2030 2e33 2e38 3020 776f 726b  sion 0.3.80 work
+00000080: 7369 6f6e 2030 2e33 2e38 3220 776f 726b  sion 0.3.82 work
 00000090: 696e 6720 2323 2323 2323 0d0a 2323 2323  ing ######..####
 000000a0: 2323 2323 2323 2323 2323 2323 2323 2323  ################
 000000b0: 2323 2323 2323 2323 2323 2323 2323 2323  ################
 000000c0: 2323 2323 2323 2323 2323 2323 2323 2323  ################
 000000d0: 2323 2323 2323 2323 2323 2323 2323 2323  ################
 000000e0: 2323 2323 2323 2323 0d0a 2323 2323 2323  ########..######
 000000f0: 2323 2323 2323 2323 2323 2323 2323 2323  ################
```

## print_tricks/test.py

```diff
@@ -1,2 +1,4 @@
 from print_tricks import pt
 pt(1)
+g=32.322
+pt(g)
```

## Comparing `Print_Tricks_And_More_Alpha-0.3.80.dist-info/RECORD` & `Print_Tricks_And_More_Alpha-0.3.82.dist-info/RECORD`

 * *Files 24% similar despite different names*

```diff
@@ -1,7 +1,7 @@
-print_tricks/__init__.py,sha256=yY_JrMk76AMWDB28EMrmsF49NpDWfKtFW-BTpLoyZc4,316905
+print_tricks/__init__.py,sha256=XOiItaE1dBERH6eKY5ZRJdhjsmiUmfMrAx5EMPkb6-E,316905
 print_tricks/print_tricks_debugger.py,sha256=uU8klZ9Wfk78hGPOagRU5YUHrfAM1Fa6zW0nRZdFk8g,315963
-print_tricks/test.py,sha256=49xOgXg_atzJToKF5_3I0Q0KeDCtKampHMXjhVz_AoU,36
-Print_Tricks_And_More_Alpha-0.3.80.dist-info/METADATA,sha256=HBkleDVILrNOy3yXNUVvN3rTljLqcKjNo6k3m_YjcVk,464
-Print_Tricks_And_More_Alpha-0.3.80.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
-Print_Tricks_And_More_Alpha-0.3.80.dist-info/top_level.txt,sha256=uzlOhEwH-SCQUJVQNvtOP4goM16yOvUeDn6PgpMogdU,13
-Print_Tricks_And_More_Alpha-0.3.80.dist-info/RECORD,,
+print_tricks/test.py,sha256=IUgC-IwzbdjiJ39dE6uoDzS8qQr45nkbGsVMESTDZlw,53
+Print_Tricks_And_More_Alpha-0.3.82.dist-info/METADATA,sha256=Rdmwr16lgQ5R3g3YabE5fhGtj-fXFpdGcd-gzYimBxI,464
+Print_Tricks_And_More_Alpha-0.3.82.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
+Print_Tricks_And_More_Alpha-0.3.82.dist-info/top_level.txt,sha256=uzlOhEwH-SCQUJVQNvtOP4goM16yOvUeDn6PgpMogdU,13
+Print_Tricks_And_More_Alpha-0.3.82.dist-info/RECORD,,
```

