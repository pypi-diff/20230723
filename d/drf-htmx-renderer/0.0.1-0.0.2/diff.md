# Comparing `tmp/drf-htmx-renderer-0.0.1.tar.gz` & `tmp/drf-htmx-renderer-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "drf-htmx-renderer-0.0.1.tar", last modified: Sat Jul 22 08:37:32 2023, max compression
+gzip compressed data, was "drf-htmx-renderer-0.0.2.tar", last modified: Sun Jul 23 10:14:46 2023, max compression
```

## Comparing `drf-htmx-renderer-0.0.1.tar` & `drf-htmx-renderer-0.0.2.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxrwxr-x   0 emma      (1001) emma      (1001)        0 2023-07-22 08:37:32.569811 drf-htmx-renderer-0.0.1/
--rw-rw-r--   0 emma      (1001) emma      (1001)     1078 2023-07-22 08:20:59.000000 drf-htmx-renderer-0.0.1/LICENSE
--rw-rw-r--   0 emma      (1001) emma      (1001)      847 2023-07-22 08:37:32.569811 drf-htmx-renderer-0.0.1/PKG-INFO
--rw-rw-r--   0 emma      (1001) emma      (1001)        0 2023-07-22 08:35:48.000000 drf-htmx-renderer-0.0.1/README.md
-drwxrwxr-x   0 emma      (1001) emma      (1001)        0 2023-07-22 08:37:32.565811 drf-htmx-renderer-0.0.1/drf_htmx_renderer.egg-info/
--rw-rw-r--   0 emma      (1001) emma      (1001)      847 2023-07-22 08:37:32.000000 drf-htmx-renderer-0.0.1/drf_htmx_renderer.egg-info/PKG-INFO
--rw-rw-r--   0 emma      (1001) emma      (1001)      513 2023-07-22 08:37:32.000000 drf-htmx-renderer-0.0.1/drf_htmx_renderer.egg-info/SOURCES.txt
--rw-rw-r--   0 emma      (1001) emma      (1001)        1 2023-07-22 08:37:32.000000 drf-htmx-renderer-0.0.1/drf_htmx_renderer.egg-info/dependency_links.txt
--rw-rw-r--   0 emma      (1001) emma      (1001)       38 2023-07-22 08:37:32.000000 drf-htmx-renderer-0.0.1/drf_htmx_renderer.egg-info/requires.txt
--rw-rw-r--   0 emma      (1001) emma      (1001)       14 2023-07-22 08:37:32.000000 drf-htmx-renderer-0.0.1/drf_htmx_renderer.egg-info/top_level.txt
-drwxrwxr-x   0 emma      (1001) emma      (1001)        0 2023-07-22 08:37:32.569811 drf-htmx-renderer-0.0.1/htmx_renderer/
--rw-rw-r--   0 emma      (1001) emma      (1001)        0 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.1/htmx_renderer/__init__.py
--rw-rw-r--   0 emma      (1001) emma      (1001)      318 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.1/htmx_renderer/adapters.py
--rw-rw-r--   0 emma      (1001) emma      (1001)       63 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.1/htmx_renderer/admin.py
--rw-rw-r--   0 emma      (1001) emma      (1001)      157 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.1/htmx_renderer/apps.py
--rw-rw-r--   0 emma      (1001) emma      (1001)      494 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.1/htmx_renderer/exception_handler.py
--rw-rw-r--   0 emma      (1001) emma      (1001)       57 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.1/htmx_renderer/models.py
--rw-rw-r--   0 emma      (1001) emma      (1001)     4892 2023-07-22 08:21:21.000000 drf-htmx-renderer-0.0.1/htmx_renderer/renderers.py
--rw-rw-r--   0 emma      (1001) emma      (1001)      157 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.1/htmx_renderer/routers.py
--rw-rw-r--   0 emma      (1001) emma      (1001)      797 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.1/htmx_renderer/serializers.py
--rw-rw-r--   0 emma      (1001) emma      (1001)       60 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.1/htmx_renderer/tests.py
--rw-rw-r--   0 emma      (1001) emma      (1001)     1695 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.1/htmx_renderer/views.py
--rw-rw-r--   0 emma      (1001) emma      (1001)       38 2023-07-22 08:37:32.569811 drf-htmx-renderer-0.0.1/setup.cfg
--rw-rw-r--   0 emma      (1001) emma      (1001)     1325 2023-07-22 08:37:05.000000 drf-htmx-renderer-0.0.1/setup.py
+drwxrwxr-x   0 emma      (1001) emma      (1001)        0 2023-07-23 10:14:46.695217 drf-htmx-renderer-0.0.2/
+-rw-rw-r--   0 emma      (1001) emma      (1001)     1078 2023-07-22 08:20:59.000000 drf-htmx-renderer-0.0.2/LICENSE
+-rw-rw-r--   0 emma      (1001) emma      (1001)     3852 2023-07-23 10:14:46.695217 drf-htmx-renderer-0.0.2/PKG-INFO
+-rw-rw-r--   0 emma      (1001) emma      (1001)     2975 2023-07-22 14:48:20.000000 drf-htmx-renderer-0.0.2/README.md
+drwxrwxr-x   0 emma      (1001) emma      (1001)        0 2023-07-23 10:14:46.691217 drf-htmx-renderer-0.0.2/drf_htmx_renderer.egg-info/
+-rw-rw-r--   0 emma      (1001) emma      (1001)     3852 2023-07-23 10:14:46.000000 drf-htmx-renderer-0.0.2/drf_htmx_renderer.egg-info/PKG-INFO
+-rw-rw-r--   0 emma      (1001) emma      (1001)      503 2023-07-23 10:14:46.000000 drf-htmx-renderer-0.0.2/drf_htmx_renderer.egg-info/SOURCES.txt
+-rw-rw-r--   0 emma      (1001) emma      (1001)        1 2023-07-23 10:14:46.000000 drf-htmx-renderer-0.0.2/drf_htmx_renderer.egg-info/dependency_links.txt
+-rw-rw-r--   0 emma      (1001) emma      (1001)       92 2023-07-23 10:14:46.000000 drf-htmx-renderer-0.0.2/drf_htmx_renderer.egg-info/requires.txt
+-rw-rw-r--   0 emma      (1001) emma      (1001)       14 2023-07-23 10:14:46.000000 drf-htmx-renderer-0.0.2/drf_htmx_renderer.egg-info/top_level.txt
+drwxrwxr-x   0 emma      (1001) emma      (1001)        0 2023-07-23 10:14:46.695217 drf-htmx-renderer-0.0.2/htmx_renderer/
+-rw-rw-r--   0 emma      (1001) emma      (1001)        0 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.2/htmx_renderer/__init__.py
+-rw-rw-r--   0 emma      (1001) emma      (1001)      318 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.2/htmx_renderer/adapters.py
+-rw-rw-r--   0 emma      (1001) emma      (1001)       63 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.2/htmx_renderer/admin.py
+-rw-rw-r--   0 emma      (1001) emma      (1001)      157 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.2/htmx_renderer/apps.py
+-rw-rw-r--   0 emma      (1001) emma      (1001)      494 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.2/htmx_renderer/exception_handler.py
+-rw-rw-r--   0 emma      (1001) emma      (1001)       57 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.2/htmx_renderer/models.py
+-rw-rw-r--   0 emma      (1001) emma      (1001)     6020 2023-07-22 14:48:20.000000 drf-htmx-renderer-0.0.2/htmx_renderer/renderers.py
+-rw-rw-r--   0 emma      (1001) emma      (1001)      797 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.2/htmx_renderer/serializers.py
+-rw-rw-r--   0 emma      (1001) emma      (1001)       60 2023-07-22 08:21:19.000000 drf-htmx-renderer-0.0.2/htmx_renderer/tests.py
+-rw-rw-r--   0 emma      (1001) emma      (1001)      564 2023-07-22 14:48:20.000000 drf-htmx-renderer-0.0.2/htmx_renderer/views.py
+-rw-rw-r--   0 emma      (1001) emma      (1001)     1122 2023-07-23 10:14:07.000000 drf-htmx-renderer-0.0.2/pyproject.toml
+-rw-rw-r--   0 emma      (1001) emma      (1001)       38 2023-07-23 10:14:46.695217 drf-htmx-renderer-0.0.2/setup.cfg
+-rw-rw-r--   0 emma      (1001) emma      (1001)       39 2023-07-22 09:40:29.000000 drf-htmx-renderer-0.0.2/setup.py
```

### Comparing `drf-htmx-renderer-0.0.1/LICENSE` & `drf-htmx-renderer-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `drf-htmx-renderer-0.0.1/htmx_renderer/renderers.py` & `drf-htmx-renderer-0.0.2/htmx_renderer/renderers.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import json
 import math
 
 from django.conf import settings
+from django.core.exceptions import ImproperlyConfigured
 from django.http import Http404
 from django.urls import reverse
 
 from rest_framework.pagination import PageNumberPagination
 from rest_framework.renderers import TemplateHTMLRenderer as DRFTemplateHTMLRenderer
 
 from drf_auto_endpoint.metadata import AutoMetadata
@@ -133,7 +134,41 @@
 
         partials = request.GET.get('partials', '').split(',')
         context['templates'] = {f'./partials/{p}.html': {'oob': bool(i)}
                                 for i, p in enumerate(partials)}
 
         return context
 
+    def get_template_names(self, response, view):
+        from rest_framework.routers import APIRootView
+
+        try:
+            return super().get_template_names(response, view)
+        except ImproperlyConfigured:
+            pass
+
+        if view.request.headers.get('Hx-Request', False):
+            if 'partials' in view.request.query_params:
+                return ['htmx/partial.html']
+            base_dir = 'htmx'
+        else:
+            base_dir = 'html'
+
+        if isinstance(view, APIRootView):
+            return [
+                f'{base_dir}/root.html',
+            ]
+
+        templates = [
+            f'{base_dir}/{view.endpoint.model.__module__}_{view.endpoint.model.__name__}_{view.action}.html',
+            f'{base_dir}/{view.endpoint.model.__name__}_{view.action}.html',
+            f'{base_dir}/{view.action}.html',
+        ]
+
+        if getattr(getattr(view, view.action), 'detail', False):
+            templates += [f'{base_dir}/retrieve.html', ]
+        else:
+            templates += [f'{base_dir}/list.html', ]
+
+        return templates
+
+
```

### Comparing `drf-htmx-renderer-0.0.1/htmx_renderer/serializers.py` & `drf-htmx-renderer-0.0.2/htmx_renderer/serializers.py`

 * *Files identical despite different names*

### Comparing `drf-htmx-renderer-0.0.1/setup.py` & `drf-htmx-renderer-0.0.2/pyproject.toml`

 * *Files 25% similar despite different names*

```diff
@@ -1,42 +1,40 @@
-import os
-from setuptools import setup
+[build-system]
+requires = ["setuptools>=61", "wheel"]
+build-backend = "setuptools.build_meta"
 
-with open(os.path.join(os.path.dirname(__file__), 'README.md')) as readme:
-    README = readme.read()
+[project]
+name = "drf-htmx-renderer"
+version = "0.0.2"
+description = "HTMX renderer for Django REST FRAMEWORK"
+authors = [
+    {name = "Emmanuelle Delescolle", email = "info@levit.be"},
+]
+dependencies = [
+    "Django>=3.2",
+    "drf-schema-adapter>=3.0.0",
+    "django-mathfilters>=1.0.0",
+    "django-bootstrap-v5>=1.0.11",
+]
+requires-python = ">=3.8"
+readme = "README.md"
+license = {text = "MIT License"}
+classifiers = [
+    "Environment :: Web Environment",
+    "Framework :: Django",
+    "Framework :: Django :: 3.2",
+    "Framework :: Django :: 4.2",
+    "Intended Audience :: Developers",
+    "License :: OSI Approved :: MIT License",
+    "Operating System :: OS Independent",
+    "Programming Language :: Python",
+    "Programming Language :: Python :: 3",
+    "Programming Language :: Python :: 3.10",
+    "Topic :: Internet :: WWW/HTTP",
+    "Topic :: Internet :: WWW/HTTP :: Dynamic Content",
+]
 
+[project.urls]
+Homepage = "https://github.com/nanuxbe/drf_htmx_renderer"
 
-# allow setup.py to be run from any path
-os.chdir(os.path.normpath(os.path.join(os.path.abspath(__file__), os.pardir)))
-
-setup(
-    name='drf-htmx-renderer',
-    version='0.0.1',
-    packages=['htmx_renderer', ],
-    include_package_data=True,
-    license='MIT License',
-    description='HTMX renderer for Django REST FRAMEWORK',
-    long_description_content_type="text/markdown",
-    long_description=README,
-    url='https://github.com/nanuxbe/drf_htmx_renderer',
-    author='Emmanuelle Delescolle',
-    author_email='info@levit.be',
-    classifiers=[
-        'Environment :: Web Environment',
-        'Framework :: Django',
-        'Framework :: Django :: 3.2',
-        'Framework :: Django :: 4.2',
-        'Intended Audience :: Developers',
-        'License :: OSI Approved :: MIT License',
-        'Operating System :: OS Independent',
-        'Programming Language :: Python',
-        'Programming Language :: Python :: 3',
-        'Programming Language :: Python :: 3.10',
-        'Topic :: Internet :: WWW/HTTP',
-        'Topic :: Internet :: WWW/HTTP :: Dynamic Content',
-    ],
-    install_requires=[
-        'Django>=3.2',
-        'drf-schema-adapter>=3.0.0',
-    ]
-)
-
+[tool.setuptools]
+packages = ["htmx_renderer"]
```

