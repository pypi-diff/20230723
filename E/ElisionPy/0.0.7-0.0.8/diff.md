# Comparing `tmp/ElisionPy-0.0.7.tar.gz` & `tmp/ElisionPy-0.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ElisionPy-0.0.7.tar", last modified: Sat Jul 22 20:21:40 2023, max compression
+gzip compressed data, was "ElisionPy-0.0.8.tar", last modified: Sat Jul 22 22:02:15 2023, max compression
```

## Comparing `ElisionPy-0.0.7.tar` & `ElisionPy-0.0.8.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 20:21:40.102053 ElisionPy-0.0.7/
-drwxrwxrwx   0        0        0        0 2023-07-22 20:21:40.100053 ElisionPy-0.0.7/ElisionPy.egg-info/
--rw-rw-rw-   0        0        0      552 2023-07-22 20:21:40.000000 ElisionPy-0.0.7/ElisionPy.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      246 2023-07-22 20:21:40.000000 ElisionPy-0.0.7/ElisionPy.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 20:21:40.000000 ElisionPy-0.0.7/ElisionPy.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       31 2023-07-22 20:21:40.000000 ElisionPy-0.0.7/ElisionPy.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-07-22 20:21:40.000000 ElisionPy-0.0.7/ElisionPy.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      552 2023-07-22 20:21:40.102053 ElisionPy-0.0.7/PKG-INFO
--rw-rw-rw-   0        0        0       33 2023-07-22 19:00:10.000000 ElisionPy-0.0.7/README.md
-drwxrwxrwx   0        0        0        0 2023-07-22 20:21:40.102053 ElisionPy-0.0.7/elision/
--rw-rw-rw-   0        0        0        0 2023-07-22 19:43:20.000000 ElisionPy-0.0.7/elision/__init__.py
--rw-rw-rw-   0        0        0      711 2023-07-22 20:21:20.000000 ElisionPy-0.0.7/elision/help.py
--rw-rw-rw-   0        0        0     2142 2023-07-22 20:21:27.000000 ElisionPy-0.0.7/elision/random.py
--rw-rw-rw-   0        0        0       42 2023-07-22 20:21:40.103054 ElisionPy-0.0.7/setup.cfg
--rw-rw-rw-   0        0        0      805 2023-07-22 20:20:33.000000 ElisionPy-0.0.7/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-22 22:02:15.510418 ElisionPy-0.0.8/
+drwxrwxrwx   0        0        0        0 2023-07-22 22:02:15.508422 ElisionPy-0.0.8/ElisionPy.egg-info/
+-rw-rw-rw-   0        0        0      552 2023-07-22 22:02:15.000000 ElisionPy-0.0.8/ElisionPy.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      246 2023-07-22 22:02:15.000000 ElisionPy-0.0.8/ElisionPy.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-22 22:02:15.000000 ElisionPy-0.0.8/ElisionPy.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       31 2023-07-22 22:02:15.000000 ElisionPy-0.0.8/ElisionPy.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-07-22 22:02:15.000000 ElisionPy-0.0.8/ElisionPy.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      552 2023-07-22 22:02:15.510418 ElisionPy-0.0.8/PKG-INFO
+-rw-rw-rw-   0        0        0       33 2023-07-22 19:00:10.000000 ElisionPy-0.0.8/README.md
+drwxrwxrwx   0        0        0        0 2023-07-22 22:02:15.509418 ElisionPy-0.0.8/elision/
+-rw-rw-rw-   0        0        0        0 2023-07-22 19:43:20.000000 ElisionPy-0.0.8/elision/__init__.py
+-rw-rw-rw-   0        0        0      711 2023-07-22 20:21:20.000000 ElisionPy-0.0.8/elision/help.py
+-rw-rw-rw-   0        0        0     2141 2023-07-22 21:59:13.000000 ElisionPy-0.0.8/elision/random.py
+-rw-rw-rw-   0        0        0       42 2023-07-22 22:02:15.511418 ElisionPy-0.0.8/setup.cfg
+-rw-rw-rw-   0        0        0      805 2023-07-22 22:02:01.000000 ElisionPy-0.0.8/setup.py
```

### Comparing `ElisionPy-0.0.7/ElisionPy.egg-info/PKG-INFO` & `ElisionPy-0.0.8/ElisionPy.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ElisionPy
-Version: 0.0.7
+Version: 0.0.8
 Summary: This module is under development!
 Home-page: https://github.com/Ginji-Fox/ElisionPy
 Author: Ginji
 Author-email: bfire1999@gmail.com
 Project-URL: Documentation, https://github.com/Ginji-Fox/ElisionPy
 Keywords: ElisionPy Elision
 Classifier: Programming Language :: Python :: 3.11
```

### Comparing `ElisionPy-0.0.7/PKG-INFO` & `ElisionPy-0.0.8/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: ElisionPy
-Version: 0.0.7
+Version: 0.0.8
 Summary: This module is under development!
 Home-page: https://github.com/Ginji-Fox/ElisionPy
 Author: Ginji
 Author-email: bfire1999@gmail.com
 Project-URL: Documentation, https://github.com/Ginji-Fox/ElisionPy
 Keywords: ElisionPy Elision
 Classifier: Programming Language :: Python :: 3.11
```

### Comparing `ElisionPy-0.0.7/elision/help.py` & `ElisionPy-0.0.8/elision/help.py`

 * *Files identical despite different names*

### Comparing `ElisionPy-0.0.7/elision/random.py` & `ElisionPy-0.0.8/elision/random.py`

 * *Files 11% similar despite different names*

```diff
@@ -27,22 +27,22 @@
 			if ei <= 40:
 				if generate >= x and generate <= y:
 					break
 				elif x == y:
 					return x
 
 				if int_for_gen < x:
-					int_for_gen = int_for_gen + y + 25
+					int_for_gen = int_for_gen + y + 50
 					ei += 1
 
-				int_for_gen /= 17
+				int_for_gen /= 5
 
 				generate = int_for_gen
 			else:
-				int_for_gen = int_for_gen + y + 26
+				int_for_gen = int_for_gen + y + 51
 				ei = 0
 		return int(round(generate))
 
 	@classmethod
 	def seed(self, a: int = seed_a, c: int = seed_c) -> None:
 
 		if c < 0: c = 0
```

### Comparing `ElisionPy-0.0.7/setup.py` & `ElisionPy-0.0.8/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 def readme():
   with open('README.md', 'r') as f:
     return f.read()
 
 setup(
   name='ElisionPy',
-  version='0.0.7',
+  version='0.0.8',
   author='Ginji',
   author_email='bfire1999@gmail.com',
   description='This module is under development!',
   long_description=readme(),
   long_description_content_type='text/markdown',
   url='https://github.com/Ginji-Fox/ElisionPy',
   packages=find_packages(),
```

