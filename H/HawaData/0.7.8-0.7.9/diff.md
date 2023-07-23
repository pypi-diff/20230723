# Comparing `tmp/HawaData-0.7.8.tar.gz` & `tmp/HawaData-0.7.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "HawaData-0.7.8.tar", last modified: Wed Jul 19 03:31:19 2023, max compression
+gzip compressed data, was "HawaData-0.7.9.tar", last modified: Sun Jul 23 08:36:35 2023, max compression
```

## Comparing `HawaData-0.7.8.tar` & `HawaData-0.7.9.tar`

### file list

```diff
@@ -1,38 +1,38 @@
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-19 03:31:19.335677 HawaData-0.7.8/
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-19 03:31:19.321685 HawaData-0.7.8/HawaData.egg-info/
--rw-r--r--   0 wangzhou   (501) staff       (20)     3273 2023-07-19 03:31:19.000000 HawaData-0.7.8/HawaData.egg-info/PKG-INFO
--rw-r--r--   0 wangzhou   (501) staff       (20)      584 2023-07-19 03:31:19.000000 HawaData-0.7.8/HawaData.egg-info/SOURCES.txt
--rw-r--r--   0 wangzhou   (501) staff       (20)        1 2023-07-19 03:31:19.000000 HawaData-0.7.8/HawaData.egg-info/dependency_links.txt
--rw-r--r--   0 wangzhou   (501) staff       (20)        5 2023-07-19 03:31:19.000000 HawaData-0.7.8/HawaData.egg-info/top_level.txt
--rw-r--r--   0 wangzhou   (501) staff       (20)     3273 2023-07-19 03:31:19.335390 HawaData-0.7.8/PKG-INFO
--rw-r--r--   0 wangzhou   (501) staff       (20)      669 2022-12-02 07:10:45.000000 HawaData-0.7.8/README.md
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-19 03:31:19.322294 HawaData-0.7.8/hawa/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:39:05.000000 HawaData-0.7.8/hawa/__init__.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-19 03:31:19.325497 HawaData-0.7.8/hawa/base/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 05:35:03.000000 HawaData-0.7.8/hawa/base/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     2627 2023-06-19 08:54:42.000000 HawaData-0.7.8/hawa/base/db.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      173 2022-12-01 06:05:08.000000 HawaData-0.7.8/hawa/base/decos.py
--rw-r--r--   0 wangzhou   (501) staff       (20)       98 2023-05-24 07:06:51.000000 HawaData-0.7.8/hawa/base/errors.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      845 2022-12-02 03:09:07.000000 HawaData-0.7.8/hawa/base/init.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-19 03:31:19.327809 HawaData-0.7.8/hawa/common/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:40:41.000000 HawaData-0.7.8/hawa/common/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)    15412 2023-07-17 07:06:20.000000 HawaData-0.7.8/hawa/common/data.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     6268 2023-07-19 03:27:45.000000 HawaData-0.7.8/hawa/common/query.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     3098 2023-06-19 08:54:42.000000 HawaData-0.7.8/hawa/common/utils.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     2696 2023-06-26 02:08:50.000000 HawaData-0.7.8/hawa/config.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-19 03:31:19.332352 HawaData-0.7.8/hawa/data/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 08:59:59.000000 HawaData-0.7.8/hawa/data/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      311 2023-05-22 06:36:14.000000 HawaData-0.7.8/hawa/data/city.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      432 2023-05-22 06:36:14.000000 HawaData-0.7.8/hawa/data/district.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     1592 2023-05-23 08:41:21.000000 HawaData-0.7.8/hawa/data/klass.py
--rw-r--r--   0 wangzhou   (501) staff       (20)      711 2023-06-26 06:27:54.000000 HawaData-0.7.8/hawa/data/province.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     1055 2023-07-17 06:57:10.000000 HawaData-0.7.8/hawa/data/school.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     1015 2023-07-19 03:28:20.000000 HawaData-0.7.8/hawa/data/student.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-19 03:31:19.333976 HawaData-0.7.8/hawa/paper/
--rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 09:27:31.000000 HawaData-0.7.8/hawa/paper/__init__.py
--rw-r--r--   0 wangzhou   (501) staff       (20)    28407 2023-06-26 01:39:47.000000 HawaData-0.7.8/hawa/paper/health.py
--rw-r--r--   0 wangzhou   (501) staff       (20)     5373 2023-07-17 07:05:31.000000 HawaData-0.7.8/hawa/paper/mht.py
--rw-r--r--   0 wangzhou   (501) staff       (20)       38 2023-07-19 03:31:19.335756 HawaData-0.7.8/setup.cfg
--rw-r--r--   0 wangzhou   (501) staff       (20)      879 2023-05-05 08:13:11.000000 HawaData-0.7.8/setup.py
-drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-19 03:31:19.334667 HawaData-0.7.8/test/
--rw-r--r--   0 wangzhou   (501) staff       (20)     2208 2022-12-08 07:17:34.000000 HawaData-0.7.8/test/test_query.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.143776 HawaData-0.7.9/
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.128074 HawaData-0.7.9/HawaData.egg-info/
+-rw-r--r--   0 wangzhou   (501) staff       (20)     3296 2023-07-23 08:36:35.000000 HawaData-0.7.9/HawaData.egg-info/PKG-INFO
+-rw-r--r--   0 wangzhou   (501) staff       (20)      584 2023-07-23 08:36:35.000000 HawaData-0.7.9/HawaData.egg-info/SOURCES.txt
+-rw-r--r--   0 wangzhou   (501) staff       (20)        1 2023-07-23 08:36:35.000000 HawaData-0.7.9/HawaData.egg-info/dependency_links.txt
+-rw-r--r--   0 wangzhou   (501) staff       (20)        5 2023-07-23 08:36:35.000000 HawaData-0.7.9/HawaData.egg-info/top_level.txt
+-rw-r--r--   0 wangzhou   (501) staff       (20)     3296 2023-07-23 08:36:35.143414 HawaData-0.7.9/PKG-INFO
+-rw-r--r--   0 wangzhou   (501) staff       (20)      669 2022-12-02 07:10:45.000000 HawaData-0.7.9/README.md
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.128605 HawaData-0.7.9/hawa/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:39:05.000000 HawaData-0.7.9/hawa/__init__.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.132874 HawaData-0.7.9/hawa/base/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 05:35:03.000000 HawaData-0.7.9/hawa/base/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     2627 2023-06-19 08:54:42.000000 HawaData-0.7.9/hawa/base/db.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      173 2022-12-01 06:05:08.000000 HawaData-0.7.9/hawa/base/decos.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)       98 2023-05-24 07:06:51.000000 HawaData-0.7.9/hawa/base/errors.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      845 2022-12-02 03:09:07.000000 HawaData-0.7.9/hawa/base/init.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.135828 HawaData-0.7.9/hawa/common/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-11-30 09:40:41.000000 HawaData-0.7.9/hawa/common/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)    16225 2023-07-21 07:03:46.000000 HawaData-0.7.9/hawa/common/data.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     6457 2023-07-21 07:00:47.000000 HawaData-0.7.9/hawa/common/query.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     3098 2023-06-19 08:54:42.000000 HawaData-0.7.9/hawa/common/utils.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     2696 2023-06-26 02:08:50.000000 HawaData-0.7.9/hawa/config.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.140677 HawaData-0.7.9/hawa/data/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 08:59:59.000000 HawaData-0.7.9/hawa/data/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      311 2023-05-22 06:36:14.000000 HawaData-0.7.9/hawa/data/city.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      432 2023-05-22 06:36:14.000000 HawaData-0.7.9/hawa/data/district.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     1592 2023-05-23 08:41:21.000000 HawaData-0.7.9/hawa/data/klass.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)      711 2023-06-26 06:27:54.000000 HawaData-0.7.9/hawa/data/province.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     1055 2023-07-17 06:57:10.000000 HawaData-0.7.9/hawa/data/school.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     1015 2023-07-19 03:28:20.000000 HawaData-0.7.9/hawa/data/student.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.142139 HawaData-0.7.9/hawa/paper/
+-rw-r--r--   0 wangzhou   (501) staff       (20)        0 2022-12-01 09:27:31.000000 HawaData-0.7.9/hawa/paper/__init__.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)    28525 2023-07-23 08:27:55.000000 HawaData-0.7.9/hawa/paper/health.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)     5373 2023-07-17 07:05:31.000000 HawaData-0.7.9/hawa/paper/mht.py
+-rw-r--r--   0 wangzhou   (501) staff       (20)       38 2023-07-23 08:36:35.143875 HawaData-0.7.9/setup.cfg
+-rw-r--r--   0 wangzhou   (501) staff       (20)      879 2023-05-05 08:13:11.000000 HawaData-0.7.9/setup.py
+drwxr-xr-x   0 wangzhou   (501) staff       (20)        0 2023-07-23 08:36:35.142737 HawaData-0.7.9/test/
+-rw-r--r--   0 wangzhou   (501) staff       (20)     2208 2022-12-08 07:17:34.000000 HawaData-0.7.9/test/test_query.py
```

### Comparing `HawaData-0.7.8/HawaData.egg-info/PKG-INFO` & `HawaData-0.7.9/HawaData.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: HawaData
-Version: 0.7.8
+Version: 0.7.9
 Summary: Use For Unified Hawa Data.
 Home-page: https://github.com/StevenLianaL/HawaData
 Author: Steven Wang
 Author-email: brightstar8284@icloud.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Description-Content-Type: text/markdown
@@ -110,7 +110,8 @@
 - 0.7.2 add cascade students
 - 0.7.3 add is_leaf to cascade students
 - 0.7.4 add ch key for dim_field data
 - 0.7.5 add ch key for dim_field data
 - 0.7.6 add ProvinceHealthApiDataLess for cascade schools
 - 0.7.7 add school mht api data
 - 0.7.8 optimization student data
+- 0.7.9 sort dim field
```

### Comparing `HawaData-0.7.8/HawaData.egg-info/SOURCES.txt` & `HawaData-0.7.9/HawaData.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/PKG-INFO` & `HawaData-0.7.9/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: HawaData
-Version: 0.7.8
+Version: 0.7.9
 Summary: Use For Unified Hawa Data.
 Home-page: https://github.com/StevenLianaL/HawaData
 Author: Steven Wang
 Author-email: brightstar8284@icloud.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Description-Content-Type: text/markdown
@@ -110,7 +110,8 @@
 - 0.7.2 add cascade students
 - 0.7.3 add is_leaf to cascade students
 - 0.7.4 add ch key for dim_field data
 - 0.7.5 add ch key for dim_field data
 - 0.7.6 add ProvinceHealthApiDataLess for cascade schools
 - 0.7.7 add school mht api data
 - 0.7.8 optimization student data
+- 0.7.9 sort dim field
```

### Comparing `HawaData-0.7.8/README.md` & `HawaData-0.7.9/README.md`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/hawa/base/db.py` & `HawaData-0.7.9/hawa/base/db.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/hawa/base/init.py` & `HawaData-0.7.9/hawa/base/init.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/hawa/common/data.py` & `HawaData-0.7.9/hawa/common/data.py`

 * *Files 3% similar despite different names*

```diff
@@ -46,14 +46,16 @@
     query: ClassVar[DataQuery] = None
 
     # 原始数据
 
     school_ids: list[int] = field(default_factory=list)
     schools: pd.DataFrame = field(default_factory=pd.DataFrame)
 
+    codebook: pd.DataFrame = field(default_factory=pd.DataFrame)
+
     cases: pd.DataFrame = field(default_factory=pd.DataFrame)
     case_ids: list[int] = field(default_factory=list)
     case_project_ids: Counter = field(default_factory=Counter)
 
     answers: pd.DataFrame = field(default_factory=pd.DataFrame)
 
     students: pd.DataFrame = field(default_factory=pd.DataFrame)
@@ -152,14 +154,23 @@
         project.logger.debug(f'students: {self.student_count}')
 
     def _to_init_g_items(self):
         self.item_ids = set(self.answers['item_id'].drop_duplicates())
         self.items = self.query.query_items(self.item_ids)
         project.logger.debug(f'items: {len(self.items)}')
 
+    def _to_init_z_dim_field(self):
+        cache_key = f"{project.PROJECT}:codebook"
+        if data := self.redis.conn.get(cache_key):
+            self.codebook = pd.DataFrame.from_records(json.loads(data))
+        else:
+            self.codebook = self.query.query_codebook()
+            cache_data = self.codebook.to_json(orient='records', force_ascii=False)
+            self.redis.conn.set(cache_key, cache_data, ex=60 * 60 * 24 * 7)
+
     def _to_build_helper(self):
         self.grade = GradeData(case_ids=self.case_ids)
         self.case = CaseData(cases=self.cases)
 
     def _to_count_a_final_answers(self):
         items = {k: {} for k in self.code_word_list}
         item_codes = self.query.query_item_codes(self.item_ids)
@@ -370,7 +381,15 @@
                         s_row = {
                             'label': s['name'], 'value': s['id'], "is_leaf": True
                         }
                         d_row['children'].append(s_row)
                     p_row['children'].append(d_row)
                 res.append(p_row)
         return res
+
+    def get_dim_field_order(self, key: str):
+        """获取维度/领域顺序的映射
+        :param key: dimension/field
+        """
+        data = self.codebook.loc[self.codebook['category'] == key, :]
+        order_map = {i['name']: i['order'] for _, i in data.iterrows()}
+        return order_map
```

### Comparing `HawaData-0.7.8/hawa/common/query.py` & `HawaData-0.7.9/hawa/common/query.py`

 * *Files 2% similar despite different names*

```diff
@@ -132,7 +132,12 @@
         return item_codes
 
     def query_locations(self, location_ids: list[int]):
         location_sql = f'select id, name, level from locations where id in {tuple(location_ids)};'
         with self.db.engine_conn() as conn:
             locations = pd.read_sql(text(location_sql), conn)
         return locations
+
+    def query_codebook(self):
+        sql = f"select code,category,name,`order` from codebook;"
+        with self.db.engine_conn() as conn:
+            return pd.read_sql(text(sql), conn)
```

### Comparing `HawaData-0.7.8/hawa/common/utils.py` & `HawaData-0.7.9/hawa/common/utils.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/hawa/config.py` & `HawaData-0.7.9/hawa/config.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/hawa/data/klass.py` & `HawaData-0.7.9/hawa/data/klass.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/hawa/data/province.py` & `HawaData-0.7.9/hawa/data/province.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/hawa/data/school.py` & `HawaData-0.7.9/hawa/data/school.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/hawa/data/student.py` & `HawaData-0.7.9/hawa/data/student.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/hawa/paper/health.py` & `HawaData-0.7.9/hawa/paper/health.py`

 * *Files 0% similar despite different names*

```diff
@@ -84,15 +84,17 @@
             'F': answers.loc[answers.gender == 'F', :]
         }
         res = {}
         for gender_k, gender_v in raw_data.items():
             res[gender_k] = self.count_dim_or_field_scores_by_answers(
                 answers=gender_v, item_code=item_code, res_format='dict'
             )
+        map_order = self.get_dim_field_order(key=item_code)
         codes = answers[item_code].unique().tolist()
+        codes = sorted(codes, key=lambda x: map_order[x])
         gender_box = []
         for gender_k, gender_data in res.items():
             row_data = {
                 "name": gender_k if key_format == 'en' else project.total_gender_map[gender_k],
                 "value": []
             }
             for c in codes:
```

### Comparing `HawaData-0.7.8/hawa/paper/mht.py` & `HawaData-0.7.9/hawa/paper/mht.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/setup.py` & `HawaData-0.7.9/setup.py`

 * *Files identical despite different names*

### Comparing `HawaData-0.7.8/test/test_query.py` & `HawaData-0.7.9/test/test_query.py`

 * *Files identical despite different names*

