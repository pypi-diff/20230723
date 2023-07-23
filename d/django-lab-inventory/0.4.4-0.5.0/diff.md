# Comparing `tmp/django-lab-inventory-0.4.4.tar.gz` & `tmp/django-lab-inventory-0.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django-lab-inventory-0.4.4.tar", last modified: Tue Jan 24 20:58:52 2023, max compression
+gzip compressed data, was "django-lab-inventory-0.5.0.tar", last modified: Sun Jul 23 12:08:13 2023, max compression
```

## Comparing `django-lab-inventory-0.4.4.tar` & `django-lab-inventory-0.5.0.tar`

### file list

```diff
@@ -1,37 +1,43 @@
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-01-24 20:58:52.213857 django-lab-inventory-0.4.4/
--rw-r--r--   0 dmeliza    (503) staff       (20)       44 2014-05-14 21:02:10.000000 django-lab-inventory-0.4.4/.gitignore
--rw-r--r--   0 dmeliza    (503) staff       (20)     1461 2023-01-24 20:31:22.000000 django-lab-inventory-0.4.4/COPYING
--rw-r--r--   0 dmeliza    (503) staff       (20)      134 2018-03-09 17:51:12.000000 django-lab-inventory-0.4.4/MANIFEST.in
--rw-r--r--   0 dmeliza    (503) staff       (20)     2069 2023-01-24 20:58:52.213966 django-lab-inventory-0.4.4/PKG-INFO
--rw-r--r--   0 dmeliza    (503) staff       (20)     1292 2023-01-24 20:32:34.000000 django-lab-inventory-0.4.4/README.md
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-01-24 20:58:52.201277 django-lab-inventory-0.4.4/django_lab_inventory.egg-info/
--rw-r--r--   0 dmeliza    (503) staff       (20)     2069 2023-01-24 20:58:52.000000 django-lab-inventory-0.4.4/django_lab_inventory.egg-info/PKG-INFO
--rw-r--r--   0 dmeliza    (503) staff       (20)      956 2023-01-24 20:58:52.000000 django-lab-inventory-0.4.4/django_lab_inventory.egg-info/SOURCES.txt
--rw-r--r--   0 dmeliza    (503) staff       (20)        1 2023-01-24 20:58:52.000000 django-lab-inventory-0.4.4/django_lab_inventory.egg-info/dependency_links.txt
--rw-r--r--   0 dmeliza    (503) staff       (20)        1 2023-01-24 20:22:01.000000 django-lab-inventory-0.4.4/django_lab_inventory.egg-info/not-zip-safe
--rw-r--r--   0 dmeliza    (503) staff       (20)       10 2023-01-24 20:58:52.000000 django-lab-inventory-0.4.4/django_lab_inventory.egg-info/top_level.txt
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-01-24 20:58:52.205336 django-lab-inventory-0.4.4/inventory/
--rw-r--r--   0 dmeliza    (503) staff       (20)       70 2023-01-24 20:58:34.000000 django-lab-inventory-0.4.4/inventory/__init__.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     1962 2016-01-13 14:48:43.000000 django-lab-inventory-0.4.4/inventory/admin.py
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-01-24 20:58:52.209418 django-lab-inventory-0.4.4/inventory/migrations/
--rw-r--r--   0 dmeliza    (503) staff       (20)     7543 2019-01-19 00:40:08.000000 django-lab-inventory-0.4.4/inventory/migrations/0001_initial.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     7952 2019-01-19 00:42:07.000000 django-lab-inventory-0.4.4/inventory/migrations/0001_squashed_0003_auto_20150626_1807.py
--rw-r--r--   0 dmeliza    (503) staff       (20)      701 2015-06-26 22:05:53.000000 django-lab-inventory-0.4.4/inventory/migrations/0002_auto_20150626_1805.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     2024 2017-06-23 21:16:49.000000 django-lab-inventory-0.4.4/inventory/migrations/0002_auto_20170623_1716.py
--rw-r--r--   0 dmeliza    (503) staff       (20)      660 2018-03-09 17:39:57.000000 django-lab-inventory-0.4.4/inventory/migrations/0003_add_vendor_email.py
--rw-r--r--   0 dmeliza    (503) staff       (20)      663 2015-06-26 22:07:04.000000 django-lab-inventory-0.4.4/inventory/migrations/0003_auto_20150626_1807.py
--rw-r--r--   0 dmeliza    (503) staff       (20)        0 2014-05-14 16:16:37.000000 django-lab-inventory-0.4.4/inventory/migrations/__init__.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     7132 2023-01-24 20:21:36.000000 django-lab-inventory-0.4.4/inventory/models.py
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-01-24 20:58:52.209915 django-lab-inventory-0.4.4/inventory/templates/
--rw-r--r--   0 dmeliza    (503) staff       (20)     2635 2023-01-24 20:21:36.000000 django-lab-inventory-0.4.4/inventory/templates/base_view.html
-drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-01-24 20:58:52.213253 django-lab-inventory-0.4.4/inventory/templates/inventory/
--rw-r--r--   0 dmeliza    (503) staff       (20)     2440 2014-05-14 16:16:37.000000 django-lab-inventory-0.4.4/inventory/templates/inventory/base.html
--rw-r--r--   0 dmeliza    (503) staff       (20)     1161 2017-06-23 20:14:29.000000 django-lab-inventory-0.4.4/inventory/templates/inventory/index.html
--rw-r--r--   0 dmeliza    (503) staff       (20)     2152 2015-06-26 22:10:57.000000 django-lab-inventory-0.4.4/inventory/templates/inventory/item.html
--rw-r--r--   0 dmeliza    (503) staff       (20)     1583 2015-06-26 22:13:16.000000 django-lab-inventory-0.4.4/inventory/templates/inventory/order.html
--rw-r--r--   0 dmeliza    (503) staff       (20)      781 2014-05-14 21:02:10.000000 django-lab-inventory-0.4.4/inventory/templates/inventory/orders.html
--rw-r--r--   0 dmeliza    (503) staff       (20)       60 2014-02-28 23:04:16.000000 django-lab-inventory-0.4.4/inventory/tests.py
--rw-r--r--   0 dmeliza    (503) staff       (20)      376 2023-01-24 20:21:36.000000 django-lab-inventory-0.4.4/inventory/urls.py
--rw-r--r--   0 dmeliza    (503) staff       (20)     1134 2019-01-19 00:42:50.000000 django-lab-inventory-0.4.4/inventory/views.py
--rw-r--r--   0 dmeliza    (503) staff       (20)      991 2023-01-24 20:58:52.216606 django-lab-inventory-0.4.4/setup.cfg
--rw-r--r--   0 dmeliza    (503) staff       (20)       84 2023-01-24 20:21:36.000000 django-lab-inventory-0.4.4/setup.py
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.214949 django-lab-inventory-0.5.0/
+-rw-r--r--   0 dmeliza    (503) staff       (20)       44 2014-05-14 21:02:10.000000 django-lab-inventory-0.5.0/.gitignore
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1461 2023-01-24 20:31:22.000000 django-lab-inventory-0.5.0/COPYING
+-rw-r--r--   0 dmeliza    (503) staff       (20)      134 2018-03-09 17:51:12.000000 django-lab-inventory-0.5.0/MANIFEST.in
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2261 2023-07-23 12:08:13.215050 django-lab-inventory-0.5.0/PKG-INFO
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1484 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/README.md
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.154438 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2261 2023-07-23 12:08:13.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/PKG-INFO
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1207 2023-07-23 12:08:13.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/SOURCES.txt
+-rw-r--r--   0 dmeliza    (503) staff       (20)        1 2023-07-23 12:08:13.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/dependency_links.txt
+-rw-r--r--   0 dmeliza    (503) staff       (20)        1 2023-01-24 20:22:01.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/not-zip-safe
+-rw-r--r--   0 dmeliza    (503) staff       (20)       49 2023-07-23 12:08:13.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/requires.txt
+-rw-r--r--   0 dmeliza    (503) staff       (20)       10 2023-07-23 12:08:13.000000 django-lab-inventory-0.5.0/django_lab_inventory.egg-info/top_level.txt
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.166587 django-lab-inventory-0.5.0/inventory/
+-rw-r--r--   0 dmeliza    (503) staff       (20)       69 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/__init__.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2302 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.0/inventory/admin.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1694 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/forms.py
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.191534 django-lab-inventory-0.5.0/inventory/migrations/
+-rw-r--r--   0 dmeliza    (503) staff       (20)     7543 2019-01-19 00:40:08.000000 django-lab-inventory-0.5.0/inventory/migrations/0001_initial.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     7952 2019-01-19 00:42:07.000000 django-lab-inventory-0.5.0/inventory/migrations/0001_squashed_0003_auto_20150626_1807.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)      701 2015-06-26 22:05:53.000000 django-lab-inventory-0.5.0/inventory/migrations/0002_auto_20150626_1805.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2024 2017-06-23 21:16:49.000000 django-lab-inventory-0.5.0/inventory/migrations/0002_auto_20170623_1716.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)      660 2018-03-09 17:39:57.000000 django-lab-inventory-0.5.0/inventory/migrations/0003_add_vendor_email.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)      663 2015-06-26 22:07:04.000000 django-lab-inventory-0.5.0/inventory/migrations/0003_auto_20150626_1807.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)        0 2014-05-14 16:16:37.000000 django-lab-inventory-0.5.0/inventory/migrations/__init__.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     7055 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.0/inventory/models.py
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.194955 django-lab-inventory-0.5.0/inventory/templates/
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2635 2023-01-24 20:21:36.000000 django-lab-inventory-0.5.0/inventory/templates/base_view.html
+drwxr-xr-x   0 dmeliza    (503) staff       (20)        0 2023-07-23 12:08:13.214674 django-lab-inventory-0.5.0/inventory/templates/inventory/
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2440 2023-07-20 17:27:51.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/base.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1093 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/index.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     3545 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/item.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1305 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/item_entry.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2411 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/item_list.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     2742 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/order.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1327 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/order_entry.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1764 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/order_list.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)        0 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/templates/inventory/order_table.html
+-rw-r--r--   0 dmeliza    (503) staff       (20)       60 2023-07-20 17:28:57.000000 django-lab-inventory-0.5.0/inventory/tests.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)      726 2023-07-21 18:56:23.000000 django-lab-inventory-0.5.0/inventory/urls.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     4981 2023-07-23 12:07:10.000000 django-lab-inventory-0.5.0/inventory/views.py
+-rw-r--r--   0 dmeliza    (503) staff       (20)     1066 2023-07-23 12:08:13.215902 django-lab-inventory-0.5.0/setup.cfg
+-rw-r--r--   0 dmeliza    (503) staff       (20)       84 2023-01-24 20:21:36.000000 django-lab-inventory-0.5.0/setup.py
```

### Comparing `django-lab-inventory-0.4.4/COPYING` & `django-lab-inventory-0.5.0/COPYING`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.4.4/PKG-INFO` & `django-lab-inventory-0.5.0/PKG-INFO`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-lab-inventory
-Version: 0.4.4
+Version: 0.5.0
 Summary: A simple Django app for managing lab inventory
 Home-page: https://github.com/melizalab/django-lab-inventory
 Author: C Daniel Meliza
 Author-email: dan@meliza.org
 Maintainer: C Daniel Meliza
 Maintainer-email: dan@meliza.org
 License: BSD 3-Clause License
@@ -19,25 +19,25 @@
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: COPYING
 
 
 ## lab-inventory
 
-lab-inventory is a Django application used to track inventory and orders in the lab.
+lab-inventory is a Django application used by our lab to to track inventory and orders. The basic idea is that users add items that can be purchased to the database, and then associate them with orders when they want to get the item. This allows us to quickly locate information about things we have purchased throughout the history of the lab. There is also some rudimentary support for keeping track of where items are located in the lab, when their warranties expire, and other useful information.
 
-The admin interface is the primary tool used to create and update item records, but there is a growing collection of views that can be used to browse the database and generate orders in a format that can be sent off to our purchasing department.
+You'll probably need some familiarity with [Django](https://docs.djangoproject.com) and some knowledge about how to deploy a web application to use it.
 
 lab-inventory is licensed for you to use under the BSD 3-Clause License. See COPYING for details
 
 ### Quick start
 
 1. Requires Python 3.8+ and Django 4.0+
 
-1. Install the package from pypi: `pip install django-labl-inventory`. Worth putting in a virtualenv.
+1. Install the package from pypi: `pip install django-lab-inventory`. Worth putting in a virtualenv.
 
 1. Add `inventory` to your INSTALLED_APPS setting like this:
 
 ```python
 INSTALLED_APPS = (
     ...
     'inventory',
@@ -53,10 +53,7 @@
 3. Run `python manage.py migrate` to create the inventory models.
 
 4. Start the development server and visit http://127.0.0.1:8000/admin/inventory/
    to create items, vendors, manufacturers, etc. (you'll need the Admin app enabled).
 
 5. Visit http://127.0.0.1:8000/inventory/ to use views.
 
-### Bash example
-
-Run [`sh example.sh`](example.sh) to create and run an example of django-lab-inventory. This is very outdated.
```

### Comparing `django-lab-inventory-0.4.4/django_lab_inventory.egg-info/PKG-INFO` & `django-lab-inventory-0.5.0/django_lab_inventory.egg-info/PKG-INFO`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-lab-inventory
-Version: 0.4.4
+Version: 0.5.0
 Summary: A simple Django app for managing lab inventory
 Home-page: https://github.com/melizalab/django-lab-inventory
 Author: C Daniel Meliza
 Author-email: dan@meliza.org
 Maintainer: C Daniel Meliza
 Maintainer-email: dan@meliza.org
 License: BSD 3-Clause License
@@ -19,25 +19,25 @@
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: COPYING
 
 
 ## lab-inventory
 
-lab-inventory is a Django application used to track inventory and orders in the lab.
+lab-inventory is a Django application used by our lab to to track inventory and orders. The basic idea is that users add items that can be purchased to the database, and then associate them with orders when they want to get the item. This allows us to quickly locate information about things we have purchased throughout the history of the lab. There is also some rudimentary support for keeping track of where items are located in the lab, when their warranties expire, and other useful information.
 
-The admin interface is the primary tool used to create and update item records, but there is a growing collection of views that can be used to browse the database and generate orders in a format that can be sent off to our purchasing department.
+You'll probably need some familiarity with [Django](https://docs.djangoproject.com) and some knowledge about how to deploy a web application to use it.
 
 lab-inventory is licensed for you to use under the BSD 3-Clause License. See COPYING for details
 
 ### Quick start
 
 1. Requires Python 3.8+ and Django 4.0+
 
-1. Install the package from pypi: `pip install django-labl-inventory`. Worth putting in a virtualenv.
+1. Install the package from pypi: `pip install django-lab-inventory`. Worth putting in a virtualenv.
 
 1. Add `inventory` to your INSTALLED_APPS setting like this:
 
 ```python
 INSTALLED_APPS = (
     ...
     'inventory',
@@ -53,10 +53,7 @@
 3. Run `python manage.py migrate` to create the inventory models.
 
 4. Start the development server and visit http://127.0.0.1:8000/admin/inventory/
    to create items, vendors, manufacturers, etc. (you'll need the Admin app enabled).
 
 5. Visit http://127.0.0.1:8000/inventory/ to use views.
 
-### Bash example
-
-Run [`sh example.sh`](example.sh) to create and run an example of django-lab-inventory. This is very outdated.
```

### Comparing `django-lab-inventory-0.4.4/django_lab_inventory.egg-info/SOURCES.txt` & `django-lab-inventory-0.5.0/django_lab_inventory.egg-info/SOURCES.txt`

 * *Files 23% similar despite different names*

```diff
@@ -4,17 +4,19 @@
 README.md
 setup.cfg
 setup.py
 django_lab_inventory.egg-info/PKG-INFO
 django_lab_inventory.egg-info/SOURCES.txt
 django_lab_inventory.egg-info/dependency_links.txt
 django_lab_inventory.egg-info/not-zip-safe
+django_lab_inventory.egg-info/requires.txt
 django_lab_inventory.egg-info/top_level.txt
 inventory/__init__.py
 inventory/admin.py
+inventory/forms.py
 inventory/models.py
 inventory/tests.py
 inventory/urls.py
 inventory/views.py
 inventory/migrations/0001_initial.py
 inventory/migrations/0001_squashed_0003_auto_20150626_1807.py
 inventory/migrations/0002_auto_20150626_1805.py
@@ -22,9 +24,13 @@
 inventory/migrations/0003_add_vendor_email.py
 inventory/migrations/0003_auto_20150626_1807.py
 inventory/migrations/__init__.py
 inventory/templates/base_view.html
 inventory/templates/inventory/base.html
 inventory/templates/inventory/index.html
 inventory/templates/inventory/item.html
+inventory/templates/inventory/item_entry.html
+inventory/templates/inventory/item_list.html
 inventory/templates/inventory/order.html
-inventory/templates/inventory/orders.html
+inventory/templates/inventory/order_entry.html
+inventory/templates/inventory/order_list.html
+inventory/templates/inventory/order_table.html
```

### Comparing `django-lab-inventory-0.4.4/inventory/admin.py` & `django-lab-inventory-0.5.0/inventory/admin.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,54 +1,101 @@
 from django.contrib import admin
-from inventory.models import Item, Category, Unit, Manufacturer, Vendor, PTAO, Order, OrderItem
+
+from inventory.models import (
+    Account,
+    Category,
+    Item,
+    Manufacturer,
+    Order,
+    OrderItem,
+    Unit,
+    Vendor,
+)
+
 
 class OrderItemInline(admin.StackedInline):
     model = OrderItem
     extra = 1
 
 
 class ItemAdmin(admin.ModelAdmin):
-    date_hierarchy = 'date_added'
+    date_hierarchy = "date_added"
 
     fieldsets = [
-        (None, {'fields': ['name', 'chem_formula', 'category']}),
-        ('Vendor Information', {'fields': ['vendor', 'catalog', 'manufacturer',
-                                           'manufacturer_number',
-                                           'size', 'unit',]}),
-        (None, {'fields': ['parent_item', 'comments']})
+        (None, {"fields": ["name", "chem_formula", "category"]}),
+        (
+            "Vendor Information",
+            {
+                "fields": [
+                    "vendor",
+                    "catalog",
+                    "manufacturer",
+                    "manufacturer_number",
+                    "size",
+                    "unit",
+                ]
+            },
+        ),
+        (None, {"fields": ["parent_item", "comments"]}),
     ]
 
-    list_display = ('name', 'category', 'date_added',)
-    list_filter = ('category', 'vendor', 'manufacturer', 'date_added')
-    search_fields = ('name', 'chem_formula', 'manufacturer_number', 'comments')
+    list_display = (
+        "name",
+        "category",
+        "vendor",
+        "catalog",
+        "date_added",
+    )
+    list_filter = ("category", "vendor", "manufacturer", "date_added")
+    search_fields = ("name", "chem_formula", "manufacturer_number", "comments")
     inlines = (OrderItemInline,)
 
+
 admin.site.register(Item, ItemAdmin)
 
+
 class OrderAdmin(admin.ModelAdmin):
-    date_hierarchy = 'order_date'
-    fields = ('name', 'order_date', 'ordered_by', 'ordered', 'ptao',)
-    list_display = ('name', 'item_count', 'order_date', 'ordered', 'ptao')
-    list_filter = ('ordered', 'ptao', 'ordered_by')
-    search_fields = ('name',)
+    date_hierarchy = "order_date"
+    fields = (
+        "name",
+        "order_date",
+        "ordered_by",
+        "ordered",
+        "account",
+    )
+    list_display = ("name", "item_count", "order_date", "ordered", "account")
+    list_filter = ("ordered", "account", "ordered_by")
+    search_fields = ("name",)
     inlines = (OrderItemInline,)
 
+
 admin.site.register(Order, OrderAdmin)
 
+
 class OrderItemAdmin(admin.ModelAdmin):
-    date_hierarchy = 'date_arrived'
-    fields = ('units_purchased', 'cost', 'date_arrived', 'serial', 'uva_equip',
-              'location', 'expiry_years', 'reconciled')
-    list_display = ('name', 'order_date', 'date_arrived', 'total_price', 'location')
-    list_filter = ('item__name', 'order__order_date', 'date_arrived', 'location')
+    date_hierarchy = "date_arrived"
+    fields = (
+        "units_purchased",
+        "cost",
+        "date_arrived",
+        "serial",
+        "uva_equip",
+        "location",
+        "expiry_years",
+        "reconciled",
+    )
+    list_display = ("name", "order_date", "date_arrived", "total_price", "location")
+    list_filter = ("item__name", "order__order_date", "date_arrived", "location")
+
 
 admin.site.register(OrderItem, OrderItemAdmin)
 
-class PTAOAdmin(admin.ModelAdmin):
-    fields = ('code', 'description', 'expires')
-    list_display = fields + ('active',)
+
+class AccountAdmin(admin.ModelAdmin):
+    fields = ("code", "description", "expires")
+    list_display = fields
 
 
-admin.site.register(PTAO, PTAOAdmin)
+admin.site.register(Account, AccountAdmin)
 
 for model in (Category, Unit, Manufacturer, Vendor):
     admin.site.register(model)
```

### Comparing `django-lab-inventory-0.4.4/inventory/migrations/0001_initial.py` & `django-lab-inventory-0.5.0/inventory/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.4.4/inventory/migrations/0001_squashed_0003_auto_20150626_1807.py` & `django-lab-inventory-0.5.0/inventory/migrations/0001_squashed_0003_auto_20150626_1807.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.4.4/inventory/migrations/0002_auto_20150626_1805.py` & `django-lab-inventory-0.5.0/inventory/migrations/0002_auto_20150626_1805.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.4.4/inventory/migrations/0002_auto_20170623_1716.py` & `django-lab-inventory-0.5.0/inventory/migrations/0002_auto_20170623_1716.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.4.4/inventory/migrations/0003_add_vendor_email.py` & `django-lab-inventory-0.5.0/inventory/migrations/0003_add_vendor_email.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.4.4/inventory/migrations/0003_auto_20150626_1807.py` & `django-lab-inventory-0.5.0/inventory/migrations/0003_auto_20150626_1807.py`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.4.4/inventory/models.py` & `django-lab-inventory-0.5.0/inventory/models.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,129 +1,141 @@
 # -*- coding: utf-8 -*-
 # -*- mode: python -*-
-from __future__ import unicode_literals
+import datetime
 
 from django.contrib.auth.models import User
-from django.urls import reverse
 from django.db import models
-import datetime
+from django.urls import reverse
 
 
 class Category(models.Model):
     id = models.AutoField(primary_key=True)
-    name = models.CharField(max_length=45)
+    name = models.CharField(max_length=45, unique=True)
 
     def __str__(self):
         return self.name
 
     class Meta:
         verbose_name_plural = "categories"
-        ordering = ['name']
+        ordering = ["name"]
 
 
 class Unit(models.Model):
     id = models.AutoField(primary_key=True)
-    name = models.CharField(max_length=45)
+    name = models.CharField(max_length=45, unique=True)
 
     def __str__(self):
         return self.name
 
     class Meta:
-        ordering = ['name']
+        ordering = ["name"]
 
 
 class Manufacturer(models.Model):
     id = models.AutoField(primary_key=True)
-    name = models.CharField(max_length=64)
+    name = models.CharField(max_length=64, unique=True)
     url = models.CharField(max_length=64, blank=True, null=True)
-    lookup_url = models.CharField(max_length=64, blank=True, null=True,
-                                  help_text="url pattern to look up part number")
+    lookup_url = models.CharField(
+        max_length=64,
+        blank=True,
+        null=True,
+        help_text="url pattern to look up part number",
+    )
     rep = models.CharField(max_length=128, blank=True, null=True)
     rep_phone = models.CharField(max_length=16, blank=True, null=True)
     rep_email = models.CharField(max_length=64, blank=True, null=True)
     support_phone = models.CharField(max_length=16, blank=True, null=True)
 
     def __str__(self):
         return self.name
 
     class Meta:
-        ordering = ['name']
+        ordering = ["name"]
 
 
 class Vendor(models.Model):
     id = models.AutoField(primary_key=True)
-    name = models.CharField(max_length=64)
+    name = models.CharField(max_length=64, unique=True)
     url = models.CharField(max_length=64, blank=True, null=True)
-    lookup_url = models.CharField(max_length=128, blank=True, null=True,
-                                  help_text="url pattern to look up catalog number")
+    lookup_url = models.CharField(
+        max_length=128,
+        blank=True,
+        null=True,
+        help_text="url pattern to look up catalog number",
+    )
     phone = models.CharField(max_length=16, blank=True, null=True)
     rep = models.CharField(max_length=45, blank=True, null=True)
     rep_phone = models.CharField(max_length=16, blank=True, null=True)
     rep_email = models.CharField(max_length=64, blank=True, null=True)
 
     def __str__(self):
         return self.name
 
     class Meta:
-        ordering = ['name']
+        ordering = ["name"]
 
 
-class PTAO(models.Model):
+class Account(models.Model):
     id = models.AutoField(primary_key=True)
     code = models.CharField(max_length=64, unique=True)
     description = models.CharField(max_length=128)
     expires = models.DateField(blank=True, null=True)
 
-    def active(self):
-        if self.expires:
-            return datetime.date.today() < self.expires
-        else:
-            return True
-
     def __str__(self):
-        return "%s (%s)" % (self.code, self.description)
+        return "%s (%s)" % (self.description, self.code)
 
     class Meta:
-        ordering = ['code']
-        verbose_name = "PTAO"
-        verbose_name_plural = "PTAOs"
+        ordering = ["code"]
+        verbose_name = "Account"
+        verbose_name_plural = "Accounts"
 
 
 class Item(models.Model):
     id = models.AutoField(primary_key=True)
     name = models.CharField(max_length=128)
-    chem_formula = models.CharField('Chemical formula', max_length=45,
-                                    blank=True, null=True)
+    chem_formula = models.CharField(
+        "Chemical formula", max_length=45, blank=True, null=True
+    )
 
     vendor = models.ForeignKey(Vendor, on_delete=models.PROTECT)
-    catalog = models.CharField('Catalog number', max_length=45,
-                               blank=True, null=True)
-    manufacturer = models.ForeignKey('Manufacturer', blank=True, null=True,
-                                     on_delete=models.SET_NULL,
-                                     help_text="leave blank if unknown or same as vendor")
-    manufacturer_number = models.CharField(max_length=45,
-                                           blank=True, null=True)
-    size = models.DecimalField('Size of unit',
-                               max_digits=10, decimal_places=2,
-                               blank=True, null=True)
+    catalog = models.CharField("Catalog number", max_length=45, blank=True, null=True)
+    manufacturer = models.ForeignKey(
+        "Manufacturer",
+        blank=True,
+        null=True,
+        on_delete=models.SET_NULL,
+        help_text="leave blank if unknown or same as vendor",
+    )
+    manufacturer_number = models.CharField(max_length=45, blank=True, null=True)
+    size = models.DecimalField(
+        "Size of unit", max_digits=10, decimal_places=2, blank=True, null=True
+    )
     unit = models.ForeignKey(Unit, on_delete=models.PROTECT)
     category = models.ForeignKey(Category, on_delete=models.PROTECT)
     date_added = models.DateField(auto_now_add=True)
-    parent_item = models.ForeignKey('self', blank=True, null=True,
-                                    on_delete=models.SET_NULL,
-                                    help_text="example: for printer cartriges, select printer")
+    parent_item = models.ForeignKey(
+        "self",
+        blank=True,
+        null=True,
+        on_delete=models.SET_NULL,
+        help_text="example: for printer cartriges, select printer",
+    )
     comments = models.TextField(blank=True)
 
     def __str__(self):
         return self.name
 
     def unit_size(self):
-        return "%s%s%s" % (self.size or "",
-                           "" if str(self.unit).startswith("/") else " ",
-                           self.unit)
+        if self.unit.name == "each":
+            return self.unit.name
+        return "%s%s%s" % (
+            self.size or "",
+            "" if str(self.unit).startswith("/") else " ",
+            self.unit,
+        )
 
     def total_price(self):
         return (self.cost or 0) * self.units_purchased
 
     def vendor_url(self):
         try:
             return self.vendor.lookup_url % self.catalog
@@ -133,25 +145,33 @@
     def mfg_url(self):
         try:
             return self.manufacturer.lookup_url % self.manufacturer_number
         except (AttributeError, TypeError):
             return None
 
     def get_absolute_url(self):
-        return reverse("inventory:item", kwargs={'pk': self.pk})
+        return reverse("inventory:item", kwargs={"pk": self.pk})
 
+    class Meta:
+        constraints = [
+            models.UniqueConstraint(
+                fields=["vendor", "catalog"], name="unique_vendor_catalog_number"
+            )
+        ]
 
 
 class Order(models.Model):
     id = models.AutoField(primary_key=True)
     name = models.CharField(max_length=64)
     created = models.DateTimeField(auto_now_add=True)
-    items = models.ManyToManyField(Item, through='OrderItem')
-    ptao = models.ForeignKey(PTAO, blank=True, null=True, on_delete=models.SET_NULL)
-    ordered = models.BooleanField()
+    items = models.ManyToManyField(Item, through="OrderItem")
+    account = models.ForeignKey(
+        Account, blank=True, null=True, on_delete=models.SET_NULL
+    )
+    ordered = models.BooleanField(default=False)
     order_date = models.DateField(default=datetime.date.today)
     ordered_by = models.ForeignKey(User, on_delete=models.PROTECT)
 
     def __str__(self):
         if self.ordered:
             status = self.order_date
         else:
@@ -159,40 +179,50 @@
         return "%s (%s)" % (self.name, status)
 
     @property
     def item_count(self):
         return self.items.count
 
     def get_absolute_url(self):
-        return reverse("inventory:order", kwargs={'pk': self.pk})
+        return reverse("inventory:order", kwargs={"pk": self.pk})
 
     class Meta:
-        ordering = ['-order_date', 'name']
+        ordering = ["-created"]
 
 
 class OrderItem(models.Model):
     id = models.AutoField(primary_key=True)
-    item  = models.ForeignKey(Item, on_delete=models.CASCADE)
+    item = models.ForeignKey(Item, on_delete=models.CASCADE)
     order = models.ForeignKey(Order, on_delete=models.CASCADE)
 
     units_purchased = models.IntegerField()
-    cost = models.DecimalField('Cost per unit', max_digits=10, decimal_places=2,
-                               blank=True, null=True)
+    cost = models.DecimalField(
+        "Cost per unit", max_digits=10, decimal_places=2, blank=True, null=True
+    )
 
     date_arrived = models.DateField(blank=True, null=True)
-    serial = models.CharField('Serial number', max_length=45,
-                              blank=True, null=True)
-    uva_equip = models.CharField('UVa equipment number', max_length=32,
-                                 blank=True, null=True)
-    location = models.CharField(max_length=45, blank=True, null=True,
-                                help_text="example: -80 freezer, refrigerator, Gilmer 283")
-    expiry_years = models.DecimalField('Warranty or Item expiration (y)', max_digits=4,
-                                       decimal_places=2, blank=True, null=True)
+    serial = models.CharField("Serial number", max_length=45, blank=True, null=True)
+    uva_equip = models.CharField(
+        "UVa equipment number", max_length=32, blank=True, null=True
+    )
+    location = models.CharField(
+        max_length=45,
+        blank=True,
+        null=True,
+        help_text="example: -80 freezer, refrigerator, Gilmer 283",
+    )
+    expiry_years = models.DecimalField(
+        "Warranty or Item expiration (y)",
+        max_digits=4,
+        decimal_places=2,
+        blank=True,
+        null=True,
+    )
 
-    reconciled = models.BooleanField()
+    reconciled = models.BooleanField(default=False)
 
     def total_price(self):
         return (self.cost or 0) * self.units_purchased
 
     def name(self):
         return self.item.name
```

### Comparing `django-lab-inventory-0.4.4/inventory/templates/base_view.html` & `django-lab-inventory-0.5.0/inventory/templates/base_view.html`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.4.4/inventory/templates/inventory/base.html` & `django-lab-inventory-0.5.0/inventory/templates/inventory/base.html`

 * *Files identical despite different names*

### Comparing `django-lab-inventory-0.4.4/setup.cfg` & `django-lab-inventory-0.5.0/setup.cfg`

 * *Files 10% similar despite different names*

```diff
@@ -26,14 +26,17 @@
 [options]
 zip_safe = false
 include_package_data = true
 packages = inventory
 python_requires = >= 3.8
 setup_requires = 
 	setuptools
+install_requires = 
+	django-filter >= 22.1
+	django-widget-tweaks >= 1.4.12
 test_suite = inventory.tests
 
 [options.packages.find]
 exclude = *test*
 
 [egg_info]
 tag_build =
```

