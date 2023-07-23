# Comparing `tmp/python-univer-1.4.2.tar.gz` & `tmp/python-univer-1.4.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "python-univer-1.4.2.tar", last modified: Sun Jul 23 10:38:24 2023, max compression
+gzip compressed data, was "python-univer-1.4.3.tar", last modified: Sun Jul 23 11:20:30 2023, max compression
```

## Comparing `python-univer-1.4.2.tar` & `python-univer-1.4.3.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 10:38:24.899999 python-univer-1.4.2/
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.2/LICENSE
--rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 10:38:24.899999 python-univer-1.4.2/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1001)      706 2023-07-18 16:09:38.000000 python-univer-1.4.2/README.md
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 10:38:24.899999 python-univer-1.4.2/python_univer.egg-info/
--rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 10:38:24.000000 python-univer-1.4.2/python_univer.egg-info/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1001)      732 2023-07-23 10:38:24.000000 python-univer-1.4.2/python_univer.egg-info/SOURCES.txt
--rw-r--r--   0 user      (1000) user      (1001)        1 2023-07-23 10:38:24.000000 python-univer-1.4.2/python_univer.egg-info/dependency_links.txt
--rw-r--r--   0 user      (1000) user      (1001)       18 2023-07-23 10:38:24.000000 python-univer-1.4.2/python_univer.egg-info/requires.txt
--rw-r--r--   0 user      (1000) user      (1001)       10 2023-07-23 10:38:24.000000 python-univer-1.4.2/python_univer.egg-info/top_level.txt
--rw-r--r--   0 user      (1000) user      (1001)       38 2023-07-23 10:38:24.899999 python-univer-1.4.2/setup.cfg
--rw-r--r--   0 user      (1000) user      (1001)      891 2023-07-23 10:37:22.000000 python-univer-1.4.2/setup.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 10:38:24.899999 python-univer-1.4.2/univer_db/
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)      472 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/config.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 10:38:24.899999 python-univer-1.4.2/univer_db/models/
--rw-r--r--   0 user      (1000) user      (1001)      225 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)     9234 2023-07-23 10:05:33.000000 python-univer-1.4.2/univer_db/models/base.py
--rw-r--r--   0 user      (1000) user      (1001)     8231 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/dormitories.py
--rw-r--r--   0 user      (1000) user      (1001)     1873 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/geo.py
--rw-r--r--   0 user      (1000) user      (1001)      951 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/grades.py
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/groups.py
--rw-r--r--   0 user      (1000) user      (1001)    33983 2023-07-23 09:49:44.000000 python-univer-1.4.2/univer_db/models/models.py
--rw-r--r--   0 user      (1000) user      (1001)     9202 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/orders.py
--rw-r--r--   0 user      (1000) user      (1001)    22710 2023-07-23 10:36:53.000000 python-univer-1.4.2/univer_db/models/roles.py
--rw-r--r--   0 user      (1000) user      (1001)     4182 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/schedule.py
--rw-r--r--   0 user      (1000) user      (1001)     3558 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/sheets.py
--rw-r--r--   0 user      (1000) user      (1001)     5047 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/models/structures.py
--rw-r--r--   0 user      (1000) user      (1001)      769 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/orm.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 10:38:24.899999 python-univer-1.4.2/univer_db/tests/
--rw-r--r--   0 user      (1000) user      (1001)      264 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/tests/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)      569 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/tests/geo.py
--rw-r--r--   0 user      (1000) user      (1001)     2635 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/tests/models.py
--rw-r--r--   0 user      (1000) user      (1001)     1136 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/tests/roles.py
--rw-r--r--   0 user      (1000) user      (1001)      624 2023-07-18 16:09:38.000000 python-univer-1.4.2/univer_db/tests/structures.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 11:20:30.299998 python-univer-1.4.3/
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.3/LICENSE
+-rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 11:20:30.299998 python-univer-1.4.3/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1001)      706 2023-07-18 16:09:38.000000 python-univer-1.4.3/README.md
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 11:20:30.296665 python-univer-1.4.3/python_univer.egg-info/
+-rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 11:20:30.000000 python-univer-1.4.3/python_univer.egg-info/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1001)      732 2023-07-23 11:20:30.000000 python-univer-1.4.3/python_univer.egg-info/SOURCES.txt
+-rw-r--r--   0 user      (1000) user      (1001)        1 2023-07-23 11:20:30.000000 python-univer-1.4.3/python_univer.egg-info/dependency_links.txt
+-rw-r--r--   0 user      (1000) user      (1001)       18 2023-07-23 11:20:30.000000 python-univer-1.4.3/python_univer.egg-info/requires.txt
+-rw-r--r--   0 user      (1000) user      (1001)       10 2023-07-23 11:20:30.000000 python-univer-1.4.3/python_univer.egg-info/top_level.txt
+-rw-r--r--   0 user      (1000) user      (1001)       38 2023-07-23 11:20:30.299998 python-univer-1.4.3/setup.cfg
+-rw-r--r--   0 user      (1000) user      (1001)      891 2023-07-23 11:18:56.000000 python-univer-1.4.3/setup.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 11:20:30.296665 python-univer-1.4.3/univer_db/
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)      472 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/config.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 11:20:30.299998 python-univer-1.4.3/univer_db/models/
+-rw-r--r--   0 user      (1000) user      (1001)      225 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)     9234 2023-07-23 10:05:33.000000 python-univer-1.4.3/univer_db/models/base.py
+-rw-r--r--   0 user      (1000) user      (1001)     8231 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/dormitories.py
+-rw-r--r--   0 user      (1000) user      (1001)     1873 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/geo.py
+-rw-r--r--   0 user      (1000) user      (1001)      951 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/grades.py
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/groups.py
+-rw-r--r--   0 user      (1000) user      (1001)    35329 2023-07-23 11:18:08.000000 python-univer-1.4.3/univer_db/models/models.py
+-rw-r--r--   0 user      (1000) user      (1001)     9202 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/orders.py
+-rw-r--r--   0 user      (1000) user      (1001)    23099 2023-07-23 11:05:03.000000 python-univer-1.4.3/univer_db/models/roles.py
+-rw-r--r--   0 user      (1000) user      (1001)     4182 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/schedule.py
+-rw-r--r--   0 user      (1000) user      (1001)     3558 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/sheets.py
+-rw-r--r--   0 user      (1000) user      (1001)     5047 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/structures.py
+-rw-r--r--   0 user      (1000) user      (1001)      769 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/orm.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 11:20:30.299998 python-univer-1.4.3/univer_db/tests/
+-rw-r--r--   0 user      (1000) user      (1001)      264 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/tests/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)      569 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/tests/geo.py
+-rw-r--r--   0 user      (1000) user      (1001)     2635 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/tests/models.py
+-rw-r--r--   0 user      (1000) user      (1001)     1136 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/tests/roles.py
+-rw-r--r--   0 user      (1000) user      (1001)      624 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/tests/structures.py
```

### Comparing `python-univer-1.4.2/PKG-INFO` & `python-univer-1.4.3/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: python-univer
-Version: 1.4.2
+Version: 1.4.3
 Summary: Данная библиотека содержить SqlAlchemy ORM для системы Univer
 Home-page: https://github.com/yessenovuniversity/python_univer
 Author: Nauryzbek Aitbayev
 Author-email: nauryzbek.aitbayev@yu.edu.kz
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: Other/Proprietary License
 Classifier: Operating System :: OS Independent
```

### Comparing `python-univer-1.4.2/README.md` & `python-univer-1.4.3/README.md`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/python_univer.egg-info/PKG-INFO` & `python-univer-1.4.3/python_univer.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: python-univer
-Version: 1.4.2
+Version: 1.4.3
 Summary: Данная библиотека содержить SqlAlchemy ORM для системы Univer
 Home-page: https://github.com/yessenovuniversity/python_univer
 Author: Nauryzbek Aitbayev
 Author-email: nauryzbek.aitbayev@yu.edu.kz
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: Other/Proprietary License
 Classifier: Operating System :: OS Independent
```

### Comparing `python-univer-1.4.2/python_univer.egg-info/SOURCES.txt` & `python-univer-1.4.3/python_univer.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/setup.py` & `python-univer-1.4.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 import setuptools
 
 with open('README.md', 'r', encoding='utf8') as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="python-univer",
-    version="1.4.2",
+    version="1.4.3",
     author="Nauryzbek Aitbayev",
     author_email="nauryzbek.aitbayev@yu.edu.kz",
     description="Данная библиотека содержить SqlAlchemy ORM для системы Univer",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/yessenovuniversity/python_univer",
     packages=setuptools.find_packages(),
```

### Comparing `python-univer-1.4.2/univer_db/models/base.py` & `python-univer-1.4.3/univer_db/models/base.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/models/dormitories.py` & `python-univer-1.4.3/univer_db/models/dormitories.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/models/geo.py` & `python-univer-1.4.3/univer_db/models/geo.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/models/grades.py` & `python-univer-1.4.3/univer_db/models/grades.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/models/models.py` & `python-univer-1.4.3/univer_db/models/models.py`

 * *Files 2% similar despite different names*

```diff
@@ -188,58 +188,104 @@
     def __str__(self):
         return self.name_ru
 
 
 class GraduateDocType(Base):
     """
     Тип документа об окончании учебного заведения перед поступлением в университет
-    Статус: Выполняется
     """
-
     __tablename__ = 'univer_graduate_doctypes'
 
+    # Идентификатор
     id = Column('graduate_doctype_id', Integer, primary_key=True)
+
+    # Наименование
     name_ru = Column('graduate_doctype_name_ru', String)
     name_kz = Column('graduate_doctype_name_kz', String)
     name_en = Column('graduate_doctype_name_en', String)
 
     def __repr__(self):
         return '<GraduateDocType {} (id={})>'.format(self, self.id)
 
     def __str__(self):
         return self.name_ru
 
 
 class GraduateInfo(Base):
     """
     Данные об окончании учебного заведения перед поступлением в университет
-    Статус: Выполняется
     """
 
     __tablename__ = 'univer_graduate_info'
 
+    # Идентификатор
     id = Column('graduate_info_id', Integer, primary_key=True)
+
+    # Дата выдачи
     date = Column('graduate_info_date', DateTime)
+
+    # Наименование учебного заведения
     institution_name = Column('graduate_info_institution_name', String)
+
+    # Тип учебного заведения
+    institution_type_id = Column(
+        'edu_institution_type_id', ForeignKey('univer_edu_institution_types.edu_institution_type_id')
+    )
+    institution_type = relationship('InstitutionType')
+
+    # Серия документа
     series = Column('graduate_info_series', String)
+
+    # Номер документа
     number = Column('graduate_info_number', String)
-    graduate_doctype_id = Column(ForeignKey(
-        'univer_graduate_doctypes.graduate_doctype_id'))
+
+    # С отличием
+    with_honor = Column('graduate_info_with_honors', Integer)
+
+    # Средняя оценка
+    average_point = Column('graduate_info_average_point', Integer)
+
+    # Тип документа
+    graduate_doctype_id = Column(ForeignKey('univer_graduate_doctypes.graduate_doctype_id'))
     graduate_doctype = relationship('GraduateDocType')
-    institution_id = Column('edu_institution_id', ForeignKey(
-        'univer_edu_institutions.edu_institution_id'))
+
+    institution_id = Column('edu_institution_id', ForeignKey('univer_edu_institutions.edu_institution_id'))
     institution = relationship('Institution')
 
     def __repr__(self):
         return '<Graduate {} (id={})>'.format(self, self.id)
 
     def __str__(self):
         return '{} {}'.format(self.series, self.number)
 
 
+class InstitutionType(Base):
+    """
+    Тип учебного заведения
+    """
+    __tablename__ = 'univer_edu_institution_types'
+
+    # Идентификатор
+    id = Column('edu_institution_type_id', Integer, primary_key=True)
+
+    # Наименование
+    name_ru = Column('edu_institution_type_name_ru', String(100))
+    name_kz = Column('edu_institution_type_name_kz', String(100))
+    name_en = Column('edu_institution_type_name_en', String(100))
+
+    # Статус
+    status = Column('status', Integer)
+
+    def __repr__(self):
+        return '<InstitutionType {} (id={} status={})>'.format(self, self.id, self.status)
+
+    def __str__(self):
+        return self.name_ru
+
+
 class AcademCalendar(Base):
     """
     Модель "Академический календарь"
     """
 
     __tablename__ = 'univer_academ_calendar_pos'
```

### Comparing `python-univer-1.4.2/univer_db/models/orders.py` & `python-univer-1.4.3/univer_db/models/orders.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/models/roles.py` & `python-univer-1.4.3/univer_db/models/roles.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 """
 Роли и пользовали внутри Univer
 """
 
-from sqlalchemy import Column, Integer, String, ForeignKey, DateTime, Unicode
+from sqlalchemy import Column, Integer, String, ForeignKey, DateTime, Unicode, Boolean
 from sqlalchemy.orm import relationship, backref, validates
 
 from univer_db.orm import get_base
 
 Base = get_base()
 
 
@@ -216,29 +216,31 @@
     document_identity_issued = Column(
         'students_document_identity_issued', String(100))
 
     # ИИН студента
     identify_code = Column('students_identify_code', String(50))
 
     # Данные об окончании учебного заведения перед поступлением в университет
-    graduate_info_id = Column(ForeignKey(
-        'univer_graduate_info.graduate_info_id'))
+    graduate_info_id = Column(ForeignKey('univer_graduate_info.graduate_info_id'))
     graduate_info = relationship('GraduateInfo')
 
     # Год начала действия учебного плана
     educ_plan_adm_year = Column(Integer)
 
     # Языковое отделение
     lang_division_id = Column(ForeignKey(
         'univer_lang_division.lang_division_id'))
     lang_division = relationship('LangDivision')
 
     # Нуждается в общежитии
     need_hostel = Column('students_need_hostel', Integer)
 
+    # Военное положение
+    is_military_bound = Column('students_military_bound', Boolean, default=False)
+
     # Сколько лет служил
     military_served_years = Column('students_military_served', Integer, default=0)
 
     @validates('military_served_years')
     def validate_military_served_years(self, key, value):
         """
         Значение данного параметра не должно быть меньше нуля
@@ -255,14 +257,21 @@
         Служил в армии
         """
         if self.military_served_years and self.military_served_years > 0:
             return True
 
         return False
 
+    # Количество детей в семье
+    children = Column('students_children_count', Integer, default=0)
+
+    # Код ИКТ
+    ikt_univer = Column('students_iktUniver', String(5))
+    ikt_additional = Column('students_iktAdditional', String(50))
+
     @property
     def payment_info_ru(self):
         """
         Возвращает специальный текст на русском для формы оплаты
         """
         if self.payment_form_id == 2:
             return 'на платной основе'
```

### Comparing `python-univer-1.4.2/univer_db/models/schedule.py` & `python-univer-1.4.3/univer_db/models/schedule.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/models/sheets.py` & `python-univer-1.4.3/univer_db/models/sheets.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/models/structures.py` & `python-univer-1.4.3/univer_db/models/structures.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/orm.py` & `python-univer-1.4.3/univer_db/orm.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/tests/geo.py` & `python-univer-1.4.3/univer_db/tests/geo.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/tests/models.py` & `python-univer-1.4.3/univer_db/tests/models.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/tests/roles.py` & `python-univer-1.4.3/univer_db/tests/roles.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.2/univer_db/tests/structures.py` & `python-univer-1.4.3/univer_db/tests/structures.py`

 * *Files identical despite different names*

