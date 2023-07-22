# Comparing `tmp/nsj_sql_utils_lib-0.0.1.tar.gz` & `tmp/nsj_sql_utils_lib-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nsj_sql_utils_lib-0.0.1.tar", last modified: Sat Jul 22 22:11:21 2023, max compression
+gzip compressed data, was "nsj_sql_utils_lib-0.0.2.tar", last modified: Sat Jul 22 22:15:35 2023, max compression
```

## Comparing `nsj_sql_utils_lib-0.0.1.tar` & `nsj_sql_utils_lib-0.0.2.tar`

### file list

```diff
@@ -1,12 +1,16 @@
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:11:21.117904 nsj_sql_utils_lib-0.0.1/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1215 2023-07-22 22:11:21.117904 nsj_sql_utils_lib-0.0.1/PKG-INFO
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      594 2023-07-22 22:08:44.000000 nsj_sql_utils_lib-0.0.1/README.md
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:11:21.117904 nsj_sql_utils_lib-0.0.1/nsj_sql_utils_lib/
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:11:21.117904 nsj_sql_utils_lib-0.0.1/nsj_sql_utils_lib/nsj_sql_utils_lib.egg-info/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1215 2023-07-22 22:11:21.000000 nsj_sql_utils_lib-0.0.1/nsj_sql_utils_lib/nsj_sql_utils_lib.egg-info/PKG-INFO
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      328 2023-07-22 22:11:21.000000 nsj_sql_utils_lib-0.0.1/nsj_sql_utils_lib/nsj_sql_utils_lib.egg-info/SOURCES.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-22 22:11:21.000000 nsj_sql_utils_lib-0.0.1/nsj_sql_utils_lib/nsj_sql_utils_lib.egg-info/dependency_links.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)       23 2023-07-22 22:11:21.000000 nsj_sql_utils_lib-0.0.1/nsj_sql_utils_lib/nsj_sql_utils_lib.egg-info/requires.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-22 22:11:21.000000 nsj_sql_utils_lib-0.0.1/nsj_sql_utils_lib/nsj_sql_utils_lib.egg-info/top_level.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      103 2023-07-22 22:03:17.000000 nsj_sql_utils_lib-0.0.1/pyproject.toml
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      829 2023-07-22 22:11:21.117904 nsj_sql_utils_lib-0.0.1/setup.cfg
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:15:35.289628 nsj_sql_utils_lib-0.0.2/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1215 2023-07-22 22:15:35.289628 nsj_sql_utils_lib-0.0.2/PKG-INFO
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      594 2023-07-22 22:08:44.000000 nsj_sql_utils_lib-0.0.2/README.md
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:15:35.289628 nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)        0 2023-07-22 21:56:47.000000 nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib/__init__.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      922 2023-07-22 22:06:27.000000 nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib/dao_util.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3274 2023-07-22 22:01:20.000000 nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib/dbadapter3.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      869 2023-07-22 22:02:23.000000 nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib/dbconection_psycopg2.py
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:15:35.289628 nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib.egg-info/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1215 2023-07-22 22:15:35.000000 nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib.egg-info/PKG-INFO
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      390 2023-07-22 22:15:35.000000 nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib.egg-info/SOURCES.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-22 22:15:35.000000 nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib.egg-info/dependency_links.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       23 2023-07-22 22:15:35.000000 nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib.egg-info/requires.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       18 2023-07-22 22:15:35.000000 nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib.egg-info/top_level.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      103 2023-07-22 22:03:17.000000 nsj_sql_utils_lib-0.0.2/pyproject.toml
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      799 2023-07-22 22:15:35.289628 nsj_sql_utils_lib-0.0.2/setup.cfg
```

### Comparing `nsj_sql_utils_lib-0.0.1/PKG-INFO` & `nsj_sql_utils_lib-0.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nsj_sql_utils_lib
-Version: 0.0.1
+Version: 0.0.2
 Summary: Biblioteca de utilitários Python para facilitar a implementação de sistemas com acesso a banco de dados.
 Home-page: https://github.com/Nasajon/nsj-sql-utils-lib
 Author: Nasajon Sistemas
 Author-email: contact.dev@nasajon.com.br
 Project-URL: Source, https://github.com/Nasajon/nsj-sql-utils-lib
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `nsj_sql_utils_lib-0.0.1/README.md` & `nsj_sql_utils_lib-0.0.2/README.md`

 * *Files identical despite different names*

### Comparing `nsj_sql_utils_lib-0.0.1/nsj_sql_utils_lib/nsj_sql_utils_lib.egg-info/PKG-INFO` & `nsj_sql_utils_lib-0.0.2/nsj_sql_utils_lib.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nsj-sql-utils-lib
-Version: 0.0.1
+Version: 0.0.2
 Summary: Biblioteca de utilitários Python para facilitar a implementação de sistemas com acesso a banco de dados.
 Home-page: https://github.com/Nasajon/nsj-sql-utils-lib
 Author: Nasajon Sistemas
 Author-email: contact.dev@nasajon.com.br
 Project-URL: Source, https://github.com/Nasajon/nsj-sql-utils-lib
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `nsj_sql_utils_lib-0.0.1/setup.cfg` & `nsj_sql_utils_lib-0.0.2/setup.cfg`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = nsj_sql_utils_lib
-version = 0.0.1
+version = 0.0.2
 author = Nasajon Sistemas
 author_email = contact.dev@nasajon.com.br
 description = Biblioteca de utilitários Python para facilitar a implementação de sistemas com acesso a banco de dados.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/Nasajon/nsj-sql-utils-lib
 project_urls = 
@@ -13,20 +13,20 @@
 	Development Status :: 3 - Alpha
 	Intended Audience :: Developers
 	Topic :: Software Development :: Libraries
 	Programming Language :: Python :: 3
 
 [options]
 package_dir = 
-	= nsj_sql_utils_lib
+	= ./
 packages = find:
 python_requires = >=3.4
 install_requires = 
 	psycopg2_binary>=2.9.6
 
 [options.packages.find]
-where = nsj_sql_utils_lib
+where = ./
 
 [egg_info]
 tag_build = 
 tag_date = 0
```

