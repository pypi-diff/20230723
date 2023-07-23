# Comparing `tmp/french_cities-0.1.0a6.tar.gz` & `tmp/french_cities-0.1.0a7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "french_cities-0.1.0a6.tar", max compression
+gzip compressed data, was "french_cities-0.1.0a7.tar", max compression
```

## Comparing `french_cities-0.1.0a6.tar` & `french_cities-0.1.0a7.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0      349 2023-07-23 11:21:34.268641 french_cities-0.1.0a6/french_cities/__init__.py
--rw-r--r--   0        0        0    19355 2023-07-23 11:21:59.588139 french_cities-0.1.0a6/french_cities/city_finder.py
--rw-r--r--   0        0        0     4654 2023-07-17 15:18:48.886858 french_cities-0.1.0a6/french_cities/departement_finder.py
--rw-r--r--   0        0        0      335 2023-07-17 15:15:52.270285 french_cities-0.1.0a6/french_cities/utils.py
--rw-r--r--   0        0        0     7791 2023-07-20 14:20:02.786838 french_cities-0.1.0a6/french_cities/vintage.py
--rw-r--r--   0        0        0     1235 2023-07-23 11:21:28.188916 french_cities-0.1.0a6/pyproject.toml
--rw-r--r--   0        0        0     8785 2023-07-20 12:28:33.096467 french_cities-0.1.0a6/README.fr.md
--rw-r--r--   0        0        0     7355 2023-07-20 12:27:35.807255 french_cities-0.1.0a6/README.md
--rw-r--r--   0        0        0    17157 1970-01-01 00:00:00.000000 french_cities-0.1.0a6/PKG-INFO
+-rw-r--r--   0        0        0      349 2023-07-23 12:10:10.458604 french_cities-0.1.0a7/french_cities/__init__.py
+-rw-r--r--   0        0        0    19360 2023-07-23 12:06:30.774859 french_cities-0.1.0a7/french_cities/city_finder.py
+-rw-r--r--   0        0        0     4654 2023-07-17 15:18:48.886858 french_cities-0.1.0a7/french_cities/departement_finder.py
+-rw-r--r--   0        0        0      335 2023-07-17 15:15:52.270285 french_cities-0.1.0a7/french_cities/utils.py
+-rw-r--r--   0        0        0     7844 2023-07-23 11:38:50.970042 french_cities-0.1.0a7/french_cities/vintage.py
+-rw-r--r--   0        0        0     1235 2023-07-23 12:10:22.989876 french_cities-0.1.0a7/pyproject.toml
+-rw-r--r--   0        0        0     8785 2023-07-20 12:28:33.096467 french_cities-0.1.0a7/README.fr.md
+-rw-r--r--   0        0        0     7355 2023-07-20 12:27:35.807255 french_cities-0.1.0a7/README.md
+-rw-r--r--   0        0        0    17157 1970-01-01 00:00:00.000000 french_cities-0.1.0a7/PKG-INFO
```

### Comparing `french_cities-0.1.0a6/french_cities/city_finder.py` & `french_cities-0.1.0a7/french_cities/city_finder.py`

 * *Files 1% similar despite different names*

```diff
@@ -149,15 +149,15 @@
             int(year)
         except ValueError:
             raise ValueError(
                 "year should either be castable to int or 'last', "
                 f"found {year} instead"
             )
 
-    if year not in {str(date.today().year), "last"}:
+    if str(year) not in {str(date.today().year), "last"}:
         logger.warning(
             "As of yet, ADMINEXPRESS can't be fetched with a vintage "
             "setting: the querying of cities using coordinates WILL have "
             "approximative results."
         )
 
     com = get_geodata("ADMINEXPRESS-COG-CARTO.LATEST:commune")
```

### Comparing `french_cities-0.1.0a6/french_cities/departement_finder.py` & `french_cities-0.1.0a7/french_cities/departement_finder.py`

 * *Files identical despite different names*

### Comparing `french_cities-0.1.0a6/french_cities/vintage.py` & `french_cities-0.1.0a7/french_cities/vintage.py`

 * *Files 1% similar despite different names*

```diff
@@ -229,15 +229,18 @@
 
     renamed = False
     if field in {"CODE, NEW_CODE"}:
         renamed = True
         df = df.rename({field: f"temp_{field}"}, axis=1)
         field = f"temp_{field}"
 
-    uniques = df[[field]].drop_duplicates(keep="first")
+    uniques = df[[field]].drop_duplicates(keep="first").dropna()
+
+    if uniques.empty:
+        return df
 
     cities = _get_cities_year_full(year, set(uniques[field]))
 
     # Uptodate cities (cities, municipal districts, delegated cities, ...)
     uniques = uniques.merge(cities, left_on=field, right_on="CODE", how="left")
     uniques = uniques.rename({"NEW_CODE": "PROJECTED"}, axis=1)
```

### Comparing `french_cities-0.1.0a6/pyproject.toml` & `french_cities-0.1.0a7/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "french-cities"
-version = "0.1.0a6"
+version = "0.1.0a7"
 description = "Toolbox on french cities: set vintage, find departments, find cities..."
 authors = ["thomas.grandjean <thomas.grandjean@developpement-durable.gouv.fr>"]
 license = "etalab-2.0"
 readme = ["README.md", "README.fr.md"]
 homepage = "https://github.com/tgrandje/french-cities/"
 repository = "https://github.com/tgrandje/french-cities/"
 documentation = "https://github.com/tgrandje/french-cities/"
```

### Comparing `french_cities-0.1.0a6/README.fr.md` & `french_cities-0.1.0a7/README.fr.md`

 * *Files identical despite different names*

### Comparing `french_cities-0.1.0a6/README.md` & `french_cities-0.1.0a7/README.md`

 * *Files identical despite different names*

### Comparing `french_cities-0.1.0a6/PKG-INFO` & `french_cities-0.1.0a7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: french-cities
-Version: 0.1.0a6
+Version: 0.1.0a7
 Summary: Toolbox on french cities: set vintage, find departments, find cities...
 Home-page: https://github.com/tgrandje/french-cities/
 License: etalab-2.0
 Keywords: france,cities
 Author: thomas.grandjean
 Author-email: thomas.grandjean@developpement-durable.gouv.fr
 Requires-Python: >=3.8,<4.0
```

