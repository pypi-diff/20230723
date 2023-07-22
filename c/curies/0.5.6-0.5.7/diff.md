# Comparing `tmp/curies-0.5.6.tar.gz` & `tmp/curies-0.5.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "curies-0.5.6.tar", last modified: Sun Jul  2 15:23:44 2023, max compression
+gzip compressed data, was "curies-0.5.7.tar", last modified: Sat Jul 22 23:20:19 2023, max compression
```

## Comparing `curies-0.5.6.tar` & `curies-0.5.7.tar`

### file list

```diff
@@ -1,62 +1,62 @@
-drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-02 15:23:44.821307 curies-0.5.6/
--rw-r--r--   0 cthoyt     (501) staff       (20)     1076 2022-07-31 23:04:00.000000 curies-0.5.6/LICENSE
--rw-r--r--   0 cthoyt     (501) staff       (20)      394 2023-04-28 13:05:54.000000 curies-0.5.6/MANIFEST.in
--rw-r--r--   0 cthoyt     (501) staff       (20)    11777 2023-07-02 15:23:44.821477 curies-0.5.6/PKG-INFO
--rw-r--r--   0 cthoyt     (501) staff       (20)    10308 2023-05-05 11:46:12.000000 curies-0.5.6/README.md
-drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-02 15:23:44.793667 curies-0.5.6/docs/
-drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-02 15:23:44.797014 curies-0.5.6/docs/source/
-drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-02 15:23:44.808138 curies-0.5.6/docs/source/api/
--rw-r--r--   0 cthoyt     (501) staff       (20)     1864 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.Converter.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      101 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.DuplicatePrefixes.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      110 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.DuplicateURIPrefixes.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      107 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.DuplicateValueError.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)       86 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.Record.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)       64 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.chain.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      124 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.get_bioregistry_converter.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)       94 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.get_fastapi_app.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      103 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.get_fastapi_router.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)       88 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.get_flask_app.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      106 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.get_flask_blueprint.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)       97 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.get_go_converter.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      112 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.get_monarch_converter.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      100 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.get_obo_converter.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      130 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.get_prefixcommons_converter.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)       82 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.get_version.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      141 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.mapping_service.MappingServiceGraph.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      332 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.mapping_service.MappingServiceSPARQLProcessor.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      134 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.mapping_service.get_fastapi_mapping_app.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      119 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.mapping_service.get_fastapi_router.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      128 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.mapping_service.get_flask_mapping_app.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      146 2023-04-13 07:20:08.000000 curies-0.5.6/docs/source/api/curies.mapping_service.get_flask_mapping_blueprint.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)     7469 2023-07-02 15:23:43.000000 curies-0.5.6/docs/source/conf.py
--rw-r--r--   0 cthoyt     (501) staff       (20)     2538 2023-03-10 11:58:39.000000 curies-0.5.6/docs/source/index.rst
--rw-r--r--   0 cthoyt     (501) staff       (20)      377 2023-07-02 15:23:36.000000 curies-0.5.6/pyproject.toml
--rw-r--r--   0 cthoyt     (501) staff       (20)     2647 2023-07-02 15:23:44.822775 curies-0.5.6/setup.cfg
-drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-02 15:23:44.794270 curies-0.5.6/src/
-drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-02 15:23:44.813037 curies-0.5.6/src/curies/
--rw-r--r--   0 cthoyt     (501) staff       (20)     1015 2023-05-15 10:11:51.000000 curies-0.5.6/src/curies/__init__.py
--rw-r--r--   0 cthoyt     (501) staff       (20)      146 2023-02-21 22:19:21.000000 curies-0.5.6/src/curies/__main__.py
--rw-r--r--   0 cthoyt     (501) staff       (20)    44040 2023-07-02 08:04:48.000000 curies-0.5.6/src/curies/api.py
--rw-r--r--   0 cthoyt     (501) staff       (20)     5065 2023-04-13 07:17:14.000000 curies-0.5.6/src/curies/cli.py
-drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-02 15:23:44.817556 curies-0.5.6/src/curies/mapping_service/
--rw-r--r--   0 cthoyt     (501) staff       (20)     4478 2023-04-13 07:57:38.000000 curies-0.5.6/src/curies/mapping_service/__init__.py
--rw-r--r--   0 cthoyt     (501) staff       (20)     8224 2023-05-05 11:46:12.000000 curies-0.5.6/src/curies/mapping_service/api.py
--rw-r--r--   0 cthoyt     (501) staff       (20)     3343 2023-03-26 20:29:12.000000 curies-0.5.6/src/curies/mapping_service/rdflib_custom.py
--rw-r--r--   0 cthoyt     (501) staff       (20)     4637 2023-05-05 11:46:12.000000 curies-0.5.6/src/curies/mapping_service/utils.py
--rw-r--r--   0 cthoyt     (501) staff       (20)        1 2022-07-31 23:04:01.000000 curies-0.5.6/src/curies/py.typed
--rw-r--r--   0 cthoyt     (501) staff       (20)     2033 2023-03-04 12:32:17.000000 curies-0.5.6/src/curies/sources.py
--rw-r--r--   0 cthoyt     (501) staff       (20)      255 2023-07-02 15:23:43.000000 curies-0.5.6/src/curies/version.py
--rw-r--r--   0 cthoyt     (501) staff       (20)     9669 2023-07-02 15:23:36.000000 curies-0.5.6/src/curies/web.py
-drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-02 15:23:44.815203 curies-0.5.6/src/curies.egg-info/
--rw-r--r--   0 cthoyt     (501) staff       (20)    11777 2023-07-02 15:23:44.000000 curies-0.5.6/src/curies.egg-info/PKG-INFO
--rw-r--r--   0 cthoyt     (501) staff       (20)     1837 2023-07-02 15:23:44.000000 curies-0.5.6/src/curies.egg-info/SOURCES.txt
--rw-r--r--   0 cthoyt     (501) staff       (20)        1 2023-07-02 15:23:44.000000 curies-0.5.6/src/curies.egg-info/dependency_links.txt
--rw-r--r--   0 cthoyt     (501) staff       (20)        1 2022-07-31 23:04:24.000000 curies-0.5.6/src/curies.egg-info/not-zip-safe
--rw-r--r--   0 cthoyt     (501) staff       (20)      290 2023-07-02 15:23:44.000000 curies-0.5.6/src/curies.egg-info/requires.txt
--rw-r--r--   0 cthoyt     (501) staff       (20)        7 2023-07-02 15:23:44.000000 curies-0.5.6/src/curies.egg-info/top_level.txt
-drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-02 15:23:44.821037 curies-0.5.6/tests/
--rw-r--r--   0 cthoyt     (501) staff       (20)       56 2022-07-31 23:04:00.000000 curies-0.5.6/tests/__init__.py
--rw-r--r--   0 cthoyt     (501) staff       (20)    18891 2023-05-15 10:20:25.000000 curies-0.5.6/tests/test_api.py
--rw-r--r--   0 cthoyt     (501) staff       (20)     5198 2023-04-13 10:20:39.000000 curies-0.5.6/tests/test_federated_sparql.py
--rw-r--r--   0 cthoyt     (501) staff       (20)    13426 2023-04-13 07:57:38.000000 curies-0.5.6/tests/test_mapping_service.py
--rw-r--r--   0 cthoyt     (501) staff       (20)     3273 2023-07-02 15:23:36.000000 curies-0.5.6/tests/test_web.py
+drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-22 23:20:19.931929 curies-0.5.7/
+-rw-r--r--   0 cthoyt     (501) staff       (20)     1076 2022-07-31 23:04:00.000000 curies-0.5.7/LICENSE
+-rw-r--r--   0 cthoyt     (501) staff       (20)      394 2023-04-28 13:05:54.000000 curies-0.5.7/MANIFEST.in
+-rw-r--r--   0 cthoyt     (501) staff       (20)    11777 2023-07-22 23:20:19.932093 curies-0.5.7/PKG-INFO
+-rw-r--r--   0 cthoyt     (501) staff       (20)    10308 2023-05-05 11:46:12.000000 curies-0.5.7/README.md
+drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-22 23:20:19.903582 curies-0.5.7/docs/
+drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-22 23:20:19.907299 curies-0.5.7/docs/source/
+drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-22 23:20:19.919090 curies-0.5.7/docs/source/api/
+-rw-r--r--   0 cthoyt     (501) staff       (20)     1864 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.Converter.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      101 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.DuplicatePrefixes.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      110 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.DuplicateURIPrefixes.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      107 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.DuplicateValueError.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)       86 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.Record.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)       64 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.chain.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      124 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.get_bioregistry_converter.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)       94 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.get_fastapi_app.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      103 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.get_fastapi_router.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)       88 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.get_flask_app.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      106 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.get_flask_blueprint.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)       97 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.get_go_converter.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      112 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.get_monarch_converter.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      100 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.get_obo_converter.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      130 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.get_prefixcommons_converter.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)       82 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.get_version.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      141 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.mapping_service.MappingServiceGraph.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      332 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.mapping_service.MappingServiceSPARQLProcessor.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      134 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.mapping_service.get_fastapi_mapping_app.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      119 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.mapping_service.get_fastapi_router.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      128 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.mapping_service.get_flask_mapping_app.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      146 2023-04-13 07:20:08.000000 curies-0.5.7/docs/source/api/curies.mapping_service.get_flask_mapping_blueprint.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)     7469 2023-07-22 23:20:18.000000 curies-0.5.7/docs/source/conf.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)     2538 2023-03-10 11:58:39.000000 curies-0.5.7/docs/source/index.rst
+-rw-r--r--   0 cthoyt     (501) staff       (20)      377 2023-07-02 15:23:36.000000 curies-0.5.7/pyproject.toml
+-rw-r--r--   0 cthoyt     (501) staff       (20)     2647 2023-07-22 23:20:19.933249 curies-0.5.7/setup.cfg
+drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-22 23:20:19.904259 curies-0.5.7/src/
+drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-22 23:20:19.923356 curies-0.5.7/src/curies/
+-rw-r--r--   0 cthoyt     (501) staff       (20)     1015 2023-05-15 10:11:51.000000 curies-0.5.7/src/curies/__init__.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)      146 2023-02-21 22:19:21.000000 curies-0.5.7/src/curies/__main__.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)    44826 2023-07-22 23:17:39.000000 curies-0.5.7/src/curies/api.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)     5065 2023-04-13 07:17:14.000000 curies-0.5.7/src/curies/cli.py
+drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-22 23:20:19.928210 curies-0.5.7/src/curies/mapping_service/
+-rw-r--r--   0 cthoyt     (501) staff       (20)     4478 2023-04-13 07:57:38.000000 curies-0.5.7/src/curies/mapping_service/__init__.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)     8224 2023-05-05 11:46:12.000000 curies-0.5.7/src/curies/mapping_service/api.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)     3343 2023-03-26 20:29:12.000000 curies-0.5.7/src/curies/mapping_service/rdflib_custom.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)     4637 2023-05-05 11:46:12.000000 curies-0.5.7/src/curies/mapping_service/utils.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)        1 2022-07-31 23:04:01.000000 curies-0.5.7/src/curies/py.typed
+-rw-r--r--   0 cthoyt     (501) staff       (20)     2033 2023-03-04 12:32:17.000000 curies-0.5.7/src/curies/sources.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)      255 2023-07-22 23:20:18.000000 curies-0.5.7/src/curies/version.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)     9669 2023-07-02 15:23:36.000000 curies-0.5.7/src/curies/web.py
+drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-22 23:20:19.925889 curies-0.5.7/src/curies.egg-info/
+-rw-r--r--   0 cthoyt     (501) staff       (20)    11777 2023-07-22 23:20:19.000000 curies-0.5.7/src/curies.egg-info/PKG-INFO
+-rw-r--r--   0 cthoyt     (501) staff       (20)     1837 2023-07-22 23:20:19.000000 curies-0.5.7/src/curies.egg-info/SOURCES.txt
+-rw-r--r--   0 cthoyt     (501) staff       (20)        1 2023-07-22 23:20:19.000000 curies-0.5.7/src/curies.egg-info/dependency_links.txt
+-rw-r--r--   0 cthoyt     (501) staff       (20)        1 2022-07-31 23:04:24.000000 curies-0.5.7/src/curies.egg-info/not-zip-safe
+-rw-r--r--   0 cthoyt     (501) staff       (20)      290 2023-07-22 23:20:19.000000 curies-0.5.7/src/curies.egg-info/requires.txt
+-rw-r--r--   0 cthoyt     (501) staff       (20)        7 2023-07-22 23:20:19.000000 curies-0.5.7/src/curies.egg-info/top_level.txt
+drwxr-xr-x   0 cthoyt     (501) staff       (20)        0 2023-07-22 23:20:19.931445 curies-0.5.7/tests/
+-rw-r--r--   0 cthoyt     (501) staff       (20)       56 2022-07-31 23:04:00.000000 curies-0.5.7/tests/__init__.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)    19293 2023-07-22 23:17:39.000000 curies-0.5.7/tests/test_api.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)     5198 2023-04-13 10:20:39.000000 curies-0.5.7/tests/test_federated_sparql.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)    13426 2023-04-13 07:57:38.000000 curies-0.5.7/tests/test_mapping_service.py
+-rw-r--r--   0 cthoyt     (501) staff       (20)     3273 2023-07-02 15:23:36.000000 curies-0.5.7/tests/test_web.py
```

### Comparing `curies-0.5.6/LICENSE` & `curies-0.5.7/LICENSE`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/PKG-INFO` & `curies-0.5.7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: curies
-Version: 0.5.6
+Version: 0.5.7
 Summary: Idiomatic conversion between URIs and compact URIs (CURIEs).
 Home-page: https://github.com/cthoyt/curies
 Download-URL: https://github.com/cthoyt/curies/releases
 Author: Charles Tapley Hoyt
 Author-email: cthoyt@gmail.com
 Maintainer: Charles Tapley Hoyt
 Maintainer-email: cthoyt@gmail.com
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: curies Version: 0.5.6 Summary: Idiomatic conversion
+Metadata-Version: 2.1 Name: curies Version: 0.5.7 Summary: Idiomatic conversion
 between URIs and compact URIs (CURIEs). Home-page: https://github.com/cthoyt/
 curies Download-URL: https://github.com/cthoyt/curies/releases Author: Charles
 Tapley Hoyt Author-email: cthoyt@gmail.com Maintainer: Charles Tapley Hoyt
 Maintainer-email: cthoyt@gmail.com License: MIT Project-URL: Bug Tracker,
 https://github.com/cthoyt/curies/issues Project-URL: Source Code, https://
 github.com/cthoyt/curies Keywords: snekpack,cookiecutter,semantic web,compact
 uniform resource identifiers,uniform resource identifiers,curies Classifier:
```

### Comparing `curies-0.5.6/README.md` & `curies-0.5.7/README.md`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/docs/source/api/curies.Converter.rst` & `curies-0.5.7/docs/source/api/curies.Converter.rst`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/docs/source/conf.py` & `curies-0.5.7/docs/source/conf.py`

 * *Files 1% similar despite different names*

```diff
@@ -23,15 +23,15 @@
 # -- Project information -----------------------------------------------------
 
 project = "curies"
 copyright = f"{date.today().year}, Charles Tapley Hoyt"
 author = "Charles Tapley Hoyt"
 
 # The full version, including alpha/beta/rc tags.
-release = "0.5.6"
+release = "0.5.7"
 
 # The short X.Y version.
 parsed_version = re.match(
     "(?P<major>\d+)\.(?P<minor>\d+)\.(?P<patch>\d+)(?:-(?P<release>[0-9A-Za-z-]+(?:\.[0-9A-Za-z-]+)*))?(?:\+(?P<build>[0-9A-Za-z-]+(?:\.[0-9A-Za-z-]+)*))?",
     release,
 )
 version = parsed_version.expand("\g<major>.\g<minor>.\g<patch>")
```

### Comparing `curies-0.5.6/docs/source/index.rst` & `curies-0.5.7/docs/source/index.rst`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/setup.cfg` & `curies-0.5.7/setup.cfg`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = curies
-version = 0.5.6
+version = 0.5.7
 description = Idiomatic conversion between URIs and compact URIs (CURIEs).
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/cthoyt/curies
 download_url = https://github.com/cthoyt/curies/releases
 project_urls = 
 	Bug Tracker = https://github.com/cthoyt/curies/issues
```

### Comparing `curies-0.5.6/src/curies/__init__.py` & `curies-0.5.7/src/curies/__init__.py`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/src/curies/api.py` & `curies-0.5.7/src/curies/api.py`

 * *Files 1% similar despite different names*

```diff
@@ -206,14 +206,26 @@
 class DuplicatePrefixes(DuplicateValueError):
     """An error raised with constructing a converter with data containing duplicate prefixes."""
 
     def __str__(self) -> str:  # noqa:D105
         return f"Duplicate prefixes:\n{self._str()}"
 
 
+class ConversionError(ValueError):
+    """An error raised on conversion."""
+
+
+class ExpansionError(ConversionError):
+    """An error raised on expansion if the prefix can't be looked up."""
+
+
+class CompressionError(ConversionError):
+    """An error raised on expansion if the URI prefix can't be matched."""
+
+
 def _get_duplicate_uri_prefixes(records: List[Record]) -> List[Tuple[Record, Record, str]]:
     return [
         (record_1, record_2, uri_prefix)
         for record_1, record_2 in itt.combinations(records, 2)
         for uri_prefix, up2 in itt.product(record_1._all_uri_prefixes, record_2._all_uri_prefixes)
         if uri_prefix == up2
     ]
@@ -680,14 +692,21 @@
         """Get the set of prefixes covered by this converter."""
         return {record.prefix for record in self.records}
 
     def format_curie(self, prefix: str, identifier: str) -> str:
         """Format a prefix and identifier into a CURIE string."""
         return f"{prefix}{self.delimiter}{identifier}"
 
+    def compress_strict(self, uri: str) -> str:
+        """Compress a URI to a CURIE, and raise an error of not possible."""
+        rv = self.compress(uri)
+        if rv is None:
+            raise CompressionError(uri)
+        return rv
+
     def compress(self, uri: str) -> Optional[str]:
         """Compress a URI to a CURIE, if possible.
 
         :param uri:
             A string representing a valid uniform resource identifier (URI)
         :returns:
             A compact URI if this converter could find an appropriate URI prefix, otherwise none.
@@ -729,14 +748,21 @@
         try:
             value, prefix = self.trie.longest_prefix_item(uri)
         except KeyError:
             return None, None
         else:
             return ReferenceTuple(prefix, uri[len(value) :])
 
+    def expand_strict(self, curie: str) -> str:
+        """Expand a CURIE to a URI, and raise an error of not possible."""
+        rv = self.expand(curie)
+        if rv is None:
+            raise ExpansionError(curie)
+        return rv
+
     def expand(self, curie: str) -> Optional[str]:
         """Expand a CURIE to a URI, if possible.
 
         :param curie:
             A string representing a compact URI
         :returns:
             A URI if this converter contains a URI prefix for the prefix in this CURIE
```

### Comparing `curies-0.5.6/src/curies/cli.py` & `curies-0.5.7/src/curies/cli.py`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/src/curies/mapping_service/__init__.py` & `curies-0.5.7/src/curies/mapping_service/__init__.py`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/src/curies/mapping_service/api.py` & `curies-0.5.7/src/curies/mapping_service/api.py`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/src/curies/mapping_service/rdflib_custom.py` & `curies-0.5.7/src/curies/mapping_service/rdflib_custom.py`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/src/curies/mapping_service/utils.py` & `curies-0.5.7/src/curies/mapping_service/utils.py`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/src/curies/sources.py` & `curies-0.5.7/src/curies/sources.py`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/src/curies/web.py` & `curies-0.5.7/src/curies/web.py`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/src/curies.egg-info/PKG-INFO` & `curies-0.5.7/src/curies.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: curies
-Version: 0.5.6
+Version: 0.5.7
 Summary: Idiomatic conversion between URIs and compact URIs (CURIEs).
 Home-page: https://github.com/cthoyt/curies
 Download-URL: https://github.com/cthoyt/curies/releases
 Author: Charles Tapley Hoyt
 Author-email: cthoyt@gmail.com
 Maintainer: Charles Tapley Hoyt
 Maintainer-email: cthoyt@gmail.com
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: curies Version: 0.5.6 Summary: Idiomatic conversion
+Metadata-Version: 2.1 Name: curies Version: 0.5.7 Summary: Idiomatic conversion
 between URIs and compact URIs (CURIEs). Home-page: https://github.com/cthoyt/
 curies Download-URL: https://github.com/cthoyt/curies/releases Author: Charles
 Tapley Hoyt Author-email: cthoyt@gmail.com Maintainer: Charles Tapley Hoyt
 Maintainer-email: cthoyt@gmail.com License: MIT Project-URL: Bug Tracker,
 https://github.com/cthoyt/curies/issues Project-URL: Source Code, https://
 github.com/cthoyt/curies Keywords: snekpack,cookiecutter,semantic web,compact
 uniform resource identifiers,uniform resource identifiers,curies Classifier:
```

### Comparing `curies-0.5.6/src/curies.egg-info/SOURCES.txt` & `curies-0.5.7/src/curies.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/tests/test_api.py` & `curies-0.5.7/tests/test_api.py`

 * *Files 2% similar despite different names*

```diff
@@ -9,17 +9,19 @@
 from tempfile import TemporaryDirectory
 
 import pandas as pd
 import rdflib
 from bioregistry.export.prefix_maps import EXTENDED_PREFIX_MAP_PATH
 
 from curies.api import (
+    CompressionError,
     Converter,
     DuplicatePrefixes,
     DuplicateURIPrefixes,
+    ExpansionError,
     Record,
     Reference,
     ReferenceTuple,
     chain,
 )
 from curies.sources import (
     BIOREGISTRY_CONTEXTS,
@@ -109,18 +111,25 @@
         self.assertIn("http://purl.obolibrary.org/obo/GO_", converter.reverse_prefix_map)
         self.assertIn("http://purl.obolibrary.org/obo/GO_", converter.trie)
         for curie, uri in [
             ("CHEBI:1", "http://purl.obolibrary.org/obo/CHEBI_1"),
             ("OBO:unnamespaced", "http://purl.obolibrary.org/obo/unnamespaced"),
         ]:
             self.assertEqual(curie, converter.compress(uri))
+            self.assertEqual(curie, converter.compress_strict(uri))
             self.assertEqual(uri, converter.expand(curie))
+            self.assertEqual(uri, converter.expand_strict(curie))
 
         self.assertIsNone(converter.compress("http://example.org/missing:00000"))
+        with self.assertRaises(CompressionError):
+            converter.compress_strict("http://example.org/missing:00000")
+
         self.assertIsNone(converter.expand("missing:00000"))
+        with self.assertRaises(ExpansionError):
+            converter.expand_strict("missing:00000")
 
         self.assertLess(0, len(converter.records), msg="converter has no records")
         self.assertIsNone(converter.get_record("nope"))
         self.assertIsNone(converter.get_record("go"), msg="synonym lookup is not allowed here")
         record = converter.get_record("GO")
         self.assertIsNotNone(record, msg=f"records: {[r.prefix for r in converter.records]}")
         self.assertIsInstance(record, Record)
```

### Comparing `curies-0.5.6/tests/test_federated_sparql.py` & `curies-0.5.7/tests/test_federated_sparql.py`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/tests/test_mapping_service.py` & `curies-0.5.7/tests/test_mapping_service.py`

 * *Files identical despite different names*

### Comparing `curies-0.5.6/tests/test_web.py` & `curies-0.5.7/tests/test_web.py`

 * *Files identical despite different names*

