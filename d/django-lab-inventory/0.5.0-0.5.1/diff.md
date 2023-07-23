# Comparing `tmp/django-lab-inventory-0.5.0.tar.gz` & `tmp/django-lab-inventory-0.5.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django-lab-inventory-0.5.0.tar", last modified: Sun Jul 23 12:08:13 2023, max compression
+gzip compressed data, was "django-lab-inventory-0.5.1.tar", last modified: Sun Jul 23 12:19:31 2023, max compression
```

## Comparing `django-lab-inventory-0.5.0.tar` & `django-lab-inventory-0.5.1.tar`

### file list

```diff
@@ -1,43 +1,48 @@
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.214949 django-lab-inventory-0.5.0/
--rw-r--r--   0 dmeliza    (503) staff       (20)       44 2014-05-14 21:02:10.000000 django-lab-inventory-0.5.0/.gitignore
--rw-r--r--   0 dmeliza    (503) staff       (20)     1461 2023-01-24 20:31:22.000000 django-lab-inventory-0.5.0/COPYING
--rw-r--r--   0 dmeliza    (503) staff       (20)      134 2018-03-09 17:51:12.000000 django-lab-inventory-0.5.0/MANIFEST.in
--rw-r--r--   0 dmeliza    (503) staff       (20)     2261 2023-07-23 12:08:13.215050 django-lab-inventory-0.5.0/PKG-INFO
--rw-r--r--   0 dmeliza    (503) staff       (20)     1484 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/README.md
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.154438 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/
--rw-r--r--   0 dmeliza    (503) staff       (20)     2261 2023-07-23 12:08:13.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/PKG-INFO
--rw-r--r--   0 dmeliza    (503) staff       (20)     1207 2023-07-23 12:08:13.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/SOURCES.txt
--rw-r--r--   0 dmeliza    (503) staff       (20)        1 2023-07-23 12:08:13.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/dependency_links.txt
--rw-r--r--   0 dmeliza    (503) staff       (20)        1 2023-01-24 20:22:01.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/not-zip-safe
--rw-r--r--   0 dmeliza    (503) staff       (20)       49 2023-07-23 12:08:13.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/requires.txt
--rw-r--r--   0 dmeliza    (503) staff       (20)       10 2023-07-23 12:08:13.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/top_level.txt
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.166587 django-lab-inventory-0.5.0/inventory/
--rw-r--r--   0 dmeliza    (503) staff       (20)       69 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/__init__.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     2302 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.0/inventory/admin.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     1694 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/forms.py
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.191534 django-lab-inventory-0.5.0/inventory/migrations/
--rw-r--r--   0 dmeliza    (503) staff       (20)     7543 2019-01-19 00:40:08.000000 django-lab-inventory-0.5.0/inventory/migrations/0001_initial.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     7952 2019-01-19 00:42:07.000000 django-lab-inventory-0.5.0/inventory/migrations/0001_squashed_0003_auto_20150626_1807.py
--rw-r--r--   0 dmeliza    (503) staff       (20)      701 2015-06-26 22:05:53.000000 django-lab-inventory-0.5.0/inventory/migrations/0002_auto_20150626_1805.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     2024 2017-06-23 21:16:49.000000 django-lab-inventory-0.5.0/inventory/migrations/0002_auto_20170623_1716.py
--rw-r--r--   0 dmeliza    (503) staff       (20)      660 2018-03-09 17:39:57.000000 django-lab-inventory-0.5.0/inventory/migrations/0003_add_vendor_email.py
--rw-r--r--   0 dmeliza    (503) staff       (20)      663 2015-06-26 22:07:04.000000 django-lab-inventory-0.5.0/inventory/migrations/0003_auto_20150626_1807.py
--rw-r--r--   0 dmeliza    (503) staff       (20)        0 2014-05-14 16:16:37.000000 django-lab-inventory-0.5.0/inventory/migrations/__init__.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     7055 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.0/inventory/models.py
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.194955 django-lab-inventory-0.5.0/inventory/templates/
--rw-r--r--   0 dmeliza    (503) staff       (20)     2635 2023-01-24 20:21:36.000000 django-lab-inventory-0.5.0/inventory/templates/base_view.html
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.214674 django-lab-inventory-0.5.0/inventory/templates/inventory/
--rw-r--r--   0 dmeliza    (503) staff       (20)     2440 2023-07-20 17:27:51.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/base.html
--rw-r--r--   0 dmeliza    (503) staff       (20)     1093 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/index.html
--rw-r--r--   0 dmeliza    (503) staff       (20)     3545 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/item.html
--rw-r--r--   0 dmeliza    (503) staff       (20)     1305 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/item_entry.html
--rw-r--r--   0 dmeliza    (503) staff       (20)     2411 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/item_list.html
--rw-r--r--   0 dmeliza    (503) staff       (20)     2742 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/order.html
--rw-r--r--   0 dmeliza    (503) staff       (20)     1327 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/order_entry.html
--rw-r--r--   0 dmeliza    (503) staff       (20)     1764 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/order_list.html
--rw-r--r--   0 dmeliza    (503) staff       (20)        0 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/order_table.html
--rw-r--r--   0 dmeliza    (503) staff       (20)       60 2023-07-20 17:28:57.000000 django-lab-inventory-0.5.0/inventory/tests.py
--rw-r--r--   0 dmeliza    (503) staff       (20)      726 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/urls.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     4981 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.0/inventory/views.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     1066 2023-07-23 12:08:13.215902 django-lab-inventory-0.5.0/setup.cfg
--rw-r--r--   0 dmeliza    (503) staff       (20)       84 2023-01-24 20:21:36.000000 django-lab-inventory-0.5.0/setup.py
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:19:31.593927 django-lab-inventory-0.5.1/
+-rw-r--r--   0 dmeliza    (503) staff       (20)       44 2014-05-14 21:02:10.000000 django-lab-inventory-0.5.1/.gitignore
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1461 2023-01-24 20:31:22.000000 django-lab-inventory-0.5.1/COPYING
+-rw-r--r--   0 dmeliza    (503) staff       (20)      168 2023-07-23 12:18:34.000000 django-lab-inventory-0.5.1/MANIFEST.in
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2261 2023-07-23 12:19:31.594049 django-lab-inventory-0.5.1/PKG-INFO
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1484 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.1/README.md
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:19:31.574317 django-lab-inventory-0.5.1/django_lab_inventory.egg-info/
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2261 2023-07-23 12:19:31.000000 django-lab-inventory-0.5.1/django_lab_inventory.egg-info/PKG-INFO
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1515 2023-07-23 12:19:31.000000 django-lab-inventory-0.5.1/django_lab_inventory.egg-info/SOURCES.txt
+-rw-r--r--   0 dmeliza    (503) staff       (20)        1 2023-07-23 12:19:31.000000 django-lab-inventory-0.5.1/django_lab_inventory.egg-info/dependency_links.txt
+-rw-r--r--   0 dmeliza    (503) staff       (20)        1 2023-01-24 20:22:01.000000 django-lab-inventory-0.5.1/django_lab_inventory.egg-info/not-zip-safe
+-rw-r--r--   0 dmeliza    (503) staff       (20)       49 2023-07-23 12:19:31.000000 django-lab-inventory-0.5.1/django_lab_inventory.egg-info/requires.txt
+-rw-r--r--   0 dmeliza    (503) staff       (20)       10 2023-07-23 12:19:31.000000 django-lab-inventory-0.5.1/django_lab_inventory.egg-info/top_level.txt
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:19:31.577238 django-lab-inventory-0.5.1/inventory/
+-rw-r--r--   0 dmeliza    (503) staff       (20)       69 2023-07-23 12:19:07.000000 django-lab-inventory-0.5.1/inventory/__init__.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2302 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.1/inventory/admin.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1694 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.1/inventory/forms.py
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:19:31.586746 django-lab-inventory-0.5.1/inventory/migrations/
+-rw-r--r--   0 dmeliza    (503) staff       (20)     7543 2019-01-19 00:40:08.000000 django-lab-inventory-0.5.1/inventory/migrations/0001_initial.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     7952 2019-01-19 00:42:07.000000 django-lab-inventory-0.5.1/inventory/migrations/0001_squashed_0003_auto_20150626_1807.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)      701 2015-06-26 22:05:53.000000 django-lab-inventory-0.5.1/inventory/migrations/0002_auto_20150626_1805.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2024 2017-06-23 21:16:49.000000 django-lab-inventory-0.5.1/inventory/migrations/0002_auto_20170623_1716.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)      660 2018-03-09 17:39:57.000000 django-lab-inventory-0.5.1/inventory/migrations/0003_add_vendor_email.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)      663 2015-06-26 22:07:04.000000 django-lab-inventory-0.5.1/inventory/migrations/0003_auto_20150626_1807.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1589 2023-01-24 20:21:36.000000 django-lab-inventory-0.5.1/inventory/migrations/0004_alter_category_id_alter_item_id_and_more.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)      722 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.1/inventory/migrations/0005_rename_ptao_account_alter_account_options_and_more.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)      395 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.1/inventory/migrations/0006_rename_ptao_order_account.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2393 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.1/inventory/migrations/0007_remove_duplicates.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1434 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.1/inventory/migrations/0008_add_uniqueness_constraints.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)        0 2014-05-14 16:16:37.000000 django-lab-inventory-0.5.1/inventory/migrations/__init__.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     7055 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.1/inventory/models.py
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:19:31.587629 django-lab-inventory-0.5.1/inventory/templates/
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2635 2023-01-24 20:21:36.000000 django-lab-inventory-0.5.1/inventory/templates/base_view.html
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:19:31.593601 django-lab-inventory-0.5.1/inventory/templates/inventory/
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2440 2023-07-20 17:27:51.000000 django-lab-inventory-0.5.1/inventory/templates/inventory/base.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1093 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.1/inventory/templates/inventory/index.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     3545 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.1/inventory/templates/inventory/item.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1305 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.1/inventory/templates/inventory/item_entry.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2411 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.1/inventory/templates/inventory/item_list.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2742 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.1/inventory/templates/inventory/order.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1327 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.1/inventory/templates/inventory/order_entry.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1764 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.1/inventory/templates/inventory/order_list.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)        0 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.1/inventory/templates/inventory/order_table.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)       60 2023-07-20 17:28:57.000000 django-lab-inventory-0.5.1/inventory/tests.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)      726 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.1/inventory/urls.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     4981 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.1/inventory/views.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1066 2023-07-23 12:19:31.597871 django-lab-inventory-0.5.1/setup.cfg
+-rw-r--r--   0 dmeliza    (503) staff       (20)       84 2023-01-24 20:21:36.000000 django-lab-inventory-0.5.1/setup.py
```

### Comparing `django-lab-inventory-0.5.0/COPYING` & `django-lab-inventory-0.5.1/COPYING`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/PKG-INFO` & `django-lab-inventory-0.5.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-lab-inventory
-Version: 0.5.0
+Version: 0.5.1
 Summary: A simple Django app for managing lab inventory
 Home-page: https://github.com/melizalab/django-lab-inventory
 Author: C Daniel Meliza
 Author-email: dan@meliza.org
 Maintainer: C Daniel Meliza
 Maintainer-email: dan@meliza.org
 License: BSD 3-Clause License
```

### Comparing `django-lab-inventory-0.5.0/README.md` & `django-lab-inventory-0.5.1/README.md`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/django_lab_inventory.egg-info/PKG-INFO` & `django-lab-inventory-0.5.1/django_lab_inventory.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-lab-inventory
-Version: 0.5.0
+Version: 0.5.1
 Summary: A simple Django app for managing lab inventory
 Home-page: https://github.com/melizalab/django-lab-inventory
 Author: C Daniel Meliza
 Author-email: dan@meliza.org
 Maintainer: C Daniel Meliza
 Maintainer-email: dan@meliza.org
 License: BSD 3-Clause License
```

### Comparing `django-lab-inventory-0.5.0/django_lab_inventory.egg-info/SOURCES.txt` & `django-lab-inventory-0.5.1/django_lab_inventory.egg-info/SOURCES.txt`

 * *Files 9% similar despite different names*

```diff
@@ -19,14 +19,19 @@
 inventory/views.py
 inventory/migrations/0001_initial.py
 inventory/migrations/0001_squashed_0003_auto_20150626_1807.py
 inventory/migrations/0002_auto_20150626_1805.py
 inventory/migrations/0002_auto_20170623_1716.py
 inventory/migrations/0003_add_vendor_email.py
 inventory/migrations/0003_auto_20150626_1807.py
+inventory/migrations/0004_alter_category_id_alter_item_id_and_more.py
+inventory/migrations/0005_rename_ptao_account_alter_account_options_and_more.py
+inventory/migrations/0006_rename_ptao_order_account.py
+inventory/migrations/0007_remove_duplicates.py
+inventory/migrations/0008_add_uniqueness_constraints.py
 inventory/migrations/__init__.py
 inventory/templates/base_view.html
 inventory/templates/inventory/base.html
 inventory/templates/inventory/index.html
 inventory/templates/inventory/item.html
 inventory/templates/inventory/item_entry.html
 inventory/templates/inventory/item_list.html
```

### Comparing `django-lab-inventory-0.5.0/inventory/admin.py` & `django-lab-inventory-0.5.1/inventory/admin.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/forms.py` & `django-lab-inventory-0.5.1/inventory/forms.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/migrations/0001_initial.py` & `django-lab-inventory-0.5.1/inventory/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/migrations/0001_squashed_0003_auto_20150626_1807.py` & `django-lab-inventory-0.5.1/inventory/migrations/0001_squashed_0003_auto_20150626_1807.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/migrations/0002_auto_20150626_1805.py` & `django-lab-inventory-0.5.1/inventory/migrations/0002_auto_20150626_1805.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/migrations/0002_auto_20170623_1716.py` & `django-lab-inventory-0.5.1/inventory/migrations/0002_auto_20170623_1716.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/migrations/0003_add_vendor_email.py` & `django-lab-inventory-0.5.1/inventory/migrations/0003_add_vendor_email.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/migrations/0003_auto_20150626_1807.py` & `django-lab-inventory-0.5.1/inventory/migrations/0003_auto_20150626_1807.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/models.py` & `django-lab-inventory-0.5.1/inventory/models.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/templates/base_view.html` & `django-lab-inventory-0.5.1/inventory/templates/base_view.html`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/templates/inventory/base.html` & `django-lab-inventory-0.5.1/inventory/templates/inventory/base.html`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/templates/inventory/index.html` & `django-lab-inventory-0.5.1/inventory/templates/inventory/index.html`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/templates/inventory/item.html` & `django-lab-inventory-0.5.1/inventory/templates/inventory/item.html`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/templates/inventory/item_entry.html` & `django-lab-inventory-0.5.1/inventory/templates/inventory/item_entry.html`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/templates/inventory/item_list.html` & `django-lab-inventory-0.5.1/inventory/templates/inventory/item_list.html`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/templates/inventory/order.html` & `django-lab-inventory-0.5.1/inventory/templates/inventory/order.html`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/templates/inventory/order_entry.html` & `django-lab-inventory-0.5.1/inventory/templates/inventory/order_entry.html`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/templates/inventory/order_list.html` & `django-lab-inventory-0.5.1/inventory/templates/inventory/order_list.html`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/urls.py` & `django-lab-inventory-0.5.1/inventory/urls.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/inventory/views.py` & `django-lab-inventory-0.5.1/inventory/views.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.5.0/setup.cfg` & `django-lab-inventory-0.5.1/setup.cfg`

 * *Files identical despite different names*

