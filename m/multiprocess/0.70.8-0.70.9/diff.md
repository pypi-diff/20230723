# Comparing `tmp/multiprocess-0.70.8.tar.gz` & `tmp/multiprocess-0.70.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, last modified: Thu Jun 27 17:31:36 2019, from Unix
+gzip compressed data, last modified: Sat Sep 28 16:46:02 2019, from Unix
```

## Comparing `multiprocess-0.70.8.tar` & `multiprocess-0.70.9.tar`

### file list

```diff
@@ -1,875 +1,890 @@
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:19:11.000000 multiprocess-0.70.8/
--rw-r--r--   0 mmckerns   (501) staff       (20)      467 2019-06-27 17:17:55.000000 multiprocess-0.70.8/.coveragerc
--rw-r--r--   0 mmckerns   (501) staff       (20)       32 2019-06-27 17:17:55.000000 multiprocess-0.70.8/.gitignore
--rw-r--r--   0 mmckerns   (501) staff       (20)     2769 2019-06-27 17:17:55.000000 multiprocess-0.70.8/.travis.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)    20653 2019-06-27 17:17:55.000000 multiprocess-0.70.8/CHANGES.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1493 2019-06-27 17:17:55.000000 multiprocess-0.70.8/COPYING.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1710 2019-06-27 17:17:55.000000 multiprocess-0.70.8/INSTALL.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1949 2019-06-27 17:17:55.000000 multiprocess-0.70.8/LICENSE
--rw-r--r--   0 mmckerns   (501) staff       (20)      369 2019-06-27 17:17:55.000000 multiprocess-0.70.8/MANIFEST.in
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:31:35.000000 multiprocess-0.70.8/py2.7/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/
--rw-r--r--   0 mmckerns   (501) staff       (20)     4922 2019-06-27 17:17:55.000000 multiprocess-0.70.8/README.md
--rw-r--r--   0 mmckerns   (501) staff       (20)    14383 2019-06-27 17:17:55.000000 multiprocess-0.70.8/setup.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      467 2019-06-27 17:17:55.000000 multiprocess-0.70.8/THANKS.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1939 2019-06-27 17:17:55.000000 multiprocess-0.70.8/tox.ini
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/index.html
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/Modules/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)    17763 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/README_MODS
--rw-r--r--   0 mmckerns   (501) staff       (20)      940 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.8/multiprocess/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    31661 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/connection.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11207 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/context.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/dummy/
--rw-r--r--   0 mmckerns   (501) staff       (20)    11830 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11626 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/heap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    48803 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/managers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    32360 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2565 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/popen_fork.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2227 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/popen_forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2029 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/popen_spawn_posix.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4060 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/popen_spawn_win32.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11899 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11806 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/queues.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9561 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/reduction.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5352 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/resource_sharer.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8374 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/resource_tracker.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    17216 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/shared_memory.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6306 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/sharedctypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9293 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/spawn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11829 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/synchronize.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)    12227 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/util.py
--rw-r--r--   0 mmckerns   (501) staff       (20)   184541 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      479 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/tests/test_multiprocessing_fork.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      394 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/tests/test_multiprocessing_forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11809 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/tests/test_multiprocessing_main_handling.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      279 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/tests/test_multiprocessing_spawn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3061 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/dummy/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1598 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/multiprocess/dummy/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/Modules/_multiprocess/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/Modules/_multiprocess/clinic/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5475 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/Modules/_multiprocess/multiprocess.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     2388 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/Modules/_multiprocess/multiprocess.h
--rw-r--r--   0 mmckerns   (501) staff       (20)     3079 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/Modules/_multiprocess/posixshmem.c
--rw-r--r--   0 mmckerns   (501) staff       (20)    19116 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/Modules/_multiprocess/semaphore.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     4061 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/Modules/_multiprocess/clinic/posixshmem.c.h
--rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/examples/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5745 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/examples/benchmarks.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1587 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/examples/ex_newtype.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7004 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/examples/ex_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/examples/ex_synchronize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/examples/ex_webserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/examples/ex_workers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/CHANGES.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/connection-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/connection-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/connection-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/connection-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/COPYING.html
--rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/header.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/html4css1.css
--rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/index.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/index.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/INSTALL.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/intro.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/intro.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/manager-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/manager-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/pool-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/pool-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/process-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/process-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/processing-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/processing-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/programming-guidelines.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/programming-guidelines.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/proxy-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/proxy-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/queue-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/queue-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/sharedctypes.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/sharedctypes.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/tests.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/tests.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/THANKS.html
--rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.8/doc/version.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/index.html
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/Modules/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)    13753 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/README_MODS
--rw-r--r--   0 mmckerns   (501) staff       (20)      947 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.7/multiprocess/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    31274 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/connection.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10923 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/context.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/dummy/
--rw-r--r--   0 mmckerns   (501) staff       (20)    11780 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8918 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/heap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    40212 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/managers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    26834 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2391 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/popen_fork.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2013 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/popen_forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1921 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/popen_spawn_posix.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3766 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/popen_spawn_win32.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10548 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11703 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/queues.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9410 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/reduction.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5350 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/resource_sharer.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5539 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/semaphore_tracker.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6306 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/sharedctypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8845 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/spawn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11806 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/synchronize.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)    12106 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/util.py
--rw-r--r--   0 mmckerns   (501) staff       (20)   152767 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      479 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/tests/test_multiprocessing_fork.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      388 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/tests/test_multiprocessing_forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11808 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/tests/test_multiprocessing_main_handling.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      279 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/tests/test_multiprocessing_spawn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3058 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/dummy/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1598 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/multiprocess/dummy/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/Modules/_multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5475 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/Modules/_multiprocess/multiprocess.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     2388 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/Modules/_multiprocess/multiprocess.h
--rw-r--r--   0 mmckerns   (501) staff       (20)    18933 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/Modules/_multiprocess/semaphore.c
--rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/examples/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5745 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/examples/benchmarks.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1587 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/examples/ex_newtype.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7004 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/examples/ex_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/examples/ex_synchronize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/examples/ex_webserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/examples/ex_workers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/CHANGES.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/connection-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/connection-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/connection-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/connection-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/COPYING.html
--rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/header.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/html4css1.css
--rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/index.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/index.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/INSTALL.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/intro.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/intro.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/manager-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/manager-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/pool-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/pool-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/process-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/process-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/processing-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/processing-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/programming-guidelines.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/programming-guidelines.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/proxy-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/proxy-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/queue-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/queue-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/sharedctypes.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/sharedctypes.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/tests.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/tests.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/THANKS.html
--rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.7/doc/version.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/index.html
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/Modules/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)    21305 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/README_MODS
--rw-r--r--   0 mmckerns   (501) staff       (20)      947 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.6/multiprocess/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    31050 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/connection.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10917 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/context.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/dummy/
--rw-r--r--   0 mmckerns   (501) staff       (20)     8691 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8319 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/heap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    38193 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/managers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    26059 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2304 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/popen_fork.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1953 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/popen_forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1904 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/popen_spawn_posix.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2999 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/popen_spawn_win32.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9211 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10879 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/queues.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9281 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/reduction.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5325 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/resource_sharer.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5465 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/semaphore_tracker.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6245 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/sharedctypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8860 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/spawn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    12269 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/synchronize.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)    11883 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/util.py
--rw-r--r--   0 mmckerns   (501) staff       (20)   126951 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      479 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/tests/test_multiprocessing_fork.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      394 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/tests/test_multiprocessing_forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11731 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/tests/test_multiprocessing_main_handling.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      279 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/tests/test_multiprocessing_spawn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2896 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/dummy/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1583 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/multiprocess/dummy/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/Modules/_multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5338 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/Modules/_multiprocess/multiprocess.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     2397 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/Modules/_multiprocess/multiprocess.h
--rw-r--r--   0 mmckerns   (501) staff       (20)    18586 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/Modules/_multiprocess/semaphore.c
--rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/examples/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5745 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/examples/benchmarks.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1587 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/examples/ex_newtype.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7004 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/examples/ex_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/examples/ex_synchronize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/examples/ex_webserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/examples/ex_workers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/CHANGES.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/connection-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/connection-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/connection-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/connection-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/COPYING.html
--rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/header.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/html4css1.css
--rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/index.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/index.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/INSTALL.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/intro.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/intro.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/manager-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/manager-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/pool-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/pool-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/process-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/process-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/processing-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/processing-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/programming-guidelines.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/programming-guidelines.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/proxy-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/proxy-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/queue-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/queue-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/sharedctypes.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/sharedctypes.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/tests.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/tests.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/THANKS.html
--rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.6/doc/version.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/index.html
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/Modules/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)    13706 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/README_MODS
--rw-r--r--   0 mmckerns   (501) staff       (20)      947 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.5/multiprocess/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    30931 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/connection.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10677 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/context.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/dummy/
--rw-r--r--   0 mmckerns   (501) staff       (20)     8210 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8325 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/heap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    35963 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/managers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    25819 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2324 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/popen_fork.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1964 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/popen_forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1915 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/popen_spawn_posix.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2998 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/popen_spawn_win32.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9136 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10825 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/queues.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8163 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/reduction.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5318 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/resource_sharer.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4891 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/semaphore_tracker.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6228 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/sharedctypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8912 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/spawn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    12229 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/synchronize.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)    11638 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/util.py
--rw-r--r--   0 mmckerns   (501) staff       (20)   123590 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      176 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/tests/test_multiprocessing_fork.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      182 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/tests/test_multiprocessing_forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11532 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/tests/test_multiprocessing_main_handling.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      177 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/tests/test_multiprocessing_spawn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2896 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/dummy/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1583 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/multiprocess/dummy/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/Modules/_multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5307 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/Modules/_multiprocess/multiprocess.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     2426 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/Modules/_multiprocess/multiprocess.h
--rw-r--r--   0 mmckerns   (501) staff       (20)    18524 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/Modules/_multiprocess/semaphore.c
--rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/examples/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5745 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/examples/benchmarks.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1587 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/examples/ex_newtype.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7004 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/examples/ex_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/examples/ex_synchronize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/examples/ex_webserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/examples/ex_workers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/CHANGES.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/connection-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/connection-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/connection-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/connection-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/COPYING.html
--rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/header.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/html4css1.css
--rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/index.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/index.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/INSTALL.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/intro.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/intro.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/manager-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/manager-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/pool-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/pool-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/process-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/process-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/processing-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/processing-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/programming-guidelines.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/programming-guidelines.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/proxy-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/proxy-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/queue-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/queue-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/sharedctypes.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/sharedctypes.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/tests.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/tests.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/THANKS.html
--rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.5/doc/version.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/index.html
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/Modules/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5289 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/README_MODS
--rw-r--r--   0 mmckerns   (501) staff       (20)      947 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/multiprocess/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    31321 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/connection.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10669 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/context.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/dummy/
--rw-r--r--   0 mmckerns   (501) staff       (20)     8474 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7952 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/heap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    36273 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/managers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    25059 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2417 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/popen_fork.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1964 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/popen_forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1915 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/popen_spawn_posix.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2998 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/popen_spawn_win32.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9144 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11631 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/queues.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8163 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/reduction.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5318 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/resource_sharer.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4891 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/semaphore_tracker.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6334 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/sharedctypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8899 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/spawn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    12401 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/synchronize.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)    10616 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/util.py
--rw-r--r--   0 mmckerns   (501) staff       (20)   120307 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      176 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/tests/test_multiprocessing_fork.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      182 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/tests/test_multiprocessing_forkserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11428 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/tests/test_multiprocessing_main_handling.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      177 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/tests/test_multiprocessing_spawn.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2881 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/dummy/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1620 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/multiprocess/dummy/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/Modules/_multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5307 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/Modules/_multiprocess/multiprocess.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     2426 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/Modules/_multiprocess/multiprocess.h
--rw-r--r--   0 mmckerns   (501) staff       (20)    18476 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/Modules/_multiprocess/semaphore.c
--rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/examples/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5745 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/examples/benchmarks.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1587 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/examples/ex_newtype.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7004 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/examples/ex_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/examples/ex_synchronize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/examples/ex_webserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/examples/ex_workers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/CHANGES.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/connection-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/connection-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/connection-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/connection-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/COPYING.html
--rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/header.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/html4css1.css
--rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/index.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/index.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/INSTALL.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/intro.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/intro.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/manager-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/manager-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/pool-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/pool-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/process-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/process-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/processing-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/processing-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/programming-guidelines.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/programming-guidelines.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/proxy-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/proxy-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py3.4/doc/queue-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/queue-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/sharedctypes.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/sharedctypes.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/tests.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/tests.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/THANKS.html
--rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.4/doc/version.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/index.html
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/Modules/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)     2928 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/README_MODS
--rw-r--r--   0 mmckerns   (501) staff       (20)     6823 2019-06-27 17:17:54.000000 multiprocess-0.70.8/py3.3/multiprocess/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    30280 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/dummy/
--rw-r--r--   0 mmckerns   (501) staff       (20)    14898 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/forking.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7081 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/heap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    36071 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/managers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    23407 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8846 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11608 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/queues.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9479 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/reduction.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6018 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/sharedctypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10884 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/synchronize.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)     9911 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/util.py
--rw-r--r--   0 mmckerns   (501) staff       (20)   110587 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4339 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/dummy/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3049 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/multiprocess/dummy/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/Modules/_multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5389 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/Modules/_multiprocess/multiprocess.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     2546 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/Modules/_multiprocess/multiprocess.h
--rw-r--r--   0 mmckerns   (501) staff       (20)    17273 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/Modules/_multiprocess/semaphore.c
--rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/examples/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5745 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/examples/benchmarks.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1587 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/examples/ex_newtype.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7004 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/examples/ex_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/examples/ex_synchronize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/examples/ex_webserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/examples/ex_workers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/CHANGES.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/connection-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/connection-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/connection-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/connection-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/COPYING.html
--rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/header.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/html4css1.css
--rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/index.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/index.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/INSTALL.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/intro.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/intro.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/manager-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/manager-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/pool-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/pool-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/process-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/process-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/processing-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/processing-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/programming-guidelines.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/programming-guidelines.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/proxy-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/proxy-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/queue-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/queue-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/sharedctypes.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/sharedctypes.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/tests.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/tests.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/THANKS.html
--rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.3/doc/version.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/index.html
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/Modules/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)     2832 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/README_MODS
--rw-r--r--   0 mmckerns   (501) staff       (20)     7748 2019-06-27 17:17:54.000000 multiprocess-0.70.8/py3.2/multiprocess/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    15129 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/dummy/
--rw-r--r--   0 mmckerns   (501) staff       (20)    16716 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/forking.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8727 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/heap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    36543 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/managers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    23890 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9841 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    12752 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/queues.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6721 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/reduction.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7565 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/sharedctypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10841 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/synchronize.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)    10687 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/util.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    76627 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4590 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/dummy/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2807 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/multiprocess/dummy/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/Modules/_multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)    13925 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/Modules/_multiprocess/connection.h
--rw-r--r--   0 mmckerns   (501) staff       (20)     9810 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/Modules/_multiprocess/multiprocess.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     4282 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/Modules/_multiprocess/multiprocess.h
--rw-r--r--   0 mmckerns   (501) staff       (20)     3642 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/Modules/_multiprocess/pipe_connection.c
--rw-r--r--   0 mmckerns   (501) staff       (20)    17490 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/Modules/_multiprocess/semaphore.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     5808 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/Modules/_multiprocess/socket_connection.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     7137 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/Modules/_multiprocess/win32_functions.c
--rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/examples/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5745 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/examples/benchmarks.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1587 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/examples/ex_newtype.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7004 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/examples/ex_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/examples/ex_synchronize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/examples/ex_webserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/examples/ex_workers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/CHANGES.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/connection-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/connection-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/connection-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/connection-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/COPYING.html
--rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/header.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/html4css1.css
--rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/index.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/index.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/INSTALL.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/intro.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/intro.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/manager-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/manager-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/pool-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/pool-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/process-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/process-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/processing-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/processing-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/programming-guidelines.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/programming-guidelines.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/proxy-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/proxy-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/queue-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/queue-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/sharedctypes.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/sharedctypes.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/tests.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/tests.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/THANKS.html
--rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.2/doc/version.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/index.html
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/Modules/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)     2461 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/README_MODS
--rw-r--r--   0 mmckerns   (501) staff       (20)     7710 2019-06-27 17:17:54.000000 multiprocess-0.70.8/py3.1/multiprocess/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    14110 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/dummy/
--rw-r--r--   0 mmckerns   (501) staff       (20)    16120 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/forking.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8727 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/heap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    36565 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/managers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    19572 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9419 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    12611 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/queues.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6721 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/reduction.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7565 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/sharedctypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10812 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/synchronize.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)     9297 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/util.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    61609 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4539 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/dummy/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2807 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/multiprocess/dummy/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/Modules/_multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)    13925 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/Modules/_multiprocess/connection.h
--rw-r--r--   0 mmckerns   (501) staff       (20)     9020 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/Modules/_multiprocess/multiprocess.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     4138 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/Modules/_multiprocess/multiprocess.h
--rw-r--r--   0 mmckerns   (501) staff       (20)     3642 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/Modules/_multiprocess/pipe_connection.c
--rw-r--r--   0 mmckerns   (501) staff       (20)    17221 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/Modules/_multiprocess/semaphore.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     5098 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/Modules/_multiprocess/socket_connection.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     7093 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/Modules/_multiprocess/win32_functions.c
--rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/examples/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5745 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/examples/benchmarks.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1587 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/examples/ex_newtype.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7004 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/examples/ex_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/examples/ex_synchronize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/examples/ex_webserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/examples/ex_workers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/CHANGES.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/connection-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/connection-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/connection-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/connection-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/COPYING.html
--rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/header.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/html4css1.css
--rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/index.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/index.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/INSTALL.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/intro.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/intro.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/manager-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/manager-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/pool-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/pool-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/process-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/process-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/processing-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/processing-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/programming-guidelines.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/programming-guidelines.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/proxy-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/proxy-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/queue-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/queue-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/sharedctypes.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/sharedctypes.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/tests.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/tests.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/THANKS.html
--rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py3.1/doc/version.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/index.html
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/Modules/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:31:35.000000 multiprocess-0.70.8/py2.7/multiprocess.egg-info/
--rw-r--r--   0 mmckerns   (501) staff       (20)    13806 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/README_MODS
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2019-06-27 17:31:35.000000 multiprocess-0.70.8/py2.7/multiprocess.egg-info/dependency_links.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2019-06-27 17:31:35.000000 multiprocess-0.70.8/py2.7/multiprocess.egg-info/not-zip-safe
--rw-r--r--   0 mmckerns   (501) staff       (20)     6024 2019-06-27 17:31:35.000000 multiprocess-0.70.8/py2.7/multiprocess.egg-info/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)       12 2019-06-27 17:31:35.000000 multiprocess-0.70.8/py2.7/multiprocess.egg-info/requires.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    21206 2019-06-27 17:31:35.000000 multiprocess-0.70.8/py2.7/multiprocess.egg-info/SOURCES.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)       27 2019-06-27 17:31:35.000000 multiprocess-0.70.8/py2.7/multiprocess.egg-info/top_level.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     7813 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.7/multiprocess/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    14852 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/dummy/
--rw-r--r--   0 mmckerns   (501) staff       (20)    17383 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/forking.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8726 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/heap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    36646 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/managers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    24195 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9684 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    12370 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/queues.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6721 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/reduction.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7750 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/sharedctypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10810 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/synchronize.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)    11075 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/util.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    83121 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4472 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/dummy/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2807 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/multiprocess/dummy/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/Modules/_multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)    13651 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/Modules/_multiprocess/connection.h
--rw-r--r--   0 mmckerns   (501) staff       (20)     9541 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/Modules/_multiprocess/multiprocess.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     4282 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/Modules/_multiprocess/multiprocess.h
--rw-r--r--   0 mmckerns   (501) staff       (20)     3642 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/Modules/_multiprocess/pipe_connection.c
--rw-r--r--   0 mmckerns   (501) staff       (20)    17823 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/Modules/_multiprocess/semaphore.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     6906 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/Modules/_multiprocess/socket_connection.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     7136 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/Modules/_multiprocess/win32_functions.c
--rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/examples/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5689 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/examples/benchmarks.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1554 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/examples/ex_newtype.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6918 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/examples/ex_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6337 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/examples/ex_synchronize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2118 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/examples/ex_webserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2187 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/examples/ex_workers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/CHANGES.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/connection-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/connection-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/connection-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/connection-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/COPYING.html
--rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/header.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/html4css1.css
--rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/index.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/index.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/INSTALL.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/intro.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/intro.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/manager-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/manager-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/pool-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/pool-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/process-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/process-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/processing-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/processing-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/programming-guidelines.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/programming-guidelines.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/proxy-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/proxy-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/queue-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/queue-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/sharedctypes.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/sharedctypes.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/tests.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/tests.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/THANKS.html
--rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.7/doc/version.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/examples/
--rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/index.html
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/Modules/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)     2376 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/README_MODS
--rw-r--r--   0 mmckerns   (501) staff       (20)     7635 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.6/multiprocess/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    12611 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/dummy/
--rw-r--r--   0 mmckerns   (501) staff       (20)    14556 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/forking.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5893 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/heap.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    34735 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/managers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    17693 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     7904 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/process.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11151 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/queues.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5263 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/reduction.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6139 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/sharedctypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9122 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/synchronize.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7833 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/util.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    57207 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2963 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/dummy/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1349 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/multiprocess/dummy/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/Modules/_multiprocess/
--rw-r--r--   0 mmckerns   (501) staff       (20)    13555 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/Modules/_multiprocess/connection.h
--rw-r--r--   0 mmckerns   (501) staff       (20)     8110 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/Modules/_multiprocess/multiprocess.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     3829 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/Modules/_multiprocess/multiprocess.h
--rw-r--r--   0 mmckerns   (501) staff       (20)     3424 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/Modules/_multiprocess/pipe_connection.c
--rw-r--r--   0 mmckerns   (501) staff       (20)    17203 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/Modules/_multiprocess/semaphore.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     5098 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/Modules/_multiprocess/socket_connection.c
--rw-r--r--   0 mmckerns   (501) staff       (20)     7092 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/Modules/_multiprocess/win32_functions.c
--rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/examples/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5689 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/examples/benchmarks.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1554 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/examples/ex_newtype.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6918 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/examples/ex_pool.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6337 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/examples/ex_synchronize.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2118 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/examples/ex_webserver.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2187 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/examples/ex_workers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/CHANGES.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/connection-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/connection-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/connection-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/connection-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/COPYING.html
--rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/header.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/html4css1.css
--rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/index.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/index.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/INSTALL.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/intro.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/intro.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/manager-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/manager-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/pool-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/pool-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/process-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/process-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/processing-ref.html
--rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/processing-ref.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/programming-guidelines.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/programming-guidelines.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/proxy-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/proxy-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/queue-objects.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/queue-objects.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/sharedctypes.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/sharedctypes.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/tests.html
--rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/tests.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/THANKS.html
--rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-06-27 17:17:56.000000 multiprocess-0.70.8/py2.6/doc/version.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/examples/
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     5097 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/index.html
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/Modules/
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1485 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/README_MODS
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     7187 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/__init__.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    13442 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/dummy/
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3534 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/finalize.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    12502 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/forking.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     6728 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/heap.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2525 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/logger.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    34718 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/managers.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    15798 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/pool.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     8982 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/process.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    10488 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/queue.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     6248 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/reduction.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     6473 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/sharedctypes.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     8975 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/synchronize.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/tests/
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    47548 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/tests/__main__.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2881 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/dummy/__init__.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1466 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/processing/dummy/connection.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/Modules/_processing/
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    11893 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/Modules/_processing/connection.h
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3648 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/Modules/_processing/pipe_connection.c
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    11220 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/Modules/_processing/processing.c
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2677 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/Modules/_processing/processing.h
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    16729 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/Modules/_processing/semaphore.c
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     4772 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/Modules/_processing/socket_connection.c
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    11665 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/Modules/_processing/win_functions.c
--rwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/examples/__init__.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     5619 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/examples/benchmarks.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1546 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/examples/ex_newtype.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     6835 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/examples/ex_pool.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     6159 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/examples/ex_synchronize.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2081 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/examples/ex_webserver.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2149 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/examples/ex_workers.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      256 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/__init__.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    38627 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/CHANGES.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     6788 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/connection-objects.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3774 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/connection-objects.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    15327 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/connection-ref.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     8704 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/connection-ref.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2065 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/COPYING.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      224 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/header.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     5534 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/html4css1.css
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3390 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/index.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1149 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/index.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3307 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/INSTALL.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    17894 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/intro.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    12397 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/intro.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    18470 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/manager-objects.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    10062 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/manager-objects.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    11625 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/pool-objects.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     6049 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/pool-objects.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    10108 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/process-objects.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     6027 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/process-objects.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    24304 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/processing-ref.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    12811 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/processing-ref.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     9005 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/programming-guidelines.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     6674 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/programming-guidelines.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     8063 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/proxy-objects.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     4975 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/proxy-objects.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     9672 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/queue-objects.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     5201 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/queue-objects.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    10351 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/sharedctypes.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     6343 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/sharedctypes.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3134 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/tests.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1499 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/tests.txt
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1021 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/THANKS.html
--rwxr-xr-x   0 mmckerns   (501) staff       (20)       28 2019-06-27 17:17:55.000000 multiprocess-0.70.8/py2.5/doc/version.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:45:59.000000 multiprocess-0.70.9/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      467 2019-09-28 16:36:20.000000 multiprocess-0.70.9/.coveragerc
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:45:59.000000 multiprocess-0.70.9/.eggs/
+-rw-r--r--   0 mmckerns   (501) staff       (20)       32 2019-09-28 16:36:20.000000 multiprocess-0.70.9/.gitignore
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2709 2019-09-28 16:36:21.000000 multiprocess-0.70.9/.travis.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)    20653 2019-09-28 16:36:21.000000 multiprocess-0.70.9/CHANGES.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1493 2019-09-28 16:36:21.000000 multiprocess-0.70.9/COPYING.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1710 2019-09-28 16:36:21.000000 multiprocess-0.70.9/INSTALL.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1949 2019-09-28 16:36:21.000000 multiprocess-0.70.9/LICENSE
+-rw-r--r--   0 mmckerns   (501) staff       (20)      369 2019-09-28 16:36:20.000000 multiprocess-0.70.9/MANIFEST.in
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:45:59.000000 multiprocess-0.70.9/py2.7/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:21.000000 multiprocess-0.70.9/py3.8/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4922 2019-09-28 16:36:21.000000 multiprocess-0.70.9/README.md
+-rw-r--r--   0 mmckerns   (501) staff       (20)    14384 2019-09-28 16:36:21.000000 multiprocess-0.70.9/setup.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      467 2019-09-28 16:36:20.000000 multiprocess-0.70.9/THANKS.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1939 2019-09-28 16:36:21.000000 multiprocess-0.70.9/tox.ini
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/_multiprocess/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:21.000000 multiprocess-0.70.9/py3.8/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/index.html
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/Modules/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    20516 2019-09-28 16:36:21.000000 multiprocess-0.70.9/py3.8/README_MODS
+-rw-r--r--   0 mmckerns   (501) staff       (20)      940 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    31661 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/connection.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11220 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/context.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/dummy/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12377 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11626 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/heap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    48803 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/managers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    32360 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2565 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/popen_fork.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2227 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/popen_forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2029 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/popen_spawn_posix.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4011 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/popen_spawn_win32.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11899 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11806 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/queues.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9637 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/reduction.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5352 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/resource_sharer.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8374 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/resource_tracker.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17216 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/shared_memory.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6306 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/sharedctypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9293 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/spawn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11829 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/synchronize.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12684 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/util.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)   184544 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      479 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/tests/test_multiprocessing_fork.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      394 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/tests/test_multiprocessing_forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11812 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/tests/test_multiprocessing_main_handling.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      279 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/tests/test_multiprocessing_spawn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3061 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/dummy/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1598 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/multiprocess/dummy/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/Modules/_multiprocess/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/Modules/_multiprocess/clinic/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5475 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/Modules/_multiprocess/multiprocess.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2388 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/Modules/_multiprocess/multiprocess.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3079 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/Modules/_multiprocess/posixshmem.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)    19116 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/Modules/_multiprocess/semaphore.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4093 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/Modules/_multiprocess/clinic/posixshmem.c.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:21.000000 multiprocess-0.70.9/py3.8/examples/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5722 2019-09-28 16:36:21.000000 multiprocess-0.70.9/py3.8/examples/benchmarks.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1595 2019-09-28 16:36:21.000000 multiprocess-0.70.9/py3.8/examples/ex_newtype.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6982 2019-09-28 16:36:21.000000 multiprocess-0.70.9/py3.8/examples/ex_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-09-28 16:36:21.000000 multiprocess-0.70.9/py3.8/examples/ex_synchronize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-09-28 16:36:21.000000 multiprocess-0.70.9/py3.8/examples/ex_webserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-09-28 16:36:21.000000 multiprocess-0.70.9/py3.8/examples/ex_workers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4182 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/examples/FAILS.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/CHANGES.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/connection-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/connection-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/connection-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/connection-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/COPYING.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/header.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/html4css1.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/index.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/index.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/INSTALL.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/intro.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/intro.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/manager-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/manager-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/pool-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/pool-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/process-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/process-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/processing-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/processing-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/programming-guidelines.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/programming-guidelines.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/proxy-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/proxy-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/queue-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/queue-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/sharedctypes.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/sharedctypes.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/tests.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/tests.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/THANKS.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/doc/version.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)       31 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.8/_multiprocess/__init__.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/_multiprocess/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/index.html
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/Modules/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13893 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/README_MODS
+-rw-r--r--   0 mmckerns   (501) staff       (20)      947 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    31274 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/connection.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10923 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/context.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/dummy/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11780 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8918 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/heap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    40212 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/managers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    26834 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2391 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/popen_fork.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2013 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/popen_forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1921 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/popen_spawn_posix.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3766 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/popen_spawn_win32.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10548 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11703 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/queues.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9486 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/reduction.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5350 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/resource_sharer.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5539 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/semaphore_tracker.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6306 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/sharedctypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8845 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/spawn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11806 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/synchronize.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12106 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/util.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)   152770 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      479 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/tests/test_multiprocessing_fork.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      388 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/tests/test_multiprocessing_forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/tests/test_multiprocessing_main_handling.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      279 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/tests/test_multiprocessing_spawn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3058 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/dummy/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1598 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/multiprocess/dummy/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/Modules/_multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5475 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/Modules/_multiprocess/multiprocess.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2388 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/Modules/_multiprocess/multiprocess.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18933 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/Modules/_multiprocess/semaphore.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/examples/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5722 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/examples/benchmarks.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1595 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/examples/ex_newtype.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6982 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/examples/ex_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/examples/ex_synchronize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/examples/ex_webserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/examples/ex_workers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/CHANGES.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/connection-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/connection-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/connection-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/connection-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/COPYING.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/header.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/html4css1.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/index.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/index.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/INSTALL.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/intro.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/intro.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/manager-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/manager-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/pool-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/pool-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/process-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/process-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/processing-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/processing-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/programming-guidelines.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/programming-guidelines.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/proxy-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/proxy-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/queue-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/queue-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/sharedctypes.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/sharedctypes.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/tests.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/tests.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/THANKS.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/doc/version.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)       31 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.7/_multiprocess/__init__.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/_multiprocess/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/index.html
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/Modules/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    21446 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/README_MODS
+-rw-r--r--   0 mmckerns   (501) staff       (20)      947 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    31050 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/connection.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10917 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/context.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/dummy/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8691 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8319 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/heap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38193 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/managers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    26059 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/popen_fork.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1953 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/popen_forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1904 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/popen_spawn_posix.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2999 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/popen_spawn_win32.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9211 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10879 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/queues.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9357 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/reduction.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5325 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/resource_sharer.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5465 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/semaphore_tracker.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6245 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/sharedctypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8860 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/spawn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12269 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/synchronize.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11883 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/util.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)   126954 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      479 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/tests/test_multiprocessing_fork.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      394 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/tests/test_multiprocessing_forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11734 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/tests/test_multiprocessing_main_handling.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      279 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/tests/test_multiprocessing_spawn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2896 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/dummy/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1583 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/multiprocess/dummy/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/Modules/_multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5338 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/Modules/_multiprocess/multiprocess.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/Modules/_multiprocess/multiprocess.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18586 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/Modules/_multiprocess/semaphore.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/examples/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5722 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/examples/benchmarks.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1595 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/examples/ex_newtype.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6982 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/examples/ex_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/examples/ex_synchronize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/examples/ex_webserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/examples/ex_workers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/CHANGES.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/connection-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/connection-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/connection-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/connection-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/COPYING.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/header.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/html4css1.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/index.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/index.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/INSTALL.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/intro.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/intro.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/manager-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/manager-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/pool-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/pool-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/process-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/process-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/processing-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/processing-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/programming-guidelines.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/programming-guidelines.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/proxy-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/proxy-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/queue-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/queue-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/sharedctypes.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/sharedctypes.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/tests.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/tests.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/THANKS.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/doc/version.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)       31 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.6/_multiprocess/__init__.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/_multiprocess/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/index.html
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/Modules/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13846 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/README_MODS
+-rw-r--r--   0 mmckerns   (501) staff       (20)      947 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    30931 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/connection.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10677 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/context.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/dummy/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8210 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8325 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/heap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    35963 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/managers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    25819 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2324 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/popen_fork.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1964 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/popen_forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1915 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/popen_spawn_posix.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2998 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/popen_spawn_win32.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9136 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10825 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/queues.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8239 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/reduction.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5318 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/resource_sharer.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4891 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/semaphore_tracker.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6228 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/sharedctypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8912 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/spawn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12229 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/synchronize.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11638 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/util.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)   123593 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      176 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/tests/test_multiprocessing_fork.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      182 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/tests/test_multiprocessing_forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11535 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/tests/test_multiprocessing_main_handling.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      177 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/tests/test_multiprocessing_spawn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2896 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/dummy/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1583 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/multiprocess/dummy/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/Modules/_multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/Modules/_multiprocess/multiprocess.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2426 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/Modules/_multiprocess/multiprocess.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18524 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/Modules/_multiprocess/semaphore.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/examples/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5722 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/examples/benchmarks.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1595 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/examples/ex_newtype.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6982 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/examples/ex_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/examples/ex_synchronize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/examples/ex_webserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/examples/ex_workers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/CHANGES.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/connection-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/connection-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/connection-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/connection-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/COPYING.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/header.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/html4css1.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/index.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/index.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/INSTALL.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/intro.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/intro.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/manager-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/manager-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/pool-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/pool-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/process-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/process-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/processing-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/processing-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/programming-guidelines.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/programming-guidelines.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/proxy-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/proxy-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/queue-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/queue-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/sharedctypes.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/sharedctypes.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/tests.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/tests.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/THANKS.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/doc/version.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)       31 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.5/_multiprocess/__init__.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/_multiprocess/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/index.html
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/Modules/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5429 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/README_MODS
+-rw-r--r--   0 mmckerns   (501) staff       (20)      947 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    31321 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/connection.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10669 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/context.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/dummy/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8474 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7952 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/heap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    36273 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/managers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    25059 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2417 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/popen_fork.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1964 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/popen_forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1915 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/popen_spawn_posix.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2998 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/popen_spawn_win32.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9144 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11631 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/queues.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8239 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/reduction.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5318 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/resource_sharer.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4891 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/semaphore_tracker.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6334 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/sharedctypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8899 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/spawn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12401 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/synchronize.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10616 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/util.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)   120310 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      176 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/tests/test_multiprocessing_fork.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      182 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/tests/test_multiprocessing_forkserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11431 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/tests/test_multiprocessing_main_handling.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      177 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/tests/test_multiprocessing_spawn.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2881 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/dummy/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1620 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/multiprocess/dummy/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/Modules/_multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/Modules/_multiprocess/multiprocess.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2426 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/Modules/_multiprocess/multiprocess.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18476 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/Modules/_multiprocess/semaphore.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/examples/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5722 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/examples/benchmarks.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1595 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/examples/ex_newtype.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6982 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/examples/ex_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/examples/ex_synchronize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/examples/ex_webserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/examples/ex_workers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/CHANGES.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/connection-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/connection-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/connection-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/connection-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/COPYING.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/header.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/html4css1.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/index.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/index.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/INSTALL.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/intro.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/intro.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/manager-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/manager-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/pool-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/pool-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/process-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/process-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/processing-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/processing-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/programming-guidelines.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/programming-guidelines.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/proxy-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/proxy-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/queue-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/queue-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/sharedctypes.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/sharedctypes.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/tests.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/tests.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/THANKS.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/doc/version.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)       31 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.4/_multiprocess/__init__.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:19.000000 multiprocess-0.70.9/py3.3/_multiprocess/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/index.html
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/Modules/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2988 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/README_MODS
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6823 2019-09-28 16:36:19.000000 multiprocess-0.70.9/py3.3/multiprocess/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    30280 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/dummy/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    14944 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/forking.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7081 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/heap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    36071 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/managers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    23407 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8846 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11608 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/queues.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9479 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/reduction.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6018 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/sharedctypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10884 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/synchronize.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9911 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/util.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)   110590 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4339 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/dummy/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/multiprocess/dummy/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/Modules/_multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5389 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/Modules/_multiprocess/multiprocess.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2546 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/Modules/_multiprocess/multiprocess.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17273 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/Modules/_multiprocess/semaphore.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/examples/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5722 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/examples/benchmarks.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1595 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/examples/ex_newtype.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6982 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/examples/ex_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/examples/ex_synchronize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/examples/ex_webserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/examples/ex_workers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/CHANGES.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/connection-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/connection-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/connection-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/connection-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/COPYING.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/header.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/html4css1.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/index.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/index.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/INSTALL.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/intro.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/intro.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/manager-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/manager-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/pool-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/pool-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/process-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/process-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/processing-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/processing-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/programming-guidelines.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/programming-guidelines.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/proxy-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/proxy-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/queue-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/queue-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/sharedctypes.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/sharedctypes.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/tests.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/tests.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/THANKS.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.3/doc/version.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)       31 2019-09-28 16:36:19.000000 multiprocess-0.70.9/py3.3/_multiprocess/__init__.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/index.html
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/Modules/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2892 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/README_MODS
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7748 2019-09-28 16:36:19.000000 multiprocess-0.70.9/py3.2/multiprocess/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15129 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/dummy/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    16833 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/forking.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8727 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/heap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    36543 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/managers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    23890 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9841 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12752 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/queues.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6721 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/reduction.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7565 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/sharedctypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10841 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/synchronize.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10687 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/util.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    76627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4590 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/dummy/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2807 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/multiprocess/dummy/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/Modules/_multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13925 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/Modules/_multiprocess/connection.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9810 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/Modules/_multiprocess/multiprocess.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4282 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/Modules/_multiprocess/multiprocess.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3642 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/Modules/_multiprocess/pipe_connection.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17490 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/Modules/_multiprocess/semaphore.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5808 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/Modules/_multiprocess/socket_connection.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7137 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/Modules/_multiprocess/win32_functions.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/examples/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5722 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/examples/benchmarks.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1595 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/examples/ex_newtype.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6982 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/examples/ex_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/examples/ex_synchronize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/examples/ex_webserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/examples/ex_workers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/CHANGES.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/connection-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/connection-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/connection-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/connection-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/COPYING.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/header.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/html4css1.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/index.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/index.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/INSTALL.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/intro.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/intro.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/manager-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/manager-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/pool-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/pool-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/process-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/process-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/processing-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/processing-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/programming-guidelines.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/programming-guidelines.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/proxy-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/proxy-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/queue-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/queue-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/sharedctypes.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/sharedctypes.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/tests.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/tests.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/THANKS.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.2/doc/version.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/index.html
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/Modules/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2521 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/README_MODS
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7710 2019-09-28 16:36:19.000000 multiprocess-0.70.9/py3.1/multiprocess/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    14110 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/dummy/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    16237 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/forking.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8727 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/heap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    36565 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/managers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    19572 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9419 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12611 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/queues.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6721 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/reduction.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7565 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/sharedctypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10812 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/synchronize.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9297 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/util.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    61609 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4539 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/dummy/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2807 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/multiprocess/dummy/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/Modules/_multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13925 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/Modules/_multiprocess/connection.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9020 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/Modules/_multiprocess/multiprocess.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4138 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/Modules/_multiprocess/multiprocess.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3642 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/Modules/_multiprocess/pipe_connection.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17221 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/Modules/_multiprocess/semaphore.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5098 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/Modules/_multiprocess/socket_connection.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7093 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/Modules/_multiprocess/win32_functions.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/examples/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5722 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/examples/benchmarks.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1595 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/examples/ex_newtype.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6982 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/examples/ex_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6404 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/examples/ex_synchronize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2112 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/examples/ex_webserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2196 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/examples/ex_workers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/CHANGES.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/connection-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/connection-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/connection-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/connection-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/COPYING.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/header.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/html4css1.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/index.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/index.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/INSTALL.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/intro.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/intro.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/manager-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/manager-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/pool-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/pool-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/process-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/process-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/processing-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/processing-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/programming-guidelines.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/programming-guidelines.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/proxy-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/proxy-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/queue-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/queue-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/sharedctypes.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/sharedctypes.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/tests.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/tests.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/THANKS.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py3.1/doc/version.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/index.html
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/Modules/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:45:59.000000 multiprocess-0.70.9/py2.7/multiprocess.egg-info/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13939 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/README_MODS
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2019-09-28 16:45:59.000000 multiprocess-0.70.9/py2.7/multiprocess.egg-info/dependency_links.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2019-09-28 16:45:59.000000 multiprocess-0.70.9/py2.7/multiprocess.egg-info/not-zip-safe
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6024 2019-09-28 16:45:59.000000 multiprocess-0.70.9/py2.7/multiprocess.egg-info/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)       12 2019-09-28 16:45:59.000000 multiprocess-0.70.9/py2.7/multiprocess.egg-info/requires.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    21366 2019-09-28 16:45:59.000000 multiprocess-0.70.9/py2.7/multiprocess.egg-info/SOURCES.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)       27 2019-09-28 16:45:59.000000 multiprocess-0.70.9/py2.7/multiprocess.egg-info/top_level.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7813 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    14852 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/dummy/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/forking.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8726 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/heap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    36646 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/managers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24195 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9684 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12370 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/queues.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6721 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/reduction.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7750 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/sharedctypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10810 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/synchronize.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11075 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/util.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    83121 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4472 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/dummy/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2807 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/multiprocess/dummy/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/Modules/_multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13651 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/Modules/_multiprocess/connection.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9541 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/Modules/_multiprocess/multiprocess.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4282 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/Modules/_multiprocess/multiprocess.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3642 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/Modules/_multiprocess/pipe_connection.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17823 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/Modules/_multiprocess/semaphore.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6906 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/Modules/_multiprocess/socket_connection.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7136 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/Modules/_multiprocess/win32_functions.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/examples/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5689 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/examples/benchmarks.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1554 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/examples/ex_newtype.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6918 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/examples/ex_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6337 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/examples/ex_synchronize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2118 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/examples/ex_webserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2187 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/examples/ex_workers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/CHANGES.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/connection-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/connection-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/connection-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/connection-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/COPYING.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/header.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/html4css1.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/index.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/index.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/INSTALL.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/intro.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/intro.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/manager-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/manager-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/pool-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/pool-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/process-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/process-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/processing-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/processing-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/programming-guidelines.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/programming-guidelines.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/proxy-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/proxy-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/queue-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/queue-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/sharedctypes.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/sharedctypes.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/tests.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/tests.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/THANKS.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.7/doc/version.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/examples/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5097 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/index.html
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/Modules/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2436 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/README_MODS
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7635 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12611 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/dummy/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    14672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/forking.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5893 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/heap.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    34735 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/managers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17693 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7904 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/process.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11151 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/queues.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5263 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/reduction.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6139 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/sharedctypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9122 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/synchronize.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7833 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/util.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    57207 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2963 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/dummy/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1349 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/multiprocess/dummy/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/Modules/_multiprocess/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13555 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/Modules/_multiprocess/connection.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8110 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/Modules/_multiprocess/multiprocess.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3829 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/Modules/_multiprocess/multiprocess.h
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3424 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/Modules/_multiprocess/pipe_connection.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17203 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/Modules/_multiprocess/semaphore.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5098 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/Modules/_multiprocess/socket_connection.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7092 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/Modules/_multiprocess/win32_functions.c
+-rw-r--r--   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/examples/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5689 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/examples/benchmarks.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1554 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/examples/ex_newtype.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6918 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/examples/ex_pool.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6337 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/examples/ex_synchronize.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2118 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/examples/ex_webserver.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2187 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/examples/ex_workers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      256 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    38627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/CHANGES.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6788 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/connection-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3774 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/connection-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    15327 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/connection-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8704 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/connection-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2065 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/COPYING.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)      224 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/header.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/html4css1.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3390 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/index.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/index.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/INSTALL.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    17894 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/intro.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/intro.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    18470 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/manager-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10062 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/manager-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11625 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/pool-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/pool-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10108 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/process-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6027 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/process-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    24304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/processing-ref.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/processing-ref.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9005 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/programming-guidelines.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6674 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/programming-guidelines.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8063 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/proxy-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/proxy-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/queue-objects.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5201 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/queue-objects.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10351 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/sharedctypes.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6343 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/sharedctypes.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/tests.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/tests.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1021 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/THANKS.html
+-rw-r--r--   0 mmckerns   (501) staff       (20)       28 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.6/doc/version.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/examples/
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     5097 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/index.html
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/Modules/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1485 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/README_MODS
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     7187 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/__init__.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    13442 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/dummy/
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/finalize.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    12502 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/forking.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     6728 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/heap.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2525 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/logger.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    34718 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/managers.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    15798 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/pool.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     8982 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/process.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    10488 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/queue.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     6248 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/reduction.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     6473 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/sharedctypes.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     8975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/synchronize.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/tests/
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    47548 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      840 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/tests/__main__.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2881 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/dummy/__init__.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1466 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/processing/dummy/connection.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/Modules/_processing/
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    11893 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/Modules/_processing/connection.h
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3648 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/Modules/_processing/pipe_connection.c
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    11220 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/Modules/_processing/processing.c
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2677 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/Modules/_processing/processing.h
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    16729 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/Modules/_processing/semaphore.c
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     4772 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/Modules/_processing/socket_connection.c
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    11665 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/Modules/_processing/win_functions.c
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/examples/__init__.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     5619 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/examples/benchmarks.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1546 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/examples/ex_newtype.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     6835 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/examples/ex_pool.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     6159 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/examples/ex_synchronize.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2081 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/examples/ex_webserver.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/examples/ex_workers.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      256 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/__init__.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    38627 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/CHANGES.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     6788 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/connection-objects.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3774 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/connection-objects.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    15327 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/connection-ref.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     8704 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/connection-ref.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2065 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/COPYING.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      224 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/header.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     5534 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/html4css1.css
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3390 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/index.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1149 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/index.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3307 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/INSTALL.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    17894 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/intro.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    12397 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/intro.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    18470 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/manager-objects.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    10062 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/manager-objects.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    11625 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/pool-objects.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     6049 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/pool-objects.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    10108 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/process-objects.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     6027 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/process-objects.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    24304 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/processing-ref.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    12811 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/processing-ref.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     9005 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/programming-guidelines.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     6674 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/programming-guidelines.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     8063 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/proxy-objects.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     4975 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/proxy-objects.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     9672 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/queue-objects.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     5201 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/queue-objects.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    10351 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/sharedctypes.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     6343 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/sharedctypes.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3134 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/tests.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1499 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/tests.txt
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1021 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/THANKS.html
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)       28 2019-09-28 16:36:20.000000 multiprocess-0.70.9/py2.5/doc/version.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)      211 2019-09-28 16:45:59.000000 multiprocess-0.70.9/.eggs/README.txt
```

### Comparing `multiprocess-0.70.8/.travis.yml` & `multiprocess-0.70.9/.travis.yml`

 * *Files 5% similar despite different names*

```diff
@@ -98,15 +98,15 @@
     - if [[ $COVERAGE == "true" ]]; then pip install coverage; fi
     - if [[ $DILL == "true" ]]; then pip install dill; fi
 
 install:
     - python setup.py build && python setup.py install
 
 script:
-    - if [[ $PYVERSION == "nightly" ]] || [[ $PYVERSION == "3.8-dev" ]]; then $PYVERSION="3.8"; else PYVERSION=$TRAVIS_PYTHON_VERSION ; fi
+    - if [[ $PYVERSION != "3.8" ]]; then PYVERSION=$TRAVIS_PYTHON_VERSION ; fi
     - cd py$PYVERSION
     - cp ../.coveragerc .coveragerc
     - for test in multiprocess/tests/__init__.py; do echo $test ; if [[ $COVERAGE == "true" ]]; then coverage run -a $test > /dev/null; else python $test > /dev/null; fi ; done
     - for test in multiprocess/tests/*.py; do if [[ $test != "__"* ]]; then echo $test ; if [[ $COVERAGE == "true" ]]; then coverage run -a $test > /dev/null; else python $test > /dev/null; fi ; fi; done
     - if [[ $COVERAGE == "true" ]]; then cat .coverage; else echo ''; fi
     - if [[ $COVERAGE == "true" ]]; then mv .coverage ../.coverage; else echo ''; fi
     - cd ..
```

### Comparing `multiprocess-0.70.8/CHANGES.txt` & `multiprocess-0.70.9/CHANGES.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/COPYING.txt` & `multiprocess-0.70.9/COPYING.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/INSTALL.txt` & `multiprocess-0.70.9/INSTALL.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/LICENSE` & `multiprocess-0.70.9/LICENSE`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/README.md` & `multiprocess-0.70.9/README.md`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/setup.py` & `multiprocess-0.70.9/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 #!/usr/bin/env python
 
 import re
 import os
 import sys
 import glob
-stable_version = '0.70.8'
+stable_version = '0.70.9'
 pymajor,pyminor = sys.version_info[:2]
 pkgdir = 'py%s.%s' % (pymajor,pyminor)
 if sys.version_info < (2, 5):
     raise ValueError('Versions of Python before 2.5 are not supported')
 elif sys.version_info >= (2, 6):
     pkgname = 'multiprocess'
 else: # (2, 5)
@@ -40,14 +40,15 @@
 if sys.platform == 'win32' and sys.version_info >= (2, 6):
     # distutils.msvc9compiler can raise IOError if the compiler is missing
     ext_errors += (IOError, )
 
 is_jython = sys.platform.startswith('java')
 is_pypy = hasattr(sys, 'pypy_version_info')
 is_py3k = sys.version_info[0] == 3
+lt_py33 = sys.version_info < (3, 3)
 
 BUILD_WARNING = """
 
 -----------------------------------------------------------------------
 WARNING: The C extensions could not be compiled
 -----------------------------------------------------------------------
 
@@ -62,15 +63,15 @@
 install a C compiler or fix the error(s) above.
 -----------------------------------------------------------------------
 
 """
 
 # -*- extra config (setuptools) -*-
 if has_setuptools:
-    extras = dict(install_requires=['dill>=0.3.0'])
+    extras = dict(install_requires=['dill>=0.3.1'])
 else:
     extras = dict()
 
 # -*- Distribution Meta -*-
 here = os.path.abspath(os.path.dirname(__file__))
 meta_fh = open(os.path.join(here, '%s/__init__.py' % libdir))
 try:
@@ -182,23 +183,23 @@
     libraries = ['rt']
 
 if sys.platform == 'win32':
     multiprocessing_srcs = [
         '%s/%s.c' % (srcdir, pkgname),
         '%s/semaphore.c' % srcdir,
     ]
-    if sys.version_info < (3, 3):
+    if lt_py33:
         multiprocessing_srcs += [
             '%s/pipe_connection.c' % srcdir,
             '%s/socket_connection.c' % srcdir,
             '%s/win32_functions.c' % srcdir,
         ]
 else:
     multiprocessing_srcs = [ '%s/%s.c' % (srcdir, pkgname) ]
-    if sys.version_info < (3, 3):
+    if lt_py33:
         multiprocessing_srcs.append('%s/socket_connection.c' % srcdir)
 
     if macros.get('HAVE_SEM_OPEN', False):
         multiprocessing_srcs.append('%s/semaphore.c' % srcdir)
 
 long_description = \
 '''-----------------------------------------------------------------
@@ -283,15 +284,15 @@
 
 Requirements
 ============
 
 ``multiprocess`` requires::
 
     - ``python``, **version >= 2.5** or **version >= 3.1**
-    - ``dill``, **version >= 0.3.0**
+    - ``dill``, **version >= 0.3.1**
 
 Optional requirements::
 
     - ``setuptools``, **version >= 0.6**
 
 
 More Information
@@ -333,17 +334,17 @@
 #
 #"""
 #long_description += open(os.path.join(HERE, 'CHANGES.txt')).read()
 #if not is_py3k:
 #    long_description = long_description.encode('ascii', 'replace')
 
 # -*- Installation Requires -*-
-py_version = sys.version_info
-is_jython = sys.platform.startswith('java')
-is_pypy = hasattr(sys, 'pypy_version_info')
+#py_version = sys.version_info
+#is_jython = sys.platform.startswith('java')
+#is_pypy = hasattr(sys, 'pypy_version_info')
 
 #def strip_comments(l):
 #    return l.split('#', 1)[0].strip()
 #
 #def reqs(f):
 #    return list(filter(None, [strip_comments(l) for l in open(
 #        os.path.join(os.getcwd(), 'requirements', f)).readlines()]))
@@ -404,15 +405,15 @@
             'Topic :: Software Development',
         ],
         **extras
     )
     setup(**config)
 
 try:
-    run_setup(not (is_jython or is_pypy))# or is_py3k))
+    run_setup(not (is_jython or is_pypy) and lt_py33)
 except BaseException:
     if _is_build_command(sys.argv):
         import traceback
         msg = BUILD_WARNING % '\n'.join(traceback.format_stack())
         if not is_py3k:
             exec('print >> sys.stderr, msg')
         else:
```

### Comparing `multiprocess-0.70.8/tox.ini` & `multiprocess-0.70.9/tox.ini`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/index.html` & `multiprocess-0.70.9/py3.8/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/README_MODS` & `multiprocess-0.70.9/py3.8/README_MODS`

 * *Files 10% similar despite different names*

```diff
@@ -516,8 +516,73 @@
 <             dt = time.monotonic() - start_time
 ---
 >             dt = getattr(time,'monotonic',time.time)() - start_time
 5518c5522
 <                 print("Warning -- multiprocessing.Manager still has %s active "
 ---
 >                 print("Warning -- multiprocess.Manager still has %s active "
+diff Python-3.8.0b1/Lib/multiprocessing/popen_spawn_win32.py Python-3.8.0b2/Lib/multiprocessing/popen_spawn_win32.py
+25,26c25
+< WINENV = (hasattr(sys, '_base_executable') and
+<           not _path_eq(sys.executable, sys._base_executable))
+---
+> WINENV = not _path_eq(sys.executable, sys._base_executable)
+diff Python-3.8.0b1/Modules/_multiprocessing/clinic/posixshmem.c.h Python-3.8.0b4/Modules/_multiprocessing/clinic/posixshmem.c.h
+38c38
+<         _PyArg_BadArgument("shm_open", 1, "str", args[0]);
+---
+>         _PyArg_BadArgument("shm_open", "argument 'path'", "str", args[0]);
+111c111
+<         _PyArg_BadArgument("shm_unlink", 1, "str", args[0]);
+---
+>         _PyArg_BadArgument("shm_unlink", "argument 'path'", "str", args[0]);
+133c133
+< /*[clinic end generated code: output=be42e23c18677c0f input=a9049054013a1b77]*/
+---
+> /*[clinic end generated code: output=9132861c61d8c2d8 input=a9049054013a1b77]*/
+diff Python-3.8.0b1/Lib/multiprocessing/forkserver.py Python-3.8.0b4/Lib/multiprocessing/forkserver.py
+41a42,60
+>     def _stop(self):
+>         # Method used by unit tests to stop the server
+>         with self._lock:
+>             self._stop_unlocked()
+> 
+>     def _stop_unlocked(self):
+>         if self._forkserver_pid is None:
+>             return
+> 
+>         # close the "alive" file descriptor asks the server to stop
+>         os.close(self._forkserver_alive_fd)
+>         self._forkserver_alive_fd = None
+> 
+>         os.waitpid(self._forkserver_pid, 0)
+>         self._forkserver_pid = None
+> 
+>         os.unlink(self._forkserver_address)
+>         self._forkserver_address = None
+> 
+diff Python-3.8.0b1/Lib/multiprocessing/util.py Python-3.8.0b4/Lib/multiprocessing/util.py
+108a109,117
+> def _remove_temp_dir(rmtree, tempdir):
+>     rmtree(tempdir)
+> 
+>     current_process = process.current_process()
+>     # current_process() can be None if the finalizer is called
+>     # late during Python finalization
+>     if current_process is not None:
+>         current_process._config['tempdir'] = None
+> 
+116c125,128
+<         Finalize(None, shutil.rmtree, args=[tempdir], exitpriority=-100)
+---
+>         # keep a strong reference to shutil.rmtree(), since the finalizer
+>         # can be called late during Python shutdown
+>         Finalize(None, _remove_temp_dir, args=(shutil.rmtree, tempdir),
+>                  exitpriority=-100)
+# ----------------------------------------------------------------------
+ADDED *args, **kwds for ForkingPickler in __init__, dump, and dumps
+diff Python-3.8.0b4/Lib/multiprocessing/context.py py3.8/multiprocessing/context.py
+312c312
+<        _default_context = DefaultContext(_concrete_contexts['spawn'])
+---
+>        _default_context = DefaultContext(_concrete_contexts['fork']) #FIXME: spawn
```

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/__init__.py` & `multiprocess-0.70.9/py3.8/multiprocess/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 # Copyright (c) 2006-2008, R Oudkerk
 # Licensed to PSF under a Contributor Agreement.
 #
 
 import sys
 from . import context
 
-__version__ = '0.70.8'
+__version__ = '0.70.9'
 
 #
 # Copy stuff from default context
 #
 
 __all__ = [x for x in dir(context._default_context) if not x.startswith('_')]
 globals().update((name, getattr(context._default_context, name)) for name in __all__)
```

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/connection.py` & `multiprocess-0.70.9/py3.8/multiprocess/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/context.py` & `multiprocess-0.70.9/py3.8/multiprocess/context.py`

 * *Files 0% similar despite different names*

```diff
@@ -308,15 +308,15 @@
         'fork': ForkContext(),
         'spawn': SpawnContext(),
         'forkserver': ForkServerContext(),
     }
     if sys.platform == 'darwin':
         # bpo-33725: running arbitrary code after fork() is no longer reliable
         # on macOS since macOS 10.14 (Mojave). Use spawn by default instead.
-        _default_context = DefaultContext(_concrete_contexts['spawn'])
+        _default_context = DefaultContext(_concrete_contexts['fork']) #FIXME: spawn
     else:
         _default_context = DefaultContext(_concrete_contexts['fork'])
 
 else:
 
     class SpawnProcess(process.BaseProcess):
         _start_method = 'spawn'
```

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/forkserver.py` & `multiprocess-0.70.9/py3.8/multiprocess/forkserver.py`

 * *Files 3% similar despite different names*

```diff
@@ -35,14 +35,33 @@
         self._forkserver_address = None
         self._forkserver_alive_fd = None
         self._forkserver_pid = None
         self._inherited_fds = None
         self._lock = threading.Lock()
         self._preload_modules = ['__main__']
 
+    def _stop(self):
+        # Method used by unit tests to stop the server
+        with self._lock:
+            self._stop_unlocked()
+
+    def _stop_unlocked(self):
+        if self._forkserver_pid is None:
+            return
+
+        # close the "alive" file descriptor asks the server to stop
+        os.close(self._forkserver_alive_fd)
+        self._forkserver_alive_fd = None
+
+        os.waitpid(self._forkserver_pid, 0)
+        self._forkserver_pid = None
+
+        os.unlink(self._forkserver_address)
+        self._forkserver_address = None
+
     def set_forkserver_preload(self, modules_names):
         '''Set list of module names to try to load in forkserver process.'''
         if not all(type(mod) is str for mod in self._preload_modules):
             raise TypeError('module_names must be a list of strings')
         self._preload_modules = modules_names
 
     def get_inherited_fds(self):
```

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/heap.py` & `multiprocess-0.70.9/py3.8/multiprocess/heap.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/managers.py` & `multiprocess-0.70.9/py3.8/multiprocess/managers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/pool.py` & `multiprocess-0.70.9/py3.8/multiprocess/pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/popen_fork.py` & `multiprocess-0.70.9/py3.8/multiprocess/popen_fork.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/popen_forkserver.py` & `multiprocess-0.70.9/py3.8/multiprocess/popen_forkserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/popen_spawn_posix.py` & `multiprocess-0.70.9/py3.8/multiprocess/popen_spawn_posix.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/popen_spawn_win32.py` & `multiprocess-0.70.9/py3.8/multiprocess/popen_spawn_win32.py`

 * *Files 4% similar despite different names*

```diff
@@ -18,16 +18,15 @@
 WINEXE = (sys.platform == 'win32' and getattr(sys, 'frozen', False))
 WINSERVICE = sys.executable.lower().endswith("pythonservice.exe")
 
 
 def _path_eq(p1, p2):
     return p1 == p2 or os.path.normcase(p1) == os.path.normcase(p2)
 
-WINENV = (hasattr(sys, '_base_executable') and
-          not _path_eq(sys.executable, sys._base_executable))
+WINENV = not _path_eq(sys.executable, sys._base_executable)
 
 
 def _close_handles(*handles):
     for handle in handles:
         _winapi.CloseHandle(handle)
```

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/process.py` & `multiprocess-0.70.9/py3.8/multiprocess/process.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/queues.py` & `multiprocess-0.70.9/py3.8/multiprocess/queues.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/reduction.py` & `multiprocess-0.70.9/py3.8/multiprocess/reduction.py`

 * *Files 2% similar despite different names*

```diff
@@ -34,37 +34,37 @@
 #
 
 class ForkingPickler(pickle.Pickler):
     '''Pickler subclass used by multiprocess.'''
     _extra_reducers = {}
     _copyreg_dispatch_table = copyreg.dispatch_table
 
-    def __init__(self, *args):
-        super().__init__(*args)
+    def __init__(self, *args, **kwds):
+        super().__init__(*args, **kwds)
         self.dispatch_table = self._copyreg_dispatch_table.copy()
         self.dispatch_table.update(self._extra_reducers)
 
     @classmethod
     def register(cls, type, reduce):
         '''Register a reduce function for a type.'''
         cls._extra_reducers[type] = reduce
 
     @classmethod
-    def dumps(cls, obj, protocol=None):
+    def dumps(cls, obj, protocol=None, *args, **kwds):
         buf = io.BytesIO()
-        cls(buf, protocol).dump(obj)
+        cls(buf, protocol, *args, **kwds).dump(obj)
         return buf.getbuffer()
 
     loads = pickle.loads
 
 register = ForkingPickler.register
 
-def dump(obj, file, protocol=None):
+def dump(obj, file, protocol=None, *args, **kwds):
     '''Replacement for pickle.dump() using ForkingPickler.'''
-    ForkingPickler(file, protocol).dump(obj)
+    ForkingPickler(file, protocol, *args, **kwds).dump(obj)
 
 #
 # Platform specific definitions
 #
 
 if sys.platform == 'win32':
     # Windows
```

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/resource_sharer.py` & `multiprocess-0.70.9/py3.8/multiprocess/resource_sharer.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/resource_tracker.py` & `multiprocess-0.70.9/py3.8/multiprocess/resource_tracker.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/shared_memory.py` & `multiprocess-0.70.9/py3.8/multiprocess/shared_memory.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/sharedctypes.py` & `multiprocess-0.70.9/py3.8/multiprocess/sharedctypes.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/spawn.py` & `multiprocess-0.70.9/py3.8/multiprocess/spawn.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/synchronize.py` & `multiprocess-0.70.9/py3.8/multiprocess/synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/util.py` & `multiprocess-0.70.9/py3.7/multiprocess/util.py`

 * *Files 2% similar despite different names*

```diff
@@ -417,13 +417,7 @@
         return _posixsubprocess.fork_exec(
             args, [os.fsencode(path)], True, passfds, None, None,
             -1, -1, -1, -1, -1, -1, errpipe_read, errpipe_write,
             False, False, None)
     finally:
         os.close(errpipe_read)
         os.close(errpipe_write)
-
-
-def close_fds(*fds):
-    """Close each file descriptor given as an argument"""
-    for fd in fds:
-        os.close(fd)
```

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/tests/__init__.py` & `multiprocess-0.70.9/py3.8/multiprocess/tests/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -25,15 +25,15 @@
 import warnings
 import test.support
 import test.support.script_helper
 from test import support
 
 
 # Skip tests if _multiprocessing wasn't built.
-_multiprocessing = test.support.import_module('_multiprocess')
+_multiprocessing = test.support.import_module('_multiprocessing')
 # Skip tests if sem_open implementation is broken.
 test.support.import_module('multiprocess.synchronize')
 import threading
 
 import multiprocess as multiprocessing
 import multiprocess.connection
 import multiprocess.dummy
```

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/tests/__main__.py` & `multiprocess-0.70.9/py3.8/multiprocess/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/tests/test_multiprocessing_main_handling.py` & `multiprocess-0.70.9/py3.8/multiprocess/tests/test_multiprocessing_main_handling.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 # tests __main__ module handling in multiprocessing
 from test import support
 # Skip tests if _multiprocessing wasn't built.
-support.import_module('_multiprocess')
+support.import_module('_multiprocessing')
 
 import importlib
 import importlib.machinery
 import unittest
 import sys
 import os
 import os.path
```

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/dummy/__init__.py` & `multiprocess-0.70.9/py3.8/multiprocess/dummy/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/multiprocess/dummy/connection.py` & `multiprocess-0.70.9/py3.8/multiprocess/dummy/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/Modules/_multiprocess/multiprocess.c` & `multiprocess-0.70.9/py3.8/Modules/_multiprocess/multiprocess.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/Modules/_multiprocess/multiprocess.h` & `multiprocess-0.70.9/py3.8/Modules/_multiprocess/multiprocess.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/Modules/_multiprocess/posixshmem.c` & `multiprocess-0.70.9/py3.8/Modules/_multiprocess/posixshmem.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/Modules/_multiprocess/semaphore.c` & `multiprocess-0.70.9/py3.8/Modules/_multiprocess/semaphore.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/Modules/_multiprocess/clinic/posixshmem.c.h` & `multiprocess-0.70.9/py3.8/Modules/_multiprocess/clinic/posixshmem.c.h`

 * *Files 3% similar despite different names*

```diff
@@ -31,15 +31,15 @@
     int _return_value;
 
     args = _PyArg_UnpackKeywords(args, nargs, NULL, kwnames, &_parser, 2, 3, 0, argsbuf);
     if (!args) {
         goto exit;
     }
     if (!PyUnicode_Check(args[0])) {
-        _PyArg_BadArgument("shm_open", 1, "str", args[0]);
+        _PyArg_BadArgument("shm_open", "argument 'path'", "str", args[0]);
         goto exit;
     }
     if (PyUnicode_READY(args[0]) == -1) {
         goto exit;
     }
     path = args[0];
     if (PyFloat_Check(args[1])) {
@@ -104,15 +104,15 @@
     PyObject *path;
 
     args = _PyArg_UnpackKeywords(args, nargs, NULL, kwnames, &_parser, 1, 1, 0, argsbuf);
     if (!args) {
         goto exit;
     }
     if (!PyUnicode_Check(args[0])) {
-        _PyArg_BadArgument("shm_unlink", 1, "str", args[0]);
+        _PyArg_BadArgument("shm_unlink", "argument 'path'", "str", args[0]);
         goto exit;
     }
     if (PyUnicode_READY(args[0]) == -1) {
         goto exit;
     }
     path = args[0];
     return_value = _posixshmem_shm_unlink_impl(module, path);
@@ -126,8 +126,8 @@
 #ifndef _POSIXSHMEM_SHM_OPEN_METHODDEF
     #define _POSIXSHMEM_SHM_OPEN_METHODDEF
 #endif /* !defined(_POSIXSHMEM_SHM_OPEN_METHODDEF) */
 
 #ifndef _POSIXSHMEM_SHM_UNLINK_METHODDEF
     #define _POSIXSHMEM_SHM_UNLINK_METHODDEF
 #endif /* !defined(_POSIXSHMEM_SHM_UNLINK_METHODDEF) */
-/*[clinic end generated code: output=be42e23c18677c0f input=a9049054013a1b77]*/
+/*[clinic end generated code: output=9132861c61d8c2d8 input=a9049054013a1b77]*/
```

### Comparing `multiprocess-0.70.8/py3.8/examples/benchmarks.py` & `multiprocess-0.70.9/py3.8/examples/benchmarks.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 #
 # Simple benchmarks for the processing package
 #
 
 import time, sys, multiprocess as processing, threading, queue as Queue, gc
 processing.freezeSupport = processing.freeze_support
-xrange = range
 
 if sys.platform == 'win32':
     _timer = time.clock
 else:
     _timer = time.time
 
 delta = 1
@@ -18,17 +17,17 @@
 
 def queuespeed_func(q, c, iterations):
     a = '0' * 256
     c.acquire()
     c.notify()
     c.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         q.put(a)
-#    q.putMany((a for i in xrange(iterations))
+#    q.putMany((a for i in range(iterations))
 
     q.put('STOP')
 
 def test_queuespeed(Process, q, c):
     elapsed = 0
     iterations = 1
 
@@ -59,15 +58,15 @@
 
 def pipe_func(c, cond, iterations):
     a = '0' * 256
     cond.acquire()
     cond.notify()
     cond.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         c.send(a)
 
     c.send('STOP')
 
 def test_pipespeed():
     c, d = processing.Pipe()
     cond = processing.Condition()
@@ -103,15 +102,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             a = seq[5]
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
 
@@ -123,15 +122,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             l.acquire()
             l.release()
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
@@ -139,15 +138,15 @@
 
 #### TEST_CONDITION
 
 def conditionspeed_func(c, N):
     c.acquire()
     c.notify()
 
-    for i in xrange(N):
+    for i in range(N):
         c.wait()
         c.notify()
 
     c.release()
 
 def test_conditionspeed(Process, c):
     elapsed = 0
@@ -160,15 +159,15 @@
         p = Process(target=conditionspeed_func, args=(c, iterations))
         p.start()
 
         c.wait()
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             c.notify()
             c.wait()
 
         elapsed = _timer()-t
 
         c.release()
         p.join()
```

### Comparing `multiprocess-0.70.8/py3.8/examples/ex_newtype.py` & `multiprocess-0.70.9/py2.7/examples/ex_newtype.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,25 +1,24 @@
 #
 # This module shows how to use arbitrary callables with a subclass of
 # `BaseManager`.
 #
 
 from multiprocess import freeze_support as freezeSupport
 from multiprocess.managers import BaseManager, BaseProxy
-xrange = range
 
 ##
 
 class Foo(object):
     def f(self):
-        print('you called Foo.f()')
+        print 'you called Foo.f()'
     def g(self):
-        print('you called Foo.g()')
+        print 'you called Foo.g()'
     def _h(self):
-        print('you called Foo._h()')
+        print 'you called Foo._h()'
 
 # A simple generator function
 def baz():
     for i in xrange(10):
         yield i*i
 
 # Proxy type for generator objects
@@ -44,35 +43,35 @@
 
 ##
 
 def test():
     manager = MyManager()
     manager.start()
 
-    print('-' * 20)
+    print '-' * 20
 
     f1 = manager.Foo1()
     f1.f()
     f1.g()
     assert not hasattr(f1, '_h')
 
-    print('-' * 20)
+    print '-' * 20
 
     f2 = manager.Foo2()
     f2.g()
     f2._h()
     assert not hasattr(f2, 'f')
 
-    print('-' * 20)
+    print '-' * 20
 
     it = manager.baz()
 
     for i in it:
-        print('<%d>' % i, end=' ')
+        print '<%d>' % i,
 
-    print()
+    print
 
 ##
 
 if __name__ == '__main__':
     freezeSupport()
     test()
```

### Comparing `multiprocess-0.70.8/py3.8/examples/ex_pool.py` & `multiprocess-0.70.9/py3.8/examples/ex_pool.py`

 * *Files 6% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 # A test of `processing.Pool` class
 #
 
 from multiprocess import Pool, TimeoutError
 from multiprocess import cpu_count as cpuCount, current_process as currentProcess, freeze_support as freezeSupport, active_children as activeChildren
 
 import time, random, sys
-xrange = range
 
 #
 # Functions used by test code
 #
 
 def calculate(func, args):
     result = func(*args)
@@ -87,26 +86,26 @@
     # Simple benchmarks
     #
 
     N = 100000
     print('def pow3(x): return x**3')
     
     t = time.time()
-    A = list(map(pow3, xrange(N)))
-    print('\tmap(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    A = list(map(pow3, range(N)))
+    print('\tmap(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
     
     t = time.time()
-    B = pool.map(pow3, xrange(N))
-    print('\tpool.map(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    B = pool.map(pow3, range(N))
+    print('\tpool.map(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
 
     t = time.time()
-    C = list(pool.imap(pow3, xrange(N), chunksize=N//8))
-    print('\tlist(pool.imap(pow3, xrange(%d), chunksize=%d)):\n\t\t%s' \
+    C = list(pool.imap(pow3, range(N), chunksize=N//8))
+    print('\tlist(pool.imap(pow3, range(%d), chunksize=%d)):\n\t\t%s' \
           ' seconds' % (N, N//8, time.time() - t))
     
     assert A == B == C, (len(A), len(B), len(C))
     print()
     
     L = [None] * 1000000
     print('def noop(x): pass')
```

### Comparing `multiprocess-0.70.8/py3.8/examples/ex_synchronize.py` & `multiprocess-0.70.9/py3.8/examples/ex_synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/examples/ex_webserver.py` & `multiprocess-0.70.9/py3.8/examples/ex_webserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/examples/ex_workers.py` & `multiprocess-0.70.9/py3.8/examples/ex_workers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/CHANGES.html` & `multiprocess-0.70.9/py3.8/doc/CHANGES.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/connection-objects.html` & `multiprocess-0.70.9/py3.8/doc/connection-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/connection-objects.txt` & `multiprocess-0.70.9/py3.8/doc/connection-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/connection-ref.html` & `multiprocess-0.70.9/py3.8/doc/connection-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/connection-ref.txt` & `multiprocess-0.70.9/py3.8/doc/connection-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/COPYING.html` & `multiprocess-0.70.9/py3.8/doc/COPYING.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/html4css1.css` & `multiprocess-0.70.9/py3.8/doc/html4css1.css`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/index.html` & `multiprocess-0.70.9/py3.8/doc/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/index.txt` & `multiprocess-0.70.9/py3.8/doc/index.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/INSTALL.html` & `multiprocess-0.70.9/py3.8/doc/INSTALL.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/intro.html` & `multiprocess-0.70.9/py3.8/doc/intro.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/intro.txt` & `multiprocess-0.70.9/py3.8/doc/intro.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/manager-objects.html` & `multiprocess-0.70.9/py3.8/doc/manager-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/manager-objects.txt` & `multiprocess-0.70.9/py3.8/doc/manager-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/pool-objects.html` & `multiprocess-0.70.9/py3.8/doc/pool-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/pool-objects.txt` & `multiprocess-0.70.9/py3.8/doc/pool-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/process-objects.html` & `multiprocess-0.70.9/py3.8/doc/process-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/process-objects.txt` & `multiprocess-0.70.9/py3.8/doc/process-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/processing-ref.html` & `multiprocess-0.70.9/py3.8/doc/processing-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/processing-ref.txt` & `multiprocess-0.70.9/py3.8/doc/processing-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/programming-guidelines.html` & `multiprocess-0.70.9/py3.8/doc/programming-guidelines.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/programming-guidelines.txt` & `multiprocess-0.70.9/py3.8/doc/programming-guidelines.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/proxy-objects.html` & `multiprocess-0.70.9/py3.8/doc/proxy-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/proxy-objects.txt` & `multiprocess-0.70.9/py3.8/doc/proxy-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/queue-objects.html` & `multiprocess-0.70.9/py3.8/doc/queue-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/queue-objects.txt` & `multiprocess-0.70.9/py3.8/doc/queue-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/sharedctypes.html` & `multiprocess-0.70.9/py3.8/doc/sharedctypes.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/sharedctypes.txt` & `multiprocess-0.70.9/py3.8/doc/sharedctypes.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/tests.html` & `multiprocess-0.70.9/py3.8/doc/tests.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/tests.txt` & `multiprocess-0.70.9/py3.8/doc/tests.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.8/doc/THANKS.html` & `multiprocess-0.70.9/py3.8/doc/THANKS.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/index.html` & `multiprocess-0.70.9/py3.7/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/README_MODS` & `multiprocess-0.70.9/py3.7/README_MODS`

 * *Files 1% similar despite different names*

```diff
@@ -393,8 +393,9 @@
 >         dt = time.monotonic() - start_time
 >         if dt > 60.0:
 >             raise RuntimeError("Timed out waiting for results (%.1f sec)" % dt)
 > 
 94a103,104
 > 
 > pool.join()
-
+# ----------------------------------------------------------------------
+ADDED *args, **kwds for ForkingPickler in __init__, dump, and dumps
```

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/__init__.py` & `multiprocess-0.70.9/py3.7/multiprocess/__init__.py`

 * *Files 15% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 # Copyright (c) 2006-2008, R Oudkerk
 # Licensed to PSF under a Contributor Agreement.
 #
 
 import sys
 from . import context
 
-__version__ = '0.70.8'
+__version__ = '0.70.9'
 
 #
 # Copy stuff from default context
 #
 
 globals().update((name, getattr(context._default_context, name))
                  for name in context._default_context.__all__)
```

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/connection.py` & `multiprocess-0.70.9/py3.7/multiprocess/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/context.py` & `multiprocess-0.70.9/py3.7/multiprocess/context.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/forkserver.py` & `multiprocess-0.70.9/py3.7/multiprocess/forkserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/heap.py` & `multiprocess-0.70.9/py3.7/multiprocess/heap.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/managers.py` & `multiprocess-0.70.9/py3.7/multiprocess/managers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/pool.py` & `multiprocess-0.70.9/py3.7/multiprocess/pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/popen_fork.py` & `multiprocess-0.70.9/py3.7/multiprocess/popen_fork.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/popen_forkserver.py` & `multiprocess-0.70.9/py3.7/multiprocess/popen_forkserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/popen_spawn_posix.py` & `multiprocess-0.70.9/py3.7/multiprocess/popen_spawn_posix.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/popen_spawn_win32.py` & `multiprocess-0.70.9/py3.7/multiprocess/popen_spawn_win32.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/process.py` & `multiprocess-0.70.9/py3.7/multiprocess/process.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/queues.py` & `multiprocess-0.70.9/py3.7/multiprocess/queues.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/reduction.py` & `multiprocess-0.70.9/py3.7/multiprocess/reduction.py`

 * *Files 2% similar despite different names*

```diff
@@ -34,37 +34,37 @@
 #
 
 class ForkingPickler(pickle.Pickler):
     '''Pickler subclass used by multiprocess.'''
     _extra_reducers = {}
     _copyreg_dispatch_table = copyreg.dispatch_table
 
-    def __init__(self, *args):
-        super().__init__(*args)
+    def __init__(self, *args, **kwds):
+        super().__init__(*args, **kwds)
         self.dispatch_table = self._copyreg_dispatch_table.copy()
         self.dispatch_table.update(self._extra_reducers)
 
     @classmethod
     def register(cls, type, reduce):
         '''Register a reduce function for a type.'''
         cls._extra_reducers[type] = reduce
 
     @classmethod
-    def dumps(cls, obj, protocol=None):
+    def dumps(cls, obj, protocol=None, *args, **kwds):
         buf = io.BytesIO()
-        cls(buf, protocol).dump(obj)
+        cls(buf, protocol, *args, **kwds).dump(obj)
         return buf.getbuffer()
 
     loads = pickle.loads
 
 register = ForkingPickler.register
 
-def dump(obj, file, protocol=None):
+def dump(obj, file, protocol=None, *args, **kwds):
     '''Replacement for pickle.dump() using ForkingPickler.'''
-    ForkingPickler(file, protocol).dump(obj)
+    ForkingPickler(file, protocol, *args, **kwds).dump(obj)
 
 #
 # Platform specific definitions
 #
 
 if sys.platform == 'win32':
     # Windows
```

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/resource_sharer.py` & `multiprocess-0.70.9/py3.7/multiprocess/resource_sharer.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/semaphore_tracker.py` & `multiprocess-0.70.9/py3.7/multiprocess/semaphore_tracker.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/sharedctypes.py` & `multiprocess-0.70.9/py3.7/multiprocess/sharedctypes.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/spawn.py` & `multiprocess-0.70.9/py3.7/multiprocess/spawn.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/synchronize.py` & `multiprocess-0.70.9/py3.7/multiprocess/synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/util.py` & `multiprocess-0.70.9/py3.6/multiprocess/util.py`

 * *Files 2% similar despite different names*

```diff
@@ -55,15 +55,15 @@
 
 def sub_warning(msg, *args):
     if _logger:
         _logger.log(SUBWARNING, msg, *args)
 
 def get_logger():
     '''
-    Returns logger used by multiprocess
+    Returns logger used by multiprocessing
     '''
     global _logger
     import logging
 
     logging._acquireLock()
     try:
         if not _logger:
@@ -145,23 +145,20 @@
 
 
 class Finalize(object):
     '''
     Class which supports object finalization using weakrefs
     '''
     def __init__(self, obj, callback, args=(), kwargs=None, exitpriority=None):
-        if (exitpriority is not None) and not isinstance(exitpriority,int):
-            raise TypeError(
-                "Exitpriority ({0!r}) must be None or int, not {1!s}".format(
-                    exitpriority, type(exitpriority)))
+        assert exitpriority is None or type(exitpriority) is int
 
         if obj is not None:
             self._weakref = weakref.ref(obj, self)
-        elif exitpriority is None:
-            raise ValueError("Without object, exitpriority cannot be None")
+        else:
+            assert exitpriority is not None
 
         self._callback = callback
         self._args = args
         self._kwargs = kwargs or {}
         self._key = (exitpriority, next(_finalizer_counter))
         self._pid = os.getpid()
```

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/tests/__init__.py` & `multiprocess-0.70.9/py3.7/multiprocess/tests/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -22,15 +22,15 @@
 import weakref
 import test.support
 import test.support.script_helper
 from test import support
 
 
 # Skip tests if _multiprocessing wasn't built.
-_multiprocessing = test.support.import_module('_multiprocess')
+_multiprocessing = test.support.import_module('_multiprocessing')
 # Skip tests if sem_open implementation is broken.
 test.support.import_module('multiprocess.synchronize')
 # import threading after _multiprocessing to raise a more relevant error
 # message: "No module named _multiprocessing". _multiprocessing is not compiled
 # without thread support.
 import threading
```

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/tests/__main__.py` & `multiprocess-0.70.9/py3.7/multiprocess/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/tests/test_multiprocessing_main_handling.py` & `multiprocess-0.70.9/py3.7/multiprocess/tests/test_multiprocessing_main_handling.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 # tests __main__ module handling in multiprocessing
 from test import support
 # Skip tests if _multiprocessing wasn't built.
-support.import_module('_multiprocess')
+support.import_module('_multiprocessing')
 
 import importlib
 import importlib.machinery
 import unittest
 import sys
 import os
 import os.path
```

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/dummy/__init__.py` & `multiprocess-0.70.9/py3.7/multiprocess/dummy/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/multiprocess/dummy/connection.py` & `multiprocess-0.70.9/py3.7/multiprocess/dummy/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/Modules/_multiprocess/multiprocess.c` & `multiprocess-0.70.9/py3.7/Modules/_multiprocess/multiprocess.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/Modules/_multiprocess/multiprocess.h` & `multiprocess-0.70.9/py3.7/Modules/_multiprocess/multiprocess.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/Modules/_multiprocess/semaphore.c` & `multiprocess-0.70.9/py3.7/Modules/_multiprocess/semaphore.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/examples/benchmarks.py` & `multiprocess-0.70.9/py3.7/examples/benchmarks.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 #
 # Simple benchmarks for the processing package
 #
 
 import time, sys, multiprocess as processing, threading, queue as Queue, gc
 processing.freezeSupport = processing.freeze_support
-xrange = range
 
 if sys.platform == 'win32':
     _timer = time.clock
 else:
     _timer = time.time
 
 delta = 1
@@ -18,17 +17,17 @@
 
 def queuespeed_func(q, c, iterations):
     a = '0' * 256
     c.acquire()
     c.notify()
     c.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         q.put(a)
-#    q.putMany((a for i in xrange(iterations))
+#    q.putMany((a for i in range(iterations))
 
     q.put('STOP')
 
 def test_queuespeed(Process, q, c):
     elapsed = 0
     iterations = 1
 
@@ -59,15 +58,15 @@
 
 def pipe_func(c, cond, iterations):
     a = '0' * 256
     cond.acquire()
     cond.notify()
     cond.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         c.send(a)
 
     c.send('STOP')
 
 def test_pipespeed():
     c, d = processing.Pipe()
     cond = processing.Condition()
@@ -103,15 +102,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             a = seq[5]
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
 
@@ -123,15 +122,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             l.acquire()
             l.release()
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
@@ -139,15 +138,15 @@
 
 #### TEST_CONDITION
 
 def conditionspeed_func(c, N):
     c.acquire()
     c.notify()
 
-    for i in xrange(N):
+    for i in range(N):
         c.wait()
         c.notify()
 
     c.release()
 
 def test_conditionspeed(Process, c):
     elapsed = 0
@@ -160,15 +159,15 @@
         p = Process(target=conditionspeed_func, args=(c, iterations))
         p.start()
 
         c.wait()
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             c.notify()
             c.wait()
 
         elapsed = _timer()-t
 
         c.release()
         p.join()
```

### Comparing `multiprocess-0.70.8/py3.7/examples/ex_newtype.py` & `multiprocess-0.70.9/py2.6/examples/ex_newtype.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,25 +1,24 @@
 #
 # This module shows how to use arbitrary callables with a subclass of
 # `BaseManager`.
 #
 
 from multiprocess import freeze_support as freezeSupport
 from multiprocess.managers import BaseManager, BaseProxy
-xrange = range
 
 ##
 
 class Foo(object):
     def f(self):
-        print('you called Foo.f()')
+        print 'you called Foo.f()'
     def g(self):
-        print('you called Foo.g()')
+        print 'you called Foo.g()'
     def _h(self):
-        print('you called Foo._h()')
+        print 'you called Foo._h()'
 
 # A simple generator function
 def baz():
     for i in xrange(10):
         yield i*i
 
 # Proxy type for generator objects
@@ -44,35 +43,35 @@
 
 ##
 
 def test():
     manager = MyManager()
     manager.start()
 
-    print('-' * 20)
+    print '-' * 20
 
     f1 = manager.Foo1()
     f1.f()
     f1.g()
     assert not hasattr(f1, '_h')
 
-    print('-' * 20)
+    print '-' * 20
 
     f2 = manager.Foo2()
     f2.g()
     f2._h()
     assert not hasattr(f2, 'f')
 
-    print('-' * 20)
+    print '-' * 20
 
     it = manager.baz()
 
     for i in it:
-        print('<%d>' % i, end=' ')
+        print '<%d>' % i,
 
-    print()
+    print
 
 ##
 
 if __name__ == '__main__':
     freezeSupport()
     test()
```

### Comparing `multiprocess-0.70.8/py3.7/examples/ex_pool.py` & `multiprocess-0.70.9/py3.7/examples/ex_pool.py`

 * *Files 6% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 # A test of `processing.Pool` class
 #
 
 from multiprocess import Pool, TimeoutError
 from multiprocess import cpu_count as cpuCount, current_process as currentProcess, freeze_support as freezeSupport, active_children as activeChildren
 
 import time, random, sys
-xrange = range
 
 #
 # Functions used by test code
 #
 
 def calculate(func, args):
     result = func(*args)
@@ -87,26 +86,26 @@
     # Simple benchmarks
     #
 
     N = 100000
     print('def pow3(x): return x**3')
     
     t = time.time()
-    A = list(map(pow3, xrange(N)))
-    print('\tmap(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    A = list(map(pow3, range(N)))
+    print('\tmap(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
     
     t = time.time()
-    B = pool.map(pow3, xrange(N))
-    print('\tpool.map(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    B = pool.map(pow3, range(N))
+    print('\tpool.map(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
 
     t = time.time()
-    C = list(pool.imap(pow3, xrange(N), chunksize=N//8))
-    print('\tlist(pool.imap(pow3, xrange(%d), chunksize=%d)):\n\t\t%s' \
+    C = list(pool.imap(pow3, range(N), chunksize=N//8))
+    print('\tlist(pool.imap(pow3, range(%d), chunksize=%d)):\n\t\t%s' \
           ' seconds' % (N, N//8, time.time() - t))
     
     assert A == B == C, (len(A), len(B), len(C))
     print()
     
     L = [None] * 1000000
     print('def noop(x): pass')
```

### Comparing `multiprocess-0.70.8/py3.7/examples/ex_synchronize.py` & `multiprocess-0.70.9/py3.7/examples/ex_synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/examples/ex_webserver.py` & `multiprocess-0.70.9/py3.7/examples/ex_webserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/examples/ex_workers.py` & `multiprocess-0.70.9/py3.7/examples/ex_workers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/CHANGES.html` & `multiprocess-0.70.9/py3.7/doc/CHANGES.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/connection-objects.html` & `multiprocess-0.70.9/py3.7/doc/connection-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/connection-objects.txt` & `multiprocess-0.70.9/py3.7/doc/connection-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/connection-ref.html` & `multiprocess-0.70.9/py3.7/doc/connection-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/connection-ref.txt` & `multiprocess-0.70.9/py3.7/doc/connection-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/COPYING.html` & `multiprocess-0.70.9/py3.7/doc/COPYING.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/html4css1.css` & `multiprocess-0.70.9/py3.7/doc/html4css1.css`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/index.html` & `multiprocess-0.70.9/py3.7/doc/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/index.txt` & `multiprocess-0.70.9/py3.7/doc/index.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/INSTALL.html` & `multiprocess-0.70.9/py3.7/doc/INSTALL.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/intro.html` & `multiprocess-0.70.9/py3.7/doc/intro.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/intro.txt` & `multiprocess-0.70.9/py3.7/doc/intro.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/manager-objects.html` & `multiprocess-0.70.9/py3.7/doc/manager-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/manager-objects.txt` & `multiprocess-0.70.9/py3.7/doc/manager-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/pool-objects.html` & `multiprocess-0.70.9/py3.7/doc/pool-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/pool-objects.txt` & `multiprocess-0.70.9/py3.7/doc/pool-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/process-objects.html` & `multiprocess-0.70.9/py3.7/doc/process-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/process-objects.txt` & `multiprocess-0.70.9/py3.7/doc/process-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/processing-ref.html` & `multiprocess-0.70.9/py3.7/doc/processing-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/processing-ref.txt` & `multiprocess-0.70.9/py3.7/doc/processing-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/programming-guidelines.html` & `multiprocess-0.70.9/py3.7/doc/programming-guidelines.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/programming-guidelines.txt` & `multiprocess-0.70.9/py3.7/doc/programming-guidelines.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/proxy-objects.html` & `multiprocess-0.70.9/py3.7/doc/proxy-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/proxy-objects.txt` & `multiprocess-0.70.9/py3.7/doc/proxy-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/queue-objects.html` & `multiprocess-0.70.9/py3.7/doc/queue-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/queue-objects.txt` & `multiprocess-0.70.9/py3.7/doc/queue-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/sharedctypes.html` & `multiprocess-0.70.9/py3.7/doc/sharedctypes.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/sharedctypes.txt` & `multiprocess-0.70.9/py3.7/doc/sharedctypes.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/tests.html` & `multiprocess-0.70.9/py3.7/doc/tests.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/tests.txt` & `multiprocess-0.70.9/py3.7/doc/tests.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.7/doc/THANKS.html` & `multiprocess-0.70.9/py3.7/doc/THANKS.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/index.html` & `multiprocess-0.70.9/py3.6/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/README_MODS` & `multiprocess-0.70.9/py3.6/README_MODS`

 * *Files 1% similar despite different names*

```diff
@@ -602,7 +602,9 @@
 <     if time.time() > deadline:
 <         raise RuntimeError("Timed out waiting for results")
 ---
 >     # up to 1 min to report the results
 >     dt = time.monotonic() - start_time
 >     if dt > 60.0:
 >         raise RuntimeError("Timed out waiting for results (%.1f sec)" % dt)
+# ----------------------------------------------------------------------
+ADDED *args, **kwds for ForkingPickler in __init__, dump, and dumps
```

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/__init__.py` & `multiprocess-0.70.9/py3.6/multiprocess/__init__.py`

 * *Files 15% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 # Copyright (c) 2006-2008, R Oudkerk
 # Licensed to PSF under a Contributor Agreement.
 #
 
 import sys
 from . import context
 
-__version__ = '0.70.8'
+__version__ = '0.70.9'
 
 #
 # Copy stuff from default context
 #
 
 globals().update((name, getattr(context._default_context, name))
                  for name in context._default_context.__all__)
```

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/connection.py` & `multiprocess-0.70.9/py3.6/multiprocess/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/context.py` & `multiprocess-0.70.9/py3.6/multiprocess/context.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/forkserver.py` & `multiprocess-0.70.9/py3.6/multiprocess/forkserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/heap.py` & `multiprocess-0.70.9/py3.6/multiprocess/heap.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/managers.py` & `multiprocess-0.70.9/py3.6/multiprocess/managers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/pool.py` & `multiprocess-0.70.9/py3.6/multiprocess/pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/popen_fork.py` & `multiprocess-0.70.9/py3.6/multiprocess/popen_fork.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/popen_forkserver.py` & `multiprocess-0.70.9/py3.6/multiprocess/popen_forkserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/popen_spawn_posix.py` & `multiprocess-0.70.9/py3.6/multiprocess/popen_spawn_posix.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/popen_spawn_win32.py` & `multiprocess-0.70.9/py3.6/multiprocess/popen_spawn_win32.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/process.py` & `multiprocess-0.70.9/py3.6/multiprocess/process.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/queues.py` & `multiprocess-0.70.9/py3.6/multiprocess/queues.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/reduction.py` & `multiprocess-0.70.9/py3.6/multiprocess/reduction.py`

 * *Files 2% similar despite different names*

```diff
@@ -34,37 +34,37 @@
 #
 
 class ForkingPickler(pickle.Pickler):
     '''Pickler subclass used by multiprocessing.'''
     _extra_reducers = {}
     _copyreg_dispatch_table = copyreg.dispatch_table
 
-    def __init__(self, *args):
-        super().__init__(*args)
+    def __init__(self, *args, **kwds):
+        super().__init__(*args, **kwds)
         self.dispatch_table = self._copyreg_dispatch_table.copy()
         self.dispatch_table.update(self._extra_reducers)
 
     @classmethod
     def register(cls, type, reduce):
         '''Register a reduce function for a type.'''
         cls._extra_reducers[type] = reduce
 
     @classmethod
-    def dumps(cls, obj, protocol=None):
+    def dumps(cls, obj, protocol=None, *args, **kwds):
         buf = io.BytesIO()
-        cls(buf, protocol).dump(obj)
+        cls(buf, protocol, *args, **kwds).dump(obj)
         return buf.getbuffer()
 
     loads = pickle.loads
 
 register = ForkingPickler.register
 
-def dump(obj, file, protocol=None):
+def dump(obj, file, protocol=None, *args, **kwds):
     '''Replacement for pickle.dump() using ForkingPickler.'''
-    ForkingPickler(file, protocol).dump(obj)
+    ForkingPickler(file, protocol, *args, **kwds).dump(obj)
 
 #
 # Platform specific definitions
 #
 
 if sys.platform == 'win32':
     # Windows
```

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/resource_sharer.py` & `multiprocess-0.70.9/py3.6/multiprocess/resource_sharer.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/semaphore_tracker.py` & `multiprocess-0.70.9/py3.6/multiprocess/semaphore_tracker.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/sharedctypes.py` & `multiprocess-0.70.9/py3.6/multiprocess/sharedctypes.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/spawn.py` & `multiprocess-0.70.9/py3.6/multiprocess/spawn.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/synchronize.py` & `multiprocess-0.70.9/py3.6/multiprocess/synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/util.py` & `multiprocess-0.70.9/py3.5/multiprocess/util.py`

 * *Files 3% similar despite different names*

```diff
@@ -385,28 +385,14 @@
         except:
             os.close(fd)
             raise
     except (OSError, ValueError):
         pass
 
 #
-# Flush standard streams, if any
-#
-
-def _flush_std_streams():
-    try:
-        sys.stdout.flush()
-    except (AttributeError, ValueError):
-        pass
-    try:
-        sys.stderr.flush()
-    except (AttributeError, ValueError):
-        pass
-
-#
 # Start a program with only specified fds kept open
 #
 
 def spawnv_passfds(path, args, passfds):
     import _posixsubprocess
     passfds = tuple(sorted(map(int, passfds)))
     errpipe_read, errpipe_write = os.pipe()
```

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/tests/__init__.py` & `multiprocess-0.70.9/py3.6/multiprocess/tests/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -19,15 +19,15 @@
 import struct
 import operator
 import test.support
 import test.support.script_helper
 
 
 # Skip tests if _multiprocessing wasn't built.
-_multiprocessing = test.support.import_module('_multiprocess')
+_multiprocessing = test.support.import_module('_multiprocessing')
 # Skip tests if sem_open implementation is broken.
 test.support.import_module('multiprocess.synchronize')
 # import threading after _multiprocessing to raise a more relevant error
 # message: "No module named _multiprocessing". _multiprocessing is not compiled
 # without thread support.
 import threading
```

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/tests/__main__.py` & `multiprocess-0.70.9/py3.6/multiprocess/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/tests/test_multiprocessing_main_handling.py` & `multiprocess-0.70.9/py3.6/multiprocess/tests/test_multiprocessing_main_handling.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # tests __main__ module handling in multiprocessing
 from test import support
 # Skip tests if _thread or _multiprocessing wasn't built.
 support.import_module('_thread')
-support.import_module('_multiprocess')
+support.import_module('_multiprocessing')
 
 import importlib
 import importlib.machinery
 import unittest
 import sys
 import os
 import os.path
```

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/dummy/__init__.py` & `multiprocess-0.70.9/py3.6/multiprocess/dummy/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/multiprocess/dummy/connection.py` & `multiprocess-0.70.9/py3.6/multiprocess/dummy/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/Modules/_multiprocess/multiprocess.c` & `multiprocess-0.70.9/py3.6/Modules/_multiprocess/multiprocess.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/Modules/_multiprocess/multiprocess.h` & `multiprocess-0.70.9/py3.6/Modules/_multiprocess/multiprocess.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/Modules/_multiprocess/semaphore.c` & `multiprocess-0.70.9/py3.6/Modules/_multiprocess/semaphore.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/examples/benchmarks.py` & `multiprocess-0.70.9/py3.6/examples/benchmarks.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 #
 # Simple benchmarks for the processing package
 #
 
 import time, sys, multiprocess as processing, threading, queue as Queue, gc
 processing.freezeSupport = processing.freeze_support
-xrange = range
 
 if sys.platform == 'win32':
     _timer = time.clock
 else:
     _timer = time.time
 
 delta = 1
@@ -18,17 +17,17 @@
 
 def queuespeed_func(q, c, iterations):
     a = '0' * 256
     c.acquire()
     c.notify()
     c.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         q.put(a)
-#    q.putMany((a for i in xrange(iterations))
+#    q.putMany((a for i in range(iterations))
 
     q.put('STOP')
 
 def test_queuespeed(Process, q, c):
     elapsed = 0
     iterations = 1
 
@@ -59,15 +58,15 @@
 
 def pipe_func(c, cond, iterations):
     a = '0' * 256
     cond.acquire()
     cond.notify()
     cond.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         c.send(a)
 
     c.send('STOP')
 
 def test_pipespeed():
     c, d = processing.Pipe()
     cond = processing.Condition()
@@ -103,15 +102,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             a = seq[5]
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
 
@@ -123,15 +122,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             l.acquire()
             l.release()
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
@@ -139,15 +138,15 @@
 
 #### TEST_CONDITION
 
 def conditionspeed_func(c, N):
     c.acquire()
     c.notify()
 
-    for i in xrange(N):
+    for i in range(N):
         c.wait()
         c.notify()
 
     c.release()
 
 def test_conditionspeed(Process, c):
     elapsed = 0
@@ -160,15 +159,15 @@
         p = Process(target=conditionspeed_func, args=(c, iterations))
         p.start()
 
         c.wait()
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             c.notify()
             c.wait()
 
         elapsed = _timer()-t
 
         c.release()
         p.join()
```

### Comparing `multiprocess-0.70.8/py3.6/examples/ex_newtype.py` & `multiprocess-0.70.9/py3.8/examples/ex_newtype.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,37 +1,36 @@
 #
 # This module shows how to use arbitrary callables with a subclass of
 # `BaseManager`.
 #
 
 from multiprocess import freeze_support as freezeSupport
-from multiprocess.managers import BaseManager, BaseProxy
-xrange = range
+from multiprocess.managers import BaseManager, IteratorProxy as BaseProxy
 
 ##
 
 class Foo(object):
     def f(self):
         print('you called Foo.f()')
     def g(self):
         print('you called Foo.g()')
     def _h(self):
         print('you called Foo._h()')
 
 # A simple generator function
 def baz():
-    for i in xrange(10):
+    for i in range(10):
         yield i*i
 
 # Proxy type for generator objects
 class GeneratorProxy(BaseProxy):
     def __iter__(self):
         return self
-    def next(self):
-        return self._callmethod('next')
+    def __next__(self):
+        return self._callmethod('__next__')
 
 ##
 
 class MyManager(BaseManager): pass
 
 # register the Foo class; make all public methods accessible via proxy
 MyManager.register('Foo1', Foo)
```

### Comparing `multiprocess-0.70.8/py3.6/examples/ex_pool.py` & `multiprocess-0.70.9/py3.6/examples/ex_pool.py`

 * *Files 6% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 # A test of `processing.Pool` class
 #
 
 from multiprocess import Pool, TimeoutError
 from multiprocess import cpu_count as cpuCount, current_process as currentProcess, freeze_support as freezeSupport, active_children as activeChildren
 
 import time, random, sys
-xrange = range
 
 #
 # Functions used by test code
 #
 
 def calculate(func, args):
     result = func(*args)
@@ -87,26 +86,26 @@
     # Simple benchmarks
     #
 
     N = 100000
     print('def pow3(x): return x**3')
     
     t = time.time()
-    A = list(map(pow3, xrange(N)))
-    print('\tmap(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    A = list(map(pow3, range(N)))
+    print('\tmap(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
     
     t = time.time()
-    B = pool.map(pow3, xrange(N))
-    print('\tpool.map(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    B = pool.map(pow3, range(N))
+    print('\tpool.map(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
 
     t = time.time()
-    C = list(pool.imap(pow3, xrange(N), chunksize=N//8))
-    print('\tlist(pool.imap(pow3, xrange(%d), chunksize=%d)):\n\t\t%s' \
+    C = list(pool.imap(pow3, range(N), chunksize=N//8))
+    print('\tlist(pool.imap(pow3, range(%d), chunksize=%d)):\n\t\t%s' \
           ' seconds' % (N, N//8, time.time() - t))
     
     assert A == B == C, (len(A), len(B), len(C))
     print()
     
     L = [None] * 1000000
     print('def noop(x): pass')
```

### Comparing `multiprocess-0.70.8/py3.6/examples/ex_synchronize.py` & `multiprocess-0.70.9/py3.6/examples/ex_synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/examples/ex_webserver.py` & `multiprocess-0.70.9/py3.6/examples/ex_webserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/examples/ex_workers.py` & `multiprocess-0.70.9/py3.6/examples/ex_workers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/CHANGES.html` & `multiprocess-0.70.9/py3.6/doc/CHANGES.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/connection-objects.html` & `multiprocess-0.70.9/py3.6/doc/connection-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/connection-objects.txt` & `multiprocess-0.70.9/py3.6/doc/connection-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/connection-ref.html` & `multiprocess-0.70.9/py3.6/doc/connection-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/connection-ref.txt` & `multiprocess-0.70.9/py3.6/doc/connection-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/COPYING.html` & `multiprocess-0.70.9/py3.6/doc/COPYING.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/html4css1.css` & `multiprocess-0.70.9/py3.6/doc/html4css1.css`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/index.html` & `multiprocess-0.70.9/py3.6/doc/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/index.txt` & `multiprocess-0.70.9/py3.6/doc/index.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/INSTALL.html` & `multiprocess-0.70.9/py3.6/doc/INSTALL.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/intro.html` & `multiprocess-0.70.9/py3.6/doc/intro.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/intro.txt` & `multiprocess-0.70.9/py3.6/doc/intro.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/manager-objects.html` & `multiprocess-0.70.9/py3.6/doc/manager-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/manager-objects.txt` & `multiprocess-0.70.9/py3.6/doc/manager-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/pool-objects.html` & `multiprocess-0.70.9/py3.6/doc/pool-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/pool-objects.txt` & `multiprocess-0.70.9/py3.6/doc/pool-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/process-objects.html` & `multiprocess-0.70.9/py3.6/doc/process-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/process-objects.txt` & `multiprocess-0.70.9/py3.6/doc/process-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/processing-ref.html` & `multiprocess-0.70.9/py3.6/doc/processing-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/processing-ref.txt` & `multiprocess-0.70.9/py3.6/doc/processing-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/programming-guidelines.html` & `multiprocess-0.70.9/py3.6/doc/programming-guidelines.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/programming-guidelines.txt` & `multiprocess-0.70.9/py3.6/doc/programming-guidelines.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/proxy-objects.html` & `multiprocess-0.70.9/py3.6/doc/proxy-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/proxy-objects.txt` & `multiprocess-0.70.9/py3.6/doc/proxy-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/queue-objects.html` & `multiprocess-0.70.9/py3.6/doc/queue-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/queue-objects.txt` & `multiprocess-0.70.9/py3.6/doc/queue-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/sharedctypes.html` & `multiprocess-0.70.9/py3.6/doc/sharedctypes.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/sharedctypes.txt` & `multiprocess-0.70.9/py3.6/doc/sharedctypes.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/tests.html` & `multiprocess-0.70.9/py3.6/doc/tests.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/tests.txt` & `multiprocess-0.70.9/py3.6/doc/tests.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.6/doc/THANKS.html` & `multiprocess-0.70.9/py3.6/doc/THANKS.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/index.html` & `multiprocess-0.70.9/py3.5/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/README_MODS` & `multiprocess-0.70.9/py3.5/README_MODS`

 * *Files 1% similar despite different names*

```diff
@@ -373,8 +373,9 @@
 >             except Exception:
 >                 import traceback
 >                 traceback.print_exc()
 389c397
 <     passfds = sorted(passfds)
 ---
 >     passfds = tuple(sorted(map(int, passfds)))
-
+# ----------------------------------------------------------------------
+ADDED *args, **kwds for ForkingPickler in __init__, dump, and dumps
```

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/__init__.py` & `multiprocess-0.70.9/py3.5/multiprocess/__init__.py`

 * *Files 15% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 # Copyright (c) 2006-2008, R Oudkerk
 # Licensed to PSF under a Contributor Agreement.
 #
 
 import sys
 from . import context
 
-__version__ = '0.70.8'
+__version__ = '0.70.9'
 
 #
 # Copy stuff from default context
 #
 
 globals().update((name, getattr(context._default_context, name))
                  for name in context._default_context.__all__)
```

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/connection.py` & `multiprocess-0.70.9/py3.5/multiprocess/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/context.py` & `multiprocess-0.70.9/py3.5/multiprocess/context.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/forkserver.py` & `multiprocess-0.70.9/py3.5/multiprocess/forkserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/heap.py` & `multiprocess-0.70.9/py3.5/multiprocess/heap.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/managers.py` & `multiprocess-0.70.9/py3.5/multiprocess/managers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/pool.py` & `multiprocess-0.70.9/py3.5/multiprocess/pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/popen_fork.py` & `multiprocess-0.70.9/py3.5/multiprocess/popen_fork.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/popen_forkserver.py` & `multiprocess-0.70.9/py3.5/multiprocess/popen_forkserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/popen_spawn_posix.py` & `multiprocess-0.70.9/py3.5/multiprocess/popen_spawn_posix.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/popen_spawn_win32.py` & `multiprocess-0.70.9/py3.5/multiprocess/popen_spawn_win32.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/process.py` & `multiprocess-0.70.9/py3.5/multiprocess/process.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/queues.py` & `multiprocess-0.70.9/py3.5/multiprocess/queues.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/reduction.py` & `multiprocess-0.70.9/py3.5/multiprocess/reduction.py`

 * *Files 3% similar despite different names*

```diff
@@ -33,37 +33,37 @@
 #
 
 class ForkingPickler(pickle.Pickler):
     '''Pickler subclass used by multiprocessing.'''
     _extra_reducers = {}
     _copyreg_dispatch_table = copyreg.dispatch_table
 
-    def __init__(self, *args):
-        super().__init__(*args)
+    def __init__(self, *args, **kwds):
+        super().__init__(*args, **kwds)
         self.dispatch_table = self._copyreg_dispatch_table.copy()
         self.dispatch_table.update(self._extra_reducers)
 
     @classmethod
     def register(cls, type, reduce):
         '''Register a reduce function for a type.'''
         cls._extra_reducers[type] = reduce
 
     @classmethod
-    def dumps(cls, obj, protocol=None):
+    def dumps(cls, obj, protocol=None, *args, **kwds):
         buf = io.BytesIO()
-        cls(buf, protocol).dump(obj)
+        cls(buf, protocol, *args, **kwds).dump(obj)
         return buf.getbuffer()
 
     loads = pickle.loads
 
 register = ForkingPickler.register
 
-def dump(obj, file, protocol=None):
+def dump(obj, file, protocol=None, *args, **kwds):
     '''Replacement for pickle.dump() using ForkingPickler.'''
-    ForkingPickler(file, protocol).dump(obj)
+    ForkingPickler(file, protocol, *args, **kwds).dump(obj)
 
 #
 # Platform specific definitions
 #
 
 if sys.platform == 'win32':
     # Windows
```

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/resource_sharer.py` & `multiprocess-0.70.9/py3.5/multiprocess/resource_sharer.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/semaphore_tracker.py` & `multiprocess-0.70.9/py3.5/multiprocess/semaphore_tracker.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/sharedctypes.py` & `multiprocess-0.70.9/py3.5/multiprocess/sharedctypes.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/spawn.py` & `multiprocess-0.70.9/py3.5/multiprocess/spawn.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/synchronize.py` & `multiprocess-0.70.9/py3.5/multiprocess/synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/util.py` & `multiprocess-0.70.9/py3.8/multiprocess/util.py`

 * *Files 4% similar despite different names*

```diff
@@ -55,15 +55,15 @@
 
 def sub_warning(msg, *args):
     if _logger:
         _logger.log(SUBWARNING, msg, *args)
 
 def get_logger():
     '''
-    Returns logger used by multiprocessing
+    Returns logger used by multiprocess
     '''
     global _logger
     import logging
 
     logging._acquireLock()
     try:
         if not _logger:
@@ -102,22 +102,34 @@
     _log_to_stderr = True
     return _logger
 
 #
 # Function returning a temp directory which will be removed on exit
 #
 
+def _remove_temp_dir(rmtree, tempdir):
+    rmtree(tempdir)
+
+    current_process = process.current_process()
+    # current_process() can be None if the finalizer is called
+    # late during Python finalization
+    if current_process is not None:
+        current_process._config['tempdir'] = None
+
 def get_temp_dir():
     # get name of a temp directory which will be automatically cleaned up
     tempdir = process.current_process()._config.get('tempdir')
     if tempdir is None:
         import shutil, tempfile
         tempdir = tempfile.mkdtemp(prefix='pymp-')
         info('created temp directory %s', tempdir)
-        Finalize(None, shutil.rmtree, args=[tempdir], exitpriority=-100)
+        # keep a strong reference to shutil.rmtree(), since the finalizer
+        # can be called late during Python shutdown
+        Finalize(None, _remove_temp_dir, args=(shutil.rmtree, tempdir),
+                 exitpriority=-100)
         process.current_process()._config['tempdir'] = tempdir
     return tempdir
 
 #
 # Support for reinitialization of objects when bootstrapping a child process
 #
 
@@ -145,20 +157,23 @@
 
 
 class Finalize(object):
     '''
     Class which supports object finalization using weakrefs
     '''
     def __init__(self, obj, callback, args=(), kwargs=None, exitpriority=None):
-        assert exitpriority is None or type(exitpriority) is int
+        if (exitpriority is not None) and not isinstance(exitpriority,int):
+            raise TypeError(
+                "Exitpriority ({0!r}) must be None or int, not {1!s}".format(
+                    exitpriority, type(exitpriority)))
 
         if obj is not None:
             self._weakref = weakref.ref(obj, self)
-        else:
-            assert exitpriority is not None
+        elif exitpriority is None:
+            raise ValueError("Without object, exitpriority cannot be None")
 
         self._callback = callback
         self._args = args
         self._kwargs = kwargs or {}
         self._key = (exitpriority, next(_finalizer_counter))
         self._pid = os.getpid()
 
@@ -385,14 +400,28 @@
         except:
             os.close(fd)
             raise
     except (OSError, ValueError):
         pass
 
 #
+# Flush standard streams, if any
+#
+
+def _flush_std_streams():
+    try:
+        sys.stdout.flush()
+    except (AttributeError, ValueError):
+        pass
+    try:
+        sys.stderr.flush()
+    except (AttributeError, ValueError):
+        pass
+
+#
 # Start a program with only specified fds kept open
 #
 
 def spawnv_passfds(path, args, passfds):
     import _posixsubprocess
     passfds = tuple(sorted(map(int, passfds)))
     errpipe_read, errpipe_write = os.pipe()
@@ -400,7 +429,13 @@
         return _posixsubprocess.fork_exec(
             args, [os.fsencode(path)], True, passfds, None, None,
             -1, -1, -1, -1, -1, -1, errpipe_read, errpipe_write,
             False, False, None)
     finally:
         os.close(errpipe_read)
         os.close(errpipe_write)
+
+
+def close_fds(*fds):
+    """Close each file descriptor given as an argument"""
+    for fd in fds:
+        os.close(fd)
```

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/tests/__init__.py` & `multiprocess-0.70.9/py3.5/multiprocess/tests/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -19,15 +19,15 @@
 import struct
 import operator
 import test.support
 import test.support.script_helper
 
 
 # Skip tests if _multiprocessing wasn't built.
-_multiprocessing = test.support.import_module('_multiprocess')
+_multiprocessing = test.support.import_module('_multiprocessing')
 # Skip tests if sem_open implementation is broken.
 test.support.import_module('multiprocess.synchronize')
 # import threading after _multiprocessing to raise a more relevant error
 # message: "No module named _multiprocessing". _multiprocessing is not compiled
 # without thread support.
 import threading
```

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/tests/__main__.py` & `multiprocess-0.70.9/py3.5/multiprocess/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/tests/test_multiprocessing_main_handling.py` & `multiprocess-0.70.9/py3.5/multiprocess/tests/test_multiprocessing_main_handling.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # tests __main__ module handling in multiprocessing
 from test import support
 # Skip tests if _thread or _multiprocessing wasn't built.
 support.import_module('_thread')
-support.import_module('_multiprocess')
+support.import_module('_multiprocessing')
 
 import importlib
 import importlib.machinery
 import zipimport
 import unittest
 import sys
 import os
```

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/dummy/__init__.py` & `multiprocess-0.70.9/py3.5/multiprocess/dummy/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/multiprocess/dummy/connection.py` & `multiprocess-0.70.9/py3.5/multiprocess/dummy/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/Modules/_multiprocess/multiprocess.c` & `multiprocess-0.70.9/py3.5/Modules/_multiprocess/multiprocess.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/Modules/_multiprocess/multiprocess.h` & `multiprocess-0.70.9/py3.5/Modules/_multiprocess/multiprocess.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/Modules/_multiprocess/semaphore.c` & `multiprocess-0.70.9/py3.5/Modules/_multiprocess/semaphore.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/examples/benchmarks.py` & `multiprocess-0.70.9/py3.5/examples/benchmarks.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 #
 # Simple benchmarks for the processing package
 #
 
 import time, sys, multiprocess as processing, threading, queue as Queue, gc
 processing.freezeSupport = processing.freeze_support
-xrange = range
 
 if sys.platform == 'win32':
     _timer = time.clock
 else:
     _timer = time.time
 
 delta = 1
@@ -18,17 +17,17 @@
 
 def queuespeed_func(q, c, iterations):
     a = '0' * 256
     c.acquire()
     c.notify()
     c.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         q.put(a)
-#    q.putMany((a for i in xrange(iterations))
+#    q.putMany((a for i in range(iterations))
 
     q.put('STOP')
 
 def test_queuespeed(Process, q, c):
     elapsed = 0
     iterations = 1
 
@@ -59,15 +58,15 @@
 
 def pipe_func(c, cond, iterations):
     a = '0' * 256
     cond.acquire()
     cond.notify()
     cond.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         c.send(a)
 
     c.send('STOP')
 
 def test_pipespeed():
     c, d = processing.Pipe()
     cond = processing.Condition()
@@ -103,15 +102,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             a = seq[5]
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
 
@@ -123,15 +122,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             l.acquire()
             l.release()
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
@@ -139,15 +138,15 @@
 
 #### TEST_CONDITION
 
 def conditionspeed_func(c, N):
     c.acquire()
     c.notify()
 
-    for i in xrange(N):
+    for i in range(N):
         c.wait()
         c.notify()
 
     c.release()
 
 def test_conditionspeed(Process, c):
     elapsed = 0
@@ -160,15 +159,15 @@
         p = Process(target=conditionspeed_func, args=(c, iterations))
         p.start()
 
         c.wait()
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             c.notify()
             c.wait()
 
         elapsed = _timer()-t
 
         c.release()
         p.join()
```

### Comparing `multiprocess-0.70.8/py3.5/examples/ex_newtype.py` & `multiprocess-0.70.9/py3.7/examples/ex_newtype.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,37 +1,36 @@
 #
 # This module shows how to use arbitrary callables with a subclass of
 # `BaseManager`.
 #
 
 from multiprocess import freeze_support as freezeSupport
-from multiprocess.managers import BaseManager, BaseProxy
-xrange = range
+from multiprocess.managers import BaseManager, IteratorProxy as BaseProxy
 
 ##
 
 class Foo(object):
     def f(self):
         print('you called Foo.f()')
     def g(self):
         print('you called Foo.g()')
     def _h(self):
         print('you called Foo._h()')
 
 # A simple generator function
 def baz():
-    for i in xrange(10):
+    for i in range(10):
         yield i*i
 
 # Proxy type for generator objects
 class GeneratorProxy(BaseProxy):
     def __iter__(self):
         return self
-    def next(self):
-        return self._callmethod('next')
+    def __next__(self):
+        return self._callmethod('__next__')
 
 ##
 
 class MyManager(BaseManager): pass
 
 # register the Foo class; make all public methods accessible via proxy
 MyManager.register('Foo1', Foo)
```

### Comparing `multiprocess-0.70.8/py3.5/examples/ex_pool.py` & `multiprocess-0.70.9/py3.5/examples/ex_pool.py`

 * *Files 6% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 # A test of `processing.Pool` class
 #
 
 from multiprocess import Pool, TimeoutError
 from multiprocess import cpu_count as cpuCount, current_process as currentProcess, freeze_support as freezeSupport, active_children as activeChildren
 
 import time, random, sys
-xrange = range
 
 #
 # Functions used by test code
 #
 
 def calculate(func, args):
     result = func(*args)
@@ -87,26 +86,26 @@
     # Simple benchmarks
     #
 
     N = 100000
     print('def pow3(x): return x**3')
     
     t = time.time()
-    A = list(map(pow3, xrange(N)))
-    print('\tmap(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    A = list(map(pow3, range(N)))
+    print('\tmap(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
     
     t = time.time()
-    B = pool.map(pow3, xrange(N))
-    print('\tpool.map(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    B = pool.map(pow3, range(N))
+    print('\tpool.map(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
 
     t = time.time()
-    C = list(pool.imap(pow3, xrange(N), chunksize=N//8))
-    print('\tlist(pool.imap(pow3, xrange(%d), chunksize=%d)):\n\t\t%s' \
+    C = list(pool.imap(pow3, range(N), chunksize=N//8))
+    print('\tlist(pool.imap(pow3, range(%d), chunksize=%d)):\n\t\t%s' \
           ' seconds' % (N, N//8, time.time() - t))
     
     assert A == B == C, (len(A), len(B), len(C))
     print()
     
     L = [None] * 1000000
     print('def noop(x): pass')
```

### Comparing `multiprocess-0.70.8/py3.5/examples/ex_synchronize.py` & `multiprocess-0.70.9/py3.5/examples/ex_synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/examples/ex_webserver.py` & `multiprocess-0.70.9/py3.5/examples/ex_webserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/examples/ex_workers.py` & `multiprocess-0.70.9/py3.5/examples/ex_workers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/CHANGES.html` & `multiprocess-0.70.9/py3.5/doc/CHANGES.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/connection-objects.html` & `multiprocess-0.70.9/py3.5/doc/connection-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/connection-objects.txt` & `multiprocess-0.70.9/py3.5/doc/connection-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/connection-ref.html` & `multiprocess-0.70.9/py3.5/doc/connection-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/connection-ref.txt` & `multiprocess-0.70.9/py3.5/doc/connection-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/COPYING.html` & `multiprocess-0.70.9/py3.5/doc/COPYING.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/html4css1.css` & `multiprocess-0.70.9/py3.5/doc/html4css1.css`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/index.html` & `multiprocess-0.70.9/py3.5/doc/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/index.txt` & `multiprocess-0.70.9/py3.5/doc/index.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/INSTALL.html` & `multiprocess-0.70.9/py3.5/doc/INSTALL.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/intro.html` & `multiprocess-0.70.9/py3.5/doc/intro.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/intro.txt` & `multiprocess-0.70.9/py3.5/doc/intro.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/manager-objects.html` & `multiprocess-0.70.9/py3.5/doc/manager-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/manager-objects.txt` & `multiprocess-0.70.9/py3.5/doc/manager-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/pool-objects.html` & `multiprocess-0.70.9/py3.5/doc/pool-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/pool-objects.txt` & `multiprocess-0.70.9/py3.5/doc/pool-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/process-objects.html` & `multiprocess-0.70.9/py3.5/doc/process-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/process-objects.txt` & `multiprocess-0.70.9/py3.5/doc/process-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/processing-ref.html` & `multiprocess-0.70.9/py3.5/doc/processing-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/processing-ref.txt` & `multiprocess-0.70.9/py3.5/doc/processing-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/programming-guidelines.html` & `multiprocess-0.70.9/py3.5/doc/programming-guidelines.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/programming-guidelines.txt` & `multiprocess-0.70.9/py3.5/doc/programming-guidelines.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/proxy-objects.html` & `multiprocess-0.70.9/py3.5/doc/proxy-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/proxy-objects.txt` & `multiprocess-0.70.9/py3.5/doc/proxy-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/queue-objects.html` & `multiprocess-0.70.9/py3.5/doc/queue-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/queue-objects.txt` & `multiprocess-0.70.9/py3.5/doc/queue-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/sharedctypes.html` & `multiprocess-0.70.9/py3.5/doc/sharedctypes.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/sharedctypes.txt` & `multiprocess-0.70.9/py3.5/doc/sharedctypes.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/tests.html` & `multiprocess-0.70.9/py3.5/doc/tests.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/tests.txt` & `multiprocess-0.70.9/py3.5/doc/tests.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.5/doc/THANKS.html` & `multiprocess-0.70.9/py3.5/doc/THANKS.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/index.html` & `multiprocess-0.70.9/py3.4/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/README_MODS` & `multiprocess-0.70.9/py3.4/README_MODS`

 * *Files 2% similar despite different names*

```diff
@@ -147,8 +147,9 @@
 <             if close:
 <                 self._close = None
 <                 close()
 ---
 >         self._reader.close()
 >         if self._close:
 >             self._close()
-
+# ----------------------------------------------------------------------
+ADDED *args, **kwds for ForkingPickler in __init__, dump, and dumps
```

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/__init__.py` & `multiprocess-0.70.9/py3.4/multiprocess/__init__.py`

 * *Files 15% similar despite different names*

```diff
@@ -11,15 +11,15 @@
 # Copyright (c) 2006-2008, R Oudkerk
 # Licensed to PSF under a Contributor Agreement.
 #
 
 import sys
 from . import context
 
-__version__ = '0.70.8'
+__version__ = '0.70.9'
 
 #
 # Copy stuff from default context
 #
 
 globals().update((name, getattr(context._default_context, name))
                  for name in context._default_context.__all__)
```

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/connection.py` & `multiprocess-0.70.9/py3.4/multiprocess/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/context.py` & `multiprocess-0.70.9/py3.4/multiprocess/context.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/forkserver.py` & `multiprocess-0.70.9/py3.4/multiprocess/forkserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/heap.py` & `multiprocess-0.70.9/py3.4/multiprocess/heap.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/managers.py` & `multiprocess-0.70.9/py3.4/multiprocess/managers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/pool.py` & `multiprocess-0.70.9/py3.4/multiprocess/pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/popen_fork.py` & `multiprocess-0.70.9/py3.4/multiprocess/popen_fork.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/popen_forkserver.py` & `multiprocess-0.70.9/py3.4/multiprocess/popen_forkserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/popen_spawn_posix.py` & `multiprocess-0.70.9/py3.4/multiprocess/popen_spawn_posix.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/popen_spawn_win32.py` & `multiprocess-0.70.9/py3.4/multiprocess/popen_spawn_win32.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/process.py` & `multiprocess-0.70.9/py3.4/multiprocess/process.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/queues.py` & `multiprocess-0.70.9/py3.4/multiprocess/queues.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/reduction.py` & `multiprocess-0.70.9/py3.4/multiprocess/reduction.py`

 * *Files 3% similar despite different names*

```diff
@@ -33,37 +33,37 @@
 #
 
 class ForkingPickler(pickle.Pickler):
     '''Pickler subclass used by multiprocessing.'''
     _extra_reducers = {}
     _copyreg_dispatch_table = copyreg.dispatch_table
 
-    def __init__(self, *args):
-        super().__init__(*args)
+    def __init__(self, *args, **kwds):
+        super().__init__(*args, **kwds)
         self.dispatch_table = self._copyreg_dispatch_table.copy()
         self.dispatch_table.update(self._extra_reducers)
 
     @classmethod
     def register(cls, type, reduce):
         '''Register a reduce function for a type.'''
         cls._extra_reducers[type] = reduce
 
     @classmethod
-    def dumps(cls, obj, protocol=None):
+    def dumps(cls, obj, protocol=None, *args, **kwds):
         buf = io.BytesIO()
-        cls(buf, protocol).dump(obj)
+        cls(buf, protocol, *args, **kwds).dump(obj)
         return buf.getbuffer()
 
     loads = pickle.loads
 
 register = ForkingPickler.register
 
-def dump(obj, file, protocol=None):
+def dump(obj, file, protocol=None, *args, **kwds):
     '''Replacement for pickle.dump() using ForkingPickler.'''
-    ForkingPickler(file, protocol).dump(obj)
+    ForkingPickler(file, protocol, *args, **kwds).dump(obj)
 
 #
 # Platform specific definitions
 #
 
 if sys.platform == 'win32':
     # Windows
```

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/resource_sharer.py` & `multiprocess-0.70.9/py3.4/multiprocess/resource_sharer.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/semaphore_tracker.py` & `multiprocess-0.70.9/py3.4/multiprocess/semaphore_tracker.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/sharedctypes.py` & `multiprocess-0.70.9/py3.4/multiprocess/sharedctypes.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/spawn.py` & `multiprocess-0.70.9/py3.4/multiprocess/spawn.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/synchronize.py` & `multiprocess-0.70.9/py3.4/multiprocess/synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/util.py` & `multiprocess-0.70.9/py3.4/multiprocess/util.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/tests/__init__.py` & `multiprocess-0.70.9/py3.4/multiprocess/tests/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -19,15 +19,15 @@
 import struct
 import operator
 import test.support
 import test.script_helper
 
 
 # Skip tests if _multiprocessing wasn't built.
-_multiprocessing = test.support.import_module('_multiprocess')
+_multiprocessing = test.support.import_module('_multiprocessing')
 # Skip tests if sem_open implementation is broken.
 test.support.import_module('multiprocess.synchronize')
 # import threading after _multiprocessing to raise a more revelant error
 # message: "No module named _multiprocessing". _multiprocessing is not compiled
 # without thread support.
 import threading
```

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/tests/__main__.py` & `multiprocess-0.70.9/py3.4/multiprocess/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/tests/test_multiprocessing_main_handling.py` & `multiprocess-0.70.9/py3.4/multiprocess/tests/test_multiprocessing_main_handling.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # tests __main__ module handling in multiprocessing
 from test import support
 # Skip tests if _thread or _multiprocessing wasn't built.
 support.import_module('_thread')
-support.import_module('_multiprocess')
+support.import_module('_multiprocessing')
 
 import importlib
 import importlib.machinery
 import zipimport
 import unittest
 import sys
 import os
```

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/dummy/__init__.py` & `multiprocess-0.70.9/py3.4/multiprocess/dummy/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/multiprocess/dummy/connection.py` & `multiprocess-0.70.9/py3.4/multiprocess/dummy/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/Modules/_multiprocess/multiprocess.c` & `multiprocess-0.70.9/py3.4/Modules/_multiprocess/multiprocess.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/Modules/_multiprocess/multiprocess.h` & `multiprocess-0.70.9/py3.4/Modules/_multiprocess/multiprocess.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/Modules/_multiprocess/semaphore.c` & `multiprocess-0.70.9/py3.4/Modules/_multiprocess/semaphore.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/examples/benchmarks.py` & `multiprocess-0.70.9/py3.4/examples/benchmarks.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 #
 # Simple benchmarks for the processing package
 #
 
 import time, sys, multiprocess as processing, threading, queue as Queue, gc
 processing.freezeSupport = processing.freeze_support
-xrange = range
 
 if sys.platform == 'win32':
     _timer = time.clock
 else:
     _timer = time.time
 
 delta = 1
@@ -18,17 +17,17 @@
 
 def queuespeed_func(q, c, iterations):
     a = '0' * 256
     c.acquire()
     c.notify()
     c.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         q.put(a)
-#    q.putMany((a for i in xrange(iterations))
+#    q.putMany((a for i in range(iterations))
 
     q.put('STOP')
 
 def test_queuespeed(Process, q, c):
     elapsed = 0
     iterations = 1
 
@@ -59,15 +58,15 @@
 
 def pipe_func(c, cond, iterations):
     a = '0' * 256
     cond.acquire()
     cond.notify()
     cond.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         c.send(a)
 
     c.send('STOP')
 
 def test_pipespeed():
     c, d = processing.Pipe()
     cond = processing.Condition()
@@ -103,15 +102,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             a = seq[5]
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
 
@@ -123,15 +122,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             l.acquire()
             l.release()
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
@@ -139,15 +138,15 @@
 
 #### TEST_CONDITION
 
 def conditionspeed_func(c, N):
     c.acquire()
     c.notify()
 
-    for i in xrange(N):
+    for i in range(N):
         c.wait()
         c.notify()
 
     c.release()
 
 def test_conditionspeed(Process, c):
     elapsed = 0
@@ -160,15 +159,15 @@
         p = Process(target=conditionspeed_func, args=(c, iterations))
         p.start()
 
         c.wait()
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             c.notify()
             c.wait()
 
         elapsed = _timer()-t
 
         c.release()
         p.join()
```

### Comparing `multiprocess-0.70.8/py3.4/examples/ex_newtype.py` & `multiprocess-0.70.9/py3.6/examples/ex_newtype.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,37 +1,36 @@
 #
 # This module shows how to use arbitrary callables with a subclass of
 # `BaseManager`.
 #
 
 from multiprocess import freeze_support as freezeSupport
-from multiprocess.managers import BaseManager, BaseProxy
-xrange = range
+from multiprocess.managers import BaseManager, IteratorProxy as BaseProxy
 
 ##
 
 class Foo(object):
     def f(self):
         print('you called Foo.f()')
     def g(self):
         print('you called Foo.g()')
     def _h(self):
         print('you called Foo._h()')
 
 # A simple generator function
 def baz():
-    for i in xrange(10):
+    for i in range(10):
         yield i*i
 
 # Proxy type for generator objects
 class GeneratorProxy(BaseProxy):
     def __iter__(self):
         return self
-    def next(self):
-        return self._callmethod('next')
+    def __next__(self):
+        return self._callmethod('__next__')
 
 ##
 
 class MyManager(BaseManager): pass
 
 # register the Foo class; make all public methods accessible via proxy
 MyManager.register('Foo1', Foo)
```

### Comparing `multiprocess-0.70.8/py3.4/examples/ex_pool.py` & `multiprocess-0.70.9/py3.4/examples/ex_pool.py`

 * *Files 6% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 # A test of `processing.Pool` class
 #
 
 from multiprocess import Pool, TimeoutError
 from multiprocess import cpu_count as cpuCount, current_process as currentProcess, freeze_support as freezeSupport, active_children as activeChildren
 
 import time, random, sys
-xrange = range
 
 #
 # Functions used by test code
 #
 
 def calculate(func, args):
     result = func(*args)
@@ -87,26 +86,26 @@
     # Simple benchmarks
     #
 
     N = 100000
     print('def pow3(x): return x**3')
     
     t = time.time()
-    A = list(map(pow3, xrange(N)))
-    print('\tmap(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    A = list(map(pow3, range(N)))
+    print('\tmap(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
     
     t = time.time()
-    B = pool.map(pow3, xrange(N))
-    print('\tpool.map(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    B = pool.map(pow3, range(N))
+    print('\tpool.map(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
 
     t = time.time()
-    C = list(pool.imap(pow3, xrange(N), chunksize=N//8))
-    print('\tlist(pool.imap(pow3, xrange(%d), chunksize=%d)):\n\t\t%s' \
+    C = list(pool.imap(pow3, range(N), chunksize=N//8))
+    print('\tlist(pool.imap(pow3, range(%d), chunksize=%d)):\n\t\t%s' \
           ' seconds' % (N, N//8, time.time() - t))
     
     assert A == B == C, (len(A), len(B), len(C))
     print()
     
     L = [None] * 1000000
     print('def noop(x): pass')
```

### Comparing `multiprocess-0.70.8/py3.4/examples/ex_synchronize.py` & `multiprocess-0.70.9/py3.4/examples/ex_synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/examples/ex_webserver.py` & `multiprocess-0.70.9/py3.4/examples/ex_webserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/examples/ex_workers.py` & `multiprocess-0.70.9/py3.4/examples/ex_workers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/CHANGES.html` & `multiprocess-0.70.9/py3.4/doc/CHANGES.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/connection-objects.html` & `multiprocess-0.70.9/py3.4/doc/connection-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/connection-objects.txt` & `multiprocess-0.70.9/py3.4/doc/connection-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/connection-ref.html` & `multiprocess-0.70.9/py3.4/doc/connection-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/connection-ref.txt` & `multiprocess-0.70.9/py3.4/doc/connection-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/COPYING.html` & `multiprocess-0.70.9/py3.4/doc/COPYING.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/html4css1.css` & `multiprocess-0.70.9/py3.4/doc/html4css1.css`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/index.html` & `multiprocess-0.70.9/py3.4/doc/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/index.txt` & `multiprocess-0.70.9/py3.4/doc/index.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/INSTALL.html` & `multiprocess-0.70.9/py3.4/doc/INSTALL.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/intro.html` & `multiprocess-0.70.9/py3.4/doc/intro.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/intro.txt` & `multiprocess-0.70.9/py3.4/doc/intro.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/manager-objects.html` & `multiprocess-0.70.9/py3.4/doc/manager-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/manager-objects.txt` & `multiprocess-0.70.9/py3.4/doc/manager-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/pool-objects.html` & `multiprocess-0.70.9/py3.4/doc/pool-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/pool-objects.txt` & `multiprocess-0.70.9/py3.4/doc/pool-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/process-objects.html` & `multiprocess-0.70.9/py3.4/doc/process-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/process-objects.txt` & `multiprocess-0.70.9/py3.4/doc/process-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/processing-ref.html` & `multiprocess-0.70.9/py3.4/doc/processing-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/processing-ref.txt` & `multiprocess-0.70.9/py3.4/doc/processing-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/programming-guidelines.html` & `multiprocess-0.70.9/py3.4/doc/programming-guidelines.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/programming-guidelines.txt` & `multiprocess-0.70.9/py3.4/doc/programming-guidelines.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/proxy-objects.html` & `multiprocess-0.70.9/py3.4/doc/proxy-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/proxy-objects.txt` & `multiprocess-0.70.9/py3.4/doc/proxy-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/queue-objects.html` & `multiprocess-0.70.9/py3.4/doc/queue-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/queue-objects.txt` & `multiprocess-0.70.9/py3.4/doc/queue-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/sharedctypes.html` & `multiprocess-0.70.9/py3.4/doc/sharedctypes.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/sharedctypes.txt` & `multiprocess-0.70.9/py3.4/doc/sharedctypes.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/tests.html` & `multiprocess-0.70.9/py3.4/doc/tests.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/tests.txt` & `multiprocess-0.70.9/py3.4/doc/tests.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.4/doc/THANKS.html` & `multiprocess-0.70.9/py3.4/doc/THANKS.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/index.html` & `multiprocess-0.70.9/py3.3/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/README_MODS` & `multiprocess-0.70.9/py3.3/README_MODS`

 * *Files 4% similar despite different names*

```diff
@@ -86,7 +86,8 @@
 >     def test_noforkbomb(self):
 
 # ----------------------------------------------------------------------
 REPLACED "from multiprocessing" with "from multiprocess"
 REPLACED "from _multiprocessing" with "from _multiprocess"
 REPLACED "import _multiprocessing" with "import _multiprocess as _multiprocessing"
 REPLACED "multprocessing" with "multiprocess" wherever else relevant...
+ADDED *args, **kwds for ForkingPickler in __init__ and dump
```

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/__init__.py` & `multiprocess-0.70.9/py3.3/multiprocess/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -12,15 +12,15 @@
 # documentation in a webbrowser.
 #
 #
 # Copyright (c) 2006-2008, R Oudkerk
 # Licensed to PSF under a Contributor Agreement.
 #
 
-__version__ = '0.70.8'
+__version__ = '0.70.9'
 
 __all__ = [
     'Process', 'current_process', 'active_children', 'freeze_support',
     'Manager', 'Pipe', 'cpu_count', 'log_to_stderr', 'get_logger',
     'allow_connection_pickling', 'BufferTooShort', 'TimeoutError',
     'Lock', 'RLock', 'Semaphore', 'BoundedSemaphore', 'Condition',
     'Event', 'Barrier', 'Queue', 'SimpleQueue', 'JoinableQueue', 'Pool',
```

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/connection.py` & `multiprocess-0.70.9/py3.3/multiprocess/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/forking.py` & `multiprocess-0.70.9/py3.3/multiprocess/forking.py`

 * *Files 1% similar despite different names*

```diff
@@ -35,16 +35,16 @@
     from dill import Pickler
 except ImportError:
     from pickle import Pickler
 from copyreg import dispatch_table
 
 class ForkingPickler(Pickler):
     _extra_reducers = {}
-    def __init__(self, *args):
-        Pickler.__init__(self, *args)
+    def __init__(self, *args, **kwds):
+        Pickler.__init__(self, *args, **kwds)
         self.dispatch_table = dispatch_table.copy()
         self.dispatch_table.update(self._extra_reducers)
     @classmethod
     def register(cls, type, reduce):
         cls._extra_reducers[type] = reduce
 
 def _reduce_method(m):
@@ -164,16 +164,16 @@
     import _winapi
 
     try:
         from dill import load, DEFAULT_PROTOCOL as HIGHEST_PROTOCOL
     except ImportError:
         from pickle import load, HIGHEST_PROTOCOL
 
-    def dump(obj, file, protocol=None):
-        ForkingPickler(file, protocol).dump(obj)
+    def dump(obj, file, protocol=None, *args, **kwds):
+        ForkingPickler(file, protocol, *args, **kwds).dump(obj)
 
     #
     #
     #
 
     TERMINATE = 0x10000
     WINEXE = (sys.platform == 'win32' and getattr(sys, 'frozen', False))
```

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/heap.py` & `multiprocess-0.70.9/py3.3/multiprocess/heap.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/managers.py` & `multiprocess-0.70.9/py3.3/multiprocess/managers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/pool.py` & `multiprocess-0.70.9/py3.3/multiprocess/pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/process.py` & `multiprocess-0.70.9/py3.3/multiprocess/process.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/queues.py` & `multiprocess-0.70.9/py3.3/multiprocess/queues.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/reduction.py` & `multiprocess-0.70.9/py3.3/multiprocess/reduction.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/sharedctypes.py` & `multiprocess-0.70.9/py3.3/multiprocess/sharedctypes.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/synchronize.py` & `multiprocess-0.70.9/py3.3/multiprocess/synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/util.py` & `multiprocess-0.70.9/py3.3/multiprocess/util.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/tests/__init__.py` & `multiprocess-0.70.9/py3.3/multiprocess/tests/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -19,15 +19,15 @@
 import struct
 import operator
 import test.support
 import test.script_helper
 
 
 # Skip tests if _multiprocessing wasn't built.
-_multiprocessing = test.support.import_module('_multiprocess')
+_multiprocessing = test.support.import_module('_multiprocessing')
 # Skip tests if sem_open implementation is broken.
 test.support.import_module('multiprocess.synchronize')
 # import threading after _multiprocessing to raise a more revelant error
 # message: "No module named _multiprocessing". _multiprocessing is not compiled
 # without thread support.
 import threading
```

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/tests/__main__.py` & `multiprocess-0.70.9/py3.3/multiprocess/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/dummy/__init__.py` & `multiprocess-0.70.9/py3.3/multiprocess/dummy/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/multiprocess/dummy/connection.py` & `multiprocess-0.70.9/py3.3/multiprocess/dummy/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/Modules/_multiprocess/multiprocess.c` & `multiprocess-0.70.9/py3.3/Modules/_multiprocess/multiprocess.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/Modules/_multiprocess/multiprocess.h` & `multiprocess-0.70.9/py3.3/Modules/_multiprocess/multiprocess.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/Modules/_multiprocess/semaphore.c` & `multiprocess-0.70.9/py3.3/Modules/_multiprocess/semaphore.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/examples/benchmarks.py` & `multiprocess-0.70.9/py3.3/examples/benchmarks.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 #
 # Simple benchmarks for the processing package
 #
 
 import time, sys, multiprocess as processing, threading, queue as Queue, gc
 processing.freezeSupport = processing.freeze_support
-xrange = range
 
 if sys.platform == 'win32':
     _timer = time.clock
 else:
     _timer = time.time
 
 delta = 1
@@ -18,17 +17,17 @@
 
 def queuespeed_func(q, c, iterations):
     a = '0' * 256
     c.acquire()
     c.notify()
     c.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         q.put(a)
-#    q.putMany((a for i in xrange(iterations))
+#    q.putMany((a for i in range(iterations))
 
     q.put('STOP')
 
 def test_queuespeed(Process, q, c):
     elapsed = 0
     iterations = 1
 
@@ -59,15 +58,15 @@
 
 def pipe_func(c, cond, iterations):
     a = '0' * 256
     cond.acquire()
     cond.notify()
     cond.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         c.send(a)
 
     c.send('STOP')
 
 def test_pipespeed():
     c, d = processing.Pipe()
     cond = processing.Condition()
@@ -103,15 +102,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             a = seq[5]
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
 
@@ -123,15 +122,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             l.acquire()
             l.release()
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
@@ -139,15 +138,15 @@
 
 #### TEST_CONDITION
 
 def conditionspeed_func(c, N):
     c.acquire()
     c.notify()
 
-    for i in xrange(N):
+    for i in range(N):
         c.wait()
         c.notify()
 
     c.release()
 
 def test_conditionspeed(Process, c):
     elapsed = 0
@@ -160,15 +159,15 @@
         p = Process(target=conditionspeed_func, args=(c, iterations))
         p.start()
 
         c.wait()
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             c.notify()
             c.wait()
 
         elapsed = _timer()-t
 
         c.release()
         p.join()
```

### Comparing `multiprocess-0.70.8/py3.3/examples/ex_newtype.py` & `multiprocess-0.70.9/py3.5/examples/ex_newtype.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,37 +1,36 @@
 #
 # This module shows how to use arbitrary callables with a subclass of
 # `BaseManager`.
 #
 
 from multiprocess import freeze_support as freezeSupport
-from multiprocess.managers import BaseManager, BaseProxy
-xrange = range
+from multiprocess.managers import BaseManager, IteratorProxy as BaseProxy
 
 ##
 
 class Foo(object):
     def f(self):
         print('you called Foo.f()')
     def g(self):
         print('you called Foo.g()')
     def _h(self):
         print('you called Foo._h()')
 
 # A simple generator function
 def baz():
-    for i in xrange(10):
+    for i in range(10):
         yield i*i
 
 # Proxy type for generator objects
 class GeneratorProxy(BaseProxy):
     def __iter__(self):
         return self
-    def next(self):
-        return self._callmethod('next')
+    def __next__(self):
+        return self._callmethod('__next__')
 
 ##
 
 class MyManager(BaseManager): pass
 
 # register the Foo class; make all public methods accessible via proxy
 MyManager.register('Foo1', Foo)
```

### Comparing `multiprocess-0.70.8/py3.3/examples/ex_pool.py` & `multiprocess-0.70.9/py3.3/examples/ex_pool.py`

 * *Files 6% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 # A test of `processing.Pool` class
 #
 
 from multiprocess import Pool, TimeoutError
 from multiprocess import cpu_count as cpuCount, current_process as currentProcess, freeze_support as freezeSupport, active_children as activeChildren
 
 import time, random, sys
-xrange = range
 
 #
 # Functions used by test code
 #
 
 def calculate(func, args):
     result = func(*args)
@@ -87,26 +86,26 @@
     # Simple benchmarks
     #
 
     N = 100000
     print('def pow3(x): return x**3')
     
     t = time.time()
-    A = list(map(pow3, xrange(N)))
-    print('\tmap(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    A = list(map(pow3, range(N)))
+    print('\tmap(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
     
     t = time.time()
-    B = pool.map(pow3, xrange(N))
-    print('\tpool.map(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    B = pool.map(pow3, range(N))
+    print('\tpool.map(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
 
     t = time.time()
-    C = list(pool.imap(pow3, xrange(N), chunksize=N//8))
-    print('\tlist(pool.imap(pow3, xrange(%d), chunksize=%d)):\n\t\t%s' \
+    C = list(pool.imap(pow3, range(N), chunksize=N//8))
+    print('\tlist(pool.imap(pow3, range(%d), chunksize=%d)):\n\t\t%s' \
           ' seconds' % (N, N//8, time.time() - t))
     
     assert A == B == C, (len(A), len(B), len(C))
     print()
     
     L = [None] * 1000000
     print('def noop(x): pass')
```

### Comparing `multiprocess-0.70.8/py3.3/examples/ex_synchronize.py` & `multiprocess-0.70.9/py3.3/examples/ex_synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/examples/ex_webserver.py` & `multiprocess-0.70.9/py3.3/examples/ex_webserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/examples/ex_workers.py` & `multiprocess-0.70.9/py3.3/examples/ex_workers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/CHANGES.html` & `multiprocess-0.70.9/py3.3/doc/CHANGES.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/connection-objects.html` & `multiprocess-0.70.9/py3.3/doc/connection-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/connection-objects.txt` & `multiprocess-0.70.9/py3.3/doc/connection-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/connection-ref.html` & `multiprocess-0.70.9/py3.3/doc/connection-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/connection-ref.txt` & `multiprocess-0.70.9/py3.3/doc/connection-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/COPYING.html` & `multiprocess-0.70.9/py3.3/doc/COPYING.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/html4css1.css` & `multiprocess-0.70.9/py3.3/doc/html4css1.css`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/index.html` & `multiprocess-0.70.9/py3.3/doc/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/index.txt` & `multiprocess-0.70.9/py3.3/doc/index.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/INSTALL.html` & `multiprocess-0.70.9/py3.3/doc/INSTALL.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/intro.html` & `multiprocess-0.70.9/py3.3/doc/intro.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/intro.txt` & `multiprocess-0.70.9/py3.3/doc/intro.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/manager-objects.html` & `multiprocess-0.70.9/py3.3/doc/manager-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/manager-objects.txt` & `multiprocess-0.70.9/py3.3/doc/manager-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/pool-objects.html` & `multiprocess-0.70.9/py3.3/doc/pool-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/pool-objects.txt` & `multiprocess-0.70.9/py3.3/doc/pool-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/process-objects.html` & `multiprocess-0.70.9/py3.3/doc/process-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/process-objects.txt` & `multiprocess-0.70.9/py3.3/doc/process-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/processing-ref.html` & `multiprocess-0.70.9/py3.3/doc/processing-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/processing-ref.txt` & `multiprocess-0.70.9/py3.3/doc/processing-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/programming-guidelines.html` & `multiprocess-0.70.9/py3.3/doc/programming-guidelines.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/programming-guidelines.txt` & `multiprocess-0.70.9/py3.3/doc/programming-guidelines.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/proxy-objects.html` & `multiprocess-0.70.9/py3.3/doc/proxy-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/proxy-objects.txt` & `multiprocess-0.70.9/py3.3/doc/proxy-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/queue-objects.html` & `multiprocess-0.70.9/py3.3/doc/queue-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/queue-objects.txt` & `multiprocess-0.70.9/py3.3/doc/queue-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/sharedctypes.html` & `multiprocess-0.70.9/py3.3/doc/sharedctypes.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/sharedctypes.txt` & `multiprocess-0.70.9/py3.3/doc/sharedctypes.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/tests.html` & `multiprocess-0.70.9/py3.3/doc/tests.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/tests.txt` & `multiprocess-0.70.9/py3.3/doc/tests.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.3/doc/THANKS.html` & `multiprocess-0.70.9/py3.3/doc/THANKS.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/index.html` & `multiprocess-0.70.9/py3.2/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/README_MODS` & `multiprocess-0.70.9/py3.2/README_MODS`

 * *Files 4% similar despite different names*

```diff
@@ -79,7 +79,8 @@
 >     def test_noforkbomb(self):
 
 # ----------------------------------------------------------------------
 REPLACED "from multiprocessing" with "from multiprocess"
 REPLACED "from _multiprocessing" with "from _multiprocess"
 REPLACED "import _multiprocessing" with "import _multiprocess as _multiprocessing"
 REPLACED "multprocessing" with "multiprocess" wherever else relevant...
+ADDED *args, **kwds for ForkingPickler in __init__ and dump
```

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/__init__.py` & `multiprocess-0.70.9/py3.2/multiprocess/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -37,15 +37,15 @@
 # OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
 # HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
 # LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
 # OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
 # SUCH DAMAGE.
 #
 
-__version__ = '0.70.8'
+__version__ = '0.70.9'
 
 __all__ = [
     'Process', 'current_process', 'active_children', 'freeze_support',
     'Manager', 'Pipe', 'cpu_count', 'log_to_stderr', 'get_logger',
     'allow_connection_pickling', 'BufferTooShort', 'TimeoutError',
     'Lock', 'RLock', 'Semaphore', 'BoundedSemaphore', 'Condition',
     'Event', 'Queue', 'JoinableQueue', 'Pool', 'Value', 'Array',
```

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/connection.py` & `multiprocess-0.70.9/py3.2/multiprocess/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/forking.py` & `multiprocess-0.70.9/py3.2/multiprocess/forking.py`

 * *Files 2% similar despite different names*

```diff
@@ -58,14 +58,18 @@
 
 try:
     from dill import Pickler
 except ImportError:
     from pickle import _Pickler as Pickler
 class ForkingPickler(Pickler):
     dispatch = Pickler.dispatch.copy()
+
+    def __init__(self, *args, **kwds):
+        Pickler.__init__(self, *args, **kwds)
+
     @classmethod
     def register(cls, type, reduce):
         def dispatcher(self, obj):
             rv = reduce(obj)
             if isinstance(rv, str):
                 self.save_global(obj, rv)
             else:
@@ -195,16 +199,16 @@
         from pickle import dump, load, HIGHEST_PROTOCOL
     try:
         from _multiprocess import win32, Connection, PipeConnection
     except ImportError:
         from _multiprocessing import win32, Connection, PipeConnection
     from .util import Finalize
 
-    def dump(obj, file, protocol=None):
-        ForkingPickler(file, protocol).dump(obj)
+    def dump(obj, file, protocol=None, *args, **kwds):
+        ForkingPickler(file, protocol, *args, **kwds).dump(obj)
 
     #
     #
     #
 
     TERMINATE = 0x10000
     WINEXE = (sys.platform == 'win32' and getattr(sys, 'frozen', False))
```

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/heap.py` & `multiprocess-0.70.9/py3.2/multiprocess/heap.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/managers.py` & `multiprocess-0.70.9/py3.2/multiprocess/managers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/pool.py` & `multiprocess-0.70.9/py3.2/multiprocess/pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/process.py` & `multiprocess-0.70.9/py3.2/multiprocess/process.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/queues.py` & `multiprocess-0.70.9/py3.2/multiprocess/queues.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/reduction.py` & `multiprocess-0.70.9/py3.2/multiprocess/reduction.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/sharedctypes.py` & `multiprocess-0.70.9/py3.2/multiprocess/sharedctypes.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/synchronize.py` & `multiprocess-0.70.9/py3.2/multiprocess/synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/util.py` & `multiprocess-0.70.9/py3.2/multiprocess/util.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/tests/__init__.py` & `multiprocess-0.70.9/py3.2/multiprocess/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/tests/__main__.py` & `multiprocess-0.70.9/py3.2/multiprocess/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/dummy/__init__.py` & `multiprocess-0.70.9/py3.2/multiprocess/dummy/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/multiprocess/dummy/connection.py` & `multiprocess-0.70.9/py3.2/multiprocess/dummy/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/Modules/_multiprocess/connection.h` & `multiprocess-0.70.9/py3.2/Modules/_multiprocess/connection.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/Modules/_multiprocess/multiprocess.c` & `multiprocess-0.70.9/py3.2/Modules/_multiprocess/multiprocess.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/Modules/_multiprocess/multiprocess.h` & `multiprocess-0.70.9/py3.2/Modules/_multiprocess/multiprocess.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/Modules/_multiprocess/pipe_connection.c` & `multiprocess-0.70.9/py3.2/Modules/_multiprocess/pipe_connection.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/Modules/_multiprocess/semaphore.c` & `multiprocess-0.70.9/py3.2/Modules/_multiprocess/semaphore.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/Modules/_multiprocess/socket_connection.c` & `multiprocess-0.70.9/py3.2/Modules/_multiprocess/socket_connection.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/Modules/_multiprocess/win32_functions.c` & `multiprocess-0.70.9/py3.2/Modules/_multiprocess/win32_functions.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/examples/benchmarks.py` & `multiprocess-0.70.9/py3.2/examples/benchmarks.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 #
 # Simple benchmarks for the processing package
 #
 
 import time, sys, multiprocess as processing, threading, queue as Queue, gc
 processing.freezeSupport = processing.freeze_support
-xrange = range
 
 if sys.platform == 'win32':
     _timer = time.clock
 else:
     _timer = time.time
 
 delta = 1
@@ -18,17 +17,17 @@
 
 def queuespeed_func(q, c, iterations):
     a = '0' * 256
     c.acquire()
     c.notify()
     c.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         q.put(a)
-#    q.putMany((a for i in xrange(iterations))
+#    q.putMany((a for i in range(iterations))
 
     q.put('STOP')
 
 def test_queuespeed(Process, q, c):
     elapsed = 0
     iterations = 1
 
@@ -59,15 +58,15 @@
 
 def pipe_func(c, cond, iterations):
     a = '0' * 256
     cond.acquire()
     cond.notify()
     cond.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         c.send(a)
 
     c.send('STOP')
 
 def test_pipespeed():
     c, d = processing.Pipe()
     cond = processing.Condition()
@@ -103,15 +102,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             a = seq[5]
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
 
@@ -123,15 +122,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             l.acquire()
             l.release()
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
@@ -139,15 +138,15 @@
 
 #### TEST_CONDITION
 
 def conditionspeed_func(c, N):
     c.acquire()
     c.notify()
 
-    for i in xrange(N):
+    for i in range(N):
         c.wait()
         c.notify()
 
     c.release()
 
 def test_conditionspeed(Process, c):
     elapsed = 0
@@ -160,15 +159,15 @@
         p = Process(target=conditionspeed_func, args=(c, iterations))
         p.start()
 
         c.wait()
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             c.notify()
             c.wait()
 
         elapsed = _timer()-t
 
         c.release()
         p.join()
```

### Comparing `multiprocess-0.70.8/py3.2/examples/ex_newtype.py` & `multiprocess-0.70.9/py3.4/examples/ex_newtype.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,37 +1,36 @@
 #
 # This module shows how to use arbitrary callables with a subclass of
 # `BaseManager`.
 #
 
 from multiprocess import freeze_support as freezeSupport
-from multiprocess.managers import BaseManager, BaseProxy
-xrange = range
+from multiprocess.managers import BaseManager, IteratorProxy as BaseProxy
 
 ##
 
 class Foo(object):
     def f(self):
         print('you called Foo.f()')
     def g(self):
         print('you called Foo.g()')
     def _h(self):
         print('you called Foo._h()')
 
 # A simple generator function
 def baz():
-    for i in xrange(10):
+    for i in range(10):
         yield i*i
 
 # Proxy type for generator objects
 class GeneratorProxy(BaseProxy):
     def __iter__(self):
         return self
-    def next(self):
-        return self._callmethod('next')
+    def __next__(self):
+        return self._callmethod('__next__')
 
 ##
 
 class MyManager(BaseManager): pass
 
 # register the Foo class; make all public methods accessible via proxy
 MyManager.register('Foo1', Foo)
```

### Comparing `multiprocess-0.70.8/py3.2/examples/ex_pool.py` & `multiprocess-0.70.9/py3.2/examples/ex_pool.py`

 * *Files 6% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 # A test of `processing.Pool` class
 #
 
 from multiprocess import Pool, TimeoutError
 from multiprocess import cpu_count as cpuCount, current_process as currentProcess, freeze_support as freezeSupport, active_children as activeChildren
 
 import time, random, sys
-xrange = range
 
 #
 # Functions used by test code
 #
 
 def calculate(func, args):
     result = func(*args)
@@ -87,26 +86,26 @@
     # Simple benchmarks
     #
 
     N = 100000
     print('def pow3(x): return x**3')
     
     t = time.time()
-    A = list(map(pow3, xrange(N)))
-    print('\tmap(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    A = list(map(pow3, range(N)))
+    print('\tmap(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
     
     t = time.time()
-    B = pool.map(pow3, xrange(N))
-    print('\tpool.map(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    B = pool.map(pow3, range(N))
+    print('\tpool.map(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
 
     t = time.time()
-    C = list(pool.imap(pow3, xrange(N), chunksize=N//8))
-    print('\tlist(pool.imap(pow3, xrange(%d), chunksize=%d)):\n\t\t%s' \
+    C = list(pool.imap(pow3, range(N), chunksize=N//8))
+    print('\tlist(pool.imap(pow3, range(%d), chunksize=%d)):\n\t\t%s' \
           ' seconds' % (N, N//8, time.time() - t))
     
     assert A == B == C, (len(A), len(B), len(C))
     print()
     
     L = [None] * 1000000
     print('def noop(x): pass')
```

### Comparing `multiprocess-0.70.8/py3.2/examples/ex_synchronize.py` & `multiprocess-0.70.9/py3.2/examples/ex_synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/examples/ex_webserver.py` & `multiprocess-0.70.9/py3.2/examples/ex_webserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/examples/ex_workers.py` & `multiprocess-0.70.9/py3.2/examples/ex_workers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/CHANGES.html` & `multiprocess-0.70.9/py3.2/doc/CHANGES.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/connection-objects.html` & `multiprocess-0.70.9/py3.2/doc/connection-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/connection-objects.txt` & `multiprocess-0.70.9/py3.2/doc/connection-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/connection-ref.html` & `multiprocess-0.70.9/py3.2/doc/connection-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/connection-ref.txt` & `multiprocess-0.70.9/py3.2/doc/connection-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/COPYING.html` & `multiprocess-0.70.9/py3.2/doc/COPYING.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/html4css1.css` & `multiprocess-0.70.9/py3.2/doc/html4css1.css`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/index.html` & `multiprocess-0.70.9/py3.2/doc/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/index.txt` & `multiprocess-0.70.9/py3.2/doc/index.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/INSTALL.html` & `multiprocess-0.70.9/py3.2/doc/INSTALL.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/intro.html` & `multiprocess-0.70.9/py3.2/doc/intro.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/intro.txt` & `multiprocess-0.70.9/py3.2/doc/intro.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/manager-objects.html` & `multiprocess-0.70.9/py3.2/doc/manager-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/manager-objects.txt` & `multiprocess-0.70.9/py3.2/doc/manager-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/pool-objects.html` & `multiprocess-0.70.9/py3.2/doc/pool-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/pool-objects.txt` & `multiprocess-0.70.9/py3.2/doc/pool-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/process-objects.html` & `multiprocess-0.70.9/py3.2/doc/process-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/process-objects.txt` & `multiprocess-0.70.9/py3.2/doc/process-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/processing-ref.html` & `multiprocess-0.70.9/py3.2/doc/processing-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/processing-ref.txt` & `multiprocess-0.70.9/py3.2/doc/processing-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/programming-guidelines.html` & `multiprocess-0.70.9/py3.2/doc/programming-guidelines.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/programming-guidelines.txt` & `multiprocess-0.70.9/py3.2/doc/programming-guidelines.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/proxy-objects.html` & `multiprocess-0.70.9/py3.2/doc/proxy-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/proxy-objects.txt` & `multiprocess-0.70.9/py3.2/doc/proxy-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/queue-objects.html` & `multiprocess-0.70.9/py3.2/doc/queue-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/queue-objects.txt` & `multiprocess-0.70.9/py3.2/doc/queue-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/sharedctypes.html` & `multiprocess-0.70.9/py3.2/doc/sharedctypes.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/sharedctypes.txt` & `multiprocess-0.70.9/py3.2/doc/sharedctypes.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/tests.html` & `multiprocess-0.70.9/py3.2/doc/tests.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/tests.txt` & `multiprocess-0.70.9/py3.2/doc/tests.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.2/doc/THANKS.html` & `multiprocess-0.70.9/py3.2/doc/THANKS.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/index.html` & `multiprocess-0.70.9/py3.1/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/README_MODS` & `multiprocess-0.70.9/py3.1/README_MODS`

 * *Files 3% similar despite different names*

```diff
@@ -65,7 +65,8 @@
 >     pickle_protocol = PyObject_GetAttrString(temp, "HIGHEST_PROTOCOL");
 
 # ----------------------------------------------------------------------
 REPLACED "from multiprocessing" with "from multiprocess"
 REPLACED "from _multiprocessing" with "from _multiprocess"
 REPLACED "import _multiprocessing" with "import _multiprocess as _multiprocessing"
 REPLACED "multprocessing" with "multiprocess" wherever else relevant...
+ADDED *args, **kwds for ForkingPickler in __init__ and dump
```

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/__init__.py` & `multiprocess-0.70.9/py3.1/multiprocess/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -37,15 +37,15 @@
 # OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
 # HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
 # LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
 # OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
 # SUCH DAMAGE.
 #
 
-__version__ = '0.70.8'
+__version__ = '0.70.9'
 
 __all__ = [
     'Process', 'current_process', 'active_children', 'freeze_support',
     'Manager', 'Pipe', 'cpu_count', 'log_to_stderr', 'get_logger',
     'allow_connection_pickling', 'BufferTooShort', 'TimeoutError',
     'Lock', 'RLock', 'Semaphore', 'BoundedSemaphore', 'Condition',
     'Event', 'Queue', 'JoinableQueue', 'Pool', 'Value', 'Array',
```

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/connection.py` & `multiprocess-0.70.9/py3.1/multiprocess/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/forking.py` & `multiprocess-0.70.9/py3.1/multiprocess/forking.py`

 * *Files 1% similar despite different names*

```diff
@@ -57,14 +57,18 @@
 
 try:
     from dill import Pickler
 except ImportError:
     from pickle import _Pickler as Pickler
 class ForkingPickler(Pickler):
     dispatch = Pickler.dispatch.copy()
+
+    def __init__(self, *args, **kwds):
+        Pickler.__init__(self, *args, **kwds)
+
     @classmethod
     def register(cls, type, reduce):
         def dispatcher(self, obj):
             rv = reduce(obj)
             if isinstance(rv, str):
                 self.save_global(obj, rv)
             else:
@@ -191,16 +195,16 @@
         from pickle import dump, load, HIGHEST_PROTOCOL
     try:
         from _multiprocess import win32, Connection, PipeConnection
     except ImportError:
         from _multiprocessing import win32, Connection, PipeConnection
     from .util import Finalize
 
-    def dump(obj, file, protocol=None):
-        ForkingPickler(file, protocol).dump(obj)
+    def dump(obj, file, protocol=None, *args, **kwds):
+        ForkingPickler(file, protocol, *args, **kwds).dump(obj)
 
     #
     #
     #
 
     TERMINATE = 0x10000
     WINEXE = (sys.platform == 'win32' and getattr(sys, 'frozen', False))
```

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/heap.py` & `multiprocess-0.70.9/py3.1/multiprocess/heap.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/managers.py` & `multiprocess-0.70.9/py3.1/multiprocess/managers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/pool.py` & `multiprocess-0.70.9/py3.1/multiprocess/pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/process.py` & `multiprocess-0.70.9/py3.1/multiprocess/process.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/queues.py` & `multiprocess-0.70.9/py3.1/multiprocess/queues.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/reduction.py` & `multiprocess-0.70.9/py3.1/multiprocess/reduction.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/sharedctypes.py` & `multiprocess-0.70.9/py3.1/multiprocess/sharedctypes.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/synchronize.py` & `multiprocess-0.70.9/py3.1/multiprocess/synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/util.py` & `multiprocess-0.70.9/py3.1/multiprocess/util.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/tests/__init__.py` & `multiprocess-0.70.9/py3.1/multiprocess/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/tests/__main__.py` & `multiprocess-0.70.9/py3.1/multiprocess/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/dummy/__init__.py` & `multiprocess-0.70.9/py3.1/multiprocess/dummy/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/multiprocess/dummy/connection.py` & `multiprocess-0.70.9/py3.1/multiprocess/dummy/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/Modules/_multiprocess/connection.h` & `multiprocess-0.70.9/py3.1/Modules/_multiprocess/connection.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/Modules/_multiprocess/multiprocess.c` & `multiprocess-0.70.9/py3.1/Modules/_multiprocess/multiprocess.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/Modules/_multiprocess/multiprocess.h` & `multiprocess-0.70.9/py3.1/Modules/_multiprocess/multiprocess.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/Modules/_multiprocess/pipe_connection.c` & `multiprocess-0.70.9/py3.1/Modules/_multiprocess/pipe_connection.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/Modules/_multiprocess/semaphore.c` & `multiprocess-0.70.9/py3.1/Modules/_multiprocess/semaphore.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/Modules/_multiprocess/socket_connection.c` & `multiprocess-0.70.9/py3.1/Modules/_multiprocess/socket_connection.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/Modules/_multiprocess/win32_functions.c` & `multiprocess-0.70.9/py3.1/Modules/_multiprocess/win32_functions.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/examples/benchmarks.py` & `multiprocess-0.70.9/py3.1/examples/benchmarks.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 #
 # Simple benchmarks for the processing package
 #
 
 import time, sys, multiprocess as processing, threading, queue as Queue, gc
 processing.freezeSupport = processing.freeze_support
-xrange = range
 
 if sys.platform == 'win32':
     _timer = time.clock
 else:
     _timer = time.time
 
 delta = 1
@@ -18,17 +17,17 @@
 
 def queuespeed_func(q, c, iterations):
     a = '0' * 256
     c.acquire()
     c.notify()
     c.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         q.put(a)
-#    q.putMany((a for i in xrange(iterations))
+#    q.putMany((a for i in range(iterations))
 
     q.put('STOP')
 
 def test_queuespeed(Process, q, c):
     elapsed = 0
     iterations = 1
 
@@ -59,15 +58,15 @@
 
 def pipe_func(c, cond, iterations):
     a = '0' * 256
     cond.acquire()
     cond.notify()
     cond.release()
 
-    for i in xrange(iterations):
+    for i in range(iterations):
         c.send(a)
 
     c.send('STOP')
 
 def test_pipespeed():
     c, d = processing.Pipe()
     cond = processing.Condition()
@@ -103,15 +102,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             a = seq[5]
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
 
@@ -123,15 +122,15 @@
     iterations = 1
 
     while elapsed < delta:
         iterations *= 2
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             l.acquire()
             l.release()
 
         elapsed = _timer()-t
 
     print(iterations, 'iterations in', elapsed, 'seconds')
     print('average number/sec:', iterations/elapsed)
@@ -139,15 +138,15 @@
 
 #### TEST_CONDITION
 
 def conditionspeed_func(c, N):
     c.acquire()
     c.notify()
 
-    for i in xrange(N):
+    for i in range(N):
         c.wait()
         c.notify()
 
     c.release()
 
 def test_conditionspeed(Process, c):
     elapsed = 0
@@ -160,15 +159,15 @@
         p = Process(target=conditionspeed_func, args=(c, iterations))
         p.start()
 
         c.wait()
 
         t = _timer()
 
-        for i in xrange(iterations):
+        for i in range(iterations):
             c.notify()
             c.wait()
 
         elapsed = _timer()-t
 
         c.release()
         p.join()
```

### Comparing `multiprocess-0.70.8/py3.1/examples/ex_newtype.py` & `multiprocess-0.70.9/py3.3/examples/ex_newtype.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,37 +1,36 @@
 #
 # This module shows how to use arbitrary callables with a subclass of
 # `BaseManager`.
 #
 
 from multiprocess import freeze_support as freezeSupport
-from multiprocess.managers import BaseManager, BaseProxy
-xrange = range
+from multiprocess.managers import BaseManager, IteratorProxy as BaseProxy
 
 ##
 
 class Foo(object):
     def f(self):
         print('you called Foo.f()')
     def g(self):
         print('you called Foo.g()')
     def _h(self):
         print('you called Foo._h()')
 
 # A simple generator function
 def baz():
-    for i in xrange(10):
+    for i in range(10):
         yield i*i
 
 # Proxy type for generator objects
 class GeneratorProxy(BaseProxy):
     def __iter__(self):
         return self
-    def next(self):
-        return self._callmethod('next')
+    def __next__(self):
+        return self._callmethod('__next__')
 
 ##
 
 class MyManager(BaseManager): pass
 
 # register the Foo class; make all public methods accessible via proxy
 MyManager.register('Foo1', Foo)
```

### Comparing `multiprocess-0.70.8/py3.1/examples/ex_pool.py` & `multiprocess-0.70.9/py3.1/examples/ex_pool.py`

 * *Files 6% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 # A test of `processing.Pool` class
 #
 
 from multiprocess import Pool, TimeoutError
 from multiprocess import cpu_count as cpuCount, current_process as currentProcess, freeze_support as freezeSupport, active_children as activeChildren
 
 import time, random, sys
-xrange = range
 
 #
 # Functions used by test code
 #
 
 def calculate(func, args):
     result = func(*args)
@@ -87,26 +86,26 @@
     # Simple benchmarks
     #
 
     N = 100000
     print('def pow3(x): return x**3')
     
     t = time.time()
-    A = list(map(pow3, xrange(N)))
-    print('\tmap(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    A = list(map(pow3, range(N)))
+    print('\tmap(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
     
     t = time.time()
-    B = pool.map(pow3, xrange(N))
-    print('\tpool.map(pow3, xrange(%d)):\n\t\t%s seconds' % \
+    B = pool.map(pow3, range(N))
+    print('\tpool.map(pow3, range(%d)):\n\t\t%s seconds' % \
           (N, time.time() - t))
 
     t = time.time()
-    C = list(pool.imap(pow3, xrange(N), chunksize=N//8))
-    print('\tlist(pool.imap(pow3, xrange(%d), chunksize=%d)):\n\t\t%s' \
+    C = list(pool.imap(pow3, range(N), chunksize=N//8))
+    print('\tlist(pool.imap(pow3, range(%d), chunksize=%d)):\n\t\t%s' \
           ' seconds' % (N, N//8, time.time() - t))
     
     assert A == B == C, (len(A), len(B), len(C))
     print()
     
     L = [None] * 1000000
     print('def noop(x): pass')
```

### Comparing `multiprocess-0.70.8/py3.1/examples/ex_synchronize.py` & `multiprocess-0.70.9/py3.1/examples/ex_synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/examples/ex_webserver.py` & `multiprocess-0.70.9/py3.1/examples/ex_webserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/examples/ex_workers.py` & `multiprocess-0.70.9/py3.1/examples/ex_workers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/CHANGES.html` & `multiprocess-0.70.9/py3.1/doc/CHANGES.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/connection-objects.html` & `multiprocess-0.70.9/py3.1/doc/connection-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/connection-objects.txt` & `multiprocess-0.70.9/py3.1/doc/connection-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/connection-ref.html` & `multiprocess-0.70.9/py3.1/doc/connection-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/connection-ref.txt` & `multiprocess-0.70.9/py3.1/doc/connection-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/COPYING.html` & `multiprocess-0.70.9/py3.1/doc/COPYING.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/html4css1.css` & `multiprocess-0.70.9/py3.1/doc/html4css1.css`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/index.html` & `multiprocess-0.70.9/py3.1/doc/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/index.txt` & `multiprocess-0.70.9/py3.1/doc/index.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/INSTALL.html` & `multiprocess-0.70.9/py3.1/doc/INSTALL.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/intro.html` & `multiprocess-0.70.9/py3.1/doc/intro.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/intro.txt` & `multiprocess-0.70.9/py3.1/doc/intro.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/manager-objects.html` & `multiprocess-0.70.9/py3.1/doc/manager-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/manager-objects.txt` & `multiprocess-0.70.9/py3.1/doc/manager-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/pool-objects.html` & `multiprocess-0.70.9/py3.1/doc/pool-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/pool-objects.txt` & `multiprocess-0.70.9/py3.1/doc/pool-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/process-objects.html` & `multiprocess-0.70.9/py3.1/doc/process-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/process-objects.txt` & `multiprocess-0.70.9/py3.1/doc/process-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/processing-ref.html` & `multiprocess-0.70.9/py3.1/doc/processing-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/processing-ref.txt` & `multiprocess-0.70.9/py3.1/doc/processing-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/programming-guidelines.html` & `multiprocess-0.70.9/py3.1/doc/programming-guidelines.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/programming-guidelines.txt` & `multiprocess-0.70.9/py3.1/doc/programming-guidelines.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/proxy-objects.html` & `multiprocess-0.70.9/py3.1/doc/proxy-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/proxy-objects.txt` & `multiprocess-0.70.9/py3.1/doc/proxy-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/queue-objects.html` & `multiprocess-0.70.9/py3.1/doc/queue-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/queue-objects.txt` & `multiprocess-0.70.9/py3.1/doc/queue-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/sharedctypes.html` & `multiprocess-0.70.9/py3.1/doc/sharedctypes.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/sharedctypes.txt` & `multiprocess-0.70.9/py3.1/doc/sharedctypes.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/tests.html` & `multiprocess-0.70.9/py3.1/doc/tests.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/tests.txt` & `multiprocess-0.70.9/py3.1/doc/tests.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py3.1/doc/THANKS.html` & `multiprocess-0.70.9/py3.1/doc/THANKS.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/index.html` & `multiprocess-0.70.9/py2.7/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/README_MODS` & `multiprocess-0.70.9/py2.7/README_MODS`

 * *Files 1% similar despite different names*

```diff
@@ -378,7 +378,9 @@
 <         from test.test_support import run_unittest as run
 ---
 >         from test.support import run_unittest as run
 2793c2819
 <     with test_support.check_py3k_warnings(
 ---
 >     with support.check_py3k_warnings(
+# ----------------------------------------------------------------------
+ADDED *args, **kwds for ForkingPickler in __init__ and dump
```

### Comparing `multiprocess-0.70.8/py2.7/multiprocess.egg-info/PKG-INFO` & `multiprocess-0.70.9/py2.7/multiprocess.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 1.1
 Name: multiprocess
-Version: 0.70.8
+Version: 0.70.9
 Summary: better multiprocessing and multithreading in python
 Home-page: https://pypi.org/project/multiprocess
 Author: Mike McKerns
 Author-email: UNKNOWN
 License: BSD
-Download-URL: https://github.com/uqfoundation/multiprocess/releases/download/multiprocess-0.70.8/multiprocess-0.70.8.tar.gz
+Download-URL: https://github.com/uqfoundation/multiprocess/releases/download/multiprocess-0.70.9/multiprocess-0.70.9.tar.gz
 Description: -----------------------------------------------------------------
         multiprocess: better multiprocessing and multithreading in python
         -----------------------------------------------------------------
         
         About Multiprocess
         ====================
         
@@ -42,15 +42,15 @@
         
             - enhanced serialization, using ``dill``
         
         
         Current Release
         ===============
         
-        This documentation is for version ``multiprocess-0.70.8`` (a fork of ``multiprocessing-0.70a1``).
+        This documentation is for version ``multiprocess-0.70.9`` (a fork of ``multiprocessing-0.70a1``).
         
         The latest released version of ``multiprocess`` is available from::
         
             https://pypi.org/project/multiprocess
         
         ``Multiprocessing`` is distributed under a BSD license.
         
@@ -68,16 +68,16 @@
         Installation
         ============
         
         ``multiprocess`` is packaged to install from source, so you must
         download the tarball, unzip, and run the installer::
         
             [download]
-            $ tar -xvzf multiprocess-0.70.8.tgz
-            $ cd multiprocess-0.70.8
+            $ tar -xvzf multiprocess-0.70.9.tgz
+            $ cd multiprocess-0.70.9
             $ python setup.py build
             $ python setup.py install
         
         You will be warned of any missing dependencies and/or settings
         after you run the "build" step above.
         
         Alternately, ``multiprocess`` can be installed with ``pip`` or ``easy_install``::
@@ -89,15 +89,15 @@
         
         Requirements
         ============
         
         ``multiprocess`` requires::
         
             - ``python``, **version >= 2.5** or **version >= 3.1**
-            - ``dill``, **version >= 0.3.0**
+            - ``dill``, **version >= 0.3.1**
         
         Optional requirements::
         
             - ``setuptools``, **version >= 0.6**
         
         
         More Information
```

### Comparing `multiprocess-0.70.8/py2.7/multiprocess.egg-info/SOURCES.txt` & `multiprocess-0.70.9/py2.7/multiprocess.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -344,14 +344,15 @@
 py3.2/multiprocess/tests/__init__.py
 py3.2/multiprocess/tests/__main__.py
 py3.3/README_MODS
 py3.3/index.html
 py3.3/Modules/_multiprocess/multiprocess.c
 py3.3/Modules/_multiprocess/multiprocess.h
 py3.3/Modules/_multiprocess/semaphore.c
+py3.3/_multiprocess/__init__.py
 py3.3/doc/CHANGES.html
 py3.3/doc/COPYING.html
 py3.3/doc/INSTALL.html
 py3.3/doc/THANKS.html
 py3.3/doc/__init__.py
 py3.3/doc/connection-objects.html
 py3.3/doc/connection-objects.txt
@@ -406,14 +407,15 @@
 py3.3/multiprocess/tests/__init__.py
 py3.3/multiprocess/tests/__main__.py
 py3.4/README_MODS
 py3.4/index.html
 py3.4/Modules/_multiprocess/multiprocess.c
 py3.4/Modules/_multiprocess/multiprocess.h
 py3.4/Modules/_multiprocess/semaphore.c
+py3.4/_multiprocess/__init__.py
 py3.4/doc/CHANGES.html
 py3.4/doc/COPYING.html
 py3.4/doc/INSTALL.html
 py3.4/doc/THANKS.html
 py3.4/doc/__init__.py
 py3.4/doc/connection-objects.html
 py3.4/doc/connection-objects.txt
@@ -480,14 +482,15 @@
 py3.4/multiprocess/tests/test_multiprocessing_main_handling.py
 py3.4/multiprocess/tests/test_multiprocessing_spawn.py
 py3.5/README_MODS
 py3.5/index.html
 py3.5/Modules/_multiprocess/multiprocess.c
 py3.5/Modules/_multiprocess/multiprocess.h
 py3.5/Modules/_multiprocess/semaphore.c
+py3.5/_multiprocess/__init__.py
 py3.5/doc/CHANGES.html
 py3.5/doc/COPYING.html
 py3.5/doc/INSTALL.html
 py3.5/doc/THANKS.html
 py3.5/doc/__init__.py
 py3.5/doc/connection-objects.html
 py3.5/doc/connection-objects.txt
@@ -554,14 +557,15 @@
 py3.5/multiprocess/tests/test_multiprocessing_main_handling.py
 py3.5/multiprocess/tests/test_multiprocessing_spawn.py
 py3.6/README_MODS
 py3.6/index.html
 py3.6/Modules/_multiprocess/multiprocess.c
 py3.6/Modules/_multiprocess/multiprocess.h
 py3.6/Modules/_multiprocess/semaphore.c
+py3.6/_multiprocess/__init__.py
 py3.6/doc/CHANGES.html
 py3.6/doc/COPYING.html
 py3.6/doc/INSTALL.html
 py3.6/doc/THANKS.html
 py3.6/doc/__init__.py
 py3.6/doc/connection-objects.html
 py3.6/doc/connection-objects.txt
@@ -628,14 +632,15 @@
 py3.6/multiprocess/tests/test_multiprocessing_main_handling.py
 py3.6/multiprocess/tests/test_multiprocessing_spawn.py
 py3.7/README_MODS
 py3.7/index.html
 py3.7/Modules/_multiprocess/multiprocess.c
 py3.7/Modules/_multiprocess/multiprocess.h
 py3.7/Modules/_multiprocess/semaphore.c
+py3.7/_multiprocess/__init__.py
 py3.7/doc/CHANGES.html
 py3.7/doc/COPYING.html
 py3.7/doc/INSTALL.html
 py3.7/doc/THANKS.html
 py3.7/doc/__init__.py
 py3.7/doc/connection-objects.html
 py3.7/doc/connection-objects.txt
```

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/__init__.py` & `multiprocess-0.70.9/py2.7/multiprocess/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -37,15 +37,15 @@
 # OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
 # HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
 # LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
 # OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
 # SUCH DAMAGE.
 #
 
-__version__ = '0.70.8'
+__version__ = '0.70.9'
 
 __all__ = [
     'Process', 'current_process', 'active_children', 'freeze_support',
     'Manager', 'Pipe', 'cpu_count', 'log_to_stderr', 'get_logger',
     'allow_connection_pickling', 'BufferTooShort', 'TimeoutError',
     'Lock', 'RLock', 'Semaphore', 'BoundedSemaphore', 'Condition',
     'Event', 'Queue', 'JoinableQueue', 'Pool', 'Value', 'Array',
```

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/connection.py` & `multiprocess-0.70.9/py2.7/multiprocess/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/forking.py` & `multiprocess-0.70.9/py2.7/multiprocess/forking.py`

 * *Files 2% similar despite different names*

```diff
@@ -59,14 +59,17 @@
 try:
     from dill import Pickler
 except ImportError:
     from pickle import Pickler
 class ForkingPickler(Pickler):
     dispatch = Pickler.dispatch.copy()
 
+    def __init__(self, *args, **kwds):
+        Pickler.__init__(self, *args, **kwds)
+
     @classmethod
     def register(cls, type, reduce):
         def dispatcher(self, obj):
             rv = reduce(obj)
             self.save_reduce(obj=obj, *rv)
         cls.dispatch[type] = dispatcher
 
@@ -198,16 +201,16 @@
 
     try:
     #   from cPickle import dump, load, HIGHEST_PROTOCOL
         from dill import load, DEFAULT_PROTOCOL as HIGHEST_PROTOCOL
     except ImportError:
         from pickle import load, HIGHEST_PROTOCOL
 
-    def dump(obj, file, protocol=None):
-        ForkingPickler(file, protocol).dump(obj)
+    def dump(obj, file, protocol=None, *args, **kwds):
+        ForkingPickler(file, protocol, *args, **kwds).dump(obj)
 
     #
     #
     #
 
     TERMINATE = 0x10000
     WINEXE = (sys.platform == 'win32' and getattr(sys, 'frozen', False))
```

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/heap.py` & `multiprocess-0.70.9/py2.7/multiprocess/heap.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/managers.py` & `multiprocess-0.70.9/py2.7/multiprocess/managers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/pool.py` & `multiprocess-0.70.9/py2.7/multiprocess/pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/process.py` & `multiprocess-0.70.9/py2.7/multiprocess/process.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/queues.py` & `multiprocess-0.70.9/py2.7/multiprocess/queues.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/reduction.py` & `multiprocess-0.70.9/py2.7/multiprocess/reduction.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/sharedctypes.py` & `multiprocess-0.70.9/py2.7/multiprocess/sharedctypes.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/synchronize.py` & `multiprocess-0.70.9/py2.7/multiprocess/synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/util.py` & `multiprocess-0.70.9/py2.7/multiprocess/util.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/tests/__init__.py` & `multiprocess-0.70.9/py2.7/multiprocess/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/tests/__main__.py` & `multiprocess-0.70.9/py2.7/multiprocess/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/dummy/__init__.py` & `multiprocess-0.70.9/py2.7/multiprocess/dummy/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/multiprocess/dummy/connection.py` & `multiprocess-0.70.9/py2.7/multiprocess/dummy/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/Modules/_multiprocess/connection.h` & `multiprocess-0.70.9/py2.7/Modules/_multiprocess/connection.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/Modules/_multiprocess/multiprocess.c` & `multiprocess-0.70.9/py2.7/Modules/_multiprocess/multiprocess.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/Modules/_multiprocess/multiprocess.h` & `multiprocess-0.70.9/py2.7/Modules/_multiprocess/multiprocess.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/Modules/_multiprocess/pipe_connection.c` & `multiprocess-0.70.9/py2.7/Modules/_multiprocess/pipe_connection.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/Modules/_multiprocess/semaphore.c` & `multiprocess-0.70.9/py2.7/Modules/_multiprocess/semaphore.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/Modules/_multiprocess/socket_connection.c` & `multiprocess-0.70.9/py2.7/Modules/_multiprocess/socket_connection.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/Modules/_multiprocess/win32_functions.c` & `multiprocess-0.70.9/py2.7/Modules/_multiprocess/win32_functions.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/examples/benchmarks.py` & `multiprocess-0.70.9/py2.7/examples/benchmarks.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/examples/ex_newtype.py` & `multiprocess-0.70.9/py3.2/examples/ex_newtype.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,36 +1,36 @@
 #
 # This module shows how to use arbitrary callables with a subclass of
 # `BaseManager`.
 #
 
 from multiprocess import freeze_support as freezeSupport
-from multiprocess.managers import BaseManager, BaseProxy
+from multiprocess.managers import BaseManager, IteratorProxy as BaseProxy
 
 ##
 
 class Foo(object):
     def f(self):
-        print 'you called Foo.f()'
+        print('you called Foo.f()')
     def g(self):
-        print 'you called Foo.g()'
+        print('you called Foo.g()')
     def _h(self):
-        print 'you called Foo._h()'
+        print('you called Foo._h()')
 
 # A simple generator function
 def baz():
-    for i in xrange(10):
+    for i in range(10):
         yield i*i
 
 # Proxy type for generator objects
 class GeneratorProxy(BaseProxy):
     def __iter__(self):
         return self
-    def next(self):
-        return self._callmethod('next')
+    def __next__(self):
+        return self._callmethod('__next__')
 
 ##
 
 class MyManager(BaseManager): pass
 
 # register the Foo class; make all public methods accessible via proxy
 MyManager.register('Foo1', Foo)
@@ -43,35 +43,35 @@
 
 ##
 
 def test():
     manager = MyManager()
     manager.start()
 
-    print '-' * 20
+    print('-' * 20)
 
     f1 = manager.Foo1()
     f1.f()
     f1.g()
     assert not hasattr(f1, '_h')
 
-    print '-' * 20
+    print('-' * 20)
 
     f2 = manager.Foo2()
     f2.g()
     f2._h()
     assert not hasattr(f2, 'f')
 
-    print '-' * 20
+    print('-' * 20)
 
     it = manager.baz()
 
     for i in it:
-        print '<%d>' % i,
+        print('<%d>' % i, end=' ')
 
-    print
+    print()
 
 ##
 
 if __name__ == '__main__':
     freezeSupport()
     test()
```

### Comparing `multiprocess-0.70.8/py2.7/examples/ex_pool.py` & `multiprocess-0.70.9/py2.7/examples/ex_pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/examples/ex_synchronize.py` & `multiprocess-0.70.9/py2.7/examples/ex_synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/examples/ex_webserver.py` & `multiprocess-0.70.9/py2.7/examples/ex_webserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/examples/ex_workers.py` & `multiprocess-0.70.9/py2.7/examples/ex_workers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/CHANGES.html` & `multiprocess-0.70.9/py2.7/doc/CHANGES.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/connection-objects.html` & `multiprocess-0.70.9/py2.7/doc/connection-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/connection-objects.txt` & `multiprocess-0.70.9/py2.7/doc/connection-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/connection-ref.html` & `multiprocess-0.70.9/py2.7/doc/connection-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/connection-ref.txt` & `multiprocess-0.70.9/py2.7/doc/connection-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/COPYING.html` & `multiprocess-0.70.9/py2.7/doc/COPYING.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/html4css1.css` & `multiprocess-0.70.9/py2.7/doc/html4css1.css`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/index.html` & `multiprocess-0.70.9/py2.7/doc/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/index.txt` & `multiprocess-0.70.9/py2.7/doc/index.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/INSTALL.html` & `multiprocess-0.70.9/py2.7/doc/INSTALL.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/intro.html` & `multiprocess-0.70.9/py2.7/doc/intro.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/intro.txt` & `multiprocess-0.70.9/py2.7/doc/intro.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/manager-objects.html` & `multiprocess-0.70.9/py2.7/doc/manager-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/manager-objects.txt` & `multiprocess-0.70.9/py2.7/doc/manager-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/pool-objects.html` & `multiprocess-0.70.9/py2.7/doc/pool-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/pool-objects.txt` & `multiprocess-0.70.9/py2.7/doc/pool-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/process-objects.html` & `multiprocess-0.70.9/py2.7/doc/process-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/process-objects.txt` & `multiprocess-0.70.9/py2.7/doc/process-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/processing-ref.html` & `multiprocess-0.70.9/py2.7/doc/processing-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/processing-ref.txt` & `multiprocess-0.70.9/py2.7/doc/processing-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/programming-guidelines.html` & `multiprocess-0.70.9/py2.7/doc/programming-guidelines.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/programming-guidelines.txt` & `multiprocess-0.70.9/py2.7/doc/programming-guidelines.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/proxy-objects.html` & `multiprocess-0.70.9/py2.7/doc/proxy-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/proxy-objects.txt` & `multiprocess-0.70.9/py2.7/doc/proxy-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/queue-objects.html` & `multiprocess-0.70.9/py2.7/doc/queue-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/queue-objects.txt` & `multiprocess-0.70.9/py2.7/doc/queue-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/sharedctypes.html` & `multiprocess-0.70.9/py2.7/doc/sharedctypes.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/sharedctypes.txt` & `multiprocess-0.70.9/py2.7/doc/sharedctypes.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/tests.html` & `multiprocess-0.70.9/py2.7/doc/tests.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/tests.txt` & `multiprocess-0.70.9/py2.7/doc/tests.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.7/doc/THANKS.html` & `multiprocess-0.70.9/py2.7/doc/THANKS.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/index.html` & `multiprocess-0.70.9/py2.6/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/README_MODS` & `multiprocess-0.70.9/py2.6/README_MODS`

 * *Files 5% similar despite different names*

```diff
@@ -62,7 +62,8 @@
 >     pickle_protocol = PyObject_GetAttrString(temp, "HIGHEST_PROTOCOL");
 
 # ----------------------------------------------------------------------
 REPLACED "from multiprocessing" with "from multiprocess"
 REPLACED "from _multiprocessing" with "from _multiprocess"
 REPLACED "import _multiprocessing" with "import _multiprocess as _multiprocessing"
 REPLACED "multprocessing" with "multiprocess" wherever else relevant...
+ADDED *args, **kwds for ForkingPickler in __init__ and dump
```

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/__init__.py` & `multiprocess-0.70.9/py2.6/multiprocess/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -36,15 +36,15 @@
 # DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS
 # OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
 # HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT
 # LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY
 # OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF
 #
 
-__version__ = '0.70.8'
+__version__ = '0.70.9'
 
 __all__ = [
     'Process', 'current_process', 'active_children', 'freeze_support',
     'Manager', 'Pipe', 'cpu_count', 'log_to_stderr', 'get_logger',
     'allow_connection_pickling', 'BufferTooShort', 'TimeoutError',
     'Lock', 'RLock', 'Semaphore', 'BoundedSemaphore', 'Condition',
     'Event', 'Queue', 'JoinableQueue', 'Pool', 'Value', 'Array',
```

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/connection.py` & `multiprocess-0.70.9/py2.6/multiprocess/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/forking.py` & `multiprocess-0.70.9/py2.6/multiprocess/forking.py`

 * *Files 3% similar despite different names*

```diff
@@ -32,14 +32,17 @@
 try:
     from dill import Pickler
 except ImportError:
     from pickle import Pickler
 class ForkingPickler(Pickler):
     dispatch = Pickler.dispatch.copy()
 
+    def __init__(self, *args, **kwds):
+        Pickler.__init__(self, *args, **kwds)
+
     @classmethod
     def register(cls, type, reduce):
         def dispatcher(self, obj):
             rv = reduce(obj)
             self.save_reduce(obj=obj, *rv)
         cls.dispatch[type] = dispatcher
 
@@ -161,16 +164,16 @@
 
     try:
     #   from cPickle import dump, load, HIGHEST_PROTOCOL
         from dill import load, DEFAULT_PROTOCOL as HIGHEST_PROTOCOL
     except ImportError:
         from pickle import load, HIGHEST_PROTOCOL
 
-    def dump(obj, file, protocol=None):
-        ForkingPickler(file, protocol).dump(obj)
+    def dump(obj, file, protocol=None, *args, **kwds):
+        ForkingPickler(file, protocol, *args, **kwds).dump(obj)
 
     #
     #
     #
 
     TERMINATE = 0x10000
     WINEXE = (sys.platform == 'win32' and getattr(sys, 'frozen', False))
```

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/heap.py` & `multiprocess-0.70.9/py2.6/multiprocess/heap.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/managers.py` & `multiprocess-0.70.9/py2.6/multiprocess/managers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/pool.py` & `multiprocess-0.70.9/py2.6/multiprocess/pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/process.py` & `multiprocess-0.70.9/py2.6/multiprocess/process.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/queues.py` & `multiprocess-0.70.9/py2.6/multiprocess/queues.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/reduction.py` & `multiprocess-0.70.9/py2.6/multiprocess/reduction.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/sharedctypes.py` & `multiprocess-0.70.9/py2.6/multiprocess/sharedctypes.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/synchronize.py` & `multiprocess-0.70.9/py2.6/multiprocess/synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/util.py` & `multiprocess-0.70.9/py2.6/multiprocess/util.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/tests/__init__.py` & `multiprocess-0.70.9/py2.6/multiprocess/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/tests/__main__.py` & `multiprocess-0.70.9/py2.6/multiprocess/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/dummy/__init__.py` & `multiprocess-0.70.9/py2.6/multiprocess/dummy/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/multiprocess/dummy/connection.py` & `multiprocess-0.70.9/py2.6/multiprocess/dummy/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/Modules/_multiprocess/connection.h` & `multiprocess-0.70.9/py2.6/Modules/_multiprocess/connection.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/Modules/_multiprocess/multiprocess.c` & `multiprocess-0.70.9/py2.6/Modules/_multiprocess/multiprocess.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/Modules/_multiprocess/multiprocess.h` & `multiprocess-0.70.9/py2.6/Modules/_multiprocess/multiprocess.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/Modules/_multiprocess/pipe_connection.c` & `multiprocess-0.70.9/py2.6/Modules/_multiprocess/pipe_connection.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/Modules/_multiprocess/semaphore.c` & `multiprocess-0.70.9/py2.6/Modules/_multiprocess/semaphore.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/Modules/_multiprocess/socket_connection.c` & `multiprocess-0.70.9/py2.6/Modules/_multiprocess/socket_connection.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/Modules/_multiprocess/win32_functions.c` & `multiprocess-0.70.9/py2.6/Modules/_multiprocess/win32_functions.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/examples/benchmarks.py` & `multiprocess-0.70.9/py2.6/examples/benchmarks.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/examples/ex_newtype.py` & `multiprocess-0.70.9/py3.1/examples/ex_newtype.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,36 +1,36 @@
 #
 # This module shows how to use arbitrary callables with a subclass of
 # `BaseManager`.
 #
 
 from multiprocess import freeze_support as freezeSupport
-from multiprocess.managers import BaseManager, BaseProxy
+from multiprocess.managers import BaseManager, IteratorProxy as BaseProxy
 
 ##
 
 class Foo(object):
     def f(self):
-        print 'you called Foo.f()'
+        print('you called Foo.f()')
     def g(self):
-        print 'you called Foo.g()'
+        print('you called Foo.g()')
     def _h(self):
-        print 'you called Foo._h()'
+        print('you called Foo._h()')
 
 # A simple generator function
 def baz():
-    for i in xrange(10):
+    for i in range(10):
         yield i*i
 
 # Proxy type for generator objects
 class GeneratorProxy(BaseProxy):
     def __iter__(self):
         return self
-    def next(self):
-        return self._callmethod('next')
+    def __next__(self):
+        return self._callmethod('__next__')
 
 ##
 
 class MyManager(BaseManager): pass
 
 # register the Foo class; make all public methods accessible via proxy
 MyManager.register('Foo1', Foo)
@@ -43,35 +43,35 @@
 
 ##
 
 def test():
     manager = MyManager()
     manager.start()
 
-    print '-' * 20
+    print('-' * 20)
 
     f1 = manager.Foo1()
     f1.f()
     f1.g()
     assert not hasattr(f1, '_h')
 
-    print '-' * 20
+    print('-' * 20)
 
     f2 = manager.Foo2()
     f2.g()
     f2._h()
     assert not hasattr(f2, 'f')
 
-    print '-' * 20
+    print('-' * 20)
 
     it = manager.baz()
 
     for i in it:
-        print '<%d>' % i,
+        print('<%d>' % i, end=' ')
 
-    print
+    print()
 
 ##
 
 if __name__ == '__main__':
     freezeSupport()
     test()
```

### Comparing `multiprocess-0.70.8/py2.6/examples/ex_pool.py` & `multiprocess-0.70.9/py2.6/examples/ex_pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/examples/ex_synchronize.py` & `multiprocess-0.70.9/py2.6/examples/ex_synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/examples/ex_webserver.py` & `multiprocess-0.70.9/py2.6/examples/ex_webserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/examples/ex_workers.py` & `multiprocess-0.70.9/py2.6/examples/ex_workers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/CHANGES.html` & `multiprocess-0.70.9/py2.6/doc/CHANGES.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/connection-objects.html` & `multiprocess-0.70.9/py2.6/doc/connection-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/connection-objects.txt` & `multiprocess-0.70.9/py2.6/doc/connection-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/connection-ref.html` & `multiprocess-0.70.9/py2.6/doc/connection-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/connection-ref.txt` & `multiprocess-0.70.9/py2.6/doc/connection-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/COPYING.html` & `multiprocess-0.70.9/py2.6/doc/COPYING.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/html4css1.css` & `multiprocess-0.70.9/py2.6/doc/html4css1.css`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/index.html` & `multiprocess-0.70.9/py2.6/doc/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/index.txt` & `multiprocess-0.70.9/py2.6/doc/index.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/INSTALL.html` & `multiprocess-0.70.9/py2.6/doc/INSTALL.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/intro.html` & `multiprocess-0.70.9/py2.6/doc/intro.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/intro.txt` & `multiprocess-0.70.9/py2.6/doc/intro.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/manager-objects.html` & `multiprocess-0.70.9/py2.6/doc/manager-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/manager-objects.txt` & `multiprocess-0.70.9/py2.6/doc/manager-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/pool-objects.html` & `multiprocess-0.70.9/py2.6/doc/pool-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/pool-objects.txt` & `multiprocess-0.70.9/py2.6/doc/pool-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/process-objects.html` & `multiprocess-0.70.9/py2.6/doc/process-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/process-objects.txt` & `multiprocess-0.70.9/py2.6/doc/process-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/processing-ref.html` & `multiprocess-0.70.9/py2.6/doc/processing-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/processing-ref.txt` & `multiprocess-0.70.9/py2.6/doc/processing-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/programming-guidelines.html` & `multiprocess-0.70.9/py2.6/doc/programming-guidelines.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/programming-guidelines.txt` & `multiprocess-0.70.9/py2.6/doc/programming-guidelines.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/proxy-objects.html` & `multiprocess-0.70.9/py2.6/doc/proxy-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/proxy-objects.txt` & `multiprocess-0.70.9/py2.6/doc/proxy-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/queue-objects.html` & `multiprocess-0.70.9/py2.6/doc/queue-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/queue-objects.txt` & `multiprocess-0.70.9/py2.6/doc/queue-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/sharedctypes.html` & `multiprocess-0.70.9/py2.6/doc/sharedctypes.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/sharedctypes.txt` & `multiprocess-0.70.9/py2.6/doc/sharedctypes.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/tests.html` & `multiprocess-0.70.9/py2.6/doc/tests.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/tests.txt` & `multiprocess-0.70.9/py2.6/doc/tests.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.6/doc/THANKS.html` & `multiprocess-0.70.9/py2.6/doc/THANKS.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/index.html` & `multiprocess-0.70.9/py2.5/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/README_MODS` & `multiprocess-0.70.9/py2.5/README_MODS`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/__init__.py` & `multiprocess-0.70.9/py2.5/processing/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/connection.py` & `multiprocess-0.70.9/py2.5/processing/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/finalize.py` & `multiprocess-0.70.9/py2.5/processing/finalize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/forking.py` & `multiprocess-0.70.9/py2.5/processing/forking.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/heap.py` & `multiprocess-0.70.9/py2.5/processing/heap.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/logger.py` & `multiprocess-0.70.9/py2.5/processing/logger.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/managers.py` & `multiprocess-0.70.9/py2.5/processing/managers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/pool.py` & `multiprocess-0.70.9/py2.5/processing/pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/process.py` & `multiprocess-0.70.9/py2.5/processing/process.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/queue.py` & `multiprocess-0.70.9/py2.5/processing/queue.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/reduction.py` & `multiprocess-0.70.9/py2.5/processing/reduction.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/sharedctypes.py` & `multiprocess-0.70.9/py2.5/processing/sharedctypes.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/synchronize.py` & `multiprocess-0.70.9/py2.5/processing/synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/tests/__init__.py` & `multiprocess-0.70.9/py2.5/processing/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/tests/__main__.py` & `multiprocess-0.70.9/py2.5/processing/tests/__main__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/dummy/__init__.py` & `multiprocess-0.70.9/py2.5/processing/dummy/__init__.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/processing/dummy/connection.py` & `multiprocess-0.70.9/py2.5/processing/dummy/connection.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/Modules/_processing/connection.h` & `multiprocess-0.70.9/py2.5/Modules/_processing/connection.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/Modules/_processing/pipe_connection.c` & `multiprocess-0.70.9/py2.5/Modules/_processing/pipe_connection.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/Modules/_processing/processing.c` & `multiprocess-0.70.9/py2.5/Modules/_processing/processing.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/Modules/_processing/processing.h` & `multiprocess-0.70.9/py2.5/Modules/_processing/processing.h`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/Modules/_processing/semaphore.c` & `multiprocess-0.70.9/py2.5/Modules/_processing/semaphore.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/Modules/_processing/socket_connection.c` & `multiprocess-0.70.9/py2.5/Modules/_processing/socket_connection.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/Modules/_processing/win_functions.c` & `multiprocess-0.70.9/py2.5/Modules/_processing/win_functions.c`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/examples/benchmarks.py` & `multiprocess-0.70.9/py2.5/examples/benchmarks.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/examples/ex_newtype.py` & `multiprocess-0.70.9/py2.5/examples/ex_newtype.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/examples/ex_pool.py` & `multiprocess-0.70.9/py2.5/examples/ex_pool.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/examples/ex_synchronize.py` & `multiprocess-0.70.9/py2.5/examples/ex_synchronize.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/examples/ex_webserver.py` & `multiprocess-0.70.9/py2.5/examples/ex_webserver.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/examples/ex_workers.py` & `multiprocess-0.70.9/py2.5/examples/ex_workers.py`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/CHANGES.html` & `multiprocess-0.70.9/py2.5/doc/CHANGES.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/connection-objects.html` & `multiprocess-0.70.9/py2.5/doc/connection-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/connection-objects.txt` & `multiprocess-0.70.9/py2.5/doc/connection-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/connection-ref.html` & `multiprocess-0.70.9/py2.5/doc/connection-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/connection-ref.txt` & `multiprocess-0.70.9/py2.5/doc/connection-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/COPYING.html` & `multiprocess-0.70.9/py2.5/doc/COPYING.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/html4css1.css` & `multiprocess-0.70.9/py2.5/doc/html4css1.css`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/index.html` & `multiprocess-0.70.9/py2.5/doc/index.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/index.txt` & `multiprocess-0.70.9/py2.5/doc/index.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/INSTALL.html` & `multiprocess-0.70.9/py2.5/doc/INSTALL.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/intro.html` & `multiprocess-0.70.9/py2.5/doc/intro.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/intro.txt` & `multiprocess-0.70.9/py2.5/doc/intro.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/manager-objects.html` & `multiprocess-0.70.9/py2.5/doc/manager-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/manager-objects.txt` & `multiprocess-0.70.9/py2.5/doc/manager-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/pool-objects.html` & `multiprocess-0.70.9/py2.5/doc/pool-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/pool-objects.txt` & `multiprocess-0.70.9/py2.5/doc/pool-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/process-objects.html` & `multiprocess-0.70.9/py2.5/doc/process-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/process-objects.txt` & `multiprocess-0.70.9/py2.5/doc/process-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/processing-ref.html` & `multiprocess-0.70.9/py2.5/doc/processing-ref.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/processing-ref.txt` & `multiprocess-0.70.9/py2.5/doc/processing-ref.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/programming-guidelines.html` & `multiprocess-0.70.9/py2.5/doc/programming-guidelines.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/programming-guidelines.txt` & `multiprocess-0.70.9/py2.5/doc/programming-guidelines.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/proxy-objects.html` & `multiprocess-0.70.9/py2.5/doc/proxy-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/proxy-objects.txt` & `multiprocess-0.70.9/py2.5/doc/proxy-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/queue-objects.html` & `multiprocess-0.70.9/py2.5/doc/queue-objects.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/queue-objects.txt` & `multiprocess-0.70.9/py2.5/doc/queue-objects.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/sharedctypes.html` & `multiprocess-0.70.9/py2.5/doc/sharedctypes.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/sharedctypes.txt` & `multiprocess-0.70.9/py2.5/doc/sharedctypes.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/tests.html` & `multiprocess-0.70.9/py2.5/doc/tests.html`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/tests.txt` & `multiprocess-0.70.9/py2.5/doc/tests.txt`

 * *Files identical despite different names*

### Comparing `multiprocess-0.70.8/py2.5/doc/THANKS.html` & `multiprocess-0.70.9/py2.5/doc/THANKS.html`

 * *Files identical despite different names*

