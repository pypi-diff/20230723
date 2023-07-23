# Comparing `tmp/HawaData-0.8.0.tar.gz` & `tmp/HawaData-0.8.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "HawaData-0.8.0.tar", last modified: Sun Jul 23 08:45:57 2023, max compression
+gzip compressed data, was "HawaData-0.8.1.tar", last modified: Sun Jul 23 08:55:10 2023, max compression
```

## Comparing `HawaData-0.8.0.tar` & `HawaData-0.8.1.tar`

### file list

```diff
@@ -1,38 +1,38 @@
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.486061 HawaData-0.8.0/
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.474141 HawaData-0.8.0/HawaData.egg-info/
--rw-r--r--   0 wangzhou   (501) staff       (20)     3319 2023-07-23 08:45:57.000000 HawaData-0.8.0/HawaData.egg-info/PKG-INFO
--rw-r--r--   0 wangzhou   (501) staff       (20)      584 2023-07-23 08:45:57.000000 HawaData-0.8.0/HawaData.egg-info/SOURCES.txt
--rw-r--r--   0 wangzhou   (501) staff       (20)        1 2023-07-23 08:45:57.000000 HawaData-0.8.0/HawaData.egg-info/dependency_links.txt
--rw-r--r--   0 wangzhou   (501) staff       (20)        5 2023-07-23 08:45:57.000000 HawaData-0.8.0/HawaData.egg-info/top_level.txt
--rw-r--r--   0 wangzhou   (501) staff       (20)     3319 2023-07-23 08:45:57.485782 HawaData-0.8.0/PKG-INFO
--rw-r--r--   0 wangzhou   (501) staff       (20)      669 2022-12-02 07:10:45.000000 HawaData-0.8.0/README.md
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.474790 HawaData-0.8.0/hawa/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:39:05.000000 HawaData-0.8.0/hawa/__init__.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.477488 HawaData-0.8.0/hawa/base/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 05:35:03.000000 HawaData-0.8.0/hawa/base/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     2627 2023-06-19 08:54:42.000000 HawaData-0.8.0/hawa/base/db.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      173 2022-12-01 06:05:08.000000 HawaData-0.8.0/hawa/base/decos.py
--rw-r--r--   0 wangzhou   (501) staff       (20)       98 2023-05-24 07:06:51.000000 HawaData-0.8.0/hawa/base/errors.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      845 2022-12-02 03:09:07.000000 HawaData-0.8.0/hawa/base/init.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.479526 HawaData-0.8.0/hawa/common/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:40:41.000000 HawaData-0.8.0/hawa/common/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)    16225 2023-07-21 07:03:46.000000 HawaData-0.8.0/hawa/common/data.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     6457 2023-07-21 07:00:47.000000 HawaData-0.8.0/hawa/common/query.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     3098 2023-06-19 08:54:42.000000 HawaData-0.8.0/hawa/common/utils.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     2696 2023-06-26 02:08:50.000000 HawaData-0.8.0/hawa/config.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.483212 HawaData-0.8.0/hawa/data/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 08:59:59.000000 HawaData-0.8.0/hawa/data/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      311 2023-05-22 06:36:14.000000 HawaData-0.8.0/hawa/data/city.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      432 2023-05-22 06:36:14.000000 HawaData-0.8.0/hawa/data/district.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     1592 2023-05-23 08:41:21.000000 HawaData-0.8.0/hawa/data/klass.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      711 2023-06-26 06:27:54.000000 HawaData-0.8.0/hawa/data/province.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     1055 2023-07-17 06:57:10.000000 HawaData-0.8.0/hawa/data/school.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     1015 2023-07-19 03:28:20.000000 HawaData-0.8.0/hawa/data/student.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.484493 HawaData-0.8.0/hawa/paper/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 09:27:31.000000 HawaData-0.8.0/hawa/paper/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)    28707 2023-07-23 08:45:55.000000 HawaData-0.8.0/hawa/paper/health.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     5373 2023-07-17 07:05:31.000000 HawaData-0.8.0/hawa/paper/mht.py
--rw-r--r--   0 wangzhou   (501) staff       (20)       38 2023-07-23 08:45:57.486141 HawaData-0.8.0/setup.cfg
--rw-r--r--   0 wangzhou   (501) staff       (20)      879 2023-05-05 08:13:11.000000 HawaData-0.8.0/setup.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:45:57.485092 HawaData-0.8.0/test/
--rw-r--r--   0 wangzhou   (501) staff       (20)     2208 2022-12-08 07:17:34.000000 HawaData-0.8.0/test/test_query.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:55:10.500066 HawaData-0.8.1/
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:55:10.488413 HawaData-0.8.1/HawaData.egg-info/
+-rw-r--r--   0 wangzhou   (501) staff       (20)     3342 2023-07-23 08:55:10.000000 HawaData-0.8.1/HawaData.egg-info/PKG-INFO
+-rw-r--r--   0 wangzhou   (501) staff       (20)      584 2023-07-23 08:55:10.000000 HawaData-0.8.1/HawaData.egg-info/SOURCES.txt
+-rw-r--r--   0 wangzhou   (501) staff       (20)        1 2023-07-23 08:55:10.000000 HawaData-0.8.1/HawaData.egg-info/dependency_links.txt
+-rw-r--r--   0 wangzhou   (501) staff       (20)        5 2023-07-23 08:55:10.000000 HawaData-0.8.1/HawaData.egg-info/top_level.txt
+-rw-r--r--   0 wangzhou   (501) staff       (20)     3342 2023-07-23 08:55:10.499785 HawaData-0.8.1/PKG-INFO
+-rw-r--r--   0 wangzhou   (501) staff       (20)      669 2022-12-02 07:10:45.000000 HawaData-0.8.1/README.md
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:55:10.488937 HawaData-0.8.1/hawa/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:39:05.000000 HawaData-0.8.1/hawa/__init__.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:55:10.491437 HawaData-0.8.1/hawa/base/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 05:35:03.000000 HawaData-0.8.1/hawa/base/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     2627 2023-06-19 08:54:42.000000 HawaData-0.8.1/hawa/base/db.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      173 2022-12-01 06:05:08.000000 HawaData-0.8.1/hawa/base/decos.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)       98 2023-05-24 07:06:51.000000 HawaData-0.8.1/hawa/base/errors.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      845 2022-12-02 03:09:07.000000 HawaData-0.8.1/hawa/base/init.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:55:10.493299 HawaData-0.8.1/hawa/common/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:40:41.000000 HawaData-0.8.1/hawa/common/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)    16330 2023-07-23 08:53:40.000000 HawaData-0.8.1/hawa/common/data.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     6457 2023-07-21 07:00:47.000000 HawaData-0.8.1/hawa/common/query.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     3098 2023-06-19 08:54:42.000000 HawaData-0.8.1/hawa/common/utils.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     2696 2023-06-26 02:08:50.000000 HawaData-0.8.1/hawa/config.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:55:10.497212 HawaData-0.8.1/hawa/data/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 08:59:59.000000 HawaData-0.8.1/hawa/data/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      311 2023-05-22 06:36:14.000000 HawaData-0.8.1/hawa/data/city.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      432 2023-05-22 06:36:14.000000 HawaData-0.8.1/hawa/data/district.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     1592 2023-05-23 08:41:21.000000 HawaData-0.8.1/hawa/data/klass.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      711 2023-06-26 06:27:54.000000 HawaData-0.8.1/hawa/data/province.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     1055 2023-07-17 06:57:10.000000 HawaData-0.8.1/hawa/data/school.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     1015 2023-07-19 03:28:20.000000 HawaData-0.8.1/hawa/data/student.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:55:10.498484 HawaData-0.8.1/hawa/paper/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 09:27:31.000000 HawaData-0.8.1/hawa/paper/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)    28707 2023-07-23 08:45:55.000000 HawaData-0.8.1/hawa/paper/health.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     5373 2023-07-17 07:05:31.000000 HawaData-0.8.1/hawa/paper/mht.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)       38 2023-07-23 08:55:10.500149 HawaData-0.8.1/setup.cfg
+-rw-r--r--   0 wangzhou   (501) staff       (20)      879 2023-05-05 08:13:11.000000 HawaData-0.8.1/setup.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:55:10.499136 HawaData-0.8.1/test/
+-rw-r--r--   0 wangzhou   (501) staff       (20)     2208 2022-12-08 07:17:34.000000 HawaData-0.8.1/test/test_query.py
```

### Comparing `HawaData-0.8.0/HawaData.egg-info/PKG-INFO` & `HawaData-0.8.1/HawaData.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: HawaData
-Version: 0.8.0
+Version: 0.8.1
 Summary: Use For Unified Hawa Data.
 Home-page: https://github.com/StevenLianaL/HawaData
 Author: Steven Wang
 Author-email: brightstar8284@icloud.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Description-Content-Type: text/markdown
@@ -112,7 +112,8 @@
 - 0.7.4 add ch key for dim_field data
 - 0.7.5 add ch key for dim_field data
 - 0.7.6 add ProvinceHealthApiDataLess for cascade schools
 - 0.7.7 add school mht api data
 - 0.7.8 optimization student data
 - 0.7.9 sort dim field
 - 0.8.0 sort dim field
+- 0.8.1 sort dim field
```

### Comparing `HawaData-0.8.0/HawaData.egg-info/SOURCES.txt` & `HawaData-0.8.1/HawaData.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/PKG-INFO` & `HawaData-0.8.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: HawaData
-Version: 0.8.0
+Version: 0.8.1
 Summary: Use For Unified Hawa Data.
 Home-page: https://github.com/StevenLianaL/HawaData
 Author: Steven Wang
 Author-email: brightstar8284@icloud.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Description-Content-Type: text/markdown
@@ -112,7 +112,8 @@
 - 0.7.4 add ch key for dim_field data
 - 0.7.5 add ch key for dim_field data
 - 0.7.6 add ProvinceHealthApiDataLess for cascade schools
 - 0.7.7 add school mht api data
 - 0.7.8 optimization student data
 - 0.7.9 sort dim field
 - 0.8.0 sort dim field
+- 0.8.1 sort dim field
```

### Comparing `HawaData-0.8.0/README.md` & `HawaData-0.8.1/README.md`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/hawa/base/db.py` & `HawaData-0.8.1/hawa/base/db.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/hawa/base/init.py` & `HawaData-0.8.1/hawa/base/init.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/hawa/common/data.py` & `HawaData-0.8.1/hawa/common/data.py`

 * *Files 1% similar despite different names*

```diff
@@ -274,17 +274,18 @@
             count_row_ranks = pd.cut(
                 row, bins=[0, 60, 80, 90, 100], labels=self.rank_names,
                 right=False, include_lowest=True,
             ).value_counts().to_dict()
             sum_value = sum(count_row_ranks.values())
             row_ranks = {k: round(v / sum_value * 100, 2) for k, v in (base_row_ranks | count_row_ranks).items()}
             res[c] = row_ranks
-
+        code_map = self.get_dim_field_order(key=item_code)
         return {
-            "data": res, "codes": codes, "legend": self.rank_names,
+            "data": res, "codes": sorted(codes, key=lambda x: code_map[x]),
+            "legend": self.rank_names,
         }
 
     def count_sub_units(self, target_level: str = 'school'):
         """查询下辖单位"""
         match target_level:
             case 'school':
                 return self.school_ids
```

### Comparing `HawaData-0.8.0/hawa/common/query.py` & `HawaData-0.8.1/hawa/common/query.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/hawa/common/utils.py` & `HawaData-0.8.1/hawa/common/utils.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/hawa/config.py` & `HawaData-0.8.1/hawa/config.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/hawa/data/klass.py` & `HawaData-0.8.1/hawa/data/klass.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/hawa/data/province.py` & `HawaData-0.8.1/hawa/data/province.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/hawa/data/school.py` & `HawaData-0.8.1/hawa/data/school.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/hawa/data/student.py` & `HawaData-0.8.1/hawa/data/student.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/hawa/paper/health.py` & `HawaData-0.8.1/hawa/paper/health.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/hawa/paper/mht.py` & `HawaData-0.8.1/hawa/paper/mht.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/setup.py` & `HawaData-0.8.1/setup.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.8.0/test/test_query.py` & `HawaData-0.8.1/test/test_query.py`

 * *Files identical despite different names*

