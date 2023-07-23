# Comparing `tmp/lisql-2.1.tar.gz` & `tmp/lisql-2.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lisql-2.1.tar", last modified: Sun Jul 23 18:21:51 2023, max compression
+gzip compressed data, was "lisql-2.1.1.tar", last modified: Sun Jul 23 18:49:32 2023, max compression
```

## Comparing `lisql-2.1.tar` & `lisql-2.1.1.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 li         (501) staff       (20)        0 2023-07-23 18:21:51.287914 lisql-2.1/
--rw-r--r--   0 li         (501) staff       (20)     1068 2023-05-14 18:33:24.000000 lisql-2.1/LICENSE
--rw-r--r--   0 li         (501) staff       (20)    19100 2023-07-23 18:21:51.288016 lisql-2.1/PKG-INFO
--rw-r--r--   0 li         (501) staff       (20)    18320 2023-07-23 17:26:59.000000 lisql-2.1/README.md
--rw-r--r--   0 li         (501) staff       (20)      103 2023-05-14 18:33:24.000000 lisql-2.1/pyproject.toml
--rw-r--r--   0 li         (501) staff       (20)      601 2023-07-23 18:21:51.288669 lisql-2.1/setup.cfg
--rw-r--r--   0 li         (501) staff       (20)      723 2023-07-21 21:32:35.000000 lisql-2.1/setup.py
-drwxr-xr-x   0 li         (501) staff       (20)        0 2023-07-23 18:21:51.286919 lisql-2.1/src/
-drwxr-xr-x   0 li         (501) staff       (20)        0 2023-07-23 18:21:51.287798 lisql-2.1/src/lisql.egg-info/
--rw-r--r--   0 li         (501) staff       (20)    19100 2023-07-23 18:21:51.000000 lisql-2.1/src/lisql.egg-info/PKG-INFO
--rw-r--r--   0 li         (501) staff       (20)      196 2023-07-23 18:21:51.000000 lisql-2.1/src/lisql.egg-info/SOURCES.txt
--rw-r--r--   0 li         (501) staff       (20)        1 2023-07-23 18:21:51.000000 lisql-2.1/src/lisql.egg-info/dependency_links.txt
--rw-r--r--   0 li         (501) staff       (20)        6 2023-07-23 18:21:51.000000 lisql-2.1/src/lisql.egg-info/top_level.txt
--rw-r--r--   0 li         (501) staff       (20)    22817 2023-07-23 18:15:58.000000 lisql-2.1/src/lisql.py
+drwxr-xr-x   0 li         (501) staff       (20)        0 2023-07-23 18:49:32.468432 lisql-2.1.1/
+-rw-r--r--   0 li         (501) staff       (20)     1068 2023-05-14 18:33:24.000000 lisql-2.1.1/LICENSE
+-rw-r--r--   0 li         (501) staff       (20)    18962 2023-07-23 18:49:32.468600 lisql-2.1.1/PKG-INFO
+-rw-r--r--   0 li         (501) staff       (20)    18180 2023-07-23 18:47:28.000000 lisql-2.1.1/README.md
+-rw-r--r--   0 li         (501) staff       (20)      103 2023-05-14 18:33:24.000000 lisql-2.1.1/pyproject.toml
+-rw-r--r--   0 li         (501) staff       (20)      644 2023-07-23 18:49:32.469153 lisql-2.1.1/setup.cfg
+-rw-r--r--   0 li         (501) staff       (20)      725 2023-07-23 18:47:03.000000 lisql-2.1.1/setup.py
+drwxr-xr-x   0 li         (501) staff       (20)        0 2023-07-23 18:49:32.467675 lisql-2.1.1/src/
+drwxr-xr-x   0 li         (501) staff       (20)        0 2023-07-23 18:49:32.468279 lisql-2.1.1/src/lisql.egg-info/
+-rw-r--r--   0 li         (501) staff       (20)    18962 2023-07-23 18:49:32.000000 lisql-2.1.1/src/lisql.egg-info/PKG-INFO
+-rw-r--r--   0 li         (501) staff       (20)      196 2023-07-23 18:49:32.000000 lisql-2.1.1/src/lisql.egg-info/SOURCES.txt
+-rw-r--r--   0 li         (501) staff       (20)        1 2023-07-23 18:49:32.000000 lisql-2.1.1/src/lisql.egg-info/dependency_links.txt
+-rw-r--r--   0 li         (501) staff       (20)        6 2023-07-23 18:49:32.000000 lisql-2.1.1/src/lisql.egg-info/top_level.txt
+-rw-r--r--   0 li         (501) staff       (20)    22817 2023-07-23 18:15:58.000000 lisql-2.1.1/src/lisql.py
```

### Comparing `lisql-2.1/LICENSE` & `lisql-2.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `lisql-2.1/PKG-INFO` & `lisql-2.1.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lisql
-Version: 2.1
+Version: 2.1.1
 Summary: Provides simple funtions to interact with MySQL databases and tables.
 Home-page: https://github.com/li812/lisql
 Author: Ali Ahammad
 Author-email: aliahammad0812@outlook.com
 Project-URL: Bug Tracker, https://github.com/li812/lisql/issues
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -34,23 +34,26 @@
 ## Key Features of LiSQL
 
 - **Efficient Connection** Management: LiSQL facilitates establishing connections to different servers, enabling seamless data access and manipulation.
 
 - **Simplified Database and Table Operations**: Create, drop, and describe databases and tables with ease, effectively organizing and structuring your data.
 
 - **Easy Data Manipulation**: Perform data manipulations effortlessly with LiSQL's functions for selecting, inserting, updating, and deleting data.
+
 - **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
-- **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
+
 - **Transaction Support**: Execute multiple database operations as a single unit with transaction support, ensuring data integrity and consistency.
 
 
 ## Requirements
 #### 1. Python 3.6 or higher:
 LiSQL requires Python 3.6 or higher.
-#### 2. MySQL Connector/Python: 
+
+
+#### 2. Python MySQL Connector: 
 LiSQL depends on the MySQL Connector/Python library to establish connections with MySQL databases. Make sure you have this library installed.
 
 You can install the mysql-connector-python library using pip:
 ```commandline
 pip install mysql-connector-python
 
 ```
```

### Comparing `lisql-2.1/README.md` & `lisql-2.1.1/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -14,23 +14,26 @@
 ## Key Features of LiSQL
 
 - **Efficient Connection** Management: LiSQL facilitates establishing connections to different servers, enabling seamless data access and manipulation.
 
 - **Simplified Database and Table Operations**: Create, drop, and describe databases and tables with ease, effectively organizing and structuring your data.
 
 - **Easy Data Manipulation**: Perform data manipulations effortlessly with LiSQL's functions for selecting, inserting, updating, and deleting data.
+
 - **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
-- **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
+
 - **Transaction Support**: Execute multiple database operations as a single unit with transaction support, ensuring data integrity and consistency.
 
 
 ## Requirements
 #### 1. Python 3.6 or higher:
 LiSQL requires Python 3.6 or higher.
-#### 2. MySQL Connector/Python: 
+
+
+#### 2. Python MySQL Connector: 
 LiSQL depends on the MySQL Connector/Python library to establish connections with MySQL databases. Make sure you have this library installed.
 
 You can install the mysql-connector-python library using pip:
 ```commandline
 pip install mysql-connector-python
 
 ```
```

### Comparing `lisql-2.1/setup.cfg` & `lisql-2.1.1/setup.cfg`

 * *Files 13% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 [metadata]
 name = lisql
-version = 2.1
+version = 2.1.1
 author = Ali Ahammad
 author_email = aliahammad0812@outlook.com
-description = Python sql companion
+description = Provides a simple interface to interact with MySQL databases.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/li812/lisql
 project_urls = 
 	Bug Tracker = https://github.com/li812/lisql/issues
 classifiers = 
 	Programming Language :: Python :: 3
```

### Comparing `lisql-2.1/setup.py` & `lisql-2.1.1/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup
 
 setup(
     name='lisql',
-    version='2.1',
+    version='2.1.1',
     py_modules=['lisql'],
     description='Provides simple funtions to interact with MySQL databases and tables.',
     author='Ali Ahammad',
     author_email='aliahammad0812@outlook.com',
     url='https://github.com/li812/lisql',
     classifiers=[
         'License :: OSI Approved :: MIT License',
```

### Comparing `lisql-2.1/src/lisql.egg-info/PKG-INFO` & `lisql-2.1.1/src/lisql.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lisql
-Version: 2.1
+Version: 2.1.1
 Summary: Provides simple funtions to interact with MySQL databases and tables.
 Home-page: https://github.com/li812/lisql
 Author: Ali Ahammad
 Author-email: aliahammad0812@outlook.com
 Project-URL: Bug Tracker, https://github.com/li812/lisql/issues
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -34,23 +34,26 @@
 ## Key Features of LiSQL
 
 - **Efficient Connection** Management: LiSQL facilitates establishing connections to different servers, enabling seamless data access and manipulation.
 
 - **Simplified Database and Table Operations**: Create, drop, and describe databases and tables with ease, effectively organizing and structuring your data.
 
 - **Easy Data Manipulation**: Perform data manipulations effortlessly with LiSQL's functions for selecting, inserting, updating, and deleting data.
+
 - **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
-- **Insightful Aggregate Functions**: Quickly gain valuable insights with LiSQL's aggregate functions, including COUNT, SUM, AVG, MIN, and MAX.
+
 - **Transaction Support**: Execute multiple database operations as a single unit with transaction support, ensuring data integrity and consistency.
 
 
 ## Requirements
 #### 1. Python 3.6 or higher:
 LiSQL requires Python 3.6 or higher.
-#### 2. MySQL Connector/Python: 
+
+
+#### 2. Python MySQL Connector: 
 LiSQL depends on the MySQL Connector/Python library to establish connections with MySQL databases. Make sure you have this library installed.
 
 You can install the mysql-connector-python library using pip:
 ```commandline
 pip install mysql-connector-python
 
 ```
```

### Comparing `lisql-2.1/src/lisql.py` & `lisql-2.1.1/src/lisql.py`

 * *Files identical despite different names*

