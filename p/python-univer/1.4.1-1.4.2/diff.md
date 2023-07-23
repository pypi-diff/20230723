# Comparing `tmp/python-univer-1.4.1.tar.gz` & `tmp/python-univer-1.4.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "python-univer-1.4.1.tar", last modified: Sun Jul 23 09:42:36 2023, max compression
+gzip compressed data, was "python-univer-1.4.2.tar", last modified: Sun Jul 23 10:38:24 2023, max compression
```

## Comparing `python-univer-1.4.1.tar` & `python-univer-1.4.2.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 09:42:36.099999 python-univer-1.4.1/
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.1/LICENSE
--rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 09:42:36.099999 python-univer-1.4.1/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1001)      706 2023-07-18 16:09:38.000000 python-univer-1.4.1/README.md
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 09:42:36.096666 python-univer-1.4.1/python_univer.egg-info/
--rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 09:42:35.000000 python-univer-1.4.1/python_univer.egg-info/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1001)      732 2023-07-23 09:42:35.000000 python-univer-1.4.1/python_univer.egg-info/SOURCES.txt
--rw-r--r--   0 user      (1000) user      (1001)        1 2023-07-23 09:42:35.000000 python-univer-1.4.1/python_univer.egg-info/dependency_links.txt
--rw-r--r--   0 user      (1000) user      (1001)       18 2023-07-23 09:42:35.000000 python-univer-1.4.1/python_univer.egg-info/requires.txt
--rw-r--r--   0 user      (1000) user      (1001)       10 2023-07-23 09:42:35.000000 python-univer-1.4.1/python_univer.egg-info/top_level.txt
--rw-r--r--   0 user      (1000) user      (1001)       38 2023-07-23 09:42:36.099999 python-univer-1.4.1/setup.cfg
--rw-r--r--   0 user      (1000) user      (1001)      891 2023-07-23 09:40:09.000000 python-univer-1.4.1/setup.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 09:42:36.096666 python-univer-1.4.1/univer_db/
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)      472 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/config.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 09:42:36.099999 python-univer-1.4.1/univer_db/models/
--rw-r--r--   0 user      (1000) user      (1001)      225 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)     9291 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/base.py
--rw-r--r--   0 user      (1000) user      (1001)     8231 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/dormitories.py
--rw-r--r--   0 user      (1000) user      (1001)     1873 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/geo.py
--rw-r--r--   0 user      (1000) user      (1001)      951 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/grades.py
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/groups.py
--rw-r--r--   0 user      (1000) user      (1001)    33972 2023-07-23 09:39:43.000000 python-univer-1.4.1/univer_db/models/models.py
--rw-r--r--   0 user      (1000) user      (1001)     9202 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/orders.py
--rw-r--r--   0 user      (1000) user      (1001)    22049 2023-07-23 09:39:05.000000 python-univer-1.4.1/univer_db/models/roles.py
--rw-r--r--   0 user      (1000) user      (1001)     4182 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/schedule.py
--rw-r--r--   0 user      (1000) user      (1001)     3558 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/sheets.py
--rw-r--r--   0 user      (1000) user      (1001)     5047 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/models/structures.py
--rw-r--r--   0 user      (1000) user      (1001)      769 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/orm.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 09:42:36.099999 python-univer-1.4.1/univer_db/tests/
--rw-r--r--   0 user      (1000) user      (1001)      264 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/tests/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)      569 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/tests/geo.py
--rw-r--r--   0 user      (1000) user      (1001)     2635 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/tests/models.py
--rw-r--r--   0 user      (1000) user      (1001)     1136 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/tests/roles.py
--rw-r--r--   0 user      (1000) user      (1001)      624 2023-07-18 16:09:38.000000 python-univer-1.4.1/univer_db/tests/structures.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 10:38:24.899999 python-univer-1.4.2/
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.2/LICENSE
+-rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 10:38:24.899999 python-univer-1.4.2/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1001)      706 2023-07-18 16:09:38.000000 python-univer-1.4.2/README.md
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 10:38:24.899999 python-univer-1.4.2/python_univer.egg-info/
+-rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 10:38:24.000000 python-univer-1.4.2/python_univer.egg-info/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1001)      732 2023-07-23 10:38:24.000000 python-univer-1.4.2/python_univer.egg-info/SOURCES.txt
+-rw-r--r--   0 user      (1000) user      (1001)        1 2023-07-23 10:38:24.000000 python-univer-1.4.2/python_univer.egg-info/dependency_links.txt
+-rw-r--r--   0 user      (1000) user      (1001)       18 2023-07-23 10:38:24.000000 python-univer-1.4.2/python_univer.egg-info/requires.txt
+-rw-r--r--   0 user      (1000) user      (1001)       10 2023-07-23 10:38:24.000000 python-univer-1.4.2/python_univer.egg-info/top_level.txt
+-rw-r--r--   0 user      (1000) user      (1001)       38 2023-07-23 10:38:24.899999 python-univer-1.4.2/setup.cfg
+-rw-r--r--   0 user      (1000) user      (1001)      891 2023-07-23 10:37:22.000000 python-univer-1.4.2/setup.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 10:38:24.899999 python-univer-1.4.2/univer_db/
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)      472 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/config.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 10:38:24.899999 python-univer-1.4.2/univer_db/models/
+-rw-r--r--   0 user      (1000) user      (1001)      225 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)     9234 2023-07-23 10:05:33.000000 python-univer-1.4.2/univer_db/models/base.py
+-rw-r--r--   0 user      (1000) user      (1001)     8231 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/dormitories.py
+-rw-r--r--   0 user      (1000) user      (1001)     1873 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/geo.py
+-rw-r--r--   0 user      (1000) user      (1001)      951 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/grades.py
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/groups.py
+-rw-r--r--   0 user      (1000) user      (1001)    33983 2023-07-23 09:49:44.000000 python-univer-1.4.2/univer_db/models/models.py
+-rw-r--r--   0 user      (1000) user      (1001)     9202 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/orders.py
+-rw-r--r--   0 user      (1000) user      (1001)    22710 2023-07-23 10:36:53.000000 python-univer-1.4.2/univer_db/models/roles.py
+-rw-r--r--   0 user      (1000) user      (1001)     4182 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/schedule.py
+-rw-r--r--   0 user      (1000) user      (1001)     3558 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/sheets.py
+-rw-r--r--   0 user      (1000) user      (1001)     5047 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/structures.py
+-rw-r--r--   0 user      (1000) user      (1001)      769 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/orm.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 10:38:24.899999 python-univer-1.4.2/univer_db/tests/
+-rw-r--r--   0 user      (1000) user      (1001)      264 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/tests/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)      569 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/tests/geo.py
+-rw-r--r--   0 user      (1000) user      (1001)     2635 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/tests/models.py
+-rw-r--r--   0 user      (1000) user      (1001)     1136 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/tests/roles.py
+-rw-r--r--   0 user      (1000) user      (1001)      624 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/tests/structures.py
```

### Comparing `python-univer-1.4.1/PKG-INFO` & `python-univer-1.4.2/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: python-univer
-Version: 1.4.1
+Version: 1.4.2
 Summary: Данная библиотека содержить SqlAlchemy ORM для системы Univer
 Home-page: https://github.com/yessenovuniversity/python_univer
 Author: Nauryzbek Aitbayev
 Author-email: nauryzbek.aitbayev@yu.edu.kz
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: Other/Proprietary License
 Classifier: Operating System :: OS Independent
```

### Comparing `python-univer-1.4.1/README.md` & `python-univer-1.4.2/README.md`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/python_univer.egg-info/PKG-INFO` & `python-univer-1.4.2/python_univer.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: python-univer
-Version: 1.4.1
+Version: 1.4.2
 Summary: Данная библиотека содержить SqlAlchemy ORM для системы Univer
 Home-page: https://github.com/yessenovuniversity/python_univer
 Author: Nauryzbek Aitbayev
 Author-email: nauryzbek.aitbayev@yu.edu.kz
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: Other/Proprietary License
 Classifier: Operating System :: OS Independent
```

### Comparing `python-univer-1.4.1/python_univer.egg-info/SOURCES.txt` & `python-univer-1.4.2/python_univer.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/setup.py` & `python-univer-1.4.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 import setuptools
 
 with open('README.md', 'r', encoding='utf8') as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="python-univer",
-    version="1.4.1",
+    version="1.4.2",
     author="Nauryzbek Aitbayev",
     author_email="nauryzbek.aitbayev@yu.edu.kz",
     description="Данная библиотека содержить SqlAlchemy ORM для системы Univer",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/yessenovuniversity/python_univer",
     packages=setuptools.find_packages(),
```

### Comparing `python-univer-1.4.1/univer_db/models/base.py` & `python-univer-1.4.2/univer_db/models/base.py`

 * *Files 1% similar despite different names*

```diff
@@ -114,18 +114,16 @@
 
     def __str__(self):
         return self.name_ru
 
 
 class EnrollmentType(Base):
     """
-    Модель "Тип поступления"
-    Статус: Выполняется
+    Тип поступления
     """
-
     __tablename__ = 'univer_enrollment_type'
 
     # Идентификатор
     id = Column('enrollment_type_id', Integer, primary_key=True)
 
     # Наименование
     name_ru = Column('enrollment_type_name_ru', String(100))
```

### Comparing `python-univer-1.4.1/univer_db/models/dormitories.py` & `python-univer-1.4.2/univer_db/models/dormitories.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/univer_db/models/geo.py` & `python-univer-1.4.2/univer_db/models/geo.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/univer_db/models/grades.py` & `python-univer-1.4.2/univer_db/models/grades.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/univer_db/models/models.py` & `python-univer-1.4.2/univer_db/models/models.py`

 * *Files 1% similar despite different names*

```diff
@@ -951,15 +951,15 @@
 
     def __str__(self):
         return f'{self.name_ru}'
 
 
 class AdmissionReason(Base):
     """
-    Причина поступления
+    Основание для поступления
     """
     __tablename__ = 'univer_admission_reason'
 
     # Идентификатор
     id = Column('admission_reason_id', Integer, primary_key=True)
 
     # Наименование
```

### Comparing `python-univer-1.4.1/univer_db/models/orders.py` & `python-univer-1.4.2/univer_db/models/orders.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/univer_db/models/roles.py` & `python-univer-1.4.2/univer_db/models/roles.py`

 * *Files 3% similar despite different names*

```diff
@@ -113,30 +113,27 @@
     education_form = relationship('EducationForm')
 
     # Статус населенного пункта
     settlement_status_id = Column(ForeignKey('univer_settlement_status.settlement_status_id'))
     settlement_status = relationship('SettlementStatus')
 
     # Иностранный язык
-    foreign_language_id = Column(ForeignKey(
-        'univer_foreign_language.foreign_language_id'))
+    foreign_language_id = Column(ForeignKey('univer_foreign_language.foreign_language_id'))
     foreign_language = relationship('ForeignLanguage')
 
-    # Причина поступления
-    admission_reason_id = Column(ForeignKey(
-        'univer_admission_reason.admission_reason_id'))
+    # Основание для поступления
+    admission_reason_id = Column(ForeignKey('univer_admission_reason.admission_reason_id'))
     admission_reason = relationship('AdmissionReason')
 
     # Регион
     region_id = Column(ForeignKey('univer_region.region_id'))
     region = relationship('Region')
 
     # Тип поступления
-    enrollment_type_id = Column(ForeignKey(
-        'univer_enrollment_type.enrollment_type_id'))
+    enrollment_type_id = Column(ForeignKey('univer_enrollment_type.enrollment_type_id'))
     enrollment_type = relationship('EnrollmentType')
 
     # Район
     district_id = Column(ForeignKey('univer_district.district_id'))
     district = relationship('District')
 
     # ФИО студента
@@ -234,14 +231,38 @@
     lang_division_id = Column(ForeignKey(
         'univer_lang_division.lang_division_id'))
     lang_division = relationship('LangDivision')
 
     # Нуждается в общежитии
     need_hostel = Column('students_need_hostel', Integer)
 
+    # Сколько лет служил
+    military_served_years = Column('students_military_served', Integer, default=0)
+
+    @validates('military_served_years')
+    def validate_military_served_years(self, key, value):
+        """
+        Значение данного параметра не должно быть меньше нуля
+        """
+        if value is None:
+            return
+
+        assert value >= 0
+        return value
+
+    @property
+    def is_military_served(self):
+        """
+        Служил в армии
+        """
+        if self.military_served_years and self.military_served_years > 0:
+            return True
+
+        return False
+
     @property
     def payment_info_ru(self):
         """
         Возвращает специальный текст на русском для формы оплаты
         """
         if self.payment_form_id == 2:
             return 'на платной основе'
```

### Comparing `python-univer-1.4.1/univer_db/models/schedule.py` & `python-univer-1.4.2/univer_db/models/schedule.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/univer_db/models/sheets.py` & `python-univer-1.4.2/univer_db/models/sheets.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/univer_db/models/structures.py` & `python-univer-1.4.2/univer_db/models/structures.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/univer_db/orm.py` & `python-univer-1.4.2/univer_db/orm.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/univer_db/tests/geo.py` & `python-univer-1.4.2/univer_db/tests/geo.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/univer_db/tests/models.py` & `python-univer-1.4.2/univer_db/tests/models.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/univer_db/tests/roles.py` & `python-univer-1.4.2/univer_db/tests/roles.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.1/univer_db/tests/structures.py` & `python-univer-1.4.2/univer_db/tests/structures.py`

 * *Files identical despite different names*

