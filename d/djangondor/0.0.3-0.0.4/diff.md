# Comparing `tmp/djangondor-0.0.3.tar.gz` & `tmp/djangondor-0.0.4.tar.gz`

## Comparing `djangondor-0.0.3.tar` & `djangondor-0.0.4.tar`

### file list

```diff
@@ -1,14 +1,14 @@
--rw-r--r--   0        0        0      133 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/__about__.py
--rw-r--r--   0        0        0      111 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/__init__.py
--rw-r--r--   0        0        0      645 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/collections.py
--rw-r--r--   0        0        0     2800 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/requests.py
--rw-r--r--   0        0        0      909 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/time.py
--rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/templatetags/__init__.py
--rw-r--r--   0        0        0      410 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/templatetags/djangondor_collection_tags.py
--rw-r--r--   0        0        0     1601 2020-02-02 00:00:00.000000 djangondor-0.0.3/src/djangondor/templatetags/djangondor_path_tags.py
--rw-r--r--   0        0        0      111 2020-02-02 00:00:00.000000 djangondor-0.0.3/tests/__init__.py
--rw-r--r--   0        0        0     3078 2020-02-02 00:00:00.000000 djangondor-0.0.3/.gitignore
--rw-r--r--   0        0        0     1103 2020-02-02 00:00:00.000000 djangondor-0.0.3/LICENSE.txt
--rw-r--r--   0        0        0     1629 2020-02-02 00:00:00.000000 djangondor-0.0.3/README.md
--rw-r--r--   0        0        0     3144 2020-02-02 00:00:00.000000 djangondor-0.0.3/pyproject.toml
--rw-r--r--   0        0        0     2539 2020-02-02 00:00:00.000000 djangondor-0.0.3/PKG-INFO
+-rw-r--r--   0        0        0      133 2020-02-02 00:00:00.000000 djangondor-0.0.4/src/djangondor/__about__.py
+-rw-r--r--   0        0        0      111 2020-02-02 00:00:00.000000 djangondor-0.0.4/src/djangondor/__init__.py
+-rw-r--r--   0        0        0      645 2020-02-02 00:00:00.000000 djangondor-0.0.4/src/djangondor/collections.py
+-rw-r--r--   0        0        0     2800 2020-02-02 00:00:00.000000 djangondor-0.0.4/src/djangondor/requests.py
+-rw-r--r--   0        0        0      909 2020-02-02 00:00:00.000000 djangondor-0.0.4/src/djangondor/time.py
+-rw-r--r--   0        0        0        0 2020-02-02 00:00:00.000000 djangondor-0.0.4/src/djangondor/templatetags/__init__.py
+-rw-r--r--   0        0        0      410 2020-02-02 00:00:00.000000 djangondor-0.0.4/src/djangondor/templatetags/djangondor_collection_tags.py
+-rw-r--r--   0        0        0     1601 2020-02-02 00:00:00.000000 djangondor-0.0.4/src/djangondor/templatetags/djangondor_path_tags.py
+-rw-r--r--   0        0        0      111 2020-02-02 00:00:00.000000 djangondor-0.0.4/tests/__init__.py
+-rw-r--r--   0        0        0     3078 2020-02-02 00:00:00.000000 djangondor-0.0.4/.gitignore
+-rw-r--r--   0        0        0     1103 2020-02-02 00:00:00.000000 djangondor-0.0.4/LICENSE.txt
+-rw-r--r--   0        0        0     1888 2020-02-02 00:00:00.000000 djangondor-0.0.4/README.md
+-rw-r--r--   0        0        0     3150 2020-02-02 00:00:00.000000 djangondor-0.0.4/pyproject.toml
+-rw-r--r--   0        0        0     2804 2020-02-02 00:00:00.000000 djangondor-0.0.4/PKG-INFO
```

### Comparing `djangondor-0.0.3/src/djangondor/collections.py` & `djangondor-0.0.4/src/djangondor/collections.py`

 * *Files identical despite different names*

### Comparing `djangondor-0.0.3/src/djangondor/requests.py` & `djangondor-0.0.4/src/djangondor/requests.py`

 * *Files identical despite different names*

### Comparing `djangondor-0.0.3/src/djangondor/time.py` & `djangondor-0.0.4/src/djangondor/time.py`

 * *Files identical despite different names*

### Comparing `djangondor-0.0.3/src/djangondor/templatetags/djangondor_path_tags.py` & `djangondor-0.0.4/src/djangondor/templatetags/djangondor_path_tags.py`

 * *Files identical despite different names*

### Comparing `djangondor-0.0.3/.gitignore` & `djangondor-0.0.4/.gitignore`

 * *Files identical despite different names*

### Comparing `djangondor-0.0.3/LICENSE.txt` & `djangondor-0.0.4/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `djangondor-0.0.3/README.md` & `djangondor-0.0.4/README.md`

 * *Files 17% similar despite different names*

```diff
@@ -16,28 +16,30 @@
 
 ```console
 pip install djangondor
 ```
 
 ## Functions
 
-### dict_values
+### Collections package
+
+#### dict_values
 
 > dict_values can be used to access data in a dict as a tuple
 
 ```python
 
 from djangondor.collections import dict_values
 
 data = {'name':'Joseph','age':30,'height':1.7}
 name, height = dict_values(data,'name','height')
 
 ```
 
-### value_list
+#### value_list
 
 > Complements the builtin `Queryset.values_list` returning one data item per entry in the list. However, it only allows you to retrieve one field per item in the queryset.
 
 ```python
 from djangondor.collections import value_list
 
 queryset = User.objects.all()
@@ -47,28 +49,36 @@
 
 
 
 ```
 
 ## Templatetags
 
-## Path tags
+### Path tags
 
 ```html
 {% load djangondor_path_tags%}
 
 <a href="{% url 'index:index'  %}" class="{% active_app 'index'%}">Index App</a>
 
 
 
 <a href="{% url 'index:home'  %}" class="{% active_path 'home'%}">Home</a>
 <a href="{% url 'index:about'  %}" class="{% active_path 'about'%}">About</a>
 
 <a href="{% url 'index:settings'  %}" class="{% active_path_in 'home_settings' 'profile_settings' %}">Settings</a>
 
+<!-- Would produce the following if navigation matched 'index:home': -->
+
+<a href="/" class="active">Index App</a>
 
-```
 
 
+<a href="/" class="active">Home</a>
+<a href="/about" class="">About</a>
+
+<a href="/settings" class="">Settings</a>
+```
+
 ## License
 
 `djangondor` is distributed under the terms of the [MIT](https://spdx.org/licenses/MIT.html) license.
```

#### html2text {}

```diff
@@ -1,18 +1,18 @@
 # djangondor [![PyPI - Version](https://img.shields.io/pypi/v/djangondor.svg)]
 (https://pypi.org/project/djangondor) [![PyPI - Python Version](https://
 img.shields.io/pypi/pyversions/djangondor.svg)](https://pypi.org/project/
 djangondor) ----- **Table of Contents** - [Installation](#installation) -
 [Template tags](#templatetags) - [Helper functions](#functions) - [License]
 (#license) ## Installation ```console pip install djangondor ``` ## Functions
-### dict_values > dict_values can be used to access data in a dict as a tuple
-```python from djangondor.collections import dict_values data = {'name':
-'Joseph','age':30,'height':1.7} name, height = dict_values
-(data,'name','height') ``` ### value_list > Complements the builtin
+### Collections package #### dict_values > dict_values can be used to access
+data in a dict as a tuple ```python from djangondor.collections import
+dict_values data = {'name':'Joseph','age':30,'height':1.7} name, height =
+dict_values(data,'name','height') ``` #### value_list > Complements the builtin
 `Queryset.values_list` returning one data item per entry in the list. However,
 it only allows you to retrieve one field per item in the queryset. ```python
 from djangondor.collections import value_list queryset = User.objects.all() #
 data would have => ['sam', 'musonda', 'waza', 'chilu'] data = value_list
-(queryset, 'first_name') ``` ## Templatetags ## Path tags ```html {% load
-djangondor_path_tags%} Index_App Home About Settings ``` ## License
-`djangondor` is distributed under the terms of the [MIT](https://spdx.org/
-licenses/MIT.html) license.
+(queryset, 'first_name') ``` ## Templatetags ### Path tags ```html {% load
+djangondor_path_tags%} Index_App Home About Settings  Index_App Home About
+Settings ``` ## License `djangondor` is distributed under the terms of the
+[MIT](https://spdx.org/licenses/MIT.html) license.
```

### Comparing `djangondor-0.0.3/pyproject.toml` & `djangondor-0.0.4/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -23,15 +23,15 @@
   "Programming Language :: Python :: 3.11",
   "Programming Language :: Python :: Implementation :: CPython",
   "Programming Language :: Python :: Implementation :: PyPy",
 ]
 dependencies = []
 
 [project.urls]
-Documentation = "https://github.com/unknown/djangondor#readme"
+Documentation = "https://github.com/dalitsosakala/djangondor#readme"
 Issues = "https://github.com/dalitsosakala/djangondor/issues"
 Source = "https://github.com/dalitsosakala/djangondor"
 
 [tool.hatch.version]
 path = "src/djangondor/__about__.py"
 
 [tool.hatch.envs.default]
```

### Comparing `djangondor-0.0.3/PKG-INFO` & `djangondor-0.0.4/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: djangondor
-Version: 0.0.3
-Project-URL: Documentation, https://github.com/unknown/djangondor#readme
+Version: 0.0.4
+Project-URL: Documentation, https://github.com/dalitsosakala/djangondor#readme
 Project-URL: Issues, https://github.com/dalitsosakala/djangondor/issues
 Project-URL: Source, https://github.com/dalitsosakala/djangondor
 Author-email: Dalitso Sakala <dalitso.1sc@gmail.com>
 License-Expression: MIT
 License-File: LICENSE.txt
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python
@@ -37,28 +37,30 @@
 
 ```console
 pip install djangondor
 ```
 
 ## Functions
 
-### dict_values
+### Collections package
+
+#### dict_values
 
 > dict_values can be used to access data in a dict as a tuple
 
 ```python
 
 from djangondor.collections import dict_values
 
 data = {'name':'Joseph','age':30,'height':1.7}
 name, height = dict_values(data,'name','height')
 
 ```
 
-### value_list
+#### value_list
 
 > Complements the builtin `Queryset.values_list` returning one data item per entry in the list. However, it only allows you to retrieve one field per item in the queryset.
 
 ```python
 from djangondor.collections import value_list
 
 queryset = User.objects.all()
@@ -68,28 +70,36 @@
 
 
 
 ```
 
 ## Templatetags
 
-## Path tags
+### Path tags
 
 ```html
 {% load djangondor_path_tags%}
 
 <a href="{% url 'index:index'  %}" class="{% active_app 'index'%}">Index App</a>
 
 
 
 <a href="{% url 'index:home'  %}" class="{% active_path 'home'%}">Home</a>
 <a href="{% url 'index:about'  %}" class="{% active_path 'about'%}">About</a>
 
 <a href="{% url 'index:settings'  %}" class="{% active_path_in 'home_settings' 'profile_settings' %}">Settings</a>
 
+<!-- Would produce the following if navigation matched 'index:home': -->
+
+<a href="/" class="active">Index App</a>
 
-```
 
 
+<a href="/" class="active">Home</a>
+<a href="/about" class="">About</a>
+
+<a href="/settings" class="">Settings</a>
+```
+
 ## License
 
 `djangondor` is distributed under the terms of the [MIT](https://spdx.org/licenses/MIT.html) license.
```

#### html2text {}

```diff
@@ -1,9 +1,9 @@
-Metadata-Version: 2.1 Name: djangondor Version: 0.0.3 Project-URL:
-Documentation, https://github.com/unknown/djangondor#readme Project-URL:
+Metadata-Version: 2.1 Name: djangondor Version: 0.0.4 Project-URL:
+Documentation, https://github.com/dalitsosakala/djangondor#readme Project-URL:
 Issues, https://github.com/dalitsosakala/djangondor/issues Project-URL: Source,
 https://github.com/dalitsosakala/djangondor Author-email: Dalitso Sakala
 1sc@gmail.com> License-Expression: MIT License-File: LICENSE.txt Classifier:
 Development Status :: 4 - Beta Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.7 Classifier: Programming
 Language :: Python :: 3.8 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10 Classifier: Programming
@@ -12,19 +12,19 @@
 Implementation :: PyPy Requires-Python: >=3.7 Description-Content-Type: text/
 markdown # djangondor [![PyPI - Version](https://img.shields.io/pypi/v/
 djangondor.svg)](https://pypi.org/project/djangondor) [![PyPI - Python Version]
 (https://img.shields.io/pypi/pyversions/djangondor.svg)](https://pypi.org/
 project/djangondor) ----- **Table of Contents** - [Installation](#installation)
 - [Template tags](#templatetags) - [Helper functions](#functions) - [License]
 (#license) ## Installation ```console pip install djangondor ``` ## Functions
-### dict_values > dict_values can be used to access data in a dict as a tuple
-```python from djangondor.collections import dict_values data = {'name':
-'Joseph','age':30,'height':1.7} name, height = dict_values
-(data,'name','height') ``` ### value_list > Complements the builtin
+### Collections package #### dict_values > dict_values can be used to access
+data in a dict as a tuple ```python from djangondor.collections import
+dict_values data = {'name':'Joseph','age':30,'height':1.7} name, height =
+dict_values(data,'name','height') ``` #### value_list > Complements the builtin
 `Queryset.values_list` returning one data item per entry in the list. However,
 it only allows you to retrieve one field per item in the queryset. ```python
 from djangondor.collections import value_list queryset = User.objects.all() #
 data would have => ['sam', 'musonda', 'waza', 'chilu'] data = value_list
-(queryset, 'first_name') ``` ## Templatetags ## Path tags ```html {% load
-djangondor_path_tags%} Index_App Home About Settings ``` ## License
-`djangondor` is distributed under the terms of the [MIT](https://spdx.org/
-licenses/MIT.html) license.
+(queryset, 'first_name') ``` ## Templatetags ### Path tags ```html {% load
+djangondor_path_tags%} Index_App Home About Settings  Index_App Home About
+Settings ``` ## License `djangondor` is distributed under the terms of the
+[MIT](https://spdx.org/licenses/MIT.html) license.
```

