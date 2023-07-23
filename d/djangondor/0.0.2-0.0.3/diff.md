# Comparing `tmp/djangondor-0.0.2.tar.gz` & `tmp/djangondor-0.0.3.tar.gz`

## Comparing `djangondor-0.0.2.tar` & `djangondor-0.0.3.tar`

### file list

```diff
@@ -1,11 +1,14 @@
--rw-r--r--   0        0        0      133 2020-02-02 00:00:00.000000 djangondor-0.0.2/src/djangondor/__about__.py
--rw-r--r--   0        0        0      111 2020-02-02 00:00:00.000000 djangondor-0.0.2/src/djangondor/__init__.py
--rw-r--r--   0        0        0      649 2020-02-02 00:00:00.000000 djangondor-0.0.2/src/djangondor/collections.py
--rw-r--r--   0        0        0     2800 2020-02-02 00:00:00.000000 djangondor-0.0.2/src/djangondor/requests.py
--rw-r--r--   0        0        0      909 2020-02-02 00:00:00.000000 djangondor-0.0.2/src/djangondor/time.py
--rw-r--r--   0        0        0      111 2020-02-02 00:00:00.000000 djangondor-0.0.2/tests/__init__.py
--rw-r--r--   0        0        0     3078 2020-02-02 00:00:00.000000 djangondor-0.0.2/.gitignore
--rw-r--r--   0        0        0     1103 2020-02-02 00:00:00.000000 djangondor-0.0.2/LICENSE.txt
--rw-r--r--   0        0        0      492 2020-02-02 00:00:00.000000 djangondor-0.0.2/README.md
--rw-r--r--   0        0        0     3144 2020-02-02 00:00:00.000000 djangondor-0.0.2/pyproject.toml
--rw-r--r--   0        0        0     1402 2020-02-02 00:00:00.000000 djangondor-0.0.2/PKG-INFO
+-rw-r--r--   0        0        0      133 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/__about__.py
+-rw-r--r--   0        0        0      111 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/__init__.py
+-rw-r--r--   0        0        0      645 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/collections.py
+-rw-r--r--   0        0        0     2800 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/requests.py
+-rw-r--r--   0        0        0      909 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/time.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/templatetags/__init__.py
+-rw-r--r--   0        0        0      410 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/templatetags/djangondor_collection_tags.py
+-rw-r--r--   0        0        0     1601 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/templatetags/djangondor_path_tags.py
+-rw-r--r--   0        0        0      111 2020-02-02 00:00:00.000000 djangondor-0.0.3/tests/__init__.py
+-rw-r--r--   0        0        0     3078 2020-02-02 00:00:00.000000 djangondor-0.0.3/.gitignore
+-rw-r--r--   0        0        0     1103 2020-02-02 00:00:00.000000 djangondor-0.0.3/LICENSE.txt
+-rw-r--r--   0        0        0     1629 2020-02-02 00:00:00.000000 djangondor-0.0.3/README.md
+-rw-r--r--   0        0        0     3144 2020-02-02 00:00:00.000000 djangondor-0.0.3/pyproject.toml
+-rw-r--r--   0        0        0     2539 2020-02-02 00:00:00.000000 djangondor-0.0.3/PKG-INFO
```

### Comparing `djangondor-0.0.2/src/djangondor/collections.py` & `djangondor-0.0.3/src/djangondor/collections.py`

 * *Files 25% similar despite different names*

```diff
@@ -8,14 +8,14 @@
     '''
     lst=[]
     for field in fields:
         lst.append(target[field])
     return lst
 
 
-def value_list(queryset:QuerySet, *fields: str):
+def value_list(queryset:QuerySet, field: str):
     '''
     Generate an actual value list of one item per entry.
     This is meant to make it easier to retrieve list of items
     from `queryset` and we want an item
     '''
-    return list(map(lambda p: p[0], list(queryset.values_list(*fields))))
+    return list(map(lambda p: p[0], list(queryset.values_list(field))))
```

### Comparing `djangondor-0.0.2/src/djangondor/requests.py` & `djangondor-0.0.3/src/djangondor/requests.py`

 * *Files identical despite different names*

### Comparing `djangondor-0.0.2/src/djangondor/time.py` & `djangondor-0.0.3/src/djangondor/time.py`

 * *Files identical despite different names*

### Comparing `djangondor-0.0.2/.gitignore` & `djangondor-0.0.3/.gitignore`

 * *Files identical despite different names*

### Comparing `djangondor-0.0.2/LICENSE.txt` & `djangondor-0.0.3/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `djangondor-0.0.2/pyproject.toml` & `djangondor-0.0.3/pyproject.toml`

 * *Files identical despite different names*

