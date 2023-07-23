# Comparing `tmp/firefish_py-0.0.1.tar.gz` & `tmp/firefish_py-0.0.2.tar.gz`

## Comparing `firefish_py-0.0.1.tar` & `firefish_py-0.0.2.tar`

### file list

```diff
@@ -1,10 +1,23 @@
--rw-r--r--   0        0        0       89 2020-02-02 00:00:00.000000 firefish_py-0.0.1/bot.py
--rw-r--r--   0        0        0     4625 2020-02-02 00:00:00.000000 firefish_py-0.0.1/example.jpg
--rw-r--r--   0        0        0      109 2020-02-02 00:00:00.000000 firefish_py-0.0.1/upload.py
--rw-r--r--   0        0        0        1 2020-02-02 00:00:00.000000 firefish_py-0.0.1/src/firefish/__init__.py
--rw-r--r--   0        0        0     2897 2020-02-02 00:00:00.000000 firefish_py-0.0.1/src/firefish/firefish.py
--rw-r--r--   0        0        0     3093 2020-02-02 00:00:00.000000 firefish_py-0.0.1/.gitignore
--rw-r--r--   0        0        0     1211 2020-02-02 00:00:00.000000 firefish_py-0.0.1/LICENSE
--rw-r--r--   0        0        0     1095 2020-02-02 00:00:00.000000 firefish_py-0.0.1/README.md
--rw-r--r--   0        0        0      567 2020-02-02 00:00:00.000000 firefish_py-0.0.1/pyproject.toml
--rw-r--r--   0        0        0     1601 2020-02-02 00:00:00.000000 firefish_py-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0       89 2020-02-02 00:00:00.000000 firefish_py-0.0.2/bot.py
+-rw-r--r--   0        0        0     4625 2020-02-02 00:00:00.000000 firefish_py-0.0.2/example.jpg
+-rw-r--r--   0        0        0      109 2020-02-02 00:00:00.000000 firefish_py-0.0.2/upload.py
+-rw-r--r--   0        0        0      237 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/pyvenv.cfg
+-rw-r--r--   0        0        0     9033 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/Activate.ps1
+-rw-r--r--   0        0        0     2001 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/activate
+-rw-r--r--   0        0        0      927 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/activate.csh
+-rw-r--r--   0        0        0     2207 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/activate.fish
+-rwxr-xr-x   0        0        0      234 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/dotenv
+-rwxr-xr-x   0        0        0      266 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/normalizer
+-rwxr-xr-x   0        0        0      243 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/pip
+-rwxr-xr-x   0        0        0      243 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/pip3
+-rwxr-xr-x   0        0        0      243 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/pip3.11
+lrwxr-xr-x   0        0        0        0 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/python -> python3
+lrwxr-xr-x   0        0        0        0 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/python3 -> /root/.pyenv/versions/3.11.3/bin/python3
+lrwxr-xr-x   0        0        0        0 2020-02-02 00:00:00.000000 firefish_py-0.0.2/firefish/bin/python3.11 -> python3
+-rw-r--r--   0        0        0      199 2020-02-02 00:00:00.000000 firefish_py-0.0.2/src/firefish/__init__.py
+-rw-r--r--   0        0        0     2897 2020-02-02 00:00:00.000000 firefish_py-0.0.2/src/firefish/firefish.py
+-rw-r--r--   0        0        0     3093 2020-02-02 00:00:00.000000 firefish_py-0.0.2/.gitignore
+-rw-r--r--   0        0        0     1211 2020-02-02 00:00:00.000000 firefish_py-0.0.2/LICENSE
+-rw-r--r--   0        0        0     1055 2020-02-02 00:00:00.000000 firefish_py-0.0.2/README.md
+-rw-r--r--   0        0        0      581 2020-02-02 00:00:00.000000 firefish_py-0.0.2/pyproject.toml
+-rw-r--r--   0        0        0     1575 2020-02-02 00:00:00.000000 firefish_py-0.0.2/PKG-INFO
```

### Comparing `firefish_py-0.0.1/example.jpg` & `firefish_py-0.0.2/example.jpg`

 * *Files identical despite different names*

### Comparing `firefish_py-0.0.1/src/firefish/firefish.py` & `firefish_py-0.0.2/src/firefish/firefish.py`

 * *Files identical despite different names*

### Comparing `firefish_py-0.0.1/.gitignore` & `firefish_py-0.0.2/.gitignore`

 * *Files identical despite different names*

### Comparing `firefish_py-0.0.1/LICENSE` & `firefish_py-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `firefish_py-0.0.1/README.md` & `firefish_py-0.0.2/README.md`

 * *Files 27% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 # firefish.py
 
 Simple python wrapper for the Firefish API.
 
 ## Getting started
 
-I don't have this project setup on pypi. You're gonna have to git clone this for now and enter the firefish.py directory when you want to make a project with this.
+You're going to want to install requests and python-dotenv in order for this to work.
 
-I'm running this with 3.11.3, which is (i think) the latest Python3 version and it should work with all versions of Python3. I haven't tested it though
+You can either install this with pypi by doing `pip install firefish.py` or by building it yourself.
 
-Make sure you have requests and python-dotenv installed as well.
+I'm running this with 3.11.3, which is (i think) the latest Python3 version and it should work with all versions of Python3. I haven't tested it though
 
-Once you clone firefish.py, create a .env file with the following:
+Once you install firefish.py, create a .env file with the following:
 
 ```
 TOKEN=<your firefish api token>
 INSTANCE=<the firefish instance associated with your api token>
 ```
 
 Don't include the < > keys when typing them in, and format your instance as "subdomain.domain.com".
```

### Comparing `firefish_py-0.0.1/PKG-INFO` & `firefish_py-0.0.2/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: firefish.py
-Version: 0.0.1
-Summary: A small example package
+Version: 0.0.2
+Summary: A python wrapper for firefish/calckey
 Project-URL: Homepage, https://codeberg.org/phin/firefish.py
 Project-URL: Bug Tracker, https://codeberg.org/phin/firefish.py/issues
 Author-email: phin <phinw@protonmail.com>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: The Unlicense (Unlicense)
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
@@ -14,21 +14,21 @@
 
 # firefish.py
 
 Simple python wrapper for the Firefish API.
 
 ## Getting started
 
-I don't have this project setup on pypi. You're gonna have to git clone this for now and enter the firefish.py directory when you want to make a project with this.
+You're going to want to install requests and python-dotenv in order for this to work.
 
-I'm running this with 3.11.3, which is (i think) the latest Python3 version and it should work with all versions of Python3. I haven't tested it though
+You can either install this with pypi by doing `pip install firefish.py` or by building it yourself.
 
-Make sure you have requests and python-dotenv installed as well.
+I'm running this with 3.11.3, which is (i think) the latest Python3 version and it should work with all versions of Python3. I haven't tested it though
 
-Once you clone firefish.py, create a .env file with the following:
+Once you install firefish.py, create a .env file with the following:
 
 ```
 TOKEN=<your firefish api token>
 INSTANCE=<the firefish instance associated with your api token>
 ```
 
 Don't include the < > keys when typing them in, and format your instance as "subdomain.domain.com".
```

