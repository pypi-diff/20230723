# Comparing `tmp/sqlite_hello-0.1.0a50-py3-none-manylinux_2_17_x86_64.manylinux2014_x86_64.manylinux1_x86_64.whl.zip` & `tmp/sqlite_hello-0.1.0a52-py3-none-manylinux_2_17_x86_64.manylinux2014_x86_64.manylinux1_x86_64.whl.zip`

## zipinfo {}

```diff
@@ -1,11 +1,11 @@
-Zip file size: 8399 bytes, number of entries: 9
--rwxr-xr-x  2.0 unx    15784 b- defN 23-May-31 22:00 noop.cpython-311-x86_64-linux-gnu.so
--rw-r--r--  2.0 unx      305 b- defN 23-May-31 22:00 sqlite_hello/__init__.py
--rwxr-xr-x  2.0 unx    15856 b- defN 23-May-31 22:00 sqlite_hello/hello0.so
--rwxr-xr-x  2.0 unx    15848 b- defN 23-May-31 22:00 sqlite_hello/hola0.so
--rw-r--r--  2.0 unx       80 b- defN 23-May-31 22:00 sqlite_hello/version.py
--rw-r--r--  2.0 unx      507 b- defN 23-May-31 22:00 sqlite_hello-0.1.0a50.dist-info/METADATA
--rw-r--r--  2.0 unx      105 b- defN 23-May-31 22:00 sqlite_hello-0.1.0a50.dist-info/WHEEL
--rw-r--r--  2.0 unx       18 b- defN 23-May-31 22:00 sqlite_hello-0.1.0a50.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      741 b- defN 23-May-31 22:00 sqlite_hello-0.1.0a50.dist-info/RECORD
-9 files, 49244 bytes uncompressed, 7121 bytes compressed:  85.5%
+Zip file size: 8401 bytes, number of entries: 9
+-rwxr-xr-x  2.0 unx    15784 b- defN 23-Jul-23 19:05 noop.cpython-311-x86_64-linux-gnu.so
+-rw-r--r--  2.0 unx      305 b- defN 23-Jul-23 19:04 sqlite_hello/__init__.py
+-rwxr-xr-x  2.0 unx    15856 b- defN 23-Jul-23 19:04 sqlite_hello/hello0.so
+-rwxr-xr-x  2.0 unx    15848 b- defN 23-Jul-23 19:04 sqlite_hello/hola0.so
+-rw-r--r--  2.0 unx       80 b- defN 23-Jul-23 19:04 sqlite_hello/version.py
+-rw-r--r--  2.0 unx      507 b- defN 23-Jul-23 19:05 sqlite_hello-0.1.0a52.dist-info/METADATA
+-rw-r--r--  2.0 unx      105 b- defN 23-Jul-23 19:05 sqlite_hello-0.1.0a52.dist-info/WHEEL
+-rw-r--r--  2.0 unx       18 b- defN 23-Jul-23 19:05 sqlite_hello-0.1.0a52.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      741 b- defN 23-Jul-23 19:05 sqlite_hello-0.1.0a52.dist-info/RECORD
+9 files, 49244 bytes uncompressed, 7123 bytes compressed:  85.5%
```

## zipnote {}

```diff
@@ -9,20 +9,20 @@
 
 Filename: sqlite_hello/hola0.so
 Comment: 
 
 Filename: sqlite_hello/version.py
 Comment: 
 
-Filename: sqlite_hello-0.1.0a50.dist-info/METADATA
+Filename: sqlite_hello-0.1.0a52.dist-info/METADATA
 Comment: 
 
-Filename: sqlite_hello-0.1.0a50.dist-info/WHEEL
+Filename: sqlite_hello-0.1.0a52.dist-info/WHEEL
 Comment: 
 
-Filename: sqlite_hello-0.1.0a50.dist-info/top_level.txt
+Filename: sqlite_hello-0.1.0a52.dist-info/top_level.txt
 Comment: 
 
-Filename: sqlite_hello-0.1.0a50.dist-info/RECORD
+Filename: sqlite_hello-0.1.0a52.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## noop.cpython-311-x86_64-linux-gnu.so

 * *File has been modified after NT_GNU_BUILD_ID has been applied.*

### readelf --wide --dynamic {}

```diff
@@ -1,11 +1,11 @@
 
 Dynamic section at offset 0x2e80 contains 18 entries:
   Tag        Type                         Name/Value
- 0x000000000000001d (RUNPATH)            Library runpath: [/opt/hostedtoolcache/Python/3.11.3/x64/lib]
+ 0x000000000000001d (RUNPATH)            Library runpath: [/opt/hostedtoolcache/Python/3.11.4/x64/lib]
  0x000000000000000c (INIT)               0x1000
  0x000000000000000d (FINI)               0x10fc
  0x0000000000000019 (INIT_ARRAY)         0x3e70
  0x000000000000001b (INIT_ARRAYSZ)       8 (bytes)
  0x000000000000001a (FINI_ARRAY)         0x3e78
  0x000000000000001c (FINI_ARRAYSZ)       8 (bytes)
  0x000000006ffffef5 (GNU_HASH)           0x2b8
```

### readelf --wide --notes {}

```diff
@@ -1,8 +1,8 @@
 
 Displaying notes found in: .note.gnu.property
   Owner                Data size 	Description
   GNU                  0x00000010	NT_GNU_PROPERTY_TYPE_0	      Properties: x86 feature: IBT, SHSTK
 
 Displaying notes found in: .note.gnu.build-id
   Owner                Data size 	Description
-  GNU                  0x00000014	NT_GNU_BUILD_ID (unique build ID bitstring)	    Build ID: 6e49341f6e718fa8b5e872e0c7ae88529876ca7c
+  GNU                  0x00000014	NT_GNU_BUILD_ID (unique build ID bitstring)	    Build ID: 62b623d49330d9c91f59042f06ad8fa0bb403ca5
```

### strings --all --bytes=8 {}

```diff
@@ -1,12 +1,12 @@
 __gmon_start__
 _ITM_deregisterTMCloneTable
 _ITM_registerTMCloneTable
 __cxa_finalize
-/opt/hostedtoolcache/Python/3.11.3/x64/lib
+/opt/hostedtoolcache/Python/3.11.4/x64/lib
 GCC: (Ubuntu 9.4.0-1ubuntu1~20.04.1) 9.4.0
 GNU C17 9.4.0 -mtune=generic -march=x86-64 -g -O3 -fwrapv -fPIC -fasynchronous-unwind-tables -fstack-protector-strong -fstack-clash-protection -fcf-protection
 /home/runner/work/sqlite-hello/sqlite-hello/bindings/python
 crtstuff.c
 deregister_tm_clones
 __do_global_dtors_aux
 completed.8061
```

### readelf --wide --decompress --hex-dump=.dynstr {}

```diff
@@ -3,9 +3,9 @@
   0x00000350 005f5f67 6d6f6e5f 73746172 745f5f00 .__gmon_start__.
   0x00000360 5f49544d 5f646572 65676973 74657254 _ITM_deregisterT
   0x00000370 4d436c6f 6e655461 626c6500 5f49544d MCloneTable._ITM
   0x00000380 5f726567 69737465 72544d43 6c6f6e65 _registerTMClone
   0x00000390 5461626c 65005f5f 6378615f 66696e61 Table.__cxa_fina
   0x000003a0 6c697a65 002f6f70 742f686f 73746564 lize./opt/hosted
   0x000003b0 746f6f6c 63616368 652f5079 74686f6e toolcache/Python
-  0x000003c0 2f332e31 312e332f 7836342f 6c696200 /3.11.3/x64/lib.
+  0x000003c0 2f332e31 312e342f 7836342f 6c696200 /3.11.4/x64/lib.
```

## sqlite_hello/hello0.so

 * *File has been modified after NT_GNU_BUILD_ID has been applied.*

### readelf --wide --notes {}

```diff
@@ -1,8 +1,8 @@
 
 Displaying notes found in: .note.gnu.property
   Owner                Data size 	Description
   GNU                  0x00000010	NT_GNU_PROPERTY_TYPE_0	      Properties: x86 feature: IBT, SHSTK
 
 Displaying notes found in: .note.gnu.build-id
   Owner                Data size 	Description
-  GNU                  0x00000014	NT_GNU_BUILD_ID (unique build ID bitstring)	    Build ID: d65d4d8072a38c6ff17bfc0c0c0177f2902f0799
+  GNU                  0x00000014	NT_GNU_BUILD_ID (unique build ID bitstring)	    Build ID: 0e89593460094c679b6416727f82515b0bee9882
```

### strings --all --bytes=8 {}

```diff
@@ -1,15 +1,15 @@
 __gmon_start__
 _ITM_deregisterTMCloneTable
 _ITM_registerTMCloneTable
 __cxa_finalize
 sqlite3_api
 sqlite3_hello_init
 Hello, %s!
-v0.1.0-alpha.50
+v0.1.0-alpha.52
 hello_version
 GCC: (Ubuntu 9.4.0-1ubuntu1~20.04.1) 9.4.0
 crtstuff.c
 deregister_tm_clones
 __do_global_dtors_aux
 completed.8061
 __do_global_dtors_aux_fini_array_entry
```

### readelf --wide --decompress --string-dump=.rodata {}

```diff
@@ -1,7 +1,7 @@
 
 String dump of section '.rodata':
   [     0]  Hello, %s!
-  [     b]  v0.1.0-alpha.50
+  [     b]  v0.1.0-alpha.52
   [    1b]  hello
   [    21]  hello_version
```

## sqlite_hello/hola0.so

### readelf --wide --notes {}

```diff
@@ -1,8 +1,8 @@
 
 Displaying notes found in: .note.gnu.property
   Owner                Data size 	Description
   GNU                  0x00000010	NT_GNU_PROPERTY_TYPE_0	      Properties: x86 feature: IBT, SHSTK
 
 Displaying notes found in: .note.gnu.build-id
   Owner                Data size 	Description
-  GNU                  0x00000014	NT_GNU_BUILD_ID (unique build ID bitstring)	    Build ID: 14ed66d548e37f30f60af594145d82fffa7f78e3
+  GNU                  0x00000014	NT_GNU_BUILD_ID (unique build ID bitstring)	    Build ID: da510819b9610ca3fb4d7b55d40fd2d96a18b044
```

### strings --all --bytes=8 {}

```diff
@@ -1,15 +1,15 @@
 __gmon_start__
 _ITM_deregisterTMCloneTable
 _ITM_registerTMCloneTable
 __cxa_finalize
 sqlite3_api
 sqlite3_hola_init
 Hola, %s!
-v0.1.0-alpha.50
+v0.1.0-alpha.52
 hola_version
 GCC: (Ubuntu 9.4.0-1ubuntu1~20.04.1) 9.4.0
 crtstuff.c
 deregister_tm_clones
 __do_global_dtors_aux
 completed.8061
 __do_global_dtors_aux_fini_array_entry
```

### readelf --wide --decompress --string-dump=.rodata {}

```diff
@@ -1,7 +1,7 @@
 
 String dump of section '.rodata':
   [     2]  Hola, %s!
-  [     c]  v0.1.0-alpha.50
+  [     c]  v0.1.0-alpha.52
   [    1c]  hola
   [    21]  hola_version
```

## sqlite_hello/version.py

```diff
@@ -1,2 +1,2 @@
-__version__ = "0.1.0-alpha.50"
+__version__ = "0.1.0-alpha.52"
 __version_info__ = tuple(__version__.split("."))
```

