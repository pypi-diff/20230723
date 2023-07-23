# Comparing `tmp/zdatabase-0.5.7.tar.gz` & `tmp/zdatabase-0.5.8.tar.gz`

## Comparing `zdatabase-0.5.7.tar` & `zdatabase-0.5.8.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0      707 2020-02-02 00:00:00.000000 zdatabase-0.5.7/src/zdatabase/__init__.py
--rw-r--r--   0        0        0     2581 2020-02-02 00:00:00.000000 zdatabase-0.5.7/src/zdatabase/model.py
--rw-r--r--   0        0        0     4802 2020-02-02 00:00:00.000000 zdatabase-0.5.7/src/zdatabase/utility.py
--rw-r--r--   0        0        0       10 2020-02-02 00:00:00.000000 zdatabase-0.5.7/.gitignore
--rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 zdatabase-0.5.7/LICENSE
--rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 zdatabase-0.5.7/README.md
--rw-r--r--   0        0        0      639 2020-02-02 00:00:00.000000 zdatabase-0.5.7/pyproject.toml
--rw-r--r--   0        0        0      585 2020-02-02 00:00:00.000000 zdatabase-0.5.7/PKG-INFO
+-rw-r--r--   0        0        0      707 2020-02-02 00:00:00.000000 zdatabase-0.5.8/src/zdatabase/__init__.py
+-rw-r--r--   0        0        0     2581 2020-02-02 00:00:00.000000 zdatabase-0.5.8/src/zdatabase/model.py
+-rw-r--r--   0        0        0     4709 2020-02-02 00:00:00.000000 zdatabase-0.5.8/src/zdatabase/utility.py
+-rw-r--r--   0        0        0       10 2020-02-02 00:00:00.000000 zdatabase-0.5.8/.gitignore
+-rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 zdatabase-0.5.8/LICENSE
+-rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 zdatabase-0.5.8/README.md
+-rw-r--r--   0        0        0      639 2020-02-02 00:00:00.000000 zdatabase-0.5.8/pyproject.toml
+-rw-r--r--   0        0        0      585 2020-02-02 00:00:00.000000 zdatabase-0.5.8/PKG-INFO
```

### Comparing `zdatabase-0.5.7/src/zdatabase/__init__.py` & `zdatabase-0.5.8/src/zdatabase/__init__.py`

 * *Files identical despite different names*

### Comparing `zdatabase-0.5.7/src/zdatabase/model.py` & `zdatabase-0.5.8/src/zdatabase/model.py`

 * *Files identical despite different names*

### Comparing `zdatabase-0.5.7/src/zdatabase/utility.py` & `zdatabase-0.5.8/src/zdatabase/utility.py`

 * *Files 4% similar despite different names*

```diff
@@ -8,14 +8,18 @@
         db.session.flush()
 
     @staticmethod
     def commit():
         db.session.commit()
 
     @staticmethod
+    def rollback():
+        db.session.rollback()
+
+    @staticmethod
     def query_(*args, **kwargs):
         return db.session.query(*args, **kwargs)
 
     @staticmethod
     def add_all(items):
         db.session.add_all(items)
         db.session.commit()
@@ -51,104 +55,96 @@
         flts = []
         start_date = params.get('start_date')
         end_date = params.get('end_date')
         flts += [getattr(cls, attr_name) >= start_date] if start_date else []
         flts += [getattr(cls, attr_name) <= end_date] if end_date else []
         return flts
 
-
     @staticmethod
     def all(cls, query, method='to_json'):
         """返回全部记录
         """
         items = query.all()
         return [getattr(item, method)() for item in items]
 
     @staticmethod
     def paginate(query, params, method='to_json'):
         """分页
         page_size=100&page_num=1
         """
         page_num = int(params.get('page_num', '1'))
         page_size = int(params.get('page_size', '10'))
-        pagination = query.paginate(page_num, per_page=page_size)  
+        pagination = query.paginate(page_num, per_page=page_size)
         rst = {
             'items': [getattr(item, method)() for item in pagination.items],
             'total': pagination.total,
             'pages': pagination.pages
         }
         return rst
 
 
 class MapperUtility:
     @staticmethod
     def jsonlize(items):
         return [item.to_json() for item in items]
-    
+
     @classmethod
     def add_(cls, data):
         obj = cls.new(data)
         obj.add_one()
         return obj
-    
+
     @classmethod
     def add(cls, data, sync=True):
         if hasattr(cls, 'schema'):
             validate(instance=data, schema=cls.schema)
         obj = cls.add_(data)
         if sync:
             cls.commit()
         return obj
 
     @classmethod
     def save(cls, primary_key, data):
         if hasattr(cls, 'schema'):
             validate(instance=data, schema=cls.schema)
         obj = cls.get(primary_key)
-        if obj:
-            obj.update(data)
-        else:
-            cls.add_(data)
-        cls.commit()
-
-    @classmethod
-    def update(cls, primary_key, data):
-        obj = cls.get(primary_key)
         obj.update(data)
         cls.commit()
 
     @classmethod
     def get(cls, primary_key):
         return cls.query.get(primary_key)
-    
+
     @classmethod
-    def delete(cls, **kwargs):
+    def delete(cls, sync=True, **kwargs):
         cls.make_query(**kwargs).delete(synchronize_session=False)
+        if sync:
+            cls.commit()
 
     @classmethod
     def make_flts(cls, **kwargs):
-        return [getattr(cls, k) == v for k, v in kwargs.items()]
+        return [getattr(cls, k) == v for k, v in kwargs.items() if v is not None]
 
     @classmethod
     def make_query(cls, **kwargs):
         flts = cls.make_flts(**kwargs)
         return cls.filter(*flts)
-    
+
     @classmethod
     def get_list(cls, **kwargs):
         return cls.make_query(**kwargs).all()
-    
+
     @classmethod
     def get_json(cls, primary_key):
         obj = cls.get(primary_key)
         return obj.to_json() if obj else {}
 
     @classmethod
     def get_jsons(cls, page_num=None, page_size=None, **kwargs):
-        if page_num or page_size :
+        if page_num or page_size:
             pagination = {
                 'page_num': page_num if page_num else 1,
                 'page_size': page_size if page_size else 20
             }
             query = cls.make_query(**kwargs)
             return cls.paginate(query, pagination)
         else:
@@ -164,9 +160,7 @@
     @classmethod
     def get_map(cls, attr_names):
         rst_map = {}
         for item in cls.get_attrs(attr_names):
             a, b = item
             rst_map[a] = b
         return rst_map
-
-
```

### Comparing `zdatabase-0.5.7/LICENSE` & `zdatabase-0.5.8/LICENSE`

 * *Files identical despite different names*

### Comparing `zdatabase-0.5.7/pyproject.toml` & `zdatabase-0.5.8/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "zdatabase"
-version = "0.5.7"
+version = "0.5.8"
 authors = [
   { name="inspirare6", email="inspirare6@163.com" },
 ]
 description = "zen database library"
 readme = "README.md"
 requires-python = ">=3.7"
 dependencies = [
```

### Comparing `zdatabase-0.5.7/PKG-INFO` & `zdatabase-0.5.8/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zdatabase
-Version: 0.5.7
+Version: 0.5.8
 Summary: zen database library
 Project-URL: Homepage, https://github.com/inspirare6/zdatabase
 Project-URL: Bug Tracker, https://github.com/inspirare6/zdatabase/issues
 Author-email: inspirare6 <inspirare6@163.com>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

