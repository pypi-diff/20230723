# Comparing `tmp/crypto_licensing-3.3.0.tar.gz` & `tmp/crypto_licensing-3.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "crypto_licensing-3.3.0.tar", last modified: Tue Feb 21 16:53:47 2023, max compression
+gzip compressed data, was "crypto_licensing-3.3.1.tar", last modified: Sun Jul 23 20:36:47 2023, max compression
```

## Comparing `crypto_licensing-3.3.0.tar` & `crypto_licensing-3.3.1.tar`

### file list

```diff
@@ -1,49 +1,49 @@
-drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-02-21 16:53:47.467643 crypto_licensing-3.3.0/
--rw-rw-r--   0 perry      (501) staff       (20)    35147 2022-01-25 19:29:48.000000 crypto_licensing-3.3.0/COPYING
--rw-rw-r--   0 perry      (501) staff       (20)     1184 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/LICENSE
--rw-rw-r--   0 perry      (501) staff       (20)      138 2022-02-23 17:37:17.000000 crypto_licensing-3.3.0/MANIFEST.in
--rw-rw-r--   0 perry      (501) staff       (20)     1392 2023-02-21 16:53:47.466894 crypto_licensing-3.3.0/PKG-INFO
--rw-rw-r--   0 perry      (501) staff       (20)     4468 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/README.org
--rw-rw-r--   0 perry      (501) staff       (20)     7177 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/README.txt
-drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-02-21 16:53:47.440753 crypto_licensing-3.3.0/crypto_licensing/
--rw-rw-r--   0 perry      (501) staff       (20)     1364 2023-02-14 14:06:11.000000 crypto_licensing-3.3.0/crypto_licensing/__init__.py
--rw-rw-r--   0 perry      (501) staff       (20)     1365 2023-02-14 14:41:09.000000 crypto_licensing-3.3.0/crypto_licensing/__main__.py
--rw-rw-r--   0 perry      (501) staff       (20)    10632 2023-02-16 18:04:11.000000 crypto_licensing-3.3.0/crypto_licensing/cli.py
--rw-rw-r--   0 perry      (501) staff       (20)     3993 2023-02-15 19:50:25.000000 crypto_licensing-3.3.0/crypto_licensing/cli_test.py
--rw-rw-r--   0 perry      (501) staff       (20)     5264 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/crypto_licensing/crypto_test.py
-drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-02-21 16:53:47.441386 crypto_licensing-3.3.0/crypto_licensing/ed25519/
--rw-rw-r--   0 perry      (501) staff       (20)     1655 2023-02-14 14:07:01.000000 crypto_licensing-3.3.0/crypto_licensing/ed25519/__init__.py
--rw-rw-r--   0 perry      (501) staff       (20)     5033 2022-01-24 17:18:08.000000 crypto_licensing-3.3.0/crypto_licensing/ed25519_djb.py
-drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-02-21 16:53:47.443278 crypto_licensing-3.3.0/crypto_licensing/ed25519ll_pyonly/
--rw-rw-r--   0 perry      (501) staff       (20)     2319 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/crypto_licensing/ed25519ll_pyonly/__init__.py
--rw-rw-r--   0 perry      (501) staff       (20)     6905 2022-01-19 19:14:43.000000 crypto_licensing-3.3.0/crypto_licensing/ed25519ll_pyonly/djbec.py
-drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-02-21 16:53:47.453781 crypto_licensing-3.3.0/crypto_licensing/licensing/
--rw-rw-r--   0 perry      (501) staff       (20)     1606 2023-02-21 15:58:27.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/__init__.py
--rw-rw-r--   0 perry      (501) staff       (20)     1196 2023-02-14 14:07:40.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/__main__.py
--rw-rw-r--   0 perry      (501) staff       (20)     1942 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/bitquery_test.py
--rw-rw-r--   0 perry      (501) staff       (20)     2194 2023-02-14 14:08:13.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/defaults.py
-drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-02-21 16:53:47.459384 crypto_licensing-3.3.0/crypto_licensing/licensing/doh/
--rw-rw-r--   0 perry      (501) staff       (20)     4511 2023-02-14 14:08:34.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/doh/__init__.py
--rw-rw-r--   0 perry      (501) staff       (20)     1362 2023-02-14 14:15:34.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/doh/__main__.py
--rw-rw-r--   0 perry      (501) staff       (20)     2731 2023-02-14 14:16:10.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/doh/cli.py
--rw-rw-r--   0 perry      (501) staff       (20)     3035 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/doh_test.py
--rw-rw-r--   0 perry      (501) staff       (20)    17971 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/grant_test.py
--rw-rw-r--   0 perry      (501) staff       (20)     7469 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/licensing_test.py
--rw-rw-r--   0 perry      (501) staff       (20)    96445 2023-02-14 14:08:47.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/main.py
--rw-rw-r--   0 perry      (501) staff       (20)   143017 2023-02-21 16:50:37.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/verification.py
--rw-rw-r--   0 perry      (501) staff       (20)    40362 2023-02-21 15:30:21.000000 crypto_licensing-3.3.0/crypto_licensing/licensing/verification_test.py
--rw-rw-r--   0 perry      (501) staff       (20)    43408 2023-02-17 20:51:56.000000 crypto_licensing-3.3.0/crypto_licensing/misc.py
--rw-rw-r--   0 perry      (501) staff       (20)     9528 2023-02-05 15:25:17.000000 crypto_licensing-3.3.0/crypto_licensing/misc_test.py
--rw-rw-r--   0 perry      (501) staff       (20)       88 2023-02-21 16:33:34.000000 crypto_licensing-3.3.0/crypto_licensing/version.py
-drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-02-21 16:53:47.465934 crypto_licensing-3.3.0/crypto_licensing.egg-info/
--rw-rw-r--   0 perry      (501) staff       (20)     1392 2023-02-21 16:53:47.000000 crypto_licensing-3.3.0/crypto_licensing.egg-info/PKG-INFO
--rw-rw-r--   0 perry      (501) staff       (20)     1331 2023-02-21 16:53:47.000000 crypto_licensing-3.3.0/crypto_licensing.egg-info/SOURCES.txt
--rw-rw-r--   0 perry      (501) staff       (20)        1 2023-02-21 16:53:47.000000 crypto_licensing-3.3.0/crypto_licensing.egg-info/dependency_links.txt
--rw-rw-r--   0 perry      (501) staff       (20)       74 2023-02-21 16:53:47.000000 crypto_licensing-3.3.0/crypto_licensing.egg-info/entry_points.txt
--rw-rw-r--   0 perry      (501) staff       (20)      263 2023-02-21 16:53:47.000000 crypto_licensing-3.3.0/crypto_licensing.egg-info/requires.txt
--rw-rw-r--   0 perry      (501) staff       (20)      134 2023-02-21 16:53:47.000000 crypto_licensing-3.3.0/crypto_licensing.egg-info/top_level.txt
--rw-rw-r--   0 perry      (501) staff       (20)       48 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/requirements-dev.txt
--rw-rw-r--   0 perry      (501) staff       (20)       21 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/requirements-tests.txt
--rw-rw-r--   0 perry      (501) staff       (20)      312 2023-02-05 15:25:14.000000 crypto_licensing-3.3.0/requirements.txt
--rw-rw-r--   0 perry      (501) staff       (20)       38 2023-02-21 16:53:47.467853 crypto_licensing-3.3.0/setup.cfg
--rw-rw-r--   0 perry      (501) staff       (20)     3157 2023-02-21 16:32:39.000000 crypto_licensing-3.3.0/setup.py
+drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-07-23 20:36:47.788294 crypto_licensing-3.3.1/
+-rw-rw-r--   0 perry      (501) staff       (20)    35147 2022-01-25 19:29:48.000000 crypto_licensing-3.3.1/COPYING
+-rw-rw-r--   0 perry      (501) staff       (20)     1184 2023-02-05 15:25:14.000000 crypto_licensing-3.3.1/LICENSE
+-rw-rw-r--   0 perry      (501) staff       (20)      138 2022-02-23 17:37:17.000000 crypto_licensing-3.3.1/MANIFEST.in
+-rw-rw-r--   0 perry      (501) staff       (20)     1392 2023-07-23 20:36:47.786661 crypto_licensing-3.3.1/PKG-INFO
+-rw-rw-r--   0 perry      (501) staff       (20)     4468 2023-02-05 15:25:14.000000 crypto_licensing-3.3.1/README.org
+-rw-rw-r--   0 perry      (501) staff       (20)     7177 2023-02-05 15:25:14.000000 crypto_licensing-3.3.1/README.txt
+drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-07-23 20:36:47.644706 crypto_licensing-3.3.1/crypto_licensing/
+-rw-rw-r--   0 perry      (501) staff       (20)     1364 2023-07-23 20:36:37.000000 crypto_licensing-3.3.1/crypto_licensing/__init__.py
+-rw-rw-r--   0 perry      (501) staff       (20)     1365 2023-02-14 14:41:09.000000 crypto_licensing-3.3.1/crypto_licensing/__main__.py
+-rw-rw-r--   0 perry      (501) staff       (20)    10632 2023-02-16 18:04:11.000000 crypto_licensing-3.3.1/crypto_licensing/cli.py
+-rw-rw-r--   0 perry      (501) staff       (20)     3993 2023-02-15 19:50:25.000000 crypto_licensing-3.3.1/crypto_licensing/cli_test.py
+-rw-rw-r--   0 perry      (501) staff       (20)     5264 2023-02-05 15:25:14.000000 crypto_licensing-3.3.1/crypto_licensing/crypto_test.py
+drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-07-23 20:36:47.645445 crypto_licensing-3.3.1/crypto_licensing/ed25519/
+-rw-rw-r--   0 perry      (501) staff       (20)     1655 2023-02-14 14:07:01.000000 crypto_licensing-3.3.1/crypto_licensing/ed25519/__init__.py
+-rw-rw-r--   0 perry      (501) staff       (20)     5033 2022-01-24 17:18:08.000000 crypto_licensing-3.3.1/crypto_licensing/ed25519_djb.py
+drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-07-23 20:36:47.648413 crypto_licensing-3.3.1/crypto_licensing/ed25519ll_pyonly/
+-rw-rw-r--   0 perry      (501) staff       (20)     2319 2023-02-05 15:25:14.000000 crypto_licensing-3.3.1/crypto_licensing/ed25519ll_pyonly/__init__.py
+-rw-rw-r--   0 perry      (501) staff       (20)     6905 2022-01-19 19:14:43.000000 crypto_licensing-3.3.1/crypto_licensing/ed25519ll_pyonly/djbec.py
+drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-07-23 20:36:47.721283 crypto_licensing-3.3.1/crypto_licensing/licensing/
+-rw-rw-r--   0 perry      (501) staff       (20)     1606 2023-02-21 15:58:27.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/__init__.py
+-rw-rw-r--   0 perry      (501) staff       (20)     1196 2023-02-14 14:07:40.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/__main__.py
+-rw-rw-r--   0 perry      (501) staff       (20)     1942 2023-02-05 15:25:14.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/bitquery_test.py
+-rw-rw-r--   0 perry      (501) staff       (20)     2194 2023-02-14 14:08:13.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/defaults.py
+drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-07-23 20:36:47.726796 crypto_licensing-3.3.1/crypto_licensing/licensing/doh/
+-rw-rw-r--   0 perry      (501) staff       (20)     4511 2023-02-14 14:08:34.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/doh/__init__.py
+-rw-rw-r--   0 perry      (501) staff       (20)     1362 2023-02-14 14:15:34.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/doh/__main__.py
+-rw-rw-r--   0 perry      (501) staff       (20)     2731 2023-02-14 14:16:10.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/doh/cli.py
+-rw-rw-r--   0 perry      (501) staff       (20)     3015 2023-07-21 15:44:18.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/doh_test.py
+-rw-rw-r--   0 perry      (501) staff       (20)    17971 2023-02-05 15:25:14.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/grant_test.py
+-rw-rw-r--   0 perry      (501) staff       (20)     7469 2023-02-05 15:25:14.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/licensing_test.py
+-rw-rw-r--   0 perry      (501) staff       (20)    96445 2023-02-14 14:08:47.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/main.py
+-rw-rw-r--   0 perry      (501) staff       (20)   155417 2023-07-22 14:39:37.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/verification.py
+-rw-rw-r--   0 perry      (501) staff       (20)    41145 2023-02-23 18:12:32.000000 crypto_licensing-3.3.1/crypto_licensing/licensing/verification_test.py
+-rw-rw-r--   0 perry      (501) staff       (20)    43488 2023-07-21 15:31:55.000000 crypto_licensing-3.3.1/crypto_licensing/misc.py
+-rw-rw-r--   0 perry      (501) staff       (20)     9528 2023-02-05 15:25:17.000000 crypto_licensing-3.3.1/crypto_licensing/misc_test.py
+-rw-rw-r--   0 perry      (501) staff       (20)       88 2023-07-22 14:28:52.000000 crypto_licensing-3.3.1/crypto_licensing/version.py
+drwxrwxr-x   0 perry      (501) staff       (20)        0 2023-07-23 20:36:47.783584 crypto_licensing-3.3.1/crypto_licensing.egg-info/
+-rw-rw-r--   0 perry      (501) staff       (20)     1392 2023-07-23 20:36:47.000000 crypto_licensing-3.3.1/crypto_licensing.egg-info/PKG-INFO
+-rw-rw-r--   0 perry      (501) staff       (20)     1331 2023-07-23 20:36:47.000000 crypto_licensing-3.3.1/crypto_licensing.egg-info/SOURCES.txt
+-rw-rw-r--   0 perry      (501) staff       (20)        1 2023-07-23 20:36:47.000000 crypto_licensing-3.3.1/crypto_licensing.egg-info/dependency_links.txt
+-rw-rw-r--   0 perry      (501) staff       (20)       74 2023-07-23 20:36:47.000000 crypto_licensing-3.3.1/crypto_licensing.egg-info/entry_points.txt
+-rw-rw-r--   0 perry      (501) staff       (20)      263 2023-07-23 20:36:47.000000 crypto_licensing-3.3.1/crypto_licensing.egg-info/requires.txt
+-rw-rw-r--   0 perry      (501) staff       (20)      134 2023-07-23 20:36:47.000000 crypto_licensing-3.3.1/crypto_licensing.egg-info/top_level.txt
+-rw-rw-r--   0 perry      (501) staff       (20)       48 2023-02-05 15:25:14.000000 crypto_licensing-3.3.1/requirements-dev.txt
+-rw-rw-r--   0 perry      (501) staff       (20)       21 2023-02-05 15:25:14.000000 crypto_licensing-3.3.1/requirements-tests.txt
+-rw-rw-r--   0 perry      (501) staff       (20)      312 2023-02-05 15:25:14.000000 crypto_licensing-3.3.1/requirements.txt
+-rw-rw-r--   0 perry      (501) staff       (20)       38 2023-07-23 20:36:47.788961 crypto_licensing-3.3.1/setup.cfg
+-rw-rw-r--   0 perry      (501) staff       (20)     3157 2023-02-21 16:32:39.000000 crypto_licensing-3.3.1/setup.py
```

### Comparing `crypto_licensing-3.3.0/COPYING` & `crypto_licensing-3.3.1/COPYING`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/LICENSE` & `crypto_licensing-3.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/PKG-INFO` & `crypto_licensing-3.3.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: crypto_licensing
-Version: 3.3.0
+Version: 3.3.1
 Summary: The crypto-licensing module implements Ed25519-signed license checking and automatic issuance after cryptocurrency payment
 Home-page: https://github.com/pjkundert/crypto-licensing
 Author: Perry Kundert
 Author-email: perry@dominionrnd.com
 License: Dual License; GPLv3 and Proprietary
 Project-URL: Bug Tracker, https://github.com/pjkundert/crypto-licensing/issues
 Keywords: licensing Bitcoin Ethereum cryptocurrency payments Ed25519 signatures
```

### Comparing `crypto_licensing-3.3.0/README.org` & `crypto_licensing-3.3.1/README.org`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/README.txt` & `crypto_licensing-3.3.1/README.txt`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/__init__.py` & `crypto_licensing-3.3.1/crypto_licensing/__init__.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/__main__.py` & `crypto_licensing-3.3.1/crypto_licensing/__main__.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/cli.py` & `crypto_licensing-3.3.1/crypto_licensing/cli.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/cli_test.py` & `crypto_licensing-3.3.1/crypto_licensing/cli_test.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/crypto_test.py` & `crypto_licensing-3.3.1/crypto_licensing/crypto_test.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/ed25519/__init__.py` & `crypto_licensing-3.3.1/crypto_licensing/ed25519/__init__.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/ed25519_djb.py` & `crypto_licensing-3.3.1/crypto_licensing/ed25519_djb.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/ed25519ll_pyonly/__init__.py` & `crypto_licensing-3.3.1/crypto_licensing/ed25519ll_pyonly/__init__.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/ed25519ll_pyonly/djbec.py` & `crypto_licensing-3.3.1/crypto_licensing/ed25519ll_pyonly/djbec.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/__init__.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/__init__.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/__main__.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/__main__.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/bitquery_test.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/bitquery_test.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/defaults.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/defaults.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/doh/__init__.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/doh/__init__.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/doh/__main__.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/doh/__main__.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/doh/cli.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/doh/cli.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/doh_test.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/doh_test.py`

 * *Files 9% similar despite different names*

```diff
@@ -68,13 +68,11 @@
 
     assert len( recs ) == 1
     assert recs[0].get( 'data' ) \
         == 'v=DKIM1; k=ed25519; p=5cijeUNWyR1mvbIJpqNmUJ6V4Od7vPEgVWOEjxiim8w='
 
     # Now ensure multi-record (long) TXT entries are properly handled.
     recs			= doh.query(
-        'default._domainkey.justicewall.com', 'TXT' )
+        "default._domainkey.xn----7hcbr.email", 'TXT' )
     print( json.dumps( recs ) )
     assert recs[0].get( 'data' ) \
-        == "v=DKIM1; k=rsa; p=MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA0PMv4yXqvYlPWxCt7ZjdfR9Q4GzkGhxIEqxFTQEsPF0GxpZPr54GTiMsvmWxsrJWCb9OFo5qx48lPnHu1Y/KZcx6"\
-        "xydZiNxYdGedcRZFtMAwQAKQgo2Iq28PamZf5D8BO1+rg9tlAo2vYKrp6Cf1zTxDqHzSVl85RA7PZj1Jb/7jpqujT1SRXngrerB4iYBtx" \
-        "aPXTN/aI+cvS8kREW7tYkb4nt2fK3sb2RtCe5hxGTOdtIie/stZj/w/5ozsrtEZ6CiGQA38IaVOFsGwAvmhucy08UzbycmXKYsJiWPpSyXBXSX+O+5WaqgOYvcGT9CHBBWoFJG37Qf4KHoQqhS7IwIDAQAB;"
+        == "v=DKIM1; k=rsa; p=MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEA7qXVANitIc6CXteBZ/iJaTkoxZvosIu9WxGLrO2C3x5WkdzYPzTGwwosdKczTGuSZct6RPrUcwR3Rkh2p+b2hq1cn8qqHWN2XPNqZKv3VIiy2Vfahu5cUqaI3WmOIFyR57s21xi8bnKkuKfCCgKPefr9qw4bsZggaythKCosyUGFq3CG4fovTsUKGXsG5JzNm" "K61IAWLA7fnNK8SGKwoj9uVVFN1ps+mINFpqLtFvM7TweT1dlx5AShD8lJ0Bt+7EUTLp/nRRbZXbW1iKViSqiyJP4+2D0fxj8DkLOos5KKzAq9BrHYD9DsF9c8qgApO1U0iF4KsnqXMIHPbjtycTQIDAQAB;"
```

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/grant_test.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/grant_test.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/licensing_test.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/licensing_test.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/main.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/main.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/verification.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/verification.py`

 * *Files 2% similar despite different names*

```diff
@@ -1661,17 +1661,24 @@
         constraints['dependencies'].  If no additional constraints are supplied, this will simply
         return the empty constraints dict on success.  The returned constraints would be usable in
         constructing a new License (assuming at least the necessary author, author_domain and
         product were defined).
 
         """
         if author_pubkey:
-            author_pubkey, _	= into_keys( author_pubkey )
+            author_pubkey,_	= into_keys( author_pubkey )
             assert author_pubkey, "Unrecognized author_pubkey provided"
 
+        # TODO: This identifies and allows *only* Licenses whose primary author matches the provided
+        # pubkey.  However -- a License from a different author, which *carries* dependency licenses
+        # (ie. has sub-licensed some License that carries Grants matching the desired author!) is
+        # also something we want to allow!  In other words -- if I'm looking for a Grant from a
+        # certain author, I might be interested in *any* License that is available that carries such
+        # a Grant.  So, if some License from some author is A) sub-licenseable by me, and B) carries
+        # a Grant from the desired author, than verify it!
         if author_pubkey and author_pubkey != self.author.pubkey:
             raise LicenseIncompatibility(
                 "License for {auth}'s {prod!r} public key mismatch: {lhs} != {rhs}{stack}".format(
                     auth	= self.author.name,
                     prod	= self.author.product,
                     lhs		= into_b64( author_pubkey ),
                     rhs		= str( self.author ) if log.isEnabledFor( logging.TRACE ) else into_b64( self.author.pubkey ),
@@ -1710,17 +1717,21 @@
         # verifying License dependencies, we don't supply the constraints and decline inclusion of
         # dependencies, because we're not interested in sub-Licensing these Licenses, only verifying
         # them.  If a License dependency specifies a client, make certain it matches the issued
         # License's author; otherwise, any author is allowed.
 
         # TODO: Issuing a License that allows "anonymous" clients is somewhat dangerous, as the
         # entire package of License capabilities can be acquired by anyone.  When we validate
-        # capabilities requested against those granted by a License, we must "stop", when we
+        # capabilities requested against those granted by a License, should we "stop", when we
         # encounter any anonymous License dependencies -- any capabilities they grant cannot be
-        # assumed to be "for" the licensee; the Agent authoring the present license.
+        # assumed to be "for" the licensee; the Agent authoring the present license?  I don't think
+        # so -- if some author issues "anonymous" License Grants for some capabilities, they must
+        # intend that these are safe/approved for any sub-licensee to acquire...  If they want to
+        # protect valuable Grants from widespread usage, then they would only issue them in Licenses
+        # with specific client restrictions.
         for prov_dct in self.dependencies or []:
             prov		= LicenseSigned( confirm=confirm, machine_id_path=machine_id_path, **prov_dct )
             try:
                 prov.verify( confirm=confirm, machine_id_path=machine_id_path )
                 assert prov.license.client is None or prov.license.client.pubkey is None or prov.license.client.pubkey == self.author.pubkey, \
                     "sub-License client public key {client_pubkey} doesn't match Licence author's public key {author_pubkey}".format(
                         client_pubkey	= into_b64( prov.license.client.pubkey ),
@@ -2485,23 +2496,25 @@
 ):
     """Verify that the supplied License or LicenseSigned contains a valid signature, and that the
     License follows the rules in all of its License dependencies.  Optionally, 'confirm' the
     validity of any public keys.
 
     Apply any additional constraints, returning a License serialization dict satisfying them.  If
     you plan to issue a new LicenseSigned, it is recommended to include your author, author_domain
-    and product names, and perhaps also the client and client_pubkey of the intended License
-    recipient.
+    and product names, and perhaps also the client and client_pubkey of any intended License
+    recipient (otherwise, any client may sub-license, so be careful to only grant capabilities
+    appropriate for many generic licensees).
 
     Works with either a License and signature= keyword parameter, or a LicenseSigned provenance.
 
-    Defaults to demand that any supplied LicenseSigned dependencies are included in the resultant
-    remaining constraints.  If None, by default (unlike the License{Signed}.verify), includes the
-    target LicenseSigned in the returned constraints required, so that a sub-License for the
-    verified License can be produced.
+    Defaults to demand that any supplied LicenseSigned 'dependencies' are included in the resultant
+    remaining constraints.  If it is None, by default (unlike the License{Signed}.verify, which is
+    intended for recursive verification, so doesn't alter constraints), this will include this
+    target LicenseSigned provenance in the returned constraints required, so that a sub-License for
+    the verified License can be produced.
 
     Therefore, when you have a LicenseSigned or a License + a signature, calling verify( <lic> ... )
     will return a requirements dict ready to pass to License, along with an author and (optionally)
     designated client Agent, with the target verified License itself in the dependencies list,
     producing a new License which sub-licenses the just verified License.
 
     """
@@ -2702,15 +2715,16 @@
     if not found:
         for f_name in issues:
             log.warning( "Cannot load Keypair(s) from {f_name}: {reasons}".format(
                 f_name=f_name, reasons=', '.join( "{}".format( exc ) for exc in issues[f_name] )))
 
 
 def key_lic_sequence_logger( func ):
-    """Logs a sequence of <Keypair>,<License>, including _from (if available)"""
+    """Logs a sequence of <Keypair>,<License>, including _from (if available).  Passes thru any
+    <generator>.send( payload ).  Supports either ed25519.Keypair, or Keypair{Plaintext,Encrypted}"""
     @wraps( func )
     def wrapper( *args, **kwds ):
         labelled		= False
         func_iter		= func( *args, **kwds )
         try:
             payload		= None
             while True:
@@ -2723,15 +2737,16 @@
                         ))
                         labelled	= True
                     log.log( level, "{:56} {:20.20} {:20.20} {:16.16}: {}{}".format(
                         'N/A' if not hasattr( lic, '_from' ) or not lic._from else os.path.basename( lic._from ),
                         'N/A' if not lic or not lic.license.client else "{}/{}".format( lic.license.client.name, into_b64( lic.license.client.pubkey )),
                         'N/A' if not lic else "{}/{}".format( lic.license.author.name, into_b64( lic.license.author.pubkey )),
                         'N/A' if not lic or not lic.license.author.product else lic.license.author.product,
-                        'N/A' if not key else into_b64( key.vk ), key._from if hasattr( key, '_from' ) else '',
+                        'N/A' if not key else into_b64( key.vk ),
+                        key._from if hasattr( key, '_from' ) else '',
                     ))
                 payload		= ( yield key,lic )
         except StopIteration:
             pass
     return wrapper
 
 
@@ -2740,14 +2755,15 @@
     extension_keypair	= None,
     extension_license	= None,
     username		= None,			# Keypair protected w/ supplied credentials
     password		= None,
     confirm		= None,
     machine_id_path	= None,
     constraints		= None,
+    keypairs		= None,			# Any additional ed25519.Keypairs we might need, to utilize Licenses
     **kwds  # eg. {base,file}name, package, extra=["..."], reverse_save, other open() args; see config_open
 ):
     """Load our agent key(s), check that License(s) have been (or can be) issued to our agent, for
     this machine and/or username, yielding a sequence of:
 
         (None,None)			- nothing, if no Keypair could be found w/ given credentials
         (<Keypair>,None,)		- if Keypair found, but no Licenses available
@@ -2762,25 +2778,46 @@
     - Load our Ed25519 Keypair
       - Create one, if not found
     - Load our Licenses
       - Obtain one, if not found
 
     If an Ed25519 Agent signing authority Keypair or License must be created, the default location
     where they should be stored is in the most general configuration path location that is writable.
+    We don't do that here; the caller should create one, as appropriate, and either save it (so we
+    find it with load_keypairs on a subsequent call), or pass it in via keypairs.  We will load all
+    available Keypairs/Licenses, and attempt to return any Licenses that are verified for any
+    Keypair (ie. were issued by the Keypair, or could be sub-licensed by the Keypair, which we will
+    do automatically, so the Licensee doesn't actually need to save their signed LicenseProvenance
+    -- unless they wish to avoid the need to be online and "confirm" the validity of the
+    sub-Licenses in the future; they can save the generated LicenseProvenance, and trust their
+    signature to prove that, in the past, they agreed that the sub-License(s) were verified).
 
     Agent signing authority is usually machine- or username-specific: a License to run a program on
     one machine and/or for one username usually doesn't transfer to another machine/username.
-
-        <basename>-<machine-id>.crypto-key...
-        <basename>-<machine-id>.crypto-lic...
+    However, you can arrange for a License to have a certain client Agent Keypair, and issue a
+    License for a certain Machine ID.  Later, when the client restores from backups onto a new
+    machine, the License will fail to validate (b/c new Machine ID).
+
+    However, if the issued License is specific to the client's Keypair (or the License doesn't
+    specify a client public key at all), they can load their Keypair (by entering credentials), and
+    re-sub-license their License for the new machine.  Thus, we'll automatically do this here, w/
+    proper username/password, and return the newly sub-licensed LicenseProvenance.
+
+    We assume that any Keypair we can load (ie. we have the username/password to access) must imply
+    a signing authority.  So, don't keep generic license keypairs (ie. those used to author
+    licenses, or sub-license master Licenses to clients) n the same directories (or with the same
+    credentials) as those used for end-user client agents.  Otherwise, this will pick them up and
+    use them to create sub-licenses!
 
     """
+    # Any supplied authoring ed25519.Keypairs are of unknown paths
+    keypairs			= [ (None,key) for key in keypairs or [] ]
     # Load any Keypair{Plaintext,Encrypted} available, and convert to a ed25519.Keypair,
     # ready for signing/verification.  Retains orders of load_keypairs / load.
-    keypairs			= list(
+    keypairs		       += list(
         (key_path, keypair_or_error)
         for key_path, keypair_typed, cred, keypair_or_error in load_keypairs(
             username	= username,
             password	= password,
             mode	= mode,
             extension	= extension_keypair,
             every	= True,
@@ -2799,44 +2836,51 @@
     ))
 
     # See if license(s) has been (or can be) issued to our Agent keypair(s) (ie. was issued to this
     # keypair as a specific client_pubkey or was non-client-specific, and then was signed by our
     # Keypair), for this Machine ID.
     matches			= 0
     key_seen			= set()  # of Ed25519.Keypair.vk.  No keys loaded --> yield None,None
-    for key_path,keypair in keypairs:
+    for key_path,keypair in keypairs:    # key_path may be None for any authoring Keypairs provided
         if keypair.vk in key_seen:
             log.debug( "Ignoring redundant keypair {pubkey} from {path}".format(
                 pubkey	= into_b64( keypair.vk ),
                 path	= key_path,
             ))
             continue
         key_seen.add( keypair.vk )
-
+        log.info( "Checking keypair {key_path:32} ({pubkey})...".format(
+            key_path	= os.path.basename( key_path or '(unknown)' ),
+            pubkey	= into_b64( keypair.vk ),
+        ))
         # For each unique Keypair, discover any LicenceSigned we've been issued, or can issue.
         lic_path,lic		= None,None	 # If no Licensese found, at all
         prov,reasons		= None,[]        # Why didn't any Licenses qualify?
         for lic_path,lic in licenses:
             # Was this license issued by our Keypair Agent as the author?  This means that one was
-            # issued by some author, with our Keypair Agent as a client, and we (previously) issued
-            # and saved it.
+            # issued by some author, with our Keypair Agent as a client (or no client spcecified),
+            # and we (previously) issued and saved it -- we sub-licensed it.
             log.trace( "Evaluate {lic_path:32} / {key_path:32} w/ constrints {constraints!r}".format(
-                lic_path=os.path.basename( lic_path ), key_path=os.path.basename( key_path ), constraints=constraints ))
+                lic_path	= os.path.basename( lic_path ),
+                key_path	= os.path.basename( key_path or '(unknown)' ),
+                constraints	= constraints ))
             try:
                 lic.verify(
                     author_pubkey	= keypair.vk,
                     confirm		= confirm,
                     machine_id_path	= machine_id_path,
                     dependencies	= False,
                     **( constraints or {} )
                 )
             except Exception as exc:
-                log.info( "Checked  {lic_path:32} / {key_path:32}: {exc}".format(
-                    lic_path=os.path.basename( lic_path ), key_path=os.path.basename( key_path ),
-                    exc=''.join( traceback.format_exception( *sys.exc_info() )) if log.isEnabledFor( logging.TRACE ) else exc ))
+                log.info( "Checked  {lic_path:32} / {key_path:32} ({pubkey:64}): {exc}".format(
+                    lic_path	= os.path.basename( lic_path ),
+                    key_path	= os.path.basename( key_path or '(unknown)' ),
+                    pubkey	= into_b64( keypair.vk ),
+                    exc		= ''.join( traceback.format_exception( *sys.exc_info() )) if log.isEnabledFor( logging.TRACE ) else exc ))
                 reasons.append( str( exc ))
             else:
                 # This license passed muster w/ the constraints supplied and it was already issued
                 # to us; we're done.
                 matches	       += 1
                 yield keypair,lic
                 continue
@@ -2848,26 +2892,28 @@
                 requirements	= lic.verify(
                     confirm		= confirm,
                     machine_id_path	= machine_id_path,
                     dependencies	= True,
                     **( constraints or {} )
                 )
             except Exception as exc:
-                log.info( "Verify  {lic_path:32} / {key_path:32}: {exc}".format(
-                    lic_path=os.path.basename( lic_path ), key_path=os.path.basename( key_path ),
-                    exc=''.join( traceback.format_exception( *sys.exc_info() )) if log.isEnabledFor( logging.TRACE ) else exc ))
+                log.info( "Verify  {lic_path:32} / {key_path:32} ({pubkey:64}): {exc}".format(
+                    lic_path	= os.path.basename( lic_path ),
+                    key_path	= os.path.basename( key_path or '(unknown)' ),
+                    pubkey	= into_b64( keypair.vk ),
+                    exc		= ''.join( traceback.format_exception( *sys.exc_info() )) if log.isEnabledFor( logging.TRACE ) else exc ))
                 continue
 
             # Validated this License is sub-Licensable by this Keypair Agent!  This License is
             # available to be issued to us and verified, now, as one of our License dependencies.
             # Craft a new License, w/ the requirements produced by the verify, above.  If the
             # LicenseSigned provenance can be issued, it has fully passed verification.  We are
-            # assuming that the License is sub-licensable by this agent's Keypair as the client; if
-            # the License allows anonymous clients (no lic.license.client specified), then make an
-            # ad-hoc Agent record.
+            # assuming that the License is sub-licensable (is author-able) by this agent's Keypair
+            # as the client; if the License allows anonymous clients (no lic.license.client
+            # specified), then make an ad-hoc Agent record.
             log.info( "Require {requirements!r}".format( requirements=requirements ))
             try:
                 author		= lic.license.client
                 if not author:
                     pubkey	= into_b64( keypair.vk )
                     author	= Agent( name=pubkey, pubkey=pubkey )
                 prov		= issue(
@@ -2878,33 +2924,37 @@
                         **requirements
                     ),
                     author_sigkey	= keypair.sk,
                     confirm		= confirm,
                     machine_id_path	= machine_id_path,
                 )
             except Exception as exc:
-                log.info( "Issuing {lic_path:32} / {key_path:32} failure: {exc}".format(
-                    lic_path=os.path.basename( lic_path ), key_path=os.path.basename( key_path ),
-                    exc=''.join( traceback.format_exception( *sys.exc_info() )) if log.isEnabledFor( logging.TRACE ) else exc ))
+                log.info( "Issuing {lic_path:32} / {key_path:32} ({pubkey:64}) failure: {exc}".format(
+                    lic_path	= os.path.basename( lic_path ),
+                    key_path	= os.path.basename( key_path or '(unknown)' ),
+                    pubkey	= into_b64( keypair.vk ),
+                    exc		= ''.join( traceback.format_exception( *sys.exc_info() )) if log.isEnabledFor( logging.TRACE ) else exc ))
                 continue
             else:
                 # The License was available to be issued as one of our dependencies, and passed
                 # remaining constraints requirements; Use prov; prov_path remains None.
                 matches	       += 1
                 yield (keypair,prov)		# Reports <Keypair>,<LicenseSigned>
         else:
             if not licenses:
                 yield (keypair,None)		# Reports <Keypair>,None
     else:
         if not key_seen:
             yield (None,None)			# Or None,None if no <Keypair>(s) at all (bad credentials?)
 
     log.debug( "Observed {keys} unique keys: {pubkeys}, {lics} licenses, finding {matches} possible Licenses".format(
-        keys = len( key_seen ), pubkeys=', '.join( into_b64( k ) for k in sorted( key_seen )),
-        lics = len( licenses ), matches = matches,
+        keys	= len( key_seen ),
+        pubkeys	= ', '.join( into_b64( k ) for k in sorted( key_seen )),
+        lics	= len( licenses ),
+        matches	= matches,
     ))
 
 
 check			= key_lic_sequence_logger( check_nolog )
 
 
 @key_lic_sequence_logger
@@ -2912,20 +2962,29 @@
     author,					# Details of the author's product we're licensing
     client		= None,			# ..and the intended specific client Agent
     username		= None,			# The credentials for our client Agent's Keypair
     password		= None,
     confirm		= None,
     machine_id_path	= None,
     constraints		= None,			# The additional constraints required of the author's license (if any)
+    keypairs		= None,			# Any additional ed25519.Keypairs we might need, to utilize Licenses
     registering		= None,			# Default (to True) if necessary, create a new Keypair (register a new License client)
     acquiring		= None,			# Default (to True) if necessary, obtain/create a new License
     reverse_save	= None,
+    basename		= None,			# A specific basename to use; otherwise client/author.servicekey
     **kwds  # eg. {base,file}name, package, extra=["..."], reverse_save, other open() args; see config_open
 ):
-    """If possible, load and verify the agent's KeyPair (creating one if necessary).
+    """If possible, load and verify the client Agent's KeyPair (creating one if necessary).  Looks
+    first for Keypairs/Licenses under the specified basename; defaults to client.servicekey, and
+    then looks in author.servicekey.  Any Keypairs collected are used in subsequent searches, to see
+    if a License issued by the author or to the client can be refined and issued on behalf of the
+    named agent.
+
+    All Keypairs found are assumed to be client Agent keypairs useful for issuing sub-licenses: So,
+    don't store author Agent keypairs in the same directories, or using the same credentials!
 
     Obtain any LicenseSigned provenances, and sift through them for any that authorize usage of the
     given author's domain and product, to the given client, for a certain space and time, and
     satisfying any constraints.
 
     If the period of authorization has expired, confirm with a license server that the LicenseSigned
     provenance is still valid (hasn't been revoked, eg. for reasons of license fraud, such as
@@ -2943,86 +3002,147 @@
     4) The License contains the required capabilities
        - and were issued by the expected Author
 
     then the requested capability is authorized.
 
     Otherwise, use the agent's Keypair to obtain a License for the specified remaining capability/constraints.
 
-    Yields the discovered sequence of KeyPair, License found.
+    Yields the discovered sequence of KeyPair, License found, or if none found under any name,
+    finally yields:
+
         - (None, None): No Keypair found
 
+    Any new Keypair/License created/acquired will be save in basename or client.servicekey (or by
+    package/filename if neither are supplied).
+
     """
     if registering is None:
         registering		= True
     if acquiring is None:
         acquiring		= True
 
     class State( Enum ):
         INITIAL		= 0
         CHECKING	= 1
         REGISTERING	= 2
         LICENSING	= 3
         DONE		= 4
 
+    # We'll search for Keypairs and Licenses first under any basename supplied, then
+    # client.servicekey, then author.servicekey.  This allows us to eg. save an author's License
+    # somewhere, and then (later) load and sub-license it (if possible) on behalf of one or more
+    # client Agents.  All Keypairs required to utilize a certain License must be typically found
+    # under the same basename; however, we'll collect up all Keypairs found (eg. first under
+    # basename, then client.servicekey, ...) for each subsequent License check... call.  Thus, we
+    # can same a specific application agent Keypair (eg. under basename="some-application"), then
+    # find a License we saved under eg. "our-company" Agent, or (if not found), we can locate a
+    # generic "authors-product" License which is sublicensable using our
+    # some-application.crypto-keypair.
+
     credentials_seen		= { (username,password) }
-    licenses			= dict()        # Remember all Keypair... --> [ License, ... ] under current credentials
+    # Remember all Keypair... --> [ License, ... ] under current credentials, incl. any supplied in 'keypairs'
+    licenses			= { k: [] for k in keypairs or [] }
     state			= State.INITIAL
+    basechecks			= None		# Triggers re-computation of all basenames to check (ie. after REGISTERING)
     while state is not State.DONE:
         state			= State( state.value + 1 )
         log.detail( "{state}".format( state=state ))
         if state is State.CHECKING:
             # Look for Agent Keypairs and any associated Licenses issued to it, filtered by the
-            # Author we're looking for.  We want to keep CHECKING, again and again, while the
-            # caller provides new credentials.
+            # Author we're looking for a License from.  We want to keep CHECKING, again and again,
+            # while the caller provides new credentials, in case new Keypairs become available.
+            if basechecks is None:
+                basechecks	= [ basename ] if basename else []
+                if client and client.servicekey and client.servicekey not in basechecks:
+                    basechecks	= [ client.servicekey ] + basechecks  # then client...
+                if author and author.servicekey and author.servicekey not in basechecks:
+                    basechecks	= [ author.servicekey ] + basechecks  # then author...
+            log.detail( "{state} for Keypairs/Licenses w/ {keys} Keypairs, basename {base} (of {checks})".format(
+                state=state, keys=len( licenses ), base=basechecks[-1] if basechecks else None, checks=', '.join( map( str, basechecks )),
+            ))
+
+            # Check for Licenses available under one basename, given any ed25519.Keypairs collected
+            # thus far, or found under this basename.  This will yield None,None if none found, but
+            # we don't want to re-yield that until all hope is gone...
+            basenow		= basechecks.pop() if basechecks else None  # Iff no basename or author/client.servicekey
+            keypairs		= list( licenses.keys() )  # Use all previous discovered ed25519.Keypairs
             for key,lic in check_nolog(
                 username	= username,
                 password	= password,
                 confirm		= confirm,
                 constraints	= constraints,
                 machine_id_path	= machine_id_path,
+                basename	= basenow,
+                keypairs	= keypairs,
                 **kwds
             ):
+                log.info( "{state} Checking w/ basename {base} & {keys} prior keypairs: key: {key} w/ lic: {lic}".format(
+                    state=state, base=basenow, keys=len( keypairs), key=into_b64( key.vk if key else key ), lic=lic ))
                 if key is None:
                     assert lic is None, \
                         "No Agent ID KeyPair; should not have found a License {}".format( lic )
                     # No KeyPair, and no new credentials provided.  Give them the opportunity to
                     # enter new Credentials by falling to end of loop; if none provided, then assume
                     # they want to go through the proceess; advance to REGISTERING.
-                    log.detail( "No Agent, no License(s) found -- enter different credentials?" )
-                    pass
+                    log.detail( "No Agent, no License(s) found for {base} -- enter different credentials?".format(
+                        base	= basename
+                    ))
+                    if basechecks:
+                        # There remain further basenames to examine for potential Licenses; avoid
+                        # emitting None,None 'til they've been exhausted!
+                        log.detail( "{state} no more Keypairs/Licenses w/ basename {base}; trying next)".format(
+                            state=state, base=basenow
+                        ))
+                        break  # still some basenames to check; don't yield None,None yet, avoid check's else: clause
                 elif lic is None:
                     # An Agent ID KeyPair, but no License found available under some Keypair (and no
                     # new credentials supplied).  This is our moment to issue a new License;
                     # continues in state after REGISTERING (as if we've just completed REGISTERING).
                     licenses.setdefault( key, [] )
-                    log.detail( "Agent {agent}; No License(s) found -- enter different credentials?".format(
-                        agent	= into_b64( key.vk )))
-                    pass
+                    log.detail( "{state} Agent {agent}; but no License(s) found for {base} -- enter different credentials?".format(
+                        state	= state,
+                        agent	= into_b64( key.vk ),
+                        base	= basename,
+                    ))
+                    pass  # A keypair, but no License; yield
                 else:
                     # A candidate License!  See if it's what we're looking for.  This is probably a
                     # sub-License signed by this Agent containing a chain of LicenseSigned
                     # dependencies back to a License authored by the required authoring Agent, for
-                    # the product we're looking for.  We can look at the grants to see if one in
-                    # there contains a Grant._from the required authoring Agent, eg. "cpppo-test":
-                    # Grant(..., _from=<LicenseSigned>)
+                    # the product we're looking for.  We look at the grants to see if one in there
+                    # contains a Grant._from the required authoring Agent, eg. "cpppo-test":
+                    # Grant(..., _from=<LicenseSigned>); TODO: check... won't verify any License
+                    # that isn't issued (or issuable) explicitly to one of its keypairs; Hmmm.  It
+                    # *will* emit any License that is issuable to one of our Keypairs, which may
+                    # carry a sub-licensed grant from our target author.  So, this may be sufficient
+                    # to catch all available licenses that *could* carry a sub-licensed Grant we're
+                    # interested in.  We can't use any License (w/ sub-licenses) *unless* they are
+                    # issuable to one of our Keypairs, anyway.
                     licenses.setdefault( key, [] )
-                    log.detail( "Agent {agent}; License for {auth}'s {prod!r} found {lic}".format(
+                    log.detail( "{state} Agent {agent}; License found for {auth}'s {prod!r}{lic}".format(
+                        state	= state,
                         agent	= into_b64( key.vk ),
                         auth	= lic.license.author.name,
                         prod	= lic.license.author.product,
                         lic	= str( lic ) if log.isEnabledFor( logging.DEBUG ) else ""
                     ))
+                    # BUG: We should be checking that the License is issued to the *client* agent,
+                    # or not checking at all?  The authorized API will return every License issued
+                    # (possibly just now!) to any one of our Keypairs.  This is all we care about --
+                    # that we were able to acquire the License.  If it carries no Grants from our
+                    # desired author, that's all we care about verifying here?
                     if ( author is not None
                          and author != lic.license.author  # See Agent.__equal__; pubkey or 2/4 identifying attributes
                          and not any(
                              hasattr( v, '_from' ) and isinstance( v._from, Agent ) and author == v._from
                              for k,v in lic.license.grants().vars() )):
                         # This LicenseSigned not authored directly by the requested authoring Agent;
                         # nor does it *deliver* some Grant from the requested author.  Reject.
-                        log.info( "Agent {agent}; License for {auth}'s {prod!r} doesn't grant capabilities{extra}".format(
+                        log.info( "{state} Agent {agent}; License for {auth}'s {prod!r} doesn't grant capabilities{extra}".format(
+                            state	= state,
                             agent	= into_b64( key.vk ),
                             auth	= lic.license.author.name,
                             prod	= lic.license.author.product,
                             extra	= " (author {} not in grants {})".format(
                                 author.serialize( encoding=None ),
                                 ', '.join( map( repr, (
                                     v._from if ( hasattr( v, '_from' ) and isinstance( v._from, Agent )) else k
@@ -3034,57 +3154,89 @@
                     log.normal( "License for {auth_lic}'s {prod_lic!r} does grant capabilities for {auth}'s {prod}{stack}".format(
                         auth_lic	= lic.license.author.name,
                         prod_lic	= lic.license.author.product,
                         auth		= author.name,
                         prod		= author.product,
                         stack		= ''.join( traceback.format_stack() if log.isEnabledFor( logging.TRACE ) else [] ),
                     ))
+                    # This License passed muster; either authored by 
                     licenses[key].append( lic )
 
-                # Otherwise, we've found at least one passable license (or <key>,None or None,None).
-                # Keep yielding them 'til the caller finds one that satisfies their requirements --
-                # they might have purchased multiple licenses, and could be accumulating their
-                # grants.  If we're back here, they haven't (yet) found one; yield the next
-                # (collecting any .send( (username,password) )
+                # Otherwise, we've found at least one passable license (or <key>,None or None,None
+                # and no more basenames to check).  Keep yielding them 'til the caller finds one
+                # that satisfies their requirements -- or, they might have purchased multiple licenses,
+                # and could be accumulating their grants.  If we're back here, they haven't (yet)
+                # found one; yield the next (collecting any .send( (username,password) )
+                log.detail( "{state} Authorize key: {key}, lic: {lic}".format( state=state, key=KeypairPlaintext( key ), lic=lic ))
                 credentials		= ( yield key,lic )
                 if credentials and credentials not in credentials_seen:
                     # The caller supplied new credentials via .send( (username,password) ).  Restart
-                    # the License authorization process using the new credentials, IFF they are
-                    # different from previously seen credentials.  (We do this test here (not at the
-                    # start of the loop), to catch the case where only None,None is yielded from
-                    # check).
-                    licenses		= dict()
+                    # the License authorization process using the new credentials (but retain prior
+                    # Keypairs/Licenses), IFF they are different from previously seen credentials.
+                    # (We do this test here (not at the start of the loop), to catch the case where
+                    # only None,None is yielded from check).
                     username,password	= credentials
                     credentials_seen.add( credentials )
+                    basechecks		= None  # Reset w/ new credentials; re-scan all basenames
                     state		= State.INITIAL
-                    break
+                    continue
             else:
-                # Out of licenses; none satisfactory, but if we do have an Agent ID, continue as if we've
-                # just completed REGISTER, and proceed to LICENSE.  Otherwise, fall thru to REGISTERING.
-                if licenses:
-                    state	= State.REGISTERING
+                # Out of keypairs/licenses under this basename (and no more basechecks, b/c the last
+                # thing we'd get from authorized would be (None,None), and we'd have broken out
+                # above if there were more).  So, if  no Licenses collected are satisfactory , but if we
+                # do have at least one Agent ID, continue as if we've just completed REGISTER, and
+                # proceed to LICENSE.  Otherwise, fall thru to REGISTERING (unless we've got more
+                # basenames to try; then loop back.)
+                log.info( "{state} Checking w/ basename {base} finished w/ {keys} known Keypairs, {lics} Licenses".format(
+                    state=state, base=basenow, keys=len( licenses ), lics=len( sum( licenses.values(), [] ))))
+            # At the end of check... loop, no acceptable Licenses found (or still collecting).  If
+            # any more basenames available, lets try them (inheriting all ed25519.Keypairs found).
+            if basechecks:
+                log.info( "{state} Checking w/ basenames {bases} restarts w/ {keys} known Keypairs, {lics} Licenses".format(
+                    state=state, bases=', '.join( basechecks ), keys=len( licenses ), lics=len( sum( licenses.values(), [] ))))
+                state		= State.INITIAL
+                continue
+            # No more basenames available, done CHECKING.  Did we find anything?  If not, we'll have to fall thru to REGISTERING
+            if licenses:
+                # OK, we found at least one keypair, so we dont' need to fall thru to REGISTERING.
+                # Did we find any Licenses?
+                if not any( l for l in licenses.values() ):
+                    # Keypair(s) found, but no Licenses.  Guess we have to try to get one...
+                    state	= State.REGISTERING  # continues on to LICENSING
+                    continue
+                # Success!  We found at least one Keypair, and at least one License was found/issued!
+                return
 
         elif state is State.REGISTERING:
-            # We mustn't have seen even one Keypair; should we try "registering" a new Keypair?  If
-            # None/'' is supplied for either credential, an unencrypted Keypair will be produced.
+            # We mustn't have seen even one Keypair available to sub-license an existing License;
+            # should we try "registering" a new Keypair?  If None/'' is supplied for either
+            # credential, an unencrypted Keypair will be produced.  Name defaults to basename or
+            # client.servicekey (if exists); if neither, then package/filename must be provided.
             if not registering:
                 raise NotRegistered( "No Keypair found; request registering one, or provide different credentials" )
+            savename		= basename or ( client and client.servicekey ),  # Remains None if basename/client are None
             key			= registered(
-                why		= "End-user Keypair",
+                why		= "{} Keypair".format( savename or "End-user" ),
                 username	= username,
                 password	= password,
                 registering	= True,
                 reverse_save	= reverse_save,
+                basename	= savename,
                 **kwds
             )
             log.detail( "{state}: {action} {key}".format(
                 state	= state,
                 action	= "Loaded " if key._from else "Created",
                 key	= key ))
-            licenses		= { key: [] }
+            # BUG: If we do issue a Keypair, here, we must go on to re-evaluate every available
+            # License in respect to the new Keypair; if there is a sub-licensable License w/o
+            # restrictions on the client keypair, we could obtain it.  Do we loop back to CHECKING
+            # (w/ a new client.keypair value), or carry on and do in it LICENSING?  We don't need to
+            # try to load more new Keypairs, so maybe carry on...
+            licenses		= { key.into_keypair( username=username, password=password ): [] }
 
         elif state is State.LICENSING:
             # We can end up here after yielding zero, one or more valid Licenses.  This is because
             # the caller is trying to accumulate all available Licenses, and can't know when no more
             # are available.  As they accumulate Licenses, looking for a certain accumulation of
             # License.grants(), the final remaining required Grant should be supplied.
             if acquiring and len( licenses ) != 1:
```

### Comparing `crypto_licensing-3.3.0/crypto_licensing/licensing/verification_test.py` & `crypto_licensing-3.3.1/crypto_licensing/licensing/verification_test.py`

 * *Files 0% similar despite different names*

```diff
@@ -402,14 +402,38 @@
             timespan	= Timespan( "2021-09-30 11:22:33 Canada/Mountain", "1y" ),
             confirm	= confirm,
         )
 
     # Obtain a signed Cpppo license for 2021-09-30 + 1y
     lic_prov = issue( lic, dominion_sigkey, confirm=confirm )
 
+    lic_prov_str = str( lic_prov )
+    print(lic_prov_str)
+    assert lic_prov.b64digest() == 'VR8vHPEOpm2d77/FM/23oUHus1NtBYiM4qSRudChyrQ='
+    assert lic_prov_str == """\
+{
+    "license":{
+        "author":{
+            "domain":"dominionrnd.com",
+            "name":"Dominion Research & Development Corp.",
+            "product":"Cpppo Test",
+            "pubkey":"qZERnjDZZTmnDNNJg90AcUJZ+LYKIWO9t0jz/AzwNsk="
+        },
+        "client":{
+            "name":"Awesome, Inc.",
+            "pubkey":"cyHOei+4c5X+D/niQWvDG5olR1qi4jddcPTDJv/UfrQ="
+        },
+        "timespan":{
+            "length":"1y",
+            "start":"2021-09-30 17:22:33 UTC"
+        }
+    },
+    "signature":"tr2OcE1pT0tg7i+rotQJmFG8dIf8GhLtmBYxYDIshIRGKkmvAbCpuDgBKg8V0xUyaqh7OCCvlKRvvyqOEbD5DQ=="
+}"""
+
     # Create a signing key for Awesome, Inc.; securely hide it (or, print it for everyone to see,
     # just below! ;), and publish the base-64 encoded public key as a TXT RR at:
     #
     #     ethernet-ip-tool.crypto-licensing._domainkey.awesome.com 300 IN TXT \
     #        "v=DKIM1; k=ed25519; p=PW847szICqnQBzbdr5TAoGO26RwGxG95e3Vd/M+/GZc="
     #
     enduser_keypair		= authoring( seed=enduser_seed, why="from enduser seed" )
```

### Comparing `crypto_licensing-3.3.0/crypto_licensing/misc.py` & `crypto_licensing-3.3.1/crypto_licensing/misc.py`

 * *Files 1% similar despite different names*

```diff
@@ -979,23 +979,25 @@
                 pass
             else:
                 log.info( "config_open opened {fn!r} in mode {mode!r}".format(
                     fn=f.name, mode=mode ))
                 yield f
 
 
-def deduce_name( basename=None, extension=None, filename=None, package=None ):
+def deduce_name( basename=None, extension=None, filename=None, package=None, default=None ):
     """If no basename, use filename  .../<basename>.py, or package <basename>.submodule.
 
     An absolute path 'basename' will remain unchanged.  If no extension is present, the supplied
     'extension' will be appended.
 
     """
-    assert basename or ( filename or package ), \
-        "Cannot deduce basename without either filename (__file__) or package (__package__)"
+    if not ( basename or ( filename or package )):
+        assert default, \
+            "Cannot deduce basename without either filename (__file__) or package (__package__), or default"
+        return default
     if basename is None:
         if filename:
             basename		= os.path.basename( filename )		# eg. '/a/b/c/d.py' --> 'd.py'
             basename,_		= os.path.splitext( basename )		# up to last '.' in filename (the extension)
         else:
             basename		= package
             if '.' in basename:
```

### Comparing `crypto_licensing-3.3.0/crypto_licensing/misc_test.py` & `crypto_licensing-3.3.1/crypto_licensing/misc_test.py`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/crypto_licensing.egg-info/PKG-INFO` & `crypto_licensing-3.3.1/crypto_licensing.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: crypto-licensing
-Version: 3.3.0
+Version: 3.3.1
 Summary: The crypto-licensing module implements Ed25519-signed license checking and automatic issuance after cryptocurrency payment
 Home-page: https://github.com/pjkundert/crypto-licensing
 Author: Perry Kundert
 Author-email: perry@dominionrnd.com
 License: Dual License; GPLv3 and Proprietary
 Project-URL: Bug Tracker, https://github.com/pjkundert/crypto-licensing/issues
 Keywords: licensing Bitcoin Ethereum cryptocurrency payments Ed25519 signatures
```

### Comparing `crypto_licensing-3.3.0/crypto_licensing.egg-info/SOURCES.txt` & `crypto_licensing-3.3.1/crypto_licensing.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `crypto_licensing-3.3.0/setup.py` & `crypto_licensing-3.3.1/setup.py`

 * *Files identical despite different names*

