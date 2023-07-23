# Comparing `tmp/french_cities-0.1.0a5.tar.gz` & `tmp/french_cities-0.1.0a6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "french_cities-0.1.0a5.tar", max compression
+gzip compressed data, was "french_cities-0.1.0a6.tar", max compression
```

## Comparing `french_cities-0.1.0a5.tar` & `french_cities-0.1.0a6.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0      349 2023-07-21 09:11:11.383937 french_cities-0.1.0a5/french_cities/__init__.py
--rw-r--r--   0        0        0    19353 2023-07-21 09:20:08.502684 french_cities-0.1.0a5/french_cities/city_finder.py
--rw-r--r--   0        0        0     4654 2023-07-17 15:18:48.886858 french_cities-0.1.0a5/french_cities/departement_finder.py
--rw-r--r--   0        0        0      335 2023-07-17 15:15:52.270285 french_cities-0.1.0a5/french_cities/utils.py
--rw-r--r--   0        0        0     7791 2023-07-20 14:20:02.786838 french_cities-0.1.0a5/french_cities/vintage.py
--rw-r--r--   0        0        0     1235 2023-07-21 09:11:19.186649 french_cities-0.1.0a5/pyproject.toml
--rw-r--r--   0        0        0     8785 2023-07-20 12:28:33.096467 french_cities-0.1.0a5/README.fr.md
--rw-r--r--   0        0        0     7355 2023-07-20 12:27:35.807255 french_cities-0.1.0a5/README.md
--rw-r--r--   0        0        0    17157 1970-01-01 00:00:00.000000 french_cities-0.1.0a5/PKG-INFO
+-rw-r--r--   0        0        0      349 2023-07-23 11:21:34.268641 french_cities-0.1.0a6/french_cities/__init__.py
+-rw-r--r--   0        0        0    19355 2023-07-23 11:21:59.588139 french_cities-0.1.0a6/french_cities/city_finder.py
+-rw-r--r--   0        0        0     4654 2023-07-17 15:18:48.886858 french_cities-0.1.0a6/french_cities/departement_finder.py
+-rw-r--r--   0        0        0      335 2023-07-17 15:15:52.270285 french_cities-0.1.0a6/french_cities/utils.py
+-rw-r--r--   0        0        0     7791 2023-07-20 14:20:02.786838 french_cities-0.1.0a6/french_cities/vintage.py
+-rw-r--r--   0        0        0     1235 2023-07-23 11:21:28.188916 french_cities-0.1.0a6/pyproject.toml
+-rw-r--r--   0        0        0     8785 2023-07-20 12:28:33.096467 french_cities-0.1.0a6/README.fr.md
+-rw-r--r--   0        0        0     7355 2023-07-20 12:27:35.807255 french_cities-0.1.0a6/README.md
+-rw-r--r--   0        0        0    17157 1970-01-01 00:00:00.000000 french_cities-0.1.0a6/PKG-INFO
```

### Comparing `french_cities-0.1.0a5/french_cities/city_finder.py` & `french_cities-0.1.0a6/french_cities/city_finder.py`

 * *Files 0% similar despite different names*

```diff
@@ -351,15 +351,15 @@
 
     addresses = df.loc[:, components_kept].drop_duplicates().fillna("")
 
     # Add dep recognition if not already there, just to check the result's
     # coherence (and NOT to compute city recognition using it!)
     if dep not in components_kept:
         addresses = find_departements(
-            addresses, postcode, dep, postcode, session
+            addresses, postcode, dep, "postcode", session
         )
 
     for k, components in enumerate(to_test_ok):
 
         def list_map(df, columns):
             # contatenation of multiple columns
             "https://stackoverflow.com/questions/39291499#answer-62135779"
```

### Comparing `french_cities-0.1.0a5/french_cities/departement_finder.py` & `french_cities-0.1.0a6/french_cities/departement_finder.py`

 * *Files identical despite different names*

### Comparing `french_cities-0.1.0a5/french_cities/vintage.py` & `french_cities-0.1.0a6/french_cities/vintage.py`

 * *Files identical despite different names*

### Comparing `french_cities-0.1.0a5/pyproject.toml` & `french_cities-0.1.0a6/pyproject.toml`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "french-cities"
-version = "0.1.0a5"
+version = "0.1.0a6"
 description = "Toolbox on french cities: set vintage, find departments, find cities..."
 authors = ["thomas.grandjean <thomas.grandjean@developpement-durable.gouv.fr>"]
 license = "etalab-2.0"
 readme = ["README.md", "README.fr.md"]
 homepage = "https://github.com/tgrandje/french-cities/"
 repository = "https://github.com/tgrandje/french-cities/"
 documentation = "https://github.com/tgrandje/french-cities/"
```

### Comparing `french_cities-0.1.0a5/README.fr.md` & `french_cities-0.1.0a6/README.fr.md`

 * *Files identical despite different names*

### Comparing `french_cities-0.1.0a5/README.md` & `french_cities-0.1.0a6/README.md`

 * *Files identical despite different names*

### Comparing `french_cities-0.1.0a5/PKG-INFO` & `french_cities-0.1.0a6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: french-cities
-Version: 0.1.0a5
+Version: 0.1.0a6
 Summary: Toolbox on french cities: set vintage, find departments, find cities...
 Home-page: https://github.com/tgrandje/french-cities/
 License: etalab-2.0
 Keywords: france,cities
 Author: thomas.grandjean
 Author-email: thomas.grandjean@developpement-durable.gouv.fr
 Requires-Python: >=3.8,<4.0
```

