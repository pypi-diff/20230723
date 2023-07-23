# Comparing `tmp/my-finance-package-0.1.0.tar.gz` & `tmp/my-finance-package-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "my-finance-package-0.1.0.tar", last modified: Sun Jul 23 07:52:19 2023, max compression
+gzip compressed data, was "my-finance-package-0.2.0.tar", last modified: Sun Jul 23 15:17:06 2023, max compression
```

## Comparing `my-finance-package-0.1.0.tar` & `my-finance-package-0.2.0.tar`

### file list

```diff
@@ -1,11 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 07:52:19.388843 my-finance-package-0.1.0/
--rw-rw-rw-   0        0        0      721 2023-07-23 07:52:19.387843 my-finance-package-0.1.0/PKG-INFO
--rw-rw-rw-   0        0        0        0 2023-07-23 07:45:30.000000 my-finance-package-0.1.0/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 07:52:19.386189 my-finance-package-0.1.0/my_finance_package.egg-info/
--rw-rw-rw-   0        0        0      721 2023-07-23 07:52:19.000000 my-finance-package-0.1.0/my_finance_package.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      227 2023-07-23 07:52:19.000000 my-finance-package-0.1.0/my_finance_package.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 07:52:19.000000 my-finance-package-0.1.0/my_finance_package.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       32 2023-07-23 07:52:19.000000 my-finance-package-0.1.0/my_finance_package.egg-info/requires.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 07:52:19.000000 my-finance-package-0.1.0/my_finance_package.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 07:52:19.389514 my-finance-package-0.1.0/setup.cfg
--rw-rw-rw-   0        0        0      945 2023-07-23 07:47:39.000000 my-finance-package-0.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:17:06.747237 my-finance-package-0.2.0/
+-rw-rw-rw-   0        0        0      721 2023-07-23 15:17:06.744583 my-finance-package-0.2.0/PKG-INFO
+-rw-rw-rw-   0        0        0        0 2023-07-23 07:45:30.000000 my-finance-package-0.2.0/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 15:17:06.728303 my-finance-package-0.2.0/my_finance_package.egg-info/
+drwxrwxrwx   0        0        0        0 2023-07-23 15:17:06.741340 my-finance-package-0.2.0/my_finance_package.egg-info/.ipynb_checkpoints/
+-rw-rw-rw-   0        0        0      721 2023-07-23 07:52:19.000000 my-finance-package-0.2.0/my_finance_package.egg-info/.ipynb_checkpoints/PKG-INFO-checkpoint
+-rw-rw-rw-   0        0        0      227 2023-07-23 07:52:19.000000 my-finance-package-0.2.0/my_finance_package.egg-info/.ipynb_checkpoints/SOURCES-checkpoint.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 07:52:19.000000 my-finance-package-0.2.0/my_finance_package.egg-info/.ipynb_checkpoints/dependency_links-checkpoint.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 07:52:19.000000 my-finance-package-0.2.0/my_finance_package.egg-info/.ipynb_checkpoints/top_level-checkpoint.txt
+-rw-rw-rw-   0        0        0      721 2023-07-23 15:17:06.000000 my-finance-package-0.2.0/my_finance_package.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      515 2023-07-23 15:17:06.000000 my-finance-package-0.2.0/my_finance_package.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:17:06.000000 my-finance-package-0.2.0/my_finance_package.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       32 2023-07-23 15:17:06.000000 my-finance-package-0.2.0/my_finance_package.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:17:06.000000 my-finance-package-0.2.0/my_finance_package.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 15:17:06.748068 my-finance-package-0.2.0/setup.cfg
+-rw-rw-rw-   0        0        0      945 2023-07-23 15:16:20.000000 my-finance-package-0.2.0/setup.py
```

### Comparing `my-finance-package-0.1.0/PKG-INFO` & `my-finance-package-0.2.0/my_finance_package.egg-info/.ipynb_checkpoints/PKG-INFO-checkpoint`

 * *Files identical despite different names*

### Comparing `my-finance-package-0.1.0/my_finance_package.egg-info/PKG-INFO` & `my-finance-package-0.2.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: my-finance-package
-Version: 0.1.0
+Version: 0.2.0
 Summary: A package for analyzing Financial Instruments like stocks.
 Home-page: https://github.com/MANOJ21K/FinOps/blob/main/custom_package
 Author: Manoj Kumar
 Author-email: manojkotary@gmail.com
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `my-finance-package-0.1.0/setup.py` & `my-finance-package-0.2.0/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='my-finance-package',
-    version='0.1.0',
+    version='0.2.0',
     packages=find_packages(),
     install_requires=[
         'finnhub',
         'pandas',
         'numpy',
         'matplotlib'
     ],
```

