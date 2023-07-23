# Comparing `tmp/my-magento-2.1.1b0.tar.gz` & `tmp/my-magento-2.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "my-magento-2.1.1b0.tar", last modified: Mon Feb 20 11:10:59 2023, max compression
+gzip compressed data, was "my-magento-2.1.2.tar", last modified: Sun Jul 23 20:04:08 2023, max compression
```

## Comparing `my-magento-2.1.1b0.tar` & `my-magento-2.1.2.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxrwxrwx   0        0        0        0 2023-02-20 11:10:59.173701 my-magento-2.1.1b0/
--rw-rw-rw-   0        0        0     1084 2022-06-14 16:35:08.000000 my-magento-2.1.1b0/LICENSE
--rw-rw-rw-   0        0        0    28261 2023-02-20 11:10:59.173701 my-magento-2.1.1b0/PKG-INFO
--rw-rw-rw-   0        0        0    23823 2023-02-20 10:11:26.000000 my-magento-2.1.1b0/README.rst
-drwxrwxrwx   0        0        0        0 2023-02-20 11:10:59.158081 my-magento-2.1.1b0/magento/
--rw-rw-rw-   0        0        0     1366 2023-02-20 05:44:24.000000 my-magento-2.1.1b0/magento/__init__.py
--rw-rw-rw-   0        0        0    18625 2023-02-20 05:44:24.000000 my-magento-2.1.1b0/magento/clients.py
--rw-rw-rw-   0        0        0     3092 2023-02-18 06:50:27.000000 my-magento-2.1.1b0/magento/exceptions.py
-drwxrwxrwx   0        0        0        0 2023-02-20 11:10:59.158081 my-magento-2.1.1b0/magento/models/
--rw-rw-rw-   0        0        0      211 2023-01-31 07:48:08.000000 my-magento-2.1.1b0/magento/models/__init__.py
--rw-rw-rw-   0        0        0     5932 2023-02-20 10:04:57.000000 my-magento-2.1.1b0/magento/models/category.py
--rw-rw-rw-   0        0        0     3742 2023-02-18 06:50:27.000000 my-magento-2.1.1b0/magento/models/invoice.py
--rw-rw-rw-   0        0        0    11733 2023-02-18 06:50:27.000000 my-magento-2.1.1b0/magento/models/model.py
--rw-rw-rw-   0        0        0    11528 2023-01-31 07:48:08.000000 my-magento-2.1.1b0/magento/models/order.py
--rw-rw-rw-   0        0        0    23073 2023-01-31 07:48:08.000000 my-magento-2.1.1b0/magento/models/product.py
--rw-rw-rw-   0        0        0    34142 2023-02-18 08:04:39.000000 my-magento-2.1.1b0/magento/search.py
--rw-rw-rw-   0        0        0    15255 2023-01-31 07:48:08.000000 my-magento-2.1.1b0/magento/utils.py
-drwxrwxrwx   0        0        0        0 2023-02-20 11:10:59.173701 my-magento-2.1.1b0/my_magento.egg-info/
--rw-rw-rw-   0        0        0    28261 2023-02-20 11:10:58.000000 my-magento-2.1.1b0/my_magento.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      446 2023-02-20 11:10:58.000000 my-magento-2.1.1b0/my_magento.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-02-20 11:10:58.000000 my-magento-2.1.1b0/my_magento.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-02-20 11:10:58.000000 my-magento-2.1.1b0/my_magento.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-02-20 11:10:58.000000 my-magento-2.1.1b0/my_magento.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-02-20 11:10:59.173701 my-magento-2.1.1b0/setup.cfg
--rw-rw-rw-   0        0        0     1145 2023-02-20 05:44:24.000000 my-magento-2.1.1b0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:04:08.481906 my-magento-2.1.2/
+-rw-rw-rw-   0        0        0     1084 2023-04-27 12:45:18.000000 my-magento-2.1.2/LICENSE
+-rw-rw-rw-   0        0        0    20850 2023-07-23 20:04:08.481906 my-magento-2.1.2/PKG-INFO
+-rw-rw-rw-   0        0        0    20329 2023-07-23 20:03:49.000000 my-magento-2.1.2/README.rst
+drwxrwxrwx   0        0        0        0 2023-07-23 20:04:08.472892 my-magento-2.1.2/magento/
+-rw-rw-rw-   0        0        0     1364 2023-07-23 19:58:56.000000 my-magento-2.1.2/magento/__init__.py
+-rw-rw-rw-   0        0        0    18625 2023-07-09 19:16:23.000000 my-magento-2.1.2/magento/clients.py
+-rw-rw-rw-   0        0        0     3092 2023-05-16 08:18:58.000000 my-magento-2.1.2/magento/exceptions.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:04:08.478874 my-magento-2.1.2/magento/models/
+-rw-rw-rw-   0        0        0      211 2023-05-16 12:35:32.000000 my-magento-2.1.2/magento/models/__init__.py
+-rw-rw-rw-   0        0        0     5932 2023-04-27 12:45:18.000000 my-magento-2.1.2/magento/models/category.py
+-rw-rw-rw-   0        0        0     3742 2023-05-16 12:35:32.000000 my-magento-2.1.2/magento/models/invoice.py
+-rw-rw-rw-   0        0        0    11733 2023-05-16 08:18:58.000000 my-magento-2.1.2/magento/models/model.py
+-rw-rw-rw-   0        0        0    11528 2023-05-16 12:35:32.000000 my-magento-2.1.2/magento/models/order.py
+-rw-rw-rw-   0        0        0    23073 2023-05-16 12:35:32.000000 my-magento-2.1.2/magento/models/product.py
+-rw-rw-rw-   0        0        0    34142 2023-05-16 12:35:32.000000 my-magento-2.1.2/magento/search.py
+-rw-rw-rw-   0        0        0    15255 2023-07-09 19:16:23.000000 my-magento-2.1.2/magento/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:04:08.481906 my-magento-2.1.2/my_magento.egg-info/
+-rw-rw-rw-   0        0        0    20850 2023-07-23 20:04:08.000000 my-magento-2.1.2/my_magento.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      446 2023-07-23 20:04:08.000000 my-magento-2.1.2/my_magento.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 20:04:08.000000 my-magento-2.1.2/my_magento.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 20:04:08.000000 my-magento-2.1.2/my_magento.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-07-23 20:04:08.000000 my-magento-2.1.2/my_magento.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 20:04:08.481906 my-magento-2.1.2/setup.cfg
+-rw-rw-rw-   0        0        0     1140 2023-07-23 20:02:17.000000 my-magento-2.1.2/setup.py
```

### Comparing `my-magento-2.1.1b0/LICENSE` & `my-magento-2.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `my-magento-2.1.1b0/magento/__init__.py` & `my-magento-2.1.2/magento/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from . import clients
 from . import search
 from . import models
 from . import utils
 from . import exceptions
 import os
 
-__version__ = "2.1.1b0"
+__version__ = "2.1.2"
 
 Client = clients.Client
 logger = utils.MagentoLogger(
     name=utils.MagentoLogger.PACKAGE_LOG_NAME,
     log_file=utils.MagentoLogger.PACKAGE_LOG_NAME + '.log',
     stdout_level='WARNING'  # Clients will log to console
 )
```

### Comparing `my-magento-2.1.1b0/magento/clients.py` & `my-magento-2.1.2/magento/clients.py`

 * *Files identical despite different names*

### Comparing `my-magento-2.1.1b0/magento/exceptions.py` & `my-magento-2.1.2/magento/exceptions.py`

 * *Files identical despite different names*

### Comparing `my-magento-2.1.1b0/magento/models/category.py` & `my-magento-2.1.2/magento/models/category.py`

 * *Files identical despite different names*

### Comparing `my-magento-2.1.1b0/magento/models/invoice.py` & `my-magento-2.1.2/magento/models/invoice.py`

 * *Files identical despite different names*

### Comparing `my-magento-2.1.1b0/magento/models/model.py` & `my-magento-2.1.2/magento/models/model.py`

 * *Files identical despite different names*

### Comparing `my-magento-2.1.1b0/magento/models/order.py` & `my-magento-2.1.2/magento/models/order.py`

 * *Files identical despite different names*

### Comparing `my-magento-2.1.1b0/magento/models/product.py` & `my-magento-2.1.2/magento/models/product.py`

 * *Files identical despite different names*

### Comparing `my-magento-2.1.1b0/magento/search.py` & `my-magento-2.1.2/magento/search.py`

 * *Files identical despite different names*

### Comparing `my-magento-2.1.1b0/magento/utils.py` & `my-magento-2.1.2/magento/utils.py`

 * *Files identical despite different names*

### Comparing `my-magento-2.1.1b0/setup.py` & `my-magento-2.1.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import os
 from pathlib import Path
 from setuptools import setup, find_packages
 
 
-LONG_DESCRIPTION_SRC = 'README_PyPi.rst'
+LONG_DESCRIPTION_SRC = 'README.rst'
 
 
 def read(file):
     with open(os.path.abspath(file), 'r', encoding='utf-8') as f:
         return f.read()
```

