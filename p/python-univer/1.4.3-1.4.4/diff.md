# Comparing `tmp/python-univer-1.4.3.tar.gz` & `tmp/python-univer-1.4.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "python-univer-1.4.3.tar", last modified: Sun Jul 23 11:20:30 2023, max compression
+gzip compressed data, was "python-univer-1.4.4.tar", last modified: Sun Jul 23 12:02:21 2023, max compression
```

## Comparing `python-univer-1.4.3.tar` & `python-univer-1.4.4.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 11:20:30.299998 python-univer-1.4.3/
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.3/LICENSE
--rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 11:20:30.299998 python-univer-1.4.3/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1001)      706 2023-07-18 16:09:38.000000 python-univer-1.4.3/README.md
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 11:20:30.296665 python-univer-1.4.3/python_univer.egg-info/
--rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 11:20:30.000000 python-univer-1.4.3/python_univer.egg-info/PKG-INFO
--rw-r--r--   0 user      (1000) user      (1001)      732 2023-07-23 11:20:30.000000 python-univer-1.4.3/python_univer.egg-info/SOURCES.txt
--rw-r--r--   0 user      (1000) user      (1001)        1 2023-07-23 11:20:30.000000 python-univer-1.4.3/python_univer.egg-info/dependency_links.txt
--rw-r--r--   0 user      (1000) user      (1001)       18 2023-07-23 11:20:30.000000 python-univer-1.4.3/python_univer.egg-info/requires.txt
--rw-r--r--   0 user      (1000) user      (1001)       10 2023-07-23 11:20:30.000000 python-univer-1.4.3/python_univer.egg-info/top_level.txt
--rw-r--r--   0 user      (1000) user      (1001)       38 2023-07-23 11:20:30.299998 python-univer-1.4.3/setup.cfg
--rw-r--r--   0 user      (1000) user      (1001)      891 2023-07-23 11:18:56.000000 python-univer-1.4.3/setup.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 11:20:30.296665 python-univer-1.4.3/univer_db/
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)      472 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/config.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 11:20:30.299998 python-univer-1.4.3/univer_db/models/
--rw-r--r--   0 user      (1000) user      (1001)      225 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)     9234 2023-07-23 10:05:33.000000 python-univer-1.4.3/univer_db/models/base.py
--rw-r--r--   0 user      (1000) user      (1001)     8231 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/dormitories.py
--rw-r--r--   0 user      (1000) user      (1001)     1873 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/geo.py
--rw-r--r--   0 user      (1000) user      (1001)      951 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/grades.py
--rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/groups.py
--rw-r--r--   0 user      (1000) user      (1001)    35329 2023-07-23 11:18:08.000000 python-univer-1.4.3/univer_db/models/models.py
--rw-r--r--   0 user      (1000) user      (1001)     9202 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/orders.py
--rw-r--r--   0 user      (1000) user      (1001)    23099 2023-07-23 11:05:03.000000 python-univer-1.4.3/univer_db/models/roles.py
--rw-r--r--   0 user      (1000) user      (1001)     4182 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/schedule.py
--rw-r--r--   0 user      (1000) user      (1001)     3558 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/sheets.py
--rw-r--r--   0 user      (1000) user      (1001)     5047 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/models/structures.py
--rw-r--r--   0 user      (1000) user      (1001)      769 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/orm.py
-drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 11:20:30.299998 python-univer-1.4.3/univer_db/tests/
--rw-r--r--   0 user      (1000) user      (1001)      264 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/tests/__init__.py
--rw-r--r--   0 user      (1000) user      (1001)      569 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/tests/geo.py
--rw-r--r--   0 user      (1000) user      (1001)     2635 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/tests/models.py
--rw-r--r--   0 user      (1000) user      (1001)     1136 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/tests/roles.py
--rw-r--r--   0 user      (1000) user      (1001)      624 2023-07-18 16:09:38.000000 python-univer-1.4.3/univer_db/tests/structures.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 12:02:20.996664 python-univer-1.4.4/
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.4/LICENSE
+-rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 12:02:20.996664 python-univer-1.4.4/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1001)      706 2023-07-18 16:09:38.000000 python-univer-1.4.4/README.md
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 12:02:20.996664 python-univer-1.4.4/python_univer.egg-info/
+-rw-r--r--   0 user      (1000) user      (1001)     1233 2023-07-23 12:02:20.000000 python-univer-1.4.4/python_univer.egg-info/PKG-INFO
+-rw-r--r--   0 user      (1000) user      (1001)      732 2023-07-23 12:02:20.000000 python-univer-1.4.4/python_univer.egg-info/SOURCES.txt
+-rw-r--r--   0 user      (1000) user      (1001)        1 2023-07-23 12:02:20.000000 python-univer-1.4.4/python_univer.egg-info/dependency_links.txt
+-rw-r--r--   0 user      (1000) user      (1001)       18 2023-07-23 12:02:20.000000 python-univer-1.4.4/python_univer.egg-info/requires.txt
+-rw-r--r--   0 user      (1000) user      (1001)       10 2023-07-23 12:02:20.000000 python-univer-1.4.4/python_univer.egg-info/top_level.txt
+-rw-r--r--   0 user      (1000) user      (1001)       38 2023-07-23 12:02:20.996664 python-univer-1.4.4/setup.cfg
+-rw-r--r--   0 user      (1000) user      (1001)      891 2023-07-23 12:02:05.000000 python-univer-1.4.4/setup.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 12:02:20.996664 python-univer-1.4.4/univer_db/
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)      472 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/config.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 12:02:20.996664 python-univer-1.4.4/univer_db/models/
+-rw-r--r--   0 user      (1000) user      (1001)      225 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/models/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)     9234 2023-07-23 10:05:33.000000 python-univer-1.4.4/univer_db/models/base.py
+-rw-r--r--   0 user      (1000) user      (1001)     8231 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/models/dormitories.py
+-rw-r--r--   0 user      (1000) user      (1001)     1873 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/models/geo.py
+-rw-r--r--   0 user      (1000) user      (1001)      951 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/models/grades.py
+-rw-r--r--   0 user      (1000) user      (1001)        0 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/models/groups.py
+-rw-r--r--   0 user      (1000) user      (1001)    35329 2023-07-23 11:18:08.000000 python-univer-1.4.4/univer_db/models/models.py
+-rw-r--r--   0 user      (1000) user      (1001)     9202 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/models/orders.py
+-rw-r--r--   0 user      (1000) user      (1001)    23773 2023-07-23 12:01:37.000000 python-univer-1.4.4/univer_db/models/roles.py
+-rw-r--r--   0 user      (1000) user      (1001)     4182 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/models/schedule.py
+-rw-r--r--   0 user      (1000) user      (1001)     3558 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/models/sheets.py
+-rw-r--r--   0 user      (1000) user      (1001)     5047 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/models/structures.py
+-rw-r--r--   0 user      (1000) user      (1001)      769 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/orm.py
+drwxr-xr-x   0 user      (1000) user      (1001)        0 2023-07-23 12:02:20.996664 python-univer-1.4.4/univer_db/tests/
+-rw-r--r--   0 user      (1000) user      (1001)      264 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/tests/__init__.py
+-rw-r--r--   0 user      (1000) user      (1001)      569 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/tests/geo.py
+-rw-r--r--   0 user      (1000) user      (1001)     2635 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/tests/models.py
+-rw-r--r--   0 user      (1000) user      (1001)     1136 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/tests/roles.py
+-rw-r--r--   0 user      (1000) user      (1001)      624 2023-07-18 16:09:38.000000 python-univer-1.4.4/univer_db/tests/structures.py
```

### Comparing `python-univer-1.4.3/PKG-INFO` & `python-univer-1.4.4/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: python-univer
-Version: 1.4.3
+Version: 1.4.4
 Summary: Данная библиотека содержить SqlAlchemy ORM для системы Univer
 Home-page: https://github.com/yessenovuniversity/python_univer
 Author: Nauryzbek Aitbayev
 Author-email: nauryzbek.aitbayev@yu.edu.kz
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: Other/Proprietary License
 Classifier: Operating System :: OS Independent
```

### Comparing `python-univer-1.4.3/README.md` & `python-univer-1.4.4/README.md`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/python_univer.egg-info/PKG-INFO` & `python-univer-1.4.4/python_univer.egg-info/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: python-univer
-Version: 1.4.3
+Version: 1.4.4
 Summary: Данная библиотека содержить SqlAlchemy ORM для системы Univer
 Home-page: https://github.com/yessenovuniversity/python_univer
 Author: Nauryzbek Aitbayev
 Author-email: nauryzbek.aitbayev@yu.edu.kz
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: Other/Proprietary License
 Classifier: Operating System :: OS Independent
```

### Comparing `python-univer-1.4.3/python_univer.egg-info/SOURCES.txt` & `python-univer-1.4.4/python_univer.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/setup.py` & `python-univer-1.4.4/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 import setuptools
 
 with open('README.md', 'r', encoding='utf8') as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="python-univer",
-    version="1.4.3",
+    version="1.4.4",
     author="Nauryzbek Aitbayev",
     author_email="nauryzbek.aitbayev@yu.edu.kz",
     description="Данная библиотека содержить SqlAlchemy ORM для системы Univer",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/yessenovuniversity/python_univer",
     packages=setuptools.find_packages(),
```

### Comparing `python-univer-1.4.3/univer_db/models/base.py` & `python-univer-1.4.4/univer_db/models/base.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/models/dormitories.py` & `python-univer-1.4.4/univer_db/models/dormitories.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/models/geo.py` & `python-univer-1.4.4/univer_db/models/geo.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/models/grades.py` & `python-univer-1.4.4/univer_db/models/grades.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/models/models.py` & `python-univer-1.4.4/univer_db/models/models.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/models/orders.py` & `python-univer-1.4.4/univer_db/models/orders.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/models/roles.py` & `python-univer-1.4.4/univer_db/models/roles.py`

 * *Files 2% similar despite different names*

```diff
@@ -363,14 +363,40 @@
 
     def __str__(self):
         full_name = ' '.join(
             filter(None, [self.last_name, self.first_name, self.middle_name]))
         return f'{full_name}'
 
 
+class Bachelor(Base):
+    """
+    Бакалавр
+    """
+    __tablename__ = 'univer_students_bachelor'
+
+    # Идентификатор
+    id = Column('students_bachelor_id', Integer, primary_key=True)
+
+    # Студент
+    student_id = Column(ForeignKey('univer_students.students_id'))
+    student = relationship('Student')
+
+    # Неизвестное поле
+    from_address = Column('students_from_adress', String)
+
+    # Достижения студента
+    school_achieve = Column('students_school_achieve', String)
+
+    def __repr__(self):
+        return f'<Bachelor {self} (id={self.id})>'
+
+    def __str__(self):
+        return str(self.student)
+
+
 class Personnel(Base):
     """
     Сотрудник
     """
     __tablename__ = 'univer_personal'
 
     # Идентификатор
```

### Comparing `python-univer-1.4.3/univer_db/models/schedule.py` & `python-univer-1.4.4/univer_db/models/schedule.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/models/sheets.py` & `python-univer-1.4.4/univer_db/models/sheets.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/models/structures.py` & `python-univer-1.4.4/univer_db/models/structures.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/orm.py` & `python-univer-1.4.4/univer_db/orm.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/tests/geo.py` & `python-univer-1.4.4/univer_db/tests/geo.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/tests/models.py` & `python-univer-1.4.4/univer_db/tests/models.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/tests/roles.py` & `python-univer-1.4.4/univer_db/tests/roles.py`

 * *Files identical despite different names*

### Comparing `python-univer-1.4.3/univer_db/tests/structures.py` & `python-univer-1.4.4/univer_db/tests/structures.py`

 * *Files identical despite different names*

