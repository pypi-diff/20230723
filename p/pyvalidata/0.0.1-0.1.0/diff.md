# Comparing `tmp/pyvalidata-0.0.1.tar.gz` & `tmp/pyvalidata-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyvalidata-0.0.1.tar", last modified: Sun Jul 23 21:55:30 2023, max compression
+gzip compressed data, was "pyvalidata-0.1.0.tar", last modified: Sun Jul 23 07:11:21 2023, max compression
```

## Comparing `pyvalidata-0.0.1.tar` & `pyvalidata-0.1.0.tar`

### file list

```diff
@@ -1,14 +1,13 @@
-drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 21:55:30.660827 pyvalidata-0.0.1/
--rw-r--r--   0 eklavyatomar   (502) staff       (20)     1074 2023-07-21 12:41:43.000000 pyvalidata-0.0.1/LICENSE
--rw-r--r--   0 eklavyatomar   (502) staff       (20)     2096 2023-07-23 21:55:30.660635 pyvalidata-0.0.1/PKG-INFO
--rw-r--r--   0 eklavyatomar   (502) staff       (20)     1635 2023-07-23 07:39:22.000000 pyvalidata-0.0.1/README.md
-drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 21:55:30.659603 pyvalidata-0.0.1/pyvalidata/
--rw-r--r--   0 eklavyatomar   (502) staff       (20)     9564 2023-07-23 21:51:14.000000 pyvalidata-0.0.1/pyvalidata/__init__.py
--rw-r--r--   0 eklavyatomar   (502) staff       (20)     3699 2023-07-23 21:49:51.000000 pyvalidata-0.0.1/pyvalidata/validators.py
-drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 21:55:30.660368 pyvalidata-0.0.1/pyvalidata.egg-info/
--rw-r--r--   0 eklavyatomar   (502) staff       (20)     2096 2023-07-23 21:55:30.000000 pyvalidata-0.0.1/pyvalidata.egg-info/PKG-INFO
--rw-r--r--   0 eklavyatomar   (502) staff       (20)      210 2023-07-23 21:55:30.000000 pyvalidata-0.0.1/pyvalidata.egg-info/SOURCES.txt
--rw-r--r--   0 eklavyatomar   (502) staff       (20)        1 2023-07-23 21:55:30.000000 pyvalidata-0.0.1/pyvalidata.egg-info/dependency_links.txt
--rw-r--r--   0 eklavyatomar   (502) staff       (20)       11 2023-07-23 21:55:30.000000 pyvalidata-0.0.1/pyvalidata.egg-info/top_level.txt
--rw-r--r--   0 eklavyatomar   (502) staff       (20)       38 2023-07-23 21:55:30.660892 pyvalidata-0.0.1/setup.cfg
--rw-r--r--   0 eklavyatomar   (502) staff       (20)      691 2023-07-23 21:52:35.000000 pyvalidata-0.0.1/setup.py
+drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 07:11:21.233834 pyvalidata-0.1.0/
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)     1074 2023-07-21 12:41:43.000000 pyvalidata-0.1.0/LICENSE
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)      724 2023-07-23 07:11:21.233636 pyvalidata-0.1.0/PKG-INFO
+drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 07:11:21.232440 pyvalidata-0.1.0/pyvalidata/
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)     8514 2023-07-22 08:57:48.000000 pyvalidata-0.1.0/pyvalidata/__init__.py
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)     4048 2023-07-23 07:05:18.000000 pyvalidata-0.1.0/pyvalidata/validators.py
+drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 07:11:21.233350 pyvalidata-0.1.0/pyvalidata.egg-info/
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)      724 2023-07-23 07:11:21.000000 pyvalidata-0.1.0/pyvalidata.egg-info/PKG-INFO
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)      200 2023-07-23 07:11:21.000000 pyvalidata-0.1.0/pyvalidata.egg-info/SOURCES.txt
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)        1 2023-07-23 07:11:21.000000 pyvalidata-0.1.0/pyvalidata.egg-info/dependency_links.txt
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)       11 2023-07-23 07:11:21.000000 pyvalidata-0.1.0/pyvalidata.egg-info/top_level.txt
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)       38 2023-07-23 07:11:21.233925 pyvalidata-0.1.0/setup.cfg
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)      778 2023-07-21 12:41:28.000000 pyvalidata-0.1.0/setup.py
```

### Comparing `pyvalidata-0.0.1/LICENSE` & `pyvalidata-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pyvalidata-0.0.1/pyvalidata/__init__.py` & `pyvalidata-0.1.0/pyvalidata/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -213,42 +213,15 @@
 
 
 
 
     ###validate_date(date)
 
 
-    This function validates if a given date is in the format that is specified by the user. Accepted date formats are YYYY/MM/DD, MM/DD/YYYY,DD/MM/YYYY.
-
-
-
-
-    
-
-    ###validate_url(url)
-
-    This function checks if a given url is in an url format. The validate_url considers the following url formats as acceptable:
-
-    URLs with or without "http://" or "https://" prefixes.
-    URLs with or without "www." before the domain name.
-    URLs with alphanumeric characters, hyphens ("-"), and dots (".") in the domain name.
-    URLs with domain names ending in two or more alphabetic characters (e.g., ".com", ".org", ".net").
-
-
-
-    Note that the function does not check if the URL is reachable or if it exists. It only checks the pattern of the url.
-
-
-
-    ###validate_custom(data, data_type=None, min_value=None, max_value=None, max_length=None, min_length=None, not_null=False, pattern=None)
-
-
-    With this function, the user can set their own custom rules for some given data in order to validate if it follows their rules or not. It isn't really a new function, but rather a combination of some previous functions.
-
-
+    This function validates if a given date is in the format YYYY/MM/DD.
 
 
     """
 
     print(help_text)
```

### Comparing `pyvalidata-0.0.1/pyvalidata/validators.py` & `pyvalidata-0.1.0/pyvalidata/validators.py`

 * *Files 15% similar despite different names*

```diff
@@ -71,28 +71,35 @@
     # Using a regex pattern for basic URL validation
     url_pattern = r"^(https?://)?(www\.)?[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}(/.*)?$"
     if not re.match(url_pattern, url):
         print("URL validation failed. Invalid URL format.")
         return False
     return True
 
+def validate_with_custom_rule(data, custom_rule_func):
+    if not custom_rule_func(data):
+        print("Custom rule validation failed. Data does not satisfy the custom validation rule.")
+        return False
+    return True
 
-def validate_custom(data, data_type=None, min_value=None, max_value=None, max_length=None, min_length=None, not_null=False, pattern=None):
+def validate_data(data, data_type=None, min_value=None, max_value=None, max_length=None, min_length=None, not_null=False, pattern=None, custom_rule_func=None):
     try:
         is_valid = True
 
         if data_type:
             is_valid &= validate_data_type(data, data_type)
         if isinstance(data, (int, float)):
             is_valid &= validate_range(data, min_value, max_value)
         if isinstance(data, str):
             is_valid &= validate_string_length(data, max_length, min_length)
         if not_null:
             is_valid &= validate_not_null(data)
         if pattern:
             is_valid &= validate_pattern(data, pattern)
+        if custom_rule_func:
+            is_valid &= validate_with_custom_rule(data, custom_rule_func)
 
         return is_valid
 
     except ValueError as e:
         print(f"Validation error: {str(e)}")
         return False
```

### Comparing `pyvalidata-0.0.1/setup.py` & `pyvalidata-0.1.0/setup.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,28 +1,23 @@
 from setuptools import setup
 
-
-VERSION='0.0.3'
-
-
-with open('README.md', 'r', encoding='utf-8') as f:
-    longdescription = f.read()
-
 setup(
     name='pyvalidata',
-    version='0.0.1',
+    version='0.1.0',
     description='A Python package for data validation',
-    long_description=longdescription,
-    long_description_content_type='text/markdown', 
     author='Eklavya Tomar',
     author_email='eklavyaprogramming@gmail.com',
     url='https://github.com/EklavyaT/pyvalidata',
     packages=['pyvalidata'],
     install_requires=[],
     classifiers=[
+        'Development Status :: 3 - Alpha',
         'License :: OSI Approved :: MIT License',
         'Programming Language :: Python :: 3',
-        'Operating System :: OS Independent',
-        
+        'Programming Language :: Python :: 3.6',
+        'Programming Language :: Python :: 3.7',
+        'Programming Language :: Python :: 3.8',
+        'Programming Language :: Python :: 3.9',
+        'Intended Audience :: Developers',
+        'Topic :: Software Development :: Libraries',
     ],
 )
-
```

