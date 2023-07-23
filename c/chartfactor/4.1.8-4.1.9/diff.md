# Comparing `tmp/chartfactor-4.1.8.tar.gz` & `tmp/chartfactor-4.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chartfactor-4.1.8.tar", last modified: Fri May 26 22:51:20 2023, max compression
+gzip compressed data, was "chartfactor-4.1.9.tar", last modified: Mon Jun  5 19:25:37 2023, max compression
```

## Comparing `chartfactor-4.1.8.tar` & `chartfactor-4.1.9.tar`

### file list

```diff
@@ -1,62 +1,62 @@
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:20.460125 chartfactor-4.1.8/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    10759 2022-02-01 20:13:50.000000 chartfactor-4.1.8/LICENSE
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      333 2022-09-08 13:41:06.000000 chartfactor-4.1.8/MANIFEST.in
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1651 2023-05-26 22:51:20.460006 chartfactor-4.1.8/PKG-INFO
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1191 2022-09-08 13:41:06.000000 chartfactor-4.1.8/README.md
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:20.451379 chartfactor-4.1.8/chartfactor/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      373 2022-09-15 22:28:11.000000 chartfactor-4.1.8/chartfactor/__init__.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)       65 2022-02-01 20:13:50.000000 chartfactor-4.1.8/chartfactor/main.py
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:20.453979 chartfactor-4.1.8/chartfactor/src/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      432 2022-02-01 20:13:50.000000 chartfactor-4.1.8/chartfactor/src/__init__.py
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:20.454080 chartfactor-4.1.8/chartfactor/src/assets/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-01-24 20:09:31.000000 chartfactor-4.1.8/chartfactor/src/assets/__init__.py
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:20.454248 chartfactor-4.1.8/chartfactor/src/assets/css/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-01-24 20:09:31.000000 chartfactor-4.1.8/chartfactor/src/assets/css/__init__.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1291 2022-10-10 15:44:38.000000 chartfactor-4.1.8/chartfactor/src/assets/css/style.css
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:20.455653 chartfactor-4.1.8/chartfactor/src/assets/js/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-01-24 20:09:31.000000 chartfactor-4.1.8/chartfactor/src/assets/js/__init__.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     2454 2022-09-08 13:41:06.000000 chartfactor-4.1.8/chartfactor/src/assets/js/cf-message-event-listener.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     6956 2022-06-22 21:03:10.000000 chartfactor-4.1.8/chartfactor/src/assets/js/execute-python.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      413 2022-09-08 13:41:06.000000 chartfactor-4.1.8/chartfactor/src/assets/js/jupyter-notebook-active-cell-change.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    23114 2022-09-15 22:28:11.000000 chartfactor-4.1.8/chartfactor/src/assets/js/kaggle-specs.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      348 2022-06-22 21:03:10.000000 chartfactor-4.1.8/chartfactor/src/assets/js/send-message.js
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     4643 2022-06-18 22:07:37.000000 chartfactor-4.1.8/chartfactor/src/attribute.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)       23 2023-05-26 22:51:11.000000 chartfactor-4.1.8/chartfactor/src/build_info.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    30554 2023-01-24 23:06:43.000000 chartfactor-4.1.8/chartfactor/src/cf.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    25377 2023-01-24 23:06:43.000000 chartfactor-4.1.8/chartfactor/src/code_generator.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     4552 2022-09-08 13:41:06.000000 chartfactor-4.1.8/chartfactor/src/color.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1119 2022-04-09 21:56:18.000000 chartfactor-4.1.8/chartfactor/src/column.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     5016 2022-04-09 21:56:18.000000 chartfactor-4.1.8/chartfactor/src/compare_metric.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     2025 2022-04-09 21:56:18.000000 chartfactor-4.1.8/chartfactor/src/field.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     3203 2022-04-09 21:56:18.000000 chartfactor-4.1.8/chartfactor/src/filter.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     2485 2022-04-09 21:56:18.000000 chartfactor-4.1.8/chartfactor/src/grid.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1291 2022-04-09 21:56:18.000000 chartfactor-4.1.8/chartfactor/src/legend.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1223 2022-04-09 21:56:18.000000 chartfactor-4.1.8/chartfactor/src/markline.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     4991 2022-04-09 21:56:18.000000 chartfactor-4.1.8/chartfactor/src/metric.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    96316 2023-01-24 23:06:43.000000 chartfactor-4.1.8/chartfactor/src/provider.py
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:20.456261 chartfactor-4.1.8/chartfactor/src/resources/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-01-03 21:38:09.000000 chartfactor-4.1.8/chartfactor/src/resources/__init__.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1062 2022-02-01 20:13:50.000000 chartfactor-4.1.8/chartfactor/src/resources/commons.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    45605 2022-06-22 21:03:10.000000 chartfactor-4.1.8/chartfactor/src/resources/constants.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     4190 2022-10-10 15:44:38.000000 chartfactor-4.1.8/chartfactor/src/resources/html_template.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      709 2022-06-22 21:03:10.000000 chartfactor-4.1.8/chartfactor/src/resources/static_files_manager.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1103 2022-04-09 21:56:18.000000 chartfactor-4.1.8/chartfactor/src/row.py
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:20.451907 chartfactor-4.1.8/chartfactor.egg-info/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1651 2023-05-26 22:51:20.000000 chartfactor-4.1.8/chartfactor.egg-info/PKG-INFO
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1561 2023-05-26 22:51:20.000000 chartfactor-4.1.8/chartfactor.egg-info/SOURCES.txt
--rw-r--r--   0 jorgealarcon   (501) staff       (20)        1 2023-05-26 22:51:20.000000 chartfactor-4.1.8/chartfactor.egg-info/dependency_links.txt
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      156 2023-05-26 22:51:20.000000 chartfactor-4.1.8/chartfactor.egg-info/requires.txt
--rw-r--r--   0 jorgealarcon   (501) staff       (20)       18 2023-05-26 22:51:20.000000 chartfactor-4.1.8/chartfactor.egg-info/top_level.txt
--rw-r--r--   0 jorgealarcon   (501) staff       (20)      103 2022-02-01 20:13:50.000000 chartfactor-4.1.8/pyproject.toml
--rw-r--r--   0 jorgealarcon   (501) staff       (20)       38 2023-05-26 22:51:20.460160 chartfactor-4.1.8/setup.cfg
--rw-r--r--   0 jorgealarcon   (501) staff       (20)     1014 2023-05-26 22:51:17.000000 chartfactor-4.1.8/setup.py
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:20.456760 chartfactor-4.1.8/tests/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-02-01 20:13:50.000000 chartfactor-4.1.8/tests/__init__.py
-drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-05-26 22:51:20.458628 chartfactor-4.1.8/tests/data/
--rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-02-01 20:13:50.000000 chartfactor-4.1.8/tests/data/__init__.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    51698 2022-02-01 20:13:50.000000 chartfactor-4.1.8/tests/data/get_visualization_js_code_data.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)  2109816 2022-09-29 23:56:38.000000 chartfactor-4.1.8/tests/data/provider_comparative_data.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)   562612 2023-01-24 23:06:43.000000 chartfactor-4.1.8/tests/data/provider_data.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)    54923 2022-02-01 20:13:50.000000 chartfactor-4.1.8/tests/test_get_visualization_js_code.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)   112750 2023-01-24 23:06:43.000000 chartfactor-4.1.8/tests/test_provider.py
--rw-r--r--   0 jorgealarcon   (501) staff       (20)   207185 2022-02-27 19:39:22.000000 chartfactor-4.1.8/tests/test_provider_comparative.py
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:25:37.364450 chartfactor-4.1.9/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    10759 2022-02-01 20:13:50.000000 chartfactor-4.1.9/LICENSE
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      333 2022-09-08 13:41:06.000000 chartfactor-4.1.9/MANIFEST.in
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1651 2023-06-05 19:25:37.364323 chartfactor-4.1.9/PKG-INFO
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1191 2022-09-08 13:41:06.000000 chartfactor-4.1.9/README.md
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:25:37.348769 chartfactor-4.1.9/chartfactor/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      373 2022-09-15 22:28:11.000000 chartfactor-4.1.9/chartfactor/__init__.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)       65 2022-02-01 20:13:50.000000 chartfactor-4.1.9/chartfactor/main.py
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:25:37.352956 chartfactor-4.1.9/chartfactor/src/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      432 2022-02-01 20:13:50.000000 chartfactor-4.1.9/chartfactor/src/__init__.py
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:25:37.353163 chartfactor-4.1.9/chartfactor/src/assets/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-01-24 20:09:31.000000 chartfactor-4.1.9/chartfactor/src/assets/__init__.py
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:25:37.353415 chartfactor-4.1.9/chartfactor/src/assets/css/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-01-24 20:09:31.000000 chartfactor-4.1.9/chartfactor/src/assets/css/__init__.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1291 2022-10-10 15:44:38.000000 chartfactor-4.1.9/chartfactor/src/assets/css/style.css
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:25:37.355025 chartfactor-4.1.9/chartfactor/src/assets/js/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-01-24 20:09:31.000000 chartfactor-4.1.9/chartfactor/src/assets/js/__init__.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     2454 2022-09-08 13:41:06.000000 chartfactor-4.1.9/chartfactor/src/assets/js/cf-message-event-listener.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     6956 2022-06-22 21:03:10.000000 chartfactor-4.1.9/chartfactor/src/assets/js/execute-python.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      413 2022-09-08 13:41:06.000000 chartfactor-4.1.9/chartfactor/src/assets/js/jupyter-notebook-active-cell-change.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    23114 2022-09-15 22:28:11.000000 chartfactor-4.1.9/chartfactor/src/assets/js/kaggle-specs.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      348 2022-06-22 21:03:10.000000 chartfactor-4.1.9/chartfactor/src/assets/js/send-message.js
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     4643 2022-06-18 22:07:37.000000 chartfactor-4.1.9/chartfactor/src/attribute.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)       23 2023-06-05 19:25:28.000000 chartfactor-4.1.9/chartfactor/src/build_info.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    30554 2023-01-24 23:06:43.000000 chartfactor-4.1.9/chartfactor/src/cf.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    25377 2023-01-24 23:06:43.000000 chartfactor-4.1.9/chartfactor/src/code_generator.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     4552 2022-09-08 13:41:06.000000 chartfactor-4.1.9/chartfactor/src/color.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1119 2022-04-09 21:56:18.000000 chartfactor-4.1.9/chartfactor/src/column.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     5016 2022-04-09 21:56:18.000000 chartfactor-4.1.9/chartfactor/src/compare_metric.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     2025 2022-04-09 21:56:18.000000 chartfactor-4.1.9/chartfactor/src/field.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     3203 2022-04-09 21:56:18.000000 chartfactor-4.1.9/chartfactor/src/filter.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     2485 2022-04-09 21:56:18.000000 chartfactor-4.1.9/chartfactor/src/grid.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1291 2022-04-09 21:56:18.000000 chartfactor-4.1.9/chartfactor/src/legend.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1223 2022-04-09 21:56:18.000000 chartfactor-4.1.9/chartfactor/src/markline.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     4991 2022-04-09 21:56:18.000000 chartfactor-4.1.9/chartfactor/src/metric.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    96316 2023-01-24 23:06:43.000000 chartfactor-4.1.9/chartfactor/src/provider.py
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:25:37.356358 chartfactor-4.1.9/chartfactor/src/resources/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-01-03 21:38:09.000000 chartfactor-4.1.9/chartfactor/src/resources/__init__.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1062 2022-02-01 20:13:50.000000 chartfactor-4.1.9/chartfactor/src/resources/commons.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    45605 2022-06-22 21:03:10.000000 chartfactor-4.1.9/chartfactor/src/resources/constants.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     4190 2022-10-10 15:44:38.000000 chartfactor-4.1.9/chartfactor/src/resources/html_template.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      709 2022-06-22 21:03:10.000000 chartfactor-4.1.9/chartfactor/src/resources/static_files_manager.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1103 2022-04-09 21:56:18.000000 chartfactor-4.1.9/chartfactor/src/row.py
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:25:37.349546 chartfactor-4.1.9/chartfactor.egg-info/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1651 2023-06-05 19:25:37.000000 chartfactor-4.1.9/chartfactor.egg-info/PKG-INFO
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1561 2023-06-05 19:25:37.000000 chartfactor-4.1.9/chartfactor.egg-info/SOURCES.txt
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)        1 2023-06-05 19:25:37.000000 chartfactor-4.1.9/chartfactor.egg-info/dependency_links.txt
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      156 2023-06-05 19:25:37.000000 chartfactor-4.1.9/chartfactor.egg-info/requires.txt
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)       18 2023-06-05 19:25:37.000000 chartfactor-4.1.9/chartfactor.egg-info/top_level.txt
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)      103 2022-02-01 20:13:50.000000 chartfactor-4.1.9/pyproject.toml
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)       38 2023-06-05 19:25:37.364483 chartfactor-4.1.9/setup.cfg
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)     1014 2023-06-05 19:25:34.000000 chartfactor-4.1.9/setup.py
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:25:37.357669 chartfactor-4.1.9/tests/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-02-01 20:13:50.000000 chartfactor-4.1.9/tests/__init__.py
+drwxr-xr-x   0 jorgealarcon   (501) staff       (20)        0 2023-06-05 19:25:37.362148 chartfactor-4.1.9/tests/data/
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)        0 2022-02-01 20:13:50.000000 chartfactor-4.1.9/tests/data/__init__.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    51698 2022-02-01 20:13:50.000000 chartfactor-4.1.9/tests/data/get_visualization_js_code_data.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)  2109816 2022-09-29 23:56:38.000000 chartfactor-4.1.9/tests/data/provider_comparative_data.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)   562612 2023-01-24 23:06:43.000000 chartfactor-4.1.9/tests/data/provider_data.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)    54923 2022-02-01 20:13:50.000000 chartfactor-4.1.9/tests/test_get_visualization_js_code.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)   112750 2023-01-24 23:06:43.000000 chartfactor-4.1.9/tests/test_provider.py
+-rw-r--r--   0 jorgealarcon   (501) staff       (20)   207185 2022-02-27 19:39:22.000000 chartfactor-4.1.9/tests/test_provider_comparative.py
```

### Comparing `chartfactor-4.1.8/LICENSE` & `chartfactor-4.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/PKG-INFO` & `chartfactor-4.1.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chartfactor
-Version: 4.1.8
+Version: 4.1.9
 Summary: Integrates ChartFactor with Jupyter Notebooks
 Home-page: https://github.com/Aktiun/chartfactor-py
 Author: Aktiun
 Author-email: juan.dominguez@aktiun.com
 Keywords: aktiun,jupyter,jupyterhub,jupyterlab,chartfactor-py
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
```

### Comparing `chartfactor-4.1.8/README.md` & `chartfactor-4.1.9/README.md`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/assets/css/style.css` & `chartfactor-4.1.9/chartfactor/src/assets/css/style.css`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/assets/js/cf-message-event-listener.js` & `chartfactor-4.1.9/chartfactor/src/assets/js/cf-message-event-listener.js`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/assets/js/execute-python.js` & `chartfactor-4.1.9/chartfactor/src/assets/js/execute-python.js`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/assets/js/kaggle-specs.js` & `chartfactor-4.1.9/chartfactor/src/assets/js/kaggle-specs.js`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/attribute.py` & `chartfactor-4.1.9/chartfactor/src/attribute.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/cf.py` & `chartfactor-4.1.9/chartfactor/src/cf.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/code_generator.py` & `chartfactor-4.1.9/chartfactor/src/code_generator.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/color.py` & `chartfactor-4.1.9/chartfactor/src/color.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/column.py` & `chartfactor-4.1.9/chartfactor/src/column.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/compare_metric.py` & `chartfactor-4.1.9/chartfactor/src/compare_metric.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/field.py` & `chartfactor-4.1.9/chartfactor/src/field.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/filter.py` & `chartfactor-4.1.9/chartfactor/src/filter.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/grid.py` & `chartfactor-4.1.9/chartfactor/src/grid.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/legend.py` & `chartfactor-4.1.9/chartfactor/src/legend.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/markline.py` & `chartfactor-4.1.9/chartfactor/src/markline.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/metric.py` & `chartfactor-4.1.9/chartfactor/src/metric.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/provider.py` & `chartfactor-4.1.9/chartfactor/src/provider.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/resources/commons.py` & `chartfactor-4.1.9/chartfactor/src/resources/commons.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/resources/constants.py` & `chartfactor-4.1.9/chartfactor/src/resources/constants.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/resources/html_template.py` & `chartfactor-4.1.9/chartfactor/src/resources/html_template.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/resources/static_files_manager.py` & `chartfactor-4.1.9/chartfactor/src/resources/static_files_manager.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor/src/row.py` & `chartfactor-4.1.9/chartfactor/src/row.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/chartfactor.egg-info/PKG-INFO` & `chartfactor-4.1.9/chartfactor.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chartfactor
-Version: 4.1.8
+Version: 4.1.9
 Summary: Integrates ChartFactor with Jupyter Notebooks
 Home-page: https://github.com/Aktiun/chartfactor-py
 Author: Aktiun
 Author-email: juan.dominguez@aktiun.com
 Keywords: aktiun,jupyter,jupyterhub,jupyterlab,chartfactor-py
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
```

### Comparing `chartfactor-4.1.8/chartfactor.egg-info/SOURCES.txt` & `chartfactor-4.1.9/chartfactor.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/setup.py` & `chartfactor-4.1.9/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 def readme():
     with open('README.md') as f:
         return f.read()
 
 
 setup(
     name='chartfactor',
-    version='4.1.8',
+    version='4.1.9',
     description='Integrates ChartFactor with Jupyter Notebooks',
     long_description=readme(),
     long_description_content_type='text/markdown',
     url='https://github.com/Aktiun/chartfactor-py',
     author='Aktiun',
     author_email='juan.dominguez@aktiun.com',
     packages=find_packages(),
@@ -21,15 +21,15 @@
         'pandas',
         'pandasql>=0.7.3',
         'pygeohash==1.2.0',
         'jsonschema>=3.2.0',
         'colorama>=0.4.4',
         'importlib-resources>=5.4.0',
         'tzlocal~=4.1',
-        'chartfactor-jlab-ext==4.1.8',
+        'chartfactor-jlab-ext==4.1.9',
     ],
     include_package_data=True,
     keywords=['aktiun', 'jupyter', 'jupyterhub', 'jupyterlab', 'chartfactor-py'],
     python_requires=">=3.7",
     classifiers=[
         "Programming Language :: Python :: 3",
         "Operating System :: OS Independent",
```

### Comparing `chartfactor-4.1.8/tests/data/get_visualization_js_code_data.py` & `chartfactor-4.1.9/tests/data/get_visualization_js_code_data.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/tests/data/provider_comparative_data.py` & `chartfactor-4.1.9/tests/data/provider_comparative_data.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/tests/data/provider_data.py` & `chartfactor-4.1.9/tests/data/provider_data.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/tests/test_get_visualization_js_code.py` & `chartfactor-4.1.9/tests/test_get_visualization_js_code.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/tests/test_provider.py` & `chartfactor-4.1.9/tests/test_provider.py`

 * *Files identical despite different names*

### Comparing `chartfactor-4.1.8/tests/test_provider_comparative.py` & `chartfactor-4.1.9/tests/test_provider_comparative.py`

 * *Files identical despite different names*

