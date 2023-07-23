# Comparing `tmp/TiamoTools-1.0.1.tar.gz` & `tmp/TiamoTools-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "TiamoTools-1.0.1.tar", last modified: Sun Jul 23 05:30:19 2023, max compression
+gzip compressed data, was "TiamoTools-1.0.2.tar", last modified: Sun Jul 23 07:06:48 2023, max compression
```

## Comparing `TiamoTools-1.0.1.tar` & `TiamoTools-1.0.2.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 05:30:19.365390 TiamoTools-1.0.1/
--rw-rw-rw-   0        0        0      539 2023-07-23 05:30:19.365390 TiamoTools-1.0.1/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-07-23 05:30:19.355888 TiamoTools-1.0.1/TiamoTools/
--rw-rw-rw-   0        0        0      302 2023-07-23 05:30:14.000000 TiamoTools-1.0.1/TiamoTools/__init__.py
--rw-rw-rw-   0        0        0     1584 2023-07-21 04:29:35.000000 TiamoTools-1.0.1/TiamoTools/common.py
--rw-rw-rw-   0        0        0     4802 2023-07-22 14:51:17.000000 TiamoTools-1.0.1/TiamoTools/dtime.py
--rw-rw-rw-   0        0        0      371 2023-07-23 03:52:21.000000 TiamoTools-1.0.1/TiamoTools/error.py
--rw-rw-rw-   0        0        0     1379 2023-07-23 03:43:42.000000 TiamoTools-1.0.1/TiamoTools/log.py
--rw-rw-rw-   0        0        0     4347 2023-07-23 03:52:21.000000 TiamoTools-1.0.1/TiamoTools/mongo.py
--rw-rw-rw-   0        0        0      532 2023-07-23 04:24:35.000000 TiamoTools-1.0.1/TiamoTools/mysql.py
--rw-rw-rw-   0        0        0      906 2023-07-23 03:52:21.000000 TiamoTools-1.0.1/TiamoTools/oracle.py
--rw-rw-rw-   0        0        0     2792 2023-07-23 04:24:35.000000 TiamoTools-1.0.1/TiamoTools/sql_db_base.py
-drwxrwxrwx   0        0        0        0 2023-07-23 05:30:19.365390 TiamoTools-1.0.1/TiamoTools/xgcondb/
--rw-rw-rw-   0        0        0     1817 2023-05-05 06:17:18.000000 TiamoTools-1.0.1/TiamoTools/xgcondb/__init__.py
--rw-rw-rw-   0        0        0      787 2023-07-23 03:52:21.000000 TiamoTools-1.0.1/TiamoTools/xugu.py
-drwxrwxrwx   0        0        0        0 2023-07-23 05:30:19.365390 TiamoTools-1.0.1/TiamoTools.egg-info/
--rw-rw-rw-   0        0        0      539 2023-07-23 05:30:19.000000 TiamoTools-1.0.1/TiamoTools.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      416 2023-07-23 05:30:19.000000 TiamoTools-1.0.1/TiamoTools.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 05:30:19.000000 TiamoTools-1.0.1/TiamoTools.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       47 2023-07-23 05:30:19.000000 TiamoTools-1.0.1/TiamoTools.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-07-23 05:30:19.000000 TiamoTools-1.0.1/TiamoTools.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 05:30:19.365390 TiamoTools-1.0.1/setup.cfg
--rw-rw-rw-   0        0        0      897 2023-07-23 05:30:14.000000 TiamoTools-1.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:06:48.928480 TiamoTools-1.0.2/
+-rw-rw-rw-   0        0        0      539 2023-07-23 07:06:48.928480 TiamoTools-1.0.2/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-07-23 07:06:48.921501 TiamoTools-1.0.2/TiamoTools/
+-rw-rw-rw-   0        0        0      302 2023-07-23 07:02:34.000000 TiamoTools-1.0.2/TiamoTools/__init__.py
+-rw-rw-rw-   0        0        0     1584 2023-07-21 04:29:35.000000 TiamoTools-1.0.2/TiamoTools/common.py
+-rw-rw-rw-   0        0        0     4802 2023-07-22 14:51:17.000000 TiamoTools-1.0.2/TiamoTools/dtime.py
+-rw-rw-rw-   0        0        0      371 2023-07-23 03:52:21.000000 TiamoTools-1.0.2/TiamoTools/error.py
+-rw-rw-rw-   0        0        0     1379 2023-07-23 03:43:42.000000 TiamoTools-1.0.2/TiamoTools/log.py
+-rw-rw-rw-   0        0        0     4351 2023-07-23 07:00:55.000000 TiamoTools-1.0.2/TiamoTools/mongo.py
+-rw-rw-rw-   0        0        0      532 2023-07-23 04:24:35.000000 TiamoTools-1.0.2/TiamoTools/mysql.py
+-rw-rw-rw-   0        0        0      906 2023-07-23 03:52:21.000000 TiamoTools-1.0.2/TiamoTools/oracle.py
+-rw-rw-rw-   0        0        0     2792 2023-07-23 04:24:35.000000 TiamoTools-1.0.2/TiamoTools/sql_db_base.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:06:48.926487 TiamoTools-1.0.2/TiamoTools/xgcondb/
+-rw-rw-rw-   0        0        0     1817 2023-05-05 06:17:18.000000 TiamoTools-1.0.2/TiamoTools/xgcondb/__init__.py
+-rw-rw-rw-   0        0        0      787 2023-07-23 03:52:21.000000 TiamoTools-1.0.2/TiamoTools/xugu.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:06:48.926487 TiamoTools-1.0.2/TiamoTools.egg-info/
+-rw-rw-rw-   0        0        0      539 2023-07-23 07:06:48.000000 TiamoTools-1.0.2/TiamoTools.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      416 2023-07-23 07:06:48.000000 TiamoTools-1.0.2/TiamoTools.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 07:06:48.000000 TiamoTools-1.0.2/TiamoTools.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       47 2023-07-23 07:06:48.000000 TiamoTools-1.0.2/TiamoTools.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 07:06:48.000000 TiamoTools-1.0.2/TiamoTools.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 07:06:48.928480 TiamoTools-1.0.2/setup.cfg
+-rw-rw-rw-   0        0        0      875 2023-07-23 07:06:45.000000 TiamoTools-1.0.2/setup.py
```

### Comparing `TiamoTools-1.0.1/PKG-INFO` & `TiamoTools-1.0.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 Metadata-Version: 1.2
 Name: TiamoTools
-Version: 1.0.1
+Version: 1.0.2
 Summary: 简化数据库连接、时间处理及log声明
 Home-page: UNKNOWN
 Author: wyl
 Author-email: <321081840@qq.com>
 License: UNKNOWN
 Description: 数据库：mongo、mysql、oracle、xugu；时间：格式化、转换、计算；log：声明
 Keywords: python,super,tools
 Platform: UNKNOWN
 Classifier: Intended Audience :: Developers
 Classifier: Programming Language :: Python :: 3.8
-Requires: cx_Oracle
 Requires: PyMySQL
 Requires: pymongo
+Requires: cx_Oracle
 Requires-Python: >=3.8
```

### Comparing `TiamoTools-1.0.1/TiamoTools/common.py` & `TiamoTools-1.0.2/TiamoTools/common.py`

 * *Files identical despite different names*

### Comparing `TiamoTools-1.0.1/TiamoTools/dtime.py` & `TiamoTools-1.0.2/TiamoTools/dtime.py`

 * *Files identical despite different names*

### Comparing `TiamoTools-1.0.1/TiamoTools/log.py` & `TiamoTools-1.0.2/TiamoTools/log.py`

 * *Files identical despite different names*

### Comparing `TiamoTools-1.0.1/TiamoTools/mongo.py` & `TiamoTools-1.0.2/TiamoTools/mongo.py`

 * *Files 0% similar despite different names*

```diff
@@ -96,15 +96,16 @@
 
         :param table: 目标数据表
         :param filter_query: 查询query
         :param set_query: 数据query
         :return: result
         """
         db = self.db[table]
-        return db.update_one(filter=filter_query, set_query=set_query, upsert=True)
+        db.update()
+        return db.update_one(filter_query, set_query, upsert=True)
 
     @retry_result
     def update_many(self, table: str, bulk_query: List[List[dict]]):
         """
         多约束多数据更新操作，查询到约束条件则更新，否则执行插入操作
 
         tips1: [[{'sex': '男'}, {'$set': {'is_qualified': False}}],...]
```

### Comparing `TiamoTools-1.0.1/TiamoTools/mysql.py` & `TiamoTools-1.0.2/TiamoTools/mysql.py`

 * *Files identical despite different names*

### Comparing `TiamoTools-1.0.1/TiamoTools/oracle.py` & `TiamoTools-1.0.2/TiamoTools/oracle.py`

 * *Files identical despite different names*

### Comparing `TiamoTools-1.0.1/TiamoTools/sql_db_base.py` & `TiamoTools-1.0.2/TiamoTools/sql_db_base.py`

 * *Files identical despite different names*

### Comparing `TiamoTools-1.0.1/TiamoTools/xgcondb/__init__.py` & `TiamoTools-1.0.2/TiamoTools/xgcondb/__init__.py`

 * *Files identical despite different names*

### Comparing `TiamoTools-1.0.1/TiamoTools/xugu.py` & `TiamoTools-1.0.2/TiamoTools/xugu.py`

 * *Files identical despite different names*

### Comparing `TiamoTools-1.0.1/TiamoTools.egg-info/PKG-INFO` & `TiamoTools-1.0.2/TiamoTools.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 Metadata-Version: 1.2
 Name: TiamoTools
-Version: 1.0.1
+Version: 1.0.2
 Summary: 简化数据库连接、时间处理及log声明
 Home-page: UNKNOWN
 Author: wyl
 Author-email: <321081840@qq.com>
 License: UNKNOWN
 Description: 数据库：mongo、mysql、oracle、xugu；时间：格式化、转换、计算；log：声明
 Keywords: python,super,tools
 Platform: UNKNOWN
 Classifier: Intended Audience :: Developers
 Classifier: Programming Language :: Python :: 3.8
-Requires: cx_Oracle
 Requires: PyMySQL
 Requires: pymongo
+Requires: cx_Oracle
 Requires-Python: >=3.8
```

### Comparing `TiamoTools-1.0.1/setup.py` & `TiamoTools-1.0.2/setup.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,34 +1,33 @@
 from setuptools import setup, find_packages
 
 
-VERSION = '1.0.1'
+VERSION = '1.0.2'
 DESCRIPTION = '简化数据库连接、时间处理及log声明'
 LONG_DESCRIPTION = '数据库：mongo、mysql、oracle、xugu；时间：格式化、转换、计算；log：声明'
 
 # 配置
 setup(
     name='TiamoTools',
     version=VERSION,
     author='wyl',
     author_email='<321081840@qq.com>',
     description=DESCRIPTION,
     long_description=LONG_DESCRIPTION,
     packages=find_packages(),
-    include_dirs=[],
     python_requires='>=3.8',
     requires=[
-        'cx_Oracle',
         'PyMySQL',
-        'pymongo'
+        'pymongo',
+        'cx_Oracle'
     ],
     install_requires=[
-        'cx_Oracle>=8.3.0',
         'PyMySQL>=1.0.2',
-        'pymongo>=3.8.0'
+        'pymongo>=3.8.0',
+        'cx_Oracle>=8.3.0'
     ],
     keywords=['python', 'super', 'tools'],
     classifiers=[
         'Intended Audience :: Developers',
         'Programming Language :: Python :: 3.8'
     ]
 )
```

