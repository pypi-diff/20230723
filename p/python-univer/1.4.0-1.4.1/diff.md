# Comparing `tmp/python-univer-1.4.0.tar.gz` & `tmp/python-univer-1.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "python-univer-1.4.0.tar", last modified: Tue Jul 18 17:14:33 2023, max compression
+gzip compressed data, was "python-univer-1.4.1.tar", last modified: Sun Jul 23 09:42:36 2023, max compression
```

## Comparing `python-univer-1.4.0.tar` & `python-univer-1.4.1.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-18 17:14:33.953333 python-univer-1.4.0/
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.0/LICENSE
--rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-18 17:14:33.953333 python-univer-1.4.0/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1001)      706 2023-07-18 16:09:38.000000 python-univer-1.4.0/README.md
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-18 17:14:33.953333 python-univer-1.4.0/python_univer.egg-info/
--rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-18 17:14:33.000000 python-univer-1.4.0/python_univer.egg-info/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1001)      732 2023-07-18 17:14:33.000000 python-univer-1.4.0/python_univer.egg-info/SOURCES.txt
--rw-r--r--   0 user      (1000) user      (1001)        1 2023-07-18 17:14:33.000000 python-univer-1.4.0/python_univer.egg-info/dependency_links.txt
--rw-r--r--   0 user      (1000) user      (1001)       18 2023-07-18 17:14:33.000000 python-univer-1.4.0/python_univer.egg-info/requires.txt
--rw-r--r--   0 user      (1000) user      (1001)       10 2023-07-18 17:14:33.000000 python-univer-1.4.0/python_univer.egg-info/top_level.txt
--rw-r--r--   0 user      (1000) user      (1001)       38 2023-07-18 17:14:33.953333 python-univer-1.4.0/setup.cfg
--rw-r--r--   0 user      (1000) user      (1001)      891 2023-07-18 17:14:26.000000 python-univer-1.4.0/setup.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-18 17:14:33.953333 python-univer-1.4.0/univer_db/
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)      472 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/config.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-18 17:14:33.953333 python-univer-1.4.0/univer_db/models/
--rw-r--r--   0 user      (1000) user      (1001)      225 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/models/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)     9291 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/models/base.py
--rw-r--r--   0 user      (1000) user      (1001)     8231 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/models/dormitories.py
--rw-r--r--   0 user      (1000) user      (1001)     1873 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/models/geo.py
--rw-r--r--   0 user      (1000) user      (1001)      951 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/models/grades.py
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/models/groups.py
--rw-r--r--   0 user      (1000) user      (1001)    33958 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/models/models.py
--rw-r--r--   0 user      (1000) user      (1001)     9202 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/models/orders.py
--rw-r--r--   0 user      (1000) user      (1001)    22041 2023-07-18 17:14:13.000000 python-univer-1.4.0/univer_db/models/roles.py
--rw-r--r--   0 user      (1000) user      (1001)     4182 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/models/schedule.py
--rw-r--r--   0 user      (1000) user      (1001)     3558 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/models/sheets.py
--rw-r--r--   0 user      (1000) user      (1001)     5047 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/models/structures.py
--rw-r--r--   0 user      (1000) user      (1001)      769 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/orm.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-18 17:14:33.953333 python-univer-1.4.0/univer_db/tests/
--rw-r--r--   0 user      (1000) user      (1001)      264 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/tests/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)      569 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/tests/geo.py
--rw-r--r--   0 user      (1000) user      (1001)     2635 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/tests/models.py
--rw-r--r--   0 user      (1000) user      (1001)     1136 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/tests/roles.py
--rw-r--r--   0 user      (1000) user      (1001)      624 2023-07-18 16:09:38.000000 python-univer-1.4.0/univer_db/tests/structures.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 09:42:36.099999 python-univer-1.4.1/
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.1/LICENSE
+-rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 09:42:36.099999 python-univer-1.4.1/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1001)      706 2023-07-18 16:09:38.000000 python-univer-1.4.1/README.md
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 09:42:36.096666 python-univer-1.4.1/python_univer.egg-info/
+-rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 09:42:35.000000 python-univer-1.4.1/python_univer.egg-info/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1001)      732 2023-07-23 09:42:35.000000 python-univer-1.4.1/python_univer.egg-info/SOURCES.txt
+-rw-r--r--   0 user      (1000) user      (1001)        1 2023-07-23 09:42:35.000000 python-univer-1.4.1/python_univer.egg-info/dependency_links.txt
+-rw-r--r--   0 user      (1000) user      (1001)       18 2023-07-23 09:42:35.000000 python-univer-1.4.1/python_univer.egg-info/requires.txt
+-rw-r--r--   0 user      (1000) user      (1001)       10 2023-07-23 09:42:35.000000 python-univer-1.4.1/python_univer.egg-info/top_level.txt
+-rw-r--r--   0 user      (1000) user      (1001)       38 2023-07-23 09:42:36.099999 python-univer-1.4.1/setup.cfg
+-rw-r--r--   0 user      (1000) user      (1001)      891 2023-07-23 09:40:09.000000 python-univer-1.4.1/setup.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 09:42:36.096666 python-univer-1.4.1/univer_db/
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)      472 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/config.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 09:42:36.099999 python-univer-1.4.1/univer_db/models/
+-rw-r--r--   0 user      (1000) user      (1001)      225 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)     9291 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/base.py
+-rw-r--r--   0 user      (1000) user      (1001)     8231 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/dormitories.py
+-rw-r--r--   0 user      (1000) user      (1001)     1873 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/geo.py
+-rw-r--r--   0 user      (1000) user      (1001)      951 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/grades.py
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/groups.py
+-rw-r--r--   0 user      (1000) user      (1001)    33972 2023-07-23 09:39:43.000000 python-univer-1.4.1/univer_db/models/models.py
+-rw-r--r--   0 user      (1000) user      (1001)     9202 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/orders.py
+-rw-r--r--   0 user      (1000) user      (1001)    22049 2023-07-23 09:39:05.000000 python-univer-1.4.1/univer_db/models/roles.py
+-rw-r--r--   0 user      (1000) user      (1001)     4182 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/schedule.py
+-rw-r--r--   0 user      (1000) user      (1001)     3558 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/sheets.py
+-rw-r--r--   0 user      (1000) user      (1001)     5047 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/structures.py
+-rw-r--r--   0 user      (1000) user      (1001)      769 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/orm.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 09:42:36.099999 python-univer-1.4.1/univer_db/tests/
+-rw-r--r--   0 user      (1000) user      (1001)      264 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/tests/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)      569 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/tests/geo.py
+-rw-r--r--   0 user      (1000) user      (1001)     2635 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/tests/models.py
+-rw-r--r--   0 user      (1000) user      (1001)     1136 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/tests/roles.py
+-rw-r--r--   0 user      (1000) user      (1001)      624 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/tests/structures.py
```

### Comparing `python-univer-1.4.0/PKG-INFO` & `python-univer-1.4.1/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: python-univer
-Version: 1.4.0
+Version: 1.4.1
 Summary: Данная библиотека содержить SqlAlchemy ORM для системы Univer
 Home-page: https://github.com/yessenovuniversity/python_univer
 Author: Nauryzbek Aitbayev
 Author-email: nauryzbek.aitbayev@yu.edu.kz
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: Other/Proprietary License
 Classifier: Operating System :: OS Independent
```

### Comparing `python-univer-1.4.0/README.md` & `python-univer-1.4.1/README.md`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/python_univer.egg-info/PKG-INFO` & `python-univer-1.4.1/python_univer.egg-info/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: python-univer
-Version: 1.4.0
+Version: 1.4.1
 Summary: Данная библиотека содержить SqlAlchemy ORM для системы Univer
 Home-page: https://github.com/yessenovuniversity/python_univer
 Author: Nauryzbek Aitbayev
 Author-email: nauryzbek.aitbayev@yu.edu.kz
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: Other/Proprietary License
 Classifier: Operating System :: OS Independent
```

### Comparing `python-univer-1.4.0/python_univer.egg-info/SOURCES.txt` & `python-univer-1.4.1/python_univer.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/setup.py` & `python-univer-1.4.1/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 import setuptools
 
 with open('README.md', 'r', encoding='utf8') as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="python-univer",
-    version="1.4.0",
+    version="1.4.1",
     author="Nauryzbek Aitbayev",
     author_email="nauryzbek.aitbayev@yu.edu.kz",
     description="Данная библиотека содержить SqlAlchemy ORM для системы Univer",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/yessenovuniversity/python_univer",
     packages=setuptools.find_packages(),
```

### Comparing `python-univer-1.4.0/univer_db/models/base.py` & `python-univer-1.4.1/univer_db/models/base.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/models/dormitories.py` & `python-univer-1.4.1/univer_db/models/dormitories.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/models/geo.py` & `python-univer-1.4.1/univer_db/models/geo.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/models/grades.py` & `python-univer-1.4.1/univer_db/models/grades.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/models/models.py` & `python-univer-1.4.1/univer_db/models/models.py`

 * *Files 0% similar despite different names*

```diff
@@ -882,16 +882,17 @@
 
     def __str__(self):
         return f'{self.name_ru}'
 
 
 class SettlementStatus(Base):
     """
-    Неизвестный модель
+    Статус населенного пункта
     """
+
     __tablename__ = 'univer_settlement_status'
 
     # Идентификатор
     id = Column('settlement_status_id', Integer, primary_key=True)
 
     # Наименование
     name_ru = Column('settlement_status_name_ru', String(100))
```

### Comparing `python-univer-1.4.0/univer_db/models/orders.py` & `python-univer-1.4.1/univer_db/models/orders.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/models/roles.py` & `python-univer-1.4.1/univer_db/models/roles.py`

 * *Files 1% similar despite different names*

```diff
@@ -108,17 +108,16 @@
     payment_form = relationship('PaymentForm')
 
     # Форма обучения
     education_form_id = Column(ForeignKey(
         'univer_education_form.education_form_id'))
     education_form = relationship('EducationForm')
 
-    # Неизвестное поле
-    settlement_status_id = Column(ForeignKey(
-        'univer_settlement_status.settlement_status_id'))
+    # Статус населенного пункта
+    settlement_status_id = Column(ForeignKey('univer_settlement_status.settlement_status_id'))
     settlement_status = relationship('SettlementStatus')
 
     # Иностранный язык
     foreign_language_id = Column(ForeignKey(
         'univer_foreign_language.foreign_language_id'))
     foreign_language = relationship('ForeignLanguage')
```

### Comparing `python-univer-1.4.0/univer_db/models/schedule.py` & `python-univer-1.4.1/univer_db/models/schedule.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/models/sheets.py` & `python-univer-1.4.1/univer_db/models/sheets.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/models/structures.py` & `python-univer-1.4.1/univer_db/models/structures.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/orm.py` & `python-univer-1.4.1/univer_db/orm.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/tests/geo.py` & `python-univer-1.4.1/univer_db/tests/geo.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/tests/models.py` & `python-univer-1.4.1/univer_db/tests/models.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/tests/roles.py` & `python-univer-1.4.1/univer_db/tests/roles.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.0/univer_db/tests/structures.py` & `python-univer-1.4.1/univer_db/tests/structures.py`

 * *Files identical despite different names*

