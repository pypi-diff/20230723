# Comparing `tmp/get-docker-secret-1.0.2.tar.gz` & `tmp/get-docker-secret-2.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "get-docker-secret-1.0.2.tar", last modified: Thu Mar 10 08:41:08 2022, max compression
+gzip compressed data, was "get-docker-secret-2.0.0.tar", last modified: Sun Jul 23 08:13:11 2023, max compression
```

## Comparing `get-docker-secret-1.0.2.tar` & `get-docker-secret-2.0.0.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxrwxr-x   0 amelch    (1000) amelch    (1000)        0 2022-03-10 08:41:08.941550 get-docker-secret-1.0.2/
--rw-rw-r--   0 amelch    (1000) amelch    (1000)     1051 2021-03-18 17:31:06.000000 get-docker-secret-1.0.2/LICENSE.txt
--rw-rw-r--   0 amelch    (1000) amelch    (1000)       38 2021-03-18 17:31:06.000000 get-docker-secret-1.0.2/MANIFEST.in
--rw-rw-r--   0 amelch    (1000) amelch    (1000)     2565 2022-03-10 08:41:08.937550 get-docker-secret-1.0.2/PKG-INFO
--rw-rw-r--   0 amelch    (1000) amelch    (1000)     1896 2021-03-19 10:28:44.000000 get-docker-secret-1.0.2/README.md
-drwxrwxr-x   0 amelch    (1000) amelch    (1000)        0 2022-03-10 08:41:08.937550 get-docker-secret-1.0.2/get_docker_secret.egg-info/
--rw-rw-r--   0 amelch    (1000) amelch    (1000)     2565 2022-03-10 08:41:08.000000 get-docker-secret-1.0.2/get_docker_secret.egg-info/PKG-INFO
--rw-rw-r--   0 amelch    (1000) amelch    (1000)      227 2022-03-10 08:41:08.000000 get-docker-secret-1.0.2/get_docker_secret.egg-info/SOURCES.txt
--rw-rw-r--   0 amelch    (1000) amelch    (1000)        1 2022-03-10 08:41:08.000000 get-docker-secret-1.0.2/get_docker_secret.egg-info/dependency_links.txt
--rw-rw-r--   0 amelch    (1000) amelch    (1000)       18 2022-03-10 08:41:08.000000 get-docker-secret-1.0.2/get_docker_secret.egg-info/top_level.txt
--rw-rw-r--   0 amelch    (1000) amelch    (1000)     2106 2021-03-19 09:37:28.000000 get-docker-secret-1.0.2/get_docker_secret.py
--rw-rw-r--   0 amelch    (1000) amelch    (1000)       38 2022-03-10 08:41:08.941550 get-docker-secret-1.0.2/setup.cfg
--rw-rw-r--   0 amelch    (1000) amelch    (1000)      954 2021-03-19 10:18:06.000000 get-docker-secret-1.0.2/setup.py
+drwxrwxr-x   0 amelch    (1000) amelch    (1000)        0 2023-07-23 08:13:11.608196 get-docker-secret-2.0.0/
+-rw-rw-r--   0 amelch    (1000) amelch    (1000)     1051 2023-07-23 08:02:21.000000 get-docker-secret-2.0.0/LICENSE.txt
+-rw-rw-r--   0 amelch    (1000) amelch    (1000)       38 2023-07-23 08:02:21.000000 get-docker-secret-2.0.0/MANIFEST.in
+-rw-rw-r--   0 amelch    (1000) amelch    (1000)     2807 2023-07-23 08:13:11.608196 get-docker-secret-2.0.0/PKG-INFO
+-rw-rw-r--   0 amelch    (1000) amelch    (1000)     2056 2023-07-23 08:10:33.000000 get-docker-secret-2.0.0/README.md
+drwxrwxr-x   0 amelch    (1000) amelch    (1000)        0 2023-07-23 08:13:11.608196 get-docker-secret-2.0.0/get_docker_secret.egg-info/
+-rw-rw-r--   0 amelch    (1000) amelch    (1000)     2807 2023-07-23 08:13:11.000000 get-docker-secret-2.0.0/get_docker_secret.egg-info/PKG-INFO
+-rw-rw-r--   0 amelch    (1000) amelch    (1000)      227 2023-07-23 08:13:11.000000 get-docker-secret-2.0.0/get_docker_secret.egg-info/SOURCES.txt
+-rw-rw-r--   0 amelch    (1000) amelch    (1000)        1 2023-07-23 08:13:11.000000 get-docker-secret-2.0.0/get_docker_secret.egg-info/dependency_links.txt
+-rw-rw-r--   0 amelch    (1000) amelch    (1000)       18 2023-07-23 08:13:11.000000 get-docker-secret-2.0.0/get_docker_secret.egg-info/top_level.txt
+-rw-rw-r--   0 amelch    (1000) amelch    (1000)     2099 2023-07-23 08:02:21.000000 get-docker-secret-2.0.0/get_docker_secret.py
+-rw-rw-r--   0 amelch    (1000) amelch    (1000)       38 2023-07-23 08:13:11.608196 get-docker-secret-2.0.0/setup.cfg
+-rw-rw-r--   0 amelch    (1000) amelch    (1000)     1054 2023-07-23 08:11:06.000000 get-docker-secret-2.0.0/setup.py
```

### Comparing `get-docker-secret-1.0.2/LICENSE.txt` & `get-docker-secret-2.0.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `get-docker-secret-1.0.2/PKG-INFO` & `get-docker-secret-2.0.0/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,23 +1,24 @@
 Metadata-Version: 2.1
 Name: get-docker-secret
-Version: 1.0.2
+Version: 2.0.0
 Summary: Utility function to fetch docker secrets/envvars.
 Home-page: https://github.com/fischerfredl/get-docker-secret
 Author: Alfred Melch
 Author-email: dev@melch.pro
 License: MIT
 Keywords: docker,secret,envvar,config
-Platform: UNKNOWN
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 2.7
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
 
 [![version](https://img.shields.io/pypi/v/get-docker-secret.svg)](https://pypi.python.org/pypi/get-docker-secret)
 [![license](https://img.shields.io/pypi/l/get-docker-secret.svg)](https://pypi.python.org/pypi/get-docker-secret)
 [![pyversions](https://img.shields.io/pypi/pyversions/get-docker-secret.svg)](https://pypi.python.org/pypi/get-docker-secret)
 [![coverage](https://img.shields.io/codecov/c/github/fischerfredl/get-docker-secret.svg)](https://codecov.io/gh/Fischerfredl/get-docker-secret)
@@ -53,20 +54,23 @@
 python setup.py test
 ```
 
 not tested under windows
 
 ## Changelog
 
+
+### 2.0.0 - 2023-07-23
+
+- Changed: Use canonical `/run/secrets` directory to read secrets from (changed from `/var/run/secrets`) (PR #4) (Thanks @ThorpeJosh)
+
 ### 1.0.2 - 2021-03-19
 
 - Fixed: Only strip trailing newlines from secrets file
 
 ### 1.0.1 - 2019-12-07
 
 - Fixed: Strip values read from file.
 
 ### 1.0.0 - 2018-01-30
 
 - Initial publish
-
-
```

### Comparing `get-docker-secret-1.0.2/README.md` & `get-docker-secret-2.0.0/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -100,20 +100,30 @@
 00000630: 7265 745f 6b65 7927 2c20 6465 6661 756c  ret_key', defaul
 00000640: 743d 2776 6572 795f 7365 6372 6574 2729  t='very_secret')
 00000650: 0a60 6060 0a0a 2323 2054 6573 7469 6e67  .```..## Testing
 00000660: 0a0a 6060 6070 7974 686f 6e0a 7079 7468  ..```python.pyth
 00000670: 6f6e 2073 6574 7570 2e70 7920 7465 7374  on setup.py test
 00000680: 0a60 6060 0a0a 6e6f 7420 7465 7374 6564  .```..not tested
 00000690: 2075 6e64 6572 2077 696e 646f 7773 0a0a   under windows..
-000006a0: 2323 2043 6861 6e67 656c 6f67 0a0a 2323  ## Changelog..##
-000006b0: 2320 312e 302e 3220 2d20 3230 3231 2d30  # 1.0.2 - 2021-0
-000006c0: 332d 3139 0a0a 2d20 4669 7865 643a 204f  3-19..- Fixed: O
-000006d0: 6e6c 7920 7374 7269 7020 7472 6169 6c69  nly strip traili
-000006e0: 6e67 206e 6577 6c69 6e65 7320 6672 6f6d  ng newlines from
-000006f0: 2073 6563 7265 7473 2066 696c 650a 0a23   secrets file..#
-00000700: 2323 2031 2e30 2e31 202d 2032 3031 392d  ## 1.0.1 - 2019-
-00000710: 3132 2d30 370a 0a2d 2046 6978 6564 3a20  12-07..- Fixed: 
-00000720: 5374 7269 7020 7661 6c75 6573 2072 6561  Strip values rea
-00000730: 6420 6672 6f6d 2066 696c 652e 0a0a 2323  d from file...##
-00000740: 2320 312e 302e 3020 2d20 3230 3138 2d30  # 1.0.0 - 2018-0
-00000750: 312d 3330 0a0a 2d20 496e 6974 6961 6c20  1-30..- Initial 
-00000760: 7075 626c 6973 680a                      publish.
+000006a0: 2323 2043 6861 6e67 656c 6f67 0a0a 0a23  ## Changelog...#
+000006b0: 2323 2032 2e30 2e30 202d 2032 3032 332d  ## 2.0.0 - 2023-
+000006c0: 3037 2d32 330a 0a2d 2043 6861 6e67 6564  07-23..- Changed
+000006d0: 3a20 5573 6520 6361 6e6f 6e69 6361 6c20  : Use canonical 
+000006e0: 602f 7275 6e2f 7365 6372 6574 7360 2064  `/run/secrets` d
+000006f0: 6972 6563 746f 7279 2074 6f20 7265 6164  irectory to read
+00000700: 2073 6563 7265 7473 2066 726f 6d20 2863   secrets from (c
+00000710: 6861 6e67 6564 2066 726f 6d20 602f 7661  hanged from `/va
+00000720: 722f 7275 6e2f 7365 6372 6574 7360 2920  r/run/secrets`) 
+00000730: 2850 5220 2334 2920 2854 6861 6e6b 7320  (PR #4) (Thanks 
+00000740: 4054 686f 7270 654a 6f73 6829 0a0a 2323  @ThorpeJosh)..##
+00000750: 2320 312e 302e 3220 2d20 3230 3231 2d30  # 1.0.2 - 2021-0
+00000760: 332d 3139 0a0a 2d20 4669 7865 643a 204f  3-19..- Fixed: O
+00000770: 6e6c 7920 7374 7269 7020 7472 6169 6c69  nly strip traili
+00000780: 6e67 206e 6577 6c69 6e65 7320 6672 6f6d  ng newlines from
+00000790: 2073 6563 7265 7473 2066 696c 650a 0a23   secrets file..#
+000007a0: 2323 2031 2e30 2e31 202d 2032 3031 392d  ## 1.0.1 - 2019-
+000007b0: 3132 2d30 370a 0a2d 2046 6978 6564 3a20  12-07..- Fixed: 
+000007c0: 5374 7269 7020 7661 6c75 6573 2072 6561  Strip values rea
+000007d0: 6420 6672 6f6d 2066 696c 652e 0a0a 2323  d from file...##
+000007e0: 2320 312e 302e 3020 2d20 3230 3138 2d30  # 1.0.0 - 2018-0
+000007f0: 312d 3330 0a0a 2d20 496e 6974 6961 6c20  1-30..- Initial 
+00000800: 7075 626c 6973 680a                      publish.
```

### Comparing `get-docker-secret-1.0.2/get_docker_secret.egg-info/PKG-INFO` & `get-docker-secret-2.0.0/get_docker_secret.egg-info/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,23 +1,24 @@
 Metadata-Version: 2.1
 Name: get-docker-secret
-Version: 1.0.2
+Version: 2.0.0
 Summary: Utility function to fetch docker secrets/envvars.
 Home-page: https://github.com/fischerfredl/get-docker-secret
 Author: Alfred Melch
 Author-email: dev@melch.pro
 License: MIT
 Keywords: docker,secret,envvar,config
-Platform: UNKNOWN
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 2.7
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
 
 [![version](https://img.shields.io/pypi/v/get-docker-secret.svg)](https://pypi.python.org/pypi/get-docker-secret)
 [![license](https://img.shields.io/pypi/l/get-docker-secret.svg)](https://pypi.python.org/pypi/get-docker-secret)
 [![pyversions](https://img.shields.io/pypi/pyversions/get-docker-secret.svg)](https://pypi.python.org/pypi/get-docker-secret)
 [![coverage](https://img.shields.io/codecov/c/github/fischerfredl/get-docker-secret.svg)](https://codecov.io/gh/Fischerfredl/get-docker-secret)
@@ -53,20 +54,23 @@
 python setup.py test
 ```
 
 not tested under windows
 
 ## Changelog
 
+
+### 2.0.0 - 2023-07-23
+
+- Changed: Use canonical `/run/secrets` directory to read secrets from (changed from `/var/run/secrets`) (PR #4) (Thanks @ThorpeJosh)
+
 ### 1.0.2 - 2021-03-19
 
 - Fixed: Only strip trailing newlines from secrets file
 
 ### 1.0.1 - 2019-12-07
 
 - Fixed: Strip values read from file.
 
 ### 1.0.0 - 2018-01-30
 
 - Initial publish
-
-
```

### Comparing `get-docker-secret-1.0.2/get_docker_secret.py` & `get-docker-secret-2.0.0/get_docker_secret.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import os
 
 root = os.path.abspath(os.sep)
 
 
 def get_docker_secret(name, default=None, cast_to=str, autocast_name=True, getenv=True, safe=True,
-                      secrets_dir=os.path.join(root, 'var', 'run', 'secrets')):
+                      secrets_dir=os.path.join(root, 'run', 'secrets')):
     """This function fetches a docker secret
 
     :param name: the name of the docker secret
     :param default: the default value if no secret found
     :param cast_to: casts the value to the given type
     :param autocast_name: whether the name should be lowercase for secrets and upper case for environment
     :param getenv: if environment variable should be fetched as fallback
```

