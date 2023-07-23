# Comparing `tmp/HawaData-0.7.9.tar.gz` & `tmp/HawaData-0.8.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "HawaData-0.7.9.tar", last modified: Sun Jul 23 08:36:35 2023, max compression
+gzip compressed data, was "HawaData-0.8.0.tar", last modified: Sun Jul 23 08:45:57 2023, max compression
```

## Comparing `HawaData-0.7.9.tar` & `HawaData-0.8.0.tar`

### file list

```diff
@@ -1,38 +1,38 @@
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.143776 HawaData-0.7.9/
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.128074 HawaData-0.7.9/HawaData.egg-info/
--rw-r--r--   0 wangzhou   (501) staff       (20)     3296 2023-07-23 08:36:35.000000 HawaData-0.7.9/HawaData.egg-info/PKG-INFO
--rw-r--r--   0 wangzhou   (501) staff       (20)      584 2023-07-23 08:36:35.000000 HawaData-0.7.9/HawaData.egg-info/SOURCES.txt
--rw-r--r--   0 wangzhou   (501) staff       (20)        1 2023-07-23 08:36:35.000000 HawaData-0.7.9/HawaData.egg-info/dependency_links.txt
--rw-r--r--   0 wangzhou   (501) staff       (20)        5 2023-07-23 08:36:35.000000 HawaData-0.7.9/HawaData.egg-info/top_level.txt
--rw-r--r--   0 wangzhou   (501) staff       (20)     3296 2023-07-23 08:36:35.143414 HawaData-0.7.9/PKG-INFO
--rw-r--r--   0 wangzhou   (501) staff       (20)      669 2022-12-02 07:10:45.000000 HawaData-0.7.9/README.md
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.128605 HawaData-0.7.9/hawa/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:39:05.000000 HawaData-0.7.9/hawa/__init__.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.132874 HawaData-0.7.9/hawa/base/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 05:35:03.000000 HawaData-0.7.9/hawa/base/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     2627 2023-06-19 08:54:42.000000 HawaData-0.7.9/hawa/base/db.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      173 2022-12-01 06:05:08.000000 HawaData-0.7.9/hawa/base/decos.py
--rw-r--r--   0 wangzhou   (501) staff       (20)       98 2023-05-24 07:06:51.000000 HawaData-0.7.9/hawa/base/errors.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      845 2022-12-02 03:09:07.000000 HawaData-0.7.9/hawa/base/init.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.135828 HawaData-0.7.9/hawa/common/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:40:41.000000 HawaData-0.7.9/hawa/common/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)    16225 2023-07-21 07:03:46.000000 HawaData-0.7.9/hawa/common/data.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     6457 2023-07-21 07:00:47.000000 HawaData-0.7.9/hawa/common/query.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     3098 2023-06-19 08:54:42.000000 HawaData-0.7.9/hawa/common/utils.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     2696 2023-06-26 02:08:50.000000 HawaData-0.7.9/hawa/config.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.140677 HawaData-0.7.9/hawa/data/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 08:59:59.000000 HawaData-0.7.9/hawa/data/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      311 2023-05-22 06:36:14.000000 HawaData-0.7.9/hawa/data/city.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      432 2023-05-22 06:36:14.000000 HawaData-0.7.9/hawa/data/district.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     1592 2023-05-23 08:41:21.000000 HawaData-0.7.9/hawa/data/klass.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      711 2023-06-26 06:27:54.000000 HawaData-0.7.9/hawa/data/province.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     1055 2023-07-17 06:57:10.000000 HawaData-0.7.9/hawa/data/school.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     1015 2023-07-19 03:28:20.000000 HawaData-0.7.9/hawa/data/student.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.142139 HawaData-0.7.9/hawa/paper/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 09:27:31.000000 HawaData-0.7.9/hawa/paper/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)    28525 2023-07-23 08:27:55.000000 HawaData-0.7.9/hawa/paper/health.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     5373 2023-07-17 07:05:31.000000 HawaData-0.7.9/hawa/paper/mht.py
--rw-r--r--   0 wangzhou   (501) staff       (20)       38 2023-07-23 08:36:35.143875 HawaData-0.7.9/setup.cfg
--rw-r--r--   0 wangzhou   (501) staff       (20)      879 2023-05-05 08:13:11.000000 HawaData-0.7.9/setup.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.142737 HawaData-0.7.9/test/
--rw-r--r--   0 wangzhou   (501) staff       (20)     2208 2022-12-08 07:17:34.000000 HawaData-0.7.9/test/test_query.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.486061 HawaData-0.8.0/
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.474141 HawaData-0.8.0/HawaData.egg-info/
+-rw-r--r--   0 wangzhou   (501) staff       (20)     3319 2023-07-23 08:45:57.000000 HawaData-0.8.0/HawaData.egg-info/PKG-INFO
+-rw-r--r--   0 wangzhou   (501) staff       (20)      584 2023-07-23 08:45:57.000000 HawaData-0.8.0/HawaData.egg-info/SOURCES.txt
+-rw-r--r--   0 wangzhou   (501) staff       (20)        1 2023-07-23 08:45:57.000000 HawaData-0.8.0/HawaData.egg-info/dependency_links.txt
+-rw-r--r--   0 wangzhou   (501) staff       (20)        5 2023-07-23 08:45:57.000000 HawaData-0.8.0/HawaData.egg-info/top_level.txt
+-rw-r--r--   0 wangzhou   (501) staff       (20)     3319 2023-07-23 08:45:57.485782 HawaData-0.8.0/PKG-INFO
+-rw-r--r--   0 wangzhou   (501) staff       (20)      669 2022-12-02 07:10:45.000000 HawaData-0.8.0/README.md
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.474790 HawaData-0.8.0/hawa/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:39:05.000000 HawaData-0.8.0/hawa/__init__.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.477488 HawaData-0.8.0/hawa/base/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 05:35:03.000000 HawaData-0.8.0/hawa/base/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     2627 2023-06-19 08:54:42.000000 HawaData-0.8.0/hawa/base/db.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      173 2022-12-01 06:05:08.000000 HawaData-0.8.0/hawa/base/decos.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)       98 2023-05-24 07:06:51.000000 HawaData-0.8.0/hawa/base/errors.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      845 2022-12-02 03:09:07.000000 HawaData-0.8.0/hawa/base/init.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.479526 HawaData-0.8.0/hawa/common/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:40:41.000000 HawaData-0.8.0/hawa/common/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)    16225 2023-07-21 07:03:46.000000 HawaData-0.8.0/hawa/common/data.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     6457 2023-07-21 07:00:47.000000 HawaData-0.8.0/hawa/common/query.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     3098 2023-06-19 08:54:42.000000 HawaData-0.8.0/hawa/common/utils.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     2696 2023-06-26 02:08:50.000000 HawaData-0.8.0/hawa/config.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.483212 HawaData-0.8.0/hawa/data/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 08:59:59.000000 HawaData-0.8.0/hawa/data/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      311 2023-05-22 06:36:14.000000 HawaData-0.8.0/hawa/data/city.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      432 2023-05-22 06:36:14.000000 HawaData-0.8.0/hawa/data/district.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     1592 2023-05-23 08:41:21.000000 HawaData-0.8.0/hawa/data/klass.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      711 2023-06-26 06:27:54.000000 HawaData-0.8.0/hawa/data/province.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     1055 2023-07-17 06:57:10.000000 HawaData-0.8.0/hawa/data/school.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     1015 2023-07-19 03:28:20.000000 HawaData-0.8.0/hawa/data/student.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.484493 HawaData-0.8.0/hawa/paper/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 09:27:31.000000 HawaData-0.8.0/hawa/paper/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)    28707 2023-07-23 08:45:55.000000 HawaData-0.8.0/hawa/paper/health.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     5373 2023-07-17 07:05:31.000000 HawaData-0.8.0/hawa/paper/mht.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)       38 2023-07-23 08:45:57.486141 HawaData-0.8.0/setup.cfg
+-rw-r--r--   0 wangzhou   (501) staff       (20)      879 2023-05-05 08:13:11.000000 HawaData-0.8.0/setup.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.485092 HawaData-0.8.0/test/
+-rw-r--r--   0 wangzhou   (501) staff       (20)     2208 2022-12-08 07:17:34.000000 HawaData-0.8.0/test/test_query.py
```

### Comparing `HawaData-0.7.9/HawaData.egg-info/PKG-INFO` & `HawaData-0.8.0/HawaData.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: HawaData
-Version: 0.7.9
+Version: 0.8.0
 Summary: Use For Unified Hawa Data.
 Home-page: https://github.com/StevenLianaL/HawaData
 Author: Steven Wang
 Author-email: brightstar8284@icloud.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Description-Content-Type: text/markdown
@@ -111,7 +111,8 @@
 - 0.7.3 add is_leaf to cascade students
 - 0.7.4 add ch key for dim_field data
 - 0.7.5 add ch key for dim_field data
 - 0.7.6 add ProvinceHealthApiDataLess for cascade schools
 - 0.7.7 add school mht api data
 - 0.7.8 optimization student data
 - 0.7.9 sort dim field
+- 0.8.0 sort dim field
```

### Comparing `HawaData-0.7.9/HawaData.egg-info/SOURCES.txt` & `HawaData-0.8.0/HawaData.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/PKG-INFO` & `HawaData-0.8.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: HawaData
-Version: 0.7.9
+Version: 0.8.0
 Summary: Use For Unified Hawa Data.
 Home-page: https://github.com/StevenLianaL/HawaData
 Author: Steven Wang
 Author-email: brightstar8284@icloud.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Description-Content-Type: text/markdown
@@ -111,7 +111,8 @@
 - 0.7.3 add is_leaf to cascade students
 - 0.7.4 add ch key for dim_field data
 - 0.7.5 add ch key for dim_field data
 - 0.7.6 add ProvinceHealthApiDataLess for cascade schools
 - 0.7.7 add school mht api data
 - 0.7.8 optimization student data
 - 0.7.9 sort dim field
+- 0.8.0 sort dim field
```

### Comparing `HawaData-0.7.9/README.md` & `HawaData-0.8.0/README.md`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/hawa/base/db.py` & `HawaData-0.8.0/hawa/base/db.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/hawa/base/init.py` & `HawaData-0.8.0/hawa/base/init.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/hawa/common/data.py` & `HawaData-0.8.0/hawa/common/data.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/hawa/common/query.py` & `HawaData-0.8.0/hawa/common/query.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/hawa/common/utils.py` & `HawaData-0.8.0/hawa/common/utils.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/hawa/config.py` & `HawaData-0.8.0/hawa/config.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/hawa/data/klass.py` & `HawaData-0.8.0/hawa/data/klass.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/hawa/data/province.py` & `HawaData-0.8.0/hawa/data/province.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/hawa/data/school.py` & `HawaData-0.8.0/hawa/data/school.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/hawa/data/student.py` & `HawaData-0.8.0/hawa/data/student.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/hawa/paper/health.py` & `HawaData-0.8.0/hawa/paper/health.py`

 * *Files 1% similar despite different names*

```diff
@@ -143,14 +143,17 @@
             keys.append(code)
             values.append(score)
             mapping[code] = score
         match res_format:
             case 'dict':
                 return mapping
             case 'list':
+                code_map = self.get_dim_field_order(key=item_code)
+                keys = sorted(keys, key=lambda x: code_map[x])
+                values = [mapping[k] for k in keys]
                 return keys, values
 
 
 @dataclass
 class HealthReportData(HealthData):
     # 计算数据
     code_scores: pd.DataFrame = field(default_factory=pd.DataFrame)
```

### Comparing `HawaData-0.7.9/hawa/paper/mht.py` & `HawaData-0.8.0/hawa/paper/mht.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/setup.py` & `HawaData-0.8.0/setup.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.9/test/test_query.py` & `HawaData-0.8.0/test/test_query.py`

 * *Files identical despite different names*

