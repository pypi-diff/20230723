# Comparing `tmp/python-ndev-blizzardapi-0.0.5a0.tar.gz` & `tmp/python-ndev-blizzardapi-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "python-ndev-blizzardapi-0.0.5a0.tar", last modified: Sat Jul 15 13:33:02 2023, max compression
+gzip compressed data, was "python-ndev-blizzardapi-0.1.0.tar", last modified: Sun Jul 23 02:38:03 2023, max compression
```

## Comparing `python-ndev-blizzardapi-0.0.5a0.tar` & `python-ndev-blizzardapi-0.1.0.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxrwxrwx   0        0        0        0 2023-07-15 13:33:02.947970 python-ndev-blizzardapi-0.0.5a0/
--rw-rw-rw-   0        0        0      134 2023-07-14 20:43:22.000000 python-ndev-blizzardapi-0.0.5a0/MANIFEST.in
--rw-rw-rw-   0        0        0     2311 2023-07-15 13:33:02.946972 python-ndev-blizzardapi-0.0.5a0/PKG-INFO
--rw-rw-rw-   0        0        0     1582 2023-07-14 18:06:48.000000 python-ndev-blizzardapi-0.0.5a0/README.md
-drwxrwxrwx   0        0        0        0 2023-07-15 13:33:02.912859 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/
--rw-rw-rw-   0        0        0      161 2023-03-11 02:36:09.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/__init__.py
--rw-rw-rw-   0        0        0     4981 2023-06-24 20:44:02.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/api.py
-drwxrwxrwx   0        0        0        0 2023-07-15 13:33:02.927924 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/battlenet/
--rw-rw-rw-   0        0        0       25 2023-03-10 03:36:02.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/battlenet/__init__.py
--rw-rw-rw-   0        0        0      458 2023-03-10 03:44:26.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/battlenet/battlenet_api.py
--rw-rw-rw-   0        0        0     1539 2023-03-10 03:47:42.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/battlenet/battlenet_oauth.py
--rw-rw-rw-   0        0        0      539 2023-06-21 18:46:57.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/blizzard_api.py
-drwxrwxrwx   0        0        0        0 2023-07-15 13:33:02.938451 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/tests/
--rw-rw-rw-   0        0        0        0 2023-06-21 22:10:25.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/tests/__init__.py
--rw-rw-rw-   0        0        0     1288 2023-06-22 00:13:18.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/tests/conftest.py
-drwxrwxrwx   0        0        0        0 2023-07-15 13:33:02.944970 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/
--rw-rw-rw-   0        0        0     2311 2023-07-15 13:33:02.000000 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      509 2023-07-15 13:33:02.000000 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-15 13:33:02.000000 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       17 2023-07-15 13:33:02.000000 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/requires.txt
--rw-rw-rw-   0        0        0       12 2023-07-15 13:33:02.000000 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-15 13:33:02.947970 python-ndev-blizzardapi-0.0.5a0/setup.cfg
--rw-rw-rw-   0        0        0     1010 2023-07-15 13:27:51.000000 python-ndev-blizzardapi-0.0.5a0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 02:38:03.559310 python-ndev-blizzardapi-0.1.0/
+-rw-rw-rw-   0        0        0      134 2023-07-14 20:43:22.000000 python-ndev-blizzardapi-0.1.0/MANIFEST.in
+-rw-rw-rw-   0        0        0     2335 2023-07-23 02:38:03.558315 python-ndev-blizzardapi-0.1.0/PKG-INFO
+-rw-rw-rw-   0        0        0     1608 2023-07-17 02:50:02.000000 python-ndev-blizzardapi-0.1.0/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 02:38:03.538451 python-ndev-blizzardapi-0.1.0/blizzardAPI/
+-rw-rw-rw-   0        0        0      161 2023-03-11 02:36:09.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/__init__.py
+-rw-rw-rw-   0        0        0     4981 2023-06-24 20:44:02.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/api.py
+drwxrwxrwx   0        0        0        0 2023-07-23 02:38:03.548733 python-ndev-blizzardapi-0.1.0/blizzardAPI/battlenet/
+-rw-rw-rw-   0        0        0       25 2023-03-10 03:36:02.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/battlenet/__init__.py
+-rw-rw-rw-   0        0        0      458 2023-03-10 03:44:26.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/battlenet/battlenet_api.py
+-rw-rw-rw-   0        0        0     1539 2023-03-10 03:47:42.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/battlenet/battlenet_oauth.py
+-rw-rw-rw-   0        0        0     1475 2023-07-17 03:21:51.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/blizzard_api.py
+drwxrwxrwx   0        0        0        0 2023-07-23 02:38:03.551752 python-ndev-blizzardapi-0.1.0/blizzardAPI/tests/
+-rw-rw-rw-   0        0        0        0 2023-06-21 22:10:25.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/tests/__init__.py
+-rw-rw-rw-   0        0        0     3330 2023-07-23 02:33:06.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/tests/conftest.py
+drwxrwxrwx   0        0        0        0 2023-07-23 02:38:03.556280 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/
+-rw-rw-rw-   0        0        0     2335 2023-07-23 02:38:03.000000 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      509 2023-07-23 02:38:03.000000 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 02:38:03.000000 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       38 2023-07-23 02:38:03.000000 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       12 2023-07-23 02:38:03.000000 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 02:38:03.559310 python-ndev-blizzardapi-0.1.0/setup.cfg
+-rw-rw-rw-   0        0        0     1037 2023-07-17 03:11:52.000000 python-ndev-blizzardapi-0.1.0/setup.py
```

### Comparing `python-ndev-blizzardapi-0.0.5a0/PKG-INFO` & `python-ndev-blizzardapi-0.1.0/README.md`

 * *Files 24% similar despite different names*

```diff
@@ -1,74 +1,33 @@
-Metadata-Version: 2.1
-Name: python-ndev-blizzardapi
-Version: 0.0.5a0
-Summary: Python module created to integrate your Python project with the Blizzard API
-Home-page: https://github.com/natanrmaia/python-ndev-blizzardapi
-Author: natanrmaia
-Author-email: contato@natanael.dev.br
-Project-URL: Documentation, https://python-ndev-blizzardapi.readthedocs.io/en/latest/
-Project-URL: Source, https://github.com/natanrmaia/python-ndev-blizzardapi
-Project-URL: Bug Reports, https://github.com/natanrmaia/python-ndev-blizzardapi/issues
-Classifier: Programming Language :: Python :: 3
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Operating System :: OS Independent
-Description-Content-Type: text/markdown
-
 # Python - NDEV Blizzard API
+This package is designed to make it easy to use the [Blizzard API](https://develop.battle.net/documentation) in Python. It handles authentication, the details of making requests, and receives the responses. It also provides a simple interface for accessing each of the API's features.
 
-Integration developed in Python to connect the Blizzard API.
+## Documentation
 
+- [Read the Docs](https://python-ndev-blizzardapi.readthedocs.io/)
 
 ## Author
 
 - [@natanrmaia](https://github.com/natanrmaia)
 
-
-## Support / Feedback
-
-For support / feedback, send email for contato@natanael.dev.br.
-
-
-## Reference
-
- - [Battle.Net Developer Portal](https://develop.battle.net/documentation)
-
-
-## API Documentation
-
-#### Settings
-
-| Parameter   | Type       | Description                           |
-| :---------- | :--------- | :---------------------------------- |
-| `client_id` | `string` | **Required**. Check Blizzard's documentation for more information. |
-| `client_secret` | `string` | **Required**. Check Blizzard's documentation for more information. |
-
 ## Instalation
 ```python
   pip install python-ndev-blizzardapi
 ```
 
-## Usage Example
-```python
-  from blizzardAPI import BlizzardAPI
-  
-  api = BlizzardAPI(client_id, client_secret)
-  api.bnet.oauth.get_user_info("us","imagine_token_here")
-```
-
 ## Blizzard APIs Supported
 
 | API                     | Items           | Obs                   |
 | :---------------------- | :-------------- | :-------------------- |
 | **Battle.Net**          | OAuth API       | All Regions supported |
 | **World Of Warcraft**   | Game Data API   | _Profile Data API in development_ |
 
+## Report or Request
+- [Bug Report](https://github.com/natanrmaia/python-ndev-blizzardapi/issues/new?assignees=&labels=&projects=&template=bug_report.md&title=)
+- [Feature request](https://github.com/natanrmaia/python-ndev-blizzardapi/issues/new?assignees=&labels=&projects=&template=feature_request.md&title=)
+- [Report a security vulnerability](https://github.com/natanrmaia/python-ndev-blizzardapi/issues/new?assignees=&labels=&projects=&template=feature_request.md&title=)
+- [Other questions](https://github.com/natanrmaia/python-ndev-blizzardapi/issues/new/choose)
+- [Email - contato@natanael.dev.br](mailto:contato@natanael.dev.br)
 
-## Tests using PyTest
-To perform the tests using PyTest, I recommend using the dotenv module. Read more in the documentation provided below.
-```cmd
-pytest blizzardAPI
-```
-
-## Documentation
+## Reference
 
-[Read the Docs](https://python-ndev-blizzardapi.readthedocs.io/)
+ - [Battle.Net Developer Portal](https://develop.battle.net/documentation)
```

### Comparing `python-ndev-blizzardapi-0.0.5a0/blizzardAPI/api.py` & `python-ndev-blizzardapi-0.1.0/blizzardAPI/api.py`

 * *Files identical despite different names*

### Comparing `python-ndev-blizzardapi-0.0.5a0/blizzardAPI/battlenet/battlenet_oauth.py` & `python-ndev-blizzardapi-0.1.0/blizzardAPI/battlenet/battlenet_oauth.py`

 * *Files identical despite different names*

### Comparing `python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/PKG-INFO` & `python-ndev-blizzardapi-0.1.0/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,74 +1,48 @@
 Metadata-Version: 2.1
 Name: python-ndev-blizzardapi
-Version: 0.0.5a0
+Version: 0.1.0
 Summary: Python module created to integrate your Python project with the Blizzard API
 Home-page: https://github.com/natanrmaia/python-ndev-blizzardapi
 Author: natanrmaia
 Author-email: contato@natanael.dev.br
 Project-URL: Documentation, https://python-ndev-blizzardapi.readthedocs.io/en/latest/
 Project-URL: Source, https://github.com/natanrmaia/python-ndev-blizzardapi
 Project-URL: Bug Reports, https://github.com/natanrmaia/python-ndev-blizzardapi/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Description-Content-Type: text/markdown
 
 # Python - NDEV Blizzard API
+This package is designed to make it easy to use the [Blizzard API](https://develop.battle.net/documentation) in Python. It handles authentication, the details of making requests, and receives the responses. It also provides a simple interface for accessing each of the API's features.
 
-Integration developed in Python to connect the Blizzard API.
+## Documentation
 
+- [Read the Docs](https://python-ndev-blizzardapi.readthedocs.io/)
 
 ## Author
 
 - [@natanrmaia](https://github.com/natanrmaia)
 
-
-## Support / Feedback
-
-For support / feedback, send email for contato@natanael.dev.br.
-
-
-## Reference
-
- - [Battle.Net Developer Portal](https://develop.battle.net/documentation)
-
-
-## API Documentation
-
-#### Settings
-
-| Parameter   | Type       | Description                           |
-| :---------- | :--------- | :---------------------------------- |
-| `client_id` | `string` | **Required**. Check Blizzard's documentation for more information. |
-| `client_secret` | `string` | **Required**. Check Blizzard's documentation for more information. |
-
 ## Instalation
 ```python
   pip install python-ndev-blizzardapi
 ```
 
-## Usage Example
-```python
-  from blizzardAPI import BlizzardAPI
-  
-  api = BlizzardAPI(client_id, client_secret)
-  api.bnet.oauth.get_user_info("us","imagine_token_here")
-```
-
 ## Blizzard APIs Supported
 
 | API                     | Items           | Obs                   |
 | :---------------------- | :-------------- | :-------------------- |
 | **Battle.Net**          | OAuth API       | All Regions supported |
 | **World Of Warcraft**   | Game Data API   | _Profile Data API in development_ |
 
+## Report or Request
+- [Bug Report](https://github.com/natanrmaia/python-ndev-blizzardapi/issues/new?assignees=&labels=&projects=&template=bug_report.md&title=)
+- [Feature request](https://github.com/natanrmaia/python-ndev-blizzardapi/issues/new?assignees=&labels=&projects=&template=feature_request.md&title=)
+- [Report a security vulnerability](https://github.com/natanrmaia/python-ndev-blizzardapi/issues/new?assignees=&labels=&projects=&template=feature_request.md&title=)
+- [Other questions](https://github.com/natanrmaia/python-ndev-blizzardapi/issues/new/choose)
+- [Email - contato@natanael.dev.br](mailto:contato@natanael.dev.br)
 
-## Tests using PyTest
-To perform the tests using PyTest, I recommend using the dotenv module. Read more in the documentation provided below.
-```cmd
-pytest blizzardAPI
-```
-
-## Documentation
+## Reference
 
-[Read the Docs](https://python-ndev-blizzardapi.readthedocs.io/)
+ - [Battle.Net Developer Portal](https://develop.battle.net/documentation)
```

### Comparing `python-ndev-blizzardapi-0.0.5a0/setup.py` & `python-ndev-blizzardapi-0.1.0/setup.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,15 +1,16 @@
 from setuptools import setup, find_packages
 
 setup(
     name="python-ndev-blizzardapi",
-    version="0.0.5-alpha",
+    version="0.1.0",
     packages=find_packages(),
     install_requires=[
         "requests>=2.28.2",
+        "python-dotenv>=1.0.0",
     ],
     author="natanrmaia",
     author_email="contato@natanael.dev.br",
     description="Python module created to integrate your Python project with the Blizzard API",
     long_description=open('README.md', 'r').read(),
     long_description_content_type='text/markdown',
     url="https://github.com/natanrmaia/python-ndev-blizzardapi",
```

