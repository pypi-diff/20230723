# Comparing `tmp/monkeywork-0.1.tar.gz` & `tmp/monkeywork-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "monkeywork-0.1.tar", last modified: Sun Jul 23 11:13:26 2023, max compression
+gzip compressed data, was "monkeywork-0.1.1.tar", last modified: Sun Jul 23 11:51:03 2023, max compression
```

## Comparing `monkeywork-0.1.tar` & `monkeywork-0.1.1.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 11:13:26.396269 monkeywork-0.1/
--rw-rw-rw-   0        0        0    35823 2023-07-23 11:00:58.000000 monkeywork-0.1/LICENCE
--rw-rw-rw-   0        0        0     1965 2023-07-23 11:13:26.396269 monkeywork-0.1/PKG-INFO
--rw-rw-rw-   0        0        0     1499 2023-07-23 11:03:54.000000 monkeywork-0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 11:13:26.383372 monkeywork-0.1/monkeywork/
--rw-rw-rw-   0        0        0        0 2023-07-23 10:15:15.000000 monkeywork-0.1/monkeywork/__init__.py
--rw-rw-rw-   0        0        0     9657 2023-07-23 11:07:50.000000 monkeywork-0.1/monkeywork/monkeywork.py
-drwxrwxrwx   0        0        0        0 2023-07-23 11:13:26.395271 monkeywork-0.1/monkeywork.egg-info/
--rw-rw-rw-   0        0        0     1965 2023-07-23 11:13:26.000000 monkeywork-0.1/monkeywork.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      210 2023-07-23 11:13:26.000000 monkeywork-0.1/monkeywork.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 11:13:26.000000 monkeywork-0.1/monkeywork.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       11 2023-07-23 11:13:26.000000 monkeywork-0.1/monkeywork.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 11:13:26.396269 monkeywork-0.1/setup.cfg
--rw-rw-rw-   0        0        0      624 2023-07-23 10:56:49.000000 monkeywork-0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:51:03.050101 monkeywork-0.1.1/
+-rw-rw-rw-   0        0        0    35823 2023-07-23 11:00:58.000000 monkeywork-0.1.1/LICENCE
+-rw-rw-rw-   0        0        0     2643 2023-07-23 11:51:03.050101 monkeywork-0.1.1/PKG-INFO
+-rw-rw-rw-   0        0        0     2177 2023-07-23 11:48:49.000000 monkeywork-0.1.1/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 11:51:03.038807 monkeywork-0.1.1/monkeywork/
+-rw-rw-rw-   0        0        0        0 2023-07-23 10:15:15.000000 monkeywork-0.1.1/monkeywork/__init__.py
+-rw-rw-rw-   0        0        0     9657 2023-07-23 11:07:50.000000 monkeywork-0.1.1/monkeywork/monkeywork.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:51:03.048905 monkeywork-0.1.1/monkeywork.egg-info/
+-rw-rw-rw-   0        0        0     2643 2023-07-23 11:51:02.000000 monkeywork-0.1.1/monkeywork.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      210 2023-07-23 11:51:03.000000 monkeywork-0.1.1/monkeywork.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 11:51:02.000000 monkeywork-0.1.1/monkeywork.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 11:51:02.000000 monkeywork-0.1.1/monkeywork.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 11:51:03.050101 monkeywork-0.1.1/setup.cfg
+-rw-rw-rw-   0        0        0      626 2023-07-23 11:50:23.000000 monkeywork-0.1.1/setup.py
```

### Comparing `monkeywork-0.1/LICENCE` & `monkeywork-0.1.1/LICENCE`

 * *Files identical despite different names*

### Comparing `monkeywork-0.1/PKG-INFO` & `monkeywork-0.1.1/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: monkeywork
-Version: 0.1
+Version: 0.1.1
 Summary: Write and edit random files in a given directory
 Home-page: https://github.com/pylomatic/monkeywork
 Author: Pylomatic
 Author-email: pylomatic@conelab.ch
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -30,30 +30,53 @@
 
 The idea behind this program is to run it on both ends of a file sharing or syncing solution. By doing so, you can test whether your solution is capable of handling regular and potentially conflicting user activities.
 
 ## !!! CAUTION !!!
 
 The program can and will destroy files in the selected work directory. Be sure to select a dedicated work directory and **review the code before executing it on your system**!
 
-## Installation
+## Run in console
 
 You can run the `monkeywork.py`directly from from the console with:
 
 ```bash
 python monkeywork.py "<Path to your workdir>" [OPTIONS]
 ```
 
 example:
 ```bash
-python monkeywork.py "L:\\monkeywork-test\\"
+python monkeywork.py "L:\monkeywork-test\"
 ```
 
 Options are:
-- f | force selected direcotry and delete all contents in set directory
+
+-f | force selected direcotry and delete all contents in set directory
 
 ## Installation
 
 Use it as a package
 
 ```bash
 pip install monkeywork
 ```
+
+## Usage
+
+Example with custom interval setting:
+```python
+from monkeywork import Monkey
+
+mky = Monkey(workdir="F:/mky-test", interval_min_s=.1, interval_max_s=1)
+mky.run()
+```
+
+orther avaiable setting:
+|variable | Description |
+|---|---|
+|workdir:str| must be set to a valid path |
+|interval_min_s:float | shortest interval |
+|interval_max_s:float | longest interval |
+|max_file_size_mb:int | maximum file size in MB |
+|max_file_amount:int | maximumg file count
+|target_file_amount:int | program targets this amount of files |
+|path_length_limit:int | program should not exceed set path length |
+|logging_to_file_enabled:bool | enable loggin to file |
```

### Comparing `monkeywork-0.1/monkeywork/monkeywork.py` & `monkeywork-0.1.1/monkeywork/monkeywork.py`

 * *Files identical despite different names*

### Comparing `monkeywork-0.1/monkeywork.egg-info/PKG-INFO` & `monkeywork-0.1.1/monkeywork.egg-info/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: monkeywork
-Version: 0.1
+Version: 0.1.1
 Summary: Write and edit random files in a given directory
 Home-page: https://github.com/pylomatic/monkeywork
 Author: Pylomatic
 Author-email: pylomatic@conelab.ch
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -30,30 +30,53 @@
 
 The idea behind this program is to run it on both ends of a file sharing or syncing solution. By doing so, you can test whether your solution is capable of handling regular and potentially conflicting user activities.
 
 ## !!! CAUTION !!!
 
 The program can and will destroy files in the selected work directory. Be sure to select a dedicated work directory and **review the code before executing it on your system**!
 
-## Installation
+## Run in console
 
 You can run the `monkeywork.py`directly from from the console with:
 
 ```bash
 python monkeywork.py "<Path to your workdir>" [OPTIONS]
 ```
 
 example:
 ```bash
-python monkeywork.py "L:\\monkeywork-test\\"
+python monkeywork.py "L:\monkeywork-test\"
 ```
 
 Options are:
-- f | force selected direcotry and delete all contents in set directory
+
+-f | force selected direcotry and delete all contents in set directory
 
 ## Installation
 
 Use it as a package
 
 ```bash
 pip install monkeywork
 ```
+
+## Usage
+
+Example with custom interval setting:
+```python
+from monkeywork import Monkey
+
+mky = Monkey(workdir="F:/mky-test", interval_min_s=.1, interval_max_s=1)
+mky.run()
+```
+
+orther avaiable setting:
+|variable | Description |
+|---|---|
+|workdir:str| must be set to a valid path |
+|interval_min_s:float | shortest interval |
+|interval_max_s:float | longest interval |
+|max_file_size_mb:int | maximum file size in MB |
+|max_file_amount:int | maximumg file count
+|target_file_amount:int | program targets this amount of files |
+|path_length_limit:int | program should not exceed set path length |
+|logging_to_file_enabled:bool | enable loggin to file |
```

### Comparing `monkeywork-0.1/setup.py` & `monkeywork-0.1.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="monkeywork",
-    version="0.1",
+    version="0.1.1",
     packages=find_packages(),
     author="Pylomatic",
     author_email="pylomatic@conelab.ch",
     description="Write and edit random files in a given directory",
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
     url="https://github.com/pylomatic/monkeywork",
```

