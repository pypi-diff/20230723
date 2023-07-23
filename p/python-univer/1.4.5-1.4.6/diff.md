# Comparing `tmp/python-univer-1.4.5.tar.gz` & `tmp/python-univer-1.4.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "python-univer-1.4.5.tar", last modified: Sun Jul 23 12:15:56 2023, max compression
+gzip compressed data, was "python-univer-1.4.6.tar", last modified: Sun Jul 23 20:31:15 2023, max compression
```

## Comparing `python-univer-1.4.5.tar` & `python-univer-1.4.6.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 12:15:56.936663 python-univer-1.4.5/
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.5/LICENSE
--rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 12:15:56.936663 python-univer-1.4.5/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1001)      706 2023-07-18 16:09:38.000000 python-univer-1.4.5/README.md
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 12:15:56.936663 python-univer-1.4.5/python_univer.egg-info/
--rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 12:15:56.000000 python-univer-1.4.5/python_univer.egg-info/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1001)      732 2023-07-23 12:15:56.000000 python-univer-1.4.5/python_univer.egg-info/SOURCES.txt
--rw-r--r--   0 user      (1000) user      (1001)        1 2023-07-23 12:15:56.000000 python-univer-1.4.5/python_univer.egg-info/dependency_links.txt
--rw-r--r--   0 user      (1000) user      (1001)       18 2023-07-23 12:15:56.000000 python-univer-1.4.5/python_univer.egg-info/requires.txt
--rw-r--r--   0 user      (1000) user      (1001)       10 2023-07-23 12:15:56.000000 python-univer-1.4.5/python_univer.egg-info/top_level.txt
--rw-r--r--   0 user      (1000) user      (1001)       38 2023-07-23 12:15:56.936663 python-univer-1.4.5/setup.cfg
--rw-r--r--   0 user      (1000) user      (1001)      891 2023-07-23 12:15:31.000000 python-univer-1.4.5/setup.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 12:15:56.936663 python-univer-1.4.5/univer_db/
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)      472 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/config.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 12:15:56.936663 python-univer-1.4.5/univer_db/models/
--rw-r--r--   0 user      (1000) user      (1001)      225 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/models/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)     9234 2023-07-23 10:05:33.000000 python-univer-1.4.5/univer_db/models/base.py
--rw-r--r--   0 user      (1000) user      (1001)     8231 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/models/dormitories.py
--rw-r--r--   0 user      (1000) user      (1001)     1873 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/models/geo.py
--rw-r--r--   0 user      (1000) user      (1001)      951 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/models/grades.py
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/models/groups.py
--rw-r--r--   0 user      (1000) user      (1001)    35329 2023-07-23 11:18:08.000000 python-univer-1.4.5/univer_db/models/models.py
--rw-r--r--   0 user      (1000) user      (1001)     9202 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/models/orders.py
--rw-r--r--   0 user      (1000) user      (1001)    23788 2023-07-23 12:15:28.000000 python-univer-1.4.5/univer_db/models/roles.py
--rw-r--r--   0 user      (1000) user      (1001)     4182 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/models/schedule.py
--rw-r--r--   0 user      (1000) user      (1001)     3558 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/models/sheets.py
--rw-r--r--   0 user      (1000) user      (1001)     5047 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/models/structures.py
--rw-r--r--   0 user      (1000) user      (1001)      769 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/orm.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 12:15:56.936663 python-univer-1.4.5/univer_db/tests/
--rw-r--r--   0 user      (1000) user      (1001)      264 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/tests/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)      569 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/tests/geo.py
--rw-r--r--   0 user      (1000) user      (1001)     2635 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/tests/models.py
--rw-r--r--   0 user      (1000) user      (1001)     1136 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/tests/roles.py
--rw-r--r--   0 user      (1000) user      (1001)      624 2023-07-18 16:09:38.000000 python-univer-1.4.5/univer_db/tests/structures.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 20:31:15.706666 python-univer-1.4.6/
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.6/LICENSE
+-rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 20:31:15.706666 python-univer-1.4.6/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1001)      706 2023-07-18 16:09:38.000000 python-univer-1.4.6/README.md
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 20:31:15.666666 python-univer-1.4.6/python_univer.egg-info/
+-rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 20:31:15.000000 python-univer-1.4.6/python_univer.egg-info/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1001)      732 2023-07-23 20:31:15.000000 python-univer-1.4.6/python_univer.egg-info/SOURCES.txt
+-rw-r--r--   0 user      (1000) user      (1001)        1 2023-07-23 20:31:15.000000 python-univer-1.4.6/python_univer.egg-info/dependency_links.txt
+-rw-r--r--   0 user      (1000) user      (1001)       18 2023-07-23 20:31:15.000000 python-univer-1.4.6/python_univer.egg-info/requires.txt
+-rw-r--r--   0 user      (1000) user      (1001)       10 2023-07-23 20:31:15.000000 python-univer-1.4.6/python_univer.egg-info/top_level.txt
+-rw-r--r--   0 user      (1000) user      (1001)       38 2023-07-23 20:31:15.706666 python-univer-1.4.6/setup.cfg
+-rw-r--r--   0 user      (1000) user      (1001)      891 2023-07-23 20:29:56.000000 python-univer-1.4.6/setup.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 20:31:15.673333 python-univer-1.4.6/univer_db/
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)      472 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/config.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 20:31:15.703333 python-univer-1.4.6/univer_db/models/
+-rw-r--r--   0 user      (1000) user      (1001)      225 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/models/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)     9234 2023-07-23 10:05:33.000000 python-univer-1.4.6/univer_db/models/base.py
+-rw-r--r--   0 user      (1000) user      (1001)     8231 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/models/dormitories.py
+-rw-r--r--   0 user      (1000) user      (1001)     1873 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/models/geo.py
+-rw-r--r--   0 user      (1000) user      (1001)      951 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/models/grades.py
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/models/groups.py
+-rw-r--r--   0 user      (1000) user      (1001)    35329 2023-07-23 11:18:08.000000 python-univer-1.4.6/univer_db/models/models.py
+-rw-r--r--   0 user      (1000) user      (1001)     9202 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/models/orders.py
+-rw-r--r--   0 user      (1000) user      (1001)    25488 2023-07-23 20:29:29.000000 python-univer-1.4.6/univer_db/models/roles.py
+-rw-r--r--   0 user      (1000) user      (1001)     4182 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/models/schedule.py
+-rw-r--r--   0 user      (1000) user      (1001)     3558 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/models/sheets.py
+-rw-r--r--   0 user      (1000) user      (1001)     5047 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/models/structures.py
+-rw-r--r--   0 user      (1000) user      (1001)      769 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/orm.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 20:31:15.706666 python-univer-1.4.6/univer_db/tests/
+-rw-r--r--   0 user      (1000) user      (1001)      264 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/tests/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)      569 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/tests/geo.py
+-rw-r--r--   0 user      (1000) user      (1001)     2635 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/tests/models.py
+-rw-r--r--   0 user      (1000) user      (1001)     1136 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/tests/roles.py
+-rw-r--r--   0 user      (1000) user      (1001)      624 2023-07-18 16:09:38.000000 python-univer-1.4.6/univer_db/tests/structures.py
```

### Comparing `python-univer-1.4.5/PKG-INFO` & `python-univer-1.4.6/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: python-univer
-Version: 1.4.5
+Version: 1.4.6
 Summary: Данная библиотека содержить SqlAlchemy ORM для системы Univer
 Home-page: https://github.com/yessenovuniversity/python_univer
 Author: Nauryzbek Aitbayev
 Author-email: nauryzbek.aitbayev@yu.edu.kz
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: Other/Proprietary License
 Classifier: Operating System :: OS Independent
```

### Comparing `python-univer-1.4.5/README.md` & `python-univer-1.4.6/README.md`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/python_univer.egg-info/PKG-INFO` & `python-univer-1.4.6/python_univer.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: python-univer
-Version: 1.4.5
+Version: 1.4.6
 Summary: Данная библиотека содержить SqlAlchemy ORM для системы Univer
 Home-page: https://github.com/yessenovuniversity/python_univer
 Author: Nauryzbek Aitbayev
 Author-email: nauryzbek.aitbayev@yu.edu.kz
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: Other/Proprietary License
 Classifier: Operating System :: OS Independent
```

### Comparing `python-univer-1.4.5/python_univer.egg-info/SOURCES.txt` & `python-univer-1.4.6/python_univer.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/setup.py` & `python-univer-1.4.6/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 import setuptools
 
 with open('README.md', 'r', encoding='utf8') as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="python-univer",
-    version="1.4.5",
+    version="1.4.6",
     author="Nauryzbek Aitbayev",
     author_email="nauryzbek.aitbayev@yu.edu.kz",
     description="Данная библиотека содержить SqlAlchemy ORM для системы Univer",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/yessenovuniversity/python_univer",
     packages=setuptools.find_packages(),
```

### Comparing `python-univer-1.4.5/univer_db/models/base.py` & `python-univer-1.4.6/univer_db/models/base.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/models/dormitories.py` & `python-univer-1.4.6/univer_db/models/dormitories.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/models/geo.py` & `python-univer-1.4.6/univer_db/models/geo.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/models/grades.py` & `python-univer-1.4.6/univer_db/models/grades.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/models/models.py` & `python-univer-1.4.6/univer_db/models/models.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/models/orders.py` & `python-univer-1.4.6/univer_db/models/orders.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/models/roles.py` & `python-univer-1.4.6/univer_db/models/roles.py`

 * *Files 2% similar despite different names*

```diff
@@ -363,14 +363,76 @@
 
     def __str__(self):
         full_name = ' '.join(
             filter(None, [self.last_name, self.first_name, self.middle_name]))
         return f'{full_name}'
 
 
+class ParentType(Base):
+    """
+    Тип родителя
+    """
+    __tablename__ = 'univer_parent_types'
+
+    # Идентификатор
+    id = Column('parent_type_id', Integer, primary_key=True)
+
+    # Наименование
+    name_ru = Column(String(200))
+    name_kz = Column(String(200))
+    name_en = Column(String(200))
+
+    # Пол
+    # 0 - Мужчина, 1 - Женщина
+    sex = Column(Integer)
+
+    # Статус
+    # 1 - Активный
+    status = Column(Integer)
+
+    def __repr__(self):
+        return f'<ParentType {self} (id={self.id} status={self.status})>'
+
+    def __str__(self):
+        return self.name_ru
+
+
+class StudentParent(Base):
+    """
+    Родитель студента
+    """
+    __tablename__ = 'univer_student_parents'
+
+    # Студент
+    student_id = Column(ForeignKey('univer_students.students_id'), primary_key=True)
+    student = relationship('Student')
+
+    # Тип родителя
+    type_id = Column('parent_type_id', ForeignKey('univer_parent_types.parent_type_id'), primary_key=True)
+    type = relationship('ParentType')
+
+    # ФИО
+    last_name = Column('parent_sname', Unicode(100))
+    first_name = Column('parent_name', Unicode(100))
+    middle_name = Column('parent_father_name', Unicode(100))
+
+    # Профессия/должность
+    profession = Column(Unicode(250))
+
+    # Место работы
+    work_place = Column(Unicode(250))
+
+    def __repr__(self):
+        return f'<StudentParent {self} (student_id={self.student_id} type_id={self.type_id})>'
+
+    def __str__(self):
+        full_name = ' '.join(filter(None, [self.last_name, self.first_name, self.middle_name]))
+        return full_name
+
+
 class Bachelor(Base):
     """
     Бакалавр
     """
     __tablename__ = 'univer_students_bachelor'
 
     # Идентификатор
```

### Comparing `python-univer-1.4.5/univer_db/models/schedule.py` & `python-univer-1.4.6/univer_db/models/schedule.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/models/sheets.py` & `python-univer-1.4.6/univer_db/models/sheets.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/models/structures.py` & `python-univer-1.4.6/univer_db/models/structures.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/orm.py` & `python-univer-1.4.6/univer_db/orm.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/tests/geo.py` & `python-univer-1.4.6/univer_db/tests/geo.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/tests/models.py` & `python-univer-1.4.6/univer_db/tests/models.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/tests/roles.py` & `python-univer-1.4.6/univer_db/tests/roles.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.5/univer_db/tests/structures.py` & `python-univer-1.4.6/univer_db/tests/structures.py`

 * *Files identical despite different names*

