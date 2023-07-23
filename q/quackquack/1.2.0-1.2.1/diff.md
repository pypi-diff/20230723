# Comparing `tmp/quackquack-1.2.0.tar.gz` & `tmp/quackquack-1.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "quackquack-1.2.0.tar", max compression
+gzip compressed data, was "quackquack-1.2.1.tar", max compression
```

## Comparing `quackquack-1.2.0.tar` & `quackquack-1.2.1.tar`

### file list

```diff
@@ -1,47 +1,46 @@
--rw-r--r--   0        0        0     2246 2023-01-24 13:51:39.251747 quackquack-1.2.0/pyproject.toml
--rw-r--r--   0        0        0      319 2023-01-24 09:58:18.095714 quackquack-1.2.0/qq/__init__.py
--rw-r--r--   0        0        0     1500 2023-01-24 09:58:18.095714 quackquack-1.2.0/qq/application.py
--rw-r--r--   0        0        0     1358 2023-01-24 09:58:18.095714 quackquack-1.2.0/qq/context.py
--rw-r--r--   0        0        0      599 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/errors.py
--rw-r--r--   0        0        0     2564 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/finder.py
--rw-r--r--   0        0        0     4021 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/initializers.py
--rw-r--r--   0        0        0     2106 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/injector.py
--rw-r--r--   0        0        0     1213 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugin.py
--rw-r--r--   0        0        0      679 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugin_container.py
--rw-r--r--   0        0        0       92 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/__init__.py
--rw-r--r--   0        0        0        0 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/celery/__init__.py
--rw-r--r--   0        0        0      493 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/celery/finder.py
--rw-r--r--   0        0        0      455 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/celery/plugin.py
--rw-r--r--   0        0        0      465 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/logging.py
--rw-r--r--   0        0        0      514 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/redis.py
--rw-r--r--   0        0        0     1979 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/settings.py
--rw-r--r--   0        0        0        0 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/sqlalchemy/__init__.py
--rw-r--r--   0        0        0     1248 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/sqlalchemy/alembic.py
--rw-r--r--   0        0        0      112 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/sqlalchemy/consts.py
--rw-r--r--   0        0        0      346 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/sqlalchemy/exceptions.py
--rw-r--r--   0        0        0     1358 2023-01-24 09:58:18.099048 quackquack-1.2.0/qq/plugins/sqlalchemy/injectors.py
--rw-r--r--   0        0        0     2055 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/sqlalchemy/plugin.py
--rw-r--r--   0        0        0        0 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/sqlalchemy/tests/__init__.py
--rw-r--r--   0        0        0      320 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/sqlalchemy/tests/test_exceptions.py
--rw-r--r--   0        0        0     4029 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/sqlalchemy/tests/test_plugin.py
--rw-r--r--   0        0        0        0 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/tests/__init__.py
--rw-r--r--   0        0        0      894 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/tests/test_logging.py
--rw-r--r--   0        0        0     1275 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/tests/test_redis.py
--rw-r--r--   0        0        0     4241 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/tests/test_settings.py
--rw-r--r--   0        0        0        0 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/tornado/__init__.py
--rw-r--r--   0        0        0      524 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/tornado/application.py
--rw-r--r--   0        0        0      787 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/tornado/plugin.py
--rw-r--r--   0        0        0       31 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/plugins/types.py
--rw-r--r--   0        0        0      291 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/testing.py
--rw-r--r--   0        0        0        0 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/tests/__init__.py
--rw-r--r--   0        0        0     2000 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/tests/test_configurator.py
--rw-r--r--   0        0        0     3108 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/tests/test_context_manager.py
--rw-r--r--   0        0        0     4794 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/tests/test_finder.py
--rw-r--r--   0        0        0     6538 2023-01-24 09:58:18.102381 quackquack-1.2.0/qq/tests/test_initializers.py
--rw-r--r--   0        0        0     2826 2023-01-24 09:58:18.105714 quackquack-1.2.0/qq/tests/test_injector_yield.py
--rw-r--r--   0        0        0      337 2023-01-24 09:58:18.105714 quackquack-1.2.0/qq/tests/test_plugin.py
--rw-r--r--   0        0        0     2427 2023-01-24 09:58:18.105714 quackquack-1.2.0/qq/tests/test_plugin_container.py
--rw-r--r--   0        0        0      149 2023-01-24 09:58:18.105714 quackquack-1.2.0/qq/types.py
--rw-r--r--   0        0        0     2494 2023-01-24 12:39:57.116265 quackquack-1.2.0/readme.rst
--rw-r--r--   0        0        0     3816 2023-01-27 13:35:36.837889 quackquack-1.2.0/setup.py
--rw-r--r--   0        0        0     3535 2023-01-27 13:35:36.838112 quackquack-1.2.0/PKG-INFO
+-rw-r--r--   0        0        0     2258 2023-07-23 15:52:57.749223 quackquack-1.2.1/pyproject.toml
+-rw-r--r--   0        0        0      319 2023-01-24 09:58:18.095714 quackquack-1.2.1/qq/__init__.py
+-rw-r--r--   0        0        0     1500 2023-01-24 09:58:18.095714 quackquack-1.2.1/qq/application.py
+-rw-r--r--   0        0        0     1358 2023-01-24 09:58:18.095714 quackquack-1.2.1/qq/context.py
+-rw-r--r--   0        0        0      599 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/errors.py
+-rw-r--r--   0        0        0     2564 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/finder.py
+-rw-r--r--   0        0        0     4021 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/initializers.py
+-rw-r--r--   0        0        0     2106 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/injector.py
+-rw-r--r--   0        0        0     1213 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugin.py
+-rw-r--r--   0        0        0      679 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugin_container.py
+-rw-r--r--   0        0        0       92 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/__init__.py
+-rw-r--r--   0        0        0        0 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/celery/__init__.py
+-rw-r--r--   0        0        0      493 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/celery/finder.py
+-rw-r--r--   0        0        0      455 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/celery/plugin.py
+-rw-r--r--   0        0        0      465 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/logging.py
+-rw-r--r--   0        0        0      514 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/redis.py
+-rw-r--r--   0        0        0     1979 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/settings.py
+-rw-r--r--   0        0        0        0 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/sqlalchemy/__init__.py
+-rw-r--r--   0        0        0     1248 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/sqlalchemy/alembic.py
+-rw-r--r--   0        0        0      112 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/sqlalchemy/consts.py
+-rw-r--r--   0        0        0      346 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/sqlalchemy/exceptions.py
+-rw-r--r--   0        0        0     1358 2023-01-24 09:58:18.099048 quackquack-1.2.1/qq/plugins/sqlalchemy/injectors.py
+-rw-r--r--   0        0        0     2055 2023-03-19 23:25:09.016498 quackquack-1.2.1/qq/plugins/sqlalchemy/plugin.py
+-rw-r--r--   0        0        0        0 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/plugins/sqlalchemy/tests/__init__.py
+-rw-r--r--   0        0        0      320 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/plugins/sqlalchemy/tests/test_exceptions.py
+-rw-r--r--   0        0        0     4029 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/plugins/sqlalchemy/tests/test_plugin.py
+-rw-r--r--   0        0        0        0 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/plugins/tests/__init__.py
+-rw-r--r--   0        0        0      894 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/plugins/tests/test_logging.py
+-rw-r--r--   0        0        0     1275 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/plugins/tests/test_redis.py
+-rw-r--r--   0        0        0     4241 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/plugins/tests/test_settings.py
+-rw-r--r--   0        0        0        0 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/plugins/tornado/__init__.py
+-rw-r--r--   0        0        0      524 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/plugins/tornado/application.py
+-rw-r--r--   0        0        0      787 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/plugins/tornado/plugin.py
+-rw-r--r--   0        0        0       31 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/plugins/types.py
+-rw-r--r--   0        0        0      291 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/testing.py
+-rw-r--r--   0        0        0        0 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/tests/__init__.py
+-rw-r--r--   0        0        0     2000 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/tests/test_configurator.py
+-rw-r--r--   0        0        0     3108 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/tests/test_context_manager.py
+-rw-r--r--   0        0        0     4794 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/tests/test_finder.py
+-rw-r--r--   0        0        0     6538 2023-01-24 09:58:18.102381 quackquack-1.2.1/qq/tests/test_initializers.py
+-rw-r--r--   0        0        0     2826 2023-01-24 09:58:18.105714 quackquack-1.2.1/qq/tests/test_injector_yield.py
+-rw-r--r--   0        0        0      337 2023-01-24 09:58:18.105714 quackquack-1.2.1/qq/tests/test_plugin.py
+-rw-r--r--   0        0        0     2427 2023-01-24 09:58:18.105714 quackquack-1.2.1/qq/tests/test_plugin_container.py
+-rw-r--r--   0        0        0      149 2023-01-24 09:58:18.105714 quackquack-1.2.1/qq/types.py
+-rw-r--r--   0        0        0     2494 2023-01-24 12:39:57.116265 quackquack-1.2.1/readme.rst
+-rw-r--r--   0        0        0     3594 1970-01-01 00:00:00.000000 quackquack-1.2.1/PKG-INFO
```

### Comparing `quackquack-1.2.0/pyproject.toml` & `quackquack-1.2.1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,29 +1,29 @@
 [tool.poetry]
 name = "quackquack"
-version = "1.2.0"
-description = "Quack Quack: A simple application framework"
+version = "1.2.1"
+description = "Quack Quack: A simple application initializator"
 authors = ["Dominik Dlugajczyk <msocek@gmail.com>"]
 license = "MIT"
 packages = [{ include="qq", from="." },]
 readme = "readme.rst"
 homepage = "https://github.com/socek/quackquack"
 
 [tool.poetry.dependencies]
 python = "^3.8"
 alembic = { version = "^1.0.9", optional = true }
 sqlalchemy = { version = "^1.3.3", optional = true }
-redis = { version = "^3.2.1", optional = true }
+redis = { version = ">=3.2.1,<5.0.0", optional = true }
 celery = { version = ">=5.2.2", optional = true }
 python-dateutil = "^2.8.2"
 
 [tool.poetry.dev-dependencies]
 pytest-cov = { version = "^2.10.1" }
 pytest-mock = { version = "^3.2.0" }
-ipython = { version = "^7.31.1" }
+ipython = { version = "^8.10.0" }
 ipdb = { version = "^0.13.3" }
 icecream = { version = "^2.1.1" }
 pytest_async = "^0.1.1"
 pytest-asyncio = "^0.17.2"
 pytest = {version = "^7.0.1", extras = ["toml"]}
 
 [tool.poetry.extras]
```

### Comparing `quackquack-1.2.0/qq/application.py` & `quackquack-1.2.1/qq/application.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/context.py` & `quackquack-1.2.1/qq/context.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/errors.py` & `quackquack-1.2.1/qq/errors.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/finder.py` & `quackquack-1.2.1/qq/finder.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/initializers.py` & `quackquack-1.2.1/qq/initializers.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/injector.py` & `quackquack-1.2.1/qq/injector.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugin.py` & `quackquack-1.2.1/qq/plugin.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugin_container.py` & `quackquack-1.2.1/qq/plugin_container.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugins/redis.py` & `quackquack-1.2.1/qq/plugins/redis.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugins/settings.py` & `quackquack-1.2.1/qq/plugins/settings.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugins/sqlalchemy/alembic.py` & `quackquack-1.2.1/qq/plugins/sqlalchemy/alembic.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugins/sqlalchemy/injectors.py` & `quackquack-1.2.1/qq/plugins/sqlalchemy/injectors.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugins/sqlalchemy/plugin.py` & `quackquack-1.2.1/qq/plugins/sqlalchemy/plugin.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugins/sqlalchemy/tests/test_plugin.py` & `quackquack-1.2.1/qq/plugins/sqlalchemy/tests/test_plugin.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugins/tests/test_logging.py` & `quackquack-1.2.1/qq/plugins/tests/test_logging.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugins/tests/test_redis.py` & `quackquack-1.2.1/qq/plugins/tests/test_redis.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugins/tests/test_settings.py` & `quackquack-1.2.1/qq/plugins/tests/test_settings.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugins/tornado/application.py` & `quackquack-1.2.1/qq/plugins/tornado/application.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/plugins/tornado/plugin.py` & `quackquack-1.2.1/qq/plugins/tornado/plugin.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/tests/test_configurator.py` & `quackquack-1.2.1/qq/tests/test_configurator.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/tests/test_context_manager.py` & `quackquack-1.2.1/qq/tests/test_context_manager.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/tests/test_finder.py` & `quackquack-1.2.1/qq/tests/test_finder.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/tests/test_initializers.py` & `quackquack-1.2.1/qq/tests/test_initializers.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/tests/test_injector_yield.py` & `quackquack-1.2.1/qq/tests/test_injector_yield.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/qq/tests/test_plugin_container.py` & `quackquack-1.2.1/qq/tests/test_plugin_container.py`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/readme.rst` & `quackquack-1.2.1/readme.rst`

 * *Files identical despite different names*

### Comparing `quackquack-1.2.0/PKG-INFO` & `quackquack-1.2.1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,31 +1,32 @@
 Metadata-Version: 2.1
 Name: quackquack
-Version: 1.2.0
-Summary: Quack Quack: A simple application framework
+Version: 1.2.1
+Summary: Quack Quack: A simple application initializator
 Home-page: https://github.com/socek/quackquack
 License: MIT
 Author: Dominik Dlugajczyk
 Author-email: msocek@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Provides-Extra: alembic
 Provides-Extra: celery
 Provides-Extra: developer
 Provides-Extra: redis
 Provides-Extra: sqlalchemy
-Requires-Dist: alembic (>=1.0.9,<2.0.0); extra == "alembic" or extra == "developer"
-Requires-Dist: celery (>=5.2.2); extra == "celery" or extra == "developer"
+Requires-Dist: alembic (>=1.0.9,<2.0.0) ; extra == "alembic" or extra == "developer"
+Requires-Dist: celery (>=5.2.2) ; extra == "celery" or extra == "developer"
 Requires-Dist: python-dateutil (>=2.8.2,<3.0.0)
-Requires-Dist: redis (>=3.2.1,<4.0.0); extra == "redis" or extra == "developer"
-Requires-Dist: sqlalchemy (>=1.3.3,<2.0.0); extra == "sqlalchemy" or extra == "developer"
+Requires-Dist: redis (>=3.2.1,<5.0.0) ; extra == "redis" or extra == "developer"
+Requires-Dist: sqlalchemy (>=1.3.3,<2.0.0) ; extra == "sqlalchemy" or extra == "developer"
 Description-Content-Type: text/x-rst
 
 About
 =====
 
 `Documentation <https://qqpy.org/>`_
```

