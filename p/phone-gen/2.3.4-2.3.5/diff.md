# Comparing `tmp/phone_gen-2.3.4.tar.gz` & `tmp/phone_gen-2.3.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "phone_gen-2.3.4.tar", last modified: Mon Jul 10 09:33:40 2023, max compression
+gzip compressed data, was "phone_gen-2.3.5.tar", last modified: Sun Jul 23 14:53:33 2023, max compression
```

## Comparing `phone_gen-2.3.4.tar` & `phone_gen-2.3.5.tar`

### file list

```diff
@@ -1,37 +1,37 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-10 09:33:40.444941 phone_gen-2.3.4/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-10 09:33:40.440941 phone_gen-2.3.4/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-10 09:33:40.440941 phone_gen-2.3.4/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     1096 2023-07-10 09:33:29.000000 phone_gen-2.3.4/.github/workflows/python-package.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1108 2023-07-10 09:33:29.000000 phone_gen-2.3.4/.github/workflows/python-publish.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1887 2023-07-10 09:33:29.000000 phone_gen-2.3.4/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1067 2023-07-10 09:33:29.000000 phone_gen-2.3.4/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     4778 2023-07-10 09:33:40.444941 phone_gen-2.3.4/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      353 2023-07-10 09:33:29.000000 phone_gen-2.3.4/Pipfile
--rw-r--r--   0 runner    (1001) docker     (123)     3612 2023-07-10 09:33:29.000000 phone_gen-2.3.4/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-10 09:33:40.440941 phone_gen-2.3.4/dev_tools/
--rw-r--r--   0 runner    (1001) docker     (123)     4859 2023-07-10 09:33:29.000000 phone_gen-2.3.4/dev_tools/patterns_generator.py
--rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-07-10 09:33:29.000000 phone_gen-2.3.4/dev_tools/update.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-10 09:33:40.440941 phone_gen-2.3.4/phone_gen/
--rw-r--r--   0 runner    (1001) docker     (123)     1030 2023-07-10 09:33:29.000000 phone_gen-2.3.4/phone_gen/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      160 2023-07-10 09:33:40.000000 phone_gen-2.3.4/phone_gen/__version__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10398 2023-07-10 09:33:29.000000 phone_gen-2.3.4/phone_gen/_generator.py
--rw-r--r--   0 runner    (1001) docker     (123)      562 2023-07-10 09:33:29.000000 phone_gen-2.3.4/phone_gen/alt_patterns.py
--rw-r--r--   0 runner    (1001) docker     (123)     1478 2023-07-10 09:33:29.000000 phone_gen-2.3.4/phone_gen/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)    16602 2023-07-10 09:33:29.000000 phone_gen-2.3.4/phone_gen/country_name.py
--rw-r--r--   0 runner    (1001) docker     (123)     6932 2023-07-10 09:33:29.000000 phone_gen-2.3.4/phone_gen/iso3.py
--rw-r--r--   0 runner    (1001) docker     (123)    87972 2023-07-10 09:33:29.000000 phone_gen-2.3.4/phone_gen/patterns.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-10 09:33:40.440941 phone_gen-2.3.4/phone_gen.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4778 2023-07-10 09:33:40.000000 phone_gen-2.3.4/phone_gen.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      666 2023-07-10 09:33:40.000000 phone_gen-2.3.4/phone_gen.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-10 09:33:40.000000 phone_gen-2.3.4/phone_gen.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       49 2023-07-10 09:33:40.000000 phone_gen-2.3.4/phone_gen.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-10 09:33:40.000000 phone_gen-2.3.4/phone_gen.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      125 2023-07-10 09:33:40.444941 phone_gen-2.3.4/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1713 2023-07-10 09:33:29.000000 phone_gen-2.3.4/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-10 09:33:40.444941 phone_gen-2.3.4/tests/
--rw-r--r--   0 runner    (1001) docker     (123)      108 2023-07-10 09:33:29.000000 phone_gen-2.3.4/tests/pytest.ini
--rw-r--r--   0 runner    (1001) docker     (123)      943 2023-07-10 09:33:29.000000 phone_gen-2.3.4/tests/test_alt_pattern.py
--rw-r--r--   0 runner    (1001) docker     (123)     2005 2023-07-10 09:33:29.000000 phone_gen-2.3.4/tests/test_cli.py
--rw-r--r--   0 runner    (1001) docker     (123)      956 2023-07-10 09:33:29.000000 phone_gen-2.3.4/tests/test_generator.py
--rw-r--r--   0 runner    (1001) docker     (123)     1080 2023-07-10 09:33:29.000000 phone_gen-2.3.4/tests/test_load_alt_patterns.py
--rw-r--r--   0 runner    (1001) docker     (123)     1792 2023-07-10 09:33:29.000000 phone_gen-2.3.4/tests/test_phone.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:53:33.276693 phone_gen-2.3.5/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:53:33.272693 phone_gen-2.3.5/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:53:33.276693 phone_gen-2.3.5/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     1096 2023-07-23 14:53:20.000000 phone_gen-2.3.5/.github/workflows/python-package.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1108 2023-07-23 14:53:20.000000 phone_gen-2.3.5/.github/workflows/python-publish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1887 2023-07-23 14:53:20.000000 phone_gen-2.3.5/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1067 2023-07-23 14:53:20.000000 phone_gen-2.3.5/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     4778 2023-07-23 14:53:33.276693 phone_gen-2.3.5/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      353 2023-07-23 14:53:20.000000 phone_gen-2.3.5/Pipfile
+-rw-r--r--   0 runner    (1001) docker     (123)     3612 2023-07-23 14:53:20.000000 phone_gen-2.3.5/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:53:33.276693 phone_gen-2.3.5/dev_tools/
+-rw-r--r--   0 runner    (1001) docker     (123)     4859 2023-07-23 14:53:20.000000 phone_gen-2.3.5/dev_tools/patterns_generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3871 2023-07-23 14:53:20.000000 phone_gen-2.3.5/dev_tools/update.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:53:33.276693 phone_gen-2.3.5/phone_gen/
+-rw-r--r--   0 runner    (1001) docker     (123)     1030 2023-07-23 14:53:20.000000 phone_gen-2.3.5/phone_gen/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-07-23 14:53:33.000000 phone_gen-2.3.5/phone_gen/__version__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10398 2023-07-23 14:53:20.000000 phone_gen-2.3.5/phone_gen/_generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)      562 2023-07-23 14:53:20.000000 phone_gen-2.3.5/phone_gen/alt_patterns.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1478 2023-07-23 14:53:20.000000 phone_gen-2.3.5/phone_gen/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16602 2023-07-23 14:53:20.000000 phone_gen-2.3.5/phone_gen/country_name.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6932 2023-07-23 14:53:20.000000 phone_gen-2.3.5/phone_gen/iso3.py
+-rw-r--r--   0 runner    (1001) docker     (123)    87940 2023-07-23 14:53:20.000000 phone_gen-2.3.5/phone_gen/patterns.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:53:33.276693 phone_gen-2.3.5/phone_gen.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4778 2023-07-23 14:53:33.000000 phone_gen-2.3.5/phone_gen.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      666 2023-07-23 14:53:33.000000 phone_gen-2.3.5/phone_gen.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 14:53:33.000000 phone_gen-2.3.5/phone_gen.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       49 2023-07-23 14:53:33.000000 phone_gen-2.3.5/phone_gen.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-23 14:53:33.000000 phone_gen-2.3.5/phone_gen.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      125 2023-07-23 14:53:33.276693 phone_gen-2.3.5/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1713 2023-07-23 14:53:20.000000 phone_gen-2.3.5/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:53:33.276693 phone_gen-2.3.5/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      108 2023-07-23 14:53:20.000000 phone_gen-2.3.5/tests/pytest.ini
+-rw-r--r--   0 runner    (1001) docker     (123)      943 2023-07-23 14:53:20.000000 phone_gen-2.3.5/tests/test_alt_pattern.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2005 2023-07-23 14:53:20.000000 phone_gen-2.3.5/tests/test_cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)      956 2023-07-23 14:53:20.000000 phone_gen-2.3.5/tests/test_generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1080 2023-07-23 14:53:20.000000 phone_gen-2.3.5/tests/test_load_alt_patterns.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1792 2023-07-23 14:53:20.000000 phone_gen-2.3.5/tests/test_phone.py
```

### Comparing `phone_gen-2.3.4/.github/workflows/python-package.yml` & `phone_gen-2.3.5/.github/workflows/python-package.yml`

 * *Files 1% similar despite different names*

```diff
@@ -21,15 +21,15 @@
       - name: Set up Python ${{ matrix.python-version }}
         uses: actions/setup-python@v2
         with:
           python-version: ${{ matrix.python-version }}
       - name: Install dependencies
         run: |
           python -m pip install --upgrade pip
-          python -m pip install flake8 pep8-naming pytest black pytest-cov phonenumbers==8.13.16
+          python -m pip install flake8 pep8-naming pytest black pytest-cov phonenumbers==8.13.17
           python -m pip install -e .
       - name: Flake8
         run: |
           flake8 phone_gen
       - name: Black
         run: |
           black --check phone_gen
```

### Comparing `phone_gen-2.3.4/.github/workflows/python-publish.yml` & `phone_gen-2.3.5/.github/workflows/python-publish.yml`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/.gitignore` & `phone_gen-2.3.5/.gitignore`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/LICENSE` & `phone_gen-2.3.5/LICENSE`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/PKG-INFO` & `phone_gen-2.3.5/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: phone_gen
-Version: 2.3.4
+Version: 2.3.5
 Summary: International phone number generation
 Home-page: https://github.com/tolstislon/phone-gen
 Author: tolstislon
 Author-email: tolstislon@gmail.com
 License: MIT License
 Keywords: testing,test-data,phone-number,phone,test-data-generator
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `phone_gen-2.3.4/README.md` & `phone_gen-2.3.5/README.md`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/dev_tools/patterns_generator.py` & `phone_gen-2.3.5/dev_tools/patterns_generator.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/dev_tools/update.py` & `phone_gen-2.3.5/dev_tools/update.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/phone_gen/__init__.py` & `phone_gen-2.3.5/phone_gen/__init__.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/phone_gen/_generator.py` & `phone_gen-2.3.5/phone_gen/_generator.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/phone_gen/alt_patterns.py` & `phone_gen-2.3.5/phone_gen/alt_patterns.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/phone_gen/cli.py` & `phone_gen-2.3.5/phone_gen/cli.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/phone_gen/country_name.py` & `phone_gen-2.3.5/phone_gen/country_name.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/phone_gen/iso3.py` & `phone_gen-2.3.5/phone_gen/iso3.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/phone_gen/patterns.py` & `phone_gen-2.3.5/phone_gen/patterns.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 # -*- coding: utf-8 -*-
 """
-Auto-generated file 2023-07-10 09:22:21 UTC
-Resource: https://github.com/google/libphonenumber v8.13.16
+Auto-generated file 2023-07-23 14:45:42 UTC
+Resource: https://github.com/google/libphonenumber v8.13.17
 """
 
 
 PATTERNS = {
-    "info": "libphonenumber v8.13.16",
+    "info": "libphonenumber v8.13.17",
     "data": {
         "AC": {
             "code": "247",
             "pattern": "((6[2-467][\\d]{3}))",
             "mobile": "((4[\\d]{4}))",
         },
         "AD": {
@@ -131,15 +131,15 @@
         "BJ": {
             "code": "229",
             "pattern": "((2(02)|(1[037])|(2[45])|(3[68])|(4[\\d])[\\d]{5}))",
             "mobile": "(((4[0-356])|([56][\\d])|(9[013-9])[\\d]{6}))",
         },
         "BL": {
             "code": "590",
-            "pattern": "((590(2[7-9])|(5[12])|(87)[\\d]{4}))",
+            "pattern": "((590(2[7-9])|(3[3-7])|(5[12])|(87)[\\d]{4}))",
             "mobile": "((69(0[\\d][\\d])|(1(2[2-9])|(3[0-5]))[\\d]{4}))",
         },
         "BM": {
             "code": "1",
             "pattern": "((441([46][\\d][\\d])|(5(4[\\d])|(60)|(89))[\\d]{4}))",
             "mobile": "((441([2378][\\d])|(5[0-39])|(92)[\\d]{5}))",
         },
@@ -251,15 +251,15 @@
         "CR": {
             "code": "506",
             "pattern": "((210[7-9][\\d]{4})|(2([024-7][\\d])|(1[1-9])[\\d]{5}))",
             "mobile": "(((3005[\\d])|(6500[01])[\\d]{3})|((5[07])|(6[0-4])|(7[0-3])|(8[3-9])[\\d]{6}))",
         },
         "CU": {
             "code": "53",
-            "pattern": "(((3[23])|(48)[\\d]{4:6})|((31)|(4[36])|(8(0[25])|(78)[\\d])[\\d]{6})|((2[1-4])|(4[1257])|(7[\\d])[\\d]{5:6}))",
+            "pattern": "(((3[23])|(4[89])[\\d]{4:6})|((31)|(4[36])|(8(0[25])|(78)[\\d])[\\d]{6})|((2[1-4])|(4[1257])|(7[\\d])[\\d]{5:6}))",
             "mobile": "((5[\\d]{7}))",
         },
         "CV": {
             "code": "238",
             "pattern": "((2(2[1-7])|(3[0-8])|(4[12])|(5[1256])|(6[\\d])|(7[1-3])|(8[1-5])[\\d]{4}))",
             "mobile": "(((36)|(5[1-389])|(9[\\d])[\\d]{5}))",
         },
@@ -371,15 +371,15 @@
         "FO": {
             "code": "298",
             "pattern": "(((20)|([34][\\d])|(8[19])[\\d]{4}))",
             "mobile": "((([27][1-9])|(5[\\d])|(9[16])[\\d]{4}))",
         },
         "FR": {
             "code": "33",
-            "pattern": "((([1-35][\\d])|(4[1-9])[\\d]{7}))",
+            "pattern": "((59[1-9][\\d]{6})|(([1-3][\\d])|(4[1-9])|(5[0-8])[\\d]{7}))",
             "mobile": "(((6([0-24-8][\\d])|(3[0-8])|(9[589]))|(7[3-9][\\d])[\\d]{6}))",
         },
         "GA": {
             "code": "241",
             "pattern": "(([01]1[\\d]{6}))",
             "mobile": "((((0[2-7])|(7[467])[\\d])|(6(0[0-4])|(10)|([256][\\d]))[\\d]{5})|([2-7][\\d]{6}))",
         },
@@ -396,15 +396,15 @@
         "GE": {
             "code": "995",
             "pattern": "(((3([256][\\d])|(4[124-9])|(7[0-4]))|(4(1[\\d])|(2[2-7])|(3[1-79])|(4[2-8])|(7[239])|(9[1-7]))[\\d]{6}))",
             "mobile": "((5(((0555)|(1([17]77)|(555))[5-9])|(757(7[7-9])|(8[01]))[\\d])|(22252[0-4])[\\d][\\d])|((5(00(0[\\d])|(44)|(5[05])|(77)|(88)|(99))|(1(1(00)|([124][\\d])|(3[01]))|(4[\\d][\\d]))|((44)|(68)[\\d][\\d])|(5([0157-9][\\d][\\d])|(200))|(7([0147-9][\\d][\\d])|(5(00)|([57]5)))|(8(0([01][\\d])|(2[0-4]))|(58[89])|(8(55)|(88)))|(9(090)|([1-35-9][\\d][\\d])))|(790[\\d][\\d])[\\d]{4})|(5(0(070)|(505))|(1(0[01]0)|(1(07)|(33)|(51)))|(2(0[02]0)|(2[25]2))|(3(0[03]0)|(3[35]3))|((40[04])|(900)0)|(5222)[0-4][\\d]{3}))",
         },
         "GF": {
             "code": "594",
-            "pattern": "((594([0239][\\d])|([16][0-3])|(4[03-9])|(5[6-9])|(80)[\\d]{4}))",
+            "pattern": "((594([02-49][\\d])|([16][0-3])|(5[6-9])|(80)[\\d]{4}))",
             "mobile": "((694([0-249][\\d])|(3[0-8])[\\d]{4}))",
         },
         "GG": {
             "code": "44",
             "pattern": "((1481[25-9][\\d]{5}))",
             "mobile": "((7((781)|(839)[\\d])|(911[17])[\\d]{5}))",
         },
@@ -431,15 +431,15 @@
         "GN": {
             "code": "224",
             "pattern": "((3(0(24)|(3[12])|(4[1-35-7])|(5[13])|(6[189])|([78]1)|(9[1478]))|(1[\\d][\\d])[\\d]{4}))",
             "mobile": "((6[0-356][\\d]{7}))",
         },
         "GP": {
             "code": "590",
-            "pattern": "((590(0[1-68])|([14][0-24-9])|(2[0-68])|(3[1289])|(5[3-579])|([68][0-689])|(7[08])|(9[\\d])[\\d]{4}))",
+            "pattern": "((590(0[1-68])|([14][0-24-9])|(2[0-68])|(3[1-9])|(5[3-579])|([68][0-689])|(7[08])|(9[\\d])[\\d]{4}))",
             "mobile": "((69(0[\\d][\\d])|(1(2[2-9])|(3[0-5]))[\\d]{4}))",
         },
         "GQ": {
             "code": "240",
             "pattern": "((33[0-24-9][\\d][46][\\d]{4})|(3(33)|(5[\\d])[\\d][7-9][\\d]{4}))",
             "mobile": "(((222)|(55[\\d])[\\d]{6}))",
         },
@@ -466,15 +466,15 @@
         "GY": {
             "code": "592",
             "pattern": "(((2(1[6-9])|(2[0-35-9])|(3[1-4])|(5[3-9])|(6[\\d])|(7[0-24-79]))|(3(2[25-9])|(3[\\d]))|(4(4[0-24])|(5[56]))|(77[1-57])[\\d]{4}))",
             "mobile": "(((6[\\d][\\d])|(70[0-35-7])[\\d]{4}))",
         },
         "HK": {
             "code": "852",
-            "pattern": "(((2([13-9][\\d])|(2[013-9])[\\d])|(3(([1569][0-24-9])|(4[0-246-9])|(7[0-24-69])[\\d])|(8([45][0-8])|(6[01])|(9[\\d])))|(58(0[1-8])|(1[2-9]))[\\d]{4}))",
+            "pattern": "(((2([13-9][\\d])|(2[013-9])[\\d])|(3(([1569][0-24-9])|(4[0-246-9])|(7[0-24-69])[\\d])|(8([45][0-8])|(6[01])|(9[\\d])))|(58(0[1-9])|(1[2-9]))[\\d]{4}))",
             "mobile": "(((4(44[5-9])|(6(0[0-7])|(1[0-6])|(4[0-57-9])|(6[0-4])|(7[0-8])))|(573[0-6])|(6(26[013-8])|(66[0-3]))|(70(7[1-5])|(8[0-4]))|(848[015-9])|(9(29[013-9])|(59[0-4]))[\\d]{4})|((4(4[01])|(6[2358]))|(5([1-59][0-46-9])|(6[0-4689])|(7[0-246-9]))|(6(0[1-9])|([13-59][\\d])|([268][0-57-9])|(7[0-79]))|(84[09])|(9(0[1-9])|(1[02-9])|([2358][0-8])|([467][\\d]))[\\d]{5}))",
         },
         "HN": {
             "code": "504",
             "pattern": "((2(2(0[0-59])|(1[1-9])|([23][\\d])|(4[02-6])|(5[57])|(6[245])|(7[0135689])|(8[01346-9])|(9[0-2]))|(4(0[578])|(2[3-59])|(3[13-9])|(4[0-68])|(5[1-3589]))|(5(0[2357-9])|(1[1-356])|(4[03-5])|(5[\\d])|(6[014-69])|(7[04])|(80))|(6([056][\\d])|(17)|(2[067])|(3[047])|(4[0-378])|([78][0-8])|(9[01]))|(7(0[5-79])|(6[46-9])|(7[02-9])|(8[034])|(91))|(8(79)|(8[0-357-9])|(9[1-57-9]))[\\d]{4}))",
             "mobile": "(([37-9][\\d]{7}))",
         },
@@ -593,15 +593,15 @@
             "code": "850",
             "pattern": "((((195)|(2)[\\d])|(3[19])|(4[159])|(5[37])|(6[17])|(7[39])|(85)[\\d]{6}))",
             "mobile": "((19[1-3][\\d]{7}))",
         },
         "KR": {
             "code": "82",
             "pattern": "(((2)|(3[1-3])|([46][1-4])|(5[1-5])[1-9][\\d]{6:7})|((3[1-3])|([46][1-4])|(5[1-5])1[\\d]{2:3}))",
-            "mobile": "((1(05([0-8][\\d])|(9[0-6]))|(22[13][\\d])[\\d]{4:5})|(1(0[1-46-9])|([16-9][\\d])|(2[013-9])[\\d]{6:7}))",
+            "mobile": "((1(05([0-8][\\d])|(9[0-6]))|(22[13][\\d])[\\d]{4:5})|(1(0[0-46-9])|([16-9][\\d])|(2[013-9])[\\d]{6:7}))",
         },
         "KW": {
             "code": "965",
             "pattern": "((2([23][\\d][\\d])|(4([1-35-9][\\d])|(44))|(5(0[034])|([2-46][\\d])|(5[1-3])|(7[1-7]))[\\d]{4}))",
             "mobile": "(((41[\\d][\\d])|(5(([05][\\d])|(1[0-7])|(6[56])[\\d])|(2(22)|(5[25]))|(7(55)|(77))|(88[58]))|(6((0[034679])|(5[015-9])|(6[\\d])[\\d])|(1(00)|(11)|(66))|(222)|(3[36]3)|(444)|(7(0[013-9])|([67][\\d]))|(888)|(9([069][\\d])|(3[039])))|(9((0[09])|([4679][\\d])|(8[057-9])[\\d])|(1(1[01])|(99))|(2(00)|(2[\\d]))|(3(00)|(3[03]))|(5(00)|(5[\\d])))[\\d]{4}))",
         },
         "KY": {
@@ -683,15 +683,15 @@
         "ME": {
             "code": "382",
             "pattern": "(((20[2-8])|(3([0-2][2-7])|(3[24-7]))|(4(0[2-467])|(1[2467]))|(5(0[2467])|(1[24-7])|(2[2-467]))[\\d]{5}))",
             "mobile": "((6([07-9][\\d])|(3[024])|(6[0-25])[\\d]{5}))",
         },
         "MF": {
             "code": "590",
-            "pattern": "((590(0[079])|([14]3)|([27][79])|(30)|(5[0-268])|(87)[\\d]{4}))",
+            "pattern": "((590(0[079])|([14]3)|([27][79])|(3[03-7])|(5[0-268])|(87)[\\d]{4}))",
             "mobile": "((69(0[\\d][\\d])|(1(2[2-9])|(3[0-5]))[\\d]{4}))",
         },
         "MG": {
             "code": "261",
             "pattern": "((2072[29][\\d]{4})|(20(2[\\d])|(4[47])|(5[3467])|(6[279])|(7[35])|(8[268])|(9[245])[\\d]{5}))",
             "mobile": "((3[2-47-9][\\d]{7}))",
         },
@@ -728,15 +728,15 @@
         "MP": {
             "code": "1",
             "pattern": "((670(2(3[3-7])|(56)|(8[4-8]))|(32[1-38])|(4(33)|(8[348]))|(5(32)|(55)|(88))|(6(64)|(70)|(82))|(78[3589])|(8[3-9]8)|(989)[\\d]{4}))",
             "mobile": "((670(2(3[3-7])|(56)|(8[4-8]))|(32[1-38])|(4(33)|(8[348]))|(5(32)|(55)|(88))|(6(64)|(70)|(82))|(78[3589])|(8[3-9]8)|(989)[\\d]{4}))",
         },
         "MQ": {
             "code": "596",
-            "pattern": "((596([03-7][\\d])|(10)|(2[7-9])|(8[09])|(9[4-9])[\\d]{4}))",
+            "pattern": "((596([03-7][\\d])|(10)|(2[7-9])|(8[0-39])|(9[4-9])[\\d]{4}))",
             "mobile": "((69(6([0-46-9][\\d])|(5[0-6]))|(727)[\\d]{4}))",
         },
         "MR": {
             "code": "222",
             "pattern": "(((25[08])|(35[\\d])|(45[1-7])[\\d]{5}))",
             "mobile": "(([2-4][0-46-9][\\d]{6}))",
         },
@@ -748,15 +748,15 @@
         "MT": {
             "code": "356",
             "pattern": "((20(3[1-4])|(6[059])[\\d]{4})|(2(0[19])|([1-357][\\d])|(60)[\\d]{5}))",
             "mobile": "(((7(210)|([79][\\d][\\d]))|(9([29][\\d][\\d])|(69[67])|(8(1[1-3])|(89)|(97)))[\\d]{4}))",
         },
         "MU": {
             "code": "230",
-            "pattern": "(((2([0346-8][\\d])|(1[0-7]))|(4([013568][\\d])|(2[4-7]))|(54([3-5][\\d])|(71))|(6[\\d][\\d])|(8(14)|(3[129]))[\\d]{4}))",
+            "pattern": "(((2([0346-8][\\d])|(1[0-7]))|(4([013568][\\d])|(2[4-8]))|(54([3-5][\\d])|(71))|(6[\\d][\\d])|(8(14)|(3[129]))[\\d]{4}))",
             "mobile": "((5(4(2[1-389])|(7[1-9]))|(87[15-8])[\\d]{4})|((5(2[5-9])|(4[3-689])|([57][\\d])|(8[0-689])|(9[0-8]))|(7(0[0-2])|(3[013]))[\\d]{5}))",
         },
         "MV": {
             "code": "960",
             "pattern": "(((3(0[0-3])|(3[0-59]))|(6([58][024689])|(6[024-68])|(7[02468]))[\\d]{4}))",
             "mobile": "(((46[46])|([79][\\d][\\d])[\\d]{4}))",
         },
@@ -869,15 +869,15 @@
             "code": "63",
             "pattern": "((((2[3-8])|(3[2-68])|(4[2-9])|(5[2-6])|(6[2-58])|(7[24578])[\\d]{3})|(88(22[\\d][\\d])|(42))[\\d]{4})|((2)|(8[2-8][\\d][\\d])[\\d]{5}))",
             "mobile": "(((8(1[37])|(9[5-8]))|(9(0[5-9])|(1[0-24-9])|([235-7][\\d])|(4[2-9])|(8[135-9])|(9[1-9]))[\\d]{7}))",
         },
         "PK": {
             "code": "92",
             "pattern": "((((21)|(42)[2-9])|(58[126])[\\d]{7})|((2[25])|(4[0146-9])|(5[1-35-7])|(6[1-8])|(7[14])|(8[16])|(91)[2-9][\\d]{6:7})|((2(3[2358])|(4[2-4])|(9[2-8]))|(45[3479])|(54[2-467])|(60[468])|(72[236])|(8(2[2-689])|(3[23578])|(4[3478])|(5[2356]))|(9(2[2-8])|(3[27-9])|(4[2-6])|(6[3569])|(9[25-8]))[2-9][\\d]{5:6}))",
-            "mobile": "((3([0-24][\\d])|(3[0-7])|(55)|(64)[\\d]{7}))",
+            "mobile": "((3([0-24][\\d])|(3[0-79])|(55)|(64)[\\d]{7}))",
         },
         "PL": {
             "code": "48",
             "pattern": "((47[\\d]{7})|((1[2-8])|(2[2-69])|(3[2-4])|(4[1-468])|(5[24-689])|(6[1-3578])|(7[14-7])|(8[1-79])|(9[145])([02-9][\\d]{6})|(1([0-8][\\d]{5})|(9[\\d]{3}([\\d]{2})?))))",
             "mobile": "((21(1([145][\\d])|(3[1-5]))|(2[0-4][\\d])[\\d]{4})|((45)|(5[0137])|(6[069])|(7[2389])|(88)[\\d]{7}))",
         },
         "PM": {
@@ -913,16 +913,16 @@
         "QA": {
             "code": "974",
             "pattern": "((4(1111)|(2022)[\\d]{3})|(4([04][\\d][\\d])|(14[0-6])|(999)[\\d]{4}))",
             "mobile": "(([35-7][\\d]{7}))",
         },
         "RE": {
             "code": "262",
-            "pattern": "((26(2[\\d][\\d])|(3(0[\\d])|(1[0-3]))[\\d]{4}))",
-            "mobile": "(((69(2[\\d][\\d])|(3(0[0-46])|(1[013])|(2[0-2])|(3[0-39])|(4[\\d])|(5[0-5])|(6[0-6])|(7[0-27])|(8[0-8])|(9[0-479])))|(9(399[0-3])|(479[0-2])|(76(2[27])|(3[0-37])|(9[\\d])))[\\d]{4}))",
+            "pattern": "((26(2[\\d][\\d])|(3(0[\\d])|(1[0-4]))[\\d]{4}))",
+            "mobile": "((69(2[\\d][\\d])|(3(0[0-46])|(1[013])|(2[0-2])|(3[0-39])|(4[\\d])|(5[0-5])|(6[0-6])|(7[0-27])|(8[0-8])|(9[0-479]))[\\d]{4}))",
         },
         "RO": {
             "code": "40",
             "pattern": "(([23][13-6][\\d]{7})|((2(19[\\d])|([3-6][\\d]9))|(31[\\d][\\d])[\\d][\\d]))",
             "mobile": "((7020[\\d]{5})|(7(0[013-9])|(1[0-3])|([2-7][\\d])|(8[03-8])|(9[0-29])[\\d]{6}))",
         },
         "RS": {
@@ -1004,15 +1004,15 @@
             "code": "221",
             "pattern": "((3(0(1[0-2])|(80))|(282)|(3(8[1-9])|(9[3-9]))|(611)[\\d]{5}))",
             "mobile": "((7(([06-8][\\d])|(21)|(90)[\\d])|(5(01)|([19]0)|(25)|([38]3)|([4-7][\\d]))[\\d]{5}))",
         },
         "SO": {
             "code": "252",
             "pattern": "(((1[\\d])|(2[0-79])|(3[0-46-8])|(4[0-7])|(5[57-9])[\\d]{5})|(([134][\\d])|(8[125])[\\d]{4}))",
-            "mobile": "((((15)|((3[59])|(4[89])|(6[\\d])|(79)|(8[08])[\\d])|(9(0[\\d])|([2-9]))[\\d])|(2(4[\\d])|(8))[\\d]{5})|(([67][\\d][\\d])|(904)[\\d]{5}))",
+            "mobile": "((((15)|((3[59])|(4[89])|(6[\\d])|(7[79])|(8[08])[\\d])|(9(0[\\d])|([2-9]))[\\d])|(2(4[\\d])|(8))[\\d]{5})|(([67][\\d][\\d])|(904)[\\d]{5}))",
         },
         "SR": {
             "code": "597",
             "pattern": "(((2[1-3])|(3[0-7])|((4)|(68)[\\d])|(5[2-58])[\\d]{4}))",
             "mobile": "(((7[124-7])|(8[124-9])[\\d]{5}))",
         },
         "SS": {
@@ -1199,16 +1199,16 @@
         "YE": {
             "code": "967",
             "pattern": "((78[0-7][\\d]{4})|(17[\\d]{6})|(([12][2-68])|(3[2358])|(4[2-58])|(5[2-6])|(6[3-58])|(7[24-6])[\\d]{5}))",
             "mobile": "((7[01378][\\d]{7}))",
         },
         "YT": {
             "code": "262",
-            "pattern": "((269(0[0-467])|(5[0-3])|(6[\\d])|([78]0)[\\d]{4}))",
-            "mobile": "(((639(0[0-79])|(1[019])|([267][\\d])|(3[09])|(40)|(5[05-9])|(9[04-79]))|(9398[01])[\\d]{4}))",
+            "pattern": "((269(0[0-467])|(5[0-4])|(6[\\d])|([78]0)[\\d]{4}))",
+            "mobile": "((639(0[0-79])|(1[019])|([267][\\d])|(3[09])|(40)|(5[05-9])|(9[04-79])[\\d]{4}))",
         },
         "ZA": {
             "code": "27",
             "pattern": "(((2(0330)|(4302))|(52087)0[\\d]{3})|((1[0-8])|(2[1-378])|(3[1-69])|(4[\\d])|(5[1346-8])[\\d]{7}))",
             "mobile": "(((1(3492[0-25])|(4495[0235])|(549(20)|(5[01])))|(4[34]492[01])[\\d]{3})|(8[1-4][\\d]{3:7})|((2[27])|(47)|(54)4950[\\d]{3})|((1(049[2-4])|(9[12][\\d][\\d]))|((6[\\d])|(7[0-46-9])[\\d]{3})|(8(5[\\d]{3})|(7(08[67])|(158)|(28[5-9])|(310)))[\\d]{4})|((1[6-8])|(28)|(3[2-69])|(4[025689])|(5[36-8])4920[\\d]{3})|((12)|([2-5]1)492[\\d]{4}))",
         },
         "ZM": {
```

### Comparing `phone_gen-2.3.4/phone_gen.egg-info/PKG-INFO` & `phone_gen-2.3.5/phone_gen.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: phone-gen
-Version: 2.3.4
+Version: 2.3.5
 Summary: International phone number generation
 Home-page: https://github.com/tolstislon/phone-gen
 Author: tolstislon
 Author-email: tolstislon@gmail.com
 License: MIT License
 Keywords: testing,test-data,phone-number,phone,test-data-generator
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `phone_gen-2.3.4/phone_gen.egg-info/SOURCES.txt` & `phone_gen-2.3.5/phone_gen.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/setup.py` & `phone_gen-2.3.5/setup.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/tests/test_alt_pattern.py` & `phone_gen-2.3.5/tests/test_alt_pattern.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/tests/test_cli.py` & `phone_gen-2.3.5/tests/test_cli.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/tests/test_generator.py` & `phone_gen-2.3.5/tests/test_generator.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/tests/test_load_alt_patterns.py` & `phone_gen-2.3.5/tests/test_load_alt_patterns.py`

 * *Files identical despite different names*

### Comparing `phone_gen-2.3.4/tests/test_phone.py` & `phone_gen-2.3.5/tests/test_phone.py`

 * *Files identical despite different names*

